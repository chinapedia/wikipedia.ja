> この記事は[Freenet](https://ja.wikipedia.org/wiki/Freenet)から翻訳されています。


**Freenet**（**フリーネット**）とは、[情報](https://ja.wikipedia.org/wiki/情報 "wikilink")をやり取りする場合に相手先との通信部分を[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")した[インターネット](../Page/インターネット.md "wikilink")を利用した[ネットワークである](../Page/コンピュータネットワーク.md "wikilink")。

1999年7月、Ian Clarke の論文 "A Distributed Decentralised Information Storage and Retrieval System" （分散自立型情報の保管と検索システム）に基づきFreenetプロジェクトがスタートした。 このプロジェクトの目的はインターネット上での情報発信者の[匿名](../Page/匿名.md "wikilink")を確保し自由な発言・活動を保証することにある。実際に中国・中東諸国で使用されて国家権力を以てしても通信の傍受が不可能なほどである。

## Freenetのフロントエンド

[frost_screenshot.png](https://ja.wikipedia.org/wiki/File:frost_screenshot.png "fig:frost_screenshot.png")

他の多くのP2Pソフトと違ってFreenetは暗号通信[プロトコル](../Page/プロトコル.md "wikilink")に従い相手先と情報をやり取りする機能のみを提供しているため、 ファイル共有などを行う際には[フロントエンド](../Page/フロントエンド.md "wikilink")として別途ソフトウェアを使用しなければならない。 Freenetとこれら[フロントエンド](../Page/フロントエンド.md "wikilink")との情報をやり取りする際にはFCP (Freenet Client Protocol) と呼ばれるAPIが使用されており、 これを使うことでメッセージボードやファイル共有、チャットなどの機能を実装することができる。

### フォーラム

  - \[<http://localhost:8888/freenet:USK@0npnMrqZNKRCRoGojZV93UNHCMN-6UU3rRSAmP6jNLE>,\~BG-edFtdCC1cSH4O3BWdeIYa8Sw5DfyrSV-TKdO5ec,AQACAAE/fms/137/ Freenet Messaging System (FMS)\]: DoS攻撃やスパムなどFrostの問題に対処するために設計されたメッセージサービス。
    [Frost](http://jtcfrost.sourceforge.net/): メッセージボードやファイル共有などのサービス。

### ユーティリティ

  - [FUQID](https://ja.wikipedia.org/wiki/FUQID "wikilink"): ファイルのアップロードならびにダウンロードツール
    [jSite](https://freenetproject.org/jsite.html): ウェブサイトのアップロードツール
    [Infocalypse](http://mercurial.selenic.com/wiki/Infocalypse): Freenet上にmercurialリポジトリの作成ツール

### ライブラリ

  - [FCPLib](https://github.com/freenet/lib-CppFCPLib-official): FCPLib (Freenet Client Protocol Library) はC言語ベースで書かれたクロスプラットフォームのFCPクライアントライブラリ。FCPLibは WIndows NT/2K/XP, Linux, BSD, Solaris, Mac OS Xをサポートしている。

<!-- end list -->

  - [lib-pyFreenet](https://github.com/freenet/lib-pyFreenet-staging): lib-pyFreenetはFreenetの機能をpythonで使用するためのライブラリ。Infocalypseはこれを使用している。

## 脚注

## 関連項目

  - [GNUnet](https://ja.wikipedia.org/wiki/GNUnet "wikilink")
  - [I2P](../Page/I2P.md "wikilink")
  - [Tor](../Page/Tor.md "wikilink")

## 外部リンク

  - [The Freenet Project](http://freenetproject.org/index.php?page=index) Freenet公式サイト

  - [FreenetWiki](http://wiki.freenetproject.org/) FreenetWiki

  - Freenet初心者解説

[Category:P2P](https://ja.wikipedia.org/wiki/Category:P2P "wikilink") [Category:匿名ネットワーク](https://ja.wikipedia.org/wiki/Category:匿名ネットワーク "wikilink")