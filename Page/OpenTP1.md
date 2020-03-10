> この記事は[OpenTP1](https://ja.wikipedia.org/wiki/OpenTP1)から翻訳されています。


**OpenTP1**は[日立製作所](../Page/日立製作所.md "wikilink")が開発・発売している*日立オープンミドルウェアシリーズ*のひとつで、[1994年](../Page/1994年.md "wikilink")に発売された[ソフトウェア](../Page/ソフトウェア.md "wikilink")。[オープンシステム上で](https://ja.wikipedia.org/wiki/オープンシステム_\(コンピュータ\) "wikilink")[オンライントランザクション処理](https://ja.wikipedia.org/wiki/オンライントランザクション処理 "wikilink")（OLTP）を実行する為のソフトウェア名称。1994年[日経BP技術賞](https://ja.wikipedia.org/wiki/日経BP技術賞 "wikilink")システム部門賞受賞。

## 特徴

従来の集中一括型OLTPに比べ、OpenTP1を使用した分散コンピューティング環境下でのOLTPはシステム規模や業務量など、それぞれのシステム固有の状況に応じた構成を柔軟に選択することができる。 また、[プログラムや](../Page/プログラム_\(コンピュータ\).md "wikilink")[データベース](../Page/データベース.md "wikilink")といったソフトウェア資源をハードウェア構成から独立させる事が出来る為、業務量の増加などに伴ったハードウェア構成の変更にもソフトウェア資源がほとんど影響を受けない。

## OpenTP1の構造

OpenTP1はオープンシステムの標準化団体（[X/Open](https://ja.wikipedia.org/wiki/X/Open "wikilink")）で規定している[DTPモデル](https://ja.wikipedia.org/wiki/DTPモデル "wikilink")に準拠している。 そのため、X/Openに準拠した[APIを使用でき](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、X/Openの[XAインタフェースに準拠した](https://ja.wikipedia.org/wiki/X/Open_XA "wikilink")[DBMSなどの各種リソースマネジャと接続することが可能となっている](../Page/データベース管理システム.md "wikilink")。

## プログラミング言語

OpenTP1で使用するプログラム（UAP）は[C言語](../Page/C言語.md "wikilink")、[C++言語](https://ja.wikipedia.org/wiki/C++言語 "wikilink")及び[COBOL](https://ja.wikipedia.org/wiki/COBOL "wikilink")言語が使用可能となっている。 加えて、Windowsで.NETにも対応している。

## 対応しているリソースマネジャ

  - [Oracle database](https://ja.wikipedia.org/wiki/Oracle_database "wikilink")
  - [HiRDB](https://ja.wikipedia.org/wiki/HiRDB "wikilink")
  - [SQL Server](https://ja.wikipedia.org/wiki/SQL_Server "wikilink")
  - [DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")
  - その他日立製作所製のメインフレーム製品各種

## OpenTP1ソフトウェア製品

  - TP1/ServerBase
  - TP1/Link
      -
        分散トランザクション処理の基本制御を行う製品。
  - TP1/EnterpriseEditoin(マルチスレッド,スケジュールキューに対応した高信頼/高性能製品)
  - TP1/FS/DirectAccess
  - TP1/FS/TableAccess
  - TP1/SharedTableAccess
      -
        ユーザデータを管理する製品。
  - TP1/MessageControl
  - TP1/NET/Library
  - TP1/Messaging
      -
        メッセージ制御を行う製品。
  - TP1/Client/J Java上のクライアントプログラムよりTP1にアクセスする製品
  - TP1/Client/P　Windows環境のクライアントプログラムよりTP1にアクセスする製品
  - TP1/Client/W　Unix/Linux環境のクライアントプログラムよりTP1にアクセスする製品
  - uCosminexusTP1/Clientfor.NET Framework　.NET Framework環境のクライアントプログラムよりTP1にアクセスする製品
  - TP1/NET/OSI-TP（プロトコル[OSI/TP](https://ja.wikipedia.org/wiki/OSI/TP "wikilink")）
  - TP1/NET/OSAS-NIF（プロトコル[NIF/OSI](https://ja.wikipedia.org/wiki/NIF/OSI "wikilink")）
  - TP1/NET/UserAgent（プロトコル[OSAS/UA](https://ja.wikipedia.org/wiki/OSAS/UA "wikilink")）
  - TP1/NET/TCP/IP（プロトコル[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")）
  - TP1/NET/C/S560（プロトコル[C/S560](https://ja.wikipedia.org/wiki/C/S560 "wikilink")）
  - TP1/NET/XMAP3（プロトコル[XMAP3](https://ja.wikipedia.org/wiki/XMAP3 "wikilink")）
  - TP1/NET/HSC（プロトコル[HSC](https://ja.wikipedia.org/wiki/HSC "wikilink")）
  - TP1/NET/HDLC（プロトコル[HDLC](https://ja.wikipedia.org/wiki/HDLC "wikilink")）
  - TP1/NET/X25（プロトコル[X.25](https://ja.wikipedia.org/wiki/X.25 "wikilink")）
  - TP1/NET/X25-Extended（プロトコル[X.25 VC](https://ja.wikipedia.org/wiki/X.25_VC "wikilink")）
  - TP1/NET/NCSB（プロトコル[NCSB](https://ja.wikipedia.org/wiki/NCSB "wikilink")）
  - TP1/NET/HNA-NIF（プロトコル[NIF/HNA](https://ja.wikipedia.org/wiki/NIF/HNA "wikilink")）
  - TP1/NET/SecondaryLogicalUnit-TypeP1（プロトコル[SNA](https://ja.wikipedia.org/wiki/SNA "wikilink")）
  - TP1/NET/SecondaryLogicalUnit-TypeP2（プロトコル[SNA](https://ja.wikipedia.org/wiki/SNA "wikilink")）
  - TP1/NET/UserDatagramProtocol（プロトコル[UDP](../Page/User_Datagram_Protocol.md "wikilink")）
      -
        メッセージ通信を行う場合の各種通信[プロトコル](../Page/プロトコル.md "wikilink")対応製品。
  - TP1/MessageQueue
      -
        [メッセージキューイング](https://ja.wikipedia.org/wiki/メッセージキューイング "wikilink")機能を制御する製品。対象はIBM　MQである
  - uCosminexusTP1/Extensionfor.NET Framework　サーバプログラムを.NET Framework上で動作させることができる製品
  - uCosminexusTP1Connector TP1/Client/Jおよび[Cosminexus](https://ja.wikipedia.org/wiki/Cosminexus "wikilink")と連携して動作するリソースアダプタ

## 関連項目

  - *日立オープンミドルウェアシリーズ*
      -
        [JP1](https://ja.wikipedia.org/wiki/JP1 "wikilink")：統合システム運用管理
        [Cosminexus](https://ja.wikipedia.org/wiki/Cosminexus "wikilink")：統合システム構築基盤
        [HiRDB](https://ja.wikipedia.org/wiki/HiRDB "wikilink")：スケーラブルデータベース
        [SEWB3](https://ja.wikipedia.org/wiki/SEWB3 "wikilink")：ソフトウェアエンジニアリングワークベンチ
        [COBOL85](https://ja.wikipedia.org/wiki/COBOL85 "wikilink")：ビジネスアプリケーション環境開発
        [Groupmax](https://ja.wikipedia.org/wiki/Groupmax "wikilink")：[グループウェア](../Page/グループウェア.md "wikilink")
        [EUR](https://ja.wikipedia.org/wiki/EndUserReporting "wikilink")：[帳票](https://ja.wikipedia.org/wiki/帳票 "wikilink")システム構築支援ソフトウェア
        [DocumentBroker](https://ja.wikipedia.org/wiki/DocumentBroker "wikilink")：文書管理ソフトウェア

## 外部リンク

  - [HITACHIミドルウェアプラットフォームソフトウェア総合サイト](http://www.hitachi.co.jp/Prod/comp/soft1/index.html)

[Category:トランザクションモニター](https://ja.wikipedia.org/wiki/Category:トランザクションモニター "wikilink") [Category:日立製作所](https://ja.wikipedia.org/wiki/Category:日立製作所 "wikilink")