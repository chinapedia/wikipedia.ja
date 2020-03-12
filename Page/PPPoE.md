> この記事は[PPPoE](https://ja.wikipedia.org/wiki/PPPoE)から翻訳されています。


|                                        |                                                            |                                                       |                                                       |   |                                                 |   |
| -------------------------------------- | ---------------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | - | ----------------------------------------------- | - |
| *アプリケーション層*                            | [FTP](../Page/File_Transfer_Protocol.md "wikilink")        | [SMTP](https://ja.wikipedia.org/wiki/SMTP "wikilink") | [HTTP](https://ja.wikipedia.org/wiki/HTTP "wikilink") | … | [DNS](../Page/Domain_Name_System.md "wikilink") | … |
| *トランスポート層*                             | [TCP](../Page/Transmission_Control_Protocol.md "wikilink") | [UDP](../Page/User_Datagram_Protocol.md "wikilink")   |                                                       |   |                                                 |   |
| *インターネット層*                             | [IPv4](../Page/IPv4.md "wikilink")                         | [IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink") |                                                       |   |                                                 |   |
| **リンク層**                               | [PPP](../Page/Point-to-Point_Protocol.md "wikilink")       |                                                       |                                                       |   |                                                 |   |
| **PPPoE**                              |                                                            |                                                       |                                                       |   |                                                 |   |
| [イーサネット](../Page/イーサネット.md "wikilink") |                                                            |                                                       |                                                       |   |                                                 |   |

**PPPoEとTCP/IPの[プロトコルスタック](../Page/プロトコルスタック.md "wikilink")**

**PPPoE**（**Point-to-Point Protocol over Ethernet**）は、[イーサネットフレーム](https://ja.wikipedia.org/wiki/イーサネットフレーム "wikilink")上に[PPPフレームを](../Page/Point-to-Point_Protocol.md "wikilink")[カプセル化するための](https://ja.wikipedia.org/wiki/カプセル化_\(通信\) "wikilink")[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。RFC 2516によって定義される。主に[DSLや](../Page/デジタル加入者線.md "wikilink")[CATV](../Page/ケーブルテレビ.md "wikilink")、[FTTH](../Page/FTTH.md "wikilink")などでの[インターネット](../Page/インターネット.md "wikilink")接続サービスでの[ブリッジ接続用に利用される](../Page/ブリッジ_\(ネットワーク機器\).md "wikilink")。

[イーサネット](../Page/イーサネット.md "wikilink")ではPPPoEを使わなくても、IPパケットを直接扱うことができる。あえてPPPoEを使うのは、PPPが持つユーザ認証などの機能を使うためである。代償として[MTU減少をはじめとする](../Page/Maximum_Transmission_Unit.md "wikilink")[オーバーヘッド](https://ja.wikipedia.org/wiki/オーバーヘッド "wikilink")が発生する。

2000年頃、[ISP](https://ja.wikipedia.org/wiki/ISP "wikilink")の[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")へのDSL接続を介してパケットをトンネリングするための技術として使われだした。2005年のネットワークの技術書には、「ほとんどのDSLプロバイダは、[認証](../Page/認証.md "wikilink")・[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")・[圧縮](https://ja.wikipedia.org/wiki/圧縮 "wikilink")のためにPPPoEを使用する」と書かれている\[1\]。一般的なPPPoEの利用では、ユーザー名とパスワードでユーザーを認証するために[PAPや](https://ja.wikipedia.org/wiki/Password_Authentication_Protocol "wikilink")[CHAPが使用される](https://ja.wikipedia.org/wiki/Challenge-Handshake_Authentication_Protocol "wikilink")\[2\]。

[カスタマ構内設備](https://ja.wikipedia.org/wiki/カスタマ構内設備 "wikilink")においては、PPPoEは、[ブロードバンドルーター](https://ja.wikipedia.org/wiki/ブロードバンドルーター "wikilink")で実装される場合と、ルーティングを行わない[DSLモデム](https://ja.wikipedia.org/wiki/DSLモデム "wikilink")を使用する場合には、PC上で実装される場合とがある。2016年現在では、ほとんどのOSがPPPoEをサポートしている。

## PPPoEのステージ

PPPoEは、以下の2つのステージを持つ。

### ディスカバリステージ

伝統的なPPPは、すでに確立されたダイヤルアップ接続やATMの上での接続であり、このような接続では、送信したPPPフレームはすべて対向側に到達する。

しかし、イーサネットのネットワークは、ネットワークの各々のノードがその他のノードにアクセスすることができるマルチ・アクセスである。イーサネット・フレームは、転送先のノードのハードウェア・アドレス（[MACアドレス](../Page/MACアドレス.md "wikilink")）を含み、これによってフレームが意図された宛先に到達する。

そのため、イーサネットを介した接続を樹立するためのPPP制御パケットを送信する前に、相手のMACアドレスを互いに知っていなければならない。ディスカバリステージで、MACアドレスの伝達を行う。また、以降のパケットの交換のために使うSession IDの確立も行う。

### PPPセッションステージ

ディスカバリステージによりPPPoEのセッションが確立すると、PPPセッションステージへ進む。

## PPPoEディスカバリ（PPPoED）

伝統的なPPPは[ピア・ツー・ピアである](../Page/Peer_to_Peer.md "wikilink")。それに対しPPPoEは、1つの物理的接続を介して複数のホストがサービスプロバイダに接続できることから、本質的に[クライアントサーバモデル](../Page/クライアントサーバモデル.md "wikilink")である。

PPPoEディスカバリは、クライアントの働きをするホストコンピュータとサーバの働きをするISPのアクセス・コンセントレータの間で、以下の4つの段階を踏む。最後のPADTは、既存のセッションを閉じるために使用される。

### クライアント→サーバ：Initiation（PADI）

**PADI**は「PPPoE Active Discovery Initiation」の略である\[3\]。

ユーザがDSLを用いてインターネットにダイヤルアップ接続するとき、まずユーザのコンピュータは[インターネットサービスプロバイダ](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")の(POP)のDSLアクセス・コンセントレータ(DSL-AC)を見つけなければならない。イーサネット上の通信は、[MACアドレス](../Page/MACアドレス.md "wikilink")を介してのみ行われる。そのため、コンピュータがDSL-ACのMACアドレスを知らない場合は、[ブロードキャスト](../Page/ブロードキャスト.md "wikilink")によってPADIパケットを送信する。PADIパケットには、送信元のコンピュータのMACアドレスが含まれている。

#### PADIパケットの例

    Frame 1 (44 bytes on wire, 44 bytes captured)
    Ethernet II, Src: 00:50:da:42:d7:df, Dst: ff:ff:ff:ff:ff:ff
    PPP-over-Ethernet Discovery
      Version: 1
      Type 1
      Code Active Discovery Initiation (PADI)
      Session ID: 0000
      Payload Length: 24
    PPPoE Tags
      Tag: Service-Name
      Tag: Host-Uniq
        Binary Data: (16 bytes)

`Src`（source）は、PADIの送信元のMACアドレスである。`Dst`（destination）はブロードキャストアドレスである。PADIパケットは1つ以上のDSL-ACに到達する。「Service-Name」タグに記載されたDSL-ACのみが応答を行う。

### サーバ→クライアント：Offer(PADO)

**PADO**は「PPPoE Active Discovery Offer」の略である\[4\]。

ユーザのコンピュータがPADIパケットを送信すると、DSL-ACはPADIに記載されたMACアドレスを用いてPADOパケットを返信する。

PADOパケットにはDSL-ACのMACアドレス・名前・サービス名が含まれている。複数のPOPのDSL-ACがPADOを返信してきた場合、ユーザのコンピュータは名前とサービス名から適切なDSL-ACを選択する。

#### PADOパケットの例

    Frame 2 (60 bytes on wire, 60 bytes captured)
    Ethernet II, Src: 00:0e:40:7b:f3:8a, Dst: 00:50:da:42:d7:df
    PPP-over-Ethernet Discovery
      Version: 1
      Type 1
      Code Active Discovery Offer (PADO)
      Session ID: 0000
      Payload Length: 36
    PPPoE Tags
      Tag: AC-Name
        String Data: IpzbrOOl
      Tag: Host-Uniq
        Binary Data: (16 bytes)

`AC-Name` 以下の `String data`はDSL-ACの名前である。`Src`はDSL-ACのMACアドレスである。

### クライアント→サーバ: request(PADR)

**PADR**は「PPPoE active discovery request」の略である\[5\]。

PADRパケットは、ユーザのコンピュータから選択されたDSL-ACへ送信される。PADRパケットによりPPPoEセッションの開始を要求する。

### サーバ→クライアント: session-confirmation(PADS)

**PADS**は"PPPoE Active Discovery Session-confirmation"の略である\[6\]。

PADSパケットにより、PPPoEのセッションIDをクライアントに通知する。ここで、DSL-ACとユーザのコンピュータの間のPPPoEセッションが確立される。

### どちらかからもう一方へ: termination(PADT)

**PADT**は「PPPoE Active Discovery Termination」の略である\[7\]。

このパケットは、POPとの接続を切断するときに送信される。ユーザのコンピュータとDSL-ACのどちら側からも送信される可能性がある。

## 脚注

## 関連項目

  - [Point-to-Point Protocol](../Page/Point-to-Point_Protocol.md "wikilink") (PPP)
  - [Point-to-Point Tunneling Protocol](https://ja.wikipedia.org/wiki/Point-to-Point_Tunneling_Protocol "wikilink")
  - [pppd](https://ja.wikipedia.org/wiki/pppd "wikilink")

## 外部リンク

  - RFC 2516 - A Method for Transmitting PPP Over Ethernet(PPPoE)
  - RFC 3817 - [Layer 2 Tunneling Protocol](../Page/Layer_2_Tunneling_Protocol.md "wikilink")(L2TP) Active Discovery Relay for PPP over Ethernet(PPPoE)
  - RFC 4638 - Accommodating a Maximum Transit Unit/Maximum Receive Unit(MTU/MRU) Greater Than 1492 in the Point-to-Point Protocol over Ethernet(PPPoE)
  - RFC 4938 - PPP Over Ethernet(PPPoE) Extensions for Credit Flow and Link Metrics
  - [US Patent 6891825](http://www.google.com/patents/US6891825) Method and system of providing multi-user access to a packet switched network

[Category:トンネリング](https://ja.wikipedia.org/wiki/Category:トンネリング "wikilink") [Category:リンク層プロトコル](https://ja.wikipedia.org/wiki/Category:リンク層プロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.
2.
3.  <http://tools.ietf.org/html/rfc2516#section-5.1>
4.  <http://tools.ietf.org/html/rfc2516#section-5.2>
5.  <http://tools.ietf.org/html/rfc2516#section-5.3>
6.  <http://tools.ietf.org/html/rfc2516#section-5.4>
7.  <http://tools.ietf.org/html/rfc2516#section-5.5>