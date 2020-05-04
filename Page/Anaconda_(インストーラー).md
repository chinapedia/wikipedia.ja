> この記事は[Anaconda \(インストーラー\)](https://ja.wikipedia.org/wiki/Anaconda_\(インストーラー\))から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Anaconda_installation_summary_screen_in_Fedora_19.png "wikilink")

**Anaconda**（アナコンダ）は、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")(OS)のインストーラ。[Python](../Page/Python.md "wikilink")と[C言語](../Page/C言語.md "wikilink")で実装されている。[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")の[フロントエンド](../Page/フロントエンド.md "wikilink")には[PyGTK](https://ja.wikipedia.org/wiki/PyGTK "wikilink")、テキストモードのフロントエンドには[Python-newt](https://ja.wikipedia.org/wiki/Python-newt "wikilink")が使われている。

[Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink") や [Oracle Linux](https://ja.wikipedia.org/wiki/Oracle_Linux "wikilink")、[Scientific Linux](../Page/Scientific_Linux.md "wikilink")、[CentOS](../Page/CentOS.md "wikilink")、[Qubes OS](https://ja.wikipedia.org/wiki/Qubes_OS "wikilink")、[Fedora](../Page/Fedora.md "wikilink")、[Sabayon Linux](https://ja.wikipedia.org/wiki/Sabayon_Linux "wikilink")、[BLAG Linux](https://ja.wikipedia.org/wiki/BLAG_Linux "wikilink")、[GNU](../Page/GNU.md "wikilink") で使用されているだけでなく、(Debian ベースで、Ian Murdock によって設立された) [Progeny Componentized Linux](../Page/Progeny_Debian.md "wikilink") や [Asianux](../Page/Asianux.md "wikilink")、[Foresight Linux](../Page/Foresight_Linux.md "wikilink")、[Rpath Linux](https://ja.wikipedia.org/wiki/Rpath_Linux "wikilink")、(Gentoo Linux ベースの)[VidaLinux](https://ja.wikipedia.org/wiki/VidaLinux "wikilink") といったような、あまり知られていない[ディストロや開発が中止されたディストロでも使用されている](https://ja.wikipedia.org/wiki/ディストリビューション "wikilink")。

## 機　能

Anaconda はテキストモードと GUIモードを提供しているので、ユーザーは幅広いシステムにインストールすることができる。異なるソフトウェア間で簡単に移植可能なように設計されており、幅広いハードウェア・プラットフォーム(IA-32, Itanium, DEC Alpha, IBM ESA/390, PowerPC, ARMv8)をサポートしている。CD-ROMドライブやハードディスクなどのローカル・ストレージデバイスからのインストールや、FTP、HTTP、NFS経由でのネットワーク・リソースからのインストールもサポートしている。キックスタートファイルを使用してインストールを自動化することができ、インストールを自動的に設定するので、ユーザーは最小限の監視でインストールを実行することが可能となる。OS のインストールプロセスを開始する前に、インストーラはシステムのハードウェアとリソースの要件をチェックを行う。そして、要件が満たされた場合のみ、インストールプロセスを開始する。

## 技術的情報

このプログラムは主としてに [Python](../Page/Python.md "wikilink") で書かれており、その内のいくつかのモジュールは [C](https://ja.wikipedia.org/wiki/C "wikilink") 言語で書かれている。[GTK+3](https://ja.wikipedia.org/wiki/GTK+3 "wikilink") /[PyGObject](https://ja.wikipedia.org/wiki/PyGObject "wikilink") をベースにしたグラフィカルなフロントエンドを持ち、[Glade Interface Designer](https://ja.wikipedia.org/wiki/Glade_Interface_Designer "wikilink") で設計されている。Anaconda はまた、[IBM ESA/390](https://ja.wikipedia.org/wiki/IBM_ESA/390 "wikilink") メインフレームのような[ラインプリンタ](https://ja.wikipedia.org/wiki/ラインプリンタ "wikilink")を備えたコンピュータをサポートする、カスタムテキストフロントエンドを持っている。

## 外部リンク

  - [Anaconda 公式ページ（英語）](http://fedoraproject.org/wiki/Anaconda)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Python](https://ja.wikipedia.org/wiki/Category:Python "wikilink")