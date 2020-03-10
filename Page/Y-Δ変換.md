> この記事は[Y-](https://ja.wikipedia.org/wiki/Y-)から翻訳されています。


[Delta-Star_Transformation.svg](https://ja.wikipedia.org/wiki/File:Delta-Star_Transformation.svg "fig:Delta-Star_Transformation.svg") **Y-Δ変換**（ワイ-デルタへんかん、*Y-Δ transform*)、**スターデルタ変換**(*star-delta transform*)、**T-Π変換**(ティ-パイへんかん、*T-Π transform*)とは、Y字型に接続したY接続（Y diagram）[回路](https://ja.wikipedia.org/wiki/回路 "wikilink")と、三角形に接続したΔ接続（Δ diagram）回路が、[等価](https://ja.wikipedia.org/wiki/等価 "wikilink")の回路になるように変換する手法である。回路の形状が[アルファベット](https://ja.wikipedia.org/wiki/アルファベット "wikilink")のY・Tや[ギリシア文字](../Page/ギリシア文字.md "wikilink")のΔに見えることからこの名前がつけられた。なお、[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")ではY接続回路をスター接続(star diagram)回路と呼ぶ。

一部の文献では、Y接続からΔ接続への変換をY-Δ変換と定義し、逆変換(Δ接続からY接続への変換)を、**Δ-Y変換**、**デルタスター変換**、**Π-T変換**と記載している。

## Y-Δ変換の基本

変換は図に示す3端子の回路で行なわれる。それぞれの回路の端子は同一の端子である必要がある。この変換式は、[実数](../Page/実数.md "wikilink")([抵抗](https://ja.wikipedia.org/wiki/抵抗 "wikilink")素子)の場合だけでなく、[複素数](../Page/複素数.md "wikilink")([容量](https://ja.wikipedia.org/wiki/容量 "wikilink")素子、[誘導素子](https://ja.wikipedia.org/wiki/インダクタ "wikilink"))の場合でも成立する。

### Δ回路からY回路への変換

一般に、Y接続回路のある端子に接続される[インピーダンス](../Page/インピーダンス.md "wikilink")Ryは、Δ接続回路で隣接するノードへのインピーダンス\(R'\)と\(R''\)から次のように表される。

\[R_y = \frac{R'R''}{\sum R_\Delta}\]

ただし、\(\sum R_\Delta\)はΔ接続回路の全てのインピーダンスの和である。これから次式が得られる。

\[R_{a} = \frac{R_{ab}R_{ac}}{R_{ab} + R_{bc} + R_{ac}}\]

\[R_{b} = \frac{R_{ab}R_{bc}}{R_{ab} + R_{bc} + R_{ac}}\]

\[R_{c} = \frac{R_{bc}R_{ac}}{R_{ab} + R_{bc} + R_{ac}}\]

  - 上記公式の導出は、以下のように行う。

1\. 並列接続した抵抗値を求める公式から以下の3式を導く

\[R_{a}+R_{b} = \frac{R_{ab}(R_{bc}+R_{ac})}{R_{ab} + (R_{bc} + R_{ac})}\]

\[R_{b}+R_{c} = \frac{R_{bc}(R_{ac}+R_{ab})}{R_{bc} + (R_{ac} + R_{ab})}\]

\[R_{c}+R_{a} = \frac{R_{ac}(R_{ab}+R_{bc})}{R_{ca} + (R_{ab} + R_{bc})}\]

2\. 上記3式の両辺を足して、以下の式を導く

\[R_{a}+R_{b}+R_{c} = \frac{R_{ab}R_{bc}+R_{bc}R_{ac}+R_{ac}R_{ab}}{R_{ab} + R_{bc} + R_{ac}}\]

3\. 元の3式との差を取ることで、インピーダンスを計算する式が導きだせる

例）

\[R_{b}+R_{c} = \frac{R_{bc}(R_{ac}+R_{ab})}{R_{bc} + R_{ac} + R_{ab}}\] との差を取ると、

\[R_{a} = \frac{R_{ab}R_{ac}}{R_{ab} + R_{bc} + R_{ac}}\]

### Y回路からΔ回路への変換

一般に、Δ接続回路のある端子間に接続されるインピーダンス\(R_\Delta\)は、以下の式で表される。

\[R_\Delta = \frac{R_P}{R_\mathrm{opposite}}\]

ただし、\(R_P = R_{a}R_{b}+R_{b}R_{c}+R_{c}R_{a}\)であり、Y接続回路中のインピーダンスの2つの積の和である。\(R_\mathrm{opposite}\)は、\(R_\Delta\)に対抗する辺のインピーダンスである。これから次式が得られる。

\[R_{ab} = \frac{R_{a}R_{b}+R_{b}R_{c}+R_{c}R_{a}}{R_{c}}\]

\[R_{bc} = \frac{R_{a}R_{b}+R_{b}R_{c}+R_{c}R_{a}}{R_{a}}\]

\[R_{ac} = \frac{R_{a}R_{b}+R_{b}R_{c}+R_{c}R_{a}}{R_{b}}\]

## グラフ理論

[グラフ理論](../Page/グラフ理論.md "wikilink")ではY-Δ変換は、グラフ中のYのサブグラフを同等のΔのサブグラフに置き換えることである。この変換はグラフのエッジの数を増加させることは無いが、グラフのノードの数を増加させる。2つのグラフは、Y-Δ変換と逆変換を行い、もとに戻るのであるなら、Y-Δ等価であるという。例えば、[ピータースン・グラフ](https://ja.wikipedia.org/wiki/ピータースン・グラフ "wikilink")はY-Δ等価なクラスである。

[Category:アナログ回路](https://ja.wikipedia.org/wiki/Category:アナログ回路 "wikilink")