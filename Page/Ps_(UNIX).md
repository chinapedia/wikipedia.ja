> この記事は[Ps \(UNIX\)](https://ja.wikipedia.org/wiki/Ps_\(UNIX\))から翻訳されています。


ほとんどの [UNIX](../Page/UNIX.md "wikilink") 系 OS で **ps**（ピーエス）は現在動作している[プロセス](../Page/プロセス.md "wikilink")を表示する[タスクマネージャー](https://ja.wikipedia.org/wiki/タスクマネージャー "wikilink")である。

ps にはたくさんのオプションがある。[UNIX や POSIX](../Page/Single_UNIX_Specification.md "wikilink") 標準をサポートする[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")では、ps はよく **-ef** オプションを付けて使われる。ここで、"-e" はすべて (**e**very) のプロセスを選択し、 "-f" は完全な (**f**ull) 出力フォーマットを選ぶ。このようなシステムでよく使われる他のオプションには "-l" で、長い (**l**ong) 出力フォーマットを指定する。

[BSD](../Page/BSD.md "wikilink") から派生したほとんどのシステムでは POSIX や UNIX 標準オプションをとることができない。これは歴史的なオプションの衝突によるもので、例えば "e" または "-e" オプションをつけると[環境変数](../Page/環境変数.md "wikilink")が表示される。そのようなシステムでは、ps は非標準のオプション **aux** をつけてよく使われる。ここで "a" は他のユーザの端末を含む[端末](../Page/端末.md "wikilink")上のすべてのプロセスをリストし、"u" は個々のプロセスの制御ユーザなどを追加し、"x" は制御端末をもたないすべてのプロセスをリストする。これらのオプションを使うときに互換性をできるだけ高めるには、"aux" の前に "-" をつけるべきではない。

[Linux](../Page/Linux.md "wikilink") の ps は両方のオプションに対応している。[Solaris](../Page/Solaris.md "wikilink") の /usr/bin/ps は "-ef" に対応し、/usr/ucb/ps は "aux" に対応する。

[top](https://ja.wikipedia.org/wiki/top_\(UNIX\) "wikilink") という他の UNIX ユーティリティは実行しているプロセスをリアルタイムで表示する。

## 例

`tux ~ # ps`
`  PID TTY          TIME CMD`
` 7431 pts/0    00:00:00 su`
` 7434 pts/0    00:00:00 bash`
`18585 pts/0    00:00:00 ps`

ps コマンドは、あるプロセスについて[プロセス id](../Page/プロセス識別子.md "wikilink") のような情報を得るために [grep](https://ja.wikipedia.org/wiki/grep "wikilink") コマンドと組み合わせて使うこともできる。

`tux ~ # ps -A | grep firefox-bin`
`11778 ?        02:40:08 firefox-bin`
`11779 ?        00:00:00 firefox-bin`

## 関連項目

  - [top](https://ja.wikipedia.org/wiki/top_\(UNIX\) "wikilink")
  - [pstree](https://ja.wikipedia.org/wiki/pstree_\(UNIX\) "wikilink")
  - [pgrep](https://ja.wikipedia.org/wiki/pgrep "wikilink")

## 外部リンク

  - [Manpage of PS](https://linuxjm.osdn.jp/html/procps/man1/ps.1.html) JM Project
  - [The ps Command](http://www.linfo.org/ps.html) - by The Linux Information Project (LINFO)（英語）
  - [ps(1)](https://docs.oracle.com/cd/E19455-01/816-3518/6m9ptvr3l/index.html) man page（SunOS リファレンスマニュアル）
  - [ps(1)](https://nixdoc.net/man-pages/HP-UX/man1/ps.1.html) man page（HP-UX リファレンス）

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")