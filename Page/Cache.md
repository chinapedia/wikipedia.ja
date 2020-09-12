> この記事は[Cache](https://ja.wikipedia.org/wiki/Cache)から翻訳されています。


**Caché**（キャシエ）は、[インターシステムズ](https://ja.wikipedia.org/wiki/インターシステムズ "wikilink")が開発したプロプライエタリな[MUMPS](../Page/MUMPS.md "wikilink")ベースの[データベース管理システム](../Page/データベース管理システム.md "wikilink")である。インターシステムズはその特徴を「ポストリレーショナル」と称している。Cachéは同じデータに対して、[SQL](../Page/SQL.md "wikilink")アクセス、[オブジェクトアクセス](../Page/オブジェクト_\(プログラミング\).md "wikilink")、階層型アクセスを提供している。

Cachéは[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、各種[UNIX](../Page/UNIX.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[OpenVMS](../Page/OpenVMS.md "wikilink")で動作する。

内部的にはCachéは多次元配列にデータを格納し、階層的構造化データとして扱うこともできる（MUMPSのglobalsとして知られているが、インターシステムズはMUMPSの名をあまり使いたがらない）。しかし、多くのアプリケーションは[オブジェクトアクセス手法か](../Page/オブジェクト_\(プログラミング\).md "wikilink")[SQL](../Page/SQL.md "wikilink")アクセス手法を使う。アプリケーションの[ビジネスロジック](../Page/ビジネスロジック.md "wikilink")の開発にはCaché ObjectScriptやCaché Basicを使う。外部[インタフェースとしては](../Page/インタフェース_\(情報技術\).md "wikilink")、[C++](../Page/C++.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[EJB](../Page/Enterprise_JavaBeans.md "wikilink")、[ActiveX](../Page/ActiveX.md "wikilink")へのNative Object Bindingがある。関係アクセスや高性能ダイレクトインタフェースとして、[JDBC](../Page/JDBC.md "wikilink") と[ODBCがある](../Page/Open_Database_Connectivity.md "wikilink")。[XMLと](../Page/Extensible_Markup_Language.md "wikilink")[Webサービス](../Page/Webサービス.md "wikilink")もサポートされている。Caché Server Pagesにより、Cachéデータベース上のデータを使って動的にWebページを生成するアプリケーションを構築可能である。

Cachéは高速さが特徴であるといわれ、リアルタイム・アプリケーションに最適とされている。高速さの要因として、データを最初から構造的に扱うこと、データをなるべくメモリ上に保とうとするアーキテクチャであることが挙げられる。

この製品の主な顧客はアメリカの大病院が多く、[電子カルテ](../Page/電子カルテ.md "wikilink") (EMR) システムをCachéで実現している。他にもネット証券会社[アメリトレード](https://ja.wikipedia.org/wiki/アメリトレード "wikilink")などもCachéを利用している。

## 競合する製品

主な競合製品/企業は、[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink") ([IBM](../Page/IBM.md "wikilink"))、[Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")（[マイクロソフト](../Page/マイクロソフト.md "wikilink")）、[Oracle](../Page/Oracle_Database.md "wikilink")、[Sybase](../Page/Sybase.md "wikilink")などである。

同じ用途で[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")と比較したとき、特に複雑なリレーションシップを含むシステムにおいてCachéは遥かに性能が良い（あるいは[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")が良い）とされる。この特徴は通常の[関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink") (RDBMS) において[ボトルネック](../Page/ボトルネック.md "wikilink")となりがちな[O/Rマッピング](https://ja.wikipedia.org/wiki/O/Rマッピング "wikilink")を必要としない、[MUMPS](../Page/MUMPS.md "wikilink")に由来するデータ構造によるものである。

## 外部リンク

  - [インターシステムズジャパン公式サイト](http://www.intersystems.co.jp/)
  - [Searchable Caché documentation](http://www.nlm.cz/search)
  - [cachemonitor.de](http://www.cachemonitor.de) - Caché におけるフリーなSQLクエリと管理ツール
  - [PlatinumCache](http://www.glocalizationbiz.com/product_info.php?manufacturers_id=12&products_id=43/)

[Category:データベース管理システム](https://ja.wikipedia.org/wiki/Category:データベース管理システム "wikilink") [Category:オブジェクト指向データベース管理システム](https://ja.wikipedia.org/wiki/Category:オブジェクト指向データベース管理システム "wikilink")