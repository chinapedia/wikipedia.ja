> この記事は[S3 Chrome](https://ja.wikipedia.org/wiki/S3_Chrome)から翻訳されています。


**Chrome**（クローム）は[VIA Technologiesの一部門となった](../Page/VIA_Technologies.md "wikilink")[S3 Graphicsの](../Page/S3_Graphics.md "wikilink")[GPUである](../Page/Graphics_Processing_Unit.md "wikilink")。Savageシリーズの後継にあたり、かつてはディスクリートの[ビデオカード](../Page/ビデオカード.md "wikilink")製品に採用されていた他、各社の[チップセット](../Page/チップセット.md "wikilink")統合グラフィックスコアとしても採用されていた。以下にそれぞれの世代及び製品に分けて解説をする。

[300px](https://ja.wikipedia.org/wiki/ファイル:S3_chrome_s27.jpg "wikilink")

## 概要

**Chromeシリーズ**はS3 Graphics社がリリースするGPU製品のシリーズである。コンシューマ向けとしては主にローエンド～ミドルレンジをターゲットとしており[ノートPC](https://ja.wikipedia.org/wiki/ノートPC "wikilink")向けの製品も存在した。

[Savage](../Page/Savage.md "wikilink")シリーズの後継に該当し、多くの特徴がSavageシリーズから引き継がれている。ネーミングモデルとなる[DeltaChrome](https://ja.wikipedia.org/wiki/DeltaChrome "wikilink")以降のシリーズ共通の特徴として以下が挙げられ、これらは組み込み用に特化されたChrome 4000/5000シリーズ以降でも踏襲されている。

  - 電力あたり性能効率の追求
  - 絶対的な低発熱・低消費電力
  - 高度なHD動画再生機能への積極的な対応
  - DirectXメジャーバージョンへの積極的な対応

単体GPUとしてのChromeシリーズは主にビデオカード用途でリリースされていたが、競合製品と比較してビデオカードメーカーからの採用例は少なかった。しかしノートPCでは2008年に[富士通](../Page/富士通.md "wikilink")の[FMV MGシリーズにてChrome](../Page/FMV.md "wikilink")-BIBLO 430 ULPが採用されている。

また[チップセット統合グラフィックスコアである](../Page/オンボードグラフィック.md "wikilink")**UniChrome**および**Chrome9**はVIA TechnologiesのPC用チップセットで多く搭載されていた。

2014年現在はコンシューマ向けとしては展開しておらず、VIAが主に業務用の[デジタルサイネージ](../Page/デジタルサイネージ.md "wikilink")向けとして提供している組み込み用[Mini-ITX](../Page/Mini-ITX.md "wikilink")[マザーボード](../Page/マザーボード.md "wikilink")用のチップセットの一部として展開されている。

## デスクトップ向けGPU

### Delta Chrome

[thumb](https://ja.wikipedia.org/wiki/ファイル:Powercolor_ss8-d3l_DeltaChrome_S8_256mb_agp.jpg "wikilink") **Delta Chrome**（デルタクローム）は、2003年3月に発表されたGPU。約6,000万個の[トランジスタ](../Page/トランジスタ.md "wikilink")で構成され、130nmプロセスルールで製造される。グラフィックスコアはShaderModel 2.0+の24bit精度[ピクセルシェーダを搭載し](https://ja.wikipedia.org/wiki/プログラマブルシェーダ "wikilink")[DirectX 9に対応しており](https://ja.wikipedia.org/wiki/DirectX "wikilink")、[ビデオメモリは](../Page/VRAM.md "wikilink")128bitで接続された256MBまでの[DDR SDRAMをサポートする](../Page/DDR_SDRAM.md "wikilink")。インターフェースは[AGP 8x](../Page/Accelerated_Graphics_Port.md "wikilink")。

機能面では[コンポーネント出力に対応し](https://ja.wikipedia.org/wiki/高精細度テレビジョン放送 "wikilink")、40bit出力可能な400MHz [RAMDAC](https://ja.wikipedia.org/wiki/RAMDAC "wikilink")の搭載、[MPEG2](https://ja.wikipedia.org/wiki/MPEG2 "wikilink")や[MPEG4](https://ja.wikipedia.org/wiki/MPEG4 "wikilink")に対応した動画アクセラレーション機能**Chromotion**やフォントスムージングアクセラレーション機能**ClearType Font Acceleration**も搭載するなど、2D機能にも力を入れている。

また同世代のGPUと比べ小規模な回路をHighVtトランジスタで構成しているため、消費電力も低く抑えられている。

最上位の"F1"から廉価版の"S4"まで複数のモデルが発表され、モデルによりコア・メモリクロックやサポートするメモリ容量が異なる。日本では"S8"以外に高速版の"S8 Pro"や、"S8"の名前がついているが"S4"の高速版"S8 XE"を搭載した製品が発売された。

#### 主な仕様

  - **Shader Model 2.0+** (8基、S4、S8XEは4基)
  - **Chromotion ビデオエンジン**
  - **ハードウェア頂点シェーダ4基**
  - **AGP 8x**
  - **130nmプロセスルール(TSMC)**
  - **コンポーネントビデオ出力**
  - **Duo Rotate (ハードウェアローテート)**

| ビデオチップ               | コアクロック | メモリクロック | メモリバス  | メモリ種別 |
| -------------------- | ------ | ------- | ------ | ----- |
| DeltaChrome S4 Pro   | 300MHz | 600MHz  | 64bit  | GDDR  |
| DeltaChrome S8 XE    | 350MHz | 500MHz  | 128bit | GDDR  |
| DeltaChrome S8       | 250MHz | 500MHz  | 128bit | GDDR  |
| DeltaChrome S8 Pro   | 300MHz | 600MHz  | 128bit | GDDR  |
| DeltaChrome S8 Nitro | 325MHz | 630MHz  | 128bit | GDDR  |
| DeltaChrome F1       | 300MHz | 600MHz  | 128bit | GDDR  |

### Gamma Chrome

**Gamma Chrome**（ガンマクローム）は、2004年3月に発表されたGPU。インターフェースは[PCI-Express 16xに対応するが](../Page/PCI_Express.md "wikilink")、それ以外の仕様はDeltaChrome S8とほぼ同様である。"Chromotion"はver. 2.0に改良されている。

日本では"S18 Pro"を搭載した製品が発売された。

#### 主な仕様

  - Shader Model 2.0+ (8基、S14のみ4基)
  - **Chromotion 2.0** ビデオエンジン
  - ハードウェア頂点シェーダ4基
  - **PCI Express 16x**
  - 130nmプロセスルール(TSMC)
  - コンポーネントビデオ出力
  - Duo Rotate (ハードウェアローテート)
  - Ultra Low Power configurations (省電力機能)

| ビデオチップ                | コアクロック | メモリクロック | メモリバス  | メモリ種別 |
| --------------------- | ------ | ------- | ------ | ----- |
| GammaChrome S14       | 375MHz | 600MHz  | 64bit  | GDDR  |
| GammaChrome S18 CE    | 300MHz | 600MHz  | 128bit | GDDR  |
| GammaChrome S18 Pro   | 400MHz | 800MHz  | 128bit | GDDR  |
| GammaChrome S18 Nitro | 450MHz | 800MHz  | 128bit | GDDR  |
| GammaChrome S18 Ultra | 500MHz | 900MHz  | 128bit | GDDR  |

### Chrome 20

[thumb](https://ja.wikipedia.org/wiki/ファイル:S3_chrome_s27_pciexpress16x_card.jpg "wikilink") **Chrome 20**シリーズは、2005年11月に発表されたGPU。[富士通](../Page/富士通.md "wikilink")三重Fabの90nmプロセスで製造され、上位のS27と下位のS25が存在する。

グラフィックスコアや機能はDeltaChrome以来の設計を踏襲しているが、[マルチGPU技術](../Page/マルチプロセッシング.md "wikilink")**[MultiChrome](https://ja.wikipedia.org/wiki/#Multi_Chrome "wikilink")**への対応を大きな特徴としており、**Flexible Memory Architecture**による柔軟なメモリ構成も特徴としている。これにより、32～128bitのメモリバスで接続されたGDDR1/GDDR3 32～256MBまたはGDDR2 32～512MBのビデオメモリをサポートする。またS25のみ、メインメモリ領域の一部をVRAMとして利用する**AcceleRAM**機能を搭載する。

**Chromotion 3.0**により[WMV](https://ja.wikipedia.org/wiki/WMV "wikilink")-HDや[MPEG2](https://ja.wikipedia.org/wiki/MPEG2 "wikilink")-HDへの再生支援に対応するなどHD動画コンテンツへの対応も行われている。[HDMI](https://ja.wikipedia.org/wiki/HDMI "wikilink")インターフェースを搭載したS25搭載製品の発売も[XIAiからアナウンスされていたが](../Page/AOpen.md "wikilink")、実際には発売されなかった。

S27はコアクロック700MHzと発表され、最高クロックのGPUであるとされていたが後に650MHzに引き下げられた。06年にマイナーチェンジ版の"S27JE"が発売された他、モバイル向けにLCD表示機能の最適化や省電力機能の追加がされた**Chrome XM20**シリーズもラインナップされている。

#### 主な仕様

  - Shader Model 2.0+ (8基)
  - **Chromotion 3.0** プログラマブルビデオエンジン
  - ハードウェア頂点シェーダ4基
  - PCI Express 16x
  - **90nm**プロセスルール(富士通)
  - コンポーネントビデオ出力
  - Duo Rotate (ハードウェアローテート)
  - **Multi Chrome**
  - **AcceleRAM** (S25のみ)

| ビデオチップ       | コアクロック         | メモリクロック  | メモリバス  | メモリ種別             |
| ------------ | -------------- | -------- | ------ | ----------------- |
| Chrome S25   | 375MHz         | 600MHz   | 64bit  | GDDR1,GDDR2,GDDR3 |
| Chrome S27   | 700MHz, 650MHz | 1.4GHz   | 128bit | GDDR1,GDDR2,GDDR3 |
| Chrome S27JE | (650MHz)       | (1.2GHz) | 128bit | GDDR1,GDDR2,GDDR3 |

### Chrome 400 / 500

[thumb](https://ja.wikipedia.org/wiki/ファイル:S3Graphics_Chrome_440GTX_256MB_PCIE1.0.jpg "wikilink") **Chrome 400**シリーズは2008年2月18日に発表されたGPU。[富士通](../Page/富士通.md "wikilink")[Fab](https://ja.wikipedia.org/wiki/Fab "wikilink")の65nmプロセスルールにより製造され、上位の440と下位の430が存在する。ローエンドデスクトップおよびノートPC市場をターゲットとしており、メモリバスはいずれも64bitとなっている。 DelatChrome以来となるグラフィックスコアの大幅な刷新が行われており、**Shader Model 4.1**に対応し**DirectX 10.1をサポートする**点が最大の特徴である。Microsoftによる[Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") SP1 Premium認証を取得している。また同社製品としては初となる[OpenGL 2.1のサポートをしていたが](../Page/OpenGL.md "wikilink")、後述のChrome 500発表後にリリースされたドライバでOpenGL 3.0への対応も行っている。

また、Chrome 400以降対応のS3 GPGPU用[写真修正](https://ja.wikipedia.org/wiki/写真修正 "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")「S3FotoPro」(無料で利用可能、S3Graphicsのページよりダウンロード)を2008年10月17日(現地時間)発表している。Chrome 400以降であれば、[OpenCL 1.0にも対応しているので](../Page/OpenCL.md "wikilink")、GPGPUとしての利用も可能になっている。

動画再生機能も**Chromotion HD**に強化されており、[Blu-rayビデオおよび](../Page/Blu-ray_Disc.md "wikilink")[H.264](../Page/H.264.md "wikilink")など、各種HDコンテンツに対する再生支援機能が強化されている。なお上位の440は同時に2つのビデオストリームに対する再生支援に対応するが、下位の430では1つのみとなる。

インターフェースは[PCI Express 2.0に対応する](../Page/PCI_Express.md "wikilink")。トランスミッタとオーディオコントローラを統合し[HDMI](https://ja.wikipedia.org/wiki/HDMI "wikilink")出力をネイティブサポートするほか、DVI出力もデュアルリンクに対応し、外部トランスミッタを追加することで[DisplayPort](../Page/DisplayPort.md "wikilink")出力もサポートする。

派生品としてはモバイル向けのChrome 430ULP、435ULPおよび440ULP、組込向けの4300Eが発表されている。

2008年11月20日、**Chrome 500**シリーズが発表された。これはChrome 400をベースにサポートするメモリ容量の強化が行われたマイナーアップデート版であり、**530GT**および**540GTX**ラインナップされている。これが1980年代より続く老舗GPUメーカーであるS3のコンシューマ向け最終製品となる。

#### 主な仕様

[thumb](https://ja.wikipedia.org/wiki/ファイル:S3_Chrome_440GTX_GPU.JPG "wikilink")

  - **Shader Model 4.1** (統合型シェーダー)
  - **ChromotionHD** ビデオテクノロジ
  - **Blu-ray/ HD-DVD 、H.264, VC-1, MPEG2-HD, AVS再生支援**
  - **OpenGL 3.0**サポート　(400発表時は2.1サポートで後に3.0サポート。500は発表時から3.0サポート)
  - **OpenCL 1.0**サポート

<!-- end list -->

  - **AES 128bit暗号化エンジン搭載**
  - '''PCI Express 2.0 16x '''
  - **65nm**プロセスルール
  - Duo Rotate (ハードウェアローテート)
  - Multi Chrome
  - **PowerWise Technology** (省電力機能)
  - **HDMI, デュアルリンクDVI, Display Portサポート**

| ビデオチップ        | コアクロック | メモリクロック | メモリバス | メモリ種別 | メモリ容量 |
| ------------- | ------ | ------- | ----- | ----- | ----- |
| Chrome 430GS  | 525MHz | 800MHz  | 64bit | GDDR2 | 256MB |
| Chrome 430GT  | 625MHz | 1GHz    | 64bit | GDDR2 | 256MB |
| Chrome 440GTX | 725MHz | 1.4GHz  | 64bit | GDDR3 | 256MB |
| Chrome 530GT  | 625MHz | 1GHz    | 64bit | GDDR2 | 512MB |
| Chrome 540GTX | 800MHz | 1.7GHz  | 64bit | GDDR3 | 256MB |

## 統合グラフィックス向け

### UniChrome

[thumb](https://ja.wikipedia.org/wiki/ファイル:Via_k8m800_north_bridge_\(unichrome_pro\).JPG "wikilink") **UniChrome**は[ProSavage-DDRをベースに開発された](https://ja.wikipedia.org/wiki/Savage#ProSavage-DDR "wikilink")[統合チップセット](https://ja.wikipedia.org/wiki/チップセット#統合チップセット "wikilink") (IGP) 用グラフィックスコア。内部的にAGP 8xで接続される128bitグラフィックスコアを持ち、UMAにより64MBまでのメモリをサポートする。[シェーダや](https://ja.wikipedia.org/wiki/プログラマブルシェーダ "wikilink")[ハードウェアT\&L](https://ja.wikipedia.org/wiki/ハードウェアT&L "wikilink")は搭載せず、構成的にはDirectX6世代に相当する。[マルチディスプレイ](https://ja.wikipedia.org/wiki/マルチディスプレイ "wikilink")機能**DuoView**をサポート。VIA TechnologiesのKM400チップセットなどに搭載されている。

UniChromeグラフィックスコアは[2002年](../Page/2002年.md "wikilink")[6月](../Page/6月.md "wikilink")に発表されたCLE266で採用されて以降、マイナーチェンジを重ねながら[2006年](../Page/2006年.md "wikilink")[11月](../Page/11月.md "wikilink")発表のCN800チップセットまで4年半にわたって採用されており、非常に息の長いグラフィックスコアとなった。

#### UniChrome Pro

**UniChrome Pro**はUniChromeのマイナーチェンジ強化版に当たる統合チップセット用グラフィックスコア。UniChromeと比較し、パイプラインを1本から2本に強化しコアクロックを上昇させている。コンポーネントによるHDTV出力に対応し、動画再生機能**Chromotion CE**を搭載するなどHD動画への対応がされている。VIA TechnologiesのK8M800チップセットなどに搭載されている。

#### UniChrome ProII

**UniChrome ProII**はUniChrome Proのマイナーチェンジ強化版に当たる統合チップセット用グラフィックスコア。[WMV](https://ja.wikipedia.org/wiki/WMV "wikilink")-HDの再生支援に対応するなど、HD動画再生機能の強化がされている。VIA TechnologiesのVX700チップセットなどに搭載されている。

#### 主な仕様

  - AGP 8x (内部接続)
  - UMAによる64MBまでのメモリサポート

| IGPコア           | 動作クロック | ピクセルパイプライン | マルチディスプレイ |
| --------------- | ------ | ---------- | --------- |
| UniChrome       | 133MHz | 1          | DuoView   |
| UniChrome Pro   | 200MHz | 2          | DuoView+  |
| UniChrome ProII | －      | 2          | DuoView+  |

### Chrome9 HC

[thumb](https://ja.wikipedia.org/wiki/ファイル:VIA_CN896_NorthBridge.JPG "wikilink") **Chrome9 HC**はDelta Chromeをベースに開発された統合チップセット用グラフィックスコア。128bitのグラフィックスコアを持ち、UMAにより256MBまでのメモリをサポートする。Shader Model 2.0+のProgramable Shaderを搭載し、DirectX 9に正式に対応しており、Microsoftの*Vista Basic*ロゴ認定となっている。表示機能として**Chromotion CE**およびデュアルDVIに対応した**Duo View+**をサポートし、動画再生支援機能としてはMPEG-2デコードおよびビデオデブロッキングに対応する。VIA TechnologiesのK8M890、CN896、P4M900チップセットなどに搭載されている。

#### Chrome9 HC3

**Chrome9 HC3**はChrome9 HCのマイナーチェンジ版に当たる統合チップセット用グラフィックスコア。350MHzの[RAMDAC](https://ja.wikipedia.org/wiki/RAMDAC "wikilink")を3つ搭載し、三画面の出力に対応する他、デュアルリンク[DVI出力および](../Page/Digital_Visual_Interface.md "wikilink")[ビデオキャプチャ](https://ja.wikipedia.org/wiki/ビデオキャプチャ "wikilink")にも対応する。また動画再生支援機能として、MPEG-2、VC1ビデオ デコード アクセラレーションに対応している。VIA TechnologiesのVX800チップセットに搭載されている他、低クロック版がVX800Uチップセットに搭載されている。

#### Chrome9 HCM

**Chrome9 HCM**はChrome9 HC3のマイナーチェンジ版に当たる統合チップセット用グラフィックスコア。主に動画再生支援機能が強化されており、1080pのMPEG-2/H.264 VLDハードウェア デコード アクセラレーションへの対応が追加された。VIA TechnologiesのVX855チップセットに搭載されている。

#### 主な仕様

  - **Shader Model 2.0+**
  - PCI Express 16x (内部接続)

| IGPコア       | 動作クロック          | UMA     | RAMDAC            | Chromotion              |
| ----------- | --------------- | ------- | ----------------- | ----------------------- |
| Chrome9 HC  | 250MHz          | 最大256MB | 2基                | Chromotion CE           |
| Chrome9 HC3 | 250MHz (166MHz) | 最大256MB | 3基 (350MHz/10bit) | Chromotion 3.0          |
| Chrome9 HCM | 非公表             | 最大512MB | 3基 (350MHz/10bit) | Chromotion Video Engine |

### Chrome 4000/5000

**Chrome 4000**および**Chrome 5000**シリーズはChrome 400/500シリーズをベースに組み込み用に再構成したもの。Chrome 400/500シリーズ同様にShaderModel 4.1およびDirectX 10.1をサポートする点が特徴。

  - Chrome 4300
  - Chrome 5300
  - Chrome 5400

### Chrome 600

**Chrome 600**シリーズはS3の統合グラフィックチップとしては初めてDirectX 11に対応した。VIAのMedia System ProcessorであるVX11に搭載されており、主にMini-ITXなどの小型マザーボードやノートPC向けに提供されている。VX11H with HDPCに搭載されているチップにはBlu-rayのデコーディングをサポートしている

  - Chrome 640
  - Chrome 645

## Chromeシリーズの技術

### Chromotion

### Multi Chrome

[NVIDIA](../Page/NVIDIA.md "wikilink")の[SLIや](../Page/Scalable_Link_Interface.md "wikilink")[ATI Technologies](../Page/ATI_Technologies.md "wikilink")（現・[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")）の[CrossFireに類似する](https://ja.wikipedia.org/wiki/CrossFire_\(ATI\) "wikilink")。実装環境は2枚のカードでの構成、及び一枚のカードに2つのGPUを搭載（[Radeon](https://ja.wikipedia.org/wiki/Radeon "wikilink")3000シリーズの「x2」ラインナップと同様の技術）の二つの手法で可能であり、自由度が高いことが特徴である。

Chrome S20シリーズおよびChrome 400シリーズでサポートされている。

S3 Graphicsは"Multi Chrome"に使用するChrome S20搭載カードはビデオメモリを256MB以上搭載していることが望ましいとしている。

## Chromeシリーズの呼称について

"Chrome"は一般に「クロム」と発音される金属[クロム](../Page/クロム.md "wikilink")と同じ[スペリングであるが](../Page/綴り字.md "wikilink")、本シリーズにおいては「クローム」と発音されるのが一般的である。

## 関連項目

  - [Savage](../Page/Savage.md "wikilink")
  - [S3 Graphics](../Page/S3_Graphics.md "wikilink")
  - [VIA Technologies](../Page/VIA_Technologies.md "wikilink")

## 外部リンク

  - [「Chrome 20」シリーズHP](http://www.s3graphics.com/en/products/class2.aspx?seriesId=5)
  - [「Chrome 400」シリーズHP](http://www.s3graphics.com/en/products/class2.aspx?seriesId=1)
  - [「Chrome 500」シリーズHP](http://www.s3graphics.com/en/products/class2.aspx?seriesId=4)
  - [Chrome関連技術文書](http://www.s3graphics.com/en/resources/download-center/index.jsp#whitepapers)
  - [1](http://pc.watch.impress.co.jp/docs/2008/1020/s3.htm) S3GPGPU用[写真修正](https://ja.wikipedia.org/wiki/写真修正 "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")「S3FotoPro」
  - [](http://www.s3graphics.com/en/drivers/software.aspx) S3FotoPro™
  - [2](http://www.s3graphics.com/jp/technologies/tec_dateil.aspx?supportId=34) S3 GPGPU

[Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink")