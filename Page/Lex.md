> この記事は[Lex](https://ja.wikipedia.org/wiki/Lex)から翻訳されています。


**Lex**(レック、レックス)はレキシカルアナライザ（[字句解析](../Page/字句解析.md "wikilink")プログラム、[字句解析器](https://ja.wikipedia.org/wiki/字句解析器 "wikilink")）を生成する[プログラムである](../Page/プログラム_\(コンピュータ\).md "wikilink")。[コンパイラ](../Page/コンパイラ.md "wikilink")の作成のために[パーサジェネレータ](../Page/パーサジェネレータ.md "wikilink")の[yacc](https://ja.wikipedia.org/wiki/yacc "wikilink")とともに使用されることも多い。Lexは[エリック・シュミット](../Page/エリック・シュミット.md "wikilink")とマイク・レスクによって書かれ[unix](https://ja.wikipedia.org/wiki/unix "wikilink")における標準のレキシカルアナライザとなっており、[POSIX](../Page/POSIX.md "wikilink")標準ともなっている。Lexと同等の機能を有し性能が改善されているFlex([英語版](https://ja.wikipedia.org/wiki/:en:Flex_lexical_analyser "wikilink"))がある\[1\]。

## 概要

### 名称

Lexはレキシカルアナライザジェネレータである。すなわちレキシカルアナライザ（[字句解析](../Page/字句解析.md "wikilink")プログラム、[字句解析器](https://ja.wikipedia.org/wiki/字句解析器 "wikilink")）の生成ツールであり、Lexの名称も英語の**Lex**ical analysisからきている。

### 用途

[字句解析](../Page/字句解析.md "wikilink")はテキスト中の文字列の変換、カウント、抽出などさまざまな目的に使われ、その応用領域は、[コンパイラ](../Page/コンパイラ.md "wikilink")やコンバータの作成を筆頭に、自然言語処理や簡単な整形まで幅広い。

このうち、[コンパイラ](../Page/コンパイラ.md "wikilink")におけるレキシカルアナライザの位置づけを、以下に説明する。 [プログラムを](../Page/プログラム_\(コンピュータ\).md "wikilink")[中間言語](../Page/中間言語.md "wikilink")あるいは機械語に変換する[コンパイラ](../Page/コンパイラ.md "wikilink")は、一般的に[ソース](../Page/ソース.md "wikilink")を入力し[構文木](https://ja.wikipedia.org/wiki/構文木 "wikilink")を出力する[構文解析](../Page/構文解析.md "wikilink")部(1)と、その[構文木](https://ja.wikipedia.org/wiki/構文木 "wikilink")を入力し中間言語コードまたは機械語を出力する[コード生成](https://ja.wikipedia.org/wiki/コード生成 "wikilink")部(2)からなる。

`コンパイラ`
`　├構文解析部(1)`
`　│　├字句解析器(1.1)　←〔ソース〕`
`　│　│呼出し↑↓`
`　│　│　　　↑〔トークン列〕`
`　│　│　　　↑↓`
`　│　└構文解析器(1.2)`
`　│　　　　　↓`
`　│　　〔構文木〕`
`　│　　　　　↓`
`　└コード生成部(2)　　　→〔中間言語コードまたは機械語〕`

このうち(1)の前半は、[ソース](../Page/ソース.md "wikilink")を入力し[トークン](../Page/トークン.md "wikilink")（語彙素）列を出力する[字句解析器](https://ja.wikipedia.org/wiki/字句解析器 "wikilink")（レキシカルアナライザ、トークナイザ、スキャナ）(1.1)である。 後半は、その[トークン](../Page/トークン.md "wikilink")列を入力し、[構文規則](https://ja.wikipedia.org/wiki/構文規則 "wikilink")にしたがって構文解析をし、[構文木](https://ja.wikipedia.org/wiki/構文木 "wikilink")を出力する[構文解析器](../Page/構文解析器.md "wikilink")（パーサ、パーザ）(1.2)である。 (1.1)のレキシカルアナライザを生成するのが、レキシカルアナライザジェネレータである。

### 機能概要

[構文解析器](../Page/構文解析器.md "wikilink")(1.2)に解析を数字や英字や空白などの1文字単位で行わせると、複雜になりすぎる。しかし、人間が英文から英単語や数字などの記号列を、区切り文字（たとえば空白、タブ、改行、コンマ、終止符、カッコ）やその列を目印に抽出して、意味を判断しているのと、同様の発想ができる。すなわち、区切り記号列でソースを切っていくと、「print」のような語、「1999」のような10進数、「"Hello, world"」といった文字リテラル、「++」といった演算子、「}」や「;」など意味のある区切り文字など、各種の文字列が取り出せる。これを[トークン](../Page/トークン.md "wikilink")という。ここまでの下位の文法処理を上記[字句解析器](https://ja.wikipedia.org/wiki/字句解析器 "wikilink")(1.1)に行わせ、一方、[構文解析器](../Page/構文解析器.md "wikilink")(1.2)はトークンから出発して句、文、ブロック、プログラムなどを認識する上位の文法処理に専念させる。この分業化により、それぞれの定義と処理を簡潔にできる。

この[字句解析器](https://ja.wikipedia.org/wiki/字句解析器 "wikilink")(1.1)の合理的な開発を目的とし、機械可読にした規則定義を与えれば[字句解析器](https://ja.wikipedia.org/wiki/字句解析器 "wikilink")を自動生成してくれる便利なツールがレキシカルアナライザジェネレータであり、LexやFlexなどがそれに属する。

`〔規則定義〕`
`　　↓`
`レキシカルアナライザジェネレータ（Lex, Flexなど）`
`　　↓`
`〔字句解析器(1.1)〕`

同様に、[構文解析器](../Page/構文解析器.md "wikilink")(1.2)の合理的な開発を目的とし、構文規則定義を与えれば[構文解析器](../Page/構文解析器.md "wikilink")を自動生成してくれる便利なツールとして、[Yacc](../Page/Yacc.md "wikilink")(Yet Another Compiler Compiler)などのパーサジェネレータ（コンパイラコンパイラ）がある。

### 構文解析器ジェネレータとの関係

Yaccなどの[構文解析器](../Page/構文解析器.md "wikilink")生成ツールを利用するなら、Lexに字句文法定義を与えて生成させたC言語ソースである[字句解析器](https://ja.wikipedia.org/wiki/字句解析器 "wikilink")が（Yaccがトークンをユーザから得るための）yylex関数を含んでいるので、CコンパイラでYacc出力と一緒にこれをリンクして組み込む。これにより、ソーステキストの字句解析と構文解析を両方行って、規則のアクション部（あるいはさらにそれに呼ばれるユーザ作成のC言語関数）に書かれた計算の結果や、コンパイルの生成に使われる抽象構文木の構造体データ、あるいは各種表示が出力される変換プログラムが完成する。

YaccとLexはよく似た文法定義をもち、セットで使われ、セットで解説されることが多い。LexとYaccの機能は[IEEE](../Page/IEEE.md "wikilink") [POSIX](../Page/POSIX.md "wikilink") 1003.1-2008（かつては1003.2）で標準化されている\[2\]。

### 配布と派生

Yaccはほとんどの[UNIX](../Page/UNIX.md "wikilink")システムで、デフォルトのレキスカルアナライザジェネレータとして利用可能だった。 Lexは多くのシステム、多くのプログラミング言語に移植されている。たとえばJava言語による字句解析器を生成するLex系ツールに、[JLex](http://www.cs.princeton.edu/~appel/modern/java/JLex/)、それを書き直した[JFlex](http://jflex.de/jflex_manual_j.html)がある。このJFlexとJava言語用構文解析器[CUP](http://www.cs.princeton.edu/~appel/modern/java/CUP/manual.html)と組みあわせて用いることも行われている\[3\]。

## Lex のファイル構造

Lexのファイル構造は意識的にyaccのそれに似せて定義されている。 ファイルは3つの部分に分割されており、それぞれ定義領域、規則領域、[Cコード領域である](../Page/C言語.md "wikilink")。各領域はパーセント記号2つ(%%)のみを含んだ行で区切られる。

定義領域は[正規表現](../Page/正規表現.md "wikilink")を用いてマクロを定義するところであり、かつCの[ヘッダーファイル](https://ja.wikipedia.org/wiki/ヘッダーファイル "wikilink")を取り込む場所でもある。

規則領域は最も重要な領域でありCの命令との関連付けを行う。Lexの規則と一致するパターンがあるとそれに関連付けされたCコードを実行する。

Cコード領域には生成したソースにそのままコピーされるCの命令や関数が含まれている。 これらの命令は規則領域での規則により呼ばれたコードを含む場合もある。大規模なプログラムではここに分割しておき[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")時にリンクするほうが便利である。

## Lexの正規表現

  - 通常の[正規表現](../Page/正規表現.md "wikilink")の特殊文字にくわえ、「`"`」 「`/`」 「`%`」 「`(`」 「`)`」 「`+`」 「`/`」 「`<`」 「`>`」 「`?`」 「`{`」 「`|`」 「`}`」 も特殊文字である
  - 行頭の「`%`」は、上述のように領域を区切ったり、Lex特有の指示をあたえるために使う
  - 文字クラス、否定文字クラスの内側で「`\`」が特殊文字になる
  - 陽に指定したときを除いて、否定文字クラスは、改行にも照合する
  - 「`"`」で引用できる。引用の終了も「`"`」
  - 「`パターン{`最少`,`最多`}`」や「`パターン{`回数`}`」でパターンの繰返し回数を指定できる ([Grep](../Page/Grep.md "wikilink")の拡張正規表現と同じ)
  - 「`+`」は「`{1,}`」の、「`?`」は「`{,1}`」の、それぞれの省略形である (Grepの拡張正規表現と同じ)
  - 「`|`」で択一できる。「`(`」と「`)`」で範囲を広げて指定できる (Grepの拡張正規表現と同じ)
  - 「`\b`」「`\f`」「`\n`」「`\r`」「`\t`」「`\v`」「`\`8進数」は、[Cの文字定数の定義と同じ](../Page/C言語.md "wikilink")
  - 「</tt>\<</tt>開始条件`>`正規表現」で、指定の名前の開始条件にあるときの正規表現だけに照合できる。開始条件は、コンマで区切って複数指定できる
  - 「r`/`s」は、正規表現「s」の後続する正規表現「r」を表わす。アクションで参照できるのが「r」のみになるところが、重要である
  - 「`{`名前`}`」で、定義領域で定義した名前のマクロに展開される

## Flex用のサンプルファイル

次の例はFlex版の入力ファイルのサンプルである。これは入力中の整数値を認識する。 "`abc123z.!&*24ghj6`"という入力があると次のような表示を行う。

`Saw an integer: 123`
`Saw an integer: 24`
`Saw an integer: 6`

`/* `
` * flex用字句解析　例`
` *`
` * 数値（整数値）を入力を取り出す.`
` */`

`/*** Definition section ***/`

`%{`

`/*`
` * C コードにはCの標準I/O ライブラリを使うものがある.`
` * %{と %} で囲まれた部分はそのまま生成ファイルに`
` * 取り込まれる.`
` */`
`#include <stdio.h>`

`%}`

`/* マクロ;  正規表現 */`
`DIGIT       [0-9]`
`INTEGER     {DIGIT}+`

`/* これはflexに入力ファイルが一つであることを示す. */`
`%option noyywrap`

`%%`
`    /*`
`     * 規則領域`
`     *`
`     * コメントはインデントしなければならない.`
`     * そうしないと正規表現と誤認識してしまう.`
`     */`

`{INTEGER}   {`
`                /*`
`                 * この規則は入力から整数を表示する.`
`                 * yytextには一致した文字列が含まれる.`
`                 */`
`                printf("Saw an integer: %s\n", yytext); `
`            }`

`.           { /* それ以外の文字は無視. */ }`

`%%`
`/*** Cコード領域 ***/`

`/*`
` * メインプログラム.`
` *`
` * 字句解析を呼び出し、処理が済むと終了する. `
` */`
`int main(void)`
`{`
`    /* yyin はlexが読むファイルでここでは標準入力になっている. */`
`    FILE *yyin = stdin;`

`    /* 字句解析の呼び出し. */`

`    yylex();`
`    return 0;`
`}`

## 脚注・出典

<references/>

## 関連項目

  - [字句解析器](https://ja.wikipedia.org/wiki/字句解析器 "wikilink")
  - [Yacc](../Page/Yacc.md "wikilink")

## 外部リンク

  - [字句解析](http://docs.oracle.com/cd/E19620-01/805-5827/6j5gframh/index.html) （日本語）- Oracle Documentation プログラミングユーティリティ 第2章、

特に[lex と yacc の併用](http://docs.oracle.com/cd/E19620-01/805-5827/6j5gframh/index.html#6j5gframo)

  - [Lex Online Manual](http://dinosaur.compilertools.net/lex/index.html) - 作者 M. E. Lesk and E. Schmidt （英語）
  - [Lex & Yacc Tutorial](http://epaperpress.com/lexandyacc/) - Tom Niemann epaperpress.com（英語）
  - [Cコンパイラ設計(yacc・lexの応用)](http://ns.pwv.co.jp/take_public_html/SampleC/SampleC.html)G・フリードマン著、矢吹道郎ら訳、竹本 浩OCR復刻
  - [字句スキャナ生成プログラム Flex 2.3.7、1.03版 1993年2月](http://www.asahi-net.or.jp/~wg5k-ickw/html/online/flex-2.5.4/flex_toc.html)（日本語訳）- 原著 G. T. Nicol、

特に[Flex と Lex](http://www.asahi-net.or.jp/~wg5k-ickw/html/online/flex-2.5.4/flex_10.html#SEC59)

  - [JLex: A Lexical Analyzer Generator for Java](http://www.cs.princeton.edu/~appel/modern/java/JLex/)
  - [JFlex](http://jflex.de/jflex_manual_j.html)

[Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:構文解析_(プログラミング)](https://ja.wikipedia.org/wiki/Category:構文解析_\(プログラミング\) "wikilink") [Category:字句解析](https://ja.wikipedia.org/wiki/Category:字句解析 "wikilink")

1.  [Flex The Lexical Scanner Generator](http://ipr20.cs.ehime-u.ac.jp/member/kinoshita/exp3/document/flex/flex.html#SEC3) - G. T. Nicol（日本語訳）
2.  [POSIX 1003.1-2008](http://standards.ieee.org/findstds/standard/1003.1-2008.html) - IEEE（有料）
3.  [Theory of Compilation -- JLex, CUP tools --](http://cs.haifa.ac.il/courses/compilers/BILAL/Tutorials/JLex_CUP_tools.pdf)(PDF) - by Haifa Univ. Bilal Saleh