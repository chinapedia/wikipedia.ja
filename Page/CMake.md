> この記事は[CMake](https://ja.wikipedia.org/wiki/CMake)から翻訳されています。


**CMake**はコンパイラに依存しないビルド自動化のためのフリーソフトウェアであり、様々なオペレーティングシステムで動作させることができる。CMakeは階層化ディレクトリや複数のライブラリを利用するアプリケーションをサポートするよう設計されている。実際のビルドにおいては、[make](https://ja.wikipedia.org/wiki/make "wikilink")、[Xcode](../Page/Xcode.md "wikilink")、[Visual Studioのようなネイティブのビルド環境が利用される](https://ja.wikipedia.org/wiki/Visual_Studio "wikilink")。CMake自身は最小限の依存関係を持つよう設計されており、ビルドするにはC++コンパイラのみを必要とする\[1\]。

## 歴史

CMakeは1999年に開発が始まった。その目的は[Insight Segmentation and Registration Toolkit (ITK)](https://ja.wikipedia.org/wiki/Insight_Segmentation_and_Registration_Toolkit "wikilink") のクロスプラットフォームなビルド環境の要求に答えるためのものだった\[2\]。このプロジェクトは可視化人間プロジェクト（）の一部として、[アメリカ国立医学図書館](https://ja.wikipedia.org/wiki/アメリカ国立医学図書館 "wikilink")の支援を受けた。CMakeは、可視化ソフトウェアである[Visualization Toolkit (VTK)](https://ja.wikipedia.org/wiki/VTK "wikilink") のサポートのためにKen Martinらによって開発されたpcmakerを一部参考にしている。Kitware社のBill Hoffmanはこのpcmakerの要素に、[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")の[configure](https://ja.wikipedia.org/wiki/configure "wikilink")スクリプトの代替品を作るという彼のアイディアを組み合わせた。2000年には最初の実装が作られ、2001年にはさらに開発が進められた。その後、CMakeは下に示すようなCMake開発者達自身が関与するシステムに組み込まれることによって開発や改善が加速された。

  - [VXL](https://ja.wikipedia.org/wiki/VXL "wikilink")プロジェクト（コンピュータビジョン用ライブラリ）
  - [The CABLE](http://public.kitware.com/Cable/HTML/Index.html): 機能はBrad Kingによって追加されたもの
  - [ゼネラル・エレクトリック](../Page/ゼネラル・エレクトリック.md "wikilink")の研究開発部門にてDART (Distribution Automation Remote Terminal) の開発に使用される

いくつかの機能は、VTKがビルドシステムをCMakeに切り替えたときや、同じく可視化ソフトウェアである[ParaView](https://ja.wikipedia.org/wiki/ParaView "wikilink")に対応するために追加されたものである。

## 機能

CMakeはインプレースおよびアウトオブプレースでのビルドの双方に対応しており、同じソースツリーから複数のビルド結果を生成でき、また[クロスコンパイル](https://ja.wikipedia.org/wiki/クロスコンパイル "wikilink")にも対応している。この、ソースツリーの外側にビルド結果を生成する仕組みはCMakeの重要な特徴で、ビルドツリーが削除されてもソースファイルには影響しない。

CMakeは必要な実行ファイルやその他のファイル、ライブラリの場所を探し出すことができる。その結果は[キャッシュに保存され](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")、またそれはビルドの前に調整することができる。調整には、プロジェクトに付属するグラフィカルエディタを使うことができる。

複雑なディレクトリ階層や、いくつものライブラリに依存したアプリケーションにもCMakeは対応している。例えば、依存しているツールキットやライブラリがそれぞれに複数のディレクトリを持つような場合でも処理が可能である。加えて、最終的なアプリケーションのコンパイルに必要なコードを生成する実行ファイルを事前に生成しておくことが求められるような複雑なビルドにも対応できる。CMakeはオープンソースであり、拡張も容易なため、必要に応じて特定のプロジェクト向けに改変することもできる。

CMakeは[UNIX](../Page/UNIX.md "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")といった様々なプラットフォームや[Microsoft Visual C++](../Page/Microsoft_Visual_C++.md "wikilink")、[Cygwin](../Page/Cygwin.md "wikilink")、[MinGW](../Page/MinGW.md "wikilink")、[Xcode](../Page/Xcode.md "wikilink")といった[IDEに対応したmakefileを生成することが可能である](../Page/統合開発環境.md "wikilink")。

## ビルドプロセス

CMakeのビルドプロセスは2段階からなる。まず、CMake用の設定ファイルから通常のビルド環境用のビルドファイルを生成する。次に、プラットフォームネイティブのビルドツールがそれを利用して実際のビルドを行う\[3\]。

各プロジェクトは、ディレクトリ毎にビルドプロセスを制御するためのファイル`CMakeLists.txt`を持つ。同ファイルには一つ以上のコマンドが、`COMMAND (args...)`の形式で記述される。ここで`COMMAND`はコマンドを表す名前で、`args`は空白で区切られた引数のリストが記述される。CMakeには静的/動的[ライブラリ](../Page/ライブラリ.md "wikilink")や実行ファイルをコンパイルするための様々な組み込みルールが豊富に用意されているが、ユーザーがルールを追加するための仕組みも提供されている。ビルドに関する依存関係の一部は自動的に解決される。高度な使い方としては、特殊なコンパイラやOSに対応するためのmakefile生成器を組み込むことが可能である\[4\]。

## 内部構成

CMake、CPack、CTestの実行ファイルは、[C++](../Page/C++.md "wikilink")プログラミング言語で書かれている。

CMakeの機能の多くはCMake言語で書かれたモジュールの中で実装されている。

リリース3.0から、CMakeのドキュメントには[reStructuredText](https://ja.wikipedia.org/wiki/reStructuredText "wikilink")マークアップが使用されているようになった。HTMLページとmanページは、ドキュメント・ジェネレータである[Sphinxから自動生成されている](../Page/Sphinx_\(ドキュメンテーションジェネレータ\).md "wikilink")。

## CPack

**CPack**は、CMakeと密に統合されているソフトウェア配布のためのパッケージングシステムである。しかし、CMakeがなくても動作するように作られている。

一般には、以下のような用途に利用できる。

  - Linux [RPM](../Page/RPM_Package_Manager.md "wikilink")、[deb](https://ja.wikipedia.org/wiki/Deb_\(ファイルフォーマット\) "wikilink")、[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")配布ファイルを[バイナリ](../Page/バイナリ.md "wikilink")および[ソースコード](../Page/ソースコード.md "wikilink")の2つの形式で提供する
  - [NSISファイル](https://ja.wikipedia.org/wiki/Nullsoft_Scriptable_Install_System "wikilink")（[Microsoft Windows用](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")）
  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")向けパッケージ

## 関連項目

  - [Autotools](../Page/Autotools.md "wikilink")
  - [Meson](https://ja.wikipedia.org/wiki/Meson_\(ソフトウェア\) "wikilink")
  - [Premake](https://ja.wikipedia.org/wiki/:en:Premake "wikilink")
  - [GYP](https://ja.wikipedia.org/wiki/GYP_\(ソフトウェア\) "wikilink")（Generate Your Projects）
  - [SCons](https://ja.wikipedia.org/wiki/SCons "wikilink")
  - [Waf](https://ja.wikipedia.org/wiki/:en:Waf "wikilink")

## 脚注

## 外部リンク

  - [CMake home page](https://cmake.org/)
  - [Kitware](https://www.kitware.com/)
  - [CDash](https://www.cdash.org/)
  - [CMake Examples Wiki](https://gitlab.kitware.com/cmake/community/wikis/doc/cmake/Examples)
  - [CMake Tools for Visual Studio](https://vector-of-bool.github.io/docs/vscode-cmake-tools/index.html)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink")

1.
2.
3.
4.