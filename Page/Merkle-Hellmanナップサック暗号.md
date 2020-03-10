> この記事は[Merkle-Hellman](https://ja.wikipedia.org/wiki/Merkle-Hellman)から翻訳されています。


**Merkle-Hellmanナップサック暗号**とは、[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")に[ラルフ・マークル](../Page/ラルフ・マークル.md "wikilink")と[マーティン・ヘルマン](https://ja.wikipedia.org/wiki/マーティン・ヘルマン "wikilink")が発表した[ナップサック問題](../Page/ナップサック問題.md "wikilink")（正確には[部分和問題](https://ja.wikipedia.org/wiki/部分和問題 "wikilink")）を利用した[公開鍵暗号](../Page/公開鍵暗号.md "wikilink")の一つである。 この暗号方式は、秘匿用途の方式であり、認証（[デジタル署名](../Page/デジタル署名.md "wikilink")など）を目的としたものではない。

公開鍵暗号の提案は1976年であり、比較的初期に提案された方式である。 [1982年](../Page/1982年.md "wikilink")に解読方法が発見されたため、現在は使用されていない。 近年になり、鍵の生成に[量子コンピュータ](../Page/量子コンピュータ.md "wikilink")を用いることにより、量子コンピュータでも解けない暗号として機能することが示され、ふたたび注目を浴びている。

## 概要

Merkle-Hellmanナップサック暗号は[部分和問題](https://ja.wikipedia.org/wiki/部分和問題 "wikilink")（[ナップサック問題](../Page/ナップサック問題.md "wikilink")の特別なインスタンス）に基づいている。

部分和問題は、整数の列（*a*<sub>1</sub>,...,*a*<sub>n</sub>）と目標となる整数（*t*）を入力とし、\(\sum_{i\in S}a_i=t\)となる部分集合\(S \subseteq \{1,2,...,n\}\)を求める問題（*a*<sub>*i*</sub> で*t* を合成する問題）である。

一般の部分和問題は、[NP完全](https://ja.wikipedia.org/wiki/NP完全 "wikilink")であることが知られている。しかし、超増加列と呼ばれる数列を用いた場合には、簡単に解けることが分かっている。Merkle-Hellmanナップサック暗号は、合成が簡単にできる超増加列を、見かけ上は合成がむずかしい整数列に変換し、また逆に戻せることに基づいている。超増加列とは、各項がそれまでの全ての項の和よりも大きい数列のことである。

この暗号方式は発表時から安全性に疑問をもたれていたが、1982年に[アディ・シャミア](../Page/アディ・シャミア.md "wikilink") (Adi Shamir) によって一般的解読方法が発見された。これは部分和問題自体を解いたのではなく、超増加列を変換した数列を用いた場合には、どのように変換しても元の超増加という性質が残り、容易に解けることを示したものである。

シャミアの解読以降、多くのナップサック暗号の変形版が提案されているが、そのほとんどが解読可能であることが判明している。

用語については、[暗号の用語および](https://ja.wikipedia.org/wiki/暗号#用語 "wikilink")[暗号理論の用語を参照のこと](https://ja.wikipedia.org/wiki/暗号理論#用語 "wikilink")。

## 暗号方式

### 鍵生成

*n* ビットの平文を暗号化するために、まず*n* 個の数からなる超増加列  を生成する（*n* はセキュリティパラメータであり、100ビット以上の数にすることが推奨されている）。

次に、整数*q* を *q*  \> \(\sum_{i = 1}^n w_i\) を満たすようにランダムに選ぶ。 更に、整数 *r* を gcd(*r*,*q*) = 1 となるようにランダムに選ぶ。 整数*q* は、*q* の剰余を取ったときに暗号文が一意に定まるように選ばなければならない。そうしないと二つの平文から同じ暗号文が生成されることになり、復号できなくなる。また*r* は*q* と互いに素な整数でなければならない。これは復号時に*r* の逆元を使うためである。

とし、数列  を得る。

公開鍵はβ、秘密鍵は(*w*, *q*, *r* )である。

### 暗号化

*n* ビットの平文  を暗号化する。ここで、各 α<sub>*i*</sub> は第*i* ビットを表す (α<sub>*i*</sub> ∈{0,1})。

を計算し、*c* を暗号文とする。

### 復号

暗号文*c* を受け取った後、 ''c' '' = *c* *r* <sup>-1</sup> mod *q* を計算する。ここで、*r* <sup>-1</sup> は、(mod *q*) の整数の合同における *r* の逆元である。

すると、''c' '' は*w* の部分和になっている。*w* は超増加列なので、{1,2,...,n} の部分集合*S* を次のようにして簡単に求めることができる。

具体的なアルゴリズムは、次のとおりになる。

## 安全性

Merkle-Hellmanナップサック暗号は、シャミアにより多項式時間で解読できることが示されている。

### シャミアの攻撃法

シャミアの攻撃法では、公開鍵β = (β<sub>1</sub>, β<sub>2</sub>, ..., β<sub>*n*</sub>)から、超増加列''w' '' = (''w' ''<sub>*1*</sub>, ''w' ''<sub>*2*</sub>, ..., ''w' *<sub>*n*</sub>) を求める。正しい超増加列*w'' とシャミアの攻撃法で求めた''w' '' は異なることが多いが、正しく解読できる。詳しくは参考文献のAdi Shamir, "A Polynomial Time Algorithm for Breaking the Basic Merkle-Hellman Cryptosystem"を参照のこと。

### 低密度攻撃(LDA)

密度が低い場合、高確率で格子の最短ベクトルを求める問題 (最短ベクトル問題, Shortest Vector Problem, SVP) へ帰着できる。最短ベクトル問題は、ユークリッド距離ではRandomized帰着の元で[NP困難](../Page/NP困難.md "wikilink")な問題であることが知られている。また、格子の次元が低い場合、[LLLアルゴリズム](https://ja.wikipedia.org/wiki/LLLアルゴリズム "wikilink")(Lenstra, Lenstra, Lovasz, 1982)を用いて解けることが多い。

  - LO法(Lagarias, Odlyzkoにより提案) は，密度の低いナップザック問題への解法。
  - CLOS法(Coster, LaMacchia, Odlyzko,Schnorrにより提案) は，より密度の高いナップザック問題に対しても有効である改良手法。

(参考：[格子_(数学)](https://ja.wikipedia.org/wiki/格子_\(数学\) "wikilink")) (stub)

## 参考文献

  - Ralph Merkle, Martin Hellman, "Hiding Information and Signatures in Trapdoor Knapsacks", *IEEE Trans. Information Theory*, 24(5), September 1978, pp.525–530.
  - Adi Shamir, "A Polynomial Time Algorithm for Breaking the Basic Merkle-Hellman Cryptosystem", CRYPTO'82, pp.279–288, 1982. ([PDF](http://dsns.csie.nctu.edu.tw/research/crypto/HTML/PDF/C82/279.PDF))
  - J. C. Lagarias and A. M. Odlyzko： “Solving Low Density Subset Sum Problems,” J. Assoc. Comp.Math., vol.32, pp.229–246, Preliminary version in Proc. 24th IEEE, 1985
  - M. J. Coster, B. A. LaMacchia, A. M. Odlyzko and C. P. Schnorr： “An Improved Low-Density Subset Sum Algorithm,” In Advances in Cryptology Proc. EUROCRYPTO'91,LNCS, pp.54–67.Springer-Verlag, Berlin, 1991.

## 関連項目

  - [公開鍵暗号](../Page/公開鍵暗号.md "wikilink")
  - [暗号理論](../Page/暗号理論.md "wikilink")
  - [信頼性の低い暗号アルゴリズム](../Page/信頼性の低い暗号アルゴリズム.md "wikilink")
  - [Chor-Rivestナップサック暗号](https://ja.wikipedia.org/wiki/Chor-Rivestナップサック暗号 "wikilink")

[Category:暗号](https://ja.wikipedia.org/wiki/Category:暗号 "wikilink")