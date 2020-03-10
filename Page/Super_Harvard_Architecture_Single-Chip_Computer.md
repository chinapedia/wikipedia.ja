> この記事は[Super Harvard Architecture Single-Chip Computer](https://ja.wikipedia.org/wiki/Super_Harvard_Architecture_Single-Chip_Computer)から翻訳されています。


**Super Harvard Architecture Single-Chip Computer** (**SHARC**)は、[アナログ・デバイセズ](https://ja.wikipedia.org/wiki/アナログ・デバイセズ "wikilink")のDSPで、高性能な[浮動小数点](https://ja.wikipedia.org/wiki/浮動小数点 "wikilink")と[固定小数点](https://ja.wikipedia.org/wiki/固定小数点 "wikilink")演算を特徴とする。 SHARCは、幅広い信号処理用途に利用されており、CPU 1個による砲弾の制御から、CPU 1000個によりOTHレーダーの信号処理用コンピューターまで用途が存在する。 SHARCは1994年1月ごろに設計された。

SHARCプロセッサーは、単位[消費電力](https://ja.wikipedia.org/wiki/消費電力 "wikilink")当たりの浮動小数点演算性能が良好であるため利用されている。

SHARCプロセッサーは、典型的には近隣のSHARCプロセッサーとシリアル接続されることで、 低コストで[SMPの代替として利用できるようになっている](../Page/対称型マルチプロセッシング.md "wikilink")。

## アーキテクチャー

SHARCは、[ハーバード・アーキテクチャ](../Page/ハーバード・アーキテクチャ.md "wikilink")ーの[ワードマシン](https://ja.wikipedia.org/wiki/ワードマシン "wikilink")の[VLIW](../Page/VLIW.md "wikilink")プロセッサーであり、 [オクテット](https://ja.wikipedia.org/wiki/オクテット "wikilink")ではなく32ビットワードを示すようにアドレスが振られているため、 8ビットや16ビットの値を扱うことはできない。 64ビットのデータを扱ったり、8ビットや16ビットのデータを1つの32ビットのワードに 詰め込んだりする時に、コンパイラーはリトルエンディアンやビッグエンディアンをルールとして 利用することはあるが、SHARC CPU自体はリトルエンディアンでもビッグエンディアンでもない。 アナログ・デバイセズは、問題を避けるため自社のCコンパイラーで32ビットcharを使うのを避けている。

ワードサイズは命令については[48ビット](https://ja.wikipedia.org/wiki/48ビット "wikilink")であり、整数と普通の浮動小数点数については[32ビット](../Page/32ビット.md "wikilink")、 拡張された浮動小数点数については40ビットである。 コードとデータは通常はチップ上のメモリーからフェッチされる。 つまりユーザーは求められるワードサイズに合わせて領域を分割しておく必要がある。 短いデータタイプであっても長いメモリーに保持されるため、このような利用をすると、 領域の利用には無駄が生まれる。 40ビットの拡張された浮動小数点数を利用しないシステムでは、チップ上のメモリーを コード用の48ビット領域とそれ以外のための32ビット領域に分割する。 ほとんどのメモリーに関連するCPUの命令は、48ビットメモリーの全てのビットにアクセスすることが できない。 しかし特別な48ビットレジスターを利用すれば、48ビットメモリー内のビットにアクセスする ことができる。 この特別な48ビットレジスターは、より短いレジスターとして扱うことができ、これにより 通常のレジスターとの間でデータをやり取りできる。

チップ外部のメモリーにもアクセスすることが可能である。 この外部メモリーは1つのサイズのワード用に1つの領域を設定することしかできない。 メモリーの消費を抑えるために32ビットワード用に外部メモリーを設定すると、 チップ内のメモリーにコード用と拡張された浮動小数点数のための領域を設定しなくては いけなくなる。 こうなると、オペレーティングシステムは[オーバーレイを使って](../Page/オーバーレイ_\(コンピュータ用語\).md "wikilink")48ビットのデータを 命令の実行に応じてチップ内のメモリーに転送することで対応することとなる。 [DMAエンジンがこのために用いられる](../Page/Direct_Memory_Access.md "wikilink")。 真のページングは、外部の[MMUなしには実現不可能である](../Page/メモリ管理ユニット.md "wikilink")。

SHARCは32ビットのワード単位でのアドレス空間を持ち、ワードサイズに応じて16GB、 20GB、24GBがそれぞれ上限となる。

SHARCの命令は、32ビットの即値をオペランドとしてとることができる。 32ビットの即値をオペランドとしてとらない命令は2つ以上同時に実行可能である。 多くの命令は条件節を伴い、[アセンブリー言語](https://ja.wikipedia.org/wiki/アセンブリー言語 "wikilink")では「if 条件」を前に付けて表現する。 条件には多くの選択肢があり、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")におけるフラグレジスターのように使うことができる。

2つの[遅延スロット](https://ja.wikipedia.org/wiki/遅延スロット "wikilink")があり、ジャンプの後にはそのジャンプに続く2つの命令が実行されるのが 通常である。

SHARCプロセッサーはループ制御機能を持っている。 最大6段階まであれば、ループを終了させるか判断するために、通常のブランチ命令と 状態変数を利用する必要はない。

SHARCは2セットのレジスターを持っている。 コードにより、この2つの間をすぐに切り替えることができる。 これによりアプリケーションと[OSや](https://ja.wikipedia.org/wiki/オペレーティング・システム "wikilink")、2つのスレッド間でのコンテクストスイッチを高速に実行できる。

## 関連項目

  - [TigerSHARC](https://ja.wikipedia.org/wiki/TigerSHARC "wikilink")
  - [Blackfin](https://ja.wikipedia.org/wiki/Blackfin "wikilink")
  - [Qualcomm Hexagon](https://ja.wikipedia.org/wiki/Qualcomm_Hexagon "wikilink")
  - [Texas Instruments TMS320](https://ja.wikipedia.org/wiki/Texas_Instruments_TMS320 "wikilink")
  - [CEVA, Inc.](https://ja.wikipedia.org/wiki/CEVA,_Inc. "wikilink")

## 外部リンク

  - [SHARCプロセッサーウェブサイト](http://www.analog.com/en/processors-dsp/sharc/products/index.html)

[Category:デジタル信号処理](https://ja.wikipedia.org/wiki/Category:デジタル信号処理 "wikilink") [Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")