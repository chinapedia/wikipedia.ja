> この記事は[Printf](https://ja.wikipedia.org/wiki/Printf)から翻訳されています。


**printf**（プリントエフ）は、[C言語](../Page/C言語.md "wikilink")の標準入出力ヘッダー (`stdio.h`) で宣言されている[関数である](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")。引数で与えられた書式付きの文字列を、環境によって設定された[標準出力](https://ja.wikipedia.org/wiki/標準出力 "wikilink") (`stdout`) に出力する。JIS X 3010:2003においてその機能は「[実引数に](../Page/引数.md "wikilink")`stdout`を実引数として付加した`fprintf`関数と等価とする」と規定されている (7.19.6.3)。

この関数は、第1引数に与えられた文字列を出力する。C言語の他の単純な入出力関数に比べ、比較的複雑な構造を持っており、第1引数の文字列のなかで書式を指定することで、第2引数以降の任意の数の引数（[可変長引数](https://ja.wikipedia.org/wiki/可変長引数 "wikilink")）を、書式に従って出力することができる。また、[整数型](../Page/整数型.md "wikilink")（`int`型）の戻り値を持ち、出力に成功した場合には転送したバイト数、出力に失敗した場合には負数を返却する。

## 形式

``` c
#include <stdio.h>
int printf(const char * restrict format, ...);
```

## 書式化文字列

上記形式における第一引数には、それに続く実引数の変換方法を指定する。書式化文字列には、通常の[マルチバイト文字](../Page/マルチバイト文字.md "wikilink")または`%`で始まる変換指定のいずれかの指令を0個以上含む。多バイト文字が含まれ、かつ[文字コード](../Page/文字コード.md "wikilink")が[シフトシーケンス](https://ja.wikipedia.org/wiki/シフトシーケンス "wikilink")に依存する場合には、書式化文字列は初期シフト状態で始まり、初期シフト状態で終わらなければならない。書式指定を行う`%`<var>`〜`</var>それぞれを書式指定子と呼ぶ。

### 変換指定

変換指定は次の形式をとる。（\[ \]内は省略可能）

`%[引数順][フラグ][最小フィールド幅][.精度][長さ修飾子]変換指定子`

### 引数順 (POSIX)

これは標準C規格の仕様ではなく、[POSIX](../Page/POSIX.md "wikilink")で規定されている拡張である。

書式文字列において`%`の代わりに`%`*`m`*`$`を記述することで、続く可変長引数のうちどれを使うかを番号*m*で指定できる。 例えば、

``` c
const char* fmt = "Invalid command %1$s at line %2$d.\n";
const char* cmd = "hoge";
const int lineNumber = 20;
printf(fmt, cmd, lineNumber);
```

とした場合、

`Invalid command hoge at line 20.`

と表示される。これだけならば大きな意味はないが、例えばメッセージを翻訳（[ローカライズ](../Page/国際化と地域化.md "wikilink")）する際、

``` c
const char* fmt = "%2$d行目のコマンド %1$s は不正です。\n";
```

というように書式文字列だけをローカライズする\[1\]ことで、可変長引数の指定順を変更せずに、

`20行目のコマンド hoge は不正です。`

という自然な語順の出力を得ることができる\[2\]。

### フラグ

変換指定のフラグは以下の通り。

| フラグ | 意味                         |
| --- | -------------------------- |
| \-  | フィールドの左寄せ                  |
| \+  | 常に符号を出力                    |
| 空白  | 数値が正または 0 の場合は符号の代わりに空白を出力 |
| \#  | 代替形式。基数を表すプレフィックスの出力等      |
| 0   | 出力文字数が最小フィールド幅未満の場合は'0'を出力 |

### 長さ修飾子

| 修飾子               | 意味                                         | 導入バージョン                               |
| ----------------- | ------------------------------------------ | ------------------------------------- |
| hh                | 実引数は char 型                                | C99以降                                 |
| h                 | 実引数は short 型                               | 全バージョン                                |
| l（エル）             | 実引数は long 型または wchar_t 型または double 型\[3\] | wchar_t についてはC95以降、double についてはC99以降 |
| ll（エルエル）          | 実引数は long long 型                           | C99以降                                 |
| j                 | 実引数は intmax_t 型                           | C99以降                                 |
| z                 | 実引数は size_t 型                             | C99以降                                 |
| t                 | 実引数は ptrdiff_t 型                          | C99以降                                 |
| L                 | 実引数は long double 型                         | 全バージョン \<\!--                         |
| |実引数は char16_t 型 |                                            |                                       |
| |実引数は char32_t 型 | \--\>                                      |                                       |

### 変換指定子

| 指定子  | 意味                            | 導入バージョン |
| ---- | ----------------------------- | ------- |
| d, i | 10進符号付き整数                     | 全バージョン  |
| u    | 10進符号無し整数                     | 全バージョン  |
| o    | 8進符号無し整数                      | 全バージョン  |
| x, X | 16進符号無し整数（ X は大文字で出力）         | 全バージョン  |
| e, E | 指数形式浮動小数点数（ E は大文字で出力）        | 全バージョン  |
| f, F | 小数形式浮動小数点数（ F は大文字で出力）        | 全バージョン  |
| g, G | e または f 形式のうち適した方（ G は大文字で出力） | 全バージョン  |
| a, A | 16進浮動小数点（ A は大文字で出力）          | C99以降   |
| c    | 文字                            | 全バージョン  |
| s    | 文字列                           | 全バージョン  |
| p    | ポインタの値                        | 全バージョン  |
| n    | 整数変数に出力済み文字数を格納               | 全バージョン  |
| %    | '%'の出力                        | 全バージョン  |
|      |                               |         |

## 関連する関数

### fprintf

fprintfは、引数にファイルポインタfpが追加され、標準出力の代わりにfpへ出力する変種である。

``` c
#include <stdio.h>
int fprintf(FILE * restrict fp, const char * restrict format, ...);
```

### sprintf, snprintf

sprintfとsnprintfは、引数にchar配列の要素へのポインタstrが追加されたもので、標準出力の代わりにstrへ出力する変種である。snprintfは、さらにstrに書き込んで良い文字数を指定する引数が追加されたものであるが、Cの標準規格に収録されたのは[C99](../Page/C99.md "wikilink")からである。

``` c
#include <stdio.h>
int sprintf(char * restrict str, const char * restrict format, ...);
int snprintf(char * restrict str, size_t size, const char * restrict format, ...);
```

### wprintf, fwprintf, swprintf

wprintf, fwprintf, swprintfは、それぞれprintf, fprintf, snprintfに対応し、[ワイド文字](../Page/ワイド文字.md "wikilink")を使用するものである。sprintfに対応するワイド文字関数（出力バッファサイズを受け取らない関数）は存在しない\[4\]。

``` c
#include <stdio.h>
int wprintf(const wchar_t * restrict format, ...);
int fwprintf(FILE * restrict fp, const wchar_t * restrict format, ...);
int swprintf(wchar_t * restrict str, size_t size, const wchar_t * restrict format, ...);
```

### va_listを引数に取るもの

ここまでに挙げたprintfとその変種に対して、可変個引数部分をva_listに変化させた種類が存在する。それぞれ、関数名の頭にvを付けた名称となっている。

``` c
#include <stdio.h>
int vprintf(const char * restrict format, va_list args);
int vfprintf(FILE * restrict fp, const char * restrict format, va_list args);
int vsprintf(char * restrict str, const char * restrict format, va_list args);
int vsnprintf(char * restrict str, size_t size, const char * restrict format, va_list args);
int vwprintf(const wchar_t * restrict format, va_list args);
int vfwprintf(FILE * restrict fp, const wchar_t * restrict format, va_list args);
int vswprintf(wchar_t * restrict str, size_t size, const wchar_t * restrict format, va_list args);
```

### 安全性を向上させたもの

[C11のAnnex](https://ja.wikipedia.org/wiki/C11_\(C言語\) "wikilink") K Bounds‐checking interfacesで規定された、安全性を向上させた種類が存在する。それぞれ、関数名の末尾に_sを付けた名称となっている。これらの関数は、__STDC_WANT_LIB_EXT1__を1に定義した上で対応するヘッダをインクルードすると宣言される。

``` c
#define __STDC_WANT_LIB_EXT1__ 1
#include <stdio.h>
#include <wchar.h>

int printf_s(const char * restrict format, ...);
int fprintf_s(FILE * restrict fp, const char * restrict format, ...);
int sprintf_s(char * restrict str, rsize_t size, const char * restrict format, ...);
int snprintf_s(char * restrict str, rsize_t size, const char * restrict format, ...);
int vprintf_s(const char * restrict format, va_list arg);
int vfprintf_s(FILE * restrict fp, const char * restrict format, va_list arg);
int vsprintf_s(char * restrict str, rsize_t size, const char * restrict format, va_list arg);
int vsnprintf_s(char * restrict str, rsize_t size, const char * restrict format, va_list arg);

int wprintf_s(const wchar_t * restrict format, ...);
int fwprintf_s(FILE * restrict fp, const wchar_t * restrict format, ...);
int swprintf_s(wchar_t * restrict str, rsize_t size, const wchar_t * restrict format, ...);
int snwprintf_s(wchar_t * restrict str, rsize_t size, const wchar_t * restrict format, ...);
int vwprintf_s(const wchar_t * restrict format, va_list arg);
int vfwprintf_s(FILE * restrict fp, const wchar_t * restrict format, va_list arg);
int vswprintf_s(wchar_t * restrict str, rsize_t size, const wchar_t * restrict format, va_list arg);
int vsnwprintf_s(wchar_t * restrict str, rsize_t size, const wchar_t * restrict format, va_list arg);
```

以下のような機能が追加されている。

  - FILE\*や文字列の引数（%sに対応する可変長引数部分の引数も含む）に対するNULLポインタチェック
  - %n書式の禁止

## コード例

``` c
#include <stdio.h>

int main(void)
{
    int a = 1234;
    printf("%d %o %x\n", a, a, a);
    printf("%s %c\n", "abc", 'x');
    return 0;
}
```

上記のコードをコンパイルし実行すると、次の出力が得られる。

`1234 2322 4d2`
`abc x`

## 脆弱性

一般に、書式文字列を外部や利用者から自由に指定できる状態とすることは[セキュリティホール](../Page/セキュリティホール.md "wikilink")の温床となるため望ましくない。特に%n書式を用いたものが有名である\[5\]。

## 他言語

C言語から派生した[C++](../Page/C++.md "wikilink")や[D言語](../Page/D言語.md "wikilink")はもとより、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")\[6\]、[Ruby](../Page/Ruby.md "wikilink")\[7\]、[Perl](../Page/Perl.md "wikilink")など他の言語でもprintfが実装されている。また、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")の言語の中には、C++での[Boost](https://ja.wikipedia.org/wiki/Boost "wikilink")::format\[8\]、Ruby\[9\]、[Python](../Page/Python.md "wikilink")など[演算子](../Page/演算子.md "wikilink")としてsprintfを実行できるものも存在する。
Unix系オペレーティングシステムのコマンドとして実装されたprintfもある。

## 脚注

## 参考文献

  - JIS X 3010:2003 プログラミング言語C

  - （C11の最終ドラフト）

## 関連項目

  - [C言語](../Page/C言語.md "wikilink")
  - [入出力](../Page/入出力.md "wikilink")
  - [Hello world](../Page/Hello_world.md "wikilink")
  - [scanf](https://ja.wikipedia.org/wiki/scanf "wikilink")
  - [書式文字列攻撃](../Page/書式文字列攻撃.md "wikilink")

## 外部リンク

  - UNIX コマンド
      - [printf(1)](https://linuxjm.osdn.jp/html/gnumaniak/man1/printf.1.html) man page GNU 版。JM Project
      - [printf(1)](https://docs.oracle.com/cd/E36784_01/html/E36870/printf-1g.html) man page (Solaris 10 Reference Manual)
      - [printf(1)](https://nixdoc.net/man-pages/HP-UX/man1/printf.1.html) man page（HP-UX リファレンス）
  - 標準 C ライブラリ
      - [printf(3)](https://linuxjm.osdn.jp/html/LDP_man-pages/man3/printf.3.html) JM Project
      - [printf(3C)](https://docs.oracle.com/cd/E19455-01/816-3521/6m9q0rckh/index.html) man page (Solaris 10 Reference Manual)
      - [printf(3S)](http://docs.hp.com/ja/B2355-60128/printf.3S.html) man page（HP-UX リファレンス）

[Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")

1.  実際のローカライズ作業では、[gettext](https://ja.wikipedia.org/wiki/gettext "wikilink")等によってメッセージカタログから文字列を得るようにコードを記述する。
2.  類似の順序指定可能な書式化機能を持つものとして、[Windows APIの](../Page/Windows_API.md "wikilink")[FormatMessage()](https://docs.microsoft.com/en-us/windows/desktop/api/winbase/nf-winbase-formatmessage)関数や、[Microsoft Foundation Classの](../Page/Microsoft_Foundation_Class.md "wikilink")[AfxFormatString2()](https://msdn.microsoft.com/en-us/library/kh955ebx.aspx)関数、[.NET FrameworkのSystem](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink").String.Format()メソッドなどが挙げられる。
3.  可変長引数では「既定の実引数拡張」により、float型の引数はdouble型へと変換されるため、本来はdoubleに対して修飾子を適用する必要はない。
4.  [Microsoft Visual C++には非標準関数としてバッファサイズを受け取らないswprintfが存在するが](../Page/Microsoft_Visual_C++.md "wikilink")、バージョン2005 (8.0) 以降では既定で無効化されており、非推奨となっている。\[<https://msdn.microsoft.com/ja-jp/library/ms396977(v=vs.71>).aspx sprintf、swprintf (CRT)\], \[<https://msdn.microsoft.com/ja-jp/library/ybk95axf(v=vs.120>).aspx sprintf、_sprintf_l、swprintf、_swprintf_l、__swprintf_l\]
5.
6.
7.
8.
9.