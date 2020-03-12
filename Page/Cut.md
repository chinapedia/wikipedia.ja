> この記事は[Cut](https://ja.wikipedia.org/wiki/Cut)から翻訳されています。


**cut**（カット）は、[UNIX](../Page/UNIX.md "wikilink")の[コマンドライン](https://ja.wikipedia.org/wiki/コマンドライン "wikilink")ユーティリティの1つであり、入力（通常、ファイル）の各行の一部を抜き出すのに使われる。

行の抜き出す部分の指定には、[バイト単位](../Page/バイト_\(情報\).md "wikilink")（`-b`）、[文字単位](../Page/キャラクタ_\(コンピュータ\).md "wikilink")（`-c`）、[区切り文字](https://ja.wikipedia.org/wiki/区切り文字 "wikilink")（`-d` — デフォルトでは[タブ文字](../Page/タブキー.md "wikilink")）で区切られたフィールド単位（`-f`）などがある。範囲そのものの指定をする引数の形式には、`N`、`N-M`、`N-`（N番目から行の終端まで）、`-M`（行の先頭から M 番目まで）がある。

## 使用例

**a** という名前のファイルに以下のような行があるとする。

`foo:bar:baz:qux:quux`
`one:two:three:four:five:six:seven`
`alpha:beta:gamma:delta:epsilon:zeta:eta:teta:iota:kappa:lambda:mu`

各行の4番目の文字から10番目の文字を抜き出すには、以下のように指定する。

`% cut -c 4-10 a`

このコマンドの出力結果は以下のようになる。

`:bar:ba`
`:two:th`
`ha:beta`

[コロン文字をフィールドの区切り文字](../Page/コロン_\(記号\).md "wikilink")（区切り記号、デリミタ）として、各行の5番目のフィールド以降を全て出力するには、以下のように指定する。

`% cut -d : -f 5- a`

このコマンドの出力結果は以下のようになる。

`quux`
`five:six:seven`
`epsilon:zeta:eta:teta:iota:kappa:lambda:mu`

## 外部リンク

  - [cut (1)](https://linuxjm.osdn.jp/html/gnumaniak/man1/cut.1.html) マニュアル（JM Project）
  - [cut(1)](https://docs.oracle.com/cd/E19455-01/816-3518/6m9ptvquc/index.html) man page（SunOS リファレンスマニュアル）
  - [cut(1)](https://nixdoc.net/man-pages/HP-UX/man1/cut.1.html) man page（HP-UX リファレンス）

[sv:Lista över golftermer\#Cut](https://ja.wikipedia.org/wiki/sv:Lista_över_golftermer#Cut "wikilink")

[Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink")