> この記事は[Tr \(UNIX\)](https://ja.wikipedia.org/wiki/Tr_\(UNIX\))から翻訳されています。


**`tr`**（ティーアール）は[UNIX](../Page/UNIX.md "wikilink")およびUNIX系システムのコマンドである。名称は ***tr**anslate* または ***tr**ansliterate* の略。

`tr` は標準入力から読み込んで標準出力に出力する。パラメータとして2つの文字集合を指定し、一方の文字集合に含まれる文字が出現する度に、もう一方の文字集合の同じ位置にある文字に置換して出力する。

## 使用例

次の例では、アルファベットをアルファベット順で7つ後の文字に全て置換する（*a* は *h* に。[カエサル暗号](https://ja.wikipedia.org/wiki/カエサル暗号 "wikilink")の変種）。

`$ echo cheer | tr abcdefghijklmnopqrstuvwxyz hijklmnopqrstuvwxyzabcdefg`
**`jolly`**

使用している**tr**がもし[POSIX](../Page/POSIX.md "wikilink")準拠ならば、最後の2つの語は単に`a-z h-za-g`と書くことができる。

特殊な**tr**においてのみ、"\\n" を "\\r\\n" に置換するには、以下のようにすればよい。

`$ tr -A '\12' '\15\12' < input1  > output1`
`$ tr -A '^M' '\15\12'  < output1 > output2`

ただし、すべての**tr**が`-A`オプションに対応しているわけではないことに注意してほしい。また、単一引用符の代わりに二重引用符を使うことはできない。[シェル](../Page/シェル.md "wikilink")が逆スラッシュを解釈してしまうからだ。ここで、\\nや\\12や^Jは、それぞれ[エスケープ文字](../Page/エスケープ文字.md "wikilink")、[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")8進、カレット表記を使った改行文字を示している。\\rや\\15や^Mは、復帰文字である。背景については[改行コード](https://ja.wikipedia.org/wiki/改行コード "wikilink")の項を参照。

次の例では、アルファベットをアルファベット順で1つ前の文字に全て置換する（*a* は *z* に）。

`$ echo "ibm 9000" >computer.txt`
`$ tr a-z za-y <computer.txt`
**`hal``   ``9000`**

[POSIX](../Page/POSIX.md "wikilink")互換でない古い **tr** では、文字の範囲指定を角括弧で囲む必要があり、[シェル](../Page/シェル.md "wikilink")が解釈するのを防ぐためにさらに引用符で囲む必要がある。

`$ tr "[a-z]" "z[a-y]" <computer.txt`

どちらのバージョンが呼び出されるか不明な場合、この例では範囲指定ではなく全文字を並べて示す必要がある（`tr abcdefghijklmnopqrstuvwxyz zabcdefghijklmnopqrstuvwxy`）。使い方によっては古い記法で済む場合もある。例えば、[ROT13](https://ja.wikipedia.org/wiki/ROT13 "wikilink") は `tr "[A-M][N-Z][a-m][n-z]" "[N-Z][A-M][n-z][a-m]"` となり、最近のバージョンでも問題なく動作する。これは、角括弧が2つの文字集合の同じ位置にあるため、置換されても変化しないためであって、POSIX の **tr** が角括弧を解釈しないことには変わりない。

[Ruby](../Page/Ruby.md "wikilink") と [Perl](../Page/Perl.md "wikilink") にも **tr** 演算子（メソッド）があり、同様の働きをする。例えば、日本語を扱えるPerlを使うことにより、以下のPerlスクリプトは平仮名と片仮名とを交換する。（ただし、「ヴ」「ヵ」「ヶ」を除く。）

``` perl
tr/ぁ-んァ-ン/ァ-ンぁ-ん/;
tr/ゝゞヽヾ/ヽヾゝゞ/;
```

## 外部リンク

  - [tr(1)](https://linuxjm.osdn.jp/html/gnumaniak/man1/tr.1.html) JM Project
  - [tr(1)](https://docs.oracle.com/cd/E19455-01/816-3518/6m9ptvr5i/index.html) man page（SunOS リファレンスマニュアル）
  - [tr(1)](https://nixdoc.net/man-pages/HP-UX/man1/tr.1.html) man page（HP-UX リファレンス）

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")