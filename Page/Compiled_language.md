> この記事は[Compiled language](https://ja.wikipedia.org/wiki/Compiled_language)から翻訳されています。


**コンパイル型言語**とは、その実装の主体が[コンパイラ](../Page/コンパイラ.md "wikilink") （ [ソースコード](../Page/ソースコード.md "wikilink")から[マシンコードを生成する](../Page/機械語.md "wikilink")[トランスレータ](../Page/ソースコード.md "wikilink") ）であり、 [インタプリタ](../Page/インタプリタ.md "wikilink") （ソースコードをステップバイステップで実行し、ランタイム前の翻訳が行われない）ではない[プログラミング言語](../Page/プログラミング言語.md "wikilink")です。

この用語はやや曖昧です。 原則として、どの言語もコンパイラやインタプリタで実装できます。 \[1\] 両方のソリューションの組み合わせも一般的です。コンパイラはソースコードを何らかの中間形式（しばしば[p-codeまたは](https://ja.wikipedia.org/wiki/P-Code "wikilink")[バイトコード](../Page/バイトコード.md "wikilink")と呼ばれる）に変換し、それを実行するインタプリタに渡します。

## メリットとデメリット

コンパイル時にネイティブコードにコンパイルされるプログラムは、実行時に翻訳されるプログラムよりも高速になる傾向があります。翻訳プロセスのオーバーヘッドがあるからです。しかし、JIT([実行時コンパイラ](../Page/実行時コンパイラ.md "wikilink"))のような新しい技術、および翻訳プロセスの全般的な改善により、この差は小さくなり始めています。 [バイトコード](../Page/バイトコード.md "wikilink")を使用した混合ソリューションは、中程度の効率になる傾向があります。

[低水準プログラミング言語は](../Page/低水準言語.md "wikilink")、一般的にコンパイルされます。特に、 [クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")のサポートより効率を重視する場合です。 このような言語の場合、プログラムコードと[マシンコードによって実行されるハードウェア操作の間には](../Page/機械語.md "wikilink")1対1の対応があり、プログラマが[中央処理装置](../Page/CPU.md "wikilink") （CPU）と[メモリの使用を細かく詳細に制御しやすくなります](../Page/主記憶装置.md "wikilink")。

少し努力すれば、従来の[インタプリタ型言語でも](https://ja.wikipedia.org/wiki/インタプリタ言語 "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")を作成することが常に可能です 。 たとえば、 [Common lispは](../Page/Common_Lisp.md "wikilink")、Javaバイトコード（ [Java仮想マシン](../Page/Java仮想マシン.md "wikilink")によって解釈される）、Cコード（次にネイティブマシンコードにコンパイルされる）、または直接ネイティブコードにコンパイルできます。 複数のコンパイルターゲットをサポートするプログラミング言語は、実行速度またはクロスプラットフォームの互換性のいずれかを選択するために、開発者により多くの制御を提供します。

一般的にコンパイルされると考えられているいくつかの言語：

  - [Ada](../Page/Ada.md "wikilink")
  - [ALGOL](../Page/ALGOL.md "wikilink")
      - ALGOL 60
      - ALGOL 68
      - SMALL
  - [ベーシック](../Page/BASIC.md "wikilink")
      - PowerBasic
      - [Visual Basic](../Page/Visual_Basic.md "wikilink") （バイトコードへ）
      - [PureBasic](../Page/PureBasic.md "wikilink")
  - [C](../Page/C言語.md "wikilink")
  - [C ++](../Page/C++.md "wikilink")
  - [C＃](../Page/C_Sharp.md "wikilink") （バイトコードへ）
  - クレオ
  - [COBOL](../Page/COBOL.md "wikilink")
  - コブラ
  - [結晶](https://ja.wikipedia.org/wiki/Crystal_\(プログラミング言語\) "wikilink")
  - [D](../Page/D言語.md "wikilink")
  - eC
  - [エッフェル](../Page/Eiffel.md "wikilink")
      - [サザー](https://ja.wikipedia.org/wiki/Sather "wikilink")
      - Ubercode
  - [Erlang](../Page/Erlang.md "wikilink") （バイトコードへ）
  - [F＃](../Page/F_Sharp.md "wikilink") （バイトコードへ）
  - Factor （後のバージョン）
  - [前方へ](../Page/Forth.md "wikilink")
  - [Fortran](../Page/FORTRAN.md "wikilink")
  - [Go](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink")
  - [Haskell](../Page/Haskell.md "wikilink")
  - [Haxe](https://ja.wikipedia.org/wiki/Haxe "wikilink") （バイトコードまたはC ++へ）
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink") （バイトコードへ）
      - [Scala](../Page/Scala.md "wikilink")
      - [Kotlin](https://ja.wikipedia.org/wiki/Kotlin "wikilink")
  - [JavaScript](../Page/JavaScript.md "wikilink") （バイトコードJITへ）
  - JOVIAL
  - [Julia](https://ja.wikipedia.org/wiki/Julia_\(プログラミング言語\) "wikilink")
  - [LabVIEW](../Page/LabVIEW.md "wikilink") 、G
  - [Lisp](https://ja.wikipedia.org/wiki/LISP "wikilink")
      - [Common Lisp](../Page/Common_Lisp.md "wikilink")
  - Lush
  - Mercury
  - [ML](../Page/ML_\(プログラミング言語\).md "wikilink")
      - [Standard ML](https://ja.wikipedia.org/wiki/Standard_ML "wikilink")
          - Alice
      - [OCaml](../Page/OCaml.md "wikilink")
  - [Nim](https://ja.wikipedia.org/wiki/Nim "wikilink") （C、C ++、またはObjective-C）
  - Open-URQ
  - [Pascal](../Page/Pascal.md "wikilink")
      - [Object Pascal](../Page/Object_Pascal.md "wikilink")
          - [Delphi](../Page/Delphi.md "wikilink")
          - [Free Pascal](../Page/Free_Pascal.md "wikilink") / [Lazarus](../Page/Lazarus.md "wikilink")
      - [Modula-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink")
      - [Modula-3](https://ja.wikipedia.org/wiki/Modula-3 "wikilink")
      - [Oberon](../Page/Oberon.md "wikilink")
  - [Objective-C](../Page/Objective-C.md "wikilink")
  - [PL / I](https://ja.wikipedia.org/wiki/PL/I "wikilink")
  - [RPG](../Page/RPG_\(プログラム言語\).md "wikilink")
  - [Rust](https://ja.wikipedia.org/wiki/Rust_\(プログラミング言語\) "wikilink")
  - Seed7
  - SPITBOL
  - [Swift](https://ja.wikipedia.org/wiki/Swift_\(プログラミング言語\) "wikilink")
  - [Visual Foxpro](https://ja.wikipedia.org/wiki/Microsoft_Visual_FoxPro "wikilink")
  - Visual Prolog
  - V（プログラミング言語）
  - W
  - Zig

<!-- end list -->

  - [ANTLR](../Page/ANTLR.md "wikilink")
  - CodeWorker
  - [Lex](../Page/Lex.md "wikilink")
  - Flex
  - [GNU bison](../Page/Bison.md "wikilink")
  - [Yacc](../Page/Yacc.md "wikilink")

<!-- end list -->

  - [コンパイラ](../Page/コンパイラ.md "wikilink")
  - コンパイル型言語の一覧
  - [インタプリタ](../Page/インタプリタ.md "wikilink")（コンピューティング）
  - インタプリタ型言語

<references />

  -
<!-- end list -->

1.