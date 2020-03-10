> この記事は[Sizeof](https://ja.wikipedia.org/wiki/Sizeof)から翻訳されています。


主に[Cと](../Page/C言語.md "wikilink")[C++](../Page/C++.md "wikilink")において、**`sizeof`**は、[データ型](https://ja.wikipedia.org/wiki/データ型 "wikilink")の大きさを求める[単項の](https://ja.wikipedia.org/wiki/単項演算 "wikilink")[演算子](../Page/演算子.md "wikilink")である。`sizeof`は原則として[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")時計算される演算子で、[式もしくは括弧でくくった型指定子を与えるとその大きさを](https://ja.wikipedia.org/wiki/式_\(プログラミング\) "wikilink")[バイト単位で返す](../Page/バイト_\(情報\).md "wikilink")。これは組込の数値型（[整数型](https://ja.wikipedia.org/wiki/整数型 "wikilink")や[浮動小数点数](../Page/浮動小数点数.md "wikilink")型）、[列挙型](../Page/列挙型.md "wikilink")、[ポインタ型](../Page/ポインタ_\(プログラミング\).md "wikilink")、利用者定義の複合データ型（[構造体](../Page/構造体.md "wikilink")、[共用体](https://ja.wikipedia.org/wiki/共用体 "wikilink")、C++の[クラス](../Page/クラス_\(コンピュータ\).md "wikilink")）まで全てのデータ型に対して使用できる。

## 必要性

多くのプログラムで、データ型の大きさがわかると便利な状況がある。最もよくある例としては[標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")の[`malloc`](https://ja.wikipedia.org/wiki/malloc "wikilink")などによる[動的メモリ確保](https://ja.wikipedia.org/wiki/動的メモリ確保 "wikilink")が挙げられる。組込型の大きさは処理系定義となっており、厳密な大きさは`sizeof (char)`が`1`であることを除いて標準に定められていない。次の例では10個の要素を持つ`int`型の[配列](../Page/配列.md "wikilink")を格納するのに十分なメモリを確保しようとしている。（処理系に依存したコードを書くつもりでなければ）`int`型の正確な大きさはわからないので`sizeof`が必要となる。

``` c
int *pointer; /*intへのポインタ型、メモリ確保したデータを参照する*/
pointer = malloc(sizeof (int) * 10);
```

このコードで、`malloc`は確保したメモリ領域へのポインタを返すが、その大きさはちょうど`int`型10個分になる。

一般的に、CとC++で型の大きさを仮定するのは安全でない。標準規格でも`char`以外の型がメモリ上で何バイト占めるかを規定していない。たとえば、16ビットシステムでの`int`型の大きさは通例2バイトであるが、大半の32ビットシステムでは`int`型の大きさは4バイトである。また、構造体や共用体では[アライメントもあり](https://ja.wikipedia.org/wiki/データ構造アライメント "wikilink")、ますます正確な大きさを求めるのは困難となる。そのようなこともあり、移植性の高いプログラムを書くには型の大きさを求めるために`sizeof`を使用することが推奨されている。

## CとC++

### 使用方法

`sizeof`演算子は、メモリ上に領域を占めるものであれば、ほとんどどどんなものに対しても使用できる。`sizeof`を使うには、キーワード`sizeof`の後に変数や[式あるいは括弧でくくった上で型名を書く](https://ja.wikipedia.org/wiki/式_\(プログラミング\) "wikilink")。変数や式の場合は、括弧でくくるかどうかは自由である。次の例では`int`型が`char`型の4倍のサイズを持つ実装の場合、`1, 4`と出力される（なお、`char`型に`sizeof`演算子を適用した結果は全ての実装において1でなければならない）。

``` c
// C99
char c;
printf("%zu, %zu", sizeof c, sizeof (int));
```

``` c
// Microsoft Visual C++
char c;
printf("%Iu, %Iu", sizeof c, sizeof (int));
```

``` c
// キャスト
char c;
printf("%lu, %lu", (unsigned long) sizeof c, (unsigned long) sizeof (int));
```

`sizeof`の結果は実装定義の符号無し整数型である[`size_t`](https://ja.wikipedia.org/wiki/size_t "wikilink")型となり、負数になることはない。

`sizeof`を関数型、[ビットフィールド](https://ja.wikipedia.org/wiki/ビットフィールド "wikilink")、不完全型（[後述](https://ja.wikipedia.org/wiki/#sizeofと不完全型 "wikilink")）に対して使用することはできない。

なお、[`printf`](https://ja.wikipedia.org/wiki/printf "wikilink")などで`size_t`型を書式出力する場合、[C99](../Page/C99.md "wikilink")で追加された長さ修飾子`z`を用いる。 C99に対応していない処理系では、引数をキャストするか、処理系依存の修飾子（たとえば[Microsoft Visual C++ならば修飾子](https://ja.wikipedia.org/wiki/Microsoft_Visual_C++ "wikilink")`I`）を用いる。

もし`%u`を使用すると、`size_t`型と`unsigned int`型のサイズが異なる環境において未定義動作となる。

#### 配列に対する`sizeof`

`sizeof`が[配列](../Page/配列.md "wikilink")型に使用されると、その配列がメモリ上に占める大きさが演算結果となる。配列の大きさは、要素の型の大きさに要素数をかけた値と規定されており、例えば`sizeof (T[8])`は`sizeof (T) * 8`と同じ値になる。逆に、配列`x`に対して、`sizeof x / sizeof x[0]`の演算により、配列の要素数を求めることが可能である。

次の例では、文字の複写時に[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")を起こさないよう、`sizeof`を配列の大きさを求めるために用いている。

``` c
/*sizeofを配列に使用する例*/
#include <stdio.h>
#include <string.h>

int main(void)
{
  char buffer[10]; /*要素数10のchar配列*/

  /* 標準入力から読み取った結果をbufferへ9文字までのみ複写する。
   *（sizeof (char)は常に1なので、sizeof buffer[0]で割る必要はない）
   */
  fgets(buffer, sizeof buffer, stdin);

  puts(buffer);
  return 0;
}
```

[C99](../Page/C99.md "wikilink")で[可変長配列](https://ja.wikipedia.org/wiki/可変長配列 "wikilink")に対して `sizeof`を適用する場合、配列の大きさは実行時に動的に計算され、コンパイル時定数にはならない。

#### `sizeof`と不完全型

`sizeof`は完全に定義されたデータ型のみに適用できる。配列なら、要素数が変数宣言に含まれていなければならず、構造体や共用体ならメンバが完全に定義されていなければならない。例えば次の二つのソースファイルがあったとする。

``` c
/* file1.c */
int arr[10];
struct x {int one; int two;};
```

``` c
/* file2.c */
extern int arr[];
struct x;
```

どちらのファイルも正しいCのソースであるものの、`file1.c`では`sizeof`を`arr`と`struct x`に使用できるが、`file2.c`では完全型でないため使用できない。`file2.c`では`arr`の要素数がわからず、`struct x`のメンバも分からないためである。`file2.c`で`arr`と`struct x`を`sizeof`で使用できるようにするには、`file2.c`の`arr`の宣言に要素数を指定したり、`struct x`の完全な宣言を書いたりする必要がある。

### 実装

コンパイラは言語の実装に適合するように、`sizeof`演算子をデータ型のメモリ上に占める大きさを結果とするように実装しなければならない。また（既述の例外を除いて）これはコンパイル時計算される演算子であり、[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")上では単なる[即値](https://ja.wikipedia.org/wiki/即値 "wikilink")になる。

#### 構造体のパディング

利用者定義型の大きさは[アライメントのためにメンバの大きさの合計よりも大きくなることが規格では許されている](https://ja.wikipedia.org/wiki/データ構造アライメント "wikilink")。次のコードは多くの環境において`8`と出力される。

``` c
struct student {
    char grade; /* charは1バイト */
    int age /* intは4バイト */
};

printf("%zu", sizeof (struct student));
```

この理由は、多くのコンパイラでは通常[ワード](../Page/ワード.md "wikilink")単位にデータを揃えるためであり、個々のメンバも境界を揃えられる。上の場合は、境界調整によってメンバ変数の`age`が次のワード単位に置かれるのである。このような構造体には境界調整のためにメンバ間やメンバの後ろに「パディング」と呼ばれる余分な隙間が置かれるのである。多くの[CPU](../Page/CPU.md "wikilink")ではデータがワード単位のメモリアドレスに置かれていた方が高速に読み書きでき、また中にはワード単位に揃えられていないと読み書きできないCPUもある\[1\]。

## D

[D言語](../Page/D言語.md "wikilink")では全ての型が持っている[プロパティ](../Page/プロパティ.md "wikilink")として`sizeof`が用意されている。

``` d
void main()
{
    writefln(int.sizeof);
}
```

## .NET

[.NET Frameworkでは](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、`Marshal.SizeOf`メソッド\[2\]によってオブジェクトのアンマネージサイズやアンマネージ型のサイズをバイト単位で取得可能である。.NET 4.5.1でジェネリックバージョンのオーバーロードが追加された。そのほか、各.NET言語に類似の組み込み言語機能が用意されていることがあるが、System.Booleanに対する演算結果など、必ずしも`Marshal.SizeOf`と同じ結果になるとは限らない。

### C++/CLI

[C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")の`sizeof`演算子はネイティブ型（基本型およびポインタ型）に用いる限りコンパイル時定数となり、基本的にC++と同じである。しかし値クラス（value class）型、（マネージ）ハンドル型や[ジェネリック型引数に対して用いられたときにはコンパイル時定数でなくなる](https://ja.wikipedia.org/wiki/総称型 "wikilink")。また参照クラス (ref class) 型やインターフェイス型に対して用いることはできない（不正となる）\[3\]。

### C\#

[C\#の](../Page/C_Sharp.md "wikilink")`sizeof`演算子は、アンマネージ型（組み込み型、列挙型、ポインタ型、参照型のフィールドやプロパティを含まないユーザー定義の構造体）のサイズをバイト単位で取得する。結果はint型となる。特定の組み込み型に対してsizeof演算子を用いた場合の結果はコンパイル時定数となるが、それ以外の型に使用した場合はコンパイル時定数とならない。また、sizeof演算子を使用するにはunsafeモードが必要だが、C\# 2.0以降は組み込み型に対するsizeofに関してのみunsafeが不要となった\[4\]。

## Visual Basic

[Visual Basicでは](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")、`Len`関数などが存在する。`Len`は文字列を引数に与えると文字列の長さを返すが、その他の型の変数を与えると変数の大きさを返す。

## ActiveBasic

[ActiveBasic](https://ja.wikipedia.org/wiki/ActiveBasic "wikilink")では、Visual Basicと同様の`Len`組込関数を持っているほか、`SizeOf`組込関数を持っている。`Len`は型名を指定することができないが、`SizeOf`は型名を指定できる。逆に`SizeOf`に変数や式を指定することはできない。

## 脚注

[Category:C言語](https://ja.wikipedia.org/wiki/Category:C言語 "wikilink") [Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink") [Category:プログラミング言語の演算子](https://ja.wikipedia.org/wiki/Category:プログラミング言語の演算子 "wikilink")

1.  Rentzsch, Jonathan. ["Data alignment: Straighten up and fly right."](http://www-128.ibm.com/developerworks/library/pa-dalign/#N100FE) www.ibm.com. 08 FEB 2005. Accessed 1 Oct 2006
2.  [Marshal.SizeOf Method (System.Runtime.InteropServices) | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/api/system.runtime.interopservices.marshal.sizeof?view=netframework-4.7)
3.  [Standard ECMA-372](http://www.ecma-international.org/publications/standards/Ecma-372.htm)
4.  [sizeof (C\# Reference) | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/sizeof)