> この記事は[Strlcat](https://ja.wikipedia.org/wiki/Strlcat)から翻訳されています。


**strlcat** は[C言語](../Page/C言語.md "wikilink")で[文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")を安全に[結合するための](https://ja.wikipedia.org/wiki/文字列結合 "wikilink")[関数である](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")。ISO で規定された関数ではないが、[BSD libc](https://ja.wikipedia.org/wiki/BSD_libc "wikilink") などに含まれている。危険な使い方をしてしまいがちな関数[strcat](https://ja.wikipedia.org/wiki/strcat "wikilink")や[strncat](https://ja.wikipedia.org/wiki/strncat "wikilink")の代替として、Todd C. Millerおよび[テオ・デ・ラート](../Page/テオ・デ・ラート.md "wikilink") (Theo de Raadt) が開発した\[1\]。

## 概要

[プロトタイプは](https://ja.wikipedia.org/wiki/プロトタイプ宣言 "wikilink")

``` c
size_t strlcat (char *dst, const char *src, size_t size);
```

であり、[ポインタsrcの指すアドレスから最大でsize](../Page/ポインタ_\(プログラミング\).md "wikilink") - strlen(dst) - 1バイト[文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")をdstの末尾に追記し、[NULL文字で終わるようにする](https://ja.wikipedia.org/wiki/ヌル文字 "wikilink")。つまり、dstのバッファの実際の大きさをsizeに指定すれば、[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")しないことが保証される。

strncatは似たプロトタイプを持つが、sizeの意味はsrcから最大で何バイトコピーするかであり、NULL文字を考慮すると最大でsize + 1バイトをコピーされる。またsizeの値は、dstに既に存在する文字数も考慮しなくてはいけない。この複雑さからしばしばsizeの指定を誤り、[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")の原因となる。

## 実装状況

Millerとデ・ラットは[OpenBSD](../Page/OpenBSD.md "wikilink")の開発者であり、strlcatを最初に実装した[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) はOpenBSD 2.4である。以後、[FreeBSD](../Page/FreeBSD.md "wikilink") 3.3を含め、[Solaris](../Page/Solaris.md "wikilink")や[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")にも採用されている。Linux では libbsd ライブラリ経由で利用できる。[glibc](https://ja.wikipedia.org/wiki/glibc "wikilink") や [Microsoft Visual C++](https://ja.wikipedia.org/wiki/Microsoft_Visual_C++ "wikilink") には実装されていない。

## 関連項目

  - [strlcpy](https://ja.wikipedia.org/wiki/strlcpy "wikilink") - [strcpy](https://ja.wikipedia.org/wiki/strcpy "wikilink")、[strncpy](https://ja.wikipedia.org/wiki/strncpy "wikilink") の代替

## 参照

## 外部リンク

  -
[Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink")

1.  [strlcpy and strlcat - consistent, safe, string copy and concatenation. - 1999 USENIX Annual Technical Conference, June 6-11, 1999, Monterey, California, USA](https://www.usenix.org/legacy/events/usenix99/full_papers/millert/millert_html/index.html)