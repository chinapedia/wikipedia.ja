> この記事は[XRender](https://ja.wikipedia.org/wiki/XRender)から翻訳されています。


**X Rendering Extension**(RenderまたはXRender)は、[X Window Systemが](../Page/X_Window_System.md "wikilink")[アルファチャンネル](../Page/アルファチャンネル.md "wikilink")処理を行うための拡張である。

## 歴史

最初のリリースは[2000年](../Page/2000年.md "wikilink")の[XFree86](../Page/XFree86.md "wikilink") Version 4.0.1で、[キース・パッカード](https://ja.wikipedia.org/wiki/キース・パッカード "wikilink")によって書かれた。

## 特徴

XRenderはいくつかの描画処理と、[アルファブレンディング](https://ja.wikipedia.org/wiki/アルファブレンディング "wikilink")を提供する。現在は主としてフォントの[アンチエイリアス](../Page/アンチエイリアス.md "wikilink")に実装されているが、透過処理や影を落とす処理などへの実装も予定されている。

幾何的な図形はクライアント側で[三角形](../Page/三角形.md "wikilink")か[台形](../Page/台形.md "wikilink")のどちらかにテッセレーション(tessellation:複雑な図形を単純な図形に分割すること)されて描画される。テキストは字形データをグループ化してXサーバへ渡し、描画する。その際、座標指定は、32ビットの[固定小数点座標で指定する](../Page/固定小数点数.md "wikilink")。

## 性能

XRenderは新しい[ビデオカード](../Page/ビデオカード.md "wikilink")の3Dの拡張性を視野に設計されている。

## 外部リンク

  - [The X Rendering Extension](http://www.x.org/releases/current/doc/renderproto/renderproto.txt) - 仕様書
  - [The Xrender Library](http://www.x.org/releases/current/doc/libXrender/libXrender.txt) - アプリケーション側から使用するためのライブラリ
  - [A New Rendering Model for X](http://www.keithp.com/~keithp/talks/usenix2000/render.html) (キース・パッカード、[USENIX](../Page/USENIX.md "wikilink") 2000)
  - [High Performance X Servers in the Kdrive Architecture](http://www.usenix.org/events/usenix04/tech/freenix/full_papers/anholt/anholt_html/) (Eric Anholt, [USENIX](../Page/USENIX.md "wikilink") '04)
  - [Xorg Glossary](http://wiki.x.org/wiki/XorgGlossary) ([X.Org](https://ja.wikipedia.org/wiki/X.Org "wikilink"))

[Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:Freedesktop.org](https://ja.wikipedia.org/wiki/Category:Freedesktop.org "wikilink")