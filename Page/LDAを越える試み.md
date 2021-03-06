> この記事は[LDAを越える試み](https://ja.wikipedia.org/wiki/LDAを越える試み)から翻訳されています。


**LDAを越える試み**()とは、[局所密度近似](../Page/局所密度近似.md "wikilink")(LDA)の問題点を解消する新たな手法を見出す試みの総称である。

[局所密度近似](../Page/局所密度近似.md "wikilink")は大変成功した近似であるが、実際の系に対する様々な計算の結果、その限界もまた露わになってきた。 代表的な問題点とその克服に向けたアプローチについて記述する。

## 代表的な問題点（限界）

1.  [半導体](../Page/半導体.md "wikilink")、[絶縁体](../Page/絶縁体.md "wikilink")において[バンドギャップ](../Page/バンドギャップ.md "wikilink")が実験値より過小な値となる。
2.  [鉄](../Page/鉄.md "wikilink")の[強磁性](../Page/強磁性.md "wikilink")結晶構造（体心立方構造：BCC）が安定とならない。（他にも安定構造や電子状態が[LDAが原因で](../Page/局所密度近似.md "wikilink")、実際のものと一致しない場合がある。GGA近似を行うことで修正される場合がある。）。
3.  [活性化エネルギー](../Page/活性化エネルギー.md "wikilink")の過小評価。
4.  鏡像ポテンシャルが記述できない（[表面](https://ja.wikipedia.org/wiki/表面 "wikilink")）。
5.  [自己相互作用補正](https://ja.wikipedia.org/wiki/自己相互作用補正 "wikilink")の問題。
6.  絶対零度（基底状態）での計算が前提。←[密度汎関数理論](../Page/密度汎関数理論.md "wikilink")
7.  励起状態に対する計算の正しさの保証がない（これは、むしろ密度汎関数理論の問題）。など

（**注**：問題点はこれらだけではない）

## 問題を克服する手段・手法

以下のようなものが提案、試行されている。

  - [GGA](https://ja.wikipedia.org/wiki/GGA "wikilink")（Generalized Gradient Approximation, 一般化された密度勾配近似）
  - SIC（Self-Interaction Correction, [自己相互作用補正](https://ja.wikipedia.org/wiki/自己相互作用補正 "wikilink")）
  - [GW近似](../Page/GW近似.md "wikilink")
  - [LDA+U](https://ja.wikipedia.org/wiki/LDA_plus_U "wikilink")(LSDA+U)
  - [TDDFT](https://ja.wikipedia.org/wiki/TDDFT "wikilink")([TDLDA](https://ja.wikipedia.org/wiki/TDLDA "wikilink"))（Time-Dependent DFT, 時間発展を考慮した密度汎関数理論）

などがよく利用されている。さらに、交換項を（[ハートリー-フォック法](https://ja.wikipedia.org/wiki/ハートリー-フォック法 "wikilink")での交換項として）厳密に取り扱うアプローチ(Exact Exchange)、[密度汎関数理論](../Page/密度汎関数理論.md "wikilink")の[有限温度への拡張](https://ja.wikipedia.org/wiki/有限温度への拡張 "wikilink")や、[電子](https://ja.wikipedia.org/wiki/電子 "wikilink")の[多体問題](../Page/多体問題.md "wikilink")をより直接的に扱う方法（[量子モンテカルロ法](../Page/量子モンテカルロ法.md "wikilink")による）、また動的平均場法などの強相関電子系でのモデル計算で開発された手法と組み合わせ、電子相関の効果を導入する研究がされているが、まだ汎用的な計算手法とは言い難く、簡単な系でのテスト計算どまりである。

## 関連項目

  - [第一原理バンド計算](../Page/第一原理バンド計算.md "wikilink")

[Category:固体物理学](https://ja.wikipedia.org/wiki/Category:固体物理学 "wikilink")