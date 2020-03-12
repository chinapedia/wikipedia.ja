> この記事は[Ruby on Rails](https://ja.wikipedia.org/wiki/Ruby_on_Rails)から翻訳されています。


**[Ruby](../Page/Ruby.md "wikilink") on Rails**（ルビーオンレイルズ）は、[オープンソース](../Page/オープンソース.md "wikilink")の[Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")である。**RoR**または単に**Rails**と呼ばれる。その名にも示されているように[Ruby](../Page/Ruby.md "wikilink")で書かれている。また[Model View Controller](../Page/Model_View_Controller.md "wikilink")（MVC）アーキテクチャに基づいて構築されている。

実アプリケーションの開発を他のフレームワークより少ないコードで簡単に開発できるよう考慮し設計されている。Railsの公式なパッケージはRubyの[ライブラリ](../Page/ライブラリ.md "wikilink")や[アプリケーションの流通ルートである](../Page/アプリケーションソフトウェア.md "wikilink")[RubyGems](https://ja.wikipedia.org/wiki/RubyGems "wikilink")により配布されている。

## 哲学

Railsの基本理念は「同じことを繰り返さない」（[DRY:*Don't Repeat Yourself*](https://ja.wikipedia.org/wiki/Don't_repeat_yourself "wikilink")）と「[設定より規約](https://ja.wikipedia.org/wiki/設定より規約 "wikilink")」（CoC:*Convention over Configuration*）である。

「同じことを繰り返さない」というのは、「定義などの作業は一回だけで済ませろ」との意味である\[1\]。「設定よりも規約」とは、「慎重に設計された規約（Convention）に従うことにより、設定（Configuration）を不要にする（あるいは軽減する）」ということである。Railsはフルスタックのフレームワークであり、コンポーネントの統合は手動での設定を必要とせず自動で規約に従い行われる。例えば、Ruby on Railsに組み込みの[ORMライブラリである](https://ja.wikipedia.org/wiki/オブジェクトリレーショナルマッピング "wikilink")[Active Recordでは](../Page/Active_Record.md "wikilink")、クラス定義においてデータベースから読み取るべき属性名等を指定する必要はない。Active Recordは[RDBMSの表定義から自動的にその情報を取得する](../Page/関係データベース管理システム.md "wikilink")。したがって、プログラムとRDBMSの両方にそれを定義するというような冗長な作業を行う必要はない。

## 歴史

Ruby on Railsは[デンマーク](https://ja.wikipedia.org/wiki/デンマーク "wikilink")の[プログラマ](../Page/プログラマ.md "wikilink")である[デイヴィッド・ハイネマイヤー・ハンソン](https://ja.wikipedia.org/wiki/デイヴィッド・ハイネマイヤー・ハンソン "wikilink")により、プロジェクト管理ツール "[basecamp](https://ja.wikipedia.org/wiki/basecamp_\(ソフトウェア\) "wikilink")" の開発に用いられた知見やコードを抽出し、一般化することにより作成された。

  - [2004年](../Page/2004年.md "wikilink")7月 最初のバージョン公開
  - 2005年12月13日 バージョン1.0リリース
  - 2007年12月7日 バージョン2.0リリース
  - 2010年8月29日 バージョン3.0リリース
  - 2013年6月27日 バージョン4.0リリース
  - 2016年6月30日 バージョン5.0リリース
  - 2019年8月15日 バージョン6.0リリース

2004年の登場以後、Ruby on Railsのコンセプトは他のフレームワークにも大きな影響を与えている。Ruby on Railsの影響を受けたフレームワークとしては、[PHPの](../Page/PHP_\(プログラミング言語\).md "wikilink")[CakePHP](../Page/CakePHP.md "wikilink")や[Symfony](https://ja.wikipedia.org/wiki/Symfony "wikilink")、[Perl](../Page/Perl.md "wikilink")の[Catalyst](../Page/Catalyst_\(ソフトウェア\).md "wikilink")、[groovy](https://ja.wikipedia.org/wiki/groovy "wikilink")の[Grails](https://ja.wikipedia.org/wiki/Grails "wikilink")、[Node.js](https://ja.wikipedia.org/wiki/Node.js "wikilink")の[YEOMAN](https://ja.wikipedia.org/wiki/YEOMAN "wikilink")といったものがある。

## RoRのMVCアーキテクチャ

Rails上の[MVCアーキテクチャは次のとおりである](../Page/Model_View_Controller.md "wikilink")（Action Packは、この中のViewとControllerのことを指している）。

### Model

データベース駆動のMVC WebアプリケーションではModelはRDBMSのテーブルを表すクラスを意味する。RailsではActive Recordを通じてModelクラスを扱う。通常プログラマはActiveRecord::Baseクラスのサブクラスを作る必要がある。そうすることでRDBMSのどのテーブルを使うべきか、どういったカラムを持つべきかを自動的に決定してくれる。

### View

MVCではViewは表示のためのロジックであり、コントローラクラスからのデータをどのように表示するかを規定している。WebアプリケーションではHTML内に若干のコードを埋め込むことで実現される。

### Controller

MVCではControllerはRailsのAction Packには含まれるアプリケーションコントローラクラスによって扱われる。WebベースMVCアプリケーションでは[Webブラウザを操作するユーザによりコントローラのメソッドが起動される](../Page/ウェブブラウザ.md "wikilink")。

## Merb

**Merb**（と[Erbの造語](https://ja.wikipedia.org/wiki/eRuby "wikilink")\[2\]）とは、2008年12月23日にRuby on Rails 3.0のリリースの一環として\[3\]Rails Webフレームワークに統合された\[4\][Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")である。

### 特徴

MerbのプロジェクトはRuby on Railsの[コントローラースタックにおける](../Page/Model_View_Controller.md "wikilink")[クリーンルーム実装](../Page/ソフトウェアクリーンルーム.md "wikilink")\[5\]として始められたが、Railsの精神や方法論から派生した数あるアイデアを組み込むまでに成長した。

Merbはコンポーネントに[モジュール性を持ち](https://ja.wikipedia.org/wiki/モジュール#ソフトウェア "wikilink")、伸張性のある[APIデザインや](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[垂直スケーラビリティを有している](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")。MerbはRails以上にフレキシブルで処理が早いフレームワークにしようと考えられていた\[6\]。

2008年12月23日、Rails3にこれらの機能のほとんどを組み込むことが発表された\[7\]\[8\]。

### モジュラリティ

モデル、ビュー、コントローラーアーキテクチャのコントローラーレイヤーのみを適切に内包するが、Webアプリケーションフレームワーク全体で一斉に動作する技術のより大規模なスイートのための統合ポイントを提供している。Railsとの統合の主なトピックはWebサーバインターフェイス、MVCモデルレイヤー、MVCビューレイヤー、最後にコントローラーエクステンションとアドオンである。また既定のアプリケーションスタックはモデルレイヤーでは、ビューレイヤーでは[ERB](../Page/ERuby.md "wikilink")、WebサーバレイヤーではとMongrelをそれぞれ組み込んでいる\[9\]\[10\]。

## 関連項目

  - [デイヴィッド・ハイネマイヤー・ハンソン](https://ja.wikipedia.org/wiki/デイヴィッド・ハイネマイヤー・ハンソン "wikilink")
  - [アジャイルソフトウェア開発](../Page/アジャイルソフトウェア開発.md "wikilink")
  - [重複コード](../Page/重複コード.md "wikilink")
  - [オブジェクト関係マッピング](../Page/オブジェクト関係マッピング.md "wikilink")

## 脚注

### 出典

## 外部リンク

  -
  - [Ruby on Rails ガイド](https://railsguides.jp/)

  -
[Category:ソフトウェア工学](https://ja.wikipedia.org/wiki/Category:ソフトウェア工学 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Ruby](https://ja.wikipedia.org/wiki/Category:Ruby "wikilink") [Category:ウェブアプリケーションフレームワーク](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーションフレームワーク "wikilink") [Category:ウェブサイトの構成](https://ja.wikipedia.org/wiki/Category:ウェブサイトの構成 "wikilink")

1.  重複したコードを書かない意味もある
2.
3.  [Ruby on Rails 3.0 Release Notes](http://edgeguides.rubyonrails.org/3_0_release_notes.html)
4.
5.
6.
7.
8.
9.
10.