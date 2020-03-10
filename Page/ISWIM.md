> この記事は[ISWIM](https://ja.wikipedia.org/wiki/ISWIM)から翻訳されています。


**ISWIM** は、Peter J. Landin が考案し、[1966年](../Page/1966年.md "wikilink")の *Communications of the ACM* 誌で発表した *The Next 700 Programming Languages* で初めて明らかにした抽象[プログラミング言語](../Page/プログラミング言語.md "wikilink")（あるいはプログラミング言語ファミリ）である。名称は "**I**f you **S**ee **W**hat **I** **M**ean" の[頭字語](../Page/頭字語.md "wikilink")に由来する。

実装されたことはないが、その後のプログラミング言語の開発に多大な影響を与えた。特に、[SASL](https://ja.wikipedia.org/wiki/SASL_\(プログラミング言語\) "wikilink")、[Miranda](../Page/Miranda.md "wikilink")、[ML](../Page/ML_\(プログラミング言語\).md "wikilink")、[Haskell](../Page/Haskell.md "wikilink")といった[関数型言語](../Page/関数型言語.md "wikilink")に影響を与えている。

ISWIM は、[ラムダ計算](../Page/ラムダ計算.md "wikilink")の関数型コアを[命令型言語の](../Page/命令型プログラミング.md "wikilink")[糖衣構文](../Page/糖衣構文.md "wikilink")で包んだものである。変更可能な変数と代入と強力な制御機構として Landin の J 演算子を追加してある（J演算子は[継続](https://ja.wikipedia.org/wiki/継続 "wikilink")を可能としたもので、[Scheme](../Page/Scheme.md "wikilink") の call/cc は J 演算子を簡略化したものである）。ラムダ計算に基づいており、[高階関数](https://ja.wikipedia.org/wiki/高階関数 "wikilink")と[静的スコープ](https://ja.wikipedia.org/wiki/静的スコープ "wikilink")の変数を備えている。

ISWIM の[操作的意味論](https://ja.wikipedia.org/wiki/操作的意味論 "wikilink")は Landin の[SECDマシン](https://ja.wikipedia.org/wiki/SECDマシン "wikilink")を使って定義されており、[先行評価](https://ja.wikipedia.org/wiki/先行評価 "wikilink")（eager evaluation）による値渡しを使っている。ISWIM の目標は、より数学的記法に近づけることであったため、Landin は [ALGOL](../Page/ALGOL.md "wikilink") の文の区切りであったセミコロンや `begin` と `end` によるブロックを排除し、[オフサイドルール](../Page/オフサイドルール.md "wikilink")によって字下げでブロックを示すようにした。

ISWIM で特徴的な記法として、節（clause）の利用がある。ISWIM プログラムは、'where' 節を使った1つの式（変数間の等式を含む補助的定義）、条件付きの式、関数定義からなる。ISWIM は、[CPLと共に最初に](https://ja.wikipedia.org/wiki/CPL_\(プログラミング言語\) "wikilink") 'where' 節を使ったプログラミング言語の1つであった。

意味論的特徴としては、既存のデータ型を組み合わせて（場合によっては再帰的に）新たなデータ型を定義可能であったことが挙げられる。これはやや冗長な自然言語的なスタイルであったが、最近の関数型言語にある[代数的データ型](../Page/代数的データ型.md "wikilink")と同じものである。ISWIM では、変数の型は明示的に宣言されず、Landin は（1966年の論文では明記していないが）動的型付けのようなものを想定していたと思われる（[ALGOL](../Page/ALGOL.md "wikilink")よりもむしろ[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")に近い）。もちろん、彼が何らかの[型推論](https://ja.wikipedia.org/wiki/型推論 "wikilink")を開発することを思い描いていたとも考えられる。

ISWIM をそのまま実装する試みはなされなかったが、Art Evan の PAL や John Reynold の G<small>edanken</small> は Landin の J 演算子を含む概念に影響されている。これらはどちらも動的型付けであった。Milner の [ML](../Page/ML_\(プログラミング言語\).md "wikilink") は ISWIM から J 演算子を省いて、型推論を追加したものと評される。またLandinは参考文献に自身の、[SECDマシン](https://ja.wikipedia.org/wiki/SECDマシン "wikilink")を示した"The Mechanical Evaluation of Expression"を載せている。

ISWIM から影響を受けた別の系統として、命令型の機能（代入や J 演算子）を省いた純粋関数型言語がある。この系統は[遅延評価](https://ja.wikipedia.org/wiki/遅延評価 "wikilink")への切り替えが可能となっている。例えば、[SASL](https://ja.wikipedia.org/wiki/SASL_\(プログラミング言語\) "wikilink")、[Miranda](../Page/Miranda.md "wikilink")、[Haskell](../Page/Haskell.md "wikilink") がその系統にあたる。

## 参考文献

  - P. J. Landin [*The Next 700 Programming Languages*](http://scholar.google.com/scholar?hl=en&lr=&cluster=2856797924573721037&um=1&ie=UTF-8&sa=X&oi=science_links&resnum=1&ct=sl-allversions). CACM 9(3):157–65, March 1966.
  - Art Evans. PAL — a language designed for teaching programming linguistics. Proceedings ACM National Conference 1968.
  - J. C. Reynolds. GEDANKEN: a simple typeless language which permits functional data structures and co-routines. Argonne National Laboratory September 1969.
  - Mirjana Ivanović, Zoran Budimac. A definition of an ISWIM-like language via Scheme. ACM SIGPLAN Notices, Volume 28, No. 4 April 1993.

[Category:関数型言語](https://ja.wikipedia.org/wiki/Category:関数型言語 "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")