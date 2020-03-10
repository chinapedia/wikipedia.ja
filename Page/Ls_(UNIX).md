> この記事は[Ls \(UNIX\)](https://ja.wikipedia.org/wiki/Ls_\(UNIX\))から翻訳されています。


[サムネイル](https://ja.wikipedia.org/wiki/ファイル:Ls_example.png "wikilink") **`ls`**（エルエス）は[POSIX](../Page/POSIX.md "wikilink")および[Single UNIX Specificationで規定されている](../Page/Single_UNIX_Specification.md "wikilink")[コマンドである](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")。[ファイルの一覧を表示するコマンドである](../Page/ファイル_\(コンピュータ\).md "wikilink")。

## 歴史

`ls`は[AT\&T](../Page/AT&T.md "wikilink") [UNIX](../Page/UNIX.md "wikilink")の最初のバージョンから存在していた。その名称は、[Multics](https://ja.wikipedia.org/wiki/Multics "wikilink")に存在した類似のコマンドから継承された。現在使われている主な実装には、[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")によるものと[FreeBSD](../Page/FreeBSD.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")、[Darwinなどの](../Page/Darwin_\(オペレーティングシステム\).md "wikilink")[BSD](../Page/BSD.md "wikilink")系システムで用いられているものの2つがある。どちらも[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であり、[オープンソース](../Page/オープンソース.md "wikilink")である。

## 振る舞い

[Unix系](../Page/Unix系.md "wikilink")のシステムには、現在ユーザが作業を行っている[ファイルシステム](../Page/ファイルシステム.md "wikilink")上の場所を表す「[カレントディレクトリ](https://ja.wikipedia.org/wiki/カレントディレクトリ "wikilink")」という概念がある。`ls`は引数を伴わずに起動された場合、カレントディレクトリの[ファイルの一覧を表示する](../Page/ファイル_\(コンピュータ\).md "wikilink")。引数にカレントディレクトリ以外の[ディレクトリ](../Page/ディレクトリ.md "wikilink")を指定した場合、そのディレクトリのファイル一覧を表示する。また、ディレクトリやファイルのリストを引数として指定することもでき、その場合はすべての指定されたファイルと、ディレクトリ内のファイルの一覧を表示する。

そのディレクトリ自身を示す「`.`」や親ディレクトリの「`..`」をはじめ、各種設定ファイル等のファイル名の慣例である「`.`」で始まるファイル名をもつファイル（ドットファイル）は標準では表示されず、表示するには明示的に`-a`オプションを指定する必要がある。

オプションが指定されなかった場合、`ls`はファイル名のみを表示する。しかし、この形式では[ファイルタイプ](https://ja.wikipedia.org/wiki/UNIXファイルタイプ "wikilink")、[パーミッション](../Page/ファイルパーミッション.md "wikilink")、サイズなどの情報がわからない。`ls`には表示形式を変更するオプションが多く存在するが、もっとも一般的なものは次に挙げたものである。

  - `-l` :長い形式で表示する。ファイルタイプ、パーミッション、[ハードリンク](https://ja.wikipedia.org/wiki/ハードリンク "wikilink")の数、所有者、グループ、サイズ、日付、ファイル名。
  - `-F` :ファイルの性質を表す文字をファイル名の末尾に付加する。例えば「`*`」は実行可能ファイル、「`/`」はディレクトリを表し、通常のファイルは何も付加されない。
  - `-a` :「`.`」で始まるファイル名のものを含め、ディレクトリ内のすべてのファイルを表示する。
  - `-R` :サブディレクトリ内のファイルを再帰的に表示する。従って、`ls -R /`とするとシステムに存在するすべてのファイルを表示する。

一部の環境では、`--color`（[GNU](../Page/GNUプロジェクト.md "wikilink") `ls`）または`-G`（[FreeBSD](../Page/FreeBSD.md "wikilink") `ls`）オプションを指定するとファイルタイプによって異なる色で表示される。表示する色を決定する際、FreeBSDの`ls`ではファイルタイプとパーミッションのみで決定されるが、GNUの`ls`ではそれに加え拡張子によっても色を変えることができる。

このようなオプションを指定した場合、`ls`の出力は次のようになる。

<span style="background:#000000; color:#c0c0c0; line-height:1.0em;">` brw-r--r--    1 unixguy staff 64,  64 Jan 27 05:52 `<span style="color:yellow     ">`block         `</span>
` crw-r--r--    1 unixguy staff 64, 255 Jan 26 13:57 `<span style="color:yellow     ">`character     `</span>
` -rw-r--r--    1 unixguy staff     290 Jan 26 14:08 `<span style="color:red        ">`compressed.gz `</span>
` -rw-r--r--    1 unixguy staff  331836 Jan 26 14:06 `<span style="color:purple     ">`data.ppm      `</span>
` drwxrwx--x    2 unixguy staff      48 Jan 26 11:28 `<span style="color:blue       ">`dir           `</span>
` -rwxrwx--x    1 unixguy staff      29 Jan 26 14:03 `<span style="color:green      ">`executable    `</span>
` prw-r--r--    1 unixguy staff       0 Jan 26 11:50 `<span style="color:lightyellow">`fifo          `</span>
` lrwxrwxrwx    1 unixguy staff       3 Jan 26 11:44 `<span style="color:lightblue  ">`link`</span>` -> `<span style="color:blue">`dir   `</span>
` -rw-rw----    1 unixguy staff     217 Jan 26 14:08 regularfile   `</span>

`ls`には他にも多くのオプションが存在し、それらは[manページ](https://ja.wikipedia.org/wiki/manページ "wikilink")で調べることができる。

## 使用例

次の例は2つの異なる引数を与えられた時の`ls`コマンドの出力の違いを示している。

`$ pwd`
`/home/fred`
`$ ls -l`
`drwxr--r--   1 fred  editors   4096  drafts`
`-rw-r--r--   1 fred  editors  30405  edition-32`
`-r-xr-xr-x   1 fred  fred      8460  edit`
`$ ls -F`
`drafts/ `
`edition-32 `
`edit*`

ここでユーザ`fred`の[ホームディレクトリ](../Page/ホームディレクトリ.md "wikilink")には`drafts`というディレクトリ、`edition-32`という通常の[ファイル](../Page/ファイル_\(コンピュータ\).md "wikilink")、`edit`という実行可能ファイルが存在することがわかる。`ls`はユーザ、グループ、世界（それ以外）がファイルに対しどのようなパーミッション（権限）を持っているかを表現するために特別な記法を使っている。

パーミッション部分の最初の文字はファイルの種別を表している。

| 文字        | 意味                                                              |
| --------- | --------------------------------------------------------------- |
| `-`       | 通常のファイル                                                         |
| `b`       | [ブロックデバイス](https://ja.wikipedia.org/wiki/ブロックデバイス "wikilink")   |
| `c`       | [キャラクタデバイス](https://ja.wikipedia.org/wiki/キャラクタデバイス "wikilink") |
| `d`       | ディレクトリ                                                          |
| `l`       | シンボリックリンク                                                       |
| `p`または`=` | 名前つきパイプまたはFIFO                                                  |
| `s`       | ソケット                                                            |
|           |                                                                 |

残りの部分は3文字ごとのブロックに分けられ、`r`、`w`、`x`はそれぞれ読み込み、書き込み、実行の権限が存在することを意味する。最初のブロックは所有ユーザの、2つめのブロックは所属しているグループの、3つめのブロックはその他の場合のパーミッションを表している。上の例では、ユーザ`fred`は`edition-32`を読み書きできるが、実行はできない。`editors`グループのメンバーはそれ以外のユーザと同様、`edition-32`を読めるが、書き込んだり実行したりすることはできない。 詳しくは[ファイルパーミッションを参照のこと](https://ja.wikipedia.org/wiki/ファイルパーミッション#UNIX系のパーミッション "wikilink")。

## 関連項目

  - [sl (UNIX)](https://ja.wikipedia.org/wiki/sl_\(UNIX\) "wikilink")

## 外部リンク

  - [ls](https://www.gnu.org/software/coreutils/manual/html_node/ls-invocation.html#ls-invocation) ドキュメント（[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")版、英語）

[Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink") [Category:1969年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1969年のソフトウェア "wikilink")