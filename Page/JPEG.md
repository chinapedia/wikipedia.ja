> この記事は[JPEG](https://ja.wikipedia.org/wiki/JPEG)から翻訳されています。


**JPEG**（ジェイペグ、Joint Photographic Experts Group）は、[コンピュータ](../Page/コンピュータ.md "wikilink")などで扱われる[静止画像の](../Page/画像.md "wikilink")[デジタル](../Page/デジタル.md "wikilink")[データ](../Page/データ.md "wikilink")を[圧縮する方式のひとつ](../Page/データ圧縮.md "wikilink")。またはそれをつくった組織 ([ISO/IEC JTC 1](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink")/SC 29/WG 1, [Joint Photographic Experts Group](../Page/Joint_Photographic_Experts_Group.md "wikilink")) の略称であり、[アクロニム](https://ja.wikipedia.org/wiki/アクロニム "wikilink")である。JPEG方式による画像ファイルにつけられる[拡張子](../Page/拡張子.md "wikilink")は*jpg*が多く使われるほか、*jpeg*等が使われる場合もある。

一般的に[非可逆圧縮](../Page/非可逆圧縮.md "wikilink")の画像フォーマットとして知られている。[可逆圧縮](../Page/可逆圧縮.md "wikilink")形式もサポートしているが、可逆圧縮は[特許](../Page/特許.md "wikilink")などの関係でほとんど利用されていない。1992年9月18日に最初のリリースが行われた比較的古いフォーマットであり、欠点を克服すべく数々の後継規格が提案されてきたが、企業間の思惑なども絡み、いずれも主流になるには至らず、JPEGが現在も静止画像規格の主流である。

標準では、特定の種類の画像の正式なフォーマットがなく、JFIF形式（[マジックナンバー上は](https://ja.wikipedia.org/wiki/マジックナンバー_\(フォーマット識別子\) "wikilink")、6バイト目から始まる形式部分にJFIFと記されているもの）が事実上の標準[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")となっている。[動画](../Page/動画.md "wikilink")を記録可能にしたものに[Motion JPEGがある](../Page/Motion_JPEG.md "wikilink")。立体視 (3D) 用には、ステレオJPEG (JPS) フォーマット\[1\]がある。

[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")の記録方式としてもよく利用されているが、デジタルカメラでは様々なオプション機能を使い、JFIFを拡張した[Exchangeable image file format](../Page/Exchangeable_image_file_format.md "wikilink") (**EXIF**) などのフォーマットとしてまとめられている。

## 技術の詳細

ここでは、一般に用いられる非可逆圧縮の方式について説明する。なお、JPEGの可逆圧縮には非可逆圧縮とは全く別の技術が用いられている。[JPEG 2000ではどちらにも同じ技術を用いる](../Page/JPEG_2000.md "wikilink")。

### 符号化方式

JPEGでは、画像を固定サイズ（8×8画素）のブロックに分割し、そのブロック単位で、[離散コサイン変換](../Page/離散コサイン変換.md "wikilink") (DCT: discrete cosine transform) を用いて、空間領域から[周波数領域](../Page/周波数領域.md "wikilink")へ変換する。この変換自体では情報量は削減されない。変換されたデータは、[量子化](https://ja.wikipedia.org/wiki/量子化 "wikilink")ビット数の低減によって情報量を落としてから、[ハフマン符号](../Page/ハフマン符号.md "wikilink")による[エントロピー符号化](https://ja.wikipedia.org/wiki/エントロピー符号化 "wikilink")がなされ圧縮が行われる。エントロピー符号化とは、データの生起確率の高低に応じて異なる長さの符号を割り当てることで圧縮を行うものである。

DCTによる周波数領域への変換では、変換そのものでは情報量は削減されないが、低周波数成分にエネルギーが集まることを利用して、量子化ビット数の低減による情報量削減と、エントロピー符号化での圧縮率向上を図っている。普通の画像をそのまま量子化ビット数を低減してしまうと大きな画質劣化が生じるが、重要な成分が局所的に集められた後では元の画像の性質を残したまま量子化が可能である。また、低周波数成分に集中するという形で、データに偏りが生じると、エントロピー符号化の圧縮率も向上する。なお、JPEGでは、量子化マトリックスと呼ばれる係数表を用いて、低周波数成分に比べて高周波数成分でより粗い量子化を行うのが一般的である。

エントロピー符号化ではハフマン符号を用いる。ハフマン符号は処理が単純であるため演算量が少なく、さらにその符号セットが想定する、理想的なデータが入力された場合には極めて高い圧縮率を実現する。符号セットにあわないデータが入力された場合、逆に圧縮率は下がってしまう。この問題を解消するため後継のJPEG 2000では[算術符号](../Page/算術符号.md "wikilink")が採用された。

なお、周波数領域への変換前の画像フォーマットの色成分の数は1～4の間で選択でき、各色成分が何であるかを決める[表色系](https://ja.wikipedia.org/wiki/表色系 "wikilink")も自由に選択することができる。そのため色成分が1つのグレースケール、色成分が3つの[RGB](../Page/RGB.md "wikilink")及び[YCbCr](https://ja.wikipedia.org/wiki/YCbCr "wikilink")、色成分が4つの[YMCKなどのデータのどれも用いることができる](../Page/CMYK.md "wikilink")。しかし、表色系の規定がない上にどの表色系であるかを示す情報もないことは互換性に大きな問題となる。そのためJFIF形式では、YCbCr表色系を用いること、さらに成分の順序はY、Cb、Crの順であることを規定している。各色成分の空間的な間引きをあらわすサンプリングファクタについては、各々の色成分について水平方向、垂直方向独立に定めることができ、一般的な形式の4:4:4、4:2:2、4:2:0、4:1:1のいずれもが選択可能である。

### ノイズ

JPEGではブロック単位で変換を行うため、圧縮率を上げるとブロックの境界に[ブロックノイズ](../Page/ブロックノイズ.md "wikilink")と呼ばれるノイズが生じる。

また、周波数領域への変換においては、低周波成分に画像のエネルギーが集中するため、高周波成分のエネルギーは小さくなる。このため量子化を行うと高周波成分はゼロに落ち、無くなってしまう。すると画像の急峻な変化を十分に表現できないため、エッジ周辺では、ある一点に集まる蚊にたとえ[モスキートノイズ](https://ja.wikipedia.org/wiki/モスキートノイズ "wikilink")と呼ばれるノイズが生じる。

色差を間引く為、特に[赤](../Page/赤.md "wikilink")には弱く、赤の部分でノイズが発生しやすい。

## 規格書

規格は、合同のグループで作られたため[国際標準化機構](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink") (ISO)、[国際電気標準会議](../Page/国際電気標準会議.md "wikilink") (IEC) と[国際電気通信連合](../Page/国際電気通信連合.md "wikilink") (ITU) の双方から出されている。それにならい、[日本産業規格](../Page/日本産業規格.md "wikilink") (JIS) でも規格化されている。

  - [ITU-T](../Page/ITU-T.md "wikilink")勧告 T.81

  - ISO/IEC 10918-1:1994

  -
## インターネットでの普及とその背景

JPEGは、[Webの普及黎明期において](../Page/World_Wide_Web.md "wikilink")、[Webブラウザ標準の画像フォーマットとして](../Page/ウェブブラウザ.md "wikilink")、[GIFと双璧を成していた](../Page/Graphics_Interchange_Format.md "wikilink")。

JPEGの符号化方式の特性から、同じ色が広い範囲に広がることの多い[絵画](../Page/絵画.md "wikilink")であっても、画像そのもののサイズに比例してファイルサイズが大きくなる。このため、[ダイヤルアップ接続](../Page/ダイヤルアップ接続.md "wikilink")等、一般ユーザーの末端接続が[ナローバンド](../Page/ナローバンド.md "wikilink")だった時代には、データ転送量を少なくするという観点から、絵画はGIF、[デジタルスチル写真にはJPEG](../Page/デジタルカメラ.md "wikilink")、という使い分けが存在していた。

[1999年](../Page/1999年.md "wikilink")、GIFの特許問題によって起こったGIF排斥運動（[当該項目を参照](https://ja.wikipedia.org/wiki/Graphics_Interchange_Format#特許問題とその顛末 "wikilink")）で、GIFから、JPEGや、新たにフリーのフォーマットとして開発された[PNGに移行する流れになった](../Page/Portable_Network_Graphics.md "wikilink")。PNGは当時のブラウザでは[プラグイン](../Page/プラグイン.md "wikilink")を導入しないと表示できないなどの問題を抱えているケースが多かったため、GIF画像をJPEGによって置き換えられるケースが多かった。

現在は、GIFの[LZWの特許が失効し](../Page/Lempel–Ziv–Welch.md "wikilink")、フリーな画像フォーマットとして再び使えるようになり、PNGもほぼ全てのブラウザでサポートされるようになった。この2つの画像フォーマットは現在もインターネット上でよく使われている。

## 実装

Independent JPEG Group によるフリーのライブラリ [libjpeg](https://ja.wikipedia.org/wiki/libjpeg "wikilink") は jpeg [コーデック](../Page/コーデック.md "wikilink")の実装として大変重要である。これは1991年に初版がリリースされ、jpegが標準技術として採用され成功を収める鍵となった\[2\] 。 libjpeg やその派生版は数えきれないほどのソフトウェアから利用されている。

2017年3月には Google が Guetzli というオープンソースの jpeg エンコーダを発表した。 これは同じく Google が発表した画質評価アルゴリズム Butteraugli に特化したエンコーダであり、既存のエンコーダと比較してエンコードに莫大な時間を費やす代わりに、Butteraugli の評価値と圧縮率においてバランスの取れた画像を出力する。Google は既存の方式と比較して Guetzli は高品質なjpeg画像のファイルサイズを35%削減できると主張している\[3\]。

## 出典

<references />

## 関連項目

  - 派生規格
      - [CPKTフォーマット](../Page/CPKTフォーマット.md "wikilink")
      - [JPEG-HDR](https://ja.wikipedia.org/wiki/JPEG-HDR "wikilink")
      - [Lossless JPEG](https://ja.wikipedia.org/wiki/Lossless_JPEG "wikilink")
  - ポストJPEG規格
      - [JPEG 2000](../Page/JPEG_2000.md "wikilink")
      - [JPEG XR](https://ja.wikipedia.org/wiki/JPEG_XR "wikilink") ([HD Photo](../Page/HD_Photo.md "wikilink"))
      - [WebP](https://ja.wikipedia.org/wiki/WebP "wikilink")
  - [データ圧縮](../Page/データ圧縮.md "wikilink")
  - [JBIG](https://ja.wikipedia.org/wiki/JBIG "wikilink")
  - [安田浩](../Page/安田浩.md "wikilink")
  - [プログレッシブJPEG](https://ja.wikipedia.org/wiki/インターレース#静止画のインターレース "wikilink")
  - [Portable Network Graphics](../Page/Portable_Network_Graphics.md "wikilink") (PNG)
  - [Graphics Interchange Format](../Page/Graphics_Interchange_Format.md "wikilink") (GIF)
  - [libjpeg](https://ja.wikipedia.org/wiki/libjpeg "wikilink")

## 外部リンク

  - [JPEG公式サイト](http://www.jpeg.org/jpeg/)（英語。）
  - [W3C Overview of JPEG](http://www.w3.org/Graphics/JPEG/)（英語。JPEGおよびJFIFの仕様書あり）

[Category:データ圧縮規格](https://ja.wikipedia.org/wiki/Category:データ圧縮規格 "wikilink") [Category:ラスターグラフィックス・ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ラスターグラフィックス・ファイルフォーマット "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink") [Category:ISO/IEC標準](https://ja.wikipedia.org/wiki/Category:ISO/IEC標準 "wikilink") [Category:ITU-T勧告](https://ja.wikipedia.org/wiki/Category:ITU-T勧告 "wikilink") [Category:アクロニム](https://ja.wikipedia.org/wiki/Category:アクロニム "wikilink") [Category:非可逆圧縮アルゴリズム](https://ja.wikipedia.org/wiki/Category:非可逆圧縮アルゴリズム "wikilink")

1.  <http://www.nvidia.co.jp/object/3d-vision-3d-pictures-jp-old.html>
2.  [Jpeg.org](http://jpeg.org/jpeg)
3.  [Announcing Guetzli: A New Open Source JPEG Encoder - Google Research Blog](https://research.googleblog.com/2017/03/announcing-guetzli-new-open-source-jpeg.html)