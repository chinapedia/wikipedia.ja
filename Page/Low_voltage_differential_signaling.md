> この記事は[Low voltage differential signaling](https://ja.wikipedia.org/wiki/Low_voltage_differential_signaling)から翻訳されています。


**Low voltage differential signaling** (**LVDS**) は短距離用のデジタル[有線伝送技術であり](https://ja.wikipedia.org/wiki/有線通信 "wikilink")、小振幅・低消費電力で比較的高速の[差動](../Page/平衡接続.md "wikilink")[インターフェースである](../Page/インタフェース_\(情報技術\).md "wikilink")。

[1994年](../Page/1994年.md "wikilink")に[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")/TIA/[EIA](https://ja.wikipedia.org/wiki/EIA "wikilink")-644として標準規格となり、まずコンピュータでの高速ネットワークやバスなどから使用が始まった。1998年頃からは[液晶ディスプレイ](https://ja.wikipedia.org/wiki/液晶ディスプレイ "wikilink")の標準画像インターフェースとして採用が広がり、2000年から2010年現在にいたる間にノートパソコンをはじめ液晶モニタ、薄型テレビなど多くのデジタル表示機器でほとんど標準的な技術となっている。2010年現在では、LVDSの性能の限界から高性能な液晶ディスプレイでは新たな規格へ切り替えが進んでいる。[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")と[AMD](https://ja.wikipedia.org/wiki/AMD "wikilink")は[2013年](../Page/2013年.md "wikilink")までにノートパソコンでのLVDSの搭載をやめ、[DisplayPort](../Page/DisplayPort.md "wikilink")などに置き換える予定\[1\]。

同名での似た技術として、テレビ分野では米[ナショナル セミコンダクター社が開発した](../Page/ナショナル_セミコンダクター.md "wikilink") "FPD-Link" をLVDSと呼ぶことが一般的である\[2\]。

## 標準化

米ナショナル セミコンダクター社のFlat Panel Display Link (FPD-Link) が元になり、1994年にANSI/TIA/EIA-644-AでLVDSは標準化されている。この標準ではツイストペア銅線では最大655Mbit/sまでと推奨しているが、理想的な伝送路では1.9Gbit/sを超える速度も可能だと予測している。

## 技術

### ディファレンシャル伝送

[thumb](https://ja.wikipedia.org/wiki/ファイル:LVDS_model_circuit_E.PNG "wikilink")  LVDSは2本の伝送路を使用する差動信号システムであり、2つの異なる電圧を送信し受信側で両者を比較するものである。

LVDSは信号伝送のために2線間での電圧の違いを利用する。トランスミッターは非常に少ない電流、通常は信号線一本当たり3.5mAを送出する。この値は送信される論理レベルに依存する。電流は約100から120Ωのケーブルの特性インピーダンスに整合した抵抗器を通って受信端に流れる。そして、もう一方の線に沿って反対方向へ戻ってくる。オームの法則から、抵抗の両端での電圧の違いはおよそ350mVになる。受信側はこの電圧の極性を検知して論理レベルを決定する。これはカレントループ伝送方式の一種である。

小信号の増幅や[ツイストペアケーブル](../Page/ツイストペアケーブル.md "wikilink")による2線間の電磁場カップリングにより、電磁波ノイズの放射量を減らすことができる。

約1.25Vと低いコモンモード電圧（2線上の平均電圧）により、LVDSは2.5Vないしそれ以下の電圧で電源供給される集積回路の広い箇所で使うことができる。先に350mVと述べた低い差動電圧により、LVDSは他のシステムと比べて非常に少ない電力しか消費しない。例えば、[RS-422](https://ja.wikipedia.org/wiki/RS-422 "wikilink")の[負荷抵抗](https://ja.wikipedia.org/wiki/負荷抵抗 "wikilink") 内で静的に消費される電力は90mWに対し、LVDSでは1.2mWである。[終端抵抗](../Page/終端抵抗.md "wikilink")が無い場合、信号線すべてがデータ1ビットごとにドライブされなければならない。高周波や負荷抵抗の利用により、信号線のすべてがドライブされるのを待たずに次の1ビットを送信できるため電力効率がよい。このときの信号スピードは周辺にある物質中の[光速度](https://ja.wikipedia.org/wiki/光速度 "wikilink")に近い\[3\]。

## 採用

[マイクロコンピュータ](../Page/マイクロコンピュータ.md "wikilink")の処理性能が向上すると、デジタル機器間でも、互いのデータ伝送のための信号伝送速度に不足感が生じた。それまでは単純なパラレル接続のクロックを高めることで対応してきたが、高いクロックでは伝送距離に制約が生まれケーブルも耐ノイズ性にも配慮が求められた。データ伝送容量を増やすには信号線数を増やさなければならなかった。サーバーファームやデータセンターのような大量のデータを扱うコンピュータ・システムでは、CPUユニットとRAIDシステム間のような何メートルもの長さを大量のデータをやり取りする必要があったので、LVDSに対して大変関心を持っていた。

コンピュータ・バスでのLVDSの2つの利用例は[HyperTransport](../Page/HyperTransport.md "wikilink")と[FireWire](https://ja.wikipedia.org/wiki/FireWire "wikilink")である。両者ともSCI (Scalable Coherent Interface) の流れを汲む次世代Futurebusを元とする。LVDSはSCSI標準（Ultra-2 SCSIおよびその後継）でサポートされ、より高速なデータ伝送とより長いケーブル長を実現した。[シリアルATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")や[RapidIO](https://ja.wikipedia.org/wiki/RapidIO "wikilink")、[SpaceWire](https://ja.wikipedia.org/wiki/SpaceWire "wikilink")は高速[データ転送](https://ja.wikipedia.org/wiki/データ転送 "wikilink")を可能とするためにLVDSを利用している。

LVDSはまた[グラフィックス・カードから](../Page/ビデオカード.md "wikilink")[ビデオモニター](https://ja.wikipedia.org/wiki/ビデオモニター "wikilink")へ映像データを伝送するのにも使うことができる。薄型パネル向けの応用は、米ナショナル セミコンダクター社がFlat Panel Display Link (FPD-Link) という名称で提案したのが先駆けである。TIA/EIA-644には電気的な伝送仕様のみが規定されていたが、FPD-Linkで画像クロック信号を7逓倍してシリアル伝送する仕様が初めて定義された。その後、パネルの高解像度化に合わせてOpenLDIという規格も提案された。これらの方式は最大ピクセル周波数は112MHzで1400×1050@60Hz (SXGA+) のディスプレイ解像度には十分である。デュアルリンクにより最大2048×1536@60Hz (QXGA) の解像度まで拡張できる。FPD-Linkは約5mまでのケーブル長を延ばすことができ、LDIは同じく約10mまで延長できる。

現在では、LVDSがVESAによって大型液晶パネルの標準仕様として採用され、ノートパソコン用、液晶モニター用、テレビ用パネルに広く普及している。高速化に制限のあるTTLで多数のパラレル伝送する方式に比べ、LVDSでシリアル伝送する方式では、配線数を減らせるためにコストを抑えられる上、消費電力を減らし、EMIも抑制できる利点がある。LVDSには、コンテンツ保護やスキュー調整の機能を定義した規格がないため機器間接続は制限されるが、重たいロジック回路が必要ない利点から機器内の基板間伝送に利用されている。また、最近の色深度拡張の要求に応えて、当初は6bitにしか対応できなかった仕様が10bitまで拡張されている。

しかしながら、近年（2008年現在）、映像信号を伝送する規格としてLVDS以外に多くの方式が提案され、用途に応じて棲み分けが進んでいる。TMDS方式を用いた[DVIや](../Page/Digital_Visual_Interface.md "wikilink")[HDMIは](https://ja.wikipedia.org/wiki/High-Definition_Multimedia_Interface "wikilink")、バイアスと終端方法がLVDSの仕様とは異なるが、[HDCP](https://ja.wikipedia.org/wiki/HDCP "wikilink")の採用でコンテンツ保護が可能で、チャネル間スキューの調整機能がついているため長距離接続に向き、主として機器間の接続に利用されている。また、[V-by-One HSは](../Page/V-by-One_HS.md "wikilink")、テレビ内部配線用にLVDSに代わるものとして提案されており、4K×2K (3840×2160) の超高解像度 (UD) でも、LVDS を用いると96 対のケーブルが必要なのに対し、16 対のみで対応可能になる。

[PCI Expressでは](../Page/PCI_Express.md "wikilink")1つもしくは複数（x1,x2,x4,x8,x16,x32レーンから選択）のLVDS相当の技術をチャネルとして採用し、従来の[PCIバスよりも高速なデータ転送が行えるコンピュータの内部バスとして利用されている](../Page/Peripheral_Component_Interconnect.md "wikilink")。

## SerDes

SerDes (Serializer/Deserializer) LVDSは伝送幅に柔軟性を持たせるように意図されており、データ転送速度をそれほど求めない用途では2本のデータ線と2本のクロック線だけを用いて、伝送路の両端部に "Serializer/Deserializer" と呼ばれるパラレルデータとシリアルデータを直列／並列に変換して1対のデータ線上に1ビットずつ送受信する構成を採るものがある。

デジタル機器内部での8本や16本といったパラレルバスよりも、このような "SerDes" と略して呼ばれる、数本しか使わないシリアルデータによる方が便利な基板間結線のような用途で利用されることがある。

## マルチポイントLVDS

LVDSは元々、データ線だけを見れば、1対の伝送路の両端に1組のトランスミッタと1組のレシーバが存在し片方向のみ伝送するポイント・ツー・ポイント型の形態を想定している。この基本的な形態に対して応用的な形態として、1対の伝送路上に複数のトランスミッタやレシーバを配置するバス型の形態（マルチポイント型形態）も利用されることがあり、この形態は、"**Bus LVDS**" もしくは "**BLVDS**" と呼ばれる。

標準のLVDSトランスミッタはポイント・ツー・ポイント接続用に設計されているが、マルチポイント接続では複数の終端抵抗をドライブするための大電流出力が可能な少し変なるLVDSトランスミッタを使っている。Bus LVDSと同様のものに[TI社が推進する](../Page/テキサス・インスツルメンツ.md "wikilink") **"LVDM"** があり、これらがマルチポイントLVDS規格の実質的な標準となっている。また、マルチポイントLVDS (**MLVDS**) は、TIA-899による標準化により発展してAdvancedTCAプラットフォームのクロック配送手段に採用されている。

**MLVDS**は受信側は2種類ある。Type-1はほとんどLVDSと互換であり、0Vスレッショルドを用いている。Type-2は回路が開放や短絡するなどのさまざまなエラーをある一定のやり方で扱うために100mVスレッショルドを用いている。MLVDSの例を以下に示す。

|               |                 |                 |
| ------------- | --------------- | --------------- |
| 最小/最大入力電圧     | 最小/最大出力コモンモード電圧 | 最小/最大出力電圧       |
| \-1.4 / 3.8 V | 0.3 / 2.1 V     | 0.480 / 0.650 V |

## SCI-LVD

現在のLVDSの形式になるまでには、SCI-LVDと呼ばれる方式が試みられていた。これはScalable Coherent Interconnect (SCI) のサブセットで[IEEE](../Page/IEEE.md "wikilink") 1596.3で規定された。これは複数のプロセッサ間通信のために設計された。

## 代替規格

2010年現在のLVDS技術の採用製品でも、最上位の高画質大画面TVなどでは液晶ディスプレイでの画像処理LSIとタイミング・コントローラICとの間にデータ線だけで96本、48対もの配線\[4\]が必要になっており、配線数がこれほど多いとICとケーブルのコストや機器スペースの自由度が制限され、クロックとデータのスキューやEMIの放射対策などによって、基板設計が難しくなるといった問題が生じる。LVDSを採用している各社は、これらの問題を回避するために、次世代の技術を模索している。いずれもクロック信号をデータ線に重畳してスキュー問題を回避している。

  - eDP
  - iDP
  - V-by-One HS
  - FPD-Link II
  - Advanced PPmL

主にノートパソコン用のLVDS代替規格として[VESA](../Page/VESA.md "wikilink")では**eDP**を標準化した。波形等化がオプションで規定され、[HDCPによる著作権保護機能も備える](https://ja.wikipedia.org/wiki/コピーガード#HDCP（High-bandwidth_Digital_Content_Protection） "wikilink")。2009年に米[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")社は、2013年にはノートパソコンを含む携帯端末の80%にeDPが採用されると予想した。

主にテレビ向けのLVDS代替規格に、**iDP**と**V-by-One HS**がある。iDPは2010年第2四半期にVESAで標準規格化される予定とされる。V-by-One HSは日本の[ザインエレクトロニクス](https://ja.wikipedia.org/wiki/ザインエレクトロニクス "wikilink")社が主導しており、[サムスン電子](../Page/サムスン電子.md "wikilink")がテレビの配線技術に採用する予定だとされる。ディスプレイ一般のLVDS代替規格として米[ナショナル セミコンダクター社が開発した](../Page/ナショナル_セミコンダクター.md "wikilink")**FPD-Link II**もある。

<table>
<tbody>
<tr class="odd">
<td style="text-align: center;"></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>名称</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>信号線1対当たりのデータ伝送速度</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>専用クロックの有無</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>符号化方式</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>カップリング</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>波形等化の規定</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>著作権保護機能</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>ロイヤリティー</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>備考</p></td>
</tr>
</tbody>
</table>

\[5\]

## 脚注

### 注釈

### 出典

## 関連項目

  - [DisplayPort](../Page/DisplayPort.md "wikilink")
  - [V-by-One HS](../Page/V-by-One_HS.md "wikilink")

## 外部リンク

  -
  - **, Texas Instruments, 2004

  - **, Texas Instruments, 2008

  -
[Category:コンピュータバス規格](https://ja.wikipedia.org/wiki/Category:コンピュータバス規格 "wikilink") [Category:ロジック・ファミリ](https://ja.wikipedia.org/wiki/Category:ロジック・ファミリ "wikilink")

1.  [【PC Watch】 IntelとAMD、アナログディスプレイ出力を2015年までに廃止 ～パネルメーカーやPCメーカーも賛同](http://pc.watch.impress.co.jp/docs/news/20101209_412932.html)
2.
3.  LVDSの他にも[差動伝送](https://ja.wikipedia.org/wiki/差動伝送 "wikilink")システムは存在し、信号を小さな振幅の電圧とすることで高速伝送時に伴う電力消費を抑えるように考慮されている。デジタル伝送回路では常に高速化と低消費電力が求められるため、[QuickPath Interconnectのように新たな技術ではさらに小振幅の規格が登場している](https://ja.wikipedia.org/wiki/インテル_QuickPath_インターコネクト "wikilink")。
4.  LVDSでも96本もの配線が求められる高画質大画面TVとは、各色10ビット計30ビット、240フレーム/秒、1080p映像の場合である。
5.  根津禎著、『ノート・パソコンやテレビでLVDS代替の新技術導入』、日経エレクトロニクス2010年2月8日号