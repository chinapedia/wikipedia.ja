> この記事は[NVIDIA Quadro](https://ja.wikipedia.org/wiki/NVIDIA_Quadro)から翻訳されています。


**Quadro**（クアドロ）は、[NVIDIA](../Page/NVIDIA.md "wikilink")社のグラフィックス[アクセラレータ](../Page/ハードウェアアクセラレーション.md "wikilink") ([GPU](../Page/Graphics_Processing_Unit.md "wikilink")) の製品群のひとつである。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Quadro_SGI_VPro_VR3.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Quadro_ELSA_GLoria_II_Pro.jpg "wikilink")

## 概要

[thumb](https://ja.wikipedia.org/wiki/ファイル:Quadro2_Pro_ELSA_GLoria_III.jpg "wikilink") [CAD](../Page/CAD.md "wikilink")やプロダクション3DCGのモデリング、医療イメージングなどといった業務用途に設計されており、[OpenGL](../Page/OpenGL.md "wikilink")に最適化されている\[1\] \[2\]。そのため、ゲームアプリケーション向けの[Microsoft DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink") ([Direct3D](../Page/Direct3D.md "wikilink")) に最適化された[GeForce](https://ja.wikipedia.org/wiki/GeForce "wikilink")シリーズと対比される。

GeForceを元に、特に3Dモデリング用途で処理負荷が高くなりがちな、3Dモデルの形状に狂いが出ないよう、ドライバでは処理速度よりも演算精度を重視している。 グラフィックスボード自体の品質は高く故障しにくい。上位製品は[ECCメモリを搭載するものもある](../Page/誤り検出訂正.md "wikilink")。

発売されている製品は「リファレンスボード」と呼ばれるメーカーが指定したハードウェア設計に則って作られている。

現在のCADのベンダーはソフトウェア専業が多く、動作保証はハードウェアベンダーとのアライアンスに基づく。ハードウェアベンダーの意向を踏襲する形でQuadroでの動作を保証するが、GeForceでは動作を保証しない傾向が強い\[3\]。

主な競合製品として、[AMD社の](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[AMD FireProがある](https://ja.wikipedia.org/wiki/AMD_FirePro "wikilink")\[4\] \[5\] \[6\]。

G80コアすなわちDirectX 10世代の[統合型シェーダーアーキテクチャ](https://ja.wikipedia.org/wiki/統合型シェーダーアーキテクチャ "wikilink")を採用した製品以降は[CUDA](../Page/CUDA.md "wikilink")のほか、[OpenCL](../Page/OpenCL.md "wikilink")や[DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")といった[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink") APIにも対応している。Kepler世代以降のQuadroは353.06ドライバーでOpenCL 1.2に正式対応している\[7\]が、それ以前のG80からFermiまではOpenCL 1.1までの対応となる。

OpenGLのバージョンに関しては、Fermi世代以降のQuadroは348.17ドライバーでOpenGL 4.5に正式対応している\[8\] \[9\]。

[Windows 10に搭載されるDirectX](https://ja.wikipedia.org/wiki/Windows_10 "wikilink") 12およびDirectX 11.3に関しては、Keplerアーキテクチャ以降\[10\]においてAPIレベルでサポートされる\[11\]。機能レベル (Feature Level) に関しては、Quadro M6000などのMaxwell第2世代以降でFeature Level 12_0および12_1をフルサポートし、DirectX 11.1、11.2、11.3もフルサポートすることになるが、それ以前の製品でフルサポートが保証されるのはFeature Level 11_0すなわちDirectX 11.0までの機能となる\[12\]。詳しくは[:en:Direct3D](https://ja.wikipedia.org/wiki/:en:Direct3D "wikilink")および[:en:Feature levels in Direct3Dを参照のこと](https://ja.wikipedia.org/wiki/:en:Feature_levels_in_Direct3D "wikilink")。

[Vulkan](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink") 1.0に関しては、Keplerアーキテクチャ以降で対応している\[13\]。

## 型式

[thumb](https://ja.wikipedia.org/wiki/ファイル:NVIDIA_Quadro_DCC_ELSA_GLoria_DCC.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:NVIDIA_Quadro4_980_XGL.jpg "wikilink") 型式は[GeForce](https://ja.wikipedia.org/wiki/GeForce "wikilink")シリーズとは異なり、[OpenGL](../Page/OpenGL.md "wikilink")でのパフォーマンスが高いほど大きな数となるようになっている。このため、数字が大きいほど世代が新しいというわけではない。

2008年11月現在の製品では以下のように分けることができる。

  - クラス
      - [ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink") 4桁
      - [ローエンド](https://ja.wikipedia.org/wiki/ローエンド "wikilink") (エントリー) 3桁
  - 性能指標（上1桁目）
      - 上位 5,4
      - 中位 3
      - 下位 1
  - 同レンジ世代指標（上2桁目）
      - この数字はあくまでも「同レンジ内での世代指標」であり「ここの数字が同じだから同世代」といった見方はできない。
  - X2は2コア（2基、2チップ）を指す

例として、「Quadro FX 4700 X2」は「ハイエンド」の「上位」レンジの「2コア」グラフィックボードとなる。

また、「Quadro FX 4600」は「Quadro FX 4700 X2」の1世代前と見ることができる。

そして「Quadro FX 4700 X2」は「Quadro FX 570」より新しい世代である。

しかし、この数値は近い世代間なら比較できるが、かけ離れた世代間では数値上の逆転が起こることもあるので注意が必要である。

## Quadro Plex

通常のグラフィックスボード製品とは異なり、独立した筐体に電源および2枚のグラフィックスボードや冷却ファンを内蔵する製品で、[PCI Expressに対応したインターフェースボードをホスト側に導入することで利用する](../Page/PCI_Express.md "wikilink")。

ラックマウントで利用することもできる。

  - **Quadro Plex 1000 Model I**
      -
        Quadro FX 5500 2基により構成される。Shader Model 3.0をサポート。
        トータルフレームバッファは2GB(1GB/GPU) 消費電力は最高480W
  - **Quadro Plex 1000 Model II**
      -
        Quadro FX 4500 4基により構成される。Shader Model 3.0をサポート。
        トータルフレームバッファは2GB(512MB/GPU) 消費電力は最高480W
  - **Quadro Plex 1000 Model III**
      -
        Quadro FX 5500 2基により構成される。Shader Model 3.0、HD SDIをサポート。
        トータルフレームバッファは2GB(1GB/GPU) 消費電力は最高480W
  - **Quadro Plex 1000 Model IV**
      -
        Quadro FX 5600 2基により構成される。Shader Model 4.0をサポート。
        トータルフレームバッファは3GB(1.5GB/GPU) 消費電力は最高480W
  - **Quadro Plex 1000 Model S4**
      -
        Quadro FX 5600 4基により構成される。Shader Model 4.0をサポート。
        トータルフレームバッファは6GB(1.5GB/GPU) 消費電力は最高900W
  - **Quadro Plex 2100 Model S4**
      -
        Quadro FX 5600 4基により構成される。Shader Model 4.0をサポート。
        トータルフレームバッファは6GB(1.5GB/GPU) 消費電力は最高900W
  - **Quadro Plex 2100 D2**
      -
        Quadro FX 5800 2基により構成される。Shader Model 4.0をサポート。
        トータルフレームバッファは8GB(4GB/GPU) 消費電力は最高480W
  - **Quadro Plex 2100 D4**
      -
        Quadro FX 4700 4基により構成される。Shader Model 4.0をサポート。
        トータルフレームバッファは4GB(1GB/GPU) 消費電力は最高480W

## Quadro FXシリーズ

[thumb](https://ja.wikipedia.org/wiki/ファイル:NVIDIA_Quadro_FX_1300.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:NVIDIA_Quadro_FX_2000_ES.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:NVIDIA_Quadro_FX_3000_ES.jpg "wikilink")

OpenGLアプリケーションに最適化されたシリーズ。GeForceシリーズ同様、上位モデルでは[SLI](https://ja.wikipedia.org/wiki/SLI "wikilink")に対応する。なお、Fermi世代以降の製品は型番にFXを冠さなくなっている（Quadro 400は除く）。

プロフェッショナル向けの画像処理ソフトウェアや[CAD](../Page/CAD.md "wikilink")ソフトウェア、3DCGソフトウェアにおける各種認証を取得している\[14\] \[15\]。また、10ビット表示（RGB合計30ビット、約10億色）にも対応している\[16\]。

型式末尾"G"はGenLock対応、"SDI"はSDI出力対応を示す。

### NV3xベース

#### NV30(GeForce 5800)ベース

  - **Quadro FX 1000**
      - コア300MHz/600MHz
  - **Quadro FX 2000**
      - コア400MHz、メモリ128MB/128bit/400MHz DDR2。2系統のDVI-I(1系統のみデュアルリンク)。
      - OpenGL 2.0, DirectX 9.0a, Shader Model 2.0a.
      - 消費電力は59W。2スロット仕様。

#### NV34(GeForce FX 5200 Ultra)ベース

  - **Quadro FX 500**
      - コアクロック270MHz、メモリ128MB/128bit/240MHz DDR。DVI-I x1,VGA x1。
      - OpenGL 2.0, DirectX 9.0a, Shader Model 2.0a.
      - 消費電力は11.76W。

<!-- end list -->

  - **Quadro FX 600 PCI**

#### NV35(GeForce 5900)ベース

  - **Quadro FX 700**
      - コア275MHz、メモリ128MB/256bit/(画面のプロパティのクロック周波数の設定でのメモリクロック周波数の表示は1.10GHz) DDR。DVI-I x1,VGA x1。
      - OpenGL 1.5, DirectX 9.0a, Shader Model 2.0a.

<!-- end list -->

  - **Quadro FX 3000**
      - コア400MHz、メモリ256MB/256bit/425MHz DDR。2系統のDVI-I(1系統のみデュアルリンク)。
      - OpenGL 2.0, DirectX 9.0a, Shader Model 2.0a.
      - 消費電力は66.7W。2スロット仕様。

<!-- end list -->

  - [代替文= NVIDIA Quadro FX 3000G](https://ja.wikipedia.org/wiki/ファイル:NVIDIA_Quadro_FX_3000G.jpg "wikilink")**Quadro FX 3000G**\[17\]
      - AGP8X対応
      - Frame lockサポート
          - 複数画像の同期が必要な用途(放送スタジオ編集、Autodesk Smoke,プロジェクションマッピング等)
      - Genlockサポート(House-Syncシグナルコネクタ)
          - VR,3Dステレオ動画ではGenLockで同期しないとずれる\[18\]
      - OpenGLクワッドバッファステレオ（3pin syncコネクタ）

#### NV35(GeForce PCX 5900)ベース

  - **Quadro FX 1300**

#### NV36(GeForce 5700)ベース

  - **Quadro FX 1100**

#### NV37(GeForce PCX 5300)ベース

  - **Quadro FX 330**

### NV4xベース

#### NV40(GeForce 6800)ベース

  - **Quadro FX 3400**
      - コア350MHz、メモリ256MB/256bit/450MHz GDDR3。2系統のDVI-I(1系統のみデュアルリンク)。
      - OpenGL 2.0, DirectX 9, ShaderModel 3.0.
      - 消費電力は68.5W。

[thumb](https://ja.wikipedia.org/wiki/ファイル:NVIDIA_Quadro_FX_4000_AGP.jpg "wikilink")

  - **Quadro FX 4000**
  - **Quadro FX 4000G**
  - **Quadro FX 4000SDI**
  - **Quadro FX 4400**
      - コア415MHz、メモリ512MB/256bit/1050MHz GDDR3。2系統のデュアルリンクDVI。
      - OpenGL 2.0, DirectX 9, ShaderModel 3.0.
      - 消費電力は109W。2スロット仕様。

<!-- end list -->

  - **Quadro FX 4400G**
      -
        NVIDIA G-Sync対応。3スロット仕様。

#### NV41(GeForce 6800)ベース

  - **Quadro FX 1400**
      - コア周波数:350MHz
  - **Quadro FX 3450**
      - コア周波数不明、メモリ256MB/256bit GDDR3。2系統のDVI-I(1系統のみデュアルリンク)。
      - OpenGL 2.0, DirectX 9, ShaderModel 3.0.
      - 消費電力は82W。

#### NV43(GeForce 6600)ベース

  - **Quadro FX 540**
      - コア300MHz、メモリ128MB/128bit/550MHz DDR。DVI-I x1,VGA x1,HDTV x1。
      - OpenGL, DirectX 9, ShaderModel 3.0.
      - 消費電力は35W。
  - **Quadro FX 550**
      - コア360MHz、メモリ128MB/128bit/800MHz GDDR3。2系統のデュアルリンクDVI。
      - OpenGL, DirectX 7/8/9, ShaderModel 3.0.
      - 消費電力は26W。

### G7xベース

#### G70(GeForce 7800GTX)ベース

  - **Quadro FX 4500**
      - コア470MHz、メモリ512MB/256bit/1050MHz GDDR3。2系統のデュアルリンクDVI。
      - OpenGL 2.0, DirectX 9, ShaderModel 3.0.
      - 消費電力は109W。2スロット仕様。

<!-- end list -->

  - **Quadro FX 4500G**
      -
        NVIDIA G-Sync対応。3スロット仕様。

[thumb](https://ja.wikipedia.org/wiki/ファイル:GeForce_7900_GX2_-_GeForce_7900_GTX_Duo.jpg "wikilink")

  - **Quadro FX 4500 X2**
      - コア500MHz\*2(SLI構成)、(1GPUごとに)メモリ512MB/256bit/1200MHz GDDR3。4系統のデュアルリンクDVI。
      - OpenGL 2.0, DirectX 9, ShaderModel 3.0.
      - 消費電力は145.9W、2スロット仕様。
  - **Quadro FX 4500 SDI**
      -
        SDIオプションボード付き。3スロット仕様。

#### G71(GeForce 7900系)ベース

  - **Quadro FX 1500**
      -
        コア325MHz、メモリ256MB/256bit/1250MHz GDDR3。2系統のDVI-I(1系統のみデュアルリンク)。消費電力は65W。
  - **Quadro FX 3500**
      -
        コア450MHz、メモリ256MB/256bit/1320MHz GDDR3。2系統のデュアルリンクDVI。消費電力は80W。
  - **Quadro FX 5500**
      - コア650MHz、メモリ1GB/256bit/1000MHz GDDR2。2系統のデュアルリンクDVI。
      - OpenGL 2.0, DirectX 9, ShaderModel 3.0.
      - 消費電力は109W。2スロット仕様。
  - **Quadro FX 5500G**
      -
        NVIDIA G-Sync対応。3スロット仕様。
  - **Quadro FX 5500SDI**
      -
        SDIオプションボード付き。3スロット仕様。

#### G72(GeForce 7200系)ベース

  - **Quadro FX 350**
      - コア550MHz、メモリ128MB/64bit/810MHz GDDR2。DVI-I+VGA。
      - OpenGL, DirectX 7/8/9 ShaderModel 3.0.
      - 消費電力は30W。

#### G73(GeForce 7600)ベース

  - **Quadro FX 560**
      - コア350MHz、メモリ128MB/128bit/1200MHz GDDR3。2系統のDVI-I(1系統のみデュアルリンク)。
      - OpenGL, DirectX 7/8/9 ShaderModel 3.0.
      - 消費電力は30W。

### G8xベース

#### G80(GeForce 8800 GTS)ベース

  - **Quadro FX 4600**
      - コア500MHz G80、メモリ768MB/384bit/1400MHz GDDR3。2系統のデュアルリンクDVI。
      - OpenGL 3.3, DirectX 10, ShaderModel 4.0, [CUDA](../Page/CUDA.md "wikilink")対応。
      - 消費電力は134W。2スロット仕様。SLI対応。

[thumb](https://ja.wikipedia.org/wiki/ファイル:NVIDIA_P350_A00.jpg "wikilink")

#### G80(GeForce 8800 GTX)ベース

  - **Quadro FX 5600**
      - コア600MHz G80、メモリ1536MB/384bit/1600MHz GDDR3。2系統のデュアルリンクDVI。
      - OpenGL 3.3, DirectX 10, ShaderModel 4.0, [CUDA](../Page/CUDA.md "wikilink")対応。
      - 消費電力は171W。2スロット仕様。SLI対応。

#### G84(GeForce 8600系)ベース

  - **Quadro FX 1700**
      - コア460MHz G84、メモリ512MB/128bit/800MHz DDR2。2系統のデュアルリンクDVI(HDCP対応)。
      - OpenGL 3.3, DirectX 10, ShaderModel 4.0, [CUDA](../Page/CUDA.md "wikilink")対応。
      - 消費電力は42W。

<!-- end list -->

  - **Quadro FX 570**
      - コア460MHz G84、メモリ256MB/128bit/800MHz DDR2。2系統のDVI-I(1系統のみデュアルリンク)。HDCP対応。
      - OpenGL 3.3, DirectX 10, ShaderModel 4.0, [CUDA](../Page/CUDA.md "wikilink")対応。
      - 消費電力は38W。

<!-- end list -->

  - **Quadro FX 370**
      - コア360MHz G84、メモリ256MB/64bit/800MHz DDR2。2系統のDVI-I(1系統のみデュアルリンク)。HDCP対応。
      - OpenGL 3.3, DirectX 10, ShaderModel 4.0, [CUDA](../Page/CUDA.md "wikilink")対応。
      - 消費電力は35W。

### G9xベース

  - **Quadro FX 3700**
      - コア500MHz G92、メモリ512MB/256bit/1600MHz GDDR3。2系統のデュアルリンクDVI。HDCP対応。
      - OpenGL 3.3, DirectX 10, ShaderModel 4.0, [CUDA](../Page/CUDA.md "wikilink")対応。
      - 消費電力は77.9W。SLI対応。
  - **Quadro FX 4700 x2**
      - Quadro FX 4700を2基搭載したカード
      - コア500MHz G92、メモリ2GB（1GB/GPU）/256bit/1600MHz GDDR3。2系統のデュアルリンクDVI。HDCP対応。
      - OpenGL 3.3, DirectX 10, ShaderModel 4.0, [CUDA](../Page/CUDA.md "wikilink")対応。
      - 消費電力は226W。SLI対応。
  - **Quadro FX 1800**
      - コア550MHz G94、メモリ768MB/192bit/1600MHz GDDR3。1系統のデュアルリンクDVI。HDCP対応。
      - OpenGL 3.3, DirectX 10, ShaderModel 4.0, [CUDA](../Page/CUDA.md "wikilink")対応。
      - 消費電力は59W。
  - **Quadro FX 580**
      - コア450MHz G96、メモリ512MB/128bit/1600MHz GDDR3。1系統のデュアルリンクDVI。HDCP対応。
      - OpenGL 3.3, DirectX 10, ShaderModel 4.0, [CUDA](../Page/CUDA.md "wikilink")対応。
      - 消費電力は40W。
  - **Quadro FX 380**
      - コア450MHz G96、メモリ256MB/128bit/1400MHz GDDR3。2系統のデュアルリンクDVI。HDCP対応。
      - OpenGL 3.3, DirectX 10, ShaderModel 4.0, [CUDA](../Page/CUDA.md "wikilink")対応。
      - 消費電力は33.9W。

### GT20xベース

  - **Quadro FX 3800**
      - コア600MHz GT200b、メモリ1GB/256bit/1600MHz GDDR3。1系統のデュアルリンクDVI。HDCP対応。
      - OpenGL 3.3, DirectX 10, ShaderModel 4.0, [CUDA](../Page/CUDA.md "wikilink")対応。
      - 消費電力は108W。SLI対応。
  - **Quadro FX 4800**
      - コア600MHz GT200b、メモリ1.5GB/384bit/1600MHz GDDR3。1系統のデュアルリンクDVI。HDCP対応。
      - OpenGL 3.3, DirectX 10, ShaderModel 4.0, [CUDA](../Page/CUDA.md "wikilink")対応。
      - 消費電力は150.6W。2スロット仕様。SLI対応。
  - **Quadro FX 5800**
      - コア610MHz GT200b、メモリ4GB/512bit/1600MHz GDDR3。2系統のデュアルリンクDVI。HDCP対応。
      - OpenGL 3.3, DirectX 10, ShaderModel 4.0, [CUDA](../Page/CUDA.md "wikilink")対応。
      - 消費電力は187W。2スロット仕様。SLI対応。

### GT2xxベース

  - **Quadro FX 380 LP**
      - コア550MHz GT218、メモリ512MB/64bit/1600MHz DDR3。1系統のデュアルリンクDVI+DisplayPort。HDCP対応。
      - OpenGL 3.3, DirectX 10.1, ShaderModel 4.1, [CUDA](../Page/CUDA.md "wikilink")対応。
      - 消費電力は28W。
  - **Quadro 400**
      - コア450MHz GT216、メモリ512MB/64bit/1540MHz DDR3。1系統のデュアルリンクDVI+DisplayPort。HDCP対応。
      - OpenGL 3.3, DirectX 10.1, ShaderModel 4.1, [CUDA](../Page/CUDA.md "wikilink")対応。
      - 消費電力は32W。

### GF10xベース

#### GF108(GeForce GT 430)ベース

  - **Quadro 600**
      - コア640MHz、メモリ1GB/128bit/1600MHz DDR3。
      - OpenGL 4.3, DirectX 11, ShaderModel 5.0, [CUDA](../Page/CUDA.md "wikilink")対応。1系統のデュアルリンクDVI+DisplayPort。HDCP対応。
      - 消費電力は40W。

#### GF106(GeForce GTS 450)ベース

  - **Quadro 2000**
      - コア625MHz、メモリ1GB/128bit/1300MHz [GDDR5](https://ja.wikipedia.org/wiki/GDDR5 "wikilink")。
      - OpenGL 4.3, DirectX 11, ShaderModel 5.0, [CUDA](../Page/CUDA.md "wikilink")対応。1系統のデュアルリンクDVI+DisplayPort。HDCP対応。
      - 消費電力は62W。

#### GF100(GeForce GTX 465)ベース

  - **Quadro 4000**
      - コア475MHz GF100、メモリ2GB/256bit/1400MHz GDDR5。
      - OpenGL 4.3, DirectX 11, ShaderModel 5.0, [CUDA](../Page/CUDA.md "wikilink")対応。1系統のデュアルリンクDVI+DisplayPort。HDCP対応。
      - 消費電力は142W。SLI対応。

#### GF100(GeForce GTX 470)ベース

  - **Quadro 5000**
      - コア510MHz GF100、メモリ2.5GB/320bit/1500MHz GDDR5。
      - OpenGL 4.3, DirectX 11, ShaderModel 5.0, [CUDA](../Page/CUDA.md "wikilink")対応。1系統のデュアルリンクDVI+DisplayPort。HDCP対応。
      - 消費電力は151.7W。2スロット仕様。SLI対応。

#### GF100(GeForce GTX 480)ベース

  - **Quadro 6000**
      - コア575MHz GF100、メモリ6GB/384bit/1500MHz GDDR5。
      - OpenGL 4.3, DirectX 11, ShaderModel 5.0, [CUDA](../Page/CUDA.md "wikilink")対応。1系統のデュアルリンクDVI+DisplayPort。HDCP対応。
      - 消費電力は225W。2スロット仕様。SLI対応。

### GK1xxベース

#### GK107ベース

  - **Quadro 410** \[19\] \[20\] \[21\] \[22\] \[23\]
      - CUDAコア数192、コア706MHz、メモリ512MB/64bit/891MHz (1782MHzデータレート) DDR3。
      - OpenGL 4.5, DirectX 12 (FL:11_0), ShaderModel 5.0, [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - 1系統のデュアルリンクDVI、DisplayPort 1.2 (×1)。HDCP対応。
      - 消費電力は38W。

<!-- end list -->

  - **Quadro K600** \[24\] \[25\]
      - CUDAコア数192、コア876MHz、メモリ1GB/128bit/891MHz (1782MHzデータレート) DDR3。
      - OpenGL 4.3, DirectX 12 (FL:11_0), ShaderModel 5.0, [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - 1系統のデュアルリンクDVI、DisplayPort 1.2 (×1)。HDCP対応。
      - 消費電力は41W。

<!-- end list -->

  - **Quadro K420** \[26\] \[27\]
      - CUDAコア数192、コア876MHz、メモリ1GB/128bit/891MHz (1782MHzデータレート) DDR3。
      - OpenGL 4.4, DirectX 12 (FL:11_0), ShaderModel 5.0, [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - 1系統のデュアルリンクDVI、DisplayPort 1.2 (×1)。HDCP対応。
      - 消費電力は41W。
      - Quadro K600のリネーム品。

<!-- end list -->

  - **Quadro K2000** \[28\] \[29\]
      - CUDAコア数384、コア954MHz、メモリ2GB/128bit/2000MHz (4000MHzデータレート) GDDR5。
      - OpenGL 4.5, DirectX 12 (FL:11_0), ShaderModel 5.0, [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - 1系統のデュアルリンクDVI、DisplayPort 1.2 (×2)。HDCP対応。
      - 消費電力は51W。

<!-- end list -->

  - **Quadro K2000D** \[30\] \[31\]
      - CUDAコア数384、コア954MHz、メモリ2GB/128bit/2000MHz (4000MHzデータレート) GDDR5。
      - OpenGL 4.5, DirectX 12 (FL:11_0), ShaderModel 5.0, [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - 2系統のデュアルリンクDVI、MiniDisplayPort 1.2 (×1)。HDCP対応。
      - 消費電力は51W。
      - Quadro K2000のディスプレイコネクタ違い品。

#### GK104ベース

  - **Quadro K5000** \[32\] \[33\]
      - CUDAコア数1536、コア706MHz、メモリ4GB/256bit/2700MHz (5400MHzデータレート) GDDR5。
      - OpenGL 4.5, DirectX 12 (FL:11_0), ShaderModel 5.0, [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - 2系統のデュアルリンクDVI、DisplayPort 1.2 (×2)。HDCP対応。
      - ECCサポート。
      - 消費電力は122W。SLI対応。

#### GK110ベース

  - **Quadro K6000** \[34\] \[35\]
      - CUDAコア数2880、コア900MHz、メモリ12GB/384bit/6,008MHz GDDR5。
      - OpenGL 4.5, DirectX 12 (FL:11_0), ShaderModel 5.0, [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - 2系統のデュアルリンクDVI、DisplayPort 1.2 (×2)。HDCP対応。
      - ECCサポート。
      - 消費電力は225W。SLI対応。
  - **Quadro K5200** \[36\] \[37\]
      - CUDAコア数2304、コア650MHz、メモリ8GB/256bit/6,008MHz GDDR5。
      - OpenGL 4.5, DirectX 12 (FL:11_0), ShaderModel 5.0, [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - 2系統のデュアルリンクDVI、DisplayPort 1.2 (×2)。HDCP対応。
      - 消費電力は150W。SLI対応。

### GM1xxベース

#### GM100ベース

#### GM107ベース

  - Quadro K620
      - CUDAコア数364、メモリ２GB／128bit DDR3。
      - OpenGL 4.4、 DirectX 11(Shader Model 5.0) / DirectX 10.1
      - デュアルリンクDVI-I (×1)、DisplayPort 1.2 (×１)。
      - 消費電力は41W。DPI1.2対応でマルチストリームにより最大4画面
  - Quadro K1200
      - CUDAコア数512、メモリ4GB／128bit DDR5。
      - OpenGL 4.4、 DirectX 11(Shader Model 5.0)
      - MiniDisplayPort(×4)(ver.1.2対応)。
      - 消費電力は46W。
  -
### GM2xxベース

#### GM200ベース

  - **Quadro M6000** \[38\] \[39\] \[40\] \[41\]
      - CUDAコア数3072、メモリ12GB/384bit GDDR5。24GB版も存在する。
      - OpenGL 4.5, DirectX 12 (FL:12_1), [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - デュアルリンクDVI-I (×1)、DisplayPort 1.2 (×4)。HDCP対応。
      - ECCサポート。
      - 消費電力は250W。SLI対応。

#### GM204ベース

  - **Quadro M5000** \[42\] \[43\]
      - CUDAコア数2048、メモリ8GB/256bit GDDR5。
      - OpenGL 4.5, DirectX 12 (FL:12_1), [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - デュアルリンクDVI-I (×1)、DisplayPort 1.2 (×4)。HDCP対応。
      - 消費電力は150W。SLI対応。
  - **Quadro M4000** \[44\] \[45\]
      - CUDAコア数1664、メモリ8GB/256bit GDDR5。
      - OpenGL 4.5, DirectX 12 (FL:12_1), [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - DisplayPort 1.2 (×4)。HDCP対応。
      - 消費電力は120W。SLI対応。

#### GM206ベース

  - **Quadro M2000** \[46\] \[47\]
      - CUDAコア数768、メモリ4GB/128bit GDDR5。
      - OpenGL 4.5, DirectX 12 (FL:12_1), [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - DisplayPort 1.2 (×4)。HDCP対応。
      - 消費電力は75W。

### GP1xxベース

#### GP100ベース

  - **Quadro GP100** \[48\] \[49\]
      - CUDAコア数3584、メモリ16GB/4096bit HBM2。
      - OpenGL 4.5, DirectX 12 (FL:12_1), [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - デュアルリンクDVI-D (×1)、DisplayPort 1.4 (×4)。HDCP対応。
      - 消費電力は235W。

#### GP102ベース

  - **Quadro P6000** \[50\] \[51\]
      - CUDAコア数3840、メモリ24GB/384bit GDDR5X。
      - OpenGL 4.5, DirectX 12 (FL:12_1), [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - デュアルリンクDVI-D (×1)、DisplayPort 1.4 (×4)。HDCP対応。
      - 消費電力は250W。

#### GP104ベース

  - **Quadro P5000** \[52\] \[53\]
      - CUDAコア数2560、メモリ16GB/256bit GDDR5X。
      - OpenGL 4.5, DirectX 12 (FL:12_1), [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - デュアルリンクDVI-D (×1)、DisplayPort 1.4 (×4)。HDCP対応。
      - 消費電力は180W。

<!-- end list -->

  - **Quadro P4000** \[54\] \[55\]
      - CUDAコア数1792、メモリ8GB/256bit GDDR5。
      - OpenGL 4.5, DirectX 12 (FL:12_1), [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - DisplayPort 1.4 (×4)。HDCP対応。
      - 消費電力は105W。

#### GP106ベース

  - **Quadro P2000** \[56\] \[57\]
      - CUDAコア数1024、メモリ5GB/160bit GDDR5。
      - OpenGL 4.5, DirectX 12 (FL:12_1), [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - DisplayPort 1.4 (×4)。HDCP対応。
      - 消費電力は75W。

#### GP107ベース

  - **Quadro P1000** \[58\] \[59\]
      - CUDAコア数640、メモリ4GB/128bit GDDR5。
      - OpenGL 4.5, DirectX 12 (FL:12_1), [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - DisplayPort 1.4 (×4)。HDCP対応。
      - 消費電力は47W。

<!-- end list -->

  - **Quadro P620** \[60\] \[61\]
      - CUDAコア数512、メモリ2GB/128bit GDDR5。
      - OpenGL 4.5, DirectX 12 (FL:12_1), [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - Mini DisplayPort 1.4 (×4)。HDCP対応。
      - 消費電力は40W。
  - **Quadro P600** \[62\] \[63\]
      - CUDAコア数384、メモリ2GB/128bit GDDR5。
      - OpenGL 4.5, DirectX 12 (FL:12_1), [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - Mini DisplayPort 1.4 (×4)。HDCP対応。
      - 消費電力は40W。

<!-- end list -->

  - **Quadro P400** \[64\] \[65\]
      - CUDAコア数256、メモリ2GB/64bit GDDR5。
      - OpenGL 4.5, DirectX 12 (FL:12_1), [CUDA](../Page/CUDA.md "wikilink")対応。[OpenCL](../Page/OpenCL.md "wikilink") 1.2。
      - Mini DisplayPort 1.4 (×3)。HDCP対応。
      - 消費電力は30W。

### OpenGLへの最適化

NVIDIA Quadro FXシリーズは、主に[Microsoft DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink") ([Direct3D](../Page/Direct3D.md "wikilink")) に最適化されている同社の3Dゲーム向けグラフィックスカード製品である[NVIDIA GeForceシリーズと比べて](../Page/NVIDIA_GeForce.md "wikilink")、[OpenGL](../Page/OpenGL.md "wikilink")に最適化されている。ハードウェア面でも信頼性・安定性や表示精度を重視した設計がなされているほか、ドライバーソフトウェアも（OpenGL APIが利用されることの多い）[Adobe Photoshop](../Page/Adobe_Photoshop.md "wikilink")、[Autodesk](https://ja.wikipedia.org/wiki/Autodesk "wikilink") [3ds Maxや](../Page/3ds_Max.md "wikilink")[SolidWorks](../Page/SolidWorks.md "wikilink")といったプロフェッショナル向け・業務用途の画像処理ソフトウェア、統合型3DCGソフトウェアやCADソフトウェアに最適化されたものが提供されており、高負荷時のハンドリング性を向上するなど、運用時の安定性を確保できるようになっている\[66\]。

## Quadro FX Mシリーズ

モバイルワークステーション（ノート）に利用されるオンボードタイプのアクセラレータ。ラック積載型のブレード・ワークステーションにも採用される。

### [Centrino](../Page/Centrino.md "wikilink")向け

  - **Quadro FX 350M**
  - **Quadro FX 360M**
  - **Quadro FX 1500M**
  - **Quadro FX 1600M** (HP,IBMのブレード型ワークステーションで搭載される）
  - **Quadro FX 2500M**
  - **Quadro FX 3500M**

### Centrino2向け

OpenGL 2.1, DirectX 10, ShaderModel 4.0, [CUDA](../Page/CUDA.md "wikilink")対応。

  - **Quadro FX 370M**
      - 14.1インチフォームファクタエントリーレベル
      - CUDAプロセッサ 8コア(64bit)、メモリ256MB(9.6GB/秒) GDDR3。
      - TDP 20W。
  - **Quadro FX 770M/1700M**
      - 15.4インチフォームファクタミドルレンジ
      - CUDAプロセッサ 32コア(128bit)、メモリ512MB(25.6GB/秒) GDDR3。
      - TDP 35W/50W。
  - **Quadro FX 2700M/3700M**
      - 17インチフォームファクタハイエンド
      - CUDAプロセッサ 48コア/128コア(256bit)、メモリ512MB/1GB(51.2GB/秒) GDDR3。
      - TDP 65W/75W。

### Calpella向け

OpenGL 3.2, DirectX 10.1, ShaderModel 4.0, CUDA対応。

  - **Quadro FX 380M**
  - **Quadro FX 880M**
  - **Quadro FX 1800M**
  - **Quadro FX 2800M**
  - **Quadro FX 3800M**

## Quadro NVSシリーズ

高いOpenGLパフォーマンスは必要ない、マルチディスプレイユーザー向けの製品シリーズ。金融取引用途に使用される事も多い。FXシリーズにはロープロファイルのフォームファクタがないため、NVSシリーズの一部は省スペースPCに搭載できるQuadroとして利用される。

  - **Quadro NVS 440 PCI-E**
  - **Quadro NVS 440 PCI-E X1**
  - **Quadro NVS 295 PCI-E**
      -
        コアG98(65nm)
  - **Quadro NVS 295 PCI-E X1**
  - **Quadro NVS 290 PCI-E**
      -
        コアG86(80nm) コアクロック400MHz(一部450MHz) SPクロック900MHz メモリクロック800MHz メモリバス幅64bit SP数16。
  - **Quadro NVS 290 PCI-E X1**
  - **Quadro NVS 285 PCI-E**
      -
        Native PCI-E対応となった製品。コアNV44(110nm) コアクロック400MHz 消費電力:17.784W\~Max:22.87W
  - **Quadro NVS 285 PCI-E X1**
  - **Quadro NVS 280 PCI**
      -
        PCIバス対応。PCI-E対応品が登場したことにより、Quadro NVS 280 PCIと呼ばれる。コアクロック350MHz 消費電力:11.41W
  - **Quadro NVS 280 PCI-E**
      -
        Quadro NVS 280をブリッジチップによりPCI-E対応としたもの。
  - **Quadro NVS 280 AGP8X**
  - **Quadro NVS 110M**
  - **Quadro NVS 120M**
  - **Quadro NVS 130M**
  - **Quadro NVS 135M**
  - **Quadro NVS 140M**
  - **Quadro NVS 150M**
  - **Quadro NVS 160M**
  - **Quadro NVS 300M**
  - **Quadro NVS 320M**
  - **Quadro NVS 510M**

### Quadro4 NVSシリーズ

  - **Quadro4 200 NVS**
  - **Quadro4 400 NVS**

### Quadro4 XGLシリーズ

  - **Quadro4 380 XGL**
  - **Quadro4 550 XGL**
  - **Quadro4 580 XGL**
  - **Quadro4 700 XGL**
  - **Quadro4 750 XGL**
  - **Quadro4 900 XGL**
  - **Quadro4 980 XGL**

## Quadro4 Go GLシリーズ

Quadro4のノートPC向けシリーズ。

  - **Quadro4 500 Go GL**
  - **Quadro4 700 Go GL**

## Quadro RTXシリーズ

Turingアーキテクチャを採用することで、リアルタイム レイ トレーシングに対応。\[67\][NVLink](https://ja.wikipedia.org/wiki/NVLink "wikilink")の接続には2つの同じGPUが必要です

| 製品名                                | コア名(nm) | コアクロック | コア数  | メモリ | [FLOPS](../Page/FLOPS.md "wikilink") | [NVNink](https://ja.wikipedia.org/wiki/NVNink "wikilink") | [VR](../Page/バーチャル・リアリティ.md "wikilink") | 消費電力        | 接続          | [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") |
| ---------------------------------- | ------- | ------ | ---- | --- | ------------------------------------ | --------------------------------------------------------- | --------------------------------------- | ----------- | ----------- | ----------------------------------------------------------- |
| [CUDA](../Page/CUDA.md "wikilink") | Tensor  | RT     |      | 容量  | バス幅                                  | 帯域                                                        | 単精度                                     | Tensor      | 帯域 (双方向)    | 対応                                                          |
| Quadro RTX 4000\[68\]              |         |        | 2304 | 288 | 36                                   | GDDR6                                                     | 8GB                                     | 256bit      | 416GB/s     | 7.1 TFLOPS                                                  |
| Quadro RTX 5000\[69\]              |         |        | 3072 | 384 | 48                                   | 16GB                                                      | 448GB/s                                 | 11.2 TFLOPS | 89.2 TFLOPS | 50GB/s                                                      |
| Quadro RTX 6000\[70\]              |         |        | 4608 | 576 | 72                                   | 24GB                                                      | 384bit                                  | 672GB/s     | 16.3 TFLOPS | 130.5 TFLOPS                                                |
| Quadro RTX 8000\[71\]              |         |        | 48GB |     |                                      |                                                           |                                         |             |             |                                                             |

## 脚注

## 関連項目

  - [SLI](https://ja.wikipedia.org/wiki/SLI "wikilink")
  - [NVIDIA GeForce](../Page/NVIDIA_GeForce.md "wikilink")
  - [NVIDIA Tesla](https://ja.wikipedia.org/wiki/NVIDIA_Tesla "wikilink")
  - [AMD FirePro](https://ja.wikipedia.org/wiki/AMD_FirePro "wikilink")

## 外部リンク

  - [Quadro製品情報](http://www.elsa-jp.co.jp/products/index.html)

[Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink") [Category:NVIDIA](https://ja.wikipedia.org/wiki/Category:NVIDIA "wikilink")

1.  [ASCII.jp：NVIDIA Quadroでクリエイターデビューしよう！ (2/3)](http://ascii.jp/elem/000/000/877/877026/index-2.html)
2.  [プロフェッショナル・グラフィックス NVIDIA Quadro シリーズの真骨頂 | 教えて！FRONTIER - パソコン通販・販売・購入ならお任せください ～](http://www.frontier-direct.jp/sp/tutor/quadro_24.html)
3.  [推奨ハードウェア - システム ハードウェアとグラフィックス ハードウェア - Autodesk](http://www.autodesk.co.jp/graphics-hardware)
4.  [実アプリケーションでの性能はQuadroより優秀\!? AMDが「FirePro W」シリーズの説明会で実力をアピール - 4Gamer.net](http://www.4gamer.net/games/133/G013322/20130420010/)
5.  [AMD FirePro](http://www.fireprographics.com/ws/mae/autodesk/index.asp)
6.  [第１回　GPUコンピューティングおよびCUDAについて | G-DEP](http://www.gdep.jp/page/view/248)
7.  [Release 352 Quadro, NVS, Tesla, GRID, & Notebook Drivers - Version 353.06; RN-WQ35306-01_v01 | June 1, 2015; Windows 7, Windows 8, & Windows 8.1; Release Notes](http://us.download.nvidia.com/Windows/Quadro_Certified/353.06/353.06-win8-win7-winvista-quadro-grid-release-notes.pdf)
8.  [OpenGL Driver Support](https://developer.nvidia.com/opengl-driver)
9.  [Release 346 Quadro, NVS, Tesla, GRID, & Notebook Drivers - Version 348.17; RN-WQ34817-01_v01 | May 28, 2015; Windows 7, Windows 8, & Windows 8.1; Release Notes](http://jp.download.nvidia.com/Windows/Quadro_Certified/348.17/348.17-win8-win7-winvista-quadro-grid-release-notes.pdf)
10. Fermiに関しては、Kepler、MaxwellとともにDirectX 12対応することが当初アナウンスされたものの、2017年9月現在でも対応ドライバーが提供されていない。
11. [Maxwell and DirectX 12 Delivered | The Official NVIDIA Blog](http://blogs.nvidia.com/blog/2014/09/19/maxwell-and-dx12-delivered/)
12. [［COMPUTEX］「現行のGeForceが対応するDirectX 12の機能レベル」をNVIDIAが明らかに。VR向けGameWorksもリリース - 4Gamer.net](http://www.4gamer.net/games/274/G027467/20150529001/)
13. [Vulkan Driver Support | NVIDIA Developer](https://developer.nvidia.com/vulkan-driver)
14. [NVIDIA Quadroとは？- 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/html/quadro/contents08.html)
15. [GeForce と Quadro の違い](http://direct.pc-physics.com/geforce-quadro-difference.html)
16. [Quadro × 10bit for Photoshop - 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/html/quadro/contents14.html)
17.
18.
19. [NVIDIA Quadro 410 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/entry_2/quadro_410/)
20. [NVIDIA Quadro 410 512MB Graphics - c04128793.pdf](http://h20195.www2.hp.com/v2/getpdf.aspx/c04128793.pdf)
21. [NVIDIA Quadro Keplerグラフィックスカードにおけるディスプレイ出力の制限 - Lenovo Support (JP)](https://support.lenovo.com/jp/ja/documents/ht076847)
22. [CGiN: NVIDIA Quadro 410](http://cgin.jp/index.php?dispatch=products.view&product_id=2073)
23. [NVIDIA Quadro 410 | techPowerUp GPU Database](http://www.techpowerup.com/gpudb/1316/quadro-410.html)
24. [NVIDIA Quadro K600 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/entry_2/quadro_k600/)
25. [NVIDIA Quadro K600 | techPowerUp GPU Database](https://www.techpowerup.com/gpudb/1839/quadro-k600)
26. [NVIDIA Quadro K420 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/entry_2/quadro_k420/)
27. [NVIDIA Quadro K420 | techPowerUp GPU Database](https://www.techpowerup.com/gpudb/2599/quadro-k420)
28. [NVIDIA Quadro K2000 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/entry_2/quadro_k2000/)
29. [NVIDIA Quadro K2000 | techPowerUp GPU Database](https://www.techpowerup.com/gpudb/1838/quadro-k2000)
30. [NVIDIA Quadro K2000D | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/entry_2/quadro_k2000D/)
31. [NVIDIA Quadro K2000D | techPowerUp GPU Database](https://www.techpowerup.com/gpudb/2021/quadro-k2000d)
32. [NVIDIA Quadro K5000 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/ultra_high_end_2/quadro_k5000/)
33. [4Gamer.net ― NVIDIA，GK104ベースの「Quadro K5000」を発表，第2世代Maximusも](http://www.4gamer.net/games/121/G012181/20120808031/)
34. [NVIDIA Quadro K6000 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/ultra_high_end_2/quadro_k6000/)
35. [NVIDIA，GK110ベースの「Quadro K6000」を発表。史上最多，2880基のシェーダプロセッサを集積 - 4Gamer.net](http://www.4gamer.net/games/121/G012181/20130723005/)
36. [NVIDIA Quadro K5200 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/ultra_high_end_2/quadro_k5200/)
37. [NVIDIA Quadro K5200 8GB Graphics - c04446487.pdf](http://h20195.www2.hp.com/v2/getpdf.aspx/c04446487.pdf)
38. [NVIDIA Quadro M6000 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/ultra_high_end_2/quadro_m6000/)
39. [Data Sheet: Quadro M6000 - NV_DS_Quadro_M6000_FEB15_NV_US_FNL_HR.pdf](http://images.nvidia.com/content/pdf/quadro/data-sheets/NV_DS_Quadro_M6000_FEB15_NV_US_FNL_HR.pdf)
40. [NVIDIA Quadro M6000 12GB Graphics - c04570048.pdf](http://www8.hp.com/h20195/v2/GetPDF.aspx/c04570048.pdf)
41. [NVIDIA Quadro M6000 24GB | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/ultra_high_end_2/quadro_m6000_24gb/)
42. [NVIDIA Quadro M5000 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/ultra_high_end_2/quadro_m5000/)
43. [Data Sheet: Quadro M5000 - 12488_NV_DS_Quadro_M5000_US_NV_Fnl_HR.pdf](http://images.nvidia.com/content/pdf/quadro/data-sheets/12488_NV_DS_Quadro_M5000_US_NV_Fnl_HR.pdf)
44. [NVIDIA Quadro M4000 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/high_end_2/quadro_m4000/)
45. [Data Sheet: Quadro M4000 - 12489_NV_DS_Quadro_M4000_US_NV_FNL_HR.pdf](http://images.nvidia.com/content/pdf/quadro/data-sheets/12489_NV_DS_Quadro_M4000_US_NV_FNL_HR.pdf)
46. [NVIDIA Quadro M2000 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/midrange_2/quadro_m2000/)
47. [Datasheet Quadro M2000 - 38111-DS-NV-Quadro-M2000-Feb16-US-NV-Fnl-HR.pdf](http://images.nvidia.com/content/pdf/quadro/data-sheets/38111-DS-NV-Quadro-M2000-Feb16-US-NV-Fnl-HR.pdf)
48. [NVIDIA Quadro GP100 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/ultra_high_end_2/quadro_gp100/)
49. [Data Sheet: Quadro GP100 - 302049-NV-DS-Quadro-Pascal-GP100-US-NV-27Feb17-HR.pdf](http://images.nvidia.com/content/pdf/quadro/data-sheets/302049-NV-DS-Quadro-Pascal-GP100-US-NV-27Feb17-HR.pdf)
50. [NVIDIA Quadro P6000 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/ultra_high_end_2/quadro_p6000/)
51. [Data Sheet: Quadro P6000 - 192152-NV-DS-Quadro-P6000-US-12Sept-NV-FNL-WEB.pdf](http://images.nvidia.com/content/pdf/quadro/data-sheets/192152-NV-DS-Quadro-P6000-US-12Sept-NV-FNL-WEB.pdf)
52. [NVIDIA Quadro P5000 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/ultra_high_end_2/quadro_p5000/)
53. [Data Sheet: Quadro P5000 - 192195-DS-NV-Quadro-P5000-US-12Sept-NV-FNL-WEB.pdf](http://images.nvidia.com/content/pdf/quadro/data-sheets/192195-DS-NV-Quadro-P5000-US-12Sept-NV-FNL-WEB.pdf)
54. [NVIDIA Quadro P4000 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/high_end_2/quadro_p4000/)
55. [Data Sheet: Quadro P4000 - 301283-DS-NV-Quadro-Pascal-P4000-US-03Feb17-NV-fnl-WEB.pdf](http://images.nvidia.com/content/pdf/quadro/data-sheets/301283-DS-NV-Quadro-Pascal-P4000-US-03Feb17-NV-fnl-WEB.pdf)
56. [NVIDIA Quadro P2000 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/midrange_2/quadro_p2000/)
57. [Datasheet Quadro P2000 - 301941-DS-NV-Quadro-Pascal-P2000-US-03Feb17-NV-fnl-WEB.pdf](http://images.nvidia.com/content/pdf/quadro/data-sheets/301941-DS-NV-Quadro-Pascal-P2000-US-03Feb17-NV-fnl-WEB.pdf)
58. [NVIDIA Quadro P1000 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/midrange_2/quadro_p1000/)
59. [Datasheet Quadro P1000 - 301968-DS-NV-Quadro-Pascal-P1000-US-03Feb17-NV-fnl-WEB.pdf](http://images.nvidia.com/content/pdf/quadro/data-sheets/301968-DS-NV-Quadro-Pascal-P1000-US-03Feb17-NV-fnl-WEB.pdf)
60. [NVIDIA Quadro P600 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/entry_2/quadro_p600/)
61. [Datasheet Quadro P600 - 301995-DS-NV-Quadro-Pascal-P600-US-03Feb17-NV-fnl-WEB.pdf](https://images.nvidia.com/content/pdf/quadro/data-sheets/301995-DS-NV-Quadro-Pascal-P600-US-03Feb17-NV-fnl-WEB.pdf)
62. [NVIDIA Quadro P600 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/entry_2/quadro_p600/)
63. [Datasheet Quadro P600 - 301995-DS-NV-Quadro-Pascal-P600-US-03Feb17-NV-fnl-WEB.pdf](https://images.nvidia.com/content/pdf/quadro/data-sheets/301995-DS-NV-Quadro-Pascal-P600-US-03Feb17-NV-fnl-WEB.pdf)
64. [NVIDIA Quadro P400 | 株式会社 エルザ ジャパン](http://www.elsa-jp.co.jp/products/products-top/graphicsboard_pro/quadro/entry_2/quadro_p400/)
65. [Datasheet Quadro P400 - 302022-DS-NV-Quadro-Pascal-P400-A4-03Feb17-NV-fnl-WEB.pdf](http://images.nvidia.com/content/pdf/quadro/data-sheets/302022-DS-NV-Quadro-Pascal-P400-A4-03Feb17-NV-fnl-WEB.pdf)
66. [「デジタル世界のクリエイター」入門 ～いいマシンを獲得してこそ、よいスタートが切れる！ - Impress Watch](http://www.watch.impress.co.jp/headline/extra/2013/newlife/pc/20130204.html)
67.
68. <https://www.nvidia.com/content/dam/en-zz/Solutions/design-visualization/quadro-product-literature/quadro-rtx-4000-data-sheet-us-nvidia-830682-r6-web.pdf>
69. <https://www.nvidia.com/content/dam/en-zz/ja/Solutions/design-visualization/productspage/quadro/quadro-desktop/quadro-rtx-5000-data-sheet-a4-704120-r4-JP.pdf>
70. <https://www.nvidia.com/content/dam/en-zz/ja/Solutions/design-visualization/productspage/quadro/quadro-desktop/quadro-rtx-6000-a4-nvidia-704093-r4-JP.pdf>
71. <https://www.nvidia.com/content/dam/en-zz/Solutions/design-visualization/quadro-product-literature/quadro-rtx-8000-us-nvidia-946977-r1-web.pdf>