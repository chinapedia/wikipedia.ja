> この記事は[MetaPost](https://ja.wikipedia.org/wiki/MetaPost)から翻訳されています。


**MetaPost**は[プログラミング言語](../Page/プログラミング言語.md "wikilink")、およびその[インタプリタ](../Page/インタプリタ.md "wikilink")の両方を意味する。[ドナルド・クヌース](../Page/ドナルド・クヌース.md "wikilink")が作った[METAFONT](https://ja.wikipedia.org/wiki/METAFONT "wikilink")に由来する。[PostScript](../Page/PostScript.md "wikilink")内における図形の描写に優れる。METAFONTの優れた宣言構文を共有している。

## 例

MetaPostインタプリタ ([Linux](../Page/Linux.md "wikilink")上で`mpost`コマンドを経由) にて生成された、`example.mp`という単一のファイルは、3つの[epsファイル](../Page/Encapsulated_PostScript.md "wikilink")`example.1`, `example.2`, `example.3`を生成する。右のそれらが描画されたものである。

これら3つのepsファイルの結果は以下で使うことが出来る。

  - [LaTeX](../Page/LaTeX.md "wikilink")経由の[TeX](../Page/TeX.md "wikilink")にて\\includegraphicsコマンド
  - [ConTeXt](../Page/ConTeXt.md "wikilink")にて\\externalfigure
  - [plain TeX](https://ja.wikipedia.org/wiki/TeX#機能 "wikilink")\\epsfboxコマンド
  - supp-pdf.texからの(Plain pdftexにて)\\convertMPtoPDFコマンド

<div style="float:right; background: white">

[Metapost_ex.svg](https://ja.wikipedia.org/wiki/File:Metapost_ex.svg "fig:Metapost_ex.svg")

</div>

    <nowiki>transform pagecoords;</nowiki>
    <nowiki>pagecoords:=identity scaled 10mm shifted (100mm,150mm);</nowiki>
    <nowiki>beginfig (1)</nowiki>
    <nowiki>    fill ((0,0)--(2,0)--(2,1)--(1,1)--(1,2)--(0,2)--cycle)</nowiki>
    <nowiki>        transformed pagecoords withcolor green;</nowiki>
    <nowiki>    draw ((2,0)..(2,1)..(1,1)..(1,2)..(0,2))</nowiki>
    <nowiki>        transformed pagecoords;</nowiki>
    <nowiki>    drawarrow ((0,0)--(2,2)) transformed pagecoords;</nowiki>
    <nowiki>endfig;</nowiki>
    <nowiki>beginfig (2)</nowiki>
    <nowiki>    draw (for i=0 upto 7: dir (135i)-- endfor cycle)</nowiki>
    <nowiki>        transformed pagecoords;</nowiki>
    <nowiki>endfig;</nowiki>
    <nowiki>pagecoords:=identity scaled 15mm shifted (100mm,150mm);</nowiki>
    <nowiki>beginfig (3);</nowiki>
    <nowiki>    % declare paths to be used</nowiki>
    <nowiki>    path p[],p[]t;</nowiki>
    <nowiki>    % set up points by defining relationships</nowiki>
    <nowiki>    z1=(0,0);   z2=z1+2up;</nowiki>
    <nowiki>    z3=z1+whatever*dir (60)=z2+whatever*dir (-50);</nowiki>
    <nowiki>    z4=z3+(-1.5,-.5);</nowiki>
    <nowiki>    z5=z1+dir (135);</nowiki>
    <nowiki>    z0=whatever[z1,z2]=whatever[z3,z4];</nowiki>
    <nowiki>    % set up paths</nowiki>
    <nowiki>    p0=fullcircle yscaled .5 rotated 45 shifted z0 ;</nowiki>
    <nowiki>    p1=z2---z4..z0..z3---z1;</nowiki>
    <nowiki>    p2=p1 cutbefore p0 cutafter p0;</nowiki>
    <nowiki>    p3=p0 cutbefore p1 cutafter p1;</nowiki>
    <nowiki>    p4=p2---p3---cycle;</nowiki>
    <nowiki>    % define transformed versions of paths and points</nowiki>
    <nowiki>    for i=0 upto 4: p[i]t=p[i] transformed pagecoords; endfor</nowiki>
    <nowiki>    for i=0 upto 5: z[i]t=z[i] transformed pagecoords; endfor</nowiki>
    <nowiki>    % do some drawing</nowiki>
    <nowiki>    fill p4t withcolor (1,1,0.2);</nowiki>
    <nowiki>    draw z1t---z2t withcolor .5white;</nowiki>
    <nowiki>    draw z3t---z4t withcolor .5white;</nowiki>
    <nowiki>    pickup pencircle;</nowiki>
    <nowiki>    draw p0t dashed withdots scaled .3;</nowiki>
    <nowiki>    draw p1t dashed evenly;</nowiki>
    <nowiki>    draw p2t withcolor blue;</nowiki>
    <nowiki>    draw p3t withcolor red;</nowiki>
    <nowiki>    label.lrt (btex $z_0$ etex, z0t);</nowiki>
    <nowiki>    label.llft (btex $z_1$ etex, z1t);</nowiki>
    <nowiki>    label.top (btex $z_2$ etex, z2t);</nowiki>
    <nowiki>    label.rt (btex $z_3$ etex, z3t);</nowiki>
    <nowiki>    label.llft (btex $z_4$ etex, z4t);</nowiki>
    <nowiki>    for i=0 upto 4:</nowiki>
    <nowiki>        drawdot z[i]t withpen pencircle scaled 2;</nowiki>
    <nowiki>    endfor</nowiki>
    <nowiki>endfig;</nowiki>
    <nowiki>bye</nowiki>

## 関連項目

  - [ConTeXt](../Page/ConTeXt.md "wikilink")

  - [PSTricks](../Page/PSTricks.md "wikilink")

  - [PGF/TikZ](https://ja.wikipedia.org/wiki/PGF/TikZ "wikilink")

  - [METAFONT](https://ja.wikipedia.org/wiki/METAFONT "wikilink")

  -
  - [Asymptote](https://ja.wikipedia.org/wiki/Asymptote "wikilink")

## 脚注・出典

  - MetaFun (modules for Metapost) by Hans Hagen, [1](http://wiki.contextgarden.net/MetaFun)
  - [Donald Knuth](https://ja.wikipedia.org/wiki/Donald_Knuth "wikilink"): *The [METAFONT](https://ja.wikipedia.org/wiki/METAFONT "wikilink")book*, ([Computers and Typesetting](https://ja.wikipedia.org/wiki/Computers_and_Typesetting "wikilink") Volume C) [Addison-Wesley](https://ja.wikipedia.org/wiki/Addison-Wesley "wikilink") 1986. ISBN 0-201-13444-6
  - Comprehensive T<sub>E</sub>X Archive Network ([CTAN](https://ja.wikipedia.org/wiki/CTAN "wikilink")): <http://www.ctan.org/>. Repository of the T<sub>E</sub>X source and hundreds of add-ons and style files.
  - (La)TeX Navigator provides 305 simple MetaPost examples: <http://tex.loria.fr/prod-graph/zoonekynd/metapost/metapost.html>
  - Taco Hoekwater: [MetaPost developments—autumn 2006](http://www.tug.org/TUGboat/Articles/tb27-1/tb86hoekwater-metapost.pdf). *TUGboat* **27**:1 (2006).

## 外部リンク

  - [MetaPost TeX Wiki](https://texwiki.texjp.org/?MetaPost) - TeX Wiki内のMetaPostの解説ページ
  - [METAPOST](http://www.sat.t.u-tokyo.ac.jp/~hideyuki/metapost/) - 鈴木秀幸のページ。松山道夫より引き継いで日本語MetaPostのソース管理・配布を行なっている。

[Category:TeX](https://ja.wikipedia.org/wiki/Category:TeX "wikilink") [Category:PostScript](https://ja.wikipedia.org/wiki/Category:PostScript "wikilink") [Category:ベクターグラフィックス・マークアップ言語](https://ja.wikipedia.org/wiki/Category:ベクターグラフィックス・マークアップ言語 "wikilink")