> この記事は[Atol](https://ja.wikipedia.org/wiki/Atol)から翻訳されています。


**atol** (ASCII to Long Integer) は、文字列を[整数型](https://ja.wikipedia.org/wiki/整数型 "wikilink")に変換する[C言語](../Page/C言語.md "wikilink")の[標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")の[関数](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")。標準ヘッダーファイル `<stdlib.h>`で宣言されている。読み方は規格では特に定められていない。

## 概要

[引数](../Page/引数.md "wikilink")として与えられた文字列を解析し、文字列先頭の連続する[10進数](https://ja.wikipedia.org/wiki/10進数 "wikilink")[整数](../Page/整数.md "wikilink")部分を`long`型の整数に変換する。例えば`"123456789"`という文字列を与えると`long`型の`123456789L`を返す。また`"123456789abc"`を与えると`123456789L`を返し、`"123456abc789"`を与えると`123456L`を返す。変換不可能な文字列の場合、一般的には`0L`を返すが、[C99](../Page/C99.md "wikilink") や [C11](https://ja.wikipedia.org/wiki/C11_\(C言語\) "wikilink") の仕様上は[戻り値](https://ja.wikipedia.org/wiki/戻り値 "wikilink")は未定義 (undefined) とされている\[1\]。また、変換に失敗しても`errno`を書き換えない。

正常に変換可能な文字列の場合は `strtol(s, NULL, 10)` と同じ結果を返す。

## 形式

``` c
#include<stdlib.h>
long atol(const char *nptr);
```

## 脚注

## 関連項目

  - [atoi](https://ja.wikipedia.org/wiki/atoi "wikilink")
  - [atof](https://ja.wikipedia.org/wiki/atof "wikilink")
  - [itoa](https://ja.wikipedia.org/wiki/itoa "wikilink")

## 外部リンク

  -
  - [atoi, atol, atoll - cppreference.com](https://ja.cppreference.com/w/c/string/byte/atoi)

[Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink")

1.  [ISO/IEC 9899:201x Programming languages — C](http://www.open-std.org/jtc1/sc22/wg14/www/docs/n1548.pdf)