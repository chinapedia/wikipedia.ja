> この記事は[Revision Control System](https://ja.wikipedia.org/wiki/Revision_Control_System)から翻訳されています。


**Revision Control System**（**RCS**）は、初期の[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")の1つ。[プログラムや](../Page/プログラム_\(コンピュータ\).md "wikilink")[文書などの頻繁に改版されるテキストの管理に使われる](../Page/ソフトウェアドキュメンテーション.md "wikilink")。能率や機能は限定されるが、[バイナリファイル](https://ja.wikipedia.org/wiki/バイナリファイル "wikilink")のバージョンも管理できる。バージョンの記録には[diff](https://ja.wikipedia.org/wiki/diff "wikilink")ユーティリティを利用している。

RCS は、Walter F. Tichy が 1980年代に[パデュー大学](../Page/パデュー大学.md "wikilink")に在籍していたころ開発した。早くとも2011年10月まではパデュー大学で保守されていた\[1\]。2013年5月現在、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の一部となっている。

バージョン管理はファイル単位で行い、プロジェクト全体を管理するといった概念はなく、複数のユーザーが同時に作業することも想定していない。このため、[CVSなどのプロジェクトをサポートできるソフトウェアに取って代わられた](../Page/Concurrent_Versions_System.md "wikilink")。しかし1人で使う場合、例えば[サーバ](../Page/サーバ.md "wikilink")の構成ファイルや自動化スクリプトなどを管理する用途には充分な機能を持ち、[デーモンなどが不要で軽量](../Page/デーモン_\(ソフトウェア\).md "wikilink")・単純という利点もあることから、現在もRCSが使われる場面がある。CVS は本来、RCS を利用して構築されていた。

[ウィキ](../Page/ウィキ.md "wikilink")エンジンの中には、ページのリビジョンを格納するために RCS を使っているものもある（[TWiki](../Page/TWiki.md "wikilink")など）。

## 参考文献

  - Walter F. Tichy: *[RCS--A System for Version Control](http://www.uvm.edu/~ashawley/rcs/tichy1985rcs/html/)*. In: *Software--Practice and Experience*. July 1985. Volume 15. Number 7. Pages 637-654. [References to the paper at CiteSeer](http://citeseer.ist.psu.edu/tichy91rc.html)

## 脚注

<references />

## 外部リンク

  - [RCS at Purdue](http://www.cs.purdue.edu/homes/trinkle/RCS/)
  - [RCS at GNU](http://www.gnu.org/software/rcs/rcs.html)
  - [RCS(1)](http://linuxjm.sourceforge.jp/html/GNU_rcs/man1/rcs.1.html) マニュアル
  - [The RCS MINI-HOWTO](http://linuxjf.sourceforge.jp/JFdocs/RCS.html) - [Linux](../Page/Linux.md "wikilink") JF Project

[Category:バージョン管理システム](https://ja.wikipedia.org/wiki/Category:バージョン管理システム "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink")

1.