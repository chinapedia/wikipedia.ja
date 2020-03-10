> この記事は[Star Ruby](https://ja.wikipedia.org/wiki/Star_Ruby)から翻訳されています。


**Star Ruby**（スタールビー）とは、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")[スクリプト言語](../Page/スクリプト言語.md "wikilink") [Ruby](../Page/Ruby.md "wikilink")の、2Dゲーム開発のための拡張ライブラリである。星一によって開発された。[スーパーファミコン](../Page/スーパーファミコン.md "wikilink")風のゲームを開発することを目的としている。

## 特徴

### 描画

減色、加色、彩度変更、色相回転などの色調を変更するエフェクトや、拡大縮小、回転などの幾何変換まで、豊富なエフェクトが自由に使える。加算、減算合成、マスク処理なども可能である。

スーパーファミコンのゲームでよく使われる透視座標変換を、Star Rubyでは簡単に実現できる。

Star Rubyの描画の基本概念は、「テクスチャ」と呼ばれるオブジェクトしかない。[PNG画像ファイル](../Page/Portable_Network_Graphics.md "wikilink")、最終出力画面、中間バッファすべてがテクスチャである。つまり、ほとんどの描画操作が「テクスチャからテクスチャへの描画」だけで済む。さらに、テクスチャ描画の際、描画エフェクトを自由にかけることができる。

テクスチャはフルカラー、[αチャンネル付きの](../Page/アルファチャンネル.md "wikilink")[32ビット](https://ja.wikipedia.org/wiki/32ビット "wikilink")[ビットマップ](https://ja.wikipedia.org/wiki/ビットマップ画像 "wikilink")。 PNG形式のファイルとして出力することが可能である。

### 入力

[キーボード](https://ja.wikipedia.org/wiki/キーボード_\(コンピュータ\) "wikilink")、[ゲームパッド](https://ja.wikipedia.org/wiki/ゲームパッド "wikilink")、[マウスに対応している](../Page/マウス_\(コンピュータ\).md "wikilink")。

### サウンド

[Ogg](https://ja.wikipedia.org/wiki/Ogg "wikilink")、 [WAV](https://ja.wikipedia.org/wiki/WAV "wikilink")の形式に対応している。 [BGMの一時停止](https://ja.wikipedia.org/wiki/バックグラウンドミュージック "wikilink")、途中からの再生が可能。

### マルチプラットフォーム

[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")で動作する。

### 他のライブラリとの連携　

各クラスは、ゲームに限らずなるべく独立して使えるように設計されている。 たとえば、 [GUIライブラリであるRuby](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")-GNOME2などのウィンドウに、 Star RubyのTextureを描画することも可能となっている。

### オープンソース

[MITライセンス](https://ja.wikipedia.org/wiki/MITライセンス "wikilink")を採用している。ただし、ライセンスが[LGPLである](../Page/GNU_Lesser_General_Public_License.md "wikilink")[SDL](../Page/SDL.md "wikilink")を使用しているので、それらを含めて全体としてはLGPLとなる。

## 関連項目

他のRubyベースのゲームライブラリ。

  - [Miyako](https://ja.wikipedia.org/wiki/Miyako "wikilink")
  - [MyGame](https://ja.wikipedia.org/wiki/MyGame "wikilink")

## 外部リンク

  - [Star Ruby公式サイト](http://www.starruby.info/)

[Category:Ruby](https://ja.wikipedia.org/wiki/Category:Ruby "wikilink") [Category:ゲーム開発](https://ja.wikipedia.org/wiki/Category:ゲーム開発 "wikilink")