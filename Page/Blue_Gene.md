> この記事は[Blue Gene](https://ja.wikipedia.org/wiki/Blue_Gene)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:BlueGeneL_cabinet.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:LLNL_BGL_Diagram.png "wikilink")  **Blue Gene**（**ブルージーン**）は[IBM](../Page/IBM.md "wikilink")の[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")プロジェクトである。

Blue Geneプロジェクトは1999年に発表され\[1\]\[2\]、第1世代は**Blue Gene/L**\[3\]、第2世代は**Blue Gene/P**\[4\]、第3世代は**Blue Gene/Q**\[5\]である。Blue Geneは[PowerPC](../Page/PowerPC.md "wikilink")系の[プロセッサ](../Page/プロセッサ.md "wikilink")を多数使用した[HPCクラスタで](../Page/高性能計算.md "wikilink")、[TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")や[Green500](https://ja.wikipedia.org/wiki/Green500 "wikilink")、[HPCCアワードなどのスーパーコンピュータ性能ランキングの上位を占めている](https://ja.wikipedia.org/wiki/HPCチャレンジベンチマーク "wikilink")。

IBMでは1997年にチェスの世界王者[ガルリ・カスパロフ](../Page/ガルリ・カスパロフ.md "wikilink")に勝利した「[Deep Blueの子孫](../Page/ディープ・ブルー_\(コンピュータ\).md "wikilink")」と称している\[6\]

## 概要

Blue Gene プロジェクトの最初のコンピュータである「Blue Gene/L」は、1億[ドル](../Page/ドル.md "wikilink")の費用をかけてピーク性能で360[T](../Page/テラ.md "wikilink")[FLOPS](../Page/FLOPS.md "wikilink")を目指し、[ローレンス・リバモア国立研究所](../Page/ローレンス・リバモア国立研究所.md "wikilink")と共同で開発された。この目標は日本製の旧[地球シミュレータ](../Page/地球シミュレータ.md "wikilink")の実効性能35.86TFLOPSの10倍の速さである。2010年までにピーク性能1[PFLOPSの](https://ja.wikipedia.org/wiki/ペタ "wikilink")「Blue Gene/P」、2010～2012年には10PFLOPSの「Blue Gene/Q」の開発を目指した。

### 特徴

  - プロセッサ

Blue Gene登場前のスーパーコンピュータでは、専用の[ベクトルプロセッサや](../Page/ベクトル計算機.md "wikilink")[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")、[POWERなどの高性能な](../Page/POWER_\(マイクロプロセッサ\).md "wikilink")[プロセッサ](../Page/プロセッサ.md "wikilink")を数十個から最高で数千個搭載するものが中心であった。Blue Geneプロジェクトでは、一つ一つの性能は高くないプロセッサを最高で数十万個以上搭載し、[並列実行するプログラム数を格段に増やすことで高い性能を実現する設計を採用した](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")。

  - ネットワーク

[メッセージパッシング](https://ja.wikipedia.org/wiki/メッセージパッシング "wikilink")、[同期など並列アプリケーション特有の](../Page/モニタ_\(同期\).md "wikilink")[プログラミング](../Page/プログラミング.md "wikilink")手法を支援する独自のコンピュータネットワークを搭載している。

  - 導入・管理コスト

発熱の低いプロセッサの採用や周辺回路の1チップ化によって、設置面積、消費電力、冷却に必要な空調設備などに要するコストを低く抑えている。

### システム構成

Blue Geneは、システムとしての最小構成となるラックを必要に応じて複数接続することでユーザが求める性能を提供する。そのラックは、1プロセスを実行する最小単位となる計算ノードを複数個搭載しており、各ノードはコンピュータネットワークによって接続されている。

## 歴史

### ローレンス・リバモア研究所のシステム

2004年11月に発表された第24回Top500リスト\[7\]において、スーパーコンピュータ向けベンチマーク[LINPACK](../Page/LINPACK.md "wikilink")におけるBlue Gene/Lの実効性能は70.72TFLOPSとなり、地球シミュレータを抜いて当時の世界最速のスーパーコンピュータとなった。当時はまだ搭載CPUコアが32,768個であり、ベータ版という位置づけであった。

その半年後の2005年6月、Blue Gene/LはCPU数を65,536個に倍増して136.80TFLOPSを達成\[8\]し、さらに2005年10月には131,072個のCPUで280TFLOPSを達成\[9\]したと発表した。 2007年11月の第30回Top500では、CPUコアをさらに増やし212,992個で478TFLOPSを記録\[10\]し、当初の計画目標である360TFLOPSを達成した。 [thumb](https://ja.wikipedia.org/wiki/ファイル:20080831-R0012506.JPG "wikilink")

### 日本国内への導入

日本国内では[産業技術総合研究所](../Page/産業技術総合研究所.md "wikilink")[生命情報工学研究センター](https://ja.wikipedia.org/wiki/生命情報工学研究センター "wikilink")が4ラックを導入し、2005年6月に発表されたTop500で第8位を記録した\[11\]。その後[ニイウス](https://ja.wikipedia.org/wiki/ニイウス "wikilink")株式会社で1ラック、2006年には[高エネルギー加速器研究機構](../Page/高エネルギー加速器研究機構.md "wikilink")で10ラックが稼働を開始した。

### その他

[2009年](../Page/2009年.md "wikilink")9月17日、米国家技術賞を受賞した。\[12\]

## Blue Gene/L

### 計算ノード

[rightの構成図](https://ja.wikipedia.org/wiki/ファイル:Blue_Gene_L_scheda.png "wikilink")\]\] 計算ノードの構成をシンプルにすることで、[はんだ](../Page/はんだ.md "wikilink")不良などによるハードウェア故障を減らし、また[高密度実装を実現した](https://ja.wikipedia.org/wiki/#高密度実装 "wikilink")。計算ノード単体の性能は、PCにくらべ低くまた搭載メモリ量も少ないため、一般的な環境に比べるとプロセスに対する制約が大きい。

#### 構成

メモリ以外の要素は[SoCとして統合し](../Page/System-on-a-chip.md "wikilink")、一つの集積回路に収めたことから、実質的には二つの部品のみで構成される。

  - [PowerPC](../Page/PowerPC.md "wikilink") 440ベースのプロセッサ x 2
    [組み込みシステム](../Page/組み込みシステム.md "wikilink")向けの省電力プロセッサであるPowerPC 440\[13\]をベースにしたものを2つ搭載している。各コアにはそれぞれ独立した[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink")[浮動小数点演算ユニットとL](../Page/FPU.md "wikilink")2キャッシュが付属し、2コア間では4[MiBのL](https://ja.wikipedia.org/wiki/メビバイト "wikilink")3キャッシュを共有している。
  - ネットワークインタフェース
    計算ノード間の通信に利用するBlue Gene独自の[三次元トーラスネットワーク](https://ja.wikipedia.org/wiki/#三次元トーラスネットワーク "wikilink")、[集団通信ネットワーク](https://ja.wikipedia.org/wiki/#集団通信ネットワーク "wikilink")、[グローバルバリアネットワークと](https://ja.wikipedia.org/wiki/#グローバルバリアネットワーク "wikilink")、[ギガビット・イーサネットのインタフェースを備える](https://ja.wikipedia.org/wiki/イーサネット#ギガビット・イーサネット "wikilink")。
  - [JTAG](../Page/JTAG.md "wikilink")インタフェース
    計算ノードの診断やデバッグに用いる。
  - メモリ
    512[MiBの](https://ja.wikipedia.org/wiki/メビバイト "wikilink")[DDR SDRAM](../Page/DDR_SDRAM.md "wikilink")

#### 高密度実装

省電力プロセッサを採用した理由は高密度実装を実現するためである。一般的なPCやサーバ、また旧来のスーパーコンピュータが採用する高性能プロセッサの多くは、消費電力とそれに伴う発熱も大きいため、そのようなCPUを筐体に多数詰め込むと排熱が非常に困難になる。かといって筐体内の密度を下げるとケーブルや接続コネクタなどの構成部品が増え、それが信頼性の低下を招く。 Blue Gene/Lでは消費電力あたりの性能が高い組み込み用途向けプロセッサを導入することでその問題を解決した\[14\]。この設計方針により、Blue Gene/Lはその性能に対し電力消費や設置面積において非常にコンパクトなシステムとなった。Blue Gene/Lの消費電力あたりの性能は112.24MFLOPS/Wであり\[15\]、地球シミュレータの3.01MFLOPS/Wと比べると、Blue Gene/Lは37倍も電力効率の良いシステムである。

### ラック

[thumb](https://ja.wikipedia.org/wiki/ファイル:BlueGeneL_rack.jpg "wikilink") Blue Gene/Lのラック内には、[計算ノードを](https://ja.wikipedia.org/wiki/#計算ノード "wikilink")2つ搭載する計算カードが512枚搭載され、2048CPUのマシンとして構成されている。それに加え、ファイルシステムへのアクセスを担当するI/Oノードが1ラック当り2から64枚搭載されている。I/Oノードは[ギガビット・イーサネットでラック外部のファイルサーバと接続し](https://ja.wikipedia.org/wiki/イーサネット#ギガビット・イーサネット "wikilink")、[集団通信ネットワークを介して計算ノードと通信を行う](https://ja.wikipedia.org/wiki/#集団通信ネットワーク "wikilink")。ラックに搭載するI/Oノードの数は、実行するアプリケーションの性質によって調整する。

### ネットワーク

Blue Gene/L内のノード接続には、その用途に応じて異なる5種類のネットワークが使われている。

#### 三次元トーラスネットワーク

[thumb](https://ja.wikipedia.org/wiki/ファイル:2x2x2torus.svg "wikilink") 三次元[トーラス](../Page/トーラス.md "wikilink")ネットワークは低遅延・広帯域を要求されるノード間の一対一通信に使われ、Blue Geneの通信ネットワークの中でも最も重要な位置を占める。

三次元トーラスネットワークは隣接ノード同士の接続から構成されるため、通信相手によってはその通信データが複数ノードを経由して到達することになる。 よって、トーラスネットワークの帯域を効率的に用いるには、三次元トーラスにおける通信を出来るだけ局所的に抑えるようなアルゴリズムを適用する必要がある。また、通信局所性をBlue Geneの物理的な接続配置にあわせることも重要である。

各計算ノード間の接続は1方向あたり1.4G[bps](../Page/ビット毎秒.md "wikilink")、遅延は100[ナノ](https://ja.wikipedia.org/wiki/ナノ "wikilink")秒となる。各ノードは近隣の6ノードとそれぞれ双方向に接続しており、1ノードの合計入出力帯域は16.8Gbpsに達する。ノード数が65,536の場合トーラスは64x32x32となり、最大ホップ数は32+16+16=64ホップ、最大遅延は6.4[マイクロ](../Page/マイクロ.md "wikilink")秒となる。

#### 集団通信ネットワーク

[thumb](https://ja.wikipedia.org/wiki/ファイル:Blue_Gene_L_Collective_network.svg "wikilink") 集団通信ネットワークは、ある1ノードと複数ノードとの一対多通信やファイル転送に用いられるもので、各ノードと他の1～3ノードとの相互接続による2分木ネットワークによって構成される。発信元から末端までの遅延は最大5マイクロ秒、帯域は2.8Gbpsである。

  - ノード処理結果の収集・集約

現在のスーパーコンピュータ向け並列アプリケーションでは、各ノードの処理結果を集約する操作に多く時間を費やしている。その性質を踏まえ、Blue Geneの集団通信ネットワークには最大・最小値、合計等の整数演算やビット列論理演算による集約機能を備えている。Blue Geneの集団通信ネットワークの遅延は他の一般的なスーパーコンピュータにくらべ1/10から1/100であり、Blue Gene/Lの最大構成時においても効率的な集約処理を実現している。

  - [ブロードキャスト](../Page/ブロードキャスト.md "wikilink")

あるノードから複数のノードにデータをブロードキャストするのに集合通信ネットワークが用いられる。三次元トーラスネットワークでもブロードキャストは可能だが、ネットワークトポロジの面から見て集合通信ネットワークのほうがずっと効率的である。

#### グローバルバリアネットワーク

並列アプリケーションでは、各プロセスの[同期がよく行われる](../Page/モニタ_\(同期\).md "wikilink")。プロセッサ数とノード数におけるスケーラビリティを確保するためには、同期待ちに伴う遅延を改良する必要がある。グローバルバリアネットワークには、複数ノードの同期をハードウェアによる支援によって高速に行う機構が備えられている。 このバリアネットワークは低遅延という特徴を持ち、65,536ノードの同期に必要な時間は1.5マイクロ秒未満である。

#### システム管理ネットワーク

計算ノードの初期化や監視・管理・デバッグのためにイーサネットとJTAG等のインタフェースを変換回路を介して接続するネットワークが用意されている。このネットワークを用いて管理用コンピュータから遠隔操作を行う。

#### I/Oネットワーク

I/Oノードが持つギガビット・イーサネットが接続されるネットワークで、I/Oノード同士の通信と外部のファイルサーバへのアクセスを担う。

### [システムソフトウェア](../Page/システムソフトウェア.md "wikilink")

#### OS

  - 計算ノード

計算ノードでは、*Compute Node Kernel*(CNK)と呼ばれる独自のOSカーネルが動作している。マルチユーザをサポートしない、同時実行スレッド数はCPUの数と同じ2つのみ、ページング機能を持たずアドレス空間は512MiBに固定するなど、機能を絞ることでOSのオーバーヘッドを小さくしている。 CNKは[POSIX](../Page/POSIX.md "wikilink")に近いインタフェースを持ち、アプリケーション開発者に対してGNU GlibcとファイルI/O用システムコールを提供している。I/O処理はCNKが行うのではなく、CNKの要求を受けたI/Oノードが代わりに実行する。上で述べたCNKの制限から[fork](https://ja.wikipedia.org/wiki/fork "wikilink")やexecなどのマルチプロセスはサポートしない。

  - I/Oノード

I/Oノードでは、I/Oノード独自のデバイスをサポートした[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")ベースのカーネルを採用している。

I/Oノード上では*Control and I/O Daemon*(CIOD)が動作しており、計算ノードのファイルアクセスやジョブの制御を行っている。計算ノードでのジョブ実行は、I/Oノードがプログラムを計算ノードにロードし、実行開始指令をCNKに出すことで開始される。ジョブ実行中、I/OノードはCNKから送られてきたI/O処理依頼を実行する。

  - サービスノード

計算ノードとI/Oノードの管理を担うサービスノードでは、*Core Management and Control System*(CMCS)が動作している。CMCSの役割は、各ノードの電源投入や温度やファンなどの監視と異常検知時の緊急シャットダウン、ノードの初期化や再設定などである。

## Blue Gene/P

[BlueGeneP_rack.jpg](https://ja.wikipedia.org/wiki/File:BlueGeneP_rack.jpg "fig:BlueGeneP_rack.jpg") **Blue Gene/P**は、2007年6月26日にIBMが発表した、次世代のBlue Geneスーパーコンピュータ。継続的に1 PFLOPSで稼動し、最大3 PFLOPSまで構成可能な余地を持って設計された。更に、小型で低電力の多数のチップを5つの特別なネットワークで結合する事で、他のスーパーコンピュータより少なくとも7倍のエネルギー効率を実現した。それぞれのBlue Gene/Pチップには、4個のPowerPC 450 850MHzプロセッサが搭載されている。1 PFLOPSのBlue Gene/Pは、高速の光ネットワークを備えた72ラックに294,912個のプロセッサで構成される。216ラックに884,736個のプロセッサまで拡張する事で、3 PFLOPS性能に達する。標準のBlue Gene/P構成では、1ラックに4,096個のプロセッサを格納する。

2007年11月12日、最初のシステムの[JUGENE](https://ja.wikipedia.org/wiki/JUGENE "wikilink")が、[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")のユーリッヒ研究センターで、65,536プロセッサを搭載し167 TFLOPSで稼動した\[16\]。

## Blue Gene/Q

**Blue Gene/Q**は、Blue Geneシリーズの最新のスーパーコンピュータの設計で、2011年内に20 PFLOPS達成を目標としたが、2012年に延期された。Blue Gene/Qは、高い電力当り性能を持つ Blue Gene/L や Blue Gene/P の拡張と強化を続けたもので、1684 MFLOPS/Watt を実現した\[17\]\[18\]。

### 設計

Blue Gene/Qのプロセッサは**Power BQC**と呼ばれ、[PowerPC A2をベースにしている](https://ja.wikipedia.org/wiki/:en:PowerPC_A2 "wikilink")。Blue Gene/Q は、16コアを持つ、4-Way の[ハイパースレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink") [64ビット](../Page/64ビット.md "wikilink") の [PowerPC](../Page/PowerPC.md "wikilink") A2 ベースのチップを搭載している。そのチップは統合されたメモリとI/Oコントローラを持ち、各プロセッサコアに1 GB DDR3 RAMを持つノードカードに搭載される\[19\]\[20\]。

### 導入

Blue Gene/Qを採用したシステムには以下がある。

  - [セコイア](https://ja.wikipedia.org/wiki/セコイア_\(スーパーコンピュータ\) "wikilink")
  - [Mira](https://ja.wikipedia.org/wiki/Mira_\(スーパーコンピュータ\) "wikilink") - [アルゴンヌ国立研究所](../Page/アルゴンヌ国立研究所.md "wikilink")\[21\]
  - Fermi
  - JuQUEEN

## プログラミングモデル

Blue Gene/Lの[システム構成は](https://ja.wikipedia.org/wiki/#システム構成 "wikilink")、各計算ノードで独立して実行されるプロセスがネットワークを介して互いにデータを交換する[メッセージパッシングモデルを想定した設計となっている](https://ja.wikipedia.org/wiki/メッセージ_\(コンピュータ\)#メッセージパッシング "wikilink")。メッセージパッシングにおいて[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")として利用される[Message Passing Interface](../Page/Message_Passing_Interface.md "wikilink") (MPI)をサポートしていることから、MPIを利用して実装された既存のスーパーコンピュータ向け並列アプリケーションの多くは移植するだけでBlue Gene/Lの特徴を生かして実行される。 しかし、[ネットワークで述べたように通信の局所性が乏しい](https://ja.wikipedia.org/wiki/#ネットワーク "wikilink")、また処理全体の中で通信時間の比率が高いもの、元々並列度が低いアプリケーションについては、より低遅延・広帯域なネットワークを備える他のシステムに比べ低い実行効率しか得られない。Blue Geneは、通信に対する計算の比率が高いアプリケーションほどより有利に実行可能である。

## 脚注

<references/>

## 参考文献

  -
  -
## 外部リンク

  - [IBM Blue Gene（英語）](http://www.research.ibm.com/bluegene/)
  - [ローレンスリバモア国立研究所 Blue Gene/L](http://www.llnl.gov/asci/platforms/bluegenel/)
  - [産業技術総合研究所 生命情報工学研究センター](http://www.cbrc.jp/)

[Category:IBM](https://ja.wikipedia.org/wiki/Category:IBM "wikilink") [Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink")

1.  [世界最速のスーパーコンピューターの開発に向け1億ドル規模の研究計画を発表 - 日本IBM](http://www-06.ibm.com/jp/press/1999/12076.html)
2.  [「Blue Gene」研究プロジェクト拡大を目的に米エネルギー省NNSAとIBMが提携 - 日本IBM](http://www-06.ibm.com/jp/press/2001/11122.html)
3.  [米エネルギー省向けに世界最速スーパーコンピューターを開発 - 日本IBM](http://www-06.ibm.com/jp/press/2002/11202.html)
4.  [IBM Blue Geneが最速スーパーコンピューター・リストで圧勝 - 日本IBM](http://www-06.ibm.com/jp/press/20070628002.html)
5.  [IBMが科学発展の原動力となるスーパーコンピューターを発表 最大100ペタフロップス演算性能を誇るBlue Gene/Qで現代の難問解決を支援 - 日本IBM](http://www-06.ibm.com/jp/press/2011/11/1802.html)
6.  [新たな科学技術の発見のためのエンジンとなったIBM Blue Gene - IBMの生んだチェス・チャンピオン「Deep Blue」の子孫として -](http://www-06.ibm.com/jp/press/20070516001.html)
7.
8.
9.
10.
11.
12. [IBM、Blue Geneで米国家技術賞を受賞 - ITmedia](http://www.itmedia.co.jp/enterprise/articles/0909/21/news004.html)
13.
14.
15.
16. [Supercomputing: Jülich Amongst World Leaders Again](http://www.pressebox.de/pressemeldungen/ibm-deutschland-gmbh-4/boxid-136200.html)
17. [Top500 Supercomputing List Reveals Computing Trends](http://www.serverwatch.com/hreviews/article.php/3913536/Top500-Supercomputing-List-Reveals-Computing-Trends.htm)
18. [IBM Research A Clear Winner in Green 500](http://www.datacenterknowledge.com/archives/2010/11/18/ibm-system-clear-winner-in-green-500/)
19. [IBM uncloaks 20 petaflops BlueGene/Q super](http://www.theregister.co.uk/2010/11/22/ibm_blue_gene_q_super/)
20. [US commissions beefy IBM supercomputer - IDG News Service](http://www.itworld.com/hardware/136215/us-commissions-beefy-ibm-supercomputer)
21. [Argonne National Laboratory Selects IBM Supercomputer to Advance Research - Based on next generation IBM Blue Gene, the 10 petaflop "Mira" supercomputer will fuel national innovation - IBM](http://www-03.ibm.com/press/us/en/pressrelease/33586.wss)