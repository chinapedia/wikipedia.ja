> この記事は[Apache Derby](https://ja.wikipedia.org/wiki/Apache_Derby)から翻訳されています。


**Apache Derby**（アパッチ・ダービー）は、[IBM](../Page/IBM.md "wikilink")から寄贈された[Cloudscape](https://ja.wikipedia.org/wiki/Cloudscape "wikilink")の[ソースコード](../Page/ソースコード.md "wikilink")を元に、 [Apacheソフトウェア財団](../Page/Apacheソフトウェア財団.md "wikilink")によって[プログラムの開発が進められている](../Page/プログラム_\(コンピュータ\).md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")技術で実装された[RDBMSの](../Page/関係データベース管理システム.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")。

## 歴史

  - 1996年: Cloudscape Inc. 設立
    1997年: Cloudscape Inc. よりJBMSという名称でリリースされ、その後Cloudscapeと改名。
    1999年: Informix Software, Inc.により、Cloudscape Inc が買収される。
    2001年: [IBM](../Page/IBM.md "wikilink")が[Informix](../Page/Informix.md "wikilink")からCloudscapeを含むDBMSのソフトウェア資産を買収。IBM Cloudscapeとブランド名称が変更されリリースが続けられる。主に、IBM製品の組み込みDBMSとして使われる。
    2004年: [IBM](../Page/IBM.md "wikilink")よりソースコードが[Apacheソフトウェア財団](../Page/Apacheソフトウェア財団.md "wikilink")に寄贈される。
    2005年: incubationを卒業してApache DBのsubprojectとなる。
    [サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")がApache Derbyを基にしたJava DBを提供することを発表。
    2006年: サン・マイクロシステムズが[JDK](../Page/Java_Development_Kit.md "wikilink") 6にJava DBを同梱することを発表。
    2007年: IBMがCloudscapeの販売終了を決定。[1](http://www-1.ibm.com/support/docview.wss?rs=636&uid=swg21256502)

## 特徴

  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")技術により実装されている。
  - [APIとして](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[JDBC](../Page/JDBC.md "wikilink")を提供する。特に10.2.2.0より提供されるバイナリはJDBC4.0をサポートする。

### 構成

  - EngineとNetwork Server、Network Clientおよびツール群から構成される。

### Engine

  - [RDBMSの機能を提供する](../Page/関係データベース管理システム.md "wikilink")。
  - [トランザクション](../Page/トランザクション.md "wikilink")処理が、[IBM](../Page/IBM.md "wikilink")が[1989年](../Page/1989年.md "wikilink")に開発した、[ARIES](https://ja.wikipedia.org/wiki/ARIES "wikilink")(Algorithm for Recovery and Isolation Exploiting Semantics)という[アルゴリズム](../Page/アルゴリズム.md "wikilink")により実現されている。 [2](http://db.apache.org/derby/papers/recovery.html#ARIES+-+An+Overview)[3](http://www.almaden.ibm.com/u/mohan/RJ6649Rev.pdf)
  - [アプリケーションに](../Page/アプリケーションソフトウェア.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")として組み込んでembedded modeで利用可能。
  - プログラムのフットプリントが小さい。
      - Engineが固有の[インタープリタ](https://ja.wikipedia.org/wiki/インタープリタ "wikilink")を持たずに済むよう、SQLの[実行計画](https://ja.wikipedia.org/wiki/実行計画 "wikilink")から[バイトコード](../Page/バイトコード.md "wikilink")が出力され、Javaのクラスが内部的に生成される設計となっている。

### Network Server/Network Client

  - [DRDA](https://ja.wikipedia.org/wiki/DRDA "wikilink")を実装しており、Engineを[network経由で利用する機能を提供する](../Page/コンピュータネットワーク.md "wikilink")。
  - [JDBC](../Page/JDBC.md "wikilink")、[ODBC](../Page/Open_Database_Connectivity.md "wikilink")/[CLI](../Page/Call_Level_Interface.md "wikilink")、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")/[Perl](../Page/Perl.md "wikilink")からの利用が可能。

### ツール群

#### ij

Derbyのデータベースに接続してSQLを発行する。

#### dblook

データベースからDDL文を抽出する。

#### sysinfo

Javaの実行環境に関する情報とDerbyのバージョン情報を表示する。

<references/>

## 利用

Apache Derbyに付加価値を加えて商品化した[Cloudscape](https://ja.wikipedia.org/wiki/Cloudscape "wikilink")と[Java DBを](https://ja.wikipedia.org/wiki/Java_DB "wikilink")、[IBM](../Page/IBM.md "wikilink")と[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")がそれぞれ提供している。

また様々な製品やプロジェクトにて、Apache Derbyは組み込まれたDBMSとして使われている/DBMSとして利用可能である。[4](http://wiki.apache.org/db-derby/UsesOfDerby)

## 雑学

[Apache Derbyのロゴ](http://db.apache.org/derby/logo.html)はダービー帽に掛けている。

## 参考文献

  - Apache Derby Projectのサイト: [The Apache Derby Project](http://db.apache.org/derby/)

    Cloudscapeのサイト: [IBM Cloudscape](http://www-306.ibm.com/software/data/cloudscape/)

    Java DBのサイト:[Java DB](http://developers.sun.com/prodtech/javadb/index.jsp)

## 関連項目

  - [JDBC](../Page/JDBC.md "wikilink")
  - [Java Platform, Standard Edition](../Page/Java_Platform,_Standard_Edition.md "wikilink")

[Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink") [Category:データベース管理システム](https://ja.wikipedia.org/wiki/Category:データベース管理システム "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")