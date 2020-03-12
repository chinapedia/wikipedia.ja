> この記事は[NP](https://ja.wikipedia.org/wiki/NP)から翻訳されています。


**NP完全（な）問題**（エヌピーかんぜん（な）もんだい、NP-complete problem）とは、(1) クラス[NP](../Page/NP.md "wikilink")（Non-deterministic Polynomial）に属する決定問題（言語）で、かつ (2) 任意のクラスNPに属する問題から[多項式時間還元（帰着）可能なもののことである](../Page/多項式時間変換.md "wikilink")。条件 (2) を満たす場合は、問題の定義が条件 (1) を満たさない場合にも、[NP困難](../Page/NP困難.md "wikilink")な問題とよびその計算量的な困難性を特徴づけている。多項式時間還元の推移性から、クラスNPに属する問題で、ある一つのNP完全問題から多項式時間還元可能なものも、またNP完全である。現在発見されているNP完全問題の証明の多くはこの推移性によって[充足可能性問題](../Page/充足可能性問題.md "wikilink")などから導かれている。[充足可能性問題](../Page/充足可能性問題.md "wikilink")がNP完全であることは[1971年](https://ja.wikipedia.org/wiki/1971年 "wikilink")、[スティーブン・クック](../Page/スティーブン・クック.md "wikilink")（Stephen Cook (1971). "The Complexity of Theorem Proving Procedures". Proceedings of the third annual ACM symposium on Theory of computing. pp. 151–158.）によって証明され、R. M. カープの定義した多項式時間還元（Richard M. Karp (1972). "Reducibility Among Combinatorial Problems" (PDF). In R. E. Miller and J. W. Thatcher (editors). Complexity of Computer Computations. New York: Plenum. pp. 85–103.）によって多くの計算量的に困難な問題が NP 完全であることが示された。

## NP困難との違い

**NP困難 (NP-hard)** は「NP完全な問題と比べ、同等またはそれ以上に難しい」という意味である。一方、**NP完全**はあくまでNPに属する問題で、NP困難である問題は必ずしもNPに属さなくてもよいという違いがある。

一般にNP完全とNP困難は極めて混同されやすく、特に[アルゴリズム](../Page/アルゴリズム.md "wikilink")を扱う本などでは、NP完全と表記しながらもNP困難の説明をしていたり、本来はNP困難ではあってもNP完全ではない問題を「NP完全の例」として挙げる物が多々ある。

これは定義をよく理解せずに議論していることが主な理由だが、多くのNP完全な問題は、組合せ最適化問題の問題例にコスト／ゲインの閾値を与えた決定問題として定義されていることも一因であろう。

## 例

以下の問題、あるいはその判定問題版は、NP完全である。

  - [充足可能性問題](../Page/充足可能性問題.md "wikilink")
  - [頂点被覆問題](https://ja.wikipedia.org/wiki/頂点被覆問題 "wikilink")
  - [ハミルトン閉路問題](https://ja.wikipedia.org/wiki/ハミルトン閉路問題 "wikilink")
  - [部分和問題](https://ja.wikipedia.org/wiki/部分和問題 "wikilink")
  - [行商人問題](../Page/巡回セールスマン問題.md "wikilink")
  - [ナップサック問題](../Page/ナップサック問題.md "wikilink")
  - [テトリス](../Page/テトリス.md "wikilink")をはじめとした様々なパズルゲーム\[1\]

## 脚注

[Category:計算複雑性理論](https://ja.wikipedia.org/wiki/Category:計算複雑性理論 "wikilink") [Category:数学の問題](https://ja.wikipedia.org/wiki/Category:数学の問題 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.  、 、、