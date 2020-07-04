> この記事は[Notepad++](https://ja.wikipedia.org/wiki/Notepad++)から翻訳されています。


**Notepad++**は、[Windowsで動作する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[フリーな](../Page/フリーソフトウェア.md "wikilink")[ソースコードエディタ](https://ja.wikipedia.org/wiki/ソースコードエディタ "wikilink")である。[Stack Overflowが毎年実施している人気調査によれば](https://ja.wikipedia.org/wiki/Stack_Overflow "wikilink")、2015年で1位、2019年で3位と上位に位置している。

## 歴史

Notepad++は、[2003年](../Page/2003年.md "wikilink")9月にDon Hoによって開発された\[1\]。Donは、会社でJEXT（[Java](https://ja.wikipedia.org/wiki/Java "wikilink")ベースのテキストエディタ）を使用していたが、そのパフォーマンスの低さへの不満から、[Scintilla](https://ja.wikipedia.org/wiki/Scintilla "wikilink")を用いて[C++](../Page/C++.md "wikilink")でテキストエディタの開発を始めた\[2\]。彼は、会社によってこの開発に関するアイディアが退けられたため、彼自身の個人的な時間を割いて開発を進めた\[3\]。Notepad++は、[Microsoft Windows用のアプリケーションとして構築されている](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。開発者は、[wxWidgets](https://ja.wikipedia.org/wiki/wxWidgets "wikilink")を用いて[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")と[UNIX](../Page/UNIX.md "wikilink")プラットフォームへ移植することを検討したが、最終的にはこれは断念された\[4\]。

Notepad++は、最初、Windows向けのみのアプリケーションとして2003年[11月25日](../Page/11月25日.md "wikilink")、[SourceForge](https://ja.wikipedia.org/wiki/SourceForge "wikilink")に公開された。Scintillaコンポーネントをベースにしており、C++を用いて書かれているが、パフォーマンスの向上とプログラムサイズの削減のため、STLのみをWin32 APIコールとして用いている\[5\]。

2010年1月、米国政府は、アメリカを拠点に開発されているオープンソースプロジェクトについて、[キューバ](../Page/キューバ.md "wikilink")、[イラン](../Page/イラン.md "wikilink")、[北朝鮮](https://ja.wikipedia.org/wiki/北朝鮮 "wikilink")、[スーダン](../Page/スーダン.md "wikilink")、[シリア](../Page/シリア.md "wikilink")からのアクセス禁止を義務付けた\[6\]。開発者は、これがフリーソフトウェア、オープンソース・ソフトウェアの思想にたいする侵害であると感じられたため、2010年7月、Notepad++は、米国の司法管轄権から退出した。ただし、フォーラムやバグトラッカーなどいくつかのコミュニティサービスは、[2015年](../Page/2015年.md "wikilink")にNotepad++がSourceforgeから撤退するまでとどまり続けた\[7\]\[8\]\[9\]。

[2011年](../Page/2011年.md "wikilink")、Lifehackerは、Notepad++を"The Best Programming Text Editor for Windows"とした。これは「もし単純、軽量で拡張可能なプラグラミング向けのテキストエディタを好むなら、フリーでオープンソースなNotepad++がファーストチョイスとなる」というものである\[10\]。Lifehackerは、[2014年](../Page/2014年.md "wikilink")には、読者による投票に基づいてNotepad++を"Most Popular Text Editor"に選出している\[11\]。

[2015年](../Page/2015年.md "wikilink")には、前述のようにNotepad++はSourceForgeを完全に撤退し、フォーラムはNodeBBに、バグトラッカーは[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")に移転している\[12\]\[13\]。

## 詳細

Notepad++の開発目的は、自在にカスタマイズ可能な[GUIを備えたスリムで効率的な](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[バイナリ](../Page/バイナリ.md "wikilink")を提供することである。 本ソフトウェアは[Scintilla](https://ja.wikipedia.org/wiki/Scintilla "wikilink")という[コンポーネントをベースにしており](../Page/ソフトウェアコンポーネント.md "wikilink")、[Win32 APIコールを用いて](../Page/Windows_API.md "wikilink")[STLを利用した](../Page/Standard_Template_Library.md "wikilink")[C++](../Page/C++.md "wikilink")で記述されている。 なお、Scintillaは複数行にわたる正規表現の検索と置換をサポートしていないが、Notepad++はこの問題を解決し得るプラグインを有している。

Notepad++の開発者は1人だけで、本ソフトウェアを他の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")(OS)へ移植する資源が無い。 [Linux](../Page/Linux.md "wikilink")や[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")などの[Unix系](../Page/Unix系.md "wikilink")OS上では、[Wine](../Page/Wine.md "wikilink")を利用すれば、本ソフトウェアを動作させられる。

### 特徴

  - [マクロと](../Page/マクロ_\(コンピュータ用語\).md "wikilink")[プラグイン](../Page/プラグイン.md "wikilink")
      - 多くのテキスト変換のオプションを提供するTextFXと呼ばれるユーザが書いたプラグインがデフォルトで含まれている
  - [自動補完](https://ja.wikipedia.org/wiki/自動補完 "wikilink")（言語とファイル）
  - ブックマーク
  - [シンタックスハイライト](../Page/シンタックスハイライト.md "wikilink")（加えて、括弧とインデントのハイライト）
  - [正規表現](../Page/正規表現.md "wikilink")による検索と置換
  - 画面分割（スクロールの同期も可能）
  - ズーム
  - [スペルチェッカ](../Page/スペルチェッカ.md "wikilink")（組み込まれているが[Aspellを要する](../Page/GNU_Aspell.md "wikilink")）
  - Hex編集（標準インストールに含まれるプラグイン）
  - タブエディタ（多段表示にも対応）
  - [FTPブラウザ](../Page/File_Transfer_Protocol.md "wikilink")（標準インストールに含まれるプラグイン）
  - 様々な[文字コード](../Page/文字コード.md "wikilink")のサポート
  - 自動アップデート

次に列挙されているように多数の[コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")向けのシンタックスハイライト（構文の強調表示や変数・関数の色分けや折り畳みなど）のサポートが本ソフトウェアの特徴である。 更に、ユーザー言語定義システムを利用すれば、たとえば[MediaWiki](../Page/MediaWiki.md "wikilink")や[Fortran 90](https://ja.wikipedia.org/wiki/FORTRAN#Fortran_90 "wikilink")、[CAPLといった](../Page/Communication_Access_Programming_Language.md "wikilink")、デフォルトで定義されていない言語のシンタックスハイライトをユーザーが自ら作成できる。

  - [ActionScript](../Page/ActionScript.md "wikilink")
  - [Ada](../Page/Ada.md "wikilink")
  - [ASN.1](../Page/Abstract_Syntax_Notation_One.md "wikilink")
  - [ASP](../Page/Active_Server_Pages.md "wikilink")

<!-- end list -->

  - [アセンブリ言語](../Page/アセンブリ言語.md "wikilink")
  - [AutoIt](https://ja.wikipedia.org/wiki/AutoIt "wikilink")
  - [AviSynth](../Page/AviSynth.md "wikilink")スクリプト
  - BaanC
  - [BAT](../Page/バッチファイル.md "wikilink")
  - Blitz BASIC
  - [C言語](../Page/C言語.md "wikilink")
  - [C\#](../Page/C_Sharp.md "wikilink")
  - [C++](../Page/C++.md "wikilink")
  - [Caml](https://ja.wikipedia.org/wiki/Caml "wikilink")
  - [CMake](https://ja.wikipedia.org/wiki/CMake "wikilink")
  - [COBOL](../Page/COBOL.md "wikilink")
  - [Csound](../Page/Csound.md "wikilink")
  - [CoffeeScript](https://ja.wikipedia.org/wiki/CoffeeScript "wikilink")
  - [CSS](../Page/Cascading_Style_Sheets.md "wikilink")
  - [D言語](../Page/D言語.md "wikilink")
  - [diff](https://ja.wikipedia.org/wiki/diff "wikilink")

<!-- end list -->

  - [Erlang](../Page/Erlang.md "wikilink")
  - ESCRIPT
  - [Forth](../Page/Forth.md "wikilink")
  - [FORTRAN](../Page/FORTRAN.md "wikilink")
  - [FreeBASIC](../Page/FreeBASIC.md "wikilink")
  - Gui4Cli
  - [Haskell](../Page/Haskell.md "wikilink")
  - [HTML](../Page/HyperText_Markup_Language.md "wikilink")
  - MS [INIファイル](https://ja.wikipedia.org/wiki/INIファイル "wikilink")
  - [Inno Setupスクリプト](https://ja.wikipedia.org/wiki/Inno_Setup "wikilink")
  - [Intel HEX](https://ja.wikipedia.org/wiki/Intel_HEX "wikilink")
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
  - [JavaScript](../Page/JavaScript.md "wikilink")
  - [JSON](https://ja.wikipedia.org/wiki/JSON "wikilink")
  - [JSP](../Page/JavaServer_Pages.md "wikilink")
  - KiXtart
  - [LaTeX](../Page/LaTeX.md "wikilink")
  - [LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")
  - [Lua](../Page/Lua.md "wikilink")
  - [make](https://ja.wikipedia.org/wiki/make "wikilink")file
  - [MATLAB](../Page/MATLAB.md "wikilink")
  - [MMIX](../Page/MMIX.md "wikilink")AL
  - [Nim](https://ja.wikipedia.org/wiki/Nim "wikilink") (Nimrod)
  - nnCrontab
  - [NSYS](https://ja.wikipedia.org/wiki/Nullsoft_Scriptable_Install_System "wikilink")
  - [Objective-C](../Page/Objective-C.md "wikilink")
  - OScript
  - [Pascal](../Page/Pascal.md "wikilink")
  - [Perl](../Page/Perl.md "wikilink")
  - [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")
  - [PostScript](../Page/PostScript.md "wikilink")
  - [PowerShell](../Page/PowerShell.md "wikilink")
  - Properties
  - [PureBasic](../Page/PureBasic.md "wikilink")
  - [Python](../Page/Python.md "wikilink")
  - [R言語](../Page/R言語.md "wikilink")
  - [REBOL](../Page/REBOL.md "wikilink")
  - [レジストリ](../Page/レジストリ.md "wikilink") (\*.reg)
  - [リソースファイル](../Page/リソース_\(Windows\).md "wikilink")
  - [Ruby](../Page/Ruby.md "wikilink")
  - [Rust](https://ja.wikipedia.org/wiki/Rust "wikilink")
  - [シェルスクリプト](../Page/シェルスクリプト.md "wikilink")・[Unix Shell Script](https://ja.wikipedia.org/wiki/Unixシェル "wikilink")
  - [Scheme](../Page/Scheme.md "wikilink")
  - [Smalltalk](../Page/Smalltalk.md "wikilink")
  - [SPICE](../Page/SPICE_\(ソフトウェア\).md "wikilink")
  - [SQL](../Page/SQL.md "wikilink")
  - [Swift](https://ja.wikipedia.org/wiki/Swift "wikilink")
  - [S-record](../Page/S-record.md "wikilink")
  - [Tcl](https://ja.wikipedia.org/wiki/Tcl "wikilink")
  - Tektronix extended HEX
  - [TeX](../Page/TeX.md "wikilink")
  - txt2tags
  - [Verilog](../Page/Verilog.md "wikilink")
  - [VHDL](../Page/VHDL.md "wikilink")
  - [Visual Basic](../Page/Visual_Basic.md "wikilink")・[VBScript](../Page/VBScript.md "wikilink")
  - Visual Prolog
  - [XML](../Page/Extensible_Markup_Language.md "wikilink")
  - [YAML](../Page/YAML.md "wikilink")

## 注釈

## 外部リンク

  -
  -
<!-- end list -->

  -
  -
  -   -
  -   -
  -
  -
  -
  -   -
  -
<!-- end list -->

  -
[Category:テキストエディタ](https://ja.wikipedia.org/wiki/Category:テキストエディタ "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Windowsのソフトウェア](https://ja.wikipedia.org/wiki/Category:Windowsのソフトウェア "wikilink") [Category:2003年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2003年のソフトウェア "wikilink")

1.
2.
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
13.