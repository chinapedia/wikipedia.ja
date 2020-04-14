> この記事は[Haskell](https://ja.wikipedia.org/wiki/Haskell)から翻訳されています。


（ハスケル）は[非正格な評価を特徴とする](https://ja.wikipedia.org/wiki/評価戦略#正格でない評価 "wikilink")[純粋関数型プログラミング言語である](../Page/関数型言語.md "wikilink")。名称は[数学者](../Page/数学者.md "wikilink")であり[論理学者](https://ja.wikipedia.org/wiki/論理学者 "wikilink")である[ハスケル・カリー](../Page/ハスケル・カリー.md "wikilink")に由来する。

## 概要

は[高階関数](../Page/高階関数.md "wikilink")や[静的](https://ja.wikipedia.org/wiki/静的型付け "wikilink")[多相型付け](../Page/ポリモーフィズム.md "wikilink")、[定義](https://ja.wikipedia.org/wiki/定義 "wikilink")可能な[演算子](https://ja.wikipedia.org/wiki/演算子#プログラミングにおける演算子 "wikilink")、例外処理といった多くの言語で採用されている現代的な機能に加え、パターンマッチングや[カリー化](../Page/カリー化.md "wikilink")、リスト内包表記、[ガードといった多くの特徴的な機能を持っている](../Page/ガード_\(プログラミング\).md "wikilink")。また、[遅延評価](../Page/遅延評価.md "wikilink")や[再帰](../Page/再帰.md "wikilink")的な[関数や](https://ja.wikipedia.org/wiki/サブルーチン#関数 "wikilink")[代数的データ型](../Page/代数的データ型.md "wikilink")もサポートしているほか、独自の概念として[圏論](../Page/圏論.md "wikilink")のアイデアを利用し[参照透過性](../Page/参照透過性.md "wikilink")を壊すことなく副作用のある操作（例えば [代入](https://ja.wikipedia.org/wiki/変数_\(プログラミング\)#代入 "wikilink")、[入出力](https://ja.wikipedia.org/wiki/入出力#コンピュータ処理における入出力 "wikilink")、[配列](../Page/配列.md "wikilink")など）を実現する[モナドを含む](../Page/モナド_\(プログラミング\).md "wikilink")。このような機能の組み合わせにより、[手続き型プログラミング言語](https://ja.wikipedia.org/wiki/手続き型プログラミング言語 "wikilink")では記述が複雑になるような処理がしばしば簡潔になるばかりではなく、必要に応じて手続き型プログラミングを利用できる。

は関数型プログラミングの研究対象として人気が高い。あわせて  と呼ばれる[マサチューセッツ工科大学](../Page/マサチューセッツ工科大学.md "wikilink")や[グラスゴー大学](../Page/グラスゴー大学.md "wikilink")によるものをはじめ、他にも \[1\] や  といった分散バージョン、 と呼ばれる[投機的実行](../Page/投機的実行.md "wikilink")バージョン、 や 、 といった[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")バージョンも複数存在しているなど、いくつもの派生形が開発されてきている。

[GUI開発向けサポートの新しい方法を提供する](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink")、 と呼ばれる  に似た言語もある。 と  の最大の違いは、[モナドを代用する一意型の採用である](../Page/モナド_\(プログラミング\).md "wikilink")。

は比較的小規模なユーザコミュニティを持つが、。オードリー・タングによる  は [Perl6](https://ja.wikipedia.org/wiki/Raku "wikilink") の[インタプリタ](../Page/インタプリタ.md "wikilink")と[コンパイラ](../Page/コンパイラ.md "wikilink")の実装で、（現在は開発停止）。Darcs はさまざまな革新的な機能を含むリビジョンコントロールシステムである。

の急速な進化は今も継続しており、[GHCは現在の](https://ja.wikipedia.org/wiki/Glasgow_Haskell_Compiler "wikilink")[事実上の標準の処理系であるといえる](../Page/デファクトスタンダード.md "wikilink")。

では[2001年](../Page/2001年.md "wikilink")、[2004年](../Page/2004年.md "wikilink")、[2005年](../Page/2005年.md "wikilink")に最優秀賞に選ばれている。

は  用のビルドおよびパッケージングシステムである。 を利用して  ライブラリのアーカイブである  を参照して、新たなパッケージを簡単にインストールすることもできる。しばしばパッケージのが発生しがちだが、それらを解決するため、という環境も有志によって提供されている。

## 歴史

[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")、遅延関数言語である  がリサーチ・ソフトウェア社によって発表された。[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")にはこのような非正格な純粋関数型プログラミング言語が十二以上存在していたが、そのうち最も広く使われていた  は[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")ではなかった。[オレゴン州ポートランドで開催された](../Page/ポートランド_\(オレゴン州\).md "wikilink")  () において開かれた会議中に、遅延関数型言語のオープンな標準を作成するための委員会が発足されるべき、という強い合意が参加者のあいだで形成された。委員会の目的は、関数型言語のデザインにおける将来の研究のための基礎として役立つ共通のものへと、既存の関数型言語を統合することであった\[2\]。

###  1.0

最初の版の （ 1.0）は[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")に作成された\[3\]。委員会の活動は一連の言語仕様を結果に残し、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")後半にそのシリーズは、安定しており小さく可搬なバージョンの言語仕様と、学習用および将来の拡張の基礎としての基本ライブラリなどを定義した 98 に到達した。実験的な機能の付加や統合を通じて 98 の拡張や派生物を作成することを、委員会ははっきりと歓迎した\[4\]。

###  98

[1999年](../Page/1999年.md "wikilink")2月、 98 言語標準は最初に  として発表された\[5\]。[2003年](../Page/2003年.md "wikilink")1月、改定されたバージョンが  として発表された\[6\]。GHC に代表されるように、 は急速に発達しつづけている。

###

[2006年](../Page/2006年.md "wikilink")前半、非公式に （）と呼ばれている  98  の後継の作成プロセスが開始された\[7\]。このプロセスは  98 のマイナーバージョンアップを目的としている\[8\]。

###  2010

2010 は他のプログラミング言語とのバインディングを可能にする （FFI）を  に追加し, いくつかの構文上の問題を修正する(正式な構文を変更する)。「`n + k` パターン」と呼ばれる構文を削除し, `fak (n+1) = (n+1) * fak n`というような形式の定義はもはや許されない。 に  2010 のソースかどうかや, いくつかの必要な拡張の指定を可能にする言語プラグマ構文拡張\[9\]を導入する。 2010 に導入された拡張の名前は, `DoAndIfThenElse`, `HierarchicalModules`（階層化ライブラリ）, `EmptyDataDeclarations`, `FixityResolution`, `ForeignFunctionInterface`, `LineCommentSyntax`, `PatternGuards`, `RelaxedDependencyAnalysis`, `LanguagePragma`, `NoNPlusKPatterns` である。

## 主な構文

ここでは以降の解説を読む上で必要な  の文法規則を簡単に説明する。 の構文は数学で用いられるものによく似せられていることに注意されたい。

### 型

の型名は先頭が大文字でなければならない。標準で存在する単純なデータ型としては、`Bool`（真偽値）型、`Int`（整数）型、`Float`（単精度浮動小数点数）型、`Char`（文字）型、`String`（文字列）型などが予め定義されている。任意の式の型を定義するには、式と型の間に `::` 記号をおく。また、変数などのシンボル\[10\]を定義する際に変数名を式に指定して書くことで、その変数の型を指定することができる。例えば、次は[円周率](https://ja.wikipedia.org/wiki/円周率 "wikilink")および[ネイピア数](../Page/ネイピア数.md "wikilink")を定数として定義し、さらにその型も浮動小数点型として指定している。\[11\]

``` haskell
pi :: Float
pi = 3.1415926535

e = 2.7182818284 :: Float    -- 式の中でその型を指定している
```

関数の型は、各引数の間を `->` 記号で区切って表記する。関数は引数をひとつ適用するたびに、その型は `->` で区切られたうちの一番左が消えた型となると考えればよい。<ref> はカリー化によりすべての関数を 1 引数の関数として表現できるが、これにしたがって `->` は右結合であるとして読むこともできる。上記の関数の型の定義は、括弧を明示した次の定義と同等である。

``` haskell
gcd :: Int -> (Int -> Int)
```

関数を引数にとる関数は、引数の型を括弧で囲んで -\> 記号の優先順位を指定すればよい。次は関数を二つとり、その合成関数を返す演算子 . の定義である。

``` haskell
(.) :: (b -> c) -> (a -> b) -> a -> c
```

</ref>例えば、ふたつの整数を引数にとりその最大公約数を返す関数 `gcd` の型は次のように定義される。\[12\]

``` haskell
gcd :: Int -> Int -> Int    -- 関数名 :: 引数1の型 -> 引数2の型 -> 返り値の型
```

型変数を使い、型を抽象化することもできる。これは  のテンプレートや  のジェネリクスに相当するが、様々な種(型の型)に適用できるためより柔軟である。例えば、`a` 型の値をとり、それをそのまま返す恒等関数 `id` を型の指定とともに定義すると以下のようになる。ここで任意の型を示す型名 `a` が定義に使われているが、このように先頭が小文字で始まっている型名は具体的な型名ではなく型変数である。この関数はあらゆる型の値を引数にとることができる。

``` haskell
id :: a -> a
id x = x
```

また、データ型はパラメータとして型変数を持つことができる。例えば、スタックやハッシュテーブルなどのデータ型は、その要素の型を型変数として定義する。ハッシュテーブルを実装するデータ型 `HashMap :: * -> * -> *` があり、キーに文字列（`String`）、値に整数（`Int`）を持つハッシュテーブル `hashtable` の型は次のようになる。<ref> これは、 や  のような言語では次のようなコードに相当する。

``` Java
Hashtable<String,Int> hashtable;
```

</ref>

``` haskell
hashtable :: HashMap String Int
```

そのほか、特殊な表記を持つ型として[リスト](https://ja.wikipedia.org/wiki/リスト "wikilink")と[タプル](../Page/タプル.md "wikilink")、[文字列](../Page/文字列.md "wikilink")がある。リストは  で極めて頻繁に用いられるため、[特別な構文が用意されている](../Page/糖衣構文.md "wikilink")。リストは要素の型を角括弧で囲む。次は `Char`（文字）のリストを束縛する変数 `text` の定義である。\[13\]文字のリストは文字列と等価である。2行目にあるように、文字列は殆どのプログラミング言語と同じように二重引用符で囲む。コメントにHaskellでのリストの表記を添えた。最後にデシュガー（糖衣構文を元の表記に戻すこと）したリストの表記法を示した。textもhelloも等価である。

``` haskell
text :: [Char]
text = "Hello"    -- ['H','e','l','l','o'] の糖衣構文
hello :: [Char]
hello = 'H':'e':'l':'l':'o':[]
```

タプルは要素の型をカンマで区切り、括弧で囲む。次は `Float`（浮動小数点数）の値をもつ2次元座標のタプルが束縛される変数 `point` の定義である。

``` haskell
point :: (Float,Float)
point = (3, 7)
```

タプルは2以上ならいくつでも要素を持つことができる。1要素のタプルは優先順位の括弧と表記が衝突し、また用途がないので存在しない。要素数がゼロのタプルは特に「ユニット」(`Unit`) と呼ばれ、有効な値を持たないなどの時に使われる。\[14\]

`type` キーワードを用いて、型に別名をつけることができる。\[15\]次は `[Char]` に `String` という別名をつけている。\[16\]

``` haskell
type String = [Char]
text :: String
```

Haskellの型は**型構築子**（型コンストラクタ、***type constructor***）から構築される\[17\]。型構築子`T`に型変数（Type variables）`v1 v2 vN`を与え型式（type expression）`T v1 v2 vN`として評価することで型が構築される。型構築子の例には以下が挙げられる。

| [カインド](https://ja.wikipedia.org/wiki/カインド_\(型理論\) "wikilink") | 総称                                        | 例             | 出典     |
| ------------------------------------------------------------- | ----------------------------------------- | ------------- | ------ |
| \*                                                            | nullary type constructors, type constants | `Int`, `Bool` | \[18\] |
| \* -\> \*                                                     | unary type constructors                   | `Maybe`, `IO` | \[19\] |
| \* -\> \* -\> \*                                              | binary type constructors                  | `Either`      |        |

表: 型構築子の分類と例

例えば型構築子`Maybe`に型変数`Int`を渡し、`Maybe Int`とすることで型が構築される。

### 関数と演算子

関数名は先頭が小文字でなければならず、記号を含むことはできない。演算子名は記号のみで構成されていなければならない。関数の定義ではC言語のような引数を囲む括弧や区切りのカンマは使われず、単に引数を空白文字で区切って表記する。次は先程示した恒等関数 `id` に、型の定義に加えて本体の定義もした例である。

``` haskell
id :: a -> a
id x = x    -- 関数名 仮引数1 仮引数2 … = 関数本体の式
```

関数の適用も同様で、単に関数に続いて空白文字で区切った引数を並べればよい。以下では上記の恒等関数 `id` を(ここでは使う必要はないが)適用して、別の変数を定義した例である。

``` haskell
hoge = id "piyo"    -- hoge == "piyo" となる。
```

引数がつねに2個であることや引数の間に演算子をおくことなどを除けば、演算子についても関数の定義や適用と同様である。標準で定義されている算術演算子を使って、[BMIを計算する関数](../Page/ボディマス指数.md "wikilink") `bmi` を定義してみる。

``` haskell
bmi :: Float -> Float -> Float
bmi weight height = weight / height ^ 2
```

この定義では `Float` を引数にとり `Float` で結果を返すが、この関数では `Double` を引数に使うことはできない。どの浮動小数点数型でも扱えるような関数にするには、次のように型変数を使えばよい。

``` haskell
bmi :: Floating a => a -> a -> a
bmi weight height = weight / height ^ 2
```

このバージョンの関数 `bmi` では引数や返り値の型が `a` とされているが、これにさらに `a` は `Floating` であるとの制約をつけている。`Floating` は `Float` や `Double` を抽象化する型クラスであり `/` や `^` といった演算子を適用できるので、`bmi` の定義においてこれらの演算子を使うことができている。また、整数などの値は引数に取れないし、返り値は引数に与えた型で戻ってくる。

関数と演算子は新たに定義し直さなくても相互に変換可能である。関数を演算子として使うには、関数を `` ` `` (バッククォート)で囲む。逆に、演算子を関数として使うには括弧で囲む。例えば、整数を除算する関数 `div` はよく演算子として使われる\[20\]。

``` haskell
aspectRatio = width `div` height
```

なお、関数適用の優先順位はすべての[演算子の優先順位](https://ja.wikipedia.org/wiki/演算子の優先順位 "wikilink")よりも高い。

## 特徴的な機能

ここではあまり他の言語では見られない  特有の機能を中心に解説する。ここでは説明していないが、現代的な実用言語では常識となっている[ガーベジコレクション](https://ja.wikipedia.org/wiki/ガーベジコレクション "wikilink")、[例外処理](../Page/例外処理.md "wikilink")、[モジュール](../Page/モジュール.md "wikilink")、外部関数の呼び出し、[正規表現](../Page/正規表現.md "wikilink")ライブラリなどの機能は、 にも当然存在している。

### 遅延評価

は[遅延評価](../Page/遅延評価.md "wikilink")を基本的な評価戦略とする。ほとんどの言語では関数の呼び出しにおいて引数に与えられたすべての式を評価してから呼び出された関数に渡す[先行評価](https://ja.wikipedia.org/wiki/先行評価 "wikilink")を評価戦略とするが、これに対し  ではあらゆる式はそれが必要になるまで評価されない。次の定数 `answer` は評価すると常に `42` を返すが、その定義には未定義の式を含む。

``` haskell
answer = const 42 (1 `div` 0)
```

ここで、`const` は常に第1[引数](../Page/引数.md "wikilink")を返す[定数](../Page/定数.md "wikilink")関数である。また、`` `div` `` は整数の除算を行う演算子であり、``1 `div` 0`` は `1 / 0` に相当し、この値は未定義であり、この部分を評価すればエラーになる。正格評価をする言語でこのような式を評価しようとすると、[ゼロ除算](../Page/ゼロ除算.md "wikilink")によるエラーになるであろう。しかし 上記の定数 `answer` を評価してもエラーにはならない。`const` は第1引数をつねに返すので第2引数を評価する必要はなく、第2引数に与えられた式 ``1 `div` 0`` は無視されるので評価されないからである。遅延評価がデフォルトで行われることにより、不要な計算は省かれ、[参照透過性](../Page/参照透過性.md "wikilink")により同じ式を複数回評価する必要もなくなるため、 では最適化によって計算効率の向上が期待できる場合がある。ただし、頻繁に新たな値を計算する場合は正格評価のほうが効率がよく、必要に応じて`seq`関数やBangPatterns拡張による明示により正格評価もできる。

### 型推論

では[関数の](https://ja.wikipedia.org/wiki/サブルーチン#関数 "wikilink")[データ型](../Page/データ型.md "wikilink")を明示しなくても処理系が自動的に型を推論する。以下は型の宣言を省略し、本体のみを宣言した引数の平方を返す関数 `square` である。

``` haskell
square x = x * x
```

この場合 `square` の型は型推論され、次のように明示的に型を宣言したのと同じになる。

``` haskell
square :: (Num a) => a -> a
square x = x * x
```

この宣言は、「`Num`のインスタンス\[21\]である `a` の型の値を引数にとり、`a` の型の値を返す」と読める。ここでは「`*`」[演算子が適用可能な最も広い型である](https://ja.wikipedia.org/wiki/演算子#プログラミングにおける演算子 "wikilink") `Num a` が選択されており、整数や浮動小数点数、有理数のような `Num` のインスタンスであるあらゆる型の値を渡すことができる。外部に公開するような関数を定義するときは、型推論によって自動的に選択される最も広い型では適用可能な範囲が広すぎる場合もある。`Integer` のみを渡せるように制限する場合は、次のように明示的に型を宣言すればよい。

``` haskell
square :: Integer -> Integer
square x = x * x
```

型推論のため、 は型安全でありながらほとんどの部分で型宣言を省略できる\[22\]。なお、次のコードは型宣言が必要な例である。`read` は文字列をその文字列があらわすデータ型に変換する抽象化された関数である。

``` haskell
main = print (read "42")    -- コンパイルエラー！
```

このコードはコンパイルエラーになる。`read` は複数のインスタンスで実装されており、数値なら数値型に変換する `read`、リストならリストに変換する `read` というように型ごとに実装が存在する。 の型は総て静的に決定されなければならない。このコード場合、プログラマは

``` haskell
read :: String -> Int
```

という型をもつ実装の `read` が選択されると期待しているであろうが、これはコンパイラによる静的な型検査では決定できない。つまり、 コンパイラは `read` の返り値を受け取っている関数 `print` の型を検査し多数の実装の中から適切な `read` を選択しようとするが、`print` は `Show` のインスタンスが存在するあらゆる型を引数にとるため、型推論によっても `read` の型を一意に決定できない。これを解消するひとつの方法は、`::` によって型を明示することである。

``` haskell
main = print ((read "42") :: Int)    -- コンパイル成功！read の返り値を Int と明示している
```

また、そもそも `read` の返り値を整数型しか取らない関数に与えていればあいまいさは生じず、型推論は成功する。

``` haskell
printIntOnly :: Int -> IO ()
printIntOnly x = print x

main = printIntOnly (read "42")    -- コンパイル成功！
```

他の言語、たとえば  でこのような抽象的な関数を書こうとしても、 では返り値の値の型によって関数を選択するようなことはできない（引数の型によって選択するメソッドのオーバーロードは存在する）。そのため、関数の実装ごとに別の名前をつけてプログラマに明示的に選択させて解決させることになる\[23\]。この方法は簡潔でわかりやすいが、抽象性の高さに基づく再利用性という点では  のような多相には劣ってしまう。

### 代数的データ型

のデータ型には[代数的データ型](../Page/代数的データ型.md "wikilink")\[24\]と呼ばれる、C言語などでいう構造体や列挙体の性質を兼ね備えたものが用いられる。次の例は二つのInt型の値をフィールドに持つ二次元の座標、`Point2D` 型を定義したもので、これは代数的データ型の構造体的な性質を示す。先頭のトークン「`data`」は代数的データ型の宣言であることを示す予約語である。ここで最初の `Point2D` はデータ型名を表し、次の `Point2D` はデータコンストラクタ名を示す\[25\]。

``` haskell
data Point2D = Point2D Int Int

origin :: Point2D
origin = Point2D 0 0    -- データコンストラクタは関数のように適用できる
```

データコンストラクタは値を定義するための特殊な関数といえる。データコンストラクタは後述するパターンマッチによって値を取り出す際にも用いられる。

次の例は[トランプ](../Page/トランプ.md "wikilink")の4つの[スーツを示す](../Page/スート.md "wikilink") `Suit` 型を定義したものである。`Spade`、`Heart`、`Club`、`Diamond` の4つのデータコンストラクタが定義されており、`Suit` 型の式は `Spade`、`Heart`、`Club`、`Diamond` のいずれかの値をとる。

``` haskell
data Suit = Spade | Heart | Club | Diamond
```

次の例は `String` 型の値を格納する[二分木](../Page/二分木.md "wikilink")の型である。`Leaf`（葉）は `String` 型の値を持ち、`Branch`（枝）は `Leaf` もしくは `Branch` である `Tree` 型の変数を二つ持つ。これは代数的データ型の構造体的な性質と列挙体的な性質の両方が現れている。

``` haskell
data Tree = Leaf String | Branch Tree Tree

organisms :: Tree
organisms = Branch animals plants    -- Branch (Branch (Branch (Leaf "Lion") (Leaf "Tiger")) (Leaf "Wolf")) (Leaf "Cherry")

animals = Branch cats (Leaf "Wolf")

cats = Branch (Leaf "Lion") (Leaf "Tiger")

plants = Leaf "Cherry"
```

GADTと呼ばれる機能を使うと、コンストラクタの型を明示してデータ型を定義することもできる。

``` haskell
{-# LANGUAGE GADTs #-}
data Male
data Female

data Person s where
    Adam :: Person Male
    Eve :: Person Female
    Child :: Person Male -> Person Female -> Int -> Person a
```

### 無名関数

は[第一級関数](https://ja.wikipedia.org/wiki/第一級関数 "wikilink")をサポートしており、[高階関数](../Page/高階関数.md "wikilink")を定義することができる。つまり、関数の引数として関数を与えたり、返り値として関数を返すことができる。無名関数は `\` (バックスラッシュ)から始まり、それに続いて引数となる変数、引数と本体のあいだに `->` 記号をおく。`List` モジュールに定義されているリストのソートを行う関数 `sortBy` は、二つの要素に大小関係を与える関数を引数にとるが、無名関数を使うと例えばリストをその長さの短い順にソートする関数 `sortList` は次のように定義できる。

``` haskell
sortList xs = sortBy (\as bs -> compare (length as) (length bs)) xs
```

### 関数のカリー化と部分適用

において、2つの引数を持つ関数は、1つの引数をとり「1つの引数をとる関数」を返す関数と同義である。このように、関数を返すことで全ての関数を1つの引数の関数として表現することを[カリー化](../Page/カリー化.md "wikilink")という。(あえてタプルを使うことで複数の引数を渡すような見かけにすることもできるが。)次の例は2つの引数をとり、そのうち値が大きい値を返す関数 `max` である。

``` haskell
 max a b = if a > b then a else b
```

この関数maxは無名関数を用いて次のように書き換えることができる。先ほどの表現とまったく同様に動作するが、この表現では関数を返す様子がより明らかになっている。

``` haskell
 max a = \b -> if a > b then a else b
```

さらに、次のようにも書き換えることができる。

``` haskell
 max = \a -> \b -> if a > b then a else b
```

あるいは、`f x = ... x ...`は、`f = (\x -> ... x ...)`の[糖衣構文](../Page/糖衣構文.md "wikilink")であるとも言える。このため、 の定義は変数に束縛するのが定数であるか関数であるかにかかわらず、「変数 = 値」という一貫した形でも定義できる。

カリー化によって、 のあらゆる関数は引数を部分適用することができる。つまり、関数の引数の一部だけを渡すことで、一部の変数だけが適用された別の関数を作り出すことができる。また、 では演算子を部分適用することすら可能であり、演算子の部分適用をとくにセクション\[26\]と呼ぶ。

任意のリストをとり、その要素から条件にあう要素のみを取り出す関数 `filter` が標準ライブラリに定義されている。

``` haskell
filter :: (a -> Bool) -> [a] -> [a]
```

この関数では第一引数に残す要素を判定する関数をとるが、このときに部分適用を使えばそのような関数を簡潔に書くことができる。整数のリストから正の値のみを取り出す関数 `positives` は次のように定義できる。

``` haskell
positives :: [Int] -> [Int]
positives = filter (> 0)

ps = positives [-4, 5, 0, 3, -1, 9]    -- [5, 3, 9]
```

ここで、`positives` および `filter` の第2引数はソースコード上に現れずに記述できているが、このように単純に書けるのもカリー化の恩恵によるものである。

### パターンマッチ

では関数の引数を様々な形で受け取ることができる。

次は整数の要素をもつリストの全要素の合計を返す関数 `total` である。

``` haskell
total :: [Int] -> Int
total [] = 0
total (x:xs) = x + total xs
```

`total` の関数本体の定義がふたつあるが、このうち引数の実行時の値と適合する本体が選択され呼び出される。上の本体定義では、引数が空のリストであるときのみ適合し、呼び出される。下の本体定義では、引数が少なくともひとつの要素を持つとき適合し、`x` に先頭の要素が束縛され、`xs` に残りのリストが束縛される。この例の場合はパターンに漏れはないが、もし適合するパターンが見つからない場合はエラーになる。

複数の返り値を扱うのもタプルなどを利用して極めて簡明に書くことができる。

``` haskell
(x, y) = (10, 20)
```

このとき、定義される変数は `x` および `y` で、それぞれ `x` は `10` に、`y` は `20` に定義される。

### リストとリスト内包表記

で順序付けられた複数の値を扱うのにもっとも柔軟で簡潔な方法は[リストを用いることである](../Page/リスト_\(抽象データ型\).md "wikilink")。次は四季の名前のリストである。

``` haskell
 ["Spring", "Summer", "Autumn", "Winter"]
```

次は初項10、公差4の等差数列のリストである。このリストは無限リストであり、その長さは無限大である。

``` haskell
 [10, 14..]
```

次の式は先ほどの数列の先頭20項を要素に持つリストである。`take n l` はリスト `l` の先頭 `n` 個の項を要素に持つリストを返す関数である。

``` haskell
 take 20 [10, 14..]
```

もし正格な動作を持つ言語でこのような定義をしようとすると関数 `take` に値を渡す前に無限リストを生成することになるが、長さが無限のため無限リストの生成が終わることはなく関数 `take` がいつまでも呼び出されなくなってしまう。 は遅延評価されるため、このようなリストを定義しても必要になるまで必要な項の値の生成は遅延される。このように無限リストを扱えるのは  の大きな強みである。次は[素数](../Page/素数.md "wikilink")列をリスト内包表記を用いて定義した一例である。

``` haskell
 primes :: [Int]
 primes = [x | x <- [2..], and [rem x y /= 0 | y <- [2 .. x - 1]]]
```

リストはその柔軟性から再帰的な関数での値の受け渡しに向いているが、任意の位置の要素にアクセスするためには参照を先頭からたどる必要があるのでランダムアクセスが遅い、要素を変更するたびにリストの一部を作り直さなければならないなどの欠点がある。このため  にも[配列](../Page/配列.md "wikilink")が用意されており、高速な参照や更新が必要なプログラムではリストの代わりに配列を用いることでパフォーマンスを改善できる可能性がある。

### 型クラスとインスタンス

型クラス\[27\]は相異なるデータ型に共通したインターフェイスを持つ関数を定義する。例えば、順序づけることができる要素をもつリストを[ソート](../Page/ソート.md "wikilink")できる関数 `sort` を定義することを考える。リストの要素のデータ型は関数 `sort` を定義するときには不明であり、その要素をどのように順序付けるかを予め決定しておくことはできない。数値型も文字列型もそれぞれのデータを順序付けることができるであろうが、共通してデータの順序を返す抽象的な関数 `order` を定義することができれば、それを用いてソートすることができる。

まず型クラス `Comparer` を定義して、順序付ける関数 `order` の形式を定義する。値の順序を調べる関数 `order x y` は `x` → `y` が昇順のときは負の値、降順の時は正の値、`x` と `y` が等しいときは `0` を返すものとする。ここで `class` は型クラスの宣言であることを示す予約語である。

``` haskell
 class Comparer a where
     order :: a -> a -> Int
```

型クラスを実装するには、対象のデータ型に対してインスタンス宣言を行う。次は型 `a` の型クラス `Comparer` に対するインスタンスを宣言したものである。このインスタンス宣言により、`Enum` のインスタンスである任意の型のリストを辞書順に比較できる。例えば、文字列 `Char` は `Enum` のインスタンスの `Char` のリストであり、このインスタンス定義により `order` を適用することができるようになる。ここで関数 `fromEnum c` は文字 `c` を数値に変換する関数である。`Comparer` のインスタンスを定義する型 `a` を `Eq` および `Enum` のインスタンスを持つものに限定しているので（`(Eq a, Enum a) =>` の部分）、インスタンス定義の内部で `Eq` の関数である `(/=)` や `Enum` の関数である `fromEnum` を使うことができている。

``` haskell
instance (Eq a, Enum a) => Comparer [a] where
    order [] [] = 0
    order _ [] = 1
    order [] _ = -1
    order (x:xs) (y:ys) | x /= y    = fromEnum x - fromEnum y
                        | otherwise = order xs ys
```

次にリストをクイックソートする関数 `sort` を示す。型クラスを用いて順序付ける関数 `order` を抽象化したため、このように型クラス `Comparer` のインスタンスを持つ全ての型の値に適用できる一般化されたソート関数を定義できるのである。

``` haskell
 sort :: Comparer a => [a] -> [a]
 sort [] = []
 sort (x:xs) = sort [e | e <- xs, order e x < 0] ++ [x] ++ sort [e | e <- xs, order e x >= 0]
```

この関数 `sort` は次のように使う。

``` haskell
main = do
    print (sort ["foo", "bar", "baz"]) -- ["bar", "baz", "foo"] と出力される。
    print (sort [[5,_9],_[1,_2],_[5,_6|5, 9], [1, 2], [5, 6]]) -- [[1,_2],_[5,_6],_[5,_9|1, 2], [5, 6], [5, 9]] と出力される。
```

のインスタンス宣言は複数の型に共通する操作を定義するという点で  や  の「インターフェイス」と似ているが、 では既存の任意の型についてもインスタンスを定義できる点でもインターフェイスに比べて柔軟である。

### 入出力

すべての式が[参照透過である](../Page/参照透過性.md "wikilink")  においては、[副作用を式の評価そのものでは表現できない](../Page/副作用_\(プログラム\).md "wikilink")。そのため、 では[圏論](../Page/圏論.md "wikilink")のアイデアを利用した[モナドによって入出力が表現されており](../Page/モナド_\(プログラミング\).md "wikilink")、 でも最も特徴的な部分となっている。次は  による  の一例である。実際に単独で実行可能形式にコンパイルできる、小さいが完全なプログラムの一例にもなっている。

``` haskell
 main :: IO ()
 main = putStrLn "Hello,World!"
```

は純粋関数型言語であり、`main` もやはり参照透過である（副作用はない）。しかし処理系は `main` として定義された `IO ()` 型の値をそのプログラムの動作を示す値として特別に扱う。`putStrLn` は標準出力に文字列を出力する動作を表す `IO ()` 型の値を返す関数であり、実行すると引数として渡された `Hello,World!` を出力する。次に標準入力から一行読み込み、そのまま標準出力に出力する[エコープログラムを考える](../Page/エコー_\(コンピュータ\).md "wikilink")。次のような、C言語などのような表記はできない。`getLine` 関数は標準入力から一行読み取る関数である。

``` haskell
 main = putStrLn getLine --コンパイルエラー！
```

`getLine` と `putStrLn` はそれぞれ次のような型を持っている。

``` haskell
 getLine :: IO String

 putStrLn :: String -> IO ()
```

純粋関数型である  では `getLine` もやはり副作用はなく、`getLine` は一行読み込むという動作を表す値を常に返す。このように入出力の動作を表す値をアクション\[28\]と呼ぶ。`getLine` が返すのは `String` そのものではなくあくまで `IO String` という型を持ったアクションであって、それを `putStrLn` の引数に与えることはできない。正しいエコープログラムの一例は次のようになる。

``` haskell
 main :: IO ()
 main = getLine >>= putStrLn
```

ここでは演算子 `>>=` によってふたつのアクションを連結している。このとき、`main` は一行読み込みそれを出力するというアクションとなり、このプログラムを実行すると処理系は `main` が持つアクションの内容を実行する。このアクションを実行すると、`getLine` は一行読み込み、それを `putStrLn` に渡す。このとき、読み込まれたデータにこれらのアクションの外側からアクセスすることはできない。このため、この式は参照透過性を保つことができる。\[29\]

モナドは、Freeモナド、Operationalモナドと呼ばれる構造により、より単純なデータ型から導出することもできる。これにより、非常に強力な[依存性の注入](../Page/依存性の注入.md "wikilink")が実現できる。

## 実例

以下の単純な例は関数型言語としての構文の実例にしばしば用いられるもので、 で示された[階乗](../Page/階乗.md "wikilink")関数である。

``` haskell
 fac :: Integer -> Integer
 fac 0 = 1
 fac n | n > 0 = n * fac (n-1)
```

階乗を単一の条件による終端を伴う再帰的関数として表現している。これは[数学](../Page/数学.md "wikilink")の[教科書](../Page/教科書.md "wikilink")でみられる階乗の表現に似ている。 コードの大半は、その簡潔さと構文において基本的な数学的記法と似通っている。

この階乗関数の1行目は関数の型を示すもので、省略可能である。これは「関数 `fac` は `Integer` から `Integer` へ（`Integer -> Integer`）の型を持つ（`::`）」と読める。これは整数を引数としてとり、別の整数を返す。もしプログラマが型注釈を与えない場合、この定義の型は自動的に推測される。

2行目では  の重要な機能であるパターンマッチングに頼っている。 関数の[引数](../Page/引数.md "wikilink")が `0`であれば、これは `1` を返す。その他の場合は3行目が試される。これは再帰的な呼び出しで、nが0に達するまで繰り返し関数が実行される。

ガードは階乗が定義されない[負の値から](https://ja.wikipedia.org/wiki/正の数と負の数 "wikilink")3行目を保護している。このガードが無ければこの関数は0の終端条件に達することなく、再帰してすべての負の値を経由してしまう。実際、このパターンマッチングは完全ではない。もし関数facに負の整数が引数として渡されると、このプログラムは実行時[エラー](../Page/エラー.md "wikilink")とともに落ちるであろう。`fac _ = error "negative value"`のように定義を追加すれば適切な[エラーメッセージ](https://ja.wikipedia.org/wiki/エラーメッセージ "wikilink")を出力することができる。

### より複合的な例

引数 `f` を伴う[高階関数](../Page/高階関数.md "wikilink")で表現された単純な[逆ポーランド記法](../Page/逆ポーランド記法.md "wikilink")評価器が、[パターンマッチング](../Page/パターンマッチング.md "wikilink")と型クラス `Read` を用いた `where` 節で定義されている。

``` haskell
 calc :: String -> [Float]
 calc = foldl f [] . words
   where
     f (x:y:zs) "+" = y+x:zs
     f (x:y:zs) "-" = y-x:zs
     f (x:y:zs) "*" = y*x:zs
     f (x:y:zs) "/" = y/x:zs
     f xs y = read y : xs
```

空リストを初期状態とし、`f` を使って一語ずつ文字列を解釈していく。`f` は、注目している語が演算子ならばその演算を実行し、それ以外ならば浮動小数点として計算スタックに積んでいる。

次は[フィボナッチ数列](https://ja.wikipedia.org/wiki/フィボナッチ数列 "wikilink")のリストである。ある値nに対するfib(n)は一回しか計算しないようになっており、その点ではナイーブなフィボナッチと異なる効率の良いコードとなっている。

``` haskell
 fibs = 0 : 1 : zipWith (+) fibs (tail fibs)
```

[無限](../Page/無限.md "wikilink")リストは 余再帰\[30\]（リストの後ろの値は要求があったときに `0` と `1` の二つの初期要素から開始され算出される）によって実現される。このような定義は遅延評価の実例で、 プログラミングでも重要な部分である。

ただし、フィボナッチ数列の生成の場合は、ある要素の値が必要であれば、その要素より前にある要素の値は全て必要である。従って、遅延させた上で結局は後から全てその値を求めることになり、むしろ無駄であるので、この場合は遅延させない組込関数seqを使用したほうが効率は良くなり\[31\]、fib 1000000 といったような値を計算するような場合には差が見えてくる。あるいはリストの先に出る値から順番に計算させるとそのほうが速い、といったことが起きる。（さらに、フィボナッチ数はnに対して2<sup>n</sup>と大きな値になるので、そのようなBigIntegerの加算のコストも掛かり、以前にこの場所に書かれていたような「線形時間でのフィボナッチ数列の生成」は、大きい値では不可能である）

どのように評価が進行するかの例示のために、次は6つの要素の計算の後の `fibs` と `tail fibs` の値と、どのように`zipWith (+)` が4つの要素を生成し、次の値を生成し続けるかを図示したものである。

``` haskell
 fibs         = 0 : 1 : 1 : 2 : 3 : 5 : ...
                +   +   +   +   +   +
 tail fibs    = 1 : 1 : 2 : 3 : 5 : ...
                =   =   =   =   =   =
 zipWith ...  = 1 : 2 : 3 : 5 : 8 : ...
 fibs = 0 : 1 : 1 : 2 : 3 : 5 : 8 : ...
```

次はGHCで使える言語拡張で、リスト内包表記を並列的な生成を記述できるよう拡張するParallelListCompを用いて書いた同様の式である。（GHCの拡張は特別な[コマンドライン](https://ja.wikipedia.org/wiki/コマンドライン "wikilink")[フラグ](../Page/フラグ_\(コンピュータ\).md "wikilink")、またはLANGUAGEプラグマによって有効にしなければならない。詳しくはGHCのマニュアルを参照のこと）

``` haskell
{-# LANGUAGE ParallelListComp #-}
 fibs = 0 : 1 : [ a+b | a <- fibs | b <- tail fibs ]
```

先に見た階乗の定義は、次のように関数の列を内包表記で生成して書く事もできる。

``` haskell
 fac n = foldl (.) id [(*k) | k <- [1..n]] 1
```

特に簡潔に書ける例として、ハミング数が順番に並ぶリストを返す以下のような関数がある。

``` haskell
 hamming = 1 : map (*2) hamming # map (*3) hamming # map (*5) hamming
     where xxs@(x:xs) # yys@(y:ys)
               | x==y = x : xs # ys
               | x<y  = x : xs # yys
               | x>y  = y : xxs # ys
```

上に示されたさまざまな `fibs` の定義のように、これはオンデマンドに数のリストを実現するために無限リストを使っており、`1` という先頭要素から後続の要素を生成している。

ここでは、後続要素の構築関数は `where` 節内の記号 `#` で表現された中置演算子で定義されている。

各|は、[等号](../Page/等号.md "wikilink")の前半の条件部分と、後半の定義部分からなるガード節を構成する。

## ライブラリ

### parsec

parsec は  で書かれたパーサコンビネータである。[パーサ](https://ja.wikipedia.org/wiki/パーサ "wikilink")の一種であるが[コンパイラコンパイラ](https://ja.wikipedia.org/wiki/コンパイラコンパイラ "wikilink")とは異なり、`Parsec` はパーサのソースコードを出力するのではなく、純粋に  の関数としてパーサを構成する。 のようにプログラミング言語と異なる言語を新たに習得する必要がなく、高速でかつ堅牢で、型安全で、演算子の結合性や優先順位を考慮したパーサを自動的に構成したり、動的にパーサを変更することすらできる。

派生として、大幅に高速なパースが可能な**attoparsec**\[32\]、高機能でより洗練された**trifecta**\[33\]がある。

###

は  の[メタプログラミング](../Page/メタプログラミング.md "wikilink")を可能にする拡張である。 ソースコードの構文木を直接  から操作することができ、C、 のマクロやテンプレートを上回る極めて柔軟なプログラミングを行うことができる。

### QuickCheck

[`QuickCheck`](https://ja.wikipedia.org/wiki/QuickCheck "wikilink") はデータ駆動型のテストを行うモジュールである。自動的にテストデータを作成してプログラムの正当性をテストすることができる。

### lens

lensはアクセサの概念を一般化するライブラリであり、様々なデータ構造に対して共通のインタフェースを与える。Getter、Setterは一つの関数として表現されており、それらを合成することもできる。[JSONや](../Page/JavaScript_Object_Notation.md "wikilink")[XMLや](../Page/Extensible_Markup_Language.md "wikilink")、JSONやXML以外の処理にも応用できる。

## 批判

は他の[プログラミング言語](../Page/プログラミング言語.md "wikilink")には見られない多くの先進的機能を持っているが、これらの機能のいくつかは言語を複雑にしすぎており、理解が困難であると批判されてきた。とりわけ、関数型プログラミング言語と主流でないプログラミング言語に対する批判は  にもあてはまる。加えて、 の潔癖さとその理論中心の起源に起因する不満がある。

[2002年](../Page/2002年.md "wikilink")に Jan-Willem Maessen、[2003年](../Page/2003年.md "wikilink")に[サイモン・ペイトン・ジョーンズ](https://ja.wikipedia.org/wiki/サイモン・ペイトン・ジョーンズ "wikilink")が遅延評価に関連するこの問題を議論し、その上でこの理論的動機を認識した。彼らは実行時のオーバーヘッドの悪化に加え、遅延はコードのパフォーマンスの推察をより困難にすると言及した。

2003年に Bastiaan Heeren と Daan Leijen、Arjan van IJzendoorn は  の学習者にとってのつまづきに気がついた。これを解決するために、彼らは  と呼ばれる新たなインタプリタを開発し、この中でいくつかの型クラスのサポートを取り除き、 の機能の一般化を制限することによってエラーメッセージのユーザ親和性を改善した。

## 実装

以下は  98 仕様を完全に満たす、または仕様に非常に近く、[オープンソース](../Page/オープンソース.md "wikilink")ライセンスの下で配布されているものである。ここには現在のところ商用のHaskell実装は含まれない。

  -
    [The Glasgow Haskell Compiler](https://ja.wikipedia.org/wiki/Glasgow_Haskell_Compiler "wikilink") は異なる複数の[アーキテクチャのネイティブコードにコンパイルできるほか](../Page/コンピュータ・アーキテクチャ.md "wikilink")、C言語にコンパイルすることもできる。おそらくGHCは最も知られた  コンパイラで、現在のところGHCのみで動く言語拡張が実装されており、かなり便利ないくつかのライブラリはGHCのみで動作する（たとえは  の[バインディングなど](https://ja.wikipedia.org/wiki/言語バインディング "wikilink")）。\[34\]
  -
    初期（Haskell 1.2）の仕様をベースとした、等式推論に向いた\[35\]方言およびインタプリタの実装。当時の  より  に似た構文、標準の機能をいくつか満たさない、逆に標準にないいくつかの機能の追加、などの特徴があった。マーク・ジョーンズにより開発された。その役割の多くは  に譲られた。 の「」は  に由来する。
  - HBC
    これは別のネイティブコード  コンパイラ。\[36\]
  -
    これは新しい  の方言である。開発の際の焦点は、明瞭なエラーメッセージを提供し学習を容易にすることである。Heliumは型クラスをサポートせず、多くのHaskellプログラムとは互換性のない実装である。\[37\]
  -
    これはバイトコードインタプリタである。これは速いプログラム編集とそれなりの実行スピードを提供する。これは単純なグラフィックスライブラリを含む。多くの人が  の基本を学ぶのによいが、これはオモチャ的な実装であるということではない。これは最も可搬で軽量な  実装である。\[38\]
  - jhc
    これは新しいプログラム変換の研究用としてのみならず、スピードと生成されるプログラムの効率を重視した John Meacham によって書かれた  コンパイラである。\[39\]
  - nhc98
    これは別のバイトコードコンパイラであるが、そのバイトコードは  より顕著に速く走る。Nhc98は省メモリ使用に焦点を絞っており、古いマシンや遅いマシンにはとりわけよい選択肢となる。\[40\]
  - yhc
    これはnhc98の派生物で、単純かつ可搬で効率的、 のサポートを目標とする。\[41\]

## 代表的なアプリケーション

  - \- 分散[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")。

  - Monadius - [グラディウス](../Page/グラディウス_\(ゲーム\).md "wikilink")・クローンのシューティングゲーム。

  - [Pandoc](https://ja.wikipedia.org/wiki/Pandoc "wikilink") - [Markdown](https://ja.wikipedia.org/wiki/Markdown "wikilink")などを変換するドキュメント・コンバータ。

  - [xmonad](https://ja.wikipedia.org/wiki/xmonad "wikilink") - [X Window Systemの](../Page/X_Window_System.md "wikilink")[ウィンドウマネージャ](../Page/ウィンドウマネージャ.md "wikilink")。

  - \- [Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")。

## 脚注

## 参考文献

  - Simon Peyton Jones. [*Wearing the hair shirt: a retrospective on Haskell*](http://research.microsoft.com/~simonpj/papers/haskell-retrospective) 2003年の[:en:POPL](https://ja.wikipedia.org/wiki/:en:POPL "wikilink")での招待演説。
  - Jan-Willem Maessen. *Eager Haskell: Resource-bounded execution yields efficient iteration*. 2002年の[ACM](../Page/Association_for_Computing_Machinery.md "wikilink") SIGPLAN workshopでのHaskellの記録。
  - Bastiaan Heeren, Daan Leijen, Arjan van IJzendoorn. [*Helium, for learning Haskell*](http://www.cs.uu.nl/~bastiaan/heeren-helium.pdf). 2003年の ACM SIGPLAN workshop でのHaskellの記録。

## 関連項目

  - [Atom](https://ja.wikipedia.org/wiki/Atom_\(ハードウェア記述言語\) "wikilink") - Haskell言語ベースのハードウェア記述言語

  - [Bluespec](https://ja.wikipedia.org/wiki/Bluespec "wikilink") - Haskell言語ベースのハードウェア記述言語

  - [Hydra](https://ja.wikipedia.org/wiki/Hydra "wikilink") - Haskell言語ベースのハードウェア記述言語

  - \- Haskellに似た構文を持つ、[依存型](https://ja.wikipedia.org/wiki/依存型 "wikilink")を持つ、正格な純粋関数型言語

  - [Elm](https://ja.wikipedia.org/wiki/Elm_\(プログラミング言語\) "wikilink") - JavaScriptのコードを生成するリアクティブなプログラミング言語

  - [Fay](https://ja.wikipedia.org/wiki/Fay "wikilink") - JavaScriptのコードを生成するHaskellのサブセット

<!-- end list -->

  - [オフサイドルール](../Page/オフサイドルール.md "wikilink")

## 外部リンク

  -   - [Old HaWiki](http://haskell.org/hawiki/) - Haskellのいくつかの古い話題の議論
      - [Haskell Humor](http://haskell.org/haskellwiki/Humor)
      - [Haskell Tutorial for C Programmers](http://www.haskell.org/~pairwise/intro/intro.html) by Eric Etheridge
      - [A Gentle Introduction to Haskell 98](http://haskell.org/tutorial/) - ([[PDF](../Page/Portable_Document_Format.md "wikilink")[ファイルとしても入手可能](../Page/ファイル_\(コンピュータ\).md "wikilink")](http://www.haskell.org/tutorial/haskell-98-tutorial.pdf))
      - [Haskell vs. Ada vs. C++ vs. Awk vs. ... An Experiment in Software Prototyping Productivity](http://haskell.cs.yale.edu/wp-content/uploads/2011/03/HaskellVsAda-NSWC.pdf) - （[PDF](https://ja.wikipedia.org/wiki/PDF "wikilink")ファイル）

  - [Yet Another Haskell Tutorial](http://www.umiacs.umd.edu/~hal/docs/daume02yaht.pdf) - Hal Daume IIIによるよいHaskellチュートリアル。公式チュートリアルに先立つより厳選された知識。

  - [The Evolution of a Haskell Programmer](http://www.willamette.edu/~fruehr/haskell/evolution.html) - Haskellで使える異なるプログラミングスタイルのちょっとユーモラスな概説。

  - [An Online Bibliography of Haskell Research](http://haskell.readscheme.org)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:関数型言語](https://ja.wikipedia.org/wiki/Category:関数型言語 "wikilink") [Category:エポニム](https://ja.wikipedia.org/wiki/Category:エポニム "wikilink")

1.  かつては  と呼ばれていた。
2.
3.
4.
5.
6.
7.
8.
9.
10. 「変数」は実際にはその値を動的に変更することはできないなど、C言語など手続き型言語の変数とは明らかに異なるものである。
11. ここでは説明のため単に Float としているが、標準ライブラリで定義されている円周率 `pi` は浮動小数点数型の抽象的な型クラスである `Floating a` で定義されており、`Float` のみならず 倍精度浮動小数点数型 `Double` の値としても取得できる。
12. 式の外で演算子の型を指定するときは、演算子を括弧で囲めばよい。以下の関数と演算子の相互変換を参照のこと。
13. 当然ながら、リストの要素としてリストを持つこともできる。例えば、文字リスト（文字列）のリストの型は [`Char`](../Page/Char.md "wikilink") となるであろう。
14. ユニットはC言語や  などでいう `void` のような使われ方をする。
15. 言い換えれば、単純な型名に見えても何か複雑な別の型の別名である可能性がある。
16. 実際に標準ライブラリでは `String` は `[Char]` の別名であり、`String` にはあらゆるリストの操作が可能である。
17. type values are built from type constructors. [haskell2010](https://www.haskell.org/onlinereport/haskell2010/haskellch4.html#x10-680004.2)
18. Char, Int, Integer, Float, Double and Bool are type constants with kind ∗. [haskell2010](https://www.haskell.org/onlinereport/haskell2010/haskellch4.html#x10-680004.2)
19. Maybe and IO are unary type constructors, and treated as types with kind ∗→∗. [haskell2010](https://www.haskell.org/onlinereport/haskell2010/haskellch4.html#x10-680004.2)
20. 除算する演算子 `/` は存在するが、これは `Float` などを除算する演算子であり整数ではない。他の言語のように自動的に値を変換する（int → float など）ような動作は  では意図的に排除されている。
21.  の型システムにおける汎用型が実体化されたもの。オブジェクト指向におけるインスタンスとは異なる。
22. ただし、型を明示することは可読性を向上したり問題の発見に役立つため、常に省略するのがよいとは限らない。
23. `java.lang.Integer.parseInt`、`java.lang.Double.parseDouble` など
24.
25. データ型名とデータコンストラクタ名は同じでも構わない。このような単純な代数的データ型であれば型名とデータコンストラクタ名を同じにすることも多い。
26.
27.
28.
29. GHC には `System.IO.Unsafe` モジュールに `unsafePerformIO` という関数があり、副作用を持ちながらアクションでない型を返すことができる。これは参照透過性に対する[バックドア](../Page/バックドア.md "wikilink")であり、 の参照透過性を破壊する恐れがあるので、注意深く使わなければならない。
30.
31. [Haskellの神話 - あどけない話](http://d.hatena.ne.jp/kazu-yamamoto/20100624/1277348961)
32. [attoparsec: Fast combinator parsing for bytestrings and text](http://hackage.haskell.org/package/attoparsec)
33. [trifecta: A modern parser combinator library with convenient diagnostics](http://hackage.haskell.org/package/trifecta)
34. [Home — The Glasgow Haskell Compiler](https://www.haskell.org/ghc/)
35.
36. <http://www.cs.chalmers.se/~augustss/hbc/hbc.html> （リンク切れ）
37. <http://foswiki.cs.uu.nl/foswiki/Helium>
38. [Hugs 98](https://www.haskell.org/hugs/)
39. [jhc](http://repetae.net/john/computer/jhc/)
40. [nhc98](https://www.cs.york.ac.uk/fp/nhc98/)
41. [Yhc - HaskellWiki](https://wiki.haskell.org/Yhc)