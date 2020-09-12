> この記事は[Informix](https://ja.wikipedia.org/wiki/Informix)から翻訳されています。


**Informix Corporation**（インフォミックス コーポレーション）は、かつて[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")にあった[ソフトウェア](../Page/ソフトウェア.md "wikilink")企業である。[関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink") (RDBMS) 製品群[Informixを開発したが](../Page/IBM_Informix.md "wikilink")、経営不振により2001年に[IBM](../Page/IBM.md "wikilink")に買収された\[1\]。

## 歴史

### 1980年: 草創期

ロジャー・シップル(Roger Sippl)とローラ・キング(Laura King)は、[S-100バス](../Page/S-100バス.md "wikilink")コンピュータメーカーである[クロメンコ](../Page/クロメンコ.md "wikilink")に勤務していた。そこで報告書作成ソフトウェアのための [ISAM技術に基づいた小型の](../Page/Indexed_Sequential_Access_Method.md "wikilink")[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")の開発に従事した。

シップルとキングは1980年にクロメンコ社を辞め、**Relational Database Systems** (RDS）を設立した。最初の製品*Marathon*は彼らがクロメンコで開発したシステムの16ビット版であり、[ザイログ](../Page/ザイログ.md "wikilink")の初期の[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")向けの[UNIX](../Page/UNIX.md "wikilink") (Onyx) 上で動作した。

彼らは成長しつつある[関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink") (RDBMS) 市場に注目し、1981年に**Informix** (INFORMation on unIX）をリリースした。これには独自の言語 **Informer** が含まれていた。また、データを抽出して読みやすい報告書を作成するサブシステム**ACE**も付属していた。画面入力フォーム作成ツール**PERFORM**もあり、ユーザーが対話的にデータベースとやりとりすることができた。この製品の最終バージョンは3.30で、1986年にリリースされた。

[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")、新たな[SQL](../Page/SQL.md "wikilink")ベースのクエリエンジンが**INFORMIX-SQL** (ISQL) バージョン1.10の一部としてリリースされた。もちろんACEとPERFORMのSQL対応版も含まれている。ISQLと以前のInformixの最大の違いは、データベースアクセスコードをクライアントコードと完全に分離した点である。これがクライアント・サーバ型のデータベースシステムへの布石となった。

1980年代前半を通してInformixは市場で優位に立つことはなかったが、1980年代中ごろにはUNIXとSQLの組合せが人気となり、情勢が変わってきた。[1986年](../Page/1986年.md "wikilink")には[株式公開](../Page/株式公開.md "wikilink")にこぎつけ、社名を**Informix Software**に変更した。当時の製品はINFORMIX-SQLバージョン2.00と INFORMIX-4GL 1.00であり、どちらもデータベースエンジンと開発ツールを含んでいる（I4GLはプログラマ向け、ISQLは非プログラマ向け）。

その後も新製品のリリースが続き、新たなクエリエンジンを使ったINFORMIX-Turboがリリースされた。TurboはISAMよりマルチユーザー性能が優れたRSAM技術を使っている。1989年、バージョン4.00製品がリリースされ、TurboはINFORMIX-OnLineと改称（オンライン状態でユーザーが使用中にデータベースバックアップが可能）、従来のC-ISAMベースのサーバ機能（ISQLとI4GL）はツール群と分離され、INFORMIX-SE (Standard Engine) と改称された。Informix OnLineのバージョン5.00は1990年末にリリースされた。これには[2相コミット](../Page/2相コミット.md "wikilink")と[ストアドプロシージャ](../Page/ストアドプロシージャ.md "wikilink")による[分散トランザクション](https://ja.wikipedia.org/wiki/分散トランザクション "wikilink")機能が含まれている。

### 1988年: Innovative Software 買収

[1988年](../Page/1988年.md "wikilink")、InformixはDOSおよびUNIX向けのオフィスソフトのメーカー**Innovative Software**を買収した。特に[WingZ](https://ja.wikipedia.org/wiki/WingZ "wikilink")という[Macintosh](../Page/Macintosh.md "wikilink")用[表計算ソフト](../Page/表計算ソフト.md "wikilink")が有名であった。

[WingZ](https://ja.wikipedia.org/wiki/WingZ "wikilink")は高度なGUIで巨大な表が使え、HyperScript と呼ばれる[HyperCard](../Page/HyperCard.md "wikilink")風の言語でプログラミング可能であった。最初のリリースは好評で、[Microsoft Excelに次ぐ](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")2位のシェアを獲得した。[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")、WingZは主に[UNIX](../Page/UNIX.md "wikilink")系OS向けにいくつかのプラットフォームに移植され始めた。このころ、多くの金融機関は大型の金融モデルを計算するためにパーソナルコンピュータよりも強力なシステムを必要としており、UNIXワークステーションがその目的で使われ始めたのであった。そのため、ある期間WingZはこのニッチ市場で成功を収めた。

しかし、サーバ向けでないソフトウェア市場に対する全体的な理解不足から、開発やマーケティングのリソースが不足するようになった。1990年代初めWingZは競争力を失い、Informixはこれを[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")に売却した。また、ライセンスは[クラリス](../Page/クラリス.md "wikilink")に売却され、そこからGUIを改良してClaris Resolveが生まれた。

### 1994年: 動的スケーラブルアーキテクチャ

オフィスソフトで失敗し、Informixは再度データベースサーバ市場に注力するようになった。1994年、[シークエント・コンピュータ](../Page/シークエント・コンピュータ.md "wikilink")との協業でInformixはバージョン6.00データベースサーバをリリースした。その目玉となった機能が動的スケーラブルアーキテクチャ (DSA) である。

DSAは製品のエンジン中核部を大幅に刷新し、垂直および水平の並行性をサポートするもので、シークエントが得意とした[対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink")向きのマルチスレッド型コアを採用していた。この動きに[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")や[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")も追随した。これにより業界でもトップレベルの[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")を備え、[OLTPにも](../Page/オンライントランザクション処理.md "wikilink")[データウェアハウス](../Page/データウェアハウス.md "wikilink")にも対応可能となった。

現在は**[Informix Dynamic Server](https://ja.wikipedia.org/wiki/Informix_Dynamic_Server "wikilink")** (**IDS**) として知られるこの製品は 1994年にバージョン7がリリースされた。当時、ちょうどUNIXでは対称型マルチプロセッシングが一般化しつつあった。バージョン7は当時の競合他社製品より進んでおり、性能[ベンチマーク](../Page/ベンチマーク.md "wikilink")でも常に勝っていた。その結果、Informixは1997年までに[サイベース](https://ja.wikipedia.org/wiki/サイベース "wikilink")を押しのけ、業界2位となったのである。

バージョン7の成功により、Informixは中核部分の設計を2段階とし、従来からの延長を*XMP* (eXtended Multi Processing)、より大型のシステム向けを*XPS* (eXtended Parallel Server) として、バージョン8をリリースした。XPSは[データウェアハウス](../Page/データウェアハウス.md "wikilink")やクラスター上のデータベースを指向している。

### 1995年: Illustra 買収

[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")、Informixは[オブジェクト関係データベース](../Page/オブジェクト関係データベース.md "wikilink") (ORD) に着目し、[Illustra](https://ja.wikipedia.org/wiki/Illustra "wikilink")を買収した。Illustraは[マイケル・ストーンブレーカー](../Page/マイケル・ストーンブレーカー.md "wikilink")の[Postgres開発チームが作ったもので](../Page/Ingres.md "wikilink")、データベースと[オブジェクトを関連付ける各種機能を備え](../Page/オブジェクト指向.md "wikilink")、多くのプロジェクトでプログラミングにかかる時間を劇的に改善できる機能が備わっていた。Illustraには**DataBlades**と呼ばれる新たなデータ型をサーバに導入できる機能があった。これらの機能がSQLが[時系列](../Page/時系列.md "wikilink")データやマルチメディアデータを扱う際の問題への解決策を与えた。Informixはこれらの機能を7.x OnLine製品に取り入れ、**[Informix Universal Server](https://ja.wikipedia.org/wiki/Informix_Universal_Server "wikilink")** (IUS) と名づけた（また、通常バージョン9と呼ばれている）。

V8 (XPS) と V9 (IUS) は[1996年](../Page/1996年.md "wikilink")にリリースされ、Informixは3大データベース企業（他は[オラクルと](../Page/オラクル_\(企業\).md "wikilink")[サイベース](https://ja.wikipedia.org/wiki/サイベース "wikilink")）の中でいち早くオブジェクト関係データベースをサポートすることとなった。特にDataBladesは注目され、人気となり、即座に各プラットフォームに移植されていった。他社はこの動きにあわてた。オラクルは追加パッケージとして時系列サポートを1997年に行い、サイベースは[サードパーティー](../Page/サードパーティー.md "wikilink")に解決策を求めた。

### 1997年: 経営問題

技術的には成功したものの、マーケティングと企業運営での失敗が影を落とした。1997年4月1日、Informixは収益が予測より1億ドル少ないことを公表した。この時点がInformixの成長の最高点だった。技術的には進化を続けたものの、1997年の[CEO解任に端を発した経営陣のごたごたにより](../Page/最高経営責任者.md "wikilink")、会社は勢いを失っていった。

### 2001年: その他の買収

[2000年](../Page/2000年.md "wikilink")、Informixに起きた出来事はもはや技術革新の話ではなかった。3月、Informixは、それまでも何度も合併を繰り返してきたArdent Softwareを買収した。これにより、多次元型エンジンUniVerseとUniDataが製品系列に加わった。他にもInformix以外のエンジンとしてデータウェアハウス向けのRed Brick、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で書かれたCloudscapeなどもあった。

6月、Ardentの前CEO James D. FoyがInformixのCEOに就任し、彼はInformixを買収の対象として魅力的になるよう改編していった。大きな変更として、全てのデータベースエンジン技術とアプリケーションおよびツールを分離した。

[2001年](../Page/2001年.md "wikilink")、IBMはInformixを買収し、そのデータベース技術とブランドと将来の開発計画と10万を超える顧客ベースを入手した。アプリケーションおよびツールは買収には含まれず、Ascential Softwareという会社になった。

2005年5月、IBMはAscential Softwareの買収も完了した。

### 2002年: 経営問題の余波

[2002年](../Page/2002年.md "wikilink")11月、1997年に解任された元CEOフィリップ・ホワイトは連邦大陪審に起訴され、セキュリティ、メール詐欺など8つの訴因で告発された。13ヵ月後、司法取引により米国証券取引委員会への偽の報告書提出の罪を認めた。

[2004年](../Page/2004年.md "wikilink")5月、司法省はホワイトが2ヶ月間連邦刑務所に収監されたことを発表した。また、罰金は1万ドルで、2年間保護観察下におかれ、300時間の公共サービス従事が義務付けられた。この発表では、これらが株主が被った損害を考慮した罰ではないことを強調した。

Informixでヨーロッパを任されていたWalter Königsederも同様に起訴されたが、ドイツ在住であったため、引渡しが行われなかった。

2005年11月、Informixと フィル・ホワイトの事の顛末を記した本が出版された。

## 参考文献

<references/>

[Category:かつて存在したアメリカ合衆国のソフトウェア会社](https://ja.wikipedia.org/wiki/Category:かつて存在したアメリカ合衆国のソフトウェア会社 "wikilink")

1.  記事のアーカイブ [HP's Secret Software Weapon](https://web.archive.org/web/20050719075914/http://www.interex.org/hpworldnews/hpw207/features5.jsp)、[出典](http://www.interex.org/hpworldnews/hpw207/features5.jsp)