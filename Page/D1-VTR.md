> この記事は[D1-VTR](https://ja.wikipedia.org/wiki/D1-VTR)から翻訳されています。


[Sony_DVR-2000_20070525.jpg](https://ja.wikipedia.org/wiki/File:Sony_DVR-2000_20070525.jpg "fig:Sony_DVR-2000_20070525.jpg") [BOSCH_BTS_D1_DCR_500.jpg](https://ja.wikipedia.org/wiki/File:BOSCH_BTS_D1_DCR_500.jpg "fig:BOSCH_BTS_D1_DCR_500.jpg")

**D1-VTR**とは[ITU-R BT.601フォーマット](https://ja.wikipedia.org/wiki/:en:Rec._601 "wikilink")（4:2:2[コンポーネント方式](../Page/コンポーネント映像信号.md "wikilink")）で符号化された[デジタル](../Page/デジタル.md "wikilink")ビデオ信号を、19mm(約3/4インチ)カセットテープに非圧縮で記録する放送業務用[VTRである](../Page/ビデオテープレコーダ.md "wikilink")。

## 概要

1982年に日米欧で共通のデジタルビデオ記録・伝送フォーマットを策定する目的で標準化が行われた。この結果決まった4:2:2コンポーネント符号化規格がCCIR 601、現在のITU-R BT.601である。 ITU-R BT.601規格の[サンプリング](../Page/サンプリング.md "wikilink")（標本化）周波数は、輝度信号Yが13.5MHz、色差信号R-Y,B-Yが各々6.75MHzである。ITU-R BT.601規格に則った信号（D1-VTRの入出力インターフェース信号）を「D1信号」と呼ぶこともある。

続いてこの方式による放送業務用VTRの規格化が行われ、1986年にCCIR 657として制定後、[ソニー](../Page/ソニー.md "wikilink")と[BTS](https://ja.wikipedia.org/wiki/:en:Broadcast_Television_Systems_Inc. "wikilink")（フィリップスとの合弁放送機器メーカー、その後フランスのThomsonに買収され現在はThomson Grass Valleyが継承）が対応するVTRを発売した。

[SDTV](../Page/SDTV.md "wikilink")用VTRとしては最高画質であり、[テレビコマーシャル](https://ja.wikipedia.org/wiki/テレビコマーシャル "wikilink")の[編集や](../Page/映像編集.md "wikilink")[コンピュータグラフィックス](../Page/コンピュータグラフィックス.md "wikilink")の出力など高画質を要求される分野で用いられたが、放送局では機器が高価なこと（VTRだけでなく編集設備もコンポーネント信号に対応させる必要がある、[コンポジット映像信号](../Page/コンポジット映像信号.md "wikilink")用機器も残るので変換機器が必要など）、ビデオテープのランニングコストが高いことなどから[D2-VTR](../Page/D2-VTR.md "wikilink")の方が普及した。

D1-VTRの入出力インターフェースの物理規格は、当初ECLレベルのパラレル式([ITU-R BT.656](https://ja.wikipedia.org/wiki/:en:ITU-R_BT.656 "wikilink"))であったが、ソニーが[同軸ケーブル](../Page/同軸ケーブル.md "wikilink")を用いた[シリアル伝送方式を開発](../Page/シリアル通信.md "wikilink")・普及させた（[SMPTE 259Mとして規格化](https://ja.wikipedia.org/wiki/:en:SMPTE_259M "wikilink")。**[SDI](https://ja.wikipedia.org/wiki/:en:SMPTE_259M "wikilink")**と略される。）ため、のちの[圧縮技術を用いた放送業務用デジタルVTRの多くが](../Page/データ圧縮.md "wikilink")[SDIをインターフェース規格として採用した](https://ja.wikipedia.org/wiki/:en:SMPTE_259M "wikilink")。また、プロダクションスイッチャ等のビデオ編集・制作機器も「D1信号」および「SDI」に対応した製品が普及している。

## D1 フォーマット概要

※525/59.94/2：1[インターレース方式の場合を](../Page/走査.md "wikilink")“525”、625/50/2：1インターレース方式の場合を“625”と付記。

  - 記録方式：[ヘリカルスキャン方式](../Page/ヘリカルスキャン方式.md "wikilink")
  - ヘッドドラム回転数：150Hz/1.001（525）／150Hz（625）（9,000rpm）
  - 記録ヘッド数：4
  - 総トラック数/sec：600track/sec（10track/Field：525／12track/Field：625）
  - ヘッドドラム径：75mm
  - 巻き付け角：約270°
  - ヘッド相対速度：約35.6m/s
  - 記録トラック幅：35μm
  - トラックピッチ：45μm（内、ガードバンド10μm）
  - アジマス角：0°
  - カセットテープサイズ: 254×150×33mm（M）、他にLとSがあり
  - テープ磁性体：酸化鉄塗布型（保磁力：850 Oe）
  - テープ幅：19mm（約3/4インチ）
  - テープ厚：16μmまたは13μm
  - テープ送り速度：約286.6mm/s
  - 記録時間：94分（13μmテープ、Lカセット）
  - 信号記録方式：デジタル記録
      - 情報源[符号化方式](../Page/符号化方式.md "wikilink")：
          - 映像：4:2:2コンポーネントデジタル \* 8bit量子化 \* 8-8変換（非圧縮）
              - 映像帯域幅（±0.1dB） - Y：5.75MHz、B-Y/R-Y：2.75MHz
              - 標本化周波数 - Y：13.5MHz、B-Y/R-Y：6.75MHz
              - 総サンプル数/line - 858（525）／ 864（625）
              - 有効サンプル数/line - 720（525／625）
              - 総記録ライン数/Frame- 500（525）／ 600（625）
          - 音声：非圧縮 48kHz/20ビット直線量子化×4ch \*2重書き
      - チャネル記録速度：約80Mbps/ヘッド（正味、約176Mbps）
      - 記録（チャネル）符号化方式：スクランブルドNRZ\*RS積符号（Inner\[60,64\]/Outer\[30,32\]）

## 規格名称

  - CCIR 657：CCIR Recommendation 657：Digital Television Tape Recording
  - SMPTE 224M：[SMPTE](../Page/SMPTE.md "wikilink")による記録方式規格
  - SMPTE 225M：磁気テープ規格
  - SMPTE 226M：テープカセット規格（D1/D2共通）
  - SMPTE 227M：テープへの記録フォーマット（映像データ）
  - SMPTE 228M：同上（[タイムコード](https://ja.wikipedia.org/wiki/タイムコード "wikilink")、制御、キューデータ）
  - SMPTE 125M：パラレルインターフェース規格
  - [SMPTE 259M](https://ja.wikipedia.org/wiki/:en:SMPTE_259M "wikilink")：[シリアルデジタルインターフェイス](https://ja.wikipedia.org/wiki/シリアルデジタルインターフェイス "wikilink")規格

## 関連項目

  - [D2-VTR](../Page/D2-VTR.md "wikilink")
  - [D3-VTR](https://ja.wikipedia.org/wiki/D3-VTR "wikilink")
  - [D5-VTR](../Page/D5-VTR.md "wikilink")
  - [D6-VTR](https://ja.wikipedia.org/wiki/D6-VTR "wikilink")
  - [HDCAM](../Page/HDCAM.md "wikilink")
  - [DVCPRO](../Page/DVCPRO.md "wikilink")
  - [P2](../Page/P2.md "wikilink")
  - [D-VHS](../Page/D-VHS.md "wikilink")
  - [W-VHS](../Page/W-VHS.md "wikilink")

[Category:ビデオテープ](https://ja.wikipedia.org/wiki/Category:ビデオテープ "wikilink") [Category:ビデオストレージ](https://ja.wikipedia.org/wiki/Category:ビデオストレージ "wikilink")