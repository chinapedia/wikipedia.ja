> この記事は[Portage](https://ja.wikipedia.org/wiki/Portage)から翻訳されています。


**Portage** は[Gentoo Linuxで使われている](../Page/Gentoo_Linux.md "wikilink")[パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink")である。Gentoo Linuxの他に[Solaris](../Page/Solaris.md "wikilink")にもPortageが移植されているが、この[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")では標準的なパッケージ管理システムではない。よく似たパッケージ管理システムとして[ports](https://ja.wikipedia.org/wiki/ports "wikilink")と呼ばれるものが、[FreeBSD](../Page/FreeBSD.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、および[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")に存在するが、Portageはこのパッケージ管理システムを参考にして作られたものである。

Portageは[ebuild](https://ja.wikipedia.org/wiki/ebuild "wikilink")の階層的なツリーと、[emerge](https://ja.wikipedia.org/wiki/emerge "wikilink")などのコマンドと[gentoolkit](https://ja.wikipedia.org/wiki/gentoolkit "wikilink")などの関連ツールから構成される。ebuildは各ソフトウェアパッケージの依存関係やライセンスなどのメタデータと実際の構築手順が書かれたファイルである。利用者はprofileを選びemergeを走らせることでPortageにオペレーティングシステムを構成するソフトウェアや[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")のパッケージのインストールやメンテナンスを行わせる。Portageによるインストールは基本的に[ソースコード](../Page/ソースコード.md "wikilink")からのコンパイルである。

Portageの名前とデザインはFreeBSDや[OpenBSD](../Page/OpenBSD.md "wikilink")などの[BSD系OS](https://ja.wikipedia.org/wiki/BSD系OS "wikilink")の[ports](https://ja.wikipedia.org/wiki/ports "wikilink")システムに由来する。portsはMakefileに基づいたシステムであるが、Portageは[Python](../Page/Python.md "wikilink")で記述されている。

## コマンドの例

`emerge -pvuDN world`

  - pオプション:実際には作業を実行せず、どんなことをするのか表示させる。
    vオプション:省略せずコンパイル過程などをすべて表示する。
    uオプション:アップグレードを意味する。
    Dオプション:依存関係のあるソフトウェアまでたどる。
    Nオプション:新しく設定された*USEフラグ*を検知する。
    world:今までにユーザの指示でインストールされたパッケージ。

全体としてこのコマンドは、システム上にあるすべてのプログラムのうち、変更や更新があったものについてのリストを表示せよ、という意味になる。pオプションを取り除くと、実際に更新作業が実行される。

## 関連項目

  - [APT](../Page/APT.md "wikilink")
  - [Gentoo Linux](../Page/Gentoo_Linux.md "wikilink")
  - [ebuild](https://ja.wikipedia.org/wiki/ebuild "wikilink")

## 外部リンク

  -
[Category:フリーパッケージ管理システム](https://ja.wikipedia.org/wiki/Category:フリーパッケージ管理システム "wikilink")