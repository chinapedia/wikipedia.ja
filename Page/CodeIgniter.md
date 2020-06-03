> この記事は[CodeIgniter](https://ja.wikipedia.org/wiki/CodeIgniter)から翻訳されています。


**CodeIgniter**（コードイグナイター）は、[PHPを用いて動的Webサイトを構築するために利用する](../Page/PHP_\(プログラミング言語\).md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の[Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")である。

## 概要

CodeIgniterは軽量で速度重視であることを特徴とする[Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")である\[1\]。CodeIgniterには、一般に必要とされるプログラミングタスクに対する豊富なライブラリが用意されているだけでなく、それらのライブラリにアクセスするためのシンプルなインターフェースと論理的な構造が用意されている。開発者はこれらが備わったCodeIgniterを用いることで、より短時間でアプリケーションを構築することができる。

CodeIgniterの最初の公開バージョンは、[2006年](../Page/2006年.md "wikilink")にリリースされた\[2\]。[Google](../Page/Google.md "wikilink")の検索数による比較では、[2011年](../Page/2011年.md "wikilink")にはPHPの他の主要フレームワーク ([CakePHP](../Page/CakePHP.md "wikilink"), [Zend Framework](https://ja.wikipedia.org/wiki/Zend_Framework "wikilink"), [Symfony](https://ja.wikipedia.org/wiki/Symfony "wikilink")) を抑えCodeIgniterが最多となるなど、広く用いられている\[3\]。 その後はライセンス問題もあり、後発のLaravelに人気を奪われるが、アメリカ、インド、インドネシア、ブラジル、トルコなどでは依然として人気が高く、インド、インドネシア等でのWEBサイト数は2019年2月現在においてもLaravelを凌いでいる。\[4\]

2020年2月には[名前空間](../Page/名前空間.md "wikilink")の全面採用などが行われたバージョン4.0がリリースされた\[5\]。

## 特徴

[Ruby on Rails](../Page/Ruby_on_Rails.md "wikilink") のように、CodeIgniterでは、ユーザは [Active Record](../Page/Active_Record.md "wikilink")（バージョン3.0以降はQuery Builderに改称）を用いて[データベース](../Page/データベース.md "wikilink")に接続でき、[モデル・ビュー・コントローラアーキテクチャパターンの利用が推奨される](../Page/Model_View_Controller.md "wikilink")。

  - 極めて軽量
  - 複数のデータベースプラットフォームをサポート
  - Formとデータの検証 (Validation)
  - セキュリティと [XSSフィルタリング](../Page/クロスサイトスクリプティング.md "wikilink")
  - [セッション](../Page/セッション.md "wikilink")管理
  - Eメール送信クラス。添付・HTML/テキストEメール・複数プロトコル（sendmail・SMTPおよび Mail）のサポートなど
  - 画像操作ライブラリ（切り抜き・リサイズ・回転など）。[GD](../Page/GD_Graphics_Library.md "wikilink")・[ImageMagick](../Page/ImageMagick.md "wikilink") および [Netpbm](https://ja.wikipedia.org/wiki/Netpbm "wikilink") に対応。
  - ファイルアップロードクラス
  - [FTPクラス](../Page/File_Transfer_Protocol.md "wikilink")
  - [ローカライゼーション](../Page/国際化と地域化.md "wikilink")
  - ページ付け
  - データ[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")
  - [ベンチマーク](../Page/ベンチマーク.md "wikilink")
  - 完全ページ[キャッシュ](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")
  - エラーロギング
  - アプリケーションの [プロファイリング](../Page/性能解析.md "wikilink")
  - カレンダークラス
  - [ユーザーエージェント](../Page/ユーザーエージェント.md "wikilink")クラス
  - [Zip圧縮クラス](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")
  - テンプレートエンジンクラス
  - [トラックバック](https://ja.wikipedia.org/wiki/トラックバック "wikilink")クラス
  - [XML-RPC](../Page/XML-RPC.md "wikilink")ライブラリ
  - [単体テスト](../Page/単体テスト.md "wikilink")クラス
  - [検索エンジンフレンドリURL](../Page/検索エンジン最適化.md "wikilink")
  - 柔軟なURIルーティング
  - フック・クラス拡張およびプラグインへの対応
  - 多数の「ヘルパー」関数ライブラリ
  - [Composer](../Page/Composer.md "wikilink")への対応（バージョン3.0以降）

## Kohana

**Kohana**は、CodeIgniterから[フォーク](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")（派生・分岐）したプロジェクトである。（2011年頃までは "KohanaPHP" と称していたが、"PHP" という言葉の使用がPHP Licenceに違反する可能性があったため、現在はプロジェクト名も単に "Kohana" と表記している。）

Kohanaは、モデル・ビュー・コントローラ アキーテクチャパターンを使ったPHP5のフレームワークである。Kohanaは、セキュアで、軽量、かつ、簡単に利用できるということを目標としている。

もともとは、BlueFlameという名前のプロジェクトで作成されていたKohana（当時は "KohanaPHP"）の最初のリリースは、よく知られたPHP MVCフレームワークを見据えたいくつかのバグ修正が主たるものであった。

KohanaとCodeIgniterの主な違いの一つとしては、CodeIgniterの長期に渡る（1.7.2まで）PHP4下位互換に対する、Kohanaの厳格なPHP5によるOOP（オブジェクト指向開発）が挙げられる。

2017年7月1日をもって開発を終了することが告知されている。\[6\]

## ライセンス

バージョン2.xまでのCodeIgniterは、[ライセンス](../Page/ライセンス.md "wikilink")に独自の[オープンソース](../Page/オープンソース.md "wikilink")ライセンスであるCodeIgniterライセンスを採用していた\[7\]。CodeIgniterライセンスは[Apache](../Page/Apache_License.md "wikilink")/[BSDスタイルのオープンソースライセンスであるが](../Page/BSDライセンス.md "wikilink")、宣伝条項を含んでおり[GPLとは互換性がない](../Page/GNU_General_Public_License.md "wikilink")\[8\]。

2011年10月、EllisLabはCodeIgniterのライセンスをに変更すると発表し\[9\]、バージョン3.x開発ブランチで/[AFL-3.0への変更がコミットされた](https://ja.wikipedia.org/wiki/Academic_Free_License "wikilink")\[10\]。

その後もバージョン3.0の開発が続けられていたが、2013年7月、EllisLabはCodeIgniterの新しい所有者を探していることを発表\[11\]。翌2014年10月、[ブリティッシュコロンビア工科大学](https://ja.wikipedia.org/wiki/ブリティッシュコロンビア工科大学 "wikilink")が開発を引き継ぐことになった\[12\]。バージョン3.xも[MITライセンス](https://ja.wikipedia.org/wiki/MITライセンス "wikilink")に変更されることになり\[13\]、2015年3月30日に3.0.0がリリースされた\[14\]。

## 脚注

## 関連項目

  - [アプリケーションフレームワーク](../Page/アプリケーションフレームワーク.md "wikilink")
  - [Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")

## 外部リンク

  - [CodeIgniter公式サイト](http://www.codeigniter.com/)
  - [日本CodeIgniterユーザ会](http://codeigniter.jp/)
  - [bcit-ci/CodeIgniter · GitHub](https://github.com/bcit-ci/CodeIgniter)
  - [CodeIgniter 3のライセンスがMITライセンスに変更され、いわゆるライセンス問題は完全に解消 — A Day in Serenity (Reloaded)](http://blog.a-way-out.net/blog/2014/10/31/codeigniter-3-license-mit/)

[Category:PHP](https://ja.wikipedia.org/wiki/Category:PHP "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ウェブアプリケーションフレームワーク](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーションフレームワーク "wikilink")

1.
2.
3.
4.
5.
6.  <http://discourse.kohanaframework.org/t/kohana-retirement-2017-07-01/1277>
7.
8.
9.  [The Heart of EllisLab: Why we do what we do](https://speakerdeck.com/salvator/the-heart-of-ellislab-why-we-do-what-we-do?slide=17) EllisLab CEOのLeslie Camacho氏による発表。ExpressionEngine & CodeIgniter Conference 2011。
10. [adding new license file (OSL 3.0) and updating readme to ReST · bcit-ci/CodeIgniter@f4a4bd8](https://github.com/EllisLab/CodeIgniter/commit/f4a4bd8fac188ebc9cda822ffc811c218fd92b45)
11. [EllisLab Seeking New Owner for CodeIgniter](http://ellislab.com/blog/entry/ellislab-seeking-new-owner-for-codeigniter) EllisLab公式ブログ（2013年7月9日）
12. [Your Favorite PHP Framework, CodeIgniter, Has a New Home](https://ellislab.com/blog/entry/your-favorite-php-framework-codeigniter-has-a-new-home) EllisLab公式ブログ（2014年10月6日）
13. [CodeIgniter 3 Will be Released Under the MIT License](http://forum.codeigniter.com/thread-40.html) CodeIgniter公式フォーラム（2014年10月27日）
14. [CodeIgniter 3.0](http://forum.codeigniter.com/thread-1657.html) CodeIgniter公式フォーラム（2015年3月30日）