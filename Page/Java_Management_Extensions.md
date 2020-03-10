> この記事は[Java Management Extensions](https://ja.wikipedia.org/wiki/Java_Management_Extensions)から翻訳されています。


**Java Management Extensions**（**JMX**）は、[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")/システムオブジェクト/デバイス（[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")など）/サービス指向ネットワークなどの監視・管理のためのツールを提供する[Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")技術の一種。これらのリソースは MBean（[Managed Bean](https://ja.wikipedia.org/wiki/Managed_Bean "wikilink")）と呼ばれるオブジェクトで表現される。この[APIの面白い特徴として](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、[クラス群を動的にロードしてインスタンス化できる](../Page/クラス_\(コンピュータ\).md "wikilink")。

JMX 1.0、1.1、1.2 は [Java Community Process](https://ja.wikipedia.org/wiki/Java_Community_Process "wikilink") の [JSR](https://ja.wikipedia.org/wiki/Java_Community_Process "wikilink") [3](http://www.jcp.org/en/jsr/detail?id=3) で定義された。JMX 2.0 が JSR [255](http://www.jcp.org/en/jsr/detail?id=255) として開発されてきたが、2016年で中止された\[1\]。遠隔管理・監視のための JMX Remote API 1.0 は JSR [160](http://www.jcp.org/en/jsr/detail?id=160) で規定された。Webサービスのための JMX Remote API 拡張は JSR [262](http://www.jcp.org/en/jsr/detail?id=262) で開発中である。

当初、[J2EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink") に受け入れられたが、JMX は [Java SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") のバージョン5.0以降にも組み込まれている。なお「JMX」 は[オラクルの商標である](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")。

## Managed Bean

**Managed Bean**（しばしば略してMBeanと呼ぶ）は、[JavaBeans](../Page/JavaBeans.md "wikilink")の一種であり、[依存性の注入](https://ja.wikipedia.org/wiki/依存性の注入 "wikilink")により作られている。MBeanは特にJava Management Extensions技術で用いられている。しかし、Java EE 6仕様ではmanaged beanにより詳細な意味を与えている。

MBeanは[Java Virtual Machine上で走るリソース](https://ja.wikipedia.org/wiki/Java_Virtual_Machine "wikilink")（アプリケーションやJava EE技術サービス（トランザクション・モニタやJDBCドライバなど））との連絡窓口の役割を果たす。MBeanは、関心のある統計数値（パフォーマンス、リソース使用量、問題など）を収集すること（プル）、アプリケーションの設定値を取得または設定すること（プッシュ/プル）、および障害や状態変化などのイベントを通知すること（プッシュ）に使える。

Java EE 6仕様では、managed beanはJavaクラスで実装されたBeanであるとしており、beanクラスと呼ばれる。他の何らかのJava EE 技術仕様（たとえば[JavaServer Faces技術仕様](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink")）でmanaged beanであると定義されたトップレベルJavaクラス、あるいは次の条件をすべて満たすトップレベルJavaクラスであれば、それはmanaged beanである。

1.  非staticな内部クラス(inner class)ではないこと
2.  具象クラスであるか、または@Decoratorアノーテーションされていること
3.  EJBコンポーネント定義アノーテーションでアノーテーションされていないか、またはejb-jar.xml内でEJB beanクラスとして宣言されていること

アノーテーションのような特殊な宣言は、managed beanを定義するために必須なものではない。

MBeanはその内部的な（属性の）変化を`javax.management.NotificationEmitter`を実装することによりMBeanServerに通知できる。MBeanの変化に関心のあるアプリケーションは、リスナー (`javax.management.NotificationListener`) をMBeanServerに登録する。 JMX はリスナー群が全ての通知を受け取れることは保証しないことに留意されたい。

## アーキテクチャ

JMX は以下の3階層アーキテクチャに基づいている:

  - *Probe* レベル*（Instrumentation*レベルとも呼ぶ） : プローブ（MBean）によりリソースの状態を監視・測定する。
  - *Agent* レベル （MBeanServer とも呼ぶ）: JMX の中核である。MBean とアプリケーションの仲介を行う。
  - *Remote Management* レベル : 遠隔のアプリケーションが Connector や Adaptor を通して MBeanServer にアクセスできるようにする。Connector は各種通信フレームワーク（[Java RMI](https://ja.wikipedia.org/wiki/Java_Remote_Method_Invocation "wikilink")、[IIOP](https://ja.wikipedia.org/wiki/IIOP "wikilink")、[JMS](../Page/Java_Message_Service.md "wikilink")、[WS-\*など](https://ja.wikipedia.org/wiki/Webサービス "wikilink")）を使って MBeanServer API への完全なリモートアクセスを提供する。Adaptor はそのAPIを他のプロトコル（[SNMPなど](../Page/Simple_Network_Management_Protocol.md "wikilink")）に接続したり、WebベースのGUI（[HTML](../Page/HyperText_Markup_Language.md "wikilink")/[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[WML](https://ja.wikipedia.org/wiki/Wireless_Markup_Language "wikilink")/[HTTPなど](../Page/Hypertext_Transfer_Protocol.md "wikilink")）に接続したりする。

アプリケーションとしては、汎用のコンソール（[JConsole](http://java.sun.com/developer/technicalArticles/J2SE/jconsole.html) や [MC4J](http://mc4j.org/confluence/display/mc4j/Home) など）でもよいし、ドメイン固有の（監視）アプリケーションでもよい。

## サポート

JMX のサポート状況はベンダーによって様々である:

  - Java [アプリケーションサーバ](https://ja.wikipedia.org/wiki/アプリケーションサーバ "wikilink")（[JBoss](https://ja.wikipedia.org/wiki/JBoss "wikilink")、[JOnAS](https://ja.wikipedia.org/wiki/JOnAS "wikilink")、[WebSphere Application Server](https://ja.wikipedia.org/wiki/WebSphere_Application_Server "wikilink")、[BEA WebLogic Server](https://ja.wikipedia.org/wiki/BEA_WebLogic_Server "wikilink")、[Sun Java System Application Serverなど](https://ja.wikipedia.org/wiki/Sun_Java_System_Application_Server "wikilink")）は JMX をサポートしている。
  - [システム管理](https://ja.wikipedia.org/wiki/システム管理 "wikilink")ツールとして JMX をサポートしているものには [HP OpenView](https://ja.wikipedia.org/wiki/OpenView "wikilink") などがある。
  - [MX4J](http://mx4j.sourceforge.net/) はオープンソースの JMX 実装である。
  - [JManage](http://www.jmanage.org) はオープンソースの JMX コンソールであり、Webインタフェースとコマンド行インタフェースがある。
  - [MC4J](http://mc4j.org/) はオープンソースのJMXコンソールである。

## 脚注

## 関連項目

  - [Java Beans](https://ja.wikipedia.org/wiki/Java_Beans "wikilink")
  - [Jini](../Page/Jini.md "wikilink")
  - [OSGi](../Page/OSGi.md "wikilink")
  - [Simple Network Management Protocol](../Page/Simple_Network_Management_Protocol.md "wikilink")
  - [ネットワーク管理](../Page/ネットワーク管理.md "wikilink")
  - [メタクラス](https://ja.wikipedia.org/wiki/メタクラス "wikilink")
  - [メタプログラミング](https://ja.wikipedia.org/wiki/メタプログラミング "wikilink")
  - [リフレクション](https://ja.wikipedia.org/wiki/リフレクション_\(情報工学\) "wikilink")

## 参考文献

  - J. Steven Perry: *Java Management Extensions*, O'Reilly, ISBN 0-596-00245-9
  - Marc Fleury, Juha Lindfors: *JMX: Managing J2EE with Java Management Extensions*, Sams Publishing, ISBN 0-672-32288-9
  - Jeff Hanson: *Connecting JMX Clients and Servers: Understanding the Java Management Extensions*, APress L. P., ISBN 1-59059-101-1
  - Benjamin G Sullins, *Mark B Whipple : JMX in Action: You will also get your first JMX application up and running*, Manning Publications Co. 2002, ISBN 1-930110-56-1

## 外部リンク

  - [JMX on java.sun.com](http://java.sun.com/products/JavaManagement/)
  - [JMX at JBoss.com](http://wiki.jboss.org/wiki/Wiki.jsp?page=JMXConsole)
  - [JSR 255](http://jcp.org/en/jsr/detail?id=255) (JMX 2.0)
  - [JSR 3](http://jcp.org/en/jsr/detail?id=3) (JMX 1.0, 1.1, and 1.2)
  - [JMX/JBoss](http://jboss.org/index.html?module=html&op=userdisplay&id=developers/projects/jboss/jbossmx) - [マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")設計
  - [JMXを使用する監視と管理](http://java.sun.com/j2se/1.5.0/ja/docs/ja/guide/management/agent.html)
  - [J2SE 5.0 虎の穴 JMX 基礎編](http://www.javainthebox.net/laboratory/J2SE1.5/MonitoringAndManagement/JMX/JMX1.html)

[Category:Java_enterprise_platform](https://ja.wikipedia.org/wiki/Category:Java_enterprise_platform "wikilink") [Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink") [Category:ネットワーク管理](https://ja.wikipedia.org/wiki/Category:ネットワーク管理 "wikilink")

1.  <https://www.jcp.org/en/jsr/detail?id=255>