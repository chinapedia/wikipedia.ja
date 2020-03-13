> この記事は[Break](https://ja.wikipedia.org/wiki/Break)から翻訳されています。


**break文**は、[プログラミング言語](../Page/プログラミング言語.md "wikilink")の[ループ](../Page/ループ_\(プログラミング\).md "wikilink")[制御構造](../Page/制御構造.md "wikilink")で用いられる文で、最も内側の[for文](https://ja.wikipedia.org/wiki/for文 "wikilink")、[while文](https://ja.wikipedia.org/wiki/while文 "wikilink")、[do-while文](https://ja.wikipedia.org/wiki/do-while文 "wikilink")から脱出する。また、[C言語](../Page/C言語.md "wikilink")のような[switch文](https://ja.wikipedia.org/wiki/switch文 "wikilink")がある言語では、（ループではないが）switch文から脱出する際にも使用される\[1\]。

## 構文と意味

[C言語](../Page/C言語.md "wikilink")、およびそれに仕様を類似させている言語が備える[文のひとつであり](https://ja.wikipedia.org/wiki/文_\(プログラミング\) "wikilink")、構文としては[キーワード](../Page/予約語.md "wikilink") `break` とセミコロンから成る。[Perl](../Page/Perl.md "wikilink")では`last`というキーワードである。

``` c
  break;
```

ループ中（またはswitch文）の内部で実行されると、ループ全体（またはswitch文）を打ち切って、次の文へと制御を移す。

## 例

C言語において、単純なループからbreak文を使って抜ける例を示す。

``` c
while (1) {
  if (条件式) break;
}
```

この例では、if文の条件式が成立すると**break文**が実行され、このループの直後に制御が移される。

switch文から脱出する例も示す。詳細は[switch文](https://ja.wikipedia.org/wiki/switch文 "wikilink")を参照。

``` c
switch (式) {
case 定数式:
  文
  break;
default:
  文
  break;
}
```

## 多重ループからの抜け出し

### C言語

最初の例として、内側のループからの抜け出しを示す。

``` c
while (1) {
  while (1) {
    if (条件式) break;
  }
}
```

このコードの`break;`は内側のループのみから抜け出す。外側のwhileループは[無限ループ](../Page/無限ループ.md "wikilink")になる。

次に、多重ループからの抜け出しについて論じる。

C言語では、多重ループから一気に抜ける際には[goto文](https://ja.wikipedia.org/wiki/goto文 "wikilink")を使用することができる\[2\]。

``` c
while (1) {
  while (1) {
    if (条件式) goto label;
  }
}
label: ;
```

もしgoto文を使わずにbreak文を使って書くとすれば、一例としては以下のようになり、複雑かつ冗長となる。複雑度の上昇はバグの混入を許す原因ともなる。

``` c
int flag = 0;
while (1) {
  while (1) {
    if (条件式) {
      flag = 1;
      break;
    }
  }
  if (flag == 1) {
     break;
  }
}
```

ほかにも、[関数をそのまま脱出して呼び出し元に制御を返してよいということが前提にあるのであれば](../Page/サブルーチン.md "wikilink")、多重ループを脱出するのに[return文](https://ja.wikipedia.org/wiki/return文 "wikilink")を使うこともできる。

``` c
while (1) {
  while (1) {
    if (条件式) return;
  }
}
```

このような場合について、gotoを使うのと同程度に明瞭簡潔に書けるようにするため、次節以降で述べるように、gotoを廃した言語では、ラベル付きbreakなどの「弱められたgoto」と言えるような機能が考案されている。

### Java および JavaScript

``` java
label: // 外側のwhile文にラベルをつける
  while (true) {
    while (true) {
      if (条件式) break label;
    }
  }
```

[Java](https://ja.wikipedia.org/wiki/Java "wikilink")や[JavaScript](../Page/JavaScript.md "wikilink")はgoto文をサポートしておらず、代わりにラベル指定付きのbreak文を使うことで多重ループから一気に抜けることができる。

### PHP

``` php
while (true) {
  while (true) {
    if (条件式) break 2;
  }
}
```

[PHPではgoto文がバージョン](../Page/PHP_\(プログラミング言語\).md "wikilink")5.3から実装されたが、break文にループを抜ける段数を指定することも可能である\[3\]。

## 脚注

## 関連項目

  - [continue文](https://ja.wikipedia.org/wiki/continue文 "wikilink")

[Category:制御構造](https://ja.wikipedia.org/wiki/Category:制御構造 "wikilink")

1.  このbreak文の性質上、ループ脱出のためのbreak文を含むif文をswitch文で置き換えようとする際には注意が必要である。一例としてはそのようなコードによるバグが、1990年1月15日に米国AT\&Tの長距離電話網が大規模に麻痺する障害を起こした。詳細は「[All Circuits are Busy Now: The 1990 AT\&T Long Distance Network Collapse](http://users.csc.calpoly.edu/~jdalbey/SWE/Papers/att_collapse.html)」を参照。[:en:List of software bugs\#Telecommunicationsも参照](https://ja.wikipedia.org/wiki/:en:List_of_software_bugs#Telecommunications "wikilink")。
2.  最後の「label:」の後のセミコロンは「空の文」である。C言語の標準仕様では、ラベルは「ラベル付き文」としてしか存在できないので、ラベルの後に何もしない場合には構文規則上「空の文」を追加しなければならない（）。
3.  [break](http://php.net/manual/ja/control-structures.break.php) PHPマニュアル、2015年4月3日閲覧。