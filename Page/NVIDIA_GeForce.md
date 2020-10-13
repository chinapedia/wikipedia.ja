> この記事は[NVIDIA GeForce](https://ja.wikipedia.org/wiki/NVIDIA_GeForce)から翻訳されています。


**GeForce**（ジーフォース）は、[NVIDIA](../Page/NVIDIA.md "wikilink")社が設計開発している[Graphics Processing Unit](../Page/Graphics_Processing_Unit.md "wikilink") (GPU) の[ブランド](../Page/ブランド.md "wikilink")名である 。

1999年に発表されたGeForce 256を最初に、競合する[アドバンスト・マイクロ・デバイセズ](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") (AMD) の[Radeon](https://ja.wikipedia.org/wiki/Radeon "wikilink")と共に[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")におけるグラフィックス・テクノロジーを先導している。2020年9月現在の主力は、GeForce GTX 16シリーズとGeForce RTX 20・30シリーズである。

## 概要

同社のグラフィックスアクセラレータ製品は『GeForce』シリーズをベースに、[ノートパソコン](../Page/ノートパソコン.md "wikilink")向けに『GeForce M（第7世代まではGeForce Go）』シリーズ、[ワークステーション](../Page/ワークステーション.md "wikilink")向けに[OpenGL](../Page/OpenGL.md "wikilink")処理性能を向上させた『[Quadro](../Page/NVIDIA_Quadro.md "wikilink")』シリーズ、そして[HPC向けに](../Page/高性能計算.md "wikilink")[倍精度浮動小数点](https://ja.wikipedia.org/wiki/倍精度浮動小数点 "wikilink")演算性能の強化や[ECC機構などを搭載した](../Page/誤り検出訂正.md "wikilink")『[Tesla](https://ja.wikipedia.org/wiki/NVIDIA_Tesla "wikilink")』シリーズを展開している。また、モバイル向けに[ARMベースの](../Page/ARMアーキテクチャ.md "wikilink")[CPU](../Page/CPU.md "wikilink")とGeForceベースのGPUを搭載した統合型プロセッサ『[Tegra](https://ja.wikipedia.org/wiki/NVIDIA_Tegra "wikilink")』シリーズを展開している。対応する主なリアルタイム3DグラフィックスAPIは[DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink") ([Direct3D](../Page/Direct3D.md "wikilink")) と[OpenGL](../Page/OpenGL.md "wikilink")だが、主に[DirectXに最適化されている](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")。汎用性や柔軟性を増した[DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink") 10世代の[統合型シェーダーアーキテクチャ](https://ja.wikipedia.org/wiki/統合型シェーダーアーキテクチャ "wikilink") (Unified Shader Architecture) を搭載したGeForce 8シリーズ (G80) \[1\]が発表された2006年以降、NVIDIAはGeForceシリーズのGPUやそれから派生・発展させたチップを使った汎用[コンピューティング](../Page/コンピューティング.md "wikilink")（[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")）のための統合開発環境技術（、[CUDA](../Page/CUDA.md "wikilink")）の開発に注力している。

[Windows 10に搭載される](https://ja.wikipedia.org/wiki/Windows_10 "wikilink")[DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink") 12に関しては、Fermiアーキテクチャ以降においてAPIレベルでサポートされる\[2\]\[3\]。機能レベル (Feature Level) に関しては、GeForce GTX 900シリーズなどのMaxwell第2世代以降でFeature Level 12_0および12_1をフルサポートするが、それ以前のFermi～Maxwell第1世代でフルサポートされるのはFeature Level 11_0すなわち[DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink") 11.0までの機能となる\[4\]。詳しくは[:en:Direct3D](https://ja.wikipedia.org/wiki/:en:Direct3D "wikilink")および[:en:Feature levels in Direct3Dを参照のこと](https://ja.wikipedia.org/wiki/:en:Feature_levels_in_Direct3D "wikilink")。

GeForce 8シリーズ以降は、[CUDA](../Page/CUDA.md "wikilink")\[5\]のほか、[OpenCL](../Page/OpenCL.md "wikilink")や[DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")といったGPGPU APIにも対応している。また、[物理演算](https://ja.wikipedia.org/wiki/物理演算 "wikilink")ライブラリ[PhysX](../Page/PhysX.md "wikilink")\[6\]のハードウェアアクセラレーションにも対応している。

[OpenGL](../Page/OpenGL.md "wikilink")に関しては、Fermiアーキテクチャ以降の388.00ドライバー以降で[OpenGL](../Page/OpenGL.md "wikilink") 4.6に対応している\[7\]。それ以前のGeForce 8シリーズからTeslaアーキテクチャまでは[OpenGL](../Page/OpenGL.md "wikilink") 3.3までの対応となる。

[OpenCL](../Page/OpenCL.md "wikilink")に関しては、Keplerアーキテクチャ以降の350.12ドライバー以降で[OpenCL](../Page/OpenCL.md "wikilink") 1.2に対応している\[8\]。それ以前のGeForce 8シリーズからFermiアーキテクチャまでは[OpenCL](../Page/OpenCL.md "wikilink") 1.1までの対応となる。

DSR (Dynamic Super Resolution) に関しては、Fermiアーキテクチャ以降の344.48ドライバー以降で対応している\[9\]。

ステレオ立体視を可能にする3D Visionに関しては、GeForce 8シリーズ以降の上位製品とFermiアーキテクチャ以降で対応している\[10\]。

[Vulkanに関しては](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink")、Keplerアーキテクチャ以降で[Vulkan](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink") 1.2に対応している\[11\]。

## 命名規則

GeForceシリーズは、その名称からビデオチップの大まかな相対性能を知ることができる。なお同数同指標の製品でも[ベンダー](https://ja.wikipedia.org/wiki/ベンダー "wikilink")によって性能には差違があるので、導入の際には確認が必要である。

### 現行

2008年6月17日発表のGeForce GTX 200シリーズより従来のGeForce4 Tiシリーズから使われていた命名規則が一新され、GeForce 500シリーズからは性能向上に伴い従来のGTSクラスに該当する製品がGTXクラスに吸収された。2009年3月に発表されたリネーム製品であるGeForce 100シリーズにも導入されている。これまでの命名規則では最後に置かれていたモデル内のクラスを表すアルファベットの代わりに、シリーズ内のクラスを表すアルファベットを前に置き、続く3 - 4桁の数字の内、上位から百の位まででシリーズを、末尾2桁と数値05相当の"Ti"付加によってシリーズ内の性能指標(モデル)を表している。7シリーズから20シリーズまでは、従来シリーズでの性能指標95, 90(デュアルチップ)に相当する製品として、命名規則の異なるTITAN(TITAN Zを除きシングルチップ)が存在する。30シリーズは性能指標90のモデルもシングルチップである。2018年からはGTXクラスの上位モデルを置き換える形でRTXクラスも販売されている。

<table>
<thead>
<tr class="header">
<th></th>
<th><p>GPU</p></th>
<th><p>クラス</p></th>
<th><p>シリーズ</p></th>
<th><p>性能指標 (モデル)</p></th>
<th><p>価格の目安</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/ハイエンド" title="wikilink">ハイエンド</a></p></td>
<td><p>デュアル/シングル</p></td>
<td><p>GTX/RTX</p></td>
<td><p>1 - 30, 16</p></td>
<td><p>95, 90</p></td>
<td><p>100,000円 -</p></td>
</tr>
<tr class="even">
<td><p>シングル</p></td>
<td><p>80 Ti, 80 SUPER, 80 (85 - 80)</p></td>
<td><p>60,000 - 150,000円</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ハイクラス</p></td>
<td><p>70 Ti, 70 SUPER, 70 (75 - 70)</p></td>
<td><p>40,000 - 70,000円</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/ミドルレンジ" title="wikilink">ミドルレンジ</a></p></td>
<td><p>60 Ti, 60 SUPER, 60 (65 - 60)</p></td>
<td><p>20,000 - 40,000円</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>50 Ti, 50 SUPER, 50 (55 - 50)</p></td>
<td><p>12,000 - 20,000円</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GTS</p></td>
<td><p>(50 - 40)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ロークラス (エントリークラス)</p></td>
<td><p>GT</p></td>
<td><p>45 - 30</p></td>
<td><p>6,000 - 10,000円</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/ローエンド" title="wikilink">ローエンド</a></p></td>
<td><p>25 - 05</p></td>
<td><p>3,000 - 6,000円</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>(無印)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### 例

| クラス | シリーズ | 性能指標 |
| --- | ---- | ---- |
| GTX | 2    | 60   |

「GTX 260」ならば、200シリーズのミドルレンジモデルとなる。

### 過去

GeForce4 TiシリーズからGeForce 9シリーズまでは、千の位でシリーズを、百と十の位でシリーズ内の性能指標(モデル)を、末尾のアルファベットでモデル内のクラスを表している。

| ハイエンド    | 950 - 800 |
| -------- | --------- |
| メインストリーム | 750 - 600 |
| ローエンド    | 550 - 000 |

性能指標 (モデル)

| 最上位  | Ultra, GX2 |
| ---- | ---------- |
| GTX  |            |
| 上位   | GTS        |
| GT   |            |
| 中位   | GS         |
| （無印） |            |
| 下位   | XT         |
| LE   |            |
| SE   |            |

クラス

#### 例

| シリーズ | 性能指標 (モデル) | クラス |
| ---- | ---------- | --- |
| 9    | 800        | GTX |

「9800 GTX」ならば、9シリーズのハイエンドクラスの最上位モデルとなる。

## 歴代の製品

### デスクトップPC向け

[thumb](https://ja.wikipedia.org/wiki/ファイル:Canopus_GeForce_256_DDR.png "wikilink")

#### GeForce 256

**GeForce 256**は、NVIDIAが開発したGeForceシリーズ初の製品である。1999年8月31日発表。開発コードネームは *NV10*。

同社のビデオチップ製品 [RIVA](https://ja.wikipedia.org/wiki/RIVA "wikilink") シリーズの後継製品で、[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") 7に対応。これまで[CPU](../Page/CPU.md "wikilink") () でソフトウェア的に行なっていたT\&L (、物体の座標変換と陰影計算) 処理を実行する機能（[ハードウェアT\&L](https://ja.wikipedia.org/wiki/ハードウェアT&L "wikilink")）を備えており、NVIDIAはGeForce 256を指して **GPU** () という用語を提唱した。以後、業界全体で[ジオメトリエンジン](https://ja.wikipedia.org/wiki/ジオメトリエンジン "wikilink")搭載の[グラフィックアクセラレータ](../Page/グラフィックアクセラレータ.md "wikilink")をGPUと呼ぶようになった。この製品では、最大128 MBまでのビデオメモリ容量、SDR（*Single Data Rate*、シングルデータレート）の[SDRAM](../Page/SDRAM.md "wikilink")やSGRAM（グラフィクス機能を追加したSDRAM）に対応していたが、後にDDR（*Double-Data-Rate*、ダブルデータレート）に対応した。前世代のハイエンド*RIVA TNT2 Ultra*と比較すると、コアクロックやメモリクロックは低下しているものの、*Riva TNT2*の2倍の4[パイプラインの](../Page/パイプライン処理.md "wikilink")[レンダリングエンジン](https://ja.wikipedia.org/wiki/レンダリングエンジン "wikilink")、二基の[ジオメトリエンジン](https://ja.wikipedia.org/wiki/ジオメトリエンジン "wikilink")を搭載しており、性能が大幅に向上した。また、チップの集積トランジスタ数は2,300万、3D計算能力は50 G[flops](https://ja.wikipedia.org/wiki/flops "wikilink")、製造[プロセスが](https://ja.wikipedia.org/wiki/集積回路#プロセス・ルール "wikilink")0.22 μmとなっている。

当時、最大のライバルであった[3dfx](../Page/3dfx.md "wikilink")に対し、事実上勝利した事を印象づけた製品でもある。

  - GeForce 256［Core:120 MHz Mem:150（SDR版）/ 300 MHz (128bit)］

#### GeForce2 Series

[thumb](https://ja.wikipedia.org/wiki/ファイル:GF2GTS.JPG "wikilink")

##### GeForce2 GTS

**GeForce2 GTS**（ジーフォース・ツー・ジーティーエス）は、GeForceシリーズの第二世代製品である。2000年4月25日発表。開発コードネームは *NV15*。

GeForce 256に改良を加え、[テクセル](https://ja.wikipedia.org/wiki/テクセル "wikilink")フィルレートは1ギガテクセル毎秒を突破（GeForce 256の実に3倍以上を達成）。製品に与えられた *GTS* とは、ギガテクセルシェーダー (<u>G</u>iga <u>T</u>exel <u>S</u>hader) を意味している。後に、GeForce2 GTSのコア、メモリクロックを向上させた **GeForce2 Ultra**（ジーフォース・ツー・ウルトラ）、メモリクロックのみ向上させた *GeForce2 Pro*が発売された。元々、*NV15*は設計段階からメモリクロック400 MHzに対応していたが、GeForce2 GTS発売時にはクロックが333 MHzのメモリしか調達できなかった為、スペック的に制限がかかっていた。製造プロセスは0.18 μm、集積トランジスタ数は2,500万となっている。

| 製品名            | コア名 (プロセス)    | コアクロック | メモリクロック (バス幅）   | PS数 | VS数 | 消費電力 | DirectX | OpenGL               |
| -------------- | ------------- | ------ | --------------- | --- | --- | ---- | ------- | -------------------- |
| GeForce2 GTS   | NV15 (0.18μm) | 200MHz | 333MHz (128bit) |     |     |      | 7       | rowspan="3" 7.0 |1.2 |
| GeForce2 Pro   | NV15 (0.18μm) | 200MHz | 400MHz (128bit) |     |     |      |         |                      |
| GeForce2 Ultra | NV15 (0.18μm) | 250MHz | 460MHz (128bit) |     |     |      |         |                      |

[thumb](https://ja.wikipedia.org/wiki/ファイル:Grafikkarte_NVidia_Geforce2MX_400_ohne_Kuehlkoerper.jpg "wikilink")

##### GeForce2 MX

**GeForce2 MX**（ジーフォース・ツー・エムエックス）（コードネーム*NV11*）は、GeForce2シリーズの廉価製品である。

GeForce 256の製造プロセスルールを0.18 μmに微細化したもの。パイプラインを2つ減らし、メモリバスを半分に抑える事によってコストを抑えている。性能的には前世代のハイエンドグラフィックスカードであるGeForce 256とほぼ同じであり、人気を集めた。派生として*GeForce2 MX 200*と*GeForce2 MX 400*が発売された。*GeForce2 MX*の対応メモリは64か128bitのSDRメモリ、64bitのDDRメモリであるが、*GeForce2 MX 200*は64bitのSDRメモリのみ、*GeForce2 MX 400*は128bitのSDRメモリ、64bitのDDRメモリに対応している。

| 製品名             | コア名 (プロセス)    | コアクロック | メモリクロック （バス幅）      | PS数 | VS数 | 消費電力 | DirectX | OpenGL |
| --------------- | ------------- | ------ | ------------------ | --- | --- | ---- | ------- | ------ |
| GeForce2 MX 200 | NV11 (0.18μm) | 175MHz | 167MHz (64bit,SDR) |     |     |      | 7       | 1.2    |
| GeForce2 MX     | NV11 (0.18μm) | 175MHz | 333MHz (64bit,DDR) |     |     |      |         |        |
| GeForce2 MX 400 | NV11 (0.18μm) | 200MHz | 333MHz (64bit,DDR) |     |     |      |         |        |

##### GeForce2 Ti

**GeForce2 Ti**（ジーフォース・ツー・チタニウム）は、*GeForce3*シリーズ発売後に、*GeForce Titanium*シリーズとして発売された廉価製品である。

*GeForce2 Ultra*を置き換える製品であるが、スペックはメモリクロック以外は同一のものである。性能もメモリクロック低下分だけ落ちる。

| 製品名         | コア名 (プロセス)    | コアクロック | メモリクロック （バス幅）   | PS数 | VS数 | 消費電力 | DirectX | OpenGL |
| ----------- | ------------- | ------ | --------------- | --- | --- | ---- | ------- | ------ |
| GeForce2 Ti | NV15 (0.18μm) | 250MHz | 400MHz (128bit) |     |     |      | 7       | 1.2    |

[thumb](https://ja.wikipedia.org/wiki/ファイル:Canopus_GeForce3_Ti_500.png "wikilink")

#### GeForce3 Series

**GeForce3 Series**（ジーフォース・スリー・シリーズ）は、GeForceシリーズの第三世代製品である。2001年の2月に発表された。開発コードネームは *NV20*。

バーテックスシェーダー・ピクセルシェーダー **nfiniteFX** を搭載し、DirectX 8に対応。最初にGeForce3が発売され、その後*GeForce Titanium*シリーズとして、*GeForce3 Ti 500*、*GeForce3 Ti 200*が発売された。これらはGeForce3のそれぞれ高クロック、低クロック版であり、オーバークロックすることで上位版とほぼ同じ性能となることから、*GeForce3 Ti 200*が人気を集めた。製造プロセスは0.15 μm、集積トランジスタ数は5,700万となっている。

[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[ゲーム機](../Page/ゲーム機.md "wikilink")[XboxにはGeForce](../Page/Xbox_\(ゲーム機\).md "wikilink")3相当のGPUを統合したチップセットが採用されている。

| 製品名             | コア名 (プロセス)    | コアクロック | メモリクロック （バス幅）   | PS数 | VS数 | 消費電力 | DirectX | OpenGL |
| --------------- | ------------- | ------ | --------------- | --- | --- | ---- | ------- | ------ |
| GeForce3 Ti 200 | NV20 (0.15μm) | 175MHz | 400MHz (128bit) |     |     |      | 8.0     | 1.3    |
| GeForce3        | NV20 (0.15μm) | 200MHz | 460MHz (128bit) |     |     |      |         |        |
| GeForce3 Ti 500 | NV20 (0.15μm) | 240MHz | 500MHz (128bit) |     |     |      |         |        |

#### GeForce4 Series

[thumb](https://ja.wikipedia.org/wiki/ファイル:MSI_GeForce4_Ti_4800.png "wikilink")

##### GeForce4 Ti

**GeForce4 Ti**（ジーフォース・フォー・チタニウム）は、GeForceシリーズの第四世代製品である。2002年の2月に発表された。開発コードネームは *NV25*。

GeForce3を大幅に改良した製品であり、[アンチエイリアス](../Page/アンチエイリアス.md "wikilink")機能が強化された。人気[オンラインゲーム](../Page/オンラインゲーム.md "wikilink") ([MMORPG](../Page/MMORPG.md "wikilink"))、[ファイナルファンタジーXI](https://ja.wikipedia.org/wiki/ファイナルファンタジーXI "wikilink")をプレイするために、手頃な価格ながら十分な性能を有していた[ローエンド](https://ja.wikipedia.org/wiki/ローエンド "wikilink")製品 *GeForce4 Ti 4200* に人気が集中した。*GeForce4 Ti 4800*と*GeForce4 Ti 4800 SE*はそれぞれ*GeForce4 Ti 4600*と*GeForce4 Ti 4400*をAGP 8Xに対応させた製品であり、仕様では変化していない。製造プロセスは0.15 μm、集積トランジスタ数は6,300万となっている。

| 製品名                 | コア名 (プロセス)    | コアクロック | メモリクロック （バス幅）       | PS数 | VS数 | 消費電力 | DirectX | OpenGL |
| ------------------- | ------------- | ------ | ------------------- | --- | --- | ---- | ------- | ------ |
| GeForce4 Ti 4200    | NV25 (0.15μm) | 250MHz | 500MHz (128bit,DDR) |     |     |      | 8.1     | 1.3    |
| GeForce4 Ti 4400    | NV25 (0.15μm) | 275MHz | 550MHz (128bit,DDR) |     |     |      |         |        |
| GeForce4 Ti 4600    | NV25 (0.15μm) | 300MHz | 650MHz (128bit,DDR) |     |     |      |         |        |
| GeForce4 Ti 4800 SE | NV25 (0.15μm) | 275MHz | 500MHz (128bit,DDR) |     |     |      |         |        |
| GeForce4 Ti 4800    | NV25 (0.15μm) | 300MHz | 650MHz (128bit,DDR) |     |     |      |         |        |

##### GeForce4 MX

**GeForce4 MX**（ジーフォース・フォー・エムエックス）は、GeForce4世代の廉価版製品である。開発コードネームは *NV17*。

製品名ではGeForce4シリーズの一製品であるが、コードネームはGeForce2 MXのNV11に次ぐものであり、事実上GeForce2 MXの改良版といった位置づけの製品である。GeForce2 MXと比べ、コアクロックとメモリクロックが引き上げられ、メモリバス幅も最大128bitに拡張（一部64bitの製品もある）され、「Lightspeed Memory Architecture II」というGeForce4 Tiシリーズにも採用されているビデオメモリの帯域幅をより効率よく使うための機能を搭載しているため、GeForce2 MXより、およそ倍の性能になっている。また、製造プロセスが0.18 μmから0.15 μmに微細化した事により消費電力や発熱の低減もあった。しかし、GeForce4 Tiシリーズとは違い、DirectX 8の技術の一つであるピクセルシェーダーに対応しておらず、実質的にはDirectX 7世代のカードである。GeForce4 MXシリーズはAGP2.0(4X)対応であったが、AGP3.0(8X)対応の*GeForce4 MX 440 AGP 8X*も販売された。また、メモリチップの容量の対応を増やした、 *GeForce MX 4000*という製品も発売された。この製品の命名規則は他のGeForce4 MXシリーズと異なっており、GeForce4 Tiシリーズの命名規則を当てはめたものと推察できる。

| 製品名                    | コア名 (プロセス)     | コアクロック | メモリクロック （バス幅）       | PS数 | VS数 | 消費電力 | DirectX | OpenGL |
| ---------------------- | -------------- | ------ | ------------------- | --- | --- | ---- | ------- | ------ |
| GeForce4 MX 420        | NV17 (0.15μm)  | 250MHz | 166MHz (128bit,SDR) |     |     |      | 7       | 1.3    |
| GeForce4 MX 440        | NV17 (0.15μm)  | 270MHz | 400MHz (128bit,DDR) |     |     |      |         |        |
| GeForce4 MX 440 AGP 8X | NV18 (0.15μm)  | 270MHz | 500MHz (128bit,DDR) |     |     |      |         |        |
| GeForce4 MX 460        | NV17 (0.15μm)  | 300MHz | 550MHz (128bit,DDR) |     |     |      |         |        |
| GeForce4 MX 4000       | NV18B (0.15μm) | 275MHz | 400MHz (128bit,DDR) |     |     |      |         |        |

#### GeForce FX Series

**GeForce FX Series**（ジーフォース・エフエックス・シリーズ）は、GeForceシリーズの第五世代製品である。発表は2002年の11月である。

第5世代でありながらGeForce5でなくGeForce FXとなっているのは、買収した3dfxの技術が導入されていることによる。ただし、NVIDIAのドライバダウンロードサイトでは、GeForce 5 FXという表記になっている。[VLIW](../Page/VLIW.md "wikilink")のプログラマブルシェーダーを搭載し、DirectX 9に対応。NVIDIA拡張として、DirectX 9.0aとOpenGL 1.5に対応する。

特徴的なデザインとして、ピクセルシェーダーは非常に高いクロックで駆動する1基のみであり、シェーダーの演算結果を出力するROPも全モデルで4本しかない（当時の表現で4ピクセルパイプ）、という点が挙げられる。高速な1機のピクセルシェーダーの演算結果を、4本のROPに順次流し込むというデザインは、シェーダーユニットの動作やバスアクセスタイミングが、全て同時に行われるわけではない点に着目している（CPUでのスーパーパイプライン処理に類似する）。したがって、最上位の5900系から最下位の5200まで、ピクセルパイプとしては全て4本である。最上位のFX 5900/5800系列は、仮想8パイプ相当と公称されているが、この数値が達成されるのは、カラー・Z圧縮が最大限に効いた場合である。

また、DirectX 9.0では、実質的にATIがリファレンスデザインであり、これら、実数バッファ、MRT、テセレータと言った機能は、ATIのGPU自身でも実用には殆ど使われなかったが、実数フォーマットに関しては、FXでもハード的にサポートしているとコメントしつつ、対応ドライバを出す事は無かった。結局、対応したのは、後継製品のGeForce 6が発売された後であり、実数テクスチャのみ対応がなされた。この時期は、NVIDIAの対応が非常に消極的だったため、商品サイクル終了まで、FXは劣勢に立たされたままだった。

商品としては、殆ど良い点が無かったFXであるが、シェーダーリソースの動的な管理、ピクセルシェーダーでのテクスチャの扱いにほぼ制限が無い点、DirectX 10で正式に導入された指数付き整数フォーマット(ERGB)をサポートした、など技術的には見るべき点もあった。

この世代より、GPUの消費電力の増大とともにその冷却手段が課題となっていった。特に、ハイエンドモデル、さらに最初に発売される製品は製造プロセスルールが1世代古いものでハイエンドとして発売されることから、発熱は巨大なものとなっている。その多大な発熱を処理するため、高性能製品には大きな冷却機構を必要とするようになった。なお、5200、5500シリーズが150 nm(0.15 μm)、それ以外の製品では130 nm(0.13 μm)の製造プロセスで生産された。集積トランジスタ数は5200、5500が4,500万、5600、5700が8,000万、5800が1億2,500万、5900、5950が1億3,000万となっている。

Windows XP用のデバイスドライバは、バージョン175.19でサポートが終了した。Windows Vistaに関しては、当初は対応が予定されていたが、RTM版（6000以降）用のバージョン96.85のβドライバが存在するのみ。なお、このVista用βドライバは、パフォーマンスが非常に低く、また細かいバグが残っているが、FXファミリのサポートが終了した為に、更新予定は無い。

また、FXファミリの派生として、PCI Expressバスに対応したGeForce PCXシリーズも2004年2月18日に発表された。これは市場に出た初めてのPCI Express対応ビデオカードであるが、AGPネイティブ対応であるGeForce FXに、PCI Express high-speed interconnect(PCX HSI)と呼ばれるブリッジチップを載せる事でPCI Expressバスに対応したものであり、PCI Expressネイティブ対応はGeForce 6シリーズからになる。

##### GeForce FX 5200

  - GeForce FX 5200 LE \[Core:250 MHz Mem:333 MHz (64bit)\]
  - GeForce FX 5200 \[Core:250 MHz Mem:400 MHz (128bit/64bit)\]
  - GeForce FX 5200 Ultra \[Core:325 MHz Mem:650 MHz (128bit)\]

GeForce FXシリーズのローエンド向けモデル。開発コードネームは *NV34*。新世代GPUであるが、プログラマブルシェーダーを用いない場面での性能の面では前世代のGeForce 4 Ti 4200に劣る。 [thumb](https://ja.wikipedia.org/wiki/ファイル:NVidia_GeForceFX_5500_SX.jpg "wikilink")

##### GeForce FX 5500

  - GeForce FX 5500 \[Core:270 MHz Mem:400 MHz (128bit/64bit)\]

FX 5200の後継で、高クロック化されている。開発コードネームは *NV34*。

##### GeForce FX 5600

  - GeForce FX 5600 XT \[Core:235 MHz Mem:400 MHz (128bit)\]
  - GeForce FX 5600 \[Core:325 MHz Mem:500 MHz (128bit)\]
  - GeForce FX 5600 Ultra \[Core:400 MHz Mem:800 MHz (128bit)\]

GeForce FXシリーズのメインストリーム向けモデル。開発コードネームは *NV31*。

##### GeForce FX 5700

  - GeForce FX 5700 LE \[Core:250 MHz Mem:400 MHz (64bit)\]
  - GeForce FX 5700 \[Core:425 MHz Mem:500 MHz (128bit)\]
  - GeForce FX 5700 Ultra \[Core:475 MHz Mem:900 MHz (128bit)\]

GeForce FX 5600シリーズの後継モデル。実装されている付加機能の関係から、設計そのものは、FX 5900系を下敷きにしているとされる。開発コードネームは *NV36*。

##### GeForce FX 5800

[NVIDIA_GeForce_FX_5800_Ultra_ES.jpg](https://ja.wikipedia.org/wiki/File:NVIDIA_GeForce_FX_5800_Ultra_ES.jpg "fig:NVIDIA_GeForce_FX_5800_Ultra_ES.jpg")

  - GeForce FX 5800 \[Core:400 MHz Mem:800 MHz (128bit)\]
  - GeForce FX 5800 Ultra \[Core:500 MHz Mem:1000 MHz (128bit)\]

GeForce FXシリーズの最初の製品でハイエンド向けモデル。開発コードネームは *NV30*。

これまでにない冷却機構 **FX Flow**（エフエックス・フロー）を搭載していたが、動作音の大きさから不評を買った（アメリカなどでは**ダストバスター**と呼ばれていた）。FX Flowは、拡張ブラケットスペースを2個占有し、シロッコファンを用いて機外より外気を吸入して機外に排出するというもの。ちなみに、FX 5900の発表会ではNVIDIAのスタッフ自らがFX 5800を**ドライヤー**代わりに使ったり、FX 5800の熱をコーヒーやバーベキューに利用したりといった、自虐的なジョークビデオ\[12\]が流された。なお、FX 5900発表後は、NVIDIAのWebからも存在が抹消された。しかしその後、高性能グラフィックスカードで大型ファンを搭載した製品が大半を占めるようになっている。 [thumb](https://ja.wikipedia.org/wiki/ファイル:PixelView_GeForce_FX5900.jpg "wikilink")

##### GeForce FX 5900

  - GeForce FX 5900 XT \[Core:400 MHz Mem:700 MHz (256bit)\]
  - GeForce FX 5900 \[Core:400 MHz Mem:850 MHz (256bit)\]
  - GeForce FX 5900 Ultra \[Core:450 MHz Mem:850 MHz (256bit)\]

GeForce FX 5800シリーズの後継モデル。開発コードネームは *NV35*。

**FX Flow**ではなく、5900シリーズではコアクロックとメモリクロックを下げ、従来の冷却機構に戻している。ただし、GPUの設計がリファインされ、メモリバスの幅が2倍になった事もあり、トータルでの性能は変わらない（ベンチマークでは若干性能が改善されている）。しかし冷却に余裕を持たせる為に隣の拡張スロットにはみ出すような形状のものが多かった。 [thumb](https://ja.wikipedia.org/wiki/ファイル:ASUS_GeForce_FX_5950_Ultra.png "wikilink")

##### GeForce FX 5950

  - GeForce FX 5950 Ultra \[Core:475 MHz Mem:950 MHz (256bit)\]

FX 5900の後継。実質的には、FX 5900の高クロック選別品。開発コードネームは *NV38*。

##### GeForce PCX

  - GeForce PCX 5300 \[Core:250 MHz Mem:400 MHz (128bit)\]
  - GeForce PCX 5750 \[Core:425 MHz Mem:500 MHz (128bit)\]
  - GeForce PCX 5900 \[Core:400 MHz Mem:850 MHz (256bit)\]

PCI Expressに対応したFXファミリ製品。ブリッジチップによる対応である。PCX 5300はFX 5200と同じ*NV37*、PCX 5750はFX 5500と同じ*NV34*、PCX 5900は FX 5900と同じ、*NV35*チップを使用している。

#### GeForce 6 Series

**GeForce 6 Series**（ジーフォース・シックス・シリーズ）は、GeForceシリーズの第六世代製品群である。2004年4月14日発表。

スーパースカラーのプログラマブルシェーダーを搭載し、DirectX 9および拡張版の9.0cに対応。PCI ExpressとAGPの両方に対応するアーキテクチャ。シェーダーを動画再生支援に利用する **[PureVideo](https://ja.wikipedia.org/wiki/PureVideo "wikilink")**（ピュアビデオ）を搭載。PCI Express版のハイエンドモデルには2枚のビデオカードを特殊なブリッジコネクタで直結することで実現する[マルチGPU技術](../Page/マルチプロセッシング.md "wikilink") **[SLI](../Page/Scalable_Link_Interface.md "wikilink")**（エスエルアイ）、ローエンドモデルには[メインメモリの一部を](../Page/主記憶装置.md "wikilink")[VRAM](../Page/VRAM.md "wikilink")として割り当て共有する **[TurboCache](../Page/TurboCache.md "wikilink")**（ターボキャッシュ）が搭載されている。製造プロセスはNV43コア、NV44コアを採用した6200、6500、6600シリーズ、NV42コアを採用した6800 XTは110 nm、それ以外の6800シリーズは130 nmプロセスとなっている。集積トランジスタ数はNV40、NV45コアが2億2,200万、NV41、NV42コアが1億8,600万、NV43コアが1億4,600万、NV44コアが7,700万となっている。NVIDIAはGeForce 6シリーズのアーキテクチャ名をCineFX 3.0としている。

| 製品名                | コア名 (プロセス)          | コアクロック                            | メモリクロック （バス幅）                        | PS数 | VS数 | TC  | SLI | 消費電力 | DirectX | OpenGL |
| ------------------ | ------------------- | --------------------------------- | ------------------------------------ | --- | --- | --- | --- | ---- | ------- | ------ |
| GeForce 6200       | NV43V (110nm)       | 300MHz (300MHz)                   | DDR2 550MHz (128bit)                 | 4   | 3   | ×   | ×   | 22W  | 9.0c    | 2.1    |
| GeForce 6200 TC    | NV44 (110nm)        | 350MHz (350MHz)                   | DDR2 700MHz (64bit)                  | 〇   | 18W |     |     |      |         |        |
| GeForce 6200 A     | NV44A (110nm)       | 300MHz (300MHz)                   | DDR2 500MHz (128bit / 64bit)         | ×   | 23W |     |     |      |         |        |
| GeForce 6500       | NV44 (110nm)        | 400MHz (400MHz)                   | DDR2 666MHz (64bit)                  | 〇   | 24W |     |     |      |         |        |
| GeForce 6600 LE    | NV43 (110nm)        | 425MHz (425MHz)                   | DDR2 500MHz (128bit)                 | ×   | ◯   |     |     |      |         |        |
| GeForce 6600       | 300MHz (300MHz)     | DDR2 500MHz - 550MHz (128bit)     | 8                                    | 28W |     |     |     |      |         |        |
| GeForce 6600 GT    | 500MHz (500MHz)     | GDDR3 1000MHz (128bit)            | 48W                                  |     |     |     |     |      |         |        |
| GeForce 6800 LE    | NV40 / NV41 (130nm) | 325MHz / 300MHz (300MHz)          | DDR2 600MHz / 700MHz (256bit)        | 8   | 4   | ×   |     |      |         |        |
| GeForce 6800 XT    | NV40 / NV41 (130nm) | 300MHz / 425MHz (300MHz / 425MHz) | DDR2 700MHz / GDDR3 1000MHz (256bit) | ◯   |     |     |     |      |         |        |
| NV42 (110nm)       | 450MHz (450MHz)     | GDDR3 1200MHz (256bit)            | 12                                   | 5   |     |     |     |      |         |        |
| GeForce 6800       | NV40 / NV41 (130nm) | 325MHz (325MHz)                   | DDR2 700MHz / 600MHz (256bit)        | 39W |     |     |     |      |         |        |
| GeForce 6800 GTO   | NV40 (130nm)        | 350MHz (350MHz)                   | GDDR3 1000MHz (256bit)               | ×   |     |     |     |      |         |        |
| GeForce 6800 GS    | NV40 / NV41 (130nm) | 350MHz / 425MHz (350MHz / 425MHz) | GDDR3 1000MHz (256bit)               | ◯   | 55W |     |     |      |         |        |
| GeForce 6800 GT    | NV40 / NV45 (130nm) | 350MHz (350MHz)                   | GDDR3 1000MHz (256bit)               | 16  | 6   | 56W |     |      |         |        |
| GeForce 6800 Ultra | NV40 / NV45 (130nm) | 400MHz (400MHz)                   | GDDR3 1100MHz (256bit)               | 72W |     |     |     |      |         |        |

[thumb](https://ja.wikipedia.org/wiki/ファイル:Gigabyte_GV-NX62TC256D8_Rev_1.0.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Gigabyte_GV-NX66T128D_Rev._1.0.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:IMG_3321_6800GT_Top.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:NVIDIA_GeForce_6800_Ultra.png "wikilink")

  - GeForce 6150/GeForce 6100
    AMD向けチップセット、GeForce 6100/[nForce](https://ja.wikipedia.org/wiki/nForce "wikilink") 400シリーズのノースブリッジ。GPU部は6200系のものを使用している。
  - GeForce 6200
    GeForce6シリーズのローエンド向けモデル。それまでのGeForceローエンドチップに比べて3D描画性能が大きく底上げされており、前世代のミドルレンジ並みの性能を発揮する。NVIDIAの公式呼称はいずれもGeForce 6200であるが、3種類のコアがある。
      - GeForce 6200
        当初はローエンド専用モデルが開発されていなかったため、メインストリーム向けモデルであるGeForce 6600(NV43)の機能を一部殺した廉価版のNV43Vコアを投入。PCI Expressネイティブコアであり、AGPにはブリッジで対応。メモリ最大容量は256 MB。
      - Geforce 6200 TC
        NV44コアを使用している。PCI Expressの双方向性を生かし、ビデオメモリを削減してメインメモリで代用することでシステム全体の価格を引き下げるターボキャッシュ（TC）技術を搭載した製品。PCI Express専用。メモリ最大容量は64 MB。
      - GeForce 6200 A
        AGP接続にブリッジを用いないAGPネイティブコアのNV44Aコアを使用している。AGP専用。
  - GeForce 6500
    GeForce 6200 TCの上位に当たるモデル。ターボキャッシュ（TC）技術を搭載している。コアは高速化された *NV44*を使用している。
  - GeForce 6600
    GeForce 6シリーズのメインストリーム向けモデル。SLIに対応している。PCI Expressネイティブコアであり、AGPにはブリッジで対応。開発コードネームは *NV43*。
  - GeForce 6800
    GeForce6シリーズのハイエンド向けモデル。SLIに対応している。UltraとGTとGTOの場合、開発コードネームは *NV40*及びに*NV45*（PCI-E用とAGP用）。い。AGPネイティブコアのAGP対応版、AGPネイティブコアとブリッジチップを並べて実装したPCI Express対応版、PCI Expressネイティブコアが混在する。因みにPCI Expressネイティブコアとされているが、6800系のコアはAGPネイティブコアのNV40に前述したPCX HSIを組み込み、ワンチップ化したものであり（フルスペックのNV45、機能制限したものがNV41、NV41を110 nmプロセスに移行させたものがNV42）、厳密にはPCI Expressネイティブコアではない。PCI-Eスロット対応版のみSLIに対応しており、メーカー独自派生商品としてGeForce 6800 GTを二つ搭載した製品が発売された\[13\]。

{{-}}

#### GeForce 7 Series

**GeForce 7 Series**（ジーフォース・セブン・シリーズ）は、GeForceシリーズの第七世代製品群である。2005年6月22日発表。

GeForce 6シリーズをもとに大幅な改良を施され、ワットあたりの性能が向上した。また、この世代の開発途中から開発コードネームがNV+数字からG+数字に変更されている。製造プロセスは7600、7900シリーズ以降は90 nm、それ以外は110 nmとなっている。集積トランジスタ数はG70（7800シリーズ）は3億200万、G71（7900シリーズ）が2億7,800万、G73（7600シリーズ、7300GT）が1億7,700万、G72（7300、7200シリーズ）が1億1,200万。NVIDIAはGeForce 7シリーズのアーキテクチャ名をCineFX 4.0としている。

| 製品名                  | コア名 (プロセス)             | コアクロック                             | メモリクロック （バス幅）          | PS数       | VS数   | TC   | SLI   | 消費電力 | DirectX | OpenGL |
| -------------------- | ---------------------- | ---------------------------------- | ---------------------- | --------- | ----- | ---- | ----- | ---- | ------- | ------ |
| GeForce 7100 GS      | NV44 (110nm)           | 350MHz (350MHz)                    | DDR2 533MHz (64bit)    | 4         | 3     | 〇    | 2-way | 22W  | 9.0c    | 2.1    |
| GeForce 7200 GS      | G72 (90nm)             | 450MHz (450MHz)                    | DDR2 666MHz (64bit)    | 2         | 2     | ×    | 23W   |      |         |        |
| GeForce 7300 SE      | 4                      | 3                                  |                        |           |       |      |       |      |         |        |
| GeForce 7300 LE      | 8                      | 5                                  |                        |           |       |      |       |      |         |        |
| GeForce 7300 GS      | DDR2 800MHz (64bit)    | 4                                  | 3                      |           |       |      |       |      |         |        |
| GeForce 7300 GT      | G73 (90nm)             | 350MHz (400MHz)                    | DDR2 650MHz (128bit)   | 8         | 4     | ×    | 2-way | 24W  |         |        |
| GeForce 7600 GS      | 400MHz (400MHz)        | DDR2 800MHz (128bit)               | 12                     | 5         | 27W   |      |       |      |         |        |
| GeForce 7600 GT      | 560MHz (560MHz)        | GDDR3 1400MHz (128bit)             | 40W                    |           |       |      |       |      |         |        |
| GeForce 7800 GS AGP  | G70 (110nm)            | 375MHz (375MHz)                    | GDDR3 1200MHz (256bit) | 16        | 8     | 75W  |       |      |         |        |
| GeForce 7800 GT      | 400MHz (400MHz)        | GDDR3 1000MHz (256bit)             | 20                     | 7         | 85W   |      |       |      |         |        |
| GeForce 7800 GTX     | 430MHz (430MHz)        | GDDR3 1200MHz (256bit)             | 24                     | 8         | 110W  |      |       |      |         |        |
| GeForce 7800 GTX 512 | 550MHz (550MHz)        | GDDR3 1700MHz (256bit)             | 120W                   |           |       |      |       |      |         |        |
| GeForce 7900 GS      | G71 (90nm)             | 450MHz (470MHz)                    | GDDR3 1320MHz (256bit) | 20        | 7     | 80W  |       |      |         |        |
| GeForce 7900 GT      | 24                     | 8                                  | 82W                    |           |       |      |       |      |         |        |
| GeForce 7900 GTO     | 650MHz (700MHz)        | 115W                               |                        |           |       |      |       |      |         |        |
| GeForce 7900 GTX     | GDDR3 1600MHz (256bit) | 120W                               |                        |           |       |      |       |      |         |        |
| GeForce 7900 GX2     | 500MHz (500MHz)        | GDDR3 1200MHz (512bit\[256bitx2\]) | 48\[24x2\]             | 16\[8x2\] | Quad  | 150W |       |      |         |        |
| GeForce 7950 GT      | 550MHz (570MHz)        | GDDR3 1400MHz (256bit)             | 24                     | 8         | 2-way | 82W  |       |      |         |        |
| GeForce 7950 GX2     | 500MHz (500MHz)        | GDDR3 1200MHz (512bit\[256bitx2\]) | 48\[24x2\]             | 16\[8x2\] | Quad  | 143W |       |      |         |        |

[thumb](https://ja.wikipedia.org/wiki/ファイル:GeForce_7600_GS.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:GeForce_7900_GX2_-_GeForce_7900_GTX_Duo.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:NVIDIA_GeForce_7950_GX2.png "wikilink")

  - GeForce 7050PV / GeForce 7025
    nForce 630aを統合したAMD向けチップセットのGPU。なお、チップセットはワンチップでできている。[DVI出力にも対応する](../Page/Digital_Visual_Interface.md "wikilink")。GeForce 7050PVはGeForce 7025に比べPure Videoに対応している点、[HDMI](https://ja.wikipedia.org/wiki/HDMI "wikilink")の出力にも対応する点が異なる。
  - 7100 GS
    GeForce 7シリーズで最もローエンドのモデル。内容としてはGeForce 6200と同じものであるが最大256 MBのVRAMとSLIに対応している 。
  - 7200 GS
    2007年5月8日発表。GeForce 7シリーズのローエンド向けモデル。開発コードネームは *G72*。
  - 7300 SE、7300 LE
    2006年3月22日発表。7300 GSのさらに下位モデル。
  - 7300 GS
    2006年1月16日発表。開発コードネームは7200と同じ *G72*。
  - 7300 GT
    2006年5月15日発表。7300 GTはシェーダーの数やメモリ幅が他の7300シリーズと違い比較的性能が高い。これは、7300 GTのみ*G73*のダイを使用している為である。
  - 7600 GS
    2006年3月22日発表。7600 GTの下位モデル。
  - 7600 GT
    2006年3月9日発表。GeForce 7シリーズのメインストリーム向けモデル。開発コードネームは *G73*。
  - 7800 GS AGP
    2006年2月2日発表。AGP対応製品として発表されたが、HSIブリッジチップでの対応である。
  - 7800 GT
    2005年8月12日発表。7800 GTXの機能を削減した製品。チップを二つ載せた製品も発売された\[14\] \[15\]。
  - 7800 GTX
    2005年6月22日発表。この製品の開発コードネームである、G70コアは改名される前に、NV47というコードネームであった。この事からも分かる様に、GeForce 7シリーズはGeForce 6シリーズの改良版である。しかし、様々な部分が改良されており、トランジスタ数で約1億もの機能拡張が行われている。また、アーキテクチャ名がCineFX 4.0、アンチエイリアス機能がIntelliSample 4.0にそれぞれGeForce 6シリーズから一つずつ上がっている。
  - 7800 GTX 512
    2005年11月15日発表。7800 GTXを改良し、より高クロックと512 MBまでのグラフィックスメモリに対応した製品。
    GeForce 7シリーズのハイエンド向けモデル。
  - 7900 GS
    2006年9月6日発表。7900シリーズ最下位製品。他の7900シリーズ製品よりも、バーテックスシェーダー、ピクセルシェーダーが削減されている。
  - 7900 GT
    2006年3月9日発表。7800 GTの後継製品。G71コアを採用した最初の製品。7800 GTXよりも性能が向上している。
  - 7900 GTO
    未発表で限定発売された製品。7900 GTよりも性能が高く、7900 GTXに近い性能だが低価格であり、人気があった。
  - 7900 GTX
    2006年3月9日発表。7800 GTXの後継製品。G71コアを採用した最初の製品。7800 GTXより高クロックで動作するものの、7800 GTX 512よりもメモリクロックは100 MHz低い。
  - 7900 GX2 (7900 GTX Duo)
    どちらもOEM販売のみで、正式には発表されていない。名前が異なるが同じカードである。基板を二枚重ねにした様なカードで、カード毎に6ピン補助電源が必要である。Quad SLIに対応している。
  - 7950 GT
    2006年9月6日発表。G71コアを採用した、GeForce 7900 GTの後継製品。リファレンスレベルで[HDCP](https://ja.wikipedia.org/wiki/HDCP "wikilink")に対応している。
  - 7950 GX2
    2006年6月5日発表。G71コアを二つ搭載したハイエンドモデル。7900 GTXの上位に当たる、GeForce 7000シリーズ最上位製品。Quad SLIに対応している。

{{-}}

#### GeForce 8 Series

**GeForce 8 Series**（ジーフォース・エイト・シリーズ）は、GeForceシリーズの第八世代製品群である。

前世代まで、ピクセルシェーダーとバーテックスシェーダーに分離していたシェーダーユニットは、ストリーミングプロセッサ （Streaming Processor : **SP**）に統合された。この統合型シェーダーユニットの事を「**ユニファイドシェーダー**」と呼ぶ。*G80コア*の8800モデルは動画再生支援機能であるPureVideoが前世代であるGeForce 7シリーズと同じVideoProcessor1 (VP1) のサポートに留まり、*G84コア*や*G86コア*、*G92コア*ではHD動画再生支援を持つPureVideo HDVideoProcessor2 (VP2) がサポートされた。DirectX 10 Shader Model 4.0、Quantum Effects、HDCP（HDCPについてはオプションとなるものもあり）などをサポート。DirectX 10.1のGPUの仮想化は非対応。PCI Express 2.0に対応。

| 製品名              | コア名 (プロセス)       | コアクロック (SPクロック)        | メモリクロック （バス幅）          | SP数 | TC | SLI   | 消費電力 | DirectX | OpenGL |
| ---------------- | ---------------- | ---------------------- | ---------------------- | --- | -- | ----- | ---- | ------- | ------ |
| GeForce 8300 GS  | G86 (80nm)       | 459MHz (918MHz)        | DDR2 800MHz (64bit)    | 8   | 〇  | ×     | 40W  | 10.0    | 3.3    |
| GeForce 8400 GS  | 16               |                        |                        |     |    |       |      |         |        |
| G98 (65nm)       | 567MHz (1400MHz) | 8                      | ×                      | 25W |    |       |      |         |        |
| GT218 (40nm)     | 520MHz (1230MHz) | 16                     | 10.1                   |     |    |       |      |         |        |
| GeForce 8500 GT  | G86 (80nm)       | 450MHz (900MHz)        | DDR2 800MHz (128bit)   | 16  | 〇  | 2-way | 30W  | 10.0    |        |
| GeForce 8600 GT  | G84 (80nm)       | 540MHz (1190MHz)       | GDDR3 1400MHz (128bit) | 32  | ×  | 47W   |      |         |        |
| GeForce 8600 GTS | 675MHz (1450MHz) | GDDR3 2000MHz (128bit) | 60W                    |     |    |       |      |         |        |

  - GeForce 8100/8200
    GeForce 8シリーズをベースにした統合GPUを搭載した[チップセット](../Page/チップセット.md "wikilink")。AMD製CPU向け。GeForce 6・7系のGPU統合型GPUは[nForceと呼ばれたが](https://ja.wikipedia.org/wiki/NVIDIA#nForce "wikilink")、このシリーズからチップセット名もGeForceと呼ばれるようになった。
  - GeForce 8300 GS
    メーカーOEM（組み込み向けモデル）なので個人が手にする機会は少ない。
  - GeForce 8400 GS
    GeForce 8500 GTのメモリバス幅を64bitに削減したもの。Hybrid SLIに対応している。なお、GT218コア（GeForce 210で使用されているものと同じコア）を使用した8400 GSも存在する。コアがGT218のため、DirectX 10.1に対応する。
  - GeForce 8500 GT
    2007年4月17日（日本時間）発表。Hybrid SLIに対応している。
  - GeForce 8600 GT/8600 GTS
    2007年4月17日（日本時間）発表。

[thumb](https://ja.wikipedia.org/wiki/ファイル:NVIDIA_GeForce_8800_Ultra.png "wikilink")

##### G80

| 製品名                     | コア名 (プロセス)       | コアクロック (SPクロック)        | メモリクロック （バス幅）          | SP数                     | SLI                                                       | 消費電力 | DirectX | OpenGL |
| ----------------------- | ---------------- | ---------------------- | ---------------------- | ----------------------- | --------------------------------------------------------- | ---- | ------- | ------ |
| GeForce 8800 GTS 640 MB | G80 (90nm)       | 500MHz (1200MHz)       | GDDR3 1600MHz (320bit) | 96                      | 2-way                                                     | 143W | 10.0    | 3.3    |
| GeForce 8800 GTX        | 575MHz (1350MHz) | GDDR3 1800MHz (384bit) | 128                    | {{Unbulleted list|3-way | 177W <small>(初期ロット)</small>|155W <small>(後期ロット)</small>}} |      |         |        |
| GeForce 8800 Ultra      | 612MHz (1500MHz) | GDDR3 2160MHz (384bit) | 175W                   |                         |                                                           |      |         |        |

  - GeForce 8800 GTS
    2006年11月9日（日本時間）発表。
    メモリバス幅が320bitに削減されている。PCI Express 補助電源コネクタ、SLIコネクタは1系統。2007年2月13日には、グラフィックスメモリを320 MBに削減した廉価モデルが発表、発売された。
  - GeForce 8800 GTX
    2006年11月9日（日本時間）発表。
    GeForce 8800 GTXはGeForce 7900 GTXから動作クロックはあまり向上していないが、GPUに統合型シェーダーユニットを128個内蔵して能力を向上させており、諸々の[ベンチマーク](../Page/ベンチマーク.md "wikilink")ソフトで「7900 GTX」の[SLIを超える結果を出しており](../Page/Scalable_Link_Interface.md "wikilink")、性能が大幅に伸びた。SLIコネクタが2つ備えられており、デイジーチェーンで接続する事で3WAY-SLIに対応する。また、PCI Express補助電源コネクタも2系統接続する。
  - GeForce 8800 Ultra
    2007年5月2日発表。
    GeForce 8800 GTXをより高クロックで動作させたGeForce 8シリーズ最上位製品。GeForce 8800 GTXよりも高クロックながら、コアの最適化により最大消費電力が177 Wから175 Wに若干減少している。しかしリファレンスクーラーはより巨大なものを採用している。クロック以外の仕様は8800 GTXに準ずる。

G80世代において、リファレンスデザインではどれも2スロット占有型の大型ファンを搭載している。

##### G92

| 製品名                     | コア名 (プロセス)       | コアクロック (SPクロック)        | メモリクロック （バス幅）          | SP数  | 消費電力 | SLI   | DirectX | OpenGL |
| ----------------------- | ---------------- | ---------------------- | ---------------------- | ---- | ---- | ----- | ------- | ------ |
| GeForce 8800 GS         | G92 (65nm)       | 550MHz (1375MHz)       | GDDR3 1600MHz (192bit) | 96   | 105W | 2-way | 10.0    | 3.3    |
| GeForce 8800 GT         | 600MHz (1500MHz) | GDDR3 1800MHz (256bit) | 112                    | 125W |      |       |         |        |
| GeForce 8800 GTS 512 MB | 650MHz (1625MHz) | GDDR3 1940MHz (256bit) | 128                    | 135W |      |       |         |        |

2007年11月9日（日本時間）発表。GeForce 8シリーズのハイエンド向けモデル。

開発コードネームは 、8800 GTXなどの初期のモデルは*G80*、8800 GT以降のモデル*G92*とされている。

後発になるGeForce 8800 GTは、65 nmプロセス技術を採用して消費電力を下げたほか、メモリバス幅が256bitに削減され、搭載可能なメモリ量が512 MBに減ったものの、コアクロックとシェーダークロックが向上している（後から1 GB版もリリースされた）。さらに次世代DVDの再生支援などを含むVideo Processor 2が実装されている。性能は同GTXと同GTSの中間ほどで、従来のグレード表記の逆転が起きていた。リファレンスデザインでは、発熱が減ったことで1スロットに収まるファンを搭載している。

また2007年12月には PCI Express 2.0 などに対応した新型 GeForce 8800 GTS 512 MB(G92)が発売され、上記の逆転現象は解消された。

#### GeForce 9 Series

**GeForce 9 Series**（ジーフォース・ナイン・シリーズ）は、GeForceシリーズの第九世代製品群である。DirectX 10.1には対応していない。DX10のアプリケーションが充実していないことやDX10.1の普及がまだ先との判断から実用上問題ないと判断されていた。回路幅が65 nmのものと、55 nmのものがある。また、このシリーズにはGeForce 8シリーズのリネーム品が多い。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック &lt;(SPクロック)</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>SP数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX</p></th>
<th><p>OpenGL</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce 9300</p></td>
<td><p>G86 (80nm)</p></td>
<td><p>450MHz (1200MHz)</p></td>
<td></td>
<td><p>16</p></td>
<td><p>×</p></td>
<td></td>
<td><p>10.0</p></td>
<td><p>3.3</p></td>
</tr>
<tr class="even">
<td><p>GeForce 9400</p></td>
<td><p>G86 (80nm)</p></td>
<td><p>580MHz (1400MHz)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 9300 GS</p></td>
<td></td>
<td><p>567MHz (1400MHz)</p></td>
<td><p>DDR2 1000MHz (64bit)</p></td>
<td><p>35W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 9400 GT</p></td>
<td><p>G86 (80nm)</p></td>
<td><p>459MHz (918MHz)</p></td>
<td><p>DDR2 1200MHz (64bit)</p></td>
<td><p>50W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>550MHz (1400MHz)</p></td>
<td><p>DDR2 800MHz (128bit)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GT218 (40nm)</p></td>
<td><p>589MHz (1402MHz)</p></td>
<td><p>DDR2 1200MHz (64bit)</p></td>
<td><p>10.1</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 9500 GT</p></td>
<td></td>
<td><p>550MHz (1400MHz)</p></td>
<td><p>GDDR3 1600MHz (128bit)</p></td>
<td><p>32</p></td>
<td><p>2-way</p></td>
<td><p>50W</p></td>
<td><p>10.0</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 9600 GSO</p></td>
<td><p>G92 (65nm)</p></td>
<td><p>550MHz (1375MHz)</p></td>
<td><p>GDDR3 1600MHz (192bit)</p></td>
<td><p>96</p></td>
<td><p>105W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 9600 GSO 512</p></td>
<td><p>G94b (55nm)</p></td>
<td><p>650MHz (1625MHz)</p></td>
<td><p>GDDR3 1800MHz (256bit)</p></td>
<td><p>48</p></td>
<td><p>90W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 9600 GT</p></td>
<td><p>G94 (65nm)</p></td>
<td><p>650MHz (1625MHz)</p></td>
<td><p>GDDR3 1800MHz (256bit)</p></td>
<td><p>64</p></td>
<td><p>96W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>G94b (55nm)</p></td>
<td><p>600MHz (1500MHz)</p></td>
<td><p>59W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 9800 GT</p></td>
<td><p>G92 (65nm)</p></td>
<td><p>600MHz (1500MHz)</p></td>
<td><p>GDDR3 1800MHz (256bit)</p></td>
<td><p>112</p></td>
<td><p>105W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>G92b (55nm)</p></td>
<td><p>550MHz (1375MHz)</p></td>
<td><p>66W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 9800 GTX</p></td>
<td><p>G92 (65nm)</p></td>
<td><p>675MHz (1688MHz)</p></td>
<td><p>GDDR3 2200MHz (256bit)</p></td>
<td><p>128</p></td>
<td><p>2/3-way</p></td>
<td><p>140W</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 9800 GTX+</p></td>
<td><p>G92b (55nm)</p></td>
<td><p>738MHz (1836MHz)</p></td>
<td><p>GDDR3 2200MHz (256bit)</p></td>
<td><p>141W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 9800 GX2</p></td>
<td><p>G92 (65nm)</p></td>
<td><p>600MHz (1500MHz)</p></td>
<td><p>GDDR3 2000MHz (512bit[256bitx2])</p></td>
<td><p>256[128x2]</p></td>
<td><p>Quad</p></td>
<td><p>197W</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

  - GeForce 9300/9400
    GeForce 9シリーズの統合GPUを搭載したチップセット。Intel製CPU向け。グラフィックスメモリはメインメモリの一部を利用する、UMA ([Unified Memory Architecture](https://ja.wikipedia.org/wiki/Unified_Memory_Architecture "wikilink")) 方式を採用し、LFB (Local Frame Buffer) の方式はサポートしていない。
  - GeForce 9300 GS
    GeForce 8400GSのリネーム品。G98コアの、55 nm版も流通していると言われている。
  - GeForce 9400 GT
    2008年8月26日（米国時間）発表。GeForce 9シリーズのローエンド向けモデル。補助電源コネクタが搭載されていない。なお、GT218コア（GeForce 210で使用されているものと同じコア）を使用した9400 GTも存在する。コアがGT218のため、DirectX 10.1に対応する。
  - GeForce 9500 GT
    2008年7月29日（米国時間）発表。GeForce 8600 GTの後継とされる、GeForce 9シリーズのバリューモデル。9400 GT同様、補助電源コネクタが搭載されていない。
  - GeForce 9600 GSO
    GeForce 8800 GSと同一のコアを採用し、ほぼ同等のスペックを持つ。9600 GTより下位におかれていたものの、SP数が多いため、条件によっては9600 GTを上回る性能を出すこともある。搭載メモリ量は384/768 MB。
  - GeForce 9600 GSO 512
    NVIDIAからの公式発表はないものの、2008年12月に55 nmプロセスのG94bを採用するマイナーチェンジが行なわれている。型番こそ変更はないものの中身はまったく別物になり、明確に9600 GTの下位におかれるようになった。搭載メモリ量は256/512 MB。
  - GeForce 9600 GT
    2008年2月21日（米国時間）発表。開発コードネームは *G94*。GeForce 9シリーズのメインストリーム向けモデル。対応メモリは[GDDR3](../Page/GDDR3.md "wikilink")。メモリインタフェースが256bitとなり、前シリーズのGeForce 8800 GTに近い性能を出せるようになっている。
  - GeForce 9600 GT (59 W)
    **GeForce 9600 GT Green Edition**とも呼ばれ、GeForce 9600 GTのコアを55 nmにシュリンクしたG94bを搭載し、コアクロックを落とす事で消費電力が59Wまで落ち、補助電源が不要となった製品。
    当初Green Editionとして発表されたが、NVIDIAの製品ページには59 W版として掲載され\[16\]、これを搭載したビデオカードも"9600 GT"の補助電源不要版として発売されている。NVIDIAから公式にはアナウンスはされていないが、ROPユニット数を8基に下げてメモリバス幅が128bitに下げられた仕様の物（いわゆる地雷品）も流通しており\[17\]、中にはパッケージ上では区別が付かない製品もあり、。
  - GeForce 9800GX2
    2008年3月18日（米国時間）発表。GeForce 9シリーズのハイエンド向けモデル。対応メモリは[GDDR3](../Page/GDDR3.md "wikilink")。HybridPower、Hybrid SLI、PureVideo HDに対応。
    GeForce 9800 GX2では単体でのSLI動作が可能なため、SLI非対応のマザーボードでもSLI(2-way)が構築可能。また、Quad SLIに対応し、GX2を2枚使用することで運用可能。Quad SLI時には4つのGPUがそれぞれ1フレームごとにレンダリングする4way-AFRとして動作する。しかし、[Windows Vistaのみで動作し](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")、単体（4枚）と、Quad SLIの切り替えのみとなる。
  - GeForce 9800 GTX
    2008年4月1日（日本時間）発表。GeForce 9シリーズのハイエンド向シングルチップモデル。9800 GTX、同 GX2はG92コアであり、特にGTXはGeForce 8800 GTS(G92)のクロックアップ版に近く（3-Way SLIに対応しており、ただのクロックアップ版ではない）、GeForce 8800 GTX、同 Ultraに性能で劣る場面がある。
  - GeForce 9800 GTX+
    2008年6月19日（米国時間）発表。日本では7月26日発売。9800 GTXを55 nmにシュリンクしたG92bコアを採用し、その分クロックを増やして性能を上げている。また、ベンダーによっては6ピン仕様のPCI Express補助電源コネクタが一つだけのマイナーチェンジ版が存在する。Hybrid SLIに対応。
  - GeForce 9800 GT
    2008年7月29日（米国時間）発表。前世代にあたるはずのGeForce 8800 GTと全く同じ（チップ上の刻印まで同じ）ものがある一方で55 nmにシュリンクした製品もあるなど消費者にわかりにくい製品になっていた。Hybrid Power対応はカードベンダーが選択する。消費電力は105 Wといわれている。
    ※Hybrid Powerについて、情報の混乱から「55 nm版はHybrid Powerに対応している」という噂が流れていたが、実際はカードの設計によるオプション扱いで65 nm版も55 nm版も共に対応している。Hybrid Powerの可否は製品パッケージやカードメーカーのサイトで確認できる。Hybrid Powerの記述が無ければ対応していないが、記述があっても[ランニングチェンジ](https://ja.wikipedia.org/wiki/ランニングチェンジ "wikilink")で非対応になっていることもあり混乱に拍車をかけている。
  - GeForce 9800 GT(66 W)
    **GeForce 9800 GT Green Edition**とも呼ばれ、GeForce 9800 GTのコアを55 nmにシュリンクしたG92bを搭載し、コアクロックを落とす事で消費電力が66 Wまで落ち、補助電源が不要となった製品。

#### GeForce 100 Series

**GeForce 100 Series**（ジーフォース・100・シリーズ）は、GeForce 9シリーズのリネーム版とされている。すべてOEM向けであり、一般ユーザー向けには市販されていない。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック （CUDAコアクロック）</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>CUDA</p></th>
<th><p>TeX</p></th>
<th><p>FLOPS 単精度 (理論値)</p></th>
<th><p>SLI</p></th>
<th><p>最大消費電力 (補助電源)</p></th>
<th><p>|<a href="https://ja.wikipedia.org/wiki/DirectX" title="wikilink">DirectX</a><br />
<small>(Feature Level)</small></p></th>
<th><p>OpenGL</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce G100 (OEM)</p></td>
<td><p>G98b (55nm)</p></td>
<td><p>567MHz (1400MHz)</p></td>
<td><p>DDR2 1000MHz (64bit)</p></td>
<td><p>8</p></td>
<td><p>8</p></td>
<td><p>9GFLOPS</p></td>
<td><p>×</p></td>
<td><p>35W</p></td>
<td><p>11.1 API<br />
<small>(FL:10_0)</small></p></td>
<td><p>3.3</p></td>
</tr>
<tr class="even">
<td><p>GeForce GT 120 (OEM)</p></td>
<td><p>G96b (55nm)</p></td>
<td><p>500MHz (1400MHz)</p></td>
<td><p>DDR2 1000MHz (128bit)</p></td>
<td><p>32</p></td>
<td><p>16</p></td>
<td><p>32GFLOPS</p></td>
<td><p>2-way</p></td>
<td><p>50W</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 130 (OEM)</p></td>
<td><p>G94b (55nm)</p></td>
<td><p>500MHz (1250MHz)</p></td>
<td><p>DDR2 1000MHz (192bit)</p></td>
<td><p>48</p></td>
<td><p>24</p></td>
<td><p>48GFLOPS</p></td>
<td><p>75W (6pin)</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTS 150 (OEM)</p></td>
<td><p>G92b (55nm)</p></td>
<td><p>738MHz (1836MHz)</p></td>
<td><p>GDDR3 2000MHz (256bit)</p></td>
<td><p>128</p></td>
<td><p>64</p></td>
<td><p>0.19TFLOPS</p></td>
<td><p>2/3-way</p></td>
<td><p>141W (6pin×2)</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce 200 Series

**GeForce 200 Series**（ジーフォース・200・シリーズ）は、2008年6月17日に発表された、GeForceシリーズの第10世代製品群である。GeForce 8800以来、1年半以上にわたり、NVIDIAのハイエンドを担ってきた、G80/90系コアの後継となるべく開発された。開発コードは65 nmのものはGT200、55 nmのものはGT200bもしくはGT206と呼ばれる。GeForce/Tesla第二世代の意味であるという。

なお、これ以降NVIDIAのGPUの命名規則が変更されたが、後述のGTSシリーズがリネーム品（実質二世代前の製品のシュリンク版）であったり、後発の下位モデルであるGTシリーズのみ最新プロセスのコアを使用してDirectX 10.1への対応など、型番や製品ラインナップがGeForce 9シリーズと同様に非常に分かりづらくなっている。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック （CUDAコアクロック）</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>CUDA</p></th>
<th><p>TeX</p></th>
<th><p>TFLOPS 単精度 (理論値)</p></th>
<th><p>SLI</p></th>
<th><p>最大消費電力 (補助電源)</p></th>
<th><p>|<a href="https://ja.wikipedia.org/wiki/DirectX" title="wikilink">DirectX</a><br />
<small>(Feature Level)</small></p></th>
<th><p>OpenGL</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce 210</p></td>
<td><p>GT218 (40nm)</p></td>
<td><p>589MHz (1402MHz)</p></td>
<td><p>DDR2 1000MHz (64bit)</p></td>
<td><p>16</p></td>
<td><p>8</p></td>
<td><p>18.8GFLOPS</p></td>
<td><p>×</p></td>
<td><p>30.5W</p></td>
<td><p>11.1 API<br />
<small>(FL:10_1)</small></p></td>
<td><p>3.3</p></td>
</tr>
<tr class="even">
<td><p>GeForce GT 220</p></td>
<td><p>G94 (65nm)</p></td>
<td><p>600MHz (1500MHz)</p></td>
<td><p>GDDR3 1400MHz (128bit)</p></td>
<td><p>48</p></td>
<td><p>24</p></td>
<td><p>57.6GFLOPS</p></td>
<td><p>58W</p></td>
<td><p>11.1 API<br />
<small>(FL:10_0)</small></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GT216 (40nm)</p></td>
<td><p>625MHz (1360MHz)</p></td>
<td><p>DDR3 1380MHz (128bit)</p></td>
<td><p>48</p></td>
<td><p>16</p></td>
<td><p>60GFLOPS</p></td>
<td><p>11.1 API<br />
<small>(FL:10_1)</small></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 240</p></td>
<td><p>GT215 (40nm)</p></td>
<td><p>550MHz (1340MHz)</p></td>
<td></td>
<td><p>96</p></td>
<td><p>32</p></td>
<td><p>0.1TFLOPS</p></td>
<td><p>69W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTS 240 (OEM)</p></td>
<td><p>G92b (55nm)</p></td>
<td><p>675MHz (1620MHz)</p></td>
<td><p>GDDR3 2200MHz (256bit)</p></td>
<td><p>112</p></td>
<td><p>56</p></td>
<td><p>0.15TFLOPS</p></td>
<td><p>2-way</p></td>
<td><p>120W (6pin)</p></td>
<td><p>11.1 API<br />
<small>(FL:10_0)</small></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTS 250</p></td>
<td><p>G92b (55nm)</p></td>
<td><p>738MHz (1836MHz)</p></td>
<td><p>GDDR3 2200MHz (256bit)</p></td>
<td><p>128</p></td>
<td><p>64</p></td>
<td><p>0.19TFLOPS</p></td>
<td><p>2/3-way</p></td>
<td><p>150W (6pin)</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 260 (OEM)</p></td>
<td><p>GT200b[GT206] (55nm)</p></td>
<td><p>518MHz (1080MHz)</p></td>
<td><p>GDDR3 2016MHz (448bit))</p></td>
<td><p>192</p></td>
<td><p>64</p></td>
<td><p>0.2TFLOPS</p></td>
<td><p>182W (6pin×2)</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 260</p></td>
<td><p>GT200 (65nm)</p></td>
<td><p>576MHz (1242MHz)</p></td>
<td><p>GDDR3 1998MHz (448bit)</p></td>
<td><p>0.22TFLOPS</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 260 Rev.2</p></td>
<td><p>216</p></td>
<td><p>72</p></td>
<td><p>0.25TFLOPS</p></td>
<td><p>182W (6pin×2)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GT200b[GT206] (55nm)</p></td>
<td><p>171W (6pin×2)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 275</p></td>
<td><p>GT200b[GT206] (55nm)</p></td>
<td><p>633MHz (1404MHz)</p></td>
<td><p>GDDR3 2268MHz (448bit)</p></td>
<td><p>240</p></td>
<td><p>80</p></td>
<td><p>0.3TFLOPS</p></td>
<td><p>219W (6pin×2)</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 280</p></td>
<td><p>GT200 (65nm)</p></td>
<td><p>602MHz (1296MHz)</p></td>
<td><p>GDDR3 2214MHz (512bit)</p></td>
<td><p>0.29TFLOPS</p></td>
<td><p>236W (6pin+8pin)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 285</p></td>
<td><p>GT200b[GT206] (55nm)</p></td>
<td><p>648MHz (1476MHz)</p></td>
<td><p>GDDR3 2484MHz (512bit)</p></td>
<td><p>0.31TFLOPS</p></td>
<td><p>204W (6pin×2)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 295</p></td>
<td><p>GT200b[GT206] (55nm)×2チップ</p></td>
<td><p>576MHz (1242MHz)</p></td>
<td><p>GDDR3 1998MHz (448bit×2)</p></td>
<td><p>240×2</p></td>
<td><p>80×2</p></td>
<td><p>0.55TFLOPS</p></td>
<td><p>Quad</p></td>
<td><p>289W (6pin+8pin)</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

[thumb](https://ja.wikipedia.org/wiki/ファイル:Gtx280.jpg "wikilink")

  - 210、GT 220
    2009年7月9日（日本時間）、NVIDIA公式Webサイトにて発表。発表当初はOEM向けの先行発売品となっていた。GeForceシリーズ初となる40 nmプロセスによる量産品であり、NVIDIAのデスクトップ向けGPUとして初めてDirectX 10.1に対応した（NVIDIAはノート向けGPU、GeForce GTS/GT/G 2\*0 MシリーズにおいてDirectX 10.1に初めて対応している）。GeForce 210とGT 220はそれぞれGeForce 9400 GTとGeForce 9500 GTの後継品となっている。210がGeForce 9400 GTからメモリバス幅を64bitに削減しPhysXを省略したもので性能は低下し、GT 220がGeForce 9500 GTからシェーダープロセッサを16基増やしたもので性能はやや向上している。
  - GT 240 \[18\]
    2009年11月17日（米国時間）発表。NVIDIAのデスクトップ向け製品としては初めて[GDDR5](https://ja.wikipedia.org/wiki/GDDR5 "wikilink")に対応している。GT200系コアとして初めてミドルレンジ製品であり、*GeForce 9600 GT*の後継品であるが、DirectX 10.1に対応、CUDAコア（以前はSPと呼ばれていたもの）が96基、ビデオメモリが[GDDR5](https://ja.wikipedia.org/wiki/GDDR5 "wikilink")に対応。しかしメモリバス幅が128bitに半減し、性能はそれほど向上していない。
  - GTS 240、GTS 250
    2009年3月3日（米国時間）発表。200番台が付番されているが、コア自体はGT200bではなくG92bであり、実質的にGTS 250は9800 GTX+と同じ製品、GTS 240は9800 GTの周波数向上版である。ただし、値段も大幅に安くなったほか、基板の設計の改良により消費電力が削減されており、その結果GTS 250は補助電源コネクタが6ピン1個になり（9800 GTX+は2個）、基板の長さも短くなった。また、新たに1 GB版が登場した。GTS 240は１スロット、GTS 250は2スロット占有する。
  - GTX 260
    GTX 260はGTX 280のコアの一部を無効にしたものである。
  - GTX 260 Rev.2 \[19\]
    2008年9月には仕様変更によりSP数が192基から216基へ増やされた。さらに2009年2月には消費電力を低減した55 nm版GTX260が発売された。同名ながら僅かに仕様の異なる3種類のコアが存在していたことになり、入れ替わり時期では店頭での区別が難しい場合があった。
  - GTX 275
    2009年4月2日 （日本時間） 発表。55 nmのGT200b(GT206)チップを採用し、一部機能を制限した製品である。スペック的にはSP数が240、メモリインタフェース448bitとなり、GTX 295のワンチップ版と言える性能である。消費電力が最大219 Wと、GTX 275の上位にあたるGTX 285の204 Wより高く、GTX 285の選別に漏れたチップをGTX 275に回しているとの推察が出来る。この製品はAMDのATI [Radeon](https://ja.wikipedia.org/wiki/Radeon "wikilink") HD 4890の発表から三時間後に発表され、明確に対抗製品である事を伺わせた。
    また、メーカーの独自派生製品であるが、GTX 275とGTS 250（メモリインターフェースを192bitに削減した物）という異なるチップを、PCI Express 2.0対応のブリッジチップ、nForce 200によって動作させて、GTS 250を[PhysX](../Page/PhysX.md "wikilink")演算専用コアとして使うカードも発売されている。外見、構造共にシングルPCB版GeForce GTX 295のリファレンスデザインとよく似ている。
  - GTX 280
    シングルチップで、デュアルチップのGeForce 9800 GX2と同等程度の性能を持つ。
    それ以上に、これまでGPUの強力な並列演算能力を他分野に生かそうというCUDAテクノロジに最適化されており、GPUを単なる3D描画装置以上に使うNVIDIAの戦略に沿った製品である。
    これにより、医療分野や天文分野など専門的な分野のみならず、たとえば動画のエンコードを革新的に高速化するといった利用方法が期待されており、一部で始まってもいる。
    ただし、GeForce 9シリーズと同様にDirectX 10.1には対応していない。
    同じチップを使い、より[GPUコンピューティングに特化したモデルが](https://ja.wikipedia.org/wiki/GPGPU "wikilink")[Teslaである](https://ja.wikipedia.org/wiki/NVIDIA_Tesla "wikilink")。
    65 nmプロセスにおいて、576mm2の巨大なチップゆえに発熱も大きく、価格も高い。
    最大消費電力は236 Wとこれまでより増えているが、なんらかの省電力時専用回路が搭載されたようで、アイドル時の消費電力は逆に低下しており、Hybrid SLIにも対応しているため、対応したnForceチップセットと組み合わせて使えば、Hybrid Powerモードにより低負荷時に消費電力を0にできる。
  - GTX 285
    2009年1月8日（米国時間）発表。55 nmに微細化したGT200b(GT206)を採用し、GTX 280のクロックを向上させながら消費電力を低減、GTX 280から1割程度性能が向上している。
    正式なものではないが、ASUSから独自設計でGTX 285を2基搭載（今までのNVIDIAのデュアルチップ製品同様、二つの基板の間に冷却機構を挟む構造をとっている）したものが発売されている。GTX 295より23% - 75%高い性能を発揮する。
  - GTX 295
    2008年12月18日（米国時間）発表。55 nmのGT200b (GT206) チップを2基搭載した製品で、GeForce 9800 GX2同様、二つの基板の間に冷却機構を挟む構造をとっている。2009年6月にはシングル基板のモデルも各社から販売されており、冷却機構がGTX 285などに近い形となった。消費電力は289 W。
    単体のビデオカードとして、RADEON HD 4870 X2より場合によっては50%以上高速である。また、Quad-SLI構成時にはGTX 285の3way-SLIより25%ほど高速。

#### GeForce 300 Series

**GeForce 300 Series**（ジーフォース・300・シリーズ）は、OEM専用の製品群で、従来製品のリネーム品であることが多い。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック （CUDAコアクロック）</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>CUDA</p></th>
<th><p>TeX</p></th>
<th><p>FLOPS 単精度 (理論値)</p></th>
<th><p>SLI</p></th>
<th><p>最大消費電力 (補助電源)</p></th>
<th><p>|<a href="https://ja.wikipedia.org/wiki/DirectX" title="wikilink">DirectX</a><br />
<small>(Feature Level)</small></p></th>
<th><p>OpenGL</p></th>
<th><p>PhysX</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce 315 (OEM)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>×</p></td>
<td><p>33W</p></td>
<td><p>11.1 API<br />
<small>(FL:10_1)</small></p></td>
<td><p>3.3</p></td>
<td><p>非対応</p></td>
</tr>
<tr class="even">
<td><p>GeForce GT 320 (OEM)</p></td>
<td><p>GT215 (40nm)</p></td>
<td><p>540MHz (1302MHz)</p></td>
<td><p>GDDR3 1580MHz (128bit)</p></td>
<td><p>72</p></td>
<td><p>24</p></td>
<td><p>77.7GFLOPS</p></td>
<td><p>43W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 330 (OEM)</p></td>
<td><p>G92b (65nm)</p></td>
<td><p>500MHz (1250MHz)</p></td>
<td><p>DDR2 1020MHz (128bit)</p></td>
<td><p>96</p></td>
<td><p>48</p></td>
<td><p>96GFLOPS</p></td>
<td><p>75W</p></td>
<td><p>11.1 API<br />
<small>(FL:10_0)</small></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GT215 (40nm)</p></td>
<td><p>550MHz (1340MHz)</p></td>
<td><p>GDDR3 2000MHz (128bit)</p></td>
<td><p>96</p></td>
<td><p>32</p></td>
<td><p>0.1TFLOPS</p></td>
<td><p>11.1 API<br />
<small>(FL:10_1)</small></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 340 (OEM)</p></td>
<td><p>GT215 (40nm)</p></td>
<td><p>550MHz (1340MHz)</p></td>
<td><p>GDDR3 1700MHz (128bit)</p></td>
<td><p>96</p></td>
<td><p>32</p></td>
<td><p>69W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce 400 Series

**GeForce 400 Series**（ジーフォース・400・シリーズ）は、2010年3月27日に発表された、GeForceシリーズの第11世代製品群である。NVIDIAのグラフィックスチップとしては初めてDirectX 11に対応し、また、GPGPUへの最適化が進められた製品である。開発コードはGF100（GT300という開発コードで呼ばれていた時期もあった）。これはGeForce/Fermi第1世代の意味であるという。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック (CUDAコアクロック)</p></th>
<th><p>コア数</p></th>
<th><p>メモリ</p></th>
<th><p>FLOPS</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/SLI" title="wikilink">SLI</a></p></th>
<th><p>最大消費電力 (補助電源)</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/DirectX" title="wikilink">DirectX</a><br />
<small>(Feature Level)</small></p></th>
<th><p><a href="../Page/OpenGL.md" title="wikilink">OpenGL</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SM</p></td>
<td><p><a href="../Page/CUDA.md" title="wikilink">CUDA</a></p></td>
<td><p>TeX</p></td>
<td><p>ROP</p></td>
<td><p>L2</p></td>
<td><p>バス幅</p></td>
<td><p>動作クロック</p></td>
<td><p>容量</p></td>
<td><p>単精度 (理論値)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 420 (OEM)</p></td>
<td><p>GF108 (40nm)</p></td>
<td><p>675MHz (1350MHz)</p></td>
<td><p>1</p></td>
<td><p>48</p></td>
<td><p>8</p></td>
<td><p>4</p></td>
<td><p>256KB</p></td>
<td><p>128bit</p></td>
<td><p>DDR3 1800MHz相当</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 430</p></td>
<td><p>700MHz (1400MHz)</p></td>
<td><p>2</p></td>
<td><p>96</p></td>
<td><p>16</p></td>
<td><p>1GB</p></td>
<td><p>0.13TFLOPS</p></td>
<td><p>49W</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 440</p></td>
<td><p>810MHz (1620MHz)</p></td>
<td><p>1GB</p></td>
<td><p>0.16TFLOPS</p></td>
<td><p>65W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GDDR5 3200MHz相当</p></td>
<td><p>0.5GB</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 440 (OEM)</p></td>
<td><p>GF106 (40nm)</p></td>
<td><p>594MHz (1189MHz)</p></td>
<td><p>3</p></td>
<td><p>144</p></td>
<td><p>24</p></td>
<td><p>24</p></td>
<td><p>384KB</p></td>
<td><p>192bit</p></td>
<td><p>DDR3 1800MHz相当</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTS 450</p></td>
<td><p>783MHz (1566MHz)</p></td>
<td><p>4</p></td>
<td><p>192</p></td>
<td><p>32</p></td>
<td><p>16</p></td>
<td><p>256KB</p></td>
<td><p>128bit</p></td>
<td><p>GDDR5 3608MHz相当</p></td>
<td><p>1GB</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 460 SE</p></td>
<td><p>GF104 (40nm)</p></td>
<td><p>650MHz (1300MHz)</p></td>
<td><p>6</p></td>
<td><p>288</p></td>
<td><p>48</p></td>
<td><p>32</p></td>
<td><p>512KB</p></td>
<td><p>256bit</p></td>
<td><p>GDDR5 3400MHz相当</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 460 (768 MB)</p></td>
<td><p>675MHz (1350MHz)</p></td>
<td><p>7</p></td>
<td><p>336</p></td>
<td><p>56</p></td>
<td><p>24</p></td>
<td><p>384KB</p></td>
<td><p>192bit</p></td>
<td><p>GDDR5 3600MHz相当</p></td>
<td><p>0.75GB</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 460 (1GB)</p></td>
<td><p>32</p></td>
<td><p>512KB</p></td>
<td><p>256bit</p></td>
<td><p>1GB</p></td>
<td><p>160W (6pin×2)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 465</p></td>
<td><p>GF100 (40nm)</p></td>
<td><p>607MHz (1215MHz)</p></td>
<td><p>11</p></td>
<td><p>352</p></td>
<td><p>44</p></td>
<td><p>GDDR5 3206MHz相当</p></td>
<td><p>0.43TFLOPS</p></td>
<td><p>3-way</p></td>
<td><p>200W (6pin×2)</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 470</p></td>
<td><p>14</p></td>
<td><p>448</p></td>
<td><p>56</p></td>
<td><p>|40</p></td>
<td><p>640KB</p></td>
<td><p>320bit</p></td>
<td><p>GDDR5 3348MHz相当</p></td>
<td><p>1.25GB</p></td>
<td><p>0.54TFLOPS</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 480</p></td>
<td><p>700MHz (1401MHz)</p></td>
<td><p>15</p></td>
<td><p>480</p></td>
<td><p>60</p></td>
<td><p>48</p></td>
<td><p>768KB</p></td>
<td><p>384bit</p></td>
<td><p>GDDR5 3696MHz相当</p></td>
<td><p>1.5GB</p></td>
</tr>
</tbody>
</table>

[thumb](https://ja.wikipedia.org/wiki/ファイル:Nvidia_GeForce_GTX480.jpg "wikilink")

  - GT 420 (OEM)
    2010年9月3日（日本時間）Webサイトにて発表。Fermiアーキテクチャの下位モデルで、GF108を採用した製品。
  - GT 430
    2010年10月11日（日本時間）発表。GT 420と同じFermiアーキテクチャの下位モデルで、GF108を採用した製品。
  - GT 440
    2011年2月1日（米国時間）発表。GT430のオーバークロック版。GDDR5メモリにも対応。
  - GTS 450
    2010年9月13日（日本時間）Webサイトにて発表。Fermiアーキテクチャのバリューモデルである、GF106を採用した製品。GF106はGF104のちょうど半分のスペックのコアである。リファレンスモデルで6ピン補助電源が1系統で済む製品はGeForce400シリーズで初。OEM版も存在するがスペックは異なる（CUDAコアなどが削減されている）。
    なおMicrosoft Expression Encoder 4 でのCUDAによるGPUエンコーディングを使用する際には、通常のPCを使用した1ストリームのMP4エンコードの場合で1 GBのメモリーと128以上のCUDAコアを持つGPUが推奨となっており、現在の製品ラインアップではGTS 450/GTX 550以上が推奨スペックとなる\[20\]。
  - GTX 460 SE
    2010年11月15日（米国時間）発表。GTX 460(1 GB)からSM 1基が無効化されているが、メモリバス幅は256bitから削減されていない。
  - GTX 460(768 MB)、GTX 460(1 GB)
    2010年7月12日（日本時間）NVIDIAウェブサイトにて発表と同時に販売開始。FermiアーキテクチャであるGF100の派生コア、GF104を初めて採用した製品。
    GF100とGF104の相違点は以下のとおりである。
      - GPC数が4基から2基に半減
      - 一つのSM当たりのCUDAコア数が32基から48基に増加、テクスチャユニット(TeX)が4基から8基に倍増
      - ROPパーティション（ROPユニットが8基まとまったもの）が6基から4基に削減
      - メモリバス幅が384bitから256bitに削減
    GF104のフルスペックはCUDAコアが384基、テクスチャユニットが56基、ROPユニットが32基、メモリバス幅が256bitであるが、GF100採用製品と同じ様に歩留まり向上の為にCUDAコアが336基に削減され、更に768 MB版はメモリ周りもメモリコントローラとROPパーテーションが1基ずつ（つまりはメモリバス幅64bit分、ROPユニットで8基）削減されている。
    仕様変更により、GF100に比べて、DirectX 9、10世代のアプリケーションでのパフォーマンスが向上し、768 MB版ではGTX 465に匹敵、1 GB版ではGTX 465を上回る性能となっている。
    どちらのモデルも6ピン補助電源が2系統必要であるが、消費電力はGTX 465に比べて大きく削減され、メーカーオリジナルデザインであれば768 MB版は6ピン補助電源1系統も存在する。カードサイズも短小化され、取り回しが容易になっている。
  - GTX 465
    2010年5月31日（台湾時間）COMPUTEX TAIPEI 2010開幕前日に開催した報道関係者向け説明会にて発表。FermiアーキテクチャであるGF100を採用した製品。歩留まり向上の為に、GTX 470から更に一部のCUDAコア等が無効化されている。
  - GTX 470、GTX 480
    2010年3月27日（米国時間）発表。NVIDIAのGPUとして初めてDirectX 11に対応した。その構造は、CUDAコアを32基、超越関数ユニット(SFU)やキャッシュ、テクスチャユニット(TeX)を4基、頂点処理エンジン（PolyMorph Engine、いわゆるテッセレーター）が1基で、Streaming Multi-Processor(SM)という最小構成単位を形作り、SMが4基集まってGraphics Processing Cluster(GPC)というミニGPUを構成している。GF100は4基のGPCでクラスタ化された構造を持ち、クアッドコア的な構成となっている。GF100のフルスペックなCUDAコアは512基であり、GTX 470、GTX 480の両方で歩留まり向上の為に一部のCUDAコアが無効化されている。本来はこの世代で倍精度演算が大幅に強化される予定であったが、予定の1/4の性能にとどまっている（ただしこれでも前世代のGeforceを多少上回っている）。今後発売予定のTeslaでは計画通りの性能を発揮できるようになる予定である。
    前世代のハイエンドであるGT200系のチップに比べ、ピクセルシェーダー機能の性能向上は押さえられ、頂点シェーダー機能が大幅に強化された（GTX 280はGeForce FX 5800に比べ、ピクセルシェーダーの性能は150倍になった一方で、頂点シェーダーの性能は3倍にも達していなかった）。これは、GF100がDirectX 11の新機能であるテッセレーションに最適化されている為である。
    また、GeForce FXシリーズの教訓から、GeForce 6シリーズより続いた、ハイエンドは枯れたプロセスで生産する原則を破り、TSMCの最新プロセスである40 nmプロセスを採用している。GTX 480は非常に発熱が激しく、基板に吸気口を持ち、ヒートパイプを利用した特徴的なGPUクーラーを採用している。GTX 480は消費電力の公称値は250 W\[21\]となっているが、フルロード時に消費電力が300 W近くになるという動画やレビューが日本国外で掲載されている（なお、電源供給は6ピン補助電源と8ピン補助電源の2系統と、PCI-Expressスロットからの給電で合計300 Wになるので、電力不足になる事はない）。

#### GeForce 500 Series

**GeForce 500 Series**（ジーフォース・500・シリーズ）は、2010年11月9日に発表された、GeForceシリーズの第12世代製品群である。Fermi第2世代のGF11xコアを採用しているが、コアのアーキテクチャは前世代とほぼ同じである。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック (CUDAコアクロック)</p></th>
<th><p>コア数</p></th>
<th><p>メモリ</p></th>
<th><p>FLOPS</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/SLI" title="wikilink">SLI</a></p></th>
<th><p>最大消費電力 (補助電源)</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/DirectX" title="wikilink">DirectX</a><br />
<small>(Feature Level)</small></p></th>
<th><p><a href="../Page/OpenGL.md" title="wikilink">OpenGL</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SM</p></td>
<td><p><a href="../Page/CUDA.md" title="wikilink">CUDA</a></p></td>
<td><p>TeX</p></td>
<td><p>ROP</p></td>
<td><p>L2</p></td>
<td><p>バス幅</p></td>
<td><p>動作クロック</p></td>
<td><p>容量</p></td>
<td><p>単精度 (理論値)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 510 (OEM)</p></td>
<td><p>GF119 (40nm)</p></td>
<td><p>523MHz (1046MHz)</p></td>
<td><p>1</p></td>
<td><p>48</p></td>
<td><p>8</p></td>
<td><p>4</p></td>
<td><p>128KB</p></td>
<td><p>64bit</p></td>
<td><p>DDR3 1796MHz相当</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 520</p></td>
<td><p>810MHz (1620MHz)</p></td>
<td><p>DDR3 1800MHz相当</p></td>
<td><p>77.7GFLOPS</p></td>
<td><p>29W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 530 (OEM)</p></td>
<td><p>GF118 (40nm)</p></td>
<td><p>700MHz (1400MHz)</p></td>
<td><p>2</p></td>
<td><p>96</p></td>
<td><p>16</p></td>
<td><p>4</p></td>
<td><p>256KB</p></td>
<td><p>128bit</p></td>
<td><p>DDR3 1796MHz相当</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 545 DDR3 (OEM)</p></td>
<td><p>GF116 (40nm)</p></td>
<td><p>720MHz (1440MHz)</p></td>
<td><p>3</p></td>
<td><p>144</p></td>
<td><p>24</p></td>
<td><p>24</p></td>
<td><p>384KB</p></td>
<td><p>192bit</p></td>
<td><p>DDR3 1800MHz相当</p></td>
</tr>
<tr class="even">
<td><p>GeForce GT 545 GDDR5 (OEM)</p></td>
<td><p>870MHz (1740MHz)</p></td>
<td><p>16</p></td>
<td><p>256KB</p></td>
<td><p>128bit</p></td>
<td><p>GDDR5 3996MHz相当</p></td>
<td><p>1GB</p></td>
<td><p>0.25TFLOPS</p></td>
<td><p>105W (6pin)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 550 Ti</p></td>
<td><p>900MHz (1800MHz)</p></td>
<td><p>4</p></td>
<td><p>192</p></td>
<td><p>32</p></td>
<td><p>24</p></td>
<td><p>384KB</p></td>
<td><p>192bit</p></td>
<td><p>GDDR5 4100MHz相当</p></td>
<td><p>1GB / 2GB</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 555 (OEM)</p></td>
<td><p>GF114 (40nm)</p></td>
<td><p>776MHz (1553MHz)</p></td>
<td><p>6</p></td>
<td><p>288</p></td>
<td><p>48</p></td>
<td><p>GDDR5 3828MHz相当</p></td>
<td><p>1GB</p></td>
<td><p>0.45TFLOPS</p></td>
<td><p>150W (6pin×2)</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 560 SE</p></td>
<td><p>736MHz (1472MHz)</p></td>
<td><p>0.42TFLOPS</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 560</p></td>
<td><p>810MHz (1620MHz) - 950MHz (1900MHz)</p></td>
<td><p>7</p></td>
<td><p>336</p></td>
<td><p>56</p></td>
<td><p>32</p></td>
<td><p>512KB</p></td>
<td><p>256bit</p></td>
<td><p>GDDR5 4004 - 4488MHz相当</p></td>
<td><p>1GB / 2GB</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 560 Ti</p></td>
<td><p>822MHz (1644MHz)</p></td>
<td><p>8</p></td>
<td><p>384</p></td>
<td><p>64</p></td>
<td><p>GDDR5 4008MHz相当</p></td>
<td><p>1GB / 2GB</p></td>
<td><p>0.63TFLOPS</p></td>
<td><p>170W (6pin×2)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 560 Ti (OEM)</p></td>
<td><p>GF110 (40nm)</p></td>
<td><p>732MHz (1464MHz)</p></td>
<td><p>11</p></td>
<td><p>352</p></td>
<td><p>44</p></td>
<td><p>40</p></td>
<td><p>640KB</p></td>
<td><p>320bit</p></td>
<td><p>GDDR5 3800MHz相当</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 560 Ti (448 Cores Limited Edition)</p></td>
<td><p>14</p></td>
<td><p>448</p></td>
<td><p>56</p></td>
<td><p>1.25GB</p></td>
<td><p>0.66TFLOPS</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 570</p></td>
<td><p>15</p></td>
<td><p>480</p></td>
<td><p>60</p></td>
<td><p>1.25GB / 2.5GB</p></td>
<td><p>0.7TFLOPS</p></td>
<td><p>3-way</p></td>
<td><p>219W (6pin×2)</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 580</p></td>
<td><p>772MHz (1544MHz)</p></td>
<td><p>16</p></td>
<td><p>512</p></td>
<td><p>64</p></td>
<td><p>48</p></td>
<td><p>768KB</p></td>
<td><p>384bit</p></td>
<td><p>GDDR5 4008MHz相当</p></td>
<td><p>1.5GB / 3GB</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 590</p></td>
<td><p>GF110 (40nm)×2チップ</p></td>
<td><p>607MHz (1215MHz)</p></td>
<td><p>16×2</p></td>
<td><p>512×2</p></td>
<td><p>64×2</p></td>
<td><p>48×2</p></td>
<td><p>768KB×2</p></td>
<td><p>384bit×2</p></td>
<td><p>GDDR5 3414MHz相当</p></td>
</tr>
</tbody>
</table>

  - GT 520
    2011年4月12日（米国時間）発表。GeForce 500シリーズのローエンドモデル。
  - GT 530 (OEM)
    2011年5月19日（米国時間）発表。GF118版のGT 430と言える製品。
  - GT 545 (OEM)
    2011年5月19日（米国時間）発表。GDDR5メモリ搭載品とDDR3メモリ搭載品があり、メモリ容量はDDR3搭載品が大きいが、性能はGDDR5搭載品が高くなる。
  - GTX 550 Ti
    2011年3月15日（日本時間）発表。GTX 550 Tiに搭載されているGF116チップはGTS 450に搭載されているGF106チップを改良したモデルである。GTX 560 Tiと同様に''Ti ''が名称につけられている。性能にはGTS 450からは順当に上昇しているものの、GTX 460(768 MB)に及ばず、GTX 460 SE程度となっている\[22\]。
  - GTX 555 (OEM)
    2012年1月19日（日本時間）発表。Alienware社のBTOPCである「Alienware X51」のBTOオプションの一つとして採用されているOEM専用品。GTX 555と550番台でありながらGF114コアを採用している。GTX 560からあらゆる面でデチューンされているが、最大消費電力はGTX 560と同じ150 Wとされ、6ピン補助電源2系統を必要としている（ただし、「Alienware X51」のBTOオプションとして採用されたものはクロック数が若干落とされ、補助電源が1系統になっている）。
  - GTX 560 SE \[23\]
    2012年3月、公式発表なしに発売。
  - GTX 560
    2011年5月17日（日本時間）発表。GTX 460の後継製品であり、GF114版のGTX 460と言える製品。製品の周波数がリファレンスデザインで定められていない。リファレンスデザインで定められているのは、150 Wまでという製品の消費電力の制限のみであり、発表では想定される製品の周波数を大まかに示すだけであった。なお、一番低い周波数がリファレンスクロックという訳ではなくNVIDIAは「GTX 560のリファレンスデザインはないため、リファレンスクロックも設定していない」\[24\]という公式見解を出している。この為、周波数ではGTX 560 Tiを超える製品も存在し、3D性能が同程度に高められている。
  - GTX 560 Ti
    2011年1月25日（日本時間）発表。GF114のフルスペック版。GeForce 400シリーズでモデルナンバーが3桁しか無い為に分かりにくくなった命名規則の反省からか、GeForce 4 Tiシリーズ以来となる''Ti ''の命名規則が復活した。GTX 460系に比べ、コア数が増加（SM換算で7基から8基）している他に、コアクロックやメモリクロックが上昇して、性能はGTX 460系を完全に上回り、GTX 470と同程度になっている。
  - GTX 570
    2010年12月7日（米国時間）発表。GTX 580から、CUDAコアとテクスチャーユニット、ROPユニットとメモリバス幅が削減されている。GPUクーラーはGTX 580で採用されたものと同じ、ベイパーチャンバーが採用されている。カードサイズはGTX 580と等しい。性能はGTX 470を完全に上回り、GTX 480と同程度の性能となっている。
  - GTX 580
    2010年11月9日（日本時間）23時発表。GF110のフルスペック版。アーキテクチャ的にはGF100に若干の機能を追加した以外はほぼ同一であるが、歩留まりの向上や消費電力の改善などの物理設計が大きく見直された可能性がある\[25\]。GTX 480で無効化されていたコアが全て有効化されたが、消費電力はGTX 480と同程度に抑えられた。また、GPUクーラーに関しても[ベイパーチャンバー](https://ja.wikipedia.org/wiki/ベイパーチャンバー "wikilink")を採用するなどしてGTX 480から大幅に改善され（特徴的なヒートシンクや基板の吸気口も姿を消している）、冷却力と静音性が向上した。性能に関してもGTX 480から十数%向上している。
  - GTX 590
    2011年3月24日（日本時間）22時発表。GTX 295以来であり、Fermi世代初のデュアルGPUカードである。使用しているコアはGTX 580と同じGF110のフルスペック版となる（ROPユニットやテクスチャユニット等に関してもGTX 580と同じフルスペック）。公称消費電力は365 Wで、8ピン補助電源が2系統必要となる。これにより合計375 Wの電力をカードに供給する事が可能であるが、PCI-SIGの規定は6ピン補助電源と8ピン補助電源を1系統ずつの合計2系統（供給電力はPCI-Eスロットからのものと合わせて300 W）までと定められており、このリファレンスデザインを超えるものである（メーカー独自デザインのものであれば既に規定を超えるものは発売されていた）。しかし、動作クロックはGTX 580と比べて大きく引き下げられている。これは、公称消費電力が244 WであるGTX 580（と同じGF110コアのフルスペック版）をGTX 590として一つのカードに搭載する為だが、既に本来のPCI-SIG規定を超えている為に、この制限は他社製品であるRadeon HD 6990（GTX 590発売時点でのデュアルGPUカードの最上位製品であり、補助電源は8ピンx2）を意識したものであると推察できる。性能的にはGTX 570のSLIと同程度になっているが、消費電力まで実測では公称219 WのGTX 570のSLI（単純計算として合計438 W）と同程度になっている。GPUクーラーはコンパクトでありながら静音性と冷却力に優れている。

#### GeForce 600 Series

**GeForce 600 Series**（ジーフォース・600・シリーズ）は、2012年3月22日に発表された、GeForceシリーズの第13世代製品群である。GeForce 500 Seriesからアーキテクチャの大幅な刷新をおこなった。NVIDIAはKeplerアーキテクチャをCUDAの転換点と位置付けており、電力あたりの性能（ワットパフォーマンス、[Performance per Watt](https://ja.wikipedia.org/wiki/:en:Performance_per_watt "wikilink")）に重きを置いた設計をおこなっている。

KeplerアーキテクチャではTesla - Fermi世代で採用されたシェーダクロック倍速機能を廃止し、FermiアーキテクチャではGF100コアとGF110コアで32基、その他のコアで48基のCUDAコアでSM(Streaming Multiprocessor)構成していたのに対し、Keplerアーキテクチャでは192基のCUDAコアでSMX(Streaming Multiprocessor eXtreme)を構成。またFermiプロッセッサに比べパイプラインの段数が大幅に減少しており、プロッセッサ内でハードウェア処理されていたスケジューリングの大半がソフトウェア処理に回った。パイプラインが浅くなったことによりラッチ回路が減少し消費電力を大幅に押し下げる結果となった。

なおGK104チップは汎用コンピューティング ([GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")) 向けの機能をいくつか切り捨てており、特に[倍精度浮動小数点](https://ja.wikipedia.org/wiki/倍精度浮動小数点 "wikilink")の演算性能は単精度の1/24となっている。そのため、倍精度対応が必要とされる分野にはGK110チップが対応することになる。

そのほか、GeForce GTX 670およびGTX 680は、[シャープ](../Page/シャープ.md "wikilink")の[4K解像度](https://ja.wikipedia.org/wiki/4K解像度 "wikilink")ディスプレイPN-K321における3840x2160ドットの60Hz映像伝送に対応するグラフィックスカードとして、AMD Radeon HD 7750/HD 7970、AMD FirePro W600/W5000/W8000、NVIDIA GeForce GTX Titan/760、NVIDIA Quadro K600/K5000などとともにシャープ公式の動作検証がなされている\[26\]。

##### GeForce GT 600 Series

GeForce GT 600シリーズは、主にFermi世代の下位モデルのリネーム製品で構成され、Keplerアーキテクチャを採用する製品はGeForce GT 640 1製品のみだったが、2013年5月のGK208コアの発表により、Keplerアーキテクチャを採用する製品が増加した。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック (CUDAコアクロック)</p></th>
<th><p>コア数</p></th>
<th><p>メモリ</p></th>
<th><p>FLOPS</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/SLI" title="wikilink">SLI</a></p></th>
<th><p>最大消費電力 (補助電源)</p></th>
<th><p>接続</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/DirectX" title="wikilink">DirectX</a><br />
<small>(Feature Level)</small></p></th>
<th><p><a href="../Page/OpenGL.md" title="wikilink">OpenGL</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SM</p></td>
<td><p><a href="../Page/CUDA.md" title="wikilink">CUDA</a></p></td>
<td><p>TeX</p></td>
<td><p>ROP</p></td>
<td><p>L2</p></td>
<td><p>バス幅</p></td>
<td><p>動作クロック</p></td>
<td><p>帯域</p></td>
<td><p>容量</p></td>
<td><p>単精度 (理論値)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 610</p></td>
<td><p>GF119 (40nm)</p></td>
<td><p>810MHz (1620MHz)</p></td>
<td><p>1</p></td>
<td><p>48</p></td>
<td><p>8</p></td>
<td><p>4</p></td>
<td><p>128KB</p></td>
<td><p>64bit</p></td>
<td><p>DDR3 1800MHz相当</p></td>
<td><p>14.4GB/s</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 620</p></td>
<td><p>GF108 (40nm)</p></td>
<td><p>700MHz (1400MHz)</p></td>
<td><p>2</p></td>
<td><p>96</p></td>
<td><p>16</p></td>
<td><p>4</p></td>
<td><p>0.13TFLOPS</p></td>
<td><p>49W</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 630 (DDR3)</p></td>
<td><p>810MHz (1620MHz)</p></td>
<td><p>256KB</p></td>
<td><p>128bit</p></td>
<td><p>28.8GB/s</p></td>
<td><p>1GB / 2GB / 4GB</p></td>
<td><p>0.16TFLOPS</p></td>
<td><p>49W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 630 (GDDR5)</p></td>
<td><p>GDDR5 3200MHz相当</p></td>
<td><p>51.2GB/s</p></td>
<td><p>1GB</p></td>
<td><p>65W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 630 Rev.2 (64bit DDR3)</p></td>
<td><p>GK208 (28nm)</p></td>
<td><p>902MHz</p></td>
<td><p>2</p></td>
<td><p>384</p></td>
<td><p>32</p></td>
<td><p>8</p></td>
<td><p>512KB</p></td>
<td><p>64bit</p></td>
<td><p>DDR3 1800MHz相当</p></td>
<td><p>14.4GB/s</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 635 (OEM)</p></td>
<td><p>967MHz</p></td>
<td><p>0.74TFLOPS</p></td>
<td><p>35W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 640 Rev.2 (GDDR5)</p></td>
<td><p>1046MHz</p></td>
<td><p>GDDR5 5000MHz相当</p></td>
<td><p>40.0GB/s</p></td>
<td><p>0.8TFLOPS</p></td>
<td><p>49W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 640</p></td>
<td><p>GK107 (28nm)</p></td>
<td><p>900MHz</p></td>
<td><p>2</p></td>
<td><p>384</p></td>
<td><p>32</p></td>
<td><p>16</p></td>
<td><p>256KB</p></td>
<td><p>128bit</p></td>
<td><p>DDR3 1800MHz相当</p></td>
<td><p>28.8GB/s</p></td>
</tr>
</tbody>
</table>

  - GT 610
    2012年5月16日販売開始。Fermi世代のGT 520のリネーム品。
  - GT 620
    2012年5月16日販売開始。Fermi世代のGT 430のメモリバス幅を半減させたもの。
  - GT 630 (DDR3)
    2012年5月16日販売開始。Fermi世代のGT 440 (DDR3)のリネーム品。DDR3メモリを4 GB搭載した製品やDVI-D出力端子を2系統搭載した製品も存在する。
  - GT 630 (GDDR5)
    2012年5月16日販売開始。Fermi世代のGT 440 (GDDR5)のリネーム品。
  - GT 630 Rev.2 (64bit DDR3)
    2013年5月29日販売開始。新しいGK208コアを採用し、メモリバス幅64bitのDDR3メモリを搭載する。
  - GT 640 Rev.2 (GDDR5)
    2013年5月29日販売開始。新しいGK208コアを採用し、メモリバス幅64bitのGDDR5メモリを搭載する。
  - GT 640
    2012年6月5日販売開始。GK107コアを採用し、メモリバス幅128bitのDDR3メモリを搭載する。

##### OEM品 (リネーム品)

  - 605 (OEM)
    510 (OEM)のリネーム品。
  - GT 640 (OEM) (192bit DDR3)
    GT 545 DDR3 (OEM)のリネーム品。
  - GT 645 (OEM)
    GTX 555 (OEM)のリネーム品。

##### GeForce GTX 600 Series

GeForce GTX 600シリーズは、Keplerアーキテクチャを採用する、ミドルレンジからハイエンドクラスの2012年 - 2013年前半の製品群である。

GTX 650 Ti BOOST以上で[Intel Turbo Boost Technologyと非常に近い機能を有するGPU](https://ja.wikipedia.org/wiki/インテル_ターボ・ブースト・テクノロジー "wikilink") Boostが搭載されている。GPUの消費電力が想定より低かった場合、想定電力に達するまでGPUコアクロックとGPUコア電圧を引き上げる機能である\[27\]。

GTX 650 Ti BOOST以上でDisplayPort 1.2出力端子を搭載し、4Kモニタの60Hz表示に対応する。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック [GPU Boost]</p></th>
<th><p>コア数</p></th>
<th><p>メモリ</p></th>
<th><p>FLOPS</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/SLI" title="wikilink">SLI</a></p></th>
<th><p>最大消費電力 (補助電源)</p></th>
<th><p>接続</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/DirectX" title="wikilink">DirectX</a><br />
<small>(Feature Level)</small></p></th>
<th><p><a href="../Page/OpenGL.md" title="wikilink">OpenGL</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SM</p></td>
<td><p><a href="../Page/CUDA.md" title="wikilink">CUDA</a></p></td>
<td><p>TeX</p></td>
<td><p>ROP</p></td>
<td><p>L2</p></td>
<td><p>バス幅</p></td>
<td><p>動作クロック</p></td>
<td><p>帯域</p></td>
<td><p>容量</p></td>
<td><p>単精度 (理論値)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 645 (OEM)</p></td>
<td><p>GK106 (28nm)</p></td>
<td><p>|824MHz [889MHz]</p></td>
<td><p>3</p></td>
<td><p>576</p></td>
<td><p>48</p></td>
<td><p>16</p></td>
<td><p>256KB</p></td>
<td><p>128bit</p></td>
<td><p>GDDR5 4000MHz相当</p></td>
<td><p>64.0GB/s</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 650</p></td>
<td><p>GK107 (28nm)</p></td>
<td><p>1058MHz</p></td>
<td><p>2</p></td>
<td><p>384</p></td>
<td><p>32</p></td>
<td><p>GDDR5 5000MHz相当</p></td>
<td><p>80.0GB/s</p></td>
<td><p>1GB / 2GB</p></td>
<td><p>0.81TFLOPS</p></td>
<td><p>64W (6pin)</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 650 Ti</p></td>
<td><p>GK106 (28nm)</p></td>
<td><p>925MHz</p></td>
<td><p>4</p></td>
<td><p>768</p></td>
<td><p>64</p></td>
<td><p>GDDR5 5400MHz相当</p></td>
<td><p>86.4GB/s</p></td>
<td><p>1.4TFLOPS</p></td>
<td><p>110W (6pin)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 650 Ti BOOST</p></td>
<td><p>980MHz [1033MHz]</p></td>
<td><p>24</p></td>
<td><p>384KB</p></td>
<td><p>192bit</p></td>
<td><p>GDDR5 6008MHz相当</p></td>
<td><p>144.2GB/s</p></td>
<td><p>1.5TFLOPS</p></td>
<td><p>2-way</p></td>
<td><p>134W (6pin)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 660</p></td>
<td><p>5</p></td>
<td><p>960</p></td>
<td><p>80</p></td>
<td><p>2GB</p></td>
<td><p>1.9TFLOPS</p></td>
<td><p>140W (6pin)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 660 Ti</p></td>
<td><p>GK104 (28nm)</p></td>
<td><p>915MHz [980MHz]</p></td>
<td><p>7</p></td>
<td><p>1344</p></td>
<td><p>112</p></td>
<td><p>2.5TFLOPS</p></td>
<td><p>150W (6pin×2)</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 670</p></td>
<td><p>32</p></td>
<td><p>512KB</p></td>
<td><p>256bit</p></td>
<td><p>192.2GB/s</p></td>
<td><p>2GB / 4GB</p></td>
<td><p>3-way</p></td>
<td><p>170W (6pin×2)</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 680</p></td>
<td><p>1006MHz [1058MHz]</p></td>
<td><p>8</p></td>
<td><p>1536</p></td>
<td><p>128</p></td>
<td><p>3TFLOPS</p></td>
<td><p>195W (6pin×2)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 690</p></td>
<td><p>GK104 (28nm)×2チップ</p></td>
<td><p>915MHz [1019MHz]</p></td>
<td><p>8×2</p></td>
<td><p>1536×2</p></td>
<td><p>128×2</p></td>
<td><p>32×2</p></td>
<td><p>512KB×2</p></td>
<td><p>256bit×2</p></td>
<td><p>192.2GB/s×2</p></td>
<td><p>2GB×2</p></td>
</tr>
</tbody>
</table>

  - GTX 650 \[28\]
    2012年9月13日発表。ロークラスモデルのGT 640と同じGK107コアを採用しているが、コアクロックが引き上げられ、メモリがDDR3からGDDR5に変更されている。補助電源を不要にした製品も発売された。同時発表の上位モデルのGTX 660と比べてコア数は2/5しか無く、性能はFermi世代のGTXクラスでは最下位モデルとなるGTX 460 SEやGTX 550 Tiと同程度でしかない。GTXクラスの安売りと苦評され、後にGT 740 (GDDR5)としてリネームされる事になる。
  - GTX 650 Ti \[29\]
    2012年10月9日発表。同年9月13日発表のGTX 650とGTX 660の間で2倍以上の性能差があり、その中間付近を埋めるエントリーミドルレンジモデル。上位モデルであるGTX 660と同じGK106コアを採用しているが、5基のSMX中の1基のSMXが無効化されており、メモリバス幅が192bitから128bitに抑えられている。また、GPUコアクロックの自動引き上げ機能であるGPU Boostが非対応に、SLIも非対応になっている。性能はGTX 650の約1.5倍。
  - GTX 650 Ti BOOST \[30\]
    2013年3月26日発表。上位モデルであるGTX 660との違いは、5基のSMX中の1基のSMXが無効化されている点のみで、その他のコアクロックやメモリ周りは同じ。性能はGTX 650の約1.9倍。性能も価格も消費電力も上位モデルのGTX 660に近く、早々と終息してしまう。
  - GTX 660 \[31\]
    2012年9月13日発表。フルスペックのGK106コアを採用するミドルレンジモデル。5基のSMXで3基のGPCを構成する。64bitメモリコントローラが3基のため、2 GB(8チップ)のメモリ中1.5 GBを超えた分は64bit幅でのアクセスとなり、帯域が1/3に制限される。6ピン補助電源は1系統だけ必要で、6ピン補助電源が2系統必要なGTX 760と補助電源が不要なGTX 750 Tiの発売後も、その隙間を埋めるモデルとしてGTX 660は存続した。
  - GTX 660 Ti \[32\]
    2012年8月16日発表。上位モデルのGTX 670からメモリバス幅が192bitに抑えられ、メモリ周りは下位モデルのGTX 660と同じとなっている。
  - GTX 670 \[33\]
    2012年5月10日発表。ハイエンドモデルのGTX 680と同じGK104コアを採用しているが、8基のSMX中の1基のSMXが無効化されている。コアクロックはGTX 680の9割程度に抑えられているが、メモリ周りはGTX 680と全く同じである。リファレンスデザインでは、基板から大きくはみ出したGPUクーラーが特徴的である。基板のみであれば170mm程度のサイズにもかかわらず、クーラーが70mmも基板よりも大きい。その為に補助電源コネクタがカードの中央付近にあり、少々奇異に感じるかもしれない。性能はGTX 580を上回る。
  - GTX 680 \[34\]
    2012年3月22日発表。フルスペックのGK104コアを採用し、8基のSMXで4基のGPCを構成する。トランジスタ数がGTX 580と比べて18％のみの増加でありながら、CUDAコアは3倍、テクスチャユニットは2倍となった。メモリバス幅が384bitから256bitに削減されているが、メモリクロックが1.5倍に高速化された為、メモリ帯域は変わっていない。
    TXAAといわれる新しい[アンチエイリアシング](https://ja.wikipedia.org/wiki/アンチエイリアシング "wikilink")手法をハードウェアでサポートすることによって、GPUへの負荷を減らしながら従来よりも高品質なAA処理が可能となっており、GTX 580を3枚使用したデモをGTX 680 1枚で行うことを可能にしている。また1枚で画面を4出力することができ、3D Vision Surroundに対応しているのでトリプルヘッドのためにSLIを組む必要はない。
    NVIDIA AdaptiveV-Syncによって、画面のティアリングとフレームレートのカクツキを最小限に抑えることができる。
    Intel X79 ExpressプラットフォームがPCIe Gen3に対応しておらず動作確認が完全にとれるまで無効としていると説明していたが、2012年6月現在、NVIDIAはX79プラットフォームの各社マザーボードでのマザーボード-CPU間の通信タイミングに開きが見られるためX79プラットフォームでのPCIe Gen3対応は見送られた。なお公式ではサポートを行わない条件においてX79でのPCIe Gen3を有効化する無保証パッチを配布している\[35\]。
  - GTX 690 \[36\]
    2012年4月29日発表。GTX 680に搭載されているフルスペックのGK104コアを2基搭載した製品である。本製品はコアクロックをGTX 680に比べて落としているものの、CUDAコア数やメモリ周りの仕様はGTX 680と変わらない。GPUクーラーのファンカバーは[マグネシウム合金](../Page/マグネシウム合金.md "wikilink")、それ以外のクーラーカバーは[クロムメッキ](https://ja.wikipedia.org/wiki/クロムメッキ "wikilink")処理が施された[アルミ](https://ja.wikipedia.org/wiki/アルミ "wikilink")素材を採用し、それぞれのGPUにはベイパーチャンバー式ヒートシンクが搭載されている。なお中央のファンは3000rpmで回転している。冷却性能の向上に注力しているが、GTX 680二枚をSLIで動作させるよりも騒音が小さい。
    電源は10フェーズで基板は10層となっている。起動中は側面のGTX 690のロゴが緑色に光る。消費電力は300 W。リファレンスデザインでは補助電源は8ピンが2系統必要となる。インターフェイスはPCIe Gen3、ディスプレイインターフェイスはDual-Link DVI×3、Mini DisplayPort 1.2。カード長は279mmとなり、GTX 580から1mmだけ伸びている。
    なお、前世代までのデュアルチップカードでは、ブリッジチップとしてnForce 200が採用されていたが、PCIe Gen3に対応する為かブリッジチップにはLX Technology製のPEX 8747が採用されている。

#### GeForce 700 Series

##### GeForce GT 700 Series

GeForce GT 700シリーズは、主にKeplerアーキテクチャを採用するGeForce 600シリーズの下位モデルに調整を加えたリネーム製品で構成されるが、一部にFermi世代のリネーム製品も含まれる。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック (CUDAコアクロック)</p></th>
<th><p>コア数</p></th>
<th><p>メモリ</p></th>
<th><p>FLOPS</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/SLI" title="wikilink">SLI</a></p></th>
<th><p>最大消費電力</p></th>
<th><p>接続</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/DirectX" title="wikilink">DirectX</a><br />
<small>(Feature Level)</small></p></th>
<th><p><a href="../Page/OpenGL.md" title="wikilink">OpenGL</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SM</p></td>
<td><p><a href="../Page/CUDA.md" title="wikilink">CUDA</a></p></td>
<td><p>TeX</p></td>
<td><p>ROP</p></td>
<td><p>L2</p></td>
<td><p>バス幅</p></td>
<td><p>動作クロック</p></td>
<td><p>帯域</p></td>
<td><p>容量</p></td>
<td><p>単精度 (理論値)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 705 (OEM)</p></td>
<td><p>GF119 (40nm)</p></td>
<td><p>874MHz (1748MHz)</p></td>
<td><p>1</p></td>
<td><p>48</p></td>
<td><p>8</p></td>
<td><p>4</p></td>
<td><p>128KB</p></td>
<td><p>64bit</p></td>
<td><p>DDR3 1650MHz相当</p></td>
<td><p>13.2GB/s</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 710</p></td>
<td><p>GK208 (28nm)</p></td>
<td><p>954MHz</p></td>
<td><p>1</p></td>
<td><p>192</p></td>
<td><p>16</p></td>
<td><p>8</p></td>
<td><p>512KB</p></td>
<td><p>DDR3 1800MHz相当</p></td>
<td><p>14.4GB/s</p></td>
<td><p>1GB / 2GB</p></td>
</tr>
<tr class="even">
<td><p>GDDR5 5012MHz相当</p></td>
<td><p>40.1GB/s</p></td>
<td><p>2GB</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>??</p></td>
<td><p>32bit</p></td>
<td><p>20.0GB/s</p></td>
<td><p>1GB</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 720</p></td>
<td><p>797MHz</p></td>
<td><p>512KB</p></td>
<td><p>64bit</p></td>
<td><p>DDR3 1600MHz相当</p></td>
<td><p>12.8GB/s</p></td>
<td><p>1GB / 2GB</p></td>
<td><p>0.3TFLOPS</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GDDR5 5012MHz相当</p></td>
<td><p>40.1GB/s</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 730 (128bit DDR3)</p></td>
<td><p>GF108 (40nm)</p></td>
<td><p>700MHz (1400MHz)</p></td>
<td><p>2</p></td>
<td><p>96</p></td>
<td><p>16</p></td>
<td><p>4</p></td>
<td><p>256KB</p></td>
<td><p>128bit</p></td>
<td><p>DDR3 1800MHz相当</p></td>
<td><p>28.8GB/s</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 730 (64bit DDR3)</p></td>
<td><p>GK208 (28nm)</p></td>
<td><p>902MHz</p></td>
<td><p>2</p></td>
<td><p>384</p></td>
<td><p>32</p></td>
<td><p>8</p></td>
<td><p>512KB</p></td>
<td><p>64bit</p></td>
<td><p>14.4GB/s</p></td>
<td><p>1GB / 2GB</p></td>
</tr>
<tr class="even">
<td><p>GeForce GT 730 (GDDR5)</p></td>
<td><p>GDDR5 5012MHz相当</p></td>
<td><p>40.1GB/s</p></td>
<td><p>38W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 740</p></td>
<td><p>GK107 (28nm)</p></td>
<td><p>993MHz</p></td>
<td><p>2</p></td>
<td><p>384</p></td>
<td><p>32</p></td>
<td><p>16</p></td>
<td><p>256KB</p></td>
<td><p>128bit</p></td>
<td><p>DDR3 1800MHz相当</p></td>
<td><p>28.8GB/s</p></td>
</tr>
<tr class="even">
<td><p>GeForce GT 740 (GDDR5)</p></td>
<td><p>GDDR5 5000MHz相当</p></td>
<td><p>80.0GB/s</p></td>
<td><p>64W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

  - GT 710
    2016年1月25日発表。GT 730 (64bit DDR3)から、2基のSMX中の1基を無効化したローエンドモデル。旧製品のGT 720からコアクロックとメモリクロックが引き上げられている。デュアルリンクDVI-D出力端子、HDMI 1.4a出力端子、D-Sub15ピンのアナログ出力端子を搭載し、WQHD(2560×1440)モニタ表示に対応する。
    2017年8月以降はGDDR5メモリを搭載する製品も販売されているが、1 GB版はメモリバス幅が32bitに縮小されている。
  - GT 720
    2014年8月13日販売開始。GT 730 (64bit DDR3)から、2基のSMX中の1基を無効化したローエンドモデル。GDDR5版も存在するが、日本国内ではOEM品しか流通していない。高クロック化されたGT 710の登場で終息した。
  - GT 730 (128bit DDR3)
    2014年6月18日発表。Fermi世代のGT 430のリネーム品。GT 440 (DDR3)のリネーム品であるGT 630 (DDR3)からコアクロックが引き下げられ、性能はGT 710以下にまで低下した。DDR3メモリを4 GB搭載した製品やDVI-D出力端子を2系統搭載した製品も存在する。
  - GT 730 (64bit DDR3)
    2014年6月18日発表。GT 630 Rev.2 (64bit DDR3)のリネーム品。HDMI 1.4出力端子を4系統搭載した製品も存在する。
  - GT 730 (GDDR5)
    2014年6月18日発表。GT 640 Rev.2 (GDDR5)のコアクロックを902 MHzに引き下げたもの。
  - GT 740
    2014年5月30日販売開始。GT 640のコアクロックを900 MHzから993 MHzに引き上げたもの。
  - GT 740 (GDDR5)
    2014年5月30日販売開始。GTX 650のコアクロックを1058 MHzから993 MHzに引き下げたもの。実際にはベンダー各社からコアクロック1058 MHzのOC版が出揃い、GTX 650の補助電源不要版となった。

##### GeForce GTX 700 Series

GeForce GTX 700シリーズは、Keplerアーキテクチャ - 第1世代Maxwellアーキテクチャを採用する、ミドルレンジからハイエンドクラスの2013年後半 - 2014年前半の製品群である。

Keplerアーキテクチャでは192基のCUDAコアでSMXを構成していたのに対し、Maxwellアーキテクチャでは128基のCUDAコアでSMM(Maxwell Streaming Multiprocessor)を構成。128基のCUDAコアを4つのプロセシングブロックに分割し、32個のCUDAコア毎にシンプルな制御ロジックを配置、L2キャッシュを大幅に増加させたことで、コア当たりのパフォーマンスが35%向上、電力効率は2倍になったという\[37\]。

GTX 760以上でDisplayPort 1.2出力端子を標準で搭載し（GTX 750/GTX 750 TiでDisplayPort 1.2出力端子を搭載する製品もある）、4Kモニタの60Hz表示に対応する。GTX 750 Ti以下では、デュアルリンクDVI出力またはHDMI 1.4出力でWQHDモニタの60Hz表示、HDMI 1.4出力で4Kモニタの30Hz表示までの対応となる。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック [GPU Boost]</p></th>
<th><p>コア数</p></th>
<th><p>メモリ</p></th>
<th><p>FLOPS</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/SLI" title="wikilink">SLI</a></p></th>
<th><p>最大消費電力 (補助電源)</p></th>
<th><p>接続</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/DirectX" title="wikilink">DirectX</a><br />
<small>(Feature Level)</small></p></th>
<th><p><a href="../Page/OpenGL.md" title="wikilink">OpenGL</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SM</p></td>
<td><p><a href="../Page/CUDA.md" title="wikilink">CUDA</a></p></td>
<td><p>TeX</p></td>
<td><p>ROP</p></td>
<td><p>L2</p></td>
<td><p>バス幅</p></td>
<td><p>動作クロック</p></td>
<td><p>帯域</p></td>
<td><p>容量</p></td>
<td><p>単精度 (理論値)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 745 (OEM)</p></td>
<td><p>GM107 (28nm)</p></td>
<td><p>1033MHz</p></td>
<td><p>3</p></td>
<td><p>384</p></td>
<td><p>24</p></td>
<td><p>16</p></td>
<td><p>2MB</p></td>
<td><p>128bit</p></td>
<td><p>DDR3 1800MHz相当</p></td>
<td><p>28.8GB/s</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 750</p></td>
<td><p>1020MHz [1085MHz]</p></td>
<td><p>4</p></td>
<td><p>512</p></td>
<td><p>32</p></td>
<td><p>GDDR5 5000MHz相当</p></td>
<td><p>80.0GB/s</p></td>
<td><p>1GB / 2GB</p></td>
<td><p>1TFLOPS</p></td>
<td><p>55W</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 750 Ti</p></td>
<td><p>5</p></td>
<td><p>640</p></td>
<td><p>40</p></td>
<td><p>GDDR5 5400MHz相当</p></td>
<td><p>86.4GB/s</p></td>
<td><p>2GB / 4GB[38]</p></td>
<td><p>1.3TFLOPS</p></td>
<td><p>60W</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 760 (192bit) (OEM)</p></td>
<td><p>GK104 (28nm)</p></td>
<td><p>824MHz [889MHz]</p></td>
<td><p>6</p></td>
<td><p>1152</p></td>
<td><p>96</p></td>
<td><p>24</p></td>
<td><p>384KB</p></td>
<td><p>192bit</p></td>
<td><p>GDDR5 5600MHz相当</p></td>
<td><p>134.4GB/s</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 760</p></td>
<td><p>980MHz [1033MHz]</p></td>
<td><p>32</p></td>
<td><p>512KB</p></td>
<td><p>256bit</p></td>
<td><p>GDDR5 6008MHz相当</p></td>
<td><p>192.2GB/s</p></td>
<td><p>2GB / 4GB</p></td>
<td><p>2.3TFLOPS</p></td>
<td><p>170W (6pin×2)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 770</p></td>
<td><p>1046MHz [1085MHz]</p></td>
<td><p>8</p></td>
<td><p>1536</p></td>
<td><p>128</p></td>
<td><p>GDDR5 7010MHz相当</p></td>
<td><p>224.3GB/s</p></td>
<td><p>2GB / 4GB</p></td>
<td><p>3.2TFLOPS</p></td>
<td><p>230W (6pin+8pin)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 780</p></td>
<td><p>GK110 (28nm)</p></td>
<td><p>863MHz [900MHz]</p></td>
<td><p>12</p></td>
<td><p>2304</p></td>
<td><p>192</p></td>
<td><p>48</p></td>
<td><p>1.5MB</p></td>
<td><p>384bit</p></td>
<td><p>GDDR5 6008MHz相当</p></td>
<td><p>288.4GB/s</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 780 Ti</p></td>
<td><p>875MHz [928MHz]</p></td>
<td><p>15</p></td>
<td><p>2880</p></td>
<td><p>240</p></td>
<td><p>GDDR5 7000MHz相当</p></td>
<td><p>336.0GB/s</p></td>
<td><p>3GB</p></td>
<td><p>5TFLOPS</p></td>
<td><p>4-way &lt;!-- NVIDIA公式情報がなく、存在自体が怪しいため、コメントアウト。英語版Wikipediaの"GeForce 700 series"にも該当製品は記載されていない。</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 780 Ti Special Black Edition</p></td>
<td><p>GK110 (28nm)</p></td>
<td></td>
<td><p>2880</p></td>
<td><p>240</p></td>
<td><p>48</p></td>
<td><p>GDDR5 7000MH相当 (384bit)</p></td>
<td><p>336.0GB/s</p></td>
<td><p>Unknown</p></td>
<td><p>Unknown</p></td>
<td><p>Unknown</p></td>
</tr>
</tbody>
</table>

  - GTX 750、GTX 750 Ti \[39\]
    2014年2月18日発表。第1世代MaxwellアーキテクチャのGM107コアを採用するエントリーミドルレンジモデル。L2キャッシュを2 MB搭載する。GTX 650 Tiの後継としてGTX 660の下位に位置付けられる(GTX 660は存続)。電力効率に優れたMaxwellアーキテクチャの採用により消費電力は半減し、補助電源が不要となった。同年5月にはロープロファイル対応の製品も発売された。
    GTXクラスの最下位モデルの性能は、GTX 460 SE(150 W)→GTX 550 Ti(116 W)→GTX 650(64 W)でほぼ変わらなかったが、GTX 750によって大きく底上げされた。GTX 750(55 W)の性能はGTX 650の約1.65倍で、GTX 650 Ti(110 W)から約10％上昇した。
    GTX 750 Ti(60 W)の性能はGTX 650の約1.9倍で、GTX 650 Ti BOOST(134 W)と同程度となった。その低価格と低消費電力から2017年初頭まで人気は続いた。（最終的にGTX 750 Tiの価格は9,000円程度まで下落した）
  - GTX 760 \[40\]
    2013年6月25日発表。GTX 660 Tiの後継と位置付けられ、GTX 660 Ti、GTX 670、GTX 680と同じGK104コアを採用する。GTX 660 TiはGTX 670からメモリバス幅が192bitに抑えられていたのに対し、GTX 760はGTX 670からSMX 1基が無効化され、コアクロックが引き上げられている。性能はGTX 660 Tiと同程度だが\[41\]、消費電力が高い。
  - GTX 770 \[42\]
    2013年5月30日発表。GTX 680の後継と位置付けられ、GTX 680と同じフルスペックのGK104コアを採用し、8基のSMXで4基のGPCを構成する。GDDR5メモリはGTX 680の6.0Gbps品から7.0Gbps品に変更されたが、消費電力が上がって6ピン補助電源と8ピン補助電源が1系統ずつ必要になった。
  - GTX 780 \[43\]
    2013年5月23日発表。GTX TITAN Black同じGK110コアを採用するが、SMX 15基中の3基が無効化されている。GeForce TITANシリーズにあった「DPフルスピードモード」は利用できない。
  - GTX 780 Ti \[44\]
    2013年11月7日発表。GTX TITAN Blackと同じフルスペックのGK110コアを採用し、15基のSMXで5基のGPCを構成する。GeForce TITANシリーズにあった「DPフルスピードモード」は利用できない。

##### GeForce GTX TITAN Series

ハイエンドの中でもさらに最上位クラスの製品ブランドとして、GeForce GTX TITANシリーズが追加された。ただし、製品世代としては、GeForce GTX 700シリーズと同列である。

GeForce GTX TITANシリーズのGK110コアのSMXの中には64基の倍精度演算ユニットも搭載されている。倍精度演算ユニットは、GK104コアの単精度演算ユニットによる倍精度演算の8分の1のクロック数で倍精度演算するが、コアクロックの8分の1のクロック速度で動作している。これをNVIDIA Control Panelの設定を変更することで、コアと同クロックで動作させられるように変更できる。この倍精度浮動小数点演算のフルスピードモード化機能を「DPフルスピードモード」と呼ぶ。但し、DPフルスピードモード時は消費電力が上がり、コアクロックが抑えられるため、実際の倍精度演算性能は理論値の8倍には届かない。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック [GPU Boost]</p></th>
<th><p>コア数</p></th>
<th><p>メモリ</p></th>
<th><p>FLOPS</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/SLI" title="wikilink">SLI</a></p></th>
<th><p>最大消費電力 (補助電源)</p></th>
<th><p>接続</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/DirectX" title="wikilink">DirectX</a><br />
<small>(Feature Level)</small></p></th>
<th><p><a href="../Page/OpenGL.md" title="wikilink">OpenGL</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SM</p></td>
<td><p><a href="../Page/CUDA.md" title="wikilink">CUDA</a></p></td>
<td><p>TeX</p></td>
<td><p>ROP</p></td>
<td><p>L2</p></td>
<td><p>バス幅</p></td>
<td><p>動作クロック</p></td>
<td><p>帯域</p></td>
<td><p>容量</p></td>
<td><p>単精度 (理論値)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX TITAN</p></td>
<td><p>GK110 (28nm)</p></td>
<td><p>836MHz [876MHz]</p></td>
<td><p>14</p></td>
<td><p>2688</p></td>
<td><p>224</p></td>
<td><p>48</p></td>
<td><p>1.5MB</p></td>
<td><p>384bit</p></td>
<td><p>GDDR5 6008MHz相当</p></td>
<td><p>288.4GB/s</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX TITAN Black</p></td>
<td><p>889MHz [980MHz]</p></td>
<td><p>15</p></td>
<td><p>2880</p></td>
<td><p>240</p></td>
<td><p>GDDR5 7000MHz相当</p></td>
<td><p>336.0GB/s</p></td>
<td><p>5.1TFLOPS</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX TITAN Z</p></td>
<td><p>GK110 (28nm)×2チップ</p></td>
<td><p>705MHz [876MHz]</p></td>
<td><p>15×2</p></td>
<td><p>2880×2</p></td>
<td><p>240×2</p></td>
<td><p>48×2</p></td>
<td><p>1.5MB×2</p></td>
<td><p>384bit×2</p></td>
<td><p>336.0GB/s×2</p></td>
<td><p>|6GB×2</p></td>
</tr>
</tbody>
</table>

  - GTX TITAN \[45\]

<!-- end list -->

  -
    2013年2月19日発表。先に「Tesla K20X」として投入されていたGK110コアを採用するコンシューマ向けモデル。製品名については、Tesla K20Xを採用し、[TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")で2012年11月に性能ランキング1位となった米[オークリッジ国立研究所](../Page/オークリッジ国立研究所.md "wikilink")の[スーパーコンピューター](https://ja.wikipedia.org/wiki/スーパーコンピューター "wikilink")「[タイタン](https://ja.wikipedia.org/wiki/タイタン_\(スーパーコンピュータ\) "wikilink")」\[46\]に由来している。
    GPUコアのSMX 15基中の1基が無効化されている。
    浮動小数点数演算性能は、単精度が4.5 TFLOPS（GTX 680は3.09 TFLOPS）、DPフルスピードモード時の倍精度が1.5 TFLOPS（理論値）（GTX 680は0.13 TFLOPS）。
  - GTX TITAN Black \[47\]
    2014年2月18日発表。フルスペックのGK110コアを採用。GTX TITANと比べて動作クロックとメモリークロックが引き上げられている。
    浮動小数点数演算性能は、単精度が5.1 TFLOPS、DPフルスピードモード時の倍精度が1.7 TFLOPS（理論値）。
  - GTX TITAN Z \[48\]
    2014年3月25日発表。フルスペックのGK110コアを2基搭載するデュアルGPU。接続にトリプルスロット幅の空きを必要とする。
    浮動小数点数演算性能は、単精度が8.1 TFLOPS、DPフルスピードモード時の倍精度が2.7 TFLOPS（理論値）。
    発売時の価格は、史上最高の40万円 - \[49\]。

<!-- end list -->

  - ＜コアでまとめ＞

[サムネイル](https://ja.wikipedia.org/wiki/ファイル:Kepler001.gif "wikilink")

  -
    {| class="wikitable" style="font-size:80%;"

\! rowspan="2" |コア名 \! rowspan="2" |SM数 \! rowspan="2" |メモリバス幅 \! rowspan="2" |メモリタイプ \! colspan="2" |GeForce 600シリーズ \! colspan="2" |GeForce 700シリーズ |- \!製品名\!\!コアクロック \!製品名\!\!コアクロック |- | Fermi GF119||1 | rowspan="2" |64bit|| rowspan="2" |DDR3 |GT 610 = GT 520||810MHz | rowspan="2" colspan="2" | |- | rowspan="3" |Fermi GF108|| rowspan="3" |2 |GT 620||700MHz |- | rowspan="2" |128bit||DDR3 |GT 630 (DDR3) = GT 440 (DDR3)|| rowspan="2" |810MHz |GT 730 (128bit DDR3) = GT 430||700MHz |- |GDDR5||GT 630 (GDDR5) = GT 440 (GDDR5) | colspan="2" | |- | rowspan="5" |Kepler GK208|| rowspan="3" |1 | 32bit|| rowspan="2" |GDDR5 | rowspan="3" colspan="2" | |GT 710 (GDDR5 1GB)|| rowspan="3" |954MHz |- | rowspan="4" |64bit |GT 710 (GDDR5 2GB) |- |DDR3 |GT 710 (DDR3) |- | rowspan="4" |2 |DDR3||GT 630 Rev.2 (64bit DDR3)||902MHz |GT 730 (64bit DDR3)|| rowspan="2" |902MHz |- |GDDR5||GT 640 Rev.2 (GDDR5)||1046MHz |GT 730 (GDDR5) |- | rowspan="2" |Kepler GK107 | rowspan="5" |128bit||DDR3 |GT 640||900MHz |GT 740|| rowspan="2" |993MHz |- |GDDR5||GTX 650||1058MHz |GT 740 (GDDR5) |- | rowspan="2" |Maxwell GM107||4 | rowspan="15" |GDDR5 | rowspan="2" colspan="2" | |GTX 750|| rowspan="2" |1020MHz |- |5 |GTX 750 Ti |- | rowspan="3" |Kepler GK106 | rowspan="2" |4||GTX 650 Ti |925MHz | rowspan="3" colspan="2" | |- | rowspan="2" |192bit |GTX 650 Ti BOOST|| rowspan="2" |980MHz |- |5 |GTX 660 |- | rowspan="4" |Kepler GK104 |6 |256bit | colspan="2" | |GTX 760 |980MHz |- | rowspan="2" |7 |192bit||GTX 660 Ti|| rowspan="2" |915MHz | rowspan="2" colspan="2" | |- | rowspan="2" |256bit |GTX 670 |- |8||GTX 680||1006MHz |GTX 770 |1046MHz |- | rowspan="4" |Kepler GK110 |12 | rowspan="4" | 384bit | rowspan="4" colspan="2" | |GTX 780 |863MHz |- |14 |GTX TITAN |836MHz |- | rowspan="2" |15 |GTX 780 Ti |875MHz |- |GTX TITAN Black |889MHz |- |Kepler GK104×2チップ |8×2 |256bit×2 |GTX 690 |915MHz | colspan="2" | |- |Kepler GK110×2チップ |15×2 |384bit×2 | colspan="2" | |GTX TITAN Z |705MHz |}

#### GeForce 900 Series

GeForce 900シリーズは、第2世代Maxwellアーキテクチャを採用する、ミドルレンジからハイエンドクラスの2014年後半 - 2015年の製品群である。

第2世代Maxwellアーキテクチャでは、新たなメモリ圧縮技術を採用しメモリのアクセス効率が高まった。MFAA(Multi-Frame Sampled Anti Aliasing)技術に対応\[50\]。64bitメモリコントローラ1基に対するROPユニットは8基から16基に変更された\[51\]。GTX 970以上でVR(Virtual Reality)をサポートする\[52\]。

HDMI 2.0出力端子×1とDisplayPort 1.2出力端子×3を搭載し、4画面の4Kモニタの60Hz表示に対応する。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック [GPU Boost]</p></th>
<th><p>コア数</p></th>
<th><p>メモリ</p></th>
<th><p>FLOPS</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/SLI" title="wikilink">SLI</a></p></th>
<th><p>VR</p></th>
<th><p>最大消費電力 (補助電源)</p></th>
<th><p>接続</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/DirectX" title="wikilink">DirectX</a><br />
<small>(Feature Level)</small></p></th>
<th><p><a href="../Page/OpenGL.md" title="wikilink">OpenGL</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SM</p></td>
<td><p><a href="../Page/CUDA.md" title="wikilink">CUDA</a></p></td>
<td><p>TeX</p></td>
<td><p>ROP</p></td>
<td><p>L2</p></td>
<td><p>バス幅</p></td>
<td><p>動作クロック</p></td>
<td><p>帯域</p></td>
<td><p>容量</p></td>
<td><p>単精度 (理論値)</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 950</p></td>
<td><p>GM206 (28nm)</p></td>
<td><p>1024MHz [1188MHz]</p></td>
<td><p>6</p></td>
<td><p>768</p></td>
<td><p>48</p></td>
<td><p>32</p></td>
<td><p>1MB</p></td>
<td><p>128bit</p></td>
<td><p>GDDR5 6.6GHz相当</p></td>
<td><p>105.6GB/s</p></td>
<td><p>2GB</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 960</p></td>
<td><p>1127MHz [1178MHz]</p></td>
<td><p>8</p></td>
<td><p>1024</p></td>
<td><p>64</p></td>
<td><p>GDDR5 7GHz相当</p></td>
<td><p>112GB/s</p></td>
<td><p>2GB / 4GB</p></td>
<td><p>2.3TFLOPS</p></td>
<td><p>120W (6pin)</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 970</p></td>
<td><p>GM204 (28nm)</p></td>
<td><p>1050MHz [1178MHz]</p></td>
<td><p>13</p></td>
<td><p>1664</p></td>
<td><p>104</p></td>
<td><p>56</p></td>
<td><p>1.75MB</p></td>
<td><p>224bit (3.5GB) + 32bit (0.5GB)</p></td>
<td><p>196GB/s (3.5GB) + 28GB/s (0.5GB)</p></td>
<td><p>4GB (3.5GB + 0.5GB)</p></td>
<td><p>3.5TFLOPS</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 980</p></td>
<td><p>1126MHz [1216MHz]</p></td>
<td><p>16</p></td>
<td><p>2048</p></td>
<td><p>128</p></td>
<td><p>64</p></td>
<td><p>2MB</p></td>
<td><p>256bit</p></td>
<td><p>224GB/s</p></td>
<td><p>4GB</p></td>
<td><p>4.6TFLOPS</p></td>
<td><p>4-way</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 980 Ti</p></td>
<td><p>GM200 (28nm)</p></td>
<td><p>1000MHz [1075MHz]</p></td>
<td><p>22</p></td>
<td><p>2816</p></td>
<td><p>176</p></td>
<td><p>96</p></td>
<td><p>3MB</p></td>
<td><p>384bit</p></td>
<td><p>336GB/s</p></td>
<td><p>6GB</p></td>
<td><p>5.6TFLOPS</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX TITAN X</p></td>
<td><p>24</p></td>
<td><p>3072</p></td>
<td><p>192</p></td>
<td><p>12GB</p></td>
<td><p>6.1TFLOPS</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

  - GTX 950 \[53\] \[54\] \[55\]
    2015年8月20日発表。GTX 960と同じGM206コアを採用するが、SMM 8基中の2基が無効化され、コア数や消費電力はGTX 960の3/4となる。価格的にも性能的にもGTX 750 TiとGTX 960の隙間を埋めるモデルとして登場し、性能はGTX 750 Ti比で約1.5倍になったが\[56\]、消費電力も1.5倍に増えて補助電源が必要な上に2万円前後という価格に割高感があり、2万円台前半に価格がこなれていた上位のGTX 960に人気が集まった。2016年3 - 4月には消費電力を抑えて補助電源を不要にした製品、5月にはロープロファイル対応の製品も発売された。（しかし半年後の同年10月には次世代Pascalアーキテクチャ採用のGTX 1050を搭載した製品がより安価に発売される事になる）
  - GTX 960 \[57\]
    2015年1月22日発表。フルスペックのGM206コアを採用するミドルレンジモデル。GM206コアはGM204コアの半分となる2基のGPC(8基のSMM)で構成されていて、コア数やメモリ帯域はGTX 980の半分となる。GM206コアはH.265ハードウェアデコーダを統合しており、ミドルレンジでも4K/60fpsのデコードが可能となっている。
    スペック的にはGTX 950 Tiのような製品で、性能はGTX 950比で1.2倍程度に過ぎない。前世代のGTX 760と比べてメモリバス幅が256bitから128bitに半減しているため、高負荷時の性能はGTX 760と僅差にまで落ち込む。
  - GTX 970 \[58\]
    2014年9月19日発表。GTX 980と同じGM204コアを採用するが、SMM 16基中の3基が無効化されている。当初はメモリ周りはGTX 980と同じとされていたが、実際にはROPユニットが64基から56基に削減され、L2キャッシュも32bit幅1基分0.25 MB少なかった。このため、4 GBのメモリ中3.5 GBまでは帯域が7/8に、3.5 GBを超えた分は帯域が1/8に制限されていた\[59\]。NVIDIAは、2015年1月にスペックを下方修正した\[60\] \[61\]。また、電源周りの回路に問題があり、高fpsで描画時にコイル鳴きが発生する製品が多い。
  - GTX 980 \[62\] \[63\]
    2014年9月19日発表。フルスペックのGM204コアを採用し、4基のGPC(16基のSMM)で構成されている。7.0GbpsのGDDR5メモリを搭載し、メモリ圧縮技術により9.3Gbps相当のパフォーマンスを発揮する。GM204コアはH.265/HEVCハードウェアエンコーダを統合する。
  - GTX 980 Ti \[64\] \[65\] \[66\]
    2015年6月1日発表。GTX TITAN Xと同じGM200コアを採用するハイエンドモデル。SMM 24基中の2基が無効化されている。
  - GTX TITAN X \[67\] \[68\]
    2015年3月18日発表。フルスペックのGM200コアを採用し、6基のGPC(24基のSMM)で構成されている。「TITAN」の名を冠してはいるが、Kepler世代のGeForce GTX TITANシリーズとは異なり、DPフルスピードモードはサポートされない。

#### GeForce 10 Series

GeForce 10シリーズは、Pascalアーキテクチャを採用する、ロークラスからハイエンドクラスの2016年 - 2018年前半の製品群である。\[69\]。

Pascalアーキテクチャでは、16 nmプロセス採用によって、消費電力の増加を抑えながらコアクロックが大幅に引き上げられた。新開発された「SLI HB」と呼ばれるブリッジを推奨\[70\]、3-way/4-wayのSLI構成は非推奨となっている\[71\]。75 - 150 Wの補助電源の供給方法は、従来の6pin×2から8pin×1に変更された。 GTX 1060以上でVR(Virtual Reality)をサポートする\[72\]。GTX 1080以上で、新たなメモリ規格のGDDR5Xメモリの採用により、メモリ帯域が向上している。

HDMI 2.0bやDisplayPort 1.4の最新のインターフェイスに対応。アナログ映像信号出力は廃止された。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック [GPU Boost]</p></th>
<th><p>コア数</p></th>
<th><p>メモリ</p></th>
<th><p>FLOPS</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/SLI" title="wikilink">SLI</a></p></th>
<th><p>VR</p></th>
<th><p>最大消費電力 (補助電源)</p></th>
<th><p>接続</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/DirectX" title="wikilink">DirectX</a><br />
<small>(Feature Level)</small></p></th>
<th><p><a href="../Page/OpenGL.md" title="wikilink">OpenGL</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SM</p></td>
<td><p><a href="../Page/CUDA.md" title="wikilink">CUDA</a></p></td>
<td><p>TeX</p></td>
<td><p>ROP</p></td>
<td><p>L2</p></td>
<td><p>バス幅</p></td>
<td><p>動作クロック</p></td>
<td><p>帯域</p></td>
<td><p>容量</p></td>
<td><p>単精度 (理論値)</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 1030</p></td>
<td><p>GP108 (14nm)</p></td>
<td><p>1227MHz [1468MHz]</p></td>
<td><p>3</p></td>
<td><p>384</p></td>
<td><p>24</p></td>
<td><p>16</p></td>
<td><p>0.5MB</p></td>
<td><p>64bit</p></td>
<td><p>GDDR5 6GHz相当</p></td>
<td><p>48GB/s</p></td>
<td><p>2GB</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 1030 (DDR4版)</p></td>
<td><p>1151MHz [1379MHz]</p></td>
<td><p>SDDR4 2GHz相当</p></td>
<td><p>16.8GB/s</p></td>
<td><p>0.88TFLOPS</p></td>
<td><p>20W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 1050 (2GB)</p></td>
<td><p>GP107 (14nm)</p></td>
<td><p>1354MHz [1455MHz]</p></td>
<td><p>5</p></td>
<td><p>640</p></td>
<td><p>40</p></td>
<td><p>32</p></td>
<td><p>1MB</p></td>
<td><p>128bit</p></td>
<td><p>GDDR5 7GHz相当</p></td>
<td><p>112GB/s</p></td>
<td><p>1.7TFLOPS</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 1050 (3GB)</p></td>
<td><p>1392MHz [1518MHz]</p></td>
<td><p>6</p></td>
<td><p>768</p></td>
<td><p>48</p></td>
<td><p>24</p></td>
<td><p>0.75MB</p></td>
<td><p>96bit</p></td>
<td><p>84GB/s</p></td>
<td><p>3GB</p></td>
<td><p>2.1TFLOPS</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 1050 Ti</p></td>
<td><p>1290MHz [1392MHz]</p></td>
<td><p>32</p></td>
<td><p>1MB</p></td>
<td><p>128bit</p></td>
<td><p>112GB/s</p></td>
<td><p>4GB</p></td>
<td><p>2TFLOPS</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 1060 (3GB)</p></td>
<td><p>GP106 (16nm)</p></td>
<td><p>1506MHz [1709MHz]</p></td>
<td><p>9</p></td>
<td><p>1152</p></td>
<td><p>72</p></td>
<td><p>48</p></td>
<td><p>1.5MB</p></td>
<td><p>192bit</p></td>
<td><p>GDDR5 8GHz相当</p></td>
<td><p>192GB/s</p></td>
<td><p>3GB</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 1060 (6GB)</p></td>
<td><p>10</p></td>
<td><p>1280</p></td>
<td><p>80</p></td>
<td><p>6GB</p></td>
<td><p>3.9TFLOPS</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 1070</p></td>
<td><p>GP104 (16nm)</p></td>
<td><p>1506MHz [1683MHz]</p></td>
<td><p>15</p></td>
<td><p>1920</p></td>
<td><p>120</p></td>
<td><p>64</p></td>
<td><p>2MB</p></td>
<td><p>256bit</p></td>
<td><p>256GB/s</p></td>
<td><p>8GB</p></td>
<td><p>5.8TFLOPS</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 1070 Ti</p></td>
<td><p>1607MHz [1683MHz]</p></td>
<td><p>19</p></td>
<td><p>2432</p></td>
<td><p>152</p></td>
<td><p>7.8TFLOPS</p></td>
<td><p>180W (8pin)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 1080</p></td>
<td><p>1607MHz [1733MHz]</p></td>
<td><p>20</p></td>
<td><p>2560</p></td>
<td><p>160</p></td>
<td><p>GDDR5X 10GHz相当</p></td>
<td><p>320GB/s</p></td>
<td><p>8.2TFLOPS</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 1080 Ti</p></td>
<td><p>GP102 (16nm)</p></td>
<td><p>1480MHz [1582MHz]</p></td>
<td><p>28</p></td>
<td><p>3584</p></td>
<td><p>224</p></td>
<td><p>88</p></td>
<td><p>2.75MB</p></td>
<td><p>352bit</p></td>
<td><p>GDDR5X 11GHz相当</p></td>
<td><p>484GB/s</p></td>
<td><p>11GB</p></td>
</tr>
<tr class="odd">
<td><p>NVIDIA TITAN X</p></td>
<td><p>1417MHz [1531MHz]</p></td>
<td><p>96</p></td>
<td><p>3MB</p></td>
<td><p>384bit</p></td>
<td><p>GDDR5X 10GHz相当</p></td>
<td><p>480GB/s</p></td>
<td><p>12GB</p></td>
<td><p>10.1TFLOPS</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>NVIDIA TITAN Xp</p></td>
<td><p>1405MHz [1582MHz]</p></td>
<td><p>30</p></td>
<td><p>3840</p></td>
<td><p>240</p></td>
<td><p>GDDR5X 11.4GHz相当</p></td>
<td><p>547GB/s</p></td>
<td><p>10.8TFLOPS</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

[代替文=](https://ja.wikipedia.org/wiki/ファイル:MiddleRange001.png "wikilink") [NVIDIA-GTX-1070-FoundersEdition-FL.jpg](https://ja.wikipedia.org/wiki/File:NVIDIA-GTX-1070-FoundersEdition-FL.jpg "fig:NVIDIA-GTX-1070-FoundersEdition-FL.jpg")

  - GT 1030 \[73\]
    2017年5月17日発表。PascalアーキテクチャのGP108コアを採用するロークラスモデル。14 nmプロセス採用。GP108コアはGP107コアの半分となる1基のGPC(3基のSM)で構成されていて、コア数、メモリバス幅とメモリ容量はGTX 1050 Tiの半分となる。Kepler世代のGT 730の後継となる製品であるが、GTX 750に近い性能がある\[74\]。PCIe 3.0×4接続でロープロファイルかつ1スロット。
  - GT 1030 (DDR4版)
    2018年3月12日にリリース（NVIDIAからの正式発表は無し）。GDDR5の価格高騰を受けて、VRAMをSDDR4に置き換えた。TDPは20 Wに低減しているが、性能はGDDR5版の60%弱にまで低下し、GT 730 (GDDR5版)を下回る。
  - GTX 1050 (2 GB)、 1050 Ti \[75\]
    2016年10月18日発表。GP107コアを採用するエントリーミドルレンジモデル。14 nmプロセス採用で補助電源が不要。同年12月にはロープロファイル対応の製品も発売された。
    GTX 1050 Tiは2基のGPC×3で計6基のSMで構成され、前世代のGTX 950とコア数は同じだが、コアクロックとメモリクロックが上がって、性能はGTX 960と同程度となった。
    GTX 1050(2 GB)はそこからSM 1基が無効化、前々世代のGTX 750 Tiとコア数は同じとなり、性能はGTX 950から数％の上昇に収まった。
    NVIDIAはGTX 1050(2 GB)の性能を、GeForce GTX 650の約3倍、GTX 750 Tiの約1.5倍としている\[76\]。
  - GTX 1050 (3 GB) \[77\]
    GTX 1050 Tiの1 GBのGDDR5チップの数を4個から3個に減らしたもの。メモリバス幅は4分の3となる96bitへ減少したが、GPUクロックが引き上げられている。性能はGTX 1050(2 GB)とGTX 1050 Tiの中間となる。
  - GTX 1060 (3 GB) \[78\]
    2016年8月18日発表。GTX 1060 (6 GB)からSM 1基が無効化されている。性能はGTX 970と同程度で、Kepler世代のGTX TITANを超える。
  - GTX 1060 (6 GB) \[79\]
    2016年7月7日発表。フルスペックのGP106コアを採用するミドルレンジモデル。2基のGPC×5で計10基のSMで構成されている。性能はGTX 980と同程度で、Kepler世代のGTX TITAN Blackを超える。
  - GTX 1070 \[80\]
    2016年5月6日発表。ハイエンドモデルのGTX 1080で採用されているGP104コアから、GPC 4基中の1基が無効化され、3基のGPC×5で計15基のSMで構成されている。メモリは従来のGDDR5となっている。性能は前世代ハイエンドモデルのGTX 980 Tiと同程度。
  - GTX 1070 Ti \[81\]
    2017年10月26日発表。ハイエンドモデルのGTX 1080と同じGP104コアを採用しているが、SM 20基中の1基が無効化され、メモリは従来のGDDR5となっている。
  - GTX 1080 \[82\]
    2016年5月6日発表。先に「DRIVE PX 2」や「Tesla P100 (GP100)」として投入されていたPascalアーキテクチャを採用する初のコンシューマ向けモデル。フルスペックのGP104コアを採用し、4基のGPC×5で計20基のSMで構成されている。新たなメモリ規格のGDDR5Xメモリの採用により、プリフェッチを底上げすることで、メモリ帯域が向上している。
  - GTX 1080 Ti \[83\] \[84\]
    2017年2月28日発表。NVIDIA TITANシリーズと同じGP102コアを採用しているが、SM 30基中の2基とROPユニット96基中の8基が無効化され、メモリバス幅が32bit減少、メモリ容量も1 GB減少、L2キャッシュ容量も0.25 MB減少している。メモリ帯域については、GDDR5XメモリのデータレートがGTX 1080/NVIDIA TITAN Xの10Gbpsから11Gbpsに引き上げられたことで、NVIDIA TITAN Xより広くなっている。
  - NVIDIA TITAN X \[85\]
    2016年7月22日発表、同年8月2日発売。GP102コアを採用しているが、SM 30基中の2基が無効化されている。
  - NVIDIA TITAN Xp \[86\]
    2017年4月7日発表。フルスペックのGP102コアを採用し、6基のGPC×5で計30基のSMで構成されている。

#### GeForce 16 Series/GeForce 20 Series

##### GeForce GTX 16 Series

GeForce GTX 16シリーズは、Turingアーキテクチャを採用する、ミドルレンジの2019年前半 - の製品群である。

32bit版OSではドライバーがサポートされない。\[87\]

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック [GPU Boost]</p></th>
<th><p>コア数</p></th>
<th><p>メモリ</p></th>
<th><p>FLOPS</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/SLI" title="wikilink">SLI</a></p></th>
<th><p>VR</p></th>
<th><p>最大消費電力 (補助電源)</p></th>
<th><p>接続</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/DirectX" title="wikilink">DirectX</a><br />
<small>(Feature Level)</small></p></th>
<th><p><a href="../Page/OpenGL.md" title="wikilink">OpenGL</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SM</p></td>
<td><p><a href="../Page/CUDA.md" title="wikilink">CUDA</a></p></td>
<td><p>Tensor</p></td>
<td><p>RT</p></td>
<td><p>TeX</p></td>
<td><p>ROP</p></td>
<td><p>L2</p></td>
<td><p>バス幅</p></td>
<td><p>動作クロック</p></td>
<td><p>帯域</p></td>
<td><p>容量</p></td>
<td><p>単精度 (理論値)</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 1650 (GDDR5)</p></td>
<td><p>TU117 (12nm)</p></td>
<td><p>1485MHz [1665MHz]</p></td>
<td><p>14</p></td>
<td><p>896</p></td>
<td><p>rowspan="7" </p></td>
<td><p>rowspan="7" </p></td>
<td><p>56</p></td>
<td><p>32</p></td>
<td><p>1MB</p></td>
<td><p>128bit</p></td>
<td><p>GDDR5 8GHz相当</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 1650 (GDDR6)</p></td>
<td><p>GDDR6 12GHz相当</p></td>
<td><p>192GB/s</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 1650 (TU106)</p></td>
<td><p>TU106 (12nm)</p></td>
<td><p>[1605MHz]</p></td>
<td><p>90W (6pin)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 1650 SUPER</p></td>
<td><p>TU116 (12nm)</p></td>
<td><p>1530MHz [1725MHz]</p></td>
<td><p>20</p></td>
<td><p>1280</p></td>
<td><p>80</p></td>
<td><p>3.9TFLOPS</p></td>
<td><p>100W (6pin)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 1660</p></td>
<td><p>1530MHz [1785MHz]</p></td>
<td><p>22</p></td>
<td><p>1408</p></td>
<td><p>88</p></td>
<td><p>48</p></td>
<td><p>1.5MB</p></td>
<td><p>192bit</p></td>
<td><p>GDDR5 8GHz相当</p></td>
<td><p>192GB/s</p></td>
<td><p>6GB</p></td>
<td><p>4.3TFLOPS</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 1660 SUPER</p></td>
<td><p>GDDR6 14GHz相当</p></td>
<td><p>336GB/s</p></td>
<td><p>125W (8pin)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 1660 Ti</p></td>
<td><p>1500MHz [1770MHz]</p></td>
<td><p>24</p></td>
<td><p>1536</p></td>
<td><p>96</p></td>
<td><p>GDDR6 12GHz相当</p></td>
<td><p>288GB/s</p></td>
<td><p>4.6TFLOPS</p></td>
<td><p>120W (8pin)</p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

  - GTX 1650 \[88\] \[89\] \[90\]
    2019年4月23日発売。フルスペックのTU117コアからSM 16基中の2基が無効化されている。前世代のGTX 1050 Tiの後継に位置する。米国での小売価格は、GTX 1050 Tiの139ドルより僅かに高い149ドルとなった。
  - GTX 1650 (TU106) \[91\]
    2020年7月発売。GeForce RTX 2070用のTU106コアの一部を無効化したもの。NVENCの世代が他の1650のVolta世代より新しいTuring世代になっている。補助電源を必要とする。中国市場では GeForce GTX 1650 Ultra と称して販売されている\[92\]。
  - GTX 1650 SUPER \[93\]
    2019年11月22日発売。GTX1650の上位版。GTX1650とは違い、TU116コアを採用している。CUDAコア数を1280コアに増やし、クロックも1530 MHz(ブースト時1725 MHz)に上がっている。メモリがGDDR6の12 GHz相当になり、帯域も192 GB/sに拡張されている。ただ、その分消費電力が100 Wに増え、補助電源も6pinが一本必要になっている。VRAMが4 GBなので、重量級ゲームは厳しい。
  - GTX 1660 \[94\]
    2019年3月14日発売。フルスペックのTU116コアからSM 24基中の2基が無効化されている。従来のメモリ規格のGDDR5メモリに据え置かれ、価格が抑えられた。前世代のGTX 1060(6 GB)の後継に位置し、消費電力は前世代のGTX 1060と同等だが、補助電源の供給方法は8ピン×1に変更された。米国での小売価格は、GTX 1060(3 GB)の199ドルとGTX 1060(6 GB)の249ドルの中間の219ドルとなった。
  - GTX 1660 SUPER \[95\]
    2019年10月29日発売。メモリがGDDR6の14 GHz相当になり、帯域も336 GB/sに拡張されている。ただ、従来のSUPERシリーズとは違い、コアクロックもコア数も変わらない。ただメモリ関連が強化されているだけだが、NVIDIA公式によると、無印より1.2倍性能がアップしているらしい。\[96\]
  - GTX 1660 Ti \[97\]
    2019年2月22日発売。フルスペックのTU116コアを採用し、3基のGPC×12で計24基のSMで構成されている。消費電力は前世代のGTX 1060と同等だが、補助電源の供給方法は8ピン×1に変更された。性能は前世代のGTX 1070を僅かに下回る。米国での小売価格は、GTX 1070の379ドルより100ドル安い279ドルとなった。

##### GeForce RTX 20 Series

GeForce RTX 20シリーズは、Turingアーキテクチャを採用する、ハイクラスからウルトラハイエンドクラスの2018年後半 - の製品群である。

新しいSUPERグレードは、“無印”と，その上位モデルを示す“Ti”の間に位置する\[98\]\[99\]。

SM内部にTensorコアとRay Tracingコア (RTコア) と呼ばれる新しい演算器が追加されており、[ディープラーニング](https://ja.wikipedia.org/wiki/ディープラーニング "wikilink")の高速化およびリアルタイム[レイトレーシング](../Page/レイトレーシング.md "wikilink")のハードウェアアクセラレーションを実現している\[100\]。また、新たなメモリ規格のGDDR6メモリの採用により、メモリ帯域が向上している\[101\]。

32bit版OSではドライバーがサポートされない\[102\]。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名<br />
(プロセス)</p></th>
<th><p>コアクロック<br />
[GPU Boost]</p></th>
<th><p>コア数</p></th>
<th><p>メモリ</p></th>
<th><p><a href="../Page/FLOPS.md" title="wikilink">FLOPS</a></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/SLI" title="wikilink">SLI</a></p></th>
<th><p>VR</p></th>
<th><p>最大消費電力<br />
(補助電源)</p></th>
<th><p>接続</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/DirectX" title="wikilink">DirectX</a><br />
<small>(Feature Level)</small></p></th>
<th><p><a href="../Page/OpenGL.md" title="wikilink">OpenGL</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SM</p></td>
<td><p><a href="../Page/CUDA.md" title="wikilink">CUDA</a></p></td>
<td><p>Tensor</p></td>
<td><p>RT</p></td>
<td><p>TeX</p></td>
<td><p>ROP</p></td>
<td><p>L2</p></td>
<td><p>バス幅</p></td>
<td><p>動作クロック</p></td>
<td><p>帯域</p></td>
<td><p>容量</p></td>
<td><p>単精度<br />
(理論値)</p></td>
</tr>
<tr class="even">
<td><p>GeForce RTX 2060</p></td>
<td><p>TU106 (12nm)</p></td>
<td><p>1365MHz [1680MHz]</p></td>
<td><p>30</p></td>
<td><p>1920</p></td>
<td><p>240</p></td>
<td><p>30</p></td>
<td><p>120</p></td>
<td><p>48</p></td>
<td><p>3MB</p></td>
<td><p>192bit</p></td>
<td><p>GDDR6 14GHz相当</p></td>
</tr>
<tr class="odd">
<td><p>GeForce RTX 2060 SUPER</p></td>
<td><p>1470MHz [1620MHz]</p></td>
<td><p>34</p></td>
<td><p>2176</p></td>
<td><p>272</p></td>
<td><p>34</p></td>
<td><p>136</p></td>
<td><p>64</p></td>
<td><p>4MB</p></td>
<td><p>256bit</p></td>
<td><p>448GB/s</p></td>
<td><p>8GB</p></td>
</tr>
<tr class="even">
<td><p>GeForce RTX 2070</p></td>
<td><p>1410MHz [1620MHz]</p></td>
<td><p>36</p></td>
<td><p>2304</p></td>
<td><p>288</p></td>
<td><p>36</p></td>
<td><p>144</p></td>
<td><p>6.8TFLOPS</p></td>
<td><p>52 Tensor TFLOPS</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce RTX 2070 SUPER</p></td>
<td><p>TU104 (12nm)</p></td>
<td><p>1605MHz [1770MHz]</p></td>
<td><p>40</p></td>
<td><p>2560</p></td>
<td><p>320</p></td>
<td><p>40</p></td>
<td><p>160</p></td>
<td><p>8.2TFLOPS</p></td>
<td><p>65.7 Tensor TFLOPS</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/NVLink" title="wikilink">NVLink</a><br />
2-way</p></td>
<td><p>215W (6pin+8pin)</p></td>
</tr>
<tr class="even">
<td><p>GeForce RTX 2080</p></td>
<td><p>1515MHz [1710MHz]</p></td>
<td><p>46</p></td>
<td><p>2944</p></td>
<td><p>368</p></td>
<td><p>46</p></td>
<td><p>184</p></td>
<td><p>8.9TFLOPS</p></td>
<td><p>71.4 Tensor TFLOPS</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce RTX 2080 SUPER</p></td>
<td><p>1650MHz [1815MHz]</p></td>
<td><p>48</p></td>
<td><p>3072</p></td>
<td><p>384</p></td>
<td><p>48</p></td>
<td><p>192</p></td>
<td><p>GDDR6 15.5GHz相当</p></td>
<td><p>496GB/s</p></td>
<td><p>10.1TFLOPS</p></td>
<td><p>81.1 Tensor TFLOPS</p></td>
<td><p>250W (6pin+8pin)</p></td>
</tr>
<tr class="even">
<td><p>GeForce RTX 2080 Ti</p></td>
<td><p>TU102 (12nm)</p></td>
<td><p>1350MHz [1545MHz]</p></td>
<td><p>68</p></td>
<td><p>4352</p></td>
<td><p>544</p></td>
<td><p>68</p></td>
<td><p>272</p></td>
<td><p>88</p></td>
<td><p>6MB</p></td>
<td><p>352bit</p></td>
<td><p>GDDR6 14GHz相当</p></td>
</tr>
<tr class="odd">
<td><p>NVIDIA TITAN RTX</p></td>
<td><p>1350MHz [1770MHz]</p></td>
<td><p>72</p></td>
<td><p>4608</p></td>
<td><p>576</p></td>
<td><p>72</p></td>
<td><p>288</p></td>
<td><p>96</p></td>
<td><p>384bit</p></td>
<td><p>672GB/s</p></td>
<td><p>24GB</p></td>
<td><p>12.4TFLOPS</p></td>
</tr>
</tbody>
</table>

  - RTX 2060 \[103\]
    2019年1月7日発表、同年1月15日発売。フルスペックのTU106コアからSM 36基中の6基が無効化され、メモリバス幅も4分の3となる192bitへ抑えたもの。前世代のGTX 1070 Tiと同等性能\[104\]でありながら、米国での小売価格は、GTX 1070 Tiの449ドルより100ドル安い349ドルとなった。
  - RTX 2060 SUPER \[105\]
    2019年7月2日発表、同年7月9日発売。RTX 2070(無印)に近い性能まで引き上げられたが、米国での小売価格は、399ドルに抑えられた。
  - RTX 2070 \[106\]
    2018年8月20日発表、同年10月17日発売。フルスペックのTU106コアを採用し、3基のGPC×12で計36基のSMで構成されている。前世代のGTX 1080と同等性能。米国での小売価格は、GTX 1080と同じ499ドルとなった。上位のRTX 2070 SUPERの発売後は、実売価格が下落した。
  - RTX 2070 SUPER \[107\]
    2019年7月2日発表、同年7月9日発売。上位のとRTX 2080(無印)と同じTU104コアを採用し、RTX 2070(無印)とRTX 2080(無印)のほぼ中間の性能まで引き上げられたが、米国での小売価格は、RTX 2070(無印)と同じ499ドルに据え置かれた。
  - RTX 2080 \[108\]
    2018年8月20日発表、同年9月20日発売。フルスペックのTU104コアである6基のGPC×8で計48基のSMから、GPC 2基が無効化されている。前世代のGTX 1080 Tiと同等性能。米国での小売価格は、GTX 1080 Tiと同じ699ドルとなった。上位のRTX 2080 SUPERの発売後は、実売価格が下落した。
  - RTX 2080 SUPER \[109\]
    2019年7月2日発表、同年7月23日発売。フルスペックのTU104コアを採用し、GDDR6メモリのデータレートが14 Gbpsから15.5 Gbpsに引き上げられたが、米国での小売価格は、RTX 2080(無印)と同じ699ドルに据え置かれた。
  - RTX 2080 Ti \[110\]
    2018年8月20日発表、同年9月27日発売。フルスペックのTU102コアからSM 72基中の4基が無効化され、メモリバス幅が32bit減少している。米国での小売価格は999ドルで、日本国内での小売価格は15万円前後から。

##### NVIDIA TITAN RTX Series

NVIDIA TITAN RTXシリーズは、Turingアーキテクチャを採用する、2018年後半 - のフラグシップ製品である。製品世代としては、GeForce RTX 20シリーズと同列である。

  - NVIDIA TITAN RTX \[111\]
    2018年12月3日発表、同年12月19日発売。フルスペックのTU102コアを採用し、6基のGPC×12で計72基のSMで構成されている。

#### GeForce RTX 30 Series

GeForce RTX 30シリーズは、Ampereアーキテクチャを採用する、ハイクラスからウルトラハイエンドクラスの2020年後半 - の製品群である\[112\]\[113\]\[114\]。

上位製品では、SDRAMとして初となる4レベルパルス振幅変調(PAM4)を使用するGDDR6X規格の採用により、メモリ帯域が向上している\[115\]\[116\]。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名<br />
(プロセス)</p></th>
<th><p>コアクロック<br />
[GPU boost]</p></th>
<th><p>コア数</p></th>
<th><p>メモリ</p></th>
<th><p><a href="../Page/FLOPS.md" title="wikilink">FLOPS</a></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/SLI" title="wikilink">SLI</a></p></th>
<th><p><a href="../Page/バーチャル・リアリティ.md" title="wikilink">VR</a></p></th>
<th><p>消費電力<br />
(補助電源)</p></th>
<th><p>接続</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Microsoft_DirectX" title="wikilink">DirectX</a><br />
<small>(Feature Level)</small></p></th>
<th><p><a href="../Page/OpenGL.md" title="wikilink">OpenGL</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SM</p></td>
<td><p><a href="../Page/CUDA.md" title="wikilink">CUDA</a></p></td>
<td><p>Tensor</p></td>
<td><p>RT</p></td>
<td><p>TeX</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/:en:Render_output_unit" title="wikilink">ROP</a></p></td>
<td><p>L1 [L2]</p></td>
<td><p>動作クロック</p></td>
<td><p>バス幅</p></td>
<td><p>帯域</p></td>
<td><p>容量</p></td>
<td><p>単精度<br />
(理論値)</p></td>
</tr>
<tr class="even">
<td><p>GeForce RTX 3070</p></td>
<td><p>GA104 (8 nm)</p></td>
<td><p>1500 MHz [1725 MHz]</p></td>
<td><p>46</p></td>
<td><p>5888</p></td>
<td><p>184</p></td>
<td><p>46</p></td>
<td><p>184</p></td>
<td><p>64</p></td>
<td><p>128 KB/SM [4 MB]</p></td>
<td><p>GDDR6 14 GHz相当</p></td>
<td><p>256bit</p></td>
</tr>
<tr class="odd">
<td><p>GeForce RTX 3080</p></td>
<td><p>GA102 (8 nm)</p></td>
<td><p>1440 MHz [1710 MHz]</p></td>
<td><p>68</p></td>
<td><p>8704</p></td>
<td><p>272</p></td>
<td><p>68</p></td>
<td><p>272</p></td>
<td><p>96</p></td>
<td><p>128 KB/SM [5 MB]</p></td>
<td><p>GDDR6X 19 GHz相当</p></td>
<td><p>320bit</p></td>
</tr>
<tr class="even">
<td><p>GeForce RTX 3090</p></td>
<td><p>1395 MHz [1695 MHz]</p></td>
<td><p>82</p></td>
<td><p>10496</p></td>
<td><p>328</p></td>
<td><p>82</p></td>
<td><p>328</p></td>
<td><p>112</p></td>
<td><p>128 KB/SM [6 MB]</p></td>
<td><p>GDDR6X 19.5 GHz相当</p></td>
<td><p>384bit</p></td>
<td><p>936 GB/s</p></td>
</tr>
</tbody>
</table>

  - RTX 3070
    2020年9月1日発表、同年10月15日発売。価格は$499(¥79,980)から

<!-- end list -->

  - RTX 3080
    2020年9月1日発表、同年9月17日発売。価格は$699(¥109,800)から

<!-- end list -->

  - RTX 3090
    2020年9月1日発表、同年9月24日発売。価格は$1,499(¥229,800)から

### ノートPC向け

#### GeForce 2 Go Series

**GeForce 2 Go Series**（ジーフォース・ツー・ゴー・シリーズ）は、GeForceシリーズの初代ノートPC向け製品群である。

| 製品名              | コア名 (プロセス)   | コアクロック | メモリクロック （バス幅）   | メモリ容量 | PP数 | VS数 | SLI | 消費電力 | DirectX |
| ---------------- | ------------ | ------ | --------------- | ----- | --- | --- | --- | ---- | ------- |
| GeForce 2 Go     | NV11 (180nm) | 166MHz | 143MHz (128bit) | 64MB  | 1   | 0   | ×   | 2W   | 7       |
| GeForce 2 Go 200 | NV11 (180nm) | 166MHz | 286MHz (64bit)  | 32MB  | 1   | 0   | ×   | 2W   |         |
| GeForce 2 Go 100 | NV11 (180nm) | 166MHz | 286MHz (32bit)  | 16MB  | 1   | 0   | ×   | 2W   |         |

#### GeForce 3 Go Series

**GeForce 3 Go Series**（ジーフォース・スリー・ゴー・シリーズ）は、GeForceシリーズの第2世代ノートPC向け製品群である。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>メモリ容量</p></th>
<th><p>PP数</p></th>
<th><p>VS数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce 3 Go</p></td>
<td><p>NV11 (180nm)</p></td>
<td><p>250MHz</p></td>
<td><p>MHz (128bit)</p></td>
<td><p>64MB</p></td>
<td><p>1</p></td>
<td><p>0</p></td>
<td><p>×</p></td>
<td><p>2W</p></td>
<td><p>7</p></td>
</tr>
</tbody>
</table>

#### GeForce 4 Go Series

**GeForce 4 Go Series**（ジーフォース・フォー・ゴー・シリーズ）は、GeForceシリーズの第3世代ノートPC向け製品群である。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>メモリ容量</p></th>
<th><p>PP数</p></th>
<th><p>VS数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce 4 488 Go</p></td>
<td><p>NV18 (150nm)</p></td>
<td><p>300MHz</p></td>
<td><p>550MHz (128bit)</p></td>
<td><p>64MB</p></td>
<td><p>2</p></td>
<td><p>0</p></td>
<td><p>×</p></td>
<td><p>W</p></td>
<td><p>8.0</p></td>
</tr>
<tr class="even">
<td><p>GeForce 4 460 Go</p></td>
<td><p>NV17 (150nm)</p></td>
<td><p>250MHz</p></td>
<td><p>500MHz (128bit)</p></td>
<td><p>64MB</p></td>
<td><p>2</p></td>
<td><p>0</p></td>
<td><p>×</p></td>
<td><p>W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 4 440 Go</p></td>
<td><p>NV17 (150nm)</p></td>
<td><p>220MHz</p></td>
<td><p>440MHz (128bit)</p></td>
<td><p>64MB</p></td>
<td><p>2</p></td>
<td><p>0</p></td>
<td><p>×</p></td>
<td><p>W</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 4 420 Go</p></td>
<td><p>NV17 (150nm)</p></td>
<td><p>200MHz</p></td>
<td><p>400MHz (64bit)</p></td>
<td><p>32MB</p></td>
<td><p>2</p></td>
<td><p>0</p></td>
<td><p>×</p></td>
<td><p>W</p></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce FX Go Series

**GeForce FX Go Series**（ジーフォース・エフエックス・ゴー・シリーズ）は、GeForceシリーズの第4世代PCノート向け製品群である。DirectX 9に対応。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック（シェーダークロック）</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>メモリ容量</p></th>
<th><p>PP数</p></th>
<th><p>VS数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce FX Go 5700</p></td>
<td><p>NV36M (130nm)</p></td>
<td><p>450MHz</p></td>
<td><p>550MHz (128bit)</p></td>
<td><p>64MB</p></td>
<td><p>4</p></td>
<td><p>1</p></td>
<td><p>×</p></td>
<td><p>W</p></td>
<td><p>9.0a</p></td>
</tr>
<tr class="even">
<td><p>GeForce FX Go 5600 / 5650</p></td>
<td><p>NV31M (150nm / 130nm)</p></td>
<td><p>350MHz</p></td>
<td><p>600MHz (128bit)</p></td>
<td><p>64MB</p></td>
<td><p>4</p></td>
<td><p>1</p></td>
<td><p>×</p></td>
<td><p>18W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce FX Go 5200</p></td>
<td><p>NV31M (150nm)</p></td>
<td><p>300MHz (300MHz)</p></td>
<td><p>600MHz (128bit)</p></td>
<td><p>32MB</p></td>
<td><p>4</p></td>
<td><p>1</p></td>
<td><p>×</p></td>
<td><p>9W</p></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce Go 6 Series

**GeForce Go 6 Series**（ジーフォース・ゴー・シックス・シリーズ）は、GeForceシリーズの第5世代ノートPC向け製品群である。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック（シェーダークロック）</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>メモリ容量</p></th>
<th><p>PP数</p></th>
<th><p>VS数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce Go 6800 Ultra</p></td>
<td><p>NV41M (110nm)</p></td>
<td><p>450MHz (450MHz)</p></td>
<td><p>1200MHz (256bit)</p></td>
<td><p>256MB</p></td>
<td><p>12</p></td>
<td><p>5</p></td>
<td><p>○</p></td>
<td><p>66W</p></td>
<td><p>9.0c</p></td>
</tr>
<tr class="even">
<td><p>GeForce Go 6800</p></td>
<td><p>NV42M (110nm)</p></td>
<td><p>300MHz (300MHz)</p></td>
<td><p>600MHz (256bit)</p></td>
<td><p>256MB</p></td>
<td><p>12</p></td>
<td><p>5</p></td>
<td><p>○</p></td>
<td><p>27W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce Go 6600</p></td>
<td><p>NV44MV (110nm)</p></td>
<td><p>350MHz (350MHz)</p></td>
<td><p>600MHz (128bit)</p></td>
<td><p>256MB</p></td>
<td><p>8</p></td>
<td><p>4</p></td>
<td><p>○</p></td>
<td><p>18W</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce Go 6400</p></td>
<td><p>NV44M1 (110nm)</p></td>
<td><p>400MHz (400MHz)</p></td>
<td><p>700MHz (64bit)</p></td>
<td><p>32MB</p></td>
<td><p>4</p></td>
<td><p>3</p></td>
<td><p>○</p></td>
<td><p>W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce Go 6250</p></td>
<td><p>NV44MV (110nm)</p></td>
<td><p>400MHz (400MHz)</p></td>
<td><p>700MHz (64bit)</p></td>
<td><p>32MB</p></td>
<td><p>4</p></td>
<td><p>3</p></td>
<td><p>○</p></td>
<td><p>10W</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce Go 6200</p></td>
<td><p>NV44MV (110nm)</p></td>
<td><p>300MHz (300MHz)</p></td>
<td><p>600MHz (64bit)</p></td>
<td><p>32MB</p></td>
<td><p>4</p></td>
<td><p>3</p></td>
<td><p>○</p></td>
<td><p>9W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce Go 6150</p></td>
<td><p>C51MV (110nm)</p></td>
<td><p>350MHz (350MHz)</p></td>
<td></td>
<td><p>0MB(TC)</p></td>
<td><p>2</p></td>
<td><p>1</p></td>
<td><p>○</p></td>
<td><p>W</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce Go 6100</p></td>
<td><p>C51MV (110nm)</p></td>
<td><p>425MHz (425MHz)</p></td>
<td></td>
<td><p>0MB(TC)</p></td>
<td><p>2</p></td>
<td><p>1</p></td>
<td><p>○</p></td>
<td><p>W</p></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce Go 7 Series

**GeForce Go 7 Series**（ジーフォース・ゴー・セブン・シリーズ）は、GeForceシリーズの第6世代ノートPC向け製品群である。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック（シェーダークロック）</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>メモリ容量</p></th>
<th><p>PP数</p></th>
<th><p>VS数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce Go 7950 GTX</p></td>
<td><p>G71M (90nm)</p></td>
<td><p>575MHz (575MHz)</p></td>
<td><p>1400MHz (256bit)</p></td>
<td><p>512MB</p></td>
<td><p>24</p></td>
<td><p>8</p></td>
<td><p>○</p></td>
<td><p>45W</p></td>
<td><p>9.0c</p></td>
</tr>
<tr class="even">
<td><p>GeForce Go 7900 GTX</p></td>
<td><p>G71M (90nm)</p></td>
<td><p>500MHz (500MHz)</p></td>
<td><p>1200MHz (256bit)</p></td>
<td><p>512MB</p></td>
<td><p>24</p></td>
<td><p>8</p></td>
<td><p>○</p></td>
<td><p>45W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce Go 7900 GS</p></td>
<td><p>G71M (90nm)</p></td>
<td><p>375MHz (375MHz)</p></td>
<td><p>1000MHz (256bit)</p></td>
<td><p>512MB</p></td>
<td><p>20</p></td>
<td><p>7</p></td>
<td><p>○</p></td>
<td><p>20W</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce Go 7800 GTX</p></td>
<td><p>G70M (110nm)</p></td>
<td><p>440MHz (440MHz)</p></td>
<td><p>1100MHz (256bit)</p></td>
<td><p>512MB</p></td>
<td><p>24</p></td>
<td><p>8</p></td>
<td><p>○</p></td>
<td><p>65W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce Go 7800</p></td>
<td><p>G70M (110nm)</p></td>
<td><p>400MHz (400MHz)</p></td>
<td><p>1100MHz (128bit)</p></td>
<td><p>256MB</p></td>
<td><p>16</p></td>
<td><p>6</p></td>
<td><p>○</p></td>
<td><p>W</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce Go 7700</p></td>
<td><p>G73M-B1 (80nm)</p></td>
<td><p>450MHz (450MHz)</p></td>
<td><p>1000MHz (128bit)</p></td>
<td><p>512MB</p></td>
<td><p>12</p></td>
<td><p>5</p></td>
<td><p>○</p></td>
<td><p>W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce Go 7600 GT</p></td>
<td><p>G73M (90nm)</p></td>
<td><p>500MHz (500MHz)</p></td>
<td><p>1200MHz (128bit)</p></td>
<td><p>256MB</p></td>
<td><p>12</p></td>
<td><p>5</p></td>
<td><p>○</p></td>
<td><p>W</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce Go 7600</p></td>
<td><p>G73M (90nm)</p></td>
<td><p>450MHz (450MHz)</p></td>
<td><p>700MHz (128bit)</p></td>
<td><p>256MB</p></td>
<td><p>8</p></td>
<td><p>5</p></td>
<td><p>○</p></td>
<td><p>W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce Go 7400</p></td>
<td><p>G72M (90nm)</p></td>
<td><p>450MHz (450MHz)</p></td>
<td><p>900MHz (64bit)</p></td>
<td><p>64MB</p></td>
<td><p>4</p></td>
<td><p>3</p></td>
<td><p>○</p></td>
<td><p>W</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce Go 7300</p></td>
<td><p>G72M (90nm)</p></td>
<td><p>350MHz (350MHz)</p></td>
<td><p>700MHz (64bit)</p></td>
<td><p>64MB</p></td>
<td><p>4</p></td>
<td><p>3</p></td>
<td><p>○</p></td>
<td><p>W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce Go 7200</p></td>
<td><p>G72M (90nm)</p></td>
<td><p>450MHz (450MHz)</p></td>
<td><p>700MHz (32bit) / (</p></td>
<td><p>64MB / 0MB(TC)</p></td>
<td><p>4</p></td>
<td><p>3</p></td>
<td><p>○</p></td>
<td><p>W</p></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce 8 M Series

**GeForce 8 M Series**（ジーフォース・エイト・エム・シリーズ）は、GeForceシリーズの第7世代ノートPC向け製品群である。名称がそれまでの*GeForce Go*から*GeForce M*に変更された。DirectX 10に対応。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック (SPクロック)</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>SP数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX</p></th>
<th><p>CUDA</p></th>
<th><p>PhysX</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce 8800M GTX</p></td>
<td><p>G92M (65nm)</p></td>
<td><p>500MHz (1250MHz)</p></td>
<td><p>1600MHz (256bit)</p></td>
<td><p>96</p></td>
<td><p>○</p></td>
<td><p>65W</p></td>
<td><p>10.0</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 8800M GTS</p></td>
<td><p>G92M (65nm)</p></td>
<td><p>500MHz (1250MHz)</p></td>
<td><p>1600MHz (256bit)</p></td>
<td><p>64</p></td>
<td><p>○</p></td>
<td><p>50W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 8700M GT</p></td>
<td><p>G84M (80nm)</p></td>
<td><p>625MHz (1250MHz)</p></td>
<td><p>1600MHz (128bit)</p></td>
<td><p>32</p></td>
<td><p>○</p></td>
<td><p>29W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 8600M GT</p></td>
<td><p>G84M (80nm)</p></td>
<td><p>450MHz (900MHz)</p></td>
<td><p>1200MHz (128bit)</p></td>
<td><p>32</p></td>
<td><p>○</p></td>
<td><p>22W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 8600M GS</p></td>
<td><p>G84M (80nm)</p></td>
<td><p>600MHz (1200MHz)</p></td>
<td><p>1400MHz (128bit)</p></td>
<td><p>16</p></td>
<td><p>○</p></td>
<td><p>20W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 8400M GT</p></td>
<td><p>G86M (80nm)</p></td>
<td><p>450MHz (900MHz)</p></td>
<td><p>1200MHz (128bit)</p></td>
<td><p>16</p></td>
<td><p>×</p></td>
<td><p>14W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 8400M GS</p></td>
<td><p>G86M (80nm)</p></td>
<td><p>400MHz (800MHz)</p></td>
<td><p>1200MHz (64bit)</p></td>
<td><p>16</p></td>
<td><p>×</p></td>
<td><p>11W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 8400M G</p></td>
<td><p>G86M (80nm)</p></td>
<td><p>400MHz (800MHz)</p></td>
<td><p>1200MHz (64bit)</p></td>
<td><p>8</p></td>
<td><p>×</p></td>
<td><p>10W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 8200M G</p></td>
<td><p>MCP77MV MCP79MVL (80nm)</p></td>
<td><p>400MHz (800MHz)</p></td>
<td></td>
<td><p>8</p></td>
<td><p>×</p></td>
<td><p>W</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce 9 M Series

**GeForce 9 M Series**（ジーフォース・ナイン・エム・シリーズ）は、GeForceシリーズの第8世代ノートPC向け製品群である。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック (SPクロック)</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>SP数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce 9800M GTX</p></td>
<td><p>G92M, NB9E-GTX (65nm)</p></td>
<td><p>500MHz (1250MHz)</p></td>
<td><p>1600MHz (256bit)</p></td>
<td><p>112</p></td>
<td><p>○</p></td>
<td><p>75W</p></td>
<td><p>10.0</p></td>
</tr>
<tr class="even">
<td><p>GeForce 9800M GTS</p></td>
<td><p>G94M, NB9E-GT (65nm)</p></td>
<td><p>600MHz (1500MHz)</p></td>
<td><p>1600MHz (256bit)</p></td>
<td><p>64</p></td>
<td><p>○</p></td>
<td><p>75W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 9800M GT</p></td>
<td><p>G92M, NB9E-GT2 (65nm)</p></td>
<td><p>500MHz (1250MHz)</p></td>
<td><p>1600MHz (256bit)</p></td>
<td><p>96</p></td>
<td><p>○</p></td>
<td><p>65W</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 9800M GS</p></td>
<td><p>G94M, NB9E-GS1 (65nm)</p></td>
<td><p>530MHz (1325MHz)</p></td>
<td><p>1600MHz (256bit)</p></td>
<td><p>64</p></td>
<td><p>○</p></td>
<td><p>60W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 9700M GTS</p></td>
<td><p>G94M, NB9E-GS (65nm)</p></td>
<td><p>530MHz (1325MHz)</p></td>
<td><p>1600MHz (256bit)</p></td>
<td><p>48</p></td>
<td><p>○</p></td>
<td><p>60W</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 9700M GT</p></td>
<td><p>G96M, NB9E-GE (65nm)</p></td>
<td><p>625MHz (1550MHz)</p></td>
<td><p>1600MHz (128bit)</p></td>
<td><p>32</p></td>
<td><p>○</p></td>
<td><p>45W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 9650M GT</p></td>
<td><p>G96M, NB9P-GT (55nm)</p></td>
<td><p>550MHz (1325MHz)</p></td>
<td><p>1600MHz (128bit)</p></td>
<td><p>32</p></td>
<td><p>○</p></td>
<td><p>23W</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 9600M GT</p></td>
<td><p>G96M, NB9P-GS (65nm)</p></td>
<td><p>500MHz (1250MHz)</p></td>
<td><p>1600MHz (128bit)</p></td>
<td><p>32</p></td>
<td><p>○</p></td>
<td><p>23W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 9600M GS</p></td>
<td><p>G96M, NB9P-GE2 (65nm)</p></td>
<td><p>430MHz (1075MHz)</p></td>
<td><p>1600MHz (128bit)</p></td>
<td><p>32</p></td>
<td><p>○</p></td>
<td><p>W</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 9500M GS</p></td>
<td><p>G84M, NB9P-GE1 (80nm)</p></td>
<td><p>475MHz (1200MHz)</p></td>
<td><p>1400MHz (128bit)</p></td>
<td><p>32</p></td>
<td><p>○</p></td>
<td><p>W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 9500M G</p></td>
<td><p>G96M, NB9P-GE (65nm)</p></td>
<td><p>500MHz (1250MHz)</p></td>
<td><p>1600MHz (128bit)</p></td>
<td><p>16</p></td>
<td><p>○</p></td>
<td><p>W</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 9400M G</p></td>
<td><p>MCP79MX (65nm)</p></td>
<td><p>450MHz (1100MHz)</p></td>
<td></td>
<td><p>16</p></td>
<td><p>○</p></td>
<td><p>12W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 9300M GS</p></td>
<td><p>G98M, NB9M-GS1 (65nm)</p></td>
<td><p>550MHz (1400MHz)</p></td>
<td><p>1400MHz (64bit)</p></td>
<td><p>8</p></td>
<td><p>○</p></td>
<td><p>13W</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 9300M G</p></td>
<td><p>G86M, NB9M-GS (80nm)</p></td>
<td><p>400MHz (800MHz)</p></td>
<td><p>1200MHz (64bit)</p></td>
<td><p>16</p></td>
<td><p>×</p></td>
<td><p>W</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 9200M GS</p></td>
<td><p>G98M, NB9M-GE (65nm)</p></td>
<td><p>550MHz (1300MHz)</p></td>
<td><p>1400MHz (64bit)</p></td>
<td><p>8</p></td>
<td><p>×</p></td>
<td><p>13W</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 9100M G</p></td>
<td><p>MCP77MH MCP79MH (65nm)</p></td>
<td><p>450MHz (1100MHz)</p></td>
<td></td>
<td><p>8</p></td>
<td><p>×</p></td>
<td><p>W</p></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce 100 M Series

**GeForce 100 M Series**（ジーフォース・100・エム・シリーズ）は、GeForce 100シリーズのノートPC向け製品群である。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック (CUDAコアクロック)</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>CUDAコア数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX<br />
<small>(Feature Level)</small></p></th>
<th><p>PhysX</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce GTS 160M</p></td>
<td><p>G94M, N10E-GS1 (55nm)</p></td>
<td><p>600MHz (1500MHz)</p></td>
<td><p>1600MHz (256bit)</p></td>
<td><p>64</p></td>
<td><p>2-way</p></td>
<td><p>60W</p></td>
<td><p>11.1 API<br />
<small>(FL:10_0)</small></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTS 150M</p></td>
<td><p>G94M, N10E-GE1 (55nm)</p></td>
<td><p>400MHz (1000MHz)</p></td>
<td><p>45W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 130M</p></td>
<td><p>G96M, N10P-GE1 (55nm)</p></td>
<td><p>600MHz (1500MHz)</p></td>
<td><p>1600MHz (128bit)</p></td>
<td><p>32</p></td>
<td><p>23W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce G 110M</p></td>
<td><p>G96M, N10M-GS1 (55nm)</p></td>
<td><p>400MHz (1000MHz)</p></td>
<td><p>1400MHz (64bit)</p></td>
<td><p>16</p></td>
<td><p>×</p></td>
<td><p>14W</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce G 105M</p></td>
<td><p>G96M, N10M-GE1 (55nm)</p></td>
<td><p>640MHz (1600MHz)</p></td>
<td><p>8</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GT218-300-A2 (40nm)</p></td>
<td><p>535MHz (1230MHz)</p></td>
<td><p>1580MHz (64bit)</p></td>
<td><p>16</p></td>
<td><p>11.1 API<br />
<small>(FL:10_1)</small></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce G 102M</p></td>
<td><p>MCP79MX (90nm)</p></td>
<td><p>450MHz (1100MHz)</p></td>
<td></td>
<td><p>11.1 API<br />
<small>(FL:10_0)</small></p></td>
<td><p>×</p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce 200 M Series

**GeForce 200 M Series**（ジーフォース・200・エム・シリーズ）は、GeForce 200シリーズのノートPC向け製品群である。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック (CUDAコアクロック)</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>CUDAコア数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX<br />
<small>(Feature Level)</small></p></th>
<th><p>PhysX</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce GTX 285M</p></td>
<td><p>G92M, N10E-GTX1 (65nm)</p></td>
<td><p>600MHz (1500MHz)</p></td>
<td><p>GDDR3 2000MHz (256bit)</p></td>
<td><p>128</p></td>
<td><p>2-way</p></td>
<td><p>75W</p></td>
<td><p>11.1 API<br />
<small>(FL:10_0)</small></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 280M</p></td>
<td><p>G92M, N10E-GTX (65nm)</p></td>
<td><p>585MHz (1463MHz)</p></td>
<td><p>GDDR3 1900MHz (256bit)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 260M</p></td>
<td><p>G92M, N10E-GT (65nm)</p></td>
<td><p>550MHz (1375MHz)</p></td>
<td><p>112</p></td>
<td><p>65W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTS 260M</p></td>
<td><p>GT215, N10E-GS (40nm)</p></td>
<td><p>GDDR5 3600MHz (128bit)</p></td>
<td><p>96</p></td>
<td><p>38W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTS 250M</p></td>
<td><p>GT215, N10E-GS (40nm)</p></td>
<td><p>500MHz (1250MHz)</p></td>
<td><p>GDDR3 1600MHz (128bit)</p></td>
<td><p>28W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 240M</p></td>
<td><p>GT216, N10P-GS (40nm)</p></td>
<td><p>550MHz (1210MHz)</p></td>
<td><p>48</p></td>
<td><p>×</p></td>
<td><p>23W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 230M</p></td>
<td><p>GT216, N10P-GS (40nm)</p></td>
<td><p>500MHz (1100MHz)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce G 210M</p></td>
<td><p>GT218, N10M-GS (40nm)</p></td>
<td><p>625MHz (1500MHz)</p></td>
<td><p>GDDR3 1600MHz (64bit)</p></td>
<td><p>16</p></td>
<td><p>14W</p></td>
<td><p>×</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce 300 M Series

**GeForce 300 M Series**（ジーフォース・300・エム・シリーズ）は、GeForce 300シリーズのノートPC向け製品群である。DirectX 10.1に対応。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック (CUDAコアクロック)</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>メモリ帯域</p></th>
<th><p>CUDAコア数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>単精度演算能力</p></th>
<th><p>DirectX<br />
<small>(Feature Level)</small></p></th>
<th><p>PhysX</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce GTS 360M</p></td>
<td><p>GT215, N11E-GS1 (40nm)</p></td>
<td><p>550MHz (1436MHz)</p></td>
<td><p>GDDR5 3600MHz (128bit)</p></td>
<td><p>57.6GB/s</p></td>
<td><p>96</p></td>
<td><p>2-way</p></td>
<td><p>38W</p></td>
<td><p>275.7GFlops</p></td>
<td><p>11.1 API<br />
<small>(FL:10_1)</small></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTS 350M</p></td>
<td><p>GT215, N11E-GE1 (40nm)</p></td>
<td><p>500MHz (1250MHz)</p></td>
<td><p>GDDR5 3200MHz (128bit)</p></td>
<td><p>51.2GB/s</p></td>
<td><p>240.0GFlops</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 335M</p></td>
<td><p>GT215, N11P-GS1 (40nm)</p></td>
<td><p>450MHz (1080MHz)</p></td>
<td><p>GDDR3 1600MHz (128bit)</p></td>
<td><p>25.6GB/s</p></td>
<td><p>72</p></td>
<td><p>×</p></td>
<td><p>155.5GFlops</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 330M</p></td>
<td><p>GT216, N11P-GE1-A3 (40nm)</p></td>
<td><p>575MHz (1265MHz)</p></td>
<td><p>48</p></td>
<td><p>23W</p></td>
<td><p>121.4GFlops</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 325M</p></td>
<td><p>GT216, N11P-GV1 (40nm)</p></td>
<td><p>450MHz (990MHz)</p></td>
<td><p>DDR3 1400MHz (128bit)</p></td>
<td><p>22.4GB/s</p></td>
<td><p>95.04GFlops</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 320M</p></td>
<td><p>MCP89 (40nm)</p></td>
<td><p>450MHz (950MHz)</p></td>
<td></td>
<td><p>-</p></td>
<td><p>91.20GFlops</p></td>
<td><p>×</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 310M</p></td>
<td><p>GT218, N11M-GE1 (40nm)</p></td>
<td><p>625MHz (1530MHz)</p></td>
<td><p>GDDR3 1600MHz (64bit)</p></td>
<td><p>12.8GB/s</p></td>
<td><p>16</p></td>
<td><p>14W</p></td>
<td><p>48.96GFlops</p></td>
<td><p>×</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 305M</p></td>
<td><p>GT218, N11M-LP1 (40nm)</p></td>
<td><p>525MHz (1150MHz)</p></td>
<td><p>DDR3 1400MHz (64bit)</p></td>
<td><p>11.2GB/s</p></td>
<td><p>36.80GFlops</p></td>
<td><p>×</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce 400 M Series

**GeForce 400 M Series**（ジーフォース・400・エム・シリーズ）は、GeForce 400シリーズのノートPC向け製品群である。DirectX 12 APIに対応。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>MXM</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック (CUDAコアクロック)</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>メモリ帯域</p></th>
<th><p>CUDAコア数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX<br />
<small>(Feature Level)</small></p></th>
<th><p>OpenGL</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce GTX 485M</p></td>
<td><p>〇</p></td>
<td><p>GF104, N12E-GTX (40nm)</p></td>
<td><p>575MHz (1150MHz)</p></td>
<td><p>GDDR5 3000MHz (256bit)</p></td>
<td><p>96.0GB/s</p></td>
<td><p>384</p></td>
<td><p>2-way</p></td>
<td><p>70W</p></td>
<td><p>12 API<br />
<small>(FL:11_0)</small></p></td>
<td><p>4.6</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 480M</p></td>
<td><p>〇</p></td>
<td><p>GF100, N11E-GTX (40nm)</p></td>
<td><p>425MHz (850MHz)</p></td>
<td><p>GDDR5 2400MHz (256bit)</p></td>
<td><p>76.8GB/s</p></td>
<td><p>352</p></td>
<td><p>100W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 470M</p></td>
<td><p>〇</p></td>
<td><p>GF104, N11E-GT (40nm)</p></td>
<td><p>535MHz (1070MHz)</p></td>
<td><p>GDDR5 3000MHz (192bit)</p></td>
<td><p>72.0GB/s</p></td>
<td><p>288</p></td>
<td><p>75W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 460M</p></td>
<td><p>〇</p></td>
<td><p>GF106, N11E-GS (40nm)</p></td>
<td><p>675MHz (1350MHz)</p></td>
<td><p>GDDR5 2500MHz (192bit)</p></td>
<td><p>60.0GB/s</p></td>
<td><p>192</p></td>
<td><p>50W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 445M</p></td>
<td><p>-</p></td>
<td><p>GF106, N11E-GE (40nm)</p></td>
<td><p>590MHz (1180MHz)</p></td>
<td><p>DDR3 1600MHz (192bit)</p></td>
<td><p>38.4GB/s</p></td>
<td><p>144</p></td>
<td><p>×</p></td>
<td><p>35W</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 435M</p></td>
<td><p>-</p></td>
<td><p>GF106, N11P-GT (40nm)</p></td>
<td><p>650MHz (1300MHz)</p></td>
<td><p>DDR3 1600MHz (128bit)</p></td>
<td><p>25.6GB/s</p></td>
<td><p>96</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 425M</p></td>
<td><p>-</p></td>
<td><p>GF108, N11P-GS (40nm)</p></td>
<td><p>560MHz (1120MHz)</p></td>
<td><p>23W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 420M</p></td>
<td><p>-</p></td>
<td><p>GF108, N11P-GE (40nm)</p></td>
<td><p>500MHz (1000MHz)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 415M</p></td>
<td><p>-</p></td>
<td><p>GF108, N11P-GV (40nm)</p></td>
<td><p>48</p></td>
<td><p>12W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce 500 M Series

**GeForce 500 M Series**（ジーフォース・500・エム・シリーズ）は、GeForce 500シリーズのノートPC向け製品群である。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>MXM</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック (CUDAコアクロック)</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>メモリ帯域</p></th>
<th><p>CUDAコア数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX<br />
<small>(Feature Level)</small></p></th>
<th><p>OpenGL</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce GTX 580M</p></td>
<td><p>〇</p></td>
<td><p>GF114, N12E-GTX2 (40nm)</p></td>
<td><p>620MHz (1240MHz)</p></td>
<td><p>GDDR5 3000MHz (256bit)</p></td>
<td><p>96.0GB/s</p></td>
<td><p>384</p></td>
<td><p>2-way</p></td>
<td><p>100W</p></td>
<td><p>12 API<br />
<small>(FL:11_0)</small></p></td>
<td><p>4.6</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 570M</p></td>
<td><p>〇</p></td>
<td><p>GF114, N12E-GT (40nm)</p></td>
<td><p>575MHz (1150MHz)</p></td>
<td><p>GDDR5 3000MHz (192bit)</p></td>
<td><p>72.0GB/s</p></td>
<td><p>336</p></td>
<td><p>75W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 560M</p></td>
<td><p>〇</p></td>
<td><p>GF116, N12E-GS (40nm)</p></td>
<td><p>775MHz (1550MHz)</p></td>
<td><p>GDDR5 2500MHz (192bit)</p></td>
<td><p>60.0GB/s</p></td>
<td><p>192</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 555M</p></td>
<td></td>
<td><p>GF116, N12E-GE (40nm)</p></td>
<td><p>675MHz (1350MHz)</p></td>
<td><p>DDR3 1800MHz (128bit)</p></td>
<td><p>28.8GB/s</p></td>
<td><p>144</p></td>
<td><p>×</p></td>
<td><p>35W</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>GF108-400-A1 (40nm)</p></td>
<td><p>753MHz (1506MHz)</p></td>
<td><p>GDDR5 3136MHz (128bit)</p></td>
<td><p>50.18GB/s</p></td>
<td><p>96</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 550M</p></td>
<td></td>
<td><p>GF108, N12P-GT (40nm)</p></td>
<td><p>740MHz (1480MHz)</p></td>
<td><p>DDR3 1800MHz (128bit)</p></td>
<td><p>28.8GB/s</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 540M</p></td>
<td></td>
<td><p>GF108, N12P-GS (40nm)</p></td>
<td><p>672MHz (1344MHz)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 525M</p></td>
<td></td>
<td><p>GF108, N12P-GE (40nm)</p></td>
<td><p>600MHz (1200MHz)</p></td>
<td><p>25W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 520MX</p></td>
<td></td>
<td><p>GF119, N12P-GVR (40nm)</p></td>
<td><p>900MHz (1800MHz)</p></td>
<td><p>DDR3 1800MHz (64bit)</p></td>
<td><p>14.4GB/s</p></td>
<td><p>48</p></td>
<td><p>20W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 520M</p></td>
<td></td>
<td></td>
<td></td>
<td><p>DDR3 1600MHz (64bit)</p></td>
<td><p>12.8GB/s</p></td>
<td><p>12W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce 600 M Series

**GeForce 600 M Series**（ジーフォース・600・エム・シリーズ）は、GeForce 600シリーズのノートPC向け製品群である。FermiアーキテクチャとKeplerアーキテクチャが混在する。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>MXM</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック (CUDAコアクロック)</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>メモリ帯域</p></th>
<th><p>CUDAコア数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX<br />
<small>(Feature Level)</small></p></th>
<th><p>OpenGL</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce GTX 680MX</p></td>
<td><p>〇</p></td>
<td><p>GK104, N13E-GTX2-A2 (28nm)</p></td>
<td><p>720MHz</p></td>
<td><p>GDDR5 5000MHz (256bit)</p></td>
<td><p>160.0GB/s</p></td>
<td><p>1536</p></td>
<td><p>2-way</p></td>
<td><p>122W</p></td>
<td><p>12 API<br />
<small>(FL:11_0)</small></p></td>
<td><p>4.6</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 680M</p></td>
<td><p>〇</p></td>
<td><p>GK104, N13E-GTX-A2 (28nm)</p></td>
<td><p>720MHz</p></td>
<td><p>GDDR5 3600MHz (256bit)</p></td>
<td><p>115.2GB/s</p></td>
<td><p>1344</p></td>
<td><p>100W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 675MX</p></td>
<td><p>〇</p></td>
<td><p>GK104, N13E-GSR-A2 (28nm)</p></td>
<td><p>600MHz</p></td>
<td><p>960</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 675M</p></td>
<td><p>〇</p></td>
<td><p>GF114, N13E-GS1-A1 (40nm)</p></td>
<td><p>620MHz (1240MHz)</p></td>
<td><p>GDDR5 3000MHz (256bit)</p></td>
<td><p>96.0GB/s</p></td>
<td><p>384</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 670MX</p></td>
<td><p>〇</p></td>
<td><p>GK104, N13E-GR-A2 (28nm)</p></td>
<td><p>601MHz</p></td>
<td><p>GDDR5 2800MHz (192bit)</p></td>
<td><p>67.2GB/s</p></td>
<td><p>960</p></td>
<td><p>75W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 670M</p></td>
<td><p>〇</p></td>
<td><p>GF114, N13E-GS1-LP (40nm)</p></td>
<td><p>598MHz (1196MHz)</p></td>
<td><p>GDDR5 3000MHz (192bit)</p></td>
<td><p>72.0GB/s</p></td>
<td><p>336</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 660M</p></td>
<td><p>〇</p></td>
<td><p>GK107, N13E-GE-A2 (28nm)</p></td>
<td><p>950MHz</p></td>
<td><p>GDDR5 4000MHz (128bit)</p></td>
<td><p>64.0GB/s</p></td>
<td><p>384</p></td>
<td><p>50W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 650M</p></td>
<td></td>
<td><p>GK107, N13P-GT-A2 (28nm)</p></td>
<td><p>850MHz</p></td>
<td><p>DDR3 1800MHz (128bit)</p></td>
<td><p>28.8GB/s</p></td>
<td><p>-</p></td>
<td><p>45W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 645M</p></td>
<td></td>
<td><p>GK107, N13P-GS (28nm)</p></td>
<td><p>709MHz</p></td>
<td><p>32W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 640M</p></td>
<td></td>
<td><p>GK107, N13P-GS (28nm)</p></td>
<td><p>625MHz</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 640M LE</p></td>
<td></td>
<td><p>GK107, N13P-LP (28nm)</p></td>
<td><p>500MHz</p></td>
<td><p>20W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 635M</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>35W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 630M</p></td>
<td></td>
<td><p>GF117, N13P-GL-A1 (28nm)</p></td>
<td><p>800MHz (1600MHz)</p></td>
<td><p>GDDR5 3600MHz (128bit)</p></td>
<td><p>57.6GB/s</p></td>
<td><p>96</p></td>
<td><p>33W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 625M</p></td>
<td></td>
<td><p>GF117, N13M-GS-B-A2 (28nm)</p></td>
<td><p>625MHz (1250MHz)</p></td>
<td><p>DDR3 1800MHz (64bit)</p></td>
<td><p>14.4GB/s</p></td>
<td><p>15W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 620M</p></td>
<td></td>
<td><p>GF108, N13P-GLP (40nm)</p></td>
<td><p>660MHz (1320MHz)</p></td>
<td><p>DDR3 1800MHz (128bit)</p></td>
<td><p>28.8GB/s</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 610M</p></td>
<td></td>
<td><p>GF119, N13M-GE (40nm)</p></td>
<td><p>738MHz (1476MHz)</p></td>
<td><p>DDR3 1800MHz (64bit)</p></td>
<td><p>14.4GB/s</p></td>
<td><p>48</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce 700 M Series

**GeForce 700 M Series**（ジーフォース・700・エム・シリーズ）は、GeForce 700シリーズのノートPC向け製品群である。720M以下を除き、Keplerアーキテクチャとなった。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>MXM</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック [Boost]</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>メモリ帯域</p></th>
<th><p>CUDAコア数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX<br />
<small>(Feature Level)</small></p></th>
<th><p>OpenGL</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce GTX 780M</p></td>
<td><p>〇</p></td>
<td><p>GK104, N14E-GTX-A2 (28nm)</p></td>
<td><p>771MHz [797MHz]</p></td>
<td><p>GDDR5 5000MHz (256bit)</p></td>
<td><p>160.0GB/s</p></td>
<td><p>1536</p></td>
<td><p>2-way</p></td>
<td><p>122W</p></td>
<td><p>12 API<br />
<small>(FL:11_0)</small></p></td>
<td><p>4.6</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 770M</p></td>
<td><p>〇</p></td>
<td><p>GK106, N14E-GS-A1 (28nm)</p></td>
<td><p>706MHz [797MHz]</p></td>
<td><p>GDDR5 4000MHz (192bit)</p></td>
<td><p>96.0GB/s</p></td>
<td><p>960</p></td>
<td><p>75W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 765M</p></td>
<td><p>〇</p></td>
<td><p>GK106, N14E-GE-B-A1 (28nm)</p></td>
<td><p>797MHz [863MHz]</p></td>
<td><p>GDDR5 4000MHz (128bit)</p></td>
<td><p>64.0GB/s</p></td>
<td><p>768</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 760M</p></td>
<td></td>
<td><p>GK106, N14E-GL-A1 (28nm)</p></td>
<td><p>628MHz [657MHz]</p></td>
<td><p>55W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 755M</p></td>
<td><p>〇</p></td>
<td><p>GK107 (28nm)</p></td>
<td><p>980MHz</p></td>
<td><p>GDDR5 5400MHz (128bit)</p></td>
<td><p>86.4GB/s</p></td>
<td><p>384</p></td>
<td><p>rowspan="11" </p></td>
<td><p>50W</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 750M</p></td>
<td><p>〇</p></td>
<td><p>GK107 (28nm)</p></td>
<td><p>941MHz [967MHz]</p></td>
<td><p>GDDR5 4000MHz (128bit)</p></td>
<td><p>64.0GB/s</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 745M</p></td>
<td></td>
<td><p>GK107 (28nm)</p></td>
<td><p>837MHz</p></td>
<td><p>DDR3 1800MHz (128bit)</p></td>
<td><p>28.8GB/s</p></td>
<td><p>45W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 740M</p></td>
<td><p>〇</p></td>
<td><p>GK208 (28nm)</p></td>
<td><p>980MHz</p></td>
<td><p>DDR3 1800MHz (64bit)</p></td>
<td><p>14.4GB/s</p></td>
<td><p>33W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GT 735M</p></td>
<td></td>
<td><p>GK208 (28nm)</p></td>
<td><p>575MHz</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 730M</p></td>
<td><p>〇</p></td>
<td><p>GK107 (28nm)</p></td>
<td><p>725MHz</p></td>
<td><p>DDR3 1800MHz (128bit)</p></td>
<td><p>28.8GB/s</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>〇</p></td>
<td><p>GK208 (28nm)</p></td>
<td><p>719MHz [758MHz]</p></td>
<td><p>DDR3 1600MHz (64bit)</p></td>
<td><p>12.8GB/s</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GT 720M</p></td>
<td><p>〇</p></td>
<td><p>GK208 (28nm)</p></td>
<td><p>719MHz [758MHz]</p></td>
<td><p>192</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>GF117 (28nm)</p></td>
<td><p>775MHz</p></td>
<td><p>96</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 710M</p></td>
<td></td>
<td><p>GK208 (28nm)</p></td>
<td><p>719MHz</p></td>
<td><p>DDR3 1800MHz (64bit)</p></td>
<td><p>14.4GB/s</p></td>
<td><p>192</p></td>
<td><p>15W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>GF117 (28nm)</p></td>
<td><p>775MHz</p></td>
<td><p>DDR3 1800MHz (64bit)</p></td>
<td><p>14.4GB/s</p></td>
<td><p>96</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce 800 M Series

**GeForce 800 M Series**（ジーフォース・800・エム・シリーズ）は、GeForce 700シリーズのノートPC向け製品群である。Fermiから第1世代Maxwellまでの3世代のアーキテクチャが混在する。下位モデルにもMXM (Mobile pci eXpress Module)規格品が存在するが、消費電力が高い。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>MXM</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック [Boost]</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>メモリ帯域</p></th>
<th><p>CUDAコア数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX<br />
<small>(Feature Level)</small></p></th>
<th><p>OpenGL</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce GTX 880M</p></td>
<td><p>〇</p></td>
<td><p>GK104, N15E-GX-A2 (28nm)</p></td>
<td><p>954MHz [993MHz]</p></td>
<td><p>GDDR5 5000MHz (256bit)</p></td>
<td><p>160GB/s</p></td>
<td><p>1536</p></td>
<td><p>2-way</p></td>
<td><p>122W</p></td>
<td><p>12 API<br />
<small>(FL:11_0)</small></p></td>
<td><p>4.6</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 870M</p></td>
<td><p>〇</p></td>
<td><p>GK104, N15E-GT-A2 (28nm)</p></td>
<td><p>941MHz [967MHz]</p></td>
<td><p>GDDR5 5000MHz (192bit)</p></td>
<td><p>120GB/s</p></td>
<td><p>1344</p></td>
<td><p>100W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 860M</p></td>
<td><p>〇</p></td>
<td><p>GM107, N15P-GX-A1 (28nm)</p></td>
<td><p>1020MHz [1085MHz]</p></td>
<td><p>GDDR5 5000MHz (128bit)</p></td>
<td><p>80GB/s</p></td>
<td><p>640</p></td>
<td><p>75W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>GK104, N15P-GX-A1 (28nm)</p></td>
<td><p>797MHz [915MHz]</p></td>
<td><p>1152</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 850M</p></td>
<td></td>
<td><p>GM107, N15P-GT-A1 (28nm)</p></td>
<td><p>902MHz [N/A]</p></td>
<td><p>DDR3 2000MHz (64bit)</p></td>
<td><p>16GB/s</p></td>
<td><p>640</p></td>
<td><p>rowspan="8" </p></td>
<td><p>45W</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 840M</p></td>
<td></td>
<td><p>GM108, N15S-GT (28nm)</p></td>
<td><p>1029MHz [1124MHz]</p></td>
<td><p>384</p></td>
<td><p>33W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce 830M</p></td>
<td></td>
<td><p>GM108, N15S-GM (28nm)</p></td>
<td><p>1082MHz [1150MHz]</p></td>
<td><p>DDR3 1800MHz (64bit)</p></td>
<td><p>14.4GB/s</p></td>
<td><p>256</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 820M</p></td>
<td><p>〇</p></td>
<td><p>GK107 (28nm)</p></td>
<td><p>810MHz</p></td>
<td><p>DDR3 1802MHz (128bit)</p></td>
<td><p>28.83GB/s</p></td>
<td><p>384</p></td>
<td><p>45W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>GF117, N15V-GM (28nm)</p></td>
<td><p>775MHz</p></td>
<td><p>DDR3 1800MHz (64bit)</p></td>
<td><p>14.4GB/s</p></td>
<td><p>96</p></td>
<td><p>15W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 810M</p></td>
<td><p>〇</p></td>
<td><p>GK107 (28nm)</p></td>
<td><p>810MHz</p></td>
<td><p>DDR3 1802MHz (128bit)</p></td>
<td><p>28.83GB/s</p></td>
<td><p>384</p></td>
<td><p>45W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>GF117, N14M-GL (28nm)</p></td>
<td><p>738MHz</p></td>
<td><p>DDR3 1800MHz (64bit)</p></td>
<td><p>14.4GB/s</p></td>
<td><p>48</p></td>
<td><p>15W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce 800M</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce 900 M Series

**GeForce 900 M Series**（ジーフォース・900・エム・シリーズ）は、GeForce 900シリーズのノートPC向け製品群である。第1世代と第2世代のMaxwellアーキテクチャが混在する。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>MXM</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック [Boost]</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>メモリ帯域</p></th>
<th><p>CUDAコア数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX<br />
<small>(Feature Level)</small></p></th>
<th><p>OpenGL</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce GTX 950M</p></td>
<td><p>rowspan="2" </p></td>
<td><p>GM107 (28nm)</p></td>
<td><p>914MHz [1124MHz]</p></td>
<td><p>DDR3 2000MHz (128bit)</p></td>
<td><p>32GB/s</p></td>
<td><p>640</p></td>
<td><p>-</p></td>
<td><p>75W</p></td>
<td><p>12 API<br />
<small>(FL:12_1)</small></p></td>
<td><p>4.6</p></td>
</tr>
<tr class="even">
<td><p>GDDR5 5GHz相当 (128bit)</p></td>
<td><p>80GB/s</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 960M</p></td>
<td></td>
<td><p>1097MHz [1176MHz]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 965M</p></td>
<td><p>〇</p></td>
<td></td>
<td></td>
<td><p>1024</p></td>
<td><p>2-way</p></td>
<td><p>90W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 970M</p></td>
<td><p>〇</p></td>
<td><p>GM204 (28nm)</p></td>
<td><p>924MHz [993MHz]</p></td>
<td><p>GDDR5 5GHz相当 (192bit)</p></td>
<td><p>120GB/s</p></td>
<td><p>1280</p></td>
<td><p>100W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 970MX</p></td>
<td><p>〇</p></td>
<td><p>941MHz [993MHz]</p></td>
<td><p>|1408</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 980M</p></td>
<td><p>〇</p></td>
<td><p>1038MHz [1127MHz]</p></td>
<td><p>GDDR5 5GHz相当 (256bit)</p></td>
<td><p>160GB/s</p></td>
<td><p>1536</p></td>
<td><p>125W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 980MX</p></td>
<td><p>〇</p></td>
<td><p>1048MHz [1127MHz]</p></td>
<td><p>|1664</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 980[117]</p></td>
<td></td>
<td><p>1126MHz [1216MHz]</p></td>
<td><p>GDDR5 7GHz相当 (256bit)</p></td>
<td><p>224GB/s</p></td>
<td><p>2048</p></td>
<td><p>165W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce 10 Series Note PC

**GeForce 10 Series Note PC** は、GeForce 10シリーズのノートPC向け製品群である。Pascalアーキテクチャを採用する。デスクトップ版に近い性能となり、製品名末尾のモバイルを示す「M」が無くなった\[118\]。

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>MXM</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック [Boost]</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>メモリ帯域</p></th>
<th><p>CUDAコア数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX<br />
<small>(Feature Level)</small></p></th>
<th><p>OpenGL</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce GTX 1050</p></td>
<td><p>〇</p></td>
<td><p>GP107 (14nm)</p></td>
<td><p>1354MHz [1493MHz]</p></td>
<td><p>GDDR5 7GHz相当 (128bit)</p></td>
<td><p>112GB/s</p></td>
<td><p>640</p></td>
<td><p>rowspan="4" </p></td>
<td><p>75W</p></td>
<td><p>12 API<br />
<small>(FL:12_1)</small></p></td>
<td><p>4.6</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 1050 Ti</p></td>
<td></td>
<td><p>1493MHz [1620MHz]</p></td>
<td><p>768</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 1060 (3GB)</p></td>
<td><p>〇</p></td>
<td><p>GP106 (16nm)</p></td>
<td><p>1404MHz [1670MHz]</p></td>
<td><p>GDDR5 8GHz相当 (192bit)</p></td>
<td><p>192GB/s</p></td>
<td><p>1280</p></td>
<td><p>80W</p></td>
<td><p>3GB版も6GB版もコア数は同じで、3GB版はデスクトップ版よりもCUDAコアが128基増加</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 1060 (6GB)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 1070</p></td>
<td><p>〇</p></td>
<td><p>GP104 (16nm)</p></td>
<td><p>1442MHz [1645MHz]</p></td>
<td><p>GDDR5 8GHz相当 (256bit)</p></td>
<td><p>256GB/s</p></td>
<td><p>2048</p></td>
<td><p>2-way</p></td>
<td><p>120W</p></td>
<td><p>デスクトップ版よりもCUDAコアが128基増加</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 1080</p></td>
<td><p>〇</p></td>
<td><p>1556MHz [1733MHz]</p></td>
<td><p>GDDR5X 10GHz相当 (256bit)</p></td>
<td><p>320GB/s</p></td>
<td><p>2560</p></td>
<td><p>150W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce 20 Series Gaming Note PC

**GeForce 20 Series Gaming Note PC** は、GeForce 20シリーズのノートPC向け製品群である。Turingアーキテクチャを採用する。

2019年1月8日に発表された。\[119\]

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>MXM</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック [Boost]</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>メモリ帯域</p></th>
<th><p>CUDAコア数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX<br />
<small>(Feature Level)</small></p></th>
<th><p>OpenGL</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce RTX 2060</p></td>
<td></td>
<td><p>TU106 (12nm)</p></td>
<td><p>960MHz [1185MHz]</p></td>
<td><p>GDDR6 14GHz相当 (192bit)</p></td>
<td><p>336GB/s</p></td>
<td><p>1920</p></td>
<td><p>rowspan="3" </p></td>
<td><p>65 - 90W</p></td>
<td><p>12 API<br />
<small>(FL:12_1)</small></p></td>
<td><p>4.6</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce RTX 2070</p></td>
<td></td>
<td><p>TU106 (12nm)</p></td>
<td><p>885MHz [1185MHz] - 1215MHz [1440MHz]</p></td>
<td><p>GDDR6 14GHz相当 (256bit)</p></td>
<td><p>448GB/s</p></td>
<td><p>2304</p></td>
<td><p>80 - 115W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce RTX 2080</p></td>
<td></td>
<td><p>TU104 (12nm)</p></td>
<td><p>735MHz [1095MHz] - 1380MHz [1590MHz]</p></td>
<td><p>GDDR6 14GHz相当 (256bit)</p></td>
<td><p>448GB/s</p></td>
<td><p>2944</p></td>
<td><p>80 - 150+W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### GeForce 16 Series Gaming Note PC

**GeForce 16 Series Gaming Note PC** は、GeForce 16シリーズのノートPC向け製品群である。Turingアーキテクチャを採用する。

2019年4月23日に、デスクトップ版のGTX 1650の発売と当時に発表された。\[120\]

<table>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>MXM</p></th>
<th><p>コア名 (プロセス)</p></th>
<th><p>コアクロック [Boost]</p></th>
<th><p>メモリクロック （バス幅）</p></th>
<th><p>メモリ帯域</p></th>
<th><p>CUDAコア数</p></th>
<th><p>SLI</p></th>
<th><p>消費電力</p></th>
<th><p>DirectX<br />
<small>(Feature Level)</small></p></th>
<th><p>OpenGL</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce GTX 1650(GDDR5)</p></td>
<td></td>
<td><p>TU117 (12nm)</p></td>
<td><p>1020MHz [1245MHz] - 1395MHz [1560MHz]</p></td>
<td><p>GDDR5 8GHz相当 (128bit)</p></td>
<td><p>128GB/s</p></td>
<td><p>1024</p></td>
<td><p>rowspan="2" </p></td>
<td><p>30 - 50W</p></td>
<td><p>12 API<br />
<small>(FL:12_1)</small></p></td>
<td><p>4.6</p></td>
<td><p>デスクトップ版と違いフルスペックのTU117コアを使用し、デスクトップ版よりもCUDAコアが128基増加</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 1650 Ti</p></td>
<td></td>
<td><p>1035MHz [1200MHz] - 1350MHz [1485MHz]</p></td>
<td><p>GDDR6 12GHz相当 (128bit)</p></td>
<td><p>35 - 55W</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 1660 Ti</p></td>
<td></td>
<td><p>TU116 (12nm)</p></td>
<td><p>1140MHz [1335MHz] - 1455MHz [1590MHz]</p></td>
<td><p>GDDR6 12GHz相当 (192bit)</p></td>
<td><p>192GB/s</p></td>
<td><p>1536</p></td>
<td></td>
<td><p>60 - 80W</p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 注釈

## 出典

## 関連項目

  - [NVIDIA](../Page/NVIDIA.md "wikilink")
  - [ForceWare](../Page/ForceWare.md "wikilink")
  - [NVIDIA Quadro](../Page/NVIDIA_Quadro.md "wikilink") - OpenGLに最適化されたシリーズ
  - [NVIDIA Tesla](https://ja.wikipedia.org/wiki/NVIDIA_Tesla "wikilink") - [高性能計算](../Page/高性能計算.md "wikilink")に最適化されたシリーズ
  - [NVIDIA Tegra](https://ja.wikipedia.org/wiki/NVIDIA_Tegra "wikilink") - 省電力[統合型プロセッサのシリーズ](../Page/System-on-a-chip.md "wikilink")
  - [NV1](https://ja.wikipedia.org/wiki/NV1 "wikilink")
  - [SLI](../Page/Scalable_Link_Interface.md "wikilink")
  - [CUDA](../Page/CUDA.md "wikilink")
  - [PhysX](../Page/PhysX.md "wikilink")
  - [AMD Radeon](../Page/AMD_Radeon.md "wikilink") - GeForceと競合するGPUシリーズ
  - [Microsoft DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")
      - [Direct3D](../Page/Direct3D.md "wikilink")
  - [OpenGL](../Page/OpenGL.md "wikilink")
  - [OpenCL](../Page/OpenCL.md "wikilink")

## 外部リンク

  - [NVIDIA GeForce 公式サイト](https://www.nvidia.com/ja-jp/geforce/)

  -
  -
  -
  -
  -
  - [GPU Database TechPowerUp](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&sort=released)

[Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink") [Category:NVIDIA](https://ja.wikipedia.org/wiki/Category:NVIDIA "wikilink")

1.  [【レビュー】初の統合型シェーダーアーキテクチャ「GeForce 8800シリーズ」を試す (1) 新アーキテクチャで登場したG80 | マイナビニュース](http://news.mynavi.jp/articles/2006/11/09/g80/)
2.  [Maxwell and DirectX 12 Delivered | The Official NVIDIA Blog](http://blogs.nvidia.com/blog/2014/09/19/maxwell-and-dx12-delivered/)
3.  [NVIDIAの最新ドライバでFermi世代のGPUがDirectX 12対応に ～3年越しに公約を果たす - PC Watch](http://pc.watch.impress.co.jp/docs/news/1068752.html)
4.  [［COMPUTEX］「現行のGeForceが対応するDirectX 12の機能レベル」をNVIDIAが明らかに。VR向けGameWorksもリリース - 4Gamer.net](http://www.4gamer.net/games/274/G027467/20150529001/)
5.  [CUDA Legacy GPUs | NVIDIA Developer](https://developer.nvidia.com/cuda-legacy-gpus)
6.  [NVIDIAのGeForce用PhysXドライバを試す | PC Watch](https://pc.watch.impress.co.jp/docs/2008/0926/physx.htm)
7.  [Release 387 Graphics Drivers for Windows, Version 388.00; RN-08399-388.00_v01 | October 23, 2017; Windows 10 / Windows 8.1 / Windows 8 / Windows 7](http://us.download.nvidia.com/Windows/388.00/388.00-win10-win8-win7-desktop-release-notes.pdf)
8.  [Release 349 Graphics Drivers for Windows, Version 350.12; RN-W35012-01v01 | April 13, 2015; Windows Vista / Windows 7 / Windows 8 / Windows 8.1](http://jp.download.nvidia.com/Windows/350.12/350.12-win8-win7-winvista-desktop-release-notes.pdf)
9.  [「Dynamic Super Resolution」を試す。「ディスプレイ解像度を超えた精細感をゲームにもたらす」という新機能は使えるのか - 4Gamer.net](http://www.4gamer.net/games/022/G002210/20141027007/)
10. [3D Vision | Supported GPUs | GeForce](https://www.geforce.com/hardware/technology/3d-vision/supported-gpus)
11. [Vulkan Driver Support | NVIDIA Developer](https://developer.nvidia.com/vulkan-driver)
12. [nVidia GeForce FX 5800 - nVidia's Thoughts](http://www.youtube.com/watch?v=WOVjZqC1AE4)
13. [1枚でGeForce 6800 GT SLIの巨大グラフィックスカード「Extreme N6800 GT Dual」を試す - 4Gamer.net](http://www.4gamer.net/games/022/G002225/20050623222000/)
14.
15.
16.
17.
18. [NVIDIAのDX 10.1 GPU上位版、GeForce GT 240が発売 - PC Watch](https://akiba-pc.watch.impress.co.jp/hotline/20091121/etc_nvidia.html)
19. [SP216基版「GeForce GTX 260」レビュー掲載。結局，これは何なのか？ - 4Gamer.net](https://www.4gamer.net/games/050/G005004/20081017041/)
20.
21.
22. [「GeForce GTX 550 Ti」を試す。バランスの取れた性能＆価格と，バランスを欠く消費電力が特徴 - 4Gamer.net](http://www.4gamer.net/games/123/G012385/20110315018/)
23. [謎のGPU「GeForce GTX 560 SE」をテスト。性能はGTX 560とGTX 550 Tiのちょうど中間に - 4Gamer.net](http://www.4gamer.net/games/123/G012385/20120417026/)
24. [ついに登場した「GeForce GTX 560」を試す。予想以上に「よい子」で，価格次第ながら相当に面白い存在だ - 4Gamer.net](http://www.4gamer.net/games/123/G012385/20110517060/)
25.
26. [検証済みビデオボードPN-K321｜インフォメーションディスプレイ｜法人のお客様へ（BtoB）：シャープ](http://www.sharp.co.jp/business/lcd-display/support/pnk321_video.html)
27. [「GeForce GTX 680」レビュー（後編）。NVIDIA版Turbo Boostになる「GPU Boost」とは何か - 4Gamer.net](http://www.4gamer.net/games/120/G012093/20120322072/)
28. [「GeForce GTX 650」レビュー。1万円台前半で買えるKeplerはコスト重視型ゲーマーの福音となるか - 4Gamer.net](http://www.4gamer.net/games/120/G012093/20120916003/)
29. [「GeForce GTX 650 Ti」レビュー。第1世代Kepler最後の1ピースは誰のためのGPUなのか - 4Gamer.net](http://www.4gamer.net/games/120/G012093/20121005112/)
30. [「GeForce GTX 650 Ti BOOST」レビュー。1万9800円で市場投入される“GTX 660の弟分”は買いなのか - 4Gamer.net](http://www.4gamer.net/games/120/G012093/20130325075/)
31. [「GeForce GTX 660」レビュー。これは2万円台前半から買える“超低消費電力版GTX 580”だ\! - 4Gamer.net](http://www.4gamer.net/games/120/G012093/20120905100/)
32. [「GeForce GTX 660 Ti」レビュー。Kepler世代初のミドルクラスGPUはGTX 580より速かった - 4Gamer.net](http://www.4gamer.net/games/120/G012093/20120814062/)
33. [「GeForce GTX 670」レビュー。GTX 680比で9割弱の性能を発揮するが，すべては価格とラインナップ次第か - 4Gamer.net](http://www.4gamer.net/games/120/G012093/20120509088/)
34. [「GeForce GTX 680」レビュー（前編）。低消費電力で「扱いやすい史上最速GPU」に - 4Gamer.net](http://www.4gamer.net/games/120/G012093/20120320002/)
35. [Geforce Gen3 Support On X79 Platform NVIDIA](http://nvidia.custhelp.com/app/answers/detail/a_id/3135/~/geforce-gen3-support-on-x79-platform)
36. [「GeForce GTX 690」レビュー。「プレイアブルな3画面環境」をカード1枚で実現可能に - 4Gamer.net](http://www.4gamer.net/games/120/G012093/20120503003/)
37. [NVIDIA，「GeForce GTX 750 Ti＆GTX 750」発表。新世代GPUアーキテクチャ「Maxwell」第1弾の詳細をまとめてみた - 4Gamer.net](http://www.4gamer.net/games/216/G021677/20140215011/)
38. [ASUS、ビデオメモリ4GBのGTX 750 Ti OCモデル「STRIX-GTX750TI-DC2OC-4GD5」 - エルミタージュ秋葉原](http://www.gdm.or.jp/pressrelease/2015/0212/103514)
39. [「GeForce GTX 750 Ti」「GeForce GTX 750」をテスト。TDP 60 W以下で登場した第1世代Maxwellは速いのか - 4Gamer.net](http://www.4gamer.net/games/216/G021677/20140218026/)
40. [「GeForce GTX 760」レビュー。「GTX 660 Tiの弱点」にメスを入れてきた後継製品はありやなしや - 4Gamer.net](http://www.4gamer.net/games/216/G021677/20130625069/)
41. [userbenchmark Nvidia GTX 660 Ti vs 760](http://gpu.userbenchmark.com/Compare/Nvidia-GTX-760-vs-Nvidia-GTX-660-Ti/2159vs2183)
42. [「GeForce GTX 770」レビュー。GTX 700シリーズ第2弾となる“メモリクロック7 GHz版GTX 680”は買いなのか - 4Gamer.net](http://www.4gamer.net/games/216/G021677/20130527035/)
43. [「GeForce GTX 780」レビュー。新世代GPUシリーズ第1弾に見せかけた「低価格版GTX TITAN」の実力を探る - 4Gamer.net](http://www.4gamer.net/games/216/G021677/20130523038/)
44. [「GeForce GTX 780 Ti」レビュー。GTX TITANより300ドル安い“史上最速GPU”，その実力は？ - 4Gamer.net](http://www.4gamer.net/games/216/G021677/20131107065/)
45. [「GeForce GTX TITAN」登場。500円玉より大きなモンスターGPUの“性能以外”を徹底解説 - 4Gamer.net](http://www.4gamer.net/games/204/G020420/20130217001/)
46. [TOP500\#2012年11月](https://ja.wikipedia.org/wiki/TOP500#2012年11月 "wikilink")
47. [NVIDIA，Kepler世代の最上位GPU「GeForce GTX TITAN Black」を発表 - 4Gamer.net](http://www.4gamer.net/games/204/G020420/20140217058/)
48. [「GeForce GTX TITAN Z」レビュー。史上最も高価な“2999ドルのGeForce”はどれだけ速い？ - 4Gamer.net](http://www.4gamer.net/games/204/G020420/20140627105/)
49. [価格は約40万円～約45万円！「GeForce GTX TITAN Z」が降臨 - ASCII.jp](http://ascii.jp/elem/000/000/898/898851/)
50. [supported-MFAA | GeForce](https://www.geforce.com/hardware/technology/mfaa)
51. [Maxwell 2 Architecture Introducing GM204 - The NVIDIA GeForce GTX 980 Review Maxwell Mark 2](https://www.anandtech.com/show/8526/nvidia-geforce-gtx-980-review/3)
52. [Virtual Reality | Supported GPUs | GeForce](https://www.geforce.com/hardware/technology/vr/supported-gpus)
53. [NVIDIA、オンラインRTSゲーム向けのエントリーGPU「GeForce GTX 950」 - PC Watch](http://pc.watch.impress.co.jp/docs/news/20150820_716584.html)
54. [【レビュー】同列GPUから性能志向へとシフトした「GeForce GTX 950」の実力 - PC Watch](http://pc.watch.impress.co.jp/docs/topic/review/20150820_717129.html)
55. [「GeForce GTX 950」レビュー。ついに登場した900番台エントリーミドルの実力を検証する - 4Gamer.net](http://www.4gamer.net/games/274/G027467/20150820108/)
56. [実は買い\!Windows 10時代のミドルレンジモデル\!GeForce GTX 950をベンチマーク\! - パソコン工房](https://www.pc-koubou.jp/blog/gtx950_bench.php)
57. [「GeForce GTX 960」レビュー。第2世代Maxwell初のミドルクラスGPUは，得手不得手のはっきりした低消費電力モデルだ - 4Gamer.net](http://www.4gamer.net/games/274/G027467/20150121125/)
58.
59. [NVIDIAがGeForce GTX 970の「VRAM 3.5 GB問題」で訴えられる - GIGAZINE](https://gigazine.net/news/20150225-nvidia-lawsuit-gtx-970/net)
60. [NVIDIA，GTX 970のスペックを修正。L2キャッシュとROPのスペックが引き下げられる - 4Gamer.net](http://www.4gamer.net/games/274/G027467/20150130080/)
61. [NVIDIAのGPU開発部門責任者に聞く「GeForce GTX 970のVRAM 3.5 GB問題」 - 4Gamer.net](http://www.4gamer.net/games/274/G027467/20150130109/)
62. [「GeForce GTX 980 ＆ 970」レビュー。極めて高い電力効率が謳われる第2世代Maxwellの第1弾は「看板に偽りなし」 - 4Gamer.net](https://www.4gamer.net/games/274/G027467/20140918001/)
63. [【レビュー】Maxwell世代のハイエンド「GeForce GTX 980」ベンチマーク速報 - PC Watch](https://pc.watch.impress.co.jp/docs/topic/review/667457.html)
64. [NVIDIA、4K解像度に最適化した「GeForce GTX 980 Ti」 ～DirectX 12_1に完全対応 - PC Watch](http://pc.watch.impress.co.jp/docs/news/20150601_704466.html)
65. [【レビュー】NVIDIA、TITAN Xに肉薄し980を圧倒する「GeForce GTX 980 Ti」 ～価格は649ドルから - PC Watch](http://pc.watch.impress.co.jp/docs/topic/review/20150601_704669.html)
66. [「GeForce GTX 980 Ti」レビュー。649ドルで登場した「一般ユーザー向けフラグシップ」は，GTX TITAN Xキラーだ\!? - 4Gamer.net](http://www.4gamer.net/games/274/G027467/20150530003/)
67. [【レビュー】Maxwellのモンスター、「GeForce GTX TITAN X」をベンチマーク - PC Watch](http://pc.watch.impress.co.jp/docs/topic/review/20150318_693058.html)
68. [「GeForce GTX TITAN X」レビュー。3072基のシェーダプロセッサを集積した999ドルの新型フラグシップは，文句なしに速い - 4Gamer.net](http://www.4gamer.net/games/204/G020420/20150316083/)
69. [GEFORCE® GTX 10 シリーズ | NVIDIA GeForce](https://www.nvidia.com/ja-jp/geforce/products/)
70. [「GeForce GTX 1080」のSLI構成を試す。「SLI HB Bridge」は必須アイテムなのか？ - 4Gamer.net](http://www.4gamer.net/games/251/G025177/20160830068/)
71. [【特集】明らかとなったGeForce GTX 1080の詳細 ～新圧縮モードによるメモリ帯域の節約や新SLIブリッジなど - PC Watch](http://pc.watch.impress.co.jp/docs/topic/feature/20160517_757832.html)
72.
73. [NVIDIA，「GeForce GT 1030」を製品リストに追加。Pascal世代初のエントリー市場向けモデル - 4Gamer.net](http://www.4gamer.net/games/380/G038056/20170516085/)
74. [「GeForce GT 1030」と「Radeon RX 550」直接対決。新世代のエントリー市場向けGPUをゲーマー目線でチェックする - 4Gamer.net](http://www.4gamer.net/games/251/G025177/20170525163/)
75. [「GeForce GTX 1050 Ti」「GeForce GTX 1050」レビュー。上位モデルは「補助電源不要版GTX 960」だ - 4Gamer.net](http://www.4gamer.net/games/251/G025177/20161022012/)
76. [VRもギリギリ行ける? GeForce GTX 1050、同1050 Tiの情報が公開 - ドスパラ](http://www.dospara.co.jp/express/vr/271424)
77. [GeForce GTX 1050シリーズに「GeForce GTX 1050 3GB」が加わる。GTX 1050 Tiからメモリ容量とメモリインタフェースを削減 - 4Gamer.net](https://www.4gamer.net/games/251/G025177/20180522001/)
78. [「GeForce GTX 1060 3GB」レビュー。199ドルの「RX 470キラー」が持つポテンシャルに迫る - 4Gamer.net](http://www.4gamer.net/games/251/G025177/20160902132/)
79. [「GeForce GTX 1060」レビュー。249ドルの新世代ミドルクラスGPU，その性能はGTX 980並みで，消費電力はGTX 960並みだった - 4Gamer.net](http://www.4gamer.net/games/251/G025177/20160718008/)
80. [「GeForce GTX 1070」レビュー。449ドルの「Founders Edition」は，GTX 970より低い消費電力で，GTX TITAN Xより速い - 4Gamer.net](http://www.4gamer.net/games/251/G025177/20160528005/)
81. [「GeForce GTX 1070 Ti」レビュー。GTX 1080より100ドル安価な新型GPUは，2017年クリスマス商戦の主役となり得るか？ - 4Gamer.net](http://www.4gamer.net/games/251/G025177/20171101068/)
82. [「GeForce GTX 1080」レビュー。Pascal世代最初のGeForceは，GTX 980と同等の消費電力で，GTX 980 SLIと同等の性能を発揮する - 4Gamer.net](http://www.4gamer.net/games/251/G025177/20160517060/)
83. [「GeForce GTX 1080 Ti」レビュー。699ドルのGeForceは1200ドルのTITAN Xより本当に速かった - 4Gamer.net](http://www.4gamer.net/games/251/G025177/20170309070/)
84. [【レビュー】ゲーマーにとって“現実的な”ハイエンドGPU「GeForce GTX 1080 Ti」をテスト - PC Watch](https://pc.watch.impress.co.jp/docs/topic/review/1048722.html)
85. [NVIDIA，Pascal世代の新GPU「TITAN X」を発表。製品名から「GeForce」表記が外れた最上位モデルは，シェーダプロセッサ3584基を集積 - 4Gamer.net](https://www.4gamer.net/games/204/G020420/20160722012/)
86. [NVIDIA，「TITAN Xp」を製品リストに追加。GP102コアのフルスペックで1200ドル - 4Gamer.net](https://www.4gamer.net/games/204/G020420/20170406121/)
87. [NVIDIA、32bit版OSのサポートを終了へ - PC Watch](https://pc.watch.impress.co.jp/docs/news/1098690.html)
88. [デスクトップPC向け「GeForce GTX 1650」の販売がスタート。税込平均価格は2万2000円前後に - 4Gamer.net](https://www.4gamer.net/games/421/G042134/20190423107/)
89. [NVIDIA Launches GeForce GTX 1650 Budget Turing For $149, Available Today - AnandTech](https://www.anandtech.com/show/14255/nvidia-launches-geforce-gtx-1650-budget-turing-for-149-available-today)
90. [【Hothotレビュー】補助電源コネクタなしでどのぐらい性能が出せるか。「GeForce GTX 1650」をテスト - PC Watch](https://pc.watch.impress.co.jp/docs/column/hothot/1182169.html)
91. [玄人志向、TU106コア採用のGeForce GTX 1650ビデオカード](https://pc.watch.impress.co.jp/docs/news/1267161.html)
92. [GALAX、RTX 20シリーズと同じTU106ダイを採用する「GeForce GTX 1650 Ultra」](https://www.gdm.or.jp/pressrelease/2020/0630/353931)
93.
94. [「GeForce GTX 1660」レビュー。税別219ドルからという安価なTuringは性能だけでなく消費電力も要注目だ - 4Gamer.net](https://www.4gamer.net/games/421/G042134/20190313117/)
95. [NVIDIA，新型エントリー～ミドルクラスGPU「GeForce GTX 16 SUPER」シリーズを発表。GTX 1660 SUPERの実力をベンチマークで検証してみた - 4Gamer.net](https://www.4gamer.net/games/421/G042134/20191028066/)
96.
97. [「GeForce GTX 1660 Ti」レビュー。レイトレ非対応のTuringこそが新世代の鉄板GPUになる\! - 4Gamer.net](https://www.4gamer.net/games/421/G042134/20190220116/)
98.
99.
100.
101.
102.
103.
104.
105.
106.
107.
108.
109.
110.
111. [NVIDIA,「TITAN RTX」を発表。TU102コアのフルスペックで2499ドル - 4Gamer.net](https://www.4gamer.net/games/204/G020420/20181203130/)
112. [GeForce RTX 30 シリーズ グラフィックス カード概要 - NVIDIA](https://www.nvidia.com/ja-jp/geforce/graphics-cards/30-series/)
113. [NVIDIA Ampere GA102 GPU Architecture](https://www.nvidia.com/content/dam/en-zz/Solutions/geforce/ampere/pdf/NVIDIA-ampere-GA102-GPU-Architecture-Whitepaper-V1.pdf)
114. [西川善司の3DGE：GeForce RTX 30シリーズのアーキテクチャを探る。CUDA Coreの増量とRT Coreの高性能化に注目だ](https://www.4gamer.net/games/527/G052743/20200911024/)
115. [World’s Fastest Discrete Graphics Memory From Micron Powers NVIDIA’s Breakthrough Gaming Speeds | Micron Technology](https://investors.micron.com/news-releases/news-release-details/worlds-fastest-discrete-graphics-memory-micron-powers-nvidias)
116. [ASCII.jp：謎が多いGeForce RTX 3000シリーズのプロセスとGDDR6X　NVIDIA GPUロードマップ](https://ascii.jp/elem/000/004/027/4027542/)
117. [【レポート】米NVIDIA、デスクトップ向けGPU「GeForce GTX 980」をノートPC向けに提供 - マイナビニュース](http://news.mynavi.jp/articles/2015/09/22/nvidia/)
118. [モバイル版GeForce 10シリーズは、デスクトップ版と（ほぼ）同じ鬼スペック！ - ASCII.jp](http://ascii.jp/elem/000/001/213/1213009/)
119.
120. [NVIDIA，Turing GTXベースのノートPC向けGPU「GeForce GTX 1660 Ti」と「GeForce GTX 1650」を発表 - 4Gamer.net](https://www.4gamer.net/games/421/G042134/20190422066/)