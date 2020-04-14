> この記事は[L-system](https://ja.wikipedia.org/wiki/L-system)から翻訳されています。


**L-system**（エルシステム、Lindenmayer system）は[形式文法](../Page/形式文法.md "wikilink")の一種で、[植物](../Page/植物.md "wikilink")の[成長](../Page/成長.md "wikilink")プロセスを初めとした様々な自然物の構造を記述・表現できる[アルゴリズム](../Page/アルゴリズム.md "wikilink")である。自然物の他にも、[反復関数系](../Page/反復関数系.md "wikilink")（Iterated Function System; IFS）のようないわゆる[自己相似](../Page/自己相似.md "wikilink")図形や[フラクタル](../Page/フラクタル.md "wikilink")図形を生成する場合にも用いられる。L-System は1968年、[ハンガリー](../Page/ハンガリー.md "wikilink")[ユトレヒト大学](../Page/ユトレヒト大学.md "wikilink")の理論生物学者にして植物学者であった[アリステッド・リンデンマイヤー](https://ja.wikipedia.org/wiki/アリステッド・リンデンマイヤー "wikilink")（[Aristid Lindenmayer](https://ja.wikipedia.org/wiki/:en:Aristid_Lindenmayer "wikilink")）により提唱され、発展した。

## 起源

[right](https://ja.wikipedia.org/wiki/ファイル:Dragon_trees.jpg "wikilink") 生物学者としてリンデンマイヤーは、[酵母](../Page/酵母.md "wikilink")や[糸状菌](../Page/糸状菌.md "wikilink")、そして[藍藻](https://ja.wikipedia.org/wiki/藍藻 "wikilink")類の *Anabaena catenula* のような[藻類](../Page/藻類.md "wikilink")など、様々な生物の成長パターンを研究していた。もともと L-system は、そのような[単細胞生物](../Page/単細胞生物.md "wikilink")もしくは体制の単純な[多細胞生物](../Page/多細胞生物.md "wikilink")の成長様式や、植物[細胞](../Page/細胞.md "wikilink")における近隣の細胞の相互関係を記述するために開発されたものであった。後に L-system はより高等な植物の形態や、複雑な分岐構造を記述する為のツールとして発展を遂げるのである。

## L-system の構造

L-system の基本は再帰性で、自己相似図形やフラクタル図形のような形状を簡単に記述する事ができる。植物やその他の見た目が自然な生物構造も同様に簡単に定義でき、再帰呼出の回数を増やす事であたかも構造が「成長」し、複雑化していくように見える。L-system は[人工生命](../Page/人工生命.md "wikilink")の生成にもよく用いられる。

L-system の文法は [:en:Unrestricted grammar](https://ja.wikipedia.org/wiki/:en:Unrestricted_grammar "wikilink") のものに似ている（→ [チョムスキー階層](../Page/チョムスキー階層.md "wikilink")）。現在では、以下のような四ツ組によって定義されることが多い。

  -
    **G** = {*V*, *S*, ω, *P*},

各要素は、

  - **V**（文字）： 置換規則（後述の **P** ）により順次置き換えられてゆく[変数の集合](../Page/変数_\(プログラミング\).md "wikilink")。L-system の再帰的な反復計算が進んでいく時に、物として「成長」してゆくのはこの **V** の要素からなる文字列である。
  - **S** ： 計算が進んでも変化しない[定数の集合](../Page/定数_\(プログラミング\).md "wikilink")。
  - **ω** ： システムの初期状態を示す**V** の要素からなる文字列。
  - **P** ： **V** を変化させてゆく置換規則の集合。各要素は、例えば (A → AB) のように、置換前（置換対象）の文字列と置換後の文字列の組み合わせにより記述される。

置換規則 **P** において、置換対象が単独の文字のみである場合、L-system は[文脈自由言語](../Page/文脈自由言語.md "wikilink")である。一方、置換規則が近隣の文字との相互関係まで考慮するものである場合、L-system は[文脈依存言語](../Page/文脈依存言語.md "wikilink")である。また、置換規則**P**が各文字に対して毎回確実に適用される時、L-system は「[決定論](../Page/決定論.md "wikilink")的」であると言われ、D0L-system（deterministic context-free L-system ）などと呼ばれる。逆に、置換規則の適用が[確率](https://ja.wikipedia.org/wiki/確率 "wikilink")に左右される場合には「[確率論](../Page/確率論.md "wikilink")的」L-system と呼ばれる。

L-system をグラフィックスに応用する場合、L-system が生成する文字列を、何らかの形で画面上の図形に変換しなければならない。例えば *FractInt* というプログラム（文末の外部リンク参照）では、[LOGO](../Page/LOGO.md "wikilink")のようなタートルを利用してグラフィックスを生成する。つまりプログラムが L-system の文字列をタートルの制御命令に[翻訳](../Page/翻訳.md "wikilink")し、図形を描画させている。

## L-systems の実例

### 例1：藻類

L-system 誕生の契機となった、藻類の成長を記述する例。

  -
    **V** ： A, B
    **S** ： なし
    **ω**： A
    **P** ： (A → AB), (B → A)

順次計算してゆくと、文字列は以下のように成長する。

  -
    *n* = 0 ： A
    *n* = 1 ： AB
    *n* = 2 ： ABA
    *n* = 3 ： ABAAB
    *n* = 4 ： ABAABABA

この例では、置換規則 **P** において、*(A → AB)* は不均等な[細胞分裂](../Page/細胞分裂.md "wikilink")により通常の細胞Aと未熟な細胞Bが生じる事を表し、*(B → A)* は未熟な細胞Bが成長して分裂可能な細胞 *A* へと成熟する事を表している。この文字列を図形化（例えば *A* を[分枝型の細胞](../Page/分枝_\(生物学\).md "wikilink")、*B* を小型の細胞の図などにそれぞれ置き換える）する事で、あたかも[寒天培地](../Page/寒天培地.md "wikilink")上に展開した藻類の[コロニー](https://ja.wikipedia.org/wiki/コロニー "wikilink")のような絵を得る事ができる。

### 例2：フィボナッチ数列

  -
    **V** ： A, B
    **S** ： なし
    **ω**： A
    **P** ： (A → B), (B → AB)

計算を進めると、以下のような文字列となる。

  -
    *n* = 0 ： A
    *n* = 1 ： B
    *n* = 2 ： AB
    *n* = 3 ： BAB
    *n* = 4 ： ABBAB
    *n* = 5 ： BABABBAB
    *n* = 6 ： ABBABBABABBAB
    *n* = 7 ： BABABBABABBABBABABBAB

この文字列の各文字数を *n*=0 から順に数えると、[フィボナッチ数](../Page/フィボナッチ数.md "wikilink")列（1 1 2 3 5 8 13 21 34 55 89 …）となっている。この例では文字列の内容は問わず長さだけに注目しているので、例えば置換規則の *(B → AB)* を *(B → BA)* で置き換えても同様の数列を得る事ができる。

### 例3：カントール集合

  -
    **V** ： A, B
    **S** ： なし
    **ω**： A
    **P** ： (A → ABA), (B → BBB)

計算を進めると、以下のような文字列となる。

  -
    *n* = 0 ： A
    *n* = 1 ： ABA
    *n* = 2 ： ABABBBABA
    *n* = 3 ： ABABBBABABBBBBBBBBABABBBABA

この文字列の *A* を線分、*B* を抜き取られた部分に置き換えると下のような図が得られる。置換規則の *(A → ABA)* は[線分](../Page/線分.md "wikilink")（[閉区間](../Page/区間_\(数学\).md "wikilink")）を3等分して中央を抜き取る操作に相当する。*(B → BBB)* は一度取り除かれた区間が戻らない事を意味する。詳しくは[カントール集合](../Page/カントール集合.md "wikilink")（[Cantor set](https://ja.wikipedia.org/wiki/:en:Cantor_set "wikilink")）を参照

[300px](https://ja.wikipedia.org/wiki/ファイル:Cantors_dust_in_seven_iterations.png "wikilink")

### 例4：コッホ曲線

直角で構成される[コッホ曲線](../Page/コッホ曲線.md "wikilink")の描画例。

  -
    **V** ： F
    **S** ： +, -;
    **ω**： F
    **P** ： (F → F+F-F-F+F)

上記において、*F* はタートルによる直線の描画、*+* はタートルを左へ90°回転、同じく*-* は右へ90°回転する事を意味する。これを順次計算すると、以下のような図形が得られる。

  -
    *n* = 0 ： [Koch Square - 0 iterations](https://ja.wikipedia.org/wiki/ファイル:square_koch_0.png "wikilink")

> > `   F`

  -
    *n* = 1 ： [Koch Square - 1 iterations](https://ja.wikipedia.org/wiki/ファイル:square_koch_1.png "wikilink")

> > `   F+F-F-F+F`

  -
    *n* = 2 ： [Koch Square - 2 iterations](https://ja.wikipedia.org/wiki/ファイル:square_koch_2.png "wikilink")

> > `   F+F-F-F+F+F+F-F-F+F-F+F-F-F+F-F+F-F-F+F+F+F-F-F+F`

  -
    *n* = 3 ： [Koch Square - 3 iterations](https://ja.wikipedia.org/wiki/ファイル:square_koch_3.png "wikilink")

> > `   F+F-F-F+F+F+F-F-F+F-F+F-F-F+F-F+F-F-F+F+F+F-F-F+F+`
> > `   F+F-F-F+F+F+F-F-F+F-F+F-F-F+F-F+F-F-F+F+F+F-F-F+F-`
> > `   F+F-F-F+F+F+F-F-F+F-F+F-F-F+F-F+F-F-F+F+F+F-F-F+F-`
> > `   F+F-F-F+F+F+F-F-F+F-F+F-F-F+F-F+F-F-F+F+F+F-F-F+F+`
> > `   F+F-F-F+F+F+F-F-F+F-F+F-F-F+F-F+F-F-F+F+F+F-F-F+F`

### 例5：ペンローズ・タイル

L-system を利用して、下図のような[平面充填](../Page/平面充填.md "wikilink")模様を生成する事もできる。詳しくは[ペンローズ・タイル](../Page/ペンローズ・タイル.md "wikilink")及び[ロジャー・ペンローズ](../Page/ロジャー・ペンローズ.md "wikilink")を参照。

[centre](https://ja.wikipedia.org/wiki/ファイル:Pen0305c.gif "wikilink")

### 例6：シェルピンスキーの三角形

L-system で[シェルピンスキーの三角形を作図する例](../Page/シェルピンスキーのギャスケット.md "wikilink")。

  -
    **V** ： A, B
    **S** ： +, -
    **ω**： A
    **P** ： (A → B−A−B), (B → A+B+A)

上記において、*A* 及び *B* はタートルによる直線の描画、*+* はタートルを左へ60°回転、同じく*-* は右へ60°回転する事を意味する。同様の図形を描く置換規則は他にもあるが、この規則の場合、タートルは三角形の左下から描き始める事になる。

[centre](https://ja.wikipedia.org/wiki/ファイル:Serpinski_Lsystem.svg "wikilink")

<div class="center" style="width:auto; margin-left:auto; margin-right:auto">

*n* = 2, *n* = 4, *n* = 6, *n* = 8 の時にそれぞれ描画される図形。*n* → ∞ の時、シェルピンスキーの三角形に等しくなる。

</div>

### 例7：コッホ曲線の変形

通常の[コッホ曲線](../Page/コッホ曲線.md "wikilink")に、周期的な角度の変更を加えながら描画したフラクタル図形の一種。

[centre](https://ja.wikipedia.org/wiki/ファイル:Kochsnowflake_algorith_modified.jpg "wikilink")

## その他の L-system を利用したグラフィックス

  - [地衣類](../Page/地衣類.md "wikilink")、あるいは[蘚苔類](../Page/コケ植物.md "wikilink")：

|                                                                               |                                                                               |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [150px](https://ja.wikipedia.org/wiki/ファイル:L-system_Penrose02.jpg "wikilink") | [150px](https://ja.wikipedia.org/wiki/ファイル:L-system_Penrose01.jpg "wikilink") |

  - 草本の作図例：

|                                                                              |                                                                              |                                                                            |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| [150px](https://ja.wikipedia.org/wiki/ファイル:L-system_Spiral03.jpg "wikilink") | [150px](https://ja.wikipedia.org/wiki/ファイル:L-system_Spiral04.jpg "wikilink") | [150px](https://ja.wikipedia.org/wiki/ファイル:L-system_Bush01.jpg "wikilink") |

  - 木本の作図例：

|                                                                                         |                                                                                         |                                                                                         |                                                                                  |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| [150px](https://ja.wikipedia.org/wiki/ファイル:Fractal_tree_\(Plate_b_-_1\).jpg "wikilink") | [150px](https://ja.wikipedia.org/wiki/ファイル:Fractal_tree_\(Plate_b_-_2\).jpg "wikilink") | [150px](https://ja.wikipedia.org/wiki/ファイル:Fractal_tree_\(Plate_b_-_3\).jpg "wikilink") | [150px](https://ja.wikipedia.org/wiki/ファイル:L-system_frakdal_agac.jpg "wikilink") |

  - [原生動物](../Page/原生動物.md "wikilink")など：

<table>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/ファイル:L-system_frakdal01.jpg" title="wikilink">150px</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ファイル:L-system_frakdal02.jpg" title="wikilink">150px</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ファイル:L-system_karebitki.jpg" title="wikilink">165px</a></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ファイル:Haeckel_Spumellaria.jpg" title="wikilink">135px</a></p>
<ul>
<li><small>（参考）<a href="../Page/エルンスト・ヘッケル.md" title="wikilink">ヘッケルによる放散虫のスケッチ</a>。</small></li>
</ul></td>
</tr>
</tbody>
</table>

## 既知の問題

L-system に関する問題は数多く存在するが、その最たるものは L-system を逆に辿る事が困難であるというものである。具体的には、ある構造が示された時に、その構造を生成するパラメータや置換規則を見つける事が難しい。これは自然物のような複雑な（反復回数の多い）過程を経て形成された図形に顕著である。

## L-system の種類

[実数](../Page/実数.md "wikilink")列における L-system：

  - [Thue-Morse sequence](https://ja.wikipedia.org/wiki/:en:Thue-Morse_sequence "wikilink")

[平面](../Page/平面.md "wikilink")における L-system：

  - [平面充填曲線・図形](https://ja.wikipedia.org/wiki/空間充填曲線 "wikilink")（[Space-filling curve](https://ja.wikipedia.org/wiki/:en:Space-filling_curve "wikilink")）ほか：
      - [ヒルベルト曲線](https://ja.wikipedia.org/wiki/ヒルベルト曲線 "wikilink")（[Hilbert curve](https://ja.wikipedia.org/wiki/:en:Hilbert_curve "wikilink")）
      - [ペアノ曲線](https://ja.wikipedia.org/wiki/ペアノ曲線 "wikilink")（[Peano's curves](https://ja.wikipedia.org/wiki/:en:Peano's_curves "wikilink")）
      - [コーラム](../Page/砂絵.md "wikilink")（[Kolam](https://ja.wikipedia.org/wiki/:en:Kolam "wikilink")）
      - [レヴィC曲線](../Page/レヴィC曲線.md "wikilink")（[Lévy C curve](https://ja.wikipedia.org/wiki/:en:Lévy_C_curve "wikilink")）
      - [ドラゴン曲線](https://ja.wikipedia.org/wiki/ドラゴン曲線 "wikilink")（[Dragon curve](https://ja.wikipedia.org/wiki/:en:Dragon_curve "wikilink")）
      - [ペンローズ・タイル](../Page/ペンローズ・タイル.md "wikilink")（[Penrose tiling](https://ja.wikipedia.org/wiki/:en:Penrose_tiling "wikilink")）

[空間](../Page/空間.md "wikilink")における L-system：

  - 自然物
      - [植物](../Page/植物.md "wikilink")
          - [木](https://ja.wikipedia.org/wiki/木 "wikilink")本
          - [草本](../Page/草本.md "wikilink")
          - [シダ植物](../Page/シダ植物.md "wikilink")
      - [藻類](../Page/藻類.md "wikilink")・[原生動物](../Page/原生動物.md "wikilink")
          - [放散虫](../Page/放散虫.md "wikilink")

### 確率的L-system

確率的 (Stochastic) L-systemは、L-systemを拡張して確率的に分岐できるようにしたものである。確率的L-systemには標準が無いため、ソフトウェアによって文法が異なる。

以下は確率的な分岐を行うL-systemの実装毎の例である。

<table>
<thead>
<tr class="header">
<th><p>Tong Linの実装<br />
(1996)</p></th>
<th><p>Houdini<br />
(L-system SOP)</p></th>
<th><p>Cinema 4D<br />
(MoSplineのTurtle)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>A=(0.5)FA
A=(0.25)+F-A
A=(0.25)-F+A</code></pre></td>
<td><pre><code>A=FA:0.5
A=+F-A:0.25
A=-F+A:0.25</code></pre></td>
<td><pre><code>A:(rnd(1)&lt;0.5)=FA
A:(rnd(1)&lt;0.75)=+F-A
A:(rnd(1)&gt;0.75)=-F+A</code></pre></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### 文脈依存L-system

[文脈依存](../Page/文脈依存文法.md "wikilink") (Context-sensitive) L-systemは、L-systemを拡張したものであり、パターンマッチングによって文脈に依存した分岐が可能となっている。文脈依存L-systemを実装したものとしては、Tong Linの実装などが存在する。

## 関連項目

  - [フラクタル](../Page/フラクタル.md "wikilink")
      - [反復関数系](../Page/反復関数系.md "wikilink")
      - [フラクタル幾何](../Page/フラクタル幾何.md "wikilink")
          - [シェルピンスキーのギャスケット](../Page/シェルピンスキーのギャスケット.md "wikilink")
          - [コッホ曲線](../Page/コッホ曲線.md "wikilink")
  - [先端成長](../Page/先端成長.md "wikilink")

## 参考文献

  - Przemyslaw Prusinkiewicz - [:en:The Algorithmic Beauty of Plants](https://ja.wikipedia.org/wiki/:en:The_Algorithmic_Beauty_of_Plants "wikilink") [PDF version available here for free](http://algorithmicbotany.org/papers/#abop)

## 外部リンク

  - [David J. Wright's article on L-systems](http://www.math.okstate.edu/mathdept/dynamics/lecnotes/node12.html#SECTION00040000000000000000)
  - [Algorithmic Botany at the University of Calgary](http://algorithmicbotany.org/)
  - [Branching: L-system Tree](http://www.mizuno.org/applet/branching/) L-systemを用いて木の生長をシミュレートする[Javaアプレット](../Page/Javaアプレット.md "wikilink")（英語）
  - [Fractint L-System True Fractals](http://spanky.triumf.ca/www/fractint/lsys/truefractal.html)
  - ["An introduction to Lindenmayer systems", by Gabriela Ochoa](http://www.biologie.uni-hamburg.de/b-online/e28_3/lsys.html). Brief description of L-systems and how the strings they generate can be interpreted by computer.
  - ["powerPlant" an open-source landscape modelling software](http://sourceforge.net/projects/pplant/)
  - [*Fractint* home page](http://spanky.triumf.ca/www/fractint/fractint.html)

<!-- end list -->

  - ["L-system in Falk arts" The FORMA commurative issue of the conference ISKFA06](http://www.cityfujisawa.ne.jp/~intvsn/)
  - [A simple L-systems generator (Windows)](http://www.generation5.org/content/2002/lse.asp)
  - [Lyndyhop: another simple L-systems generator (Windows & Mac)](http://www.lab4web.com/chelmiger/lyndyhop/)
  - [An evolutionary L-systems generator (anyos\*)](http://www.cs.ucl.ac.uk/staff/W.Langdon/pfeiffer.html)
  - [L-systems gallery – a tribute to Fractint](http://fractint.oblivion.cz./)
  - ["LsystemComposition"](http://www.pawfal.org/index.php?page=LsystemComposition). Page at Pawfal ("poor artists working for a living") about using L-systems and [genetic algorithms](https://ja.wikipedia.org/wiki/:en:Genetic_algorithms "wikilink") to generate music.
  - [eXtended L-Systems (XL), Relational Growth Grammars, and open-source software platform GroIMP.](http://www.grogra.de/)
  - [A JAVA applet with many fractal figures generated by L-systems.](http://to-campos.planetaclix.pt/fractal/plantae.htm)
  - [L-systems in Architecture; genetic housing.](http://www.arch.columbia.edu/Students/Fall2003/Cheng.Chih-Wei/)
  - [L-systems in Plant Growth,Simulation and Visualization (PlantVR).](http://www.somporn.net/)
  - [Musical L-systems: Theory and applications about using L-systems to generate musical structures, from waveforms to macro-forms.](http://www.koncon.nl/public_site/220/Sononieuw/NL/thesis-pdf/Stelios%20Manousakis-Musical%20L-systems.pdf)
  - [LSys/JS](http://lsysjs.qwert.ch/) - Interactive L-System interpreter using the [Canvas HTML element](https://ja.wikipedia.org/wiki/:en:Canvas_\(HTML_element\) "wikilink").

[Category:コンピュータグラフィックス](https://ja.wikipedia.org/wiki/Category:コンピュータグラフィックス "wikilink") [Category:フラクタル](https://ja.wikipedia.org/wiki/Category:フラクタル "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink") [Category:形式言語](https://ja.wikipedia.org/wiki/Category:形式言語 "wikilink") [Category:生物学](https://ja.wikipedia.org/wiki/Category:生物学 "wikilink")