> この記事は[MyNETS](https://ja.wikipedia.org/wiki/MyNETS)から翻訳されています。


**MyNETS**（マイネッツ）は、[データベース](../Page/データベース.md "wikilink")に[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")を利用し、[PHPで書かれた](../Page/PHP_\(プログラミング言語\).md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の[SNS運営用サーバサイドプログラムである](../Page/ソーシャル・ネットワーキング・サービス.md "wikilink")。[PHPライセンスの下で配布されている](https://ja.wikipedia.org/wiki/PHP_License "wikilink")。

## 歴史

SNSエンジンである[OpenPNE](../Page/OpenPNE.md "wikilink")2.4系からの派生プロジェクトとしてスタート。

Usagi Project が作成、開発を続けている。

  - 2006年12月 プロジェクト立ち上げ準備
  - 2007年1月 OpenPNEプロジェクトからの派生プロジェクトとして立ち上げ
  - 2007年2月 MyNETS1.0.0Nightyリリース
  - 2007年4月 MyNETS1.0.1Nightyリリース
  - 2007年5月 MyNETS1.1.0Nightyリリース
  - 2007年8月 MyNETS1.1.0Stableリリース
  - 2007年8月 国際化プロジェクトスタート
  - 2007年8月 MyNETS1.1.1Nightyリリース
  - 2008年9月 MyNETS1.2.0リリース（最新安定版） [Google ストリートビューに対応](https://ja.wikipedia.org/wiki/Google_ストリートビュー "wikilink")

## 特徴

[mixi](https://ja.wikipedia.org/wiki/mixi "wikilink")風のインターフェースを採用。

テンプレートエンジンは、[Smarty](https://ja.wikipedia.org/wiki/Smarty "wikilink")を採用。

[OpenPNE](../Page/OpenPNE.md "wikilink")2.4系から派生後、インストーラを標準で実装し、データベース接続ライブラリの高速化や細かなSQLのチューニングが施され、各種動作の高速化が図られている。

また次期バージョンのMyNETS 2.0ではMapleフレームワークの採用が決定していたが、Maple4フレームワークが現状形になっていないので、MyNETS2のコアフレームワークは[CodeIgniter](https://ja.wikipedia.org/wiki/CodeIgniter "wikilink")を利用することとなった。

## 動作環境

  - [Webサーバ](../Page/Webサーバ.md "wikilink")：[Apache](../Page/Apache_HTTP_Server.md "wikilink")
  - [データベース](../Page/データベース.md "wikilink")：[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink") 4.0.x以降 (**4.1.x以降推奨**)
  - [スクリプト言語](../Page/スクリプト言語.md "wikilink")：[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink") 4.3.x以降
  - [メールサーバ](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")：[Postfix](../Page/Postfix.md "wikilink")推奨（[sendmail](https://ja.wikipedia.org/wiki/sendmail "wikilink")、[qmail](https://ja.wikipedia.org/wiki/qmail "wikilink")などでの動作実績あり）

## 主な機能

  - ユーザ登録・認証機能
  - 日記機能
  - コミュニティ機能
  - コミュニティでのイベント機能
  - ユーザ間での「フレンド関係」構築機能
  - 足あと機能
  - 招待機能
  - レビュー機能
  - カレンダ機能

## OpenPNEとの比較

  - BIZ機能は無い
  - [インストーラー](https://ja.wikipedia.org/wiki/インストーラー "wikilink")機能
  - 伝言板機能
  - [ソーシャルマップ](https://ja.wikipedia.org/wiki/ソーシャルマップ "wikilink")機能

## 外部リンク

  - [OSDNプロジェクトページ](https://ja.osdn.net/projects/usagi/)
  - [Usagi Project MyNETS SNSについて](http://blog.livedoor.jp/mobile_sns_/)
  - [日本CodeIgniterユーザ会](http://codeigniter.jp/)

[Category:ソーシャル・ネットワーキング・サービス](https://ja.wikipedia.org/wiki/Category:ソーシャル・ネットワーキング・サービス "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")