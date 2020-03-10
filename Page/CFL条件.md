> この記事は[CFL](https://ja.wikipedia.org/wiki/CFL)から翻訳されています。


**CFL条件**（シーエフエルじょうけん、）または**クーラン条件**とは、[数値解析](https://ja.wikipedia.org/wiki/数値解析 "wikilink")によるコンピュータ[シミュレーション](../Page/シミュレーション.md "wikilink")において、「情報が伝播する速さ」は「実際の現象で波や物理量が伝播する速さ」よりも速くなければならないという必要条件のことである。1928年に、Richard Courant、Kurt Friedrichs、Hans Lewyによって提唱された\[1\]。

## 概要

例えば、[離散格子系において](https://ja.wikipedia.org/wiki/メッシュ法 "wikilink")[波動](../Page/波動.md "wikilink")を扱う場合に、その[運動方程式](https://ja.wikipedia.org/wiki/運動方程式 "wikilink")の数値解を求める際に用いる時間ステップΔ*t* の値は、実際の波動が隣り合う格子に伝達するまでの時間よりも小さくなければならない。もしΔ*t* の値がその時間の上限を超えると、計算上の情報伝達速度が実現象の速さに追従できずに数値[発散が生じてしまい](../Page/極限.md "wikilink")、物理的に意味の無い解を得てしまう。格子の間隔Δ*x* が小さくなると、時間ステップΔ*t* の上限値も減少する。

CFL条件は[陽解法](https://ja.wikipedia.org/wiki/陽解法 "wikilink")の時間進展を行う際に用いられる条件であり、この条件を回避するためにしばしば[陰解法](https://ja.wikipedia.org/wiki/陰解法 "wikilink")が用いられる場合がある。陰解法を用いることでCFL条件を回避したり緩和できる理由としては様々な説明が存在するが、最も簡潔に説明すると、陽解法は1ステップ前の自分の周りのごくわずかな[格子点](https://ja.wikipedia.org/wiki/格子点 "wikilink")のみから情報を得て次の時間の値を決めるのに対して、陰解法は1ステップ前の(ほぼ)全ての格子点の情報を処理して次の時間の値を決めるためであり、CFL条件におけるΔ*x* が実質的に巨大になるためである。

## 数式による説明

実際の現象を速さ（特性速度）が *C* の波動であるとする。この現象は次の[移流](https://ja.wikipedia.org/wiki/移流 "wikilink")方程式で記述される：

  -
    \(\frac{\partial u}{\partial t}+C\frac{\partial u}{\partial x}=0\)

この方程式を時間ステップ幅Δ*t* 、格子幅Δ*x* として、時間微分に1次精度陽解法、空間微分に1次精度[風上差分](https://ja.wikipedia.org/wiki/風上差分 "wikilink")を用いて[離散化すると](../Page/差分法.md "wikilink")、

  -
    \(\frac{u^{n+1}_i-u^n_i}{\Delta t}+C\frac{u^n_i-u^n_{i-1}}{\Delta x}=0\)

すなわち

  -
    \(u^{n+1}_i=u^n_i-\frac{C\Delta t}{\Delta x}(u^n_i-u^n_{i-1})\)

となる。このとき、情報が伝播する速さはΔ*x* /Δ*t*、実際の波の速さは*C*であるから

  -
    \(\frac{\Delta x}{\Delta t}>C\)

がCFL条件となる。この式を[無次元数](https://ja.wikipedia.org/wiki/無次元数 "wikilink")である**クーラン数** *C* Δ*t* /Δ*x* を使って、「クーラン数は1より小さくなければならない」と表現することもある。

## 参考文献

## 関連項目

  - [拡散数](https://ja.wikipedia.org/wiki/拡散数 "wikilink")

[Category:数値微分方程式](https://ja.wikipedia.org/wiki/Category:数値微分方程式 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink") [Category:流体力学の無次元数](https://ja.wikipedia.org/wiki/Category:流体力学の無次元数 "wikilink") [Category:数値流体力学](https://ja.wikipedia.org/wiki/Category:数値流体力学 "wikilink")

1.