> この記事は[CrossFireX](https://ja.wikipedia.org/wiki/CrossFireX)から翻訳されています。


[AMD_CrossFireX_Logo.svg](https://ja.wikipedia.org/wiki/File:AMD_CrossFireX_Logo.svg "fig:AMD_CrossFireX_Logo.svg") **CrossFire**（クロスファイア）および**CrossFireX**（クロスファイア エックス）は、[ATI Technologies](../Page/ATI_Technologies.md "wikilink")（現[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")）が[開発](../Page/開発.md "wikilink")した[マルチGPU技術である](../Page/マルチプロセッシング.md "wikilink")。CrossFire/CrossFireX対応[グラフィックスカード](https://ja.wikipedia.org/wiki/グラフィックスカード "wikilink")（[ビデオカード](../Page/ビデオカード.md "wikilink")、[ビデオボード](https://ja.wikipedia.org/wiki/ビデオボード "wikilink")、[グラフィックスボード](https://ja.wikipedia.org/wiki/グラフィックスボード "wikilink")、グラフィックスチップ）を、同一の[マザーボード](../Page/マザーボード.md "wikilink")上に複数枚挿入し、それらを電気的に接続する。複数個の[GPU](https://ja.wikipedia.org/wiki/GPU "wikilink")による[並列処理により](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")、処理能力の大幅な向上が期待できる。[AMD製](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[チップセット](../Page/チップセット.md "wikilink")を搭載したマザーボードに限らず、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")製チップセットを搭載したマザーボードでも構築できる点が大きな特徴といえる。

は最大4個のGPUを並列動作可能なCrossFireXとなっている（GPU2個搭載のデュアルGPUカードは2枚まで、また通常のシングルGPUカードは4枚まで接続可能）。

## 世代

  - CrossFire（第1世代）- 2005年9月27日\[1\]
  - Software CrossFire（第2世代）
  - CrossFireX（第3世代）- 2007年9月19日

## 接続方法

CrossFireによるマルチGPU環境の構成にあたっては、まず複数枚のグラフィックスカードと、それらを挿入できるだけの拡張スロットを有するマザーボード、そして最新の[デバイスドライバー](https://ja.wikipedia.org/wiki/デバイスドライバー "wikilink")を必要とし、いずれもCrossFireに対応するものでなければならない。

### 手順

1.  CrossFire対応[チップセット](../Page/チップセット.md "wikilink")を搭載するマザーボードと、CrossFireに対応する同一モデルのグラフィックスカードを2つ（または2つ以上）用意する。
2.  マニュアルに従い、グラフィックスカードを[PCI Expressコネクターに接続し](../Page/PCI_Express.md "wikilink")、各カードをブリッジケーブルで接続する (Native CrossFire)。[Radeon](https://ja.wikipedia.org/wiki/Radeon "wikilink") X1950 XTX以前にリリースされたモデルの場合、両方をマニュアルに従いPCI Expressコネクターに接続（たいていCPUに近いほうに「CrossFire Edition」を接続）し、そして専用出力コードをつける。
3.  PCを起動させ、ユーティリティソフト「[AMD Catalyst](../Page/AMD_Catalyst.md "wikilink")」でCrossFire設定を有効にする。

[Radeon](https://ja.wikipedia.org/wiki/Radeon "wikilink") HD 2000シリーズ以降は同一モデルを用意すれば構築が可能だが、それ以前に発売されたRadeon X1000シリーズなどは仕組みが複雑で「CrossFire Edition」のもの（こちらのことを「マスター」あるいは「マスターボード」と呼ぶことがある）と、それと同じモデル（例: 「Radeon X1900 CrossFire Edition」なら「Radeon X1900 XTX/XT/PRO」）を用意する必要がある。なお、2007年以降「CrossFire Edition」というラインナップは存在せず、ATI CrossFire、またはATI CrossFireX対応というラインナップで統一された。

なおRadeon R9 290Xには、ブリッジケーブルによる接続が不要となるXDMAが実装されている\[2\]。

## 特徴

  - CrossFire規格はオープン化されているので、ATI製、[AMD製チップセット搭載マザーボードだけでなく](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")、インテル等の他社製チップセットでも構築できる。インテルであれば、intel P965 Express以降、PCI Express×16スロットを2つ以上搭載したマザーボードであれば構築できる（975X、P35、P45、P55、H55、H57、X58など）。。一方NVIDIAは、自社製チップセット（ないしはNVIDIA製のPCI Expressスイッチのようなチップ）を搭載しないマザーボードでの[SLI](https://ja.wikipedia.org/wiki/SLI "wikilink")対応を拒否していたが、2009年8月にはintel X58チップセットに、2011年4月にはAMDの次期チップセット「AMD 9」シリーズの一部にSLIのライセンスを提供することを発表した\[3\]。これにより、一部ではあるがCrossFire・SLI共に「プラットフォーム・チップセットの違いによる制限」は取り払われることになった。
  - 全てのGPUが[ノースブリッジ](../Page/ノースブリッジ.md "wikilink")からの[PCI Express接続なので](../Page/PCI_Express.md "wikilink")[ボトルネック](../Page/ボトルネック.md "wikilink")が発生しにくい。
  - [PCI Expressレーン数を増やすのが難しく](../Page/PCI_Express.md "wikilink")、レーン数8を2つで動かすものが多い。CrossFireに対応し、レーン数16が2つのものにATI CrossFire Xpress 3200、AMD 790FX、intel X38、X48、X58などがある。
  - マルチGPU環境では「交互フレームのレンダリング」と「上下または左右分割のレンダリング」が一般的であるが、CrossFireでは全体を32ピクセル四方のブロックに分けて1つ飛ばしのブロックをレンダリングする方法「SuperTilingモード\[4\]」（分かりやすく言うと[チェス](../Page/チェス.md "wikilink")のフィールドすなわちチェッカーボードの白マス同士あるいは黒マス同士の部分を一度にレンダリングするということ）もサポートする。
  - CrossFire (CrossFireX) ではメモリのミラーリングが行なわれるため、たとえば4GBグラフィックスメモリを搭載するカードを2枚使用していても、実際にアプリケーションで利用できるメモリ総量は4GB×2の8GBにはならず、4GBあるいはそれ未満となる。
  - AMDマルチGPU環境で[OpenCL](../Page/OpenCL.md "wikilink")を利用した[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")分散処理を行なう場合、CrossFire (CrossFireX) をOFFにすることが推奨されている\[5\]。

なお、増設の際は電源ユニットの総電力、12V1、12V2などの仕様も確認が必要である。ので注意が必要となる。

## 派生規格

### Hybrid CrossFire (Hybrid CrossFireX)

グラフィックスカード上のGPUと[AMDチップセット](https://ja.wikipedia.org/wiki/AMDチップセット "wikilink")内蔵GPUを並列処理させる技術\[6\] \[7\] \[8\]。

  - 対応グラフィックスカード
      - Radeon HD 2400 PRO/XT
      - Radeon HD 3450
      - Radeon HD 3470
  - 対応チップセット
      - AMD 790GX
      - AMD 780G
      - AMD 760G
      - AMD 785G
      - AMD 880G
      - AMD 890GX

### AMD Dual Graphics

Hybrid CrossFireXの後継規格。[シェーダー](../Page/シェーダー.md "wikilink")数（ストリームプロセッサ数）の異なるGPUの並列処理が可能になった。

  - 対応チップセット
      - AMD 890GX
  - 対応グラフィックスカード
      - Radeon HD 5450

<!-- end list -->

  - 対応[APU](https://ja.wikipedia.org/wiki/AMD_APU "wikilink") \[9\] \[10\]
      - AMD A4, A6, A8, A10
  - 対応グラフィックスカード \[11\] \[12\]
      - Radeon HD 6450, HD 6570, HD 6670

## 関連項目

  - [3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")
  - [グラフィックスカード](https://ja.wikipedia.org/wiki/グラフィックスカード "wikilink")
  - [GPU](https://ja.wikipedia.org/wiki/GPU "wikilink")
  - [AMD Radeon](../Page/AMD_Radeon.md "wikilink")
  - [AMD FirePro](https://ja.wikipedia.org/wiki/AMD_FirePro "wikilink")
  - [Scalable Link Interface](../Page/Scalable_Link_Interface.md "wikilink") ([NVIDIA](../Page/NVIDIA.md "wikilink") SLI)
  - [Hydra Engine](https://ja.wikipedia.org/wiki/Hydra_Engine "wikilink") (RadeonとGeForceを同期させる技術)

## 脚注

<references />

## 外部リンク

  - [AMD CrossFireX™ 公式サイト](http://sites.amd.com/us/game/technology/Pages/crossfirex.aspx) (英語)
  - [AMD CrossFireX™ 公式サイト](http://sites.amd.com/jp/game/technology/Pages/crossfirex.aspx) (日本語)
  - [AMD Crossfire™ Technology](http://www.amd.com/en-us/innovations/software-technologies/crossfire) (英語)
  - [AMD CrossFire™ FAQ](http://support.amd.com/en-us/kb-articles/Pages/AMDCrossFireFAQ.aspx) (英語)
  - [AMD CrossFire™ Compatibility Chart](http://support.amd.com/en-us/kb-articles/Pages/Crossfire-Chart.aspx) (英語)

<!-- end list -->

  - [4Gamer.net ATI Catalyst 最新記事](http://www.4gamer.net/games/022/G002212/)

[Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink") [Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink")

1.
2.  [「AMD Radeon R9 290X」徹底検証\!\! 新世代ハイエンドRadeonの実力を探る (1) ついに明らかになった"Radeon R9 290X"の詳細 | マイナビニュース](http://news.mynavi.jp/special/2013/290x/)
3.  [NVIDIA、AMDの次期チップセット向けにSLIを提供　SLIのライセンスを拡大、AMD 990FX/990X/970でSLIが使用可能に](http://pc.nikkeibp.co.jp/article/news/20110429/1031610/) PCオンライン 2011年4月29日
4.  [【4Gamer.net】 － 西川善司の3Dゲームエクスタシー:ATIのデュアルチップソリューション「CrossFire」の秘密に迫る](http://www.4gamer.net/specials/3de/050621_crossfire/050621_crossfire.shtml)
5.  [Frequently Asked Questions AMD OpenCL™ Coding Competition : OpenCL Questions : 26. Does the AMD APP SDK v2.4 with OpenCL 1.1 support work on multiple GPUs (ATI CrossFire)?](http://community.topcoder.com/amdapp/faq-2/)
6.  [AMD、内蔵＋外付けGPUのハイブリッドCrossFireをデモ - Engadget Japanese](http://japanese.engadget.com/2007/12/13/amd-gpu-crossfire/)
7.  [Layout 1 - 45689-A-ATI-Hybrid-Gfx-Brochure.pdf](http://www.amd.com/Documents/45689-A-ATI-Hybrid-Gfx-Brochure.pdf)
8.  [ニュース - 効果は抜群、AMD 780GのHybrid CrossFireX：ITpro](http://itpro.nikkeibp.co.jp/article/NEWS/20080307/295718/)
9.  <http://www.amd.com/us/products/technologies/dual-graphics/Pages/dual-graphics.aspx#3>
10. [ASCII.jp：ゲームPCを安く作るならAMD Dual Graphicsを活用すべし！ (1/3)](http://ascii.jp/elem/000/000/626/626734/)
11.
12.