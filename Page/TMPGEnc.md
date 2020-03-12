> この記事は[TMPGEnc](https://ja.wikipedia.org/wiki/TMPGEnc)から翻訳されています。


**TMPGEnc**（ティーエムペグエンク）は、現在は株式会社ペガシスが販売している[MPEG](https://ja.wikipedia.org/wiki/MPEG "wikilink")映像作成・編集[ソフトウェア](../Page/ソフトウェア.md "wikilink")、及びそのシリーズの名称である。[Microsoft Windows用のみ](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。**T**sunami **MP**E**G** **Enc**oderの略。

## 歴史

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")頃に堀浩行が1人で開発を始めた。当時堀は17歳だったという。[MPEG-1](../Page/MPEG-1.md "wikilink")圧縮ソフトとして始まり、[ビデオCD](../Page/ビデオCD.md "wikilink")や[MPEG-2](../Page/MPEG-2.md "wikilink")フォーマットに対応するなど改良した。[フリーウェア](../Page/フリーウェア.md "wikilink")でありながら高画質・高機能で、一般ユーザーに広い支持を受けるのみならず、ゲームソフトのムービー作成などプロにも使用されてきた。『[グランツーリスモ3](../Page/グランツーリスモ_\(ゲーム\).md "wikilink")』や『[鬼武者](../Page/鬼武者.md "wikilink")』などで採用されたことが知られている。

[2000年](../Page/2000年.md "wikilink")、フリーウェアでMPEG-2作成機能を備えることは[MPEG-LA](https://ja.wikipedia.org/wiki/MPEG-LA "wikilink")の特許に抵触するというクレームがつき、MPEG-2への対応が外される影響が出た。[2001年](../Page/2001年.md "wikilink")に[プロジー](../Page/プロジー.md "wikilink")（後に[ライブドア](../Page/ライブドア.md "wikilink")に吸収）からMPEG-2対応など高機能な有料版「TMPGEnc Professional」の発売が決まったが、結局実現しなかった。

2001年、堀らが株式会社ペガシスを設立し、MPEG-2に対応した「TMPGEnc Plus」を発売した。MPEG-2作成機能を期限付きにした無料版TMPGEncも引き続き公開されている。

その後、[DVD-Video](../Page/DVD-Video.md "wikilink")作成ソフト「TMPGEnc DVD Author」、TMPGEncを進化させた「TMPGEnc XPress」、MPEGカット編集ソフト「TMPGEnc MPEG Editor」などを発売。TMPGEncの開発で培ったノウハウを活かし、高機能ながら操作性がシンプルでファンが多い。

また、XPressでは[ストリーミングSIMD拡張命令](../Page/ストリーミングSIMD拡張命令.md "wikilink")など[CPU](../Page/CPU.md "wikilink")の拡張命令 ([SIMD](../Page/SIMD.md "wikilink")) への対応が素早いことでも知られている。さらに2008年には[CUDA](../Page/CUDA.md "wikilink")への対応も果たした。上記のようにエンコードした動画を楽しむ他に、CPUまたはGPUの性能を測る検証目的としても使われることも多い（もっとも他社製品に比べて高速というわけではない）。

近年はハイビジョン映像や[Blu-ray Disc等への対応も進めているが](../Page/Blu-ray_Disc.md "wikilink")、他の動画編集ソフトと同様に[デジタルテレビ放送](../Page/デジタルテレビ放送.md "wikilink")の録画を取り扱うことができず（著作権保護目的で暗号化が施されるため）、本来の力を発揮できていないのが現状である。

XPressにおいて、多数のハイビジョン動画をバッチエンコードしようとするとメモリ不足が発生したり、動作が不安定になる場合がある。これは大量のメモリを必要とするハイビジョン動画エンコードにも関わらず、全バッチ処理を1プロセス上で行っているため、仮想メモリアドレスそのものが足りなくなるためで、メモリ増設をしたり64bitOS上で動かしても解消しない。このような場合で、どうしても同時にエンコードを行いたい場合、バッチエンコードに登録せず、直接エンコードを行うことで解消できる場合がある。この現象はTMPGEnc Video Mastering Worksにおいてはエンコード部をマルチプロセスに改良することによって改善された。

## 製品群

  - TMPGEnc Video Mastering Works
      -
        TMPGEnc XPressの機能を更に大幅進化させたエンコーダ。2011年1月12日に最初のバージョンである5がリリースされた。H.264エンコーダにオープンソース開発の[x264](https://ja.wikipedia.org/wiki/x264 "wikilink")を採用。[MKVファイルや](../Page/Matroska.md "wikilink")[WebM](https://ja.wikipedia.org/wiki/WebM "wikilink")ファイルにも対応している。タイムライン編集にも対応。
  - TMPGEnc Authoring Works
      -
        TMPGEnc DVD Authorの後継として発売されたDVD/BD-Video[オーサリングツール](../Page/オーサリングツール.md "wikilink")。2008年10月に最初のバージョンである4が発売。2012年1月12日に最新版バージョンである5がリリースされる。[BDMV](../Page/BDMV.md "wikilink")形式の書き出しに対応。
  - TMPGEnc MPEG Smart Renderer
      -
        TMPGEnc MPEG Editorの後継として発売されたカット編集ツール。2012年8月に最初のバージョンである4が発売。あらたに[H.264/AVC](https://ja.wikipedia.org/wiki/H.264/AVC "wikilink")のスマートレンダリング（必要最小限の箇所のみ再エンコードして画質の劣化を抑えフレーム単位の編集を可能にする）に対応した。[BDAV](../Page/BDAV.md "wikilink")形式の書き出し・追記も可能。
  - TMPGEnc Movie Plug-in MPEG-2 for EDIUS
      -
        [グラスバレー（旧トムソン・カノープス）の映像編集ソフト](../Page/グラスバレー_\(企業\).md "wikilink")[EDIUS](../Page/EDIUS.md "wikilink")専用。TMPGEncのエンジンを使用してMPEG2出力が可能になる。EDIUSのバージョン毎に別売されている。
        以前は同社のFirecoder Bluや東芝のノートパソコン「[コスミオ](https://ja.wikipedia.org/wiki/コスミオ "wikilink")」等に搭載されている[SpursEngine](https://ja.wikipedia.org/wiki/SpursEngine "wikilink")ハードウェアによる高速化にも対応していた。
  - TMPGEnc Movie Plug-in AVC for EDIUS / Premiere Pro
      -
        前述のTMPGEnc Movie Plug-in MPEG-2 for EDIUSのAVC版。EDIUS用プラグインは対象バージョン毎に別売されている。また、Adobeの[Premiere Pro用プラグインも存在する](../Page/Adobe_Premiere.md "wikilink")。
  - TMPGEnc Movie Plug-in Commercial Candidates Detector
      -
        TMPGEnc Video Mastering Works / Authoring Works用のCM検出プラグイン。
  - TMPGEnc KARMA.. Plus
      -
        動画管理ソフトウェア。
  - TMPGEnc PGMX CREATOR
      -
        ファイルベースの独自動画形式「PGMX」用オーサリングソフト。
  - これらの製品の機能限定版や[OEM](../Page/OEM.md "wikilink")版も複数存在する。

### 開発を終了した製品群

  - TMPGEnc期限付き無料版 / TMPGEnc Plus (有料)
      -
        初期バージョンの流れを汲むエンコーダ。外部のコーデックを使用すれば[DivX](https://ja.wikipedia.org/wiki/DivX "wikilink")などのMPEG以外のエンコードも可能である。2008年5月29日リリースのv2.525が最終バージョン。バージョン3からはXPressへ移行し開発終了したが、3.0 XPressのリリース後も愛用者が多かった。なお、TMPGEnc無料版は現在も入手可能だが、商用利用は禁じられている。2015年9月30日をもってTMPGEnc Plusの販売が終了予定となっている。
  - TMPGEnc XPress
      -
        TMPGEncの機能を大幅に進化させたエンコーダ。2004年に最初のバージョンである3.0 XPress、2006年に4.0 XPressがリリースされた。[ドルビーデジタル](../Page/ドルビーデジタル.md "wikilink")、[WMV](../Page/Windows_Media_Video.md "wikilink")、XDVD（後述）、[HDV](../Page/HDV.md "wikilink")準拠のハイビジョンMPEG-2、[MPEG-4](../Page/MPEG-4.md "wikilink")/[H.264](../Page/H.264.md "wikilink")、[Flash Video](../Page/Flash_Video.md "wikilink")（要・有料プラグイン）など多数のフォーマットに対応する。バージョン5からはVideo Mastering Worksへ移行し、開発終了。
  - TMPGEnc DVD Author
      -
        2003年に発売されたDVD-Video[オーサリングツール](../Page/オーサリングツール.md "wikilink")。TMPGEncの流れを汲む直観的なカット編集機能を持つ。v1.xは評価の高い製品ではなかったが、2005年に発売されたv2.0では編集機能を大幅に進化させスマートレンダリングや[トランスコード](../Page/トランスコード.md "wikilink")（再エンコードに比べて画質劣化を抑えながらビットレートを下げる）機能を搭載した。2006年に「DVD Author 3 with [DivX](https://ja.wikipedia.org/wiki/DivX "wikilink") Authoring」が公開され、DVD-Videoと同様にメニュー機能等を持つDivX Ultraに対応した。バージョン4からはAuthoring Worksへ移行し、開発終了。
  - TMPGEnc MPEG Editor
      -
        TMPGEnc無料版に搭載されていたMPEGカット編集ツールを進化・独立させたソフトウェア。2004年発売。スマートレンダリング（必要最小限の箇所のみ再エンコードして画質の劣化を抑えフレーム単位の編集を可能にする）を搭載。後に[HDV](../Page/HDV.md "wikilink")・[DVD-VR](../Page/DVD-VR.md "wikilink")・[BDAV](../Page/BDAV.md "wikilink")形式の編集・書き出しにも対応。
  - 萌えぺぐえんく
      -
        TMPGEnc XPress/TMPGEnc DVD Authorをベースに[アニメ](../Page/アニメ.md "wikilink")の圧縮に特化したエンコーダ。[丸紅インフォテック](https://ja.wikipedia.org/wiki/丸紅インフォテック "wikilink")が発売。
  - Movie to Portable / TMPGEnc Movie Style
      -
        [iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")・[PSPなど外部機器との連携に特化したエンコーダ](../Page/PlayStation_Portable.md "wikilink")。

## 関連事項

  - XDVD
      -
        MPEG-2の[GOPの長さをDVD](https://ja.wikipedia.org/wiki/Group_Of_Pictures "wikilink")-Video準拠の18フレームから60フレーム以上に拡張した独自規格。DVD-Videoの規格からは外れているが一般的なDVDプレーヤーで再生できる場合が多い。圧縮率を最大2倍にまで高めることができ、特に低ビットレートで効果が高いが、エンコードが低速なことやDivX・MPEG-4等に比べてメリットが少ないことなどでほとんど普及していない。
  - L.E.A.P.System
      -
        2004年以降のTMPGEncシリーズで導入された[アクティベーション](../Page/アクティベーション.md "wikilink")システム。インターネット認証を利用した強固な海賊版対策を施しているが、既に[クラック](https://ja.wikipedia.org/wiki/クラック "wikilink")されネット認証をスキップできる[海賊版](https://ja.wikipedia.org/wiki/海賊版 "wikilink")が出回るようになった。外販されているが導入事例は多くない。[RPGツクールXP](../Page/RPGツクールXP.md "wikilink")/[VXが本システムを採用している](../Page/RPGツクールVX.md "wikilink")。

## 注釈

## 関連項目

  - [動画編集ソフトウェア](https://ja.wikipedia.org/wiki/動画編集ソフトウェア "wikilink")
  - [Avidemux](https://ja.wikipedia.org/wiki/Avidemux "wikilink")

## 外部リンク

  - [株式会社ペガシス](http://www.pegasys-inc.com/ja/)
  - [TMPGEnc.net](http://www.tmpgenc.net/) （TMPGEnc無料版、サポート掲示板など）
  - [Hori Homepage](http://www.yks.ne.jp/~hori/) （開発者・堀浩行のホームページ。更新は2002年まで）
  - [Impress AV Watch - 小寺信良の週刊Electric Zooma\! 第50回](https://av.watch.impress.co.jp/docs/20020306/zooma50.htm) （開発者へのインタビュー 2002年3月6日）

[Category:画像処理ソフト](https://ja.wikipedia.org/wiki/Category:画像処理ソフト "wikilink") [Category:映像編集・合成ソフト](https://ja.wikipedia.org/wiki/Category:映像編集・合成ソフト "wikilink") [Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink") [Category:アプリケーションソフト_(製品)](https://ja.wikipedia.org/wiki/Category:アプリケーションソフト_\(製品\) "wikilink") [Category:Blu-ray_Disc関連のソフト](https://ja.wikipedia.org/wiki/Category:Blu-ray_Disc関連のソフト "wikilink") [Category:DVD関連のソフト](https://ja.wikipedia.org/wiki/Category:DVD関連のソフト "wikilink")