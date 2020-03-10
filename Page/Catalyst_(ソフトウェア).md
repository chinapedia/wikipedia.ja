> この記事は[Catalyst \(\)](https://ja.wikipedia.org/wiki/Catalyst_\(\))から翻訳されています。


**Catalyst** （かたりすと）は、[Perl](../Page/Perl.md "wikilink")で書かれた[オープンソース](../Page/オープンソース.md "wikilink")の[ウェブアプリケーションフレームワークで](https://ja.wikipedia.org/wiki/Webアプリケーションフレームワーク "wikilink")、[Model View Controller](https://ja.wikipedia.org/wiki/Model_View_Controller "wikilink") (MVC)のアーキテクチャを持ち、実験的なウェブのパターンを数多く持っている。[Ruby on Rails](https://ja.wikipedia.org/wiki/Ruby_on_Rails "wikilink")、 [Maypole](https://ja.wikipedia.org/wiki/Maypole_framework "wikilink")、 [Springといったフレームワークに強い影響を受けている](https://ja.wikipedia.org/wiki/Spring_framework "wikilink")。

Catalystは、主に、Perlのライブラリやアプリケーションの公式配布元である[CPAN](https://ja.wikipedia.org/wiki/CPAN "wikilink")を通じて配布される。

## 哲学

Catalystは、定義は一度のみ行われるべきとする"[Don't Repeat Yourself](https://ja.wikipedia.org/wiki/Don't_repeat_yourself "wikilink")" (DRY)原則に基づいている。

Catalystは、多くのモジュールのうちからひとつだけを使って、データベースからクラスを引っ張り出すことによって利用される。従って、データベース層に関するコードは必要とされない。しかし、何かに付け融通を効かせようとするなら、それもオプションで利用できる。Catalystのもうひとつの原則は、自在さである。

Catalystは、既にウェブアプリケーションを操作するために使われている既存のPerlモジュールの再利用を促す。

  - **Model**部分は、*DBIx::Class*、*Plucene*、*Net::LDAP*、またはほかのモデルクラスを通じて操作する。
  - **View**部分は、*[Template Toolkit](https://ja.wikipedia.org/wiki/Template_Toolkit "wikilink")*、*Mason*、または*HTML::Template*によって主に操作される。
  - **Controller**は、もちろん個々のアプリケーションの作者によって書かれる。Controller機能の大部分は、Catalystのプラグインのうちのひとつに委ねることが出来る（Catalyst::Plugin::FormValidator、 Catalyst::Plugin::Prototype、 Catalyst::Plugin::Account::AutoDiscoveryなど）。

Catalystには、多くのプラグインがある\[1\]。例えば、[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")や[RIAのための](https://ja.wikipedia.org/wiki/Rich_Internet_application "wikilink")[JavaScript](../Page/JavaScript.md "wikilink")の生成には、Catalyst::Plugin::Prototypeモジュールが使われる（[prototypeはAjaxフレームワークである](https://ja.wikipedia.org/wiki/Prototype_JavaScript_Framework "wikilink")）。

## Webサーバのサポート

開発やテストのために、Catalystは、組み込みの簡易HTTPサーバがある。製品の利用については[Apacheか](../Page/Apache_HTTP_Server.md "wikilink")、[FastCGI](https://ja.wikipedia.org/wiki/FastCGI "wikilink")付きの[lighttpd](https://ja.wikipedia.org/wiki/lighttpd "wikilink")、 [mod perlサポートが推奨されるが](https://ja.wikipedia.org/wiki/mod_perl "wikilink")、[CGIやFastCGIをサポートした](../Page/Common_Gateway_Interface.md "wikilink")[Webサーバ](../Page/Webサーバ.md "wikilink")なら動作する。Apache上では、mod_perlでの利用が、相当のパフォーマンスの助けになるが、複数のアプリケーションでmod_perlを共有することで不安定になるため、問題もある。

## データベースサポート

Catalystは、PerlのDBIがサポートする[データベース](../Page/データベース.md "wikilink")なら（つまりほぼ全て、[CSVファイルでさえも](../Page/Comma-Separated_Values.md "wikilink")）どれでも動作するが、[関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink") (RDBMS) が推奨されている。データベースアクセスは、モジュールのひとつを通し、全てのデータベースへのアクセスを自動的に操作することで、プログラマーやCatalystからは、完全に抽象化されている。もし必要なら、ダイレクトに[SQL](../Page/SQL.md "wikilink")のクエリを利用することもできる。これは、異なるデータベース間でも移植性のある、データベースにおいて中立的なアプリケーションが利用でき、Catalystアプリケーション開発において、可能な限り、既存のデータベースのユーザビリティを保つことが出来ることを意味する。ただし、RDBMS間で機能が異なる場合には、フレームワーク単独では、完全に機能を保証できない。[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")、[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")、[SQLite](https://ja.wikipedia.org/wiki/SQLite "wikilink")、[IBM DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")、[Oracle](../Page/Oracle_Database.md "wikilink")、[Microsoft SQL Serverといった複数のデータベースをサポートしている](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")。（[オブジェクト関係マッピング](https://ja.wikipedia.org/wiki/オブジェクト関係マッピング "wikilink")）

## Catalystを使って作られたウェブサイト

  - [iusethis](http://osx.iusethis.com/) - 利用パターンを元にしたソフトウェアのサイト
  - [MightyV](http://www.mightyv.com) - BBCのTV-program listingを受賞した
  - [Vox](../Page/Vox_\(ブログ\).md "wikilink") - ソーシャルブログプラットフォーム
  - [EditGrid](https://ja.wikipedia.org/wiki/EditGrid "wikilink") - ウェブベースの表計算
  - [ボケて](http://bokete.jp/) - 写真で一言ボケることに特化したウェブサービス

## Catalystを使って作られたオープンソースソフトウェア

  - [Agave (software)](https://ja.wikipedia.org/wiki/Agave_\(software\) "wikilink") （ブログ）
  - [Angerwhale](https://ja.wikipedia.org/wiki/Angerwhale "wikilink") （ブログ） [Trac Site](http://www.jrock.us/trac/blog_software)
  - *Devel::ebug* （Perlのデバッガ） [CPANのサイト](http://search.cpan.org/dist/Devel-ebug/)
  - [Handel (software)](https://ja.wikipedia.org/wiki/Handel_\(software\) "wikilink") (commerce framework) [サイト](http://handelframework.com/)
  - [Meios](https://ja.wikipedia.org/wiki/Meios "wikilink")
  - [MojoMojo](https://ja.wikipedia.org/wiki/MojoMojo "wikilink") （ウィキ）
  - [Sosa (software)](https://ja.wikipedia.org/wiki/Sosa_\(software\) "wikilink")

## Perlで記述された他のフレームワーク

  - [Sledge](https://ja.wikipedia.org/wiki/Sledge "wikilink") - ライブドアによって開発されたフレームワーク
  - [Mojolicious](https://ja.wikipedia.org/wiki/Mojolicious "wikilink") - Catalyst作者による次世代Webフレームワーク [サイト](http://mojolicious.org/)

## 脚注

<references/>

## 外部リンク

  - [プロジェクトホームページ](http://catalystframework.org/)
  - [Perl5とCatalystで作られている](http://www.dev411.com/blog/2006/09/05/perl-5-powering-web-2.0)
  - [PerlNet](http://perl.net.au/)上の[Catalystの記事](http://perl.net.au/wiki/Catalyst)
  - [CPANのCatalyst](http://search.cpan.org/dist/Catalyst-Runtime/)
  - [Planet Catalyst](http://planet.catalystframework.org/)

[Category:ウェブアプリケーション](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーション "wikilink") [Category:Perl](https://ja.wikipedia.org/wiki/Category:Perl "wikilink")

1.  [CPANにおけるCatalystのモジュール](http://search.cpan.org/search?query=Catalyst%3A%3APlugin%3A%3A&mode=module)