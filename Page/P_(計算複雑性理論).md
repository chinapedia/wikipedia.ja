> この記事は[P \(計算複雑性理論\)](https://ja.wikipedia.org/wiki/P_\(計算複雑性理論\))から翻訳されています。


[計算量理論](https://ja.wikipedia.org/wiki/計算量理論 "wikilink")における**P**とは[多項式時間](https://ja.wikipedia.org/wiki/多項式時間 "wikilink")（polynomial time）で解ける判定問題の集合である。

## 定義

[判定問題](https://ja.wikipedia.org/wiki/判定問題 "wikilink")のうち、ある[決定性チューリング機械によって](https://ja.wikipedia.org/wiki/チューリング機械 "wikilink")[多項式時間](https://ja.wikipedia.org/wiki/多項式時間 "wikilink")で解かれるものの全体を**P**で表す。

## 意義

**P**はしばしば、「効率的に解ける」問題のクラスとして扱われる。しかしながら、[RPや](../Page/RP_\(計算複雑性理論\).md "wikilink")[BPPといった乱択で解けるクラスも](https://ja.wikipedia.org/wiki/BPP_\(計算量理論\) "wikilink")、Pより大きいかもしれないが「効率的に解ける」と考えることもできる。逆に**P**に属しても実際には扱うことが困難である問題もある。例えば、入力のサイズ*n*に対して*n*<sup>1000000</sup>の時間を必要とする問題も、定義からは**P**に属する。

**P**に属する問題のうち[対数領域還元](https://ja.wikipedia.org/wiki/対数領域還元 "wikilink")に関して最大なものは**P完全**であるという。

## 他の問題クラスとの関係

[非決定性チューリング機械](https://ja.wikipedia.org/wiki/非決定性チューリング機械 "wikilink")によって多項式時間で解かれる[判定問題](https://ja.wikipedia.org/wiki/判定問題 "wikilink")のクラスを[NP](../Page/NP.md "wikilink")という。**P**がNPに含まれることは自明である。多くの研究者が**P**はNPの[真部分集合](https://ja.wikipedia.org/wiki/真部分集合 "wikilink")であると信じているが、証明されていない（[P≠NP予想](../Page/P≠NP予想.md "wikilink")）。

[対数領域](https://ja.wikipedia.org/wiki/対数領域 "wikilink")の[決定性チューリング機械で判定可能な問題のクラスである](https://ja.wikipedia.org/wiki/チューリング機械 "wikilink")[Lは](https://ja.wikipedia.org/wiki/L_\(計算複雑性理論\) "wikilink")**P**に含まれるが、L = **P**かどうかは未解決である。対数領域の[交替性チューリング機械](../Page/交替性チューリング機械.md "wikilink")によって解ける問題のクラス[ALOGSPACE](https://ja.wikipedia.org/wiki/ALOGSPACE "wikilink")は**P**に等しい。**P**は[PSPACE](https://ja.wikipedia.org/wiki/PSPACE "wikilink")の部分集合であるが、**P** = PSPACEであるかどうかは未解決である。まとめると次のような関係がある:

\[\mathbf{L} \subseteq \mathbf{ALOGSPACE} = \mathbf{P} \subseteq \mathbf{NP} \subseteq \mathbf{PSPACE} \subseteq \mathbf{EXPTIME}\]

ここで、[EXPTIME](https://ja.wikipedia.org/wiki/EXPTIME "wikilink")は指数時間で解ける問題のクラスである。**P**はEXPTIMEの真部分集合であるから、**P**よりも右の包含関係のうち少なくとも一つは真部分集合である（実際には上に示された包含がみな真の包含であると広く予想されている）。

## 関連するクラス

  - クラス [NP](../Page/NP.md "wikilink") - 提出された答えの検算がクラス **P** になる決定問題のクラス。
  - クラス [FP](https://ja.wikipedia.org/wiki/FP_\(計算量理論\) "wikilink") - クラス **P** と類似した概念ではあるが、クラス **P** とは違い解を出力することができる問題のクラス。
  - クラス [RP](../Page/RP_\(計算複雑性理論\).md "wikilink") - 答えが no のときは必ず no で返すが、答えが yes のときはある確率で no と答えることがある[乱択算法によって解かれる判定問題のクラス](https://ja.wikipedia.org/wiki/乱択アルゴリズム "wikilink")。[モンテカルロ法](../Page/モンテカルロ法.md "wikilink")などの手法を計算理論上で解析するために生まれた。
  - [多項式階層](https://ja.wikipedia.org/wiki/多項式階層 "wikilink")

[Category:計算複雑性理論](https://ja.wikipedia.org/wiki/Category:計算複雑性理論 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")