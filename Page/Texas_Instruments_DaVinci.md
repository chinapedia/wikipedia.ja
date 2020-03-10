> この記事は[Texas Instruments DaVinci](https://ja.wikipedia.org/wiki/Texas_Instruments_DaVinci)から翻訳されています。


**[Texas Instruments](https://ja.wikipedia.org/wiki/テキサス・インスツルメンツ "wikilink") DaVinci テクノロジー**（ダビンチ・テクノロジー）は、広範な最適化されたデジタルビデオとデジタル機器の開発のために、[テキサス・インスツルメンツ](https://ja.wikipedia.org/wiki/テキサス・インスツルメンツ "wikilink") (TI) が統合したデジタルシグナルプロセッサ、ソフトウェア、ツールのセットである。DaVinci DSP は、広く使われている[TMS320](https://ja.wikipedia.org/wiki/Texas_Instruments_TMS320 "wikilink") DSP ファミリの一部である。

## 概要

[ハードディスクレコーダー](https://ja.wikipedia.org/wiki/ハードディスクレコーダー "wikilink")や[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")のような、典型的なマルチメディアシステムは、大まかに２つの部分に分けることができる。制御部とメディア処理部である。メディア処理部が音声や画像のエンコード・デコードの処理を行っている間、制御部は[メモリーカード](../Page/メモリーカード.md "wikilink")や[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")のアクセス、[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")、[ネットワーキング](https://ja.wikipedia.org/wiki/ネットワーキング "wikilink")のような処理を行う。汎用プロセッサは制御部のタスクで良い性能を発揮するが、最も強力な汎用プロセッサでも、[リアルタイムの高画質ビデオエンコーディングのようなメディア処理関連のタスクには](https://ja.wikipedia.org/wiki/リアルタイムシステム "wikilink")、十分に強力であるとはいえない。一方で DSP は、反復的で容易に並列化できるメディア処理関連のタスクで素晴らしい性能を発揮するが、制御タスクでは十分な性能を発揮できない。

DaVinci ファミリーのプロセッサの背後にあるアイデアは、汎用プロセッサと DSP を用いて、制御部とメディア処理部のタスクを、それぞれに適したプロセッサで実行させることである。これらの 2つの構成要素の 1チップへの統合により、システムデザインを単純化し、2つの構成要素の間のより効率的なコミュニケーションを行うことができる。

現在の DaVinci ファミリーのプロセッサは、ARM と DSP のマルチコアデバイス (例：DM644x) から、DSP のシングルコアデバイス (例：DM643x)、ARM のシングルコアデバイス (例：DM355) まで、幅広いスケーラビリティがある。

## 周辺デバイス

DaVinci プロセッサファミリーは、多くのオンチップデバイスを搭載している。それぞれのモデルにより搭載状況は異なる。

  - [コンパクトフラッシュ](../Page/コンパクトフラッシュ.md "wikilink")・[SDカード](https://ja.wikipedia.org/wiki/SDメモリーカード "wikilink")・[MMC](../Page/マルチメディアカード.md "wikilink") などの[メモリーカード](../Page/メモリーカード.md "wikilink")のサポート（後ろの2つ用のLinux用ドライバは、現状では適切な性能での書き込みができない）
  - [ATAインタフェース](../Page/Advanced_Technology_Attachment.md "wikilink")
  - デジタルカメラ／ビデオカメラ用の [CCDコントローラ](../Page/CCDイメージセンサ.md "wikilink")
  - ホスト/デバイス用の [USB](../Page/ユニバーサル・シリアル・バス.md "wikilink") 2.0コントローラ、[VLYNQ](https://ja.wikipedia.org/wiki/VLYNQ "wikilink") ([:en:VLYNQ](https://ja.wikipedia.org/wiki/:en:VLYNQ "wikilink"))（[FPGA](https://ja.wikipedia.org/wiki/FPGA "wikilink")、[無線LAN](../Page/無線LAN.md "wikilink")、[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink") 用のインタフェース）、[MDIO](https://ja.wikipedia.org/wiki/MDIO "wikilink")([:en:MDIO](https://ja.wikipedia.org/wiki/:en:MDIO "wikilink")) に対応したEMAC（[イーサネット](../Page/イーサネット.md "wikilink")[MAC](../Page/媒体アクセス制御.md "wikilink")）などのコネクティビティ
  - [GPIO](https://ja.wikipedia.org/wiki/GPIO "wikilink")
  - 強化された[DMA](../Page/Direct_Memory_Access.md "wikilink")
  - [割り込みコントローラ](../Page/割り込み_\(コンピュータ\).md "wikilink")
  - デジタル[LCDコントローラ](https://ja.wikipedia.org/wiki/液晶ディスプレイ "wikilink")
  - [SPI](../Page/シリアル・ペリフェラル・インタフェース.md "wikilink")、[I²C](https://ja.wikipedia.org/wiki/I²C "wikilink")、[I²S](https://ja.wikipedia.org/wiki/Inter-IC_Sound "wikilink")、[UART](../Page/UART.md "wikilink")などのシリアルインタフェース
  - ヒストグラム、自動フォーカス、自動露光、自動ホワイトバランス (H3A) のアクセラレータ
  - 画像リサイズのためのアクセラレータ
  - アナログビデオ入出力用の [A/D](../Page/アナログ-デジタル変換回路.md "wikilink")・[D/Aコンバータ](../Page/デジタル-アナログ変換回路.md "wikilink")

## モデル

  - DM6443 - [ARM9](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink") + [Texas Instruments TMS320C64x+](https://ja.wikipedia.org/wiki/Texas_Instruments_TMS320C64x+ "wikilink") DSP + DaVinci Video (デコード) - 標準解像度の表示のためのビデオアクセラレータとネットワーキング
  - DM6446 - ARM9 + Texas Instruments TMS320C64x+ DSP + DaVinci Video (エンコードとデコード) - 標準解像度の撮影と表示のためのビデオアクセラレータとネットワーキング
  - DM6467 - ARM9 + Texas Instruments TMS320C64x+ DSP + DaVinci Video (エンコードとデコード) - 高解像度の撮影と表示のためのビデオアクセラレータとネットワーキング
  - DM643x - Texas Instruments TMS320C64x+ DSP
  - DM355 - ARM9 + DaVinci Video (エンコードとデコード) - [MPEG-4](../Page/MPEG-4.md "wikilink")/[JPEG](../Page/JPEG.md "wikilink") コプロセッサ
  - DM365 - ARM9 + DaVinci Video (エンコードとデコード) - [MPEG-2](../Page/MPEG-2.md "wikilink")/MPEG-4/[H.264](https://ja.wikipedia.org/wiki/H.264 "wikilink")/[VC-1](https://ja.wikipedia.org/wiki/VC-1 "wikilink")/JPEG コプロセッサ
  - DM368 - DM365の機能強化版

## ライブラリ

  - ほとんどの[TMS320](https://ja.wikipedia.org/wiki/TMS320 "wikilink") DSP は、周辺デバイスを制御するためのAPIである [TMS320チップ・サポート・ライブラリ](https://ja.wikipedia.org/wiki/TMS320チップ・サポート・ライブラリ "wikilink") (CSL) を含んでいる。 しかし DaVinci は ARM/Linux 側の Linuxデバイスドライバで周辺デバイスを制御する思想のため、現状では DM644x (ARM/DSP のデュアルコア) の CSL のサポートは DSP 側で使用できない。

## オペレーティング・システム

多くの DaVinci ベースのデバイスに内蔵される DSP は、一般的に TI の [DSP/BIOS](https://ja.wikipedia.org/wiki/DSP/BIOS "wikilink") [リアルタイムOS](../Page/リアルタイムオペレーティングシステム.md "wikilink") が動作している。複数の異種のコアが搭載されるデバイス(例えば DM644x)では、[DSP/BIOS Link](https://ja.wikipedia.org/wiki/DSP/BIOS_Link "wikilink") ドライバが、ARMとDSPの両側で動作し、2つのコアの間の通信を提供する。

多くのオペレーティング・システムが、[Davinci ARM](https://ja.wikipedia.org/wiki/Davinci_ARM "wikilink") と DaVinci の DSP/BIOS Link ドライバをサポートしている。

  - [モンタビスタ](https://ja.wikipedia.org/wiki/モンタビスタ "wikilink") [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")
  - [メンター・グラフィックス](https://ja.wikipedia.org/wiki/メンター・グラフィックス "wikilink") [Nucleus PLUS](https://ja.wikipedia.org/wiki/Nucleus_PLUS_\(operating_system\) "wikilink") [リアルタイムOS](../Page/リアルタイムオペレーティングシステム.md "wikilink")
  - [グリーン・ヒルズ・ソフトウェア](https://ja.wikipedia.org/wiki/グリーン・ヒルズ・ソフトウェア "wikilink") [INTEGRITY](https://ja.wikipedia.org/wiki/INTEGRITY "wikilink") [リアルタイムOS](../Page/リアルタイムオペレーティングシステム.md "wikilink")
  - [QNX](https://ja.wikipedia.org/wiki/QNX "wikilink") Neutrino
  - [Microsoft Windows CE](https://ja.wikipedia.org/wiki/Microsoft_Windows_CE "wikilink")
  - [LEOs (RTOS)](https://ja.wikipedia.org/wiki/LEOs_\(RTOS\) "wikilink")

## 外部リンク

  - [DaVinci ホームページ](http://focus.tij.co.jp/jp/paramsearch/docs/parametricsearch.tsp?family=dsp&sectionId=2&tabId=1852&familyId=1300)（日本語）
  - [DaVinci Developers Wiki](http://wiki.davincidsp.com) （TIが運営）

## 関連項目

  - [Texas Instruments OMAP](../Page/Texas_Instruments_OMAP.md "wikilink")

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")