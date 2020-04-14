> この記事は[ML \(プログラミング言語\)](https://ja.wikipedia.org/wiki/ML_\(プログラミング言語\))から翻訳されています。


**ML**（えむえる、Meta-Language）は、[関数型言語](../Page/関数型言語.md "wikilink")のひとつである。現代風の関数型言語としては歴史が古いほうで、[型推論](../Page/型推論.md "wikilink")機能などを持つが、デフォルトの[評価戦略](https://ja.wikipedia.org/wiki/評価戦略 "wikilink")は[遅延評価](../Page/遅延評価.md "wikilink")ではなく[先行評価](https://ja.wikipedia.org/wiki/先行評価 "wikilink")で、書き換えが可能なレコード型を持つなど、いわゆる「純粋関数型」でない特徴や機能を持つ。

## 概要

[自動定理証明](../Page/自動定理証明.md "wikilink")系において、証明の道筋を関数として記述するための[メタ言語](https://ja.wikipedia.org/wiki/メタ言語 "wikilink")として生まれたという経緯を持ち（[\#歴史](https://ja.wikipedia.org/wiki/#歴史 "wikilink")の節を参照）、名前はそのことに由来する。構文は[ISWIM](../Page/ISWIM.md "wikilink")の影響を受けている。

MLによってプログラマに知られるようになった機能に、[型推論](../Page/型推論.md "wikilink")がある。これは、明示的に型の宣言を行わなくても、データの利用のされ方から、引数や関数の返す型を自動的に推論してくれる機能である。これにより、プログラマの負担が著しく軽減される。

標準（ないし一方言）として[Standard ML](https://ja.wikipedia.org/wiki/Standard_ML "wikilink") (SML) があり、その実装には、 (SML/NJ) や、東北大学電気通信研究所大堀研究室が開発を進めているSML\#\[1\]などがある。標準以外の仕様\[2\]の実装としては[OCaml](../Page/OCaml.md "wikilink")などがある。詳細仕様は実装ごとに異なっており、各実装での仕様をそれぞれのMLの方言と捉える場合もある。

SMLの詳細とその実装の一覧は[Standard MLを参照のこと](https://ja.wikipedia.org/wiki/Standard_ML "wikilink")。

## 言語仕様

以降の記法や名前はSMLのものである。[OCaml](../Page/OCaml.md "wikilink")などその他の実装については、SMLと差異があるため各実装の記事を参照のこと。

### 演算子

MLの基本的な演算子は以下の通り

  - \+ 加算, - 減算, \* 乗算
  - / 実数での除算, div 整数での除算, mod 剰余
  - :: [リストに要素を追加](https://ja.wikipedia.org/wiki/線形リスト "wikilink"), @ [リストの結合](https://ja.wikipedia.org/wiki/線形リスト "wikilink")
  - ^ [文字列](../Page/文字列.md "wikilink")の連結, if～then～else if文（扱いは3項演算子）

### 関数の定義

MLの関数の定義は

`   fun (関数名)(引数) = (内容);`

と書く。[Haskell](../Page/Haskell.md "wikilink")と同様な[パターンマッチング](../Page/パターンマッチング.md "wikilink")がある。複数のパターンはガード記法 | をセパレータとする。

例として[階乗](../Page/階乗.md "wikilink")を求めるプログラムを以下に示す。

`   fun factorial(1) = 1`
`   | factorial(n) = n * factorial(n-1);`

MLでの関数の評価は関数が定義されたときに行われる。このためMLでは関数定義の順序が無視できない。例として

`   fun a(x) = b(x-1) + x;`

`   fun b(x) = x * x;`

のような関数がある場合は必ず b の方が先に定義されていないといけない。しかしこの場合はお互いを呼ぶような[再帰呼び出し](https://ja.wikipedia.org/wiki/再帰呼び出し "wikilink")の実装が不可能である。そこでMLではそのような関数のために二つの関数を and でつなぐことによってこれを実装することができる。 例を挙げると

`   fun take(nil) = nil`
`   | take(x::xs) = x::skip(xs)`
`   and skip(nil) = nil`
`   | skip(x::xs) = take(xs);`

これは take が与えられたリストの奇数番目の要素を返し、skip が偶数番目の要素を返す関数である。

## 歴史

[デイナ・スコット](../Page/デイナ・スコット.md "wikilink")の提案したPPLAMBDAという論理体系を利用し、[ロビン・ミルナー](../Page/ロビン・ミルナー.md "wikilink")は (LCF) という証明のチェックや定理の自動証明をするシステムを実装した。1973年に発足したEdinburgh LCFのプロジェクトにおいて、証明の道筋を関数として記述するための[メタ言語](https://ja.wikipedia.org/wiki/メタ言語 "wikilink")として開発されたのが、MLの最初であり、強い型付きの言語として設計された。

Edinburgh LCFとMLは、1975～76年に[エディンバラ大学](../Page/エディンバラ大学.md "wikilink")で実装された。特に1980年代以降、汎用プログラミング言語として多数の機能やライブラリが追加されている。

（この節 参考文献『新しいプログラミング・パラダイム』(ISBN 4-320-02493-1) pp. 120-121）

## 参照

<references/>

## 参考文献

  -
## 外部リンク

  - [Standard ML of New Jersey](http://www.smlnj.org/)
  - [The Caml language: Home](http://caml.inria.fr/)
  - [Standard ML リンク集](http://lang.x0.com/func/ml/sml.htm)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:関数型言語](https://ja.wikipedia.org/wiki/Category:関数型言語 "wikilink")

1.  [SML＃プロジェクト](http://www.pllab.riec.tohoku.ac.jp/smlsharp/ja/)
2.  OCamlは、表層文法 (surface grammar) すなわち綴りや字句的構文 (lexical syntax) の違いが目立つので差異が大きいと思われやすいが、