> この記事は[PSTricks](https://ja.wikipedia.org/wiki/PSTricks)から翻訳されています。


**PSTricks** は、[PostScript](../Page/PostScript.md "wikilink") で描いた図形を直接 [](../Page/TeX.md "wikilink") や [](../Page/LaTeX.md "wikilink") のコード内に取り込むためのマクロ群である。Timothy Van Zandt が開発し、最近では Denis Girou、Sebastian Rahtz、Herbert Voss が保守している。

## 使用例

[thumb](https://ja.wikipedia.org/wiki/ファイル:PSTricksSimple.svg "wikilink") PSTricks には[グラフィックスを作るための各種コマンドが用意されている](../Page/コンピュータグラフィックス.md "wikilink")。以下の例のように、PSTricks における座標は常に丸括弧で囲まれて書かれている。

`\begin{pspicture}(0,0)(6,6)`
` %\psgrid[gridcolor=lightgray,gridlabels=0pt]`
`  \psline[linecolor=red](1,1)(5,1)(1,4)(1,1)`
`  \pscurve[linecolor=green,linewidth=2pt,%`
`    showpoints=true](5,5)(3,2)(4,4)(2,3)`
`  \pscircle[linecolor=blue,linestyle=dashed](3,2.5){1}`
`\end{pspicture}`

## 拡張

PSTricks のコマンド群は低レベルであるため、数学関係の[組版](../Page/組版.md "wikilink")で使うような各種グラフィックスを簡単に描けるよう、様々な  パッケージが作られている。

**pst-plot** は、[関数のグラフを描くコマンドを用意している](../Page/関数_\(数学\).md "wikilink")。使用例を以下に示す。

`\begin{pspicture*}(-7.5,-3)(7.5,3)`
`  \psaxes[labels=none](0,0)(-7,-2)(7,2)`
`  \psplot[linecolor=blue, linewidth=1.5pt]%`
`    {-7}{7}{x 0.01745329252 div sin}`
`  \uput[45](3.1415926,0){$\pi$}`
`  \uput[90](-1.570796,0){$-\pi/2$}`
`  \uput[-90](1.570796,0){$\pi/2$}`
`  \uput[-135](-3.1415926,0){$-\pi$}`
`  \psline[linewidth=1pt,linecolor=red,linestyle=dotted]%`
`    (1.57079632,1)(1.57079632,0) `
`  \psline[linewidth=1pt,linecolor=red,linestyle=dotted]%`
`    (-1.57079632,-1)(-1.57079632,0) `
`\end{pspicture*}`

[400px](https://ja.wikipedia.org/wiki/ファイル:PSTricks-Sine.png "wikilink")(*x*) \]\] この例で示されているように、 のコマンドを図の要素として利用できる。また、PostScript は数学的操作を[逆ポーランド記法](../Page/逆ポーランド記法.md "wikilink")で行うため、pst-plot に渡す引数はそのような順序で渡す必要がある。

**pstricks-add** は、pst-plot を[極座標系](../Page/極座標系.md "wikilink")のグラフに使えるようにするもので、同時に逆ポーランド記法でない一般的な引数指定を可能とする。

**pst-math** は、[三角関数](../Page/三角関数.md "wikilink")での角度の単位を[ラジアン](../Page/ラジアン.md "wikilink")で指定可能にするとともに（PostScript のデフォルトは[度である](../Page/度_\(角度\).md "wikilink")）、[双曲線関数](../Page/双曲線関数.md "wikilink")を利用可能としている。

**pst-plot3d** は、3次元グラフィックスを以下のように作成できる。

[thumb](https://ja.wikipedia.org/wiki/ファイル:PSTricks-Hyperboloid.png "wikilink")

**multido** は、基本的なループ機能を提供するもので、パラメータを変化させてグラフを重ねて描くような場合に有効である。 [thumb](https://ja.wikipedia.org/wiki/ファイル:Drini-nonuniformconvergence.png "wikilink")

**pst-eucl** は、[幾何学](../Page/幾何学.md "wikilink")図形を容易に描けるようにする拡張である。 [thumb](https://ja.wikipedia.org/wiki/ファイル:PSTricks-Circumcircle.png "wikilink")

他にも、[回路図](../Page/回路図.md "wikilink")を描くための拡張、[グラフのための拡張](../Page/グラフ理論.md "wikilink")、[木構造のための拡張](../Page/木_\(数学\).md "wikilink")、データの視覚化のための拡張などがある。

## 関連項目

  - [](../Page/TeX.md "wikilink")
  - [](../Page/LaTeX.md "wikilink")
  - [PostScript](../Page/PostScript.md "wikilink")
  - [Inkscape](../Page/Inkscape.md "wikilink") には、[SVG](../Page/Scalable_Vector_Graphics.md "wikilink") イメージを PSTricks のコードに変換する機能がある。

## 脚注・出典

## 参考文献

  - Herbert Voss; [PSTricks -- Grafik für TeX und LaTeX](http://www.lob.de/cgi-bin/out?isbn=3865411754), 4th edition, DANTE and Lob.media, 800 pages, Heidelberg and Hamburg 2007.

## 外部リンク

  - 公式サイト [PSTricks](http://tug.org/PSTricks/main.cgi)
  - [PSTricks](https://texwiki.texjp.org/?PSTricks) TeX Wiki
  - [PSTricksパッケージ](http://www.cityfujisawa.ne.jp/~huzinami/tex/g-pack2.html)
  - [PSTricks入門](http://surgery.matrix.jp/comp/tex/PSTricks/pstricks.html)
  - [LaTeXDraw](http://latexdraw.sourceforge.net/) - [オープンソース](../Page/オープンソース.md "wikilink")のグラフィックエディタで、PSTricks のコードを生成できる。Java で書かれている。
  - [JPicEdt](http://jpicedt.sourceforge.net/site/index.php) - 同様に[オープンソース](../Page/オープンソース.md "wikilink")のグラフィックエディタで、PSTricks のコードを生成できる。Java で書かれている。

[Category:TeX](https://ja.wikipedia.org/wiki/Category:TeX "wikilink") [Category:コンピュータ言語](https://ja.wikipedia.org/wiki/Category:コンピュータ言語 "wikilink")