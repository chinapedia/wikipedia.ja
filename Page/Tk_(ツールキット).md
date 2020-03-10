> この記事は[Tk \(\)](https://ja.wikipedia.org/wiki/Tk_\(\))から翻訳されています。


**Tk**は、[GUIを開発するための](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、[オープンソース](../Page/オープンソース.md "wikilink")の、[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")の[ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/ウィジェット・ツールキット "wikilink")である。デスクトップ・アプリケーションを開発するために通常必要な、ボタン、メニュー、テキスト、フレーム、ラベルなどのウィジェットを提供する。カリフォルニア大学バークレー校の John Ousterhout によって、スクリプト言語 [Tcl](https://ja.wikipedia.org/wiki/Tcl "wikilink")の拡張として開発された。Tk は "*Tool Kit*" の略である。[Unix系](../Page/Unix系.md "wikilink")OS、[Macintosh](../Page/Macintosh.md "wikilink")、[Microsoft Windowsなどに移植されている](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

## 機能

もともとの Tk では、各プラットフォームの標準的なものとは異なるルック・ アンド・フィールであったが、Tk 8　からは、ネイティブなルック・アンド・フィールを提供するようになった（例えば、メニューとボタンはそのプラットフォームの「ネイティブな」ソフトウェアの作法で表示される）。さらに、外部とのドラッグ・アンド・ドロップ、非長方形のウィンドウ、ネイティブのウィジェットなどのいくつかの拡張が提供された。Tk 8.5 からは、Tk 8.4で試験的に提供されていた、Tk Tile と呼ばれる新しいテーマ・エンジンが、リリースに取り込まれた。これは、Ttk Widget と呼ばれるもので、テーマを変更し GUI の見栄えを切り替えることができる。 Tk は、[Unicode](../Page/Unicode.md "wikilink")の[基本多言語面](https://ja.wikipedia.org/wiki/基本多言語面 "wikilink") (BMP) をサポートするが、32-bitの Unicode を扱うための拡張はまだされていない。[Unix系](../Page/Unix系.md "wikilink")のシステムでは、Tk 8.4 以前は、ビットマップフォントを使用していたが、Tk 8.5 では、アンチエイリアスフォントを使用することができる。

Tcl では、Tcl Shell (tclsh) という[コマンドライン・インタプリタ](https://ja.wikipedia.org/wiki/コマンドライン・インタプリタ "wikilink")を使用するが、Tk は wish (Windowing Shell) というコマンドライン・インタプリタから簡単に呼び出すことができる。

## Tcl以外の言語バインディング

[Ada](../Page/Ada.md "wikilink")（TASH\[1\] と呼ばれる）、[Perl](../Page/Perl.md "wikilink")、[Python](../Page/Python.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink") および [Common Lisp](https://ja.wikipedia.org/wiki/Common_Lisp "wikilink") を含むいくつかのほかの[言語バインディング](https://ja.wikipedia.org/wiki/言語バインディング "wikilink")が存在する。

[Perl](../Page/Perl.md "wikilink")から、Tk を動かす方法はいくつかある。Tcl::Tk と Tkx の Perl モジュール、これらは両方とも、Tcl を用いて Tk にアクセスするためのブリッジである。Perl/Tk は、Perl からのネイティブな Tk の機構へのアクセスを提供する。Python と Ruby は、Tk へのブリッジとして、Tcl を使うバインディングを使用する。

## 脚注

<div class="references-small">

<references />

</div>

## 参考文献

## 外部リンク

  - [Tcl and Tk website](http://www.tcl.tk/)

  - [Active Tcl - Tk manual](http://aspn.activestate.com/ASPN/docs/ActiveTcl/8.5/tcl/tk_contents.htm)

  -
## 関連項目

  - [Tcl/Tk](https://ja.wikipedia.org/wiki/Tcl/Tk "wikilink")
  - [Tkinter](https://ja.wikipedia.org/wiki/Tkinter "wikilink") - Python 用の言語バインディング
  - [GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink") - The GIMP Toolkit
  - [Qt](https://ja.wikipedia.org/wiki/Qt "wikilink")
  - [wxWidgets](https://ja.wikipedia.org/wiki/wxWidgets "wikilink")

[Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/Category:ウィジェット・ツールキット "wikilink")

1.  [TASH](http://tcladashell.sourceforge.net/)