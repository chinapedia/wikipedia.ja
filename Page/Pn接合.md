> この記事は[Pn接合](https://ja.wikipedia.org/wiki/Pn接合)から翻訳されています。


**pn接合**（pnせつごう、pn junction）とは、[半導体](../Page/半導体.md "wikilink")中で[P型半導体の領域と](https://ja.wikipedia.org/wiki/p型 "wikilink")[N型半導体の領域が接している部分を言う](https://ja.wikipedia.org/wiki/n型 "wikilink")。[整流](https://ja.wikipedia.org/wiki/整流 "wikilink")性、[エレクトロルミネセンス](https://ja.wikipedia.org/wiki/エレクトロルミネセンス "wikilink")、[光起電力効果](../Page/光起電力効果.md "wikilink")などの現象を示すほか、接合部には[電子](https://ja.wikipedia.org/wiki/電子 "wikilink")や[正孔](../Page/正孔.md "wikilink")の不足する[空乏層](https://ja.wikipedia.org/wiki/空乏層 "wikilink")が発生する。これらの性質が[ダイオード](../Page/ダイオード.md "wikilink")や[トランジスタ](../Page/トランジスタ.md "wikilink")を始めとする各種の半導体素子で様々な形で応用されている。また[ショットキー接合](https://ja.wikipedia.org/wiki/ショットキー接合 "wikilink")の示す整流性も、pn接合と原理的に良く似る。

## 熱平衡状態（ゼロバイアス）

[thumb](https://ja.wikipedia.org/wiki/ファイル:PnJunction-J.PNG "wikilink") p型とn型の[半導体](../Page/半導体.md "wikilink")を接合した瞬間では、n型側の多数[キャリアである](https://ja.wikipedia.org/wiki/電荷担体 "wikilink")[伝導電子](https://ja.wikipedia.org/wiki/伝導電子 "wikilink")とp型側の多数キャリアである[正孔](../Page/正孔.md "wikilink")がそれぞれ[拡散](../Page/拡散.md "wikilink")することで[拡散電流](https://ja.wikipedia.org/wiki/拡散電流 "wikilink")が生じる。

電子と正孔が[再結合](https://ja.wikipedia.org/wiki/再結合 "wikilink")により消滅すると、接合部付近にキャリアの少ない領域（空乏層）が形成される。接合の両側で電子と正孔の密度は異なるため、拡散電流が流れる。

空乏層のn型側では、本来存在する伝導電子が不足する一方で正電荷をもつドナーイオンが固定されているため、正に帯電する。一方で空乏層のp型側では、本来存在する正孔が不足する一方で負電荷をもつアクセプターイオンが固定されているため、負に帯電する。その結果、空乏層は正に帯電した層と負に帯電した層が重なり合った[電気二重層](../Page/電気二重層.md "wikilink")を形成し、内蔵電場が生まれる。内蔵電場によって発生する[静電ポテンシャル](https://ja.wikipedia.org/wiki/静電ポテンシャル "wikilink")の差\(V_{bi}\)を**拡散電位**または**内蔵電位**(built-in potential)と言う。内部電場は電子と正孔をそれぞれn型、p型領域へ引き戻そうとする。内蔵電場の発生によって[ドリフト電流](https://ja.wikipedia.org/wiki/ドリフト電流 "wikilink")も発生する。

熱平衡状態では正味の電流はゼロであり、拡散電流とドリフト電流は釣り合っている。よってpn接合全体の[フェルミ準位](https://ja.wikipedia.org/wiki/フェルミ準位 "wikilink")（[化学ポテンシャル](../Page/化学ポテンシャル.md "wikilink")）は一定となる。

### 拡散電位

[非縮退のp型半導体とn型半導体を階段型に接合した理想的な場合を考える](https://ja.wikipedia.org/wiki/非縮退半導体 "wikilink")。p型半導体中のアクセプター濃度を\(N_{p,A}\)、ドナー濃度を\(N_{p,D}\)とすると、\(N_{p,D}<N_{p,A}\)である。同様にn型半導体では\(N_{n,A}<N_{n,D}\)である。全ての不純物がイオン化していると仮定すると、p型半導体の正孔濃度\(p_p\)とn型半導体の電子濃度\(n_n\)は、

\[p_p=N'_A=N_{p,A}-N_{p,D}\]

\[n_n=N'_D=N_{n,D}-N_{n,A}\] となる。この2つを接合したときの拡散電位はp型とn型それぞれの仕事関数の差であり、次のように与えられる\[1\]。

\[\begin{align}
V_{bi}
&=\frac{1}{q}\left[E_g-(E_C-E_F)_{n-type}-(E_F-E_V)_{p-type}\right] \\
&=\frac{1}{q}\left[kT \ln \left(\frac{N_VN_C}{n_i^2}\right)-kT\ln \left(\frac{N_C}{N'_D}\right)-kT\ln \left(\frac{N_V}{N'_A}\right)\right] \\
&=\frac{kT}{q} \ln \left(\frac{N'_DN'_A}{n_i^2}\right) \\
\end{align}\] ここで\(E_g\)は[バンドギャップ](../Page/バンドギャップ.md "wikilink")、\(E_C\)は伝導帯の下端のエネルギー、\(E_V\)は価電子帯の上端のエネルギー、\(N_C\)と\(N_V\)は[有効状態密度](https://ja.wikipedia.org/wiki/有効状態密度 "wikilink")、\(n_i\)は[真性キャリア密度](https://ja.wikipedia.org/wiki/真性キャリア密度 "wikilink")である。

例えば[シリコン](https://ja.wikipedia.org/wiki/シリコン "wikilink")（バンドギャップ1.17eV）のpn接合の場合、内蔵電位は0.6～0.7V程度となる。

### 空乏層の幅

[Pn-junction-equilibrium-graphs.png](https://ja.wikipedia.org/wiki/File:Pn-junction-equilibrium-graphs.png "fig:Pn-junction-equilibrium-graphs.png") p型側の空乏層の幅を\(x_p\)、n型側の空乏層の幅を\(x_n\)とする。また空乏層では価電子帯の電子と伝導帯の正孔は存在しないと仮定する。つまり電荷密度\(Q(x)\)は、p型側ではアクセプターイオンの負電荷、n型側ではドナーイオンの正電荷によるものだけとする。空乏層の外側は電気的に中性である。

\[Q(x)=0\quad\quad(x<-x_p)\]

\[Q(x)=-qN'_A\quad(-x_p\le x\le0)\]

\[Q(x)=qN'_D\quad(0< x\le x_n)\]

\[Q(x)=0\quad\quad(x_n<x)\] 半導体の[誘電率](../Page/誘電率.md "wikilink")を\(\epsilon_s\)とすると、この電荷密度が作る[電場](../Page/電場.md "wikilink")は\(\frac{dE}{dx}=\frac{Q}{\epsilon_s}\)を満たす。空乏層の端（\(x=-x_p,x_n\)）では\(E=0\)であるため、

\[E(x)=-\frac{qN'_A}{\epsilon_s}(x_p+x)\quad(-x_p\le x\le0)\]

\[E(x)=-\frac{qN'_D}{\epsilon_s}(x_n-x)\quad(0< x\le x_n)\] 内蔵電位\(V_{bi}\)は、p型側の端\(x=-x_p\)とn型側の端\(x=x_n\)との[電位差](https://ja.wikipedia.org/wiki/電位差 "wikilink")である。

\[V_{bi}=\frac{qN'_A}{2\epsilon_s}x_p^2+\frac{qN'_D}{2\epsilon_s}x_n^2\] これと電荷中性条件\(N_Ax_p=N_Dx_n\)より、空乏層の幅\(W\)は次のように得られる\[2\]。

\[x_p=\sqrt{\frac{2\epsilon_s}{q}\left(\frac{N'_A}{N'_D(N'_A+N'_D)}\right)V_{bi}}\]

\[x_n=\sqrt{\frac{2\epsilon_s}{q}\left(\frac{N'_D}{N'_A(N'_A+N'_D)}\right)V_{bi}}\]

\[W=x_p+x_n=\sqrt{\frac{2\epsilon_s}{q}\left(\frac{N'_A+N'_D}{N'_AN'_D}\right)V_{bi}}\]

## pn接合の電流-電圧特性

[thumb](https://ja.wikipedia.org/wiki/ファイル:PnJunction-Diode-ForwardBias.PNG "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:PnJunction-Diode-ReverseBias.PNG "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:P-n_junction_characteristics.svg "wikilink") pn接合は一方向にのみ電流を流しやすい性質があり、これを**整流性**という。pn接合[ダイオード](../Page/ダイオード.md "wikilink")や[トランジスタ](../Page/トランジスタ.md "wikilink")など各種の半導体素子で利用される。

### 順方向バイアス時

pn接合に**順方向バイアス**を印加した場合を考える。順方向バイアスとは、p型側に正電圧を印加すること、つまり内蔵電位を小さくする方向に電圧をかけることと定義する。するとポテンシャルの釣り合いが崩れて[拡散電流](https://ja.wikipedia.org/wiki/拡散電流 "wikilink")が増加し、電流が流れる。

電極からn型、p型それぞれの領域に注入された[電子](https://ja.wikipedia.org/wiki/電子 "wikilink")と[正孔](../Page/正孔.md "wikilink")（[多数キャリア](https://ja.wikipedia.org/wiki/多数キャリア "wikilink")）は接合領域にて再結合する。通常のシリコン・ダイオードの場合、接合面を通過してさらに10〜100μm程度の領域まで（[少数キャリア](https://ja.wikipedia.org/wiki/少数キャリア "wikilink")として）注入される。

キャリアが[禁制帯](https://ja.wikipedia.org/wiki/禁制帯 "wikilink")を超えて再結合する時、再結合エネルギーを熱や光として放出する。この現象を利用したのが[発光ダイオード](../Page/発光ダイオード.md "wikilink")や[半導体レーザ](https://ja.wikipedia.org/wiki/半導体レーザ "wikilink")である。逆にいえば順方向電流を流すにはこの分の電圧（禁制帯幅が2[電子ボルト](../Page/電子ボルト.md "wikilink")(eV)なら、最低2V）を外部から与えてやる必要があることになる。ダイオードを順方向バイアスで用いる場合は、ここから[不純物準位](https://ja.wikipedia.org/wiki/不純物準位 "wikilink")等を介した遷移による電圧の低下分を差し引き、また電極でのショットキー障壁による電位差や素子各部での抵抗損失を加えた電圧を与える必要があり、これを**順方向電圧降下**（または**順方向降下電圧**）と呼ぶ。順方向電圧降下は[シリコン](https://ja.wikipedia.org/wiki/シリコン "wikilink")ダイオードの場合は0.6〜0.7V程度、[ショットキーバリアダイオード](../Page/ショットキーバリアダイオード.md "wikilink")の場合で0.2Vである。[発光ダイオード](../Page/発光ダイオード.md "wikilink")では発光波長や出力によって異なり、1～5V程度になる。

### 逆方向バイアス時

pn接合に**逆方向バイアス**を印加した場合を考える。逆方向バイアスとは、n型側に正電圧を印加すること、つまりポテンシャル障壁を大きくする方向に電圧をかけることと定義する。すると、n型、p型領域それぞれに於いて、[多数キャリア](https://ja.wikipedia.org/wiki/多数キャリア "wikilink")（電子と正孔）が[少数キャリア](https://ja.wikipedia.org/wiki/少数キャリア "wikilink")（正孔と電子）の注入によって減少する。これによって空乏層幅が増大すると共に内蔵電位が大きくなり、内蔵電位の増加分が外部からの印加電圧と釣り合った所で平衡に達し、電流が止まる。 実際の素子では、逆バイアス状態でもドリフト電流によってわずかに逆方向電流が流れる。さらに逆方向バイアスを増してゆくと、[ツエナー降伏](https://ja.wikipedia.org/wiki/ツエナー降伏 "wikilink")や[なだれ降伏](https://ja.wikipedia.org/wiki/なだれ降伏 "wikilink")を起こして急激に電流が流れるようになる。この時の電圧を（逆方向）[降伏電圧](https://ja.wikipedia.org/wiki/降伏電圧 "wikilink")と言う。

### 電流-電圧特性

空乏層を流れる電流密度\(J\)は、電子による部分\(J_n\)と正孔による部分\(J_p\)に分けることができる。空乏層での[キャリア生成と再結合](https://ja.wikipedia.org/wiki/キャリア生成と再結合 "wikilink")を無視できると仮定すると、全電流密度\(J\)は空乏層の両端（\(x=x_n,x_p\)）での電子と正孔による拡散電流の和となる。

\[J=J_n(x_p)+J_p(x_n)\] ここでn型領域とp型領域の少数キャリアによる電流は[拡散電流](https://ja.wikipedia.org/wiki/拡散電流 "wikilink")であるとする。また少数キャリア濃度\(n_p, p_n\)は、定数である熱平衡キャリア部分\(n_{p0}, p_{n0}\)と位置と時間に依存する過剰キャリア部分\(\Delta n_p,\Delta p_n\)に分解できる。

\[J_n(x_p)
=qD_n \left.\frac{\partial n_p}{\partial x}\right|_{x=x_p}
=qD_n \left.\frac{\partial \Delta n_p}{\partial x}\right|_{x=x_p}\]

\[J_p(x_n)
=-qD_p \left.\frac{\partial p_n}{\partial x}\right|_{x=x_n}
=-qD_p \left.\frac{\partial \Delta p_n}{\partial x}\right|_{x=x_n}\]

\(\Delta n_p\)と\(\Delta p_n\)を求めるために[連続の式](https://ja.wikipedia.org/wiki/連続の式 "wikilink")を考える。電子と正孔の[生成速度を](https://ja.wikipedia.org/wiki/キャリア生成と再結合 "wikilink")\(G_n,G_p\)とし、また電子と正孔の[再結合速度は電子と正孔の寿命を](https://ja.wikipedia.org/wiki/キャリア生成と再結合 "wikilink")\(\tau_n,\tau_p\)として\(R_n=\Delta n/\tau_n\)、\(R_p=\Delta p/\tau_p\)と書けるため、連続の式は次のように書ける。

\[\frac{\partial n}{\partial t}
=\frac{\partial\Delta n}{\partial t}
=\frac{1}{q}\left(\frac{\partial J_n}{\partial x}\right)+G_n-\frac{\Delta n}{\tau_n}\]

\[\frac{\partial p}{\partial t}
=\frac{\partial\Delta p}{\partial t}
=-\frac{1}{q}\left(\frac{\partial J_p}{\partial x}\right)+G_p-\frac{\Delta p}{\tau_p}\] 熱平衡では時間変化はゼロである。また電子と生成の生成を無視すると、

\[0=D_n\frac{\partial^2 \Delta n(x.t)}{\partial x^2}-\frac{\Delta n}{\tau_n}\]

\[0=D_p\frac{\partial^2 \Delta p(x.t)}{\partial x^2}-\frac{\Delta p}{\tau_p}\] 境界条件として空乏層から十分に離れたp型側、n型側では\(\Delta n_p=\Delta p_n=0\)、空乏層の両端\(x=x_p,x_n\)では\(\Delta n_p=n_p-n_{p0}=e^{qV/kT}\)、\(\Delta p_n=p_n-p_{n0}=e^{qV/kT}\)として解くと、

\[\Delta n_p=n_{p0}\left(e^{qV/kT}-1\right)e^{-(x-x_n)/L_n}\]

\[\Delta p_n=p_{n0}\left(e^{qV/kT}-1\right)e^{-(x-x_n)/L_p}\] ここで\(L_n=\sqrt{D_n\tau_n}\)、\(L_p=\sqrt{D_p\tau_p}\)は[拡散長](https://ja.wikipedia.org/wiki/拡散長 "wikilink")である。これらを代入すると、全電流密度は次のように与えられる。

\[J=J_n+J_p=q\left(\frac{D_nn_{p0}}{L_n}+\frac{D_pp_{n0}}{L_p}\right)\left(e^{qV/kT}-1\right)\]

降伏していない領域におけるpn接合ダイオードの電流と電圧の関係は、J<sub>o</sub> を[逆方向飽和電流](https://ja.wikipedia.org/wiki/逆方向飽和電流 "wikilink")、qを[電気素量](../Page/電気素量.md "wikilink")、Vを[電圧](../Page/電圧.md "wikilink")、nを[理想ダイオード因子](https://ja.wikipedia.org/wiki/理想ダイオード因子 "wikilink")、kを[ボルツマン定数](../Page/ボルツマン定数.md "wikilink")、Tを[温度](../Page/温度.md "wikilink")として

  -
    \(J = J_o \Big\{ \exp \Big( \frac{qV}{nkT} \Big) - 1 \Big\}\)

のように表される。ここで n=1 としたものがpn接合の理想I-V特性である。

## pn接合と発光・受光

順バイアス時に於いて、pn接合領域で[キャリアの再結合が発生する](https://ja.wikipedia.org/wiki/半導体#キャリア "wikilink")。この時、[禁制帯幅](https://ja.wikipedia.org/wiki/禁制帯幅 "wikilink")が光子のエネルギーより大きければ、再結合に伴って光が放出される場合がある（発光再結合または[エレクトロルミネセンス](https://ja.wikipedia.org/wiki/エレクトロルミネセンス "wikilink")）。これを応用した素子が[発光ダイオード](../Page/発光ダイオード.md "wikilink")や[半導体レーザ](https://ja.wikipedia.org/wiki/半導体レーザ "wikilink")である。

逆にpn接合領域に禁制帯幅よりも大きなエネルギーの光子などが入射すると、[価電子帯](https://ja.wikipedia.org/wiki/価電子帯 "wikilink")から電子が励起されて[伝導電子](https://ja.wikipedia.org/wiki/伝導電子 "wikilink")となり、内蔵電場に引かれてドリフト電流を増大させる、[光起電力効果](../Page/光起電力効果.md "wikilink")（[内部光電効果](https://ja.wikipedia.org/wiki/内部光電効果 "wikilink")）が発生する。これを応用した素子が[フォトダイオード](../Page/フォトダイオード.md "wikilink")や[フォトトランジスタ](https://ja.wikipedia.org/wiki/フォトトランジスタ "wikilink")、[太陽電池](../Page/太陽電池.md "wikilink")などである。

[伝導帯](https://ja.wikipedia.org/wiki/伝導帯 "wikilink")の底と[価電子帯](https://ja.wikipedia.org/wiki/価電子帯 "wikilink")の頂上の間を電子が一気に遷移する際に吸収・放出する光の波長との関係は、[光子](../Page/光子.md "wikilink")のエネルギーをE、[プランク定数](../Page/プランク定数.md "wikilink")h、[振動数](../Page/振動数.md "wikilink")ν、[光速度](https://ja.wikipedia.org/wiki/光速度 "wikilink")c、[波長](../Page/波長.md "wikilink")λ、[電荷素量](https://ja.wikipedia.org/wiki/電荷素量 "wikilink")e、[禁制帯幅](https://ja.wikipedia.org/wiki/禁制帯幅 "wikilink")をE<sub>g</sub>として

  -
    \(E = h\nu = h\frac{c}{\lambda} = E_g\)

の関係がある。 たとえば[キャリアが](https://ja.wikipedia.org/wiki/半導体#キャリア "wikilink")2.200eV（[電子ボルト](../Page/電子ボルト.md "wikilink")）のエネルギーを一気に越えて発光再結合した場合、おおよその発光波長は

  -
    \(\lambda = \frac{hc}{E_g} = \frac{6.626 \times 10^{-34} \times 3.000 \times 10^8}{2.200 \times 1.602 \times 10^{-19}} = 5.64 \times 10^{-7} \mbox{m} = 564 \mbox{nm}\)

の黄緑色と計算できる。 実際には、[禁制帯](https://ja.wikipedia.org/wiki/禁制帯 "wikilink")から離れた準位からの遷移や、禁制帯中の[不純物準位](https://ja.wikipedia.org/wiki/不純物準位 "wikilink")などを介した遷移も起こるため、発光スペクトルは多少の幅を持つ。これを[誘導放出](../Page/誘導放出.md "wikilink")によって1つの波長に揃えるのが[半導体レーザ](https://ja.wikipedia.org/wiki/半導体レーザ "wikilink")である。

なお一般に、[発光ダイオード](../Page/発光ダイオード.md "wikilink")などに光を当てても、ごく僅かだが[光起電力](https://ja.wikipedia.org/wiki/光起電力 "wikilink")が発生する。逆に、一般的な[フォトダイオード](../Page/フォトダイオード.md "wikilink")や[太陽電池](../Page/太陽電池.md "wikilink")に電圧を印加しても、禁制帯幅が小さいために赤外域での発光になったり、熱になって殆ど発光しない場合が多い（素子を破壊する可能性が高いので、安易に試すのは避けるべきである）。

## 主な応用

  - 整流性：各種[ダイオード](../Page/ダイオード.md "wikilink")、[トランジスタ](../Page/トランジスタ.md "wikilink")
  - [空乏層](https://ja.wikipedia.org/wiki/空乏層 "wikilink")：[電界効果型トランジスタ](https://ja.wikipedia.org/wiki/電界効果型トランジスタ "wikilink")、[可変容量ダイオード](https://ja.wikipedia.org/wiki/可変容量ダイオード "wikilink")
  - 発光（[エレクトロルミネセンス](https://ja.wikipedia.org/wiki/エレクトロルミネセンス "wikilink")、発光再結合）：[発光ダイオード](../Page/発光ダイオード.md "wikilink")、[半導体レーザ](https://ja.wikipedia.org/wiki/半導体レーザ "wikilink")
  - 受光（[内部光電効果](https://ja.wikipedia.org/wiki/内部光電効果 "wikilink")、[光起電力効果](../Page/光起電力効果.md "wikilink")）：[フォトダイオード](../Page/フォトダイオード.md "wikilink")、[フォトトランジスタ](https://ja.wikipedia.org/wiki/フォトトランジスタ "wikilink")、[太陽電池](../Page/太陽電池.md "wikilink")

## 脚注

<references />

[Category:半導体接合](https://ja.wikipedia.org/wiki/Category:半導体接合 "wikilink") [Category:半導体構造](https://ja.wikipedia.org/wiki/Category:半導体構造 "wikilink")

1.
2.