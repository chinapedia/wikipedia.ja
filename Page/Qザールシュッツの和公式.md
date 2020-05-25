> この記事は[Qザールシュッツの和公式](https://ja.wikipedia.org/wiki/Qザールシュッツの和公式)から翻訳されています。


**qザールシュッツの和公式**(q-Saalschütz summation formula)はザールシュッツの定理の[q-類似](https://ja.wikipedia.org/wiki/q-類似 "wikilink")であり、[q超幾何級数](https://ja.wikipedia.org/wiki/q超幾何級数 "wikilink")\({_3\phi_2}\)の和を与える公式である\[1\]。

\[{_3\phi_2}\left[\begin{matrix}a,b,q^{-n}\\c,\frac{ab}{c}q^{-n+1}\end{matrix};q,q\right]=\frac{(\frac{c}{a};q)_n(\frac{c}{b};q)_n}{(\frac{c}{ab};q)_n(c;q)_n}\] 但し、\((a;q)_n\)は[qポッホハマー記号](https://ja.wikipedia.org/wiki/qポッホハマー記号 "wikilink")である。

## 証明

qザールシュッツの和公式は[ハイネの変換式](https://ja.wikipedia.org/wiki/ハイネの変換式 "wikilink")から導かれる。ハイネの変換式を反復すると

\[\begin{align}{_2\phi_1}\left[\begin{matrix}a,b\\c\end{matrix};q,z\right]
&=\frac{(b;q)_\infty(az;q)_\infty}{(c;q)_\infty(z;q)_\infty}
{_2\phi_1}\left[\begin{matrix}z,\frac{c}{b}\\az\end{matrix};q,b\right]\\
&=\frac{(b;q)_\infty(az;q)_\infty}{(c;q)_\infty(z;q)_\infty}\cdot
\frac{(\frac{b}{c};q)_\infty(bz;q)_\infty}{(az;q)_\infty(b;q)_\infty}
{_2\phi_1}\left[\begin{matrix}b,\frac{abz}{c}\\bz\end{matrix};q,\frac{c}{b}\right]\\
&=\frac{(b;q)_\infty(az;q)_\infty}{(c;q)_\infty(z;q)_\infty}\cdot
\frac{(\frac{b}{c};q)_\infty(bz;q)_\infty}{(az;q)_\infty(b;q)_\infty}\cdot
\frac{(\frac{abz}{c};q)_\infty(c;q)_\infty}{(bz;q)_\infty(\frac{c}{b};q)_\infty}
{_2\phi_1}\left[\begin{matrix}\frac{c}{b},\frac{c}{a}\\c\end{matrix};q,\frac{abz}{c}\right]\\
&={_2\phi_1}\left[\begin{matrix}\frac{c}{a},\frac{c}{b}\\c\end{matrix};q,\frac{abz}{c}\right]\frac{(\frac{abz}{c};q)_\infty}{(z;q)_\infty}\\
\end{align}\] となり、[q二項定理](https://ja.wikipedia.org/wiki/q二項定理 "wikilink")を用いて

\[\begin{align}{_2\phi_1}\sum_{n=0}^{\infty}\frac{(a;q)_n(b;q)_n}{(q;q)_n(c;q)_n}z^n
&=\sum_{m=0}^{\infty}\frac{(\frac{c}{a};q)_m(\frac{c}{b};q)_m}{(q;q)_m(c;q)_m}\left(\frac{abz}{c}\right)^m\sum_{k=0}^{\infty}\frac{(\frac{ab}{c};q)_k}{(q;q)_k}z^k\\
\end{align}\] となる。\(z^n\)の係数を比べると

\[\begin{align}\frac{(a;q)_n(b;q)_n}{(q;q)_n(c;q)_n}
&=\sum_{m=0}^{\infty}\frac{(\frac{c}{a};q)_m(\frac{c}{b};q)_m}{(q;q)_m(c;q)_m}\left(\frac{ab}{c}\right)^m\frac{(\frac{ab}{c};q)_{n-m}}{(q;q)_{n-m}}\\
&=\sum_{m=0}^{\infty}\frac{(\frac{c}{a};q)_m(\frac{c}{b};q)_m}{(q;q)_m(c;q)_m}\left(\frac{ab}{c}\right)^m\frac{(\frac{ab}{c};q)_n(q^{1+n-m};q)_{m}}{(q;q)_n(\frac{ab}{c}q^{n-m};q)_{m}}
\end{align}\] であるが、[qポッホハマー記号の変換式](https://ja.wikipedia.org/wiki/qポッホハマー記号#変換式 "wikilink")\((aq^{-m+1};q)_m=(-a)^mq^{-m(m-1)/2}\left(a^{-1};q\right)_m\)を用いて、

\[\begin{align}
&\frac{(a;q)_n(b;q)_n}{(q;q)_n(c;q)_n}=\sum_{m=0}^{\infty}\frac{(\frac{c}{a};q)_m(\frac{c}{b};q)_m}{(q;q)_m(c;q)_m}\frac{(\frac{ab}{c};q)_n(q^{-n};q)_{m}}{(q;q)_n(\frac{c}{ab}q^{-n+1};q)_{m}}q^m\\
&\frac{(a;q)_n(b;q)_n}{(\frac{ab}{c};q)_n(c;q)_n}=\sum_{m=0}^{\infty}\frac{(\frac{c}{a};q)_m(\frac{c}{b};q)_m}{(q;q)_m(c;q)_m}\frac{(q^{-n};q)_{m}}{(\frac{c}{ab}q^{-n+1};q)_{m}}q^m
={_3\phi_2}\left[\begin{matrix}\frac{c}{a},\frac{c}{b},q^{-n}\\c,\frac{c}{ab}q^{-n+1}\end{matrix};q,q\right]
\end{align}\] を得る。\(a,b\)を\(\tfrac{c}{a},\tfrac{c}{b}\)に置き換えて

\[{_3\phi_2}\left[\begin{matrix}a,b,q^{-n}\\c,\frac{ab}{c}q^{-n+1}\end{matrix};q,q\right]=\frac{(\frac{c}{a};q)_n(\frac{c}{b};q)_n}{(\frac{c}{ab};q)_n(c;q)_n}\] を得る。

## 出典

<references/>

[Category:q-解析学](https://ja.wikipedia.org/wiki/Category:q-解析学 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.  [Wolfram Mathworld: q-Saalschütz Sum](http://mathworld.wolfram.com/q-SaalschuetzSum.html)