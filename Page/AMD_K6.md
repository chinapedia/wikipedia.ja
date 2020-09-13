> この記事は[AMD K6](https://ja.wikipedia.org/wiki/AMD_K6)から翻訳されています。


| AMD K6                           |
| -------------------------------- |
| 製造元                              |
| 種類                               |
| [周波数](../Page/周波数.md "wikilink") |
| FSB                              |
| 1次キャッシュ                          |
| 2次キャッシュ                          |
| 拡張命令                             |
| プロセス                             |
| トランジスタ数                          |
| プラットホーム                          |
| パッケージ                            |
| 製造期間                             |

**AMD K6**は[Advanced Micro Devices](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")（以下、AMD）が開発した[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")互換[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")である。

## 概要

[thumb](https://ja.wikipedia.org/wiki/ファイル:AMD_K6-166ALR.jpg "wikilink") K6はx86命令を内部でRISC86OPに変換し、内部のRISC86[パイプラインで命令を高速実行する](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")、[Socket 7互換](../Page/Socket_7.md "wikilink")[CPU](../Page/CPU.md "wikilink")である。

[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")製CPUとの[ソケット互換CPUとして](../Page/CPUソケット.md "wikilink")、同一ソケットで同一クロック動作のインテル純正CPUを凌駕する高性能を発揮するため、低価格パーソナルコンピュータ (PC) を中心に普及し、また既存PCのアップグレード用としても市場に受け入れられた。 製造時期によって使用半導体製造プロセスが異なり、これにより166MHz〜233MHzと、200〜300MHzの2モデルに分類される。

## 開発経緯

AMDは、x86互換プロセッサメーカーであった、Atiq Raza率いる[NexGen](https://ja.wikipedia.org/wiki/NexGen "wikilink")社を買収し、当時NexGenが開発中だったNx686というx86互換CPUを手に入れた。AMDがもともと開発していたK6は性能がこのNx686より劣るものであったため、Nx686を元に開発した新プロセッサをK6として、1997年に市場に投入した。

本来、Nx686は前作Nx586やIntelのPentium Proなどと同様に[2次キャッシュバスが](../Page/L2キャッシュ.md "wikilink")[フロントサイドバス](../Page/フロントサイドバス.md "wikilink")から独立した構成の、専用バス・専用ソケットに対応するCPUとして開発が進められていたが、AMDはそれをSocket7対応に変更し、2次キャッシュバス廃止に伴うペナルティ軽減を目的に1次キャッシュを増量（32+32=64KB）の上で、Nx686独自のマルチメディア命令をIntelからライセンスを受け[MMX](../Page/MMX.md "wikilink")命令セットに変更して完成させた。

このCPUは時期により様々な開発コードネームが用いられたが、その一つに「Catapult」があった。これは、この新CPUを強大な[ゴリアテ](../Page/ゴリアテ.md "wikilink")（=インテル）を打ち倒した[ダビデ](../Page/ダビデ.md "wikilink") (=AMD) の武器（[投石機](../Page/カタパルト_\(投石機\).md "wikilink")）になぞらえての命名であり、AMDが相当な自信と意気込みをもってこのCPUの開発に臨んだことを窺わせていた。

K6は上述の通りインテルの[Pentium](../Page/Intel_Pentium_\(1993年\).md "wikilink") (Socket 7) とソケット互換であり、出荷開始の段階でインテルのMMX Pentiumシリーズよりも高クロック（233MHz）動作モデルが提供され、発売当初は、x86系で最速クロック動作のCPUとなった。このため、AMDはK6を「インテル製品よりも高速な初めての互換プロセッサ」だとして大々的に売り出した。K6はその発売開始一か月後にインテルが販売開始した当時最速のインテル製プロセッサ[Pentium IIと競合する製品であったとAMDは宣伝していたが](../Page/Pentium_II.md "wikilink")、クロックあたりの命令実行効率ではPentium IIにやや劣っていた。発表から約1年後の1998年5月には、[SIMD](../Page/SIMD.md "wikilink")拡張命令セットである[3DNow\!](../Page/3DNow!.md "wikilink")を追加した[K6-2](https://ja.wikipedia.org/wiki/K6-2 "wikilink")という後継プロセッサが登場している。

Pentium IIでは、Socket 7ではなく、[Slot 1](../Page/Slot_1.md "wikilink") (P6バス) が採用されており、Socket 7ユーザーがPentium IIにアップグレードするには、[マザーボード](../Page/マザーボード.md "wikilink")ごと（そして多くの場合メモリも）交換しなければならなかった。これに対しK6はSocket 7を採用していたため、[ローエンド](https://ja.wikipedia.org/wiki/ローエンド "wikilink")向けPC用の[CPU](../Page/CPU.md "wikilink")として採用されたり、Socket 7ユーザーのアップグレード用[CPU](../Page/CPU.md "wikilink")としても使用された。

## 特徴

K6は次のような特徴を備えている。

  - 第6世代RISC86[スーパースケーラ](https://ja.wikipedia.org/wiki/スーパースケーラ "wikilink")・マイクロアーキテクチャ
  - 8192エントリー2レベル分岐予測
  - 16エントリーBTB
  - 最大2命令[デコード](https://ja.wikipedia.org/wiki/エンコード#デコード "wikilink")
  - [投機的実行](../Page/投機的実行.md "wikilink")
  - [レジスタ・リネーム](../Page/レジスタ・リネーミング.md "wikilink")
  - 24エントリー[リザベーションステーション](https://ja.wikipedia.org/wiki/リザベーションステーション "wikilink")
  - [アウト・オブ・オーダー実行](../Page/アウト・オブ・オーダー実行.md "wikilink")
  - 1クロックあたり最高6個(5個＋分岐1個)のRISC86命令実行

メモリから読み出された命令は、まずフェッチユニットが16バイト分のブロックを1次キャッシュからフェッチを行い、命令バッファで命令が切り出され、デコーダに送られる。デコーダは、単純命令を処理できるショート・デコーダが同時に2命令のデコードが可能である。その他ロング・デコーダとベクター・デコーダがあるが、これら3種類のデコーダはサイクルあたりで同時稼働できない。したがって、ピークのX86命令デコード・スループットは2命令ということになる。また、MMX命令は二つのショートデコーダのうち最初のショートデコーダでしかデコードできない仕様になっている。

デコーダはRISC86OPという内部命令に変換され、サイクルあたり最大4つのRISC86OPが出力可能である。この4つのRISC86OPがグループ化され（4つに満たない場合NOP命令で埋められる）、後段の24エントリーある[リザベーション・ステーション](https://ja.wikipedia.org/wiki/リザベーション・ステーション "wikilink")に送られる。

命令は、[リザベーション・ステーション](https://ja.wikipedia.org/wiki/リザベーション・ステーション "wikilink")から5命令、分岐予測ユニットから分岐命令が実行可能である、また内部に整数2つ、MMX1つ、FPU1つ、ロード1つ、ストア1つ、分岐1つの計7つの並列実行ユニットを備えている。MMX実行ユニットはレジスタXパイプラインにしか繋がっておらず、2つのMMX実行ユニットをもつ[MMX Pentiumおよび](https://ja.wikipedia.org/wiki/Intel_Pentium_\(1993年\)#第三世代 "wikilink")[Pentium IIにこの点で劣っている](../Page/Pentium_II.md "wikilink")。これはのちの[K6-2でMMX命令が](../Page/AMD_K6-2.md "wikilink")2命令実行できるように改良された。

また、K6は整数乗算を[パイプライン実行できず](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")、一方[K5はパイプライン実行を行えるため](../Page/AMD_K5.md "wikilink")、整数乗算命令のスループットは先代から大幅に低下している。

ただし、K6では[分岐予測](../Page/分岐予測.md "wikilink")や[投機実行の実装により](../Page/投機的実行.md "wikilink")[パイプラインを効率的に利用可能にするさまざまな機能がサポートされており](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")、K5では分岐先予測のバッファを保持していなかったのに対し、分岐先予測バッファとして16エントリーを保持するようになっている。

さらに、[レジスタリネーム機能もサポートされており](../Page/レジスタ・リネーミング.md "wikilink")、汎用レジスタ本数が少ないというx86系プロセッサの弱点を補っている。

## 各世代についての詳細

### K6 （Model 6）

  - プロセス：0.35マイクロメートル
  - トランジスタ：880万個
  - 一次キャッシュ：データ32KB,命令32KB
  - 拡張命令：MMX
  - バス：Socket7
  - FSB：66MHz
  - クロック：166／200／233MHz
  - 販売開始日：[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")4月2日
  - 電圧：2.9V（200Mhz以下）3.2／3.3V（233MHz）

### K6 "Little Foot" （Model 7）

  - プロセス：0.25マイクロメートル
  - トランジスタ：880万個
  - 一次キャッシュ：データ32KB,命令32KB
  - 拡張命令：MMX
  - バス：Socket7
  - FSB：66MHz
  - クロック：200／233／266／300MHz
  - 販売開始日：[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")1月6日
  - 電圧：2.2V

## 関連項目

  - [AMD K6-2](../Page/AMD_K6-2.md "wikilink")
  - [AMD K6-III](../Page/AMD_K6-III.md "wikilink")
  - [アドバンスト・マイクロ・デバイセズ](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")

## 外部リンク

  - [AMD-K6プロセッサデータシート](http://www17.tok2.com/home/taro/file/j20695h.pdf)
  - [モバイルAMD-K6製品情報](http://www.amd.com/jp-ja/Processors/ProductInformation/0,,30_118_1260_1262,00.html)

[Category:AMDのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:AMDのマイクロプロセッサ "wikilink")