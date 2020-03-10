> この記事は[Informix](https://ja.wikipedia.org/wiki/Informix)から翻訳されています。


**Informix**（いんふぉみっくす）は、[IBM](../Page/IBM.md "wikilink")の[関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink") (RDBMS) 製品群の名称。[2001年](../Page/2001年.md "wikilink")に買収した企業（InformixまたはInformix Software）が[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")に開発したものが起源である。

## 概要

Informix[データベース管理システム](../Page/データベース管理システム.md "wikilink") (DBMS) は1970年代末にRoger Sipplが考案・設計した。1980年にInformix社が設立され、1986年に株式公開され、[1990年代](../Page/1990年代.md "wikilink")には[Oracleに次ぐデータベースシステムの地位を得るに至った](../Page/Oracle_Database.md "wikilink")。しかし成功は長くは続かず、経営上の失敗が度重なって 2000年までに財政的に極めて困難な状態となった。

[2001年](../Page/2001年.md "wikilink")、Informix最大の顧客であった[ウォルマート](../Page/ウォルマート.md "wikilink")の示唆を受けて、[IBM](../Page/IBM.md "wikilink")がInformixを買収した\[1\]。IBMは[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")とInformixの技術共通化に関する長期計画を持っている。[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")初め、IBMは[Informix Dynamic Server](https://ja.wikipedia.org/wiki/Informix_Dynamic_Server "wikilink") (IDS) バージョン10 をリリースした。

[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")、[IBM](../Page/IBM.md "wikilink")内でデータサーバ技術をIDS (Informix Dynamic Server) に集約する動きがあった。DB2部門を統括していたJanet Pernaは30年以上勤務した同社を退職し、同部門は**DB2** Information Management部門から**Information Management**部門へと改称された。

IDSはIBM 内では戦略データサーバ (strategic data server) という位置づけになっている。[2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink")、IBMは Informix (IDS) バージョン11をリリースした。[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")5月、IBMはInformix (IDS) バージョン11.5を発表した。

## 歴史

### 1980年: 草創期

Roger SipplとLaura Kingは、[S-100バスや](https://ja.wikipedia.org/wiki/Altair_8800#S-100バス "wikilink")[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")関係の企業[クロメムコ](https://ja.wikipedia.org/wiki/クロメムコ "wikilink")に勤務していた。そこで報告書作成ソフトウェアのための [ISAM技術に基づいた小型の](https://ja.wikipedia.org/wiki/Indexed_Sequential_Access_Method "wikilink")[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")の開発に従事した。

Sipplと Kingは1980年に同社を辞め、**Relational Database Systems** (RDS）を設立。最初の製品*Marathon*は彼らがクロメムコで開発したシステムの16ビット版であり、[ザイログ](../Page/ザイログ.md "wikilink")の初期の[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")向けの[UNIX](../Page/UNIX.md "wikilink") (Onyx) 上で動作した。

彼らは成長しつつある[関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink") (RDBMS) 市場に注目し、1981年に**Informix** (INFORMation on unIX）をリリースした。これには独自の言語 **Informer** が含まれていた。また、データを抽出して読みやすい報告書を作成するサブシステム**ACE**も付属していた。画面入力フォーム作成ツール**PERFORM**もあり、ユーザーが対話的にデータベースとやりとりすることができた。この製品の最終バージョンは3.30で、1986年にリリースされた。

[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")、新たな[SQL](../Page/SQL.md "wikilink")ベースのクエリエンジンが**INFORMIX-SQL** (ISQL) バージョン1.10の一部としてリリースされた。もちろんACEとPERFORMのSQL対応版も含まれている。ISQLと以前のInformixの最大の違いは、データベースアクセスコードをクライアントコードと完全に分離した点である。これがクライアント・サーバ型のデータベースシステムへの布石となった。

1980年代前半を通してInformixは市場で優位に立つことはなかったが、1980年代中ごろにはUNIXとSQLの組合せが人気となり、情勢が変わってきた。[1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")には[株式公開](../Page/株式公開.md "wikilink")にこぎつけ、社名を**Informix Software**に変更した。当時の製品はINFORMIX-SQLバージョン2.00と INFORMIX-4GL 1.00であり、どちらもデータベースエンジンと開発ツールを含んでいる（I4GLはプログラマ向け、ISQLは非プログラマ向け）。

その後も新製品のリリースが続き、新たなクエリエンジンを使ったINFORMIX-Turboがリリースされた。TurboはISAMよりマルチユーザー性能が優れたRSAM技術を使っている。1989年、バージョン4.00製品がリリースされ、TurboはINFORMIX-OnLineと改称（オンライン状態でユーザーが使用中にデータベースバックアップが可能）、従来のC-ISAMベースのサーバ機能（ISQLとI4GL）はツール群と分離され、INFORMIX-SE (Standard Engine) と改称された。Informix OnLineのバージョン5.00は1990年末にリリースされた。これには[2相コミット](../Page/2相コミット.md "wikilink")と[ストアドプロシージャ](https://ja.wikipedia.org/wiki/ストアドプロシージャ "wikilink")による[分散トランザクション](https://ja.wikipedia.org/wiki/分散トランザクション "wikilink")機能が含まれている。

### 1988年: Innovative Software 買収

[1988年](../Page/1988年.md "wikilink")、InformixはDOSおよびUNIX向けのオフィスソフトのメーカー**Innovative Software**を買収した。特に[WingZ](https://ja.wikipedia.org/wiki/WingZ "wikilink")という[Macintosh](../Page/Macintosh.md "wikilink")用[表計算ソフト](../Page/表計算ソフト.md "wikilink")が有名であった。

[WingZ](https://ja.wikipedia.org/wiki/WingZ "wikilink")は高度なGUIで巨大な表が使え、HyperScript と呼ばれる[HyperCard](../Page/HyperCard.md "wikilink")風の言語でプログラミング可能であった。最初のリリースは好評で、[Microsoft Excelに次ぐ](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")2位のシェアを獲得した。[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")、WingZは主に[UNIX](../Page/UNIX.md "wikilink")系OS向けにいくつかのプラットフォームに移植され始めた。このころ、多くの金融機関は大型の金融モデルを計算するためにパーソナルコンピュータよりも強力なシステムを必要としており、UNIXワークステーションがその目的で使われ始めたのであった。そのため、ある期間WingZはこのニッチ市場で成功を収めた。

しかし、サーバ向けでないソフトウェア市場に対する全体的な理解不足から、開発やマーケティングのリソースが不足するようになった。1990年代初めWingZは競争力を失い、Informixはこれを[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")に売却した。また、ライセンスは[クラリス](https://ja.wikipedia.org/wiki/クラリス "wikilink")に売却され、そこからGUIを改良してClaris Resolveが生まれた。

### 1994年: 動的スケーラブルアーキテクチャ

オフィスソフトで失敗し、Informixは再度データベースサーバ市場に注力するようになった。1994年、[シークエント・コンピュータ](https://ja.wikipedia.org/wiki/シークエント・コンピュータ "wikilink")との協業でInformixはバージョン6.00データベースサーバをリリースした。その目玉となった機能が動的スケーラブルアーキテクチャ (DSA) である。

DSAは製品のエンジン中核部を大幅に刷新し、垂直および水平の並行性をサポートするもので、シークエントが得意とした[対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink")向きのマルチスレッド型コアを採用していた。この動きに[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")や[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")も追随した。これにより業界でもトップレベルの[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")を備え、[OLTPにも](https://ja.wikipedia.org/wiki/オンライントランザクション処理 "wikilink")[データウェアハウス](../Page/データウェアハウス.md "wikilink")にも対応可能となった。

現在は**[Informix Dynamic Server](https://ja.wikipedia.org/wiki/Informix_Dynamic_Server "wikilink")** (**IDS**) として知られるこの製品は 1994年にバージョン7がリリースされた。当時、ちょうどUNIXでは対称型マルチプロセッシングが一般化しつつあった。バージョン7は当時の競合他社製品より進んでおり、性能[ベンチマーク](https://ja.wikipedia.org/wiki/ベンチマーク "wikilink")でも常に勝っていた。その結果、Informixは1997年までに[サイベース](https://ja.wikipedia.org/wiki/サイベース "wikilink")を押しのけ、業界2位となったのである。

バージョン7の成功により、Informixは中核部分の設計を2段階とし、従来からの延長を*XMP* (eXtended Multi Processing)、より大型のシステム向けを*XPS* (eXtended Parallel Server) として、バージョン8をリリースした。XPSは[データウェアハウス](../Page/データウェアハウス.md "wikilink")やクラスター上のデータベースを指向している。

### 1995年: Illustra 買収

[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")、Informixは[オブジェクト関係データベース](https://ja.wikipedia.org/wiki/オブジェクト関係データベース "wikilink") (ORD) に着目し、[Illustra](https://ja.wikipedia.org/wiki/Illustra "wikilink")を買収した。Illustraは[マイケル・ストーンブレーカー](../Page/マイケル・ストーンブレーカー.md "wikilink")の[Postgres開発チームが作ったもので](../Page/Ingres.md "wikilink")、データベースと[オブジェクトを関連付ける各種機能を備え](../Page/オブジェクト指向.md "wikilink")、多くのプロジェクトでプログラミングにかかる時間を劇的に改善できる機能が備わっていた。Illustraには**DataBlades**と呼ばれる新たなデータ型をサーバに導入できる機能があった。これらの機能がSQLが[時系列](https://ja.wikipedia.org/wiki/時系列 "wikilink")データやマルチメディアデータを扱う際の問題への解決策を与えた。Informixはこれらの機能を7.x OnLine製品に取り入れ、**[Informix Universal Server](https://ja.wikipedia.org/wiki/Informix_Universal_Server "wikilink")** (IUS) と名づけた（また、通常バージョン9と呼ばれている）。

V8 (XPS) と V9 (IUS) は[1996年](../Page/1996年.md "wikilink")にリリースされ、Informixは3大データベース企業（他は[オラクルと](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")[サイベース](https://ja.wikipedia.org/wiki/サイベース "wikilink")）の中でいち早くオブジェクト関係データベースをサポートすることとなった。特にDataBladesは注目され、人気となり、即座に各プラットフォームに移植されていった。他社はこの動きにあわてた。オラクルは追加パッケージとして時系列サポートを1997年に行い、サイベースは[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")に解決策を求めた。

### 1997年: 経営問題

技術的には成功したものの、マーケティングと企業運営での失敗が影を落とした。1997年4月1日、Informixは収益が予測より1億ドル少ないことを公表した。この時点がInformixの成長の最高点だった。技術的には進化を続けたものの、1997年の[CEO解任に端を発した経営陣のごたごたにより](https://ja.wikipedia.org/wiki/最高経営責任者 "wikilink")、会社は勢いを失っていった。

### 2001年: その他の買収

[2000年](../Page/2000年.md "wikilink")、Informixに起きた出来事はもはや技術革新の話ではなかった。3月、Informixは、それまでも何度も合併を繰り返してきたArdent Softwareを買収した。これにより、多次元型エンジンUniVerseとUniDataが製品系列に加わった。他にもInformix以外のエンジンとしてデータウェアハウス向けのRed Brick、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で書かれたCloudscapeなどもあった。

6月、Ardentの前CEO James D. FoyがInformixのCEOに就任し、彼はInformixを買収の対象として魅力的になるよう改編していった。大きな変更として、全てのデータベースエンジン技術とアプリケーションおよびツールを分離した。

[2001年](../Page/2001年.md "wikilink")、IBMはInformixを買収し、そのデータベース技術とブランドと将来の開発計画と10万を超える顧客ベースを入手した。アプリケーションおよびツールは買収には含まれず、Ascential Softwareという会社になった。

2005年5月、IBMはAscential Softwareの買収も完了した。

### 2002年: 経営問題の余波

[2002年](../Page/2002年.md "wikilink")11月、1997年に解任された元CEOフィリップ・ホワイトは連邦大陪審に起訴され、セキュリティ、メール詐欺など8つの訴因で告発された。13ヵ月後、司法取引により米国証券取引委員会への偽の報告書提出の罪を認めた。

[2004年](https://ja.wikipedia.org/wiki/2004年 "wikilink")5月、司法省はホワイトが2ヶ月間連邦刑務所に収監されたことを発表した。また、罰金は1万ドルで、2年間保護観察下におかれ、300時間の公共サービス従事が義務付けられた。この発表では、これらが株主が被った損害を考慮した罰ではないことを強調した。

Informixでヨーロッパを任されていたWalter Königsederも同様に起訴されたが、ドイツ在住であったため、引渡しが行われなかった。

2005年11月、Informixと フィル・ホワイトの事の顛末を記した本が出版された。

## 主な製品

  - Informix C-ISAM - 最初のMarathonに基づいた製品
  - Informix SE - アプリケーションへの組み込み向けの[ローエンド](https://ja.wikipedia.org/wiki/ローエンド "wikilink")製品
  - Informix OnLine - 中規模データベース製品
  - Informix Extended Parallel Server (XPS, V8) - 大規模分散システム向け
  - [Informix Universal Server](https://ja.wikipedia.org/wiki/Informix_Universal_Server "wikilink") (V9) - [Illustra](https://ja.wikipedia.org/wiki/Illustra "wikilink")の技術を導入した製品
  - Informix 4GL - 第4世代言語
  - Red Brick Warehouse - [データウェアハウス](../Page/データウェアハウス.md "wikilink")製品
  - Cloudscape - モバイル機器からJ2EEの[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")までをカバーするJavaで書かれたRDBMS。2004年、[IBM](../Page/IBM.md "wikilink")はこれを[オープンソース](../Page/オープンソース.md "wikilink")とし、今後の保守を[Apache Software Foundationに委ねた](https://ja.wikipedia.org/wiki/Apache_Software_Foundation "wikilink")。名称は[Apache Derbyとなっている](https://ja.wikipedia.org/wiki/Apache_Derby "wikilink")。
  - UniVerse、UniData - [多次元データベース](https://ja.wikipedia.org/wiki/多次元データベース "wikilink")はSQLでは扱いにくいネットワーク/階層/配列などのデータモデルを扱う。

## 参考文献

<references/>

## 外部リンク

  - [Informix V12.10 資料 - IBM](https://www.ibm.com/support/knowledgecenter/ja/SSGU8G_12.1.0/com.ibm.welcome.doc/welcome.htm)
  - [日本IBMプレスリリース 2008/05/18・Informix Dynamic Server V11.5](http://www-06.ibm.com/jp/press/2008/05/0803.html)
  - [IIUG (International Informix Users Group)](http://www.iiug.org/)
  - [The (good) problem with Informix](http://www.theregister.co.uk/2004/10/19/ibm_informix_db2/)
  - [The Informix Handbook](http://www.informixhandbook.com/)
  - [The Informix Zone](http://www.informix-zone.com/)
  - [Database-Books.us](http://www.database-books.us/informix.php) - Informix database books online.

[Category:データベース管理システム](https://ja.wikipedia.org/wiki/Category:データベース管理システム "wikilink") [Category:IBMのソフトウェア](https://ja.wikipedia.org/wiki/Category:IBMのソフトウェア "wikilink") [Category:かつて存在したアメリカ合衆国のソフトウェア会社](https://ja.wikipedia.org/wiki/Category:かつて存在したアメリカ合衆国のソフトウェア会社 "wikilink")

1.  記事のアーカイブ [HP's Secret Software Weapon](http://web.archive.org/web/20050719075914/http://www.interex.org/hpworldnews/hpw207/features5.jsp)、[出典](http://www.interex.org/hpworldnews/hpw207/features5.jsp)