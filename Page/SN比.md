> この記事は[SN](https://ja.wikipedia.org/wiki/SN)から翻訳されています。


**SN比**（エスエヌひ）は、**通信理論**ないし[情報理論](../Page/情報理論.md "wikilink")あるいは[電子工学](../Page/電子工学.md "wikilink")などで扱われる値で、[信号](../Page/信号_\(電気工学\).md "wikilink") () と[雑音](https://ja.wikipedia.org/wiki/雑音 "wikilink") () の[比](../Page/比.md "wikilink")である。

**信号雑音比** () または **信号対雑音比** () の略。**S/N比**、**SNR**、**S/N**とも略す。

、 ともいう。

SN比が高ければ伝送における雑音の影響が小さく、SN比が小さければ影響が大きい。SN比が大きいことをSN比がよい、小さいことを悪いとも言う。

## 定義

SN比は、信号の[分散を雑音の分散で割った値である](../Page/分散_\(確率論\).md "wikilink")。

SN比で考える信号と雑音の定義は、何に着目しているかによる。見方によっては、通常「雑音」とされている成分に着目する場合など、逆転することさえありうる。雑音は[確率過程](../Page/確率過程.md "wikilink")とも限らない。

また、考えるのは、真の信号*S* と真の雑音*N* の分散である。真の値が得られず測定値しかない場合は、不偏分散で代用する必要がある（データ数が多い場合はほとんど影響しないが）。実測されるのは *S* +*N* であり、これと *S* を混同しない注意も必要である。

数式では

\[S / N = \frac{ P_\mathrm S }{ P_\mathrm N } = \left ( \frac{ A_\mathrm S }{ A_\mathrm N } \right )^2,\]

  -
    *P* = 信号電力、
    *P* = 雑音電力、
    *A* = 信号電圧（電流）の実効値、
    *A* = 雑音電圧（電流）の実効値

と表される。分散は[電気工学](../Page/電気工学.md "wikilink")では[交流](../Page/交流.md "wikilink")成分の[電力](../Page/電力.md "wikilink")（パワー）となるので、*P* で表している。[平均値](https://ja.wikipedia.org/wiki/平均値 "wikilink")に相当する[直流](../Page/直流.md "wikilink")成分を除いた、交流成分のみを考慮する。*A* は[偏差](../Page/偏差.md "wikilink")の[実効値](../Page/実効値.md "wikilink")（[二乗平均平方根](../Page/二乗平均平方根.md "wikilink")）で、電気工学では交流成分の[電流](../Page/電流.md "wikilink")または[電圧](../Page/電圧.md "wikilink")になる。

分野や[物理量](../Page/物理量.md "wikilink")に関わらず電力やパワーと呼び *P* で表すことが多いが、実際は電力とは限らず、たとえば[映像](https://ja.wikipedia.org/wiki/映像 "wikilink")では[輝度](https://ja.wikipedia.org/wiki/輝度 "wikilink")であり、[測定](../Page/測定.md "wikilink")では[長さ](../Page/長さ.md "wikilink")や[質量](../Page/質量.md "wikilink")などさまざまな物理量でありうる。

## 単位（デシベル）

| dB    | 電力比     | 電流比   |
| ----- | ------- | ----- |
| 0     | 1       | 1     |
| 3.010 | 2       | 1.414 |
| 6.021 | 4       | 2     |
| 10    | 10      | 3.162 |
| 20    | 100     | 10    |
| 40    | 10000   | 100   |
| 60    | 1000000 | 1000  |
| 90    | 10億     | 31623 |

**よく使われる値の対比**

多くの信号は[ダイナミックレンジ](../Page/ダイナミックレンジ.md "wikilink")が非常に広いので、通常SN比は[常用対数](https://ja.wikipedia.org/wiki/常用対数 "wikilink")（10を底にした[対数](../Page/対数.md "wikilink")）で表現される。ただし、単位には[デシベル](../Page/デシベル.md "wikilink") (dB) を使うので、常用対数の10倍の数値になる。電流比率で考えれば20倍である。

\[[S / N]_\mathrm{dB} = 10 \log_{10} \frac { P_\mathrm S }{  P_\mathrm N } = 20 \log_{10} \frac { A_\mathrm S }{ A_\mathrm N }\]

## SN比と通信効率

伝送路の[通信路容量](../Page/通信路容量.md "wikilink")は、ノイズが[正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")の場合、[シャノン＝ハートレーの定理](../Page/シャノン＝ハートレーの定理.md "wikilink")より

\[C \le  B \log_2 \left( 1+\frac{S}{N} \right)\]

で表される。*B* は[帯域幅](../Page/帯域幅.md "wikilink")である。等号は通信方式が理想的な場合に成り立つ。

SN比が高いほど通信効率がよくなる。また \(S \gg N\) ならば

\[C \le 0.332 [S / N]_\mathrm{dB} B\]

と表せ、通信効率はSN比をデシベルで表した値に比例する。

## その他の信号対雑音比

SN比以外にも、信号と雑音の比率を表す方法がある。

### 搬送波対雑音比（CN比）

「信号」を[搬送波](https://ja.wikipedia.org/wiki/搬送波 "wikilink")とした場合は、[搬送波対雑音比](https://ja.wikipedia.org/wiki/搬送波対雑音比 "wikilink")（）あるいは C/N （シーエヌ、CN比、CNR とも）といい、[デジタル信号](../Page/デジタル信号.md "wikilink")伝送では主にこちらを使う。

### 搬送波対干渉波比（CI比）

搬送波と干渉波の比率をと呼ぶ。ラジオなどの無線通信において、他のチャネルをノイズ源（干渉波）とするときなどに使われる。

### ピーク信号対雑音比（PSNR）

最大電力と雑音の比率を[ピーク信号対雑音比](https://ja.wikipedia.org/wiki/ピーク信号対雑音比 "wikilink")（PSNR: ）と呼ぶ。

### Eb/N0

1ビット当たりの信号電力と雑音密度の比を () と呼ぶ。

### SINAD

SN比の計算式において、雑音電力の項に機器が生じる歪み電力を加えたものを[SINAD](https://ja.wikipedia.org/wiki/SINAD "wikilink")と呼ぶ。受信機（特にFM）の出力雑音を表すために用いる。

## 脚注

## 参考文献

  -
## 関連項目

  - [ノイズ](../Page/ノイズ.md "wikilink")
  - [量子化雑音](https://ja.wikipedia.org/wiki/量子化雑音 "wikilink")
  - [SNDR](https://ja.wikipedia.org/wiki/SNDR "wikilink")
  - [音質](https://ja.wikipedia.org/wiki/音質 "wikilink")
  - [明瞭度](https://ja.wikipedia.org/wiki/明瞭度 "wikilink")

[Category:無次元数](https://ja.wikipedia.org/wiki/Category:無次元数 "wikilink") [Category:情報理論](https://ja.wikipedia.org/wiki/Category:情報理論 "wikilink") [Category:データ転送](https://ja.wikipedia.org/wiki/Category:データ転送 "wikilink") [Category:無線工学](https://ja.wikipedia.org/wiki/Category:無線工学 "wikilink")