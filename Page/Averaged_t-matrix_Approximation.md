> この記事は[Averaged t-matrix Approximation](https://ja.wikipedia.org/wiki/Averaged_t-matrix_Approximation)から翻訳されています。


**ATA**(Averaged t-matrix Approximation)は、ポテンシャルの配置が[ランダム](https://ja.wikipedia.org/wiki/ランダム "wikilink")な系における[電子](https://ja.wikipedia.org/wiki/電子 "wikilink")の[散乱](https://ja.wikipedia.org/wiki/散乱 "wikilink")を記述するt行列の扱い（平均化）に対する近似の一つ。この近似を利用することによってランダムな系での電子状態の計算が可能となる。ATAは[CPAの前段階の近似であり](https://ja.wikipedia.org/wiki/コヒーレントポテンシャル近似 "wikilink")、[自己無撞着](https://ja.wikipedia.org/wiki/自己無撞着 "wikilink")（＝セルフコンシステント）な計算が行われていない。従ってその分、計算は高速だが精度は劣る。ATA、CPAが比較的扱い易いのは、[合金](https://ja.wikipedia.org/wiki/合金 "wikilink")などでポテンシャルは周期的に並んでいるが、その各成分原子がランダムに配置しているような場合である。

## 原理

置換型の[不規則二元合金](https://ja.wikipedia.org/wiki/不規則二元合金 "wikilink")を考え、これによる2種類のポテンシャルをそれぞれ **A**、**B** で区別する。それぞれの成分比は、A : B = x : 1 - x(= y) とする（三元以上の系への拡張も可能）。ポテンシャルAのサイトに対応するt行列をτ<sub>A</sub>、ポテンシャルBに対応するt行列をτ<sub>B</sub>として、ATAでは、

\[\tau_l^{AT} = x \tau_l^A + y \tau_l^B = \left\langle \tau_l \right\rangle\] とする（lは[軌道角運動量](https://ja.wikipedia.org/wiki/軌道角運動量 "wikilink")とし、これ以降は省略）。\(\, \langle \rangle\)は濃度平均を意味している。つまり、合金の成分濃度による平均を行ったt行列（τ<sup>AT</sup>）を用いるのが“平均されたt行列による近似”(=ATA)である。

以上から、[単サイト近似](https://ja.wikipedia.org/wiki/単サイト近似 "wikilink")での\(T_{\mathbf{q}}^{eff}\)は、

\[T_{\mathbf{q}}^{eff} \to T_{\mathbf{q}}^{AT} = \left[{\left\langle \tau \right\rangle}^{-1} - B_{\mathbf{q}} \right]^{-1}\] となり、\<T<sub>00</sub>\>は、

\[{\left\langle T_{00} \right\rangle}_{0 = A(B)} = \tau_{A(B)} {\left\langle \tau \right\rangle}^{-1} \left\langle T_{00} \right\rangle = {\tau_{A(B)} \over {N {\left\langle \tau \right\rangle} } } \sum_{\mathbf{q}} T_{\mathbf{q}}^{AT}\] となる。これは、[多重散乱理論](https://ja.wikipedia.org/wiki/多重散乱理論 "wikilink")の記事内でT<sub>n</sub>の式が、

\[T_n = t_n \left[1 + \tilde{G} \sum_{n \ne m} T_m\right]\] と表されるので、

\[{\left\langle T_0 \right\rangle}_{0 = A} = t_0^A \left[1 + \tilde{G} \sum_{n \ne 0} \left\langle T_n \right\rangle\right] = t_0^A {\left\langle t_0 \right\rangle}^{-1} \cdot {\left\langle t_0 \right\rangle} \left[1 + \tilde{G} \sum_{n \ne 0} \left\langle T_n \right\rangle\right] = t_0 {\left\langle t_0 \right\rangle}^{-1} {\left\langle T_0 \right\rangle}\] から導かれる。この、\({\left\langle T_{00} \right\rangle}_{0 = A(B)}\)を、単サイト近似での[状態密度](../Page/状態密度.md "wikilink")の表式に代入すると、

\[\begin{matrix} & D(E) - D_0(E) & \\ \ & = & - {2 \over {\pi} } \mathrm{Im Tr} \left[x {\tau_{A} \over {N {\left\langle \tau \right\rangle} } } \sum_{\mathbf{q}} T_{\mathbf{q}}^{AT} {d \tau_A^{-1} \over {dE} } + y {\tau_{B} \over {N {\left\langle \tau \right\rangle} } } \sum_{\mathbf{q}} T_{\mathbf{q}}^{AT} {d \tau_B^{-1} \over {dE} } - {1 \over N} \sum_{\mathbf{q}} T_{\mathbf{q}}^{AT} {d B_{\mathbf{q}} \over {dE} } \right] \\ \ & = & - {2 \over {\pi} } \mathrm{Im Tr} \left[{\left\langle \tau \right\rangle}^{-1} \left\{ x \tau_A {d \tau_A^{-1} \over {dE} } + y \tau_B {d \tau_B^{-1} \over {dE} } \right\} \sum_{\mathbf{q}} T_{\mathbf{q}}^{AT} - \sum_{\mathbf{q}} T_{\mathbf{q}}^{AT} {d B_{\mathbf{q}} \over {dE} }\right] \\ \ & = & {2 \over {\pi} } \mathrm{Im Tr} \sum_{\mathbf{q}} T_{\mathbf{q}}^{AT} \left[{\left\langle \tau \right\rangle}^{-1} \left\{ x \tau_A {d \tau_A^{-1} \over {dE} } + y \tau_B {d \tau_B^{-1} \over {dE} } \right\} + {d B_{\mathbf{q}} \over {dE} }\right] \end{matrix}\] となる。これが**ATA**における電子の状態密度の表式である。Imは複素数の虚数部分を取ること、Trはトレース（跡）を取ることである。

更に、ここで**スペクトル密度**a(**q**,E)を以下のように定義する（D<sub>0</sub>(E)からの寄与は省略）。

\[D(E) = \sum_{\mathbf{q}} a (\mathbf{q}, E)\] 従って、スペクトル密度の表式は、

\[a (\mathbf{q}, E) = {2 \over {\pi} } \mathrm{Im Tr} T_{\mathbf{q}}^{AT} \left[{\left\langle \tau \right\rangle}^{-1} \left\{ x \tau_A {d \tau_A^{-1} \over {dE} } + y \tau_B {d \tau_B^{-1} \over {dE} } \right\} + {d B_{\mathbf{q}} \over {dE} }\right]\] となる。ここで、**q**を[k点に対応させると](https://ja.wikipedia.org/wiki/ブリュアンゾーン#k点 "wikilink")、スペクトル密度から[バンド構造](../Page/バンド構造.md "wikilink")（E-k曲線）が得られる。

## 関連項目

  - [散乱理論](https://ja.wikipedia.org/wiki/散乱理論 "wikilink")
  - [仮想結晶近似](https://ja.wikipedia.org/wiki/仮想結晶近似 "wikilink")
  - [バンド計算](../Page/バンド計算.md "wikilink")

[Category:バンド計算](https://ja.wikipedia.org/wiki/Category:バンド計算 "wikilink")