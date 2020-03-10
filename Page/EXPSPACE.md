> この記事は[EXPSPACE](https://ja.wikipedia.org/wiki/EXPSPACE)から翻訳されています。


[計算複雑性理論](https://ja.wikipedia.org/wiki/計算複雑性理論 "wikilink")において、[複雑性クラス](https://ja.wikipedia.org/wiki/複雑性クラス "wikilink") **EXPSPACE** とは、[決定性チューリング機械で](../Page/チューリングマシン.md "wikilink") [O](../Page/ランダウの記号.md "wikilink")(2<sup>*p*(*n*)</sup>) の領域を使って解ける全[決定問題](https://ja.wikipedia.org/wiki/決定問題 "wikilink")の[集合](../Page/集合.md "wikilink")である。ここで、*p*(*n*) は *n* の多項式関数である。*p*(*n*) を[一次関数](../Page/一次関数.md "wikilink")に限定する場合もあるが、通常そのようなクラスは **[ESPACE](https://ja.wikipedia.org/wiki/ESPACE "wikilink")** と呼ばれる。

**[DSPACE](https://ja.wikipedia.org/wiki/DSPACE "wikilink")**の記法では以下のように表される。

\[\mbox{EXPSPACE} = \bigcup_{k\in\mathbb{N}} \mbox{DSPACE}(2^{n^k})\]

**EXPSPACE**完全な決定問題とは、**EXPSPACE** に属し、かつ全ての **EXPSPACE** に属する問題を[多項式時間多対一還元によってその問題に帰着させることができる場合を指す](https://ja.wikipedia.org/wiki/多項式時間変換 "wikilink")。換言すれば、多項式時間[アルゴリズム](../Page/アルゴリズム.md "wikilink")によって、ある問題から別の問題へ解を変えずに変換可能である。**EXPSPACE**完全問題は、**EXPSPACE**の中でも最も難しい問題とされる。

**EXPSPACE** は **[PSPACE](https://ja.wikipedia.org/wiki/PSPACE "wikilink")**、**[NP](../Page/NP.md "wikilink")**、**[P](https://ja.wikipedia.org/wiki/P_\(計算複雑性理論\) "wikilink")** を真に包含する。また、**[EXPTIME](https://ja.wikipedia.org/wiki/EXPTIME "wikilink")** をも真に包含すると考えられている。

**EXPSPACE**完全な問題の例として、2つの[正規表現](../Page/正規表現.md "wikilink")が異なる言語を表現しているかどうかの決定問題がある。このとき、その表現は4つの演算子（和集合、連結、[クリーネ閉包](https://ja.wikipedia.org/wiki/クリーネ閉包 "wikilink")（ゼロ個以上のコピー）、平方（2つのコピー））に制限される。

クリーネ閉包を除くと、この問題は **[NEXPTIME](https://ja.wikipedia.org/wiki/NEXPTIME "wikilink")**完全となる。これは **[EXPTIME](https://ja.wikipedia.org/wiki/EXPTIME "wikilink")**完全に似ているが、決定性ではなく[非決定性チューリング機械](https://ja.wikipedia.org/wiki/非決定性チューリング機械 "wikilink")で定義される。

また[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")、L. Berman は[実数](../Page/実数.md "wikilink")の[加法](https://ja.wikipedia.org/wiki/加法 "wikilink")と比較（[乗法](https://ja.wikipedia.org/wiki/乗法 "wikilink")は含まない）についての[一階述語論理](https://ja.wikipedia.org/wiki/一階述語論理 "wikilink")式の評価問題が **EXPSPACE** であることを示した。

## 参考文献

  - L. Berman *The complexity of logical theories*, Theoretical Computer Science 11:71-78, 1980.

  - Section 9.1.1: Exponential space completeness, pp.313–317. 冪乗の正規表現の等価性判定が **EXPSPACE**完全な問題であることを例示している。

[Category:計算複雑性理論](https://ja.wikipedia.org/wiki/Category:計算複雑性理論 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")