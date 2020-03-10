> この記事は[Windows Media Video](https://ja.wikipedia.org/wiki/Windows_Media_Video)から翻訳されています。


**Windows Media Video**（ウィンドウズ・メディア・ビデオ、略称**WMV**）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")がWindows Media Formatの中核をなすものとして開発した[ビデオ](../Page/映像信号.md "wikilink")[コーデック](../Page/コーデック.md "wikilink")。[オーディオ](https://ja.wikipedia.org/wiki/オーディオ "wikilink")コーデックとして[Windows Media Audio](../Page/Windows_Media_Audio.md "wikilink")（WMA）があり、一般にはWMVとWMAの組み合わせが用いられる。

## 概要

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")、マイクロソフトは[Windows Media Player](../Page/Windows_Media_Player.md "wikilink")6を発表し、[MS-MPEG4](https://ja.wikipedia.org/wiki/MS-MPEG4 "wikilink")コーデックを搭載した。以後、[2000年](../Page/2000年.md "wikilink")に発表したWindows Media Player 7でWindows Media Video 7を採用したのを皮切りに、独自コーデックとして8、9へと改良を重ね、現在に至る。

[2003年](../Page/2003年.md "wikilink")[9月](../Page/9月.md "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")は米国映画テレビジョン技術者協会（[SMPTE](../Page/SMPTE.md "wikilink")）にWMV9のデコーダ部分の[ソースコード](../Page/ソースコード.md "wikilink")を標準規格候補としてVC-9という名称で提出した（後に[VC-1](https://ja.wikipedia.org/wiki/VC-1 "wikilink")に改称された）。その際Windows Media Video 9がMPEG-4をベースとして改良された方式であることが表面化し、ライセンスの扱いが問題となったが、結局[2004年](../Page/2004年.md "wikilink")[2月](https://ja.wikipedia.org/wiki/2月 "wikilink")には[DVDフォーラム](../Page/DVDフォーラム.md "wikilink")によってVC-9（当時）が[HD DVDの必須](../Page/HD_DVD.md "wikilink")[映像](https://ja.wikipedia.org/wiki/映像 "wikilink")[コーデック](../Page/コーデック.md "wikilink")として承認され、2004年9月には[第3世代光ディスク](../Page/第3世代光ディスク.md "wikilink")（当時の「次世代DVD」）規格としてHD DVDと競合していた[Blu-ray DiscもビデオコーデックとしてVC](../Page/Blu-ray_Disc.md "wikilink")-1を採用するなど、[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")向け以外にもWindows Media Video技術の用途が拡大しつつある。

## 特徴

  - [Microsoft Windowsで標準対応](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")（Windows Media Playerで再生可能）であるため、PCでの再生環境の普及率は高い。
  - WMV9はDVD（[MPEG-2](../Page/MPEG-2.md "wikilink")）の約半分の[ビットレート](https://ja.wikipedia.org/wiki/ビットレート "wikilink")で同等の画質を得られるとしている。また、[HDTVにも対応している](https://ja.wikipedia.org/wiki/高精細度テレビジョン放送 "wikilink")（WMV HD）。
  - 低ビットレートでも映像の破綻が少なく、[ストリーミング](../Page/ストリーミング.md "wikilink")（[ASFコンテナ格納時のみ](../Page/Advanced_Systems_Format.md "wikilink")）にも対応しているので、[インターネット](../Page/インターネット.md "wikilink")の[ネット配信](../Page/ネット配信.md "wikilink")に適している。
  - [デジタル著作権管理](https://ja.wikipedia.org/wiki/デジタル著作権管理 "wikilink")（DRM）対応（ASFコンテナ格納時のみ）によって、著作者の意図しないコピーを防止することができる。
  - [エンコード](../Page/エンコード.md "wikilink")に時間がかかる（[DivX](https://ja.wikipedia.org/wiki/DivX "wikilink")などの約1.5倍〜2倍程度）。エンコードの速度指定でかなり改善できる。
  - シーク出来ないように出来る（ASFコンテナ格納時）。

## 利用例

  - 企業や団体の一般向け動画配信。
  - テレビ番組やビデオカメラで録画した映像を保存する。
  - Windows Media EncoderやMicrosoft Expression Encoderを使用すると個人配信も容易。

## コンテナ形式

従来のビデオコーデック同様に[DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")を利用した[コンテナ形式](../Page/コンテナフォーマット.md "wikilink")（[ASF](../Page/Advanced_Systems_Format.md "wikilink")/WMV、[AVI等](../Page/Audio_Video_Interleave.md "wikilink")）に格納することが可能。

  - 通常のWMV9（ASFコンテナに格納）

<!-- end list -->

  - （WMV9+WMA9）.wmv

<!-- end list -->

  - VCMを使用したWMV9（AVIコンテナに格納）

<!-- end list -->

  - （WMV9+MP3）.avi

## 注意事項

WMV9は、下記の3つが存在する。

  - 通常のWMV9コーデックで圧縮したもの=[FourCC](https://ja.wikipedia.org/wiki/FourCC "wikilink"):WMV3
  - WMP10系エンコーダで圧縮したWMV9 Advanced Profile=FourCC:WMVA
  - WMP11系エンコーダで圧縮したWMV9 Advanced Profile=FourCC:WVC1

VC-1として採用されたのは、WMV3とWVC1であるため、WMVAでエンコードされたファイルは、[HD DVDや](../Page/HD_DVD.md "wikilink")[Blu-ray Discに用いることが出来ない](../Page/Blu-ray_Disc.md "wikilink")。

マイクロソフトは、今後エンコードする際は、WMVAではなくWVC1を用いるよう呼びかけている\[1\]。

## 脚注

<references />

## 関連項目

### VC-1採用規格

  - [Blu-ray Disc](../Page/Blu-ray_Disc.md "wikilink")
  - [HD DVD](../Page/HD_DVD.md "wikilink")

### コンテナ形式

  - [Advanced Systems Format](../Page/Advanced_Systems_Format.md "wikilink")（ASF）
  - [Audio Video Interleave](../Page/Audio_Video_Interleave.md "wikilink")（AVI）

### コーデック

  - [Windows Media Audio](../Page/Windows_Media_Audio.md "wikilink")（WMA）
  - [VC-1](https://ja.wikipedia.org/wiki/VC-1 "wikilink")
  - [H.264](../Page/H.264.md "wikilink")

### 関連団体

  - [MPEG LA](https://ja.wikipedia.org/wiki/MPEG_LA "wikilink")
  - [SMPTE](../Page/SMPTE.md "wikilink")

### その他

  - [Windows Media Player](../Page/Windows_Media_Player.md "wikilink")
  - [ffdshow](https://ja.wikipedia.org/wiki/ffdshow "wikilink")
  - [FairUse4WM](https://ja.wikipedia.org/wiki/FairUse4WM "wikilink")

## 外部リンク

  - [Microsoft Windows Media - 9 シリーズのコーデック - ビデオ](http://www.microsoft.com/japan/windows/windowsmedia/9series/codecs/video.aspx)
  - [MPEGラボ 第23回 Microsoftが標準規格化を目指す「Windows Media Video 9」の仕組み](http://www.mpeg.co.jp/libraries/mpeg_labo/winPC_23.html)
  - [SMPTE](http://www.smpte.org/)
  - [MPEGLA](http://www.mpegla.com/)
  - [Windows Media Video 9 VCM](http://www.microsoft.com/japan/windows/windowsmedia/9series/codecs/vcm.aspx)
  - [Windows Media エンコーダ](http://www.microsoft.com/japan/windows/windowsmedia/download/encode.aspx)
  - [AzWM9 Script Frontend](http://hp.vector.co.jp/authors/VA033749/azwm9sf.html)
  - [WmvTool](http://tsukino-utage.homeip.net/)

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:Windows_Media](https://ja.wikipedia.org/wiki/Category:Windows_Media "wikilink")

1.  [Using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec](http://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)