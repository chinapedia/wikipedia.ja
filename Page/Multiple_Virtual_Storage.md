> この記事は[Multiple Virtual Storage](https://ja.wikipedia.org/wiki/Multiple_Virtual_Storage)から翻訳されています。


**MVS** （えむぶいえす、、**多重仮想記憶**）は、[1974年](../Page/1974年.md "wikilink")に発表された[IBM](../Page/IBM.md "wikilink")の[メインフレーム](../Page/メインフレーム.md "wikilink")用[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の1つ。前身は[OS/360](https://ja.wikipedia.org/wiki/OS/360 "wikilink")のMVTやOS/VS。当初の名称は「OS/VS2 R2」であったが、後に「OS/VS2 MVS」、更に「MVS」と呼ばれた。後継は[OS/390](https://ja.wikipedia.org/wiki/OS/390 "wikilink")と[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")である。

## 概要

MVS は、[System/360](https://ja.wikipedia.org/wiki/System/360 "wikilink") 用のオペレーティングシステム [OS/360](https://ja.wikipedia.org/wiki/OS/360 "wikilink") のバリエーションのひとつで[1964年](../Page/1964年.md "wikilink")に発表された MVT(Multiprogramming with a Variable number of Tasks)の後継の SVS (Single Virtual Storage)の後継として誕生した。

MVT は、[OS/360](https://ja.wikipedia.org/wiki/OS/360 "wikilink") の最初の バリエーションである PCP (Primary Control Program) に[マルチタスク](../Page/マルチタスク.md "wikilink")機能を加えたものである。SVS はこれに、1つの[アドレス空間](../Page/アドレス空間.md "wikilink")を複数の[タスク](https://ja.wikipedia.org/wiki/タスク "wikilink")で共有する[仮想記憶](../Page/仮想記憶.md "wikilink")（virtual storage、IBM[汎用コンピュータ](https://ja.wikipedia.org/wiki/汎用コンピュータ "wikilink")以外の表現ではvirtual memory）機能を追加したものである。MVS ではさらに、異なるタスクは異なるアドレス空間で動くことを許容する仮想記憶機能を持つことになった。

MVS はもともと、[24ビット](https://ja.wikipedia.org/wiki/24ビット "wikilink")システムをサポートした。[ハードウェア](../Page/ハードウェア.md "wikilink")の進歩に従って、XAとESAでは31ビットシステムを、z/OSでは[64ビット](../Page/64ビット.md "wikilink")システムをサポートする。

オペレーティングシステム MVS の[インターフェースは主に](../Page/インタフェース_\(情報技術\).md "wikilink")、[バッチ処理](../Page/バッチ処理.md "wikilink")のインターフェースである [JCL](../Page/Job_Control_Language.md "wikilink") (Job Control Language)と、対話式のコマンド・ライン・インタープリタで[タイムシェアリングシステム](../Page/タイムシェアリングシステム.md "wikilink")である [TSO](https://ja.wikipedia.org/wiki/Time_Sharing_Option "wikilink") (Time Sharing Option)である。TSO は最初はオプションであったが、現在では標準の機能として装備されている。[ISPF](https://ja.wikipedia.org/wiki/ISPF "wikilink") (Interactive System Productivity Facility)は、ユーザーに TSO 機能を提供する、しかしメニューのある、形式志向の態様を持つインターフェースである。

MVSシステムは伝統的に、[IBM 3270](../Page/IBM_3270.md "wikilink")[端末](../Page/端末.md "wikilink")（※[ダム端末](../Page/ダム端末.md "wikilink")も参照）または、[PCで動く](../Page/パーソナルコンピュータ.md "wikilink") 3270[端末エミュレータ](../Page/端末エミュレータ.md "wikilink") によりアクセスされる。しかしながら、今日では、メインフレームで動く多くのアプリケーションは[World Wide Webや](../Page/World_Wide_Web.md "wikilink")[GUIをインターフェースに持つ](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink")。z/OSは、[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")をビルトインでサポートする。システムのマネジメントは、かつては3270端末を通して行われたが、今日では、ハードウェア・マネジメント・コンソール(HMC)や、さらにウェブ/[インターネット](../Page/インターネット.md "wikilink")で使用されるインターフェースを介して行われることも増えている。オペレーター・コンソールは 2074エミュレータ で提供（供給）されるので、3270接続を介して OS/390 や z/OS のプロセッサにアクセスすることはありそうにない。z/OS はまた、[POSIX](../Page/POSIX.md "wikilink")アプリケーションの実行をネイティブ・サポートする。

1つの MVS は1つの物理システムを占有する。その論理的な単位を1つの「論理区画」(Logical Partition, LPAR)という。z/VM 下では、それを1つのヴァーチャル・マシン(a virtual machine)と呼んだ。複数の MVS が組織化・編成され、「Systems Complex」(Sysplex)と呼ぶ1つの構造体に共同で管理されることが可能になったのは、[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")9月のことである。複数の LPAR 間のオペレートは、「Cross-system Coupling Facility」または「XCF」と呼ばれるソフトウェア・コンポーネントと、「Hardware Coupling Facility」または「CF」あるいは「ICF」と呼ばれるハードウェア・コンポーネントを通して行われる。複数のSysplexは、TCP/IP や IBM の製品である「[Systems Network Architecture](../Page/Systems_Network_Architecture.md "wikilink")」(SNA)といった標準的な[ネットワーク](../Page/コンピュータネットワーク.md "wikilink")[プロトコル](../Page/プロトコル.md "wikilink")によって結びつけることが出来る。複数のLPAR は、Linux on IBM System z、z/VSE、[z/TPF](https://ja.wikipedia.org/wiki/z/TPF "wikilink")、z/VM といった異なるオペレーティングシステムで稼動させることができる。

MVS は主に[ビジネス](../Page/ビジネス.md "wikilink")や[銀行](../Page/銀行.md "wikilink")の[システムに使われ](../Page/コンピュータシステム.md "wikilink")、MVS 上で動く業務[アプリケーション・プログラムは主に](../Page/アプリケーションソフトウェア.md "wikilink")[コボル(COBOL)で記述される](../Page/COBOL.md "wikilink")。COBOLのプログラムは、伝統的に、[IMS](../Page/IMS.md "wikilink") (Information Management System) や [CICS](../Page/CICS.md "wikilink") (Customer Information Control System) のような[トランザクション](../Page/トランザクション.md "wikilink")処理システムで使われる。CICS で動くプログラムには、COBOL プログラムの[ソースコード](../Page/ソースコード.md "wikilink")に特別な EXEC CICS ステートメントが挿入される。プリプロセッサは、プログラムのコンパイルの前に、これらの EXEC CICS ステートメントを、CICS をコールする COBOL のコードに変換する。[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")をコールする [SQL](../Page/SQL.md "wikilink") の場合と似ている。業務アプリケーションはもちろん、[C言語](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")、[FORTRAN](../Page/FORTRAN.md "wikilink")、[BASIC](../Page/BASIC.md "wikilink")、[RPG](../Page/RPG_\(プログラム言語\).md "wikilink")、[REXX](../Page/REXX.md "wikilink")など他の[プログラミング言語](../Page/プログラミング言語.md "wikilink")で書くことも出来る。これらの言語のサポートは「Language Environment」「LE」と呼ばれる共通コンポーネントにパッケージされていて、[デバッグ](../Page/デバッグ.md "wikilink")、トレース、プロファイリングや、その他の各言語独自の機能を提供する。

## MVSファイルシステム

[ファイルは](../Page/ファイル_\(コンピュータ\).md "wikilink")、MVS では「[データ・セット](../Page/データセット_\(IBMメインフレーム\).md "wikilink")」と呼ばれる。これらのファイルは「カタログ」によって組織・系統が立てられる。MVS の本来の[文字コード](../Page/文字コード.md "wikilink")はビッグ・[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink") [EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink")だが、[ASCII](../Page/ASCII.md "wikilink")やリトル・エンディアン、[Unicode](../Page/Unicode.md "wikilink")のトランスフォームのソフトウェアサポートのためのhardware-specific serviceを持つ。

MVS の[伝統](../Page/伝統.md "wikilink")的な[ファイルシステム](../Page/ファイルシステム.md "wikilink")は、[レコード・オリエンテッド・ファイルシステム](../Page/Record-oriented_filesystem.md "wikilink")（レコード志向ファイルシステム）である。ファイル名は階層的に組織・編成され、ドットによって分けられる。それぞれの階層の名前は、8文字まで認められる。ファイル名の全体の長さは、44文字までである。

大体、ドットによって分けられた[コンポーネント](https://ja.wikipedia.org/wiki/コンポーネント "wikilink")は、他のオペレーティングシステムの[ディレクトリ](../Page/ディレクトリ.md "wikilink")のように使われる。たとえば、最上階のコンポーネントは、通常プロジェクト名やサブシステム名や機能名やユーザーの[名前](../Page/名前.md "wikilink")を表現する。しかしながら、これは他のシステムのものとは違って、本当のディレクトリではない。ネーミング上の慣例にすぎない。

区分[データセットは](../Page/データセット_\(IBMメインフレーム\).md "wikilink")、ある意味で1階層のディレクトリに似ている。MVS は幅広いファイルアクセス方式をサポートする。これは主として、レガシーニーズ（これまでに蓄えた多くのソフトウェア資産を無視できない）によるものである。これらにはVSAM、BSAM、QSAM、その他が含まれる。MVS のファイルシステムは、IBM が何年にも渡って使用し続けた [ディスクストラクチャ](../Page/ディスクメディア.md "wikilink") [VTOC](https://ja.wikipedia.org/wiki/VTOC "wikilink") (Volume Table Of Contents) に基づいている。

MVS の2006年現在のバージョンである i.e. z/OS は、POSIXコンパチブルである「slash」ファイルシステムをサポートする。これは2つのファイルシステムの長所を一緒に統合するものである。すなわち、POSIX は MVS のデータセットを POSIX 下で稼動するプログラムで取り扱うことができ、POSIX 下で稼動するサブシステムで使用することができる、というものである。このような新しいファイルシステムとしては、「[Hierarchical File System](../Page/Hierarchical_File_System.md "wikilink")」(HFS)、「zFS」（[SunのZFSとは違うもの](../Page/サン・マイクロシステムズ.md "wikilink")）がある。

  -
    *→ [データセット (IBMメインフレーム)](../Page/データセット_\(IBMメインフレーム\).md "wikilink") および [ファイル編成法](../Page/ファイル編成法.md "wikilink") も参照*

## 歴史

MVS が最初に発表されたのは[1974年](../Page/1974年.md "wikilink")。改訂されて次に出された同オペレーティングシステムの名前は **MVS/XA** (eXtended Architecture)、次が **MVS/ESA** (Enterprise Systems Architecture)、UNIX System Services (USS)機能が追加された次の版は**[OS/390](https://ja.wikipedia.org/wiki/OS/390 "wikilink")**、64ビットシステムをサポートすることになった[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")（zSeries、System z）と続く。このオペレーティングシステムの中核（コア）の部分は、根本的にはシリーズを通して変わっていない。設計上、MVSのために書かれた[プログラムはz](../Page/プログラム_\(コンピュータ\).md "wikilink")/OSにいたるまで、モディファイを受けずに動いている。

MVS は[2006年](../Page/2006年.md "wikilink")現在ではサポートが終了している。IBM は、31ビットコンバチブルの z/OS のサポートも[2007年](../Page/2007年.md "wikilink")までに終了することを公表しており、以後は、64ビットの z/OS のみ公式なサポートが受けられることになる。MVS はこれからも、エンタープライズオペレーティングシステムのフラッグシップとして、最先端の改良を受け、その先端性を拡張し続ける。その機能強化は上記で述べられているものに加えて、下記のものを含む。

  - XML (Xerces-based toolkits for C/C++ and Java)
  - network file systems
      - NFS Version 4
      - Common Internet Filing System(CIFS)/SMB
  - Transport Layer Security(TLS/SSL)support throughout (TCP/IP stack levelを含む)
  - removal of previous architectural limits
  - encrypting file systems
  - Workload Manager (WLM)
  - special Java acceleration (zAAP support)
  - Hipersockets

z/OS の下では古い24ビットの MVS アプリケーションが稼動し続けている一方、たとえば、64ビットのハードウェアで動く Java プログラム、フレキシブルなマウントと長いファイル名をサポートする堅牢なファイルシステム上の Unicode XML [フォーマットの](../Page/ファイルフォーマット.md "wikilink")[データ](../Page/データ.md "wikilink")が今まさに書き続けられ、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink") と速い CFs で、最新のパフォーマンス拡張SQLを使用した地理学的にひしめいた関係[データベースと](https://ja.wikipedia.org/wiki/関係データベース "wikilink")[コミュニケーション](../Page/コミュニケーション.md "wikilink")をとり続けている。

## 関連項目

  - [コンピュータシステム](../Page/コンピュータシステム.md "wikilink")
      - [情報処理システム](../Page/情報処理システム.md "wikilink")
      - [情報システム](../Page/情報システム.md "wikilink")
      - [IBM](../Page/IBM.md "wikilink")
      - [メインフレーム](../Page/メインフレーム.md "wikilink")
  - マシン
      - [System/360](https://ja.wikipedia.org/wiki/System/360 "wikilink")
      - [System/370](https://ja.wikipedia.org/wiki/System/370 "wikilink")
      - [System z](../Page/System_z.md "wikilink")
  - [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS)
      - [OS/360](https://ja.wikipedia.org/wiki/OS/360 "wikilink")
      - [OS/390](https://ja.wikipedia.org/wiki/OS/390 "wikilink")
      - [z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")
  - [ツール](https://ja.wikipedia.org/wiki/ツールソフトウェア "wikilink")/ユーティリティ/[ミドルウェア](../Page/ミドルウェア.md "wikilink")/[ネットワーク](../Page/コンピュータネットワーク.md "wikilink")/その他
      - [JCL](../Page/Job_Control_Language.md "wikilink")
      - [IBM メインフレーム ユーティリティプログラム](../Page/IBM_メインフレーム_ユーティリティプログラム.md "wikilink")
      - [JES](https://ja.wikipedia.org/wiki/Job_Entry_Subsystem_2/3 "wikilink")
      - [データセット (IBMメインフレーム)](../Page/データセット_\(IBMメインフレーム\).md "wikilink")
      - [IMS](../Page/IMS.md "wikilink")
      - [DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")
      - [CICS](../Page/CICS.md "wikilink")
      - [Systems Network Architecture](../Page/Systems_Network_Architecture.md "wikilink") (SNA)
      - [VTAM](https://ja.wikipedia.org/wiki/VTAM "wikilink")
      - [ダム端末](../Page/ダム端末.md "wikilink")
      - [IBM 3270](../Page/IBM_3270.md "wikilink") (3270端末)
      - [端末エミュレータ](../Page/端末エミュレータ.md "wikilink")
      - [Time Sharing Option](https://ja.wikipedia.org/wiki/Time_Sharing_Option "wikilink") (TSO)
      - [ISPF](https://ja.wikipedia.org/wiki/ISPF "wikilink")
      - [コマンドラインインタプリタ](../Page/コマンドラインインタプリタ.md "wikilink")

## 外部リンク

  - [Bob DuCharme: "The Operating Systems Handbook, Part 06: MVS" (available online)](http://www.snee.com/bob/opsys/part6mvs.pdf)

<!-- end list -->

  - [MVS便利帳](http://www33.ocn.ne.jp/~yfuku/mvs/mvsindex.html)（JCL簡易解説、よく使うかもしれないコマンド、マニュアルへのリンク）

[Category:IBMのオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:IBMのオペレーティングシステム "wikilink") [Category:メインフレームのオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:メインフレームのオペレーティングシステム "wikilink") [Category:1974年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1974年のソフトウェア "wikilink")