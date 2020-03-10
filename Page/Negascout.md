> この記事は[Negascout](https://ja.wikipedia.org/wiki/Negascout)から翻訳されています。


**NegaScout** または **PVS** (Principal Variation Search) は Alexander Reinefeld によって考案された [アルファ・ベータ法](../Page/アルファ・ベータ法.md "wikilink")よりも効率の良い[ミニマックス法](https://ja.wikipedia.org/wiki/ミニマックス法 "wikilink")アルゴリズムの一種である。

NegaScout は手の選択肢を列挙し何らかの方法で並び替えた上で、初めに最も良さそうな手を通常の探索窓で[探索](https://ja.wikipedia.org/wiki/探索 "wikilink")し評価値を得る。 それ以降の手はまず [Null Window Search](https://ja.wikipedia.org/wiki/MTD-f#Null_Window_Search "wikilink") を行いそれまでに見つかった最善手の評価値を超えるかどうかを調べ、 超えた場合にのみあらためて通常の探索窓で再探索し評価値を得る。 但し、得られた評価値がβ値以上でもあれば再探索を行わずその場でカットできる。 Null Window Searchは探索窓が狭くカットが頻繁に起こるため通常の探索よりも短時間で終了するが、 探索順序がランダムだと再探索が頻繁に起こり、結局はアルファ・ベータ法よりも時間が掛かってしまう。 この様に NegaScout が効率よく機能するかどうかは手の並べ替えの精度に依存しており、初めに調べる手が最善手である場合に最も効率が良くなる。 その際よく用いられる方法としては、浅い探索の結果による並び替えがある。

チェスプログラムではアルファ・ベータ法に比べ、典型的には10％程度のパフォーマンス上昇が見込めると言われる。 後にさらに少ない探索量が期待できる[MTD(f)と呼ばれる探索法も考案されたが](../Page/MTD-f.md "wikilink")、 置換表に強く依存するなどの性質を避けるために今日のチェスプログラムでも NegaScout は広く使われている。 また、MTD(f)の基礎となった[SSS\*](https://ja.wikipedia.org/wiki/SSS* "wikilink")と呼ばれる[最良優先探索](https://ja.wikipedia.org/wiki/最良優先探索 "wikilink")アルゴリズムもあるが、 探索する[ゲーム木](https://ja.wikipedia.org/wiki/ゲーム木 "wikilink")によっては NegaScout と比べ探索量が増えたりもする事や、 最良優先探索の性質である多くのメモリを必要とする事などの問題があるため普及していない。

## Fail-Soft

通常のアルファベータ法が返す値は探索窓の範囲内の値であるが、 子ノードを探索した結果が探索窓の範囲外だった場合、 探索窓の境界値ではなく実際に出現した子ノードの最大値を返すと探索量が減る事がある。 これは親ノードに伝わったときにβ値以上となってカットしたりα値を更新して探索窓を狭めたりできる可能性が高くなるためである。 このような性質を Fail-Soft と言い、 Null Window Search などの狭い探索窓による探索や置換表を使った探索をする場合にその効果がよく現れる。

## 擬似コード

以下に NegaScout の擬似コードを示す。

` `**`function`**` NegaScout( node, α, β, depth ) {`
`     `**`if`**` ( node.IsLeafNode || depth == 0 )`
`         `**`return`**` Evaluate( node ); /* 終端ノードなので現在のノードを評価する */`
` `
`     node.ExpandChildNode(); /* 手を列挙 */`
`     node.MoveOrdering(); /* 手の並べ替え */`
` `
`     child = node.GetNextChild(); `
`     max = v = -NegaScout ( child, -β, -α, depth - 1 ); /* 最善候補を通常の窓で探索 */`
`     `**`if`**` ( β <= v ) `**`return`**` v; /* カット */`
`     `**`if`**` ( α < v ) α = v;`
` `
`     `**`while`**` ( ( child = node.GetNextChild() ) != `**`null`**` ){`
`         v = -NegaScout ( child, -α - 1, -α, depth - 1 ); /* Null Window Search */`
`         `**`if`**` ( β <= v ) `**`return`**` v; /* カット */`
`         `**`if`**` ( α < v ) {`
`             α = v;`
`             v = -NegaScout( child, -β, -α, depth - 1 ); /* 通常の窓で再探索 */`
`             `**`if`**` ( β <= v ) `**`return`**` v; /* カット */`
`             `**`if`**` ( α < v ) α = v;`
`         }`
`         `**`if`**`( max < v ) max = v;`
`     }`
`     `**`return`**` max; /* 子ノードの最大値を返す (fail-soft) */`
` }`

## 参考文献

  - Alexander Reinefeld. Spielbaum-Suchverfahren. Informatik-Fachbericht 200, Springer-Verlag, Berlin (1989), ISBN 3-540-50742-6

[Category:最適化アルゴリズム](https://ja.wikipedia.org/wiki/Category:最適化アルゴリズム "wikilink")