> この記事は[Miranda](https://ja.wikipedia.org/wiki/Miranda)から翻訳されています。


**Miranda**は、[遅延評価](https://ja.wikipedia.org/wiki/遅延評価 "wikilink")方式の純粋[関数型](../Page/関数型言語.md "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。作者デビッド・ターナー（David Turner）による以前の言語SASLや[KRCの後継でもあり](https://ja.wikipedia.org/wiki/Kent_Recursive_Calculator "wikilink")、また[MLやHopeの影響も受けている](../Page/ML_\(プログラミング言語\).md "wikilink")。イギリスのリサーチ・ソフトウェア社（Research Software Ltd.）が販売しており、同社の商標でもある。研究目的ではない商用を目指した最初の純粋関数型言語であった。

よくある例題を解くプログラムに関して言えば、Mirandaのコードは（[APL](../Page/APL.md "wikilink")などを別とすれば）ほとんどの主流のプログラミング言語よりも簡単で短く表現でき、他の[関数型言語](../Page/関数型言語.md "wikilink")と同様、信頼性の高いプログラムの開発が[命令型言語](https://ja.wikipedia.org/wiki/命令型言語 "wikilink")に比べて短期間で可能になったという報告がある。

1985年に登場した。処理系の実装としては[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")向けの[C言語](../Page/C言語.md "wikilink")で実装されたもののみがある。後発の[Haskell](../Page/Haskell.md "wikilink")は多くの面でMirandaの影響を受けている。

## 概要

Miranda は[遅延評価](https://ja.wikipedia.org/wiki/遅延評価 "wikilink")の純粋関数型言語であり、[副作用がなく](https://ja.wikipedia.org/wiki/副作用_\(プログラム\) "wikilink")、[命令型プログラミング](../Page/命令型プログラミング.md "wikilink")機能は存在しない。

具象構文の最も大きい特徴としては、[オフサイドルール](../Page/オフサイドルール.md "wikilink")を採用している。

`||` からその行の終わりまでが[コメントとして扱われる](../Page/コメント_\(コンピュータ\).md "wikilink")。別のコメント記法は「[文芸的プログラミング](https://ja.wikipedia.org/wiki/文芸的プログラミング "wikilink")」的なもので、行の先頭に `>` がない行は全てコメントとして扱われる。

Miranda の基本[データ型](https://ja.wikipedia.org/wiki/データ型 "wikilink")は `char`、`num`、`bool` である。文字列は `char` のリストであり、`num` は内部的には2種類の形式があって、自動的に変換される（[多倍長整数](https://ja.wikipedia.org/wiki/多倍長整数 "wikilink")がデフォルトで使われ、必要に応じて[浮動小数点数](../Page/浮動小数点数.md "wikilink")が使われる）。

[タプル](https://ja.wikipedia.org/wiki/タプル "wikilink")は様々な型のデータの羅列であり、抽象的な観点からは直積型である。

    this_employee = ("Folland, Mary", 10560, False, 35)

[リストもある](../Page/リスト_\(抽象データ型\).md "wikilink")。角括弧で表され、各要素はカンマで区切られる。全要素は同じ型でなければならない。

    week_days = ["Mon","Tue","Wed","Thur","Fri"]

リストの連結は `++`、差分は `--`、要素追加は `:`、サイズ（要素数）は `#`、インデックス指定は `!` である。以下に使用例を挙げる。

    days = week_days ++ ["Sat","Sun"]
    days = "Nil":days
    days!0
     → "Nil"
    days = days -- ["Nil"]
    #days
     → 7

その他にもリスト構築のショートカットがある。`..` は要素が数列の場合に利用可能で、1 ずつ増加する数列以外も指定可能である。

    fac n   = product [1..n]
    odd_sum = sum [1,3..100]

さらに強力なリスト構築機能として「リスト内包表記」（ZF記法とも呼ばれていた\[1\]）があり、2種類の形式がある。式を項の列に適用する形式は以下のようになる。

    squares = [ n * n | n <- [1..] ]

この意味は、n の自乗のリストで、n は全ての正の整数のリストから取られる。また、ある項がその1つ前の項の関数から得られる形式は以下のようになる。

    powers_of_2 = [ n | n <- 1, 2*n .. ]

これは、2のべき乗のリストである。これらの例から分かるように、Miranda では無限のリストを表現可能である。たとえばごく単純な無限のリストの例として、全ての正の整数のリスト `[1..]` がある。

さらに（これは[Haskell](../Page/Haskell.md "wikilink")には無い機能のため、Mirandaの特色と言えるが）、`//` という記号を使う diagonalising list comprehensions（対角化リスト内包表記）により、`[1..]` というような無限のリスト2つから、`[(1, 1), (1, 2), (2, 1), (1, 3), (2, 2), (3, 1), ..]` というようなそれらを合成したリストを作ることができる（普通の内包表記で普通に作ろうとすると、片方のリストを辿り続けてしまい、もう片方のリストを辿ることをしないため、うまくできない）。`[(x, y) // x <- [1..]; y <- [1..]]` というように書く。\[2\]

関数への実引数の適用は `sin x` のように、単に関数に実[引数](../Page/引数.md "wikilink")を続ける。

Miranda は他の純粋関数型言語と同様、関数を引数として他の関数に渡したり、関数の結果として関数を返したり、データ構造に要素として関数を含むといったことが可能である。また、関数は全て1引数に[カリー化](https://ja.wikipedia.org/wiki/カリー化 "wikilink")されているものと見ることもでき、実引数の数が足りていない適用は部分適用となる**（注意: しばしば混同されるが、「カリー化」と「部分適用」は違うものである）**。例えば次のようになる。

    add a b = a + b
    increment = add 1

この場合、`increment` は自身の引数に 1 を加算する。実際、`add 4 7` は2つの引数をとる関数 `add` だが、これも実際には単一引数 `7` に 4 を加算する関数とも解釈できる。

2つの引数をとる関数を中置演算子にすることができる。例えば、上記の `add` 関数では、`$add` という項を `+` 演算子と同じように使うことができる。逆に2つの引数に作用する中置演算子を関数に変換することもできる。従って、次のようになる。

    increment = (+) 1

これは、引数に 1 を足す関数を記述する一番単純な方法である。同様に

    half = (/ 2)
    reciprocal = (1 /)

といった単一引数関数を作成できる。この場合、インタプリタは除算のどちらの引数が関数の引数として供給されるのかを理解しており、引数を 2 で割る関数や 1 を引数で割る関数が得られる。

Miranda は[強い型付けをする言語だが](https://ja.wikipedia.org/wiki/型システム#強い型付けと弱い型付け "wikilink")、記述上は明確な型の宣言を必ずしも要しない。関数の型が明示されない場合、インタプリタは引数の型や引数の使われ方から[型推論](https://ja.wikipedia.org/wiki/型推論 "wikilink")を行う。例えばリスト逆転関数などでは、基本データ型（`char`, `num`, `bool`）に加えて、引数の型を問題としない `anything` 型がある。

    rev [] = []
    rev (a:x) = rev x ++ [a]

これは、任意のデータ型のリストに適用可能である。これを明示的に関数型を宣言するなら、次のようになる。

    rev :: [*] -> [*]

モジュール機構による名前空間の分離機構もある。モジュール外から内部の名前が見えないようにできる。

## コード例

以下の  のスクリプトは、数の集合について、全ての部分集合を求める関数である。

    subsets []     = [[]]
    subsets (x:xs) = [[x] ++ y | y <- ys] ++ ys
    where ys = subsets xs

以下は文芸的な記法で、全ての素数のリストを与える関数 `primes` を定義している。

    > || The infinite list of all prime numbers, by the sieve of Eratosthenes.

    The list of potential prime numbers starts as all integers from 2 onwards;
    as each prime is returned, all the following numbers that can exactly be
    divided by it are filtered out of the list of candidates.

    > primes = sieve [2..]
    > sieve (p:x) = p : sieve [n | n <- x; n mod p ~= 0]

## 注

<references/>

## 外部リンク

  - [公式サイト（英）](http://miranda.org.uk)

[Category:関数型言語](https://ja.wikipedia.org/wiki/Category:関数型言語 "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")

1.  ZFは[ツェルメロ・フレンケルの意](https://ja.wikipedia.org/wiki/公理的集合論#ZF_公理系 "wikilink")
2.  <https://www.cs.kent.ac.uk/people/staff/dat/miranda/manual/13/3.html>