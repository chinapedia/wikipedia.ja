> この記事は[PowerPC G3](https://ja.wikipedia.org/wiki/PowerPC_G3)から翻訳されています。


[thumb製のPowerPC](https://ja.wikipedia.org/wiki/ファイル:XPC750.jpg "wikilink") 750。Power Macintosh G3向けのもので、上部に[バックサイドキャッシュ](https://ja.wikipedia.org/wiki/バックサイドキャッシュ "wikilink")が見られる。以下の製品と比べ、[ヒートスプレッダ](https://ja.wikipedia.org/wiki/ヒートスプレッダ "wikilink")が無いのが特徴である。\]\] [thumb](https://ja.wikipedia.org/wiki/ファイル:PPC750CXEHP55-3_01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:GEKKO.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:PowerForceG3.jpg "wikilink")  **PowerPC G3**（パワーピーシー・ジースリー）は[PowerPC](../Page/PowerPC.md "wikilink")の第3世代[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")を呼ぶものとして、[アップルコンピュータによって使われた名称である](../Page/アップル_\(企業\).md "wikilink")。主にアップルの製品に採用されていたPowerPC 75xシリーズを指すが、組み込み用途などに使われるPowerPC 74xを含むこともある。

当初は[Macintosh互換機](../Page/Macintosh互換機.md "wikilink")用として互換機メーカーに供給されたが、後に[Macintosh](../Page/Macintosh.md "wikilink")コンピュータの[CPU](../Page/CPU.md "wikilink")としても、97年発売の[Power Macintosh G3に採用された](https://ja.wikipedia.org/wiki/Power_Macintosh#Power_Macintosh_G3_DT,_MT,AIO "wikilink")。**PowerPC G3**の名称が使われたのは、この時からである。引き続いて、[PowerBook G3](../Page/PowerBook_G3.md "wikilink")、[iMac](https://ja.wikipedia.org/wiki/iMac "wikilink")、[iBook](https://ja.wikipedia.org/wiki/iBook "wikilink")などに広く採用され、2003年にiBook G4が発売されるまで6年間採用され続けた。

2006年のAppleの路線変更（MacintoshのCPUをPowerPC系からIntel系に変更）により、PowerPCは組込み用途専用の製品となった。IBMは2009年よりPowerPC G3シリーズをPowerPC 400系と統合し、PowerPC 476FPを発表した。

## 設計

PowerPC G3は[PowerPC 603e及びPowerPC](../Page/PowerPC_603.md "wikilink") 603evの発展系として開発された。開発はアップルコンピュータ、[IBM](../Page/IBM.md "wikilink")、[モトローラ](../Page/モトローラ.md "wikilink")の共同で行われた。

[CPUバス](../Page/CPUバス.md "wikilink")は60xバスで、パッケージは[CBGA](https://ja.wikipedia.org/wiki/CBGA "wikilink")または[PBGA](https://ja.wikipedia.org/wiki/PBGA "wikilink")。発展系であるため、既存のPowerPCと完全な互換性がある。

PowerPC G3ではベースとなるPowerPC 603eの2+1(1は分岐)命令実行のスーパースカラプロセッサコアをベースに、以下の様な改良を加えた。

  - [バックサイド・キャッシュ・アーキテクチャーの採用](../Page/キャッシュメモリ.md "wikilink")（75xのみ）
    これは、従来システムバス上に置かれていた外部の[L2キャッシュを](../Page/キャッシュメモリ.md "wikilink")、専用の高速なバスによってCPUと直接繋げることにより、L2キャッシュへのアクセスを高速化させるというものである。また、G3ではL2キャッシュのタグもプロセッサに内蔵しており、高速なキャッシュヒットの検出が可能であった。この仕組みの採用により、PowerPC G3は従来型に比べ効率的な処理が可能となり、大幅な性能向上が見られた。
  - 内蔵する[L1キャッシュを](../Page/キャッシュメモリ.md "wikilink")64KBに倍増
    603eではデータ16KB+命令16KBの合計32KBであったが、G3では倍増された。これは604eと同じ容量である。
  - 一次命令キャッシュの帯域を16バイト/サイクルに倍増
    603eではL1命令キャッシュの帯域が8バイト/サイクルで、コアには1サイクル当たり2命令しか供給できなかった。603eのコア自体は3-way (2命令+1分岐) のスーパースカラであったが、この制限によりコアの性能を生かしきれていなかった。
  - 整数演算ユニットを2つに増加
    乗除算等のレイテンシが長い命令以外を実行可能な演算器を新たに追加し、整数演算ユニットの数は2個になった。これによって多くの整数演算命令について2命令を同時に実行することが可能になり、大幅に性能が向上した。この改良により、整数演算命令同士を並び替えてアウト・オブ・オーダー実行することも可能になったが、各整数演算ユニットに備えられているリザベーション・ステーションは1エントリであり、効果は限定的である。
  - 動的[分岐予測](../Page/分岐予測.md "wikilink")機構の採用
    603eではPowerPC命令のヒントを利用した静的分岐予測機構のみ実装されていたが、G3では動的分岐予測 (2レベル予測) も行われる。G3の動的分岐予測は604のものとは異なり、604では分岐先の予測にBTAC (Branch Target Address Cache) と呼ばれる分岐先アドレスのキャッシュを用いていたのに対し、G3ではBTIC (Branch Target Instruction Cache) と呼ばれる分岐先の命令 (2命令分) を直接キャッシュする仕組みが用いられている。分岐命令がBTICにヒットすると、分岐先の命令を命令キャッシュからではなくこのBTICから直接供給することが可能であり、1サイクル早く命令キューに分岐先の命令を入れることができる。
  - ハードウェアによる[TLB](https://ja.wikipedia.org/wiki/TLB "wikilink")ミスの処理
    603シリーズではTLBミス時に例外が発生し、OSがTLBを更新する必要があったが、G3プロセッサでは604シリーズと同様にプロセッサが自動的にTLBを更新する。これによってTLBミス時のペナルティが減少している。

当初はハイエンドの[PowerPC 604の後継として](../Page/PowerPC_604.md "wikilink")、"Mach5"の名で知られる、インラインキャッシュを搭載したPowerPC604evが開発されており、PowerPC 750/740は、互換機メーカー向けの安価なマイクロプロセッサとして供給されていた。PowerPC750の性能がMach5を上回ることが明らかになったため、アップルコンピュータ自身も採用し、その際に新たに**PowerPC G3**と命名される。ほぼ同時期にアップルは互換機戦略を撤回している。

## 特徴

PowerPC G3は以下の様な優れた特徴を備えていた。

  - サイズは25mm角または27mm角と小型である
  - 1クロックあたりの処理能力が高い
  - 低消費電力
  - 安価

特に低消費電力は大きな特徴で、例えば銅配線のPowerPC 750Lの場合、500MHzでの平均/最大消費電力は、6.0W/7.5Wであった。このためPowerPC G3は[ノートパソコン](../Page/ノートパソコン.md "wikilink")にも動作クロックをほとんど下げることなくそのまま搭載され、据え置き型と同等の処理能力を与えることに成功した。 また、安価であったため、[iMac](https://ja.wikipedia.org/wiki/iMac "wikilink")などの低価格なパソコンにも採用された。

一方で、L2キャッシュなどの影響を考慮しない、純粋な演算能力の比較では[PowerPC 604がG](../Page/PowerPC_604.md "wikilink")3を圧倒する。604シリーズを全面的に越えるのは、その強力な浮動小数点ユニットを採用したG3の後継の[PowerPC G4が登場してからである](../Page/PowerPC_G4.md "wikilink")。

## 製品

  - PowerPC 750
  - PowerPC 750L -750の銅配線版
  - PowerPC 750CX/CXe -180nm SOIで製造、-256KB L2キャッシュを内蔵、350〜550MHzで動作する。
  - PowerPC 750FX/FL -[SOI](../Page/SOI.md "wikilink")で製造、L2キャッシュ512KB
  - PowerPC 750GX -90nm SOIで製造、200MHz [FSB対応](../Page/フロントサイドバス.md "wikilink")、L2キャッシュ1MB、1.1GHzまで
  - PowerPC 750CL -90nm SOIで製造、L2キャッシュ256KB、1GHzまで。消費電力は400MHzで1.7W、900MHzで5.6Wにまで省電力化されている。64ビットの倍精度浮動小数点レジスタを利用して単精度のSIMD演算を行う命令が追加されている等、いくつかの機能が追加されている。
  - PowerPC 74x-組み込み用途向け、L2キャッシュなし
  - [Gekko](../Page/Gekko.md "wikilink") -180nm SOIで製造、[ニンテンドーゲームキューブ](../Page/ニンテンドーゲームキューブ.md "wikilink")用に開発されたもの（PowerPC 750CXeをベースに倍精度浮動小数点数演算対応[SIMD](../Page/SIMD.md "wikilink")を追加した設計）
  - [Broadway](https://ja.wikipedia.org/wiki/Broadway_\(マイクロプロセッサ\) "wikilink") - 90nm SOIで製造、[任天堂](../Page/任天堂.md "wikilink")の[Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")用に開発されたもの（Gekko互換であり、PowerPC 750CLがベースと思われるが詳細は非公開）
  - [Espresso](https://ja.wikipedia.org/wiki/Espresso "wikilink") - 45nm SOIで製造、[任天堂](../Page/任天堂.md "wikilink")の[Wii U用に開発されたもの](https://ja.wikipedia.org/wiki/Wii_U "wikilink")（Broadway互換）
  - RAD750 - PowerPC 750をベースに、耐放射線仕様を付加したマイクロコントローラ。宇宙での使用を想定しRAD6000の後継として開発され、[マーズ・リコネッサンス・オービター](../Page/マーズ・リコネッサンス・オービター.md "wikilink")をはじめとする宇宙探査機に搭載される。

## 関連項目

  - [PowerPC G4](../Page/PowerPC_G4.md "wikilink")
  - [PowerPC 970](../Page/PowerPC_970.md "wikilink")
  - [IBM POWER](../Page/POWER_\(マイクロプロセッサ\).md "wikilink")

[Category:IBMのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:IBMのマイクロプロセッサ "wikilink") [Category:アップルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:アップルのマイクロプロセッサ "wikilink") [Category:モトローラのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:モトローラのマイクロプロセッサ "wikilink")