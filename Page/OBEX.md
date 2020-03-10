> この記事は[OBEX](https://ja.wikipedia.org/wiki/OBEX)から翻訳されています。


**OBEX**(**OBject EXchange**)は**IrOBEX**とも呼ばれ、デバイス間のバイナリオブジェクトの交換を容易にする[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。

## 概要

OBEXは[IrDA](../Page/IrDA.md "wikilink")の規格の一つであるが、[Bluetooth Special Interest Group](https://ja.wikipedia.org/wiki/Bluetooth_Special_Interest_Group "wikilink")（以下Bluetooth SIGと表記する）や[Open Mobile Alliance](https://ja.wikipedia.org/wiki/Open_Mobile_Alliance "wikilink")（以下OMAと表記する）の[SyncML](https://ja.wikipedia.org/wiki/SyncML "wikilink")派にも支持されている。OBEXの最初のアプリケーションは[PDAの](../Page/携帯情報端末.md "wikilink")[Palm III](../Page/Palm.md "wikilink")。名刺、データ、アプリケーションを交換するために、このPDAや多くの後継機ではOBEXが利用されている。

クライアントがサーバに接続するときに信頼性の高い転送を行う点と、接続した後にオブジェクトの要求・提供を行う点において、OBEXは[HTTPに似ている](../Page/Hypertext_Transfer_Protocol.md "wikilink")。しかし、いくつかの重要な点が異なっている。

  - **転送** - HTTPは通常、[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")ポートの上でレイヤが作られる。OBEXは通常、IrDAデバイス上の[IrLAP](https://ja.wikipedia.org/wiki/IrLAP "wikilink")/[IrLMP](https://ja.wikipedia.org/wiki/IrLMP "wikilink")/[Tiny TPスタック上に実装される](https://ja.wikipedia.org/wiki/Tiny_TP "wikilink")。[Bluetooth](https://ja.wikipedia.org/wiki/Bluetooth "wikilink")の場合、[Baseband](https://ja.wikipedia.org/wiki/Baseband "wikilink")/[Link Manager](https://ja.wikipedia.org/wiki/Link_Manager "wikilink")/[L2CAP](https://ja.wikipedia.org/wiki/L2CAP "wikilink")/[RFCOMM](https://ja.wikipedia.org/wiki/RFCOMM "wikilink")スタック上に実装される。また、他にもこのようなOBEXの*[バインディング](https://ja.wikipedia.org/wiki/バインディング "wikilink")*が可能である。

<!-- end list -->

  - **バイナリデータの伝送** - HTTPは可読なテキストデータを利用する。しかし、OBEXは、要求やオブジェクトについての情報を交換するために、ヘッダ(Header)と呼ばれる[「型(Type)」「データ長(Length)」「値(Value)」の三つ組のバイナリフォーマットを利用する](https://ja.wikipedia.org/wiki/type-length-value "wikilink")。限られたリソースの中でデバイスがデータを解析することが容易である。

<!-- end list -->

  - **セッションのサポート** - HTTPのトランザクションは、もともと状態を保持しない。通常HTTPのクライアントが要求を行うときは、接続を開始し、単一の要求を行い、応答を受け取り、接続を終了する。OBEXの場合、1つのオブジェクトを転送する接続において、複数の関連するオペレーションを送受信することができる。実は、最近のOBEXの仕様追加によって、どのような状態であっても、突然トランザクションを中断し、その後再開することができるようになった。

## Profile

OBEXは多くの上位レイヤにおける「Profile」の元となった。

### IrDA

  - Point and Shoot profile
  - [Infrared Financial Messaging (IrFM)](https://ja.wikipedia.org/wiki/IrFM "wikilink") profile

### Bluetooth SIG

  - Generic Object Exchange Profile
  - Object Push Profile (phone to phone transfers)
  - File Transfer Profile (phone to PC transfers)
  - Synchronization Profile
  - Basic Imaging Profile
  - Basic Printing Profile

### OMA

  - SyncML binding

## サポートされたデバイス

  - ほとんどの[携帯電話](../Page/携帯電話.md "wikilink")
  - Palm III以降のすべての[Palm](../Page/Palm.md "wikilink")
  - [2003年](../Page/2003年.md "wikilink")以降に発売されたほとんどのPDA

## 関連項目

  - [IrDA](../Page/IrDA.md "wikilink")
  - [TransferJet](https://ja.wikipedia.org/wiki/TransferJet "wikilink")

## 外部リンク

  - [Infrared Data Association](http://www.irda.org/) OBEXの最新の仕様書が有料で配布されている。
  - [OpenOBEX](http://www.openobex.org/) OBEXのオープンソースの実装。

[Category:通信](https://ja.wikipedia.org/wiki/Category:通信 "wikilink") [Category:インタフェース規格](https://ja.wikipedia.org/wiki/Category:インタフェース規格 "wikilink") [Category:モバイルネットワーク](https://ja.wikipedia.org/wiki/Category:モバイルネットワーク "wikilink")