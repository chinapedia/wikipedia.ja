> この記事は[MTD-f](https://ja.wikipedia.org/wiki/MTD-f)から翻訳されています。


**MTD(f)** は MTD(n, f) (Memory-enhanced Test Driver with node n and value f) の略で、[アルファ・ベータ法](../Page/アルファ・ベータ法.md "wikilink")や[NegaScoutよりも効率の良い](../Page/Negascout.md "wikilink")[ミニマックス法](../Page/ミニマックス法.md "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")の一種である。 MTD(f) は、ミニマックス値を見積もった値 f から、 Null Window Search を何度も繰り返す事で実際のミニマックス値に向けて近づいていく探索法である。 ミニマックス値が見つかると、再び Null Window Search を行っても同じ値が返るようになるので、これを探索の終了条件とする。

## 擬似コード

以下に MTD(f) の擬似コードを示す。

` node：探索開始ノード`
` f：ミニマックス値を見積もった値`
` depth：探索の最大深さ`
` `
` `**`function`**` MTDF( node, f, depth ) {`
`     g = f;`
`     upperBound = +∞;`
`     lowerBound = -∞;`
`     `**`while`**` ( lowerBound < upperBound ) {`
`         `**`if`**` ( g == lowerBound )`
`             β = g + 1;`
`         `**`else`**
`             β = g;`
`         /* 置換表付きアルファ・ベータ法で Null Window Search を行う*/`
`         g = AlphaBetaWithMemory( node, β - 1, β, depth );`
`         `**`if`**` ( g < β )`
`             upperBound = g;`
`         `**`else`**
`             lowerBound = g;`
`     }`
`     `**`return`**` g;`
` }`

## Null Window Search

Zero Window Search とも。 アルファ・ベータ法やそれを改良した探索法におけるα（下限値）とβ（上限値）の幅を Window (探索窓)といい、 この幅を Null(Zero) にして行う探索を Null Window Search と言う。（但し、通常の実装では Null Window の幅は１とする。） 十分広い探索窓を設定して探索をすれば返る値はミニマックス値であるが、 狭い探索窓を設定して探索をすると、ミニマックス値がその範囲内に無い場合、探索窓の上限値以上の評価値が返る事がある。 この状態を fail-high といい、これはミニマックス値がその評価値以上である事を示している。 また、同様に探索窓の下限値以下の評価値が返る事もある。 この状態を fail-low といい、こちらはミニマックス値がその評価値以下である事を示している。 つまりNull Window Searchを行えばミニマックス値の存在範囲を知ることができる。 このような探索は MTD(f) だけでなく NegaScout法でも使われている。

## 置換表付きアルファ・ベータ法

MTD(f)はその性質上、何度も同じノードを展開するので、効率改善のために置換表付きアルファ・ベータ法が用いられる。 置換表に前回の計算結果（探索窓の上限値や下限値）を保持しておく事で再探索時の計算を削減する事ができる。 以下に置換表付きアルファ・ベータ法の擬似コードを示す。

` node：探索ノード`
` α：探索ノード評価値の下限値`
` β：探索ノード評価値の上限値`
` depth：探索の最大深さ`
` `
` `**`function`**` AlphaBetaWithMemory( node, α, β, depth ){`
`     /* 置換表に前回の計算結果があれば利用する。 */`
`     `**`if`**` ( table.Contains( node ) ) {`
`         lowerBound = table.GetLowerBound( node );`
`         `**`if`**` ( β <= lowerBound ) /* fail-high */`
`             `**`return`**` lowerBound; /* カット */`
`         upperBound = table.GetUpperBound( node );`
`         `**`if`**` ( upperBound <= α ) /* fail-low */`
`             `**`return`**` upperBound; /* カット */`
`         /* 探索窓を狭められる事がある。 */`
`         α = Max( α, lowerBound );`
`         β = Min( β, upperBound );`
`     }`
`     `**`if`**` ( depth == 0 || node.IsLeafNode ) {`
`         /* 現在のノードを評価する。 */`
`         g = Evaluate( node );`
`     } `**`else`**` {`
`         node.ExpandChildNodes();`
`         `**`if`**` ( node.IsMyNode ) {`
`             /* node が自分のノード。子ノードを探索し最大値を得る。*/`
`             g = -∞;`
`             a = α;`
`             `**`while`**` ( ( child = node.GetNextChild() ) != null ) {`
`                 g = Max( g, AlphaBetaWithMemory( child, a, β, depth - 1 ) );`
`                 `**`if`**` ( β <= g ) { // fail high`
`                     /* ミニマックス値は g 以上なので g を下限値として置換表に登録する。 */`
`                     table.StoreLowerBound( node, g );`
`                     return g; /* カット */`
`                 }`
`                 a = Max( a, g );`
`             }`
`         } `**`else`**` {`
`             /* node が相手のノード。子ノードを探索し最小値を得る。 */`
`             g = +∞;`
`             b = β;`
`             `**`while`**` ( ( child = node.GetNextChild() ) != null ) {`
`                 g = Min( g, AlphaBetaWithMemory( child, α, b, depth - 1 ) );`
`                 `**`if`**` ( g <= α ){ /* fail low */`
`                     /* ミニマックス値は g 以下なので g を上限値として置換表に登録する。 */`
`                     table.StoreUpperBound( node, g );`
`                     return g; /* カット */`
`                 }`
`                 b = Min( b, g );`
`             }`
`         }`
`     }`
`     /* α < g < β の場合。 Null Window Search の場合にここが実行される事は無い。 */`
`     table.StoreUpperBound( node, g );`
`     table.StoreLowerBound( node, g );`
`     `**`return`**` g;`
` }`

## パフォーマンス

MTD(f)は、チェス\[[http://portal.acm.org/citation.cfm?id=240998\&coll=GUIDE\&dl=GUIDE\&CFID=50049687\&CFTOKEN=16181537\]などのゲームに於いて](http://portal.acm.org/citation.cfm?id=240998&coll=GUIDE&dl=GUIDE&CFID=50049687&CFTOKEN=16181537%5Dなどのゲームに於いて) NegaScout法などの探索アルゴリズムよりも探索ノード数が少なくて済む事が示されている。 しかし置換表に強く依存する事や、探索の非安定性などの問題が存在するので、 現在のチェスプログラムではNegaScout法もいまだに広く使われている。

## 外部リンク

  - [Aske Plaat: MTD(f), a new chess algorithm](http://home.tiscali.nl/askeplaat/mtdf.html) MTD(f)アルゴリズムの解説(英語)

[Category:最適化アルゴリズム](https://ja.wikipedia.org/wiki/Category:最適化アルゴリズム "wikilink")