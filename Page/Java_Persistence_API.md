> この記事は[Java Persistence API](https://ja.wikipedia.org/wiki/Java_Persistence_API)から翻訳されています。


**Java Persistence API**（**JPA**）とは、[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")のデータを扱う [Java SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") および [Java EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink") のアプリケーションを開発するための[Java](https://ja.wikipedia.org/wiki/Java "wikilink")用フレームワークである。

JPA は、以下の3つの部分から成る。

  - API（javax.persistence パッケージで定義されている）
  - Java Persistence Query Language
  - オブジェクト/関係メタデータ

JPAの[リファレンス実装](../Page/リファレンス実装.md "wikilink")は[EclipseLinkとして実装されている](https://ja.wikipedia.org/wiki/:en:EclipseLink "wikilink")。

## 歴史

Java Persistence [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") 1.0 は、[JSR 220](http://www.jcp.org/en/jsr/detail?id=220) ([EJB](../Page/Enterprise_JavaBeans.md "wikilink") 3.0) Expert Group の作業の一部として[2006年](../Page/2006年.md "wikilink")[5月11日](../Page/5月11日.md "wikilink")に策定された。JPA 2.0は[JSR 317](http://www.jcp.org/en/jsr/detail?id=317)として、[2009年](../Page/2009年.md "wikilink")[12月10日](../Page/12月10日.md "wikilink")に Java EE 6 や EJB 3.1 と同一日に承認された。JPA 2.1は[JSR 338](https://jcp.org/en/jsr/detail?id=338)として、[2013年](../Page/2013年.md "wikilink")[4月22日](../Page/4月22日.md "wikilink")に承認された。

## エンティティ

JPAにおける[永続性エンティティは](https://ja.wikipedia.org/wiki/永続性_\(計算機科学\) "wikilink")、[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")における表を表した軽量Javaクラスである。そのインスタンスは表の個別の行に対応する。通常、他のエンティティとの関係を持ち、その関係はオブジェクト/関係メタデータで表される。オブジェクト/関係メタデータは、[アノテーション](../Page/アノテーション.md "wikilink")を使ってエンティティクラスのソースファイルに直接記述することもできるし、別の[XMLファイルとして記述することもできる](../Page/Extensible_Markup_Language.md "wikilink")。

## Java Persistence Query Language

Java Persistence Query Language (JPQL) は、関係データベースに格納されたエンティティに対する[クエリ](https://ja.wikipedia.org/wiki/クエリ "wikilink")に使用される。文法的には[SQL](../Page/SQL.md "wikilink")に似ているが、データベースの表を直接操作するのではなく、エンティティオブジェクトを操作する。

## Enterprise JavaBeans との関係

Java Persistence API 1.0 は [EJB](../Page/Enterprise_JavaBeans.md "wikilink") 3.0 仕様の一部であり、EJB 3.0 は Java EE 5 プラットフォームの一部である。ただし、永続性を利用したアプリケーションを実行するのに EJB コンテナや Java EE [アプリケーションサーバ](../Page/アプリケーションサーバ.md "wikilink")が必須というわけではない。

Java Persistence API 2.0 は EJB 3.1 とは分離され、独立した[JSR仕様として定義された](../Page/Java_Community_Process.md "wikilink")。EJB 3.1 や JPA 2.0 は Java EE 6 の一部である。

## Service Data Object API との関係

Java Persistence API は、[Hibernate](../Page/Hibernate.md "wikilink") や [TopLink](https://ja.wikipedia.org/wiki/TopLink "wikilink") などの[オブジェクト関係マッピング](../Page/オブジェクト関係マッピング.md "wikilink")ツールの主要機能である関係永続性のために設計された。一般に Java Persistence API は EJB 2.0 仕様を大幅に強化したものと受け取られている。[Service Data Objects](../Page/Service_Data_Objects.md "wikilink") (SDO) API (JSR 235) は Java Persistence API とは目的が異なり、相互に補完するものとされている。SDO API は[サービス指向アーキテクチャ](../Page/サービス指向アーキテクチャ.md "wikilink")のために設計されており、関係データモデルだけでなく様々なデータ形式や各種プログラミング言語を扱う。SDO API のJavaバージョンは[JCPによって管理され](../Page/Java_Community_Process.md "wikilink")、[C++](../Page/C++.md "wikilink")バージョンは[OASISが管理する](../Page/OASIS_\(組織\).md "wikilink")。

## 開発の背景

EJB 2.0 までの Entity Bean などのエンタープライズ・ビーンは、重すぎて複雑すぎ、Java EE アプリケーションサーバでしか使えないという問題があった。このため、その代替として [Data Access Object](../Page/Data_Access_Object.md "wikilink") やオープンソースのフレームワークを使った軽量の永続性オブジェクトが使われることが多くなった。そのようなサードパーティの永続性フレームワークの機能を集約したのが Java Persistence API であり、[Hibernate](../Page/Hibernate.md "wikilink") や [TopLink](https://ja.wikipedia.org/wiki/TopLink "wikilink") のようなプロジェクトも現在では Java Persistence API を実装している。

## 関連項目

  - 仕様
      - [Java Data Objects](../Page/Java_Data_Objects.md "wikilink")
  - 実装
      - [DataNucleus](https://ja.wikipedia.org/wiki/DataNucleus "wikilink")
      - [GlassFish](../Page/GlassFish.md "wikilink")
      - [Hibernate](../Page/Hibernate.md "wikilink")

## 外部リンク

  - 一般的情報
      - [Sun's Persistence page](http://java.sun.com/javaee/technologies/entapps/persistence.jsp)
      - [GlassFish's Persistence page](https://glassfish.dev.java.net/javaee5/persistence/)
      - [The Java Community Process(SM) Program - JSRs: Java Specification Requests - detail JSR\# 317](http://www.jcp.org/en/jsr/detail?id=317)
      - [Documentation for the final version of the EJB3 spec (called JSR220)](http://jcp.org/aboutJava/communityprocess/final/jsr220/index.html)
      - [Nabble JPA Forum](http://www.nabble.com/JPA-f27109.html)
  - ドキュメンテーション
      - [Persistence in the Java EE 5 Tutorial](http://java.sun.com/javaee/5/docs/tutorial/doc/?wp406141&JavaEETutorialPartFour.html#wp996871)
      - [Sun's Persistence FAQ](http://java.sun.com/javaee/overview/faq/persistence.jsp)
      - [Java Persistence API Javadoc](https://java.sun.com/javaee/5/docs/api/javax/persistence/package-summary.html)
      - [Getting started with Java Persistence API 1.0](https://www.sdn.sap.com/irj/sdn/go/portal/prtroot/docs/library/uuid/40ff8a3d-065a-2910-2f84-a222e03d1f43)
  - 実装
      - [Amber](http://www.caucho.com/resin-3.1/doc/amber.xtp) - Resinの一部
      - [Apache OpenJPA](http://openjpa.apache.org/)
      - [DataNucleus](http://www.datanucleus.org/)
      - [GlassFish](https://glassfish.dev.java.net)
      - [Hibernate](http://www.hibernate.org/)
      - Oracle
          - [EclipseLink](http://www.eclipse.org/eclipselink/)
          - [Oracle TopLink](http://www.oracle.com/technology/products/ias/toplink/index.html)
          - [Oracle Kodo](http://download.oracle.com/docs/cd/E13189_01/kodo/docs41/index.html)
      - [SAP Netweaver Application Server](http://www.sap.com/platform/netweaver/components/applicationserver/index.epx)
      - [SimpleJPA](http://code.google.com/p/simplejpa/) - [Amazon SimpleDB](https://ja.wikipedia.org/wiki/Amazon_SimpleDB "wikilink")
  - 記事
      - [Master the New Persistence Paradigm with JPA](http://www.devx.com/Java/Article/33650)
      - [Persistence Pays Offs: Advanced Mapping with JPA](http://www.devx.com/Java/Article/33906)

[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:Java_enterprise_platform](https://ja.wikipedia.org/wiki/Category:Java_enterprise_platform "wikilink") [Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink") [Category:永続性](https://ja.wikipedia.org/wiki/Category:永続性 "wikilink")