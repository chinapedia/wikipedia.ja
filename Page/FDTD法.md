> この記事は[FDTD法](https://ja.wikipedia.org/wiki/FDTD法)から翻訳されています。


**FDTD法**（Finite-difference time-domain method; FDTD method）は、[数値計算の手法の](https://ja.wikipedia.org/wiki/数値解析 "wikilink")1つ。日本語訳として「時間領域差分法」「有限差分時間領域法」などの呼び方もあるが、もっぱらFDTD法と呼ばれる。

## 電磁気学における定式化

### Yeeアルゴリズム

[マクスウェルの方程式](../Page/マクスウェルの方程式.md "wikilink")を直接、空間・[時間領域](../Page/時間領域.md "wikilink")での差分方程式に展開して逐次計算をすることで、[電場](../Page/電場.md "wikilink")・[磁場](../Page/磁場.md "wikilink")の値を数値的に得る。ここで言うマクスウェルの方程式とは

\[\nabla \times \mathbf{E} = -\frac{\partial\mathbf{B}}{\partial t}\]・・・(1)

\[\nabla \times \mathbf{H}=\frac{\partial \mathbf{D}}{\partial t}+\mathbf{J}\]・・・(2)

の2式である（[ファラデーの電磁誘導の法則](../Page/ファラデーの電磁誘導の法則.md "wikilink")と[アンペールの法則](../Page/アンペールの法則.md "wikilink")）。ここに[電束密度](../Page/電束密度.md "wikilink")と[電場](../Page/電場.md "wikilink")、[磁束密度](../Page/磁束密度.md "wikilink")と[磁場](../Page/磁場.md "wikilink")の間の関係式

\[\mathbf{D}= \varepsilon\mathbf{E}\]・・・(3)

\[\mathbf{B}=\mu\mathbf{H}\]・・・(4)

と、[オームの法則](../Page/オームの法則.md "wikilink")

\[\mathbf{J}=\sigma\mathbf{E}\]・・・(5) を用いると式(1)、(2)は

\[\nabla \times \mathbf{E}=-\mu\frac{\partial \mathbf{H}}{\partial t}\]・・・(6)

\[\nabla \times \mathbf{H}=\varepsilon\frac{\partial \mathbf{E}}{\partial t}+\sigma\mathbf{E}\]・・・(7)

となる\[1\]。これをYee格子 [サムネイル](https://ja.wikipedia.org/wiki/ファイル:Yee_cell.png "wikilink") を用いて差分化する。

### 吸収境界条件

  -
    **FDTD法**を用いて開放領域の[電磁場解析](https://ja.wikipedia.org/wiki/電磁場解析 "wikilink")をする際、計算領域境界に到達した電磁波の反射を抑えるために境界あるいは境界付近に導入される条件
      - 吸収境界で反射がないという近似的な微分方程式から導かれたもの（例：[Murの吸収境界条件](https://ja.wikipedia.org/wiki/Murの吸収境界条件 "wikilink")）
      - 境界に仮想的な媒質を置いて入射波を減衰させようという発想から生まれたもの（例：[BerengerのPML吸収境界条件](https://ja.wikipedia.org/wiki/BerengerのPML吸収境界条件 "wikilink")）
    の2種類がある。

## 脚注

## 関連項目

  - [Yee格子](https://ja.wikipedia.org/wiki/Yee格子 "wikilink")
  - [散乱界表示](https://ja.wikipedia.org/wiki/散乱界表示 "wikilink")
  - [遠方界](https://ja.wikipedia.org/wiki/遠方界 "wikilink")
  - [サブセル法](https://ja.wikipedia.org/wiki/サブセル法 "wikilink")
  - [サブグリッド法](https://ja.wikipedia.org/wiki/サブグリッド法 "wikilink")

[Category:計算物理学](https://ja.wikipedia.org/wiki/Category:計算物理学 "wikilink") [Category:計算電磁気学](https://ja.wikipedia.org/wiki/Category:計算電磁気学 "wikilink") [Category:アルゴリズム](https://ja.wikipedia.org/wiki/Category:アルゴリズム "wikilink")

1.  ただし、ここでは[誘電率](../Page/誘電率.md "wikilink")・[透磁率](https://ja.wikipedia.org/wiki/透磁率 "wikilink")ともに方向に依らず定数とする。つまり[等方性媒質](https://ja.wikipedia.org/wiki/等方性媒質 "wikilink")ということである。[異方性媒質](https://ja.wikipedia.org/wiki/異方性媒質 "wikilink")なら誘電率・透磁率がテンソルとなる。