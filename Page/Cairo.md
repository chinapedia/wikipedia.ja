> この記事は[Cairo](https://ja.wikipedia.org/wiki/Cairo)から翻訳されています。


**cairo**（カイロ）は、デバイスに依存しない[ベクトルベースの描画](https://ja.wikipedia.org/wiki/ベクトル画像 "wikilink")[APIを提供する](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、[フリーの](../Page/フリーソフトウェア.md "wikilink")2Dグラフィックス[ライブラリ](../Page/ライブラリ.md "wikilink")である。[アンチエイリアス](../Page/アンチエイリアス.md "wikilink")がかかった綺麗な表示が特徴である。直線、矩形、円弧の他、[ベジェ曲線](../Page/ベジェ曲線.md "wikilink")や文字の描画も可能である。[半透明描画](../Page/アルファブレンド.md "wikilink")、マスクやグラデーション機能がある。ソフトウェアによるテセレーションが基本だが、可能な場合にはハードウェアアクセラレーションを利用するよう設計されている。

## 歴史

[キース・パッカード](https://ja.wikipedia.org/wiki/キース・パッカード "wikilink")、[カール・ワース](https://ja.wikipedia.org/wiki/カール・ワース "wikilink")らによって、X Window Systemに利用するために開発が始められた。当初はXr・Xr/Xcと呼ばれていたが、後にcairoへと変更された。[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")でXに依存しないライブラリである点を強調することを意図したものである。

## バックエンド

出力バックエンドとして [X Window System](../Page/X_Window_System.md "wikilink") (XlibとXCB), [GDI](../Page/Graphics_Device_Interface.md "wikilink") ([Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")), [Quartz](../Page/Quartz.md "wikilink") ([macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")), イメージバッファ, [PostScript](../Page/PostScript.md "wikilink"), [PDF](../Page/Portable_Document_Format.md "wikilink"), [SVG](../Page/Scalable_Vector_Graphics.md "wikilink") をサポートしている。実験的に、[OpenGL](../Page/OpenGL.md "wikilink"), OpenGL ES 2.0, OpenVG, [BeOS](../Page/BeOS.md "wikilink"), [OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink"), [DirectFB](https://ja.wikipedia.org/wiki/DirectFB "wikilink") をサポートしている。

## バインディング

[C言語](../Page/C言語.md "wikilink")が基本APIだが、Ada, C++, Common Lisp, Factor, Haskell, Java, Lua, Mono と .NET, Perl, PHP, Python, Ruby, Scheme, Smalltalk などの[バインディングが存在する](https://ja.wikipedia.org/wiki/言語バインディング "wikilink")\[1\]。

## 採用例

  - [GTK](../Page/GTK_\(ツールキット\).md "wikilink") - バージョン2.8以降、cairoを用いてWidgetの描画を行っている。
  - [Mozilla](../Page/Mozilla.md "wikilink"), [Firefox](../Page/Mozilla_Firefox.md "wikilink") - レンダリングエンジン[Gecko](../Page/Gecko.md "wikilink")の描画にcairoを採用。
  - [Poppler](../Page/Poppler.md "wikilink") - cairo を用いたPDF描画ライブラリ。
  - [OpenOffice.org](../Page/OpenOffice.org.md "wikilink")
  - [GIMP](../Page/GIMP.md "wikilink")

## 関連項目

  - [Skia](https://ja.wikipedia.org/wiki/Skia "wikilink") - [Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink") や [Android](../Page/Android.md "wikilink") で使用

## 参照

<references />

## 外部リンク

  -
[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Freedesktop.org](https://ja.wikipedia.org/wiki/Category:Freedesktop.org "wikilink") [Category:グラフィックライブラリ](https://ja.wikipedia.org/wiki/Category:グラフィックライブラリ "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:GTK+](https://ja.wikipedia.org/wiki/Category:GTK+ "wikilink")

1.  [Language bindings](http://cairographics.org/bindings/)