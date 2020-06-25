> この記事は[A\*](https://ja.wikipedia.org/wiki/A\*)から翻訳されています。


[Astar_progress_animation.gif](https://ja.wikipedia.org/wiki/File:Astar_progress_animation.gif "fig:Astar_progress_animation.gif") **A\*（A-star, エースター）探索アルゴリズム**は、[グラフ](https://ja.wikipedia.org/wiki/グラフ "wikilink")[探索](../Page/探索.md "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")の一つ。 [最良優先探索](../Page/最良優先探索.md "wikilink")を拡張した[Z\*](https://ja.wikipedia.org/wiki/Z* "wikilink")に、さらにf値として「現時点までの距離」gと「ゴールまでの推定値」hの和を採用したもの。\[1\] h は ヒューリスティック関数と呼ばれる。

## 概要

A\* アルゴリズムは、「グラフ上でスタートからゴールまでの道を見つける」というグラフ探索問題において、 ヒューリスティック関数 *h(n)* という探索の道標となる関数を用いて探索を行うアルゴリズムである。hは各頂点nからゴールまでの距離のある妥当な推定値を返す関数で、解くグラフ探索問題の種類に応じてさまざまなhを設計することが出来る。 例えば、カーナビなどで用いられる単純な二次元の地図での探索では、hとしてユークリッド距離 \(\sqrt{x^2 + y^2}\) を使うことができ、この値は道に沿った実際の距離のおおまかな予測になっている。しかし、高次元空間でのグラフ探索を効率的に行うためには、より高度に設計された関数を用いる必要がある。例えば、[15パズル](../Page/15パズル.md "wikilink")においては[マンハッタン距離](../Page/マンハッタン距離.md "wikilink")や[パターンデータベース](https://ja.wikipedia.org/wiki/パターンデータベース "wikilink")、[STRIPS](https://ja.wikipedia.org/wiki/STRIPS "wikilink")プランニングにおいては[FFヒューリスティック](https://ja.wikipedia.org/wiki/FFヒューリスティック "wikilink")\[2\],[Merge-and-Shrink](https://ja.wikipedia.org/wiki/Merge-and-Shrink "wikilink")\[3\],[Landmark-Cut](https://ja.wikipedia.org/wiki/Landmark-Cut "wikilink")\[4\] などがある。

A\* アルゴリズムは、[ダイクストラ法](../Page/ダイクストラ法.md "wikilink")を推定値付きの場合に一般化したもので、h が恒等的に0である場合はもとのダイクストラ法に一致する。

A\*の探索効率はhの正確さに左右される。 もしもhがまったくでたらめな値を返すならば、探索はゴールとはあさっての方向に進んでしまい、現実的な時間内(一時間、一週間、一年)では解を発見できない場合がある。しかし、いくらおかしな方向に探索が進んだとしても、いつかは必ず解を発見できる保証がある(完全性)。 一方、hが常に正しい値*h\**を返す場合、計算機は「迷うこと無く=分岐をすること無く」グラフ上の最短経路を発見することができる。そのようなhのことを、パーフェクト・ヒューリスティクスとよぶ\[5\]。 現実に用いられる有用なhは、これらの中間の位置にある。

## 歴史

A\* アルゴリズムは[1968年](https://ja.wikipedia.org/wiki/1968年 "wikilink")に [Peter E. Hart](https://ja.wikipedia.org/wiki/:w:Peter_E._Hart "wikilink")、[Nils J. Nilsson](https://ja.wikipedia.org/wiki/:w:Nils_John_Nilsson "wikilink")、[Bertram Raphael](https://ja.wikipedia.org/wiki/:w:Bertram_Raphael "wikilink") の三人が発表した論文\[6\]の中で最初に記述された。A\* というこの一風変わった名前は、この論文でスタートからゴールまでの最短経路を確実に見つけるアルゴリズムを**許容的** () と呼び、論文の数式中に 許容的なアルゴリズムの[集合](../Page/集合.md "wikilink")を **A** と表し、その**A**の中でも評価回数が最適になる物を **A<sup>\*</sup>** と表記していたためである\[7\]。

## A\*の考え方

スタートノードから、あるノード *n* を通って、ゴールノードまでたどり着くときの最短経路を考える。このときこの最短経路のコストを *f\* (n)* とおくと、

  -
    *f\* (n)= g\* (n) + h\* (n)*

と置くことが出来る。ここで *g\* (n)* はスタートノードから *n* までの最小コスト、*h\* (n)* は*n* からゴールノードまでの最小コストである。もし *g\* (n)* の値と *h\* (n)*の値を知っていれば、全体の最短経路*f\* (n)* は容易に求まる。しかしながら実際には *g\* (n)* と *h\* (n)* をあらかじめ与えることは出来ない。そこで *f\* (n)* を次のような推定値 *f (n)* に置き換えることを考える。

\[f(n) = g(n) + h(n)\]

ここで *g(n)* はスタートノードから *n* までの最小コストの推定値、*h(n)* は *n* からゴールノードまでの最小コストの推定値である。この場合 *g* に関しては探索の過程で更新を加えることにより*g\**に近づけてゆくことができるが、 *h\** は、実際にゴールに辿り着くまでは誰にもわからない。そこで、 *h(n)* には人間が(ある程度妥当性を持つように)設計した推定値を与えることにする。このアルゴリズムを **A\*探索アルゴリズム**といい、 *h (n)* を[ヒューリスティック](https://ja.wikipedia.org/wiki/ヒューリスティック "wikilink")関数という。

## アルゴリズムの流れ

A\* のアルゴリズムの実装を以下に示す。このOPENリスト実装は後に述べるように遅いことを記しておく。

1.  スタートノード（\(S\) ）を作成する。また計算中のノードを格納しておくための[優先度付きキュー](../Page/優先度付きキュー.md "wikilink") **OPENリスト**と、計算済みのノードを格納しておく**CLOSEリスト**を用意する。(名前は「リスト」だが、これらの実際のデータ構造は必ずしも[連結リスト](../Page/連結リスト.md "wikilink")である必要はない。)
2.  ゴールは必ずしも１つである必要はないので、ゴール条件を満たすノード集合を \(G\) と呼ぶことにする。
3.  スタートノードをOpenリストに追加する、このとき \(g(S)\) = \(0\) であり \(f(S)\) = \(h(S)\) となる。また Closeリストは空にする。
4.  Openリストが空なら探索は失敗とする（スタートからゴールにたどり着くような経路が存在しなかったことになる）。
5.  Openリストに格納されているノードの内、最小の \(f(n)\) を持つノード \(n\) を1つ取り出す。同じ\(f(n)\)を持つノードが複数ある場合、タイブレーク手法によりどれかのノードを選択する。
6.  \(n \in G\) であるなら探索を終了する。それ以外の場合は \(n\) を Close リストに移す。
7.  \(n\) に隣接している全てのノード（ここでは隣接ノードを \(m\) とおく）に対して以下の操作を行う
    1.  \(f'(m) = g(n) + COST(n,m) + h(m)\) を計算する、ここで \(COST(n,m)\) はノード n から m へ移動するときのコストである。また g(n) は \(g(n) = f(n) - h(n)\) で求めることができる。
    2.  m の状態に応じて以下の操作を行う
          - m が Openリストにも Closeリストにも含まれていない場合 \(f(m) \leftarrow f'(m)\) とし m を Openリストに追加する。このとき m の親を n として記録する。
          - m が Openリストにある場合、\(f'(m) < f(m)\) であるなら、m をOpenから削除し、\(f(m) \leftarrow f'(m)\) に置き換え、再びOpenに挿入する(Openが正しくソートされていることを保証するため)。また、記録してある m の親を n に置き換える。
          - m が Closeリストにある場合、\(f'(m) < f(m)\) であるなら \(f(m) \leftarrow f'(m)\) として m を Openリストに移動する。また記録してある m の親を n に置き換える。
8.  3 以降を繰り返す。
9.  探索終了後、発見されたゴール \(n_G\) から親を順次たどっていくと S から ゴール \(n_G\) までの最短経路が得られる。

以上の流れを見れば、アルゴリズムが手続き的で、並列化が非常に難しいことがわかる。しかし、近年では [HDA\*](https://ja.wikipedia.org/wiki/HDA* "wikilink")\[8\], [PBFS](https://ja.wikipedia.org/wiki/PBFS "wikilink") などの並列手法が開発され、特にHDA\*は768コア以上の大規模並列計算環境にもスケールすることが実証されている。

## 実際に使われているOPEN/CLOSEリストの実装

OPEN/CLOSEリストに登録されているノードの数が多い場合、ノードの展開ごとに子ノードmをOPENからCLOSEへ移動(あるいは逆)するのは非常に高価な操作である。 たとえば、OPEN/CLOSEリストが2分探索木([赤黒木](../Page/赤黒木.md "wikilink")など)で実装されている場合、まずノードの探すのに \(O(log N)\) かかり(ノードのIDで検索)、また削除にも\(O(log N)\)かかる。配列の場合には削除により大きなコストがかかる。

しかし、データ構造を工夫することで、より効率よい実装を行うことが出来る。ノードをOPEN/CLOSEリスト間で行ったり来たりさせる代わりに、以下のように実装する\[9\]:

1.  それぞれのノードに、ノードの状態として OPEN, CLOSE の2種類のタグをもたせる。全てのノードは始めOPENである。
2.  ノードに一意な整数IDをもたせる。
3.  また、IDからノードを\(O(1)\)で参照できる[ハッシュテーブル](../Page/ハッシュテーブル.md "wikilink")を用意する。
4.  OPENにノードを追加する際には、m が Openリストに含まれているかは検証せず、重複を許して追加する。かつ、このときノードではなくIDのみを追加する。
    1.  ID は整数1つ分なので、重複のオーバーヘッドを最小化出来る。
5.  OPENからノードをpopする際、popしたノードの状態がOPENであれば展開を行うが、CLOSEであれば単にスキップする。
    1.  このことにより、重複があっても同じノードを無駄に展開しないようにできる。
    2.  このことにより、OPENリストは、f値による[優先度付きキュー](../Page/優先度付きキュー.md "wikilink")の下に先入れ先出し/[先入れ後出しのキューを用意することで実装できる](https://ja.wikipedia.org/wiki/FILO "wikilink")。
    3.  ノードの検索がおこなわれず、かつ削除が先頭あるいは末尾にしかおこらないので、効率的な実装が可能である。
6.  CLOSEリストは使用しない。
7.  f値による優先度付きキューは、辺のコストが1である場合には単にf値ごとの可変配列にしたほうが高速な操作が可能である。
    1.  辺のコストに大幅なばらつきがある場合には、ヒープとして実装したほうがよい。

## 性質

A\*の性質はhの性質によって大きく左右される。

  - A\*はダイクストラの一般化であり、ダイクストラと同様、グラフに負のコストの辺があれば完全性を失う。その場合には[ベルマン–フォード法](https://ja.wikipedia.org/wiki/ベルマン–フォード法 "wikilink")を用いる。
  - h(n) は常に非負でなくてはならない。
  - あるヒューリスティクス h(n) が 全てのノード n について 真のゴール距離 h\*(n) を上回らない場合、hはAdmissible/**許容的**であると言う。

\[\forall n,0 \le h(n) \le h^*(n)\] このとき、A\*の返す経路は[最適](https://ja.wikipedia.org/wiki/最適 "wikilink")、つまり最短経路である。

  - あるヒューリスティクス h(n) について、全てのノード n と、それに隣接しているノード m について \(h(n) \le cost(n,m) + h(m)\) である場合、そのhはconsistent/**無矛盾**であるという。
  - consistent なhは、常にadmissibleである。\[10\]
  - ある２つのヒューリスティック関数 h1, h2 について、 \(\forall n,h_1(n) \le h_2(n)\) が成り立つ時、 h2 は h1 を支配する(dominate)とよぶ。このとき、特に両者が許容的な場合、h2 を用いた探索はより効率的だろうと考えられている。しかし、いくつかのコーナーケースではこのことは成り立たない。\[11\]

このアルゴリズムは[CPU](../Page/CPU.md "wikilink")の使用率、[メモリの使用率など](../Page/主記憶装置.md "wikilink")、計算負荷は高いが、問題に応じた適切なヒューリスティック関数を用いることにより、問題に対しての最適化が可能である。

## 部分問題に分割する場合

[分割統治法](../Page/分割統治法.md "wikilink")のように、部分問題に分割したうえで全体問題を解いた方が効率的な問題もある。A<sup>\*</sup> 同様の通常の状態遷移はどれかがゴールに到達すれば良いので OR と呼び、部分問題に分割する場合は全ての部分問題が解けないといけないので AND と呼ぶと、探索木が AND/OR 木になる。AND で状態を分割する際、ゴールも分割する必要がある。

同じ状態が2度出現した場合に1つのノードにまとめると AND/OR グラフになる。[閉路](../Page/閉路.md "wikilink")のない AND/OR グラフに対する A<sup>\*</sup> アルゴリズムに対応する物が[1968年](https://ja.wikipedia.org/wiki/1968年 "wikilink")に開発され\[12\]、[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")に **AO<sup>\*</sup>アルゴリズム** と命名された\[13\]。閉路のある AND/OR グラフに対する A<sup>\*</sup> アルゴリズムに対応する **A<sub>0</sub>アルゴリズム** は[1976年](../Page/1976年.md "wikilink")に開発された\[14\]。AND ノードのコストを「辺のコスト＋部分問題のコストの最大値」や「辺のコスト＋部分問題のコストの総和」などの単調非減少関数で定義すると\[15\]、ヒューリスティック関数が許容的であれば、A<sup>\*</sup> 同様、最適解が求まる。なお、閉路のない AND/OR グラフは[文脈自由文法](../Page/文脈自由文法.md "wikilink")（タイプ-2 文法）\[16\]、閉路のある AND/OR グラフは制限のない文法（タイプ-0 文法）に1対1対応することが証明されている。

## 関連項目

  - [最良優先探索](../Page/最良優先探索.md "wikilink")
  - [ダイクストラ法](../Page/ダイクストラ法.md "wikilink")
  - [均一コスト探索](../Page/均一コスト探索.md "wikilink")
  - [双方向探索](https://ja.wikipedia.org/wiki/双方向探索 "wikilink")
  - [シェーキー](https://ja.wikipedia.org/wiki/シェーキー "wikilink")

## 参照

[Category:検索アルゴリズム](https://ja.wikipedia.org/wiki/Category:検索アルゴリズム "wikilink") [Category:アルゴリズム](https://ja.wikipedia.org/wiki/Category:アルゴリズム "wikilink") [Category:ゲーム人工知能](https://ja.wikipedia.org/wiki/Category:ゲーム人工知能 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.  Pearl,Judea. "Heuristics: intelligent search strategies for computer problem solving." (1984).
2.  Hoffmann, Jörg, and Bernhard Nebel. "The FF planning system: Fast plan generation through heuristic search." Journal of Artificial Intelligence Research (2001): 253-302.
3.  Hoffmann, Jörg, and Bernhard Nebel. "The FF planning system: Fast plan generation through heuristic search." Journal of Artificial Intelligence Research (2001): 253-302.
4.  Helmert, Malte, and Carmel Domshlak. "Landmarks, critical paths and abstractions: what's the difference anyway?." ICAPS. 2009.
5.  How Good is Almost Perfect?. M Helmert, G Röger - AAAI, 2008
6.
7.
8.  Kishimoto, Akihiro, Alex S. Fukunaga, and Adi Botea. "Scalable, Parallel Best-First Search for Optimal Sequential Planning." ICAPS. 2009.
9.  Burns, E. A., Hatem, M., Leighton, M. J., & Ruml, W. (2012, July). Implementing fast heuristic search code. In Fifth Annual Symposium on Combinatorial Search. <https://www.aaai.org/ocs/index.php/SOCS/SOCS12/paper/view/5404/5173>
10. Russel, Norvig, Artificial intelligence: a modern approach
11. Robert C. Holte. Common Misconceptions Concerning Heuristic Search, SoCS 2010
12.
13.
14.
15.
16.