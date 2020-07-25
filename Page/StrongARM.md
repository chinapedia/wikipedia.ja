> この記事は[StrongARM](https://ja.wikipedia.org/wiki/StrongARM)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:DEC_StrongARM.jpg "wikilink") **StrongARM**（ストロングアーム）は、[ARM V4](../Page/ARMアーキテクチャ.md "wikilink") [命令セット](../Page/命令セット.md "wikilink")アーキテクチャ (ISA) に基づいて[DECが開発した](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")ファミリである。後に[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")へ売却され、最終的には[XScale](../Page/XScale.md "wikilink")に取って代わられた。

## 歴史

StrongARMは [ARMと](https://ja.wikipedia.org/wiki/ARMホールディングス "wikilink")[DECの共同プロジェクトとして](https://ja.wikipedia.org/wiki/デジタル・イクイップメント・コーポレーション "wikilink")、既存のARMシリーズよりも高速な[CPU](../Page/CPU.md "wikilink")(ただし完全互換ではない)を開発することから始まった。StrongARMは低消費電力の組み込み市場の中でも従来のARMシリーズでは性能が足りなかった[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")市場を目指して設計された。ターゲットは[PDAや](../Page/携帯情報端末.md "wikilink")[セットトップボックス](../Page/セットトップボックス.md "wikilink")である\[1\]\[2\]。

DECは[マサチューセッツ州](../Page/マサチューセッツ州.md "wikilink")を[半導体](../Page/半導体.md "wikilink")部門の拠点としていたが、[シリコンバレー](../Page/シリコンバレー.md "wikilink")の才能ある人材を獲得しやすくするためカリフォルニア州[パロアルトにデザインセンターを開設した](../Page/パロアルト_\(カリフォルニア州\).md "wikilink")。ここがStrongARMプロジェクトの拠点となった。また、DECから[アップルや](../Page/アップル_\(企業\).md "wikilink")[モトローラ](../Page/モトローラ.md "wikilink")に一旦移籍して戻った技術者らが作ったテキサス州[オースティンの設計拠点もプロジェクトに関わっている](../Page/オースティン_\(テキサス州\).md "wikilink")。プロジェクトは1995年に始まり、まもなく最初の設計である **SA-110** が完成した。

訴訟問題の結果として[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")、DECの StrongARM を含む半導体部門は後に[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")に売却された\[3\]。インテルは不振だった同社の[RISC](../Page/RISC.md "wikilink")プロセッサ([i860](../Page/Intel_i860.md "wikilink"), [i960](../Page/Intel_i960.md "wikilink"))の代わりにStrongARMを使った。[2000年](../Page/2000年.md "wikilink")、その設計はインテルの[XScale](../Page/XScale.md "wikilink")に取って代わられた。なお、そのXScaleも[2006年](../Page/2006年.md "wikilink")に[マーベル・テクノロジー・グループ](https://ja.wikipedia.org/wiki/マーベル・テクノロジー・グループ "wikilink")に売却された。

DECの半導体部門がインテルに売却された際、パロアルトの技術者の多くは[MIPSアーキテクチャ](../Page/MIPSアーキテクチャ.md "wikilink")の通信向け [System-on-a-chip](../Page/System-on-a-chip.md "wikilink") (SoC) を設計していた[ベンチャー](../Page/ベンチャー.md "wikilink") SiByte（後に[ブロードコム](../Page/ブロードコム.md "wikilink")が買収）へ移籍した。オースティンの設計グループもMIPSの携帯機器向け SoC を設計するベンチャー Alchemy Semiconductor に参加した。

## SA-110

SA-110は StrongARM ファミリの最初の[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")である。当初 100MHz、160MHz、200MHz で動作するバージョンが1996年2月5日に発表された\[4\]。発表時点でサンプルが用意されていたが、量産品が出荷されたのは1996年中ごろである。より高速な166MHz版と233MHz版が1996年9月12日に発表された\[5\]。こちらも発表時点でサンプルが用意されており、量産品は1996年12月に出荷となった。1996年時点で、携帯機器向けマイクロプロセッサではSA-110が最高性能を誇っていた\[6\]。SA-110は[アップル・ニュートン](../Page/アップル・ニュートン.md "wikilink")の後期に発表された**メッセージパッド2000/2100**で採用され\[7\]、他にも[エイコーン社の](../Page/エイコーン・コンピュータ.md "wikilink")[Risc PCなど多数の製品で使われた](../Page/Risc_PC.md "wikilink")。SA-110は、[Daniel W. Dobberpuhl](https://ja.wikipedia.org/wiki/:en:Daniel_W._Dobberpuhl "wikilink")、Gregory W. Hoeppner、Liam Madden、Richard T. Witek らが設計した\[8\]。

### 詳細

SA-110の[マイクロアーキテクチャ](../Page/マイクロアーキテクチャ.md "wikilink")は単純である。[スカラー設計であり](https://ja.wikipedia.org/wiki/スカラー計算機 "wikilink")、5段の典型的な[命令パイプライン](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")で命令を[イン・オーダー実行する](../Page/アウト・オブ・オーダー実行.md "wikilink")。内部は、IBOX, EBOX, IMMU, DMMU, BIU, WB, PLL というブロックで構成されている。IBOXはパイプラインの最初の2段を処理するブロックで、命令をフェッチし、デコードし、発行する。命令フェッチは1段目で行われ、デコードと発行は2段目で行われる。ARM命令セットには単純に実行できない複雑な命令もあり、IBOXではそれを単純な命令の列に変換する。IBOXは分岐命令も扱う。SA-110には[分岐予測](../Page/分岐予測.md "wikilink")機能はないが、分岐命令自体が高速に処理される。

命令の実行は3段目から開始される。このステージはEBOXで処理され、その中に[レジスタファイル](https://ja.wikipedia.org/wiki/レジスタファイル "wikilink")、[ALU](https://ja.wikipedia.org/wiki/演算論理装置 "wikilink")、[バレルシフタ](../Page/バレルシフタ.md "wikilink")、[乗算器](../Page/乗算器.md "wikilink")、条件処理ロジックなどが含まれる。レジスタファイルには3つのリードポートと2つのライトポートがある。ALUとバレルシフタは1サイクルで命令を実行する。乗算器はパイプライン化されておらず、実行には複数サイクルを要する。

IMMUとDMMUはそれぞれ、命令とデータの[メモリ管理ユニット](../Page/メモリ管理ユニット.md "wikilink")である。各MMUには32エントリのフルアソシアティブ[TLBがあり](../Page/トランスレーション・ルックアサイド・バッファ.md "wikilink")、1エントリで4KB、64KB、1MBのいずれかをマッピングできる（可変ページサイズ）。ライトバッファ (WB) は1エントリ16バイトで8エントリある。それによってストア動作をパイプライン化できる。バスインタフェースユニット (BIU) はSA-110と外部とのインタフェースである。

[PLLは外部から供給される](../Page/位相同期回路.md "wikilink")3.68MHzのクロック信号から内部[クロック](../Page/クロック.md "wikilink")信号を生成する。これはDECが設計したものではなく、スイスの[ヌーシャテル](../Page/ヌーシャテル.md "wikilink")にある Centre Suisse d'Electronique et de Microtechnique (CSEM) が設計を請け負った。

命令[キャッシュとデータキャッシュはそれぞれ](../Page/キャッシュメモリ.md "wikilink")16KBで、32ウェイ・セットアソシアティブで仮想インデックスである。StrongARMは遅い（それゆえに単純で安価な）メモリと使うことを念頭に設計されている。したがって、セットアソシアティブ数を高くすることでキャッシュヒット率を実現し、仮想インデックスにすることでキャッシュを通すメモリアクセスとキャッシュを通さないメモリアクセスを同時に扱えるようにしている。キャッシュはトランジスタ数を多く費やすため、ダイの半分をキャッシュで占めている。

SA-110は250万個のトランジスタを集積しており、大きさは 7.8mm×6.4mm (49.92mm<sup>2</sup>) である。DECがマサチューセッツ州ハドソンにある[ファブ](../Page/ファウンドリ.md "wikilink")-6で、同社独自の CMOS-6 プロセスで製造した。CMOS-6 はDECの第6世代[CMOS](../Page/CMOS.md "wikilink")プロセスで、機能サイズ0.35μm、実効チャネル長0.25μmだが、SA-110ではアルミニウム配線層を3層しか使っていない。電源電圧は1.2Vから2.2Vの可変であり、電力消費量と性能のバランスを調整できるようになっている（電圧が高いほど高周波数で駆動できる）。パッケージは144ピンの薄型[QFP](https://ja.wikipedia.org/wiki/QFP "wikilink") (TQFP) である。

## SA-1100

SA-1100はSA-110の派生品でDECが開発した。1997年発表。PDAをターゲットとしており、SA-110との違いはそういった市場にふさわしい機能を組み込んだ点である。データキャッシュの大きさは8KBに減らしている。

追加機能としては、メモリコントローラ、[PCMCIAコントローラ](../Page/PCカード.md "wikilink")、カラーLCDコントローラをダイ上のシステムバスに接続する形で内蔵し、システムバスに接続した周辺バスにシリアルI/Oチャネルを5つ装備した。メモリコントローラは、[FPM](https://ja.wikipedia.org/wiki/FPM_DRAM "wikilink")、[EDO DRAM](https://ja.wikipedia.org/wiki/EDO_DRAM "wikilink")、[SRAM](../Page/Static_Random_Access_Memory.md "wikilink")、[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")、ROMをサポートしている。PCMCIAコントローラは2スロットをサポートしている。メモリアドレスおよびデータバスはPCMCIAインタフェースと共有される。シリアルI/Oチャネルはスレーブ側USBインタフェース、[SDLC](https://ja.wikipedia.org/wiki/Synchronous_Data_Link_Control "wikilink")、[UART](../Page/UART.md "wikilink")×2、[IrDA](../Page/IrDA.md "wikilink")インタフェース、MCP、同期シリアルポートを実装している。

SA-1100には周辺チップであるSA-1101があり、インテルが1998年10月7日にリリースした\[9\]。SA-1101は、SA-1100に内蔵された周辺回路を補う周辺機能を提供するもので、ビデオ出力ポート、[PS/2ポート](https://ja.wikipedia.org/wiki/PS/2コネクタ "wikilink")×2、SA-1100上のものを置換するUSBコントローラとPCMCIAコントローラがある。このデバイスの設計はDECが始めたが、インテルが取得した際には完了しておらず、インテルが設計を引き継いで完成させた。DECから引き継いだハドソン工場で製造している。

SA-11000は250万個のトランジスタを集積し、大きさは8.24mm×9.12mm (75.15 mm<sup>2</sup>) である。0.35 μm CMOSプロセスで、アルミニウム配線層は3層であり、208ピンTQFPPでパッケージされている\[10\]。

## SA-1110

SA-1110はSA-110からの派生品で、インテルが開発した。[1999年](../Page/1999年.md "wikilink")[3月31日](../Page/3月31日.md "wikilink")、SA-1100の代替品として発表された\[11\]。発表では、サンプル出荷を1999年6月、量産出荷を同年末としていた。SA-1110は2003年初めごろまで販売された\[12\]。133MHz版と206MHz版がある。SA-1100との違いは、66MHz（133MHz版）または103MHz（206MHz版）の[SDRAM](../Page/SDRAM.md "wikilink")をサポートした点である。周辺チップとしてSA-1111もリリース。SA-1110は256ピンのMBGAでパッケージされている。携帯電話、PDA（コンパック [iPAQ](https://ja.wikipedia.org/wiki/iPAQ "wikilink")、HP Jornada、シャープ SL-5x00）、[シンピュータ](../Page/シンピュータ.md "wikilink")などに採用された。

## SA-1500

SA-1500はSA-110の派生品で、DECが[セットトップボックス](../Page/セットトップボックス.md "wikilink")向けに開発した\[13\]\[14\]。DECが設計し少量だけ生産したが、インテルでは生産しなかった。200から300MHzで駆動できる。SA-110に対する改良点は、*Attached Media Processor* (AMP) と呼ばれる[コプロセッサ](../Page/コプロセッサ.md "wikilink")とSDRAMおよびI/Oバスのコントローラを内蔵した点である。SDRAMコントローラは100MHzのSDRAMをサポートし、I/Oコントローラは最高50MHzで動作する32ビットI/Oバスを実装し、各種周辺機器や周辺チップ SA-1501 を接続できる。

AMPはマルチメディア向けに設計された命令を実装しており、整数および浮動小数点数の[積和演算](../Page/積和演算.md "wikilink")や[SIMD](../Page/SIMD.md "wikilink")演算を行う。命令語長は64ビットで、演算命令以外に分岐命令やロード/ストア命令もある。36ビット64本のレジスタファイルと一連の制御レジスタがある。SA-110コアとはチップ上のバスでやりとりし、データキャッシュを共有している。AMPにはALU、シフタ、分岐ユニット、ロード/ストアユニット、積和ユニット、[単精度](https://ja.wikipedia.org/wiki/単精度 "wikilink")[FPU](../Page/FPU.md "wikilink")が含まれる。また、AMPには書き換え可能な512エントリの[コントロールストア](../Page/コントロールストア.md "wikilink")があり、ユーザー定義命令をサポート可能である。

周辺チップのSA-1501は動画・音声処理機能とPS/2ポート、パラレルポートなど各種周辺機器を接続可能なI/O機能を有する。

SA-1500は330万個のトランジスタを集積しており、チップ面積は 60 mm<sup>2</sup> である。0.28 µm CMOS プロセスで製造されている。内部ロジックは1.5から2.0Vで駆動し、I/Oは3.3V。消費電力は100MHzで0.5W、300MHzで2.5Wである。240ピン[MQFPまたは](https://ja.wikipedia.org/wiki/QFP "wikilink")256ピンPBGAでパッケージされている。

## 脚注・出典

## 参考文献

  - "StrongARM-1500 Grapples With MPEG-2". (8 December 1997). *Microprocessor Report*.
  - Halfhill, Tom R. (19 April 1999). "Intel Flexes StrongArm With New Chips". *Microprocessor Report*.
  - Litch, Tim; Slaton, Jeff (March/April) 1998). "StrongARMing Portable Communications". *IEEE Micro*. pp. 48–55.
  - Santhanam, S. et al. (November 1998). "A low-cost, 300-MHz, RISC CPU with attached media processor". *IEEE Journal of Solid-State Circuits*, vol. 33, no. 11. pp. 1829–1839.
  - Turley, Jim (13 November 1995). "StrongArm Punches Up ARM Performance". *Microprocessor Report*.
  - Turley, Jim (15 September 1997). "SA-1100 Puts PDA on a Chip". *Microprocessor Report*.
  - Witek, Rich; Montanaro, James (1996). "StrongARM: A high-performance ARM processor". *Proceedings of COMPCON '96*, pp. 188–191.

[Category:ARMアーキテクチャ](https://ja.wikipedia.org/wiki/Category:ARMアーキテクチャ "wikilink") [Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink") [Category:ディジタル・イクイップメント・コーポレーション](https://ja.wikipedia.org/wiki/Category:ディジタル・イクイップメント・コーポレーション "wikilink")

1.  Montanaro, James et al. (1997). ["A 160-MHz, 32-b, 0.5-W CMOS RISC Microprocessor"](http://www.hpl.hp.com/hpjournal/dtj/vol9num1/vol9num1art5.pdf). *Digital Technical Journal*, vol. 9, no. 1. pp. 49–62.
2.
3.
4.  Digital Equipment Corporation (5 February 1996). "Digital Targets Supercharged StrongARM Chip At Consumer Electronics Market". Press release.
5.  Digital Equipment Corporation (12 September 1996). "Digital's StrongARM Chips Pull Away in Embedded Race". Press release.
6.  Turley, Jim (27 January 1997). "Embedded Vendors Seek Differentiation". *Microprocessor Report*, pp. 16–21.
7.  Turley, Jim (18 November 1996). "Newton First Design Win for StrongARM". *Microprocessor Report*, p. 5.
8.
9.  Intel Corporation (7 October 1998). "Intel Introduces StrongARM Products for PC Companions". Press release.
10. Stephany, R. et al. (1998). "A 200MHz 32b 0.5W CMOS RISC Microprocessor". *ISSCC Digest of Technical Papers*, pp. 238–239, 443.
11. Intel Corporation (31 March 1999). "Intel StrongARM Processor, Companion Chip Optimized For Handheld Computing Devices". Press release.
12. Martyn Williams (14 February 2003). "Intel puts StrongArm on death row". InfoWorld.
13. Rick Boyd-Merrit; Peter Clarke (24 July 1998). ["Intel to reveal details on StrongARM chip"](http://www.eetimes.com/news/98/1018news/strongarm.html). EE Times.
14. Prashant P. Gandhi (18 August 1998). ["SA-1500: A 300 MHz RISC CPU with Attached Media Processor"](http://www.hotchips.org/archives/hc10/3_Tue/HC10.S8/HC10.8.3.pdf). Hot Chips 10.