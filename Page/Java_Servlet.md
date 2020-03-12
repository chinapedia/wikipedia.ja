> この記事は[Java Servlet](https://ja.wikipedia.org/wiki/Java_Servlet)から翻訳されています。


**Java Servlet**（ジャバ サーブレット）とは、[サーバ](../Page/サーバ.md "wikilink")上で[ウェブページ](../Page/ウェブページ.md "wikilink")などを動的に生成したりデータ処理を行うために、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で作成された[プログラム及びその仕様である](../Page/プログラム_\(コンピュータ\).md "wikilink")。単にサーブレットと呼ばれることが多い。[Java EEの一機能という位置づけになっている](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")。この機能を用いてショッピングサイトやオンラインバンキングなどをはじめとする多種多様な動的なWebサイトが構築されている。

[2018年](../Page/2018年.md "wikilink")現在の最新版は、Java EE 8 に含まれる Servlet 4.0 (JSR-369) である。

## 概要

[thumbアーキテクチャにおけるJava](https://ja.wikipedia.org/wiki/ファイル:JSP_Model_2.svg "wikilink") Servlet, [JSP](../Page/JavaServer_Pages.md "wikilink"), [JavaBeans](../Page/JavaBeans.md "wikilink")の位置づけ\]\]

Java Servletはサーバサイド技術として登場した。

同様の技術（すなわち対抗技術）としては[Perl](../Page/Perl.md "wikilink")などを用いた[CGI](../Page/Common_Gateway_Interface.md "wikilink")、[PHPプログラムのプロセスを](../Page/PHP_\(プログラミング言語\).md "wikilink")[Apache HTTP Server上で動かすことができるmod](../Page/Apache_HTTP_Server.md "wikilink")_phpなどのモジュール、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が提供する[ASPなどがある](../Page/Active_Server_Pages.md "wikilink")。CGIが[クライアントのリクエストのたびに新しい](../Page/クライアント_\(コンピュータ\).md "wikilink")[プロセス](../Page/プロセス.md "wikilink")を起動するのに対して、サーブレットは[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")に常駐して、リクエストのたびにプロセスより軽量な[スレッドを起動するので](../Page/スレッド_\(コンピュータ\).md "wikilink")、効率がよい。また、サーブレットはJavaで書かれているのでさまざまなプラットフォームで使うことができる。

Servlet 2.3からは、フィルター機能が追加され、Servletの実行前後に処理を差し込むことが可能となった。

サーブレットの技術の延長として[JSPがあるが](../Page/JavaServer_Pages.md "wikilink")、JSPはサーブレットを自動生成して動作している。厳密に言えばサーブレットとJSPは違う技術だが、これらは組み合わせて使うのが一般的なため、JSPもサーブレットの一部として扱われることが多い。

サーブレットの実行環境（実行するためのソフトウェア）はWebコンテナ、またはサーブレットコンテナと呼ばれる。これらの言葉はあまり区別されずに使われることも多いが、純粋にサーブレットの処理を行うものをサーブレットコンテナと呼び、サーブレットコンテナを含みJSPや[HTTPサーバとしての機能も含むものを](../Page/Webサーバ.md "wikilink")[Webコンテナ](../Page/Webコンテナ.md "wikilink")と呼ぶ傾向がある。

[Webコンテナ](../Page/Webコンテナ.md "wikilink")としては、[Apache Tomcat](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink"), [Jetty](https://ja.wikipedia.org/wiki/Jetty "wikilink"), [BEA WebLogic Server](https://ja.wikipedia.org/wiki/BEA_WebLogic_Server "wikilink"), IBM [WebSphere Application Server](../Page/WebSphere_Application_Server.md "wikilink"), [Resin](https://ja.wikipedia.org/wiki/:en:Resin_Server "wikilink"), [JBoss](../Page/JBoss.md "wikilink")などがある。

## サーバサイドJava

当初、Javaは[Applet](https://ja.wikipedia.org/wiki/Applet "wikilink")などのクライアント側でJavaプログラムを稼動させるクライアントサイドの技術として注目を集めていた。しかし、サーブレットの登場以降、サーバ側でJavaプログラムを稼動させる形態が急速に普及した。こうしたサーバ側でJavaプログラムを稼動させる形態をサーバサイドJavaと呼ぶ。

## 役割

JSPの登場により、Java Servletはデータの入出力処理 (Controller) を担当することが推奨される。これは[Model View Controller](../Page/Model_View_Controller.md "wikilink") (MVC) による役割付けである。

## 歴史

| バージョン | リリース    | プラットフォーム           | 内容                                                                                                                                                                                           |
| ----- | ------- | ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1.0   | 1997/01 | \--                | \--                                                                                                                                                                                          |
| 2.0   |         | JDK 1.1            | Java Servlet Development Kit 2.0の一部としてリリース                                                                                                                                                   |
| 2.1   | 1998/11 | \--                | 公式な初版、RequestDispatcher, ServletContextを追加                                                                                                                                                   |
| 2.2   | 1999/08 | J2EE 1.2, J2SE 1.2 | J2EEの一部となる                                                                                                                                                                                   |
| 2.3   | 2001/08 | J2EE 1.3, J2SE 1.2 | Filter機能追加                                                                                                                                                                                   |
| 2.4   | 2003/11 | J2EE 1.4, J2SE 1.3 | web.xml にXML Schema を利用                                                                                                                                                                      |
| 2.5   | 2005/09 | JavaEE 5, JavaSE 5 | JavaSE 5が必須となる, annotationをサポート                                                                                                                                                              |
| 3.0   | 2009/12 | JavaEE 6, JavaSE 6 | 開発容易性の実現, 動的設定, login/logoutメソッドサポート, 非同期Servlet, アノテーションSecurity, Fileアップロード                                                                                                                |
| 3.1   | 2013/05 | JavaEE 7           | [クラウド対応](https://ja.wikipedia.org/wiki/クラウドコンピューティング "wikilink"), ノンブロッキング処理用I/O APIの追加, [WebSocket](https://ja.wikipedia.org/wiki/WebSocket "wikilink")等へのプロトコルアップグレードの対応, セキュリティ機能の強化\[1\] |
| 4.0   | 2017/09 | JavaEE 8           | [HTTP/2](https://ja.wikipedia.org/wiki/HTTP/2 "wikilink")サポート                                                                                                                                |

Servletの歴史

## 例

以下は、`service()`[メソッドが何回呼ばれたかを出力する単純なサーブレットである](../Page/メソッド_\(計算機科学\).md "wikilink")。

サーブレットは`Servlet`[インタフェースを実装する必要がある](../Page/インタフェース_\(情報技術\).md "wikilink")。サーブレットの実装は通常、[プロトコルに依存しない](../Page/通信プロトコル.md "wikilink")[抽象クラスである](https://ja.wikipedia.org/wiki/抽象型 "wikilink")`GenericServlet`か、[HTTP用のサブクラスである](../Page/Hypertext_Transfer_Protocol.md "wikilink")`HttpServlet`クラスを継承することで行う。この例では`HttpServlet`クラスを継承している。

`service()`メソッドはサーブレットの[リクエスト](https://ja.wikipedia.org/wiki/リクエスト "wikilink")ごとの処理を記述するメソッドである。`HttpServlet`クラスを継承する場合、ここからさらに`doGet()`, `doPost()`, `doPut()`, `doDelete()`といった[HTTPメソッドごとのメソッドに分岐させることができる](https://ja.wikipedia.org/wiki/Hypertext_Transfer_Protocol#メソッド "wikilink")。ただし、以下の例ではその機能を使わず、直接`service()`メソッドを[オーバーライド](../Page/オーバーライド.md "wikilink")している。

``` java
import java.io.IOException;

import javax.servlet.ServletConfig;
import javax.servlet.ServletException;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;

public class ServletLifeCycleExample extends HttpServlet {

    private int count;

    @Override
    public void init(ServletConfig config) throws ServletException {
        super.init(config);
        getServletContext().log("init() called");
        count = 0;
    }

    @Override
    protected void service(HttpServletRequest request, HttpServletResponse response)
            throws ServletException, IOException {
        getServletContext().log("service() called");
        count++;
        response.getWriter().write("Incrementing the count: count = " + count);
    }

    @Override
    public void destroy() {
        getServletContext().log("destroy() called");
    }

}
```

## Web.xml定義

<table>
<caption>Web.xml定義</caption>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>定義内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2.3</p></td>
<td><?xml version="1.0" encoding="UTF-8"?>
<p>&lt;!DOCTYPE web-app PUBLIC "-//Sun Microsystems, Inc.//DTD Web Application 2.3//EN" "<a href="http://java.sun.com/dtd/web-app_2_3.dtd">http://java.sun.com/dtd/web-app_2_3.dtd</a>"&gt;</p>
<p><web-app></p>
<p></web-app></p></td>
</tr>
<tr class="even">
<td><p>2.4</p></td>
<td><?xml version="1.0" encoding="UTF-8"?>
<p><web-app ns="http://java.sun.com/xml/ns/j2ee" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://java.sun.com/xml/ns/j2ee/web-app_2_4.xsd" version="2.4"></p>
<p></web-app></p></td>
</tr>
<tr class="odd">
<td><p>2.5</p></td>
<td><?xml version="1.0" encoding="UTF-8"?>
<p><web-app ns="http://java.sun.com/xml/ns/javaee" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://java.sun.com/xml/ns/javaee http://java.sun.com/xml/ns/javaee/web-app_2_5.xsd" version="2.5"></p>
<p></web-app></p></td>
</tr>
<tr class="even">
<td><p>3.0</p></td>
<td><?xml version="1.0" encoding="UTF-8"?>
<p><web-app ns="http://java.sun.com/xml/ns/javaee" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:web="http://java.sun.com/xml/ns/javaee/web-app_3_0.xsd"
xsi:schemaLocation="http://java.sun.com/xml/ns/javaee http://java.sun.com/xml/ns/javaee/web-app_3_0.xsd" id="WebApp_ID" version="3.0"></p>
<p></web-app></p></td>
</tr>
<tr class="odd">
<td><p>3.1</p></td>
<td><?xml version="1.0" encoding="UTF-8"?>
<p><web-app ns="http://xmlns.jcp.org/xml/ns/javaee" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:schemaLocation="http://xmlns.jcp.org/xml/ns/javaee http://xmlns.jcp.org/xml/ns/javaee/web-app_3_1.xsd" version="3.1"></p>
<p></web-app></p></td>
</tr>
</tbody>
</table>

## 脚注

## 関連項目

  - [Java Platform, Enterprise Edition](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")
  - [アプリケーションサーバ](../Page/アプリケーションサーバ.md "wikilink")
  - [ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")
  - [JavaServer Pages](../Page/JavaServer_Pages.md "wikilink")
  - [JavaBeans](../Page/JavaBeans.md "wikilink")
  - [アプレット](https://ja.wikipedia.org/wiki/アプレット "wikilink")

## 外部リンク

  - [Java Servlet 2.3](https://jcp.org/aboutJava/communityprocess/final/jsr053/) JSR-053
  - [Java Servlet 2.4](https://jcp.org/aboutJava/communityprocess/final/jsr154/) JSR-154 Final Release
  - [Java Servlet 2.5](https://jcp.org/aboutJava/communityprocess/mrel/jsr154/) JSR-154 Maintenance Release
  - [Java Servlet 3.0](https://jcp.org/en/jsr/detail?id=315) JSR-315
  - [Java Servlet 3.1](https://jcp.org/en/jsr/detail?id=340) JSR-340
  - [Java Servlet 4.0](https://jcp.org/en/jsr/detail?id=369) JSR-363

[Category:ウェブ開発](https://ja.wikipedia.org/wiki/Category:ウェブ開発 "wikilink") [Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink") [Category:Java_enterprise_platform](https://ja.wikipedia.org/wiki/Category:Java_enterprise_platform "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink")

1.