> この記事は[TOPS-10](https://ja.wikipedia.org/wiki/TOPS-10)から翻訳されています。


**TOPS-10**は1967年に[ディジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") (DEC) が[メインフレーム](../Page/メインフレーム.md "wikilink")の[PDP-10](../Page/PDP-10.md "wikilink")シリーズ向けにリリースした歴史上の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")(OS)。TOPS-10を搭載したPDP-10システムは "DECsystem-10"と呼ばれた。"TOPS" は *Timesharing / Total OPerating System* の略。元々は[PDP-6](../Page/PDP-6.md "wikilink")およびPDP-10の初期のOSだった "Monitor" が発展したもので、1970年にTOPS-10へ改名された。

## 概要

TOPS-10は[共有メモリ](../Page/共有メモリ.md "wikilink")をサポートしており、世界で初めて真のマルチプレイヤーを実現した[ゲームの](../Page/コンピュータゲーム.md "wikilink")1つが開発された。\[1\]はテキストベースの[スタートレック](../Page/スタートレック.md "wikilink")のようなゲームで、ユーザーは端末からコマンドを打ち込み、リアルタイムで対戦できた。またTOPS-10は今日では[MMORPG](../Page/MMORPG.md "wikilink")と呼ばれるオンラインロールプレイングゲームの先駆けであるMulti User Dungeon(MUD)のオリジナルを運用するのに用いられた。

他の特筆すべきアプリケーションとして FORUM がある。現在では[チャット](../Page/チャット.md "wikilink")と言われるユーザー同士の会話ができるアプリケーションであり、いわゆる「CBシミュレータ」の先駆けでだった。このアプリケーションは複数のユーザーによる対話の可能性を示したもので、[CompuServe](../Page/CompuServe.md "wikilink")のチャットが開発される要因のひとつとなった。

TOPS-10の[APIは非常に頑強であり](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、UUO（Unimplemented User Operation; 未実装ユーザー命令）を利用した機構を使っている。UUOにより[システムコール](../Page/システムコール.md "wikilink")は[機械語](../Page/機械語.md "wikilink")の命令の1つであるように実装された。このAPIはモニターコールと呼ばれ、当時としてはほとんどのOSより大きく進んでおり、DECsystem-10のシステムプログラミングを単純かつ強力なものにした。

TOPS-10はプライオリティが付いた複数のキューで構成される[スケジューラを備えており](../Page/スケジューリング.md "wikilink")、[多段フィードバックキュー](../Page/多段フィードバックキュー.md "wikilink")の原始的なもので、プライオリティに基づいて[プロセス](../Page/プロセス.md "wikilink")をキューに挿入できた。またこのOSではユーザーファイルとデバイスが独立していた。

### コマンド

下記のリストはTOPS-10がサポートしている[コマンドの一覧である](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")\[2\]。

  - ASSIGN
  - ATTACH
  - BACKSPACE
  - BACKUP
  - CCONTINUE
  - COMPILE
  - CONTINUE
  - [COPY](https://ja.wikipedia.org/wiki/copy_\(command\) "wikilink")
  - CORE
  - CPUNCH
  - CREATE
  - CREDIR
  - CREF
  - CSTART
  - D(eposit)
  - DAYTIME
  - DCORE
  - [DDT](https://ja.wikipedia.org/wiki/Dynamic_debugging_technique "wikilink")
  - DEASSIGN
  - [DEBUG](https://ja.wikipedia.org/wiki/debug_\(command\) "wikilink")
  - [DELETE](https://ja.wikipedia.org/wiki/del_\(command\) "wikilink")
  - DETACH
  - [DIRECTORY](https://ja.wikipedia.org/wiki/dir_\(command\) "wikilink")
  - DISABLE
  - DISMOUNT
  - DSK
  - DUMP
  - E(xamine)
  - EDIT
  - ENABLE
  - EOF
  - EXECUTE
  - FILCOM
  - FILE
  - FINISH
  - FUDGE
  - GET
  - GLOB
  - HALT
  - [HELP](https://ja.wikipedia.org/wiki/help_\(command\) "wikilink")
  - INITIA
  - JCONTINUE
  - KJOB
  - LABEL
  - LIST
  - LOAD
  - LOCATE
  - LOGIN
  - MAKE
  - MERGE
  - MIC
  - [MOUNT](https://ja.wikipedia.org/wiki/Mount_\(computing\) "wikilink")
  - NETWORK
  - NODE
  - NSAVE
  - NSSAVE
  - OPSER
  - PJOB
  - PLEASE
  - PLOT
  - PRESERVE
  - [PRINT](https://ja.wikipedia.org/wiki/print_\(command\) "wikilink")
  - PROTECT
  - PUNCH
  - QUEUE
  - QUOLST
  - R
  - REASSIGN
  - REATTACH
  - REENTER
  - RENAME
  - RESOURCES
  - REWIND
  - [RUN](https://ja.wikipedia.org/wiki/Run_command "wikilink")
  - SAVE
  - SSAVE
  - SCHED
  - SEND
  - SET
  - SKIP
  - [START](https://ja.wikipedia.org/wiki/start_\(command\) "wikilink")
  - SUBMIT
  - SYSTAT
  - [TECO](https://ja.wikipedia.org/wiki/TECO_\(text_editor\) "wikilink")
  - TIME
  - TPUNCH
  - [TYPE](https://ja.wikipedia.org/wiki/TYPE_\(DOS_command\) "wikilink")
  - UNLOAD
  - USESTAT
  - VERSION
  - WHERE
  - ZERO

## 歴史

### リリース履歴

PDP-6のMonitorは1964年にリリースされた。1967年のリリース2.18でPDP-10のKA10プロセッサをサポートした。1970年のリリース5.01からTOPS-10に改称された。リリース6.01（1974年5月）で初めて[仮想記憶](../Page/仮想記憶.md "wikilink")（[デマンドページング](../Page/ページング方式.md "wikilink")）を実装し、物理メモリ容量より大きなプログラムを実行できるようになった。リリース7.00から[対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink")が可能となった（それまでは[マスタースレーブ](https://ja.wikipedia.org/wiki/マスタースレーブ "wikilink")方式が使われていた）。最終版は1988年のリリース7.04である\[3\]。

### 今日のTOPS-10

1996年、DECはTOPS-10を愛好家が使用することを許諾するホビースト向けライセンスを発行した\[4\]。

今日TOPS-10を動作させる最も簡単な方法は、適当な[エミュレータ](../Page/エミュレータ.md "wikilink")\[5\]\[6\]とOSの[システムイメージ](../Page/システムイメージ.md "wikilink")\[7\]を利用する方法である。また、元もとの配布用磁気テープの内容がアーカイブされており、そこから構築することも可能である\[8\] \[9\]。

[ポール・アレン](../Page/ポール・アレン.md "wikilink")は歴史的コンピュータシステムを保守し公開しているが、その中にTOPS-10が動作する DECsystem-1090 も含まれる\[10\]。

## ソフトウェア

### 実装されたプログラミング言語

TOPS-10の[アセンブラ](../Page/アセンブリ言語.md "wikilink")がTOPS-10に同梱されていた。

以下の[プログラミング言語](../Page/プログラミング言語.md "wikilink")製品がTOPS-10上で動作した。

  - [ALGOL](../Page/ALGOL.md "wikilink") (ALGOL-10 v10B)\[11\] - 汎用コンパイラ
  - [APL](../Page/APL.md "wikilink") (APL-SF V2)\[12\] - 数学的モデリング用インタプリタ
  - [BASIC](../Page/BASIC.md "wikilink") (BASIC-10 v17F)\[13\] - 汎用インタプリタ
  - [BLISS](../Page/BLISS.md "wikilink") (BLISS-10\[14\], BLISS-36\[15\]) - システムプログラミング用コンパイラ
  - [COBOL](../Page/COBOL.md "wikilink") (COBOL-68\[16\], COBOL-74\[17\]) - 事務処理用コンパイラ
  - [FORTRAN](../Page/FORTRAN.md "wikilink") (FORTRAN-10 v11\[18\]) - 科学技術計算用コンパイラ

以下のプログラミング言語もTOPS-10上で実装されているが、DEC純正ではなくユーザーグループ  の会員が提供したものである。

  - [FOCAL](https://ja.wikipedia.org/wiki/:en:FOCAL_\(programming_language\) "wikilink") (FOCAL-10)

  - [Forth](../Page/Forth.md "wikilink") - [スレッデッドコード](https://ja.wikipedia.org/wiki/スレッデッドコード "wikilink")方式の言語

  - [IMP72](https://ja.wikipedia.org/wiki/:en:IMP_programming_language "wikilink")

  - [LISP](https://ja.wikipedia.org/wiki/LISP "wikilink") - [AIプログラミング向けインタプリタ](../Page/人工知能.md "wikilink")

  - [Pascal](../Page/Pascal.md "wikilink") - コンピュータ教育向けコンパイラ

  - \- [CAI向け言語](../Page/コンピュータ支援教育.md "wikilink")

  - [SAM76](https://ja.wikipedia.org/wiki/:en:SAM76 "wikilink")

  - [Simula](../Page/Simula.md "wikilink") - モデリング用コンパイラ

  - [SNOBOL](../Page/SNOBOL.md "wikilink") - 文字列処理用インタプリタ

  - [BCPL](../Page/BCPL.md "wikilink") - エセックス大学が実装したコンパイラ

### 実装されたユーティリティ

以下のリストはTOPS-10で実装された主なユーティリティソフトである。

  - [RMS](https://ja.wikipedia.org/wiki/Record_Management_Services "wikilink") - レコードマネジメントサービス
  - [IQL](https://ja.wikipedia.org/wiki/:en:IQL "wikilink") - 対話型クエリ言語
  - [DBMS-10](https://ja.wikipedia.org/wiki/:en:DBMS-10 "wikilink") - [CODASYL](../Page/CODASYL.md "wikilink") [データベース](../Page/データベース.md "wikilink")

### TOPS-10で実装された主なゲーム

  - [コロッサル・ケーブ・アドベンチャー](https://ja.wikipedia.org/wiki/コロッサル・ケーブ・アドベンチャー "wikilink") (ADVENT)
  - [DECWAR](https://ja.wikipedia.org/wiki/:en:DECWAR "wikilink") - 前述
  - [FORUM](https://ja.wikipedia.org/wiki/:en:FORUM "wikilink") - 前述
  - [HAUNT](https://ja.wikipedia.org/wiki/:en:HAUNT "wikilink") - 初期のロールプレイングゲーム
  - [マックハック](https://ja.wikipedia.org/wiki/マックハック "wikilink") - [リチャード・グリーンブラット](https://ja.wikipedia.org/wiki/リチャード・グリーンブラット "wikilink")が開発した[コンピュータチェス](../Page/コンピュータチェス.md "wikilink")
  - [MUD](https://ja.wikipedia.org/wiki/:en:MUD1 "wikilink") - 前述

## 影響

[MS-DOS](../Page/MS-DOS.md "wikilink")はTOPS-10から大きな影響を受けている。3文字のファイル[拡張子](../Page/拡張子.md "wikilink")、EXEやTXTといった主な拡張子名、アスタリスク(\*)を用いた[ワイルドカード](../Page/ワイルドカード_\(情報処理\).md "wikilink")、コマンドのスイッチにスラッシュ(/)を用いるなど、数多くの共通点がみられる\[19\]。

## 脚注

## 関連項目

  - [TOPS-20](../Page/TOPS-20.md "wikilink")
  - [コロッサル・ケーブ・アドベンチャー](https://ja.wikipedia.org/wiki/コロッサル・ケーブ・アドベンチャー "wikilink")

[Category:オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:オペレーティングシステム "wikilink") [Category:ディジタル・イクイップメント・コーポレーション](https://ja.wikipedia.org/wiki/Category:ディジタル・イクイップメント・コーポレーション "wikilink") [Category:1967年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1967年のソフトウェア "wikilink")

1.  [The Decwar Page](http://hsnewman.freeshell.org/decwar.htm)
2.
3.
4.  [Home hobbyist license for Digital's 36b software](http://www.inwap.com/pdp10/96license.txt)
5.  [The Computer History Simulation Project](http://simh.trailing-edge.com/)
6.  [KLH10 PDP-10 Emulator](http://klh10.trailing-edge.com/)
7.  [TOPS-10 pre-built image](http://www.steubentech.com/~talon/pdp10/)
8.  [PDP-10 software archive](http://pdp-10.trailing-edge.com/)
9.  [Notes on DEC PDP-10 Emulation](http://www.asun.net/pdp10/)
10. [Living Computer Museum](http://www.pdpplanet.com/)
11. [DECsystem10/20 ALGOL Programmer's Guide, April 1977](http://computer-refuge.org/bitsavers/pdf/dec/pdp10/TOPS10_softwareNotebooks/vol06/AA-0196C-TK_ALGOL_Programmers_Guide_Apr77.pdf)
12. [APL-SF Language Manual, August 1979](http://computer-refuge.org/bitsavers/pdf/dec/pdp10/TOPS10_softwareNotebooks/vol06/AA-H200A-TK_APLSF_Language_Manual_Aug79.pdf)
13. [DECsystem-10 BASIC Conversational Language Manual, March 1974](http://computer-refuge.org/bitsavers/pdf/dec/pdp10/TOPS10_softwareNotebooks/vol06/DEC-10-LBLMA-A-D_BASIC_Conversational_Language_Manual_Mar74.pdf)
14.
15.
16.
17.
18.
19.