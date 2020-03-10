> この記事は[SNOBOL](https://ja.wikipedia.org/wiki/SNOBOL)から翻訳されています。


**SNOBOL**は、[米国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[AT\&T](../Page/AT&T.md "wikilink")[ベル研究所](../Page/ベル研究所.md "wikilink")のグリスウォルド（[Ralph Griswold](https://ja.wikipedia.org/wiki/:en:Ralph_Griswold "wikilink")）らにより開発された[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。

## 概要

[テキスト](../Page/テキスト.md "wikilink")処理を目的として[1960年代](../Page/1960年代.md "wikilink")に作られた。[欧州を中心に](../Page/ヨーロッパ.md "wikilink")、[言語](../Page/言語.md "wikilink")処理のツールとして普及し、。名前「SNOBOL」は「文字列指向の記号言語」を意味する英語「」に由来するとされることがあるが（[バクロニム](../Page/バクロニム.md "wikilink")）、実際には英語の「[snowball's chance in hell](https://ja.wikipedia.org/wiki/wikt:en:snowball's_chance_in_hell "wikilink")」（地獄に雪玉がある可能性、まったく見込みがないこと）という言い回しに由来する\[1\]。

SNOBOLの初版は1962年に作られた。最新版のSNOBOL4は1966年以降に開発された\[2\]。

言語の特徴としては table と呼ばれる機能を実装していることである、これは後に[連想配列](../Page/連想配列.md "wikilink")として発達し多くの言語で採用されるに至っている。ゆえに SNOBOL は連想配列の祖といえる。また記述された文字列のパターンを認識し、分割することができる。この機能により文字列の解析を得意としている。

GriswoldはSNOBOLの後継として[Icon言語](https://ja.wikipedia.org/wiki/Icon言語 "wikilink")を開発している。

## 基本的な構文

SNOBOL の構文は以下のようになっている（ラベルと次に処理する行のラベルは省略可能である）。

```
 ラベル   式  :(次に処理する行のラベル)
```

SNOBOLは[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")が提唱される以前の言語であるため、ループは基本的に無条件分岐（[goto文](https://ja.wikipedia.org/wiki/goto文 "wikilink")）で行われる。全ての式は実行後、次に処理する行のラベルを選択でき、省略時は次の行が実行される。[標準入出力はINPUT](../Page/入出力.md "wikilink")/OUTPUTという変数に代入処理を行うことで実行される。[if文](https://ja.wikipedia.org/wiki/if文 "wikilink")に相当する物は無く、代わりに式を実行後、成功か失敗かで次に処理する行を変更することができる。これは具体的には

```
    LINE = INPUT :S(LABEL1) F(LABEL2)
```

のような場合（これは標準入力から1行読み込み変数 LINEに代入している）、その処理が成功した場合は LABEL1の行の処理へ、失敗した場合は LABEL2の行の処理へ遷移することを表している。

SNOBOLでは基本的な集合があらかじめキーワードとして定義されている。例えば小文字の集合("abcdefghijklmnopqrstuvwxyz")は \&LCASE というキーワードで表す事ができる、同様に大文字の集合である \&UCASEというキーワードもある。

### 連想配列

SNOBOL の特徴としてテーブル型という連想配列の原型のデータ構造の存在がある。これは

```
    変数名 = TABLE()
```

という形で定義し、*変数名\[文字列\]* というように使用することができる。

### パターンマッチング

SNOBOLでは[パターンマッチング](../Page/パターンマッチング.md "wikilink")の処理が存在する。これは以下のように行われる

```
    WORD = "abc123defABCgh"
* パターンの定義
    PAT = SPAN(&LCASE) . ITEM

* パターンマッチング
    WORD PAT =
* "abc" と表示される
    OUTPUT = ITEM

    WORD PAT =
* "def" と表示される
    OUTPUT = ITEM
```

変数 PAT は \&LCASE（アルファベットの小文字）のパターンである。上記処理では[文字列](../Page/文字列.md "wikilink")の変数 WORD とパターンマッチングを行い、PATに無いパターンが来たら、そこまでの結果を ITEMに格納する。次に同様の処理を始めるときは ITEM 以降の文字列がパターンマッチングされる。

## サンプルコード

次のサンプルコードは標準入力されたファイルの内容を読み込み、各単語毎にカウントして出力するプログラムの一例である。

``` snobol
    &TRIM = 1
    WORD = "'-" '0123456789' &LCASE
    PAT = SPAN(WORD) . ITEM
    DATA = TABLE()
READ    LINE = REPLACE(INPUT, &UCASE, &LCASE) :F(DONE)
DIV LINE PAT = :F(READ)
    DATA[ITEM] = DATA[ITEM] + 1 :(DIV)
DONE    A = CONVERT(DATA, 'ARRAY') :F(EMPTY)
    I = 0
PRINT   I = I + 1
    OUTPUT = A[I,1] '=' A[I,2] :S(PRINT) F(END)
EMPTY   OUTPUT = 'This file have no words'
END
```

## 脚注

## 関連項目

  - [Icon](../Page/Icon.md "wikilink")

## 外部リンク

  - [A Snobol4 Tutorial](http://burks.bton.ac.uk/burks/language/snobol/catspaw/tutorial/contents.htm)
  - [SNOBOL4.ORG](http://www.snobol4.org/csnobol4/) - SNOBOL の配布ページ

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")

1.
2.