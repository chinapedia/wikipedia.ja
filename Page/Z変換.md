> この記事は[Z変換](https://ja.wikipedia.org/wiki/Z変換)から翻訳されています。


[関数解析学](../Page/関数解析学.md "wikilink")において、**Z変換**（ゼッドへんかん、Z-transform）とは、離散群上で定義される、[ローラン展開](https://ja.wikipedia.org/wiki/ローラン展開 "wikilink")をベースにした[関数空間](../Page/関数空間.md "wikilink")の間の[線形](https://ja.wikipedia.org/wiki/線形写像 "wikilink")[作用素](https://ja.wikipedia.org/wiki/作用素 "wikilink")。関数変換。

Z変換は離散群上での[ラプラス変換](https://ja.wikipedia.org/wiki/ラプラス変換 "wikilink")とも説明される。なお、Z変換という呼び方は、ラプラス変換のことを「S変換」と呼んでいるようなものであり、定義式中の遅延要素である*z*に由来する名前である。

## 定義

列*x*<sub>*n*</sub>のZ変換は以下の式で定義される:  ここで*n*は[整数](../Page/整数.md "wikilink")で*z*は[複素数](../Page/複素数.md "wikilink")である。なお後述の片側Z変換に対してこれを**両側Z変換**（two-sided Z-transform、bilateral Z-transform）と呼ばれる。

*n*\<0 で*x*<sub>*n*</sub>=0のような場合は、総和の範囲を 0 〜 ∞ で計算できる：  これを元の定義と区別して**片側Z変換**（single-sided Z-transform、unilateral Z-transform）と呼ぶこともある。工学の分野などでは[因果律](https://ja.wikipedia.org/wiki/因果律 "wikilink")を想定するので、こちらの式で定義することがある。

二次元信号（例えば画像）に対する二次元Z変換の定義は類似的である：

### 収束領域

なお、Z変換の級数は一般には発散することがある。収束する*z*の領域（収束領域，Region of Convergence）を以下のように書ける:

厳密にはこの収束領域内においての*X*(*z*)を、*x*<sub>*n*</sub>のZ変換と定義する。

二次元Z変換の収束領域の定義は類似する：

## 逆Z変換

Z変換の逆変換である**逆Z変換**（inverse Z-transform）は次のようになる:  ここで*i*は[虚数単位](../Page/虚数単位.md "wikilink")で積分路*C*は*X*(*z*)の極を全て含むような閉路である。

なおこの式は[留数](../Page/留数.md "wikilink")定理を用いて留数の和として計算することができる。しかし、手計算で計算するときは以下の方法がよく使われる：

  - *X*(*z*)が既に級数展開されている場合、*z*<sup>-*k*</sup>の係数を*x*<sub>*k*</sub>の値とすることで簡単に逆変換ができる。例えば、*z*+2-3*z*<sup>-1</sup>の逆変換は { ..., 0, *x*<sub>-1</sub>=1,*x*<sub>0</sub>=2,*x*<sub>1</sub>=-3, 0, ...} のように係数をならべるだけで得られる。
  - *X*(*z*)を[部分分数分解](../Page/部分分数分解.md "wikilink")し、各々の部分分数を変換表を用いて逆変換したものの和として逆変換を得る。

いずれにせよ、定義に示した積分計算そのものを直接計算することは稀である。

## 性質

  - 線型性
    Z変換は線型性を持ち、したがって特に重ね合わせの原理を用いて計算できる。したがって任意の*x*<sub>*n*</sub>,*y*<sub>*n*</sub>に対して
    \(\mathcal{Z}[a x_n + b y_n] = a \mathcal{Z}[x_n] + b \mathcal{Z}[y_n]\)
    が成立する。但し、*a*,*b*は定数。逆Z変換も同様に線型性を持つ。したがって、与えられた関数を[部分分数分解](../Page/部分分数分解.md "wikilink")できるとき、各因子が変換表にあるものに合致すれば、その変換が求められる。
  - シフト性
    \(\mathcal{Z}[x_{n-k}] = z^{-k}\mathcal{Z}[x_n]\)
  - Z領域微分
    \(\mathcal{Z}[n x_n] = -z \frac{d}{dz} \mathcal{Z}[x_n]\)
  - 畳み込み
    [フーリエ変換](../Page/フーリエ変換.md "wikilink")のように[畳み込み定理](https://ja.wikipedia.org/wiki/畳み込み定理 "wikilink")が成り立ち、[畳み込み](https://ja.wikipedia.org/wiki/畳み込み "wikilink")はZ変換によって積となる。
    \(\mathcal{Z}[x_n * y_n] =  \mathcal{Z}[x_n] \mathcal{Z}[y_n]\)
  - 初期値定理
    \(f(0)=\lim_{z\to\infty}F(z)\)
  - 最終値定理
    \(f(\infty)=\lim_{k\to\infty}f(k)=\lim_{z\to 1}\left\{\frac{z-1}{z}F(z)\right\}\)
  - 時間領域の乗積
    \(\mathcal{Z}[x_n h_n]=\frac{1}{2\pi i}\oint_{C_1} X(v)H\left(\frac{z}{v}\right)v^{-1}\,dv=\frac{1}{2\pi i}\oint_{C_2} H(v)X\left(\frac{z}{v}\right)v^{-1}\,dv\)

積分路 \(C_1\) は \(X(v)\) と \(H\left(\frac{z}{v}\right)\) の**ROC**の共同区域にある閉路であり、 \(C_2\) は \(H(v)\) と \(X\left(\frac{z}{v}\right)\) の**ROC**の共同区域にある閉路である。

  - Parseval定理
    \(\mathcal{Z}\left[\sum_{n=-\infty}^{+\infty}x_nh_n^*\right]=\frac{1}{2\pi i}\oint_{C_1} X(v)H^*\left(\frac{1}{v^*}\right)v^{-1}\,dv=\frac{1}{2\pi i}\oint_{C_2} H^*(v)X\left(\frac{1}{v}\right)v^{-1}\,dv\)

積分路 \(C_1\) は \(X(v)\) と \(H^*\left(\frac{1}{v^*}\right)\) の**ROC**の共同区域にある閉路であり、 \(C_2\) は \(H^*(v)\) と \(X\left(\frac{1}{v}\right)\) の**ROC**の共同区域にある閉路である。

## 離散時間のLTIシステム

離散時間のLTIシステムは以下の定数係数の線形差分方程式としてモデル化できる：  一般には、\(a_0=1\)と認める。

方程式の両辺をZ変換すると、  を得られて、 {\\displaystyle \\sum_{i=0}^{N}a_{i}z^{-i}}</math>}} は、[伝達関数と呼ばれ](../Page/伝達関数法.md "wikilink")、その分母多項式は[特性多項式](https://ja.wikipedia.org/wiki/特性多項式 "wikilink")と呼ばれる。

伝達関数を分析すれば、システム特性の解明に役立つ。

## 他の変換との関係性

### ラプラス変換との関係

Z変換は両側[ラプラス変換](https://ja.wikipedia.org/wiki/ラプラス変換 "wikilink")を離散化したものである。つまり離散化された関数  のラプラス変換  に対応する。但し、*T*はサンプリング周期であり、*e*<sup>*sT*</sup>がZ変換における*z*に対応する。

### 離散時間フーリエ変換との関係

Z変換は[離散時間フーリエ変換](../Page/離散時間フーリエ変換.md "wikilink")(DTFT)の拡張である。DTFTはZ変換で*z*=*e*<sup>*iω*</sup>を代入したものと一致する。言い換えると、[複素平面](https://ja.wikipedia.org/wiki/複素平面 "wikilink")で[単位円](../Page/単位円.md "wikilink")上のZ変換がDTFTであると解釈できる。

## 変換表

| 元の関数 *x*(*n*)                       | Z変換 *X*(*z*)                                                                    | 収束領域          |
| ----------------------------------- | ------------------------------------------------------------------------------- | ------------- |
| δ(*n*)                              | 1                                                                               | 複素数全体         |
| *u*(*n*)                            | \(\frac{1}{1-z^{-1}}\)                                                          | \(|z| > 1\)   |
| *a*<sup>*n*</sup>*u*(*n*)           | \(\frac{1}{1-a z^{-1}}\)                                                        | \(|z| > |a|\) |
| *n* *a*<sup>n</sup> *u*(*n*)        | \(\frac{az^{-1} }{ (1-a z^{-1})^2 }\)                                           | \(|z| > |a|\) |
| *a*<sup>n</sup> *u*(-*n*-1)         | \(\frac{-1}{1-a z^{-1}}\)                                                       | \(|z| < |a|\) |
| *n* *a*<sup>*n*</sup> *u*(-*n*-1)   | \(\frac{az^{-1} }{ (1-a z^{-1})^2 }\)                                           | \(|z| < |a|\) |
| cos(ω<sub>0</sub>*n*) *u*(*n*)      | \(\frac{ 1-z^{-1} \cos(\omega_0) }{ 1-2z^{-1}\cos(\omega_0)+ z^{-2} }\)         | \(|z| >1\)    |
| sin(ω<sub>0</sub>*n*) *u*(*n*)      | \(\frac{ z^{-1} \sin(\omega_0) }{ 1-2z^{-1}\cos(\omega_0)+ z^{-2} }\)           | \(|z| >1\)    |
| a<sup>n</sup> cos(ω<sub>0</sub>*n*) | \(\frac{ 1-a z^{-1} \cos( \omega_0) }{ 1-2az^{-1}\cos(\omega_0)+ a^2 z^{-2} }\) | \(|z| > |a|\) |
| a<sup>n</sup> sin(ω<sub>0</sub>*n*) | \(\frac{ az^{-1} \sin(\omega_0) }{ 1-2az^{-1}\cos(\omega_0)+ a^2 z^{-2} }\)     | \(|z| > |a|\) |

## 関連項目

  - [LTIシステム理論](../Page/LTIシステム理論.md "wikilink")
  - [フーリエ変換](../Page/フーリエ変換.md "wikilink") - [ラプラス変換](https://ja.wikipedia.org/wiki/ラプラス変換 "wikilink")
  - [デジタルフィルタ](https://ja.wikipedia.org/wiki/デジタルフィルタ "wikilink")

[Category:解析学](https://ja.wikipedia.org/wiki/Category:解析学 "wikilink") [Category:信号処理](https://ja.wikipedia.org/wiki/Category:信号処理 "wikilink") [Category:変換_(数学)](https://ja.wikipedia.org/wiki/Category:変換_\(数学\) "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")