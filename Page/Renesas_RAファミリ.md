> この記事は[Renesas RAファミリ](https://ja.wikipedia.org/wiki/Renesas_RAファミリ)から翻訳されています。


**Renesas RAファミリ**は、[ルネサスエレクトロニクス](../Page/ルネサスエレクトロニクス.md "wikilink")が開発する32ビット[マイクロコントローラー](https://ja.wikipedia.org/wiki/マイクロコントローラー "wikilink")のファミリ名である。RAの名称の由来は「Renesas Advanced」の頭文字からきている。

## 概要

Arm Cortex-Mコアを採用した[CPU](../Page/CPU.md "wikilink")と、ルネサスが[SHファミリやRXファミリなどのオリジナルコアマイコンなどの長年の経験とノウハウが詰まった周辺機能を備えている](../Page/SuperH.md "wikilink")。2010年10月に発表された。\[1\]RA2シリーズ（最大60MHz）、RA4シリーズ（最大100MHz）、RA6シリーズ（最大200MHz）、そして最上位のRA8シリーズという、全4シリーズがラインアップされている。

RAファミリの特長はルネサスの独自の周辺機能と[Armアーキテクチャの融合であり](../Page/ARMアーキテクチャ.md "wikilink")、特にセキュリティに関しては自社で開発した暗号エンジンであるSecure Crypt Engine (SCE) とArmの「TrustZone for Arm v8-M」を融合し、PSAに準拠した「Trusted Firmware-M (TF-M) API」に対応することによってIoT機器のセキュリティ開発を安全かつ迅速に行えるとしている。

もう一つの特長として、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")として[FreeRTOS](https://ja.wikipedia.org/wiki/FreeRTOS "wikilink")を採用した[Flexible Software Package (FSP)](https://www.renesas.com/jp/ja/products/software-tools/software-os-middleware-driver/software-package/ra-fsp.html)を提供している。このFSPはほぼソースコードで提供されており（一部オブジェクト部分あり）、無償で利用可能であり、また様々なユースケースを想定し、ユーザーの過去からのソフトウェア資産やエコシステムソフトウェアとの併用などのフレキシブルな活用が可能である。よってデフォルトで採用されている[FreeRTOS](https://ja.wikipedia.org/wiki/FreeRTOS "wikilink")にこだわらず他の様々な商用[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")を活用することも可能としている。

## 歴史

### マイクロコントローラー

  - 2019年10月　Renesas RAファミリ発表
      - 初期ラインナップとして5グループ（RA2A1, RA4M1, RA6M1, RA6M2, RA6M3)がリリースされる
  - 2020年5月　ワイヤレス対応製品を拡充
      - Bluetooth Low Energy 5.0に対応するRA4W1をリリース

### ソフトウェア

  - 2019年10月　マイコンの初期ラインナップの評価用にFSPv0.8.0をリリース
  - 2020年3月　FSPv1.0.0をリリースし初期ラインナップの全機能に一通り対応
  - 2020年5月　RA4W1のBSPやBluetoothプロトコルスタックを備えるFSPv1.1.0をリリース
  - 2020年7月　FSPv1.2.0をリリースし、Segger emWinやCMSISのアップデートを実施

## CPUコア

RA4シリーズとRA6シリーズでは[Arm v7-Mアーキテクチャ](https://static.docs.arm.com/ddi0403/eb/DDI0403E_B_armv7m_arm.pdf)のArm Cortex-M4コアを採用、比較的ローエンドのシリーズであるRA2シリーズには[ARMv8-Mアーキテクチャ](https://static.docs.arm.com/ddi0553/a/DDI0553A_e_armv8m_arm.pdf)のArm Cortex-M23コアを採用している。またルネサスは同社のプレスリリースや各種インタビューの場でArmv8-MアーキテクチャのArm Cortex-M33コアを採用したラインアップの追加を計画していることを表明している。

## マイコンラインアップ

### RA8シリーズ

RA8シリーズはRAファミリの中でも最上位に位置付けられているシリーズである。動作周波数は200MHz以上だが、それ以外の情報は現時点で公表されていない。

<table>
<thead>
<tr class="header">
<th><p>シリーズ</p></th>
<th><p>製品グループ</p></th>
<th><p>CPUコア 最大動作周波数</p>
<p>動作電圧範囲</p></th>
<th><p>ピン数</p></th>
<th><p>Flash容量</p></th>
<th><p>SRAM容量</p></th>
<th><p>代表的な周辺機能</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RA8</p></td>
<td><p>非公開</p></td>
<td><p>非公開</p></td>
<td><p>非公開</p></td>
<td><p>非公開</p></td>
<td><p>非公開</p></td>
<td><p>非公開</p></td>
</tr>
</tbody>
</table>

### RA6シリーズ

RA6シリーズは高い処理性能と大容量メモリを搭載したシリーズである。CAN、USB、QSPIやイーサネットなどの多彩なコネクティビティに対応しており、TFTグラフィックLCDへの対応や、モーター制御用のPWMを出力するタイマやアナログ回路も豊富にサポートするなど多彩な機能が充実している。共通鍵暗号であるAESだけではなく、公開鍵暗号のRSAやECCに加えて、ハッシュ演算の処理を実行できる専用ハードウェア（Secure Crypt Engine 7）を搭載している為、IoTデバイスに要求されるセキュアコミュニケーションを容易に実現できる。

<table>
<thead>
<tr class="header">
<th><p>シリーズ</p></th>
<th><p>製品グループ</p></th>
<th><p>CPUコア 最大動作周波数</p>
<p>動作電圧範囲</p></th>
<th><p>ピン数</p></th>
<th><p>Flash容量</p></th>
<th><p>SRAM容量</p></th>
<th><p>代表的な周辺機能</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RA6</p></td>
<td><p><a href="https://www.renesas.com/jp/ja/products/microcontrollers-microprocessors/ra/ra6/ra6m3.html">RA6M3</a></p></td>
<td><p>Arm Cortex-M4 120MHz</p>
<p>2.7~3.6V動作</p></td>
<td><p>100~176</p></td>
<td><p>最大2MB</p></td>
<td><p>640KB</p></td>
<td><p>USBHS/FS, QSPI, イーサネット, SDHI, SCI, SPI, I2C, CAN, IIC,</p>
<p>12bit ADC, 12bit DAC, 各種タイマ,</p>
<p>GLCDC, JPEG, 2DG,</p>
<p>静電容量タッチセンシング,</p>
<p>Secure Crypt Engine 7 (SCE7)</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.renesas.com/jp/ja/products/microcontrollers-microprocessors/ra/ra6/ra6m2.html">RA6M2</a></p></td>
<td><p>Arm Cortex-M4 120MHz</p>
<p>2.7~3.6V動作</p></td>
<td><p>100~145</p></td>
<td><p>最大1MB</p></td>
<td><p>384KB</p></td>
<td><p>USBFS, QSPI, イーサネット, SDHI,</p>
<p>SCI, SPI, I2C, CAN, IIC,</p>
<p>12bit ADC, 12bit DAC, 各種タイマ,</p>
<p>静電容量タッチセンシング,</p>
<p>Secure Crypt Engine 7 (SCE7)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.renesas.com/jp/ja/products/microcontrollers-microprocessors/ra/ra6/ra6m1.html">RA6M1</a></p></td>
<td><p>Arm Cortex-M4 120MHz</p>
<p>2.7~3.6V動作</p></td>
<td><p>64~100</p></td>
<td><p>最大512KB</p></td>
<td><p>256KB</p></td>
<td><p>USBFS, QSPI, SDHI, 各種タイマ, SCI, SPI, I2C, CAN, IIC,</p>
<p>12bit ADC, 12bit DAC,</p>
<p>静電容量タッチセンシング,</p>
<p>Secure Crypt Engine 7 (SCE7)</p></td>
<td></td>
</tr>
</tbody>
</table>

### RA4シリーズ

RA4シリーズは最適化された処理性能と消費電力のバランスが特長である。電力消費を抑えつつ、性能やコネクティビティが必要なアプリケーションに最適である。USBやCANといったコネクティビティも充実しており、またその低消費電力を活かして、Bluetooth Low Energy 5.0に対応した製品もそろえる。高分解能A/Dコンバータ、セグメントLCDコントローラ、静電容量タッチセンシングなど、家電製品やヘルスケア製品に必要な機能を備えている。

<table>
<thead>
<tr class="header">
<th><p>シリーズ</p></th>
<th><p>製品グループ</p></th>
<th><p>CPUコア 最大動作周波数</p>
<p>動作電圧範囲</p></th>
<th><p>ピン数</p></th>
<th><p>Flash容量</p></th>
<th><p>SRAM容量</p></th>
<th><p>代表的な周辺機能</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RA4</p></td>
<td><p><a href="https://www.renesas.com/jp/ja/products/microcontrollers-microprocessors/ra/ra4/ra4m1.html">RA4M1</a></p></td>
<td><p>Arm Cortex-M4 48MHz</p>
<p>1.6~5.5V動作</p></td>
<td><p>40~100</p></td>
<td><p>最大256KB</p></td>
<td><p>32KB</p></td>
<td><p>USBFS, 各種タイマ, SCI, SPI, I2C, CAN, IIC,</p>
<p>14bit ADC, 12bit DAC,</p>
<p>静電容量タッチセンシング,</p>
<p>Secure Crypt Engine 5 (SCE5)</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.renesas.com/eu/ja/products/microcontrollers-microprocessors/ra/ra4/ra4w1.html">RA4W1</a></p></td>
<td><p>Arm Cortex-M4 48MHz</p>
<p>1.8~3.6V動作</p></td>
<td><p>56</p></td>
<td><p>最大512KB</p></td>
<td><p>96KB</p></td>
<td><p>Bluetooth 5.0, USBFS, 各種タイマ,</p>
<p>SCI, SPI, I2C, CAN, IIC,</p>
<p>14bit ADC, 12bit DAC,</p>
<p>静電容量タッチセンシング,</p>
<p>Secure Crypt Engine 5 (SCE5)</p></td>
<td></td>
</tr>
</tbody>
</table>

### RA2シリーズ

RA2シリーズはRAファミリの中でも最も低消費電力が求められるアプリケーションの為に設計されている。動作時、スタンバイ時の消費電力が極めて低く、またスタンバイからの復帰も高速で、主にバッテリ動作のアプリケーションに用いられる。1.6Vから5.5Vまで広範囲で動作し、最大24ビットの高分解能A/Dコンバータや静電容量タッチセンシングに対応している。

<table>
<thead>
<tr class="header">
<th><p>シリーズ</p></th>
<th><p>製品グループ</p></th>
<th><p>CPUコア 最大動作周波数</p>
<p>動作電圧範囲</p></th>
<th><p>ピン数</p></th>
<th><p>Flash容量</p></th>
<th><p>SRAM容量</p></th>
<th><p>代表的な周辺機能</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RA2</p></td>
<td><p><a href="https://www.renesas.com/eu/ja/products/microcontrollers-microprocessors/ra/ra2/ra2a1.html">RA2A1</a></p></td>
<td><p>Arm Cortex-M23 48MHz</p>
<p>1.6~5.5V動作</p></td>
<td><p>32~64</p></td>
<td><p>最大256KB</p></td>
<td><p>32KB</p></td>
<td><p>USBFS, 各種タイマ, SCI, SPI, I2C, CAN,</p>
<p>24bit ΔΣADC, 16bit ADC, 12/8bit DAC,</p>
<p>静電容量タッチセンシング,</p>
<p>AESアクセラレータ, TRNG</p></td>
</tr>
</tbody>
</table>

### Part Number Decoder

RAファミリのマイクロコントローラーの型名は16桁のPart Numberで表記される。

| R       | 7   | F     | A        | X      | X           | X     | X       | X          | X    | X          | X       | X       | X | X | X |
| ------- | --- | ----- | -------- | ------ | ----------- | ----- | ------- | ---------- | ---- | ---------- | ------- | ------- | - | - | - |
| Renesas | MCU | Flash | Advanced | Series | Application | Group | Feature | Flash size | Temp | ROM Number | Quality | Package |   |   |   |
| ①       | ②   | ③     | ④        | ⑤      | ⑥           | ⑦     | ⑧       | ⑨          | ⑩    | ⑪          | ⑫       | ⑬       | ⑭ | ⑮ |   |

Part Number Decoder

①　R（固定）：Renesas

②　7（固定）：マイクロコントローラ

③　F（固定）：フラッシュメモリ混載製品

④　A（固定）：Renesas RAファミリ

⑤　シリーズ：RA2=2、RA4=4、RA6=6、RA8=8

⑥　アプリケーション：M＝メインストリーム、W=ワイヤレス、T＝モータ制御、A＝アナログフロントエンド

⑨　フラッシュメモリ容量：3=16KB、4=24KB、 5=32KB、6=48KB、7=64KB、8=96KB、9=128KB、A=192KB、B=256KB、C=384KB、D=512KB、E=768KB、F=1,024KB、G=1,536KB、H=2,048KB

⑩　動作温度範囲：2=-40度\~85度、3=-40度\~105度

⑭　品質グレード：C=産業グレード(Q2A)、D=民生グレード(Q2B)

⑮　パッケージ

|    |      |     |         |           |
| -- | ---- | --- | ------- | --------- |
|    | タイプ  | ピン数 | サイズ(mm) | ピンピッチ(mm) |
| BG | BGA  | 176 | 13x13   | 0.8       |
| FC | LQFP | 174 | 24x24   | 0.5       |
| FB | LQFP | 144 | 20x20   | 0.5       |
| FP | LQFP | 100 | 14x14   | 0.5       |
| FF | LQFP | 80  | 14x14   | 0.65      |
| FN | LQFP | 80  | 12x12   | 0.5       |
| FK | LQFP | 64  | 14x14   | 0.8       |
| FM | LQFP | 64  | 10x10   | 0.5       |
| BU | BGA  | 64  | 4x4     | 0.4       |
| FL | LQFP | 48  | 7x7     | 0.5       |
| LM | LGA  | 36  | 4x4     | 0.5       |
| FJ | LQFP | 32  | 7x7     | 0.8       |
| NH | VQFN | 32  | 5x5     | 0.5       |

## Flexible Software Package (FSP)

### 概要

Flexible Software Package (FSP) は、ルネサスエレクトロニクスが提供するソフトウェア群である。無償のソースコードが[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")から提供されている。FreeRTOSや各種[ミドルウェア](../Page/ミドルウェア.md "wikilink")、HALドライバなどのソフトウェアが含まれており、RAファミリを用いたシステム開発を行うユーザーが、必要なソフトウェアを自由に活用することができる。 [サムネイル](https://ja.wikipedia.org/wiki/ファイル:Renesas_RA_FSP_Diagram.jpg "wikilink")

### 主な機能

  - FSPｖ1.2.0
      - 2020年7月リリース

#### BSP（Board Support Package）

  - CMSIS-Core準拠のスタートアップコード
  - クロック、メモリ、割込み、スタック、ランタイムなど基本的サービス
  - CMSIS-DSP
  - CMSIS-NN

#### HALドライバ

  - MCUのマニュアルに沿ったレジスタレベルのアクセス
  - 高性能、省フットプリント

#### オペレーティングシステム

  - 最新バージョンのFreeRTOSをリファレンスとして採用
  - ツールでコンフィギュレーション可能なRTOSリソース（スレッド、ミューテックスなど）
  - サードパーティ製OS対応、ベアメタル対応

#### ミドルウェア

  - FreeRTOS+FAT, LittleFSのファイルシステム
  - TCP/IPをはじめとした各種通信プロトコルスタック
  - セキュアコミュニケーションを実現するMbed TLS1.3
  - CDC、HID、マスストレージに対応したUSBミドルウェア
  - Bluetoothプロトコルスタックとサンプルアプリケーション
  - 主要なクラウドプロバイダとの簡単な接続オプション
  - Arm PSA Crypt APIと暗号ハードウェアエンジン
  - Segger emWinグラフィックスライブラリインターフェース

## ツール開発環境

### 統合開発環境

Renesas RAファミリの統合開発環境としてはルネサスエレクトロニクスが独自に用意するものだけではなく、ARM KeilやIARシステムズといったサードパーティ製の製品が使用できる。直感的な操作でデバイスの各種設定を行いコードを生成するスマートコンフィギュレータの機能は、いずれのケースでも利用できる。

<table>
<caption>RAファミリで使用できる統合開発環境</caption>
<thead>
<tr class="header">
<th><p>IDE（統合開発環境）</p></th>
<th><p>Renesas e2 studio</p></th>
<th><p><a href="https://www.youtube.com/watch?v=pMDVm-VctwE&amp;t=212s">IAR Systems</a> <a href="https://www.youtube.com/watch?v=pMDVm-VctwE&amp;t=212s">Embedded Workbench for ARM</a></p></th>
<th><p>ARM Keil MDK</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>コンパイラ</p></td>
<td><p>•<a href="https://ja.wikipedia.org/wiki/GCC" title="wikilink">GCC</a> v9.0 •Arm Compiler v6.12以降</p></td>
<td><p>•IAR arm Compiler 8.50.1以降</p></td>
<td><p>•arm Compiler v6.12以降</p></td>
</tr>
<tr class="even">
<td><p>デバッギングエミュレータ</p></td>
<td><p>•E2エミュレータ/E2 Lite •Segger J-Link</p></td>
<td><p>•IAR I-Jet •Segger J-Link</p></td>
<td><p>•Segger J-Link</p></td>
</tr>
<tr class="odd">
<td><p>コンフィギュレータ</p></td>
<td><p>e2 studioにビルトイン： •BSPコンフィギュレーション</p>
<p>•クロック・コンフィギュレーション</p>
<p>•ピン・コンフィギュレーション</p>
<p>•モジュール・コンフィギュレーション</p>
<p>•割込みコンフィギュレーション</p></td>
<td><p>•RA SC (RAスマート・コンフィギュレータ)を使用</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>その他機能</p></td>
<td><p>•QE for Capacitive Touch •QE for BLEなど</p></td>
<td><p>•C-SPY •C-RUN, C-STATなど</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="odd">
<td><p>ライセンス</p></td>
<td><p>無償</p></td>
<td><p>有償</p></td>
<td><p>有償</p></td>
</tr>
</tbody>
</table>

### 開発用/評価用ボード（Evaluation Kits）

ルネサスはRAファミリの開発用/評価用ボードとしてEvaluation Kit（EK）を製品化している。EKにはMCUの全端子にアクセス可能なピンヘッダを備え、また用途に応じたセンサやコネクティビティを拡張するための拡張コネクタとしてPmod、[Arduino](https://ja.wikipedia.org/wiki/Arduino "wikilink")、Mikrobus、Groveのコネクタを備えている。オンボードデバッガとしてJ-Link OBも実装している為、同梱されているUSBケーブルとPCで接続するだけですぐにデバッグやプログラムの書き込みが可能な仕様となっている。回路図やBOM、デザインファイルなどもルネサスの公式HPで公開されており、これらのEKはルネサスの販売代理店や電子部品の通販サイトなどで購入可能である。

<table>
<caption>Renesas RAファミリ　Evaluation Kitsのラインナップ</caption>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>型名</p></th>
<th><p>説明</p></th>
<th><p>利用できるエコシステムコネクタ</p></th>
<th><p>購入</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://www.renesas.com/eu/ja/products/software-tools/boards-and-kits/eval-kits/ek-ra6m3g.html#productInfo">EK-RA6M3G</a></p></td>
<td><p>RTK7EKA6M3S01001BU</p></td>
<td><p>RA6M3グループグラフィックス評価キット （EK-RA6M3 + 4.3インチTFTカラー液晶480x272搭載グラフィック拡張ボード）</p></td>
<td><p>Digilent Pmod Arduino uno R3</p>
<p>Seeed Grove</p>
<p>MikroBUS</p></td>
<td><p>ルネサスエレクトロニクス販売特約店・代理店 または</p>
<p>オンラインディストリビュータ</p></td>
</tr>
<tr class="even">
<td><p><a href="https://www.renesas.com/eu/ja/products/software-tools/boards-and-kits/eval-kits/ek-ra6m3.html#productInfo">EK-RA6M3</a></p></td>
<td><p>RTK7EKA6M3S00001BU</p></td>
<td><p>RA6M3グループ評価キット</p></td>
<td><p>Digilent Pmod Arduino uno R3</p>
<p>Seeed Grove</p>
<p>MikroBUS</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.renesas.com/eu/ja/products/software-tools/boards-and-kits/eval-kits/ek-ra6m2.html#productInfo">EK-RA6M2</a></p></td>
<td><p>RTK7EKA6M2S00001BU</p></td>
<td><p>RA6M2グループ評価キット</p></td>
<td><p>Digilent Pmod</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://www.renesas.com/eu/ja/products/software-tools/boards-and-kits/eval-kits/ek-ra6m1.html#productInfo">EK-RA6M1</a></p></td>
<td><p>RTK7EKA6M1S00001BU</p></td>
<td><p>RA6M1グループ評価キット</p></td>
<td><p>Digilent Pmod</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.renesas.com/eu/ja/products/software-tools/boards-and-kits/eval-kits/ek-ra4w1.html#productInfo">EK-RA4W1</a></p></td>
<td><p>RTK7EKA4W1S00000BJ</p></td>
<td><p>RA4W1グループ Bluetooth Low Energy評価キット</p></td>
<td><p>Digilent Pmod Arduino uno R3</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://www.renesas.com/eu/ja/products/software-tools/boards-and-kits/eval-kits/ek-ra4m1.html#productInfo">EK-RA4M1</a></p></td>
<td><p>RTK7EKA4M1S00001B</p></td>
<td><p>RA4M1グループ評価キット</p></td>
<td><p>Digilent Pmod</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.renesas.com/eu/ja/products/software-tools/boards-and-kits/eval-kits/ek-ra2a1.html#productInfo">EK-RA2A1</a></p></td>
<td><p>RTK7EKA2A1S00001BU</p></td>
<td><p>RA2A1グループ評価キット</p></td>
<td><p>Digilent Pmod</p></td>
<td></td>
</tr>
</tbody>
</table>

また、株式会社アルファプロジェクトや株式会社北斗電子などによるサードパーティ製ボードも存在する。

### その他

Renesas RAファミリで使用可能なツール

#### [QE for BLE](https://www.renesas.com/eu/ja/products/software-tools/tools/solution-toolkit/qe-qe-for-ble.html)

Bluetooth® low energyを使った組み込みシステム開発に対応した開発支援ツール。統合開発環境e² studioに対応。RA4W1のBluetooth®仕様の通信機能をすぐに試すことが可能。

#### [QE for Capacitive Touch](https://www.renesas.com/eu/ja/products/software-tools/tools/solution-toolkit/qe-qe-for-capacitive-touch.html)

静電容量式タッチセンサを使った組み込みシステム開発に対応した開発支援ツール。RXファミリ、RAファミリに対応。

#### [PG-FP6](https://www.renesas.com/eu/ja/products/software-tools/tools/programmer/pg-fp6.html?cid=tlbj-002-fp6)

ルネサス製フラッシュメモリ内蔵マイコンに対し、ユーザシステム上で、プログラムの消去、書き込み、ベリファイを行うためのツール。

#### [Renesas Flash Programmer V3](https://www.renesas.com/jp/ja/products/software-tools/tools/programmer/renesas-flash-programmer-programming-gui.html)

ルネサス製フラッシュ内蔵マイコンのフラッシュメモリに対し、開発フェーズ、量産フェーズそれぞれでの書き込みをサポートする操作性・機能を提供する

#### AppWizard（Segger）

RA6M3とFSPに同梱されたSegger社のemWinグラフィックスライブラリを用いたGUI開発ツール。WYSIWYGエディタ。

#### [EVRICA（DTSインサイト）](https://www.youtube.com/watch?v=VI9N9MzStYU)

動作中の組込みソフトウェア内部の入出力データや変数など、動的に変化するデータ値をリアルタイムに計測

#### FL-PR6（内藤電誠町田製作所）

フラッシュメモリプログラマ

## RA Ready 開発パートナーエコシステム

ルネサスではRAファミリですぐに使えるソフトウェア/ハードウェアソリューションを提供しているパートナー製品を「RA Ready」の表記のもとでいくつか公表している。代表的なパートナー企業は以下の通りである。(順不同)

### セキュリティとセーフティ

  - Cypherbridge Systems LLC
  - Veridify Security
  - [WolfSSL](https://ja.wikipedia.org/wiki/WolfSSL "wikilink")
  - ユビキタスAIコーポレーション
  - SmartAxiom, Inc
  - Segger
  - HEX Five Security
  - Secure Thingz
  - IARシステムズ

### コネクティビティとクラウド連携

  - [Microsoft Azure](https://ja.wikipedia.org/wiki/Microsoft_Azure "wikilink")
  - Alibaba Cloud
  - ARM Pelion
  - サイレックス・テクノロジー株式会社
  - RELOC
  - 株式会社プロアシスト
  - Clarinox
  - Altobeam

### 人工知能と機械学習

  - Qeexo
  - Ignitarium

### ヒューマン・マシン・インタフェース

  - Sensory
  - Cyberon
  - テクノマセマティカル
  - アドバンスト・メディア
  - Segger
  - FDI
  - Pachira
  - 東芝

### センシングとコントロール

  - BFG Engineering

### 特定用途/新規アプリケーション

  - ORBSTAR
  - TATA ELXSI
  - GT\&T
  - MBS

### ツールとユーザーエクスペリエンス

  - [IARシステムズ](https://ja.wikipedia.org/wiki/IARシステムズ "wikilink")
  - イー・フォース株式会社
  - 株式会社グレープシステム
  - ミナトエレクトロニクス
  - フラッシュサポートグループ
  - ユークエスト
  - アルファプロジェクト
  - arm Keil
  - DTSインサイト
  - [FreeRTOS](https://ja.wikipedia.org/wiki/FreeRTOS "wikilink")
  - CapExt

## 脚注

<references />

## 外部リンク

1.  [公式サイト](https://www.renesas.com/in/ja/products/microcontrollers-microprocessors/ra.html)
2.  [2](https://www.renesas.com/in/ja/about/press-center/news/2019/news20191008.html)

__インデックス__

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")

1.  ルネサス エレクトロニクス [1](https://www.renesas.com/in/ja/about/press-center/news/2019/news20191008.html) 2020年10月8日