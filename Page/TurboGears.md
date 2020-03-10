> この記事は[TurboGears](https://ja.wikipedia.org/wiki/TurboGears)から翻訳されています。


**TurboGears** は、[Python](../Page/Python.md "wikilink") による [Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")である。[MochiKit](https://ja.wikipedia.org/wiki/MochiKit "wikilink")、[SQLObject](https://ja.wikipedia.org/wiki/SQLObject "wikilink")、[CherryPy](https://ja.wikipedia.org/wiki/CherryPy "wikilink")、[Kid](https://ja.wikipedia.org/wiki/Kid "wikilink")などの、基礎となるコンポーネントの上に構築されている。

## 概要

TurboGears は 2005 年、いまだにリリースされていない[Zesty Newsという製品の背後のフレームワークとして](https://ja.wikipedia.org/wiki/Zesty_News "wikilink")、[Kevin Dangoor](https://ja.wikipedia.org/wiki/Kevin_Dangoor "wikilink") によって作られた。

2008 年 2 月現在、TurboGears はメーリングリストに 3000人以上を抱え、2006 年に[Prentice Hallから書籍が出版され](https://ja.wikipedia.org/wiki/Prentice_Hall "wikilink")、多数の[オープンソース](../Page/オープンソース.md "wikilink")およびプロプライエタリの TurboGears アプリケーションが実際に配置されるなど、大規模で健全なコミュニティを持っている。2008 年の PyCon で TurboGears 2 のプレビューリリースが期待されている。

TurboGears は [Struts](https://ja.wikipedia.org/wiki/Apache_Struts "wikilink") や [Ruby on Rails](https://ja.wikipedia.org/wiki/Ruby_on_Rails "wikilink") のように[model-view-controller](https://ja.wikipedia.org/wiki/model-view-controller "wikilink") アーキテクチャを元に設計されており、Pythonによる Web アプリケーションの開発をより簡単でメンテナンスが容易なよう設計されている。

TurboGears のコンポーネントには下記のものがある。

  - [SQLObject](https://ja.wikipedia.org/wiki/SQLObject "wikilink") : **Model** として利用 - データベースや多数の既存のデータベースサーバとのインターフェイスを作成可能なデータバックエンド
    [Kid](https://ja.wikipedia.org/wiki/Kid_\(Templating_Language\) "wikilink") : **View** として利用 - XHTML フロントエンドのテンプレートエンジンで、すべてのテンプレートが妥当な XHTML ないし XML ファイルで、テンプレートを検証や設計が簡単なシンプルなXHTML ファイルとして開くことができるように作れられている。また、Python の[スニペット](https://ja.wikipedia.org/wiki/スニペット "wikilink")を XML 的な方法で埋め込むための機能も提供されている。
    [CherryPy](https://ja.wikipedia.org/wiki/CherryPy "wikilink") : **Controller** として利用 - (TurboGearsでは)テンプレートに対してデータを返却するイベントハンドラを記述することでWebアプリケーションをプログラム可能にするミドルウェア。同じデータを[JSONデータストリームとして](https://ja.wikipedia.org/wiki/JavaScript_Object_Notation "wikilink")[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")的な方法で取得することもできる。
    [MochiKit](https://ja.wikipedia.org/wiki/MochiKit "wikilink") : は TurboGears の付属的な部分で、JavaScript によるプログラミングをより[Pythonic](https://ja.wikipedia.org/wiki/Pythonic "wikilink")に(Pythonらしく)するための JavaScript ライブラリである。JSON データストリームを非同期的に取得するインターフェイスを提供するため、もっぱら[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")機能を実現するために使用されている。

## テンプレートプラグイン

Kid 以外のテンプレート言語もプラグインシステムを介して使用することができる。現在、[Cheetah](https://ja.wikipedia.org/wiki/Cheetah "wikilink")、[Django](../Page/Django.md "wikilink")、[Genshi](https://ja.wikipedia.org/wiki/Genshi "wikilink")、[Jinja](https://ja.wikipedia.org/wiki/Jinja "wikilink") 向けのプラグインが存在する。複数のテンプレートエンジンを同じアプリケーション内で使うことも可能である。

## TurboGears の特徴

2007 年 1 月、Kevin Dangoor がプロジェクトリーダーを引退し、現在 [Alberto Valverde](https://ja.wikipedia.org/wiki/Alberto_Valverde "wikilink") が彼の後継者としてプロジェクトを運営している。\[1\]

TurboGears 2.0 に向けて開発が始まっており、2.0 ではSQLObject を [SQLAlchemy](https://ja.wikipedia.org/wiki/SQLAlchemy "wikilink") に置き換え、Kid を [Genshi](https://ja.wikipedia.org/wiki/Genshi "wikilink") に置き換えることを目標としている。これらのコンポーネントはソフトウェアの他の部分と密結合しているため、特にデータベースのフロントエンド "Catwalk" に関して、既存のコードベースを多数書き直す必要がある。

2007 年 6月、TurboGears のコミュニティは、TurboGears API を[Pylons](https://ja.wikipedia.org/wiki/Pylons "wikilink")で使用されているコンポーネントとプロトコル上に移植する実験を開始した。また、二つのフレームワークがやがて一つになるのではないかという予想もある。\[2\]

## 関連書籍

Ramm, M (Nov 7, 2006). Rapid Web Applications with TurboGears, Prentice Hall. ISBN 0132433885

## 参照

<div class="references-small">

<references/>

</div>

## 関連項目

  - [フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")
  - [Pythonを使っている製品あるいはソフトウェアの一覧](../Page/Pythonを使っている製品あるいはソフトウェアの一覧.md "wikilink")

## 外部リンク

  -
  - [TurboGears Blogs](http://planet.turbogears.org/)

  - [TurboGears google group](https://groups.google.com/forum/#!forum/turbogears)

  - [TurboGears screencasts](http://showmedo.com/videotutorials/TurboGears) and related videos

  - [TurboGears from start to finish](http://lucasmanual.com/mywiki/TurboGears)

[Category:ウェブアプリケーション](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーション "wikilink") [Category:Python](https://ja.wikipedia.org/wiki/Category:Python "wikilink")

1.
2.