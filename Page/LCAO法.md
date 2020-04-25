> この記事は[LCAO法](https://ja.wikipedia.org/wiki/LCAO法)から翻訳されています。


**LCAO法**（LCAOほう、）あるいは**原子軌道による線形結合法**とは、[原子軌道](../Page/原子軌道.md "wikilink")の[線形結合](https://ja.wikipedia.org/wiki/線形結合 "wikilink")（[量子力学](https://ja.wikipedia.org/wiki/量子力学 "wikilink")的[重ね合わせ](../Page/重ね合わせ.md "wikilink")）によって[電子](https://ja.wikipedia.org/wiki/電子 "wikilink")の[波動関数](../Page/波動関数.md "wikilink")を記述し、その電子状態（[分子軌道](../Page/分子軌道.md "wikilink")）を求める計算手法のことである\[1\]。

この場合、原子軌道が[基底関数](https://ja.wikipedia.org/wiki/基底関数 "wikilink")となっている。原子軌道はその原子に強く束縛された局在された[軌道であり](../Page/軌道_\(力学\).md "wikilink")、隣合う軌道間の重なりは通常小さい。この意味で、LCAO法は[タイトバインディング法](https://ja.wikipedia.org/wiki/タイトバインディング法 "wikilink")とほぼ等価として扱われることがある。比較的扱い易い計算手法であるが、原子軌道同士の重なりの部分（[重なり積分](https://ja.wikipedia.org/wiki/重なり積分 "wikilink")）の扱いが計算の負担となることがある。

LCAO法は、[ジョン・レナード＝ジョーンズ](https://ja.wikipedia.org/wiki/ジョン・レナード＝ジョーンズ "wikilink")によって周期表の[第2周期の](../Page/第2周期元素.md "wikilink")2原子分子における結合の描写と共に1929年に導入されたが、それより前に[ライナス・ポーリング](../Page/ライナス・ポーリング.md "wikilink")によって[H<sub>2</sub><sup>+</sup>に対して用いられていた](https://ja.wikipedia.org/wiki/水素分子イオン "wikilink")\[2\]\[3\]。

数学的記述は以下の通りである。

最初の仮定は、分子軌道の数は線形展開に含まれる原子軌道の数に等しい、というものである。つまり、n個の原子軌道が組み合わさり、n個の分子軌道（*i* = 1からnと番号付けされる）が作られる。*i*番目の分子軌道の式（線形展開）は

  -
    \(\ \phi_i = c_{1i} \chi_1 + c_{2i} \chi_2 + c_{3i} \chi_3 + \cdots +c_{ni} \chi_n\)

あるいは

  -
    \(\ \phi_i = \sum_{r} c_{ri} \chi_r\)

となる。\(\ \phi_i\)はn個の原子軌道の和 \(\ \chi_r\)（それぞれの原子軌道には対応する係数\(\ c_{ri}\)がかかっている）として表わされる分子軌道である。係数は原子軌道の分子軌道に対する寄与の重み付けである。この展開の係数を得るためには[ハートリー＝フォック法が用いられる](https://ja.wikipedia.org/wiki/ハートリー-フォック方程式 "wikilink")。

分子軌道は[基底関数](https://ja.wikipedia.org/wiki/基底関数 "wikilink")の[線形結合](https://ja.wikipedia.org/wiki/線形結合 "wikilink")として表わされ、基底関数は分子の構成[原子](https://ja.wikipedia.org/wiki/原子 "wikilink")の[核を中心とした](../Page/原子核.md "wikilink")1[電子](https://ja.wikipedia.org/wiki/電子 "wikilink")関数である。用いられる原子軌道は（解析的に得られる）[水素様原子のもの](https://ja.wikipedia.org/wiki/水素原子におけるシュレーディンガー方程式の解 "wikilink")、すなわち[スレーター型軌道が典型的であるが](../Page/スレーター軌道.md "wikilink")、[ガウス関数のようなその他の選択肢もある](https://ja.wikipedia.org/wiki/ガウス軌道 "wikilink")。

系の全[エネルギー](https://ja.wikipedia.org/wiki/エネルギー "wikilink")を最小化することによって、線形結合の係数の妥当な組が決定される。この定量的手法は現在[ハートリー＝フォック法として知られている](https://ja.wikipedia.org/wiki/ハートリー-フォック方程式 "wikilink")。しかしながら、[計算化学](../Page/計算化学.md "wikilink")の発展から、LCAO法は波動関数の実際の最適化ではなく、より現代的な手法から得られた結果を予測し合理的に説明するのに非常に有用な定性的議論であるとされることが多い。この場合、分子軌道の形状とれらの個々のエネルギーは個別の原子（あるいは分子断片）の原子軌道のエネルギーと比較し、として知られるいくつかの方策を適用することによって近似的に推定される。この議論をより明確にするためにプロットされたグラフは「相関図」と呼ばれる。必要な原子軌道のエネルギーは計算あるいは実験的に[クープマンズの定理](../Page/クープマンズの定理.md "wikilink")から直接得ることができる。

LCAO法による定性的議論は、[分子の対称性と結合に関与する軌道を用いることによって行われる](https://ja.wikipedia.org/wiki/分子対称性 "wikilink")。この過程における最初の段階は、分子への[点群](../Page/点群.md "wikilink")の指定である。例えば水はC<sub>2v</sub>対称性を有する。次に、結合の可約表現が決定される。

[CharakterH2Oa.svg](https://ja.wikipedia.org/wiki/File:CharakterH2Oa.svg "fig:CharakterH2Oa.svg")

点群におけるそれぞれの操作が分子に対して行われる。変化しない結合の数がその操作の指標である。この可約表現は既約表現の和へと分解される。これらの既約表現は関与する軌道の対称性と対応する。

[分子軌道ダイアグラム](https://ja.wikipedia.org/wiki/分子軌道ダイアグラム "wikilink")によって単純な定性的LCAO取扱いを図示することができる。

[MO_Diagram.svg](https://ja.wikipedia.org/wiki/File:MO_Diagram.svg "fig:MO_Diagram.svg")

定量的理論としては[ヒュッケル法](../Page/ヒュッケル法.md "wikilink")や[拡張ヒュッケル法](https://ja.wikipedia.org/wiki/拡張ヒュッケル法 "wikilink")、がある。

## 脚注

## 関連項目

  - [分子軌道法](../Page/分子軌道法.md "wikilink")

  - [量子化学的手法](https://ja.wikipedia.org/wiki/量子化学的手法 "wikilink")

  - [原子軌道](../Page/原子軌道.md "wikilink")

  - [線形結合](https://ja.wikipedia.org/wiki/線形結合 "wikilink")

  - [タイトバインディング法](https://ja.wikipedia.org/wiki/タイトバインディング法 "wikilink")

  - [基底関数系 (化学)](https://ja.wikipedia.org/wiki/基底関数系_\(化学\) "wikilink")

  -
## 外部リンク

  - [LCAO @ chemistry.umeche.maine.edu](http://chemistry.umeche.maine.edu/Modeling/lcao.html)

[Category:計算物理学](https://ja.wikipedia.org/wiki/Category:計算物理学 "wikilink") [Category:量子化学](https://ja.wikipedia.org/wiki/Category:量子化学 "wikilink") [Category:電子軌道](https://ja.wikipedia.org/wiki/Category:電子軌道 "wikilink")

1.
2.
3.