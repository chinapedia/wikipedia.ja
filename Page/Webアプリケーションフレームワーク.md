> この記事は[Webアプリケーションフレームワーク](https://ja.wikipedia.org/wiki/Webアプリケーションフレームワーク)から翻訳されています。


**Web アプリケーションフレームワーク**（ウェブアプリケーションフレームワーク、[英](../Page/英語.md "wikilink"): *Web Application Framework*）は、動的な [ウェブサイト](../Page/ウェブサイト.md "wikilink")、[Webアプリケーション](https://ja.wikipedia.org/wiki/Webアプリケーション "wikilink")、[Webサービス](../Page/Webサービス.md "wikilink")の[開発をサポートするために設計された](../Page/Webプログラミング.md "wikilink")[アプリケーションフレームワーク](../Page/アプリケーションフレームワーク.md "wikilink")である。 フレームワークの目的は、Web開発で用いられる共通した作業に伴う労力を軽減することである。たとえば、多数のフレームワークが[データベース](../Page/データベース.md "wikilink")へのアクセスのためのライブラリや、[テンプレートエンジン](../Page/テンプレートエンジン.md "wikilink")（→[Webテンプレート](https://ja.wikipedia.org/wiki/Webテンプレート "wikilink")）、[セッション](../Page/セッション.md "wikilink")管理を提供し、[コードの再利用](https://ja.wikipedia.org/wiki/コードの再利用 "wikilink")を促進させるものもある。

## Webアプリケーションフレームワークの発展

### Common Gateway Interface (CGI)

[World Wide Webの設計は元々ダイナミックなものではなく](../Page/World_Wide_Web.md "wikilink")、初期の[ハイパーテキスト](../Page/ハイパーテキスト.md "wikilink")は [Webサーバ](../Page/Webサーバ.md "wikilink")上で公開された[ハードコード](https://ja.wikipedia.org/wiki/ハードコード "wikilink")の[HTMLでできていた](../Page/HyperText_Markup_Language.md "wikilink")。

公開されたページについての変更はページの作者が行う必要があった。 ユーザーからの入力を反映したコンテンツを提供するため、Webサーバが外部のアプリケーションとやり取りするための[Common Gateway Interface](../Page/Common_Gateway_Interface.md "wikilink") (CGI) 標準が導入された。 \[1\] CGIでは各リクエストが別々のプロセスを開始しなければならないため、サーバの負荷に悪い影響を与えることがある。

### 密結合

高いトラフィックに対応したWebアプリケーションを実現するため、[プログラマ](../Page/プログラマ.md "wikilink")はWebサーバとの密な結合を望んだ。[Apache HTTP Serverは](../Page/Apache_HTTP_Server.md "wikilink")、例えば、Webサーバが任意のコードを実行したり（[mod_python](https://ja.wikipedia.org/wiki/mod_python "wikilink")など）、特定のリクエストを動的なコンテンツを扱えるWebサーバに転送するような（など）モジュールをサポートしている。[Java](https://ja.wikipedia.org/wiki/Java "wikilink")などの言語で書かれた動的なコンテンツをWebサーバで扱うことができるよう設計されたものもある（[Apache Tomcatなど](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink")） 。

### Web言語

同じころWeb用途に特化して[PHPや](../Page/PHP_\(プログラミング言語\).md "wikilink")[Active Server Pagesなどの新しい言語が開発された](../Page/Active_Server_Pages.md "wikilink")。

### Webライブラリ

Webページの動的な生成に用いられる大半のプログラミング言語が、共通した作業を行うための[ライブラリ](../Page/ライブラリ.md "wikilink")を持っているが、[Webアプリケーションは](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink") [HTMLの生成](../Page/HyperText_Markup_Language.md "wikilink")（たとえば [JavaServer Faces](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink")）などWebアプリケーションで有用なライブラリを必要とすることが多い。

### フルスタック

成熟した「フルスタック」フレームワークが登場した。 これは、複数のWeb開発に有用なライブラリを一つに結合した Web開発者向けの [ソフトウェアスタック](https://ja.wikipedia.org/wiki/ソフトウェアスタック "wikilink")として集約したものである。 例として、[JavaEE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")、[OpenACS](https://ja.wikipedia.org/wiki/OpenACS "wikilink")、[Ruby on Railsなどがある](../Page/Ruby_on_Rails.md "wikilink")。

### ポートレット

従来のフレームワークは基本的に横型に分割されているため、ユーザ機能を追加 / 変更 / 削除する場合は、アプリケーションを入れ替える必要があった。ポータルフレームワークはユーザ機能を縦型に分割し、ユーザ機能毎にホット・デプロイ / アンデプロイできる。デプロイされた[ポートレット](../Page/ポートレット.md "wikilink")をドラッグ・アンド・ドロップ操作でWebページに配置することができるのが特徴である。

なお、ポートレット毎にエンティティインターフェース（モデル）、表示（ビュー）、業務ロジックが含まれているため、ポートレット毎に異なるスタック技術を利用することもできる。例えば[JSFで作成したポートレットと](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink")[Spring Frameworkで作成したポートレットを](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink")１つのWebページに配置することができる。また、異なった言語でポートレットを記述することもできる。例えばJava、Ruby、PHPで記述したポートレットを一つのWebページに配置できる。

ユーザ機能を随時に追加／置き換え／削除することができるため、ポートレットフレームワークはアジャイル開発のように継続的に開発を行う場合に適している。例えばScrumの各ユーザストリーをプラグインにすることができる。

ポートレットフレームワークを利用したWebシステムの例として、[liferay](https://ja.wikipedia.org/wiki/liferay "wikilink")、[Alfresco](https://ja.wikipedia.org/wiki/Alfresco "wikilink")などがある。その中で[liferay](https://ja.wikipedia.org/wiki/liferay "wikilink")は開発者向けのツールが揃っている。

## アーキテクチャ

### Model view controller

多数のフレームワークが、[データモデル](../Page/データモデル.md "wikilink")、[ビジネスロジック](../Page/ビジネスロジック.md "wikilink")、[ユーザーインターフェイス](https://ja.wikipedia.org/wiki/ユーザーインターフェイス "wikilink")を分割するために[MVCモデルに従っている](../Page/Model_View_Controller.md "wikilink")。

#### プッシュ型とプル型の比較

ほとんどのMVCフレームワークは、[プッシュ型のアーキテクチャにしたがっている](https://ja.wikipedia.org/wiki/Push技術 "wikilink")。このようなフレームワークは、処理を要求するアクションを実行し、次に結果を出力するためにデータを表示のレイヤにプッシュする。 \[2\] [Struts](https://ja.wikipedia.org/wiki/Struts "wikilink")、[Django](../Page/Django.md "wikilink")、[Ruby on Rails](../Page/Ruby_on_Rails.md "wikilink")、[Spring Frameworkの一部であるSpring](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink") MVCなどがこのアーキテクチャの良い例である。

これに対するものとしてプル型のアーキテクチャがあり、「コンポーネント型」とも呼ばれている。こうしたフレームワークは表示レイヤから処理を開始し、必要に応じて複数のコントローラからの処理の結果を「プル」する。 このアーキテクチャでは、複数のコントローラーが一つのビューに関連付けられる。 [Tapestry](../Page/Apache_Tapestry.md "wikilink")、[Velocity](../Page/Apache_Velocity.md "wikilink") などがプル型アーキテクチャの一例である。

### コンテンツ管理システム

自己記述的なコンテンツ管理システムが、高位のレイヤーのWebアプリケーションフレームワークに進出し始めている。 例えば、[Drupal](../Page/Drupal.md "wikilink")の構造は Webアプリケーションフレームワークに関連した機能を提供する*モジュール*により機能を拡張できる最小限の*コア*を提供している。 [WordPress](../Page/WordPress.md "wikilink")、[Joomlaと](https://ja.wikipedia.org/wiki/Joomla! "wikilink")[Plone](https://ja.wikipedia.org/wiki/Plone "wikilink")も同様な機能を持っている。 [Liferay](https://ja.wikipedia.org/wiki/Liferay "wikilink")（オープンソース）のような高度な汎用コンテンツ管理システムでは、更にコンテンツのバージョン管理、公開開始日／終了日、公開する前の承認ワークフロー、プレビュー機能、マルチメディアコンテンツの対応など従来では[WebSphere](../Page/WebSphere.md "wikilink")や[Microsoft SharePointなどでしか提供されていない機能にも対応している](../Page/Microsoft_SharePoint.md "wikilink")。 伝統的にこれらは [コンテンツ管理システム](../Page/コンテンツ管理システム.md "wikilink")とも呼ばれる。 しかし、コンテンツの管理がこれらのシステムの上で最重要の機能であるかについては議論の余地がある。[Liferay](https://ja.wikipedia.org/wiki/Liferay "wikilink")のようなフレームワークは関数API、機能のフレームワークやコーディング標準、伝統的に*Webアプリケーションフレームワーク*に関連する機能も提供している。

## 機能

### セキュリティ

Webアプリケーションフレームワークにはアクセス制御機能（[ユーザ認証と](../Page/認証.md "wikilink")[アクセス認可](https://ja.wikipedia.org/wiki/認可_\(セキュリティ\) "wikilink")）を備えたものもある。 [Django](../Page/Django.md "wikilink")はその一例で、ロールに基づいてページに対するアクセスを管理する機能と、ユーザーの作成やロールの割り当てのためのWebベースのインターフェイスを提供する。

### データベースへのアクセスおよびマッピング

多数のWebアプリケーションフレームワークはバックエンドのデータベースに対する統一された[APIを提供し](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、コードの変更なく多数のデータベースとやりとりすることを可能にし、プログラマーがより高位の概念を扱うことができるようにしている。 また高いパフォーマンスを得るため、[AOLserverが行うようにデータベースのコネクションがプールされていなければならない](https://ja.wikipedia.org/wiki/:en:AOLserver "wikilink")。

さらに、[オブジェクト指向フレームワークは](../Page/オブジェクト指向プログラミング.md "wikilink")[オブジェクトと](../Page/オブジェクト指向プログラミング.md "wikilink")[関係モデル](../Page/関係モデル.md "wikilink")との対応づけを行う[オブジェクト関係マッピング](../Page/オブジェクト関係マッピング.md "wikilink")の機能を提供するマッピングツールを備えている。

Webアプリケーションフレームワークが提供するその他の機能として[トランザクション](../Page/トランザクション.md "wikilink")のサポートや[データベースの移行ツールなどが含まれる](https://ja.wikipedia.org/wiki/データ移行 "wikilink")。

### URLマッピング

パラメータの付加されたURLをわかりやすいURLに自動的に変換することにより、システムは使いやすく、またさらなる利点としてサーチエンジンがインデックスを作りやすくなる。 たとえば、?cat=1\&pageid=3で終わるようなアドレスを/category/science/topic/physicsや/science/physicsへの変換するような例である。 カテゴリーのIDが変更されてもURLは変わらない（従ってサーチエンジンに対して有利である）。URLの変換により、アプリケーションが[REST的な設計方法の一部の要素によりうまく適合できるようにすることができる](../Page/Representational_State_Transfer.md "wikilink")。

### Webテンプレートシステム

動的なWebページは通常静的な部分 (HTML) とHTMLを生成するコードである動的な部分からなる。HTMLを生成するコードはテンプレート上の変数あるいはコードから生成を行う。生成されるテキストをデータベースから取得することで、サイト内のページの数を劇的に少なくすることができる。

例として 500軒の家を扱う不動産会社を考える。静的なWebサイトでは、不動産会社は500ページ作成する必要があるが、動的なWebサイトでは、不動産会社はただ動的なページを500レコードを持つデータベースに接続するだけでよい。

[テンプレートでは](https://ja.wikipedia.org/wiki/Webテンプレート "wikilink")、プログラミング言語由来の変数を、コードを使わずに挿入することができるため、Webサイト内のページを更新するためにプログラミングの知識が必要なくなる。 HTMLと変数を区別するための記述方法が定義されており、たとえばJSPでは <c:out> タグが変数を出力するために使用され、Smartyでは{$variable} が用いられる。

多数のテンプレートエンジンはIFやFOREACHといった若干の論理タグをサポートしている。 これらはビジネスロジック層ないしMVCパターンにおけるM（モデル）との明確な分離を行うため、プレゼンテーション層に必要な決定を行うためだけに用いられる。

### キャッシュ

Webのキャッシングとは、[帯域使用率](../Page/帯域幅.md "wikilink")、[Webサーバ](../Page/Webサーバ.md "wikilink")の負荷、ユーザーに感じられる“[ラグ](../Page/ラグ.md "wikilink")”を削減するための [Web](../Page/World_Wide_Web.md "wikilink")[文書の](../Page/電子文書.md "wikilink")[キャッシングである](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")。Webキャッシュシステムは、ドキュメントのコピーを保存し、以降のリクエストは一定の条件が満たされればキャッシュから供給すれば問題なくなる。アプリケーションフレームワークには文書をキャッシュし、Webテンプレートシステムをバイパスする機構を提供するものもある。

### Ajax

[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")とはインタラクティブな[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")を作成するための[Web開発手法である](../Page/Webプログラミング.md "wikilink")。Ajaxの目的はユーザーが変更を要求するごとにWebページ全体がリロードされないようにするため、背後でサーバとのデータのやり取りを少なくし、Webページをより高速に反応するようにすることである。Webページのインタラクティブ性や、速度、[ユーザビリティ](../Page/ユーザビリティ.md "wikilink")を向上させることが意図されている。

Ajaxプログラミングは複雑であるため、Ajaxサポートを専門に行うAjax フレームワークが多数存在している。 他の大きなフレームワークの一部として組み込むことができるものも存在する。 たとえば、[Prototype JavaScript Frameworkは](https://ja.wikipedia.org/wiki/Prototype_JavaScript_Framework "wikilink")[Ruby on Railsに含まれている](../Page/Ruby_on_Rails.md "wikilink")。

### 自動構成

フレームワークには[型システム](../Page/型システム.md "wikilink")を利用したや以下の方法を用いてによってWebアプリケーションの構成作業をできる限り少なくするものがある。 たとえば、多数のJavaフレームワークは[Hibernate](../Page/Hibernate.md "wikilink")を永続化層として使用しており、必要な情報を永続化させるためのデータベーススキーマをランタイムに生成することができる。 これによりアプリケーションの設計者は明示的にデータベーススキーマを設計せずにビジネスオブジェクトを設計することができる。 [Ruby on Railsのようなフレームワークは逆の動作](../Page/Ruby_on_Rails.md "wikilink")、すなわちモデルオブジェクトのプロパティをデータベーススキーマに基づきランタイムに定義することが可能である。

### Webサービス

[Webサービス](../Page/Webサービス.md "wikilink")の作成と提供を行うツールを提供するツールを備えたフレームワークもある。 これらのユーティリティは、その他のWebアプリケーションと同様の機能を提供する。

## 技術

### プログラミング言語

多数のプログラミング言語に対して関連したWebアプリケーションフレームワークが存在する。 しかし、フレームワークに対するより高いレベルのサポートやフレームワークの開発に導く機能を提供したり十分な数の開発者がいる言語もあれば、そうでないものもある。

#### Java

膨大な数のJavaフレームワークが開発中、ないしは実際に使用されている。 これらのフレームワークの多くは[Java EEプラットフォームの上に構築されているか](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")、ないしは要素を借りてきている。

#### JavaScript

[Javascript framework](https://ja.wikipedia.org/wiki/Javascript_framework "wikilink")、[JavaScriptライブラリ](https://ja.wikipedia.org/wiki/JavaScriptライブラリ "wikilink")（[JavaScript library](https://ja.wikipedia.org/wiki/JavaScript_library "wikilink")）、[AJAX frameworkなどと呼ばれる](https://ja.wikipedia.org/wiki/AJAX_framework "wikilink")。 全世界に普及した成功例として代表的なものに [Prototype JavaScript Frameworkや](https://ja.wikipedia.org/wiki/Prototype_JavaScript_Framework "wikilink")[JQuery](https://ja.wikipedia.org/wiki/JQuery "wikilink")がある。 これ以外にもさまざまなものが開発されている。以下はその一例である。HTML,CSS,JavaScriptの進化が著しく、JavaScriptでは種々のフレームワークが乱立している状態であるが、

  - [AngularJS](https://ja.wikipedia.org/wiki/AngularJS "wikilink")(1.x,2.0α Ver)
  - [Aurelia.js](https://ja.wikipedia.org/wiki/Aurelia.js "wikilink")
  - [Backbone.js](https://ja.wikipedia.org/wiki/Backbone.js "wikilink")
  - [Ember.js](https://ja.wikipedia.org/wiki/Ember.js "wikilink")
  - [Knockout.js](https://ja.wikipedia.org/wiki/Knockout.js "wikilink")
  - [MooTools](https://ja.wikipedia.org/wiki/MooTools "wikilink")
  - [Polymer](https://ja.wikipedia.org/wiki/Polymer "wikilink")
  - [Ractive.js](https://ja.wikipedia.org/wiki/Ractive.js "wikilink")
  - [React.js](https://ja.wikipedia.org/wiki/React.js "wikilink")
  - [Riot.js](https://ja.wikipedia.org/wiki/Riot.js "wikilink")
  - [Vue.js](https://ja.wikipedia.org/wiki/Vue.js "wikilink")

#### C\#およびVB.NET

C\#および VB.NET は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の言語非依存の[ASP.NET](../Page/ASP.NET.md "wikilink")プラットフォーム上で最も人気のある言語である。 初期には最も人気のあるWebアプリケーションフレームワークは Webアプリケーションフレームワークであった。 [ASP.NET](../Page/ASP.NET.md "wikilink")自体はWebアプリケーションを構築するために設計された技術であるため、誤ってWebアプリケーションフレームワークとしてのみ参照されることがある。 これは、ASP.NETの一面に過ぎない。Webアプリケーションフレームワークとしての基本機能に加えて、[.NET Frameworkを採用する好みの言語を選ぶことができる](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。 ASP.NETは統合されたAJAXフレームワークである[ASP.NET](../Page/ASP.NET.md "wikilink")における[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")実装であるを備えている。

#### PHP

PHPの動的なWebページに向けた設計により、[CakePHP](../Page/CakePHP.md "wikilink")、[Symfony](https://ja.wikipedia.org/wiki/Symfony "wikilink")、[Zend Framework](https://ja.wikipedia.org/wiki/Zend_Framework "wikilink")、[FuelPHP](https://ja.wikipedia.org/wiki/FuelPHP "wikilink")、[CodeIgniter](../Page/CodeIgniter.md "wikilink")、[Yii](https://ja.wikipedia.org/wiki/Yii "wikilink")、[PRADO](https://ja.wikipedia.org/wiki/PRADO_\(フレームワーク\) "wikilink")、[Laravel](https://ja.wikipedia.org/wiki/Laravel "wikilink")、[eZ Publishなどのフレームワークが支持を得ている](https://ja.wikipedia.org/wiki/eZ_Publish "wikilink")。 これらのフレームワークは、コア言語の上にフレームワーク層を適用することにより、アプリケーションの構造とモデル化を支援する。 これらは、ボトムアップからのプログラミングについての問題に対向するものである。

上記のフレームワークとは逆に、[Magento](../Page/Magento.md "wikilink")、[MODx](https://ja.wikipedia.org/wiki/MODx "wikilink")、[Drupal](../Page/Drupal.md "wikilink")、[Joomla\!](https://ja.wikipedia.org/wiki/Joomla! "wikilink")、[TYPO3](../Page/TYPO3.md "wikilink")といったソフトウェアプロジェクトは、Web[コンテンツ管理システム](../Page/コンテンツ管理システム.md "wikilink")からより上位のWebアプリケーションフレームワークへと変貌し始めている。 これらの構造は、Webアプリケーションフレームワークに関連した機能を提供する*モジュール*により機能を拡張できる最小限の*コア*を提供している。

[オープンソース](../Page/オープンソース.md "wikilink")のプロジェクトとしてコミュニティが多数のモジュールを寄贈しており（たとえば[Drupal](../Page/Drupal.md "wikilink")は1,000以上、Typo3には2,500以上のモジュールがある）、CMSのコア＋モジュールを用いて、広い範囲の機能を持ったWebサイトを、実際にはPHPレベルのコーディングを行わずに組み立てる方法が形作られている。

#### Perl, Python, Ruby

動的な言語によるフレームワークが多数存在する。

Perlには[Catalyst](../Page/Catalyst_\(ソフトウェア\).md "wikilink")、[Ark](https://ja.wikipedia.org/wiki/Ark "wikilink")、[Mojolicious](https://ja.wikipedia.org/wiki/Mojolicious "wikilink")などのフレームワークがある。

Pythonには、たとえば[Django](../Page/Django.md "wikilink")、[TurboGears](../Page/TurboGears.md "wikilink")、[Pylons](../Page/Pylons.md "wikilink")、[Quixote](https://ja.wikipedia.org/wiki/:en:Quixote_\(web_framework\) "wikilink")、[Karrigell](https://ja.wikipedia.org/wiki/:en:Karrigell "wikilink")、[web2py](http://mdp.cti.depaul.edu)などのフレームワークが存在する。ほぼ完全なリストとしてこの[リスト](http://wiki.python.org/moin/WebFrameworks)がある。

Rubyには[Merb](https://ja.wikipedia.org/wiki/Merb "wikilink")、[Ruby on Railsといったフレームワークがある](../Page/Ruby_on_Rails.md "wikilink")。

### オペレーティングシステム

ごくわずかの例外はあるが、Webアプリケーションフレームワークは多数のプラットフォームで動作する、プラットフォーム非依存の言語の上に作られている。

特定の構成を推奨するフレームワークもあるが、大半のものは [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Linux](../Page/Linux.md "wikilink")などの[Unix系](../Page/Unix系.md "wikilink")のプラットフォーム上で動作する。 特筆すべき例外として、[.NETのために書かれた](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[DotNetNukeは](https://ja.wikipedia.org/wiki/:en:DotNetNuke "wikilink")[Monoランタイムをサポートしていない](../Page/Mono_\(ソフトウェア\).md "wikilink")。

## 参考文献

<references/>

  - Tony Shan and Winnie Hua (2006). [*Taxonomy of Java Web Application Frameworks*](http://doi.ieeecomputersociety.org/10.1109/ICEBE.2006.98). Proceedings of the 2006 IEEE International Conference on e-Business Engineering (ICEBE 2006), October 2006, p378-385.

## 関連項目

  - [:Category:ウェブアプリケーションフレームワーク](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーションフレームワーク "wikilink")
  - [ソフトウェアフレームワーク](https://ja.wikipedia.org/wiki/ソフトウェアフレームワーク "wikilink")
  - [アプリケーションフレームワーク](../Page/アプリケーションフレームワーク.md "wikilink")
  - [Don't repeat yourself](https://ja.wikipedia.org/wiki/Don't_repeat_yourself "wikilink") (DRY原則)

[Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink") [Category:ソフトウェアアーキテクチャ](https://ja.wikipedia.org/wiki/Category:ソフトウェアアーキテクチャ "wikilink") [Category:ウェブアプリケーション](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーション "wikilink") [Category:ウェブアプリケーションフレームワーク](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーションフレームワーク "wikilink") [Category:ウェブサイトの構成](https://ja.wikipedia.org/wiki/Category:ウェブサイトの構成 "wikilink")

1.
2.