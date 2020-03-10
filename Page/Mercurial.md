> この記事は[Mercurial](https://ja.wikipedia.org/wiki/Mercurial)から翻訳されています。


**Mercurial**（マーキュリアル）は、[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")の分散型[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")。 [Python](../Page/Python.md "wikilink")で実装されている（ただし、[バイナリ](../Page/バイナリ.md "wikilink")[diff](https://ja.wikipedia.org/wiki/diff "wikilink")に関しては[C言語](../Page/C言語.md "wikilink")で実装されている）。Mercurialは[コマンドラインプログラムである](https://ja.wikipedia.org/wiki/コマンドラインインタプリタ "wikilink")。全てのコマンドは `hg`で始まる。これはが[水銀](../Page/水銀.md "wikilink")を意味し、その[元素記号](../Page/元素記号.md "wikilink")がであることに由来する。

## 設計目標

設計目標は、

  - 高い性能と[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")
  - サーバが不要な、完全に分散した共同開発環境
  - [テキストファイル](https://ja.wikipedia.org/wiki/テキストファイル "wikilink")と[バイナリファイル](https://ja.wikipedia.org/wiki/バイナリファイル "wikilink")の両方を効率よく扱うこと
  - 概念上はシンプルなままで、高度なブランチ機能とマージ機能を持つこと

である。またMercurialは完全なWebインターフェースを含んでいる。 原著作者はMatt Mackallで、現在も主要開発者である。

## 主な機能

0.9.5版から、他の[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")で管理された[ソースコード](../Page/ソースコード.md "wikilink")を、取り込む機能がサポートされている。\[1\]

## 歴史

[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[4月](https://ja.wikipedia.org/wiki/4月 "wikilink")上旬、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")の開発に利用されていた[BitKeeper](https://ja.wikipedia.org/wiki/BitKeeper "wikilink")のフリー版の配布停止が発表された（詳細については[BitKeeper\#価格変更](https://ja.wikipedia.org/wiki/BitKeeper#価格変更 "wikilink")参照）。Linuxカーネル開発者の一人でもあったMatt MackallはBitKeeperに代わる分散型バージョン管理システムの開発に乗り出し、[4月19日](../Page/4月19日.md "wikilink")に0.1をリリースした。\[2\] 既にLinuxカーネルの原著作者である[Linus Torvaldsも同様の目的で](../Page/リーナス・トーバルズ.md "wikilink")[Git](https://ja.wikipedia.org/wiki/Git "wikilink")の開発を開始していたが、MackallはLinux kernel Mailing List上でMercurialの優位性（データを差分の形式で保持することにより、リポジトリのサイズを節約している、等）を訴え、Torvaldsと論争を繰り広げたこともあった。その後、Linuxカーネル開発においてはGitが採用されることとなったが、現在ではGitもMercurialも互いの機能を取り入れつつ開発が進んでおり、それぞれ様々なプロジェクトで利用されている。

## 脚注

## 外部リンク

  -
  - [Official Mercurial Project Wiki](https://www.mercurial-scm.org/wiki/)

  - [Mercurial 日本語チュートリアル](https://www.mercurial-scm.org/wiki/JapaneseTutorial)

[Category:バージョン管理システム](https://ja.wikipedia.org/wiki/Category:バージョン管理システム "wikilink") [Category:Python](https://ja.wikipedia.org/wiki/Category:Python "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:2005年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2005年のソフトウェア "wikilink")

1.  <http://www.selenic.com/mercurial/wiki/index.cgi/ConvertExtension>
2.