> この記事は[AA](https://ja.wikipedia.org/wiki/AA)から翻訳されています。


**AA木**（[英](../Page/英語.md "wikilink"): **AA tree**）は、[平衡2分探索木](https://ja.wikipedia.org/wiki/平衡2分探索木 "wikilink")の一種であり、順序のあるデータを効率的に格納し検索する。Arne Andersson が1993年に発表した\[1\]。名称は考案者の名前のイニシャルに由来する。

[赤黒木](https://ja.wikipedia.org/wiki/赤黒木 "wikilink")とは異なり、AA木では右の子ノードだけが赤となる。逆に言えば、左の子ノードは赤にはならない。結果として[2-3-4木](https://ja.wikipedia.org/wiki/2-3-4木 "wikilink")ではなく[2-3木](https://ja.wikipedia.org/wiki/2-3木 "wikilink")に相当したものとなり、操作時の処理が大幅に簡略化される。赤黒木では、平衡を保つために以下のような木構造の断片をそれぞれ異なるものとして扱う必要がある。

[ファイル:Red Black Shape Cases.svg](https://ja.wikipedia.org/wiki/ファイル:Red_Black_Shape_Cases.svg "wikilink")

これに対してAA木では、右のリンクだけが赤になりうるため、以下の2種類だけを考慮すればよい。

[ファイル:AA Tree Shape Cases.svg](https://ja.wikipedia.org/wiki/ファイル:AA_Tree_Shape_Cases.svg "wikilink")

## 平衡回転

AA木は、赤黒木とは異なり、色ではなくレベルの概念を使って実装される。各ノードにはレベルが格納され、常に以下の条件が成り立つようになっている。

1.  葉ノードのレベルは1である。
2.  左の子ノードのレベルは親ノードのレベルより必ず１つ小さい。
3.  右の子ノードのレベルは親ノードのレベルと等しいか１つ小さい。
4.  右の孫ノードのレベルは祖父（祖母）ノードのレベルより必ず小さい。
5.  レベルが1より大きいノードは、必ず2つの子ノードを持つ。

AA木では平衡を保つための操作は skew と split の2つだけである。skew は、挿入・削除によって水平左リンクが生じたときに（赤黒木で言えば、左の赤リンクに相当する）、右[回転させる操作である](https://ja.wikipedia.org/wiki/木の回転 "wikilink")。split は、挿入・削除によって水平右リンクが2つ生じたときに（赤黒木で言えば、赤ノードが2つ連続する状態に相当する）、条件付きで左回転させる操作である。水平リンクとは、子ノードが親ノードと同じレベルであることを意味する。

**`function`**` skew `**`is`**
`    `**`input:`**` T, 再平衡化が必要なAA木を表すノード`
`    `**`output:`**` 平衡化されたAA木を表すノード`

`    `**`if`**` nil(T) `**`then`**
`        `**`return`**` Nil`
`    `**`else``   ``if`**` nil(left(T)) `**`then`**
`        `**`return`**` T   `
`    `**`else``   ``if`**` level(left(T)) == level(T) `**`then`**
`        `*`水平左リンクのポインタを入れ替える。`*
`        L = left(T)`
`        left(T) := right(L)`
`        right(L) := T`
`        `**`return`**` L`
`    `**`else`**
`        `**`return`**` T`
`    `**`end``   ``if`**
**`end``   ``function`**

Skew: [ファイル:AA Tree Skew2.svg](https://ja.wikipedia.org/wiki/ファイル:AA_Tree_Skew2.svg "wikilink")

**`function`**` split `**`is`**
`    `**`input:`**` T, 再平衡化が必要なAA木を表すノード`
`    `**`output:`**` 平衡化されたAA木を表すノード`

`    `**`if`**` nil(T) `**`then`**
`        `**`return`**` Nil`
`    `**`else``   ``if`**` nil(right(T)) `**`or`**` nil(right(right(T))) `**`then`**
`        `**`return`**` T`
`    `**`else``   ``if`**` level(T) == level(right(right(T))) `**`then`**
`        `*`水平右リンクが2つある場合。真ん中を持ち上げて、それを返す。`*
`        R = right(T)`
`        right(T) := left(R)`
`        left(R) := T`
`        level(R) := level(R) + 1`
`        `**`return`**` R`
`    `**`else`**
`        `**`return`**` T`
`    `**`end``   ``if`**
**`end``   ``function`**

Split: [ファイル:AA Tree Split2.svg](https://ja.wikipedia.org/wiki/ファイル:AA_Tree_Split2.svg "wikilink")

## 挿入

挿入は、まず通常の2分木の探索と挿入を行う。そして、[コールスタック](https://ja.wikipedia.org/wiki/コールスタック "wikilink")を戻る際に木構造の妥当性をチェックし、必要に応じて回転を行う。水平左リンクが生じた場合、skew を行い、2つの水平右リンクが生じた場合、split を行う。そして、その時点の部分木の根ノードのレベルを必要に応じて上げる。レベルを上げる操作は、ここでの擬似コードでは上の skew で行われている。したがって新たに水平リンクが生じる場合があるので、木構造の妥当性チェックは、葉ノードから根に向かって戻る際に各ステップで毎回行う必要がある。

**`function`**` insert `**`is`**
`    `**`input:`**` X は挿入したい値、T は挿入先となる木構造の根`
`    `**`output:`**` T に X を挿入して平衡化させたもの`

`    `*`まず、通常の2分木の挿入操作を行う。新たなノードが作成されたか`*
`    `*`部分木の根が変わった場合、再帰呼び出しの結果を正しい子ノードに設定する。`*
`    `**`if`**` nil(T) `**`then`**
`        `*`X``   ``に対応する新たな葉ノードを生成`*
`        `**`return`**` node(X, 1, Nil, Nil)`
`    `**`else``   ``if`**` X < value(T) `**`then`**
`        left(T) := insert(X, left(T))`
`    `**`else``   ``if`**` X > value(T) `**`then`**
`        right(T) := insert(X, right(T))`
`    `**`end``   ``if`**
`    `*`X``   ``==``   ``value(T)``   ``の場合がない点に注意。その場合、挿入は行われない。`*
`    `*`場合によっては、違う動作が望ましいこともある。`*

`    `*`skew``   ``を行い、次いで``   ``split``   ``を行う。実際に回転をするかどうかは`*
`    `*`上掲のようにこれら手続き内で判断する。`*
`    T := skew(T)`
`    T := split(T)`

`    `**`return``   ``T`**
**`end``   ``function`**

## 削除

多くの平衡2分探索木と同様、内部ノードの削除は、最も近い先行(predecessor)また後続(successor)のノードと入れ替えることで、葉ノードの削除に帰着される。先行(predecessor)ノードの検索は、単に左のリンクをたどり、後は右のリンクをたどっていけばよい。同様に後続(successor)ノードは右に1回たどって、左をたどっていけばよい。AA木の特徴として2つの子ノードを持つノードのレベルは1より大きいので、先行(predecessor)または後続(successor)ノードはレベルが1であり、削除が簡単である。

木構造を再平衡化する方法はあまりバリエーションがない。Andersson が最初の論文\[2\]で記述した方法が最も単純であり、以下でもそれを説明している。もちろん実際に実装する際には、様々な最適化を施す余地がある。削除後、木の妥当性を保持するため、あるノードと子ノードのレベル差が2以上の場合、そのノードのレベルを下げる。また、子ノードがないのにレベルが1でないノードもレベルを下げる。そして、全体的なレベルの調整を skew と split で行う。この手法は以下のような3つの単純なステップで構成できるため、わかりやすい。

1.  必要ならレベルを下げる。
2.  そのレベルで skew を行う。
3.  そのレベルで split を行う。

ただし、以下のコードでは skew と split は1つのノードに対してだけでなく、レベル全体について行う必要があり、コードを複雑化させている。

**`function`**` delete `**`is`**
`    `**`input:`**` X は削除したい値、T は削除元となる木構造の根`
`    `**`output:`**` T から X を削除し、平衡化したもの`

`    `**`if`**` nil(T) `**`then`**
`        return T`
`    `**`else``   ``if`**` X > value(T) `**`then`**
`        right(T) := delete(X, right(T))`
`    `**`else``   ``if`**` X < value(T) `**`then`**
`        left(T) := delete(X, left(T))`
`    `**`else`**
`        `*`葉ノードであれば単純に復帰し、それ以外は再帰する。`*` `
`        `**`if`**` leaf(T) `**`then`**
`            return Nil`
`        `**`else``   ``if`**` nil(left(T)) `**`then`**
`            L := successor(T)`
`            right(T) := delete(value(L), right(T))`
`            value(T) := value(L)`
`        `**`else`**
`            L := predecessor(T)`
`            left(T) := delete(value(L), left(T))`
`            value(T) := value(L)`
`        `**`end``   ``if`**
`    `**`end``   ``if`**

`    `*`再平衡化。必要なら現在のレベルにある全ノードのレベルを下げて、`*
`    `*`新たなレベルの全ノードについて``   ``skew``   ``と``   ``split``   ``を行う。`*
`    T := decrease_level(T)`
`    T := skew(T)`
`    right(T) := skew(right(T))`
`    `**`if``   ``not`**` nil(right(T)) `**`then`**
`       right(right(T)) := skew(right(right(T)))`
`    `**`end``   ``if`**
`    T := split(T)`
`    right(T) := split(right(T))`
`    return T`
**`end``   ``function`**

**`function`**` decrease_level `**`is`**
`    `**`input:`**` T はリンクを削除しようとしている木`
`    `**`output:`**` T のレベルを下げたもの`

`    should_be = min(level(left(T)), level(right(T))) + 1`
`    `**`if`**` should_be < level(T) `**`then`**
`        level(T) := should_be`
`        `**`if`**` should_be < level(right(T)) `**`then`**
`            level(right(T)) := should_be`
`        `**`end``   ``if`**
`    `**`end``   ``if`**
`    return T`
**`end``   ``function`**

## 性能

AA木の性能は赤黒木と同等である。AA木は赤黒木よりも回転が多いが、アルゴリズムが単純であるため高速であり、全体としてはほぼ同等な性能となる。安定性は赤黒木のほうがよいが、AA木のほうが平坦になる傾向が強く、結果として検索が若干早くなる\[3\]。

## 関連項目

  - [赤黒木](https://ja.wikipedia.org/wiki/赤黒木 "wikilink")
  - [B木](../Page/B木.md "wikilink")
  - [AVL木](../Page/AVL木.md "wikilink")

## 脚注

## 参考文献

  - [A. Andersson. A note on searching in a binary search tree](http://user.it.uu.se/~arnea/abs/searchproc.html)

## 外部リンク

  - [AA-Tree Applet](http://people.ksp.sk/~kuko/bak/index.html) by Kubo Kovac
  - [AA Visual 2007 1.5 - OpenSource Delphi program for educating AA tree structures](http://www.softpedia.com/get/Others/Home-Education/AA-Visual-2007.shtml)
  - [Thorough tutorial with lots of code](http://www.eternallyconfuzzled.com/tuts/datastructures/jsw_tut_andersson.aspx)
  - [Practical implementation](http://www.eternallyconfuzzled.com/libs/jsw_atree.zip)（ZIP形式）
  - [Object Oriented implementation with tests](http://www.cs.fiu.edu/~weiss/dsaa_c++3/code/)
  - [Comparison of AA trees, red-black trees, treaps, skip lists, and radix trees](http://www.upgrade-cepis.org/issues/2004/5/up5-5Mosaic.pdf)
  - [An example C implementation](http://www.rational.co.za/aatree.c)

[Category:二分木](https://ja.wikipedia.org/wiki/Category:二分木 "wikilink") [Category:探索木](https://ja.wikipedia.org/wiki/Category:探索木 "wikilink")

1.  Arne Andersson （1993年）, ["Balanced Search Trees Made Simple"](http://user.it.uu.se/~arnea/abs/simp.html) PREPRINT. In Proc. Workshop on Algorithms and Data Structures, pages 60-71.
2.
3.