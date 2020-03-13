> この記事は[Return](https://ja.wikipedia.org/wiki/Return)から翻訳されています。


**return文**（リターンぶん、）とは、[プログラミング言語](../Page/プログラミング言語.md "wikilink")における[文の一つである](https://ja.wikipedia.org/wiki/文_\(プログラミング\) "wikilink")。[goto文](https://ja.wikipedia.org/wiki/goto文 "wikilink")や[break文](https://ja.wikipedia.org/wiki/break文 "wikilink")、[continue文](https://ja.wikipedia.org/wiki/continue文 "wikilink")のようなジャンプ文 () に分類される。[サブルーチン](../Page/サブルーチン.md "wikilink")からの復帰に使われ、復帰と同時に[値を返すことができる](../Page/値_\(情報工学\).md "wikilink")。その値は**戻り値**（もどりち、）、**返り値**（かえりち）、**返却値**（へんきゃくち）あるいはそのまま**return値**（リターンち）などと呼ばれる。

## 言語別の意味や構文

### C/C++

[Cおよび](../Page/C言語.md "wikilink")[C++](../Page/C++.md "wikilink")において、return文とは、[関数を実行した結果や](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")、その処理が成功したかどうか等を示すデータを呼び出し元に渡すとともに、関数を終了させ呼び出し側に制御を戻す働きを持つ[文である](https://ja.wikipedia.org/wiki/文_\(プログラミング\) "wikilink")。return文によって関数の呼び出し元にデータを渡すことを、**値を返す**と言う。

return文によって返される値の[型は](../Page/データ型.md "wikilink")、関数の定義時や[プロトタイプ宣言](https://ja.wikipedia.org/wiki/プロトタイプ宣言 "wikilink")時に指定する。例えば、

``` c
int f();
```

という宣言は、関数 `f()` が `int` 型の値を返すことを表す。

return文の形式は

``` c
return 式;
```

または

``` c
return ;
```

のいずれかでなければならない。return文に式が伴う場合、その式の評価結果がreturn文の戻り値となる。この式は構文上省略可能であるが、[意味解析](https://ja.wikipedia.org/wiki/意味解析 "wikilink")の段階において、[C99](../Page/C99.md "wikilink")及びC++98では、戻り値の型が[void](https://ja.wikipedia.org/wiki/void_\(コンピュータ\) "wikilink")（値を返さない）と定義されている場合を除いて、式の省略はできない（C++では挙動が不定）と定められている（X3010 105頁 6.8.6.4、79頁6.6.3 2節参照）。

return文の式では、その式の結果の型が関数の戻り値の型へ暗黙的に[変換できなければならない](../Page/型変換.md "wikilink")（X3010 105頁 6.8.6.4、79頁6.6.3 2節参照）。

return文に遭遇しないまま関数の終わりまでプログラムが実行された場合、そこに式を省略した `return;` が行われたと見なされる。ただし、C99とC++98では、[main関数に限り](https://ja.wikipedia.org/wiki/エントリーポイント "wikilink")、そのmain関数の戻り値の型が `int` であれば `return 0;` があったと見なされる（X3010 9頁 5.1.2.2.3、X3014 35頁 3.6.1 5節参照）

戻り値の型が `void` である関数で式を指定することは、Cだと意味解析でできないとされているが、現在のC++では、結果がvoid型になる式であれば良いとされている（X3014 79頁 6.6.3 3節参照）。このため[テンプレートでより汎用性を持たせることが可能になっている](../Page/テンプレート_\(プログラミング\).md "wikilink")。

``` C++
template<typename T> T
func_call(T fn)
{
    return fn();
}
```

もし、テンプレート引数 `T` にint型を返す関数を与えてこの関数テンプレートfunc_callを実体化させると、概念的には次のようになる。

``` C++
//擬似コード
int func_call(int fn())
{
    return fn();
}
```

そして、戻り値の型が `void` の関数を与えると、やはり概念的には次のようになる。

``` C++
//擬似コード
void func_call(void fn())
{
    return fn();
}
```

ここで `fn()` の型は `void` になるが、`func_call` の戻り値の型も `void` であるため、もとの関数テンプレート `func_call` に戻り値の型が `void` の関数を与えてもコンパイル可能である。仮にこれが認められず、Cのように戻り値の型も `void` の関数内では、式を省略したreturn文しか許されないとすると、もとの `func_call` に対して次のような[特殊化を用意しなければならない](../Page/テンプレートの部分特殊化.md "wikilink")。

``` C++
template<>
void func_call(void (*fn)())
{
    fn();
}
```

一部の古いC++コンパイラでは、void型の式をreturnに書けず、実際にこのような対策を取る必要があった。なお、この特殊化では、関数オブジェクトを対象にしていない。

### Java

[Java](https://ja.wikipedia.org/wiki/Java "wikilink")において、return文とは、実行している[メソッド](https://ja.wikipedia.org/wiki/メソッド "wikilink")から抜け出すための文である。値を返してメソッドから抜け出す場合には、そのメソッドに適切な戻り値を設定しなければならない。C言語などと同様に、以下の2通りの構文が認められている。

  - 構文1

:

``` java
return ;
```

  - 構文2

:

``` java
return 式;
```

`void`を使って宣言されたメソッドや、[コンストラクタ](../Page/コンストラクタ.md "wikilink")、[ラムダ式](https://ja.wikipedia.org/wiki/ラムダ式 "wikilink")など\[1\]、メソッドの戻り値が無い（値を返さない）場合は構文1を用い、返す場合は構文2を用いる。構文1は省略可能であり、処理がメソッド末尾に到達した場合、暗黙的に呼び出し元へ制御が戻る。

### BASIC

[BASIC](../Page/BASIC.md "wikilink")、あるいは[Visual Basicのバージョン](../Page/Visual_Basic.md "wikilink")6までにおいて、return文とは、`gosub`によって飛んだ[サブルーチン](../Page/サブルーチン.md "wikilink")から、元の[メインルーチン](https://ja.wikipedia.org/wiki/メインルーチン "wikilink")へと戻る命令である。gosub元の行番号、もしくは構文の位置を記憶しておき、`return`と書かれた個所までプログラムの進行が辿り着くと、記憶していた次の命令もしくは行番号を読み、実行を続けていく。

BASICにおけるreturn文には、行番号を伴うものと伴わないものの2つがある。

  - 構文1

:

``` basic
return
```

  -
    例

:

``` basic
 10 a=1:gosub 100
 20 a=2:gosub 100
 30 a=3:gosub 100
 40 a=4:gosub 100
 50 end
100 'サブルーチン
110 print a
120 return
```

上のプログラムリストの場合、行番号100から120がサブルーチンになり、行番号10～40はそれぞれサブルーチンへと飛び、行番号120から再びメインルーチンへと帰還する流れをとる。

また、BASICによってはreturn文に行番号を添えることで、メインルーチンへの帰還を行わずにプログラムを走らせることが可能なものもある。

  - 構文2

:

``` basic
return 行番号
```

  -
    例

:

``` basic
 10 a=1:gosub 100
 20 a=2:gosub 100
 30 a=3:gosub 100
 40 a=4:gosub 100
 50 end
100 'サブルーチン
110 print a
120 if a<3 then return
130 if a>=3 then return 150
150 'サブルーチンからの離脱
160 print "end"
170 end
```

上の例では `a` の値として `3` が代入された行番号30からのサブルーチンへのジャンプ以降は、行番号130の `return 150` によってルーチンから解放され、行番号150へと飛ぶ。既にreturnを経ているため、仮にこの後にreturn文があっても行番号40に戻ることは二度と無く、エラーを返すこととなる。

また、多くのBASICではgosub returnは[ネストを作ることが可能であり](../Page/ネスティング.md "wikilink")、サブルーチンから更に別のサブルーチンへと飛ばせる。この場合、returnも二重に扱えることとなる。

殆どのBASICでは自らのルーチンへと飛ぶことも可能であるため、サブルーチンのネストは[バグ](../Page/バグ.md "wikilink")を生む原因にもなりえる。

## 脚注

## 参考文献

以下の3つは、C/C++の節でのみ参照した。

  - 『[JIS X 3010:2003 プログラム言語C](https://www.jisc.go.jp/app/jis/general/GnrJISNumberNameSearchList?show&jisStdNo=X3010)』 105頁（6.8.6.4 return文）ほか。
  - 『[JIS X 3014:2003 プログラム言語C++](https://www.jisc.go.jp/app/jis/general/GnrJISNumberNameSearchList?show&jisStdNo=X3014)』 79頁（6.6.3 return文）ほか。
  - 平林雅英　『ANSI C言語辞典』技術評論社、1989年（初版）、189頁（return文）。

[Category:制御構造](https://ja.wikipedia.org/wiki/Category:制御構造 "wikilink")

1.  [Chapter 14. Blocks and Statements](https://docs.oracle.com/javase/specs/jls/se8/html/jls-14.html#jls-14.17)