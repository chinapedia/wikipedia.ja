> この記事は[PowerPC](https://ja.wikipedia.org/wiki/PowerPC)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:IBM_PowerPC601_PPC601FD-080-2_top.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:PPCA601v5FE1002_01.JPG "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:PPC601FF-090a-2_01.JPG "wikilink")  **PowerPC**（パワーピーシー、）は[1991年](https://ja.wikipedia.org/wiki/1991年 "wikilink")に[アップルコンピュータ](https://ja.wikipedia.org/wiki/アップル_\(企業\) "wikilink")、[IBM](https://ja.wikipedia.org/wiki/IBM "wikilink")、[モトローラ](https://ja.wikipedia.org/wiki/モトローラ "wikilink")の提携（[AIM連合](https://ja.wikipedia.org/wiki/AIM連合 "wikilink")）によって開発された、[RISC](https://ja.wikipedia.org/wiki/RISC "wikilink")タイプの[マイクロプロセッサ](https://ja.wikipedia.org/wiki/マイクロプロセッサ "wikilink")である。

PowerPCは[IBM](https://ja.wikipedia.org/wiki/IBM "wikilink")の[POWERアーキテクチャをベースに開発され](https://ja.wikipedia.org/wiki/POWER_\(マイクロプロセッサ\) "wikilink")、アップルコンピュータの[Macintosh](../Page/Macintosh.md "wikilink")やIBMの[RS/6000](https://ja.wikipedia.org/wiki/RS/6000 "wikilink")などで採用された。[ゲーム機](../Page/ゲーム機.md "wikilink")をはじめとした[組み込みシステム](https://ja.wikipedia.org/wiki/組み込みシステム "wikilink")、[スーパーコンピュータ](https://ja.wikipedia.org/wiki/スーパーコンピュータ "wikilink")で広く使われている。[POWER3](https://ja.wikipedia.org/wiki/POWER3 "wikilink")以降は、POWERファミリ自体がPowerPCアーキテクチャに準拠している。

## 概要

アーキテクチャとして、動作のベースとなる[命令セット](https://ja.wikipedia.org/wiki/命令セット "wikilink")や基本的な[レジスタセット](https://ja.wikipedia.org/wiki/レジスタ_\(コンピュータ\) "wikilink")、[メモリアドレッシング](https://ja.wikipedia.org/wiki/アドレッシングモード "wikilink")、[キャッシュモデルなどを規定しているが](https://ja.wikipedia.org/wiki/キャッシュメモリ "wikilink")、それらをどのように[実装](https://ja.wikipedia.org/wiki/実装 "wikilink")すべきかまでは規定していない。

そのため実際に製造されるモデルは高速化のためにアーキテクチャレベルでは規定されていない機構（L2、L3キャッシュや関連レジスタなど）を備えているのが普通である。

性能の割に低消費電力でダイサイズも小さいという特性から、[ゲーム機](../Page/ゲーム機.md "wikilink")やハイエンドの[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")などのネットワーク機器、[レーザープリンター](https://ja.wikipedia.org/wiki/レーザープリンター "wikilink")などの分野で広く使われており、高性能な[組み込みシステム](https://ja.wikipedia.org/wiki/組み込みシステム "wikilink")向けプロセッサとしてよく使われる。[FPGA](https://ja.wikipedia.org/wiki/FPGA "wikilink")用の[IPコア](https://ja.wikipedia.org/wiki/IPコア "wikilink")として提供されているものもある。もともとはAIMプラットフォームの[CPU](https://ja.wikipedia.org/wiki/CPU "wikilink")という意味で開発されたものだが、CPU以外は開発されなかったため、今日まで残る同プロジェクト唯一の成果物でもある。

デスクトップコンピュータ用としては、[アップルコンピュータの](https://ja.wikipedia.org/wiki/アップル_\(企業\) "wikilink")[Power Macintoshおよび](https://ja.wikipedia.org/wiki/Power_Macintosh "wikilink")[Power Macに採用されていたほか](https://ja.wikipedia.org/wiki/Power_Mac "wikilink")、[IBM](https://ja.wikipedia.org/wiki/IBM "wikilink") の一部の[ワークステーション](https://ja.wikipedia.org/wiki/ワークステーション "wikilink")、[サーバ](https://ja.wikipedia.org/wiki/サーバ "wikilink")や[BlueGene/Lをはじめとする](https://ja.wikipedia.org/wiki/Blue_Gene "wikilink")[スーパーコンピュータ](https://ja.wikipedia.org/wiki/スーパーコンピュータ "wikilink")にも採用されている。その他、2005〜2006年に発売された主要据え置き型ゲーム機三機種（[Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")、[PLAYSTATION 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")、[Xbox 360](https://ja.wikipedia.org/wiki/Xbox_360 "wikilink")）は、いずれもPowerPCアーキテクチャを採用している。

現在、PowerPCプロセッサはモトローラから半導体部門を分離して設立された[フリースケール・セミコンダクタ](https://ja.wikipedia.org/wiki/フリースケール・セミコンダクタ "wikilink")(現在は[NXP](https://ja.wikipedia.org/wiki/NXPセミコンダクターズ "wikilink"))と[IBM](https://ja.wikipedia.org/wiki/IBM "wikilink")が開発・製造を行っており、PowerPC派生品種の[CellプロセッサはIBMと](https://ja.wikipedia.org/wiki/Cell_Broadband_Engine "wikilink")[東芝](https://ja.wikipedia.org/wiki/東芝 "wikilink")セミコンダクターが設計・製造している。また、4xx のシリーズ（組込み系CPUコア）は [AMCC](https://ja.wikipedia.org/wiki/アプライド・マイクロ・サーキット "wikilink") に売却されている。しかし実際は4xx シリーズでもハイエンドクラスの製造はIBMしか行えないため、開発の中心はIBMのままである。

## 設計特徴

PowerPCは[RISC](https://ja.wikipedia.org/wiki/RISC "wikilink")の思想で作られており、[スーパースカラ](https://ja.wikipedia.org/wiki/スーパースカラ "wikilink")方式で命令を実行する。

ベースにした[POWERの特徴に](https://ja.wikipedia.org/wiki/POWER_\(マイクロプロセッサ\) "wikilink")、さらにいくつかの変更を加えた。

  - POWER[アーキテクチャのうち](../Page/コンピュータ・アーキテクチャ.md "wikilink")、複雑なものを省いた命令セット。RISCプロセッサとしては、比較的複雑な命令も含む。
  - バイエンディアン（[ビッグエンディアン](https://ja.wikipedia.org/wiki/ビッグエンディアン "wikilink")および[リトルエンディアン](https://ja.wikipedia.org/wiki/リトルエンディアン "wikilink")のサポート。G5を除く）
  - [単精度](https://ja.wikipedia.org/wiki/単精度 "wikilink")[浮動小数点演算に](https://ja.wikipedia.org/wiki/浮動小数点数 "wikilink")[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink")浮動小数点演算の追加
  - 32[ビット](https://ja.wikipedia.org/wiki/ビット "wikilink")[命令と完全](https://ja.wikipedia.org/wiki/命令_\(コンピュータ\) "wikilink")[下位互換](https://ja.wikipedia.org/wiki/下位互換 "wikilink")の64ビット[命令セット](https://ja.wikipedia.org/wiki/命令セット "wikilink")
  - 32個のGPR（汎用[レジスタ](https://ja.wikipedia.org/wiki/レジスタ_\(コンピュータ\) "wikilink")）と32個のFPR（[浮動小数点レジスタ](https://ja.wikipedia.org/wiki/浮動小数点数 "wikilink")）
  - [サブルーチン](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")の[呼出規約](https://ja.wikipedia.org/wiki/呼出規約 "wikilink")は一般的なRISCチップとは異なり[スタック渡しである](https://ja.wikipedia.org/wiki/レジスタ_\(コンピュータ\)#サブルーチン "wikilink")。実際は10個の引数まで[レジスタ渡しが行われるが](https://ja.wikipedia.org/wiki/呼出規約#Register_\(fastcall\) "wikilink")、データのビット数によっては使用可能なレジスタ数が減少したり、非揮発性レジスタの退避などを行う必要がある。
  - 1本のカウントレジスタ。専用の分岐命令などと組み合わせてループのカウントなどに利用する。
  - 複雑な命令など一部を除き、命令は基本的に[ハードワイヤード (Hard-Wired) ロジックで実装](https://ja.wikipedia.org/wiki/ワイヤードロジック "wikilink")（一部[マイクロコード](https://ja.wikipedia.org/wiki/マイクロコード "wikilink")で実装）
  - G4（第4世代）シリーズでは128ビット単位で[ベクトル演算](https://ja.wikipedia.org/wiki/ベクトル演算 "wikilink")を行う『[AltiVec](https://ja.wikipedia.org/wiki/AltiVec "wikilink")（IBMはVMX、[アップルコンピュータではVelocity](https://ja.wikipedia.org/wiki/アップル_\(企業\) "wikilink") Engineと表現している）』を採用。付随する専用のレジスタは32本。
  - 8本の4ビット条件レジスタ(いわゆる[ステータスレジスタ](https://ja.wikipedia.org/wiki/ステータスレジスタ "wikilink")やフラグレジスタと呼ばれるもの)。詳細はステータスレジスタの項を参照。
  - 原則として、現在のスタックのメモリアドレスを指す[ベースポインタを持たない](https://ja.wikipedia.org/wiki/レジスタ_\(コンピュータ\) "wikilink")。代りに汎用レジスタの一つを用いる。この規則は[ABIに依存するが](https://ja.wikipedia.org/wiki/Application_Binary_Interface "wikilink")、大抵の場合そのレジスタは1番の汎用レジスタである。また、0番の汎用レジスタは、命令によってはゼロレジスタの代用として用いられることがある。
  - 静的な[分岐予測](https://ja.wikipedia.org/wiki/分岐予測 "wikilink")を命令単位で設定できる。
  - 条件分岐命令は8×32×17=4352通り(分岐予測を含む)の条件を組み合わせることが可能である。

1998年のPOWER3以降は、POWERも64ビットPowerPC仕様に準拠したアーキテクチャを採用している。

## 歴史

PowerPC の歴史は70年代後半の[ジョン・コック](https://ja.wikipedia.org/wiki/ジョン・コック "wikilink")の[RISC](https://ja.wikipedia.org/wiki/RISC "wikilink")アイデアを使用した米 [IBM](https://ja.wikipedia.org/wiki/IBM "wikilink")の[801](https://ja.wikipedia.org/wiki/IBM_801 "wikilink")[プロトタイプ](https://ja.wikipedia.org/wiki/プロトタイプ "wikilink")・チップで始まった。801を基にしたコアは数々のIBM製組み込み用製品に採用され、最終的には16本の[レジスタを持つ](https://ja.wikipedia.org/wiki/レジスタ_\(コンピュータ\) "wikilink")[ROMP](https://ja.wikipedia.org/wiki/ROMP "wikilink")プロセッサ、[IBM RTにまで発展した](https://ja.wikipedia.org/wiki/IBM_RT "wikilink")。しかし、RTプロセッサの性能は十分とは言えなかったため、IBMは「アメリカ・プロジェクト」と呼ばれる、市場で最も高速なプロセッサを開発する計画を始動させた。その結果開発されたのがPOWERアーキテクチャであり、[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")初頭に[RISC System/6000と共に発表された](https://ja.wikipedia.org/wiki/RS/6000 "wikilink")。

本来のPOWERマイクロプロセッサは、スーパースケーラを実現した最初のプロセッサの一つであり、高性能で[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")に対応していた。IBMがRS/6000の製品群を[ローエンド](https://ja.wikipedia.org/wiki/ローエンド "wikilink")向けから[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")向け製品にまで拡大するにあたって、POWERプロセッサからいくつかの機構を取り除き、シングルチップ・プロセッサにする必要が生じたため、IBMは[RISC Single Chip](https://ja.wikipedia.org/wiki/RISC_Single_Chip "wikilink")（RSC）の開発に着手した。RSCは開発の初期段階から、工業向けに幅広く使える可能性を秘めた高機能なプロセッサになるであろうと考えられていた。

[1991年](https://ja.wikipedia.org/wiki/1991年 "wikilink")、IBMはアップルコンピュータに接近し、共同でPOWERアーキテクチャをベースとしたシングルチップ・マイクロプロセッサの開発を行なう事で合意した。その直後、当時据え置き型コンピュータ用プロセッサに関してモトローラ社最大の顧客であったアップルコンピュータは、長年の協力関係を考慮して、モトローラにマイクロプロセッサ開発に加わるよう打診した。モトローラには、マイクロプロセッサ開発における豊富な経験の活用と、[セカンドソース](https://ja.wikipedia.org/wiki/セカンドソース "wikilink")としての役割が期待された。こうしてIBM、アップルコンピュータ、モトローラは**AIM連合**と呼ばれる協力関係を組織するに至った。

1991年、PowerPCはAIM連合における最大要素の一つとなった。当時の[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")市場では[マイクロソフト](https://ja.wikipedia.org/wiki/マイクロソフト "wikilink")が[Windowsを開発中であり](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")製プロセッサはその支配を強めつつあった。また、[CISC](https://ja.wikipedia.org/wiki/CISC "wikilink")アーキテクチャのインテル[80386及び](../Page/Intel_80386.md "wikilink")[80486が大半のコンピュータに採用されており](https://ja.wikipedia.org/wiki/Intel486 "wikilink")、後継の[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")プロセッサの開発も順調に進んでいた。PowerPCプロセッサは冒険的な要素を含んでいたものの、拡大するマイクロソフトとインテルによる支配に対抗するため、開発が進められた。

モトローラにとって、POWER系プロセッサの開発に加わる事は、またとないチャンスであった。この時点でモトローラは既に自社製のRISCプロセッサ[MC88000](https://ja.wikipedia.org/wiki/MC88000 "wikilink")を市場に投入していた。しかし、このプロセッサは貧弱な設計手法と製造上の問題により市場での評価は低く、販売は低迷していた。このためモトローラは、[MIPS](https://ja.wikipedia.org/wiki/MIPS "wikilink")や[SPARC](https://ja.wikipedia.org/wiki/SPARC "wikilink")といった競合製品に市場で並ぶ機会を失いつつあった。しかし、新型POWER系プロセッサの開発に参加すれば、キャッシュ部分を設計するだけで、広くテストされた高性能RISCプロセッサを販売する事が可能になるため、RISCプロセッサ市場での巻き返しが期待された。また、重要な顧客であるアップルコンピュータとの関係の改善や、IBMに簡略化バージョンを供給できる可能性もあった。

その低評価の一方で、MC88000プロセッサは既に生産されており、アップルコンピュータは既にこのプロセッサを利用したプロトタイプのコンピュータを動作させていた。このため、開発中のPOWERアーキテクチャ・シングルチップのバスにハードウェアの段階でMC88000のバスとの互換性を持たせれば、[ロジックボード](https://ja.wikipedia.org/wiki/ロジックボード "wikilink")を再設計する事なく、より迅速に新型プロセッサを市場に投入する事が可能であった。最終的に、新型プロセッサPowerPCはこういった要求を含んだ設計となった。

PowerPCが市場に投入される直前、大きな動きがあった。アップルコンピュータに加えてIBMとモトローラの両社は、PowerPCプロセッサに対応したシステムを提案した。マイクロソフトはモトローラのPowerPCサーバ向けの[Windows NT](https://ja.wikipedia.org/wiki/Microsoft_Windows_NT "wikilink") 3.51を発表、[サン・マイクロシステムズ](https://ja.wikipedia.org/wiki/サン・マイクロシステムズ "wikilink")も[Solaris](https://ja.wikipedia.org/wiki/Solaris "wikilink")のPowerPC版を発表した。またIBMは、自社の[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")を移植し、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")の移植も計画していた。1994年には組込み用途向けに PowerPC 403 を発表、後継のPowerPC 401、440などは機器制御用途やネットワーク機器を中心に広く普及した。また同年にPowerPCの[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")版であるPowerPC 620が完成、同チップは出荷されず普及はしなかったが、その設計はPOWER3以降のPOWERファミリの礎となった。

1994年にはPowerPCをベースとしたコンピュータの仕様である**[PReP](https://ja.wikipedia.org/wiki/PReP "wikilink")**、1995年には後継の**[CHRP](https://ja.wikipedia.org/wiki/CHRP "wikilink")**が発表された。また[1994年](https://ja.wikipedia.org/wiki/1994年 "wikilink")にはPowerPC搭載のMacintosh (**[Power Macintosh](https://ja.wikipedia.org/wiki/Power_Macintosh "wikilink")**) が登場した。

しかしこれらの動きはわずかな期間で終わり、結局PowerPCという新型アーキテクチャに期待されていた理想が実現する事はなかった。Windows、OS/2、そしてサンの顧客はPowerPC用ソフトウェアの不足を理由に、PowerPCプロセッサはほとんど顧みなかった。これらのOSの後継が市場に投入される事はなく、PowerPCから完全に離れていった。また[BeOS](https://ja.wikipedia.org/wiki/BeOS "wikilink")も最初のバージョンはPowerPC向けに開発されたが、その後x86系プロセッサに移行していった。最終的にはPowerPC向けの商用のデスクトップOSは、アップルの[Classic Mac OSと](../Page/Classic_Mac_OS.md "wikilink")[Mac OS Xのほかは](https://ja.wikipedia.org/wiki/macOS "wikilink")、[AmigaOS](https://ja.wikipedia.org/wiki/AmigaOS "wikilink")などのみが残った。

1990年代中頃、PowerPCプロセッサはベンチマークにおいて、最速の[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")系プロセッサと同等または凌駕する性能を発揮した。90年代末に登場したG4では[AltiVec](https://ja.wikipedia.org/wiki/AltiVec "wikilink")を搭載し、当時の他のCPUに比較して大幅に高速な[SIMD](https://ja.wikipedia.org/wiki/SIMD "wikilink")処理を実現した。PowerPCは高性能でありながら低コスト・低消費電力といった特徴をもち、アップルはPowerPC603およびG3・G4を採用することによって、同時期のPC/AT互換ノートパソコンの性能を凌駕する[PowerBook](https://ja.wikipedia.org/wiki/PowerBook "wikilink")や、[ファンレスの](https://ja.wikipedia.org/wiki/CPUの冷却装置 "wikilink")[iMac](https://ja.wikipedia.org/wiki/iMac "wikilink")、[Power Mac G4 Cubeといった独創的な製品を作ることが可能になった](https://ja.wikipedia.org/wiki/Power_Mac_G4_Cube "wikilink")。しかしPowerPCの性能あたりの消費電力の低さは、組み込み向けとしては高く評価されたものの、デスクトップで勢力を拡大するための決め手にはならなかった。

[2002年](../Page/2002年.md "wikilink")にはPOWER4をベースとした[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")の[PowerPC 970](https://ja.wikipedia.org/wiki/PowerPC_970 "wikilink") (G5)が登場、高性能化に伴いG4から大幅に消費電力が増大したものの、同時期の[Pentium 4と比較するとほぼ同等の性能でありながら低消費電力であり](https://ja.wikipedia.org/wiki/Pentium_4 "wikilink")、IBM・アップルのサーバ製品のほか、[Power Mac](https://ja.wikipedia.org/wiki/Power_Mac "wikilink") G5・iMac G5で採用された。

[2004年](https://ja.wikipedia.org/wiki/2004年 "wikilink")はPowerPC系[CPU](https://ja.wikipedia.org/wiki/CPU "wikilink")にとって激動の年になった。まず、モトローラが、半導体部門をスピンオフし、『[フリースケール・セミコンダクタ](https://ja.wikipedia.org/wiki/フリースケール・セミコンダクタ "wikilink")』を設立。次に、2005年度の[E3において発表された各社の次世代ゲーム機レボリューション](https://ja.wikipedia.org/wiki/Electronic_Entertainment_Expo "wikilink")（コードネーム、現在の[Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")）、[PLAYSTATION 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")、[Xbox 360](https://ja.wikipedia.org/wiki/Xbox_360 "wikilink")）のCPUがすべてPowerPC系アーキテクチャのものになった。一方で、これまでPowerPCを採用していたアップルコンピュータの[Macintosh](../Page/Macintosh.md "wikilink")が、2006年から[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")社のCPUに全面的に切り替えていく事が発表された。2006年中にアップルのハードウェアは完全にインテルアーキテクチャへの切り替えが完了し、アップル社内でPowerPC向け[チップセット](https://ja.wikipedia.org/wiki/チップセット "wikilink")の開発を行っていた設計チームは[Apple A4の開発に転じた](https://ja.wikipedia.org/wiki/Apple_A4 "wikilink")。2009年にはセキュリティアップデートを除いてPowerPC向けソフトウェアの開発も終了した。

現在ではゲーム機、プリンター・ルータ・ネットワークスイッチ等の組み込み用途のほか、サーバやスーパーコンピュータに採用されている。

## PowerPCのプロセッサ

### POWER改修系 (G1)

PowerPCファミリを立ち上げる為に、[IBM](https://ja.wikipedia.org/wiki/IBM "wikilink")の既存の[POWER](https://ja.wikipedia.org/wiki/POWER_\(マイクロプロセッサ\) "wikilink")[プロセッサをベースに設計された](https://ja.wikipedia.org/wiki/CPU "wikilink")。その為、正式にはPowerPCのジェネレーション・ナンバーを持っていない。1994年代より流通。

  - [PowerPC 601](https://ja.wikipedia.org/wiki/PowerPC_601 "wikilink") - 50,66,80,90MHz、POWER[命令も実装](https://ja.wikipedia.org/wiki/命令_\(コンピュータ\) "wikilink")
      - PowerPC 601+ - 外部[バスの](https://ja.wikipedia.org/wiki/バス_\(コンピュータ\) "wikilink")3倍[クロック](https://ja.wikipedia.org/wiki/クロック "wikilink")で動作、低電源電圧化 (+2.5V) 100, 110, 120MHz
  - PowerPC 602 - 低価格版　[3DO](https://ja.wikipedia.org/wiki/3DO "wikilink")の後継機『[M2](https://ja.wikipedia.org/wiki/3DO_M2 "wikilink")』に採用される予定だった。『M2』をベースとした[コナミ](https://ja.wikipedia.org/wiki/コナミ "wikilink")の[業務用ゲーム基板に使用された](https://ja.wikipedia.org/wiki/アーケードゲーム基板 "wikilink")。

### G2

[thumb](https://ja.wikipedia.org/wiki/ファイル:XPC603EFE100LF_01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:XPC603PRX200LC_01.jpg "wikilink") アルミ配線の603、604がG2第1世代。第2世代については、IBMによる銅配線の603eと604e全てが該当するとする文献と、同シリーズで250MHz以上のものとする文献が散見され、はっきりしない。どちらも完全バス互換であったため、区別が重要でなかったこともその理由である。PowerPC 603は大変消費電力が少なく、デスクトップと同様の仕様のチップがノートパソコンに搭載されたほか、組み込み向けに広く使われた。PowerPC 604は4つの演算ユニットを並列動作させることができ、パーソナルコンピュータ向けとしては当時最高レベルの演算性能を持っていた。浮動小数点演算は特に強力であった。

  - [PowerPC 603](https://ja.wikipedia.org/wiki/PowerPC_603 "wikilink") - 低消費電力
      - PowerPC 603e - 低消費電力、高速版
      - PowerPC 603ev - PowerPC 603eの高速版
  - [PowerPC 604](https://ja.wikipedia.org/wiki/PowerPC_604 "wikilink") - [SMP対応](https://ja.wikipedia.org/wiki/対称型マルチプロセッシング "wikilink")、インラインL2キャッシュ、高速な浮動小数点演算
      - PowerPC 604e - 604の低消費電力、小型高速版
      - PowerPC 604ev - 604eの低消費電力、小型高速版
  - PowerPC 615 - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")とPowerPC命令の両立を目指したプロセッサ。[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")互換ソケット に装着可能。x86プロセッサとしては当時のPentiumなどに対抗できる性能を有すと見込まれたが、命令の切り替えの際の性能の低下が激しい、ダイサイズが330mmとPower PC系にしては大きい、マイクロソフトなどがサポートしない公算が大きかったなどの理由により開発中止になった。
  - PowerPC 620 - 64ビット版。その設計はPOWER3に引き継がれる

[thumb](https://ja.wikipedia.org/wiki/ファイル:PPC750CXEHP55-3_01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:GEKKO.jpg "wikilink")

### X704

アップルが出資していた[Exponential Technologyによる](https://ja.wikipedia.org/wiki/:en:Exponential_Technology "wikilink")[バイポーラトランジスタ](https://ja.wikipedia.org/wiki/バイポーラトランジスタ "wikilink")型の論理回路を使う消費電力の大きなハイパフォーマンスなCPUとして発表された、1996年当時の他のCPUに比べ大幅な高速クロック動作を実現するとしていたPowerPCアーキテクチャの予定製品であった。試作品が搭載された次期[Power Macintoshプロトタイプ](https://ja.wikipedia.org/wiki/Power_Macintosh "wikilink")\[1\]が展示会でAppleによって公開された\[2\]\[3\]。しかし、1997年5月のWWDC時、安価なPowerPC 750やPowerPC 604evとの性能差がないとして、Power Macintoshへの採用が中止された為にX704は量産化されずに終った\[4\]\[5\]。

### G3

G3（第3世代）以降は、PowerPC採用の代表的製品である[Power Macintoshシリーズでアップルがジェネレーション](https://ja.wikipedia.org/wiki/Power_Macintosh "wikilink")・ナンバーを前面に押し出したため、PowerPCの世代区分が一般に明確となった。性能比での消費電力が低いことが特徴で、現在では主に[組み込み用途に用いられる](https://ja.wikipedia.org/wiki/組み込みシステム "wikilink")。なお、パイプラインは浅く、603と変わらない4段にすぎない。

  - PowerPC 75x,74x - [PowerPC G3シリーズと呼ばれる](https://ja.wikipedia.org/wiki/PowerPC_G3 "wikilink")。603eの発展系。
    1.  PowerPC 75xにはバックサイド[キャッシュを採用](https://ja.wikipedia.org/wiki/キャッシュメモリ "wikilink")
    2.  整数演算ユニットを2基に
    <!-- end list -->
      - PowerPC 750L -750の銅配線版
      - PowerPC 750CX/CXe -256KB L2キャッシュを内蔵
      - PowerPC 750FX/FL -130nm [SOI](https://ja.wikipedia.org/wiki/SOI "wikilink")で製造、L2キャッシュ512KB
      - PowerPC 750GX -90nm SOIで製造、〜1.1GHz、200MHz FSB対応、L2キャッシュ1MB
      - PowerPC 750CL -L2キャッシュ256KB、400MHz〜1GHz、PowerPC 750GXの約半分まで省電力化されている
  - [Gekko](https://ja.wikipedia.org/wiki/Gekko "wikilink") - [ニンテンドーゲームキューブ](https://ja.wikipedia.org/wiki/ニンテンドーゲームキューブ "wikilink")用に開発されたもの。PowerPC 750CXeをベースに、浮動小数点演算が強化され、[SIMD](https://ja.wikipedia.org/wiki/SIMD "wikilink")命令が追加されている
  - [Broadway](https://ja.wikipedia.org/wiki/Broadway_\(マイクロプロセッサ\) "wikilink") - 90nm SOIで製造、任天堂の[Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")用に開発されたもの。Gekko互換であり、PowerPC 750CLがベースと思われるが詳細は非公開。
  - [Espresso](https://ja.wikipedia.org/wiki/Espresso "wikilink") - 45nm SOIで製造、任天堂の[Wii U用に開発されたもの](https://ja.wikipedia.org/wiki/Wii_U "wikilink")。専用GPUとのMCMに対応したマルチコアCPUで、Broadwayがベースと思われるが詳細は非公開。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Motorola_XPC7400RX400TK_top.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:XPC7455_01.jpg "wikilink")

### G4

G3をベースに浮動小数点演算機能を強化、SIMDと[対称型マルチプロセッサ機能を追加したもの](https://ja.wikipedia.org/wiki/対称型マルチプロセッシング "wikilink")。CPUバスは従来の60xバスに加え、より高度な制御機能をもったMPXバスにも対応している。MPC 7450 でマイクロアーキテクチャを刷新したため、MPC 745x・MPC 744x は、**G4+**とも呼ばれる。

  - MPC 74xx - [G4シリーズと呼ばれる](https://ja.wikipedia.org/wiki/PowerPC_G4 "wikilink")。[モトローラ](https://ja.wikipedia.org/wiki/モトローラ "wikilink")および[フリースケール・セミコンダクタ](https://ja.wikipedia.org/wiki/フリースケール・セミコンダクタ "wikilink")が開発。
    1.  AltiVec (Velocity Engine) 搭載
    2.  [CPUバス](https://ja.wikipedia.org/wiki/CPUバス "wikilink")にMPXバス (MaxBus) 採用
    3.  SMP対応
    4.  浮動小数点演算を強化
    <!-- end list -->
      - MPC 7400
          - MPC 7410 - 省電力版。180nmプロセスで製造。
      - MPC 7450 - L2キャッシュ256KB内蔵、L3キャッシュ対応、整数演算ユニットを4基に、[パイプラインを](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")7段に多段化し、高クロック化
          - MPC 7451 - 省電力版
          - MPC 7445 - 7455のL3キャッシュインターフェース省略タイプ。
          - MPC 7455 - 180 nmプロセス、SOIを採用。クロックは1GHzに到達。
          - MPC 7457 - 130nm プロセス、L2キャッシュを512KBに
          - MPC 7447 - 7457のL3キャッシュインターフェース省略タイプ。省電力。
          - MPC 7448 - 90nmプロセスで製造、1MBのL2キャッシュ、e600コアを採用。
          - MPC 8641 - e600コアを採用。メモリコントローラ、[PCI Expressコントローラを内蔵](https://ja.wikipedia.org/wiki/PCI_Express "wikilink")。
          - MPC 8641D - MPC 8641のデュアルコア版。

### G5

64ビットPowerPCアーキテクチャに準拠し、設計を全面的に刷新している。

  - [PowerPC 970](https://ja.wikipedia.org/wiki/PowerPC_970 "wikilink") - IBMがアップルと共同開発し、POWER4ベースに設計。[G5と呼ばれる](https://ja.wikipedia.org/wiki/PowerPC_970 "wikilink")。
    1.  [64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")化
    2.  パイプラインを大幅に多段化し高[クロック](https://ja.wikipedia.org/wiki/クロック "wikilink")動作(最高2GHz以上、パイプライン段数16〜25段)
    3.  CPUバスを大幅に高速化（1GHz超）
    4.  2基の[FPU](https://ja.wikipedia.org/wiki/FPU "wikilink")（G4までは1基）を搭載し、高速な[浮動小数点演算](https://ja.wikipedia.org/wiki/浮動小数点数 "wikilink")（スカラ4G[FLOPS](https://ja.wikipedia.org/wiki/FLOPS "wikilink")+単精度ベクタ8GFLOPS\[1GHz動作時\]）
    5.  AltiVec互換のVMXを搭載
    6.  2基のロード／ストアユニット（G4までは1基）
    7.  複雑な命令を[マイクロコード](https://ja.wikipedia.org/wiki/マイクロコード "wikilink")として実装
    8.  フル精度の平方根をハードウェア命令として実装（G4はソフトウェア関数）。
    9.  [リトルエンディアン](https://ja.wikipedia.org/wiki/リトルエンディアン "wikilink")に対応せず

<!-- end list -->

  -   - PowerPC 970FX - 90nmプロセス、高速化。省電力機能「PowerTune」を搭載。
      - PowerPC 970MP - [デュアルコア](https://ja.wikipedia.org/wiki/マルチコア "wikilink")、各コアにL2キャッシュ1MB内蔵。最高2.5GHz。
      - PowerPC 970GX - PowerPC 970FXの後継モデルで、970MP同等の性能でシングルコア・省電力を実現した。最高2.5GHz。

<!-- end list -->

  - PWRficient PA6T - [P.A. Semi](https://ja.wikipedia.org/wiki/P.A._Semi "wikilink")（2008年にアップルに買収された）が設計した、64ビット対応のG5互換製品。
    1.  徹底的な[クロックゲーティング](https://ja.wikipedia.org/wiki/クロックゲーティング "wikilink")（チップ全体を2万5340の要素に分けて[クロック](https://ja.wikipedia.org/wiki/クロック "wikilink")の供給を行う）により、省電力（2GHz、2コアで平均消費電力13W）を実現
    2.  [マルチコア](https://ja.wikipedia.org/wiki/マルチコア "wikilink")接続用のCONEXIUMバスを搭載
    3.  AltiVec互換のVMXを搭載
    4.  バイエンディアンに対応

### Cell

  - [PPE](https://ja.wikipedia.org/wiki/Cell_Broadband_Engine#PowerPC_Processor_Element "wikilink") - PowerPC Processor Elementの略称、SCE・ソニー・IBM・東芝の4社連合によって開発。PowerPC互換ではあるが、どのベースにも属さないフロムスクラッチ。[Cell/B.E.および](https://ja.wikipedia.org/wiki/Cell_Broadband_Engine "wikilink")[PowerXCell 8iに使用されている](https://ja.wikipedia.org/wiki/PowerXCell#PowerXCell_8i "wikilink")。
    1.  VMX拡張付き64ビットのPOWERアーキテクチャを継承した2命令同時発行のRISCプロセッサ
    2.  深いパイプラインとインオーダー実行など回路を簡略化することにより高[クロック](https://ja.wikipedia.org/wiki/クロック "wikilink")動作（最高4GHz以上、パイプライン段数19段以上）
    3.  PowerPC ISA v.2.02に準拠
    4.  2スレッドの[同時マルチスレッディング](https://ja.wikipedia.org/wiki/同時マルチスレッディング "wikilink")
    5.  仮想化機構のサポート
    6.  リアルタイム性を保障するL2キャッシュ
    7.  [リトルエンディアン](https://ja.wikipedia.org/wiki/リトルエンディアン "wikilink")にはハードウェア変換で対応

<!-- end list -->

  - [Xenon](https://ja.wikipedia.org/wiki/Xenon_\(マイクロプロセッサ\) "wikilink") - [Xbox 360用にIBMがマイクロソフトと共同開発したプロセッサ](https://ja.wikipedia.org/wiki/Xbox_360 "wikilink")。PPEの派生モデル。XCPUと呼ばれる。後にGPU「Xenos」を統合したXCGPU、更にeDRAMを統合したObanに発展した。
    1.  PPEをベースにすることで開発期間を短縮
    2.  3つの対称型マルチコアプロセッサ
    3.  ゲームやグラフィックス用に拡張されたVMX128
    4.  1MBの共有L2キャッシュ
    5.  21.6GB/sのFSB

### 4xx

最初から組込み向けとしてIBMが開発。現在は[AMCCが権利を持つ](https://ja.wikipedia.org/wiki/アプライド・マイクロ・サーキット "wikilink")。単体のマイクロプロセッサとしてではなく、[ASIC](https://ja.wikipedia.org/wiki/ASIC "wikilink")のCPUコアとして組み込まれることが多い。2005年頃より流通。

  - 405 シリーズ
      - PowerPC NPe405H
      - PowerPC 405EP
      - PowerPC 405EX
      - PowerPC 405EXr
      - PowerPC 405GP
      - PowerPC 405GPr

<!-- end list -->

  - 440 シリーズ
      - PowerPC 440EP
      - PowerPC 440EPx
      - PowerPC 440GR
      - PowerPC 440GRx
      - PowerPC 440GX
      - PowerPC 440SP
      - PowerPC 440SPe

<!-- end list -->

  - 460 シリーズ
      - PowerPC 460EX
      - PowerPC 460GT
      - PowerPC 460SX
      - PowerPC 460GTx

### 470シリーズ

2009年9月24日に発表された470シリーズは、それまでの400シリーズと比較して性能を２倍以上に引上げた。ソフトウェアは400シリーズと共通であるが、464FPと比較してパイプラインが7段から9段へ増えており、out-of-order、倍精度浮動小数点数演算対応SIMDと、[PowerPC G3](https://ja.wikipedia.org/wiki/PowerPC_G3 "wikilink") (PowerPC750) シリーズの後継シリーズとしての位置づけとなっている。

  - PowerPC 476FP 12S -45nm SOIで製造。1.6GHz時に1.6Wで動作する。倍精度浮動小数点数演算対応SIMD命令、単精度2並列SIMD命令に対応。最高2GHz。

### PowerPC A2

2010年2月9日にISSCC2010で発表されたプロセッサ\[6\]。1コアあたり4スレッドで16コア1チップで構成されている。L1キャッシュ16KB+16KB。L2キャッシュ2MB。1.6GHz時55W、204.8Gflops。最高2.3GHz、65Wで稼動する。[スーパーコンピュータ](https://ja.wikipedia.org/wiki/スーパーコンピュータ "wikilink")[Blue Gene](https://ja.wikipedia.org/wiki/Blue_Gene "wikilink")/Q（ブルージーンQ）のコアCPUに採用されている。

## 使用製品

  - [IBM POWER](https://ja.wikipedia.org/wiki/POWER_\(マイクロプロセッサ\) "wikilink") - [IBM](https://ja.wikipedia.org/wiki/IBM "wikilink")の主に[UNIX](../Page/UNIX.md "wikilink")[サーバ](https://ja.wikipedia.org/wiki/サーバ "wikilink")および[ワークステーション](https://ja.wikipedia.org/wiki/ワークステーション "wikilink")用の[CPU](https://ja.wikipedia.org/wiki/CPU "wikilink")。
  - 組み込み向け派生品
      - [MPC5xx](https://ja.wikipedia.org/wiki/MPC5xx "wikilink")
      - [PowerQUICC](https://ja.wikipedia.org/wiki/PowerQUICC "wikilink")
  - [Macintosh](../Page/Macintosh.md "wikilink") - [アップルコンピュータの](https://ja.wikipedia.org/wiki/アップル_\(企業\) "wikilink")[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")。[Power Macintoshおよび](https://ja.wikipedia.org/wiki/Power_Macintosh "wikilink")[Power Mac](https://ja.wikipedia.org/wiki/Power_Mac "wikilink")、[iBook](https://ja.wikipedia.org/wiki/iBook "wikilink")、1995年以降の[PowerBook](https://ja.wikipedia.org/wiki/PowerBook "wikilink")、2005年までの[iMac](https://ja.wikipedia.org/wiki/iMac "wikilink")。
  - 使用[ゲーム機](../Page/ゲーム機.md "wikilink")
      - [ピピンアットマーク](https://ja.wikipedia.org/wiki/ピピンアットマーク "wikilink")（[バンダイ](https://ja.wikipedia.org/wiki/バンダイ "wikilink")・デジタル・エンタテイメント）。PowerPC 603 66MHzを使用。
      - [セガ](https://ja.wikipedia.org/wiki/セガ "wikilink") [MODEL3](https://ja.wikipedia.org/wiki/MODEL3 "wikilink") アーケードゲーム基板。基板リビジョンによって使用CPUは異なり、PowerPC 603 66MHz、100MHz、PowerPC 603ev 166 MHzを使用。
      - [PlayStation 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")（[ソニー・コンピュータエンタテインメント](https://ja.wikipedia.org/wiki/ソニー・コンピュータエンタテインメント "wikilink")）。[東芝](https://ja.wikipedia.org/wiki/東芝 "wikilink")と共同開発したPowerPC系プロセッサ「[Cell](https://ja.wikipedia.org/wiki/Cell_Broadband_Engine "wikilink")」を使用。
      - [Xbox 360](https://ja.wikipedia.org/wiki/Xbox_360 "wikilink")（[マイクロソフト](https://ja.wikipedia.org/wiki/マイクロソフト "wikilink")）。PowerPC系トリプルコアプロセッサを使用。
      - [ニンテンドーゲームキューブ](https://ja.wikipedia.org/wiki/ニンテンドーゲームキューブ "wikilink")、[Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")、[Wii U](https://ja.wikipedia.org/wiki/Wii_U "wikilink")（[任天堂](../Page/任天堂.md "wikilink")）。PowerPC系プロセッサ「[Gekko](https://ja.wikipedia.org/wiki/Gekko "wikilink")」「[Broadway](https://ja.wikipedia.org/wiki/Broadway_\(マイクロプロセッサ\) "wikilink")」「[Espresso](https://ja.wikipedia.org/wiki/Espresso "wikilink")」を使用。
  - [玄箱](https://ja.wikipedia.org/wiki/玄箱 "wikilink") - [NAS自作キット一部機種にPowerPC使用](https://ja.wikipedia.org/wiki/ネットワークアタッチトストレージ "wikilink")。
  - [スウェーデン](https://ja.wikipedia.org/wiki/スウェーデン "wikilink")の多目的戦闘機[グリペンの中央情報処理装置](https://ja.wikipedia.org/wiki/サーブ_39_グリペン "wikilink")。

## 脚注

## 関連項目

  - [RISC](https://ja.wikipedia.org/wiki/RISC "wikilink")
  - [Power.org](https://ja.wikipedia.org/wiki/Power.org "wikilink")
  - [POWER](https://ja.wikipedia.org/wiki/POWER_\(マイクロプロセッサ\) "wikilink")
  - [PReP](https://ja.wikipedia.org/wiki/PReP "wikilink")
  - [CHRP](https://ja.wikipedia.org/wiki/CHRP "wikilink")
  - [PAPR](https://ja.wikipedia.org/wiki/PAPR "wikilink")
  - [Power Architecture](https://ja.wikipedia.org/wiki/Power_Architecture "wikilink")

## 外部リンク

  - [IBM::PowerPC features](http://www.ibm.com/chips/power/powerpc/)
  - [freescale::PowerPC Processors](http://www.freescale.com/webapp/sps/site/homepage.jsp?nodeId=0162468rH3bTdG)
  - [32ビットPowerPCアーキテクチャプログラミング環境(PDF)](http://www.freescale.co.jp/doc/MPCFPE32BJ_R1a.pdf)

<!-- end list -->

  - [Powerアーキテクチャーオファリング - 日本IBM](http://www-06.ibm.com/technology/jp/power/powerpc.html)

[Category:IBMのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:IBMのマイクロプロセッサ "wikilink") [Category:アップルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:アップルのマイクロプロセッサ "wikilink") [Category:モトローラのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:モトローラのマイクロプロセッサ "wikilink")

1.  [X704 with Exponential processor Power PC](http://www.computerhistory.org/collections/catalog/102662836) - [Computer History Museum](https://ja.wikipedia.org/wiki/コンピュータ歴史博物館 "wikilink")
2.
3.
4.
5.
6.  [1](https://www.power.org/wp-content/uploads/2010/11/ISSCC_WSP_Paper_5_05r2.pdf)