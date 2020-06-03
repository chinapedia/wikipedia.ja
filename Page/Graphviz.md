> この記事は[Graphviz](https://ja.wikipedia.org/wiki/Graphviz)から翻訳されています。


**Graphviz** (*Graph Visualization Software*) は [AT\&T](../Page/AT&T.md "wikilink")研究所が開発した[オープンソース](../Page/オープンソース.md "wikilink")のツールパッケージであり、[DOT言語](https://ja.wikipedia.org/wiki/DOT言語 "wikilink")で記述された[グラフ構造](../Page/グラフ理論.md "wikilink")（ノードとエッジから成るネットワーク構造）を描画する。パッケージには[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")からツールを使うための[ライブラリ](../Page/ライブラリ.md "wikilink")も含まれる。Graphvizは[Eclipse Public Licenseライセンスで提供される](https://ja.wikipedia.org/wiki/Eclipse_Public_License "wikilink")[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。

## アーキテクチャ

Graphvizはグラフ記述言語である[DOT言語](https://ja.wikipedia.org/wiki/DOT言語 "wikilink")に基づいており\[1\]、DOTファイルを生成・編集する以下のツール群からなる。

  - dot : 有向グラフをレイアウトして各種ファイル形式（[PostScript](../Page/PostScript.md "wikilink")、[PDF](../Page/Portable_Document_Format.md "wikilink")、[SVGなど](../Page/Scalable_Vector_Graphics.md "wikilink")）を生成する[コマンドラインツール](../Page/キャラクタユーザインタフェース.md "wikilink")
    neato : **dot** の無向グラフ版
    twopi : 放射状のレイアウト用
    circo : 環状のレイアウト用
    fdp : もうひとつの無向グラフ用レイアウトツール
    dotty : グラフを視覚化して編集可能とした[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") (GUI)
    lefty : DOTグラフを描画するためのプログラム可能な[ウィジェット](../Page/ウィジェット_\(GUI\).md "wikilink")。ユーザーがマウスを使ってそれらを操作できる。つまり、グラフを使った [Model View Controller型](../Page/Model_View_Controller.md "wikilink") GUI で利用可能である。

## 応用

  - lisp2dot - [LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")プログラムを[DOT言語](https://ja.wikipedia.org/wiki/DOT言語 "wikilink")に変換する。[遺伝的プログラミング](../Page/遺伝的プログラミング.md "wikilink")での利用を意図して設計された。
  - [Doxygen](../Page/Doxygen.md "wikilink") - [C++](../Page/C++.md "wikilink")や[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[Python](../Page/Python.md "wikilink")と連携してGraphVizを使ったクラスの継承関係の図を描画する
  - [GraphViz](https://ja.wikipedia.org/wiki/mw:Extension:GraphViz "wikilink") - MediaWiki GraphViz Extension
  - [MoinMoin wiki GraphViz Extension](http://moinmoin.wikiwikiweb.de/ParserMarket/dot.py)
  - [Linguine Maps Java API to Graphviz](http://www.softwaresecretweapons.com/jspwiki/linguinemaps)
  - [UMLGraph](http://www.umlgraph.org/) 宣言的記述から[UMLのクラス図とシーケンス図を作成する](../Page/統一モデリング言語.md "wikilink")
  - [Friend Explorer](http://www.friendexplorer.net/) Graphviz と [Facebook](../Page/Facebook.md "wikilink") APIを使って[社会的ネットワーク](../Page/社会的ネットワーク.md "wikilink")を描画する
  - [OmniGraffle](https://ja.wikipedia.org/wiki/OmniGraffle "wikilink") ([オムニグラフ 5](http://www.act2.com/products/omni/omni_graffle5/)) Graphviz-ベースのレイアウトエンジンを搭載し、関係図をGUI環境で作成する

## 参考文献

<references />

## 外部リンク

  - [Graphviz 公式ホームページ](http://graphviz.org/)
  - [DOTユーザーズガイド日本語訳](http://www.cbrc.jp/%7Etominaga/translations/index.html#dot)
  - [AT\&T Research Labs](http://www.research.att.com/)
  - [An Introduction to GraphViz and dot (M. Simionato, 2004)](http://www.linuxdevcenter.com/pub/a/linux/2004/05/06/graphviz_dot.html)
  - [Create relationship diagrams with Graphviz (Shashank Sharma, 2005)](http://www.linux.com/article.pl?sid=05/11/08/2018216)

[Category:グラフ作成ソフト](https://ja.wikipedia.org/wiki/Category:グラフ作成ソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink")

1.  <http://www.graphviz.org/doc/info/lang.html>