> この記事は[BitTorrent](https://ja.wikipedia.org/wiki/BitTorrent)から翻訳されています。


**BitTorrent**（ビットトレント）は、[ブラム・コーエン](../Page/ブラム・コーエン.md "wikilink")によって開発された、[Peer to Peerを用いたファイル転送用](../Page/Peer_to_Peer.md "wikilink")[プロトコル](../Page/プロトコル.md "wikilink")及びその通信を行う[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。「急流のように速く（ファイルを）落とせる」という意味を持つ。メインラインと呼ばれる本家の**BitTorrent client**の他にも様々な互換クライアントが存在する。

## 概要

開発者のコーエンは、かつて所属していたベンチャー企業で、P2Pプロトコルをベースにした情報コンテンツ流通プラットフォームの構築プロジェクトに携わった（プロジェクトは頓挫）。その際、従来のP2Pネットワークがピアの帯域を有効に利用していないことやその信頼性が低いことに不満を感じ、それらの欠点を解消するBitTorrentの開発を[2001年](../Page/2001年.md "wikilink")に一人で始めた。[2002年](../Page/2002年.md "wikilink")にP2Pプロトコルのファイナライズを、[2003年](../Page/2003年.md "wikilink")にクライアントソフトをリリースした\[1\]。2003年[4月](https://ja.wikipedia.org/wiki/4月 "wikilink")に[Red Hat Linux](../Page/Red_Hat_Linux.md "wikilink") 9がリリースされた際に、その[ISOイメージ](https://ja.wikipedia.org/wiki/ISOイメージ "wikilink")をドイツ人の一利用者がBitTorrentで公開し、3日間で3万個分のISOイメージが配布されたことで注目されるようになった\[2\]。

現在では、主要な[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")および[オープンソース](../Page/オープンソース.md "wikilink")ソフトウェアのほか、音楽や映画、商用アプリケーションを提供するために、BitTorrentが利用されている。

BitTorrentで配布されているファイルのダウンロードには、BitTorrentプロトコルを実装した[クライアントソフトウェアを利用する](https://ja.wikipedia.org/wiki/BitTorrent#主なクライアントソフトウェア "wikilink")。

インターネットでのBitTorrentが占めるトラフィックに関する報告は複数ある。CableLabs（北米CATV業界の研究機関）はCATVの上りトラフィックの55%\[3\]、英国調査会社CacheLogicはインターネットのトラフィックの35%\[4\]、別の論文はブロードバンドトラフィックの18%\[5\]であると報告している。

## 特徴

[frame](https://ja.wikipedia.org/wiki/ファイル:Torrentcomp_small.gif "wikilink") BitTorrentがこれまでのソフトウェアと大きく異なるのは、従来のインターネットにおける法則に反して、「人気のあるファイルであればあるほど、[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")が速くなる」という特徴である（[Winny](../Page/Winny.md "wikilink")など一部のP2Pプロトコルと同じ特徴）。

[Napsterに代表される従来の](https://ja.wikipedia.org/wiki/Napster#ファイル共有ソフト・サービスとしてのNapster "wikilink")[P2Pソフトウェアの構図は](../Page/Peer_to_Peer.md "wikilink")、一極集中型であった。これは、限られた数の豊富な[帯域](https://ja.wikipedia.org/wiki/帯域 "wikilink")を持っているユーザの周りに、帯域の貧弱な大量のユーザがぶら下がる構図である。このため、ある一つのファイルを取得するためにユーザが集まると、ダウンロード要求が一極集中し、全体の拡散速度としても豊富といわれた帯域を占有するだけの速度しか出すことができない。

この現象に対してBitTorrentでは、「相手（[ピア](../Page/ピア.md "wikilink")）からファイルの一部を受けとるには、自分もファイルの一部を渡さなければならない」という規則を導入し、貧弱な帯域を持つユーザでも、全体のファイル配布に協力できるようにした。これにより、人気のあるファイルに対する要求であっても、それだけ多くのユーザが配布に協力することになり、結果としてユーザ全体へ速く浸透することができる。

また、この特徴より、自分からアップロードするのは、ダウンロード中かダウンロードが完了したファイルのみである。Winnyなどとは異なり、自分がダウンロードしていないファイルのアップロードに加担させられるということが起こらないのも大きな特徴である。

また、BitTorrentは、従来のP2Pに対する進歩というだけではなく、インターネット上でのファイル配布の可能性を広げた。一般的にファイルを配布する際には、[サーバ](../Page/サーバ.md "wikilink")からそれぞれのユーザが別々にダウンロードするため、サーバの帯域が配布可能量を決めていた。しかし、BitTorrentを用いることでユーザ同士の帯域が利用可能になり、より多くのユーザにファイルを配布することができるようになる。

[2006年](../Page/2006年.md "wikilink")[10月23日](../Page/10月23日.md "wikilink")に、BitTorrent, Inc.とPC周辺機器（ネットワーク機器）メーカーである[ASUS](../Page/ASUS.md "wikilink")、[Planex](../Page/プラネックスコミュニケーションズ.md "wikilink")、[QNAP](https://ja.wikipedia.org/wiki/QNAP "wikilink")が提携し、BitTorrentクライアントを内蔵した[ルーター](../Page/ルーター.md "wikilink")や[NASを発売することを発表した](../Page/ネットワークアタッチトストレージ.md "wikilink")。

BitTorrentがこれまでのP2Pソフトウェアともう一つ大きく異なるのは、indexing web site (index home page) からインデックストレントファイルをダウンロードしてからでないと、本体ファイルをP2Pからダウンロードできないということである。この点は[Winny](../Page/Winny.md "wikilink")、[Share](../Page/Share_\(ソフトウェア\).md "wikilink")、[Perfect Dark](https://ja.wikipedia.org/wiki/Perfect_Dark "wikilink")、[LimeWire](../Page/LimeWire.md "wikilink")などの他のP2Pソフトとは異なる特徴である。

## 用語と説明

  - インデックスサイト (indexing web site)
    トレントファイルのインデックスを保持しており、トレントファイルを検索できるサイト
  - トレントファイル
    トラッカーへのリンクを含むインデックスとなるファイル。[拡張子](../Page/拡張子.md "wikilink")が「.torrent」となっており、[クライアントと関連づけがされている](../Page/クライアント_\(コンピュータ\).md "wikilink")。これを読み込むことによりクライアントはトラッカーと接続し、ピアの情報を受取り、ダウンロードが開始される。これ自体はただのインデックスにすぎないので、本体ファイルをまったく含まない。
  - ピア (peer)
    直接接続してデータのやりとりを行っているコンピュータ\[6\]。
  - トラッカー (tracker)
    新規接続者にピアのIPアドレスを教える[サーバ](../Page/サーバ.md "wikilink")。
  - シード／シーダー (seed/seeder)
    完全なファイルを提供しているコンピュータ\[7\]。最初の提供者についても、ダウンロードが完了したものについてもいう。
  - リーチャー (leecher)
    ダウンロード中のコンピュータ。本来、開発者のコーエンは、ピアにアップロードせずにダウンロードだけを試みるものに対してこの言葉を使っているが、今では、広くダウンロード中のピアを呼ぶのに使われている。
  - スウォーム (swarm)
    同じトレントファイルにより、同じファイルを提供／ダウンロード中のコンピュータのグループ全体をいう。ほとんどの場合、一つのコンピュータはその一部とだけ、直接データのやりとりを行っている。
  - 共有比／負担率 (share ratio)
    アップロード量とダウンロード量との比。オープンソースソフトウェアなど、開発者が継続的にシードの提供を続けている場合は別として、最低でもこれが1に達するまで共有を続けるのが礼儀とされている\[8\]。トラッカーによってはこの値に準じてシードの速さあるいは量に制限を掛けていることがある\[9\]。
  - 可用性／健康度 (health)
    ピアにあるデータを集めるといくつのファイルができるかを目安として表したもので、小数か%で表示される。1.0または100%を下回ると完全なファイルをダウンロードできない可能性が高い。
  - 99%病
    ファイルのダウンロードが99%ダウンロード完了し、シーダー、リーチャー共あるにもかかわらずダウンロードが完了しない状態。最後のピースが見つからないことが原因であるが、ダウンロードしたままにしておくか、一旦ダウンロードをやめ、再度ダウンロードを開始する事で完了する。

## 主なクライアントソフトウェア

BitTorrentクライアントは様々なプラットフォームに実装され、その多くが[日本語](../Page/日本語.md "wikilink")を含む多言語に対応している。

  - [BitTorrent](http://www.bittorrent.com/intl/ja/)：コーエンおよびBitTorrent, Inc.によって開発、配布されているオリジナルのBitTorrentクライアントで、**Mainline**とも呼ばれる。バージョン5までは[Python](../Page/Python.md "wikilink")によって実装され、[オープンソース](../Page/オープンソース.md "wikilink")として公開されている。BitTorrent, Inc.が[2006年](../Page/2006年.md "wikilink")[12月](https://ja.wikipedia.org/wiki/12月 "wikilink")にWindows用クライアントを開発していた[μTorrent](https://ja.wikipedia.org/wiki/μTorrent "wikilink")を買収した後、バージョン6からはこれをベースにしたものに変更され、それ以降のソースコードも非公開となった。

  - [ABC](http://pingpong-abc.sourceforge.net/) (Yet Another BitTorrent Client)：BitTornadoを元にPythonで実装されている。接続の優先度を調整する機能や、ウェブインターフェースを備える。

  - [BitComet](../Page/BitComet.md "wikilink")：[C++](../Page/C++.md "wikilink")で実装されている。[UPnP](https://ja.wikipedia.org/wiki/UPnP "wikilink")対応[ルーター](../Page/ルーター.md "wikilink")を使っている場合のNAT設定やポート設定、コンピューターのキャッシュ設定を自動で行う。トレントファイルを開いて、複数のファイルの中からダウンロードするファイルを任意で選択することができる。特に、極東アジアで使われているクライアントである。日本もその例外ではなく、多くの情報を日本語で得ることができる。一方で、動作ないし開発思想が利己的であると非難されることがあり、一部のクライアントはBitCometとの接続を禁止している。

  - [BitSpirit](http://www.167bt.com/) ([Eng](http://www.167bt.com/en/index.php))：多言語対応。DHTネットワーク、Gzip圧縮、UPnP、スーパーシード、プロキシ対応など多機能。個別ファイルダウンロード可能。ダウンロードピースマップ表示。TCPIP接続制限解除パッチ装備。

  - [BitThief](http://www.dcg.ethz.ch/projects/bitthief/)：[Javaで動作するクライアントソフトウェア](../Page/Javaプラットフォーム.md "wikilink")。BitTorrentの原則に反してアップロードを行わず、ダウンロードのみおこなうので一部のクライアントは接続を禁止している。言語は英語のみ。

  - [μTorrent](https://ja.wikipedia.org/wiki/μTorrent "wikilink")：uTorrentと表記される場合も。リソースの消費を抑えた軽量なクライアントとして開発されている。2006年[12月7日](../Page/12月7日.md "wikilink")に本家BitTorrentに買収された。多くがオープンソースで開発されているBitTorrentクライアントの中で珍しく、クローズドソースにて提供されている。ただし、元々の製作者はver. 1.6.1を最後に開発には参加していない。トレントファイルを開いて、複数のファイルの中からダウンロードするファイルを任意で選択することができる。Vuze、BitCometと並んで、最もよく使われているクライアントのひとつ。

  - [BitTornado](http://www.bittornado.com/)：Pythonによる実装。クロスプラットホーム。スーパーシードモードを備える。

  - [CTorrent](http://ctorrent.sourceforge.net/)：[C++](../Page/C++.md "wikilink")で実装されている。軽量化や機能拡張を図った[Enhanced CTorrent](http://www.rahul.net/dholmes/ctorrent/)もある。

  - [Deluge](http://deluge-torrent.org/)：Pythonによる実装。UPnPやNAT-PMP、DHTなどに対応する。

  - [Flash Get](http://www.flashget.com/)：最新版で対応している。欲しいファイルだけを入手できる機能もついている。

  - [Free Download Manager](http://www.freedownloadmanager.org/)：Windows用のオープンソースな[ダウンロードマネージャ](../Page/ダウンロードマネージャ.md "wikilink")。BitTorrentにも対応している。日本語対応。

  - [Net Transport](http://www.xi-soft.com/)：[日本語](../Page/日本語.md "wikilink")対応の[ダウンロードマネージャ](../Page/ダウンロードマネージャ.md "wikilink")。ファイルの個別ダウンロード対応。

  - [KTorrent](../Page/KTorrent.md "wikilink")：[KDE](../Page/KDE.md "wikilink")に含まれるクライアント。

  - [Lftp](https://ja.wikipedia.org/wiki/Lftp "wikilink")：コンソール上で使えるクライアント。

  - [LimeWire](../Page/LimeWire.md "wikilink")：Beta版の4.13.0でBitTorrentが実装されている。

  - [Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")：BitTorrentプロトコルを実装した[拡張機能](../Page/拡張機能_\(Mozilla\).md "wikilink")「[FireTorrent](http://www.fireaddons.com/downloads/)」「[MozTorrent](http://moztorrent.mozdev.org/)」「[AllPeers](http://www.allpeers.com/)」の開発が行われている。

  - [Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")：バージョン9より、BitTorrentに正式対応した。米BitTorrent社との間で、商標の使用やBitTorrentサーチエンジンへのアクセスなどに関して提携が結ばれている。

  - [qBittorrent](https://ja.wikipedia.org/wiki/qBittorrent "wikilink")：Qt4を使用して実装された、クロスプラットホームなクライアント。非常に高機能。

  - [QtWeb](https://ja.wikipedia.org/wiki/QtWeb "wikilink")：バージョン3.2より、Torrentクライアント機能を搭載している。

  - ：[ncurses](https://ja.wikipedia.org/wiki/ncurses "wikilink")を使用した[TUIのBitTorrentクライアント](https://ja.wikipedia.org/wiki/テキストユーザインタフェース "wikilink")

  - [Shareaza](../Page/Shareaza.md "wikilink")：[Gnutella2をメインとしたソフトウェアだが](https://ja.wikipedia.org/wiki/Gnutella#グヌーテラ第二世代 "wikilink")、[Gnutella](../Page/Gnutella.md "wikilink")、[eDonkey](https://ja.wikipedia.org/wiki/eDonkey "wikilink")2000の他にBitTorrentプロトコルにも対応している。

  - [Transmission](https://ja.wikipedia.org/wiki/Transmission "wikilink")：[Cによる実装](../Page/C言語.md "wikilink")。クロス・プラットホームバックエンドの上に、シンプルで使いやすいインターフェースを持つ。[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") ([Cocoa](../Page/Cocoa.md "wikilink")), [Linux](../Page/Linux.md "wikilink")/[NetBSD](../Page/NetBSD.md "wikilink")/[FreeBSD](../Page/FreeBSD.md "wikilink")/[OpenBSD](../Page/OpenBSD.md "wikilink") ([GTK](../Page/GTK_\(ツールキット\).md "wikilink")), [BeOS](../Page/BeOS.md "wikilink")/[ZETA](../Page/ZETA.md "wikilink")版が公開されている。非公式だがWindows版もある。

  - [4Gamer Game Loader/Torrentan Network System](http://www.torrentan.net/)：ゲームポータルサイトの[4Gamer.net](../Page/4Gamer.net.md "wikilink")が、[ジャストプレイヤー株式会社](http://www.justplayer.co.jp)と制作している。ゲームのダウンロードに特化している模様。[ベンチマークサイト](http://www.torrentan.net)を見る限り、BitTorrentとの違いが何かあるようであるが、詳細は不明。BitTorrentを使ったベンチマークサイトでもある。

  - [Vuze](../Page/Vuze.md "wikilink")（旧 Azureus）：[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で実装されており、多くのプラットフォームに対応している。細かい設定が可能であり、また、様々なプラグインがある。

  - [迅雷](https://ja.wikipedia.org/wiki/迅雷 "wikilink")（Xunlei、Thunder）：中国圏でよく使われているクライアント。利用者数だけで見れば世界最大のμtorrentに匹敵するとのデータもある。

  - [aria2](https://ja.wikipedia.org/wiki/aria2 "wikilink")：[C++](../Page/C++.md "wikilink")で実装されているクロスプラットフォームなダウンロードマネージャ。[CUIで動作するほか](../Page/キャラクタユーザインタフェース.md "wikilink")、JSON-RPCやXML-RPCでのリモートコントロールに対応。

## 脚注

### 注釈

### 出典

## 関連項目

  - [ImageShack](https://ja.wikipedia.org/wiki/ImageShack "wikilink")

## 外部リンク

  - [BitTorrent 公式サイト](https://www.bittorrent.com/)

[Category:BitTorrent](https://ja.wikipedia.org/wiki/Category:BitTorrent "wikilink") [Category:P2P](https://ja.wikipedia.org/wiki/Category:P2P "wikilink") [Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink") [Category:Web_2.0](https://ja.wikipedia.org/wiki/Category:Web_2.0 "wikilink")

1.
2.
3.
4.
5.
6.  [トレントのシーダーとピアって何なんですか？](http://wiki.nsview.net/What_are_seeders_and_peers_in_torrents%3F)
7.
8.  [ユートレントの共有比について](http://wiki.nsview.net/UTorrent_share_ratio%3F)
9.  [トレントの共有比はダウンロード速度に影響する？](http://yaview.net/q/Does_your_torrent_ratio_affect_your_download_speed%3F_%3F)