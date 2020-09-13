> この記事は[DECstation](https://ja.wikipedia.org/wiki/DECstation)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:DECstation-5000-200-hdr-0a.jpg "wikilink")

**DECstation**は、[DECのコンピュータのブランド名であり](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")、3つの独立したコンピュータシリーズで使用された名称である。第一は1978年にリリースされた[ワードプロセッサ](../Page/ワードプロセッサ.md "wikilink")システムで、その他は（こちらの方が有名だが）1989年に2種類のシリーズとしてリリースされた。後者は[MIPSアーキテクチャ](../Page/MIPSアーキテクチャ.md "wikilink")ベースの[ワークステーション](../Page/ワークステーション.md "wikilink")と[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")である。MIPSベースのワークステーションではDEC自身の[UNIX](../Page/UNIX.md "wikilink")である[Ultrix](../Page/Ultrix.md "wikilink")および[OSF/1](../Page/Tru64_UNIX.md "wikilink")（1992年1月から）が動作した。

## DECstation 78

最初にDECstationの名前を与えられたコンピュータシステムは[PDP-8](../Page/PDP-8.md "wikilink")をベースとしたワードプロセッサであった。これはVT52[端末](../Page/端末.md "wikilink")に組み込まれたもので、**VT78**という名称でも知られている。

## DECstation RISC ワークステーション

### 歴史

第二のシリーズは[1989年](../Page/1989年.md "wikilink")1月11日、DECstation 3100 から始まった。DECが初めて商用化した[RISC](../Page/RISC.md "wikilink")ベースのコンピュータである\[1\]。

このファミリは、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")のRISCベースのUNIXマシンに対抗できる安価で高性能なコンピュータを開発するというPMAXプロジェクトから生まれた。[James Billmaier](https://ja.wikipedia.org/wiki/:en:James_Billmaier "wikilink")、Mario Pagliaro、[Armando Stettner](https://ja.wikipedia.org/wiki/:en:Armando_Stettner "wikilink")、Joseph DiNucci らが開発したもので、全くの[CISC](../Page/CISC.md "wikilink")である[VAX](../Page/VAX.md "wikilink")や開発中だったアーキテクチャに比べると、真の[RISC](../Page/RISC.md "wikilink")アーキテクチャと言える。当時、DECは成功を収めた[PDPシリーズ](../Page/PDPシリーズ.md "wikilink")や[VAX](../Page/VAX.md "wikilink")シリーズなどの[CISC](../Page/CISC.md "wikilink")システムでよく知られていた。

[インテルや](../Page/Intel_i860.md "wikilink")[モトローラなどのRISCも採用が検討されたが](../Page/MC88000.md "wikilink")、[MIPSが選ばれるのに時間はかからなかった](../Page/MIPSアーキテクチャ.md "wikilink")。MIPSのマイクロプロセッサは[リトルエンディアンとビッグエンディアンの両方をサポートしていた](https://ja.wikipedia.org/wiki/エンディアン "wikilink")（ハードウェアリセット時に設定）。VAXや成長の著しい[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")がリトルエンディアンであることを考慮し、このファミリでもリトルエンディアンを選択している\[2\]。

VAX（とその後の[Alphaアーキテクチャ](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")）とは異なり、[UNIX](../Page/UNIX.md "wikilink")専用に設計されており、[VMS](../Page/OpenVMS.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")が DECstation 用にリリースされることはなかった。当時、プロジェクト開始に当たって、DEC発祥でないアーキテクチャで他社と競い成長していくことができるかという問題が議論された\[3\]。後にDECは自社開発の[Alphaアーキテクチャに乗り換えてMIPSベースのファミリを廃止するが](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")、その際に本ファミリ開発に肯定的だった人々がDECを離れている。

最初にリリースされた DEC Alpha システムである  シリーズは同時期のMIPSベースのDECstationによく似ており、DECstationはAlphaシステムによって徐々に置き換えられていった。どちらもという拡張バスを使用してビデオカードやネットワークカードを接続し、同じマウスやディスプレイやキーボードを使用していた。

後に[ECLベースの](../Page/エミッタ結合論理.md "wikilink")[R6000](https://ja.wikipedia.org/wiki/R6000 "wikilink")を採用したシステムも計画されたが、R6000を製造した [Bipolar Integrated Technology](https://ja.wikipedia.org/wiki/:en:Bipolar_Integrated_Technology "wikilink") が十分な量のプロセッサの生産に失敗したため、1990年8月14日にキャンセルとなった\[4\]。

MIPSベースのDECstationは[Mach](../Page/Mach.md "wikilink")[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")の最初のターゲットシステムとされ、開発プラットフォームとしても使われた。また、[Windows NTオペレーティングシステムの初期の開発にも使われた](../Page/Microsoft_Windows_NT.md "wikilink")。DEC Alpha システムのリリースの少し前には [OSF/1](../Page/Tru64_UNIX.md "wikilink") が DECstation で完全に動作していたが、製品としてはリリースされなかった。その後 [NetBSD](../Page/NetBSD.md "wikilink")や[Linux](../Page/Linux.md "wikilink")/MIPSといった[フリーなOSが](../Page/フリーソフトウェア.md "wikilink") MIPSベースのDECstationに移植されている。

DECstationの様々な機種は  ソフトウェアプロジェクトによって[エミュレートされている](../Page/エミュレータ.md "wikilink")。

### 機種

最初の DECstation 3100 に続き、低価格な 2100 がリリースされた。DECstation 3100 は当時世界最速のUNIXワークステーションと宣伝された。同時期にリリースされた VAXstation 3100 に比べると約3倍の性能だった。[フレームバッファやグラフィックスアクセラレータを省いた](https://ja.wikipedia.org/wiki/VRAM#フレームバッファ "wikilink")[サーバ](../Page/サーバ.md "wikilink")構成のDECstationは、または[Q-bus](../Page/Q-bus.md "wikilink")ベースで "" と呼ばれた。[PDP-10](../Page/PDP-10.md "wikilink")の一部システムも同じ名称だが、違うシステムなので注意されたい。

初期のDECstationは拡張性に乏しく拡張用バスも備えていなかった。後の DECstation 5000 システムからTURBOchanelによる拡張が可能になっている。また DECstation 5000 システムは [Advanced RISC Computing](https://ja.wikipedia.org/wiki/Advanced_RISC_Computing "wikilink") (ARC) 準拠でもある。後期のDECstationは集積度を上げるため[ASIC](../Page/ASIC.md "wikilink")化を進め、部品点数を削減している。この傾向は DECstation 5000/240 から始まり、DECstation 5000/260 では制御論理回路のほとんどを単一の VLSI ASIC で実装していた。

DECstation 5000 システムの型番にはさらに2文字か3文字が最後に付属しており、グラフィックスオプションを示していた。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Ds2100-01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:DECStation_5000_\(white_bg\).jpg "wikilink")

  - **DECstation 3100**（コードネーム *PMAX*）
      - リリース: 1989年1月11日\[5\]
      - CPU: [R2000](../Page/R2000.md "wikilink") 16.67MHz, R2010/R2020チップセット\[6\]
      - メモリ: 最大 24 Mバイト（2MバイトSIMM×2個ずつで、最大6バンク）
      - フレームバッファ: 256KB（モノクロ）または1MB（カラー）
      - グラフィックス: 1024×768ピクセル（モノクロまたは8ビットカラー）
          - マウスカーソルはハードウェアで生成
          - フレームバッファ全体が表示されるわけではなく、表示されない部分にはフォントなどのイメージを置いた。
      - 入出力: [10メガビット・イーサネット](../Page/10メガビット・イーサネット.md "wikilink")、[SCSI](../Page/Small_Computer_System_Interface.md "wikilink")（HDDは内蔵せず）、シリアルポート
  - **DECstation 2100**（コードネーム *PMIN*）
      - リリース: 1989年7月11日
      - CPU: [R2000](../Page/R2000.md "wikilink") 12.5MHz\[7\], R2010/R2020チップセット\[8\]
      - メモリ: 最大 24Mバイト（2MバイトSIMM×2個ずつで、最大6バンク）
      - フレームバッファ: 256KB（モノクロ）または1MB（カラー）
      - グラフィックス: 1024×768ピクセル（モノクロまたは8ビットカラー）
          - マウスカーソルはハードウェアで生成
          - フレームバッファ全体が表示されるわけではなく、表示されない部分にはフォントなどのイメージを置いた。
      - 入出力: [10メガビット・イーサネット](../Page/10メガビット・イーサネット.md "wikilink")、[SCSI](../Page/Small_Computer_System_Interface.md "wikilink")（HDDは内蔵せず）、シリアルポート
  - **Personal DECstation 5000/20**, **5000/25**, **5000/33**, **5000/50** （コードネーム *MAXine*）
      - リリース:（少なくとも /33 は）1992年6月22日
      - CPU: [R3000](../Page/R3000.md "wikilink") 20, 25, 33 MHz （それぞれ /20, /25, /33 に対応）\[9\], R3010
      - CPU: [R4000](https://ja.wikipedia.org/wiki/R4000 "wikilink") 100 MHz (/50)
          - CPUモジュール以外は12.5MHz動作であり、CPUモジュールとのインタフェースのためのカスタムASICが使われている\[10\]。
      - メモリ: 8 Mバイト 内蔵（最大 40 Mバイト RAM） - 8Mバイトまたは2MバイトのSIMM×2個ずつ追加可能（ただし、全SIMMは同一サイズでなければならない）
      - 拡張スロット: [TURBOchannel](https://ja.wikipedia.org/wiki/:en:TURBOchannel "wikilink")×2スロット（それぞれ64MBのアドレス空間に対応）
      - グラフィックス: 1024×768ピクセル（8ビットカラー） - 24ビットカラーのうち256色をパレットに置いて選択する\[11\]。
      - 入出力: [10メガビット・イーサネット](../Page/10メガビット・イーサネット.md "wikilink")、[SCSI](../Page/Small_Computer_System_Interface.md "wikilink")（HDD最大2台内蔵）、シリアルポート、アナログオーディオ/ISDNポート
  - **DECstation 5000/120**, **5000/125**, **5000/133**, **5000/150**（コードネーム *3MIN*）
      - CPU: [R3000](../Page/R3000.md "wikilink") 20, 25, 33 MHz（それぞれ /120, /125, /133 に対応）\[12\], R3010
          - Personal 5000 シリーズよりキャッシュ容量が大きい。
      - CPU: [R4000](https://ja.wikipedia.org/wiki/R4000 "wikilink") 100 MHz (/150)
      - メモリ: 最大 128 Mバイト - 8Mバイトまたは2MバイトのSIMM×2個ずつ追加可能（ただし、全SIMMは同一サイズでなければならない）
      - 拡張スロット: TURBOchannel×3スロット
  - **DECstation 5000/200**（コードネーム *3MAX*）, **DECstation 5000/240**, **5000/260**（コードネーム *3MAX+*）
      - リリース: 1990年4月3日 (/200)
      - CPU: R3000 25 MHz, R3010
      - CPU: R3400 40 MHz (/240)\[13\]Worksystems Base Product Marketing: "*DECstation 5000 Model 240 Workstation Technical Overview*", Version 1.0, December 1991, Digital Equipment Corporation</ref> - R3400はR3000とR3010をワンチップ化したもの
      - CPU: [R4000](https://ja.wikipedia.org/wiki/R4000 "wikilink") 120 MHz (/260)\[14\]DECstation/DECsystem 5000 Model 200 Series Maintenance Guide, Second Printing, April 1993, EK-PM38C-MG-002, Digital Equipment Corporation</ref>
      - メモリ: 最大 480 Mバイト - 32Mバイトまたは8MバイトのSIMM×2個ずつ追加可能（ただし、全SIMMは同一サイズでなければならない）\[15\]\[16\]
          - [メモリインタリーブ](https://ja.wikipedia.org/wiki/メモリインタリーブ "wikilink")方式で実効帯域幅を向上させている。
          - オプションでバッテリバックアップされた1MBの[NVRAM](https://ja.wikipedia.org/wiki/NVRAM "wikilink")のSIMMを装備でき、ディスクキャッシュとして使用可能（専用ソフトウェアが必要）\[17\]
      - 拡張スロット: TURBOchannel×3スロット（各スロットに4MB(/200)または8MB(/240,260)のアドレス空間を割り当て）\[18\]
      - 入出力:
          - 200: イーサネットとSCSIはTURBOchannelモジュールで提供。4シリアルポートで、キーボード、マウス、プリンタ、モデムを接続。
          - 240/260: TURBOchannelと2つのI/OバスをASICで接続し、そのI/OバスにSCSIやイーサネット等のデバイスを接続。このASICは Model 1xx の際に導入されたものだが、240/260では動作クロックが12.5MHzから25MHzに向上している。このI/Oサブシステムは DEC 3000 AXP でも若干修正されて採用された\[19\]。

### グラフィックス

TURBOchannelのスロットのある DECstation では、フレームバッファ、2Dアクセラレータ、3DアクセラレータをTURBOchannel経由で接続可能だった。

#### フレームバッファ

  - **CX "Color Frame-Buffer Graphics Module"** (PMAG-BA)\[20\] - 1024×864ピクセル、8ビットカラー
  - **HX "Smart Frame-Buffer Graphics Module"** (PMAGB-BA/BC/BE)\[21\] - 限定的だが高速な2Dアクセラレータ機能をASICで実装したフレームバッファ\[22\]
  - **MX "[Monochrome](../Page/モノクローム.md "wikilink") Frame-Buffer Graphics Module"** (PMAG-AA)\[23\] - 1280×1024ピクセル、1ビットカラー
  - **TX "[True Color](../Page/色深度.md "wikilink") Frame-Buffer Graphics Module"** (PMAG-JA, PMAGB-JA)\[24\] - 1280×1024ピクセル、24ビットカラー（2機種あるのは、リフレッシュレートが異なるため）

#### 2Dアクセラレータ

  - **PX "2D Graphics Accelerator"** - PixelStampアーキテクチャ採用。ただし[ジオメトリエンジン](https://ja.wikipedia.org/wiki/ジオメトリエンジン "wikilink")は含まないので、2Dグラフィックスしかアクセラレートできない。多くのアプリケーションで **HX** の方が優れていた。

#### 3Dアクセラレータ

  - **PXG** (Lo 3D Graphics Accelerator, Mid 3D Graphics Accelerator)\[25\]
  - **PXG+** (Lo 3D Plus Graphics Accelerator, Mid 3D Plus Graphics Accelerator)\[26\]
  - **PXG Turbo** (Hi 3D Graphics Accelerator)\[27\]
  - **PXG Turbo+** (Hi 3D Plus Graphics Accelerator)\[28\]

これらはいずれも8ビットカラーまたは24ビットカラーで、解像度は1280×1024ピクセル、リフレッシュレートは66Hzか72Hzである。[Zバッファ](../Page/Zバッファ.md "wikilink")は8ビットまたは24ビットで、[ダブルバッファリング](https://ja.wikipedia.org/wiki/ダブルバッファリング "wikilink")されている。[色深度](../Page/色深度.md "wikilink")とZバッファ深度は、モジュール上にVSIMMやZバッファモジュールを追加することで拡張可能である。

これら3DアクセラレータはDEC独自のPixelStampアーキテクチャを採用している。これは、[ノースカロライナ大学](https://ja.wikipedia.org/wiki/ノースカロライナ大学 "wikilink")の *Pixel Planes* と[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")の *The 8 by 8 Display* から生まれたものである\[29\]。

PixelStampアーキテクチャは、DMAエンジン、[ジオメトリエンジン](https://ja.wikipedia.org/wiki/ジオメトリエンジン "wikilink")、PixelStampから構成されるジオメトリ・パイプラインである。DMAエンジンはTURBOchannel経由でそのパイプラインとシステムのインタフェースを形成し、CPUからパケットを受け取ってそれをジオメトリエンジンに送る。ジオメトリエンジンはSRAMと [Intel i860](../Page/Intel_i860.md "wikilink") で構成されている。DMAエンジンから送り込まれたパケットをSRAMに格納し、それをi860で処理し、その結果を[FIFO](../Page/FIFO.md "wikilink")に書き出す。

PixelStamp部は STIC (STamp Interface Chip) ASIC と1つまたは2つの STAMP ASIC から構成される。STICはFIFOから結果をフェッチし、それを STAMP ASIC に渡す。STAMP ASIC は[ラスタライズ](../Page/ラスタライズ.md "wikilink")などのグラフィカル機能を実行する。STAMP ASIC が処理したデータが最終結果（RGBデータ）となり、VSIMMs (SIMM with VRAMs) で構成されたフレームバッファに書き込まれ、表示される。

PXG と PXG+ は double-width、PXG Turno と PXG Turbo+ は triple-width の基板である。"+" が付いているものは高性能版であり、i860 が40MHzではなく44MHzで動作し、STIC と STAMP ASIC の動作周波数も33%向上している。"Trubo" の付いているものはSRAM容量が倍で、STAMP ASIC も倍である。"Lo 3D" または "Lo 3D Plus" は、VSIMMsとZバッファモジュールを追加すると "Mid 3D" または "Mid 3D Plus" にアップグレードできる。

## DECstation PC

上述のDECstationワークステーションと並行して、DECは[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")プロセッサを使用し[MS-DOS](../Page/MS-DOS.md "wikilink")の動作する[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")をDECstationのブランド名で発表した\[30\]。機種名を表す3桁の数字で識別され、**DECstation 2xx** ([286](../Page/Intel_80286.md "wikilink"))、**3xx** ([386](../Page/Intel_80386.md "wikilink"))、**4xx** ([486](https://ja.wikipedia.org/wiki/Intel_486 "wikilink")) の3シリーズがある。生産はDECではなく[タンディ・コーポレーション](https://ja.wikipedia.org/wiki/タンディ・コーポレーション "wikilink")（アメリカ）と[オリベッティ](../Page/オリベッティ.md "wikilink")（ヨーロッパ）が行った。DECはDECstationの発表時、DECがかつて販売したPC非互換なコンピュータ  の下取りキャンペーンを行った。

## 脚注

## 外部リンク

  - [VT78 page at old-computers.com](http://www.old-computers.com/museum/computer.asp?c=369&st=1)
  - [NetBSD for the DECstation](http://www.netbsd.org/Ports/pmax/)
  - [Linux/MIPS DECstation page](http://www.linux-mips.org/wiki/DECstation)
  - [DECstation 2100 / DECstation 3100 Web Page](http://www.vanade.com/~blc/DS3100/)
  - [DECstation model specifications](http://www.xs4all.nl/~vhouten/mipsel/models.html)
  - [Linux for DECstation](http://decstation.unix-ag.org/)

[Category:ディジタル・イクイップメント・コーポレーション](https://ja.wikipedia.org/wiki/Category:ディジタル・イクイップメント・コーポレーション "wikilink") [Category:ワークステーション](https://ja.wikipedia.org/wiki/Category:ワークステーション "wikilink")

1.  Thomas C. Furlong et al., "Development of the DECstation 3100". *Digital Technical Journal*, Volume 2, Number 2, Spring 1990. Digital Equipment Corporation
2.  Computergram.
3.  Armando Stettner
4.  "DEC Cancels ULTRIX Workstation Using ECL R6000". *Computer Business Review*, 15 August 1990.
5.  [John Markoff: "*COMPANY NEWS; 8 Desktop Computers Introduced by Digital*," New York Times](http://query.nytimes.com/gst/fullpage.html?res=950DEEDC153AF932A25752C0A96F948260)
6.  [Workstation Systems Engineering: "*DECstation 3100 Desktop Workstation Functional Specification*", Revision 1.3, 28 August 1990, Digital Equipment Corporation](ftp://ftp.hp.com/pub/alphaserver/archive/specs/DS3100.ps.Z)
7.  RISC Family Performance Summary, 2 April 1990, Digital Equipment Corporation
8.
9.  [Personal DECstation/DECsystem 5000 Series Maintenance Guide, Third Printing, April 1993, EK-PM30F-MG-004, Digital Equipment Corporation](http://deathrow.vistech.net/~cvisors/dec94mds/pm30fmg4.pdf)
10. Worksystems Base Product Marketing: "Personal DECstation Series Technical Overview", Version 1.0, December 1991, Digital Equipment Corporation
11.
12. DECstation 5000/100 Series Workstations, Digital Equipment Corporation
13.
14.
15.
16.
17.
18.
19. Todd A. Dutton et al., "The Design of the DEC 3000 AXP Systems, Two High-performance Workstations", Digital Technical Journal, Volume 4, Number 4, Special Issue 1992.
20. TURBOchannel Maintenance Guide, October 1991, EK-TRBOC-MG-005, Digital Equipment Corporation
21.
22. [Joel McCormack and Bob McNamara. *WRL Research Report 93/1, A Smart Frame Buffer*. Western Research Laboratory, Digital Equipment Corporation.](http://www.hpl.hp.com/techreports/Compaq-DEC/WRL-93-1.pdf)
23.
24.
25.
26.
27.
28.
29. [Brian Kelleher. *PixelVision Architecture*. Workstation Systems Engineering, Digital Equipment Corporation.](http://www.hpl.hp.com/techreports/Compaq-DEC/SRC-TN-1998-013.pdf)
30. [Computergram. "DEC LAUNCHES DECSTATION FAMILY OF MS-DOS DESKTOP COMPUTERS". Computer Business Review, 30 June 1989](http://www.cbronline.com/news/dec_launches_decstation_family_of_ms_dos_desktop_computers)