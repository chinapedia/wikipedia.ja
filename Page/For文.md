> この記事は[For](https://ja.wikipedia.org/wiki/For)から翻訳されています。


**for文**（フォーぶん）は[プログラミング言語](../Page/プログラミング言語.md "wikilink")において[条件](../Page/条件.md "wikilink")が[真](https://ja.wikipedia.org/wiki/真 "wikilink")の間だけ与えられた[文の実行を繰り返すという](https://ja.wikipedia.org/wiki/文_\(プログラミング\) "wikilink")[ループを記述するための文である](../Page/ループ_\(プログラミング\).md "wikilink")。forループは、[whileループと違って](../Page/While文.md "wikilink")、ループに入る前の初期化（通常カウンタ変数の初期化を行なう）を含む点で異なる。

また言語によっては[foreach文](https://ja.wikipedia.org/wiki/foreach文 "wikilink")をfor … in … のように書くことがあり、このときのfor文は[イテレータ](../Page/イテレータ.md "wikilink")の繰り返し処理をする文になる。

## 文法

### C 系

[awk](https://ja.wikipedia.org/wiki/awk "wikilink"), [C](../Page/C言語.md "wikilink"), [C++](../Page/C++.md "wikilink"), [C\#](../Page/C_Sharp.md "wikilink"), [D](../Page/D言語.md "wikilink"), [Java](https://ja.wikipedia.org/wiki/Java "wikilink"), [JavaScript](../Page/JavaScript.md "wikilink"), [Perl](../Page/Perl.md "wikilink")などでは基本的な構文は以下のようになる。

``` c
for(初期化; ループの継続条件; カウンタ変数の更新)
    文
```

文はどのような文でもよいが、次のような文がよく使われる。

``` c
for(…; …; …)
    式;              /* 単文 */
```

``` c
for(…; …; …){
    0個以上の文       /* 複文 */
}
```

``` c
for(…; …; …)
    for(…; …; …)     /* 入れ子になったfor文 */
        式;
```

このループは次のような手順で実行される。

1.  初期化を実行する。
2.  条件を評価する。条件が偽ならば、ループを終了する。
3.  真文を実行する。
4.  カウンタ変数の更新を実行する。
5.  条件の評価に戻る。

条件がはじめから偽の場合は、真文は一度も実行されない。また、初期化・条件・カウンタ変数の更新の三つは、それぞれ省略することが出来る。条件を省略した場合、条件は常に真であるとみなされ、ループから強制的に抜け出る構文（break, return など）がなければ[無限ループ](../Page/無限ループ.md "wikilink")となる。

例えば、初期化とカウンタ変数の更新を省略し、条件のみを記述する場合、次のようになる。

``` c
for (; x < 100;)
    ……
```

初期化などを省略した場合でも、丸括弧内で区切りとして使われる ; を省略することはできない。

[C99](../Page/C99.md "wikilink")、C++、C\#、Java では初期化は式に限られず、[ローカル変数](../Page/ローカル変数.md "wikilink")を宣言できる。for文は暗黙のブロックを作る、つまり

``` c
{
    for(…; …; …)
        ……
}
```

と等価とみなされるため、宣言された変数の[スコープ](https://ja.wikipedia.org/wiki/スコープ "wikilink")はfor文内（`for(…; …; …)`を含む）に限られる。さらにC99およびC++に関しては、外側のスコープで定義した変数と同じ名前の変数を内側のスコープで定義することができる。たとえば次のコードでは、それぞれの i は別のブロックにあるため、正常なコードとなる。

``` c
int i = 1;
for(int i = 0; i < 10; i++)
    ……
for(int i = 0; i < 10; i++)
    for(int i = 0; i < 10; i++)
        ……
/* ここでの i は 1 */
```

ただしANSI C++規格が制定される前（AT\&T C++ 2.0まで）のC++では暗黙のブロックはなかったため、このコードでは同じブロック内で i が複数回宣言されておりコンパイルエラーとなった。C\#およびJavaでは、外側のスコープで定義した変数と同じ名前の変数を内側のスコープで定義することができないため、コンパイルエラーとなる。

初期化（式の場合）・ループの継続条件・カウンタ変数の更新は、それぞれ1つの式のみが許される。ただしコンマ演算子を使って、実質的に2つの演算を1つの式で表すことができる。初期化で宣言をする場合も、1つの宣言文のみが許される。したがって、同じ[型の場合に限り複数変数を宣言できる](https://ja.wikipedia.org/wiki/データ型 "wikilink")。

``` c
for (int i = 0, j = 0; i < 10; i++, j++)
    ……
```

#### 例文

``` c
int x;
for (x = 0; x < 100; x++) {
  printf("x は %d です。\n", x);
}
```

これを実行すると、次のような出力結果が得られる。

`x は 0 です。`
`x は 1 です。`

`…………`

`x は 98 です。`
`x は 99 です。`

はじめ[変数xの値は](https://ja.wikipedia.org/wiki/変数_\(プログラミング\) "wikilink")0であり、真文が1回実行されるたびに1が加えられる。真文が100回実行されるとxの値は100になり条件が成り立たなくなるため、このときこのループは終了する。

ループを終了するには、ループの条件を偽にするほかに真文において[break文](https://ja.wikipedia.org/wiki/break文 "wikilink")を使う方法もある。ループの条件が常に真であり、真文にbreak文が含まれていない場合（またはbreak文が実行されない場合）、ループは無限ループとなる。また、真文が複数の文からなる場合、[continue文](https://ja.wikipedia.org/wiki/continue文 "wikilink")を使うことで真文の実行を中止し、カウンタ変数の更新から処理を再開することができる。

C言語の[while文](https://ja.wikipedia.org/wiki/while文 "wikilink")は、初期化とカウンタ変数の更新を省略したfor文として書き換えることができる。したがって、C言語におけるfor文はwhile文を一般化したものといえる。

### [Pascal](../Page/Pascal.md "wikilink")

Pascalでの構文は以下のようになる（[BASIC](../Page/BASIC.md "wikilink")の基本的な構文も同様である）。

``` pascal
for 変数 := 初期値 to 終値 do
  文
```

このループは次のような手順で実行される。

1.  カウンタ変数に初期値を代入する。
2.  カウンタ変数の値が終値よりも大きいならば、ループを終了する。(条件の評価)
3.  文を実行する。
4.  カウンタ変数の値を次の値（Succ関数の結果。整数型変数なら1を加えることになる）にし、条件の評価に戻る。

C言語などと異なり、初期化とカウンタ変数の更新がそれぞれ、初期値の代入と1を加える（または減らす）ことに限定され、さらにループ継続条件が「カウンタ変数が終値より大きいか否か」だけに限定されている。そのため、Cのfor文よりも特殊化されたものと考えることができる。

#### 例文

``` pascal
for x := 0 to 99 do
  writeln('x は ', x, ' です。')
```

実行結果はCおよびそれに類する言語の場合で示したのと同様である。

### [BASIC](../Page/BASIC.md "wikilink")

`FOR 変数 = 初期値 TO 終値 STEP 加算値`
` 文`
`NEXT 変数`

このループは次のような手順で実行される。

1.  カウンタ変数に初期値を代入する。
2.  カウンタ変数の値が、初期値が終値よりも小さい場合大きいならば、また、初期値が終値よりも大きい場合小さいならば、ループを終了する。(条件の評価)
3.  文を実行する。
4.  カウンタ変数の値に加算値を足し、条件の評価に戻る。

また、以下の条件の場合には省略可能な部分がある。

  - "STEP 加算値" が省略された場合、加算値は1とみなされる。

#### 例文

`FOR x = 0 TO 99 STEP 1`
` PRINT "x は " & x & " です。"`
`NEXT x`

実行結果はCおよびそれに類する言語の場合で示したのと同様である。

## 関連項目

  - [foreach文](https://ja.wikipedia.org/wiki/foreach文 "wikilink")
  - [if文](https://ja.wikipedia.org/wiki/if文 "wikilink")
  - [while文](https://ja.wikipedia.org/wiki/while文 "wikilink")
  - [do-while文](https://ja.wikipedia.org/wiki/do-while文 "wikilink")
  - [goto文](https://ja.wikipedia.org/wiki/goto文 "wikilink")
  - [制御構造](../Page/制御構造.md "wikilink")

[Category:制御構造](https://ja.wikipedia.org/wiki/Category:制御構造 "wikilink") [Category:反復処理](https://ja.wikipedia.org/wiki/Category:反復処理 "wikilink")