> この記事は[KornShell](https://ja.wikipedia.org/wiki/KornShell)から翻訳されています。


**KornShell**（コーンシェル、**`ksh`**）は、[Unixシェル](https://ja.wikipedia.org/wiki/Unixシェル "wikilink")の一種であり、[1980年代](../Page/1980年代.md "wikilink")初期に[ベル研究所](../Page/ベル研究所.md "wikilink")のが開発し、1983年7月14日の[USENIX](https://ja.wikipedia.org/wiki/USENIX "wikilink")年次大会で発表した\[1\]\[2\]。初期にはベル研究所の開発者マイク・ヴィーチとパット・サリヴァンも開発に関わり、それぞれ入力行編集モードの[Emacs](../Page/Emacs.md "wikilink")スタイルと[vi](https://ja.wikipedia.org/wiki/vi "wikilink")スタイルのコードを書いた\[3\]。[Bourne Shellに対して完全上位互換であり](https://ja.wikipedia.org/wiki/Bourne_Shell "wikilink")、コマンド履歴などの[C Shellの機能の多くも取り入れている](../Page/C_Shell.md "wikilink")。彼はベル研究所内のユーザーの要望を受けてkshを開発したと言われている。

## 設計

KornShellは、[POSIX](../Page/POSIX.md "wikilink").2 Shell and Utilities, Command Interpreter (IEEE Std 1003.2-1992) に準拠している。

従来のBourne shellとKornShellとの主な違いは次の通りである。

  - 、、といった[C Shell由来の機能が追加されている](../Page/C_Shell.md "wikilink")。

  - 対話モードで使用する場合、kshはコマンド行を[WYSIWYG](../Page/WYSIWYG.md "wikilink")風の方法で編集することができる。カーソルを上に移動させるキー操作で以前入力したコマンド行を呼び出し、そのコマンド行をラインモードエディタを使うように編集できる。このときのキー操作は[`vi`](https://ja.wikipedia.org/wiki/vi "wikilink")[互換モード](https://ja.wikipedia.org/wiki/互換モード "wikilink")と[`emacs`](https://ja.wikipedia.org/wiki/emacs "wikilink")互換モードと[XEmacs](https://ja.wikipedia.org/wiki/XEmacs "wikilink")互換モードを選択できる。

  - `ksh93` では、[連想配列](../Page/連想配列.md "wikilink")や[浮動小数点数](../Page/浮動小数点数.md "wikilink")演算機能が組み込まれている。

## 歴史

2000年まで、KornShellはAT\&Tの権利保有する[プロプライエタリ・ソフトウェア](../Page/プロプライエタリ・ソフトウェア.md "wikilink")であった。その後AT\&T独自のライセンスの下で[オープンソース](../Page/オープンソース.md "wikilink")となり、2005年の 93q から [Common Public License](https://ja.wikipedia.org/wiki/Common_Public_License "wikilink") での配布となった。KornShellはAT\&T Software Technology (AST) Open Source Software Collectionの一部として入手可能である。ks は当初AT\&Tの商用ライセンスでしか入手できなかったため、オープンソースの代替実装がいくつも生まれた。その中には、パブリックドメインの`pdksh`、`mksh`、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の[`bash`](https://ja.wikipedia.org/wiki/bash "wikilink")、[`zsh`](https://ja.wikipedia.org/wiki/Z_Shell "wikilink")などが含まれる。

最初のKornShellである`ksh88`の機能が[POSIX](../Page/POSIX.md "wikilink").2 Shell and Utilities, Command Interpreter (IEEE Std 1003.2-1992) の元になっている。

ベンダーによっては古い`ksh88`を`/bin/ksh`としていまだに使っているところもあり、独自に拡張している場合もある。`ksh93`は作者であるコーンがいまだに保守している。`ksh93`の後ろにアルファベット1文字をつけてバージョンを表しており、最新版は`ksh93u`である。その1つ前は`ksh93t+`、さらに前は`ksh93t`だった。バグ修正用の中間バージョンはこのバージョン文字列を変更せずにリリースされることもある\[4\]。

デスクトップ用KornShellとされる`dtksh`は[CDEの一部として配布された](https://ja.wikipedia.org/wiki/Common_Desktop_Environment "wikilink")`ksh93`である\[5\]。このバージョンでは[Motifウィジェットのシェルレベルでのマッピングを提供しており](../Page/Motif_\(GUI\).md "wikilink")、[Tcl/Tk](https://ja.wikipedia.org/wiki/Tcl/Tk "wikilink")との対抗を意図していた\[6\]。

最初のKornShellである `ksh88` は、[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")バージョン4からAIXのデフォルトのシェルとされており\[7\]\[8\]、ksh93はそれとは別に用意されている\[9\]。

## 派生

KornShellからの派生ソフトウェアを以下に示す。

  - `dtksh` — `ksh93`からのフォーク。[CDEの一部](https://ja.wikipedia.org/wiki/Common_Desktop_Environment "wikilink")。
  - `tksh` — `ksh93`からのフォーク。[Tk](../Page/Tk_\(ツールキット\).md "wikilink")[ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/ウィジェット・ツールキット "wikilink")へのアクセスを提供。
  - `oksh` — [OpenBSD](../Page/OpenBSD.md "wikilink")版KornShellのフォーク。[GNU/Linuxでのみ動作](https://ja.wikipedia.org/wiki/GNU/Linuxシステム "wikilink")。でデフォルトのシェルとして使われている。
  - `mksh` — KornShellの[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")実装。で開発。
  - `SKsh` — [AmigaOS](https://ja.wikipedia.org/wiki/AmigaOS "wikilink")版KornShell。との相互作用などAmiga固有の機能を提供している。
  - MKS Korn shell — MKS社による商用実装。[Microsoft Windows Services for UNIX](../Page/Microsoft_Windows_Services_for_UNIX.md "wikilink") (SFU) のバージョン2.0までで使われていた。デビッド・コーンによれば、1998年時点のMKS Korn ShellはKornShellと完全互換ではなかった\[10\]\[11\]。SFUバージョン3.0で[マイクロソフト](../Page/マイクロソフト.md "wikilink")はMKS Korn shellの代替として新たにPOSIX.2準拠のシェルを[Interix](https://ja.wikipedia.org/wiki/Interix "wikilink")の一部として導入した\[12\]。
  - デビッド・コーンが開発したはWindows上のUNIX互換パッケージで、KornShellも含まれている\[13\]。

## 脚注

## 参考文献

  -
  - David G. Korn, Charles J. Northrup and Jeffery Korn [The New KornShell—ksh93](http://www.linuxjournal.com/article/1273), [Linux Journal](https://ja.wikipedia.org/wiki/Linux_Journal "wikilink"), Issue 27, July 1996

## 外部リンク

  - [Korn shell home page (AT\&T ksh)](http://www.kornshell.com)
  - [ksh93 man page](http://www.research.att.com/~gsf/man/man1/ksh.html)
  - [ksh88 man page](http://www.research.att.com/sw/download/man/man1/ksh88.html)
  - [Public Domain Korn shell (pdksh)](http://web.cs.mun.ca/~michael/pdksh/)
  - [MirBSD Korn Shell (mksh)](http://www.mirbsd.org/mksh.htm)
  - [mksh man page](http://www.mirbsd.org/htman/i386/man1/mksh.htm) (also as [PDF](http://www.mirbsd.org/MirOS/dist/mir/mksh/mksh.pdf) in DIN A4 [paper size](../Page/紙の寸法.md "wikilink"))

[Category:Unixシェル](https://ja.wikipedia.org/wiki/Category:Unixシェル "wikilink")

1.
2.
3.
4.  <http://www2.research.att.com/sw/download/notes.html>
5.
6.
7.
8.  <http://publib.boulder.ibm.com/infocenter/aix/v6r1/index.jsp?topic=/com.ibm.aix.cmds/doc/aixcmds5/sh.htm>
9.  <http://publib.boulder.ibm.com/infocenter/aix/v6r1/index.jsp?topic=/com.ibm.aix.baseadmn/doc/baseadmndita/korn_shell_enhanced.htm>
10.
11.
12.
13.