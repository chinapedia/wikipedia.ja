> この記事は[D \(データベース言語仕様\)](https://ja.wikipedia.org/wiki/D_\(データベース言語仕様\))から翻訳されています。


**D** は、[クリス・デイト](../Page/クリス・デイト.md "wikilink")と[ヒュー・ダーウェン](../Page/ヒュー・ダーウェン.md "wikilink")が著書 (共著) *[The Third Manifesto](../Page/The_Third_Manifesto.md "wikilink")* で提案した、[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")の[データベース言語](../Page/データベース言語.md "wikilink")が満たすべき要件の集合である。 D自体はデータベース言語ではない。 デイトとダーウェンは、2008年現在で広く使われているデータベース言語[SQL](../Page/SQL.md "wikilink")を、[関係モデル](../Page/関係モデル.md "wikilink")を正確に実装していないとして、批判している。

**Tutorial D** は、*The Third Manifesto* で説明され使われている、Dの抽象的な実装である。 Dの実装は、Tutorial D と必ずしも同じ構文である必要はない。 Dを正しく実装するために必要なことは、その実装が、Dで規定された機能のセットをもっていることと、デイトとダーウェンが賢明ではないと考えている機能のセットを排除していることである。 Dの正しい実装は、[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")の範囲外に位置づけられる付加的な機能をもっていても良い。

Dは、[プログラミング言語Dとは関係ない](../Page/D言語.md "wikilink")。 プログラミング言語Dは、汎用的な[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。

## Tutorial D

**Tutorial D** は、*[The Third Manifesto](../Page/The_Third_Manifesto.md "wikilink")* で説明され使われている、Dの抽象的な実装である。 Tutorial D は、Dがどのようなものであるかを示すことを目的としており、また教育用途である。

### 構文

Tutorial D の構文を、[関係代数の](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\) "wikilink")[演算子](../Page/演算子.md "wikilink")ごとに説明する。 なお R と S を[関係とする](https://ja.wikipedia.org/wiki/関係_\(データベース\) "wikilink")。 また A と B を R の[属性とする](https://ja.wikipedia.org/wiki/属性_\(データベース\) "wikilink")。

#### 和

RとSの[和](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\)#和 "wikilink") R ∪ S は、次のように記述する。

`R UNION S`

#### 差

RとSの[差](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\)#差 "wikilink") R － S は、次のように記述する。

`R MINUS S`

#### 交わり

RとSの[交わり](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\)#交わり "wikilink") R ∩ S は、次のように記述する。

`R INTERSECT S`

#### 制限

Rに対する A = 1 を条件とする[制限](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\)#制限 "wikilink") (選択) R\[A = 1\] は、次のように記述する。

`R WHERE A = 1`

#### 射影

Rの[射影](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\)#射影 "wikilink") R\[A,B\] は、次のように記述する。

`R { A, B }`

#### 自然結合

RとSの[自然結合](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\)#自然結合 "wikilink") R \(\bowtie\) S は、次のように記述する。

`R JOIN S`

#### 準結合

RとSの[準結合](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\)#準結合 "wikilink") (半結合) R \(\ltimes\) S は、次のように記述する。

`R MATCHING S`

#### 商

RとSの[商](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\)#商 "wikilink") R ÷ S は、次のように記述する。

`R DIVIDEBY S`

#### 属性名変更

Rの[属性Bをの属性名をXに変更する](https://ja.wikipedia.org/wiki/属性_\(データベース\) "wikilink")[属性名変更](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\)#属性名変更 "wikilink") R\[B→X\] は、次のように記述する。

`R RENAME ( B AS X )`

#### 拡張

Rに B \* 2.54 で計算される値をもつ属性を追加して、その属性の名前をXとする[拡張は](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\)#拡張 "wikilink")、次のように記述する。

`EXPAND R ADD (B * 2.54 AS X)`

#### 要約

Rに対してその属性AとAごとのBの最大値から構成される[関係を生成する](https://ja.wikipedia.org/wiki/関係_\(データベース\) "wikilink")[要約は](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\)#要約 "wikilink")、次のように記述する。

`SUMMARISE R PER ( R{A} ) ADD ( MAX(B) AS X )`

#### Tutorial D が備えていない構文

Tutorial D では、[直積](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\)#直積 "wikilink") (積、デカルト積) は直接サポートされない。

Tutorial D では、[外結合](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\)#外結合 "wikilink") (外部結合) に相当する演算子は存在しない。

## Industrial D

Tutorial D が学術のための言語であるのに対し、実務のために使われるDの正確な実装は **Industrial D** と呼ばれる。

## 実装

Dの最初の実装は D4 であり、[C\#で開発された](../Page/C_Sharp.md "wikilink")。 D4は、Alphora社の[関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink") (RDBMS) Dataphor で[データベース言語](../Page/データベース言語.md "wikilink")として採用されている。 他の実装としては、Rel、Opus、Duro、Dee などがある。 これらの実装はすべて Industrial D と位置づけられている。

## 関連項目

  - [The Third Manifesto](../Page/The_Third_Manifesto.md "wikilink")
  - [関係モデル](../Page/関係モデル.md "wikilink")
      - [関係代数 (関係モデル)](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\) "wikilink")
  - [データベース言語](../Page/データベース言語.md "wikilink")
      - [SQL](../Page/SQL.md "wikilink")

### 人物

  - [クリス・デイト](../Page/クリス・デイト.md "wikilink")
  - [ヒュー・ダーウェン](../Page/ヒュー・ダーウェン.md "wikilink")

## 参考文献

  -
  -
  -
  - <http://www.thethirdmanifesto.com> - [The Third Manifesto](../Page/The_Third_Manifesto.md "wikilink")

## 外部リンク

### Tutorial D

  - <http://www.dcs.warwick.ac.uk/~hugh/> - [ヒュー・ダーウェン](../Page/ヒュー・ダーウェン.md "wikilink")のホームページ ([ウォーリック大学](https://ja.wikipedia.org/wiki/ウォーリック大学 "wikilink")[コンピュータ科学](https://ja.wikipedia.org/wiki/コンピュータ科学 "wikilink")部)
      - [Tutorial D の説明 (英語)](http://www.dcs.warwick.ac.uk/~hugh/TTM/CHAP05.pdf)
      - [Tutorial D の文法 (アルファベット順、英語)](http://www.dcs.warwick.ac.uk/~hugh/TTM/APPXI.pdf)
      - [A New Relational Algebra (英語)](http://www.dcs.warwick.ac.uk/~hugh/TTM/APPXA.pdf) - Tutorial D の基盤となっている新しい[関係代数の体系の説明](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\) "wikilink")

### The Third Manifesto

  - <http://www.thethirdmanifesto.com> - [The Third Manifesto](../Page/The_Third_Manifesto.md "wikilink")

### Dの実装

  - [Alphora](http://www.alphora.com/)
  - [Rel](http://dbappbuilder.sf.net/Rel.html)
  - [Duro](http://duro.sourceforge.net/)
  - [Dee](http://www.quicksort.co.uk)

[Category:問い合わせ言語](https://ja.wikipedia.org/wiki/Category:問い合わせ言語 "wikilink")