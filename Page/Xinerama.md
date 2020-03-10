> この記事は[Xinerama](https://ja.wikipedia.org/wiki/Xinerama)から翻訳されています。


[Xinerama_4way.jpg](https://ja.wikipedia.org/wiki/File:Xinerama_4way.jpg "fig:Xinerama_4way.jpg") を四つのモニターで表示する Xinerama\]\] **Xinerama** は [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") などの [Unix系](../Page/Unix系.md "wikilink") OS で動作する [X サーバの拡張であり](../Page/X_Window_System.md "wikilink")、複数の[ディスプレイが大きな単独のディスプレイのように振る舞うことができるようになる](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")。それにより、複数のモニター上に表示される大きなデスクトップを [X Window System](../Page/X_Window_System.md "wikilink") が使えるようになる。この拡張は [XFree86](../Page/XFree86.md "wikilink")/[X.Org](../Page/X.Org_Server.md "wikilink") X11 リリース 6 バージョン 4.0 から存在する。

## 機能

[Xnest_Xinerama.png](https://ja.wikipedia.org/wiki/File:Xnest_Xinerama.png "fig:Xnest_Xinerama.png") により仮想スクリーンを作り、四つのモニターを使った Xinerama 構成のように振る舞うことができる。 この例では正方形に並べられ、ウィンドウを覆う四つのすべてのスクリーンが表示されている。\]\] X Window System では原則的に任意の数のモニターが使える。しかし X Window System 内のこれらの*スクリーン*は独立したものとみなされる。これらは全く異なる性能を持つことができるので、例えば異なる[解像度](https://ja.wikipedia.org/wiki/解像度 "wikilink")や[色深度](../Page/色深度.md "wikilink")で表示できる。技術的に見ると個々のスクリーンは固有のルートウィンドウをもっている。X Window System ではルートウィンドウを除く個々のウィンドウには親ウィンドウが必要であり、なければ表示できない。Xinerama 拡張によりすべてのスクリーンは大きなウィンドウに統合され、ルートウィンドウを覆う大きなすべてのウィンドウが生じる。こうなるとウィンドウを好きなようにスクリーンに重ねられる。

互換性のある[ウィンドウマネージャ](https://ja.wikipedia.org/wiki/ウィンドウマネージャ "wikilink")は Xinerama からモニター設定について通知を受ける。これらの情報により、個々のウィンドウの境界を越えないようにウィンドウを置くことができる。

## 関連項目

  - [マルチモニター](https://ja.wikipedia.org/wiki/マルチモニター "wikilink") - 一つのコンピュータに複数の[ディスプレイ](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")

## 外部リンク

  - [公式サイト](http://sourceforge.net/projects/xinerama/)

[Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:freedesktop.org](https://ja.wikipedia.org/wiki/Category:freedesktop.org "wikilink")