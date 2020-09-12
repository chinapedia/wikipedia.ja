> この記事は[RDNA \(マイクロアーキテクチャ\)](https://ja.wikipedia.org/wiki/RDNA_\(マイクロアーキテクチャ\))から翻訳されています。


[サムネイル](https://ja.wikipedia.org/wiki/ファイル:Generic_block_diagram_of_a_GPU.svg "wikilink") **RDNA** (**Radeon DNA**) は[GPU](https://ja.wikipedia.org/wiki/GPU "wikilink")[マイクロアーキテクチャ](../Page/マイクロアーキテクチャ.md "wikilink")のコード名である。添付の命令セットは[AMD](https://ja.wikipedia.org/wiki/AMD "wikilink")。 RDNAを代表としている最初の製品ラインアップは、Radeon RX 5000シリーズ。 [AMD RadeonグラフィックスカードのNaviシリーズで使用されている](../Page/AMD_Radeon.md "wikilink")[TSMC](../Page/TSMC.md "wikilink")の7 nm FinFETグラフィックスチップを使用して製造されている。

## アーキテクチャ

AMDの[Computex基調講演で発表された最初の詳細は](../Page/COMPUTEX_TAIPEI.md "wikilink")、[グラフィックコアネクスト](https://ja.wikipedia.org/wiki/Graphics_Core_Next "wikilink")（GCN）アーキテクチャが存在する以前の側面を示唆していたが、このアーキテクチャは新しいプロセッサ設計を特徴としていた。 [GDDR6](https://ja.wikipedia.org/wiki/GDDR6 "wikilink")メモリのサポートにより、マルチレベルキャッシュ階層と改善されたレンダリングパイプラインを備えている。

RDNAは、[プリミティブシェーダーも動作する](../Page/シェーダー.md "wikilink")。 この機能は[Vegaアーキテクチャのハードウェアに存在していたが](https://ja.wikipedia.org/wiki/AMD_RX_Vega "wikilink")、実際のパフォーマンスを向上させることは困難であったため、AMDは行わなかった。 RDNAのプリミティブシェーダーはコンパイラー制御である。

RDNAのディスプレイコントローラーは、Display Stream Compression 1.2aをサポートするように更新され、4k 240 Hz、HDR 4K 120 Hz、およびHDR 8K 60 Hzで出力が可能。

## 命令セット

AMDのGPUOpenWebサイトは、AMD「RDNA」世代デバイスの環境、組織、およびプログラムの状態を説明することを目的としたPDFドキュメントをホストしている。 プログラマーやコンパイラーがアクセスできるこのプロセッサーファミリーにネイティブな命令セットとマイクロコードフォーマットについて詳しく説明している。

RDNA命令セットはAMDが所有している。 RDNA命令セットは、いくつかの変更を加えたGCN命令セットに基づいている。

## GCNとRDNA1の違い

コードのスケジュール方法に影響するアーキテクチャ上の変更がある。

シングルサイクル命令の問題：GCNは、4サイクルごとに1回、ウェーブごとに1つの命令を発行。RDNAはサイクルごとに命令を発行。

Wave32：GCNは、64スレッド（作業項目）の波面サイズを使用した。RDNAは、32スレッドと64スレッドの両方の波面サイズをサポートしている。

ワークグループプロセッサ：GCNは、シェーダーハードウェアを、スカラーALUとベクトルALU、LDS、およびメモリアクセスを含む「計算ユニット」（CU）にグループ化している。1つのCUには、メモリへの1つのパスを共有する4つのSIMD16が含まる。RDNAは「ワークグループプロセッサ」（「WGP」）を導入している。WGPは、シェーダー計算ハードウェア/コンピューティングの基本ユニットとして計算ユニットを置き換えられている。1つのWGPには2つのCUが含まれる。これにより、単一のワークグループに、より多くの計算能力とメモリ帯域幅を割り当てることができる。RDNA 1では、CUはWGPの半分である。

## AMD RDNA 2

RDNA 1の後継であるRDNA 2(またRDNA2)マイクロアーキテクチャは2020年にリリースされる予定とされている。

RDNA 2の詳細は、2020年3月5日にAMDのFinancial Analyst Dayで公開されている。AMDは、RDNA 1よりもワットあたりのパフォーマンスが50％向上すると主張している。また、正確な値は提供されていないがクロック速度とクロックあたりの命令の増加している。AMDが確認した追加機能には、リアルタイムのハードウェアレイトレーシングと可変レートシェーディングが含まれる。

・第9世代のゲーム機での使用

  -
    RDNA 2は、今後独自の調整と異なる構成で第9世代のゲームコンソール（[Xbox seriesXおよび](../Page/Xbox_Series_X.md "wikilink")[PlayStation5](https://ja.wikipedia.org/wiki/PlayStation_5 "wikilink")）に使用されるグラフィックマイクロアーキテクチャとして確認されている。

## 外部リンク

  - [RDNAアーキテクチャー](https://www.amd.com/ja/technologies/rdna) - AMD

[Category:コンピュータアーキテクチャ](https://ja.wikipedia.org/wiki/Category:コンピュータアーキテクチャ "wikilink") [Category:2019年の作品](https://ja.wikipedia.org/wiki/Category:2019年の作品 "wikilink")