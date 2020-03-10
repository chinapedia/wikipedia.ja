> この記事は[X](https://ja.wikipedia.org/wiki/X)から翻訳されています。


[Xps-spektrum.jpg](https://ja.wikipedia.org/wiki/File:Xps-spektrum.jpg "fig:Xps-spektrum.jpg")（磁鉄鉱）のX線光電子分光スペクトル（サーベイスキャンモード）。横軸は照射したX線を基準としたときの[光電子](https://ja.wikipedia.org/wiki/光電子 "wikilink")のエネルギー、縦軸は観測された光電子の個数である。\]\] **X線光電子分光**（エックスせんこうでんしぶんこう）は、[光電子分光](../Page/光電子分光.md "wikilink")の1種である。略称は**XPS** (X-ray Photoelectron Spectroscopy) または **ESCA** (Electron Spectroscopy for Chemical Analysis, エスカ)。サンプル表面に[X線](../Page/X線.md "wikilink")を照射し、生じる光電子のエネルギーを測定することで、サンプルの構成元素とその[電子](https://ja.wikipedia.org/wiki/電子 "wikilink")状態を分析することができる。他にもPES、PS等とも呼ばれる。

## 原理

物質に数keV程度の[軟X線](https://ja.wikipedia.org/wiki/軟X線 "wikilink")を照射すると、[原子軌道](https://ja.wikipedia.org/wiki/原子軌道 "wikilink")の電子が光エネルギーを吸収し、[光電子](https://ja.wikipedia.org/wiki/光電子 "wikilink")として外にたたき出される。この光電子は \(E = h \nu - E_B-\phi\)（\(E_B\) は電子の結合エネルギー、 \(\phi\)は分光器の[仕事関数](../Page/仕事関数.md "wikilink")）にしたがったエネルギー値をもつため、X線のエネルギーが一定であれば（すなわち単一波長であれば）、\(E_B\) を求めることができる。

電子の結合エネルギーは元素によって固有なので、元素分析ができる。また結合エネルギーの微妙なシフトは、その元素の化学状態や電子状態（酸化数など）を反映しているため、化学状態を調べることができる。

ターゲットが原子番号の大きな元素の場合、[スピン軌道分裂](https://ja.wikipedia.org/wiki/スピン軌道分裂 "wikilink")によって2つのピークが出現する。

### 定量

光電子の強度（個数） \(I\)は以下の式で表される。

\[I=F(E) X_0 N \tau(E) \sigma \cos\theta\] ここで \(F(E)\)は装置によって異なる装置透過関数、\(X_0\)は入射X線強度、\(N\)は原子密度、\(\tau(E)\)は非弾性平均自由行程と相関する減衰長さ、\(\sigma\)は光イオン化断面積、\(\theta\)は光電子取り出し角度。

したがって装置と測定条件が一定であれば、これらのパラメータを感度係数に含めることで定量ができる。i成分の濃度を\(N_i\)、光電子強度を\(I_i\)、相対感度係数を\(S_i\)とすると

\[\frac{N_i}{\sum{N_i}} = \frac{I_i / S_i}{\sum{I_i / S_i}}\] と表せる。

### 化学シフト

結合エネルギーのずれは**化学シフト**と呼ばれる。[核磁気共鳴](https://ja.wikipedia.org/wiki/核磁気共鳴 "wikilink")における化学シフトと同様に、周囲の原子との相互作用に由来する。 単体元素Aを基準にしたときの化合物Bの化学シフト\(\Delta E_A^B\)は次のように表せる。

\[\Delta E_A^B = K(q_A - q_B) + (V_A - V_B)\]

\[K q_A = q_A / r_{A,V}\]

\[V_A =\sum{q_A / R}\] ここで\(K\)はカップリング定数で内殻電子と価電子の2電子積分、\(q\)は価電子の有効電荷、\(V\)は[マーデルングポテンシャル](https://ja.wikipedia.org/wiki/マーデルングポテンシャル "wikilink")(イオン結晶中の各格子点の静電ポテンシャルを表す)、\(r\)は価電子殻の平均軌道半径である。この式の第1項目は内殻電子と価電子との電子-電子相互作用の差に相当する。

## 特徴

[hires.jpg](https://ja.wikipedia.org/wiki/File:hires.jpg "fig:hires.jpg")

**利点**

  - ほぼあらゆる元素の種類、およびその電子状態がわかる（例えば、Fe(II) とFe(III) が区別できる）。結果にはある程度（有効数字で一桁ほどではあるが）の定量性がある。
  - 物質のごく表面（数[ナノメートル](../Page/ナノメートル.md "wikilink"))の元素分布がわかる。また、[アルゴン](../Page/アルゴン.md "wikilink")[エッチング](../Page/エッチング.md "wikilink")を適宜行うことで深さ方向の元素分布を知ることができる。
  - 導体、絶縁体、無機物、有機物のいずれも測定可能。

**欠点**

  - [水素](https://ja.wikipedia.org/wiki/水素 "wikilink")と[ヘリウム](https://ja.wikipedia.org/wiki/ヘリウム "wikilink")は測定できない。
  - 高[真空](../Page/真空.md "wikilink")中で固体として安定なものでないと測定できない。
  - [絶縁体](../Page/絶縁体.md "wikilink")は測定中に[チャージアップ](https://ja.wikipedia.org/wiki/チャージアップ "wikilink")が起こるので再現性が悪い。
  - X線によって試料がダメージを受けるため、正確に状態を反映しないことがある。
  - 炭素化合物の定量は難しい（装置内を高真空に保つための[ポンプ](../Page/ポンプ.md "wikilink")由来のオイルミストや試料に付着した一般的な汚れ（高級脂肪酸などの炭化水素系物質）の存在による）。

## 装置

[Xps-analysator.jpg](https://ja.wikipedia.org/wiki/File:Xps-analysator.jpg "fig:Xps-analysator.jpg")

### X線源

一般的な実験設備ではX線管から発せられる[MgKα線](https://ja.wikipedia.org/wiki/特性X線 "wikilink")(1253.6eV) や[AlKα線](https://ja.wikipedia.org/wiki/特性X線 "wikilink")(1486.6eV)などの[軟X線を照射する](../Page/X線.md "wikilink")（軟X線は表面感度が良い）。但し、老朽化したX線源を用いると[Mgや](https://ja.wikipedia.org/wiki/マグネシウム "wikilink")[Alが酸化物になっており](../Page/アルミニウム.md "wikilink")、[酸素](../Page/酸素.md "wikilink")の特性X線も同時に発生することがあるため注意が必要。X線の取り出し窓にはアルミニウム薄膜が用いられる。電子の脱出深さが一定であることから、試料表面と電子レンズとの角度を15°程度にすることによりさらに表面感度を上げることができる（バルク由来のバックグラウンドが減る）。高分解能が要求される場合は、[シンクロトロン放射光](https://ja.wikipedia.org/wiki/シンクロトロン放射光 "wikilink")を用いる。

単色化されたX線を光源として用いると、化学状態を詳細に解析できる。単色化X線源を用いると光電子スペクトルがシャープになり、X線源のサテライト線やKβ線も除去されるため、S/B比が良くなる。単色化X線源では、[ローランド円](https://ja.wikipedia.org/wiki/ローランド円 "wikilink")上にX線源（Alなど）と分光結晶を配置させる。

### 真空ポンプ

XPSでは試料の表面汚染を防ぐため、10^-7Pa以下の[超高真空](https://ja.wikipedia.org/wiki/超高真空 "wikilink")が必要となる。試料導入部では[ターボ分子ポンプ](../Page/ターボ分子ポンプ.md "wikilink")と[ロータリーポンプ](../Page/ロータリーポンプ.md "wikilink")を組み合わせる。測定部ではオイルを使わない[イオンポンプ](../Page/イオンポンプ.md "wikilink")とチタン[サブリメーションポンプ](https://ja.wikipedia.org/wiki/サブリメーションポンプ "wikilink")などを組み合わせる。他にも[拡散ポンプ](../Page/拡散ポンプ.md "wikilink")や[クライオポンプ](https://ja.wikipedia.org/wiki/クライオポンプ "wikilink")も使われる。

### エネルギー分析器

XPSでは静電型エネルギー分析器が用いられる。電場により光電子の飛行軌道を偏向させ、電場強度と偏向量の関係から光電子の運動エネルギーを測定する。

同心半球型アナライザー(concentric hemispherical analyzer, CHA)がエネルギー分解能が高いため一般的に用いられている。CHAの手前には入射レンズが付いており、CHAの入口スリットへ光電子を集光すること、エネルギー分解能の調整などが行われる。またCHAの他にも同筒鏡型のエネルギー分析器も用いられることがある。

### 検出器

検出器には、電子倍増管（[チャンネルトロン](https://ja.wikipedia.org/wiki/チャンネルトロン "wikilink")、マルチチャンネルトロン、[マイクロチャンネルプレート](https://ja.wikipedia.org/wiki/マイクロチャンネルプレート "wikilink")）が用いられる。

## 測定方法

### 測定モード

  - ワイドスキャン（サーベイスキャン）モード
    表面元素の定性分析を行うためのモードで、0 - 1500 eV程度の幅広いエネルギー範囲を、数分間でスキャンする。
  - ナロースキャンモード
    表面元素の定量と化学状態や電子状態を分析するためのモード。サーベイスキャンで得られた元素ピークについて、高エネルギー分解能で測定する。
  - 深さ分析モード
    固体表面を、[アルゴン](../Page/アルゴン.md "wikilink")や[キセノン](https://ja.wikipedia.org/wiki/キセノン "wikilink")などの希ガスイオンで[スパッタリング](../Page/スパッタリング.md "wikilink")しながら元素分析や状態分析を行うモード。
    数nm程度の深さ分析を行うときは、試料と検出器がなす角度（光電子取り込み角）を変化させることで測定深さを変化させることができる。
  - マッピングモード
    試料を移動させながら分析したり、イメージングプレートを使用することで、一次元の線分析や二次元の面分析を行うモード。

### 補正

分析するに当たり、仕事関数・チャージアップの補正を行う。上述の欠点で触れたオイルミストや汚れ由来のC1sピークを逆に利用して補正を行うなどする。[シクロヘキサン](../Page/シクロヘキサン.md "wikilink")のC1sは285.2eVであり、これをオイル・汚れの[炭化水素](../Page/炭化水素.md "wikilink")鎖のC1sとして、スペクトル中のC1sピークを285.2eVに合致するように調整することにより補正を行う。

## 参考

  - *Annotated Handbooks of Monochromatic XPS Spectra, PDF of Volumes 1 and 2*, B.V.Crist, published by XPS International LLC, 2005, Mountain View, CA, USA
  - *Handbooks of Monochromatic XPS Spectra, Volumes 1-5*, B.V.Crist, published by XPS International LLC, 2004, Mountain View, CA, USA
  - *Surface Analysis by Auger and X-ray Photoelectron Spectroscopy*, ed. J.T.Grant and D.Briggs, published by IM Publications, 2003, Chichester, UK
  - *Practical Surface Analysis by Auger and X-ray Photoelectron Spectroscopy*, 2nd edition, ed. M.P.Seah and D.Briggs, published by Wiley & Sons, 1990, Chichester, UK
  - *Practical Surface Analysis by Auger and X-ray Photoelectron Spectroscopy*, ed. M.P.Seah and D.Briggs, published by Wiley & Sons, 1983, Chichester, UK ISBN 0-471-26279-X
  - *Surface Chemical Analysis -- Vocabulary*, ISO 18115 : 2001, [International Organisation for Standardisation](https://ja.wikipedia.org/wiki/International_Organisation_for_Standardisation "wikilink") (ISO), TC/201, Switzerland, [1](http://www.iso.ch)
  - *Handbook of X-ray Photoelectron Spectroscopy*, J.F.Moulder, W.F.Stickle, P.E.Sobol, and K.D.Bomben, published by Perkin-Elmer Corp., 1992, Eden Prairie, MN, USA
  - *Handbook of X-ray Photoelectron Spectroscopy*, C.D.Wagner, W.M.Riggs, L.E.Davis, J.F.Moulder, and G.E.Mullenberg, published by Perkin-Elmer Corp., 1979, Eden Prairie, MN, USA

## 関連

  - [光電子分光](../Page/光電子分光.md "wikilink")
  - [紫外光電子分光](https://ja.wikipedia.org/wiki/紫外光電子分光 "wikilink")

[Category:分析化学](https://ja.wikipedia.org/wiki/Category:分析化学 "wikilink") [Category:分光学](https://ja.wikipedia.org/wiki/Category:分光学 "wikilink")