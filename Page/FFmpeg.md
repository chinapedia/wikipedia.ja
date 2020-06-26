> この記事は[FFmpeg](https://ja.wikipedia.org/wiki/FFmpeg)から翻訳されています。


**FFmpeg**（エフエフエムペグ）は[動画](../Page/動画.md "wikilink")と[音声](https://ja.wikipedia.org/wiki/音声 "wikilink")を記録・変換・再生するための[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である\[1\]。[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) 生まれであるが現在では[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")であり、[libavcodec](https://ja.wikipedia.org/wiki/libavcodec "wikilink")（動画/音声の[コーデック](../Page/コーデック.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")）、[libavformat](https://ja.wikipedia.org/wiki/libavformat "wikilink")（動画/音声のコンテナライブラリ）、[libswscale](https://ja.wikipedia.org/wiki/libswscale "wikilink")（色空間・サイズ変換ライブラリ）、[libavfilter](https://ja.wikipedia.org/wiki/libavfilter "wikilink")（動画のフィルタリングライブラリ）などを含む。[ライセンス](../Page/ライセンス.md "wikilink")は[コンパイル時のオプションにより](../Page/コンパイラ.md "wikilink")[LGPLか](../Page/GNU_Lesser_General_Public_License.md "wikilink")[GPLに決定される](../Page/GNU_General_Public_License.md "wikilink")。[コマンドラインから使用することができる](../Page/コマンドラインインタプリタ.md "wikilink")。対応[コーデック](../Page/コーデック.md "wikilink")が多く、多彩なオプションを使用可能なため、幅広く利用されている。

## 解説

FFmpegは、単体では[GUIを持たないツールで](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[UNIX](../Page/UNIX.md "wikilink")[コマンドのように振る舞う](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")。その為、対話式[アプリケーションとして使用される場合](../Page/アプリケーションソフトウェア.md "wikilink")、[フロントエンド](../Page/フロントエンド.md "wikilink")を用いる事も多い。コマンドラインから実行する[CUIとして配布されているのは](../Page/キャラクタユーザインタフェース.md "wikilink")、ユーザが必要とすればフロントエンドを利用でき、スクリプトなどのバッチ処理を行う際に呼び出す事もできるという利点からである。また、[FFserver](https://ja.wikipedia.org/wiki/FFserver "wikilink")と組み合わせる事により、[ファイルシステム](../Page/ファイルシステム.md "wikilink")や[デバイスファイル](../Page/デバイスファイル.md "wikilink")と[ストリーミング](../Page/ストリーミング.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")間のフィルタとしても動作する。

[2011年](../Page/2011年.md "wikilink")[3月13日](../Page/3月13日.md "wikilink")にFFmpegの開発は、開発体制の対立からffmpeg.orgとlibav.orgに分裂した。どちらもffmpegというソフトウェアをリリースしているが、側はavconvに名称を切り替える作業を進めている。この分裂に伴い、[Debian](../Page/Debian.md "wikilink")\[2\]、[Ubuntu](../Page/Ubuntu.md "wikilink")\[3\] 11.04、[Gentoo LinuxはLibav側を採用した](../Page/Gentoo_Linux.md "wikilink")。

[2015年](../Page/2015年.md "wikilink")7月にDebianはセキュリティ問題への対応姿勢からLibavを排除し、FFmpeg採用に戻った。UbuntuもFFmpeg採用に戻っている\[4\]。

## サポートしているファイル形式

  - 4xm
  - 8088flex TMV
  - Adobe Filmstrip
  - Audio IFF ([AIFF](../Page/AIFF.md "wikilink") CD-ROM XA ADPCMを含む)
  - American Laser Games MM
  - [3GPP](../Page/3GPP.md "wikilink") AMR
  - Apple HTTP Live Streaming
  - [ASF](../Page/Advanced_Systems_Format.md "wikilink")
  - [AVI](../Page/Audio_Video_Interleave.md "wikilink")
  - AVISynth
  - AVS
  - Beam Software SIFF
  - Bethesda Softworks VID
  - Bink
  - Bitmap Brothers JV
  - Brute Force & Ignorance
  - BWF
  - Interplay C93
  - Delphine Software International CIN
  - CD+G
  - Core Audio Format
  - CRC testing format
  - Creative Voice
  - CRYO APC
  - D-Cinema audio
  - Deluxe Paint Animation
  - DFA
  - DV video
  - DXA
  - Electronic Arts cdata
  - Electronic Arts Multimedia
  - FFM (FFserver live feed)
  - [Flash](../Page/Adobe_Flash.md "wikilink") (SWF)
  - Flash 9 (AVM2)
  - FLI/FLC/FLX animation
  - [Flash Video](../Page/Flash_Video.md "wikilink") (FLV)
  - framecrc testing format
  - FunCom ISS
  - [GIF](https://ja.wikipedia.org/wiki/GIF "wikilink") アニメーション
  - GXF
  - id Quake II CIN video
  - id RoQ
  - IEC61937 encapsulation
  - IFF
  - Interplay MVE
  - IV8
  - IVF (On2)
  - LMLM4
  - LOAS
  - LXF
  - [Matroska](../Page/Matroska.md "wikilink")
  - Matroska audio
  - FFmpeg metadata
  - MAXIS XA
  - MD Studio
  - Mobotix .mxg
  - [Monkey's Audio](../Page/Monkey's_Audio.md "wikilink")
  - Motion Pixels MVI

<!-- end list -->

  - MOV/[QuickTime](../Page/QuickTime.md "wikilink")/[MP4](../Page/MP4.md "wikilink")
  - MP2
  - [MP3](../Page/MP3.md "wikilink")
  - [MPEG-1](../Page/MPEG-1.md "wikilink") System
  - MPEG-PS (program stream)
  - MPEG-TS (transport stream)
  - [MPEG-4](../Page/MPEG-4.md "wikilink")
  - [MIME](https://ja.wikipedia.org/wiki/MIME "wikilink") マルチパート [JPEG](../Page/JPEG.md "wikilink")
  - MSN TCP webcam
  - MTV
  - [Musepack](../Page/Musepack.md "wikilink")
  - Musepack SV8
  - [Material eXchange Format](https://ja.wikipedia.org/wiki/Material_eXchange_Format "wikilink") (MXF)
  - Material eXchange Format (MXF), D-10 Mapping
  - NC camera feed
  - NTT [TwinVQ](https://ja.wikipedia.org/wiki/TwinVQ "wikilink") (VQF)
  - Nullsoft Streaming Video
  - NuppelVideo
  - NUT
  - [Ogg](../Page/Ogg.md "wikilink")
  - Playstation Portable PMP
  - TechnoTrend PVA
  - QCP
  - raw ADTS ([AAC](../Page/AAC.md "wikilink"))
  - raw [AC-3](https://ja.wikipedia.org/wiki/AC-3 "wikilink")
  - raw Chinese AVS video
  - raw CRI ADX
  - raw [Dirac](https://ja.wikipedia.org/wiki/Dirac "wikilink")
  - raw DNxHD
  - raw DTS
  - raw E-AC-3
  - raw [FLAC](../Page/FLAC.md "wikilink")
  - raw [GSM](https://ja.wikipedia.org/wiki/GSM "wikilink")
  - raw [H.261](../Page/H.261.md "wikilink")
  - raw [H.263](../Page/H.263.md "wikilink")
  - raw [H.264](../Page/H.264.md "wikilink")
  - raw Ingenient MJPEG
  - raw [MJPEG](https://ja.wikipedia.org/wiki/MJPEG "wikilink")
  - raw MLP
  - raw [MPEG](https://ja.wikipedia.org/wiki/MPEG "wikilink")
  - raw [MPEG-1](../Page/MPEG-1.md "wikilink")
  - raw [MPEG-2](../Page/MPEG-2.md "wikilink")
  - raw [MPEG-4](../Page/MPEG-4.md "wikilink")
  - raw NULL
  - raw video
  - raw id RoQ
  - raw Shorten
  - raw [TrueHD](https://ja.wikipedia.org/wiki/ドルビーTrueHD "wikilink")
  - raw [VC-1](../Page/VC-1.md "wikilink")
  - raw PCM [A-law](https://ja.wikipedia.org/wiki/A-law "wikilink")
  - raw PCM [mu-law](https://ja.wikipedia.org/wiki/mu-law "wikilink")
  - raw [PCM](https://ja.wikipedia.org/wiki/PCM "wikilink")
      - [整数](../Page/整数.md "wikilink"): 符号付きまたは符号なし、ビット数は8、16、24、32ビット、[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")はリトルエンディアンとビックエンディアン
      - [浮動小数点](https://ja.wikipedia.org/wiki/浮動小数点 "wikilink"): [32ビット](../Page/32ビット.md "wikilink")または[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")エンディアンはリトルエンディアンとビックエンディアン

<!-- end list -->

  - RDT
  - REDCODE R3D
  - RealMedia
  - Redirector
  - Renderware TeXture Dictionary
  - RL2
  - RPL/ARMovie
  - Lego [Mindstorms](https://ja.wikipedia.org/wiki/マインドストーム "wikilink") RSO
  - [RTMP](https://ja.wikipedia.org/wiki/Real_Time_Messaging_Protocol "wikilink")
  - [RTP](../Page/Real-time_Transport_Protocol.md "wikilink")
  - [RTSP](../Page/Real_Time_Streaming_Protocol.md "wikilink")
  - SAP
  - [SDP](../Page/Session_Description_Protocol.md "wikilink")
  - Sega FILM/CPK
  - Sierra SOL
  - Sierra VMD
  - Smacker
  - Sony [OpenMG](https://ja.wikipedia.org/wiki/OpenMG "wikilink") (OMA)
  - Sony PlayStation STR
  - Sony Wave64 (W64)
  - SoX native format
  - [SUN AU format](../Page/Sunオーディオファイル.md "wikilink")
  - [テキストファイル](../Page/テキストファイル.md "wikilink")
  - THP
  - Tiertex Limited SEQ
  - True Audio
  - [VC-1](../Page/VC-1.md "wikilink") test bitstream
  - [WAV](../Page/WAV.md "wikilink")
  - [WavPack](https://ja.wikipedia.org/wiki/WavPack "wikilink")
  - [WebM](https://ja.wikipedia.org/wiki/WebM "wikilink")
  - Windows Televison (WTV)
  - Wing Commander III movie
  - Westwood Studios audio
  - Westwood Studios VQA
  - XMV
  - xWMA
  - YUV4MPEG pipe
  - Psygnosis YOP

## サポートしている画像形式

  - [AV1](https://ja.wikipedia.org/wiki/AV1 "wikilink")
  - GIF parser
  - hcom
  - [Huffyuv](https://ja.wikipedia.org/wiki/Huffyuv "wikilink")
  - ARBC
  - [HEVC](https://ja.wikipedia.org/wiki/HEVC "wikilink")
  - agm
  - lscr
  - VP4

<!-- end list -->

  - .Y.U.V
  - [アニメーションGIF](https://ja.wikipedia.org/wiki/アニメーションGIF "wikilink")
  - [BMP](../Page/Windows_bitmap.md "wikilink")
  - [DPX](https://ja.wikipedia.org/wiki/DPX "wikilink")
  - [JPEG](../Page/JPEG.md "wikilink")
  - JPEG 2000
  - JPEG-LS

<!-- end list -->

  - LJPEG
  - PAM
  - [PBM](https://ja.wikipedia.org/wiki/PNM_\(画像フォーマット\) "wikilink")
  - PCX
  - [PGM](https://ja.wikipedia.org/wiki/PNM_\(画像フォーマット\) "wikilink")
  - PGMYUV
  - [PIC](../Page/PIC_\(画像圧縮\).md "wikilink")

<!-- end list -->

  - [PNG](../Page/Portable_Network_Graphics.md "wikilink")

  - [PPM](https://ja.wikipedia.org/wiki/PNM_\(画像フォーマット\) "wikilink")

  - PTX

  -
  - Sun Rasterfile

  - [TIFF](../Page/Tagged_Image_File_Format.md "wikilink")

  - Truevision Targa([TGA](../Page/TGA.md "wikilink"))

## サポートしているコーデック

[libavcodec](https://ja.wikipedia.org/wiki/libavcodec "wikilink")を参照。

## サポートしているプロトコル

  - [TCP](../Page/Transmission_Control_Protocol.md "wikilink")
  - [UDP](../Page/User_Datagram_Protocol.md "wikilink")
  - [HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")
  - [RTP](../Page/Real-time_Transport_Protocol.md "wikilink")
  - [RTSP](../Page/Real_Time_Streaming_Protocol.md "wikilink")
  - RealMedia RTSP/[RDT](https://ja.wikipedia.org/wiki/Real_Data_Transport "wikilink")
  - [RTMP](https://ja.wikipedia.org/wiki/Real_Time_Messaging_Protocol "wikilink")
  - RTMPT, RTMPE, RTMPTE, RTMPS (librtmp経由)
  - [SDP](../Page/Session_Description_Protocol.md "wikilink")
  - [Gopher](https://ja.wikipedia.org/wiki/Gopher "wikilink")
  - [MMS over TCP](https://ja.wikipedia.org/wiki/Microsoft_Media_Server "wikilink")

## サポートしている入出力デバイス

  - Unix
      - [OSS](https://ja.wikipedia.org/wiki/Open_Sound_System "wikilink")
      - [JACK](https://ja.wikipedia.org/wiki/JACK_Audio_Connection_Kit "wikilink")
      - [X11](https://ja.wikipedia.org/wiki/X11 "wikilink") grabbing
      - [dv1394](https://ja.wikipedia.org/wiki/dv1394 "wikilink")
      - bktrドライバ
      - Linux
          - [ALSA](https://ja.wikipedia.org/wiki/ALSA "wikilink")

          -
          - [Video4Linux2](https://ja.wikipedia.org/wiki/Video4Linux2 "wikilink")

          - [libdc1394](https://ja.wikipedia.org/wiki/libdc1394 "wikilink") (IEEE 1394)
  - Windows
      - [VfW](https://ja.wikipedia.org/wiki/VfW "wikilink")キャプチャ

## オプション

FFmpegでは数多くのオプションを利用することができる。それらはffmpegのバージョンによって差異があるため、利用前にオプションやコーデックの表記を確認することが望ましい。オプションは `ffmpeg -h` で表示できる。また、コーデック名等は `ffmpeg -formats` や `ffmpeg -codecs` で表示できる。（ *コーデック名は下記注意事項参照* ）

一般的なオプション等の例を以下に挙げる。

### メインオプション

  - \-i 入力ファイル名を設定する。
  - \-f 出力フォーマットの指定。
  - \-y 出力するファイル名と同じ名前のファイルが出力先にある場合に上書する。
  - \-fs 指定したファイルサイズになったら変換を終了する。
  - \-ss 指定した時間から変換を開始する。
  - \-title タイトルを設定する。
  - \-timestamp タイムスタンプを設定する。
  - \-vsync フレームをカットしたり加えたりして音声に動画を同期させる。

### ビデオオプション

  - \-b 動画部分のビットレートを設定、初期設定は200kbps。（ *単位は下記注意事項参照* ）
  - \-r フレームレートの設定 初期設定は25
  - \-s 動画のサイズを横×縦で設定
  - \-aspect アスペクト比の設定
  - \-vn ビデオを無効にする。音声部分のみのエンコードなどに使用する。
  - \-vcodec ビデオコーデックを設定　設定しない場合は入力ファイルと同じコーデックを使用する。
  - \-pix_fmt ピクセルフォーマット設定。例えば "-vcodec libx264" 等において[QuickTime](../Page/QuickTime.md "wikilink")、[QTKit](https://ja.wikipedia.org/wiki/QTKit "wikilink")、[AVFoundation](https://ja.wikipedia.org/wiki/AVFoundation "wikilink") ([AVKit](https://ja.wikipedia.org/wiki/AVKit "wikilink")) 互換にするには "-pix_fmt yuv420p" も合わせて指定。

### オーディオオプション

  - \-ab オーディオの全チャンネル合計（）のビットレートを設定する。（ *単位は下記注意事項参照* ）
  - \-ar サンプリング周波数を設定する。
  - \-ac 音声のチャンネル数を設定する。
  - \-acodec 音声コーデックを設定する。設定しない場合は動画同様入力されたファイルと同じコーデックを使用する。
  - \-an 音声を無効にする。ビデオ部分のみのエンコードなどに使用する。
  - \-vol 通常の音量を256として音量を設定する。(2倍の音量にしたい時は512を指定する。)

### 注意事項

  - \-bや-abオプションでビットレートを指定する場合、ffmpegのバージョンによってkbpsの場合と、bpsの場合があるので注意が必要である。（ffmpeg -hでヘルプメッセージを表示させて単位を確認するとよい）
      - たとえば、単位がbpsの場合で64kbpsのビットレートを指定する場合は『 -ab 64k 』と指定し、単位がkbpsの場合は『 -ab 64 』と指定する。ビットレートの計算では一般的にk=1000であり1024ではない。

<!-- end list -->

  - \-acodecや-vcodecで指定するコーデック名は、ffmpegのバージョンによって違うことがある。たとえば、AACコーデックの場合、aacと指定する場合と、libfaacと指定する場合がある。また、デコードのみやエンコードのみできるコーデックもあるため、必ず `ffmpeg -formats` や `ffmpeg -codecs` で指定するコーデックが機能するか確認すべきである。
  - FFmpeg と Libav の分裂に伴い、Libav 側は、コマンドラインツールとして、ffmpeg に代わる物として、引数などを（互換性なく）整理した avconv を2011年現在、開発中。各種 ff という接頭辞で始まるツールも av という名称に切り替えた。

## 使用例

引数が異なる場合、FFmpeg.orgのffmpegとLibavのavconv両方併記する。なお、Libavのffmpegは従来通りの引数が使える。

  - ヘルプの表示

`ffmpeg -h`

  - 対応形式の確認

`# ファイル形式 (コンテナ/フォーマット/スプリッター)`
`ffmpeg -formats`

`# コーデック形式 (映像や音声の形式/圧縮アルゴリズム)`
`ffmpeg -codecs`

`# プロトコル形式 (スキーマも含む)`
`ffmpeg -protocols`

  - 動画をMPEG-4/AVC形式に変換する例 (ビットレート固定)

`avconv -i inputfile -c:v libx264 -c:a libfaac -b:v 256k -b:a 64k outputfile.mp4`
`ffmpeg -i inputfile -f mp4 -vcodec libx264 -acodec libfaac -vb 256k -ab 64k outputfile.mp4`

`# -f の後に変換後のファイル形式、-acodec の後に変換後の音声コーデック、-vcodec の後に変換後の動画コーデックを指定する。`
`# -vb は変換後の映像のビットレート(ビット/秒)、-ab は変換後の音声のビットレート(ビット/秒)を指定する。`

  - 動画をMPEG-4/AVC形式に変換する例 (品質固定)

`avconv -i inputfile -c:v libx264 -c:a libfaac -cqp 23 -aq 100 outputfile.mp4`
`ffmpeg -i inputfile -f mp4 -vcodec libx264 -acodec libfaac -cqp 23 -aq 100 outputfile.mp4`

`# ビットレートを指定する代わりに品質を指定することができる。映像は cqp 、音楽は aq となる。`
`# 品質指定は cqp の場合、値が小さいほど品質が高いことを意味する。aq の場合、値が大きいほど品質が高いことを意味する。`
`# 値の意味は変換後のコーデックによるので注意。`

  - 音楽をAACに変換する例

`avconv -i inputfile -vn -c:a libfaac -b:a 128k outputfile.aac`
`ffmpeg -i inputfile -f aac -vn -acodec libfaac -ab 128k outputfile.aac`

`# -vcodec の代わりに -vn を使うことで変換後に映像を入れないという意味になる。同様に、-acodec の代わりに -an を使うことで音声を消すことも可能である。`

  - MP4形式の動画から再エンコード無しでFLV形式に変換する例

`avconv -i inputfile.mp4 -c copy outputfile.flv`
`ffmpeg -i inputfile.mp4 -vcodec copy -acodec copy outputfile.flv`

`# 変換後のフォーマットによっては、そのフォーマットの仕様の制限やFFmpegが未対応であることなどにより変換前のコーデックが入れられないことがある。`
`# また、-vcodec copy を -vn にすることによって、再エンコード無しで音楽だけにすることが出来る。`

  - RTSPサーバーからMP4動画を保存する例

`avconv -i `<rtsp://example.com/inputfile.mp4>` -c copy outputfile.mp4`
`ffmpeg -i `<rtsp://example.com/inputfile.mp4>` -vcodec copy -acodec copy -scodec copy outputfile.mp4`

`# 入力ファイルに直接URLを入れることができる。`

  - RTSPサーバーに動画を送信する例

`avconv -re -i inputfile -f rtsp -c:v libx264 -c:a libfaac -b:v 256k -b:a 64k `<rtsp://example.com/outputfile.mp4>
`ffmpeg -re -i inputfile -f rtsp -vcodec libx264 -acodec libfaac -vb 256k -ab 64k `<rtsp://example.com/outputfile.mp4>

`# 出力ファイルにも直接URLを入れることができる。-re を付けると出力速度がリアルタイムになるように調整する。`

  - サーバーとして動作させる例

`# ffserver.conf を適切に編集してから以下を実行。`
`ffserver &`
`ffmpeg -i inputfile `<http://127.0.0.1:8090/feed.ffm>

  - DVDのVOBファイルを、VideoCD形式のMPEG-1ファイルに変換する例

`avconv -i inputfile.vob -f mpeg -c:v mpeg1video -c:a mp2 -b:v 1152k -b:a 128k -s 352x240 outputfile.mpg`
`ffmpeg -i inputfile.vob -f mpeg -vcodec mpeg1video -acodec mp2 -vb 1152k -ab 128k -s 352x240 outputfile.mpg`

  - 動画を[東芝](../Page/東芝.md "wikilink")の[ハードディスクレコーダー](https://ja.wikipedia.org/wiki/ハードディスクレコーダー "wikilink")、[レグザ](../Page/レグザ.md "wikilink")が認識できるMPEG2形式に変換する例

`ffmpeg -i inputfile -target ntsc-svcd -ab 128k -aspect 4:3 -s 720x480 outputfile.mpg`

  - 複数のAVIの動画ファイルを結合する例（この例では、中間処理として、一度AVIファイルをMPEG-1ファイルに変換する必要がある(MPEG-1, MPEG-2 PS, DVも連結可能)）

`ffmpeg -i input1.avi -sameq inputfile_01.mpg`
`ffmpeg -i input2.avi -sameq inputfile_02.mpg`
`cat inputfile_01.mpg inputfile_02.mpg > inputfile_all.mpg`
`ffmpeg -i inputfile_all.mpg -sameq outputfile.avi`

なお、concatスキーマ(concat:input.avi.part1|input.avi.part2)はストリームの物理的な結合のみ行うため、この場合は使えない。

## 入手方法

公式サイトでは、コンパイル済みのバイナリは配布されていないため、自分の環境に合わせてソースコードを[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")することもできるが、 次のような手法でバイナリを入手することもできる。

### Linux

  - [RHEL](../Page/Red_Hat_Enterprise_Linux.md "wikilink"), [CentOS](../Page/CentOS.md "wikilink"), [Fedora](../Page/Fedora.md "wikilink")

RPMForge[1](https://rpmrepo.org/RPMforge)、Livna\[[http://rpm.livna.org/rlowiki/\]等のリポジトリを用いて](http://rpm.livna.org/rlowiki/%5D等のリポジトリを用いて)、[yumコマンド等でインストールできる](https://ja.wikipedia.org/wiki/Yellow_dog_Updater,_Modified "wikilink")

`yum --enablerepo=rpmforge install ffmpeg`

  - [Debian](../Page/Debian.md "wikilink"), [Ubuntu](../Page/Ubuntu.md "wikilink")など、APTがインストールされた環境

[apt installコマンドを用いて](https://ja.wikipedia.org/wiki/APT#追加・ダウンロード "wikilink")、ディストリビュージョンのリポジトリに含まれているパッケージからインストールする(root権限必要)

`sudo apt install ffmpeg  `

### FreeBSD

portsツリーに含まれており、該当ディレクトリに移動してmake installするかpkg_addコマンドでバイナリパッケージを導入する。

### macOS

<http://www.ffmpegx.com/> にて[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")用のffmpegXが配布されている。

### Windows

  - ffmpeg.org - <http://ffmpeg.zeranoe.com/builds/> にて[Windows版のバイナリが配布されている](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。
  - libav.org - <http://win32.libav.org/> にて配布している。

## FFmpegを利用・サポートしているアプリケーション

  - エンコーダ
      - [MEncoder](https://ja.wikipedia.org/wiki/MEncoder "wikilink")
      - [HandBrake](../Page/HandBrake.md "wikilink")
      - [MediaCoder](../Page/MediaCoder.md "wikilink")
      - [携帯動画変換君](../Page/携帯動画変換君.md "wikilink")
      - [WinFF](https://ja.wikipedia.org/wiki/WinFF "wikilink")
  - 動画再生
      - [MPlayer](../Page/MPlayer.md "wikilink")
      - [VLC](../Page/VLCメディアプレーヤー.md "wikilink")
      - [Xine](../Page/Xine.md "wikilink")
  - コーデック
      - [ffdshow](https://ja.wikipedia.org/wiki/ffdshow "wikilink")
      - [GStreamer](../Page/GStreamer.md "wikilink") FFmpeg plug-in
      - [Perian](https://ja.wikipedia.org/wiki/Perian "wikilink")
      - [Bellagio OpenMAX IL](https://ja.wikipedia.org/wiki/Bellagio_OpenMAX_IL "wikilink") - [STマイクロエレクトロニクス](../Page/STマイクロエレクトロニクス.md "wikilink")と[ノキア](../Page/ノキア.md "wikilink")によって開発されている[オープンソース](../Page/オープンソース.md "wikilink")の実装
      - FFmpegInterop - Microsoftによって開発されているMediaStreamSource実装
  - [3D](../Page/3D.md "wikilink")描画
      - [Blender](../Page/Blender.md "wikilink")
  - [マルチメディアプレーヤ](https://ja.wikipedia.org/wiki/マルチメディアプレーヤ "wikilink")
      - [Gnash](https://ja.wikipedia.org/wiki/Gnash "wikilink") - オープンソースの[フラッシュプレーヤー](https://ja.wikipedia.org/wiki/フラッシュプレーヤー "wikilink")
      - [swfdec](https://ja.wikipedia.org/wiki/swfdec "wikilink") - オープンソースのフラッシュプレーヤー
      - [Moonlight](https://ja.wikipedia.org/wiki/Moonlight "wikilink") - [マイクロソフト](../Page/マイクロソフト.md "wikilink")が支援して[ノベルが開発するオープンソースの](../Page/ノベル_\(企業\).md "wikilink")[Silverlight](https://ja.wikipedia.org/wiki/Silverlight "wikilink")代替実装
  - [動画編集](https://ja.wikipedia.org/wiki/動画編集ソフトウェア "wikilink")
      - [Avidemux](https://ja.wikipedia.org/wiki/Avidemux "wikilink")
      - [Kdenlive](https://ja.wikipedia.org/wiki/Kdenlive "wikilink")
      - [Jahshaka](../Page/Jahshaka.md "wikilink")
  - 音声編集
      - [Audacity](../Page/Audacity.md "wikilink")(1.3.6以降)
  - [VoIP](../Page/VoIP.md "wikilink")
      - [Ekiga](../Page/Ekiga.md "wikilink")
  - [構内交換機](https://ja.wikipedia.org/wiki/構内交換機 "wikilink") (PBX)
      - [Asterisk](../Page/Asterisk_\(PBX\).md "wikilink")
  - [画像処理](https://ja.wikipedia.org/wiki/画像処理ソフトウェア "wikilink")
      - [OpenCV](../Page/OpenCV.md "wikilink") - [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")によって開発された[コンピュータビジョン](../Page/コンピュータビジョン.md "wikilink")向けライブラリ。
      - [ImageMagick](../Page/ImageMagick.md "wikilink") - [MPEG-2](../Page/MPEG-2.md "wikilink")へ出力する際に使用する。
  - [ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")
      - [Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")\[5\] - HTML5のvideoタグに使用している。また、Chromeをベースにしたメディアプレイヤーを作るという計画がある。
  - 動画処理
      - [Ingex](https://ja.wikipedia.org/wiki/:en:Ingex "wikilink") - [BBC](../Page/英国放送協会.md "wikilink")（英国放送協会）リサーチ・アンド・デベロップメントが開発しBBCが使用している\[6\]\[7\]、オープンソースのテレビジョンプロダクション向け総合ソフトウェア
  - ラッパー
      - [JavaCV](http://code.google.com/p/javacv/) - [OpenCV](../Page/OpenCV.md "wikilink") の [Java](https://ja.wikipedia.org/wiki/Java "wikilink") ラッパーだが、FFmpeg のラッパーも含む

FFmpegに含まれるライブラリ群は多数のマルチメディアアプリケーションにより利用されている。また、[Palmのスマートフォン](../Page/パーム_\(企業\).md "wikilink")([Palm WebOS](https://ja.wikipedia.org/wiki/Palm_WebOS "wikilink")\[8\])や[ソニー](../Page/ソニー.md "wikilink")の[ブルーレイプレーヤ](../Page/Blu-ray_Disc.md "wikilink")(BDP-S1\[9\]、BDP-S1E/BDP-S300/BDP-S280\[10\]、BDP-S500/BDP-S2000ES\[11\])などのデバイスにも利用されている。

## 音ズレ問題

音ズレの原因は大きく分けて以下がある。

  - フレームレート
  - 復号タイムスタンプ (DTS)/表示タイムスタンプ (PTS)
  - A/V Sync
  - ディレイ

FFmpegにおいては、フレームレートは内部的に分数を用いて処理をしているためフレームレートによる音ズレが起こることは少ない。ただし小数でフレームレートを保存するコンテナも存在するため、限界もある。FFmpegのライブラリを使用する場合に、分数を小数に直してから処理すると音ズレを起こす場合がある。

コンテナの実装においてDTSをPTSに又はDTSにPTSを代入した場合や、FFmpegのライブラリを利用したアプリケーションにおいてPTSとDTSを正しく扱わなかった場合などに音ズレを伴う問題が起きる場合がある。また、負のPTSや負のDTSを使用している場合において問題が起きる場合がある。

ディレイの問題は、遅延フレーム、エンコードに必要な無音区間の挿入、デコードに必要的に出力される無音サンプルなどによって起こる。一部のコンテナやその実装においては、ディレイはタグなどのメタデータによって打ち消す。コンテナがディレイを打ち消す方法を提供しない場合は、映像/音声データの方を調節するしかない。一部独自拡張のタグにディレイ情報を埋め込むエンコーダ（LAMEのLAMEタグやiTunesのiTunSMPBなど）も存在し、様々なソフトウェア・ハードウェアが相性問題を抱えている。FFmpegはこれらの幾つかにまだ対応していない。

また、変換前の動画を出力したソフトウェア・ハードウェアや変換後の動画を処理するソフトウェア・ハードウェアのバグや仕様によって問題が起こることも多い。変換前の動画にバグがある場合、-bugオプションを使って回避できる場合がある。

## 出典

<references/>

## 関連項目

  - [オープンソースのコーデックとコンテナフォーマット](https://ja.wikipedia.org/wiki/オープンソースのコーデックとコンテナフォーマット "wikilink")
  - [KMPlayer](../Page/KMPlayer.md "wikilink")
  - [ffvp6](https://ja.wikipedia.org/wiki/ffvp6 "wikilink")

## 外部リンク

  - FFmpeg
      - [FFmpeg公式サイト](http://ffmpeg.org/)
      - [FFmpeg Documentation](http://ffmpeg.org/documentation.html)
          -
<!-- end list -->

  - Libav
      - [Libav公式サイト](http://libav.org/)
      - [Libav Documentation](http://libav.org/documentation.html)
          - [fixedpoint.jp - FFmpeg](http://fixedpoint.jp/ffmpeg/) - 日本語訳

[Category:マルチメディアソフトウェア](https://ja.wikipedia.org/wiki/Category:マルチメディアソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  A complete, cross-platform solution to record, convert and stream audio and video.\> <http://www.ffmpeg.org/>
2.  [transition: Libav 0.7](http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=624807)
3.  [Ubuntu Release Management: Transition: "libav"](http://people.canonical.com/~ubuntu-archive/transitions/libav.html)
4.
5.  [whatwg MPEG-1 subset proposal for HTML5 video codec](http://lists.whatwg.org/pipermail/whatwg-whatwg.org/2009-May/020001.html)
6.  [Research White Paper - WHP 155](http://downloads.bbc.co.uk/rd/pubs/whp/whp-pdf-files/WHP155.pdf)
7.  [BBC R\&D - Automated tapeless production - home page](http://www.bbc.co.uk/rd/projects/tapeless-production/)
8.  [Open Source Packages](http://opensource.palm.com/packages.html)
9.  [Model/Module : BDP-S1](http://www.sony.net/Products/Linux/Video/BDP-S1.html)
10. [Model/Module : BDP-S1E/BDP-S300/BDP-S280](http://www.sony.net/Products/Linux/Video/BDP-S1E.html)
11. [Model/Module : BDP-S500/BDP-S2000ES](http://www.sony.net/Products/Linux/Video/BDP-S500.html)