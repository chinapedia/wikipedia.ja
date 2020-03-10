> この記事は[R](https://ja.wikipedia.org/wiki/R)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:R-tree.svg "wikilink") **R木**（）は、[B木](../Page/B木.md "wikilink")に似た[木構造の](../Page/木構造_\(データ構造\).md "wikilink")[データ構造](../Page/データ構造.md "wikilink")であり、多次元情報（例えば、二次元座標データなど）の[インデックス付け](../Page/索引.md "wikilink")、すなわち[空間インデックス](https://ja.wikipedia.org/wiki/空間インデックス "wikilink")に使われる。それは例えば、「現在位置から2km以内の全ての美術館を探す」といった用途に使われる。

## 概要

R木は、階層的に入れ子になった相互に重なり合う[最小外接矩形](https://ja.wikipedia.org/wiki/最小外接矩形 "wikilink") (MBR) で空間を分割する。R木のRは[矩形](https://ja.wikipedia.org/wiki/矩形 "wikilink") (Rectangle) を意味する。

R木の各ノードのエントリ数は可変である（事前に定義された上限がある）。葉ノード以外の各エントリには2つのデータが格納される。1つは子ノードへの[参照であり](https://ja.wikipedia.org/wiki/参照_\(情報工学\) "wikilink")、もう1つはその子ノードの全エントリを囲む外接矩形のデータである。

挿入および削除の[アルゴリズム](../Page/アルゴリズム.md "wikilink")はこれらの外接矩形を使い、近い要素が同じ葉ノードに属するようにする（特に、新たな要素を挿入する際に、どの最下層の外接矩形にも収まらない場合、最も拡大が小さくて済む外接矩形に対応した葉ノードに属するようにする）。葉ノードの各エントリには2つのデータが格納される。1つは実際のデータ要素への参照であり（参照ではなく、葉ノード内に直接データ要素が格納される場合もある）、もう1つはそのデータ要素を囲む外接矩形のデータである。

同様に、[探索アルゴリズム](https://ja.wikipedia.org/wiki/探索アルゴリズム "wikilink")（例えば、[共通部分](https://ja.wikipedia.org/wiki/共通部分 "wikilink")、包含、最近傍）は外接矩形を使い、子ノードに対応する外接矩形内を[探索](https://ja.wikipedia.org/wiki/探索 "wikilink")すべきかどうかを判断する。このようにすると、探索においてほとんどのノードを走査する必要がなくなる。B木と同様、R木も[データベース](../Page/データベース.md "wikilink")に適しており、必要なノードだけをメモリ上にロードして操作することができる。

ノードが一杯になったときのノード分割アルゴリズムはいくつかあり、その方式によってR木は2次R木と線形R木に分けられる。

R木はこれまで[最悪実行時間](../Page/最悪実行時間.md "wikilink")を保証できないとされてきたが、実世界のデータでは一般によい性能を発揮する。しかし2004年にPR木（Priority R木）という新たなアルゴリズムが発表された。これは、従来のものと同程度に効率的であると同時に、最悪時の性能も[最適化されている](../Page/最適化_\(情報工学\).md "wikilink")。

## 派生

  - [R\*木](https://ja.wikipedia.org/wiki/R*木 "wikilink")
  - [R+木](https://ja.wikipedia.org/wiki/R+木 "wikilink")
  - [X tree](https://ja.wikipedia.org/wiki/X_tree "wikilink")
  - [Greene tree](https://ja.wikipedia.org/wiki/Greene_tree "wikilink")
  - [ヒルベルトR木](https://ja.wikipedia.org/wiki/ヒルベルトR木 "wikilink")
  - PR木（Priority R木） - PR木は、要素のばらつきが一定のデータでは通常のR木と同程度の性能だが、より極端なデータでは非常によい性能を発揮する\[1\]。

## アルゴリズム

### 探索

入力は探索矩形（クエリボックス）である。R木での探索は[B木](../Page/B木.md "wikilink")での探索によく似ている。探索は根ノードを始点とする。内部ノードには外接矩形とそれに対応した子ノードへのポインタがあり、葉ノードには空間オブジェクトの矩形がある。それぞれのノードにある矩形について、探索矩形と重なるかどうかを判断する。重なるなら、対応する子ノードについても探索を行う。探索はこのように再帰的に行われ、全ての重なりを持つノードが探索される。葉ノードに到達すると、そこに格納されている外接矩形についても同様の比較が行われ、対応する空間オブジェクトが探索矩形内にあるかどうか（探索結果に含められるか否か）が決定される。

### 挿入

オブジェクトを挿入するには、木を根ノードから再帰的に走査する必要がある。その時点の内部ノード配下の全ての矩形を調べる。新たなオブジェクトを含めるのに拡大が最小で済む矩形を選択する。この選択基準に適合する矩形が複数存在する場合、元々の領域が小さい方を選択する。この選択を再帰的に繰り返していく。葉ノードに到達したら、葉ノードに空きエントリがあれば、そのまま挿入すればよい。葉ノードに空きがない場合、挿入する前にノードの分割を行う。R木でのノード分割アルゴリズムはいくつか存在する。

### 全体ロード

  - Sort-Tile-Recursive (STR)\[2\]
  - Packed [ヒルベルトR木](https://ja.wikipedia.org/wiki/ヒルベルトR木 "wikilink") - ノードを矩形の中心のヒルベルト値を使ってソートし、再帰的に木構造を構築する。
  - Nearest-X - X座標の値に従って矩形をソートし、ノードを生成する。

## 脚注

## 参考文献

  - Antonin Guttman: *R-Trees: A Dynamic Index Structure for Spatial Searching*, Proc. 1984 [ACM SIGMOD](https://ja.wikipedia.org/wiki/Special_Interest_Group_on_Management_of_Data "wikilink") International Conference on Management of Data, pp. 47-57. ISBN 0-89791-128-8
  - Lars Arge, Mark de Berg, Herman J.Haverkort, Ke Yi: *The Priority R-Tree: A Practically Efficient and Worst-Case Optimal R-Tree*, Proc. 2004 ACM SIGMOD international conference on Management of data, pp. 347-358. ISBN 1-58113-859-8
  - Yannis Manolopoulos, Alexandros Nanopoulos, Apostolos N. Papadopoulos, Yannis Theodoridis: *R-Trees: Theory and Applications*, Springer, 2005. ISBN 1-85233-977-2
  - N. Beckmann, H.-P. Kriegel, R. Schneider, B. Seeger: [The R\*-Tree: An Efficient and Robust Access Method for Points and Rectangles](http://dbs.mathematik.uni-marburg.de/publications/myPapers/1990/BKSS90.pdf). SIGMOD Conference 1990: 322-331

## 外部リンク

  - [R-tree portal](http://www.rtreeportal.org/)
  - [R-Trees: A Dynamic Index Structure for Spatial Searching](http://www-db.deis.unibo.it/courses/SI2/papers/R3.pdf)
  - [An example java applet](http://gis.umb.no/gis/applets/rtree2/jdk1.1/)
  - [An R-tree implementation in Common Lisp](http://www.cliki.net/spatial-trees)

[Category:Rツリー](https://ja.wikipedia.org/wiki/Category:Rツリー "wikilink") [Category:ツリー_(データ構造)](https://ja.wikipedia.org/wiki/Category:ツリー_\(データ構造\) "wikilink")

1.  Lars Arge, Mark de Berg, Herman J. Haverkort, Ke Yi: [The Priority RTree: A Practically Efficient and WorstCase Optimal RTree](http://www.win.tue.nl/~mdberg/Papers/prtree.pdf)
2.  Scott T. Leutenegger, Jeffrey M. Edgington and Mario A. Lopez: [STR: A Simple and Efficient Algorithm for R-Tree Packing](http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=4D62F569DDC2B520D1658983F40AC9DC?doi=10.1.1.106.4996&rep=rep1&type=pdf)