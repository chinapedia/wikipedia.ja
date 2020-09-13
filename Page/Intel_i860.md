> この記事は[Intel i860](https://ja.wikipedia.org/wiki/Intel_i860)から翻訳されています。


**Intel i860**（または**80860**）は[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[RISC](../Page/RISC.md "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")であり、[1989年](../Page/1989年.md "wikilink")にリリースされた。i860(と[i960](../Page/Intel_i960.md "wikilink"))は、インテルにとって[1980年代](../Page/1980年代.md "wikilink")の[i432以来の完全に新しい](../Page/Intel_iAPX_432.md "wikilink")[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")[ISAについての試みであった](../Page/命令セット.md "wikilink")。i860は鳴り物入りで登場し、多くの人が設計が優れていると考えていた[i960のリリースを覆い隠したほどだったが](../Page/Intel_i960.md "wikilink")、i960が[組み込みシステム](../Page/組み込みシステム.md "wikilink")に活路を見出したのに対して、i860は商業的には全く成功せず、プロジェクトは[1990年代](../Page/1990年代.md "wikilink")中ごろに終結させられた。

[アンドルー・グローヴ](../Page/アンドルー・グローヴ.md "wikilink")はi860の市場での失敗の原因はインテルにあるとして、次のように述べている。

## 技術的特性

i860は当時ではユニークだったいくつかの特徴を備えている\[1\]。特に[VLIW](../Page/VLIW.md "wikilink")アーキテクチャと高速[浮動小数点数演算が挙げられる](../Page/FLOPS.md "wikilink")。ひとつの[32ビット](../Page/32ビット.md "wikilink")[ALUとひとつの](https://ja.wikipedia.org/wiki/演算論理装置 "wikilink")[64ビット](../Page/64ビット.md "wikilink")[FPU](../Page/FPU.md "wikilink")を備えており、[FPU](../Page/FPU.md "wikilink")は3つの部分(加算器、乗算器、グラフィックスプロセッサ)から成っている。ALUと乗算器、加算器に対してそれぞれ[命令パイプライン](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")を備えていて、最大3命令を1[クロック](../Page/クロック.md "wikilink")サイクルで実行することができる。

バスは64ビットかそれ以上であった。[キャッシュを結ぶ内部メモリ](../Page/キャッシュメモリ.md "wikilink")[バスは](../Page/バス_\(コンピュータ\).md "wikilink")[128ビット](https://ja.wikipedia.org/wiki/128ビット "wikilink")幅である。CPUもFPUも32本の32ビット[レジスタを持ち](../Page/レジスタ_\(コンピュータ\).md "wikilink")（うち１つは必ず0を返すゼロレジスタ）、それをFPUは16本の64ビットレジスタとして使った。ALUに対する命令は一度にふたつフェッチして外部バスをフルに使っている。このため、インテルはこのデザインを「i860 64ビット マイクロプロセッサ」と称した\[2\]。

i860の命令は8ビットから128ビットまでのデータサイズを扱うことができる\[3\]。

グラフィックスユニットをマイクロプロセッサチップに内蔵するのは当時としては珍しかった。これは基本的には[FPU](../Page/FPU.md "wikilink")レジスタを8本の128ビットレジスタとして使った64ビット整数演算ユニットである。様々な[SIMD](../Page/SIMD.md "wikilink")的な命令と基本的な64ビット整数演算機能を持っていた。このi860での経験が後の[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")プロセッサの[MMX](../Page/MMX.md "wikilink")機能に影響を与えた。

i860の非常にユニークな機能のひとつとして、各機能ユニットのパイプラインに対してプログラムからアクセス可能であったことが挙げられる。そのため、[コンパイラ](../Page/コンパイラ.md "wikilink")が注意深く命令を並べてパイプラインが満たされた状態にする必要があった。一般的なアーキテクチャではCPU上のスケジューラがその役割を担うが、初期のRISC設計ではシステムの複雑さが用途を限定してしまう。i860はこれを丸ごとチップからコンパイラへ移してしまった。これによりコアが単純になり、他の機能をチップに組み込むことができるようになるため、性能向上につながる。結果としてi860はグラフィックスと浮動小数点については高速に実行できたが、一般的な用途では満足できる性能を出すようなプログラムを書くのが困難だった（後述）。

## 性能 (問題)

紙上の性能はシングルチップとしては非常に印象的なものだったが、実際の性能は全く違っていた。何が問題なのか当時は不明だったが、実行時のコードの流れを予測することが難しかったためと思われる。つまり、コンパイル時に命令を正しく並べることが非常に困難だったのである。例えば、ふたつの数値の加算命令はその数値がキャッシュ上になければ非常に時間がかかる。しかし、プログラマにはその数値がキャッシュにあるかどうかは分からないのである。もし予想が外れれば、データを待つためにパイプラインが停止する。i860のデザインはこういったことをコンパイラが効果的に行うことを前提としていて、それは不可能だったことが実証されている。XP版では理論上[単精度](https://ja.wikipedia.org/wiki/単精度 "wikilink")でも[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink")でも60から80MFLOPS\[4\]の性能が見込まれたが、[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で書いたプログラムでもせいぜい40MFLOPSで、コンパイラを使うと10MFLOPSも難しかった。

もうひとつの重大な問題は[コンテキストスイッチ](../Page/コンテキストスイッチ.md "wikilink")を高速に行う手段がなかったことである。i860はいくつかのパイプラインを持っていて、[割り込みによってそれを壊すので](../Page/割り込み_\(コンピュータ\).md "wikilink")、復帰時に元に戻さなければならなかった。この処理には最低でも62クロックサイクルを要し、最悪の場合2,000クロックサイクルにもなった。これは[クロック周波数](https://ja.wikipedia.org/wiki/クロック周波数 "wikilink")40 MHzでは2万分の1秒（50μ秒）であり、CPUにとってはとてつもなく長い。このためi860は汎用CPUになれなかったのである。

## バージョンと実際の使用例

[300px](https://ja.wikipedia.org/wiki/ファイル:Paragon_Card.jpg "wikilink") [right](https://ja.wikipedia.org/wiki/ファイル:KL_Intel_i860XR.jpg "wikilink") このチップにはふたつのバージョンがあった。コードネームN10の**XR**とコードネームN11の**XP**である。XPには大きなキャッシュ、二次キャッシュ、より高速なバスと、[並列計算](../Page/並列計算.md "wikilink")のための[バススヌーピング](https://ja.wikipedia.org/wiki/バススヌーピング "wikilink")機能と[キャッシュ・コンシステンシ機能を持っていた](https://ja.wikipedia.org/wiki/キャッシュコヒーレンシ "wikilink")。XRは25 MHzか40 MHzであったが、XPはプロセスを縮小したため(1 μm→0.8 μm)40 MHzか50 MHzで動作。どちらも同じ命令セットが動作する。

まず、i860は[ロスアラモス国立研究所](../Page/ロスアラモス国立研究所.md "wikilink")ののようないくつかの大規模マシンで使われた。コンパイラが強化されたためi860の性能もそれなりに強化されたが、当時のi860の性能は他のRISCには及ばなかった。他には、i860XRを28個またはi860XPを14個搭載した[アライアント・コンピュータ](../Page/アライアント・コンピュータ.md "wikilink")のFX/2800シリーズがある。

インテルはi860を[ワークステーション](../Page/ワークステーション.md "wikilink")のCPUとして使えないか、[MIPSアーキテクチャ](../Page/MIPSアーキテクチャ.md "wikilink")のチップなどと対抗できないか試したことがある。[マイクロソフト](../Page/マイクロソフト.md "wikilink")は内部で設計したi860ベースのワークステーション（コードネームは *Dazzle*）で後に [Windows NT](../Page/Microsoft_Windows_NT.md "wikilink") と呼ばれるようになる[OSの開発を行っていたが](https://ja.wikipedia.org/wiki/オペレーションシステム "wikilink")、最終的に NT が実際に動作したのは[MIPSと](../Page/MIPSアーキテクチャ.md "wikilink") [Intel 386](../Page/Intel_80386.md "wikilink") で、その後他のプロセッサにも移植されたが i860 には移植されなかった。NTという名称は、i860XR のコード名が "N-Ten" だったことに由来するとも言われている\[5\]。

i860をメインCPUとして持つ[UNIX](../Page/UNIX.md "wikilink")ワークステーションも存在し、[沖電気](https://ja.wikipedia.org/wiki/沖電気 "wikilink")のOKI station 7300と、それをベースにグラフィックスサブシステムに2個のi860を搭載した[クボタコンピュータの](../Page/アーデントコンピュータ.md "wikilink") Titan VISTRA がある。

i860は[ワークステーション](../Page/ワークステーション.md "wikilink")市場で[グラフィックスアクセラレータ](https://ja.wikipedia.org/wiki/グラフィックスアクセラレータ "wikilink")として使われたりした。例えば[NeXT](../Page/NeXT.md "wikilink")Dimensionでも使われた。このマシンは[Mach](../Page/Mach.md "wikilink")の機能削減版が動作し、完全な[PostScript](../Page/PostScript.md "wikilink")スタックを実装していた。ただし、PostScript部分が完全に仕上げられることはなく、単に色[ピクセル](../Page/ピクセル.md "wikilink")を動かすぐらいしかできなかった。このような環境ではi860はかなりよく動作した。主なプログラムはキャッシュに収まるサイズで、完全に予測通りに動くようにコーディングできたからである。は同社のフレームバッファカード Targa と Vista と共に使うことを意図したi860ベースのアクセラレータカードを作り、[ピクサーがそれを使って動作するバージョンの](https://ja.wikipedia.org/wiki/ピクサー・アニメーション・スタジオ "wikilink")[RenderMan](../Page/RenderMan.md "wikilink")を開発。これは386ホストの4倍の性能を発揮した。他の採用例は、ジオメトリエンジン内に複数個のi860XPを使った [SGI](../Page/シリコングラフィックス.md "wikilink")  がある。このような使用法も徐々に減っていき、多くの汎用CPUがi860の性能に追いついて、インテルもPentiumを主力とするようになった。

はi860を[並列計算](../Page/並列計算.md "wikilink")機に採用した。型ネットワークで2個から360個の計算ノードを相互接続したもので、各ノードのローカルメモリに他ノードからもアクセスできる。ノード毎に異なるシステムを採用でき、i860の他に[PowerPC](../Page/PowerPC.md "wikilink")や [SHARC](../Page/Super_Harvard_Architecture_Single-Chip_Computer.md "wikilink") DSP を3個組合わせたノードがある。i860向けにアセンブリ言語で書かれた信号処理ライブラリを提供したため、よい性能が得られた。[19インチラック](../Page/19インチラック.md "wikilink") 9U の筐体に360個の計算ノードを詰め込めるため、軍用機上でのレーダー処理などに適していた。

また1990年代前半、[ストラタスがi](https://ja.wikipedia.org/wiki/ストラタステクノロジー "wikilink")860ベースの[無停止コンピュータ](https://ja.wikipedia.org/wiki/無停止コンピュータ "wikilink") XA/R シリーズを開発している\[6\]。

1990年代後半、インテルは[ARMベースの](../Page/ARMアーキテクチャ.md "wikilink")[XScaleでRISCビジネス全体を置き換えた](https://ja.wikipedia.org/wiki/Intel_XScale "wikilink")。また、インテルの[Xeon](../Page/Xeon.md "wikilink")システム用のマザーボードのチップセットとしてi860という名前が再利用されているため混乱を招くこともある。

## 脚注・出典

## 参考文献

  -
## 外部リンク

  - [i860の画像と解説](http://www.cpu-collection.de/?l0=co&l1=Intel&l2=i860) cpu-collection.de

[Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink")

1.
2.
3.  [i860 64-Bit Microprocessor THE ADVANCE INFORMATION 1989](http://smithsonianchips.si.edu/intel/i860.htm)
4.  Mega Floating point number Operations Per Second（メガフロップス）。1秒間に浮動小数点演算を100万回行うことを示す、処理性能を表す単位。
5.
6.  [Stratus Machine History](ftp://ftp.stratus.com/vos/doc/reference/machine_history.txt)