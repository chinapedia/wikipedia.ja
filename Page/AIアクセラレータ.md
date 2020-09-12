> この記事は[AIアクセラレータ](https://ja.wikipedia.org/wiki/AIアクセラレータ)から翻訳されています。


**AIアクセラレータ**(AI accelerator)は、[人工知能](../Page/人工知能.md "wikilink")(AI)アプリケーション、特に人工[ニューラルネットワーク](../Page/ニューラルネットワーク.md "wikilink")、[マシンビジョン](../Page/マシンビジョン.md "wikilink")、[機械学習](../Page/機械学習.md "wikilink")を高速化するために設計された特殊な[ハードウェアアクセラレータ](../Page/ハードウェアアクセラレーション.md "wikilink")\[1\]またはコンピュータシステム\[2\]\[3\]のクラスである。代表的なアプリケーションには、[ロボット工学](../Page/ロボット工学.md "wikilink")、[モノのインターネット](https://ja.wikipedia.org/wiki/モノのインターネット "wikilink")、その他の[データ](../Page/データ.md "wikilink")集約型またはセンサー駆動型のタスクのためのアルゴリズムが含まれる\[4\]。それらは多くの場合、[メニーコア](https://ja.wikipedia.org/wiki/メニーコア "wikilink")設計であり、一般的には低[精度演算](../Page/精度_\(算術\).md "wikilink")、斬新な、または機能に焦点を当てている\[5\]。2018年現在、典型的なAI[集積回路](../Page/集積回路.md "wikilink")チップには個の[MOSFET](../Page/MOSFET.md "wikilink")トランジスタが含まれている\[6\]。

このカテゴリのデバイスには、多くのベンダー固有の用語が存在しており、これはのないである。

## AIアクセラレーションの歴史

[コンピュータシステム](../Page/コンピュータシステム.md "wikilink")は、[コ・プロセッサ](https://ja.wikipedia.org/wiki/コ・プロセッサ "wikilink")と呼ばれる特殊なタスクのための特殊な目的のアクセラレータで[CPU](../Page/CPU.md "wikilink")を補完することが頻繁に行われてた。注目される[アプリケーション固有の](../Page/ASIC.md "wikilink")[ハードウェアユニットには](../Page/拡張カード.md "wikilink")、[グラフィックス](https://ja.wikipedia.org/wiki/グラフィックス "wikilink")用[ビデオカード](../Page/ビデオカード.md "wikilink")、[サウンドカード](../Page/サウンドカード.md "wikilink")、[グラフィックス処理装置](https://ja.wikipedia.org/wiki/グラフィックスプロセシングユニット "wikilink")、[デジタル信号処理装置などがある](https://ja.wikipedia.org/wiki/デジタル信号プロセッサ "wikilink")。2010年代に[ディープラーニング](https://ja.wikipedia.org/wiki/ディープラーニング "wikilink")や[人工知能](../Page/人工知能.md "wikilink")のワークロードが注目されるようになると、これらのタスクを[高速化するために](../Page/ハードウェアアクセラレーション.md "wikilink")、特殊なハードウェアユニットが開発されたり、既存の製品から採用されたりした。

### 初期の試み

早くも1993年には、[デジタル・シグナル・プロセッサがニューラルネットワークのアクセラレータとして使用され](../Page/デジタルシグナルプロセッサ.md "wikilink")、例えば[光学文字認識](../Page/光学文字認識.md "wikilink")ソフトウェアを高速化するために使用されていた\[7\]。1990年代には、ニューラルネットワーク・シミュレーションを含む様々なアプリケーションを目的としたワークステーション用の並列ハイスループットシステムの開発も試みもあった\[8\]\[9\]\[10\]。[FPGA](../Page/FPGA.md "wikilink")ベースのアクセラレータも1990年代に推論\[11\]とトレーニング\[12\]の両方のために最初に検討された。ANNAはによって開発されたニューラルネットCMOSアクセラレータである\[13\]。

### ヘテロジニアス・コンピューティング

[ヘテロジニアス・コンピューティング](https://ja.wikipedia.org/wiki/ヘテロジニアス・コンピューティング "wikilink")(異機種コンピューティング)とは、1 つのシステム、あるいは1つのチップに、特定のタイプのタスクに最適化された多数の特化したプロセッサを組み込むことを意味する。[セル・マイクロプロセッサ](../Page/Cell_Broadband_Engine.md "wikilink")(cell microprocessor)のようなアーキテクチャは\[14\]、パック化低精度演算(packed low precision arithmetic)のサポート、[データフロー](../Page/データフロー.md "wikilink")・アーキテクチャ、レイテンシよりも「スループット」を優先するなど、AIアクセラレータと大きく重複する特徴を持っている。セル・マイクロプロセッサはその後、AIを含む多くのタスク\[15\]\[16\]\[17\]に応用された\[18\]\[19\]\[20\]。

[2000年代](../Page/2000年代.md "wikilink")には、[CPU](../Page/CPU.md "wikilink")は、ビデオやゲームのワークロードに牽引されて、[SIMD](../Page/SIMD.md "wikilink")ユニットのデータ幅をますます広げ、低精度の[データ型](../Page/データ型.md "wikilink")を[パック化してサポートするようになった](https://ja.wikipedia.org/wiki/データ構造アライメント#%E3%83%87%E3%83%BC%E3%82%BF%E6%A7%8B%E9%80%A0%E3%83%91%E3%83%86%E3%82%A3%E3%83%B3%E3%82%B0 "wikilink")\[21\]。

### GPUの利用

[グラフィックス・プロセッシング・ユニット](https://ja.wikipedia.org/wiki/グラフィックスプロセッシングユニット "wikilink") (GPU)は、[画像を操作したり](../Page/グラフィックスパイプライン.md "wikilink")、局所的な画像特性を計算するための特殊なハードウェアである。ニューラルネットワークと画像操作の数学的基礎は類似しており、行列を含むなタスクであり、GPUが機械学習タスクにますます使用されるようになってきている\[22\]\[23\]\[24\]。2016年現在、GPUはAI作業で人気があり、自動運転車\[25\]などのデバイスでのトレーニング\[26\]と推論の両方でディープラーニングを促進にする方向に進化し続けている。Nvidia [NVLink](https://ja.wikipedia.org/wiki/NVLink "wikilink")などのGPU開発者は、AIがもたらすデータフロー・ワークロードの種類のための追加の接続機能を開発している\[27\]。GPUのAIアクセラレーションへの応用が進むにつれ、GPUメーカは、[ニューラルネットワーク](../Page/ニューラルネットワーク.md "wikilink")に[特化したハードウェアを組み込んで](../Page/ASIC.md "wikilink")、これらのタスクをさらに高速化している\[28\]\[29\]。(テンソルコア)は、ニューラルネットワークのトレーニングを高速化することを目的としている\[30\]。

### FPGAの利用

ディープラーニングのフレームワークはまだ進化の途上にあり、カスタムのハードウェアを設計するのは難しい。[FPGA](../Page/FPGA.md "wikilink") (Field-Programmable Gate Array)のような[再構成可能なデバイスにより](https://ja.wikipedia.org/wiki/再構成可能コンピューティング "wikilink")、ハードウェア、フレームワーク、ソフトウェアを[相互に進化させることが容易になる](../Page/参加型デザイン.md "wikilink")\[31\]\[32\]\[33\]。

マイクロソフトは、FPGAチップを使って[推論](../Page/推論.md "wikilink")\[34\]を高速化している。FPGAをAIアクセラレーションに適用することは、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が[アルテラ](../Page/アルテラ.md "wikilink")を買収することを動機付け、サーバCPUにFPGAを統合することで、汎用的なタスクだけでなくAIも加速できるようにすることを目的としている\[35\]。

### AIアクセラレータ専用ASICの登場

AI関連のタスクでは、GPUとFPGAの方がCPUよりもはるかに優れた性能を発揮するが、[ASIC](../Page/ASIC.md "wikilink") (Application Specific Integrated Circuit)を介したより特殊な設計では、最大で10倍の効率性\[36\]\[37\]が得られる可能性がある。これらのアクセラレータは、最適化されたや、低精度演算を使用して計算を高速化し、計算の[スループット](../Page/スループット.md "wikilink")を向上させるなどの戦略を採用している\[38\]\[39\]。AIアクセラレーションで採用されている低精度[浮動小数点フォーマットには](../Page/浮動小数点数.md "wikilink")、[半精度浮動小数点フォーマットやbfloat](https://ja.wikipedia.org/wiki/半精度浮動小数点数 "wikilink")16浮動小数点フォーマットがある\[40\]\[41\]\[42\]\[43\]\[44\]\[45\]\[46\]。

### インメモリ・コンピューティング・アーキテクチャ

2017年6月、[IBM](../Page/IBM.md "wikilink")の研究者は、[ヘテロジニアス・コンピューティング](https://ja.wikipedia.org/wiki/ヘテロジニアス・コンピューティング "wikilink")と[大規模並列システムに一般化するアプローチを目的とした](../Page/超並列マシン.md "wikilink")、時間的相関検出に適用されると[相変化メモリ](../Page/相変化メモリ.md "wikilink")・アレイに基づく[フォン・ノイマン・アーキテクチャとは対照的なアーキテクチャを発表した](../Page/ノイマン型.md "wikilink")\[47\]。2018年10月、IBMの研究者は、インメモリ処理に基づく、人間の脳のシナプスネットワークをモデルにしたアーキテクチャを発表し、[ディープニューラルネットワークを高速化した](https://ja.wikipedia.org/wiki/ディープラーニング "wikilink")\[48\]。このシステムは相変化メモリアレイに基づいている\[49\]。

## 命名法

2016年現在、この分野はまだ流動的であり、ベンダーは自社のデザインと[APIが](../Page/アプリケーションプログラミングインタフェース.md "wikilink")になることを期待して、「AIアクセラレータ」に相当するものについて独自のマーケティング用語を推薦している。これらのデバイス間の境界線についても、正確な形式についても合意はないが、いくつかの例は明らかにこの新しい空間を埋めることを目的としており、かなりの量の機能が重複している。

コンシューマー向けの[グラフィックス・アクセラレータが登場した過去の業界では](https://ja.wikipedia.org/wiki/グラフィックスアクセラレータ "wikilink")、[Direct3D](../Page/Direct3D.md "wikilink")が提示したモデルを実装した全体的なパイプラインに落ち着くまでに、さまざまな形式をとってきた「グラフィックスアクセラレータ」の総称として、最終的にはNvidiaの「GPU」\[50\]という独自の用語を採用した。

## 潜在的なアプリケーション

  - [自動運転車](https://ja.wikipedia.org/wiki/スマートカー "wikilink") - NvidiaはこのスペースでDrive PXシリーズボードをターゲットにしている。 \[51\]
  - [軍用ロボット](../Page/軍事用ロボット.md "wikilink")
  - [農業用ロボット](https://ja.wikipedia.org/wiki/農業用ロボット "wikilink") - たとえば無農薬の雑草防除。 \[52\]
  - [音声制御](https://ja.wikipedia.org/wiki/音声操作 "wikilink") (携帯電話など) - [Qualcomm Zerothのターゲット](https://ja.wikipedia.org/wiki/Qualcomm_Zeroth "wikilink") \[53\]
  - [機械翻訳](../Page/機械翻訳.md "wikilink")
  - [無人航空機](../Page/無人航空機.md "wikilink") - たとえばナビゲーションシステム、たとえば[Movidius Myriad](https://ja.wikipedia.org/wiki/Movidius_Myriad_2 "wikilink") 2は、無人偵察機の誘導に成功した。 \[54\]
  - [産業用ロボット](../Page/産業用ロボット.md "wikilink") - さまざまな状況に適応できるようにすることで、自動化できるタスクの範囲を広げる。
  - [ヘルスケア](../Page/医療.md "wikilink") - 診断を支援する
  - [検索エンジン](../Page/検索エンジン.md "wikilink") - [データセンター](https://ja.wikipedia.org/wiki/データセンター "wikilink")の[エネルギー効率](https://ja.wikipedia.org/wiki/エネルギー効率 "wikilink")を高め、ますます高度な[クエリを使用できるようにする](../Page/情報検索.md "wikilink")
  - [自然言語処理](../Page/自然言語処理.md "wikilink")

## 関連項目

  - [認知コンピュータ](https://ja.wikipedia.org/wiki/:en:Cognitive_computer "wikilink")
  - [ニューロモーフィックコンピューティング](https://ja.wikipedia.org/wiki/:en:Neuromorphic_computing "wikilink")
  - [物理ニューラルネットワーク](https://ja.wikipedia.org/wiki/:en:Physical_neural_network "wikilink")
  - [光ニューラルネットワーク](https://ja.wikipedia.org/wiki/:en:Optical_neural_network "wikilink")
  - [深層学習アクセラレータ](https://ja.wikipedia.org/wiki/:en:Deep_learning_accelerator "wikilink")

## 脚注

## 外部リンク

  - <http://www.nextplatform.com/2016/04/05/nvidia-puts-accelerator-metal-pascal/>
  - <http://eyeriss.mit.edu>
  - <http://www.alphaics.ai/>

[Category:コンピュータの最適化](https://ja.wikipedia.org/wiki/Category:コンピュータの最適化 "wikilink")

1.
2.
3.
4.  Google using its own AI accelerators.
5.  "[A Survey of ReRAM-based Architectures for Processing-in-memory and Neural Networks](https://www.academia.edu/36504841/A_Survey_of_ReRAM-based_Architectures_for_Processing-in-memory_and_Neural_Networks)", S. Mittal, Machine Learning and Knowledge Extraction, 2018
6.
7.
8.
9.  This presentation covers a past attempt at neural net accelerators, notes the similarity to the modern SLI GPGPU processor setup, and argues that general purpose vector accelerators are the way forward (in relation to RISC-V hwacha project. Argues that NN's are just dense and sparse matrices, one of several recurring algorithms)
10.
11.
12.
13. [Application of the ANNA Neural Network Chip to High-Speed Character Recognition](http://yann.lecun.com/exdb/publis/pdf/saeckinger-92.pdf)
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29. "[A Survey on Optimized Implementation of Deep Learning Models on the NVIDIA Jetson Platform](https://www.researchgate.net/publication/329802520_A_Survey_on_Optimized_Implementation_of_Deep_Learning_Models_on_the_NVIDIA_Jetson_Platform)", 2019
30.
31.
32.
33.
34.
35. "[A Survey of FPGA-based Accelerators for Convolutional Neural Networks](https://www.academia.edu/37491583/A_Survey_of_FPGA-based_Accelerators_for_Convolutional_Neural_Networks)", Mittal et al., NCAA, 2018
36.
37.
38.
39.
40.
41.
42.
43.  Cloud TPU {{\!}} Google Cloud|author=|work=Google Cloud|date=|accessdate=2018-05-23|url=[https://cloud.google.com/tpu/docs/tensorflow-ops|quote=This](https://cloud.google.com/tpu/docs/tensorflow-ops%7Cquote=This) page lists the TensorFlow Python APIs and graph operators available on Cloud TPU.}}
44.
45.
46.
47.
48.
49.
50.
51.
52.
53.
54.