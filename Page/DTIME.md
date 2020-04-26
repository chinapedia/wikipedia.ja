> この記事は[DTIME](https://ja.wikipedia.org/wiki/DTIME)から翻訳されています。


**DTIME**（または**TIME**）は、[計算複雑性理論](https://ja.wikipedia.org/wiki/計算複雑性理論 "wikilink")における[決定性チューリング機械での計算時間という](../Page/チューリングマシン.md "wikilink")[計算資源](../Page/計算資源.md "wikilink")を表す。実在の一般的コンピュータが、ある問題を特定の[アルゴリズム](../Page/アルゴリズム.md "wikilink")で解くのに要する時間の量（ステップ数）を表す。実際の[リソース](https://ja.wikipedia.org/wiki/リソース "wikilink")（プログラムの実行にかかる時間）と直接対応することから、最もよく研究されている計算資源の1つである。

**DTIME**という資源は[複雑性クラス](https://ja.wikipedia.org/wiki/複雑性クラス "wikilink")の定義に使われる。複雑性クラスとは、ある特定の計算時間量で解ける全ての[決定問題](https://ja.wikipedia.org/wiki/決定問題 "wikilink")の集合である。入力長 *\(n\)* の問題を解くのに *\(O(f(n))\)* の計算時間がかかる場合、その複雑性クラスは **\(\text{DTIME}(f(n))\)**（または **\(\text{TIME}(f(n))\)**）となる。このとき使用するメモリ空間量に制限はないが、他の複雑性尺度は制限されることもある。

## DTIME による複雑性クラス

多くの重要な複雑性クラスが DTIME を使って定義される。それらのクラスは決定性時間のある量を使って解ける問題を含むものである。任意の[時間構成可能関数を使って複雑性クラスを定義できるが](https://ja.wikipedia.org/wiki/構成可能関数 "wikilink")、研究に値するクラスは限られている。一般に、複雑性クラスは計算モデルを変更しても安定していることが望ましく、サブルーチンの合成について閉じているのが望ましい。

DTIME は[時間階層定理](https://ja.wikipedia.org/wiki/時間階層定理 "wikilink")に従う。すなわち、漸近的に多くの時間を指定すると、常により大きな問題の集合が生成される。

よく知られている複雑性クラス **[P](../Page/P_\(計算複雑性理論\).md "wikilink")** は、多項式量の DTIME で解ける問題のクラスである。形式的には以下のように定義される。

\[\text{P} = \bigcup_{k\in\mathbb{N}} \text{DTIME}\left(n^k\right)\]

**P** は線形時間問題 **\(\text{DTIME}(n)\)** を含む最小の安定したクラスである (AMS 2004, Lecture 2.2, pg. 20)。また、**P**は「現実的計算可能」な最大の複雑性クラスの一つと考えられている。

決定性時間を使うより大きなクラスとして **[EXPTIME](https://ja.wikipedia.org/wiki/EXPTIME "wikilink")** がある。**EXPTIME** は決定性機械で[指数関数時間](https://ja.wikipedia.org/wiki/指数関数時間 "wikilink")を使って解ける問題のクラスである。形式的に示せば、以下のようになる。

\[\text{EXPTIME} = \bigcup_{k \in \mathbb{N} } \text{ DTIME } \left( 2^{ n^k } \right) .\]

より大きな複雑性クラスも同様に定義できる。時間階層定理により、これらのクラスは厳密な階層を形成する。例えば \(\text{P}\subsetneq\text{EXPTIME}\) などとなる。

## 計算機械モデル

DTIMEの定義に使われる機械モデルは様々あるが、資源に関する能力に差はない。特に小さい時間クラスを論じる場合、多テープ型のチューリング機械が使われることが多い。多テープ型の決定性チューリング機械は単一テープのチューリング機械に比較しても高々2乗の時間性能の向上にしかならない (Papadimitriou 1994, Thrm. 2.1)。

定数倍の形で表される時間の違いは DTIME によるクラス表現に影響しない。定数倍の性能向上は有限状態制御における状態数を増やすことで実現される。Papadimitriou (1994, Thrm. 2.2) によれば、言語 L について以下のように記されている。

\[\text{L}\in\text{TIME}(f(n))\] であるとき、任意の \(\epsilon>0\) について \(\text{L}\in\text{TIME}\left(f'(n)\right)\) となる。ここで \(f'(n)=\epsilon f(n) + n + 2\) である。

## 一般化

決定性チューリング機械以外のモデルを使って、DTIME を一般化したり制限したりした概念も各種存在する。例えば、[非決定性チューリング機械](https://ja.wikipedia.org/wiki/非決定性チューリング機械 "wikilink")を使った場合、その時間資源は[NTIME](https://ja.wikipedia.org/wiki/NTIME "wikilink")で表される。DTIME や他の計算資源の表現能力の関係は未だよく分かっていない。

## 参考文献

  -
  -
[Category:計算資源](https://ja.wikipedia.org/wiki/Category:計算資源 "wikilink") [Category:複雑性クラス](https://ja.wikipedia.org/wiki/Category:複雑性クラス "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")