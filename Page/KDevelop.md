> この記事は[KDevelop](https://ja.wikipedia.org/wiki/KDevelop)から翻訳されています。


**KDevelop**（ケーデベロップ）は、[Linux](../Page/Linux.md "wikilink")や他の[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")における[フリーな](../Page/フリーソフトウェア.md "wikilink")[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) の一種である。KDevelopは[GPLで提供されている](../Page/GNU_General_Public_License.md "wikilink")。

KDevelopには[コンパイラ](../Page/コンパイラ.md "wikilink")は含まれていない。代わりに[GNUコンパイラコレクション](../Page/GNUコンパイラコレクション.md "wikilink")（あるいは他のコンパイラ）を使って実行コードを生成する。

[Ada](../Page/Ada.md "wikilink")、[Bash](../Page/Bash.md "wikilink")、[C言語](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")、[Fortran](https://ja.wikipedia.org/wiki/Fortran "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[Pascal](../Page/Pascal.md "wikilink")、[Perl](../Page/Perl.md "wikilink")、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[Python](../Page/Python.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、[SQL](../Page/SQL.md "wikilink") といった多数の[プログラミング言語](../Page/プログラミング言語.md "wikilink")をサポートしている。

## 歴史

KDevelop 3.0では、KDevelop 2が完全に書き換えられた。[2004年](../Page/2004年.md "wikilink")2月に、[KDE](../Page/KDE.md "wikilink") 3.2と共にリリースされた。

## 機能

KDevelopでは、[KPart](https://ja.wikipedia.org/wiki/KPart "wikilink")技術を通して組み込みの[テキストエディタ](../Page/テキストエディタ.md "wikilink")コンポーネントを利用する。デフォルトのエディタは[Kate](../Page/Kate.md "wikilink")であるが、[Qt](../Page/Qt.md "wikilink") Designerベースのエディタに置換する設定も可能である。以下のリストでは、主にKDevelop自身の機能を列挙している。エディタ固有の機能については、それらエディタの記事を参照されたい。

  - [ソースコードエディタ](https://ja.wikipedia.org/wiki/ソースコードエディタ "wikilink")として、キーワードのハイライト表示と自動[字下げが可能](../Page/字下げスタイル.md "wikilink") (Kate)
  - 各種プロジェクト管理に対応。[Automake](../Page/Autotools.md "wikilink")、[Qt](../Page/Qt.md "wikilink")ベースの *qmake*、Javaベースのプロジェクト向けの [Apache Ant](../Page/Apache_Ant.md "wikilink") などである。
  - クラスブラウザ装備
  - GUIデザイナー装備
  - [GNUコンパイラコレクション](../Page/GNUコンパイラコレクション.md "wikilink")のための[フロントエンド](../Page/フロントエンド.md "wikilink")
  - [GNUデバッガ](../Page/GNUデバッガ.md "wikilink")のための[フロントエンド](../Page/フロントエンド.md "wikilink")
  - [クラス定義や](../Page/クラス_\(コンピュータ\).md "wikilink")[アプリケーションフレームワーク](../Page/アプリケーションフレームワーク.md "wikilink")の生成・更新のための[ウィザード](../Page/ウィザード_\(ソフトウェア\).md "wikilink")
  - 自動[入力補完](https://ja.wikipedia.org/wiki/入力補完 "wikilink") ([C言語](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink"))
  - [Doxygen](../Page/Doxygen.md "wikilink")をデフォルトでサポート
  - [バージョン管理システム](../Page/バージョン管理システム.md "wikilink")サポート。[CVS](../Page/Concurrent_Versions_System.md "wikilink")、[Subversion](../Page/Apache_Subversion.md "wikilink")、[Perforce](../Page/Perforce.md "wikilink")、[ClearCase](https://ja.wikipedia.org/wiki/ClearCase "wikilink") など。

KDevelop 3 は完全な[プラグイン](../Page/プラグイン.md "wikilink")ベースのアーキテクチャである。開発者が何らかの変更を加えたとき、彼がしなければならないのは、そのプラグインの[コンパイルだけである](../Page/コンパイラ.md "wikilink")。ロードすべき[プラグイン](../Page/プラグイン.md "wikilink")群を指定するプロファイルを複数保持することができる。KDevelop自身には[テキストエディタ](../Page/テキストエディタ.md "wikilink")は含まれていないが、それにもプラグインが利用できる。KDevelop はプログラミング言語やシステムから独立していて、[KDE](../Page/KDE.md "wikilink")、[GNOME](../Page/GNOME.md "wikilink")、[Qt](../Page/Qt.md "wikilink")、[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")、[wxWidgets](https://ja.wikipedia.org/wiki/wxWidgets "wikilink")などをサポートしている。

KDevelopは各種[プログラミング言語](../Page/プログラミング言語.md "wikilink")をサポートしており、[C言語](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")、[Perl](../Page/Perl.md "wikilink")、[Python](../Page/Python.md "wikilink")、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[Fortran](https://ja.wikipedia.org/wiki/Fortran "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、[Ada](../Page/Ada.md "wikilink")、[Pascal](../Page/Pascal.md "wikilink")、[SQL](../Page/SQL.md "wikilink")などの言語や [Bash](../Page/Bash.md "wikilink")のスクリプト作成に対応している。ビルドシステムとしては、GNU (automake)、cmake、qmake、その他をサポートしている。

入力補完は[C言語](../Page/C言語.md "wikilink")や[C++](../Page/C++.md "wikilink")で可能である。シンボルは [Berkeley DB](../Page/Berkeley_DB.md "wikilink") ファイルに保持され、再[構文解析](../Page/構文解析.md "wikilink")せずに高速に検索される。KDevelop は他のプログラミング言語向けの新たな[構文解析器](../Page/構文解析器.md "wikilink")を作成するフレームワークも提供している。

統合された[デバッガ](../Page/デバッガ.md "wikilink")によって、グラフィカルに[ブレークポイント](https://ja.wikipedia.org/wiki/ブレークポイント "wikilink")を設定したり、バックトレースを見たりといったデバッグが可能である。[コマンドラインのgdbとは異なり](https://ja.wikipedia.org/wiki/キャラクターユーザインタフェース "wikilink")、プラグインとして動的にロードして利用することができる。

*Quick Open*により、ファイル間の迅速な誘導が行われる。

現在、50から100のプラグインが存在している。主なものとして、永続的なプロジェクト全体用コード[ブックマーク](../Page/ブックマーク.md "wikilink")、テキスト入力を高速化する*Code abbreviations*、スタイルガイドに従ってコードを整形する*Source formatter*、[正規表現](../Page/正規表現.md "wikilink")による検索、プロジェクト全体に対する検索/置換機能（[リファクタリングで有効](../Page/リファクタリング_\(プログラミング\).md "wikilink")）などがある。

## 関連項目

  - [Anjuta](../Page/Anjuta.md "wikilink")
  - [Kate](../Page/Kate.md "wikilink") (KDE advanced text editor)

## 外部リンク

  - [KDevelop homepage](http://www.kdevelop.org/)
  - [KDevelop project on freshmeat](http://freshmeat.net/projects/kdevelop/)
  - [Freehackers interview with KDevelop team](http://www.freehackers.org/interviews/kdevelop-2002-08/)
  - [KDE programming tutorial using KDevelop](http://www.dazzle.plus.com/linux/)
  - [KDevelop](http://www.kde.gr.jp/pukiwiki/index.php?KDevelop) 日本KDEユーザ会

[Category:KDE](https://ja.wikipedia.org/wiki/Category:KDE "wikilink") [Category:Qtを使用するソフトウェア](https://ja.wikipedia.org/wiki/Category:Qtを使用するソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:Java開発ツール](https://ja.wikipedia.org/wiki/Category:Java開発ツール "wikilink")