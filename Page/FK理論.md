> この記事は[FK](https://ja.wikipedia.org/wiki/FK)から翻訳されています。


**FK理論**（エフケーりろん、「FK」はFrank-Kamenetskiiの略）とは[1939年](../Page/1939年.md "wikilink")に Frank Kamenetskii（[:en:David A. Frank-Kamenetskii](https://ja.wikipedia.org/wiki/:en:David_A._Frank-Kamenetskii "wikilink")）が考案した[物質](../Page/物質.md "wikilink")の[発火](https://ja.wikipedia.org/wiki/発火 "wikilink")に関する[理論](../Page/理論.md "wikilink")である。

物質が[自然発火](https://ja.wikipedia.org/wiki/自然発火 "wikilink")を起こす[条件](https://ja.wikipedia.org/wiki/条件 "wikilink")を[計算](../Page/計算.md "wikilink")する Frank-Kamenetskii の発火理論、あるいは、[粉塵爆発](https://ja.wikipedia.org/wiki/粉塵爆発 "wikilink")の発生条件を計算する熱爆発理論として用いられている。

[化学合成](https://ja.wikipedia.org/wiki/化学合成 "wikilink")の安全においては[反応](https://ja.wikipedia.org/wiki/反応 "wikilink")過程で発火、熱爆発、暴走反応などが起こらないよう[計算](../Page/計算.md "wikilink")するために用いられる理論であり、[化学実験](https://ja.wikipedia.org/wiki/化学実験 "wikilink")の[安全管理のためには重要な概念である](https://ja.wikipedia.org/wiki/安全管理者 "wikilink")。

[工業](../Page/工業.md "wikilink")[設備](../Page/設備.md "wikilink")などで発火[事故](../Page/事故.md "wikilink")が起こる[リスク](../Page/リスク.md "wikilink")を計算したり、粉塵爆発が起こる[危険](../Page/危険.md "wikilink")性を評価するために用いられる。

## 問題の説明\[1\]\[2\]\[3\]\[4\]\[5\]

一定の温度が維持されている空間\(T_o\)を仮定した場合, 均質な反応混合物を含有する。 容器の特徴的な大きさを\(a\)とする。 混合物は均質であるので、密度\(\rho\) は一定である。 発火初期の間、反応物の濃度は無視できる（下記の\(\text{fuel} + \text{oxidizer} \rightarrow \text{products} + q\)を参照）、したがって爆発は[アレニウスの式](../Page/アレニウスの式.md "wikilink")のみによって支配される。

\[\rho c_v \frac{\partial T}{\partial t} = \lambda \nabla^2 T + q \rho B Y_{Fo} e^{-E/(RT)}\]

  - \(T\)混合物の温度
  - \(c_v\) 一定の[熱容量](https://ja.wikipedia.org/wiki/熱容量 "wikilink")
  - \(\lambda\) [熱伝導率](../Page/熱伝導率.md "wikilink")
  - \(B\) 時間の経過と共に1の次元を有する[頻度因子](https://ja.wikipedia.org/wiki/頻度因子 "wikilink")
  - \(Y_{Fo}\) 初期燃料の[質量分率](https://ja.wikipedia.org/wiki/質量分率 "wikilink")
  - \(E\) [活性化エネルギー](https://ja.wikipedia.org/wiki/活性化エネルギー "wikilink")
  - \(R\) [気体定数](../Page/気体定数.md "wikilink")

### 無次元化

無次元活性化エネルギー\(\beta\)と放熱パラメータ\(\gamma\)は次のように示される。

\[\beta=\frac{E}{RT_o}, \quad \gamma = \frac{q Y_{Fo}}{c_v T_o}\]

容器を伝わる特徴的な熱伝導時間は\(t_c = \rho c_va^2/ \lambda\)で表され、特徴的な燃焼時間は \(t_f= \left(B e^{-\beta}\right)^{-1}\)で表され、特徴的な爆発/着火時間は\(t_e = \left(\beta\gamma B e^{-\beta}\right)^{-1}\)で表される。 典型的な燃焼プロセスにおいて\(\gamma\sim 6{-}8,\ \beta\sim 30{-}100\)は\(\beta\gamma\gg 1\)、したがって \(t_f = \beta\gamma t_e \gg 1\), i.e.であることに注意すべきであり、本質的に無視できる程度であり、燃料濃度が初期燃料濃度と同じであると仮定される理由である\(Y_{Fo}\)無次元のスケールは以下の式で表される。

\[\tau = \frac{t}{t_e}, \quad \theta = \frac{\beta(T-T_o)}{T_o}, \quad \eta^j = \frac{r^j} a, \quad \delta = \frac{t_c}{t_e}\]

ここで\(\delta\)は[ダムケラー数](https://ja.wikipedia.org/wiki/ダムケラー数 "wikilink")\(r\)と平面スラブの中心\(j=0\)を原点とする空間座標を表す, 球形の容器では\(j=1\)となり 円筒形の容器では\(j=2\)となる。このスケールで方程式は次のようになる。

\[\frac{\partial\theta}{\partial \tau} = \frac 1 {\delta}\frac 1 {\eta^j} \frac{\partial}{\partial \eta} \left(\eta^j \frac{\partial \theta}{\partial \eta}\right) + e^{\theta/(1+\theta/\beta)}\]

Since \(\beta\gg 1\),指数項を線形化すると\(e^{\theta/(1+\theta/\beta)}\approx e^\theta\)となる。

\[\frac{\partial\theta}{\partial \tau} = \frac 1 \delta \frac 1 {\eta^j} \frac \partial {\partial \eta} \left(\eta^j \frac{\partial \theta}{\partial \eta}\right) + e^\theta\]

## リファレンス

<references />

[Category:火](https://ja.wikipedia.org/wiki/Category:火 "wikilink") [Category:爆発](https://ja.wikipedia.org/wiki/Category:爆発 "wikilink") [Category:理論](https://ja.wikipedia.org/wiki/Category:理論 "wikilink")

1.  Frank-Kamenetskii, David Albertovich. Diffusion and heat exchange in chemical kinetics. Princeton University Press, 2015.
2.  Linan, Amable, and Forman Arthur Williams. "Fundamental aspects of combustion." (1993).
3.  Williams, Forman A. "Combustion theory." (1985).
4.  Buckmaster, John David, and Geoffrey Stuart Stephen Ludford. Theory of laminar flames. Cambridge University Press, 1982.
5.  Buckmaster, John D., ed. The mathematics of combustion. Society for Industrial and Applied Mathematics, 1985.