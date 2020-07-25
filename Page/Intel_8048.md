> この記事は[Intel 8048](https://ja.wikipedia.org/wiki/Intel_8048)から翻訳されています。


[KL_Intel_P8048H.jpg](https://ja.wikipedia.org/wiki/File:KL_Intel_P8048H.jpg "fig:KL_Intel_P8048H.jpg") [KL_Intel_D8749.jpg](https://ja.wikipedia.org/wiki/File:KL_Intel_D8749.jpg "fig:KL_Intel_D8749.jpg") [Intel_8049_Microcontroller.jpg](https://ja.wikipedia.org/wiki/File:Intel_8049_Microcontroller.jpg "fig:Intel_8049_Microcontroller.jpg") **Intel 8048**またはそのシリーズである**Intel MCS-48**は[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")初の[マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")である。当初のラインナップには8048、8035、8748が存在した。これらは元々NMOSプロセスで生産されていたが、1980年代初めにはCMOS版も供給された。既存の古い設計をサポートするため、1990年代に入っても製造された。

## 構成

8048のアーキテクチャは[ハーバード・アーキテクチャ](../Page/ハーバード・アーキテクチャ.md "wikilink")の変形であり、プログラム用ROM（内蔵または外付け）とデータ用RAMを分離して持っていた。27個のI/Oポートを持つが、それらは独自のアドレス空間にマップされ、プログラムやデータとは分離されている。また1回路の8bitタイマ・カウンタを自前でもっていた。8048の内蔵ROMは1KBで、外付けのプログラム用[ROMを用いることもできた](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")。内蔵RAMは64バイトであった。ROMの種類、メモリ容量によってファミリーを形成し、例えば**8049**は2 KiBのマスクROM（**8749**は[EPROM](../Page/EPROM.md "wikilink")）を内蔵しており、このROMは4 KiBの外部ROMで置き換えることができる。

外部から供給されたクロックは内部の発振器ブロックによって15の内部フェーズに分割される。そこで、最高動作周波数である11MHzの水晶発振器を接続すると、0.73MIPS（1クロック命令について）の性能が出る。1CPUサイクルで実行できる1バイト長の命令もあるが、多くの命令は2CPUサイクルないし2バイトを必要とする。従って実際の動作速度は0.5MIPS程度である。

## MCS-48ファミリー

*8049*は2KBのマスク[ROM](../Page/Read_only_memory.md "wikilink")（8748と8749は[EPROM](../Page/EPROM.md "wikilink")）と128バイトの[RAM](../Page/Random_Access_Memory.md "wikilink")、27個の[I/Oポート](https://ja.wikipedia.org/wiki/I/Oポート "wikilink")を搭載し、ROMは4KBの外部ROMに置き換えることができた。マイクロコントローラのクロック発振器ブロックは入力クロックを15分周し、最大11MHzで0.73[MIPS](https://ja.wikipedia.org/wiki/MIPS "wikilink")の駆動が可能であった。命令の7割は1命令サイクルあたり1バイトで、3割は2サイクル・2バイトを必要としたため、実際のパフォーマンスは0.5MIPSほどになる。

フィリップス・セミコンダクタ（現[NXP](https://ja.wikipedia.org/wiki/NXPセミコンダクターズ "wikilink")）がこのシリーズを生産するライセンスを所有しており、このアーキテクチャをベースにMAB8400ファミリとして開発していた。これらは[I2C](../Page/I2C.md "wikilink")インターフェースを統合した最初のマイクロコントローラで、[フィリップス](../Page/フィリップス.md "wikilink")の最初のCDプレーヤー「CD-100」に用いられた\[1\]。

Intel *8748*はクロック発振器を内蔵しており、8ビットタイマーを2個、I/Oポートを27個、64バイトのRAMと1KBのEPROMを搭載していた。2KB EPROMと128バイトのRAMを搭載したバージョンは*8749*としてリリースされた。

| デバイス | 内部ROM                                                                    | メモリ         | 注釈                                                         |
| ---- | ------------------------------------------------------------------------ | ----------- | ---------------------------------------------------------- |
| 8020 | 1K × 8 ROM                                                               | 64 × 8 RAM  | 8048のサブセット、20ピン、13本のI/O                                    |
| 8021 | 1K × 8 ROM                                                               | 64 × 8 RAM  | 8048のサブセット、28ピン、21本のI/O                                    |
| 8022 | 2K × 8 ROM                                                               | 64 × 8 RAM  | 8048のサブセット、[A/Dコンバータ](../Page/アナログ-デジタル変換回路.md "wikilink") |
| 8035 | 無し                                                                       | 64 × 8 RAM  |                                                            |
| 8039 | 無し                                                                       | 128 × 8 RAM |                                                            |
| 8040 | 無し                                                                       | 256 × 8 RAM |                                                            |
| 8048 | 1K × 8 ROM                                                               | 64 × 8 RAM  |                                                            |
| 8049 | 2K × 8 ROM                                                               | 128 × 8 RAM |                                                            |
| 8050 | 外部ROMソケット                                                                | 256 × 8 RAM |                                                            |
| 8748 | 1K × 8 EPROM                                                             | 64 × 8 RAM  |                                                            |
| 8749 | 2K × 8 EPROM                                                             | 128 × 8 RAM |                                                            |
| 8648 | 1K × 8 [OTP EPROM](https://ja.wikipedia.org/wiki/PROM#OTPROM "wikilink") | 64 × 8 RAM  |                                                            |

| デバイス   | 内部ROM            | メモリ         | 注釈                                   |
| ------ | ---------------- | ----------- | ------------------------------------ |
| 8041   | 1K × 8 ROM       | 64 × 8 RAM  | Universal Peripheral Interface (UPI) |
| 8041AH | 1K × 8 ROM       | 128 × 8 RAM | UPI                                  |
| 8741A  | 1K × 8 EPROM     | 64 × 8 RAM  | UPI、8041のEPROM版                      |
| 8741AH | 1K × 8 OTP EPROM | 128 × 8 RAM | UPI、8041AHのOTP EPROM版                |
| 8042AH | 2K × 8 ROM       | 256 × 8 RAM | UPI                                  |
| 8742   | 2K × 8 EPROM     | 128 × 8 RAM | UPI、EPROM版                           |
| 8742AH | 2K × 8 OTP EPROM | 256 × 8 RAM | UPI、8042AHのOTP EPROM版                |

## 応用

8048は後に開発された[8051に駆逐されつつあるが](../Page/Intel_8051.md "wikilink")、21世紀を迎えた時点でもなお極めて広く用いられている。コストが低く、広範な応用範囲を持ち、1バイト命令セットによってメモリ利用効率が高く、枯れた開発用ツールが存在することがその理由である。そのため、大量生産される民生用電子機器、例えばTVのリモコン、玩具等といったコストダウンが至上命令であるような製品によく用いられる。

8048は[マグナボックス](../Page/マグナボックス.md "wikilink")[オデッセイ](../Page/オデッセイ_\(ゲーム機\).md "wikilink")、[コルグ](https://ja.wikipedia.org/wiki/コルグ "wikilink")Tridentシリーズ、コルグPoly-61\[2\]、[ローランド](../Page/ローランド.md "wikilink")Jupiter-4およびProMars\[3\][アナログシンセサイザー](../Page/アナログシンセサイザー.md "wikilink")に使用された。

オリジナルの[IBM PCキーボードは内蔵マイクロコントローラとして](../Page/IBM_PC.md "wikilink")8048を使用していた\[4\]。PC/ATではPCのI/Oアドレス0x60～0x63にあるIntel 8255周辺機器インターフェースチップを0x60-0x64にある8042に置き換えられた\[5\]。キーボードインターフェースを管理するだけでなく、8042はATの[Intel 80286](../Page/Intel_80286.md "wikilink") CPUのA20ラインを制御、または80286をリセットするコマンドを送ることができた。（[80386やそれ以降のプロセッサとは異なり](../Page/Intel_80386.md "wikilink")、80286はリセットする以外に[プロテクトモード](../Page/プロテクトモード.md "wikilink")から[リアルモード](../Page/リアルモード.md "wikilink")に戻る方法がなかった。）後のPC互換機では8042の機能を[スーパーI/O](https://ja.wikipedia.org/wiki/スーパーI/O "wikilink")チップに統合している。[日本電気](../Page/日本電気.md "wikilink")[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")では、キーボード側は8048を、本体側は8251Aをもち、I/Oアドレス`43`[`H`](https://ja.wikipedia.org/wiki/16進数 "wikilink")でアクセスすることができた\[6\]。キーボードと本体の間は[シリアル通信](../Page/シリアル通信.md "wikilink")が行われた。[シャープ](../Page/シャープ.md "wikilink")[X1シリーズでも使用された](../Page/X1_\(コンピュータ\).md "wikilink")。

他の変種としては、ROMを持たない8035が[任天堂](../Page/任天堂.md "wikilink")のアーケードゲーム『[ドンキーコング](../Page/ドンキーコング.md "wikilink")』に用いられた。マイクロコントローラの用途としては変わっているが、ゲームのバックに音楽を流すためである。

## 関連項目

  - [Intel 8051](../Page/Intel_8051.md "wikilink") - 8048に比べ、高速化がなされ、[シリアルインタフェースも内蔵するようになった](../Page/シリアルポート.md "wikilink")。またメモリ空間の拡大と命令の強化がなされた。

## 参考文献

  - MCS-48

<!-- end list -->

  - *MCS-48 Single Component Microcomputer*, Applications Seminar Notebook, 1978, Intel Corporation.

  - , 1978, Intel Corporation.

  - [Lionel Smith, Cecil Moore: *Serial I/O and Math Utilities for the 8049 Microcomputer*](https://docs.google.com/file/d/0B9rh9tVI0J5mRFNONzlxTmNQWUk/edit?usp=sharing), Application Note AP-49, January 1979, Intel Corporation.

  - *A High-Speed Emulator for Intel MCS-48 Microcomputers*, Application Note AP-55A, August 1979, Intel Corporation.

  - Phil Dahm, Stuart Rosenberg: *Intel MCS-48 and UPI-41A Microcontrollers*, Reliability Report RR-25, December 1979, Intel Corporation.

  - *Microcontroller Handbook*, Intel 1984, Order number 210918-002.

  - *8-Bit Embedded Controllers*, Intel 1991, Order number 270645-003.

<!-- end list -->

  - UPI-41

<!-- end list -->

  - *UPI-41A User's Manual*, Intel 1980, Order number 9800504-02 Rev. B.

  - , October 1993, Order number 231318-006, Intel Corporation.

  - Johan Beaston, Jim Kahn: *An 8741A/8041A Digital Cassette Controller*, Application Note AP-90, May 1980, Intel Corporation.

## 外部リンク

  - [MCS-48](http://www.st.rim.or.jp/~nkomatsu/intel8bit/i8048.html) - try's pageの一部。命令セットなども詳しく説明されている。
  - [MCS-48 family architecture](http://home.mnet-online.de/al/mcs-48/mcs-48.pdf) ([PDF](../Page/Portable_Document_Format.md "wikilink"))
  - [Coprolite 8048 Projects](http://coprolite.com/8048.html)
  - [The PS/2 Keyboard Interface](http://www.computer-engineering.org/ps2keyboard/) - PS/2キーボードインターフェースの解説（英語）。

## 脚注

[Category:マイクロコントローラ](https://ja.wikipedia.org/wiki/Category:マイクロコントローラ "wikilink") [Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink")

1.  [Datasheet (pdf)](http://www.datasheetarchive.com/dl/Datasheets-110/DSAP005622.pdf) Philips MAB8400-Family
2.
3.
4.
5.
6.