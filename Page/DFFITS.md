> この記事は[DFFITS](https://ja.wikipedia.org/wiki/DFFITS)から翻訳されています。


**DFFITS** は[統計学](../Page/統計学.md "wikilink")の[回帰分析](../Page/回帰分析.md "wikilink")において、ある点の影響度を示す[統計量](https://ja.wikipedia.org/wiki/統計量 "wikilink")である。1980年に出版されたベルスレー、クー、ウェルシュ共著の『回帰診断：影響の強いデータと共線形性の源泉を同定する』\[1\]で提案された。

DFFITS は 問題の点を回帰から外した場合の予測（回帰）値の変化 "DFFIT" を問題の点での当てはめの標準偏差の推定値で割って（[スチューデント化](https://ja.wikipedia.org/wiki/ウィリアム・ゴセット "wikilink")、'S'）したものである。

\[\text{DFFITS} = {\widehat{y_i} - \widehat{y_{i(i)}} \over s_{(i)} \sqrt{h_{ii}}}.\]

ここで \(\widehat{y_i}\) と \(\widehat{y_{i(i)}}\) は点 i が回帰に含まれた場合と除かれた場合の予測値である。\(s_{(i)}\) は問題の点を含まずに推定された標準誤差の値である。\(h_{ii}\) は その点の[てこ値](https://ja.wikipedia.org/wiki/てこ値 "wikilink") である。

DFFITS は[外部スチューデント化残差に似ている](https://ja.wikipedia.org/wiki/スチューデント化残差#内部スチューデント化と外部スチューデント化 "wikilink")。実はそれを\(\sqrt{h_{ii}/(1-h_{ii})}\)　倍したものである\[2\]。誤差が[正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")するとき、外部スチューデント化残差はスチューデントの[t分布](https://ja.wikipedia.org/wiki/t分布 "wikilink")（[自由度は](https://ja.wikipedia.org/wiki/自由度#統計学 "wikilink")（残差の自由度−1））する。ある点での DFFITS とその点でのテコ因子 \(\sqrt{h_{ii}/(1-h_{ii})}\) との積は同じt分布をする。したがって、テコ値の小さい点では DFFITS は小さいことが期待され、テコ値が 1 に近づくと DFFITS 値の分布は無限に広がる。

完全に均衡のとれた実験計画、たとえば（や均衡部分因子計画）の場合、各点でのテコ値は \(p/n\) 、すなわち[母数](https://ja.wikipedia.org/wiki/母数 "wikilink")の個数を点の個数で割ったものである。これは DFFITS 値が（正規分布の場合）\(\sqrt{p \over n-p} \approx \sqrt{p \over n}\) と t 変数の積である。したがって、同書の著者は DFFITS が \(2\sqrt{p \over n}\) より大きい場合を外れ点としてチェックすることを薦めている。

類似の量にがある。

## 文献

[Category:回帰診断](https://ja.wikipedia.org/wiki/Category:回帰診断 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.
2.