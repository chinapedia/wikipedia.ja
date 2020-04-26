> この記事は[Source Code Control System](https://ja.wikipedia.org/wiki/Source_Code_Control_System)から翻訳されています。


**Source Code Control System**（**SCCS**）は、世界初の[ソースコード](../Page/ソースコード.md "wikilink")[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")。[1972年](../Page/1972年.md "wikilink")、[ベル研究所](../Page/ベル研究所.md "wikilink")の Marc J. Rochkind が [IBM](../Page/IBM.md "wikilink") [System/370](https://ja.wikipedia.org/wiki/System/370 "wikilink") 上の [OS/MVT](https://ja.wikipedia.org/wiki/:en:MVT "wikilink") 向けに開発した。その後、[PDP-11](../Page/PDP-11.md "wikilink")上の[UNIX](../Page/UNIX.md "wikilink")に移植され、SCCS は初期のUNIXの一部とされた。SCCS のコマンドの仕様は [Single UNIX Specification](../Page/Single_UNIX_Specification.md "wikilink") の一部ともなっている。

SCCS は [Revision Control System](../Page/Revision_Control_System.md "wikilink")(RCS)が登場するまで、ほとんど唯一のバージョン管理システムとして広く使われていた。現在、そのファイル形式は一部のバージョン管理システム内で利用されている（[BitKeeper](../Page/BitKeeper.md "wikilink") や [TeamWare](https://ja.wikipedia.org/wiki/TeamWare "wikilink")）。*Sablime*[1](http://www.bell-labs.com/project/sablime/) でも SCCS 形式のファイルを利用可能である。SCCS ファイル形式は interleaved delta（または[the weave](http://web.mit.edu/ghudson/thoughts/file-versioning)）と呼ばれる技法を使っている。この技法は[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")開発者が最新の[マージ手法の鍵として注目している](https://ja.wikipedia.org/wiki/マージ_\(バージョン管理\) "wikilink")（例えば、Precise [Codeville](https://ja.wikipedia.org/wiki/Codeville "wikilink") など）。

## SCCS を含んでいた初期のUNIXシステム

  - [Programmer's Workbench UNIX](https://ja.wikipedia.org/wiki/PWB/UNIX "wikilink")
  - [UNIX System III](../Page/UNIX_System_III.md "wikilink")
  - [UNIX System V](../Page/UNIX_System_V.md "wikilink")

## 参考文献

  - M. J. Rochkind: [The Source Code Control System](http://basepath.com/aup/talks/SCCS-Slideshow.pdf). In *[IEEE](../Page/IEEE.md "wikilink") Transactions on [Software Engineering](../Page/ソフトウェア工学.md "wikilink")* SE-1:4 (Dec. 1975), pages 364–370.
  - Greg Hudson: [Notes on keeping version histories of files](http://web.mit.edu/ghudson/thoughts/file-versioning)
  - [Cyclic SCCS Page](http://ximbiot.com/cvs/wiki/index.php?title=SCCS)

## 外部リンク

  - M. J. Rochkind: [I Hear Voices Talking About Me](http://www.mudbag.com/marcblog/2005/06/i-hear-voices-talking-about-me.html). In *[Marc's Blog](http://www.mudbag.com/marcblog/)* （2005年6月）
  - [GNU](../Page/GNU.md "wikilink") [CSSC](http://cssc.sourceforge.net/index.shtml) ("Compatibly Stupid Source Control") SCCS互換プログラム。[CVSや](../Page/Concurrent_Versions_System.md "wikilink")[Subversionといった最近のシステムへの乗り換えを可能にする](../Page/Apache_Subversion.md "wikilink")。
  - [SourceForge での SCCS 関連プロジェクト一覧](https://sourceforge.net/softwaremap/trove_list.php?form_cat=260)
  - [Sourceforge Hosted Version](http://sccs.sf.net/)
  - [sccs(1)](http://docs.hp.com/ja/B2355-60104-02/sccs.1.html) マニュアル（HP-UX）

[Category:バージョン管理システム](https://ja.wikipedia.org/wiki/Category:バージョン管理システム "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:1972年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1972年のソフトウェア "wikilink")