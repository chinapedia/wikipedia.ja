> この記事は[Curses](https://ja.wikipedia.org/wiki/Curses)から翻訳されています。


**curses**（カーシス、カーズィス）は[UNIX系](https://ja.wikipedia.org/wiki/UNIX系 "wikilink")システムでの[端末制御](https://ja.wikipedia.org/wiki/ビデオ表示端末 "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")である。[テキストユーザインタフェース](https://ja.wikipedia.org/wiki/テキストユーザインタフェース "wikilink")（TUI）アプリケーションを作成するのに使われる。名称は“[cursor](https://ja.wikipedia.org/wiki/カーソル "wikilink") optimization”に由来する。文字のみを表示する端末（例えば[VT100](https://ja.wikipedia.org/wiki/VT100 "wikilink")）を表示に使うアプリケーションが画面を管理する機能を集めた[ライブラリ](../Page/ライブラリ.md "wikilink")である\[1\]。

## 概要

cursesの[APIの解説書はいくつかある](../Page/アプリケーションプログラミングインタフェース.md "wikilink")\[2\]。最も一般的な実装では、数千に及ぶ様々な端末の機能を示したデータベースを利用している。端末データベースではなく専用[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")を採用している実装としては PDCurses があるが、そのような例は少ない。ほとんどの実装では[terminfo](https://ja.wikipedia.org/wiki/terminfo "wikilink")を使っており、一部は[termcap](https://ja.wikipedia.org/wiki/termcap "wikilink")を使っている。古い端末でもほとんどの場合動作可能であり、単純な点が長所である。[ビットマップ画像](https://ja.wikipedia.org/wiki/ビットマップ画像 "wikilink")や様々な[フォント](../Page/フォント.md "wikilink")を必要としないアプリケーションでは、[X Window System](../Page/X_Window_System.md "wikilink") を使うよりも curses を使った実装の方が単純で高速である。

curses を使用すると、プログラマは特定の端末装置を考慮せずに文字ベースのアプリケーションを書くことができる。cursesライブラリは、実行時に使用している端末装置を判別して適切に制御コードを送ることができる。curses では、実画面を1つ以上のウィンドウをマップしたものとしてモデル化する。各ウィンドウは文字の行列であり、プログラマは必要なウィンドウを実際に表示させたいように内容を設定して、curses に対して画面の更新を指示する。curses は内容の更新状況を調べ、実際に画面上で書き換える必要があるところだけを書き換えるような制御文字列を生成する。つまり、プログラマは画面にどう表示したいのかを文字行列で示し、curses がそれを実際に表示する作業を受け持つ。

## 歴史

が開発し、[BSD](../Page/BSD.md "wikilink") UNIX の一部としてリリースし、[ローグ](../Page/ローグ.md "wikilink")というゲームなどで使用された\[3\]\[4\]\[5\]。

"curses" という名称は *cursor optimization* に由来する\[6\]。また、ときおり[vi](https://ja.wikipedia.org/wiki/vi "wikilink")[エディタで](https://ja.wikipedia.org/wiki/ソースコードエディタ "wikilink") curses が使われているという趣旨の解説が記載されている場合があるが、実際にはその逆で、[vi](https://ja.wikipedia.org/wiki/vi "wikilink")のカーソル移動のコードを参考にして curses が書かれた\[7\]。

当初、[termcap](https://ja.wikipedia.org/wiki/termcap "wikilink")ライブラリを使って実装された。数年後、[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")で[vi](https://ja.wikipedia.org/wiki/vi "wikilink")とtermcapを改良していたが[AT\&T](../Page/AT&T.md "wikilink")に行き、[terminfo](https://ja.wikipedia.org/wiki/terminfo "wikilink")を使った別のバージョンを作り、それが [UNIX System III](../Page/UNIX_System_III.md "wikilink") と [UNIX System V](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink") に採用された。後者はライセンス上の制限があるため、BSDとAT\&Tそれぞれのバージョンは独立に開発されている。AT\&T版ではterminfoを使っただけでなく、以下のような改良も行われている。

  - ハイライト表示（ボールド表示、アンダーライン表示） - BSD版では単に「強調」として一種類しかサポートしていなかった。
  - 枠線の描画 - BSD版ではこの部分が貧弱だった。
  - 色付きの表示 - BSD版では全く対応していない。

AT\&Tでの curses 開発は1990年代中ごろに終り、同じころ[X/Open](https://ja.wikipedia.org/wiki/X/Open "wikilink")が curses のAPIを定義した\[8\]。その後も[ncurses](https://ja.wikipedia.org/wiki/ncurses "wikilink")との開発は継続されている。BSD版 curses は[NetBSD](../Page/NetBSD.md "wikilink")で保守されており、多バイト文字対応、termcapからterminfoへの移行などが行われている。

### pcurses と PDcurses

[ncurses](https://ja.wikipedia.org/wiki/ncurses "wikilink") は curses の代替として [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink") 向けに[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")で作られたライブラリであり、その後、[POSIX](../Page/POSIX.md "wikilink")準拠のUNIXに移植されていった。PDCurses （Public Domain Curses）はUNIX以外の [DOS](../Page/MS-DOS.md "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")など向けに作られた curses とほぼ同じ機能を提供するライブラリである。[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")のゲームなどで、Linux では ncurses、Windows では PDCurses を使っているものがある。

1990年代には、4.4BSD でBSD版 curses にハイライト表示方法を複数サポートするなどの改良を施した。しかしこちらはあまり普及しなかった。それとは別に、AT\&T版を真似た別のバージョンの開発が始まっていた。これには少なくとも2つの実装がある。**pcurses**（1982年開始）と**PDCurses**（Public Domain curses、1987年開始）である。

### ncurses

**ncurses** (new curses) は pcurses から派生したもので、1993年にバージョン1.8.1から始まった\[9\]。ncurses は今では最も普及している実装であり、これに刺激されて[NetBSD](../Page/NetBSD.md "wikilink")プロジェクトでのBSD版 curses の開発などが進められた\[10\]\[11\]。

## 移植性

ncurses ライブラリは当初[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")を対象としていたが、その後[POSIX](../Page/POSIX.md "wikilink")準拠の各種[Unix系](../Page/Unix系.md "wikilink")システムに移植された。PDCurses はAPIや機能は ncurses と全く同一ではないが、[DOS](../Page/MS-DOS.md "wikilink")、[Win32](https://ja.wikipedia.org/wiki/Windows_API "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")のコンソール端末や[X11などで動作する](../Page/X_Window_System.md "wikilink")。この両者間での移植は難しくはない。例えば[ローグライクゲーム](../Page/ローグライクゲーム.md "wikilink")の**はLinux上でncursesを使って書かれたが、後にDOS上でPDCursesを使って移植された\[12\]。

## curses を使ったソフトウェア

[Tin_console.png](https://ja.wikipedia.org/wiki/File:Tin_console.png "fig:Tin_console.png") [Jack-curses-screen.gif](https://ja.wikipedia.org/wiki/File:Jack-curses-screen.gif "fig:Jack-curses-screen.gif")

cursesは、テキストのみの表示デバイス（PCのコンソールモード、ANSI端末、[telnet](https://ja.wikipedia.org/wiki/telnet "wikilink")や[SSHのクライアントなど](../Page/Secure_Shell.md "wikilink")）で[GUI風の機能を提供するよう設計されている](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。

cursesを使ったプログラムは、テキストのみの表示デバイスでよくある[コマンドラインインタフェース](../Page/キャラクタユーザインタフェース.md "wikilink") (CLI) ではなく、一般的なGUIに似たユーザインタフェースを採用することが多く、[テキストボックス](../Page/テキストボックス.md "wikilink")やスクロール可能なリストといった[ウィジェットを使う](https://ja.wikipedia.org/wiki/ウィジェット_\(GUI\) "wikilink")。それによってCLIよりも使いやすいものになり、同時にテキストのみを表示する各種デバイスでも利用可能である。また、GUIを使うよりも少ないリソースで動作可能である。

[SVR4では](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink") curses を利用した言語 FMLI を導入し、それを使ったテキストのみのユーザインタフェース FACE を実装した。FACEはシステム管理用インタフェースに使われた。FMLIはSolarisでも使われていた。

curses を使ったソフトウェアが必ずGUI風の[テキストユーザインタフェース](https://ja.wikipedia.org/wiki/テキストユーザインタフェース "wikilink")を採用するとは限らない。例えば[vi](https://ja.wikipedia.org/wiki/vi "wikilink")エディタは[TUI](https://ja.wikipedia.org/wiki/テキストユーザインタフェース "wikilink")/GUI的なインタフェースではない。

## 脚注

## 外部リンク

  - [NCURSES - Manual Pages](http://invisible-island.net/ncurses/man/)
  - [Curses tutorial](http://heather.cs.ucdavis.edu/~matloff/UnixAndC/CLanguage/Curses.pdf) ([PDF](../Page/Portable_Document_Format.md "wikilink") 形式)
  - [Public Domain Curses](http://pdcurses.sourceforge.net/)
  - [Interface for Rexx programmers](http://rexxcurses.sourceforge.net/)
  - [Tcl Toolkit](http://www.ch-werner.de/ck/)
  - [X/Open Curses](http://www.opengroup.org/onlinepubs/007908799/cursesix.html)
  - [NetBSD Curses main manual page](http://netbsd.gw.com/cgi-bin/man-cgi?curses+3+NetBSD-current)

[Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink")

1.
2.  John Strang, *Programming with curses*, O'Reilly, ISBN 0-937175-02-1
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.