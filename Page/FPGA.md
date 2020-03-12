> この記事は[FPGA](https://ja.wikipedia.org/wiki/FPGA)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Altera_StratixIVGX_FPGA.jpg "wikilink") Stratix IV GX FPGA\]\] **FPGA**（）は、製造後に購入者や設計者が構成を設定できる[集積回路](../Page/集積回路.md "wikilink")であり、広義にはPLD（[プログラマブルロジックデバイス](../Page/プログラマブルロジックデバイス.md "wikilink")）の一種である。現場でプログラム可能な[ゲートアレイ](https://ja.wikipedia.org/wiki/ゲートアレイ "wikilink")であることから、このように呼ばれている。

## 概要

FPGAの構成設定は一般に[ハードウェア記述言語](../Page/ハードウェア記述言語.md "wikilink") (HDL) を使って指定し、その点は[ASIC](../Page/ASIC.md "wikilink")に近い。FPGAはASICで実装できる任意の論理機能を実装できる。出荷後に機能を更新でき、設計面で部分的に再構成でき\[1\]、ASIC設計よりエンジニアリングコストが低い点などが多くの用途で利点となる\[2\]。

FPGAに含まれる[プログラム可能な論理コンポーネントを](../Page/プログラマブルロジックデバイス.md "wikilink")「論理ブロック」などと呼び、それら論理ブロック間を相互接続する再構成可能な配線階層がある。この構成によっていわばワンチップのプログラム可能な[ブレッドボード](../Page/ブレッドボード.md "wikilink")の役目を果たす。論理ブロックを組み合わせて複雑な論理回路を構成することもできるし、単に[ANDゲート](https://ja.wikipedia.org/wiki/ANDゲート "wikilink")や[XORゲート](https://ja.wikipedia.org/wiki/XORゲート "wikilink")のような単純な[論理回路](https://ja.wikipedia.org/wiki/論理回路 "wikilink")を構成することもできる。多くのFPGAでは、論理ブロックにメモリ要素も含んでおり、単純な[フリップフロップ](../Page/フリップフロップ.md "wikilink")またはより完全なメモリブロックで構成されている\[3\]。

デジタル回路機能に加え、一部のFPGAはアナログ回路要素も持っている。最も典型的なアナログ機能としては、スルーレートや出力ピンの駆動強度などを設定できるものが多く、負荷の小さいピンのスルーレートを遅くすることでオーバーシュートを防いだり、負荷の大きいピンのスルーレートを速くすることで転送レートを高速化する\[4\]\[5\]。もう1つのよくあるアナログ機能としては、入力ピンに付属した差動コンパレータがあり、[差動信号](https://ja.wikipedia.org/wiki/差動信号 "wikilink")チャンネルに接続するよう設計されている。さらに、[ADCと](../Page/アナログ-デジタル変換回路.md "wikilink")[DAC](../Page/デジタル-アナログ変換回路.md "wikilink")、アナログ信号処理ブロックまで搭載し、[システム・オン・チップ](https://ja.wikipedia.org/wiki/システム・オン・チップ "wikilink")を構成できるよう意図されたFPGA（ミクスド・シグナルFPGA）もある\[6\]。全体がアナログ回路でFPGAのように配線を再構成可能な[FPAA](https://ja.wikipedia.org/wiki/FPAA "wikilink")\[7\]もあり、ミクスド・シグナルFPGAはFPGAとFPAAの中間的存在である。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Altium_NanoBoard_3000_AB.JPG "wikilink")

## 歴史

FPGA業界は[PROM](../Page/PROM.md "wikilink")とPLD（プログラマブルロジックデバイス）から発展した。PROMもPLDも出荷後に顧客企業の工場でまとめてプログラムできるが、プログラム可能なロジックは論理ゲート間に固定の配線を行うものだった\[8\]。

プログラム可能なロジックアレイ、論理ゲート、論理ブロックといった基本概念は1985年、David W. PageとLuVerne R. Petersonの取得した特許に既に見られる\[9\]\[10\]。

[ザイリンクス](../Page/ザイリンクス.md "wikilink")の共同創業者ロス・フリーマンとベルナルド・フォンデルシュミットは1985年、世界初のFPGA XC2064を製品化した\[11\]。XC2064はプログラム可能な論理ゲートとプログラム可能な配線を持っていた。これにより、新たなテクノロジーとその市場が始まった\[12\]。XC2064は64個の構成可能論理ブロック (CLB) で構成され、それぞれのCLBには3入力ルックアップテーブル (LUT) があった\[13\]。その二十数年後、Freemanは発明者殿堂入りを果たした\[14\]。

1980年代後半、[アメリカ海軍](../Page/アメリカ海軍.md "wikilink")が60万個の再プログラム可能な論理ゲートでコンピュータを構成するというスティーブ・キャセルマンの提案した実験に資金提供した。キャセルマンはこの開発に成功し、1992年に関連特許を取得した\[15\]。

ザイリンクスは1985年から1990年代中ごろまで急激に発展したが、そのころから競合企業が急成長し、市場シェアを浸食し始めた。1993年には（現Microsemi）のシェアが18%にまで増大した\[16\]。

1990年代、FPGAは微細化と生産量の両面で大きく発展した。1990年代初め、FPGAは主に通信業やネットワークに使われていた。90年代末にはコンシューマ市場、自動車、産業用途にまで使われるようになっていた\[17\]。

1997年、サセックス大学の研究者エイドリアン・トンプソンが[遺伝的アルゴリズム](../Page/遺伝的アルゴリズム.md "wikilink")とFPGAを組み合わせた[音声認識](../Page/音声認識.md "wikilink")装置を開発し、FPGAに注目が集まった。トンプソンは、ザイリンクス製の10×10セルのFPGAのアナログ機能を利用して、2つの音を識別できるよう学習するハードウェアを開発したものである。このような遺伝的アルゴリズムをFPGAのようなデバイスの構成に使う方式は、[進化型ハードウェア](https://ja.wikipedia.org/wiki/進化型ハードウェア "wikilink")と呼ばれるようになっている\[18\]\[19\]。

### 最近の発展

最近では、FPGAに[CPUコアや関連する周辺回路を組み込み](../Page/マイクロプロセッサ.md "wikilink")、完全な「プログラム可能なチップ上のシステム」を実現する製品も登場している。例えば、ザイリンクスは[PowerPC](../Page/PowerPC.md "wikilink")プロセッサを組み込んだFPGAとしてVirtex-II PROおよびVirtex-4を発売している。Atmel FPSLICも同様の製品で、[Atmel AVRプロセッサを組み込んでいる](../Page/Atmel_AVR.md "wikilink")。アクテルのSmartFusionは[ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")のCortex-M3のCPUコアを組み込んでいる。

これとは別の流れとして、[ソフトプロセッサ](../Page/ソフトプロセッサ.md "wikilink")コアをFPGA上に構成して利用する方式もある。

現在のFPGAの多くは動作中にも再構成可能であり、そこから[再構成可能コンピューティング](https://ja.wikipedia.org/wiki/再構成可能コンピューティング "wikilink")という考え方も生まれた。これはシステムがそのとき実行しようとしているタスクの傾向に沿って自らを再構成するという考え方である。例えば、ミトリオニクス社の「ミトリオン・バーチャル・プロセッサー」\[20\]はFPGA上に実装された再構成可能なソフトプロセッサである。ただし、これは実行中の動的再構成はできない。

FPGAとも異なる新たなアーキテクチャも登場しつつある。Stretch S5000はソフトウェアから構成可能な[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")で、CPUコアのアレイとFPGA風のプログラム可能なコアを同じチップに搭載している\[21\]。

### ゲート数

  - 1987年: 9,000ゲート、ザイリンクス\[22\]
  - 1992年: 600,000ゲート、Naval Surface Warfare Department\[23\]
  - 2000年代初頭: 数百万ゲート\[24\]

### 市場規模

  - 1985年: 世界初の商用FPGAが開発された（ザイリンクス）\[25\]
  - 1987年: 1400万ドル\[26\]
  - 1993年ごろ: 3億8500万ドル以上\[27\]
  - 2005年: 19億ドル\[28\]
  - 2010年: 40億ドル\[29\]
  - 2020年: 85億ドル（予想）\[30\]

### FPGAを使った設計件数

  - 10,000\[31\]
  - 2005年: 80,000\[32\]
  - 2008年: 90,000\[33\]

## FPGAの比較

従来、FPGAは[ASIC](../Page/ASIC.md "wikilink")に比べて低速でエネルギー効率が悪く、実装可能な機能も限られていた。しかし、大量生産、製造ルールの微細化、研究開発などにより、ASICとFPGAの性能差はかなり縮まっている\[34\]。

[thumb](https://ja.wikipedia.org/wiki/ファイル:알테라_사이클론2_FPGA.jpg "wikilink") Cyclone II FPGA\]\]

バグ修正が現場で可能な点、開発・製造期間が短くて済む点などが利点である。また、設計段階ではFPGAを使い、最終的に設計が確定したらASICなどに移行して生産するという手法も可能である。

ザイリンクスは最近ではこのFPGAとASICの関係が一部市場で変化してきたと主張している\[35\]。

  - [集積回路](../Page/集積回路.md "wikilink")のコストが占める割合はどんどん上昇している。
  - ASICは開発期間とコストを押し上げる要因となっていた。
  - [研究開発](../Page/研究開発.md "wikilink")部門の人材は減ってきている。
  - 市場の変化が激しくなり、タイムリーな製品投入ができないと利益が上がらなくなってきた。
  - 経済状況が悪化し、低コストのテクノロジーが重視されるようになってきた。

これらの傾向から、大量生産ならASICという観念が通用しなくなり、FPGAを採用することが多くなってきた\[36\]。

一部のFPGAは一部が動作中に残りの部分を再構成できる[動的再構成](https://ja.wikipedia.org/wiki/動的再構成 "wikilink")の機能を持っている。

### CPLDとの比較

[CPLD](../Page/CPLD.md "wikilink")とFPGAの大きな違いはアーキテクチャである。CPLDの方が構成の自由度が小さいが、遅延時間が予測しやすく、チップ面積における相互接続用経路の比率も小さい。FPGAは逆に相互接続の方が支配的で、それゆえに柔軟性が高い。

また、FPGAの方が組み込まれている機能が高度でメモリも埋め込まれており、デコーダや数学関数の演算を実装した論理ブロックもある。

### セキュリティ

セキュリティの観点ではFPGAにはASICや通常のマイクロプロセッサと比べて長所と短所がある。装置の製造（組み立て）段階で悪意ある細工をしようとしても、FPGAではそれが具体的にどう動作するのかハードウェアを見ただけではわからず、そのようなリスクが低くなる\[37\]。一方で、コンフィギュレーションをロードする際に傍受される危険性があるため、ビットストリームの暗号化をサポートするFPGAもある。

## 用途

FPGAの用途としては、[デジタル信号処理](../Page/デジタル信号処理.md "wikilink")、[ソフトウェア無線](../Page/ソフトウェア無線.md "wikilink")、[アビオニクス](../Page/アビオニクス.md "wikilink")、[ASIC](../Page/ASIC.md "wikilink")の[プロトタイピング](../Page/プロトタイピング.md "wikilink")、[医用画像処理](../Page/医用画像処理.md "wikilink")、[コンピュータビジョン](../Page/コンピュータビジョン.md "wikilink")、[音声認識](../Page/音声認識.md "wikilink")、[暗号](../Page/暗号.md "wikilink")、[バイオインフォマティクス](../Page/バイオインフォマティクス.md "wikilink")、コンピュータハードウェアの[エミュレータ](../Page/エミュレータ.md "wikilink")、[電波天文学](../Page/電波天文学.md "wikilink")、金属探知機など多岐にわたる。

FPGAは本来CPLDと競合するものとして、[プリント基板](../Page/プリント基板.md "wikilink")上の[グルー・ロジック](../Page/グルー・ロジック.md "wikilink")を対象としていた。その後、規模や機能や性能が向上するにつれ、扱う機能範囲が拡大していき、システム・オン・チップとしてマーケティングされるまでになった。特に1990年代後半にFPGAに独立した[乗算器](../Page/乗算器.md "wikilink")が組み込まれると、それまで[DSPが扱っていた分野にまでFPGAが採用されるようになっていった](../Page/デジタルシグナルプロセッサ.md "wikilink")\[38\]\[39\]。

FPGAは特に高い並列性が期待できる分野やアルゴリズムの実装で威力を発揮する。例えば[暗号解読](../Page/暗号解読.md "wikilink")がその典型例で、[総当り攻撃](https://ja.wikipedia.org/wiki/総当り攻撃 "wikilink")の実装にはFPGAが適している。

[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")や[動画](../Page/動画.md "wikilink")の圧縮、伸張、[画像処理](../Page/画像処理.md "wikilink")、[ニューラルネットワーク](../Page/ニューラルネットワーク.md "wikilink")処理などのロジックをチップ内部に持てるようになり、特定の用途の処理を高効率かつ高速化が可能になる\[40\]。一例としてマイクロプロセッサーとFPGAで電力当たりの性能を比較した場合、検索処理では約10倍、複雑な金融モデルの解析では実に約25倍もFPGAの方が性能が高いとされる\[41\]。

FPGAは[高性能計算](../Page/高性能計算.md "wikilink")用途にも採用されつつあり、[高速フーリエ変換](../Page/高速フーリエ変換.md "wikilink")や[畳み込み](https://ja.wikipedia.org/wiki/畳み込み "wikilink")といった演算を[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")とソフトウェアの代わりにFPGAで実装するといった使い方がなされている。

FPGAの論理リソースは本質的に並列動作可能であるため、クロック周波数が低くても計算時間を大幅に短縮できる可能性がある。またFPGAの柔軟性を利用すれば、演算精度と同時に動作する演算ユニット数のトレードオフにより、さらに高い演算性能を達成できる。ここから時間のかかる計算をソフトウェアからFPGAに肩代わりさせるという考え方が生まれ、[再構成可能コンピューティング](https://ja.wikipedia.org/wiki/再構成可能コンピューティング "wikilink")と呼ばれるようになった。

ソフトウェアに比べてFPGAの構成の設計は複雑で時間がかかることから、高性能計算におけるFPGAの採用は限定的なものとなっている。

従来からFPGAは生産量の少ない特定分野向け用途で使われてきた。生産量が少ない場合、ASICよりもFPGAの方がコストが低くなる。近年はこの境目が変化しつつあり、FPGAの方がコストと性能の面でASICよりも優れているという範囲が広がってきている。

並列計算でない用途としては、異なる信号規格どうしの回路信号の変換器としての用途もある\[42\]。

## アーキテクチャ

[thumb](https://ja.wikipedia.org/wiki/ファイル:Fpga_structure.svg "wikilink") 典型的なFPGAのアーキテクチャは\[43\]、論理ブロックの配列（Configurable Logic Block, CLB あるいは Logic Array Block, LAB などメーカーによって正式呼称は異なる）、I/Oパッド、配線用チャンネルから構成される。一般に配線用チャンネルは全て同じ幅（導線の本数）で、複数のI/Oパッドが論理ブロックの1行の幅または1列の高さに対応するようになっている。

アプリケーション回路は適正なリソースを用いてFPGA内に配置される。設計から必要な論理ブロック数やI/O数は容易に決定できるが、使用する論理ゲート数が同じであっても設計によって配線量は大きく異なる。例えば同じ論理ゲート数でも、[クロスバースイッチ](https://ja.wikipedia.org/wiki/クロスバースイッチ "wikilink")は[シストリックアレイ](https://ja.wikipedia.org/wiki/シストリックアレイ "wikilink")よりも多くの配線が必要である。使われない配線が多いと、性能も低下するし未使用部分が増えてしまうため、FPGA製造業者は論理ブロック数やI/O数にちょうど見合った配線を用意するよう最適化を心がけている。この配分を決定するために[Rent's ruleを使ったり](https://ja.wikipedia.org/wiki/:en:Rent's_rule "wikilink")、既存の回路設計で実験したりしている。

一般に論理ブロックはいくつかの論理セル（ALM、LE、スライスなどと呼ぶ）で構成される。典型的な論理セルは下図にあるように、4入力[ルックアップテーブル](../Page/ルックアップテーブル.md "wikilink") (LUT)、1つの[全加算器](../Page/加算器.md "wikilink") (FA)、D型[フリップフロップ](../Page/フリップフロップ.md "wikilink")などから構成される。この図ではLUTは2つの3入力LUTで構成されている。通常モードでは、左の[マルチプレクサ](../Page/マルチプレクサ.md "wikilink") (mux) を通して4入力LUTを構成している。演算モードでは、LUTの出力がFAに入力される。モード選択は中央のmuxでプログラムされる。出力は同期/非同期を選択でき、図では左端のmuxのプログラムで選択できる。実際にはスペースを節約するため、FAの機能の一部または全部をLUTに組み込むこともある\[44\]\[45\]\[46\]。

[400px](https://ja.wikipedia.org/wiki/ファイル:FPGA_cell_example.png "wikilink")

この図のような論理セルを2つまたは4つでALMやスライスを構成し、入力を共有させる。

論理ブロックは一般にALM/LE/スライス数個で構成される。

最近では高性能FPGAに6入力LUTを採用する例がある\[47\]。

クロック信号（および高[ファンアウト](https://ja.wikipedia.org/wiki/ファンアウト "wikilink")出力信号など）は、商用FPGAでは通常とは異なる配線でルーティングされ、通常の信号とは別に管理される。

上の例での論理ブロックのピン配置の例を次の図に示す。 [frame](https://ja.wikipedia.org/wiki/ファイル:logic_block_pins.svg "wikilink")

入力が論理ブロックの4つの面にひとつずつあるのに対して、出力は右と下の2箇所で配線と繋ぐことができる。配線は複数本並んでいて、出力はそれらの任意の線に接続可能である。同じことはI/Oパッドにも言える。チップ上端のI/Oパッドは上端に隣接するW本の配線のいずれとも接続可能である。

一般にFPGAの配線は分割されていない。すなわち、配線セグメントは論理ブロック1つぶんをまたぐ長さで縦の配線と横の配線が交差するスイッチボックスとスイッチボックスの間を走っている。そして、スイッチボックス内のプログラム可能なスイッチをオンにすることでさらに配線が続くことになり、そのようにして長い配線を構築する。高速化のために複数の論理ブロックをまたぐような長い配線を最初から用意しているFPGAアーキテクチャもある。

垂直な配線と水平な配線が交差する箇所にスイッチボックスがある。下の図では、水平と垂直にそれぞれ3本の線があり、その交点3カ所にプログラム可能なスイッチ群がある。交点すべてにスイッチを配するとコストがかかり遅延も大きくなるため、このように斜めの交点にだけスイッチを配するのが一般的である。どの交点にスイッチを配するかはいくつか方式がある。1つの交点には6つのプログラム可能なスイッチがある。

[frame](https://ja.wikipedia.org/wiki/ファイル:switch_box.svg "wikilink")

最近のFPGAはこれにさらに高機能な論理ブロックを加えるなどしている。高機能ブロックを埋め込むことで、一からその機能を構成するよりも必要な面積を削減でき、かつ性能が向上する。例えば、[乗算器](../Page/乗算器.md "wikilink")、汎用[DSPブロック](../Page/デジタルシグナルプロセッサ.md "wikilink")、汎用[CPU](../Page/CPU.md "wikilink")コア、高速I/Oロジック、メモリなどが埋め込まれたFPGAがある。

## FPGAの設計とプログラミング

FPGAの動作を定義するには、ユーザーが[ハードウェア記述言語](../Page/ハードウェア記述言語.md "wikilink") (HDL) または回路図で設計を提供する。大規模な場合は回路図よりもHDL方式の方が適している。しかし、回路図の方が設計の視覚化が容易で事前に確認しやすい場合もある。

HDLで記述した設計を[EDAツールに入力し](../Page/EDA_\(半導体\).md "wikilink")、[ネットリスト](https://ja.wikipedia.org/wiki/ネットリスト "wikilink")を生成する。ネットリストを実際のFPGAアーキテクチャに対応させるため、そのFPGAのメーカーが提供している[place-and-routeと呼ばれるソフトウェアを使用する](https://ja.wikipedia.org/wiki/:en:Place_and_route "wikilink")。ユーザーはその結果をシミュレータにかけるなどして、タイミングに問題がないかなどを検証する。設計と検証が終わったら、バイナリファイルを生成し（この工程もFPGAメーカーの独自ソフトウェアを使う）、FPGAの（再）構成に使う。バイナリファイルは[シリアル通信](https://ja.wikipedia.org/wiki/シリアル通信 "wikilink") ([JTAG](../Page/JTAG.md "wikilink")) 経由でFPGAに転送するか、[EEPROM](../Page/EEPROM.md "wikilink")などの外部メモリデバイスに格納する。

最も一般的なHDLとしては[VHDL](../Page/VHDL.md "wikilink")と[Verilog](../Page/Verilog.md "wikilink")があるが、これらは通常のプログラミング言語で言えば抽象度が[C言語](../Page/C言語.md "wikilink")を少し下回る程度であり、手間がかかる。そこでもっと高い抽象度でハードウェア設計を行う[言語を導入する動きもある](https://ja.wikipedia.org/wiki/ハードウェア記述言語#システムレベル設計 "wikilink")。

FPGAにおける複雑なシステムの設計を単純化するため、検証・最適化済みの既存の機能ブロックや回路をライブラリ化して利用する。このような既存の回路を[IPコア](../Page/IPコア.md "wikilink")と呼び、FPGAベンダーやサードパーティのIP業者から購入できる（一般に無償ではない）。他にも[OpenCoresといった開発者コミュニティなどでフリーなものが入手できる](https://ja.wikipedia.org/wiki/:en:OpenCores "wikilink")。

FPGAアプリケーションを開発する場合、設計の各段階でシミュレーションによる検証を行う。まず[VHDL](../Page/VHDL.md "wikilink")や[Verilog](../Page/Verilog.md "wikilink")の[RTL記述でシミュレーションを行う](../Page/レジスタ転送レベル.md "wikilink")。次に[論理合成](../Page/論理合成.md "wikilink")によって出力されたネットリスト、ネットリストを変換したゲートレベル記述でもシミュレーションによる検証を行う。そこからさらにFPGA向けに配置を決定すると配線による遅延が加わるため、再度シミュレーションによる検証が必要になる。

## 基本プロセス技術の種類

  - [SRAM](../Page/Static_Random_Access_Memory.md "wikilink") - システム内で再プログラム可能。外部ブートデバイスが必要。[CMOS](../Page/CMOS.md "wikilink")。
  - [アンチヒューズ](https://ja.wikipedia.org/wiki/アンチヒューズ "wikilink")型 - 一度だけプログラム可能。CMOS。
  - [PROM](../Page/PROM.md "wikilink") - 一度だけプログラム可能。
  - [EPROM](../Page/EPROM.md "wikilink") - 一度だけプログラム可能。ただし窓付きであれば紫外線照射で消去できる。CMOS。
  - [EEPROM](../Page/EEPROM.md "wikilink") - 消去可能。一部にはシステム内でプログラム可能なものもある。CMOS。
  - [フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink") - 消去可能。一部にはシステム内でプログラム可能なものもある。一般にフラッシュセルの方がEEPROMセルより小さく、製造コストが小さい。CMOS。
  - [ヒューズ型](../Page/電力ヒューズ.md "wikilink") - 一度だけプログラム可能。バイポーラ。

## 主なメーカー

FPGA市場を主導しているのは[ザイリンクス](../Page/ザイリンクス.md "wikilink")と[アルテラ](../Page/アルテラ.md "wikilink")で、両社は長年のライバル関係にある。両社のシェアを併せると市場の80%を占め\[48\]、2009年まではザイリンクス単独で50%程度占めていた。2012年にはアルテラがザイリンクスに売上高で肩を並べるとの予想もある\[49\]。2010年にアルテラが急成長し、売り上げが12億米ドルから20億米ドルへと急成長した\[50\]。

ザイリンクスもアルテラも[Windowsおよび](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Linux](../Page/Linux.md "wikilink")で動作する設計用ソフトウェアを無料で提供している\[51\]\[52\]。

なお、アルテラについては 2015年6月1日 に[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")による買収が発表された。\[53\]

他に以下のような企業がFPGAを開発・製造している。

  - [ラティスセミコンダクター](https://ja.wikipedia.org/wiki/ラティスセミコンダクター "wikilink")

  -
  - [クイックロジック](https://ja.wikipedia.org/wiki/クイックロジック "wikilink") (QuickLogic)

  -
## 関連項目

  - [ゲートアレイ](https://ja.wikipedia.org/wiki/ゲートアレイ "wikilink")
  - [ASIC](../Page/ASIC.md "wikilink")
  - [CPLD](../Page/CPLD.md "wikilink")
  - [ソフトプロセッサ](../Page/ソフトプロセッサ.md "wikilink")
  - [VHDL](../Page/VHDL.md "wikilink")
  - [Verilog](../Page/Verilog.md "wikilink")
  - [再構成可能コンピューティング](https://ja.wikipedia.org/wiki/再構成可能コンピューティング "wikilink")
  - [SystemC](../Page/SystemC.md "wikilink")

## 脚注・出典

## 外部リンク

  - [University of North Carolina at Charlotte's Reconfigurable Computing Laboratory](http://www.rcs.uncc.edu/wiki)

[fr:Circuit logique programmable\#FPGA](https://ja.wikipedia.org/wiki/fr:Circuit_logique_programmable#FPGA "wikilink")

[Category:集積回路](https://ja.wikipedia.org/wiki/Category:集積回路 "wikilink") [Category:デジタル回路](https://ja.wikipedia.org/wiki/Category:デジタル回路 "wikilink") [Category:頭字語](https://ja.wikipedia.org/wiki/Category:頭字語 "wikilink")

1.
2.  [FPGA Architecture for the Challenge](http://www.eecg.toronto.edu/~vaughn/challenge/fpga_arch.html)
3.
4.  [FPGA Signal Integrity tutorial](http://wiki.altium.com/display/ADOH/FPGA+SI+Tutorial+-+Simulating+the+Reflection+Characteristics)
5.  [NASA: FPGA drive strength](http://klabs.org/richcontent/fpga_content/DesignNotes/signal_quality/actel_drive_strength/index.htm)
6.  Mike Thompson. [Mixed-signal FPGAs provide GREEN POWER](http://www.eetimes.com/showArticle.jhtml?articleID=200000777). EE Times, 2007-07-02.
7.
8.  [History of FPGAs](http://filebox.vt.edu/users/tmagin/history.htm)
9.  Google Patent Search, "[Re-programmable PLA](http://www.google.com/patents?id=BB4vAAAAEBAJ&dq=4508977)". Retrieved February 5, 2009.
10. Google Patent Search, "[Dynamic data re-programmable PLA](http://www.google.com/patents?id=1-gzAAAAEBAJ&dq=4524430)". Retrieved February 5, 2009.
11. Peter Clarke, EE Times "[Xilinx, ASIC Vendors Talk Licensing](http://www.eetimes.com/electronics-news/4102293/Xilinx-ASIC-vendors-talk-licensing)" June 22, 2001. Retrieved February 10, 2009.
12. Funding Universe. “[Xilinx, Inc.](http://www.fundinguniverse.com/company-histories/Xilinx-Inc-Company-History.html)” Retrieved January 15, 2009.
13. Clive Maxfield, Programmable Logic DesignLine, "[Xilinx unveil revolutionary 65nm FPGA architecture: the Virtex-5 family](http://www.pldesignline.com/products/187203173)". May 15, 2006. Retrieved February 5, 2009.
14. Press Release, "[Xilinx Co-Founder Ross Freeman Honored as 2009 National Inventors Hall of Fame Inductee for Invention of FPGA](http://press.xilinx.com/phoenix.zhtml?c=212763&p=irol-newsArticle&ID=1255523&highlight)"
15.
16.
17. Clive Maxfield, book "[The Design Warrior's Guide to FPGAs](http://books.google.com/books?id=dnuwr2xOFpUC&pg=PA4&lpg=PA4&dq=FPGA+Market+growth+1990s&source=web&ots=YjFedB35Vp&sig=EH8y56Cih9iNLEqYXkZ63iO46K4&hl=en&sa=X&oi=book_result&resnum=4&ct=result)" Published by Elsevier, 2004. ISBN 0750676043, 9780750676045. Retrieved February 5, 2009
18.
19.
20.
21. [S5000ソフトウェア・コンフィギュラブル・プロセッサ](http://www.stretchinc.co.jp/products/s5000.php) Stretch
22.
23.
24.
25.
26.
27.
28. Dylan McGrath, EE Times, "[FPGA Market to Pass $2.7 Billion by '10, In-Stat Says](http://www.eetimes.com/electronics-news/4060747/FPGA-market-to-pass-2-7-billion-by-10-In-Stat-says)". May 24, 2006. Retrieved February 5, 2009.
29. Moshe Gavrielov, Electronics Weekly, "[FPGA Market Soaring To $4bn In 2010, says Gavrielov](http://www.electronicsweekly.com/news/components/programmable-logic-and-asic/fpga-market-soaring-to-4bn-in-2010-says-gavrielov-2010-05)". May 19, 2010. Retrieved January 8, 2013.
30. Research and Markets, "[Field-Programmable Gate Array (FPGA) Market by Architecture, Configuration, Application, and Geography - Trends & Forecasts From 2014 – 2020](http://www.researchandmarkets.com/research/ljkcnm/fieldprogrammable)". January, 2015. Retrieved March 20, 2015.
31. Narinder Lall, eASIC Corporation, "[FPGA Judgment Day: Rise of Second Generation Structured ASICs](http://www.opensystems-publishing.com/e-letter/dsp/2008/03/easic.pdf)". March, 2008. Retrieved February 5, 2009.
32. Dylan McGrath, EE Times, "[Gartner Dataquest Analyst Gives ASIC, FPGA Markets Clean Bill of Health](http://www.eetimes.com/conf/dac/showArticle.jhtml?articleID=164302400)". June 13, 2005. Retrieved February 5, 2009.
33. [Virtex-4 Family Overview](http://www.xilinx.com/support/documentation/data_sheets/ds112.pdf)
34. Bob Pencek, Industrial Embedded Systems, "[Reconfigurable Application-Specific Computing: How Hybrid Computer Systems using FPGAs are Changing Signal Processing](http://industrial-embedded.com/reconfigurable-fpgas-changing-signal-processing)". No Date. Retrieved February 5, 2009.
35. Tim Erjavec, White Paper, "[Introducing the Xilinx Targeted Design Platform: Fulfilling the Programmable Imperative](http://www.xilinx.com/publications/prod_mktg/Targeted_Design_Platforms.pdf)." February 2, 2009. Retrieved February 2, 2009
36.
37. Huffmire Paper "[Managing Security in FPGA-Based Embedded Systems](http://www2.computer.org/portal/web/csdl/doi/10.1109/MDT.2008.166)." Nov-Dec 2008. Retrieved Sept 22, 2009
38. [FPGA/DSP Blend Tackles Telecom Apps](http://www.bdti.com/articles/info_eet0207fpga.htm)
39. [Xilinx aims 65-nm FPGAs at DSP applications](http://www.eetimes.com/showArticle.jhtml?articleID=197001881)
40. [インテル、FPGA大手のアルテラ買収を完了](http://www.publickey1.jp/blog/16/fpgafpga.html)
41. [インテル「２兆円買収」で手に入れる３つの未来](http://www.nikkei.com/article/DGXMZO87633350T00C15A6000000/)
42. トランジスタ技術スペシャル編集部（編著: 森田一ほか）および大中邦彦（該当22ページの著者）、『トランジスタ技術スペシャル』、CQ出版社、22ページ図7（ページ右上にある）、2009年7月1日発行。
43.
44. [Cyclone II Architecture](http://www.altera.com/literature/hb/cyc2/cyc2_cii51002.pdf) ALTERA
45. [Section I. Device Core](http://www.altera.com/literature/hb/stratix-iv/stx4_5v1_01.pdf) ALTERA
46. [Virtex-4 FPGA User Guide](http://www.xilinx.com/support/documentation/user_guides/ug070.pdf) Xilinx
47. [Achieving Higher System Performance with the Virtex-5 Family of FPGAs](http://www.xilinx.com/bvdocs/whitepapers/wp245.pdf) Xilinx
48. Seeking Alpha, "[Altera and Xilinx Report: The Battle Continues](http://seekingalpha.com/article/85478-altera-and-xilinx-report-the-battle-continues)". July 17, 2008. Retrieved February 5, 2009.
49. [EE Time 2011年03月15日記事](http://eetimes.jp/ee/articles/1103/15/news081.html)
50. [Altera Corporation 2010 Letter to Shareholders](http://phx.corporate-ir.net/External.File?item=UGFyZW50SUQ9NDE0NDExfENoaWxkSUQ9NDI2MDQ0fFR5cGU9MQ==&t=1)
51.
52.
53. [CNET Japan 2015年6月2日](http://japan.cnet.com/news/business/35065319/)