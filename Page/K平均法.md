> この記事は[K](https://ja.wikipedia.org/wiki/K)から翻訳されています。


**k平均法**（kへいきんほう、）は、非階層型[クラスタリングの](https://ja.wikipedia.org/wiki/データ・クラスタリング "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")。クラスタの平均を用い、与えられたクラスタ数k個に分類することから、MacQueen がこのように命名した。**k-平均法**（k-means）、**c-平均法**（c-means）とも呼ばれる。

何度か再発見されており、まず、Hugo Steinhusが[1957年](../Page/1957年.md "wikilink")に発表し\[1\]、Stuart Lloydが1957年に考案し、E.W.Forgyが1965年に発表し\[2\]、James MacQueenが[1967年](../Page/1967年.md "wikilink")に発表しk-meansと命名した\[3\]。

数式で表現すると、下記[最適化問題](../Page/最適化問題.md "wikilink")を解くアルゴリズム\[4\]。本アルゴリズムでは最小値ではなく初期値依存の極小値に収束する。

\[\operatorname{arg\,min}_{V_1, \dotsc, V_k} \sum_{i=1}^n \min_j \left\| x_i - V_j \right\|^2\]

単純なアルゴリズムであり、広く用いられている。分類を[ファジィ](https://ja.wikipedia.org/wiki/ファジィ "wikilink")化した[ファジィc-平均法](https://ja.wikipedia.org/wiki/ファジィc-平均法 "wikilink")や[エントロピー法](https://ja.wikipedia.org/wiki/エントロピー法 "wikilink")をはじめ、[データ構造](../Page/データ構造.md "wikilink")を発見するさまざまな応用手法が提案されている。上記の最適化問題は[NP困難](../Page/NP困難.md "wikilink")であるが、k-平均法は局所解を求める効率的な[ヒューリスティックである](../Page/ヒューリスティクス.md "wikilink")。k-平均法は混合正規分布に対するEMアルゴリズムの特殊な場合である

## アルゴリズム

k-平均法は、一般には以下のような流れで実装される\[5\]\[6\]。データの数を \(n\)、クラスタの数を \(k\) としておく。

1.  各データ \(x_i(i=1, \dotsc, n)\) に対して[ランダム](../Page/ランダム.md "wikilink")にクラスタを割り振る。
2.  割り振ったデータをもとに各クラスタの中心 \(V_j(j=1, \dotsc, k)\) を計算する。計算は通常割り当てられたデータの各要素の[算術平均](../Page/算術平均.md "wikilink")が使用されるが、必須ではない。
3.  各 \(x_i\) と各 \(V_j\) との距離を求め、\(x_i\) を最も近い中心のクラスタに割り当て直す。
4.  上記の処理で全ての \(x_i\) のクラスタの割り当てが変化しなかった場合、あるいは変化量が事前に設定した一定の閾値を下回った場合に、収束したと判断して処理を終了する。そうでない場合は新しく割り振られたクラスタから \(V_j\) を再計算して上記の処理を繰り返す。

結果は、最初のクラスタのランダムな割り振りに大きく依存することが知られており、1回の結果で最良のものが得られるとは限らない。そのため、何度か繰り返して行って最良の結果を選択する手法や、[k-means++法](https://ja.wikipedia.org/wiki/k-means++法 "wikilink")のように最初のクラスタ中心点の振り方を工夫する手法などが使用されることがある。

なお、このアルゴリズムではクラスタ数 k は最初に所与のものとして定めるため、最適なクラスタ数を選ぶには他の計算等による考察を用いる必要がある。

## 脚注

## 参考文献

  - 宮本定明 『クラスター分析入門　ファジィクラスタリングの理論と応用』 森北出版株式会社、1999年、ISBN 4-627-91651-5

## 関連項目

  - [ベクトル量子化](../Page/ベクトル量子化.md "wikilink")
  - [自己組織化写像](../Page/自己組織化写像.md "wikilink")
  - [データ・クラスタリング](https://ja.wikipedia.org/wiki/データ・クラスタリング "wikilink")
  - [k-means++法](https://ja.wikipedia.org/wiki/k-means++法 "wikilink")
  - [階層型クラスタリング](https://ja.wikipedia.org/wiki/階層型クラスタリング "wikilink")
  - [ウォード法](https://ja.wikipedia.org/wiki/ウォード法 "wikilink")

[Category:クラスター分析アルゴリズム](https://ja.wikipedia.org/wiki/Category:クラスター分析アルゴリズム "wikilink") [Category:統計学](https://ja.wikipedia.org/wiki/Category:統計学 "wikilink") [Category:アルゴリズム](https://ja.wikipedia.org/wiki/Category:アルゴリズム "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.
2.
3.
4.
5.
6.