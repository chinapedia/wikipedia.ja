> この記事は[Stream Control Transmission Protocol](https://ja.wikipedia.org/wiki/Stream_Control_Transmission_Protocol)から翻訳されています。


**Stream Control Transmission Protocol**（ストリーム制御伝送プロトコル、ストリーム コントロール トランスミッション プロトコル、SCTP）は、[2000年](../Page/2000年.md "wikilink")に[SIGTRAN](https://ja.wikipedia.org/wiki/SIGTRAN "wikilink") ワーキンググループによって定義された[トランスポート層](../Page/トランスポート層.md "wikilink")の[プロトコル](../Page/プロトコル.md "wikilink")である。

  - RFC 4960 - Stream Control Transmission Protocol
  - RFC 3286 - 導入テキスト

[輻輳制御](https://ja.wikipedia.org/wiki/輻輳制御 "wikilink")を行い、到着順序を保証する信頼性のあるメッセージ転送を行うという点で、同じ層のプロトコルである[TCPと同様のサービスを提供する](../Page/Transmission_Control_Protocol.md "wikilink")。TCP はバイト (byte) 指向であり、SCTP はフレーム・メッセージのやり取りである。

## 利点

SCTPの利点は以下の通り。

  - マルチ・ホーミングのサポート。コネクションのエンドポイントは複数のIPアドレスを持つことができ、ホストやネットワーク・カードの障害時に[フェイルセーフ](../Page/フェイルセーフ.md "wikilink")が可能。
  - 別個のストリーム内のチャンクによる[データ転送](https://ja.wikipedia.org/wiki/データ転送 "wikilink")。これにより、TCPのバイトストリーム転送に見られるような、不必要なhead-of-the-lineブロッキング（待ち行列の先頭のデータがその後ろの転送を妨げること）を解消することができる。
  - 経路選択とモニタリング。「プライマリ」データ転送経路を選択し、その転送経路の接続性をテストする。
  - 検証と応答確認メカニズム。フラッディング攻撃からの保護や、重複あるいは欠損したデータ・チャンクの通知を提供する。

元々SCTPは電話網のシグナリング・プロトコルである[No.7共通線信号方式](https://ja.wikipedia.org/wiki/共通線信号No.7 "wikilink") (SS7) をIP上で転送することを意図しており、SS7信号網の信頼性を[IP網](https://ja.wikipedia.org/wiki/IP網 "wikilink")で再現することを目的としている。この[IETFの作業は](../Page/Internet_Engineering_Task_Force.md "wikilink")[SIGTRAN](https://ja.wikipedia.org/wiki/SIGTRAN "wikilink")として知られている。一方で他の用途も提案されており、その一例として[RADIUS](../Page/RADIUS.md "wikilink")の後継である[DIAMETER](https://ja.wikipedia.org/wiki/DIAMETER "wikilink")での利用が挙げられる。

## 実装

SCTP は次の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")で実装・導入されている。

  - [Linux](../Page/Linux.md "wikilink") kernel 2.4/2.6
  - [Solaris](../Page/Solaris.md "wikilink") 10（[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")）
  - [FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")（[KAME](https://ja.wikipedia.org/wiki/KAME "wikilink")プロジェクト）
  - QNX Neutrino Realtime OS
  - [AIX](../Page/AIX.md "wikilink") Version 5
  - Oracleの提供するWindows以外のJava SE 7実装([Java\#Java SE 7（2011年7月28日）](https://ja.wikipedia.org/wiki/Java#Java_SE_7（2011年7月28日） "wikilink"))

この他、様々なサードパーティ製の実装が他のオペレーティングシステムで利用可能である。

ユーザスペースで実装されたライブラリ:

  - The SCTP library (sctplib) [1](http://www.sctp.de/sctp-download.html)
  - Microsoft Windows XP で動くSCTPlibの実装 [2](http://www.sctp.be/sctplib/index.htm)

The following applications implement SCTP:

  - <http://spot-on.sf.net> - P2P library
  - <http://goldbug.sf.net> - Instant Messenger

[LTEやその後継規格のLTE](https://ja.wikipedia.org/wiki/Long_Term_Evolution "wikilink")-Advancedでは制御信号の送受信のトランスポート層にSCTPを使用している\[1\]。

## 関連項目

  - [トランスポート・プロトコルの比較](https://ja.wikipedia.org/wiki/トランスポート層#トランスポート・プロトコルの比較 "wikilink")
  - [Datagram Transport Layer Security](https://ja.wikipedia.org/wiki/Datagram_Transport_Layer_Security "wikilink")

## RFCs

  - RFC 5062 - Security Attacks Found Against the Stream Control Transmission Protocol (SCTP) and Current Countermeasures
  - RFC 5061 - Stream Control Transmission Protocol (SCTP) Dynamic Address Reconfiguration
  - RFC 5043 - Stream Control Transmission Protocol (SCTP) Direct Data Placement (DDP) Adaptation
  - RFC 4960 - Stream Control Transmission Protocol
  - RFC 4895 - Authenticated Chunks for the Stream Control Transmission Protocol (SCTP)
  - RFC 4820 - Padding Chunk and Parameter for the Stream Control Transmission Protocol (SCTP)
  - RFC 4460 - Stream Control Transmission Protocol (SCTP) Specification Errata and Issues
  - RFC 3873 - Stream Control Transmission Protocol (SCTP) Management Information Base (MIB)
  - RFC 3758 - Stream Control Transmission Protocol (SCTP) Partial Reliability Extension
  - RFC 3554 - On the Use of Stream Control Transmission Protocol (SCTP) with IPsec
  - RFC 3436 - Transport Layer Security over Stream Control Transmission Protocol
  - RFC 3309 - Stream Control Transmission Protocol (SCTP) Checksum Change（RFC 4960 により廃止）
  - RFC 3286 - An Introduction to the Stream Control Transmission Protocol
  - RFC 3257 - Stream Control Transmission Protocol Applicability Statement
  - RFC 2960 - Stream Control Transmission Protocol（RFC 3309 により更新 RFC 4960 により廃止）

## 脚注

<references/>

## 外部リンク

  - [SCTPによるネットワーキングの向上](http://www.ibm.com/developerworks/jp/linux/library/l-sctp/) - IBM developerWorks Japan
  - [JavaでのStream Control Transport Protocol（SCTP）](http://www.oracle.com/technetwork/jp/articles/java/jdk7-sctp-434501-ja.html) - Oracle Technology Network
  - [SCTPヘッダ](http://www.asahi-net.or.jp/~aa4t-nngk/ipttut/output/sctpheaders.html) - Iptablesチュートリアル
  - [Stream Control Transmission Protocol (SCTP)](http://download.oracle.com/docs/cd/E19253-01/819-0392/sockets-17/index.html) - Solaris 10『プログラミングインタフェース』 第 8 章 ソケットインタフェース
  - [sigtran.org （英文）](http://www.sigtran.org/)
  - [Signaling Transport (sigtran)（英文）](http://www.ietf.org/html.charters/sigtran-charter.html)
  - [OpenSS7 Project （英文）](http://www.openss7.org/)
  - [The Linux Kernel SCTP (lksctp) project （英文）](http://sourceforge.net/projects/lksctp/)
  - [www.sctp.org （英文）](http://www.sctp.org/)
  - [www.sctp.de （英文）](http://www.sctp.de/)

[Category:トランスポート層プロトコル](https://ja.wikipedia.org/wiki/Category:トランスポート層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.  <https://www.nttdocomo.co.jp/binary/pdf/corporate/technology/rd/technical_journal/bn/vol19_1/vol19_1_011jp.pdf> - NTTドコモ テクニカルレポート