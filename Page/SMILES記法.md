> この記事は[SMILES](https://ja.wikipedia.org/wiki/SMILES)から翻訳されています。


**SMILES記法**（[スマイルスきほう](https://ja.wikipedia.org/wiki/アクロニム "wikilink")、）とは、[分子](../Page/分子.md "wikilink")の[化学構造を](https://ja.wikipedia.org/wiki/化学式#構造式 "wikilink")[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")符号の[英数字](https://ja.wikipedia.org/wiki/英数字 "wikilink")で[文字列](../Page/文字列.md "wikilink")化した、構造の[曖昧性](https://ja.wikipedia.org/wiki/曖昧性 "wikilink")の無い表記方法である。SMILES[文字列](../Page/文字列.md "wikilink")は多くの種類の[分子エディタ](https://ja.wikipedia.org/wiki/分子エディタ "wikilink")においてインポート可能で、二次元の図表あるいは三次元のモデルとして表示することができる。

SMILES表記は[1980年代](../Page/1980年代.md "wikilink")の終わりにDavid Weiningerにより開発され、その後に多数の人の手で変更あるいは拡張がなされてきた。中でもDaylight Chemical Information Systems社の貢献が大きい。他の線形な同様な表記法としてはWiswesser Line Notation (WLN), ROSDAL そして SLN (Tripos社)が挙げられる。

## グラフ理論に基づいた記法の定義

[グラフ理論](../Page/グラフ理論.md "wikilink")に基づくコンピュータ処理の観点では、SMILESはを[深さ優先で走査して](../Page/深さ優先探索.md "wikilink")、[節点](https://ja.wikipedia.org/wiki/頂点_\(グラフ理論\) "wikilink")（[原子](https://ja.wikipedia.org/wiki/原子 "wikilink")）と[辺](../Page/グラフ理論.md "wikilink")（[結合](../Page/化学結合.md "wikilink")）を表現する文字列である。分子グラフの構築では、まず系の水素原子を取り除き（ただし[不斉中心](https://ja.wikipedia.org/wiki/不斉中心 "wikilink")を除く）、環を形成しているところは切り開いて[全域木](../Page/全域木.md "wikilink")（）に変換する。環を開いたところには数字でラベル付け（後置）して、つながっていた節点同士を示す。[丸括弧](https://ja.wikipedia.org/wiki/丸括弧 "wikilink")（, `()`）は[木が分枝している場所を表すのに使用する](../Page/木構造_\(データ構造\).md "wikilink")。

原子は角括弧（, `[]`）でくくられるが、、すなわち [B](../Page/ホウ素.md "wikilink"), [C](../Page/炭素.md "wikilink"), [N](../Page/窒素.md "wikilink"), [O](../Page/酸素.md "wikilink"), [P](../Page/リン.md "wikilink"), [S](../Page/硫黄.md "wikilink"), [F](../Page/フッ素.md "wikilink"), [Cl](../Page/塩素.md "wikilink"), [Br](https://ja.wikipedia.org/wiki/臭素 "wikilink"), [I](https://ja.wikipedia.org/wiki/ヨウ素 "wikilink") のいずれかで、[形式電荷](https://ja.wikipedia.org/wiki/形式電荷 "wikilink")を持たず、[同位体](../Page/同位体.md "wikilink")を陽に指定する必要がなく、かつ不斉中心でない場合は`[]`を省略してもよい。この場合は[原子価](../Page/原子価.md "wikilink")に基づいて水素が暗黙的に付加しているものとみなされる。たとえば`O`、`N`はそれぞれ[水](../Page/水.md "wikilink")、[アンモニア](../Page/アンモニア.md "wikilink")である（水素を陽に書くと`[H]O[H]`などになるが、このように書かれることはほとんどない）。形式電荷を持っている場合は`+-`と数字を後置する（たとえば[アンモニウムイオン](https://ja.wikipedia.org/wiki/アンモニウムイオン "wikilink")は`[NH4+]`、[鉄](../Page/鉄.md "wikilink") (II) は`[Fe+2]`）。同位体を陽に指定する場合は[質量数](../Page/質量数.md "wikilink")を整数で前置する（たとえば[炭素14](../Page/炭素14.md "wikilink")は`[14C]`）。不斉中心については後述する。

結合は一次から順に`-`、`=`、`#`、`$` で表される（ただし[一重結合](https://ja.wikipedia.org/wiki/一重結合 "wikilink")`-`は通常省略される）。[二重結合](https://ja.wikipedia.org/wiki/二重結合 "wikilink")`=`につながっている一重結合の向きを`/`、`\`で表すことで[シス-トランス異性体](https://ja.wikipedia.org/wiki/シス-トランス異性体 "wikilink")を区別する。たとえば`C/C=C\C`、`C/C=C/C`はそれぞれシス・トランス[2-ブテン](https://ja.wikipedia.org/wiki/2-ブテン "wikilink")である。結合がないことは`.`で表現される（たとえば[過酸化水素](../Page/過酸化水素.md "wikilink")`OO`に対し`O.O`は水2分子）。

環構造ではつながっている原子の後ろに数字でラベル付けする。たとえば[プロパン](https://ja.wikipedia.org/wiki/プロパン "wikilink")と[シクロプロパン](../Page/シクロプロパン.md "wikilink")をSMILESで表すとそれぞれ`CCC`、 `C1CC1`となる。ペアが現れて既に環を形成したラベルを再利用してもよい。ラベルは一桁の数字とみなされ、たとえば`C12`はラベル`1`、`2`につながっている炭素である。二桁のラベルを表すには`%`を前置する（たとえば`C%12`はラベル`12`）。

[芳香環](https://ja.wikipedia.org/wiki/芳香環 "wikilink")を構成する原子（[炭素](../Page/炭素.md "wikilink")だけでなく[窒素](../Page/窒素.md "wikilink")、[酸素](../Page/酸素.md "wikilink")なども）は小文字にする。例えば[シクロヘキサン](../Page/シクロヘキサン.md "wikilink")`C1CCCCC1`に対し[ベンゼン](../Page/ベンゼン.md "wikilink")は`c1ccccc1`である。芳香環の結合を一重・二重結合で表すこと（たとえば`C1=CC=CC=C1`）を[ケクレ化](../Page/アウグスト・ケクレ.md "wikilink") () とよぶ。

不斉中心には`@`または`@@`を後置し、[根の方向から見てそれぞれ左回り](../Page/木_\(数学\).md "wikilink")・右回りに後続の原子団が並んでいることを表す（@が左回りのため）。たとえば*S*-[アラニン](../Page/アラニン.md "wikilink")のSMILESは、[アミノ基を根にすると](../Page/アミノ基転移酵素.md "wikilink")`N[C@@H](C)C(=O)O`である（`N[C@@]([H])(C)C(=O)O`のように書いてもよい）。

ある系についてのSMILESは必ずしも一意に定まらず、たとえば*S*-アラニンは上のSMILESだけでなく、`C[C@H](N)C(=O)O`、`C[C@@H](C(=O)O)N`、`OC(=O)[C@H](C)N`などでも表すことができる。そのため、あるアルゴリズムに基づいて系に対し一意になるよう変換したものを、正規化された（）SMILESと呼ぶ。ただし、データベースやプログラムによってはアルゴリズムが違うことがある。

化学反応は`原系>>生成系`または`原系>触媒など>生成系`で表される。たとえば[プロペン](https://ja.wikipedia.org/wiki/プロペン "wikilink")に水が付加して[プロパン-2-オールができる反応は](../Page/2-プロパノール.md "wikilink")`CC=C.O>>CC(O)C`である。

詳細については\[1\]や\[2\]を参照すること。

## 発展

**SMARTS**\[3\]は部分構造検索ができるようにSMILESを拡張したものであり、[化学データベース](https://ja.wikipedia.org/wiki/化学データベース "wikilink")検索プログラムなどで使用される。原子ならびに結合についてのクエリが追加されており、たとえば`[C,c]`は任意の（[脂肪族](https://ja.wikipedia.org/wiki/脂肪族 "wikilink")または[芳香族](https://ja.wikipedia.org/wiki/芳香族 "wikilink")の）炭素にマッチする。

**SMIRKS**\[4\]はSMILESとSMARTSのハイブリッドで、一般的な化学反応を記述する。

## 特徴

SMILES記法の長所は化学構造を、少ないバイト長で表現できることと、ルールが簡単なので人間が文字列に変換する際に複雑な演算が不必要な点にある。

一方、欠点としては元の構造式の向きや置換基が張り出す方向などの構造式を目で見たときの印象が完全に失われる点がある。ほかにも、標準SMILES記法では相対配置も絶対配置も表現することができない。

## 実例


{|align="center" border="1" cellpadding="7" cellspacing="0" style="border:1px solid \#AAAAAA;border-collapse:collapse; font-family:Courier New; font-size:12px" |-bgcolor="khaki" \!分子||構造||SMILES記法 |----- |[窒素](../Page/窒素.md "wikilink") |N≡N |N\#N |----- |[イソシアン酸メチル](../Page/イソシアン酸メチル.md "wikilink") (MIC) |CH<sub>3</sub>N=C=O |CN=C=O |----- |[硫酸銅(II)](https://ja.wikipedia.org/wiki/硫酸銅\(II\) "wikilink") |Cu<sup>2+</sup> SO4<sup>2-</sup> |\[Cu+2\].\[O-\]S(=O)(=O)\[O-\] |----- |[エナントトキシン](https://ja.wikipedia.org/wiki/エナントトキシン "wikilink") (C<sub>17</sub>H<sub>22</sub>O<sub>2</sub>) |[180px](https://ja.wikipedia.org/wiki/ファイル:Oenanthotoxin-structure.png "wikilink") |CCC\[C@@H\](O)CC\\C=C\\C=C\\C\#CC\#C\\C=C\\CO |----- |[ピレトリン](https://ja.wikipedia.org/wiki/ピレトリン "wikilink") II (C<sub>21</sub>H<sub>28</sub>O<sub>5</sub>) |[180px](https://ja.wikipedia.org/wiki/ファイル:Pyrethrin-II-2D-skeletal.svg "wikilink") |COC(=O)C(\\C)=C\\C1C(C)(C)\[C@H\]1C(=O)O\[C@@H\]2C(C)=C(C(=O)C2)CC=CC=C |----- |[アフラトキシンB<sub>1</sub>](https://ja.wikipedia.org/wiki/アフラトキシンB1 "wikilink") (C<sub>17</sub>H<sub>12</sub>O<sub>6</sub>) |[130px](https://ja.wikipedia.org/wiki/ファイル:Aflatoxin_B1.svg "wikilink") |O1C=C\[C@H\](\[C@H\]1O2)c3c2cc(OC)c4c3OC(=O)C5=C4CCC(=O)5 |----- |[グルコース](../Page/グルコース.md "wikilink") (glucose, glucopyranose) (C<sub>6</sub>H<sub>12</sub>O<sub>6</sub>) |[140px](https://ja.wikipedia.org/wiki/ファイル:Beta-D-Glucose.svg "wikilink") |OC\[C@@H\](O1)\[C@@H\](O)\[C@H\](O)\[C@@H\](O)\[C@@H\](O)1 |----- |[クスクチン](https://ja.wikipedia.org/wiki/クスクチン "wikilink")又の名ベルゲニン(天然樹脂) (C<sub>14</sub>H<sub>16</sub>O<sub>9</sub>) |[130px](https://ja.wikipedia.org/wiki/ファイル:Cuscutine.svg "wikilink") |OC\[C@@H\](O1)\[C@@H\](O)\[C@H\](O)\[C@@H\]2\[C@@H\]1c3c(O)c(OC)c(O)cc3C(=O)O2 |----- |[カリフォルニア](https://ja.wikipedia.org/wiki/カリフォルニア "wikilink")州の[カイガラムシ](../Page/カイガラムシ.md "wikilink")の[フェロモン](../Page/フェロモン.md "wikilink") |[180px](https://ja.wikipedia.org/wiki/ファイル:Pheromone_cochenille_californienne.svg "wikilink") |CC(=O)OCCC(/C)=C\\C\[C@H\](C(C)=C)CCC=C |----- |2S,5R-[カルコガラン](https://ja.wikipedia.org/wiki/カルコガラン "wikilink"):[キクイムシ](../Page/キクイムシ.md "wikilink")（ホシガタキクイムシ(Pityogenes chalcographus)）の[フェロモン](../Page/フェロモン.md "wikilink") \[5\] |[130px](https://ja.wikipedia.org/wiki/ファイル:2S,5R-chalcogran-skeletal.svg "wikilink") |CC\[C@H\](O1)CC\[C@@\]12CCCO2 |----- |[バニリン](../Page/バニリン.md "wikilink") |[70px](https://ja.wikipedia.org/wiki/ファイル:Vanillin.png "wikilink") |O=Cc1ccc(O)c(OC)c1 |----- |[メラトニン](../Page/メラトニン.md "wikilink") (C<sub>13</sub>H<sub>16</sub>N<sub>2</sub>O<sub>2</sub>) |[160px](https://ja.wikipedia.org/wiki/ファイル:Melatonin2.svg "wikilink") |CC(=O)NCCC1=CNc2c1cc(OC)cc2 |----- |[フラボペレイリン](https://ja.wikipedia.org/wiki/フラボペレイリン "wikilink") (C<sub>17</sub>H<sub>15</sub>N<sub>2</sub>) |[160px](https://ja.wikipedia.org/wiki/ファイル:Flavopereirine.svg "wikilink") |CCc(c1)ccc2\[n+\]1ccc3c2Nc4c3cccc4 |----- |[ニコチン](../Page/ニコチン.md "wikilink") (C<sub>10</sub>H<sub>14</sub>N<sub>2</sub>) |[80px](https://ja.wikipedia.org/wiki/ファイル:Nicotine.svg "wikilink") |CN1CCC\[C@H\]1c2cccnc2 |----- |[ツジョン](../Page/ツジョン.md "wikilink") (C<sub>10</sub>H<sub>16</sub>O) |[100px](https://ja.wikipedia.org/wiki/ファイル:Alpha-thujone.svg "wikilink") |CC(C)\[C@@\]12C\[C@@H\]1\[C@@H\](C)C(=O)C2 |----- |[チアミン](../Page/チアミン.md "wikilink") (C<sub>12</sub>H<sub>17</sub>N<sub>4</sub>OS<sup>+</sup>)
(vitamine B1) |[150px](https://ja.wikipedia.org/wiki/ファイル:Thiamin.svg "wikilink") |OCCc1c(C)\[n+\](=cs1)Cc2cnc(C)nc(N)2 |}

## 脚注

## 関連項目

  - [化学データベース](https://ja.wikipedia.org/wiki/化学データベース "wikilink")

## 外部リンク

  - SMILES の教本, <http://www.daylight.com/smiles/smiles-intro.html>
  - SMILES文字列を2次元画像に変換する機能を持ったWebを使ったアプリケーション
      - <http://www.daylight.com/daycgi/depict>
      - <http://cactus.nci.nih.gov/services/gifcreator/> 種々の調節項目を持ったコンバーター
  - SMILESを生成する機能を持った分子エディター・アプレット, <http://www.molinspiration.com/jme/index.html>
  - SMILES文法チェック, <http://www.dalkescientific.com/writings/diary/archive/>
  - SMILES変換フリーウェア, <http://www.acdlabs.com/download/chemsk.html>
  - SMILES用三次元分子ビューアー, <http://jmol.sourceforge.net/>
  - [Happy Atom](http://diesel.ins.cwi.nl:8080/happyatom/show/HomePage): このプロジェクトでは、 正規化圧縮距離のアイデアをSSMILES言語 と SMILES言語に使って開発している。
  - [E-BABEL](http://www.vcclab.org/lab/babel) [OpenBabel](https://ja.wikipedia.org/wiki/OpenBabel "wikilink") に基づく分子の相互転換

[Category:化学データベース](https://ja.wikipedia.org/wiki/Category:化学データベース "wikilink") [Category:ケモインフォマティクス](https://ja.wikipedia.org/wiki/Category:ケモインフォマティクス "wikilink")

1.
2.
3.
4.
5.  [ISOLATION OF PHEROMONE SYNERGISTS OF BARK BEETLE, Pityogenes chalcographus, FROM COMPLEX INSECT-PLANT ODORS BY FRACTIONATION AND SUBTRACTIVE-COMBINATION BIOASSAY](http://www.chemical-ecology.net/pdf/Byersetal1990a.pdf)