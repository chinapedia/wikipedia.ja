> この記事は[QR分解](https://ja.wikipedia.org/wiki/QR分解)から翻訳されています。


**QR分解**（キューアールぶんかい、）とは、*m* × *n* 実行列 *A*を、 *m* 次[直交行列](../Page/直交行列.md "wikilink") *Q* と *m* × *n* [上三角行列](https://ja.wikipedia.org/wiki/三角行列 "wikilink") *R* との積への分解により表すことまたはそう表した表現をいう。このような分解は常に存在する。

QR分解は[線型最小二乗問題を解くために使用される](../Page/最小二乗法.md "wikilink")。また、[固有値問題の数値解法](https://ja.wikipedia.org/wiki/固有値問題の数値解法 "wikilink")の1つである、[QR法](../Page/QR法.md "wikilink")の基礎となっている。

## 定義

### 正方行列

すべての実[正方行列](../Page/正方行列.md "wikilink") *A*は[直交行列](../Page/直交行列.md "wikilink")*Q*と上[三角行列](https://ja.wikipedia.org/wiki/三角行列 "wikilink")(別名右三角行列)*R*を用いて

  -
    \(A = QR\)

と分解できる。もし*A*が[正則ならば](../Page/正則行列.md "wikilink")、*R*の対角成分が正になるような因数分解は一意に定まる。

もし*A*が複素正方行列ならば、*Q*が[ユニタリ行列](../Page/ユニタリ行列.md "wikilink") (つまり\(Q^* Q = QQ^* = I\))となるような分解*A* = *QR*が存在する。

もし*A*が*n*個の[線形独立](https://ja.wikipedia.org/wiki/線形独立 "wikilink")な列を持つなら、*Q*の最初の*n*列は*A*の[列空間](https://ja.wikipedia.org/wiki/列空間 "wikilink")の[正規直交基底](https://ja.wikipedia.org/wiki/正規直交基底 "wikilink")をなす。より一般的に、1 ≤ *k* ≤ *n*の任意の*k*について、*Q*の最初の*k*列は*A*の最初の*k*列の[線型包](https://ja.wikipedia.org/wiki/線型包 "wikilink")をなす\[1\]*。A*の任意の列*k*が*Q*の最初の*k*列にのみ依存するということは、*R*が三角行列であることから明らかである\[2\]。

### 矩形行列

より一般的に、*m* ≥ *n*である複素*m*×*n*行列*A*を、*m*×*m*[ユニタリ行列](../Page/ユニタリ行列.md "wikilink")*Q*と*m*×*n*上三角行列*R*に分解することができる。*m*×*n*上三角行列の下から(*m*−*n*)行はすべてゼロであるため、*R*や、*R*と*Q*両方の分割を簡単に行うことができる。

\[A = QR = Q \begin{bmatrix} R_1 \\ 0 \end{bmatrix}
    = \begin{bmatrix} Q_1, Q_2 \end{bmatrix} \begin{bmatrix} R_1 \\ 0 \end{bmatrix}
    = Q_1 R_1.\]

ここで、*R*<sub>1</sub>は*n*×*n*上三角行列、*0*は(*m* − *n*)×*n*零行列、*Q*<sub>1</sub>は*m*×*n*行列、*Q*<sub>2</sub>は*m*×(*m* − *n*)行列で、*Q*<sub>1</sub>と*Q*<sub>2</sub>は両方直交する列を持つ。

*Q*<sub>1</sub>*R*<sub>1</sub>をはAの薄い(*thin*)QR分解と呼び、 Trefethen & Bauは軽減(*reduced*)QR分解と呼んでいる\[3\]。もし*A*が最大[階数](../Page/行列の階数.md "wikilink")*n*であり、*R*<sub>1</sub>の対角成分を正にするならば、*R*<sub>1</sub>と*Q*<sub>1</sub>は一意に定まる。しかし一般的に*Q*<sub>2</sub>はそうではない。*R*<sub>1</sub>は*A*<sup>\*</sup> *A* (*A*が実行列の場合*A*<sup>T</sup>*A*に等しい)の[コレスキー分解](../Page/コレスキー分解.md "wikilink")の上三角部分に等しい。

### QL・RQ・LQ分解

同様に、*L*を下(*lower*)三角行列として、QL、RQ、LQ分解を定義することができる。

## QR分解の計算

QR分解を計算する手法として、[グラム・シュミット分解](../Page/グラム・シュミットの正規直交化法.md "wikilink")、[ハウスホルダー変換](../Page/ハウスホルダー変換.md "wikilink")、[ギブンス回転](../Page/ギブンス回転.md "wikilink")などがある。それぞれ利点と欠点がある。

### グラム・シュミットの正規直交化法の使用

[グラム・シュミットの正規直交化法](../Page/グラム・シュミットの正規直交化法.md "wikilink")を最大階数行列の列\(A = \left[\mathbf{a}_1, \ldots, \mathbf{a}_n\right]\)に適用することを考える。[内積](../Page/内積.md "wikilink")\(\langle\mathbf{v}, \mathbf{w}\rangle = \mathbf{v}^\textsf{T} \mathbf{w}\) (複素ベクトルの場合 \(\langle\mathbf{v}, \mathbf{w}\rangle = \mathbf{v}^* \mathbf{w}\))とする。

[射影の定義より](https://ja.wikipedia.org/wiki/ベクトルの成分分解 "wikilink")、

\[\operatorname{proj}_{\mathbf{u}}\mathbf{a} =
  \frac{\left\langle\mathbf{u}, \mathbf{a}\right\rangle}{\left\langle\mathbf{u}, \mathbf{u}\right\rangle}{\mathbf{u}}.\]

したがって、

\[\begin{align}
  \mathbf{u}_1 &= \mathbf{a}_1, &
    \mathbf{e}_1 &= {\mathbf{u}_1 \over \|\mathbf{u}_1\|} \\
  \mathbf{u}_2 &= \mathbf{a}_2 - \operatorname{proj}_{\mathbf{u}_1}\,\mathbf{a}_2, &
    \mathbf{e}_2 &= {\mathbf{u}_2 \over \|\mathbf{u}_2\|} \\
  \mathbf{u}_3 &= \mathbf{a}_3 - \operatorname{proj}_{\mathbf{u}_1}\,\mathbf{a}_3 - \operatorname{proj}_{\mathbf{u}_2}\,\mathbf{a}_3, &
    \mathbf{e}_3 &= {\mathbf{u}_3 \over \|\mathbf{u}_3\|} \\
                 & \vdots &
                   & \vdots \\
  \mathbf{u}_k &= \mathbf{a}_k - \sum_{j=1}^{k-1}\operatorname{proj}_{\mathbf{u}_j}\,\mathbf{a}_k,&
    \mathbf{e}_k &= {\mathbf{u}_k \over \|\mathbf{u}_k\|}
\end{align}.\]

ここで\(\mathbf{a}_i\)を新しく計算された正規直交基底上に表すことができ、\(\left\langle\mathbf{e}_i, \mathbf{a}_i\right\rangle = \left\|\mathbf{u}_i\right\|\)であるから、

\[\begin{align}
   \mathbf{a}_1 &= \langle\mathbf{e}_1, \mathbf{a}_1\rangle \mathbf{e}_1 \\
   \mathbf{a}_2 &= \langle\mathbf{e}_1, \mathbf{a}_2\rangle \mathbf{e}_1
                 + \langle\mathbf{e}_2, \mathbf{a}_2\rangle \mathbf{e}_2 \\
   \mathbf{a}_3 &= \langle\mathbf{e}_1, \mathbf{a}_3\rangle \mathbf{e}_1
                 + \langle\mathbf{e}_2, \mathbf{a}_3\rangle \mathbf{e}_2
                 + \langle\mathbf{e}_3, \mathbf{a}_3\rangle \mathbf{e}_3 \\
                &\vdots \\
   \mathbf{a}_k &= \sum_{j=1}^k \langle \mathbf{e}_j, \mathbf{a}_k \rangle \mathbf{e}_j
\end{align}.\]

これは行列の形に書くことができ、

\[A = QR\]

ただし、

\[Q = \left[\mathbf{e}_1, \ldots, \mathbf{e}_n\right],\]

\[R = \begin{pmatrix}
  \langle\mathbf{e}_1, \mathbf{a}_1\rangle &
  \langle\mathbf{e}_1, \mathbf{a}_2\rangle &
  \langle\mathbf{e}_1, \mathbf{a}_3\rangle & \ldots \\
                                         0 &
  \langle\mathbf{e}_2, \mathbf{a}_2\rangle &
  \langle\mathbf{e}_2, \mathbf{a}_3\rangle & \ldots \\
                                         0 &
                                         0 &
  \langle\mathbf{e}_3, \mathbf{a}_3\rangle & \ldots \\
                                    \vdots &
                                    \vdots &
                                    \vdots &
                                    \ddots
\end{pmatrix}.\]

#### 例

  -
    <math>A = \\begin{pmatrix}

` 12 & -51 &   4 \\`
`  6 & 167 & -68 \\`
` -4 &  24 & -41`

\\end{pmatrix}</math> の分解を考える。

正規直交行列\(Q\)に対して、

  -
    \(Q^\textsf{T} \,Q = I\)

が常に成り立つから、グラム・シュミット法により以下の手順で\(Q\)を計算できる。

  -
    <math>\\begin{align}

` U = \begin{pmatrix}`
`       \mathbf u_1 & \mathbf u_2 & \mathbf u_3`
`     \end{pmatrix} &=`
`     \begin{pmatrix}`
`       12 & -69 & -58/5 \\`
`        6 & 158 &   6/5 \\`
`       -4 &  30 & -33`
`     \end{pmatrix}; \\`
` Q = \begin{pmatrix}`
`       \frac{\mathbf u_1}{\|\mathbf u_1\|} &`
`       \frac{\mathbf u_2}{\|\mathbf u_2\|} &`
`       \frac{\mathbf u_3}{\|\mathbf u_3\|}`
`     \end{pmatrix} &=`
`     \begin{pmatrix}`
`        6/7 & -69/175 & -58/175 \\`
`        3/7 & 158/175 &   6/175 \\`
`       -2/7 &   6/35  & -33/35`
`     \end{pmatrix}.`

\\end{align}</math>

したがって、

  -
    <math>\\begin{align}

` Q^\textsf{T} A &= Q^\textsf{T}Q\,R = R; \\`
`              R &= Q^\textsf{T}A =`
`   \begin{pmatrix}`
`     14 &  21 & -14 \\`
`      0 & 175 & -70 \\`
`      0 &   0 &  35`
`   \end{pmatrix}.`

\\end{align}</math>

#### RQ分解との関係

QR分解は行列*A*を上三角行列*R*(別名右三角)と直交行列*Q*に変換する。QR分解との違いはこれらの行列の順番だけである。

QR分解はグラム・シュミットの正規直交化法を*A*の*最初の列*から*最後の列*の順に適用する。

RQ分解はグラム・シュミットの正規直交化法を*A*の*最後の行*から*最初の行*の順に適用する。

#### 利点と欠点

グラム・シュミットの正規直交化法は本来、数値的に不安定である。射影の応用として直交化との幾何学的な類似性があるが、直交化自体は数値的な差異が生じやすい。しかしながら、実装が簡単という大きな利点があり、外部線形代数ライブラリが利用できない場合のプロトタイピングに便利なアルゴリズムである。

### ハウスホルダー変換の使用

[Householder.svg](https://ja.wikipedia.org/wiki/File:Householder.svg "fig:Householder.svg")

[ハウスホルダー変換](../Page/ハウスホルダー変換.md "wikilink") (または*ハウスホルダー鏡映*)はベクトルを取り、[平面](../Page/平面.md "wikilink")または[超平面](https://ja.wikipedia.org/wiki/超平面 "wikilink")に関する鏡映をする変換である。この演算は*m*×*n*行列\(A\) (*m* ≥ *n*)の*QR*変換の計算に使うことができる。

*Q*は一つの座標を除いたすべての座標が未知でもベクトルを鏡映するために使用できる。

スカラ*α*に対して\(\|\mathbf{x}\| = |\alpha|\)を満たすような\(A\)の任意の実*m*次元列ベクトル\(\mathbf{x}\)を考える。もしこのアルゴリズムが[浮動小数点演算を用いて実装されている場合](../Page/浮動小数点数.md "wikilink")、[桁落ちを防ぐため](https://ja.wikipedia.org/wiki/誤差#桁落ち "wikilink")、行列*A*の最終的な上三角部分においてすべての要素が0である後のピボット座標\(x_k\)に対し、*α*を\(\mathbf{x}\)の*k*番目の座標の逆符号とする。複素行列の場合、

\[\alpha = -e^{i \arg x_k} \|\mathbf{x}\|\] とし、以下の*Q*の導出において転置を共役転置に読み替えること。

ここで、\(\mathbf{e}_1\)をベクトル(1 0 … 0)<sup>T</sup>、||·||を[ユークリッド距離](https://ja.wikipedia.org/wiki/ユークリッド空間#ユークリッド空間の計量 "wikilink")、\(I\)を*m*×*m*単位行列とし、

  -
    <math>\\begin{align}

` \mathbf{u} &= \mathbf{x} - \alpha\mathbf{e}_1, \\`
` \mathbf{v} &= {\mathbf{u} \over \|\mathbf{u}\|}, \\`
`          Q &= I - 2 \mathbf{v}\mathbf{v}^\textsf{T}`

\\end{align}</math>

あるいは、\(A\)が複素行列ならば、

  -
    \(Q = I - 2\mathbf{v}\mathbf{v}^*\)

とおく。

\(Q\)は*m*×*m*ハウスホルダー行列であり、

  -
    \(Q\mathbf{x} = \begin{pmatrix} \alpha & 0 & \cdots & 0 \end{pmatrix}^\textsf{T}.\,\)

これにより*m*×*n*行列*A*を上[三角の形に漸次変換できる](https://ja.wikipedia.org/wiki/三角行列 "wikilink")。まず、**x**の最初の列を選んで得られるハウスホルダー行列*Q*<sub>1</sub>に*A*を乗算する。この結果、行列*Q*<sub>1</sub>*A*は左の列が(最初の行を除き)ゼロになる。

  -
    <math>Q_1A = \\begin{bmatrix}

` \alpha_1 & \star & \dots & \star \\`
`        0 &       &       &       \\`
`   \vdots &       &    A' &       \\`
`        0 &       &       &`

\\end{bmatrix}</math>

この操作を*A*′ (*Q*<sub>1</sub>*A*から最初の列と最初の行を除いたもの)に繰り返すと、ハウスホルダー行列*Q*′<sub>2</sub>が得られる。*Q*′<sub>2</sub>は*Q*<sub>1</sub>より小さいということに注意すること。*A*′の代わりに*Q*<sub>1</sub>*A*で計算したいため、*A*′を左上に拡張し、ひとつの1を埋める必要がある。つまり、一般的には

\[Q_k = \begin{pmatrix}
  I_{k-1} & 0    \\
       0  & Q_k'
\end{pmatrix}\] とする。 \(t\)回このプロセスを繰り返すと、\(t = \min(m - 1, n)\)のとき、

\[R = Q_t \cdots Q_2 Q_1 A\]

は上三角行列である。であるからして、

\[Q = Q_1^\textsf{T} Q_2^\textsf{T} \cdots Q_t^\textsf{T}\] とすると、 \(A = QR\)は\(A\)のQR分解である。

このメソッドは先述のグラム・シュミット法よりも[数値的安定性](https://ja.wikipedia.org/wiki/数値的安定性 "wikilink")がある。

下表にサイズ*n*の正方行列を仮定したときの、ハウスホルダー変換によるQR分解の*k*番目のステップにおける計算量を示す。

| 演算  | *k*番目のステップにおける計算量                          |
| --- | ------------------------------------------ |
| 乗算  | \(2(n - k + 1)^2\)                         |
| 加算  | \((n - k + 1)^2 + (n - k + 1)(n - k) + 2\) |
| 除算  | \(1\)                                      |
| 平方根 | \(1\)                                      |

これらの数を*n* − 1ステップ(サイズ*n*の正方行列であるため)まで合計して、このアルゴリズムの(浮動小数点演算の観点からの)複雑さは

\[\frac{2}{3}n^3 + n^2 + \frac{1}{3}n - 2 = O\left(n^3\right)\] と表せる。

#### 例

  -
    <math>A = \\begin{pmatrix}

` 12 & -51 &   4 \\`
`  6 & 167 & -68 \\`
` -4 &  24 & -41`

\\end{pmatrix}</math> の分解を考える。

まず、行列*A*の最初の列、ベクトル\(\mathbf{a}_1 = \begin{pmatrix} 12 & 6 & -4 \end{pmatrix}^\textsf{T}\)を、\(\left\|\mathbf{a}_1\right\| \;\mathbf{e}_1 = \begin{pmatrix} 1 & 0 & 0\end{pmatrix}^\textsf{T}\)に変換する鏡映を見つける必要がある。

今、

  -
    \(\mathbf{u} = \mathbf{x} - \alpha\mathbf{e}_1,\)

<!-- end list -->

  -
    \(\mathbf{v} = {\mathbf{u} \over \|\mathbf{u}\|}\)

とする。

ここで、

  -
    \(\alpha = 14\)であり、\(\mathbf{x} = \mathbf{a}_1 = \begin{pmatrix} 12 & 6 & -4 \end{pmatrix}^\textsf{T}\)

であるから、

  -
    \(\mathbf{u} = \begin{pmatrix} -2 & 6 & -4 \end{pmatrix}^\textsf{T} = \begin{pmatrix} 2 \end{pmatrix}\begin{pmatrix} -1 & 3 & -2 \end{pmatrix}^\textsf{T}\) and \(\mathbf{v} = {1 \over \sqrt{14}}\begin{pmatrix} -1 & 3 & -2 \end{pmatrix}^\textsf{T}\)であり、
    <math>\\begin{align}

`     Q_1`
` ={} &I - {2 \over \sqrt{14}\sqrt{14}}`
`        \begin{pmatrix} -1 \\ 3 \\ -2 \end{pmatrix}`
`        \begin{pmatrix} -1 &  3 &  -2 \end{pmatrix} \\`
` ={} &I - {1 \over 7}\begin{pmatrix}`
`         1 & -3 &  2 \\`
`        -3 &  9 & -6 \\`
`         2 & -6 &  4`
`      \end{pmatrix} \\`
` ={} &\begin{pmatrix}`
`         6/7 &  3/7 & -2/7 \\`
`         3/7 & -2/7 &  6/7 \\`
`        -2/7 &  6/7 &  3/7 \\`
`      \end{pmatrix}`

\\end{align}</math> である。

今、

\[Q_1A = \begin{pmatrix}
  14 &  21 & -14 \\
   0 & -49 & -14 \\
   0 & 168 & -77
\end{pmatrix}\]

を見てみると、すでにほぼ三角行列である。あとは(3, 2)要素をゼロにするだけでよい。

(1, 1)における[小行列を取り](https://ja.wikipedia.org/wiki/小行列式 "wikilink")、同じプロセスを

\[A' = M_{11} = \begin{pmatrix}
  -49 & -14 \\
  168 & -77
\end{pmatrix}\] に再び適用する。

先述のメソッドと同様にして、このプロセスの次のステップが正しく動作するために、1で直和を取ることにより、ハウスホルダー変換

\[Q_2 = \begin{pmatrix}
  1 &     0 &  0 \\
  0 & -7/25 & 24/25 \\
  0 & 24/25 &  7/25
\end{pmatrix}\]

を得る。

今、

\[Q = Q_1^\textsf{T} Q_2^\textsf{T} = \begin{pmatrix}
   6/7 & -69/175 & 58/175 \\
   3/7 & 158/175 & -6/175 \\
  -2/7 &   6/35  & 33/35
\end{pmatrix}\]

または、有効数字四桁で、

\[\begin{align}
  Q &= Q_1^\textsf{T} Q_2^\textsf{T} = \begin{pmatrix}
     0.8571 & -0.3943 &  0.3314 \\
     0.4286 &  0.9029 & -0.0343 \\
    -0.2857 &  0.1714 &  0.9429
  \end{pmatrix} \\
  R &= Q_2 Q_1 A = Q^\textsf{T} A = \begin{pmatrix}
    14 &  21 & -14 \\
     0 & 175 & -70 \\
     0 &   0 & -35
  \end{pmatrix}
\end{align}\] を得た。

行列*Q*は直交行列であり、*R*は上三角行列であるため、*A* = *QR*は求めるべきQR分解である。

#### 利点と欠点

ハウスホルダー変換の使用は、*R*行列のゼロを生成するメカニズムに鏡映を利用しているため、最もシンプルな数値的に安定したQR分解アルゴリズムである。しかしながら、新しいゼロ要素を生成するすべての鏡映において*Q*、*R*行列両方の全体が変化するため、ハウスホルダー変換は帯域幅が重く、並列化できない。

### ギブンス回転の使用

*QR*分解は[ギブンス回転](../Page/ギブンス回転.md "wikilink")を使用しても計算できる。各回転により行列の亜対角要素がゼロになり、*R*行列を構成できる。すべてのギブンス回転を結合することで直交行列*Q*を構成できる。

実際には、行列全体を構成して乗算をするようなギブンス回転は行われない。代わりに、疎な要素を計算するような無駄な計算をしない、疎なギブンス行列乗算と同等なあるギブンス回転の手順が採られる。そのギブンス回転の手順は少しの非対角成分をゼロにするだけで済み、[ハウスホルダー変換](../Page/ハウスホルダー変換.md "wikilink")よりも容易に並列化できる。

#### 例

  -
    <math>A = \\begin{pmatrix}

` 12 & -51 &   4 \\`
`  6 & 167 & -68 \\`
` -4 &  24 & -41`

\\end{pmatrix}</math> の分解を考える。

まず、左下隅の要素、\(\mathbf{a}_{31} = -4\)をゼロにする回転行列を構成する必要がある。この行列\(G_1\)はギブンス回転で求めることができる。まずベクトル\(\begin{pmatrix} 12 & -4 \end{pmatrix}\)を、*X*軸に沿って回転させる。このベクトルは角度\(\theta = \arctan\left({-(-4) \over 12}\right)\)を持つ。直交ギブンス回転行列\(G_1\)を次のように作る。

\[\begin{align}
  G_1 &= \begin{pmatrix}
    \cos(\theta) & 0 & -\sin(\theta) \\
               0 & 1 &             0 \\
    \sin(\theta) & 0 &  \cos(\theta)
  \end{pmatrix} \\
      &\approx \begin{pmatrix}
    0.94868 & 0 & -0.31622 \\
    0       & 1 &  0       \\
    0.31622 & 0 &  0.94868
  \end{pmatrix}
\end{align}\]

ここで\(G_1A\)の結果は\(\mathbf{a}_{31}\)要素がゼロである。

\[G_1A \approx \begin{pmatrix}
  12.64911 & -55.97231 &  16.76007 \\
   6       & 167       & -68       \\
   0       &   6.64078 & -37.6311
\end{pmatrix}\]

同様にしてそれぞれ非対角要素\(a_{21}\)・\(a_{32}\)要素がゼロであるようなギブンス行列\(G_2\)・\(G_3\)を構成し、三角行列\(R\)を構成する。直交行列\(Q^\textsf{T}\)はすべてのギブンス行列の積\(Q^\textsf{T} = G_3 G_2 G_1\)で表される。したがって、\(G_3 G_2 G_1 A = Q^\textsf{T} A = R\)であり、*QR*分解は\(A = QR\)である。

#### 利点と欠点

ギブンス回転によるQR分解は、アルゴリズムを完全に動かすのに必要な行の順序を決定するのが簡単ではないため、実装に最も手間がかかる。しかしながら、新しいゼロ要素\(a_{ij}\)がゼロになる予定の要素の行(i)とその上の行(j)にしか影響しないという特筆すべき利点がある。これにより、ギブンス回転アルゴリズムはハウスホルダー変換手法よりも帯域幅効率が良く、容易に並列化できる。

## 行列式や固有値の積との関係

QR分解を正方行列の[行列式](../Page/行列式.md "wikilink")の絶対値を求めるのに利用できる。ある行列が\(A = QR\)と分解できるとする。このとき

\[\det(A) = \det(Q) \cdot \det(R)\] である。

*Q*はユニタリであるため、\(|\det(Q)| = 1\)である。したがって、\(r_{ii}\)を*R*の対角要素とすると、

\[\left|\det(A)\right| = \left|\det(R)\right| = \left|\prod_{i} r_{ii}\right|\]

となる。

さらに、行列式は固有値の積に等しいため、\(\lambda_i\)を\(A\)の固有値とすると、

  -
    \(\left|\prod_{i} r_{ii}\right| = \left|\prod_{i} \lambda_{i}\right|\)

となる。

QR分解の定義を非正方行列に導入し、固有値を特異値に置き換えることで、上記性質を非正方行列\(A\)に拡張することができる。

非正方行列*A*のQR分解を

  -
    \(A = Q \begin{pmatrix} R \\ O \end{pmatrix}, \qquad Q^* Q = I\)

とする。ただし、\(O\)は零行列、\(Q\)はユニタリ行列。

[特異値分解](../Page/特異値分解.md "wikilink")と行列式の性質から、\(\sigma_i\)を\(A\)の特異値として、

\[\left|\prod_i r_{ii}\right| = \prod_i\sigma_{i}.\]

\(A\)と\(R\)の特異値は同じであるが、複素固有値が異なる場合があることに注意すること。しかしながら、*A*が正方ならば、下記は真である。

\[{\prod_i \sigma_i} = \left|{\prod_i \lambda_i}\right|\]

結論として、QR分解を使うことによって行列の固有値や特異値の積を効率よく計算することができる。

## 列のピボット

ピボットQRは列のピボット\[4\]の新しいステップにおいて、それぞれ初めに残りの列で最も大きいものを取るという点で、通常のグラム・シュミット法とは異なっている。したがって、[置換行列](../Page/置換行列.md "wikilink")*P*を次のように導入する。

\[AP = QR\quad \iff\quad A = QRP^\textsf{T}\]

列のピボットは*A*が(ほぼ)[階数落ちである](https://ja.wikipedia.org/wiki/行列の階数#性質 "wikilink")、またはその疑いがある場合に便利である。また、数値的精度を向上させることもできる。通常、*R*の対角成分が非増加、つまり\(\left|r_{11}\right| \ge \left|r_{22}\right| \ge \ldots \ge \left|r_{nn}\right|\)となるように*P*を選ぶ。この手段により[特異値分解](../Page/特異値分解.md "wikilink")よりも低い計算コストで*A*の(数値的な)階数を求めることができ、いわゆるの基礎となっている。

## 線形逆問題への利用

行列の逆行列を直接求めるのに比べ、QR分解を利用した逆問題の解法は、[条件数](https://ja.wikipedia.org/wiki/条件数 "wikilink")が減少していることからも分かるように、数値的に安定している\[5\]。

次元が\(m \times n\)で階数が\(m\)であるような行列\(A\)に対して、劣決定(\(m < n\))線形問題\(Ax = b\)を解くためには、まず\(A\)の転置行列のQR分解\(A^\textsf{T} = QR\)を求める。ただし、Qは直交行列(つまり、\(Q^\textsf{T} = Q^{-1}\))であり、Rは\(R = \begin{bmatrix} R_1 \\ 0 \end{bmatrix}\)という特殊な形である。ここで、\(R_1\)は\(m \times m\)正方右三角行列、零行列は\((n-m) \times m\)次元である。計算すると、この逆問題の解を次のように表すことができる。\(x = Q \begin{bmatrix}
    \left(R_1^\textsf{T}\right)^{-1}b \\
                           0
  \end{bmatrix}\)

ここで、\(R_1^{-1}\)は[ガウスの消去法](../Page/ガウスの消去法.md "wikilink")で計算でき、\(\left(R_1^\textsf{T}\right)^{-1} b\)はを用いることで直接計算できる。後者の手法の方が数値的精度が高く、計算量も少ないという利点がある。

ノルム\(\|A \hat{x} - b\|\)を最小にするような過決定(\(m \geq n\))問題\(Ax = b\)の解\(\hat{x}\)を求めるためには、まず\(A\)のQR分解\(A = QR\)を求める。\(Q_1\)を直交行列\(Q\)全体のうち最初の\(n\)列を含む\(m \times n\)行列、\(R_1\)を先述の通りに置くと、この問題の解は\(\hat{x} = R_1^{-1} \left(Q_1^\textsf{T} b\right)\)と表せる。劣決定の場合と同様に、\(R_1\)の逆行列を直接計算しなくても、を用いることで早く正確に\(\hat x\)を求めることができる。(\(Q_1\)と\(R_1\)は数値ライブラリによっては高速な(*economic*)QR分解として実装されている。)

## 一般化

はQR分解を半単純リー群に一般化している。

## 脚注

## 参考文献

### 和文

  -
  -
  -
### 英文

  -
  -
  -
  -
  -
  - .

## 関連項目

  - [QR法](../Page/QR法.md "wikilink")

  -
  - [固有値分解](https://ja.wikipedia.org/wiki/固有値分解 "wikilink")

  - [LU分解](../Page/LU分解.md "wikilink")

  - [特異値分解](../Page/特異値分解.md "wikilink")

## 外部リンク

  - [Online Matrix Calculator](https://web.archive.org/web/20081212221215/http://www.bluebit.gr/matrix-calculator/) 行列のQR分解の実行
  - [LAPACK users manual](http://netlib.org/lapack/lug/node39.html) QR分解の計算のサブルーチンの詳細
  - [Mathematica users manual](https://web.archive.org/web/20061122183956/http://documents.wolfram.com/mathematica/functions/QRDecomposition) QR分解の計算のルーチンの詳細と例
  - [ALGLIB](http://www.alglib.net/) LAPACKのC++、C\#、Delphiなどへの移植
  - [Eigen::QR](http://eigen.tuxfamily.org/dox-devel/group__QR__Module.html) QR分解のC++での実装

[Category:数値線形代数](https://ja.wikipedia.org/wiki/Category:数値線形代数 "wikilink") [Category:行列](https://ja.wikipedia.org/wiki/Category:行列 "wikilink") [Category:行列の分解](https://ja.wikipedia.org/wiki/Category:行列の分解 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.  L. N. Trefethen and D. Bau, *Numerical Linear Algebra* (SIAM, 1997).
2.
3.
4.
5.  Parker, Geophysical Inverse Theory, Ch1.13.