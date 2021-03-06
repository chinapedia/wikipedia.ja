> この記事は[MINIX](https://ja.wikipedia.org/wiki/MINIX)から翻訳されています。


{{ infobox OS | name = MINIX | screenshot = [250px](https://ja.wikipedia.org/wiki/ファイル:MINIX_screenshot.png "wikilink") | caption = MINIX 3.1.2a | developer = [アンドリュー・タネンバウム](../Page/アンドリュー・タネンバウム.md "wikilink") | family = [Unix系](../Page/Unix系.md "wikilink") | version_number = Varies | source_model = [オープンソース](../Page/オープンソース.md "wikilink") | working_state = 開発継続中 | latest_release_version = 3.3.0 | latest_release_date =  | kernel_type = [マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink") | ui = [ash](../Page/Almquist_Shell.md "wikilink") | license = [BSDライセンス](../Page/BSDライセンス.md "wikilink") | website =  }} **MINIX**（ミニックス）とは、[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")に[オランダ](https://ja.wikipedia.org/wiki/オランダ "wikilink")・[アムステルダム自由大学](https://ja.wikipedia.org/wiki/アムステルダム自由大学 "wikilink")（）の教授である[アンドリュー・タネンバウム](../Page/アンドリュー・タネンバウム.md "wikilink")が、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")(OS) の教育用に執筆した著書、『』の中で例として開発した、[Unix系](../Page/Unix系.md "wikilink")の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) である。Minixの名は"mini-Unix"から。

## 歴史

[UNIX](../Page/UNIX.md "wikilink")の[ソースコード](../Page/ソースコード.md "wikilink")が[AT\&T](../Page/AT&T.md "wikilink")のライセンス問題により非公開になった\[1\]ため、OSの教材用にUNIX version 7の互換システムを再設計したものである。機能上の新しさはないが、[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")構造を採用するなど、モダンな洗練が行われている。元々は[IBM PCをターゲットとして開発されたが](../Page/IBM_PC.md "wikilink")、その後[Atari](../Page/アタリ_\(企業\).md "wikilink")、[Amiga](../Page/Amiga.md "wikilink")、[Macintosh](../Page/Macintosh.md "wikilink")、[SPARC](../Page/SPARC.md "wikilink")をはじめ、日本においては[NEC](https://ja.wikipedia.org/wiki/NEC "wikilink") [PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")\[2\]にも移植された。

## 特徴

初期のバージョンは非常にコンパクトであり、[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")単体での運用もできた。2005年にリリースされたMINIX 3では動作にハードディスクを要するものの、[割り込みハンドラ](https://ja.wikipedia.org/wiki/割り込みハンドラ "wikilink")、[プロセススケジューラ](../Page/スケジューリング.md "wikilink")、[プロセス間通信](../Page/プロセス間通信.md "wikilink")機能などを含むマイクロカーネル本体のソースコードは4000行弱に抑えられている。

1987年のリリース当初からすべてのコードは公開されていたが[オープンソース](../Page/オープンソース.md "wikilink")ではなかった。これは出版社である[Prentice Hall](https://ja.wikipedia.org/wiki/:en:Prentice_Hall "wikilink") の意向と、タネンバウム自身による「MINIXはあくまで教育用のホビーであり、実用が目的ではない」という考えによる。とりわけ特徴的なのは、MINIXには[仮想記憶](../Page/仮想記憶.md "wikilink")が実装されていなかったことである。

なお、ライセンスは[2000年](../Page/2000年.md "wikilink")に変更されて、過去のソースコードも含めて[BSDライセンス](../Page/BSDライセンス.md "wikilink")が採用されるようになった\[3\]。また、バージョン 3.2.0 からは[NetBSD](../Page/NetBSD.md "wikilink")との親和性を深め、コンパイラ、ブートローダー、ユーザーランドの置き換えを順次進めている。

## Linuxとの関係

MINIXの「実用を目的としない」というポリシーに対し、[ニュースグループ](../Page/ニュースグループ.md "wikilink") **[comp.os.minix](news:///comp.os.minix)** において、MINIXを実用に耐えるOSにしようという試みが提示された。しかし、タネンバウムは機能を追加することに否定的だったため、[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")は新たにOSを作ることを決断し、[1991年](../Page/1991年.md "wikilink")10月にはついに[Linux](../Page/Linux.md "wikilink") version 0.02がリリースされるに至った。

これに対し、タネンバウムはLinuxの設計に対する批判を展開し、論争が起こった（[アンドリュー・タネンバウムとリーヌス・トーヴァルズの議論](https://ja.wikipedia.org/wiki/アンドリュー・タネンバウムとリーヌス・トーヴァルズの議論 "wikilink")）\[4\]。

結果として、後発の[Linux](../Page/Linux.md "wikilink")や[FreeBSD](../Page/FreeBSD.md "wikilink")の方が広く普及することとなったが、MINIXのソースコードはコンパクトで初学者にも読みやすく、教材としての目的は十分に達しているといえる。

## 実装

### MINIX 1.0

タネンバウムは、アムステルダム自由大学で、MINIXを彼の教科書『オペレーティングシステム: 設計と実装』（[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")）で示されている原理を例示するために作成した。

おおよそ12,000行で構成された[Cによって書かれたMINIX](../Page/C言語.md "wikilink") 1.0の[カーネル](../Page/カーネル.md "wikilink")、[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")マネージャ、[ファイルシステム](../Page/ファイルシステム.md "wikilink")のソースコードは教科書の中に印刷されていた。Prentice Hallはまた、MINIXのソースコードと[バイナリ](../Page/バイナリ.md "wikilink")をリファレンスマニュアル付きで[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")に収めリリースした。MINIX 1はSeventh Edition UNIXとシステムコールの互換性がある\[5\]。

タネンバウムは当初、MINIXを[IBM PCとIBM](../Page/IBM_PC.md "wikilink") [PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")マイクロコンピュータに互換性を持つように開発していた。

### MINIX 1.5

MINIX 1.5は[1991年](../Page/1991年.md "wikilink")にリリースされ、IBM [PS/2](https://ja.wikipedia.org/wiki/PS/2 "wikilink")マイクロチャンネルシステムへのサポートを含み、Motorola 68000と[SPARC](../Page/SPARC.md "wikilink")のアーキテクチャに移植された。MINIX 1.5は、[Atari ST](../Page/Atari_ST.md "wikilink")、Commodore [Amiga](../Page/Amiga.md "wikilink")、[Apple](https://ja.wikipedia.org/wiki/Apple "wikilink") [Macintosh](../Page/Macintosh.md "wikilink")\[6\]、[Sun](https://ja.wikipedia.org/wiki/Sun "wikilink") SPARCstationの各プラットフォームをサポートする。また、非公式のポートとして、Intel 386（32ビットプロテクトモード）とNational Semiconductor [NS32532](https://ja.wikipedia.org/wiki/NS320xx#32332、32532、Swordfish、その他 "wikilink")、[ARM](../Page/ARMアーキテクチャ.md "wikilink")、Inmos transputerプロセッサーに対するものがあった。

### MINIX 2.0

68-kベースのアーキテクチャへの需要の衰退により、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")にリリースされたMINIX 2.0は[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")とSPARCへのみ提供された。MINIX 2.0はタネンバウムのテキストの第2版の主題であり、Albert Woodhullとともに開発され、テキストに同梱された[CD-ROM](../Page/CD-ROM.md "wikilink")に収録された。MINIX 2.0は[POSIX](../Page/POSIX.md "wikilink").1に準拠し\[7\]\[8\]、[32ビット](../Page/32ビット.md "wikilink")モードの386プロセッサをサポートしたほか、MINIX 1.5に含まれた[Amoeba](https://ja.wikipedia.org/wiki/Amoeba "wikilink")ネットワークのプロトコルを、[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")スタックで置き換えた。

#### Minix-vmd

Minix-vmdは、アムステルダム自由大学の研究者によって作成されたIA-32プロセッサ用のMINIX 2のバリアントで、[仮想メモリ](https://ja.wikipedia.org/wiki/仮想メモリ "wikilink")と[X Window Systemのサポートを追加した](../Page/X_Window_System.md "wikilink")。

### MINIX 3

[MINIX_3.2_Top_Command.png](https://ja.wikipedia.org/wiki/File:MINIX_3.2_Top_Command.png "fig:MINIX_3.2_Top_Command.png")"コマンド実行中のMINIX\]\] [Minix_3.png](https://ja.wikipedia.org/wiki/File:Minix_3.png "fig:Minix_3.png")（[twm](https://ja.wikipedia.org/wiki/twm "wikilink")）実行中のMINIX\]\]

MINIX 3は、[2005年](../Page/2005年.md "wikilink")[10月24日](../Page/10月24日.md "wikilink")、タネンバウムよってACMシンポジウムにおいてアナウンスされた。このOSは、依然としてタネンバウムとWoodhullのテキストで用いられていたが、これは「限られたリソースのシステムや[組み込み](https://ja.wikipedia.org/wiki/組み込み "wikilink")コンピュータ、また高い信頼性を要求するアプリケーションで使える」ことを目指して包括的に再設計された\[9\]。

MINIX 3は、現在[IA-32](../Page/IA-32.md "wikilink")と[ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")のシステムをサポートしている。OSは[Live CDのフォーマットで提供され](../Page/Live_CD.md "wikilink")、これはコンピュータにインストールすることなしに試すことができる。また、様々なバージョンの仮想化システム（[Bochs](../Page/Bochs.md "wikilink")、[QEMU](../Page/QEMU.md "wikilink")、[VMware](../Page/VMware.md "wikilink")、[VirtualBox](../Page/VirtualBox.md "wikilink")、[Virtual PCを含む](https://ja.wikipedia.org/wiki/Virtual_PC "wikilink")）にも対応している。

バージョン3.1.5は[2009年](../Page/2009年.md "wikilink")[11月5日](../Page/11月5日.md "wikilink")にリリースされ、[X11](https://ja.wikipedia.org/wiki/X11 "wikilink")、[emacs](https://ja.wikipedia.org/wiki/emacs "wikilink")、[vi](https://ja.wikipedia.org/wiki/vi "wikilink")、cc、[gcc](https://ja.wikipedia.org/wiki/gcc "wikilink")、[perl](https://ja.wikipedia.org/wiki/perl "wikilink")、[python](https://ja.wikipedia.org/wiki/python "wikilink")、[bash](https://ja.wikipedia.org/wiki/bash "wikilink")、zsh、ftp、[ssh](https://ja.wikipedia.org/wiki/SSH "wikilink")、telnet、pineなど400を超える[UNIX](../Page/UNIX.md "wikilink")のユーティリティプログラムを利用することができる。X11の追加により、このバージョンはテキストのみのシステムからの移行を示す。多くの場合、実行中のプロセスに影響を与えることなく、クラッシュしたドライバを自動的に再起動することができる。このようにMINIXは自己修復機能を持ち、高い信頼性を必要とするアプリケーションでも使用することができる\[10\]。MINIX3はまた、[仮想メモリ](https://ja.wikipedia.org/wiki/仮想メモリ "wikilink")管理をサポートしており、これはデスクトップOSとしての利用に適している。

バージョン3.2.0では、[ユーザーランド](https://ja.wikipedia.org/wiki/ユーザーランド "wikilink")の大部分が[NetBSD](../Page/NetBSD.md "wikilink")のものに置換され、[pkgsrc](https://ja.wikipedia.org/wiki/pkgsrc "wikilink")のサポートが追加された。これは、MINIXで利用できるソフトウェアの数を増加させた。また、[Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")は以前のコンパイラを置き換え、GNUデバッガである[GDB](https://ja.wikipedia.org/wiki/GDB "wikilink")が移植された\[11\]\[12\]。

続くMINIX 3.3.0は、[2014年](../Page/2014年.md "wikilink")9月にリリースされ、ARMがサポートされた。

2016年1月にはMinix 3.4.0RC(リリース候補)が利用可能になったが\[13\]、MINIX 3.4.0の安定版リリースはまだ発表されていない。

MINIXは、[C](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")、[FORTRAN](../Page/FORTRAN.md "wikilink")、[Modula-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink")、[Pascal](../Page/Pascal.md "wikilink")、[Perl](../Page/Perl.md "wikilink")、[Python](../Page/Python.md "wikilink")や[Tcl](https://ja.wikipedia.org/wiki/Tcl "wikilink")などを含む[プログラミング言語](../Page/プログラミング言語.md "wikilink")をサポートしている。また、MINIX 3の開発コミュニティは2016年のMINIXCon 2016に50人以上が出席するなど、いまでも活動中の状態である\[14\]。

2015年以降のすべてのIntelチップセットは、Intel Management Engineのソフトウェアコンポーネントとして内部的にMinix 3を実行している。\[15\]\[16\]

## ライセンス

MINIXの最初の開発時には、その[ライセンスは比較的自由であった](../Page/ソフトウェアライセンス.md "wikilink")。ライセンス料は他のオペレーティングシステムに比べて非常に少額(69ドル)であった。タネンバウムはMINIXを[学生](https://ja.wikipedia.org/wiki/学生 "wikilink")ができるだけアクセスしやすくすることを望んだが、彼の出版社は自由にコピーできる素材(ソースコードなど)を提供したくなかったため、わずかな料金を要する制限的ライセンス(タネンバウムの本の価格に含まれている)が妥協案として適用された。これにより、MINIXを自由に配布されるソフトウェアシステムの基礎として使用できなくなった。

1990年代初頭に[Linux](../Page/Linux.md "wikilink")や[386BSD](../Page/386BSD.md "wikilink")のような[フリーでオープンソースのUnixライクなオペレーティングシステムが利用できるようになると](https://ja.wikipedia.org/wiki/FOSS "wikilink")、多くの[ボランティア](../Page/ボランティア.md "wikilink")の[ソフトウェア開発者](https://ja.wikipedia.org/wiki/ソフトウェア開発者 "wikilink")たちはMINIXを放棄してこれらのオペレーティングシステムを支持した。2000年4月、MINIX 2は[パーミッシブ・ライセンス](https://ja.wikipedia.org/wiki/パーミッシブ・ライセンス "wikilink")(BSDライセンス)のもとでフリーでオープンソースのソフトウェアとなったが\[17\]、この時点までに他のオペレーティングシステムがその能力を超えており、主に学生やホビイストのためのオペレーティングシステムであり続けた。

## 脚注

<references/>

## 関連項目

  - [MINIXファイルシステム](https://ja.wikipedia.org/wiki/MINIXファイルシステム "wikilink")

  -
  -
  - [マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")

  - [モノリシックカーネル](../Page/モノリシックカーネル.md "wikilink")

  - [Linux](../Page/Linux.md "wikilink")

  - [xv6](https://ja.wikipedia.org/wiki/xv6 "wikilink")

## 参考文献

  -
  -
  -
## 外部リンク

  -
  - [minix-up project](http://minix-up.sourceforge.jp/)

  - [MINIX on VMware Player](http://minixvmp.com/)

  - [GitHubのMinixリポジトリ](https://github.com/Stichting-MINIX-Research-Foundation/minix/)

[Category:Unix系オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:Unix系オペレーティングシステム "wikilink") [Category:フリーソフトウェアOS](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアOS "wikilink") [Category:教育ソフトウェア](https://ja.wikipedia.org/wiki/Category:教育ソフトウェア "wikilink") [Category:1987年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1987年のソフトウェア "wikilink")

1.  [UNIX\#UNIXの普及と展開](https://ja.wikipedia.org/wiki/UNIX#UNIXの普及と展開 "wikilink")
2.  MINIXオペレーティング・システム　ANDREW S. TANENABAUM著　坂本 文監修　大西 輝代翻訳　株式会社アスキー発行　1989年4月21日発行 13頁 ISBN 4-7561-0000-7
3.  ["MINIX is now available under the BSD license"](http://minix1.woodhull.com/faq/mxlicense.html), Apr 9 2000, minix1.woodhull.com
4.  [ディベート：リナックスは時代遅れだ](http://www.oreilly.co.jp/BOOK/osp/OpenSource_Web_Version/appen_A/appen_A.html)
5.
6.
7.
8.
9.
10.
11.
12. [MINIX 3.2: A microkernel with NetBSD applications \[LWN.net](https://lwn.net/Articles/485658/)\]
13.
14.
15.
16. [Minix: Intel's hidden in-chip operating system](https://www.zdnet.com/article/minix-intels-hidden-in-chip-operating-system/)
17.