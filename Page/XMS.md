> この記事は[XMS](https://ja.wikipedia.org/wiki/XMS)から翻訳されています。


**XMS** (**eXtended Memory Specification**) は、[MS-DOS](../Page/MS-DOS.md "wikilink")上での[メモリ拡張規格のひとつ](../Page/記憶装置.md "wikilink")。XMS自身はMS-DOSバージョン3.0以上を動作対象とする。MS-DOSバージョン5.0以降から**公式に**サポートが開始され、MS-DOSのパッケージにXMS[ドライバが付属し](../Page/デバイスドライバ.md "wikilink")、MS-DOS自体もXMSを用いるようになった。

それ以前のバージョンのMS-DOSにおいては、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が一部の製品に添付していたドライバ、あるいはフリーウェアや[サードパーティー](../Page/サードパーティー.md "wikilink")製のドライバを用いることでXMSを使用することができた。また、MS-DOSバージョン5.0以降であっても、標準添付のXMSドライバではなく[フリーウェア](../Page/フリーウェア.md "wikilink")やサードパーティー製のドライバ、あるいはマイクロソフトの一部製品に添付されていたより新しいXMSドライバを用いることが可能で、機能や速度などで標準ドライバに勝るものを使用することが多かった。

## 基本概念

[サムネイルの場合](https://ja.wikipedia.org/wiki/ファイル:PC_DOS_memory_map_ja.svg "wikilink")）\]\] XMSは、次の3つのメモリ領域の規格からなる。

  - 100000h – 10FFEFhの64キロバイト弱を使用する**HMA** (High Memory Area)
  - 10FFF0h以降のメモリ領域を使用する**EMB** (Extended Memory Block)。このメモリ領域の内容は、XMSドライバの助けを借りてコンベンショナルメモリ（MS-DOSが管理するメモリ領域）間とブロック転送できる
  - [BIOS](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")・[VRAM](../Page/VRAM.md "wikilink")等が用いるA0000h（アーキテクチャにより異なる）– FFFFFhの、空き領域にRAMを出現させる**UMB**（Upper Memory Blocks、上位メモリとも言う）

XMSは、これら3規格の総称であるが、「XMSメモリを使うプログラム」などといった文脈で使う場合は、EMBを指す場合も多い。ただし、XMS ver.1はHMAの規格であり、 ver.2でEMBとUMBが追加され、 ver.3でEMBが64MB以上のメモリに対応し、UMBも1個機能が追加された。

なお、XMSという用語はメモリ領域を指す言葉の他に、それらの領域を管理するファンクションコールを意味する言葉としても使用された。例えば「このメモリマネージャーは、EMSの他、XMSもサポートする」のように使用された場合には、ファンクションコールを意味する。

またHMAとEMBに関するファンクションコールを提供するデバイスドライバは、[プロテクトメモリ](https://ja.wikipedia.org/wiki/プロテクトメモリ "wikilink")BIOS等の機種依存部分を吸収する役割も担っていた。*XMSドライバ が提供するHMA*とEMB*ファンクションコールを利用するお陰で、Windows 3.xは、*プロテクトメモリBIOSの直接呼出し等と、*A20ラインのハードウェア制御という機種依存処理を回避することが出来た。*。

## HMA

[8086では](../Page/Intel_8086.md "wikilink")、[セグメントとオフセットという](../Page/セグメント方式.md "wikilink")2つの16ビット値を用いてメモリ管理を行っている（これは[8080等との互換性を考慮した結果の設計である](../Page/Intel_8080.md "wikilink")）。MS-DOSにおけるメモリ管理も、このセグメント単位で行っている。参照する実メモリはセグメント×10h + オフセットとなる。

上記の理由から、286以降のCPUを使用しているコンピュータで、アドレスライン20以上のアドレスバスを有効にした後（8086との互換性のため、初期状態では電気的に無効になっている。なお、このアドレスライン20制御は機種依存する）、セグメントレジスタにFFFFhを指定すると、アクセスする[実アドレスはFFFF](https://ja.wikipedia.org/wiki/物理アドレス "wikilink")0h – 10FFEFhとなる。すなわち、セグメント＋オフセットという8086・MS-DOSのメモリ管理の枠内で、65520バイトのメモリが余分に扱えることになる。この領域をHMAと呼ぶ。

  -
    セグメント FFFFh:オフセット 0000h = FFFF0h + 0000h = FFFF0h（8086などでも可）
    セグメント FFFFh:オフセット 0010h = FFFF0h + 0010h = 100000h
    セグメント FFFFh:オフセット FFFFh = FFFF0h + FFFFh = 10FFEFh

HMAの使用には、アドレスバスが21ビット以上の(アドレスライン20がある)[80286以降のCPUと](../Page/Intel_80286.md "wikilink")1メガバイト超のメモリが必要である。

基本的には排他的な利用となり、Windows/286（日本ではWindows 2.1x）かMS-DOS 5.0以降が占有する。DOS 5.0以降に関してはDOSカーネル、ディスクバッファ、また一部のユーティリティ（display.sysなど）で利用する。変わったところでは、[ATOK](../Page/ATOK.md "wikilink")7の後期バージョンでHMAを使用するバージョン (ATOK7H) があった。

多くのEMSドライバが使用する仮想86モード環境下においては、一般に仮想86モニタ（プロテクトモードで稼動するプログラム）が上位メモリに存在するため、ハードウェア的にはアドレスの20ビットマスクを常に行わずに、該当する中間線形アドレスに対応するページのメモリアドレスを置き換えることでエミュレーションする対応を行っていた。

## EMB

[80286以降のCPUの](../Page/Intel_80286.md "wikilink")[プロテクトメモリ](https://ja.wikipedia.org/wiki/プロテクトメモリ "wikilink")領域の内、HMAより上位の10FFF0h以降のメモリ領域をEMBと呼ぶ。

XMSドライバは、EMBに関してメモリ領域の空メモリサイズの取得、EMBの割当、解放、ロック、アンロック等のファンクションコールを提供するので、[DOSエクステンダ](https://ja.wikipedia.org/wiki/DOSエクステンダ "wikilink")やWindows 3.x のスタンダードモード・エンハンストモード等、プロテクトモードを使用できるプログラムは、XMSドライバのファンクションコールを利用すれば、機種依存する処理を記述することなくプロテクトメモリを利用できた。

EMB領域はプロテクトモードでないとアクセスできないので、一般のMS-DOSアプリケーションは直接アクセスできないが、XMSドライバは、EMB同士またはEMBと任意のコンベンショナルメモリ領域とのブロック転送を行うファンクションコールも提供したので、[リアルモード](https://ja.wikipedia.org/wiki/リアルモード "wikilink")専用のプログラムでもXMSドライバを使用すれば、EMB領域を利用できた。

## UMB

BIOS・VRAM等が用いる、A0000h – FFFFFh（[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")や[PC-98ノーマルモードの場合](../Page/PC-9800シリーズ.md "wikilink")。[PC-98ハイレゾリューションモードや](https://ja.wikipedia.org/wiki/PC-9800シリーズ#高解像度（ハイレゾ）系 "wikilink")[FMR](../Page/FMRシリーズ.md "wikilink")・[FM TOWNSの場合はC](../Page/FM_TOWNS.md "wikilink")0000h – FFFFFh）の空き領域にRAMを割り当てて利用するもの。

このメモリ空間は1メガバイト以内に収まっていることから、リアルモードおよび仮想86モードにおいて通常通りにアクセスすることができるため、デバイスドライバの読込用やソフトの実行・常駐用等に使用できる。MS-DOSバージョン5.0以降であればMS-DOS標準付属の仮想メモリマネージャ ([EMM386.EXE](https://ja.wikipedia.org/wiki/EMM386.EXE "wikilink")) がUMBを含むメモリ管理を統合しており、文字通りCPUが80386以降の場合に限られるものの、MS-DOSの機能としてUMBを用いることができる。それ以前のバージョンのMS-DOSもしくはCPUが80286以前の場合は、それぞれのプログラムがXMSファンクションを用いて明示的にUMBを使用するか、UMBに読み込むための専用のプログラムを用いることが必要であった。

UMBの実装にはチップセットや専用のRAMボードの機能を使ってハードウェア的にRAMを出現させるものと、80386以降の[仮想86モード](https://ja.wikipedia.org/wiki/仮想86モード "wikilink")を使って、仮想メモリマネージャ（EMM386.EXE等）がメモリを割り当てるものがある。

前者はCPUが80386以降である必要性は無い（XMSが80286以降を前提とするが、ハードウエア的な手法でRAMを出現させる形であれば8086/8088などでもUMBが使えるようになるドライバもある）。

  - [UMBPCI - a hardware UMB driver for DOS and Win95](http://www.uwe-sieber.de/umbpci_e.html) (英文 PC/AT互換機用)
  - [擬似UMBドライバ](http://www.vector.co.jp/soft/dos/hardware/se010042.html) (Vectorライブラリ PC-98用)

など。

## よく使われたドライバ

  - MS-DOS・Windows 9xのHIMEM.SYS（EMB, HMA担当） +EMM386.EXE （UMB, EMS担当、386以降）
  - [メルコのMELEMM](../Page/バッファロー_\(パソコン周辺機器\).md "wikilink").SYS（XMS+EMS担当、386以降）
  - [I・O DATAのVMM](../Page/アイ・オー・データ機器.md "wikilink")386.EXE （XMS+EMS担当、386以降）
  - [Quarterdeck](https://ja.wikipedia.org/wiki/:en:Quarterdeck "wikilink")（[シマンテック](../Page/シマンテック.md "wikilink")に吸収）の[QEMM](../Page/QEMM.md "wikilink")
  - ZOBplus Hayami（速水祐）の個人開発によるXMZ（EMB, HMA担当、286以降）ソースコード添付
  - taQの個人開発によるtdpmi（DPMI+XMS+EMS担当、386以降）※別途XMSドライバが必要
  - K.Ogino（荻野晃史）の個人開発によるVEM486（XMS+EMS担当、386以降）

## 関連項目

  - [MS-DOS](../Page/MS-DOS.md "wikilink")
  - [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")
  - [DOSエクステンダ](https://ja.wikipedia.org/wiki/DOSエクステンダ "wikilink")
  - [DPMI](../Page/DPMI.md "wikilink") (DOS Protected Mode Interface)
  - [VCPI](../Page/VCPI.md "wikilink") (Virtual Control Program Interface)
  - [Expanded Memory Specification](../Page/Expanded_Memory_Specification.md "wikilink") (EMS)
  - [プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")

## 参考文献

  - 『MS-DOSメモリ管理ソフト技法-メモリ常駐ソフト＆拡張メモリ活用プログラミング』(CQ出版、1990年), ISBN 978-4789834841
  - 「インターフェース 1990年9月号」(CQ出版)
  - 「インターフェース 1993年10月号」(CQ出版)
  - [Duncan, Ray](https://ja.wikipedia.org/wiki/Duncan,_Ray "wikilink") (1992). *Extending-DOS*:A Programmer's Guide to Protected-Mode DOS (Addison-Wesley), ISBN 978-0-201-56798-4

## 外部リンク

  - [Windows 3.1のメモリ制限](http://support.microsoft.com/kb/84388/en-us) - Windows 3.xのスタンダード・モード/エンハンスト・モードとXMSの関連が記述されたページの一例。

[Category:メモリ管理](https://ja.wikipedia.org/wiki/Category:メモリ管理 "wikilink") [Category:MS-DOS](https://ja.wikipedia.org/wiki/Category:MS-DOS "wikilink")