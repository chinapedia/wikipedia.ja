> この記事は[NL \(\)](https://ja.wikipedia.org/wiki/NL_\(\))から翻訳されています。


**NL**（えぬえる、）は、[計算複雑性理論](https://ja.wikipedia.org/wiki/計算複雑性理論 "wikilink")における[決定問題](https://ja.wikipedia.org/wiki/決定問題 "wikilink")の[複雑性クラス](https://ja.wikipedia.org/wiki/複雑性クラス "wikilink")の一つである。[非決定性チューリングマシン](https://ja.wikipedia.org/wiki/非決定性チューリングマシン "wikilink")で[対数](../Page/対数.md "wikilink")規模の記憶領域を使って解ける問題がこのクラスに属する。

**NL** は **[L](https://ja.wikipedia.org/wiki/L_\(計算複雑性理論\) "wikilink")**を一般化したものである。**L** は[決定性チューリングマシンでの対数領域問題のクラスである](../Page/チューリングマシン.md "wikilink")。決定性チューリングマシンは非決定性チューリングマシンに含まれるため、**L** も **NL** に含まれる。

**NL**は[非決定性領域](https://ja.wikipedia.org/wiki/NSPACE "wikilink")(NSPACE)の計算資源記法で形式的に定義でき、**NL** = **NSPACE**(log *n*) となる。

計算複雑性理論の研究により、このクラスと他の複雑性クラスの関係が明らかとなり、必要な[計算資源](https://ja.wikipedia.org/wiki/計算資源 "wikilink")も明らかとなってきた。一方、[アルゴリズム](../Page/アルゴリズム.md "wikilink")の研究によって、対数領域で解ける問題も明らかとなってきつつある。しかし、計算複雑性理論の他の分野と同様、**NL**についての重要な部分は未解決である。

**NL**の[確率的定義](https://ja.wikipedia.org/wiki/#確率的定義 "wikilink")（後述）を指して **RL** と呼ぶこともある。しかし、**RL**という名称は**RLP**という複雑性クラスの別名として使われることが多い（**RLP**とは、[確率的チューリングマシン](https://ja.wikipedia.org/wiki/確率的チューリングマシン "wikilink")で対数領域と多項式時間で解ける問題のクラス）。

## NL完全問題

ある複雑性クラスに属する最も難しい問題を指して完全問題という。直観的には、完全問題を効率的に解く方法が判っていれば、それを使ってそのクラスのあらゆる問題を解くことが出来る。すなわち、完全問題はその複雑性クラスの能力の程度を示すものである。

**NL完全**であることが判っている問題はいくつかある。STCON問題（[有向グラフの](../Page/グラフ理論.md "wikilink")2点間の経路の有無を問う問題）と2元[充足可能性問題](https://ja.wikipedia.org/wiki/充足可能性問題 "wikilink")は**NL完全**である。2元充足可能性問題とは、[連言標準形](../Page/連言標準形.md "wikilink")の[論理式](https://ja.wikipedia.org/wiki/論理式 "wikilink")の各節（論理和で表される部分）が2つの変数で構成されているとき、その論理式を真とする変数値の組み合わせが存在するかどうかを問う問題である。以下にそのような論理式の例を示す。なお、\~（チルダ）は「否定」を意味する。

  -
    (*x*<sub>1</sub> or \~*x*<sub>3</sub>) and (\~*x*<sub>2</sub> or *x*<sub>3</sub>) and (\~*x*<sub>1</sub> or \~*x*<sub>2</sub>)

## 包含関係

**NL** は **[P](https://ja.wikipedia.org/wiki/P_\(計算複雑性理論\) "wikilink")**に含まれる。これは、2元充足可能性問題に多項式時間のアルゴリズムが存在していることから明らかである。しかし、**NL** = **P** かどうか、あるいは **L** = **NL** かどうかは未だわかっていない。非決定性領域は補集合演算について閉じているため、**NL** = **co-NL** であることが判っている。これは、Neil Immerman と Róbert Szelepcsényi が 1987年にそれぞれ独自に証明した。彼らはこの業績によって1995年の[ゲーデル賞](https://ja.wikipedia.org/wiki/ゲーデル賞 "wikilink")を受賞している（[PSPACE](https://ja.wikipedia.org/wiki/PSPACE "wikilink")のようなより大きいクラスでは、[サヴィッチの定理](https://ja.wikipedia.org/wiki/サヴィッチの定理 "wikilink")（1970年）により**PSPACE** = **NPSPACE**、**NPSPACE** = **co-NPSPACE**であることが既に知られていた）。

[回路計算量](https://ja.wikipedia.org/wiki/回路計算量 "wikilink")理論では、**NL** は**[NC](https://ja.wikipedia.org/wiki/NC_\(計算複雑性理論\) "wikilink")**の階層に置くことができる。Papadimitriou 1994, Theorem 16.1 によれば、次のようになる。

\[\mathsf{NC_1 \subseteq L \subseteq NL \subseteq NC_2}\]

また、**NL** = **RL** であることも知られている。**RL**は確率的チューリングマシンで対数領域で解ける問題のクラスであり、3分の1未満の確率で間違ってNOと答える可能性のあるクラスである。また、**ZPL** とも同じであることが知られている。**ZPL** は[乱択アルゴリズム](https://ja.wikipedia.org/wiki/乱択アルゴリズム "wikilink")で対数領域で解ける問題のクラスである（誤答はない）。しかし、**RLP**または**ZPLP**とは異なると考えられている。これらは **RL** や **ZPL** を多項式時間に制限したもので、書籍によってはこれらを混同している場合もある。

[サヴィッチの定理](https://ja.wikipedia.org/wiki/サヴィッチの定理 "wikilink")を使って **NL** を決定性領域に関連付けることもできる。つまり、非決定性アルゴリズムは、決定性機械で高々二乗の領域を使うことでシミュレートできる。サヴィッチの定理によれば、\(\mathbf{NL \subseteq SPACE}(\log^2 n)\) となる（\(\mathbf{NL \subseteq L}^2\) と同じことである）。この強力な原理は1994年に知られるようになった（Papadimtriou 1994 Problem 16.4.10, "Symmetric space"）。

## 確率的定義

[確率的チューリングマシン](https://ja.wikipedia.org/wiki/確率的チューリングマシン "wikilink")上で対数領域で解ける問題の[複雑性クラス](https://ja.wikipedia.org/wiki/複雑性クラス "wikilink")を *C* とする。*C* の回答がYESである場合は常に正しいが、回答がNOである場合は3分の1未満の確率で間違った回答だとする。3分の1という定数は、0 ≤ *x* \< 1/2 となる任意の *x* であればよい。

このようなクラスは **NL** と同じである。*C* は時間が多項式時間に制限されていない。なぜなら、対数領域の状態の組み合わせがたかだか多項式で表せるほどしかないとしても、確率的な解法であるために無限ループに陥る可能性があるからである。これを多項式時間に制限すると **RLP** という別のクラスになる。

*C* = **NL** であることを示す。まず *C* が **NL** に含まれることを簡単に示すアルゴリズムが存在する。

  - ある文字列がある言語に含まれない場合、*C* も **NL** も全計算経路でこれらを拒否（reject）する。
  - 文字列が言語に含まれる場合、**NL**のアルゴリズムはそれを少なくとも1つの計算経路で受容（accept）し、*C* のアルゴリズムは少なくとも3分の2の計算経路で受容する。

**NL** が *C* に含まれることを示すため、一つの **NL**アルゴリズムで長さ *n* の計算経路を無作為に選び、これを 2<sup>*n*</sup> 回行う。計算経路は長さ *n* を超えず、全体として 2<sup>n</sup> 個の計算経路があるため、一定確率以上で受容状態となる可能性がある。

問題は、最大値が 2<sup>*n*</sup> となるカウンタを保持する領域が対数領域にないことである（O(*n*)になる）。これに対処するため、カウンタをランダムカウンタとし、単純に *n* 個のコインを投げて全部のコインが表なら停止または拒否するものとする。この事象の確率は 2<sup>-n</sup> なので、停止するまでの平均ステップ数の[期待値](../Page/期待値.md "wikilink")は 2<sup>*n*</sup> となる。この場合に必要な領域は対数領域に収まる（表になるコインを数えるだけなら O(log *n*) に収まる）。

以上から、領域だけに着目すれば、確率的なアルゴリズムも非決定性のアルゴリズムも同じ能力を持つことがわかる。

## 記述計算量

**NL**の簡単な論理的定義として、[推移閉包](https://ja.wikipedia.org/wiki/推移閉包 "wikilink")演算子を付与した[一階述語論理](https://ja.wikipedia.org/wiki/一階述語論理 "wikilink")で表される言語が**NL**に含まれる。

## 参考文献

  -
  -
  - [Introduction to Complexity Theory: Lecture 7](http://www.wisdom.weizmann.ac.il/~oded/PS/CC/l7.ps). Oded Goldreich. Proposition 6.1. 本文で *C* と称していたものは、この文書では badRSPACE(log n) となっている。

[Category:計算複雑性理論](https://ja.wikipedia.org/wiki/Category:計算複雑性理論 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")