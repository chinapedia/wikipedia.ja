> この記事は[Switch文](https://ja.wikipedia.org/wiki/Switch文)から翻訳されています。


**switch文**（スイッチぶん）とは、[プログラミング言語](../Page/プログラミング言語.md "wikilink")において、ある式の値に応じて多分岐を行なう文である。

[最適化の仕方によって多少変わることはあるが](../Page/コンパイラ最適化.md "wikilink")、場合によっては[テーブルジャンプ](../Page/テーブルジャンプ.md "wikilink")などにより、条件判断を繰り返す[if文](https://ja.wikipedia.org/wiki/if文 "wikilink")より効率的に実行される。 __TOC__

## 文法

### C言語

構文は以下の通り。

``` C
switch (制御式) {
case 値1:
    文
    文
    ………
    break;
case 値2:
    文
    文
    ………
    break;
default:
    文
}
```

上記の「case」ラベルはいくつでも記述することができる。caseラベルの「値」はコンパイル時に決まる整定数式 (integer constant expression) である必要がある。

この文は次のような手順で実行される。

1.  制御式 を評価し、整数値を得る。
2.  その整数値がどれかのcaseで指定された値であるなら、そのcaseに引き続く文に飛ぶ。
3.  どのcaseでも指定されていなければ、defaultに引き続く文に飛ぶ。
4.  もしdefaultが記述されていなければ、何も実行せずにswitch文を抜ける。

#### フォールスルー

ここで注意しなければならないのが、caseは[ラベルに過ぎず](https://ja.wikipedia.org/wiki/ラベル_\(プログラミング\) "wikilink")、そのcaseより前からの実行から、そこでswitch文を抜けさせる働きはない点である（一般的には、次のcaseがあらわれる直前に[break文](https://ja.wikipedia.org/wiki/break文 "wikilink")を置く）。このルールはフォールスルー (fall through) と言い、制御の流れが合流する動作をさせたい場合に便利であるが、一方でbreak文の書き忘れによる[バグ](../Page/バグ.md "wikilink")、ループを抜けるbreakと取り違える誤読によるバグなど、バグの温床として問題視されてきた。

そのため[lint](https://ja.wikipedia.org/wiki/lint "wikilink")では、意図的にフォールスルーしていることを示す`/* FALLTHROUGH */`などのコメントが記述されていない限り警告を出す。また、Cに類似した構文を採用した言語でも、[C\#のように対策](../Page/C_Sharp.md "wikilink")（後述）した言語仕様にされていることがある。

上記の例は、[if文](https://ja.wikipedia.org/wiki/if文 "wikilink")を羅列することで同様の動作を実現することができる。なおif文では比較対象の「値」が整定数式である必要がない点においてswitch文よりも柔軟である。

``` C
_tmp_ = 制御式;
if (_tmp_ == 値1) {
    文
}
else if (_tmp_ == 値2) {
    文
}

………

else {
    文
}
```

defaultは最後に記述される場合が多いが、必ずしも最後である必要はない。

switchによる分岐は以下のように[do-while文](https://ja.wikipedia.org/wiki/do-while文 "wikilink")と組み合わせることも可能である。

``` C
switch (count)
{
    default:       do {    printf("%d\n", count); count++;
    case 0:                printf("%d\n", count); count++;
    case 1:                printf("%d\n", count); count++;
    case 2:                printf("%d\n", count); count++;
                   } while (count);
}
```

例えば[Duff's deviceではそのような使われ方をしている](../Page/Duff's_device.md "wikilink")。

### C\#

[C\#でのswitch文はC言語と似たような見た目であるが](../Page/C_Sharp.md "wikilink")、フォールスルーについての挙動は異なる。

``` csharp
switch (式)
{
case 0:
case 1:
  // 式が0か1の時に実行
  System.Console.WriteLine("Case 0 or 1.");
  return 1;

case 2:
  System.Console.WriteLine("Case 2.");
  goto case 3: // case 3も実行

case 3:
  System.Console.WriteLine("Case 3.");
  break;

default:
  System.Console.WriteLine("Default.");
  break; // ここのbreakも省略不可
}
```

C\#では、caseラベルは文に付属する扱いとなるが、1つの文に複数のcaseラベルを付けることができる。また、C言語のようなフォールスルーは禁止されており、次のcaseラベル付きの文、あるいはswitchブロックの末端に、通常の制御フローで[到達してはならない](https://ja.wikipedia.org/wiki/到達不能コード "wikilink")。すなわち、[breakでswitchを抜ける](https://ja.wikipedia.org/wiki/break文 "wikilink")、[returnで関数ごと抜ける](https://ja.wikipedia.org/wiki/return文 "wikilink")、[例外を投げる](../Page/例外処理.md "wikilink")、[無限ループ](../Page/無限ループ.md "wikilink")してそれ以上進まない\[1\]、goto caseするなどの書き方が必要となる\[2\]。goto caseにより、C言語ではフォールスルーを使って書くことができた、制御の合流を書くことができる。

Cや[C++](../Page/C++.md "wikilink")では、switch文の制御式には整数型の式、またcaseラベルには整定数式しか使用できないのに対し、C\#ではそれぞれ文字列型および文字列リテラルも使用できる。また、整数型あるいは整数型に準ずる値型のnull許容型`System.Nullable`も使用することができる。

C\# 7.0以降では型switchを使用できる。

``` csharp
// C# 7.0以降
switch (obj)
{
    case int num when num < 0:
        Console.WriteLine($"objは負の32bit整数{num}です。");
        break;
    case string str when str.StartsWith("H"):
        Console.WriteLine($"objはHから始まる文字列{str}です。");
        break;
    case string str:
        Console.WriteLine($"objは文字列{str}です。");
        break;
    default:
        Console.WriteLine("objは想定外の型あるいは値です。");
        break;
}
```

### Go

[Goでは](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink")、caseに複数の値を指定できる。次のcaseの直前にfallthrough文を置くとフォールスルーになる。

### PHP

[PHPでは](../Page/PHP_\(プログラミング言語\).md "wikilink")、C\#と同様、文字列にも、switch文が適用できる。

``` php
switch (str) {
    case "ABC":
        文A;
        break;
    case "XYZ":
        文B;
        break;
    case "123":
        文C;
        break;
    default:
        文D;
        break;
}
```

### BASIC

[構造化された](../Page/構造化プログラミング.md "wikilink")[BASIC](../Page/BASIC.md "wikilink")では、Select Caseステートメントが存在することが多い。このステートメントでは、文字列または整数を対象にできる。

``` vb
Select Case str
    Case "ABC"
        文A
    Case "XYZ"
        文B
    Case "123"
        文C
    Case Else
        文D
End Select
```

``` vb
Select Case age
    Case Is < 20
        文A
    Case 20 To 29
        文B
    Case 30,50,70
        文C
    Case Else
        文D
End Select
```

Cなどと違い、各Caseはラベルではなく、Selectステートメントはフォールスルーでない。

### Perl

[Perl](../Page/Perl.md "wikilink")では、perl-5.8以降からuse Switchとした上でswitch case文が使えるようになった。それ以前のバージョンのperlに関しては、Perl付属文章perlsynドキュメントのBasic BLOCKs and Switch Statementsの節に書式の例が書かれている。

### Ruby

[Ruby](../Page/Ruby.md "wikilink")では、case式により同様の多分岐ができる。フォールスルーはない。ラベルとして置いたものと条件値は`===`演算子で比較される\[3\]\[4\]ため、これを[オーバーロードすることでクラスに応じた一致判定を行うことができる](../Page/多重定義.md "wikilink")。Ruby自体のクラスライブラリ内でも、[正規表現](../Page/正規表現.md "wikilink")の一致判定\[5\]、範囲オブジェクトでの範囲内かどうかの判定、オブジェクトがあるクラスに属するかの判定など、各種の定義がなされている。

### Mediawiki

[Mediawiki](https://ja.wikipedia.org/wiki/Mediawiki "wikilink")系の[Template](https://ja.wikipedia.org/wiki/Template "wikilink")においては、[ParserFunctionsを用いて多分岐をおこなうことができる](https://ja.wikipedia.org/wiki/mw:Help:Extension:ParserFunctions/ja "wikilink")。一対一の分岐処理の他、複数の値に対して同一の処理を定義する一種のフォールスルーも実現できる。しかし、CやC\#といった言語でのreturn文やbreak文が無い。そのため処理の途中でSwitch文を抜けるにはif等の条件文で処理を囲み、実行させないよう制御する必要がある。

詳細については、[Help:条件文\#switchの項を参照の事](https://ja.wikipedia.org/wiki/Help:条件文#switch "wikilink")。

### Excel(Office 365),Libre Office Calcの場合

CHOOSE関数の拡張としてSWITCH関数が利用できる。

` SWITCH(検索値, 値1, 結果1, 値2, 結果2, ..., 値126, 結果126, 既定の結果)`

| 検索値   | 検索する値を指定します。数値または文字列が指定できる。                             |
| ----- | ------------------------------------------------------- |
| 値     | 検索される値を指定する。数値または文字列が指定できる。                             |
| 結果    | ［検索値］が［値］に一致したときに返したい値を指定する。［値］と［結果］の組み合わせは126個まで指定できる。 |
| 既定の結果 | ［検索値］が［値］のどれにも一致しなかったときに返したい値を指定する。この引数は省略することもできる。     |

## 条件式ベースで使う

Ruby\[6\]や[SQL](../Page/SQL.md "wikilink")\[7\]では、switchに相当する文の後の式が必須ではなく、省略した場合はwhenとして書かれた式のうち、最初に真となるところを実行するようになる。PHPやJavaScriptなど、caseの式が定数である必要性がない言語の場合、`switch(true)`と書くことで同様の動作を実現できる。

## 脚注

### 脚注

### 出典

## 関連項目

  - [if文](https://ja.wikipedia.org/wiki/if文 "wikilink")
  - [制御構造](../Page/制御構造.md "wikilink")

[ru:Оператор ветвления\#Переключатель](https://ja.wikipedia.org/wiki/ru:Оператор_ветвления#Переключатель "wikilink")

[Category:制御構造](https://ja.wikipedia.org/wiki/Category:制御構造 "wikilink")

1.  むろん、C\#コンパイラが[停止性問題](../Page/停止性問題.md "wikilink")を解くことはできないため、この扱いはループ条件が定数の場合に限られる。
2.  [switch(C\#リファレンス)](http://msdn.microsoft.com/ja-jp/library/06tc147t.aspx)、[MSDN](https://ja.wikipedia.org/wiki/MSDN "wikilink")（2014年5月30日閲覧）。
3.  [Ruby 1.9.3マニュアル - 制御構造](http://docs.ruby-lang.org/ja/1.9.3/doc/spec=2fcontrol.html#case)、2014年3月3日閲覧。
4.  なお、Rubyの`===`演算子は、JavaScriptやPHPでのような「厳密に等しい」という意味ではない。
5.  [Ruby 1.9.3マニュアル - class Regexp](http://docs.ruby-lang.org/ja/1.9.3/class/Regexp.html#I_--3D--3D--3D)、2014年3月3日閲覧。
6.
7.  どちらの言語も、switch...caseではなく、case...whenと書く。