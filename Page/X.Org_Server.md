> この記事は[X.Org Server](https://ja.wikipedia.org/wiki/X.Org_Server)から翻訳されています。


**X.Org Server**（X.Org Foundation Open Source Public Implementation of X11）とは、[X Window Systemの公式](../Page/X_Window_System.md "wikilink")[リファレンス実装](../Page/リファレンス実装.md "wikilink")である。[オープンソース](../Page/オープンソース.md "wikilink")であり、かつ[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。 プロジェクト運営組織は [X.Org Foundation](../Page/X.Org_Foundation.md "wikilink") であり、[freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink") の援助を受けている。

## 歴史

X.Org Foundation は、Xの標準仕様を監督し公式リファレンス実装を行った開発者と、[XFree86](../Page/XFree86.md "wikilink") の開発者が合流した集団である。

X11R6.7.0（X.Org Server の最初のバージョン）は、[XFree86](../Page/XFree86.md "wikilink") 4.4 RC2 からの分岐であった。分岐の直接の理由は、XFree86 4.4 最終リリース版における新しいライセンス条件に関する見解の不一致であるが、関係者の見解の相違は分岐以前に明らかだった。分岐が行われたとき、共通のコードベースである X11R6.6 に対して修正が行われた。かつて XFree86 の開発を行っていた多くの開発者が X.Org Server プロジェクトに参加した。

X11R6.9.0/X11R7.0.0 のリリースでは第一に、[GNU Autotools](../Page/Autotools.md "wikilink") に基づいたモジュール化されたビルドシステムを追加した。6.9.0 までは古い [imake](https://ja.wikipedia.org/wiki/imake "wikilink") ビルドシステムを使っていたのに対して、7.0.0 では同じコードベースに autotools を使っている。モジュール化に伴い、X11バイナリのインストールパスは `/usr/X11R6` から `/usr` に変更されている。

## 採用例

X.Org Server は、[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")や[BSD](../Page/BSD.md "wikilink")系や[Solaris](../Page/Solaris.md "wikilink")（かつてはSPARC系では独自の[Xsun](https://ja.wikipedia.org/wiki/Xsun "wikilink")を使用していた）など、[UNIX](../Page/UNIX.md "wikilink")系オペレーティングシステムのほぼ全てで採用されている。また、X.Org Server は、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") 向けでは [Cygwin](../Page/Cygwin.md "wikilink") 併用で [Cygwin/X](https://ja.wikipedia.org/wiki/Cygwin/X "wikilink") (XWin) として、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") 向けは [X11.app](../Page/X11.app.md "wikilink") (XQuartz) として公開されている。その他、[Xming](https://ja.wikipedia.org/wiki/Xming "wikilink") などオープンソースやプロプライエタリなどで派生したものが多数ある。

## リリース履歴

[X Window System リリース履歴を参照](https://ja.wikipedia.org/wiki/X_Window_System#リリース履歴 "wikilink")。

## 外部リンク

  - [X.Org Wiki](http://www.x.org/)
  - [man page](http://www.x.org/releases/current/doc/man/man7/X.7.xhtml)
  - [xorg/xserver - X server](http://cgit.freedesktop.org/xorg/xserver/)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Freedesktop.org](https://ja.wikipedia.org/wiki/Category:Freedesktop.org "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink")