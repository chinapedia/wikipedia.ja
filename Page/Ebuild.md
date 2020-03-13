> この記事は[Ebuild](https://ja.wikipedia.org/wiki/Ebuild)から翻訳されています。


**ebuild** は [Gentoo Linux](../Page/Gentoo_Linux.md "wikilink") の [Portage](../Page/Portage.md "wikilink") で使われるパッケージ管理用の [Bash](../Page/Bash.md "wikilink") スクリプトである。

なお、Portage には同名のコマンドも存在するが、ここでは ebuild スクリプトに話を限定する。

## 概要

ebuild スクリプトは「(パッケージ名)-(バージョン)-(リビジョン).ebuild」という命名規則に従ったファイル名で、Portage ツリーの中の (カテゴリー名)/(パッケージ名) という [ディレクトリ](../Page/ディレクトリ.md "wikilink") に納められる。ファイルの中にはパッケージの依存関係やライセンスなどのメタデータと実際のソフトウェアの構築手順が書かれている。構築に際して、Portage は使用されているアーキテクチャと事前に設定された[USEフラグ](https://ja.wikipedia.org/wiki/USEフラグ "wikilink")に従って細かい構成を選択する。これによって、バイナリーパッケージでは得られない構成の柔軟性が得られ、また最適化されたバイナリーの構築が可能となる。

Gentoo Portage リポジトリ にあるほとんどの ebuild はソースコードからプログラムをコンパイルするのに用いられる。しかし、中には [mozilla-firefox-bin](../Page/Mozilla_Firefox.md "wikilink") のようにバイナリパッケージをインストールするものや、ドキュメントやフォントのようなデータをインストールするものがある。

## eclass

多くの ebuild に共通の処理を eclass というファイルにまとめてあり、それを継承(inherit)することで記述量を減らすことができる。 たとえば、[Python](../Page/Python.md "wikilink") で書かれたソフトウェアのパッケージは distutils という標準モジュールを利用してインストールされるものが多いが、このようなパッケージのために distutils.eclass というものが用意されており、これを利用するとほとんど具体的なインストール手順を ebuild スクリプトには書かなくて済む。

## メタデータ

全ての ebuild で必須のメタデータは、

  - DESCRIPTION (パッケージの概要)
  - SRC_URI (ソフトウェア配布元)
  - LICENSE (ソフトウェアライセンス)
  - DEPEND (依存関係)

である。 依存関係には直接的なものだけを記述すれば、間接的に依存するパッケージは Portage が自動で辿る。

## 構築手順

ソースコードからの手動でのインストールに使われる手順と、ほぼ同じ処理が自動で実行される。

多くのパッケージでは、ソフトウェアの構築は大きく分けて「展開」「コンパイル」「インストール」の3段階で行われる。「展開」の段階では、主にダウンロードしたソースコードの [tar](https://ja.wikipedia.org/wiki/tar "wikilink")ball などを展開する。「コンパイル」の段階では、多くの場合、[configure](https://ja.wikipedia.org/wiki/Autotools#configure "wikilink") を実行し、[make](https://ja.wikipedia.org/wiki/make "wikilink") を実行する。「インストール」の段階では、多くの場合、make install を実行する。

なお、Portage では、[sandbag](https://ja.wikipedia.org/wiki/sandbag "wikilink") と呼ばれる保護機能が標準で動作していて、すべての手順が完了するまでの間に、稼動中のルートファイルシステムには変更が及ばないようになっている。

## 関連項目

  - [Gentoo Linux](../Page/Gentoo_Linux.md "wikilink")
  - [Portage](../Page/Portage.md "wikilink")

## 外部リンク

  - [Ebuild HOWTO](http://www.gentoo.org/proj/en/devrel/handbook/handbook.xml?part=2&chap=1)
  - [ebuildの登録ガイド](http://www.gentoo.org/doc/ja/ebuild-submit.xml)
  - [Gentoo Development Guide](http://devmanual.gentoo.org/)

[Category:フリーパッケージ管理システム](https://ja.wikipedia.org/wiki/Category:フリーパッケージ管理システム "wikilink")