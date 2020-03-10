> この記事は[CakePHP](https://ja.wikipedia.org/wiki/CakePHP)から翻訳されています。


**CakePHP**（ケイクピーエイチピー）とは、[PHPで書かれた](../Page/PHP_\(プログラミング言語\).md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の[Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")である。先行する[Ruby on Railsの概念の多くを取り入れており](https://ja.wikipedia.org/wiki/Ruby_on_Rails "wikilink")、Rails流の高速開発とPHPの機動性を兼ね備えたフレームワークと言われている。[MITライセンスの元でフリーで配布されている](https://ja.wikipedia.org/wiki/MIT_License "wikilink")。

## 歴史

[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")3月、Cakeという名前の小さなフレームワークが公開されたことでCakePHPプロジェクトは始まった。[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")12月にはcakeソフトウェア財団が設立され、多くのサブプロジェクトを生みながら、利用者の拡大を続けている。特に日本においては、[2009年](../Page/2009年.md "wikilink")以降、2017年までもっとも人気のあるPHPフレームワークとなっており、\[1\]2018年からは世界的な潮流を受けてLaravelに人気を奪われるも根強い人気を得ている。なお、2020年1月現在も日本での稼働WEBサイト数はLaravelを上回っており、世界で最も多いという調査結果がある（日本以下、アメリカ、ブラジルと続く）。\[2\]\[3\]

## 特徴

  - [MVCアーキテクチャ](https://ja.wikipedia.org/wiki/Model_View_Controller "wikilink")。
  - 高い後方互換性。

:\* 下位バージョンからのアップグレードをサポートする公式移行ガイド及びUpgrade shell。

  - 統合された柔軟な[O/Rマッピング](../Page/オブジェクト関係マッピング.md "wikilink")。

:\* [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")、[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")、[SQLite](https://ja.wikipedia.org/wiki/SQLite "wikilink")、[Microsoft SQL Serverを標準サポート](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")。

  - フォームバリデーション機能。
  - セキュリティ対策機能（XSS対策・CSRF対策・フォーム改竄検知）。
  - カスタムURLを実現するためのリクエストディスパッチャー。
  - [PEAR](https://ja.wikipedia.org/wiki/PEAR "wikilink")等の外部ライブラリに依存しておらず、単体での利用が可能。
  - 必要なライブラリをその都度利用できるインポート機能。
  - プラグインによる機能拡張。
  - 柔軟なビュー機構。

:\* テンプレートの継承や拡張。

:\* ページ単位及び部品単位の[キャッシュ](https://ja.wikipedia.org/wiki/キャッシュ_\(コンピュータシステム\) "wikilink")。

  - [Composer](https://ja.wikipedia.org/wiki/Composer "wikilink")への標準対応（バージョン3以降）。

## リリース

リリースバージョンは、メジャーバージョン・マイナーバージョン・アップデートバージョンで構成されている。

  - メジャーバージョン
    アーキテクチャーの変更等を管理するバージョン。
      - 例）CakePHP 1 → 2（PHP4のサポートがなくなり、PHP5専用へ）。CakePHP 2 → 3（PHP5.4以降専用・名前空間の使用・モデルが配列でなくオブジェクトを返す）
  - マイナーバージョン
    新機能の追加等を管理するバージョン。基本的に新機能を使用しなければ、同じメジャーバージョン内では互換性を持つとしている。
      - 例）CakePHP 2.0 → 2.1（ビュークラスの機能拡張・コールバックに変わるイベントマネージャーの導入）
  - アップデートバージョン
    バグ修正や性能改善を管理するバージョン。

### CakePHP 1.2

  - リリース日 :
  - 対応PHPバージョン : PHP4.3.2以降及びPHP5以降
  - CakePHP 1.1 からの変更点\[4\]

:\* テストが全クラスをカバーし、コードカバレッジもより網羅

:\* コマンドラインからアプリケーションを実行するシェル機構の導入

:\* i18n（国際化）とl10n（地域化）をサポート

:\* ユニコードの文字列をサポート

:\* [CSRF](https://ja.wikipedia.org/wiki/CSRF "wikilink")対策の導入

:\* モデル内のメソッドを再利用可能にするビヘイビア機能の導入

:\* バリデーションの強化(複数バリデーションのサポートと組み込みバリデーションルールの増加)

:\* [DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")、[Oracle Database](../Page/Oracle_Database.md "wikilink") のサポート

:\* APC/XCache/Memcache のサポート

:\* より詳細なエラー表示（開発時のみ、バックトレースやビュー変数をエラーとともに表示）

:\* ページ分割やソートを可能にするPagination機能の追加

:\* Htmlヘルパーの肥大化解消のため、フォーム関連をFormヘルパーに移行

:\* アプリケーション全体の設定をConfigureクラスによる定義へと変更

:\* 外部ファイルの読み込みをAppクラスによる読み込みへと変更

:\* ビューのファイル拡張子が「.thtml」から「.ctp」へと変更

### CakePHP 1.3

  - リリース日 :
  - 対応PHPバージョン : PHP4.3.2以降及びPHP5以降

### CakePHP 2.0

  - リリース日 :
  - 対応PHPバージョン : PHP5.2.6以上
  - CakePHP 2.0.3

:\* PHPUnit 3.6 に対応

### CakePHP 2.1

  - リリース日 :
  - 対応PHPバージョン : PHP5.2.8以上

### CakePHP 2.2

  - リリース日 :
  - 対応PHPバージョン : PHP5.2.8以上

### CakePHP 2.3

  - リリース日 :
  - 対応PHPバージョン : PHP5.2.8以上

### CakePHP 2.4

  - リリース日 :
  - 対応PHPバージョン : PHP5.2.8以上

### CakePHP 2.5

  - リリース日 :
  - 対応PHPバージョン : PHP5.2.8以上

### CakePHP 2.6

  - リリース日 :
  - 対応PHPバージョン : PHP5.2.8以上

### CakePHP 2.7

  - リリース日 :
  - 対応PHPバージョン : PHP5.3.0以上

### CakePHP 3.0

  - リリース日 : \[5\]
  - 対応PHPバージョン : PHP5.4.16以上

:\* 新しい[ORMの導入](../Page/オブジェクト関係マッピング.md "wikilink")

:\* View Cellsクラスの導入

### CakePHP 3.1

  - リリース日 :
  - 対応PHPバージョン : PHP5.4.16以上

### CakePHP 3.2

  - リリース日 :
  - 対応PHPバージョン : PHP5.5.9以上

### CakePHP 3.3

  - リリース日 :
  - 対応PHPバージョン : PHP5.5.9以上

### CakePHP 3.4

  - リリース日 :
  - 対応PHPバージョン : PHP5.6.0以上

### CakePHP 3.5

  - リリース日 : \[6\]
  - 対応PHPバージョン : PHP5.6.0以上

### CakePHP 3.6

  - リリース日 : \[7\]
  - 対応PHPバージョン : PHP5.6.0以上

### CakePHP 3.7

  - リリース日 : \[8\]
  - 対応PHPバージョン : PHP5.6.0以上

### CakePHP 3.8

  - リリース日 : \[9\]
  - 対応PHPバージョン : PHP5.6.0以上

### CakePHP 4.0

  - リリース日 : \[10\]
  - 対応PHPバージョン : PHP7.2.0以上

## 発音・読み方

日本国内では英語での発音に近い「ケイクピーエイチピー」と読まれることが多い。

## 脚注

<references/>

## 外部リンク

  - [日本語公式サイト](https://cakephp.org/jp/)
  - [API](https://api.cakephp.org/)
  - [日本語マニュアル（3.x系）](https://book.cakephp.org/3.0/ja/index.html)
  - [日本語マニュアル（2.x系）](https://book.cakephp.org/2.0/ja/index.html)
  - [日本語マニュアル（1.3系）](https://book.cakephp.org/1.3/ja/index.html)

[Category:ソフトウェア工学](https://ja.wikipedia.org/wiki/Category:ソフトウェア工学 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ウェブアプリケーションフレームワーク](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーションフレームワーク "wikilink") [Category:PHP](https://ja.wikipedia.org/wiki/Category:PHP "wikilink")

1.
2.
3.
4.  <http://bakery.cakephp.org/articles/gwoo/2008/12/25/the-gift-of-1-2-final>
5.
6.
7.
8.
9.
10.