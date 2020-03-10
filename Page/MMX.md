> この記事は[MMX](https://ja.wikipedia.org/wiki/MMX)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Intel_Pentium_MMX_166_PGA_Front.jpg "wikilink"))\]\] **MMX**は、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が同社の[Pentiumプロセッサ向けに開発した](../Page/Intel_Pentium_\(1993年\).md "wikilink")[SIMD](../Page/SIMD.md "wikilink")型拡張命令セットである。56個の[命令を含む](../Page/命令_\(コンピュータ\).md "wikilink")。MMXは、MultiMedia eXtensions の略であるとの説があったが、インテルは、略語ではない一つの語であるとしている。

## 概要

MMXは、[x87](https://ja.wikipedia.org/wiki/x87 "wikilink")[FPU](../Page/FPU.md "wikilink")の[レジスタを転用し](../Page/レジスタ_\(コンピュータ\).md "wikilink")、1つの命令で同時に複数の整数演算を扱う[SIMD](../Page/SIMD.md "wikilink")型命令拡張である。MMXレジスタはFPUレジスタを共有するため、浮動小数点演算命令とは排他的に使用しなければならない。[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")がプロセスのコンテキストを保存する際には、MMX命令を使用するプロセスはFPU命令を使用しているものと同様に見え、同様にレジスタを保存すれば良い。DSPの得意分野である[音声](https://ja.wikipedia.org/wiki/音声 "wikilink")、[画像](../Page/画像.md "wikilink")、[動画](../Page/動画.md "wikilink")などの[マルチメディア](../Page/マルチメディア.md "wikilink")関係の処理を、CPUで扱う際の性能向上が期待されたが、[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")側がMMXを用いるようにプログラムされていなければ、MMXによる性能向上の恩恵は受けられない。

後に、専用のレジスタを使う[SSE命令セットが拡張され](../Page/ストリーミングSIMD拡張命令.md "wikilink")、より複雑なデータ処理や浮動小数点の演算にも対応。実質的にMMXは不要となったため、インテルではアプリケーション開発の最適化にあたってMMXの使用を避ける事を推奨している。SSE命令搭載以降、命令の種類や処理能力で劣るMMX命令は、主に過去の資産との互換性のみを目的に実装・提供されている。

インテルはまず、すでにリリースしていた[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")の新バージョン (開発コードネーム *[P55C](https://ja.wikipedia.org/wiki/Pentium#第三世代 "wikilink")*) にMMXを搭載、**Pentium Processor with MMX Technology**と称して発売。一般には**MMX Pentium**という呼称で浸透した。インテルは、これ以降に発売した[IA-32](../Page/IA-32.md "wikilink")アーキテクチャのプロセッサの多くに、MMXを搭載している。また、他のメーカーのIA-32互換プロセッサのいくつかにも搭載されている。例えば、[AMDの](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[K6などである](../Page/AMD_K6.md "wikilink")。インテルは他社がMMXという名称を使用していることに対し、これを停止するよう求め訴訟に発展したが、最終的には各社間で和解した。

## 性能と限界

MMXは元々、一般的なアプリケーションにおいて常用される事の少ない浮動小数点演算のレジスタの有効利用の観点から発想された。x87命令とMMX命令とを混在させる場合、最初のMMX命令の実行時に必要な初期化が自動で行われるが、その後でまたx87命令を実行する場合、その前にEMMS命令を実行して状態をクリアする必要がある。EMMS命令はPentiumでは数十サイクルを要した。それぞれの実行における、レジスタの状態は維持や保存はされない。他方、新たに専用レジスタを増やさず既存のx87のレジスタを流用したため、[コンテキストスイッチ](https://ja.wikipedia.org/wiki/コンテキストスイッチ "wikilink")毎の新設レジスタのセーブなどの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")のサポートを待つ必要はなかった。

また、MMXによって高速化できるのは整数演算処理に限られ、浮動小数点演算処理を多用する[3Dグラフィックス関連の処理能力の向上は期待できない](../Page/3次元コンピュータグラフィックス.md "wikilink")。インテルと競合するAMDは、先んじて浮動小数点演算も扱えるSIMD拡張命令セット[3DNow\!](../Page/3DNow!.md "wikilink")を発表し、同社の[K6-2](https://ja.wikipedia.org/wiki/K6-2 "wikilink")プロセッサに搭載。インテルはAMDより浮動小数点用のSIMD命令セットの提供に遅れをとった。インテルの浮動小数点SIMD演算による高速化は[Pentium III以降に搭載される](../Page/Pentium_III.md "wikilink")[SSEを待つこととなる](../Page/ストリーミングSIMD拡張命令.md "wikilink")。

## 歴史

  - [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink") [1月](https://ja.wikipedia.org/wiki/1月 "wikilink"): インテルが[MMX Pentiumを発表](https://ja.wikipedia.org/wiki/Pentium#第三世代 "wikilink")\[1\]。
  - [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink") [4月](https://ja.wikipedia.org/wiki/4月 "wikilink"): AMDがMMXに対応した[K6プロセッサを発表](../Page/AMD_K6.md "wikilink")。
  - [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink") [5月](https://ja.wikipedia.org/wiki/5月 "wikilink"): インテルが[Pentium ProにMMXを付加し高速化した](../Page/Pentium_Pro.md "wikilink")[Pentium IIプロセッサを発表](../Page/Pentium_II.md "wikilink")。

<!-- end list -->

  - 対抗（競合）機能登場

:\* [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink") [5月](https://ja.wikipedia.org/wiki/5月 "wikilink"): AMDが浮動小数点演算処理を高速化する[3DNow\!](../Page/3DNow!.md "wikilink")搭載の[K6-2プロセッサを発表](../Page/AMD_K6-2.md "wikilink")。

  - 自社による後継機能発表

:\* [1999年](../Page/1999年.md "wikilink") [2月](https://ja.wikipedia.org/wiki/2月 "wikilink"): インテルが浮動小数点演算処理を高速化する[ストリーミングSIMD拡張命令](../Page/ストリーミングSIMD拡張命令.md "wikilink") (SSE) 搭載の[Pentium IIIプロセッサを発表](../Page/Pentium_III.md "wikilink")。

## 脚注

## 関連項目

  - [SIMD](../Page/SIMD.md "wikilink")
  - [ストリーミングSIMD拡張命令](../Page/ストリーミングSIMD拡張命令.md "wikilink") (SSE)
  - [3DNow\!](../Page/3DNow!.md "wikilink")
  - [AltiVec](../Page/AltiVec.md "wikilink") (Velocity Engine)
  - [:en:Visual Instruction Set](https://ja.wikipedia.org/wiki/:en:Visual_Instruction_Set "wikilink")

[Category:CPU](https://ja.wikipedia.org/wiki/Category:CPU "wikilink") [Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink") [Category:X86アーキテクチャ](https://ja.wikipedia.org/wiki/Category:X86アーキテクチャ "wikilink")

1.