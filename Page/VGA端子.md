> この記事は[VGA](https://ja.wikipedia.org/wiki/VGA)から翻訳されています。


[DE15_Diagram.svg](https://ja.wikipedia.org/wiki/File:DE15_Diagram.svg "fig:DE15_Diagram.svg") [thumb](https://ja.wikipedia.org/wiki/image:VGA_Stecker.jpg "wikilink") [thumbになっているケーブル](https://ja.wikipedia.org/wiki/image:BNC_connectors.jpg "wikilink")\]\] **VGA端子**（他に**アナログRGB端子**等とも）は、アナログ[RGB](../Page/RGB.md "wikilink")[コンポーネント映像信号](https://ja.wikipedia.org/wiki/コンポーネント映像信号 "wikilink")を出力（もしくは入力）する装置の[コネクタ](https://ja.wikipedia.org/wiki/コネクタ "wikilink")、およびその信号を伝送するケーブルに用いられるコネクタである。

## 概要

[VGA規格に準拠した](../Page/Video_Graphics_Array.md "wikilink")[IBM](../Page/IBM.md "wikilink")製の[グラフィックボード](https://ja.wikipedia.org/wiki/グラフィックボード "wikilink")にこのコネクタが採用されたことから、この名前が用いられるようになった。伝送する信号の形式からアナログRGB端子とも言う。「HD15」とも呼ばれる。

主に[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")などの[コンピュータ](../Page/コンピュータ.md "wikilink")で用いられ、もともとは[CRT](../Page/ブラウン管.md "wikilink")[ディスプレイといったアナログ信号を用いるディスプレイに映像を出力することを想定している](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")。

[ラップトップ](https://ja.wikipedia.org/wiki/ラップトップ "wikilink")コンピュータなどでコネクタのサイズを小型化したい場合、標準のVGA端子の代わりに小型化した[mini-VGA](https://ja.wikipedia.org/wiki/mini-VGA "wikilink")端子を実装した製品も存在する。

なお、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")や[AMDなどは](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[12月8日](../Page/12月8日.md "wikilink")に、2015年までにVGAへの対応を終了し[HDMI](https://ja.wikipedia.org/wiki/HDMI "wikilink")や[DisplayPort](../Page/DisplayPort.md "wikilink")に移行する方針を表明した\[1\]。

## 仕様

VGA端子にはいくつかのバリエーションがある。

1.  3列15ピンのDE-15（ミニ[D-Sub](../Page/D-subminiature.md "wikilink")15とも呼ばれる）コネクタに、RGBのそれぞれのアナログ信号と[HとVの同期信号を配置したもの](https://ja.wikipedia.org/wiki/同期信号#映像信号伝送のための同期信号 "wikilink")
2.  コネクタ形状はそのままで1にVESA DDC([VESA Display Data Channel](https://ja.wikipedia.org/wiki/VESA_Display_Data_Channel "wikilink"))の信号を追加したもの
3.  1と同等の信号線を9ピンD-Subコネクタに配置したもの
4.  1と同等の信号線を同軸ピンを内包した13W3と呼ばれるコネクタに配置したもの

VESA DDCはディスプレイの情報をコンピュータ側から取得できるようにした通信方式で、DDC1とDDC2では通信方式が異なる。DDC2では通信方式として[I²C](https://ja.wikipedia.org/wiki/I²C "wikilink")が採用されている。

また同期信号は、HとVを混合したものを複合同期信号として1本の信号で伝送したり、さらに複合同期信号を緑映像信号に載せて、信号線を減らしている場合（Sync on Green）もある。これはVGA端子が登場する以前、BNCコネクタで同信号を伝送していたことの名残である。

なお、かつてSun系ワークステーションで主流だった13W3コネクタと同一形状であるにも関わらずピンアサインが異なる機種が存在しているため、市販品の3列15ピンとの変換アダプタ（カモンADVGA-13Wなど）が流用不可能という問題が発生している\[2\]\[3\]。

RGBの信号はディスプレイ側に75Ωの[インピーダンス](../Page/インピーダンス.md "wikilink")があり、最も明るい状態は0.7Vで表現する。よって、1ビット出力で良いなら、[デジタル回路](../Page/デジタル回路.md "wikilink")からの出力が3.3Vなら、間に279Ωの[抵抗](https://ja.wikipedia.org/wiki/抵抗 "wikilink")を挟むと約0.7Vになる。デジタル回路から8ビット出力をするには、[デジタル-アナログ変換回路](../Page/デジタル-アナログ変換回路.md "wikilink")を使う。

### コネクタとピン配置

下に15ピンのコネクタの図とピン番号/信号線の表を示す。図中のピン番号はグラフィックカード側のメスコネクタであることに注意すること。ケーブルの端のピン番号は、普通オスコネクタなので図を反転させること。

ピン番号 (ソケットを見たもの):

[DE15_Connector_Pinout.svg](https://ja.wikipedia.org/wiki/File:DE15_Connector_Pinout.svg "fig:DE15_Connector_Pinout.svg")

| ピン | 名称             | 機能                                                                  |
| -- | -------------- | ------------------------------------------------------------------- |
| 1  | RED            | Red video signal                                                    |
| 2  | GREEN          | Green video signal or Sync on Green signal                          |
| 3  | BLUE           | Blue video signal                                                   |
| 4  | N/C            | Not connected                                                       |
| 5  | GND            | Ground                                                              |
| 6  | RED_RTN       | Red video signal return                                             |
| 7  | GREEN_RTN     | Green video signal return                                           |
| 8  | BLUE_RTN      | Blue video signal return                                            |
| 9  | N/C            | Not connected                                                       |
| 10 | GND            | Ground                                                              |
| 11 | N/C            | Not connected                                                       |
| 12 | SDA            | [I<sup>2</sup>C](https://ja.wikipedia.org/wiki/I²C "wikilink") data |
| 13 | HSYNC or CSYNC | Horizontal or Composite synchronization signal                      |
| 14 | VSYNC          | Vertical synchronization signal                                     |
| 15 | SCL            | I<sup>2</sup>C clock                                                |

**ピン配置**

アナログRGB信号はVGA規格が登場する以前からコンピュータで用いられていた。 一部の[Macintosh](../Page/Macintosh.md "wikilink")(MacIIより)や[PC-9801](../Page/PC-9800シリーズ.md "wikilink")(VM/VFより)などでは、ディスプレイへの映像出力コネクタとして、2列15ピンのDA-15コネクタを用いてアナログRGB信号を伝送していた。ちなみにコネクタ形状は同じでも両者のピン配置は異なる。

2000年代以降、コンピュータのディスプレイは、CRTディスプレイから[液晶ディスプレイ](https://ja.wikipedia.org/wiki/液晶ディスプレイ "wikilink")に主力が移りつつあり、デジタル伝送も行える[DVIコネクタが広く普及してきた](../Page/Digital_Visual_Interface.md "wikilink")。液晶ディスプレイは内部ではデジタル信号を用いてカラーを表示するため、アナログ信号を伝送するよりデジタル信号を伝送するほうが適している。

また、アナログRGB信号よりも前にデジタルRGB信号というものが存在していた。デジタルRGBではRGBそれぞれをON/OFFの1ビットで表し、

  - R=0,G=0,B=0 黒
  - R=0,G=0,B=1 青
  - R=0,G=1,B=0 緑
  - R=0,G=1,B=1 水色
  - R=1,G=0,B=0 赤
  - R=1,G=0,B=1 紫
  - R=1,G=1,B=0 黄
  - R=1,G=1,B=1 白

の8色が表示できるものである。この各RGBをON/OFFの2階調のみではなく多階調にしたものがアナログRGBである。近年のDVIなどのデジタル信号とは別のものである。

## 脚注

## 関連項目

  - [RGB21ピン](../Page/RGB21ピン.md "wikilink")
  - [8ピン角型デジタル端子](../Page/8ピン角型デジタル端子.md "wikilink") - 先述のデジタル8色が使われている端子
  - [DisplayPort](../Page/DisplayPort.md "wikilink")

## 外部リンク

  - [VGA pinout](http://pinouts.ru/Video/VGA15_pinout.shtml)
  - [VGA (VESA DDC) pinout](http://pinouts.ru/Video/VGAVesaDdc_pinout.shtml)
  - [VGA-9 pinout](http://old.pinouts.ru/Video/VGA9_pinout.shtml)

[it:Video Graphics Array\#Connettore VGA](https://ja.wikipedia.org/wiki/it:Video_Graphics_Array#Connettore_VGA "wikilink")

[Category:映像端子](https://ja.wikipedia.org/wiki/Category:映像端子 "wikilink") [Category:コネクタ](https://ja.wikipedia.org/wiki/Category:コネクタ "wikilink") [Category:インタフェース規格](https://ja.wikipedia.org/wiki/Category:インタフェース規格 "wikilink")

1.  [Leading PC Companies Move to All Digital Display Technology, Phasing out Analog | Intel Newsroom](https://newsroom.intel.com/news-releases/leading-pc-companies-move-to-all-digital-display-technology-phasing-out-analog/)
2.  [13W3 ‐ 通信用語の基礎知識](http://www.wdic.org/w/WDIC/13W3)
3.