> この記事は[N体シミュレーション](https://ja.wikipedia.org/wiki/N体シミュレーション)から翻訳されています。


**N体シミュレーション** (エヌたいシミュレーション、N-body simulation) とは、[天体物理学](../Page/天体物理学.md "wikilink")および[天文学](../Page/天文学.md "wikilink")において、[重力](../Page/重力.md "wikilink")相互作用する\(N\)個の粒子の[力学](https://ja.wikipedia.org/wiki/力学 "wikilink")的な進化を数値的に計算するシミュレーションのことをいう\[1\]。2体系つまり[ケプラー問題](https://ja.wikipedia.org/wiki/ケプラー問題 "wikilink")は[可積分](https://ja.wikipedia.org/wiki/可積分 "wikilink")であるが、3体以上の系（[重力多体系](https://ja.wikipedia.org/wiki/重力多体系 "wikilink")）は可積分ではなく、その力学的進化を定量的に予測するためには数値シミュレーションが必須である\[2\]。[太陽系](../Page/太陽系.md "wikilink")や[球状星団](../Page/球状星団.md "wikilink")、[銀河](../Page/銀河.md "wikilink")あるいは[宇宙の大規模構造](../Page/宇宙の大規模構造.md "wikilink")など、重力多体系は宇宙のあらゆる領域において重要な役割を果たすため、N体シミュレーションは宇宙に関する理論的研究において極めて重要な役割を果たしている。

[Galaxy_cluster_sim.png](https://ja.wikipedia.org/wiki/File:Galaxy_cluster_sim.png "fig:Galaxy_cluster_sim.png")における質量分布。\]\]

ナイーブなN体シミュレーションの実装（直接総和法）は重力相互作用の計算に \(\mathcal{O} ( N^2 )\) のコストを要するため、より大規模かつ長時間にわたるシミュレーションを実現することは[計算機科学](../Page/計算機科学.md "wikilink")特に[高性能計算](../Page/高性能計算.md "wikilink") (HPC) の分野においても興味深い問題であり、複数の[ゴードン・ベル賞](../Page/ゴードン・ベル賞.md "wikilink")が\(N\)体シミュレーションの研究に対して与えられた\[3\]\[4\]。現在でも\(N\)体シミュレーションはコンピュータの[ベンチマーク](../Page/ベンチマーク.md "wikilink")のためにしばしば用いられる\[5\]。

## 概要

[Three-body_Problem_Animation.gif](https://ja.wikipedia.org/wiki/File:Three-body_Problem_Animation.gif "fig:Three-body_Problem_Animation.gif")

[太陽系](../Page/太陽系.md "wikilink")における[惑星](../Page/惑星.md "wikilink")の運動\[6\]、[原始惑星系円盤](../Page/原始惑星系円盤.md "wikilink")における[微惑星](../Page/微惑星.md "wikilink")の集積過程\[7\]、[球状星団](../Page/球状星団.md "wikilink")の構造の力学的な進化\[8\]、[宇宙の大規模構造](../Page/宇宙の大規模構造.md "wikilink")の形成\[9\]といった問題は、系を構成する要素（惑星や恒星、[暗黒物質](../Page/暗黒物質.md "wikilink")など）が互いに[重力](../Page/重力.md "wikilink")相互作用を及ぼし合うものである。その進化を定量的に求めることは[天文学](../Page/天文学.md "wikilink")および[宇宙物理学](https://ja.wikipedia.org/wiki/宇宙物理学 "wikilink")の多くの分野で重要であるが、それは解析的な手法では困難であり、[数値シミュレーションに頼らざるを得ない](https://ja.wikipedia.org/wiki/数値解析 "wikilink")\[10\]。\(N\)体シミュレーションはこのような系の数値シミュレーション手法のひとつであり、系を構成する要素を多数の（\(N\)個の）粒子とみなし、それらの粒子が互いにニュートン重力を及ぼし合うものとモデル化するものである。

典型的な\(N\)体シミュレーションでは、\(i = 1, 2, \cdots, N\) 番目の粒子（質量 \(m_i\)) の[運動方程式](https://ja.wikipedia.org/wiki/運動方程式 "wikilink")は

\[m_i \frac{ d^2 \mathbf{r}_i }{ d t^2 } = - \sum_{j \neq i} G m_i m_j \frac{ \mathbf{r}_i - \mathbf{r}_j }{ \left| \mathbf{r}_i - \mathbf{r}_j \right|^3 }\] であり、これを適切な初期条件のもとで数値的に積分することが主たる目標となる\[11\]（[宇宙の大規模構造](../Page/宇宙の大規模構造.md "wikilink")など[宇宙論](../Page/宇宙論.md "wikilink")的なスケールでの進化を扱う場合、後述のように方程式が修正されるが、本質的な差異はない）。その最も単純かつ非自明な問題が[三体問題](https://ja.wikipedia.org/wiki/三体問題 "wikilink")である。

シミュレーションの目的によって様々な数値計算上の困難が存在し、各分野毎に様々な手法が開発されてきた。

  - 太陽系シミュレーションの場合、長時間の進化の結果として最終的にどのような状態になるのかに興味がある。この場合、数値誤差の累積が最大の問題であり、高次のシンプレクティック積分を用いるなどの誤差を極力抑えるための工夫が必要となる。また、この場合中心天体（[太陽](../Page/太陽.md "wikilink")）の重力が支配的で、それに対して摂動が加わった系であるとみなせるため、[天体力学](../Page/天体力学.md "wikilink")的手法など特有の手法が用いられる。\[12\]
  - 球状星団の場合、重力相互作用のコストが重い上に、近接散乱や連星形成などの効果を正しく計算することが必要である\[13\]。初期の[GRAPE](../Page/GRAPE.md "wikilink")は球状星団の力学進化の計算に用いられ、大きな成果を上げた。
  - 銀河またはより大きなスケールを扱う問題の場合、これは無衝突系であるため \(N\) 体粒子は真の粒子である必要はなく、ある空間領域に存在する[暗黒物質](../Page/暗黒物質.md "wikilink")あるいは[バリオン](https://ja.wikipedia.org/wiki/バリオン "wikilink")を束ねたものである。一方で、より計算領域を大きく、またシミュレーションの分解能を小さくすることが必要である。このため[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")などの大規模並列計算機が採用され、また重力相互作用の計算コストを下げるためにアルゴリズム上の改善が続けられている。

### 無衝突系と衝突系

[The_globular_cluster_NGC_6388_observed_by_the_European_Southern_Observatory.jpg](https://ja.wikipedia.org/wiki/File:The_globular_cluster_NGC_6388_observed_by_the_European_Southern_Observatory.jpg "fig:The_globular_cluster_NGC_6388_observed_by_the_European_Southern_Observatory.jpg")は典型的な重力多体系（衝突系）であり、その力学的進化の理論的研究において\(N\)体シミュレーションが重要な役割を果たした。\]\] \(N\) 体シミュレーションはその対象によって大きく無衝突系 (collisionless system) と衝突系 (collisional system) に分類される\[14\]\[15\]。これは[二体緩和](https://ja.wikipedia.org/wiki/二体緩和 "wikilink")の効果が重要かどうかを意味し、それによってシミュレーションの性質が大きく変化する。

[二体緩和](https://ja.wikipedia.org/wiki/二体緩和 "wikilink")とは、重力多体系において二体間の近接散乱による系の熱的な進化のことを言う\[16\]。二体緩和による系の進化に要する時間スケール \(t_\mathrm{relax}\) は、粒子数 \(N\) と crossing-time \(t_\mathrm{cross}\) を用いて

\[t_\mathrm{relax} = \frac{ N }{ \ln N } t_\mathrm{cross}\] と書ける\[17\]。それ故に、極めて粒子数の大きなスケールでは二体緩和が効く時間は[宇宙年齢](https://ja.wikipedia.org/wiki/宇宙年齢 "wikilink")よりも長くなり、その効果を無視することができる。例えば[銀河](../Page/銀河.md "wikilink")は \(N \sim 10^{10}\) 個の恒星からなる系であり、その力学的な進化には二体緩和の効果は重要ではないと考えられている。一方、[球状星団](../Page/球状星団.md "wikilink")では \(N \sim 10^{4-6}\) であり、二体緩和が重要である\[18\]。

二体緩和が効かない無衝突系では粒子数無限大の極限に相当する\[19\]。このとき重力場はある種の平均場として扱うことが可能であり、個々の粒子に起因する特異性を考慮する必要はない\[20\]。そのため、シミュレーションに際してツリー法などのより効率的なスキームを使用することができる\[21\]。また、シミュレーションで扱われる粒子は真の粒子ではなく、[位相空間のある領域を代表する点であると解釈される](../Page/位相空間_\(物理学\).md "wikilink")\[22\]。

## 時間積分

### 積分子

\(N\) 体シミュレーションはエネルギーが保存するため、時間積分子として[リープ・フロッグ法](https://ja.wikipedia.org/wiki/リープ・フロッグ法 "wikilink")などのがしばしば採用される。例えば太陽系の高精度シミュレーション\[23\]、宇宙論的構造形成\[24\]など。

衝突系では後述する可変時間刻みと相性の良い[予測子修正子法](https://ja.wikipedia.org/wiki/予測子修正子法 "wikilink")\[25\]や[エルミート積分子](https://ja.wikipedia.org/wiki/エルミート積分子 "wikilink")\[26\]も用いられる。

### 可変時間刻みと独立時間刻み

自己重力系は一般に[重力不安定性](https://ja.wikipedia.org/wiki/重力不安定性 "wikilink")により[密度](../Page/密度.md "wikilink")ゆらぎが成長し、高密度領域を形成するように進化する。その結果、高密度領域の中心部では

\[t_\mathrm{free} = \frac{ 1 }{ \sqrt{ G \rho } }\] が急速に短くなるため, 精度の良いシミュレーションを行うためには時間積分のタイムステップを動的に小さく調整することが望ましい\[27\]。このような手法はと呼ばれる\[28\]。

ところが、特に衝突系で連星形成が起こるような状況では、一部の\(N\)体粒子は極めて短い時間で進化するものの、その他の大多数の粒子の軌道進化に小さな時間刻みが必要ないという可能性がある。この場合、最も小さな時間ステップに合わせて全体の時間刻みを調整すると、シミュレーションに多大な時間を要することになり、また不必要に小さな時間ステップに伴う数値積分誤差が累積する可能性がある。そこで必要な粒子のみ小さな時間刻み幅で時間積分を行う[独立時間刻み](https://ja.wikipedia.org/wiki/独立時間刻み "wikilink")という手法が開発された\[29\]\[30\]。この場合、その他の大多数の粒子については適当な補間を用いてその重力場を見積もり、必要な粒子のみ正確に時間積分を行うことになる。

## 重力相互作用

特に無衝突系においてはシミュレーションの規模 (つまり粒子数 \(N\)) を大きくすることが重要である。しかし粒子 \(i\) に作用する重力

\[\mathbf{F}_i = - \sum_{j \neq i} G m_i m_j \frac{ \mathbf{r}_i - \mathbf{r}_j }{ \left| \mathbf{r}_i - \mathbf{r}_j \right|^3 }\] をすべての粒子について愚直に計算する（これを直接総和法 direct summation という）ことは \(\mathcal{O} ( N^2 )\) という大きな計算時間を要するため、粒子数 \(N\) を大きくすると急速に計算時間が増大し、現実的な時間で計算を終えることができなくなる\[31\]。このため、PM法とツリー法という重力計算の精度を下げてでもより効率的な相互作用の計算アルゴリズムが開発された。現在ではこれらの方法を組み合わせた P<sup>3</sup>M 法やtree-PM 法が大規模シミュレーションにおいて標準的な方法として採用されている\[32\]。

### Particle-Mesh 法

Particle-Mesh (PM) 法は[高速フーリエ変換](../Page/高速フーリエ変換.md "wikilink")に基づいて[重力ポテンシャル](https://ja.wikipedia.org/wiki/重力ポテンシャル "wikilink")の計算を行う\[33\]。まず最初に計算領域に[グリッドを生成し](../Page/格子.md "wikilink")、各頂点での密度の値をその近傍の粒子分布に基づいて決定する。重力ポテンシャルは (フーリエ空間では) [ラプラス方程式](../Page/ラプラス方程式.md "wikilink")

\[- k^2 \Phi_\mathbf{k} = 4 \pi G \rho_\mathrm{k}\] により密度場に結びついているため、密度場のフーリエ係数 \(\rho_\mathbf{k}\) を求め、そこから逆フーリエ変換することにより重力ポテンシャル \(\Phi\) や重力場 \(- \nabla \Phi\) を求めることができる。この計算時間はグリッド数を \(M\) とすると \(\mathcal{O} ( M \ln M )\) である。

なお近くの粒子からの重力は直接法で、遠方の粒子からの寄与は PM 法で計算する複合的な手法のことを Particle-Particle Particle-Mesh (P<sup>3</sup>M) 法と呼ぶ\[34\]\[35\]。

### ツリー法

[Barnes-Hut_tree_construction.png](https://ja.wikipedia.org/wiki/File:Barnes-Hut_tree_construction.png "fig:Barnes-Hut_tree_construction.png") Barnes & Hut (1986) により提案された、粒子分布をツリー構造という形で保持することにより重力相互作用の計算を \(\mathcal{O} ( N \ln N )\) で行うアルゴリズムは現在 Barnes & Hut のツリー法として広く用いられている\[36\]。これは計算領域を表す立方体を階層的により小さな立方体に分割し、最終的に各立方体がひとつ以下の粒子しか含まないようにすることにより、粒子分布の情報を[ツリーとして保持するものである](../Page/木構造_\(データ構造\).md "wikilink")。ツリーの深さは \(\mathcal{O} ( \ln N )\) であるため、ツリーの構成に要する計算量は \(\mathcal{O} ( N \ln N )\) である\[37\]。

ある粒子に作用する重力を計算する際には、遠方の粒子群からの寄与をまとめて計算することによりコストを削減する。この際に各立方体の重心および質量を用いるが、計算の精度を上げるために[四重極モーメント](https://ja.wikipedia.org/wiki/四重極モーメント "wikilink")などを用いる場合もある\[38\]。

なお近くの粒子からの重力はツリー法で、遠方の粒子からの寄与は PM 法で計算する複合的な手法のことを tree-PM 法と呼ぶ\[39\]。

## 重力の近距離発散

ふたつの\(N\)体粒子間の距離が極めて小さくなると、両者の間に働く重力は任意に大きくなり得る。これは衝突系においては物理的に重要であり、その影響を正しくシミュレーションする必要がある。一方、無衝突系ではこの効果は物理的ではなく、カットオフにより除去される。

### 正則化

衝突系において近距離発散に対処するために可変時間刻み幅を用いる場合、時間ステップが際限なく小さくなり、シミュレーションがほとんど進まなくなってしまう。しかしながら、二体問題における近距離重力に起因する特異性は見かけのものであり、適切な変数変換により除去することができる。この手続きは正則化 (regularization) として知られる。

Burdet-Heggie正則化\[40\]\[41\]\[42\]は、時間座標 \(t\) を近接粒子の距離に応じて調整することで特異性を除去するもので、新しい時間座標 \(\tau\) を二体の粒子間距離 \(r\) と真の時間 \(t\) から

\[d\tau = \frac{ d t }{ r }\] により定義するものである\[43\]。このとき二体の相対位置ベクトル \(\mathbf{r}\) の従う方程式は

\[\frac{ d^2 \mathbf{r} }{ d \tau^2 } - 2 E_2 \mathbf{r} = - \mathbf{e} + r^2 \mathbf{g}\] へと帰着される。ここに \(E_2\) は二体の相対運動エネルギー、\(\mathbf{e}\) は[離心率ベクトル](https://ja.wikipedia.org/wiki/ルンゲ＝レンツベクトル "wikilink")、\(\mathbf{g}\) は他の天体による重力場である。この表式からわかるように、BH正則化により \(r \to 0\) での特異性が除去される\[44\]。

[1965年](../Page/1965年.md "wikilink")に提案された[クスターンハイモ・シュティーフェル変換](https://ja.wikipedia.org/wiki/クスターンハイモ・シュティーフェル変換 "wikilink") (Kustaanheimo-Stiefel transformation)\[45\] は3次元直交座標 \(x, y, z\) を4次元のスピノルへと変換するもので、BH正則化よりも精度の良い結果が得られる\[46\]。

\[u_1^2 = \frac{ x + r }{ 2 } \cos^2 \psi , \ \ u_2 = \frac{ y u_1 + z u_4 }{ x + r } , \ u_4^2 = \frac{ x + r }{ 2 } \sin^2 \psi , \ u_3 = \frac{ z u_1 - y u_4 }{ x + r }\]

### 近距離カットオフ

無衝突系においては、\(N\)体粒子は真の粒子ではなく、多数の粒子が占める[位相空間上の領域を表す](../Page/位相空間_\(物理学\).md "wikilink")。そのため、\(N\)体粒子間に働く重力が近距離で発散する効果は物理的ではなく、適当なカットオフにより除去される必要がある\[47\]。最も簡単なカットオフとしては重力ポテンシャル \(\Phi\) を

\[\Phi ( r ) = - \frac{ G M }{ \sqrt{ r^2 + \epsilon^2 } }\] へと変更するものである\[48\]。ここに \(\epsilon\) は距離の次元を持つ定数で、この距離スケールより近距離での重力の発散を抑える効果を持つ。このポテンシャルは\(N\)体粒子が[プラマーモデル](https://ja.wikipedia.org/wiki/プラマーモデル "wikilink")であるような質量分布を持つと仮定した場合に得られるものに等しい。\(\epsilon\) の値は平均粒子間距離のオーダーに選ばれる\[49\]。

## 宇宙論的\(N\)体シミュレーション

[LCDM.jpg](https://ja.wikipedia.org/wiki/File:LCDM.jpg "fig:LCDM.jpg")の密度分布を表す。[フィラメント](../Page/フィラメント.md "wikilink")構造や[ダークマターハロー](https://ja.wikipedia.org/wiki/ダークマターハロー "wikilink")が形成されていることが確認できる。\]\]

[大規模構造の形成などの宇宙論的な問題は](../Page/宇宙の大規模構造.md "wikilink")\(N\)体シミュレーションが用いられる典型的かつ重要なセットアップであるが、[宇宙膨張](https://ja.wikipedia.org/wiki/宇宙膨張 "wikilink")を考慮する必要があるという点で他の問題とは異なっている。この種のシミュレーションは非線型成長後の物質の密度ゆらぎの[パワースペクトル](https://ja.wikipedia.org/wiki/パワースペクトル "wikilink")、あるいは[ダークマターハロー](https://ja.wikipedia.org/wiki/ダークマターハロー "wikilink")の密度プロファイルや質量関数を求めるために用いられる\[50\]。これらの量は観測可能量であり、実際の観測データと比較することにより例えば[宇宙論パラメータ](../Page/宇宙論パラメータ.md "wikilink")の制限を与えることができる。

### 運動方程式

宇宙膨張は、宇宙の現在の大きさを1とする相対的な大きさを表す[スケール因子](https://ja.wikipedia.org/wiki/スケール因子 "wikilink") \(a ( t )\) により表され、その時間発展は[フリードマン方程式](../Page/フリードマン方程式.md "wikilink")

\[\frac{ 1 }{ a } \frac{ d a }{ d t } = H_0 \sqrt{ \Omega_{\mathrm{\Lambda}0} + \Omega_{m0} a^{-3} + \Omega_{r 0} a^{-4} }\] により与えられる。ここに \(H_0\) は[ハッブル定数](https://ja.wikipedia.org/wiki/ハッブル定数 "wikilink")、\(\Omega_{x 0}\) は[密度パラメータである](../Page/宇宙論パラメータ.md "wikilink")。これにより、逆に独立変数として時刻 \(t\) の代わりにスケール因子 \(a\) を用いることができる。

粒子の座標としては宇宙膨張の効果を取り除いた[共動座標](https://ja.wikipedia.org/wiki/共動座標 "wikilink") \(\mathbf{x}\) が用いられる。これは固有座標 \(\mathbf{r}\) と

\[\mathbf{r} = a ( t ) \mathbf{x}\] という関係にある\[51\]。粒子の速度はその微分 \(\frac{ d \mathbf{r} }{ d t } = H \mathbf{r} + a ( t ) \frac{ d \mathbf{x} }{ d t }\) であるが、初期宇宙での発散を回避するために \(\mathbf{w} := \sqrt{ a ( t ) } \frac{ d \mathbf{x} }{ d t }\) が用いられる\[52\]。最終的な運動方程式は

\[\frac{ d \mathbf{x} }{ d a } = \frac{ \mathbf{w} }{ S ( a ) }\]

\[\frac{ d \mathbf{w} }{ d a } = - \frac32 \frac{ \mathbf{w} }{ a } + \frac{ 1 }{ a^2 S ( a ) } \nabla \Phi ( \mathbf{x} )\]

\[S ( a ) = H_0 \sqrt{ \Omega_{m 0} + a^3 \Omega_{\Lambda 0} }\] である\[53\]。

### 周期境界条件

無限に広い計算領域を実現することは不可能であるため、宇宙論的シミュレーションでは[周期境界条件](https://ja.wikipedia.org/wiki/周期境界条件 "wikilink")が採用される\[54\]。通常、計算領域は立方体であり、その一片の長さを \(L\) とするとき、座標 \(x\) と \(x \pm L\) の点は同一視される。

周期境界条件のもとでは隣接する立方体に自らの構造のコピーが存在するため、それが及ぼす重力を考慮する必要がある。これは[分子動力学法](../Page/分子動力学法.md "wikilink")において[クーロン電場に対して開発された](https://ja.wikipedia.org/wiki/クーロンの法則 "wikilink")[エバルトの方法](../Page/エバルトの方法.md "wikilink")を適用することで可能であり、付近のボックスからの重力は直接計算し、遠方のボックスからの重力を[フーリエ級数](../Page/フーリエ級数.md "wikilink")の形で取り入れることにより効率的に精度よく計算される\[55\]。例えば、座標原点にある質量 \(m\) の質点がつくる（規格化された）重力ポテンシャルは、周期境界条件のもとで

\[\hat{\Phi} ( t, {\mathbf{x}}) = - \frac{ G m }{ a } \sum_{{\mathbf{n}}\in \mathbf{Z}^3} \frac{ {{\mathrm{erfc}\,}}( \alpha | {\mathbf{x}}- {\mathbf{n}}L | ) }{ | {\mathbf{x}}- {\mathbf{n}}L | } - \frac{ G m }{ \pi a L } \sum_{{\mathbf{h}}\neq {\mathbf{0}}} \exp \left( - \frac{ \pi^2 | {\mathbf{h}}|^2 }{ \alpha^2 L^2 } \right) \frac{ 1 }{ | {\mathbf{h}}|^2 } e^{i {\mathbf{k}}_{\mathbf{h}}\cdot {\mathbf{x}}} + \frac{ G m }{ a } \frac{ \pi }{ \alpha^2 L^3 }\] となる。ここに \(\alpha\) は任意の正の定数、\(\mathrm{erfc}\) は相補[誤差関数](https://ja.wikipedia.org/wiki/誤差関数 "wikilink")である。

### 初期条件

[Λ-CDMモデル](../Page/Λ-CDMモデル.md "wikilink")では宇宙論的ゆらぎは[インフレーション期に](../Page/宇宙のインフレーション.md "wikilink")[ガウス分布に従って生成されたと考えられており](../Page/ガウス過程.md "wikilink")、線型摂動の範囲では密度ゆらぎのパワースペクトルが指定されれば初期条件を確率的に生成することができる。パワースペクトルは与えられた宇宙論パラメータのもとで[宇宙論的摂動論](https://ja.wikipedia.org/wiki/宇宙論的摂動論 "wikilink")に基づいて計算することができる。なお宇宙論的\(N\)体シミュレーションで最も広く用いられる初期条件は2次の[ラグランジュ摂動](https://ja.wikipedia.org/wiki/ラグランジュ摂動 "wikilink") (2LPT) に基づくものである。\[56\]

## プロジェクト

### ソフトウェア

が中心になって開発された[:en:GADGET](https://ja.wikipedia.org/wiki/:en:GADGET "wikilink")は銀河や宇宙論的構造形成を主なターゲットとする無衝突系のシミュレーションコードであり\[57\]、[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")にバージョン1\[58\]が、[2005年](../Page/2005年.md "wikilink")にバージョン2\[59\]が公開された。[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")などの大規模並列計算機で動かすために[並列化されており](../Page/並列計算.md "wikilink")\[60\]、[C言語](../Page/C言語.md "wikilink")によって実装されている。ライセンスは[GNU GPL](../Page/GNU_General_Public_License.md "wikilink")。

2010年代には[牧野淳一郎](../Page/牧野淳一郎.md "wikilink")らが中心となって汎用的な多体問題シミュレーションフレームワークである[FDPS](https://ja.wikipedia.org/wiki/FDPS "wikilink")が開発されている\[61\]。

### ハードウェア

[GRAPE](../Page/GRAPE.md "wikilink")は[杉本大一郎](../Page/杉本大一郎.md "wikilink")、[牧野淳一郎](../Page/牧野淳一郎.md "wikilink")らによって[東京大学](https://ja.wikipedia.org/wiki/東京大学 "wikilink")で開発された\(N\)体シミュレーション専用計算機であり、重力相互作用の計算を[パイプライン](https://ja.wikipedia.org/wiki/パイプライン "wikilink")として物理的に実装することにより効率的に計算を進めるものである\[62\]\[63\]。現在も[国立天文台](../Page/国立天文台.md "wikilink")などで運用されている\[64\]。

また [GPUの活用](../Page/Graphics_Processing_Unit.md "wikilink")（[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")）も進められている\[65\]\[66\]。

### シミュレーション

21世紀に入ってから、特に大規模なシミュレーションはスーパーコンピュータを長時間占有する必要があるため、大規模なシミュレーションを行いその出力を公開するプロジェクトが行われるようになった。その有名なものが\[67\]であり、他に The Aquarius Project\[68\] などがある。2010年代に実行された[:en:Illustris project](https://ja.wikipedia.org/wiki/:en:Illustris_project "wikilink")\[69\]は\(N\)体シミュレーションだけでなく、[星形成](../Page/星形成.md "wikilink")や[AGNといったバリオン物理を考慮した流体シミュレーションを行っている](../Page/活動銀河.md "wikilink")。

## 歴史

重力多体系の[計算機](../Page/計算機.md "wikilink")を用いた研究すなわち\(N\)体シミュレーションは1960年代から実際的な研究で採用されるようになった\[70\]。例えば[1963年](../Page/1963年.md "wikilink")の[:en:Sverre Aarsethによる](https://ja.wikipedia.org/wiki/:en:Sverre_Aarseth "wikilink") \(N = 100\) 体のシミュレーション\[71\]、[1964年](../Page/1964年.md "wikilink")の Hénon & Heiles による[第三積分](https://ja.wikipedia.org/wiki/第三積分 "wikilink")に関する数値的研究\[72\]（これは \(N = 1\) であるが）、[1973年](../Page/1973年.md "wikilink")の Hénon による多体系の安定性の研究\[73\]など。[ジェームズ・ピーブルス](https://ja.wikipedia.org/wiki/ジェームズ・ピーブルス "wikilink")は[1970年](../Page/1970年.md "wikilink")に \(N = 300\) 体を用いて銀河団形成過程のシミュレーションを行った\[74\]。その後も[1979年](../Page/1979年.md "wikilink")には Efstathiou & Jones が \(N = 500\) 体による[銀河回転](https://ja.wikipedia.org/wiki/銀河回転 "wikilink")の研究\[75\]など、計算機の発達に伴ってより大規模なシミュレーションがなされるようになっていった。

より大規模なシミュレーションの要求は強く、[1986年](../Page/1986年.md "wikilink")に Barnes & Hut\[76\] はツリー法を導入し、同時期に PM 法も確立した\[77\]。[1989年](../Page/1989年.md "wikilink")には[GRAPE](../Page/GRAPE.md "wikilink")プロジェクトがスタートしている。

一方で積分スキームに関する研究も進められた。[天体力学](../Page/天体力学.md "wikilink")の分野からは[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")に[吉田春夫](https://ja.wikipedia.org/wiki/吉田春夫 "wikilink")によりシンプレクティック積分子の一般的な構成方法が示された\[78\]。その翌年牧野はエルミート積分子を導入した\[79\]。やがて[対称型公式](https://ja.wikipedia.org/wiki/対称型公式 "wikilink")の有用性が認められるようになった\[80\]。

[2005年](../Page/2005年.md "wikilink")のでは \(N = 1.0 \times 10^{10}\) の宇宙論的構造形成シミュレーションが遂行されるに至った\[81\]。

## 脚注

## 参考文献

  -
  -
  -
  -
  -
## 関連項目

  - [計算物理学](../Page/計算物理学.md "wikilink")
  - [多体問題](../Page/多体問題.md "wikilink")

[Category:計算物理学](https://ja.wikipedia.org/wiki/Category:計算物理学 "wikilink") [Category:天文学に関する記事](https://ja.wikipedia.org/wiki/Category:天文学に関する記事 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11. 牧野, p.399-400.
12.
13. 牧野, p.399-400, 413-414.
14. 牧野, 福重, et al., p.24-25.
15. Binney & Tremaine, p.122-123.
16.
17. 牧野, 福重, et al., p.27.
18.
19.
20. Binney & Tremaine, p.124.
21. Aarseth, p.94.
22.
23.
24.
25. 牧野, p.402-403.
26. 牧野, p.404-406.
27. 牧野, p.400.
28. Binney & Tremaine, p.205.
29. Aarseth, p.21-23.
30. Binney & Tremaine, p.206-208.
31. Mo, van den Bosch & White, p. 766.
32.
33. Mo, van den Bosch & White, p. 766-767.
34. Binney & Tremaine, p.135.
35. Mo, van den Bosch & White, p. 767.
36.
37. Aarseth, p.94-96.
38. Binney & Tremaine, p.125-129.
39.
40.
41.
42.
43. Binney & Tremaine, p.208-210.
44.
45.
46. Binney & Tremaine, p.210-211.
47. Binney & Tremaine, p.123-125
48.
49.
50. Mo, van den Bosch & White, p. 258-261.
51. Mo, van den Bosch & White, p. 163.
52.
53.
54. Mo, van den Bosch & White, p. 769.
55.
56.
57.
58.
59.
60.
61.
62.
63. 牧野, 福重, et al., p.57-61.
64.
65.
66.
67.
68.
69.
70.  p.7.
71.
72.
73.
74.
75.
76.
77.
78.
79.
80.
81.