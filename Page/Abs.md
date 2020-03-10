> この記事は[Abs](https://ja.wikipedia.org/wiki/Abs)から翻訳されています。


**abs**は、多くのプログラミング言語において引数の[絶対値](https://ja.wikipedia.org/wiki/絶対値 "wikilink") (absolute value) を返す[関数である](../Page/サブルーチン.md "wikilink")。言語によってabs, Abs, ABSなどと大文字小文字に揺れがあったり、多少の修飾辞を伴っていたりする場合もある。例えば[Fortranの場合](../Page/FORTRAN.md "wikilink")、引数の[型によってABS](../Page/データ型.md "wikilink"), IABSなど、異なる名前の関数が用意されている。

## C/C++

[C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")では[ヘッダーファイル](https://ja.wikipedia.org/wiki/ヘッダーファイル "wikilink")\<stdlib.h\>および<cstdlib>の中で、次のように関数absが[宣言されている](https://ja.wikipedia.org/wiki/プロトタイプ宣言 "wikilink")。ただし、後述するようにこれ以外にもいくつか種類が存在する。

``` c
int abs(int);
```

そして、例えば次のように使用できる。

``` c
#include <stdio.h>
#include <stdlib.h>

int main(void) {
    int x = -5;
    int abs_x = abs(x);
    printf("%dの絶対値は%d\n", x, abs_x);
    return 0;
}
```

出力結果:

``` text
-5の絶対値は5
```

なお、符号付整数型に[2の補数](../Page/2の補数.md "wikilink")を用いる処理系で`abs(INT_MIN)`を実行する場合など、結果が表現できない場合の動作はC言語の仕様上は未定義である\[1\]が、[GCCなどの典型的な実装では](../Page/GNUコンパイラコレクション.md "wikilink")（絶対値ではない）元の値をそのまま返す。

### absの種類

[C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")の場合、Fortran同様に引数の型によって異なる名前の関数が用意されている。ただしC++では`abs`がそれぞれの型に対して[多重定義](../Page/多重定義.md "wikilink")されているので、異なる型に対して一律`abs`を使用することもできる。

| 関数名       | 型                                                                                   | 宣言ヘッダー                  | 備考                                                                                            |
| --------- | ----------------------------------------------------------------------------------- | ----------------------- | --------------------------------------------------------------------------------------------- |
| `abs`     | `int`（[整数型](../Page/整数型.md "wikilink")）                                             | \<stdlib.h\>, <cstdlib> |                                                                                               |
| `labs`    | `long`（長整数型）                                                                        | \<stdlib.h\>, <cstdlib> |                                                                                               |
| `llabs`   | `long long`（長々整数型）                                                                  | \<stdlib.h\>, <cstdlib> | [C99](../Page/C99.md "wikilink")、[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")で標準化。 |
| `imaxabs` | `intmax_t`（[処理系](https://ja.wikipedia.org/wiki/処理系 "wikilink")が扱える最大の整数型）           | \<stdlib.h\>, <cstdlib> | [C99](../Page/C99.md "wikilink")、[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")で標準化。 |
| `fabs`    | `double`（[倍精度浮動小数点数](../Page/倍精度浮動小数点数.md "wikilink")型）                             | \<math.h\>, <cmath>     |                                                                                               |
| `fabsf`   | `float`（[単精度浮動小数点数](../Page/単精度浮動小数点数.md "wikilink")型）                              | \<math.h\>              | [C99](../Page/C99.md "wikilink")で標準化。                                                         |
| `fabsl`   | `long double`（[拡張倍精度浮動小数点数](https://ja.wikipedia.org/wiki/拡張倍精度浮動小数点数 "wikilink")型） | \<math.h\>              | [C99](../Page/C99.md "wikilink")で標準化。                                                         |
| `cabs`    | `double complex`（倍精度[複素数](../Page/複素数.md "wikilink")型、C99のみ）                        | \<complex.h\>           | [C99](../Page/C99.md "wikilink")で標準化。                                                         |
| `cabsf`   | `float complex`（単精度複素数型、C99のみ）                                                      | \<complex.h\>           | [C99](../Page/C99.md "wikilink")で標準化。                                                         |
| `cabsl`   | `long double complex`（拡張倍精度複素数型、C99のみ）                                              | \<complex.h\>           | [C99](../Page/C99.md "wikilink")で標準化。                                                         |
| `abs`     | `complex`<T>（複素数型テンプレート、C++のみ）                                                      | <complex>               |                                                                                               |
| `abs`     | `valarray`<T>（ベクトル演算対応配列型テンプレート、C++のみ）                                              | <valarray>              |                                                                                               |

### 実装例

C言語におけるabs関数の典型的な実装例は以下である。

``` c
int my_abs(int x) {
    if (x < 0)
        return -x;
    else
        return x;
}
```

もしくは、[マクロを用いればC言語でも型を気にせずに用いることが可能となる](https://ja.wikipedia.org/wiki/マクロ_\(コンピュータ用語\) "wikilink")。しかし[副作用に注意する必要性が生じる](../Page/副作用_\(プログラム\).md "wikilink")。

``` c
#define my_abs(x) ((x) >= 0 ? (x) : -(x))
```

C99では[ジェネリック版のfabs関数が](../Page/ジェネリックプログラミング.md "wikilink")\<tgmath.h\>に宣言されている。

## Java

java.lang.Math.abs() にて実装されている。int, long, float, double 用に多重定義されている。int, long の負数の最小値を引数に与えると同じ値をそのまま返すと規定されている。

## .NET

[C\#を始めとする](../Page/C_Sharp.md "wikilink")[.NET Frameworkに対応した言語では](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、System.Math.Abs() にて実装されている。System.SByte, System.Int16, System.Int32, System.Int64, System.Decimal, System.Single, System.Double 用に多重定義されている。SByte.MinValue, Int16.MinValue, Int32.MinValue, Int64.MinValue をそれぞれのメソッドオーバーロードに渡すと System.OverflowException 例外がスローされる。

## 脚注

## 外部リンク

  -
[Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink") [Category:プログラミング言語の構文](https://ja.wikipedia.org/wiki/Category:プログラミング言語の構文 "wikilink")

1.  [JISC 日本工業標準調査会 JIS X3010 プログラム言語C](https://www.jisc.go.jp/app/jis/general/GnrJISNumberNameSearchList?show&jisStdNo=X3010)。