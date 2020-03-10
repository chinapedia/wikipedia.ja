> この記事は[EBNF](https://ja.wikipedia.org/wiki/EBNF)から翻訳されています。


**EBNF**（**Extended Backus–Naur Form**）とは、[文脈自由文法](../Page/文脈自由文法.md "wikilink")を表現する[メタ文法記法であり](https://ja.wikipedia.org/wiki/メタ言語 "wikilink")、コンピュータの[プログラミング言語](../Page/プログラミング言語.md "wikilink")や[形式言語](../Page/形式言語.md "wikilink")の形式的表現として使われる。[バッカス・ナウア記法](../Page/バッカス・ナウア記法.md "wikilink") (BNF) の拡張であり、**拡張バッカス・ナウア記法**とも呼ばれるが、[ABNF](https://ja.wikipedia.org/wiki/ABNF "wikilink")（Augmented Backus-Naur Form）も同じ訳語となるため、区別するためあえて **EBNF** としている。

[ニクラウス・ヴィルト](https://ja.wikipedia.org/wiki/ニクラウス・ヴィルト "wikilink")が最初に開発した。EBNF の標準化されたものとして ISO-14977 などがある。

## 基本

[プログラムの](../Page/プログラム_\(コンピュータ\).md "wikilink")[ソースコード](../Page/ソースコード.md "wikilink")は、[終端記号で構成される](../Page/終端記号と非終端記号.md "wikilink")。終端記号は、具体的な文字や数字や記号で構成される。

EBNF は、[非終端記号に対応する記号列を指示する](../Page/終端記号と非終端記号.md "wikilink")[生成規則](https://ja.wikipedia.org/wiki/生成規則 "wikilink")によって定義される。

``` ebnf
 digit excluding zero = "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9" ;
 digit                = "0" | digit excluding zero ;
```

この生成規則では、非終端記号 "digit" が左辺に定義されている。[バーティカルバー](https://ja.wikipedia.org/wiki/バーティカルバー "wikilink")は、その前後にある終端記号や非終端記号のいずれかが選択されることを示す。また、終端記号は、終端文字を[引用符](https://ja.wikipedia.org/wiki/引用符 "wikilink")で囲んである。従って、"digit" は *0* または *digit excluding zero* のどちらかであり、後者は *1* か *2*、あるいは *9* までのいずれかになる。

生成規則は、終端記号や非終端記号の並びを含むこともでき、それらは[コンマ](https://ja.wikipedia.org/wiki/コンマ "wikilink")で区切られる。

``` ebnf
 twelve                          = "1" , "2" ;
 two hundred one                 = "2" , "0" , "1" ;
 three hundred twelve            = "3" , twelve ;
 twelve thousand two hundred one = twelve , two hundred one ;
```

省略可能かつ繰り返し可能な部分は、中括弧 { … } で表される。

``` ebnf
 natural number = digit excluding zero , { digit } ;
```

この場合、 *1* も *2* も *10* も *12345* も natural number（自然数）として正しい文字列となる。つまり、中括弧で囲まれた部分はゼロ回以上の任意の回数繰り返すことができる。

省略可能な部分は大括弧 \[ … \] で表される。

``` ebnf
 integer = "0" | [ "-" ] , natural number ;
```

この場合、integer（整数）はゼロ (*0*) か、natural number であり、natural number にはオプションでマイナス符号を前置することができる。

EBNF はこれらの他に、繰り返し回数を指定したり、一部生成規則の適用を除外したり、コメントを挿入したりといったことができる。

## ISO による拡張

ISO 14977 で標準化された EBNF では、拡張を可能とする2つのファシリティが述べられている。第一は EBNF 文法の一部として、疑問符で挟まれた任意のテキストを EBNF 標準の解釈範囲外とするものである。例えば、空白文字は以下のような規則で定義できる。

``` ebnf
 space = ? US-ASCII character 32 ?;
```

第二は、EBNF では括弧を識別子（終端記号や非終端記号）に続けて配置することができないという事実を利用する。次の表現は EBNF としては正しくない。

``` ebnf
 something = foo ( bar );
```

そこで、このような記法を EBNF の拡張として利用する。例えば、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")の文法における function application は次の規則で定義される。

`function application = list( symbol , [ { expression } ] );`

## BNF を拡張する理由

BNF では、オプションや繰り返しを直接的に表現できないという問題があった。そのため、中間的な規則を定義したり、空（何も生成しない）とオプションの選択型の生成規則を定義したり、再帰的な規則で繰り返しを表したりしていた。同様の記法は EBNF でも利用可能である。

オプションは EBNF では次のように表される。

``` ebnf
 signed number = [ sign ] , number ;
```

これを BNF スタイルで次のように表すこともできる。

``` ebnf
 signed number = sign , number | number ;
```

または

``` ebnf
 signed number = optional sign , number ;
 optional sign = ε | sign ; (* ε は何も生成しないことをより明確に示すのに使われる *)
```

繰り返しは EBNF では次のように表される。

``` ebnf
 number = { digit } ;
```

これを BNF スタイルで次のように表すこともできる。

``` ebnf
 number = digit | number , digit;
```

## その他の追加・修正

EBNF は次のような BNF の欠陥を排除している。

  - BNF は記号として (\<, \>, |, ::=) を使っている。定義対象の言語にもこれらの記号が使われている場合、BNF はそれを何かに置き換えて表現する必要があった。
  - BNF では1つの規則を一行で表す必要があった。

EBNF はこれらの問題を次のように解決している。

  - [終端記号は必ず引用符](../Page/終端記号と非終端記号.md "wikilink")（"…" または '…'）で囲まれる。[非終端記号を囲んでいた山括弧](../Page/終端記号と非終端記号.md "wikilink")（"\<…\>"）は省略されている。
  - 規則の最後にセミコロンなどの記号を付与して、規則の範囲を明確化している。

他にも様々な拡張がされているが、定義できる言語の範囲という意味では BNF に比べて「強力」というわけではない。実際、EBNF で定義可能な[文法](../Page/文法.md "wikilink")は、基本的に BNF でも表現できる。ただし、その場合 BNF での表現は非常に大きくなってしまう。

EBNF は[ISOが](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink") *ISO/IEC 14977:1996(E)* として標準化した。

BNF に何らかの拡張をしたものを EBNF と呼ぶこともある。例えば、[W3C](../Page/World_Wide_Web_Consortium.md "wikilink") は [XML](../Page/Extensible_Markup_Language.md "wikilink") の文法記述に [*独自の* EBNF](http://www.w3c.org/TR/REC-xml#sec-notation) を使っている。

## 別の例

代入文しかない単純なプログラミング言語を EBNF で定義した例を以下に示す。

``` ebnf
 (* a simple program in EBNF − Wikipedia *)
 program = 'PROGRAM' , white space , identifier , white space ,
            'BEGIN' , white space ,
            { assignment , ";" , white space } ,
            'END.' ;
 identifier = alphabetic character , [ { alphabetic character | digit } ] ;
 number = [ "-" ] , digit , [ { digit } ] ;
 string = '"' , { all characters - '"' } , '"' ;
 assignment = identifier , ":=" , ( number | identifier | string ) ;
 alphabetic character = "A" | "B" | "C" | "D" | "E" | "F" | "G"
                      | "H" | "I" | "J" | "K" | "L" | "M" | "N"
                      | "O" | "P" | "Q" | "R" | "S" | "T" | "U"
                      | "V" | "W" | "X" | "Y" | "Z" ;
 digit = "0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9" ;
 white space = ? white space characters ? ;
 all characters = ? all visible characters ? ;
```

この場合、文法的に正しいプログラムは次のようになる。

``` text
 PROGRAM DEMO1
 BEGIN
   A0:=3;
   B:=45;
   H:=-100023;
   C:=A;
   D123:=B34A;
   BABOON:=GIRAFFE;
   TEXT:="Hello world!";
 END.
```

この言語は容易に[制御構造](https://ja.wikipedia.org/wiki/制御構造 "wikilink")や数式や入出力命令を持つように拡張できる。そうすると、小型の実用可能なプログラミング言語の仕様が完成する。

標準的な表記で使うよう提案されている文字を以下の表に示す。

| 用途    | 表記          |
| ----- | ----------- |
| 定義    | \=          |
| 連結    | ,           |
| 終端    | ;           |
| 区切り   | |           |
| オプション | \[ ... \]   |
| 繰り返し  | { ... }     |
| グループ化 | ( ... )     |
| 二重引用符 | " ... "     |
| 一重引用符 | ' ... '     |
| コメント  | (\* ... \*) |
| 特殊文字列 | ? ... ?     |
| 例外    | \-          |

## 慣例

1\. 以下のような慣例が使われている。

  - EBNF におけるそれぞれのメタ識別子（非終端記号）は、単語を[ハイフン](../Page/ハイフン.md "wikilink")で連結した形式で記述される。
  - メタ識別子の名前が“-symbol”で終わっている場合、それは EBNF の終端記号に名前を付けたものと解釈できる。

2\. EBNF で特別な意味を持つ文字とその優先順位は次の通り（上の方が優先順位が高い）。

`* repetition-symbol`
`- except-symbol`
`, concatenate-symbol`
`| definition-separator-symbol`
`= defining-symbol`
`; terminator-symbol`

3\. 通常の優先順位は以下の括弧のペアで変更される。

`´  first-quote-symbol            first-quote-symbol  ´`
`"  second-quote-symbol          second-quote-symbol  "`
`(* start-comment-symbol          end-comment-symbol *)`
`(  start-group-symbol              end-group-symbol  )`
`[  start-option-symbol            end-option-symbol  ]`
`{  start-repeat-symbol            end-repeat-symbol  }`
`?  special-sequence-symbol   special-sequence-symbol ?`

以下の例は、様々な繰り返しの記法を示したものである。

`aa = "A";`
`bb = 3 * aa, "B";`
`cc = 3 * [aa], "C";`
`dd = {aa}, "D";`
`ee = aa, {aa}, "E";`
`ff = 3 * aa, 3 * [aa], "F";`
`gg = {3 * aa}, "D";`

この規則群から生成される終端文字列は以下のようになる。

`aa: A`
`bb: AAAB`
`cc: C AC AAC AAAC`
`dd: D AD AAD AAAD AAAAD etc.`
`ee: AE AAE AAAE AAAAE AAAAAE etc.`
`ff: AAAF AAAAF AAAAAF AAAAAAF`
`gg: D AAAD AAAAAAD etc.`

## 関連仕様

  - [W3Cは](../Page/World_Wide_Web_Consortium.md "wikilink") [異なる EBNF](http://www.w3c.org/TR/REC-xml#sec-notation) を使って[XMLの文法を示している](../Page/Extensible_Markup_Language.md "wikilink")。
  - 英国規格協会は[1981年](../Page/1981年.md "wikilink")に EBNF の標準として BS 6154 を発表した。
  - [IETFは](../Page/Internet_Engineering_Task_Force.md "wikilink") RFC 5234 で定義された [ABNF](https://ja.wikipedia.org/wiki/ABNF "wikilink") (Augmented BNF) を使っている。

## 関連項目

  - [ABNF](https://ja.wikipedia.org/wiki/ABNF "wikilink")
  - [バッカス・ナウア記法](../Page/バッカス・ナウア記法.md "wikilink")
  - [正規表現](../Page/正規表現.md "wikilink")

## 参考文献

  - Niklaus Wirth: [What can we do about the unnecessary diversity of notation for syntactic definitions?](http://doi.acm.org/10.1145/359863.359883) CACM, Vol. 20, Issue 11, November 1977, pp. 822-823.
  - Roger S. Scowen: Extended BNF — A generic base standard. Software Engineering Standards Symposium 1993.
  - EBNF を定義した[国際標準](https://ja.wikipedia.org/wiki/国際標準 "wikilink") ([ISO 14977](http://www.iso.org/iso/en/CatalogueDetailPage.CatalogueDetail?CSNUMBER=26153)) は [zip化されたpdfファイル](http://standards.iso.org/ittf/PubliclyAvailableStandards/s026153_ISO_IEC_14977_1996\(E\).zip) として無料で入手可能である。

## 外部リンク

  - Article "[EBNF: A Notation to Describe Syntax (PDF)](http://www.cs.cmu.edu/~pattis/misc/ebnf.pdf)" by Richard E. Pattis
  - Article "[BNF and EBNF: What are they and how do they work?](http://www.garshol.priv.no/download/text/bnf.html)" by Lars Marius Garshol
  - Article "[The Naming of Parts](http://xml.com/pub/a/2001/07/25/namingparts.html)" by John E. Simpson
  - [ISO/IEC 14977 : 1996(E)](http://www.cl.cam.ac.uk/~mgk25/iso-14977.pdf)
  - RFC 4234 - Augmented BNF for Syntax Specifications: ABNF
  - [BNF/EBNF variants](http://www.cs.man.ac.uk/~pjj/bnf/ebnf.html) - by Pete Jinks
  - [Create syntax diagrams from EBNF](http://dotnet.jku.at/applications/Visualizer)

[Category:形式言語](https://ja.wikipedia.org/wiki/Category:形式言語 "wikilink") [Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink")