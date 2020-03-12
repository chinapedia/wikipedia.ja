> この記事は[Eval](https://ja.wikipedia.org/wiki/Eval)から翻訳されています。


**eval**（イーバル）はいくつかの[プログラミング言語](../Page/プログラミング言語.md "wikilink")が持つ、[文字列](../Page/文字列.md "wikilink")を[式として評価する](../Page/式_\(プログラミング\).md "wikilink")[関数](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")、または複数の[文を](https://ja.wikipedia.org/wiki/文_\(プログラミング\) "wikilink")[プログラム中のあるコンテキストで実行する](../Page/プログラム_\(コンピュータ\).md "wikilink")[サブルーチン](../Page/サブルーチン.md "wikilink")である。

evalの類の機能は[コンパイラ](../Page/コンパイラ.md "wikilink")言語よりも[インタプリタ](../Page/インタプリタ.md "wikilink")言語でより一般的である。なぜならコンパイラ言語でこのような機能を実現するには、プログラム自体に言語[処理系](https://ja.wikipedia.org/wiki/処理系 "wikilink")や（変数名などの）実行時情報を埋め込む必要があるからである。evalに近い機能を実現しているコンパイラ言語も存在する。

## セキュリティ上のリスク

信頼されないソースからのデータをevalするときには特に注意が必要である。例として[インターネット](../Page/インターネット.md "wikilink")上からデータを得る `get_data()` 関数を考える。次の擬似コードのようなプログラムは潜在的に危険である。

`data = get_data()`
`foo = eval(data)`

攻撃者がこのプログラムに例えば `"delete_system_files()"` という[文字列](../Page/文字列.md "wikilink")を与えることができると、`delete_system_files()` 関数が実行されてしまい、重要なファイルが消されてしまうかもしれない。これを防ぐためには、evalされる文字列はすべてエスケープしたり、潜在的に危険な機能を利用できないようにして実行するなどの対策が必要となる。[プログラミング言語](../Page/プログラミング言語.md "wikilink")によっては、外部から入力されたデータを「汚染されている」として印をつけるものもある。

## 適切な使用

evalは非常に強力なため、経験の浅い[プログラマ](../Page/プログラマ.md "wikilink")は何でもevalを使って済ませてしまうことがある。たいてい、そのような場合には専用のより良い選択肢が存在し、コードのパースにかかる時間が節約できる。

例えば、evalは簡易[テンプレートエンジン](../Page/テンプレートエンジン.md "wikilink")として使われることがある。[PHPでの例を示す](../Page/PHP_\(プログラミング言語\).md "wikilink")。

``` php
$name = 'John Doe';
$greeting = 'Hello';
$template = '"$greeting,  $name! How can I help you today?"';
print eval("return $template;")
```

この例は期待した動作をするが、前述のようにセキュリティ上の問題を抱えており、他の方法よりもはるかに遅い。より高速で安全な方法は単に `"$name"` という文字列を `$name` の値で置換することである。

eval は[表計算ソフト](../Page/表計算ソフト.md "wikilink")などの数式を評価する必要のあるアプリケーションで使われることがある。これは数式のパーサを自作するよりも手軽だが、自作や既存の専用のパーサを利用するほうがより良い。前述の問題点に加え、言語組み込みのevalはアプリケーション用にカスタマイズできないからである。

おそらく、evalの最も優れた使い道は（[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")などでの）[処理系のブートストラップや](../Page/ブートストラップ問題.md "wikilink")、言語の[対話的な実行環境でユーザが書いたプログラムを実行することであろう](https://ja.wikipedia.org/wiki/インタラクティブシェル "wikilink")。

## 実装

インタプリタ言語ではevalは通常のコードと同じインタプリタで実装されるのがほとんどである。

コンパイラ言語ではevalを実装するために通常のコンパイラをプログラムに埋め込むこともある。また特別のインタプリタを使うこともあり、その場合は[コードの重複が問題となる](../Page/重複コード.md "wikilink")。

## 実例

### JavaScript, ActionScript

[JavaScript](../Page/JavaScript.md "wikilink")や[ActionScript](../Page/ActionScript.md "wikilink")においては、evalは式の評価器と文の実行器のハイブリッドのような存在である。evalは最後に評価された式の値を返し（JavaScriptとActionScriptではすべての文は式である）、最後のセミコロンは省くことができる。

式評価器としての例:

``` javascript
foo = 2;
alert(eval('foo + 2'));
```

文実行器としての例:

``` javascript
foo = 2;
eval('foo = foo + 2;alert(foo);');
```

JavaScriptでのevalの使用の一例は[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")などにおける[JSONのパースである](../Page/JavaScript_Object_Notation.md "wikilink")。しかし、現在は多くのブラウザでより特化したJSON.parseが定義されている。

ActionScriptではevalを任意の式を評価するために使うことはできない。[Flash](../Page/Adobe_Flash.md "wikilink") 8のドキュメントによれば、その使用は「変数、プロパティ、オブジェクト、ムービークリップの名前」を表す式に限られ、「パラメータはStringまたはオブジェクトのインスタンスへの直接の参照のどちらでもよい」\[1\]。

###

はが最初に登場した言語である。の実装によって、最初のインタプリタが現れたのである。それ以前は、の式はコンパイルされていた。しかし一度evalが実装されると、それは単純な入力・評価・出力のループ ([REPL](https://ja.wikipedia.org/wiki/REPL "wikilink")) の一部として使われるようになり、最初のインタプリタの基礎を形作った。の後のバージョンのはコンパイラとしても実装されている。

### Perl

[Perl](../Page/Perl.md "wikilink")のevalは、文字列をプログラムとして解釈するほか、例外処理機構としても機能する。コードの塊をテストし、必要ならそれに関して警告することができる。例えば、除算において実行時エラーが発生すると`$@`で警告を出力することができる。

``` perl
# 0による除算の例外を回避する
eval { $answer = $x / $y; };
warn $@ if $@;
```

### PHP

[PHPでのevalは](../Page/PHP_\(プログラミング言語\).md "wikilink")、ほぼ、文字列中のコードをまるで `eval()` 呼び出しの代わりにファイル中に記述されているかのように実行する。例外は、エラーは `eval()` から復帰した時点で報告され、またreturn文で `eval()` の戻り値を返すことができる点である。

echoを使った例:

``` php
<?php
$foo = "Hello, world!\n";
eval('echo $foo;');
?>
```

値を返す例:

``` php
<?php
$foo = "Goodbye, world!\n";
echo eval('return $foo;');
?>
```

### PostScript

[PostScript](../Page/PostScript.md "wikilink")の`exec`演算子はオペランドを1つ取り、それが単純なリテラルならスタックにプッシュし返す。PostScriptの式を含む文字列が来た場合は、その文字列をインタプリタによって実行可能な形式に変換する。例えば、

`((Hello World) =) cvx exec`

は PostScript の式である `(Hello World) =`（文字列 `Hello World` をスタックからポップして画面に表示する）を実行可能な型を持つように変換し、そして実行する。

PostScriptでは `run` 演算子も似た機能を持つが、代わりにインタプリタそのものがファイル中のPostScriptの式を評価する。

### Python

[Python](../Page/Python.md "wikilink")での `eval` 関数は単一の式を評価する。文を実行することはできないが、文を実行する関数を実行することはできる。`exec` 文は文を実行することができる。

`eval` の例（対話モード）:

``` python
>>> x = 1
>>> eval('x + 1')
2
>>> eval('x')
1
```

`exec` の例（対話モード）:

``` python
>>> x = 1
>>> y = 1
>>> exec "x += 1; y -= 1"
>>> x
2
>>> y
0
```

### ColdFusion

[ColdFusion](../Page/ColdFusion.md "wikilink")の `evaluate` 関数は文字列で与えられた式を実行時に評価することができる。

``` cfm
<cfset x = "int(1+1)">
<cfset y = Evaluate(x)>
```

これは読み込む変数をプログラム的に選択するときなどに、特に便利である。

``` cfm
<cfset x = Evaluate("queryname.#columnname#[rownumber]")>
```

### Ruby

[Ruby](../Page/Ruby.md "wikilink")には式を評価するコンテキストごとに3種類のevalが存在する。`eval` はその場またはProcやBindingオブジェクト、`instance_eval` はインスタンス、`module_eval`（別名は`class_eval`）はモジュールかクラス、それぞれのコンテキストで評価を行う。なお、評価コンテキスト変更のために`instance_eval`や`module_eval`を使う場合、文字列でなく[ブロックを引数とすることができる](../Page/ブロック_\(プログラミング\).md "wikilink")\[2\]。

`eval`の例（メソッドfooのコンテキストで評価している）:

``` ruby
def foo
  x = 1
  binding
end

eval('x + 1', foo) #=> 2
```

`instance_eval` と `module_eval` の例:

``` ruby
class Bar
@@cvar = 10 #クラス変数
  def initialize
    @ivar = 5 #インスタンス変数
  end
end

bar = Bar.new
bar.instance_eval('@ivar') #=> 5
Bar.class_eval('@@cvar') #=> 10
```

## 脚注

## 外部リンク

  - [ANSI and GNU Common Lisp Document - eval](http://www.cs.queensu.ca/software_docs/gnudev/gcl-ansi/gcl_256.html)

[Category:制御構造](https://ja.wikipedia.org/wiki/Category:制御構造 "wikilink")

1.  [Adobe - Flash 8 LiveDocs](http://livedocs.macromedia.com/flash/8/index.html)
2.  [instance method BasicObject\#instance_eval](http://doc.ruby-lang.org/ja/1.9.3/method/BasicObject/i/instance_eval.html) - Ruby1.9.3リファレンスマニュアル