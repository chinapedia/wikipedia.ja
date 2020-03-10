> この記事は[T](https://ja.wikipedia.org/wiki/T)から翻訳されています。


**t検定**（ティーけんてい）とは、[帰無仮説](https://ja.wikipedia.org/wiki/帰無仮説 "wikilink")が正しいと仮定した場合に、統計量が[t分布](https://ja.wikipedia.org/wiki/t分布 "wikilink")に従うことを利用する[統計学](../Page/統計学.md "wikilink")的[検定法](https://ja.wikipedia.org/wiki/検定法 "wikilink")の総称である。[母集団](../Page/母集団.md "wikilink")が[正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")に従うと仮定する[パラメトリック検定法](https://ja.wikipedia.org/wiki/パラメトリック検定法 "wikilink")であり、t分布が直接、もとの[平均](../Page/平均.md "wikilink")や[標準偏差](../Page/標準偏差.md "wikilink")にはよらない（ただし[自由度](https://ja.wikipedia.org/wiki/自由度 "wikilink")による）ことを利用している。2組の[標本について平均に有意差があるかどうかの検定などに用いられる](../Page/標本_\(統計学\).md "wikilink")。統計的仮説検定の一つ。[日本工業規格](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink")では、「検定統計量が，帰無仮説の下でt分布に従うことを仮定して行う統計的検定。」と定義している\[1\]。

**スチューデントのt検定**（Student's t-test）とも呼ばれるが、これは統計学者の[ウィリアム・ゴセット](../Page/ウィリアム・ゴセット.md "wikilink")が雇用者である[ギネス](https://ja.wikipedia.org/wiki/ギネス "wikilink")ビール社に本名使用を許されず*Student* というペンネームで最初の論文を発表した（[1908年](../Page/1908年.md "wikilink")）ためである。

## 種類

t検定は大きく次のように分けられる。

  - 2つの母集団がいずれも[正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")に従うと仮定したうえでの、[平均](../Page/平均.md "wikilink")が等しいかどうかの検定。
      - 標本が対になっている、つまり1組の標本のメンバー各々と、もう1組の特定のメンバーとの間に特別な関係がある場合（例えば、同じ人に前後2回調査する場合、夫と妻とで比較する場合など）。
      - 標本が独立で、比較する2つの群の[分散が等しいと仮定できる場合](../Page/分散_\(確率論\).md "wikilink")（[等分散性](https://ja.wikipedia.org/wiki/等分散性 "wikilink")の仮定）。
      - 標本が独立で、等分散性が仮定できない（異分散）場合。これは正確には**ウェルチのt検定**と呼ばれる。
  - 正規分布に従う母集団の平均が、特定の値に等しいかどうかの検定。
  - [回帰直線](https://ja.wikipedia.org/wiki/回帰直線 "wikilink")の[勾配](https://ja.wikipedia.org/wiki/勾配 "wikilink")が0と有意に異なるかどうかの検定。

## 方法

### 一群のt検定

母集団の平均値*μ*が特定の値である *μ*<sub>0</sub>と等しいかどうかの帰無仮説を検定する際に使用する。

\[t = \frac{\overline{x} - \mu_0}{s/\sqrt{n}},\]

\(\overline{x}\)は標本平均であり *s*は 標本の[標準偏差](../Page/標準偏差.md "wikilink") である。標本サイズは *n*であり、t検定における自由度は*n* − 1である。

### 回帰分析の係数

次のような回帰分析のモデルを考える。

  -
    \(Y_i = \alpha + \beta x_i + \varepsilon_i,\)

*x*<sub>*i*</sub>, *i* = 1, ..., *n*は既存の説明変数であり、 *α* と *β*は未知の係数である。そして *ε*<sub>*i*</sub>は独立に同一の正規分布に従った期待値0で未知の分散*σ*<sup>2</sup>であるランダムな誤差とする。 *Y*<sub>*i*</sub>, *i* = 1, ..., *n*は観測値である。この際、 *β*がある特定の値*β*<sub>0</sub>と等しいかどうかをテストしたい (多くの場合*β*<sub>0</sub>は 0である。何故なら、*β*が0であれば*x* と *y* に相関性が無いと言う事になり、0以外の値であれば*x* と *y* は相関しているということになる)。

  -
    <math>

\\begin{align} \\widehat\\alpha, \\widehat\\beta & = \\text{least-squares estimators}, \\\\ SE_{\\widehat\\alpha}, SE_{\\widehat\\beta} & = \\text{the standard errors of least-squares estimators}. \\end{align} </math> すると

  -
    <math>

t_\\text{score} = \\frac{\\widehat\\beta - \\beta_0}{ SE_{\\widehat\\beta} } </math>

帰無仮説が正しければ、この数値(t値という)は自由度が*n* − 2のt分布に従う。

  -
    <math>

SE_{\\widehat\\beta} = \\frac{\\sqrt{\\frac{1}{n - 2}\\sum_{i=1}^n (Y_i - \\widehat y_i)^2}}{\\sqrt{ \\sum_{i=1}^n (x_i - \\overline{x})^2 }} </math>

  -
    <math>

\\begin{align} \\widehat\\varepsilon_i & = Y_i - \\widehat y_i = Y_i - (\\widehat\\alpha + \\widehat\\beta x_i) = \\text{residuals} = \\text{estimated errors}, \\\\ \\text{SSE} & = \\sum_{i=1}^n \\widehat\\varepsilon_i^{\\;2} = \\text{sum of squares of residuals}. \\end{align} </math>

すると\(t_\text{score}\) は

  -
    \(t_\text{score} = \frac{(\widehat\beta - \beta_0)\sqrt{n-2}}{ \sqrt{\text{SSE}/\sum_{i=1}^n \left(x_i - \overline{x}\right)^2} }.\)

### 独立二群の平均値の差の検定

一つ目の母集団の平均値*μ*<sub>1</sub>が二つ目の母集団の平均値*μ*<sub>2</sub>と等しいかどうかの帰無仮説を検定する際に使用する。言い換えると*μ*<sub>1</sub>－*μ*<sub>2</sub>＝0かどうかの帰無仮説を検定する。

#### t検定を始める前に

実務的なデータ分析では、母集団が様々な前提を満たしているかどうかを調べるため、以下のような検定をt検定の前段階に行う場合がある。

  - 標本が正規分布に従うかどうかは、[コルモゴロフ-スミルノフ検定](https://ja.wikipedia.org/wiki/コルモゴロフ-スミルノフ検定 "wikilink")や[シャピロ-ウィルク検定](https://ja.wikipedia.org/wiki/シャピロ-ウィルク検定 "wikilink")などの正規性検定によって判断することもできる。
  - 標本の分散が等しいかどうかは、[F検定](https://ja.wikipedia.org/wiki/F検定 "wikilink")、[ルベーン検定](https://ja.wikipedia.org/wiki/ルベーン検定 "wikilink")、[バートレット検定](../Page/バートレット検定.md "wikilink")などにより判断する方法がある。

#### 等分散の場合

比較する両群を*X*<sub>1</sub>, ..., *X*<sub>*m*</sub>および*Y*<sub>1</sub>, ..., *Y*<sub>*n*</sub>（標本サイズはmおよびn）とする。両群から標本平均\(\overline{X}\)および\(\overline{Y}\)、ならびに不偏分散\(U_x\)および\(U_y\)を求める。 両群を合わせた分散の推定値\(U_e\)を

\[U_e=\frac{(m-1)U_x+(n-1)U_y}{m+n-2}\] により算出するか。

これから検定統計量*t<sub>0</sub>* を

\[t_0=\frac{|\overline{X}-\overline{Y}|}{\sqrt{U_e\left(\frac{1}{m}+\frac{1}{n}\right)}}\] により算出する。 両群の平均が等しい場合には「統計量*T* は[自由度](https://ja.wikipedia.org/wiki/自由度 "wikilink")*ν* = *m* + *n* – 2 の[t分布](https://ja.wikipedia.org/wiki/t分布 "wikilink")に従う」ので、これを帰無仮説として両側検定を行う。 このt分布における\(t_0\)の上側の*p*値を求め、有意水準*α*と比較する（あるいは[数表](../Page/数表.md "wikilink")で比較を行う）。*p* \< *α* ならば帰無仮説は棄却され、「両群の平均には有意差がある」といえる。

#### 異分散の場合（ウェルチのt検定）

前と同じ標本（ただし分散が等しくない）を対象とする。

検定統計量*t<sub>0</sub>* を

\[t_0=\frac{|\overline{X}-\overline{Y}|}{\sqrt{\frac{U_x}{m}+\frac{U_y}{n}}}\] により算出する。 t分布の自由度*ν*は、

\[\nu=\frac{(\frac{U_x}{m}+\frac{U_y}{n})^2}{\frac{U_x^2}{m^2(m-1)}+\frac{U_y^2}{n^2(n-1)}}\] であるが、これは[整数](../Page/整数.md "wikilink")になるとは限らないので、10未満の場合は[小数](../Page/小数.md "wikilink")自由度のt分布表を利用する。10以上ならば小数部を切り捨て整数部のみを使用してよい。

### 関連二組の差の平均値のt検定

*n* 対のデータがあるとし、対応する2変数を*X<sub>i</sub>* と*Y<sub>i</sub>* 、両者の差を*d<sub>i</sub>* = *X<sub>i</sub>* - *Y<sub>i</sub>* とする（*i* = 1, 2, ... , *n*）。*d<sub>i</sub>* の平均を\(\overline{X}_D\)とする。差の母集団の平均値*μ*<sub>d</sub>が特定の値である *μ*<sub>0</sub>と等しいかどうかの帰無仮説を検定する際に使用する。

検定統計量 *t<sub>0</sub>* を

\[t = \frac{\overline{X}_D - \mu_0}{s_D/\sqrt{n}}.\] により算出する。 t分布の自由度は*ν* = *n* -1となる。

## t検定の代替手段

t検定は、母集団が正規分布をしており標本の分散がχ<sup>2</sup> 分布をしているという前提の下において、「完全に」正確な確率を計算することができる（ウェルチ検定では「ほぼ」正確な値を計算できる）。逆の言い方をすると、母集団が正規分布に従っていない場合は、標本平均はt値からは多かれ少なかれ乖離する。実務的に標本から母集団が正規分布をしているかどうかという事を判断する事は、色々な検定方法があるとは言うものの、非常に困難である。ただし、[中心極限定理](../Page/中心極限定理.md "wikilink")によると、母集団の分布が正規分布に従わない標本でさえも、サンプル数が多くなればなるほど、標本平均は正規分布に近似していく。したがって、標本サイズが多ければ多いほど、標準検定値である\(\frac{\bar{X}}{\frac{\sigma}{\sqrt{n}}}\)はZ値に近似することになる。このような基礎に基づくと、母集団が正規分布から完全に逸脱した分布に従っていて、標本サイズが十分に大きな場合（大学の初等の統計の教科書などではn＞30などと載っている場合があるが、勿論多ければ多いほど良い）、Z検定で近似的な確率を計算できる。ただしt値は自由度が上がるとZ値に近似するため、計算上はt検定を用いても殆ど大差ない結果を得られる（哲学的には異なるが）。それがt検定が頑強（robust）であると言われる所以である。

### ノンパラメトリック手法

t検定は母集団の正規分布を前提とするパラメトリック検定であるが、この条件が満たされず、さらに標本サイズが小さいと、t検定で近似することも困難となる。そういった場合には[ノンパラメトリック検定](https://ja.wikipedia.org/wiki/ノンパラメトリック検定 "wikilink")を用いる方法がある。ノンパラメトリック検定は汎用性を重視し、効率性を犠牲にしているというものの、場合によっては統計のパワー（1 − β）がt検定に比べて高い。ただし、例えば[正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")の場合、最善はパラメトリック検定のt検定であるが、ノンパラメトリック検定の[ウィルコクソンの符号順位検定](../Page/ウィルコクソンの符号順位検定.md "wikilink")を用いても、必要なデータ数は \(\pi / 3\) = 約1.05 倍であり、5%程度多めに標本が必要なだけである\[2\]。

  - 標本が独立ならば[マン・ホイットニーのU検定](../Page/マン・ホイットニーのU検定.md "wikilink")など
  - 対になる標本ならば[ウィルコクソンの符号順位検定](../Page/ウィルコクソンの符号順位検定.md "wikilink")など

を用いることができる。ただしt検定やZ検定が母集団の平均値に注目して仮説を立てるのに対して、ノンパラメトリック検定ではランキング、中央値や分布などに注目して仮説を立てることに注意が必要。

t検定が[マン・ホイットニーのU検定](../Page/マン・ホイットニーのU検定.md "wikilink")および[ウィルコクソンの符号順位検定](../Page/ウィルコクソンの符号順位検定.md "wikilink")と比較して必要な標本数の比率\[3\]。1未満はt検定の方が必要標本数が小さいことを意味する。

  - 正規分布 - 0.9549
  - 一様分布 - 1
  - 両側指数分布 - 1.5
  - ロジスティク分布 - 1.0966
  - 指数分布 - 3
  - 対数正規分布 - 7.3537
  - ガンベル分布 - 1.2337
  - 三角分布 - 0.8889
  - この比率が最小となる分布 - 0.864

## 脚注

## 参考文献

  -
  -
  -
  - [JIS Z 8101](https://ja.wikipedia.org/wiki/JIS_Z_8101 "wikilink")-1:1999 [統計](../Page/統計.md "wikilink") − [用語](../Page/用語.md "wikilink")と[記号](../Page/記号.md "wikilink") − 第1部:[確率](https://ja.wikipedia.org/wiki/確率 "wikilink")及び一般統計用語, [日本規格協会](../Page/日本規格協会.md "wikilink"), <http://kikakurui.com/z8/Z8101-1-1999-01.html>

## 関連項目

  - [確率](https://ja.wikipedia.org/wiki/確率 "wikilink")
      - [確率論](../Page/確率論.md "wikilink")
  - [統計学](../Page/統計学.md "wikilink")

[Category:統計検定](https://ja.wikipedia.org/wiki/Category:統計検定 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.  [JIS Z 8101](https://ja.wikipedia.org/wiki/JIS_Z_8101 "wikilink")-1 : 1999 [統計](../Page/統計.md "wikilink") − [用語](../Page/用語.md "wikilink")と[記号](../Page/記号.md "wikilink") − 第1部:[確率](https://ja.wikipedia.org/wiki/確率 "wikilink")及び一般統計用語 2.61 t検定, [日本規格協会](../Page/日本規格協会.md "wikilink"), <http://kikakurui.com/z8/Z8101-1-1999-01.html>
2.
3.