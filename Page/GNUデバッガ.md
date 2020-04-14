> この記事は[GNUデバッガ](https://ja.wikipedia.org/wiki/GNUデバッガ)から翻訳されています。


**GNUデバッガ**（単に**GDB**とも）は、[GNU](../Page/GNU.md "wikilink")ソフトウェア・システムで動く標準の[デバッガ](../Page/デバッガ.md "wikilink")である。 これは、多くの[Unix系](../Page/Unix系.md "wikilink")システムで動作可能な移植性の高いデバッガであり、[Ada](../Page/Ada.md "wikilink")、[C言語](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")、[FORTRAN](https://ja.wikipedia.org/wiki/Fortran "wikilink")、[FreeBASIC](../Page/FreeBASIC.md "wikilink")といった[プログラミング言語](../Page/プログラミング言語.md "wikilink")に対応している。

## 歴史

GDBは初め、[GNU Emacs](../Page/GNU_Emacs.md "wikilink") が「そこそこ安定化 [1](http://www.gnu.org/philosophy/stallman-kth.html)」した後、[1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink") に[GNU](../Page/GNU.md "wikilink") システムの一部として [リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink") が書いた。GDBは、[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL) の下でリリースしている [フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink") である。これは、[バークレーUnixの配布物件についてくる](../Page/BSD.md "wikilink")[Dbx デバッガをモデルにしている](https://ja.wikipedia.org/wiki/Dbx_デバッガ "wikilink")。

[ジョン・ギルモア](../Page/ジョン・ギルモア.md "wikilink") が [シグナスソリューションズ](../Page/シグナスソリューションズ.md "wikilink") に勤務していた [1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")から[1993年](../Page/1993年.md "wikilink")まで保守をしていた。

## 技術詳細

### 機能

GDBは、[プログラムの実行の変更や追跡といった充実した機能を提供する](../Page/プログラム_\(コンピュータ\).md "wikilink")。プログラム内部の [変数](../Page/変数_\(プログラミング\).md "wikilink") の値を修正したり、監視したりすることや、プログラムの通常の動作とは別に [関数](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink") を呼び出すことができる。

[2003年](../Page/2003年.md "wikilink") 現在、GDBのターゲット・プロセッサは、以下のとおりである。

  - [Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")
  - [ARM](../Page/ARMアーキテクチャ.md "wikilink")
  - [H8](../Page/H8.md "wikilink")/300
  - [System/370](https://ja.wikipedia.org/wiki/System/370 "wikilink") / [System 390](../Page/System_z.md "wikilink")
  - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink") / [x64](https://ja.wikipedia.org/wiki/x64 "wikilink")
  - [IA-64](../Page/Itanium.md "wikilink")「Itanium」
  - [Motorola 68000](../Page/MC68000.md "wikilink")
  - [MIPS](../Page/MIPSアーキテクチャ.md "wikilink")
  - [PA-RISC](../Page/PA-RISC.md "wikilink")
  - [PowerPC](../Page/PowerPC.md "wikilink")
  - [SuperH](../Page/SuperH.md "wikilink")
  - [SPARC](../Page/SPARC.md "wikilink")
  - [VAX](../Page/VAX.md "wikilink")

標準リリースでサポートされている、さほど有名でないターゲット・プロセッサには、以下がある。

  - [AMD 29000](https://ja.wikipedia.org/wiki/AMD_29000 "wikilink")
  - [ARC](https://ja.wikipedia.org/wiki/Advanced_RISC_Computing "wikilink")
  - [AVR](../Page/Atmel_AVR.md "wikilink")
  - [CRIS](https://ja.wikipedia.org/wiki/CRIS "wikilink")
  - [D10V](https://ja.wikipedia.org/wiki/D10V "wikilink") / [D30V](https://ja.wikipedia.org/wiki/D30V "wikilink")
  - [FR-30](https://ja.wikipedia.org/wiki/FR-30 "wikilink") / [FR-V](https://ja.wikipedia.org/wiki/FR-V "wikilink")
  - [Intel i960](../Page/Intel_i960.md "wikilink")
  - [M32R](https://ja.wikipedia.org/wiki/M32R "wikilink")
  - [68HC11](https://ja.wikipedia.org/wiki/Freescale_68HC11 "wikilink")
  - [Motorola 88000](https://ja.wikipedia.org/wiki/88000_\(CPU\) "wikilink")
  - [MCORE](https://ja.wikipedia.org/wiki/MCORE "wikilink")
  - [MN10200](https://ja.wikipedia.org/wiki/MN10200 "wikilink") / [MN10300](https://ja.wikipedia.org/wiki/MN10300 "wikilink")
  - [NS32K](../Page/NS320xx.md "wikilink")
  - [Stormy16](https://ja.wikipedia.org/wiki/Stormy16 "wikilink")
  - [V850](https://ja.wikipedia.org/wiki/V850 "wikilink")
  - [Z8000](../Page/Z8000.md "wikilink")

M32RやV850といった、日本製のCPUにもコンパイル時の組込み[シミュレータがある](https://ja.wikipedia.org/wiki/命令セット・シミュレータ "wikilink")。

### 遠隔デバッグ

GDBには「遠隔」モードがあり、しばしば組込みシステムのデバッグで使われる。遠隔操作では、GDBとデバッグ対象のプログラムは別のマシンで動作する。GDBは、GDBプロトコルをシリアルやTCP/IP経由で理解する遠隔「スタブ」と通信することができる。

gdbを使い、動いている[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")をソース・レベルでデバッグするKGDBでも、同じモードを使っている。kgdbを使い、カーネル開発者は、アプリケーション・プログラムのようにカーネルをデバッグできる。カーネル・コードに[ブレークポイント](https://ja.wikipedia.org/wiki/ブレークポイント "wikilink")を設定でき、ステップ動作ができ、変数を参照できる。ハードウェアのデバッグ・レジスタ (debugging register) が使える[アーキテクチャでは](../Page/コンピュータ・アーキテクチャ.md "wikilink")、ウォッチポイントが設定できる。ウォッチポイントとは、特定のメモリー・アドレスを実行したり、アクセスしたときのブレークポイントをかけるものである。kgdbには、[シリアルケーブル](https://ja.wikipedia.org/wiki/シリアルケーブル "wikilink")や[イーサネット](../Page/イーサネット.md "wikilink")を使ってデバッグ対象マシンに繋がったマシンが必要となる。[FreeBSD](../Page/FreeBSD.md "wikilink")では、[FireWire](../Page/IEEE_1394.md "wikilink") [DMAを使ったデバッグもできる](../Page/Direct_Memory_Access.md "wikilink")。

### 特徴

このデバッガは、[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") (GUI) がなく、[コマンドラインユーザインタフェース](../Page/キャラクタユーザインタフェース.md "wikilink") (CUI) である。[DDD](https://ja.wikipedia.org/wiki/Data_Display_Debugger "wikilink")、[Eclipse CDT](http://download.eclipse.org/tools/cdt/docs/tutorials/debug_tutorial/cdt_w_debug.htm)、[GDBtk](https://ja.wikipedia.org/wiki/GDBtk "wikilink")/[Insight](http://sources.redhat.com/insight/)、[GNU Emacs](../Page/GNU_Emacs.md "wikilink") の「GUDモード」といった[フロントエンド](../Page/フロントエンド.md "wikilink")がある。 これらは、[統合開発環境](../Page/統合開発環境.md "wikilink") のデバッガ同様の機能を備えている。

[メモリリーク](../Page/メモリリーク.md "wikilink")検出といった、若干のデバッグ用ツールがGDBとともに働くように設計している。

## コマンド例

`gdb prog.out      debug prog.out`
`gdb > run         run`

## セッション例

次は、プログラムの[スタック・トレース](https://ja.wikipedia.org/wiki/スタック・トレース "wikilink")をとるGDBセッションの例である。

    GNU gdb Red Hat Linux (6.3.0.0-1.21rh)
    Copyright 2004 Free Software Foundation, Inc.
    GDB is free software, covered by the GNU General Public License, and you are
    welcome to change it and/or distribute copies of it under certain conditions.
    Type "show copying" to see the conditions.
    There is absolutely no warranty for GDB.  Type "show warranty" for details.
    This GDB was configured as "i386-redhat-linux-gnu"...Using host libthread_db library "/lib/libthread_db.so.1".

    (gdb) run
    Starting program: /home/sam/programming/crash
    Reading symbols from shared object read from target memory...done.
    Loaded system supplied DSO at 0xc11000
    This program will demonstrate gdb

    Program received signal SIGSEGV, Segmentation fault.
    0x08048428 in function_2 (x=24) at crash.c:22
    22         return *y;
    (gdb) edit
    (gdb) shell gcc crash.c -o crash -gstabs+
    (gdb) run
    The program being debugged has been started already.
    Start it from the beginning? (y or n) y
    warning: cannot close "shared object read from target memory": File in wrong format
    `/home/sam/programming/crash' has changed; re-reading symbols.
    Starting program: /home/sam/programming/crash
    Reading symbols from shared object read from target memory...done.
    Loaded system supplied DSO at 0xa3e000
    This program will demonstrate gdb
    24
    Program exited normally.
    (gdb) quit

プログラムを動かすと､セグメント違反の原因を見つけた後、正しく振る舞うようプログラムを編集する。訂正したプログラムが、[GCCで再コンパイルした後に動作する](../Page/GNUコンパイラコレクション.md "wikilink")。

## 参考文献

  - [Richard M. Stallman](../Page/リチャード・ストールマン.md "wikilink"), [Roland Pesch](https://ja.wikipedia.org/wiki/Roland_Pesch "wikilink"), [Stan Shebs](https://ja.wikipedia.org/wiki/Stan_Shebs "wikilink"), et al., *Debugging with GDB* ([Free Software Foundation](https://ja.wikipedia.org/wiki/Free_Software_Foundation "wikilink"), 2002) ISBN 1-882114-88-4

## 外部リンク

  - [GDBホームページ](http://www.gnu.org/software/gdb/)
  - [gdbのドキュメント「Debugging with GDB」](http://sourceware.org/gdb/current/onlinedocs/gdb.html) (htmlと400ページ以上のPDF)
  - [GDBの内部資料](http://sourceware.org/gdb/current/onlinedocs/gdbint.html)
  - [入門書](http://users.actcom.co.il/~choo/lupg/tutorials/debugging/debugging-with-gdb.html)
  - [Linuxカーネルのデバッグ用gdbバックエンド、kgdb](http://kgdb.linsyssoft.com)
  - [Peter Jay SalzmanのGDB案内](http://www.dirac.org/linux/gdb)

[Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:デバッガ](https://ja.wikipedia.org/wiki/Category:デバッガ "wikilink")