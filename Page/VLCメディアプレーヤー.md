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

  - メディア
    [DVD-Video](../Page/DVD-Video.md "wikilink")、[ビデオCD](../Page/ビデオCD.md "wikilink")、[スーパービデオCD](../Page/スーパービデオCD.md "wikilink")、[音楽CD](../Page/CD-DA.md "wikilink")、[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[FTP](../Page/File_Transfer_Protocol.md "wikilink")、[MMS](https://ja.wikipedia.org/wiki/MMS "wikilink")など

また[AACS](https://ja.wikipedia.org/wiki/AACS "wikilink")が使用されていなければ[HD_DVD](../Page/HD_DVD.md "wikilink")も3.0以降で再生できるという\[1\]。

  - コンテナ形式
    [AVI](https://ja.wikipedia.org/wiki/AVI "wikilink")([DMF](https://ja.wikipedia.org/wiki/DivX#DivX_Media_Format "wikilink"))、[ASF](../Page/Advanced_Systems_Format.md "wikilink")、[MP4](../Page/MP4.md "wikilink")、[MOV](../Page/QuickTime.md "wikilink")、[MPEG-2システム](../Page/MPEG-2システム.md "wikilink")、[Ogg](../Page/Ogg.md "wikilink")、[OGM](../Page/Ogg_Media.md "wikilink")、[Matroska](../Page/Matroska.md "wikilink")([WebM](https://ja.wikipedia.org/wiki/WebM "wikilink"))、[WAV](../Page/WAV.md "wikilink")、[FLVなど](../Page/Flash_Video.md "wikilink")

<!-- end list -->

  - ビデオコーデック
    [MPEG-4](../Page/MPEG-4.md "wikilink")([DivX](https://ja.wikipedia.org/wiki/DivX "wikilink")・[Xvid](../Page/Xvid.md "wikilink")・3ivX)、[MS-MPEG4](https://ja.wikipedia.org/wiki/MS-MPEG4 "wikilink")、[H.263](../Page/H.263.md "wikilink")、[WMV9](../Page/Windows_Media_Video.md "wikilink")([VC-1](../Page/VC-1.md "wikilink"))、[DV](../Page/DV_\(ビデオ規格\).md "wikilink")、[Theora](../Page/Theora.md "wikilink")、[H.264](../Page/H.264.md "wikilink")、[Motion JPEG](../Page/Motion_JPEG.md "wikilink")、[On2VP3](https://ja.wikipedia.org/wiki/On2VP3 "wikilink")、[On2 VP6](https://ja.wikipedia.org/wiki/On2_VP6 "wikilink")、[VP8](https://ja.wikipedia.org/wiki/VP8 "wikilink")、[Cinepak](../Page/Cinepak.md "wikilink")、[RealVideo](https://ja.wikipedia.org/wiki/RealVideo "wikilink")、[Dirac](https://ja.wikipedia.org/wiki/Dirac "wikilink")など

<!-- end list -->

  - オーディオコーデック
    MP1、[MP2](https://ja.wikipedia.org/wiki/MP2 "wikilink")、[MP3](../Page/MP3.md "wikilink")、[AC-3](../Page/ドルビーデジタル.md "wikilink")、[DTS](https://ja.wikipedia.org/wiki/デジタル・シアター・システムズ "wikilink")、[LPCM](../Page/パルス符号変調.md "wikilink")、[AAC](../Page/AAC.md "wikilink")、[Vorbis](../Page/Vorbis.md "wikilink")、[WMA](../Page/Windows_Media_Audio.md "wikilink")、[ADPCM](https://ja.wikipedia.org/wiki/ADPCM "wikilink")、[DV Audio](../Page/DV_\(ビデオ規格\).md "wikilink")、[FLAC](../Page/FLAC.md "wikilink")、[Real Audio](https://ja.wikipedia.org/wiki/Real_Audio "wikilink")、[Speex](../Page/Speex.md "wikilink")、[ATRAC](../Page/ATRAC.md "wikilink")、[WavPack](https://ja.wikipedia.org/wiki/WavPack "wikilink")、[TTA](../Page/TTA.md "wikilink")、[Monkey's Audio](../Page/Monkey's_Audio.md "wikilink")、[Musepack](../Page/Musepack.md "wikilink")、[Apple Lossless](../Page/Apple_Lossless.md "wikilink") など

## 対応OS

以下の[OSに対応している](../Page/オペレーティングシステム.md "wikilink")。

  - [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")
    [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")
    [GNU/Linux](https://ja.wikipedia.org/wiki/GNU/Linux "wikilink")
    [Debian GNU/Linux](https://ja.wikipedia.org/wiki/Debian_GNU/Linux "wikilink")

    [Ubuntu](../Page/Ubuntu.md "wikilink")

    [Mint](https://ja.wikipedia.org/wiki/Linux_Mint "wikilink")

    [openSUSE](https://ja.wikipedia.org/wiki/openSUSE "wikilink")

    [Gentoo Linux](../Page/Gentoo_Linux.md "wikilink")

    [Fedora](../Page/Fedora.md "wikilink")

    [Arch Linux](https://ja.wikipedia.org/wiki/Arch_Linux "wikilink")

    [Slackware Linux](https://ja.wikipedia.org/wiki/Slackware_Linux "wikilink")

    [Mandriva Linux](../Page/Mandriva_Linux.md "wikilink")

    [Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink")

  - [FreeBSD](../Page/FreeBSD.md "wikilink")
    [NetBSD](../Page/NetBSD.md "wikilink")
    [OpenBSD](../Page/OpenBSD.md "wikilink")
    [Solaris](../Page/Solaris.md "wikilink")
    [Android](../Page/Android.md "wikilink")
    [iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")
    [QNX](../Page/QNX.md "wikilink")
    [Syllable](https://ja.wikipedia.org/wiki/Syllable "wikilink")
    [OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")

## 脚注

## 関連項目

  - [ソフトウェア特許](../Page/ソフトウェア特許.md "wikilink")
  - [HD_DVD](../Page/HD_DVD.md "wikilink")
  - [オープンソースのメディアプレーヤー](https://ja.wikipedia.org/wiki/オープンソースのメディアプレーヤー "wikilink")

## 外部リンク

  -
  - [VLC Media Player Portable](https://portableapps.com/apps/music_video/vlc_portable) PortableApps.com Windows用

[Category:メディアプレーヤーソフト](https://ja.wikipedia.org/wiki/Category:メディアプレーヤーソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:DVD関連のソフト](https://ja.wikipedia.org/wiki/Category:DVD関連のソフト "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:Qtを使用するソフトウェア](https://ja.wikipedia.org/wiki/Category:Qtを使用するソフトウェア "wikilink") [Category:2001年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2001年のソフトウェア "wikilink")

1.  <https://av.watch.impress.co.jp/docs/news/1106943.html>