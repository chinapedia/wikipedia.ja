> この記事は[ \(DTP\)](https://ja.wikipedia.org/wiki/_\(DTP\))から翻訳されています。


**レイヤー** (*Layer*) とは、[グラフィックソフトウェア](../Page/グラフィックソフトウェア.md "wikilink")などに搭載されている、[画像](../Page/画像.md "wikilink")を[セル画](../Page/セル画.md "wikilink")のように重ねて使うことができる機能のことである。**レイヤ**とも呼ばれる。日本語では層、重ね合わせの意味である。[Adobe Photoshopや](../Page/Adobe_Photoshop.md "wikilink")[Painter](../Page/Painter.md "wikilink")などの商用ソフトだけではなく、フリーのグラフィックソフトウェア（[GIMP](../Page/GIMP.md "wikilink")など）にも搭載されているものがある。

## 概念

例えば、今2枚のガラスがあったとして、1枚目に「あ」、2枚目に「い」と描いたとしよう。この「あ」と描かれたガラスの上のちょうど良い位置に「い」と描かれたガラスを置けば、「あい」という文字列が完成する。このときのそれぞれのガラスがレイヤーである。

このとき、一枚目のみに「あい」と描いた場合、例えば「あ」を大きく描きたい、「い」をもっと右に移動したい、といった場合に各文字を消さなければならない。しかし、レイヤーを使えばそれぞれ「あ」レイヤーを拡大するだけ、「い」レイヤーを右に移動するだけで済む。このような単純な例では レイヤーを使うことにより受けられる恩恵は比較的小さいが、複数枚の写真をレイヤーとして重ねるような場合においては、それぞれのレイヤーを個別に編集可能であることが大きな意味を持つようになる。

|                                                                                          |   |                                                                                             |
| ---------------------------------------------------------------------------------------- | - | ------------------------------------------------------------------------------------------- |
| [LayersLeft.jpg](https://ja.wikipedia.org/wiki/File:LayersLeft.jpg "fig:LayersLeft.jpg") | ⇔ | [LayersRight.jpg](https://ja.wikipedia.org/wiki/File:LayersRight.jpg "fig:LayersRight.jpg") |
| レイヤーを使えば、レイヤーを[D\&Dで移動するだけで済む](../Page/ドラッグ・アンド・ドロップ.md "wikilink")。                     |   |                                                                                             |

## デメリット

レイヤーは使う枚数の分だけ余計に[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")を消費するので、枚数が極端に多くなるとメモリ不足を招くことがある。

## 合成オプション

### 不透明度

不透明度は、レイヤーごとに数値を設定する。通常は100%で、これを0%に近づけるほど設定レイヤーが透明に近づく（すなわち、下位のレイヤーが見えるようになる）。0%で全く見えなくなる。

|                                                                                                               |
| ------------------------------------------------------------------------------------------------------------- |
| [LayersTransparent.jpg](https://ja.wikipedia.org/wiki/File:LayersTransparent.jpg "fig:LayersTransparent.jpg") |
| 不透明度を使った合成                                                                                                    |

### マスク

マスクは、レイヤーごとに[モノクロ画像を設定し](../Page/モノクローム.md "wikilink")、レイヤーの一部（マスクが黒い部分）を隠すことができる。[αチャンネルの一種だが](../Page/アルファチャンネル.md "wikilink")、レイヤー自体のαチャンネルとは別個に設定できる。

|                                                                                                |    |                                                                                                |   |                                                                                                            |    |                                                                                             |
| ---------------------------------------------------------------------------------------------- | -- | ---------------------------------------------------------------------------------------------- | - | ---------------------------------------------------------------------------------------------------------- | -- | ------------------------------------------------------------------------------------------- |
| [Layer-masks1.jpg](https://ja.wikipedia.org/wiki/File:Layer-masks1.jpg "fig:Layer-masks1.jpg") | \+ | [Layer-masks2.jpg](https://ja.wikipedia.org/wiki/File:Layer-masks2.jpg "fig:Layer-masks2.jpg") | × | [Layer-masks-mask.jpg](https://ja.wikipedia.org/wiki/File:Layer-masks-mask.jpg "fig:Layer-masks-mask.jpg") | \= | [Layer-masks.jpg](https://ja.wikipedia.org/wiki/File:Layer-masks.jpg "fig:Layer-masks.jpg") |
| 元画像                                                                                            |    | レイヤー                                                                                           |   | マスク                                                                                                        |    | 結果                                                                                          |

[ラスタイメージのラスタマスクと](../Page/ビットマップ画像.md "wikilink")[ベクタイメージのベクタマスクがあり](https://ja.wikipedia.org/wiki/ベクタ形式 "wikilink")、ソフトによっては共に備える。

### 描画モード

描画モード（ブレンドモード）は、レイヤーごとにいずれかから選択する。ピクセルを合成する際に、演算方法を変更するもの。乗算、スクリーン、オーバーレイなどのほかに、ソフトウェアごとに特有のモードが存在する。不透明度と組み合わせることによって様々な効果を出すことができる。それぞれのモードには「暗くなる」「黒と組み合わせると影のような色を表現できる」といったような特色があるが、モードを使いこなすには若干の慣れが必要である。

基本的な描画モードには以下のようなものがある。名称はソフトによって異なるものもあるが、[Photoshop日本語版と英語版の名称を最初に記した](../Page/Adobe_Photoshop.md "wikilink")。数式は[C言語](../Page/C言語.md "wikilink")風[擬似コード](../Page/擬似コード.md "wikilink")で、x が元画像の、y が合成するレイヤーの、[RGB](../Page/RGB.md "wikilink")（など）それぞれの値を表す。

| 名称        | 数式                                                                                                  | 用途例                                        |
| --------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------ |
| 通常 ()、標準  | y                                                                                                   | 普通の重ね合わせ。                                  |
| 乗算 ()     | x\*y                                                                                                | [影](../Page/影.md "wikilink")の合成。           |
| スクリーン ()  | 1-((1-x)\*(1-y))                                                                                    | [ハイライトの合成](../Page/鏡面ハイライト.md "wikilink")。 |
| オーバーレイ () | x\<.5 [?](../Page/条件演算子.md "wikilink") 2\*x\*y [:](../Page/条件演算子.md "wikilink") 1-2\*((1-x)\*(1-y)) | [模様](../Page/模様.md "wikilink")の合成。         |
| 比較(暗) ()  | [min](../Page/最大と最小.md "wikilink")(x,y)                                                             |                                            |
| 比較(明) ()  | [max](../Page/最大と最小.md "wikilink")(x,y)                                                             |                                            |
| 差の絶対値 ()  | [abs](https://ja.wikipedia.org/wiki/絶対値 "wikilink")(x-y)                                            | 違いの確認。                                     |

## レイヤー機能があるフリーのグラフィックソフトウェア

  - [GIMP](../Page/GIMP.md "wikilink") - Linux、Windows、MacOSそれぞれに対応している。
  - [PictBear](https://ja.wikipedia.org/wiki/PictBear "wikilink") [1](http://sleipnir.pos.to/software/pictbear/index.html) - Windows用。
  - [Pixia](../Page/Pixia.md "wikilink") - Windows用。

## 関連項目

  - [CAD](../Page/CAD.md "wikilink")（同様のレイヤーの概念を持つ）

[Category:画像処理](https://ja.wikipedia.org/wiki/Category:画像処理 "wikilink") [Category:DTP](https://ja.wikipedia.org/wiki/Category:DTP "wikilink")