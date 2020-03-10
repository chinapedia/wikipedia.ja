> この記事は[Atmel AVR](https://ja.wikipedia.org/wiki/Atmel_AVR)から翻訳されています。


[250px](https://ja.wikipedia.org/wiki/ファイル:ATmega8_01_Pengo.jpg "wikilink").\]\] **AVR**（AVR）は、[Atmel](https://ja.wikipedia.org/wiki/Atmel "wikilink")社が[1996年](../Page/1996年.md "wikilink")に開発した、[RISC](../Page/RISC.md "wikilink")ベースの[8ビット](../Page/8ビット.md "wikilink")[マイクロコントローラ](https://ja.wikipedia.org/wiki/マイクロコントローラ "wikilink")（制御用IC）製品群の総称である。2016年以降は[Microchip社によって製造](https://ja.wikipedia.org/wiki/マイクロチップ・テクノロジー "wikilink")・販売されている。

## 概要

[PIC同様に回路構成が簡単でCPU](../Page/PIC_\(コントローラ\).md "wikilink")、[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")（[RAM](../Page/Random_Access_Memory.md "wikilink")、[ROM](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")）、[I/O](../Page/入出力.md "wikilink")、データ記憶用の[EEPROM](../Page/EEPROM.md "wikilink")、クロック発振回路、タイマーなどが1チップに収められており、書き込まれたプログラムにより制御される。

ISP ([In-System Programming](https://ja.wikipedia.org/wiki/In-System_Programming "wikilink")) に対応し、[コンパレータ](../Page/コンパレータ.md "wikilink")を内蔵する等、[i8051ピンコンパチ品や外部にRAMやI](../Page/Intel_8051.md "wikilink")/Oを増設する外部バスのあるものもあり、[電子工作](https://ja.wikipedia.org/wiki/電子工作 "wikilink")を行う人の間で人気がある。ISPには、In Circuit Serial Programming ([ICSP](https://ja.wikipedia.org/wiki/:en:ICSP "wikilink")) や[JTAG](../Page/JTAG.md "wikilink")という仕組みがある。

品種によっては、USBコントローラを内蔵した上でDFU対応Bootloaderをプログラムした状態で出荷されるものがあり、それらは外付け回路無しにUSB接続でプログラミング可能である。

また、ラインが変わっても基本的なCPUコアのアーキテクチャが変わらず、RAM空間がリニアである等、[C言語](../Page/C言語.md "wikilink")でのプログラミングを意識しており、さらに[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")を含んだ統合開発環境「AVR Studio」が無償配布され、[GCCも対応しているため安価に開発環境を構築できる](../Page/GNUコンパイラコレクション.md "wikilink")。

MCSエレクトロニクス社より4Kバイト(2Kワード)までのコード生成が無償試用できるBascomAVRというBASICを基調としたコンパイラーが公開されている。液晶表示コマンド等、即実用可能なコマンド満載でC言語やマシン語にアレルギーのある人でも簡単にAVRを試用できる。(ただしRAM未搭載のものは殆どのコマンド使用不可)

プログラム格納用のROMは全品種で[FlashROMを採用している](../Page/フラッシュメモリ.md "wikilink")。[ハーバード・アーキテクチャ](https://ja.wikipedia.org/wiki/ハーバード・アーキテクチャ "wikilink")である。

AVRという名前は、チップを設計した**A**lf Egil Bogen と **V**egard Wollanの名前と、**R**ISC から取られている。

## AVRの種類

起源となった90Sシリーズと、それを大容量化、I/Oを拡張したMegaシリーズ、高機能化・低消費電力化・低電圧対応したTinyシリーズがあり、今後は、MegaシリーズとTinyシリーズを主力する方向であるが、90Sシリーズもまだ多く使われている。

既に品種数がかなり多く、[廃品種](https://ja.wikipedia.org/wiki/廃品種 "wikilink")となったものも多いため、流通量が多い主な品種や著名な品種のみを取り上げ、特定顧客・特殊用途向けは割愛する。

  - 90Sシリーズ
      - 90S1200
      - 90S2313
      - 90S4433
      - 90S8515
      - 90S8535
  - Megaシリーズ
      - Mega1280/2560
      - Mega8/48/88/168/328
      - Mega161/162
      - Mega163/323
      - Mega169/329/649
      - Mega8515
      - Mega8535
      - Mega16/32
      - Mega64/128
  - Tinyシリーズ

| Tinyシリーズ | I/Oピン数 | 8bitタイマ | 16bitタイマ | PWM | Flash mem   | EEPROM      | SRAM        |
| -------- | ------ | ------- | -------- | --- | ----------- | ----------- | ----------- |
| tiny2313 | 18     | 1       | 1        | 4   | 2048|2kByte | 128|128Byte | 128|128Byte |
| tiny4313 | 18     | 1       | 1        | 4   | 4096|4kByte | 256|256Byte | 256|256Byte |
| tiny4    | 4      | 0       | 1        | 2   | 512|512Byte | 0|0Byte     | 32|32Byte   |
| tiny5    | 4      | 0       | 1        | 2   | 512|512Byte | 0|0Byte     | 32|32Byte   |
| tiny9    | 4      | 0       | 1        | 2   | 1024|1kByte | 0|0Byte     | 32|32Byte   |
| tiny10   | 4      | 0       | 1        | 2   | 1024|1kByte | 0|0Byte     | 32|32Byte   |
| tiny13   | 6      | 1       | 0        | 2   | 1024|1kByte | 64|64Byte   | 64|64Byte   |
| tiny20   | 12     | 1       | 1        | 3   | 2048|2kByte | 0|0Byte     | 128|128Byte |
| tiny24   | 12     | 1       | 1        | 4   | 2048|2kByte | 128|128Byte | 128|128Byte |
| tiny26   | 16     | 2       | 0        | 4   | 2048|2kByte | 128|128Byte | 128|128Byte |
| tiny40   | 18     | 1       | 1        | 2   | 4096|4kByte | 0|0Byte     | 256|256Byte |
| tiny44   | 12     | 1       | 1        | 4   | 4096|4kByte | 256|256Byte | 256|256Byte |
| tiny45   | 6      | 2       | 0        | 6   | 4096|4kByte | 256|256Byte | 256|256Byte |
| tiny85   | 6      | 2       | 0        | 6   | 8192|8kByte | 512|512Byte | 512|512Byte |

## AVRのレジスタセット

| 呼称         | 説明                   |
| ---------- | -------------------- |
| R0-25      | 汎用レジスタ R0-R15は即値演算不可 |
| X(R26,R27) | インデックスレジスタX          |
| Y(R28,R29) | インデックスレジスタY          |
| Z(R30,R31) | インデックスレジスタZ          |
| PC         | プログラムカウンタ            |
| SP         | スタックポインタ             |
| SREG       | ステータスレジスタ            |

  -
  -
## 命令セット

  - 16ビット固定長
  - C言語でのプログラミングを意識した命令群
  - メモリへのアクセスはロードとストアのみであり、演算はレジスタとレジスタあるいはイミディエイトのみ
  - イミディエイト減算やキャリー付加減算のサポート
  - Megaシリーズは乗算命令をサポート

### 主なアドレッシングモード

| 呼称      | 説明                                                   |
| ------- | ---------------------------------------------------- |
| イミディエイト | 直接8ビットの値を指定する。                                       |
| 直接      | 直接16ビットの番地を指定する。                                     |
| 間接      | X,Y,Zレジスタで番地を指定する。ディスプレースメント付、ポストインクリメント、プリデクリメントも可。 |

  -
## 関連項目

  - [PIC](../Page/PIC_\(コントローラ\).md "wikilink") - [Microchip社が開発したマイクロコントローラ](https://ja.wikipedia.org/wiki/マイクロチップ・テクノロジー "wikilink")。元AVRの競合製品だが現在は併売されている
  - [Arduino](https://ja.wikipedia.org/wiki/Arduino "wikilink") - AVRを利用した[オープンソースハードウェア](../Page/オープンソースハードウェア.md "wikilink")
  - [組み込みシステム](../Page/組み込みシステム.md "wikilink")
  - [シーケンス制御](https://ja.wikipedia.org/wiki/シーケンス制御 "wikilink")

## 外部リンク

  - [Atmel本社](http://www.atmel.com/)

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")