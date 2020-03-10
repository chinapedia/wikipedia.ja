> この記事は[Hibernate](https://ja.wikipedia.org/wiki/Hibernate)から翻訳されています。


**Hibernate** は、[Java](https://ja.wikipedia.org/wiki/Java "wikilink") のための[オブジェクト関係マッピング](../Page/オブジェクト関係マッピング.md "wikilink") (ORM) ライブラリであり、[オブジェクト指向の](../Page/オブジェクト指向プログラミング.md "wikilink")[ドメインモデル](https://ja.wikipedia.org/wiki/ドメインモデル "wikilink")を[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")にマッピングするためのフレームワークを提供する。Hibernate は、[永続性に関わるデータベースアクセスを直接高レベルなオブジェクト操作機能に置換することでオブジェクト指向と関係モデルの不整合を解決する](https://ja.wikipedia.org/wiki/永続性_\(計算機科学\) "wikilink")。

Hibernate は[オープンソース](../Page/オープンソース.md "wikilink")の[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であり、[GNU Lesser General Public License](../Page/GNU_Lesser_General_Public_License.md "wikilink") で提供されている。

## 機能概要

第一の機能は、Javaクラスからデータベースの表（およびJavaデータ型から[SQL](../Page/SQL.md "wikilink")データ型）へのマッピングである。また、データのクエリと検索機能も提供する。SQL呼び出しを自動生成することで、開発者がSQL呼び出しの結果をいちいちオブジェクトに変換する手間から解放し、性能への影響を最小にしつつ、あらゆるSQLデータベースへの移植性を達成している。

Hibernate は [Plain Old Java Object](https://ja.wikipedia.org/wiki/Plain_Old_Java_Object "wikilink") (POJO) のための透過的永続性を提供する。永続性クラスに要求されることは、引数のない [コンストラクタ](https://ja.wikipedia.org/wiki/コンストラクタ "wikilink") が存在することであり、コンストラクタの可視性が *public* でなくともよい（一部アプリケーションでは、*equals()* と *hashCode()* メソッドにも注意が必要[1](http://www.hibernate.org/109.html)）。

Hibernate には「ダーティチェッキング」機能がある。この機能は、永続的オブジェクトの変更されたフィールドについてのみ SQL による更新を行うもので、不必要なデータベース更新を削減する。

Hibernate は「HQL」という[SQL](../Page/SQL.md "wikilink")ライクなクエリ言語を提供している。オブジェクト指向的な代替手段としてクライテリアクエリも提供されている。

Hibernate は[スタンドアローン](https://ja.wikipedia.org/wiki/スタンドアローン "wikilink")の[Java](https://ja.wikipedia.org/wiki/Java "wikilink")アプリケーションにも使えるし、[Java Servlet](../Page/Java_Servlet.md "wikilink") や [EJBセッションビーンを使った](../Page/Enterprise_JavaBeans.md "wikilink") [Java EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink") アプリケーションにも使える。

## 歴史

Hibernate は Gavin King をリーダーとして世界中の Java ソフトウェア開発者がチームを結成して開発した。その後、[JBoss](https://ja.wikipedia.org/wiki/JBoss "wikilink")社（現在は[レッドハット](../Page/レッドハット.md "wikilink")の一部）が Hibernate の主要開発者を雇い入れ、サポートを行うようになった。

バージョン3.xでは、Interceptor/Callback アーキテクチャ、ユーザ定義フィルタ、JDK 5.0 [アノテーション](https://ja.wikipedia.org/wiki/アノテーション "wikilink")（Javaの[メタデータ](https://ja.wikipedia.org/wiki/メタデータ "wikilink")機能）などの新機能が新たに追加された。このバージョンは[EJB](../Page/Enterprise_JavaBeans.md "wikilink") 3.0仕様とも非常に近く（ただし、EJB 3.0仕様が完成し[Java Community Processによってリリースされる前にリリースされた](https://ja.wikipedia.org/wiki/Java_Community_Process "wikilink")）、[JBoss](https://ja.wikipedia.org/wiki/JBoss "wikilink")のEJB 3.0実装の基盤となった。

## モジュール

Hibernate はモジュール化され、それぞれ独立したチームが開発している。

  - ORM (4.1 より前は Core)
    主モジュールであり、主要機能が全て実装されている（`Session` サポート、トランザクション管理、オブジェクト・キャッシング、HQL）。

  - Annotations
    JSR 175 の[アノテーション](https://ja.wikipedia.org/wiki/アノテーション "wikilink")サポート（JSR 220 [JPAアノテーション標準に準拠](https://ja.wikipedia.org/wiki/Java_Persistence_API "wikilink")）。XMLによるメタデータマッピングの代替手法を提供する。

  - Entity manager
    Core モジュールのラッパーであり、JSR 220 JPA Entity Manager 標準をサポート

  - Envers
    履歴管理

  - Metamodel Generator

  - OGM
    Object/Grid Mapper。[NoSQL](https://ja.wikipedia.org/wiki/NoSQL "wikilink") 対応。

  - Search
    Hibernate で管理されている永続性実体群に対して、[Lucene](https://ja.wikipedia.org/wiki/Lucene "wikilink") を使った検索を行うための抽象化層を提供するモジュール

  - Shards
    Hibernate Core の[縦分割を提供するモジュール](https://ja.wikipedia.org/wiki/分割_\(データベース\) "wikilink")

  - Tools
    [Apache Ant](https://ja.wikipedia.org/wiki/Apache_Ant "wikilink") のタスク群や[Eclipseプラグインなど](../Page/Eclipse_\(統合開発環境\).md "wikilink")、Hibernate を使った開発に役立つモジュール

  - Validator
    一般的なデータベースの制約（数値の範囲、文字列形式、ヌルチェックなど）を[アノテーション](https://ja.wikipedia.org/wiki/アノテーション "wikilink")を使って検証可能にするモジュール

## 永続性クラスのマッピング

JavaオブジェクトとSQLの変換をするには、JavaクラスとSQLテーブルの間の「マッピングデータ」がなければならない。Hibernate はこのためのいくつかの手段を提供する。

  - XMLメタデータ
    最も一般的な手法。各クラス（とそのプロパティ群）は、所定のDTDスキーマに対応したXML文書にて、XML要素として表現される。
  - [アノテーション](https://ja.wikipedia.org/wiki/アノテーション "wikilink")によるメタデータ
    JSR 175 に準拠して、永続性クラスのソースコードに注釈として記述する。Hibernate がそれを解釈して設定ファイルにそのクラスに関する情報を追加する（あるいは、実行時に `Configuration` インスタンスに追加する）。アノテーション機能は別モジュール化されている。
  - [XDoclet](https://ja.wikipedia.org/wiki/XDoclet "wikilink")メタデータ
    JSR 175 および Java 5.0 がリリースされる以前に、アノテーションと似たような機能を実装したもの。XDoclet 属性は永続性クラスのソースファイル上で記述され、[Apache Ant](https://ja.wikipedia.org/wiki/Apache_Ant "wikilink") の独立したタスクで構文解析され、XMLメタデータを生成する。
  - メタデータのプログラムからの操作
    Hibernate は、`SessionFactory` のインスタンスを生成する前に、マッピングの詳細を操作するAPI（`Configuration` インスタンスを使用）も提供している。

## ダーティチェッキング

不要なSQLによる更新を防ぐため、Hibernate はダーティチェッキングという機能を提供している。この機能は、永続的オブジェクトの変更されたフィールドやコレクションのみを更新できるようにするものである。コレクションに含まれない部分の更新が必要かどうかを確認するため、Hibernate はそれらのフィールドを `Object.equals()` メソッドで比較する。一方、コレクションフィールド（[`java.util.List`](http://java.sun.com/javase/6/docs/api/java/util/List.html) や [`java.util.Set`](http://java.sun.com/javase/6/docs/api/java/util/Set.html) など）は同一性（参照）比較を行う。

## API

Hibernate API は、[パッケージ](../Page/パッケージ_\(Java\).md "wikilink") [org.hibernate](http://www.hibernate.org/hib_docs/v3/api/index.html) で提供されている。

  - [org.hibernate.SessionFactory](http://www.hibernate.org/hib_docs/v3/api/org/hibernate/SessionFactory.html) インタフェース
    新たな Hibernate セッションを生成する[イミュータブル](../Page/イミュータブル.md "wikilink")で[スレッドセーフ](https://ja.wikipedia.org/wiki/スレッドセーフ "wikilink")なオブジェクトへの参照。Hibernate ベースのアプリケーションは、一般にこのインタフェースを実装したクラスのインスタンスを1つだけ使う（[Singleton パターン](https://ja.wikipedia.org/wiki/Singleton_パターン "wikilink") を利用）。
  - [org.hibernate.Session](http://www.hibernate.org/hib_docs/v3/api/org/hibernate/Session.html) インタフェース
    Hibernate セッション、すなわちデータベース上で行う操作の主要ポイントを表す。オブジェクトの永続性状態（一時的、永続的、分離）を管理し、データベースから永続的オブジェクトを取り出し、トランザクション境界を管理する。セッションは、データベース上の論理トランザクションと同程度に維持されることを意図している。セッションはスレッドセーフではなく、複数のクライアントから使われることを意図していない。

## 脚注

<references/>

## 関連項目

  - [EJB](../Page/Enterprise_JavaBeans.md "wikilink") 3.0
  - [NHibernate](https://ja.wikipedia.org/wiki/NHibernate "wikilink")
  - [Spring Framework](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink")
  - [シリアライズ](../Page/シリアライズ.md "wikilink")
  - [iBATIS](https://ja.wikipedia.org/wiki/iBATIS "wikilink")
  - [Service Data Objects](../Page/Service_Data_Objects.md "wikilink")
  - [Apache Struts](https://ja.wikipedia.org/wiki/Apache_Struts "wikilink")

## 参考文献

  - Christian Bauer, Gavin King: <cite>Java Persistence with Hibernate</cite>, Manning Publications Company, ISBN 1-932394-88-5
  - Christian Bauer, Gavin King: <cite>Hibernate In Action</cite>, Manning Publications Company, ISBN 1-932394-15-X
  - Will Iverson: <cite>Hibernate: A J2EE™ Developer's Guide</cite>, Addison Wesley Professional, ISBN 0-321-26819-9
  - James Elliott: <cite>Hibernate: A Developer's Notebook</cite>, [O'Reilly](https://ja.wikipedia.org/wiki/オライリー・メディア "wikilink"), ISBN 0-596-00696-9

## 外部リンク

  - [Hibernate公式サイト](http://www.hibernate.org)
  - [Interview with Gavin King, founder of Hibernate](http://www.javafree.org/content/view.jf?idContent=3)

[Category:オブジェクト関係マッピング](https://ja.wikipedia.org/wiki/Category:オブジェクト関係マッピング "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:Java_enterprise_platform](https://ja.wikipedia.org/wiki/Category:Java_enterprise_platform "wikilink") [Category:永続性](https://ja.wikipedia.org/wiki/Category:永続性 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")