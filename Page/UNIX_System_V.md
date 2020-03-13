> この記事は[UNIX System V](https://ja.wikipedia.org/wiki/UNIX_System_V)から翻訳されています。


[Unix_history-simple.png](https://ja.wikipedia.org/wiki/File:Unix_history-simple.png "fig:Unix_history-simple.png") **System V**（システムファイブ、**SysV**）は、初期の商用[UNIX](../Page/UNIX.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の一種である。

## 概要

本来は[AT\&T](../Page/AT&T.md "wikilink")が開発し[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")に最初にリリースした。4つの主要バージョンがリリースされている（Release 1, 2, 3, 4）。その中でもSystem V Release 4、通称SVR4は最も成功したバージョンであり、いくつかの一般的なUNIXの機能の起源でもある。例えばシステムの立ち上がりとシャットダウンを制御する「SysV [init](https://ja.wikipedia.org/wiki/init "wikilink") スクリプト」（`/etc/init.d`）などである。また、このシステムは *[System V Interface Definition](../Page/System_V_Interface_Definition.md "wikilink")* (SVID) の元になっている。System V がどのように動作するかを定義したものである。

AT\&Tも System V が動作するハードウェアを販売していたが、ほとんどの顧客は、再販業者がAT\&Tの[リファレンス実装](../Page/リファレンス実装.md "wikilink")に基づいて実装したものを使っていた。 有名な System V の派生品としては、System V Release 3 をベースとしている[IBM](../Page/IBM.md "wikilink")の[AIX](../Page/AIX.md "wikilink")や[OpenServer](https://ja.wikipedia.org/wiki/OpenServer "wikilink")、System V Release 4 をベースにしている[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の[Solaris](../Page/Solaris.md "wikilink")や[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")の[HP-UX](../Page/HP-UX.md "wikilink")がある。他にも[NEC](https://ja.wikipedia.org/wiki/NEC "wikilink")の[EWS-UX](../Page/EWS-UX.md "wikilink")や[UP-UX](../Page/UP-UX.md "wikilink")とその後継OSの[UX/4800](https://ja.wikipedia.org/wiki/UX/4800 "wikilink")が System V Release 4 をベースにしていた。

1980年代から1990年代初めごろまで、System V は[BSD](../Page/BSD.md "wikilink")と並ぶ、UNIXの大きなふたつの系統のひとつだった。しかし、現在ではそれ以外の[Linux](../Page/Linux.md "wikilink")や[QNX](../Page/QNX.md "wikilink")の系統が大きく発展しているため、この言い方は過去のものである。[UNIX戦争](../Page/UNIX戦争.md "wikilink")と言われた時期、[BSD](../Page/BSD.md "wikilink")はデスクトップ[ワークステーション](../Page/ワークステーション.md "wikilink")等で使われたのに対し、System V は大規模[マルチユーザシステム向けのシステムを作ろうとしていた企業にとっては最善の選択だった](https://ja.wikipedia.org/wiki/マルチユーザー "wikilink")。[POSIX](../Page/POSIX.md "wikilink")のような標準化作業はこれらの実装の違いを減らすために行われた経緯がある。

## SVR1

最初のSystem Vであり、1983年にリリースされた\[1\]。AT\&Tの Unix Support Group が、[System III](../Page/UNIX_System_III.md "wikilink")（System IV は外部に公開されなかった\[2\]）と[ベル研究所](../Page/ベル研究所.md "wikilink")内で使われていた USG UNIX 5.0 をベースとして開発した。[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink") (UCB) で開発された BSD 4.1 から[vi](https://ja.wikipedia.org/wiki/vi "wikilink")エディタや[curses](https://ja.wikipedia.org/wiki/curses "wikilink")が導入されている。また、バッファや[inode](https://ja.wikipedia.org/wiki/inode "wikilink")キャッシュを追加することで性能を向上させている。[ディジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")(DEC)の[VAX](../Page/VAX.md "wikilink")と[PDP-11](../Page/PDP-11.md "wikilink")で動作した。[プロセス間通信](../Page/プロセス間通信.md "wikilink")機能として[メッセージ](../Page/メッセージ_\(コンピュータ\).md "wikilink")、[セマフォ](../Page/セマフォ.md "wikilink")、[共有メモリ](../Page/共有メモリ.md "wikilink")が導入されている。

## SVR2

System V Release 2 は[1984年](../Page/1984年.md "wikilink")4月にリリースされた\[3\]。[シェル](../Page/シェル.md "wikilink")機能と[SVIDが導入されている](../Page/System_V_Interface_Definition.md "wikilink")。新たなカーネル機能として、[ファイルロック](../Page/ファイルロック.md "wikilink")、[デマンドページング](../Page/ページング方式.md "wikilink")、[コピーオンライト](../Page/コピーオンライト.md "wikilink")が導入された\[4\]。「ポーティングベース; porting base」の概念が定式化され、このリリースでは DEC VAX 11/780 が選択された。「ポーティングベース」とはいわゆる[リファレンス実装](../Page/リファレンス実装.md "wikilink")であり、他のプラットフォームへの移植はそれに基づいて行われる。SVR2 カーネルの詳しい説明は Maurice J. Bach の著書 *The Design of the UNIX Operating System* にある\[5\] 。[アップルコンピュータの](../Page/アップル_\(企業\).md "wikilink") [A/UX](https://ja.wikipedia.org/wiki/A/UX "wikilink")はこのリリースに基づき（後にSVR3、SVR4、BSDから各種拡張を取り入れている）、そこに[Macintosh](../Page/Macintosh.md "wikilink")のツールボックスを導入している。初期の[HP-UX](../Page/HP-UX.md "wikilink")もSVR2からの派生だった\[6\]。

## SVR3

System V Release 3は[1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")にリリースされた\[7\]\[8\]。[STREAMS](../Page/STREAMS.md "wikilink")、リモートファイル共有 (RFS)、File System Switch（FSS）と呼ばれる一種の[仮想ファイルシステム](../Page/仮想ファイルシステム.md "wikilink")機構、機能の制限された[共有ライブラリ](../Page/ライブラリ.md "wikilink")、[Transport Layer Interface](../Page/Transport_Layer_Interface.md "wikilink") (TLI) ネットワーク[APIがサポートされている](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。最終版は[1988年](../Page/1988年.md "wikilink")の Release 3.2 であり、[XENIX](../Page/XENIX.md "wikilink")との互換性が追加されている。[OpenServer](https://ja.wikipedia.org/wiki/OpenServer "wikilink") などが、この3.2をベースとしていた。「ポーティングベース」にはAT\&Tの3B2コンピュータが選ばれた。[IBM](../Page/IBM.md "wikilink")の[AIX](../Page/AIX.md "wikilink")は SVR3 から派生したOSである。

## SVR4

System V Release 4.0 は1988年10月18日に発表され\[9\]、1989年以降に各社の商用UNIXとしてリリースされた\[10\]。[UNIX Systems Laboratories](https://ja.wikipedia.org/wiki/UNIX_Systems_Laboratories "wikilink")（USL）とサン・マイクロシステムズの共同開発であり、Release 3 と [4.3BSD](../Page/BSD.md "wikilink")、[XENIX](../Page/XENIX.md "wikilink")、[SunOS](../Page/SunOS.md "wikilink")の技術を統合したものである。以下のような新機能がある。

  - BSD起源: [TCP/IPサポート](../Page/インターネット・プロトコル・スイート.md "wikilink")、[ソケット](../Page/ソケット_\(BSD\).md "wikilink")、[ufs](../Page/Unix_File_System.md "wikilink")、複数グループのサポート、[csh](../Page/C_Shell.md "wikilink")
  - SunOS起源: [NFS](https://ja.wikipedia.org/wiki/NFS "wikilink")(ネットワークファイルシステム)、[仮想ファイルシステム](../Page/仮想ファイルシステム.md "wikilink")インタフェース（SVR3での "File System Switch" を置換）、[メモリマップドファイル](https://ja.wikipedia.org/wiki/mmap "wikilink")、新たな共有ライブラリ、 [GUI環境](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、[XDR](../Page/XDR.md "wikilink")、[ONC RPC](../Page/Open_Network_Computing_Remote_Procedure_Call.md "wikilink")
  - XENIX起源: [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")向け[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")、（x86版 System Vにおける）XENIXとのバイナリ互換
  - その他:
      - [ksh](../Page/KornShell.md "wikilink")
      - [ANSI X3J11 C互換](https://ja.wikipedia.org/wiki/C言語#C89 "wikilink")
      - 多国語対応 (Multi-National Language Support, MNLS)
      - [国際化の改善](../Page/国際化と地域化.md "wikilink")
      - [ABI](../Page/Application_Binary_Interface.md "wikilink")
      - [POSIX](../Page/POSIX.md "wikilink")、[X/Open](https://ja.wikipedia.org/wiki/X/Open "wikilink")、[SVID](../Page/System_V_Interface_Definition.md "wikilink")3 といった標準のサポート

主なプラットフォームはx86と[SPARC](../Page/SPARC.md "wikilink")だった（ポーティングベースとしては3B2もあった）。SPARC版は Solaris 2 としてサンがリリースしている（内部的には [SunOS](../Page/SunOS.md "wikilink") 5.x）。AT\&Tとサンの関係はSVR4のリリースまでであり、その後のSolarisは SVR4.x での更新に追随していない。サンは[2005年](../Page/2005年.md "wikilink")に Solaris 10 のソースコードを[オープンソース](../Page/オープンソース.md "wikilink")の[OpenSolaris](../Page/OpenSolaris.md "wikilink")としてリリースしたが、System V 由来の実装をオープンソース化するために大幅に修正している。

SVR4は多くのハードウェアベンダーに採用された（[HP-UX](../Page/HP-UX.md "wikilink")、[IRIX](../Page/IRIX.md "wikilink")など）。また移植業者（SCO、Microport、ESIX、UHC）\[11\]がx86版の拡張版を販売した。変わったところでは、[Amiga](../Page/Amiga.md "wikilink")の Amiga Unix、[アタリの](../Page/アタリ_\(企業\).md "wikilink") ASV SVR4 Unix などがある。他にも [Dell](../Page/デル.md "wikilink") SVR4\[12\]、[Bull](../Page/Bull.md "wikilink") SVR4 などがある。

### SVR4.0MP

[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")製チップを使っているベンダー（[ユニシス](../Page/ユニシス.md "wikilink")、ICL、[NCR](../Page/NCR_\(企業\).md "wikilink")、[オリベッティ](../Page/オリベッティ.md "wikilink")など）がコンソーシアムを結成して開発した。[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")を限定的にサポートしている。各プロセッサは[システムコール](../Page/システムコール.md "wikilink")を実行できるが、[割り込みはマスタープロセッサと呼ばれる](../Page/割り込み_\(コンピュータ\).md "wikilink")1つのプロセッサだけが処理するという方式であり、カーネルの大部分はそのマスタープロセッサ上で動作する\[13\]。

### SVR4.1 ES

Release 4.1 ES (Enhanced Security) は、[オレンジブック](https://ja.wikipedia.org/wiki/オレンジブック_\(セキュリティ\) "wikilink") B2 に準拠すべくセキュリティを強化した版で、[アクセス制御リスト](../Page/アクセス制御リスト.md "wikilink") (ACL) やダイナミック・ローダブル（カーネル）モジュール (DLM)をサポートしている\[14\]\[15\]。DLMとはドライバなどを実行時に動的にメモリにロードする機能のことである。

### SVR4.2

[1992年](../Page/1992年.md "wikilink")、AT\&T USL と[ノベルのジョイントベンチャー](../Page/ノベル_\(企業\).md "wikilink") Univel が創業。同年、System V 4.2 が Univel [UnixWare](../Page/UnixWare.md "wikilink") としてリリースされた。[VERITASファイルシステムを新たにサポートしている](../Page/VERITAS_File_System.md "wikilink")。

### SVR4.2MP

[1993年](../Page/1993年.md "wikilink")末ごろ完成。Release 4.2 MPでは、[対称型マルチプロセッサ](https://ja.wikipedia.org/wiki/対称型マルチプロセッサ "wikilink")システムサポートと、[POSIXスレッド](https://ja.wikipedia.org/wiki/POSIXスレッド "wikilink")を含む[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")機能が追加された。1995年に UnixWare 2 としてリリースされた\[16\]。

## SVR5

XENIXの開発元であるSCOは、UnixWareの商標権と System V Release 4.2 のコードベースの販売権をノベルから取得した。このころ主要ベンダー（Sun、IBM、HP）は既存の System V Release 4 のコードベースを独自に改造・拡張して使っていた。また、UNIXの商標権はノベルから [The Open Group](../Page/The_Open_Group.md "wikilink") に移管されている。System V Interface Definition を発展させた [Single UNIX Specification](../Page/Single_UNIX_Specification.md "wikilink") (SUS) に準拠したOSはUNIXを名乗れるようになった。アップルの[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")はBSDからの派生だが、SUSに準拠している。他にもBSDや System V の系統ではないOSがSUS準拠となっている。

System V Release 5 は1997年、SCOが開発した。SVR3から派生した [OpenServer](https://ja.wikipedia.org/wiki/OpenServer "wikilink") と UnixWare を統合したもので、大規模サーバ向けを意図していた\[17\]。SCO UnixWare 7 としてリリース。また OpenServer 6 もSVR5ベースだが、このバージョンは他社では全く使われていない。

## SVR6

System V Release 6 は、SCOが2004年末にリリースすると発表したが、結局キャンセルされた\[18\]。[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")システムをサポートする予定だった\[19\]。

## 脚注

## 外部リンク

  - [PC-clone UNIX Software Buyer's Guide](http://www.catb.org/~esr/faqs/clone-unix-guide.txt) by [エリック・レイモンド](../Page/エリック・レイモンド.md "wikilink")（[1994年](../Page/1994年.md "wikilink")、[USENETへのポスト](../Page/ネットニュース.md "wikilink")）
  - [Unix FAQ - history](http://www.faqs.org/faqs/unix-faq/faq/part6/)
  - [A Unix History Diagram](http://www.levenez.com/unix/) - 継続的に更新されているUNIX史。（オライリー）

[Category:System_V](https://ja.wikipedia.org/wiki/Category:System_V "wikilink") [Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:1983年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1983年のソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.  [SEVERAL MAJOR COMPUTER AND SOFTWARE COMPANIES ANNOUNCE STRATEGIC COMMITMENT TO AT\&T'S UNIX SYSTEM V, RELEASE 4.0](http://groups.google.com/group/comp.unix.questions/msg/2e02a599c5c62848) Amdahl, Control Data Corporation, et al、1988年10月18日
10.
11. [Eric S. Raymond](../Page/エリック・レイモンド.md "wikilink"), [A buyer's guide to UNIX versions for PC-clone hardware](http://www.catb.org/~esr/faqs/clone-unix-guide.txt), posted to [Usenet](../Page/ネットニュース.md "wikilink") November 16, 1994.
12.
13.
14.
15.
16.
17. Kenneth H. Rosen (1999). *UNIX: The Complete Reference*. McGraw-Hill Professional, pp. 23, 32, 33.
18. [SCO updates Unix, OpenServer product plans](http://www.infoworld.com/t/platforms/sco-updates-unix-openserver-product-plans-798) InfoWorld, August 19 2003
19.