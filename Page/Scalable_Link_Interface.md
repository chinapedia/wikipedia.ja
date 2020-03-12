> この記事は[Scalable Link Interface](https://ja.wikipedia.org/wiki/Scalable_Link_Interface)から翻訳されています。


**Scalable Link Interface** (SLI、スケーラブル・リンク・インターフェース) とは、[NVIDIA](../Page/NVIDIA.md "wikilink")の[マルチ](../Page/マルチ.md "wikilink")[GPU動作システムである](../Page/Graphics_Processing_Unit.md "wikilink")。2枚あるいはそれ以上のSLI対応[グラフィックスカード](https://ja.wikipedia.org/wiki/グラフィックスカード "wikilink")（[ビデオカード](../Page/ビデオカード.md "wikilink")、[ビデオボード](https://ja.wikipedia.org/wiki/ビデオボード "wikilink")、[グラフィックスボード](https://ja.wikipedia.org/wiki/グラフィックスボード "wikilink")、グラフィックスチップ）を並列動作させ、出力は1つに集約させることで、[コンピュータグラフィックス](../Page/コンピュータグラフィックス.md "wikilink")の描画処理を高速に行なうことができる。派生した規格としてHybrid SLIがある。

## 技術

元々は[3dfx](../Page/3dfx.md "wikilink")が**Scan-Line Interleave**として開発し、[Voodoo](https://ja.wikipedia.org/wiki/Voodoo "wikilink")2で導入した技術である。2基のVoodoo2チップをシステムに搭載し、画面の[走査線](https://ja.wikipedia.org/wiki/走査線 "wikilink")を奇数と偶数で分けることでそれぞれのVoodoo2チップが並列して描画する。当時の3D描画機能としては極めて高い水準にあり、他社製品を大きくリードした。

Voodoo2の時代に開発されたSLI技術は、3dfxを買収したNVIDIAが[PCI Express用に改良し](../Page/PCI_Express.md "wikilink")、GeForceシリーズの機能の1つであるSLI (**Scalable Link Interface**) として実装した。これは画面を奇数・偶数走査線に分けて描画する3dfxのSLIに対し、画面を上下2分割 (あるいは搭載チップ数で分割)、フレーム毎に担当GPUを分ける方式で、3dfx SLIが潜在的に持っていた[メモリコヒーレンシ問題の解消を狙ったものである](https://ja.wikipedia.org/wiki/メモリ一貫性 "wikilink")。

同様の手法はATI（現[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")）の[RAGE FURY MAXXにも取り入れられ](https://ja.wikipedia.org/wiki/ATI_Rage#Rage_Fury_MAXX "wikilink")、また同社の[RADEON](https://ja.wikipedia.org/wiki/RADEON "wikilink") X850以降で採用された[ATI CrossFireとして利用されている](https://ja.wikipedia.org/wiki/ATI_CrossFire "wikilink")。

## 効果

ATIのCrossFireと同様、GPU2基による並列処理によってグラフィックス性能を高めることができる。対応ソフトウェアにおける平均的な処理速度上昇率はおよそ1.87倍となっている。特に[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") 11、[シェーダーモデル](https://ja.wikipedia.org/wiki/シェーダーモデル "wikilink")5.0となり、今まで以上にリッチなコンテンツが増加しつつある では有用な技術である。また、GTX 460などのGPUでは、本来の2倍以上の処理速度を発揮する場合もある。\[1\]

[ワークステーション](../Page/ワークステーション.md "wikilink")や[サーバ](../Page/サーバ.md "wikilink")の場合には、Quadro Plex（[Quadro](https://ja.wikipedia.org/wiki/Quadro "wikilink")の項参照）を導入することでもSLIを利用できる。

## 応用

SLIの延長技術として、Quad SLIや3-way SLIがある。Quad SLIは、2個のGPUを搭載したデュアルGPUカードを2枚用いてSLI動作させることにより、処理速度がおよそ3.4倍となる。しかし、SLI動作可能なデュアルGPUカードは種類が少なく高価であるため、通常のSLIとQuad SLIの中間技術としてグラフィックスカード3枚で構築できる3-way SLIが考案された。3-way SLIを利用すれば処理速度が最大2.8倍になると謳われている。ただし、対応プラットフォームが数少ないため一般にはあまり普及していない。

### LinkBoostテクノロジー

チップセット「[nForce](https://ja.wikipedia.org/wiki/nForce "wikilink") 590 SLI」搭載マザーボードにおいて「[GeForce](https://ja.wikipedia.org/wiki/GeForce "wikilink") 7900 GTX」でSLIを組むと、ノースブリッジとサウスブリッジ間および[PCI Expressで帯域が](../Page/PCI_Express.md "wikilink")125パーセント（毎秒8GBから10GB）になる\[2\]。

なお、GeForce 8800シリーズ以降はこれをサポートせず、また7900 GTXは生産終了となっているため、2015年現在はこの機能を利用したシステムを新規構築することは難しい。

### Hybrid SLI

**Hybrid SLI**とは2008年に発表された内蔵GPUと外付けGPUでSLIを構築する技術である。ATIのHybrid CrossFireXに相当する。利用するにはこの技術に対応するマザーボードとGPU、[Windows Vista以降のOSが必要である](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")。

Hybrid SLIには2種類の動作モードがある。外付けGPUによっては片方のモードのみしか利用できない。

  - GeForce Boost
    内蔵GPUと外付けGPUでSLIを構築し、性能を上昇させるモード。
  - Hybrid Power
    外付けGPUと内蔵GPUを状況に応じて切り替えることができるモード。これによって省電力化が可能になる。

## 接続方法

SLIによるマルチGPU環境の構成にあたっては、まず複数枚のグラフィックスカードと、それらを挿入できるだけの拡張スロットを有する[マザーボード](../Page/マザーボード.md "wikilink")、そして最新の[デバイスドライバー](https://ja.wikipedia.org/wiki/デバイスドライバー "wikilink")を必要とし、いずれもSLIに対応するものでなければならない。

### 手順

1.  SLI対応[チップセット](../Page/チップセット.md "wikilink")を搭載するマザーボードと、SLIに対応する同一モデルのグラフィックスカードを2つ（または2つ以上）用意する。
2.  マニュアルに従い、グラフィックスカードを[PCI Expressコネクターに接続し](../Page/PCI_Express.md "wikilink")、各カードをブリッジケーブルで接続する。
3.  PCを起動させ、ユーティリティソフト「NVIDIAコントロールパネル」でSLI設定を有効にする。

SLI構成時には電源容量にも配慮する必要がある。SLIに対応した電源ユニット製品には「SLI-Ready」のロゴが記載されている\[3\]が、グラフィックスカードが要求する電力や補助電源仕様に関しては製品ごとに幅があるため、電源ユニット製品が実際に対応しているグラフィックスカード製品に関してもあらかじめ調査しておく必要がある。

なお[Linux](../Page/Linux.md "wikilink")環境にて[X Window Systemを利用している場合](../Page/X_Window_System.md "wikilink")、NVIDIAコントロールパネルのほか、Xサーバー設定ファイルによってSLI設定を変更することもできる\[4\]。

レンダリング方式に関しては、大別してスプリットフレームレンダリング（Split Frame Rendering, SFR）モードと、オルタネートフレームレンダリング（Alternate Frame Rendering, AFR）モードの2つから選択することができる。

## 特徴

  - 基本的に[ノースブリッジ](../Page/ノースブリッジ.md "wikilink")と[サウスブリッジ](../Page/サウスブリッジ.md "wikilink")からの接続なので[PCI Expressレーン数を増やすのが容易な代わり](../Page/PCI_Express.md "wikilink")、[ボトルネック](../Page/ボトルネック.md "wikilink")が発生しやすい（ノースブリッジとサウスブリッジ一体型タイプもある）。
  - NVIDIA製のチップセット以外では基本的に動作しないものであったが、2008年8月28日(日本時間)、NVISION08においてIntel X58 ExpressチップセットでネイティブでのSLI動作をサポートすることを発表した。また、2009年8月10日(米国時間)、NVIDIAはIntelのCore i7、Core i5に対応するP55チップセットを利用したマザーボードにおいてSLI技術に対応する事を可能とするライセンス契約をIntel、その他マザーボードベンダーと結んだと発表した。NVIDIAはSLI対応[サードパーティー](../Page/サードパーティー.md "wikilink")製チップセットの開発を認めていなかったが\[5\]、2011年4月28日にライバルである[AMD](https://ja.wikipedia.org/wiki/AMD "wikilink")の次期チップセットにSLIのライセンスを提供することを発表した\[6\]\[7\]。これにより、一部ではあるがSLI・CrossFire共に「プラットフォーム・チップセットの違いによる制限」は取り払われることになった。これはCore iシリーズ以降のバスライセンス利用の許可がインテルより下りなかったため、自社製チップセットを発売できなくなったためである。
  - 同じメーカーの同じ製品を使用しないと、[フリーズ](../Page/フリーズ.md "wikilink")してしまい、[セーフモード](../Page/セーフモード.md "wikilink")で起動する羽目になる\[8\]。
  - AFRモードではフレームレートを稼ぎやすいが、1フレームの処理時間が短くなるわけではないため、レスポンスの向上は限定的となる (理論値66%～)。4GPUの場合、さらにこの現象が顕著になる (理論値40%～)。
  - SLIではメモリのミラーリングが行なわれるため、たとえば4GBグラフィックスメモリを搭載するカードを2枚使用していても、実際にアプリケーションで利用できるメモリ総量は4GB×2の8GBにはならず、4GBあるいはそれ未満となる。
  - SLIは主にグラフィックスフレームのレンダリングを自動的に分散処理して高速化する技術であり、SLI環境下での[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")分散処理を行なう場合は注意点や制約が存在する\[9\]（NVIDIA GPUにおける[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")はすべて[CUDA](../Page/CUDA.md "wikilink")基盤を利用しているため、このSLI環境における制約は[CUDA](../Page/CUDA.md "wikilink")/[OpenCL](../Page/OpenCL.md "wikilink")/[DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")/[OpenGL](../Page/OpenGL.md "wikilink") Compute Shaderを問わない）。

## 脚注

<references />

## 関連項目

  - [3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")
  - [グラフィックスカード](https://ja.wikipedia.org/wiki/グラフィックスカード "wikilink")
  - [GPU](https://ja.wikipedia.org/wiki/GPU "wikilink")
  - [NVIDIA GeForce](../Page/NVIDIA_GeForce.md "wikilink")
  - [NVIDIA Quadro](../Page/NVIDIA_Quadro.md "wikilink")
  - [AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") [CrossFireX](../Page/CrossFireX.md "wikilink")
  - [Hydra Engine](https://ja.wikipedia.org/wiki/Hydra_Engine "wikilink")

## 外部リンク

  - [NVIDIA公式日本語ウェブサイト](http://www.nvidia.co.jp/page/home.html)
  - [NVIDIA SLI技術 | NVIDIA](http://www.nvidia.co.jp/object/sli-technology-overview-jp.html)
  - [SLIに関するFAQ | NVIDIA](http://www.nvidia.co.jp/object/sli-technology-faq-jp.html)
  - [Hybrid SLI テクノロジ](http://www.nvidia.co.jp/object/hybrid_sli_jp.html)
  - [NVIDIA、Hybrid SLI技術を正式発表](http://pc.watch.impress.co.jp/docs/2008/0108/ces03.htm)

[Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink") [Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink")

1.  GPUの扱うデータに対してメモリ帯域が不足している場合、SLIまたはCrossFireによってそれを隠蔽し本来の性能を発揮できるようになる。具体例は <http://www.4gamer.net/games/099/G009929/20100716100/> 等を参照。
2.  [自作パーツ実験室 (52) LinkBoostとは? SLI Memoryとは? nForce 500シリーズの新機能(1) | マイナビニュース](http://news.mynavi.jp/column/jisakuparts/052/)
3.  [DOS/V POWER REPORT | Impress Japan](http://www.dosv.jp/feature/0804/28.htm)
4.  [Chapter 25. Configuring SLI and Multi-GPU FrameRendering](ftp://download.nvidia.com/XFree86/Linux-x86_64/180.18/README/chapter-25.html)
5.  Intel 5400チップセット搭載のSkulltrailプラットフォームやLGA1336プラットフォーム環境であればSLI動作が可能なのは、[エンスー](https://ja.wikipedia.org/wiki/エンスー "wikilink")向けであり出荷量が少ないことと、nForce 100、200というNVIDIAのブリッジチップを採用しているためであった。
6.  [NVIDIA、AMDの次期チップセット向けにSLIを提供　SLIのライセンスを拡大、AMD 990FX/990X/970でSLIが使用可能に](http://pc.nikkeibp.co.jp/article/news/20110429/1031610/) PCオンライン 2011年4月29日
7.  解放しない理由としては、。しかし、後にNVIDIA自身がチップセット事業を大幅縮小したことで他社に開放する方針に転換した。
8.  ForceWare 81.84β以降のドライバーにより、異なるメーカーでの同一GPUのグラフィックボードによる、SLIでの動作が可能となった。だが、。。
9.  [Programming Guide :: CUDA Toolkit Documentation](http://docs.nvidia.com/cuda/cuda-c-programming-guide/index.html#sli-interoperability)