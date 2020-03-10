> この記事は[Q](https://ja.wikipedia.org/wiki/Q)から翻訳されています。


数学において、**q二項定理**（）は[二項定理](../Page/二項定理.md "wikilink")の[q-類似](https://ja.wikipedia.org/wiki/q-類似 "wikilink")である\[1\]。[超幾何級数](https://ja.wikipedia.org/wiki/超幾何級数 "wikilink") \(_1F_0\)の和は通常の[二項定理](../Page/二項定理.md "wikilink")

  -
    \(_1F_0(a;z)=F(a,b,b;z)=\sum_{n=0}^{\infty}\frac{(a)_n}{(1)_n}z^n=(1-z)^{-a}\qquad(|z|<1)\)

で与えられる。これに倣い、[q超幾何級数](https://ja.wikipedia.org/wiki/q超幾何級数 "wikilink")\(_1\phi_0\)の和を与える公式

  -
    \(_1\phi_0\left[\begin{matrix}a\\-\end{matrix};q,z\right]=\sum_{n=0}^{\infty}\frac{(a;q)_n}{(q;q)_n}z^n=\frac{(az;q)_\infty}{(z;q)_\infty}\qquad(|q|<1,|z|<1)\)

をq二項定理と呼ぶ。ただし、\((a)_n\)は[ポッホハマー記号](https://ja.wikipedia.org/wiki/ポッホハマー記号 "wikilink")、\((a;q)_n\)は[qポッホハマー記号](https://ja.wikipedia.org/wiki/qポッホハマー記号 "wikilink")である。

## 証明

右辺を\(\ f(a,z;q)\)として[関数方程式](https://ja.wikipedia.org/wiki/関数方程式 "wikilink")を導く。

  -
    <math>\\begin{align}(1-z)f(a,z;q)

&=(1-z)\\sum_{n=0}^{\\infty}\\frac{(a;q)_n}{(q;q)_n}z^n\\\\ &=\\left(1+\\sum_{n=1}^{\\infty}\\frac{(a;q)_n}{(q;q)_n}z^n\\right)-z\\sum_{n=0}^{\\infty}\\frac{(a;q)_n}{(q;q)_n}z^n\\\\ &=1+\\sum_{n=1}^{\\infty}\\left(\\frac{(a;q)_n}{(q;q)_n}z^n-z\\frac{(a;q)_{n-1}}{(q;q)_{n-1}}z^{n-1}\\right)\\\\ &=1+\\sum_{n=1}^{\\infty}\\frac{(a;q)_{n-1}}{(q;q)_n}\\left((1-aq^{n-1})z^n-(1-q^n)z^n\\right)\\\\ &=1+\\sum_{n=1}^{\\infty}\\frac{(a;q)_{n-1}}{(q;q)_n}\\left((1-aq^{n-1})q^nz^n-a(1-q^n)q^{n-1}z^n\\right)\\\\ &=1+\\sum_{n=1}^{\\infty}\\left(\\frac{(a;q)_n}{(q;q)_n}(qz)^n-az\\frac{(a;q)_{n-1}}{(q;q)_{n-1}}(qz)^{n-1}\\right)\\\\ &=\\left(1+\\sum_{n=1}^{\\infty}\\frac{(a;q)_n}{(q;q)_n}(qz)^n\\right)-az\\sum_{n=0}^{\\infty}\\frac{(a;q)_n}{(q;q)_n}(qz)^n\\\\ &=(1-az)\\sum_{n=0}^{\\infty}\\frac{(a;q)_n}{(q;q)_n}(qz)^n\\\\ &=(1-az)f(a,qz;q) \\end{align}</math> これにより、左辺を得る。

  -
    <math>\\begin{align}f(a,z;q)

&=\\frac{1-az}{1-z}f(a,qz;q)\\\\ &=\\lim_{n\\to\\infty}\\frac{(1-az)_n}{(1-z)_n}f(a,q^nz;q)\\\\ &=\\frac{(1-az)_\\infty}{(1-z)_\\infty}f(a,0;q)\\\\ &=\\frac{(1-az)_\\infty}{(1-z)_\\infty}\\\\ \\end{align}</math>

## 別証明

左辺を\(\ g(a,z;q)\)として[関数方程式](https://ja.wikipedia.org/wiki/関数方程式 "wikilink")を導く。

  -
    <math>\\begin{align}(1-z)g(a,z;q)

&=(1-z)\\prod_{n=0}^{\\infty}\\frac{1-azq^n}{1-zq^n}\\\\ &=(1-z)\\frac{1-az}{1-z}\\prod_{n=1}^{\\infty}\\frac{1-azq^n}{1-zq^n}\\\\ &=(1-az)\\prod_{n=0}^{\\infty}\\frac{1-aqzq^n}{1-qzq^n}\\\\ &=(1-az)g(a,qz;q)\\\\ \\end{align}</math> \(g(a,z;q)\)を[テイラー級数](https://ja.wikipedia.org/wiki/テイラー級数 "wikilink")に展開して\(z^n\)の係数を比較すると

  -
    <math>\\begin{align}

\&g(a,qz;q)=\\sum_{n=0}^{\\infty}c_nz^n\\\\ &(1-z)\\sum_{n=0}^{\\infty}c_nz^n=(1-az)\\sum_{n=0}^{\\infty}c_n(qz)^n\\\\ &1+\\sum_{n=1}^{\\infty}(c_n-c_{n-1})z^n=1+\\sum_{n=1}^{\\infty}(c_n-ac_{n1})(qz)^n\\\\ \&c_n-c_{n-1}=c_nq^n-ac_{n-1}q^{n-1}\\\\ \&c_n=\\frac{1-aq^{n-1}}{1-q^n}c_{n-1}\\\\ \\end{align}</math> となり、\(c_0=1\)であるから

  -
    \(c_n=\frac{(a;q)_n}{(q;q)_n}\)

となる。これにより、右辺を得る。

  -
    \(g(a,z;q)=\sum_{n=0}^{\infty}c_nz^n=\sum_{n=0}^{\infty}\frac{(a;q)_n}{(q;q)_n}z^n\)

## コーシーの二項定理

コーシーの二項定理はq二項定理の特殊な場合である\[2\]。

  -
    \(\sum_{n=0}^{N}y^nq^{n(n+1)/2}\begin{bmatrix}N\\n\end{bmatrix}_q=\prod_{k=1}^{N}\left(1+yq^k\right)\qquad(|q|<1)\)

ただし、

  -
    \(\begin{bmatrix}N\\n\end{bmatrix}_q\)

はq二項係数である。q二項定理に\(a=q^{-N},z=-q^{N+1}y\)を代入すると

  -
    \(\sum_{n=0}^{\infty}\frac{(q^{-N};q)_n}{(q;q)_n}(-q^{N+1}y)^n=\frac{(-qy;q)_\infty}{(-q^{N+1}y;q)_\infty}=\prod_{k=0}^{\infty}\frac{1+yq^{1+k}}{1+yq^{N+1+k}}\)

となるが、左辺は\(n>N\)で\((q^{-N};q)_n=0\)となり、右辺は\(k{\ge}N\)の分子が\(k-N\)の分母を打ち消す。従って、

  -
    \(\sum_{n=0}^{N}\frac{(q^{-N};q)_n}{(q;q)_n}(-q^{N+1}y)^n=\prod_{k=0}^{N-1}\frac{1+yq^{1+k}}{1+yq^{N+1+k}}=\prod_{k=1}^{N}\left(1+yq^{k}\right)\)

である。左辺は[qポッホハマー記号の変換式](https://ja.wikipedia.org/wiki/qポッホハマー記号#変換式 "wikilink")\((aq^{-n+1};q)_n=(-a)^nq^{-n(n-1)/2}\left(a^{-1};q\right)_n\)により、

  -
    <math>\\begin{align}\\sum_{n=0}^{\\infty}\\frac{(q^{-N};q)_n}{(q;q)_n}(-q^{N+1}y)^n

&=\\sum_{n=0}^{\\infty}\\frac{(q^{-N+n-1}q^{-n+1};q)_n}{(q;q)_n}(-1)^nq^{n(N+1)}y^n\\\\ &=\\sum_{n=0}^{\\infty}\\frac{(-q^{-N+n-1})^nq^{-n(n-1)/2}(q^{N-n+1};q)_n}{(q;q)_n}(-1)^nq^{n(N+1)}y^n\\\\ &=\\sum_{n=0}^{\\infty}\\frac{(-1)^nq^{-n(N+1)}q^{n(n+1)/2}(q^{N-n+1};q)_n}{(q;q)_n}(-1)^nq^{n(N+1)}y^n\\\\ &=\\sum_{n=0}^{\\infty}\\frac{y^nq^{n(n+1)/2}(q^{N-n+1};q)_n}{(q;q)_n}\\\\ &=\\sum_{n=0}^{\\infty}\\frac{y^nq^{n(n+1)/2}(q;q)_N}{(q;q)_{N-n}(q;q)_n}\\\\ &=\\sum_{n=0}^{N}y^nq^{n(n+1)/2}\\begin{bmatrix}N\\\\n\\end{bmatrix}_q\\\\ \\end{align}</math> となる。

## 出典

<references/>

[Category:q-解析学](https://ja.wikipedia.org/wiki/Category:q-解析学 "wikilink") [Category:解析学の定理](https://ja.wikipedia.org/wiki/Category:解析学の定理 "wikilink") [Category:複素解析](https://ja.wikipedia.org/wiki/Category:複素解析 "wikilink") [Category:数論](https://ja.wikipedia.org/wiki/Category:数論 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.  [Wolfram Mathworld: q-Binomial Theorem](http://mathworld.wolfram.com/q-BinomialTheorem.html)
2.  [Wolfram Mathworld: Cauchy Binomial Theorem](http://mathworld.wolfram.com/CauchyBinomialTheorem.html)