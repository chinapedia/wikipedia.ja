> この記事は[Intel 8051](https://ja.wikipedia.org/wiki/Intel_8051)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:KL_Intel_P8051.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:SystèmeMicroproc.png "wikilink")

**Intel 8051** は[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")、[組み込みシステム](../Page/組み込みシステム.md "wikilink")用に[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が開発した[ハーバード・アーキテクチャ](../Page/ハーバード・アーキテクチャ.md "wikilink")をもつワンチップ[マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")である。1980年代から1990年代初頭まで極めて広範に用いられたが、2006年現在では様々な機能拡張を施された8051互換のプロセッサコアが20以上の製造業者から出荷されている。例えば[Atmel](https://ja.wikipedia.org/wiki/:en:Atmel "wikilink")、[Maxim IC](https://ja.wikipedia.org/wiki/マキシム・インテグレーテッド "wikilink")、[NXP](https://ja.wikipedia.org/wiki/NXPセミコンダクターズ "wikilink")、[Winbond](https://ja.wikipedia.org/wiki/Winbond "wikilink")、[Silicon Laboratoriesである](https://ja.wikipedia.org/wiki/Silicon_Laboratories "wikilink")。「8051」は型番であり、このファミリーのマイクロコントローラの名称は**MCS 51**である。

オリジナルの8051ファミリーは[NMOS](https://ja.wikipedia.org/wiki/NMOS "wikilink")テクノロジーで製造されたが、後には[CMOS](../Page/CMOS.md "wikilink")化され、80C51のように型名にCがついた。CMOS化にともない、消費電力が減り、電池で動く製品に採用しやすくなった。

## 主な特徴

  - 中央処理装置 ([CPU](../Page/CPU.md "wikilink"))、[RAM](../Page/Random_Access_Memory.md "wikilink")、[ROM](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")、 [シリアルポート](../Page/シリアルポート.md "wikilink")、[パラレルポート](../Page/パラレルポート.md "wikilink")、[割込用論理回路](../Page/割り込み_\(コンピュータ\).md "wikilink")、[タイマ](https://ja.wikipedia.org/wiki/タイマ "wikilink")その他を内蔵している。
  - [データバス](https://ja.wikipedia.org/wiki/データバス "wikilink") - 8ビット幅である。一回の操作で8ビットデータをアクセスすることができる。故に8bit[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")と呼ばれる。
  - [アドレスバス](https://ja.wikipedia.org/wiki/アドレスバス "wikilink") - 16ビット幅である。2<sup>16</sup>番地、即ち64KBのメモリ空間をRAM、ROM独立にアクセス可能である。
  - 内蔵RAM - 128バイト（データ用）。
  - 内蔵ROM - 4KB（プログラム用）。
  - 4ビットの双方向I/Oポート。
  - シリアルポート。
  - 2本の16ビットアップカウンタ。
  - 2レベルの割込優先順位。
  - 節電モード。

8051コアの特に有用な特徴に論理演算機能がある。これによって、ビットレベルで[ブーリアン型](../Page/ブーリアン型.md "wikilink")の演算が可能である。演算は内蔵[レジスタとRAM間で直接かつ効率的に行うことができる](../Page/レジスタ_\(コンピュータ\).md "wikilink")。この特徴によって8051は工業界に確固とした地位を築くに至った。他にも4つの独立したレジスタセットがあり、一般的に用いられるスタックへのレジスタ退避に比べ、割込時のレイテンシー（割込発生から、割込ルーチンを実行するまでの時間）を大きく改善することができた。

8051の非同期シリアル通信端末 ([UART](../Page/UART.md "wikilink")) はデータ長を9ビットにすることができ、[RS-485](https://ja.wikipedia.org/wiki/RS-485 "wikilink")環境下でアドレス付きの通信ができた。

8051ベースのマイクロコントローラは典型的には1個または2個のUARTと2個または3個のタイマ、128または256バイトの内蔵データRAM（その内16バイトはビットレベルでアドレス可能である）、128バイトまでのI/O、512バイトから128KBの内蔵プログラムメモリ、時にはかなりの容量の外付けRAMをプログラム空間用に持っている。オリジナルの8051コアは12クロックサイクルあたり1マシンサイクルを発生し、殆どの命令は1または2マシンサイクルで実行可能であった。そこで、12MHzのクロックを与えると、8051は1MIPSから0.5MIPSの性能を出した。現在一般に用いられている性能向上型の8051コアは1マシンサイクル当たりのクロックが6、4、2、果ては1クロックにまで低下しており、クロック自体も100MHz以上に達している。従って、遥かに高いMIPS値が可能である。SILab製品の全て、Dallas製品の一部、Atmel製品の若干が1クロックコアを持っている。

現在では130MHzから150MHzのシングルサイクル8051コアが[FPGA](../Page/FPGA.md "wikilink")などの[プログラマブルロジックデバイス](../Page/プログラマブルロジックデバイス.md "wikilink")用に存在し、インターネットから得られる。[ASIC](../Page/ASIC.md "wikilink")向けには数百MHzに及ぶものがある。例えば[e8051.comの](https://ja.wikipedia.org/wiki/#外部リンク "wikilink")[netlist](https://ja.wikipedia.org/wiki/netlist "wikilink")である。

現代の8051ベースのマイクロコントローラは、低電圧（ブラウンアウト）検出機能付きタイマ、オンチップ発振器、自己プログラム可能な[フラッシュROMプログラムメモリ](../Page/フラッシュメモリ.md "wikilink")、ROM内のブートローダーコード、EEPROMによる不揮発性データ記憶領域、[I2C](../Page/I2C.md "wikilink")、 [SPI](../Page/シリアル・ペリフェラル・インタフェース.md "wikilink")、[USBホストインタフェース](../Page/ユニバーサル・シリアル・バス.md "wikilink")、[PWM](https://ja.wikipedia.org/wiki/PWM "wikilink")信号発生器、AD/DA変換器、リアルタイムクロック、さらに多くのカウンタとタイマ、イン-サーキットのデバグ機能、より拡張された割込ソース、さらに強力な節電モードなどの特徴を含むことも一般的である。

[Cコンパイラの中には](../Page/C言語.md "wikilink")8051向きのものがある。プログラマは変数を8051が扱うことのできる6種類のメモリのどこに置くか指定することができ、8051特有のハードウェア的特徴（複数のレジスタバンク、ビット操作命令など）を活かすことができる。他の高級言語では[FORTH](../Page/Forth.md "wikilink")、[BASIC](../Page/BASIC.md "wikilink")、[Pascal](../Page/Pascal.md "wikilink")、[PL/M](https://ja.wikipedia.org/wiki/PL/M "wikilink")、[Modula-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink")が利用可能であるが、Cまたは[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")を用いることが多い。

8051の祖先である[8048は初代](../Page/Intel_8048.md "wikilink")[IBM PCのキーボードに用いられ](../Page/IBM_PC.md "wikilink")、キー操作をシリアルデータ列に変換し、計算機に送信した。8048ファミリーは2006年現在でもベーシックグレードのキーボードに用いられている。

**8031**は8051のコストカット版で、内蔵プログラムROMを持たない。

**8052**は8051の拡張版で、内蔵RAMが128バイトから256バイトに増え、4KBの内蔵ROMが8KBに増え、3本目の16ビットタイマを持っている。**8032**は8052から内蔵プログラムROMを除いたものである。後の8051ベースのマイクロコントローラがこれらの特徴を持っているので、8052と8032はさほど有用と見られなかった。

## 外部リンク

  - [8051 Forum](http://avr.15.forumer.com/index.php?showforum=7)
  - [e8051 netlist download](http://www.e8051.com/downloadw.htm)
  - [Microcontroller.com](http://Microcontroller.com)
  - [8051 Tutorial](http://www.8052.com/tut8051.phtml) (8052.com)
  - [Official 8051 FAQ (Link dead?)](http://microcontroller.com/Embedded.asp?did=93)
  - [Intel MCS 51 series microcontrollers](http://www.intel.com/design/mcs51/)
  - [Maxim/Dallas 8051 Drop-In microcontrollers](http://www.maximintegrated.com/products/microcontrollers/8051/index.cfm?CMP=WP-11)
  - [Open Core 8052 Cores with and without [Wishbone bus](https://ja.wikipedia.org/wiki/Wishbone_\(computer_bus\) "wikilink")](http://www.opencores.org/projects.cgi/web/t51/overview)
  - [8051 Macro Assembler ASEM-51](http://plit.de/asem-51/)
  - [SDCC, a free open-source C compiler](http://sdcc.sourceforge.net/)
  - [Free resources for 8051 and other development tools](http://www.devicetools.com/)

[Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink")