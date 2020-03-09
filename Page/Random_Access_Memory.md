> この記事は[Random Access Memory](https://ja.wikipedia.org/wiki/Random_Access_Memory)から翻訳されています。


[200px](https://ja.wikipedia.org/wiki/ファイル:RAM_n.jpg "wikilink") **Random access memory**（ランダムアクセスメモリ、**RAM**、ラム）とは、[コンピュータ](../Page/コンピュータ.md "wikilink")で使用する[メモリの一分類である](../Page/記憶装置.md "wikilink")。本来は、格納された[データ](https://ja.wikipedia.org/wiki/データ "wikilink")に任意の順序でアクセスできる（[ランダムアクセス](https://ja.wikipedia.org/wiki/ランダムアクセス "wikilink")）メモリといった意味で、かなりの粗粒度で「端から順番に」からしかデータを読み書きできない「シーケンシャルアクセスメモリ」と対比した意味を持つ語であった。しかし本来の意味からズレて、[ROM](../Page/Read_only_memory.md "wikilink")（読み出し専用メモリ）に対して、任意に\[1\]書き込みできるメモリの意で使われていることが専らである。

## 概説

本来の「ランダムアクセス・メモリ」とは、任意のアドレスの記憶素子に対して随時、アクセスパターンに依存した待ち時間などを要することなく、読み出しや書き込みといった操作ができるメモリを指す語である。[磁気テープ](https://ja.wikipedia.org/wiki/磁気テープ "wikilink")のように記憶情報が順番に格納されていて所要の番地への操作を行なうには順番待ちをしなければならないメモリを指す「[シーケンシャルアクセス](https://ja.wikipedia.org/wiki/シーケンシャルアクセス "wikilink")・メモリ」に対比した語であって、RAMという言葉には読み書き(Read/Write)可能という意味は（本来は）ない。

読み書き(Read/Write)可能という意味ではRWM（Read write memory）という表現がある。しかし実際上はほとんど全く使われていない。

### DRAMとSRAM（と、その他）

厳密にはこれらも、半導体チップによるものだけを指す語ではないが、ここでは専ら半導体チップによるものについて述べる。

半導体DRAMは、記憶データを[コンデンサ](https://ja.wikipedia.org/wiki/コンデンサ "wikilink")（キャパシタ）の[電荷](https://ja.wikipedia.org/wiki/電荷 "wikilink")として蓄えているため、一定時間経つと自然放電によりデータが消えてしまう。そのため、定期的に情報を読み出し、再度書き込みをする必要がある。この動作を「リフレッシュ」といい、記憶を保持するためには1秒間に数十回の頻度で繰り返しリフレッシュを行う必要がある。一般にそのようなメモリをダイナミックメモリといい\[2\]、ダイナミックなRAMということでDRAMと呼ばれている。DRAMは、アドレスを指定してからデータを読み出すまでの時間がSRAMよりも若干遅いものの、記憶部の構造が単純であるため、容量あたりのコストが低いという特徴がある。また、常にリフレッシュを行っているため、消費電力が大きい。DRAMのアクセス方式によってさまざまな種類のものが市販されている。

半導体SRAMは、記憶部に[フリップフロップ](https://ja.wikipedia.org/wiki/フリップフロップ "wikilink")を用いており、リフレッシュ動作を必要としない。また、DRAMより高速動作させることができるが、記憶部の回路が複雑になるため、容量あたりのコストが高い。リフレッシュ動作を必要としないため、リフレッシュ動作による電力の消費が無い。

半導体DRAMも半導体SRAMも[揮発性メモリ](https://ja.wikipedia.org/wiki/揮発性メモリ "wikilink")である。揮発性でないメモリとして、[不揮発性メモリ](https://ja.wikipedia.org/wiki/不揮発性メモリ "wikilink")がある。

## 歴史

最初期（1940年代）の電子計算機の時点で、当時の主力素子である[真空管](https://ja.wikipedia.org/wiki/真空管 "wikilink")で1ビット1ビットメモリを作っていたのでは高価につきすぎることから、いくつかの[記憶装置](../Page/記憶装置.md "wikilink")に特化した素子や機器が考案された。[アタナソフ&ベリー・コンピュータ](https://ja.wikipedia.org/wiki/アタナソフ&ベリー・コンピュータ "wikilink")ではリフレッシュ操作を機械的に行う、キャパシタによる一種のDRAMのような装置が考案された。1949年に稼働した[EDSAC](https://ja.wikipedia.org/wiki/EDSAC "wikilink")で使われた水銀[遅延記憶装置](https://ja.wikipedia.org/wiki/遅延記憶装置 "wikilink")などの信号の遅延を利用するものは、原理上シーケンシャルアクセスである。EDSACは初の「実用的な」[プログラム内蔵方式](https://ja.wikipedia.org/wiki/プログラム内蔵方式 "wikilink")のコンピュータだとされているが、プログラム内蔵方式の実用性のためにはある程度多くのメモリが必要であり（EDSACでは1024短語）、水銀遅延記憶装置は同機の成功の重要な要素であった。当時の他の素子では、ブラウン管面の帯電を利用する[ウィリアムス管](https://ja.wikipedia.org/wiki/ウィリアムス管 "wikilink")は、ランダムアクセスでリフレッシュを必要とするなどDRAMに近い性格を持つ。

以降には「ランダムアクセス」メモリに関する話題は特に無い。

その後、1949年から1952年に[磁気](https://ja.wikipedia.org/wiki/磁気 "wikilink")コアを用いた[磁気コアメモリ](https://ja.wikipedia.org/wiki/磁気コアメモリ "wikilink")が開発された。コアメモリでは、格子状に配置した磁気コアと呼ばれるリング状の磁性体に、縦と横方向から電線を貫いた構造をしていた。磁気コアメモリは、[集積回路](../Page/集積回路.md "wikilink")による[半導体メモリ](https://ja.wikipedia.org/wiki/半導体メモリ "wikilink")が登場する1960年代末から1970年代初頭まで、広く使われていた。特には、[放射線](https://ja.wikipedia.org/wiki/放射線 "wikilink")などの影響を受けにくいという特性から、宇宙機用などでは1980年代でも用いられていた例がある\[3\]。また、破壊読み出しなので読み出したら書き戻す必要がある一方、ドーナツ状のフェライトコアの磁性を利用しているため不揮発という特性がある。

[21世紀](../Page/21世紀.md "wikilink")の現在では、コンピュータの[主記憶装置](../Page/主記憶装置.md "wikilink")は、すべて[DRAMになっている](https://ja.wikipedia.org/wiki/Dynamic_Random_Access_Memory "wikilink")。原理的に[SRAMは容量あたりの単価が高くならざるをえないため](https://ja.wikipedia.org/wiki/Static_Random_Access_Memory "wikilink")、（何らかのブレークスルーがないかぎり）主記憶装置をSRAMで構成するようになるとは考えられていない。いっぽうで、何らかの[不揮発性メモリ](https://ja.wikipedia.org/wiki/不揮発性メモリ "wikilink")がDRAMを置き換える可能性はあるものと考えられており、研究開発がおこなわれている。例えば、[カーボンナノチューブ](https://ja.wikipedia.org/wiki/カーボンナノチューブ "wikilink")を使ったもの\[4\]や、[トンネル磁気抵抗効果](https://ja.wikipedia.org/wiki/トンネル磁気抵抗効果 "wikilink")を使った[MRAMがある](https://ja.wikipedia.org/wiki/磁気抵抗メモリ "wikilink")。また、2004年には、[インフィニオン・テクノロジーズ](https://ja.wikipedia.org/wiki/インフィニオン・テクノロジーズ "wikilink")が16[MiBのMRAM試作品を公開した](https://ja.wikipedia.org/wiki/メビバイト "wikilink")。現在開発が進んでいる第二世代の技術は、[Thermal Assisted Switching](https://ja.wikipedia.org/wiki/:en:Thermal_Assisted_Switching "wikilink") (TAS) 方式\[5\]と [Spin Torque Transfer](https://ja.wikipedia.org/wiki/:en:Spin_Torque_Transfer "wikilink") (STT) 方式がある。前者はベンチャー企業が単独で開発しているが、後者は[IBM](../Page/IBM.md "wikilink")などを含め複数の企業が開発に乗り出している\[6\]。ただし、これらが今後の主流となるかどうかは、まだ不透明である。

主記憶装置において、アクセススピードや容量あたりコストと並んで重要なのは、消費電力である。過去の[組み込みシステム](../Page/組み込みシステム.md "wikilink")においては、消費電力を抑えるために[SRAMが用いられていたが](https://ja.wikipedia.org/wiki/Static_Random_Access_Memory "wikilink")、近年では低消費電力に特化したDRAMが使われている。例えば、[サーバファーム](https://ja.wikipedia.org/wiki/サーバファーム "wikilink")などでは、高速性よりも消費電力を抑えることに重点を置いた、"EcoRAM" と呼ばれるRAMも登場している\[7\]\[8\]。

## RAMの種類

  - [SRAM](https://ja.wikipedia.org/wiki/Static_Random_Access_Memory "wikilink") (Static RAM)
  - [DRAM](https://ja.wikipedia.org/wiki/Dynamic_Random_Access_Memory "wikilink") (Dynamic RAM)
      - [FPM DRAM](https://ja.wikipedia.org/wiki/FPM_DRAM "wikilink") (First Page Mode DRAM)
      - [EDO DRAM](https://ja.wikipedia.org/wiki/EDO_DRAM "wikilink") (Extended Data Out DRAM)
      - [SDRAM](https://ja.wikipedia.org/wiki/SDRAM "wikilink") (Synchronous DRAM)
          - [DDR SDRAM](https://ja.wikipedia.org/wiki/DDR_SDRAM "wikilink") (Double Data Rate SDRAM)
          - [DDR2 SDRAM](https://ja.wikipedia.org/wiki/DDR2_SDRAM "wikilink")
          - [DDR3 SDRAM](https://ja.wikipedia.org/wiki/DDR3_SDRAM "wikilink")
          - [DDR4 SDRAM](https://ja.wikipedia.org/wiki/DDR4_SDRAM "wikilink")
          - [DDR5 SDRAM](https://ja.wikipedia.org/wiki/DDR5_SDRAM "wikilink")
          - [GDDR3](https://ja.wikipedia.org/wiki/GDDR3 "wikilink")
          - [GDDR4](https://ja.wikipedia.org/wiki/GDDR4 "wikilink")
          - [GDDR5](https://ja.wikipedia.org/wiki/GDDR5 "wikilink")
          - [GDDR6](https://ja.wikipedia.org/wiki/GDDR6_SDRAM "wikilink")
      - [RDRAM](https://ja.wikipedia.org/wiki/RDRAM "wikilink") (Rambus DRAM)
          - [DRDRAM](https://ja.wikipedia.org/wiki/DRDRAM "wikilink") (Direct RDRAM)
  - [擬似SRAM](https://ja.wikipedia.org/wiki/擬似SRAM "wikilink")
  - [FeRAM](https://ja.wikipedia.org/wiki/FeRAM "wikilink") (Ferroelectric RAM)
  - [MRAM](https://ja.wikipedia.org/wiki/Magnetoresistive_Random_Access_Memory "wikilink") (Magnetoresistive RAM)
  - [ReRAM](https://ja.wikipedia.org/wiki/ReRAM "wikilink") (Resistive RAM)
  - [PRAM](https://ja.wikipedia.org/wiki/PRAM "wikilink") (Phase change RAM)

## メモリの階層

理論的にはRandom Access Machine（理論の文脈では、RAMという略語はこちらのこともある）といって、全てのメモリに一定時間でランダムアクセスできるような機械のモデルなどもあるが、現実のコンピュータでは一般に「早くて小さい」メモリと「遅くて大きい」メモリを組み合わせて使う。

多くのコンピュータシステムは、[レジスタを頂点として](https://ja.wikipedia.org/wiki/レジスタ_\(コンピュータ\) "wikilink")、[マイクロプロセッサ](https://ja.wikipedia.org/wiki/マイクロプロセッサ "wikilink")チップ上の[SRAMキャッシュ](https://ja.wikipedia.org/wiki/Static_Random_Access_Memory "wikilink")、外部[キャッシュメモリ](https://ja.wikipedia.org/wiki/キャッシュメモリ "wikilink")、[主記憶装置](../Page/主記憶装置.md "wikilink")、[補助記憶装置](../Page/補助記憶装置.md "wikilink")等々といったようなメモリ階層を持っている。DRAMという階層だけを見てもアクセス時間にはバラつきがあるが、その範囲は回転式の[電子媒体](https://ja.wikipedia.org/wiki/電子媒体 "wikilink")や[磁気テープ](https://ja.wikipedia.org/wiki/磁気テープ "wikilink")ほど大きくはない。メモリ階層を使う目的は、メモリシステム全体のコストを最小化しつつ、平均的なアクセス性能を向上させることにある。一般に、レイテンシ・スループット・アクセス単位といった点で、レジスタが最も高速・細粒度であり、階層を下に行くほど低速・粗粒度となる。

## プロセッサとメモリの速度差

[マイクロプロセッサ](https://ja.wikipedia.org/wiki/マイクロプロセッサ "wikilink")の速度（ここでは、周辺の速度によって待たされることが無かった場合の単位時間あたりのデータ処理量）とその向上に対して、メモリの速度（レイテンシとスループット）とその向上を比較すると、メモリの方が遅いという傾向は、マイクロプロセッサの誕生以来一貫して続いている。最大の問題は、チップとチップの間のデータ転送[帯域幅](https://ja.wikipedia.org/wiki/帯域幅 "wikilink")に限界があることである。1986年から2000年まで、CPUの性能向上は年率平均で55%であったのに対して、メモリの性能向上は年率平均で10%ほどであった。この傾向から、メモリ[レイテンシ](https://ja.wikipedia.org/wiki/レイテンシ "wikilink")がコンピュータ全体の性能において[ボトルネック](https://ja.wikipedia.org/wiki/ボトルネック "wikilink")になるだろうと予想されていた\[9\]。

その後、CPUの性能向上は鈍化した。これには、微細化により性能向上が物理的限界に近づいていることや発熱の問題もあるが、同時にメモリとの速度差を考慮した結果でもある。インテルは、その原因について次のように分析している\[10\]。

> 第一に、チップが微細化しクロック周波数が上がると、個々のトランジスタのリーク電流が増大し、消費電力の増大と発熱量の増大を招く（中略）、第二にクロック高速化による利点はメモリレイテンシによって一部相殺される。つまり、メモリアクセス時間は、クロック周波数の向上に合わせて短縮することができなかった。第三に、これまでの逐次的アーキテクチャでは、ある種のアプリケーションは、プロセッサが高速化したほど性能が向上しなくなっている（[フォン・ノイマン・ボトルネック](https://ja.wikipedia.org/wiki/フォン・ノイマン・ボトルネック "wikilink")）。さらに、集積回路の微細化が進行したことにより、[インダクタンス](https://ja.wikipedia.org/wiki/インダクタンス "wikilink")の付与が難しく、信号伝送における[RC遅延が大きくなる](https://ja.wikipedia.org/wiki/RC回路 "wikilink")。これも周波数向上を阻害するボトルネックの一つである。

信号伝送におけるRC遅延については [Clock Rate versus IPC: The End of the Road for Conventional Microarchitectures](http://www.cs.utexas.edu/users/cart/trips/publications/isca00.pdf) にもあり、2000年から2014年のCPUの性能向上は、最大でも年率平均で12.5%という見積もりが示されていた。インテルのデータを見ても\[11\]、2000年から2004年の間、CPUの速度の向上は鈍化している。

しかし、この見積もりはCPUの性能向上があくまで「クロック周波数の向上によって」高性能化するという前提に立っていた。だが、2004年に [AMDが](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[K8](https://ja.wikipedia.org/wiki/K8 "wikilink")アーキテクチャを発表すると、パイプラインバーストによる処理遅延を抑え単位クロック数あたりの命令実行数を向上することがトレンドとなり、クロック周波数のむやみな向上は止まったが、処理能力の向上はむしろ激化した。さらに、この頃から1つのプロセッサダイに複数の主演算コアを搭載し、さらにそれを仮想的に複数のコアとするスレッディング技術を搭載することが主流となった。AMDの製品では、2005年のAthlon64 X2 3800+ では約7.31GFLOPS相当だったが、2017年のRyzen 7 1800Xでは約42.53GFLOPSにも達しており、これは年率平均にすると約50%程度の性能向上と、2000年以前とさして変わっていない。

## その他

### DVD-RAM

一般にRAMという語は、[主記憶装置](../Page/主記憶装置.md "wikilink")寄りのそれを指し、[補助記憶装置](../Page/補助記憶装置.md "wikilink")寄りのそれは指さないことが多い。しかし、[DVD-RAM](../Page/DVD-RAM.md "wikilink")のような（もっぱら「ROM」の対置語として使われているためによる）例外もある。

### RAMディスク

RAMディスクという語は2通りに使われている。どちらも「論理的には超高速のハードディスクのように見える」という点は共通である。

1種類目は、SCSIなどのインタフェースでアクセスできる、外からはハードディスクのように見える装置だが、内部は(D)RAMで構成されているというもので、バッテリーバックアップ等により記憶が保持できるようにしたものも多いが、そうでないものもある。

2種類目は、オペレーティングシステムのデバイスドライバとして、ユーザーのプログラムからはストレージ（ブロックデバイス）のように見えるが、実際には[メインメモリに確保した領域に記録している](../Page/主記憶装置.md "wikilink")、というもので、当然ながらシャットダウンにより情報は失われる。テンポラリファイル等の置き場等として使われることが意図されている。

### シャドウRAM

ROMの内容をRAMにコピーしてアクセス時間を短縮することがある（ROMは一般に低速である）。コンピュータの電源投入時、メモリを初期化した後、ROMの配置されていたアドレス範囲をコピーしたRAMに切り替える。これをシャドウRAMと呼ぶ。これは[組み込みシステム](../Page/組み込みシステム.md "wikilink")でもよく行われる技法である。

典型例として、パーソナルコンピュータの[BIOSがあり](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")、ファームウェアのなんらかのオプション設定でBIOSをシャドウRAMにコピーして使うことができる（システム内の他のROMをRAMにコピーして使うオプションもある）。それによって性能向上する場合もあるし、非互換問題が発生する場合もある。例えば、ある種のハードウェアはシャドウRAMが使われていると[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")にアクセスできない。また、[ブート](https://ja.wikipedia.org/wiki/ブート "wikilink")後は全くBIOSを使わないシステムなら、性能は向上しない。当然ながらシャドウRAMを使うと、主記憶の空き容量が少なくなる\[12\]。

## 関連項目

  - [デュアルチャネル](https://ja.wikipedia.org/wiki/デュアルチャネル "wikilink")
  - [メモリバス規格](https://ja.wikipedia.org/wiki/デバイス帯域幅の一覧#メモリバス規格_/_RAM "wikilink")
  - [仮想記憶](../Page/仮想記憶.md "wikilink")

## 脚注・出典

## 外部リンク

  - [Memory Prices (1957-2010)](http://www.jcmit.com/memoryprice.htm)

[Category:記憶装置](https://ja.wikipedia.org/wiki/Category:記憶装置 "wikilink") [Category:半導体メモリ](https://ja.wikipedia.org/wiki/Category:半導体メモリ "wikilink") [Category:主記憶装置](https://ja.wikipedia.org/wiki/Category:主記憶装置 "wikilink")

1.  「フラッシュROM」などは逆に、ブロック単位ではあるが書き込みできるのに「ROM」と呼ばれており、やはりネジレがある。
2.  [ウィリアムス管](https://ja.wikipedia.org/wiki/ウィリアムス管 "wikilink")などが、半導体DRAMよりも古くからあるダイナミックメモリである。
3.  『困ります、[ファインマンさん](https://ja.wikipedia.org/wiki/リチャード・P・ファインマン "wikilink")』でスペースシャトルのコンピュータに使われていることが語られているのがよく知られている。
4.  [データを「10億年」保持可能：カーボン・ナノチューブ利用](http://wired.jp/wv/2009/06/03/%E3%83%87%E3%83%BC%E3%82%BF%E3%82%92%E3%80%8C10%E5%84%84%E5%B9%B4%E3%80%8D%E4%BF%9D%E6%8C%81%E5%8F%AF%E8%83%BD%EF%BC%9A%E3%82%AB%E3%83%BC%E3%83%9C%E3%83%B3%E3%83%BB%E3%83%8A%E3%83%8E%E3%83%81%E3%83%A5/) WIRED.jp、2009年6月3日
5.  [The Emergence of Practical MRAM](http://www.crocus-technology.com/pdf/BH%20GSA%20Article.pdf) CROCUS Technology
6.  [Tower invests in Crocus, tips MRAM foundry deal](http://www.eetimes.com/news/latest/showArticle.jhtml?articleID=218000269) EETimes、2009年6月18日
7.  ["EcoRAM held up as less power-hungry option than DRAM for server farms"](http://blogs.zdnet.com/green/?p=1165) by Heather Clancy 2008
8.  [Spansion社が「EcoRAM」の詳細を明らかに、サーバーのメインメモリー用途を狙う](http://ednjapan.cancom-j.com/news/2008/11/4788) EDN Japan、2008年11月
9.  Wm. A. Wulf, Sally A. McKee, [Hitting the Memory Wall: Implications of the Obvious (PDF)](http://www.cs.virginia.edu/papers/Hitting_Memory_Wall-wulf94.pdf). 1994
10. [Platform 2015 documentation (PDF)](http://download.intel.com/technology/computing/archinnov/platform2015/download/RMS.pdf) Intel
11. [Microprocessor Quick Reference Guide](http://www.intel.com/pressroom/kits/quickreffam.htm) Intel
12.