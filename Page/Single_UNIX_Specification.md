> この記事は[Single UNIX Specification](https://ja.wikipedia.org/wiki/Single_UNIX_Specification)から翻訳されています。


**Single UNIX Specification**（**SUS**、唯一のUNIX仕様）は、"[UNIX](../Page/UNIX.md "wikilink")"を名乗ることができる[コンピュータ](../Page/コンピュータ.md "wikilink")の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) の標準規格全体を総称したものである。SUSは、[IEEE](../Page/IEEE.md "wikilink")と [The Open Group](../Page/The_Open_Group.md "wikilink") の標準化作業の結果に基づくもので、Austin Group が開発および保守を行っている。

## 歴史

[1980年代](../Page/1980年代.md "wikilink")中頃、様々なUNIX系OSの[インタフェースを標準化するプロジェクトが開始され](../Page/インタフェース_\(情報技術\).md "wikilink")、これらがSUSの元となった。標準化の必要性は様々なベンダーのシステムを使っている企業の要望によるもので、ベンダーの異なるシステムでのソフトウェア移植のコストをなるべく減らしたいということから始まった。その標準化のベースとしてUNIXが選択された。というのもUNIXはベンダーに依存していない中立なOSと考えられたからである。

この標準化作業の結果できたのが1988年の **IEEE 1003**（**[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")/[IEC](../Page/国際電気標準会議.md "wikilink") 9945**としても登録された）または**[POSIX](../Page/POSIX.md "wikilink")** (Portable Operating System Interface for uniX) である。

[1990年代](../Page/1990年代.md "wikilink")初期、それとは別に[UNIX戦争](../Page/UNIX戦争.md "wikilink")の結果として、いくつかの主要ベンダーが[COSEアライアンスを結成し](../Page/Common_Open_Software_Environment.md "wikilink")、Common API Specification または Spec 1170 と呼ばれる仕様を策定した。この仕様は無料で入手可能であったため、IEEEがアクセス料を徴収したPOSIXよりも一般化した。

1997年、the Open Group が **Single UNIX Specification Version 2** (SUSv2) をリリース\[1\]\[2\]。この仕様は以下の部分から構成されている。

  - Base Definitions, Issue 5
  - System Interfaces and Headers, Issue 5
  - Commands and Utilities, Issue 5
  - Networking Services, Issue 5
  - X/Open Curses, Issue 4, Version 2

そして、これが UNIX 98 ブランドの中核となった\[3\]。

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")、Austin Group と呼ばれる共同ワーキンググループがこれらの仕様の統合を開始し、その成果が **Single UNIX Specification Verision 3** (SUSv3) となり、**POSIX:2001**（正式には IEEE Std 1003.1-2001）としても採用された。これは2002年1月30日にリリースとなった\[4\]。この仕様は以下の部分から構成されている。

  - Base Definitions, Issue 6
  - System Interfaces and Headers, Issue 6
  - Commands and Utilities, Issue 6

そして、これが UNIX 03 ブランドの中核となった\[5\]。

2004年、POSIX:2001 の改訂版がリリースされ、2つの技術的訂正がなされている。これを **POSIX:2004**（正式には IEEE Std 1003.1-2004）と呼ぶ\[6\]\[7\]。

2008年12月、Austin Group は新たな大幅修正版 **POSIX:2008**（正式名称は IEEE Std 1003.1-2008）を公表した\[8\]\[9\]\[10\]。これが Single UNIX Specification, Version 4 (SUSv4) の中核となっている\[11\]。この仕様は以下の部分から構成されている。

  - Base Definitions, Issue 7
  - System Interfaces and Headers, Issue 7
  - Commands and Utilities, Issue 7

## 仕様

SUSv3 は全部で3700ページに及び、テーマ別に以下の4つに分けられている。

  - **Base Definitions (XBD)** - 仕様記述に使われる定義と約束事のリストと、準拠するシステムが必ず提供しなければならない[C言語](../Page/C言語.md "wikilink")の[ヘッダーファイル](https://ja.wikipedia.org/wiki/ヘッダーファイル "wikilink")のリスト。全部で84のヘッダファイルが提供されている。
  - **Shell and Utilities (XCU)** - ユーティリティ（コマンド）のリストとシェル [sh](https://ja.wikipedia.org/wiki/Bourne_shell "wikilink") の詳細。全部で160のユーティリティが示されている。
  - **System Interfaces (XSH)** - 提供しなければならない[システムコール](../Page/システムコール.md "wikilink")とC[ライブラリ](../Page/ライブラリ.md "wikilink")の詳細。全部で1123のシステムインタフェースが示されている。
  - **Rationale (XRAT)** - この標準についての解説

この標準でのユーザのコマンドラインインターフェイスとスクリプトインターフェイスは[POSIX](../Page/POSIX.md "wikilink")シェルであり、[KornShell](../Page/KornShell.md "wikilink") の初期バージョンをベースにした拡張版 [Bourne Shell](../Page/Bourne_Shell.md "wikilink") である。他のユーザレベルのプログラムやサービス、ユーティリティとしては、[awk](../Page/AWK.md "wikilink")、[echo](../Page/エコー_\(コンピュータ\).md "wikilink")、[ed](https://ja.wikipedia.org/wiki/ed_\(テキストエディタ\) "wikilink")、[vi](https://ja.wikipedia.org/wiki/vi "wikilink")などが含まれる。プログラムレベルで要求されているサービスとしては、[I/O](../Page/入出力.md "wikilink")（[ファイル](../Page/ファイル_\(コンピュータ\).md "wikilink")、[端末](../Page/端末.md "wikilink")、[ネットワーク](../Page/コンピュータネットワーク.md "wikilink")）サービスなどがある。標準にはテストプログラム集が付随していて、**PCTS** (**Posix Certification Test Suite**) と呼ばれている。

さらに、SUSには [CURSES](../Page/Curses.md "wikilink") (XCURSES) の仕様も含まれている。372の関数と3つのヘッダファイルが定義されている。これを含めると、SUSv3は全部で1742のインタフェースを定義している。

注意しなければならないのは、この仕様を満たすために[AT\&T](../Page/AT&T.md "wikilink")のUNIXの[ソースコード](../Page/ソースコード.md "wikilink")を使う必要はないという点である。実際、[IBM](../Page/IBM.md "wikilink")の[OS/390](https://ja.wikipedia.org/wiki/OS/390 "wikilink")（現在は[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")）はコードは完全に独自だが "UNIX"と名乗ることを認定されている。

## 準拠システムを示すマーク

準拠システムを示すふたつのマークが存在する。

  - UNIX 98 - SUS Version 2 に準拠したシステムを示すマーク
  - UNIX 03 - SUS Version 3 に準拠したシステムを示すマーク

これらより古い準拠システム示すマークとして UNIX 93 や UNIX 95 がある。

## 各種OSの準拠状況

  - [AIX](../Page/AIX.md "wikilink") - AIX 5L V5.2 にいくつか更新を加えたものと AIX 5L V5.3 と AIX 6.1 は UNIX 03 準拠として登録されている。AIX 5L V5.2 は UNIX 98 準拠として登録されている。
  - [HP-UX](../Page/HP-UX.md "wikilink") - HP-UX 11i V3 Release B.11.31 は UNIX 03 準拠として登録されている。それ以前のリリースは UNIX 95 として登録されていた。
  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") - UNIXを標榜しつつも長らくSUSを取得していなかったが、[Mac OS X v10.5 Leopard](../Page/Mac_OS_X_v10.5.md "wikilink")\[12\]\[13\]以降が Open Brand UNIX 03 に登録されている\[14\]。
      - [macOS Server](https://ja.wikipedia.org/wiki/macOS_Server "wikilink") - Leopard同様、Mac OS X Server v10.5 で Open Brand UNIX 03 に登録された\[15\]。
  - SCO
      - [UnixWare](../Page/UnixWare.md "wikilink") 7.1.3 は UNIX 95 準拠として登録されている。
      - [OpenServer](https://ja.wikipedia.org/wiki/OpenServer "wikilink") 5 は UNIX 93 準拠として登録されている。
  - [Solaris](../Page/Solaris.md "wikilink") - Solaris 10 は UNIX 03 準拠として登録されている（[富士通](../Page/富士通.md "wikilink")が登録）。Solaris 8 および 9 は UNIX 98 準拠として登録されている。
  - [Tru64 UNIX](../Page/Tru64_UNIX.md "wikilink") - Tru64 UNIX V5.1A およびその後のリリースは UNIX 98 準拠として登録されている。
  - [z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink") - IBM z/OSは1.9以前は UNIX 95 準拠として登録されていた。2007年9月28日にリリースされた z/OS 1.9 は UNIX 03 にさらに近くなると発表した（完全準拠かどうかは不明）\[16\]。
  - [IRIX](../Page/IRIX.md "wikilink") - [SGI](../Page/シリコングラフィックス.md "wikilink") IRIX 6.5 は UNIX 95 準拠として登録されている\[17\]。

### 登録されていないUNIX系システム

[Unix系](../Page/Unix系.md "wikilink")の[Linux](../Page/Linux.md "wikilink")や[FreeBSD](../Page/FreeBSD.md "wikilink")などのシステムベンダーは、仕様変更が頻繁に行われるため、その度に認証を受ける必要が生じ、コストに見合わないため認証を受けないのが一般的である\[18\]。

#### BSD系

現在、無料で入手可能な [BSD系システムは](../Page/BSDの子孫.md "wikilink") SUS 準拠として登録されていない。

FreeBSD は "C99 and POSIX Conformance Project" により SUS の大部分に準拠する計画がある\[19\]。

[DarwinはFreeBSDベースのオープンソースの](../Page/Darwin_\(オペレーティングシステム\).md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である。これはmacOSのサブセットのオープンソース版とも言える。DarwinはSUSv3準拠である\[20\]。

#### Linux

かつてドイツの Unifix Linux 2.0 という古いディストリビューション/バージョンが POSIX.1 に準拠していた。2007年12月の時点では、SUSに準拠・登録されたLinuxディストリビューションは存在していない。

[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")は、Linuxが可能な限り POSIX互換となるよう設計した\[21\]。当初、この大部分は推測によるもので、彼はLinuxが始まってからしばらくしてPOSIX標準の印刷されたものを購入した。彼は、他のシステムの[manページ](https://ja.wikipedia.org/wiki/manページ "wikilink")を見て、システムコールの動作を決めていたとも述べている\[22\]。

[Linux](../Page/Linux.md "wikilink")システムには、共通な拡張、共通なデファクトスタンダードがあり、それらは [Linux Standard Base](../Page/Linux_Standard_Base.md "wikilink") から提供されている。これは、POSIX 仕様や Single UNIX Specification その他のオープン標準に基づき、それらを一部拡張しているものである。[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")として多くの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")がこれを採用している。

## 参考文献

  -
## 脚注

## 関連項目

  - [UNIX戦争](../Page/UNIX戦争.md "wikilink")
  - [manページ](https://ja.wikipedia.org/wiki/manページ "wikilink")
  - [POSIX](../Page/POSIX.md "wikilink")
  - [オープンシステム](../Page/オープンシステム_\(コンピュータ\).md "wikilink")
  - [オープン標準](../Page/オープン標準.md "wikilink")

## 外部リンク

  - [The Single UNIX Specification](http://www.unix.org/what_is_unix/single_unix_specification.html)
      - [Text of the Single UNIX Specification, version 2](http://www.opengroup.org/onlinepubs/7990989775/)
      - [Text of the Single UNIX Specification, version 3 (= POSIX:2001), 2004 edition](http://www.opengroup.org/onlinepubs/009695399/)
      - [Text of POSIX.1-2017, 2018 edition](http://www.opengroup.org/onlinepubs/9699919799/)
  - [Register of products certified for the UNIX and other Open Group brands](https://www.opengroup.org/openbrand/register/)
  - [Unix-Wars](https://www.livinginternet.com/i/iw_unix_war.htm) (Living Internet)
  - [Unix Standards](http://www.faqs.org/docs/artu/ch17s02.html) ([エリック・レイモンド](../Page/エリック・レイモンド.md "wikilink"), *The Art of Unix Programming*)
  - [AIX Commands, Tools, Scripts and Explanations](http://icancompute.ca/aix)

[Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:IEEE標準](https://ja.wikipedia.org/wiki/Category:IEEE標準 "wikilink")

1.  [Keyword Search the Single UNIX Specification, Version 2](http://www.opengroup.org/onlinepubs/7990989775/)
2.
3.  [UNIX 98](http://www.opengroup.org/openbrand/register/xxm0.htm) The Open Group
4.
5.  [UNIX 03](http://www.opengroup.org/openbrand/register/xym0.htm) The Open Group
6.  [The Open Group Base Specifications Issue 6](http://www.opengroup.org/onlinepubs/009695399/)
7.
8.  [The Open Group Base Specifications Issue 7](http://www.opengroup.org/onlinepubs/9699919799/)
9.
10.
11. [Single UNIX Specification Version 4](http://www.unix.org/version4)
12.
13.
14.
15.
16.
17.
18.  UNIX ブランドを使用するのにかかる料金のリスト
19. [FreeBSD C99 and POSIX Conformance Project](http://www.freebsd.org/projects/c99/)
20. [compat(5)](http://developer.apple.com/documentation/Darwin/Reference/Manpages/man5/compat.5.html) manページ
21. [com.os.minix LINUX is obsolute](http://groups.google.com/group/comp.os.minix/browse_thread/thread/c25870d7a41696d2/f447530d082cd95d)
22. "Just for Fun - The story of an accidental revolutionary"邦題『[それがぼくには楽しかったから](https://ja.wikipedia.org/wiki/それがぼくには楽しかったから "wikilink")』(ISBN:4-7968-8001-1)