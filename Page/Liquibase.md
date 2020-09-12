> この記事は[Liquibase](https://ja.wikipedia.org/wiki/Liquibase)から翻訳されています。


**Liquibase** は、データベーススキーマの変更を追跡、管理、適用するための[オープンソース](../Page/オープンソース.md "wikilink")のデータベースに依存しないライブラリである。Liquibase は、特に[アジャイルソフトウェア開発](../Page/アジャイルソフトウェア開発.md "wikilink")において、データベースの変更をより簡単に追跡できるようにするために2006年に開始された。

## 概観

データベースへのすべての変更はテキストファイル([XML](../Page/Extensible_Markup_Language.md "wikilink")、[YAML](../Page/YAML.md "wikilink")、[JSONまたは](../Page/JavaScript_Object_Notation.md "wikilink")[SQL](../Page/SQL.md "wikilink"))に保存され、ファイル名と同様に「id」タグと「author」タグの組み合わせで識別される。適用されたすべての変更のリストが各データベースに保存され、すべてのデータベース更新時に参照され、どのような新しい変更が適用される必要があるかを判断する。その結果、データベースのバージョン番号はないが、このアプローチにより、複数の開発者やコードブランチが存在する環境でも機能するようになる。

Liquibase は、最初にChangeLogファイルを実行すると、自動的にDatabaseChangeLogテーブルとDatabaseChangeLog Lock テーブルを作成する。

## 主な機能

  - 30以上の組み込みデータベースリファクタリング
  - カスタム変更を作成するための拡張性
  - データベースを最新バージョンに更新
  - 最後のX回の変更をデータベースにロールバック
  - データベースの変更を特定の日時にロールバック
  - データベースを「タグ」にロールバック
  - データベースの更新とロールバックのためのSQLは、手動でレビューするために保存することができます。
  - スタンドアロン[IDE](../Page/統合開発環境.md "wikilink") と[Eclipseプラグイン](../Page/Eclipse_\(統合開発環境\).md "wikilink")
  - 実行する変更セットを含む/除外するための 「コンテキスト」
  - データベース差分レポート
  - データベースの差分変更履歴の生成
  - 既存のデータベースを生成するための変更ログを作成する能力
  - データベースの変更ドキュメントの生成
  - DBMSチェック、ユーザーチェック、SQLチェックの前提条件
  - 変更ログを複数のファイルに分割して管理しやすくする機能
  - コマンドライン、[Apache Ant](../Page/Apache_Ant.md "wikilink")、[Apache Maven](../Page/Apache_Maven.md "wikilink")、[サーブレットコンテナー](../Page/Webコンテナ.md "wikilink")、または[Spring Framework経由で実行可能](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink")。
  - 10種類のデータベースシステムをサポート

## 商用版

[Liquibase（旧Datical）](http://www.liquibase.com) \[1\]は、Liquibaseプロジェクトへの最大のコントリビューターであり、Liquibase Enterprise \[2\]開発者でもある。商用版はLiquibaseコア機能と追加機能を提供する。

  - 変更予測：変更がデータに与える影響を判断するために、実行前に実行される変更を予測する。 \[3\]
  - 企業の標準とポリシーを適用するルールエンジン。 \[4\]
  - データベースストアドロジックのサポート：関数、ストアドプロシージャ、パッケージ、テーブルスペース、トリガー、シーケンス、ユーザー定義タイプ、シノニムなど。
  - データベース比較を利用すると、2つのデータベーススキーマを比較して変更を識別し、それを変更ログに簡単に移動できる。
  - 変更セットウィザードを使用すると、データベースに中立的な方法でデータベースの変更を簡単に定義およびキャプチャできる。
  - 論理的な展開ワークフローをモデル化および管理するための展開計画ウィザード
  - [Jenkins](https://ja.wikipedia.org/wiki/Jenkins "wikilink") 、Atlassian Bamboo、UrbanCode、CA Release Automation（Nolio）、Serena Release Automation、BMC Bladelogic、 [Puppet](https://ja.wikipedia.org/wiki/Puppet_\(ソフトウェア\) "wikilink") 、 Chef \[5\]、および[SVN](../Page/Apache_Subversion.md "wikilink")、[Git](../Page/Git.md "wikilink") 、[TFS](https://ja.wikipedia.org/wiki/Azure_DevOps_Server "wikilink")、[CVSなどの一般的なソース管理システム全てのプラグイン](../Page/Concurrent_Versions_System.md "wikilink")

Liquibase Enterprise（旧称：Datical DB）を含むLiquibase製品は、アプリケーションリリースプロセスに関わるDBA、リリースマネージャ、DevOpsチーム、アプリケーションオーナー、アーキテクト、開発者に利用されている。Liquibase は、エラーや遅延を排除し、迅速なアジャイルリリースを可能にするために、アプリケーションコードと一緒にデータベーススキーマの変更をプログラム的に管理する。Liquibase商用版は、開発環境からテスト環境、本番環境に移行する際に、アプリケーションバージョン全体のデータ構造固有のコンテンツを管理するためのLiquibase Data Modelアプローチに基づいている。Liquibase Enterpriseは、デプロイ前に、どのような環境でもスキーマ変更の影響をプレビューすることで、リスクを軽減し、よりスムーズで迅速なアプリケーション変更を実現する。

Liquibase開発者のNathan Voxlandは、Liquibase（旧Datical）の幹部である。 \[6\]

## Liquibase ChangeLogファイルのサンプル

``` xml
<?xml version="1.0" encoding="UTF-8"?>

<databaseChangeLog
        ns="http://www.liquibase.org/xml/ns/dbchangelog/1.3"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xsi:schemaLocation="http://www.liquibase.org/xml/ns/dbchangelog/1.3
        http://www.liquibase.org/xml/ns/dbchangelog/dbchangelog-1.3.xsd">
    <preConditions>
            <dbms type="oracle"/>
    </preConditions>

    <changeSet id="1" author="author1">
        <createTable tableName="persons">
            <column name="id" type="int" autoIncrement="true">
                <constraints primaryKey="true" nullable="false"/>
            </column>
            <column name="name" type="varchar(50)"/>
        </createTable>
    </changeSet>

    <changeSet id="2" author="author2" context="test">
        <insert tableName="persons">
            <column name="id" value="1"/>
            <column name="name" value="Test1"/>
        </insert>
        <insert tableName="persons">
            <column name="id" value="2"/>
            <column name="name" value="Test2"/>
        </insert>
    </changeSet>
</databaseChangeLog>
```

## 関連ツール

  - Flyway
  - alembic

## 外部リンク

  -
[Category:アジャイルソフトウェア開発](https://ja.wikipedia.org/wiki/Category:アジャイルソフトウェア開発 "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:データベース接続クライアント](https://ja.wikipedia.org/wiki/Category:データベース接続クライアント "wikilink")

1.  <https://www.liquibase.com/blog/2020-05-19>
2.
3.
4.
5.
6.