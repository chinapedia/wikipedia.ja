> この記事は[AIX](https://ja.wikipedia.org/wiki/AIX)から翻訳されています。


**AIX**（**A**dvanced **I**nteractive E**x**ecutive、エーアイエックス\[1\]）は、[IBM](../Page/IBM.md "wikilink") の [UNIX](../Page/UNIX.md "wikilink") [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")のブランド名である。

## 概要

AIX は [UNIX](../Page/UNIX.md "wikilink") [System V Release 3](https://ja.wikipedia.org/wiki/UNIX_System_V#SVR3 "wikilink") (SVR3) ベースの [IBM](../Page/IBM.md "wikilink") の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")で、[The Open Group](../Page/The_Open_Group.md "wikilink") の UNIX認証を受けている\[2\]。AIXは、IBM の [RT-PC](https://ja.wikipedia.org/wiki/RT-PC "wikilink")、[RS/6000](https://ja.wikipedia.org/wiki/RS/6000 "wikilink")、[pSeries](https://ja.wikipedia.org/wiki/pSeries "wikilink")、[System p](https://ja.wikipedia.org/wiki/System_p "wikilink")、[Power Systems](https://ja.wikipedia.org/wiki/Power_Systems "wikilink") シリーズの他、[フランス](https://ja.wikipedia.org/wiki/フランス "wikilink")の [Bull](../Page/Bull.md "wikilink") や、[日立製作所](../Page/日立製作所.md "wikilink")の [EP8000](https://ja.wikipedia.org/wiki/EP8000 "wikilink") シリーズやSR16000などでも採用されている。

最新版の AIX 7.2 では、[カーネル](../Page/カーネル.md "wikilink")は [64-bit](https://ja.wikipedia.org/wiki/64ビット "wikilink") で、[POWER](../Page/POWER_\(マイクロプロセッサ\).md "wikilink") 系の [CPU](../Page/CPU.md "wikilink")（[POWER7](https://ja.wikipedia.org/wiki/POWER7 "wikilink")、[POWER8](https://ja.wikipedia.org/wiki/POWER8 "wikilink")）をサポートする\[3\]。

## 特徴

### コマンド体系

AIX は [System V Release 3](https://ja.wikipedia.org/wiki/UNIX_System_V#SVR3 "wikilink") (SVR3) をベースに、更に [BSD](../Page/BSD.md "wikilink") や [System V Release 4](https://ja.wikipedia.org/wiki/UNIX_System_V#SVR4 "wikilink") (SVR4) などのコマンド等を追加したものである。このため SVR4 ベースの他の商用 UNIX（[Solaris](../Page/Solaris.md "wikilink") など）や、[UNIX 互換](../Page/Unix系.md "wikilink") OS である [Linux](../Page/Linux.md "wikilink") OS などとはコマンド体系が多少異なる。AIX V3 までは [Bourne Shell](../Page/Bourne_Shell.md "wikilink") をデフォルトのシェルとしていたが、AIX V4 以降は[XPG4と](https://ja.wikipedia.org/wiki/X/Open "wikilink")[POSIX](../Page/POSIX.md "wikilink")に準拠するため [KornShell](../Page/KornShell.md "wikilink") (ksh88) をデフォルトのシェルとするようになった\[4\]。

なお LM (Loadable Module) のオブジェクトフォーマット形式は、Power チップ間の非互換部分の吸収幅を残すため、[ELF](../Page/Executable_and_Linkable_Format.md "wikilink") ではなく [COFF](../Page/COFF.md "wikilink") の拡張である [XCOFF](https://ja.wikipedia.org/wiki/:en:XCOFF "wikilink")（拡張共通オブジェクト・ファイル形式、XCOFF32 および XCOFF64）を使用している。

### 論理ボリュームマネージャ

[論理ボリュームマネージャ](../Page/論理ボリュームマネージャ.md "wikilink") (LVM) を比較的早く採用している。AIX では更にディスク装置のミラーリングやストライピングをサポートし、AIX 5L 5.2 以降では稼働中のバックアップ機能 (split copy)、AIX 5L V5.3 以降ではスケーラブル・ボリュームグループ、AIX V6.1 ではログ収集機能が強化された。

### ジャーナルファイルシステム

[ジャーナルファイルシステムである](../Page/ジャーナリングファイルシステム.md "wikilink") [JFS](../Page/Journaled_File_System.md "wikilink")/JFS2 を実装している。JFS は、ディスク障害時の回復時間を短縮する[ファイルシステム](../Page/ファイルシステム.md "wikilink")である。JFS では最大 64 [GiB](https://ja.wikipedia.org/wiki/ギビバイト "wikilink") のファイル、最大 1 [TiB](https://ja.wikipedia.org/wiki/テビバイト "wikilink") のファイルシステムを作成できる。JFS2 では最大1 TiB（AIX 5L V5.2 以降では、最大 16 TiB）のファイルおよびファイルシステムを作成できる。また AIX 5L V5.2 以降の JFS2 は snapshot コマンドによるスナップショットバックアップ、AIX 5L V5.3 以降の JFS2 ではファイルシステムサイズの動的縮小、AIX V6.1 の JFS2 では暗号化ファイルシステムがサポートされた。

### デスクトップ環境

標準の[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")は [CDE](../Page/Common_Desktop_Environment.md "wikilink") である。[COSE](../Page/Common_Open_Software_Environment.md "wikilink") で採用されてから一貫して標準搭載している。なお AIX Toolbox for Linux Applications（後述）には [KDE](../Page/KDE.md "wikilink") や [GNOME](../Page/GNOME.md "wikilink") も含まれている。

### 管理ツール

他の [UNIX](../Page/UNIX.md "wikilink") および [UNIX 互換](../Page/Unix系.md "wikilink") OS と比較して特徴的な点として、主要なシステム設定を階層型の管理画面である [SMIT](https://ja.wikipedia.org/wiki/SMIT "wikilink") から行う（[HP-UX](../Page/HP-UX.md "wikilink") の SAM に相当する）。また主要なシステム設定情報は **ODM** という /etc ディレクトリ配下のデータベースに[バイナリ](../Page/バイナリ.md "wikilink")形式で格納される。このためコマンドの知識が少ないユーザーでも操作を行え履歴も残り、システム設定ファイルの誤編集による問題も発生しにくいが、仮にデータベース情報の不整合などが発生した場合は専用の知識が必要である。

### 大規模ワークロードサポート

AIX7の時点で、最大256プロセッサー・コア、1024スレッドをサポートする。

### 仮想化

ハードウェアの機能と連係し、商用UNIXとしては早い時期から各種の仮想化をサポートしており実績も多い。物理分割([PPAR](../Page/PPAR.md "wikilink"))よりも柔軟性の高い論理区画([LPAR](../Page/LPAR.md "wikilink"))、LPARへの動的なリソースの割当変更が可能な[Dynamic Logical Partitioning](https://ja.wikipedia.org/wiki/Dynamic_Logical_Partitioning "wikilink")、LPARへCPUを 1/100 単位で割当可能な[Micro-Partitioning](https://ja.wikipedia.org/wiki/Micro-Partitioning "wikilink")、1つの AIX インスタンス内で複数の AIX 環境を作成できる[Workload Partition](https://ja.wikipedia.org/wiki/Workload_Partition "wikilink") (WPAR) 、稼働中のLPARを別の物理マシン（別筐体）へ移動できる[Live Partition Mobility](https://ja.wikipedia.org/wiki/Live_Partition_Mobility "wikilink")、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink") [32ビット](../Page/32ビット.md "wikilink") [Linux](../Page/Linux.md "wikilink")アプリケーションのバイナリを無修正で実行できる[Lx86](https://ja.wikipedia.org/wiki/Lx86 "wikilink")などである。これらは[PowerVM](../Page/PowerVM.md "wikilink")として総称されている。

### Linux との親和性

AIX 4.3.3 以降から付属する CD-ROM の AIX Toolbox for Linux Applications には、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")および[オープンソース](../Page/オープンソース.md "wikilink")の AIX 用ツールが含まれている。またAIXバージョン5は「AIX 5L」とネーミングされたが、"L" は[Linux](../Page/Linux.md "wikilink")との親和性(Linux Affinity)を意味し、Linux のプログラムソースの移植性を高めた。

### パッチ

累積フィックスであるフィックスパック (Fix Pack) は、IBM のサイト (Fix Central) よりダウンロードできる。従来は ML (Maintenance Level)、SP (Service Pack)、CSP（Concluding Service Pack、各 ML レベルでの最終の SP）の組み合わせだったが、[2006年](../Page/2006年.md "wikilink")2月より **TL**（Technology Level、年2回、通常は2月と8月）、SP、CSP の組み合わせに変更され、更に[2007年](../Page/2007年.md "wikilink")に CSP は廃止された。ML は過去の ML および SP を含む。SP は過去の SP を含む。2月の TL は安定性重視（フィックスおよび新ハードウェアのサポート中心）だが、8月の TL は更に機能拡張を含む。

単体フィックス (PTF) は現在は原則として提供されないが、緊急性・重要度が高いものは暫定フィックス（Interim fix、iFix、i-fix、IF。従来の緊急フィックス、e-fix）として暫定提供される。これらも最終的には TL、SP 等に含まれる。

現状の確認は AIX 4.3 では `instfix`、AIX 5L 以降では更に `oslevel -r` または `-s` などで行う。暫定フィックスは `fixmgr` で管理する。

## 歴史

いくつかの異なるバージョンの AIX がかつて存在していたが、不人気なものは消えていった。

[1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")に登場した AIX V1 は [IBM RT-PC](../Page/IBM_RT-PC.md "wikilink") で動作した。このバージョンは [UNIX System V](../Page/UNIX_System_V.md "wikilink") Release 3 をベースにしていた。

[1989年](../Page/1989年.md "wikilink")、AIX は [RS/6000](https://ja.wikipedia.org/wiki/RS/6000 "wikilink") シリーズのワークステーションとサーバ用 OS となった。AIX は開発の過程で 4.2[BSD](../Page/BSD.md "wikilink") や 4.3[BSD](../Page/BSD.md "wikilink") の機能を IBM と INTERACTIVE Systems Corporation がマージした。

[UNIX 戦争の際には](../Page/UNIX戦争.md "wikilink")、AIX は [OSF](../Page/Open_Software_Foundation.md "wikilink") 陣営の [OSF/1](https://ja.wikipedia.org/wiki/OSF/1 "wikilink") のカーネルとして採用された。OSF/1 は普及しなかったが、[論理ボリュームマネージャ](../Page/論理ボリュームマネージャ.md "wikilink") (LVM) はこの際に [HP-UX](../Page/HP-UX.md "wikilink") などに移植された。

1994年には [SMP](https://ja.wikipedia.org/wiki/対称型マルチプロセッサ "wikilink") 対応を行っていたが、SMP によるスケールアップ型の性能向上よりも、RS6000-SP (Scallable parallel) に代表されるスケールアウト型による並列処理性能の拡充を目指していた。世界のチェス王者を破ったシステムも、AIXが稼動するRS/6000-SP であった。[2001年](../Page/2001年.md "wikilink")、AIX 5L の登場と共に、1チップでSMP構成が可能な POWER4 プロセッサーを複数接続した大規模 SMP 構成のサーバを発表し、真の意味でエンタープライズ領域での必要な可用性と、Linux との先端的な親和性などを加え、基幹系 UNIX ベンダーとして疾走を始めた。

この2001年の AIX 5L の登場以降、可用性の圧倒的な向上とスケーラビリティの向上、CPU 性能の強化による性能の大幅向上を武器に IBM 社による強力なセールスによりライセンス数を伸ばし、基幹系システムにおける商用 UNIX としては [HP-UX](../Page/HP-UX.md "wikilink") と並んで主流であり、基幹系適用に際して必須とされる高信頼性・高可用性がある。

さらに IBM 製 UNIX および Linux OS の基幹系への圧倒的な傾注と、やっと基幹系向けとして認知された [Itanium](../Page/Itanium.md "wikilink") 系への不人気もあり、現状として基幹系ではトップの伸び率を誇る。

AIX 5L 5.3 でのスケーラビリティは以下の通りである。

  - 最大 64 [プロセッサ](../Page/CPU.md "wikilink")
  - [主記憶](../Page/主記憶装置.md "wikilink") 2 Tバイト
  - [JFS](../Page/Journaled_File_System.md "wikilink")2: 最大ファイルシステムサイズ 16 [TiB](https://ja.wikipedia.org/wiki/テビバイト "wikilink")
  - JFS2: 最大ファイルサイズ 16 TiB

## サポートするアーキテクチャ

  - AIX v1…[IBM PS/2](https://ja.wikipedia.org/wiki/IBM_PS/2 "wikilink") [Micro Channel Architecture](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink") PC と [IBM RT](../Page/IBM_RT-PC.md "wikilink")。
  - AIX v2…6150-シリーズ IBM RT。
  - AIX v3…[POWER](../Page/POWER_\(マイクロプロセッサ\).md "wikilink") アーキテクチャサポート開始。
  - AIX v4…[PowerPC](../Page/PowerPC.md "wikilink") アーキテクチャと [PCI](../Page/Peripheral_Component_Interconnect.md "wikilink") バスサポート開始。
  - AIX v5…[IA64](../Page/Itanium.md "wikilink") アーキテクチャサポート（ただし、β 版のまま商用化されていない\[5\]\[6\]）。
      - AIX v5.1…POWER4 での論理パーティショニングサポート。[Micro Channel Architecture](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink") サポートはこのバージョンまで。
      - AIX v5.2…[PowerPC 970](../Page/PowerPC_970.md "wikilink") ベースのブレードサーバサポート。途中より[Dynamic LPARのサポート](https://ja.wikipedia.org/wiki/:en:Dynamic_Logical_Partitioning "wikilink")。
      - AIX v5.3…POWER5 での[Micro-Partitioning](https://ja.wikipedia.org/wiki/Micro-Partitioning "wikilink")サポート。
  - AIX v6.1…POWER6 での[Live Partition Mobilityサポート](https://ja.wikipedia.org/wiki/Live_Partition_Mobility "wikilink")。
  - AIX v7.1
  - AIX v7.2…暫定修正(i-fix)用のAIX Live Update、CAA自動化、SRIOVでのVNICなど。

### メインフレームでの AIX

1988年、IBM は AIX/370 を発表した。[System/370](https://ja.wikipedia.org/wiki/System/370 "wikilink") で UNIX 風の機能を提供するものである。AIX/370 は 1990年にリリースされ、System V Release 2 と 4.3BSD の機能に IBM 独自の機能拡張がされたものとなっていた。[System/390](https://ja.wikipedia.org/wiki/System/390 "wikilink") のアーキテクチャ (ESA/390) が登場すると、1991年には AIX/370 を AIX/ESA とし、[OSF/1](https://ja.wikipedia.org/wiki/OSF/1 "wikilink") のコードをベースとした[カーネル](../Page/カーネル.md "wikilink")で System/390 上で動作させた。AIX/ESA はネイティブ OS としても VM 上のゲスト OS としても動作する。しかし、商業的には成功とは言い難く、現在では [Linux](../Page/Linux.md "wikilink") on System z にその座を譲っている。

### アップル製ハードでの AIX

1996年、[アップルコンピュータはサーバの最上位シリーズとして](../Page/アップル_\(企業\).md "wikilink")、AIXが標準OSで[PowerPC 604ベースの](../Page/PowerPC_604.md "wikilink")[Apple Network Serverを開発し](https://ja.wikipedia.org/wiki/:en:Apple_Network_Server "wikilink")、他にはない様々な拡張を施した。このシリーズ以外にアップルでAIXを採用した例はなく、翌年には販売終了と短命に終っている。

### 日立製ハードでの AIX

[日立のエンタープライズサーバ](../Page/日立製作所.md "wikilink")\[7\][EP8000](https://ja.wikipedia.org/wiki/EP8000 "wikilink") シリーズは Power Systems と互換性が高いハードウェア（ファームウェアも提携）であり、OS は AIX である。同社のスーパコンピュータ（同社の呼称ではスーパーテクニカルサーバ）SRシリーズのOSも、プロセッサがPA-RISCベースだったSR8000シリーズまではHP-UXベースであったが、POWERベースに変更したSR11000シリーズ以降ではAIXベースである。

## バージョン

  - AIX v1, [1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")
  - AIX v2, [1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")
  - AIX v3, [1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")
  - AIX v3.1
      - [Journaled File System](../Page/Journaled_File_System.md "wikilink") (JFS) をサポート
  - AIX 4.1, [1994年](../Page/1994年.md "wikilink")
      - [SMP](https://ja.wikipedia.org/wiki/対称型マルチプロセッサ "wikilink") をサポート
  - AIX 4.2.1, [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")4月
      - [NFS](https://ja.wikipedia.org/wiki/NFS "wikilink") Version 3 をサポート
  - AIX 4.3, 1997年10月
      - 64ビット[CPU](../Page/CPU.md "wikilink") をサポート
      - UNIX98 認証
      - IPv6
  - AIX 4.3.3, [1999年](../Page/1999年.md "wikilink")9月
      - オンラインバックアップ機能追加
      - ワークロード管理 (WLM)
  - AIX 5L 5.1, [2001年](../Page/2001年.md "wikilink")5月（“5L” の L は [Linux](../Page/Linux.md "wikilink") との相互運用性を高めたことを示す。)
      - [カーネル](../Page/カーネル.md "wikilink")の64ビット化
      - POWER4 をサポート
      - ロジカルパーティション（LPAR。マルチプロセッサシステムを論理的に複数に分割して、CPU・メモリー・I/O などのリソースを割当できる。物理分割 \[PPAR\] と異なり、CPU は1プロセッサを0.1単位で、I/O ならば PCI スロット単位で、配分できる。）
      - JFS2
  - AIX 5L 5.2, [2002年](../Page/2002年.md "wikilink")10月
      - POWER4+ をサポート
      - マルチパス I/O [ファイバーチャネル](../Page/ファイバーチャネル.md "wikilink")ディスクをサポート
      - [iSCSI](https://ja.wikipedia.org/wiki/iSCSI "wikilink")
      - ダイナミック・ロジカルパーティション（D-LPAR。LPAR の拡張。パーティション内で AIX が稼動中に、CPU などのリソース割当を自動または手動で変更できる。）
  - AIX 5L 5.3, [2004年](../Page/2004年.md "wikilink")8月
      - POWER5 をサポート
      - マイクロパーティションをサポート（LPAR・D-LPAR より更に細かいリソース配分が可能。CPU は1プロセッサを100分の1単位で配分できる。）
      - 仮想 I/O サーバ（VIOS。仮想 [SCSI](../Page/Small_Computer_System_Interface.md "wikilink")、仮想[イーサネット](../Page/イーサネット.md "wikilink")など。）
      - [NFS](../Page/Network_File_System.md "wikilink") Version 4 をサポート
      - 拡張アカウンティング
      - [同時マルチスレッディング](../Page/同時マルチスレッディング.md "wikilink") (SMT) をサポート
      - JFS2 クォータサポート
      - JFS2 ファイルシステム縮小をサポート
  - AIX 6.1 [2007年](../Page/2007年.md "wikilink")11月\[8\]
      - [Workload Partitions](https://ja.wikipedia.org/wiki/Workload_Partition "wikilink") (WPARs)
      - [Live Partition Mobility](https://ja.wikipedia.org/wiki/Live_Partition_Mobility "wikilink")
      - Role Based Access Control ([RBAC](../Page/ロールベースアクセス制御.md "wikilink"))
      - AIX Security Expert enhancements
      - Name Resolver Caching Daemon
      - probevue dynamic tracing
      - System Director Console for AIX
  - AIX 7.1 [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")8月発表\[9\]
      - Express、Standard、Enterprise の3エディション化
  - AIX 7.2 2015年10月発表

## 脚注

## 関連項目

  - [UNIX](../Page/UNIX.md "wikilink")
  - [IBM](../Page/IBM.md "wikilink")
  - [Project Monterey](../Page/Project_Monterey.md "wikilink")
  - [IBM i 統合オペレーティング環境（旧称 : AS/400、ESERVER I SERIES、SYSTEM I）](https://www.ibm.com/jp-ja/it-infrastructure/power/os/ibm-i)

## 外部リンク

  - [IBM AIX — 日本IBM](https://www.ibm.com/jp-ja/it-infrastructure/power/os/aix)
  - [Power Systemsソフトウェア — 日本IBM](https://www.ibm.com/jp-ja/it-infrastructure/power/software)
  - [IBM マーケットプレイス](https://www.ibm.com/jp-ja/products)
  - [IBM ソフトウェア](https://www.ibm.com/software/jp/)
  - [AIX - 日立製作所](http://www.hitachi.co.jp/Prod/comp/soft1/AIX/product/lineup/aix5los.html)
  - [IBM AIX 7.1 インフォメーションセンター](http://publib.boulder.ibm.com/infocenter/aix/v7r1/index.jsp)
  - [developerworks AIX and UNIX](http://www.ibm.com/developerworks/aix/)
  - [Parallel Environment for AIX 5L V4.1.1 Hitchhiker's Guide (AIX 並列環境のヒッチハイクガイド)](http://publib.boulder.ibm.com/infocenter/clresctr/topic/com.ibm.cluster.pe.doc/pe_411/am104001/am10400102.html#wq1)……IBM 自身の手によるパロディ・ページ。AIX を使用している[ディープ・ブルーには](../Page/ディープ・ブルー_\(コンピュータ\).md "wikilink")、「[銀河ヒッチハイクガイド](https://ja.wikipedia.org/wiki/銀河ヒッチハイクガイド "wikilink")」の「[生命、宇宙、そして万物についての究極の疑問の答え](../Page/生命、宇宙、そして万物についての究極の疑問の答え.md "wikilink")」から名称が取られている。

[Category:IBMのオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:IBMのオペレーティングシステム "wikilink") [Category:System_V](https://ja.wikipedia.org/wiki/Category:System_V "wikilink") [Category:1986年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1986年のソフトウェア "wikilink") [Category:PowerPCオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:PowerPCオペレーティングシステム "wikilink")

1.  [Unix Pronounciation](http://tehtable.wordpress.com/2010/01/29/unix-pronunciation)
2.
3.
4.
5.  [Unigroup's April 2004 Meeting Announcement](http://www.unigroup.org/unigroup-0404.html)
6.
7.  ほぼメインフレームであるが、同社はUnixをOSとするメインフレームを「エンタープライズサーバ」と呼称している。
8.
9.  [IBM AIX V7およびPowerVM V2機能拡張の発表](http://www-06.ibm.com/jp/domino02/NewAIS/aisextr.nsf/ByLetterNo/PWR10090)