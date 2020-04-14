> この記事は[DIPS \(野球\)](https://ja.wikipedia.org/wiki/DIPS_\(野球\))から翻訳されています。


**DIPS**（ディーアイピーエス）はDefense Independent Pitching Statisticsの略で、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")でが提唱した、守備の影響とは独立に投手の成績を評価するという概念及びその評価手法である。

マクラッケンが考案したDIPSのコンセプトは、投手の成績を「投手自身でコントロールできる部門」と「投手自身ではコントロールできない部門」に分けて、「投手自身でコントロールできる部門」だけで投手を評価することである\[1\]。「投手の[インプレイ](https://ja.wikipedia.org/wiki/インプレイ "wikilink")打率（[BABIP](https://ja.wikipedia.org/wiki/BABIP_\(野球\) "wikilink")）はシーズンごとの一貫性がない」という事実の発見から、失点の増減には野手の守備と運の要素が大きくかかわると考えた。そこでインプレイの要素を最初から無視し、投手のみに責任がある要素である[奪三振](https://ja.wikipedia.org/wiki/三振 "wikilink")、[与四球](../Page/四球.md "wikilink")、[被本塁打から投手を評価しようとする考え方がDIPSである](../Page/本塁打.md "wikilink")。

## 概要

DIPSが定義する「投手自身ではコントロールできない部門」とは[勝利](../Page/勝利投手.md "wikilink")、[敗戦](../Page/敗戦投手.md "wikilink")、勝率など（いずれも、味方打線や救援投手の影響を大きく受ける）と同時に、[被安打や](https://ja.wikipedia.org/wiki/安打 "wikilink")[自責点](../Page/自責点.md "wikilink")、[防御率](../Page/防御率.md "wikilink")も入る。これらは主に守っている野手の影響が大きく関与するが、その野手の違いを数値化するのが極めて難しいので、最初から無視してしまうのがDIPSのコンセプトとなっている。

一方で、「投手自身でコントロールできる部門」とは、野手が関与しない[奪三振](https://ja.wikipedia.org/wiki/三振 "wikilink")、[与四球](../Page/四球.md "wikilink")、[被本塁打の三部門であり](../Page/本塁打.md "wikilink")、DIPSで投手を順位付けをする場合は基本的にこの三部門によって行われる。近年では[ゴロ](../Page/ゴロ.md "wikilink")や[フライ](../Page/フライ.md "wikilink")の割合も投手がコントロールしやすい事が判明し、DIPSの評価に組み込まれている。

元来、投手の責任とされていた、被安打や自責点の増減を「守っている野手の影響が大きく、投手の責任とはできない」としたDIPSのコンセプトはアメリカの[セイバーメトリクス](../Page/セイバーメトリクス.md "wikilink")の間で大きな議論を巻き起こした。

## DIPSに基づいた指標

### FIP

DIPSを簡潔に算出するような公式というのは存在せず、個々の項目を補正しながら算出した値を回帰的に積み重ねて答えにいたる方式であるが、簡易版として、[カナダ](https://ja.wikipedia.org/wiki/カナダ "wikilink")の[トム・タンゴ](https://ja.wikipedia.org/wiki/トム・タンゴ "wikilink")（[Tom Tango](https://ja.wikipedia.org/wiki/:en:Tom_Tango "wikilink")）は、**FIP** (**F**ielding **I**ndependent **P**itching)を提唱している。FIPの係数は[得点価値を基に算出されている](https://ja.wikipedia.org/wiki/Linear_Weights#得点期待値 "wikilink")。

  -
    HR = 本塁打　Home Run
    uBB = 四球 - 敬遠　unintentional Base on Balls (故意でない四球)
    HBP = 死球　Hit By Pitch
    SO = 奪三振　StrikeOut
    IP = 投球回　Inning Pitched
    Constant = 定数(補正値)
    ERA = 防御率　Earned Run Average
    lg = リーグ全体　League

\[\begin{align}
FIP & = \frac{\{13\times HR + 3\times \left ( uBB + HBP \right ) - 2\times SO \}}{IP} + Constant
\\
Constant & = lgERA - \frac{\{13\times lgHR + 3\times \left ( lguBB + lgHBP \right ) - 2\times lgSO \}}{lgIP}
\,
\end{align}\]

  - **FIP={13×被本塁打+3×（与四球+与死球-敬遠）-2×奪三振}÷投球回+リーグごとの補正値**

<!-- end list -->

  -
    **補正値：リーグ全体の防御率-{13×被本塁打+3×（与四球+与死球-敬遠）-2×奪三振}÷投球回**

通算のFIPと防御率は近い値になる傾向があり、BABIPの影響を受けないFIPは防御率より安定度が高い。そのため、FIPは翌年の防御率を予測する際に参考となる\[2\]。

### xFIP

投球回が多ければ投手ごとに[フライボールあたりの本塁打の割合はほぼ一定の範囲に収束するという性質により](https://ja.wikipedia.org/wiki/Batted_Ball_#HR/FB "wikilink")、打たれたフライボールに一定の本塁打を見込んでFIPを計算するのがxFIPである\[3\]。 なおフライボールとは外野フライ（アウト）、内野フライ（アウト）、本塁打、単打などの打席結果にかかわらず全てのフライ性の打球のことをいう。

  - **xFIP={13×（フライボール×リーグ全体のフライボールに対する本塁打の割合）+3×（与四球+与死球）-2×奪三振}÷投球回+リーグごとの補正値**

<!-- end list -->

  -
    **補正値：リーグ全体の\[防御率-{13×被本塁打+3×（与四球+与死球-敬遠）-2×奪三振}÷投球回\]**

なお、NPBのxFIPを算出しているベースボールラボではフライボールではなく外野フライを用いるとしている\[4\]。

### DIPS2.0

マクラッケンはその後の研究で、DIPS2.0と呼ばれる改良式を提示した。この式では、変化球投手の評価精度を高めるほかに、[BABIP](https://ja.wikipedia.org/wiki/BABIP_\(野球\) "wikilink")（ホームラン・三振以外での打率）との相関性を追求している。しかし、公式成績に出ていない指標と小数の係数を多く含めているため、計算が煩雑になっている。

  - **DIPS2.0={フェアフライによるアウト数×（-0.041）+ゴロによるアウト数×0.05+ファウルフライによるアウト数×0.251+ライナーによるアウト数×0.224+与四球数×0.316+与死球数×0.43-奪三振数×0.12}÷投球回数×9**

### tERA(tRA)

グラハム・マカリーは今までDIPSで排除されていたインプレーの打球について、ゴロやフライ等の打球別に分類して評価に加えた**tRA** (**T**rue **R**uns **A**llowed)を考案した\[5\] \[6\]。まず[Linear Weightsによって各打球の得点価値とアウト期待値を算出し](https://ja.wikipedia.org/wiki/Linear_Weights "wikilink")、打球の発生数と掛け合わせる事で平均的な守備力のチームで投げた場合の仮想的な失点とアウト数を計算する。この2つを用いてtRAは以下の式で表される。

  - **tRA=仮想的な失点÷(仮想的なアウト数×27)**

**　　　　　=\[Σ(各要素の得点価値×各要素の数)\]÷\[奪三振＋Σ(各打球のアウト期待値×各打球の数)\]÷27**

tRAの計算に含まれる要素は奪三振、与四死球、被本塁打、打球(ゴロ、内野フライ、外野フライ、ライナー)である。
tRAに自責点と失点の比率を掛ければ防御率ベースのtERAとなる。

### SIERA

奪三振や与四球、ゴロの相互作用を取り入れて対戦打者数ベースで評価を行うなど\[7\]、より高い精度で投手の能力を反映させた**SIERA** (**S**kill-**I**nteractive **E**arned **R**un **A**verage)が提唱されている\[8\]。相互作用の例として、ゴロ率が高い投手は与四球が多くても併殺機会が増えるため、四球の影響がFIPで見込まれるほど大きく作用しないといった効果がある\[9\]。SIERAはxFIP以上の精度で防御率を推定できるが、計算方法は非常に煩雑で導出過程も複雑である。そのため作用している能力を分けて考える事が難しく、FIPやxFIP等と合わせてバランスよく見る事が推奨されている\[10\]。

## 脚注

## 関連項目

  - [野球の各種記録](../Page/野球の各種記録.md "wikilink")
  - [PECOTA](https://ja.wikipedia.org/wiki/PECOTA "wikilink")

## 外部リンク

  - [FanGraphs Library Stat Glossary](http://www.fangraphs.com/library/) FanGraphs
  - [用語集](http://archive.baseball-lab.jp/glossary/)Baseball LAB「Archives」

[Category:セイバーメトリクス](https://ja.wikipedia.org/wiki/Category:セイバーメトリクス "wikilink") [Category:ピッチング](https://ja.wikipedia.org/wiki/Category:ピッチング "wikilink")

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