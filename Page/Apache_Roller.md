> この記事は[Apache Roller](https://ja.wikipedia.org/wiki/Apache_Roller)から翻訳されています。


**Apache Roller**（アパッチ・ローラ）は、[Javaベースで](../Page/Javaプラットフォーム.md "wikilink")[マルチブログ](https://ja.wikipedia.org/wiki/マルチブログ "wikilink")・[マルチユーザ](https://ja.wikipedia.org/wiki/マルチユーザ "wikilink")機能を兼ね備えた[オープンソース](../Page/オープンソース.md "wikilink")[ブログ](../Page/ブログ.md "wikilink")[サーバソフト](../Page/Webサーバ.md "wikilink")。[Apacheプロダクトのひとつ](../Page/Apacheソフトウェア財団.md "wikilink")。

## 概要

が2002年に雑誌記事のために書いたツールであるが、（現[](http://www.jroller.com/)）におけるポピュラーなものとなり、後に[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の従業員ブログや[IBM](../Page/IBM.md "wikilink") に採用された。2005年には[Apache](https://ja.wikipedia.org/wiki/Apache_Software_Foundation "wikilink") として採択された。3.1以降Incubatorを卒業、[Apache Software Foundationの公式プロジェクトとなっている](https://ja.wikipedia.org/wiki/Apache_Software_Foundation "wikilink")。

なお、Daveは2019年現在CloudBeesに所属している。

## 特徴

インストールガイドの前提環境は[Java SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") 5 + [Apache Tomcat](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink") 5.5以降または[Sun Web Server](https://ja.wikipedia.org/wiki/Sun_Web_Server "wikilink") 7.0またはProject [GlassFish](https://ja.wikipedia.org/wiki/GlassFish "wikilink") 2.0 ＋ [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")または[Apache Derbyであるのだが](../Page/Apache_Derby.md "wikilink")、[Java Servletソフトウェアの性格上](../Page/Java_Servlet.md "wikilink")、動作環境は懐が深い側面を持つ。

  - Servlet 2.4準拠なので、同規格に対応していれば[Webコンテナ](../Page/Webコンテナ.md "wikilink")は何でもよい。
  - データベースはMySQLまたはApache Derbyが推奨であるが、他に[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")、[IBM DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")、 [Oracle](../Page/Oracle_Database.md "wikilink")、[HSQLDB](https://ja.wikipedia.org/wiki/HSQLDB "wikilink")のセットアップスクリプトがデフォルトで用意されている。
  - 上記コンテナ環境およびデータベースソフトウェアが動作するのであればどのようなOSでもよい。

4.0より、Project GlassFishを用いる場合、同ソフトのアップデートツールを用いる事でインストールがきわめて容易に可能となった（基本的にGlassFishのインストール＞updatetoolからのRoller本体インストール＞JavaDBを立ちあげるだけ[1](http://blogs.sun.com/shioda/entry/glassfish_%E3%81%A8_apache_roller_%E7%B0%A1%E5%8D%98%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB)）。

動的にページを生成するのでサイト再構築の必要がない。[テンプレート](../Page/テンプレート.md "wikilink")があらかじめいくつか用意されているが、カスタマイズやオリジナルのテンプレートを用意することもできる。テンプレートはHTMLと独自マクロで構成されている。エディタは添付のものもあるが、[JSPを知っていれば独自に作成できる](../Page/JavaServer_Pages.md "wikilink")。内部的に[UTF-8](../Page/UTF-8.md "wikilink")を採用しているため[国際化](https://ja.wikipedia.org/wiki/国際化 "wikilink")対応もしており、[ローカライズ](https://ja.wikipedia.org/wiki/ローカライズ "wikilink")も容易にできる。現バージョンで一部機能にかかる部分を除いてほぼ日本語表示がなされるようになった。

代表的なブログソフトウェアの中でもRoller独特の機能として、

  - ひとりのユーザが複数のブログを作成・更新・管理できる
  - ひとつのブログを複数人で更新できる
  - ブログの投稿・設定権限が設定できる
      - 下書きのみ書けるLimited（下書き）権限
      - 下書きや投稿ができるAuthor（著者）権限
      - 投稿やブログの設定ができるAdmin（管理者）権限
  - サービス全体の管理者特権が用意されている
  - エントリごとにコメントの投稿制限や期限が設定できる
  - 特定言語向けの記事を書くことができる（3.0から）

がある。さらに3.1では以下の機能が追加された。

  - キーワードタグ
  - [Xinha](https://ja.wikipedia.org/wiki/Xinha "wikilink")ベースのエントリエディタ
  - フルプレビュー機能
  - コメント削除機能の強化
  - ファイルアップロードにおけるフォルダ機能のサポート

また、現行版ではLDAPサポートも入っている（設定を若干いじる必要あり）。

2009年10月にリリースされた5.0では以下の機能が追加された。

  - [OpenID](../Page/OpenID.md "wikilink")のサポート。
  - ビデオや画像、オーディオファイルを簡単にアップロードし、管理する機能。
  - 簡単なマルチドメインのサポート。
  - ブログの所有者が他人のコメントを編集する機能。
  - OAuthのサポート。

## 関連項目

  - [Apache Tomcat](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink")
  - [ブログ](../Page/ブログ.md "wikilink")
  - [Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")

## 外部リンク

基本的に英語サイトであるが、公式を含めいくつかのサイトでは日本語のドキュメントもある。

### 公式サイト

  - [公式プロジェクト](http://rollerweblogger.org/)
  - [Apache Project](http://roller.apache.org/)
  - [Java.net Support Project](https://roller.dev.java.net/)
  - [Daveのブログ](http://rollerweblogger.org/roller/)

### Rollerを採用しているサイト

  - [JRoller](http://www.jroller.com/)
  - [IBM developerWorks blogs](http://www-03.ibm.com/developerworks/blogs/)
  - [blogs.sun.com](http://blogs.sun.com/)
  - [NetBeans.jp](http://www.netbeans.jp)（日本語）

[Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink") [Category:ブログソフト](https://ja.wikipedia.org/wiki/Category:ブログソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")