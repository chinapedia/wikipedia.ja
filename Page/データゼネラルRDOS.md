> この記事は[データゼネラルRDOS](https://ja.wikipedia.org/wiki/データゼネラルRDOS)から翻訳されています。


**データゼネラルRDOS (*R****eal-time **D**isk **O**perating **S**ystem) は、*1970年にリリースされた[リアルタイム](../Page/リアルタイムオペレーティングシステム.md "wikilink") [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である。\[1\] このソフトウェアは、同社の評判が高い[Novaと](https://ja.wikipedia.org/wiki/データゼネラルNova "wikilink")[Eclipse](../Page/Eclipse_\(コンピュータ\).md "wikilink")[ミニコンピュータ](../Page/ミニコンピュータ.md "wikilink")に同梱し販売されていた。\[2\]

## 概要

RDOSは[マルチタスク](../Page/マルチタスク.md "wikilink")を実行することができ、64[kBのメモリ空間内にある](https://ja.wikipedia.org/wiki/キビバイト "wikilink")2つの[グラウンド](../Page/プロセス.md "wikilink") (フォアグラウンドとバックグラウンド ) のそれぞれで、同時に最大32個の "タスク"（現在の[スレッドと同様](../Page/スレッド_\(コンピュータ\).md "wikilink")）を実行できた。それ以降のバージョンのRDOSは、データゼネラルの[16ビット](../Page/16ビット.md "wikilink") Eclipseミニコンピュータラインと互換性があった。\[3\]

RDOSの簡易版は、リアルタイムのバックグラウンド機能やフォアグラウンド機能を備えていないものの、マルチスレッドおよびマルチユーザーのデータゼネラル ビジネス Basic ([Data General Business Basic](https://ja.wikipedia.org/wiki/データ一般事業基本 "wikilink"))を実行することが可能なデータゼネラル ディスクオペレーティングシステム (Data General Diskette Operating System) \[4\] (DG-DOS、または現在は多少まぎわしいもののシンプルにDOS) と呼ばれた。もう1つ関連するオペレーティングシステムは、ディスクレス環境用のリアルタイムオペレーティングシステムであるRTOSである。 [microNOVAベースの](https://ja.wikipedia.org/wiki/データゼネラルNova#microNOVA "wikilink") "Micro Products" マイクロミニコンピューター上のRDOSは、DG/RDOSと呼ばれることもある。 \[5\]

RDOSは、1980年代初頭にAOS/VSやMP/AOS(小規模システムではMP/OS)など、データゼネラルのAOSファミリーのオペレーティングシステムによって置き換わった。

### コマンド

次のリストの[コマンドが](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink") RDOS/DOS CLIで使用できる。\[6\]

  - [ALGOL](../Page/ALGOL.md "wikilink")
  - [APPEND](https://ja.wikipedia.org/wiki/append "wikilink")
  - [ASM](https://ja.wikipedia.org/wiki/Assembly_language "wikilink")
  - [BASIC](../Page/BASIC.md "wikilink")
  - BATCH
  - BOOT
  - BPUNCH
  - BUILD
  - CCONT
  - CDIR
  - CHAIN
  - CHATR
  - CHLAT
  - CLEAR
  - CLG
  - COPY
  - CPART
  - CRAND
  - CREATE
  - DEB
  - [DELETE](https://ja.wikipedia.org/wiki/del_\(command\) "wikilink")
  - DIR
  - DISK
  - DUMP
  - EDIT
  - ENDLOG
  - ENPAT
  - EQUIV
  - EXFG
  - FDUMP
  - FGND
  - FILCOM
  - FLOAD
  - [FORT](https://ja.wikipedia.org/wiki/Fortran "wikilink")
  - [FORTRAN](https://ja.wikipedia.org/wiki/Fortran "wikilink")
  - FPRINT
  - GDIR
  - GMEM
  - GSYS
  - GTOD
  - INIT
  - LDIR
  - LFE
  - LINK
  - LIST
  - LOAD
  - LOG
  - MAC
  - MCABOOT
  - MDIR
  - MEDIT
  - MESSAGE
  - MKABS
  - MKSAVE
  - MOVE
  - NSPEED
  - OEDIT
  - OVLDR
  - PATCH
  - POP
  - [PRINT](https://ja.wikipedia.org/wiki/print_\(command\) "wikilink")
  - PUNCH
  - RDOSSORT
  - RELEASE
  - [RENAME](https://ja.wikipedia.org/wiki/ren_\(command\) "wikilink")
  - REPLACE
  - REV
  - RLDR
  - SAVE
  - SDAY
  - SEDIT
  - SMEM
  - SPDIS
  - SPEBL
  - SPEED
  - SPKILL
  - STOD
  - SYSGEN
  - TPRINT
  - TUOFF
  - TUON
  - [TYPE](https://ja.wikipedia.org/wiki/TYPE_\(DOS_command\) "wikilink")
  - VFU
  - XFER

## 反トラスト訴訟

1970年代の後半、RDOSをデータゼネラルNovaやEclipseミニコンピュータに同梱する策略のために、データゼネラルは競合他社から (シャーマンおよびクレイトン独占禁止法の下で)\[7\]  訴えられた。\[8\] データゼネラルがNovaを発表したとき、デジダイン (Digidyne) 社は、自社のハードウェアクローンで RDOS [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")を使う事を望んだ。 データゼネラルは「バンドリング権」を主張し、[ソフトウェアのライセンスを拒否した](../Page/ソフトウェアライセンス.md "wikilink")。1985年、米国第9連邦巡回区控訴裁判所を含む裁判所は、デジダイン対データゼネラルと呼ばれる訴訟でデータゼネラルに対して判決を下した。 [合衆国最高裁判所](../Page/合衆国最高裁判所.md "wikilink")は、 [ホワイトとブラックマン連邦最高裁判事がそれを聞いたであろうが](https://ja.wikipedia.org/wiki/バイロン・ホワイト "wikilink")、データゼネラルの控訴を審理することを断った。ソフトウェアをデータゼネラルのハードウェアのみに制限することは違法な結束の取り決めであったため、下級裁判所の先例により、最終的にはデータゼネラルにオペレーティングシステムのライセンスを強制することになった。\[9\]

1999年、データゼネラルは[EMC Corporationによって買収された](../Page/Dell_EMC.md "wikilink")。\[10\]

## 参考文献

## 外部リンク

  - [コンピューター歴史博物館のRDOS資料](http://www.computerhistory.org/collections/accession/102685123)
  - [RDOS 7.50ユーザーパラメータ定義](http://www.telegraphics.com.au/svn/dpa/trunk/nova/rdos/paru.sr)
  - [SimuLogics 'ReNOVAte - DOS / WindowsNT / UN\*X / VMS上でNOVA/Eclipseソフトウェアを実行するためのエミュレータ](http://www.simulogics.com/)

[Category:リアルタイムオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:リアルタイムオペレーティングシステム "wikilink") [Category:未査読の翻訳があるページ](https://ja.wikipedia.org/wiki/Category:未査読の翻訳があるページ "wikilink") [Category:プロプライエタリOS](https://ja.wikipedia.org/wiki/Category:プロプライエタリOS "wikilink")

1.
2.
3.
4.
5.
6.  [RDOS/DOS Command Line Interpreter User's Manual](https://ja.wikipedia.org/wiki/iarchive:bitsavers_dgsoftwareCommandLineInterpreter_21045936/page/n5 "wikilink")
7.
8.
9.
10.