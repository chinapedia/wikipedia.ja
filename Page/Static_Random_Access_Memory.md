> この記事は[Static Random Access Memory](https://ja.wikipedia.org/wiki/Static_Random_Access_Memory)から翻訳されています。


[thumbクローンに使われていた](https://ja.wikipedia.org/wiki/ファイル:Hyundai_RAM_HY6116AP-10.jpg "wikilink")2K×8ビットSRAM\]\] **Static RAM**・**SRAM**（スタティックラム・エスラム）は、[半導体メモリ](../Page/半導体メモリ.md "wikilink")の一種である。[ダイナミックRAM](../Page/Dynamic_Random_Access_Memory.md "wikilink") (DRAM) とは異なり、定期的なリフレッシュ（回復動作）が不要であり、内部構造的に [フリップフロップ](../Page/フリップフロップ.md "wikilink")等の[順序回路という](https://ja.wikipedia.org/wiki/論理回路#順序回路 "wikilink")「スタティック(静的)な回路方式により情報を記憶するもの」であることからその名がある。「データ残留現象」といった性質\[1\]が無いわけでもないが、基本的に[電力](../Page/電力.md "wikilink")の供給がなくなると記憶内容が失われる[揮発性メモリ](https://ja.wikipedia.org/wiki/揮発性メモリ "wikilink")（volatile memory）である。但し原理上、アクセス動作が無ければ極く僅かな電力のみで記憶を保持できるため\[2\]、比較的大容量の[キャパシタ](https://ja.wikipedia.org/wiki/キャパシタ "wikilink")を電池交換中のバックアップとしたり、保存性のよい電池を組み合わせて不揮発性メモリのように利用したりといった利用法もある（特に後者はフラッシュメモリ一般化以前に、[ゲーム機](../Page/ゲーム機.md "wikilink")などのカートリッジ内のセーブデータ用に多用された）。

[ランダムアクセス](../Page/ランダムアクセス.md "wikilink")メモリ（[Random Access Memory](../Page/Random_Access_Memory.md "wikilink")）ではあるが、[ランダムアクセス](../Page/ランダムアクセス.md "wikilink")だからそう呼ばれているのではないので本来の語義からはほぼ完全に誤用として、読み書き可能という意味で慣用的にRAMと呼ばれているものである、という点についてはDRAMと同様である。

## 概要

[ダイナミックRAM](../Page/Dynamic_Random_Access_Memory.md "wikilink")（DRAM）と異なり、記憶部に[フリップフロップ回路](https://ja.wikipedia.org/wiki/フリップフロップ回路 "wikilink")を用いているため、リフレッシュ操作が不要であり、記憶保持状態での[消費電力](https://ja.wikipedia.org/wiki/消費電力 "wikilink")は極めて小さい。

DRAMと比べて記憶容量あたりの単価が高いため、高速な情報の出し入れが可能な点を生かした[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")での使用や、低消費電力を生かした携帯型機器での使用など、比較的データ量の少ない用途によく用いられる。また、低消費電力の例として、SRAMに小さな電池を内蔵あるいは外部に配置することで、主電源が供給されない間も記憶情報を保持する仕組みの[不揮発メモリ](https://ja.wikipedia.org/wiki/不揮発メモリ "wikilink")（NVRAM, コンピュータの[時計](../Page/時計.md "wikilink")や[BIOS設定情報の保持など](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")）が挙げられる（[バッテリーバックアップ](../Page/バッテリーバックアップ.md "wikilink")機能）。

なお、現在では従来のDRAMの記憶セルを用いながら、消費電力を低減してSRAMと同じインターフェースを持つ[疑似SRAM](https://ja.wikipedia.org/wiki/疑似SRAM "wikilink")もある。

また、SRAMの応用として、[プログラマブルロジックデバイス](../Page/プログラマブルロジックデバイス.md "wikilink")がある。これは、SRAMの高速動作を利用したものであり、[記憶セル](https://ja.wikipedia.org/wiki/記憶セル "wikilink")の状態によってマトリクス状の配線を接続・切断することにより、[ゲートアレイ](https://ja.wikipedia.org/wiki/ゲートアレイ "wikilink")として機能させる。プログラマブルロジックデバイスの一種である[FPGA](../Page/FPGA.md "wikilink")は、配線だけでなく論理セルの構造もSRAMによるLUT（[ルックアップテーブル](../Page/ルックアップテーブル.md "wikilink")）で構成されているものもある。

## 設計

[thumb](https://ja.wikipedia.org/wiki/ファイル:SRAM_Cell_\(6_Transistors\).svg "wikilink") SRAM内の各[ビット](../Page/ビット.md "wikilink")は4つの[トランジスタ](../Page/トランジスタ.md "wikilink")で構成される2つの交差接続された[インバータに格納される](https://ja.wikipedia.org/wiki/NOTゲート "wikilink")。その記憶セルは2つの安定状態があり、それぞれを **0** と **1** に対応させる。さらに読み出しと書き込みアクセスのために2つのトランジスタを必要とする。したがって、典型的なSRAMでは1ビットを格納するのに6個の[MOSFET](../Page/MOSFET.md "wikilink")（6T）を使用する。他にも8Tや10Tで記憶セルを構成するものもあるが\[3\]\[4\]、これは読み書きポートを複数実装するのに使われ、ある種のビデオメモリや[レジスタファイル](https://ja.wikipedia.org/wiki/レジスタファイル "wikilink")などがマルチポート型SRAM回路を使っている。

一般的に、セル当たりのトランジスタ数が少ないほど個々のセルを小さくできる。シリコンウェハーの製造コストは比較的一定であるため、セルが小さくなれば単位面積により多くのビットを格納でき、メモリのビット当たりのコストも低減される。

6Tよりも少ないトランジスタ数で記憶セルを構成することも可能だが、そのような3T\[5\]\[6\]や1Tのセルは実際には[DRAMであり](../Page/Dynamic_Random_Access_Memory.md "wikilink")、SRAMではない。例えば[1T-SRAM](https://ja.wikipedia.org/wiki/1T-SRAM "wikilink")と呼ばれるものがある。

セルへのアクセスは、ワード線（図ではWL）でイネーブルとなり、それによって2つのアクセス用トランジスタ M<sub>5</sub> と M<sub>6</sub> を制御し、次いでセル本体をビット線（図では<span style="text-decoration: overline;">BL</span>とBL）に接続すべきか否かを制御する。ビット線は読み取り操作と書き込み操作でのデータ転送に使われる。厳密にはビット線を2本持つ必要はないが、その信号と反転信号を同時に提供することで[ノイズマージン](https://ja.wikipedia.org/wiki/ノイズマージン "wikilink")を改善している。

読み取りアクセスでは、SRAMのセルが能動的にビット線を High または Low に駆動する。それに対して、[DRAMでは](../Page/Dynamic_Random_Access_Memory.md "wikilink")、ビット線がコンデンサと繋がっており、電荷共有（[charge sharing](https://ja.wikipedia.org/wiki/:en:charge_sharing "wikilink")）によって、ビット線がHighまたはLowとなるまでに少し時間がかかる。そのため、SRAMの方が帯域幅が大きくなる。SRAMのセルは対称形となっているため、[差動信号](https://ja.wikipedia.org/wiki/差動信号 "wikilink")処理が可能であり、小さな電圧の変化を容易に検出できる。また、DRAMと比べて、SRAMが高速動作できる他の要因として、商用のSRAMチップがアドレスを表す全ビットを同時に受け付けるという点も挙げられる。DRAMは、ピン数を減らして小型大容量化するためにアドレスビットが多重化されており、一度に全アドレスビットを受け付けられない。

アドレス線が *m* 本でデータ線が *n* 本のSRAMの大きさは、2<sup>*m*</sup> ワード または 2<sup>*m*</sup> × *n* ビットである。

## SRAM の動き

SRAMセルは3種類の異なる状態をとりうる。回路が何もしていない「スタンバイ」モード、データの読み取り要求に対応する「読み取り」モード、内容の更新をする際の「書き込み」モードである。読み取りモードと書き込みモードのSRAMはそれぞれ「読み取り可能性 (readability)」と「書き込み安定性 (write stability)」がなけれはならない。ここではそれら3つの状態を解説する。

### スタンバイ

ワード線がアサートされていないとき、アクセス用トランジスタ M<sub>5</sub> と M<sub>6</sub> がセル本体とビット線を切り離した状態となっている。交差接続された2つのインバータ（M<sub>1</sub> から M<sub>4</sub> で構成）はその間、状態を保持し続ける。

### 読み取り

図のQに格納されているセルの内容が **1** だとする。読み取りサイクルでは両方のビット線が **1** に事前充電され、次いでワード線 WL をアサートすることで両方のアクセス用トランジスタをイネーブル状態とする。次にQと<span style="text-decoration: overline;">Q</span>に保持されている値がビット線に転送される。Qが **1** なので、BLは事前充電された値のままとなり、<span style="text-decoration: overline;">BL</span>はM<sub>1</sub>とM<sub>5</sub>を通して **0** に放電される。BLの側ではトランジスタM<sub>4</sub>とM<sub>6</sub>がビット線をV<sub>DD</sub>すなわち **1** にする。メモリ内容が **0** だった場合、逆のことが起こり、<span style="text-decoration: overline;">BL</span>が **1** となり、BLが **0** となる。BLと<span style="text-decoration: overline;">BL</span>の電位差は小さくても、センスアンプがそれらの線のうちどちらの電位が高いかを判別し、格納されているメモリの値が **1** なのか **0** なのかを決定する。センスアンプの感度が高いほど、読み取り操作の速度が速くなる。

### 書き込み

書き込みサイクルは、まず書き込むべき値をビット線に印加することで始まる。**0** を書き込みたい場合、ビット線には **0** を入力する。つまり、<span style="text-decoration: overline;">BL</span>を **1**、BLを **0** とする。これは[RS型フリップフロップにリセットパルスを与えるのと同じであり](../Page/フリップフロップ.md "wikilink")、それによってフリップは状態を変化させる。ビット線に与える入力を逆転させると **1** が書き込まれる。次にWLをアサートすると、格納すべき値がラッチされる。これがうまく機能するには、ビット線の入力ドライバが相対的に弱いセル内のトランジスタよりも強く、交差接続されたインバータの状態を上書きできるよう設計する必要がある。SRAMセル内のトランジスタの大きさは慎重に決定する必要があり、それによって正しい動作を保証する。

### バスの動き

アクセス時間が70nsとされるメモリは、アドレス線群に正しいアドレス信号が送られてから70ナノ秒以内に対応するデータが出力される。しかし、データはある時間（5nsから10ns）だけ保持され続ける。また信号の0と1の間での遷移に要する時間も考慮する必要があり、約5nsと見積もられる。アドレスの下位ビットを順次変えながらある範囲のメモリを読み取る場合、アクセス時間はもっと短くなる（30nsなど）。

## 用途・用例

### 特徴

SRAMは一般に[DRAMに比べて高価だが](../Page/Dynamic_Random_Access_Memory.md "wikilink")、高速で消費電力が極めて低い（特にアイドル状態の場合）。そのため、高速性または低消費電力あるいは両方が要求される用途で使われることが多い。また、制御が容易（インタフェースが単純）で、最近のDRAMに比べるとより真の「ランダムアクセス性」があると言える。内部構造が複雑であるため、DRAMほど高密度に実装できず、大容量メモリには向かない。そのため[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")の[主記憶装置](../Page/主記憶装置.md "wikilink")のような低コストが要求される用途には使われていない。

#### クロック周波数と消費電力

SRAMの[電力](../Page/電力.md "wikilink")消費は、どの程度頻繁にアクセスされるかに依存する。頻繁にアクセスされる用途ではDRAMと同程度に電力を消費し、一部の[ICは最大帯域幅で使用すると何](../Page/集積回路.md "wikilink")[ワット](../Page/ワット.md "wikilink")も消費する。一方でアクセス頻度が小さい場合、例えばやや低いクロック周波数で駆動した[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")で利用する場合などは極めて消費電力が低くなり、アクセスがないアイドル状態ではほとんど無視できる程度の電力消費（数マイクロワット）となる。

SRAMには主に次のようなものがある。

  - 汎用製品
      - 「非同期」インタフェース。28ピンの32k×8ビットのチップ（XXC256 などの名称）や類似の製品。最大16Mビットのチップまである。
      - 「同期」インタフェース。[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")などバースト転送を要求される用途で使用される。最大18Mビット（256k×72ビット）のチップまである。
  - チップ上への統合
      - RAMまたはキャッシュとして[マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")に搭載（通常、32バイトから128[KBの容量](../Page/キロバイト.md "wikilink")）
      - 一次キャッシュとして[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")ファミリーや他の高性能[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")に搭載（8[KBから数MB](../Page/キロバイト.md "wikilink")）
      - マイクロプロセッサなどのレジスタの実装に使われている。[レジスタファイル](https://ja.wikipedia.org/wiki/レジスタファイル "wikilink")を参照。
      - 特殊なICや[ASIC](../Page/ASIC.md "wikilink")に搭載（一般に数KBのオーダー）
      - [FPGA](../Page/FPGA.md "wikilink")や[CPLD](../Page/CPLD.md "wikilink")

### 組み込み用途

産業システム、科学技術システム、自動車の車載エレクトロニクスなどによく遣われている。最近の電子機器や電子玩具には、ある程度の量（数KBかそれ以下）のSRAMがほとんど必ず搭載されている。デジタルカメラや携帯電話、シンセサイザーなどの複雑な製品には数MBのSRAMが搭載されている。

デュアルポート型のSRAMは、リアルタイム方式の[デジタル信号処理](../Page/デジタル信号処理.md "wikilink")[回路に使われることもある](../Page/電子回路.md "wikilink")。

### コンピュータにおける用途

SRAMは、パーソナルコンピュータ、ワークステーション、ルーター、その他周辺機器にも使われている。[CPU](../Page/CPU.md "wikilink")内蔵の[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")、外付けのバーストモードのSRAMキャッシュ、[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")のバッファ、[ルーター](../Page/ルーター.md "wikilink")のバッファなどである。[液晶ディスプレイ](https://ja.wikipedia.org/wiki/液晶ディスプレイ "wikilink")や[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")も表示（印刷）する画像を保持するのにSRAMを使っていることが多い。[CD-ROM](../Page/CD-ROM.md "wikilink")ドライブや[CD-RW](../Page/CD-RW.md "wikilink")ドライブでも256KB程度のバッファをSRAMで構成しており、ブロック単位でデータをバッファリングするのに使っている。同様に[ケーブルモデム](../Page/ケーブルモデム.md "wikilink")などの機器もSRAMをバッファとして使っている。

### 趣味

インタフェースが単純ということで趣味でデジタル回路を作る際にはSRAMが好まれることが多い。[DRAMに比べてリフレッシュサイクルがなく](../Page/Dynamic_Random_Access_Memory.md "wikilink")、アドレスバスとデータバスを[多重化](../Page/多重化.md "wikilink")せずに直接アクセスでき、回路設計が単純である。バスや電源供給以外にSRAMが必要とする制御は Chip Enable (CE)、Write Enable (WE)、Output Enable (OE) の3種類だけである。同期SRAMでは Clock (CLK) も必要となる。

## 種類

### nvSRAM

[nvSRAM](https://ja.wikipedia.org/wiki/nvSRAM "wikilink")はSRAMを内蔵しているが、主電源が切れた状態でも重要なデータを保持することができる[不揮発性メモリ](../Page/不揮発性メモリ.md "wikilink")である。nvSRAMの用途は幅広く、ネットワーク、航空宇宙、医療などで利用されている。電池を内蔵する方式のBBSRAM (Battery Backup SRAM) もnvSRAMと呼ばれることがあるが、大容量コンデンサと不揮発性メモリセルを内蔵していて、主電源が切れるとコンデンサに蓄えた電力を使って自動的にSRAMから不揮発性メモリにデータを転送して保持する方式のnvSRAMもある。

### 非同期SRAM

非同期SRAMは4Kbから32Mbのものがある。アクセス速度が高速であるため、キャッシュを持たない組み込みプロセッサの[主記憶装置](../Page/主記憶装置.md "wikilink")としてよく使われており、[パワーエレクトロニクス](../Page/パワーエレクトロニクス.md "wikilink")などの制御装置（自動車の車載エレクトロニクスなど）、計測システム（ICテスタ）、[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")、ネットワーク機器（スイッチ、ルーター、IP電話、[DSLAM](../Page/DSLAM.md "wikilink")）など様々な機器に使われている。

### トランジスタの種類による分類

  - [バイポーラトランジスタ](../Page/バイポーラトランジスタ.md "wikilink") - [TTLや](../Page/Transistor-transistor_logic.md "wikilink")[ECLで使用](../Page/エミッタ結合論理.md "wikilink")。非常に高速だが消費電力が大きい。
  - [MOSFET](../Page/MOSFET.md "wikilink") - [CMOS](../Page/CMOS.md "wikilink")で使用。低消費電力であり、今日の主流である。

### 機能による分類

  - [非同期](https://ja.wikipedia.org/wiki/非同期 "wikilink") - クロック信号とは独立しており、アドレスの変化によってデータの読み書きを制御する。
  - [同期](../Page/同期.md "wikilink") - クロック信号の変わり目（エッジ）を全てのタイミングに使用する。アドレス、データ、その他の制御信号も全てクロックに同期している。

### 特徴による分類

  - ZBT (zero bus turnaround) - ターンアラウンドとは、SRAMが「書き込み」から「読み取り」に遷移するときなどにかかるクロック数である。ZBT SRAMではこのターンアラウンドまたはレイテンシがゼロとなっている。
  - syncBurst - 同期バースト書き込みアクセスが可能なSRAM。書き込み速度が向上する。
  - DDR SRAM - 同期式、単一読み書きポートで、入出力がDDR（ダブルデータレート）となっているSRAM。
  - QDR SRAM - 同期式、読み取りポートと書き込みポートが独立しており、入出力がQDR（クアドラプルデータレート）となっているSRAM。

## 脚注・出典

## 関連項目

  - [ダイナミックランダムアクセスメモリ](https://ja.wikipedia.org/wiki/ダイナミックランダムアクセスメモリ "wikilink")（DRAM)

  - [SRAMカード](https://ja.wikipedia.org/wiki/SRAMカード "wikilink")

  - [バッテリーバックアップ](../Page/バッテリーバックアップ.md "wikilink")

  -
[Category:半導体メモリ](https://ja.wikipedia.org/wiki/Category:半導体メモリ "wikilink")

1.
2.  そのような動作モードを設計としてハードウェア的に持っている製品もある。
3.  [A 160 mV Robust Schmitt Trigger Based Subthreshold SRAM](http://ieeexplore.ieee.org/Xplore/login.jsp?url=/iel5/4/4317684/04317699.pdf?arnumber=4317699)
4.  United States Patent 6975532: [Quasi-static random access memory](http://www.freepatentsonline.com/6975532.html)
5.  United States Patent 6975531: [6F2 3-transistor DRAM gain cell](http://www.freepatentsonline.com/6975531.html)
6.  [3T-iRAM(r) Technology](http://www.tezzaron.com/technology/3T-iRAM.htm)