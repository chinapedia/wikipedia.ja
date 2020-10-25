> この記事は[Django](https://ja.wikipedia.org/wiki/Django)から翻訳されています。


**Django**（ジャンゴ）は、[Python](../Page/Python.md "wikilink")で実装された[Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")。[MVC](../Page/Model_View_Controller.md "wikilink")[デザインパターン](https://ja.wikipedia.org/wiki/デザインパターン "wikilink")に緩やかに従う。もともとは[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[カンザス州](../Page/カンザス州.md "wikilink")[ローレンスにあるWorld](https://ja.wikipedia.org/wiki/ローレンス_\(カンザス州\) "wikilink") Company\[1\]のために、ニュース系のサイトを管理する目的で開発され、[2005年](../Page/2005年.md "wikilink")7月に[BSD Licenseで公式にリリースされた](https://ja.wikipedia.org/wiki/BSD_License "wikilink")。フレームワークは[ジプシー・スウィング](https://ja.wikipedia.org/wiki/ジプシー・スウィング "wikilink")のギタリストである[ジャンゴ・ラインハルト](../Page/ジャンゴ・ラインハルト.md "wikilink")にちなんで命名された。

Djangoの第一の目的は、複雑なデータベース主体の[ウェブサイト](../Page/ウェブサイト.md "wikilink")の構築を簡単にすることであり、コンポーネントの再利用性と'pluggability'、素早い開発、[Don't repeat yourselfの原則に力点を置いている](../Page/Don't_repeat_yourself.md "wikilink")。ファイルやデータのモデルにいたるまで、[Python](../Page/Python.md "wikilink")が一貫して用いられている。Djangoはまた、動的に生成され、データモデルの定義を通じて完全に構成することができる、データベース管理[CRUD](../Page/CRUD.md "wikilink")インターフェイスをオプションで提供する。Python3系統にはDjango 1.5バージョンで実験的に対応し、Django 1.6より本格的に対応した\[2\]\[3\]。Python2系統への対応は、バージョン1.11（3年サポートのLTS、2020年4月まで）が最後となり、2.0でPython3.4以降、2.1でPython3.5以降にのみの対応となった\[4\]。

Djangoを使用している有名なサイトには、\[5\]、[Instagram](https://ja.wikipedia.org/wiki/Instagram "wikilink")\[6\]、 [Mozilla](../Page/Mozilla_Foundation.md "wikilink")\[7\]*、[The Washington Times](https://ja.wikipedia.org/wiki/The_Washington_Times "wikilink")*\[8\]、[Disqus](https://ja.wikipedia.org/wiki/Disqus "wikilink")\[9\]、[Bitbucket](https://ja.wikipedia.org/wiki/Bitbucket "wikilink")\[10\]、\[11\]などがある。

## Djangoのコンポーネント

Djangoフレームワークのコア部分は[データモデル](../Page/データモデル.md "wikilink")（Pythonクラスとして定義される）と[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")との間を仲介する[O/Rマッパー](../Page/オブジェクト関係マッピング.md "wikilink")、[正規表現](../Page/正規表現.md "wikilink")に基づく[URLディスパッチャ](../Page/Uniform_Resource_Locator.md "wikilink")、要求を処理するビューシステム、[テンプレートシステムから構成される](https://ja.wikipedia.org/wiki/テンプレートエンジン#ウェブテンプレートエンジン "wikilink")。

そのほか、下記のものがコアのフレームワークに含まれる:

  - 開発とテストのための軽量のスタンドアロン[Webサーバ](../Page/Webサーバ.md "wikilink")
  - [HTMLフォームをデータベースに格納できる値に変換するフォームの](../Page/フォーム_\(ウェブ\).md "wikilink")[シリアル化と検証システム](https://ja.wikipedia.org/wiki/シリアライゼーション "wikilink")
  - 複数のキャッシュ方法に対応した[キャッシュフレームワーク](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")
  - 要求を処理するさまざまな段階に挿入し、カスタムの処理を実行できる[ミドルウェア](../Page/ミドルウェア.md "wikilink")クラスのサポート
  - アプリケーションのコンポーネントがあらかじめ定義されたシグナルを用いてイベント通信できるようにする内部ディスパッチャシステム
  - [国際化の機構](../Page/国際化と地域化.md "wikilink")（Django自身のコンポーネントも多数の言語へ翻訳されている）
  - Django モデルのインスタンスを[XMLおよび](../Page/Extensible_Markup_Language.md "wikilink")[JSONに対して入出力可能なシリアル化機構](../Page/JavaScript_Object_Notation.md "wikilink")
  - テンプレートエンジンの機能を拡張する機構

## バンドルされるアプリケーション

Djangoの公式配布物は、"contrib"パッケージ内に多数のアプリケーションを含んでいる。

  - 拡張可能な認証機構
  - 動的な管理インターフェイス
  - [RSS](../Page/RSS.md "wikilink")と[Atom配信用のフィードを生成するツール](../Page/Atom_\(ウェブコンテンツ配信\).md "wikilink")
  - 柔軟なコメントシステム
  - [Sitemaps](https://ja.wikipedia.org/wiki/Sitemaps "wikilink")を生成するツール
  - [クロスサイトリクエストフォージェリ](../Page/クロスサイトリクエストフォージェリ.md "wikilink") (CSRF) を防止するためのツール
  - [Textile](https://ja.wikipedia.org/wiki/Textile "wikilink")や[Markdown](https://ja.wikipedia.org/wiki/Markdown "wikilink")などの[軽量マークアップ言語](../Page/軽量マークアップ言語.md "wikilink")の使用が可能なテンプレートライブラリ

## サーバ構成

Djangoは[Apache 2で](../Page/Apache_HTTP_Server.md "wikilink")[mod_python](https://ja.wikipedia.org/wiki/mod_python "wikilink")を使って、あるいは任意の[WSGI準拠のウェブサーバで動作させることができる](../Page/Web_Server_Gateway_Interface.md "wikilink")。[Nginx](https://ja.wikipedia.org/wiki/Nginx "wikilink")とuWSGIでも動作が可能となっている。Djangoは[FastCGI](../Page/FastCGI.md "wikilink")サーバを起動することができ、FastCGIをサポートする任意のWebサーバのバックエンドで使用することができる。

以下のデータベースが、Djangoでの使用を公式にサポートされている。

  - [PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")
  - [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")
  - [SQLite](../Page/SQLite.md "wikilink")
  - [Oracle](../Page/Oracle_Database.md "wikilink")

サードパーティから、[Microsoft SQL Server用のアダプター](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")[Django MSSQL](https://django-mssql.readthedocs.io/en/latest/)、[IBM DB2用のアダプター](https://ja.wikipedia.org/wiki/IBM_DB2 "wikilink")[ibm_db](http://code.google.com/p/ibm-db/)に加え、SAP SQL Anywhere、[ODBC](../Page/Open_Database_Connectivity.md "wikilink")、[Firebird](../Page/Firebird.md "wikilink")へのアダプターも提供されている。

## The Django Book

The Django Bookは、Djangoについての[GNU Free Documentation Licenseでライセンスされたフリーの書籍である](../Page/GNU_Free_Documentation_License.md "wikilink")。2007年12月、[Apress](https://ja.wikipedia.org/wiki/Apress "wikilink")によって出版された。書籍は\[<http://www.djangobook.com/> [http://www.djangobook.com/\]で入手できる](http://www.djangobook.com/%5Dで入手できる)。

## 脚注

## 外部リンク

  -

  - [The Django Book](http://www.djangobook.com/)

  - [DJANGOPROJECT.JP](http://djangoproject.jp/) - 日本のユーザーコミュニティ

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Python](https://ja.wikipedia.org/wiki/Category:Python "wikilink") [Category:ウェブアプリケーションフレームワーク](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーションフレームワーク "wikilink")

1.  [LJWorld.com / About us](http://www2.ljworld.com/about)
2.
3.
4.
5.
6.
7.
8.  [Opensource.washingtontimes.com](http://opensource.washingtontimes.com/). Retrieved on 2014-05-30.
9.
10.
11.