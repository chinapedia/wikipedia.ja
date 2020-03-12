> この記事は[Lazarus](https://ja.wikipedia.org/wiki/Lazarus)から翻訳されています。


**Lazarus(Ĺãżàŗůş)** は、[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")の[ビジュアルプログラミング](../Page/ビジュアルプログラミング言語.md "wikilink")[統合開発環境](../Page/統合開発環境.md "wikilink")である。[オープンソース](../Page/オープンソース.md "wikilink")の[Pascal](../Page/Pascal.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")である[Free Pascal向けに開発された](../Page/Free_Pascal.md "wikilink")。これはPascal及び[Object Pascalプログラマのために](../Page/Object_Pascal.md "wikilink")、[RADの一つである](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")[Delphi](../Page/Delphi.md "wikilink")に良く似たフリーの開発環境を作ろうとするものである。

Free Pascalは[オープンソース](../Page/オープンソース.md "wikilink")のコンパイラで、 **[Linux](../Page/Linux.md "wikilink")**、***Win32***、**[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")**、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[BSD](../Page/BSD.md "wikilink")、*68K*といった幅広い環境に対応している。Free Pascalは、Pascalのコンパイラであるが、Object指向の拡張がなされた*Delphi*の文法に従って書かれたソースもコンパイルすることができるように開発された。「[一度プログラムを書けば、どこでも走る](https://ja.wikipedia.org/wiki/write_once,_run_anywhere "wikilink")」というのは **[Java](https://ja.wikipedia.org/wiki/Java "wikilink")** のキャッチフレーズであるが、Lazarusは「[一度プログラムを書けば、どこでもコンパイルできる](https://ja.wikipedia.org/wiki/write_once,_compile_anywhere "wikilink")」を合言葉に、Free Pascalをベースとしたクロスラットフォームのコンパイラとライブラリの統合を目指している。Free Pascalは上記のような多くのプラットフォーム向けのコード生成が可能なので、Lazarusは、その特徴をいかした、GUIライブラリ (LCL) と、統合開発環境を提供している。Lazarusでは、コンポーネント等を用いるアプリケーションであれば、たとえGUIアプリケーションでも、プラットフォーム別にプログラムを書き換えなくてもいいように設計されている。

PascalのRAD-GUIアプリケーション開発言語としては、[Windowsでは](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[ボーランド](../Page/ボーランド.md "wikilink")のDelphiが歴史が古く、安定しており、サンプルや資料も多い。だが、DelphiはWindows(最新版はmacOSを含む)でしか動作しない。Free PascalとLazarusを用いると、日本語部分の処理を除けば、多少の修正でLinuxやmacOSなどでDelphiで書かれたプログラムをコンパイルすることができる。

特に最近の流れとして、海外では、DelphiやPascalで書かれた優れた多くのコンポーネントが、LazarusやFree Pascal向けに移植され、同じソースからコンパイルできるようになっている。

修正可能かどうか、また修正量はプログラムに依存するので、どういう部分が異なっているか、LazarusのWikiが参考になる。特に日本語については、[UTF-8](../Page/UTF-8.md "wikilink")にするという方針になっているものの、IDEまわりを含め、クロスプラットフォームでの実装が充分されていない。LazarusでASCII文字以外を扱う際は、注意して利用すべきである。Lazarus 0.9.22でも、まだ日本語を完全に扱えていない。 Lazarus 0.9.25から、公式にUTF-8をサポートされているが、全角文字が3バイトになるUTF-8でのストリング処理は、依然として容易とは言えない。

## ユーザインタフェースの利用

### LCL

Lazarusの[GUIサブシステムはLCL](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink") (Lazarus Component Library) と呼ばれ、基本的に[ウィジェット・ツールキット](../Page/ウィジェット・ツールキット.md "wikilink")関連部分を構成する[クラスをまとめたものである](../Page/クラス_\(コンピュータ\).md "wikilink")。LCLは[VCLを手本にしているが](../Page/Visual_Component_Library.md "wikilink")、100%互換ではない。

LCLは、Delphiとの互換性よりも、Windows以外のプラットフォームでのプログラミングを想定している。DelphiやWindowsに依存したVCLは手本にしつつ、幅広いクロスプラットフォームプログラミング、および、ソースが全て公開されたものを理想にしている。

### インターフェース - ウィジェット・ツールキット依存部分

Lazarusでは単に「インターフェース」と呼ぶ。事実、ウィジェット・ツールキットあたり一つのインターフェースがあるようなものである。

ウィジェット・ツールキットインターフェースに関する現状はおおむね以下の通り。

  - win32 GDI support (win32 ネイティブ) は普通に使える 状態である
  - GTK+ 1.2.x は普通に使える 状態である（macOS含む）
  - GTK+ 2.x は開発中である。国際化とフォーカシングの点で改良された
  - Qt 4 (C++) のヘッダが移植された。簡単なアプリケーションではインターフェースが利用可能である
  - wxWidgets (C++) に関しては、ヘッダの移植が終わっていない
  - Aqua（macOS ネイティブのツールキット、Objective C）プレーンなCのインターフェースだが、まだヘッダの移植が終わっていない
  - Carbon（macOS ネイティブのツールキット、Objective C）Pascal ヘッダ（[呼出規約\#Pascal](https://ja.wikipedia.org/wiki/呼出規約#Pascal "wikilink")参照）は移植され、ごく簡単なアプリケーションではインターフェースが利用可能である
  - wince（Windows CE ネイティブ）は移植作業中である

### PDAのサポート

[PDA用には](../Page/携帯情報端末.md "wikilink")、いまのところ良いクロス開発環境やRADツールがない。LazarusはPDAをサポートすべく実装作業中であり、この穴を埋めることになろう。

LCL移植作業中のプラットフォーム

  - Windows CE
  - [Qtopia](https://ja.wikipedia.org/wiki/Qtopia "wikilink") for Linux-based PDAs

将来は

  - PalmOS
  - Symbian OS

にも移植されるだろう。

### 文字コードに関する問題

日本語の場合、プラットホームによって、文字コードが違うが、LazarusではユニコードのUTF-8を標準として、各プラットホームでのインターフェースでそれをプラットホームに変換して吸収しようとしている。

しかし、この方針は最近決められたことであり、実装 0.9.22 ではそのようにはなっていない。UTF-8で今後開発が進むにつれ、日本語でもクロスプラットホームが実現できるようになるだろう。

現在のIDEのエディタでは、日本語やIME/[XIMの処理が不十分である](https://ja.wikipedia.org/wiki/X_Input_Method "wikilink")。LazarusのWindows版は、[シフトJISでの編集になっているが](../Page/Shift_JIS.md "wikilink")、FreePascalJpプロジェクトでは暫定的にIDEエディタの日本語パッチを公開している。

  - [SourceForge.jpのfreepascaljpプロジェクト](http://sourceforge.jp/projects/freepascaljp)

## 開発プロセス

Lazarusプロジェクトには多くのプログラマとテスタが集まり、良いコミュニティと高度な開発プロセスをもたらしている。問題点があればディスカッションボードで解決され、プログラマがそれを修正するパッチを投稿する。毎晩テスト前の[ビルドが作られ](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink")、ベータテスタに渡される。Lazarusの開発は大変ダイナミックである。

## データベースのサポート

Lazarusはいくつかの外部データベースをサポートしているが、それらを利用するにはデータベースに応じたパッケージをインストールする必要がある。ソースコードを用いても、フォーム上のコンポーネントを用いてもデータベースにアクセスすることができる。データ関連コンポーネントはデータのフィールドを表し、TDataSourceオブジェクトのプロパティを正しく設定することで実際に接続される。TDataSourceはテーブル（表）を表し、これにも対応するコンポーネントがある（TPSQLDatabase、TSQLiteDataSetなど）。

サポートされている外部データベースは次のとおり:

  - PostgreSQL PSQLパッケージが必要
  - [dBase](../Page/DBASE.md "wikilink")、[FoxPro](https://ja.wikipedia.org/wiki/FoxPro "wikilink") TDbfを使って、外部サーバやライブラリなしに利用することができる
  - MySQL
  - SQLite 一つの外部ライブラリとTSqliteDatasetコンポーネントでアクセスできる
  - MSSQL Zeoslibを用いる
  - InterBase / Firebird これも最新のZeoslibでサポートされる

## クロス開発

Free Pascalはクロス開発環境をサポートする。Lazarusのアプリケーションも、マイクロソフトWindows、Linux、FreeBSDで[クロスコンパイル](https://ja.wikipedia.org/wiki/クロスコンパイル "wikilink")が可能である。macOSでコンパイルしてWindows、Linux、FreeBSDで利用することもできる。macOSへのクロスコンパイルは可能になっているが、まだ一般公開されていない。

## 限界

DelphiのRADにいろいろな点で似てはいるものの、パフォーマンスや仕様上の制限がある。

  - 実行ファイルの大きさがDelphiよりいささか大きい。GNUリンカとのからみである
  - 前述のようにVCLと100%互換なわけではない。これは設計上の相違であるが、ほとんどの場合現在のLCL widgetで問題なく動作する。しかし、今存在するVCL widgetの深いリポジトリに触ろうとするなら、変換作業が必要である。まれに設計上の根本的な相違にぶつかることもあるが、ほとんどの場合は編集ですむ。ライブラリに欠けているunit（モジュール）があることと、COMサポートが実現されていないことが、LCLとVCLの互換性の上で大きな問題になってきた。
  - Delphiのコンポーネントを IDE にインストールすることができるが、面倒な変換作業が必要である。
  - 重要なライブラリ/widgetである Media ライブラリが存在しない。
      - Office との結合性
      - Datasnap
  - ネットワーク機能
      - Indy、ICS、Synapseは動作するが、Indyは100%のプラットフォームで動作している訳ではない（Linux、win32は100%。FreeBSD、macOSは動作しないかテスト前）
      - [lNet](http://wiki.lazarus.freepascal.org/index.php/LNet) は FPC　ネイティブの non-blocking variantである。
  - .NET、COMがサポートされていない。.NETをサポートしないのは設計上の問題である。
  - パッケージの動的ロードができない

## 使用条件

Lazarusは[GPLライセンスだが](../Page/GNU_General_Public_License.md "wikilink")、Lazarusで開発したソフトウェアはこのライセンスに縛られず、どのようなライセンスであってもいい。LCLはプログラムに[静的リンク](https://ja.wikipedia.org/wiki/静的リンク "wikilink")されるが、modifiedLGPLというライセンスにより、必要に応じてリンクされたバイナリを配布してもよいことになっている。

## 関連項目

  - [Free Pascal](../Page/Free_Pascal.md "wikilink")

## 外部リンク

  - [Lazarus, a RAD for FPC](http://lazarus.freepascal.org) ([Download at SourceForge.net](http://sourceforge.net/projects/lazarus/))
  - [Lazarus CCR知識ベース](http://wiki.lazarus.freepascal.org/Main_Page/ja)
      - Lazarus開発者むけドキュメントを集積している。VCLからLCLに移植する際のヘルプなどがある。
      - LCL はVCL/CLXと似たような感じでLazarusで利用するクロスプラットフォームなオープンソースライブラリである。
      - 詳細は[DelphiからLazarusへのコード変換ガイド](http://wiki.lazarus.freepascal.org/Code_Conversion_Guide/ja)
  - [Lazarusドキュメンテーション](http://wiki.lazarus.freepascal.org/Lazarus_Documentation/ja)
  - [Free Pascal Documentation](http://www.freepascal.org/docs.html)
  - [3DライブラリGLSceneを使ったLazarusアプリケーション](http://wiki.lazarus.freepascal.org/GLScene/ja)
  - [SourceForge.jpのfreepascaljpプロジェクト](http://sourceforge.jp/projects/freepascaljp)

[Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:Pascal](https://ja.wikipedia.org/wiki/Category:Pascal "wikilink")