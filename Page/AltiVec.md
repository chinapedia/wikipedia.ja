> この記事は[AltiVec](https://ja.wikipedia.org/wiki/AltiVec)から翻訳されています。


**AltiVec**（アルティベック、アルチベック、アルタベク）は[米国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[モトローラ](../Page/モトローラ.md "wikilink")が開発した[ベクトル演算](https://ja.wikipedia.org/wiki/ベクトル演算 "wikilink")ユニット。

## 概要

科学計算用の[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")に採用されていたベクトル演算ユニットを踏襲し、[128ビット](https://ja.wikipedia.org/wiki/128ビット "wikilink")の[レジスタを](../Page/レジスタ_\(コンピュータ\).md "wikilink")32本搭載し、162もの[命令を追加している](../Page/命令_\(コンピュータ\).md "wikilink")。

AltiVec は [PowerPC G4](../Page/PowerPC_G4.md "wikilink") (PowerPC 74xx) シリーズに採用されている。

## Vector Multimedia Extension

**Vector Multimedia Extension** (VMX) は[IBM](../Page/IBM.md "wikilink")がモトローラと共同開発した[ベクトル演算](https://ja.wikipedia.org/wiki/ベクトル演算 "wikilink")ユニット。AltiVec とはハードウェアの実装などが異なるが基本的な構成や命令セットは同一のものである。ただし、要素ロード命令や一部のシフト命令など、AltiVecとVMXで厳密には動作が異なる命令があり、完全な[互換性](../Page/互換性.md "wikilink")はない\[1\]。

PowerPC G5 ([PowerPC 970](../Page/PowerPC_970.md "wikilink")) で初めて採用され、POWER6以降のPOWERプロセッサシリーズで使用可能である。[マイクロソフト](../Page/マイクロソフト.md "wikilink")のゲーム機 [Xbox 360](../Page/Xbox_360.md "wikilink") のCPU"PX"では、PowerPC 970 の VMX を拡張し、レジスタを128本とした **VMX-128** が搭載されている。VMX-128は[プレイステーション3に搭載された](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")[Cell](../Page/Cell_Broadband_Engine.md "wikilink") の Power Processor Element (PPE) にも採用された。

## Velocity Engine

**Velocity Engine**（ベロシティ・エンジン）は、[アップルコンピュータ](../Page/アップル_\(企業\).md "wikilink") によるAltiVecならびにVMXの呼称。AltiVecとVMXは別の技術であるが、互換性があるためアップルコンピュータでは同一の呼称を使用している。

[QuickTime](../Page/QuickTime.md "wikilink")が全面対応しており、『[GarageBand](../Page/GarageBand.md "wikilink")』や『[iTunes](https://ja.wikipedia.org/wiki/iTunes "wikilink")』『[Final Cut Pro](../Page/Final_Cut_Pro.md "wikilink")』『iDVD』など多くの[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")で活用される。

## 脚注

## 関連項目

  - [SIMD](../Page/SIMD.md "wikilink")
  - [ストリーミングSIMD拡張命令](../Page/ストリーミングSIMD拡張命令.md "wikilink") (SSE)
  - [POWER](../Page/POWER_\(マイクロプロセッサ\).md "wikilink")
  - [PowerPC](../Page/PowerPC.md "wikilink")
  - [Cell](../Page/Cell_Broadband_Engine.md "wikilink")
  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")
  - [フリースケール・セミコンダクタ](../Page/フリースケール・セミコンダクタ.md "wikilink")

## 外部リンク

  - [Freescale's AltiVec](http://www.freescale.com/webapp/sps/site/overview.jsp?nodeId=0162468rH3bTdGmKqW5Nf2)
  - [Apple's Velocity Engine](http://developer.apple.com/hardware/ve/)

[Category:CPU](https://ja.wikipedia.org/wiki/Category:CPU "wikilink")

1.  [Instruction Level Differences Between G4 and G5](http://developer.apple.com/hardwaredrivers/ve/g5.html#differences)