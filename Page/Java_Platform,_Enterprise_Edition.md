> この記事は[Java Platform, Enterprise Edition](https://ja.wikipedia.org/wiki/Java_Platform,_Enterprise_Edition)から翻訳されています。


**Java Platform, Enterprise Edition** (**Java EE**) は、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で実装されたアプリケーションサーバーの標準規格及びそのAPIを定めたもの。[Java Platform, Standard Edition](../Page/Java_Platform,_Standard_Edition.md "wikilink") (Java SE) の拡張機能の形で提供される。

## 概要

[thumbにおけるJava](https://ja.wikipedia.org/wiki/ファイル:Java_Platforms.PNG "wikilink") EEの位置づけ。Java EEは[Java SEの拡張機能として位置づけられている](../Page/Java_Platform,_Standard_Edition.md "wikilink")。\]\]

[1999年](../Page/1999年.md "wikilink")に初版である1.2が発表された。主に小規模〜大規模サーバーシステムの標準仕様として、動的HTTPサーバー機能、自動トランザクション管理機能、データベース接続機能、メッセージング機能、各種通信プロトコル機能がAPIとして定められている。大規模システムにおける[多層システムの構築も想定されており](../Page/多層アーキテクチャ.md "wikilink")、XAプロトコルを用いた分散トランザクションにも対応している。

過去のリリースに伴い名称が変化しており、[2017年](../Page/2017年.md "wikilink")現在のバージョンはJava Platform, Enterprise Edition 8 (Java EE 8) と命名されているが、Java EE 5より過去のバージョンはJava 2 Platform, Enterprise Edition (J2EE) と命名されていた。

Java EE自体は仕様であるため、各社・各組織がライセンスを受け実装している。オープンソースのものからプロプライエタリなもの、無償のものや有償のものなど選択肢が多い。

Java EEの権利は[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")を買収した[オラクルが保有してきたが](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")、同社は2017年にJava EEを[Eclipse Foundationに寄贈して](../Page/Eclipse_Foundation.md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")化をすることを発表。Java EEの商標については引き続きオラクルが保有するため、Java EE 9以後は**Jakarta EE**の名で開発が進められる事が発表された。\[1\]

## 歴史

Java EEは[1999年](../Page/1999年.md "wikilink")の登場以後、数年おきに新しいバージョンが策定されている。

  - Java 2 Platform, Enterprise Edition 1.2
    最初のJ2EEの仕様。[Sun Microsystemsが開発をし](../Page/サン・マイクロシステムズ.md "wikilink")、[1999年](../Page/1999年.md "wikilink")12月12日にリリースされた。1.2当初は以下のような技術から構成されていた。
    [JDBC](../Page/JDBC.md "wikilink") 2.0, [JNDI](../Page/Java_Naming_and_Directory_Interface.md "wikilink") 1.2, [RMI-IIOP](../Page/RMI-IIOP.md "wikilink") 1.0, [Servlet](../Page/Java_Servlet.md "wikilink") 2.2, [JSP](../Page/JavaServer_Pages.md "wikilink") 1.1, [EJB](../Page/Enterprise_JavaBeans.md "wikilink") 1.1, [JMS](../Page/Java_Message_Service.md "wikilink") 1.0, [JTA](../Page/Java_Transaction_API.md "wikilink") 1.0,  1.1,  1.0

<!-- end list -->

  - Java 2 Platform, Enterprise Edition 1.3
    JSR 58 として[2001年](../Page/2001年.md "wikilink")9月24日にリリースされた。仕様検討は、[Java Community Processの元で行われた](../Page/Java_Community_Process.md "wikilink")。[ベータ版](../Page/ベータ版.md "wikilink")が2001年4月にSunによってリリースされている。1.3では新たにJSPの標準カスタムタグライブラリである[JSTLや](https://ja.wikipedia.org/wiki/JavaServer_Pages#JSTL "wikilink")、[JAXP](../Page/Java_API_for_XML_Processing.md "wikilink"), , といった技術が追加された。またEJBが2.0へと更新され、JNDIは[J2SEへの移行により取り除かれた](../Page/Java_Platform,_Standard_Edition.md "wikilink")。

<!-- end list -->

  - Java 2 Platform, Enterprise Edition 1.4
    JSR 151 として[2003年](../Page/2003年.md "wikilink")11月24日にリリースされた。ベータ版は[2002年](../Page/2002年.md "wikilink")12月にSunによってリリースされている。SOAPによるWebサービスを実現するJAXP, JAXR, JAX-RPCが導入された他は、小改良に留まっている。

<!-- end list -->

  - Java Platform, Enterprise Edition 5
    JSR 244として[2006年](../Page/2006年.md "wikilink")5月11日にリリースされた。5からは名称・バージョン体系が改められており、またJ2SE 5.0で導入された[アノテーション](../Page/アノテーション.md "wikilink")を使った仕組みが導入されるなど、仕様自体も大きく変更された。中でもEJBは[DIや](../Page/依存性の注入.md "wikilink")[POJOの概念を取り入れ仕様を全面的に見直した](../Page/Plain_Old_Java_Object.md "wikilink")3.0へと更新されており、さらにEJBから派生する形で永続化フレームワークである[JPAも追加されている](../Page/Java_Persistence_API.md "wikilink")。また、新たに[Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")である[JSFが採用された](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink")。

<!-- end list -->

  - Java Platform, Enterprise Edition 6
    JSR 316として[2009年](../Page/2009年.md "wikilink")12月10日にリリースされた。6では新たにDIを実現するCDIや、バリデーションを提供する[Bean Validationといった技術が追加されている](https://ja.wikipedia.org/wiki/Bean_Validation "wikilink")。また、[JSFが](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink")2.0となり大幅に仕様が変更となっている。

<!-- end list -->

  - Java Platform, Enterprise Edition 7
    JSR 342として[2013年](../Page/2013年.md "wikilink")5月28日にリリースされた。7ではJSFが2.2となりCDIに準拠した上で[HTML5](../Page/HTML5.md "wikilink")にも対応した。[WebSocket](https://ja.wikipedia.org/wiki/WebSocket "wikilink")や[バッチ処理](../Page/バッチ処理.md "wikilink")に関する仕様が追加されている。Java EE 7は以下のような技術から構成されている。
    [WebSocket](https://ja.wikipedia.org/wiki/WebSocket "wikilink"), [JSON](../Page/JavaScript_Object_Notation.md "wikilink") Processing, [Servlet](../Page/Java_Servlet.md "wikilink") 3.1, [JSF](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink") 2.2, [EL](https://ja.wikipedia.org/wiki/JavaServer_Pages#EL式 "wikilink") 3.0, [JSP](../Page/JavaServer_Pages.md "wikilink") 2.3, [JSTL](https://ja.wikipedia.org/wiki/JavaServer_Pages#JSTL "wikilink") 1.2, [Batch Applications](../Page/バッチ処理.md "wikilink"), Concurrency Utilities, CDI 1.1, [DI](../Page/依存性の注入.md "wikilink") 1.0, [Bean Validation](https://ja.wikipedia.org/wiki/Bean_Validation "wikilink") 1.1, [EJB](../Page/Enterprise_JavaBeans.md "wikilink") 3.2, Interceptors 1.2,  1.7, [JPA](../Page/Java_Persistence_API.md "wikilink") 2.1,  1.2, [JMS](../Page/Java_Message_Service.md "wikilink") 2.0, [JTA](../Page/Java_Transaction_API.md "wikilink") 1.2,  1.5, [JAX-RS](https://ja.wikipedia.org/wiki/JAX-RS "wikilink") 2.0, Enterprise Web Services 1.3,  2.2, , [JAX-RPC](https://ja.wikipedia.org/wiki/JAX-RPC "wikilink") 1.1,  1.3,  1.0, JASPIC 1.1, Java ACC 1.5, Java EE Application Deployment 1.2,  1.1, Debugging Support for Other Languages 1.0, [JAXB](../Page/Java_Architecture_for_XML_Binding.md "wikilink") 2.2, [JAXP](../Page/Java_API_for_XML_Processing.md "wikilink") 1.3, [JDBC](../Page/JDBC.md "wikilink") 4.0, [JMX](../Page/Java_Management_Extensions.md "wikilink") 2.0,  1.1, [StAX](../Page/Streaming_API_for_XML.md "wikilink")

<!-- end list -->

  - Java Platform, Enterprise Edition 8
    JSR 366として[2017年](../Page/2017年.md "wikilink")9月21日にリリースされた。8ではServletが[HTTP/2](https://ja.wikipedia.org/wiki/HTTP/2 "wikilink")をサポートした4.0に更新されている。全体としては7の小改良に留まっているものの、JSF 2.3によるHTML処理が大きく改良されている。

## 主なAPI

Java EE APIは Java SE APIを元に機能拡張された様々な技術を包含している。

  - [Java EE 8 Specification APIs](https://javaee.github.io/javaee-spec/javadocs/)
  - [Java EE 7 Specification APIs](http://docs.oracle.com/javaee/7/api)
  - [Java EE 6 API Specification](http://docs.oracle.com/javaee/6/api)

###

[Servlet](../Page/Java_Servlet.md "wikilink")[パッケージでは](../Page/パッケージ_\(Java\).md "wikilink")、主に[HTTPリクエストのためのAPIが定義されている](../Page/Hypertext_Transfer_Protocol.md "wikilink")。また[JavaServer Pages](../Page/JavaServer_Pages.md "wikilink") (JSP) に関するAPIも含まれる。

###

WebSocketパッケージでは、[WebSocket](https://ja.wikipedia.org/wiki/WebSocket "wikilink")の通信に関するAPIが定義されている。

###

Facesパッケージでは、 [Java Server Faces](https://ja.wikipedia.org/wiki/Java_Server_Faces "wikilink") (JSF) に関するAPIが定義されている。JSFはコンポーネントによるUI構築技術である。

###

ELパッケージでは、Java EEの[EL式に関する](https://ja.wikipedia.org/wiki/JavaServer_Pages#EL式 "wikilink")[クラスと](../Page/クラス_\(コンピュータ\).md "wikilink")[インターフェースが定義されている](../Page/インタフェース_\(情報技術\).md "wikilink")。EL式はJSPやJSFを作成するWebアプリケーション開発者のためにデザインされた簡単な構文である。主にJSFにおいてコンポーネントに管理beanを結びつけるために用いられるが、仕様自体は独立しており、それ以外の部分でも使用可能である。

###

Injectパッケージでは、[Contexts and Dependency Injection](http://jcp.org/en/jsr/detail?id=299) (CDI) APIのためのインジェクション[アノテーション](../Page/アノテーション.md "wikilink")が定義されている。CDIは[依存性の注入](../Page/依存性の注入.md "wikilink") (DI) に関する仕様である。

###

Contextパッケージでは、Contexts and Dependency Injection (CDI) APIのためのコンテキストアノテーションとインタフェースが定義されている。

###

[Enterprise JavaBeans](../Page/Enterprise_JavaBeans.md "wikilink") (EJB) パッケージでは、EJBコンテナがサポートする[トランザクション処理](../Page/トランザクション処理.md "wikilink") ([JTA](https://ja.wikipedia.org/wiki/JTA "wikilink"))、[RPC](../Page/遠隔手続き呼出し.md "wikilink")（[RMIまたは](../Page/Java_Remote_Method_Invocation.md "wikilink")[RMI-IIOP](../Page/RMI-IIOP.md "wikilink")）、[並行性制御](../Page/並行性制御.md "wikilink")、[依存性の注入](../Page/依存性の注入.md "wikilink") (DI)、ビジネスオブジェクトのための[アクセス制御](../Page/アクセス制御.md "wikilink")といった軽量APIが定義されている。またこのパッケージは、エンタープライズBeanとそのクライアント間、エンタープライズBeanとEJBコンテナ間の取り決めを定義したクラスとインタフェースも含む。

###

Validationパッケージでは、[Bean Validation](https://ja.wikipedia.org/wiki/Bean_Validation "wikilink") APIのためのアノテーションとインタフェースが定義されている。Bean Validationはbean（例えばJPAのモデルクラス）に対する統一されたバリデーション（値の検証）手法を提供する。Java EEの各要素では、[JPAが永続化層におけるバリデーションに](../Page/Java_Persistence_API.md "wikilink")、[JSFがビュー層におけるバリデーションにまた関与する](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink")。

###

Persistenceパッケージには、永続化プロバイダと管理クラス、それに[Java Persistence API](../Page/Java_Persistence_API.md "wikilink") (JPA) クライアントの間の取り決めを定義したクラスとインタフェースが含まれている。

###

Transactionパッケージでは、Java EEの[トランザクション処理](../Page/トランザクション処理.md "wikilink")を担う[Java Transaction API](../Page/Java_Transaction_API.md "wikilink") (JTA) のインタフェースとアノテーションを含むAPIが定義されている。これらのAPIは低レベルAPIが抽象化されたものであり、通常のアプリケーション開発者がJava EEを用いて開発する場合は、EJBのより高レベルのトランザクション管理を用いたり、このAPIのアノテーションとCDIの管理Beanとを組み合わせて使用することが想定されている。

###

Messageパッケージでは、Java Authentication SPI (JASPIC) のインタフェースやクラスを含むAPIが定義されている。JASPICはセキュアなJava EEアプリケーションを構築するための仕様である。

###

Concurrentパッケージでは、Java EEプラットフォーム標準の管理されたスレッドプールと連携する、並行処理に関するインタフェースが定義されている。

###

JMSパッケージでは、[Java Message Service](../Page/Java_Message_Service.md "wikilink") (JMS) APIが定義されている。JMSはJavaプログラムにエンタープライズメッセージの生成、送信、受信、読込のための手法を提供する。

###

BatchのAPIパッケージでは、Java EEの[バッチ処理](../Page/バッチ処理.md "wikilink")のためのAPIが定義されている。バッチ処理APIは、大容量のデータを扱う長時間に亘るバックグラウンドタスクや、定期的に実行されるタスクのための手法を提供する。

###

Resourceパッケージでは、 (JCA) APIが定義されている。JCAは[Enterprise application integration](../Page/Enterprise_application_integration.md "wikilink") (EAI) の一部であるアプリケーションサーバーや企業情報システム (EIS) の相互接続を実現するための技術である。このAPIはベンダーのための低レベルAPIであり、通常のアプリケーション開発者をターゲットとしてはいない。

## Java EEの実装

Java EEの機能を用いた[アプリケーションを動作させるには](../Page/アプリケーションソフトウェア.md "wikilink")、Java EEの仕様を実装した実行環境や[ライブラリ](../Page/ライブラリ.md "wikilink")が必要である。Java EE SDKには、Java EEに準拠した[オープンソース](../Page/オープンソース.md "wikilink")の[アプリケーションサーバ](../Page/アプリケーションサーバ.md "wikilink")である[GlassFish Open Source Editionが同梱されている](https://ja.wikipedia.org/wiki/GlassFish "wikilink")。GlassFish 4.0はJava EE 7の[参照実装である](../Page/リファレンス実装.md "wikilink")。[NetBeans](../Page/NetBeans.md "wikilink")や[EclipseといったJava開発ツールの多くもJava](../Page/Eclipse_\(統合開発環境\).md "wikilink") EEに対応している。

以下に、Java EEに準拠した主なアプリケーションサーバを示す。表のバージョン番号は、該当するJava EE仕様に対応したバージョンを表している。

<table>
<thead>
<tr class="header">
<th><p><a href="../Page/アプリケーションサーバ.md" title="wikilink">アプリケーションサーバ</a></p></th>
<th><p>Java EE 8準拠</p></th>
<th><p>Java EE 7準拠</p></th>
<th><p>Java EE 6準拠<br />
(Full Profile)</p></th>
<th><p>Java EE 6準拠<br />
(Web Profile)</p></th>
<th><p>Java EE 5準拠</p></th>
<th><p>J2EE 1.4準拠</p></th>
<th><p><a href="../Page/ライセンス.md" title="wikilink">ライセンス</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/GlassFish" title="wikilink">GlassFish</a> server Open Source Edition</p></td>
<td><p>v5.x</p></td>
<td><p>v4.x [2]</p></td>
<td><p>v3.x [3]</p></td>
<td><p>v3.x Web Profile</p></td>
<td><p>v2.1.x[4]</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://www.payara.fish/">Payara Server</a></p></td>
<td><p>v5.x</p></td>
<td><p>4.x</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Oracle GlassFish Server</p></td>
<td></td>
<td></td>
<td><p>v3[5]</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/GlassFish" title="wikilink">Sun Java System Application Server</a> v9.0</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/GlassFish" title="wikilink">Sun Java System Application Server</a> v8.2</p></td>
<td><p><br />
（OSS版を元とする）</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>v12.2.x</p></td>
<td><p>v12.1.x[6]</p></td>
<td></td>
<td><p>v10.3.5.0</p></td>
<td><p>v9</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/JBoss.md" title="wikilink">WildFly</a></p></td>
<td><p>v14.x[7]</p></td>
<td><p>v12,x, v11.x, v10.x, v9.x, v8.x[8][9][10], v7.1[11]</p></td>
<td><p>v6.0 <a href="http://www.jboss.org/jbossas">1</a>, v7.0 <a href="http://www.jboss.org/as7">2</a></p></td>
<td></td>
<td><p>v5.1[12][13]</p></td>
<td><p>v4.x</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/JBoss.md" title="wikilink">JBoss Enterprise Application Platform</a></p></td>
<td><p>v7.2 [14]</p></td>
<td><p>v7.0</p></td>
<td><p>v6.0 [15]</p></td>
<td></td>
<td><p>v5</p></td>
<td></td>
<td><p><br />
（WildFlyの商用版）</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/WebSphere_Application_Server.md" title="wikilink">IBM WebSphere Application Server</a></p></td>
<td></td>
<td></td>
<td><p>v8[16]</p></td>
<td></td>
<td><p>v7</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://openliberty.io/">Open Liberty</a></p></td>
<td><p>v18.0.0.2[17]</p></td>
<td><p>v18.x, v17.x, IBM WAS Liberty v8.5.5.6 [18][19]</p></td>
<td><p>IBM WAS Liberty v8.5.5 [20]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/WebSphere_Application_Server.md" title="wikilink">IBM WebSphere Application Server Community Edition</a></p></td>
<td></td>
<td></td>
<td><p>v3.0[21]</p></td>
<td></td>
<td><p>v2.1</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Apache_Geronimo.md" title="wikilink">Apache Geronimo</a></p></td>
<td></td>
<td></td>
<td><p>v3.0 <a href="http://geronimo.apache.org/">3</a>[22]</p></td>
<td></td>
<td><p>v2.0</p></td>
<td><p>v1.0</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>JEUS</p></td>
<td></td>
<td><p>v8 [23][24][25]</p></td>
<td><p>v7[26][27]</p></td>
<td></td>
<td><p>v6</p></td>
<td><p>v5</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/富士通.md" title="wikilink">富士通</a> <a href="../Page/Interstage.md" title="wikilink">Interstage Application Server</a>[28]</p></td>
<td></td>
<td></td>
<td><p>v1[29]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/日本電気.md" title="wikilink">NEC</a> <a href="../Page/WebOTX.md" title="wikilink">WebOTX</a></p></td>
<td></td>
<td></td>
<td><p>[30]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p></p></td>
<td></td>
<td></td>
<td></td>
<td><p>v4.0.[31]</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>[32][33]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/OW2_Consortium.md" title="wikilink">OW2</a> <a href="../Page/JOnAS.md" title="wikilink">JOnAS</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>v5.3 rc1 [34]</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/SAP_NetWeaver" title="wikilink">SAP NetWeaver</a></p></td>
<td></td>
<td></td>
<td></td>
<td><p>v2.x [35]</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Oracle_iPlanet_Web_Server" title="wikilink">Oracle iPlanet Web Server</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>Sun Java System Web Server</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Sybase.md" title="wikilink">Sybase</a> Enterprise Application Server [36]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 例

以下に、Java EE 7の様々な技術を組み合わせて作成した、ユーザーの登録を行うWeb入力画面のサンプルを示す。

Java EEには、[サーブレットに](../Page/Java_Servlet.md "wikilink")[JSP](../Page/JavaServer_Pages.md "wikilink")、また[JSFと](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink")[Faceletsといった](https://ja.wikipedia.org/wiki/JavaServer_Faces#Facelets "wikilink")、Web UIを作ることが可能ないくつかの技術が存在する。以下はJSFとFaceletsを用いた例である。コード上では明示されていないが、入力コンポーネントでは入力値の検証に[Bean Validationを使用している](https://ja.wikipedia.org/wiki/Bean_Validation "wikilink")。

``` xml
<html ns="http://www.w3.org/1999/xhtml"
      xmlns:h="http://xmlns.jcp.org/jsf/html" xmlns:f="http://xmlns.jcp.org/jsf/core">

    <f:metadata>
        <f:viewParam name="user_id" value="#{userEdit.user}" converter="#{userConvertor}" />
    </f:metadata>

    <h:body>

        <h:messages />

        <h:form>
            <h:panelGrid columns="2">
                <h:outputLabel for="firstName" value="First name" />
                <h:inputText id="firstName" value="#{userEdit.user.firstName}" label="First name" />

                <h:outputLabel for="lastName" value="Last name" />
                <h:inputText id="lastName" value="#{userEdit.user.lastName}" label="Last name" />

                <h:commandButton action="#{userEdit.saveUser}" value="Save" />
            </h:panelGrid>
        </h:form>

    </h:body>
</html>
```

### バッキングBeanの例

Java EEでは、ビューの処理の実装にバッキングBean（画面の背後で処理するBean、管理Beanとも）と呼ばれる仕組みを用いる。以下はCDIと[EJBを用いたバッキングBeanの例である](../Page/Enterprise_JavaBeans.md "wikilink")。

``` java
@Named
@ViewScoped
public class UserEdit {

    private User user;

    @Inject
    private UserDAO userDAO;

    public String saveUser() {
        userDAO.save(this.user);
        addFlashMessage("User " + this.user.getId() + " saved");

        return "users.xhtml?faces-redirect=true";
    }

    public void setUser(User user) {
        this.user = user;
    }

    public User getUser() {
        return user;
    }
}
```

### DAOの例

Java EEでは、[ビジネスロジック](../Page/ビジネスロジック.md "wikilink")の実装のために[EJBが用意されている](../Page/Enterprise_JavaBeans.md "wikilink")。データの永続化では[JDBC](../Page/JDBC.md "wikilink")や[JPAが使用できる](../Page/Java_Persistence_API.md "wikilink")。以下はEJBとJPAを用いた[Data Access Object](../Page/Data_Access_Object.md "wikilink") (DAO) の例である。コード上では明示されていないが、EJBではトランザクション管理に[JTAが使用される](../Page/Java_Transaction_API.md "wikilink")。

``` java
@Stateless
public class UserDAO {

    @PersistenceContext
    private EntityManager entityManager;

    public void save(User user) {
        entityManager.persist(user);
    }

    public void update(User user) {
        entityManager.merge(user);
    }

    public List<User> getAll() {
        return entityManager.createNamedQuery("User.getAll", User.class)
                            .getResultList();
    }

}
```

### エンティティの例

Java EEでは、[エンティティ](https://ja.wikipedia.org/wiki/エンティティ "wikilink")/モデルクラスのために[JPAが用意されており](../Page/Java_Persistence_API.md "wikilink")、またバリデーション（値の検証）では[Bean Validationが使用できる](https://ja.wikipedia.org/wiki/Bean_Validation "wikilink")。以下は両者を用いた例である。

``` java
@Entity
public class User {

    @Id
    @GeneratedValue(strategy = IDENTITY)
    private Integer id;

    @Size(min = 2, message="First name too short")
    private String firstName;

    @Size(min = 2, message="Last name too short")
    private String lastName;

    public Integer getId() {
        return id;
    }

    public void setId(Integer id) {
        this.id = id;
    }

    public String getFirstName() {
        return firstName;
    }

    public void setFirstName(String firstName) {
        this.firstName = firstName;
    }

    public String getLastName() {
        return lastName;
    }

    public void setLastName(String lastName) {
        this.lastName = lastName;
    }

}
```

## 脚注

## 関連項目

  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink") 、[Java\#Javaのエディション](https://ja.wikipedia.org/wiki/Java#Javaのエディション "wikilink")（Java SE、Java EE、Java MEなど）、[Java\#バージョン履歴](https://ja.wikipedia.org/wiki/Java#バージョン履歴 "wikilink")（JDK 1.0からJ2SE 1.2、Java SE 8、Java SE 9など）
  - [Java Platform, Standard Edition](../Page/Java_Platform,_Standard_Edition.md "wikilink") (Java SE) - Java の汎用的なエディション
  - [Java Platform, Micro Edition](../Page/Java_Platform,_Micro_Edition.md "wikilink") (Java ME) - Java の[組み込みシステム](../Page/組み込みシステム.md "wikilink")向けエディション
  - [EAR](https://ja.wikipedia.org/wiki/EAR "wikilink") - Java EEアプリーケーションのパッケージ形式

## 外部リンク

  - [Oracle - Java EE](http://www.oracle.com/technetwork/jp/java/javaee/overview/)
  - [Jakarta EE](https://jakarta.ee/)

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:ウェブアプリケーション](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーション "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:Java_enterprise_platform](https://ja.wikipedia.org/wiki/Category:Java_enterprise_platform "wikilink") [Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.
2.  <http://www.oracle.com/technetwork/java/javaee/community/testedconfiguration-glassfish4-0-1957654.html>
3.  <https://glassfish.dev.java.net/public/comparing_v2_and_v3.html>
4.
5.
6.  <http://wcc.on24.com/event/37/57/27/rt/1/documents/player_docanchr_3/weblogic12c_launch_tech_webinar_v8.pdf>
7.  <http://wildfly.org/news/2018/08/30/WildFly14-Final-Released/>
8.  wildfly.org/about/\#compliant
9.  <https://issues.jboss.org/browse/WFLY-469>
10. <http://lists.jboss.org/pipermail/wildfly-dev/2013-May/000062.html>
11.
12. [Java EE Compatibility](http://java.sun.com/javaee/overview/compatibility.jsp)
13. [JBoss AS is now EE5 certified](http://sacha.labourey.com/2008/09/15/jboss-as-is-now-ee5-certified/)
14.
15.
16.
17.
18. <http://oracle.com/technetwork/java/javaee/overview/waslibertyprofile8556-2587134.html>
19. <https://developer.ibm.com/wasdev/blog/2015/06/25/java-ee-7-has-landed-in-was-liberty>
20. <http://www.oracle.com/technetwork/java/javaee/community/ibm-javaee6-web-tested-configs-1961333.html>
21.
22.
23. <http://www.oracle.com/technetwork/java/javaee/community/tmax-jeus-8-tested-configuration-1995477.html>
24. <http://tmaxsoft.com/product/jeus/certification>
25. <https://blogs.oracle.com/theaquarium/entry/tmaxsoft_jeus_8_now_java>
26.
27.
28. [Fujitsu Interstage Application Server powered by Windows Azure](http://www.fujitsu.com/global/services/software/windows-azure)
29.
30. <http://www.oracle.com/technetwork/java/javaee/community/nec-webotx-v9x-certification-2002719.html>
31. <http://www.caucho.com/articles/Caucho_Web%20Profile%20JavaEE6_whitepaper_byRR.pdf>
32.
33.
34. <http://jonas.ow2.org/xwiki/bin/view/Blog/JOnAS+530+RC1+released>
35. <https://blogs.oracle.com/theaquarium/entry/sap_netweaver_cloud_java_ee>
36. [EAServer](http://www.sybase.com/products/modelingdevelopment/easerver)