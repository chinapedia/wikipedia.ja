> この記事は[Matroska](https://ja.wikipedia.org/wiki/Matroska)から翻訳されています。


**Matroska**（、**マトロスカ**、**マトリョーシカ**）は、[マルチメディア](../Page/マルチメディア.md "wikilink")[コンテナフォーマット](../Page/コンテナフォーマット.md "wikilink")。

## 概要

Matroskaは[映像](https://ja.wikipedia.org/wiki/映像 "wikilink")、[音声](https://ja.wikipedia.org/wiki/音声 "wikilink")、[字幕](https://ja.wikipedia.org/wiki/字幕 "wikilink")などの[データ](../Page/データ.md "wikilink")を格納するためのマルチメディアコンテナフォーマットで、一般的には「.mkv」ファイル（Matroska Video）や「.mka」ファイル（Matroska Audio）として知られている。[ロシア](../Page/ロシア.md "wikilink")の入れ子人形[マトリョーシカにちなんで名付けられた](https://ja.wikipedia.org/wiki/マトリョーシカ人形 "wikilink")。[オープンソース](../Page/オープンソース.md "wikilink")（[GNU LGPL](../Page/GNU_Lesser_General_Public_License.md "wikilink")）で開発が行われている。

[EBML](https://ja.wikipedia.org/wiki/#EBML "wikilink")（Extensible Binary Meta Language）というデータ格納技術を採用し、後方[互換性](https://ja.wikipedia.org/wiki/互換性 "wikilink")と拡張性を両立させている。 [家電の](../Page/家庭用電気機械器具.md "wikilink")[DVDプレーヤー](https://ja.wikipedia.org/wiki/DVDプレーヤー "wikilink")等でも一部対応した機種が存在する。 [DivX](https://ja.wikipedia.org/wiki/DivX "wikilink")7が標準コンテナとしてMatroskaを採用している。 [Google](../Page/Google.md "wikilink")社の動画規格[WebM](https://ja.wikipedia.org/wiki/WebM "wikilink")のコンテナとしてMatroskaのサブセットを採用している。

2014年、[Microsoft Windows 10がMatroskaに標準対応することが](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")[マイクロソフト](../Page/マイクロソフト.md "wikilink")社から発表された。

## 主な特徴

### 共通

  - 多種多様な[コーデック](../Page/コーデック.md "wikilink")に対応。
      - 動画：[VFW Codec](https://ja.wikipedia.org/wiki/Audio_Video_Interleave "wikilink"), [QuickTime Codec](../Page/QuickTime.md "wikilink"), [Motion JPEG](../Page/Motion_JPEG.md "wikilink"), [MPEG-1](../Page/MPEG-1.md "wikilink")/[-2](../Page/MPEG-2.md "wikilink")/[-4](../Page/MPEG-4.md "wikilink"), [H.264](https://ja.wikipedia.org/wiki/H.264 "wikilink"), [H.265](https://ja.wikipedia.org/wiki/H.265 "wikilink"), [RealVideo](https://ja.wikipedia.org/wiki/RealVideo "wikilink"), [Snow](../Page/Snow_\(コーデック\).md "wikilink"), [Theora](https://ja.wikipedia.org/wiki/Theora "wikilink"), [VC-1](https://ja.wikipedia.org/wiki/VC-1 "wikilink"), [VP8](https://ja.wikipedia.org/wiki/VP8 "wikilink"), [VP9](https://ja.wikipedia.org/wiki/VP9 "wikilink"), [AV1](https://ja.wikipedia.org/wiki/AOMedia_Video_1 "wikilink")
      - 音声：[AAC](../Page/AAC.md "wikilink"), [AC-3](../Page/ドルビーデジタル.md "wikilink"), [DTS](https://ja.wikipedia.org/wiki/デジタル・シアター・システムズ "wikilink"), [MP3](../Page/MP3.md "wikilink"), [MP2](https://ja.wikipedia.org/wiki/MP3#MPEG-1/2_Audio_Layer-2 "wikilink"), [Vorbis](https://ja.wikipedia.org/wiki/Vorbis "wikilink"), [Opus](https://ja.wikipedia.org/wiki/Opus_\(音声圧縮\) "wikilink"), [PCM](../Page/パルス符号変調.md "wikilink"), [RealAudio](../Page/RealAudio.md "wikilink"), [FLAC](../Page/FLAC.md "wikilink"), [TTA](https://ja.wikipedia.org/wiki/TTA "wikilink"), [WavPack](https://ja.wikipedia.org/wiki/WavPack "wikilink")

### MKV（Matroska Video File）

  - 複数音声
  - 前参照フレーム（Bフレーム）に対応
  - [チャプター](https://ja.wikipedia.org/wiki/チャプター "wikilink")（頭出し機能。1/1000秒単位で設定可能）
  - 可変[フレームレート](https://ja.wikipedia.org/wiki/フレームレート "wikilink")（VFR）対応
  - 高度な字幕機能（テキスト型、VisualBob型両対応）
  - [アスペクト比](../Page/アスペクト比.md "wikilink")指定
  - 映像、音声、字幕以外のファイル添付
  - [DVD-Video](../Page/DVD-Video.md "wikilink")のようなメニュー（未実装）

### MKA（Matroska Audio File）

  - [アルバム](../Page/アルバム.md "wikilink")化（複数の曲を一つのファイルに入れ、順番に再生）
  - 時間が同じでないファイルの多重化
  - 異なるコーデックの音声を収録可能

## EBML

**EBML（Extensible Binary Meta Language）**は[XMLを基に作られた](../Page/Extensible_Markup_Language.md "wikilink")、拡張性に優れたデータ格納方式である。

[HTML](../Page/HyperText_Markup_Language.md "wikilink")、XMLの様にタグ形式（正確には[バイナリ](../Page/バイナリ.md "wikilink")の擬似形式）で記述されており、対応していない機能においては無視するようになっている。

従って、新機能の追加においても互換性を落とすことなく対応させることができ、なおかつ、[不具合](https://ja.wikipedia.org/wiki/不具合 "wikilink")の起きにくい設計にすることを可能にした。

## 拡張子

  - `.mkv` Matroska Video（映像）
  - `.mka` Matroska Audio（音声のみ）
  - `.mks` Matroska Subtitles（字幕のみ）
  - `.mk3d` Matroska 3D（3D映像）

## CodecIDの例

### ビデオ

  - V_MPEG4/ISO/AVC（H.264/MPEG-4 AVC）

### オーディオ

  - A_AAC/MPEG4/LC（AAC-LC）

## 対応ソフト

以下の「SSA」は「Sub Station Alpha」、「ASS」は「Advanced SSA」と呼ばれる字幕のファイルフォーマットである。

### メディアプレーヤー

<table>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>OS</p></th>
<th><p>SSA/ASSサポート</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/ALLPlayer" title="wikilink">ALLPlayer</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows" title="wikilink">Windows</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/ALShow" title="wikilink">ALShow</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>BS.Player</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Chameleo" title="wikilink">Chameleo</a></p></td>
<td><p><a href="../Page/クロスプラットフォーム.md" title="wikilink">クロスプラットフォーム</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/CorePlayer" title="wikilink">CorePlayer</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/DivX" title="wikilink">DivX Player</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/PotPlayer" title="wikilink">Daum PotPlayer</a></p></td>
<td><p>Windows</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/GOM_Player.md" title="wikilink">GOM Player</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Gstreamer" title="wikilink">Gstreamer</a>ベースのプレイヤー<br />
</p></td>
<td><p>クロスプラットフォーム</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/jetAudio" title="wikilink">jetAudio</a></p></td>
<td><p>Windows</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Kantaris</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/The_KMPlayer" title="wikilink">The KMPlayer</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/TotalMedia_Theatre" title="wikilink">TotalMedia Theatre</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Media_Player_Classic" title="wikilink">Media Player Classic</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/MPlayer.md" title="wikilink">MPlayer</a></p></td>
<td><p>クロスプラットフォーム</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/MPlayer_Extended" title="wikilink">MPlayer Extended</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/macOS" title="wikilink">macOS</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Nero_(software_suite)" title="wikilink">ShowTime</a></p></td>
<td><p>Windows</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/SMPlayer" title="wikilink">SMPlayer</a></p></td>
<td><p>クロスプラットフォーム</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Target_Longlife_Media_Player" title="wikilink">Target Longlife Media Player</a></p></td>
<td><p>Windows</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/The_Core_Pocket_Media_Player" title="wikilink">The Core Pocket Media Player</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Windows_Mobile" title="wikilink">Windows Mobile</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/VLCメディアプレーヤー.md" title="wikilink">VLC media player</a></p></td>
<td><p>クロスプラットフォーム</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/xine" title="wikilink">xine</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Zoom_Player" title="wikilink">Zoom Player</a></p></td>
<td><p>Windows</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/ビデオ_(GNOME).md" title="wikilink">GNOME ビデオ</a></p></td>
<td><p><a href="../Page/Unix系.md" title="wikilink">Unix系</a></p></td>
<td></td>
</tr>
</tbody>
</table>

### メディアセンター

| 名前                                                                            | OS                                    | SSA/ASSサポート                         |
| ----------------------------------------------------------------------------- | ------------------------------------- | ----------------------------------- |
| [Boxee](https://ja.wikipedia.org/wiki/Boxee "wikilink")                       | クロスプラットフォーム                           | [1](http://www.boxee.tv/)           |
| [DivX Connected](https://ja.wikipedia.org/wiki/DivX_Connected "wikilink")     | Windows                               | [2](http://www.divx.com/connected/) |
| [MediaPortal](http://www.team-mediaportal.com/content/view/42/117/)           | [3](http://www.team-mediaportal.com/) |                                     |
| [Moovida](https://ja.wikipedia.org/wiki/Moovida "wikilink")                   | クロスプラットフォーム                           | [4](http://www.moovida.com/)        |
| [MythTV](https://ja.wikipedia.org/wiki/MythTV "wikilink")                     | [Linux](../Page/Linux.md "wikilink")  | [5](http://www.mythtv.org/)         |
| [Plex](https://ja.wikipedia.org/wiki/Plexapp "wikilink")                      | macOS                                 | [6](http://plexapp.com/)            |
| [PS3 Media Server](https://ja.wikipedia.org/wiki/PS3_Media_Server "wikilink") | クロスプラットフォーム                           | [7](http://ps3mediaserver.org/)     |
| [Xbmc](https://ja.wikipedia.org/wiki/Xbmc "wikilink")                         | [8](http://xbmc.org/)                 |                                     |

### ツール

<table>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>OS</p></th>
<th><p>SSA/ASSサポート</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Avidemux" title="wikilink">Avidemux</a></p></td>
<td><p>クロスプラットフォーム</p></td>
<td><p><a href="http://www.avidemux.org/">9</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Conceiva" title="wikilink">Conceiva</a><br />
<a href="https://ja.wikipedia.org/wiki/ConvertHQ" title="wikilink">ConvertHQ</a></p></td>
<td><p>Windows</p></td>
<td><p><a href="http://www.conceiva.com/products/converthq/default.asp">10</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/HandBrake.md" title="wikilink">HandBrake</a></p></td>
<td><p>クロスプラットフォーム</p></td>
<td><p><a href="http://handbrake.fr/">11</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/iFunia_Video_Converter" title="wikilink">iFunia Video Converter</a></p></td>
<td><p>macOS</p></td>
<td><p><a href="http://www.ifunia.com/mkv-converter-mac.html">12</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/DivX_Converter" title="wikilink">DivX Converter</a></p></td>
<td><p>クロスプラットフォーム</p></td>
<td><p><a href="http://www.divx.com/">13</a></p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/FFmpeg.md" title="wikilink">FFmpeg</a></p></td>
<td><p><a href="http://www.ffmpeg.org/">14</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/FormatFactory" title="wikilink">FormatFactory</a></p></td>
<td><p>Windows</p></td>
<td><p><a href="http://www.formatoz.com/">15</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/iVerio_Software" title="wikilink">iVerio Software</a> Video Converter for Camcorders</p></td>
<td><p>クロスプラットフォーム</p></td>
<td><p><a href="http://www.iverio-convertmod.com/">16</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/MediaCoder.md" title="wikilink">MediaCoder</a></p></td>
<td><p>Windows</p></td>
<td><p><a href="http://www.mediacoderhq.com/">17</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/MKVToolnix" title="wikilink">MKVToolnix</a></p></td>
<td><p>クロスプラットフォーム</p></td>
<td><p><a href="http://www.bunkus.org/videotools/mkvtoolnix/">18</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/MKV2VOB" title="wikilink">MKV2VOB</a> for converting MKV for playback on PS3 etc</p></td>
<td><p>Windows</p></td>
<td><p><a href="http://www.mkv2vob.com/">19</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Perian" title="wikilink">Perian</a> Quicktime Plugin for Mac OS X</p></td>
<td><p>macOS</p></td>
<td><p><a href="http://perian.org/">20</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/SUPER_(ソフトウェア).md" title="wikilink">SUPER</a></p></td>
<td><p>Windows</p></td>
<td><p><a href="http://www.erightsoft.com/SUPER.html/">21</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Total_video_converter" title="wikilink">Total video converter</a></p></td>
<td><p><a href="http://www.effectmatrix.com/">22</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Video_Converter_Ultimate" title="wikilink">Video Converter Ultimate</a></p></td>
<td><p>Windows<br />
<a href="https://ja.wikipedia.org/wiki/Mac_OS" title="wikilink">Mac OS</a></p></td>
<td><p><a href="http://www.imtoo.com/video-converter.html">23</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/VirtualDubMod" title="wikilink">VirtualDubMod</a></p></td>
<td><p>Windows</p></td>
<td><p><a href="http://virtualdubmod.sourceforge.net/">24</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/MakeMKV" title="wikilink">MakeMKV</a></p></td>
<td><p><a href="http://www.makemkv.com/">25</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/VSO_Software#Products" title="wikilink">ConvertXtoDVD</a></p></td>
<td><p><a href="http://www.vso-software.fr/">26</a></p></td>
<td></td>
</tr>
</tbody>
</table>

## 脚注

## 関連項目

### ソフトウェア

  - [Combined Community Codec Pack](../Page/Combined_Community_Codec_Pack.md "wikilink")
  - [Haali Media Splitter](../Page/Haali_Media_Splitter.md "wikilink")
  - [VLC media player](https://ja.wikipedia.org/wiki/VLC_media_player "wikilink")
  - [Media Player Classic](https://ja.wikipedia.org/wiki/Media_Player_Classic "wikilink")
  - [GOM Player](../Page/GOM_Player.md "wikilink")
  - [ratDVD](https://ja.wikipedia.org/wiki/ratDVD "wikilink")
  - [MPlayer](../Page/MPlayer.md "wikilink")
  - [ビデオ (GNOME)](../Page/ビデオ_\(GNOME\).md "wikilink")
  - [FFmpeg](../Page/FFmpeg.md "wikilink")（ffplay）

### その他

  - [ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")
  - [コンテナフォーマット](../Page/コンテナフォーマット.md "wikilink")
  - [ファンサブ](https://ja.wikipedia.org/wiki/ファンサブ "wikilink")
  - [MADムービー](../Page/MADムービー.md "wikilink")
  - [マトリョーシカ人形](https://ja.wikipedia.org/wiki/マトリョーシカ人形 "wikilink")

## 外部リンク

  -

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:動画ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:動画ファイルフォーマット "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink") [Category:マルチメディア](https://ja.wikipedia.org/wiki/Category:マルチメディア "wikilink")