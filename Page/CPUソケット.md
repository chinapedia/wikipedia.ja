> この記事は[CPU](https://ja.wikipedia.org/wiki/CPU)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Socket_775.png "wikilink") (または [LGA775](https://ja.wikipedia.org/wiki/LGA775 "wikilink"))\]\] [thumb](https://ja.wikipedia.org/wiki/ファイル:SocketA.jpg "wikilink") (または [Socket 462](https://ja.wikipedia.org/wiki/Socket_462 "wikilink"))\]\] **CPUソケット**は、大規模[集積回路](../Page/集積回路.md "wikilink")（LSI IC）パッケージ用のICソケットで、[CPU](../Page/CPU.md "wikilink")用のものである。数十〜数千接点で、高い動作周波数でも動作する必要があるなどの特殊性はあるが、基本的にはCPU以外のLSI用のICソケットと何ら変わるものではない。しかし、CPUとマザーボード間のインタフェースとしての電気的・論理的仕様も含んで「[Socket AM4](https://ja.wikipedia.org/wiki/Socket_AM4 "wikilink")」などといった名前で識別される場合もある。形状によっては（「[Slot 1](../Page/Slot_1.md "wikilink")」など）「CPUスロット」などもある。CPU以外の[プロセッサ](../Page/プロセッサ.md "wikilink")（[GPUや](../Page/Graphics_Processing_Unit.md "wikilink")[APU](https://ja.wikipedia.org/wiki/AMD_Accelerated_Processing_Unit "wikilink")）についても何ら変わる所はないが、GPUなどでは選択に自由度が無いことも多く、そういった場合は直接ハンダ付けで実装してしまってあり、ソケットは使われない。

## 概要

2017年現在、ほとんどのマザーボードは、CPUの選択にそれなりの自由度があることから、CPUソケットを使用している。

多くのCPUとソケット間のインタフェースは[Pin grid array](https://ja.wikipedia.org/wiki/Pin_grid_array "wikilink") (PGA) で、CPU[パッケージ底面の短く硬いピンがソケットの穴に嵌る](../Page/パッケージ_\(電子部品\).md "wikilink")。Zero Insertion Force (ZIF) ソケットではほとんど抵抗なくCPUを挿入することができる。確実に装着した後、レバーを倒してピンをしっかりと圧接・保持し、接点を確実に接触させる。

2018年現在、いくつかの現行のCPUと今後予定されているCPUの設計では、[Land Grid Array](https://ja.wikipedia.org/wiki/パッケージ_\(電子部品\)#LGA_\(Land_grid_array\) "wikilink") (LGA) が使用されている。このパッケージではピンはソケットの側に存在する。ピンは、CPUパッケージ底面のパッド または*ランド*と接触する。

  - スロット
    [1990年代](../Page/1990年代.md "wikilink")後半に、多くの[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")プロセッサはソケットではなくスロットに装着された。CPUスロットは[拡張スロットに似た](https://ja.wikipedia.org/wiki/拡張カード "wikilink")、シングルエッジのコネクタであり、そこにCPUを搭載した[プリント基板](../Page/プリント基板.md "wikilink")であるCPUユニットを挿入した。スロット型のCPUパッケージは2つの利点があった。CPUユニットのプリント基板に[集積回路](../Page/集積回路.md "wikilink")を追加することによりL2[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")を拡充できることと、CPUの挿入・抜却が容易になることである。しかし、スロット型のパッケージはCPUと[チップセット](../Page/チップセット.md "wikilink")の間の配線長が長くなり、その長いプリントパターンに[分布する静電容量と](https://ja.wikipedia.org/wiki/寄生容量 "wikilink")[電気抵抗](../Page/電気抵抗.md "wikilink")が、500MHzを超えるクロックスピードにおいて無視できない[インピーダンス](../Page/インピーダンス.md "wikilink")として顕在化し不適切なものとなった。CPUスロットは、[AMDの](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[Socket Aとインテルの](https://ja.wikipedia.org/wiki/Socket_A "wikilink")[Socket 370が導入されたことで使われることはなくなった](https://ja.wikipedia.org/wiki/Socket_370 "wikilink")。

<!-- end list -->

  - 名称の混同
    例えば、[LGA775](https://ja.wikipedia.org/wiki/LGA775 "wikilink")パッケージを採用した（すなわち外形がLGA775である）CPUを接続するCPUソケットの正しい名称は **Socket T** であるが、しばしば *LGA775 ソケット* 、あるいは略して単に *LGA775* と表記される。また *LGA775* という語は、[後述するとおりハードウェアプラットフォームの名称としても拡大使用されている](https://ja.wikipedia.org/wiki/#広義のCPUソケット・スロット "wikilink")。これらのことから、*LGA775* とのみ表記されている場合はそれがCPUの形状を指すのか[マザーボード](https://ja.wikipedia.org/wiki/マザーボード "wikilink")の構成部品を指すのかコンピュータのハードウェア仕様を指すのか、文脈から判断しなければならない。

### 汎用品

以下は、もっぱら既存の汎用のICソケットが使われる[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")である。ZIFソケットではないものが多く、引き抜く際に適切な工具が必要になる。

  - [DIPソケット](https://ja.wikipedia.org/wiki/パッケージ_\(電子部品\)#DIP_\(Dual_Inline_Package\) "wikilink")（40個の接点）
      - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")系 - [8086](../Page/Intel_8086.md "wikilink"), [8088](../Page/Intel_8088.md "wikilink"), [V30, V20など](https://ja.wikipedia.org/wiki/NEC_Vシリーズ#V30 "wikilink")
      - 他 - [8080](../Page/Intel_8080.md "wikilink")\[1\], [Z80](../Page/Z80.md "wikilink"), [8085など](https://ja.wikipedia.org/wiki/Intel_8085 "wikilink")
  - [PLCC](../Page/PLCC.md "wikilink")ソケット（68個の接点）
      - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")系 - [80186](https://ja.wikipedia.org/wiki/Intel_80186 "wikilink")\[2\] \[3\], [V50](https://ja.wikipedia.org/wiki/NEC_Vシリーズ#V40・V50 "wikilink"), [80286など](../Page/Intel_80286.md "wikilink")
      - 他 - [MC68000](../Page/MC68000.md "wikilink")など
  - [PGA](https://ja.wikipedia.org/wiki/PGA "wikilink")ソケット - [80386](../Page/Intel_80386.md "wikilink") 14列・接点数132（3重の接点配列）
  - PGAソケット - [MC68040](https://ja.wikipedia.org/wiki/MC68040 "wikilink") 18列・接点数179（3重の接点配列、一隅なし）

## インタフェース

CPUソケットに関する、各種インタフェース仕様の一覧と解説である。

3桁の数字を含んでいる多くのソケット名は、CPUやソケットのピンの数を意味している。

### インテルおよびその互換

  - [Socket 1](https://ja.wikipedia.org/wiki/Socket_1 "wikilink") - [486](../Page/Intel486.md "wikilink")\[4\]
  - [Socket 2](https://ja.wikipedia.org/wiki/Socket_2 "wikilink") - 486, 486用Pentium ODP（以下P24T）
  - [Socket 3](https://ja.wikipedia.org/wiki/Socket_3 "wikilink") - 486（5[Vまたは](../Page/ボルト_\(単位\).md "wikilink")3.3V）, P24Tおよび互換製品
  - [Socket 4](https://ja.wikipedia.org/wiki/Socket_4 "wikilink") - [Pentium](../Page/Intel_Pentium_\(1993年\).md "wikilink") 60/66[MHz](https://ja.wikipedia.org/wiki/メガヘルツ "wikilink")
  - [Socket 5](https://ja.wikipedia.org/wiki/Socket_5 "wikilink") - Pentium 75-133MHz, [AMD K5](https://ja.wikipedia.org/wiki/AMD_K5 "wikilink"), [IDT](https://ja.wikipedia.org/wiki/IDT "wikilink") [WinChip](../Page/WinChip.md "wikilink") C6, WinChip 2
  - [Socket 6](https://ja.wikipedia.org/wiki/Socket_6 "wikilink") - 486向けに設計されたが、あまり使用されなかった。ライトバック(WB)対応486DX2, IntelDX4\[5\]
  - [Socket 7](https://ja.wikipedia.org/wiki/Socket_7 "wikilink") - Pentium, Pentium MMX, [AMD K6シリーズ](https://ja.wikipedia.org/wiki/AMD_K6 "wikilink"), いくつかの[サイリックス](../Page/サイリックス.md "wikilink")製CPU, WinChip2 Rev.A

### インテル専用

#### デスクトップ

  - [Socket 8](https://ja.wikipedia.org/wiki/Socket_8 "wikilink") - [Pentium Pro](../Page/Pentium_Pro.md "wikilink")
  - [Slot 1](../Page/Slot_1.md "wikilink") - [Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink"), [Pentium II](../Page/Pentium_II.md "wikilink"), [Pentium III](../Page/Pentium_III.md "wikilink")
  - [Socket 370](https://ja.wikipedia.org/wiki/Socket_370 "wikilink") - Pentium III, Celeron; [Cyrix](https://ja.wikipedia.org/wiki/Cyrix "wikilink") III; [VIA C3](https://ja.wikipedia.org/wiki/VIA_C3 "wikilink")
  - [Socket 423](https://ja.wikipedia.org/wiki/Socket_423 "wikilink") - [Pentium 4](../Page/Pentium_4.md "wikilink")\[6\]と Celeron プロセッサ（Willamette コア）
  - [Socket N](https://ja.wikipedia.org/wiki/Socket_478 "wikilink")（または Socket 478 として知られる） - Pentium 4, Celeron（Northwood, Prescott, Willamette コア）, [Pentium 4 Extreme Edition](https://ja.wikipedia.org/wiki/Pentium_Extreme_Edition "wikilink")\[7\]
  - [Socket 479](https://ja.wikipedia.org/wiki/Socket_479 "wikilink") - [Pentium M](https://ja.wikipedia.org/wiki/Pentium_M "wikilink")
  - [Socket T](https://ja.wikipedia.org/wiki/LGA775 "wikilink")（または Socket 775 や LGA775 として知られる） - Pentium 4, [Pentium D](https://ja.wikipedia.org/wiki/Pentium_D "wikilink"), Celeron D, [Pentium Extreme Edition](https://ja.wikipedia.org/wiki/Pentium_Extreme_Edition "wikilink"), [Pentium Dual-Core](../Page/Pentium_Dual-Core.md "wikilink"), [Core 2 Duo](https://ja.wikipedia.org/wiki/Intel_Core_2 "wikilink"), [Core 2 Extreme](https://ja.wikipedia.org/wiki/Intel_Core_2 "wikilink"), Celeron\[8\], [Xeon 3000 シリーズ](https://ja.wikipedia.org/wiki/Xeon#インテル_Xeon_プロセッサー_3000_系 "wikilink"), [Core 2 Quad](https://ja.wikipedia.org/wiki/Intel_Core_2 "wikilink")（Northwood, Prescott, Conroe, Kentsfield, Wolfdale, Yorkfield と Cedar Mill コア）
  - [Socket B](https://ja.wikipedia.org/wiki/LGA1366 "wikilink") (LGA1366 \[9\]) - [Nehalemマイクロアーキテクチャ](https://ja.wikipedia.org/wiki/Nehalemマイクロアーキテクチャ "wikilink")の[Intel Core i7](https://ja.wikipedia.org/wiki/Intel_Core_i7 "wikilink")（DDR3統合メモリコントローラと [Intel QuickPath Interconnect](https://ja.wikipedia.org/wiki/Intel_QuickPath_Interconnect "wikilink")(QPI) を取り入れた）
  - [Socket H](https://ja.wikipedia.org/wiki/LGA1156 "wikilink") (LGA1156) - Nehalemマイクロアーキテクチャ および Westmereマイクロアーキテクチャの[Intel Core i7](https://ja.wikipedia.org/wiki/Intel_Core_i7 "wikilink"), [Core i5](https://ja.wikipedia.org/wiki/Intel_Core_i5 "wikilink"), [Core i3](https://ja.wikipedia.org/wiki/Intel_Core_i3 "wikilink"), [Pentium G](https://ja.wikipedia.org/wiki/Intel_Pentium "wikilink"), [Celeron G](../Page/Intel_Celeron.md "wikilink")。QPIではなく[Direct Media Interface](https://ja.wikipedia.org/wiki/Direct_Media_Interface "wikilink")(DMI)を採用し、CPU側にメモリコントローラや[PCI Expressコントローラを内蔵した](https://ja.wikipedia.org/wiki/PCI_Express "wikilink")。
  - [Socket H2](https://ja.wikipedia.org/wiki/LGA1155 "wikilink") (LGA1155) - [Sandy Bridgeマイクロアーキテクチャ](https://ja.wikipedia.org/wiki/Sandy_Bridgeマイクロアーキテクチャ "wikilink") 及び [Ivy BridgeマイクロアーキテクチャのIntel](https://ja.wikipedia.org/wiki/Ivy_Bridgeマイクロアーキテクチャ "wikilink") Core i7, Core i5, Core i3, Pentium G, Celeron G
  - [Socket H3](https://ja.wikipedia.org/wiki/LGA1150 "wikilink") (LGA1150) - [Haswellマイクロアーキテクチャ](https://ja.wikipedia.org/wiki/Haswellマイクロアーキテクチャ "wikilink") 及び [Broadwellマイクロアーキテクチャ](https://ja.wikipedia.org/wiki/Broadwellマイクロアーキテクチャ "wikilink")のIntel Core i7, Core i5, Core i3, Pentium G, Celeron G
  - [Socket H4](https://ja.wikipedia.org/wiki/LGA1151 "wikilink") (LGA1151) - [Skylakeマイクロアーキテクチャ](https://ja.wikipedia.org/wiki/Skylakeマイクロアーキテクチャ "wikilink")、[Kaby Lakeマイクロアーキテクチャ](https://ja.wikipedia.org/wiki/Kaby_Lakeマイクロアーキテクチャ "wikilink") 及び Coffee Lakeマイクロアーキテクチャ、Coffee Lake RefreshマイクロアーキテクチャのIntel Core i9, Core i7, Core i5, Core i3, Pentium G, Celeron G
  - [Socket R](https://ja.wikipedia.org/wiki/LGA2011 "wikilink") (LGA2011) - Sandy Bridgeマイクロアーキテクチャ 及び Ivy Bridgeマイクロアーキテクチャの [Core i7 Extreme](https://ja.wikipedia.org/wiki/Intel_Core_i7 "wikilink")（3800/3900/4800/4900番台）
  - [Socket R3](https://ja.wikipedia.org/wiki/LGA2011 "wikilink") (LGA2011-v3) - Haswellマイクロアーキテクチャ 及び Broadwellマイクロアーキテクチャの Intel Core i7 Extreme（5800/5900/6800/6900番台）
  - [Socket R4](https://ja.wikipedia.org/wiki/LGA2066 "wikilink") (LGA2066) - [Skylakeマイクロアーキテクチャ](https://ja.wikipedia.org/wiki/Skylakeマイクロアーキテクチャ "wikilink") 及び [Kaby LakeマイクロアーキテクチャのIntel](https://ja.wikipedia.org/wiki/Kaby_Lakeマイクロアーキテクチャ "wikilink") Core i9(7900番台) ,Core i7 (7900/7800番台・7740X),Core i5 (7640X)

#### モバイル

  - [Socket 479](https://ja.wikipedia.org/wiki/Socket_479 "wikilink") - [Pentium M](https://ja.wikipedia.org/wiki/Pentium_M "wikilink") と Celeron M(Banias と Dothan コア)
  - [Socket 495](https://ja.wikipedia.org/wiki/Socket_495 "wikilink") - PPGA-B495 としても知られる。Mobile P3 Coppermine と Celeron \[10\] で使用された。
  - [Socket M](https://ja.wikipedia.org/wiki/Socket_M "wikilink") - [Core Solo](https://ja.wikipedia.org/wiki/Intel_Core "wikilink"), [Core Duo](https://ja.wikipedia.org/wiki/Intel_Core "wikilink"), [Core 2 Duo](https://ja.wikipedia.org/wiki/Intel_Core_2 "wikilink")
  - [Micro-FCBGA](https://ja.wikipedia.org/wiki/Micro-FCBGA "wikilink") - [Mobile Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink"), Core 2 Duo (モバイル向け), Core Duo, Core Solo, [Celeron M](https://ja.wikipedia.org/wiki/Celeron_M "wikilink"), [Pentium III](../Page/Pentium_III.md "wikilink") (モバイル向け)
  - [Socket P](https://ja.wikipedia.org/wiki/Socket_P "wikilink") - インテルベース。[Socket 479](https://ja.wikipedia.org/wiki/Socket_479 "wikilink") と [Socket M](https://ja.wikipedia.org/wiki/Socket_M "wikilink") を置き換える。2007年5月9日にリリースされた。
  - [Socket G1](https://ja.wikipedia.org/wiki/Socket_G1 "wikilink")（rPGA 988A,PGA 989,PGA 988）\[11\]- Nehalemマイクロアーキテクチャ および　WestmereマイクロアーキテクチャのIntel Core i7, Core i5, Core i3, Pentium, Celeron（モバイル向け）
  - [Socket G2](https://ja.wikipedia.org/wiki/Socket_G2 "wikilink")（rPGA 988B）- Sandy Bridgeマイクロアーキテクチャ および Ivy BridgeマイクロアーキテクチャのIntel Core i7, Core i5, Core i3, Pentium, Celeron（モバイル向け）
  - [Socket G3](https://ja.wikipedia.org/wiki/Socket_G3 "wikilink")（rPGA 946B/947,FCPGA 946）- HaswellマイクロアーキテクチャのIntel Core i7, Core i5, Core i3, Pentium, Celeron（モバイル向け）

#### サーバ

  - [Slot 2](https://ja.wikipedia.org/wiki/Slot_2 "wikilink") - Pentium II [Xeon](../Page/Xeon.md "wikilink"), [Pentium III Xeon](https://ja.wikipedia.org/wiki/Xeon#Pentium_III_Xeon "wikilink")

  - [Socket 603](https://ja.wikipedia.org/wiki/Socket_603 "wikilink") - [Xeon](../Page/Xeon.md "wikilink")（Northwood と Willamette コア）

  - [Socket 604](https://ja.wikipedia.org/wiki/Socket_604 "wikilink") - [Xeon](../Page/Xeon.md "wikilink")

  - \- [Itanium](https://ja.wikipedia.org/wiki/Itanium "wikilink")

  - \- [Itanium 2](https://ja.wikipedia.org/wiki/Itanium_2 "wikilink"), [HP](../Page/ヒューレット・パッカード.md "wikilink") [PA-RISC](https://ja.wikipedia.org/wiki/PA-RISC "wikilink") 8800 と 8900

  - [Socket J](https://ja.wikipedia.org/wiki/Socket_J "wikilink") (または Socket 771 や LGA 771 として知られる) - [Xeon](../Page/Xeon.md "wikilink")（Woodcrest コア）

  - [Socket N](https://ja.wikipedia.org/wiki/Socket_478 "wikilink") - [Dual-Core Xeon LV](../Page/Xeon.md "wikilink")

  - [LGA1567](https://ja.wikipedia.org/wiki/LGA1567 "wikilink")\[12\] （またはSocket LS）- [Xeon](https://ja.wikipedia.org/wiki/Xeon#ネハレム（ネハレン）_EX_\(Nehalem-EX\) "wikilink")(Nehalem-EX)

  - [LGA1356](https://ja.wikipedia.org/wiki/LGA1356 "wikilink") （または Socket B2） - Sandy Bridge-EN

  - [LGA2011](https://ja.wikipedia.org/wiki/LGA2011 "wikilink") （または Socket R） - [Xeon](../Page/Xeon.md "wikilink")（SandyBridge-EP, Ivy Bridge-EP, Haswell-EP4S/EX：Xeon E5/E7系の一部）

  - [LGA2011](https://ja.wikipedia.org/wiki/LGA2011 "wikilink")-1 （または Socket R2） - [Xeon](../Page/Xeon.md "wikilink")（Ivy Bridge-EX, Haswell-EX：Xeon E7 v2系の一部）

  - [LGA2011](https://ja.wikipedia.org/wiki/LGA2011 "wikilink")-v3 （または Socket R3） - [Xeon](../Page/Xeon.md "wikilink")（Haswell-EP, Broadwell-EP：Xeon E5 v3, v4系の一部）

### AMD

#### デスクトップ (AMD)

  - [Super Socket 7](https://ja.wikipedia.org/wiki/Super_Socket_7 "wikilink") - [AMD K6-2](https://ja.wikipedia.org/wiki/AMD_K6-2 "wikilink"), [AMD K6-III](https://ja.wikipedia.org/wiki/AMD_K6-III "wikilink"); [Rise](https://ja.wikipedia.org/wiki/Rise_Technology "wikilink") , [Cyrix MII](https://ja.wikipedia.org/wiki/Cyrix_6x86#Cyrix_MII "wikilink"), [WinChip](../Page/WinChip.md "wikilink").
  - [Slot A](https://ja.wikipedia.org/wiki/Slot_A "wikilink") - [AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") [Athlon](../Page/Athlon.md "wikilink")
  - [Socket A](https://ja.wikipedia.org/wiki/Socket_A "wikilink")（または "Socket 462" として知られている） - [Athlon](../Page/Athlon.md "wikilink"), [Duron](../Page/Duron.md "wikilink"), Athlon XP, Athlon XP-M, Athlon MP, [Sempron](https://ja.wikipedia.org/wiki/Sempron "wikilink"), [Geode](https://ja.wikipedia.org/wiki/Geode "wikilink") プロセッサをサポートする AMD のソケット（462 個の接点の PGA）。
  - [Socket 754](https://ja.wikipedia.org/wiki/Socket_754 "wikilink") - シングルチャネルの[DDR SDRAMに対応したAMDのシングルプロセッサ用のソケット](https://ja.wikipedia.org/wiki/DDR_SDRAM "wikilink")。[Athlon 64](https://ja.wikipedia.org/wiki/Athlon_64 "wikilink"), Sempron, [Turion 64](https://ja.wikipedia.org/wiki/Turion_64 "wikilink") プロセッサに対応する（754 個の接点の PGA）。このソケット以降はメモリコントローラがCPUに統合されているため、CPUソケットとメモリが直結されている。
  - [Socket 939](https://ja.wikipedia.org/wiki/Socket_939 "wikilink") - デュアルチャネルの DDR-SDRAM に対応した AMD のシングルプロセッサ用のソケット。Athlon 64, 1 GHz\[13\] までの Athlon 64 FX, 4800+ までの [Athlon 64 X2](https://ja.wikipedia.org/wiki/Athlon_64_X2 "wikilink"), [Opteron](https://ja.wikipedia.org/wiki/Opteron "wikilink") 100 シリーズのプロセッサに対応する（939 個の接点の PGA）。発売後、約 2 年で Socket AM2 に置き換えられた。
  - [Socket AM2](https://ja.wikipedia.org/wiki/Socket_AM2 "wikilink") - DDR2-SDRAM に対応した AMD のシングルプロセッサ用のソケット。Socket 754 と Socket 939\[14\] を置き換えた（940 個の接点の PGA であり、Socket AM2 とサーバプロセッサ用の "Socket 940" と混用することがある）。 Athlon 64, Athlon 64 X2, [Athlon 64 FX](https://ja.wikipedia.org/wiki/Athlon_64_FX "wikilink"), Opteronプロセッサに対応し、電源回路と[BIOSの対応があれば](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")、[Phenom](https://ja.wikipedia.org/wiki/Phenom "wikilink"), [PhenomII](https://ja.wikipedia.org/wiki/AMD_Phenom_II "wikilink") プロセッサにも対応できる。
  - [Socket AM2+](https://ja.wikipedia.org/wiki/Socket_AM2+ "wikilink") - シングルプロセッサシステム用の AMD のソケット。[DDR2](../Page/DDR2_SDRAM.md "wikilink") と電源回路の分離された [HyperTransport](https://ja.wikipedia.org/wiki/HyperTransport "wikilink") 3 をサポートする。Socket AM2 を置き換えた（940 個の接点の PGA の Socket AM2 と電気的に互換性がある）。Athlon 64, Athlon 64 X2, Athlon 64 FX, Opteronプロセッサに対応し、電源回路とBIOSの対応があれば、Phenom, PhenomII プロセッサにも対応できる。
  - [Socket AM3](https://ja.wikipedia.org/wiki/Socket_AM3 "wikilink") - シンプルプロセッサシステム用のAMDのソケット。[DDR3](../Page/DDR3_SDRAM.md "wikilink") と電源回路の分離された [HyperTransport](https://ja.wikipedia.org/wiki/HyperTransport "wikilink") 3 をサポートする。DDR3-SDRAM をサポートすることで Socket AM2+ を置き換える（938 個の接点の PGA）。AM3版[PhenomIIをサポートしているが](https://ja.wikipedia.org/wiki/AMD_Phenom_II "wikilink")、DDR3メモリコントローラを搭載していないAM2+版PhenomIIやPhenom以前のCPUは使用できない。
  - [Socket AM3+](https://ja.wikipedia.org/wiki/Socket_AM3+ "wikilink") - Socket AM3の後継のソケットである。2011年Q3発売の[Bulldozerのために設計された](https://ja.wikipedia.org/wiki/Bulldozer_\(マイクロアーキテクチャ\) "wikilink")。[DDR2 SDRAMのサポートが削除された](../Page/DDR2_SDRAM.md "wikilink")。AM3およびそれ以前のソケットとの区別をつけやすくするため、AM3+では黒いソケットが採用されている。この黒いソケットそのものの名称は「AM3b」である。
  - [Socket AM4](https://ja.wikipedia.org/wiki/Socket_AM4 "wikilink") - 2017年3月発売の[Ryzen](https://ja.wikipedia.org/wiki/Ryzen "wikilink")プロセッサ用に発売された。[DDR4 SDRAMをサポート](https://ja.wikipedia.org/wiki/DDR4_SDRAM "wikilink")。以前のソケットと寸法が異なるため、一部のCPUクーラーのリテンションは互換性がない\[15\]。
  - [Socket FM1](https://ja.wikipedia.org/wiki/Socket_FM1 "wikilink") - [Fusion APU用のAMDのソケット](https://ja.wikipedia.org/wiki/AMD_Accelerated_Processing_Unit "wikilink")。ノースブリッジの廃止やCPUソケットに映像出力が加わることで、従来とは別のソケットとされた。FM1を使用するのは最初のデスクトップ向けAPUであるLlanoとその派生であるFM1版Athlonのみで、次世代のTrinityからはSocket FM2に置き換えられた。
  - [Socket FM2](https://ja.wikipedia.org/wiki/Socket_FM2 "wikilink") - Fusion APU用のAMDのソケット。二世代目のデスクトップ向けAPUであるTrinityと三世代目のデスクトップAPUであるRichland用。
  - [Socket AM1](https://ja.wikipedia.org/wiki/Socket_AM1 "wikilink") - Fusion APU用のAMDのソケット。[SoCデスクトップ向けAPU用](https://ja.wikipedia.org/wiki/System-on-a-chip "wikilink")。ソケットそのものの名称は「Socket FS1b」である。

#### ハイエンド・デスクトップ (AMD)

  - [Socket TR4](https://ja.wikipedia.org/wiki/Socket_TR4 "wikilink") - Zen および Zen+世代のCPUである [Ryzen](https://ja.wikipedia.org/wiki/Ryzen "wikilink") Threadripper 1000シリーズ および 2000シリーズ用。

  - \- Zen2 世代のCPUである [Ryzen](https://ja.wikipedia.org/wiki/Ryzen "wikilink") Threadripper 3000シリーズ用。

#### モバイル (AMD)

  - Socket A - モバイルDuron,モバイル[Athlon](../Page/Athlon.md "wikilink")4,モバイル [Athlon](../Page/Athlon.md "wikilink") XP,Geode

  - [Socket 563](https://ja.wikipedia.org/wiki/Socket_563 "wikilink") - AMDの省電力モバイル [Athlon](../Page/Athlon.md "wikilink") XP-M（563 個の接点を持つ μ-PGA版Socket A。基板の面積を取らないため主にモバイル用として使用された）。

  - [Socket 754](https://ja.wikipedia.org/wiki/Socket_754 "wikilink")

  - [Socket S1](https://ja.wikipedia.org/wiki/Socket_S1 "wikilink") - DDR2-SDRAM に対応したモバイルプラットフォーム用の AMD のソケット。モバイルプロセッサ用の Socket 754 を置き換えた（638 個の接点の PGA）。

  - \- 将来の、CPU と GPU の機能を持ったノート PC 向けの *Fusion* プロセッサ用（コードネーム *Swift*）。DDR3-SDRAM をサポートする。2009年にリリースされる予定。

  - [Socket FP5](https://ja.wikipedia.org/wiki/Socket_FP5 "wikilink") - モバイル向け [Ryzen](https://ja.wikipedia.org/wiki/Ryzen "wikilink") APU 用ソケット

#### サーバ (AMD)

  - [Socket 940](https://ja.wikipedia.org/wiki/Socket_940 "wikilink") - DDR-SDRAM に対応した AMD のシングル、およびマルチプロセッサ用のソケット。AMD [Opteron](https://ja.wikipedia.org/wiki/Opteron "wikilink")\[16\]（2xx と 8xx シリーズ）, Athlon 64 FX プロセッサに対応する（940 個の接点の PGA）。

  - Socket A

  - [Socket F](https://ja.wikipedia.org/wiki/Socket_F "wikilink")（または "Socket 1207" として知られている） - DDR2-SDRAM をサポートした、AMD のマルチプロセッサ用のソケット。AMD [Opteron](https://ja.wikipedia.org/wiki/Opteron "wikilink")\[17\]（2xxx と 8xxx シリーズ）と Athlon 64 FX プロセッサに対応する。 Socket 940 を置き換え、部分的に Socket F+ と互換性がある（1207 個の接点の [LGA](https://ja.wikipedia.org/wiki/パッケージ_\(電子部品\)#LGA_\(Land_grid_array\) "wikilink")）。

  - [Socket F+](https://ja.wikipedia.org/wiki/Socket_F+ "wikilink") - 最高 2.6 GHz までの高速 [HyperTransport](https://ja.wikipedia.org/wiki/HyperTransport "wikilink") をサポートする、AMD の将来のマルチプロセッサ用のソケット。Socket F を置き換えるが、Socket F 用のプロセッサを後方互換性としてサポートする。

  - プロジェクトコードネーム *[Fusion](https://ja.wikipedia.org/wiki/AMD_Fusion "wikilink")* で開発されている将来のプロセッサは、 と他の 2 つのソケットを使用する。

  - \- Socket F+ の後継であり、サーバのメモリ拡張のための、 とあわせて使用される。

  - [Socket SP3](https://ja.wikipedia.org/wiki/Socket_SP3 "wikilink") - ZenアーキテクチャのサーバーCPUである [EPYC](https://ja.wikipedia.org/wiki/EPYC "wikilink")シリーズのソケット

### その他

  - Socket 463（または [Socket NexGen](https://ja.wikipedia.org/wiki/Socket_NexGen "wikilink") としても知られる） - [NexGen](https://ja.wikipedia.org/wiki/NexGen "wikilink") [Nx586](https://ja.wikipedia.org/wiki/Nx586 "wikilink")

  - Socket 499 - [DEC Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink") [21164a](https://ja.wikipedia.org/wiki/Alpha_21164 "wikilink")

  - Slot B - [DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") [Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")

  - \- ソケット型のプロセッサを、バスが互換のスロット型マザーボードで使用するためのアダプタの[通称](../Page/通称.md "wikilink")。

## 脚注

## 関連項目

  - [CPU製品一覧](https://ja.wikipedia.org/wiki/CPU製品一覧 "wikilink")
  - [CPUバス](https://ja.wikipedia.org/wiki/CPUバス "wikilink")
  - [インテル\#マイクロプロセッサ](https://ja.wikipedia.org/wiki/インテル#マイクロプロセッサ "wikilink")
  - [アドバンスト・マイクロ・デバイセズ\#マイクロプロセッサ](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ#マイクロプロセッサ "wikilink")
  - [パッケージ (電子部品)](../Page/パッケージ_\(電子部品\).md "wikilink")

## 外部リンク

  - [CPU Sockets Chart](http://users.erols.com/chare/sockets.htm) - x86 のソケットと関連する仕様の詳細なリスト。
  - [techPowerUp\! CPU Database](http://www.techpowerup.com/cpudb/)
  - [Processor sockets](http://www.cpu-world.com/Sockets/index.html)

[Category:CPUソケット](https://ja.wikipedia.org/wiki/Category:CPUソケット "wikilink") [Category:CPU](https://ja.wikipedia.org/wiki/Category:CPU "wikilink") [Category:電子部品](https://ja.wikipedia.org/wiki/Category:電子部品 "wikilink") [Category:ハードウェア](https://ja.wikipedia.org/wiki/Category:ハードウェア "wikilink")

1.  8080ソフトウェア互換CPUであるNECのµCOM-8(µPD753)のピン数は42でありピン配置も異なるが、増えた2本のピンはNC（無接続）である。後に8080とピン互換のµCOM-80(µPD8080A)も出た
2.  <http://www.ciao.se/Intel_80186_12_MHz_processor__5790>
3.  <http://www.mwiacek.com/pc.pl/x86/x86.htm#4.2.80286/80287%20Socket%20%2880286/80287%29%7Coutline>
4.  初期には、486用に汎用の17列PGAソケット（3周、接点数168または169（487SXおよびODP用））が使用されたこともある
5.  WB対応486はWB制御のピン配置がP24T（Socket 2および3で486が使用しない最外周を使用）と異なるため専用ソケットが開発され、また、Socket 6用Pentium ODP（Kバージョン）にはピン配置を変換する基板が装着されていた（基板を外すと通常版のP24Tとして使用できる）。IntelDX4用マザーボードの中にはSocket 3を採用し、WB制御の配線をIntelDX4用とP24T用の両方にしてあるものもある（ただし、IntelDX4→P24Tは、インテルは正規のアップグレードパスとしていない）。
6.  この 478 ピンのソケットは、[micro-PGA](https://ja.wikipedia.org/wiki/micro-PGA "wikilink") レイアウトにより Socket 423 よりも物理的サイズを縮小するために導入された。Socket 775 は [PCI Express](https://ja.wikipedia.org/wiki/PCI_Express "wikilink") 、[DDR2](../Page/DDR2_SDRAM.md "wikilink") メモリと [Intel 64](https://ja.wikipedia.org/wiki/x64 "wikilink") (x86-64 のインテルによる実装) をサポートすることで導入されたが、新しい [Land Grid Array](https://ja.wikipedia.org/wiki/パッケージ_\(電子部品\)#LGA_\(Land_grid_array\) "wikilink") レイアウトへの変更も行われた。より良い電気的性能のため、ピンは CPU パッケージでなくソケットの側にある。
7.
8.
9.  [Fudzilla report](http://www.fudzilla.com/index.php?option=com_content&task=view&id=3757&Itemid=1)、2007年10月23日に取得
10. <http://download.intel.com/design/mobile/applnots/24528401.pdf>
11. [インテル次世代ノートPC向けCPU用「ソケットG1,PGA989/988Aソケット](http://www.entamail.com/dempa/show_product_news.php?id=71559)2011年1月19日に取得
12. <http://www.intel.com/cd/channel/reseller/asmo-na/eng/products/server/processors/index.htm> 2011年1月19日に取得
13.
14.
15.
16. これらのソケットは、統合メモリコントローラを持った CPU 向けである。754ピンのモデルは CPU のピンに 1 つのメモリチャンネルがある。939 ピンのモデルは 2 つのメモリチャンネルがあり、ピンの数が増えている。940 ピンのモデルにも 2 つのメモリチャンネルがあるが、レジスタードメモリが必要であり、[SMP](../Page/対称型マルチプロセッシング.md "wikilink") をサポートする。Socket F と AM2 は、[DDR2](../Page/DDR2_SDRAM.md "wikilink") をサポートするために再設計された。Socket F は 1207 ピンを持っている（より高いスケーラビリティと、電力分配の改善のためと推測されるピンが追加）。Socket AM2 は 940 のピンホールを持つが、現行の AMD Opteron プロセッサには対応していない。
17.