> この記事は[RGB21ピン](https://ja.wikipedia.org/wiki/RGB21ピン)から翻訳されています。


**RGB21ピン**とは、[アナログ](../Page/アナログ.md "wikilink")で映像・音声を伝送するための[端子](https://ja.wikipedia.org/wiki/端子 "wikilink")の名称。[フランス](https://ja.wikipedia.org/wiki/フランス "wikilink")で標準化された[SCART端子](../Page/SCART端子.md "wikilink")と同一形状である。SCART規格では[コンポジット](../Page/コンポジット映像信号.md "wikilink")、[RGB](../Page/RGB.md "wikilink")（RGBの代わりに[S端子](../Page/S端子.md "wikilink")映像信号を伝送する拡張規格もある）と2チャンネルの音声を伝送出来るが、日本ではゲーム機器や一部のパソコンなどのRGB接続手段として使われることが多く、コンポジット接続は省略されたためRGB接続専用端子として「RGB21ピン端子」という名称が多用されている\[1\]。[EIAJで規格化された端子である](../Page/電子情報技術産業協会.md "wikilink") (EIAJ CPR-1201)。

## 概要

RGB接続は垂直同期信号 (V SYNC) と水平同期信号 (H SYNC) を別に伝送する[DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")機の[D-sub](../Page/D-subminiature.md "wikilink")15Pin端子や通常のPC-9801用[モニター端子とは違い](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")、テレビと同じ15.75kHzの複合同期信号 (C SYNC) を伝送するため（したがって240p、480iより上の解像度の表示も不可能\[2\]）現在のパソコンのモニタ端子としては使用できない。

日本国内ではMSX2パソコン用モニタやそのモニタ兼用テレビ、PC-9801用モニタの一部機種でこの端子を用意しているものが存在していた。

また、[NTSC](../Page/NTSC.md "wikilink")対応のモニタ（ソニー GVM14/21シリーズ、NEC PC-TVシリーズ、NEC MultiSyncシリーズの一部、シャープ CZ-600系モニタの大多数など）では、複合同期信号を水平同期信号・垂直同期信号に分離する同期分離回路（LM1881Nなど）と、その回路用の変換ケーブルを自作することで、この問題を解消できた。変換ボックスには市販されているものもある（[電波新聞社XSYNC](../Page/マイコンソフト.md "wikilink")-1\[3\]など）。

[FM TOWNS用の一部モニタでは複合同期信号入力に対応しており](../Page/FM_TOWNS.md "wikilink")、21ピンから15ピンへの変換ケーブル\[4\]を自作することで表示可能である。

## 端子配列

[none](https://ja.wikipedia.org/wiki/ファイル:Scart_pin_layout.png "wikilink") レセプタクル、またはプラグを半田面から見た図となる。なお、本来のSCART端子とは端子配列（用法）が異なるので注意。

| **ピン番号** | **RGB21ピン**            | SCART （参考）                                               |
| -------- | ---------------------- | -------------------------------------------------------- |
| 1        | **音声入力（左）**            | 音声出力（右）                                                  |
| 2        | **音声出力（左）**            | 音声入力（右）                                                  |
| 3        | **音声入力グランド**           | 音声出力（左）                                                  |
| 4        | **音声出力グランド**           | 音声グランド                                                   |
| 5        | **音声入力（右）**            | 映像（青）入力/出力グランド                                           |
| 6        | **音声出力（右）**            | 音声入力（左）                                                  |
| 7        | **コンポジット・ビデオ信号入力グランド** | 映像（青）入力/出力                                               |
| 8        | **コンポジット・ビデオ信号出力グランド** | ワイドスクリーン切替                                               |
| 9        | **コンポジット・ビデオ信号入力**     | 映像（緑）入力/出力グランド                                           |
| 10       | **コンポジット・ビデオ信号出力**     | デジタル・データ・バス入力                                            |
| 11       | **AVコントロール信号 (AV)**    | 映像（緑）入力/出力                                               |
| 12       | **RGB映像マスク信号 (Ym)**    | デジタル・データ・バス出力                                            |
| 13       | **RGB映像信号（赤）グランド**     | 映像（赤）/色信号 (C) 入力/出力グランド                                  |
| 14       | **Ym・Ysグランド**          | デジタル・データ・バス グランド                                         |
| 15       | **RGB映像信号（赤）入力**       | 映像（赤）/色信号 (C) 入力/出力                                      |
| 16       | **RGB映像切替信号 (Ys)**     | RGB・コンポジット切替                                             |
| 17       | **RGB映像信号（緑）グランド**     | コンポジット・ビデオ信号出力グランド/同期出力信号グランド/輝度信号 (Y) 出力グランド            |
| 18       | **RGB映像信号（青）グランド**     | コンポジット・ビデオ信号入力グランド/同期入力信号グランド/輝度信号 (Y) 入力グランド/RGB・切替グランド |
| 19       | **RGB映像信号（緑）入力**       | コンポジット・ビデオ信号出力/同期信号出力/輝度信号 (Y) 出力                        |
| 20       | **RGB映像信号（青）入力**       | コンポジット・ビデオ信号入力/同期信号入力/輝度信号 (Y) 入力                        |
| 21       | **フレームグランド（金属フレーム）**   | フレームグランド（金属フレーム）                                         |
|          |                        |                                                          |

**ピン配置**

  - 使わない端子はNC（無接続）とすることが可能。
  - 信号名と対のグランドは、その信号と同軸または「より線」にしてインピーダンス整合を取ることが望ましい。
  - コンポジット・ビデオ信号は、通常のビデオ端子（黄）と同じ。複合同期信号が重畳されており、0.7Vp-p、75Ω整合。
  - RGB映像（赤、緑、青）は正極アナログ信号、0.7Vp-p、75Ω整合。
  - 音声信号は0.4Vrms、インピーダンスは入力47kΩ、出力10kΩ。
  - YsはHレベルでRGBから入力、Lレベルでコンポジットから入力。Lレベルが0 - 0.4VDC、Hレベルが1.0 - 3.0VDC、75Ω整合。
  - YmはHレベルでコンポジットがマスクされる。レベル、インピーダンスはYsと同じ。
  - AVは入力切替信号、Hレベルでこの端子からの入力が有効となる。TTLレベル、22kΩ整合。

## RGB21ピン端子で接続できる機器（純正ケーブルあり）

  - [スーパーファミコン](../Page/スーパーファミコン.md "wikilink")（SHVC-010で対応）※ケーブル内のコンデンサが劣化している場合あり\[5\]。現在はコンデンサを格納しやすく設計された自作用基板が存在する\[6\]。
  - [PlayStation](../Page/PlayStation_\(ゲーム機\).md "wikilink")、[PS one](../Page/PS_one.md "wikilink")、[PlayStation 2](../Page/PlayStation_2.md "wikilink")、[PlayStation 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")（SCPH-1050で対応）※サードパーティ製のRGBケーブルは空中配線で、音声の左右が逆に接続されている\[7\]。自作に必要なコンデンサ・抵抗の仕様はスーパーファミコン用と同じ\[8\]。
  - [セガサターン](../Page/セガサターン.md "wikilink")（HSS-0109で対応）※純正RGBケーブルはグランドが接続されておらず音声ノイズが乗る\[9\]。
  - [ネオジオ](https://ja.wikipedia.org/wiki/ネオジオ "wikilink")、[ネオジオCD](../Page/ネオジオCD.md "wikilink")（FCG-9で対応）
  - [スーパーカセットビジョン](../Page/スーパーカセットビジョン.md "wikilink")（専用RGB接続コードで対応）
  - [SMC-777](../Page/SMC-777.md "wikilink")（ソニーSMK-702で対応\[10\]）
  - [MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")2（およびその後継規格）（ソニーHBK-0821Ⅱ・松下FS-VC3011・ヤマハRC-01・東芝TVC-15P等で対応）
      - 東芝パソコン接続アダプターTVC-15PはRGB信号強度と水平位置の調整が可能
  - [FM77AV](https://ja.wikipedia.org/wiki/FM-7#FM77AV "wikilink")（およびその後継規格）（FM77-721で対応、詳しくは外部リンクを参照のこと）
  - FM77AV40SX（FM77-724で対応） ※25ピン→21ピンへの変換ケーブル
  - [PC-8801mkIISR](https://ja.wikipedia.org/wiki/PC-8800シリーズ "wikilink")（PC-CA403\[11\]・ソニーVMC-2115\[12\]、サンワサプライKB-D1521\[13\]などで対応） ※分離同期の他に複合同期を出力している。
  - [PC-9801U2・VM2・VM0・VF2](../Page/PC-9800シリーズ.md "wikilink")（ケーブルに関しては同上） ※分離同期の他に複合同期を出力している。
  - シグマ電子、KIC等各社アーケードゲーム基板用コントロールボックス（MSX用ケーブルが転用できるものもあり）

また、MSXの一部の機種ではRGB出力端子が[DIN](../Page/DINコネクタ.md "wikilink")8ピンでない場合があり、ケーブルが転用不可能な事も考えられる\[14\]。

## RGB21ピン端子で接続できる機器（純正ケーブルなし）

[thumb](https://ja.wikipedia.org/wiki/画像:Xbox_360_Advanced_SCART_cable.jpg "wikilink")

  - [編集ファミコン](../Page/編集ファミコン.md "wikilink") ※内部チップから信号を取り出す必要あり\[15\]、チップを移植すれば他のファミコンでも可能
  - [NINTENDO64](../Page/NINTENDO64.md "wikilink") ※内部チップから信号を取り出し[DACで変換する必要あり](../Page/デジタル-アナログ変換回路.md "wikilink")\[16\]。
  - [ニンテンドーゲームキューブ](../Page/ニンテンドーゲームキューブ.md "wikilink") ※純正のコンポーネントケーブルもしくはD端子ケーブルを改造する必要あり\[17\]
  - [セガ・マークIII](../Page/セガ・マークIII.md "wikilink") ※出力が弱くアンプ回路が必要、RGBケーブルにFMサウンドユニット入力端子を増設する必要あり\[18\]
  - [マスターシステム](https://ja.wikipedia.org/wiki/マスターシステム "wikilink") ※セガ製カスタムチップ搭載機でなければRGB出力不可能
  - [メガドライブ](../Page/メガドライブ.md "wikilink") ※RGB各線の終端処理がされておらず抵抗を内蔵したRGBケーブルを自作する必要あり\[19\]。RGB出力回路はスーパーファミコンやPlayStationなどと同等なため\[20\]、SHVC-010・SCPH-1050の入力プラグを取り替える改造で対応できる。
  - メガドライブ2 ※サードパーティからRGB出力を可能にする周辺機器が販売されていた。また出力端子が同じ形状なのでメガジェットやスーパー32Xでも使用可能である。
  - [ドリームキャスト](../Page/ドリームキャスト.md "wikilink") ※使用するソフトによってはRGB出力不可能\[21\]
  - [Xbox](../Page/Xbox_\(ゲーム機\).md "wikilink") ※サードパーティ製RGBケーブルは音声ラインが左右逆に接続されていることあり\[22\]
  - [Xbox 360](../Page/Xbox_360.md "wikilink") ※VGAケーブルほどの高画質化は望めない。また、欧州では純正SCARTケーブルあり。
  - [PCエンジン](../Page/PCエンジン.md "wikilink") ※拡張バス、内部チップから信号を取り出す必要あり\[23\]\[24\]、拡張バス無しの型は内部チップからのみ

## 脚注

## 関連項目

  - [AVマルチ](../Page/AVマルチ.md "wikilink")

[Category:映像端子](https://ja.wikipedia.org/wiki/Category:映像端子 "wikilink") [Category:音声端子](https://ja.wikipedia.org/wiki/Category:音声端子 "wikilink") [Category:コネクタ](https://ja.wikipedia.org/wiki/Category:コネクタ "wikilink")

1.  「RGBマルチ」という名称が使用されているケースもある
2.  FM77AV40シリーズ、PC-8801mkIISRなど一部の機種では約24kHzの複合同期信号を出力しており、モニタ側が対応していれば400ライン表示は可能である
3.  [SC-512N1-L/DVI](http://www.micomsoft.co.jp/sc-512n1.htm)
4.  [●FM-77AV用TOWNSモニター接続アダプター](http://dempa.jp/rgb/drug/fmavtw01.html)
5.  [純正RGBケーブルが発売されている（された）ゲーム機](http://rgbcharmer.kt.fc2.com/rgb-junsei-cable.htm)
6.  [ファミコンRGB化の部屋 - emulation number 9 - Windows用エミュレータ専門ニュースサイト](http://www.emulation9.com/fcmod/)
7.  [プレステ用RGBケーブルの秘密？ – What will be, will be\!\! It's {HIRO}'s Blog\!\!](https://hkjunk0.com/game/game-other/playstation-rgb-output.html)
8.
9.
10. [SMC-777 アナログRGBケーブル「SMK702」 - SMC-777 アナログRGBケーブルのレビュー ジグソー](http://zigsow.jp/portal/own_item_detail/285159/)
11. [品名：RGBテレビ用ケーブル](http://121ware.com/psp/PA121/NECS_SUPPORT_SITE/CRM/s/WEBLIB_NECS_PRO.PRODUCT_ID.FieldFormula.IScript_Product_Spec_Details?prodId=PC-CA403)
12.
13. [KB-D1521【アナログRGBケーブル　3m】アナログRGBケーブル　3m - サンワサプライ株式会社](http://www.sanwa.co.jp/product/syohin.asp?code=KB-D1521)
14. [PASOPIAの謎](http://blogs.yahoo.co.jp/dr_kikkie/25661990.html)
15. [ゲーム機をRGB出力改造しないと駄目なゲーム機](http://rgbcharmer.kt.fc2.com/rgb-kaizou.htm)
16. [N64RGB Installation Guide](https://etim.net.au/n64rgb/instructions-new/)
17. [RGB出力は出てるがRGBケーブルを自作しないといけないゲーム機](http://rgbcharmer.kt.fc2.com/rgb-jisaku-cablergb.htm)
18.
19.
20.
21. [サードパーティーからしかRGBケーブルが発売されていないゲーム機](http://rgbcharmer.kt.fc2.com/rgb-3rdparty-cable.htm)
22.
23.
24. [BEEPで取り扱いさせて頂く同人アイテムにこちらのPCエンジンJAMMA接続キット「羽生構想」が加わりました。｜BEEP](http://www.beep-shop.com/blog/6023/)