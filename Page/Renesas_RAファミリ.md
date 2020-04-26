> この記事は[Renesas RAファミリ](https://ja.wikipedia.org/wiki/Renesas_RAファミリ)から翻訳されています。


**Renesas RAファミリ**は、[ルネサスエレクトロニクス](../Page/ルネサスエレクトロニクス.md "wikilink")が開発する32ビット[マイクロコントローラー](https://ja.wikipedia.org/wiki/マイクロコントローラー "wikilink")のファミリ名である。RAの名称の由来は「Renesas Advanced」の頭文字からきている。

## 概要

Arm Cortex-Mコアを採用した[CPU](../Page/CPU.md "wikilink")と、ルネサスが[SHファミリやRXファミリなどのオリジナルコアマイコンなどの長年の経験とノウハウが詰まった周辺機能を備えている](../Page/SuperH.md "wikilink")。2010年10月に発表された。\[1\]RA2シリーズ（最大60MHz）、RA4シリーズ（最大100MHz）、RA6シリーズ（最大200MHz）、そして最上位のRA8シリーズという、全4シリーズがラインアップされている。

RAファミリの特長はルネサスの独自の周辺機能と[Armアーキテクチャの融合であり](../Page/ARMアーキテクチャ.md "wikilink")、特にセキュリティに関しては自社で開発した暗号エンジンであるSecure Crypt Engine (SCE) とArmの「TrustZone for Arm v8-M」を融合し、PSAに準拠した「Trusted Firmware-M (TF-M) API」に対応することによってIoT機器のセキュリティ開発を安全かつ迅速に行えるとしている。

もう一つの特長として、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")として[FreeRTOS](https://ja.wikipedia.org/wiki/FreeRTOS "wikilink")を採用した[Flexible Software Package (FSP)](https://www.renesas.com/jp/ja/products/software-tools/software-os-middleware-driver/software-package/ra-fsp.html)を提供している。このFSPは全てソースコードで提供されており、無償で利用可能であり、また様々なユースケースを想定し、ユーザーの過去からのソフトウェア資産やエコシステムソフトウェアとの併用などのフレキシブルな活用が可能である。よってデフォルトで採用されている[FreeRTOS](https://ja.wikipedia.org/wiki/FreeRTOS "wikilink")にこだわらず他の様々な商用[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")を活用することも可能としている。

## CPUコア

RA4シリーズとRA6シリーズでは[Arm v7-Mアーキテクチャ](https://static.docs.arm.com/ddi0403/eb/DDI0403E_B_armv7m_arm.pdf)のArm Cortex-M4コアを採用、比較的ローエンドのシリーズであるRA2シリーズには[ARMv8-Mアーキテクチャ](https://static.docs.arm.com/ddi0553/a/DDI0553A_e_armv8m_arm.pdf)のArm Cortex-M23コアを採用している。またルネサスは同社のプレスリリースや各種インタビューの場でArmv8-MアーキテクチャのArm Cortex-M33コアを採用したラインアップの追加を計画していることを表明している。

## マイコンラインアップ

<table>
<caption>Renesas RAファミリ マイコンラインアップ</caption>
<thead>
<tr class="header">
<th><p>シリーズ</p></th>
<th><p>製品グループ</p></th>
<th><p>CPUコア</p></th>
<th><p>動作周波数</p></th>
<th><p>最大Flash容量</p></th>
<th><p>SRAM容量</p></th>
<th><p>代表的な周辺機能</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RA8シリーズ</p></td>
<td><p>非公開</p></td>
<td><p>非公開</p></td>
<td><p>非公開</p></td>
<td><p>非公開</p></td>
<td><p>非公開</p></td>
<td><p>非公開</p></td>
</tr>
<tr class="even">
<td><p>RA6シリーズ</p></td>
<td><p><a href="https://www.renesas.com/jp/ja/products/microcontrollers-microprocessors/ra/ra6/ra6m3.html">RA6M3</a></p></td>
<td><p>Arm Cortex-M4</p></td>
<td><p>120MHz</p></td>
<td><p>2MB</p></td>
<td><p>640KB</p></td>
<td><p>USBHS/FS, QSPI, Ethernet, SDHI, SCI, SPI, I2C, CAN, IIC,</p>
<p>12bit ADC, 12bit DAC, 各種タイマ,</p>
<p>GLCDC, JPEG, 2DG,</p>
<p>静電容量タッチセンシング,</p>
<p>Secure Crypt Engine 7 (SCE7)</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://www.renesas.com/jp/ja/products/microcontrollers-microprocessors/ra/ra6/ra6m2.html">RA6M2</a></p></td>
<td><p>Arm Cortex-M4</p></td>
<td><p>120MHz</p></td>
<td><p>1MB</p></td>
<td><p>384KB</p></td>
<td><p>USBFS, QSPI, SDHI, 各種タイマ,</p>
<p>SCI, SPI, I2C, CAN, IIC,</p>
<p>12bit ADC, 12bit DAC,</p>
<p>静電容量タッチセンシング,</p>
<p>Secure Crypt Engine 7 (SCE7)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://www.renesas.com/jp/ja/products/microcontrollers-microprocessors/ra/ra6/ra6m1.html">RA6M1</a></p></td>
<td><p>Arm Cortex-M4</p></td>
<td><p>120MHz</p></td>
<td><p>512KB</p></td>
<td><p>256KB</p></td>
<td><p>USBFS, QSPI, SDHI, 各種タイマ, SCI, SPI, I2C, CAN, IIC,</p>
<p>12bit ADC, 12bit DAC,</p>
<p>静電容量タッチセンシング,</p>
<p>Secure Crypt Engine 7 (SCE7)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>RA4シリーズ</p></td>
<td><p><a href="https://www.renesas.com/jp/ja/products/microcontrollers-microprocessors/ra/ra4/ra4m1.html">RA4M1</a></p></td>
<td><p>Arm Cortex-M4</p></td>
<td><p>48MHz</p></td>
<td><p>256KB</p></td>
<td><p>32KB</p></td>
<td><p>USBFS, 各種タイマ, SCI, SPI, I2C, CAN, IIC,</p>
<p>14bit ADC, 12bit DAC,</p>
<p>静電容量タッチセンシング,</p>
<p>Secure Crypt Engine 5 (SCE5)</p></td>
</tr>
<tr class="even">
<td><p>RA2シリーズ</p></td>
<td><p><a href="https://www.renesas.com/jp/ja/products/microcontrollers-microprocessors/ra/ra2/ra2a1.html">RA2A1</a></p></td>
<td><p>Arm Cortex-M23</p></td>
<td><p>48MHz</p></td>
<td><p>256KB</p></td>
<td><p>32KB</p></td>
<td><p>USBFS, 各種タイマ, SCI, SPI, I2C, CAN,</p>
<p>24bit ΔΣADC, 16bit ADC, 12/8bit DAC,</p>
<p>静電容量タッチセンシング,</p>
<p>AESアクセラレータ, TRNG</p></td>
</tr>
</tbody>
</table>

## Flexible Software Package (FSP)

Flexible Software Package (FSP) は、ルネサスエレクトロニクスが提供するソフトウェア群である。無償のソースコードが[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")から提供されている。FreeRTOSや各種[ミドルウェア](../Page/ミドルウェア.md "wikilink")、HALドライバなどのソフトウェアが含まれており、RAファミリを用いたシステム開発を行うユーザーが、必要なソフトウェアを自由に活用することができる。

  - FSPｖ1.0.0
      - 2020年3月リリース
      - 主な機能
          - メモリ使用量の小さいHALドライバ
          - 直感的操作が可能なコンフィグレータとコードジェネレータ
          - RTOSを使用するアプリケーション、RTOSを使用しないアプリケーションの双方をサポート
          - 最新バージョンのFreeRTOSを採用
          - ツールでコンフィギュレーション可能なRTOSリソース（thread, mutexなど）
          - TCP/IPをはじめとした各種通信プロトコルスタック
          - 主要なクラウドプロバイダとの簡単な接続オプション
          - CDC、マスストレージに対応したUSBミドルウェア
          - セキュアコミュニケーションを実現するMbed TLS1.3
          - Arm PSA Crypt APIと暗号ハードウェアエンジン
          - Segger emWinによる グラフィックスインターフェース対応
          - セキュアデバッグ機能

## RA Ready 開発パートナーエコシステム

ルネサスではRAファミリですぐに使えるソフトウェア/ハードウェアソリューションを提供しているパートナー製品を「RA Ready」の表記のもとでいくつか公表している。代表的なパートナー企業は以下の通りである。(順不同)

  - セキュリティとセーフティ
      - Cypherbridge Systems LLC
      - Veridify Security
      - [WolfSSL](https://ja.wikipedia.org/wiki/WolfSSL "wikilink")
      - ユビキタスAIコーポレーション
      - SmartAxiom, Inc
      - Segger
      - HEX Five Security
  - コネクティビティとクラウド連携
      - [Microsoft Azure](https://ja.wikipedia.org/wiki/Microsoft_Azure "wikilink")
      - Alibaba Cloud
      - ARM Pelion
      - サイレックス・テクノロジー株式会社
      - RELOC
      - 株式会社プロアシスト
      - Clarinox
      - Altobeam
  - 人工知能と機械学習
      - Qeexo
      - Ignitarium
  - ヒューマン・マシン・インタフェース
      - Sensory
      - Cyberon
      - テクノマセマティカル
      - アドバンスト・メディア
      - Segger
  - センシングとコントロール
      - BFG Engineering
  - 特定用途/新規アプリケーション
      - ORBSTAR
      - TATA ELXSI
      - GT\&T
      - MBS
  - ツールとユーザーエクスペリエンス
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

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")

1.  ルネサス エレクトロニクス [1](https://www.renesas.com/in/ja/about/press-center/news/2019/news20191008.html) 2020年10月8日