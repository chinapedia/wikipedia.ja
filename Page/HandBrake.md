> この記事は[HandBrake](https://ja.wikipedia.org/wiki/HandBrake)から翻訳されています。


**HandBrake**（ハンドブレイク/ハンドブレーキ\[1\]）は[DVD](../Page/DVD.md "wikilink")等の動画ファイルを[MPEG-4](../Page/MPEG-4.md "wikilink")ビデオに変換する[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")、[オープンソース](../Page/オープンソース.md "wikilink")、[GPLライセンス](../Page/GNU_General_Public_License.md "wikilink")、[マルチ・スレッド](../Page/スレッド_\(コンピュータ\).md "wikilink")、[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")のトランスコーダーソフトである。[BeOS](../Page/BeOS.md "wikilink")のために開発されたが、現在では[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[Windowsで利用できる](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

## インプット（入力）

バージョン0.9.5からコピープロテクトされていない[BDMV](https://ja.wikipedia.org/wiki/BDMV "wikilink") (BD-Video) フォーマット（構造）の入力がサポートされた。

  - [DVD-Video](../Page/DVD-Video.md "wikilink")フォーマット（プロテクトされた一部のものを除く）
      - 物理ドライブおよび仮想ドライブ
      - ディスクイメージファイル
      - VOBフォーマットファイル
      - VIDEO_TSフォルダ
  - [BDMV](https://ja.wikipedia.org/wiki/BDMV "wikilink") (BD-Video) フォーマット（コピープロテクトされていないものに限る）
      - 物理ドライブおよび仮想ドライブ
      - ディスクイメージファイル
      - [MPEG-2 TS](https://ja.wikipedia.org/wiki/MPEG-2_システム "wikilink") (M2TS) フォーマットファイル
      - BDMVフォルダ
  - [MPEG-4](../Page/MPEG-4.md "wikilink")フォーマット
  - [Matroska](https://ja.wikipedia.org/wiki/Matroska "wikilink") (MKV) フォーマット
  - [Audio Video Interleave](https://ja.wikipedia.org/wiki/Audio_Video_Interleave "wikilink") (AVI) フォーマット
  - [Ogg Media](https://ja.wikipedia.org/wiki/Ogg_Media "wikilink") (OGM) フォーマット

など

## アウトプット（出力）

バージョン0.9.5からは[MPEG-4](../Page/MPEG-4.md "wikilink")フォーマット (.mp4) と[Matroska](https://ja.wikipedia.org/wiki/Matroska "wikilink")フォーマット (.mkv) での出力がサポートされた。バージョン0.9.4以降、フォーマットの機能不足などによる理由から[Audio Video Interleaveフォーマット](https://ja.wikipedia.org/wiki/Audio_Video_Interleave "wikilink") (.avi) と[Ogg Mediaフォーマット](https://ja.wikipedia.org/wiki/Ogg_Media "wikilink") (.ogm) の出力はサポートから外れた（取扱中止）。バージョン0.10.5で、ライセンスの問題から fdk-aac が削除。各[コーデック](../Page/コーデック.md "wikilink")に続く括弧はそのコーデックの利用ライブラリを示す。

  -
    {| class="wikitable" style="text-align:center"

|+出力できるコーデックとコンテナ \! colspan="2" |コーデック \!MPEG-4 フォーマット \!Matroska フォーマット |- \! rowspan="7" | ビデオ |[H.264](https://ja.wikipedia.org/wiki/H.264 "wikilink") ([x264](https://ja.wikipedia.org/wiki/x264 "wikilink"))||○||○ |- |H.264 ([Intel Quick Sync Video](https://ja.wikipedia.org/wiki/Intel_Quick_Sync_Video "wikilink"))||○||○ |- |[H.265](https://ja.wikipedia.org/wiki/H.265 "wikilink") ()||○||○ |- |[MPEG-4](../Page/MPEG-4.md "wikilink") ([ffmpeg](../Page/FFmpeg.md "wikilink"))||○||○ |- |[MPEG-2](../Page/MPEG-2.md "wikilink") (ffmpeg)||○||○ |- |[VP8](https://ja.wikipedia.org/wiki/VP8 "wikilink") (Libvpx)||×||○ |- |[VP3](https://ja.wikipedia.org/wiki/VP3 "wikilink") ([Theora](https://ja.wikipedia.org/wiki/Theora "wikilink"))||×||○ |- \! rowspan="6" |オーディオ |[AAC](../Page/AAC.md "wikilink") ([Libav](https://ja.wikipedia.org/wiki/Libavcodec "wikilink"))||○||○ |- |[MP3](../Page/MP3.md "wikilink") ([LAME](https://ja.wikipedia.org/wiki/LAME "wikilink"))||○||○ |- |[AC3](../Page/ドルビーデジタル.md "wikilink") (Libav)||○||○ |- |[DTS](https://ja.wikipedia.org/wiki/DTS_\(サウンドシステム\) "wikilink")、[DTS-HD](https://ja.wikipedia.org/wiki/DTS-HDマスターオーディオ "wikilink")||△||△ |- |[Vorbis](https://ja.wikipedia.org/wiki/Vorbis "wikilink")||×||△ |- |[FLAC](../Page/FLAC.md "wikilink") (16bit/24bit)||×||△ |}

  -

      -
        ○：エンコード、パススルー両方可能
        △：パススルーのみ可能
        ×：不可

## 主な特徴および機能

  - チャプター
      - チャプターおよびタイトル単位でのコンバートが可能
      - チャプター情報の埋め込み
  - 字幕
      - ソフト字幕（フレームに焼きこまない）
      - 表示・非表示を切り替え可能な字幕
      - [SRT](https://ja.wikipedia.org/wiki/SRT "wikilink")フォーマットの字幕データのインポートおよびパススルー
      - [SSA](https://ja.wikipedia.org/wiki/SSA "wikilink")フォーマットの字幕データのパススルーおよび焼きこみ
      - なお、ブルーレイのイメージベースのPGS字幕はMatroskaフォーマットにおいてのみ、ソフト字幕に対応する。これは、MPEG-4フォーマットがイメージベースのソフト字幕に対応していないためである。MPEG-4フォーマットでPGSから字幕を入れる場合、常にハード字幕（フレームに焼き込まれる）になる。
  - ビデオフィルタ
      - デテレシネ（逆テレシネ化）
      - デコーム（櫛状ノイズを除去）
      - デインターレース（インタレースを除去）
      - デノイズ（ノイズを除去）
      - デブロッキング
      - グレースケール（モノクロ化）
  - 固定フレームレート (CFR) もしくは可変フレームレート (VFR) によるコンバート

<!-- end list -->

  -
    可変フレームレート (VFR) を採用したビデオは[VLC Media Playerや](https://ja.wikipedia.org/wiki/VLC_Media_Player "wikilink")[iOSといった仕様に準拠したごく一部のプレイヤーでしか正確に再生できないので注意が必要である](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")。例えば[QuickTime](../Page/QuickTime.md "wikilink") Player、[プレイステーション3などでは音ズレが発生し正しく再生できない](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")。

<!-- end list -->

  - ビデオクロップ
  - 画質一定コンバートもしくは画質不定・平均ビットレートコンバート
  - キューへの追加によるコンバートのバッチ処理
  - ビデオプレビュー
  - エンコードプリセット

<!-- end list -->

  -
    様々なデバイス、再生環境に適したビデオを作成するためのエンコード設定をプリセット搭載されている。

## 脚注

## 外部リンク

  - [HandBrakeホームページ](http://handbrake.fr/)
  - [HandBrake日本語化プロジェクト](http://sourceforge.jp/projects/handbrake-jp/wiki/FrontPage)

[Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink")

1.  海外製ソフトであるため正式なカタカナ表記は定まっていない。ハンドブレイク表記はBreak(壊す)の誤読としばしば勘違いされるが、Brake(ブレーキ)とBreak(壊す)は同音異字で発音はブレイクが近い、英語発音でハンドブレイクと表記する人がいる一方、日本語発音でハンドブレーキと表記する人もいるがどちらも間違いではない。