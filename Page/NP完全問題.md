> この記事は[NP完全問題](https://ja.wikipedia.org/wiki/NP完全問題)から翻訳されています。


**NP完全（な）問題**（エヌピーかんぜん（な）もんだい、NP-complete problem）とは、(1) クラス[NP](../Page/NP.md "wikilink")（Non-deterministic Polynomial）に属する決定問題（言語）で、かつ (2) 任意のクラスNPに属する問題から[多項式時間還元（帰着）可能なもののことである](../Page/多項式時間変換.md "wikilink")。条件 (2) を満たす場合は、問題の定義が条件 (1) を満たさない場合にも、[NP困難](../Page/NP困難.md "wikilink")な問題とよびその計算量的な困難性を特徴づけている。多項式時間還元の推移性から、クラスNPに属する問題で、ある一つのNP完全問題から多項式時間還元可能なものも、またNP完全である。現在発見されているNP完全問題の証明の多くはこの推移性によって[充足可能性問題](../Page/充足可能性問題.md "wikilink")などから導かれている。[充足可能性問題](../Page/充足可能性問題.md "wikilink")がNP完全であることは[1971年](https://ja.wikipedia.org/wiki/1971年 "wikilink")、[スティーブン・クック](../Page/スティーブン・クック.md "wikilink")によって証明され\[1\]、R. M. カープの定義した多項式時間還元\[2\]によって多くの計算量的に困難な問題が NP 完全であることが示された。

## NP困難との違い

**NP困難 (NP-hard)** は「NP完全な問題と比べ、同等またはそれ以上に難しい」という意味である。一方、**NP完全**はあくまでNPに属する問題で、NP困難である問題は必ずしもNPに属さなくてもよいという違いがある。

一般にNP完全とNP困難は極めて混同されやすく、特に[アルゴリズム](../Page/アルゴリズム.md "wikilink")を扱う本などでは、NP完全と表記しながらもNP困難の説明をしていたり、本来はNP困難ではあってもNP完全ではない問題を「NP完全の例」として挙げる物が多々ある。

これは定義をよく理解せずに議論していることが主な理由だが、多くのNP完全な問題は、組合せ最適化問題の問題例にコスト／ゲインの閾値を与えた決定問題として定義されていることも一因であろう。

## NP完全な問題の例

以下の問題は、NP完全である。NP完全な問題はすべて同じ難しさというわけではなく、最適化問題に直したときに問題によって近似可能性が大きく異なることがある。

  - [充足可能性問題](../Page/充足可能性問題.md "wikilink")

変数の集合\(X=\{ x_1, \ldots , x_n \}\)上のクローズ\(C_1, \ldots , C_k\)の集合が与えられる。これらすべてを充足する変数への真偽割り当ては存在するか？という問題。英語表記の最初の三文字をとってSATともいう。クローズの長さを3に制限した3-SATもNP完全であることが知られている。ある問題がNP完全であることを示そうとするとき、リダクションによく使われる問題である。\[3\]

  - [頂点被覆問題](https://ja.wikipedia.org/wiki/頂点被覆問題 "wikilink")

点カバー問題ともいう。グラフ\(G\)と整数\(k\)が与えられる。このときGにサイズが高々\(k\)の点カバーが存在するか？という問題。この問題の最適化版（できるだけ少ない頂点数の点カバーを求める）は2-近似アルゴリズムを持ち、この近似比はP≠NPとユニークゲーム問題のNP困難性を仮定すれば最善である。\[4\]

  - [ハミルトン閉路問題](https://ja.wikipedia.org/wiki/ハミルトン閉路問題 "wikilink")

有向グラフ\(G\)が与えられる。このとき\(G\)に[ハミルトン閉路が存在するか](https://ja.wikipedia.org/wiki/ハミルトン路 "wikilink")？という問題。この問題の最適化版(できるだけ最大次数が小さな全点木を求める)は、最小次数全点木問題と呼ばれる。

  - [部分集合和問題](https://ja.wikipedia.org/wiki/部分和問題 "wikilink")

部分和問題ともいう。整数\(w_1, \ldots , w_n\)と目標値\(W\)が与えられる。このとき\(\{ w_1, \ldots , w_n \}\)の部分集合\(U\)であって合計がちょうど\(W\)となるものは存在するか？という問題。

  - [巡回セールスマン問題](../Page/巡回セールスマン問題.md "wikilink")

英語の頭文字をとってTSPともいう。\(n\)個の点をもつ完全グラフ\(G\)と、\(G\)の任意の辺\(e\)に対する非負の重み\(w_e\)と上限\(D\)が与えられる。このとき重みの総和が高々\(D\)であるような\(G\)のハミルトン閉路は存在するか？という問題。この問題の最適化版(できるだけ重みが小さなハミルトン路を求める)は、P=NPでない限りいかなる定数近似アルゴリズムも持たないことが知られている。辺重みが三角不等式を満たしているような特別な場合には、1.5-近似アルゴリズム(Christofidesのアルゴリズム)が知られている。\[5\]

  - [ナップサック問題](../Page/ナップサック問題.md "wikilink")

品物の集合\(J = \{ j_1, \ldots , j_n \}\)とその価値\(p_j \; (j \in J)\)と重み\(w_j \; (j \in J)\)とナップサックの容量\(W\)と要求量\(D\)が与えられる。\(J\)の部分集合\(U\)はそのなかの品物の重みの総和が\(W\)以下であるとき許容できると言われる。このとき、許容できる集合\(U\)であって、そのなかの品物の価値の総和が\(D\)以上になるようなものは存在するか？という問題。この問題の最適化版（できるだけ価値が大きな許容できる部分集合を求める）は、[多項式時間近似スキーム](https://ja.wikipedia.org/wiki/多項式時間近似スキーム "wikilink")(PTAS)を持つ。つまり任意の正の数\(0 < \epsilon \leq 1\)に対して、\((1 - \epsilon)\)-近似アルゴリズムが存在する。\[6\]

  - [点彩色問題](https://ja.wikipedia.org/wiki/グラフ彩色 "wikilink")

グラフ\(G\)と３以上の上界\(k\)が与えられる。このとき、\(G\)はk-点彩色を持つか？という問題。\(k=2\)のときはこれはグラフが二部グラフかどうか決定する問題と同じになる。

  - そのほか

[テトリス](../Page/テトリス.md "wikilink")をはじめとした様々なパズルゲーム\[7\]もNP困難であることが知られている。

## 脚注

## 参考文献

  - J.Kleinberg・E.Tardos『アルゴリズムデザイン』浅野孝夫ほか訳, 共立出版, 2008

<!-- end list -->

  - David P.Williamson・Daivid B.Shmoys『近似アルゴリズムデザイン』浅野孝夫訳, 共立出版, 2015

[Category:NP完全問題](https://ja.wikipedia.org/wiki/Category:NP完全問題 "wikilink") [Category:計算問題](https://ja.wikipedia.org/wiki/Category:計算問題 "wikilink") [Category:数学の問題](https://ja.wikipedia.org/wiki/Category:数学の問題 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.  （Stephen Cook (1971). "The Complexity of Theorem Proving Procedures". Proceedings of the third annual ACM symposium on Theory of computing. pp. 151–158.）
2.  （Richard M. Karp (1972). "Reducibility Among Combinatorial Problems" (PDF). In R. E. Miller and J. W. Thatcher (editors). Complexity of Computer Computations. New York: Plenum. pp. 85–103.）
3.  J.Kleinberg・E.Tardos『アルゴリズムデザイン』浅野孝夫ほか訳, 共立出版, 2008, 455ページ
4.  David P.Williamson・Daivid B.Shmoys『近似アルゴリズムデザイン』浅野孝夫訳, 共立出版, 2015,21ページ
5.  David P.Williamson・Daivid B.Shmoys『近似アルゴリズムデザイン』浅野孝夫訳, 共立出版, 2015, 43ページ
6.  David P.Williamson・Daivid B.Shmoys『近似アルゴリズムデザイン』浅野孝夫訳, 共立出版, 2015,67ページ
7.  、 、、