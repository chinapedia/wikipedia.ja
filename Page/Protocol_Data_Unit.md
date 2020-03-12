> この記事は[Protocol Data Unit](https://ja.wikipedia.org/wiki/Protocol_Data_Unit)から翻訳されています。


[Pdu_and_sdu.svg](https://ja.wikipedia.org/wiki/File:Pdu_and_sdu.svg "fig:Pdu_and_sdu.svg")(MAC)層のprotocol data unit(PDU)は[物理層](../Page/物理層.md "wikilink")の(SDU)となる。\]\]

[電気通信](../Page/電気通信.md "wikilink")において、**protocol data unit**（**PDU**、プロトコルデータユニット）とは、[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")のピアエンティティ（両端）の間で送受信される最小の情報の単位である。

PDUは、[通信プロトコル](../Page/通信プロトコル.md "wikilink")で定義された制御情報（[ヘッダ](https://ja.wikipedia.org/wiki/ヘッダ "wikilink")）部分と、通信データの中身である[ペイロードからなる](https://ja.wikipedia.org/wiki/ペイロード_\(コンピュータ\) "wikilink")。 通信プロトコルスタックの階層化アーキテクチャでは、各層は、特定のタイプやモードのデータ交換に合わせて調整されたプロトコルを実装し、それによって、プロトコルで規定されるPDUが異なる。例えば、[TCPはコネクション型転送モードを実施し](../Page/Transmission_Control_Protocol.md "wikilink")、このプロトコルにおけるPDUはセグメントと呼ばれる。一方、[UDPはコネクションレス型転送モードを実施し](../Page/User_Datagram_Protocol.md "wikilink")、PDUとして[データグラム](https://ja.wikipedia.org/wiki/データグラム "wikilink")を使用する。[インターネット・プロトコル・スイート](../Page/インターネット・プロトコル・スイート.md "wikilink")の下位層である[インターネット層](https://ja.wikipedia.org/wiki/インターネット層 "wikilink")では、PDUはペイロードタイプに関係なく[パケット](../Page/パケット.md "wikilink")と呼ばれる。

## 例

### OSI参照モデル

[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")の各層のPDUは次のようになる\[1\]。

| 階層  | PDU                                        |
| --- | ------------------------------------------ |
| 第4層 | [トランスポート層](../Page/トランスポート層.md "wikilink") |
| 第3層 | [ネットワーク層](../Page/ネットワーク層.md "wikilink")   |
| 第2層 | [データリンク層](../Page/データリンク層.md "wikilink")   |
| 第1層 | [物理層](../Page/物理層.md "wikilink")           |

特定のOSI階層に関する文脈においては、PDUはその階層での表現の同義語として使用されることがある。

### インターネット・プロトコル・スイート

[インターネット・プロトコル・スイート](../Page/インターネット・プロトコル・スイート.md "wikilink")の各層のPDUは次のようになる。

| 階層                                                            | PDU                                                                           |
| ------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [トランスポート層](../Page/トランスポート層.md "wikilink")                    | TCPではTCPセグメント。UDPでは[データグラム](https://ja.wikipedia.org/wiki/データグラム "wikilink")。 |
| [インターネット層](https://ja.wikipedia.org/wiki/インターネット層 "wikilink") | [パケット](../Page/パケット.md "wikilink")                                            |
| [リンク層](../Page/リンク層.md "wikilink")                            | [フレーム](https://ja.wikipedia.org/wiki/フレーム_\(ネットワーク\) "wikilink")              |

[イーサネット](../Page/イーサネット.md "wikilink")上の[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")では、物理層のデータは[イーサネットフレーム](https://ja.wikipedia.org/wiki/イーサネットフレーム "wikilink")によって転送される。

### ATM

[ATMのデータリンク層のPDUは](../Page/Asynchronous_Transfer_Mode.md "wikilink")[セルと呼ばれる](https://ja.wikipedia.org/wiki/Asynchronous_Transfer_Mode#ATMの仕組み "wikilink")。

### media access control protocol data unit

**media access control protocol data unit** (**MPDU**) は、[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")に基づいて通信システム内の[媒体アクセス制御](../Page/媒体アクセス制御.md "wikilink")(MAC)エンティティ間で交換されるメッセージである。

MPDUが(MSDU)よりも大きくなることのあるシステムでは、MPDUはによって複数のMSDUに分割される場合がある。MPDUがMSDUよりも小さいシステムでは、によって、1つのMSDUが複数のMPDUを生成することがある。

### transport protocol data unit

**transport protocol data unit** (**TPDU**) は、ペイロードメッセージの先頭に数バイトのルーティングヘッダを追加したメッセージ[カプセル化フォーマットである](https://ja.wikipedia.org/wiki/カプセル化_\(通信\) "wikilink")。

TPDUには、オーバーヘッドTPDUとバイトあたりのオーバーヘッドの2つの処理がある。

## 関連項目

  - [フレーム (ネットワーク)](https://ja.wikipedia.org/wiki/フレーム_\(ネットワーク\) "wikilink")

  -
  -
## 脚注

## 外部リンク

  - [comp.protocols.iso FAQ](http://www.cl.cam.ac.uk/~mgk25/osi-faq.txt) (search for "PDU")

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:データ転送](https://ja.wikipedia.org/wiki/Category:データ転送 "wikilink")

1.