> この記事は[VLCメディアプレーヤー](https://ja.wikipedia.org/wiki/VLCメディアプレーヤー)から翻訳されています。


**VLCメディアプレーヤー** (VLC media player, **V**ideo**L**AN **C**lient) は、[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")で動作する[メディアプレーヤー](../Page/メディアプレーヤー.md "wikilink")である。非常に多くのメディアファイル用[コーデック](../Page/コーデック.md "wikilink")が内蔵されており、動画ファイルや音声ファイルなど多くのメディアファイルを再生、表示することができる。[GPL下で公開されている](../Page/GNU_General_Public_License.md "wikilink")[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。

## 概要

もともとは、フランスの名門校である[エコール・セントラル・パリ](https://ja.wikipedia.org/wiki/エコール・セントラル・パリ "wikilink")の学生らによって、[VideoLAN](https://ja.wikipedia.org/wiki/VideoLAN "wikilink")プロジェクトの一部として開発され、Video LAN Clientの頭文字をとってVLCと名づけられた。[コーデック](../Page/コーデック.md "wikilink")を内蔵し、[DVD-Video](../Page/DVD-Video.md "wikilink")、[ビデオCD](../Page/ビデオCD.md "wikilink")の他、さまざまな[ストリーミング](../Page/ストリーミング.md "wikilink")[プロトコル](../Page/プロトコル.md "wikilink")や[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")をサポートしている。広帯域ネットワーク上の[IPv4](../Page/IPv4.md "wikilink")ないし[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")における[ユニキャスト](https://ja.wikipedia.org/wiki/ユニキャスト "wikilink")、[マルチキャスト](../Page/マルチキャスト.md "wikilink")のストリームの[サーバ](../Page/サーバ.md "wikilink")としても使われる。内蔵されているのは[FFmpeg](../Page/FFmpeg.md "wikilink")プロジェクトのlibavcodecコーデックライブラリである。暗号化されたDVD-Videoの再生を扱うためには、[libdvdcss](https://ja.wikipedia.org/wiki/libdvdcss "wikilink")DVD暗号復文ライブラリを用いている。

## 特徴

対応するコーデックの多さが、VLCの最も大きな特徴で、現在数あるメディアプレイヤーの中でも群を抜いている。コーデックは内蔵されており、別途入手する必要はない。

[ネットワーク上の](../Page/コンピュータネットワーク.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")のファイルを再生するためのクライアントソフトとして開発され始めたため、[ブラウザ](https://ja.wikipedia.org/wiki/ブラウザ "wikilink")や端末上からでも比較的簡単に[ストリーミング](../Page/ストリーミング.md "wikilink")再生などを行うことができる。[ポッドキャスト](../Page/ポッドキャスト.md "wikilink")にも対応している。

上記のクライアントのような使い方をしない大半のユーザは[Qt](../Page/Qt.md "wikilink")を使用したシンプルな[GUIから操作する](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。 VLCに対して設定できる項目は非常に多い。そのため、画面をシンプルにみせるようにした設定画面が用意されている。

QtのGUIは[スキン](https://ja.wikipedia.org/wiki/スキン "wikilink")と呼ばれるもので見た目を自在に変更できる。スキンはVLCの公式ページなどでダウンロードできる。

VLCメディアプレーヤーは[ポータブルアプリケーション](../Page/ポータブルアプリケーション.md "wikilink")としても使うこともできる。

## 他のプログラムからVLCを使う

他のプログラムからVLCの機能にアクセスするための[APIが用意されている](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

### API

VLCのコーデックはCで書かれたlibvlcというプログラムに内蔵されており、[C](../Page/C言語.md "wikilink")・[C++](../Page/C++.md "wikilink")・[C\#からアクセスできる](../Page/C_Sharp.md "wikilink")。 [JavaScript](../Page/JavaScript.md "wikilink")、[Python](../Page/Python.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")などを使ってもVLCにアクセスできる。

### ブラウザ プラグイン

Windows、LinuxなどのプラットフォームでNPAPIプラグインを提供する。これは[QuickTime](../Page/QuickTime.md "wikilink")、[Windows Media](https://ja.wikipedia.org/wiki/Windows_Media "wikilink")、[MP3](../Page/MP3.md "wikilink")、[Ogg](../Page/Ogg.md "wikilink")などが埋め込まれたウェブコンテンツを[アップルや](../Page/アップル_\(企業\).md "wikilink")[マイクロソフト](../Page/マイクロソフト.md "wikilink")のツールに依存せず再生するためで、ブラウザではFirefoxを含む[Mozilla](../Page/Mozilla.md "wikilink")アプリケーション、[Safari](../Page/Safari.md "wikilink")、[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")、[Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")、[Netscape](https://ja.wikipedia.org/wiki/Netscape "wikilink")に対応している。[Adobe Flashも見ることができる](../Page/Adobe_Flash.md "wikilink")。[Internet Explorerにもバージョン](../Page/Internet_Explorer.md "wikilink")0.8.2以降は[ActiveX](../Page/ActiveX.md "wikilink")プラグインによって、同様の機能を提供している。

## 主な機能

### 再生機能

  - 音楽ファイルの再生
  - 動画ファイルの再生
  - CD, DVDの再生
  - 早送り、巻き戻しなどの操作
  - 加速再生、減速再生
  - ステレオ、モノラル再生、PANの設定
  - 一定区間の繰り返し再生
  - イコライザ
  - 再生位置ブックマーク
  - メディア情報の表示
  - ポッドキャストの再生
  - サーバーからのストリーミング再生

### GUI

  - ビジュアライザ
  - Qtインターフェイスの改造、スキンの適用
  - マウスジェスチャ
  - OSDによる表示
  - キーボードショートカット

### 動画

  - 動画ファイルの再生
  - 字幕再生
  - スナップショットの撮影
  - フルスクリーン再生
  - ズーム、縦横比率の変更
  - スケール、クロップ

### その他

  - プレイリストの読み込み、書き出し
  - メディアコーデックの相互変換
  - プラグインの追加と削除（[Blu-ray Disc再生など](../Page/Blu-ray_Disc.md "wikilink")）

## 再生サポート

### 入力メディア

  - ディスク

[DVD-Video](../Page/DVD-Video.md "wikilink")、[ビデオCD](../Page/ビデオCD.md "wikilink")、[スーパービデオCD](../Page/スーパービデオCD.md "wikilink") (メニューに対応)、[音楽CD](../Page/CD-DA.md "wikilink") (DTS-CDは非対応。[CD-TEXT](https://ja.wikipedia.org/wiki/CD-TEXT "wikilink")に対応)\[1\] 3.0以降では、[AACS](https://ja.wikipedia.org/wiki/AACS "wikilink")がかかっていない[HD_DVD](../Page/HD_DVD.md "wikilink")に限りその中の`.evo`ファイルを再生できる \[2\]。 2.0以降では、[AACS](https://ja.wikipedia.org/wiki/AACS "wikilink")がかかっていない[ブルーレイを再生できる](../Page/Blu-ray_Disc.md "wikilink")。

  - ネットワークプロトコル

[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[FTP](../Page/File_Transfer_Protocol.md "wikilink")、[MMS](https://ja.wikipedia.org/wiki/MMS "wikilink")、[YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink")など

  - その他

DVB、ビデオキャプチャーデバイス ([Webカメラ](../Page/Webカメラ.md "wikilink")など)

### コンテナ形式

[AVI](https://ja.wikipedia.org/wiki/AVI "wikilink")([DMF](https://ja.wikipedia.org/wiki/DivX#DivX_Media_Format "wikilink"))、[ASF](../Page/Advanced_Systems_Format.md "wikilink")、[MP4](../Page/MP4.md "wikilink")、[MOV](../Page/QuickTime.md "wikilink")、[MPEG-2システム](../Page/MPEG-2システム.md "wikilink")、[Ogg](../Page/Ogg.md "wikilink")、[OGM](../Page/Ogg_Media.md "wikilink")、[Matroska](../Page/Matroska.md "wikilink")([WebM](https://ja.wikipedia.org/wiki/WebM "wikilink"))、[WAV](../Page/WAV.md "wikilink")、[FLVなど](../Page/Flash_Video.md "wikilink")

### ビデオコーデック

[MPEG-1/2](../Page/Moving_Picture_Experts_Group.md "wikilink")、[DivX](https://ja.wikipedia.org/wiki/DivX "wikilink") (1/2/3/4/5/6)、[MPEG-4 ASP](../Page/MPEG-4.md "wikilink")、[Xvid](../Page/Xvid.md "wikilink")、3ivX D4、[H.261](../Page/H.261.md "wikilink")、[H.263](../Page/H.263.md "wikilink")、H.263i、[H.264](../Page/H.264.md "wikilink") (MPEG-4 AVC)、[Cinepak](../Page/Cinepak.md "wikilink")、[Theora](../Page/Theora.md "wikilink")、[Dirac](https://ja.wikipedia.org/wiki/Dirac "wikilink") (VC-2)、[モーションJPEG](../Page/Motion_JPEG.md "wikilink") (A/B)、[WMV](../Page/Windows_Media_Video.md "wikilink") 1/2、 WMV 3、WMV9、[VC-1](../Page/VC-1.md "wikilink")、Sorenson 1/3、[DV](../Page/DV_\(ビデオ規格\).md "wikilink")、On2 ([VP3](https://ja.wikipedia.org/wiki/VP3 "wikilink")/VP5/[VP6](../Page/VP6.md "wikilink"))、[Indeo Video v3](../Page/Indeo.md "wikilink")、[RealVideo](https://ja.wikipedia.org/wiki/RealVideo "wikilink") (1/2/3/4)\[3\]

### オーディオコーデック

MPEG-1/2 Layer 1、[MP2](https://ja.wikipedia.org/wiki/MPEG-1/2_Layer_2 "wikilink")、[MP3](../Page/MP3.md "wikilink")、[MPEG-4 AAC](https://ja.wikipedia.org/wiki/MPEG-4_AAC "wikilink") part3、[Ogg Vorbis](../Page/Vorbis.md "wikilink")、[AC-3](https://ja.wikipedia.org/wiki/AC-3 "wikilink") (ドルビーデジタル)、E-AC-3、MLP/TrueHD、[DTS](https://ja.wikipedia.org/wiki/DTS "wikilink")、[WMA](../Page/Windows_Media_Audio.md "wikilink") (1/2/3)、[FLAC](../Page/FLAC.md "wikilink")、[ALAC](../Page/Apple_Lossless.md "wikilink")、[Speex](../Page/Speex.md "wikilink")、[Musepack](../Page/Musepack.md "wikilink") (MPC)、[ATRAC](../Page/ATRAC.md "wikilink") 3、[WavPack](https://ja.wikipedia.org/wiki/WavPack "wikilink")、[Mod](../Page/MOD_\(ファイルフォーマット\).md "wikilink")、TrueAudio、APE ([Monkey's Audio](../Page/Monkey's_Audio.md "wikilink"))、[Real Audio](https://ja.wikipedia.org/wiki/Real_Audio "wikilink")、[Alaw](https://ja.wikipedia.org/wiki/A-lawアルゴリズム "wikilink")/[μlaw](https://ja.wikipedia.org/wiki/Μ-lawアルゴリズム "wikilink")、[AMR](../Page/Adaptive_Multi-Rate.md "wikilink") (3GPP)、[MIDI](../Page/MIDI.md "wikilink")、[LPCM](https://ja.wikipedia.org/wiki/LPCM "wikilink")、[ADPCM](https://ja.wikipedia.org/wiki/ADPCM "wikilink")、QCELP、[DV Audio](../Page/DV_\(ビデオ規格\).md "wikilink")、QDM2 (QDMC)、MACE\[4\]

### 字幕コーデック

DVD字幕、テキストファイル (MicroDVD、[SubRIP](https://ja.wikipedia.org/wiki/SubRip "wikilink") (SRT)、SubViewer、SSA1-5、SAMI、VPlayer)、[クローズドキャプション](../Page/クローズドキャプション.md "wikilink")、Vobsub、Universal Subtitle Format (USF)、SVCD字幕 (CVD)、DVB字幕、OGM、CMML、OggKate、[ID3タグ](../Page/ID3タグ.md "wikilink")、APEv2、Vorbis comment

## 対応OS

以下の[OSに対応している](../Page/オペレーティングシステム.md "wikilink")。\[5\]

  - Windows

<!-- end list -->

  - [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")
  - [UWPアプリ形式](https://ja.wikipedia.org/wiki/ユニバーサルWindowsプラットフォーム "wikilink")
  - Windows Phone

<!-- end list -->

  - Apple

<!-- end list -->

  - [MacOS X](../Page/MacOS.md "wikilink")
  - [iOS](https://ja.wikipedia.org/wiki/IOS_\(アップル\) "wikilink")
  - [Apple TV](../Page/Apple_TV.md "wikilink")

<!-- end list -->

  - [GNU/Linux](https://ja.wikipedia.org/wiki/GNU/Linux "wikilink")

<!-- end list -->

  - [Debian GNU/Linux](https://ja.wikipedia.org/wiki/Debian_GNU/Linux "wikilink")
  - [Ubuntu](../Page/Ubuntu.md "wikilink")
  - [Mint](../Page/Linux_Mint.md "wikilink")
  - [openSUSE](https://ja.wikipedia.org/wiki/openSUSE "wikilink")
  - [Gentoo Linux](../Page/Gentoo_Linux.md "wikilink")
  - [Fedora](../Page/Fedora.md "wikilink")
  - [Arch Linux](https://ja.wikipedia.org/wiki/Arch_Linux "wikilink")
  - [Slackware Linux](https://ja.wikipedia.org/wiki/Slackware_Linux "wikilink")
  - [Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink")

<!-- end list -->

  - その他

<!-- end list -->

  - [Android](../Page/Android.md "wikilink")
  - [Chrome OS](https://ja.wikipedia.org/wiki/Google_Chrome_OS "wikilink")
  - [FreeBSD](../Page/FreeBSD.md "wikilink")
  - [NetBSD](../Page/NetBSD.md "wikilink")
  - [OpenBSD](../Page/OpenBSD.md "wikilink")
  - [Solaris](../Page/Solaris.md "wikilink")
  - [QNX](../Page/QNX.md "wikilink")
  - [OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")

## 脚注

## 関連項目

  - [ソフトウェア特許](../Page/ソフトウェア特許.md "wikilink")
  - [HD DVD](../Page/HD_DVD.md "wikilink")
  - [オープンソースのメディアプレーヤー](https://ja.wikipedia.org/wiki/オープンソースのメディアプレーヤー "wikilink")

## 外部リンク

  -
  - [VLC Media Player Portable](https://portableapps.com/apps/music_video/vlc_portable) PortableApps.com Windows用

[Category:メディアプレーヤーソフト](https://ja.wikipedia.org/wiki/Category:メディアプレーヤーソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:DVD関連のソフト](https://ja.wikipedia.org/wiki/Category:DVD関連のソフト "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:Qtを使用するソフトウェア](https://ja.wikipedia.org/wiki/Category:Qtを使用するソフトウェア "wikilink") [Category:2001年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2001年のソフトウェア "wikilink")

1.
2.
3.
4.
5.