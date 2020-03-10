> この記事は[NTRU](https://ja.wikipedia.org/wiki/NTRU)から翻訳されています。


**NTRU暗号**とは、[公開鍵暗号](../Page/公開鍵暗号.md "wikilink")の一つである。 1996年にJeffrey Hoffstein, Jill Pipher, Joseph H. SilvermanがCRYPTO'96のRump Sessionで発表した。2000年にNTRU Cryptosystems社が米国で特許を取得している。 多項式環を用いて定義された格子の最短ベクトル問題が困難と予想されることを基にしているが、実際に帰着出来るか否かは未解決問題である。

## 暗号方式

### 鍵生成

*N* をセキュリティパラメータとする。 **Z**\[*X*\]で整数係数の[多項式](../Page/多項式.md "wikilink")環を表す。(*X*<sup>*N*</sup>-1)を*X*<sup>*N*</sup>-1が生成する[イデアル](https://ja.wikipedia.org/wiki/イデアル "wikilink")とする。 環*R*を **Z**\[*X*\]/(*X*<sup>*N*</sup>-1) とする。以下、⊗で *R* の要素の積を表す。 *q* を *O*(*N*) の整数とし、*p* を環*R*中の小さい要素とする。（2, 3, 2+*X*等が用いられる。） また, *L*<sub>*f*</sub>, *L*<sub>*g*</sub>を *R* の係数が小さい部分集合とする。

1.  *f* を *L*<sub>*f*</sub> からランダムに選ぶ。
    1.  *f* が *f* ⊗ *F*<sub>*q*</sub> ≡ 1 ([mod](https://ja.wikipedia.org/wiki/合同式 "wikilink") *q*) となる*R*中の要素 *F*<sub>*q*</sub> を持たない場合 *f* を選び直す。
    2.  同様に *f* が *f* ⊗ *F*<sub>*p*</sub> ≡ 1 (mod *p*) となる*R*中の要素 *F*<sub>*q*</sub> を持たない場合 *f* を選び直す。
2.  *g* を *L*<sub>*g*</sub> からランダムに選ぶ。
3.  *h* ≡ *F*<sub>*q*</sub> ⊗ *p* ⊗ *g* (mod *q*) とする。

公開鍵は *h*、秘密鍵は*f*である。

### 暗号化

平文空間*L*<sub>*m*</sub>、乱数空間*L*<sub>*r*</sub>を *R* の係数が小さい部分集合とする。 *L*<sub>*m*</sub>中の平文*m*と*L*<sub>*r*</sub>中の乱数*r*を用いて、*c* = *h* ⊗ *r* + *m* mod *q* を計算し、*c*を出力する。

### 復号

*c*を暗号文とする。 まず*a* = *f* ⊗ *c* mod *q* を計算する。次に、*a*の係数を\[-q/2,q/2\]の範囲に収め、それを''a' *とする。最後に、*m' '' = *F*<sub>*p*</sub> ⊗ ''a' '' mod p を計算し、''m' ''を出力する。

### 完全性について

  -
    *a* ≡ *f* ⊗ *c* ≡ *p* ⊗ *g* ⊗ *r* + *f* ⊗ *m* (mod q)

である。 上手くパラメータを調節すると、**Z**上で

  -
    ''a' '' = *p* ⊗ *g* ⊗ *r* + *f* ⊗ *m*

が高い確率で成立する。 この等式が成立している場合、

  -
    *F*<sub>*p*</sub> ⊗ ''a' '' ≡ *F*<sub>*p*</sub> ⊗ *f* ⊗ *m* ≡ *m* (mod p)

となる。

## 実装

*T*で係数が1, 0, -1の*N*-1次以下の多項式の集合を表す。 *T*(*d*)で、係数が1, 0, -1かつ、1と-1の個数が*d*の*N*-1次以下の多項式の集合を表す。 IEEE P1361.1/D10では例えば以下のようにパラメータ集合が定められている。

  - ees449ep1
    (*N*, *q*, *p*, *L*<sub>*f*</sub>, *L*<sub>*g*</sub>, *L*<sub>*r*</sub>, *L*<sub>*m*</sub>) = (449, 2048, 3, T(134), T(149), T(134), T)
  - ees853ep1
    (*N*, *q*, *p*, *L*<sub>*f*</sub>, *L*<sub>*g*</sub>, *L*<sub>*r*</sub>, *L*<sub>*m*</sub>) = (853, 2048, 3, T(268), T(284), T(268), T)

## 性能

## 安全性

## 応用

実用の際には[RSA暗号](../Page/RSA暗号.md "wikilink")と同様にパディングを行うことが推奨されている。

## 参考文献

### 原論文

  - *NTRU: A Ring-Based Public Key Cryptosystem*; Jeffrey Hoffstein, Jill Pipher, Joseph H. Silverman; Algorithmic Number Theory (ANTS III), Portland, OR, June 1998, J.P. Buhler (ed.), Lecture Notes in Computer Science 1423, Springer-Verlag, Berlin, 1998, 267-288.
  - <http://sourceforge.net/projects/ntru/> NTRUのオープンソース実装

## 関連項目

  - [暗号](../Page/暗号.md "wikilink")
  - [暗号理論](../Page/暗号理論.md "wikilink")
  - [ラティス暗号](https://ja.wikipedia.org/wiki/ラティス暗号 "wikilink")
  - [NTRU署名](https://ja.wikipedia.org/wiki/NTRU署名 "wikilink")

[Category:暗号](https://ja.wikipedia.org/wiki/Category:暗号 "wikilink")