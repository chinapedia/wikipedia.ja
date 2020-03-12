> この記事は[Intel486](https://ja.wikipedia.org/wiki/Intel486)から翻訳されています。


**Intel486**（インテルよんはちろく）は、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")系[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")で、[386の後継製品である](../Page/Intel_80386.md "wikilink")。

当初の名称は「80486」で、後に廉価版の「486SX」をラインナップに追加した際に、従来の80486を「[486DX](../Page/Intel486_DX.md "wikilink")」と改名し、同時にそれらの総称として「**i486**」の[商標](../Page/商標.md "wikilink")を使うようになった。"i" を付けたのは、米国では番号だけの名前は商標権を取れない（登録できない）ためである。インテルが現在使用している名称は**Intel486プロセッサ** (Intel486 Processor) である。

## 概要

[thumb](https://ja.wikipedia.org/wiki/ファイル:80486dx2-large.jpg "wikilink") 486は[386の上位ないし後継の](../Page/Intel_80386.md "wikilink")[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")である。基本的な[命令セット](../Page/命令セット.md "wikilink")は386と同様に[IA-32](../Page/IA-32.md "wikilink")と後に呼ばれることになったもので、BSWAPなどいくつかの命令の追加がある。

実装としては、性能向上を重視した全くの新設計である。他に、新アーキテクチャの最初の実装のため386で発覚したいくつかの問題点の修正、[NDP](../Page/FPU.md "wikilink")（数値演算コプロセッサ）の標準での内蔵、x86系としては初のオンダイキャッシュ、などが主な特徴に挙げられる。なお、NDPを内蔵しない廉価版もある。

比較的複雑なx86およびIA-32命令セットを実装するため、8086以降386までは機能のほぼ全てを[マイクロプログラム方式](../Page/マイクロプログラム方式.md "wikilink")で実装していた。しかし、[RISC](../Page/RISC.md "wikilink")ブームなどもあり、インテルとしても性能向上は至上命題だったことから、ほどんどの[命令を](../Page/命令_\(コンピュータ\).md "wikilink")[ワイヤードロジック](https://ja.wikipedia.org/wiki/ワイヤードロジック "wikilink")による実行とし、5段[パイプラインも動作周波数の向上を狙ったものである](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")。周波数の向上と同時に、多くの命令のサイクル数も386と比べ大幅に削減され、基本的な命令は1サイクルとなった。またあまり本質的ではないが、当時の利用者にとって影響が大きかったものとしては仮想86モード中での入出力命令の高速化などもある。なお、乗算だけは42サイクルとなり386より1クロック遅くなった。ただし、複雑な動作を行う一部の命令についてはマイクロプログラムを併用している。浮動小数点モジュールは、統合によるオーバヘッドの削減による高速化のみで、パイプライン化はしていない。

## バリエーション

  - [Intel486 DX](../Page/Intel486_DX.md "wikilink")
    当初のラインナップ。当初は「80486」と呼ばれ、後に「486SX」が登場した時から「486DX」と呼ばれるようになった。
  - 486SX
    数値演算コプロセッサ機能無効の廉価版
  - [IntelDX2](../Page/IntelDX2.md "wikilink")
    DXの2倍クロックダブリング。当初の名称は「486DX2」。
  - DX4
    DXの3倍クロックダブリング
  - SX2
    SXの2倍クロックダブリング
  - 486SL
    486DXの省電力版（名称が似ているが、486SXの省電力版ではない）

### 内部が486の製品

[thumb](https://ja.wikipedia.org/wiki/ファイル:Intel_486_dx2_overdrive_2007_03_27.jpg "wikilink")

  - [オーバードライブプロセッサ](../Page/オーバードライブプロセッサ.md "wikilink")
    486DXや486SXを486DX2相当に変更する DX2ODP
    486DXや486SXを486DX4相当に変更する DX4ODP
    486SXを486SX2相当に変更する SX2ODP
  - 数値演算[コプロセッサ](../Page/コプロセッサ.md "wikilink")
    486SXと組み合わせ486DX相当を実現する [487SX](https://ja.wikipedia.org/wiki/Intel487 "wikilink")
    486SX2と組み合わせ486DX2相当を実現する 487SX2

## 発売履歴

  - [1989年](../Page/1989年.md "wikilink"): 80486発売（後に486DXと呼ばれるようになった）。
  - [1991年](../Page/1991年.md "wikilink"): 486SX発売。内蔵されていた数値演算コプロセッサの機能を無効化し、普及製品として価格を抑えたもの。外部バスはアドレス/データ共に32ビットのままであり、[486DXとピン配置もほぼ同じである](../Page/Intel486_DX.md "wikilink")。また、486SX搭載機に後から浮動小数点演算機能を追加する目的で[487SXが登場したが](https://ja.wikipedia.org/wiki/Intel487 "wikilink")、従来の[x87的コプロセッサではなく](../Page/Intel_8087.md "wikilink")、486DXの機能を全て含んでおり、内部的に同じものである。487SXを接続すると、従来の486SX CPU側は機能を停止する（この機能は後の486ベースのODPに活用された）。
  - [1992年](../Page/1992年.md "wikilink"): [486DX2発売](../Page/IntelDX2.md "wikilink")。486DXに[クロックダブラ](https://ja.wikipedia.org/wiki/クロックダブラ "wikilink")を内蔵し、内部クロックを2倍にし、システムクロック周波数はそのままにしたもの。周辺チップなどを高速なシステムクロックに対応させる必要なく、486DXで使用されていた周辺回路をそのまま利用してシステムを組むことが出来る。
  - [1992年](../Page/1992年.md "wikilink"): 486SX2発売。486SXの内部クロックを2倍にしたもの。
  - [1994年](../Page/1994年.md "wikilink"): IntelDX4発売。1次キャッシュメモリ容量を従来製品の2倍の16KBに増やし、486DXの内部クロックを3倍にしたもの。密かに乗算命令も高速化された。3倍なのにDX3ではない理由は、2.5倍での設定も可能であり、単なる3ではないことを意図している。名称に「Intel」と、従来の「i」よりさらに長いプレフィックスを含めたのは、他社の類似製品名との差別化と、商標権を主張しにくい単なる数字と記号の羅列を避けたため。同時に486DX2や486SX2もIntelDX2やIntelSX2と改称している。

## 互換他社製品

### 正規

  - IBM 486SLC
    インテルと[IBM](../Page/IBM.md "wikilink")の提携に基づく、IBMによる改良・製造版。[IBM 386SLCをベースに内蔵キャッシュを](../Page/IBM_386SLC.md "wikilink")16Kに増やし、486SLと同レベルの性能を実現したもの。名称より「486SLベース」との誤解が多いがコアは386SLベースである。名称の「C」はCacheの略とも言われる。インテル版に相当する「i486SLC」は存在しない。
  - IBM 486SLC2
    IBM 486SLCの内部クロック倍増版。50/25（内部50MHz、外部25MHz）など。
  - IBM 486DX4
    インテルと[IBM](../Page/IBM.md "wikilink")の提携に基づく、IntelDX4のIBM製造版。
  - IBM 486DLC3(IBM 486BL - Blue Lightning)
    インテルと[IBM](../Page/IBM.md "wikilink")の提携に基づく、486SL (486SX) ベースの内部クロック3倍速版。1次キャッシュ16Kを内蔵し、386DXピン互換では最高速と言われた。通称IBM Blue Lightning（青い稲妻）のため「486BL」とも呼ばれた。（当時IBMは[PowerPC](../Page/PowerPC.md "wikilink")推進のため、[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")以後の製造ライセンスは結ばず、自社PCにも[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")採用は遅らせたため、代わりに486ベースの改良版で対抗した）
  - 486SX(J)
    [日本電気](../Page/日本電気.md "wikilink")とインテルジャパンが共同設計した486SXベースのCPU。ノートPC向けに省電力化が図られている。このほかに、486DXベースの486DX (J) が存在する。いずれもデータバスが16ビットとなっており、386SX用マザーボードの製造技術が流用出来た。

### 非正規

#### AMD

  - AMD Am486SX
    AMD Am486DX
    AMD Am486DX2
    [アドバンスト・マイクロ・デバイセズ](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") (AMD) が開発した、486互換プロセッサ。それぞれ486SX、486DX、486DX2相当。
  - AMD Am486DX4
    アドバンスト・マイクロ・デバイセズ (AMD) が開発した、486互換プロセッサ。DX4相当の3倍速動作だが、一次キャッシュがIntelのDX4より少ない8KB止まりの製品もある。
  - AMD [Am5x86](../Page/Am5x86.md "wikilink") (後にAm486DX5と改名)
    アドバンスト・マイクロ・デバイセズ (AMD) が開発した、486互換プロセッサ。システムクロックの4倍で動作。

#### Cyrix

  - Cyrix Cx486S
    Cyrix Cx486DX
    Cyrix Cx486DX2
    Cyrix Cx486DX4
    [サイリックス](../Page/サイリックス.md "wikilink")が開発した、486互換プロセッサ。従来の[Cx486DLC](../Page/Cyrix_Cx486DLC.md "wikilink")/Cx486DRx2とは違い、i486ピン互換となった。それぞれ486SX、486DX、486DX2、486DX4相当。DX2相当品ではIntel版には無い80MHz版が存在した。
  - Cyrix [Cx5x86](../Page/Cyrix_Cx5x86.md "wikilink")
    サイリックスが開発した、486互換プロセッサ。486とピン互換ではあるものの、内部は Cyrix 6x86 ・ AMD K5 ・ インテル Pentium のような第五世代のプロセッサと多くの共通点を持ち、486や他の486互換プロセッサとは基本的な設計から異なっている。

## 注

<references/>

## 外部リンク

  - [- インテルミュージアム - 486画像](http://www.intel.com/jp/intel/museum/hof/486.htm)

[Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink")