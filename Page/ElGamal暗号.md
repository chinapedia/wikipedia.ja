> この記事は[ElGamal暗号](https://ja.wikipedia.org/wiki/ElGamal暗号)から翻訳されています。


**ElGamal暗号**（エルガマルあんごう、ElGamal encryption）とは、[位数](../Page/位数.md "wikilink")が大きな群の[離散対数](../Page/離散対数.md "wikilink")問題が困難であることを安全性の根拠とした[公開鍵暗号](../Page/公開鍵暗号.md "wikilink")の一つである。1984年[Taher Elgamalが発表した](https://ja.wikipedia.org/wiki/:en:Taher_Elgamal "wikilink")。

## 概要

Diffie-Hellman鍵共有方式で共有した[乱数](https://ja.wikipedia.org/wiki/乱数 "wikilink")を使って[ワンタイムパッド](../Page/ワンタイムパッド.md "wikilink") (OTP) を行うと暗号通信ができる。ElGamal暗号は、これを利用して[Diffie-Hellman鍵共有](https://ja.wikipedia.org/wiki/Diffie-Hellman鍵共有 "wikilink")方式を暗号方式として利用できるように変形したものである。

ElGamal暗号は[暗号](../Page/暗号.md "wikilink") (cipher) であるが、これとは別に[デジタル署名](../Page/デジタル署名.md "wikilink") (digital signature) に応用することができる[ElGamal署名](https://ja.wikipedia.org/wiki/ElGamal署名 "wikilink")も発表されている。

用語については、[暗号の用語](https://ja.wikipedia.org/wiki/暗号#用語 "wikilink")、[暗号理論の用語を参照](https://ja.wikipedia.org/wiki/暗号理論#用語 "wikilink")。

## 暗号方式

\(k\) をセキュリティ・パラメータとする。

### 鍵生成

  - [巡回群](https://ja.wikipedia.org/wiki/巡回群 "wikilink")*G*で、位数*q*が[素数](../Page/素数.md "wikilink")であり、かつ \(q\) のビット数が \(k\) であるものを選ぶ。
  - *G*の[生成元](https://ja.wikipedia.org/wiki/生成元 "wikilink") \(g\) を選ぶ。
  - *x*を\(\{0,...,q-1\}\)からランダムに選ぶ。
  - \(h = g^x\)とする。
  - \((G, q, g, h)\)を公開鍵とし、*x*を秘密鍵とする。

平文空間は*G*であり、暗号文空間は*G<sup>2</sup>*である。

### 暗号化

  - *G*の元*m*を平文として受け取る。
  - *r*を\(\{0,...,q-1\}\)からランダムに選ぶ。
  - \(c_1 = g^{r}\), \(c_2 = m \cdot h^{r}\)を計算する。
  - \((c_1, c_2)\)を暗号文とする。

### 復号

受け取った暗号文を\((c_1, c_2) \in G \times G\)とする。

  - \(m = c_2 \cdot ({c_1}^x)^{-1}\)とする。

実際、もし\((c_1, c_2)\)が正しい方法で生成された暗号文であれば、\(m' = c_2 \cdot ({c_1}^x)^{-1} = m \cdot (g^x)^r \cdot ((g^r)^x)^{-1} = m\)を満たす。

## 安全性

上で"離散対数問題が困難であることを基にした"と書いたがこれは正確な表現では無い。 実際には、DLP仮定ではなく、[Computational Diffie-Hellman仮定](https://ja.wikipedia.org/wiki/Computational_Diffie-Hellman仮定 "wikilink")（CDH仮定）および[Decisional Diffie-Hellman仮定](https://ja.wikipedia.org/wiki/Decisional_Diffie-Hellman仮定 "wikilink")（DDH仮定）を基にしている。 ElGamal暗号が[選択平文攻撃](https://ja.wikipedia.org/wiki/選択平文攻撃 "wikilink")に対して完全解読できないということ（OW-CPAであるということ）と、CDH仮定とが同値である。 また、ElGamal暗号が[選択平文攻撃](https://ja.wikipedia.org/wiki/選択平文攻撃 "wikilink")のもとIndistinguishabillityをもつということ（IND-CPAであるということ）と、DDH仮定とが同値である。

ElGamal暗号は、選択暗号文攻撃に対しては安全ではない。平文\(m\)に対応する\((c_1, c_2)\)から、\(2 m\)に対応する暗号文\((c_1, 2 c_2)\)を作成することができるからである。

## 巡回群*G*について

*p*を素数とするとき、*G* = \({\mathbb Z}_p^{*}\)としてはいけない。このような群上ではDDH仮定が破れる。 主な方法は二つある。

  - 巡回群*G*を\({\mathbb Z}_p^{*}\)の部分群とする。
  - 巡回群*G*を楕円曲線上で定義する（[楕円曲線暗号](../Page/楕円曲線暗号.md "wikilink")）。

ここでは上の方法を説明する。

  - 小さな自然数*k*と大きな素数*q*に対して、素数*p*を*p = kq+1*となるように取る。
      - まず素数*q*を選んでから、*p = kq + 1*が素数かどうかを調べればよい。
  - \(g \in {\mathbb Z}_p^{*}\)を、*g*の位数が*q*となるようにランダムに選ぶ。
  - \(G = <g>\)は\({\mathbb Z}_p^{*}\)の部分群となっている。

尚、*k=2*に対して*p = 2q + 1*が成り立つ素数の組(*p,q*)が無限に存在するかどうかは未解決問題である（ソフィー・ジェルマン問題、[素数\#素数に関連する未解決の問題](https://ja.wikipedia.org/wiki/素数#素数に関連する未解決の問題 "wikilink")）。

## 参考文献

### 原論文

  - *A Public-Key Cryptosystem and a Signature Scheme Based on Discrete Logarithms*; Taher Elgamal; IEEE Transactions on Information Theory, v. IT-31, n. 4, 1985, pp. 469–472 or CRYPTO 84, pp. 10–18, Springer-Verlag.

## 関連項目

  - [暗号](../Page/暗号.md "wikilink")
  - [暗号理論](../Page/暗号理論.md "wikilink")
  - [ElGamal署名](https://ja.wikipedia.org/wiki/ElGamal署名 "wikilink")
  - [離散対数](../Page/離散対数.md "wikilink")

[Category:暗号](https://ja.wikipedia.org/wiki/Category:暗号 "wikilink")