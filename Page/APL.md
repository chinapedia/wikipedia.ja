> この記事は[APL](https://ja.wikipedia.org/wiki/APL)から翻訳されています。


**APL**（エーピーエル）は、[プログラミング言語](../Page/プログラミング言語.md "wikilink")のひとつで、1957年の[ケネス・アイバーソン](https://ja.wikipedia.org/wiki/ケネス・アイバーソン "wikilink")による創案に基づいた独特の表記法を用いる。処理系の実装は、ほとんどが対話型[インタプリタ](../Page/インタプリタ.md "wikilink")である。とくに多次元[配列](../Page/配列.md "wikilink")の柔軟な処理が特徴である。「APL」は「**プログラミング言語**」() の略であるが、言語の特性から、ときに「配列処理言語」() などとされる。

## 概要

APLは他の多くのプログラミング言語と異なり、「APL記号」と呼ばれる特殊な記号を用いるが、これにより計算式をきわめて簡潔（過ぎるほど）に記述できる。

[IBM-Kugelkopf_(2._Generation).jpg](https://ja.wikipedia.org/wiki/File:IBM-Kugelkopf_\(2._Generation\).jpg "fig:IBM-Kugelkopf_(2._Generation).jpg")の「ゴルフボール」印字ヘッドにAPL文字を載せた物を使った[IBM 2741キーボード・プリンター通信端末などを利用した](https://ja.wikipedia.org/wiki/IBM_274x "wikilink")。\]\] 特殊な記号の扱いに関しては、キーボードからの入力については、これを支援するためキートップに貼るシールや交換用キーキャップ、はては専用キーボードもある。情報交換用ないし計算機の内部表現としては、従来は1バイトの文字コードを切り替えるなどしていたが、Unicodeでは「[その他の技術用記号](https://ja.wikipedia.org/wiki/その他の技術用記号 "wikilink")」(Miscellaneous Technical)に収録された（U+2336～U+237A）。出力は、初期には[IBM Selectricイプライタのゴルフボール状のタイプボールを専用のものに取り替えて印字された](https://ja.wikipedia.org/wiki/IBM_Selectric_typewriter "wikilink")。[DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")の、グラフィックによる文字表示環境を利用した処理系が作られたこともあった。現在は（新しく実装されたりしたものでは）前述のUnicode[フォント](../Page/フォント.md "wikilink")が使われる。

APLではプログラムを非常に簡潔に記述できるが、その反面、[可読性](https://ja.wikipedia.org/wiki/可読性 "wikilink")に乏しく、「」というジョーク由来の「書き込み専用プログラム」とか、「他人の書いたものを修正するくらいであれば、新たに書き起こす方が速い」と言われることもある。

1957年に創案された記法は、1962年に著書 "*A Programming Language*" として発表された。続いて1964年にプログラミング言語処理系として実装された。1966年には[IBM System/360上のOS](https://ja.wikipedia.org/wiki/System/360 "wikilink")、[OS/360](https://ja.wikipedia.org/wiki/OS/360 "wikilink")上での処理系の実装の（インタラクティブ環境を含む）APL\\360 が発表された。

APLは[タイムシェアリングシステム](https://ja.wikipedia.org/wiki/タイムシェアリングシステム "wikilink")で利用できる対話型[インタプリタ](../Page/インタプリタ.md "wikilink")のある言語として注目を集めた。しかしながら、[FORTRAN](../Page/FORTRAN.md "wikilink")ほどに普及することはなかった。

[マイクロコンピュータ](../Page/マイクロコンピュータ.md "wikilink")からの時代には[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")(CP/M80)上に構築した APL\\80 があり、端末によってはAPL記号を扱うことが可能であった。

日本では、[日本IBMからの販売の他](https://ja.wikipedia.org/wiki/日本アイ・ビー・エム "wikilink")、1980年代に株式会社[アンペールからノート型のAPLマシン](https://ja.wikipedia.org/wiki/アンペール_\(企業\) "wikilink")"WS-1"が発売された。

APLを発展させた言語に、**[J](https://ja.wikipedia.org/wiki/J_\(プログラミング言語\) "wikilink")**がある。主な変更点の1つに、[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")だけで表記するようにした点が挙げられる。

<table>
<tbody>
<tr class="odd">
<td><table>
<tbody>
<tr class="odd">
<td><p>'</p></td>
<td><p>(</p></td>
<td><p>)</p></td>
<td><p>+</p></td>
<td><p>,</p></td>
<td><p>-</p></td>
<td><p>.</p></td>
<td><p>/</p></td>
<td><p>:</p></td>
<td><p>;</p></td>
<td><p>&lt;</p></td>
<td><p>=</p></td>
<td><p>&gt;</p></td>
<td><p>?</p></td>
<td><p>[</p></td>
<td><p>]</p></td>
</tr>
<tr class="even">
<td><p>\</p></td>
<td><p>_</p></td>
<td><p>¨</p></td>
<td><p>¯</p></td>
<td><p>×</p></td>
<td><p>÷</p></td>
<td><p>←</p></td>
<td><p>↑</p></td>
<td><p>→</p></td>
<td><p>↓</p></td>
<td><p>∆</p></td>
<td><p>∇</p></td>
<td><p>∘</p></td>
<td><p>∣</p></td>
<td><p>∧</p></td>
<td><p>∨</p></td>
</tr>
<tr class="odd">
<td><p>∩</p></td>
<td><p>∪</p></td>
<td><p>∼</p></td>
<td><p>≠</p></td>
<td><p>≤</p></td>
<td><p>≥</p></td>
<td><p>≬</p></td>
<td><p>⊂</p></td>
<td><p>⊃</p></td>
<td><p>⌈</p></td>
<td><p>⌊</p></td>
<td><p>⊤</p></td>
<td><p>⊥</p></td>
<td><p>⋆</p></td>
<td><p>⌶</p></td>
<td><p>⌷</p></td>
</tr>
<tr class="even">
<td><p>⌸</p></td>
<td><p>⌹</p></td>
<td><p>⌺</p></td>
<td><p>⌻</p></td>
<td><p>⌼</p></td>
<td><p>⌽</p></td>
<td><p>⌾</p></td>
<td><p>⌿</p></td>
<td><p>⍀</p></td>
<td><p>⍁</p></td>
<td><p>⍂</p></td>
<td><p>⍃</p></td>
<td><p>⍄</p></td>
<td><p>⍅</p></td>
<td><p>⍆</p></td>
<td><p>⍇</p></td>
</tr>
<tr class="odd">
<td><p>⍈</p></td>
<td><p>⍉</p></td>
<td><p>⍊</p></td>
<td><p>⍋</p></td>
<td><p>⍌</p></td>
<td><p>⍍</p></td>
<td><p>⍎</p></td>
<td><p>⍏</p></td>
<td><p>⍐</p></td>
<td><p>⍑</p></td>
<td><p>⍒</p></td>
<td><p>⍓</p></td>
<td><p>⍔</p></td>
<td><p>⍕</p></td>
<td><p>⍖</p></td>
<td><p>⍗</p></td>
</tr>
<tr class="even">
<td><p>⍘</p></td>
<td><p>⍙</p></td>
<td><p>⍚</p></td>
<td><p>⍛</p></td>
<td><p>⍜</p></td>
<td><p>⍝</p></td>
<td><p>⍞</p></td>
<td><p>⍟</p></td>
<td><p>⍠</p></td>
<td><p>⍡</p></td>
<td><p>⍢</p></td>
<td><p>⍣</p></td>
<td><p>⍤</p></td>
<td><p>⍥</p></td>
<td><p>⍦</p></td>
<td><p>⍧</p></td>
</tr>
<tr class="odd">
<td><p>⍨</p></td>
<td><p>⍩</p></td>
<td><p>⍪</p></td>
<td><p>⍫</p></td>
<td><p>⍬</p></td>
<td><p>⍭</p></td>
<td><p>⍮</p></td>
<td><p>⍯</p></td>
<td><p>⍰</p></td>
<td><p>⍱</p></td>
<td><p>⍲</p></td>
<td><p>⍳</p></td>
<td><p>⍴</p></td>
<td><p>⍵</p></td>
<td><p>⍶</p></td>
<td><p>⍷</p></td>
</tr>
<tr class="even">
<td><p>⍸</p></td>
<td><p>⍹</p></td>
<td><p>⍺</p></td>
<td><p>⎕</p></td>
<td><p>○</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ファイル:APL2-nappaimisto.png" title="wikilink">thumb</a></p></td>
</tr>
</tbody>
</table>

## 演算機能

APLは他の[プログラミング言語](../Page/プログラミング言語.md "wikilink")と比べ特徴的な演算機能を持つ。特に（他には[PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")などで見られるが）スカラ値だけではなく配列も、式中の演算の直接の対象にできるという原始的な[ジェネリックプログラミング](https://ja.wikipedia.org/wiki/ジェネリックプログラミング "wikilink")の機能がある点と、[w:Fold (higher-order function)等に類似した](https://ja.wikipedia.org/wiki/w:Fold_\(higher-order_function\) "wikilink")[高階関数](https://ja.wikipedia.org/wiki/高階関数 "wikilink")に相当する機能がある点が特徴である。ここではAPLの基本的な演算機能について述べる。

### 関数と作用子

それぞれ英語ではfunctionとoperatorで、ここでは訳語は日本APL協会が配布している三枝協亮訳「APL2の紹介」のそれに従っている。APLでは、前置演算子ないし中置演算子のように使う記号列を「関数」、関数を対象として操作する[高階関数](https://ja.wikipedia.org/wiki/高階関数 "wikilink")の意味をもつ記号列を「作用子」という。高階関数をoperatorとするのは、解析学における[作用素](https://ja.wikipedia.org/wiki/作用素 "wikilink")から来ており、作用子の語も「作用素」から来ている。

### 右から左

まず、四則演算の関数を中置で使う例から始める。 一般の算術の式では、
3+2-1
は左から右の順で、
((3+2)-1)
の意味とする（左結合）のが一般的なルールだが、APLでは右から左に、
(3+(2-1))
の意味（右結合）である。

さらに、APLにはこの「右から左」のルールしか存在しない。たとえば一般の算術では、左から右の規則より優先するルールとして、加減算より乗除算が先、という[ルールがあり](https://ja.wikipedia.org/wiki/演算子の優先順位 "wikilink")、たとえば、
1+2×3+4
は、
(1+(2×3)+4)
の意味である。これに対しAPLでは、乗算も加算も同様に「右から左」のルールに従い、
(1+(2×(3+4)))
となる。

### 一項と二項

APLでは、同じ記号列（関数）を前置演算子（単項演算子）の形でも中置演算子（2項演算子）の形でも使い、それぞれで意味が違う（基本的にはある程度それぞれ連想できる意味だが）という、一種の[多重定義](https://ja.wikipedia.org/wiki/多重定義 "wikilink")が多用される。APLの用語では「一項」「二項」と言う。他の言語でも、例えば[C言語](../Page/C言語.md "wikilink")では `*`（アスタリスク）は乗算の中置演算子であると同時に、前置演算子としては[ポインタのデリファレンスである](https://ja.wikipedia.org/wiki/ポインタ_\(プログラミング\) "wikilink")。しかしAPLでは、ほとんどの関数が一項と二項それぞれの意味を持つ。

例えば `!` は前置では[階乗](../Page/階乗.md "wikilink")を表し、例えば

`! 5`

は 120 を返す。しかし中置として使用すると[組み合わせの数を表し](https://ja.wikipedia.org/wiki/組合せ_\(数学\) "wikilink")、例えば

`2 ! 5`

とした場合、 10 (=<sub>5</sub>C<sub>2</sub>) を返す。

前の節で述べたように、優先順位がなく常に右結合であるため、文法の曖昧性（多義性）の問題はない。

### 配列演算

APL の特徴の一つに配列演算、すなわち[配列](../Page/配列.md "wikilink")同士の演算が可能なことが挙げられる。例として

`1 2 3 + 4 5 6`

という式を評価すると（値の、空白で区切られた連続する並びは配列の[リテラル](https://ja.wikipedia.org/wiki/リテラル "wikilink")である）、それぞれの要素毎に加算を行い 5 7 9 という配列を返す。この場合二つの配列は同じ長さでないとエラーとなる。前置記法で使用した場合でも同じく各要素毎の演算結果を返す。

`! 2 3 4`

は、各要素の階乗を要素とする配列を返す、この場合は 2 6 24 となる。

### 作用子

ここでは、「内積」と「外積」と呼ばれる作用子を例として紹介する。これは、積 (および和) を演算子としてとり、それによって定義される[内積](../Page/内積.md "wikilink")と[直積 (ベクトル)](https://ja.wikipedia.org/wiki/直積_\(ベクトル\) "wikilink") (outer product) を計算する演算子を返す作用子と解釈できる。

内積の作用子の記号は "." であり、

`(関数1).(関数2)`

とすることで、二つの関数を以下で説明するように合成する。例えば、

`9 8 7 +.× 6 5 4`

とした場合、まず後の関数（この場合は `×`）を各要素毎に適用し、

`9×6 8×5 7×4`

となる。この結果の要素間に、前の関数（ここでは `+`）を入れた計算である、

`9×6 + 8×5 + 7×4`

が全体の意味であり、評価すると得られる値は 122 である。なお、右から左のルールがここでは、

`(9×6) + ((8×5) + (7×4))`

のように効くことに注意する。

この例のように、2個の1次元配列に対し . を +.× のように使うと、ベクトルの内積の計算となり、同様に +.× を2次元配列に対し使うと[行列積となるが](https://ja.wikipedia.org/wiki/行列#行列の積 "wikilink")、これに限らず . は他の関数とも組み合わせて使うことができる。

外積の作用子の記号列は "∘." であり（ "∘" と前述した内積との組み合わせではない）、

`∘.(関数)`

とすると、配列に対して以下で説明するように関数を適用する。例えば、

`1 2 3 ∘.× 4 5 6 7`

とした場合、

| × | 4     | 5     | 6     | 7     |
| - | ----- | ----- | ----- | ----- |
| 1 | 1 × 4 | 1 × 5 | 1 × 6 | 1 × 7 |
| 2 | 2 × 4 | 2 × 5 | 2 × 6 | 2 × 7 |
| 3 | 3 × 4 | 3 × 5 | 3 × 6 | 3 × 7 |

という計算が行われ

|    |    |    |    |
| -- | -- | -- | -- |
| 4  | 5  | 6  | 7  |
| 8  | 10 | 12 | 14 |
| 12 | 15 | 18 | 21 |

という2次元の配列を返す。

## 関連項目

  - [J (プログラミング言語)](https://ja.wikipedia.org/wiki/J_\(プログラミング言語\) "wikilink")
  - [A+](https://ja.wikipedia.org/wiki/A+ "wikilink")

## 外部リンク

  - [日本APL協会](http://www.ae.keio.ac.jp/lab/soc/takeuchi/japla/index.html)
  - [日本語APL](http://www.vector.co.jp/soft/maker/ibm/se001160.html?y) - [MS-DOS](../Page/MS-DOS.md "wikilink")用のAPL[インタープリタ](https://ja.wikipedia.org/wiki/インタープリタ "wikilink")、日本語に対応している。
  - [APL Unicode Font – Extended](http://www.vector.org.uk/resource/simp2.htm) - [フリーのAPLフォント](../Page/フリーウェア.md "wikilink")。
  - [NARS2000](http://www.nars2000.org/) ISO/IEC 13751 Extended APLのオープンソースな実装。

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:IBMのソフトウェア](https://ja.wikipedia.org/wiki/Category:IBMのソフトウェア "wikilink")