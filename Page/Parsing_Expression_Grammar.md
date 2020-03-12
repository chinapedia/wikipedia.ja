> この記事は[Parsing Expression Grammar](https://ja.wikipedia.org/wiki/Parsing_Expression_Grammar)から翻訳されています。


**Parsing Expression Grammar** (**PEG**, Parsing Expression Grammar) は、[分析的形式文法の一種であり](../Page/形式文法.md "wikilink")、[形式言語](../Page/形式言語.md "wikilink")をその言語に含まれる[文字列](../Page/文字列.md "wikilink")を認識するための一連の規則を使って表したものである。PEGは[再帰下降構文解析](../Page/再帰下降構文解析.md "wikilink")を文法を示すためだけに純粋に図式的に表現したものと見ることもでき、具体的な[構文解析器](../Page/構文解析器.md "wikilink")の実装やその用途とは独立している。

PEGにおける構文（文法）の定義は[文脈自由文法](../Page/文脈自由文法.md "wikilink")の[バッカス・ナウア記法](../Page/バッカス・ナウア記法.md "wikilink")によるそれに似ているが、文脈自由文法では一般に「｜」（縦棒、[バーティカルバー](../Page/バーティカルバー.md "wikilink")）で表される「これらのうちどれか」ではなく、「最初の解析がうまくいったらそれを、失敗なら次を順に試してゆき、成功したものを採用」（「/」であらわす）という意味を使う。

このため、文脈自由文法とは異なり、PEGには[曖昧さは存在しない](../Page/曖昧な文法.md "wikilink")。文字列を構文解析する場合、正しい[構文木](https://ja.wikipedia.org/wiki/構文木 "wikilink")は常に1つしかない。このためPEGはコンピュータ言語の構文解析に向いており、一方、[自然言語](../Page/自然言語.md "wikilink")の多義性を、そのまま複数の構文木が可能である、という形で形式化するのには向かない。

## 定義

形式的には、PEGは次の要素からなる。

  - [非終端記号](https://ja.wikipedia.org/wiki/非終端記号 "wikilink")の[有限集合](../Page/有限集合.md "wikilink") *N*
  - [終端記号](https://ja.wikipedia.org/wiki/終端記号 "wikilink")の有限集合 Σ（*N*とは交わらない）
  - 規則の有限集合 *P*

*P* に含まれる各規則は、*A* ← *e* という形式であり、*A* は非終端記号、*e* は、次のように構築される記号およびメタ記号の列である。前述のように、文脈自由文法における「どれかを選択」という意味の「 | 」の代わりに、「順番に試す」という意味の「 / 」を使うことが特徴である。

1.  「atomic parsing expression」は次のいずれかである。
      - 任意の終端記号
      - 任意の非終端記号
      - 空文字列 ε

<!-- end list -->

1.  任意の既存のparsing expressionを *e*, *e*<sub>1</sub>, *e*<sub>2</sub> としたとき、以下のように構築されるものもparsing expressionである。
      - 並び: *e*<sub>1</sub> *e*<sub>2</sub>
      - 選択: *e*<sub>1</sub> / *e*<sub>2</sub>
      - ゼロ個以上: *e*\*
      - 1個以上: *e*+
      - 省略可能: *e*?
      - AND predicate: &*e*
      - NOT predicate: \!*e*

[文脈自由文法](../Page/文脈自由文法.md "wikilink")や他の[生成文法](https://ja.wikipedia.org/wiki/生成文法 "wikilink")とは異なり、PEGでは、ある非終端記号が左辺にくる規則は常に1つしか存在しない。すなわち、規則群は「定義」であり、各非終端記号には1つしか定義が存在しない。

### 解釈

PEGにおける各非終端記号は、ある意味で[再帰下降構文解析](../Page/再帰下降構文解析.md "wikilink")における構文解析[関数](https://ja.wikipedia.org/wiki/関数 "wikilink")を表現しており、それに対応するparsing expressionはその関数のコードであると解釈できる。各構文解析関数は、引数として入力文字列をとり、以下のいずれかの結果を返す。

  - 「成功」- 引数として与えられた文字列からいくつかの文字を「消費」するなどした場合
  - 「失敗」- 入力を全く消費できなかった場合

非終端記号は入力を全く消費しなくとも成功と見なされる場合があり、単に返される結果だけで失敗と区別される。

1つの終端記号からなるatomic parsing expressionは、入力文字列の先頭の文字と一致した場合に成功し、その入力文字を消費する。さもなくば、そのparsing expressionは失敗の結果を返す。空文字列だけからなるatomic parsing expressionは、入力を消費せずに常に成功と見なされる。非終端記号 *A* からなるatomic parsing expressionは、非終端関数 *A* の[再帰呼び出し](https://ja.wikipedia.org/wiki/再帰呼び出し "wikilink")を表している。

並び *e*<sub>1</sub> *e*<sub>2</sub> は、まず *e*<sub>1</sub> を呼び出し、*e*<sub>1</sub> が成功なら続いて *e*<sub>2</sub> を *e*<sub>1</sub> が消費した文字列を除いた入力文字列を引数として呼び出し、その結果を全体の結果として返す。*e*<sub>1</sub> か *e*<sub>2</sub> のいずれかが失敗した場合、並び *e*<sub>1</sub> *e*<sub>2</sub> 全体が失敗となる。

選択 *e*<sub>1</sub> / *e*<sub>2</sub> は、まず *e*<sub>1</sub> を呼び出し、*e*<sub>1</sub> が成功ならそれを結果として即座に返す。あるいは *e*<sub>1</sub> が失敗なら入力文字列を *e*<sub>1</sub> を呼び出す前の元の位置に[バックトラッキング](../Page/バックトラッキング.md "wikilink")して *e*<sub>2</sub> を呼び出し、*e*<sub>2</sub> の結果を返す。

ゼロ個以上、1個以上、省略可能の場合、それぞれゼロ個以上、1個以上、ゼロ個または1個の *e* が続くものとして入力を消費する。しかし、[文脈自由文法](../Page/文脈自由文法.md "wikilink")や[正規表現](../Page/正規表現.md "wikilink")とは異なり、PEGにおける繰り返しは常に貪欲であり、マッチし続ける限り入力を消費し、バックトラックしない。正規表現では貪欲にマッチするものの、失敗するともっと短いマッチを試すためにバックトラックする。例えば、a\* という表現は 'a' が連続する限り入力文字列を消費し、(a\* a) という表現は最初の (a\*) が全ての 'a' の並びを消費してしまうため、最後の (a) にマッチする 'a' がなくなるので、常に失敗する。

AND predicateとNOT predicateはsyntactic predicateである。&*e* という表現は *e* をまず呼び出して、それが成功した場合には成功し、失敗した場合には失敗する。しかし、どちらの場合も「入力文字列を消費しない」。逆に \!*e* という表現は *e* が失敗した場合には成功し、成功した場合には失敗する。こちらも入力文字列は消費しない。*e* には任意の複雑な表現が当てはまるので、これらは強力な[先読み](../Page/先読み.md "wikilink")機能となる。

### 例

以下は、非負整数についての四則演算を行う数式を認識するPEGである。

  -
    *Value* ← \[0-9\]+ / '(' *Expr* ')'
    *Product* ← *Value* (('\*' / '/') *Value*)\*
    *Sum* ← *Product* (('+' / '-') *Product*)\*
    *Expr* ← *Sum*

この例では、終端記号は文字であり、シングルクオートで囲んで `'('` や `')'` のように表されている。範囲 `[0-9]` も10種類の数字 0 から 9 を表している。このような範囲表現は[正規表現](../Page/正規表現.md "wikilink")でも用いられている。非終端記号は各規則の左辺に現れている *Value*, *Product*, *Sum*, *Expr* である。

次の例ではシングルクオートを省略して読みやすくしている。小文字は終端記号、大文字のイタリック体が非終端記号である。実際のPEGパーサでは、小文字で表される終端記号は引用記号で囲む必要がある。

parsing expression (a/b)\* は任意の長さの a および b の並びにマッチする。規則 *S* ← a *S*? b は単純な[文脈自由マッチング言語](../Page/文脈自由言語.md "wikilink") \(\{ a^n b^n : n \ge 1 \}\) を表している。以下のPEGは文脈自由でない言語 \(\{ a^n b^n c^n : n \ge 1 \}\) を表している。

  -
    *S* ← &(*A* \!b) a+ *B* \!.
    *A* ← a *A*? b
    *B* ← b *B*? c

次の例は、再帰的規則でC言語風の if/then/else 文にマッチするものである。"else" 節は省略可能で、'/' オペレータの暗黙の優先順位付けによって常に最も内側の "if" と対応付けられる。[文脈自由文法](../Page/文脈自由文法.md "wikilink")では、else の対応関係は曖昧となる。

  -
    *S* ← if *C* then *S* else *S* / if *C* then *S*

foo &(bar) というparsing expressionは、"bar" というテキストが後に続く場合のみ "foo" というテキストにマッチし消費する。foo \!(bar) というparsing expressionは、"bar" というテキストが後に続かない場合のみ "foo" というテキストにマッチし消費する。\!(a+ b) a という表現は、'a' の任意の長さの並びに 'b' が続く形式でない場合のみ 'a' にマッチする。

以下の再帰的規則はPascal風の (\* このように (\* 入れ子に \*) できる \*) コメントの構文にマッチするものである。コメント記号はPEGのオペレータと区別するためにダブルクオートで囲んでいる。

  -
    *Begin* ← "(\*"
    *End* ← "\*)"
    *C* ← *Begin* *N*\* *End*
    *N* ← *C* / (\!*Begin* \!*End* *Z*)
    *Z* ← *any single character*

## PEGに基づいた構文解析器の実装

PEGはそのまま[再帰下降構文解析](../Page/再帰下降構文解析.md "wikilink")器に変換可能である\[1\]。先読みが無制限に可能であるため、最悪の場合[指数関数時間](https://ja.wikipedia.org/wiki/指数関数時間 "wikilink")かかる。

解析の途中結果を[メモ化](../Page/メモ化.md "wikilink")し、各構文解析関数が同じ入力位置について高々1回までしか呼ばれないようにすると、任意のPEGを **[Packrat Parser](https://ja.wikipedia.org/wiki/パックラット構文解析 "wikilink")** に変換でき、メモリ領域を余分に必要とするものの、常に[線形時間](../Page/線形時間.md "wikilink")で動作する。

Packrat Parser\[2\] は再帰下降構文解析器と構造的にはよく似た[構文解析器](../Page/構文解析器.md "wikilink")である。ただし、Packrat Parser は[相互再帰](https://ja.wikipedia.org/wiki/相互再帰 "wikilink")構文解析関数を呼び出す度に途中結果をメモ化する。このメモ化によって Packrat Parser は、多くの[文脈自由文法](../Page/文脈自由文法.md "wikilink")と任意のPEG（文脈自由でない場合も含む）を[線形時間](../Page/線形時間.md "wikilink")で構文解析できるようになっている。

## 利点

PEGは[正規表現](../Page/正規表現.md "wikilink")より強力であり、よい代替手法となる。例えば、正規表現は再帰的ではないため本質的に括弧の対応付けができないが、PEGでは可能である。

PEGは上述のように Packrat Parser を使えば線形時間で構文解析可能である。

文脈自由文法で表される言語の構文解析器（例えば[LR法](../Page/LR法.md "wikilink")）は、事前に入力を[字句解析](../Page/字句解析.md "wikilink")しておく必要がある。字句解析は線形時間内で先読みしつつ構文解析するにあたって必要となるものである。しかしPEGは事前に字句解析する必要はなく、字句解析規則を他の構文規則と同じように記述できる。

文脈自由文法は多くの場合本質的に曖昧であり、曖昧でない言語を記述する場合でもそのようになる傾向がある。C、C++、Javaにおける else の曖昧さの問題はその例である。通常、このような曖昧さは文法以外の規則を適用することで解決される。PEGでは、優先順位が厳密に決まるため、そのような曖昧さは発生しない。

## 欠点

PEGは、文字列上で位置を変更せずにある規則が自分自身を呼び出すという[左再帰](../Page/左再帰.md "wikilink")規則を表現できない。例えば、上述の数式の文法では、次のような規則としたほうが自然である。

  -
    *Value* ← \[0-9.\]+ / '(' *Expr* ')'
    *Product* ← *Expr* (('\*' / '/') *Expr*)\*
    *Sum* ← *Expr* (('+' / '-') *Expr*)\*
    *Expr* ← *Product* / *Sum* / *Value*

この場合、`Expr` とマッチするかを判定するには、まず `Product` とマッチするかを判定する必要があり、`Product` とマッチするかを判定するには、`Expr` とマッチするかを判定しなければならない。これは不可能である（[循環定義](../Page/循環定義.md "wikilink")になっていて完了しない）。

しかし、左再帰規則は常に左再帰を使わない形式で書き換え可能である。例えば、左再帰規則で任意長の繰り返しを表すと（文脈自由文法では）次のようになる。

  -
    *string-of-a* ← *string-of-a* 'a' | 'a'

PEGではこれを + オペレータを使って書き換え可能である。

  -
    *string-of-a* ← 'a'+

## PEGパーサ生成器ほか

PEGパーサ（多くはPackratパーサ）を生成する[パーサジェネレータ](../Page/パーサジェネレータ.md "wikilink")やパーサコンビネータライブラリなどを以下に示す。

  - [Parser Grammar Engine](http://search.cpan.org/dist/parrot/compilers/pge/README.pod) (PGE) - [Parrot](../Page/Parrot.md "wikilink")[バイトコード](../Page/バイトコード.md "wikilink")を生成する構文解析エンジン
  - [Pappy](http://www.pdos.lcs.mit.edu/~baford/packrat/thesis/) - Haskell用パーサ生成器
  - [Frisby](http://repetae.net/computer/frisby/) - Haskell用パーサ生成器
  - [Rats\!](http://www.cs.nyu.edu/rgrimm/xtc/) - Java用パーサ生成器
  - [grammar::peg](http://tcllib.sourceforge.net/doc/peg.html) - TCLライブラリ
  - [cl-peg](http://common-lisp.net/project/cl-peg/) - Common Lisp用生成器
  - [packrat](http://www.call-with-current-continuation.org/eggs/packrat.html) - CHICKEN Scheme用 Packrat Parser 生成器
  - [LPeg](http://www.inf.puc-rio.br/~roberto/lpeg/lpeg.html) - Luaライブラリ
  - [re::engine::LPEG](http://search.cpan.org/dist/re-engine-LPEG/) - Perl（5.10.0以降）の正規表現エンジンをLPegに差し替えるモジュール
  - [PyPy rlib parsing](http://codespeak.net/pypy/dist/pypy/doc/rlib.html#parsing) - Python用 Packrat Parser 生成器（[ソース](http://codespeak.net/pypy/dist/pypy/rlib/parsing/)）
  - [pyPEG](http://fdik.org/pyPEG/) - Python用パーサインタプリタ
  - [ppeg](http://bitbucket.org/pmoore/ppeg/src/) - [Python](../Page/Python.md "wikilink") LPegのPython版
  - [PEG ¥ Openpear](http://openpear.org/package/PEG) - PHP用パーサコンビネータ
  - [Parboiled](http://parboiled.org) - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[Scala](../Page/Scala.md "wikilink")用
  - [Mouse](http://mousepeg.sourceforge.net) - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")用
  - [PetitParser](http://source.lukas-renggli.ch/petit.html) - [Smalltalk](../Page/Smalltalk.md "wikilink")用
  - [Kouprey](http://www.deadpixi.com/Deadpixi.COM/Kouprey.html), [PEG.js](http://pegjs.majda.cz/) - [JavaScript](../Page/JavaScript.md "wikilink")用
  - [Boost::Spirit V2](http://spirit.sourceforge.net/) - [C++](../Page/C++.md "wikilink")用
  - [Narwhal](http://sourceforge.net/projects/narwhal/) - C用パーサ生成器
  - [PackCC](http://sourceforge.net/p/packcc/wiki/Home/) - [C用](../Page/C言語.md "wikilink") Packrat Parser 生成器（左再帰サポート）
  - [peg/leg](http://piumarta.com/software/peg/) - [C用](../Page/C言語.md "wikilink")
  - [pegc](http://fossil.wanderinghorse.net/repos/pegc/index.cgi/index) - [C用](../Page/C言語.md "wikilink")
  - [peg-sharp](http://code.google.com/p/peg-sharp/) - [C\#用](../Page/C_Sharp.md "wikilink")
  - [Treetop](http://treetop.rubyforge.org/), [Citrus](https://github.com/mjijackson/citrus/) - [Ruby](../Page/Ruby.md "wikilink")用
  - [Perl6](http://dev.perl.org/perl6/) - 言語に組込み
  - [pyparsing](http://pyparsing.wikispaces.com/) - [Python](../Page/Python.md "wikilink")用PEGライブラリ
  - [pijnu](http://spir.wikidot.com/pijnu) - [Python](../Page/Python.md "wikilink")によるテキストパースツール
  - [Neotoma](https://github.com/seancribbs/neotoma/) - [Erlang](../Page/Erlang.md "wikilink")用
  - [clj-peg](http://www.lithinos.com/clj-peg/) - [Clojure](https://ja.wikipedia.org/wiki/Clojure "wikilink")用
  - [FParsec](http://www.quanttec.com/fparsec/) - [F\#用](../Page/F_Sharp.md "wikilink")
  - [EPEG](http://dev.eiffel.com/PEG_Library) - [Eiffel](../Page/Eiffel.md "wikilink")用
  - [Aurochs](http://aurochs.fr/) - [OCaml用](https://ja.wikipedia.org/wiki/Objective_Caml "wikilink")
  - [rust-peg](https://github.com/kevinmehall/rust-peg) - [Rust用](https://ja.wikipedia.org/wiki/Rust_\(プログラミング言語\) "wikilink")
  - [pegtl](http://code.google.com/p/pegtl/) - [C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")用
  - [chilon::parser](http://chilon.net/library.html) - [C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")用
  - [LL(1) DSL PEG parser (toolkit framework)](http://expressionscompiler.codeplex.com/)
  - [Nemerle.Peg](http://nemerle.googlecode.com/svn/nemerle/trunk/snippets/peg-parser) - [Nemerle](../Page/Nemerle.md "wikilink")用
  - [peg](https://github.com/pointlander/peg) -- [Go言語](https://ja.wikipedia.org/wiki/Go言語 "wikilink")用
  - [pigeon](https://github.com/mna/pigeon) - [Go言語](https://ja.wikipedia.org/wiki/Go言語 "wikilink")用

## 関連項目

  - [形式文法](../Page/形式文法.md "wikilink")
  - [正規表現](../Page/正規表現.md "wikilink")
  - [REBOL](../Page/REBOL.md "wikilink")

## 参考文献

## 外部リンク

  - [Parsing Expression Grammars: A Recognition-Based Syntactic Foundation](http://www.brynosaurus.com/pub/lang/peg-slides.pdf) (PDF)
  - The [PEG Board](http://www.ieuc.org/research/specific-projects/peg-board.html) at The Institute for End User Computing - 正規表現の代わりにPEGを広めようとしている
  - [The Packrat Parsing and Parsing Expression Grammars Page](http://www.pdos.lcs.mit.edu/~baford/packrat/)
  - [人工言語](https://ja.wikipedia.org/wiki/人工言語 "wikilink")[ロジバン](https://ja.wikipedia.org/wiki/ロジバン "wikilink")は[かなり大規模なPEG文法](http://www.digitalkingdom.org/~rlpowell/hobbies/lojban/grammar/)を持っており、曖昧さのない解釈が可能となっている。

[Category:形式言語](https://ja.wikipedia.org/wiki/Category:形式言語 "wikilink") [Category:構文解析_(プログラミング)](https://ja.wikipedia.org/wiki/Category:構文解析_\(プログラミング\) "wikilink")

1.  "Packrat Parsing: a Practical Linear-Time Algorithm with Backtracking" §3.1.1 pp.32〜33
2.