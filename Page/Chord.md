> この記事は[Chord](https://ja.wikipedia.org/wiki/Chord)から翻訳されています。


**Chord**は、[分散ハッシュテーブル](../Page/分散ハッシュテーブル.md "wikilink")を実現する[アルゴリズム](../Page/アルゴリズム.md "wikilink")の一つ。[P2P](https://ja.wikipedia.org/wiki/ピア・ツー・ピア "wikilink")[ネットワークにおいて](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")、[サーバ](../Page/サーバ.md "wikilink")を用いることなく高速にコンテンツの検索、[ルーティング](../Page/ルーティング.md "wikilink")を行う手法。

## アルゴリズム

Chordでは、コンテンツの[ハッシュ値を求める関数に](../Page/ハッシュ関数.md "wikilink")[SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink")を採用するのが一般的である。ネットワークに参加するノードは、SHA-1のハッシュ値の[値域](https://ja.wikipedia.org/wiki/値域 "wikilink")\(0 \le NodeID \le 2^{160}-1\)を満たす一意な\(NodeID\)が割り当てられる。

ここで、\(next(x)\)という関数を定義する。この関数は、ハッシュ値\(x\)が与えられたとき、値を増加させる方向で次に存在しているノードの\(NodeID\)を返す。なお、\(2^{160}-1\)と\(0\)は接続されていると考える。

ネットワークで情報を共有する際には、共有したい情報のハッシュ値を\(x\)として\(NodeID = next(x)\)を満たす\(NodeID\)を持つノードが、実際に情報を保持しているノードの位置を示す[IPアドレス](../Page/IPアドレス.md "wikilink")等の情報を保持する。

また、ネットワークに参加するノードは、自身の\(NodeID\)を\(MyNodeID\)とした場合、

\(next(Z)\), ただし\(Z=MyNodeID+2^{i}mod2^{160}(0 \le i < 160)\)

の\(NodeID\)をもつノードのIPアドレスをルーティングテーブルとして保持する。

共有されている情報を検索する際には、検索したい情報のハッシュ値を\(y\)としたとき、\(NodeID\)として\(next(y)\)が割り当てられているノードを各ノードのルーティングテーブルを利用して検索することになる。

## 参考文献

  -
## 外部リンク

  - [Chord project](http://pdos.csail.mit.edu/chord/) Chord を使ってP2Pネットワークを構築するプロジェクト

[Category:P2P](https://ja.wikipedia.org/wiki/Category:P2P "wikilink") [Category:アルゴリズム](https://ja.wikipedia.org/wiki/Category:アルゴリズム "wikilink") [Category:分散処理](https://ja.wikipedia.org/wiki/Category:分散処理 "wikilink") [Category:分散データ共有](https://ja.wikipedia.org/wiki/Category:分散データ共有 "wikilink")