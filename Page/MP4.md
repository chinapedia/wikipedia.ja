> この記事は[MP4](https://ja.wikipedia.org/wiki/MP4)から翻訳されています。


**MP4**（エムピーフォー）はデジタルマルチメディアコンテナファイルフォーマットである。ビデオやオーディオを格納するのによく用いられ、他にも字幕や静止画なども格納できる。[MPEG-4](../Page/MPEG-4.md "wikilink")規格の一部で、**MPEG-4 Part 14**（正式には**ISO/IEC 14496-14:2003**、[ISO/IEC JTC 1](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink")）で標準化されている。

拡張子.mp4を推奨されており、[MPEG-4](../Page/MPEG-4.md "wikilink")の動画・音声の記録に用いられている。また、[第3世代携帯電話の業界団体である](../Page/第3世代移動通信システム.md "wikilink")[3GPP](../Page/3GPP.md "wikilink")および[3GPP2](../Page/3GPP2.md "wikilink")でも、これに独自拡張を加えたものが標準ファイルフォーマットとして採用されている（あくまで標準であり[キャリアごとにさらなる拡張が加えられている](../Page/電気通信事業者.md "wikilink")）。

## 歴史

2001年に最初の標準であるMPEG-4 Part1:Systems（ISO/IEC 14496-1:2001）が標準化された。この規格は後の規格と区別するため「MP4 version1」と呼ばれる。これはApple社のQuickTimeコンテナフォーマットをもとに策定された。

2003年には「MP4 version2」として知られる MPEG-4 Part14:MP4 file format（ISO/IEC 14496-14:2003）で標準化された。この規格は「ISOベースメディアファイルフォーマット」（MPEG-4 Part12、ISO/IEC 14496-12:2003）を拡張して作られている。

2004年には「MP4 AVCE」（MPEG-4 Part15、ISO/IEC 14496-15:2004）と呼ばれる拡張規格が定められ、[H.264](../Page/H.264.md "wikilink")や[AAC](../Page/AAC.md "wikilink")を格納できるようになった。

## 技術詳細

### ISOベースメディアファイルフォーマット

[Relations_between_ISO_Base_Media_File_Format_and_MP4_File_Format.svg](https://ja.wikipedia.org/wiki/File:Relations_between_ISO_Base_Media_File_Format_and_MP4_File_Format.svg "fig:Relations_between_ISO_Base_Media_File_Format_and_MP4_File_Format.svg") MPEG-4の第12部 (ISO/IEC 14496-12) で規定されているISOベースメディアファイルフォーマットは[木構造を持ち](../Page/木構造_\(データ構造\).md "wikilink")、各ノードを**ボックス** (**box**) と呼ぶ。あるいは、元になった[QuickTime](../Page/QuickTime.md "wikilink")ファイルフォーマットの用語である**アトム** (**atom**) と呼ぶこともある。また、一つないし複数のボックスを子要素として持つことができるボックスがあり、その親要素のボックスを**コンテナボックス** (**container box**) ないし単に**コンテナ**と呼ぶ。コンテナが子要素以外のデータを持つことはできない。各ボックスの先頭には符号なし32[ビット](../Page/ビット.md "wikilink")[整数型](../Page/整数型.md "wikilink")の自身のサイズおよび、半角英数4文字（32ビット）のボックスタイプが必ず与えられる。なお、慣例的にボックスタイプは小文字で記述される。

ボックス構造を採用したことにより、複数の**トラック** (**track**) を同時に1つのファイルに格納したり、時刻情報やメタデータを記述することにより多重化や任意時刻でのアクセス（ランダムアクセス）を容易に実現できる。また、さまざまな種類のメディアを柔軟に扱えるという特徴もあり、MP4のようにMPEGに完全に準拠したメディアのみを含むことだけでなく、3GPP/3GPP2などのようにMPEGの規格外であるAMRやH.263などのメディアを含むことも可能である。

ボックス構造の扱い方はある程度はユーザが任意に決めることができる。例えば、動画、音声などのストリームを単純に直列に並べることも可能であり、また、同期やランダムアクセスを容易にするために動画と音声を細切れに格納することも可能である。

#### ボックス構造

ISOベースメディアファイルフォーマットのボックス構造は木構造をとるが、ここでは主なボックスについて述べる。実際には多数の木構造のボックスが含まれ、さまざまなレベルの情報を柔軟に格納することができるようになっている。

  - ftyp：ファイルタイプの記述。ファイルの先頭にただ一つだけ含まれる。
  - moov：全てのメタデータを含むコンテナ。ファイル中にただ一つだけ含まれる。[メタデータ](../Page/メタデータ.md "wikilink")として含まれる情報としては、各トラック（動画、音声など）のヘッダ情報やコンテンツの内容のメタ記述、時刻情報などが含まれる。
  - mdat：トラックのメディアデータ本体のコンテナ。ファイル中のmdatボックスの数は任意である。すなわち、動画と音声、動画だけ、音声だけ、あるいは複数の種類のトラックを同時に含む、などのように、任意のトラック構成を持てるようになっている。

### MP4ファイルフォーマット

MP4ファイルフォーマットは、ISOベースメディアファイルフォーマットに対して、MPEG-4の[オブジェクト符号化に対応するためのオブジェクト記述ボックス](https://ja.wikipedia.org/wiki/MPEG-4#MPEG-4_システム（第1部） "wikilink") (iods) の追加や、動画や音声などのエレメンタリストリームに関する情報を記述するサンプル記述ボックス (mp4v, mp4a, mp4s) の追加などの拡張を行ったものである。

#### 格納できるメディアの種類

MP4ファイルは以下に示す映像・音声[コーデック](../Page/コーデック.md "wikilink")のメディアデータを組み合わせて（多重化して）格納し利用できる。

  - ビデオ：[MPEG-1](../Page/MPEG-1.md "wikilink")、[MPEG-2](../Page/MPEG-2.md "wikilink")、MPEG-4 Visual ([MPEG-4 Part 2](https://ja.wikipedia.org/wiki/MPEG-4#MPEG-4_動画（第2部） "wikilink"))、[H.264 AVC](../Page/H.264.md "wikilink")/MPEG-4 (MPEG-4 Part 10)、[H.265](https://ja.wikipedia.org/wiki/H.265 "wikilink") (H.265/HEVC)、[AV1](https://ja.wikipedia.org/wiki/AOMedia_Video_1 "wikilink") など
  - オーディオ：[AAC](../Page/AAC.md "wikilink")、[HE-AAC](../Page/HE-AAC.md "wikilink")、[MP3](../Page/MP3.md "wikilink")、[MP2](https://ja.wikipedia.org/wiki/MP3#MPEG-1/2_Audio_Layer-1 "wikilink")、[MP1](https://ja.wikipedia.org/wiki/MP3#MPEG-1/2_Audio_Layer-2 "wikilink")、[MPEG-4 ALS](https://ja.wikipedia.org/wiki/MPEG-4_ALS "wikilink")、[TwinVQ](https://ja.wikipedia.org/wiki/TwinVQ "wikilink")、[CELP](https://ja.wikipedia.org/wiki/CELP "wikilink")（**QCELPとは異なるので注意）**、[Opus](https://ja.wikipedia.org/wiki/Opus_\(音声圧縮\) "wikilink") など
  - 静止画：[PNG](../Page/Portable_Network_Graphics.md "wikilink")、[JPEG](../Page/JPEG.md "wikilink")
  - テキスト

また、[3GPP](../Page/3GPP.md "wikilink")/[3GPP2](../Page/3GPP2.md "wikilink")ファイルフォーマットでは、[H.263](../Page/H.263.md "wikilink")、[MPEG-4](../Page/MPEG-4.md "wikilink")（オプション）、[AMR](../Page/Adaptive_Multi-Rate.md "wikilink")、[AAC](../Page/AAC.md "wikilink")などを格納できる。

#### 拡張子

仕様書では、MP4ファイルの[拡張子](../Page/拡張子.md "wikilink")は.mp4が望ましいとされている。.m4vや.m4a、.m4pはアップル社が決めた拡張子であり\[1\]、[iTunes Storeで配信されるファイルはDRM技術の](https://ja.wikipedia.org/wiki/iTunes_Store "wikilink")[FairPlay](../Page/FairPlay.md "wikilink") (.m4v, .m4p) とISOで標準化されていない[AC-3](../Page/ドルビーデジタル.md "wikilink") (.m4v) が使用されることがある。また、.m4aでは[Apple Losslessがサポートされる](../Page/Apple_Lossless.md "wikilink")。

また、派生フォーマットである[3GPP](../Page/3GPP.md "wikilink")/[3GPP2](../Page/3GPP2.md "wikilink")ファイルフォーマットの拡張子はそれぞれ.3gp、.3g2である。

また、.m4rという拡張子もあり、これは[iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink")用[着信メロディ](../Page/着信メロディ.md "wikilink")に使われる拡張子であるが、中身は40秒までの長さの制約がついたMP4オーディオファイルそのものである。

また、[Adobe Flashの](../Page/Adobe_Flash.md "wikilink")[Flash Videoでは](../Page/Flash_Video.md "wikilink").f4vという拡張子が使われている。

## 利用例

MP4は下記に採用されており、実際に利用されている。

  - [Adobe Flash Player](../Page/Adobe_Flash.md "wikilink") 9以降
  - [WALKMAN](../Page/ウォークマン.md "wikilink")
  - [iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")
  - [iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink")
  - [iPad](https://ja.wikipedia.org/wiki/iPad "wikilink")
  - [PlayStation 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")
  - [QuickTime](../Page/QuickTime.md "wikilink")
  - [Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")（写真チャンネル、音声ファイルのみの対応）
  - [携帯電話](../Page/携帯電話.md "wikilink")
  - [PlayStation Portable](../Page/PlayStation_Portable.md "wikilink") (PSP)
  - [PlayStation Vita](https://ja.wikipedia.org/wiki/PlayStation_Vita "wikilink") (PS Vita)
  - [XMedia Recode](https://ja.wikipedia.org/wiki/XMedia_Recode "wikilink")
  - [YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink")
  - [ニコニコ動画](../Page/ニコニコ動画.md "wikilink")
  - [ニンテンドーDSi](https://ja.wikipedia.org/wiki/ニンテンドーDSi "wikilink")
  - [SONY XDCAM EX](../Page/XDCAM.md "wikilink")
  - [Windows Media Player](../Page/Windows_Media_Player.md "wikilink") 12以降
  - [Windows Phone](https://ja.wikipedia.org/wiki/Windows_Phone "wikilink") ([Windows Mobile](../Page/Windows_Mobile.md "wikilink"))
  - [Android](../Page/Android.md "wikilink")
  - [DivX Plus](https://ja.wikipedia.org/wiki/DivX "wikilink") v9以降
  - [mora](https://ja.wikipedia.org/wiki/mora "wikilink")
  - [chromebook](https://ja.wikipedia.org/wiki/chromebook "wikilink")

## 脚注

## 関連項目

  - [HTML5](../Page/HTML5.md "wikilink")
  - [データ圧縮](../Page/データ圧縮.md "wikilink")
  - [MPEG-4](../Page/MPEG-4.md "wikilink")
  - [JPEG 2000](../Page/JPEG_2000.md "wikilink")

## 外部リンク

  - 竹松昇, [MPEGラボ 第26回 携帯ゲーム機PSPの動画ファイル「MP4」とは何か](http://www.mpeg.co.jp/libraries/mpeg_labo/winPC_26.html), 朋栄アイ・ビー・イー

  - [AAC音声のMP4動画の作り方（妖精現実フェアリアル）](http://www.faireal.net/dat/d3/d30731.xml), 個人サイト

  - , 個人サイト

  - , 個人サイト

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:動画ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:動画ファイルフォーマット "wikilink") [Category:MPEG](https://ja.wikipedia.org/wiki/Category:MPEG "wikilink")

1.  アップル社ではiTunes Video format、iTunes Audio formatと表現している。