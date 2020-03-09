> この記事は[YUV](https://ja.wikipedia.org/wiki/YUV)から翻訳されています。


[YUV_UV_plane.svg](https://ja.wikipedia.org/wiki/File:YUV_UV_plane.svg "fig:YUV_UV_plane.svg") [Barn-yuv.png](https://ja.wikipedia.org/wiki/File:Barn-yuv.png "fig:Barn-yuv.png")

**YUV**や**YCbCr**や**YPbPr**とは、輝度信号Yと、2つの色差信号を使って表現される[色空間](../Page/色空間.md "wikilink")。

## 概要

ソニーの[ベータカム](https://ja.wikipedia.org/wiki/ベータカム "wikilink")VTRで使用されて以来、高画質アナログ映像信号の伝送や、デジタルビデオの記録方式として使用されている。

U, Cb, Pb はB信号(青)から輝度Yを差し引いた (B - Y) に特定の定数を掛けた値であり、同じくV, Cr, Pr はR信号(赤)から輝度Yを差し引いた (R - Y) に特定の定数を掛けた値である。

## YUVおよびYCbCrの表記

YCbCrをYUVと表記される例を見かけるが、YUVは[PAL](https://ja.wikipedia.org/wiki/PAL "wikilink")信号や[SECAM](https://ja.wikipedia.org/wiki/SECAM "wikilink")信号を得るための[コンポーネント信号であり](https://ja.wikipedia.org/wiki/コンポーネント映像信号 "wikilink")、YCbCr や YPbPr とは似ていながらも異なるため、DVDやHD映像の記録に使われるデータ表記として、YUVを用いるのは誤りである。ただし、U, Vの値域を\[-0.5, 0.5\]に変換するとCb, Crになる。

現在では YUV を色空間モデルの総称とし、RGB との色空間変換におけるカラーマトリックスの違いやサンプリング仕様を定義した信号の呼称として YCbCr および YPbPr を使用するのが主流となっている。

## YCbCrとYPbPrの使い分け

YCbCr と YPbPr の使い分けについて、

1.  アナログ信号にCb, Crを用い、デジタル化された数値にはPb, Prを使う。
2.  アナログ、デジタルを問わず、[SD映像用の色差コンポーネント成分にはCb](https://ja.wikipedia.org/wiki/標準画質映像 "wikilink"), Crを、[HD映像用の色差コンポーネント成分にはPb](https://ja.wikipedia.org/wiki/高精細度テレビジョン放送 "wikilink"), Prを使う。

の2説があり、明確には統一されていない。 規格によっても用法が異なり、[ARIB](https://ja.wikipedia.org/wiki/ARIB "wikilink") (日本) ではPb, Prを、SMPTE (米国) ではアナログにPb, Prを、デジタルにCb, Crを使用している\[1\]。デジタル伝送の[HDMI](https://ja.wikipedia.org/wiki/HDMI "wikilink")ではCb, Crを使用している。 一般的なビデオ機器には後者が採用されているようである。GBR成分からのカラーマトリックスがSD用とHD用で異なることを考慮すると、後者の使い方が望ましいと考えられる。

## ケーブル

YCbCr信号の伝送には、業務用ビデオ機器のアナログ伝送の場合は、[BNC](https://ja.wikipedia.org/wiki/BNC "wikilink")端子（ケーブル）で接続された3本の信号線を用いる。デジタル伝送ではBNC端子で接続される1本のケーブルを用いる[SDIか](https://ja.wikipedia.org/wiki/シリアルデジタルインタフェース "wikilink")、パラレルインターフェースを用いる。 家庭用ビデオ機器では、アナログ信号の場合、[RCA端子](https://ja.wikipedia.org/wiki/RCA端子 "wikilink")（ケーブル）で接続された3本の信号線である[コンポーネント端子](https://ja.wikipedia.org/wiki/コンポーネント端子 "wikilink")を用いるか、ケーブルをまとめた[D端子](../Page/D端子.md "wikilink")ケーブルを用いる。デジタル伝送では、[IEEE 1394や](../Page/IEEE_1394.md "wikilink")[HDMI](https://ja.wikipedia.org/wiki/HDMI "wikilink")を用いる。 なお、[コンポジット端子](https://ja.wikipedia.org/wiki/コンポジット端子 "wikilink")や[S端子](../Page/S端子.md "wikilink")から伝送される[NTSC](https://ja.wikipedia.org/wiki/NTSC "wikilink")信号（[コンポジット映像信号](../Page/コンポジット映像信号.md "wikilink")）は、輝度, 色相, 彩度の成分を持っており、[色差コンポーネント信号とは根本的に異なる](https://ja.wikipedia.org/wiki/コンポーネント映像信号 "wikilink")。

## 色差成分を間引く方法

YCbCrで帯域を減らす際に、色差成分を間引く方法も併せて使用される。人間の目は色の変化よりも明るさの変化に敏感なので、色差成分を減らしても不自然だと感じにくいためである。ビデオフォーマットとして採用されているものには、以下の種類がある。

  - 4：4：4
    Y, Cb(Pb), Cr(Pr)の各成分を水平画素に関して各成分4:4:4の割合で記録する。つまり以下で説明する4:2:2や4:1:1等と違い、信号を間引かず全て記録するので最も高画質のフォーマットである。
  - 4：2：2
    一般的な業務用ビデオに採用されている方式で、Y, Cb(Pb), Cr(Pr)の各成分を、水平に4:2:2の画素割合で記録する。すなわち、水平に並んだ画素に1,2,3,4,5,6,7,…の番号を振った場合、Y信号は1,2,3,4,5,6,7,…の各画素について情報を記録するが、Cb(Pb)とCr(Pr)については1,3,5,7,…の画素のみの情報を記録し、再生時には画素1の色差情報を画素1,2に適用し、画素3の色差情報を画素3,4に適用し……という具合に補完する。ソニーのデジタルベータカム、ベータカムSX、HDCAM、HDCAM-SR（YPbPr記録）、PanasonicのD-5、DVCPRO50、HD-D5（YPbPr記録）、AVC-Intra（100Mbps記録）で採用されている。
  - 4：1：1
    525/60圏で使用する家庭用DVフォーマットと業務用DVCAM、DVCPRO（25Mbps記録）フォーマットに採用されている方式で、Y, Cb(Pb), Cr(Pr)の各成分を水平に4:1:1の画素割合（輝度4画素に対して色差1画素）で記録する。
  - 4：2：0
    [DVD](../Page/DVD.md "wikilink")を始めとする一般的な[MPEG圧縮フォーマット](../Page/Moving_Picture_Experts_Group.md "wikilink")（[デジタル放送](https://ja.wikipedia.org/wiki/デジタル放送 "wikilink")、[D-VHS](../Page/D-VHS.md "wikilink")、[BD](../Page/Blu-ray_Disc.md "wikilink")）や[HDV](https://ja.wikipedia.org/wiki/HDV "wikilink")、[AVCHD](https://ja.wikipedia.org/wiki/AVCHD "wikilink")などの家庭用カメラフォーマットで使用するほか、ソニーのXDCAM-HD、XDCAM-EX、AVC-Intra（50Mbps記録）、625/50圏のDV、DVCAMフォーマットなど、業務用のビデオフォーマットでも使用されている。4:2:2方式と同様に、色差信号を輝度信号の2画素ごとに記録する方式であるが、1フレーム目の奇数番目の走査線ではCb(Pb)信号のみを記録して、偶数番目の走査線ではCr(Pr)信号のみを記録、2フレーム目の奇数番目の走査線では逆にCr(Pr)信号のみを記録して、偶数番目の走査線ではCb(Pb)信号のみを記録し、以下のフレームではこれを繰り返すという具合に、Cb(Pb)とCr(Pr)信号を走査線ごとに間引いて記録する。再生時、記録されていない色差信号のデータは、1本上の走査線のデータで補完する。情報量は4:1:1方式と同じになるものの、色信号の水平解像度と垂直解像度のバランスがよく、家庭用デジタルビデオの主流方式となっている。

## 動画フォーマット

尚、同様の概念がPCやネットで使用する動画フォーマットにも見られる。

  - YUV444 (YUV)
    水平4[ピクセル](https://ja.wikipedia.org/wiki/ピクセル "wikilink")につき、輝度成分と２つの色差成分を各4ピクセルずつサンプルする方式。各成分を8bitで量子化すると、1ピクセルあたりの情報量は24bitとなる。
  - YUV12
    各ピクセルを表現するのに必要なビット数が12ビットのYUV。YUV420とYUV411の総称。
  - YUV422
    水平2ピクセルから色差信号を1ピクセル分だけとる形式。輝度信号は1ピクセルごとにとる。1ピクセルは16bitの情報量となる。主に業務用ビデオのフォーマットとして採用されている。
  - YUV420
    水平・垂直2×2ピクセルのうち、Cb信号を上2ピクセルから1ピクセル取り、Cr信号を下2ピクセルから1ピクセル取る方式。フレームごとにCbとCrの位置を反転させる。輝度信号は1ピクセルごとにとる。原理的に幅・高さは2の倍数でないといけない。[デジタル放送](https://ja.wikipedia.org/wiki/デジタル放送 "wikilink")ではこれが採用されている。
    YUV420のうち、ピクセル単位ではなく、フレーム単位でY→U→Vの順番に並べたものを**I420** や **IYUV**、Y→V→Uの順番に並べたものを**YV12**と呼ぶ。このどちらかが、動画圧縮ではよく使われている。
  - YUV411
    水平4ピクセルのうち、Cb,Cr信号を各色1ピクセルずつ取る形式。輝度信号は1ピクセルごとにとる。
  - YUV9
    4×4ピクセルで1つの色差信号しかとらない方式。輝度信号は1ピクセルごとにとる。1ピクセルは9ビット。

## RGBからの変換

以下、R, G, B, Yの値域は\[0, 1\]。Cb, Crの値域は\[-0.5, 0.5\]。U = 0.872 × Cb, V = 1.23 × Cr。

[RGB](../Page/RGB.md "wikilink")からの変換式は

  - YUV ([PAL](https://ja.wikipedia.org/wiki/PAL "wikilink"), [SECAM](https://ja.wikipedia.org/wiki/SECAM "wikilink"))
    <math>\\begin{pmatrix}

` Y\\`
` U\\`
` V`

\\end{pmatrix} = \\begin{pmatrix}

` 0.299 & 0.587 & 0.114\\`
` -0.14713 & -0.28886 & 0.436\\`
` 0.615 & -0.51499 & -0.10001`

\\end{pmatrix}\\begin{pmatrix}

` R\\`
` G\\`
` B`

\\end{pmatrix}</math>\[2\]

  - [ITU-R BT.601](https://ja.wikipedia.org/wiki/:en:Rec._601 "wikilink") / [ITU-R BT.709](https://ja.wikipedia.org/wiki/:en:Rec._709 "wikilink") (1250/50/2:1)
    <math>\\begin{pmatrix}

` Y\\`
` Cb\\`
` Cr`

\\end{pmatrix} = \\begin{pmatrix}

` 0.299 & 0.587 & 0.114\\`
` -0.168736 & -0.331264 & 0.5\\`
` 0.5 & -0.418688 & -0.081312`

\\end{pmatrix}\\begin{pmatrix}

` R\\`
` G\\`
` B`

\\end{pmatrix}</math>\[3\]

  - ITU-R BT.709 (1125/60/2:1)
    <math>\\begin{pmatrix}

` Y\\`
` Cb\\`
` Cr`

\\end{pmatrix} = \\begin{pmatrix}

` 0.2126 & 0.7152 & 0.0722\\`
` -0.114572 & -0.385428 & 0.5\\`
` 0.5 & -0.454153 & -0.045847`

\\end{pmatrix}\\begin{pmatrix}

` R\\`
` G\\`
` B`

\\end{pmatrix}</math>\[4\]

逆にRGBに変換するときは

  - YUV (PAL, SECAM)
    <math>\\begin{pmatrix}

` R\\`
` G\\`
` B`

\\end{pmatrix} = \\begin{pmatrix}

` 1 & 0 & 1.13983\\`
` 1 & -0.39465 & -0.58060\\`
` 1 & 2.03211 & 0`

\\end{pmatrix}\\begin{pmatrix}

` Y\\`
` U\\`
` V`

\\end{pmatrix}</math>\[5\]

  - ITU-R BT.601 / ITU-R BT.709 (1250/50/2:1)
    <math>\\begin{pmatrix}

` R\\`
` G\\`
` B`

\\end{pmatrix} = \\begin{pmatrix}

` 1 & 0 & 1.402\\`
` 1 & -0.344136 & -0.714136\\`
` 1 & 1.772 & 0`

\\end{pmatrix}\\begin{pmatrix}

` Y\\`
` Cb\\`
` Cr`

\\end{pmatrix}</math>\[6\]

  - ITU-R BT.709 (1125/60/2:1)
    <math>\\begin{pmatrix}

` R\\`
` G\\`
` B`

\\end{pmatrix} = \\begin{pmatrix}

` 1 & 0 & 1.5748\\`
` 1 & -0.187324 & -0.468124\\`
` 1 & 1.8556 & 0`

\\end{pmatrix}\\begin{pmatrix}

` Y\\`
` Cb\\`
` Cr`

\\end{pmatrix}</math>\[7\]

### MPEG の場合

[MPEG用の整数演算は以下の方法で行う](../Page/Moving_Picture_Experts_Group.md "wikilink")。RGBの値域は0〜255の8ビット。YCbCrに基づいているが、8ビット整数に変換する際、Yの値域として16〜235、UやVの値域としては16〜240を使用する。Yの値域の中心は128になっていない。また、値域として0〜255を使ってないことから証明できるように、RGB → YUV → RGBの変換を行うと、元の色に戻らない場合がある。

1\. 基本的な変形

\[\begin{bmatrix}Y' \\ U \\ V \end{bmatrix} =
\begin{bmatrix}
  66 & 129 & 25  \\
 -38 & -74 & 112 \\
 112 & -94 & -18
\end{bmatrix}
\begin{bmatrix} R \\ G \\ B \end{bmatrix}\]

2\. 8ビットへ丸め処理を行う（[四捨五入](https://ja.wikipedia.org/wiki/四捨五入 "wikilink")）

\[\begin{array}{rcl}
Y' &=& (Y' + 128) \gg 8\\
U  &=& (U  + 128) \gg 8\\
V  &=& (V  + 128) \gg 8
\end{array}\]

3\. 値域をずらす

\[\begin{array}{rcl}
Y' &=& Y' + 16\\
U  &=& U + 128\\
V  &=& V + 128
\end{array}\]

コンピュータではYUVとRGBの相互変換は、は整数演算で行われることが多かったが、は[SIMD](https://ja.wikipedia.org/wiki/SIMD "wikilink")を使い[内積](../Page/内積.md "wikilink")計算するのが一般的。

## 参照

<references />

## 外部リンク

  - [YUV pixel formats - fourcc.org](http://www.fourcc.org/yuv.php)
  - [libyuv](http://code.google.com/p/libyuv/)

[Category:色空間](https://ja.wikipedia.org/wiki/Category:色空間 "wikilink") [Category:心理学](https://ja.wikipedia.org/wiki/Category:心理学 "wikilink")

1.
2.  0.14713 ≒ 0.299 × 0.436 ÷ 0.886
    0.28886 ≒ 0.587 × 0.436 ÷ 0.886
    0.51499 ≒ 0.587 × 0.615 ÷ 0.701
    0.10001 ≒ 0.114 × 0.615 ÷ 0.701
3.  0.168736 ≒ 0.299 ÷ 1.772
    0.331264 ≒ 0.587 ÷ 1.772
    0.418688 ≒ 0.587 ÷ 1.402
    0.081312 ≒ 0.114 ÷ 1.402
4.  0.114572 ≒ 0.2126 ÷ 1.8556
    0.385428 ≒ 0.7152 ÷ 1.8556
    0.454153 ≒ 0.7152 ÷ 1.5748
    0.045847 ≒ 0.0722 ÷ 1.5748
5.  2.03211 ≒ 0.886 ÷ 0.436
    0.39465 ≒ 0.114 ÷ 0.587 × 2.03211
    1.13983 ≒ 0.701 ÷ 0.615
    0.58060 ≒ 0.299 ÷ 0.587 × 1.13983
6.  0.344136 ≒ 0.114 ÷ 0.587 × 1.772
    0.714136 ≒ 0.299 ÷ 0.587 × 1.402
7.  0.187324 ≒ 0.0722 ÷ 0.7152 × 1.8556
    0.468124 ≒ 0.2126 ÷ 0.7152 × 1.5748