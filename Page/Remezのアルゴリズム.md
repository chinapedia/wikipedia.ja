> この記事は[Remez](https://ja.wikipedia.org/wiki/Remez)から翻訳されています。


**Remezのアルゴリズム**または**Remezの交換アルゴリズム**とはによって1934年に発表された、関数に簡単な近似関数を見つけるために使用される反復アルゴリズムであり、具体的には、関数を[チェビシェフ空間で](https://ja.wikipedia.org/wiki/:en:haar_space "wikilink")[一様ノルム](https://ja.wikipedia.org/wiki/一様ノルム "wikilink") *L*<sub>∞</sub>を最適化することで求める 。\[1\]

チェビシェフ空間の典型的な例は、 [区間](../Page/区間_\(数学\).md "wikilink") \(C=[a,b]\)上の実[連続関数](https://ja.wikipedia.org/wiki/連続写像 "wikilink")[空間における次数](https://ja.wikipedia.org/wiki/ベクトル空間 "wikilink")\(n\)の [チェビシェフ多項式](https://ja.wikipedia.org/wiki/チェビシェフ多項式 "wikilink")の部分空間であり、与えられた部分空間内の最良近似の多項式は、多項式と関数の間の最大[絶対差](https://ja.wikipedia.org/wiki/絶対差 "wikilink")を最小にするものと定義される。 この場合、解の形式はによって正確性が保証される。

## 手順

まず近似する関数*f*に対し、近似区間中の\(n + 2\)のサンプル点の集合\(X=\{x_1, x_2, ...,x_{n+2}\}\)を考える。\(X\)は通常、区間中に線形に射影されたチェビシェフ多項式の極値を用いる。

1.  未知数\(b_0, b_1...b_n\)および\(E\)*について*以下の線形連立方程式を解く
      -
        \(b_0 + b_1 x_i+ ... +b_n x_i ^ n + (-1)^ i E = f(x_i)\) （\(i=1, 2, ... n+2\) ）
2.  \(b_i\)を多項式\(P_n (x) =\sum b_i x^i\)を形成する係数とする。
3.  絶対誤差 \(|P_n (x) - f(x)|\)が極大となる点\(m\)の集合\(M\)を見つける。
4.  誤差がすべての\(m\)について大きさが等しく、符号が交互である場合、 \(P_n\)は、最大誤差最小の近似多項式となる。 そうでない場合は、 \(X\)を\(M\)に置き換え、上記の手順を繰り返す。
5.  上記の手順を繰り返す。

結果は、最良近似多項式またはと呼ばれる。

Remezアルゴリズムの実装における技術のレビューはW. Fraserによってなされた。 \[2\]

### 初期値の選択

多項式補間の理論における役割のため、近似の初期値としてチェビシェフノードが一般的に使用される。 [ラグランジュ補間](../Page/ラグランジュ補間.md "wikilink")\(L_n(f)\)を用いた関数\(f\)*の*最適化問題の初期化では、この近似の初期値が次の範囲にあることが示される。

\(\lVert f - L_n(f)\rVert_\infty \le (1 + \lVert L_n\rVert_\infty) \inf_{p \in P_n} \lVert f - p\rVert\)

ここで、ノード（\(t_1,\ldots,t_{n+1}\)）のラグランジュ補間演算子\(L_n\)のノルム（）は

\(\lVert L_n\rVert_\infty = \overline{\Lambda}_n(T) = \max_{-1 \le x \le 1} \lambda_n(T; x)\)

と表される。

\(T\)はチェビシェフ多項式の[零点であり](https://ja.wikipedia.org/wiki/関数の零点 "wikilink")、ルベーグ関数は

\(\lambda_n(T; x) = \sum_{j = 1}^{n + 1} \left| l_j(x) \right|, \quad l_j(x) = \prod_{\stackrel{i = 1}{i \ne j}}^{n + 1} \frac{(x - t_i)}{(t_j - t_i)}\)

となる。

Theodore A. Kilgore、 \[3\] Carl de Boor、およびAllan Pinkus \[4\]は、各*\(L_n\)*に一意の*\(t_i\)*が存在することを証明したが、（通常の）多項式については明示的に知られていない。 同様に、 \(\underline{\Lambda}_n(T) = \min_{-1 \le x \le 1} \lambda_n(T; x)\) 、およびノードの選択の最適性は\(\overline{\Lambda}_n - \underline{\Lambda}_n \ge 0\)のように表現できる。

準最適ではあるが分析的に明示的な選択肢を提供するチェビシェフノードの場合、漸近的挙動は以下の様になることが知られている\[5\]

\(\overline{\Lambda}_n(T) = \frac{2}{\pi} \log(n + 1) + \frac{2}{\pi}\left(\gamma + \log\frac{8}{\pi}\right) + \alpha_{n + 1}\)

（ は[オイラー・マスケローニ定数](../Page/オイラーの定数.md "wikilink") ）

ここで、

\(0 < \alpha_n < \frac{\pi}{72 n^2}\)for \(n \ge 1,\)

であり、および上限\[6\]

\(\overline{\Lambda}_n(T) \le \frac{2}{\pi} \log(n + 1) + 1\)

があたえられる。

Lev Brutman \[7\]は\(n \ge 3\) かつ\(\hat{T}\)が拡張されたチェビシェフ多項式の零点であるとき以下を示した。

\(\overline{\Lambda}_n(\hat{T}) - \underline{\Lambda}_n(\hat{T}) < \overline{\Lambda}_3 - \frac{1}{6} \cot \frac{\pi}{8} + \frac{\pi}{64} \frac{1}{\sin^2(3\pi/16)} - \frac{2}{\pi}(\gamma - \log\pi)\approx 0.201\)

また、Rüdiger Günttner \[8\]は、 \(n \ge 40\)について

\(\overline{\Lambda}_n(\hat{T}) - \underline{\Lambda}_n(\hat{T}) < 0.0196\)

を示した。

## 詳細な議論

この節では、上記の手順の詳細について説明する。\(i\) は\(0 \le i \le n+1\)である。

**ステップ1**

与えられた\(x_0, x_1, ... x_{n+1}\)に対して 、以下の線形連立方程式を未知数\(b_0, b_1...b_n\)および\(E\)について解く

\(b_0 + b_1 x_i+ ... +b_n x_i ^ n + (-1) ^ i E = f(x_i)\)

\((-1)^i E\)の項が存在しているためノード\(x_0, ...,x_{n+1}\) は整列（単調増加もしくは単調減少）している必要があることがわかる。 このとき、この線形方程式には一意の解が存在する。また、標準的なライブラリのソルバーで線形方程式を解く場合は\(O(n^3)\)の計算量となるが、この処理は\(O(n^2)\)の計算量で得られることがわかっている。

以下に簡単な証明を次に示す。

\(f(x)\)に対して*\(n\)*次補間関数\(p_1(x)\)を、\((-1)^i\)について*\(n\)*次補間関数\(p_2(x)\)を最初の*\(n+1\)*ノード（\(x_0, ...,x_{n}\)）について計算する。

\(p_1(x_i) = f(x_i), p_2(x_i) = (-1)^i, i = 0, ..., n.\)

この計算のため、各補間関数の計算において\(0, ...,n\)階の[差商](https://ja.wikipedia.org/wiki/差商 "wikilink")を使用した[ニュートン補間](../Page/ニュートン補間.md "wikilink")を用いるとそれぞれ\(O(n^2)\)の計算量となる。

多項式\(p_2(x)\)の\(x_{i-1}\)と\(x_i\)の間に\(i\)番目の零点がある（ \(i=1, \ldots,n\)）。したがって、\(x_n\)と\(x_{n+1}\)の間に零点はなく、\(p_2(x_n)\)と\(p_2(x_{n+1})\)は\((-1)^n\) と同符号である。

線形結合\(p(x) := p_1 (x) - p_2(x)\!\cdot\!E\)は、\(n\)次*の*多項式であり、

\(p(x_i) = p_1(x_i) - p_2(x_i)\!\cdot\! E \ = \ f(x_i) - (-1)^i E,\ \ \ \ i =0, \ldots, n.\)

と変形できる。

これは任意の*\(E\)*に対して、\(i = 0,\ldots,n\)において式\(b_0 + b_1 x_i+ ... +b_n x_i ^ n + (-1) ^ i E\)と同じである。\(i = n+1\)とのときは

\(p(x_{n+1}) \ = \ p_1(x_{n+1}) - p_2(x_{n+1})\!\cdot\!E \ = \ f(x_{n+1}) - (-1)^{n+1} E\)

となり、*\(E\)*について以下の式を得ることができる。

\(E \ := \ \frac{p_1(x_{n+1}) - f(x_{n+1})}{p_2(x_{n+1}) + (-1)^n}.\)

上述の通り、分母の2項は同じ符号を持つため、\(E\)*及び* \(p(x) \equiv b_0 + b_1x + \ldots + b_nx^n\)常に一意に定まる。

与えられた\(n+2\)の整列したノードでの誤差は、以下の通り正負の交互の順になる。

\(p(x_i) - f(x_i) \ = \ -(-1)^i E,\ \ i = 0, ..., n\!+\!1.\)

*de La Vallée Poussin*の定理によれば、この条件下では誤差が*\(E\)*より小さい*\(n\)*次の多項式は存在しない。もしそのような多項式\(\tilde p(x)\)が存在した場合、\(p(x)-\tilde p(x) = (p(x) - f(x)) - (\tilde p(x) - f(x))\)はノード\(x_i\)において正負交互のままであり\(n+1\)個の零点を有することになるが、次数\(n\)の多項式ではありえない。 したがって、この*\(E\)*は、次数*\(n\)の*多項式におけるで達成できる誤差の下限となる。

**ステップ2**

\(p(x)\)を\(b_0 + b_1x + ... + b_nx^n\)とする。

**ステップ3**

次のように入力ノード\(x_0, ..., x_{n+1}\)とそのエラー\(\pm E\)を更新する。

\(p(x) - f(x)\)について、零点によって区切られる正負の領域にそれぞれついて、正の領域で\(x_i\)を極大値\(\bar{x}_i\)に置き換え、負の領域では\(x_i\)極小値\(\bar{x}_i\)に置き換える。 （期待する\(\bar{x}_0\) *A*で\(\bar {x}_i\)近く\(x_i\) 、そして\(\bar{x}_{n+1}\) *Bで* 。）このステップでは高い精度は必要なく2つの*2次近似*を使用した[直線探索](https://ja.wikipedia.org/wiki/直線探索 "wikilink")で十分である。 （ \[9\]）

ここで\(z_i := p(\bar{x}_i) - f(\bar{x}_i)\) とする。 各\(z_i\)に対して絶対値\(|z_i|\)は*E*以上となる。 *de La Vallée Poussin*の定理とその証明は、 \(z_0, ... ,z_{n+1}\)についての\(\min\{|z_i|\} \geq E\)についても適用可能で、次数*\(n\)の*最良多項式近似の最大誤差の下限と考えることができる。

また、 \(\max\{|z_i|\}\)は最大誤差の上限となる。

**ステップ4**

\(\min\,\{|z_i|\}\)と\(\max\,\{|z_i|\}\)を最良多項式近似の最大誤差の下限と上限として、十分な精度、すなわち \(\max\{|z_i|\} - \min\{|z_i|\}\)十分に小さいか、減少しなくなったら繰り返しを終了する。 これらの上下限は反復処理の収束状況を示していると考えられる。

## 派生

以下のような派生が有る。

  - 複数のサンプル点を、同時に最大絶対差の近くの場所に置き換える。
  - すべてのサンプル点を、すべての位置、交互の符号、最大差となるよう単一の反復で置き換える。 \[10\]
  - [浮動小数点演算を使用するコンピューターで関数を計算するために近似を使用する場合は](../Page/浮動小数点数.md "wikilink")、 [相対誤差を使用して近似と関数の差を定義することがある](https://ja.wikipedia.org/wiki/近似による誤差 "wikilink")。
  - 修正されたRemez交換アルゴリズムには、無誤差点制約が含まれることがある。 \[11\]

## 関連項目

  - [近似法](https://ja.wikipedia.org/wiki/近似法 "wikilink")

## 参考文献

[Category:数値解析](https://ja.wikipedia.org/wiki/Category:数値解析 "wikilink") [Category:多項式](https://ja.wikipedia.org/wiki/Category:多項式 "wikilink") [Category:近似理論](https://ja.wikipedia.org/wiki/Category:近似理論 "wikilink") [Category:未査読の翻訳があるページ](https://ja.wikipedia.org/wiki/Category:未査読の翻訳があるページ "wikilink")

1.  E. Ya. Remez, "Sur la détermination des polynômes d'approximation de degré donnée", Comm. Soc. Math. Kharkov **10**, 41 (1934);
    "Sur un procédé convergent d'approximations successives pour déterminer les polynômes d'approximation, Compt. Rend. Acad. Sc. **198**, 2063 (1934);
    "Sur le calcul effectiv des polynômes d'approximation des Tschebyscheff", Compt. Rend. Acade. Sc. **199**, 337 (1934).
2.
3.
4.
5.
6.  T. Rivlin, "The Lebesgue constants for polynomial interpolation", in *Proceedings of the Int. Conf. on Functional Analysis and Its Application*, edited by H. G. Garnier *et al.* (Springer-Verlag, Berlin, 1974), p. 422; *The Chebyshev polynomials* (Wiley-Interscience, New York, 1974).
7.
8.
9.  David G. Luenberger: *Introduction to Linear and Nonlinear Programming*, Addison-Wesley Publishing Company 1973.
10. 2/73 "The Optimization of Bandlimited Systems" – G. C. Temes, F. C. Marshall and V. Barcilon. Proceedings IEEE.
11.