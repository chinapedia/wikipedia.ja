> この記事は[Atof](https://ja.wikipedia.org/wiki/Atof)から翻訳されています。


**atof** (ASCII to Floating Point Number) は、文字列を[倍精度浮動小数点数](https://ja.wikipedia.org/wiki/倍精度浮動小数点数 "wikilink")に変換する[C言語](../Page/C言語.md "wikilink")の[標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")の[関数](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")。標準ヘッダーファイル `<stdlib.h>` で宣言されている。読み方は規格では特に定められていない。

## 概要

引数で与えられた文字列を解析し、文字列先頭の連続する数値部分を`double`型の[浮動小数点数](../Page/浮動小数点数.md "wikilink")に変換する。例えば、引数に`"0.123abc"`を与えると、`0.123`を返す。`"INF"`や`"NAN"`といった表現は、それぞれ無限大、非数 ([NaN](https://ja.wikipedia.org/wiki/NaN "wikilink")) として変換する（大文字・小文字を区別しない）。また、変換に失敗しても`errno`を書き換えない。

正常に変換可能な文字列の場合は `strtod(nptr, NULL)` と同じ結果を返すが、不正な値の場合は atof はエラーを返さない。

名称は atof であるが戻り値は[単精度浮動小数点数](https://ja.wikipedia.org/wiki/単精度浮動小数点数 "wikilink")型 (`float`) ではなく、[倍精度浮動小数点数](https://ja.wikipedia.org/wiki/倍精度浮動小数点数 "wikilink")型 (`double`) であることに注意が必要。

[ANSI C標準ではない](https://ja.wikipedia.org/wiki/ANSI_C "wikilink") atoff 関数をサポートする処理系もある\[1\]。

## 形式

``` c
#include <stdlib.h>
double atof(const char *nptr);
```

## 脚注

## 関連項目

  - [atoi](https://ja.wikipedia.org/wiki/atoi "wikilink")
  - [atol](https://ja.wikipedia.org/wiki/atol "wikilink")
  - [itoa](https://ja.wikipedia.org/wiki/itoa "wikilink")

## 外部リンク

  -
  - [atof - cppreference.com](https://ja.cppreference.com/w/c/string/byte/atof)

[Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink")

1.  [atof atoff Subroutine](https://www.ibm.com/support/knowledgecenter/ssw_aix_72/a_bostechref/atof.html)