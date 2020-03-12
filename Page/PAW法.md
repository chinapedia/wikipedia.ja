> この記事は[PAW](https://ja.wikipedia.org/wiki/PAW)から翻訳されています。


**PAW法** () は[第一原理電子構造計算](https://ja.wikipedia.org/wiki/第一原理電子構造計算 "wikilink")の手法の一つ。[擬ポテンシャル](../Page/擬ポテンシャル.md "wikilink")法と[LAPW法](https://ja.wikipedia.org/wiki/LAPW法 "wikilink")を一般化した手法であり、より効率的に[密度汎関数計算を行うことを可能とする](../Page/密度汎関数理論.md "wikilink")。P. E. Blöchlが1994年に発表した手法で、数ある全電子計算手法の中でも新しい。

価電子[波動関数](../Page/波動関数.md "wikilink")はイオンコア近傍では、コア波動関数との直交性を保つために短い波長で振動することが多い。このことは、波動関数を正確に表現するために多くのフーリエ成分（グリッドを用いる手法では細かいメッシュ）を必要とするため計算コスト上の問題となる。 PAW法ではこの問題を、短波長で振動する波動関数を、計算コスト的により扱いやすい長波長で滑らかな波動関数に変形し、この滑らかな波動関数から全電子の特性を計算することを可能とすることで解決する試みである。全電子計算の手法であるため、内核付近の記述や、光学応答の計算に適している。このアプローチは、[シュレーディンガー描像](https://ja.wikipedia.org/wiki/シュレーディンガー描像 "wikilink")から[ハイゼンベルク描像](../Page/ハイゼンベルク描像.md "wikilink")への転換にある意味で似ている。

## 波動関数の変換

ある[線形変換](https://ja.wikipedia.org/wiki/線型写像 "wikilink") \(\mathcal{T}\) により、仮定上の擬波動関数 \(|\tilde{\Psi}\rangle\) が全電子波動関数 \(|\Psi\rangle\) に変換されるものとする。

  -
    \(|\Psi\rangle=\mathcal{T}|\tilde{\Psi}\rangle\)

「全電子」波動関数はコーン・シャム一粒子波動関数であり、[多体波動関数](https://ja.wikipedia.org/wiki/多体波動関数 "wikilink")ではないことに注意。イオンコア近傍以外では \(|\tilde{\Psi}\rangle\) と \(|\Psi\rangle\) が一致するようにするため、線形変換を以下のように書くものとする。

  -
    \(\mathcal{T}=1+\sum_R\hat{\mathcal{T}}_R\)

ここでは \(\hat{\mathcal{T}}_R\) はある球形の原子  を含む補正領域 \(\Omega_R\) でのみ非零であるとする。

各原子の周辺では、擬波動関数を[擬部分波により展開するのが便利である](https://ja.wikipedia.org/wiki/部分波展開 "wikilink")。

  -
    \(|\tilde{\Psi}\rangle=\sum_i|\tilde{\phi}_i\rangle c_i\) within \(\Omega_R\)

\(\mathcal{T}\) は線形な変換であるから、係数 \(c_i\) はプロジェクタ関数と呼ばれる関数の集合 \(|p_i\rangle\) との内積により表現される。

  -
    \(c_i=\langle p_i|\tilde{\Psi}\rangle\)

ここで \(\langle p_i|\tilde{\phi}_j\rangle=\delta_{ij}\) とする。全電子部分波は \(|\phi_i\rangle=\mathcal{T}|\tilde{\phi}_i\rangle\) と書かれ、典型的には孤立原子におけるコーン・シャム・シュレーディンガー方程式の解と一致するように取る。 よって、線形変換 \(\mathcal{T}\) は次の三つの量で記述される。

1.  全電子部分波の集合 \(|\phi_i\rangle\)
2.  擬部分波の集合 \(|\tilde{\phi}_i\rangle\)
3.  プロジェクタ関数の集合 \(|p_i\rangle\)

そして、次のように陽に書き下せる。

  -
    \(\mathcal{T} = 1 + \sum_i \left( | \phi_i \rangle - | \tilde{\phi}_i \rangle \right) \langle p_i |\)

補正領域の外側では擬部分波は全電子部分波と一致する。領域の内側では、適当な滑らかな接続関数、たとえば多項式や[ベッセル関数](../Page/ベッセル関数.md "wikilink")の線形結合により表わされる。

PAW法は通常、コア状態はイオンのおかれた環境により影響されないとする[フローズンコア近似](https://ja.wikipedia.org/wiki/フローズンコア近似 "wikilink")と共に用いられることが多い。事前に計算されたPAWデータのオンラインリポジトリがいくつか存在する\[1\]\[2\]\[3\]。

## 作用素の変換

PAW変換により、全電子波動関数を陽にメモリ上に展開することなく、擬波動関数から全電子の可観測量を計算することが可能となる。このことは、原子核近傍の波動関数に強く依存する[NMRなどの特性を計算する際に特に重要である](https://ja.wikipedia.org/wiki/核磁気共鳴 "wikilink")。まず、ある作用素の期待値は次のように定義される。

  -
    \(a_i = \langle \Psi | \hat{A} | \Psi \rangle\)

ここで、全電子波動関数から擬波動関数に \(|\Psi\rangle=\mathcal{T}|\tilde{\Psi}\rangle\) のように変換すると、以下を得る。

  -
    \(a_i = \langle \tilde{\Psi} | \mathcal{T}^\dagger \hat{A} \mathcal{T} | \tilde{\Psi} \rangle\)

「擬作用素」をチルダで表わすこととして、次のように定義することができる。

  -
    \(\tilde{A} = \mathcal{T}^\dagger \hat{A} \mathcal{T}\)

もし \(\hat{A}\) が局所的でふるまいの良い作用素であれば、 \(\mathcal{T}\) の定義式を代入して下のような PAW 作用素変換を得ることができる。

  -
    \(\tilde{A} = \hat{A} + \sum_{i,j} | p_i \rangle \left( \langle \phi_i | \hat{A} | \phi_j \rangle - \langle \tilde{\phi}_i | \hat{A} |\tilde{\phi}_j \rangle \right) \langle p_j |\)

ここで、添字 \(i,j\) は全原子についてのプロジェクタを走るものとする。通常、同一の原子上の添字のみを足し上げ、オフサイトの寄与は無視することが多い。これを「オンサイト近似」と呼ぶ。

原論文で、 Blöchl は補正領域の内部に局在した任意の作用素 \(\hat{B}\) についてのこの等式には自由度があると述べている。つまり次のような項が付け加わる。

  -
    \(\hat{B} - \sum_{i,j} | p_i \rangle \langle \tilde{\phi}_i | \hat{B} |\tilde{\phi}_j \rangle \langle p_j |\)

このことはPAW法において擬ポテンシャルを実装して原子核によるクーロンポテンシャルをより滑らかなポテンシャルに置き換える際の基礎ととらえることができる。

## 出典

## 参考文献

  -
  -
  -
  -
  -
## PAW法を実装するソフトウェア

  - [ABINIT](../Page/ABINIT.md "wikilink")

  - (NMR特性計算)

  - [CP-PAW](http://www2.pt.tu-clausthal.de/paw/)

  - [GPAW](http://wiki.fysik.dtu.dk/gpaw/)

  -
  -
  - [S/PHI/nX](http://www.sphinxlib.de)

  -
  - [VASP](https://ja.wikipedia.org/wiki/Vienna_Ab_initio_Simulation_Package "wikilink")

## 外部リンク

  -
  -
  -

[Category:計算科学](https://ja.wikipedia.org/wiki/Category:計算科学 "wikilink") [Category:物性物理学](https://ja.wikipedia.org/wiki/Category:物性物理学 "wikilink") [Category:バンド計算](https://ja.wikipedia.org/wiki/Category:バンド計算 "wikilink")

1.  [PAW atomic data for ABINIT code](https://ja.wikipedia.org/wiki/#abinit "wikilink")
2.  [Periodic Table of the Elements for PAW Functions](https://ja.wikipedia.org/wiki/#periodictable "wikilink")
3.  [Atomic PAW Setups](https://ja.wikipedia.org/wiki/#gpaw "wikilink")