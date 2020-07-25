> この記事は[3DNow!](https://ja.wikipedia.org/wiki/3DNow!)から翻訳されています。


**3DNow\!**（スリーディー・ナウ）は、[アドバンスト・マイクロ・デバイセズ](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") (AMD) が[ドルビーデジタル](../Page/ドルビーデジタル.md "wikilink")の[デコード](https://ja.wikipedia.org/wiki/デコード "wikilink")や[3D処理の高速化を目的に開発した](../Page/3次元コンピュータグラフィックス.md "wikilink")、[CPU](../Page/CPU.md "wikilink")の[SIMD](../Page/SIMD.md "wikilink")拡張命令、およびその拡張版の総称である。

## 概要

[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[MMX](../Page/MMX.md "wikilink")では[整数](../Page/整数.md "wikilink")演算のみをサポートし、[浮動小数点演算には未対応であった](../Page/浮動小数点数.md "wikilink")。3DNow\!は、MMXに21個の[命令を追加することで浮動小数点演算の高速化を図ったものである](../Page/命令_\(コンピュータ\).md "wikilink")\[1\]\[2\]。

具体的には[64ビット](../Page/64ビット.md "wikilink")MMX[レジスタに](../Page/レジスタ_\(コンピュータ\).md "wikilink")[32ビット](../Page/32ビット.md "wikilink")の浮動小数点演算データを2個格納し、それぞれを独立して演算出来るようにしている。3DNow\!ではさらに2個のMMXユニットが並列動作可能であるため、最大4個の浮動小数点演算が可能となる。

3DNow\!は同社のCPU・[K6-2](../Page/AMD_K6-2.md "wikilink")\[3\]、[IDT](../Page/IDT.md "wikilink")の[WinChip 2](https://ja.wikipedia.org/wiki/WinChip#WinChip_2 "wikilink")\[4\]から搭載され始めた。開発当初はAMD、[サイリックス](../Page/サイリックス.md "wikilink")、IDT共に各社別々の仕様を発表していたが、AMDの働きかけにより、三社とも3DNow\!を採用することとなった。

しかし競合製品であるインテル製CPUがサポートする[SSE命令に対して](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE "wikilink")、登場は約1年早かったものの普及で後れを取ったため、[Enhanced 3DNow\!](https://ja.wikipedia.org/wiki/#Enhanced_3DNow! "wikilink")、[3DNow\! Professionalと世代が進むごとにSSEと互換性のある命令が追加されることとなった](https://ja.wikipedia.org/wiki/#3DNow!_Professional "wikilink")。

2010年8月、AMDは[Bobcat以降の世代のプロセッサーでは](https://ja.wikipedia.org/wiki/Bobcat_\(マイクロアーキテクチャ\) "wikilink")「3DNow\!」と「3DNow\!+」は2つの命令 (PREFETCH, PREFETCHW) を除いてサポートされないと発表\[5\]。3DNow\!の展開は終了した。

## Enhanced 3DNow\!

**エンハンスト3DNow\! テクノロジ** () は、3DNow\!に24個の命令を追加したものである\[6\]\[7\]。[Athlon](../Page/Athlon.md "wikilink") (K7) から搭載され始めた。一部の[K6-2や](../Page/AMD_K6-2.md "wikilink")[K6-IIIにも搭載されている](../Page/AMD_K6-III.md "wikilink")。

Enhanced 3DNow\!は、「3DNow\!+」 と「MMX+」の2つから構成される。

  - 「3DNow\!+」は、[サウンド](../Page/音源.md "wikilink")・[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")制御用[DSP命令](../Page/デジタル信号処理.md "wikilink")5個である。
  - 「MMX+」の実体は、SSE（初代）で追加されたMMX命令19個である\[8\]。

## 3DNow\! Professional

**3DNow\! プロフェッショナル・テクノロジ** () は、エンハンスト3DNow\!に52個の命令を追加し、インテルのSSEとの[互換性](../Page/互換性.md "wikilink")を持たせた物である\[9\]。同社の[Athlon XP](https://ja.wikipedia.org/wiki/Athlon#Athlon_XP "wikilink")、[モバイルAthlon 4](https://ja.wikipedia.org/wiki/Athlon#モバイルAthlon_4 "wikilink")、[Duron](../Page/Duron.md "wikilink")（Morganコア）から搭載され始めた。

SSEと同じく古い[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")では使用することができず、オペレーティングシステムによって、CR4レジスタのOSFXSRビットを1にすることにより使用することができる。

## 脚注

<references />

## 関連項目

  - [SIMD](../Page/SIMD.md "wikilink")
  - [ストリーミングSIMD拡張命令](../Page/ストリーミングSIMD拡張命令.md "wikilink") (SSE)
  - [AltiVec](../Page/AltiVec.md "wikilink") (Velocity Engine)
  - [PowerNow\!](../Page/PowerNow!.md "wikilink")

[Category:SIMDコンピューティング](https://ja.wikipedia.org/wiki/Category:SIMDコンピューティング "wikilink") [Category:X86アーキテクチャ](https://ja.wikipedia.org/wiki/Category:X86アーキテクチャ "wikilink") [Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink") [Category:アドバンスト・マイクロ・デバイセズ](https://ja.wikipedia.org/wiki/Category:アドバンスト・マイクロ・デバイセズ "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.  SSEでは、XMMレジスタを操作する命令に加えて、MMXレジスタを操作する整数演算命令も追加している。
9.