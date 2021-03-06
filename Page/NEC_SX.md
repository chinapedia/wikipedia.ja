> この記事は[NEC SX](https://ja.wikipedia.org/wiki/NEC_SX)から翻訳されています。


**SXシリーズ**は[日本電気](../Page/日本電気.md "wikilink") (NEC) が開発・提供している[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")のシリーズで、主戦力級の[ベクトル型スーパーコンピュータとして](../Page/ベクトル計算機.md "wikilink")、世界で唯一生き残っているシリーズである。2019年現在の最新モデルは[SX-Aurora TSUBASA](https://ja.wikipedia.org/wiki/NEC_SX-Aurora_TSUBASA "wikilink")（続き番号としてはSX-11に相当）である。

1983年にSX-2と下位モデルのSX-1を発表、1985年に出荷したのがシリーズのはじまりである。さらに廉価版のSX-0もラインナップされた。その後は主力機の新世代ごとに、末尾の数字を1つずつ増やしていた。サフィックスの数字や英字は、サブモデルや改良版（SX-2A、SX-3Rなど）やサーバモデル（SX-4B、SX-5S）や小型モデル（SX-6i、SX-8i）等を示す。

[TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")首位で話題となった[地球シミュレータ](../Page/地球シミュレータ.md "wikilink")の初代システムは本シリーズのSX-5、2代目システムはSX-9/E、そして3代目となる現行システムはSX-ACEがベースである。

## シリーズ

### SX-2, SX-1

1983年（昭和58年）4月発表。SXシリーズで最初に登場したのはSX-2である（1985年出荷）。SX-2の下位モデルとして、SX-1,SX-0が提供された。改良版として、SX-2A等が開発・出荷された。SX-2は世界で最初に[G](../Page/ギガ.md "wikilink")[FLOPS](../Page/FLOPS.md "wikilink")を越えた[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")で、[Cray-2](../Page/Cray-2.md "wikilink")に抜かれるまでのひとときであったが世界最高速であった。

### SX-3

1989年（平成元年）4月発表。[OSを](../Page/オペレーティングシステム.md "wikilink")、[ACOS-4](../Page/ACOS-4.md "wikilink")（メインフレーム用）ベースの[SX-OS](https://ja.wikipedia.org/wiki/SX-OS "wikilink")から、[Unixベースの](../Page/UNIX.md "wikilink")[SUPER-UX](../Page/SUPER-UX.md "wikilink")に切り替えたモデルである。その後、1990年に低価格モデル、1992年1月に改良型モデル(SX-3 R)を発表。最大4つのAPが構成できる。[メモリを共有して動作する](../Page/主記憶装置.md "wikilink")。CPも2つ構成できる。ベクトルレジスタの容量、[パイプラインの本数](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")、とAPの台数によって、1Lから44まで、10個のサブモデルがあった。

### SX-4

1994年（平成6年）11月発表。SX-3まではバイポーラ論理LSIを使っていたが、SX-4では[CMOS](../Page/CMOS.md "wikilink")論理LSIを使うようになった。このためサイクルタイムはSX-3Rの2.5nsから8nsに遅くなったが、消費電力と発熱の低下による空冷化と、[CPU](../Page/CPU.md "wikilink")モジュール1個のチップ数37、面積38.6cm x 45.7cmという高い実装密度により、コストパフォーマンスは向上している。

計算性能は、ノードあたり64[G](../Page/ギガ.md "wikilink")[FLOPS](../Page/FLOPS.md "wikilink")、システムあたり最大1024GFLOPSとなった。SX-3同様ノード単位で[メモリを共有するが](../Page/主記憶装置.md "wikilink")、ノード間では分散したシステム間で協調動作を行う。コンパクトモデル、シングルノードモデル、マルチノードモデルがあった。（1[ノード](https://ja.wikipedia.org/wiki/ノード "wikilink")は1つの処理単位、言い替えれば[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) が動作する単位である）

### SX-5

[thumb](https://ja.wikipedia.org/wiki/ファイル:Vcfe2007_img_5174.jpg "wikilink") 1998年（平成10年）6月発表。シングル[ノード](https://ja.wikipedia.org/wiki/ノード "wikilink")の最大[CPU](../Page/CPU.md "wikilink")数は16個(128GFLOPS)、最大共有メモリ容量は128GB、主記憶転送速度は1024GB/sであった。

SX-4と同様にCMOSを採用、集積化を進めチップの処理速度向上施策と共に排熱設計/多層配線などにより全体の処理速度の向上を図ったモデルがSX-5であり、クロックが4ns(250MHz)、ベクトル命令パイプラインが16本と、SX-4に比べCPUモジュール1個あたりの性能が4倍の8GFLOPSとなった。この32チップで構成されたCPUモジュールを1チップLSI化したのが初代[地球シミュレータ](../Page/地球シミュレータ.md "wikilink")のCPUである。

1999年5月に、ベクトルパイプラインが半分の8本のサーバモデルSX-5Sを発表。2000年6月クロックを約3.2nsに向上させた1CPUモジュール10GFLOPSのモデルを発表。このCPU演算性能強化モデルではシングルノードの最大演算性能は160GFLOPSと向上したが主記憶転送速度は640GB/sに低下した。

### SX-6

2001年（平成13年）10月発表。シングルノードの最大CPU数は8個(64GFLOPS)、最大共有メモリ容量は64GB、主記憶転送速度は256GB/sであった。[地球シミュレータ](../Page/地球シミュレータ.md "wikilink")のシングルノードを改良(メモリ容量が2倍)したものを用いている。従来はスカラー部とベクトル部は同期動作だったが、地球シミュレータ同様にベクトル部がスカラー部の倍速で動作するように改良された。クロック2ns(500MHz）で動作する[スカラ演算ユニットと](https://ja.wikipedia.org/wiki/スカラー "wikilink")、クロックが1ns(1GHz)で動作する8本のベクトルパイプラインを持つ、1チップベクトルプロセッサから構成されている。0.15μmCMOSプロセスを採用している。

2001年11月にデスクサイドモデルSX-6i（1CPU、メモリ最大搭載量8GB）を発表。

2003年9月に9GFLOPS CPUとシングルノード当たりの最大メモリ容量が2倍(128GB,主記憶転送速度289GB/s)の機種を発表。

### SX-7

2002年（平成14年）10月発表。シングルノードの最大CPU数は32個(282GFLOPS)、最大共有メモリ容量は256GB、主記憶転送速度は1131GB/sである。基本的にはSX-6のシングルノード内のCPU数と最大共有メモリ量を拡張したモデル。0.15μmCMOSプロセスを採用。

### SX-8

2004年（平成16年）10月発表。シングルノードの最大CPU数は8個(128GFLOPS)、最大共有メモリ容量は64GB(FCRAM)/128GB(DDR2-SDRAM)、主記憶転送速度は512GB/sである。1ノード1モジュールを達成しCPUとメモリモジュール間にSX-6/7まで有った同軸布線20,000本を廃しカード化（ケーブルレス化）を高密度実装(15インチUXGAディスプレイの画素と同じ密度の外部接続ピン密度）を用いて実現した。90nmCMOSプロセスを採用。クロックが SX-6比2倍、スカラ演算ユニット1ns(1GHz), ベクトル演算ユニット0.5ns(2GHz)となり1CPUあたり16GFLOPSを達成。SXシリーズとしては初のSQRT命令のハードウェアサポートを実現。

2005年9月、SX-6iの後継相当のデスクサイドモデルSX-8i発表。SX-6iで不評だった最大搭載メモリ量を32GBと大幅に拡大し、主記憶転送速度は64GB/s。

### SX-8R

2006年（平成18年）10月発表。ベクトルプロセッサ(CPU)の中枢機能であるベクトル加算器と乗算器を倍増し、CPU当たりの性能を従来機に比べ2倍以上の35.2GFLOPS(従来は16GFLOPS)に向上した。同時に、1CPU(シングルコア)当たりの最大ベクトル性能で100GFLOPSを超える1チップベクトルプロセッサを搭載した次期ベクトルスーパーコンピュータを開発中であることを表明した。

### SX-9

2007年（平成19年）10月発表。ペタフロップス時代を視野に入れ開発された。当初の予定通り1チップベクトルプロセッサを採用し、プロセッサ当たりの性能は100GFLOPSを越える。(発表時点ではシングルプロセッサとして世界最高性能)これに伴い、性能当たりの電力効率を大幅に向上させている。65nm CMOSプロセス、11層銅配線採用。最大で8192台のCPUを接続できる。ノード間の接続速度も見直され、回線交換方式からパケット交換方式に変更。最大で256GB/S(128GB/S×2)となった。オペレーティングシステムはSUPER-UXを継続採用している。

### SX-ACE

2011年（平成23年）11月に開発開始を発表\[1\]。SX-9と比較し、性能当たりの消費電力を1/10に、設置面積を1/5に、CPUコア性能を64GFLOPSに、データ転送速度をCPUコア当たり64GB/sにする事を目指すとしていた。SXシリーズとして初めて複数のCPUコアを1チップ上に集積するマルチCPUコアのLSIを採用した。

名称については、2013年4月のCool Chips 16では決まっていないとのことでNGVと呼んでいたが、筐体の写真にはSX-Xとあった\[2\]（なお、SX-Xという仮称はSX-3の開発中などで使っている例がある\[3\]）。発売時にSX-ACEとして発表された。

2013年11月発売、SC13で展示もおこなわれた。「SX-10」は商標登録されており使えなかったため変えたとのことである。\[4\]。ACEの名は16進法などで10に使う記号であるAを意識している。\[5\]

### SX-Aurora TSUBASA

2017年10月25日に、発売予定を発表した\[6\]。演算器周辺は前世代までと同様のパイプライン演算器だが、ノードをPCIeカードに実装し、それを1枚使用するデスクサイドマシン形態の最小構成から、多数使用するラック実装のスーパコンピュータセンタ向けまでを揃えている（地球シミュレータの更新が2020年代前半にあると思われるが、それとの関連についての情報は2018年末の時点では無い）。そしてPCIe化にともない、管理側のシステムが変更され、ハードウェアの面では管理側（NECでは、演算側の「ベクトルエンジン」に対し「ベクトルホスト」と呼んでいる）が独自の専用アーキテクチャからx86機ベースに、ソフトウェアの面ではOSはSUPER-UXから、[Unix系](../Page/Unix系.md "wikilink")である点は同じだが\[7\]Linuxに更新された。8コアのベクトルエンジンは、SX-ACEと比較し、性能当たりの消費電力を1/5に、設置面積を1/10に、CPUコア性能を307GFLOPSに、データ転送速度をCPUコア当たり150GB/sとした\[8\]。

## アーキテクチャ

[アーキテクチャはSX](../Page/コンピュータ・アーキテクチャ.md "wikilink")-3以前(SX-2まで)とそれ以降は多少差はあるが、ここでは全体的な特徴について説明する。大きく分けて2つのユニットから構成されている、非対称密結合マルチプロセッサ構成をとっている。また同時期に開発された他系統の機種と比較すると、[日立のもの](../Page/日立製作所.md "wikilink")（HITAC S-810）と対照的で、S-810は既存メインフレームの拡張という形態であるのに対し、SXシリーズでは制御部のメインフレームとは分離独立した形態をとった\[9\]。

また、モデル毎に高速化をはかる機能が追加されてきている。たとえば、[パイプラインの増加](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")、[命令セット](../Page/命令セット.md "wikilink")の強化(8[バイト演算命令の追加など](../Page/バイト_\(情報\).md "wikilink"))、データのロード/ストア用のバスの分離や強化などがあげられる。

### 制御プロセッサ(CP)

#### SX-2までのアーキテクチャ

いわゆる[汎用コンピュータ](https://ja.wikipedia.org/wiki/汎用コンピュータ "wikilink")的な仕事をする所である。[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) はこのプロセッサ上で実行される。データの入出力、[プログラムの編集や](../Page/プログラム_\(コンピュータ\).md "wikilink")[コンパイル作業などを行う](../Page/コンパイラ.md "wikilink")。SX-2までは[ACOS-4](../Page/ACOS-4.md "wikilink")系の汎用コンピュータである。CPはさらに、通常の演算を行うEPUとシステム制御部(SCU)から構成される。入出力を行うIOPもSCUから接続される。

#### SX-3以降のアーキテクチャ

SX-3以降は[UP4800](../Page/UP4800.md "wikilink")等の[UNIX](../Page/UNIX.md "wikilink")サーバとなった。CP単独で処理をする、というようなイメージではなくなった。APの制御、入出力処理の制御を行うためのプロセッサという役割になった。

### 演算プロセッサ(AP)

数値演算のプログラムを実行するだけのプロセッサである。[アーキテクチャはSXシリーズ用に新たに開発された](../Page/コンピュータ・アーキテクチャ.md "wikilink")。[RISC](../Page/RISC.md "wikilink")形式風の命令セットであり、1命令は4[バイトまたは](../Page/バイト_\(情報\).md "wikilink")8バイトである。基本的に64[ビット](../Page/ビット.md "wikilink")マシンである。大きく分けて[スカラ演算ユニット](https://ja.wikipedia.org/wiki/スカラー "wikilink")(SU)、[ベクトル演算](https://ja.wikipedia.org/wiki/ベクトル演算 "wikilink")ユニット(VU)とインターフェースユニット(IU)から構成される。

APはSX-2,SX-1,SX-0は1システムに1ユニットであるが、SX-3以降は1システムに複数ユニット構成できるようになった。そのため、各APは共有メモリ型マルチプロセッサを構成している。

数値演算を高速に行うために、ベクトル演算機能が用意されている。スカラ演算は、RISC風のため、SX-2シリーズにおいては、同社で当時最新の[汎用コンピュータ](https://ja.wikipedia.org/wiki/汎用コンピュータ "wikilink") S1000の3.5倍以上を目標に設計されていた。ベクトル演算機能とスカラ演算機能(汎用[レジスタ](../Page/レジスタ_\(コンピュータ\).md "wikilink"))は独立しているため、並行に動作可能である。[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")は、[命令キャッシュと](../Page/命令_\(コンピュータ\).md "wikilink")[オペランドキャッシュが独立している](https://ja.wikipedia.org/wiki/被演算子 "wikilink")。

データを高速に処理するための工夫が用意されている。たとえば、SX-2,1においては、メモリは512ウェイインターレース(最大)構成をとっていて、6ns[クロック](../Page/クロック.md "wikilink")のスピードと共に、最大11[G](../Page/ギガ.md "wikilink")[バイト](../Page/バイト_\(情報\).md "wikilink")/sのデータ転送能力(SX-2において)、1.3G [FLOPS](../Page/FLOPS.md "wikilink")(SX-2)の性能を誇る。クロックはSX-3Rで2.5nsまで高速化されたが、SX-4ではデバイスが[CMOS](../Page/CMOS.md "wikilink")になったため、8nsまで遅くなった。

#### レジスタ

SX-2の[レジスタはおおよそ以下のとおりである](../Page/レジスタ_\(コンピュータ\).md "wikilink")。なお、SX-1では[ベクトル](../Page/ベクトル.md "wikilink")関係のレジスタはSX-2の半分になる。SX-3以降も基本的にはこの構成をとっている。

  - [スカラレジスタ](https://ja.wikipedia.org/wiki/スカラー "wikilink")(64[ビット](../Page/ビット.md "wikilink")×128個)
  - ベクトルレジスタ(256語×40個:80Kバイト)
  - ベクトルマスク(256ビット×8個)
  - その他(カウンタ類)

##### ベクトル演算機能

[ベクトル演算](https://ja.wikipedia.org/wiki/ベクトル演算 "wikilink")機能は4つの[パイプライン](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")(SX-3まで、SX-4は最大8つ、モデルによって本数は変わる)を持っている。そのため、1サイクルで複数の演算を同時に行うことが出来る。また、ベクトル演算機能は、[加算](https://ja.wikipedia.org/wiki/加算 "wikilink")、[乗算](https://ja.wikipedia.org/wiki/乗算 "wikilink")、[論理演算](../Page/論理演算.md "wikilink")、[シフト演算](https://ja.wikipedia.org/wiki/シフト演算 "wikilink")の4つの演算機能が別々に用意されている。そのため、それぞれの演算を独立して行うことが出来る。たとえば、

``` fortran
   DO 100 I = 1, 100
     C(I) = A(I) + B(I)
 100 CONTINUE
```

というようなDO[ループはベクトル演算命令の](../Page/ループ_\(プログラミング\).md "wikilink")1マシン[命令に](../Page/命令_\(コンピュータ\).md "wikilink")[コンパイルされ](../Page/コンパイラ.md "wikilink")、実行される(ベクトル化。詳しくは[ベクトル化](../Page/ベクトル化.md "wikilink")のページを参照のこと)。もちろん、[浮動小数点数](../Page/浮動小数点数.md "wikilink")だけではなく[整数](../Page/整数.md "wikilink")に対してもベクトル処理が可能である。

また、ベクトルマスク機能を使い、ベクトル内で演算対象のものだけをふるい分けたり、ベクトルをマスクの価によって圧縮、伸張するような演算を行うことが出来る。そのため、より高速な演算が可能である。この機能は、DO[ループ内にある](../Page/ループ_\(プログラミング\).md "wikilink")[IF文内のベクトル演算](../Page/If文.md "wikilink")(条件付き演算)を高速に行うために用意されている。

そのほか、累和を高速に求める機能や、浮動小数点数の0.5倍/2倍を高速に行う機能も用意されている。

##### スカラ演算機能

[スカラ演算機能も](https://ja.wikipedia.org/wiki/スカラー計算機 "wikilink")[パイプライン化で高速化されている](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")。

さらに、SX-3では、[命令の](../Page/命令_\(コンピュータ\).md "wikilink")[アウト・オブ・オーダー実行](../Page/アウト・オブ・オーダー実行.md "wikilink")機能が加わった。

SX-4では[スーパースカラー化されている](https://ja.wikipedia.org/wiki/スーパースケーラ "wikilink")。同時に2命令のデコード、フェッチと分岐を含め、最大4命令が同時に実行可能である。[固定小数点数](../Page/固定小数点数.md "wikilink")演算用の演算器が2つ、[浮動小数点数](../Page/浮動小数点数.md "wikilink")演算用の演算器が1つ、[乗算](https://ja.wikipedia.org/wiki/乗算 "wikilink")器が1つある。固定小数点数演算は1マシンサイクル、浮動小数点数演算も2マシンサイクルで実行可能であり、極めて高速な演算が可能になっている。

#### 命令セット

[命令セット](../Page/命令セット.md "wikilink")は3[オペランド形式である](https://ja.wikipedia.org/wiki/被演算子 "wikilink")。演算はすべて[レジスタで行なわれる](../Page/レジスタ_\(コンピュータ\).md "wikilink")。[RISC](../Page/RISC.md "wikilink")風のため、演算[命令とロード](../Page/命令_\(コンピュータ\).md "wikilink")/ストア命令が分かれている(メモリ上のデータをレジスタ上の値と演算を行う命令はない)。

[スカラ演算用の命令と](https://ja.wikipedia.org/wiki/スカラー "wikilink")[ベクトル演算](https://ja.wikipedia.org/wiki/ベクトル演算 "wikilink")用の命令が分かれている。スカラ演算用の命令(RX型)は1命令1[ワード](../Page/ワード.md "wikilink")(4[バイト](../Page/バイト_\(情報\).md "wikilink"))または2ワード（8バイト）である。1バイトの[オペコード](../Page/オペコード.md "wikilink")の後に、3つのオペランドが続く。オペランドはレジスタ、インデックスレジスタ、あるいは即値である。

ベクトル演算用の命令(RR型/RV型)も、1バイトのオペコードの後に3つのオペランドが続く。主な命令は

  - ベクトルのロード/ストア
  - [四則演算](https://ja.wikipedia.org/wiki/四則演算 "wikilink")
  - [論理演算](../Page/論理演算.md "wikilink")/[シフト演算](https://ja.wikipedia.org/wiki/シフト演算 "wikilink")
  - [整数](../Page/整数.md "wikilink")←→[浮動小数点数](../Page/浮動小数点数.md "wikilink")変換
  - マスク制御/マスク演算

などが用意されている。演算は、ベクトルとベクトルの演算だけではなく、ベクトルとスカラーの演算なども用意されている。このため、ベクトルに特定の価を足したり掛けたりするようなDO[ループが](../Page/ループ_\(プログラミング\).md "wikilink")、[ハードウェア](../Page/ハードウェア.md "wikilink")的な1命令で実行できる。

また、数値演算専用のプロセッサのため、いわゆる10進演算等の命令は用意されていない。基本的にワード(64ビット)単位の処理であるが、ロード/ストア命令についてはバイト/16ビット単位のものが用意されている。

SX-3では、64[ビット](../Page/ビット.md "wikilink")整数演算命令、最大値/最小値検索命令等が追加されている。

SX-4では、浮動小数点演算に、[IBM](../Page/IBM.md "wikilink")形式、[CRAY形式の他に](../Page/クレイ.md "wikilink")、[IEEE](../Page/IEEE.md "wikilink")形式もサポートするようになった。

ベクトル命令は、複数のオペランドを持つが、1つのベクトルのオペランドを全て処理してから次のベクトル命令を実行すると処理が遅くなる。SXシリーズでは、1つのベクトルのオペランドが演算を終えた後、次のベクトル命令の処理を開始する機能がハードウェアによって用意されている。このため、ベクトル命令の高速化が可能である。

## 実装

### 筐体形状

SX-2(SX-1を含む)では、配線を最適化するために、APとメモリ部分がY型になっている。APの先に、CPやIOPが接続される。冷却機構は別筐体である。水冷のため、SX-2本体はそばによっても熱を感じず、ひんやりとして、音も静かであるが、冷却機構の空気吹き出し口(機構の上部)は猛烈に熱い風が吹き上げている。

SX-3では各筐体が平行に並び、その装置間をインタフェースユニットが接続している。

SX-4では、1つのユニットの筐体が人の形に似た、非常に特徴のある形状になっている。

### 水冷方式

SX-2以降、AP、CPとも主要部分は水冷方式となっている。SX-2では複数のICを集積したICモジュールに10cm四方の水冷ユニットが取り付けられている。 SX-3では、APのみLCM（リキッドクーリングモジュール）と呼ばれる30×20cm程度のモジュールが採用され複数の集積回路と水冷機構が一体となっている。CPは[UNIX](../Page/UNIX.md "wikilink")サーバとなったため空冷化となり、外部に設置する設備の大幅な縮小が可能となった。

SX-4ではチップが[CMOS](../Page/CMOS.md "wikilink")になったため、空冷になっている。

## ソフトウェア

### OS

#### SX-2までのOS

SX-2、SX-1は、[ACOS-4](../Page/ACOS-4.md "wikilink")をベースとした[SX-OS](https://ja.wikipedia.org/wiki/SX-OS "wikilink")という[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS)で動作している。 ACOS-4系で提供されている機能がほとんどすべて動作可能である。また、ACOS-4/MVP XE と[疎結合マルチプロセッサ構成をとることが出来る](https://ja.wikipedia.org/wiki/疎結合クラスター "wikilink")(ディスクの共有)。

さらに、チェックポイントリスタート機能を有している。この機能を使うことで、長期間処理を行う[ジョブ](https://ja.wikipedia.org/wiki/ジョブ "wikilink")を分割して実行したり、出力制限値を越えてしまってアボートしたジョブのリスタートも可能になる。長い数値計算を行う処理には便利である。

#### SX-3以降のOS

SX-3以降は、[メインフレーム](../Page/メインフレーム.md "wikilink")ベースの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) をやめ、[UNIX](../Page/UNIX.md "wikilink")ベース([System V](../Page/UNIX_System_V.md "wikilink") ベース)のOS、[SUPER-UX](../Page/SUPER-UX.md "wikilink")となった。ベースは System V ではあるが、4.3[BSD](../Page/BSD.md "wikilink")の機能を取り入れ、[ネットワーク関係等が強化されている](../Page/コンピュータネットワーク.md "wikilink")[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")だけではなく、[OSIへの対応もなされている](https://ja.wikipedia.org/wiki/開放型システム間相互接続 "wikilink")。そのほかの特徴は以下のとおり。

  - [マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")対応
    [カーネル](../Page/カーネル.md "wikilink")の[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")化を行なっている。
  - 2つのページサイズ
    32K[バイトと](../Page/バイト_\(情報\).md "wikilink")1Mバイトのページサイズを提供している。UNIXコマンドのような小さなプログラムは32Kバイト、科学技術計算には1Mバイトのページサイズを割り当てている。どちらを使うかは、実行可能バイナリファイルに設定されている。
  - オーバレイ機能
    メモリを効率的に使うため、[サブルーチン](../Page/サブルーチン.md "wikilink")単位にオーバレイ機能を使うことが出来る。この機能は[ソースプログラムを変更することなく実行可能である](../Page/ソースコード.md "wikilink")。
  - スケジューリング機能の大幅な変更
    通常の処理(UNIXコマンドによる対話的な処理)と、数値演算のような[バッチ的な処理のスケジューリングを適切に行うために](../Page/バッチ処理.md "wikilink")、ドメイン、スケジューリンググループという機能を用意している。
      - ドメイン
        会話処理ドメインとバッチ処理ドメインが用意されている。それぞれに対して、CPU配分、メモリ配分を設定できる。
      - スケジューリンググループ
        ユーザ毎にスケジュール方法を設定できる。従来のUNIX風のスケジュール方法の他に、固定的にスケジュールを設定する機能も、バッチ的な処理のために用意されている。
      - [ファイルシステム](../Page/ファイルシステム.md "wikilink")の改良
        ファイルシステムはs5fs(System V固有のファイルシステム)をベースに改良したSFS(Supercomputing File System)である。このファイルシステムは、基本的なUNIXのファイルシステムをベースに、大量の[入出力](../Page/入出力.md "wikilink") (I/O) に対応するように改良されている。たとえば、I/O単位がブロックをまとめたクラスタ単位である、[カーネル](../Page/カーネル.md "wikilink")の[バッファ](../Page/バッファ.md "wikilink")を使わず、直接ユーザ[アプリケーションとI](../Page/アプリケーションソフトウェア.md "wikilink")/Oを行う、仮想ボリューム機能を用いて、ディスク容量より大きな[ファイルを作成できるなどである](../Page/ファイル_\(コンピュータ\).md "wikilink")。
      - NQS機能
        [バッチ処理](../Page/バッチ処理.md "wikilink")を効率的に行うために、NQS(Network Queuing System)という[ジョブ](https://ja.wikipedia.org/wiki/ジョブ "wikilink")管理システムが提供されている。

SX-4対応のOSでは、SVR4.2MP (System V Release 4.2 MP) 対応になった。また、[並列処理](https://ja.wikipedia.org/wiki/並列処理 "wikilink")も、SX-3ではタスクライブラリという[Fortran指向のライブラリを用意していたが](../Page/FORTRAN.md "wikilink")、SX-4では[POSIXスレッド](https://ja.wikipedia.org/wiki/POSIXスレッド "wikilink")を使えるようになった。また、より並列度が上がるように、粒度を向上したり、アトミック命令が追加されている。

### コンパイラ

#### SX-2まで

SX-2、SX-1では、AP上で実行するバイナリを生成する [FORTRAN](../Page/FORTRAN.md "wikilink")77/SXと、CP上で実行可能なバイナリを生成するFORTRAN77が提供されている。CP上では、FORTRAN77以外にも[COBOL](../Page/COBOL.md "wikilink")や[PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")など、他の言語もコンパイル、実行可能である。しかし、AP上で処理可能な[高水準言語](../Page/高水準言語.md "wikilink")は、FORTRAN77しかない。

CP上実行可能なFORTRANは、[デバッグ](../Page/デバッグ.md "wikilink")用途である。また、FORTRANの[ソースコード](../Page/ソースコード.md "wikilink")を整形するBEAUTIFIERや、動作を解析する(動的/静的)ANALIZER/SX、対話的に[ベクトル化](../Page/ベクトル化.md "wikilink")を推進するVECTRIZER/SXも用意されている。

#### SX-3以降

SX-3以降の[SUPER-UX](../Page/SUPER-UX.md "wikilink")向けには、新しい[ハードウェア](../Page/ハードウェア.md "wikilink")に対応して、[コンパイラ](../Page/コンパイラ.md "wikilink")も機能強化されている。たとえば、8[バイト整数](../Page/バイト_\(情報\).md "wikilink")、[ベクトル](../Page/ベクトル.md "wikilink")[レジスタの容量拡大対応などである](../Page/レジスタ_\(コンピュータ\).md "wikilink")。機能的にも、外部手続きをインラインで展開したり、[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")演算を認識して、[関数呼び出しに変えたり](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")、[ループ数を減らして](../Page/ループ_\(プログラミング\).md "wikilink")、ループ内演算を増やして([ループアンローリング](https://ja.wikipedia.org/wiki/ループアンローリング "wikilink"))、[メモリアクセスの軽減](../Page/主記憶装置.md "wikilink")、ベクトルレジスタの効率的な利用をはかるように改良されている。

さらに、APが複数あることを利用し、[並列実行を行う機能が用意されている](https://ja.wikipedia.org/wiki/並列処理 "wikilink")。並列実行は、[サブルーチン](../Page/サブルーチン.md "wikilink")レベルで並列化を行う、マクロタスク機能、ループ内演算を並列化する、マイクロタスク機能がある。マクロタスク機能はソースコードレベルでの修正が必要だが、マイクロタスク機能機能では自動的に並列化が行なわれる。さらに、より高度な並列化を行うために、並列化を指示するような命令や、並列実行のための補助的な命令も追加されている。

また、SUPER-UXでベースとなっている[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) が[UNIX](../Page/UNIX.md "wikilink")であるので、UNIXに関係が深い[C言語](../Page/C言語.md "wikilink")もサポートしている。C言語でも[FORTRAN](../Page/FORTRAN.md "wikilink")と同様、[ベクトル化](../Page/ベクトル化.md "wikilink")機能を有効に使えるようなコード生成を行なえるようになっている。

性能向上のためのツールは、新たに、ANALIZER-P/SXと、PARALLELIZER/SXが提供されている。

SX-4からはFORTRAN90が提供されている。 また、SX-4用のコンパイラは、SX-4で新たに追加された命令や、高速化のための[アーキテクチャの改良を取り込んで最適化を行なっている](../Page/コンピュータ・アーキテクチャ.md "wikilink")。さらに、マルチノードにも対応している。

## アメリカによるダンピング課税問題

SXシリーズは、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink") (米国) において[ダンピング](https://ja.wikipedia.org/wiki/ダンピング "wikilink")を行っていると大幅に課税されたことがある。これは、当時、米国社製の[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")に比べ、SX-3等の価格が安かった為でもある。当時、米国にはSX-3は殆ど輸出されておらず、専ら米国国外でSX-3の出荷が順調に進み、米国社製のスーパーコンピュータの販売がしにくくなった為でもある。

米国などのスーパーコンピュータメーカでは制御系を専用マシンで補わなければならないためこの製作が高額であった。これに対し[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")メーカーは自社の汎用マシンで補い、さらに、SX-3等では小型汎用サーバに置き換える事により大幅な価格差が生じる結果となった。

米国では軍事産業保護の観点からスーパーコンピュータも保護すべき対象となっていた為、安価であった日本のスーパーコンピュータの導入は一向に進まなかった。 後に、米国国内でも安価なスーパーコンピュータが使えない事に抗議の声が上がり、この問題は消え去ることとなった。2001年2月28日に、[日本電気](../Page/日本電気.md "wikilink") (NEC) は[クレイ](../Page/クレイ.md "wikilink")社にSXシリーズを[OEM](../Page/OEM.md "wikilink")することで合意している。なお、詳しい経緯については[日米スパコン貿易摩擦](../Page/日米スパコン貿易摩擦.md "wikilink")を参照されたい。

## SX シリーズ システム

SX-4, SXシリーズ以降のスーパーコンピュータは二重並列構成である。複数の[CPU](../Page/CPU.md "wikilink")は[並列](https://ja.wikipedia.org/wiki/並列計算機 "wikilink")[ベクトル処理ノードに配置される](../Page/ベクトル計算機.md "wikilink")。 これらのノードは標準的な[SMP構成である](../Page/対称型マルチプロセッシング.md "wikilink")。

|                                                                   | SX-2                                  | [SX-3](https://ja.wikipedia.org/wiki/NEC_SX-3 "wikilink") | SX-4  | SX-5   | [SX-6](https://ja.wikipedia.org/wiki/NEC_SX-6 "wikilink") | SX-7   | [SX-8](https://ja.wikipedia.org/wiki/NEC_SX-8 "wikilink") | SX-8R  | [SX-9](https://ja.wikipedia.org/wiki/NEC_SX-9 "wikilink") | [SX-ACE](https://ja.wikipedia.org/wiki/NEC_SX-ACE "wikilink") |
| ----------------------------------------------------------------- | ------------------------------------- | --------------------------------------------------------- | ----- | ------ | --------------------------------------------------------- | ------ | --------------------------------------------------------- | ------ | --------------------------------------------------------- | ------------------------------------------------------------- |
| 最大CPUの個数                                                          | 1                                     | 4                                                         | 32    | 16     | 8                                                         | 32     | 8                                                         | 8      | 16                                                        | 1                                                             |
| ピーク CPU [GFLOPS](https://ja.wikipedia.org/wiki/GFLOPS "wikilink") | 1.3                                   | 5.5                                                       | 2     | 8      | 8                                                         | 8.83   | 16                                                        | 35.2   | 102.4                                                     | 256                                                           |
| ピークシステム GFLOPS                                                    | 1.3                                   | 22                                                        | 64    | 128    | 64                                                        | 282    | 128                                                       | 281.6  | 1638                                                      | 256                                                           |
| 最大主メモリ                                                            | 256 [MB](../Page/メガバイト.md "wikilink") | 2 [GB](../Page/ギガバイト.md "wikilink")                       | 16 GB | 128 GB | 64 GB                                                     | 256 GB | 128 GB                                                    | 256 GB | 1 [TB](../Page/テラバイト.md "wikilink")                       | 1 [TB](../Page/テラバイト.md "wikilink")                           |
| システムメモリ帯域幅 (GB/s)                                                 | 11                                    | 44                                                        | 512   | 1,024  | 256                                                       | 1,129  | 512                                                       | 563.2  | 4,096                                                     | 256                                                           |
| CPU毎のメモリ帯域幅 (GB/s)                                                | 11                                    | 22                                                        | 16    | 64     | 32                                                        | 35.3   | 64                                                        | 70.4   | 256                                                       | 256                                                           |
|                                                                   |                                       |                                                           |       |        |                                                           |        |                                                           |        |                                                           |                                                               |

シングルノード SX システム

|                 | SX-4   | SX-4A  | SX-5 | [SX-6](https://ja.wikipedia.org/wiki/NEC_SX-6 "wikilink") | [SX-8](https://ja.wikipedia.org/wiki/SX-8 "wikilink") | SX-8R  | [SX-9](https://ja.wikipedia.org/wiki/SX-9 "wikilink") | [SX-ACE](https://ja.wikipedia.org/wiki/NEC_SX-ACE "wikilink") |
| --------------- | ------ | ------ | ---- | --------------------------------------------------------- | ----------------------------------------------------- | ------ | ----------------------------------------------------- | ------------------------------------------------------------- |
| 最大ノード数          | 16     | 16     | 32   | 128                                                       | 512                                                   | 512    | 512                                                   | 512                                                           |
| 最大CPUの個数        | 512    | 256    | 512  | 1,024                                                     | 4,096                                                 | 4,096  | 8,192                                                 | 512                                                           |
| ピーク TFLOPS      | 1      | 0.5    | 4    | 8                                                         | 65                                                    | 140.8  | 839                                                   | 131                                                           |
| 最大主メモリ          | 256 GB | 512 GB | 4 TB | 8 TB                                                      | 64 TB                                                 | 128 TB | 512 TB                                                | 32 TB                                                         |
| 合計メモリ帯域幅 (TB/s) | 8      | 4      | 32   | 32                                                        | 131                                                   | 281.6  | 2,048                                                 | 131                                                           |

マルチノード SX システム

## 参考文献

  - SXシステムの開発背景、NEC技報,Vol39 No1/1986
  - SXシステムの概要、NEC技報,Vol39 No1/1986
  - SXシステムの科学演算処理装置、NEC技報,Vol39 No1/1986
  - SXシステムの制御プログラム、NEC技報,Vol39 No1/1986
  - SX-3シリーズの開発背景と概要、NEC技報,Vol45 No2/1992
  - SX-3シリーズのハードウェア構成、NEC技報,Vol45 No2/1992
  - オペレーティングシステム SUPER-UX NEC技報,Vol45 No2/1992
  - SX-3シリーズの言語プロセッサと開発支援ツール、NEC技報,Vol45 No2/1992
  - SX-4シリーズの開発背景と概要 NEC技報,Vol48 No11/1995
  - SX-4シリーズのハードウェア構成 NEC技報,Vol48 No11/1995
  - オペレーティングシステム SUPER-UX NEC技報,Vol48 No11/1992
  - SX-4シリーズの言語プロセッサと開発支援ツール、NEC技報,Vol48 No11/1992

## 脚注

## 外部リンク

  - [NECのSXシリーズのページ](http://jpn.nec.com/hpc/sxace/index.html)

[Category:NECのスーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:NECのスーパーコンピュータ "wikilink")

1.  [次世代ベクトル型スーパコンピュータの製品化について ～世界トップクラスの省エネスパコンを目指す～](http://www.nec.co.jp/press/ja/1111/0702.html)
2.  [Hisa Ando、2013年4月26日、Cool Chips 16 - 分散メモリとなるNECの次世代ベクトルスパコン(後編) | マイナビニュース](http://news.mynavi.jp/articles/2013/04/26/coolchips16_ngv_02/) 2014年2月11日閲覧
3.  "Packaging technology for the NEC SX-3/SX-X Supercomputer" () など
4.  [Hisa Ando、2013年12月12日、スパコン最大の学会「SC13」に見る先端技術 (6) SC13 - NECが次世代ベクトル型スパコン「SX-ACE」を発表 | マイナビニュース](http://news.mynavi.jp/column/sc13/006/)
5.  <http://www.hpcwire.jp/archives/1265>
6.  NEC、デジタル産業革命の進展を加速させる新プラットフォーム「SX-Aurora TSUBASA」を発売～AI・ビッグデータ解析領域への利用も拡大～[1](http://jpn.nec.com/press/201710/20171025_01.html)
7.  商標である「[UNIX](../Page/UNIX.md "wikilink")」を名乗るには、2016年現在、[The Open Groupによる認証が必要だが](../Page/The_Open_Group.md "wikilink")、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")を使用している多くのシステムは認証を受けていないことが多く、（公式には）「UNIX」ではないことが多い。
8.
9.  詳しく見れば、この時期の日本の各コンピュータメーカーのスーパーコンピュータのアーキテクチャには、種々の違いがある（ <http://olab.is.s.u-tokyo.ac.jp/~oyanagi/reports/vc-history.txt> の、§2.2 などを参照のこと）