> この記事は[Code::Blocks](https://ja.wikipedia.org/wiki/Code::Blocks)から翻訳されています。


**Code::Blocks**は[フリー](../Page/フリーソフトウェア.md "wikilink") / [オープンソース](../Page/オープンソース.md "wikilink")で[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")の[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) である。[wxWidgets](https://ja.wikipedia.org/wiki/wxWidgets "wikilink")を[GUIツールキットとして使い](https://ja.wikipedia.org/wiki/ウィジェット・ツールキット "wikilink")、[C++](../Page/C++.md "wikilink")で開発されている。プラグイン方式であり、機能は使用しているプラグイン群で決定される。現在のところ、Code::Blocks が対象とする開発言語は[C言語](../Page/C言語.md "wikilink") / [C++](../Page/C++.md "wikilink")だけである。

Code::Blocksは、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") で動作する。[FreeBSD](../Page/FreeBSD.md "wikilink")上でもビルドできる\[1\]。

## 歴史

2005年7月25日の1.0rc1と2005年10月25日の1.0rc2という2つの[リリース候補版](https://ja.wikipedia.org/wiki/リリース候補版 "wikilink")を経て、最終リリース版を完成させずにプロジェクトは新たな機能を多数追加し始めたため、最終リリースは何度も延期されていった。ただし、"nightly builds" と呼ばれる最新[SVN版のバイナリパッケージが毎日リリースされていた](../Page/Apache_Subversion.md "wikilink")。そのサポート状況は公式リリース版の1.0rc2よりも良かった。これによってユーザーは最新の改良が入手でき、開発者は定期的なフィードバックを得られたが、対外的にはプロジェクトが停滞しているように見えた（新たな公式リリースがなされなかったため）。

最初の安定版は2008年2月28日にリリースされ、バージョン番号は8.02とされた。バージョン番号のつけ方は[Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")方式に変更され、メジャー番号がリリース年、マイナー番号がリリース月を表している。

Jennic Ltd.は、[マイクロコントローラ](https://ja.wikipedia.org/wiki/マイクロコントローラ "wikilink")向けにカスタマイズされたCode::Blocksを配布している\[2\]。

## 機能

Code::Blocksは複数の[コンパイラ](../Page/コンパイラ.md "wikilink")をサポートしている（[MinGW](https://ja.wikipedia.org/wiki/MinGW "wikilink") / [GCC](../Page/GNUコンパイラコレクション.md "wikilink")、[Digital Mars D programming language](../Page/D言語.md "wikilink")、[Microsoft Visual C++](https://ja.wikipedia.org/wiki/Microsoft_Visual_C++ "wikilink")、、、[Intel C++ Compiler](../Page/Intel_C++_Compiler.md "wikilink")）。Code::BlocksはC++向けに設計されているが、一部の他の言語のコンパイラをサポートしている。例えば、[GNU Fortran](https://ja.wikipedia.org/wiki/GFortran "wikilink")、の[D言語](../Page/D言語.md "wikilink")、GNU GDCがある。

IDEには、[Scintilla](https://ja.wikipedia.org/wiki/Scintilla "wikilink")エディタコンポーネントを使ったシンタックスハイライトやコードの折りたたみ、[C++コード補完](https://ja.wikipedia.org/wiki/自動補完 "wikilink")、クラスブラウザ、統合TODOリスト、統合[デバッガ](../Page/デバッガ.md "wikilink")フロントエンド（[GDBをサポートし](../Page/GNUデバッガ.md "wikilink")、ちょっとした拡張でMicrosoft CDBもサポートできる）がある。また、[wxWidgets](https://ja.wikipedia.org/wiki/wxWidgets "wikilink")ツールキット向けの統合[RADプラグインwxSmithもある](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")。

他のIDEからの移行を促進するための機能もある（[Dev-C++](https://ja.wikipedia.org/wiki/Dev-C++ "wikilink")やMicrosoft Visual C++のプロジェクトインポートなど）。

Code::Blocksは独自のビルドシステムを使い、[XMLベースのプロジェクトファイルに情報を格納するが](../Page/Extensible_Markup_Language.md "wikilink")、GNUや[トロールテック](https://ja.wikipedia.org/wiki/トロールテック "wikilink")ののビルドシステムとのインタフェースを単純化するために外部Makefileもオプションでサポートしている。

## 関連項目

  - [SciTE](https://ja.wikipedia.org/wiki/SciTE "wikilink")
  - [wxWidgets](https://ja.wikipedia.org/wiki/wxWidgets "wikilink")

## 脚注

## 外部リンク

  - [Code::Blocks 公式サイト](http://www.codeblocks.org/)
  - [BerliOS プロジェクトサイト](http://developer.berlios.de/projects/codeblocks/) nightly buildsとSubversionへのアクセスはこちら
  - [Comparison of RADs for WxWidgets](http://wiki.codeblocks.org/index.php?title=Comparison_of_wxSmith_features)
  - [Code::Blocks](http://freshmeat.net/projects/codeblocks/) on Freshmeat（古い）

[Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink")

1.  [FreeBSD ports collection](ftp://ftp.freebsd.org/pub/FreeBSD/ports/i386/packages-7.0-release/Latest/)に Code::Blocksがある。
2.  [JN-UG-3028 Code::Blocks IDE User Guide](http://www.jennic.com/jennic_support/user_guides/jn-ug-3028_codeblocks_ide).