> この記事は[Xargs](https://ja.wikipedia.org/wiki/Xargs)から翻訳されています。


**xargs**（エックスアーグズ）は、[UNIX](../Page/UNIX.md "wikilink") 系[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")に用意されているコマンドで、標準入力を読み込み、それを引数として指定したコマンドを実行する。

__TOC__

## 概要

xargsは、改行等で区切られた標準入力を読み込み、空白で区切られた１行の文字列へ加工し、それを引数として指定したコマンドへ渡して実行させる。

`$ seq 8 | xargs echo '-'`
`- 1 2 3 4 5 6 7 8`

ただし、この１行の文字列がシステムで許容される長さを超える場合は、xargsはその文字列を許容の長さになるよう最少の複数に分割し、コマンドを複数回に分けて実行させる。これにより、コマンドが許容の長さを超える引数のリストを受け付けない問題 \[1\]を回避できる。

例えば、以下のようなコマンドは

`rm /path/*`
``rm `find /path -type f` ``

*/path* に多すぎるファイルがあれば「引数リストが長すぎます」というエラーメッセージとともに *rm* コマンドは失敗する。しかし *rm \`find /path -type f\`* と機能的には同等な以下のコマンドは失敗しない。

`find /path -type f -print0 | xargs -0 rm`

この例では、*find* は *xargs* への入力としてファイル名の長いリストを出力している。そして、*xargs* はこのリストをいくつかの部分リストに分割して、それぞれ一回ずつ *rm* を呼んでいる。上の方法は機能的に同等な以下の方法より効率的である。これはすべてのファイルに対して一回ずつ *rm* を呼ぶことになる。

`find /path -type f -exec rm '{}' \;`

しかし、最近の *find* では *xargs* を使った方法と同じことができる。

`find /path -type f -exec rm '{}' +`

xargs はしばしばたくさんの[シェル](../Page/シェル.md "wikilink")の[バッククォート](https://ja.wikipedia.org/wiki/バッククォート "wikilink")機能と同じ機能を持っている。しかし、より柔軟で、入力に空白や特殊文字を含む場合にはしばしばより安全でもある。[find](https://ja.wikipedia.org/wiki/find "wikilink")、[locate](https://ja.wikipedia.org/wiki/locate "wikilink") や [grep](https://ja.wikipedia.org/wiki/grep "wikilink") のような長いリストを出力するコマンドとともによく使われる。

## 動作例

`find . -name "*.foo" | xargs grep bar`

は下と同じように動作する。

`` grep bar `find . -name "*.foo"` ``

上のコマンドではシングルクォート (') ではなくバッククォート (\`) を使っていることに注意しなければならない。上のコマンドは現在の[ディレクトリ](../Page/ディレクトリ.md "wikilink")とサブディレクトリ内の`.foo` で終わっているファイルから[文字列](../Page/文字列.md "wikilink") `bar` を検索する。ファイル名に[改行コード](../Page/改行コード.md "wikilink")を含む空白文字が含まれていた場合、このコマンドは期待した通りには動作しない。この制限を避けるには、[ヌル文字](https://ja.wikipedia.org/wiki/ヌル文字 "wikilink")を使ってファイル名を分割する find や xargs の GNU 拡張を使って

`find . -name "*.foo" -print0 | xargs -0 grep bar`

とすればよい。

`find . -name "*.foo" -print0 | xargs -0 -t -r vi`

も上と同じ検索条件である。しかし、各ファイル名に対して [vi](https://ja.wikipedia.org/wiki/vi "wikilink") を起動する。-t はそれを実行する前に標準エラー出力にコマンドを表示する。-r は入力を受け取らなかったときにコマンドを実行しないということを xargs に伝える GNU 拡張である。

`find . -name "*.foo" -print0 | xargs -0 -I {} mv {} /tmp/trash`

では xargs に {} のシンボルを引数に置き換えるということを伝えるために -I を使っている。ただし、この {} は一個の引数に置き換えられ、\*.foo にマッチするファイル一つ一つに対して mv コマンドが実行されるので、効率的とはいえない。

## 脚注

## 関連項目

  - [GNU parallel](https://ja.wikipedia.org/wiki/GNU_parallel "wikilink")

## 外部リンク

  - [Manpage of XARGS](https://linuxjm.osdn.jp/html/GNU_findutils/man1/xargs.1.html) GNU 版。JM Project
  - [xargs(1)](https://docs.oracle.com/cd/E19683-01/817-3838/6mjdft877/index.html) man page（SunOS リファレンスマニュアル）

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")

1.  [GNU Core Utilities FAQ](http://www.gnu.org/software/coreutils/faq/coreutils-faq.html#Argument-list-too-long)