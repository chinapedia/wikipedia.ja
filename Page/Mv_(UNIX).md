> この記事は[Mv \(UNIX\)](https://ja.wikipedia.org/wiki/Mv_\(UNIX\))から翻訳されています。


**mv**（エムブイ）は[POSIX](../Page/POSIX.md "wikilink")およびSingle UNIX Specificationで規定されているコマンドである。mvは「move」の略であり、ファイルやディレクトリの移動、名前の変更をするコマンドである。

## 構文

mv \[options\] source destination
mv \[options\] source... directory

## POSIXオプション

  - \-f 上書きの確認の問い合わせをしない。
  - \-i destination がすでに存在する場合、上書きの確認の問い合わせをする（-fと-iが両方とも指定された場合、後から指定された方のオプションが有効になる）。

## 例

|                           |                                            |
| ------------------------- | ------------------------------------------ |
| `mv myfile mynewfilename` | 'mynewfilename'がディレクトリでないとしてファイル名が変更される。   |
| `mv myfile /myfile`       | 'myfile'をカレントディレクトリからルートディレクトリに移動する。       |
| `mv myfile dir/myfile`    | 'myfile'をカレントディレクトリのdir配下に移動する。            |
| `mv myfile dir/`          | 前述と同様の意味となる。ファイル名は暗黙的におなじと扱われる。            |
| `mv myfile dir/myfile2`   | 'myfile'をdir/に移動し、さらにファイル名を'myfile2'に変更する。 |
| `mv foo bar baz dir/`     | 複数のファイルをdir/に移動する。                         |
| `mv --help`               | コマンドの構文について簡潔なヘルプを表示する。（GNU の版のみ）          |
| `man mv`                  | 'mv'のオンライン・マニュアルを表示する。                     |
|                           |                                            |

## \-で始まるファイル名の変更

mvコマンドの多くの実装では、`-` で始まるファイル名を引数に指定する目的で、オプション終了を意味する特殊オプション(`--` または `-`)が用意されている。例えば前者の場合、ファイル `-` を `f` に変える指定は `mv -- - f` とすれば良い。

ただし、これら特殊オプションが存在しなくとも、パス名を付加した `mv ./- f` とすることで回避可能である。

これらは **[cp (UNIX)](https://ja.wikipedia.org/wiki/cp_\(UNIX\) "wikilink")** や **[rm (UNIX)](https://ja.wikipedia.org/wiki/rm_\(UNIX\) "wikilink")** でも同様のことが言える。

## 外部リンク

  - [Manpage of MV](https://linuxjm.osdn.jp/html/GNU_fileutils/man1/mv.1.html) (JM Project)
  - [mv](https://www.freebsd.org/cgi/man.cgi?query=mv&apropos=0&sektion=0&manpath=FreeBSD+5.3-RELEASE+and+Ports&format=html) man page（FreeBSD版、英語）
  - [mv](https://man.openbsd.org/mv) man page（OpenBSD版、英語）
  - [mv](https://www.gnu.org/software/coreutils/manual/coreutils.html#mv-invocation) ドキュメント（GNU版、英語）
  - [mv(1)](https://docs.oracle.com/cd/E19455-01/816-3518/6m9ptvr2o/index.html) man page（SunOS リファレンスマニュアル）
  - [mv(1)](https://nixdoc.net/man-pages/HP-UX/man1/mv.1.html) man page（HP-UX リファレンス）

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")