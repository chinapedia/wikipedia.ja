> この記事は[Oracle TimesTen In-Memory Database](https://ja.wikipedia.org/wiki/Oracle_TimesTen_In-Memory_Database)から翻訳されています。


**Oracle TimesTen**とは 基幹DB([Oracle](../Page/Oracle_Database.md "wikilink"))を利用したシステム付加することができるインメモリのデータベース。([Oracle](../Page/Oracle_Database.md "wikilink")10gから完全サポート）

## 特徴

  - [データ](../Page/データ.md "wikilink")構造は、既存のRDBと同じ。[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")へのアクセスを最適化した[インデックス方式](../Page/索引.md "wikilink")
  - 速度は[RDBMSに比べて](../Page/関係データベース管理システム.md "wikilink")10倍程度
  - Oracleに買収されてからはCPUライセンスもしくは同時利用ユーザライセンスになっている。

## アプリケーション・インターフェース

  - [SQL](../Page/SQL.md "wikilink")-92準拠
  - [ODBC](../Page/Open_Database_Connectivity.md "wikilink")、[JDBC](../Page/JDBC.md "wikilink")、JMS API for Data publish等

## 特性

  - [データ](../Page/データ.md "wikilink")の更新に伴う[データ](../Page/データ.md "wikilink")・数値・計算値等の変化を任意の定義にもとづく設定により、別[アプリケーションに通知](../Page/アプリケーションソフトウェア.md "wikilink")。
  - アプリケーションからのリクエストに応じて、[Oracle Database](../Page/Oracle_Database.md "wikilink") 10gのレコードをTimesTen上のデータストアにロードする「動的データローディング」
  - 使用頻度が低いキャッシュデータを自動的に削除する「自動データエージング」
  - インメモリのため、株価ボードのように一度の更新されたデータを、大多数ユーザーが見るような処理に向いているデータベースである。

## 歴史

  - 2005年6月、イン[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")DBのトップベンダーだった米タイムズテンを買収
  - Oracle Databaseラインアップへの統合されておりバージョンがあがるにつれて、Oracle Databaseとの親和性が向上している。
  - Oracle以外のSybaseやDB2などのデータベースにも対応しているが,データの同期などを考えるとOracleが使われていることがほとんどである。

[Category:関係データベース管理システム](https://ja.wikipedia.org/wiki/Category:関係データベース管理システム "wikilink") [Category:オラクル](https://ja.wikipedia.org/wiki/Category:オラクル "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")