> この記事は[LU](https://ja.wikipedia.org/wiki/LU)から翻訳されています。


[数学](../Page/数学.md "wikilink")における行列の**LU分解**（エルユーぶんかい、）とは、[正方行列](../Page/正方行列.md "wikilink") *A* を[下三角行列](https://ja.wikipedia.org/wiki/三角行列 "wikilink") *L* と[上三角行列](https://ja.wikipedia.org/wiki/三角行列 "wikilink") *U* の積に分解すること。すなわち *A* = *LU* が成立するような *L* と *U* を求めることをいう。

## LU分解の手法

以下、*n* 次[正方行列](../Page/正方行列.md "wikilink")の場合で説明する。基本的には*A* = *LU* の各成分について書き下した *n*<sup>2</sup> 個の式を解くことにより、行列 *L* , *U* を求めるのだが、このままでは未知の係数の個数（*n* (*n* +1)個）が式の個数（*n*<sup>2</sup>個）より多いので解けない。これを解くための解法には **ドゥーリトル法** と **クラウト法** の2つがある。

  - ドゥーリトル法では、行列 *L* の対角成分の全てを 1 とおき、(1, 1) 成分 , (2, 1) 成分 , (3, 1) 成分 , ... , (1, 2) 成分, (2, 2) 成分, ... の順に *n*<sup>2</sup> 個の式を解く。
  - クラウト法では、行列 *U* の対角成分の全てを 1 とおき、(1, 1) 成分 , (1, 2) 成分 , (1, 3) 成分 , ... , (2, 1) 成分, (2, 2) 成分, ... の順に *n*<sup>2</sup> 個の式を解く。

### 例

ドゥーリトル法による2次行列のLU分解を行う。与えられた正方行列*A* の成分を*a<sub>ij</sub>* とする。

1.  下三角行列*L* の対角成分を全て 1 とおき、残りの成分、(1, 2)を0、(2, 1)を変数*l*<sub>12</sub> とおく。
    \[L=\begin{pmatrix}1&0\\l_{21}&1\end{pmatrix}\]
2.  上三角行列*U* の対角成分と対角成分より上の成分を変数におく。
    \[U=\begin{pmatrix}u_{11}&u_{12}\\0&u_{22}\end{pmatrix}\]
3.  *A*=*LU* の両辺を係数比較する。
    :<math>\\begin{align}

a_{11}&=u_{11}\\\\ a_{12}&=u_{12}\\\\ a_{21}&=l_{21}u_{11}\\\\ a_{22}&=l_{21}u_{12}+u_{22} \\end{align}</math>

1.  上式を上から順に解くことで*L* , *U* が求められる。
    :<math>\\begin{align}

L&=\\begin{pmatrix}1&0\\\\\\frac{a_{21}}{a_{11}}&1\\end{pmatrix}\\\\ U&=\\begin{pmatrix}a_{11}\&a_{12}\\\\0\&a_{22}-\\frac{a_{21}a_{12}}{a_{11}}\\end{pmatrix} \\end{align}</math>

## 応用

### 連立1次方程式

[連立1次方程式](../Page/線型方程式系.md "wikilink")

\[A \boldsymbol{x} = \boldsymbol{b}\] の解き方に、行列 *A* を LU分解する方法がある。*L* , *U* は下三角行列、上三角行列であるため、逆行列を求めることなく計算することが可能である。このため、同じ*A* に対し***b*** だけを変えていくつも連立方程式を解く場合、LU分解は有用である\[1\]。

与えられた方程式

\[A \boldsymbol{x} = L U \boldsymbol{x} = \boldsymbol{b}\] に対し、変数***y*** を

\[U \boldsymbol{x} = \boldsymbol{y}\] とおき、これを上式に代入する。

\[L \boldsymbol{y} = \boldsymbol{b}\] から変数***y**'' を求める<ref>左辺*L*'y*** を計算し、左辺と右辺を係数比較すれば、***y**'' が求まる。</ref>。求めた解***y''*' を*U**x**'' = ***y*** の右辺に代入し、解 ***x*** を求めることができる\[2\]。

*L**y*** = ***b***は[ガウスの消去法](../Page/ガウスの消去法.md "wikilink")の前進消去、*U**x*** = ***y***は後退代入に対応する。

### 逆行列

行列 *A* を LU 分解すると、

\[A^{-1} = U^{-1}L^{-1}\] により[逆行列](../Page/正則行列.md "wikilink")*A*<sup>-1</sup> を求められる。

また、

\[LU\boldsymbol{x_i}=\boldsymbol{e_i}\ (i=1,2,\ldots ,n)\]

  -
    （***e**<sub>i</sub>* は[単位行列](../Page/単位行列.md "wikilink")*I* の第*i* 列）

の解***x**<sub>i</sub>* を並べた行列\(X=[\boldsymbol{x_1},\boldsymbol{x_2},\ldots ,\boldsymbol{x_n}]\)は *AX* = *I* を満たすので、このようにしても逆行列*A*<sup>-1</sup> を求めることができる。

### 行列式

行列 *A* を LU 分解できれば、その[行列式](../Page/行列式.md "wikilink")は簡単に求めることができる。なぜならば、行列 *L* および *U* は三角行列であることから、それらの行列式 |*L* | , |*U* | は対角成分の積で表され、|*A* | は、

\[|A| = |L||U|\] と計算できるからである。

## 変種

  - LDU 分解
    下三角行列 *L* と[対角行列](../Page/対角行列.md "wikilink") *D* と上三角行列 *U* の積に分解する。
    \[A = LDU\]
  - LUP 分解
    下三角行列 *L* と上三角行列 *U* と[置換行列](https://ja.wikipedia.org/wiki/置換行列 "wikilink") *P* の積に分解する。
    \[PA = LU\]

## 脚注

## 関連項目

  - [:en:Crout matrix decomposition](https://ja.wikipedia.org/wiki/:en:Crout_matrix_decomposition "wikilink")

[de:Gaußsches Eliminationsverfahren\#LR-Zerlegung](https://ja.wikipedia.org/wiki/de:Gaußsches_Eliminationsverfahren#LR-Zerlegung "wikilink")

[Category:数値線形代数](https://ja.wikipedia.org/wiki/Category:数値線形代数 "wikilink") [Category:行列の分解](https://ja.wikipedia.org/wiki/Category:行列の分解 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.
2.  左辺*U**x***を計算し、左辺と右辺を係数比較すれば、***x*** が求まる。