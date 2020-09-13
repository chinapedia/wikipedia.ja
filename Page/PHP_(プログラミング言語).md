> この記事は[PHP \(プログラミング言語\)](https://ja.wikipedia.org/wiki/PHP_\(プログラミング言語\))から翻訳されています。


`| latest release version = 7.4.9`\[1\]
`| latest release date    = `
`| latest preview version = 8.0.0 beta 2`\[2\]
`| latest preview date    = `
`| typing                 = 弱い`[`動的型付け`](../Page/動的型付け.md "wikilink")
`| implementations        = `[`PHP`](https://php.net/)`, `[`HHVM`](https://ja.wikipedia.org/wiki/HHVM "wikilink")`, `[`Phalanger`](https://ja.wikipedia.org/wiki/Phalanger "wikilink")
`| dialects               = `[`Hack`](https://ja.wikipedia.org/wiki/Hack_\(プログラミング言語\) "wikilink")
`| influenced             =`
`| programming language   =`
`| wikibooks              = PHP`

}}  **PHP**（ピー・エイチ・ピー）は "The PHP Group" によってコミュニティベースで開発\[3\]されているオープンソースの汎用[プログラミング言語](../Page/プログラミング言語.md "wikilink")およびその[公式の処理系であり](../Page/リファレンス実装.md "wikilink")、特にサーバーサイドで動的な[ウェブページ](../Page/ウェブページ.md "wikilink")作成するための機能を多く備えていることを特徴とする\[4\]。 名称の **PHP** は[再帰的頭字語](../Page/再帰的頭字語.md "wikilink")として、 "" を意味\[5\]\[6\]するとされており、「PHPは[HTML](https://ja.wikipedia.org/wiki/HTML "wikilink")の[プリプロセッサ](../Page/プリプロセッサ.md "wikilink")である」とPHP自身を再帰的に説明している。

## 概要

PHPは[ラスマス・ラードフ](https://ja.wikipedia.org/wiki/ラスマス・ラードフ "wikilink")が個人的に[Cで開発していた](../Page/C言語.md "wikilink")[CGIプログラムである](../Page/Common_Gateway_Interface.md "wikilink") "" （短縮されて "" と呼ばれていた）を起源とする\[7\]。 元々はラードフ自身のWebサイトで簡単な動的Webページを作成するために用いられていたが、その後データベースへのアクセス機能などを追加したPHP Toolsを1995年に[GPLの下で公開した](../Page/GNU_General_Public_License.md "wikilink")\[8\]。 オープンソースライセンスの下で公開されたことにより同ツールの利用者が増加し、機能の追加を行う開発者たちの貢献もあって、幾度かの大きなバージョンアップを経て今日に至っている。 PHPの[再帰的頭字語](../Page/再帰的頭字語.md "wikilink")が PHP: Hypertext Preprocessor となったのは2017年現在の文法の基礎が確立したPHP 3から\[9\]である。

先に述べたように、PHPは動的なWebページを生成するツールを起源としているため、公式の処理系にはWebアプリケーション開発に関する機能が豊富に組み込まれている。 元々PHPはプログラミング言語と言えるものではなく、単にテンプレート的な処理を行うだけであったが、度重なる機能追加やコードの書き直しにより、2017年現在リリースされているPHP 5やPHP 7は目的によらず汎用的に使うことの出来るスクリプト言語となっている。 特に[Apache HTTP Serverや](../Page/Apache_HTTP_Server.md "wikilink")[nginx](https://ja.wikipedia.org/wiki/nginx "wikilink")といった[Webサーバー](https://ja.wikipedia.org/wiki/Webサーバー "wikilink")ソフトウェアから動作させるスクリプト言語として選択されてサーバーサイドWebアプリケーション開発に利用されることが多い。

プログラミング言語としてのPHPは、[Cや](../Page/C言語.md "wikilink")[Perl](../Page/Perl.md "wikilink"), [Java](https://ja.wikipedia.org/wiki/Java "wikilink")などのプログラミング言語に強く影響を受けており、これらの言語に近く学習しやすい文法を有する。 組み込み関数についてもこれらの言語から直接輸入されたものも多く、関数名を変えずにそのまま取り込んだことで標準関数の命名規則が一貫していないといった問題も有している。 また[C由来の](../Page/C言語.md "wikilink")[ヌル終端文字列](https://ja.wikipedia.org/wiki/ヌル終端文字列 "wikilink")と[ヌル文字](https://ja.wikipedia.org/wiki/ヌル文字 "wikilink")を含むことを許容する文字列とが併存し、関数によってどちらを取り扱うかが異なっていたために深刻なセキュリティ上の問題を起こしたこともある\[10\]。

PHPで書かれたライブラリは、[PEAR](../Page/PEAR.md "wikilink")を利用してシステムワイドにインストールしたりユーザ単位で利用することが多かったが、2012年に[Rubyのパッケージ管理ツールである](https://ja.wikipedia.org/wiki/Ruby_\(代表的なトピック\) "wikilink")[RubyGems](https://ja.wikipedia.org/wiki/RubyGems "wikilink")及び依存関係管理ツール[bundler](https://ja.wikipedia.org/wiki/:en:Bundler_\(Software\) "wikilink")、[Node.js](https://ja.wikipedia.org/wiki/Node.js "wikilink")の[npm](https://ja.wikipedia.org/wiki/npm "wikilink")に影響を受けて開発された[Composer](../Page/Composer.md "wikilink")が公開されたことにより、パッケージリポジトリPackagist\[11\]に登録されたライブラリをプロジェクト単位で利用することが容易になった。

PHP製のWebアプリケーションフレームワークが増加したことにより、それらが提供するロガーやHTTPリクエストハンドラなどといった共通の機能を実装するコードの再利用性を高めるため、2010年頃にフレームワーク開発者などが集まってPHP Standard Groupを立ち上げた\[12\]。 PHP Standard Groupはその後PHP-FIG (Framework Interoperability Group)に改称し、クラスオートローディングの規格やコーディング規約などの推奨される標準規格、**PSR** (PHP Standards Recommendations)の策定を行っている\[13\]。

### プログラミング言語としての特徴

  - [HTML埋め込み型の構文](https://ja.wikipedia.org/wiki/Hypertext_Markup_Language "wikilink")（Hypertext Preprocessorたる所以）
  - 弱い[動的型付け](../Page/動的型付け.md "wikilink")
  - [クラスベース](../Page/クラスベース.md "wikilink")[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")のサポート
  - [例外](../Page/例外.md "wikilink")処理 (try, catch, throw) のサポート

### 処理系としての特徴

  - サーバーサイドWebアプリケーション構築のための豊富な組み込み関数
  - データベースへの容易なアクセス（ベンダーごとの組み込み関数、[PDO](https://ja.wikipedia.org/wiki/PHP_Data_Object "wikilink")）
  - [PECL](../Page/PECL.md "wikilink")による言語機能の拡張
  - 多くのWebサーバへの組み込みの標準サポート

## 構文

[プログラミング言語](../Page/プログラミング言語.md "wikilink")としてのPHPは[Cや](../Page/C言語.md "wikilink")[Perl](../Page/Perl.md "wikilink")などの影響を強く受けており、同じくこれらに影響を受けた[Rubyや](https://ja.wikipedia.org/wiki/Ruby_\(代表的なトピック\) "wikilink")[Python](../Page/Python.md "wikilink")と比較してよりCそのままに近い制御構文を有している。 また[クラスや](../Page/クラス_\(コンピュータ\).md "wikilink")[インターフェイスといったオブジェクト指向構文は](../Page/インタフェース_\(情報技術\).md "wikilink")[C++](../Page/C++.md "wikilink")より[Java](https://ja.wikipedia.org/wiki/Java "wikilink")に近いものが採用されている。 文法の近さによって利用者の多いCやJavaからPHPを学んだり、その逆も行いやすいことは言語の学習コストの面からは大きな利点である。

### Hello world

PHPによる[Hello worldの最も簡単な実装は](../Page/Hello_world.md "wikilink")、単にテキストファイルとして「Hello world」を記述するだけでよい。

``` php
Hello world!
```

PHPはテキストファイルに[HTML](https://ja.wikipedia.org/wiki/HTML "wikilink")タグのように埋め込んで書き、それ以外の部分はそのまま出力されるため、上記は（プログラムとして実行される部分は存在しないものの）正しく処理系によって認識されて「Hello world\!」を出力する。 もう少しプログラムらしい書き方をすれば次のような記述が出来る。

``` php
<?php echo 'Hello world!'; ?>
```

PHPの処理系は**PHPタグ**<code>

<?php ?>

</code>で囲われた部分を解釈・実行し、その外側の部分はそのまま文字列として出力する。 単純にデータを出力する場合にはPHPタグを`<?= ?>`と略記することが可能であり、更にPHPタグがファイルの末尾にある場合はファイル末尾の空白や改行の影響を避けるためにPHPタグを閉じないことが推奨されるので、次のように書いても同じ結果が得られる。

``` php
<?='Hello world!'
```

### 文字列と数値の違い

次のように、[数値](https://ja.wikipedia.org/wiki/数値 "wikilink")として「 5+2 」を行うと7が出力される。ただし「5+2」を[シングルクォーテーション](https://ja.wikipedia.org/wiki/シングルクォーテーション "wikilink")や[ダブルクォーテーション](https://ja.wikipedia.org/wiki/ダブルクォーテーション "wikilink")で囲むと、[文字列](../Page/文字列.md "wikilink")と解釈されてそのまま出力される。

``` php
<?php
   echo 5+2; //結果: 7
   echo '5+2'; //結果: 5+2
?>
```

## 処理系

プログラミング言語としてのPHPを実行するための The PHP Group による[公式な処理系の実装も](../Page/リファレンス実装.md "wikilink")、プログラミング言語としてのPHPと区別されることなく **PHP** と呼ばれる。 2014年頃までプログラミング言語としてのPHPには規格などが存在しなかった\[14\]ため、公式の処理系の実装およびマニュアルの記述がその代わりとなっていた。 2018年1月現在では、作業中となっているが、プログラミング言語としての仕様は処理系の実装と分かれて文書化されている\[15\]。

この実装は[Cで書かれており](../Page/C言語.md "wikilink")、[PHP Licenseおよび](https://ja.wikipedia.org/wiki/PHP_License "wikilink")[Zend Engine Licenseの下で公開されている](https://ja.wikipedia.org/wiki/PHP_License#Zend_Engine_License "wikilink")[自由なソフトウェア](https://ja.wikipedia.org/wiki/自由なソフトウェア "wikilink")である。 PHP4以降において、プログラミング言語としてのPHPを解釈・実行するエンジンとして[Zend Engineが使用されており](https://ja.wikipedia.org/wiki/Zend_Engine "wikilink")、PHP5よりZend Engine 2、PHP7ではZend Engine 3へと順次バージョンアップされている。 Zend EngineはPHP 3の主要な開発者である[アンディ・ガトマンズ](https://ja.wikipedia.org/wiki/アンディ・ガトマンズ "wikilink")および[ゼーブ・スラスキー](https://ja.wikipedia.org/wiki/ゼーブ・スラスキー "wikilink")（後に[Zend Technologies Ltd.を設立](https://ja.wikipedia.org/wiki/ゼンド・テクノロジーズ "wikilink")）により設計・開発されたスクリプト言語エンジンであり、現在はThe PHP GroupによりPHPと共に開発されている。 Zend Engineは1つのプロセスが1つのインタプリタのコンテキストを持つように設計されていて、単独では[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")を用いた処理をサポートしていない。 PHPはそのソースコードのほとんどがPHP Licenseの下でリリースされるが、Zend EngineのコードについてはZend Engine Licenseが適用される。

実際のPHPの構成はZend Engineに加え、PHPの組み込み関数の実装、Webサーバや[標準入出力](https://ja.wikipedia.org/wiki/標準入出力 "wikilink")とスクリプティングエンジンの間を仲介するSAPI (Server API) レイヤ、マルチスレッドで動くWebサーバのモジュールとして利用される場合にグローバル変数の[セマンティクス](https://ja.wikipedia.org/wiki/セマンティクス "wikilink")を提供するTSRM (Thread Safe Resource Manager)、プラットフォーム間での入出力機構やAPIの差異を吸収するStreamsレイヤを含む。 一部の組み込み関数はプラットフォームごとに挙動が違うため、スクリプトによっては移植作業が必要になる場合がある。

### PECLによる拡張

公式の処理系に対して、[Cや](../Page/C言語.md "wikilink")[C++](../Page/C++.md "wikilink")で記述された拡張ライブラリを提供する **[PECL](../Page/PECL.md "wikilink")** (The PHP Extension Community Library) というプロジェクトが存在する。 基本的にPECLのライブラリは標準ではPHPに組み込まれてはいないものが多いが、PECLで開発されていたライブラリがPHPの本体に標準でバンドルされるようになったり([PDO](https://ja.wikipedia.org/wiki/PHP_Data_Object "wikilink"))、逆に非推奨となった機能が本体より取り除かれ、PECLでメンテナンスが継続される([mcrypt](https://pecl.php.net/package/mcrypt))こともあり、拡張機能としてはPHPの準標準と言える立ち位置にある。

### 対応する主要DBMS

PHPは数多くの[DBMS](https://ja.wikipedia.org/wiki/DBMS "wikilink")を標準でサポートしている。 提供されるAPIは、**ベンダ固有モジュール**というDBMS毎に提供される専用モジュールによるものと、ベンダ毎の差異を吸収して一貫したインターフェイスで様々なDBMSに接続出来る**データベース抽象化レイヤ**とがある。 特にデータベースをより高度に抽象化して扱うライブラリなどでは、様々なDBMSに対応するためにPHP5.1で標準になったデータベース抽象化レイヤ [PDO](https://ja.wikipedia.org/wiki/PHP_Data_Object "wikilink") をバックエンドとして選択するものが多い。

<div style="columns: 24em 4; column-rule: 2px solid #eee;">

  - [Apache Derby](../Page/Apache_Derby.md "wikilink")
  - [DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")
  - [Informix Dynamic Server](https://ja.wikipedia.org/wiki/Informix_Dynamic_Server "wikilink")
  - [InterBase](../Page/InterBase.md "wikilink")
  - [Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")
  - [mSQL](https://ja.wikipedia.org/wiki/mSQL "wikilink")
  - [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")
  - [ODBC](../Page/Open_Database_Connectivity.md "wikilink")
  - [Oracle Database](../Page/Oracle_Database.md "wikilink")
  - [PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")
  - [Sybase Adaptive Server Enterprise](https://ja.wikipedia.org/wiki/Adaptive_Server_Enterprise "wikilink")
  - [SQLite](../Page/SQLite.md "wikilink")
  - [Redis](https://ja.wikipedia.org/wiki/Redis "wikilink")

</div>

### Webサーバとの統合

PHPをWebサーバで動作させる方法には、実行ファイル形式 (CGI / [FastCGI](../Page/FastCGI.md "wikilink"))、モジュール形式（mod_phpなど）がある。 どの方法を利用するか（利用出来るか）はWebサーバにより異なる。 実行ファイル形式によるCGIはほぼ全てのWebサーバに対応しているが、[Apacheで動作させる場合はmod](../Page/Apache_HTTP_Server.md "wikilink")_phpとFastCGI、[IIS](../Page/Internet_Information_Services.md "wikilink")、[lighttpd](https://ja.wikipedia.org/wiki/lighttpd "wikilink")や[Nginx](https://ja.wikipedia.org/wiki/Nginx "wikilink")で動作させる場合は[FastCGI](../Page/FastCGI.md "wikilink")が利用可能である。

PHPに標準で実装されているWebサーバ用[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") (SAPI)の一覧を以下に挙げる。以前はこのほかにも存在したがPHP 7.0で削除された\[16\]。

  - [CGI](../Page/Common_Gateway_Interface.md "wikilink") / [FastCGI](../Page/FastCGI.md "wikilink")

      - FastCGIについては、php-cgiプログラムとFastCGI Process Manager (FPM)の2種類が用意されている。

  - [Apache HTTP Server](../Page/Apache_HTTP_Server.md "wikilink")

  -
とくに、HTTPリクエストの度にプロセスを起動させないインタフェース（Apacheとmod_phpの組み合わせ、または[lighttpd](https://ja.wikipedia.org/wiki/lighttpd "wikilink")などの[FastCGI](../Page/FastCGI.md "wikilink")に対応したWebサーバ）での動作が高速である。

### その他の処理系

PHPの[処理系](https://ja.wikipedia.org/wiki/処理系 "wikilink")は公式の実装を含めいくつかの異なる実装が存在する。 そのうち比較的よく知られているものについて簡単に記述する。

  - [HHVM](https://ja.wikipedia.org/wiki/HipHop_Virtual_Machine "wikilink") (HipHop Virtual Machine) ([PHP License](https://ja.wikipedia.org/wiki/PHP_License "wikilink"), [Zend Engine License](https://ja.wikipedia.org/wiki/Zend_Engine_License "wikilink"))
    [Facebook](../Page/Facebook.md "wikilink")によって開発された処理系で、実行の高速化のために[実行時(JIT)コンパイル方式を採用している](../Page/実行時コンパイラ.md "wikilink")。HHVMは実行時にソースコードをHipHopバイトコードと呼ばれる独自の中間言語にコンパイルし、そこから動的に機械語にコンパイル/最適化を経て実行される。ただし、HHVM4.0 以降はPHPから派生した言語である[Hack専用となり](https://ja.wikipedia.org/wiki/Hack_\(プログラミング言語\) "wikilink")、PHP自体のサポートは削除された。

<!-- end list -->

  - [Phalanger](https://ja.wikipedia.org/wiki/Phalanger "wikilink") ([Apache License](../Page/Apache_License.md "wikilink"))
    [プラハ・カレル大学](../Page/プラハ・カレル大学.md "wikilink")のオープンソースプロジェクトとして開発されている処理系で、PHPのソースコードを[CILバイトコード](https://ja.wikipedia.org/wiki/CILバイトコード "wikilink")にコンパイルすることにより[.NET Framework上で動作させることを可能にしている](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。

## PHPで書かれたソフトウェア

PHPは学習コストの低さ、記述の容易さから多くのアプリケーションが開発されている。 [Wikipedia](https://ja.wikipedia.org/wiki/Wikipedia "wikilink")を動作させているアプリケーションである[MediaWiki](../Page/MediaWiki.md "wikilink")もPHPによって記述されている。

本節ではPHPで書かれた代表的なアプリケーションを列挙する。

### ウェブアプリケーション、CMSなど

<div style="columns: 24em 4; column-rule: 2px solid #eee;">

  - [IBM WebSphere sMash](https://www.ibm.com/jp-ja/cloud/info/websphere)
  - [MediaWiki](../Page/MediaWiki.md "wikilink")
  - [phpBB](https://ja.wikipedia.org/wiki/phpBB "wikilink")
  - [phpMyAdmin](https://ja.wikipedia.org/wiki/phpMyAdmin "wikilink")
  - [PukiWiki](../Page/PukiWiki.md "wikilink")
  - [Serendipity Weblog System](https://docs.s9y.org/)
  - [SilverStripe CMS](https://www.silverstripe.org/)
  - [WordPress](../Page/WordPress.md "wikilink")
  - [XOOPS](../Page/XOOPS.md "wikilink")
  - [OpenPNE](../Page/OpenPNE.md "wikilink")
  - [KinagaCMS](https://ja.wikipedia.org/wiki/KinagaCMS "wikilink")

</div>

### ウェブアプリケーション・フレームワーク

<div style="columns: 24em 4; column-rule: 2px solid #eee;">

  - [CakePHP](../Page/CakePHP.md "wikilink")

  - [CodeIgniter](../Page/CodeIgniter.md "wikilink")

  - [Cosmos](https://cwf.codeplex.com/)

  - [Ethna](http://ethna.jp/)

  - [eZ components](https://ez.no/index.php/products/ez_components)

  - [FuelPHP](https://ja.wikipedia.org/wiki/FuelPHP "wikilink")

  - [Kohana](https://kohanaframework.org/)

  - [Laravel](https://ja.wikipedia.org/wiki/Laravel "wikilink")

  - [Lithium](https://lithiumseo.com/)

  - [PHP on TRAX](https://github.com/phpontrax/trax)

  - [PRADO](https://ja.wikipedia.org/wiki/PRADO_\(フレームワーク\) "wikilink")

  - [Risoluto](https://ja.osdn.net/projects/risoluto/)

  - [Seasar.PHP](https://www.seasar.org/#seasar.php)

  - [Symfony](https://ja.wikipedia.org/wiki/Symfony "wikilink")

  - [WACT](https://www.acronymfinder.com/Web-Application-Component-Toolkit-\(PHP-development-framework\)-\(WACT\).html)

  -
  - [Yii](https://ja.wikipedia.org/wiki/Yii "wikilink")

  - [Zend Framework](https://ja.wikipedia.org/wiki/Zend_Framework "wikilink")

  - [ちいたん](https://ja.osdn.net/projects/cheetan/)

  - [Chimpanzee](https://chimpanzee-php.com/)

</div>

### テンプレートエンジン

<div style="columns: 24em 4; column-rule: 2px solid #eee;">

  - [Smarty](https://ja.wikipedia.org/wiki/Smarty "wikilink")
  - [Twig](https://ja.wikipedia.org/wiki/Twig "wikilink")

</div>

## 歴史

### 前史

[ラスマス・ラードフ](https://ja.wikipedia.org/wiki/ラスマス・ラードフ "wikilink")は自身のWebページで利用するため、1994年に[Cで書かれたCGI用バイナリ群を作成し](../Page/C言語.md "wikilink")、 "**Personal Home Page Tools**" と命名した。 このCGIソフトウェアは略して "**PHP Tools**" と呼ばれることが多かったようである。 その後、利用者からの機能要望が増えたため、オリジナルのPHP Toolsは大きく書き直され、データベースを利用することが出来るようになった。 単純なツール群から一種のフレームワークとしての機能を有するようになったのである。 ラードフは[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")6月8日に[GPLの下でPHP](../Page/GNU_General_Public_License.md "wikilink") Toolsを公開、オープンソースソフトウェアとして最初のリリースを行った。

1995年9月、ラードフはPHP Toolsを発展させ、現在のPHPにも受け継がれている特徴、[Perl](../Page/Perl.md "wikilink")風の変数名やHTMLフォームデータの自動取得、そしてHTMLへの埋め込み型の記述方式などを持ったツール "**FI**" (Form Interpreter) を実装した。 翌月にはFIを完全に書き直し、 "**Personal Home Page Construction Kit**" という名前でリリースを行い、CやPerlに近い構文を有する簡易スクリプトツールへと発展した。

このツールは再び一から書き直され、ユーザ定義関数のサポートなど、プログラミング言語としての機能を有するようになった。 1996年4月になるとPHPとFIの名称を合わせた "**PHP/FI**" として公開された。 同年6月に、後にPHP 2として言及される "**PHP/FI Version 2.0**" の[ベータ版](../Page/ベータ版.md "wikilink")がリリースされた。 PHP/FI Version 2.0は翌1997年11月に正式版がリリースされ、その後1998年1月に一度アップデートが行われたあとはメンテナンスは行われなかった。

### PHP 3

イスラエルの[アンディ・ガトマンズ](https://ja.wikipedia.org/wiki/アンディ・ガトマンズ "wikilink")と[ゼーブ・スラスキー](https://ja.wikipedia.org/wiki/ゼーブ・スラスキー "wikilink")は、[e-コマースアプリケーションを開発するためにPHP](../Page/電子商取引.md "wikilink")/FI Version 2.0を利用しようと考えていたが、PHP/FIには機能が不足していた。 そこで1997年、彼らはラードフに対してPHP/FIを作り直す方法を検討していることを伝えた。 ガトマンズとスラスキ―はPHP/FIで使われていたパーサを書き直し、ラードフとも協力して新たなプログラミング言語を開発した。 この言語は再び "**PHP**" と命名されたが、"Personal Home Page Tools"が抱えていた個人用という印象を避けるため、新しく "**PHP: Hypertext Preprocessor**" という[再帰的頭字語](../Page/再帰的頭字語.md "wikilink")を与えられることになった。 1998年6月、ラードフ、ガトマンズそしてスラスキーに加え、世界中の開発者らが立ち上げたPHP Development Teamは "**PHP 3.0**" をPHP/FI Version 2.0の後継として、[GPL](https://ja.wikipedia.org/wiki/GPL "wikilink")と[PHP Licenseとのデュアルライセンスの下でリリースした](https://ja.wikipedia.org/wiki/PHP_License "wikilink")。

### PHP 4

PHP 3.0がリリースされて間もなく、ガトマンズとスラスキーはPHPのプログラミング言語を処理するコアの部分の再設計を行い、新しく作り上げた実行エンジンを彼らの名前からとって "**[Zend Engine](https://ja.wikipedia.org/wiki/Zend_Engine "wikilink")**" と命名した。 2000年5月、このZend Engineを使用した大幅なパフォーマンスの改善を行い、より多くのWebサーバのサポートなどの機能拡張を行った新しいバージョンである"**PHP 4.0**"がリリースされた。 PHP 4では[コピーレフト](../Page/コピーレフト.md "wikilink")条項がPHPの利用拡散を妨げるという判断\[17\]により、ライセンスから[GPL](https://ja.wikipedia.org/wiki/GPL "wikilink")が外れて[PHP LicenseおよびZend](https://ja.wikipedia.org/wiki/PHP_License "wikilink") Engineのコードについては[Zend Engine Licenseが適用されることになった](https://ja.wikipedia.org/wiki/Zend_Engine_License "wikilink")。

PHP 4は4.0から4.4までがリリースされ、2008年8月にセキュリティ対応を含めた全ての開発が終了している。

### PHP 5

[2004年](../Page/2004年.md "wikilink")7月、新たにZend Engine 2をコアとし、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")構文をより一層強化したバージョンである "**PHP 5.0**" がリリースされた。 マイナーアップデートにより様々な機能の追加が行われ、DBMSへの一貫したアクセスインターフェイスを提供する抽象化レイヤ[PDOが導入されたり](https://ja.wikipedia.org/wiki/PHP_Data_Object "wikilink")、PHPが欠いていた[名前空間](../Page/名前空間.md "wikilink")、[静的遅延束縛](../Page/束縛_\(情報工学\).md "wikilink")、[クロージャ](../Page/クロージャ.md "wikilink")などをはじめとしたプログラミング言語としての機能強化が頻繁に取り入れられている。

PHP 5.4では特筆すべき機能として開発用の組み込みWebサーバが導入されており、他のWebサーバを導入しなくともWebアプリケーション開発が容易に行えるようになった。 PHP 5.6では対話式デバッガがSAPIとして組み入れられた。

PHP 5は既にほとんどのバージョンで開発が終了しており、最終バージョンであるPHP 5.6のセキュリティ対応も2018年12月31日をもって終了した。。

### PHP 6

PHP 5.3の次のリリースとなるべく開発されていたバージョンで、エンジンの内部処理がUTF-16に置き換えられる計画であったが、多くの問題に見舞われたことから2010年に開発が断念されている。 PHP 5.3の次のリリースはPHP 5.4へと置き換えられ\[18\]、また次のPHPのメジャーリリースがPHP 7とされたことでPHP 6は欠番となった。

### PHP 7

2015年12月に内部エンジンをZend Engine 3とした"**PHP 7.0**"がリリースされた\[19\]。 Zend Engineの改善を行うPHPNG (PHP Next-Gen) プロジェクトの成果を取り入れており、データ構造の改善などにより、前バージョンのPHP 5.6と比べて25%から70%の性能改善が図られている。 また言語仕様も大きく拡張されており、引数のタイプヒンティングにスカラー型が指定できるようになる\[20\]（タイプヒンティングは5.1で導入されたが、クラスや配列など一部の型に限られていた）他、戻り値へのタイプヒンティング\[21\]も導入されており、前年に発表された[HHVM用プログラミング言語](https://ja.wikipedia.org/wiki/HipHop_Virtual_Machine "wikilink")[Hackの影響が見受けられるものになっている](https://ja.wikipedia.org/wiki/Hack_\(プログラミング言語\) "wikilink")。\[22\]

### リリース履歴

| 色      | 意味  | メンテナンスの状況     |
| ------ | --- | ------------- |
| Red    | 旧版  | メンテナンス終了      |
| Yellow | 安定版 | セキュリティ対応のみ    |
| Green  | 安定版 | バグ修正とセキュリティ対応 |
| Blue   | 開発版 | 新機能の追加        |

凡例

<table>
<thead>
<tr class="header">
<th><p>Ver.</p></th>
<th><p>リリース日時</p></th>
<th><p>サポート期限[23][24]</p></th>
<th><p>特記事項</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>アクティブ</p></td>
<td><p>セキュリティ</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.0</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2.0</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.0</p></td>
<td></td>
<td></td>
<td><p>[25]</p></td>
</tr>
<tr class="odd">
<td><p>4.0</p></td>
<td></td>
<td></td>
<td><p>[26]</p></td>
</tr>
<tr class="even">
<td><p>4.1</p></td>
<td></td>
<td></td>
<td><p>[27]</p></td>
</tr>
<tr class="odd">
<td><p>4.2</p></td>
<td></td>
<td></td>
<td><p>[28]</p></td>
</tr>
<tr class="even">
<td><p>4.3</p></td>
<td></td>
<td></td>
<td><p>[29]</p></td>
</tr>
<tr class="odd">
<td><p>4.4</p></td>
<td></td>
<td></td>
<td><p>[30]</p></td>
</tr>
<tr class="even">
<td><p>5.0</p></td>
<td></td>
<td></td>
<td><p>[31]</p></td>
</tr>
<tr class="odd">
<td><p>5.1</p></td>
<td></td>
<td></td>
<td><p>[32]</p></td>
</tr>
<tr class="even">
<td><p>5.2</p></td>
<td></td>
<td></td>
<td><p>[33]</p></td>
</tr>
<tr class="odd">
<td><p>5.3</p></td>
<td></td>
<td></td>
<td><p>[34]</p></td>
</tr>
<tr class="even">
<td><p>5.4</p></td>
<td></td>
<td></td>
<td><p>[35]</p></td>
</tr>
<tr class="odd">
<td><p>5.5</p></td>
<td></td>
<td></td>
<td><p>[36]</p></td>
</tr>
<tr class="even">
<td><p>5.6</p></td>
<td></td>
<td><p>[37]</p></td>
<td><p>[38]</p></td>
</tr>
<tr class="odd">
<td><p>6.x</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>7.0</p></td>
<td><p>[39]</p></td>
<td><p>[40]</p></td>
<td><p>[41]</p></td>
</tr>
<tr class="odd">
<td><p>7.1</p></td>
<td></td>
<td><p>[42]</p></td>
<td><p>[43]</p></td>
</tr>
<tr class="even">
<td><p>7.2</p></td>
<td></td>
<td><p>[44]</p></td>
<td><p>[45]</p></td>
</tr>
<tr class="odd">
<td><p>7.3</p></td>
<td></td>
<td><p>[46]</p></td>
<td><p>[47]</p></td>
</tr>
<tr class="even">
<td><p>7.4</p></td>
<td></td>
<td><p>[48]</p></td>
<td><p>[49]</p></td>
</tr>
</tbody>
</table>

## 脚注

## 関連項目

  - [Perl](../Page/Perl.md "wikilink")

  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")

  - [スクリプト言語](../Page/スクリプト言語.md "wikilink")

  - [オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")

  -
## 外部リンク

  -

      - [日本語マニュアル](https://www.php.net/manual/ja/)

  - [日本PHPユーザー会](http://www.php.gr.jp/)

[Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:PHP](https://ja.wikipedia.org/wiki/Category:PHP "wikilink") [Category:テンプレートエンジン](https://ja.wikipedia.org/wiki/Category:テンプレートエンジン "wikilink")

1.
2.
3.  {{ Cite web |url=//php.net/get-involved.php |title=Contributing to PHP |publisher=php.net |accessdate=2018-02-02 }}
4.  {{ Bquote |PHP is a popular general-purpose scripting language that is especially suited to web development. | | |The PHP Group |php.net }}
5.  {{ Cite web |url=//php.net/manual/intro-whatis.php |title=What is PHP |work=PHP Manual |publisher=php.net |accessdate=2018-02-02 }}
6.  {{ Cite web |url=//php.net/manual/history.php.php |title=History of PHP |work=PHP Manual |publisher=php.net |accessdate=2018-02-02 }}
7.
8.  {{ Cite web |url=<https://groups.google.com/forum/#!msg/comp.infosystems.www.authoring.cgi/PyJ25gZ6z7A/M9FkTUVDfcwJ> |title=Announce: Personal Home Page Tools (PHP Tools) |publisher=Google Group |author=[Rasmus Lerdorf](https://ja.wikipedia.org/wiki/ラスマス・ラードフ "wikilink") |accessdate=2018-02-02 }}
9.
10. {{ Cite web |url=//php.net/manual/security.filesystem.nullbytes.php |title=Null bytes related issues |work=PHP Manual |publisher=php.net |accessdate=2018-02-02 }}
11. [packagist.org](https://packagist.org/)
12. [www.php-fig.org](http://www.php-fig.org/)
13. {{ Cite web |url=<http://www.php-fig.org/psr/> |title=PHP Standards Recommendations |publisher=PHP-FIG |accessdate=2018-02-02 }}
14. {{ Cite web |author=Joab Jackson |date=2014-07-31 |url=<https://www.itworld.com/article/2697195/enterprise-software/php-gets-a-formal-specification--at-last.html> |title=PHP gets a formal specification, at last |publisher=IDG |work=ITworld |accessdate=2018-02-02 }}
15. {{ Cite web |url=<https://github.com/php/php-langspec> |title=PHP Language Specifications |author=The PHP Group |publisher=[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink") |accessdate=2018-02-02 }}
16.
17. {{ Cite web |url=<https://www.php.net/license/> |title=PHP Licensing |publisher=php.net |accessdate=2018-02-02 }}
18. {{ Cite web |url=<http://news.mynavi.jp/news/2010/03/17/053/> |title=PHP6開発 UTF-16化を断念、5.3へロールバック |publisher=[マイナビニュース](https://ja.wikipedia.org/wiki/マイナビニュース "wikilink") |date=2010-03-17 |accessdate=2015-05-03 }}
19. {{ cite web | url=<http://php.net/archive/2015.php#id2015-12-03-1> | title=PHP 7.0.0 Released | publisher=php.net | accessdate=2015-12-04 }}
20. {{ cite web |url=<https://wiki.php.net/rfc/scalar_type_hints_v5> |title=RFC: Scalar Type Declarations |date=2015-03-16 |accessdate=2015-03-17 |publisher=php.net }}
21. {{ cite web |url=<https://wiki.php.net/rfc/return_types> |title=RFC: Return Types |date=2015-01-27 |accessdate=2015-01-28 |publisher=php.net }}
22. {{ Cite web |url=<https://pages.zend.com/ty-infographic.html> |title=PHP 7 Infographic - 5 things you need to know \#php \#zend |publisher=Zend Technologies Inc. |accessdate=2015-05-03 }}
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.
35.
36.
37.
38.
39.
40.
41.
42.
43.
44.
45.
46.
47.
48.
49.