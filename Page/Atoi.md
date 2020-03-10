> この記事は[Atoi](https://ja.wikipedia.org/wiki/Atoi)から翻訳されています。


**atoi** (ASCII to Integer) は、文字列を[整数型](../Page/整数型.md "wikilink")に変換する[C言語](../Page/C言語.md "wikilink")の[標準Cライブラリ](../Page/標準Cライブラリ.md "wikilink")の[関数](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")。標準ヘッダーファイル `<stdlib.h>` で宣言されている。読み方は規格では特に定められていない。

## 概要

引数で与えられた文字列を解析し、文字列先頭の連続する[10進数](https://ja.wikipedia.org/wiki/10進数 "wikilink")[整数](../Page/整数.md "wikilink")部分を`int`型の整数に変換する。例えば、引数に`"123abc"`を与えると`123`を返し、`"-5"`なら`-5`を返す。`"abc"`や`"１２３"`（[全角文字](https://ja.wikipedia.org/wiki/全角文字 "wikilink")）など変換不可能な文字列の場合、一般的には 0 を返すが、[C99](../Page/C99.md "wikilink") や [C11](https://ja.wikipedia.org/wiki/C11_\(C言語\) "wikilink") の仕様上は[戻り値](https://ja.wikipedia.org/wiki/戻り値 "wikilink")は未定義 (undefined) とされている\[1\]。また、変換に失敗しても`errno`を書き換えない。

正常に変換可能な文字列の場合は `(int)strtol(s, NULL, 10)` と同じ結果を返す。

## 形式

``` c
#include <stdlib.h>
int atoi(const char *nptr);
```

## 脚注

## 関連項目

  - [atof](https://ja.wikipedia.org/wiki/atof "wikilink")
  - [atol](https://ja.wikipedia.org/wiki/atol "wikilink")
  - [itoa](https://ja.wikipedia.org/wiki/itoa "wikilink")

## 外部リンク

  -
  - [atoi, atol, atoll - cppreference.com](https://ja.cppreference.com/w/c/string/byte/atoi)

[Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink")

1.  [ISO/IEC 9899:201x Programming languages — C](http://www.open-std.org/jtc1/sc22/wg14/www/docs/n1548.pdf)