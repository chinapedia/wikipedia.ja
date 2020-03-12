> この記事は[Java Data Objects](https://ja.wikipedia.org/wiki/Java_Data_Objects)から翻訳されています。


**Java Data Objects** (**JDO**) とは、[Java](../Page/Javaプラットフォーム.md "wikilink")[オブジェクトの](../Page/オブジェクト_\(プログラミング\).md "wikilink")[永続性に関する仕様である](https://ja.wikipedia.org/wiki/永続性_\(計算機科学\) "wikilink")。[ドメインモデル](https://ja.wikipedia.org/wiki/ドメインモデル "wikilink")の永続的サービスの透過性などもそれに含まれる。JDOの永続的オブジェクトは通常の[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の[クラスである](../Page/クラス_\(コンピュータ\).md "wikilink")。永続性を持たせるために特別なインタフェースを実装する必要もないし、特別なクラスから継承する必要もない。JDO 1.0は[Java Community Processの](../Page/Java_Community_Process.md "wikilink")[JSR 12](http://www.jcp.org/en/jsr/detail?id=12)として[2002年](../Page/2002年.md "wikilink")[4月30日](../Page/4月30日.md "wikilink")にリリースされた。JDO 2.0は[JSR 243](http://www.jcp.org/en/jsr/detail?id=243)として開発され、[2006年](../Page/2006年.md "wikilink")[5月10日](../Page/5月10日.md "wikilink")にリリースされた。

## 概要

オブジェクトの永続性は、外部の[XMLメタファイルで定義され](../Page/Extensible_Markup_Language.md "wikilink")、その中にはベンダー固有の拡張を含めることも可能である。JDOベンダーは開発者向けにエンハンサ (enhancers) を提供する。エンハンサはコンパイル済みの[Javaクラスファイル](https://ja.wikipedia.org/wiki/Javaクラスファイル "wikilink")を編集し、透過的な永続性が得られるようにする。JDOの仕様ではバイトコードの改良を必須としているわけではないが、JDOを実装する手段としてはこれが一般的である。現在、JDOベンダーが提供する永続性にはいくつかのオプションがある。例えば、[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")への保存、[オブジェクトデータベース](../Page/オブジェクトデータベース.md "wikilink")への保存、[ファイルへの保存などである](../Page/ファイル_\(コンピュータ\).md "wikilink")。

JDO強化クラスは異なるベンダーの実装であっても機能する。一度強化（エンハンス）した Java クラスは任意のベンダーのJDO製品で使うことができる。

JDOは[Java EEにいくつかの方法で統合されている](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")。まず、ベンダー実装はJava EE Connectorとして提供される。そして、JDOはJava EE transaction service（[JTA](../Page/Java_Transaction_API.md "wikilink") Transaction Managerの実装）のコンテキストで動作する。

## JDOとJPA

[Enterprise JavaBeans](../Page/Enterprise_JavaBeans.md "wikilink") 3.0 (EJB 3.0) では、[永続性がカバーされている](https://ja.wikipedia.org/wiki/永続性_\(計算機科学\) "wikilink")。それはEJB 2.0のEntity Beansの発展したものである。しかしEJB 3.0はJDOを採用せずに、[Java Persistence API](../Page/Java_Persistence_API.md "wikilink") (JPA) 1.0を採用した。EJB 3.0はJDO 2.0のリリースの翌日の2006年5月11日に仕様が制定された。JDOとJPAは対立する仕様である。

JPAはjavax.persistenceパッケージを使い、EJB 3.0 ([JSR 220](http://www.jcp.org/en/jsr/detail?id=220)) の中の独立した文書で定義されている。JPAはEJBコンテナを必要とせず、JDOのようにJava SE環境でも機能する。しかし、JPAは[オブジェクト関係マッピング](../Page/オブジェクト関係マッピング.md "wikilink") (ORM) の仕様であって、JDOのようにデータストアの種類に関係なく使える、透過的なオブジェクトの永続の仕様ではない。

JPAはJava EEの仕様の一部であるため、JDOよりも多く使われている。JDOの商用製品やオープンソースのプロジェクトの中には、既にJPA APIも実装し選択肢を増やしているものがある。

## JDO 2.0での機能追加

  - Disconnected Object Graphsの概念
  - Standardized ORM Mapping Descriptors （ORMベースのJDO実装向け）
  - JDOQL拡張
  - Get e.g. a java.sql.Connection from javax.jdo.PersistenceManager
  - その他: Named Queries (pm.newNamedQuery), FetchPlan, Sequence, Delete by Query, multiple User Objects on PM

## 関連項目

  - [Java Persistence API](../Page/Java_Persistence_API.md "wikilink")
  - [オブジェクト関係マッピング](../Page/オブジェクト関係マッピング.md "wikilink")
  - [オブジェクトデータベース](../Page/オブジェクトデータベース.md "wikilink")
  - [Hibernate](../Page/Hibernate.md "wikilink")
  - [JPOX](../Page/JPOX.md "wikilink")

## 外部リンク

### 仕様

  - [JDO Home page at Sun's Web site](http://java.sun.com/products/jdo/)
  - [JSR 243: JDO 2.0 Specification](http://www.jcp.org/en/jsr/detail?id=243)
  - [JSR 12: JDO 1.0 Specification](http://www.jcp.org/en/jsr/detail?id=12)

### オープンソース実装

  - [JPOX](http://www.jpox.org/) – オープンソースのJDO 2リファレンス実装 ([ORM](../Page/オブジェクト関係マッピング.md "wikilink"))
  - [Eclipse JSR 220](http://www.eclipse.org/jsr220orm/) [ORM](../Page/オブジェクト関係マッピング.md "wikilink")
  - [Orient Technologies](http://sourceforge.net/projects/orient) – JDOインタフェースを持つ[ODBMS](../Page/オブジェクトデータベース.md "wikilink")
  - [JDOinstruments](http://sourceforge.net/projects/jdoinstruments) – JDOインタフェースを持つODBMS
  - [Speedo](http://speedo.objectweb.org) – オープンソースのJDO 2実装 (ORM)
  - [Apache JDO](http://db.apache.org/jdo/) - オープンソースのJDO 2実装

### コミュニティなど

  - [JDOcentral.com Community Site](http://www.jdocentral.com/)
  - [JavaPersistence Community Site](http://www.javapersistence.com/)

[Category:オブジェクト関係マッピング](https://ja.wikipedia.org/wiki/Category:オブジェクト関係マッピング "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:Java_enterprise_platform](https://ja.wikipedia.org/wiki/Category:Java_enterprise_platform "wikilink") [Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink") [Category:永続性](https://ja.wikipedia.org/wiki/Category:永続性 "wikilink")