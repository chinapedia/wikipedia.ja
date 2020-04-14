> この記事は[In-placeアルゴリズム](https://ja.wikipedia.org/wiki/In-placeアルゴリズム)から翻訳されています。


**in-placeアルゴリズム**とは、[計算機科学](../Page/計算機科学.md "wikilink")において[データ構造](../Page/データ構造.md "wikilink")の変換を行うにあたって、追加の記憶領域をほとんど使わずに行う[アルゴリズム](../Page/アルゴリズム.md "wikilink")を意味する。 in-place とは「その場で」といった意味であり、入力が出力で上書きされることが多いことから来る用語である。 in-place でないアルゴリズムは **not-in-place** あるいは **out-of-place** などと呼ばれることもある。

in-placeの定義にはやや揺れがある。最も狭義にはポインタなども含めて一定の空間しか使用しないアルゴリズムを指す。しかし長さ*n*の配列の添字を表すだけでも O(log *n*) の空間を必要とするため、この意味で in-place であるアルゴリズムはごく限られている。多くの場合、 O(log *n*) の空間を使うことが許される。より広く O((log *n*)<sup>const.</sup>) 程度まで認めることもあり、時には o(*n*) であればよいとすることもある。

入力を出力で上書きしない場合、出力を追加の記憶領域とみなすかどうかについても揺れがある。出力先が通常の記憶装置である場合は記憶領域に含めて評価するが、書き込み専用メモリやストリームに出力する場合にはその大きさを無視して作業領域だけを評価することがある。特に[対数領域帰着](https://ja.wikipedia.org/wiki/対数領域帰着 "wikilink")のような[計算複雑性理論](https://ja.wikipedia.org/wiki/計算複雑性理論 "wikilink")の問題では出力空間を無視するのが一般的である（その場合、出力をライトオンリーとすることが本質的に必要である）。

## 例

*n*個の要素からなる[配列](../Page/配列.md "wikilink")の要素を逆順に入れ替える場合を考える。単純な方法として以下の方式が考えられる:

` `**`function`**` reverse(a[0..n])`
`     allocate b[0..n]`
`     `**`for`**` i `**`from`**` 0 `**`to`**` n`
`         b[n - i] = a[i]`
`     `**`return`**` b`

この方法では配列 *b* の領域に O(*n*) の空間を必要とする。記憶領域の確保は時間がかかることが多い。もし *a* を今後必要としないなら、以下のような in-placeアルゴリズムで *a* に逆順の出力結果を書き込むことができる:

` `**`function`**` reverse-in-place(a[0..n])`
`     `**`for`**` i `**`from`**` 0 `**`to`**` floor(n/2)`
`         swap(a[i], a[n-i])`

他の例として、以下のような[整列アルゴリズム](https://ja.wikipedia.org/wiki/整列アルゴリズム "wikilink")は入力[配列](../Page/配列.md "wikilink")そのものを操作して整列を施す in-placeアルゴリズムである:

  - [バブルソート](../Page/バブルソート.md "wikilink")
  - [コムソート](https://ja.wikipedia.org/wiki/コムソート "wikilink")
  - [選択ソート](../Page/選択ソート.md "wikilink")
  - [挿入ソート](../Page/挿入ソート.md "wikilink")
  - [ヒープソート](../Page/ヒープソート.md "wikilink")
  - [シェルソート](../Page/シェルソート.md "wikilink")

[クイックソート](../Page/クイックソート.md "wikilink")は in-place アルゴリズムと言われることが多いが、実際にはそうではない。最悪の場合再帰の深さが O(*n*) に達し O(*n* log *n*) の領域を消費するからである。[イントロソート](https://ja.wikipedia.org/wiki/イントロソート "wikilink")に改めれば再帰が浅くなるため広い意味では in-place になる。

[選択アルゴリズム](../Page/選択アルゴリズム.md "wikilink")は多くの場合 in-place だが、結果を得るために入力配列の要素の配置を大幅に変えてしまう。

[文字列操作](https://ja.wikipedia.org/wiki/文字列操作 "wikilink")アルゴリズム（[トリム](https://ja.wikipedia.org/wiki/トリム "wikilink")や文字列の逆転など）は in-place で行われることが多い。

## 計算複雑性理論

[計算複雑性理論](https://ja.wikipedia.org/wiki/計算複雑性理論 "wikilink")では、in-place アルゴリズムは空間複雑性が O(1) であるアルゴリズム（**[DSPACE](https://ja.wikipedia.org/wiki/DSPACE "wikilink")**(1)クラス）を全て含む。このクラスは非常に限定されており、[正規言語](../Page/正規言語.md "wikilink")と等価である\[1\]。実際、上述の例にあるアルゴリズムはいずれもこのクラスには含まれない。

このため、一般に in-placeアルゴリズムには[Lクラスのアルゴリズム](https://ja.wikipedia.org/wiki/L_\(計算複雑性理論\) "wikilink")（すなわち、O(log *n*)の追加領域を必要とする問題のクラス）を含める。これは、定義と矛盾しているように見えるが、抽象世界では非常に巨大な入力を考慮する。実際のコンピュータでは、物理メモリ量が限られているため[ポインタに要する領域は極めて小さいが](../Page/ポインタ_\(プログラミング\).md "wikilink")、サイズ *n* のリストのインデックスを表すには一般に O(log *n*)ビットの領域を必要とする。

この定義によれば[ヒープソート](../Page/ヒープソート.md "wikilink")は in-place であるが[イントロソート](https://ja.wikipedia.org/wiki/イントロソート "wikilink")は O((log *n*)<sup>2</sup>) の追加領域を必要とするため in-place ではないということになる。

Lクラスのアルゴリズムを in-placeアルゴリズムであると認めると、興味深い洞察が得られる。例えば、[無向グラフでの](../Page/グラフ理論.md "wikilink")2ノード間の経路が存在するかどうかを決定する in-placeアルゴリズムが存在することになる\[2\]。通常、この問題は[深さ優先探索](../Page/深さ優先探索.md "wikilink")などでは O(*n*) の追加領域を必要とする。同様に、[2部グラフ](../Page/2部グラフ.md "wikilink")かどうかの判定問題や2つのグラフが同数の[連結成分](https://ja.wikipedia.org/wiki/連結成分 "wikilink")を持つかどうかという問題などに関しても in-placeアルゴリズムが存在することになる。

## 無作為性の役割

[乱択アルゴリズム](https://ja.wikipedia.org/wiki/乱択アルゴリズム "wikilink")を使うことで必要な領域を劇的に減らすことができる場合が多い。例えば、ある2つのノードがグラフ内の1つの連結成分に含まれるかどうかを判定する問題を考える。この問題には既知の単純で[決定的な](../Page/決定的アルゴリズム.md "wikilink") in-placeアルゴリズムは存在しない。しかし、1つのノードを選んで約 20*n*<sup>3</sup>回[ランダムウォーク](../Page/ランダムウォーク.md "wikilink")を行うと、もう1つのノードが同じ連結成分に含まれていることを発見する確率が非常に高い。また、[素数判定](../Page/素数判定.md "wikilink")にも確率的（乱択） in-placeアルゴリズムが存在するし（[ミラー-ラビン素数判定法](https://ja.wikipedia.org/wiki/ミラー-ラビン素数判定法 "wikilink")など）、[素因数分解](../Page/素因数分解.md "wikilink")にも同様のアルゴリズムが存在する（[ポラード・ロー素因数分解法](../Page/ポラード・ロー素因数分解法.md "wikilink")）。

## 関数型プログラミング

[関数型言語](../Page/関数型言語.md "wikilink")ではデータを上書きするような明確な in-placeアルゴリズムをサポートしていない（推奨しない）ことが多い。これは、データの上書きが[副作用の一種であるためで](../Page/副作用_\(プログラム\).md "wikilink")、関数型言語では新たにデータ構造を作成することだけを許す（推奨する）のが一般的である。しかし、コンパイラが高度なものであれば、新たなデータが既存のデータに似ていて、かつ既存のデータが捨てられるだけであった場合、最適化によってデータ領域を再利用することがある。

ただし、これはデータの更新と以前のデータの参照が前後しないよう注意深く構築された in-placeアルゴリズムでなければならず、実際にはめったにない。

## 参考文献

<references/>

[Category:アルゴリズム](https://ja.wikipedia.org/wiki/Category:アルゴリズム "wikilink")

1.  Maciej Liśkiewicz and Rüdiger Reischuk. [The Complexity World below Logarithmic Space](http://citeseer.ist.psu.edu/34203.html). *Structure in Complexity Theory Conference*, pp. 64-78. 1994. Online: p. 3, Theorem 2.
2.  Omer Reingold. [Undirected ST-connectivity in Log-Space](http://www.wisdom.weizmann.ac.il/~reingold/publications/sl.ps). Electronic Colloquium on Computational Complexity. No. 94.