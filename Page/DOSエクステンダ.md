> この記事は[DOS](https://ja.wikipedia.org/wiki/DOS)から翻訳されています。


**DOSエクステンダ**（ドスエクステンダ）とは、[MS-DOS](../Page/MS-DOS.md "wikilink")などの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")を拡張するためのプログラムのことであり、[アプリケーションプログラム](https://ja.wikipedia.org/wiki/アプリケーションプログラム "wikilink")の操作・実行環境である。

## 概要

DOSエクステンダは、アプリケーションソフトウェアが、[MS-DOS](../Page/MS-DOS.md "wikilink")環境下において[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")[CPU](../Page/CPU.md "wikilink")の[プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")を利用するためのプログラムである。通常は、MS-DOSより起動され、DOSエクステンダ専用のアプリケーションソフトの実行を可能にする。他にも、MS-DOS用のプログラムを[マルチタスク](../Page/マルチタスク.md "wikilink")で稼働させるものや、[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")を提供するものなど、DOSエクステンダと、その上で実行されるプログラムの種類に応じて、様々な機能が提供される。

MS-DOS上では通常、メモリアドレスは1メガバイト以内、CPU命令も16bit用のそれしか用いることができず、例え32bitCPUであっても、実質的には高速な16bitCPUとしてのみ利用され、CPUが32bitである意味は薄かった。しかし、386|DOS-Extender などの32bit命令/メモリアドレスに対応したDOSエクステンダを用いる事により、MS-DOSを経由して32bit環境を構築する事が可能となり、種々の制約に縛られながらも、16bit環境と比較すればアプリケーションのパフォーマンスは大幅に向上した。

また、副次的なことながら、従来のMS-DOSプログラムでほぼ必須であった[Intel 8086由来の制限による複雑なメモリモデルや](../Page/Intel_8086.md "wikilink")[C言語](../Page/C言語.md "wikilink")での[ポインタ制御](../Page/ポインタ_\(プログラミング\).md "wikilink")、セグメント切り替えなどの必要性が、事実上ほぼ撤廃され、これにより開発効率の向上や、更なる速度面での優位性も確保されている。このことは、従来のMS-DOS環境では、連続して扱えるメモリ領域(リニアメモリ)が64[KiB](https://ja.wikipedia.org/wiki/KiB "wikilink")、もしくは1[MiB](https://ja.wikipedia.org/wiki/MiB "wikilink")に過ぎなかったことに起因する。Windowsの、[Microsoft Windows 3.x以前のもの及び](../Page/Microsoft_Windows_3.x.md "wikilink")[Microsoft Windows 9x系も](https://ja.wikipedia.org/wiki/Microsoft_Windows_9x "wikilink")、技術的にはDOSから起動され[プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")で稼働する、DOSエクステンダの一種、ないし、一体化しているDOSエクステンダ上で稼働する[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")と言える。

[プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")で稼働するアプリケーションは、通常の[EXEフォーマット](../Page/EXEフォーマット.md "wikilink")のプログラムではなく、提供されるDOSエクステンダ専用にコンパイルされたプログラムでないと実行できない。またDOSエクステンダごとに実行可能なプログラムの形式は異なり、たとえばRUN386でGO32用にコンパイルされたプログラムを実行することはできない。この事は、DOSエクステンダが、その有用性が認識されながらも、大きく普及が進まなかった要因の1つとなった。

DOSエクステンダには、[DESQview](../Page/DESQview.md "wikilink")や、PharLap Softwareが開発した386|DOS-Extender (RUN386)等がある。RUN386は[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")用、[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")用、[FMRシリーズ](../Page/FMRシリーズ.md "wikilink")用と[FM TOWNS用が存在し](../Page/FM_TOWNS.md "wikilink")、機種依存の[BIOS等を直接利用しない限りどの機種でも同じプログラムを実行できる](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")。なおRUN386用の実行プログラムの[拡張子](../Page/拡張子.md "wikilink")は.EXP（EXecutable Programの略とされている）である。

現在では[Windowsの普及で](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、DOSエクステンダはその役目を失いつつある。

## 技術的特徴

[MS-DOS](../Page/MS-DOS.md "wikilink")でアクセス可能なメモリ空間（コンベンショナルメモリ）は、最大でも640KB([PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")および[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")等)から768KB (PC-H98等)であった。[8086は](../Page/Intel_8086.md "wikilink")[アドレス空間](../Page/アドレス空間.md "wikilink")が1Mバイトしか無かったため、最大で16Mバイトまで使用できる[80286をインテルは発表するが](../Page/Intel_80286.md "wikilink")、16Mバイトまでメモリが使用できる16ビット[プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")をサポートしたのは、当初は[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")等の[マルチタスク](../Page/マルチタスク.md "wikilink")OSだけであった。しかしながら[80286や上位互換の](../Page/Intel_80286.md "wikilink")[80386は](../Page/Intel_80386.md "wikilink")、[マルチタスク](../Page/マルチタスク.md "wikilink")OSを快適に使用するには速度不足であったし、当時のPCは複数の[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")を同時に実行するには実装しているメモリが不足していた。そのため多くのユーザーはMS-DOSを利用しつづけたのである。

やがてMS-DOS上でメモリ容量が不足してくると、様々な方法でMS-DOSで利用可能なメモリ容量を拡張する試みがなされた。それらの内、80286で導入されたプロテクトモードを使用してアドレス空間の大きさそのものを拡張することにより、MS-DOS上でアプリケーションで利用可能なメモリ容量を拡張するソフトウェアがDOSエクステンダである。

一般にDOSエクステンダは[シングルタスク](https://ja.wikipedia.org/wiki/シングルタスク "wikilink")であったので、これらの低速なCPUでも快適に利用できたし、せいぜい数Mバイト程度しか[プロテクトメモリ](https://ja.wikipedia.org/wiki/プロテクトメモリ "wikilink")が実装されていなかったPCにおいても、1つのアプリケーションでそれらのメモリを独占的に利用できたので十分な容量であったといえた。またメモリの拡張方法としてはアドレス空間そのものを拡張するため、[バンク切り換え](../Page/バンク切り換え.md "wikilink")処理とページフレームに出現しているメモリのページ管理が不要な分[EMSより高速でありメモリ管理に手間がかからない方法であった](../Page/Expanded_Memory_Specification.md "wikilink")。

DOSエクステンダは擬似OSと呼ばれMS-DOSを拡張するものである。プロテクトメモリの管理は独自に行うものの[ファイルシステム](../Page/ファイルシステム.md "wikilink")等はMS-DOSに依存する。そのため同時にオープン可能なファイル数はMS-DOSと変わるところは無いなど、MS-DOSの制限をかなり受けた。DOSエクステンダは、プロテクトモードアプリケーションからは、プロテクトメモリをサポートするMS-DOSのように見え、一方MS-DOSからは、DOSアプリケーションとして振舞う。つまりアプリケーションとOSの両方の性質をもったソフトウェアであった。

## DOSエクステンダの動作

[プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")アプリケーションがDOSエクステンダに対してファイルアクセスなどのファンクションコールを実行すると、DOSエクステンダはCPUを[リアルモード](https://ja.wikipedia.org/wiki/リアルモード "wikilink")（場合によっては[仮想86モード](../Page/仮想86モード.md "wikilink")）に切替えて、自身が受けたDOSエクステンダのファンクションコールをMS-DOSのファンクションコールに翻訳してMS-DOSを呼び出す。ファイルアクセスのような、大量のデータをMS-DOSとやり取りするファンクションコールのために、コンベンショナルメモリ上にリアルモードとプロテクトモード間のデータ通信用のバッファ領域が必要となることに注意しなくてはならない。なぜならMS-DOSは[プロテクトメモリ](https://ja.wikipedia.org/wiki/プロテクトメモリ "wikilink")を直接アクセスできないからである。

例えば、ファイル読み出しの場合には、MS-DOSのファンクションコールを利用して、このコンベンショナルメモリ上にある通信バッファ領域にデータを読み出した後、DOSエクステンダはCPUをプロテクトモードに切替えて、読み込んだデータを通信バッファからプロテクトメモリに転送する。この時データサイズが大きくて、一度に通信バッファに読込みきれない場合には、CPUを再びリアルモードに切替えて、残りのデータを通信バッファに読み出すように再度MS-DOSにファンクションコールを発行して、ファイルデータの残りの部分の読み出しを行う。そしてデータサイズが極めて大きい場合には、このリアルモードとプロテクトモードの交互切替えの繰返しによるファイル上のデータのプロテクトメモリへの読込を行う。

このように、アプリケーションの実行中に何度もプロテクトモードとリアルモードの切替えが行われることもDOSエクステンダの特徴の一つである。

DOSエクステンダ起動時のプロテクトモードアプリケーションのプロテクトメモリへの読み出しも、上記と同様のシーケンスを経て行われる。 アプリケーションをプロテクトメモリに全て読み込み終えると、DOSエクステンダはCPUをプロテクトモードに切替え、アプリケーションを実行する。

アプリケーションが終了すると、確保したプロテクトメモリを全て開放しCPUをリアルモードへ切替えて、DOSエクステンダはMS-DOSアプリケーションとして終了する。

## DOSエクステンダの機種依存部分

CPUを[リアルモード](https://ja.wikipedia.org/wiki/リアルモード "wikilink")から[プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")に切替えることはCPU単体で行えるが、DOSエクステンダというものは基本的に機種依存するソフトウェアである。一つの実行ファイルで複数の機種に対応したDOSエクステンダも存在するが、それは対応する機種分だけ機種依存コードを内部に持っているだけのことである。

以下にDOSエクステンダの機種依存部分について記す。

### プロテクトメモリ確保

DOSエクステンダは、その性質上、起動時にそのハードウェアで利用可能なプロテクトメモリを確保する必要があるが、MS-DOSは元来リアルモード用のOSであるために、直接プロテクトメモリを管理する機能を有していない。そのため、DOSエクステンダがプロテクトメモリを確保するためには、プロテクトメモリ管理用のデバイスドライバを用意する方法もあるが、基本的にはプロテクトメモリBIOSあるいはMS-DOSの拡張としてメーカーが用意した固有のファンクションコールを直接呼び出して、そのハードウェアで利用可能なプロテクトメモリを確保することになる。プロテクトメモリBIOSおよびメーカー固有のファンクションコールの仕様は、機種依存するので、DOSエクステンダが直接プロテクトメモリBIOSを呼び出すということは、DOSエクステンダが機種依存することになる。

### アドレスライン20(A20)制御

[80286や上位互換のCPUを搭載した](../Page/Intel_80286.md "wikilink")[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")や[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")では、[8086](../Page/Intel_8086.md "wikilink")/[88を搭載した旧機種との互換性を取るために](../Page/Intel_8088.md "wikilink")、起動直後はCPU周辺の回路によって外部に出力するアドレスライン20(A20)を強制的に0にしているが、プロテクトメモリを利用するためには、このアドレスライン20をCPUから出力されるアドレスに切り換える（A20オン）制御を行わなくてはならない。しかし、A20をオンにするためのI/Oポートアドレス等は機種によって異なるので、DOSエクステンダに限らずプロテクトメモリを利用するソフトウェアは基本的に機種依存することになる。

### 割り込み再配置

[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")系のCPUは、最初の8086がリリースされた時に、割り込みベクトル 0～ 0x1F をCPU例外用に予約されていたにもかかわらず、[IBM PC](../Page/IBM_PC.md "wikilink") や [PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")は、この予約領域の一部を BIOS やハードウェア割り込みの処理のために割り当ててしまった。そのため、[80286が開発されて例外が追加されると](../Page/Intel_80286.md "wikilink")、CPU例外とBIOSやハードウェア割り込みの割り込みベクトルが衝突するようになった。[80286以降のCPUで追加された例外は](../Page/Intel_80286.md "wikilink")、その殆どが[プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")に関連したものであった。そのため、リアルモードで処理をしている場合には、この衝突は殆ど問題にならなかったのだが、プロテクトモードでは割り込みベクトルの衝突が問題になった。そのため、プロテクトモードを利用するために、[割り込みコントローラの設定を変更して](../Page/Programmable_Interrupt_Controller.md "wikilink")、効率的にハードウェア割り込みのハンドリングを行うためにハードウェア割り込みの割り込みベクトルを変更する実装があった。この割り込みベクトルの変更処理を割り込み再配置という（BIOSもプロテクトモードで利用するためには、割り込みベクトルの再配置が必要だが、プロテクトモードからはBIOSを呼び出さないことにして衝突を回避する方法もある）。割り込みコントローラは、[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")も[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")も[FMRシリーズ](../Page/FMRシリーズ.md "wikilink")も[8259を使用していたが](../Page/Intel_8259.md "wikilink")、その接続しているI/Oアドレスが異なるために、割り込みベクトル再配置処理は機種依存する。よって、プロテクトモードを使用するために割り込み再配置処理が必要なので、DOSエクステンダは機種依存することになる。なおFMR/FM TOWNS シリーズは、予め割り込みベクトルが衝突しないように割り込みコントローラやBIOSの割り込みベクトルが割り当てられているので、割り込み再配置は必要ない。

割り込みの再配置は必須ではなく、あくまでも効率的にハードウェア割り込みを処理するための手段の一つである。実際には割り込みを管理する8259に対して割り込み要因の確認（ポール・ワードの読み出し）を行うことで、ハードウェア割り込みを再配置しなくとも、[割り込みハンドラ](https://ja.wikipedia.org/wiki/割り込みハンドラ "wikilink")はハードウェア割り込みなのかソフトウェア割り込み（フォルトおよびトラップ）なのかを認識することが可能である。

### 仮想記憶対応

32ビットDOSエクステンダは、標準またはオプションで[IA-32](../Page/IA-32.md "wikilink")のページング機能を利用した仮想記憶をサポートして、物理メモリより大きなメモリを利用可能にしている場合が多い。

仮想記憶により物理メモリより大きいメモリを利用出来るようにするためには、ページ不在が検出されて該当ページをディスクからロードする必要が起こった場合に、ディスクにスワップアウトするページを決定する必要があるが、スワップアウトするページとなる利用頻度の低いページを探すために、ページの利用状況の統計を取っておかねばならない。

この処理のためには、インターバルタイマーの割り込みハンドラを組み込む必要があるが、割り込みハンドラとその組込みプログラムは、機種毎にI/Oアドレスの異なる割り込みコントローラを制御する必要があるので、機種依存プログラムとなる。 そのため仮想記憶をサポートするDOSエクステンダは機種依存する。

### CPUリセット回路(16ビットDOSエクステンダの場合)

「DOSエクステンダの動作」の項で解説したように、DOSエクステンダはリアルモードとプロテクトモードを交互に切り換えながら動作する。ところが[80286は](../Page/Intel_80286.md "wikilink")、プロテクトモードからリアルモードに切り換える方法がCPUリセットしかない\[1\]ため、プロテクトモードからリアルモードへの切り換えが必要なプログラムのために[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")や[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")は、CPUのみをリセットする回路を装備していた。このCPUのみをリセットする回路は機種毎に異なっていたので、80286対応のDOSエクステンダ（当然16ビットDOSエクステンダとなる）のようなプロテクトモードからリアルモードへの切り換えが必要なプログラムは必然的に機種依存することとなった。また80286をリセットすると、アドレス 0FFFFF0hにジャンプするが、リアルモードに遷移後、処理をDOSエクステンダに戻すためには、この領域にあるプログラム（プロテクトモードBIOSの一種）の助けを必要とするが、BIOSの仕様も機種によって異なるということに注意が必要である。つまり32ビットよりも16ビットDOSエクステンダの方がPC/AT互換機対応版から他機種への移植の手間が多かったのである。なお、PC/AT互換機対応の16ビットDOSエクステンダをPC-9800シリーズ等に移植する場合に、移植作業の手間を少しでも減らすために、サポートするCPUを[386以上に限定することにより](../Page/Intel_80386.md "wikilink")、CPUリセット回路の制御とCPUリセットBIOSに関する移植を回避しているケースもあった。

## 著名なDOSエクステンダの一覧

  - 286|DOS-Extender (RUN286)、386|DOS-Extender (RUN386)、TNT|DOS-Extender（PharLap Softwareが開発）

特にFM TOWNSはMS-DOS上でRUN386を介してOSが動作しており、[富士通](../Page/富士通.md "wikilink")から提供されていた開発ツールもエクステンダ用アプリケーションの開発を念頭に置かれていた。そのような環境であったため、市販アプリケーションや[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")の大多数がエクステンダ用プログラムであった点は、特筆に値する。

  - EXE286、EXE386（京都マイクロコンピュータが開発、販売版と非営利版が存在、[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")用、PC/AT互換機用、[FMRシリーズ](../Page/FMRシリーズ.md "wikilink")・FM TOWNS用が存在。286・386|DOS-Extender互換）

これ以外にも286・386|DOS-Extender互換のDOSエクステンダは多数存在する。

  - OS/286、OS/386（ERGOが開発）
  - DOS/16M、DOS4G（Rational Systemsが開発）
  - NDP-RUN (MicroWay社、NDPコンパイラシリーズ (Ver.4以降)にバンドルされていた。ERGO 社の OS/386ベースで .LTL 形式という独自のファイルフォーマットをサポート)
  - GO32（[フリーウェア](../Page/フリーウェア.md "wikilink")）
  - CauseWay（Watcom C/C++に付属、現在は[PDSとして公開されている](../Page/パブリックドメインソフトウェア.md "wikilink")）
  - WDOSX (Michael Tippach作) Win32 APIエミュレーション機能を搭載したDOSエクステンダで2005年まで開発が行われていた。

## 主な32ビットDOSエクステンダ対応開発ツール

  - 386ASM/386LINK (PharLap Software社) - FM TOWNS用以外は、386|DOS-Extender SDK (日本国内では 386TOOLBOXという商品名で販売)にバンドルされていた
  - 386|VMM (PharLap Software社) - 386|DOS-Extender 又は TNT|DOS-Extender (Ver.6以降) のオプションツールで、これらのDOSエクステンダと共に使用することにより、MS-DOS 上で 32ビット仮想記憶環境を構築する仮想記憶マネージャ
  - HIGH-C386、HIGH C/C++ (MetaWare社) FM TOWNSの標準Cコンパイラであり、富士通から様々なライブラリが提供されていた。
  - WATCOM C (WATCOM社)
  - NDP-Fortran386、NDP-C/C++、NDP-PASCAL (MicroWay社)
  - Lahey Fortran (Lahey社)
  - WIN32 SDK Cコンパイラ (Microsoft社) - WIN32 SDKに付属の32ビットCコンパイラ (MS-C Ver.8.0 32ビット版に相当する)。 PharLap社のTNT|DOS-Extenderを使用することで、TNT|DOS-Extender用のアプリケーションを開発することが出来た。
  - SoftProbe 386X (SSI社) - HIGH C386対応のソースコードデバッガ。[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")版が存在した。[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")対応版は MetaWare社にOEM供給され、MetaWare Debuggerという名称でHIGH Cコンパイラにバンドルされていた。
  - GO32上で動く[GNU Cコンパイラ(GCC)としてdjgppが存在する](../Page/GNUコンパイラコレクション.md "wikilink")。またこれとは別に386|DOS-Extender・EXE386にも移植された。
  - Rapid Deployment Softrware Euphoria Version.3.1 マルチプラットホームスクリプト言語でDOSエクステンダとしてCauseWayを使用している。またC言語ソースも出力が可能。
  - XSCompiler

## 脚注

## 参考文献

  - 『MS-DOSメモリ管理ソフト技法-メモリ常駐ソフト&拡張メモリ活用プログラミング』（CQ出版、1990年）, ISBN 978-4-7898-3484-1
  - 「インターフェース 1990年9月号」（CQ出版）
  - 「インターフェース 1993年10月号」（CQ出版）
  - [Duncan, Ray](https://ja.wikipedia.org/wiki/Duncan,_Ray "wikilink") (1992). *Extending-DOS*:A Programmer's Guide to Protected-Mode DOS (Addison-Wesley), ISBN 0-201-56798-9

## 関連項目

  - [MS-DOS](../Page/MS-DOS.md "wikilink")
  - [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")
  - [DPMI](../Page/DPMI.md "wikilink") (DOS Protected Mode Interface)
  - [VCPI](../Page/VCPI.md "wikilink") (Virtual Control Program Interface)
  - [EMS](../Page/Expanded_Memory_Specification.md "wikilink") (Expanded Memory Specification)
  - [XMS](../Page/XMS.md "wikilink") (Extended Memory Specification)
  - [DESQview](../Page/DESQview.md "wikilink")

[Category:メモリ管理](https://ja.wikipedia.org/wiki/Category:メモリ管理 "wikilink") [Category:MS-DOS](https://ja.wikipedia.org/wiki/Category:MS-DOS "wikilink")

1.  80286では、非公開の[LOADALL](https://ja.wikipedia.org/wiki/LOADALL "wikilink")命令を使用しても、プロテクトモードからリアルモードへ戻ることはできない。