> この記事は[Glitz](https://ja.wikipedia.org/wiki/Glitz)から翻訳されています。


**glitz** は[2D グラフィックス用の](https://ja.wikipedia.org/wiki/2次元コンピュータグラフィックス "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")であり、[OpenGL](../Page/OpenGL.md "wikilink") という[3Dグラフィックス用の](../Page/3次元コンピュータグラフィックス.md "wikilink") [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") を使って[ハードウェアアクセラレーションを提供する](https://ja.wikipedia.org/wiki/グラフィックアクセラレータ "wikilink")。glitz は[オープンソース](../Page/オープンソース.md "wikilink")ソフトウェアであり、（古い種類の）[MIT License](https://ja.wikipedia.org/wiki/MIT_License "wikilink") のもとで配布されている。開発は [freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink") でホストされている。

glitz はオープンソースのオペレーティングシステム用のグラフィックスで戦略上重要な役割を果たしている\[1\]。

## 提供される機能

glitz は [XRender](https://ja.wikipedia.org/wiki/XRender "wikilink") と同じ機能を提供するように設計されている。

  - [アルファコンポジット](../Page/アルファチャンネル.md "wikilink")
  - [アンチエイリアス](https://ja.wikipedia.org/wiki/アンチエイリアス "wikilink")
  - [サブピクセルレンダリング](https://ja.wikipedia.org/wiki/サブピクセルレンダリング "wikilink")
  - 幾何学的な形やテキストのレンダリング
  - [平行移動](https://ja.wikipedia.org/wiki/平行移動 "wikilink")、[回転](../Page/回転.md "wikilink")や[拡大縮小](https://ja.wikipedia.org/wiki/拡大縮小 "wikilink")といった[幾何学的変換](../Page/変換_\(数学\).md "wikilink")

XRender と同様に、glitz が提供する鍵となる操作は[Porter-Duff コンポジションである](../Page/アルファチャンネル.md "wikilink")。

glitz は XRender の提供しない機能もいくつか提供する。

  - [色のグラデーション](https://ja.wikipedia.org/wiki/色のグラデーション "wikilink")
  - [畳み込み](https://ja.wikipedia.org/wiki/畳み込み "wikilink")フィルター

## glitz を使っているソフトウェア

glitz は [Xgl](https://ja.wikipedia.org/wiki/Xgl "wikilink") X サーバの鍵となるコンポーネントで、現在ほとんどの [Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")に含まれている。

次第に人気の集まっている [Cairo](https://ja.wikipedia.org/wiki/Cairo "wikilink") グラフィックライブラリはバックエンドとして glitz をサポートし、これは数行のコードにより Cairo を使っているすべてのアプリケーションやツールキットはグラフィックスハードウェアを利用できるようになるということである。

## 脚注

[Category:Freedesktop.org](https://ja.wikipedia.org/wiki/Category:Freedesktop.org "wikilink") [Category:OpenGL](https://ja.wikipedia.org/wiki/Category:OpenGL "wikilink")

1.