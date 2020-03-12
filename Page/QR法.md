> この記事は[QR](https://ja.wikipedia.org/wiki/QR)から翻訳されています。


**QR法**（きゅーあーるほう、QR algorithm）は、行列Aの[固有値](../Page/固有値.md "wikilink")を求める方法の一つで、 行列の[QR分解](../Page/QR分解.md "wikilink")を利用するものである。QR法は[数値解析的に安定な](https://ja.wikipedia.org/wiki/数値的安定性 "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")である。

## 手順

行列Aの次数をnとする。

まず

\[A_1=A\]

とおく。以下、

\[A_k=Q_kR_k\]

\[A_{k+1}=R_kQ_k\left(=Q_k^{-1}A_kQ_k\right)\]

\[(k=1, 2, \cdots, m)\]

と繰り返す。この繰り返し手順は[相似](https://ja.wikipedia.org/wiki/相似 "wikilink")変換であるため、行列A<sub>1</sub>の固有値と行列A<sub>k</sub>の固有値はすべて一致する。 （ただし、固有ベクトルは必ずしも一致しない）したがって、固有ベクトルを求める必要があれば、行列A<sub>m+1</sub>の固有値を求めた後、 行列Aに戻って各固有値に対応する固有ベクトルをそれぞれ求めなければならない。

## 特別な場合

行列Aが対称行列である場合、 相似変換後に得られる行列A<sub>m+1</sub>は 三重対角行列（対角成分とその上下左右に隣接する成分のみに0以外の値が出現する行列）となる。 三重対角行列の固有値は対角線上に並ぶため、固有値の特定が容易である。

## 原点移動付きQR法

上記手順では、A<sub>k</sub>が収束するまで繰り返すQR分解の回数が多くなりやすい。 このため、上記繰り返し手順を

\[A_k-\mu_kI=Q_kR_k\]

\[A_{k+1}=R_kQ_k+\mu_kI\left(=Q_k^{-1}AQ_k\right)\]

\[(k=1, 2, \cdots, m)\]

と置き換えて、QR分解の回数を減らそうとすることがある。 このような手順を原点移動付きQR法という。

μ<sub>k</sub>の選択方法として、A<sub>k</sub>の右下隅の2×2小行列の固有値のうち、 A<sub>k</sub>の右下隅の値に近いほうを選択することが多い（**ウィルキンソンの移動法**）。

## 関連項目

  - [QR分解](../Page/QR分解.md "wikilink")

[Category:数値線形代数](https://ja.wikipedia.org/wiki/Category:数値線形代数 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")