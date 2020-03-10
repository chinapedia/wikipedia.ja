> この記事は[NC \(\)](https://ja.wikipedia.org/wiki/NC_\(\))から翻訳されています。


[計算複雑性理論](https://ja.wikipedia.org/wiki/計算複雑性理論 "wikilink")において、**NC**（Nick's Class）とは多項式個数のプロセッサで構成される[並列計算機で](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")，問題サイズの対数について多項式時間で解ける[決定問題](https://ja.wikipedia.org/wiki/決定問題 "wikilink")の[複雑性クラス](https://ja.wikipedia.org/wiki/複雑性クラス "wikilink")である。換言すれば、**NC** に属する問題は、O(*n*<sup>*k*</sup>)個の並列プロセッサを使って O((log *n*)<sup>*c*</sup>) の時間で解ける（*c* と *k* は定数）。"Nick's Class" という用語は[スティーブン・クック](../Page/スティーブン・クック.md "wikilink")の造語で、計算機科学者 Nick Pippenger にちなんでいる。

クラス **[P](https://ja.wikipedia.org/wiki/P_\(計算複雑性理論\) "wikilink")** と同様、**NC** に属する問題は並列計算機で効率的に解くことができると見なされている。並列計算機は通常の計算機でシミュレート可能であるため、**NC** は **P** に含まれる。**NC** = **P** かどうかは判っていないが、おそらく違うだろうと言われている。つまり、多項式時間で解ける問題には「本質的に逐次的」なものがあり、並列化によって高速化できないと考えられている。**[NP完全問題](../Page/NP完全問題.md "wikilink")**は効率的に解けないと考えられているように、**P完全問題**は「本質的に並列化不可能」または「本質的に逐次的」であると考えられている。

この定義における並列計算機は「並列ランダムアクセス機械」（[PRAM](https://ja.wikipedia.org/wiki/並列ランダムアクセス機械 "wikilink")）である。これは、共有メモリ型の並列計算機の[計算モデル](https://ja.wikipedia.org/wiki/計算モデル "wikilink")で、全プロセッサがどのメモリ位置についても一定の時間でアクセスできるものと定義されている。**NC** の定義は PRAM において複数のプロセッサが同じメモリ位置にアクセスした場合の対処方法には影響されない。この排他モデルとして CRCW、CREW、EREW がある。詳しくは[PRAMを参照されたい](https://ja.wikipedia.org/wiki/並列ランダムアクセス機械 "wikilink")。

**NC** の別の定義として、[対数多項式](https://ja.wikipedia.org/wiki/対数多項式 "wikilink")の深さと多項式個の論理ゲートからなる[一様ブール回路で解ける決定問題の集合という定義もある](https://ja.wikipedia.org/wiki/論理回路 "wikilink")。

**NC**<sup>*i*</sup> は、多項式個の論理ゲートからなる一様ブール回路（深さ O((log *n*)<sup>*i*</sup>)）で解ける決定問題の集合である。また、多項式個のプロセッサからなる並列計算機上で O((log *n*)<sup>*i*</sup>) 時間で解ける決定問題の集合でもある。

**NC** クラス群と **[L](https://ja.wikipedia.org/wiki/L_\(計算複雑性理論\) "wikilink")** および **[NL](../Page/NL_\(計算複雑性理論\).md "wikilink")** の関係は Papadimitriou 1994, Theorem 16.1 により次のように示される。

\(\mathbf{NC^1 \subseteq L \subseteq NL \subseteq NC^2}\)

同様に、**NC**<sup>*i*</sup> は、[交替性チューリングマシン](https://ja.wikipedia.org/wiki/交替性チューリングマシン "wikilink")で O(log *n*) の領域と (log *n*)<sup>O(1)</sup> 回の交替で解ける決定問題の集合と同じである。

## 参考文献

  - Greenlaw, Raymond, James Hoover, and Walter Ruzzo. *Limits To Parallel computation; P-Completeness Theory*. ISBN 0-19-508591-4

  - Heribert Vollmer. *[Introduction to Circuit Complexity -- A Uniform Approach](http://www.thi.uni-hannover.de/forschung/publikationen/cc/index.en.php)*. ISBN 3-540-64310-9

  - Section 15.3: The class **NC**, pp.375–381.

  - Lecture 12: Relation of *NC* to Time-Space Classes

[Category:計算複雑性理論](https://ja.wikipedia.org/wiki/Category:計算複雑性理論 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")