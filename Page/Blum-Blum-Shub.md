> この記事は[Blum-Blum-Shub](https://ja.wikipedia.org/wiki/Blum-Blum-Shub)から翻訳されています。


**Blum-Blum-Shub**（**B.B.S.**）は、[マヌエル・ブラム](https://ja.wikipedia.org/wiki/マヌエル・ブラム "wikilink")とLenore BlumとMichael Shubが提案した[暗号論的擬似乱数生成器](../Page/暗号論的擬似乱数生成器.md "wikilink")である。1986年に発表された (Blum et al, 1986)。

漸化式は次のような形をしている。

  -
    *x*<sub>*n*+1</sub> = (*x<sub>n</sub>*)<sup>2</sup> [mod](https://ja.wikipedia.org/wiki/合同式 "wikilink") *M*

ここで *M=pq* は2つの[素数](../Page/素数.md "wikilink") *p* と *q* の積である。アルゴリズムの各ステップにおいて、*x*<sub>*n*</sub> から何らかの出力が得られる。この出力は一般に *x*<sub>*n*</sub> の[ビットパリティを使うか](https://ja.wikipedia.org/wiki/パリティビット "wikilink")、または *x*<sub>*n*</sub> の1ビット以上の最下位ビット列を使う。

2つの素数 *p* と *q* は共に、(mod 4 で）3 と[合同で](../Page/合同関係.md "wikilink")（このとき、それぞれの[平方剰余](https://ja.wikipedia.org/wiki/平方剰余 "wikilink")数の4つの[平方根](../Page/平方根.md "wikilink")のうち、平方剰余であるものがちょうど一つである）、かつ [gcd](../Page/最大公約数.md "wikilink")([φ](../Page/オイラーのφ関数.md "wikilink")(*p*-1), φ(*q*-1)) が小さいのが望ましい（これにより、反復周期が長くなる）。

Blum-Blum-Shub の興味深い性質として、任意の *x*<sub>*i*</sub> の値を次のように直接計算することができる。

\[x_i = \left( x_0^{2^i \bmod (p-1)(q-1)} \right) \bmod M\]

## セキュリティ

[暗号論的擬似乱数生成器](../Page/暗号論的擬似乱数生成器.md "wikilink")であるため、[情報セキュリティ](https://ja.wikipedia.org/wiki/情報セキュリティ "wikilink")や[暗号](../Page/暗号.md "wikilink")目的で使われる。計算量的に不利なためシミュレーションなどには向かない。セキュリティ目的での強度としては、[素因数分解](../Page/素因数分解.md "wikilink")の[複雑さを利用した暗号の品質に匹敵する](https://ja.wikipedia.org/wiki/計算複雑性理論 "wikilink")。適切な素数を選べば、各 *x<sub>n</sub>* の [O](../Page/ランダウの記号.md "wikilink")([log](../Page/対数.md "wikilink") log *M*) ビットの下位ビット列が出力となり、*M* を無限大に近づけると、そのビット列と[乱数](https://ja.wikipedia.org/wiki/乱数 "wikilink")を見分けることは、*M* を素因数分解するのと同程度かそれ以上に困難となる。

[素因数分解](../Page/素因数分解.md "wikilink")が困難であれば、十分に大きな *M* の B.B.S. の出力から、ランダムでないパターンを適切な量の計算で検出することはできない。このため、[RSA暗号](../Page/RSA暗号.md "wikilink")のような素因数分解問題を利用した暗号技術と同程度に安全とされている。

### 周期に関する注意点

gcd(φ(p-1), φ(q-1))=2を満たすような素数の組*p*、*q*であっても、短い周期を持つことがある。

例えば、*p=839*、*q=5119139*の場合ではその周期は最長で129124380となるのに対し、*p=887*、*q=4842091*の場合では、*M=pq*の値がほとんど同じであるにもかかわらず、その周期は最長でも437580となる。

## 例

*p=11*、*q=19*、*s=3* とする。gcd(φ(*p*-1), φ(*q*-1))=2 であるため、生成される擬似乱数列が反復する周期は長いことが期待できる。*x* <sub>-1</sub>=*s* として *x*<sub>0</sub> を求めるところから始め、*x*<sub>0</sub>, *x*<sub>1</sub>, *x*<sub>2</sub>, ... *x*<sub>5</sub>= 9, 81, 82, 36, 42, 92 という数列が得られる。最下位ビットを出力とする場合、出力されるビット列は 1 1 0 0 0 0 となる。

## 参考文献

  - Lenore Blum, Manuel Blum, and Michael Shub. "A Simple Unpredictable Pseudo-Random Number Generator", *SIAM Journal on Computing*, volume 15, pages 364–383, May 1986.
  - Lenore Blum, Manuel Blum, and Michael Shub. "Comparison of two pseudo-random number generators", *Advances in Cryptology: Proceedings of Crypto '82*. [PDF](http://dsns.csie.nctu.edu.tw/research/crypto/HTML/PDF/C82/61.PDF)形式
  - Martin Geisler, Mikkel Krøigård, and Andreas Danielsen. "About Random Bits", December 2004. [PDF](http://daimi.au.dk/~mg/mamian/random-bits.pdf)形式、[Gzipped Postscript](http://daimi.au.dk/~mg/mamian/random-bits.ps.gz)形式

## 外部リンク

  - [GMPBBS](http://firefly.is-a-geek.org/gmpbbs/) - [GMPベースの](https://ja.wikipedia.org/wiki/GNU_Multi-Precision_Library "wikilink") Blum-Blum-Shub の実装
  - [Javaでの実装例](http://code.google.com/p/javarng/)
  - [Randomness tests](http://www.ciphersbyritter.com/NEWS2/TESTSBBS.HTM)

[Category:乱数](https://ja.wikipedia.org/wiki/Category:乱数 "wikilink")