> この記事は[Django](https://ja.wikipedia.org/wiki/Django)から翻訳されています。


**Django**（ジャンゴ）は、[Python](../Page/Python.md "wikilink")で実装された[Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")。 [model-view-controller](https://ja.wikipedia.org/wiki/model-view-controller "wikilink") [デザインパターン](https://ja.wikipedia.org/wiki/デザインパターン "wikilink")に緩やかに従う。 もともとは[ローレンス (カンザス州)にある](https://ja.wikipedia.org/wiki/ローレンス_\(カンザス州\) "wikilink") World Company\[1\] のために、ニュース系のサイトを管理する目的で開発され、[2005年](../Page/2005年.md "wikilink")7月に [BSD License](https://ja.wikipedia.org/wiki/BSD_License "wikilink") で公式にリリースされた。フレームワークは[ジプシー・スウィング](https://ja.wikipedia.org/wiki/ジプシー・スウィング "wikilink")のギタリストである[ジャンゴ・ラインハルト](../Page/ジャンゴ・ラインハルト.md "wikilink")にちなんで命名された。

Django の第一の目的は、複雑なデータベース主体の Web サイトの構築を簡単にすることである。Django はコンポーネントの再利用性と'pluggability'、素早い開発、[DRY (Don't Repeat Yourself)の原則に力点を置いている](../Page/Don't_repeat_yourself.md "wikilink")。ファイルやデータのモデルにいたるまで、[Python](../Page/Python.md "wikilink") が一貫して用いられている。

Django はまた、動的に生成され、データモデルの定義を通じて完全に構成することができる、データベース管理 [CRUD](../Page/CRUD.md "wikilink") インターフェイスをオプションで提供する。

Python3系統にはDjango 1.5バージョンで実験的に対応し、Django 1.6より本格的に対応した\[2\]\[3\]。

Python2系統への対応は、バージョン1.11(3年サポートのLTS、2020年4月まで)が最後となり、2.0でPython3.4以降、2.1でPython3.5以降にのみの対応となった\[4\]。

## Djangoのコンポーネント

Django フレームワークのコア部分は [データモデル](../Page/データモデル.md "wikilink")（Python クラスとして定義される）と[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")との間を仲介する [O/R マッパー](../Page/オブジェクト関係マッピング.md "wikilink")、 [正規表現](../Page/正規表現.md "wikilink")に基づく [URL](../Page/Uniform_Resource_Locator.md "wikilink") ディスパッチャ、要求を処理するビューシステム、 [テンプレートシステムから構成される](https://ja.wikipedia.org/wiki/テンプレートエンジン#ウェブテンプレートエンジン "wikilink")。

そのほか、下記のものがコアのフレームワークに含まれる:

  - 開発とテストのための軽量のスタンドアロン Web サーバ
  - [HTMLフォームをデータベースに格納できる値に変換するフォームのシリアル化と検証システム](../Page/HyperText_Markup_Language.md "wikilink")
  - 複数のキャッシュ方法に対応した[キャッシュフレームワーク](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")
  - 要求を処理するさまざまな段階に挿入し、カスタムの処理を実行できる[ミドルウェア](../Page/ミドルウェア.md "wikilink")クラスのサポート
  - アプリケーションのコンポーネントがあらかじめ定義されたシグナルを用いてイベント通信できるようにする内部ディスパッチャシステム
  - [国際化の機構](../Page/国際化と地域化.md "wikilink")(Django 自身のコンポーネントも多数の言語へ翻訳されている)
  - Django モデルのインスタンスを [XML](../Page/Extensible_Markup_Language.md "wikilink") および [JSON](../Page/JavaScript_Object_Notation.md "wikilink") に対して入出力可能なシリアル化機構
  - テンプレートエンジンの機能を拡張する機構

## バンドルされるアプリケーション

Django の公式配布物は、"contrib"パッケージ内に多数のアプリケーションを含んでいる。

  - 拡張可能な認証機構
  - 動的な管理インターフェイス
  - [RSS](../Page/RSS.md "wikilink") と [Atom](../Page/Atom_\(ウェブコンテンツ配信\).md "wikilink") 配信用のフィードを生成するツール
  - 柔軟なコメントシステム
  - [Google Sitemaps](https://ja.wikipedia.org/wiki/Google_Sitemaps "wikilink") を生成するツール
  - CSRF([cross-site request forgery](../Page/クロスサイトリクエストフォージェリ.md "wikilink"))を防止するためのツール
  - [Textile](https://ja.wikipedia.org/wiki/Textile "wikilink") や [Markdown](https://ja.wikipedia.org/wiki/Markdown "wikilink") などの [軽量マークアップ言語](../Page/軽量マークアップ言語.md "wikilink") の使用が可能なテンプレートライブラリ

## サーバ構成

Django は [Apache 2](../Page/Apache_HTTP_Server.md "wikilink") で [mod python](https://ja.wikipedia.org/wiki/mod_python "wikilink") を使って、あるいは任意の [WSGI](../Page/Web_Server_Gateway_Interface.md "wikilink") 準拠のウェブサーバで動作させることができる。[Nginx](https://ja.wikipedia.org/wiki/Nginx "wikilink")とuWSGIでも動作が可能となっている。 Django は [FastCGI](../Page/FastCGI.md "wikilink") サーバを起動することができ、FastCGI をサポートする任意のウェブサーバのバックエンドで使用することができる。

以下のデータベースが、Django での使用を公式にサポートされている。

  - [PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")
  - [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")
  - [SQLite](../Page/SQLite.md "wikilink")
  - [Oracle](../Page/Oracle_Database.md "wikilink")

サードパーティから、[Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink") 用のアダプター [Django MSSQL](https://django-mssql.readthedocs.io/en/latest/)、 [IBM DB2](https://ja.wikipedia.org/wiki/IBM_DB2 "wikilink") 用のアダプター [ibm_db](http://code.google.com/p/ibm-db/) に加え、SAP SQL Anywhere、[ODBC](../Page/Open_Database_Connectivity.md "wikilink")、[Firebird](../Page/Firebird.md "wikilink")へのアダプターも提供されている。

## The Django Book

The Django Book は、 Django についての [GNU Free Documentation License](../Page/GNU_Free_Documentation_License.md "wikilink") でライセンスされたフリーの書籍である。 2007年12月、[Apress](https://ja.wikipedia.org/wiki/Apress "wikilink") によって出版された。書籍は <http://www.djangobook.com/> で入手できる。

## 脚注

## 外部リンク

  - [公式サイト（英語）](http://www.djangoproject.com/)
  - [The Django Book（英語）](http://www.djangobook.com/)
  - [The Django Book（日本語）](http://djangobook-ja.appspot.com/)
  - [djangoproject.jp](http://djangoproject.jp/) 日本のユーザコミュニティ
  - [日本Djangoのインストーラ](http://bitnami.org/stack/djangostack)
  - [Toptal - Top 10 Mistakes that Django Developers Make](https://www.toptal.com/django/django-top-10-mistakes)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Python](https://ja.wikipedia.org/wiki/Category:Python "wikilink") [Category:ウェブアプリケーションフレームワーク](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーションフレームワーク "wikilink")

1.  [LJWorld.com / About us](http://www2.ljworld.com/about)
2.
3.
4.