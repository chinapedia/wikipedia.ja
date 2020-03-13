> この記事は[ARM](https://ja.wikipedia.org/wiki/ARM)から翻訳されています。


**ARMアーキテクチャ** とは、[ARMホールディングス](https://ja.wikipedia.org/wiki/ARMホールディングス "wikilink")の事業部門であるARM Ltdにより設計・ライセンスされている、[組み込み機器や低電力アプリケーション向けに広く用いられている](../Page/組み込みシステム.md "wikilink")、[プロセッサ](../Page/プロセッサ.md "wikilink")コアの[アーキテクチャである](../Page/コンピュータ・アーキテクチャ.md "wikilink")。

## 概要

ARMアーキテクチャは消費電力を抑える特徴を持ち、低消費電力を目標に設計される[モバイル機器において支配的となっている](../Page/携帯機器.md "wikilink")。本アーキテクチャの[命令セットは](../Page/命令_\(コンピュータ\).md "wikilink")「（基本的に）固定長の命令」「簡素な命令セット」という[RISC](../Page/RISC.md "wikilink")風の特徴を有しつつ、「条件実行、定数シフト/ローテート付きオペランド、比較的豊富なアドレッシングモード」といった[CISC](../Page/CISC.md "wikilink")風の特徴を併せ持つのが特徴的だが、これは初期のARMがパソコン向けに設計された際、当時の同程度の性能のチップとしてはかなり少ないゲート数（約25,000トランジスタ）で実装されたチップの多くの部分を常に活用する設計として工夫されたもので、回路の複雑さを増さないという方向性だというように見れば、CISC風の特徴というよりむしろRISC風の特徴とも言える。ともあれ以上のような設計が、初期の世代の実装において、（性能の割に）低消費電力、小さなコア、（RISCとしては）高いコード密度といった優れた特性に結びつき、広く普及する原動力となった。

2005年の時点で、ARMファミリーは[32ビット](../Page/32ビット.md "wikilink")[組込み](../Page/組み込みシステム.md "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")（乃至、特にマイクロコントローラ）のおよそ75%を占め\[1\]、全世界で最も使用されている32ビットCPUアーキテクチャである。ARMアーキテクチャに基づくCPUコアは、[PDA](../Page/携帯情報端末.md "wikilink")・[携帯電話](../Page/携帯電話.md "wikilink")・[メディアプレーヤー](../Page/メディアプレーヤー.md "wikilink")・[携帯型ゲーム](../Page/携帯型ゲーム.md "wikilink")・[電卓](../Page/電卓.md "wikilink")などの携帯機器から、[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")・[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")などの[PC周辺機器まで](../Page/パーソナルコンピュータ.md "wikilink")、あらゆる電子機器に使用される。2013年現在、[NECのEMMA](../Page/日本電気.md "wikilink") MobileはCortex-A9を\[2\]や[日立系の](../Page/日立製作所.md "wikilink")[SuperH](../Page/SuperH.md "wikilink")系のSH Mobile GシリーズはARMを内蔵するなど、携帯電話では100%近いシェアがある。

携帯機器や電子機器の高性能化に伴いARMコアの出荷数は加速度的に伸びており、2008年1月の時点で100億個以上\[3\]、2010年9月の時点で200億個以上\[4\]が出荷されている。ARMアーキテクチャを使用したプロセッサの例としては、[テキサス・インスツルメンツ](../Page/テキサス・インスツルメンツ.md "wikilink")の[OMAP](https://ja.wikipedia.org/wiki/OMAP "wikilink")シリーズや[マーベル・テクノロジー・グループ](https://ja.wikipedia.org/wiki/マーベル・テクノロジー・グループ "wikilink")の[XScale](../Page/XScale.md "wikilink")、[NVIDIA](../Page/NVIDIA.md "wikilink")の[Tegra](https://ja.wikipedia.org/wiki/NVIDIA_Tegra "wikilink")、[クアルコム](../Page/クアルコム.md "wikilink")の[Snapdragon](https://ja.wikipedia.org/wiki/Snapdragon "wikilink")、[フリースケールのi](../Page/フリースケール・セミコンダクタ.md "wikilink").MXシリーズ、[ルネサス エレクトロニクスのRZファミリ](../Page/ルネサスエレクトロニクス.md "wikilink")、Synergyなどがある。

既存のARMプロセッサは組み込みとクライアントシステムに特化していたため全て[32ビット](../Page/32ビット.md "wikilink")であるが、顧客からは電力効率に優れるARMアーキテクチャの[サーバ](../Page/サーバ.md "wikilink")への応用を望む声が高まり、ARM社は2011年10月27日、ARMの[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")拡張であるARMv8アーキテクチャを発表した\[5\]。

## 歴史

ARMの設計は、[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")に[エイコーン・コンピュータ](https://ja.wikipedia.org/wiki/エイコーン・コンピュータ "wikilink")（イギリス）によって開始された。当時エイコーンは[モステクノロジー](../Page/モステクノロジー.md "wikilink")の[MOS 6502を搭載したコンピューターを製造](../Page/MOS_6502.md "wikilink")・販売しており、小さなハードウェア規模でシンプルな命令セットを持つ、より高速なプロセッサを開発することによって、6502を置き換えることが目的であった。

開発チームは[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")までに**ARM1**と呼ばれる開発サンプルを完成させ、最初の製品となる**ARM2**は次の年に完成した。ARM2は32ビットのデータバス、26ビットの[アドレス空間](../Page/アドレス空間.md "wikilink")と16個の32ビット[レジスタを備えていた](../Page/レジスタ_\(コンピュータ\).md "wikilink")。レジスタの1つは、上位6ビットが状態フラグを保持するプログラムカウンタである。ARM2の[トランジスタ](../Page/トランジスタ.md "wikilink")数は30000個しかなく、おそらく世界で最もシンプルな実用32ビットマイクロプロセッサであった。これは、[マイクロコードを持たないこと](../Page/マイクロプログラム方式.md "wikilink")（[モトローラ](../Page/モトローラ.md "wikilink")の[MC68000](../Page/MC68000.md "wikilink")の場合は1/4から1/3がマイクロコードであった）と、現在のほとんどのCPUと違って[キャッシュを含まないことによるものである](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")。このシンプルさのために消費電力は極めて低いが、それにもかかわらず[80286よりも性能は高かった](../Page/Intel_80286.md "wikilink")。後継となる**ARM3**は、4KBのキャッシュを含みさらに性能を高めた。

1980年代後半、[アップルコンピュータはエイコーンと共同で新しいARMコアの開発に取り組んだ](../Page/アップル_\(企業\).md "wikilink")。この作業は非常に重要視されていたため、エイコーンは[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")に開発チームをスピンオフしてAdvanced RISC Machinesという新会社を設立した。このため、ARMは本来のAcorn RISC Machineではなく**Advanced RISC Machine**の略であるという説明をよく見かけることになる。Advanced RISC Machinesは、[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に[ロンドン証券取引所](../Page/ロンドン証券取引所.md "wikilink")と[NASDAQ](../Page/NASDAQ.md "wikilink")に上場した際、ARM Limitedとなった。

この作業の結果、**ARM6**が開発された。[1991年](../Page/1991年.md "wikilink")に最初のモデルがリリースされ、アップルはARM6ベースのARM610を[アップル・ニュートン](../Page/アップル・ニュートン.md "wikilink")に採用した。

これらの変化を経てもコアは大体同じサイズに収まっている。ARM2は30000個のトランジスタを使用していたが、ARM6は35000個にしか増えていない。そこにあるアイデアは、エンドユーザーがARMコアと多くのオプションのパーツを組み合わせて完全なCPUとし、それによって古い設備でも製造でき、かつ安価に高性能を得られる、というものである。

このARM6の改良版である**ARM7**も、ARM6を採用した製品群に引き続き採用されたほか、普及期に入りつつあった[携帯電話](../Page/携帯電話.md "wikilink")にも広く採用されたことから、今日のARMの礎ともなった。

さらに、新世代のARMv4アーキテクチャに基いてARM7を再設計したものが**[ARM7TDMI](https://ja.wikipedia.org/wiki/:en:ARM7TDMI "wikilink")**である。ARM7TDMIはThumb命令（後述）を実装し、低消費電力と高いコード効率を両立する利点を備えていたことから、ライセンスを受けた多くの企業によって製品化され、特に[携帯電話](../Page/携帯電話.md "wikilink")や[ゲームボーイアドバンス](../Page/ゲームボーイアドバンス.md "wikilink")といった民生機器に採用されたことから、莫大な数の製品に搭載された。なお、TDMIとはThumb命令、[デバッグ](../Page/デバッグ.md "wikilink") (Debug) 回路、[乗算器](../Page/乗算器.md "wikilink") (Multiplier)、[ICE機能を搭載していることを意味している](../Page/インサーキット・エミュレータ.md "wikilink")。しかし、これより後のコアには全てこれらの機能が標準的に搭載されるようになったため、この名称は省かれている。

[DECはARMv](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")4アーキテクチャの設計のライセンスを得て[StrongARM](../Page/StrongARM.md "wikilink")を製造した。233MHzでStrongARMはほんの1[Wの電力しか消費しない](../Page/ワット.md "wikilink")（最近のバージョンはさらに少ない）。この業績は後に訴訟の解決の一環として[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")に移管され、インテルはこの機会を利用して古くなりつつあった[i960をStrongARMで補強することにし](https://ja.wikipedia.org/wiki/Intel_960 "wikilink")、それ以降[XScale](../Page/XScale.md "wikilink")という名で知られる高性能の実装を開発した。

以後も、StrongARMの技術のフィードバックを受けた**ARM9**や**ARM10**を経て、NECとの提携などによって携帯電話向けプロセッサとしての地位を確固たるものにした**ARM11**をリリースする。

2005年には製品ラインナップを一新し、高機能携帯電話などのアプリケーションプロセッサ向けである**Cortex-A**、リアルタイム制御向けである**Cortex-R**、[組み込みシステム](../Page/組み込みシステム.md "wikilink")向けである**Cortex-M**と、ターゲットごとにシリーズを分類した。なお、Cortexの末尾に付く文字は、社名であるARMの一文字ずつをそれぞれ割り当てたものである\[6\]。また、2012年11月にはARM初となる64ビットアーキテクチャによるプロセッサコアである**Cortex-A50**シリーズを発表した\[7\]。

ARMから[IPコア](../Page/IPコア.md "wikilink")のライセンス供与を受けている主な企業には、[モトローラ](../Page/モトローラ.md "wikilink")、[IBM](../Page/IBM.md "wikilink")、[テキサス・インスツルメンツ](../Page/テキサス・インスツルメンツ.md "wikilink")、[任天堂](../Page/任天堂.md "wikilink")、[フィリップス](../Page/フィリップス.md "wikilink")、[Atmel](https://ja.wikipedia.org/wiki/Atmel "wikilink")、[シャープ](../Page/シャープ.md "wikilink")、[サムスン電子](../Page/サムスン電子.md "wikilink")、[STマイクロエレクトロニクス](../Page/STマイクロエレクトロニクス.md "wikilink")、[アナログ・デバイセズ](https://ja.wikipedia.org/wiki/アナログ・デバイセズ "wikilink")、[パナソニック](https://ja.wikipedia.org/wiki/パナソニック "wikilink")、[クアルコム](../Page/クアルコム.md "wikilink")、[マーベル・テクノロジー・グループ](https://ja.wikipedia.org/wiki/マーベル・テクノロジー・グループ "wikilink")などがある。ARMチップは世界で最もよく使われているCPUデザインの一つとなっており、[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")、[携帯電話](../Page/携帯電話.md "wikilink")、[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")、[電卓](../Page/電卓.md "wikilink")から[玩具](../Page/玩具.md "wikilink")に至るまであらゆる製品の中に見ることができる。32ビット組み込みCPUで圧倒的なシェアを占め、[2004年](../Page/2004年.md "wikilink")の世界シェアは61%であった\[8\]。

## 主な採用製品

### ARM6

  - ARM60 [3DO マルチプレーヤー](../Page/3DO.md "wikilink")インタラクティブ

IMAGE:VY86C06020FC-2 02.jpg|
ARM60 CPU (VY86C06020FC-2) IMAGE:P60ARM GC 01.jpg|
ARM60 CPU (P60ARM)

  - ARM610 [アップル](../Page/アップル_\(企業\).md "wikilink") [ニュートン・メッセージパッド](../Page/アップル・ニュートン.md "wikilink")、メッセージパッド100、メッセージパッド110、メッセージパッド120

### ARM7/7E

  - 携帯情報端末
      - [eMate 300](https://ja.wikipedia.org/wiki/eMate_300 "wikilink")
  - 携帯電話
      - 一般的な[GSM](https://ja.wikipedia.org/wiki/GSM "wikilink")携帯電話
      - [cdmaOne](https://ja.wikipedia.org/wiki/cdmaOne "wikilink")携帯電話
      - 初期の[3G](https://ja.wikipedia.org/wiki/3G "wikilink")携帯電話（例：au [CDMA 1X](../Page/CDMA_1X.md "wikilink") A1400番台の一部を除くA1000番台・A3000番台・A5500番台を除くA5000番台。一部例外除く）
  - 携帯ゲーム機
      - [ゲームボーイアドバンス](../Page/ゲームボーイアドバンス.md "wikilink")
      - [ニンテンドーDS](../Page/ニンテンドーDS.md "wikilink")/[ニンテンドーDS Lite](../Page/ニンテンドーDS_Lite.md "wikilink")（サブCPU、[GBAソフトの動作にも使われる](../Page/ゲームボーイアドバンス.md "wikilink")）
      - [ニンテンドーDSi](https://ja.wikipedia.org/wiki/ニンテンドーDSi "wikilink")（サブCPU）
  - 携帯音楽プレーヤー
      - [iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")シリーズ（[デュアルコア実装](../Page/マルチコア.md "wikilink")）
  - 電卓
      - HP 20b / HP 30b
  - その他
      - [レゴマインドストーム NXT](https://ja.wikipedia.org/wiki/MINDSTORMS#レゴマインドストーム_NXT "wikilink")（知能ブロックの一部）
      - [ルンバ](../Page/ルンバ_\(掃除機\).md "wikilink")（一部の機種）

### ARM9/9E

  - 携帯ゲーム機
      - [ニンテンドーDS](../Page/ニンテンドーDS.md "wikilink")/[DS Lite](../Page/ニンテンドーDS_Lite.md "wikilink")/[ニンテンドーDSi](https://ja.wikipedia.org/wiki/ニンテンドーDSi "wikilink")（メインCPU、ARM7とのダブル実装）
      - [Tapwave Zodiac](https://ja.wikipedia.org/wiki/:en:Tapwave_Zodiac "wikilink")
  - 携帯電話
      - [Sun SPOT](../Page/Sun_SPOT.md "wikilink")
      - [Qualcomm](../Page/クアルコム.md "wikilink") MSM6550（[CDMA2000 1xEV-DO Rel.0対応携帯電話用チップセット](https://ja.wikipedia.org/wiki/CDMA2000_1x#Rel.0 "wikilink")）
      - Qualcomm MSM6800（[CDMA2000 1xEV-DO Rev.A対応携帯電話用チップセット](https://ja.wikipedia.org/wiki/CDMA2000_1x#Rev.A "wikilink")）
      - [3Gおよび](https://ja.wikipedia.org/wiki/第三世代携帯電話 "wikilink")[3.5G携帯電話](https://ja.wikipedia.org/wiki/第三・五世代携帯電話 "wikilink")（例：NTTドコモ [FOMA](../Page/FOMA.md "wikilink") 900i・901iシリーズ、[au](../Page/Au_\(携帯電話\).md "wikilink")([KDDI](../Page/KDDI.md "wikilink")、[沖縄セルラー電話](../Page/沖縄セルラー電話.md "wikilink"))の[CDMA 1Xシリーズおよび](../Page/CDMA_1X.md "wikilink")[CDMA 1X WINシリーズ](../Page/CDMA_1X_WIN.md "wikilink")、[ソフトバンクモバイル](https://ja.wikipedia.org/wiki/ソフトバンクモバイル "wikilink")の[SoftBank 3Gシリーズ等](../Page/SoftBank_3G.md "wikilink")。一部例外除く）
      - [H11T](../Page/H11T.md "wikilink")（[イー・モバイル](../Page/イー・モバイル.md "wikilink")の音声通話用3.5G端末）
      - [WS009KE](../Page/WS009KE.md "wikilink") "9 (nine)"（[WILLCOM](../Page/ウィルコム.md "wikilink")（ウィルコム）の[PHS](../Page/PHS.md "wikilink")端末）
      - Nokia [N-Gage](../Page/N-Gage.md "wikilink")
  - 携帯情報端末
      - Handheld Engine CXD2230GA （SONY [CLIE](../Page/CLIE.md "wikilink")に搭載）\[9\]
  - その他
      - [Sharp Brain](https://ja.wikipedia.org/wiki/Brain_\(電子辞書\) "wikilink")
      - [レゴマインドストーム EV3](../Page/MINDSTORMS.md "wikilink")

### ARM11/11E

  - [2007年](../Page/2007年.md "wikilink")頃から採用されるようになる。発表は[2002年](../Page/2002年.md "wikilink")[4月29日](../Page/4月29日.md "wikilink")\[10\]。
      - 2007年7月17日、[東芝](../Page/東芝.md "wikilink")がARM1176JZF-S搭載の携帯電話用プロセッサ、TC35711XBGを発表。2008年第2四半期より量産開始予定。
  - [NVIDIA](../Page/NVIDIA.md "wikilink") [Tegra](https://ja.wikipedia.org/wiki/NVIDIA_Tegra "wikilink")
      - [Zune HD](../Page/Zune.md "wikilink")
  - 携帯音楽プレーヤー
      - [iPod touch](https://ja.wikipedia.org/wiki/iPod_touch "wikilink")
      - [Zune](../Page/Zune.md "wikilink")
  - 携帯電話
      - [T-Mobile G1](https://ja.wikipedia.org/wiki/T-Mobile_G1 "wikilink")
      - Qualcomm　MSM7500（EV-DO Rev.A対応携帯電話用チップセット。ARM9Eとのダブル実装）
          - [KDDI](../Page/KDDI.md "wikilink")／[沖縄セルラー電話](../Page/沖縄セルラー電話.md "wikilink")（各auブランド）の「[KCP+](../Page/KCP+.md "wikilink")」対応CDMA 1X WINシリーズの携帯電話（例・[W56T](../Page/W56T.md "wikilink")、[W54SA](../Page/W54SA.md "wikilink")、[W61S](../Page/W61S.md "wikilink")、[W62T](../Page/W62T.md "wikilink")等）。ARM9Eとのダブル実装
          - KDDI／沖縄セルラー電話（各auブランド）のCDMA 1X WINシリーズのスマートフォン（例・[E30HT](https://ja.wikipedia.org/wiki/E30HT "wikilink")等）
      - Qualcomm　MSM7600（EV-DO Rev.A対応携帯電話用チップセット。ARM9Eとのダブル実装）
          - [KYOCERA](../Page/京セラ.md "wikilink") Zio M6000
          - HTC Hero
      - [NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")の[FOMA](../Page/FOMA.md "wikilink")902iシリーズ以降の携帯電話。905i以降のSymbian採用機はSH-4Aとダブル実装。
      - [WS018KE](../Page/WS018KE.md "wikilink") (WILLCOM 9)　（[WILLCOM](../Page/ウィルコム.md "wikilink")（ウィルコム）の[PHS](../Page/PHS.md "wikilink")端末）
      - Samsung S3C6400（ARM 1176JZ(F)-S v1.0）
          - [iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink") 3G（412 MHzで駆動）
  - タブレット・PDA
      - ノキア Internet Tablet N800
      - [mylo](https://ja.wikipedia.org/wiki/mylo "wikilink") COM-2
  - ゲーム機
      - [Zeebo](https://ja.wikipedia.org/wiki/Zeebo "wikilink") (新興国向けDL専用3Dゲーム機)
  - シングルボードコンピュータ
      - [Raspberry Pi](https://ja.wikipedia.org/wiki/Raspberry_Pi "wikilink") model 1A

### Cortex-M3

  - [2004年](../Page/2004年.md "wikilink")に発表された[マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")。
  - 同じARMv7-M/v7E-MシリーズのCortex-M3,M4,M7共に[ハーバード・アーキテクチャ](../Page/ハーバード・アーキテクチャ.md "wikilink")であることが最大の特徴である。
  - 自動車・工場・家電などの機器制御などに使われている。自動車では、モーター制御、[パワーステアリング](../Page/パワーステアリング.md "wikilink")、[横滑り防止装置](https://ja.wikipedia.org/wiki/横滑り防止装置 "wikilink")などいろいろな場所で使われている。
  - ワンボードマイコン
      - [mbed](https://ja.wikipedia.org/wiki/mbed "wikilink") - NXPのLPC1768の評価ボード。ホビー用途としても広く流通している。

### Cortex-A8

  - [2009年](../Page/2009年.md "wikilink")頃から採用されるようになる。2010年発売のAndroidスマートフォンは大多数が採用。
  - [NetWalker](https://ja.wikipedia.org/wiki/NetWalker "wikilink")
  - Samsung S5PC100
      - [iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink") 3GS（600 MHzで駆動）
      - [iPod touch](https://ja.wikipedia.org/wiki/iPod_touch "wikilink") (第3世代)
  - [Apple A4](https://ja.wikipedia.org/wiki/Apple_A4 "wikilink")（Cortex-A8をもとにアップルと[サムスンが携帯機器向けに開発](../Page/サムスン電子.md "wikilink")）
      - [iPhone 4](https://ja.wikipedia.org/wiki/iPhone_4 "wikilink")（800MHz）
      - [iPad](https://ja.wikipedia.org/wiki/iPad "wikilink")（1GHz）
      - [iPod touch](https://ja.wikipedia.org/wiki/iPod_touch "wikilink")（第4世代）
      - [Apple TV](../Page/Apple_TV.md "wikilink")（2010年モデル）
  - シングルボードコンピュータ
      - [BeagleBoard](https://ja.wikipedia.org/wiki/BeagleBoard "wikilink")、BeagleBoard-xM、BeableBone、BeagleBone Black
          - テキサス・インスツルメンツが技術支援をして[オープンソースハードウェア](../Page/オープンソースハードウェア.md "wikilink")によって開発されたボード。
      - Cubieboard

### Cortex-A9

  - タブレットは2010年頃から、スマートフォンは2011年から採用された。初期は2コアだったが、4コアのものがタブレットは2011年から、スマートフォンは2012年から登場した。
  - [NVIDIA](../Page/NVIDIA.md "wikilink") [Tegra 2](https://ja.wikipedia.org/wiki/NVIDIA_Tegra "wikilink")
      - [Surface RT](https://ja.wikipedia.org/wiki/Microsoft_Surface#Surface "wikilink")
  - 携帯ゲーム機
      - [PlayStation Vita](https://ja.wikipedia.org/wiki/PlayStation_Vita "wikilink")
  - [Apple A5](https://ja.wikipedia.org/wiki/Apple_A5 "wikilink")
      - [Apple TV (第3世代)](../Page/Apple_TV.md "wikilink")
      - [iPod touch (第5世代)](https://ja.wikipedia.org/wiki/iPod_touch "wikilink")
      - [iPad 2](https://ja.wikipedia.org/wiki/iPad_2 "wikilink"), [iPad mini](https://ja.wikipedia.org/wiki/iPad_mini "wikilink")
      - [iPhone 4S](https://ja.wikipedia.org/wiki/iPhone_4S "wikilink")
  - Apple A5X
      - [iPad (第3世代)](https://ja.wikipedia.org/wiki/iPad_\(第3世代\) "wikilink")
  - シングルボードコンピュータ
      - [PandaBoard](https://ja.wikipedia.org/wiki/PandaBoard "wikilink")
          - BeagleBoard同様、テキサス・インスツルメンツの技術支援によって開発されたボード。
      - Wandboard

### Cortex-A15

  - タブレットは2012年から、スマートフォンは2013年から採用された。

<!-- end list -->

  - [サムスン電子](../Page/サムスン電子.md "wikilink")は1.7GHzのデュアルコア Exynos 5250 を2012年10月\[11\]から搭載商品を販売開始。メモリ帯域12.8GB/s\[12\]。
  - テキサス・インスルメンツは2GHzのデュアルコアで2012年第3四半期から商品を出荷予定\[13\]。
  - NVIDIA は Tegra 4 を2013年第1四半期から出荷予定。
  - シングルボードコンピュータ
      - [ODROID](https://ja.wikipedia.org/wiki/ODROID "wikilink")-XU

### Cortex-A57

  - 2012年10月に[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink") ARMのCortex-A57, A53（コードネーム「Atlas」と「Apollo」）が発表され\[14\]、2014年に搭載商品（Samsung Galaxy Note 4 など）が販売開始された。
  - AMD は2015年下半期にサーバー向け Opteron A1100 (Seattle) をリリース予定\[15\]\[16\]。
  - A57やA53では、8コアや全てのコア同時稼働できる4+4コア（A57が4コア、A53が4コア）などが登場した。

### Cortex-A72

  - [2015年](../Page/2015年.md "wikilink")[2月3日](../Page/2月3日.md "wikilink")に発表され\[17\]、2015年に搭載商品が販売される予定\[18\]。Cortex-A57の後継製品。

## コアの性能と採用実績

### ARM社製

<table>
<thead>
<tr class="header">
<th><p>ファミリー</p></th>
<th><p>アーキテクチャ</p></th>
<th><p>コア</p></th>
<th><p>特徴</p></th>
<th><p>キャッシュ (I/D)/<a href="../Page/メモリ管理ユニット.md" title="wikilink">MMU</a></p></th>
<th><p>性能 MIPS @ MHz</p></th>
<th><p>採用製品</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ARM1</p></td>
<td><p>ARMv1</p></td>
<td><p>ARM1</p></td>
<td></td>
<td><p>なし</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/BBC_Cheese_Wedge#ARM_Evaluation_System" title="wikilink">ARM Evaluation System</a> second processor for <a href="https://ja.wikipedia.org/wiki/BBC_Micro" title="wikilink">BBC Micro</a></p></td>
</tr>
<tr class="even">
<td><p>ARM2</p></td>
<td><p>ARMv2</p></td>
<td><p>ARM2</p></td>
<td><p>MUL(乗算)命令を追加</p></td>
<td><p>なし</p></td>
<td><p>4 MIPS @ 8 MHz<br />
0.33 <a href="https://ja.wikipedia.org/wiki/DMIPS" title="wikilink">DMIPS</a>/MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Acorn_Archimedes" title="wikilink">Acorn Archimedes</a>, <a href="https://ja.wikipedia.org/wiki/Chessmachine" title="wikilink">Chessmachine</a></p></td>
</tr>
<tr class="odd">
<td><p>ARMv2a</p></td>
<td><p>ARM250</p></td>
<td><p>統合メモリコントローラ (MMU), Graphics and IO processor. SWAP命令を追加</p></td>
<td><p>なし, MEMC1a</p></td>
<td><p>7 MIPS @ 12 MHz</p></td>
<td><p>Acorn Archimedes</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM3</p></td>
<td><p>ARMv2a</p></td>
<td><p>ARM2a</p></td>
<td><p>ARMとしてはじめてのキャッシュの採用</p></td>
<td><p>4K 統合</p></td>
<td><p>12 MIPS @ 25 MHz<br />
0.50 <a href="https://ja.wikipedia.org/wiki/DMIPS" title="wikilink">DMIPS</a>/MHz</p></td>
<td><p>Acorn Archimedes</p></td>
</tr>
<tr class="odd">
<td><p>ARM6</p></td>
<td><p>ARMv3</p></td>
<td><p>ARM60</p></td>
<td><p>32ビットアドレス空間をサポート(それまでは26ビット)</p></td>
<td><p>なし</p></td>
<td><p>10 MIPS @ 12 MHz</p></td>
<td><p><a href="../Page/3DO.md" title="wikilink">3DO</a>, Zarlink GPS Receiver</p></td>
</tr>
<tr class="even">
<td><p>ARM600</p></td>
<td><p>キャッシュ、コプロセッサバス (FPA10浮動小数点演算ユニット用)</p></td>
<td><p>4K 統合</p></td>
<td><p>28 MIPS @ 33 MHz</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM610</p></td>
<td><p>キャッシュ、コプロセッサバスは無し</p></td>
<td><p>4K 統合</p></td>
<td><p>17 MIPS @ 20 MHz<br />
0.65 <a href="https://ja.wikipedia.org/wiki/DMIPS" title="wikilink">DMIPS</a>/MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Risc_PC" title="wikilink">Acorn Risc PC 600</a>, <a href="../Page/アップル・ニュートン.md" title="wikilink">アップル・ニュートン</a> 100シリーズ</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM7</p></td>
<td><p>ARMv3</p></td>
<td><p>ARM700</p></td>
<td></td>
<td><p>8KB 統合</p></td>
<td><p>40 MHz</p></td>
<td><p>Acorn Risc PC 試作CPUカード</p></td>
</tr>
<tr class="odd">
<td><p>ARM710</p></td>
<td></td>
<td><p>8KB 統合</p></td>
<td><p>40 MHz</p></td>
<td><p>Acorn Risc PC 700</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM710a</p></td>
<td></td>
<td><p>8KB 統合</p></td>
<td><p>40 MHz<br />
0.68 <a href="https://ja.wikipedia.org/wiki/DMIPS" title="wikilink">DMIPS</a>/MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Risc_PC" title="wikilink">Acorn Risc PC 700</a>, <a href="../Page/アップル・ニュートン.md" title="wikilink">アップル・ニュートン</a> eMate 300</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM7100</p></td>
<td><p>Integrated SoC.</p></td>
<td><p>8KB 統合</p></td>
<td><p>18 MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Psion_5" title="wikilink">Psion Series 5</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM7500</p></td>
<td><p>Integrated SoC.</p></td>
<td><p>4KB 統合</p></td>
<td><p>40 MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Acorn_A7000" title="wikilink">Acorn A7000</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM7500FE</p></td>
<td><p>Integrated SoC. "FE"、FPA・EDOメモリコントローラを追加</p></td>
<td><p>4KB 統合</p></td>
<td><p>56 MHz<br />
0.73 <a href="https://ja.wikipedia.org/wiki/DMIPS" title="wikilink">DMIPS</a>/MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/RiscStation" title="wikilink">Acorn A7000+</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM7TDMI</p></td>
<td><p>v4T</p></td>
<td><p>ARM7TDMI(-S)</p></td>
<td><p>3ステージ パイプライン</p></td>
<td><p>無し</p></td>
<td><p>15 MIPS @ 16.8 MHz</p></td>
<td><p><a href="../Page/ゲームボーイアドバンス.md" title="wikilink">ゲームボーイアドバンス</a>, <a href="../Page/ニンテンドーDS.md" title="wikilink">ニンテンドーDS</a>, <a href="https://ja.wikipedia.org/wiki/iPod" title="wikilink">iPod</a></p></td>
</tr>
<tr class="odd">
<td><p>ARM710T</p></td>
<td></td>
<td><p>MMU</p></td>
<td><p>36 MIPS @ 40 MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:Psion_5" title="wikilink">Psion 5 series</a>, <a href="../Page/アップル・ニュートン.md" title="wikilink">アップル・ニュートン</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM720T</p></td>
<td></td>
<td><p>8KB 統合キャッシュ, MMU</p></td>
<td><p>60 MIPS @ 59.8 MHz</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM740T</p></td>
<td></td>
<td><p>MPU</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>v5TEJ</p></td>
<td><p>ARM7EJ-S</p></td>
<td><p>Jazelle DBX</p></td>
<td><p>なし</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM9TDMI</p></td>
<td><p>v4T</p></td>
<td><p>ARM9TDMI</p></td>
<td><p>5ステージ パイプライン</p></td>
<td><p>なし</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM920T</p></td>
<td></td>
<td><p>16KB/16KB, MMU</p></td>
<td><p>200 MIPS @ 180 MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:Armadillo_CPU_Boards" title="wikilink">Armadillo</a>, <a href="https://ja.wikipedia.org/wiki/GP32" title="wikilink">GP32</a>,<a href="https://ja.wikipedia.org/wiki/GP2X" title="wikilink">GP2X</a> (マスタ), <a href="https://ja.wikipedia.org/wiki/:en:Tapwave_Zodiac" title="wikilink">:en:Tapwave Zodiac</a> (<a href="https://ja.wikipedia.org/wiki/Motorola" title="wikilink">Motorola</a> i. MX1)</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM922T</p></td>
<td></td>
<td><p>8KB/8KB, MMU</p></td>
<td><p>200/250 MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/CNS2132" title="wikilink">Cavium CNS2132 (Econa product lines)</a><a href="http://www.cnusers.org/">1</a>, <a href="https://ja.wikipedia.org/wiki/STR8132" title="wikilink">Cavium STR8132 (Econa evaluation board)</a>, <a href="https://ja.wikipedia.org/wiki/LN-86BT" title="wikilink">Ritmo Torrent Box/Mini Lan Server/BT-Downloader (ZAP-LN-86BT)</a><a href="http://www.zoobab.com/ritmo-torrent-box">2</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM940T</p></td>
<td></td>
<td><p>4KB/4KB, MPU</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/GP2X" title="wikilink">GP2X</a> (スレーブ)</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM9E</p></td>
<td><p>v5TE</p></td>
<td><p>ARM946E-S</p></td>
<td></td>
<td><p>variable, tightly coupled memories(TCM), MPU</p></td>
<td><p>231 MIPS @ 210MHz　74.47 MIPS @ 67.024MHz</p></td>
<td><p><a href="../Page/ニンテンドーDS.md" title="wikilink">ニンテンドーDS</a>, <a href="../Page/ノキア.md" title="wikilink">ノキア</a> <a href="../Page/N-Gage.md" title="wikilink">N-Gage</a>, Conexant 802.11 chips</p></td>
</tr>
<tr class="even">
<td><p>ARM966E-S</p></td>
<td></td>
<td><p>キャッシュレス, TCMs</p></td>
<td></td>
<td><p>ST Micro STR91xF, Ethernet内蔵 <a href="http://mcu.st.com/mcu/modules.php?name=mcu&amp;file=devicedocs&amp;DEV=STR912FW44&amp;FAM=101">3</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM968E-S</p></td>
<td></td>
<td><p>キャッシュレス, TCMs</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>v5TEJ</p></td>
<td><p>ARM926EJ-S</p></td>
<td><p>Jazelle DBX</p></td>
<td><p>variable, TCMs, MMU</p></td>
<td><p>220 MIPS @ 200 MHz</p></td>
<td><p>Mobile phones: <a href="https://ja.wikipedia.org/wiki/ソニー・エリクソン・モバイルコミュニケーションズ" title="wikilink">ソニー・エリクソン・モバイルコミュニケーションズ</a> (K, W シリーズ),<a href="../Page/シーメンス.md" title="wikilink">シーメンス</a> and <a href="https://ja.wikipedia.org/wiki/Benq" title="wikilink">Benq</a> (x65 シリーズ以降), <a href="../Page/Texas_Instruments_OMAP.md" title="wikilink">テキサスインスツルメンツ OMAP1710</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>v5TE</p></td>
<td><p>ARM996HS</p></td>
<td><p>Clockless processor</p></td>
<td><p>キャッシュレス, TCMs, MPU</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM10E</p></td>
<td><p>v5TE</p></td>
<td><p>ARM1020E</p></td>
<td><p>(VFP)</p></td>
<td><p>32KB/32KB, MMU</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM1022E</p></td>
<td><p>(VFP)</p></td>
<td><p>16KB/16KB, MMU</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>v5TEJ</p></td>
<td><p>ARM1026EJ-S</p></td>
<td><p>Jazelle DBX</p></td>
<td><p>variable, MMU or MPU</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM11</p></td>
<td><p>v6</p></td>
<td><p>ARM1136J(F)-S</p></td>
<td><p>SIMD, Jazelle DBX, (VFP)</p></td>
<td><p>variable, MMU</p></td>
<td><p>1.25 DMIPS/MHz</p></td>
<td><p><a href="../Page/Texas_Instruments_OMAP.md" title="wikilink">TI OMAP 2</a>, Freescale <a href="https://ja.wikipedia.org/wiki/i.MX" title="wikilink">i.MX</a>3</p></td>
</tr>
<tr class="even">
<td><p>v6T2</p></td>
<td><p>ARM1156T2(F)-S</p></td>
<td><p>SIMD, Thumb-2, (VFP)</p></td>
<td><p>variable, MPU</p></td>
<td><p>1.54 DMIPS/MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>v6KZ</p></td>
<td><p>ARM1176JZ(F)-S</p></td>
<td><p>SIMD, Jazelle DBX, (VFP)</p></td>
<td><p>variable, MMU+TrustZone</p></td>
<td><p>1.25 DMIPS/MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/iPhone" title="wikilink">iPhone</a>, iPhone 3G, Broadcom BCM2835</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>v6K</p></td>
<td><p>ARM11 MPCore</p></td>
<td><p>1-4 core SMP, SIMD, Jazelle DBX, (VFP)</p></td>
<td><p>variable, MMU</p></td>
<td><p>1.25 DMIPS/MHz(最大608MHz)</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/NVIDIA_Tegra" title="wikilink">NVIDIA Tegra</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>SecurCore</p></td>
<td><p>v6-M</p></td>
<td><p>SC000</p></td>
<td></td>
<td></td>
<td><p>0.9 DMIPS/MHz</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>v4T</p></td>
<td><p>SC100</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>v7-M</p></td>
<td><p>SC300</p></td>
<td></td>
<td></td>
<td><p>1.25 DMIPS/MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cortex-M</p></td>
<td><p>v6-M</p></td>
<td><p>Cortex-M0</p></td>
<td><p>マイクロコントローラ向け。M1はFPGA上で動作。命令はM3のサブセット。Thumb-2 (BL, MRS, MSR, ISB, DSB, and DMB)対応。</p></td>
<td></td>
<td><p>0.9 DMIPS/MHz</p></td>
<td><p>NXP LPC11xx, Triad Semiconductor, Melfas, 忠北テクノパーク, Nuvoton, オーストリアマイクロシステムズ, ローム, SwissMicros GmbH (<a href="https://ja.wikipedia.org/wiki/HP-10Cシリーズ#DM1x_(DM-1xCC)" title="wikilink">DM15</a>, <a href="https://ja.wikipedia.org/wiki/HP-41#DM41" title="wikilink">DM41等</a>)</p></td>
</tr>
<tr class="odd">
<td><p>Cortex-M0+</p></td>
<td></td>
<td><p>0.93 DMIPS/MHz</p></td>
<td><p>NXP LPC81x, LPC82x</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cortex-M1</p></td>
<td><p>なし, tightly coupled memory optional.</p></td>
<td><p>0.8 DMIPS/MHz[19]<br />
最大 136 DMIPS @ 170 MHz[20] (クロックはFPGA依存)</p></td>
<td><p><a href="../Page/アルテラ.md" title="wikilink">Altera</a> Cyclone III[21], Actel FPGA[22]</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>v7-M</p></td>
<td><p>Cortex-M3</p></td>
<td><p>マイクロコントローラ向け（ハーバード・アーキテクチャ）</p></td>
<td><p>キャッシュなし, (MPU)</p></td>
<td><p>1.25 DMIPS/MHz</p></td>
<td><p>Texas Instruments Stellaris MCU, STMicroelectronics STM32, NXP LPC1000, NXP <a href="https://ja.wikipedia.org/wiki/mbed" title="wikilink">mbed</a>, 東芝 TX03, <a href="https://ja.wikipedia.org/wiki/:en:Luminary_Micro" title="wikilink">Luminary Micro</a>, Ember EM3xx, Atmel AT91SAM3, Europe Technologies EasyBCU, Energy Micro EFM32, Actel SmartFusion, <a href="../Page/ルネサスエレクトロニクス.md" title="wikilink">Renesas</a> R-IN32</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>v7E-M</p></td>
<td><p>Cortex-M4</p></td>
<td><p>マイクロコントローラ向け（ハーバード・アーキテクチャ）。M3にDSP追加。モーター制御、FA/電力制御、オーディオ/ビデオ処理など。</p></td>
<td></td>
<td><p>Freescale Kinetis, NXP LPC43xx, STMicroelectronics, <a href="../Page/ルネサスエレクトロニクス.md" title="wikilink">Renesas</a> Synergy MCU(S3/S5/S7)</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>v7-M</p></td>
<td><p>Cortex-M7</p></td>
<td><p>マイクロコントローラ向け（ハーバード・アーキテクチャ）。M4までの3段パイプラインから、スーパースカラ(デュアル)6段パイプラインとなり、命令/データ1次キャッシュ、倍精度浮動小数点演算を追加するなど大幅に強化された。クロック周波数は最大800MHz程度までをターゲットとしており、2017年現在600MHzで動作する製品がある(NXP i.MX RT1050シリーズ)。 反面、M3,M4にあったBitBand機能が削除されているなどの変更点もある。</p></td>
<td><p>L1 命令/データ 各0～64KB, (MPU)</p></td>
<td><p>2.14 DMIPS/MHz[23][24]</p></td>
<td><p>STMicroelectronics STM32 F7, Atmel SAM x7x, NXP i.MX RT1050</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>v8-M</p></td>
<td><p>Cortex-M23</p></td>
<td><p>マイクロコントローラ向け（ノイマン・アーキテクチャ）</p></td>
<td></td>
<td><p>0.98 DMIPS/MHz[25]</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Cortex-M33</p></td>
<td><p>マイクロコントローラ向け（ハーバード・アーキテクチャ）</p></td>
<td></td>
<td><p>1.50 DMIPS/MHz[26]</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cortex-R</p></td>
<td><p>v7-R</p></td>
<td><p>Cortex-R4</p></td>
<td><p>組み込み向け</p></td>
<td><p>可変キャッシュ, MMUはオプション</p></td>
<td><p>1.66 DMIPS/MHz</p></td>
<td><p>Texas Instruments TMS570, <a href="https://ja.wikipedia.org/wiki/Broadcom" title="wikilink">Broadcom</a>, <a href="../Page/ルネサスエレクトロニクス.md" title="wikilink">Renesas</a> RZ/T</p></td>
</tr>
<tr class="odd">
<td><p>Cortex-R5</p></td>
<td></td>
<td><p>1.66 DMIPS/MHz</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cortex-R7</p></td>
<td></td>
<td><p>2.53 DMIPS/MHz</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Cortex-A</p></td>
<td><p>v7-A</p></td>
<td><p>Cortex-A5</p></td>
<td><p>低コスト、低消費電力</p></td>
<td><p>L1 4K-64K可変, L2 オプション, メモリ管理ユニット, TrustZone</p></td>
<td><p>400MHz〜800MHz<br />
1.57 DMIPS/MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Atmel" title="wikilink">Atmel</a> SAMA5, PS-T328, <a href="https://ja.wikipedia.org/wiki/Snapdragon" title="wikilink">Snapdragon</a> S4 Play, Snapdragon 200</p></td>
</tr>
<tr class="even">
<td><p>Cortex-A7</p></td>
<td><p>1-4マルチプロセッシング　浮動小数点演算器　L2キャッシュメモリ4MB（最高）</p></td>
<td><p>メモリ管理ユニット, TrustZone, ラージ<a href="../Page/物理アドレス拡張.md" title="wikilink">物理アドレス拡張</a></p></td>
<td><p>〜1.5Ghz<br />
1.9 DMIPS/MHz　</p></td>
<td><p>Snapdragon S4 Play, Snapdragon 200, 208, 210, 212, 400, <a href="https://ja.wikipedia.org/wiki/Allwinner" title="wikilink">Allwinner</a> A20, <a href="https://ja.wikipedia.org/wiki/Allwinner" title="wikilink">Allwinner</a> A31, <a href="https://ja.wikipedia.org/wiki/MediaTek" title="wikilink">MediaTek</a> MT6589, Broadcom BCM2836</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Cortex-A8</p></td>
<td><p>アプリケーション向け, NEON, Jazelle RCT, Thumb-2</p></td>
<td><p>可変(L1+L2), <a href="../Page/メモリ管理ユニット.md" title="wikilink">メモリ管理ユニット</a>, TrustZone</p></td>
<td><p>600MHz〜1GHz<br />
2.0 DMIPS/MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Texas_Instruments_OMAP#OMAP_3.E3.82.B7.E3.83.AA.E3.83.BC.E3.82.BA" title="wikilink">TI OMAP 3</a>, Freescale <a href="https://ja.wikipedia.org/wiki/i.MX" title="wikilink">i.MX</a> 5, <a href="https://ja.wikipedia.org/wiki/Apple_A4" title="wikilink">Apple A4</a>, Samsung <a href="https://ja.wikipedia.org/wiki/Exynos" title="wikilink">Exynos</a> 3, <a href="https://ja.wikipedia.org/wiki/Allwinner" title="wikilink">Allwinner</a> A1x, <a href="https://ja.wikipedia.org/wiki/Rockchip" title="wikilink">Rockchip</a> RK29xx</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cortex-A9</p></td>
<td><p>アプリケーション向け, 1-4コア<a href="../Page/対称型マルチプロセッシング.md" title="wikilink">対称型マルチプロセッシング</a>, (VFP), (NEON), Jazelle RCT and DBX, Thumb-2, <a href="../Page/アウト・オブ・オーダー実行.md" title="wikilink">アウト・オブ・オーダー実行</a>, <a href="../Page/投機的実行.md" title="wikilink">投機的実行</a>, <a href="https://ja.wikipedia.org/wiki/スーパースケーラ" title="wikilink">スーパースケーラ</a></p></td>
<td><p>メモリ管理ユニット, TrustZone</p></td>
<td><p>800MHz〜2GHz<br />
2.5 DMIPS/MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Texas_Instruments_OMAP#OMAP_4.E3.82.B7.E3.83.AA.E3.83.BC.E3.82.BA" title="wikilink">TI OMAP 4</a>, Freescale <a href="https://ja.wikipedia.org/wiki/i.MX" title="wikilink">i.MX</a> 6, ST-Ericsson NovaThor U8500, <a href="https://ja.wikipedia.org/wiki/NVIDIA_Tegra" title="wikilink">NVIDIA Tegra</a> 2, <a href="https://ja.wikipedia.org/wiki/NVIDIA_Tegra" title="wikilink">NVIDIA Tegra</a> 3, <a href="https://ja.wikipedia.org/wiki/NVIDIA_Tegra" title="wikilink">NVIDIA Tegra</a> 4i, STMicroelectronics <a href="http://www.st.com/stonline/products/families/embedded_mpu/spear_mpus/spear_with_1300k.htm">SPEAr1300</a>, <a href="../Page/ザイリンクス.md" title="wikilink">ザイリンクス</a> Zynq-7000, <a href="https://ja.wikipedia.org/wiki/Apple_A5" title="wikilink">Apple A5</a>, <a href="https://ja.wikipedia.org/wiki/Rockchip" title="wikilink">Rockchip</a> RK3xxx, Samsung <a href="https://ja.wikipedia.org/wiki/Exynos" title="wikilink">Exynos</a> 4, <a href="https://ja.wikipedia.org/wiki/HiSilicon" title="wikilink">HiSilicon</a> K3V2, Kirin 910, <a href="https://ja.wikipedia.org/wiki/MediaTek" title="wikilink">MediaTek</a>, <a href="../Page/ルネサスエレクトロニクス.md" title="wikilink">Renesas</a> RZ/A</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Cortex-A15</p></td>
<td><p>1-4コア対称型マルチプロセッシング</p></td>
<td><p>メモリ管理ユニット, TrustZone, ラージ<a href="../Page/物理アドレス拡張.md" title="wikilink">物理アドレス拡張</a></p></td>
<td><p>1GHz〜2.5GHz<br />
3.5 DMIPS/MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Texas_Instruments_OMAP#OMAP_5.E3.82.B7.E3.83.AA.E3.83.BC.E3.82.BA" title="wikilink">TI OMAP 5</a>, Samsung <a href="https://ja.wikipedia.org/wiki/Exynos" title="wikilink">Exynos</a> 5, <a href="https://ja.wikipedia.org/wiki/NVIDIA_Tegra" title="wikilink">NVIDIA Tegra</a> 4, <a href="https://ja.wikipedia.org/wiki/NVIDIA_Tegra" title="wikilink">NVIDIA Tegra</a> K1, <a href="https://ja.wikipedia.org/wiki/HiSilicon" title="wikilink">HiSilicon</a> Kirin 920, <a href="https://ja.wikipedia.org/wiki/Renesas" title="wikilink">Renesas</a> APE6, <a href="https://ja.wikipedia.org/wiki/Renesas" title="wikilink">Renesas</a> R-Car H2, <a href="https://ja.wikipedia.org/wiki/Renesas" title="wikilink">Renesas</a> MP6530</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cortex-A17</p></td>
<td><p>1-4コア対称型マルチプロセッシング</p></td>
<td><p>メモリ管理ユニット, TrustZone, ラージ<a href="../Page/物理アドレス拡張.md" title="wikilink">物理アドレス拡張</a></p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Rockchip" title="wikilink">Rockchip</a> RK3288</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>v8-A</p></td>
<td><p>Cortex-A32</p></td>
<td><p>超小型、低消費電力、電力効率重視。<a href="https://ja.wikipedia.org/wiki/モノのインターネット" title="wikilink">IoT機器向け</a>。32ビット命令セット。</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cortex-A35</p></td>
<td><p>低コスト、低消費電力、電力効率重視。64ビット命令セット。</p></td>
<td><p>メモリ管理ユニット, TrustZone, 64bit仮想アドレス</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/MediaTek" title="wikilink">MediaTek</a> Helio X30</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Cortex-A53</p></td>
<td><p>64ビット命令セット。<a href="https://ja.wikipedia.org/wiki/暗号化" title="wikilink">暗号化</a>命令</p></td>
<td><p>メモリ管理ユニット, TrustZone, 64bit仮想アドレス</p></td>
<td><p>2.3 DMIPS/MHz</p></td>
<td><p>Snapdragon 410, 412, 415, 425, 610, 615, 617, 625, 808, 810, <a href="https://ja.wikipedia.org/wiki/HiSilicon" title="wikilink">HiSilicon</a> Kirin 620, 930, 935, <a href="https://ja.wikipedia.org/wiki/Rockchip" title="wikilink">Rockchip</a> RK3368, <a href="https://ja.wikipedia.org/wiki/MediaTek" title="wikilink">MediaTek</a> MT6732, 6735, 6737, 6737T, 6738, 6750, 6752, 6753, Helio P10, P20, P25, X10, X30</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cortex-A57</p></td>
<td></td>
<td><p>メモリ管理ユニット, TrustZone, 64bit仮想アドレス</p></td>
<td><p>4.1 DMIPS/MHz</p></td>
<td><p>Snapdragon 808, 810, Nvidia <a href="https://ja.wikipedia.org/wiki/Tegra" title="wikilink">Tegra</a> X1, Samsung <a href="https://ja.wikipedia.org/wiki/Exynos" title="wikilink">Exynos</a> 7</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Cortex-A72</p></td>
<td></td>
<td><p>メモリ管理ユニット, TrustZone, 64bit仮想アドレス</p></td>
<td></td>
<td><p>Snapdragon 618, 620, 650, 652, HiSilicon Kirin 950, 955</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cortex-A73</p></td>
<td></td>
<td><p>メモリ管理ユニット, TrustZone, 64bit仮想アドレス</p></td>
<td></td>
<td><p>HiSilicon Kirin 960, MediaTek Helio X30</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>v8.2-A</p></td>
<td><p>Cortex-A55</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cortex-A75</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### サードパーティー

<table>
<thead>
<tr class="header">
<th><p>ファミリー</p></th>
<th><p>アーキテクチャ</p></th>
<th><p>名称</p></th>
<th><p>特徴</p></th>
<th><p>キャッシュ (I/D)/<a href="../Page/メモリ管理ユニット.md" title="wikilink">MMU</a></p></th>
<th><p>性能 MIPS @ MHz</p></th>
<th><p>採用製品</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/StrongARM.md" title="wikilink">StrongARM</a></p></td>
<td><p>v4</p></td>
<td><p>SA-1</p></td>
<td></td>
<td><p>16 KB/8–16 KB, MMU</p></td>
<td><p>203–206 MHz<br />
1.0 DMIPS/MHz</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/XScale.md" title="wikilink">XScale</a></p></td>
<td><p>v5TE</p></td>
<td><p>80200/IOP310/IOP315</p></td>
<td><p>I/O Processor</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>80219</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>IOP321</p></td>
<td></td>
<td></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:Iyonix" title="wikilink">:en:Iyonix</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>IOP33x</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>PXA210/PXA250</p></td>
<td><p>Applications processor</p></td>
<td></td>
<td></td>
<td><p><a href="../Page/ザウルス.md" title="wikilink">ザウルス</a> SL-5600, SL-A300</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>PXA255</p></td>
<td></td>
<td><p>32KB/32KB, MMU</p></td>
<td><p>400 <a href="../Page/BogoMips.md" title="wikilink">BogoMips</a> @400 MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:Gumstix" title="wikilink">:en:Gumstix</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>PXA26x</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>PXA27x</p></td>
<td></td>
<td></td>
<td><p>800 MIPS @ 624 MHz</p></td>
<td><p><a href="../Page/HTC_(企業).md" title="wikilink">HTC</a> Universal, <a href="../Page/ザウルス.md" title="wikilink">ザウルス</a> SL-C1000,3000,3100,3200,<a href="https://ja.wikipedia.org/wiki/Willcom" title="wikilink">Willcom</a> <a href="../Page/W-ZERO3.md" title="wikilink">W-ZERO3</a>シリーズ WS003SH,WS004SH,WS007SH,WS011SH,WS020SH</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>PXA800(E)F</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Monahans</p></td>
<td></td>
<td></td>
<td><p>1000 MIPS @ 1.25 GHz</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>PXA900</p></td>
<td></td>
<td></td>
<td></td>
<td><p>Blackberry 8700, Blackberry Pearl (8100)</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>IXC1100</p></td>
<td><p>Control Plane Processor</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>IXP2400/IXP2800</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>IXP2850</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>IXP2325/IXP2350</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>IXP42x</p></td>
<td></td>
<td></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:NSLU2" title="wikilink">:en:NSLU2</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>IXP460/IXP465</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Snapdragon" title="wikilink">Snapdragon</a></p></td>
<td><p>v7-A</p></td>
<td><p>Scorpion</p></td>
<td><p>アプリケーション向け, 1-2コア対称型マルチプロセッシング, VFPv3, NEON, Thumb-2, Jazelle RCT, <a href="../Page/アウト・オブ・オーダー実行.md" title="wikilink">アウト・オブ・オーダー実行</a>, <a href="../Page/投機的実行.md" title="wikilink">投機的実行</a></p></td>
<td><p>可変(L1+L2), <a href="../Page/メモリ管理ユニット.md" title="wikilink">MMU</a>, TrustZone</p></td>
<td><p>800MHz〜1.5GHz<br />
2.1 DMIPS/MHz</p></td>
<td><p><a href="../Page/クアルコム.md" title="wikilink">Qualcomm</a> Snapdragon S1, S2, S3 (第1〜3世代)</p></td>
</tr>
<tr class="even">
<td><p>Krait</p></td>
<td><p>アプリケーション向け, 1-4コア対称型マルチプロセッシング, VFPv4</p></td>
<td><p><a href="../Page/メモリ管理ユニット.md" title="wikilink">MMU</a>, TrustZone</p></td>
<td><p>〜2.5GHz<br />
3.3 DMIPS/MHz</p></td>
<td><p>Qualcomm Snapdragon S4 (第4世代・S4 Playは除く), 400/600/800 (第5世代)</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>v8-A</p></td>
<td><p>Kryo</p></td>
<td></td>
<td><p>64KB/512KB–1MB</p></td>
<td><p>〜2.6GHz<br />
6.3 DMIPS/MHz</p></td>
<td><p>Qualcomm Snapdragon 820</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Centriq</p></td>
<td><p>v8-A</p></td>
<td><p>Folker</p></td>
<td></td>
<td></td>
<td></td>
<td><p>Centriq 2400</p></td>
</tr>
<tr class="odd">
<td><p>ARMADA</p></td>
<td><p>v7-A</p></td>
<td><p>Sheeva PJ4</p></td>
<td><p>アプリケーション向け, 1-4コア対称型マルチプロセッシング, VFPv3, Wireless MMX2, Thumb-2</p></td>
<td><p>可変(L1+L2), <a href="../Page/メモリ管理ユニット.md" title="wikilink">MMU</a>, TrustZone</p></td>
<td><p>〜1.5GHz<br />
2.42 DMIPS/MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/マーベル・テクノロジー・グループ" title="wikilink">Marvell</a> ARMADA 500/600シリーズ</p></td>
</tr>
<tr class="even">
<td><p>Sheeva PJ4B</p></td>
<td><p>組み込み向け, 1-4コア対称型マルチプロセッシング, VFPv3, NEON, Wireless MMX2, Thumb-2</p></td>
<td><p>可変(L1+L2), <a href="../Page/メモリ管理ユニット.md" title="wikilink">MMU</a>, TrustZone</p></td>
<td><p>〜1.6GHz<br />
2.61 DMIPS/MHz</p></td>
<td><p>Marvell ARMADA XP/370/1500</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Apple Ax</p></td>
<td><p>v7-A</p></td>
<td><p>Swift</p></td>
<td><p>アプリケーション向け, 2コア対称型マルチプロセッシング, VFPv4</p></td>
<td><p>32KB/32KB</p></td>
<td><p>1.1GHz, 1.4GHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Apple_A6" title="wikilink">Apple A6</a>, <a href="https://ja.wikipedia.org/wiki/Apple_A6X" title="wikilink">Apple A6X</a></p></td>
</tr>
<tr class="even">
<td><p>v8-A</p></td>
<td><p>Cyclone</p></td>
<td><p>アプリケーション向け, 2コア, AArch64</p></td>
<td><p>64KB/64KB</p></td>
<td><p>1.3GHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Apple_A7" title="wikilink">Apple A7</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Cyclone gen 2</p></td>
<td><p>アプリケーション向け, 2コア, AArch64</p></td>
<td><p>64KB/64KB</p></td>
<td><p>1.1GHz, 1.4GHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Apple_A8" title="wikilink">Apple A8</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Typhoon</p></td>
<td><p>アプリケーション向け, 3コア, AArch64</p></td>
<td><p>64KB/64KB</p></td>
<td><p>1.5GHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Apple_A8X" title="wikilink">Apple A8X</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Twister</p></td>
<td><p>アプリケーション向け, 2コア, AArch64</p></td>
<td><p>64KB/64KB</p></td>
<td><p>1.8GHz, 2.25GHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Apple_A9" title="wikilink">Apple A9</a>, <a href="https://ja.wikipedia.org/wiki/Apple_A9X" title="wikilink">Apple A9X</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Hurricane</p>
<p>Zephyr</p></td>
<td><p>アプリケーション向け, 2+2コア, AArch64</p></td>
<td><p>64KB/64KB</p></td>
<td><p>2.33GHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Apple_A10" title="wikilink">Apple A10 Fusion</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>アプリケーション向け, 3+3コア, AArch64</p></td>
<td><p>2.38Ghz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Apple_A10X" title="wikilink">Apple A10X Fusion</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Monsoon Mistral</p></td>
<td><p>アプリケーション向け, 2+4コア, AArch64</p></td>
<td><p>64KB/64KB</p></td>
<td><p>2.39GHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Apple_A11" title="wikilink">Apple A11 Bionic</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Vortex Tempest</p></td>
<td><p>アプリケーション向け, 2+4コア, AArch64</p></td>
<td><p>128KB/128KB</p></td>
<td><p>2.49GHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Apple_A12" title="wikilink">Apple A12 Bionic</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>アプリケーション向け, 4+4コア, AArch64</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Apple_A12X" title="wikilink">Apple A12X Bionic</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Tegra K1</p></td>
<td><p>v8-A</p></td>
<td><p>Denver</p></td>
<td></td>
<td><p>128kB/64kB</p></td>
<td></td>
<td><p>Google <a href="https://ja.wikipedia.org/wiki/Nexus_9" title="wikilink">Nexus 9</a>, <a href="https://ja.wikipedia.org/wiki/小米科技" title="wikilink">Xiaomi</a> Mi Pad</p></td>
</tr>
<tr class="even">
<td><p>Parker</p></td>
<td><p>Denver 2.0</p></td>
<td></td>
<td></td>
<td></td>
<td><p>DRIVE PX2</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Xavier</p></td>
<td><p>Carmel</p></td>
<td></td>
<td></td>
<td></td>
<td><p>DRIVE Xavier, Jetson AGX Xavier</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Exynos</p></td>
<td><p>v8-A</p></td>
<td><p>Exynos M1</p></td>
<td></td>
<td><p>64kB/2MB(4コアシェア)</p></td>
<td></td>
<td><p>Exynos 8890(Exynos 8 Octa)</p></td>
</tr>
<tr class="odd">
<td><p>Exynos M2</p></td>
<td></td>
<td><p>64kB/2MB(4コアシェア)</p></td>
<td></td>
<td><p>Exynos 8895</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Exynos M3</p></td>
<td></td>
<td><p>64kB/2MB(4コアシェア)</p></td>
<td></td>
<td><p>Exynos 9810</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

ARMv7-A, v8-A は以下の SoC で実装されている。

  - [Allwinner](https://ja.wikipedia.org/wiki/Allwinner "wikilink") (全志科技)
  - Amlogic (晶晨半导体)
  - [Apple A4](https://ja.wikipedia.org/wiki/Apple_A4 "wikilink"), [Apple A5](https://ja.wikipedia.org/wiki/Apple_A5 "wikilink"), [Apple A5X](https://ja.wikipedia.org/wiki/Apple_A5 "wikilink"), [Apple A6](https://ja.wikipedia.org/wiki/Apple_A6 "wikilink"), [Apple A6X](https://ja.wikipedia.org/wiki/Apple_A6X "wikilink"), [Apple A7](https://ja.wikipedia.org/wiki/Apple_A7 "wikilink"), [Apple A8](https://ja.wikipedia.org/wiki/Apple_A8 "wikilink"), [Apple A8X](https://ja.wikipedia.org/wiki/Apple_A8X "wikilink"), [Apple A9](https://ja.wikipedia.org/wiki/Apple_A9 "wikilink"), [Apple A9X](https://ja.wikipedia.org/wiki/Apple_A9X "wikilink"), [Apple A10](https://ja.wikipedia.org/wiki/Apple_A10 "wikilink"), [Apple A10X](https://ja.wikipedia.org/wiki/Apple_A10X "wikilink"), [Apple A11](https://ja.wikipedia.org/wiki/Apple_A11 "wikilink"), [Apple A12](https://ja.wikipedia.org/wiki/Apple_A12 "wikilink"), [Apple A12X](https://ja.wikipedia.org/wiki/Apple_A12X "wikilink")
  - Freescale [i.MX](https://ja.wikipedia.org/wiki/i.MX "wikilink")
  - Fujitsu ARM based SoC Platform (FASP)
  - [HiSilicon](https://ja.wikipedia.org/wiki/HiSilicon "wikilink") (海思半导体)
  - [Marvell](https://ja.wikipedia.org/wiki/マーベル・テクノロジー・グループ "wikilink") ARMADA
  - [MediaTek](https://ja.wikipedia.org/wiki/MediaTek "wikilink")
  - [NVIDIA Tegra](https://ja.wikipedia.org/wiki/NVIDIA_Tegra "wikilink")
  - [Qualcomm](../Page/クアルコム.md "wikilink") [Snapdragon](https://ja.wikipedia.org/wiki/Snapdragon "wikilink")
  - [Renesas](https://ja.wikipedia.org/wiki/Renesas "wikilink") EV2, APE6
  - [Rockchip](https://ja.wikipedia.org/wiki/Rockchip "wikilink") (瑞芯微电子)
  - [Samsung](https://ja.wikipedia.org/wiki/Samsung "wikilink") Hummingbird, [Samsung](https://ja.wikipedia.org/wiki/Samsung "wikilink") [Exynos](https://ja.wikipedia.org/wiki/Exynos "wikilink")
  - ST-Ericsson NovaThor
  - STMicroelectronics SPEAr
  - [Texas Instruments OMAP](../Page/Texas_Instruments_OMAP.md "wikilink")
  - Trident PNX
  - ZiiLABS ZMS

## ARMアーキテクチャを採用しているCPU/メーカ

[ARMホールディングスの概要にあるように](https://ja.wikipedia.org/wiki/ARMホールディングス#概要 "wikilink")、ARMホールディングスはARMアーキテクチャの設計のみをしており、製造は行ってはいない。ARMは[IPコア](../Page/IPコア.md "wikilink")として各社にライセンスされ、それぞれの会社において機能を追加するなどして[CPU](../Page/CPU.md "wikilink")として製造される。製造されたCPUはそのまま、あるいはボード上に実装、もしくは製品に組み込まれた形で販売などされる。

以下に『CPUそのもの』『ボード上に実装したもの』などCPUやボードのシリーズ名やブランド名などが明確な主なメーカ名/CPU名/シリーズ名等を記する。

  - [NXPセミコンダクターズ](https://ja.wikipedia.org/wiki/NXPセミコンダクターズ "wikilink")
      - LPC
      - LPCXpresso
      - mbed
  - [フリースケール・セミコンダクタ](../Page/フリースケール・セミコンダクタ.md "wikilink")
      - i.MX
      - Kinetis
  - [DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")-[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")
      - [StrongARM](../Page/StrongARM.md "wikilink")
  - [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink") - [マーベル・テクノロジー・グループ](https://ja.wikipedia.org/wiki/マーベル・テクノロジー・グループ "wikilink")
      - [XScale](../Page/XScale.md "wikilink")
  - [STマイクロエレクトロニクス](../Page/STマイクロエレクトロニクス.md "wikilink")
      - STM32
  - [サイプレス・マイクロシステムズ](https://ja.wikipedia.org/wiki/サイプレス・マイクロシステムズ "wikilink")
      - [PSoC 5](https://ja.wikipedia.org/wiki/PSoC "wikilink")
  - [東芝](../Page/東芝.md "wikilink")
      - [TX03](https://ja.wikipedia.org/wiki/TX03 "wikilink"),[TX09](https://ja.wikipedia.org/wiki/TX09 "wikilink")シリーズ
  - [Panasonic](https://ja.wikipedia.org/wiki/Panasonic "wikilink")
      - [MN2WS0220](https://ja.wikipedia.org/wiki/MN2WS0220 "wikilink")シリーズ(スマートテレビ用UniPhier)
  - [ルネサス エレクトロニクス](https://ja.wikipedia.org/wiki/ルネサス_エレクトロニクス "wikilink")
      - RZファミリ
      - EMMA Mobile
      - R-Mobile
      - R-Car
      - Renesas Synergy MCU

## 32ビットARM

### 命令セット

ARM は RISC プロセッサであり、Thumb 命令ではなく ARM 命令の場合、その命令セットは

  - 32ビット固定長命令
  - ロード/ストアアーキテクチャ
  - 3オペランドのレジスタ間演算
  - 多くの命令が1サイクルで実行可能

といった、多くの32ビットRISCプロセッサに共通する特徴が見られる。

ARMプロセッサは、[PC相対アドレッシングやプレ](https://ja.wikipedia.org/wiki/レジスタ_\(コンピュータ\)#プログラムカウンタ "wikilink")-/ポスト-インクリメント・アドレッシングモードなど、RISCとみなされる他のアーキテクチャと比べ、豊富な[アドレッシングモード](../Page/アドレッシングモード.md "wikilink")を持っている。

もう一つ留意すべきことは、ARMの命令セットが時間とともに増加しているということである。例えば、初期のARMプロセッサ（ARM7TDMIより以前のもの）は2バイトの値をロードする命令がなかった。

### CPUモード

32ビット ARM アーキテクチャはいくつかのCPUモードを持つ。同時には1つのモードにしかなれない。命令や外部からの割込みなどでモードが切り替わる\[27\]。

  - ユーザーモード
    唯一の非特権モード。
  - 高速割込みモード
    FIQ 割込みが発生したときに切り替わる特権モード。
  - 割込みモード
    IRQ 割込みが発生したときに切り替わる特権モード。
  - スーパーバイザーモード
    CPU がリセットされたときか SWI 命令が実行されたときに切り替わる特権モード。
  - アボートモード
    プリフェッチアボートかデータアボート例外が発生したときに切り替わる特権モード。
  - 未定義モード
    未定義命令が実行されたときに切り替わる特権モード。
  - システムモード (ARMv4以降)
    これが唯一例外が原因で切り替わるモードではない。CPSRレジスタにこのモードを書くことによりこのモードに切り替えることが出来る。
  - MONモード (要セキュリティ拡張)
    TrustZone 拡張をサポートするために作られたモニターモード。
  - HYP 別名 PL2 モード (ARMv7以降)
    仮想化拡張、ハイパーバイザーモード。\[28\]

### レジスタ

レジスタ R0 から R7 は全ての CPU モードで同一。これらは決してバンクされない。

R13 と R14 はシステムモード以外の全ての特権 CPU モードでバンクされる。独自の R13 と R14 を持つことにより例外からそれぞれのモードに切り替えられる。R13 はスタックポインタ、R14 は関数からの戻りアドレスを持つ。

| usr  | sys       | svc       | abt       | und       | irq       | fiq |
| ---- | --------- | --------- | --------- | --------- | --------- | --- |
| R0   |           |           |           |           |           |     |
| R1   |           |           |           |           |           |     |
| R2   |           |           |           |           |           |     |
| R3   |           |           |           |           |           |     |
| R4   |           |           |           |           |           |     |
| R5   |           |           |           |           |           |     |
| R6   |           |           |           |           |           |     |
| R7   |           |           |           |           |           |     |
| R8   | R8_fiq   |           |           |           |           |     |
| R9   | R9_fiq   |           |           |           |           |     |
| R10  | R10_fiq  |           |           |           |           |     |
| R11  | R11_fiq  |           |           |           |           |     |
| R12  | R12_fiq  |           |           |           |           |     |
| R13  | R13_svc  | R13_abt  | R13_und  | R13_irq  | R13_fiq  |     |
| R14  | R14_svc  | R14_abt  | R14_und  | R14_irq  | R14_fiq  |     |
| R15  |           |           |           |           |           |     |
| CPSR |           |           |           |           |           |     |
|      | SPSR_svc | SPSR_abt | SPSR_und | SPSR_irq | SPSR_fiq |     |

CPU モードごとのレジスタ

別名：

  - R13 は SP とも呼ばれ、スタックポインタ
  - R14 は LR とも呼ばれ、リンクレジスタ
  - R15 は PC とも呼ばれ、プログラムカウンタ

CPSR は下記32ビットを持つ\[29\]。

  - M (ビット 0 - 4) はプロセッサモードビット
  - T (ビット 5) は Thumb ステートビット
  - F (ビット 6) は FIQ 無効ビット
  - I (ビット 7) は IRQ 無効ビット
  - A (ビット 8) は不正データアボート無効ビット
  - E (ビット 9) はデータエンディアンビット
  - IT (ビット 10 - 15 と 25 - 26) は if-then ステートビット
  - GE (ビット 16 - 19) は greater-than-or-equal-to ビット
  - DNM (ビット 20 - 23) は書き換え禁止ビット
  - J (ビット 24) は Java ステートビット
  - Q (ビット 27) は sticky overflow ビット
  - V (ビット 28) はオーバーフロービット
  - C (ビット 29) は carry/borrow/extend ビット
  - Z (ビット 30) は零ビット
  - N (ビット 31) は negative/less ビット

VFP/NEON用として、これらとは別に32ビット用はs0〜s31のレジスタがある。これらは、64ビットレジスタとしてd0〜d15として使える。s0〜s31とd0〜d15はオーバーラップしている。大半の ARMv7-A SoC はさらに、d16〜d31も使える。

VFP/NEON用のシステムレジスタとして、以下の3つがある。

  - FPSCR - Floating-point status and control register (浮動小数点状態制御レジスタ)
  - FPEXC - Floating-point exception register (浮動小数点例外レジスタ)
  - FPSID - Floating-point system ID register (浮動小数点システムIDレジスタ)

### 条件実行

ARMの命令セットにおいてユニークなのは、マシン語の最上位4ビットを占める*条件コード*を使用した条件実行命令であり、これによってほぼ全ての命令を分岐命令無しに条件付きで実行することができる。

これにより、マシン語中の即値フィールドに割けるビット数が減ってしまう等の欠点もあるものの、小さなif文に対応するコードの生成時に分岐命令を避けることが可能になる。例として、[ユークリッドの互除法](../Page/ユークリッドの互除法.md "wikilink")を挙げる。

（この例は[C言語](../Page/C言語.md "wikilink")による）

``` c
int gcd(int i, int j)
{
    while (i != j) {
        if (i > j)
            i -= j;
        else
            j -= i;
    }
    return i;
}
```

ARMの[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")では、whileループの部分は以下のようになる。

``` nasm

 loop
        CMP    Ri, Rj       ; i と j を比較
        SUBGT  Ri, Ri, Rj   ; もし "GT" ならば i = i - j;
        SUBLT  Rj, Rj, Ri   ; もし "LT" ならば j = j - i;
        BNE    loop         ; もし "NE" ならば loop に戻る
```

通常分岐命令を使用しなければならないthenやelse節のところで分岐が省かれていることが分かる。

命令セットのもう一つのユニークな機能が、[シフト演算を](https://ja.wikipedia.org/wiki/ビット演算#ビットシフト "wikilink")「データ処理」（算術演算、論理演算、レジスタ間の代入）命令の中に織り込むことができることである。例えば、C言語の

``` c
a += (j << 2);
```

のような文を1つのARM命令

``` nasm
        ADD     Ra, Ra, Rj, LSL #2
```

として表すことができる。（なお、[Intel 80386などでも](../Page/Intel_80386.md "wikilink")1個の命令でできる。

``` asm
LEA EAX,[EAX+EBX*4]
```

とすればよい。）

これにより、多くのARMプログラムは通常RISCプロセッサに期待されるようなプログラムよりも密度の高いものになる。このため、命令フェッチに伴うメモリへのアクセス頻度が少なくなり、分岐に伴うストールも回避しやすく、パイプライン処理を効率的に使うことができる。このことが、ARMがARMより複雑なCPUデザインと競合することを可能にした特徴的な一因のひとつである。

### Thumb

ARMプロセッサは**Thumb**と呼ばれるコード効率の向上を意図した[16ビット](../Page/16ビット.md "wikilink")長の命令モードを持っている([SuperH](../Page/SuperH.md "wikilink")の命令16ビット/データ32ビットに倣い追加された)。条件実行のための4ビットプレディケートが削除されている。メモリポートやバスが32ビットよりも狭い状況において32ビットコードよりも性能が向上する。多くの場合、組み込みアプリケーションでは32ビットのデータパスを持っているのは一部のアドレス範囲のみであり（例: [ゲームボーイアドバンス](../Page/ゲームボーイアドバンス.md "wikilink")）、残りは16ビットかそれよりも狭くなっている。このような状況では、Thumbコードをコンパイルし、CPUに最も負荷のかかる部分だけを32ビット長の命令セットを使用して手作業で最適化するのが、通常は理にかなっている。Thumb命令とARM命令は単一の実行ファイル内で混在が可能であるが、Thumb命令を実行できるモードとARM命令を実行できるモードは独立しており、両者を使うにはその都度プロセッサの状態を切り替える必要がある。状態の切り替えは分岐命令 (BX, BLX) で行うことができるため、通常は関数単位でThumb命令とARM命令を使い分け、関数呼び出しの際に切り替えを行うのが一般的である。

Thumbテクノロジを搭載した最初のプロセッサはARM7TDMIである。ARM9とそれ以降のファミリは、[XScale](../Page/XScale.md "wikilink")も含めて全てThumbテクノロジを搭載している。

### Thumb-2

**Thumb-2**テクノロジは2003年に発表された**ARM1156コア**で登場した。Thumb-2はThumbの制限された16ビット長の命令セットを追加の32ビット長命令で拡張し、命令セットの幅を広げるものである。公称されているThumb-2の目的は、Thumbと同様のコード密度と32ビットメモリ上でのARM命令セットと同様の性能を得ることであり、Thumb-2はビットフィールド操作、テーブル分岐や条件付き実行などを含んでいる。従来はThumbモードにおいて使用可能な汎用レジスタは8本のみであり自由度が低かったが、Thumb-2で導入された32ビット長命令では16本全てのレジスタが使用可能である。16ビット長命令と32ビット長命令はモードの切り替えなしで混在可能であるため、ThumbモードにおいてもARMモードに近い自由度が得られるようになった。

### Jazelle

ARMは、[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")をハードウェアでネイティブに実行できる技術を実装した。これはARMやThumbモードと並ぶもう一つの実行モードであり、ARM/Thumbの切り替えと同様にしてアクセスすることができる。後述のJazelle RCTに対して**Jazelle DBX** (Direct Bytecode eXecution) とも言う。

Jazelleテクノロジを搭載した最初のプロセッサは**ARM926EJ-S**である。CPU名の'J'がJazelleを表している。

### Thumb Execution Environment (ThumbEE)

**ThumbEE**は**Jazelle RCT** (Runtime Compilation Target)とも呼ばれる第4のモードである。2005年にアナウンスされ、**Cortex-A8**プロセッサで最初に実装された。Thumb-2命令セットに小規模な変更を加えたもので、[JITコンパイラ](https://ja.wikipedia.org/wiki/JITコンパイラ "wikilink")のように実行時にコードを生成する場合に向いている。主な対象は[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[.NET](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") [MSIL](../Page/共通中間言語.md "wikilink")（[C\#など](../Page/C_Sharp.md "wikilink")）、[Python](../Page/Python.md "wikilink")、[Perl](../Page/Perl.md "wikilink")などの言語である。

### DSP 拡張命令

[デジタル信号処理](../Page/デジタル信号処理.md "wikilink")とマルチメディアアプリケーション向けに ARMアーキテクチャを拡張するため、いくつかの命令が追加された[4](http://www.arm.com/products/CPUs/cpu-arch-DSP.html)。**ARMv5TE** と **ARMv5TEJ** というアーキテクチャ名の "E" がこれを表していると思われる。

追加された命令は、[デジタルシグナルプロセッサ](../Page/デジタルシグナルプロセッサ.md "wikilink")アーキテクチャで一般的なものである。例えば、符号付積和演算、飽和加算と飽和減算、「先行する0のカウント」のバリエーションである。

### SIMD

ARMv6で導入された\[30\]。32ビット幅。

### Advanced SIMD (NEON)

**Advanced SIMD**拡張は**NEON**とも呼ばれ、メディアおよびデジタル信号の処理に向いた64ビットと[128ビット](https://ja.wikipedia.org/wiki/128ビット "wikilink")の[SIMD](../Page/SIMD.md "wikilink")命令セットである。8/16/32/64ビットの整数演算と、32ビット (単精度) 浮動小数点演算のためのSIMD命令が定義されており、ARMv7から利用可能。32ビットCPUでは倍精度浮動小数点数は利用不可で、倍精度にはVFPを使用。

ほとんどの ARMv7 SoC で NEON に対応しているが、[NVIDIA Tegra](https://ja.wikipedia.org/wiki/NVIDIA_Tegra "wikilink") 2 シリーズ、SPEAr1310、SPEAr1340 などで対応していない。

レジスタはVFPレジスタとして用意されている32本の64ビットレジスタを用いて、32本の64ビットSIMDレジスタ (D0-D31) 、もしくは16本の128ビットSIMDレジスタ (Q0-Q15) としてアクセスできる。例えば128ビットレジスタQ0はD0とD1の2つの64ビットレジスタの領域にマッピングされている。

Cortex-A15 などより、NEONv2 (version 2) が搭載され、Fused Multiply-Add ができる。これにより、単精度浮動小数点数で 8 FLOPS/cycle となった。

### Wireless MMX

**Wireless MMX** (WMMX) はインテルが[XScale](../Page/XScale.md "wikilink")プロセッサ向けに開発したSIMD命令セットである。64ビット幅のレジスタが16本用意されており、8/16/32/64ビットのSIMD整数演算が可能。XScaleとその売却先であるマーベル・テクノロジー・グループ製のARM SoCに採用されている。命令セット自体はx86プロセッサのMMXとは全く異なるものの、[GCCや](../Page/GNUコンパイラコレクション.md "wikilink")[Visual C++等のコンパイラで利用できる組み込み関数はMMXとの互換性がある程度確保されており](https://ja.wikipedia.org/wiki/Visual_C++ "wikilink")、これを利用すればMMX向けに記述されたコードを比較的容易に移植することができる。

### VFP

**VFP** (Vector Floating Point) はARMアーキテクチャのコプロセッサ拡張である。半精度（v3以降）・単精度・倍精度の[浮動小数点](https://ja.wikipedia.org/wiki/浮動小数点 "wikilink")演算機能を提供する。

  - VFPv1 - 廃止
  - VFPv2 - ARMv5TE、ARMv5TEJ、ARMv6 で利用可能
  - VFPv3 - ARMv7 で利用可能。通常はレジスタ数32個であるが、[NVIDIA Tegra](https://ja.wikipedia.org/wiki/NVIDIA_Tegra "wikilink") 2 シリーズなどはレジスタ数が半分のVFPv3-D16を採用。Cortex-A8の実装はパイプライン化されておらず非常に低速 (VFP Lite)。
  - VFPv4 - Cortex-A5, A7, A15, [Apple A6](https://ja.wikipedia.org/wiki/Apple_A6 "wikilink"), [Snapdragon](https://ja.wikipedia.org/wiki/Snapdragon "wikilink") Krait などで利用可能。[IEEE754準拠の](../Page/IEEE_754.md "wikilink")（乗算結果の丸めを行わない）Fused multiply add 対応。VFPv4-D16 もあり。

"Vector" の名を冠する通り、いくつかの命令においてはベクタモードと呼ばれる1命令で複数のレジスタに対して演算を行うモードが用意されている。このモードを使えば[SIMD](../Page/SIMD.md "wikilink")演算が可能であるが、プログラミングモデルがやや煩雑であったことや、当時のARM11プロセッサにおける実装はスカラ命令を要素数分だけシーケンシャルに実行するというSIMD演算のメリットを享受できないものであったため、あまり積極的には使われなかった。VFPv3を実装するARMv7世代以降ではモダンなSIMD命令セットであるAdvanced SIMD拡張命令 (NEON) が導入されたため、現在ではベクタモードの利用は推奨されていない。Cortex-A9やA15ではベクタモードに対応していないことから分かるように、現在のARMアーキテクチャにおけるVFPの位置づけはスカラ専用の浮動小数点演算コプロセッサであり、SIMD演算用途についてはNEONに道を譲っている。

単精度の浮動小数点演算はNEONでも実行可能であるが、倍精度の浮動小数点演算やIEEE754準拠の4つの丸めモード、非正規化数のサポート等はNEONには存在しないため、これらを利用したい場合はVFP命令を使う必要がある。

## 64ビットARM

ARMv8-Aから採用。ARMの64ビットモードアーキテクチャAArch64では、汎用レジスタはすべて64ビットとなり、数も16個から31個に増やされる。サーバ用途も意識して[仮想化](../Page/仮想化.md "wikilink")支援命令および[暗号](../Page/暗号.md "wikilink")支援命令が追加され、[SIMD](../Page/SIMD.md "wikilink")拡張命令であるNEONも大幅に強化される。

### 命令セットの特徴

汎用レジスタの増加と64ビット化に伴い、命令セットは完全に再定義されている。コード効率を重視して命令長は32ビットのままで、32ビットARMの特徴であった条件付き実行命令の大半が削除される。これによって一般的なRISC命令セットに近くなったが、依然としてコードサイズを小さくするための工夫が随所に織り込まれている。

AArch64モードにおける命令セットはA64と呼ばれ、以下にA64命令セットの特徴を示す。

  - 即値シフト付きオペランド
    これは従来の32ビットARM命令セットにおいて*フレキシブル第2オペランド (Flexible second operand)* と呼ばれていたものに相当する。多くの基本的な演算命令においては、入力オペランドのうち1つに対する操作を即値左シフト、即値論理右シフト、即値算術右シフト、シフトなし、の4つから選択することができ、演算命令と即値シフト命令を一体化することができる。なお、従来とは異なりローテートは不可能となった。
  - 条件付き実行命令
    汎用レジスタ数が倍増したのに伴い、基本命令の多くからは条件付き実行機能が削除されたが、それでも比較的豊富な条件付き実行命令が定義されている。代表的なものを挙げるとCCMP（条件付き比較）、CINC（条件付きインクリメント）、CSEL（条件付き選択; いわゆるCMOV）等が存在する。
  - Compare-and-Branch命令
    PC相対分岐においては、ゼロフラグを参照する場合のみであるが比較と条件分岐を1命令で行うことが可能になっている (CBZ/CBNZ)。これは従来Thumb-2命令セットでのみ定義されていたものであるが、A64モードでは基本命令として定義されている。
  - 符号拡張/ゼロ拡張付き命令
    算術演算/比較命令については、入力オペランドのうち1つを8,16,32ビットから32もしくは64ビットに符号/ゼロ拡張するバージョンが用意されている。

汎用レジスタは64ビット幅であるが、多くの演算命令にはレジスタの下位32ビットのみを参照する32ビット命令が用意されている。この場合、レジスタの部分書き換えが発生しないように、演算結果の32ビットの値は暗黙のゼロ拡張が行われた上で64ビットレジスタに格納される。

### SIMD and Floating-point (NEON) 命令

A64命令セットにおいては従来のVFPとAdvanced SIMD (NEON) は統合され、一つの命令体系となった。これに伴い、名称については単にSIMD and Floating-point命令と呼ばれるようになった。

主な変更点は倍精度浮動小数点演算への対応、IEEE754への準拠、レジスタ本数の増加の3点である。レジスタについては128ビットのレジスタが32本に増加している。依然として64ビットレジスタとしてアクセスすることも可能であるが、32ビットモードとは異なり、64ビットレジスタは128ビットレジスタの下位64ビットにマッピングされている。

VFPとAdvanced SIMDの統合に伴い、従来はVFPが担っていたスカラの浮動小数点演算命令は、SIMDレジスタのうち下位の32/64ビットにのみ作用する命令として再定義されている。例えば浮動小数点加算命令については

``` nasm
 fadd  s2, s1, s0             ; s2 <= s0 + s1（単精度スカラ）
 fadd  d2, d1, d0             ; d2 <= d0 + d1（倍精度スカラ）
 fadd  v2.4s, v1.4s, v0.4s    ; [v2] <= [v0] + [v1]（単精度x4 SIMD）
 fadd  v2.2d, v1.2d, v0.2d    ; [v2] <= [v0] + [v1]（倍精度x2 SIMD）
```

のようなバリエーションが命令のニーモニックを保ちつつ、オペランドのプレフィックス (s, d, v) とサフィックスを変更することによって記述可能になっている（サフィックスについては、一部の環境向けのアセンブラではニーモニック側に付加する省略記法も許されるようである）。これはx86プロセッサのSSE命令セットがスカラ命令とSIMD命令の双方を備えているのとよく似ている。

## 脚注

### 注釈

### 出典

## 関連項目

  - [μClinux](https://ja.wikipedia.org/wiki/μClinux "wikilink")
  - [ソフィー・ウィルソン](https://ja.wikipedia.org/wiki/ソフィー・ウィルソン "wikilink")

## 外部リンク

  - [ARM Ltd.](http://www.arm.com/)
  - [Linux Zaurusでアセンブリプログラミング](http://www.mztn.org/slasm/arm_idx.html)

[Category:ARMアーキテクチャ](https://ja.wikipedia.org/wiki/Category:ARMアーキテクチャ "wikilink") [Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink") [Category:コンピュータアーキテクチャ](https://ja.wikipedia.org/wiki/Category:コンピュータアーキテクチャ "wikilink")

1.  <http://www.arm.com/miscPDFs/3823.pdf>
2.  NEC、モバイル機器でフルHD動画や5.1chサウンドを再生できるLSI「EMMA Mobile／EV」を発売へhttp://gigazine.net/news/20100208_nec_emma_mobile/
3.  <http://www.jp.arm.com/pressroom/08/080125.html>
4.  <https://news.mynavi.jp/articles/2010/09/10/cortex-a15/index.html>
5.  <http://ascii.jp/elem/000/000/645/645995/>
6.
7.
8.  [2005年](../Page/2005年.md "wikilink")、ARM社のセミナー資料による。
9.   プレスリリース{{\!}} クリエ用新アプリケーションCPU「Handheld EngineTM」の開発について|url=[https://www.sony.co.jp/SonyInfo/News/Press_Archive/200307/03-0717/|website=www.sony.co.jp|accessdate=2019-04-08](https://www.sony.co.jp/SonyInfo/News/Press_Archive/200307/03-0717/%7Cwebsite=www.sony.co.jp%7Caccessdate=2019-04-08)}}
10. [News：米速報：次世代マイクロアーキテクチャ「ARM11」発表](http://www.itmedia.co.jp/news/0204/30/b_0429_01.html)
11. [Googleが新型「Chromebook」を発表、Samsung製で249ドル](http://internet.watch.impress.co.jp/docs/news/20121019_567253.html)
12. [【PC Watch】 Samsung、初のARM Cortex-A15プロセッサ「Exynos 5250」](http://pc.watch.impress.co.jp/docs/news/20111202_495443.html)
13. [日本TI、モバイルの概念を一変させる高性能、高機能のOMAP™5プラットフォームを発表](http://newscenter.ti.com/jp/Blogs/newsroom/archive/2011/02/10/ti-omap-5.aspx)
14. [【後藤弘茂のWeekly海外ニュース】 ARMが次世代CPU「Atlas」と「Apollo」の計画を発表](http://pc.watch.impress.co.jp/docs/column/kaigai/20120214_511793.html)
15. [AMD’s K12 ARM CPU Now In 2017](http://www.anandtech.com/show/9232/amds-k12-arm-cpu-now-in-2017)
16. [苦難の2013年を越え、輝かしい2014年に賭けるAMD (大きな期待が寄せられているサーバー向け64ビットARMプロセッサ)](http://cloud.watch.impress.co.jp/docs/column/virtual/20130702_605540.html)
17. [ARM Sets New Standard for the Premium Mobile Experience - ARM](http://www.arm.com/about/newsroom/arm-sets-new-standard-for-the-premium-mobile-experience.php)
18. [Qualcomm Introduces Next Generation Snapdragon 600 and 400 Tier Processors for High Performance, High-Volume Smartphones with Advanced LTE | Qualcomm](https://www.qualcomm.com/news/releases/2015/02/18/qualcomm-introduces-next-generation-snapdragon-600-and-400-tier-processors)
19. ["ARM Cortex-M1"](http://www.arm.com/products/CPUs/ARM_Cortex-M1.html), ARM product website. Accessed April 11, 2007.
20. ["ARM Extends Cortex Family with First Processor Optimized for FPGA"](http://www.arm.com/news/17017.html), ARM press release, March 19 2007. Accessed April 11, 2007.
21. [ARM Cortex-M1](http://www.altera.co.jp/products/ip/processors/32_16bit/m-arm-cortex-m1.html)
22. [Actel: 製品とサービス: プロセッサ: ARM: Cortex-M1](http://www.actel.com/intl/japan/products/mpu/cortexm1/)
23. [AnandTech | Cortex-M7 Launches: Embedded, IoT and Wearables](http://www.anandtech.com/show/8542/cortexm7-launches-embedded-iot-and-wearables/2)
24. [Cortex-M7 Overview - ARM](https://developer.arm.com/products/processors/cortex-m/cortex-m7)
25. [Cortex-M23 Overview - ARM](https://developer.arm.com/products/processors/cortex-m/cortex-m23)
26. [Cortex-M33 Overview - ARM](https://developer.arm.com/products/processors/cortex-m/cortex-m33)
27.
28.
29. [2.14. The program status registers - Cortex-A8 Technical Reference Manual](http://infocenter.arm.com/help/index.jsp?topic=/com.arm.doc.ddi0290g/I27695.html)
30. [DSP & SIMD - ARM](http://www.arm.com/ja/products/processors/technologies/dsp-simd.php)