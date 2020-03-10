> この記事は[Q](https://ja.wikipedia.org/wiki/Q)から翻訳されています。


数学において、**超幾何級数**（ちょうきかきゅうすう、）は[超幾何級数](https://ja.wikipedia.org/wiki/超幾何級数 "wikilink")の[{{mvarである](https://ja.wikipedia.org/wiki/q-類似 "wikilink")。超幾何級数は

\[\begin{align}
{}_r\phi_s \left[ \begin{matrix} a_1, a_2, \dotsc, a_r \\ b_1, b_2, \dotsc, b_s \end{matrix}; q, z \right] &= \sum_{n=0}^{\infty} \frac{(a_1, a_2, \dotsc, a_r;q)_n}{(b_1, b_2, \dotsc, b_s, q;q)_n} \left((-1)^nq^\binom{n}{2}\right)^{s+1-r} z^n \\
{}_r\psi_s \left[ \begin{matrix} a_1, a_2, \dotsc, a_r \\ b_1, b_2, \dotsc, b_s \end{matrix}; q, z \right] &= \sum_{n=-\infty}^{\infty} \frac{(a_1, a_2, \dotsc, a_r;q)_n}{(b_1, b_2, \dotsc, b_s;q)_n} \left((-1)^nq^\binom{n}{2}\right)^{s-r} z^n \\
\end{align}\] の形式で表される[級数](../Page/級数.md "wikilink")である\[1\]。中でも

\[\begin{align}
{}_r\phi_{r-1} \left[ \begin{matrix} a_1, a_2, \dotsc, a_r \\ b_1, b_2, \dotsc, b_{r-1} \end{matrix}; q, z \right] &= \sum_{n=0}^{\infty} \frac{(a_1, a_2, \dotsc, a_r;q)_n}{(b_1, b_2, \dotsc, b_{r-1}, q;q)_n} z^n \\
{}_r\psi_r \left[ \begin{matrix} a_1, a_2, \dotsb, a_r \\ b_1, b_2, \dotsb, b_{r} \end{matrix}; q, z \right] &= \sum_{n=-\infty}^{\infty} \frac{(a_1, a_2, \dotsc, a_r;q)_n}{(b_1, b_2, \dotsc, b_r;q)_n} z^n \\
\end{align}\] が多く研究されている。但し、

\[(a_1, a_2, \dotsc, a_r; q)_n = (a_1; q)_n (a_2; q)_n \dotsm (a_r; q)_n\] であり、ここで

  -
    <math>

(a;q)_n = \\begin{cases} \\prod_{0 \\le k \< n} (1-aq^k) & (n \> 0) \\\\ 1 & (n = 0) \\\\ \\prod_{n \\le k \< 0}(1 - aq^k)^{-1} & (n \< 0) \\end{cases} </math> は[{{mvarである](https://ja.wikipedia.org/wiki/qポッホハマー記号 "wikilink")。なお、厳密にいうと、右辺の級数が超幾何級数であり、左辺の記号は級数の和によって定義される超幾何関数を表すものである。

## 関連記事

  - [{{mvar](https://ja.wikipedia.org/wiki/q二項定理 "wikilink")
  - [ハイネの和公式](https://ja.wikipedia.org/wiki/ハイネの和公式 "wikilink")
  - [ラマヌジャンの和公式](https://ja.wikipedia.org/wiki/ラマヌジャンの和公式 "wikilink")
  - [{{mvar](https://ja.wikipedia.org/wiki/qザールシュッツの和公式 "wikilink")

## 出典

<references/>

## 参考文献

  - 堀田良之・渡辺敬一・庄司俊明・[三町勝久](../Page/三町勝久.md "wikilink"): 群論の進化, 代数学百科, I, [朝倉書店](../Page/朝倉書店.md "wikilink"), 2004 年, ISBN 4-254-11099-5
  - Gasper, G., Rahman, M. (2004). Basic hypergeometric series. [:en:Cambridge university press](https://ja.wikipedia.org/wiki/:en:Cambridge_university_press "wikilink").
  - Andrews, G. E., Askey, R., & Roy, R. (1999). Special functions. [:en:Cambridge university press](https://ja.wikipedia.org/wiki/:en:Cambridge_university_press "wikilink").

[Category:離散数学](https://ja.wikipedia.org/wiki/Category:離散数学 "wikilink") [Category:特殊関数](https://ja.wikipedia.org/wiki/Category:特殊関数 "wikilink") [Category:微分方程式](https://ja.wikipedia.org/wiki/Category:微分方程式 "wikilink") [Category:級数](https://ja.wikipedia.org/wiki/Category:級数 "wikilink") [Category:q-解析学](https://ja.wikipedia.org/wiki/Category:q-解析学 "wikilink") [Category:数論](https://ja.wikipedia.org/wiki/Category:数論 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.  [Wolfram Mathworld: q-Hypergeometric Function](http://mathworld.wolfram.com/q-HypergeometricFunction.html)