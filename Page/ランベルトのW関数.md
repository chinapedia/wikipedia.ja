> この記事は[W](https://ja.wikipedia.org/wiki/W)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/file:Lambert-w.svg "wikilink") [数学](../Page/数学.md "wikilink")における**ランベルト W 函数**（ランベルトWかんすう、）あるいは**オメガ函数** (*ω function*), 対数積（*product logarithm*; 乗積対数）は、函数  の[逆関係](https://ja.wikipedia.org/wiki/逆関係 "wikilink")の[分枝として得られる](https://ja.wikipedia.org/wiki/分岐点 "wikilink")[函数](https://ja.wikipedia.org/wiki/函数 "wikilink")  の総称である。ここに  は[指数函数](https://ja.wikipedia.org/wiki/指数函数 "wikilink")で  は任意の[複素数](../Page/複素数.md "wikilink")とする。すなわち  は  を満たす。

上記の方程式で '' = *ze*}} と置きかえれば、任意の複素数 }} に対する  函数（一般には  関係）の定義方程式

  -
    \(z' = W(z')e^{W(z')}\)

を得る。

函数  は[単射](../Page/単射.md "wikilink")ではないから、[関係](../Page/二項関係.md "wikilink")  は（ を除いて）[多価である](https://ja.wikipedia.org/wiki/多価函数 "wikilink")。仮に実数値の  に注意を制限するとすれば、複素変数  は実変数  に取り換えられ、関係の定義域は区間  に限られ、また開区間  上で二価の函数になる。さらに制約条件として  を追加すれば一価函数  が定義されて、 および  を得る。それと同時に、下側の枝は  であって、 と書かれる。これは  から  まで単調減少する。

ランベルト  関係は[初等函数](https://ja.wikipedia.org/wiki/初等函数 "wikilink")では表すことができない\[1\]。ランベルト  は[組合せ論](https://ja.wikipedia.org/wiki/組合せ論 "wikilink")において有用で、例えば[木の数え上げに用いられる](../Page/木_\(数学\).md "wikilink")。指数函数を含む様々な方程式（例えば[プランク分布](https://ja.wikipedia.org/wiki/プランクの法則 "wikilink")、[ボーズ–アインシュタイン分布](https://ja.wikipedia.org/wiki/ボース分布関数 "wikilink")、[フェルミ–ディラック分布などの最大値](../Page/フェルミ分布関数.md "wikilink")）を解くのに用いられ、また のような の解としても生じる。[生化学](../Page/生化学.md "wikilink")において、また特に[酵素動力学において](../Page/酵素反応速度論.md "wikilink")、[ミカエリス–メンテン動力学の経時動力学解析に対する閉じた形の解はランベルト](https://ja.wikipedia.org/wiki/ミカエリス・メンテン式 "wikilink")  函数によって記述される。

[thumbは](https://ja.wikipedia.org/wiki/file:Product_Log.jpg "wikilink")  を端点に持つ。この図では、点  における色相を  の[偏角で](https://ja.wikipedia.org/wiki/偏角_\(複素解析\) "wikilink")、輝度を  の[絶対値](https://ja.wikipedia.org/wiki/絶対値 "wikilink")で決定している。\]\]

## 用語について

[Diagram_of_the_real_branches_of_the_Lambert_W_function.png](https://ja.wikipedia.org/wiki/File:Diagram_of_the_real_branches_of_the_Lambert_W_function.png "fig:Diagram_of_the_real_branches_of_the_Lambert_W_function.png") ランベルト -函数は[ヨハン・ハインリヒ・ランベルト](https://ja.wikipedia.org/wiki/ヨハン・ハインリヒ・ランベルト "wikilink")に因んで名づけられた。[Digital Library of Mathematical Functions](https://ja.wikipedia.org/wiki/Digital_Library_of_Mathematical_Functions "wikilink") では主枝  を , 分枝  は  と書いている。ここでの表記の規約（つまり ）はランベルト  に関する標準的な参考文献\[2\]に従った。

## 歴史

ランベルトは初め「ランベルトの超越方程式」に関連して1758年に考察した\[3\]。これは[レオンハルト・オイラー](../Page/レオンハルト・オイラー.md "wikilink")の1783年の  の特別な場合を論じた論文\[4\]に繋がる。

ランベルト -函数は、特殊化された応用において、十年程度毎に「再発見」されてきた。1993年には、等電荷に対する量子力学的（物理学における基本問題）の厳密解をランベルト -函数が与えることが報告されたとき、コーレスら計算機代数システム[Maple](https://ja.wikipedia.org/wiki/Maple "wikilink")の開発者たちはライブラリを精査して、この函数が自然界に遍く存在することを発見した\[5\]\[6\]。

## 微分積分学

### 導函数

[陰函数微分法](https://ja.wikipedia.org/wiki/陰函数微分法 "wikilink")により、 の任意の枝が[常微分方程式](../Page/常微分方程式.md "wikilink")

\[z(1+W)\frac{dW}{dz}=W\quad(z\neq -1/e)\] を満たすことが示せる（ では  は微分できない）。従って、 の導函数は

  -
    \(\frac{dW}{dz}=\frac{W(z)}{z(1 + W(z))}\quad(z\notin\{0,-1/e\})\)

を満たす。ここで恒等式  を用いるならば、

  -
    \(\frac{dW}{dz}=\frac{1}{z+e^{W(z)}}\quad(z\ne -1/e)\)

と書きなおすこともできる。

### 原始函数

函数 （およびそれを含む多くの式）は、 と置いた[置換積分](https://ja.wikipedia.org/wiki/置換積分 "wikilink")によって

  -
    <math> \\begin{align}

\\int W(x)\\mathit{dx} &= x W(x)-x+e^{W(x)}+C\\\\ & = x \\left( W(x) - 1 + \\frac{1}{W(x)} \\right) + C. \\\\ \\end{align}</math>

と積分できる。

したがって、（ であることも考慮して）等式

  -
    \(\int_{0}^{e} W(x)\,\mathit{dx} = e-1\)

が得られる。

## 漸近展開

の  を中心とする[テイラー級数](https://ja.wikipedia.org/wiki/テイラー級数 "wikilink")は、

  -
    <math>

W_0 (x) = \\sum_{n=1}^\\infty \\frac{(-n)^{n-1}}{n\!}\\ x^n = x - x^2 + \\frac{3}{2}x^3 - \\frac{8}{3}x^4 + \\frac{125}{24}x^5 - \\cdots </math>

[ダランベールの収束判定法](https://ja.wikipedia.org/wiki/ダランベールの収束判定法 "wikilink")によると、[収束半径](https://ja.wikipedia.org/wiki/収束半径 "wikilink")は  である。この級数の定める函数は、[区間](../Page/区間_\(数学\).md "wikilink") }}に沿ってを入れれば、ガウス平面の全域で定義される[正則函数](https://ja.wikipedia.org/wiki/正則函数 "wikilink")に延長することができる。この正則函数をランベルト  函数の[主値](https://ja.wikipedia.org/wiki/主値 "wikilink")と定める。

が十分大きければ、 は漸近的に

  -
    <math>\\begin{align} W_0(x)

`&= L_1 - L_2 + \frac{L_2}{L_1} + \frac{L_2(-2+L_2)}{2L_1^2}\\`
`&\qquad\qquad +\frac{L_2(6-9L_2+2L_2^2)}{6L_1^3}+\frac{L_2(-12+36L_2-22L_2^2+3L_2^3)}{12L_1^4}+\cdots\\[8pt]`
`& =L_1-L_2+\sum_{\ell=0}^{\infty}\sum_{m=1}^{\infty}\frac{(-1)^{\ell}\left[{ \ell+m \atop \ell + 1 }\right]}{m!} L_1^{-\ell-m} L_2^{m}\\`
`& =\ln(x)-\ln(\ln(x))+o(1)`

\\end{align}</math> と展開される。ただし、 であり、\[\] は非負の第一種[スターリング数](https://ja.wikipedia.org/wiki/スターリング数 "wikilink")である\[7\]。

もう一つの、区間 }} 上で定義される実函数な枝  は、 と書けば、 が十分  に近いとき同じ形の漸近展開を持つ。

なるとき、

  -
    \(\ln(x)-\ln\bigl(\ln(x)\bigr)+\frac{\ln\bigl(\ln(x)\bigr)}{2\ln(x)}\le W_0(x)\le\ln(x)-\ln\bigl(\ln(x)\bigr)+\frac{e}{e-1}\frac{\ln\bigl(\ln(x)\bigr)}{\ln(x)}\)

という上下の評価が成り立つ\[8\]。また もう一つの枝  の評価は  に対して

  -
    \(-1-\sqrt{2u}-u < W_{-1}(-e^{-u-1}) < -1-\sqrt{2u}-\frac{2}{3}u\)

となる\[9\]。

### 整数冪・複素数冪の展開

の整数乗もまた  において単純なテイラー級数（あるいは[ローラン級数](https://ja.wikipedia.org/wiki/ローラン級数 "wikilink")）展開を持つ。例えば

  -
    \(W_0(x)^2 = \sum_{n=2}^\infty \frac{-2(-n)^{n-3}}{(n-2)!}\ x^n = x^2-2x^3+4x^4-\frac{25}{3}x^5+18x^6- \cdots.\)

より一般に、ラグランジュの反転公式を用いれば、 に対して

  -
    \(W_0(x)^r = \sum_{n=r}^\infty \frac{-r(-n)^{n-r-1}}{(n-r)!}\ x^n\)

となることが示せる（これは一般に、位数  のローラン級数になっている）。あるいは同じことだが、この式を  の冪に関するテイラー級数として

  -
    \(\left(\frac{W_0(x)}{x}\right)^r =\exp(-r W_0(x)) = \sum_{n=0}^\infty \frac{r(n+r)^{n-1}}{n!}(-x)^n\)

と書くことができる。これは任意の  と  に対して成立する。

## 特殊値

任意の非零[代数的数](../Page/代数的数.md "wikilink")  に対して  は[超越数](../Page/超越数.md "wikilink")になる。実際、 が零ならば  も零でなければならず、また  が非零代数的数ならば[リンデマン–ワイエルシュトラスの定理により](https://ja.wikipedia.org/wiki/リンデマンの定理 "wikilink")  は超越的でなければならず、従って もまた超越的でなければならない。

\[W(-\pi/2) = i\pi/2\]

\[W({\ln 4})= \ln 2\]

\[W(-(\ln a)/a)= -\ln a \quad(1/e\le a\le e)\]

\[W(-1/e) = -1\]

\[W(0) = 0\]

\[W(1) = \Omega=\frac{1}{\displaystyle \int_{-\infty}^{+\infty}\frac{dt}{(e^t-t)^2+\pi^2}}-1\approx 0.56714329\dots\] ([オメガ定数](https://ja.wikipedia.org/wiki/オメガ定数 "wikilink"))

\[W(1) = e^{-W(1)} = -\ln W(1)\]

\[W(e) = 1\]

\[-W(-1) = e^{-W(-1)} = \ln( -{W(-1)}) \approx 0.31813+1.33723\,i\]

\[W'(0) = 1\]

## 等式

いくつかの等式は定義から直ちに得られる:

\[\begin{align}
W(xe^{x}) &= x & (x \geq 0,\, x=-1) \\
W_0(xe^{x}) &= x & (x \geq -1) \\
W_{-1}(xe^{x}) &= x & (x \leq -1)
\end{align}\]

ここで、 は単射でないから、 は常には成り立たないことに注意すべきである。 かつ  なる  を固定して、方程式  は  に関して二つの解を持ち、その一方はもちろん  である。もう一方の解は、 の場合  に、 の場合  にある。これらを踏まえて、次の式を導くことができる。

\[W_0(xe^{x}) = y \quad(x < -1).\]

\[W_{-1}(xe^{x}) = y \quad(x > -1).\]

\[W(x) e^{W(x)} = x.\]

\[e^{W(x)} = x/W(x).\]

\[W(x) = \ln x - \ln W(x) \quad (x \ge -1/e).\]

\[\ln W(x) = \ln x - W(x)\quad(x>0).\]\[10\]

\[W(nx^n / W(x)^{n-1})= n W(x)\quad(n>0, x>0).\]（これは正しく枝を選べば他の  に対しても拡張できる）

を反転すれば

\[W(x \ln x) = \ln x = W(x) + \ln W(x) \quad (x > 0)\]

を得る。

オイラーの反復指数函数  を用いれば

  -
    \(h(x) = e^{-W(-\ln(x))} = \frac{W(-\ln(x))}{-\ln(x)}\quad(x\ne 1)\)

を得る。

を含む有用な積分公式がいくつか存在し、例えば以下のようなものが挙げられる: \\,dx = 2\\sqrt{2\\pi}.</math> \\,dx &=\\int_{0}^{\\infty} \\frac{u}{ue^{u}\\sqrt{ue^{u}}}(u+1)e^{u}\\,du \\\\\[5pt\] &=\\int_{0}^{\\infty} \\frac{u+1}{\\sqrt{ue^{u}}}\\,du \\\\\[5pt\] &=\\int_{0}^{\\infty} \\frac{u+1}{\\sqrt{u}}\\frac{1}{\\sqrt{e^{u}}}\\,du\\\\\[5pt\] &=\\int_{0}^{\\infty} u^{\\frac{1}{2}}e^{-\\frac{u}{2}}\\,du+\\int_{0}^{\\infty} u^{-\\frac{1}{2}}e^{-\\frac{u}{2}}\\,du\\\\ &=2\\int_{0}^{\\infty} (2w)^{\\frac{1}{2}}e^{-w}\\,dw+2\\int_{0}^{\\infty} (2w)^{-\\frac{1}{2}}e^{-w}\\,dw && \\quad (u =2w) \\\\ &=2\\sqrt{2}\\int_{0}^{\\infty} w^{\\frac{1}{2}}e^{-w}\\,dw+\\sqrt{2}\\int_{0}^{\\infty} w^{-\\frac{1}{2}}e^{-w}\\,dw \\\\ &=2\\sqrt{2} \\cdot \\Gamma(\\tfrac{3}{2})+\\sqrt{2} \\cdot \\Gamma(\\tfrac{1}{2}) \\\\ &=2\\sqrt{2} (\\tfrac{1}{2}\\sqrt{\\pi})+\\sqrt{2}(\\sqrt{\\pi}) \\\\ &=2\\sqrt{2\\pi} \\end{align}</math> }} |3= 三つ目の式

  -
    \(\int_{0}^{\infty} W(\tfrac{1}{x^2})\,dx = \sqrt{2\pi}\)

は、二つ目の式で  と置き換えることによって得られる。また一つ目の式はこの三つ目の式で  と置くことでも得られる。 }} 分岐切断 }} に沿う  を除けば（そのような  では以下の積分が確定しない）、ランベルト  函数の主枝は、以下の積分

  -
    \(W(z)=\frac{z}{2\pi}\int\limits_{-\pi}^{\pi}\frac{(1-\nu\cot\nu)^2+\nu^2}{z+\nu\csc\nu e^{-\nu\cot\nu}}d\nu=\frac{z}{\pi}\int\limits_0^{\pi}\frac{(1-\nu\cot\nu)^2+\nu^2}{z+\nu\csc\nu e^{-\nu\cot\nu}}d\nu\)

によって計算できる\[11\]。この二つの積分の値が等しいことは被積分函数の対称性による。

## 応用

指数関数を含む方程式の多くは、W関数を用いることで解くことができる。主な方針は、[未知数](https://ja.wikipedia.org/wiki/未知数 "wikilink")を含む項を方程式の左辺（あるいは右辺）に寄せ、W関数で解を表現できる \(xe^x\)の形にすることである。例えば、方程式 \(2^t = 5t\) を解くには、両辺に \(-\ln(2) ~ 2^{-t} / 5\)を掛け、\(-\ln(2)/5 = -t \ln(2) \exp(-t\ln 2)\)を得る。ここで、両辺のW関数をとれば、\(W(-\ln(2)/5) = -t \ln 2\)、即ち \(t = -W(-\ln(2)/5) / \ln 2 = 0.235\dots, 4.488\dots\)となる。

同様の方法で、*x*<sup>*x*</sup> = *z* の解は、  あるいは  となる。

複素数の無限回の累乗 } \\\!</math>}} が収束するとき、ランベルトのW関数を用いれば、その[極限値](https://ja.wikipedia.org/wiki/極限値 "wikilink")を次のように表現できる。  ただし、log(*z*) は[複素対数函数](https://ja.wikipedia.org/wiki/複素対数函数 "wikilink")の[主値](https://ja.wikipedia.org/wiki/主値 "wikilink")とする。

## 一般化

通常のランベルト  は  に関する  の形（ただし、 は実定数）の「超越代数」方程式の厳密解  を記述することができる。

ランベルト  函数の一般化\[12\]\[13\]\[14\]\[15\]として以下のようなものを挙げることができる:

  - 低次元における[一般相対論](https://ja.wikipedia.org/wiki/一般相対論 "wikilink")および[量子力学](https://ja.wikipedia.org/wiki/量子力学 "wikilink")（[量子重力](../Page/量子重力理論.md "wikilink")）（実は、両分野の繋がりは、以前には知られていなかった\[16\]）への応用では、式  の右辺を今度は  の二次多項式とした

<!-- end list -->

  -
    を考える。ここで、この二次多項式の根  は相異なる実定数とする。この方程式の解は一つの引数  を持つ函数だが、 や  のような項は解函数のパラメータとして働く。そのような側面で見れば、この一般化は[超幾何函数](https://ja.wikipedia.org/wiki/超幾何函数 "wikilink")やを作るのと似たような方式とも思えるが、これらの函数とは異なる「クラス」に属する。 のときは、式  の両辺は因数分解できて、 に帰着されるから、解函数も通常の  函数に還元される。式  は[ディラトン](https://ja.wikipedia.org/wiki/ディラトン "wikilink")場を支配する方程式を表すから、それにより不等静止質量の場合に対する -次元（空間一次元・時間一次元）における あるいは「直列」(*lineal*) 二体重力問題の計量や、一次元の不等電荷に対する量子力学的の固有エネルギーが導かれる。

<!-- end list -->

  - 量子力学的の特別の場合、具体的には（三次元）[水素分子イオン](https://ja.wikipedia.org/wiki/水素分子イオン "wikilink")\[17\]の固有エネルギーの解析解の場合、今度は式  の（あるいは式  の）右辺を  に関する無限次多項式の比とした

<!-- end list -->

  -
    を考える。各  は実定数、 は固有エネルギーと核間距離  の函数である。式  は、その特別の場合として式  および  も含めて、の成す大きなクラスに関係する。

"" 函数の基礎物理問題への応用は、 で表される通常の  函数の場合でさえも、近年のの分野に見られる\[18\]ように、尽くされてはいない。

## 複素平面上のグラフ

Image:LambertWRe.png| Re(*W*<sub>0</sub>(*x* + *iy*))}} Image:LambertWIm.png| Im(*W*<sub>0</sub>(*x* + *iy*))}} Image:LambertWAbs.png| }} Image:LambertWAll.png|Superimposition of the previous three plots

## 数値的評価

函数は[ニュートン法](../Page/ニュートン法.md "wikilink")を用いて近似することができて、（したがって ）に対する逐次近似は

  -
    \(w_{j+1}=w_j-\frac{w_j e^{w_j}-z}{e^{w_j}+w_j e^{w_j}}\)

として与えられる。また、 を用いた近似

  -
    <math>w_{j+1}=w_j-\\frac{w_j e^{w_j}-z}{e^{w_j}(w_j+1)-\\frac{(w_j+2)(w_je^{w_j}-z)}

{2w_j+2}}</math> を  は  の計算において与えている。

## ソフトウェア実装

函数の実装は:

  - [LambertW in Maple](http://www.maplesoft.com/support/help/Maple/view.aspx?path=LambertW),
  - `lambertw` in [GP](https://ja.wikipedia.org/wiki/PARI/GP "wikilink") (`glambertW` in PARI),
  - `lambertw` in MATLAB,\[19\]
  - `lambertw` in octave with the 'specfun' package,
  - `lambert_w` in Maxima,\[20\]
  - `ProductLog` (with a silent alias `LambertW`) in Mathematica,\[21\]
  - `lambertw` in Python scipy's special function package\[22\]
  - `gsl_sf_lambert_W0` and `gsl_sf_lambert_Wm1` functions in [special functions](http://www.gnu.org/software/gsl/manual/html_node/Lambert-W-Functions.html) section of the [GNU Scientific Library](http://www.gnu.org/software/gsl/) - GSL.

などがある。

## 関連項目

  -
  - ランベルトの[三項方程式](https://ja.wikipedia.org/wiki/三項方程式 "wikilink")

  -
  -
  -
  -
  -
## 注

## 参考文献

  -
  -
  - (Lambert function is used to solve delay-differential dynamics in human disease.)

  -
  -
  -
  - [Veberic, D., "Having Fun with Lambert W(x) Function" arXiv:1003.1628 (2010)](http://arxiv.org/abs/1003.1628);

  -
## 外部リンク

  - [National Institute of Science and Technology Digital Library - Lambert W](http://dlmf.nist.gov/4.13)

  -
  - [Computing the Lambert W function](https://web.archive.org/web/20060824060948/http://www.whim.org/nebula/math/lambertw.html)

  - [Corless et al. Notes about Lambert W research](http://www.apmaths.uwo.ca/~rcorless/frames/PAPERS/LambertW/)

  - GPL [C++ implementation](https://github.com/DarkoVeberic/LambertW) with Halley's and Fritsch's iteration.

  - [Special Functions](http://www.gnu.org/software/gsl/manual/html_node/Special-Functions.html) of the [GNU Scientific Library](http://www.gnu.org/software/gsl/) - GSL

[Category:特殊関数](https://ja.wikipedia.org/wiki/Category:特殊関数 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink") [Category:エポニム](https://ja.wikipedia.org/wiki/Category:エポニム "wikilink")

1.  .
2.
3.  Lambert JH, "Observationes variae in mathesin puram", *Acta Helveticae physico-mathematico-anatomico-botanico-medica*, Band III, 128–168, 1758 ([facsimile](http://www.kuttaka.org/~JHL/L1758c.pdf))
4.  Euler, L. "De serie Lambertina Plurimisque eius insignibus proprietatibus." *Acta Acad. Scient. Petropol. 2*, 29–51, 1783. Reprinted in Euler, L. *Opera Omnia, Series Prima, Vol. 6: Commentationes Algebraicae*. Leipzig, Germany: Teubner, pp. 350–369, 1921. ([facsimile](http://math.dartmouth.edu/~euler/docs/originals/E532.pdf))
5.
6.
7.  [Approximation of the Lambert W function and the hyperpower function](http://rgmia.org/papers/v10n2/lambert-v2.pdf), Hoorfar, Abdolhossein; Hassani, Mehdi.
8.  <http://www.emis.de/journals/JIPAM/images/107_07_JIPAM/107_07_www.pdf>
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19. [lambertw - MATLAB](http://www.mathworks.com.au/help/toolbox/symbolic/lambertw.html)
20. [Maxima, a Computer Algebra System](http://maxima.sourceforge.net)
21. [ProductLog at WolframAlpha](http://reference.wolfram.com/mathematica/ref/ProductLog.html)
22. [1](http://docs.scipy.org/doc/scipy-0.16.0/reference/generated/scipy.special.lambertw.html)