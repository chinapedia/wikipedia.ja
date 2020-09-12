> この記事は[Folding@homeコアのリスト](https://ja.wikipedia.org/wiki/Folding@homeコアのリスト)から翻訳されています。


[Folding@home](../Page/Folding@home.md "wikilink")の分散コンピューティングプロジェクトは、FahCores(ファーコア)またはCore(コア)と呼ばれる科学的なコンピュータプログラムを使用して計算を実行する。\[1\]\[2\] Folding@homeのコアは、, [GROMACS](../Page/GROMACS.md "wikilink"), [AMBER](https://ja.wikipedia.org/wiki/AMBER "wikilink"), , SHARPEN, ProtoMol, などの計算用分子シミュレーションプログラムの修正・[最適化されたバージョンに基づいている](../Page/最適化_\(情報工学\).md "wikilink")。\[3\]\[4\]\[5\] これらの種類には、それぞれ[任意](../Page/任意.md "wikilink")の識別子(Core xx)が与えられている。 同じコアを様々なバージョンのクライアントで使用することができるが、コアをクライアントから分離することで、クライアントの更新なしに必要に応じて科学的手法を自動的に更新することができる。\[6\]

## 使用されているコア

これらのコアは、現在プロジェクトで使用されている。\[7\]

### GROMACS

  - Core a7
      - Windows、Linux、およびmacOSで利用可能で、利用可能な場合は[Advanced Vector Extensionsを使用することで](https://ja.wikipedia.org/wiki/Advanced_Vector_Extensions "wikilink")、大幅な速度改善が可能である。\[8\]

### GPU

[グラフィックス・プロセシング・ユニットのコアは](https://ja.wikipedia.org/wiki/グラフィックスプロセシングユニット "wikilink")、分子動力学を行うために、新しいビデオカードのグラフィックスチップを使用する。GPU Gromacs コアは Gromacs の真の移植ではなく、Gromacs の主要な要素を取り入れ、GPU機能のために強化したものである。\[9\]

#### GPU3

これらは第3世代のGPUコアで、パンデGroupが独自に開発した分子シミュレーション用のオープンライブラリであるをベースにしている。GPU2のコードをベースにしているが、安定性と新機能が追加されている。\[10\]

  - core 21
      - OpenCLを使用したAMDとNVIDIA GPU用のWindowsとLinuxで利用可能。OpenMM 6.2を使用しており、Core 18 AMD/NVIDIAのパフォーマンス問題を修正している。\[11\]
  - core 22
      - OpenCLを使用したAMDとNVIDIA GPU用のWindowsとLinuxに対応している。OpenMM 7.4.1を使用している。\[12\]

## 使用されないコア

これらのコアは、時代遅れになりつつあるために引退しているか、一般的なリリースの準備ができていないため、現在プロジェクトでは使用されていない。\[13\]

### TINKER

は、分子力学と分子動力学のための完全かつ一般的なパッケージを備えた分子動力学シミュレーションのためのコンピュータ・ソフトウェア・アプリケーションであり、生体高分子のためのいくつかの特別な機能を備えている。\[14\]

  - Tinker core (Core 65)
      - 最適化されていない単一プロセッサコアで、AMBERコアとGromacsコアが同じタスクをはるかに高速に実行するため、これは公式に引退しました。このコアは Windows、Linux、Mac で利用可能であった。\[15\]

### GROMACS

  - GroGPU (Core 10)
      - Windows 上で動作する [ATI](../Page/ATI_Technologies.md "wikilink")  で利用可能。ほとんどが Gromacs ベースであるが、コアの一部が書き換えられた。 このコアは、第二世代のGPUクライアントへの移行に伴い、2008年6月6日をもって引退した。
  - Gro-SMP (Core a1)
      - Windows [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")、Mac x86、Linux x86/[64クライアントで利用可能で](https://ja.wikipedia.org/wiki/X86_64 "wikilink")\[16\]、これは[SMPバリアントの第一世代であり](../Page/対称型マルチプロセッシング.md "wikilink")、[プロセス間通信](../Page/プロセス間通信.md "wikilink")に[MPIを使用していた](../Page/Message_Passing_Interface.md "wikilink")。 このコアは、スレッドベースの SMP2 クライアントへの移行により、引退した。\[17\]\[18\]
  - GroCVS (Core a2)
      - x86 Mac および x86/64 Linux でのみ利用可能なこのコアは、MPI の使用など、同じコアベースの多くを使用しているため、Core a1 と非常によく似ている。 しかし、このコアはより最近の Gromacs コードを利用しており、特大のワークユニットなどのより多くの機能をサポートしている。\[19\]\[20\] スレッドベースの SMP2 クライアントへの移行に伴い、正式に引退した。
  - Gro-PS3
      - SCEARD コアとしても知られているこのバリアントは、2012年11月に引退するまで Folding@Home クライアントをサポートしていた [PlayStation 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink") ゲームシステム用のものである\[21\]\[22\]。このコアは、GPUコアと同様に暗黙の解法計算を実行するものだが、CPUコアと同様に明示的な解法計算を実行することもでき、柔軟性に欠ける高速GPUコアと柔軟性に欠ける低速CPUコアの中間的な役割を果たしていた。\[23\] このコアは最適化に[SPEコアを使用していたが](https://ja.wikipedia.org/wiki/Cell_Broadband_Engine#SPEによる自己マルチタスク "wikilink")、SIMDはサポートしていなかった。
  - Gromacs (Core 78)
      - これはオリジナルのGromacsコアで\[24\]、現在はクライアントのみが利用可能で、Windows、Linux、macOSをサポートしている。\[25\]
  - Gromacs 33 (Core a0)
      - Windows、Linux、およびmacOSの単一プロセッサクライアントでのみ利用可能なこのコアは、Gromacs 3.3のを使用しているため、より幅広いシミュレーションを実行することができる。\[26\]\[27\]
  - Gromacs SREM (Core 80)
      - このコアは、REMD(Replica Exchange Molecular Dynamics)やGroST(Gromacs Serial replica exchange with Temperatures)とも呼ばれるシリアル[レプリカ交換方式をシミュレーションに使用しており](https://ja.wikipedia.org/wiki/レプリカ交換法 "wikilink")、WindowsとLinuxの単一プロセッサクライアントのみで利用できる。\[28\]\[29\]\[30\]
  - GroSimT (Core 81)
      - このコアは、温度を定期的に上げたり下げたりすることでサンプリングを向上させることを基本的な考え方としており、シミュレーテッドテンパリング(simulated tempering)を行う。 これにより、Folding@homeは、タンパク質の折り畳まれた状態と折り畳まれていない状態の間の遷移をより効率的にサンプリングできるようになる。\[31\] WindowsとLinuxの単一プロセッサクライアントでのみ利用可能である。\[32\]
  - DGromacs (Core 79)
      - 単一プロセッサクライアントで利用可能なこのコアは、サポートされている[SSE2](https://ja.wikipedia.org/wiki/SSE2 "wikilink")プロセッサの最適化を使用しており、Windows、Linux、およびmacOSで実行できる。\[33\]\[34\]
  - DGromacsB (Core 7b)
      - Core 79 とは異なり、いくつかの科学的な機能が追加されている。\[35\] 2007年8月にLinuxプラットフォームのみにリリースされたが、最終的にはすべてのプラットフォームで利用できるようになる予定である。\[36\]
  - DGromacsC (Core 7c)
      - Core 79に非常に似ており、2008年4月にLinuxとWindows向けにWindows、Linux、macOSの単一プロセッサクライアント向けにリリースされた。\[37\]
  - GB Gromacs (Core 7a)
      - Windows、Linux、macOS上のすべての単一プロセッサクライアントでのみ利用可能である。\[38\]\[39\]\[40\]
  - GB Gromacs (Core a4)
      - Windows、Linux\[41\]、macOS\[42\] で利用可能なこのコアは、2010年10月初旬にリリースされ\[43\]、2010年2月現在、最新バージョンの Gromacs v4.5.3 を使用している。\[44\]
  - SMP2 (Core a3)
      - 次世代のSMPコアであるこのコアは、プロセス間通信にMPIの代わりにスレッドを使用し、Windows、Linux、macOSで利用可能である。\[45\]\[46\]
  - SMP2 bigadv (Core a5)
      - a3に似ているが、このコアは通常よりも大きなシミュレーションを実行するために特別に設計されている。\[47\]\[48\]
  - SMP2 bigadv (Core a6)
      - a5コアの新しいバージョン。

### CPMD

[カー・パリネロ分子動力学](https://ja.wikipedia.org/wiki/カー・パリネロ分子動力学 "wikilink")法(Car-Parinello Molecular Dynamics)の略で、このコアは[第一原理計算](../Page/第一原理計算.md "wikilink")(*ab-initio*)の[量子力学](https://ja.wikipedia.org/wiki/量子力学 "wikilink")的[分子動力学を実行する](../Page/分子動力学法.md "wikilink")。力場アプローチを用いる古典的な分子動力学計算とは異なり、CPMDではエネルギー、力、運動の計算に[電子](https://ja.wikipedia.org/wiki/電子 "wikilink")の運動が含まれる。\[49\]\[50\] 量子化学計算は、非常に信頼性の高いポテンシャルエネルギー面が得られる可能性があり、自然にマルチボディ相互作用を組み込むことができる。\[51\]

  - QMD (Core 96)
      - これはWindowsとLinuxの単一プロセッサクライアント用の倍精度\[52\]バリアントである。\[53\] このコアは、主要な QMD 開発者である Young Min Rhee が 2006 年に卒業したため、現在は "保留" となっている。\[54\] このコアは、かなりの量のメモリを使用することができ、「オプトイン」を選択したマシンでのみ利用可能であった\[55\]。 Intel CPU上でのSSE2最適化がサポートされている。\[56\] [Intel](https://ja.wikipedia.org/wiki/Intel "wikilink")ライブラリとSSE2が関係するライセンス問題のため、[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") CPUにはQMD Work Unitは割り当てられていなかった。\[57\]\[58\]

### SHARPEN

  - SHARPEN Core\[59\]\[60\]
      - 2010年初頭、は「SHARPENは今のところ保留にしている。申し訳ないが、ETAはない。それをさらに推し進めるかどうかは、その時の科学的ニーズに大きく依存している」と語った。\[61\] このコアは標準的なF@Hコアとは異なるフォーマットを使用しており、クライアントに送信される各ワークパケットには1つ以上の「ワークユニット」(通常の定義を使用)が含まれている。

### Desmond

このコアのソフトウェアは、で開発された。 Desmondは、従来のコンピュータクラスタ上で生物系の高速[分子動力学シミュレーションを実行する](../Page/分子動力学法.md "wikilink")。\[62\]\[63\]\[64\]\[65\] このコードは、新しい並列アルゴリズム\[66\]と数値計算技術\[67\]を用いて、多数のプロセッサを含むプラットフォーム上で高い性能を実現しているが\[68\]、単一のコンピュータ上でも実行することができる。  Desmondとそのソースコードは、大学やその他の非営利の研究機関が非商業的に利用するために無償で提供されている。

  - Desmond Core
      - Windows x86とLinux x86/64で利用可能で\[69\]、このコアは現在開発中である。\[70\]

### AMBER

Assisted Model Building with Energy Refinementの略で、AMBERは分子動力学のための力場のファミリーであり、これらの力場をシミュレートするソフトウェアパッケージの名前でもある。\[71\] AMBERはもともと[カリフォルニア大学サンフランシスコ校](../Page/カリフォルニア大学サンフランシスコ校.md "wikilink")のPeter Kollmanによって開発され、現在は様々な大学の教授によって管理されている。\[72\] 倍精度AMBERコアは現在SSEやSSE2で最適化されていないが\[73\]\[74\]、AMBERはTinkerコアよりも大幅に高速で、Gromacsコアでは実行できない機能も追加されている。\[75\]

  - PMD (Core 82)
      - WindowsとLinuxの単一プロセッサクライアントでのみ利用可能である。\[76\]

### ProtoMol

は、分子動力学(MD)シミュレーションのためのオブジェクト指向、コンポーネントベースのフレームワークです。ProtoMolは、高い柔軟性、容易な拡張性とメンテナンス、並列化を含む高い性能要求を提供する。\[77\] 2009年には、Pandeグループはノーマルモード・ランジュバン・ダイナミクス(Normal Mode Langevin Dynamics)と呼ばれる補完的な新しい手法に取り組んでいたが、これは同じ精度を維持しながらシミュレーションを大幅に高速化できる可能性を秘めていた。\[78\]\[79\]

  - ProtoMol Core (Core b4)
      - Linux x86/64およびx86 Windowsに対応している。\[80\]

### GPU

#### GPU2

これらは第2世代のGPUコアである。引退したGPU1コアとは異なり、ATI CAL対応の2xxx/3xxx以降のシリーズと[NVIDIA](../Page/NVIDIA.md "wikilink") [CUDA](../Page/CUDA.md "wikilink")対応のNVIDIA 8xxx以降のシリーズのGPU向けのバリアントである。\[81\]

  - GPU2 (Core 11)
      - x86 Windowsクライアントでのみ利用可能。\[82\] AMD/ATIが利用していたプログラミング言語のサポートを終了し、[OpenCL](../Page/OpenCL.md "wikilink")に移行したため、2011年9月1日頃までサポートされていた。このため、F@hはATIのGPUコアコードをOpenCLで書き換えることを余儀なくされ、その結果、Core 16となった。\[83\]
  - GPU2 (Core 12)
      - x86 Windowsクライアントでのみ利用可能。\[84\]
  - GPU2 (Core 13)
      - x86 Windowsクライアントでのみ利用可能。\[85\]
  - GPU2 (Core 14)
      - このコアはx86 Windowsクライアントでのみ利用可能で\[86\]、2009年3月2日に正式にリリースされた。\[87\]

#### GPU3

これらは第3世代のGPUコアで、パンデ・グループが独自に開発した分子シミュレーション用のオープンライブラリである[OpenMM](https://ja.wikipedia.org/wiki/OpenMM "wikilink")をベースにしている。GPU2のコードに基づき、安定性と新機能が追加されている。\[88\]

  - GPU3 (core 15)
      - x86 Windowsのみで利用可能。\[89\]
  - GPU3 (core 16)
      - x86 Windowsのみで利用可能。\[90\] 新しいv7クライアントと一緒にリリースされ、これは[OpenCL](../Page/OpenCL.md "wikilink")でCore 11を書き換えたものである。\[91\]
  - GPU3 (core 17)
      - OpenCLを使用したAMDとNVIDIA GPU用のWindowsとLinuxで利用可能。OpenMM 5.1のため、パフォーマンスが大幅に向上している。\[92\]
  - GPU3 (core 18)
      - OpenCLを使用したAMDおよびNVIDIA GPU用のWindowsで利用可能。このコアは、Core17のいくつかの重要な科学的問題に対処するために開発され\[93\]、OpenMM 6.0.1の最新技術を使用している。\[94\] 現在、一部のAMDおよびNVIDIA Maxwell GPU上では、このコアの安定性とパフォーマンスに問題がある。このため、一部のGPUでは、このコア上で動作するワークユニットの割り当てが一時的に停止されていいる。\[95\]

## References

<references group="" responsive="1">

</references>

## External links

  - [Main F@h Core FAQ](http://folding.stanford.edu/English/FAQ)
  - [GROMACS Core FAQ](https://www.webcitation.org/6AqrEXY89?url=http://folding.stanford.edu/English/FAQ-gromacs)
  - [AMBER Core FAQ](http://folding.stanford.edu/English/FAQ-AMBER)
  - [PROTOMOL Core FAQ](http://folding.stanford.edu/English/FAQ-PROTOMOL)
  - [QMD Core FAQ](http://folding.stanford.edu/English/FAQ-QMD)

[Category:計算化学](https://ja.wikipedia.org/wiki/Category:計算化学 "wikilink") [Category:数理生物学](https://ja.wikipedia.org/wiki/Category:数理生物学 "wikilink") [Category:計算生物学](https://ja.wikipedia.org/wiki/Category:計算生物学 "wikilink") [Category:分子モデリングソフトウェア](https://ja.wikipedia.org/wiki/Category:分子モデリングソフトウェア "wikilink") [Category:分子動力学ソフトウェア](https://ja.wikipedia.org/wiki/Category:分子動力学ソフトウェア "wikilink") [Category:シミュレーション](https://ja.wikipedia.org/wiki/Category:シミュレーション "wikilink")

1.
2.
3.
4.   *The site indicates that Folding@home uses a modification of CPMD allowing it to run on the supercluster environment.*
5.
6.
7.
8.
9.
10.
11.
12.
13.
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
29.
30.
31.
32.
33.
34.
35.
36.
37.
38.
39.
40.
41.
42.
43.
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
55.
56.
57.
58.
59.
60.
61.
62.
63.
64.
65.
66.
67.
68.
69.
70.
71.
72.
73.
74.
75.
76.
77.
78.
79.
80.
81.
82.
83.
84.
85.
86.
87.
88.
89.
90.
91.
92.
93.
94.
95.