> この記事は[Cyrix Cx5x86](https://ja.wikipedia.org/wiki/Cyrix_Cx5x86)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Cyrix_5x86-100GP_G5F8543J_top.jpg "wikilink") **Cyrix Cx5x86**は[サイリックス](../Page/サイリックス.md "wikilink")が、[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")8月に発売した、[i486とのソケット互換性を備える](../Page/Intel486.md "wikilink")32ビット[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")互換[CPU](../Page/CPU.md "wikilink")である。[AMDが開発した](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[Am5x86](https://ja.wikipedia.org/wiki/Am5x86 "wikilink")と共にもっとも高速なi486互換CPUの1つとして知られる。

## 概要

[Cx486シリーズの後継](https://ja.wikipedia.org/wiki/Cyrix_Cx486 "wikilink")・上位機種として、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")[Pentium互換プロセッサである](../Page/Intel_Pentium_\(1993年\).md "wikilink")[Cyrix 6x86](https://ja.wikipedia.org/wiki/Cyrix_6x86 "wikilink")（開発コード名M1）のコアロジックのサブセットと486系プロセッサ用[フロントサイドバス](https://ja.wikipedia.org/wiki/フロントサイドバス "wikilink") (FSB) インターフェイスを組み合わせて開発された。

開発コード名はM1scで、外部FSBは32ビット幅であるが内部データバスは64ビット幅となっており、[命令パイプライン](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")技術や[スーパースケーラ](https://ja.wikipedia.org/wiki/スーパースケーラ "wikilink")、128エントリの分岐ターゲットバッファーによる[分岐予測](https://ja.wikipedia.org/wiki/分岐予測 "wikilink")といったPentiumをはじめとする第5世代のx86系プロセッサと同様のアーキテクチャを採用しており\[1\]、ユニファイドキャッシュによる1次キャッシュを16[KB内蔵する](https://ja.wikipedia.org/wiki/キロバイト "wikilink")。このアーキテクチャにより、6x86の約50%の[トランジスタ](../Page/トランジスタ.md "wikilink")数で80%の性能を実現した。

そのため、このCx5x86は100[MHz動作時にほとんどのアプリケーションで](https://ja.wikipedia.org/wiki/メガヘルツ "wikilink")75MHz動作のPentiumプロセッサよりも優れた性能を発揮し、古く安価な[486対応Socket](../Page/Intel486.md "wikilink") 3[マザーボード](https://ja.wikipedia.org/wiki/マザーボード "wikilink")\[2\]のアップグレードパスとして、CPUコア電圧の対応\[3\]や[BIOSレベルでの対応](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")、それにFSBの動作周波数などに一部制限があったものの、一定の成功を収めた。

このチップはi486の[命令セット](https://ja.wikipedia.org/wiki/命令セット "wikilink")をほぼ完全にサポートしていたが、Pentium固有命令への対応はごく限られていた。面白いことに、このCPUの性能を強化するいくつかの特徴は、故意に無効化されていた。これは、出荷前に修正されなかった[バグ](../Page/バグ.md "wikilink")による、潜在的な不安定性の恐れのためである\[4\]。本CPUを使った、[80386やi](../Page/Intel_80386.md "wikilink")486SXを搭載するマシン用の[CPUアクセラレータ](https://ja.wikipedia.org/wiki/CPUアクセラレータ "wikilink")も数社から発売された。

なお、同じような名称の[SGS トムソン](https://ja.wikipedia.org/wiki/STマイクロエレクトロニクス "wikilink")[ST5x86](https://ja.wikipedia.org/wiki/ST5x86 "wikilink")と[IBM](../Page/IBM.md "wikilink")[5x86Cは](https://ja.wikipedia.org/wiki/IBM_5x86C "wikilink")、[ファブレス](../Page/ファブレス.md "wikilink")であるサイリックスとの間でチップの製造委託契約を結んでいた両社が、契約条項に含まれていた自社ブランドでのチップ販売権により商標を変更して販売したものである\[5\]。

そのため、実質的には同一のものであったが、サイリックスが市場に投入しなかった75MHz版の入手性や、電圧条件などでわずかな違いがあった。

これに対し、同じ[Socket 3に対応していて同程度の性能を発揮し](https://ja.wikipedia.org/wiki/Socket_3 "wikilink")、しかも同じ年の終わりに発表された[AMD Am5x86とこのCx](https://ja.wikipedia.org/wiki/AMD_5x86 "wikilink")5x86 の設計を混同するべきでない。Am5x86は基本的には高速な486\[6\]であり、これらは本質的に全く異質なプロセッサである。

本チップのアーキテクチャを元に[MediaGX](https://ja.wikipedia.org/wiki/MediaGX "wikilink")が作られ、その後[Geode](https://ja.wikipedia.org/wiki/Geode "wikilink")が生まれて[ネットブック](https://ja.wikipedia.org/wiki/ネットブック "wikilink")や[シンクライアント](https://ja.wikipedia.org/wiki/シンクライアント "wikilink")で使われていることからも先進的なアーキテクチャだったことがうかがえる。

## 仕様

[300px](https://ja.wikipedia.org/wiki/ファイル:Cy5x86_arch.png "wikilink")

  - iDX4WB ピンアウト、 168ピンPGAあるいは208ピンQFP
  - [Socket 3](https://ja.wikipedia.org/wiki/Socket_3 "wikilink")
  - 0.65μm プロセス、200万トランジスタ
  - ダイサイズ 144mm<sup>2</sup>
  - 3.45 ボルト電源を使用
  - 16 [キロバイト](https://ja.wikipedia.org/wiki/キロバイト "wikilink") L1 ユニファイドキャッシュ
  - 25 MHz (25×4), 33 MHz (33×3) と 50 MHz (50×2) のフロントサイドバスをサポートする 100 MHz 版。
  - 40 MHz (40×3) と 33 MHz (33×4) のフロントサイドバスをサポートする 120/133 MHz 版。133 MHz 版は大変希少であったが、アップグレードキットの製作者は優先的に入手することができた。

## 脚注

## 外部リンク

  - [Comparative performance benchmarks](http://www.interwb.com/486bench.txt)
  - [Cyrix 5x86](http://www.pcguide.com/ref/cpu/fam/g4C5x86-c.html)
  - [Cyrix 5x86 Processor Brief](http://www.worldwide-web-design.com/5x-tb.html)
  - [Entry in 486 processors chart](http://users.erols.com/chare/486.htm)

<!-- end list -->

  - [Performance-enhancing utility to enable 5x86 "register bits"](http://www.simtel.net/pub/pd/50153.html)
  - [Information on write-back cache performance-enhancing utility from Evergreen Tech](http://homepage3.nifty.com/sandy55/PowerBoard/PowerBoard.html)(ページ中央の "Cyrix5x86" のセクションと "et9603.exe" のリンクを参照)

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")

1.  そればかりか、第6世代に当たるインテル[Pentium Proとの共通点さえ存在した](../Page/Pentium_Pro.md "wikilink")。ただし、PentiumやCx6x86とは異なり2本の演算パイプは実装されておらず、シンプルなイン・オーダー実行1演算パイプ構成となっている。
2.  [Pentium Overdrive](../Page/オーバードライブプロセッサ.md "wikilink") を除いて、Pentium系のCPUを使用できなかった。
3.  インテル製486系プロセッサが使用しない3.45[V駆動であるため](../Page/ボルト_\(単位\).md "wikilink")、この電圧をサポートしないマザーボードでは電圧変換アダプタを併用する必要がある。
4.  これらの無効化された特徴は、自由にダウンロードできるソフトウェアで有効にすることができた。外部リンクを参照。
5.  IBMは自社製パーソナルコンピュータ製品の一部について、サイリックスが設計し自社で製造したプロセッサを搭載して販売していた。
6.  サイリックス製品のように新しいアーキテクチャを採用した設計ではなく、従来の486コアの製造プロセスをシュリンクして高クロック動作可能とし、1次キャッシュを増量して性能向上をはかった。