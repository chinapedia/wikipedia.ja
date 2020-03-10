> この記事は[Jess](https://ja.wikipedia.org/wiki/Jess)から翻訳されています。


**Jess**は[Java](https://ja.wikipedia.org/wiki/Java "wikilink")プラットフォーム向けの[ルールエンジンである](../Page/推論エンジン.md "wikilink")。[CLIPS](../Page/CLIPS.md "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")の上位互換であり、[サンディア国立研究所](https://ja.wikipedia.org/wiki/サンディア国立研究所 "wikilink")の Ernest Friedman-Hill が開発した。[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")末ごろ最初の版が完成した。

[エキスパートシステム](../Page/エキスパートシステム.md "wikilink")開発自動化に適したルールベースのプログラミング言語であり、しばしば「エキスパートシステム・シェル」と呼ばれる。近年、[知的エージェント](https://ja.wikipedia.org/wiki/知的エージェント "wikilink")と呼ばれるシステムも開発されているが、それと同様の機能を持つ。

Jess は手続き型パラダイムではなく宣言型パラダイムであり、「パターンマッチング」と呼ばれる処理によって規則群を事実群に適用する。規則は事実群に変更を加えたり、何らかの Java コードを実行したりする。

Jess は、宣言型規則の形で知識を使って結論や推論を導くタイプの Java の[アプレット](https://ja.wikipedia.org/wiki/アプレット "wikilink")やアプリケーションを構築するのに使える。多くの規則が多くの入力にマッチするが、効果的な汎用マッチングアルゴリズムは少ない。Jessのルールエンジンは[Reteアルゴリズム](../Page/Reteアルゴリズム.md "wikilink")を使用している。

なお、オープンソースではない。

## コード例

` ; これはコメント`

`(bind ?x 100)`

`; x = 100`

`(deffunction max (?a ?b)`
`  (if (> ?a ?b) then ?a else ?b))`

`(deffacts myroom`
`   (furniture chair)`
`   (furniture table)`
`   (furniture bed)`
`)`

`(deftemplate car`
`   (slot color)`
`   (slot mileage)`
`   (slot value)`
`)`

`(assert (car (color red) (mileage 10000) (value 400)))`

`(clear)`
`(deftemplate blood-donor (slot name) (slot type))`
`(deffacts blood-bank ; 名前と血液型をワーキングメモリに置く`
`      (blood-donor (name "Alice")(type "A"))`
`      (blood-donor (name "Agatha")(type "A"))`
`      (blood-donor (name "Bob")(type "B"))`
`      (blood-donor (name "Barbara")(type "B"))`
`      (blood-donor (name "Jess")(type "AB"))`
`      (blood-donor (name "Karen")(type "AB"))`
`      (blood-donor (name "Onan")(type "O"))`
`      (blood-donor (name "Osbert")(type "O"))`
`)`
`(defrule can-give-to-same-type-but-not-self ; A>A, B>B, O>O, AB>AB をカバー。ただし同一人による輸血は不可`
`      (blood-donor (name ?name)(type ?type))`
`      (blood-donor (name ?name2)(type ?type2 &:(eq ?type ?type2) &: (neq ?name ?name2)  ))`
`      =>`
`      (printout t ?name " can give blood to " ?name2 crlf)`
`)`
`(defrule O-gives-to-others-but-not-itself ; O型からO型は上の規則でカバー`
`      (blood-donor (name ?name)(type ?type &:(eq ?type "O")))`
`      (blood-donor (name ?name2)(type ?type2 &: (neq ?type ?type2) &: (neq ?name ?name2)  ))`
`      =>`
`      (printout t ?name " can give blood to " ?name2 crlf)`
`)`
`(defrule A-or-B-gives-to-AB ; O型からAB型、AB型からAB型は既にカバーされている`
`      (blood-donor (name ?name)(type ?type &:(or (eq ?type "A") (eq ?type "B" ))))`
`      (blood-donor (name ?name2)(type ?type2 &: (eq ?type2 "AB")  &: (neq ?name ?name2)  ))`
`      =>`
`      (printout t ?name " can give blood to " ?name2 crlf)`
`)`
`;(watch all)`
`(reset)`
`(run)`

## 書籍

  - Jess in Action - ISBN 1-930110-89-8

## 外部リンク

  - [Official Website](http://www.jessrules.com/)（英語）

[Category:エキスパートシステム](https://ja.wikipedia.org/wiki/Category:エキスパートシステム "wikilink")