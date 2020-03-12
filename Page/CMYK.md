> この記事は[CMYK](https://ja.wikipedia.org/wiki/CMYK)から翻訳されています。


[CMYK_color_swatches.svg](https://ja.wikipedia.org/wiki/File:CMYK_color_swatches.svg "fig:CMYK_color_swatches.svg") [Synthese-.svg](https://ja.wikipedia.org/wiki/File:Synthese-.svg "fig:Synthese-.svg") [Refill_Ink_Kit_Color_crop.jpg](https://ja.wikipedia.org/wiki/File:Refill_Ink_Kit_Color_crop.jpg "fig:Refill_Ink_Kit_Color_crop.jpg")をしている。\]\] **CMYK**（または**CMYKカラーモデル**）は、[シアン](../Page/シアン_\(色\).md "wikilink")、[マゼンタ](../Page/マゼンタ.md "wikilink")、[イエロー](../Page/黄色.md "wikilink")、[ブラックの](https://ja.wikipedia.org/wiki/黒 "wikilink")4成分によって色を表す[色](../Page/色.md "wikilink")の表現法の一種である。

は、シアン（）、マゼンタ（）、イエロー（）と、キー・プレート（）から、頭文字1字を取ったものである。キー・プレートは、他の印刷の合わせになる版のことで、通常、文字や図の輪郭を表す黒で印刷される。CMYKの""が、ブルー（）と混同しないようにブラック（）の"K"を用いたものであるとか、[日本語](../Page/日本語.md "wikilink")の黒（）に由来するという説明は誤りである\[1\]。ただし、CMYKはと表記されることもあり、この場合の はブラックを指す。

|      |              |          |
| ---- | ------------ | -------- |
| 色名   | ウェブカラー（モニター） | プロセスカラー  |
| シアン  | \#00FFFF     | \#00AEEF |
| マゼンタ | \#FF00FF     | \#EC008C |
| イエロー | \#FFFF00     | \#FFF500 |

## 概要

[Newspaper-cmyk2.jpg](https://ja.wikipedia.org/wiki/File:Newspaper-cmyk2.jpg "fig:Newspaper-cmyk2.jpg")のテレビ欄に印刷されているCMYKカラーチップ。左の縦列は100%、右は50%を示す。コンマ数ミリ単位ではあるが、それぞれの色版の印刷に多少のズレが生じているのが分かる。</SMALL>\]\] CMYKは[CMYから派生した](https://ja.wikipedia.org/wiki/色空間#CMY "wikilink")、[減法混合](https://ja.wikipedia.org/wiki/減法混合 "wikilink")に基づく色の表現法である。理論上では[CMY](https://ja.wikipedia.org/wiki/CMY "wikilink")によって全ての色を表現できるはずであるが、実際にはCMYのインクを混合して綺麗な[黒](https://ja.wikipedia.org/wiki/黒 "wikilink")色を表現するのは技術的に困難であり、せいぜい鈍い暗色にしかならない。このため、[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")などの印刷機で[黒](https://ja.wikipedia.org/wiki/黒 "wikilink")色をより美しく表現する目的として**CMYK**が採用されている。また見た目の美しさ以外にも、黒を表現するのに必要なインク量が少なくなるためにCMYの場合と比べてランニングコストが下がる、乾燥が速く高速印刷に向く、といった利点がある。

なお、[インクジェットプリンター](../Page/インクジェットプリンター.md "wikilink")などでは、階調表現力を良くするために通常のCMYKに加えて淡いシアン・淡いマゼンタ・[グレー](https://ja.wikipedia.org/wiki/グレー "wikilink")などの追加インクを使用する場合がある\[2\]。これらは使用される追加インクの色やインクの数に関わらず、色の表現法としてはCMYKとの違いはない。

## CMYKとRGBの違い

[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")などで撮影された[画像](../Page/画像.md "wikilink")、あるいは[パソコンの](../Page/パーソナルコンピュータ.md "wikilink")[ディスプレイ上に表現される色は](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")[ライトの発光を利用して色を表現](https://ja.wikipedia.org/wiki/照明器具 "wikilink")（[加法混合](https://ja.wikipedia.org/wiki/加法混合 "wikilink")）する[RGB](../Page/RGB.md "wikilink")形式であるが、印刷物では[インク](../Page/インク.md "wikilink")（[色素](../Page/色素.md "wikilink")）による光の吸収を利用して色を表現している（減法混合）。このように、画面と紙とでは発色の原理が全く異なる為、RGB形式の画像を[印刷](../Page/印刷.md "wikilink")する場合はRGB形式からCMYK形式への変換作業が必要となる。

原理的には(C=1-R),(M=1-G),(Y=1-B)でRGB値からCMY値が得られる。さらにK=min(C,M,Y)を求め、(C'=C-K)(M'=M-K),(Y'=Y-K)で、CMYK値を得る。しかし、この計算で得られた濃度を印刷に適用すると、一般的なRGB色空間とCMYK色空間の[γ特性が全く正反対である事が考慮されていないこと](https://ja.wikipedia.org/wiki/ビットマップ画像#.E3.82.AC.E3.83.B3.E3.83.9E.E8.A3.9C.E6.AD.A3 "wikilink")、RGBとCMYKそれぞれの補色の波長が一致していない事などから、印刷結果は全く期待通りとならない（インクジェットシステムで紙に印刷すると、紙に乗り切れなかったインクがプリンターの底に溜まる程である）。この為、それぞれの色空間を[カラーマネージメントシステム](../Page/カラーマネージメントシステム.md "wikilink")で補正する必要がある。通常の画面表示用カラーマネージメントシステムでは、実解像度をリアルタイムで処理すれば良いので精密に再現されるが、プリンターの場合にはきわめて高い解像度と非常に少ないインク液粒（[ピコ](https://ja.wikipedia.org/wiki/ピコ "wikilink")[リットル](../Page/リットル.md "wikilink")単位）やトナー（[ナノ](https://ja.wikipedia.org/wiki/ナノ "wikilink")[グラム](../Page/グラム.md "wikilink")単位）を制御しなければならない事から莫大な量の演算が必要になるため、事前に発色特性を[サンプリングして作った多次元](https://ja.wikipedia.org/wiki/標本化 "wikilink")[ベジェ曲線](../Page/ベジェ曲線.md "wikilink")等によって、特性をシミュレートする事で演算を軽減するなどして、印刷の速度を向上させている。完全な再現は基本的には不可能である事から、あらかじめ印刷対象がどのような物であるか（代表的なプリセット値として自然風景・人物写真・ビジネス文書などが候補として用意されている）をユーザーが手動で指示したり、あるいはプリンタドライバソフトウェアが画像解析によって印刷対象を予測するといった、高度なシステムが実装されている。

## 補足

日本の製版・印刷業界では、永らく**YMCK**という順番で呼ばれてきた。これは、昭和20年頃までのオフセット印刷機でカラー印刷していた際の版の順番が、Y版→M版→C版→K版であったことに由来する。当時のイエローインキ顔料は[クロム酸鉛系の透明度の低いものであり](../Page/クロム酸鉛\(II\).md "wikilink")、他色を隠蔽してしまう恐れがあったためでY版を先にする必要があった。

後に登場した[ジスアゾ系顔料を使った透明度が高いイエローインキでは刷り順は逆に最後にするのが一般的で](https://ja.wikipedia.org/wiki/アゾ化合物#ジスアゾ "wikilink")、2013年現在の刷り順はK-C-M-Y（4色機）、CM-KY（2色機）である。各色の刷り重ね順はカラーマネジメントの上でもこの順で固定され、またオフセットインキ自体もこの刷り順に適するよう調整されている。

## 脚注

## 関連項目

  - [網点](../Page/網点.md "wikilink")
  - [プロセスカラー](../Page/プロセスカラー.md "wikilink")
  - [色空間](../Page/色空間.md "wikilink")
  - [色空間\#CMY](https://ja.wikipedia.org/wiki/色空間#CMY "wikilink")：[色の三原色](https://ja.wikipedia.org/wiki/色の三原色 "wikilink")
  - [RGB](../Page/RGB.md "wikilink")：[光の三原色](https://ja.wikipedia.org/wiki/光の三原色 "wikilink")。主に[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")などで使用される色の表現方法。

[Category:色](https://ja.wikipedia.org/wiki/Category:色 "wikilink") [Category:画像処理](https://ja.wikipedia.org/wiki/Category:画像処理 "wikilink")

1.
2.  [最上位はグレーインクを装備：キヤノン、新インクで発色を向上させた複合機／プリンタ08年モデル](http://www.itmedia.co.jp/pcuser/articles/0809/17/news037.html) ITmedia PC USER、2008年9月17日