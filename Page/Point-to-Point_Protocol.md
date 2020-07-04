> この記事は[Point-to-Point Protocol](https://ja.wikipedia.org/wiki/Point-to-Point_Protocol)から翻訳されています。


**Point-to-Point Protocol**（ポイントトゥポイントプロトコル、略称**PPP**）は、2点間を接続して[データ通信](../Page/データ通信.md "wikilink")を行うための[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。

## 概要

PPPはSLIP ([Serial Line Internet Protocol](../Page/Serial_Line_Internet_Protocol.md "wikilink")) の後継として[1992年](../Page/1992年.md "wikilink")に規定されたが、現在は[1994年](../Page/1994年.md "wikilink")に規定された版 (RFC 1661) が使われている。PPPはSLIPと異なり、[TCP/IP以外の通信プロトコル](../Page/インターネット・プロトコル・スイート.md "wikilink")（[NetBEUI](../Page/NetBEUI.md "wikilink")、[AppleTalk](../Page/AppleTalk.md "wikilink")など）とも接続できるように設計されているのが特長である。

[ダイヤルアップPPPは](../Page/ダイヤルアップ接続.md "wikilink")、PPPにダイヤル発信や着信の機能を追加したものであり、遠隔地から[電話](../Page/電話.md "wikilink")回線を通じて[ネットワークに](../Page/コンピュータネットワーク.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")を接続するためのプロトコルとして一般に広く利用されてきた。初期の[IIJ](https://ja.wikipedia.org/wiki/IIJ "wikilink")による実装「iij-ppp」が有名である。

PPPの通信は**リンク制御プロトコル**（**LCP**、[Link Control Protocol](../Page/Link_Control_Protocol.md "wikilink")）と**ネットワーク制御プロトコル**（**NCP、**[Network Control Protocol](https://ja.wikipedia.org/wiki/Network_Control_Protocol "wikilink")）の2つの通信プロトコルを使用している。LCPによってパスワード認証プロトコル（PAP、[Password Authentication Protocol](../Page/Password_Authentication_Protocol.md "wikilink")）やCHAP（[Challenge-Handshake Authentication Protocol](../Page/Challenge-Handshake_Authentication_Protocol.md "wikilink")）を使ってユーザ[認証](../Page/認証.md "wikilink")を行ってリンクを確立した後、NCPがそれぞれの通信プロトコルに必要な設定や[認証](../Page/認証.md "wikilink")を行って接続を確立する。

[シリアル通信](../Page/シリアル通信.md "wikilink")の回線を利用する。

複数のPPP回線を束ねることにより[スループット](../Page/スループット.md "wikilink")の向上を図ることがあり、**マルチリンクPPP**と呼ばれる。[ISDN](../Page/ISDN.md "wikilink")や[PHS](../Page/PHS.md "wikilink")などで使われる。

[イーサネット](../Page/イーサネット.md "wikilink")上でPPPによるセッションを確立する方法として**PPPoE**（[次節参照](https://ja.wikipedia.org/wiki/#PPPoE "wikilink")）、[ATM上での同様の方法として](../Page/Asynchronous_Transfer_Mode.md "wikilink")**PPPoA（**PPP over ATM）がある。

|                                                                                   |                                                                                                                                                                                                                                               |                                                                                     |                                                         |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ------------------------------------------------------- |
|                                                                                   |                                                                                                                                                                                                                                               |                                                                                     | [IP](../Page/Internet_Protocol.md "wikilink")           |
| [LCP](../Page/Link_Control_Protocol.md "wikilink")                                | [CHAP](https://ja.wikipedia.org/wiki/Challenge-handshake_authentication_protocol "wikilink") [PAP](https://ja.wikipedia.org/wiki/Password_authentication_protocol "wikilink") [EAP](../Page/Extensible_Authentication_Protocol.md "wikilink") | [IPCP](https://ja.wikipedia.org/wiki/Internet_Protocol_Control_Protocol "wikilink") |                                                         |
| PPP encapsulation                                                                 |                                                                                                                                                                                                                                               |                                                                                     |                                                         |
| [HDLC](../Page/High-Level_Data_Link_Control.md "wikilink")-like Framing           | [PPPoE](https://ja.wikipedia.org/wiki/Point-to-Point_Protocol_over_Ethernet "wikilink")                                                                                                                                                       | [PPPoA](https://ja.wikipedia.org/wiki/Point-to-Point_Protocol_over_ATM "wikilink")  |                                                         |
| [RS-232](../Page/RS-232.md "wikilink")                                            | [POS](https://ja.wikipedia.org/wiki/Packet_over_SONET/SDH "wikilink")                                                                                                                                                                         | [Ethernet](https://ja.wikipedia.org/wiki/Ethernet "wikilink")                       | [ATM](../Page/Asynchronous_Transfer_Mode.md "wikilink") |
| [SONET/SDH](https://ja.wikipedia.org/wiki/Synchronous_Optical_Network "wikilink") |                                                                                                                                                                                                                                               |                                                                                     |                                                         |

**PPPのアーキテクチャ**

## PPPoE

**PPPoE**、**PPPOE** (Point-to-point protocol over Ethernet) は、[イーサネットフレーム](https://ja.wikipedia.org/wiki/イーサネットフレーム "wikilink")上にPPPを[カプセル化する通信プロトコルである](https://ja.wikipedia.org/wiki/カプセル化_\(通信\) "wikilink")。RFC 2516によって定義される。主に[DSLや](../Page/デジタル加入者線.md "wikilink")[CATV](../Page/ケーブルテレビ.md "wikilink")、[FTTH](../Page/FTTH.md "wikilink")等での[インターネット](../Page/インターネット.md "wikilink")接続サービスでの[ブリッジ接続用に利用される](../Page/ブリッジ_\(ネットワーク機器\).md "wikilink")。

[イーサネット](../Page/イーサネット.md "wikilink")ではPPPoEを使わなくても、IPパケットを直接扱うことができる。あえてPPPoEを使うのは、PPPが持つユーザ認証などの機能を使うためである。代償として[MTU減少をはじめとする](../Page/Maximum_Transmission_Unit.md "wikilink")[オーバーヘッド](https://ja.wikipedia.org/wiki/オーバーヘッド "wikilink")が発生する。

## 関連項目

  - [pppd](https://ja.wikipedia.org/wiki/pppd "wikilink")
  - [High-Level Data Link Control](../Page/High-Level_Data_Link_Control.md "wikilink")（HDLC）
  - [ISDN](../Page/ISDN.md "wikilink")
  - [RADIUS](../Page/RADIUS.md "wikilink")
  - [Extensible Authentication Protocol](../Page/Extensible_Authentication_Protocol.md "wikilink")（EAP）

## 外部リンク

  - RFC 1661 - The Point-to-Point Protocol (PPP)
  - RFC 2516 - A Method for Transmitting PPP Over Ethernet (PPPoE)
  - [RASPPPOE](http://www.raspppoe.com/) - PPPoE プロトコル

[Category:リンク層プロトコル](https://ja.wikipedia.org/wiki/Category:リンク層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")