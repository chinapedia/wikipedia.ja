> この記事は[Digital Visual Interface](https://ja.wikipedia.org/wiki/Digital_Visual_Interface)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:DVI_Diagram.svg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:DVI_Connector.jpg "wikilink") **Digital Visual Interface**（デジタル ビジュアル インターフェース、**DVI**：ディー ブイ アイ）は、[液晶ディスプレイ](https://ja.wikipedia.org/wiki/液晶ディスプレイ "wikilink")や[デジタル](../Page/デジタル.md "wikilink")[プロジェクタ](../Page/プロジェクタ.md "wikilink")のような、デジタル[ディスプレイ装置の映像品質を最大限活かすよう設計された映像出力](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")[インタフェースの標準](../Page/インタフェース_\(情報技術\).md "wikilink")[規格](https://ja.wikipedia.org/wiki/規格 "wikilink")である。これは**Digital Display Working Group**(DDWG)という、産業界の[コンソーシアム](../Page/コンソーシアム.md "wikilink")によって開発された。この規格は一種のシリアルインターフェイスであり、ディスプレイに無圧縮のデジタルビデオデータを送るように設計され、完全にノイズレスでドットバイドットとなる表示を可能にしている。また、派生規格である[HDMI](https://ja.wikipedia.org/wiki/HDMI "wikilink")は、DVIと部分的に[互換性](../Page/互換性.md "wikilink")がある。DVIは2000年代後半までは唯一のデジタルディスプレイ規格として利用されていたが、後に次世代規格として登場したHDMIやDisplayPortに主流が移行し、古い規格となっている。事実として、次世代規格では対応可能な8Kや4Kに対応出来ないと言う制約がある。DVIはデジタルディスプレイに最適化した規格ではあるが、実用上は従来のD-Subでも画質の劣化を感じない事が多く、機器やケーブル交換の手間を掛ける必要も無い事から、ディスプレイにDVI端子が搭載されていても使わない例も多かった。

## 規格化の背景

DVIインタフェースは各[ピクセル](../Page/ピクセル.md "wikilink")の[輝度](https://ja.wikipedia.org/wiki/輝度 "wikilink")を[バイナリ](../Page/バイナリ.md "wikilink")データとして送信するのにデジタル[プロトコル](../Page/プロトコル.md "wikilink")を用いている。ディスプレイをデバイスの持つ[解像度](../Page/解像度.md "wikilink")で動作させると、ディスプレイはそれぞれの値を読み取って、適切なピクセルに輝度を適用する。この方法だと、ソースのデバイスの出力[バッファ](../Page/バッファ.md "wikilink")（代表的には[ビデオカード](../Page/ビデオカード.md "wikilink")上の[VRAM](../Page/VRAM.md "wikilink")）にあるそれぞれのピクセルとディスプレイデバイス内の1つのピクセルが直接対応する。ところが、[アナログ](../Page/アナログ.md "wikilink")信号ではそれぞれのピクセルの表示は電気的[ノイズ](../Page/ノイズ.md "wikilink")やアナログ信号の[ひずみ](../Page/ひずみ.md "wikilink")などにより隣接するピクセルの影響を受けてしまう。

アナログ[VGA](../Page/Video_Graphics_Array.md "wikilink")（[VGA端子](../Page/VGA端子.md "wikilink")）のような以前の規格は[CRTベースのデバイスに対して設計されていたため](../Page/ブラウン管.md "wikilink")、離散的な時間で伝送していなかった。アナログソースは画像の水平線それぞれを送信する際、望みの明るさを表現するために出力[電圧](../Page/電圧.md "wikilink")を変化させている。CRTデバイス内で、この信号は走査[ビーム](https://ja.wikipedia.org/wiki/ビーム "wikilink")がスクリーンを横切って動く際にその[輝度](https://ja.wikipedia.org/wiki/輝度 "wikilink")を変えるために使っている。

しかし、VGAのようなアナログ信号をLCDのようなデジタルディスプレイに入力すると、個々のピクセルに対して似通った明るさの値が選ばれてしまう可能性がある。これはディスプレイでのデコードサンプリングが（アナログ水平掃引における）それぞれのピクセルのちょうど真ん中のタイミングで行われるとは限らないからである。デコーダは特定の間隔で入力信号の電圧をサンプリングする、つまりある瞬間の値を採用するので、このようなことが起きてしまう。コンピュータのようなデジタルデバイスのソースで、VRAMなどからのエンコードサンプリングはアナログ水平掃引を模したうえでピクセルのちょうど真ん中のタイミングで行わないと、ひずみを引き起こし、[クロストークの原因となる](../Page/漏話.md "wikilink")。

## 技術概要

DVIで用いられているデータ[フォーマット](https://ja.wikipedia.org/wiki/フォーマット "wikilink")は、[半導体](../Page/半導体.md "wikilink")製品メーカーである[Sillicon Image社が提唱した](https://ja.wikipedia.org/wiki/Sillicon_Image "wikilink")**PanelLink**という[シリアル通信](https://ja.wikipedia.org/wiki/シリアル通信 "wikilink")フォーマットを元にしている。PanelLinkを元に**[Transition Minimized Differential Signaling](https://ja.wikipedia.org/wiki/Transition_Minimized_Differential_Signaling "wikilink")** (TMDS) として標準化された規格が既にあり、これがDVI規格に内包された。伝送路は4つの[ツイストペアケーブル](../Page/ツイストペアケーブル.md "wikilink")（赤、緑、青、クロック）で構成され、1ピクセル当たり24[ビット](../Page/ビット.md "wikilink")（[フルカラー](../Page/フルカラー.md "wikilink")）を伝送する。この伝送路をTMDSリンクと言う。 信号タイミングはアナログ映像信号の垂直同期および水平同期とほとんど正確に合うようになっている。デジタル映像データは、アナログ映像信号の同期タイミングを模して、ライン間や[フレーム間の](../Page/コマ_\(映画・漫画\).md "wikilink")[帰線消去期間](https://ja.wikipedia.org/wiki/帰線消去期間 "wikilink")を含めてラインごとに送信され、[パケット](../Page/パケット.md "wikilink")化は行われない。DVIは[データ圧縮](../Page/データ圧縮.md "wikilink")（例えば変更された画像の部分のみを送るなど）をせず、フレームを構成するデータは常に全量送信される。このTMDSリンクを単一で用いる方式を**シングルリンク**という。

DVI仕様では、シングルリンクにおけるピクセルクロック周波数の最大値は165メガヘルツである。この制限から、垂直同期周波数60[ヘルツ](../Page/ヘルツ.md "wikilink")の場合の[最大解像度は](../Page/画面解像度.md "wikilink")2.6メガピクセルとなる。[WUXGAの解像度はこの制限に収まるので伝送できるが](../Page/Ultra_Extended_Graphics_Array.md "wikilink")、[QXGAの解像度やWUXGAでも垂直同期周波数を](../Page/Ultra_Extended_Graphics_Array.md "wikilink")60ヘルツより上げた場合には制限を超え伝送できない。それゆえ、広大な高解像度表示と多様な垂直同期周波数に対応するためにDVIコネクタは、2つ目のTMDSリンクを用意している。シングルリンクよりも伝送帯域が必要なときは、2番目のTMDSリンクを有効にする。そしてそれぞれのTMDSリンクで交互にピクセルデータを送信する。これを**デュアルリンクモード**という。デュアルリンクモードを使う場合、シングルリンク時のピクセルクロック周波数制限は取り払われ、それぞれのTMDSリンクのピクセルクロック周波数は165メガヘルツを超えてもよい。そのためデュアルリンクモードでの総合的なピクセルクロック周波数は、シングルリンクのピクセルクロック周波数最大値165メガヘルツを2倍した330メガヘルツよりも、高くすることができる。

DVI仕様は「ピクセルクロック周波数が165メガヘルツに達しないディスプレイモードはすべてシングルリンクモードを使い、それ以上のディスプレイモードはデュアルリンクモードを使わなければならない」とも規定しており、ピクセルクロック周波数165メガヘルツ未満（リンクあたり82.5メガヘルツ未満）でデュアルリンクモードを使うことを禁じている。

2番目のリンクは、上述した高解像度表示のほか、1ピクセルあたり24ビット以上（48ビットディープカラーなど）を必要とする場合にも使われる。この場合、[LSBからピクセルデータが転送される](../Page/最下位ビット.md "wikilink")。

最終期の[アナログVGAコネクタと同様に](../Page/VGA端子.md "wikilink")、DVIコネクタには[Display Data Channel](https://ja.wikipedia.org/wiki/VESA_Display_Data_Channel "wikilink") バージョン2 (DDC 2) のピンがあり、これによりグラフィックアダプタがディスプレイのExtended Display Identification Data (EDID) を読み取ることができる。

## コネクタ

[thumb](https://ja.wikipedia.org/wiki/ファイル:DVI_Connector_Types.svg "wikilink") DVIコネクタは普通DVI専用のデジタル映像信号を通すためのピンが含まれている。デュアルリンクシステムの場合は、データ信号線の2番目のセットに追加のピンを用いる。

DVIコネクタはVGA標準で使用されている古いアナログ信号も通すピンも併せ持っている。この特長は、DVIを普及させるための互換機能として規格に含まれた。ディスプレイタイプの変遷過程においてアナログ方式かデジタル方式かにかかわらず、同じコネクタ経由で映像信号を扱うことができた。

デバイスにあるDVIコネクタは実装されている信号線によって3つの名前がある。

  - **DVI-D**（デジタル専用）
  - **DVI-A**（アナログ専用）
  - **DVI-I**（Integrated, デジタルおよびアナログ兼用）

規格ではコネクタに広帯域伝送のための2番目のデータリンクを規定しているが、その性能に満たないすなわち2番目のデータリンクを要さないデバイスのほとんどは、コストダウンのためにこれを実装はしていない。ただしコネクタの接続互換性を上げる目的で、内部結線はされていないもののコネクタ自体は2番目のデータリンクピンを持つものを採用する機器が存在し外観上の区別を難しくしている。そのためそれら機器とを区別するために、2番目のリンクを正しく実装しているコネクタは、しばしば**DVI-DL**（**デュアルリンク**）と[通称](../Page/通称.md "wikilink")されている。なおこの通称はアナログ信号路の並装有無を表してはいない。同様に、DVIケーブルの多くも2番目のリンク（伝送路すなわち内部結線）を実装していないが、これを実装しているケーブルは、そうではないシングルリンクケーブルと区別するために**デュアルリンクケーブル**と呼ばれることがある。

DVI-Iコネクタにある長くて平たいピン（ピン番号はC5）はAnalog Ground に用いられる。このピンはDVI-Dコネクタにある同じピンよりも幅広い。そのため、仮にDVI-Iオスコネクタから4つのアナログピンを取り除いてもDVI-Dメスコネクタに接続することはできない。

  - DVI/HDCP

いくつかの新しいDVDプレーヤーやTVシステム（[HDTVを含む](https://ja.wikipedia.org/wiki/高精細度テレビジョン放送 "wikilink")）、ビデオプロジェクターはDVI/[HDCP](https://ja.wikipedia.org/wiki/HDCP "wikilink")コネクタを持っている。これらはDVIコネクタと物理的には同じであるが、著作権保護のためにHDCPプロトコルを用いて信号を暗号化して伝送している。DVIビデオコネクタを持つコンピュータはディスプレイとして多くのDVI付HDTVを使うことができる。

  - Mini-DVI

（ラップトップコンピュータのように）サイズに制限がある場合は、フルサイズDVI端子の代わりに[Mini-DVI](../Page/Mini-DVI.md "wikilink")端子が時々見受けられる。

## 仕様

  - ケーブル長: 最大5m

### デジタル

  - シングルリンクモード時の最小ピクセルクロック周波数: 21.76MHz
  - シングルリンクモード時の最大ピクセルクロック周波数: 165MHz (3.7Gbit/s)
  - デュアルリンクモード時の最小ピクセルクロック周波数: 165MHz超 (3.7Gbit/s超)
  - デュアルリンクモード時の最大ピクセルクロック周波数: 規定なし（高速伝送の品質は、ケーブル伝送特性を含む各機器の性能に依存する）
  - 1クロック当たりのピクセル数: 1 (シングルリンク)、2 (デュアルリンク)
  - 1ピクセル当たりのビット数: 24 (シングルリンク、デュアルリンク)、48 (デュアルリンク)
  - ディスプレイモードの例（シングルリンク）
      - HDTV (1920 × 1080) @ 60Hz + 5% LCD blanking(131MHz)
      - UXGA (1600 × 1200) @ 60Hz + 5% GTF blanking(161MHz)
      - WUXGA (1920 × 1200) @ 60Hz(154MHz)
      - SXGA (1280 × 1024) @ 85Hz + 5% GTF blanking(159MHz)
  - ディスプレイモードの例（デュアルリンク）
      - QXGA (2048 × 1536) @ 75Hz + GTF blanking(2 × 170MHz = 340MHz)
      - HDTV (1920 × 1080) @ 85Hz + GTF blanking(2 × 126MHz = 252MHz)
      - WQXGA (2560 × 1600) @ 60Hz + GTF blanking(2 × 174MHz = 348MHz) - 市販[ディスプレイの例として](../Page/ディスプレイ_\(コンピュータ\).md "wikilink") 30" LCD Dell、Apple、Samsung
      - WQUXGA (3840 × 2400) @ 33Hz + GTF blanking(2 × 159MHz = 318MHz)

GTF ([Generalized Timing Formula](https://ja.wikipedia.org/wiki/Generalized_Timing_Formula "wikilink")) はVESA標準であり、Linuxのgtfユーティリティツールで簡単に計算できる。

[4K解像度](https://ja.wikipedia.org/wiki/4K解像度 "wikilink")である[2160p](https://ja.wikipedia.org/wiki/2160p "wikilink") (3840 × 2160) @ 60Hzにはデュアルリンクでも帯域不足で対応しておらず、初期の4KディスプレイにはDVI-DLを複数本接続することで必要帯域を確保しているものもあったが、その後は[DisplayPort](../Page/DisplayPort.md "wikilink")（1.2以上）や[HDMI](https://ja.wikipedia.org/wiki/HDMI "wikilink")（2.0以上）などでの接続が一般的である。

### アナログ

  - RGB帯域上限: -3dBまで減衰を許容した場合に400MHzまで確保

### コネクタ

[393px](https://ja.wikipedia.org/wiki/ファイル:DVI_Connector_Pinout.svg "wikilink") ピン番号(ソケットを見た側から)

| **ピン** | **名称**                                                                          | **機能**                                   |
| ------ | ------------------------------------------------------------------------------- | ---------------------------------------- |
| 1      | [TMDS](https://ja.wikipedia.org/wiki/TMDS "wikilink") Data 2-                   | Digital red - (Link 1)                   |
| 2      | TMDS Data 2+                                                                    | Digital red + (Link 1)                   |
| 3      | TMDS Data 2/4 shield                                                            |                                          |
| 4      | TMDS Data 4-                                                                    | Digital green - (Link 2)                 |
| 5      | TMDS Data 4+                                                                    | Digital green + (Link 2)                 |
| 6      | [DDC](https://ja.wikipedia.org/wiki/VESA_Display_Data_Channel "wikilink") clock |                                          |
| 7      | DDC data                                                                        |                                          |
| 8      | Analog Vertical Sync                                                            |                                          |
| 9      | TMDS Data 1-                                                                    | Digital green - (Link 1)                 |
| 10     | TMDS Data 1+                                                                    | Digital green + (Link 1)                 |
| 11     | TMDS Data 1/3 shield                                                            |                                          |
| 12     | TMDS Data 3-                                                                    | Digital blue - (Link 2)                  |
| 13     | TMDS Data 3+                                                                    | Digital blue + (Link 2)                  |
| 14     | \+5V                                                                            | Power for monitor when in standby        |
| 15     | Ground                                                                          | Return for pin 14 and analog sync        |
| 16     | Hot Plug Detect                                                                 |                                          |
| 17     | TMDS data 0-                                                                    | Digital blue - (Link 1) and digital sync |
| 18     | TMDS data 0+                                                                    | Digital blue + (Link 1) and digital sync |
| 19     | TMDS data 0/5 shield                                                            |                                          |
| 20     | TMDS data 5-                                                                    | Digital red - (Link 2)                   |
| 21     | TMDS data 5+                                                                    | Digital red + (Link 2)                   |
| 22     | TMDS clock shield                                                               |                                          |
| 23     | TMDS clock+                                                                     | Digital clock + (Links 1 and 2)          |
| 24     | TMDS clock-                                                                     | Digital clock - (Links 1 and 2)          |
| C1     | Analog Red                                                                      |                                          |
| C2     | Analog Green                                                                    |                                          |
| C3     | Analog Blue                                                                     |                                          |
| C4     | Analog Horizontal Sync                                                          |                                          |
| C5     | Analog Ground                                                                   | Return for R, G and B signals            |

**ピン配置**

## DVIとHDMIの互換性

HDMIはDVIを基にしたデジタル映像・音声用の新しい規格で、AV機器用に機能が付加されている。基本的なデジタル映像信号については共通であり、DVI-HDMI変換ケーブルなどで相互に接続可能であるが、いくつかの違いもある。

  - HDMIはアナログRGBをサポートしない。信号線もなくなっている。
  - フルHDを超える高解像度への対応は、DVIが信号線を増やしたデュアルリンク、HDMIはシングルリンクのままでの規格のアップデートによる高速化と、方向性が分かれたため互換性はなくなった。
      - HDMIはタイプBコネクタ（2015年現在商品化されていない）を除き、デュアルリンクをサポートしない。
          - 一部商品にHDMI（一般的なAコネクタ） - DVI デュアルリンク変換ケーブルがあるが、実際の結線はシングルリンクのみであるので注意を要する。デュアルリンクの結線には必ずHDMI Bコネクタを要する。
      - DVIのシングルリンクはHDMI 1.3以降（340MHz・10.2Gbps）および2.0以降の高速伝送（600MHz・18Gbps）に未対応。
  - DVIはデジタル音声重畳に未対応。

HDMIのみで規格化されているデジタル音声重畳などは、DVI信号を扱う機器ではサポートされない。なお規格外製品の中には、DVI端子からHDMI信号を出力してデジタル音声を内包させているものや、DVI入力コネクタではあるがHDMI規格のデジタル音声信号を受け入れる機器もある。

## 競合規格

DVIは同じコネクタでアナログとデジタル伝送を選択できる規格としては唯一、広く普及した標準である。競合する標準はもっぱらデジタルのみである。これらのシステムは[Low voltage differential signaling](../Page/Low_voltage_differential_signaling.md "wikilink") (LVDS) を使用していて、[FPD](../Page/薄型テレビ.md "wikilink") (for Flat-Panel Display) LinkやFLATLINKと独自に呼ばれるものとして知られていた。その後継が、[LVDS Display Interface](https://ja.wikipedia.org/wiki/LVDS_Display_Interface "wikilink") (LDI) や[OpenLDI](https://ja.wikipedia.org/wiki/OpenLDI "wikilink")である。

USB信号はコネクタの中に入っていないので、[InFocus](https://ja.wikipedia.org/wiki/InFocus "wikilink")社が彼らのプロジェクタシステムに搭載したVESA M1-DAコネクタの中に入れた。そして、[アップルコンピュータによって](../Page/アップル_\(企業\).md "wikilink")[2005年](../Page/2005年.md "wikilink")まで[Apple Display Connectorとして使われた](../Page/Apple_Display_Connector.md "wikilink")。VESA M1コネクタは本質的にVESA Plug & Display (P\&D) である。それ自身は元々Enhanced Video Connector (EVC) と呼ばれていた。Apple Display Connectorは電気的にVESA P\&D/M1と互換性があるが、物理的にはコネクタのカバーの形が異なる。

## 関連項目

  - [Mini-DVI](../Page/Mini-DVI.md "wikilink")
  - [Micro-DVI](https://ja.wikipedia.org/wiki/Micro-DVI "wikilink")
  - [VGA端子](../Page/VGA端子.md "wikilink")
  - [HDMI](https://ja.wikipedia.org/wiki/HDMI "wikilink")
  - [DisplayPort](../Page/DisplayPort.md "wikilink")
  - [DFP](../Page/DFP.md "wikilink")

## 外部リンク

  - [The DVI specification at the Digital Display Working Group](http://www.cs.unc.edu/Research/stc/FAQs/Video/dvi_spec-V1_0.pdf)
  - [DVI video pinout](http://pinouts.ws/dvi-video-pinout.html)
  - [Silicon Image understanding DVI](http://www.siimage.com/docs/understanding_DVI/)

[Category:映像端子](https://ja.wikipedia.org/wiki/Category:映像端子 "wikilink") [Category:インタフェース規格](https://ja.wikipedia.org/wiki/Category:インタフェース規格 "wikilink") [Category:コネクタ](https://ja.wikipedia.org/wiki/Category:コネクタ "wikilink")