> この記事は[Rc \(\)](https://ja.wikipedia.org/wiki/Rc_\(\))から翻訳されています。


**rc**（"run commands"）は、[Version 10 Unixと](../Page/Research_Unix.md "wikilink")[Plan 9のための](../Page/Plan_9_from_Bell_Labs.md "wikilink")[コマンドラインインターフェースである](../Page/キャラクタユーザインタフェース.md "wikilink")。rcは[Bourne shellに似ているが](https://ja.wikipedia.org/wiki/Bourne_shell "wikilink")、その構文はより簡潔なものになっている。また、rcはトム・ダフによって作られた。彼は[Duff's deviceと呼ばれる](../Page/Duff's_device.md "wikilink")[C言語](../Page/C言語.md "wikilink")の構築で有名である。

オリジナルなrcの[UNIX](../Page/UNIX.md "wikilink")に対するポートは、[Plan 9 form User Spaceの一部としてなされた](https://ja.wikipedia.org/wiki/Plan_9_form_User_Space "wikilink")。rcの[UNIX系](https://ja.wikipedia.org/wiki/UNIX系 "wikilink")OSへのリライトはバイロン・ラキツィスによるものも利用可能だが、それはいくつかの互換性のない変更を含んでいる。

rcは、オリジナルのBourne shellが[ALGOL](../Page/ALGOL.md "wikilink")風の構造を持つのに対して、C言語のような構造を持つ。ただし、"if not"構造を"else"の代わりに使い、リストの繰り返しにBourne shell風の"for"ループを持っている。rcにおいては"$@"のような構造を排除する必要のために、すべての変数は文のリストとなっている。

## 影響

### es

es（"extensible shell"）は、ラキツィスとポール・ハウァーによって開発\[1\]された、[オープンソース](../Page/オープンソース.md "wikilink")のコマンドラインインターフェースで、rcシェルに影響を受けた[スクリプト言語](../Page/スクリプト言語.md "wikilink")の構文を利用している\[2\]\[3\]。esは、ラツキィスによるUNIXのためのrcのクローン のコードをオリジナルのベースにしている\[4\]\[5\]。

es（＝"extensible shell"）は、[UNIXシェル](https://ja.wikipedia.org/wiki/UNIXシェル "wikilink")として、完全な[関数型プログラミング言語](https://ja.wikipedia.org/wiki/関数型プログラミング言語 "wikilink")を提供することを意図している\[6\]。esの大部分の開発は1990年代の初頭に始まり、1993年冬の[サンディエゴ](../Page/サンディエゴ.md "wikilink")における[USENIX](../Page/USENIX.md "wikilink")の会議において紹介された後\[7\]、公式の リリースは1997年の0.9-beta-1以後やめられた\[8\]。また、esは、[zsh](https://ja.wikipedia.org/wiki/zsh "wikilink")や[bash](https://ja.wikipedia.org/wiki/bash "wikilink")などのポピュラーなシェルに比べて機能が欠けている\[9\]。

## 出典

## 外部リンク

  - \- Plan 9のmanページ

  - [Plan 9 from User Space](https://9fans.github.io/plan9port/) - [Linux](../Page/Linux.md "wikilink")や[mac OSなどの](https://ja.wikipedia.org/wiki/mac_OS "wikilink")[UNIX系](https://ja.wikipedia.org/wiki/UNIX系 "wikilink")システム向けのrcなどのPlan 9由来のツールを含む

  - [Byron Rakitzis' rewrite for Unix](http://tobold.org/article/rc)

  - [es Official website](http://hawkwind.utcs.utoronto.ca:8001/mlists/es.html)

[Category:Unixシェル](https://ja.wikipedia.org/wiki/Category:Unixシェル "wikilink") [Category:Inferno_(オペレーティングシステム)](https://ja.wikipedia.org/wiki/Category:Inferno_\(オペレーティングシステム\) "wikilink")

1.
2.
3.
4.
5.
6.
7.  [Es: A shell with higher-order functions](http://stuff.mit.edu/afs/sipb/user/yandros/doc/es-usenix-winter93.html) by Byron Rakitzis, [NetApp Inc](https://ja.wikipedia.org/wiki/NetApp "wikilink"),, and Paul Haahr, [Adobe Systems Incorporated](https://ja.wikipedia.org/wiki/Adobe_Systems_Incorporated "wikilink"); <u>Archived</u> at [Archive.Org](https://web.archive.org/web/20090415213858/http://192.220.96.201/es/es-usenix-winter93.html).
8.  [](ftp://ftp.sys.utoronto.ca/pub/es/)
9.