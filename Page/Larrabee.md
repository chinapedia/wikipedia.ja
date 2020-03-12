> この記事は[Larrabee](https://ja.wikipedia.org/wiki/Larrabee)から翻訳されています。


**Larrabee**（ララビー）は、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が社内用のソフトウェア開発プラットフォームとして開発中の半導体製品の社内[コードである](../Page/コードネーム.md "wikilink")。これはインテルが進めている[メニイコア戦略による次世代CPU製品](https://ja.wikipedia.org/wiki/マルチコア#プロセッサ例 "wikilink")、または汎用処理能力の高い[GPU製品として開発を進めていたものであったが](../Page/Graphics_Processing_Unit.md "wikilink")、グラフィック用半導体製品として販売される予定は当面なくなった。

## 位置付け

Larrabeeは、従来型のGPU製品のようにグラフィック処理用の[命令セット](../Page/命令セット.md "wikilink")を単純で専門化された[プログラマブルシェーダ](https://ja.wikipedia.org/wiki/プログラマブルシェーダ "wikilink")で固定的なパイプラインにより実行する代わりに、LRBni (Larrabee New Instruction, LNI) と呼ばれる100以上の新規命令で拡張された[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")命令セットを実行する16個、又はそれ以上のCPUコアを1つのダイ上にまとめて持つ製品となる予定であった\[1\]。

グラフィック処理に専門化されたGPUのアーキテクチャでは、プログラム実行を細かく指示するホスト役のCPUが必要になり、処理データの受渡しにまで実行時間を割り当てる必要があるが、x86命令を備えたLarrabeeではホスト役も含めて処理が行えるため、処理データの移動が基本的に避けられる。グラフィック処理だけでなく広範なデータ並列処理の用途に向けてGPUから派生した[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")も、Larrabeeと似た位置付けにあるが、Larrabeeがスカラー演算部を得意とする汎用演算用のIA CPUにSIMD型演算機能を取り込んだのに対して、GPGPUはGPUのプログラマブルシェーダやキャッシュ機構の改良による汎用演算性能の強化が進められているという違いがある\[2\]。

本半導体が製品として登場していれば、インテルの主流CPUである"Core 2"や"Core i7"といった従来型のIA CPUファミリと、GPUとの中間領域、又は両者を兼ねたものとして使用される予定であった。[ストリーム・プロセッシング](https://ja.wikipedia.org/wiki/ストリーム・プロセッシング "wikilink")を行う多様な用途、例えば物理シミュレーションによる3Dゲームや高解像度動画像処理、HPCサーバなどでの使用が対象となる\[3\]\[4\]\[5\]。

この半導体は2009年末現在で見れば、GPU製品である[NVIDIA](../Page/NVIDIA.md "wikilink")の[GeForce](https://ja.wikipedia.org/wiki/GeForce "wikilink")シリーズや、[AMDの](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[RADEON](https://ja.wikipedia.org/wiki/RADEON "wikilink")シリーズなどの製品市場で競合する予定だった。また近い将来は[AMD Fusionとも競合する可能性があった](https://ja.wikipedia.org/wiki/AMD_Fusion "wikilink")。

[2006年](../Page/2006年.md "wikilink")12月の[インテル・デベロッパー・フォーラム](https://ja.wikipedia.org/wiki/インテル・デベロッパー・フォーラム "wikilink")によれば、Larrabeeは1.7 - 2.5 GHzで動作し、16 - 24のインオーダー実行コアで修正されたx86命令セット、および[テクスチャ処理ユニットと](../Page/テクスチャマッピング.md "wikilink")、グラフィック向けの典型的な[ハードウェア](../Page/ハードウェア.md "wikilink")処理が実行されるとされた \[6\]。 [Ars TechnicaのJon](https://ja.wikipedia.org/wiki/Ars_Technica "wikilink") StokesはLarrabeeの[マイクロアーキテクチャ](../Page/マイクロアーキテクチャ.md "wikilink")は[Pentium MMXをベースとしているだろうと示唆している](https://ja.wikipedia.org/wiki/Pentium_MMX "wikilink")\[7\]。 Larrabeeはインテルの技術研究プロジェクトである「テラスケール・コンピューテング研究計画」(Intel's Tera-scale Computing Research Program) の研究成果が使用されている。インテルはテラスケール・コンピューテング研究で、Larrabeeを含む並列演算処理のプログラム記述用に[C言語](../Page/C言語.md "wikilink")を拡張した"Ct"言語も開発している。またCやC++もLarrabee用に拡張している。\[8\]\[9\]。

## 製品化予定とその見直し

インテルは2007年の段階ではLarrabeeの製品化を2009年後半または2010年としていた\[10\]。

2009年9月23日、IDF 2009にて試作カードによる実機デモが行われた。6＋8の補助電源で動作し2スロットクーラーを搭載していた。

2009年12月8日、開発の遅延と満足なパフォーマンスを得られなかったことから、2009年12月までにGPUとしての開発は中止され、2010年にソフトウェア開発プラットフォームとしてリリースする予定とされている\[11\]。

## 内部構成

[Larrabee_block_diagram_(Total_pic._and_CPU_core_bloack).PNG](https://ja.wikipedia.org/wiki/File:Larrabee_block_diagram_\(Total_pic._and_CPU_core_bloack\).PNG "fig:Larrabee_block_diagram_(Total_pic._and_CPU_core_bloack).PNG") 第1世代のLarrabee製品の構成として伝えられているものを以下に示す。

  - リング・ネットワーク

16個のCPUコア・ブロックや周辺回路がダイ内の高速双方向リング・ネットワークで結ばれ、データの外部とのやり取りや、レベル2キャッシュの[コヒーレント制御を行うのに使用される](../Page/コヒーレンス.md "wikilink")。それぞれ片方向で512ビット幅の転送路を持つ。隣接ユニットとの転送は2クロックごとに行われる。

  - CPUコア・ブロック

[ペンティアムP](../Page/Intel_Pentium_\(1993年\).md "wikilink")54C相当の2命令同時発行可能なインオーダー実行型のスカラー演算部に加え、「ベクタユニット」と呼ばれる16個の並列演算処理部を持ち、単一の命令処理によるホモジニアスCPUコア\[12\]を構成している。このスカラーとベクターの演算部に加えローカルで命令用32KBとデータ用32KBの合計64KBのレベル1キャッシュと、256KBのレベル2キャッシュを持つ。命令用とデータ用のレベル1キャッシュは1つのスレッドごとに16KBが割り当てられ、4wayのマルチスレッドに対応するのでそれぞれの合計が64KBとなる。命令キャッシュからインオーダー実行によるインストラクション・デコーダ部へ命令は伝えられ、内部的には2つのスカラー演算部と16wideが同時処理を行うSIMD型ベクター演算部が制御される。

ベクター演算用のレジスタは1つのスレッドごとに32ビットの16個で合計512ビット長のもの32本分にアクセス可能であり、4wayのマルチスレッドの対応する合計128本分を持っている。

レベル1キャッシュもレベル2キャッシュも共にプリフェッチ可能である。

リング・ネットワーク・インターフェース部が外部メモリや他のコアとの連絡を行う。

これらが1つのCPUコア・ブロックを構成している。

  - フィックスド・ファンクション・ロジック

テクスチャー・フィルターを備える。テクスチャー・フィルターはレベル2キャッシュを経由して入出力を行う。

  - 入出力インターフェース

外部との入出力にはシステム・インターフェース部とディスプレイ・インターフェース部を持つ。

## 命令セット

Larrabee用命令セットは、ペンティアム (P54C) 世代の完全なx86命令セットに加えて、32ビット整数演算、32ビットと64ビットの浮動小数点演算や、ビットカウント、ビットスキャン、キャッシュ制御といった100種類以上の新たな命令が加わった\[13\]。

## 「MIC」へ継承

インテル副社長の1人であり、"Intel Labs"を統括しているJustin Rattner氏は、2011年9月13日から3日間開かれている"IDF 2011"（インテル・デベロッパー・フォーラム 2011）の初日のキーノートスピーチにおいて、社内で"MIC"（Many Integrated Core、マイク）と呼んでいる新たなアーキテクチャに基づく、"Knights Ferry"（ナイツフェリー）メニーコアCPU、チップ自体のコードネームは"Aubrey Isle"と呼んでいる32個のコアを集積したメニーコア半導体をすでに一部の研究者向けに提供していると公表した。このMICアーキテクチャは、XEON系などインテルの通常のCPUと組み合わせたヘテロジニアス（異種混合）構成で使うことを前提としたコプロセッサであるとしている。MICアーキテクチャは、Larrabee用として開発された"LRBni" (Larrabee New Instruction, LNI) と呼ばれる100以上の新規命令で拡張されたx86命令セットを実装しており、512-bit幅のベクタ実行パイプラインを備えたコアを従来のx86系のプログラムで制御可能にしている\[14\]。

また、"Knights Ferry"での経験を活かしたMICアーキテクチャの正式製品([Xeon Phi](https://ja.wikipedia.org/wiki/Xeon_Phi "wikilink"))として、チップ自体は22nmプロセスを用いた"Aubrey Isle"と呼ばれるコア50個以上を集積する"Knights Corner"（ナイツコーナー）の製造を計画していると公表した\[15\]。

## 脚注

### 注釈

### 出典

## 関連項目

  - [AMD Fusion](https://ja.wikipedia.org/wiki/AMD_Fusion "wikilink")
  - [CUDA](../Page/CUDA.md "wikilink")
  - [Xeon Phi](https://ja.wikipedia.org/wiki/Xeon_Phi "wikilink")

[Category:インテル](https://ja.wikipedia.org/wiki/Category:インテル "wikilink")

1.  それぞれのCPUコアはインストラクション・デコーダを共有する[SIMD](../Page/SIMD.md "wikilink")型ベクトル演算部とスカラー演算部、それにレベル1とレベル2のキャッシュを持つ。
2.  <http://download.intel.com/technology/architecture-silicon/Siggraph_Larrabee_paper.pdf> Intek.com "Larrabee: Next-Generation Visual Computing Microarchitecture"
3.  インテル社ではLarrabeeを画像処理や科学技術計算だけでなく一般アプリケーションやマンマシンインターフェイスの向上に使用したいと考えている、または、考えていた。
4.
5.  インテル社は[MMX](../Page/MMX.md "wikilink")で64ビットでのSIMD命令拡張セットを追加して以来、[SSEで](../Page/ストリーミングSIMD拡張命令.md "wikilink")128ビットを行い、2010年に予定されているAVX (Advanced Vector Extensions) で256ビットまで拡張する流れの1つとも考えられる。
6.
7.
8.
9.  インテルは[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")第2[四半期](https://ja.wikipedia.org/wiki/四半期 "wikilink")だけで研究開発費用に14億7,000万米ドルを投資した。この金額はライバルであるAMDの同四半期における売上高を超えるものであった。
10.
11.
12. ホモジニアス (Homogeneous) の反対は、ヘテロジニアス (Heterogeneous) である。マルチプロセッサの多くがホモジニアス型プロセッサであり、すべて同質、又はほぼ同質のプロセッサを複数並べて、それぞれに命令コードを与えて個別に実行させるものであるヘテロジニアス型プロセッサとは、複数種の異なるアークテクチャのプロセッサをつないで、1つのプロセッサ複合体にしたものであり、異種のプロセッサが協調して動作するようになっている。ベクター演算プロセッサに制御用のスカラー演算プロセッサが付けられて、結果としてヘテロジニアス型となるコンピュータ・システムの構成は多いが、1つ又は数個程度のダイで実現されるヘテロジニアス型のプロセッサはそれほど多くはない。Larrabeeに似た位置付けのヘテロジニアス型のプロセッサに、[ソニー](../Page/ソニー.md "wikilink")の[Cell Broadband EngineとAMDが開発中の](../Page/Cell_Broadband_Engine.md "wikilink")[Fusionがある](https://ja.wikipedia.org/wiki/AMD_Fusion "wikilink")。Larrabeeは、ベクター演算までこなすホモジニアス型CPUである点で他とは異なる。
13. インテルでは、2010年から登場予定の主流CPUファミリの新製品（おそらく"Sandy Bridge"）によりAVX拡張命令セットを付加することで256ビット幅のベクタ演算をサポートする予定である。開発予定が変更されたLarrabeeの拡張命令セットである512ビット幅のベクタ演算も合わせれば、マルチコアとメニーコアの動きと平行してベクタ演算能力も大きく強化されることになったが、当面の製品では256ビット幅止まりとなる。
14. 主に整数系演算を担うスカラ演算パイプラインは、Larrabeeが用いた2命令実行可能な中規模／中性能なPentium系P54Cから、MICアーキテクチャではより小規模／低性能なAtom系、またはそれに近いのものへ変更されているという分析・予想がある。
15. [IDF 2011レポート Justin Rattner氏キーノートスピーチ ～メニイコア時代が到来する](http://pc.watch.impress.co.jp/docs/news/event/20110920_478686.html) - PC Watch（2011年9月20日配信、2011年9月20日閲覧）