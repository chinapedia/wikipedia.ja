> この記事は[Abstract Window Toolkit](https://ja.wikipedia.org/wiki/Abstract_Window_Toolkit)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Easy_Java_AWT_example.jpg "wikilink") **Abstract Window Toolkit** (AWT) とは、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の独自のプラットフォーム非依存な[ウィンドウシステム](https://ja.wikipedia.org/wiki/ウィンドウシステム "wikilink")、[グラフィックス](../Page/コンピュータグラフィックス.md "wikilink")、[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink") (UI)、[ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/ウィジェット・ツールキット "wikilink")のことである。AWTは現在は[Java Foundation Classes](https://ja.wikipedia.org/wiki/Java_Foundation_Classes "wikilink") (JFC) に含まれ、Javaプログラム用[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") (GUI) を提供する標準[APIの一部となっている](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")は1995年にJavaを最初にリリースしたとき、AWTは、下層のネイティブなユーザインタフェース上に薄い抽象化レベルを提供した。例えば、AWTの[チェックボックス](https://ja.wikipedia.org/wiki/チェックボックス "wikilink")を作成する際、AWTはチェックボックスを作成する下層のネイティブサブルーチンを直接呼び出していた。しかしながら、[Microsoft Windowsのチェックボックスは](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Mac OSや様々な](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")[UNIX](../Page/UNIX.md "wikilink")互換OSにおけるチェックボックスとは厳密には同じではなかった。下層のネイティブなウィンドウツールキットに高度に忠実で、ネイティブなアプリケーションとのシームレスな統合を提供することから、[アプリケーション開発者の中にはこのモデルを好む者もいる](../Page/アプリケーションソフトウェア.md "wikilink")。言い換えれば、AWTを使って書かれたGUIプログラムは、Windows上で動作するときはネイティブなWindowsアプリケーションのような外観になるが、Mac上で動作するときはネイティブな[Apple Macintoshアプリケーションのような外観になる](../Page/Macintosh.md "wikilink")、などということである。しかしながら、アプリケーション開発者の中には、全てのプラットフォーム上で開発したアプリケーションが厳密に同じ外観であることを好むため、このモデルを嫌う者もいた。

[J2SE 1.2では](../Page/Java_Platform,_Standard_Edition.md "wikilink")、[Swing](../Page/Swing.md "wikilink")ツールキットがAWTの[ウィジェットの大部分に取って代わった](https://ja.wikipedia.org/wiki/ウィジェット_\(GUI\) "wikilink")。よりリッチなUIウィジェットの集合を提供することに加えて、Swingは、OSの高レベルユーザインタフェースモジュールに依存するのではなく、(ローカルのグラフィックスサブシステムにおける低レベルのサブルーチンを呼び出す[Java 2Dを使用した](https://ja.wikipedia.org/wiki/Java_2D "wikilink")) 独自のウィジェットを描画する。Swingはアプリケーションのために、ネイティブの[ルック・アンド・フィール](https://ja.wikipedia.org/wiki/ルック・アンド・フィール "wikilink")、またはすべてのウィンドウシステム上で同じ外観を持つクロスプラットフォームなルック・アンド・フィール (Java Look and Feel) を使用するオプションを提供する。

AWTはGUIイベントサブシステムとネイティブなウィンドウシステムと、Swingが頼る構造的な土台を提供するJavaアプリケーションとの間のインタフェースの中核の提供を継続する。 それは、サポートシステム上で[システムトレイ](https://ja.wikipedia.org/wiki/システムトレイ "wikilink")にアクセスできるだけでなく、様々な基本[レイアウトマネージャ](https://ja.wikipedia.org/wiki/レイアウトマネージャ "wikilink")、[クリップボード](https://ja.wikipedia.org/wiki/クリップボード "wikilink")や[ドラッグ・アンド・ドロップ](../Page/ドラッグ・アンド・ドロップ.md "wikilink")を使用するデータ転送パッケージ、[マウスや](../Page/マウス_\(コンピュータ\).md "wikilink")[キーボードのような](https://ja.wikipedia.org/wiki/キーボード_\(コンピュータ\) "wikilink")[入力デバイス](https://ja.wikipedia.org/wiki/入力デバイス "wikilink")インタフェースをも提供する。

## 関連項目

  - [Swing](../Page/Swing.md "wikilink")
  - [Standard Widget Toolkit](https://ja.wikipedia.org/wiki/Standard_Widget_Toolkit "wikilink")

## 外部リンク

  - [AWT homepage](http://java.sun.com/products/jdk/awt/)

  - (AWT [Javadoc](https://ja.wikipedia.org/wiki/Javadoc "wikilink") API documentation)

  -
  -
[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/Category:ウィジェット・ツールキット "wikilink")