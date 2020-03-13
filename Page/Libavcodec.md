> この記事は[Libavcodec](https://ja.wikipedia.org/wiki/Libavcodec)から翻訳されています。


**libavcodec**は動画・音声データのエンコード・デコードのための[オープンソース](../Page/オープンソース.md "wikilink")なコーデックライブラリである\[1\]。2011年3月の Libav と [FFmpeg](../Page/FFmpeg.md "wikilink") の分裂に伴い、両方のプロジェクトから同一名称で互換性のない形でリリースされている。

libavcodecはマルチメディアを扱う多くのオープンソースなアプリケーションやフレームワークにとって欠かせないものである。一般的に良く使われる[MPlayer](../Page/MPlayer.md "wikilink")、[xine](https://ja.wikipedia.org/wiki/xine "wikilink")及び[VLC](https://ja.wikipedia.org/wiki/VLC "wikilink")メディアプレーヤが全サポートプラットフォーム上でたくさんの音声・動画形式を再生可能にするためにメインの内蔵デコードエンジンとしてlibavcodecを使っている。また、[ffdshow](https://ja.wikipedia.org/wiki/ffdshow "wikilink") tryoutsのデコーダにもプライマリなデコードライブラリとして使われている。[GStreamer](../Page/GStreamer.md "wikilink") FFmpeg [plugin](https://ja.wikipedia.org/wiki/plugin "wikilink")\[2\]が一般的に良く使われる[特許を持つフォーマット](../Page/ソフトウェア特許.md "wikilink")(例えば [MPEG-2](../Page/MPEG-2.md "wikilink") (DVD video)、[MPEG-4 ASP](https://ja.wikipedia.org/wiki/MPEG-4_Part_2 "wikilink")、[H.264](../Page/H.264.md "wikilink")や[プロプライエタリ](https://ja.wikipedia.org/wiki/プロプライエタリ "wikilink")なフォーマットである[Windows Media Videoや](../Page/Windows_Media_Video.md "wikilink")[VP6](../Page/VP6.md "wikilink")、[RealVideo](https://ja.wikipedia.org/wiki/RealVideo "wikilink")など)を再生するために、[Ubuntu](../Page/Ubuntu.md "wikilink")のようなLinuxディストリビューションで使うことができる\[3\]。またlibavcodecはエンコード・デコードの為に[Avidemux](https://ja.wikipedia.org/wiki/Avidemux "wikilink")や[MEncoder](https://ja.wikipedia.org/wiki/MEncoder "wikilink")、[Kdenlive](https://ja.wikipedia.org/wiki/Kdenlive "wikilink")のようなビデオエディタやトランスコーディングアプリケーションにも使われている。

## 実装しているビデオコーデック

libavcodecは以下のフォーマットの動画のデコーダとエンコーダを含む\[4\]:

  - 4X Movie
  - 8088flex TMV
  - 8SVX exponential
  - 8SVX fibonacci
  - A64 multicolor
  - American Laser Games MM
  - AMV Video
  - ANSI/ASCII art
  - Apple MJPEG-B
  - Apple QuickDraw
  - Asus v1, v2
  - ATI VCR1, VCR2
  - Auravision Aura, Auravision Aura 2
  - Autodesk Animator Flic video
  - Autodesk RLE
  - [AVS](https://ja.wikipedia.org/wiki/Audio_Video_Standard "wikilink") (デコードのみ)
  - [Bink](https://ja.wikipedia.org/wiki/Bink "wikilink") (デコードのみ)
  - Beam Software VB
  - Bethesda VID video
  - Bitmap Brothers JV video
  - Brute Force & Ignorance
  - C93 video
  - [CamStudio](https://ja.wikipedia.org/wiki/CamStudio "wikilink") (デコードのみ)
  - CD+G
  - Chinese AVS video
  - Delphine Software International CIN video
  - [Cinepak](../Page/Cinepak.md "wikilink") (デコードのみ)
  - Cirrus Logic AccuPak
  - [Creative](https://ja.wikipedia.org/wiki/Creative "wikilink") YUV ([CYUV](https://ja.wikipedia.org/wiki/CYUV "wikilink"))
  - DFA
  - Dirac
  - Deluxe Paint Animation
  - [DNxHD](https://ja.wikipedia.org/wiki/DNxHD "wikilink")
  - [Duck](https://ja.wikipedia.org/wiki/On2_Technologies "wikilink") TrueMotion v1, v2 (デコードのみ)
  - [DV](../Page/DV_\(ビデオ規格\).md "wikilink")
  - Feeble Files/ScummVM DXA
  - Electronic Arts CMV video
  - Electronic Arts Madcow video
  - Electronic Arts TGV video
  - Electronic Arts TGQ video
  - Electronic Arts TQI video
  - Escape 124
  - FFmpeg video codec \#1
  - Flash Screen Video v1, v2
  - [FFV1](https://ja.wikipedia.org/wiki/FFV1 "wikilink")
  - [FLV1(Sorenson Spark)](../Page/Flash_Video.md "wikilink")
  - [Fraps](https://ja.wikipedia.org/wiki/Fraps "wikilink")（デコードのみ）
  - [H.261](../Page/H.261.md "wikilink")
  - [H.263](../Page/H.263.md "wikilink") / H.263-1996
  - H.263+ / H.263-1998 / H.263 version 2
  - [H.264](../Page/H.264.md "wikilink") / AVC / MPEG-4 AVC / MPEG-4 part 10 (デコードのみ、エンコードは[libx264を通して可能](https://ja.wikipedia.org/wiki/x264 "wikilink"))
  - H.264 / AVC / MPEG-4 AVC / MPEG-4 part 10 (VDPAU acceleration)
  - [Huffyuv](https://ja.wikipedia.org/wiki/Huffyuv "wikilink")/ffvhuff
  - HuffYUV FFmpeg variant
  - IBM Ultimotion
  - id Cinematic video
  - [id Software](https://ja.wikipedia.org/wiki/id_Software "wikilink") RoQ Video
  - IFF ILBM
  - IFF ByteRun1
  - Intel H.263
  - [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink") [Indeo](../Page/Indeo.md "wikilink")2, 3, 5 (デコードのみ)

<!-- end list -->

  - Interplay C93
  - Interplay MVE video
  - Karl Morton's video codec
  - Kega Game Video (KGV1)
  - Lagarith
  - LCL (LossLess Codec Library) MSZH
  - LCL (LossLess Codec Library) ZLIB
  - LOCO (デコードのみ)
  - lossless MJPEG
  - Microsoft RLE
  - [Microsoft Video 1](https://ja.wikipedia.org/wiki/Microsoft_Video_1 "wikilink")
  - Mimic (デコードのみ)
  - Miro VideoXL
  - [MJPEG](https://ja.wikipedia.org/wiki/MJPEG "wikilink") (Motion JPEG)
  - [MPEG-1](../Page/MPEG-1.md "wikilink")
  - MPEG-1/2 video XvMC (X-Video Motion Compensation)
  - MPEG-1/2 video (VDPAU acceleration)
  - [MPEG-2](../Page/MPEG-2.md "wikilink")/[H.262](https://ja.wikipedia.org/wiki/H.262 "wikilink")
  - [MPEG-4 Part 2](https://ja.wikipedia.org/wiki/MPEG-4_Part_2 "wikilink") (エンコードは別に[xvidcoreを利用可](../Page/Xvid.md "wikilink"))
  - [MS-MPEG4](https://ja.wikipedia.org/wiki/MS-MPEG4 "wikilink")v1/v2/v3
  - Nintendo Gamecube THP video
  - NuppelVideo/RTjpeg
  - [On2](https://ja.wikipedia.org/wiki/On2_Technologies "wikilink") [VP3](https://ja.wikipedia.org/wiki/On2VP3 "wikilink"), VP5, [VP6](https://ja.wikipedia.org/wiki/On2_VP6 "wikilink") (デコードのみ)
  - [VP8](https://ja.wikipedia.org/wiki/VP8 "wikilink")（デコードのみ、エンコードは別にlibvpxを通して可能）
  - planar RGB
  - Q-team QPEG
  - QuickTime 8BPS video
  - QuickTime Animation (RLE) video
  - QuickTime Graphics (SMC)
  - QuickTime video (RPZA)
  - R10K AJA Kona 10-bit RGB Codec
  - R210 Quicktime Uncompressed RGB 10-bit
  - Raw Video
  - [RealVideo](https://ja.wikipedia.org/wiki/RealVideo "wikilink") 1.0, 2.0
  - [RealVideo](https://ja.wikipedia.org/wiki/RealVideo "wikilink") 3.0, 4.0 (デコードのみ)
  - Renderware TXD (TeXture Dictionary)
  - RL2 video
  - [Sierra](../Page/Sierra.md "wikilink") [VMD](https://ja.wikipedia.org/wiki/Sierra_Video_and_Music_Data_File "wikilink") Video
  - [Smacker video](https://ja.wikipedia.org/wiki/Smacker_video "wikilink") (デコードのみ)
  - SMPTE [VC-1](../Page/VC-1.md "wikilink") (デコードのみ)
  - [Snow](../Page/Snow_\(コーデック\).md "wikilink")
  - Sony PlayStation MDEC (Motion DECoder)
  - [Sorenson](https://ja.wikipedia.org/wiki/Sorenson "wikilink") [SVQ1](https://ja.wikipedia.org/wiki/Sorenson_codec "wikilink")
  - [Sorenson](https://ja.wikipedia.org/wiki/Sorenson "wikilink") [SVQ3](https://ja.wikipedia.org/wiki/Sorenson_codec "wikilink") (デコードのみ)
  - Sunplus JPEG (SP5X)
  - TechSmith Screen Capture Codec
  - [Theora](../Page/Theora.md "wikilink") (デコードのみ、エンコードは別にlibtheoraを利用可)
  - Tiertex Limited SEQ video
  - V210 Quicktime Uncompressed 4:2:2 10-bit
  - [VMware](../Page/VMware.md "wikilink") [VMnc](https://ja.wikipedia.org/wiki/VMnc "wikilink") (デコードのみ)
  - [Westwood Studios](https://ja.wikipedia.org/wiki/Westwood_Studios "wikilink") VQA (デコードのみ)
  - [Windows Media Image](https://ja.wikipedia.org/wiki/Windows_Media_Image "wikilink") (デコードのみ)
  - [Windows Media Video](../Page/Windows_Media_Video.md "wikilink") 7, 8
  - [Windows Media Video](../Page/Windows_Media_Video.md "wikilink") 9 (デコードのみ)
  - [Wing Commander](https://ja.wikipedia.org/wiki/Wing_Commander_\(video_game\) "wikilink")/Xan Video (デコードのみ)
  - Winnov WNV1
  - YAMAHA SMAF
  - Psygnosis YOP Video
  - ZLIB
  - Zip Motion Blocks Video

## 実装しているオーディオコーデック

libavcodecは以下のフォーマットの音声のデコーダとエンコーダを含む\[5\]:

  - [8SVX](https://ja.wikipedia.org/wiki/8SVX "wikilink") (デコードのみ)
  - [AAC](https://ja.wikipedia.org/wiki/Advanced_Audio_Coding "wikilink")
  - [AC-3](../Page/ドルビーデジタル.md "wikilink")
  - [Apple Lossless](../Page/Apple_Lossless.md "wikilink")
  - [ATRAC3](https://ja.wikipedia.org/wiki/ATRAC3 "wikilink") (デコードのみ)
  - [Cook Codec](https://ja.wikipedia.org/wiki/Cook_Codec "wikilink") (デコードのみ)
  - [DTS](https://ja.wikipedia.org/wiki/デジタル・シアター・システムズ "wikilink") (デコードのみ)
  - [EA ADPCM](https://ja.wikipedia.org/wiki/SimCity_3000 "wikilink") (デコードのみ)
  - [E-AC-3](https://ja.wikipedia.org/wiki/E-AC-3 "wikilink") (デコードのみ)
  - [FLAC](../Page/FLAC.md "wikilink")
  - Intel Music Coder (デコードのみ)
  - [Meridian Lossless Packing](https://ja.wikipedia.org/wiki/Meridian_Lossless_Packing "wikilink") / [Dolby TrueHD](https://ja.wikipedia.org/wiki/Dolby_TrueHD "wikilink") (デコードのみ)
  - [Monkey's Audio](../Page/Monkey's_Audio.md "wikilink") (デコードのみ)
  - [MP2](https://ja.wikipedia.org/wiki/MP2 "wikilink")
  - [MP3](../Page/MP3.md "wikilink") (独自デコーダ、エンコードは[LAME](../Page/LAME.md "wikilink")を通して)
  - [MPEG-4 ALS](https://ja.wikipedia.org/wiki/MPEG-4_ALS "wikilink") (デコードのみ)
  - [Nellymoser Asao Codec](https://ja.wikipedia.org/wiki/Nellymoser_Asao_Codec "wikilink")
  - [QCELP](https://ja.wikipedia.org/wiki/QCELP "wikilink") (デコードのみ)
  - [QDM2](https://ja.wikipedia.org/wiki/QDesign "wikilink") (デコードのみ)
  - [RealAudio 1.0](https://ja.wikipedia.org/wiki/VSELP "wikilink") (デコードのみ)
  - [RealAudio 2.0](https://ja.wikipedia.org/wiki/LD-CELP "wikilink") (デコードのみ)
  - [Shorten](https://ja.wikipedia.org/wiki/Shorten "wikilink") (デコードのみ)
  - [Truespeech](https://ja.wikipedia.org/wiki/Truespeech "wikilink") (デコードのみ)
  - [TTA](../Page/TTA.md "wikilink") (デコードのみ)
  - [Vorbis](../Page/Vorbis.md "wikilink") (エンコードは別に[libvorbisencを利用可](../Page/Vorbis.md "wikilink"))
  - [WavPack](https://ja.wikipedia.org/wiki/WavPack "wikilink") (デコードのみ)
  - [Windows Media Audio](../Page/Windows_Media_Audio.md "wikilink") 1
  - [Windows Media Audio](../Page/Windows_Media_Audio.md "wikilink") 2

## libavcodecに依存するライブラリ

  - libavformat ([FFmpeg](../Page/FFmpeg.md "wikilink")の一部)
  - libgegl ([GEGL](https://ja.wikipedia.org/wiki/GEGL "wikilink")の一部。任意)
      - libgimp ([GIMP](../Page/GIMP.md "wikilink")の一部)
  - libmpcodecs ([MPlayer](../Page/MPlayer.md "wikilink")の一部)
      - libmpdemux ([MPlayer](../Page/MPlayer.md "wikilink")の一部)
  - libvlc ([VLC](https://ja.wikipedia.org/wiki/VLC "wikilink")の一部)

## libavcodecを使用しているアプリケーション

### 動画プレーヤ

  - [FFplay](../Page/FFmpeg.md "wikilink")
  - [GOM Player](../Page/GOM_Player.md "wikilink") (ライセンス問題あり)
  - [Media Player Classic](../Page/Media_Player_Classic.md "wikilink")
  - [Media Player Classic -Homecinema](../Page/Media_Player_Classic.md "wikilink")
  - [MPlayer](../Page/MPlayer.md "wikilink")
  - [PSPTube](https://ja.wikipedia.org/wiki/PSPTube "wikilink") - PSP用ネットワーク動画プレーヤ
  - [VLC](https://ja.wikipedia.org/wiki/VLC "wikilink")
  - [xine](https://ja.wikipedia.org/wiki/xine "wikilink")

### 音声プレーヤ

  - [Audacious](https://ja.wikipedia.org/wiki/Audacious "wikilink") (audacious-pluginsにwmaのコードだけを含む)
  - [Rockbox](../Page/Rockbox.md "wikilink") (FLACのコードだけを含む)
  - [XMMS2](https://ja.wikipedia.org/wiki/XMMS2 "wikilink")

### マルチメディアプレーヤ

  - [Gnash](https://ja.wikipedia.org/wiki/Gnash "wikilink")
  - [Moonlight](https://ja.wikipedia.org/wiki/Moonlight_\(runtime\) "wikilink")
  - [swfdec](https://ja.wikipedia.org/wiki/swfdec "wikilink")

### 動画編集

  - [Avidemux](https://ja.wikipedia.org/wiki/Avidemux "wikilink")
  - [Cinelerra](https://ja.wikipedia.org/wiki/Cinelerra "wikilink")
  - [Kdenlive](https://ja.wikipedia.org/wiki/Kdenlive "wikilink")
  - [Kino](https://ja.wikipedia.org/wiki/Kino "wikilink")

### 音声編集

  - [Audacity](../Page/Audacity.md "wikilink") (1.3.6以降)

### 動画変換

  - [FFmpeg](../Page/FFmpeg.md "wikilink")
  - [MEncoder](https://ja.wikipedia.org/wiki/MEncoder "wikilink")
  - [Transcode](https://ja.wikipedia.org/wiki/Transcode "wikilink")

### 音声変換

  - [BeSweet](https://ja.wikipedia.org/wiki/BeSweet "wikilink")

### グラフィックライブラリ

  - [GEGL](https://ja.wikipedia.org/wiki/GEGL "wikilink")

### 3Dグラフィック編集

  - [Blender](../Page/Blender.md "wikilink")

### VoIP

  - [Ekiga](../Page/Ekiga.md "wikilink")
  - [QuteCom](https://ja.wikipedia.org/wiki/QuteCom "wikilink")

### マルチメディアストリーミングサーバー

  - [FFserver](../Page/FFmpeg.md "wikilink")
  - [VLC](https://ja.wikipedia.org/wiki/VLC "wikilink")

### マルチメディアフレームワーク

  - [ac3encode](https://ja.wikipedia.org/wiki/ac3encode "wikilink") - DirectShow用AC3エンコーダ
  - [ffdshow](https://ja.wikipedia.org/wiki/ffdshow "wikilink") ([DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")フィルタとしてlibavcodecをラップし、ポストプロセスを追加してイメージの品質を改善する。一度インストールすると[Windows Media Player](../Page/Windows_Media_Player.md "wikilink")、[Media Player Classic](../Page/Media_Player_Classic.md "wikilink")、[Winamp](https://ja.wikipedia.org/wiki/Winamp "wikilink")、[Zoom PlayerなどのWindowsのDirectShowを使用する全ての動画プレーヤが自動的にこれを使うようになる](https://ja.wikipedia.org/wiki/Zoom_Player "wikilink"))
  - [ffdshow tryouts](https://ja.wikipedia.org/wiki/ffdshow_tryouts "wikilink")
  - [GStreamer](../Page/GStreamer.md "wikilink")
  - [Perian](https://ja.wikipedia.org/wiki/Perian "wikilink")

### メタデータ管理

  - [GNU libextractor](https://ja.wikipedia.org/wiki/GNU_libextractor "wikilink") (いくらかのlibavcodecのコードを含む)

### API ラッパー

  - FFmpeg-Perl - [Perl](../Page/Perl.md "wikilink")
  - ffmpeg-php - [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")
  - Jffmpeg - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
  - Xuggler - Java\[6\]

### その他

  - [AtGLas](https://ja.wikipedia.org/wiki/AtGLas "wikilink")
  - [avifile](https://ja.wikipedia.org/wiki/avifile "wikilink")
  - [Avview](https://ja.wikipedia.org/wiki/Avview "wikilink")
  - [bbplay](https://ja.wikipedia.org/wiki/bbplay "wikilink")
  - [BeOS FFmpeg decoders](https://ja.wikipedia.org/wiki/BeOS_FFmpeg_decoders "wikilink")
  - [BeOS HybridDivx](https://ja.wikipedia.org/wiki/BeOS_HybridDivx "wikilink")
  - [Chameleo](https://ja.wikipedia.org/wiki/Chameleo "wikilink")
  - [Chroma Player](https://ja.wikipedia.org/wiki/Chroma_Player "wikilink")
  - [chronictv](https://ja.wikipedia.org/wiki/chronictv "wikilink")
  - [CorePlayer](https://ja.wikipedia.org/wiki/CorePlayer "wikilink")
  - [D-Volution](https://ja.wikipedia.org/wiki/D-Volution "wikilink")
  - [DivXray](https://ja.wikipedia.org/wiki/DivXray "wikilink")
  - [DivXtoDVD](https://ja.wikipedia.org/wiki/DivXtoDVD "wikilink")
  - [Dr. Divx](https://ja.wikipedia.org/wiki/Dr._Divx "wikilink")
  - [DreaMule](https://ja.wikipedia.org/wiki/DreaMule "wikilink") (「SimpleVLC」と呼ばれるレイヤを使用)
  - [dvbcut](https://ja.wikipedia.org/wiki/dvbcut "wikilink")
  - [DVDFlick](https://ja.wikipedia.org/wiki/DVDFlick "wikilink")
  - [Easy VOB 2 DivX](https://ja.wikipedia.org/wiki/Easy_VOB_2_DivX "wikilink")
  - [ffmpeg2theora](https://ja.wikipedia.org/wiki/ffmpeg2theora "wikilink")
  - [FFMPEG for QT](https://ja.wikipedia.org/wiki/FFMPEG_for_QT "wikilink")
  - [FFmpegSource](https://ja.wikipedia.org/wiki/FFmpegSource "wikilink")
  - [ffmpegX for Mac OS X](https://ja.wikipedia.org/wiki/ffmpegX_for_Mac_OS_X "wikilink")
  - [ffmpegX Companion](https://ja.wikipedia.org/wiki/ffmpegX_Companion "wikilink")
  - [FFRecord](https://ja.wikipedia.org/wiki/FFRecord "wikilink")
  - [fftv](https://ja.wikipedia.org/wiki/fftv "wikilink")
  - [FFusion](https://ja.wikipedia.org/wiki/FFusion "wikilink") - Mac OS X用の代替コーデックスイート
  - [Fobs](https://ja.wikipedia.org/wiki/Fobs "wikilink")
  - [FreeJ](https://ja.wikipedia.org/wiki/FreeJ "wikilink")
  - [Frogger](http://frogger.rules.pl/)
  - [Gallery](http://gallery.sourceforge.net/)
  - [gmerlin](https://ja.wikipedia.org/wiki/gmerlin "wikilink")
  - [GPAC](https://ja.wikipedia.org/wiki/GPAC_Project_on_Advanced_Content "wikilink")
  - [HandBrake](../Page/HandBrake.md "wikilink")
  - [HTS (Home Theater System)](https://ja.wikipedia.org/wiki/HTS_\(Home_Theater_System\) "wikilink")
  - [Hyperion](https://ja.wikipedia.org/wiki/Hyperion "wikilink")
  - [ImTOO DVD Ripper](https://ja.wikipedia.org/wiki/ImTOO_DVD_Ripper "wikilink")
  - [Internet DJ Console](https://ja.wikipedia.org/wiki/Internet_DJ_Console "wikilink")
  - [K3b](../Page/K3b.md "wikilink")
  - [OpenCV](../Page/OpenCV.md "wikilink")
  - [PulseAudio](https://ja.wikipedia.org/wiki/PulseAudio "wikilink") - リサンプラのコードのみを含む\[7\]
  - [x264](https://ja.wikipedia.org/wiki/x264 "wikilink") - x264CLI(コマンドラインフロントエンド)の入力部に使用

## 外部リンク

  - [FFmpeg General Documantation - 2.Supported File Formats and Codecs](http://www.ffmpeg.org/general.html#SEC3)
  - [Libav General Documantation - 2.Supported File Formats and Codecs](http://libav.org/general.html#Supported-File-Formats-and-Codecs)

## 出典

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink")

1.  <http://www.afterdawn.com/glossary/terms/libavcodec.cfm>
2.  <http://gstreamer.freedesktop.org/modules/gst-ffmpeg.html>
3.  <http://packages.ubuntu.com/jaunty/gstreamer0.10-ffmpeg>
4.  <http://www.ffmpeg.org/general.html#SEC6>
5.  <http://www.ffmpeg.org/general.html#SEC7>
6.  <http://www.xuggle.com/xuggler>
7.  [/src/pulsecore/ffmpeg - PulseAudio - Trac](http://www.pulseaudio.org/browser/src/pulsecore/ffmpeg)