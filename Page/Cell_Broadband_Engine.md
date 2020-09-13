> この記事は[Cell Broadband Engine](https://ja.wikipedia.org/wiki/Cell_Broadband_Engine)から翻訳されています。


**Cell Broadband Engine**（セル ブロードバンド エンジン、略称: **Cell/B.E.**、**Cell**、**CBE**）は、[ソニー・コンピュータエンタテインメント](https://ja.wikipedia.org/wiki/ソニー・コンピュータエンタテインメント "wikilink") (SCE) 、[ソニー](../Page/ソニー.md "wikilink")、[IBM](../Page/IBM.md "wikilink")、[東芝](../Page/東芝.md "wikilink")によって開発された[PowerPC](../Page/PowerPC.md "wikilink")アーキテクチャベースの[64ビット](../Page/64ビット.md "wikilink")[RISC](../Page/RISC.md "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")である\[1\]。

[Emotion Engineの実質的な後継](../Page/Emotion_Engine.md "wikilink")。ソニーは本プロセッサの後継を発表していないが、東芝は後継として[レグザエンジンCEVO](https://ja.wikipedia.org/wiki/レグザエンジンCEVO "wikilink")（CEVOはCell Evolutionの意）\[2\]を開発している。また、IBMは本プロセッサの後継となるPowerXcellを開発した。

## 概要

主に大容量データを効率良く処理するための[ストリーム・プロセッシング](https://ja.wikipedia.org/wiki/ストリーム・プロセッシング "wikilink")を志向したプロセッサである。GPGPUと言う言葉が無い頃に、プログラム全体の制御を担う汎用コアとデータ処理に特化した補助コアのヘテロ構成のアーキテクチャを実現した。

Cell誕生のきっかけであったSCEの[家庭用ゲーム機](https://ja.wikipedia.org/wiki/家庭用ゲーム機 "wikilink")である「[PlayStation 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")」を筆頭に、一部の[サーバー](https://ja.wikipedia.org/wiki/サーバー "wikilink")や[ワークステーション](../Page/ワークステーション.md "wikilink")、[薄型テレビ](../Page/薄型テレビ.md "wikilink")などの様々な製品に採用された。また、[米エネルギー省が保有する](../Page/アメリカ合衆国エネルギー省.md "wikilink")[スーパーコンピューター](https://ja.wikipedia.org/wiki/スーパーコンピューター "wikilink")「[Roadrunner](https://ja.wikipedia.org/wiki/Roadrunner "wikilink")」や、同アーキテクチャーのプロセッサのみで構成されたシステム「[QPACE](https://ja.wikipedia.org/wiki/:en:QPACE "wikilink")」が、スーパーコンピューターランキング[TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")のみならず電力効率を争う[Green500のランキングも賑わせた](https://ja.wikipedia.org/wiki/:en:Performance_per_watt#Green500_List "wikilink")。

Cellは年々改良され、90nm→65nm→45nmと微細化された。なお、SCEは「[PlayStation 4](https://ja.wikipedia.org/wiki/PlayStation_4 "wikilink")」にはCellを採用せずAMD社のJaguarコアを採用した。

Cellは独自色が強く普及しなかったが、[ヘテロジニアスマルチコア](../Page/ヘテロジニアスマルチコア.md "wikilink")という構造は、2010年代にCPUとGPUをワンチップに収めたAMDのAPU等で普及している。

## 特徴

Cellは[マルチコア](../Page/マルチコア.md "wikilink")に分類され、ひとつのマイクロプロセッサに9つのコアを持っている。内訳には1個の汎用的なプロセッサコアと、8個のシンプルなプロセッサコア（うち1基は歩留まり向上のため非使用）を組み合わせた[ヘテロジニアスマルチコア](../Page/ヘテロジニアスマルチコア.md "wikilink")（ヘテロジニアス: 非対称、異種混合）という形態をもつ。

汎用プロセッサコアは*[PowerPC Processor Element](https://ja.wikipedia.org/wiki/#PowerPC_Processor_Element "wikilink")* (PPE) と呼ばれる制御を担うコアで、8個のコアは*[Synergistic Processor Element](https://ja.wikipedia.org/wiki/#Synergistic_Processor_Element "wikilink")* (SPE) と呼ばれる演算を担うコアである。

PPE、SPE共に従来の[パソコン向けのマイクロプロセッサである](../Page/パーソナルコンピュータ.md "wikilink")[PowerPC G5や](../Page/PowerPC_970.md "wikilink")[Pentium 4](../Page/Pentium_4.md "wikilink")、[Athlon 64といった高度な](../Page/Athlon_64.md "wikilink")[アウト・オブ・オーダー実行](../Page/アウト・オブ・オーダー実行.md "wikilink")機能や[分岐予測](../Page/分岐予測.md "wikilink")機構を持つマイクロプロセッサとは異なり、[命令を並べ替えたりするような複雑な](../Page/命令_\(コンピュータ\).md "wikilink")[スケジューリング](../Page/スケジューリング.md "wikilink")機構を搭載しないことでコアを単純化し、高[クロック](../Page/クロック.md "wikilink")化を実現している。

そのため、複雑な条件分岐を伴う整数演算能力はパソコン向けのマイクロプロセッサと比べ劣るが、強力で高度に[並列化](../Page/並列化.md "wikilink")された演算機能を備え、[数値解析](https://ja.wikipedia.org/wiki/数値解析 "wikilink")や[シミュレーション](../Page/シミュレーション.md "wikilink")、[動画](../Page/動画.md "wikilink")、[画像処理](../Page/画像処理.md "wikilink")、[音声処理](https://ja.wikipedia.org/wiki/音声処理 "wikilink")などにおいては、複数のコアを並列に動作させることによって、Cellの性能を発揮させることができる。

また、[仮想マシン支援機能が搭載されており](../Page/仮想機械.md "wikilink")、複数の仮想マシン上で複数のOS（ゲストOS）を互いに干渉させること無く走らせることができる。通常のOSが動作する[スーパーバイザー](../Page/カーネル.md "wikilink")[モードの上位に](../Page/CPUモード.md "wikilink")[ハイパーバイザ](../Page/ハイパーバイザ.md "wikilink")ーモードがあり、仮想マシンを管理する最上位OSはこのハイパーバイザーモードで動作している。

PowerPCは[バイエンディアンだが](https://ja.wikipedia.org/wiki/エンディアン "wikilink")、Cellではビッグエンディアンで統一している。

## プロセッサアーキテクチャ

### PowerPC Processor Element

[thumb](https://ja.wikipedia.org/wiki/ファイル:PPE_\(Cell\).png "wikilink") PPE は[64ビット](../Page/64ビット.md "wikilink")[Powerアーキテクチャであり](https://ja.wikipedia.org/wiki/Power_Architecture "wikilink")、命令セットはPowerPC G5互換ではあるが、既存の[PowerPC](../Page/PowerPC.md "wikilink")系CPUとは異なる内部構造をもつ新設計のコアである。2[スレッドを交代に実行することが可能で](../Page/スレッド_\(コンピュータ\).md "wikilink")、スレッドの切り換えが速い事から、[OSの駆動などを受け持つ](../Page/オペレーティングシステム.md "wikilink")。また、[AltiVec](../Page/AltiVec.md "wikilink")にも対応している。

PowerPC Architecture,Book I〜III に準拠することが求められ、中にはBook I〜IIIでのオプション仕様がPPEでは必須になっているものがある。[VMXもその一つ](https://ja.wikipedia.org/wiki/AltiVec#Vector_Multimedia_Extension "wikilink")。

PPEの[浮動小数点演算性能はIBMの示した](../Page/浮動小数点数.md "wikilink")[布シミュレーション](https://ja.wikipedia.org/wiki/布シミュレーション "wikilink")の例では、2.4[GHz駆動のPPEがPentium](../Page/ギガヘルツ.md "wikilink") 4 3.6GHz相当CPUの20%程度のパフォーマンスしか出ておらず、浮動小数点演算は得意ではないと言え、通常はSPEなどへの[リソースマネージメントを行うことになる](https://ja.wikipedia.org/wiki/計算資源#システム資源管理 "wikilink")\[3\]。

Cellの仕様を満たすためには最低1つは搭載することが求められる。

### Synergistic Processor Element

[thumb](https://ja.wikipedia.org/wiki/ファイル:SPE_\(cell\).png "wikilink") SPE は [SIMD](../Page/SIMD.md "wikilink")系の[アーキテクチャ](../Page/アーキテクチャ.md "wikilink")で、単精度浮動小数点演算を4スロット同時に処理することができ、倍精度浮動小数点演算を2スロット同時に演算できる。また整数も16ビット値を8スロット、32ビット値を4スロットの演算ができる。以上のような[ベクトル演算](https://ja.wikipedia.org/wiki/ベクトル演算 "wikilink")が可能な128ビット長128個のレジスタを持ち、ソフトウェアパイプライニングなど処理の最適化を可能とする。また、[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")は持たず代わりに256[KiBのローカルストア](https://ja.wikipedia.org/wiki/キビバイト "wikilink") (LS) と呼ばれる[SRAM専用メモリを持っており](../Page/Static_Random_Access_Memory.md "wikilink")、そこにプログラムとデータを格納して実行する。SPEはメインメモリ上のプログラムとデータを直接扱えず、[DMAを用いて](../Page/Direct_Memory_Access.md "wikilink")[XDR DRAMメモリとLS間の転送を行う必要がある](../Page/XDR_DRAM.md "wikilink")。LSはメインメモリから独立した[メモリ空間を持つため](../Page/アドレス空間.md "wikilink")、[キャッシュコヒーレンシ](https://ja.wikipedia.org/wiki/キャッシュコヒーレンシ "wikilink")保持の仕組みが不要で高速化に貢献している。例えるなら常にL1キャッシュに当たっている状態である。SPEは*Memory Flow Controller* (MFC) と呼ばれる制御ユニットに専用のDMAコントローラを持ち、これによりSPEは多量のデータを高速に処理する[ストリーム処理を可能とする](https://ja.wikipedia.org/wiki/ストリーム・プロセッシング "wikilink")。IBMの示した物理挙動シミュレーションと[レンダリングの例では](../Page/レンダリング_\(コンピュータ\).md "wikilink")、3.2GHzのPentium 4と比較し、2.1GHz駆動のSPE1基で1.5倍、8基で12倍の性能差を記録した\[4\]。IBMの示したシミュレーションをPentium 4 3.6GHzクラスのCPUで実装した場合との比較では3基のSPEでPentium 4 3.6GHzクラスCPUの2倍のパフォーマンスを記録した\[5\]。命令長は32ビット固定である。

1基あたり3.2GHz駆動で25.6GFLOPSの演算性能がある\[6\]。

Cellの仕様を満たすためには最低1つは搭載することが求められる。

#### アイソレーションモード

セキュリティ強化のため、SPEはアイソレーションモードと呼ばれる特殊な動作モードを備えている\[7\]。これは、暗号化・復号処理や[CSSや](../Page/Content_Scramble_System.md "wikilink")[AACSなどの](../Page/Advanced_Access_Content_System.md "wikilink")[デジタル著作権管理](../Page/デジタル著作権管理.md "wikilink")システムでの利用が想定されている。

アイソレーションモードで動作するSPEのLS領域は他のSPEやPPEからのアクセスが遮断され、外部からの読み書きは一切できない。アイソレーションモードで[暗号](../Page/暗号.md "wikilink")に用いる[秘密鍵などの機密情報を扱うことで](../Page/鍵_\(暗号\).md "wikilink")、他のプロセスからそれらを盗み取ることを不可能にする。

SPEはアイソレーションモード用の移行・離脱命令を実行することでそのモードに遷移する。一旦SPEがアイソレーションモードに入ると、外部から可能な操作はそのSPEで動作するプロセスの停止のみである。離脱命令および外部からのプロセス停止が実行されると、SPEのコンテキストおよびそのLSに置かれたプログラムやデータは速やかに消去されるため、機密情報が外部に漏洩することは無い。また、アイソレーションモードで実行されるプログラムコードは、それが本来のものと改変されていないか検証してから実行されるため、第三者による有害なコードを実行する危険性を排除している。

プロセス間の干渉を防ぐ機構として多くのプロセッサでは[CPUモード](../Page/CPUモード.md "wikilink")を備えているが、[スーパーユーザー](../Page/スーパーユーザー.md "wikilink")などの元々高い権限を持つユーザが有害なプロセスを特権モードで動作させた場合にはこれを防止できない。アイソレーションモードはこのような場合でも機密情報を守ることが可能である。

### 入出力

プロセッサコア以外に、[Rambus](https://ja.wikipedia.org/wiki/Rambus "wikilink")社からライセンス供与を受けた帯域幅25.6[GB](../Page/ギガバイト.md "wikilink")/sの新メモリ*[XDR DRAM](../Page/XDR_DRAM.md "wikilink")*の[メモリコントローラ](https://ja.wikipedia.org/wiki/メモリコントローラ "wikilink")と、チップ間接続のための新[インタフェース](../Page/インタフェース_\(情報技術\).md "wikilink")*FlexIO*も搭載する。FlexIOの帯域幅は最大76.8GB/sとなる。Cell内のコアとこれらのインタフェース群はやはり広帯域のリング状内部バス*Element Interconnect Bus* ([EIB](https://ja.wikipedia.org/wiki/#EIB "wikilink"))と呼ばれるもので接続される。

### IIC

Internal Interrupt Controller の事であり、Cell内部で[割り込み処理を担っている](../Page/割り込み_\(コンピュータ\).md "wikilink")。外部からの割り込み信号の対応や内部のPPEやSPEから発せられた割り込みを外部に伝えたりしている。

### EIB

Element Interconnect Bus の事であり、Cell内部のメインバスとして各部を接続している。現在の実装（PPE×1+SPE×8）ではリングバス構造をしている。

コア個数など仕様によって最適な実装が大きく異なるのでCell仕様の範囲外とされている。EIBとしての役目が果たせるならば実装上の制限は無い。

### 構成

2005年現在はコアが9個（PPE×1+SPE×8）搭載されているが、これはCell Broadband Engine アーキテクチャと呼ばれる規格化された拡張可能なアーキテクチャの一実装形態であり、これを1PEとした4PE（PPE×4+SPE×32）など多様な構成を取り得る\[8\]。

Cell Broadband Engineアーキテクチャ仕様書ではPPEとSPEがそれぞれ一つ以上が含まれる事を要求している。さらにIIC、EIBがそれぞれ一つ含まれる事を要求している\[9\]。

東芝が2007年9月に発表した\[10\]Cellベースのメディアプロセッサ「[SpursEngine](https://ja.wikipedia.org/wiki/SpursEngine "wikilink")」は、SPEを4個と[MPEG-2](../Page/MPEG-2.md "wikilink")、[H.264](../Page/H.264.md "wikilink")の[エンコード](../Page/エンコード.md "wikilink")・デコード回路を搭載し、動作周波数もCellより低い1.5GHz駆動(10W台)という構成である。

### ビット長呼称

CPUの[ニーモニック](https://ja.wikipedia.org/wiki/ニーモニック "wikilink")によってビット長呼称が違っているが、Cellの場合は以下の通りになっている。

| ビット長 | 名称                                      |
| ---- | --------------------------------------- |
| 128  | クワッドワード                                 |
| 64   | ダブルワード                                  |
| 32   | [ワード](../Page/ワード.md "wikilink")        |
| 16   | ハーフワード                                  |
| 8    | [バイト](../Page/バイト_\(情報\).md "wikilink") |

## プログラミングモデル

CellのSPEは通常のマルチプロセッサと異なり各SPEが独立したメモリ空間を持ち、また[分岐予測](../Page/分岐予測.md "wikilink")などのハードウェア機構を持たないため、その性能を十分に引き出すにはそれに合わせたプログラミングモデルを採用する必要がある。Cellの開発者たちは次のようなモデルを提案している\[11\]。

### ジョブ・キュー

PPEがシステムメモリ上の[ジョブ](https://ja.wikipedia.org/wiki/ジョブ "wikilink")・[キューを管理し](../Page/キュー_\(コンピュータ\).md "wikilink")、複数のSPEにジョブを割り当てて管理する。ジョブ・キューからジョブをDMAコントローラを介してローカルストアに読み込む *mini kernel* が各SPE上で走り、ジョブを実行した結果をシステムメモリに返し、PPEと同期を取る。

### SPEによる自己マルチタスク

各SPEにkernelを持ち、共有メモリのタスク・キューを使い、分散してスケジュールが行なわれる。タスクの同期は、[ミューテックス](../Page/ミューテックス.md "wikilink")または[セマフォ](../Page/セマフォ.md "wikilink")により実現される。

### ストリーム・プロセッシング

各SPEは、input stream からの入力データに対してカーネル関数を実行し、その結果をoutput stream に送る。これは、シリアルまたは並列パイプラインを容易に実現する。このモデルは、データができるだけ長くローカルストアに存在するので効率がよい\[12\]。

### 最適化コンパイラ

最適化は、Synergistic Processing Unit (SPU) のインストラクションレベル、自動[SIMD](../Page/SIMD.md "wikilink")化、共有メモリモデルの自動並列化の3レベルがある。SPUのインストラクションレベルでは、ハードウエアで分岐予測を持たないので、分岐ヒント命令を少なくとも分岐の11サイクル前に自動的にスケジュールする。共有メモリモデルの自動並列化は、[OpenMP](../Page/OpenMP.md "wikilink")で記述された1つのソースからPPEとSPEに自動分割する。SPEにおいては、コードは自動分割され、規則的なデータは共有メモリとローカルストア間のDMA命令に自動生成され、不規則なデータはソフトウエアキャシュにより処理される。ソフトウエアキャッシュ（4 way set [連想メモリ](../Page/連想メモリ.md "wikilink")）は、SIMD命令で実行される。

## Cellコンピューティング

Cellコンピューティングとは[久夛良木健](../Page/久夛良木健.md "wikilink")によれば以下の2つが要点となる\[13\]。

  - 従来のネットワークは情報のネットワークだったが、それが[ピア・ツー・ピアコンピューティングのバスになる](../Page/Peer_to_Peer.md "wikilink")。
  - 従来のバッチで非[リアルタイム](../Page/リアルタイム.md "wikilink")の[グリッド・コンピューティング](../Page/グリッド・コンピューティング.md "wikilink")から、リアルタイムでのグリッドコンピューティングへ。

Cellではこのリアルタイムな処理分散を実現する前提の設計がなされている。SPEが独自にSPE用メインメモリーであるとも言えるローカルストアを持っている理由の一つには、この一環もある。

PS3発売当初のSCEは、PS3を核とした複数の機器による家庭内ネットワークでのCellコンピューティングを提唱していた\[14\]。しかし、久夛良木がSCE社長を退いて[平井一夫](../Page/平井一夫.md "wikilink")体制になって以降は、Cellコンピューティングについて触れられることはほとんど無くなった。現状ではCellコンピューティングが行える環境は整備されておらず、実現できる見通しも立っていない。[PlayStation 4ではCell](https://ja.wikipedia.org/wiki/PlayStation_4 "wikilink") Broadband Engineではなく他社製のチップをCPUに採用したため、Cellコンピューティング構想は事実上放棄された形となっている。

## 評価

多数のコアを備えることにより処理能力の向上を実現したCell Broadband Engineの登場は衝撃的であった\[15\]。当時のPS3に搭載されたCell Broadband Engineのチップ全体のスループットは、当時の汎用PC向けCPUの10倍程度に達した\[16\]。その影響は大きく、IntelやAMDなどCPUベンダーは勿論、GPUベンダーまでもコアを肥大化させてシングルスレッド性能を追求する方向から、マルチコア化によってチップ全体での処理能力を追求する方向に転じた\[17\]。GPUコアをCell B.E.のように汎用処理にも使用するというアイデアを展開していった\[18\]。

## 沿革

  - [2001年](../Page/2001年.md "wikilink")[3月9日](../Page/3月9日.md "wikilink") - SCE、IBM、東芝がブロードバンド時代に向けた超並列プロセッサの共同研究および開発に合意。
  - [2004年](../Page/2004年.md "wikilink")[11月29日](../Page/11月29日.md "wikilink") - SCE、IBM、ソニー、東芝が次世代プロセッサ「Cell」について[ISSCC](https://ja.wikipedia.org/wiki/ISSCC "wikilink")（国際固体素子回路会議）に関連する論文を提出と発表。
  - [2005年](../Page/2005年.md "wikilink")
      - [2月](https://ja.wikipedia.org/wiki/2月 "wikilink") - 米国で開催されたISSCC（国際固体素子回路会議）で概要を公表、試作品が初披露された。
      - [3月31日](../Page/3月31日.md "wikilink") - [Transmeta](https://ja.wikipedia.org/wiki/Transmeta "wikilink")社がCell派生品などに自社の省電力技術「**LongRun2**」を組み込んでいくことを発表した\[19\]\[20\]。
      - [5月17日](../Page/5月17日.md "wikilink") - [E3において](../Page/Electronic_Entertainment_Expo.md "wikilink") [PLAYSTATION 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink") に搭載されるCellが3.2GHz動作で1PPE+7SPEであることが発表された。7SPEなのは、SPE一つが不良でも動作するようにし、[歩留まり](../Page/歩留まり.md "wikilink")向上を計ったとのこと\[21\]。
      - [6月](../Page/6月.md "wikilink") - 米Mercury Computer Systemsがサーバ/ワークステーションの開発を表明。2006年春から評価ボードを発売。2007年初頭までにブレードサーバシステムもリリースしている。なお、2006年夏にはCELLを用いたアクセラレータボードを発表している。
      - [8月25日](../Page/8月25日.md "wikilink") - SCE、IBM、ソニー、東芝はCellブロードバンド・エンジン・アーキテクチャの革新的な技術の詳細について、主要な技術仕様書を公開（英語）。
      - [9月](../Page/9月.md "wikilink") - [東芝](../Page/東芝.md "wikilink")がデジタル家電向けの開発キットを発表。
      - [9月7日](../Page/9月7日.md "wikilink") - 公式サイトの技術仕様書の一部に日本語版追加。
      - [11月9日](../Page/11月9日.md "wikilink") - 開発キットおよび関連仕様書「Cell Broadband Engine Software Development Kit（CBE SDK）」を公開。
      - [12月14日](../Page/12月14日.md "wikilink") - 公式サイトの技術仕様書の一部に日本語版追加。同年8月25日から英語版で公開されていた物の日本語版が揃う。
  - [2006年](../Page/2006年.md "wikilink")
      - [2月8日](../Page/2月8日.md "wikilink") - 米IBMがCellプロセッサを採用したブレードサーバを開発したと発表。2006年9月に発売開始（価格は1台100万円台〜）。
      - [9月](../Page/9月.md "wikilink") - IBM、[ロスアラモス国立研究所](../Page/ロスアラモス国立研究所.md "wikilink")の[ペタ](https://ja.wikipedia.org/wiki/ペタ "wikilink")[フロップススパコン計画Roadrunnerシステムにアクセラレータとして採用](../Page/FLOPS.md "wikilink")\[22\] \[23\]。
      - [11月11日](../Page/11月11日.md "wikilink") - **90nm**プロセスのCellを搭載したPLAYSTATION 3が発売\[24\]。
      - [11月15日](../Page/11月15日.md "wikilink") - [ジョージア工科大学](http://sti.cc.gatech.edu/)がSony-Toshiba-IBM（第三者による自主的活動拠点）Center of Competenceとして選定された。
  - [2007年](../Page/2007年.md "wikilink")
      - [2月](https://ja.wikipedia.org/wiki/2月 "wikilink") - IBMが、ISSCC(IEEE International Solid-State Circuits Conference)2007にて、**65nm**プロセスのCellを発表。
      - [9月20日](../Page/9月20日.md "wikilink") - [東芝](../Page/東芝.md "wikilink")が、Cell技術を用いた省電力フル[HD画像処理コプロセッサ](https://ja.wikipedia.org/wiki/ハイディフィニション "wikilink")「[SpursEngine](https://ja.wikipedia.org/wiki/SpursEngine "wikilink")」を発表\[25\]\[26\]。
      - [10月12日](https://ja.wikipedia.org/wiki/10月12日 "wikilink") - [IBM](../Page/IBM.md "wikilink")が、集積度を二倍に高めたCellブレードサーバを発表\[27\]。
      - [10月29日](../Page/10月29日.md "wikilink") - [Cell Open Cafe](http://www.cell-hibikino.net)（財）[北九州産業学術推進機構](http://www.ksrp.or.jp/fais/)（FAIS）がSony-Toshiba-IBM（第三者による自主的活動拠点）Center of Competenceとして選定された。
      - [11月11日](../Page/11月11日.md "wikilink") - **65nm**プロセスのCellを搭載したPLAYSTATION 3（CECHH00シリーズ）が発売\[28\]。
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")
      - [2月4日](../Page/2月4日.md "wikilink") - SCE、IBM、Toshiba America Electronic Componentsが共同で、ISSCC(IEEE International Solid-State Circuits Conference)2008にて、**45nm**プロセスのCellを発表\[29\]。今後のPLAYSTATION 3等に搭載される予定。
      - [4月3日](../Page/4月3日.md "wikilink") - フィックスターズ、最新型Cellを搭載した[PCIe](https://ja.wikipedia.org/wiki/PCIe "wikilink")ボード「GigaAccel 180」を発売。\[30\]
      - [5月8日](../Page/5月8日.md "wikilink") - [東芝](../Page/東芝.md "wikilink")経営方針説明会において、Cell搭載テレビを[2009年](../Page/2009年.md "wikilink")秋に発売予定を発表\[31\]。
      - [5月17日](../Page/5月17日.md "wikilink") - [IBM](../Page/IBM.md "wikilink")、拡張倍精度（eDP）[SPEを](https://ja.wikipedia.org/wiki/#Synergistic_Processor_Element "wikilink")8基搭載し、[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink")[浮動小数点演算を最大](../Page/浮動小数点数.md "wikilink")5倍に強化した「[PowerXCell](https://ja.wikipedia.org/wiki/PowerXCell "wikilink") 8i プロセッサー」を開発、搭載ブレードサーバーをリリース。\[32\]
      - [5月27日](../Page/5月27日.md "wikilink") - [みずほ証券](../Page/みずほ証券.md "wikilink")、金融[デリバティブ](../Page/デリバティブ.md "wikilink")高速計算システムに、Cell/B.Eを世界で初めて採用。従来システムに比べて高速化に成功。10倍以上の見込みも。\[33\]\[34\]
      - [6月10日](../Page/6月10日.md "wikilink") - Cellベースの[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")「[Roadrunner](https://ja.wikipedia.org/wiki/Roadrunner "wikilink")」が「[Blue Gene/L](https://ja.wikipedia.org/wiki/Blue_Gene#Blue_Gene/L "wikilink")」を二倍以上引き離す1[ペタ](https://ja.wikipedia.org/wiki/ペタ "wikilink")[フロップスを世界最速達成](../Page/FLOPS.md "wikilink")。\[35\]
      - [6月23日](../Page/6月23日.md "wikilink") - [東芝](../Page/東芝.md "wikilink")が、Cell技術を用いたメディアプロセッサ「[SpursEngine](https://ja.wikipedia.org/wiki/SpursEngine "wikilink") SE1000」を搭載した[ノートパソコン](../Page/ノートパソコン.md "wikilink")「[Qosmio](../Page/Qosmio.md "wikilink") G50/F50」を発売すると発表\[36\]。
      - [7月18日](../Page/7月18日.md "wikilink") - [CRI・ミドルウェア](../Page/CRI・ミドルウェア.md "wikilink")、[東芝](../Page/東芝.md "wikilink")[SpursEngine](https://ja.wikipedia.org/wiki/SpursEngine "wikilink")向け[ミドルウェア](../Page/ミドルウェア.md "wikilink")に参入\[37\]
      - [7月25日](../Page/7月25日.md "wikilink") - [東芝セミコンダクター](https://ja.wikipedia.org/wiki/東芝セミコンダクター "wikilink")、「[SpursEngine](https://ja.wikipedia.org/wiki/SpursEngine "wikilink") Developers Forum 2008」を開催。「SPEのプログラミング手法を知らなくても利用可能」\[38\]
      - [8月13日](../Page/8月13日.md "wikilink") - [ソニー](../Page/ソニー.md "wikilink")、北米市場へ向けCell/B.E.搭載、[4K解像度](https://ja.wikipedia.org/wiki/4K解像度 "wikilink")映像制作ユニット『BCU-100』“ZEGO(ゼゴ)”発表。年内発売へ\[39\]
      - [11月26日](https://ja.wikipedia.org/wiki/11月26日 "wikilink") - [CRI・ミドルウェア](../Page/CRI・ミドルウェア.md "wikilink")、[SpursEngine](https://ja.wikipedia.org/wiki/SpursEngine "wikilink")向けコンソールツール、SpursEngineコンソール[エンコーダ](../Page/エンコード.md "wikilink")「CRI SpursCoder」及び[掲示板を公開](../Page/電子掲示板.md "wikilink")\[40\]
      - [12月8日](../Page/12月8日.md "wikilink") - [三菱総合研究所](../Page/三菱総合研究所.md "wikilink")、動産担保融資における在庫データのモニタリングにCell/B.E.を活用\[41\]
  - [2009年](../Page/2009年.md "wikilink")
      - [2月24日](https://ja.wikipedia.org/wiki/2月24日 "wikilink") - [フィックスターズ](https://ja.wikipedia.org/wiki/フィックスターズ "wikilink")、Cell活用の[H.264](../Page/H.264.md "wikilink")リアルタイムソフトウェアエンコーダ「CodecSys CEシリーズ」発売\[42\]
      - [5月22日](../Page/5月22日.md "wikilink") - [北九州産業学術推進機構](https://ja.wikipedia.org/wiki/北九州産業学術推進機構 "wikilink")（FAIS）、Cell/B.E.システム群を[北九州学術研究都市](../Page/北九州学術研究都市.md "wikilink")の研究者に無償で開放。\[43\]\[44\]
      - [8月19日](../Page/8月19日.md "wikilink") - SCEが、**45nm**プロセスのCellを搭載した[PlayStation 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")（CECH-2000A）を、[9月3日](https://ja.wikipedia.org/wiki/9月3日 "wikilink")に発売する事を発表\[45\]。
      - [10月5日](../Page/10月5日.md "wikilink") - [東芝](../Page/東芝.md "wikilink")は、Cellプラットフォームを初めて搭載した液晶テレビ「[CELL REGZA](https://ja.wikipedia.org/wiki/CELL_REGZA "wikilink") 55X1」を12月上旬より発売すると発表\[46\]。
      - [11月20日](../Page/11月20日.md "wikilink") - 連邦政府調達サイトに、[アメリカ空軍](https://ja.wikipedia.org/wiki/アメリカ空軍 "wikilink")が軍用の[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")の研究開発のためにPlayStation 3を2,200台発注する予定であることが掲載された\[47\]。
  - [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")
      - [3月15日](../Page/3月15日.md "wikilink") - [ソニー](../Page/ソニー.md "wikilink")、3D映像撮影制作業務用機器Cell/B.E.チップ搭載マルチイメージプロセッサー「MPE-200」を発売。
      - [3月30日](../Page/3月30日.md "wikilink") - [ソニー](../Page/ソニー.md "wikilink")、放送業務用機器拡張用PCI-Expressインターフェイス、Cell/B.E.チップ搭載マルチコアプロセッシングボード「BKMP-AB100」を発売。
      - [7月28日](../Page/7月28日.md "wikilink") - [東芝](../Page/東芝.md "wikilink")は、Cell/B.E.チップ搭載した3D対応液晶テレビ「[CELL REGZA](https://ja.wikipedia.org/wiki/CELL_REGZA "wikilink") 55X2」を10月下旬より発売すると発表\[48\]。
      - [9月30日](../Page/9月30日.md "wikilink") - [ソニー](../Page/ソニー.md "wikilink")、放送業務用機器、Cell/B.E.チップ搭載マルチフォーマットインジェストステーション「MPE-L1000」を発売。

## 長崎セミコンダクターマニュファクチャリング

**長崎セミコンダクターマニュファクチャリング株式会社**（NSM）は、2008年3月3日に設立した、東芝、ソニー、SCEの合弁会社。Cell Broadband Engine、[RSX](https://ja.wikipedia.org/wiki/PlayStation_3#仕様 "wikilink")、東芝とソニーのデジタルコンシューマー機器等向け[システム・オン・チップ](https://ja.wikipedia.org/wiki/システム・オン・チップ "wikilink")（SoC）を生産する\[49\]\[50\]。

製造設備は、東芝が2008年4月\[51\]にソニーとソニーセミコンダクタ九州株式会社（SCK）から約900億円で購入\[52\] \[53\]したSCK長崎テクノロジーセンター Fab2の下層\[54\]の300mmウェハーラインが東芝から貸与されている。資本金は1億円で、出資比率は東芝 60%、ソニー 20% 、SCE 20%\[55\]\[56\]。

東芝とソニーは2010年12月24日のニュースリリースで、東芝が所有しNSMが操業する、SCK長崎テクノロジーセンターの300mmウェーハラインをソニーに譲渡する旨の基本合意書を締結したこと、法的拘束力を有する正式契約は2010年度内早期の締結を目指すこと、東芝、ソニー、SCEの三社によるNSMの合弁関係は譲渡に伴い解消されることを発表した\[57\]\[58\]。ソニーは2010年12月27日のプレスリリースで、CMOSイメージセンサーの生産能力を倍増するために、東芝からSCK長崎テクノロジーセンターの300mmウェーハラインを取得し、設備の一部をCMOSイメージセンサーの製造ができるように整備すること等を発表した\[59\]。日本経済新聞では、東芝は世界2位のシェアであるNAND型メモリに経営資源を集中するため、不採算のシステムLSI事業では、巨額の設備投資が必要な先端品のシステムLSIについて、2011年度からは設計だけを行い、生産はサムスン電子に委託、収益改善につなげるため長崎工場はソニーに売却すると報じた\[60\]。

## 関連項目

  - [PlayStation 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")
  - [Roadrunner](https://ja.wikipedia.org/wiki/Roadrunner "wikilink")
  - [CELL REGZA](https://ja.wikipedia.org/wiki/CELL_REGZA "wikilink")
  - [レグザ](../Page/レグザ.md "wikilink")
  - [フィックスターズ](https://ja.wikipedia.org/wiki/フィックスターズ "wikilink")
  - [セリウス (企業)](../Page/セリウス_\(企業\).md "wikilink")
  - [SpursEngine](https://ja.wikipedia.org/wiki/SpursEngine "wikilink")
  - [ストリームプロセッシング](https://ja.wikipedia.org/wiki/ストリームプロセッシング "wikilink")

## 脚注・出典

## 外部リンク、参考文献

### SCE

  - [Cell Broadband Engine/Sony Computer Entertainment Inc.](http://cell.scei.co.jp/)

<!-- end list -->

  -
    アーキテクチャ、[ニーモニック](https://ja.wikipedia.org/wiki/ニーモニック "wikilink")、SPE向けの言語拡張などCellに関する基本情報を網羅している。

<!-- end list -->

  - [CELL: A New Platform for Digital Entertainment](http://research.scea.com/research/html/CellGDC05/index.html)

<!-- end list -->

  -
    2005年のGame Developers ConferenceでSony Computer Entertainment US Research and Developmentが発表したスライド。

### IBM

  - [IBM developerWorks:Cell Broadband Engine resource center](http://www-128.ibm.com/developerworks/power/cell/)
  - [IBM Journal of Research and Development Vol. 51, No. 5, 2007 - Cell Broadband Engine Technology and Systems](http://researchweb.watson.ibm.com/journal/rd51-5.html)

<!-- end list -->

  -
    [製造プロセスや](https://ja.wikipedia.org/wiki/集積回路#プロセス "wikilink")、[音声認識](../Page/音声認識.md "wikilink")エンジンでの性能評価やプログラミングモデルなどの応用に関するジャーナル。

<!-- end list -->

  - [Hardware and Software Architectures for the CELL BROADBAND ENGINE processor](http://www.casesconference.org/cases2005/pdf/Cell-tutorial.pdf)

<!-- end list -->

  -
    Cellの開発で中心的役割を担ったIBMのPeter Hofsteeらによるチュートリアルスライド。

<!-- end list -->

  - [PACT 2005: Optimizing Compiler for the Cell Processor](http://domino.research.ibm.com/comm/research_projects.nsf/pages/cellcompiler.refs.html/$FILE/slide-pact05.pps)

### 東芝

  - [東芝レビュー 61巻6号（2006年6月号)](http://www.toshiba.co.jp/tech/review/abstract/2006_06.htm)

<!-- end list -->

  -
    Cellの概要のほか、開発用リファレンスキット、家電向けのI/Oインタフェースを提供する*SuperCompanionChip*、ハイパーバイザー、ソフトウェア開発環境、画像処理における性能評価などの技術報告。

<!-- end list -->

  - [東芝セミコンダクター社: Cell ユーザーズ・グループ](http://www.cellusersgroup.com/)

### COC世界二拠点

  - [ジョージア工科大学](http://sti.cc.gatech.edu/)
  - [Multi-core Lounge](http://www.ksrp.or.jp/fais/sec/cell/index.html)（[財団法人 北九州産業学術推進機構 FAIS](http://www.ksrp.or.jp/fais/)）

[Category:Cell_BEアーキテクチャ](https://ja.wikipedia.org/wiki/Category:Cell_BEアーキテクチャ "wikilink") [Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink") [Category:IBMのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:IBMのマイクロプロセッサ "wikilink") [Category:ソニー・コンピュータエンタテインメント](https://ja.wikipedia.org/wiki/Category:ソニー・コンピュータエンタテインメント "wikilink") [Category:東芝](https://ja.wikipedia.org/wiki/Category:東芝 "wikilink") [Category:SIMDコンピューティング](https://ja.wikipedia.org/wiki/Category:SIMDコンピューティング "wikilink")

1.
2.  ただし、命令セットはPowerPCアーキテクチャベースではなく、[ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")ベースである。
3.  [西川善司の3DゲームファンのためのPS3パフォーマンス考察講座](http://watch.impress.co.jp/game%2Fdocs/20060331/ps3_2.htm), GameWatch, 2006年3月31日
4.
5.
6.
7.
8.  [後藤弘茂のWeekly海外ニュース - SCEIのPlayStation 3の心臓「Cell」の正体 -](http://pc.watch.impress.co.jp/docs/2003/0529/kaigai01.htm), PC Watch 2003年5月29日
9.  [Cell Broadband Engine技術資料公開](http://cell.scei.co.jp/)
10. [新プロセッサ「SpursEngine™」の開発サンプルをCEATEC JAPANで初公開](http://www.toshiba.co.jp/about/press/2007_09/pr_j2001.htm), 株式会社 東芝, 2007年9月20日
11.
12. メインメモリに比べ、ローカルストアは高速アクセス可能なため
13.
14.
15.
16.
17.
18. [PlayStation 4のGPUコンピュート機能 後藤弘茂のWeekly海外ニュース](http://pc.watch.impress.co.jp/docs/column/kaigai/20130422_596857.html)
19. [Transmetaプレスリリース（英語）：Accelerates LongRun2 Adoption for Cell Derivatives; Builds Technology Collaboration in Other Areas](http://investor.transmeta.com/ReleaseDetail.cfm?ReleaseID=158938)
20. [ソニー、CellにTransmetaの省電力技術「LongRun2」搭載](http://pc.watch.impress.co.jp/docs/2005/0401/transmeta.htm), PC Watch 2005年4月1日
21. なお、PS3では7SPEのうち1SPEはOSが占有するため、アプリケーションが使用可能なのは実質6SPEとなる。
22. [IBM、ロスアラモス国立研究所のペタフロップスパコン計画を落札--情報筋が明らかに](http://japan.cnet.com/news/ent/story/0,2000056022,20224287-2,00.htm), *[CNET Japan](../Page/CNET.md "wikilink")*, 2006年9月6日
23.
24. [PLAYSTATION 3ハードウェアレポート【速報編】](http://pc.watch.impress.co.jp/docs/2006/1111/ps3.htm), PC Watch, 2006年11月11日
25.
26. [「フルHD時代に向け原点に立ち戻った」--東芝、Cellベースの新プロセッサを公開](http://japan.cnet.com/news/tech/story/0,2000056025,20356878,00.htm)
27.
28. [新型PS3ハードウェアレポート 〜大幅に縮小された冷却機構](http://pc.watch.impress.co.jp/docs/2007/1112/ps3_2.htm), PC Watch, 2007年11月12日
29. [ISSCCに次世代Cell B.E. 45nm版が登場 〜6GHz動作、電力を30%以上削減](http://pc.watch.impress.co.jp/docs/2008/0206/kaigai416.htm), PC Watch 後藤弘茂のWeekly海外ニュース, 2008年2月6日
30. [フィックスターズ、最新型Cell/B.E.を搭載したアクセラレータボードを発売](http://www.fixstars.com/company/press/20080403.html) プレスリリース 2008年4月3日
31. [東芝、Cellテレビや“超解像”テレビ/DVDなど計画](http://www.watch.impress.co.jp/av/docs/20080508/toshiba.htm), AV watch, 2008年5月8日
32. [IBM、Cellベースのブレード・サーバ「BladeCenter QS22」を発表](http://www.computerworld.jp/news/hw/107589.html) Computerworld News （2008年05月14日）
33. [IBM みずほ証券へCell/B.E.搭載ブレードサーバーを納入](http://www-06.ibm.com/jp/press/2008/05/2701.html) IBMプレスリリース 2008年5月27日
34. [フィックスターズ、みずほ証券のデリバティブシステムをCell/B.E.で高速化に成功](http://www.fixstars.com/company/press/20080527.html) プレスリリース 2008年5月27日
35. [米エネルギー省、IBMのスパコン「Roadrunner」が1PFLOPSを達成と発表](https://news.mynavi.jp/news/2008/06/10/059/index.html)
36. [東芝、SpursEngine搭載/超解像度変換AVノート「Qosmio」](http://www.watch.impress.co.jp/av/docs/20080623/toshiba.htm), AV watch, 2008年6月23日
37. [ＣＲＩ・ミドルウェア、東芝SpursEngine™向けミドルウェアに参入](http://www.cri-mw.co.jp/newsrelease/release/2008/sdf2008/sdf2008_j.htm), CRI・ミドルウェア プレスリリース, 2008年7月18日
38. [「SpursEngine」のハード/ソフト開発環境が明らかに](http://hdpro.jp/third/index_080806.html), HD Processing FORUM, 2008年8月6日
39. [米国市場に向けてCell/B.E.およびRSX®搭載“ZEGO(ゼゴ)”コンピューティングユニット年内発売](http://www.sony.co.jp/SonyInfo/News/Press/200808/08-095/index.html), Sony プレスリリース, 2008年8月13日
40. [ＣＲＩ・ミドルウェア：「CRI SpursCoder」ダウンロード](http://criware.jp/spurscoder/), CRI・ミドルウェア, 2008年11月26日
41. [三菱総合研究所、動産担保融資における在庫データのモニタリングにCell/B.E.を活用](http://www.fixstars.com/company/press/20081208.html) プレスリリース 2008年12月8日
42. [フィックスターズ、Cell活用のH.264リアルタイムソフトウェアエンコーダ](https://news.mynavi.jp/articles/2009/02/24/fixstars_powerxcell8i/) マイコミジャーナル 2009年2月24日
43. [北部九州の研究者はCell/B.E.を無償で活用](http://www.itmedia.co.jp/enterprise/articles/0905/22/news051.html) ITmedia エンタープライズニュース 2009年5月22日
44. [北九州産業学術推進機構、高性能プロセッサ「Cell/B.E.」を用いたシステム基盤を研究者に開放](http://www.rbbtoday.com/news/20090522/60042.html) エンタープライズ RBB TODAY 2009年5月22日
45. [SCEJ、「プレイステーション」戦略発表会で新型PS3発表 「機動戦士ガンダム戦記」同梱BOXは38,359円で同時発売](http://game.watch.impress.co.jp/docs/news/20090819_309424.html), GAME Watch, 2009年8月19日
46. [世界初「Cell Broadband EngineTM」搭載 高画質液晶テレビ「CELLレグザ 55X1」の発売について](http://www.toshiba.co.jp/about/press/2009_10/pr_j0501.htm) ニュースリリース 2009年10月5日
47. [Air Force To Expand PlayStation-Based Supercomputer](http://www.informationweek.com/news/software/linux/showArticle.jhtml?articleID=221900487) InfomationWeek 2009年11月20日
48. [3D放送を高精細に映す3D超解像技術を採用した液晶テレビ「CELLレグザ」の発売について](http://www.toshiba.co.jp/about/press/2010_07/pr_j2803.htm) ニュースリリース 2010年7月28日
49. [東芝及びソニーによる半導体製造設備の譲渡に関する基本合意書の締結について](http://www.toshiba.co.jp/about/press/2010_12/pr_j2402.htm), 東芝ニュースリリース, 2010年12月24日
50. [東芝及びソニーによる半導体製造設備の譲渡に関する基本合意書の締結について](http://www.sony.co.jp/SonyInfo/News/Press/201012/10-1224/index.html), ソニーニュースリリース, 2010年12月24日
51. 「東芝、半導体改革メド　大分は画像センサー中心　設計・生産、分業時代に」『日本経済新聞』2010年12月24日付日刊、第13版、第9面。
52. [高性能半導体の生産合弁会社の概要について](http://www.toshiba.co.jp/about/press/2008_02/pr_j2002.htm), 東芝ニュースリリース, 2008年2月20日
53. [高性能半導体の生産合弁会社の概要について](http://www.sony.co.jp/SonyInfo/News/Press/200802/08-0220/index.html), ソニーニュースリリース, 2008年2月20日
54. [ソニーの裏面照射型CMOSセンサー工場を訪ねる](http://dc.watch.impress.co.jp/docs/review/special/20100304_351111.html), デジカメWatch, 2010年3月4日
55.
56.
57.
58.
59. [ソニー、イメージセンサーの生産能力を倍増](http://www.sony.co.jp/SonyInfo/News/Press/201012/10-165/index.html), ソニーニュースリリース, 2010年12月27日
60. 「東芝、サムスンと提携　先端LSI生産委託　投資競争から撤退　メモリー事業に集中」『日本経済新聞』2010年12月24日付日刊、第13版、第1面。