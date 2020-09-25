> この記事は[Grep](https://ja.wikipedia.org/wiki/Grep)から翻訳されています。


**`grep`**（グレップ、グレプ）は、および[{{lang](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")におけるコマンド。[テキストファイル](../Page/テキストファイル.md "wikilink")中から、[正規表現](../Page/正規表現.md "wikilink")に一致する行を検索して出力する。

## 概要

`grep` の名の由来は、[ラインエディタ](https://ja.wikipedia.org/wiki/ラインエディタ "wikilink")[edのコマンド](https://ja.wikipedia.org/wiki/ed_\(テキストエディタ\) "wikilink") `g/re/p` である。その意味するところは「global regular expression print(ファイル全体から/正規表現に一致する行を/表示する)」で略号になっている\[1\]。

姉妹コマンドとして、正規表現ではなくリテラル（即値文字列）のみを扱う高速な `fgrep`\[2\]、拡張正規表現が使える `egrep`\[3\] がある。 では `fgrep`、`egrep` を旧形式としていて、それぞれ `grep -F`、`grep -E` を使うことを標準としている。Linux Standard Baseでも指定コマンドになっている\[4\]。

## 使用法

`grep` コマンドの基本的な使い方は

`grep `<var>`オプション`</var>` `<var>`パターン`</var>` `<var>`ファイル`</var>

である。

<var>ファイル</var>は複数指定することができ、また省略して標準入力から検索することもできる。

<var>オプション</var>には次のようなものがある：

  - `-i` : [アルファベット](https://ja.wikipedia.org/wiki/アルファベット "wikilink")の大文字小文字の区別をしない。
  - `-o`：パターンに一致した箇所**のみ**出力する。
  - `-v` : パターンに**一致しない**行を出力する。
  - `-r` : *ファイル*としてディレクトリを指定し、その中の全てのファイルと、再帰的に下位ディレクトリに対して検索する。
  - `-q`：何も出力しない。
  - `-E` : 拡張正規表現を使用する。`egrep` コマンドと同じ動作をする。
  - `-F` : 正規表現ではなくリテラルを使用する。`fgrep` コマンドと同じ動作をする。

## 移植

テキストから文字列を検索するプログラムとして、有志により、 や  用に多数移植されている。また、テキストから文字列を検索するプログラムのことを  と呼ばれることもある。

## 参考文献

  -
## 脚注

## 関連項目

  - [フィルタ](../Page/フィルタ_\(ソフトウェア\).md "wikilink")
  - [`find`](https://ja.wikipedia.org/wiki/find_\(UNIX\) "wikilink")
  - [`agrep`](https://ja.wikipedia.org/wiki/agrep "wikilink")

## 外部リンク

  - [](https://www.gnu.org/software/grep/)（英語）
  - [`grep`(1)](https://linuxjm.osdn.jp/html/GNU_grep/man1/grep.1.html) -  JMプロジェクトによる日本語のマニュアルページ
  - [`grep`(1)](https://docs.oracle.com/cd/E19683-01/816-3986/6ma7sa297/index.html) - （ リファレンス・マニュアル）
  - [`grep`(1)](https://nixdoc.net/man-pages/HP-UX/grep.1.html) - （HP-UX リファレンス）

[Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink")

1.
2.   または
3.
4.  Linux Standard Base <https://refspecs.linuxfoundation.org/lsb.shtml>