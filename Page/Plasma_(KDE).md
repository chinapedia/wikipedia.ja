> この記事は[Plasma \(KDE\)](https://ja.wikipedia.org/wiki/Plasma_\(KDE\))から翻訳されています。


**Plasma**（プラズマ）は、[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")の[KDE](../Page/KDE.md "wikilink")の[グラフィカルシェル](https://ja.wikipedia.org/wiki/グラフィカルシェル "wikilink")である。KDE 4以前のバージョンにおけるKDesktopシェル、[Kicker](https://ja.wikipedia.org/wiki/Kicker "wikilink")タスクバーや[SuperKaramba](../Page/SuperKaramba.md "wikilink")ウィジェットエンジンから、一つの統一されたワークスペースに置き換えるという、KDE 4へのメジャーバージョンアップに伴う大きな変更の一つであった。その他に、画面の解像度に依らないインターフェイスを導入し、どの画面の大きさや解像度であってもデスクトップの表示を理想的なものにすること、などの目的を持って設計されている。

Plasmaのアプレットは*Plasmoid*と呼ばれ、情報の表示を行うウィジェットや電卓、辞書のようなアプリケーションなどがある。

Plasmaの重要な機能の一つには、タスクバーのようなパネル、デスクトップアイコンやウィジェットは同じ方法で作成されるようになるため、それらをもはや区別しないということが挙げられる。

Plasmaにおいて、各コンポーネントは「データエンジン」とコンポーネントの表示を担当する部分に分けられる。これによって、与えられたデータを表示しようとする際に必要なプログラミングの労力を削減することや、データエンジンとヴィジュアル面のコードを独立して容易に記述できるようにすることが意図されている。KDE 4の後期に[Kmenu](https://ja.wikipedia.org/wiki/Kmenu "wikilink")を置き換える[Raptor](https://ja.wikipedia.org/wiki/Raptor "wikilink")は、Plasmaを積極的に利用することが見込まれている。

## 機能

Plasmaは“コンテナ”と呼ばれる「他のアプレットを含むアプレット」を扱うことができる。コンテナの例にはデスクトップの背景とタスクバーを挙げられる。コンテナは画像やSVG、動画、[OpenGL](../Page/OpenGL.md "wikilink")など開発者が任意に構成できる。コンテナには主に画像が用いられるが、ユーザーはどのアプレットでもその機能を損なうことなくデスクトップの背景に指定することが可能。

また、アプレットはデスクトップとタスクバー（すなわち、2つの異なるコンテナ）間でドラッグして移動することが可能であり、タスクバーと分割して表示することができる。

Plasmaのウィジェットはスケーラブルであるため、どんなサイズへの変更や回転もわずかな時間で再描画できる。また、[Kross](../Page/Kross.md "wikilink")スクリプティング・フレームワークが導入されるため、開発者はウィジェットを[C++](../Page/C++.md "wikilink")以外のプログラミング言語でも記述できるようになると見られている\[1\]。 また、ウィジェットは自身のサイズを認識できるので、それに合わせた情報量を表示できる。

Plasmaは他のウィジェットもサポートする。SuperKaramba（KDE 3シリーズで使われていたウィジェットエンジン）は既にサポートされており、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")に搭載されている[Dashboard](../Page/Dashboard.md "wikilink")や、[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")ブラウザウィジェットはKDE 4の以降のリリースでサポートされることが予想されている\[2\]。

## ロードマップ

Plasmaに予定されている改良点のほぼ全ては、キャンバスモジュールによるウィジェット表示機能やウィジェット内部で[HTMLや](../Page/HyperText_Markup_Language.md "wikilink")[CSSを容易にレンダリングするためQtに移植された](../Page/Cascading_Style_Sheets.md "wikilink")[WebKit](../Page/WebKit.md "wikilink")など、Qt 4.4に含まれる新機能を利用するものである。

他にもドキュメントの整備や既存のウィジェットの改善、冗長コードの置き換え作業などが行われる予定である。

## 脚注

<references />

## 外部リンク

  - [Plasma公式ページ](http://plasma.kde.org/)
  - [Plasma開発者向けwiki](http://techbase.kde.org/Projects/Plasma)
  - [Plasmaスクリーンショット](http://youtube.com/results?search_query=plasma+kde)
  - [Linux.comによるPlasma紹介記事](http://www.linux.com/feature/114560)
  - [\#plasma](irc://irc.kde.org/plasma) IRCチャンネル

[Category:KDE](https://ja.wikipedia.org/wiki/Category:KDE "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ウィジェット](https://ja.wikipedia.org/wiki/Category:ウィジェット "wikilink")

1.  [Linux.com :: KDE's Plasma is heating up](http://www.linux.com/feature/114560)
2.  [commit-digest.org - 22nd July 2007](http://commit-digest.org/issues/2007-07-22/)