> この記事は[GTK \(\)](https://ja.wikipedia.org/wiki/GTK_\(\))から翻訳されています。


[Free_and_open-source-software_display_servers_and_UI_toolkits.svg](https://ja.wikipedia.org/wiki/File:Free_and_open-source-software_display_servers_and_UI_toolkits.svg "fig:Free_and_open-source-software_display_servers_and_UI_toolkits.svg")\]\]

**GTK** (以前は **GTK+**\[1\], **The GIMP Toolkit**) は、[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")の[ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/ウィジェット・ツールキット "wikilink")（GUIツールキット）である。当初は、[GIMP](../Page/GIMP.md "wikilink")の実装のために開発され、現在は、[GNOME](../Page/GNOME.md "wikilink")[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")のツールキット等として広く利用されている。

GTKは[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の一部であり、[GNU LGPLの元で開発されている](../Page/GNU_Lesser_General_Public_License.md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")な[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。

GTKアプリケーションは、GNOMEに限らず[KDE](../Page/KDE.md "wikilink")などのGTKベースでない[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")でも動作する。GNOMEライブラリを使用することにより、GNOMEデスクトップ環境のさまざまな機能を使用したアプリケーションを開発することができるが、GTKだけでアプリケーションを構成することも可能。

GTKは、主に[FreeBSD](../Page/FreeBSD.md "wikilink")や[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")といった[オープンソース](../Page/オープンソース.md "wikilink")のOS向けのソフトウェアに多く利用されているが、[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")にも[移植されている](https://ja.wikipedia.org/wiki/移植_\(ソフトウェア\) "wikilink")。

2019年、「GTK」に改名することが決まった\[2\]。

## プログラミング言語

[Qt](../Page/Qt.md "wikilink")と違ってGTKは[C言語](../Page/C言語.md "wikilink")を使うが、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")のパラダイムで普通デザインする。また、公式に[C++](../Page/C++.md "wikilink") ([gtkmm](https://ja.wikipedia.org/wiki/gtkmm "wikilink"))、[Perl](../Page/Perl.md "wikilink") (gtk2-perl)、[Python](../Page/Python.md "wikilink") ([PyGTK](https://ja.wikipedia.org/wiki/PyGTK "wikilink"))、[C\#](../Page/C_Sharp.md "wikilink")(Gtk\#)、[Java](https://ja.wikipedia.org/wiki/Java "wikilink") (Java-GNOME)、[JavaScript](../Page/JavaScript.md "wikilink")、[Vala](https://ja.wikipedia.org/wiki/Vala "wikilink")、非公式に[Fortran](https://ja.wikipedia.org/wiki/Fortran "wikilink") (gtk-fortran)、[Ruby](../Page/Ruby.md "wikilink") (Ruby/Gtk2)、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink") (PHP-GTK)、[Pascal](../Page/Pascal.md "wikilink")、[Lua](../Page/Lua.md "wikilink")、[Haskell](../Page/Haskell.md "wikilink")、[FreeBASIC](../Page/FreeBASIC.md "wikilink")といった言語でもバインディングを用いることにより開発が可能である\[3\]。

## テーマ（ルックアンドフィール）

ユーザーがGTKの見た目を変えられる。これはテーマエンジンを切り替えることで実現されていて、多くのテーマが提供されている\[4\]。これらのテーマの中には[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")の[Aquaや](../Page/Aqua_\(コンピュータ\).md "wikilink")[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Motifや](../Page/Motif_\(GUI\).md "wikilink")[Qt](../Page/Qt.md "wikilink")等の他の有名なツールキットやプラットホームをまねた見た目を提供するのもある。

## 歴史

### Linux/Unix

GTKは当初、[Motif](https://ja.wikipedia.org/wiki/Motif "wikilink")の代替として、[GIMP](../Page/GIMP.md "wikilink")のために設計され、用いられた。Peter MattisはMotifに失望し、彼自身の[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")[ツールキット](https://ja.wikipedia.org/wiki/ツールキット "wikilink")、GIMP toolkitが書かれた。これはGIMP 0.60のリリースでMotifを置き換えることに成功した\[5\]。最終的にGTKは書き直され、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")となり、GTK+に名前が変更された\[6\]。これはGIMPの0.99リリースで最初に使われた。GTKはその後、[GNOME Foundationによってメンテナンス対応がなされ](../Page/GNOME_Foundation.md "wikilink")[GNOME](../Page/GNOME.md "wikilink")[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")で使われるようになった。

GTK 2.0.0リリースシリーズは、[Pango](https://ja.wikipedia.org/wiki/Pango "wikilink")を使った改善されたテキストのレンダリング新しいテーマエンジンやさらに柔軟な[API](https://ja.wikipedia.org/wiki/API "wikilink")などを含んでいた。バージョン2.8から、GTK 2はベクターグラフィックスの描画のためのライブラリとして[Cairo](https://ja.wikipedia.org/wiki/Cairo "wikilink")に依存するようになっている。

GTK 3.0.0は、修正されたインプットデバイスの取り扱いや、[CSS](../Page/CSS.md "wikilink")のような構文で書かれたテーマのサポート、他の開かれているGTKアプリケーションからの情報受け取り機能などを含んでいる。

### macOS

[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")では、[Quartz](../Page/Quartz.md "wikilink")バックエンド\[7\]のGTKを利用することができる。

### Windows

  - GTK 2.24.10と3.6.4のあと、インストーラー付きのWindows向け開発はGNOMEによって中止された。MSYS2 on Windowsをインストールするのが、実際にGTKを使うためにはよい手段である\[8\]。
  - GTK 2.24.10と3.6.4は[インターネット](../Page/インターネット.md "wikilink")上で利用可能だが、バグが多く実際のバージョンよりも限られたものとなっている\[9\]。
  - [64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")版Windows向けのバージョンはTom Schoonjansによって準備され、2.24.32と3.22.30を利用することができる\[10\]。

## GTK2

**GTK2**とはGTK1の次のバージョンのGTKとして開発されたツールキットである。[Pango](https://ja.wikipedia.org/wiki/Pango "wikilink")による多言語テキスト出力、新テーマエンジン、(ATK)による[アクセシビリティ](https://ja.wikipedia.org/wiki/アクセシビリティ "wikilink")サポートの向上、[UTF-8](../Page/UTF-8.md "wikilink")による[Unicode](../Page/Unicode.md "wikilink")環境への移行などがされている。GTK2はGTK1と互換性がないので、GTK1用のプログラムをGTK2環境で動かすにはGTK2用に[ソースコード](../Page/ソースコード.md "wikilink")等を修正する必要がある。いくつかのアプリケーションは軽量さや組み込みアプリケーションに適しているなどの理由からオリジナルバージョンを使いつづけGTK1のままで使われているのもある。

[インプットメソッド](../Page/インプットメソッド.md "wikilink")が必要な日本語などの言語のためにimmoduleという[プラグイン](../Page/プラグイン.md "wikilink")スタイルの[フレームワーク](https://ja.wikipedia.org/wiki/フレームワーク "wikilink")が用意されており、[XIMや](https://ja.wikipedia.org/wiki/X_Input_Method "wikilink")[IIIMF](https://ja.wikipedia.org/wiki/IIIMF "wikilink")を利用するための仕組みも、それぞれこのimmoduleの1つとして実装されている。

### GTK2を利用したソフトウェア

[thumb](https://ja.wikipedia.org/wiki/ファイル:gimp2-2.png "wikilink")

  - [GIMP](../Page/GIMP.md "wikilink")
  - [Inkscape](https://ja.wikipedia.org/wiki/Inkscape "wikilink")
  - [Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")
  - [Mozilla Thunderbird](../Page/Mozilla_Thunderbird.md "wikilink")
  - [Sylpheed](https://ja.wikipedia.org/wiki/Sylpheed "wikilink") (メールソフト)
  - [Web](https://ja.wikipedia.org/wiki/Web_\(ウェブブラウザ\) "wikilink") (ウェブブラウザ)
  - [風博士](https://ja.wikipedia.org/wiki/風博士_\(ウェブブラウザ\) "wikilink") (ウェブブラウザ)
  - [mikutter](https://ja.wikipedia.org/wiki/mikutter "wikilink") (Twitterクライアント)
  - 各種[GNOME 2アプリケーション](../Page/GNOME.md "wikilink") - GNOME環境はGTKをベースにしており、GNOMEアプリケーションはツールキットとしてGTKを使用している。

### GTK2 immodule のさまざまな実装

  - im-canna - [かんなのimmodule](../Page/Canna.md "wikilink")
  - im-freewnn - [FreeWnnのimmodule](https://ja.wikipedia.org/wiki/Wnn "wikilink")
  - im-perl - [Perl](../Page/Perl.md "wikilink")で入力メソッドを記述するためのimmodule
  - im-euro - 'euro'をユーロ記号に変換して、欧米人に入力メソッドをわかりやすく説明するためのimmodule
  - im-ja - [im-canna](https://ja.wikipedia.org/wiki/im-canna "wikilink")ベースに、手書き入力などさまざまな日本語入力に対応
  - im-ime - [Windows専用のimmodule](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。Windows上のIMEでのインライン日本語入力に対応
  - im-xim - [XIMのimmodule](https://ja.wikipedia.org/wiki/X_Input_Method "wikilink")
  - im-iiim - [IIIMF](https://ja.wikipedia.org/wiki/IIIMF "wikilink")のimmodule
  - im-uim - [uim](https://ja.wikipedia.org/wiki/uim "wikilink")のimmodule

## 出典

## 関連項目

  - [ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/ウィジェット・ツールキット "wikilink")
  - [GLib](../Page/GLib.md "wikilink")
  - [FLTK](../Page/FLTK.md "wikilink")
  - [Gtk\#](https://ja.wikipedia.org/wiki/Gtk_Sharp "wikilink")
  - [GTK-Qt](https://ja.wikipedia.org/wiki/GTK-Qt "wikilink")
  - [gtkmm](https://ja.wikipedia.org/wiki/gtkmm "wikilink")

## 外部リンク

  - [GTKオフィシャルサイト](https://www.gtk.org/)
  - [GNOMEオフィシャルサイト](https://www.gnome.org/)
  - [日本GNOMEユーザ会](http://www.gnome.gr.jp/)(APIリファレンス・チュートリアル等の日本語訳)

[Category:GTK+](https://ja.wikipedia.org/wiki/Category:GTK+ "wikilink") [Category:GNOME](https://ja.wikipedia.org/wiki/Category:GNOME "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/Category:ウィジェット・ツールキット "wikilink")

1.
2.  [GTK+ renamed to GTK](https://lwn.net/Articles/779305/rss)
3.  [Language Bindings](http://www.gtk.org/language-bindings.php)
4.  [GNOME ART](http://art.gnome.org/themes/gtk2/)
5.
6.
7.  [Projects/GTK/OSX](https://wiki.gnome.org/action/show/Projects/GTK/OSX?action=show&redirect=Projects%2FGTK%2B%2FOSX)
8.  [GTK Download: Windows](https://www.gtk.org/download/windows.php)
9.  [GTK+ for Windows Runtime Environment](https://sourceforge.net/projects/gtk-win/)
10. [GTK+ for Windows Runtime Environment Installer (fork from <http://gtk-win.sourceforge.net>): tschoonj/GTK-for-Windows-Runtime-Environment-Installer](https://github.com/tschoonj/GTK-for-Windows-Runtime-Environment-Installer)