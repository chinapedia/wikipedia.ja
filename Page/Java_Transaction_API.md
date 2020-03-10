> この記事は[Java Transaction API](https://ja.wikipedia.org/wiki/Java_Transaction_API)から翻訳されています。


** トランザクション API**（、JTA）とは、 の[APIの](../Page/アプリケーションプログラミングインタフェース.md "wikilink")1つであり、[XAリソース間の分散](https://ja.wikipedia.org/wiki/X/Open_XA "wikilink")[トランザクション処理](https://ja.wikipedia.org/wiki/トランザクション処理 "wikilink")を扱う。JTA は [{{langで](https://ja.wikipedia.org/wiki/Java_Community_Process "wikilink") JSR 907 として開発された仕様である。JTA は以下を提供する:

  - トランザクション境界の設定

  - API を使ったトランザクション処理

##  アーキテクチャ

[thumb](https://ja.wikipedia.org/wiki/ファイル:JTA1.PNG "wikilink")

アーキテクチャでは、トランザクションマネージャ（あるいは[TPモニター](https://ja.wikipedia.org/wiki/トランザクション処理 "wikilink")）がデータベースなどの複数リソース間のトランザクションを調整する。各リソースにはマネージャが対応している。リソースマネージャは一般にリソースを操作するための独自APIを持ち、例えば[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")では [JDBC](../Page/JDBC.md "wikilink") API が使われる。さらに、TPモニターは複数のリソースマネージャ間の分散トランザクションの調整を行う。そして、アプリケーションはTPモニターと通信し、TPモニターにトランザクション群の開始、[コミット](https://ja.wikipedia.org/wiki/コミット "wikilink")、[ロールバック](https://ja.wikipedia.org/wiki/ロールバック "wikilink")を指示する。また、アプリケーションは個々のリソースマネージャとも独自APIで通信し、リソースの更新などを行う。

## JTA の実装

[thumb](https://ja.wikipedia.org/wiki/ファイル:JTA2.PNG "wikilink")

JTA API は2つの[Java](https://ja.wikipedia.org/wiki/Java "wikilink")パッケージにあるクラス群で構成される:

  -
  -
JTA は  アーキテクチャに基づいているが、トランザクション境界を設定するために2つのAPIを定義している。JTA では EJBサーバのようなアプリケーションサーバとその上のアプリケーションコンポーネントを区別する。アプリケーションサーバがトランザクションの開始/コミット/ロールバックを指示するためのインターフェイスとして  がある。また、[サーブレットや](../Page/Java_Servlet.md "wikilink") [EJB](../Page/Enterprise_JavaBeans.md "wikilink") がトランザクションを管理するためのインターフェイスとして  がある。右の図は  インターフェイスとして使われる JTA のクラスを示している。

JTA アーキテクチャでは、各リソースマネージャ上に  インターフェイスを実装してTPモニターから制御できるようにする必要がある。前述したように各リソースマネージャには以下のような固有のAPIがある。

  - 関係データベース用: [JDBC](../Page/JDBC.md "wikilink")
  - メッセージングサービス用: [JMS](../Page/Java_Message_Service.md "wikilink")
  - 汎用EIS（企業情報システム）リソース用:  コネクター API

##  トランザクション・サービス

** トランザクション・サービス**（JTS\[1\]）とは、JTAを使ったトランザクションマネージャの実装である。アーキテクチャに基づいており、複数のJTS間のトランザクションの伝播には[IIOP](https://ja.wikipedia.org/wiki/IIOP "wikilink")を使う。 [アプリケーションサーバ](https://ja.wikipedia.org/wiki/アプリケーションサーバ "wikilink")はJTSの実装が必須とされている。

## 脚注

<references />

## 外部リンク

  - [ (JTA)](http://java.sun.com/products/jta/)
  - [ (JTS)](http://java.sun.com/products/jts/)
  - [JSR 907](http://www.jcp.org/en/jsr/detail?id=907)

[Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink") [Category:Java_enterprise_platform](https://ja.wikipedia.org/wiki/Category:Java_enterprise_platform "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")

1.