> この記事は[Initng](https://ja.wikipedia.org/wiki/Initng)から翻訳されています。


**Initng**は、[sysvinitの完全な置換である](https://ja.wikipedia.org/wiki/init "wikilink")。[init](https://ja.wikipedia.org/wiki/init "wikilink")とは、[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")で最初に起動される[プロセス](../Page/プロセス.md "wikilink")であり、他の全プロセスの初期化の責任を持つ。Initngの公式サイトでは、Initngを「次世代（next generation）init システム」と称している。

## 利点

initの実装（[System Vのsysvinitなど](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink")、[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")の多くで使われている実装）では、事前に定義された順序でプロセスを起動し、あるプロセスの初期化が完了した時点で次のプロセスの起動を行う。Initngでは、あるプロセスを起動するのに必要な条件が整うと、すぐさまそのプロセスを起動する。複数のプロセスを並行して起動できる。InitngはUnix系システムでのプロセス起動を非同期に行うことで、ブートにかかる時間を大幅に削減する。また、システムがより制御しやすくなるようなデータが得られるとの指摘もある。

## 開発

Initngはまだ[ベータ版](../Page/ベータ版.md "wikilink")である。[Debian](../Page/Debian.md "wikilink")、[Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")、[Fedora](../Page/Fedora.md "wikilink")といった各種ディストリビューション向けのパッケージや、[Gentoo Linux向けの](../Page/Gentoo_Linux.md "wikilink")[ebuild](https://ja.wikipedia.org/wiki/ebuild "wikilink")スクリプトもある。

当初の開発者はJimmy Wennlund。現在は、Ismael Luceno率いるプロジェクトが開発・保守を行っている。

## 関連項目

  - [init](https://ja.wikipedia.org/wiki/init "wikilink")
  - [Upstart](https://ja.wikipedia.org/wiki/Upstart "wikilink")
  - [Launchd](https://ja.wikipedia.org/wiki/Launchd "wikilink")

## 外部リンク

  - [Initng 公式サイト](http://www.initng.org)
  - [Install InitNG on Ubuntu/Kubuntu](http://hermann.czedik.net/ubuntu_initng.html)

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")