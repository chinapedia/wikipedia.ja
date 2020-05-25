> この記事は[RC \(野球\)](https://ja.wikipedia.org/wiki/RC_\(野球\))から翻訳されています。


**RC**(*Runs Created*)とは、[野球](../Page/野球.md "wikilink")において[打者](../Page/打者.md "wikilink")を評価する指標の一つ。[メジャーリーグベースボール](https://ja.wikipedia.org/wiki/メジャーリーグベースボール "wikilink")における[セイバーメトリクス](../Page/セイバーメトリクス.md "wikilink")の第一人者[ビル・ジェームズ](https://ja.wikipedia.org/wiki/ビル・ジェームズ "wikilink")により考案された個人の得点能力を表す総合指標の一つ。

## 概要

過去に生まれた[打率](../Page/打率.md "wikilink")や[本塁打](../Page/本塁打.md "wikilink")などの指標はそれぞれ独立した指標であり、お互いを比較することが困難であった。打率を例にしてみると、[安打](https://ja.wikipedia.org/wiki/安打 "wikilink")と本塁打が同じ価値であったり、[四球](../Page/四球.md "wikilink")は[投手](../Page/投手.md "wikilink")の完全なるミスという理由で無価値とみなされるなど欠陥も多かった。RCはそんな古来の指標に変わる新たな指標として開発された。

当初は出塁率に塁打数を掛けるだけのシンプルな指標だったが、盗塁や犠打、犠飛などの要素を加えたり、実際の得点から逆算して係数を求めるなど常に得点との相関性を高める改良が加えられ、さまざまなバリエーションが存在する。また、これを更に改良したものがXRである。

チームの全打者のRCを合計すると、シーズン中のチームの総得点とほぼ一致するように式が作られている。

### RC

RCは何度か改良が加えられたが、この指標の基本は**（出塁能力A × 進塁能力B）/ 出塁機会C**を基に構成されている。

  -
    A = [安打](https://ja.wikipedia.org/wiki/安打 "wikilink") + [四球](../Page/四球.md "wikilink") + [死球](../Page/死球.md "wikilink") - [盗塁](../Page/盗塁.md "wikilink")死 - [併殺打](https://ja.wikipedia.org/wiki/併殺打 "wikilink")
    B = [塁打](../Page/塁打.md "wikilink") + 0.26 ×（[四球](../Page/四球.md "wikilink") + [死球](../Page/死球.md "wikilink")） + 0.53 ×（[犠飛](https://ja.wikipedia.org/wiki/犠飛 "wikilink") + [犠打](../Page/犠打.md "wikilink")） + 0.64 × [盗塁](../Page/盗塁.md "wikilink") - 0.03 × [三振](https://ja.wikipedia.org/wiki/三振 "wikilink")
    C = [打数](../Page/打数.md "wikilink") + [四球](../Page/四球.md "wikilink") + [死球](../Page/死球.md "wikilink") + [犠飛](https://ja.wikipedia.org/wiki/犠飛 "wikilink") + [犠打](../Page/犠打.md "wikilink")

    \(RC = \left ( \frac{(A+2.4C)\;(B+3C)}{9C} \right ) - 0.9C\)


同じ得点との相関を示した[OPSなどより難解な計算方法となっているが](../Page/OPS_\(野球\).md "wikilink")、OPSの欠陥として指摘されていた走塁能力（[盗塁](../Page/盗塁.md "wikilink")）を考慮したため、より正確な得点能力を算出できるようになった。これによってリードオフマンとパワーヒッターなどの全くタイプ・役割の違う選手同士を平等に比較できるようになった。
RCはチームの他選手や打順に左右される打点や得点を補正する点では優れているが、その性質上打席が多いほど大きくなる傾向があり、打席数の大きく異なる選手を比較することには向いていない。そのため、RCを応用し打席数を均等化した指標としてRC27が使われることがある。

### RC27

**RC27**(*Runs Created per 27 outs*)はRCを元にある特定の選手1人で構成された打線で試合を行った場合、27アウト（9イニング×3アウト=1試合）で平均何点とれるかを算出した指標。
この数値が大きいほど、その選手の総合的な得点能力が優れているとされる。
ただし、欠陥として場合によってはマイナス値になることがある。\[1\]
:TO = [打数](../Page/打数.md "wikilink") - [安打](https://ja.wikipedia.org/wiki/安打 "wikilink") + [犠打](../Page/犠打.md "wikilink") + [犠飛](https://ja.wikipedia.org/wiki/犠飛 "wikilink") + [盗塁死](https://ja.wikipedia.org/wiki/盗塁死 "wikilink") + [併殺打](https://ja.wikipedia.org/wiki/併殺打 "wikilink")

\[RC27 = \frac{27RC}{TO}\]

### RCAA (RC+)

平均的な打者と比較して増やしたRCを**RCAA** (**R**uns **C**reated **A**bove **A**verage)、あるいはRC+と呼ぶ。

  -
    PA = 打席数
    lg = リーグ全体

    \(RCAA = RC - \left ( \frac{lgRC}{lgPA} \right )\times PA\)

### RCWIN

RCAAを勝利数に変換したものを**RCWIN**と呼ぶ。RCAAは単位がRC (≒得点)だが、リーグやシーズンによって1点の価値は必ずしも等しくない。平均得点が異なるリーグでは1勝あたりの平均得点(失点)も異なるため、得点の価値に差が出てしまう。そこで1勝あたりに必要な得点を表すRuns Per Win (RPW)を導入し、RCAAを勝利数に変換することで異なる時代やリーグ間での比較が可能となる。

  -
    RPW = 10×√{(リーグ得点＋リーグ失点)/リーグ投球回}

    \(RCWIN = \frac{RCAA}{RPW}\)

## NPB記録

### シーズンRC27

| 順位 | 選手名                                                                       | 所属球団(記録当時)                                                          | RC27  | 記録年                                                     |
| -- | ------------------------------------------------------------------------- | ------------------------------------------------------------------- | ----- | ------------------------------------------------------- |
| 1  | [王貞治](../Page/王貞治.md "wikilink")                                          | [読売ジャイアンツ](https://ja.wikipedia.org/wiki/読売ジャイアンツ "wikilink")       | 14.98 | [1974年](../Page/1974年.md "wikilink")                    |
| 2  | 王貞治                                                                       | 読売ジャイアンツ                                                            | 14.02 | [1973年](../Page/1973年.md "wikilink")                    |
| 3  | [ランディ・バース](../Page/ランディ・バース.md "wikilink")                                | [阪神タイガース](../Page/阪神タイガース.md "wikilink")                            | 13.87 | [1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink") |
| 4  | [アレックス・カブレラ](../Page/アレックス・カブレラ.md "wikilink")                            | [西武ライオンズ](https://ja.wikipedia.org/wiki/埼玉西武ライオンズ "wikilink")       | 13.15 | [2002年](../Page/2002年.md "wikilink")                    |
| 5  | 王貞治                                                                       | 読売ジャイアンツ                                                            | 13.00 | [1966年](../Page/1966年.md "wikilink")                    |
| 6  | [落合博満](../Page/落合博満.md "wikilink")                                        | [ロッテオリオンズ](../Page/千葉ロッテマリーンズ.md "wikilink")                        | 12.94 | [1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink") |
| 7  | 落合博満                                                                      | ロッテオリオンズ                                                            | 12.84 | 1986年                                                   |
| 8  | 王貞治                                                                       | 読売ジャイアンツ                                                            | 12.64 | [1967年](../Page/1967年.md "wikilink")                    |
| 9  | 王貞治                                                                       | 読売ジャイアンツ                                                            | 12.63 | [1968年](https://ja.wikipedia.org/wiki/1968年 "wikilink") |
| 10 | 王貞治                                                                       | 読売ジャイアンツ                                                            | 12.52 | [1976年](../Page/1976年.md "wikilink")                    |
| 11 | [松中信彦](https://ja.wikipedia.org/wiki/松中信彦 "wikilink")                     | [福岡ダイエーホークス](https://ja.wikipedia.org/wiki/福岡ソフトバンクホークス "wikilink") | 12.43 | [2004年](../Page/2004年.md "wikilink")                    |
| 12 | 王貞治                                                                       | 読売ジャイアンツ                                                            | 12.12 | [1969年](https://ja.wikipedia.org/wiki/1969年 "wikilink") |
| 13 | 王貞治                                                                       | 読売ジャイアンツ                                                            | 12.08 | [1965年](../Page/1965年.md "wikilink")                    |
| 14 | 王貞治                                                                       | 読売ジャイアンツ                                                            | 12.07 | [1970年](../Page/1970年.md "wikilink")                    |
| 15 | [ウラディミール・バレンティン](https://ja.wikipedia.org/wiki/ウラディミール・バレンティン "wikilink") | [東京ヤクルトスワローズ](https://ja.wikipedia.org/wiki/東京ヤクルトスワローズ "wikilink") | 12.06 | [2013年](../Page/2013年.md "wikilink")                    |
| 16 | [張本勲](../Page/張本勲.md "wikilink")                                          | [東映フライヤーズ](../Page/北海道日本ハムファイターズ.md "wikilink")                     | 11.97 | 1970年                                                   |
| 17 | [大下弘](../Page/大下弘.md "wikilink")                                          | 東急フライヤーズ                                                            | 11.92 | [1951年](https://ja.wikipedia.org/wiki/1951年 "wikilink") |
| 18 | [松井秀喜](https://ja.wikipedia.org/wiki/松井秀喜 "wikilink")                     | 読売ジャイアンツ                                                            | 11.79 | [2002年](../Page/2002年.md "wikilink")                    |
| 19 | 落合博満                                                                      | [中日ドラゴンズ](../Page/中日ドラゴンズ.md "wikilink")                            | 11.69 | [1991年](../Page/1991年.md "wikilink")                    |
| 20 | 王貞治                                                                       | 読売ジャイアンツ                                                            | 11.68 | [1977年](../Page/1977年.md "wikilink")                    |
|    |                                                                           |                                                                     |       |                                                         |

### 通算RCWIN

| 順位 | 選手名                                                      | RCWIN  |
| -- | -------------------------------------------------------- | ------ |
| 1  | 王貞治                                                      | 142.20 |
| 2  | 張本勲                                                      | 85.09  |
| 3  | [長嶋茂雄](../Page/長嶋茂雄.md "wikilink")                       | 76.13  |
| 4  | 落合博満                                                     | 62.80  |
| 5  | [野村克也](../Page/野村克也.md "wikilink")                       | 61.21  |
| 6  | [門田博光](../Page/門田博光.md "wikilink")                       | 53.42  |
| 7  | [榎本喜八](https://ja.wikipedia.org/wiki/榎本喜八 "wikilink")    | 52.23  |
| 8  | [山本浩二](../Page/山本浩二.md "wikilink")                       | 51.02  |
| 9  | [金本知憲](https://ja.wikipedia.org/wiki/金本知憲 "wikilink")    | 47.56  |
| 10 | |[小笠原道大](https://ja.wikipedia.org/wiki/小笠原道大 "wikilink") | |45.55 |
|    |                                                          |        |

  - 1955年以降の選手対象（1954年以前の成績は概算値となるため）
  - 1954年から規定打席に到達し、キャリアのほとんどにおいて十分な記録が得られている選手として[山内一弘](../Page/山内一弘.md "wikilink")がおり、概算値を含めた場合は65.68となり歴代4位に位置する。また同様に概算値を含めた場合、野村と門田に挟まれて[川上哲治](../Page/川上哲治.md "wikilink")が58.34となり7位に入る。

### シーズンRCWIN

| 順位 | 選手名                                        | 所属球団(記録当時)                                                    | RCWIN | 記録年                                                     |
| -- | ------------------------------------------ | ------------------------------------------------------------- | ----- | ------------------------------------------------------- |
| 1  | [王貞治](../Page/王貞治.md "wikilink")           | [読売ジャイアンツ](https://ja.wikipedia.org/wiki/読売ジャイアンツ "wikilink") | 10.98 | [1973年](../Page/1973年.md "wikilink")                    |
| 2  | 王貞治                                        | 読売ジャイアンツ                                                      | 9.72  | [1966年](../Page/1966年.md "wikilink")                    |
| 3  | 王貞治                                        | 読売ジャイアンツ                                                      | 9.65  | [1965年](../Page/1965年.md "wikilink")                    |
| 4  | 王貞治                                        | 読売ジャイアンツ                                                      | 9.48  | [1970年](../Page/1970年.md "wikilink")                    |
| 5  | 王貞治                                        | 読売ジャイアンツ                                                      | 9.13  | [1964年](../Page/1964年.md "wikilink")                    |
| 6  | 王貞治                                        | 読売ジャイアンツ                                                      | 9.03  | [1968年](https://ja.wikipedia.org/wiki/1968年 "wikilink") |
| 7  | 王貞治                                        | 読売ジャイアンツ                                                      | 9.02  | 1974年                                                   |
| 8  | 王貞治                                        | 読売ジャイアンツ                                                      | 8.95  | [1965年](../Page/1965年.md "wikilink")                    |
| 9  | 王貞治                                        | 読売ジャイアンツ                                                      | 8.88  | [1967年](../Page/1967年.md "wikilink")                    |
| 10 | [ランディ・バース](../Page/ランディ・バース.md "wikilink") | [阪神タイガース](../Page/阪神タイガース.md "wikilink")                      | 8.83  | [1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink") |
|    |                                            |                                                               |       |                                                         |

  - [2017年](../Page/2017年.md "wikilink")終了時点

## 脚注

## 関連項目

  - [野球の各種記録](../Page/野球の各種記録.md "wikilink")
  - [セイバーメトリクス](../Page/セイバーメトリクス.md "wikilink")
  - [OPS](../Page/OPS_\(野球\).md "wikilink")

[Category:セイバーメトリクス](https://ja.wikipedia.org/wiki/Category:セイバーメトリクス "wikilink") [Category:バッティング_(野球)](https://ja.wikipedia.org/wiki/Category:バッティング_\(野球\) "wikilink")

1.  無安打の場合など。http://baseballdata.jp/playerB/900082_2.html