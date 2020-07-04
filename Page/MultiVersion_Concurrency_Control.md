> この記事は[MultiVersion Concurrency Control](https://ja.wikipedia.org/wiki/MultiVersion_Concurrency_Control)から翻訳されています。


**MultiVersion Concurrency Control** (**MVCC**, マルチバージョン コンカレンシー コントロール) は、[データベース管理システム](../Page/データベース管理システム.md "wikilink")の可用性を向上させる制御技術のひとつ。複数のユーザから同時に処理要求が行われた場合でも同時並行性を失わずに処理し、かつ情報の一貫性を保証する仕組みが提供される。日本では**多版型同時実行制御**、**多重バージョン並行処理制御**などと訳される。また単に**マルチバージョン**とも呼ばれる。

## 動作

MVCCは、書き込み処理（[トランザクション](../Page/トランザクション.md "wikilink")）が行われている最中に他のユーザによる読み取りアクセスがあった場合、書き込みの直前の状態（[スナップショット](https://ja.wikipedia.org/wiki/スナップショット "wikilink")）を処理結果として返す。つまり、書き込み中も読み取りができ、読み取り中でも書き込みができる。

MVCCにおいて可用性を達成するには、最低限、全ての処理が「どの順番で」行われたかを確実に記録する必要がある。そのため、タイムスタンプやトランザクションIDなどを用いて全ての更新処理が管理される。

なお、[SQL](../Page/SQL.md "wikilink")規格(SQL92)で定められた4種類の[トランザクション分離レベル](https://ja.wikipedia.org/wiki/トランザクション分離レベル "wikilink")においては、**Read Committed** (コミット済みデータは常に読み取る) に該当する処理である。

## 歴史

MVCCの考え方は、[1981年](../Page/1981年.md "wikilink")に Philip A. Bernstein と Nathan Goodman により、 [ACM Computing Surveys](../Page/Association_for_Computing_Machinery.md "wikilink") 誌上に掲載された。

## MVCCの考え方を採用するデータベース

  - [Rethink DB](https://ja.wikipedia.org/wiki/Rethink_DB "wikilink")1.0 以降
  - [Berkeley DB](../Page/Berkeley_DB.md "wikilink")
  - [DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink") 9.7以降(CS with CC)
  - [Firebird](../Page/Firebird.md "wikilink")
  - [H2 Database](../Page/H2_Database.md "wikilink")
  - [InterBase](../Page/InterBase.md "wikilink")
  - [Microsoft SQL Server 2005以降のREAD](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")_COMMITTED_SNAPSHOT
  - [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink") （ただし、エンジンに InnoDB を使用したとき）
  - [Oracle Database](../Page/Oracle_Database.md "wikilink") Oracle 4 以降
  - [SAP IQ](https://ja.wikipedia.org/wiki/SAP_IQ "wikilink")
  - [PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")6.5 以降
  - [Zope Object Database](../Page/Zope.md "wikilink")
  - [OrientDB](https://ja.wikipedia.org/wiki/OrientDB "wikilink")

## MVCCの考え方を採用するその他のソフトウェア

  - [Clojure](https://ja.wikipedia.org/wiki/Clojure "wikilink")の[ソフトウェアトランザクショナルメモリ](../Page/ソフトウェアトランザクショナルメモリ.md "wikilink")
  - [バージョン管理システム](../Page/バージョン管理システム.md "wikilink")全般

## 関連項目

  - [Snapshot isolation](https://ja.wikipedia.org/wiki/Snapshot_isolation "wikilink")
  - [Serializable isolation](https://ja.wikipedia.org/wiki/直列化可能性 "wikilink")
  - [時刻印ロック](https://ja.wikipedia.org/wiki/時刻印ロック "wikilink")
  - [リード・コピー・アップデート](../Page/リード・コピー・アップデート.md "wikilink")

[Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink") [Category:トランザクション処理](https://ja.wikipedia.org/wiki/Category:トランザクション処理 "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")