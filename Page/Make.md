> この記事は[Make](https://ja.wikipedia.org/wiki/Make)から翻訳されています。


は、[プログラムの](../Page/プログラム_\(コンピュータ\).md "wikilink")[ビルド作業を自動化するツール](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink")。[コンパイル](../Page/コンパイラ.md "wikilink")、[リンク](../Page/リンケージエディタ.md "wikilink")、[インストール](../Page/インストール.md "wikilink")等のルールを記述したテキストファイル (makefile) に従って、これらの作業を自動的に行う。

## 機能

複雑に関連し合ったファイルの依存関係を解決するのがmakeの長所である。例えば、A というファイルを処理して B というファイルを生成するとき、makeはそれぞれのファイルの更新時刻（[タイムスタンプ](https://ja.wikipedia.org/wiki/タイムスタンプ "wikilink")）を参照し、A が B よりも新しいときには作業を行うが、B が A より新しければ作業は不要と見なして何もしない。ファイル数が増え、依存関係が複雑になっても、makeはmakefileの記述を頼りに必要最低限の作業だけを自動で行う。[Autotools](../Page/Autotools.md "wikilink")という別のツールを使う事でmakefileの自動生成が可能である。

[UNIX](../Page/UNIX.md "wikilink")系[ソフトウェア](../Page/ソフトウェア.md "wikilink")は、ソースコードの形で配布されることがある。そのビルド作業にはほぼ必須のツールといえる（ごくまれにmakeを使わないソフトウェアも存在する）。

なお、makeはプログラムコードのビルド以外の用途にも使用可能である。例えば、[LaTeX](../Page/LaTeX.md "wikilink")のソースファイルから[DVI形式のファイルを生成する作業などにも使用することができる](https://ja.wikipedia.org/wiki/DVI_\(ファイルフォーマット\) "wikilink")。[バッチ処理](../Page/バッチ処理.md "wikilink")の簡略化にも使うこともできる。

## 歴史

元々は1976年4月に[ベル研究所](../Page/ベル研究所.md "wikilink")でによって作成された。

Feldman は、変更されたが実行ファイルが誤って更新されていないプログラムを無駄にデバッグしている同僚の経験から、Makeを書くことをひらめいた。

## 互換性

Linux Standard Baseでも指定コマンドになっている\[1\]。最近では[CMake](../Page/CMake.md "wikilink")を使う場合がある。

makeには互換性のない亜種が存在する。同様のツールとして[rake](https://ja.wikipedia.org/wiki/rake_\(ソフトウェア\) "wikilink")（[Ruby](../Page/Ruby.md "wikilink")用）、setup（[Python](../Page/Python.md "wikilink")用）がある。

## makeの実装

  - GNU make - [GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")による実装。
  - Schily make - ポータブルで拡張可能なmake。
  - BSD make - [BSD](../Page/BSD.md "wikilink")の実装。
  - Microsoft Program Maintenance Utility (make, nmake) - [マイクロソフト](../Page/マイクロソフト.md "wikilink")の実装。makeは極めて初期の処理系にのみ付属。

## 注釈

<references />

## 関連項目

  - [Apache Maven](../Page/Apache_Maven.md "wikilink") - Java用のプロジェクト管理ツール
  - [Apache Ant](../Page/Apache_Ant.md "wikilink") - Java用のmake
  - [SCons](https://ja.wikipedia.org/wiki/SCons "wikilink") - makeの代替ユーティリティ
  - [Ninja](https://ja.wikipedia.org/wiki/Ninja_\(ソフトウェア\) "wikilink") - makeの代替ユーティリティ
  - [CMake](../Page/CMake.md "wikilink") - クロスプラットフォームでオープンソースなビルドシステム
  - [Meson](https://ja.wikipedia.org/wiki/Meson_\(ソフトウェア\) "wikilink") - クロスプラットフォームでオープンソースなビルドシステム
  - [NAnt](https://ja.wikipedia.org/wiki/NAnt "wikilink") - .NET Frameworkで使用できるオープンソースのビルドシステム
  - [MSBuild](https://ja.wikipedia.org/wiki/MSBuild "wikilink") - .NET Frameworkで構築されたマイクロソフト標準のビルドシステム

## 外部リンク

  - [GNU make](https://www.gnu.org/software/make/)
  - [Makepp Home Page](http://makepp.sf.net)
  - [GNU Make 日本語マニュアル(Coop編)](http://www.ecoop.net/coop/translated/GNUMake3.77/make_toc.jp.html)

[Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")

1.  Linux Standard Base <https://refspecs.linuxfoundation.org/lsb.shtml>