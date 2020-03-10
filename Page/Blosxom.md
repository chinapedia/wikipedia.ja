> この記事は[Blosxom](https://ja.wikipedia.org/wiki/Blosxom)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Etech05_Rael.jpg "wikilink") **blosxom**（ブロッサム）は、[Rael Dornfest](https://ja.wikipedia.org/wiki/:en:Rael_Dornfest "wikilink") により開発された[オープンソース](../Page/オープンソース.md "wikilink")の[ブログ](../Page/ブログ.md "wikilink")用ソフトウェアである。[Perl](../Page/Perl.md "wikilink")で記述され、[ウェブサーバから](../Page/Webサーバ.md "wikilink")[CGIを経由して動作する](../Page/Common_Gateway_Interface.md "wikilink")。発音は英語の*blossom*と同じ。[BSDスタイルのライセンスで配布されている](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")。

## 特徴

blosxomは、単純で小さな単一のスクリプトで最小限の機能しか備わっていないため、動作に必要な条件は最小限である。導入手順も、ブログのメタ情報などを設定して実行権限を付与し、数個のディレクトリを作成するのみである。記事の投稿は、[テキストファイル](https://ja.wikipedia.org/wiki/テキストファイル "wikilink")を所定のディレクトリに配置するのみで、blosxomはファイルの1行目をタイトルとして、ファイルの更新日時を投稿された日時として表示を行う。年、月、日などでの表示、カテゴリ別にディレクトリを分けることによりディレクトリ名をカテゴリ名として指定しての表示をすることができる。

表示、機能もデフォルトでは最低限の機能しかないが、表示に関しては、フレーバー(flavor)と呼ばれるテンプレートを、機能に関しては[プラグイン](../Page/プラグイン.md "wikilink")を使用して、カスタマイズ、拡張を行うことができる。[RSS](../Page/RSS.md "wikilink")などの[フィード](https://ja.wikipedia.org/wiki/フィード "wikilink")は、基本的にフレーバーの機能を用いて提供する。機能拡張用のプラグインは多数公開されている。

## プラグイン

blosxomのプラグインのアーキテクチャは柔軟で、多数の公開されたプラグインを使用することにより他の高機能なブログ用のソフトウェアと遜色ない機能を付加することができる。

プラグインはごく単純なものから大規模なものまでさまざまなものが公開されている。同種のソフトウェアではあたりまえの機能でも、blosxomにおいてはプラグインを必要とする機能は多い。カテゴリやタグに関するもの、ページ遷移に関するもの、ファイルを更新すると投稿日が変更されてしまうことを抑止するもの、トラックバック、コメントの機能を拡張するもの、ウェブブラウザからの投稿を実現するもの、投稿形式に[軽量マークアップ言語](https://ja.wikipedia.org/wiki/軽量マークアップ言語 "wikilink")を使用するためのもの、記事一覧を生成するものなどがある。

## そのほかのblosxom

blosxomのアイデアを用いたソフトウェアがさまざまな言語で開発された。[Python](../Page/Python.md "wikilink")で記述された[PyBlosxom](https://ja.wikipedia.org/wiki/PyBlosxom "wikilink")、[Apacheモジュールとして実装された](../Page/Apache_HTTP_Server.md "wikilink")、mod_blosxomをはじめとして[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、[PHPによる実装もある](../Page/PHP_\(プログラミング言語\).md "wikilink")。

## 脚注

## 外部リンク

  - [Official Blosxom website](http://blosxom.sourceforge.net/)
  - [PyBlosxom](http://pyblosxom.sourceforge.net/) - Pythonによる実装
  - [mod_blosxom](http://mod-blosxom.sourceforge.net/cgi-bin/blosxom/ja/) - blosxom の機能をそのまま使える Apacheのモジュール

[Category:ブログソフト](https://ja.wikipedia.org/wiki/Category:ブログソフト "wikilink") [Category:Perl](https://ja.wikipedia.org/wiki/Category:Perl "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")