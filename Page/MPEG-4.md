> この記事は[MPEG-4](https://ja.wikipedia.org/wiki/MPEG-4)から翻訳されています。


**MPEG-4**（エムペグフォー、ISO/IEC 14496）は、動画・音声全般を[デジタル](../Page/デジタル.md "wikilink")[データ](../Page/データ.md "wikilink")として扱うための規格のことである。[MPEG-1](../Page/MPEG-1.md "wikilink")や[MPEG-2](../Page/MPEG-2.md "wikilink")と同様、システム、ビジュアル(MPEG-1/-2ではビデオと呼ぶ)、オーディオ、ファイルフォーマットの各技術から構成される。しかしながら、一般的には「MPEG-4」と呼ぶ場合、動画の符号化方式を記述したビジュアル部分だけを指すことが多い。

規格が広範なことが「MPEG-4とは何か」という説明を難しくさせている上に、ビジュアル、あるいはファイルフォーマットの一部の規格を利用したものも単に「MPEG-4です」と説明されることが多く、使われ方、意味のとられ方が混乱している用語でもある。

なお、規格化を行っている[Moving Picture Experts GroupではMPEG](../Page/Moving_Picture_Experts_Group.md "wikilink")-4を最後の動画/音声符号化の規格とする意向であり、現在では3次元コンピュータグラフィクスや音声合成などを含む大変広範な規格になっている。MPEG技術は、各技術毎にパート（Part）と呼ばれる規格が作成され、技術が採用/規格化されるたびにパートが増える。[2003年](../Page/2003年.md "wikilink")に[H.264](../Page/H.264.md "wikilink")が**MPEG-4 Part 10 Advanced Video Coding**として規格化されるなど\[1\]、現在もなお追加・拡張が継続されている規格である。

## 規格の構成

MPEG-4(ISO/IEC 14496)自体は、動画・音声全般を扱う多様なマルチメディア符号化フォーマットを規定している。これらは以下に示す複数の「**部**（Part）」に分れて標準化されている。MPEG-4の各部は、ISO/IEC 14496を翻訳したJIS X 4332の各部と対応する。なお、第31部以降は現在開発中である。

動画には第2部(1999年制定)と第10部(2003年制定)があることに注意する。一般にMPEG-4動画(またはMPEG-4ビジュアル)といえば第2部を指すことが多く、第10部は第2部と区別するために、MPEG-4 AVC と呼ばれることがある。MPEG-4は動画の符号化規格と呼ばれることもあるが、実際に規定されているのは復号のみであり、符号化は規定していない。

| 部  | ISO/IEC規格番号                                                                         | 名称                                                                                                                                                                                      | 概要                                                                                                                                                                                                   |
| -- | ----------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1  | [ISO/IEC 14496-1](https://ja.wikipedia.org/wiki/ISO/IEC_14496-1 "wikilink")         | システム                                                                                                                                                                                    | 各メディアの同期・多重化などを規定。                                                                                                                                                                                   |
| 2  | [ISO/IEC 14496-2](https://ja.wikipedia.org/wiki/ISO/IEC_14496-2 "wikilink")         | 動画                                                                                                                                                                                      | 動画像の圧縮符号化技術。多数のプロファイルが規定されている。                                                                                                                                                                       |
| 3  | [ISO/IEC 14496-3](https://ja.wikipedia.org/wiki/ISO/IEC_14496-3 "wikilink")         | 音響                                                                                                                                                                                      | [AAC](../Page/AAC.md "wikilink") や[音響ロスレス圧縮](https://ja.wikipedia.org/wiki/音響ロスレス圧縮 "wikilink")を含む各種音声符号化技術を規定。                                                                                      |
| 4  | [ISO/IEC 14496-4](https://ja.wikipedia.org/wiki/ISO/IEC_14496-4 "wikilink")         | 適合性試験                                                                                                                                                                                   | MPEG-4の他の部の適合性試験の手続きを規定。                                                                                                                                                                             |
| 5  | [ISO/IEC 14496-5](https://ja.wikipedia.org/wiki/ISO/IEC_14496-5 "wikilink")         | 参照ソフトウェア                                                                                                                                                                                | MPEG-4の他の部を明確化するソフトウェアを規定。                                                                                                                                                                           |
| 6  | [ISO/IEC 14496-6](https://ja.wikipedia.org/wiki/ISO/IEC_14496-6 "wikilink")         | [Delivery Multimedia Integration Framework](https://ja.wikipedia.org/wiki/Delivery_Multimedia_Integration_Framework "wikilink") ([DMIF](https://ja.wikipedia.org/wiki/DMIF "wikilink")) |                                                                                                                                                                                                      |
| 7  | [ISO/IEC TR 14496-7](https://ja.wikipedia.org/wiki/ISO/IEC_TR_14496-7 "wikilink")   | 最適化ソフトウェア                                                                                                                                                                               | 処理の高速化やエラー耐性などの応用に関する検証に用いられる。                                                                                                                                                                       |
| 8  | [ISO/IEC 14496-8](https://ja.wikipedia.org/wiki/ISO/IEC_14496-8 "wikilink")         | [IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")上の伝送                                                                                                                       | MPEG-4コンテンツのIPネットワーク上の伝送                                                                                                                                                                             |
| 9  | [ISO/IEC TR 14496-9](https://ja.wikipedia.org/wiki/ISO/IEC_TR_14496-9 "wikilink")   | 参照ハードウェア                                                                                                                                                                                | MPEG-4の他の部のハードウェアをデザインする方法を提供。                                                                                                                                                                       |
| 10 | [ISO/IEC 14496-10](../Page/H.264.md "wikilink")                                     | [先進動画符号化](https://ja.wikipedia.org/wiki/先進動画符号化 "wikilink") (AVC)                                                                                                                       | [ITU-T](../Page/ITU-T.md "wikilink") [H.264](../Page/H.264.md "wikilink") と同一な動画圧縮符号化標準。                                                                                                             |
| 11 | [ISO/IEC 14496-11](https://ja.wikipedia.org/wiki/ISO/IEC_14496-11 "wikilink")       | シーン記述とアプリケーションエンジン                                                                                                                                                                      |                                                                                                                                                                                                      |
| 12 | [ISO/IEC 14496-12](https://ja.wikipedia.org/wiki/ISO/IEC_14496-12 "wikilink")       | [ISOベースメディアファイルフォーマット](https://ja.wikipedia.org/wiki/MP4#ISOベースメディアファイルフォーマット "wikilink")                                                                                               | [MP4](../Page/MP4.md "wikilink")フォーマット、[JPEG 2000のJP](../Page/JPEG_2000.md "wikilink")2フォーマットで用いられている、[QuickTime](../Page/QuickTime.md "wikilink")ベースの[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink") |
| 13 | [ISO/IEC 14496-13](https://ja.wikipedia.org/wiki/ISO/IEC_14496-13 "wikilink")       | [知的財産権](../Page/知的財産権.md "wikilink")の保護技術に関する規定                                                                                                                                         |                                                                                                                                                                                                      |
| 14 | [ISO/IEC 14496-14](../Page/MP4.md "wikilink")                                       | [MP4](../Page/MP4.md "wikilink")ファイルフォーマット                                                                                                                                              | 第12部に基くMP4のファイルフォーマット                                                                                                                                                                                |
| 15 | [ISO/IEC 14496-15](https://ja.wikipedia.org/wiki/ISO/IEC_14496-15 "wikilink")       | AVCファイルフォーマット                                                                                                                                                                           | [H.264 AVCに関する](../Page/H.264.md "wikilink")/MPEG-4[MP4](../Page/MP4.md "wikilink")ファイルフォーマットの拡張                                                                                                     |
| 16 | [ISO/IEC 14496-16](https://ja.wikipedia.org/wiki/ISO/IEC_14496-16 "wikilink")       | アニメーションフレームワーク拡張 (AFX)                                                                                                                                                                  | 主に3次元グラフィクスに関する規定                                                                                                                                                                                    |
| 17 | [ISO/IEC 14496-17](https://ja.wikipedia.org/wiki/ISO/IEC_14496-17 "wikilink")       | Timed Text subtitle format.                                                                                                                                                             |                                                                                                                                                                                                      |
| 18 | [ISO/IEC 14496-18](https://ja.wikipedia.org/wiki/ISO/IEC_14496-18 "wikilink")       | フォント圧縮とストリーミング                                                                                                                                                                          | [OpenType](../Page/OpenType.md "wikilink")フォントの規定                                                                                                                                                    |
| 19 | [ISO/IEC 14496-19](https://ja.wikipedia.org/wiki/ISO/IEC_14496-19 "wikilink")       | 合成テクスチャストリーム                                                                                                                                                                            |                                                                                                                                                                                                      |
| 20 | [ISO/IEC 14496-20](https://ja.wikipedia.org/wiki/ISO/IEC_14496-20 "wikilink")       | 軽量応用シーン表現 (LASeR).                                                                                                                                                                      |                                                                                                                                                                                                      |
| 21 | [ISO/IEC 14496-21](https://ja.wikipedia.org/wiki/ISO/IEC_14496-21 "wikilink")       | MPEG-J グラフィカルフレームワーク拡張 (GFX)                                                                                                                                                            |                                                                                                                                                                                                      |
| 22 | [ISO/IEC 14496-22](https://ja.wikipedia.org/wiki/ISO/IEC_14496-22 "wikilink")       | 公開フォントフォーマット仕様 (OFFS)                                                                                                                                                                   | [OpenType](../Page/OpenType.md "wikilink")に基く。                                                                                                                                                       |
| 23 | [ISO/IEC 14496-23](https://ja.wikipedia.org/wiki/ISO/IEC_14496-23 "wikilink")       | シンボル音楽表現 (SMR)                                                                                                                                                                          |                                                                                                                                                                                                      |
| 24 | [ISO/IEC TR 14496-24](https://ja.wikipedia.org/wiki/ISO/IEC_TR_14496-24 "wikilink") | Audio and systems interaction                                                                                                                                                           |                                                                                                                                                                                                      |
| 25 | [ISO/IEC 14496-25](https://ja.wikipedia.org/wiki/ISO/IEC_14496-25 "wikilink")       | 3D Graphics Compression Model                                                                                                                                                           |                                                                                                                                                                                                      |
| 26 | [ISO/IEC 14496-26](https://ja.wikipedia.org/wiki/ISO/IEC_14496-26 "wikilink")       | Audio Conformance                                                                                                                                                                       |                                                                                                                                                                                                      |
| 27 | [ISO/IEC 14496-27](https://ja.wikipedia.org/wiki/ISO/IEC_14496-27 "wikilink")       | 3D Graphics conformance                                                                                                                                                                 |                                                                                                                                                                                                      |
| 28 | [ISO/IEC 14496-28](https://ja.wikipedia.org/wiki/ISO/IEC_14496-28 "wikilink")       | Composite font representation                                                                                                                                                           |                                                                                                                                                                                                      |
| 29 | [ISO/IEC 14496-29](https://ja.wikipedia.org/wiki/ISO/IEC_14496-29 "wikilink")       | Web video coding                                                                                                                                                                        |                                                                                                                                                                                                      |
| 30 | [ISO/IEC 14496-30](https://ja.wikipedia.org/wiki/ISO/IEC_14496-30 "wikilink")       | Timed text and other visual overlays in ISO base media file format                                                                                                                      |                                                                                                                                                                                                      |

## MPEG-4 システム（第1部）

マルチメディアデータをファイルや記録メディアに保存したり、ネットワーク上で伝送するには、動画と音声毎に別々に符号化した符号化データの統合(多重化)と同期のための仕組みが必要となる。この多重化方式を規定するものがシステムである。なお、システムによって多重化される以前の動画像や音声のバイナリデータをエレメンタリストリーム(ES: Elementary Stream)と呼ぶ。

動画像と音声のエレメンタリストリームを多重化するという目的においては、[MPEG-1](../Page/MPEG-1.md "wikilink")や[MPEG-2](../Page/MPEG-2.md "wikilink")のシステムに近いといえるが、MPEG-4についてはオブジェクト符号化という概念があるという点で異なる。MPEG-4においては、オーディオ、ビジュアル（ビデオ）のデータは各1つのオブジェクトとして扱われ、これらのオブジェクトを多重化・同期するのがシステムの役割である。なお、MPEG-4の動画像(ビジュアルおよびAVC)や音声のエレメンタリストリームの多重化には、MPEG-4システムの他に[MPEG-2トランスポートストリーム](https://ja.wikipedia.org/wiki/MPEG-2_SYSTEMS "wikilink")(MPEG-2 TS)を用いることも可能であり、[地上デジタルテレビジョン放送](https://ja.wikipedia.org/wiki/地上デジタルテレビジョン放送 "wikilink")の[1セグメント放送ではAVCとAACの伝送にMPEG](../Page/ワンセグ.md "wikilink")-2 TSが用いられる。

さらに、複数のオブジェクトを組み合わせて扱うことを可能にするためのシーン記述のための仕様として、[VRML](../Page/VRML.md "wikilink")97をベースとしたBIFS(Binary Format for Scenes)が規定されている。例えば、人物や背景の動画および音声をそれぞれ別個のオブジェクトとして符号化し、それらを重ね合わせて表示したり、ユーザが任意にオブジェクトを動かしたりできるようなアプリケーションを作ることが可能である。しかし、このようなオブジェクト符号化は、一般向けに実用化されていないのが現状である。

オブジェクト符号化の概念の導入やBIFSなどにより、MPEG-4システムの内容が肥大化してしまったため、ファイルフォーマット(MP4)に関しては後述のPart 14として独立して規定されている。ちなみに、ネットワーク上での伝送に関しては、Part 8および[RFC 3640](http://www.faqs.org/rfcs/rfc3640.html)で規定されている。

なお、バイナリフォーマットであるBIFSを容易に扱えるようにするため、[XML準拠の記述形式として](../Page/Extensible_Markup_Language.md "wikilink")、Extensible MPEG-4 Textual Format in XML (XMT)がPart 11で規定されている。

## MPEG-4 動画（第2部）

[MPEG-1](../Page/MPEG-1.md "wikilink")では[ビデオCD](../Page/ビデオCD.md "wikilink")、[MPEG-2](../Page/MPEG-2.md "wikilink")では放送や[HDTVでの使用を想定しているのに対して](https://ja.wikipedia.org/wiki/高精細度テレビジョン放送 "wikilink")、MPEG-4では低ビットレートでの使用にまで用途を拡大することを目標として規格化が開始された。符号化技術としては先に規格化が進んでいた[H.263](../Page/H.263.md "wikilink")を基に幾つかのツールを追加した構成になっている。H.263との相違点は、[フレーム間予測](../Page/フレーム間予測.md "wikilink")におけるBフレームの採用、DCT係数のAC/DC予測の導入、などが挙げられる。

このビジュアル技術自体も、エラー耐性技術のほか、任意形状技術やスプライト符号化技術、顔画像の動きを符号化するフェース（Face）符号化技術、スケーラビリティ技術などを盛り込んだ巨大なものであったが、現在ではエラー耐性技術のほかは殆ど使用されていない。

圧縮アルゴリズムの基本原理は、[MPEG-1](../Page/MPEG-1.md "wikilink")、[MPEG-2](../Page/MPEG-2.md "wikilink")、[H.263](../Page/H.263.md "wikilink")などと基本的には同様であり、[空間変換](https://ja.wikipedia.org/wiki/空間変換 "wikilink")や[フレーム間予測](../Page/フレーム間予測.md "wikilink")、[量子化](https://ja.wikipedia.org/wiki/量子化 "wikilink")、[エントロピー符号化](https://ja.wikipedia.org/wiki/エントロピー符号化 "wikilink")を採用している。

### 空間変換

MPEG-4では、空間変換に[離散コサイン変換](../Page/離散コサイン変換.md "wikilink")が用いられる。8×8画素のブロックを単位として、原画像もしくは[フレーム間予測](../Page/フレーム間予測.md "wikilink")の予測誤差画像のDCT係数を求め、その係数を[量子化](https://ja.wikipedia.org/wiki/量子化 "wikilink")している。

### フレーム間予測

[フレーム間予測](../Page/フレーム間予測.md "wikilink")において参照フレームとして指定できるフレームは、Iフレーム, Pフレーム、Bフレームが存在する。Pフレームでは時間軸で前方のフレーム1枚の画像を利用して符号化を行うが、Bフレームでは前方・後方2枚の画像を利用して符号化を行う。

### 1/4画素精度動き補償

動き補償の精度としては1/2画素精度まで基本的に利用可能である。MPEG-4 ASP(Advanced Simple Profile)では、1/4画素精度動き補償も採用している。

### AC/DC予測

空間変換で得られたDCT係数に対して、さらに係数の最上列ないし最左列の係数から予測を行って情報量を削減する技術が導入されている。

DC予測とは、隣接した「左MBと左上MBのDC成分の変化量」と「左上MBと上MBのDC成分の変化量」を比較して、より傾きの小さい方向から現在のMBのDC成分を予測する手法である。この方法を用いることによって、相関の高い画素からの予測を行うことが可能であるため、圧縮率の向上が期待できる。

AC予測とは、フレーム間予測を用いずに符号化される画素ブロックについて、単純に[離散コサイン変換](../Page/離散コサイン変換.md "wikilink")(DCT)の係数を量子化して符号化するのではなく、DCT係数行列のうち最上列ないし最左行の値について、上ないし左の隣接ブロックの値との差分を符号化することによって符号量を削減する方式である。予測の方向の決定については、DC予測での予測方向に従う。 この予測方式は、後にH.263でもAnnex Iとして採用された。

DC予測は必ず使用しなければならず、AC予測は使用有無をヘッダで切り替えることが可能である。

### エントロピー符号化

ハフマン符号をベースとした[可変長符号化](https://ja.wikipedia.org/wiki/可変長符号化 "wikilink")(VLC; Variable Length Coding)が採用されている。

## MPEG-4 音響（第3部）

{{ main|MPEG-4 Part 3}}

MPEG-4の音響符号化技術では、もっとも広く知られている[MPEG-4 AACの他にも](../Page/AAC.md "wikilink")[MPEG-4 CELP](https://ja.wikipedia.org/wiki/MPEG-4_CELP "wikilink")、[TwinVQ](https://ja.wikipedia.org/wiki/TwinVQ "wikilink")、[HVXC](https://ja.wikipedia.org/wiki/HVXC "wikilink")(Harmonic Vector eXcitation Coding)、[HILN](https://ja.wikipedia.org/wiki/HILN "wikilink")(Harmonic and Individual Lines plus Noise)、[TTSI](../Page/音声合成.md "wikilink")(Text To Speech Interface) など様々な音響符号化技術が規格化されている。

### AAC（先進的音響符号化）

MPEG-4 第3部で採択された[AAC](../Page/AAC.md "wikilink")符号化には以下の種類がある。

  - Low Complexity Advanced Audio Coding (LC-AAC)
  - High-Efficiency Advanced Audio Coding ([HE-AAC](../Page/HE-AAC.md "wikilink"))
  - Scalable Sample Rate Advanced Audio Coding (AAC-SSR)
  - Bit Sliced Arithmetic Coding (BSAC)
  - Long Term Predictor (LTP)

### ALS（音響ロスレス圧縮方式）

MPEG-4 第3部 サブパート11において、圧縮時に音響符号が劣化しない[MPEG-4 ALS技術が規格化された](https://ja.wikipedia.org/wiki/MPEG-4_ALS "wikilink")。

### SLS（段階化ロスレス圧縮方式）

MPEG-4 第3部 サブパート12において、圧縮時にAAC部分の階層と、補完してロスレスになる階層の複数階層で音響を符号化できる[MPEG-4 SLSが規格化された](https://ja.wikipedia.org/wiki/MPEG-4_SLS "wikilink")。SLS符号化された音響信号は、SLS再生機では劣化せず再生でき、さらにAAC再生機でも再生できるという特徴を持つ。

## MPEG-4 AVC 動画（第10部）

第2部では、規格範囲が拡散しすぎてしまったという反省のもと、通常の動画像の[圧縮効率](https://ja.wikipedia.org/wiki/圧縮効率 "wikilink")を追求するという方針のもと開発が進められた（第2部では使用されることがなかったフェース技術やスケーラブル技術は範囲から外されている）。[ITU-T](../Page/ITU-T.md "wikilink")と共同で規格化したものでありH.264と同じもの。H.264/AVCとも呼ばれる。詳細は[H.264](../Page/H.264.md "wikilink")ページを参照のこと。

## MPEG-4 ファイルフォーマット (第12および14部）

マルチメディアデータをファイルに記録するには、動画像と音声のエレメンタリストリームを多重化する必要があるが、後で再生する際に早送りや編集を容易にするためにフレーム単位でアクセスできるように、データを区分けして、さらにアクセス用管理データを付加する方が便利である。MPEG-4では、そのための[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")としてMP4ファイルフォーマットを規定している。

音声の場合には、ファイルフォーマットに格納せず、符号化データをそのまま使用することもある。[MPEG-1](../Page/MPEG-1.md "wikilink")などで規定された[MP3](../Page/MP3.md "wikilink")はこの例である。

MP4ファイルフォーマットは[アップルの](../Page/アップル_\(企業\).md "wikilink")[QuickTime](../Page/QuickTime.md "wikilink")のファイルフォーマットをベースに開発されている\[2\]。QuickTimeファイルフォーマットで採用されているファイル構造は、さまざまな動画像や音声のエレメンタリストリームを柔軟に多重化可能となっており、汎用的なファイルフォーマットとしてISOベースメディアファイルフォーマット(Part 12)に採用された。このPart 12からMPEG-4用のファイルフォーマットとして派生したものがMP4ファイルフォーマットである。詳細は、[MP4](../Page/MP4.md "wikilink")ページ参照。

## プロファイルとレベル

ビジュアル、オーディオ共その規格内において、[プロファイルとレベルと呼ばれる概念が規定されている](https://ja.wikipedia.org/wiki/プロファイル_\(工学\) "wikilink")。プロファイルとは使用できるツールを示すものであり、レベルとは使用できるパラメータの範囲を規定するものである。例えば、MPEG-4 Part 2では、シンプルプロファイル(SP)、アドバンスドシンプルプロファイル(ASP)、メインプロファイル (MP)などが規定されそれぞれ使用可能なツールが異なる。[MPEG-4 AVCでは](../Page/H.264.md "wikilink")、ベースラインプロファイル、メインプロファイル、拡張(Extended)プロファイルの3種類が規定されていたが、2004年に高忠実度化規格（FRExt）が策定され、ハイプロファイル、ハイ10プロファイル、ハイ4:2:2プロファイル、ハイ4:4:4プロファイルの4種類が新たに規定された。

## 歴史

[1999年](../Page/1999年.md "wikilink")に規格化された直後から、動画像を長時間記録する用途で[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")の一機能として使用された。当初は、ファイルフォーマットが規格化されていなかったため、[マイクロソフト](../Page/マイクロソフト.md "wikilink")社の[ASFファイルフォーマットが使用された](../Page/Advanced_Systems_Format.md "wikilink")。近年では、第三世代[携帯電話](../Page/携帯電話.md "wikilink")の動画フォーマットとして採用され、PDAを含めてモバイルで見る動画フォーマットの主流になりつつある。特に[iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")や[PSPがこのフォーマットに対応したことを機に爆発的に普及している](../Page/PlayStation_Portable.md "wikilink")。これらの動画符号化技術は、現状MPEG-4 Part 2であるが、2005年後半からは、MPEG-4 AVCも使用されることが確実視されている。

放送や通信分野においては、ライセンスの問題もあり主だった利用例も少なかったが、MPEG-4 AVC (H.264)が[地上波デジタル放送の携帯端末向け](https://ja.wikipedia.org/wiki/地上デジタルテレビジョン放送 "wikilink")(1セグメント)放送での採用、[Blu-ray Discや](../Page/Blu-ray_Disc.md "wikilink")[HD DVDのビデオ](../Page/HD_DVD.md "wikilink")・[コーデック](../Page/コーデック.md "wikilink")として承認、などされており、応用例は増えていく見込みである。

## 利用例

### 3GPP/3GPP2動画フォーマット

[第三世代携帯電話](https://ja.wikipedia.org/wiki/第三世代携帯電話 "wikilink")の業界団体である[3GPP](../Page/3GPP.md "wikilink")と[3GPP2](../Page/3GPP2.md "wikilink")は、動画コンテンツにMPEG-4を採用している。なお、同じファイルフォーマットをサポートした[第二世代携帯電話](https://ja.wikipedia.org/wiki/第二世代携帯電話 "wikilink")端末も存在する。

  - [コンテナに](../Page/コンテナフォーマット.md "wikilink")[MP4](../Page/MP4.md "wikilink")ファイルフォーマット
  - 音声に[AMR又は](../Page/Adaptive_Multi-Rate.md "wikilink")[AAC](../Page/AAC.md "wikilink")
  - 映像には[H.263](../Page/H.263.md "wikilink")又はMPEG-4 Part 2(のSimple Profile)

を使用している。[解像度はQCIF](../Page/画面解像度.md "wikilink")(Sub-QCIF)などに限定されているが、一部端末では[QVGAなども利用可能](../Page/Quarter_Video_Graphics_Array.md "wikilink")。

### DivX

2000年代前半に[パソコンで動画を扱う際によく使われた](../Page/パーソナルコンピュータ.md "wikilink")[DivX](https://ja.wikipedia.org/wiki/DivX "wikilink")や[Xvid](../Page/Xvid.md "wikilink")はMPEG-4 Visual (Video) の技術を利用したものである。これらを利用した映像を[AVIの箱](../Page/Audio_Video_Interleave.md "wikilink")(コンテナ)に収めたものは一部の[DVDプレーヤー](../Page/DVDプレーヤー.md "wikilink")や[ゲーム機](../Page/ゲーム機.md "wikilink")等での再生に対応している。

  - (DivX + MP3).avi

### メモリーカード規格

[SDメモリーカード](https://ja.wikipedia.org/wiki/SDメモリーカード "wikilink")のSD-Video規格や[メモリースティック](../Page/メモリースティック.md "wikilink")の[メモリースティックビデオ](../Page/メモリースティックビデオ.md "wikilink")フォーマットにMPEG-4が採用されている。前者は[ASF形式](../Page/Advanced_Systems_Format.md "wikilink")、後者は[MP4](../Page/MP4.md "wikilink")を採用している。

## 脚注

## 関連項目

  - [MPEG-1](../Page/MPEG-1.md "wikilink")
  - [MPEG-2](../Page/MPEG-2.md "wikilink")
  - [MPEG-7](https://ja.wikipedia.org/wiki/MPEG-7 "wikilink")
  - [MPEG-21](https://ja.wikipedia.org/wiki/MPEG-21 "wikilink")
  - [MPEG-4オーディオ](https://ja.wikipedia.org/wiki/MPEG-4オーディオ "wikilink")
  - [MP4](../Page/MP4.md "wikilink")
  - [MS-MPEG4](https://ja.wikipedia.org/wiki/MS-MPEG4 "wikilink")
  - [AAC](../Page/AAC.md "wikilink")
  - [3GPP](../Page/3GPP.md "wikilink")
  - [3GPP2](../Page/3GPP2.md "wikilink")
  - [H.263](../Page/H.263.md "wikilink")
  - [H.264](../Page/H.264.md "wikilink")

## 外部リンク

  - [MPEG-4](https://mpeg.chiariglione.org/standards/mpeg-4) - MPEGオフィシャルサイト

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:MPEG](https://ja.wikipedia.org/wiki/Category:MPEG "wikilink")

1.
2.