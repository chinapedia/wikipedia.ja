> この記事は[NP](https://ja.wikipedia.org/wiki/NP)から翻訳されています。


**NP**は、[複雑性クラス](https://ja.wikipedia.org/wiki/複雑性クラス "wikilink")のひとつで、Non-deterministic Polynomial time（非決定性多項式時間）の略である（「Non-P」ないしは「Not-P」**ではない**）。

## 定義

NP の定義は次の2つである、ただしこれらはお互い[同値](../Page/同値.md "wikilink")であることが証明されている。

1.  [非決定性チューリングマシン](../Page/非決定性チューリングマシン.md "wikilink")によって[多項式時間](https://ja.wikipedia.org/wiki/多項式時間 "wikilink")で解くことができる問題。
2.  yes となる証拠が与えられたとき、その証拠が本当に正しいかどうかを[多項式時間](https://ja.wikipedia.org/wiki/多項式時間 "wikilink")で判定できる問題。

端的に説明するときは 2番目の定義（多項式時間で検算可能）が用いられることが多い。

なお NP はクラス [P](../Page/P_\(計算複雑性理論\).md "wikilink") 同様、[判定問題](https://ja.wikipedia.org/wiki/判定問題 "wikilink")のクラスであり yes/no で答えることの出来ない問題は NP には属さない。

例として、ハミルトン閉路問題を考えてみよう。これは「与えられたグラフについて、全ての頂点を一度だけ通る閉路が存在するか」という問題であり、この問題に対してyes/noを判定するのは容易ではない(多項式時間で解けるアルゴリズムは知られていない)。しかしyesとなる証拠、すなわち実際の閉路が与えられたならば、「本当に全ての点を一度ずつ通っているか」という検証は多項式時間で可能である。したがって、ハミルトン閉路問題はNPに属する。

誤解されることが多いが、NP は**多項式時間で解けない問題のクラスではない**（Not P の略ではない)。上記の定義は全てのクラス P の問題にも当てはまるので、クラス P は クラス NP に含まれる。

NPは[Pよりも大きいと予想されているが](../Page/P_\(計算複雑性理論\).md "wikilink")、証明されていない。[P≠NP予想](../Page/P≠NP予想.md "wikilink")という。

NPに属する任意の問題と少なくとも同じくらい難しい問題を[NP困難](../Page/NP困難.md "wikilink")であるといい、そのうちNPに属するものをNP完全問題という。これらの概念は正確には[多項式時間帰着](https://ja.wikipedia.org/wiki/多項式時間帰着 "wikilink")を使って定義する。

## 関連項目

  - [量子コンピュータ](../Page/量子コンピュータ.md "wikilink")（ただし「[BQP](https://ja.wikipedia.org/wiki/BQP "wikilink")」という、量子コンピュータの計算複雑性クラスとNPがどういう関係にあるかは、2018年現在、明確ではない。従って、関連項目ではあるが、どういう関連があるのかは2018年の時点では明確ではない）
  - [多項式階層](https://ja.wikipedia.org/wiki/多項式階層 "wikilink")
  - [対話型証明系](https://ja.wikipedia.org/wiki/対話型証明系 "wikilink")

[Category:計算複雑性理論](https://ja.wikipedia.org/wiki/Category:計算複雑性理論 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")