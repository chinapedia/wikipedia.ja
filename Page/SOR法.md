> この記事は[SOR法](https://ja.wikipedia.org/wiki/SOR法)から翻訳されています。


**SOR法**(、**逐次加速緩和法**)とは \(n\)元[連立一次方程式](https://ja.wikipedia.org/wiki/連立一次方程式 "wikilink")\(A\boldsymbol{x}=\boldsymbol{b}\)を [反復法で解く手法の一つであり](../Page/反復法_\(数値計算\).md "wikilink")、 [ガウス＝ザイデル法](../Page/ガウス＝ザイデル法.md "wikilink")に加速パラメータ\(\omega\)を導入してその修正量を拡大することで、 更なる加速を図った手法である\[1\]。

## 反復のスキーム

\(n\)次[正方行列](../Page/正方行列.md "wikilink")\(A\)は、上[三角行列](https://ja.wikipedia.org/wiki/三角行列 "wikilink")\(U\)、 下[三角行列](https://ja.wikipedia.org/wiki/三角行列 "wikilink")\(L\)、[対角行列](../Page/対角行列.md "wikilink")\(D\)の和に分離すると、

<center>

\(A=L+D+U\)

</center>

と書ける。

非対角成分に相当する項をすべて右辺に移項し、すべての量\(x_1,x_2,\ldots,x_n\)に 各段階で得られている最新のデータを代入するようにする([ガウス＝ザイデル法](../Page/ガウス＝ザイデル法.md "wikilink"))。こうして計算された値を\(\boldsymbol{\tilde{x}}^{(k+1)}\) とすると、\(\tilde{x}_i^{(k+1)}\)は次の形となる\[2\]。

<center>

\(\tilde{x}_i^{(k+1)} = \frac{1}{a_{ii}} \left( b_i-\sum_{j=1}^{i-1} a_{ij}x_j^{(k+1)}-\sum_{j=i+1}^n a_{ij}x_j^{(k)} \right)\)

</center>

この値を次段でそのまま採用せずに、[ガウス＝ザイデル法](../Page/ガウス＝ザイデル法.md "wikilink")で本来修正される量\(\tilde{x}_i^{(k+1)}-x_i^{(k)}\)に1より大きい **加速パラメータ**（\[3\]では**緩和因子**、**緩和係数**と呼ばれている）\(\omega\)を乗じてこの修正量を拡大し、これを前段の近似値\(x_i^{(k)}\)に加えることで、新たな値は

<center>

\(x_i^{(k+1)} = x_i^{(k)} + \omega \left( \tilde{x}_i^{(k+1)}-x_i^{(k)} \right)\)

</center>

とできる\[4\]。ただし、桁落ちを防ぐ観点からこの式の通り計算するのではなく、

<center>

\(x_i^{(k+1)} = (1-\omega)x_i^{(k)} + \omega\tilde{x}_i^{(k+1)}\)

</center>

として計算するか、または本節の最後に書かれた式を用いるのがよい。

この漸化式を、上の\(A=L+D+U\)を用いて行列で表現すると、

<center>

\(\Biggl\{\begin{matrix}
\boldsymbol{\tilde{x}}^{(k+1)} &=& D^{-1} \left( \boldsymbol{b}-L\boldsymbol{x}^{(k+1)}-U\boldsymbol{x}^{(k)} \right) \\
\boldsymbol{x}^{(k+1)} &=& \boldsymbol{x}^{(k)}+\omega \left( \boldsymbol{\tilde{x}}^{(k+1)}-\boldsymbol{x}^{(k)} \right)
\end{matrix}\)

</center>

となり、この2式から\(\boldsymbol{\tilde{x}}^{(k+1)}\)を消去することで、次式が得られる。

<center>

\(\boldsymbol{x}^{(k+1)} = \left( I+\omega D^{-1}L \right)^{-1} \left\{ \left( 1-\omega \right) I-\omega D^{-1}U \right\} \boldsymbol{x}^{(k)}
+\omega \left( D+\omega L \right)^{-1}\boldsymbol{b}\)

</center>

上式における\(\boldsymbol{x}^{(k)}\)の係数 \(M_{\omega}=\left( I+\omega D^{-1}L \right)^{-1} \left\{ \left( 1-\omega \right) I-\omega D^{-1}U \right\}\)を反復行列という。

実際の数値計算においては、これを各成分について表した下の式が用いられる。

<center>

\(x_i^{(k+1)} = x_i^{(k)} + \omega\frac{1}{a_{ii}} \left( b_i-\sum_{j=1}^{i-1} a_{ij}x_j^{(k+1)}-\sum_{j=i}^n a_{ij}x_j^{(k)} \right)\)

</center>

## 収束性

反復行列の固有値を\(\lambda\)とすると、

\[\max|\lambda| \geq |\omega-1| \quad \forall\omega\]

が成立することから、少なくとも\(0<\omega<2\)でなければSOR法の収束性は保証されない \[5\]。

さらに、[正定値対称行列](../Page/対称行列.md "wikilink")\(A\)を係数にもつ方程式\(A\boldsymbol{x}=\boldsymbol{b}\)に対するSOR法は、 加速パラメータ\(\omega\)が\(0<\omega<2\)のとき必ず収束する（Ostrowskiの定理）\[6\]。

また、\(\omega=1\)のとき[ガウス＝ザイデル法](../Page/ガウス＝ザイデル法.md "wikilink")と同じになり\[7\]、\(\omega\)が*1*より小さいとき [ガウス＝ザイデル法](../Page/ガウス＝ザイデル法.md "wikilink")より収束が遅くなる。ただし、[ガウス＝ザイデル法](../Page/ガウス＝ザイデル法.md "wikilink")で収束しないような問題には使える \[8\]。

## 加速パラメータ\(\omega\)の選択

一般に加速パラメータ\(\omega\)の値をあらかじめ最適に定めることはできない。そのため、問題ごとに適当な値を選択する必要がある。

しかし、\(\omega\)の最適な値を決定することができる例も存在する。それは、係数行列\(A\)が、ある基本行列\(P\)に 対して

\[PAP^{-1}=\left[\begin{matrix}
 D_1 & M_1 \\
 M_2 & D_2
\end{matrix}\right]\]

という形の行列に相似変換することができ、さらに[ヤコビ法](../Page/ヤコビ法.md "wikilink")の反復行列\(M_J=-D^{-1}\left(L+U\right)\)の [スペクトル半径](https://ja.wikipedia.org/wiki/スペクトル半径 "wikilink")\(\rho\left(M_J\right)\)が既知であるときである。 なお、上の行列内の\(D_1,D_2\)は[対角行列](../Page/対角行列.md "wikilink")である。

このとき、SOR法の反復行列の[スペクトル半径](https://ja.wikipedia.org/wiki/スペクトル半径 "wikilink")\(\rho\left(M_{\omega}\right)\)が最小となる\(\omega\)の最適値は、 次の形で得られる\[9\]。

\[\omega = \frac{2}{1+\sqrt{1-\rho\left(M_J\right)^2}}\]

## 近年の研究

[共役勾配法](https://ja.wikipedia.org/wiki/共役勾配法 "wikilink")をはじめとした[クリロフ部分空間](https://ja.wikipedia.org/wiki/クリロフ部分空間 "wikilink")法の普及が進んだことでSOR法の使用が減ってしまったこともあったが\[10\]、離散勾配法 (構造保存型数値解法の一つ) との関係が明らかになったことで再び注目されている\[11\]\[12\]。

## 脚注

<div class="references-small">

<references/>

</div>

## 参考文献

  -
  - [杉原正顯](https://ja.wikipedia.org/wiki/杉原正顯 "wikilink"), 室田一雄, 線形計算の数理, [岩波書店](../Page/岩波書店.md "wikilink"), 2009年.

  - 線形方程式の反復解法、 一般社団法人 日本計算工学会 編、藤野清次 著、阿部邦美 著、[杉原正顯](https://ja.wikipedia.org/wiki/杉原正顯 "wikilink") 著、[丸善出版](https://ja.wikipedia.org/wiki/丸善出版 "wikilink")、2013年09月。

  - 数値線形代数の数理とHPC, 櫻井鉄也, 松尾宇泰, 片桐孝洋編（シリーズ応用数理 / [日本応用数理学会](https://ja.wikipedia.org/wiki/日本応用数理学会 "wikilink")監修, 第6巻）[共立出版](../Page/共立出版.md "wikilink"), 2018.8

## 関連項目

  - [数値解析](https://ja.wikipedia.org/wiki/数値解析 "wikilink")
  - [数値線形代数](https://ja.wikipedia.org/wiki/数値線形代数 "wikilink")
  - [ヤコビ法](../Page/ヤコビ法.md "wikilink")
  - [ガウス＝ザイデル法](../Page/ガウス＝ザイデル法.md "wikilink")

[Category:応用力学](https://ja.wikipedia.org/wiki/Category:応用力学 "wikilink") [Category:数値線形代数](https://ja.wikipedia.org/wiki/Category:数値線形代数 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink") [Category:数値解析](https://ja.wikipedia.org/wiki/Category:数値解析 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.  Varga, R. S. (2009). Matrix iterative analysis (Vol. 27). Springer Science & Business Media.
10.
11. 宮武勇登, 曽我部知広, & 張紹良. (2017). 微分方程式に対する離散勾配法に基づく線形方程式の数値解法の生成. [日本応用数理学会](https://ja.wikipedia.org/wiki/日本応用数理学会 "wikilink")論文誌, 27(3), 239-249.
12. Miyatake, Y., Sogabe, T., & Zhang, S. L. (2018). On the equivalence between SOR-type methods for linear systems and the discrete gradient methods for gradient systems. [:en:Journal of Computational and Applied Mathematics](https://ja.wikipedia.org/wiki/:en:Journal_of_Computational_and_Applied_Mathematics "wikilink"), 342, 58-69.