> この記事は[R言語](https://ja.wikipedia.org/wiki/R言語)から翻訳されています。


**R言語**（あーるげんご）は[オープンソース](../Page/オープンソース.md "wikilink")・[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")の[統計](../Page/統計.md "wikilink")解析向けの[プログラミング言語](../Page/プログラミング言語.md "wikilink")及びその開発実行環境である。ファイル名拡張子は.r, .R, .RData, .rds, .rda。

R言語は[ニュージーランド](../Page/ニュージーランド.md "wikilink")の[オークランド大学](../Page/オークランド大学.md "wikilink")の[Ross Ihakaと](https://ja.wikipedia.org/wiki/:en:Ross_Ihaka "wikilink")[Robert Clifford Gentlemanにより作られた](https://ja.wikipedia.org/wiki/:en:Robert_Gentleman_\(statistician\) "wikilink")。現在では**R Development Core Team** によりメンテナンスと拡張がなされている。

R言語のソースコードは主に[C言語](../Page/C言語.md "wikilink")、[FORTRAN](../Page/FORTRAN.md "wikilink")、そしてRによって開発された。

なお、R言語の仕様を[実装した処理系の呼称名はプロジェクトを支援する](https://ja.wikipedia.org/wiki/実装#ソフトウェア分野における実装 "wikilink")[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")によれば『GNU R』である\[1\] が、他の実装形態が存在しないために[日本語](../Page/日本語.md "wikilink")での慣用的呼称に倣って、当記事では、仕様・実装を纏めて適宜に**R言語**や単に**R**等と呼ぶ。

## 特徴

R言語は文法的には、統計解析部分は[AT\&Tベル研究所が開発した](../Page/ベル研究所.md "wikilink")[S言語](../Page/S言語.md "wikilink")を参考としており、またデータ処理部分は[Scheme](../Page/Scheme.md "wikilink")の影響を受けている\[2\]。

### ベクトル処理言語

R言語は、「ベクトル処理」と呼ばれる実行機構により、柔軟な処理を簡便な記法で実現している。

R言語で言う「ベクトル」とは数学的用語の[ベクトル](../Page/ベクトル.md "wikilink")とはやや異なり「構造を持ったデータ集合」という「[リスト](https://ja.wikipedia.org/wiki/リスト "wikilink")」に近い意味を持つ。すなわち、[実数](../Page/実数.md "wikilink")や[複素数](../Page/複素数.md "wikilink")からなる数学上のベクトルや行列はもちろん、[配列](../Page/配列.md "wikilink")・[リスト](https://ja.wikipedia.org/wiki/リスト "wikilink")・[テーブル](../Page/テーブル_\(情報\).md "wikilink")（データフレーム）・[集合](../Page/集合.md "wikilink")・[時系列](../Page/時系列.md "wikilink")などといった複雑な構造を持ったデータも、特に宣言することなく変数に入れることができる。 ベクトルの要素がさらにテーブルや時系列の配列などであるといった「[入れ子構造](https://ja.wikipedia.org/wiki/入れ子構造 "wikilink")」であってもよい。このおかげで複雑な[データ構造](../Page/データ構造.md "wikilink")が他愛もなく構築・管理できる。

[予約語](../Page/予約語.md "wikilink")としてRに組込まれた演算も、関数も、ベクトルを扱うことができる。ユーザー定義関数をベクトル対応にするための関数もある。こうしたRの演算子やRの関数は、ベクトルの全要素に順に作用したり調べるといった構造にできている。 そのおかげで、プログラム全体の制御構造が単純化して意味が明瞭になる。リストをうまく使うことによって、通常他の言語で複数要素を処理する時の「目的とする計算の本質とかけ離れた[アルゴリズム](../Page/アルゴリズム.md "wikilink")」（たとえば、カウンターを使った[ループ](../Page/ループ.md "wikilink")や[条件分岐](https://ja.wikipedia.org/wiki/条件分岐 "wikilink")等）の作成負担から解放される。（他のプログラミング言語で似た記法を探すとすれば、たとえば[Lisp](https://ja.wikipedia.org/wiki/Lisp "wikilink")言語のmapcar関数、[Perl](../Page/Perl.md "wikilink")言語のmap関数など。）

例として、[円周率](https://ja.wikipedia.org/wiki/円周率 "wikilink")を[モンテカルロ法](../Page/モンテカルロ法.md "wikilink")で近似する計算を挙げる\[3\]。

``` rsplus
s <- 100000
x <- runif(s)
y <- runif(s)
sum(x^2 + y^2 <= 1) * 4 / s
```

ここで『 `<-` 』は代入（この場合『 `=` 』とも書けるが推奨はされていない）、『 `runif(a)` 』は[一様乱数を](https://ja.wikipedia.org/wiki/乱数列#一様乱数 "wikilink") `a` 個作りベクトルで返す関数、『 `a^2` 』は `a` の二乗、『 `sum( a <= b)` 』は引数のベクトル要素数を返す関数、を意味する。 この場合sum関数の引数はTRUEまたはFALSEのリストからなる論理値型ベクトルである。ベクトル`a`および`b`の対応要素同士を比較演算子で比較した結果が並んでいるので、真であった個数が返る。

上の例で、sum関数によって、[条件分け計算を複数回行なう指示が暗黙のうちになされていることに注目されたい](https://ja.wikipedia.org/wiki/制御構文 "wikilink")。 すなわち、0から1の値をとる一様乱数`x`と`y`の組からなる「[サンプルを十万個作り](../Page/標本_\(統計学\).md "wikilink")、そのうち[半径](../Page/半径.md "wikilink")1の円内に入ったサンプルが何個かを数える。」という計算の本質を、forループのような繰返し処理の記述を必要とせず、簡潔に表現できている。

代入『 `<-` 』は「付値」と呼ばれる関数でもあり、以下のように一行に書き換えても意味は同じとなる。

``` rsplus
sum(runif(s <- 100000)^2 + runif(s)^2 <= 1) * 4 / s
```

また、付値記号に矢印を用いると代入の向きを左右に使い分けられる。

ベクトルは「論理添字（元のベクトルと要素数が等しい論理値型ベクトルを用いた添字指定）」を使うことで要素の絞り込みができ、そのベクトルに対して付値を行うと、絞り込んだ要素だけを別内容に置き換えることが可能になる。

以下は[FizzBuzz問題の解答例である](https://ja.wikipedia.org/wiki/FizzBuzz#FizzBuzz問題 "wikilink")。（記号"\#"から改行まではコメント文）

``` rsplus
#  1から100までの整数を、ベクトルで生成する。（n: 加工前の数列 ・ Ans: 加工後の結果用数列）
1:100 -> n -> Ans

#  3の倍数FizzSet相当のAns要素を、文字列"Fizz"に置き換える。（FizzSet: 3の倍数位置を示す論理ベクトル)
Ans[n %% 3 == 0 -> FizzSet] <- "Fizz"

#  5の倍数BuzzSet相当のAns要素を、文字列"Buzz"に置き換える。（BuzzSet: 5の倍数位置を示す論理ベクトル)
Ans[n %% 5 == 0 -> BuzzSet] <- "Buzz"

#  両倍数の共通集合相当のAns要素を、文字列"FizzBuzz"に置き換える。
Ans[FizzSet & BuzzSet] <- "FizzBuzz"

#  出力する。
cat(Ans)
```

ベクトルの各種演算に加えて、行列の各種演算が可能である。

[イテレータ](../Page/イテレータ.md "wikilink")ーとしての `for` をはじめ[各種制御命令も充実しているので](https://ja.wikipedia.org/wiki/#制御構造・サブルーチン "wikilink")、ベクトルや行列の簡潔な処理では書けない制御や大型の計算も記述できる。

### 統計に適した解析環境

最小限の労力で見通しよく解析するために工夫された命令体系を備えている。

  - ベクトル、配列、[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")、[データフレーム](https://ja.wikipedia.org/wiki/#データフレーム "wikilink")（テーブルに相当）、リスト、時系列、などの[動的型付け](../Page/動的型付け.md "wikilink")[データ型](../Page/データ型.md "wikilink")。（後出「[データ型](https://ja.wikipedia.org/wiki/#データ型 "wikilink")」参照）
  - [高階関数](../Page/高階関数.md "wikilink")（データとして関数を操作する関数）をベクトル処理として記述できる
  - 『モデル式』の導入により、複雑な統計[モデル記述と](../Page/モデル_\(自然科学\).md "wikilink")[曲線あてはめ](https://ja.wikipedia.org/wiki/曲線あてはめ "wikilink")等のモデルフィット指示を簡潔で統一的に表現できる
  - 欠損値（NA）・無効値（NULL）・無限大（Inf,-Inf）・非数値（NaN）などの定数とそれらの検査関数
  - [集合](../Page/集合.md "wikilink")計算・[複素数](../Page/複素数.md "wikilink")計算・時間日付計算・因子計算
  - d（[確率密度関数](../Page/確率密度関数.md "wikilink")）・p（[累積分布関数](../Page/累積分布関数.md "wikilink")）・q（[分位関数](https://ja.wikipedia.org/wiki/分位関数 "wikilink")）・r（乱数生成）の4機能と分布名を組合せる命名規則を持つ多次元[確率分布](../Page/確率分布.md "wikilink")機能関数\[4\]
  - sample関数による数値・複素数・文字列などの[標本抽出](../Page/標本_\(統計学\).md "wikilink")（サンプリング）記述
  - [オブジェクト指向](../Page/オブジェクト指向.md "wikilink")（関数・代入式もオブジェクト）（「[オブジェクト指向](https://ja.wikipedia.org/wiki/#オブジェクト指向 "wikilink")」を参照のこと）
  - 単純な構文・[データ型宣言不要](../Page/動的型付け.md "wikilink")・[名前空間](../Page/名前空間.md "wikilink")（「[仕様](https://ja.wikipedia.org/wiki/#仕様 "wikilink")」を参照のこと）
  - 文字列・式の相互変換や[パターンマッチング](../Page/パターンマッチング.md "wikilink")検索・編集などの[文字列](../Page/文字列.md "wikilink")操作
  - 対話的処理だけでなく[バッチ処理](../Page/バッチ処理.md "wikilink")も可能
  - 解析手法の比較検証には欠かせない「定番の検証用データ集」
  - [ニューラルネット](https://ja.wikipedia.org/wiki/ニューラルネット "wikilink")、[決定木](../Page/決定木.md "wikilink")、[クラスター](../Page/クラスター.md "wikilink")、[線形](https://ja.wikipedia.org/wiki/線形 "wikilink")・[非線形](https://ja.wikipedia.org/wiki/非線形 "wikilink")・[自己相関](../Page/自己相関.md "wikilink")モデルなど、多数の高水準組込関数群
  - [画像処理](../Page/画像処理.md "wikilink")・[音声合成](../Page/音声合成.md "wikilink")・[GIS](../Page/地理情報システム.md "wikilink")・[テキストマイニング](../Page/テキストマイニング.md "wikilink")など**CRAN**によって日々強化される拡張機能
  - [擬似乱数](../Page/擬似乱数.md "wikilink")生成法として[メルセンヌ・ツイスタ](../Page/メルセンヌ・ツイスタ.md "wikilink")（[デフォルト設定](../Page/デフォルト_\(コンピュータ\).md "wikilink")）や他の多種の生成法が選択可能
  - すべてのプラットフォームにおいて64bit対応

### 高速な組込み関数群

  - [インタプリタ](../Page/インタプリタ.md "wikilink")でありながらも行列などの複雑なデータ構造に最適化された高速な組込み関数群を持つ（「[処理速度](https://ja.wikipedia.org/wiki/#処理速度 "wikilink")」を参照のこと）
  - 更なる高速計算が要求される場合には[C](../Page/C言語.md "wikilink")・[C++](../Page/C++.md "wikilink")・[FORTRAN](../Page/FORTRAN.md "wikilink")などの外部プログラムと[動的リンク](../Page/動的リンク.md "wikilink")して拡張できる

### 視覚化に優れたグラフ機能

  - データの[グラフ](../Page/統計図表.md "wikilink")・[図解化機能が柔軟であり](https://ja.wikipedia.org/wiki/Category:図 "wikilink")[インフォグラフィック](https://ja.wikipedia.org/wiki/インフォグラフィック "wikilink")環境とでも呼べるほど高度な[グラフ作成ソフト](../Page/グラフ作成ソフト.md "wikilink")機能を持つうえにユーザー独自の図解定義もプログラムが容易である
  - グラフ画像を多くの[画像フォーマット](https://ja.wikipedia.org/wiki/画像フォーマット "wikilink")・商業印刷品質で出力できる（「[データのプロット](https://ja.wikipedia.org/wiki/#データのプロット "wikilink")」を参照のこと）

### データ互換性

  - 他の統計ソフト（[Excelなど](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")）のデータ読込みに対応している\[5\]（「[データ入出力](https://ja.wikipedia.org/wiki/#データ入出力 "wikilink")」参照）。手軽なデータソースの例として、[csv](../Page/Comma-Separated_Values.md "wikilink")[フォーマット](https://ja.wikipedia.org/wiki/フォーマット "wikilink")の[ファイルを](../Page/ファイル_\(コンピュータ\).md "wikilink")「`read.csv("ファイル名")`」というコマンドにより、Rの標準的な[テーブルデータ形式である](../Page/テーブル_\(情報\).md "wikilink")[データフレームに自動変換して読込める](https://ja.wikipedia.org/wiki/#データフレーム "wikilink")。タブ区切りのテキスト形式（TSV）は「read.table("mytsv.txt", header=T, sep="\\t")」で読み込める。
  - [ODBC対応により各種](../Page/Open_Database_Connectivity.md "wikilink")[データベース](../Page/データベース.md "wikilink")にアクセスできる。
  - webなど多様なデータソースからの入力形態に対応した「コネクション機能」を備える。

### ユーザープログラムを配信・利用できるCRANネットワーク機能

  - 世界中のRユーザが開発したRプログラム（[ライブラリ](../Page/ライブラリ.md "wikilink")）（これを「パッケージ」と呼ぶ）が**CRAN** (The Comprehensive R Archive Network) と呼ばれるネットワークで配信されており、それらをR環境単独でオンラインでダウンロード・インストール・アップグレードと一連の管理が可能である。**R-Forge**等の他のサーバーも設定できる。CRANはRにシームレス統合されているため利用可能な機能（基本機能・オプションプログラムの両方）は日々増加拡張している\[6\]。（「[パッケージ](https://ja.wikipedia.org/wiki/#パッケージ "wikilink")」・「[最近の展開](https://ja.wikipedia.org/wiki/#最近の展開 "wikilink")」を参照のこと）

### 教育現場から実務・研究現場へ永続的に利用可能

  - [マルチプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")・[オープンソース](../Page/オープンソース.md "wikilink")で無償であるため誰もが同一作業環境を構築できる
  - 「命令の文法が単純である」・「高水準な統計解析と視覚化機能・永続的な利用に耐える」などの理由で教育機関において[統計学教育や統計処理を必要とする講義で利用し易いうえに](https://ja.wikipedia.org/wiki/統計学#教育 "wikilink")[プログラミングに手間取る事なく統計解析の教育](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")・学習に専念できて解析のプロフェッショナルな道具であるので学習スキルは後々も実践で活かせる（「[プログラムの入手](https://ja.wikipedia.org/wiki/#プログラムの入手 "wikilink")」・「[持続可能な統計環境](https://ja.wikipedia.org/wiki/#持続可能な統計環境 "wikilink")」・「[最近の展開](https://ja.wikipedia.org/wiki/#最近の展開 "wikilink")」を参照のこと）

## 言語仕様

Rはマルチパラダイムなプログラミング言語である。広義の[関数型言語](../Page/関数型言語.md "wikilink")の一つである[Scheme](../Page/Scheme.md "wikilink")の影響を受けていて、リストを基本にした内部処理・[遅延評価](../Page/遅延評価.md "wikilink")・[静的スコープ](../Page/静的スコープ.md "wikilink")などの特徴をもつ。インスタンス生成など[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")機能ももっている。手続的な表記法には[Cの影響がある](../Page/C言語.md "wikilink")。いわゆる「Hello, world」プログラムのコードと実行結果は以下とおり。

``` rsplus
> print("Hello world")
[1] "Hello world"
```

### 制御構造・サブルーチン

`for`, `if`, `while`, `repeat`, `switch`, `break` といった構造化構文がある。自前の関数（手続き）を定義することができ、自前の二項演算子さえも定義することができる。関数は `function` 関数で生成する。次に、[階乗](../Page/階乗.md "wikilink")を計算する自前の関数を生成し、`toyfactorial` として呼出しできるようにする例を示す。

``` rsplus
toyfactorial <- function (n) {
    if (n <= 0) return(NA)
    f <- function(i) {
        if (i == 1) return(1) else return(i * Recall(i-1))
    }
    return(f(n))
}
```

上記は実用的ではないかもしれないが、関数の[ネスティング](../Page/ネスティング.md "wikilink")・[再帰](../Page/再帰.md "wikilink")呼び出し・[スコープ](../Page/スコープ.md "wikilink")の例として挙げた。R言語では[Pascal](../Page/Pascal.md "wikilink")や[Modula-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink")のように関数の[ネスティング](../Page/ネスティング.md "wikilink")が可能である。この例では、関数内部でさらに局所的な関数を生成し、`f` として参照している。スコープも[Pascal](../Page/Pascal.md "wikilink")等と同様、辞書式で、関数 `f` の中ではその外側にある `toyfactorial` の変数が「見える」。`f` は局所変数なので、関数の外側に同じ名前の変数があっても影響を与えない。ただし、Rでは呼び出し[スタック](../Page/スタック.md "wikilink")をさかのぼる[動的スコープ](../Page/動的スコープ.md "wikilink")も実現可能である。

`f` の内部では自分の名前を参照することができないので、自分自身を再帰的に呼び出すために `Recall` 関数を用いている。関数型の引数を利用することもでき、その場合複数の関数が互いに呼び出しあうことができ、また無名の関数をその場で定義して関数型の引数として渡すことができる。一種の[複文](../Page/複文.md "wikilink")のような用途に用いられる。[NA](https://ja.wikipedia.org/wiki/n/a "wikilink")(not available) は統計処理においては欠くことのできない特殊なデータ「欠損値」（欠測値）(missing value)で、データが無効であることを示す。

R言語の関数はそれ自体がオブジェクトであり、ある関数自体を外から参照したり書き換えたりすることができる。関数の本体部分を返す `body` 関数・仮引数リストを返す `formals` 関数・関数に付随する環境を返す `environment` 関数などが用意されている。

渡された式そのものを操作することも可能で、特定の環境（名前とポインタのリスト）の下で与えられた式を評価する `eval` 関数・渡された式の要素を環境に応じて置き換える `substitute` 関数・式を文字列に分解する `deparse` 関数等がある。

関数呼び出しも一種のリストとして処理されており、次のように `call` 関数を用いて、関数名と引数のリストから関数呼び出しオブジェクトを生成できる。

``` rsplus
x <- 1:3
y <- 2:4
z <- call('plot', x, y)
eval(z)
```

関数は[ファイルから読み込むこともでき](../Page/ファイル_\(コンピュータ\).md "wikilink")、さらには、パッケージとしてひとまとまりにすることもできる。

### オブジェクト指向

R言語には[継承や](../Page/継承_\(プログラミング\).md "wikilink")[メソッドの実行時ディスパッチといった](../Page/メソッド_\(計算機科学\).md "wikilink")[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")プログラミングの手法が取り入られており、数多くの総称的な (generic) 関数を持つ。これは同じ関数名であっても、取り扱う[オブジェクトが属している](../Page/オブジェクト_\(プログラミング\).md "wikilink")[クラスによって独自の方法で処理を行うものである](../Page/クラス_\(コンピュータ\).md "wikilink")。Rでは、クラスはオブジェクトに付随する[属性](../Page/属性.md "wikilink")として扱われるものの一つであり、リストとして保持される。

### データ型

[数値型](https://ja.wikipedia.org/wiki/数値型 "wikilink")（[複素数](../Page/複素数.md "wikilink")を含む）・[文字型](https://ja.wikipedia.org/wiki/文字型 "wikilink")・[論理型](https://ja.wikipedia.org/wiki/論理型 "wikilink")といった基本的な型や[ベクトル](../Page/ベクトル.md "wikilink")・[リスト](https://ja.wikipedia.org/wiki/リスト "wikilink")・[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")といった統計処理や情報処理に必要な型を備えている。既述のように、関数それ自体もデータである。データフレームは配列ないしはリストの拡張版で、コラムごとに異なった[データ型](../Page/データ型.md "wikilink")をもてるため、[表](https://ja.wikipedia.org/wiki/表 "wikilink")の形で表現されたデータを格納／操作するのに有用である。データフレームは行列から生成することもあるが、ここではリストとの関連で説明する。

#### ベクトルとリスト

ベクトル型は、データをある順序で並べたものである。 `2:5` または `c(2, 3, 4, 5)` は数値型データ2, 3, 4, 5をこの順序で並べたものである。変数 `a, b` を同じ要素数をもつ数値型データのベクトルとすると、 `a + b` は両ベクトルを要素毎に加算してできた、同じ要素数の数値型ベクトルを返す。 `a + 1` はベクトル `a` の各要素に1を加算したベクトルを返す。 `c('猫', '猫', '犬')` のように文字（列）型・論理型データを要素とするベクトルを作ることもできる。

リスト型は様々な型のデータを並べたものである。ベクトルのリストやリストのリストも可能である。 `list` 関数によって生成できる。

``` rsplus
f1 <- c('猫', '猫', '犬')
f2 <- c(1, 2, 3)
f <- list(field1 = f1, field2 = f2)
```

文字型データを要素とするベクトル `f1` ・数値型データを要素とするベクトル `f2` からリスト `f` が生成される。 `field1, field2` はリストの要素を指す「タグ」である。[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")風のdotted pair listも実装されているので必要に応じて用いられる。

#### データフレーム

さて、上記の2つのベクトル `f1, f2` の要素数は等しい。このような場合、リストをデータフレームに変換できる。

``` rsplus
df <- data.frame(f, row.names = c('たま ', 'みけ', 'ぽち'))
```

dfはデータフレーム型変数であり、各ROW（以下「行」）に「たま」「みけ」「ぽち」のラベルがつく。

もうすこし大きな表、例えば

|      | 種 | 性別 | 月齢  | 愛らしさ |
| ---- | - | -- | --- | ---- |
| たま   | 猫 | ♀  | 1   | 5    |
| しろ   | 猫 | ♂  | 2   | 4    |
| くろ   | 猫 | ♂  | 1   | 5    |
| みけ   | 猫 | ♀  | 3   | 5    |
| ぶち   | 猫 | ♂  | 12  | 3    |
| とら   | 猫 | ♂  | 18  | 2    |
| みゃぁ  | 猫 | ♀  | 30  | 4    |
| 猫じゃ  | 猫 | ♂  | 80  | 0    |
| ぽち   | 犬 | ♀  | 2   | 5    |
| ころ   | 犬 | ♀  | 10  | 5    |
| たろ   | 犬 | ♂  | 40  | 3    |
| じろ   | 犬 | ♂  | 40  | 3    |
| じんぺい | 犬 | ♂  | 50  | 2    |
| わん   | 犬 | ♀  | 60  | 4    |
| のらくろ | 犬 | ♂  | 100 | 5    |

を例えば「犬猫」という名前の変数にデータフレームとして付値（代入に相当）すると、その内容は

```
 犬猫
種 性別 月齢 愛らしさ
たま 猫 ♀ 1 5
しろ 猫 ♂ 2 4
くろ 猫 ♂ 1 5
みけ 猫 ♀ 3 5
ぶち 猫 ♂ 12 3
とら 猫 ♂ 18 2
みゃぁ 猫 ♀ 30 4
猫じゃ 猫 ♂ 80 0
ぽち 犬 ♀ 2 5
ころ 犬 ♀ 10 5
たろ 犬 ♂ 40 3
じろ 犬 ♂ 40 3
じんぺい 犬 ♂ 50 2
わん 犬 ♀ 60 4
のらくろ 犬 ♂ 100 5
```

のように、本来のデータをよく表現するものとなっている。それだけでなく、「猫」「犬」「♀」「♂」などの文字データは内部的に[因子](https://ja.wikipedia.org/wiki/因子 "wikilink")ないしは[カテゴリ](../Page/カテゴリ.md "wikilink")に変換されている。データフレームから特定のデータコラムを抽出するには `変数名$タグ名` 、例えば、 `犬猫$月齢` とする。特定のデータ行だけを抽出するには `subset` 関数または要素の指定 `[ ]` を用いる。例えば、

``` rsplus
猫 <- subset(犬猫, 犬猫['種'] == '猫')
犬 <- 犬猫[犬猫['種'] == '犬']
t.test(猫$愛らしさ, 犬$愛らしさ)
```

は「愛らしさ」の平均値を猫と犬の間で[t検定](https://ja.wikipedia.org/wiki/t検定 "wikilink")する。（この例では、[p値](https://ja.wikipedia.org/wiki/p値 "wikilink") = 0.6537 となる。）

## 機能

Rには標準状態でも統計、検定、解析向けの強力な関数が備わっており、必要に応じて新たな関数を定義することができ（既述のとおり、[Cや](../Page/C言語.md "wikilink")[FORTRAN](../Page/FORTRAN.md "wikilink")などによって記述し、外部でコンパイルした関数を呼び出すこともできる。）、自分でプログラムを書かなくても、多くのパッケージを利用できる。これに加えて、便利な入出力機能、グラフ作成機能を備えている。

### データ入出力

ベクトルを読み込む `scan` 関数や簡易にデータフレームを読み込むことのできる `read.table` 関数等のように[テキスト](../Page/テキスト.md "wikilink")ファイル入出力用のさまざまな関数が用意されている。また、市販の統計解析パッケージ[SPSS](../Page/SPSS.md "wikilink")・[SAS等の独自形式](../Page/SAS_Institute.md "wikilink")[バイナリ](../Page/バイナリ.md "wikilink")データを直接扱うこともできる。画像をバイナリデータとして読むこともでき、読み込み後は行列として扱うことができるので、画像処理にも用い得る。[パイプや](../Page/パイプ_\(コンピュータ\).md "wikilink")[ソケット](../Page/ソケット_\(BSD\).md "wikilink")（[ポート参照](../Page/ポート_\(コンピュータネットワーク\).md "wikilink")）を扱う関数も用意されている。

### データのプロット

`plot` 関数によって多彩なプロットができる。 `plot` は総称的な関数であり、引数として渡されたデータの種類によって、自動的に様々なグラフを描き分ける。他に[ヒストグラム](../Page/ヒストグラム.md "wikilink")を描画する関数、イメージを描画する関数など高レベルの描画関数がある。これらはデフォルトでも機能するが、細かなパラメーターを指定することもできる。加えて、単に線を引いたり点を打ったりする低レベルの描画関数も用意されているため、好みのグラフを生成することができる。プロットは画面に対して行われるだけでなく、[PDF](../Page/Portable_Document_Format.md "wikilink")・[SVG](https://ja.wikipedia.org/wiki/SVG "wikilink")・[PS](../Page/PostScript.md "wikilink")・[PNGといった形式の出力を直接行うこともできる](../Page/Portable_Network_Graphics.md "wikilink")。

[180px](https://ja.wikipedia.org/wiki/ファイル:R-PlotExample.png "wikilink") 図にデフォルトでのプロット例を示す。上から順に `plot(犬猫$種, 犬猫$性別)` ・ `plot(sin(seq(0, 2 *pi, 0.1)))` ・ `image(x <- -50:50, x, x %*% t(x))` の実行結果である。 `seq` 関数は等差級数からなるベクトルを生成する。 `%*%` は行列の積を計算する演算子、 `t` は[転置行列](../Page/転置行列.md "wikilink")を生成する関数である。最初の例では先に扱った動物種毎の性比を表示、次の例では、[正弦](https://ja.wikipedia.org/wiki/正弦 "wikilink")関数（自動的にベクトルの添字が横軸となり、ベクトル生成式が縦軸のラベルとなっている）を表示し、最後の例では、引数を評価する中でベクトルを生成してxに代入し、積を計算し、その各要素の値を色の濃さで表現している。

### ワークスペースの保存

現在の作業状況に名前を付けて保存し、後に再利用することができる。コマンドを発行するコンソールの内容も保存できるので、どのような処理を行って結果を得たかを確実に記録し、再現することができる。発見的操作を伴う研究用途では極めて重要な要素である。

## その他

### 日本語対応

[日本語](../Page/日本語.md "wikilink")に対応しており、関数名・変数名・コメントなどに[日本語](../Page/日本語.md "wikilink")を使える。

### プログラムの入手

**CRAN** (The Comprehensive R Archive Network) からダウンロード・インストールすれば直ちにRを利用開始できる。動作環境は[マルチプラットフォーム](https://ja.wikipedia.org/wiki/マルチプラットフォーム "wikilink")に対応し、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")・[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")・[UNIX](../Page/UNIX.md "wikilink")・[Linux](../Page/Linux.md "wikilink")で動作する。アップデートは精力的に継続され、[ソースコード](../Page/ソースコード.md "wikilink")もCRANにて公開されている。

### パッケージ

Rの用語でパッケージとはR言語のプログラムを配布用の形式に保存したものをいう。関数やデータセット・リファレンスマニュアルなどがひとまとめにされた、いわば、でき合いのアプリケーション・関数ライブラリ・データベースなどといえる。Rにはあらかじめいくつかの標準パッケージが添付されており、たとえば、3層[ニューラルネット](https://ja.wikipedia.org/wiki/ニューラルネット "wikilink") (nnet) などがすぐに利用できる。

CRANを使い、インターネット越しに随時パッケージの一覧検索・ダウンロード・インストール・作業領域へのロード・アップデートをRシステムが管理する。パッケージ間で関数を引用しあう依存関係も自動的に処理され、ユーザーが気を配らなくてよい。Rユーザから見ると、CRANはRとシームレスに統合された機能の一部になっている。世界中のRユーザーが作成したパッケージがCRANで公開されており、これらは自由に使用できる。CRANはR資産の[知識](../Page/知識.md "wikilink")共有メカニズムともいえ、CRANによってRの機能は日々強化されている。R本体のみでも機能は潤沢だが、第一線ユーザ達の実務経験が反映した豊富なパッケージ群は、大きな助力となり得る。

パッケージのダウンロードは自由に手動でできるが、相互依存関係の解決やインストール・アップデート・ロード管理は人手で行なうとわずらわしいので、そのための機能を備えているRシステムに一元管理させるのが推奨される。パッケージの管理をR自体が行なうためには、あらかじめいずれかのCRANサイトを手元のRシステムに登録設定しておく必要がある。設定は一度行なえばよい\[7\]。

なお、パッケージを用いなければ上記設定をしなくてもRを使うことはできる、また、[オフライン](https://ja.wikipedia.org/wiki/オフライン "wikilink")のみでRを使用しても問題はない。パッケージが必要になった時に改めてCRANに接続するようにすればよい。

Rユーザー自身がパッケージを作成するためのツールキットが、標準パッケージとしてRに添付されている。

### CUIとGUI

Rは以下の標準インタフェース画面を通じて用いる。

  - コマンド入力や出力を[CUIで行う](../Page/キャラクタユーザインタフェース.md "wikilink")「コンソールウィンドウ」
  - コマンドやデータの文字列を編集しそれらをコンソールへ入力する「Rエディタ」
  - ロードしたオブジェクトを管理する「ワークスペースブラウザ」
  - データテーブルをスプレッドシート状の形式で編集できる「データエディタ」
  - CRANからパッケージをインストールするための「パッケージインストーラ」
  - インストール済みパッケージのロード管理をする「パッケージマネージャ」
  - 各パッケージに含まれているデータセットをブラウズする「データマネージャ」
  - 基本設定を行う「環境設定」

厳密に言えば、この方式はマルチウインドウの[GUIと言えなくはないが](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、Rを操作する「コンソールウィンドウ」は「命令をテキスト入力して使うCUI」である。この点についてユーザーの間でも商業ソフトに見られるような[マウスオペレーションを望む声は多く](../Page/マウス_\(コンピュータ\).md "wikilink")、それに呼応して**R Commander**というGUIがCRANからパッケージとして提供されている。

R標準以外のGUIを利用する方法として、**RStudio**・**Tinn-R**がある。なお、他にも、GNUの時系列解析環境である[gretl](https://ja.wikipedia.org/wiki/gretl "wikilink")があり、そのGUIを通じてRを操作できる。（[gretl](https://ja.wikipedia.org/wiki/gretl "wikilink")はR以外に対しても使用できる。）また、データ分析プロセスをフローチャート式に描くことでプログラムできる**R AnalyticFlow**というソフトウェアも企業から無償提供されている。

### 処理速度

[インタプリタ](../Page/インタプリタ.md "wikilink")言語であることから、R言語の処理速度は不当に低く評価されることが多い。しかし[S言語](../Page/S言語.md "wikilink")商用版である[S-PLUS](../Page/S-PLUS.md "wikilink")よりも多くの場合高速であるばかりか、汎用行列系言語のスタンダードとも言える[MATLAB](../Page/MATLAB.md "wikilink")やその派生語の[GNU Octave](../Page/GNU_Octave.md "wikilink")・[Scilab](../Page/Scilab.md "wikilink")よりも総合的に高速であるという評価例がある。

「[特徴](https://ja.wikipedia.org/wiki/#特徴 "wikilink")」にもあるとおり、「統計計算に特化した情報処理」機能を充分生かしてこそ高い生産性を発揮できる。生産性の最たる「計算速度」への効果に関しては、基本的な作法が幾つも提唱されている。

R言語プログラムの高速化を目指すときは、R言語に組み込みの関数群が充分に高速化されているので、これらを活用すべきである。組み込み関数と同じ機能を新たにコーディングすることは避けなければならない。

ベクトルを纏めて扱える関数がある場合では、それを用いる。ベクトル要素ごとに分けて処理すると、速度は低下する。論理判断を含んだ[ループ処理をするのは](../Page/ループ_\(プログラミング\).md "wikilink")、多くの場合、間違った方法である。それに替えて論理添字集合の操作で一挙に答えを出すといった方法が推奨される。（R言語に限らず行列系言語何れにおいても、高速化するには「forやrepeatといったループ系の命令を無駄に使わず、極力ベクトル化（あるいは行列化）する」ことが基本である。）

### 持続可能な統計環境

教育課程から実務への移行や職務環境の変化が生じると、利用可能な計算資源というものは変わってしまう。

R言語の登場以前は、学術論文など社会的信頼性を要求される統計データの処理環境といえば高額な[プロプライエタリ](https://ja.wikipedia.org/wiki/プロプライエタリ "wikilink")ソフトウェアばかりが前提とされた。だが、これでは継続的な予算がつかなくなれば環境のサポートやアップデートは停止してしまい、極端な話、予算が元から無い立場に異動してしまうと在来の統計処理が何もできなくなる事態になり兼ねない。

[統計](../Page/統計.md "wikilink")家にとっては、今まで習得し錬成した手法と蓄積したデータとその運用方法は例え環境が変化しようとも継承できなくては困る。この意味から、他に多く存在する[プロプライエタリ](https://ja.wikipedia.org/wiki/プロプライエタリ "wikilink")・「生かすも殺すも版権保持者の都合次第」というような統計処理ツールと比べ、R言語のような[オープンソース](../Page/オープンソース.md "wikilink")で、それゆえ、CRAN[パッケージ等によって日々機能拡張し得る](https://ja.wikipedia.org/wiki/#パッケージ "wikilink")、つまり、「[フリーソフトウェアの精神に則り永続的で世界規模な](../Page/フリーソフトウェアの定義.md "wikilink")[集合知](https://ja.wikipedia.org/wiki/集合知 "wikilink")に支えられ、無償でありながら高い信頼に値する。」統計環境というのは、[統計](../Page/統計.md "wikilink")家の長期的な生産性に大きく寄与する「持続可能な統計環境」と言える。

### 展開

Rパッケージ数の飛躍的な増大に見られるとおり、[統計学](../Page/統計学.md "wikilink")を超えて学問分野や業界を問わず、[金融工学](../Page/金融工学.md "wikilink")・[時系列分析](https://ja.wikipedia.org/wiki/時系列分析 "wikilink")・[機械学習](../Page/機械学習.md "wikilink")・[データマイニング](../Page/データマイニング.md "wikilink")・[バイオインフォマティクス](../Page/バイオインフォマティクス.md "wikilink")など、柔軟なデータ解析や視覚化そして知識共有の需要に応え得るR言語の普及は世界的な広がりを見せている。

近年では、[生命科学](../Page/生命科学.md "wikilink")分野のためのRパッケージプロジェクトの**Bioconductor**が立ち上がり、既に多くの[ゲノム](../Page/ゲノム.md "wikilink")スケール関連のパッケージが配布されている。ゲノムスケールデータの諸情報、すなわち、大規模遺伝子発現プロファイル・質量分析データ・蛋白質相互作用データなどを解析するプログラムやデータをRパッケージとしてRユーザーに配布する仕組みである。

また、[アメリカ食品医薬品局](../Page/アメリカ食品医薬品局.md "wikilink") (FDA) への、嘗て[SAS一辺倒だった](../Page/SAS_Institute.md "wikilink")、薬事申請や報告の際にも現在ではRが用いられている\[8\]。

[SPSS](../Page/SPSS.md "wikilink")では、[2009年](../Page/2009年.md "wikilink")より製品名を[PASW Statisticsと改め](https://ja.wikipedia.org/wiki/PASW_Statistics "wikilink")、R言語との連携強化を発表した。[SPSS](../Page/SPSS.md "wikilink")のインタフェースからR言語の機能を使える\[9\]。

[2009年](../Page/2009年.md "wikilink")[7月](https://ja.wikipedia.org/wiki/7月 "wikilink")に[SAS Instituteは](../Page/SAS_Institute.md "wikilink")"R Interface Coming to SAS/IML Studio"によってSASからR言語へのインタフェースを提供することを発表した\[10\]。[SAS InstituteのWebサイトには](../Page/SAS_Institute.md "wikilink")、新たな[統計](../Page/統計.md "wikilink")手法は大抵の場合は真先にR言語上で実装されるという現状を踏まえて、[SAS](../Page/SAS.md "wikilink")ユーザーの要望に応えてインタフェースの提供を行なう、との旨が述べられている。

RGLと呼ばれる3Dグラフ描画パッケージも提供されている。このパッケージを使用することでOpenGLにより実現される高速かつ美麗な3DCGを用いてデータのグラフ化が出来る。

## 脚注

### 注釈

### 出典

## 関連項目

  - [S言語](../Page/S言語.md "wikilink")

## 学習参考書等

  - U. リゲス：「Rの基礎とプログラミング技法」、丸善出版、ISBN 978-4621061312，（2012年2月）｡
  - Hadley Wickham：「R言語徹底解説」、共立出版、ISBN 978-4320123939、（2016年2月）｡

## 外部リンク

  -
<!-- end list -->

  - 国内

<!-- end list -->

  - [フリーの統計環境 R について](http://www.is.titech.ac.jp/is-wiki/?maselab/R) - 間瀬茂（東京工業大学）による簡単な紹介や公式マニュアル『Introduction to R』 の和訳「R 基本統計関数マニュアル」
  - [フリー統計ソフトEZR (Easy R)](http://www.jichi.ac.jp/saitama-sct/SaitamaHP.files/statmed.html) - 自治医科大学附属さいたま医療センター血液科
  - [R言語](http://wwwhum.meijo-u.ac.jp/labs/hh002/r/rtop.html) - 名城大学人間学部 神谷俊次研究室
  - [R-Tips](http://cse.naro.affrc.go.jp/takezawa/r-tips/r.html) - 舟尾 暢男氏
  - [統計分析フリーソフト「R」](http://www.statistics.co.jp/reference/software_R/free_software-R.htm) - 法人 統計科学研究所
  - [biostatistics（生物統計学）](https://stat.biopapyrus.net/) （R基礎編、R発展編、Rグラフィックス、ggplot2、統計学）- biopapyrus
  - [Rで解析：手軽で綺麗なグラフが欲しいなら、ggplot2のまとめです。](https://www.karada-good.net/analyticsr/r-78) - からだにいいもの
  - [RjpWiki](http://www.okadajp.org/RWiki/) （Rに関する情報交換を目的とした日本語Wiki）

<!-- end list -->

  - 海外

<!-- end list -->

  - [The Comprehensive R Archive Network (CRAN)](http://cran.r-project.org/)
  - [R-Forge](http://r-forge.r-project.org/index.php)
  - [The R Journal](http://journal.r-project.org/index.html)
  - [R - Documentation](http://www.r-project.org/other-docs.html)
  - [RSeek.org R-project Search Engine](http://www.rseek.org/index.php)  - R言語関連に特化させた[検索](../Page/検索.md "wikilink")サイトである。
  - [Hadley Wickham:"Advanced R"](http://adv-r.had.co.nz/)

{{-}}

[Category:数値解析ソフトウェア](https://ja.wikipedia.org/wiki/Category:数値解析ソフトウェア "wikilink") [Category:Linux向け数値解析ソフトウェア](https://ja.wikipedia.org/wiki/Category:Linux向け数値解析ソフトウェア "wikilink") [Category:統計処理ツール](https://ja.wikipedia.org/wiki/Category:統計処理ツール "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink") [Category:関数型言語](https://ja.wikipedia.org/wiki/Category:関数型言語 "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")

1.  [GNU R](http://directory.fsf.org/wiki/GNU_R#tab=Overview)
2.  [S言語](../Page/S言語.md "wikilink")は[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に[ACMの](../Page/Association_for_Computing_Machinery.md "wikilink")[ソフトウェアシステム賞を獲得した](https://ja.wikipedia.org/wiki/ACMソフトウェアシステム賞 "wikilink")。
3.  簡略化のために、円の[第一象限でカウントして](https://ja.wikipedia.org/wiki/直交座標系#平面上の直交座標系 "wikilink")4倍する方法をとる。
4.  [Rにおける確率分布](http://www.okadajp.org/RWiki/?R%E3%81%AB%E3%81%8A%E3%81%91%E3%82%8B%E7%A2%BA%E7%8E%87%E5%88%86%E5%B8%83)
5.  [Rがインポート・エクスポートできるデータ形式](http://www.okada.jp.org/RWiki/index.php?Rがインポート・エクスポートできるデータ形式)
6.  [CRANパッケージリスト](http://www.okada.jp.org/RWiki/index.php?CRANパッケージリスト)
7.  [CRAN国内ミラーの使い方](http://www.okada.jp.org/RWiki/index.php?CRAN国内ミラーの使い方)
8.  [RとFDA](http://www.okadajp.org/RWiki/?R%E3%81%A8FDA)
9.  [IBM RユーザーのためのIBM SPSS Statistics Developer](http://www-06.ibm.com/software/jp/analytics/spss/store/stats/pasw_sd.html)
10. [R Interface Now Available in SAS/IML Studio](http://support.sas.com/rnd/app/studio/Rinterface2.html)