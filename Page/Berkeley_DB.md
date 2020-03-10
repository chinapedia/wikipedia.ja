> この記事は[Berkeley DB](https://ja.wikipedia.org/wiki/Berkeley_DB)から翻訳されています。


**Berkeley DB**は、[アプリケーション組み込み型の](../Page/アプリケーションソフトウェア.md "wikilink")[データベース](../Page/データベース.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")である。現在は[オラクルの製品であり](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")、また[オープンソース](../Page/オープンソース.md "wikilink")として公開されている。

## 歴史

Berkeley DBは、元々[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")の[プロジェクト](../Page/プロジェクト.md "wikilink")が4.3 [BSD](../Page/BSD.md "wikilink")に含まれる[AT\&T](../Page/AT&T.md "wikilink")由来のコードを置き換える過程\[1\]で生まれた。その後、開発者によって設立されたSleepycat Softwareが開発・販売を手がけていた。[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[2月](https://ja.wikipedia.org/wiki/2月 "wikilink")にオラクルがSleepycat Softwareを買収した\[2\]のちは、*Oracle Berkeley DB*とブランド名を変えオラクルの製品群の一部を成している。

## 特徴

Berkeley DBには、[Cで実装されたオリジナルの](../Page/C言語.md "wikilink")*Berkeley DB*、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で実装された*Berkeley DB Java Edition*、[XMLデータベース](https://ja.wikipedia.org/wiki/XMLデータベース "wikilink")の*Berkeley DB XML Edition*の三種類が存在する。いずれもオープンソースとして公開されているが、その用途に応じてオープンソース[ライセンス](../Page/ライセンス.md "wikilink")\[3\]と商用用途向けライセンスを選択できる[デュアルライセンス](../Page/デュアルライセンス.md "wikilink")方式を採っている。

いわゆる[リレーショナルデータベースではない](https://ja.wikipedia.org/wiki/関係データベース "wikilink")。

### Berkeley DB

オリジナルの*Berkeley DB*は、[UNIX](../Page/UNIX.md "wikilink")に古くから含まれていた[dbm](https://ja.wikipedia.org/wiki/dbm "wikilink")より発展したアプリケーション組み込み型データベースである。dbmと同じく、[SQL](../Page/SQL.md "wikilink")のような[データ操作言語](https://ja.wikipedia.org/wiki/データ操作言語 "wikilink")を持たず、データベースへのアクセスは全て[サブルーチン](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")呼び出しによって行う。しかしdbmとは異なり、データ操作機能に[トランザクション](../Page/トランザクション.md "wikilink")や[レプリケーション](../Page/レプリケーション.md "wikilink")に対応する[インタフェースが備わっているのが特徴である](../Page/インタフェース_\(情報技術\).md "wikilink")（[X/Open XAなど](https://ja.wikipedia.org/wiki/X/Open_XA "wikilink")）。その他に[ロックやオンライン](https://ja.wikipedia.org/wiki/ロック_\(情報工学\)#データベースのロック "wikilink")[バックアップ](../Page/バックアップ.md "wikilink")機能を持つ。

*Berkeley DB*本体が対応する[プログラミング言語](../Page/プログラミング言語.md "wikilink")はCおよび[C++](../Page/C++.md "wikilink")だけだが、[Perl](../Page/Perl.md "wikilink")、[Python](../Page/Python.md "wikilink")、[Tcl](https://ja.wikipedia.org/wiki/Tcl "wikilink")他多くの言語に[バインディングが用意されており](https://ja.wikipedia.org/wiki/束縛_\(情報工学\) "wikilink")、それらから容易に利用することができる。

### Berkeley DB Java Edition

Javaのみを使って実装されているため、[Java実行環境さえあればプロセッサや](../Page/Java_Runtime_Environment.md "wikilink")[OSを問わず利用できるのが大きな特徴である](../Page/オペレーティングシステム.md "wikilink")。 データベースそのものの機能はオリジナルのBerkeley DBとほぼ同等である。

### Berkeley DB XML Edition

[XQuery](https://ja.wikipedia.org/wiki/XQuery "wikilink")および[XPathによるXML文書の検索に特化したデータベースである](https://ja.wikipedia.org/wiki/XML_Path_Language "wikilink")。バックエンドに*Berkeley DB*を利用している。

## Berkeley DBを利用するソフトウェア

数多くのソフトウェアがBerkeley DBをバックエンドデータベース・ストレージとして現在または過去に採用している。

  - [Bogofilter](https://ja.wikipedia.org/wiki/Bogofilter "wikilink")
  - [GlusterFS](https://ja.wikipedia.org/wiki/GlusterFS "wikilink")
  - [KDevelop](../Page/KDevelop.md "wikilink")
  - [OpenLDAP](https://ja.wikipedia.org/wiki/OpenLDAP "wikilink")
  - [Spamassassin](https://ja.wikipedia.org/wiki/Spamassassin "wikilink")
  - [Apache Subversion](../Page/Apache_Subversion.md "wikilink")
  - [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")
      - バージョン5.1からはBerkeley DBのサポートを廃止した。
  - [Movable Type](https://ja.wikipedia.org/wiki/Movable_Type "wikilink")
      - バージョン4.0からはBerkeley DBのサポートを廃止した。

## 脚注

## 関連項目

  - [データベース管理システム](../Page/データベース管理システム.md "wikilink") (DBMS)
  - [関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink") (RDBMS)

## 外部リンク

  - [Oracle Berkeley DB Product Family](http://www.oracle.com/database/berkeley-db/)

  -
[Category:データベース管理システム](https://ja.wikipedia.org/wiki/Category:データベース管理システム "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:オラクル](https://ja.wikipedia.org/wiki/Category:オラクル "wikilink")

1.  [BSDの歴史](https://ja.wikipedia.org/wiki/BSD#歴史 "wikilink")
2.  [Oracle® Buys Open Source Software Company Sleepycat](http://www.oracle.com/corporate/press/2006_feb/sleepycat.html)
3.  [Open Source License for Berkeley DB](http://www.oracle.com/technology/software/products/berkeley-db/htdocs/oslicense.html)