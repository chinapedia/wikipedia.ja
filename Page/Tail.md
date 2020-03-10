> この記事は[Tail](https://ja.wikipedia.org/wiki/Tail)から翻訳されています。


**tail**（テール）は[UNIX](../Page/UNIX.md "wikilink")および[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")のシステムで、テキスト[ファイルや](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")[パイプ上のデータの末尾から数行を表示する](../Page/パイプ_\(コンピュータ\).md "wikilink")[プログラムである](../Page/プログラム_\(コンピュータ\).md "wikilink")。[Coreutils](https://ja.wikipedia.org/wiki/GNU_Core_Utilities "wikilink") の一部。

## 文法

このコマンドの[文法](../Page/文法.md "wikilink")は以下の通り。

` tail [options]  `<file_name>

デフォルトでは、`tail`は入力の末尾10行を[標準出力に表示する](https://ja.wikipedia.org/wiki/ファイル記述子 "wikilink")。表示すべき行数はコマンド行オプションで指定でき、表示単位（行、ブロック、バイトなど）も変更できる。以下の例では、*filename*の末尾20行を表示する。

` tail -n 20  `*`filename`*

次の例では、名前が*foo\**で始まる全てのファイルの末尾15バイトを表示する。

` tail -c 15  `*`foo*`*

次の例では、*filename*の先頭から2行目以降を全て表示する。

` tail -n +2  `*`filename`*

古い文法では（Solarisなど）、*filename*の末尾20行の表示や末尾50バイトの表示は次のように記される。

` tail -20  `*`filename`*
` tail -50c  `*`filename`*

しかし、この構文は既に古く、[POSIX](../Page/POSIX.md "wikilink") 1003.1-2001に準拠していない。現在のバージョンでこの構文がサポートされているとしても、他のオプション（たとえば後述の -f）とともに指定することはできない。

## ファイル監視

`tail`には特殊なコマンド行オプション `-f` (follow) があり、ファイルの監視ができる。末尾数行を表示して終了するのではなく、表示後もファイルの監視を続ける。他の[プロセス](../Page/プロセス.md "wikilink")の処理によって新たな行がそのファイルに追加されると、`tail` は表示を更新する。これは特にログファイルを監視するのに便利である。以下のコマンドは*messages*の最後尾10行を表示後、*messages*に新たな行が追加される度にそれを表示する。

`tail -f /var/adm/messages`

監視中の`tail`を停止させるには、CTRL-Cを押下する。このコマンドは`&`を付けてバックグラウンドで実行することもできる（[ジョブコントロール](https://ja.wikipedia.org/wiki/ジョブコントロール "wikilink")）。

また、類似オプションとして`-F` (follow) が設けられているものも存在する。`-f`はコマンド起動時に開いたファイルを監視するが、`-F`は開いたファイルの[inode](https://ja.wikipedia.org/wiki/inode "wikilink")を監視し、inode番号の変化を検出すると、ファイルを開き直す。以下のコマンドは前例同様*messages*の最後尾10行を表示後、*messages*に新たな行が追加される度にそれを表示する。

`tail -F /var/adm/messages`

前者との違いは、/var/adm/messagesがローテートされると、前者ではローテートに伴う移動先のファイル（例えばmessages.1など）を監視しつづけるのに対し、後者では/var/adm/messagesを監視しつづける点である。

## 類似のプログラム

  - [CCZE](http://freshmeat.net/redir/ccze/33590/url_homepage/ccze.html) - tailに似ているが、表示がカラーになっている。
  - [pctail](http://sourceforge.net/projects/pctail/) - CCZEに似た、[Python](../Page/Python.md "wikilink")で書かれた色つきTail。
  - [root-tail](http://www.goof.com/pcg/marc/root-tail.html) - [X Window Systemのルートウィンドウに出力を表示する](../Page/X_Window_System.md "wikilink")。
  - [Inotail](http://distanz.ch/inotail/) - 本来の tail は新たな表示すべきデータがあるかどうかを毎秒チェックする。Inotailは[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")にある[inotify](https://ja.wikipedia.org/wiki/inotify "wikilink")インタフェースを使うので、本当に何らかの新たなデータがあるときだけチェックする。
  - [MultiTail](http://www.vanheusden.com/multitail/) - ログファイルをカラーで表示するだけでなく、マージ、フィルター、スクロールバック、サブウィンドウへの分割などが可能。tail、[sed](../Page/Sed_\(コンピュータ\).md "wikilink")、[watch](https://ja.wikipedia.org/wiki/watch "wikilink")、CCZE/pctail、[grep](https://ja.wikipedia.org/wiki/grep "wikilink")、[diff](https://ja.wikipedia.org/wiki/diff "wikilink")、[Beeper](http://cosoleto.free.fr/beeper/)などの組合せである。

## 関連項目

  - [head](https://ja.wikipedia.org/wiki/head "wikilink")

## 外部リンク

  - [tail (1)](https://linuxjm.osdn.jp/html/gnumaniak/man1/tail.1.html) マニュアル JM Project
  - [FreeBSD documentation for tail](https://www.freebsd.org/cgi/man.cgi?query=tail&apropos=0&sektion=0&manpath=FreeBSD+5.3-RELEASE+and+Ports&format=html)（英語）
  - [tail(1)](https://docs.oracle.com/cd/E19683-01/817-7410/6mmnue1dd/index.html) man page（SunOS リファレンスマニュアル）
  - [tail(1)](https://nixdoc.net/man-pages/HP-UX/man1/tail.1.html) man page（HP-UX リファレンス）

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")