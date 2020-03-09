> この記事は[JavaServer Pages](https://ja.wikipedia.org/wiki/JavaServer_Pages)から翻訳されています。


**JavaServer Pages** (**JSP**) は、[HTML内に](../Page/HyperText_Markup_Language.md "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のコードを埋め込んでおき、[Webサーバ](../Page/Webサーバ.md "wikilink")で動的に[Webページを生成してクライアントに返す技術のこと](../Page/ウェブページ.md "wikilink")。

## 概要

[thumbアーキテクチャにおけるJSP](https://ja.wikipedia.org/wiki/ファイル:JSP_Model_2.svg "wikilink"), [Java Servlet](../Page/Java_Servlet.md "wikilink"), [JavaBeans](https://ja.wikipedia.org/wiki/JavaBeans "wikilink")の位置づけ\]\]

Javaのコードは、`<%`と`%>`記号で囲まれた部分に書かれる。HTMLの中にスクリプトが断片的に見えるため、この記法をスクリプトレット (scriptlet) と呼ぶ。これよりプログラムコードをタグに見立てることができるため、プログラムとデザインの棲み分けができる。定義されたカスタムタグライブラリを使用すればスクリプトレットを使わずに独自のタグでコードを埋め込むことができる。

[サーブレットの機能のひとつとして実装されている](../Page/Java_Servlet.md "wikilink")。

サーブレットと違い、HTMLの中でデザイン部分とプログラム部分を分けて書くためにある程度までウェブデザイナの負担を減らすこともできる。また、静的な出力が多い場合に適している\[1\]。類似技術として[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[ASP](https://ja.wikipedia.org/wiki/Active_Server_Pages "wikilink")、[ASP.NET](https://ja.wikipedia.org/wiki/ASP.NET "wikilink")などがある。

クライアントからのJSPの実行がリクエストされると、[アプリケーションサーバ](https://ja.wikipedia.org/wiki/アプリケーションサーバ "wikilink")の[サーブレットコンテナ](https://ja.wikipedia.org/wiki/サーブレットコンテナ "wikilink")はJSPソースファイルをサーブレットのソースコードに変換する。そしてさらにそのソースコードをその場でコンパイルして実行し、結果をクライアントに返信する。このため、最初はコンパイルの時間がかかるが、いちどコンパイルが実行されると2回目以降は必要なくなるため、結果としてアクセス速度が早くなる。

カスタムタグライブラリとしては、Javaの標準仕様の一部として定義された[JSTLや](https://ja.wikipedia.org/wiki/#JSTL "wikilink")、[Apache Strutsのようなフレームワークが独自に定義したものがあり](https://ja.wikipedia.org/wiki/Apache_Struts "wikilink")、こうしたタグを使用することでより可読性を高めることができる。JSP2.0では、従来のタグハンドラクラスを作成しなくてもカスタムタグライブラリを作成できるタグファイルの仕組みが導入された。タグファイは、JSPの文法で作成されるファイルで拡張子は、「.tag」となる。

[Model View Controllerアーキテクチャでは](https://ja.wikipedia.org/wiki/Model_View_Controller "wikilink")、JSPをView、[Java ServletをController](../Page/Java_Servlet.md "wikilink")、[JavaBeans](https://ja.wikipedia.org/wiki/JavaBeans "wikilink")をModelとして用いることが想定されている。

## 構文

### タグ

HTMLの中に以下の特殊タグを記述することができる。

| 名称       | タグ               | 説明                           |
| -------- | ---------------- | ---------------------------- |
| ディレクティブ  | \<%@ ディレクティブ %\> | このJSPファイルの処理時の属性をWebコンテナに伝える |
| 宣言       | \<%\! 宣言 %\>     | JSPで使用する変数やメソッドを宣言する         |
| スクリプトレット | \<% Javaコード %\>  | タグ内にJavaのコードを自由に記述する         |
| 式        | \<%= 式 %\>       | 式の評価結果をHTMLの中に出力する           |
| アクション    | <jsp:アクション名>     | JSPでよく行う処理をタグで簡潔に記述する        |
| コメント     | \<%-- コメント --%\> | JSPとしてのコメントを記述する             |

JSPのタグ

### ディレクティブ

ディレクティブの種類としては、以下のものがある。

| 名称      | 説明                                                                                                                               | 例                                                                                     |
| ------- | -------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| page    | JSPファイルのエンコーディングやJSPプログラムのコーディングに必要なimport文、セッション管理を行う                                                                           | \<%@ page contentType="text/html; charset=Windows-31J" pageEncoding="Windows-31J" %\> |
| include | テキストファイルやその他のJSPファイルをインクルードする。インクルードは、JSPからServletに変換される時に行われる。ファイルの拡張子としてJSPを使用せずに他の拡張子を使用する。一般的には、「.jspf」(JSP Fragment)が使用される。 | \<%@ include file="header.jspf" %\>                                                   |
| taglib  | カスタムタグを使用できるようにするための設定を行う                                                                                                        | \<%@ taglib uri="<http://www.sample.com/tags/test>" prefix="tst" %\>                  |

ディレクティブの種類

### アクション

アクションの種類としては、以下のものがある。

  - jsp:include
    jsp:param
    jsp:forward
    jsp:plugin
    jsp:fallback
    jsp:getProperty
    jsp:setProperty
    jsp:useBean

JSP2.0では、以下のものが追加になった。

  - jsp:attribute
    jsp:body
    jsp:doBody
    jsp:invoke
    jsp:element

### 暗黙オブジェクト

Javaのコード中で以下の変数があらかじめ利用できる状態（暗黙オブジェクトとして）で用意されている。

| 変数名         | 説明                                                 |
| ----------- | -------------------------------------------------- |
| out         | javax.servlet.jsp.JspWriterクラスのオブジェクト変数            |
| request     | javax.servlet.http.HttpServletRequestクラスのオブジェクト変数  |
| response    | javax.servlet.http.HttpServletResponseクラスのオブジェクト変数 |
| pageContext | javax.servlet.jsp.PageContextクラスのオブジェクト変数          |
| session     | javax.servlet.http.HttpSessionクラスのオブジェクト変数         |
| application | javax.servlet.ServletContextクラスのオブジェクト変数           |
| config      | javax.servlet.ServletConfigクラスのオブジェクト変数            |
| page        | javax.servlet.jsp.HttpJspPageクラスのオブジェクト変数          |
| exception   | java.lang.Throwableクラスのオブジェクト変数                    |

暗黙オブジェクト

## JSTL

JSTL（、JSP標準タグライブラリ）は、JSPでよく用いられる標準的な機能を定義したカスタムタグ[ライブラリ](../Page/ライブラリ.md "wikilink")である。[2001年](../Page/2001年.md "wikilink")に定義された[J2EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink") 1.3において標準仕様の一つとして導入された。\[2\]

JSTLでは、[変数の操作や](https://ja.wikipedia.org/wiki/変数_\(プログラミング\) "wikilink")[if文](https://ja.wikipedia.org/wiki/if文 "wikilink")といった標準的な機能を提供するコアライブラリに加え、[XMLや](../Page/Extensible_Markup_Language.md "wikilink")[国際化](https://ja.wikipedia.org/wiki/国際化と地域化 "wikilink")、[SQL](../Page/SQL.md "wikilink")のライブラリ、さらに[文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")操作といった[関数をまとめたライブラリが提供されている](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")。\[3\]

## EL式

EL式（、式言語）は、JSP 2.0で導入された新たな構文で、従来のスクリプトレットに代わってより可読性に優れたJSPファイルを記述できるようにしたもの。EL式はJSPをベースにした[Webアプリケーションフレームワーク](https://ja.wikipedia.org/wiki/Webアプリケーションフレームワーク "wikilink")である[JSFにおいても独自に定義されていたが](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink")、後のJSP 2.1, JSF 1.2において一つの仕様に統合され（、統合式言語）、さらに[2013年](https://ja.wikipedia.org/wiki/2013年 "wikilink")のEL 3.0ではJSPから独立した[Java EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink") 7の仕様の一つとなっている。\[4\]

Expression Languageは、${}で表現する。

    ${sessionScope.user.id}

Expression Languageでは、以下のような暗黙オブジェクトが利用できる。

| 変数名              | 説明                                        |
| ---------------- | ----------------------------------------- |
| pageContext      | javax.servlet.jsp.PageContextクラスのオブジェクト変数 |
| pageScope        | pageスコープからオブジェクトを取得                       |
| requestScope     | requestスコープからオブジェクトを取得                    |
| sessionScope     | sessionスコープからオブジェクトを取得                    |
| applicationScope | applicationスコープからオブジェクトを取得                |
| param            | リクエストパラメータを格納するMapオブジェクト                  |
| paramValues      | 複数の値を持つリクエストパラメータを格納するString型配列           |
| header           | リクエストヘッダーと値を格納するMapオブジェクト                 |
| headerValues     | 複数の値を持つリクエストヘッダーを格納するString型配列            |
| cookie           | クッキーを格納するMapオブジェクト                        |
| initParam        | コンテクスト初期化パラメータを格納するMapオブジェクト              |
|                  |                                           |

暗黙オブジェクト

## 歴史

| バージョン                         | JSR                                        | リリース日       |
| ----------------------------- | ------------------------------------------ | ----------- |
| 1.0                           |                                            | 1999年6月2日   |
| 1.1                           |                                            | 1999年12月17日 |
| 1.2                           | [53](http://jcp.org/en/jsr/detail?id=53)   | 2001年9月25日  |
| 2.0                           | [152](http://jcp.org/en/jsr/detail?id=152) | 2003年11月24日 |
| 2.1                           | [245](http://jcp.org/en/jsr/detail?id=245) | 2006年5月11日  |
| 2.2(2.1 Maintenance Release)  | 2009年12月10日                                |             |
| 2.3(2.1 Maintenance Release2) | 2013年6月12日                                 |             |

歴史

## 脚注

## 関連項目

  - [Java Servlet](../Page/Java_Servlet.md "wikilink")
  - [JavaServer Faces](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink")
  - [Webコンテナ](https://ja.wikipedia.org/wiki/Webコンテナ "wikilink")
  - [アプリケーションサーバ](https://ja.wikipedia.org/wiki/アプリケーションサーバ "wikilink")

## 外部リンク

  - [JavaServer Pages Technology](http://www.oracle.com/technetwork/java/jsp-138432.html)
  - [JSP Standard Tag Library](https://jstl.java.net/)
  - [Apache Taglibs](http://tomcat.apache.org/taglibs/)  - JSTL実装
  - [Javaの道 - Servlet・JSP](http://www.javaroad.jp/servletjsp/)
  - [TECHSCORE - JSP](http://www.techscore.com/tech/Java/JavaEE/JSP/index/)

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:ウェブ開発](https://ja.wikipedia.org/wiki/Category:ウェブ開発 "wikilink") [Category:テンプレートエンジン](https://ja.wikipedia.org/wiki/Category:テンプレートエンジン "wikilink") [Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink") [Category:Java_enterprise_platform](https://ja.wikipedia.org/wiki/Category:Java_enterprise_platform "wikilink")

1.  サーブレットではprintlnメソッドが頻繁に現れて、可読性が低下するため
2.
3.
4.