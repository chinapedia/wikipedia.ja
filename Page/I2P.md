> この記事は[I2P](https://ja.wikipedia.org/wiki/I2P)から翻訳されています。


**I2P**（The **I**nvisible **I**nternet **P**roject: 「不可視インターネットプロジェクト」）とは、[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")による通信の始点と終点を[匿名](../Page/匿名.md "wikilink")化し、さらに端点間の通信内容も[暗号](../Page/暗号.md "wikilink")化するという方法で匿名化されたネットワークを構成する[ソフトウェア](../Page/ソフトウェア.md "wikilink")、および[プロトコルの名称である](../Page/通信プロトコル.md "wikilink")。

I2Pにおける通信では端点は暗号化された識別子（[公開鍵暗号](../Page/公開鍵暗号.md "wikilink")の鍵ペアにもとづく）によってネットワーク上で一意に識別される。[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")による通信が[ホスト名](../Page/ホスト名.md "wikilink")（[IPアドレス](../Page/IPアドレス.md "wikilink")）と[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")によって一意に識別される事と似ている。このI2Pの端点識別子からはIPアドレスを知る事ができないため、ネットワークの利用者、[サービス](../Page/サービス.md "wikilink")提供者ともに匿名での通信が可能になっている。

I2Pは既存のTCP/IPネットワークの上にオーバレイされたネットワークとして機能する。I2Pネットワークの[APIを直接使った](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[アプリケーションの開発が計画されているが](../Page/アプリケーションソフトウェア.md "wikilink")、今のところ存在しない。かわりに、既存のアプリケーションをI2Pネットワークを通信路として利用できるようにするための[ブリッジ](../Page/ブリッジ_\(ネットワーク機器\).md "wikilink")（[プロキシ](../Page/プロキシ.md "wikilink")）ソフトウェアI2PTunnelが提供されている。

## メリット

  - I2PTunnelを利用する事で、IPアドレスを公開する事なく[WWWサーバや](../Page/Webサーバ.md "wikilink")[IRC](https://ja.wikipedia.org/wiki/インターネット・リレー・チャット "wikilink")[サーバ](../Page/サーバ.md "wikilink")を提供する事ができ、利用者側もIPアドレスを秘匿してサービスを受ける事ができる。[Apache HTTP Serverや](../Page/Apache_HTTP_Server.md "wikilink")[Mozilla](../Page/Mozilla.md "wikilink")など既存のソフトウェアをそのまま利用できるのが利点である。

## デメリット

  - デフォルトで用意されているI2P HTTP PROXY(127.0.0.1:4444)にはoutboundproxyとしてfalse.i2pが指定されているため、これを通してI2Pネットワーク内だけでなく通常のWebにもアクセスできるが非常に重たい。この機能は専らおまけ程度のものであり、I2PはI2P外のネットワークにアクセスする手段には適していない。
  - 起動し始めて実際に使えるようになるまで数十秒間～1分間ほどのラグを要する。
  - よく知られている匿名ソフトウェア[Tor](../Page/Tor.md "wikilink")とは対照的に、使用するためにしなければならない設定が幾つかある。

## ソフト

現在、Windows、Mac、Linux、Android向けにソフトが提供されておりJavaがあれば作動し、操作はブラウザ上で行う。

  - [I2PSnark](https://ja.wikipedia.org/wiki/I2PSnark "wikilink") I2Pで標準的に実装されている[BitTorrent](../Page/BitTorrent.md "wikilink")クライアント
  - [Vuze](../Page/Vuze.md "wikilink") I2Pネットワークに対応したプラグインが提供されているBitTorrentクライアント
  - [Susimail](https://ja.wikipedia.org/wiki/Susimail "wikilink") I2Pネットワークを通してのみ送受信可能なメールサービス
  - HiddenService(eepsite) I2Pネットワークを通してのみ閲覧可能なWebサーバー

## 外部リンク

  - [Welcome to I2P](http://www.i2p2.de/) I2Pプロジェクトサイト
  - [I2Pの日本語翻訳](https://www.transifex.net/projects/p/I2P/)

[Category:暗号化プロトコル](https://ja.wikipedia.org/wiki/Category:暗号化プロトコル "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:匿名ネットワーク](https://ja.wikipedia.org/wiki/Category:匿名ネットワーク "wikilink") [Category:2003年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2003年のソフトウェア "wikilink")