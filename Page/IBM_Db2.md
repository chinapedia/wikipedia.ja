> この記事は[IBM Db2](https://ja.wikipedia.org/wiki/IBM_Db2)から翻訳されています。


**IBM Db2** （あいびーえむ でぃーびーつー）は、1983年より[IBM](../Page/IBM.md "wikilink")が開発・販売する[データベース管理システム](../Page/データベース管理システム.md "wikilink")の1つであり、および当製品を中心としたデータ管理ソフトウェア群のブランド名。

旧称は**IBM DB2**、**IBM Database 2**など。DB2は[関係データベースだが](https://ja.wikipedia.org/wiki/関係データベース管理システム "wikilink")、2001年以降は[オブジェクトデータベース](https://ja.wikipedia.org/wiki/オブジェクトデータベース "wikilink")機能や[XMLデータベース](https://ja.wikipedia.org/wiki/XMLデータベース "wikilink")機能なども持つ。DB2ファミリーは、IBMのソフトウェアブランドの1つである[IBM Information Management Softwareを構成する](https://ja.wikipedia.org/wiki/IBM_Information_Management_Software "wikilink")。

[データベース言語](https://ja.wikipedia.org/wiki/データベース言語 "wikilink")である[SQL](../Page/SQL.md "wikilink")を初めて採用した関係データベース管理システムと言われている。

[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")及び[Windows向けの](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")**IBM DB2 for Linux, UNIX, and Windows**、[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")向けの**IBM DB2 for z/OS**、[z/VSE及び](https://ja.wikipedia.org/wiki/VSE "wikilink")[z/VM](https://ja.wikipedia.org/wiki/z/VM "wikilink")向けの**IBM DB2 Server for VSE and VM**、[IBM i向けの](https://ja.wikipedia.org/wiki/IBM_i "wikilink")**IBM DB2 Server for i**がある。

[IBM i](https://ja.wikipedia.org/wiki/IBM_i "wikilink")（かつてのOS/400、i5/OS）には標準でインストールされている。

## 概要

Db2はIBMの関係データベース用の[ミドルウェア](https://ja.wikipedia.org/wiki/ミドルウェア "wikilink")である。1981年に[メインフレーム](https://ja.wikipedia.org/wiki/メインフレーム "wikilink")の[DOS/VSE](https://ja.wikipedia.org/wiki/DOS/VSE "wikilink")および[VM/CMS用の](https://ja.wikipedia.org/wiki/z/VM "wikilink")**[SQL/DS](https://ja.wikipedia.org/wiki/SQL/DS "wikilink")**が登場し、1983年の[MVS用が](https://ja.wikipedia.org/wiki/Multiple_Virtual_Storage "wikilink")**DB2**と名付けられ、1990年代に[UNIX](../Page/UNIX.md "wikilink")版や[Windows版などが追加され](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、更にオブジェクト管理データベースを兼ねた[ORDBMSとなった](https://ja.wikipedia.org/wiki/オブジェクト関係データベース管理システム "wikilink")。IBMは関係データベースの概念を世界で初めて提唱したが、製品の出荷は[オラクルが先となった](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")。特徴としては、大規模なデータベースを支える信頼性とスケーラビリティ、コストベースの[照会最適化](https://ja.wikipedia.org/wiki/クエリ最適化 "wikilink")、メインフレーム用から[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")用までの[マルチプラットフォーム対応などが挙げられる](https://ja.wikipedia.org/wiki/クロスプラットフォーム "wikilink")。

なお、IBMのデータベース関連のソフトウェアブランド名も従来は「DB2」で、多数の製品群でDB2ファミリーを形成した。しかし[2001年](../Page/2001年.md "wikilink")のIBMによる[Informix](https://ja.wikipedia.org/wiki/Informix "wikilink")買収後は、ソフトウェアブランド名は徐々に「Information Management Software」に変更され、DB2ファミリーやInformixファミリーはその中の製品群となった。

## 名称

DB2 (Database2) との名称は、1983年にメインフレーム用のRDBMSとして発表された際に、従来の[階層型データモデル](https://ja.wikipedia.org/wiki/階層型データモデル "wikilink")の[データベース管理システム](../Page/データベース管理システム.md "wikilink")（DBMS; [IMS](https://ja.wikipedia.org/wiki/IMS "wikilink")、[DL/I](https://ja.wikipedia.org/wiki/DL/I "wikilink")など）との対比で与えられた。バージョン7、8ではDB2ユニバーサルデータベース (DB2 UDB) と称したが、バージョン9ではUDBの名称は消えた。

2017年6月、「Db2」にリブランドした\[1\]。

## 製品構成

[プラットフォームの](https://ja.wikipedia.org/wiki/プラットフォーム_\(コンピューティング\) "wikilink")[アーキテクチャに応じて](../Page/コンピュータ・アーキテクチャ.md "wikilink")、以下の製品構成に大別される（実際の製品名では、これらにバージョンやエディションを組み合わせる）。

  - DB2 for z/OS
    [z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")用。DB2ファミリーの元祖。[クラスタリング](https://ja.wikipedia.org/wiki/クラスタリング "wikilink")はDISK共有モデル。
  - DB2 Server for VSE and VM
    [VSE](https://ja.wikipedia.org/wiki/z/VSE "wikilink"), [VM用](https://ja.wikipedia.org/wiki/z/VM "wikilink")。従来の「[SQL/DS](https://ja.wikipedia.org/wiki/SQL/DS "wikilink") for VSE and VM」を改名したもの。
  - DB2 for i
    [IBM i用](https://ja.wikipedia.org/wiki/OS/400 "wikilink")。内部的にはH/W（[AS/400](https://ja.wikipedia.org/wiki/AS/400 "wikilink")、iSeries、[System i](https://ja.wikipedia.org/wiki/System_i "wikilink")、[Power Systems](https://ja.wikipedia.org/wiki/Power_Systems "wikilink") i Edition）標準の、H/WのRDBMS機能を使用している。単独製品ではなく、IBM i の標準機能として提供されている。
  - DB2 for Linux, UNIX and Windows (DB2 for LUW)
    [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink"), [AIX](https://ja.wikipedia.org/wiki/AIX "wikilink"), [HP-UX](../Page/HP-UX.md "wikilink"), [Solaris](../Page/Solaris.md "wikilink"), [Windows用](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。従来の「DB2 for [Multiplatform](https://ja.wikipedia.org/wiki/マルチプラットフォーム "wikilink")」。ソフトウェアでRDBMS機能を実現している。オプションの[クラスタリング](https://ja.wikipedia.org/wiki/クラスタリング "wikilink")はシェアードナッシングモデルだった。ただし2009年10月にAIXの特定のモデルのみDB2 pureScaleを用意しておりこちらはメインフレーム版のDB2およびOracleRACと同じDISK共有モデルを採用している。

## 歴史

Db2は長い歴史をもつソフトウェアである。一部の人々は、Db2が[データベース言語](https://ja.wikipedia.org/wiki/データベース言語 "wikilink")[SQL](../Page/SQL.md "wikilink")を初めて採用した関係データベース管理システム (RDBMS) の製品だと考えている。

[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")にIBMは[System/38](https://ja.wikipedia.org/wiki/System/38 "wikilink")（現在の [System i](https://ja.wikipedia.org/wiki/System_i "wikilink")）というコンピュータシステムをリリースした。 System/38 では、そのシステムの中核部分に、RDBMSの機能を統合していた。[1981年](https://ja.wikipedia.org/wiki/1981年 "wikilink")にIBM は[SQL/DS](https://ja.wikipedia.org/wiki/SQL/DS "wikilink")というRDBMS製品をリリースし、[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")にはDB2 (Database2) をリリースした。SQL/DSとDB2は、IBMの[メインフレーム](https://ja.wikipedia.org/wiki/メインフレーム "wikilink")で動くRDBMSであった。IBMがRDBMを製品化する以前には、IBMで [1970年代](../Page/1970年代.md "wikilink")に研究目的で開発されたRDBMSである[System Rがあった](https://ja.wikipedia.org/wiki/System_R "wikilink")。SQL/DSとDB2は、IBMに勤めていた[エドガー・F・コッド](../Page/エドガー・F・コッド.md "wikilink")博士が [1969年](https://ja.wikipedia.org/wiki/1969年 "wikilink")に論文で発表した[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")の理論 ([関係モデル](https://ja.wikipedia.org/wiki/関係モデル "wikilink")) と、System Rが基礎となっている。

System Rは、IBMのサンノゼ研究所で 1970年代に行われた、[関係モデル](https://ja.wikipedia.org/wiki/関係モデル "wikilink")をソフトウェアとして[実装](https://ja.wikipedia.org/wiki/実装 "wikilink")するプロジェクトであった。System R で、コッドは関係データベースを扱う言語を必要とした。コッドはこのために[データベース言語](https://ja.wikipedia.org/wiki/データベース言語 "wikilink")を設計し、Alphaという名前をつけた。IBMはこのとき、コッドが考案した関係データベースの理論に秘められた可能性を、軽視していた。そのためIBMは、関係データベースを実装するための[プログラマ](../Page/プログラマ.md "wikilink")のチームをコッドに預けたが、このプログラマたちはもともとコッドの管理下にいた人々ではなかった。このプログラマたちは、関係モデルのいくつかの重要な構成要素を曲解してしまった。こうした混乱はあったものの、System Rプロジェクトは成功し、RDBMSが実用化できることが示された。

System Rの成果の一つが、[データベース言語](https://ja.wikipedia.org/wiki/データベース言語 "wikilink")SEQUELである（コッドのAlphaとは別の言語）。SEQUELは、"Structured English QUEry Language" を略した呼称である。しかしSEQUELという名称は、当時すでに別の会社が[登録商標としていた](../Page/商標.md "wikilink")。そのためIBMは、"Structured Query Language" の短い呼称として、頭文字をとって[SQL](../Page/SQL.md "wikilink")という名称に変え、現在に至っている。

[データベース](../Page/データベース.md "wikilink")の歴史においては、[Informix](https://ja.wikipedia.org/wiki/Informix "wikilink")が自社の関係データベース管理システム[Informixのエンジンを](https://ja.wikipedia.org/wiki/Informix_Dynamic_Server "wikilink")[オブジェクト関係データベース管理システム](https://ja.wikipedia.org/wiki/オブジェクト関係データベース管理システム "wikilink")の[エンジン](https://ja.wikipedia.org/wiki/エンジン "wikilink")に改良したときのことが特筆される ([Informix Universal Server](https://ja.wikipedia.org/wiki/Informix_Dynamic_Server "wikilink")) 。Informixは、Informixのデータベースエンジンの改良を、[Illustra](https://ja.wikipedia.org/wiki/Illustra "wikilink")を買収して Illustraのユニバーサルサーバの技術を導入することによって、行った。Informixの動きをみて、[オラクルとIBMも追随した](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")。両社は、それぞれのデータベースエンジンを改良し、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")関係データベース管理システムの機能を、拡張機能として実装した。このとき、IBMはDB2を「DB2ユニバーサルデータベース」(DB2 UDB) という名称にしている。2001年に、IBMはInformixを買収した。その後、IBMはInformixの技術をDB2の製品群に導入している。現在 DB2 は、技術的には[オブジェクト関係データベース管理システム](https://ja.wikipedia.org/wiki/オブジェクト関係データベース管理システム "wikilink") (ORDBMS) として位置づけられる。

長い間、DB2はIBMの[汎用コンピュータ](https://ja.wikipedia.org/wiki/汎用コンピュータ "wikilink")（[System/370](https://ja.wikipedia.org/wiki/System/370 "wikilink")や[System/390](https://ja.wikipedia.org/wiki/System/390 "wikilink")、[AS/400](https://ja.wikipedia.org/wiki/AS/400 "wikilink")など）のプラットフォームの上でしか動かなかった。先述したように、IBMのコンピュータ[System/38](https://ja.wikipedia.org/wiki/System/38 "wikilink")（後の[AS/400](https://ja.wikipedia.org/wiki/System_i "wikilink")、現在の[System i](https://ja.wikipedia.org/wiki/System_i "wikilink")）では、そのシステムの中核部分に、RDBMSの機能を統合していた 。このRDBMSの機能には当初は名前がつけられていなかったが、[1994年](../Page/1994年.md "wikilink")にDB2/400と名付けられた。DB2/400はDB2ソフトウェア群の一つと位置づけられている。DB2/400は、現在ではDB2 for [IBM iという名称で呼ばれることが多い](https://ja.wikipedia.org/wiki/IBM_i "wikilink")。

1990年代にIBMはDB2を他のプラットフォームに移植し、DB2は[UNIX](../Page/UNIX.md "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[サーバ](../Page/サーバ.md "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")（Linux on IBM [System zも含む](https://ja.wikipedia.org/wiki/System_z "wikilink")）、各社の[携帯情報端末](https://ja.wikipedia.org/wiki/携帯情報端末 "wikilink") (PDA) でも動くようになった。DB2の実装の細部は、一部、IBM [DL/I](https://ja.wikipedia.org/wiki/DL/I "wikilink")と[IBM IMSという](https://ja.wikipedia.org/wiki/IMS "wikilink")[階層型データベース](https://ja.wikipedia.org/wiki/階層型データベース "wikilink")が基になっている。 IBMが近年開発した汎用コンピュータ[System zのOSである](https://ja.wikipedia.org/wiki/System_z "wikilink")、z/VSEやz/VMで動作するDB2のバージョンも、利用することができるようになっている。少し前のDB2のバージョンは、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")向けにも提供されていた。

### 年表

主なバージョンのリリース年月 (GA, General Available) は以下である \[2\] \[3\]。以下の他に、DB2 Server for VSE and VMと、DB2 for i（IBM iの機能として提供）が存在する。

  - メインフレーム版
      - 1983年 DB2 （MVS版）リリース
      - 1986年 DB2 R2 （MVS版）リリース
      - 1997年6月 DB2 for OS/390 V5.1 リリース
      - 1998年6月 DB2 for OS/390 V6.1 リリース
      - 2001年3月 DB2 for OS/390 and z/OS V7.1 リリース
      - 2004年3月 DB2 for z/OS V8.1 リリース
      - 2008年2月 DB2 for z/OS V9.1 リリース
      - 2010年10月 DB2 for z/OS V10 リリース
  - マルチプラットフォーム版
      - 1993年 DB2 （AIX版） リリース
      - 1994年 DB2 （Solaris、HP-UX版） リリース
      - 1995年 DB2 （Windows版） リリース
      - 1999年 DB2 （Linux版） リリース
      - 2001年6月 DB2 Universal Database V7.2 リリース
      - 2002年12月 DB2 Universal Database V8.1 リリース
      - 2004年10月 DB2 Universal Database V8.2 リリース
      - 2006年9月 DB2 V9.1（開発コード名：Viper）リリース
      - 2007年12月 DB2 V9.5（開発コード名：Viper2）リリース
      - 2009年6月 DB2 V9.7（開発コード名：Cobra）リリース
      - 2012年4月 DB2 V10.1 リリース
      - 2013年4月 DB2 V10.5 リリース\[4\]
      - 2016年6月 DB2 V11.1 リリース

## エディション

DB2ユニバーサルデータベース (Db2 UDB) は、いくつかの[ライセンス](https://ja.wikipedia.org/wiki/ライセンス "wikilink")形態（エディション）で提供されている。[汎用コンピュータ](https://ja.wikipedia.org/wiki/汎用コンピュータ "wikilink")における、[データベース](../Page/データベース.md "wikilink")機能のない「エディション」では、ユーザは、自分たちが必要としないデータベース機能のために、金銭を支払う必要がない。他のエディションとして、ワークグループ、ワークグループアンリミテッド、エンタープライズサーバの、各エディションが提供されている。[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")のエディションは、「DB2 UDB データウェアハウスエンタープライズエディション」(DWE) である。このエディション (DWE) は、[オンライントランザクション処理](https://ja.wikipedia.org/wiki/オンライントランザクション処理 "wikilink") (OLTP) と[ビジネスインテリジェンス](https://ja.wikipedia.org/wiki/ビジネスインテリジェンス "wikilink") (BI) の複合したワークロードを、対象としたものであり、ビジネスインテリジェンスの機能を実装している。 DWEでは、いくつかのビジネスインテリジェンスの機能（[データウェアハウス](https://ja.wikipedia.org/wiki/データウェアハウス "wikilink")、[ETL](https://ja.wikipedia.org/wiki/Extract/Transform/Load "wikilink")、[データマイニング](https://ja.wikipedia.org/wiki/データマイニング "wikilink")、[OLAP](https://ja.wikipedia.org/wiki/OLAP "wikilink")拡張、インライン分析）が提供される。

[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")向けのDB2 (DB2 for System z) は、z/OSプラットフォームに固有のライセンス形態で、利用することができる。z/OSは、[IBM](../Page/IBM.md "wikilink")の[メインフレーム](https://ja.wikipedia.org/wiki/メインフレーム "wikilink")[System/390](https://ja.wikipedia.org/wiki/System/390 "wikilink")の後継機種である[System zのOSである](https://ja.wikipedia.org/wiki/System_z "wikilink")。DB2 UDBのバージョン8 以降、IBMはz/OS上でDB2を利用できるようにしている。DB2 for System zは、z/OS以外のプラットフォームのDB2との関係が、より密接になっている（それまでは、例えばデータベース言語[SQL](../Page/SQL.md "wikilink")の文法が異なるなど、大きな違いがいくつかあった）。DB2 for System zは、いくつかの高度な機能を備えている。その中でも特筆すべき機能は、マルチレベルセキュリティ (MLS)、非常に大きな容量のテーブル、[ハードウェア](../Page/ハードウェア.md "wikilink")の機能を利用した[データ圧縮](../Page/データ圧縮.md "wikilink")である。このような高度な機能は、z/OSが提供する優れた環境と、ユーザからの要望によって、実現された。DB2 for System z は、その第一級の[オンライントランザクション処理](https://ja.wikipedia.org/wiki/オンライントランザクション処理 "wikilink") (OLTP) 性能と処理能力によって、人々に認知されていた。しかし現在DB2 for System zは、マテリアライズ照会表 (MQT) の導入など、[ビジネスインテリジェンス](https://ja.wikipedia.org/wiki/ビジネスインテリジェンス "wikilink")の機能も備えつつある。[オラクルのCEOの](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")[ラリー・エリソン](https://ja.wikipedia.org/wiki/ラリー・エリソン "wikilink")は、2003年10月に、[並列シスプレックス](https://ja.wikipedia.org/wiki/並列シスプレックス "wikilink")を用いたDB2 UDB for z/OS（現在の DB2 for System z）に言及して、[Oracle Databaseと競い合う唯一のデータベースであり尊敬と称賛に値する](https://ja.wikipedia.org/wiki/Oracle_Database "wikilink")、と論評したことが、広く報道された。

## 競争相手

DB2はオラクルの[Oracle Database](https://ja.wikipedia.org/wiki/Oracle_Database "wikilink")、[SAPの](https://ja.wikipedia.org/wiki/SAP_\(企業\) "wikilink")[SAP HANAと激しいトップシェア争いをしている](https://ja.wikipedia.org/wiki/SAP_HANA "wikilink")。DB2の主要な市場は[メインフレーム](https://ja.wikipedia.org/wiki/メインフレーム "wikilink")、[オフィスコンピュータ](../Page/オフィスコンピュータ.md "wikilink")の領域であったが、1990年代以降は、[UNIX](../Page/UNIX.md "wikilink")、[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink") (PC) 向けのDB2もシェアを伸ばしている。2004年5月3日、[IBM](../Page/IBM.md "wikilink")のデータベース開発と販売を統括するジャネット・パーナ (Janet Perna) は、IBMの主要な競争相手は、高度な[トランザクション](https://ja.wikipedia.org/wiki/トランザクション "wikilink")処理においてはOracle Databaseであり、意思決定支援システム ([データウェアハウス](https://ja.wikipedia.org/wiki/データウェアハウス "wikilink")など) においては[NCRの](https://ja.wikipedia.org/wiki/NCR_\(企業\) "wikilink")[Teradata](https://ja.wikipedia.org/wiki/Teradata "wikilink")であると、見解を述べている。また、2010年にSAPより[インメモリーデータベース](https://ja.wikipedia.org/wiki/インメモリデータベース "wikilink")[SAP HANAがリリースされてからは従来基幹系システムや情報系システムにDB](https://ja.wikipedia.org/wiki/SAP_HANA "wikilink")2やOracle Databaseを採用していた企業がSAP HANAに移行する事例も相次いで出てきており、2016年現在、大企業向けのデータベース管理システム市場はDB2、Oracle Database、SAP HANAの3大製品が占める構図になっている。

中小規模のデータベースにおいても、DB2は有力な存在であるが、多くの競争相手が存在している。Oracleは大規模データベースと同様に、中小規模のデータベースにおいても、DB2と激しく争っている。Oracle Databaseの他、商用では[マイクロソフト](../Page/マイクロソフト.md "wikilink")の [Microsoft SQL Serverや](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")[SAP Sybase Adaptive Server Enterprise](https://ja.wikipedia.org/wiki/Adaptive_Server_Enterprise "wikilink") 、[オープンソース](../Page/オープンソース.md "wikilink")では[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")や[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")などが有力な存在である。

[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")向けのDB2 (DB2 for System z) は、z/OS[プラットフォームにおいて非常に強く](https://ja.wikipedia.org/wiki/プラットフォーム_\(コンピューティング\) "wikilink")、正面から競合する相手はほとんど存在しないといってよいであろう。z/OSプラットフォームにおいては、Oracleがz/OSの顧客に[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") on IBM [System z向けのOracleを採用するようはたらきかけている](https://ja.wikipedia.org/wiki/System_z "wikilink")。ただしOracleを採用するケースでも顧客がDB2を捨てるわけではないようである。また[CAが](https://ja.wikipedia.org/wiki/CA_\(企業\) "wikilink")、同社のDatacomという関係データベースのz/OS向けのバージョンで、DB2に挑戦している。Datacomを採用するケースでもDatacomの顧客は多くの場合DB2を手放すわけではない。

メインフレームでは、DB2 for System z以外には、日本のメインフレーマー各社が自社開発したRDBMSが提供されている。

IBMおよびDB2は、[トランザクション処理性能評議会](https://ja.wikipedia.org/wiki/トランザクション処理性能評議会 "wikilink") (TPC) のウェブサイトで公表されているTPC-C ([OLTP](https://ja.wikipedia.org/wiki/オンライントランザクション処理 "wikilink")) とTPC-H ([データウェアハウス](https://ja.wikipedia.org/wiki/データウェアハウス "wikilink")) の[ベンチマーク](https://ja.wikipedia.org/wiki/ベンチマーク "wikilink")において、業界の首位もしくは首位に近い性能を示す常連である。

## RDBMSとしての特徴

  - コストベースオプティマイザー
    クエリー最適化については、当初よりコストベースのオプティマイザーが実装されており、様々な実行計画から最適なプランをDB2が自動的に選択する。
  - 読み取り一貫性
    読み取り一貫性はロックにより実現される。ロックは必要に応じて自動的に行われるが、アプリケーションやデータベース構成パラメーターの設計が不適切な場合には、ロック・エスカレーションにより想定以上のロックが取得されたり、場合によってはデッドロックが発生するケースもある。ただし、その他の方式としてよくみられるMVCCに比較すると、更新前のデータを退避する必要が無いため、ストレージコストが少ないというメリットも存在する。
  - 移植性
    元々SQLがIBMから始まっているということもあって、SQL-92といった国際標準へ準拠度は高めである。また、v9.7よりOracle Databaseとの互換性強化のため、PL/SQLがサポートされた。

## その他

DB2は、[Oracle Databaseと同じく](https://ja.wikipedia.org/wiki/Oracle_Database "wikilink")、[データベース](../Page/データベース.md "wikilink")を管理するための[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink") (UI) として、[コマンドラインユーザインタフェース](../Page/キャラクタユーザインタフェース.md "wikilink") (CUI) と[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") (GUI) の両方を提供している。DB2のコマンドラインインタフェースを使う場合は、DB2に関してのある程度の知識が必要であるが、管理作業の[スクリプト化や自動化が簡単にできる](../Page/スクリプト言語.md "wikilink")。DB2のGUIは、豊富な[ウィザードを使うことができ](https://ja.wikipedia.org/wiki/ウィザード_\(ソフトウェア\) "wikilink")、まだDB2に習熟していない人にとって使いやすい。DB2のGUIは、マルチ[プラットフォームの](https://ja.wikipedia.org/wiki/プラットフォーム_\(コンピューティング\) "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")である。

DB2では、非常に多くの[プログラミング言語](../Page/プログラミング言語.md "wikilink")やプラットフォームに対応した[アプリケーションプログラミングインタフェース](../Page/アプリケーションプログラミングインタフェース.md "wikilink") (API) を、利用することができる。主要なものでは、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[.NET Frameworkの](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[CLI](https://ja.wikipedia.org/wiki/共通言語基盤 "wikilink") ([CLR](https://ja.wikipedia.org/wiki/Common_Language_Runtime "wikilink"))、[Ruby](https://ja.wikipedia.org/wiki/Ruby_\(代表的なトピック\) "wikilink")、[Python](../Page/Python.md "wikilink")、[Perl](../Page/Perl.md "wikilink")、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[C++](../Page/C++.md "wikilink")、[C](../Page/C言語.md "wikilink")、[REXX](https://ja.wikipedia.org/wiki/REXX "wikilink")、[PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")、[RPG](https://ja.wikipedia.org/wiki/RPG_\(プログラム言語\) "wikilink")、[COBOL](https://ja.wikipedia.org/wiki/COBOL "wikilink")、[FORTRAN](../Page/FORTRAN.md "wikilink") などがある。DB2ではまた、[Eclipseと](../Page/Eclipse_\(統合開発環境\).md "wikilink")[Visual Studioの](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) に対しても、DB2を利用した[ソフトウェア開発](https://ja.wikipedia.org/wiki/ソフトウェア開発 "wikilink")を支援する機能を、統合的に使えるようにしている。

ジャネット・パーナ (Janet Perna) は、[IBM](../Page/IBM.md "wikilink")ソフトウェアグループのインフォメーション・マネジメント事業部で、部長 (General Manager) を務めていた。パーナは2005年7月にIBMを退職した。パーナの後は、アンブシュ・ゴヤール (Ambuj Goyal) がその地位を引き継いだ。

## 参照

<references />

## 関連項目

  - [関係データベース管理システム](https://ja.wikipedia.org/wiki/関係データベース管理システム "wikilink")
  - [IBM](../Page/IBM.md "wikilink")
  - [System R](https://ja.wikipedia.org/wiki/System_R "wikilink") - DB2の元ともなったRDBMS
  - [SQL/DS](https://ja.wikipedia.org/wiki/SQL/DS "wikilink") - [VSEや](https://ja.wikipedia.org/wiki/z/VSE "wikilink")[VMで稼働するDB](https://ja.wikipedia.org/wiki/z/VM "wikilink")2の兄弟分
  - [IMS](https://ja.wikipedia.org/wiki/IMS "wikilink") - IMS/TM(IMS/DC)とDB2の組み合わせが可能
  - [Informix](https://ja.wikipedia.org/wiki/Informix "wikilink") - IBMによる買収後はDB2との技術共有が進められている

## 外部リンク

  - [IBM DB2- 日本IBM](https://www.ibm.com/jp-ja/analytics/database-management)
  - [IBM マーケットプレイス](https://www.ibm.com/jp-ja/products)
  - [IBM ソフトウェア](https://www.ibm.com/software/jp/)
  - [IBM 無料評価版](https://www.ibm.com/software/jp/info/trials/)
  - [IBM DB2 product family web page](http://www.ibm.com/software/data/)
      - [DB2 Express-C](https://www.ibm.com/jp-ja/products/db2-database/) - DB2の無料版
  - [IBM DB2 Developer Domain - Japan](http://www.ibm.com/jp/software/data/developer/)
  - [IBM DB2 resources for developers](http://www.ibm.com/developerworks/db2)
  - [An Expert's Guide to DB2](http://blogs.ittoolbox.com/database/technology)
  - [Ambuj Goyal's IBM Research home page](http://www.research.ibm.com/people/a/ambuj/)
  - [Blog about DB2 for z/OS](http://db2usa.blogspot.com/)
  - [DB2usa - Links to DB2 for z/OS documents available on the web](http://db2usa2.free.fr/eliendb2.htm/)

[Category:データベース管理システム](https://ja.wikipedia.org/wiki/Category:データベース管理システム "wikilink") [Category:IBMのソフトウェア](https://ja.wikipedia.org/wiki/Category:IBMのソフトウェア "wikilink") [Category:1983年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1983年のソフトウェア "wikilink")

1.
2.  [コンピュータの歴史 - 日本IBM](http://www-06.ibm.com/jp/ibm/mugendai/no116/pdf/116m.pdf)
3.  [IBM Software Support Lifecycle](http://www-01.ibm.com/software/support/lifecycle/)
4.  [IBM DB2 10.5 for Linux, UNIX and Windows、IBM InfoSphere BigInsights V2.1、および IBM InfoSphere Streams V3.1](http://www-01.ibm.com/common/ssi/ShowDoc.wss?docURL=/common/ssi/rep_ca/5/760/JAJPJP13-0245/index.html&lang=ja&request_locale=ja)