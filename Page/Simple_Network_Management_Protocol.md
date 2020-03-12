> この記事は[Simple Network Management Protocol](https://ja.wikipedia.org/wiki/Simple_Network_Management_Protocol)から翻訳されています。


**Simple Network Management Protocol**（簡易ネットワーク管理プロトコル、またはシンプル ネットワーク マネージメント プロトコル、SNMP）は、[DARPAモデル](https://ja.wikipedia.org/wiki/DARPAモデル "wikilink")に準じた[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")上のネットワーク機器を監視（**モニタリング**）・制御するための情報の通信方法を定める[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。

## 概要

巨大なネットワーク上で、数多くの機器の状態を把握するためには、この規格化されたプロトコルを使い、機器からの情報を集めて監視や制御を行う。コンピュータ等の能動的な機器以外にも[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")や[ハブなどもSNMPを使って監視することが出来る](../Page/ハブ_\(ネットワーク機器\).md "wikilink")。

SNMPに関する最初の[RFCは](../Page/Request_for_Comments.md "wikilink")[1988年](../Page/1988年.md "wikilink")に登場した。

プロトコルを管理情報の構造から分離することにより、SNMPはネットワーク上の非常に多種多様なサブシステムを容易にモニターできるようになった。それは[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")の全ての層を超えて、[データベース](../Page/データベース.md "wikilink")やe-mail、J2EE参照モデルなどにまでその範囲を拡大している。

SNMPのフレームワークの構造は、マスターエージェント、サブエージェント、マネージャからなる3つの主要な要素から構成されている。

  - マスターエージェント : IPアドレスによって特定可能なネットワーク上のノード上のシステムで、ルータや[ホストといったようなものがマスターエージェントと呼ばれる](https://ja.wikipedia.org/wiki/ホスト_\(ネットワーク\) "wikilink")。典型的なマスターエージェントはプロトコルの構文解析や出力の整形などを行うのみである。
    サブエージェント : あるシステム内に複数の管理可能なサブシステムが含まれている場合、マスターエージェントは受け取った要求を、一つまたは複数のサブエージェントに渡す。各サブエージェントはそれぞれがサブシステムに対応していて、サブシステムに対する監視や管理のインタフェースとなっている。マスターエージェントとサブエージェントが外部から見たときに単純な一つのエージェントとみなせるような場合には、それらの役割はまとめて扱われることもある。
    マネージャ : クライアント・サーバ型で言うところのクライアントに相当する。管理者やアプリケーションによる管理操作はここからリクエストとして送出される他、各エージェントからの[トラップを受信したりする](https://ja.wikipedia.org/wiki/SNMPのトラップ "wikilink")。

## アーキテクチャ

SNMP v1 (SNMP version 1) で、次の5つの[Protocol Data Unit](../Page/Protocol_Data_Unit.md "wikilink") (PDU) が定義されている。

  - GET REQUEST: 一部の管理情報を取得するときに使用する
  - GETNEXT REQUEST: 連続する管理情報を取得するときに使用する
  - GET RESPONSE
  - SET REQUEST: 管理するサブシステムに対して変更を加えるときに使用する
  - TRAP (**トラップ**): 管理するサブシステムに関する警告や非同期イベントの通知に使用する

それ以降のバージョンで、次の[PDU](../Page/Protocol_Data_Unit.md "wikilink") が追加されている。

  - GETBULK REQUEST: 高速に複数の管理情報を取得するときに使用する
  - INFORM: マネージャからマネージャへの通信するときに使用する

SNMP は、[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")の[アプリケーション層](../Page/アプリケーション層.md "wikilink") (第7層) に相当する。

SNMP は、下位プロトコルとして[UDP](../Page/User_Datagram_Protocol.md "wikilink") を使用する。一般的に、エージェントが161番ポートを、マネージャが162番ポートを使用している。

### エージェント

管理対象の機器を**エージェント**と呼ぶ (スイッチ、[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")、[ホストなど](https://ja.wikipedia.org/wiki/ホスト_\(ネットワーク\) "wikilink"))。

エージェントは、その役割から次の2つに分類される。

1.  マスター・エージェント
2.  サブ・エージェント

**マスター・エージェント**は、1つ以上の**サブ・エージェント**を監視することができる。

エージェントは、Management Information Base(MIB; [管理情報ベース](../Page/管理情報ベース.md "wikilink")) と呼ばれる一種のデータベースを持つ。

### マネージャ

ネットワークを管理するシステムを**マネージャ** (管理ステーション) と呼ぶ。これは[クライアント・サーバ型](https://ja.wikipedia.org/wiki/クライアント・サーバ型 "wikilink")のクライアントに相当する。

マネージャは、主に次のような管理操作を行う。

  - エージェントへ**リクエスト** (要求) を送信し、その**レスポンス** (応答) を受信する
  - エージェントから**トラップ** (通知) を受信する

### SNMP version 1

**SNMP v1** は、主に次のRFCで定義されている。

  - RFC 1065 - TCP/IPネットワーク上の管理情報の種類と構造
  - RFC 1066 - TCP/IPネットワーク管理のためのMIBの最初の定義
  - RFC 1156 - RFC1066の改訂
  - RFC 1158 - MIB-II と呼ばれるネットワーク機器の持つべき標準データ構造の定義
  - RFC 1213 - RFC1158の改訂
  - RFC 1067 - 簡易ネットワーク管理プロトコル (SNMP)の最初の定義（現在はobsoleted）
  - RFC 1157 - 簡易ネットワーク管理プロトコル (SNMP) RFC1067を置き換えてこちらが現在の標準

SNMP v1 は、[パスワード](../Page/パスワード.md "wikilink")に相当する**コミュニティ**文字列がクリア・テキストで通信されるため、セキュリティの脆弱性が指摘されている。

### SNMP version 2

**SNMP v2**、**SNMP v2p** (RFC 1441 - RFC 1452) は、機能性、セキュリティ、機密性が改善され、マネージャからマネージャへの通信をサポートしている。SNMP v2は、GETNEXT の代わりとしてGETBULK を導入した。しかし、SNMP v2 のセキュリティ・システムは複雑であり、広く採用されていない。

**SNMP v2c** (RFC 1901 - RFC 1908) は、論争の多かったSNMP v2 の新しいセキュリティ・モデルを採用する代わりに、SNMP v1 の**コミュニティ**を改善している。このドラフト案がSNMP v2 の**[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")**となっている。

**SNMP v2u** (RFC 1909 - RFC 1910) は、SNMP v2 の複雑さを受けないように、セキュリティに最大限の妥協を試みている。この変形は**SNMP v2\*** として商品化され、SNMP v3 のセキュリティの枠組みとして採用されている。

### SNMP version 3

**SNMP v3** (RFC 3411 - RFC 3418, **STD0062**) は、SNMP の最新版である ([2004年](../Page/2004年.md "wikilink")現在)。[IETF](../Page/Internet_Engineering_Task_Force.md "wikilink") は、SNMP v3 の登場によって旧式のSNMP が不要 (Obsolete) になると考えている。

実際にSNMP を実装するときは、複数のバージョンをサポートすることが多い (RFC 3584 参照)。

## 補足事項

  - 典型的なマスター・エージェントはプロトコルの構文解析や出力の整形などを行うのみである。
  - マスター・エージェントとサブ・エージェントが外部から見たときに単純な一つのエージェントとみなせるような場合には、それらの役割はまとめて扱われることもある。
  - プロトコルを管理情報の構造から分離することにより、SNMP は多種多様なサブシステムを容易に監視できるようになった。それは[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")の全ての層を超えて、[データベース](../Page/データベース.md "wikilink")や**電子メール**、**J2EE参照モデル**など、その範囲を拡大している。
  - [Request for Comments](../Page/Request_for_Comments.md "wikilink") (RFC) は、[Internet Engineering Task Force](../Page/Internet_Engineering_Task_Force.md "wikilink") (IETF) によって公開されている規格文書である。
  - SNMP に関する最初の[RFC](../Page/Request_for_Comments.md "wikilink") は1988年に提出された。
  - SNMP v2 はセキュリティに関する意見の不一致によって、広く採用されていない。
  - SNMP v2c は"Community-Based Simple Network Management Protocol version 2"であり、非公式だがSNMP v1.5 として知られていた。
  - SNMP v2u は"User-Based Simple Network Management Protocol version 2"である。

## 参考文献

  - SNMPバイブル―インターネット管理への実践ガイド (Professional Computing Series), William Stallings,アジソンウェスレイパブリッシャーズジャパン, 1994/11, ISBN 978-4795296510
  - 入門SNMP ダグラス・R. マウロ (著), ケビン・J. シュミット オライリー・ジャパン, 2002/7/1, ISBN 978-4873110905
  - 実践SNMP教科書―ネットワーク管理ツールの開発と活用 (IT TEXT), 山居 正幸, CQ出版, 2005/3, ISBN 978-4789818759

## 外部リンク

  - [RFC-Editor Webpage (英文)](http://www.rfc-editor.org/)
  - [SNMP old FAQ part 1, 2 Jul 2003 (英文)](http://www.snmp.com/FAQs/snmp-faq-part1.txt)
  - [SNMP old FAQ part 2, 2 Jul 2003(英文)](http://www.snmp.com/FAQs/snmp-faq-part2.txt)
  - [Simple Network Management Protocol FAQ, 2017 (英文)](http://www.snmp.com/FAQs/)
  - RFC (すべて英文):
      - RFC 1065 - *Obsolete* -Structure and Identification of Management Information for TCP/IP-based internets
      - RFC 1066 - *Obsolete* - Management Information Base for Network Management of TCP/IP-based internets
      - RFC 1067 - *Obsolete* - A Simple Network Management Protocol
      - RFC 1098 - *Obsolete* - A Simple Network Management Protocol (SNMP)
      - RFC 1155 - Structure and Identification of Management Information for TCP/IP-based Internets
      - RFC 1156 - Management Information Base for Network Management of TCP/IP-based internets
      - RFC 1157 - A Simple Network Management Protocol (SNMP)
      - RFC 1158 - *Obsolete* - Management Information Base for Network Management of TCP/IP-based internets: MIB-II
      - RFC 1441 - Introduction to version 2 of the Internet-standard Network Management Framework
      - RFC 1448 - *Obsolete* - Protocol Operations for version 2 of the Simple Network Management Protocol (SNMPv2)
      - RFC 1449 - *Obsolete* - Transport Mappings for version 2 of the Simple Network Management Protocol (SNMPv2)
      - RFC 1213 - Management Information Base for Network Management of TCP/IP-based internets: MIB-II
      - RFC 1905 - *Obsolete* - Protocol Operations for Version 2 of the Simple Network Management Protocol (SNMPv2)
      - RFC 1906 - *Obsolete* - Transport Mappings for Version 2 of the Simple Network Management Protocol (SNMPv2)
      - RFC 1907 - *Obsolete* - Management Information Base for Version 2 of the Simple Network Management Protocol (SNMPv2)
      - RFC 2262 - *Obsolete* - Message Processing and Dispatching for the Simple Network Management Protocol (SNMP)
      - RFC 2265 - *Obsolete* - View-based Access Control Model (VACM) for the Simple Network Management Protocol (SNMP)
      - RFC 2271 - *Obsolete* - An Architecture for Describing SNMP Management Frameworks
      - RFC 2272 - *Obsolete* - Message Processing and Dispatching for the Simple Network Management Protocol (SNMP)
      - RFC 2275 - *Obsolete* - View-based Access Control Model (VACM) for the Simple Network Management Protocol (SNMP)
      - RFC 2570 - *Obsolete* - Introduction to Version 3 of the Internet-standard Network Management Framework
      - RFC 2571 - *Obsolete* - An Architecture for Describing SNMP Management Framework
      - RFC 2572 - *Obsolete* - Message Processing and Dispatching for the Simple Network Management Protocol (SNMP)
      - RFC 2573 - *Obsolete* - SNMP Applications
      - RFC 2574 - *Obsolete* - User-based Security Model (USM) for version 3 of the Simple Network Management Protocol (SNMPv3)
      - RFC 2575 - *Obsolete* - View-based Access Control Model (VACM) for the Simple Network Management Protocol (SNMP)
      - RFC 2576 - *Obsolete* - Coexistence between Version 1, Version 2, and Version 3 of the Internet-standard Network Management Framework
      - RFC 2741 - *Memo* - Agent Extensibility (AgentX) Protocol Version 1
      - RFC 3410 - Informational - Introduction and Applicability Statements for Internet Standard Management Framework
      - RFC 3411 - Standard 62 - An Architecture for Describing Simple Network Management Protocol (SNMP) Management Frameworks
      - RFC 3412 - Standard 62 - Message Processing and Dispatching for the Simple Network Management Protocol (SNMP)
      - RFC 3413 - Standard 62 - Simple Network Management Protocol (SNMP) Application
      - RFC 3414 - Standard 62 - User-based Security Model (USM) for version 3 of the Simple Network Management Protocol (SNMPv3)
      - RFC 3415 - Standard 62 - View-based Access Control Model (VACM) for the Simple Network Management Protocol (SNMP)
      - RFC 3416 - Standard 62 - Version 2 of the Protocol Operations for the Simple Network Management Protocol (SNMP)
      - RFC 3417 - Standard 62 - Transport Mappings for the Simple Network Management Protocol (SNMP)
      - RFC 3418 - Standard 62 - Management Information Base (MIB) for the Simple Network Management Protocol (SNMP)
      - RFC 3512 - Informational- Configuring Networks and Devices with Simple Network Management Protocol (SNMP)
      - RFC 3584 - Best Current Practice- Coexistence between Version 1, Version 2, and Version 3 of the Internet-standard Network Management Framework

[Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:ネットワーク管理](https://ja.wikipedia.org/wiki/Category:ネットワーク管理 "wikilink") [Category:システム管理](https://ja.wikipedia.org/wiki/Category:システム管理 "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:マルチエージェントシステム](https://ja.wikipedia.org/wiki/Category:マルチエージェントシステム "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")