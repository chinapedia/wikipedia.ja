> この記事は[FLTK](https://ja.wikipedia.org/wiki/FLTK)から翻訳されています。


**FLTK**（**F**ast, **L**ight **T**ool**k**it）は、[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")の[GUIライブラリであり](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、Bill Spitzakらが1998年に開発した。[3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")との親和性を考慮し、[OpenGL](../Page/OpenGL.md "wikilink")とのインタフェースも持っているが、一般的GUIプログラミングにも適している。

独自の[ウィジェット](https://ja.wikipedia.org/wiki/ウィジェット_\(GUI\) "wikilink")、描画、イベントシステムを使って、基盤となっている各システム固有のコードを抽象化している（なお、FLTK2では実験的に [cairo](https://ja.wikipedia.org/wiki/cairo "wikilink") もサポートしている）。これによって、どの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")でも同じ見た目のプログラムを書くことができる。

FLTKは[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であり、[LGPLに非互換なライセンスのアプリケーションとの静的リンクを許すという条項を加えたライセンスとなっている](../Page/GNU_Lesser_General_Public_License.md "wikilink")。ライブラリだけなくFLUID (*FLTK User Interface Designer*) というグラフィカルなGUI設計ツールが含まれ、[C++](../Page/C++.md "wikilink") のソースファイルとヘッダファイルを生成する。

[Qt](https://ja.wikipedia.org/wiki/Qt "wikilink")や[wxWidgets](https://ja.wikipedia.org/wiki/wxWidgets "wikilink")に比べると、FLTKはより軽量に設計されていて、機能もGUI機能に限定されている。このためライブラリは非常に小さく（FLTKによる "Hello World" プログラムは約100[KiB](https://ja.wikipedia.org/wiki/キビバイト "wikilink")）、[静的リンク](https://ja.wikipedia.org/wiki/静的リンク "wikilink")されることが多い。また、複雑なマクロやプリプロセッサもなく、C++ の最新機能（テンプレート、[例外](../Page/例外処理.md "wikilink")、[RTTI](https://ja.wikipedia.org/wiki/実行時型情報 "wikilink")、FLTK 1.x では名前空間）も使っていない。従って、習熟が比較的容易である。

長所は短所にもなる。FLTKは多くのウィジェット・ツールキットよりも提供するウィジェットの種類が少ない。また、ネイティブでないウィジェットであるため、そのプラットフォームのネイティブな[ルック・アンド・フィール](../Page/ルック・アンド・フィール.md "wikilink")とは異なる。

## 名称の由来

FLTKは当初、[シリコングラフィックス](../Page/シリコングラフィックス.md "wikilink")のマシン向けのForms Library互換となるよう設計された。このライブラリでは、全ての関数や構造体の名前に "fl_" というプレフィックスが付いていた。FLTKでもこの命名規則がそのまま適用され、そこから "FL" という名称とされた。しかし、リリースして見ると "FL" という名称をインターネット上で検索するのが困難だったため（例えば[フロリダ州](https://ja.wikipedia.org/wiki/フロリダ州 "wikilink")も"FL"と略記される）、盛んに議論と調査を行った上で "FLTK" という名称が選ばれ、後付けで "Fast Light Tool Kit" の略とされた。

## プログラミング言語での使用

FLTKは[C++](../Page/C++.md "wikilink")で書かれているので、C++での利用に適している。しかし、他の[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")言語向けの[バインディングもあり](https://ja.wikipedia.org/wiki/束縛_\(情報工学\) "wikilink")、例えば、[Python](../Page/Python.md "wikilink")向けバインディング\[1\]や[Ruby](../Page/Ruby.md "wikilink")向けバインディング\[2\]や[Lua](../Page/Lua.md "wikilink")向けバインディング\[3\]がある。

以下のコード例は、FLTK 1.xを使って "Okay" [ボタンのあるウィンドウを生成するものである](https://ja.wikipedia.org/wiki/ボタン_\(GUI\) "wikilink")。

``` cpp
#include <FL/Fl.H>
#include <FL/Fl_Window.H>
#include <FL/Fl_Button.H>

int main(int argc, char *argv[]) {
   Fl_Window* w = new Fl_Window(330, 190);
   new Fl_Button(110, 130, 100, 35, "Okay");
   w->end();
   w->show(argc, argv);
   return Fl::run();
}
```

## FLTKを使っているソフトウェア

  - [CinePaint](https://ja.wikipedia.org/wiki/CinePaint "wikilink")は[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")からFLTKに移行中
  - [flwm](http://flwm.sourceforge.net) - [ウィンドウマネージャ](https://ja.wikipedia.org/wiki/ウィンドウマネージャ "wikilink")
  - [Nuke](https://ja.wikipedia.org/wiki/Nuke "wikilink") - ハイエンドデジタル合成ソフトウェア
  - [en:SmallBASICのWindows版](https://ja.wikipedia.org/wiki/:en:SmallBASIC "wikilink")
  - [PosteRazor](http://posterazor.sourceforge.net) - オープンソースのポスター印刷ソフトウェア (Windows, macOS, Linux)
  - [en:Avimator](https://ja.wikipedia.org/wiki/:en:Avimator "wikilink") - [en:BVHエディタ](https://ja.wikipedia.org/wiki/:en:Biovision_Hierarchy "wikilink")
  - [Dillo](https://ja.wikipedia.org/wiki/Dillo "wikilink") - ウェブブラウザ
  - [Gmsh](https://ja.wikipedia.org/wiki/Gmsh "wikilink") - オープンソースの[有限要素法](../Page/有限要素法.md "wikilink")用メッシュ生成
  - [en:EDE](https://ja.wikipedia.org/wiki/:en:EDE "wikilink") - Equinox Desktop Environment
  - [Open Movie Editor](http://www.openmovieeditor.org/)
  - [en:ZynAddSubFX](https://ja.wikipedia.org/wiki/:en:ZynAddSubFX "wikilink") - オープンソースの[ソフトウェア・シンセサイザー](https://ja.wikipedia.org/wiki/ソフトウェア・シンセサイザー "wikilink")
  - [en:Agenda VR3](https://ja.wikipedia.org/wiki/:en:Agenda_VR3 "wikilink") - [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")搭載[携帯情報端末](../Page/携帯情報端末.md "wikilink")用ソフトウェア
  - [GNU Octave](../Page/GNU_Octave.md "wikilink") - [MATLAB](https://ja.wikipedia.org/wiki/MATLAB "wikilink")互換の数値解析ソフトウェア

## 関連項目

  - [ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/ウィジェット・ツールキット "wikilink")
  - [Qt](https://ja.wikipedia.org/wiki/Qt "wikilink")
  - [wxWidgets](https://ja.wikipedia.org/wiki/wxWidgets "wikilink")
  - [GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")

## 脚注

## 外部リンク

  - [FLTK公式サイト](http://www.fltk.org)
  - [初心者用チュートリアル（英語）](http://www3.telus.net/public/robark/)
  - [Erco's FLTK Cheat Page](http://www.seriss.com/people/erco/fltk/)

[Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/Category:ウィジェット・ツールキット "wikilink")

1.  [pyFLTK Home Page](http://pyfltk.sourceforge.net/)
2.  [Ruby/FLTK Home Page](http://ruby-fltk.sourceforge.net/)
3.  [murgaLua Home Page](http://www.murga-projects.com/murgaLua.html/)