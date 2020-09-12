> この記事は[データゼネラルAOS](https://ja.wikipedia.org/wiki/データゼネラルAOS)から翻訳されています。


**Data General AOS** (**Advanced Operating System**の略称\[1\])は、[データゼネラル](../Page/データゼネラル.md "wikilink")社の [16ビット](../Page/16ビット.md "wikilink") [Eclipse](../Page/Eclipse_\(コンピュータ\).md "wikilink") C、M、S [ミニコンピュータ](../Page/ミニコンピュータ.md "wikilink")用のオペレーティングシステムのファミリーの名前であり、その後に [AOS/VS](https://ja.wikipedia.org/wiki/:en:AOS/VS "wikilink")、[AOS/RT32](https://ja.wikipedia.org/wiki/:en:AOS/RT32 "wikilink") \[2\](1980年)、および32ビット [Eclipse MV](https://ja.wikipedia.org/wiki/Eclipse_MV "wikilink") ライン用の [AOS/VS II](https://ja.wikipedia.org/wiki/データゼネラルAOS/VS_II "wikilink") (1988年) と続いた。

## 概観

AOS/VS は [Eclipse MV](https://ja.wikipedia.org/wiki/Eclipse_MV "wikilink") ハードウェアの 8 つの[リング保護アーキテクチャを利用しており](../Page/リングプロテクション.md "wikilink")、リング 7 は最も特権が少なく、リング 0 は最も特権が多い。AOS/VS カーネルはリング 0 で実行され、仮想アドレス変換に関連するデータ構造のためにリング 1 アドレスを使用していた。リング２は未使用で、カーネルが将来使用するために予約されていた。AOS/VS カーネルのシステムコール検証の多くを実行したエージェントや、一部の I/O バッファリング、および多くの互換性機能は、各プロセスのリング 3 で実行された。リング 4 は [INFOS II](https://ja.wikipedia.org/wiki/:en:INFOS_II "wikilink") [DBMS](https://ja.wikipedia.org/wiki/DBMS "wikilink") のような様々な DG 製品によって使用された。リング 5 と 6 はユーザプログラム用に予約されていたが、MV/UX インナーリングエミュレータや [Oracle](../Page/Oracle_Database.md "wikilink") などの大規模なソフトウェアがリング 5 を使用する以外はほとんど使用されなかった。すべてのユーザプログラムはリング 7 で実行された。

AOS ソフトウェアは、競合する [PDP-11](../Page/PDP-11.md "wikilink") オペレーティングシステムよりもはるかに高度なものであった。16ビットの AOS アプリケーションは、32ビットの Eclipse MV ライン上の AOS/VS と AOS/VS II の下でネイティブに実行された。AOS/VS (Advanced Operating System/Virtual Storage) は、最も一般的に使用されている DG ソフトウェア製品であり、複雑なスクリプト、DUMP/LOAD、およびその他のカスタムコンポーネントを可能にする[コマンドラインインタプリタ](../Page/コマンドラインインタプリタ.md "wikilink") (CLI) が含まれていた。

CLI の16ビット版は、*[Colossal Cave Adventure](https://ja.wikipedia.org/wiki/コロッサル・ケーブ・アドベンチャー "wikilink")* ゲームから直接取得した[イースター・エッグが含まれていることで有名である](../Page/イースター・エッグ_\(コンピュータ\).md "wikilink")。ユーザーが[コマンド](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")「[xyzzy](https://ja.wikipedia.org/wiki/:en:Xyzzy "wikilink")」を入力すると、CLI から「Nothing Happens」というレスポンスが返される。[32ビット](../Page/32ビット.md "wikilink")版の CLI が [AOS/VS II](https://ja.wikipedia.org/wiki/AOS/VS_II "wikilink") で利用できるようになると、同じコマンドは「Twice As Much Happens」を報告した。

AOS/VS の下でホストされた MV/UX と呼ばれる System V.2 [Unix](../Page/UNIX.md "wikilink") の修正版も利用可能であった。[DG/UX](https://ja.wikipedia.org/wiki/DG/UX "wikilink") と呼ばれる [System V](https://ja.wikipedia.org/wiki/System_V "wikilink") Unix の修正版が Eclipse MV ラインと後の [88K](../Page/MC88000.md "wikilink") と [x86](https://ja.wikipedia.org/wiki/x86 "wikilink") [AViiON](../Page/データゼネラルAviion.md "wikilink") マシン用に作られた。

AOS と AOS/VS カーネルはすべて[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で記述されていた。オペレーティングシステムのリリースに含まれるほとんどすべての AOS と AOS/VS ユーティリティは、[PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink") プログラミング言語の変種で書かれていた。当初は、AOS/VS ユーティリティは AOS のソース開発に密接に追従していた。AOS/VS が成熟するにつれ、DG が提供する多くのユーティリティは、32ビットアドレス空間を利用してアセンブリ言語への依存度を減らすために書き換えられ、その結果、AOS の祖先と比較してしばしば機能性、性能、信頼性が大幅に向上した。

## セッション

    **** Atari S/W Development HCD1 / BATCH OUTPUT FILE ****

    AOS/VS  3.07 / EXEC  3.07   19-JAN-84   10:11:01
    QPRI=254    SEQ=31324
    INPUT FILE -- :UDD:SYSTEMS:850:?031.CLI.004.JOB (WILL BE DELETED AFTER PROCESSING)
    LIST FILE  -- :QUEUE:NORDIN.LIST.31324

    --------
    LAST MESSAGE CHANGE 12-JAN-84   16:06:08

            Atari S/W Development System HCD1

    Backup schedule (system shut down): Saturday  21-Jan-84  9:30-11:30am

    Refer to HELP *COMMANDS, HELP *PSEUDO, HELP, APHELP, and ?MHELP.

    Refer to DISP FUNC in SED for list of default function key commands.

    --------
    LAST PREVIOUS LOGON 19-JAN-84   10:09:45
    * searchlist :UDD:NORDIN:UTIL :UDD:NORDIN:LINKS :C :UTIL :

    AOS/VS CLI   REV 03.03.00.00    19-JAN-84   10:11:05
    Ý SEARCHLIST :UDD:SYSTEMS:UTIL,:UDD:NORDIN:UTIL,:UDD:NORDIN:LINKS,:C,:UTIL,:
    Ý DIRECTORY :UDD:SYSTEMS:850
    Ý DEFACL SYSTEMS,OWARE,A.JOE,OWARE,A.OLIVIA,OWARE,ARKEN,OWARE,BLOTCKY,OWARE,NORDIN,OWARE,TITTSLER,OWARE,FOWKES,OWARE
    Ý CAMAC R850AMAC H=R850AMAC.OBJ L=R850AMAC.PRN R=F SL=132


    ATARI CAMAC Assembler Ver  1.0A
    Copyright 1981 ATARI Inc.

    Enter source file name and options

    d:R850AMAC  h=d:R850AMAC.OBJ l=d:R850AMAC.PRN R=F SL=132

      Pass 1 - Reading D1:R850AMAC.
      Pass 2 - Reading D1:R850AMAC.

      no ERRORs,  669 Labels, $67E8 free.
    �

    ATARI CAMAC Assembler Ver  1.0A
    Copyright 1981 ATARI Inc.

    Enter source file name and options



    Ý
    Ý
    END OF FILE
    AOS/VS CLI   TERMINATING    19-JAN-84   10:12:06

    PROCESS 42 TERMINATED
    ELAPSED TIME  0:01:06
    (OTHER JOBS, SAME USERNAME)
    USER 'NORDIN' LOGGED OFF    19-JAN-84   10:12:07


    ****
    * LIST FILE EMPTY, WILL NOT BE PRINTED
    ****

## 関連項目

  - [データゼネラルRDOS](../Page/データゼネラルRDOS.md "wikilink")
  - CEO (Data General)

## 参考文献

[Category:プロプライエタリOS](https://ja.wikipedia.org/wiki/Category:プロプライエタリOS "wikilink")

1.  <https://archive.org/details/bitsavers_dgsoftwarebraryFileEditorUMApr77raw_1324483>
2.