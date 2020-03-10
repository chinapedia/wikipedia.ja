> この記事は[Uniq](https://ja.wikipedia.org/wiki/Uniq)から翻訳されています。


**uniq**（ユニーク）は[UNIX](../Page/UNIX.md "wikilink")およびUNIX系システムで、テキストをファイルを入力として、隣接する同じ内容の行を1つの行だけ残して他を削除した出力をするユーティリティである。[フィルタの一種であり](../Page/フィルタ_\(ソフトウェア\).md "wikilink")、[sortの出力を入力とするような形で使われることが多い](https://ja.wikipedia.org/wiki/sort_\(UNIX\) "wikilink")。また、逆にダブっている行だけを出力することもできるし（`-d` オプション）、各行の出現回数を付与することもできる（`-c` オプション）。

例えば、あるファイルの異なる内容の行を各行の出現頻度順にソートして一覧したい場合、次のようになる。

  -
    `sort file | uniq -c | sort -n`

`uniq` はこのように[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")などでの[パイプの一部として使われることがある](../Page/パイプ_\(コンピュータ\).md "wikilink")。

## コマンド行オプション

  - `-u` : 元のファイルで繰り返し出現しない行だけを出力する。
  - `-d` : 元のファイルで繰り返し出現した行だけを出力する。
  - `-c` : 出力の各行の先頭に出現回数を挿入した形式で出力する。これが指定されると `-u` と `-d` は無視される。
  - `-i` : 大文字/小文字を区別しないで行を比較する。（GNU 拡張）
  - `-s` *n* : 各行の先頭 *n* 文字を無視する。
  - `-w` *n* : 各行の先頭 *n* 文字を比較し、それ以降を無視する。

## 外部リンク

  - [uniq(1)](https://linuxjm.osdn.jp/html/gnumaniak/man1/uniq.1.html) JM Project
  - [uniq(1)](https://docs.oracle.com/cd/E19253-01/819-1210/uniq-1/index.html) man page（SunOS リファレンスマニュアル）
  - [uniq(1)](https://nixdoc.net/man-pages/HP-UX/man1/uniq.1.html) man page（HP-UX リファレンス）

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")