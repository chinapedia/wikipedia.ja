> この記事は[NP困難](https://ja.wikipedia.org/wiki/NP困難)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:P_np_np-complete_np-hard.svg "wikilink")、[NP](../Page/NP.md "wikilink")、[NP完全](../Page/NP完全問題.md "wikilink")、**NP困難**の相関を表す[ベン図](../Page/ベン図.md "wikilink")\]\]

**NP困難**（エヌピーこんなん、）とは[計算量理論](https://ja.wikipedia.org/wiki/計算量理論 "wikilink")において、問題が「[NP](../Page/NP.md "wikilink")に属する任意の問題と比べて、少なくとも同等以上に難しい」ことである\[1\]。正確にいうと問題 *H* がNP困難であるとは、「[NP](../Page/NP.md "wikilink")に属する任意の問題 *L* が *H* へ帰着可能である」と定義される。この「帰着」の定義として何を用いるかにより微妙に定義が異なることになるが、例えば[多項式時間多対一帰着や](https://ja.wikipedia.org/wiki/多項式時間帰着 "wikilink")[多項式時間チューリング帰着を用いる](https://ja.wikipedia.org/wiki/多項式時間帰着 "wikilink")。NP困難問題を解ける多項式時間の[機械](../Page/機械.md "wikilink")がもしあれば、それを利用してNPに属するどの問題も多項式時間で解くことができる。

NP完全問題とは、NP困難であり、かつNPに属する問題である。これと異なり、NP困難である問題はNPに属するとは限らない。[NP](../Page/NP.md "wikilink")は[決定問題](https://ja.wikipedia.org/wiki/決定問題 "wikilink")のクラスなのでNP完全もまた決定問題に限られるが、定義に用いる帰着の種類によってはNP困難には決定問題、[探索問題](https://ja.wikipedia.org/wiki/探索問題 "wikilink")([en](https://ja.wikipedia.org/wiki/:en:Search_problem "wikilink"))、[組合せ最適化](../Page/組合せ最適化.md "wikilink")問題など様々な問題が属しうる。

上に挙げた定義から、問題 *H* がNP困難なとき次のことが言える（以下は定義ではなく主張）。

  - すべてのNP完全問題は *H* に還元して多項式時間で解ける。またNPに属する全ての問題も *H* に還元できる。
  - もし最適化問題 *H* の特殊例としてNP完全な決定問題 *L* を考えられるなら、*H* はNP困難である。

NP困難な[組合せ最適化](../Page/組合せ最適化.md "wikilink")問題は、一般に最適解を求めるのが非常に困難であると考えられているため、[近似アルゴリズム](../Page/近似アルゴリズム.md "wikilink")に関しても研究されている。

## P≠NP予想との関係

もし、いずれかのNP困難な問題を[多項式時間](https://ja.wikipedia.org/wiki/多項式時間 "wikilink")で解くアルゴリズムが存在したなら、NPの全ての問題について多項式時間で解けることになり、P = NP が成り立つ。ところが、P＝NPが成立しても「**任意の**NP困難な問題が多項式時間で解ける」とは言えない。この関係を右上の[ベン図](../Page/ベン図.md "wikilink")に示す。

## NP困難な問題の例

### 決定問題

  - [停止問題](https://ja.wikipedia.org/wiki/停止問題 "wikilink") - NP困難だがNPではない決定問題。なぜなら、停止問題は決定不可能という問題クラスに属しており、決定不可能はNPより困難で、かつ決定不可能とNPは互いに素だからである。具体的に示すには、NP困難であることは、例えば[充足可能性問題](../Page/充足可能性問題.md "wikilink")を停止問題に容易に還元できることから言える（充足できる解を見付けたら停止し、そうでない場合は無限ループするような[チューリングマシン](../Page/チューリングマシン.md "wikilink")の停止問題を考えればよい）。NPでないことは、NPに属する問題は全て有限の手続きで決定可能だが、停止問題は一般には決定不可能であることによる。ただし、NP困難でありかつNP完全でない問題の全てが決定不可能というわけではない。例えば[TQBF問題](https://ja.wikipedia.org/wiki/TQBF問題 "wikilink")([en](https://ja.wikipedia.org/wiki/:en:True_quantified_Boolean_formula "wikilink"))は[PSPACE](https://ja.wikipedia.org/wiki/PSPACE "wikilink")で決定可能だが、多分NPではない。
  - [ハミルトン閉路問題](https://ja.wikipedia.org/wiki/ハミルトン閉路問題 "wikilink") - 巡回セールスマン問題の特殊ケース。NP困難かつNP完全な決定問題。
  - [部分和問題](https://ja.wikipedia.org/wiki/部分和問題 "wikilink") - ナップサック問題の特殊ケース。NP困難かつNP完全な決定問題。

### 組合せ最適化問題

  - [巡回セールスマン問題](../Page/巡回セールスマン問題.md "wikilink")
  - [ナップサック問題](../Page/ナップサック問題.md "wikilink")
  - [最小頂点被覆問題](https://ja.wikipedia.org/wiki/最小頂点被覆問題 "wikilink")
  - [最大独立集合問題](https://ja.wikipedia.org/wiki/最大独立集合問題 "wikilink")
  - [最大クリーク問題](../Page/最大クリーク問題.md "wikilink")
  - [分数和計画問題](https://ja.wikipedia.org/wiki/分数和計画問題 "wikilink")
  - 最小シュタイナー問題

## NP関連クラスの命名規約

NPに関連するクラスの名称はまぎらわしい。「NP困難」はクラス名に「NP」と付くのに、全てが[NP](../Page/NP.md "wikilink")というわけではない。しかし現状では定着した名称なので、いまさら変わりそうにない。とはいえ、NPを中心に置いた上でそれなりに体系があるのも事実である。

  - NP完全
    NPの**中では**「完全」な問題を意味する。つまりNPの**中では**最も解くのが難しい。
  - NP困難
    「少なくとも」NPと同等以上に難しい問題（ただし、NP**に属する**とは限らない）。
  - NP-easy
    「たかだか」NPと同等以下しか難しくない問題（ただし、NP**に属する**とは限らない）。
  - NP-equivalent
    NPと同等に難しい問題（ただし、NP**に属する**とは限らない）。

## 脚注

<references/>

## 関連項目

  - [NP完全問題](../Page/NP完全問題.md "wikilink")
  - [多項式時間変換](../Page/多項式時間変換.md "wikilink") - 多対一還元やチューリング還元に計算時間の制限を付加したもの。
  - [チューリング還元](https://ja.wikipedia.org/wiki/チューリング還元 "wikilink") - 計算時間を多項式時間に制限する場合は、それを示すために前に「多項式時間～」と付けるか、または Cook還元と呼ぶ。
  - [多対一還元](https://ja.wikipedia.org/wiki/多対一還元 "wikilink") - 計算時間を多項式時間に制限する場合は、それを示すために前に「多項式時間～」と付けるか、または Karp還元と呼ぶ。単に「多項式変換」と書けば通常 Karp還元を指す。

[he:NP (מחלקת סיבוכיות)\#NP-קושי ובעיות NP-שלמות](https://ja.wikipedia.org/wiki/he:NP_\(מחלקת_סיבוכיות\)#NP-קושי_ובעיות_NP-שלמות "wikilink")

[Category:計算複雑性理論](https://ja.wikipedia.org/wiki/Category:計算複雑性理論 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.