> この記事は[Audio Video Interleave](https://ja.wikipedia.org/wiki/Audio_Video_Interleave)から翻訳されています。


**Audio Video Interleave**（オーディオ ビデオ インターリーブ）は[動画](../Page/動画.md "wikilink")用[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")である。

## 概要

[Windows標準の](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[動画](../Page/動画.md "wikilink")用[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")（[コンテナ形式](../Page/コンテナフォーマット.md "wikilink")）で、AVIファイル、AVIコンテナなどと呼ばれている。[拡張子](../Page/拡張子.md "wikilink")は「.avi」である。一部の古いコーデックは[Windows Media Playerで再生可能である](../Page/Windows_Media_Player.md "wikilink")。

[マイクロソフト](../Page/マイクロソフト.md "wikilink")が[アップルコンピュータの](../Page/アップル_\(企業\).md "wikilink")[QuickTime](../Page/QuickTime.md "wikilink")に対抗するために開発した[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、[Video for Windowsで対応している](https://ja.wikipedia.org/wiki/Video_for_Windows "wikilink")。

[RIFFというフォーマットを利用し](../Page/Resource_Interchange_File_Format.md "wikilink")[画像](../Page/画像.md "wikilink")と[音声](https://ja.wikipedia.org/wiki/音声 "wikilink")を交互に織り交ぜながら（[インターリーブ](../Page/インターリーブ.md "wikilink")）格納する。

[インデックスが最後にあるため](../Page/索引.md "wikilink")、AVIファイルの内容が不完全な状態では再生が出来ず、修復を行わなければならない。

拡張子が「.divx」の[DivX Media Formatは基本部分はAVIそのものである](https://ja.wikipedia.org/wiki/DivX#DivX_Media_Format "wikilink")。

今となってはAVI自体は入れ物（[コンテナ](../Page/コンテナフォーマット.md "wikilink")）となってしまった。現在ではいくつかの種類（[後述](https://ja.wikipedia.org/wiki/#AVIファイルで使われるコーデック "wikilink")）の[コーデック](../Page/コーデック.md "wikilink")でエンコードされた[動画](../Page/動画.md "wikilink")や[音声](https://ja.wikipedia.org/wiki/音声 "wikilink")のデータを格納できる。そのため再生には適切なコーデックを用意する必要があるが、ファイルの拡張子を見ただけではコーデックが何であるか判断できない\[1\]。しかし。

## 主な特徴

AVIを含むRIFFファイルは、バイナリのままでも[可読性](../Page/可読性.md "wikilink")が高く構造を理解しやすい。また、AVIを扱うAPI（Video for Windows）をWindowsが提供しているため、対応ソフトウェアを開発しやすく、実際に多数のソフトウェアが公開されている。

### 欠点

AVIは[1992年](../Page/1992年.md "wikilink")以前に策定された比較的古い形式であり、策定当初は問題とはならなかった次のような点が現在では欠点となってしまっている。

  - [ストリーミング](../Page/ストリーミング.md "wikilink")配信用途には不向き。
  - AVI1.0では2GBを超えるファイルを作成できない（AVI2.0（[OpenDML](https://ja.wikipedia.org/wiki/OpenDML "wikilink")）で解決済み）。
  - [データ](../Page/データ.md "wikilink")が個別の[タイムスタンプ](https://ja.wikipedia.org/wiki/タイムスタンプ "wikilink")を保持できない。
      - 映像の可変フレームレート（VFR）に対応していない（擬似的な方法での実現例はある）。
      - [Bフレーム](https://ja.wikipedia.org/wiki/Bフレーム "wikilink")（前方参照フレーム）の表示に不都合が生じる。

### Bフレームの表示不都合

AVIコンテナに格納されたストリームデータは、再生時に一定間隔で先頭から順に取り出される。Bフレームが[フレーム間予測](../Page/フレーム間予測.md "wikilink")において前方フレームを参照して符号化されていた場合、参照する**Pフレーム**が処理されて初めて復号可能となる。このため、BフレームをAVIコンテナに格納する際に、このフレーム間の参照関係を考慮しPフレームと順序を入れ替えて格納することになる。こうして格納されたデータは、データを復号し、復号された画像を表示するという作業を特定のタイミングで繰り返すことで[動画](../Page/動画.md "wikilink")として再生される事になるが、データの復号と表示の間隔はフレームレートから計算するため同一のタイミングとなる。その結果、復号した画像がそのままの順序で表示される事になり、部分的に逆再生を行っているかのような動画となってしまう（たとえば、[MP4](../Page/MP4.md "wikilink")コンテナではデータ復号・復号画像の合成・表示のタイミングを個別に指定できるためこの問題は発生しない）。

しかし、近年のデコーダは入力されたデータに対し本来の表示順序通りにフレームを出力するよう改良されているため、利用上の問題はなくなっている。ただし、この方法を用いたデコーダでは最初のIフレームが他のフレームの2倍の表示時間となり、最終フレームは表示されないという副作用が発生する。この副作用についても、**Packed-bitstream**と呼ばれる特殊なストリームフォーマットを用いることで解消した例がある（[Xvid](../Page/Xvid.md "wikilink")、[DivX](https://ja.wikipedia.org/wiki/DivX "wikilink")がサポートしている）。以上の様に、[コーデック](../Page/コーデック.md "wikilink")側の工夫によってBフレームは問題なく利用可能となっているが、AVIコンテナ自体にBフレームを正確に扱う為の情報が不足しているため、今後も新しい映像圧縮技術をAVIで扱えるかどうかはコーデック側に委ねられたことになる。

## AVI2.0

Matrox OpenDMLグループが[1996年](../Page/1996年.md "wikilink")2月に発表したAVIの拡張仕様で、これらはマイクロソフトによってサポートされ、非公式であるが「AVI2.0」と呼称されている。1996年2月28日にバージョン1.02が制定されている\[2\]。

特徴としては以下が挙げられる。

  - 2GBを超えるファイルの取り扱いが可能。ファイルサイズはほぼ無制限（[NTFSの許容範囲よりはるかに大きい](../Page/NT_File_System.md "wikilink")）。
  - 3%のオーバーヘッド削減。

Windowsにおいては標準APIがVideo For Windowsに代わってDirectShowとなっており、DirectShowが出力するAVIファイルは通常AVI2.0形式となっている。これは従来のAVIが持つ古典的インデックスを余分に含んでおり、2GB未満のファイルの場合は通常のAVIとしても使用することができる\[3\]。

## 利用例

  - さまざまな[コーデック](../Page/コーデック.md "wikilink")による動画圧縮保存。
      - デジタル[ビデオカメラ](../Page/ビデオカメラ.md "wikilink")で撮影した映像の、編集作業用ファイルとして。
      - テレビ番組の無圧縮AVI[キャプチャー](https://ja.wikipedia.org/wiki/ビデオキャプチャ "wikilink")。
  - [ファイル共有ソフト](../Page/ファイル共有ソフト.md "wikilink")での動画の交換、共有。

## AVIファイルで使われるコーデック

### コーデック一覧

現在エンコーダーが公開されていない形式を含む。

  - 映像（FourCC）

<!-- end list -->

  - [MPEG-1](../Page/MPEG-1.md "wikilink")/[-2](../Page/MPEG-2.md "wikilink")（MPEG/MPG1/MPG2） - 通常は[MPEG-2システム](../Page/MPEG-2システム.md "wikilink")などが使われる。
  - [MPEG-4](../Page/MPEG-4.md "wikilink")（MP4V/XVID/DX50/DIVX/DIV5/DIV4/3IVX/3IV2/RMP4）
  - [MS-MPEG4](https://ja.wikipedia.org/wiki/MS-MPEG4 "wikilink")（MPG4/MP42/MP43）
  - [WMV7](../Page/Windows_Media_Video.md "wikilink")/WMV8/WMV9（WMV1/WMV2/WMV3） - 通常は[ASF](https://ja.wikipedia.org/wiki/ASF "wikilink")コンテナが使われる。
  - [DV](../Page/DV_\(ビデオ規格\).md "wikilink")（DVSD/DVIS）
  - [Flash Video](../Page/Flash_Video.md "wikilink")（FLV1/FLV4）
  - [Motion JPEG](../Page/Motion_JPEG.md "wikilink")（MJPG）
  - [Lossless JPEG](https://ja.wikipedia.org/wiki/Lossless_JPEG "wikilink")（LJPG）
  - [H.264](../Page/H.264.md "wikilink")（AVC1/DAVC/H264/X264）
  - [H.263](../Page/H.263.md "wikilink")/[H.263](../Page/H.263.md "wikilink")+（H263/S263）
  - [H.261](../Page/H.261.md "wikilink")（H261）
  - [FFV1](../Page/FFmpeg.md "wikilink")（FFV1）
  - [Huffyuv](https://ja.wikipedia.org/wiki/Huffyuv "wikilink")/[FFvHuff](https://ja.wikipedia.org/wiki/Huffyuv "wikilink")（HFYU/FFVH）
  - [AVImszh](https://ja.wikipedia.org/wiki/AVImszh "wikilink")（MSZH）
  - [Theora](../Page/Theora.md "wikilink")（THEO） - 通常は[Ogg](../Page/Ogg.md "wikilink")コンテナが使われる。
  - [Indeo Video](../Page/Indeo.md "wikilink")（IV31/IV32）
  - [Cinepak](../Page/Cinepak.md "wikilink")（CVID）
  - [Microsoft Video 1](https://ja.wikipedia.org/wiki/Microsoft_Video_1 "wikilink")（CRAM）
  - [On2VP3](https://ja.wikipedia.org/wiki/On2VP3 "wikilink")（VP30/VP31）
  - [On2VP4](https://ja.wikipedia.org/wiki/On2VP4 "wikilink")（VP40）
  - [On2VP5](https://ja.wikipedia.org/wiki/On2VP5 "wikilink")（VP50）
  - [On2 VP6](https://ja.wikipedia.org/wiki/On2_VP6 "wikilink")（VP60/VP61/VP62）
  - [On2 VP7](https://ja.wikipedia.org/wiki/On2_VP7 "wikilink")（VP70）
  - [VP8](https://ja.wikipedia.org/wiki/VP8 "wikilink")（VP80） - 通常は[WebM](https://ja.wikipedia.org/wiki/WebM "wikilink")コンテナが使われる。
  - [VC-1](../Page/VC-1.md "wikilink")（WVC1）

<!-- end list -->

  - 音声（Code）

<!-- end list -->

  - [リニアPCM](../Page/パルス符号変調.md "wikilink")
  - [ADPCM](../Page/適応的差分パルス符号変調.md "wikilink")
  - [MP3](../Page/MP3.md "wikilink")（0x0055）
  - [AC-3](../Page/ドルビーデジタル.md "wikilink")（0x0092）
  - [AAC](../Page/AAC.md "wikilink")
  - [HE-AAC](../Page/HE-AAC.md "wikilink")
  - [FLAC](../Page/FLAC.md "wikilink")
  - [Indeo Audio](../Page/Indeo.md "wikilink")
  - [TrueSpeech](https://ja.wikipedia.org/wiki/TrueSpeech "wikilink")
  - [Windows Media Audio](../Page/Windows_Media_Audio.md "wikilink")
  - [Vorbis](../Page/Vorbis.md "wikilink") - VBR（[可変ビットレート](../Page/可変ビットレート.md "wikilink")）メインで設計されており、CBR（[固定ビットレート](https://ja.wikipedia.org/wiki/固定ビットレート "wikilink")）は擬似方式のみサポートのため、互換性に難がある。

### コーデックの組み合わせ

コーデックの組み合わせは以下の例のように動画作成者が自由に選択できる。この自由度の高さが、再生できないAVIファイルが生まれる原因となっている。

  - DivX+MP3
  - H.264+MP3
  - H.264+AAC
  - WMV9+MP3

## 脚注

<references />

## 関連項目

  - コンテナ形式

<!-- end list -->

  - [Advanced Systems Format](../Page/Advanced_Systems_Format.md "wikilink")（ASF）
  - [DivX Media Format](https://ja.wikipedia.org/wiki/DivX#DivX_Media_Format "wikilink")（DMF）
  - [Matroska](../Page/Matroska.md "wikilink")（MKV）

<!-- end list -->

  - コーデック

<!-- end list -->

  - [Divx](https://ja.wikipedia.org/wiki/Divx "wikilink")
  - [Xvid](../Page/Xvid.md "wikilink")
  - [3ivx](https://ja.wikipedia.org/wiki/3ivx "wikilink")

<!-- end list -->

  - ソフトウェア

<!-- end list -->

  - [AviUtl](../Page/AviUtl.md "wikilink")
  - [AVI-Mux GUI](https://ja.wikipedia.org/wiki/AVI-Mux_GUI "wikilink")
  - [Avisynth](https://ja.wikipedia.org/wiki/Avisynth "wikilink")
  - [VirtualDub](../Page/VirtualDub.md "wikilink")

<!-- end list -->

  - その他

<!-- end list -->

  - [ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")
  - [コンテナフォーマット](../Page/コンテナフォーマット.md "wikilink")
  - [FourCC](https://ja.wikipedia.org/wiki/FourCC "wikilink")
  - [AviUtl](../Page/AviUtl.md "wikilink")

## 外部リンク

  - [Microsoft AVI ファイルフォーマット](http://msdn.microsoft.com/library/ja/directx9_c/directx/htm/avifileformat.asp)
  - [Broadband Watch--BBっとWORDS 「AVIの生い立ちとそのコーデック」](http://bb.watch.impress.co.jp/cda/bbword/14580.html)
  - [VIDEO-ITを取り巻く市場と技術 第1回 ファイルフォーマットとは?](http://www.mpeg.co.jp/libraries/video_it/video_01.html)
  - [mpeg.co.jp MPEGラボ 第18回 AVIはストリーミングできない?動画ファイルの内部構造を知る](http://www.mpeg.co.jp/libraries/mpeg_labo/winPC_18.html)

[Category:マイクロソフト](https://ja.wikipedia.org/wiki/Category:マイクロソフト "wikilink") [Category:動画ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:動画ファイルフォーマット "wikilink")

1.  [真空波動研](https://ja.wikipedia.org/wiki/真空波動研 "wikilink")や[MMname2](https://ja.wikipedia.org/wiki/MMname2 "wikilink")といったコーデックを調べるソフトがある。
2.
3.