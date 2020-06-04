> この記事は[Stan \(プログラミング言語\)](https://ja.wikipedia.org/wiki/Stan_\(プログラミング言語\))から翻訳されています。


**Stan**（スタン）は[C++](../Page/C++.md "wikilink")で書かれた統計的推論のための確率的プログラミング言語\[1\]\[2\]。 Stan言語では、対数[確率密度関数](../Page/確率密度関数.md "wikilink")を計算する[命令型プログラムを使用して](../Page/命令型プログラミング.md "wikilink")、（ベイジアン） 統計モデルを実装できる。

らによって開発され\[3\]、 [モンテカルロ法](../Page/モンテカルロ法.md "wikilink")の先駆者である[スタニスワフ・ウラム](../Page/スタニスワフ・ウラム.md "wikilink")にちなんで名付けられた。 [BSDライセンス](../Page/BSDライセンス.md "wikilink")の下でライセンスされている。

## インターフェース

Stanにはいくつかのインターフェースからアクセスできる。

  - RStan - [R言語](../Page/R言語.md "wikilink")との統合。アンドリュー・ゲルマンらによってメンテナンスされている。
  - PyStan - [Python](../Page/Python.md "wikilink")との統合。
  - CmdStan - [Unixシェル](https://ja.wikipedia.org/wiki/Unixシェル "wikilink")のコマンドライン実行可能ファイル。
  - MatlabStan - [MATLAB](../Page/MATLAB.md "wikilink")数値計算環境との統合。
  - Stan.jl - [Juliaとの統合](https://ja.wikipedia.org/wiki/Julia_\(プログラミング言語\) "wikilink")。
  - StataStan - [Stata](https://ja.wikipedia.org/wiki/Stata "wikilink")との統合。
  - MathematicaStan - [Mathematica](../Page/Mathematica.md "wikilink")との統合。
  - ScalaStan - [Scala](../Page/Scala.md "wikilink")との統合

## アルゴリズム

Stanは、ベイジアン推論のための勾配ベースの[マルコフ連鎖モンテカルロ法](../Page/マルコフ連鎖モンテカルロ法.md "wikilink") （MCMC法）アルゴリズム、近似ベイズ推論のための確率論的勾配ベース変分ベイズ法 、およびペナルティ付き最尤推定のための勾配ベース[最適化を実装している](https://ja.wikipedia.org/wiki/数理最適化 "wikilink")。

  - MCMC法のアルゴリズム：
      - No-U-Turn Sampler\[4\]\[5\]\[6\]（NUTS）：HMC法の変法であり、StanのデフォルトのMCMCエンジンとなっている。
      - [ハミルトニアン・モンテカルロ法](../Page/ハミルトニアン・モンテカルロ法.md "wikilink") （HMC法）
  - 変分推論アルゴリズム：
      - ブラックボックス変分推論\[7\]
  - 最適化アルゴリズム：
      - 制限付きメモリBFGS （Stanのデフォルトの最適化アルゴリズム）
      - [Broyden–Fletcher–Goldfarb–Shannoアルゴリズム](https://ja.wikipedia.org/wiki/BFGS法 "wikilink")
      - 古典的な標準誤差の推定値と近似ベイズ後置子に対する[ラプラスの方法](../Page/ラプラスの方法.md "wikilink")

## 活用例

スタンは、社会科学、医薬品統計\[8\]、市場調査\[9\]、[医用画像](../Page/医用画像処理.md "wikilink")\[10\]などの分野で使用されている。

## 参考文献

  -
  - Gelman, Andrew, Daniel Lee, and Jiqiang Guo (2015).  [Stan: A probabilistic programming language for Bayesian inference and optimization](http://www.stat.columbia.edu/~gelman/research/published/stan_jebs_2.pdf), Journal of Educational and Behavioral Statistics.

  - Hoffman, Matthew D., Bob Carpenter, and Andrew Gelman (2012). [Stan, scalable software for Bayesian modeling](http://probabilistic-programming.org/wiki/NIPS*2012_Workshop/Schedule#talk-hoffman), Proceedings of the NIPS Workshop on Probabilistic Programming.

## 外部リンク

  - [Stan](http://mc-stan.org/) - 公式ウェブサイト
  - [Stan source](https://github.com/stan-dev/stan), a [Git](https://ja.wikipedia.org/wiki/Git_\(software\) "wikilink") repository hosted on [GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")

[Category:確率的ソフトウェア](https://ja.wikipedia.org/wiki/Category:確率的ソフトウェア "wikilink") [Category:ドメイン固有言語](https://ja.wikipedia.org/wiki/Category:ドメイン固有言語 "wikilink") [Category:計算統計学](https://ja.wikipedia.org/wiki/Category:計算統計学 "wikilink")

1.  Stan Development Team. [Stan User’s Guide 2.23](https://mc-stan.org/docs/2_23/stan-users-guide/index.html)
2.  Stan Development Team. [Stan Reference Manual 2.23](https://mc-stan.org/docs/2_23/reference-manual/)
3.
4.
5.
6.
7.
8.
9.
10.