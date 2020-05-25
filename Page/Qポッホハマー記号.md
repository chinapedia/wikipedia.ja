> この記事は[Qポッホハマー記号](https://ja.wikipedia.org/wiki/Qポッホハマー記号)から翻訳されています。


数学において、**qポッホハマー記号**()は[q-類似](https://ja.wikipedia.org/wiki/q-類似 "wikilink")の数式に頻出する乗積を略記する記号である\[1\]\[2\]\[3\]。

  -
    <math>\\begin{align}

&(a;q)_\\infty:=\\prod_{k=0}^{\\infty}(1-aq^k)\\\\ &(a;q)_n:=\\frac{(a;q)_\\infty}{(aq^n;q)_\\infty}\\\\ \\end{align}</math> \(|q|<1\)の仮定が普通であり、実用上、\(n\)は[整数](../Page/整数.md "wikilink")であることが多い。\(n\)が整数である場合は

  -
    <math>(a;q)_n=\\begin{cases}

\\displaystyle\\prod_{k=0}^{n-1}(1-aq^k)\&n\>0\\\\ 1\&n=0\\\\ \\displaystyle\\prod_{k=n}^{-1}\\frac{1}{(1-aq^k)}\&n\<0\\\\ \\end{cases}</math> となる。\(m,n\)が整数であり、\(a=q^{-m}\)であるとき、\(0{\le}m<n\)であれば\((q^{-m};q)_n=0\)であり、\(n{\le}m<0\)であれば\((q^{-m};q)_n\)である。

## 更なる略記

基底 () が文字\(q\)である場合は省略することがある。

  -
    <math>\\begin{align}

&(a)_n=(a;q)_n\\\\ &(q)_n=(q;q)_n\\\\ \\end{align}</math> 複数のqポッホハマー記号が並ぶときは合成することがある。

  -
    <math>\\begin{align}

&(a,b,c)_n=(a,b,c;q)_n:=(a;q)_n(b;q)_n(c;q)_n\\\\ \\end{align}</math>

## 変換式

以下の変換式が成立する。

\[\begin{align}(aq^{-n+1};q)_n
&=\prod_{k=0}^{n-1}(1-aq^{-n+1+k})\\
&=(-a)^nq^{-n(n-1)/2}\prod_{k=0}^{n-1}\left(1-\frac{q^{n-1-k}}{a}\right)\\
&=(-a)^nq^{-n(n-1)/2}\prod_{k=0}^{n-1}\left(1-\frac{q^{k}}{a}\right)\qquad(n-1-k{\mapsto}n)\\
&=(-a)^nq^{-n(n-1)/2}\left(\dfrac{1}{a};q\right)_n
\end{align}\]

## qブラケット

qブラケット () は整数、実数、複素数などの[q-類似](https://ja.wikipedia.org/wiki/q-類似 "wikilink")を表す記号である\[4\]。

\[[n]=[n]_q:=\frac{1-q^n}{1-q}=\sum_{k=0}^{n-1}q^k.\]

## q階乗

q階乗 () は[階乗](../Page/階乗.md "wikilink")の[q-類似](https://ja.wikipedia.org/wiki/q-類似 "wikilink")である\[5\]\[6\]。（分母は普通の冪乗であることを為念）

  -
    \([n]_q!:=\prod_{k=1}^{n}[k]_q=\frac{(q;q)_n}{(1-q)^n}.\)

## q二項係数

q二項係数 () は二項係数の[q-類似](https://ja.wikipedia.org/wiki/q-類似 "wikilink")である\[7\]\[8\]。

  -
    \(\begin{bmatrix}n\\k\end{bmatrix}_q:=\frac{[n]_q!}{[n-k]_q![k]_q!}=\frac{(q;q)_n}{(q;q)_{n-k}(q;q)_k}.\)

## 出典

<references/>

## 関連項目

  - [:en:q-gamma function](https://ja.wikipedia.org/wiki/:en:q-gamma_function "wikilink")
  - [:en:Jackson's q-Bessel function](https://ja.wikipedia.org/wiki/:en:Jackson's_q-Bessel_function "wikilink")
  - [:en:Hahn-Exton q-Bessel function](https://ja.wikipedia.org/wiki/:en:Hahn-Exton_q-Bessel_function "wikilink")

[Category:数学の表記法](https://ja.wikipedia.org/wiki/Category:数学の表記法 "wikilink") [Category:q-解析学](https://ja.wikipedia.org/wiki/Category:q-解析学 "wikilink") [Category:特殊関数](https://ja.wikipedia.org/wiki/Category:特殊関数 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.  [Wolfram Mathworld: q-Pochhammer Symbol](http://mathworld.wolfram.com/q-PochhammerSymbol.html)
2.  Andrews, G. E., Askey, R., & Roy, R. (2000). Special functions. Cambridge university press.
3.  Gasper, G., Rahman, M. (2004). Basic hypergeometric series. Cambridge university press.
4.  [Wolfram Mathworld: q-Bracket](http://mathworld.wolfram.com/q-Bracket.html)
5.
6.  [Wolfram Mathworld: q-Factorial](http://mathworld.wolfram.com/q-Factorial.html)
7.
8.  [Wolfram Mathworld: q-Binomial Coefficient](http://mathworld.wolfram.com/q-BinomialCoefficient.html)