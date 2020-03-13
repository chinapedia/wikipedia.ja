> この記事は[PowerPC G4](https://ja.wikipedia.org/wiki/PowerPC_G4)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:XPC7450.jpg "wikilink")

**PowerPC G4**は[PowerPC](../Page/PowerPC.md "wikilink")の第4世代[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")を呼ぶものとして、[アップルコンピュータによって使われた名称である](../Page/アップル_\(企業\).md "wikilink")。[モトローラ](../Page/モトローラ.md "wikilink")及びモトローラから分離した[フリースケールのプロセッサPowerPC](https://ja.wikipedia.org/wiki/NXPセミコンダクターズ "wikilink") 74xxシリーズに対して、アップルはこの名前を使うようになった。

[Macintosh](../Page/Macintosh.md "wikilink")コンピュータのシリーズ、[PowerBook G4や](../Page/PowerBook_G4.md "wikilink")[iBook G4のようなノートPCや](https://ja.wikipedia.org/wiki/IBook#iBook_G4 "wikilink")、[Power Mac G4や](https://ja.wikipedia.org/wiki/Power_Mac#Power_Mac_G4 "wikilink")[Power Mac G4 CubeのようなデスクトップPCは](../Page/Power_Mac_G4_Cube.md "wikilink")、このプロセッサの名前からとっている。PowerPC G4はまた、[eMac](https://ja.wikipedia.org/wiki/eMac "wikilink")や初代[Xserve](../Page/Xserve.md "wikilink")、初代[Mac mini](https://ja.wikipedia.org/wiki/Mac_mini "wikilink")、そしてG5プロセッサ採用前の液晶iMacにも使われた。

アップルは、IBMが開発した64bitプロセッサである[PowerPC 970を採用してから](../Page/PowerPC_970.md "wikilink")、デスクトップモデルについてはG4シリーズの採用を終了した。G4を採用した最後のデスクトップモデルは[Mac miniであった](https://ja.wikipedia.org/wiki/Mac_mini "wikilink")。G4を採用した最後のノートPCはiBook G4である。

本来、組み込み向けが用途の中心であり、[ルータや](../Page/ルーター.md "wikilink")[スイッチ等のネットワーク機器](../Page/レイヤ3スイッチ.md "wikilink")、[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")エンジンなどで利用され、過去に採用されていたMacintosh向けよりも大量に出荷されている。

## PowerPC 7400

7400(コードネームはMax)は1999年夏の終わりにデビューし、G4という愛称をつけられた最初のプロセッサであった。このチップは350MHzから500MHzの間で動作し、1,050万トランジスタを含んでおり、モトローラのHiPerMOS6プロセスを使って製造された。チップのダイサイズは83[mm<sup>2</sup>で](https://ja.wikipedia.org/wiki/平方ミリメートル "wikilink")[銅配線技術](https://ja.wikipedia.org/wiki/銅配線技術 "wikilink")を使用している。

モトローラはアップルに対して500MHzまでの動作クロックの製品を出荷すると約束していたが、初期の[歩留まり](../Page/歩留まり.md "wikilink")は非常に悪かった。このことにより、アップルはPower Mac G4の500MHzモデルの広告を取り消さざるを得なかった。Power Macシリーズは400、450、500MHzのクロックを突然350、400、450MHzに落とした。アップルとモトローラの関係には溝ができ、これによりアップルはIBMに対してモトローラの7400シリーズの製品歩留まりを上げるのを助けてくれるように頼んだと報じられた。500MHzモデルは2000年2月16日に再度採用された。

### 設計

アップルとIBMと緊密に協力する中で、7400の大部分はモトローラにより設計が行われていた。G4アーキテクチャは、[PowerPC G3プロセッサに](../Page/PowerPC_G3.md "wikilink")[AltiVec](../Page/AltiVec.md "wikilink")と呼ばれる (アップルは**Velocity Engine**と呼称している) 128bitのベクタプロセッシングユニットを加えたものとなった。[AIM allianceの](https://ja.wikipedia.org/wiki/AIM連合 "wikilink")3番目のメンバーであるIBMは、従来よりサマーセットデザインセンターでモトローラと共同でPowerPCプロセッサを設計していたが、IBMはベクタプロセッシング ([SIMD](../Page/SIMD.md "wikilink")) ユニットを必要とは考えていなかったので、G4チップを製造することはなかった。

AltiVecユニットを用いると、7400マイクロプロセッサは4並列単精度 (32bit) 浮動小数点演算ないし、16並列8bit、8並列16bit、4並列32bitの整数演算を1サイクルで行うことができる。さらに、このベクタプロセッシングユニットは[スーパースカラ](https://ja.wikipedia.org/wiki/スーパースカラ "wikilink")構造を持っており、2つのベクタ演算操作を同時に行うことができる。この特徴はAltiVecユニットを利用するように設計されたアプリケーションを使う場合に、当時のIntelのx86マイクロプロセッサに対して、パフォーマンスを上げることができた。エフェクトやオブジェクトの軌跡をレンダリングする際にAltiVecユニットを利用すると高速化されるAdobe Photoshopや、AltiVecユニットを利用することでオンザフライでファイルのインポートや変換を行うアップルの[iLife](https://ja.wikipedia.org/wiki/iLife "wikilink")アプリケーションスイートはアプリケーションの一例である。

7400のPowerPCプロセッサとしての基本的な仕様やマイクロアーキテクチャの多くは[PowerPC 750のものを踏襲しており](../Page/PowerPC_G3.md "wikilink")、AltiVecのサポートが加えられた点以外は大きく変わっていない。その中でも数少ない改良点として挙げられるのが[対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink") (SMP) のサポートと[FPU](../Page/FPU.md "wikilink")の改良である。7400は、改良された[キャッシュコヒーレンシー](https://ja.wikipedia.org/wiki/キャッシュコヒーレンシー "wikilink")プロトコル (MERSI) により、SMPをサポートするよう機能強化されている。また、7400のFPUは[PowerPC 604のFPUをベースとして開発されたものを搭載している](../Page/PowerPC_604.md "wikilink")。これは、604のFPUがPowerPC 750のFPUよりも倍精度演算命令のレイテンシが小さく、クロック当たりおよそ25%高速であったためである。

## PowerPC 7410 "Nitro"

PowerPC 7410は7400と同じ設計であったが、200nmの代わりに180nmで製造された。7400と同じく1,050万トランジスタを搭載している。これは2001年1月9日に初代PowerBook G4でデビューした。

このチップはキャッシュの全量ないし半分を「高速なメインメモリ」として使う機能が追加されている。これは、キャッシュを指定のプロセッサの物理アドレス空間に割り当てることができるというものである。この機能は[Mercury Computer Systemsのような組み込みベンダによって使われた](https://ja.wikipedia.org/wiki/Mercury_Computer_Systems "wikilink")。

## PowerPC 7450 "Voyager"

PowerPC 7450は、G4プロセッサにおいて最初の(そして唯一の)大きな設計変更が行われたものである。チップには3,300万トランジスタ搭載され、7400/7410から大きく増加している。主な変更点は以下の通り。

  - 強化されたスーパースカラ実行
    7400/7410ではクロックあたり2+1(1は分岐)命令実行だったが、7450では3+1(1は分岐)命令実行に強化されている。

  - より長いパイプライン
    整数パイプで従来の4段から6-7段、FPUパイプで従来の6段から11段等と各実行パイプラインで2-5段程度増加しており、より高い周波数での動作をターゲットとしている。7400/7410のパイプラインはPowerPC G3 (さらに言えば [PowerPC 603](../Page/PowerPC_603.md "wikilink")) と同じ非常に短いパイプラインであり、クロック当たりの性能は高かったが動作周波数はあまり上がらず、当時の[Pentium IIIや](../Page/Pentium_III.md "wikilink")[Athlon](../Page/Athlon.md "wikilink")などの[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")プロセッサが1GHzを超える周波数で動いていたのに対して大きく見劣りしていた。この改良により、G4プロセッサでも1GHzを超える周波数での動作が見込めるようになった。

  - 整数演算ユニットの増加
    7400/7410ではSimple x1, Complex x1の2ユニット構成であったのが、7450ではSimple x3, Complex x1の4ユニットと倍増している。

  - [アウト・オブ・オーダー実行](../Page/アウト・オブ・オーダー実行.md "wikilink")機構の強化
    リオーダ・バッファのエントリ数が6から16に大きく増加し、in-flightで制御可能な命令が増加している。しかしながら、依然として完全にアウト・オブ・オーダー実行が可能なのは整数演算命令のみであり、FPUで実行される命令同士や、AltiVecの同じサブユニットで実行される命令同士は並べ替えて実行することができない。また、整数演算命令についても4つの演算器のリザベーション・ステーションと発行キューの合計で4命令\[1\]分の命令ウィンドウしか存在せず、広い命令ウィンドウを持ち積極的なアウト・オブ・オーダー実行を行っていた当時のx86プロセッサと比較すると見劣りする仕様となっている。

  - AltiVecユニットの改良
    7400/7410のAltiVecユニットはVector Permute命令を実行するユニットとそれ以外の命令を実行するユニットに分かれており、この2つの命令の組み合わせでのみ同時実行可能であった。7450ではこれがPermute, Simple Integer, Complex Integer, Floating Pointの4ユニット構成となり、4種類の命令の中から任意の2種類の命令の組み合わせで同時に実行できるようになった。

  - 256KBのオンチップL2キャッシュの搭載
    最大2MBまでの外部L3キャッシュをサポート

7450は2001年1月9日に、733MHzのPower Mac G4に採用された。なお、PowerPC 7451は7450と同等の機能を持つマイナーチェンジ版であり、7441は7451からL3キャッシュのインターフェイスを省いたものである。

7400/7410に対して大きな改良が行われた745x/744x系列のプロセッサを**G4e**もしくは**G4+**と呼ぶことがあるが、これは公式のものではない。

## PowerPC 7445/7455 "Apollo 6"

PowerPC 7455で、オンチップキャッシュバスがより広い256ビットになり、180nmの[SOI](../Page/SOI.md "wikilink")プロセスで製造された。これはアップルにとって1GHzの壁を越えた最初のプロセッサだった。7445は同じチップでL3キャッシュインタフェースを除いたものである。7455は[AmigaOne](https://ja.wikipedia.org/wiki/AmigaOne "wikilink") XE G4で採用された。

## PowerPC 7447/7457 ""Apollo 7"

2005年初頭、アップルのG4シリーズの中で出荷されたもっとも高速なプロセッサはMPC 7447Bであり、これは1.67GHzで動作するもので、2005年1月のPowerBook G4に採用された。5,800万トランジスタからなる7447は7450/55からほんの少し改良された。これは512KBのオンチップL2キャッシュを持ち130nmで製造され、その後低消費電力化される。7447Aでは、DFS（動的周波数変更）と共にサーマルダイオードも集積し、フリースケールは少しだけクロックを上げることができた。7457はL3キャッシュインタフェースを追加されたものである。

Power Mac G4とPower Mac G4 Cubeをアップグレードするのに7457を使う企業は、Giga Designs社とDaystar Technology社（OWCが買収。iMac G4アップグレードに7457を唯一使っていた）とPowerlogix社のみであった。[Pegasosコンピュータもまた](https://ja.wikipedia.org/wiki/:en:Pegasos "wikilink")7447を使ってPegasos-II/G4を販売していた。

## PowerPC 7448 "Apollo 8"

MPC7448\[2\]は7447が進化したもので、本質的に1MBのL2キャッシュと200MHzのFSBを持つ、90nmで製造された7447の高速かつ低消費電力版である。フリースケールの新しい標準コアであるe600はこれらの機能を備えている。Daystar社は、2GHzまで動作する、[アルミニウムPowerBook G4に対する](https://ja.wikipedia.org/wiki/PowerBook_G4#アルミニウムPowerBook_G4 "wikilink")7448アップグレードキットを出荷している。

## 将来

### e600

745xに見られる多重化バスインタフェースによって、帯域が抑えられているという問題が思い起こされる。また、フリースケールのSoCチップの商品ラインアップ計画と対照的だと思わせる。このラインアップは、シングルないしデュアルのe600コアを用い[RapidIO](https://ja.wikipedia.org/wiki/RapidIO "wikilink")や[PCI Expressを通してより速いシステムインタフェースと接続できる](../Page/PCI_Express.md "wikilink")。またIO同士を667MHzで動作する多重化バスで接続し、コアとDDR/DDR2メモリコントローラは非同期マルチプロセッサをサポートする。このアーキテクチャはフリースケールのMPC8641およびMPC8641Dプロセッサモデルで登場し、2005年の10月にリビジョン1.0としてテープアウト、2006年中頃に特定顧客向けにサンプル出荷される。商品化されるのは2007年初頭を予定され、出荷時のコアクロックは1-1.5GHz、メモリクロックは400-600MHzを予定している。

### e700

2004年、フリースケールは新しい処理能力の高いコアであるe700を発表した。これまで公表された2、3の詳細情報から、このコアはe600とよく似ていて、64bitプロセッサで、3GHzないしそれ以上のクロックで動作し、MPC87xxと名づけられている。

## 脚注

<references />

## 関連項目

  - [PowerPC](../Page/PowerPC.md "wikilink")
  - [F-35](../Page/F-35_\(戦闘機\).md "wikilink") - 電子系統を制御するICP（Integrated Core Processor：統合型コアプロセッサー)はPowerPC G4をベースとしている。

[Category:モトローラのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:モトローラのマイクロプロセッサ "wikilink") [Category:アップルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:アップルのマイクロプロセッサ "wikilink")

1.  3つのSimple IUが1エントリ、Complex IUが2エントリのリザベーション・ステーションを持つ。ただし、Complex IUのリザベーション・ステーションからの発行はイン・オーダーであるため、命令ウィンドウとしては1命令分しかない。リザベーション・ステーションに空きがあれば、発行キューのうち最新の3命令分についてもアウト・オブ・オーダーで発行できる対象になるため、これを含めれば6命令 (リザベーション・ステーションに3命令と、空いているリザベーション・ステーションに発行されうる3命令) となる。
2.  [MPC7448: RISC Microprocessor](http://www.nxp.com/ja/products/microcontrollers-and-processors/power-architecture-processors/integrated-host-processors/risc-microprocessor:MPC7448)