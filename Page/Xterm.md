> この記事は[Xterm](https://ja.wikipedia.org/wiki/Xterm)から翻訳されています。


**xterm**は、[X Window Systemの標準的な](../Page/X_Window_System.md "wikilink")[端末エミュレータ](https://ja.wikipedia.org/wiki/端末エミュレータ "wikilink")である。ユーザは一つの[ディスプレイの中に複数のxtermを表示し](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")、同時に作業を行うことができる。それぞれのxtermは、xtermの中で動作する[プロセス](../Page/プロセス.md "wikilink")に対し、独立した入出力を提供する（通常、このプロセスとは[Unixシェル](https://ja.wikipedia.org/wiki/Unixシェル "wikilink")である）。

## 概要

xtermは、X Window Systemに先立って開発されていた。もともとxtermは、[1984年](../Page/1984年.md "wikilink")夏、VAXStation 100 (VS100) のスタンドアロン・端末エミュレータとしてMark Vandevoordeによって開発された。ところが、スタンドアロンで動作するよりもXの一部となった方が便利であることがすぐにわかり、X向けに変更された。

現在、xtermから派生した多くの端末エミュレータが存在する。

xtermには、通常メニューバーが存在しない。ユーザは、Controlキーを押しながら左クリック、中クリック、右クリックをすることで3つの異なるメニューにアクセスすることができる。コンパイル時にツールバーを組み込むことも可能だが、これは前述のものと同じメニューを呼び出す。

## 機能

### 端末エミュレーション

初期のバージョンでは、VT102とTektronix 4014をエミュレートしていた\[1\]。後のバージョンでは、次のような、DECや他の端末のためのコントロールシークエンスが追加されている。

  - VT220:パッチ24にて追加\[2\]。
  - VT320:パッチ24にて追加\[3\]。
  - VT420:DECSTRはパッチ34にて追加\[4\]。
  - VT520:公式にはエミュレートされていないが、VT520の機能の一部は実装されている\[5\]。

### プロトコル

端末コントロール機能は以下のものなどがサポートされている。

  - [ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink") X3.64
  - Difgital Quipment Corporation VTのファミリ
      - VT52
      - 初期のバージョンでは、VT102とTektronix
      - VT220
  - Tektronixのファミリ
      - Tektronix 4014

加えて、商業的に用いられるターミナルマシンで使われるプロトコルのほかに、xtermは下のような若干のプロトコルを追加している。

  - マウスのトラッキング: ボタン4とボタン5に対するサポートはパッチ120で追加\[6\]。
  - 16色ターミナルプロトコル: パッチ39で追加\[7\]。
  - 256色ターミナルプロトコル: パッチ111で追加\[8\]。
  - 88色ターミナルプロトコル: パッチ115で追加\[9\]。
  - カスタムのカラーパレット: パレットのエントリの[RGB](../Page/RGB.md "wikilink")値を指定する機能がパッチ111で追加されている\[10\]。

## 脚注

## 関連項目

  - [端末エミュレータ](https://ja.wikipedia.org/wiki/端末エミュレータ "wikilink")
  - [VT100](../Page/VT100.md "wikilink")

## 外部リンク

  - [xterm](http://freshmeat.net/projects/xterm/) on Freshmeat

[Category:端末エミュレータ](https://ja.wikipedia.org/wiki/Category:端末エミュレータ "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink")

1.
2.
3.
4.
5.
6.  [Patch \#120 - 1999/10/28 - XFree86 3.9.16c](http://invisible-island.net/xterm/xterm.log.html#xterm_120)
7.  [Patch \#39 - 1997/5/24 - XFree86 3.2Xl](http://invisible-island.net/xterm/xterm.log.html#xterm_39)
8.  [title=Patch \#111 - 1999/7/10 - XFree86 3.9Pw](http://invisible-island.net/xterm/xterm.log.html#xterm_111)
9.  [Patch \#115 - 1999/9/18 - XFree86 3.9.16](http://invisible-island.net/xterm/xterm.log.html#xterm_115)
10.