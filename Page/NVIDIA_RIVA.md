> この記事は[NVIDIA RIVA](https://ja.wikipedia.org/wiki/NVIDIA_RIVA)から翻訳されています。


**RIVA**（リーヴァ）は米[NVIDIA](../Page/NVIDIA.md "wikilink")社のビデオチップ（[グラフィックアクセラレータ](../Page/グラフィックアクセラレータ.md "wikilink")）である。 1990年代後半の[NVIDIA](../Page/NVIDIA.md "wikilink")の成長を支えた。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Canopus_RIVA_TNT.png "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Canopus_RIVA_TNT2_Ultra.png "wikilink")

## 概要

1993年に設立されたNVIDIAは、3Dアクセラレーション機能をもつ**[NV1](https://ja.wikipedia.org/wiki/NV1 "wikilink")**を開発した。NV1は曲面描画エンジンを採用し、専用のソフトウェア製品では高い性能を発揮したものの、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")において多角形（[ポリゴン](../Page/ポリゴン.md "wikilink")）描画を仕様としたため、DirectXへの対応が不完全なNV1の売り上げは伸びなかった。

NVIDIAは、[Windows CEのカスタマイズ版が搭載された](https://ja.wikipedia.org/wiki/Windows_CE "wikilink")[セガ](https://ja.wikipedia.org/wiki/セガ "wikilink")の[ドリームキャスト](../Page/ドリームキャスト.md "wikilink")（1998年発売）に向けてNV1を元にした**[NV2](https://ja.wikipedia.org/wiki/:en:NV2 "wikilink")**を設計したが、曲面描画エンジンは、DirectXを利用してゲームタイトルを移植することが難しく、多角形描画が一般的になりつつあったことから途中で中止された。

この反省からNVIDIAは、多角形描画を採用しDirectXに対応、[Direct3D](../Page/Direct3D.md "wikilink")の性能を追求したビデオチップ**NV3**を開発し、1997年に**RIVA 128**として発表した。RIVA 128の描画品質はあまり良くなかったが、描画速度が非常に高速であり高解像度のディスプレイもサポートしていた。また、RIVA 128は低価格であり多くのOEMメーカーが搭載ボードを販売した。

1998年にNVIDIAは、RIVA 128の後継としてDirectX 6に対応し、マルチテクスチャリング処理が可能となった**RIVA TNT**（開発コード名はNV4）を発表した\[1\]。RIVA TNTは2本のピクセルパイプラインを持ち（製品名のTNTはTwiN Texelからとられた）、24ビットの[Zバッファ](../Page/Zバッファ.md "wikilink")を採用しており、描画品質も改善されている。また1999年には、RIVA TNTの後継として32ビットの[フレームバッファ](https://ja.wikipedia.org/wiki/フレームバッファ "wikilink")をもつ**RIVA TNT2**（開発コード名はNV5）を発表\[2\]、後に廉価版のRIVA TNT2 M64とRIVA TNT2 Vanta（ともに開発コード名はNV6）、チップセットにグラフィックコアを統合した[ALADDiN-TNT2なども販売された](https://ja.wikipedia.org/wiki/ALi "wikilink")。

[thumb](https://ja.wikipedia.org/wiki/ファイル:RIVA_128_NV_GPU.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:RIVA_128ZX_GPU.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:RIVA_TNT_GPU.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:RIVA_TNT2_Ultra_GPU.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:RIVA_TNT2_VANTA_GPU.jpg "wikilink")

## RIVA 128

| 製品名         | コア名 (製造プロセス) | トランジスタ数 | コアクロック | メモリクロック(バス幅)   | RAMDAC | VRAM      | インターフェイス                                                                                                                  | DirectX |
| ----------- | ------------ | ------- | ------ | -------------- | ------ | --------- | ------------------------------------------------------------------------------------------------------------------------- | ------- |
| RIVA 128    | NV3 (0.35μm) | 350万    | 100MHz | 100MHz(128bit) | 230MHz | SGRAM 4MB | [AGPまたは](../Page/Accelerated_Graphics_Port.md "wikilink")[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink")   | 5       |
| RIVA 128 ZX | NV3 (0.35μm) | 350万    | 100MHz | 100MHz(128bit) | 250MHz | SGRAM 8MB | [AGP](../Page/Accelerated_Graphics_Port.md "wikilink")2xまたは[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink") | 5       |

## RIVA TNT

| 製品名      | コア名 (製造プロセス)        | トランジスタ数 | コアクロック       | メモリクロック(バス幅)   | RAMDAC | VRAM       | インターフェイス                                                                                                                  | DirectX |
| -------- | ------------------- | ------- | ------------ | -------------- | ------ | ---------- | ------------------------------------------------------------------------------------------------------------------------- | ------- |
| RIVA TNT | NV4 (0.35μm/0.25μm) | 700万    | 90MHz/125MHz | 125MHz(128bit) | 250MHz | SDRAM 16MB | [AGP](../Page/Accelerated_Graphics_Port.md "wikilink")2xまたは[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink") | 6       |

## RIVA TNT2

| 製品名                | コア名 (製造プロセス) | トランジスタ数 | コアクロック | メモリクロック(バス幅)   | RAMDAC | VRAM       | インターフェイス                                                                                                                  | DirectX |
| ------------------ | ------------ | ------- | ------ | -------------- | ------ | ---------- | ------------------------------------------------------------------------------------------------------------------------- | ------- |
| RIVA TNT2 Ultra    | NV5 (0.25μm) | 1500万   | 150MHz | 183MHz(128bit) | 300MHz | SDRAM 32MB | [AGP](../Page/Accelerated_Graphics_Port.md "wikilink")2xまたは[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink") | 6       |
| RIVA TNT2 Pro      | NV5 (0.25μm) | 1500万   | 143MHz | 166MHz(128bit) | 300MHz | SDRAM 32MB | [AGP](../Page/Accelerated_Graphics_Port.md "wikilink")2xまたは[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink") | 6       |
| RIVA TNT2          | NV5 (0.25μm) | 1500万   | 125MHz | 150MHz(128bit) | 300MHz | SDRAM 32MB | [AGP](../Page/Accelerated_Graphics_Port.md "wikilink")2xまたは[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink") | 6       |
| RIVA TNT2 M64      | NV6 (0.25μm) | 1500万   | 125MHz | 135MHz(64bit)  | 300MHz | SDRAM 32MB | [AGP](../Page/Accelerated_Graphics_Port.md "wikilink")2xまたは[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink") | 6       |
| RIVA TNT2 Vanta    | NV6 (0.25μm) | 1500万   | 100MHz | 110MHz(64bit)  | 300MHz | SDRAM 32MB | [AGP](../Page/Accelerated_Graphics_Port.md "wikilink")2xまたは[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink") | 6       |
| RIVA TNT2 Vanta LT | NV6 (0.25μm) | 1500万   | 80MHz  | 100MHz(64bit)  | 300MHz | SDRAM 32MB | [AGP](../Page/Accelerated_Graphics_Port.md "wikilink")2xまたは[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink") | 6       |

## 脚注

## 関連項目

  - [NVIDIA](../Page/NVIDIA.md "wikilink")
  - [Geforce](https://ja.wikipedia.org/wiki/Geforce "wikilink")

## 外部リンク

  - [NVIDIA](http://www.nvidia.co.jp/)

[Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink") [Category:NVIDIA](https://ja.wikipedia.org/wiki/Category:NVIDIA "wikilink")

1.
2.