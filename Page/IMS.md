> この記事は[IMS](https://ja.wikipedia.org/wiki/IMS)から翻訳されています。


**IMS** （、アイエムエス）は、[IBM](../Page/IBM.md "wikilink")が開発・販売する、[メインフレーム](../Page/メインフレーム.md "wikilink")専用の[データ管理システム](https://ja.wikipedia.org/wiki/データ管理システム "wikilink")。最新版の名称は「IMS Transaction and Database Servers」\[1\]。IMSは[トランザクション処理システムである](../Page/トランザクションモニター.md "wikilink")**IMS TM**(IMS Transaction Manager)と、[階層型の](https://ja.wikipedia.org/wiki/階層型データモデル "wikilink")[データベース管理システム](../Page/データベース管理システム.md "wikilink") (DBMS) である**IMS DB**(IMS Database Manager)から構成される。

## 概要

IMSは、商用では初めての本格的なデータ管理システム（情報管理システム）であり、特に高い信頼性・[可用性](../Page/可用性.md "wikilink")・処理速度・容量が求められるデータ処理に使用される。

IMSは以下の2機能から構成される。

  - IMS Transaction Server

<!-- end list -->

  -
    [トランザクション処理システム](../Page/トランザクションモニター.md "wikilink")。IMS Transaction Manager **(IMS TM)**により実現される。旧称はIMS Data Communication(IMS DC)。

<!-- end list -->

  - IMS Database Server

<!-- end list -->

  -
    [階層型データモデル](https://ja.wikipedia.org/wiki/階層型データモデル "wikilink")の[データベース管理システム](../Page/データベース管理システム.md "wikilink")。IMS Database Manager **(IMS DB)**により実現される。

上記2機能は、1機能のみの使用もできるため、2機能をまとめてIMS TM/DB（旧称IMS DB/DC）とも呼ぶ。IMS DBを別のトランザクション処理システム（[CICS](../Page/CICS.md "wikilink")など）と組み合わせることもできる。[関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink")(RDBMS) である[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")も、IMSに搭載されるDBMSとして開発されてきたと言われる。

IMSは、IBM[メインフレーム](../Page/メインフレーム.md "wikilink")の専用[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である、[MVS](https://ja.wikipedia.org/wiki/MVS "wikilink")、[OS/390](https://ja.wikipedia.org/wiki/OS/390 "wikilink")、[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")上でのみ稼動する。同じIBMメインフレーム専用OSでも、[VM](https://ja.wikipedia.org/wiki/VM "wikilink")や[VSE](https://ja.wikipedia.org/wiki/VSE "wikilink")では稼動しない。（MVS系の基本機能である、複数アドレス空間を使用しているため。）

### 特徴

以下の理由から、非常に大規模な[情報システム](../Page/情報システム.md "wikilink")に使われる。

  - データベースが[階層型データモデル](https://ja.wikipedia.org/wiki/階層型データモデル "wikilink")であり、応答時間(レスポンスタイム)をかなり正確に見積もれる
  - 特に参照頻度の高いDB（テーブル）は[メモリ上に展開できる](../Page/主記憶装置.md "wikilink")
  - 高機能[クラスタであるXRF](../Page/コンピュータ・クラスター.md "wikilink")（専用のネットワーク機器と連携し、引継ぎ時の瞬断がほとんど無い）
  - （IMSに限らないが）修正プログラム (FIX) 等も単体で取寄せ・適用できる

ただし以下のように専用の知識（スキル）が必要である。

  - プログラム開発にはデータ照会言語[DL/I](https://ja.wikipedia.org/wiki/DL/I "wikilink")を使用する
  - 運用管理には[メインフレーム](../Page/メインフレーム.md "wikilink")の知識、費用が必要

大規模なシステムでは、IMS/ESAに金融機関向けパッケージ「SAIL/ESA」(**S**ystem Development **A**id for **I**MS/ESA On-**L**ine Applications) \[2\] を組み合わせ、SAIL/ESA の提供するAPI(マクロ)でアプリケーションを構築する場合が多い。

### 実績

日本の金融機関での実績は*→ [勘定系システム\#大手行の勘定系システム](https://ja.wikipedia.org/wiki/勘定系システム#大手行の勘定系システム "wikilink") を参照*。

## 歴史

[IBM](../Page/IBM.md "wikilink")は[1966年](../Page/1966年.md "wikilink")、[ロックウェル・インターナショナル](../Page/ロックウェル・インターナショナル.md "wikilink")、[キャタピラー社とともに](../Page/キャタピラー_\(企業\).md "wikilink")、[アポロ計画](../Page/アポロ計画.md "wikilink")のために IMS の設計を始めた。IMSは、[サターンVロケット](https://ja.wikipedia.org/wiki/サターンVロケット "wikilink")（[サターンロケット](../Page/サターンロケット.md "wikilink")）やアポロ宇宙船の膨大なパーツを整理しその目録を作るために開発された。

最初の「IMS READY」というメッセージは、[1968年](https://ja.wikipedia.org/wiki/1968年 "wikilink")[8月14日](../Page/8月14日.md "wikilink")、[カリフォルニア州](../Page/カリフォルニア州.md "wikilink") [Downey](https://ja.wikipedia.org/wiki/w:Downey,_California "wikilink") のIBM 2740端末に現れた。以来IMSは40年以上に渡って、[System/360](https://ja.wikipedia.org/wiki/System/360 "wikilink") で動く重要な[ミドルウェア](../Page/ミドルウェア.md "wikilink") の1つとして生まれてから、[2000年代](../Page/2000年代.md "wikilink")初頭の [z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink") や [System z9](../Page/System_z.md "wikilink") で動く[2005年](../Page/2005年.md "wikilink")現在に至るまで、稼動し続けている。IMS は2005年現在、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[JDBC](../Page/JDBC.md "wikilink")、[XML](../Page/Extensible_Markup_Language.md "wikilink")、[Webサービス](../Page/Webサービス.md "wikilink")をサポートする。

ヴァーン・ワッツ (Vern Watts) はIMSのチーフ・アーキテクトである。ワッツは[1950年代](../Page/1950年代.md "wikilink")後半に IBM に参加し、2005年現在も IBM の[シリコンバレー](../Page/シリコンバレー.md "wikilink")の研究所で働いている。彼は、[1960年代](../Page/1960年代.md "wikilink")からずっとIMSに関わる仕事をしている。

[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")にはIMSの[クラスタリングであるExtended](../Page/コンピュータ・クラスター.md "wikilink") Recovery Facility（XRF、拡張回復機能）が登場した\[3\]。

## IMS DB

DEDBは[VSAMの上にのみ作成することができる](https://ja.wikipedia.org/wiki/Virtual_storage_access_method "wikilink")。[DL/I](https://ja.wikipedia.org/wiki/DL/I "wikilink")[データベース](../Page/データベース.md "wikilink")はVSAM、OSAM両方の上に作成することができる。どのアクセス方式にデータベースを作成できるかは、データベースの編成によって決まる。2005年現在ではz/OSのVSAMデータセットのサイズは最大128テラバイトだが、IMSが扱えるVSAMデータセットの大きさは4ギガバイト、OSAMデータセットは8ギガバイトに制限されている。これはIMSのユーザーが、大量のデータを扱う場合はマルチ・データセットを使うことによる。「VSAM」や「OSAM」は通常、アクセス方式の例として言及される言葉である。IMSデータベースの論理的なVIEWとしては、データベースの編成として言及される（HDAM、HIDAM、HISAM、ほか）。内部のデータは、4バイトのポインターまたはアドレスによってリンクされる。データベースが作成されているデータセット上ではRBA (relative byte addresses) として言及される。

### IMSの基本的な3つの階層型データベース

#### フル・ファンクション・データベース

[DL/I](https://ja.wikipedia.org/wiki/DL/I "wikilink")データベースと同様に、アポロ計画のために開発された。フル・ファンクション・データベースは、プライマリ/セカンダリ インデックスを持つことができ、業務[アプリケーションプログラムからは](../Page/アプリケーションソフトウェア.md "wikilink") DL/Iコール でアクセスする。[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")や[Oracle Databaseのような](../Page/Oracle_Database.md "wikilink")[SQL](../Page/SQL.md "wikilink")コールとは異なっている。

フル・ファンクション・テータベースは複数のアクセス方式 (access method) を持つ。HDAM (Hierarchical Direct)、HIDAM (Hierarchical Indexed Direct) が主要なアクセス方式である。他に、SHISAM (Simple Hierarchical Indexed Sequential)、HSAM (Hierarchical Sequential)、HISAM (Hierarchical Indexed Sequential) がある。

フル・ファンクション・テータベースのデータは[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")ネイティブなアクセス方式[VSAMか](https://ja.wikipedia.org/wiki/Virtual_storage_access_method "wikilink")、OSAM (Overflow Sequential) を使ってストアされる。これらはIMSのアクセスパターン用の I/Oチャネルプログラムに最適なものである。とりわけOSAMはIMSデータベースへのシーケンシャルなアクセスにパフォーマンス上の大きな利益をもたらす (OSAM Sequential Buffering)。

#### ファスト・パス・データベース

ファスト・パス・データベースは、トランザクションを高速に処理することを目的として開発されたデータベースのタイプである。ファスト・パス・データベースとしては、DEDB (Data Entry Databases) およびMSDB (Main Storage Databases) の2つの種類の編成方式が存在する。どちらの編成もインデックスを持つことは出来ないが、DEDBはインデックスの替わりにランダマイザと呼ばれるプログラムを用いて、キーからレコードの位置を特定する。MSDBはレコードを全てメモリ上に展開するDBであり、小規模で特にアクセス頻度の高いDBに向いている。IMSの最新のバージョンでは、DEDBにおいてもVSO (Virtual Storage Option) 機能によりDBをメモリ上に展開することが可能となっている。またそれに加え、MSDBはSYSPLEX環境での共用が不可能なため、MSDBは徐々に姿を消しつつある。

#### High Availability Large Databases (HALDB)

IMS V7から実装された。フル・ファンクション・データベースの可用性を高め、巨大なデータベースを扱うことを可能にしたものである。IMS V9からオンライン再編をサポートするようになった（サードパーティによる製品ではIMS V9より前からオンライン再編を実施するツールは在った）。

## IMS TM (IMS DC)

IMSはまた、強力な[トランザクション処理ソフトウェアとして知られる](../Page/トランザクションモニター.md "wikilink")（**IMS TM**または**IMS DC**）。**[CICS](../Page/CICS.md "wikilink")** (Customer Information Control System)、**[Java EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")**（Java Platform, Enterprise Edition、特に[WebSphere Application Server上で稼動する](../Page/WebSphere_Application_Server.md "wikilink")）と並んで、3大トランザクション処理ソフトウェアの1つといわれている。トランザクションマネージャーは、[エンドユーザー](../Page/エンドユーザー.md "wikilink")と業務処理を行う業務[アプリケーション](../Page/アプリケーションソフトウェア.md "wikilink")（たとえば[銀行](../Page/銀行.md "wikilink")の[預金](../Page/預金.md "wikilink")引き出しシステム）との間に立ち（[VTAM](https://ja.wikipedia.org/wiki/VTAM "wikilink")や[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")、[3270や](../Page/IBM_3270.md "wikilink")[Web](../Page/World_Wide_Web.md "wikilink")[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")を通して）、業務アプリケーションが[レコード](../Page/レコード.md "wikilink")を処理し、正しくデータストアに格納し、[プロセス](../Page/プロセス.md "wikilink")が終了するまでその状態を維持する。IMS TM (IMS DC) は[データベース](../Page/データベース.md "wikilink")に問い合わせ、更新するインタフェースを提供するという点において、たとえば[CGIプログラムで稼動する](../Page/Common_Gateway_Interface.md "wikilink")[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")に似ている。IMS TM (IMS DC) のバックエンドデータベースとしてはIMS DBか[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")が置かれるのが典型的なパターンである。

IMS TM (IMS DC) はメッセージングとキューイングの[パラダイム](../Page/パラダイム.md "wikilink")を用いる。IMSのコントロールプログラムは[端末](../Page/端末.md "wikilink")から入力された（打鍵された）トランザクションを受け取り、[メモリまたはデータセットに用意された](../Page/主記憶装置.md "wikilink")[メッセージキュー](../Page/メッセージキュー.md "wikilink")にストアする。次にIMSはメッセージ・キューに格納されたトランザクションに対するスケジューラーを呼び出し、メッセージ・プロセッシング・リージョンに展開されている業務処理アプリケーションを起動させる。メッセージ・プロセッシング・リージョンはIMSのメッセージ・キューに格納したそのトランザクションを検索しこれを処理し、IMSまたはDB2のデータベースを読み、更新し、そのトランザクションの正しいレコーディングを保証する。そして、もし要求があれば、IMS は、応答メッセージを IMS メッセージ・キューに格納する。そのメッセージはメッセージ・キューから取り出され、IMS のコントロールプログラムはトランザクションが入力された（打鍵された）最初の端末へ、そのメッセージを送り返す。IMS TM (IMS DC) は、1秒間に何千、何万という単位で、このプロセス全体をハンドリングする。

[ビジネス](../Page/ビジネス.md "wikilink")や[行政](../Page/行政.md "wikilink")は、そのトランザクションを処理する環境を必要とした。IMS TM (IMS DC) は、簡単に、使いやすい形で、信頼性高く、効率的なトランザクション処理を行うスタンダードな環境を提供する。実際、世界中の銀行業界はこのIMSに頼っている。[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")の[連邦準備制度](../Page/連邦準備制度.md "wikilink")もそうである。[現金自動預け払い機](../Page/現金自動預け払い機.md "wikilink") (ATM) からの預金引き出し要求は、IMSトランザクションのトリガーである。最近（2005年から見て）、急速に発展する国の金融業を支えるため、[中国の数行の銀行がIMSを購入した](../Page/中華人民共和国.md "wikilink")。報道によれば、そのときのIMS単体の価格は、1年間で10億US[ドル](../Page/ドル.md "wikilink")だそうである。

## 関連項目

  - [データ管理システム](https://ja.wikipedia.org/wiki/データ管理システム "wikilink")
  - [トランザクションモニター](../Page/トランザクションモニター.md "wikilink")
  - [データベース管理システム](../Page/データベース管理システム.md "wikilink")
  - [メインフレーム](../Page/メインフレーム.md "wikilink")
  - [COBOL](../Page/COBOL.md "wikilink")
  - [PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")
  - [w:Datacom](https://ja.wikipedia.org/wiki/w:Datacom "wikilink")
  - [w:IDMS](https://ja.wikipedia.org/wiki/w:IDMS "wikilink")
  - [w:IMS/DB](https://ja.wikipedia.org/wiki/w:IMS/DB "wikilink")

## 脚注

<references />

## 外部リンク

  - [IMS - 日本IBM](http://www-01.ibm.com/software/jp/solutions/imsfamily/)
  - [IMS - IBM](http://www-01.ibm.com/software/data/ims/)
  - [IMS - IBM Knowledge Center](http://www.ibm.com/support/knowledgecenter/ja/SSEPH2)

[Category:IBMのソフトウェア](https://ja.wikipedia.org/wiki/Category:IBMのソフトウェア "wikilink") [Category:データベース管理システム](https://ja.wikipedia.org/wiki/Category:データベース管理システム "wikilink") [Category:トランザクションモニター](https://ja.wikipedia.org/wiki/Category:トランザクションモニター "wikilink") [Category:1968年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1968年のソフトウェア "wikilink")

1.  [IBM Information Management System (IMS) 13 Transaction and Database Servers は、ハイパフォーマンスと総所有コストの削減を実現します - 日本IBM](http://www-01.ibm.com/common/ssi/rep_ca/3/760/JAJPJP13-0473/index.html)
2.
3.  [IMS XRF and Parallel Sysplex: A Positioning Paper](http://www-01.ibm.com/support/docview.wss?rs=81&context=SSEPH2&q1=7011829&uid=swg27011829&loc=en_US&cs=utf-8&lang=en)