> この記事は[Whitespace](https://ja.wikipedia.org/wiki/Whitespace)から翻訳されています。


[Whitespace_in_vim2-recolored.png](https://ja.wikipedia.org/wiki/File:Whitespace_in_vim2-recolored.png "fig:Whitespace_in_vim2-recolored.png")。以下のような色付けをしてある。 \]\] **Whitespace**（ホワイトスペース）は、[プログラミング言語](../Page/プログラミング言語.md "wikilink")のひとつであり、またそれを動作させる[インタプリタ](../Page/インタプリタ.md "wikilink")を指している。Whitespaceは[GPLにより配布されている](https://ja.wikipedia.org/wiki/GNU_GPL "wikilink")。実用言語ではない[難解プログラミング言語](https://ja.wikipedia.org/wiki/難解プログラミング言語 "wikilink")のひとつ。

本来 "whitespace" とは「空白」や「余白」を意味する英単語である。多くの一般的なプログラミング言語では空白に相当する文字（[スペース](../Page/スペース.md "wikilink")、[タブ](../Page/タブキー.md "wikilink")、言語によっては[改行も](https://ja.wikipedia.org/wiki/改行コード "wikilink")）は他の言語要素間の区切りとして使われている。しかし、言語 Whitespace においてはプログラムは空白文字だけで構成される（それ以外の文字列はコメント扱いで無視される）。そのため、一見するとプログラムであることすらわからないという珍しい言語である。

## 実例

ソースコードに添付されているサンプルコード ([hworld.ws](http://compsoc.dur.ac.uk/whitespace/hworld.ws)) を見てもらいたい。信じられないかもしれないが、このコードをWhitespaceインタプリタに渡すときちんと動作する。

`$ ./wspace examples/hworld.ws                                                  `
`Hello, world of spaces!`

## 文法

IMP (Instruction Modification Parameter)、コマンド、パラメータの3つ組で命令を表現する。

IMPとしては、以下の物がある

  - \[Space\] スタック操作
  - \[Tab\]\[Space\] 演算
  - \[Tab\]\[Tab\] ヒープアクセス
  - \[LF\] フロー制御
  - \[Tab\]\[LF\] I/O

数値は[二進記数法](https://ja.wikipedia.org/wiki/二進記数法 "wikilink")で表現する。\[Space\]が0で、\[Tab\]が1で、\[LF\]が終端記号である。

### スタック操作

  - \[Space\] 数値：数値をスタックに積む
  - \[LF\]\[Space\]：スタックの一番上を複製する
  - \[Tab\]\[Space\] 数値：スタックのn番目をコピーして一番上に積む
  - \[LF\]\[Tab\]：スタックの1番目と2番目を交換する
  - \[LF\]\[LF\]：スタックの一番上の物を捨てる

### 演算

  - \[Space\]\[Space\]：加算
  - \[Space\]\[Tab\]：引き算
  - \[Space\]\[LF\]：かけ算
  - \[Tab\]\[Space\]：割り算
  - \[Tab\]\[Tab\]：剰余

## 関連項目

  - [Brainfuck](../Page/Brainfuck.md "wikilink")

## 外部リンク

  - [Whitespace 本家サイト](http://compsoc.dur.ac.uk/whitespace/tutorial.html)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:難解プログラミング言語](https://ja.wikipedia.org/wiki/Category:難解プログラミング言語 "wikilink")