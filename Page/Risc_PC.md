> この記事は[Risc PC](https://ja.wikipedia.org/wiki/Risc_PC)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Acorn_Risc_PC_600.jpg "wikilink")

**Risc PC** は[エイコーン・コンピュータ](https://ja.wikipedia.org/wiki/エイコーン・コンピュータ "wikilink")が[1994年](../Page/1994年.md "wikilink")にリリースした[RISC OS](https://ja.wikipedia.org/wiki/RISC_OS "wikilink")/[ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")のコンピュータであり、[Acorn Archimedes](https://ja.wikipedia.org/wiki/Acorn_Archimedes "wikilink") の後継である。開発コード名は"[Medusa](../Page/メドゥーサ.md "wikilink")"。

Archimedes と同様、Risc PC でも RISC OS [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")は[ROMモジュール上に格納している](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")。Risc PC ではROMベースのOSを拡張し、ディスク上の構成情報や以前はROM上にあったアプリケーションなどを含むディレクトリ構造を扱えるようにしている。

## 仕様と技術的詳細

  - **メモリ**: [SIMM](../Page/SIMM.md "wikilink")、2スロット、最大256MB
  - **ビデオ**: VIDC20 コントローラ、オプションでデュアルポートVRAM（最大2MB）を装備
  - **拡張バス**: Archimedes と同様の[Eurocard](https://ja.wikipedia.org/wiki/Eurocard "wikilink")サイズの Podule をサポート。また、バス上の最初の2つの Podule では [DMA](../Page/Direct_Memory_Access.md "wikilink") をサポートしている。
  - **オペレーティングシステム**: RISC OS 3.5 (Risc PC 600)、RISC OS 3.6 (Risc PC 700)、RISC OS 3.7 (StrongARM Risc PC)。後に RISC OS 4 が標準で使われるようになった。
  - **ケース**: Cambridge Product Design（[BBC Microのデザインをした会社](../Page/BBC_Micro.md "wikilink")）の工業デザイナー Allen Boothroyd のデザイン。スライスと呼ばれる拡張筐体を重箱のように重ねて、内部の拡張用の空間を広げる形になっている。各拡張筐体の後部には2個の Podule ベイがあり、前面には2個のドライブベイ（一方は3.5インチ、もう一方は5.25インチ）がある。リトラクタブル式フラップでベイの前面を隠すことができる。プラスチック製のケースの内面はニッケル塗料がスプレーされていて、電磁波放射の規制に対応している。
  - **ポート**: シリアル、パラレル、PS/2キーボード、Acornマウス、ヘッドホン音声出力、[DE15](../Page/D-subminiature.md "wikilink") [VGA](../Page/Video_Graphics_Array.md "wikilink")、ネットワーク（オプション）
  - **CPU**: 2つのプロセッサスロットがあり、[ドーターボード](../Page/ドーターボード.md "wikilink")上に次のいずれかのチップを実装可能: [ARM](../Page/ARMアーキテクチャ.md "wikilink")610 （30 MHz、33 MHz）、ARM700 （33 MHz、プロトタイプのみ）、ARM710 （40 MHz）、ARM810 （55 MHz、プロトタイプのみ）、[StrongARM](../Page/StrongARM.md "wikilink") （203 MHz、236 MHz、300 MHz）。コプロセッサとして、[Intel 486](https://ja.wikipedia.org/wiki/Intel_486 "wikilink") および [Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")ベースのCPUカード（133MHzまで）と[DSPを使ったCPUカード](../Page/デジタルシグナルプロセッサ.md "wikilink")（サードパーティ）がある。
  - **形状**: 117（二段重ねの場合 182）×355×384 mm (HxWxD)

## 年表

  - 1994年 - Risc PC 600 リリース（30MHz ARM6 CPU）
  - 1995年 - ARM7 CPU アップグレードと Risc PC 700 を新たにリリース
  - 1996年 - StrongARM CPU アップグレードをリリース。
  - 2000年 - 5月、Castle Technology から Kinetic Risc PC がリリースされる。[1](http://www.iconbar.com/news/news2.html)
  - 2001年 - Viewfinder Podule という [AGP](../Page/Accelerated_Graphics_Port.md "wikilink") アダプターにより、IBM PC 用 AGP グラフィックカードが使えるようになった。
  - 2003年 - エイコーンによる Risc PC の製造が終了。

なお、Kinetic Risc PC は、Risc PC 用CPUカードであり、カード上にメモリを搭載している。これは、Risc PC の[FSBが遅いため](../Page/フロントサイドバス.md "wikilink")、マザーボード上のメモリへのアクセスがCPUのクロックに比較して極めて低速になってしまったことへの対処である。

## Risc PC の現在

Risc PC の設計を継承した以下のようなマシンが今日でも販売されているが、Risc PC 自体は既に販売終了している。

  - [Iyonix PC](http://www.iyonix.com/) - [XScale](../Page/XScale.md "wikilink")と[PCIバスを採用](../Page/Peripheral_Component_Interconnect.md "wikilink")（Castle Technology）
  - [A9Home](http://www.advantage6.com/products/A9home.html) - [サムスン電子](../Page/サムスン電子.md "wikilink") S3C2440 ARM プロセッサを採用（Advantage6）
  - RiscStation R7500 - ARM7500-FE プロセッサを採用

## 関連項目

  - [BBC Micro](../Page/BBC_Micro.md "wikilink")
  - [Acorn Archimedes](https://ja.wikipedia.org/wiki/Acorn_Archimedes "wikilink")

## 外部リンク

  - [Acorn's famous 10-slice **Rocket Ship** RiscPC including pizza oven and kitchen sink](http://www.d1.dion.ne.jp/~r_high/memorial/rocketship.html)
  - [Advantage six reveal A9Home to the press](http://www.drobe.co.uk/riscos/artifact1350.html)
  - [Castle reveal Kinetic Risc PC to the press](http://www.iconbar.com/hardware/kinetic/)
  - [Risc PC 10th Birthday](http://www.iconbar.com/Happy_10th_Birthday_Risc_PC/news430.html)
  - [Risc PC production ceases](http://www.iconbar.com/R.I.P.__Risc_PC/news374.html)
  - [Castle bids farewell to Risc PC](http://www.drobe.co.uk/riscos/artifact869.html)

[Category:パーソナルコンピュータ_(製品)](https://ja.wikipedia.org/wiki/Category:パーソナルコンピュータ_\(製品\) "wikilink")