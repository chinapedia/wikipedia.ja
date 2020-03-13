> この記事は[While](https://ja.wikipedia.org/wiki/While)から翻訳されています。


**while文** () は[プログラミング言語](../Page/プログラミング言語.md "wikilink")において繰り返し（[ループ](../Page/ループ_\(プログラミング\).md "wikilink")）の[制御構造](../Page/制御構造.md "wikilink")を記述するための[文](https://ja.wikipedia.org/wiki/文_\(プログラミング\) "wikilink") (statement) である。英語の接続詞  の意味「〜である間」の通り、継続条件として指定された[式](../Page/式_\(プログラミング\).md "wikilink")（制御式）を評価した値が真である間、ループ本体 (loop body) \[1\]の処理を繰り返し実行する。

while文では通例、ループの最初に継続条件式を評価する。したがって、継続条件式が偽であった場合はループ本体の処理は一度も実行されない。プログラミング言語によっては、ループの本体を一度実行した後、継続条件式を評価する[do-while文](https://ja.wikipedia.org/wiki/do-while文 "wikilink")をサポートするものもある。do-while文では継続条件式の真偽にかかわらず、ループ本体の処理が必ず一度は実行される。詳細は当該記事も参照のこと。

なお、[関数型言語](../Page/関数型言語.md "wikilink")では通例、whileループは文ではなく式 (expression) として定義される。while式はwhile文よりもプログラム中で記述できる位置に関して柔軟性がある。[Haskell](../Page/Haskell.md "wikilink")のような純粋関数型言語では、ループは常に[再帰](../Page/再帰.md "wikilink")（[末尾再帰](../Page/末尾再帰.md "wikilink")）を使って記述するため、whileループの構文をサポートしないものもある。

## 例

### Cおよびそれに類する言語

[C言語](../Page/C言語.md "wikilink"), [C++](../Page/C++.md "wikilink"), [C\#](../Page/C_Sharp.md "wikilink"), [D](../Page/D言語.md "wikilink"), [Java](https://ja.wikipedia.org/wiki/Java "wikilink"), [Perl](../Page/Perl.md "wikilink")などでは以下のような構文である。

``` c
while (条件)
    文 // ここの部分を「ループ本体」と呼ぶ
```

このループの実行は、次のような手順となる。

1.  「条件」を評価する。「条件」が[偽](https://ja.wikipedia.org/wiki/偽 "wikilink")ならば、ループを終了する。
2.  「文」を実行する。
3.  「条件」の評価に戻る。

「条件」がはじめから偽の場合は、「文」は一度も実行されない。

ループ本体が複数の文からなる場合、[ブロック](../Page/ブロック_\(プログラミング\).md "wikilink")（複文）を使う。

``` c
while (条件) {
    ...
}
```

#### プログラム例

``` c
int x = 0;
while (x < 100) {
    printf("x は %d です。\n", x);
    ++x; // x の値を 1 だけ増やす（インクリメントする）。
}
```

これを実行すると、次のように[標準出力](https://ja.wikipedia.org/wiki/標準出力 "wikilink")に出力する。

`x は 0 です。`
`x は 1 です。`

`…………`
` `
`x は 98 です。`
`x は 99 です。`

[変数](../Page/変数_\(プログラミング\).md "wikilink")`x`の初期値は0であり、ループ本体の処理を1回実行するたびにインクリメントされる。`x`の値が100未満すなわち99のときまではループ本体の処理が実行され、最終的に`x`の値が100になる。その後、継続条件式を評価するとき、条件は成り立たなくなり、ループは終了する。

#### ループの脱出と継続

ループの脱出と継続の制御に利用できる分岐文を備える言語もある。[break文](https://ja.wikipedia.org/wiki/break文 "wikilink")は、ループ本体の複文の途中からであっても、またwhileの条件が成り立っていても、ループ中から抜け出す。[continue文](https://ja.wikipedia.org/wiki/continue文 "wikilink")はループの途中から、**ループ本体の最後**に飛び\[2\]、while文の場合にはそこから先頭に戻って条件の評価となる。

[goto文](https://ja.wikipedia.org/wiki/goto文 "wikilink")を使える言語では、whileループの脱出にgoto文を使うこともできる。通常はbreak文のほうが好ましいが、多重ループを脱出する場合や[switch文](https://ja.wikipedia.org/wiki/switch文 "wikilink")をループ本体に含む場合などでは、goto文のほうが簡潔に記述できる。[return文](https://ja.wikipedia.org/wiki/return文 "wikilink")や例外のスローによってループを脱出することのできる言語もある。

### Pascal

[Pascal](../Page/Pascal.md "wikilink")におけるwhile文は、C言語系列と概ね同様であり、キーワードとして **while** と **do** を使う。一方、do-while文に関しては、repeat-until文が相当するが、キーワードとして **repeat** と **until** を使う点が異なるだけでなく、制御式として継続条件ではなく終了条件（真のときループを終了）を記述する点も異なる。

#### 構文

``` pascal
while 条件 do 文
```

``` pascal
repeat 文; 文...; 文 until 条件
```

LL(1)の単純な構文というPascalのポリシーから、両者で全く違う[キーワードを使う設計](../Page/予約語.md "wikilink")（デザイン）となっている。

whileでは複数の文を置く場合には begin-end で複文にしなければならないが、repeat-until はそれ自身が暗黙のブロック構文になっているので、セミコロンで区切って複数の文を置くことができる。

### Basic

Full BASIC（INCITS/ISO/IEC 10279-1991 (R2005) "Information Technology – Programming Languages – Full BASIC"）には、ループの多くのパターンに対応する柔軟性のあるDo-Loop文がある。また[Visual Basicには](../Page/Visual_Basic.md "wikilink")、それに加えて伝統的な[BASIC](../Page/BASIC.md "wikilink")のWHILEに近いWhile文もある。

#### 構文

[Visual Basic .NETにおけるWhile文は以下のような構文である](../Page/Visual_Basic_.NET.md "wikilink")\[3\]。[Visual Basicでは](../Page/Visual_Basic.md "wikilink") While...Wend だが、VB.NETでは While...End While となっている。

``` vbnet
While 条件
    文...
    [ (Continue|Exit) While ]
    文...
End While
```

Exit While は[break文](https://ja.wikipedia.org/wiki/break文 "wikilink")、Continue While は[continue文](https://ja.wikipedia.org/wiki/continue文 "wikilink")に相当する機能を持つ。

Do...Loop文は以下のような構文である\[4\]。

``` vbnet
Do [(While|Until) 条件]
    文...
    [ (Continue|Exit) Do ]
    文...
Loop [(While|Until) 条件]
```

Do の後に While を続ければ、while文に相当し、Loop の後に Until を続ければ、Pascalの repeat-until に相当する。どちらにも条件を付けなければ、単純な[無限ループ](../Page/無限ループ.md "wikilink")になる。

## 注

<references/>

## 関連項目

  - [if文](https://ja.wikipedia.org/wiki/if文 "wikilink")
  - [for文](https://ja.wikipedia.org/wiki/for文 "wikilink")
  - [do-while文](https://ja.wikipedia.org/wiki/do-while文 "wikilink")
  - [goto文](https://ja.wikipedia.org/wiki/goto文 "wikilink")
  - [制御構造](../Page/制御構造.md "wikilink")
  - [無限ループ](../Page/無限ループ.md "wikilink")

[Category:制御構造](https://ja.wikipedia.org/wiki/Category:制御構造 "wikilink") [Category:C言語](https://ja.wikipedia.org/wiki/Category:C言語 "wikilink") [Category:Pascal](https://ja.wikipedia.org/wiki/Category:Pascal "wikilink")

1.  JIS X 3010:2003「プログラム言語C」§6.8.5「繰返し文」
2.  JIS X 3010:2003「プログラム言語C」§6.8.6.2「continue文」
3.  [While...End While Statement (Visual Basic) | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/visual-basic/language-reference/statements/while-end-while-statement)
4.  [Do...Loop Statement (Visual Basic) | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/visual-basic/language-reference/statements/do-loop-statement)