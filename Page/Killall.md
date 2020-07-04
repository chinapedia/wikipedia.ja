> この記事は[Killall](https://ja.wikipedia.org/wiki/Killall)から翻訳されています。


**killall**（キルオール）は [UNIX](../Page/UNIX.md "wikilink") 系 OS で利用できる[コマンドラインユーティリティである](../Page/コマンドラインインタプリタ.md "wikilink")。このコマンドには大変異なる2種類の実装がある。

  - （[Solaris](../Page/Solaris.md "wikilink") を含む）正統な [UNIX System V](../Page/UNIX_System_V.md "wikilink") や（[killall5](https://ja.wikipedia.org/wiki/killall5 "wikilink") のような）[Linux](../Page/Linux.md "wikilink") の [sysvinit](ftp://ftp.cistron.nl/pub/people/miquels/sysvinit/) ツールが与える実装では `killall` は特に危険なコマンドであり、ユーザが強制終了できるプロセスを全て強制終了する。そのため root で動作させることによって効果的にシステムを終了することができる。
  - [psmisc](http://psmisc.sourceforge.net/) ツールによって与えられる実装における振る舞いは [pkill](https://ja.wikipedia.org/wiki/pkill "wikilink") や [skill](https://ja.wikipedia.org/wiki/skill "wikilink") コマンドに似たものとなっており、コマンドラインで指定されたプロセスを強制終了させる。

`killall` は [kill](https://ja.wikipedia.org/wiki/kill "wikilink") プログラムのように[シグナルを送る](../Page/シグナル_\(Unix\).md "wikilink")。

## 使用例

すべてのプロセスを強制終了させる（UNIX System V バージョン）

**`killall`**

すべてのシグナルを列挙する（Linux バージョン）

**`killall``   ``-l`**

dd プロセスに [USR1](https://ja.wikipedia.org/wiki/USR1 "wikilink") をおくる（Linux バージョン）

**`killall``   ``-s``   ``USR1``   ``dd`**

dd プロセスを強制終了する（Linux バージョン）

**`killall``   ``-9``   ``dd`**

`killall` はデフォルトで [SIGTERM](https://ja.wikipedia.org/wiki/SIGTERM "wikilink") を送る。しかし数字のオプションではプロセスに送るシグナルを指定することができる。上記の場合、コマンドはプロセスにシグナル 9 ([SIGKILL](https://ja.wikipedia.org/wiki/SIGKILL "wikilink")) を送る。

## 関連項目

  - [シグナル](../Page/シグナル_\(Unix\).md "wikilink")
  - [kill](https://ja.wikipedia.org/wiki/kill "wikilink")
  - [pidof](https://ja.wikipedia.org/wiki/pidof "wikilink")
  - [pkill](https://ja.wikipedia.org/wiki/pkill "wikilink")

## 外部リンク

  - [MANPAGE of killall](https://linuxjm.osdn.jp/html/psmisc/man1/killall.1.html) JM Project
  - [killall(1M)](https://www.unix.com/man-page/sunos/1m/killall/) Solaris 10 Reference Manual Collection（英語）
  - [killall(1M)](https://www.unix.com/man-page/hpux/1M/killall/) man page（HP-UX リファレンス）

[de:Kill (Unix)\#killall](https://ja.wikipedia.org/wiki/de:Kill_\(Unix\)#killall "wikilink")

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")