> この記事は[Scanf](https://ja.wikipedia.org/wiki/Scanf)から翻訳されています。


**scanf**（スキャンエフ）は、[C言語](../Page/C言語.md "wikilink")の標準関数。[ヘッダーファイル](https://ja.wikipedia.org/wiki/ヘッダーファイル "wikilink") stdio.h で定義されている、書式付き入力[関数である](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")。

[標準入力](https://ja.wikipedia.org/wiki/標準ストリーム "wikilink")（大抵は[キーボード](https://ja.wikipedia.org/wiki/キーボード_\(コンピュータ\) "wikilink")）からの入力を、書式に従って[変数に読み込む機能を持つ](https://ja.wikipedia.org/wiki/変数_\(プログラミング\) "wikilink")。標準出力関数の[printf](https://ja.wikipedia.org/wiki/printf "wikilink")()と対比させて考えると分かりやすい。

ユーザーからの入力を受ける、ごく基本的な機能を持つにもかかわらず、後述するように異常入力（エラー）に配慮すると相応の手間がかかるため、テストプログラムや入門書を除いてはあまり使われない。

このファミリーの関数には、入力ストリームを指定できる fscanf() や、メモリ上の文字列ストリームを入力対象とする sscanf() などがある。

## 形式

stdio.h内で以下の様に宣言されている。

``` c
int scanf(const char *format, ...);
```

[printf](https://ja.wikipedia.org/wiki/printf "wikilink") と同様、第1引数の`format`は、それに続く可変長の実引数の変換方法（書式）を指定する。また[戻り値](https://ja.wikipedia.org/wiki/戻り値 "wikilink")は入力（スキャン）に成功した入力項目の数が返される。

利用例を以下に示す。

``` c
#include <stdio.h>

int main(void)
{
  int x; /* スキャン結果を格納する変数。 */

  printf("x = ? "); /* 入力を促すプロンプト。 */
  /* スキャンと結果の確認。 */
  if (scanf("%d", &x) == 1) {
    printf("スキャン結果 = %d\n", x);
  }
  else {
    printf("スキャン失敗\n");
  }
  return 0;
}
```

### 変換指定

scanf の変換指定は次の形式をとる。

`% [代入抑止][最大フィールド幅][長さ修飾子]変換指定子`

### 代入抑止

| フラグ | 意味                              |
| --- | ------------------------------- |
| \*  | フォーマットに合わせて入力を読み込むが実引数に代入はされない。 |

例えば

``` c
char c;
scanf("%*c%c", &c);
```

というコードがあり、 "ab"という入力があった場合 1文字目の 'a' は無視され 2文字目の 'b' という文字が代入される。

### 長さ修飾子

| 修飾子      | 意味                                    | 導入バージョン             |
| -------- | ------------------------------------- | ------------------- |
| hh       | 実引数は char 型                           | C99以降               |
| h        | 実引数は short 型                          | 全バージョン              |
| l（エル）    | 実引数は long 型または wchar_t 型または double 型 | wchar_t についてはC95以降 |
| ll（エルエル） | 実引数は long long 型                      | C99以降               |
| j        | 実引数は intmax_t 型                      | C99以降               |
| z        | 実引数は size_t 型                        | C99以降               |
| t        | 実引数は ptrdiff_t 型                     | C99以降               |
| L        | 実引数は long double 型                    | 全バージョン              |

### 変換指定子

<table>
<thead>
<tr class="header">
<th><p>指定子</p></th>
<th><p>意味</p></th>
<th><p>導入バージョン</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>d,i</p></td>
<td><p>10進符号付き整数</p></td>
<td><p>全バージョン</p></td>
</tr>
<tr class="even">
<td><p>u</p></td>
<td><p>10進符号無し整数</p></td>
<td><p>全バージョン</p></td>
</tr>
<tr class="odd">
<td><p>o</p></td>
<td><p>8進符号無し整数</p></td>
<td><p>全バージョン</p></td>
</tr>
<tr class="even">
<td><p>x,X</p></td>
<td><p>16進符号無し整数</p></td>
<td><p>全バージョン</p></td>
</tr>
<tr class="odd">
<td><p>e,E</p></td>
<td><p>浮動小数点数</p></td>
<td><p>全バージョン</p></td>
</tr>
<tr class="even">
<td><p>f,F</p></td>
<td><p>浮動小数点数</p></td>
<td><p>全バージョン</p></td>
</tr>
<tr class="odd">
<td><p>g,G</p></td>
<td><p>浮動小数点数</p></td>
<td><p>全バージョン</p></td>
</tr>
<tr class="even">
<td><p>a,A</p></td>
<td><p>浮動小数点数</p></td>
<td><p>C99以降</p></td>
</tr>
<tr class="odd">
<td><p>c</p></td>
<td><p>文字</p></td>
<td><p>全バージョン</p></td>
</tr>
<tr class="even">
<td><p>s</p></td>
<td><p>文字列</p></td>
<td><p>全バージョン</p></td>
</tr>
<tr class="odd">
<td><p>p</p></td>
<td><p>ポインタの値、対応する引数は void* になる。</p></td>
<td><p>全バージョン</p></td>
</tr>
<tr class="even">
<td><p>n</p></td>
<td><p>整数変数に出力済み文字数を格納</p></td>
<td><p>全バージョン</p></td>
</tr>
<tr class="odd">
<td><p>%</p></td>
<td><p>'%'の入力</p></td>
<td><p>全バージョン</p></td>
</tr>
<tr class="even">
<td><p>[...]</p></td>
<td><p>[ ]内で囲まれた文字だけを取得し、<br />
それ以外の文字が現れた場所以降は入力を終了する（下記参照）。</p></td>
<td><p>全バージョン</p></td>
</tr>
</tbody>
</table>

\[ \] は例えば

``` c
char str[256];
scanf("%[abc]", str);
```

というコードがあり、入力に "babaacdeabfghijabcef" という[文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")が入った場合、str には "babaac" という文字列のみが入力され、残りの文字列は入力されずに終了する。strに代入されなかった、"deabfghijabcef"は入力ストリームに残る形となる。また\[^ ... \]とした場合は逆に\[ \]内の文字が入ってくるまで文字を読み込む。 例えば、

``` c
char str[256];
scanf("%[^abc]", str);
```

という場合、"ghetbceajk"と入力すると、str には"ghet"が代入される。上記と同様に、入力されなかった文字列は入力ストリームに保持される。

## コード例

ソース:

``` c
#include <stdio.h>
#include <limits.h>

int main(void)
{
  int n1, n2, nadd, nsub, nmul, ndiv, nmod;

  printf("1つ目の入力数値:");
  if (scanf("%d", &n1) != 1) {
    puts("スキャン失敗");
    return -1;
  }
  printf("2つ目の入力数値:");
  if (scanf("%d", &n2) != 1) {
    puts("スキャン失敗");
    return -1;
  }
  if (n2 == 0) {
    /* ゼロ除算防止のチェック。 */
    puts("2つ目の数値は非ゼロを入力してください");
    return -1;
  }
  if (n1 == INT_MIN && n2 == -1) {
    /* 除算と剰余のオーバーフローエラー防止のチェック。 */
    puts("オーバーフローしない数値の組み合わせを入力してください");
    return -1;
  }

  nadd = n1 + n2;
  nsub = n1 - n2;
  nmul = n1 * n2;
  ndiv = n1 / n2;
  nmod = n1 % n2;

  printf("%d + %d = %d\n", n1, n2, nadd);
  printf("%d - %d = %d\n", n1, n2, nsub);
  printf("%d * %d = %d\n", n1, n2, nmul);
  printf("%d / %d = %d + %d / %d\n", n1, n2, ndiv, nmod, n2);

  return 0;
}
```

出力結果の例:

``` text
1つ目の入力数値:60
2つ目の入力数値:21
60 + 21 = 81
60 - 21 = 39
60 * 21 = 1260
60 / 21 = 2 + 18 / 21
```

## 関連する関数

### fscanf

``` c
int fscanf(FILE *fp, const char *format, ...);
```

fscanf は第1引数にFILEポインタを指定することで、標準入力からではなくファイルストリームから読み込む。[C言語](../Page/C言語.md "wikilink")では標準入力は stdin というFILEポインタで表すので、fscanf(stdin, ...) は scanf と完全に同義である。

### sscanf

``` c
int sscanf(const char *str, const char *format, ...);
```

sscanf は第1引数に文字列へのポインタを指定することで、標準入力からではなく文字列ストリームから読み込む。後述するように scanf でエラー処理を実装しようとすると、エラーにならずに再度入力待ちになってしまうパターンがある。このため標準入力から数値を入力する場合には、直接 scanf を使わずにいったん [fgets](https://ja.wikipedia.org/wiki/fgets "wikilink") 関数等で文字列として読み込んでから sscanf で処理することの方が多い。

## scanfの問題点と回避方法

scanf は非常に簡潔に入力の制御が行えるため、[C言語](../Page/C言語.md "wikilink")の入門書では必ずと言っていいほど登場する。しかしこの関数にはいくつかの問題点が指摘されている。ここではよく指摘される scanf の問題点とその回避方法について宣べる。

### 改行文字の取り扱い

入力が文字（char）の場合、主にキーボードで入力の際に押されるリターンキーが無視できないという問題点がある。例えば

``` c
char a, b, c;
scanf("%c", &a);
scanf("%c", &b);
scanf("%c", &c);
```

とした場合、通常なら3回入力待ちが行われることが期待されていると思われるが、実際には2回しか行われない（予期しない入力はここでは考慮しない）。これは最初の a の入力には入力された文字が代入されるが、このとき[ストリーム上に改行コードが残されてしまい](https://ja.wikipedia.org/wiki/ストリーム_\(プログラミング\) "wikilink")、次の b には a を入力する際に押下されたリターンキーの改行コードが代入されるためである。通常の %d や %s の場合改行コードは無視して入力を読み込むので問題にはならないが、 %c の場合は無条件にストリーム上の次のバイトを返すためこのような現象が発生する。これを防ぐには、

``` c
scanf("%c", &a);
scanf(" %c", &b);
scanf(" %c", &c);
```

のように最初に空白を入れることで回避される。これは入力前に空白（改行コードも含む）を読み飛ばすことを意味している。ただしこの場合 a, b, c に半角スペースを代入することはできない。そのような場合としては

``` c
scanf("%c%*c", &a);
scanf("%c%*c", &b);
scanf("%c%*c", &c);
```

という方法がとられる。これは入力した際の改行文字を%\*cで除去することを意味する。

### 空白、タブの読み飛ばし

scanf は空白とタブは改行文字と同じ区切り文字として扱われる。例えば、

``` c
char a[20];
scanf("%s", a);
```

という方法で文字列を読み込もうとしたとする。このとき入力文字列が "This is a pen" というものだった場合、実引数に入力されるものは "This" までである。これだけでも問題であるが、さらに問題なのは、残りの " is a pen" という文字列はストリーム上に残されてしまうことである。このため次に scanf を呼んだ場合、入力にかかわらず実引数に "is" という文字列を代入しようとしてしまうことになる。これを防ぐ手段としては

``` c
scanf("%[^\n]", a);
```

という方法がとられる。この場合は改行文字以外の文字列を全て a に代入するため、a には空白やタブも含めて文字列が代入される。なお前述における入力時の改行コードの取り扱いも考慮した場合は、

``` c
scanf("%[^\n]%*c", a);
```

という記述になる。

### バッファオーバーラン

他の C言語の文字列処理関数と同様に、scanf を使用する際にも[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")が発生する可能性がある\[1\]。例えば

``` c
char a[20];
scanf("%s", a);
```

というコードがあった場合、a に入力できる文字列は終了文字を除く、19バイトまでしか入力することが出来ず、それ以上の文字列が入力されるとバッファオーバーランが発生する。a の領域が十分であれば問題はないが、しかし入力されてくる文字列の長さを予測することは不可能であり、結局 a の長さをいくら大きくしても、さらにそれを上回る長さの入力が行われてしまえばバッファオーバーランが発生してしまう危険性がある。 この問題を防ぐ手段として一般的なのは最大フィールド幅を指定することである。上記の例の場合は

``` c
char a[20];
scanf("%19s", a);
```

とすることで、aには最初の19バイトが読み込まれ入力を終了する。ただしこの場合は残りの文字列はストリーム上に残ってしまうので実際には以下のようにすることで対処される。

``` c
char a[20];
scanf("%19s%*[^\n]", a);
```

これは19バイト読み込みさらに改行文字までの文字列を空読みすることを意味する。

さらに前述の改行コードがストリームに残る問題を考慮すると

``` c
char a[20];
scanf("%19s%*[^\n]%*c", a);
```

となるが、この場合はaに入る文字列が 19バイト以下の場合には、入力ストリームにやはり改行文字が残る。よって実際には、

``` c
char a[20];
scanf("%19s%*[^\n]", a);
getchar();
```

のように入力終了後、改行文字を空読みするなどの方法がとられる。空白文字の取り扱いも考慮する場合

``` c
char a[20];
scanf("%19[^\n]%*[^\n]", a);
getchar();
```

となる。

バージョン8.0 (2005) 以降の[Microsoft Visual C++コンパイラには](https://ja.wikipedia.org/wiki/Microsoft_Visual_C++ "wikilink")、[scanf_s()](https://msdn.microsoft.com/ja-jp/library/w40768et.aspx) という関数が用意されていて、バッファのサイズを指定することができる。scanf_s は[C11規格で標準化されたが](https://ja.wikipedia.org/wiki/C11_\(C言語\) "wikilink")、実装は任意である。

### 異常な入力が行われた時の処理

scanf関数は、予期せぬ値が[入力](https://ja.wikipedia.org/wiki/入力 "wikilink")されると、その値を読み込まず、[ストリーム上に残してしまう](https://ja.wikipedia.org/wiki/ストリーム_\(プログラミング\) "wikilink")。例えば

``` c
int i;
scanf("%d", &i);
```

としたコードがあった場合、入力が数字でなかった場合は scanf はストリームにその文字列を残したまま終了することになる。このため次に scanf が呼ばれたときはそのストリーム上のバッファが実引数に代入され、他の scanf にも異常な結果を返すことになる。例として 1 が入力されたら終了、それ以外はもう一度入力を求めるようなプログラムを考えてみる、もしこのプログラムを

``` c
int i;
while(1) {
  scanf("%d", &i);
  if (i == 1) {
     break;
  }
}
```

というようなコードで記述した場合、数字以外の文字を入力してしまうと[無限ループ](https://ja.wikipedia.org/wiki/無限ループ "wikilink")に陥ることになる。このような現象を防ぐ手段として scanf の戻り値を利用する方法がとられる。これは scanf は代入に成功した変数の数を戻り値として返すため、指定した実引数の数と scanf の戻り値が一致しないときに入力バッファをクリアすることで回避できる。例えば上記の例の場合は以下のようになる。

``` c
int i;
while(1) {
  if (scanf("%d", &i) != 1) {
     scanf("%*s");
     if (feof(stdin)) {
       /* エラー処理 */
     }
     continue;
  }

  if (i == 1) {
     break;
  }
}
```

入力バッファのクリアはここでは文字列を空読みすることで実現している（入力バッファのクリア方法は状況によって異なる方法が考えられる）。なお主にウェブ上などで、標準入力のバッファクリアの方法に fflush(stdin) や rewind(stdin) とする方法が紹介されることがあるが、[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")規格ではこれらの動作は未定義であり、正しい動作を保障するものではない。

この方法でエラー処理をする場合には上記の空白文字の取り扱いの関連で問題になることがある。例えば

``` c
int i, j;
scanf("%d %d", &i, &j);
```

のようなコードで、異常な入力があった場合エラー処理をしたいとする。これを

``` c
int i, j;
if (scanf("%d %d", &i, &j) != 2) {
  エラー処理
}
```

という方法で実現すると入力が "1" のみの場合、空白と改行は同一視されてしまうため、変数 "i" に 1 を入力して後、変数 "j"の入力待ち状態となる。もし、このような場合にもエラー処理を実行したい場合には、例えば以下のように一度文字列として読み込んで、その後 sscanf で読み込むことで実装すればよい。

``` c
char a[20];
int i, j;

scanf("%19[^\n]%*[^\n]", a);
getchar();

if (sscanf(a, "%d %d", &i, &j) != 2) {
  エラー処理
}
```

## 脚注

<references />

## 関連項目

  - [C言語](../Page/C言語.md "wikilink")
  - [アルゴリズム](../Page/アルゴリズム.md "wikilink")
  - [標準入力](https://ja.wikipedia.org/wiki/標準入力 "wikilink")

[Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink")

1.