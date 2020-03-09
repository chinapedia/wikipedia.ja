> この記事は[JDeveloper](https://ja.wikipedia.org/wiki/JDeveloper)から翻訳されています。


**JDeveloper**は、[オラクルが開発する](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE)。元々[JBuilder](https://ja.wikipedia.org/wiki/JBuilder "wikilink")のソースから派生した[Java](https://ja.wikipedia.org/wiki/Java "wikilink")用のIDEであったが、バージョン9.0.2以降で、それ自身をJavaで完全に記述しなおすことにより完全なオリジナルIDEとして生まれ変わっている。

## JDeveloperの機能

JDeveloperの主な機能は以下のとおり。

### プラグイン

機能統合環境にプラグインとしてさまざまな機能を組み込むことができる。

### デバッグ・ステップ実行

グラフィカルデバッガによってローカル・リモート・分散デバッグが可能。

### CVS

バージョン管理システム[CVSをつかってソースコード管理を行うことができる](../Page/Concurrent_Versions_System.md "wikilink")。

### JUnit連携

JUnitテストコードの生成、テスト実行を行うことができる。

### Antプラグイン

ビルドシステム[antと連携できる](https://ja.wikipedia.org/wiki/Apache_Ant "wikilink")。ant は、Unix系のコマンド [make](https://ja.wikipedia.org/wiki/make "wikilink") を置き換えるプログラムで、Makefile に相当する各ソースコードの依存関係を XML により記述する。antは、Java により書かれており、ウェブサーバで知られる [Apache](https://ja.wikipedia.org/wiki/Apacheソフトウェア財団 "wikilink") プロジェクトに開発されている。

### リファクタリング

[リファクタリングについては](https://ja.wikipedia.org/wiki/リファクタリング_\(プログラミング\) "wikilink")、getter, setterメソッドの自動生成や、クラス名・メソッド名の変更(使用しているコード側のクラス名・メソッド名も変更される)、メソッドの移動や抽出などをウィザード形式で行ってくれる。

### コード編集支援

メソッド名の保管や、import文の整理・自動生成、 必要なthrows節の自動追加、必要なメソッドスケルトンの自動生成などさまざまな編集支援機能を持つ。

### フルJ2EEエンジン内蔵

サーブレット・JSPコンテナ、EJBコンテナとなりうるテスト用J2EEエンジンを内蔵。JDeveloperだけでフルのJ2EE開発・実行・テストが可能。

### UML対応

クラス図・アクティビティ図のダイアグラムが標準で用意されている。コードとモデルは完全同期する。

## データアクセス・フレームワーク

データベースとのデータのやり取り、そのデータの転送、セッション管理などの一通りのデータアクセスに関する機能をJ2EEデザイン・パターンを実装して提供している。このフレームワークを利用すれば、何も考えなくてもそれなりのJ2EEデータアクセス・アプリケーションを実現できる。

## 他の統合環境との比較

J2EE用のIDEという点では、基本機能はどの統合環境もほぼ同等。JDeveloperは以下の点で他にはない特徴を持つ。

  - フルJ2EEエンジン内蔵
  - フレームワーク・ベースでの開発が可能
  - SQL対応度が高い

## 外部リンク

  - [Oracle JDeveloper](http://www.oracle.com/technetwork/jp/developer-tools/jdev/overview/)

[Category:Java開発ツール](https://ja.wikipedia.org/wiki/Category:Java開発ツール "wikilink") [Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:オラクル](https://ja.wikipedia.org/wiki/Category:オラクル "wikilink")