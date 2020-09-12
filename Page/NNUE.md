> この記事は[NNUE](https://ja.wikipedia.org/wiki/NNUE)から翻訳されています。


**Efficiently updatable neural network**（**NNUE**; ****と図案化されることもある）は、[Graphics Processing Unit](../Page/Graphics_Processing_Unit.md "wikilink")（GPU）を必要とせず、[中央処理装置](https://ja.wikipedia.org/wiki/中央処理装置 "wikilink")（CPU）上で効率的に動作する[ニューラルネットワーク](../Page/ニューラルネットワーク.md "wikilink")に基づく[評価関数](../Page/評価関数.md "wikilink")である。NNUEは那須悠によって考案され、2018年に[コンピュータ将棋](https://ja.wikipedia.org/wiki/コンピュータ将棋 "wikilink")に導入された\[1\]。NNUEはチェスエンジン[Stockfish](https://ja.wikipedia.org/wiki/Stockfish "wikilink")のコードに[マージされることが発表されている](https://ja.wikipedia.org/wiki/マージ_\(バージョン管理システム\) "wikilink")\[2\]。

## 構造

NNUEのニューラルネットワークは4つの重み層から構成される。W1は16ビット整数、W2、W3、およびW4は8ビット整数である。および[single instruction multiple data](../Page/SIMD.md "wikilink")（SIMD）技術が適切な、具体的には2018年のコンピュータ将棋版ではVPADDW、VPSUBW、VPMADDUBSW、VPACKSSDW、VPACKSSWB、およびVPMAXSBと共に用いられる\[3\]。

## 出典

## 関連項目

  - [elmo (コンピュータ将棋ソフト)](https://ja.wikipedia.org/wiki/elmo_\(コンピュータ将棋ソフト\) "wikilink")
  - [Stockfish](https://ja.wikipedia.org/wiki/Stockfish "wikilink")

## 外部リンク

  - [NNUE](https://www.chessprogramming.org/NNUE) on the Chess Programming Wiki.
  - [Stockfish NNUE](https://www.chessprogramming.org/Stockfish_NNUE) - Chess Programming Wiki

[Category:コンピュータチェス](https://ja.wikipedia.org/wiki/Category:コンピュータチェス "wikilink") [Category:コンピュータ将棋](https://ja.wikipedia.org/wiki/Category:コンピュータ将棋 "wikilink") [Category:評価方法](https://ja.wikipedia.org/wiki/Category:評価方法 "wikilink") [Category:ニューラルネットワーク](https://ja.wikipedia.org/wiki/Category:ニューラルネットワーク "wikilink")

1.
2.
3.