> この記事は[Rabin暗号](https://ja.wikipedia.org/wiki/Rabin暗号)から翻訳されています。


**Rabin暗号**（[:en:Rabin cryptosystem](https://ja.wikipedia.org/wiki/:en:Rabin_cryptosystem "wikilink")）とは、1979年に[マイケル・ラビン](../Page/マイケル・ラビン.md "wikilink")が発表した[公開鍵暗号](../Page/公開鍵暗号.md "wikilink")である。[選択平文攻撃](https://ja.wikipedia.org/wiki/選択平文攻撃 "wikilink")で解読することと[素因数分解](../Page/素因数分解.md "wikilink")問題を解くことが等価であることが証明された初の暗号である。

## 概要

Rabin暗号は[1979年](../Page/1979年.md "wikilink")、[マイケル・ラビン](../Page/マイケル・ラビン.md "wikilink")により発明された。この暗号は[RSA暗号](../Page/RSA暗号.md "wikilink")と同じく、大きな[合成数](../Page/合成数.md "wikilink")の[素因数分解](../Page/素因数分解.md "wikilink")の困難さを安全性の根拠とした暗号方式である。

この暗号は、鍵となる合成数が素因数分解できない限り、少なくとも[選択平文攻撃](https://ja.wikipedia.org/wiki/選択平文攻撃 "wikilink")による[解読に対して理論的に](../Page/暗号解読.md "wikilink")「安全である」と証明されている。しかしながら[選択暗号文攻撃](https://ja.wikipedia.org/wiki/選択暗号文攻撃 "wikilink")に対しては全く安全でないことも証明できる。そのため、証明可能安全性を有するという意味で[暗号理論](../Page/暗号理論.md "wikilink")的な意義は大きいが、そのまま使用することは推奨されない。

## 暗号方式

Rabin暗号は、以下の3つのアルゴリズム（鍵生成、暗号化、復号）で定義される。

### 鍵生成

まず 2つの異なる[素数](../Page/素数.md "wikilink") *p* と *q* を用意しその[積](https://ja.wikipedia.org/wiki/積 "wikilink")を *n* と置く。 そして 0 ≤ B ≤ n-1 の B を選び、これと *n* を[公開鍵](https://ja.wikipedia.org/wiki/公開鍵 "wikilink")（暗号化鍵）とし、*p,q* を[秘密鍵](https://ja.wikipedia.org/wiki/秘密鍵 "wikilink")（復号鍵）とする。

このとき *p* ≡ *q* ≡ 3 (mod 4) となるように *p,q* を選ぶ（*n* を[ブラム数](../Page/ブラム数.md "wikilink")とする）と復号処理が簡易化される。以下、*n* はブラム数とする。また、B は単純に 0 とすることもできるため、B を省略する場合もある。

### 暗号化

暗号化は以下のように行われる。平文を *x* とする。

\[e(x) = x(x + B)\ \bmod \ n\]

### 復号

一方、復号は次のように行われる。暗号文を *y* とすると、次の2つの[連立方程式](https://ja.wikipedia.org/wiki/連立方程式 "wikilink")の解 *x* が求める平文である。このとき、暗号化は[単射](../Page/単射.md "wikilink")ではなく、そのため復号の際に一意に平文を求めることができないことに注意を要する。

  -
    \(x^2 + Bx - y = 0  \pmod p\)
    \(x^2 + Bx - y = 0  \pmod q\)

上記の方程式には4つの解が求まるが、4個の解から正しい平文を特定することはできない。正しい平文が求められるには、平文に十分な[冗長度](https://ja.wikipedia.org/wiki/冗長度 "wikilink")を持たせる等の条件が必要となる。具体的には、

  -
    \(x_p = {\left(y+\frac{B^2}{4}\right)}^{(p+1)/4} - \frac{B}{2} \ \bmod \ p\)
    \(x_q = {\left(y+\frac{B^2}{4}\right)}^{(q+1)/4} - \frac{B}{2} \ \bmod \ q\)

とすると、求める解 *x* は、(a,b) in { \((x_p, x_q)\), \((p-B-x_p, x_q)\), \((x_p, q-B-x_q)\), \((p-B-x_p, q-B-x_q)\) }の4組を[中国の剰余定理](../Page/中国の剰余定理.md "wikilink")により、x=a mod p, x=b mod qとして求める。

## 安全性

Rabin暗号の解読問題は、次のように素因数分解問題へ帰着できることが示せる。 ある平文 *x1* に対応する暗号文 *y1* を与えられたときに、

  -
    \(x^2 + Bx - y1 = 0  \pmod n\)

を満たす *x* を求めることができた場合、3/4 の確率で *x1* とは異なる値 *x2* が得られる。そのとき、無視できない確率で GCD(|x1+x2+B|,n) = p または q となる。

## 参考文献

  - Michael Rabin, "Digitalized Signatures and Public-Key Functions as Intractable as Factorization", MIT Laboratory for Computer Science, January 1979. [(in PDF)](http://www.lcs.mit.edu/publications/pubs/pdf/MIT-LCS-TR-212.pdf).

## 関連項目

  - [公開鍵暗号](../Page/公開鍵暗号.md "wikilink")
  - [暗号](../Page/暗号.md "wikilink")

[Category:暗号](https://ja.wikipedia.org/wiki/Category:暗号 "wikilink") [Category:エポニム](https://ja.wikipedia.org/wiki/Category:エポニム "wikilink")