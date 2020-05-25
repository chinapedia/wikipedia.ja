> この記事は[Pwd](https://ja.wikipedia.org/wiki/Pwd)から翻訳されています。


[サムネイル](https://ja.wikipedia.org/wiki/ファイル:Pwdkommando.png "wikilink")  **pwd** (ピーダブリューディー、**p**ositioning **w**orking **d**irectory\[1\]) は、[カレントディレクトリ](https://ja.wikipedia.org/wiki/カレントディレクトリ "wikilink")（ポジショニングワーキングディレクトリ）のフルパスを出力するコマンドである。

## 概要

一般に[Unix系](../Page/Unix系.md "wikilink")などの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) では、プロセスは何らかの[カレントディレクトリ](https://ja.wikipedia.org/wiki/カレントディレクトリ "wikilink")に「居る」。pwdは、自分自身のプロセスのカレントディレクトリのフルパス（absolute pathname）を、それを取得するシステムコールgetcwd(2)を利用するなどして取得し、標準出力に出力する。

このコマンドは[cdコマンドなどと違い](https://ja.wikipedia.org/wiki/cd_\(UNIX\) "wikilink")、組込みコマンドにする必要性は全く無い（理由は、プロセスというものを理解していれば、わかるだろう）。しかし、[sh](../Page/Bourne_Shell.md "wikilink") や [Bash](../Page/Bash.md "wikilink") などの一部の[シェル](../Page/シェル.md "wikilink")では、組込みコマンドに含まれている。

[MS-DOS](../Page/MS-DOS.md "wikilink")や[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")のシェル（[COMMAND.COM](../Page/COMMAND.COM.md "wikilink")や[cmd.exe](https://ja.wikipedia.org/wiki/cmd.exe "wikilink")）では、cd コマンドを引数なしで実行すると、ほぼ同様の機能となっている。

使用例:

`$ pwd`
`/home/foobar`

## オプション

POSIXでは、pwdコマンドには下記のようなオプションがある\[2\]。（シェル組込み版があるシェルを使っている場合、これを使うには一般に何らかの方法で、外部コマンド版を実行するようにしなければならない）

  - `-L`（`--logical`）:論理的なカレントディレクトリ名を出力する。
  - `-P`（`--physical`）:物理的なカレントディレクトリ名を出力する（＝もし現在のディレクトリがシンボリックリンクであった場合、リンク先のディレクトリ名を出力する）。

## 出典

<references />

## 外部リンク

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")

1.
2.  <http://pubs.opengroup.org/onlinepubs/9699919799/utilities/pwd.html>