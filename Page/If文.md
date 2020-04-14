> この記事は[If文](https://ja.wikipedia.org/wiki/If文)から翻訳されています。


**if文**（イフぶん）は[プログラミング言語](../Page/プログラミング言語.md "wikilink")において、[真理値](https://ja.wikipedia.org/wiki/真理値 "wikilink")に従って「もしXならば、Yせよ、さもなくばZせよ」というような条件実行の「[文 (プログラミング)](https://ja.wikipedia.org/wiki/文_\(プログラミング\) "wikilink") 」で、[制御構造](../Page/制御構造.md "wikilink")のひとつである。**if else文**と呼ばれることもある。

具体的な構文はプログラミング言語によって異なるが一般的に、条件式と、条件式の評価結果の値が「真として扱うべき値」の場合に実行される「then節」と呼ばれる部分があり、「偽として扱うべき値」の場合に実行されるelse節と呼ばれる部分が付く場合もある。

then節とelse節が式になる「[条件演算子](../Page/条件演算子.md "wikilink")」がある言語も多い。言語によってはifが文ではなく、条件演算子と同様の「if式」である言語もある。

## 真偽値

「真として（あるいは、偽として）扱うべき値」について詳説する。条件式の値が[真理値](https://ja.wikipedia.org/wiki/真理値 "wikilink")をとる[ブーリアン型](../Page/ブーリアン型.md "wikilink")でなければならない言語もあるが、そのように限定していない言語もある。C言語にはそもそもブーリアン型が無くintで代用しているが、条件式としては汎整数型のゼロ（0）の他、[ヌルポインタ](https://ja.wikipedia.org/wiki/ヌルポインタ "wikilink")や 0.0 なども偽として扱われる。Rubyではnilとfalse以外は真として扱われる。JavaScriptにはtruthyとfalsyという用語があり、falseの他いくつかの値がfalsyで、その他の多くの値はtruthyである。比較的少数の偽になる値の他は、真、という言語が多いが、それと逆に、[Dart](https://ja.wikipedia.org/wiki/Dart "wikilink")言語（のproduction mode）のようにtrue以外は偽という言語もある（checked modeではbool以外の型だとエラー）。

## 構文と構文以外

以下ではいくつかの言語における、if文、乃至それに類似したものの、構文（syntax）と、構文以外のことについて述べる。

### C

条件式は任意の式である（C99以前には真理値のみを扱うための型は無かった）。整数値0となる値は偽、他の値は真として扱われる。真を代表して表すための値は整数値1である。then節とelse節には、1個の文か、{ } で囲まれる複文を書く。

真の時だけ実行するとき

``` c
if (条件式)
 then節
```

真と偽の両方に振り分けるとき

``` c
if (条件式)
 then節
else
 else節
```

### Lisp

Lispでは、ifは関数のような見掛けだが実引数が評価されない特殊形式（[マクロ](https://ja.wikipedia.org/wiki/マクロ_\(コンピュータ用語\)#Lisp_のマクロ "wikilink")）である。真偽値は、`nil` という名前や中身の無いカッコ `()` で表現される空リストが偽として扱われ、他の値は真として扱われる。then節とelse節のどちらも式である。

真の時だけ実行するとき

``` lisp
(if 条件式 then節)
```

真と偽の両方に振り分けるとき

``` lisp
(if 条件式 then節 else節)
```

Lispにはcondという、同等の機能を実現できる特殊形式もある。仕様や実装によっては、ifがcondに展開されるマクロのこともあるし、condがifに展開されるマクロのこともある。

### Pascal

then節とelse節には、1個の文か、`begin`～`end` で囲まれる複文を書く。

真の時だけ実行するとき

``` pascal
if 条件式 then
 then節
```

真と偽の両方に振り分けるとき

``` pascal
if 条件式 then
 then節
else
 else節
```

### Ada

Adaでは条件式の型は`Boolean`(もしくは`Boolean`の派生型)でなければならない。これは[Java](https://ja.wikipedia.org/wiki/Java "wikilink")等も同様である。

真の時だけ実行するとき

``` ada
if 条件式 then
 then節
end if;
```

真と偽で実行文を変えるとき

``` ada
if 条件式 then
 then節
else
 else節
end if;
```

### Perlの場合

真の時だけ実行するとき

``` perl
真文 if 条件文
```

偽の時だけ実行するとき

``` perl
偽文 unless 条件文
```

また、C言語風の記述法も可能である。

真の時だけ実行するとき

``` perl
if(条件文) {
 真文
}
```

真と偽で実行文を変えるとき

``` perl
if(条件文) {
 真文
} else {
 偽文
}
```

### Rubyの場合

Rubyのifは厳密に言えば**if式**であり、条件が成立した方の節で最後に評価された式の値を返す。

真の時だけ実行するとき

``` ruby
if 条件式 (then)
 真文
end
```

真と偽で実行文を変えるとき

``` ruby
if 条件文 (then)
 真文
else
 偽文
end
```

### BASICの場合

真の時だけ実行するとき

`IF 条件式 THEN 真文`

真と偽で実行文を変えるとき

`IF 条件式 THEN 真文 ELSE 偽文`

真文・偽文が1行で書ききれない場合は[goto文](https://ja.wikipedia.org/wiki/goto文 "wikilink")が併用される。

### Visual Basicの場合

真の時だけ実行するとき

``` vb
If 条件式 Then
 真文
End If
```

真と偽で実行文を変えるとき

``` vb
If 条件式 Then
 真文
Else
 偽文
End If
```

真文・偽文が短い場合には BASIC と同様の書き方も可能である。

### REALbasicの場合

真の時だけ実行するとき

`If 条件式 Then`
` 真文`
`End If`

真と偽で実行文を変えるとき

`If 条件式 Then`
` 真文`
`Else`
` 偽文`
`End If`

### OpenOffice.org Calc,Libre Office Calc, Excel の場合

真の式だけ実行するとき

`IF(条件式;真文;"")`

真と偽で実行文を変えるとき

`IF(条件式;真文;偽文)`

ただし[Libre Office Calc](https://ja.wikipedia.org/wiki/LibreOffice_Calc "wikilink"), [Office 365ではさらに条件を追加することができ](https://ja.wikipedia.org/wiki/Office_365 "wikilink")

`IFS(条件式1, 真の場合1, 条件式2, 真の場合2, ..., 条件式127, 真の場合127)　(条件式は厳しいものから並べる必要がある。)`

IF文の入れ子構造と処理は同一である。ただし可読性が良い。

### FORTRAN

以下は、Fortran77以降の、論理IF文の場合である。1行のみの場合

``` fortran
if(条件式) 真文
```

複数行にまたがる場合

``` fortran
if(条件式1) then
  条件式1が真の場合ここから
  ここまでのプログラムが実行される（複数行）
else　if(条件式2) then
  条件式2が真の場合ただしすでに条件式1が成り立っている場合は除くここから
  ここまでのプログラムが実行される（複数行）
else
  すべてのなかのいずれの条件にも当てはまらない場合ここから
  ここまでのプログラムが実行される（複数行）
end if
```

### Forthの場合

真の時だけ実行するとき

`条件式 IF 真文 THEN`

偽の時だけ実行するとき

`条件式 NIF 偽文 THEN`

真と偽で実行文を変えるとき

`条件式 IF 真文 ELSE 偽文 THEN`

または

`条件式 NIF 偽文 ELSE 真文THEN`

### ひまわりの場合

真の時だけ実行するとき

`もし、{条件式}ならば、(`
`{処理}`
`)`

真と偽で実行文を変えるとき

`もし、{条件式}ならば、(`
`{処理}`
`)`
`違ったら、(`
`{処理}`
`)`

### HSPの場合

真の時だけ実行するとき

`if 条件式 : 真文`

真と偽で実行文を変えるとき

`if 条件式 : 真文 : else : 偽文`

また、Cのようにブレイスを用いることもできる。

`if 条件式 {`
`  真文`
`} else {`
`  偽文`
`}`

## プログラム例

特に断りがない場合`na`と`nb`の大きい方を`nc`に代入という意味である。

### Cでの例

``` c
if(na > nb) {
  nc = na;
} else {
  nc = nb;
}
```

  - `nc = (na > nb) ? na : nb` としても同じ事ができる。

### Common Lisp での例

``` lisp
(if (> na nb)
 (setq nc na)
 (setq nc nb)
 )
```

これはcondを使った

``` lisp
(cond
 ((> na nb) (setq nc na))
 (t (setq nc nb))
 )
```

と同様であるが、そもそもまともな神経を持っていれば、

``` lisp
(setq nc (if (> na nb) na nb))
```

と書くであろう。

### Pascalでの例

``` pascal
if na > nb then nc := na else nc := nb
```

### R言語での例

### FORTRANの例

``` fortran
if(a.eq.b) c=5
```

上記の記述では`a=b`の場合`c=5`になる簡単なプログラム例である。

``` fortran
if(a.eq.100) then
b=30
else if(a.eq.80) then
b=25
else
b=20
end if
```

上記の記述では`a=100`の場合は`b=30`となり，`a=80`の場合は`b=25`，その他の場合は`b=20`となるプログラム例である。

## 論理積・論理和による擬似的なIf文

仮に `&&` を論理積を表す演算子として、

`左辺 && 右辺`

という論理式で、左辺が真にならなければ右辺を評価しない言語（[短絡評価](../Page/短絡評価.md "wikilink")）では、これを

`If (左辺) { 右辺 }`

と等価とみなすことができる。つまり左辺が条件文で、右辺が真文となるわけである。
同様に `||` を論理和を表す演算子だとすると、

`左辺 || 右辺`

は

`If (Not 左辺) { 右辺 }`

と等価となり、左辺が偽のときだけ右辺が実行される。

たとえばMS-DOSやWindowsのバッチファイルでは

``` bat
CHDIR C:\HOGE || ECHO フォルダがみつかりません
```

（もしCHDIRコマンドが失敗したら、ECHOコマンドが実行される）

言語によっては、このように論理積演算や論理和演算を擬似的なIf文として代用する場合が多々ある。

## 関連項目

  - [論理包含](../Page/論理包含.md "wikilink")
  - [分岐命令](../Page/分岐命令.md "wikilink") - [機械語](../Page/機械語.md "wikilink")
  - [制御構造](../Page/制御構造.md "wikilink")
  - [ヨーダ記法](https://ja.wikipedia.org/wiki/ヨーダ記法 "wikilink") - If文内の条件式で定数を左辺に置くプログラミングスタイル

[Category:制御構造](https://ja.wikipedia.org/wiki/Category:制御構造 "wikilink") [Category:条件](https://ja.wikipedia.org/wiki/Category:条件 "wikilink")