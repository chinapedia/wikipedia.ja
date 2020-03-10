> この記事は[Strlcpy](https://ja.wikipedia.org/wiki/Strlcpy)から翻訳されています。


**strlcpy** は[C言語](../Page/C言語.md "wikilink")で[文字列](../Page/文字列.md "wikilink")を安全にコピーするための[関数である](../Page/サブルーチン.md "wikilink")。ISO で規定された関数ではないが、[BSD libc](https://ja.wikipedia.org/wiki/BSD_libc "wikilink") などに含まれている。危険な使い方をしてしまいがちな関数 [strcpy](https://ja.wikipedia.org/wiki/strcpy "wikilink") や [strncpy](https://ja.wikipedia.org/wiki/strncpy "wikilink") の代替として、Todd C. Miller および[テオ・デ・ラート](../Page/テオ・デ・ラート.md "wikilink") (Theo de Raadt) が開発した\[1\]。

## 概要

[プロトタイプは](https://ja.wikipedia.org/wiki/プロトタイプ宣言 "wikilink")

``` c
size_t strlcpy (char *dst, const char *src, size_t size);
```

であり、[ポインタsrcの指すアドレスから最大でsize](../Page/ポインタ_\(プログラミング\).md "wikilink") - 1バイトの[文字列](../Page/文字列.md "wikilink")をdstにコピーし、dstの指す文字列が必ず[NULL文字で終わるようにする](https://ja.wikipedia.org/wiki/ヌル文字 "wikilink")。これによって、dstがchar配列の場合にsizeof(dst)をsizeとして指定すれば[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")しないことが保証される。

strncpyは似たプロトタイプを持つが、最大でsizeバイトをコピーするのでNULL文字で終わるとは限らない点や、文字列が短い場合にdstの残った部分をすべてゼロで埋める点がstrlcpyと異なる。

## 実装状況

Millerとde Raadtは[OpenBSD](../Page/OpenBSD.md "wikilink")の開発者であり、strlcpyを最初に実装したOSはOpenBSD 2.4である。以後、[FreeBSD](../Page/FreeBSD.md "wikilink") 3.3を含め、[Solaris](../Page/Solaris.md "wikilink")や[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")等の各OS、[OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")等のライブラリにも採用されている。[Linux](../Page/Linux.md "wikilink") では libbsd ライブラリ経由で利用できる。

一方で、[GNU Cライブラリ](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink") (glibc) の開発者たちは、[GNU Coding Standardsで禁じられている](https://ja.wikipedia.org/wiki/:en:GNU_Coding_Standards "wikilink")「長い行を黙って切り詰める」関数である、このような仕様の関数はバグである、いい加減なプログラムを助長してしまう、新たなセキュリティ問題を生む、など否定的な見解を示しており\[2\]、標準規格に含まれない限りはglibcには実装しない意向である。

strlcpyが危険な例：

``` c
char cmd[] = "rm *.bak";
char buf[5];
strlcpy(buf, cmd, sizeof(buf));
system(buf);
```

（sizeof(buf) が5であるため、最初の5-1=4文字しかコピーされず、"rm \*" が実行されることになります）

## 関連項目

  - [strlcat](https://ja.wikipedia.org/wiki/strlcat "wikilink") - [strcat](https://ja.wikipedia.org/wiki/strcat "wikilink")の代替

## 脚注

## 外部リンク

  -
[en:Strlcpy](https://ja.wikipedia.org/wiki/en:Strlcpy "wikilink")

[Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink")

1.  [strlcpy and strlcat - consistent, safe, string copy and concatenation. - 1999 USENIX Annual Technical Conference, June 6-11, 1999, Monterey, California, USA](https://www.usenix.org/legacy/events/usenix99/full_papers/millert/millert_html/index.html)
2.  libc-alphaメーリングリストでの議論[1](http://sources.redhat.com/ml/libc-alpha/2000-08/msg00052.html)\[[http://sources.redhat.com/ml/libc-alpha/2002-01/msg00001.html\]より](http://sources.redhat.com/ml/libc-alpha/2002-01/msg00001.html%5Dより)