> この記事は[マローズのCp](https://ja.wikipedia.org/wiki/マローズのCp)から翻訳されています。


**Mallowsの*C<sub>p</sub>***\[1\] \[2\]は、最小二乗法によって推定された[回帰モデルの適合度を評価するために用いられる指標である](../Page/回帰分析.md "wikilink")。名前は[コリン・リングウッド・マローにちなむ](https://ja.wikipedia.org/wiki/:en:Colin_Lingwood_Mallows "wikilink")。[モデル選択を行う際に用いられ](https://ja.wikipedia.org/wiki/:en:model_selection "wikilink")、ある複数の変数から出力を予測することができるとき、その中から一部の変数を選んで最も良いモデルを見つけることが目的である。C<sub>p</sub>の値が小さいほど、モデルが比較的正確であることを意味する。

マローズの*C<sub>p</sub>*は、ガウス[線形回帰](../Page/線形回帰.md "wikilink")という特殊な場合において[赤池情報量基準に相当することが示されている](../Page/赤池情報量規準.md "wikilink")。\[3\]

## 定義と性質

マローズの*C<sub>p</sub>*は、[過剰適合](../Page/過剰適合.md "wikilink")の問題に対する方法である。一般にモデルの変数が増えれば増えるほど、[残差平方和](https://ja.wikipedia.org/wiki/残差平方和 "wikilink")などのモデル適合度の指標は常に小さくなる。したがって、残差平方和が最小となるモデルを選択する場合、常にすべての変数を含むモデルが選択されてしまう。代わりに、データの[サンプルで計算された](../Page/標本_\(統計学\).md "wikilink")*C <sub>p</sub>*統計は、 [母集団](../Page/母集団.md "wikilink")ターゲットとして平均二乗予測誤差 （MSPE）を推定する。

  -
    <math>

E\\sum_j \\frac{(\\hat{Y}_j - E(Y_j\\mid X_j))^2}{\\sigma^2} </math>

ただし、\(\hat{Y}_j\) は *j* 番目のケースのフィット値、*E* (*Y*<sub>*j*</sub> | *X*<sub>*j*</sub>) は *j* 番目*の*ケースの期待値であり、σ<sup>2</sup>は誤差分散（全ケース共通の定数とみなされる）である。変数が追加されても、MSPEは自動的に小さくなることはない。この基準での最適なモデルは、サンプルサイズ、さまざまな予測変数の[効果量](https://ja.wikipedia.org/wiki/効果量 "wikilink")、および変数間の[共線](https://ja.wikipedia.org/wiki/共線 "wikilink")性の程度によって決まる。

*P個の*変数が*K*\>*P*であるような*K個の変数*から選択された場合、*C<sub>p</sub>*は次のように定義される。

  -
    \(C_p={SSE_p \over S^2} - N + 2P,\)

ただし、

  - \(SSE_p = \sum_{i=1}^N(Y_i-Y_{pi})^2\)は、*P個の*変数を持つモデルの[残差平方和](https://ja.wikipedia.org/wiki/残差平方和 "wikilink")
  - *Y* <sub>pi</sub>は、 *P* リグレッサからの*Yの* *i*番目の観測の[予測値](../Page/予言.md "wikilink")
  - *S* <sup>2</sup>は、 *K個すべての変数*を用いて[回帰分析](../Page/回帰分析.md "wikilink")を行った場合の残差平均平方（residual mean square）であり、[平均二乗誤差](https://ja.wikipedia.org/wiki/平均二乗偏差 "wikilink")（MSE*）*によって推定される。
  - *N*は標本サイズ

## その他の定義

次のような線形モデルがあるとする。

  -
    \(Y = \beta_0 + \beta_1X_1+\cdots+\beta_pX_p + \varepsilon\)

ただし、

  - \(\beta_0,\ldots,\beta_p\)は予測変数\(X_1,\ldots,X_p\)の係数
  - \(\varepsilon\)は誤差を表す

*C<sub>p</sub>以下のようにも定義される*\[4\]。

  -
    \(C_p=\frac{1}{n}(\operatorname{RSS} + 2d\hat{\sigma}^2)\)

ただし、

  - RSSは、教師データセットの残差平方和

  - は予測変数の数

  - \(\hat{\sigma}^2\)は線形モデルの各応答に関連する分散の推定値を指す（すべての予測子を含むモデルで推定される）

この定義による*C<sub>p</sub>*の値は、前掲の定義による*C<sub>p</sub>*の値と等しくないが、いずれの定義においても*C<sub>p</sub>を最小にするようなモデルは同一である。*

## 制約

*C<sub>p</sub>*基準には主に2つの制約がある\[5\]。

1.  *C<sub>p</sub>*近似は大きなサンプルサイズに対してのみ有効である。
2.  *C<sub>p</sub>は*変数選択（または[特徴選択](https://ja.wikipedia.org/wiki/特徴選択 "wikilink")）の問題のようなモデルの複雑な集合を扱うことができない\[6\]。

## 実用

## 関連項目

  - [回帰分析](../Page/回帰分析.md "wikilink")
  - [決定係数](../Page/決定係数.md "wikilink")
  - [赤池情報量基準](https://ja.wikipedia.org/wiki/赤池情報量基準 "wikilink")

## 参考文献

## 参照

  -
  -
  -
[Category:回帰診断](https://ja.wikipedia.org/wiki/Category:回帰診断 "wikilink")

1.
2.
3.
4.
5.  Giraud, C. (2015), *Introduction to high-dimensional statistics*, Chapman & Hall/CRC,
6.  Giraud, C. (2015), *Introduction to high-dimensional statistics*, Chapman & Hall/CRC, [ISBN](https://ja.wikipedia.org/wiki/ISBN_\(identifier\) "wikilink") [9781482237948](https://ja.wikipedia.org/wiki/Special:BookSources/9781482237948 "wikilink")