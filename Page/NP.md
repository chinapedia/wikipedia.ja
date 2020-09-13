> この記事は[NP](https://ja.wikipedia.org/wiki/NP)から翻訳されています。


[計算複雑性理論](https://ja.wikipedia.org/wiki/計算複雑性理論 "wikilink")における **NP** (*Non-deterministic Polynomial time*)は、[複雑性クラス](https://ja.wikipedia.org/wiki/複雑性クラス "wikilink")のひとつであり、答えがyesとなるような問いに対して、多項式時間で検証できる証拠が存在する決定問題のクラスである。

## 定義

**NP** は、**[NTIME](https://ja.wikipedia.org/wiki/NTIME "wikilink")**を使って次のように定義される\[1\]。

\[\textsf{NP} = \bigcup_{k\in\mathbb{N}} \textsf{NTIME}(n^k)\]

つまり、[非決定性チューリングマシン](../Page/非決定性チューリングマシン.md "wikilink")によって[多項式時間](https://ja.wikipedia.org/wiki/多項式時間 "wikilink")で解ける[決定問題](https://ja.wikipedia.org/wiki/決定問題 "wikilink")のクラスであり、名称も *Non-deterministic Polynomial time*（非決定性多項式時間）の略である。また、多項式時間検証可能という[同値](../Page/同値.md "wikilink")な定義もある。言語 L が **NP** に属するとは、多項式時間決定性[チューリングマシン](../Page/チューリングマシン.md "wikilink") *M* と多項式 *p* が存在し、次の性質を満たすことを言う。

  - \(x\in L\)ならば、ある証拠 \(w \in \{0, 1\}^{p(|x|)}\) が存在し、\(M(x, w) = 1\)
  - \(x\not\in L\)ならば、どんな証拠 \(w \in \{0, 1\}^{p(|x|)}\) でも、\(M(x, w) = 0\)

## 例

[ハミルトン閉路問題](https://ja.wikipedia.org/wiki/ハミルトン閉路問題 "wikilink")は、「与えられたグラフについて、全ての頂点を一度だけ通る閉路(ハミルトン閉路)が存在するか」という問題である。そのような閉路が与えられれば、yesであること(つまり、「本当に全ての点を一度ずつ通っているか」)は多項式時間で検証できるから、これが証拠と言えるため、ハミルトン閉路問題は **NP** に属する。証拠を具体的に求める計算量などを考える必要がなく、ただ「存在すること」が要求されることに注意する。また、noであった場合は、どんな証拠であっても検証時に間違ってハミルトン閉路であるとはならないことも重要である。

合成数判定問題は因数が証拠となるため、**NP**に属することがすぐさま分かるが、その補問題の素数判定問題ではそのような直感的で分かりやすい証拠が知られていない。[整数論](https://ja.wikipedia.org/wiki/整数論 "wikilink")によれば、 *p*-1 の完全な素因数分解と原始根が与えられれば、奇数 *p* が素数であることを多項式時間で検証できる。ということは、素数であるという証拠は、 *p*-1 の素因数分解と原始根で足りるかというと厳密にはそうではない。 *p*-1 の素因数分解が本当にすべて素因数に分解されているか、ということを検証しなければならないからである。幸いにも、再帰的に素数判定の検証を行うことによって、全体として *p* が素数であることを多項式時間で検証できる。以上より、素数判定問題は**NP**に属する。合成数判定問題の結果と併せると \(\textsf{NP}\cap\textsf{co-NP}\) に属することが言える。なお、現在では素数判定問題は **P** に属することが証明されている\[2\]。

**NP** に属するが、 **P** に属することが証明されていない問題の多くは **NP**完全であり、その例は「[NP完全問題](../Page/NP完全問題.md "wikilink")」の項に譲る。それ以外の、 **P** にも **NP**完全にも属さない問題の候補としてが挙げられる。

## 関連する複雑性クラス

### 多項式階層

[Polynomial_time_hierarchy.svg](https://ja.wikipedia.org/wiki/File:Polynomial_time_hierarchy.svg "fig:Polynomial_time_hierarchy.svg") **[P](../Page/P_\(計算複雑性理論\).md "wikilink")**は、決定性チューリングマシンを使って多項式時間で解ける問題のクラスである。定義より明らかに \(\textsf{P} \subseteq \textsf{NP}\) だが、 \(\textsf{P} \neq \textsf{NP}\) かどうかは未解決問題である([P≠NP予想](../Page/P≠NP予想.md "wikilink"))。また **[co-NP](https://ja.wikipedia.org/wiki/co-NP "wikilink")** は、 **NP** の補問題のクラスである。つまり、

\[\textsf{co-NP} = \{\bar{L} | L \in \textsf{NP} \}\] というクラスである。

これらクラスと **NP** は[多項式階層](https://ja.wikipedia.org/wiki/多項式階層 "wikilink")を構成する。\(\textsf{P} = \Sigma_0^{\rm P} = \Pi_0^{\rm P}\)とし、適切に定義することによって、

\[\Sigma_0^{\rm P} \subseteq \Sigma_1^{\rm P} \subseteq \ldots\]

\[\Pi_0^{\rm P} \subseteq \Pi_1^{\rm P} \subseteq \ldots\] という階層を成し、全クラスの和集合を **PH** とする。このとき、 \(\textsf{NP} = \Sigma_1^{\rm P}\)、 \(\textsf{co-NP} = \Pi_1^{\rm P}\) である。ある *k* について \(\Sigma_k^{\rm P} = \Sigma_{k+1}^{\rm P}\) すなわち \(\Sigma_k^{\rm P} = \Pi_{k}^{\rm P}\) となることを「多項式階層が第 *k* 層で潰れる」と言うが、

  - もし \(\textsf{P} = \textsf{NP}\) なら、階層は完全に潰れ、 \(\textsf{NP} = \textsf{co-NP} = \textsf{PH}\)。
  - もし \(\textsf{NP} = \textsf{co-NP}\) なら、階層が第1層で潰れ、 \(\textsf{NP} = \textsf{PH}\)。

つまりP≠NP予想は、多項式階層で考えると「完全には潰れない」という予想に換言できる。多項式階層は、すべての階層で潰れないと考えられているが、未解決問題である。

### NP完全およびNP困難

**[NP完全](../Page/NP完全問題.md "wikilink")**と**[NP困難](../Page/NP困難.md "wikilink")**は、**NP**の完全問題と困難問題のクラスである。直感的には、NPに属する任意の問題と少なくとも同じくらい難しい問題を[NP困難](../Page/NP困難.md "wikilink")であるといい、そのうちNPに属するものをNP完全問題という。これらの概念は正確には[多項式時間帰着](https://ja.wikipedia.org/wiki/多項式時間帰着 "wikilink")を使って定義する。[充足可能性問題](../Page/充足可能性問題.md "wikilink")が**NP**完全に属することが知られている()。**NP**完全問題の1つでも **P** に属することが証明できれば **P**=**NP** と言えるが、そのような問題は見つかっていない。

### NEXPTIMEとEXPSPACE

**[NEXPTIME](https://ja.wikipedia.org/wiki/NEXPTIME "wikilink")**は、非決定性チューリングマシンを使って指数時間で解ける問題のクラスであり、より \(\textsf{NP} \subsetneq \textsf{NEXPTIME}\) が言える。また、**[EXPSPACE](../Page/EXPSPACE.md "wikilink")**は、決定性チューリングマシンの指数サイズの領域を使って解ける問題のクラスであり、より \(\textsf{NP} \subsetneq \textsf{EXPSPACE}\) が言える。

### 対話証明系

多項式時間検証可能という側面から **NP** を考えると、対話証明とみなすこともできる。**[AM](https://ja.wikipedia.org/wiki/Arthur–Merlinプロトコル "wikilink")**は(**P** を **BPP** に拡張したように) **NP** から確率的な挙動を許すようにしたクラスである。は、\(\textsf{NP} = \textsf{PCP}(O(\log n), O(1))\) を示している。

## 関連項目

  - [複雑性クラス](https://ja.wikipedia.org/wiki/複雑性クラス "wikilink")
      - **[co-NP](https://ja.wikipedia.org/wiki/co-NP "wikilink")**
      - **[NP完全](../Page/NP完全問題.md "wikilink")**
      - **[NP困難](../Page/NP困難.md "wikilink")**
  - [P≠NP予想](../Page/P≠NP予想.md "wikilink")

## 外部リンク

  - [Complexity Zoo NP](https://complexityzoo.uwaterloo.ca/Complexity_Zoo:N#np)

## 参考文献

[Category:計算複雑性理論](https://ja.wikipedia.org/wiki/Category:計算複雑性理論 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.
2.