> この記事は[RGB](https://ja.wikipedia.org/wiki/RGB)から翻訳されています。


[AdditiveColorMixiing.svg](https://ja.wikipedia.org/wiki/File:AdditiveColorMixiing.svg "fig:AdditiveColorMixiing.svg") [RBG_color_wheel-ja.svg](https://ja.wikipedia.org/wiki/File:RBG_color_wheel-ja.svg "fig:RBG_color_wheel-ja.svg") [Spectrum4websiteEval.png](https://ja.wikipedia.org/wiki/File:Spectrum4websiteEval.png "fig:Spectrum4websiteEval.png")\]\] **RGB**（または**RGBカラーモデル**）とは、[色](../Page/色.md "wikilink")の表現法の一種で、[赤](../Page/赤.md "wikilink") (**R**ed)(<span style="color:#FF0000">●</span>)、[緑](../Page/緑.md "wikilink") (**G**reen)(<span style="color:#00FF00">●</span>)、[青](../Page/青.md "wikilink") (**B**lue)(<span style="color:#0000FF">●</span>) の三つの[原色](../Page/原色.md "wikilink")を混ぜて幅広い色を再現する[加法混合](https://ja.wikipedia.org/wiki/加法混合 "wikilink")の一種である。RGBは三原色の頭文字である。[ブラウン管](../Page/ブラウン管.md "wikilink")（CRT）や[液晶ディスプレイ](https://ja.wikipedia.org/wiki/液晶ディスプレイ "wikilink")（LCD）、[パソコン](https://ja.wikipedia.org/wiki/パソコン "wikilink")、[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")などで画像再現に使われている。

同様の表色系に「**[RGBA](https://ja.wikipedia.org/wiki/色空間#RGBA "wikilink")**」というものもある。これは赤 (**R**ed)、緑 (**G**reen)、青 (**B**lue)、[アルファチャンネル](../Page/アルファチャンネル.md "wikilink") (**A**lpha) の略である。RGBAはカラーモデルとしてはRGBと異なるものではないが、異なる表現法である。アルファチャンネルは透過（透明度）を表現するもので、画像合成などに使われる補助的なデータである。

RGBカラーモデル自体は、「赤」・「緑」・「青」とは測色学（[colorimetry](https://ja.wikipedia.org/wiki/:en:colorimetry "wikilink")、比色法）的にどのような色を意味するかを定義していない。赤・緑・青の三原色を測色学的に厳密に定量化した場合、sRGBやAdobeRGBなどさまざまな[色空間](../Page/色空間.md "wikilink")（RGB色空間）が定義される。ここでは、RGBカラーモデルを使う異なるRGB色空間に共通した概念や、かつて[電子工学](../Page/電子工学.md "wikilink")分野で使用されていたカラーモデルについて説明する。

## 加法混合における原色

[CIExy1931_sRGB.png](https://ja.wikipedia.org/wiki/File:CIExy1931_sRGB.png "fig:CIExy1931_sRGB.png")カラートライアングル。三角形の頂点がSRGBで定義される赤・緑・青の三原色に当たり、中央に白色点 (white point) がある（ここでは「[D65](https://ja.wikipedia.org/wiki/D65光源 "wikilink")」という白色が使用されている）。パソコンのディスプレイで正確に表示されるのはこの三角形の範囲内のみで、三角形の外は実際には再現されていない\]\] どのような色を「[原色](../Page/原色.md "wikilink")」として選択するかは、人間の[目](../Page/目.md "wikilink")の[生理学](../Page/生理学.md "wikilink")的特徴と関係する。より適切に選ばれた光の[波長](../Page/波長.md "wikilink")をもつ三原色は、[網膜](../Page/網膜.md "wikilink")にある三種類の[錐体細胞](../Page/錐体細胞.md "wikilink")（すいたいさいぼう）それぞれに色刺激として働きかけ、それぞれの種類の錐体細胞からの反応の差を最大化させ、より大きな[色域](https://ja.wikipedia.org/wiki/色域 "wikilink")を表現することができる。

もっとも淡い白色からもっとも鮮やかな[スペクトル](../Page/スペクトル.md "wikilink")色までを示す「色度図」内において、三原色として選ばれた色を頂点にした三角形をカラートライアングル\[1\]といい、三原色が表現できる色域の広さと関係する。

[可視光線](../Page/可視光線.md "wikilink")にはさまざまな波長の光がさまざまな割合で合成されているが、人間の錐体細胞はそれぞれある特定の波長の範囲に最大限反応するようになっている。ひとつは長波長（L、[黄色](../Page/黄色.md "wikilink")付近）、ひとつは中波長（M、緑色付近）、もうひとつは短波長（S、[紫](../Page/紫.md "wikilink")色付近）である。これら三種類の錐体細胞からの刺激を大脳が組み合わせて、光の色が認識される。たとえば[オレンジ色](https://ja.wikipedia.org/wiki/オレンジ色 "wikilink")の光（波長577ナノメートルから597ナノメートル）が目に入り網膜を刺激すると、長波長に反応する錐体細胞と中波長に反応する錐体細胞が興奮するが、短波長に反応する錐体細胞はほとんど興奮しない。これら三種類の錐体細胞の反応の差を大脳が分析し「オレンジ色」と結び付けられる。

三原色を測色学的に定義してできるカラートライアングル内の色のみが加法混合で再現される。カラートライアングルをいかに大きくするか、いかに必要な色の範囲をカバーするか、再現に使われる物質にかかるコストなどから、様々な組み合わせの三原色が構成されてきた。

## RGBとディスプレイ

[Barn_grand_tetons_rgb_separation.jpg](https://ja.wikipedia.org/wiki/File:Barn_grand_tetons_rgb_separation.jpg "fig:Barn_grand_tetons_rgb_separation.jpg") [RGB_pixels.jpg](https://ja.wikipedia.org/wiki/File:RGB_pixels.jpg "fig:RGB_pixels.jpg") RGBカラーモデルを使用している一般的な例は、[ブラウン管](../Page/ブラウン管.md "wikilink")・[液晶ディスプレイ](https://ja.wikipedia.org/wiki/液晶ディスプレイ "wikilink")・[プラズマディスプレイ](../Page/プラズマディスプレイ.md "wikilink")など、[コンピュータ](../Page/コンピュータ.md "wikilink")や[テレビ](../Page/テレビ.md "wikilink")の[映像](https://ja.wikipedia.org/wiki/映像 "wikilink")表示に使われる[ディスプレイであろう](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")。画面を構成する各[ピクセル](../Page/ピクセル.md "wikilink")は、コンピュータや[グラフィクスカードなどによって赤色](../Page/ビデオカード.md "wikilink")・緑色・青色の[明度](https://ja.wikipedia.org/wiki/明度 "wikilink") ([Value](https://ja.wikipedia.org/wiki/:en:Lightness_\(color\) "wikilink")) として表現される。これらの数値は[ガンマ補正](https://ja.wikipedia.org/wiki/ガンマ補正 "wikilink")によって、表現したい輝度でディスプレイ上に表示されるような[輝度](https://ja.wikipedia.org/wiki/輝度 "wikilink") (intensity) や[電圧](../Page/電圧.md "wikilink")に転換されている。

適切な赤・緑・青の輝度の組み合わせで様々な色が表現される。2017年現在で典型的なディスプレイは一つのピクセルに[24ビット](https://ja.wikipedia.org/wiki/24ビット "wikilink")までの情報を使用している。これは[8ビット](../Page/8ビット.md "wikilink")分を赤・緑・青にそれぞれ割り当てることで各[色相](https://ja.wikipedia.org/wiki/色相 "wikilink") ([hue](https://ja.wikipedia.org/wiki/:en:Hue "wikilink")) ごとに256通りの明度や輝度を与えることができる。このシステムにより、16,777,216通り（256<sup>3</sup>もしくは2<sup>24</sup>）の色相 (hue) ・[彩度](https://ja.wikipedia.org/wiki/彩度 "wikilink") ([saturation](https://ja.wikipedia.org/wiki/:en:Colorfulness "wikilink")) ・明度 (value) が特定できる。

### ビデオエレクトロニクス

RGBはビデオ技術で用いられる[コンポーネント映像信号](../Page/コンポーネント映像信号.md "wikilink")に使われる。ここでは、3つのケーブルと端子にそれぞれ赤・緑・青の信号が割り当てられている。また同期信号のためにもう一本ケーブルを使う時もある。ビデオ信号のタイミングには、もともとモノクロームビデオ信号のために使われた規格であるRS-170 やRS-343を修正したものが使われている。RGBビデオ信号は、[SCART端子](../Page/SCART端子.md "wikilink")には最適の規格であるため[ヨーロッパ](../Page/ヨーロッパ.md "wikilink")ではビデオほかテレビ周辺機器に広く使われているが、それ以外の地域では[S端子](../Page/S端子.md "wikilink")が使われRGBビデオ信号は一般にはあまり使われない規格である。しかし、コンピュータのモニターには全世界的にRGB信号が用いられる。

### 非直線性

ガンマ補正により、コンピュータ機器による色出力の際の輝度は、ふつう[イメージファイルのR](../Page/ファイルフォーマット.md "wikilink")・G・Bの明度の比率とは異なる。明度0.5は、輝度0（最小）から輝度1.0（最大）の半分に非常に近いが、(0.5, 0.5, 0.5) を表示する際のディスプレイ上の輝度はふつう（標準的な 2.2-gamma のブラウン管・液晶ディスプレイで）、(1.0, 1.0, 1.0) を表示する際の50%の輝度ではなく、わずか22%ほどの輝度である\[2\]。

### プロの使用する環境下

高度な専門家などが映像・画像を制作・編集・出力する環境下では、色の適切な再生には、制作・編集の過程で使用される全機器において正確に色を合わせるための[カラーキャリブレーション](../Page/カラーマネージメントシステム.md "wikilink")（color calibration、色補正、色較正）を必要とする。この結果、制作・編集過程において色の一貫性を保証するため、機器依存の色空間の間での透過の変換などが行われる。しかし制作過程でデジタルイメージが様々な機器を経由しそのたびに変換されることで、イメージの色域が削減されるなどの劣化が起こる。このため、オリジナルのデジタル化画像の色域が広いほど、視覚的な劣化なく処理する方式が求められる。プロの機器やソフトウェアは色域の濃度を高めるため、48bpp（ピクセル当たり48[ビット](../Page/ビット.md "wikilink")、RGBの各チャンネル当たり16ビット）の精細な画像を扱えるようになっている。

## 数値表示

[RGBCube_b.svg](https://ja.wikipedia.org/wiki/File:RGBCube_b.svg "fig:RGBCube_b.svg")  RGBカラーモデルにおける色は、赤・緑・青の各要素がどれだけ含まれているかで記述することができる。各要素は輝度最小（闇）から輝度最大までの範囲を持つ。もし各要素とも最小なら、表示結果は黒になる。もし各要素とも最大なら、表示結果は白になる。

これらの色はいくつかの方法で数量化できる。

  - 色彩の研究者は、分析する個々の色を赤・緑・青に分解しそれぞれの要素の明度を0（最小）から1（最大）の間に置く。つまり、1ビットである。多くの色は、これらの明度からなる数式で表現できる。たとえば輝度最大の赤色は、この表示方法を使えば、 1，0，0（赤・緑・青の順）となる。
  - 色の明度はパーセンテージでも表現できる。最小は0%、最大は100%となる。輝度最大の赤は、100%，0%，0%となる。
  - 色の明度は0から255までの256個の数字でも表現できる。最少は0、最大は255となる。これは各要素の明度を8ビット（1[バイト](../Page/バイト_\(情報\).md "wikilink")）以内に収めたうえで[十進数](https://ja.wikipedia.org/wiki/十進数 "wikilink")で表したもので、コンピュータにおける色の表示によく使われている。このモデルを使えば輝度最大の赤は255，0，0となる\[3\]。この明度の幅は他と比例していないが、非直線性のガンマ補正スケールには比例する。
  - 0から255までの数字は[16進法でも表される](../Page/十六進法.md "wikilink")。16進法は、赤・緑・青の順に「0・1・2・3・4・5・6・7・8・9・A・B・C・D・E・F」の16文字の英数字が使われ、最初に\#を付け、16進数2桁ずつで色を表現している。1バイトの情報は十六進数で二桁で表示できる。最少は0、最大はFFとなる。輝度最大の赤はFF, 00, 00となる。またHTMLでは\#FF0000と短縮される。

24bpp（ピクセル当たり24ビット）でエンコードされたRGB明度は、赤・緑・青の輝度を示す三つの8ビット符号無し整数（8-bit unsigned integers、0から255まで）で表せる。たとえば次の画像はRGB立方体の三面を開いたものであるが、その上の色は次のように表される。

<table>
<tbody>
<tr class="odd">
<td><ul>
<li>(0, 0, 0) は<a href="https://ja.wikipedia.org/wiki/黒" title="wikilink">黒</a></li>
<li>(255, 255, 255) は<a href="../Page/白.md" title="wikilink">白</a></li>
<li>(255, 0, 0) は<a href="../Page/赤.md" title="wikilink">赤</a></li>
<li>(0, 255, 0) は<a href="../Page/緑.md" title="wikilink">緑</a></li>
<li>(0, 0, 255) は<a href="../Page/青.md" title="wikilink">青</a></li>
<li>(255, 255, 0) は<a href="../Page/黄色.md" title="wikilink">黄色</a></li>
<li>(0, 255, 255) は<a href="../Page/シアン_(色).md" title="wikilink">シアン</a></li>
<li>(255, 0, 255) は<a href="../Page/マゼンタ.md" title="wikilink">マゼンタ</a></li>
</ul></td>
<td><p>yellow(<span style="color:#FFFF00">●</span>)<br />
(255,255,0)</p></td>
<td style="text-align: center;"><p>green(<span style="color:#00FF00">●</span>)<br />
(0,255,0)</p></td>
<td><p>cyan(<span style="color:#00FFFF">●</span>)<br />
(0,255,255)</p></td>
</tr>
<tr class="even">
<td><p>red(<span style="color:#FF0000">●</span>)<br />
(255,0,0)</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/File:RGBR.png" title="fig:RGBR.png">RGBR.png</a></p></td>
<td style="text-align: center;"><p>blue(<span style="color:#0000FF">●</span>)<br />
(0,0,255)</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>red(<span style="color:#FF0000">●</span>)<br />
(255,0,0)</p></td>
<td style="text-align: center;"><p>magenta(<span style="color:#FF00FF">●</span>)<br />
(255,0,255)</p></td>
<td></td>
</tr>
</tbody>
</table>

これは「full-range RGB」という変換方法を用いている。full-range RGB は各原色ごとに8ビットを用いるため、各原色の明度を白から黒まで256通りに表示できる。ただしガンマ補正のため、256段階の数字は等間隔の輝度にはならない。また[デジタルビデオ](../Page/デジタルビデオ.md "wikilink")のRGBはフルレンジではない。その代りビデオRGBはITU-R BT.601（放送局用）などのエンコード規格を用いている。

この24ビットカラー (24-bit color)、および32ビットカラー (32-bit color) は「トゥルーカラー」(Truecolor) と呼ばれる。その他、256色までしか表示できない8ビットカラー (8-bit color)、16ビットのハイカラー (16-bit color : Highcolor)、Adobe Photoshopなどで使われる48ビットカラー (48-bit color) などがある。

### メモリ領域

圧縮されていない画像に使われる[メモリの領域は](../Page/記憶装置.md "wikilink")、画像のピクセル数および各ピクセルの色深度によって決定される。24ビットカラーの画像では、24ビット×ピクセル数の数値が、その画像の情報量となる。これをバイトに換算するには、8で割る必要がある（8ビット=1バイト）。

640ピクセル×480ピクセルのサイズの画像の情報量:

24 × 640 × 480 = 7,372,800 ビット

7,372,800 / 8 = 921,600 バイト（921.6 キロバイト）

### 15ビットカラー・16ビットカラー

24ビットカラーのほか、1ピクセルあたり16ビットの輝度の情報を割り当てる**15ビットカラー**や**16ビットカラー**（Highcolor、ハイカラー）もあり、一般的な色彩の表現のためには十分な色数を表示できる。この場合、赤・緑・青の各色当たり5ビットずつが使われる（555 mode、555モード）。合計15ビットのほか、緑は人間の目がもっとも反応しやすい色であるため、緑にもう1ビット分の輝度の情報を加え合計16ビットとする（565 mode、565モード）こともある。

### 32ビットカラー

1ピクセルあたり32ビットの情報を使う**32ビットカラー**は、表示の正確さにおいてはほとんど常に24ビットカラーと同じである。24ビットモードに比べ、1ピクセル当たりあと8ビットの情報を使うことができるが、これはほとんどの場合使用されない。32ビットモードが存在する理由は、現代のハードウェアは2の乗数のバイト数に整列されたデータには、整列されていないデータよりも速いスピードでアクセスできるためである（32=2<sup>5</sup>）。

### 48ビットカラー

**48ビットカラー**（48ビットモード）は1ピクセルの三原色それぞれに16ビットの情報量を当てるもので（それゆえ、16ビットモードと呼ばれることもある）、1ピクセル当たり48ビットの情報がある。このモードでは三原色のそれぞれに対し輝度は65,536段階で表現できる。48ビットカラーは、[Adobe Photoshopなどプロ向けのソフトウェアで使われており](../Page/Adobe_Photoshop.md "wikilink")、画像処理を繰り返した場合の画像の誤差蓄積による劣化を防ぐことができる。

## 脚注

### 注釈

### 出典

## 参考文献

  -
## 関連項目

  - [原色](../Page/原色.md "wikilink")（[減法混合](https://ja.wikipedia.org/wiki/原色#減法混合 "wikilink")）
  - [色空間](../Page/色空間.md "wikilink")（[表色系](https://ja.wikipedia.org/wiki/色空間#表色系 "wikilink")、[RGBA色空間](https://ja.wikipedia.org/wiki/色空間#一般的な色空間 "wikilink")、[CMY](https://ja.wikipedia.org/wiki/色空間#一般的な色空間 "wikilink")）
  - [CMYK](../Page/CMYK.md "wikilink")
  - [RGBY](https://ja.wikipedia.org/wiki/RGBY "wikilink")
  - [RGB21ピン](../Page/RGB21ピン.md "wikilink")
  - [Roy G. Biv](https://ja.wikipedia.org/wiki/w:en:Roy_G._Biv "wikilink")

## 外部リンク

  - [画像処理ポータル 画像機器総覧](http://www.j-imaging.com/)画像機器総覧は画像処理に関連する製品、技術情報を紹介しているポータルサイト
  - [Demonstrative color conversion applet](http://www.cs.rit.edu/~ncs/color/a_spaces.html)

[Category:光](https://ja.wikipedia.org/wiki/Category:光 "wikilink") [Category:光学](https://ja.wikipedia.org/wiki/Category:光学 "wikilink") [Category:色](https://ja.wikipedia.org/wiki/Category:色 "wikilink") [Category:色空間](https://ja.wikipedia.org/wiki/Category:色空間 "wikilink") [Category:画像処理](https://ja.wikipedia.org/wiki/Category:画像処理 "wikilink")

1.
2.
3.  なお、半分の輝度を表す場合は127（または128）,0,0となる