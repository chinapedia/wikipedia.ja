> この記事は[TOPS-20](https://ja.wikipedia.org/wiki/TOPS-20)から翻訳されています。


**TOPS-20**は[デジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")(DEC)によるDECの36ビット[メインフレーム](../Page/メインフレーム.md "wikilink")コンピューター用のプロプライエタリ\[1\]な[OSで](../Page/オペレーティングシステム.md "wikilink")、[PDP-10](../Page/PDP-10.md "wikilink")向けの[TOPS-10](../Page/TOPS-10.md "wikilink")の後継OSである。ハードウェアリファレンスマニュアルには「DECsystem-10 / DECSYSTEM-20 プロセッサ」と記載された（DEC [PDP-10とDECSYSTEM](https://ja.wikipedia.org/wiki/:en:PDP-10 "wikilink")-20を意味している)\[2\]。

TOPS-20の起源は、 [BBNテクノロジーズ](../Page/BBNテクノロジーズ.md "wikilink")(BBN)のTENEXオペレーティングシステム([1969年](https://ja.wikipedia.org/wiki/1969年 "wikilink"))であり、1976年にDECから販売された\[3\]。このシステムは名前の類似している[TOPS-10](../Page/TOPS-10.md "wikilink")とはほぼ全く関係がなかったが、PA1050というTOPS-10のモニターコールをエミュレーションする機能が同梱されており、一部を除いてTOPS-10用[実行ファイル](../Page/実行ファイル.md "wikilink")をほとんど修正なしで動作させることができた。DECの方針により、DECのアプリを実行するのに必要となった場合を除いて、TOPS-10のその後の修正をフォローするためにPA1050をアップデートすることはなかった。

TOPS-20はPDP-10で当時利用可能だったOSとして、TOPS-10、[ITS](../Page/Incompatible_Timesharing_System.md "wikilink")\[4\]、[WAITSなどの著名なタイムシェアリングシステムと競合関係にあった](https://ja.wikipedia.org/wiki/:en:WAITS "wikilink")。

## TENEX

TOPS-20は[BBNが](https://ja.wikipedia.org/wiki/Bolt,_Beranek_and_Newman "wikilink")[DECの](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[PDP-10](../Page/PDP-10.md "wikilink")用に開発した[TENEX](../Page/TENEX.md "wikilink")というOSをベースに開発された。TENEXはPDP-10で動作するサードパーティー製のOSとして当時最も人気があったが、DECが新たに開発した高速なKI-10版PDP-10では動作しなかった。この問題に対応するため、DECのPDP-10担当セールスマネージャはBBNからTENEXの権利を買い取り、新機種に移植するプロジェクトを立ち上げた。最終的には元のTENEXのコードはほとんど残らず、TOPS-20という名前で販売された。

## PA1050

このTOPS-20のおまけは[TOPS-10](../Page/TOPS-10.md "wikilink")のシステムコールをエミュレーションするエミュレーターに過ぎなかった。UUO (Unimplemented User Operation; 未実装ユーザー命令)と呼ばれる仕組みを利用し\[5\]、TOPS-20用ではないコンパイラを実行したり、こうした言語で書かれたユーザープログラムを実行したりするのに必要だった。ユーザーアドレス空間にマップされたパッケージの名称がPA1050だった。PAまたはPATは互換の意味で、10はDECやPDP-10を意味し、50はPDP-10モデル50、10/50、1050を意味していた\[6\]。

PA1050はPATと呼ばれることもあり、PA1050は特権を持たないユーザーモードのプログラムであり、JSYSコールを使って必要な時だけ動作することから、この名前は体をよく表していた\[7\]。

## TOPS-20の機能

TOPS-20は以下の機能によりその特徴を最大限に活用できる。

  - コマンドプロセッサEXEC.EXEを介してコマンドを入力する\[8\]
  - マクロ言語(.MAC)からJSYS(Jump to System)を呼び出す\[9\] \[10\]

EXECは主に以下の方法で機能を実現している。

  - JSYS経由の呼び出しを含むコード
  - GALAXYコンポーネント（スプーラなど）からのサービスの要求

### コマンドプロセッサー

TOPS-20は当時としては非常に先進的な機能があった。

  - コマンド補完 \[11\]
  - 次のような動的ヘルプ

:\* *ノイズワード* - DIRと入力してESCapeキーを押すと次のようになる。

  -

      -
        DIRectory (of files)

    <!-- end list -->

      -
        「I」と入力して<ESC>キーを押すと次のようになる。
          -

              -
                Information (about)

「？」を入力すると、許されるオペランドや必要なオペランドが補完される。

### コマンド

以下の[コマンド一覧はTOPS](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")-20のコマンドプロセッサによりサポートされる\[12\]。  <small>

  - ACCESS
  - ADVISE
  - [APPEND](https://ja.wikipedia.org/wiki/append "wikilink")
  - ARCHIVE
  - ASSIGN
  - ATTACH
  - BACKSPACE
  - BLANK
  - BREAK
  - BUILD
  - CANCEL
  - CLOSE
  - COMPILE
  - CONNECT
  - CONTINUE
  - [COPY](https://ja.wikipedia.org/wiki/copy_\(command\) "wikilink")
  - CREATE
  - CREF
  - CSAVE
  - DAYTIME
  - [DDT](https://ja.wikipedia.org/wiki/Dynamic_debugging_technique "wikilink")
  - DEASSIGN
  - [DEBUG](https://ja.wikipedia.org/wiki/debug_\(command\) "wikilink")
  - DEFINE
  - [DELETE](https://ja.wikipedia.org/wiki/del_\(command\) "wikilink")
  - DEPOSIT
  - DETACH
  - [DIRECTORY](https://ja.wikipedia.org/wiki/dir_\(command\) "wikilink")
  - DISABLE
  - DISCARD
  - DISMOUNT
  - EDIT
  - ENABLE
  - END-ACCESS
  - EOF
  - ERUN
  - EXAMINE
  - EXECUTE
  - EXPUNGE
  - FDIRECTORY
  - FORK
  - FREEZE
  - GET
  - [HELP](https://ja.wikipedia.org/wiki/help_\(command\) "wikilink")
  - INFORMATION
  - KEEP
  - LOAD
  - [LOGIN](https://ja.wikipedia.org/wiki/Login "wikilink")
  - LOGOUT
  - MERGE
  - MODIFY
  - [MOUNT](https://ja.wikipedia.org/wiki/Mount_\(computing\) "wikilink")
  - PERUSE
  - PLOT
  - POP
  - [PRINT](https://ja.wikipedia.org/wiki/print_\(command\) "wikilink")
  - PUNCH
  - PUSH
  - R
  - RECEIVE
  - REENTER
  - REFUSE
  - [REMARK](https://ja.wikipedia.org/wiki/Comment_\(computer_programming\) "wikilink")
  - [RENAME](https://ja.wikipedia.org/wiki/ren_\(command\) "wikilink")
  - RESET
  - RETRIEVE
  - REWIND
  - [RUN](https://ja.wikipedia.org/wiki/Run_command "wikilink")
  - SAVE
  - SEND
  - SET
  - SET HOST
  - SKIP
  - [START](https://ja.wikipedia.org/wiki/start_\(command\) "wikilink")
  - SUBMIT
  - SYSTAT
  - TAKE
  - TALK
  - TDIRECTORY
  - TERMINAL
  - TRANSLATE
  - [TYPE](https://ja.wikipedia.org/wiki/TYPE_\(DOS_command\) "wikilink")
  - UNATTACH
  - [UNDELETE](https://ja.wikipedia.org/wiki/Undeletion "wikilink")
  - UNKEEP
  - UNLOAD
  - VDIRECTORY

</small>

### JSYSの機能

JSYSは **J**ump to **SYS**temの略\[13\]。オペランドにはメモリアドレスの指定もあった。TOPS-20は18ビットまたは30ビットのアドレスを使用できた。モニタコールには1つないしは2つのオペランドが必要だった。一部のコールは両方の形式をサポートした。一部のモニタコールでは指定したアドレスのうちの18ビット以上が無視された。これらのコールは18ビットのアドレスが現在のセクションを参照しているものと解釈された\[14\]。

内部的には、まずGTJFN (Get Job File Number)というJSYSでファイルを識別し、次にOPENFでJFN番号を指定してファイルを開き、ファイルの内容を操作した。

## PCL（プログラム可能コマンド言語）

**PCL（Programmable Command Language）**はTOPS-20で動作するプログラミング言語。PCLのソースプログラムは、デフォルトでは.PCLというファイル形式で保存され、TOPS-20の拡張されたEXECでDECLAREという動詞名を使ってコンパイルでき、コンパイルしたコマンドはEXECの一部として機能した\[15\] \[16\] \[17\] \[18\]。

### PCL言語の機能

PCLには次のような機能があった： \[19\]

  - フロー制御：DO While / Until、CASE / SELECT、IF-THEN-ELSE、GOTO
  - 文字列操作 (length, substring, concatenation）
  - システム情報へのアクセス (日付/時刻、ファイル属性、デバイス特性)

## 今日のTOPS-20

[ポール・アレン](../Page/ポール・アレン.md "wikilink")は、TOPS-20が動作するXKL TOAD-2など、死去する前にいくつかの公にアクセス可能な歴史的なコンピューターシステムを維持していました。

## 参照

  - [タイムシェアリングシステムの進化](https://ja.wikipedia.org/wiki/:en:Time-sharing_system_evolution "wikilink")

## 参考文献

  - [デジタルコンピューティングタイムライン](http://www.vt100.net/timeline/1976.html)

## さらに読む

  - *[Storage Organization and Management in TENEX](http://tenex.opost.com/fjcc72/)* ダニエル・L・マーフィー。 AFIPS Proceedings 1972年 FJCC
  - *KI10でのTENEXの実装* ダニエル・L・マーフィー TENEXパネルセッション NCC 1974
  - *[Origins and Development of TOPS-20](http://tenex.opost.com/hbook.html)* ダニエル・L・マーフィー 1989年
  - [TOPS-20 User's Guide](http://tilt.twenex.org/) 1988.
  - [DECSYSTEM-20 Assembly Language Guide](ftp://kermit.columbia.edu/kermit/dec20/assembler-guide.txt) フランクダクルス、クリスライランド 1980年
  - [Running TOPS-20 V4.1 under the SIMH Emulator](http://gunkies.org/wiki/Running_TOPS-20_V4.1_under_SIMH)

## 外部リンク

  - [Origins and Development of TOPS-20](http://tenex.opost.com/hbook.html) 詳細な歴史
  - [1](http://panda.trailing-edge.com)[Panda TOPS-20 distribution](http://panda.trailing-edge.com/) 。
  - [2](http://www.twenex.org)[SDF Public Access TWENEX](http://www.twenex.org/) 。
  - [SIMHシミュレータ](http://simh.trailing-edge.com)PDP-10のシミュレーションとTOPS-20の実行が可能。
  - [Manuals for DEC 36-bit computers](http://www.36bit.org/dec/manual/) 。
  - [PDP-10ソフトウェアアーカイブ](http://pdp-10.trailing-edge.com) 。
  - [36-bits Forever](http://www.inwap.com/pdp10/) 。
  - [Request a login](https://livingcomputers.org/Computer-Collection/Online-Systems/Request-A-Login.aspx) to [Living Computers: Museum + Labs](https://ja.wikipedia.org/wiki/:en:Living_Computers:_Museum_+_Labs "wikilink") TOPS-20が動くTOAD-2

[Category:1969年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1969年のソフトウェア "wikilink")

1.
2.
3.
4.
5.  <http://www.abbreviations.com/term/223192>
6.  The 10/50 was the top-of-the-line KA machine at that time.  The family continued with another KA, the 10/55, and then came KI, KL & KS.
7.
8.
9.  The JSYS was the counterpart for the 20 of what was done by TOPS-10 on a "10" and thus the emulator for a DEC PDP-10 Model 50 was what PA1050 was emulating. The 10's system calls were known as UUO's
10. <ftp://kermit.columbia.edu/kermit/dec20/assembler-guide.txt>
11. <http://www.opost.com/dlm/tenex/hbook.html>
12.
13. <https://www.allacronyms.com/JSYS/Jump_to_System>
14.
15.
16.
17.
18.
19.