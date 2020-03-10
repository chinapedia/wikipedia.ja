> この記事は[X-BASIC](https://ja.wikipedia.org/wiki/X-BASIC)から翻訳されています。


**X-BASIC**は、シャープ[X68000](https://ja.wikipedia.org/wiki/X68000 "wikilink")用に[ハドソン](../Page/ハドソン.md "wikilink")および[シャープ](../Page/シャープ.md "wikilink")が開発した[BASIC](../Page/BASIC.md "wikilink")言語である。

特徴としてはC言語に似た独自の構文をもった構造化言語であり、他の多くのBASICとは似ていないという印象が強い。一般にBASICには大文字を基本としているものが多いが、小文字を使うのも特徴である。

## セーブとロード

ユーザが記述した関数部分は[行番号](https://ja.wikipedia.org/wiki/行番号 "wikilink")なしで`save`することによって、ライブラリ的なファイルを作って再利用することも可能である（なお行番号なしで`save`された関数を実行する際には、行番号付きで`end`よりも後の行に`load`する必要がある）。

## 外部関数

X-BASIC[インタプリタ](../Page/インタプリタ.md "wikilink")環境は、[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")などで記述された[機械語](../Page/機械語.md "wikilink")の外部モジュールを追加／削除することによって、インタプリタで処理できる外部関数の機能をカスタマイズできる仕様になっている。

## 構文

実行可能なコードでは、標準的なBASICと同様にすべての行の先頭に行番号を記述する。　トークンの大文字・小文字を区別し、予約ステートメントは小文字で記述される。

ブロックは、ブラケット文字*{*と*}*で囲んで複数行に渡って構文を記述することができる。

### 変数

変数は型を持ち、変数の宣言を記述する。

  - 整数型 `int` 32ビット長の符号付き整数を扱う。
  - 整数型 `char` 8ビット長の符号なし整数を扱う。
  - 浮動小数点型 `float` 倍精度浮動小数点数を扱う。
  - 文字列型 `str` 255文字以内の文字列を扱う。

### 配列

配列はdimステートメントを用いて定義し添字は*(*と*)*で括る。

### 制御

繰り返し制御には、`for`～`next`の他に、`break`および`cotinue`の制御が可能な`while`～`endwhile`、`repeat`～`until`ステートメントを有する。

### 関数

ユーザー関数の定義は`end`より後の行にて、`func`～`endfunc`ステートメントを用いて定義することができ、引数は*(*と*)*の間にカンマで区切って変数の型を含めて定義する。

## コード例

``` basic
 10 /* Tiny EDITOR ted.bas
 20 str fname[20]
 30 str buff[200]
 40 int fp, fc
 50 char CR=13, LF=10
 60 /*
 70 title()
 80 fninput ()
 90 fp=fopen(fname, "c")
100 edit()
110 fc=fclosc(fp)
120 end
130 /*
140 func title()
150 str dummy
160   cls
170   print "これは簡易エデイタです。"
180   print "メモなどを作成するときにお伎いください。"
190   print "なお、すでに存在するファイル名を指定したときは、無条"
200   print "件にそのファイルの内容を削除してしまいます。"
210   print
220   print "                            何かキーを押してください  ";
230   dummy=inkey$
240   cls
250 endfunc
260 func fninput()
270   print "Input file name >";
280   linput fname
290 endfunc
300 func edit()
310   print "Input data(END =/)":print
320   while buff <> "/"
330     linput ">";buff
340      if buff <> "/" then {
350        fwrites(buff,fp)
360        fputc(CR,fp)
370        fputc(LF,fp)
380      }
390   endwhile
400 endfunc
```

## コンパイル

X68000本体を購入すると標準で付属していたX-BASIC開発環境は、エディタ機能を持ったインタプリタであるが、別売りのC[コンパイラ](../Page/コンパイラ.md "wikilink")を購入すると、X-BASICから[C言語](../Page/C言語.md "wikilink")に変換するツールを用いて機械語にコンパイルして実行できる。

### 構文チェッカ

X-BASICとC言語の言語仕様では、[演算子の優先順位](https://ja.wikipedia.org/wiki/演算子の優先順位 "wikilink")などプログラミング上問題になりやすい若干の差異があったために、「XBAStoC CHECKER PRO-68K(CZ-260LS)」（BCチェッカ）という構文検査ツールが発売されていた。

## 関連書籍

  -
  -
## 関連項目

  - [X68000](https://ja.wikipedia.org/wiki/X68000 "wikilink")
  - [BASIC](../Page/BASIC.md "wikilink")
  - [C言語](../Page/C言語.md "wikilink")
  - [Human68k](../Page/Human68k.md "wikilink")

[Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink") [Category:シャープ](https://ja.wikipedia.org/wiki/Category:シャープ "wikilink") [Category:ハドソン](https://ja.wikipedia.org/wiki/Category:ハドソン "wikilink")