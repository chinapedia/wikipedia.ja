> この記事は[Ffdshow](https://ja.wikipedia.org/wiki/Ffdshow)から翻訳されています。


**ffdshow** （<small>エフエフディーショウ、エフエフダイレクトショウ</small>）とは、[動画](../Page/動画.md "wikilink")・[音声](https://ja.wikipedia.org/wiki/音声 "wikilink")形式の圧縮・伸張を行う為の [DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink") フィルタと [VFW](https://ja.wikipedia.org/wiki/Video_for_Windows "wikilink") [コーデック](../Page/コーデック.md "wikilink")である。

## 概要

主に高速で高画質な[デコーダとして利用されている](../Page/エンコード.md "wikilink")。[MPEG-4](../Page/MPEG-4.md "wikilink") ([Xvid](https://ja.wikipedia.org/wiki/Xvid "wikilink"), [DivX](https://ja.wikipedia.org/wiki/DivX "wikilink"), [H.264](https://ja.wikipedia.org/wiki/H.264 "wikilink") 等) の他にも数多くの動画・音声形式に対応している。また、[インタレース解除](https://ja.wikipedia.org/wiki/インターレース#プログレッシブへの変換 "wikilink")、[ポストプロセッシング](https://ja.wikipedia.org/wiki/ポストプロセッシング "wikilink")、リサイズ、シャープ、字幕などの多彩な画像処理フィルタ、イコライザ、ミキサなどの音声処理フィルタを備えている。

ffdshow は[メディアプレイヤや](https://ja.wikipedia.org/wiki/メディアプレーヤー "wikilink")[スプリッタを内蔵していない](https://ja.wikipedia.org/wiki/スプリッタフィルタ "wikilink")。その代わりに ffdshow を導入すると、DirectShow, VFW に対応したメディアプレイヤで自動的に ffdshow の機能が使用されるようになる。

[FFmpeg](../Page/FFmpeg.md "wikilink") を始めとする多くの[ライブラリ](../Page/ライブラリ.md "wikilink")を、DirectShow, VFWで利用できるようにした[オープンソース](../Page/オープンソース.md "wikilink")の[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。当初の主要な開発者は Milan Cutka であったが、Milan Cutka による更新は[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[5月](https://ja.wikipedia.org/wiki/5月 "wikilink")に停止された。その後、元の ffdshow と同じく [SourceForge.net](../Page/SourceForge.net.md "wikilink") において、[ffdshow-tryouts](http://sourceforge.net/projects/ffdshow-tryout/) が企画され、事実上開発を引き継いだ為、現在ではこれが ffdshow を名乗っている。

[GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") は[日本語](../Page/日本語.md "wikilink")に対応している。

## 動作環境

対応 [OS](../Page/オペレーティングシステム.md "wikilink")

  - Windows XP 以降
  - Windows 98/Me/2000 （リビジョンによる制限あり）

ffdshow-tryouts beta7 は日本語を指定すると、インストーラが文字化けする。ffdshow-tryouts beta6 は Windows 2000/Xp/Server 2003/Vista に対応している。 Windows2000 で動作する最後のビルドは clsid によるリビジョン 3904(20110623) である｡ Windows98/Me で動作する最後のビルドは clsid によるリビジョン 2322 である。

## 対応コーデック

以下が対応している主な[コーデック](../Page/コーデック.md "wikilink")である（[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")（[平成](../Page/平成.md "wikilink")22年）[9月14日](../Page/9月14日.md "wikilink")現在）。

### 映像コーデック

  - [MPEG-1](../Page/MPEG-1.md "wikilink")
  - [MPEG-2](../Page/MPEG-2.md "wikilink")
  - [MPEG-4](../Page/MPEG-4.md "wikilink")
      - [XviD](https://ja.wikipedia.org/wiki/XviD "wikilink")
      - [DivX](https://ja.wikipedia.org/wiki/DivX "wikilink")
      - [RMP4](https://ja.wikipedia.org/wiki/RMP4 "wikilink")
      - [3ivx](https://ja.wikipedia.org/wiki/3ivx "wikilink")
  - [MS-MPEG4](https://ja.wikipedia.org/wiki/MS-MPEG4 "wikilink")
  - [Dirac](https://ja.wikipedia.org/wiki/Dirac "wikilink")
  - [H.263](https://ja.wikipedia.org/wiki/H.263 "wikilink") ([FLV1](https://ja.wikipedia.org/wiki/Flash_Video "wikilink"))
  - [H.264](https://ja.wikipedia.org/wiki/H.264 "wikilink") ([x264](https://ja.wikipedia.org/wiki/x264 "wikilink"))
      - [H.264 Lossless](https://ja.wikipedia.org/wiki/H.264_Lossless "wikilink")
  - [Motion JPEG](https://ja.wikipedia.org/wiki/Motion_JPEG "wikilink")
      - [Lossless JPEG](https://ja.wikipedia.org/wiki/Lossless_JPEG "wikilink")
  - [DV](../Page/DV_\(ビデオ規格\).md "wikilink")
  - [Huffyuv](https://ja.wikipedia.org/wiki/Huffyuv "wikilink")
  - [Indeo Video](../Page/Indeo.md "wikilink")
  - [VP3](https://ja.wikipedia.org/wiki/VP3 "wikilink")
  - [VP6](https://ja.wikipedia.org/wiki/VP6 "wikilink") ([FLV4](https://ja.wikipedia.org/wiki/Flash_Video "wikilink"))
  - [VP8](https://ja.wikipedia.org/wiki/VP8 "wikilink")
  - [Theora](https://ja.wikipedia.org/wiki/Theora "wikilink")
  - [RealVideo](https://ja.wikipedia.org/wiki/RealVideo "wikilink")
  - [Chinese AVS](https://ja.wikipedia.org/wiki/AVS_\(コーデック\) "wikilink")
  - [Cinepak](../Page/Cinepak.md "wikilink")
  - [CorePNG](https://ja.wikipedia.org/wiki/CorePNG "wikilink")
  - [MSZH](https://ja.wikipedia.org/wiki/MSZH "wikilink")
  - [ZLIB](https://ja.wikipedia.org/wiki/AVIzlib "wikilink")
  - [Windows Media Video](https://ja.wikipedia.org/wiki/Windows_Media_Video "wikilink")
      - [VC-1](https://ja.wikipedia.org/wiki/VC-1 "wikilink")

### 音声コーデック

  - [AAC](../Page/AAC.md "wikilink")
  - [AC3](../Page/ドルビーデジタル.md "wikilink")
  - [EAC3](https://ja.wikipedia.org/wiki/EAC3 "wikilink")
  - [ADPCM](https://ja.wikipedia.org/wiki/適応的差分パルス符号変調 "wikilink")
  - [AMR](../Page/Adaptive_Multi-Rate.md "wikilink")
  - [ATRAC](https://ja.wikipedia.org/wiki/ATRAC "wikilink")3
  - [Dolby TrueHD](https://ja.wikipedia.org/wiki/Dolby_TrueHD "wikilink")
  - [DTS](https://ja.wikipedia.org/wiki/デジタル・シアター・システムズ "wikilink")
  - [DTS-HD](https://ja.wikipedia.org/wiki/DTS-HD "wikilink")
  - [FLAC](../Page/FLAC.md "wikilink")
  - [リニア PCM](../Page/パルス符号変調.md "wikilink")
  - [MLP](https://ja.wikipedia.org/wiki/MLP "wikilink")
  - [MP1](https://ja.wikipedia.org/wiki/MP3#MPEG-1/2_Audio_Layer-1 "wikilink")
  - [MP2](https://ja.wikipedia.org/wiki/MP3#MPEG-1/2_Audio_Layer-2 "wikilink")
  - [MP3](../Page/MP3.md "wikilink")
  - [Nellymoser](https://ja.wikipedia.org/wiki/Nellymoser "wikilink")
  - [Vorbis](https://ja.wikipedia.org/wiki/Ogg_Vorbis "wikilink")
  - [QDesign Music](https://ja.wikipedia.org/wiki/QDesign_Music "wikilink")
  - [True Audio](https://ja.wikipedia.org/wiki/TTA "wikilink")
  - [TrueSpeech](https://ja.wikipedia.org/wiki/TrueSpeech "wikilink")
  - [MACE](https://ja.wikipedia.org/wiki/MACE "wikilink")
  - [Windows Media Audio](https://ja.wikipedia.org/wiki/Windows_Media_Audio "wikilink")

## 備考

**ffdshow**及び**ffdshow tryouts**の開発は停滞しており、このソフトの利用者には[LAV Filtersを後継として使うことが推奨されている](https://ja.wikipedia.org/wiki/LAV_Filters "wikilink")。\[1\]

## 関連項目

  - [libavcodec](https://ja.wikipedia.org/wiki/libavcodec "wikilink")
  - [FFmpeg](../Page/FFmpeg.md "wikilink")
  - [Video for Windows](https://ja.wikipedia.org/wiki/Video_for_Windows "wikilink")
  - [DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")
  - [コーデック](../Page/コーデック.md "wikilink")
  - [ソフトウェア特許](https://ja.wikipedia.org/wiki/ソフトウェア特許 "wikilink")

## 脚注

## 外部リンク

  - [ffdshow 公式サイト](http://sourceforge.net/projects/ffdshow-tryout/) [(日本語サイト)](http://sourceforge.jp/projects/ffdshow-tryout/)
  - [ffdshow 旧・公式サイト](http://sourceforge.net/projects/ffdshow/)
  - [Wiki, オンラインヘルプ](http://ffdshow-tryout.sourceforge.net/wiki)  - [（日本語訳）](http://sourceforge.jp/projects/ffdshow-tryout/wiki/FrontPage)
  - [ffdshow-tryouts 更新履歴](http://ffdshow-tryout.sourceforge.net/wiki/changelog)
  - [ffdshow-tryouts サポートフォーラム](http://ffdshow-tryout.sourceforge.net/phpBB2/)  - [サポートフォーラム](http://ffdshow-tryout.sourceforge.net/phpBB2/viewtopic.php?t=144)
  - [ffdshow-tryouts 公式ダウンロード](http://sourceforge.net/projects/ffdshow-tryout/files/)  - [(日本語ダウンロード)](http://sourceforge.jp/projects/ffdshow-tryout/releases/)

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.