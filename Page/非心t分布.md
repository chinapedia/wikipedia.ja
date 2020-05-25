> この記事は[非心t分布](https://ja.wikipedia.org/wiki/非心t分布)から翻訳されています。


**非心*t*分布**（ひしんティーぶんぷ、）とは、[確率分布](../Page/確率分布.md "wikilink")と[統計学](../Page/統計学.md "wikilink")におけるスチューデントの[t分布](https://ja.wikipedia.org/wiki/t分布 "wikilink")を一般化したものである。

非心な統計[母数](../Page/母数.md "wikilink")、例えば「 の上位10パーセント値」のようなものの[信頼区間](https://ja.wikipedia.org/wiki/信頼区間 "wikilink")を標本データだけに基いて計算するのに有用である。

## 非心t分布の特徴

*Z* は[分散](../Page/分散_\(確率論\).md "wikilink") 、[平均](../Page/平均.md "wikilink") 0 の[正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink") に従う[確率変数](../Page/確率変数.md "wikilink") 、*V* は自由度 νの[カイ二乗分布](../Page/カイ二乗分布.md "wikilink")に従いかつ、*Z* と独立な確率変数、μは実定数としたときに、

\[T=\frac{Z+\mu}{\sqrt{V/\nu}}\]

が従う分布のことを、「自由度ν、非心パラメーターμの非心t分布」と呼ぶ。μ=0の場合は[t分布](https://ja.wikipedia.org/wiki/t分布 "wikilink")そのものである。 この非心t分布においては（[非心F分布](https://ja.wikipedia.org/wiki/非心F分布 "wikilink")等の他の多くの非心分布とは異なり）非心パラメータμは負の値であってもよい。

### 累積分布関数

この非心t分布の[累積分布関数](../Page/累積分布関数.md "wikilink")は、以下の式で与えられる。\[1\]

\[F_{\nu,\mu}(x)=\begin{cases}
\tilde{F}_{\nu,\mu}(x), & \mbox{if } x\ge 0; \\
1-\tilde{F}_{\nu, -\mu}(x), &\mbox{if } x < 0,
\end{cases}\]

ここで、

\[\tilde{F}_{\nu,\mu}(x)=\Phi(-\mu)+\frac{1}{2}\sum_{j=0}^\infty\left[p_jI_y\left(j+\frac{1}{2},\frac{\nu}{2}\right)+q_jI_y\left(j+1,\frac{\nu}{2}\right)\right],\]

\[I_y\,\!(a,b)\] は、正則化された[不完全ベータ関数](../Page/不完全ベータ関数.md "wikilink"),

\[y=\frac{x^2}{x^2+\nu},\]

\[p_j=\frac{1}{j!}\exp\left\{-\frac{\mu^2}{2}\right\}\left(\frac{\mu^2}{2}\right)^j,\]

\[q_j=\frac{\mu}{\sqrt{2}\Gamma(j+3/2)}\exp\left\{-\frac{\mu^2}{2}\right\}\left(\frac{\mu^2}{2}\right)^j,\] であり、 Φ は、標準正規分布の[累積分布関数](../Page/累積分布関数.md "wikilink")である。

他の表現として、以下の書き方もできる。

\[F_{v,\mu}(x)=\begin{cases}
\frac{1}{2}\sum_{j=0}^\infty\frac{1}{j!}(-\mu\sqrt{2})^je^{\frac{-\mu^2}{2}}\frac{\Gamma(\frac{j+1}{2})}{\sqrt{\pi}}I\left (\frac{v}{v+x^2};\frac{v}{2},\frac{j+1}{2}\right ), & x\ge 0 \\
1-\frac{1}{2}\sum_{j=0}^\infty\frac{1}{j!}(-\mu\sqrt{2})^je^{\frac{-\mu^2}{2}}\frac{\Gamma(\frac{j+1}{2})}{\sqrt{\pi}}I\left (\frac{v}{v+x^2};\frac{v}{2},\frac{j+1}{2}\right ), & x < 0
\end{cases}\] ここで、 Γ は [ガンマ関数](../Page/ガンマ関数.md "wikilink") 、 *I* は、正則化された[不完全ベータ関数](../Page/不完全ベータ関数.md "wikilink")である。

### 確率密度関数

この非心t分布の[確率密度関数](../Page/確率密度関数.md "wikilink")は\[2\]

\[f(t)=\frac{\nu^{\nu/2} e^{-\nu \mu^2 /2(t^2 +\nu )}}{\sqrt{\pi} \Gamma (\nu /2)2^{(\nu -1)/2}(t^2 +\nu )^{(\nu +1)/2}}\]

\[\times \int_0^\infty x^\nu \exp \left[ -\frac{1}{2} \left( x-\frac{\mu t}{\sqrt{t^2 +\nu}} \right)^2 \right] \, dx\] ここで  である。この確率密度関数の定義域は[実数](../Page/実数.md "wikilink")である。

非心t分布の平均および分散は\[3\]

\[\operatorname{E} \left[ T\right] =\begin{cases}
\mu \sqrt{\frac{\nu}{2}} \frac{\Gamma ((\nu -1)/2)}{\Gamma (\nu /2)} &\nu >1 \\
\mbox{Does not exist} &\nu \le 1
\end{cases}\]

\[\operatorname{Var} \left[ T\right] =\begin{cases}
\frac{\nu(1+\mu^2)}{\nu -2} -\frac{\mu^2 \nu}{2} \left( \frac{\Gamma ((\nu -1)/2)}{\Gamma (\nu /2)} \right)^2 &\nu >2 \\
\mbox{Does not exist} &\nu \le 2
\end{cases}.\]

## 特別の場合

もしも  0}} の場合、非心t分布は[t分布](https://ja.wikipedia.org/wiki/t分布 "wikilink")になる。

## 関連する分布

  - もしも  が非心t分布にしたがう場合、 *T*}} とおくと  は[非心F分布](https://ja.wikipedia.org/wiki/非心F分布 "wikilink")にしたがう。

  - が非心t分布にしたがう場合、\(Z=\lim_{\nu\to\infty} T\) とおくと、 は[正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")にしたがう。

## 関連事項

  - [カイ二乗分布](../Page/カイ二乗分布.md "wikilink")
  - [非心F分布](https://ja.wikipedia.org/wiki/非心F分布 "wikilink")
  - [正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")
  - [t分布](https://ja.wikipedia.org/wiki/t分布 "wikilink")

## 脚注

## 外部リンク

  - [Eric W. Weisstein. "Noncentral Student's t-Distribution."](http://mathworld.wolfram.com/NoncentralStudentst-Distribution.html) From MathWorld--A Wolfram Web Resource

## 翻訳元

本記事は英語版ウィキペディア記事

  - Noncentral chi-square_distribution. [\[:en](https://ja.wikipedia.org/wiki/:en:Noncentral_t-distribution "wikilink")\] *Wikipedia: Free Encyclopedia* (English language), 14:14, 21 July 2007

からの抄訳に基づいて作成された。

[Category:確率分布](https://ja.wikipedia.org/wiki/Category:確率分布 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.
2.  L. Scharf, Statistical Signal Processing, (Massachusetts: Addison-Wesley, 1991), p.177.
3.  <http://www.mathworks.com/access/helpdesk_r13/help/toolbox/stats/nctstat.html>