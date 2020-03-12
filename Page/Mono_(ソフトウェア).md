> この記事は[Mono \(\)](https://ja.wikipedia.org/wiki/Mono_\(\))から翻訳されています。


**Mono**（モノ）は、[GNOME](../Page/GNOME.md "wikilink")プロジェクト創設者の[ミゲル・デ・イカザ](../Page/ミゲル・デ・イカザ.md "wikilink")が開発した、[Ecma標準に準じた](https://ja.wikipedia.org/wiki/Ecma_International "wikilink")[.NET Framework互換の環境を実現するための](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の[ソフトウェア](../Page/ソフトウェア.md "wikilink")群、またその[プロジェクト](../Page/プロジェクト.md "wikilink")名である。

2018年3月現在、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[子会社](../Page/子会社.md "wikilink")である[Xamarin](https://ja.wikipedia.org/wiki/Xamarin "wikilink")と[.NET Foundationが開発](https://ja.wikipedia.org/wiki/.NET_Foundation "wikilink")、販売、サポート業務を行っている。

[共通言語基盤](../Page/共通言語基盤.md "wikilink") (CLI) の実装や[C\#の](../Page/C_Sharp.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")などが含まれる。

## 動作プラットフォーム

Monoは[マルチプラットフォームであり](../Page/クロスプラットフォーム.md "wikilink")、[Linux](../Page/Linux.md "wikilink") ([Android](../Page/Android.md "wikilink"))、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[BSD](../Page/BSD.md "wikilink")（[OpenBSD](../Page/OpenBSD.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")）、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")、[PlayStation 3で動作する](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")\[1\]。

特定[プラットフォーム向けに特化したサブプロジェクトも存在する](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。Xamarin.iOS（旧称:MonoTouch、2013年に改称）では、[iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink")や[iPad](https://ja.wikipedia.org/wiki/iPad "wikilink")、[iPod touchといった](https://ja.wikipedia.org/wiki/iPod_touch "wikilink")[iOSでの動作をサポートしている](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")。また、MonoTouchの技術を応用し、[Mac OS Xへのネイティブ対応を行うMonoMacプロジェクトも](https://ja.wikipedia.org/wiki/macOS "wikilink")2010年に発表された。

## プロジェクトの目標

[マイクロソフト](../Page/マイクロソフト.md "wikilink")はFreeBSD、Windows、Mac OS Xで動作する[シェアードソースCLIというCLIの実装を公開したが](../Page/シェアードソース共通言語基盤.md "wikilink")、マイクロソフトの[シェアードソース](../Page/シェアードソース.md "wikilink")ライセンスは商用利用が禁止されているなど、コミュニティにとって十分とはいえない。Monoプロジェクトはプロジェクトとさまざまな点で共通した目標を掲げている。2016年6月にマイクロソフトから[MITライセンス](https://ja.wikipedia.org/wiki/MITライセンス "wikilink")に基づいた\[2\]クロスプラットフォームかつオープンソースの.NET Framework実装として**[.NET Core](https://ja.wikipedia.org/wiki/.NET_Core "wikilink")**が正式リリースされ、SSCLIは存在意義を失ったが、Monoにも.NET Coreが取り込まれるなどの波及効果が表れている\[3\]。

Monoプロジェクトの公式発表ではないが、その主導者である[ミゲル・デ・イカザ](../Page/ミゲル・デ・イカザ.md "wikilink")の言葉として、「Cでプログラミングするには人生は短すぎる」という標語が掲げられている。

## Monoランタイム

Monoランタイムは多くの[プロセッサ](../Page/プロセッサ.md "wikilink")で動作する[JITコンパイラを搭載している](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")。JITコンパイラは[アプリケーションの実行中に](../Page/アプリケーションソフトウェア.md "wikilink")[共通中間言語](../Page/共通中間言語.md "wikilink") (CLI) コードを[ネイティブコードに変換し](../Page/機械語.md "wikilink")、それらを[キャッシュする](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")。実行前にネイティブコードに変換し、キャッシュしておくことも可能である。JITコンパイラが対応するプロセッサは[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")、[x86-64](https://ja.wikipedia.org/wiki/x64 "wikilink")、[IA-64](../Page/IA-64.md "wikilink")、[SPARC](../Page/SPARC.md "wikilink")、[PowerPC](../Page/PowerPC.md "wikilink")、[ARM](../Page/ARMアーキテクチャ.md "wikilink")、[S/390](https://ja.wikipedia.org/wiki/System/390 "wikilink")（[32ビット](../Page/32ビット.md "wikilink")および[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")）、[MIPS](https://ja.wikipedia.org/wiki/MIPS "wikilink")である\[4\]。それ以外のシステムでは、ネイティブコードに変換するのではなく[インタプリタ](../Page/インタプリタ.md "wikilink")によって逐次[バイトコード](../Page/バイトコード.md "wikilink")が実行される。ほとんどの状況で、JITコンパイラによる方法は[インタプリタ](../Page/インタプリタ.md "wikilink")よりもパフォーマンスの点で勝っている。

また、マイクロソフト純正の.NET Frameworkではサポートされていない[SIMD](../Page/SIMD.md "wikilink")への対応など、Mono独自の革新的な機能の取り込みも積極的に行われている。

## 歴史

[2000年](../Page/2000年.md "wikilink")12月に[.NETドキュメントが公開されると](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、Monoプロジェクトの創始者である[ミゲル・デ・イカザ](../Page/ミゲル・デ・イカザ.md "wikilink")は.NET技術に興味を魅かれた。[バイトコード](../Page/バイトコード.md "wikilink")インタプリタを調べてみると、彼は[メタデータに関する仕様が存在しないことに気がついた](../Page/メタデータ_\(共通言語基盤\).md "wikilink")。[2001年](../Page/2001年.md "wikilink")2月、彼は.NET[メーリングリスト](../Page/メーリングリスト.md "wikilink")において不足している情報を公開するよう求め、同時に[C\#の習得のため](../Page/C_Sharp.md "wikilink")、C\#で書かれたC\#[コンパイラ](../Page/コンパイラ.md "wikilink")の開発に着手した。[2001年](../Page/2001年.md "wikilink")4月、[Ecma Internationalは不足していたファイル形式を公開し](https://ja.wikipedia.org/wiki/Ecma_International "wikilink")、デ・イカザは[GUADEC](https://ja.wikipedia.org/wiki/GUADEC "wikilink")（[2001年](../Page/2001年.md "wikilink")[4月6日](../Page/4月6日.md "wikilink")-[8日](../Page/4月8日.md "wikilink")）において彼の開発したコンパイラのデモンストレーションを行った（それは自分自身の解析が可能であった）。

[Ximian](https://ja.wikipedia.org/wiki/Ximian "wikilink")（[ノベルに買収される前のMonoの開発会社](../Page/ノベル_\(企業\).md "wikilink")）では、生産性を向上するためのツールを開発するための会議が内部的に行われていた。実現可能性の調査の結果、そのような技術は構築可能であるという結論に至り、Ximianは他のプロジェクトからスタッフを集め、Monoチームを結成した。しかしXimian内部だけで.NETと同等のものを作るには人材が不足していたため、Monoをオープンソースプロジェクトとした。これは[2001年](../Page/2001年.md "wikilink")7月19日、[オライリー](https://ja.wikipedia.org/wiki/オライリー "wikilink")カンファレンスによって発表された。

3年近く経った[2004年](../Page/2004年.md "wikilink")[6月30日](../Page/6月30日.md "wikilink")、Mono 1.0がリリースされた。

  - 2009年12月15日、Mono 2.6がリリースされた。Mono 2.6では、[Windows Communication Foundation](https://ja.wikipedia.org/wiki/Windows_Communication_Foundation "wikilink") (WCF) や [LLVM](../Page/LLVM.md "wikilink") などをサポートした。
  - Mono 2.8ではC\# 4.0がサポートされた。
  - Mono 2.8.1ではSystem.Text.Encodingにおいて[日本語](../Page/日本語.md "wikilink") ([Shift_JIS](../Page/Shift_JIS.md "wikilink")) がサポートされた。
  - Mono 3.0.0ではC\# 5.0がサポートされ、async/awaitなどが利用可能となった。
  - Mono 4.0.0ではC\# 6.0がサポートされ、またマイクロソフトが[MIT License下で公開した](../Page/MIT_License.md "wikilink").NET Coreにより一部のコンポーネントが置き換えられた。.NET2.0/3.5/4.0のサポートが終了し、[浮動小数点演算処理が最適化された](../Page/浮動小数点数.md "wikilink")\[5\]。
  - Mono 5.0.0ではC\# 7.0がサポートされた。[Visual Studioで利用されているものと同じRoslyn](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") C\#コンパイラ`csc`が追加された\[6\]。
  - Mono 5.2.0では.NET Standard 2.0のサポートが行われた。`mono`がデフォルトで[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")で動作するように変更が行われた\[7\]。
  - Mono 5.10.0では.NET 4.7.1・C\# 7.2・F\# 4.1への対応が行われた\[8\]。
  - Mono 5.12.0では[IBM AIXと](../Page/AIX.md "wikilink")[IBM iに対応した](../Page/IBM_i.md "wikilink")。Roslynベースの[VB.NETコンパイラ](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink")`vbc`が追加された\[9\]。

## プロジェクト名の由来

は[スペイン語](https://ja.wikipedia.org/wiki/スペイン語 "wikilink")で猿を意味するため、Monoのロゴには猿が描かれている。猿に関する名称は[Ximian](https://ja.wikipedia.org/wiki/Ximian "wikilink")の他のプロジェクトにも見られる。Mono FAQでは、名称の由来に関する質問に対して「我々は猿が好きなのです。」() と回答している\[10\]。

## Monoコンポーネント

Monoは大きく分けて3種類の[コンポーネント](https://ja.wikipedia.org/wiki/コンポーネント "wikilink")から構成される。

1.  中核コンポーネント
2.  Mono/Linux/GNOME開発スタック
3.  マイクロソフト互換スタック

### 中核コンポーネント

中核コンポーネントにはC\#コンパイラ、[仮想機械](../Page/仮想機械.md "wikilink")、[基本クラスライブラリ](https://ja.wikipedia.org/wiki/基本クラスライブラリ "wikilink")が含まれる。これらはEcma-334\[11\]およびEcma-335\[12\]の標準に基づいており、これによってMonoを標準準拠のオープンソースなCLI仮想機械たらしめている。

### Mono/Linux/GNOME開発スタック

Mono/Linux/GNOME開発スタックは、従来の[GNOME](../Page/GNOME.md "wikilink")や他の[フリーな](../Page/フリーソフトウェア.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")をアプリケーション開発に活用するためのツール群である。

これに含まれるものとしては、以下のものが含まれる。

  - [Gtk\#](https://ja.wikipedia.org/wiki/Gtk_Sharp "wikilink") - [GUI開発のためのライブラリ](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。
      - [Gnome\#](https://ja.wikipedia.org/wiki/Gnome_Sharp "wikilink")
  - WebBrowser - 各種レンダリングエンジンをラッピングしたコンポーネント。
      - [Gecko\#](https://ja.wikipedia.org/wiki/Gecko_Sharp "wikilink") - [Gecko](../Page/Gecko.md "wikilink")をレンダリングエンジンとして利用する[Mozilla](../Page/Mozilla.md "wikilink")ライブラリ。
      - [WebKit\#](https://ja.wikipedia.org/wiki/WebKit_Shart "wikilink") - [WebKit](../Page/WebKit.md "wikilink")をレンダリングエンジンとして利用する[WebKit](../Page/WebKit.md "wikilink")ライブラリ。

特に、Gtk\#及びGnome\#ではMonoアプリケーションを[GNOME](../Page/GNOME.md "wikilink")デスクトップにネイティブアプリケーションとして統合することができ、また最新の[MonoDevelop](https://ja.wikipedia.org/wiki/MonoDevelop "wikilink")を用いる事でVisual StudioとWindows Formsの様な[RAD開発](https://ja.wikipedia.org/wiki/RAD開発 "wikilink")も可能となった。

データベースライブラリは[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")、[SQLite](../Page/SQLite.md "wikilink")、[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")、[Firebird](../Page/Firebird.md "wikilink")、[Open Database Connectivity](../Page/Open_Database_Connectivity.md "wikilink") (ODBC)、[Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink") (MSSQL)、[Oracle](../Page/Oracle_Database.md "wikilink")、オブジェクトリレーショナルデータベース[db4o](https://ja.wikipedia.org/wiki/db4o "wikilink")など、多くのデータベースに接続することができる。

その他にも、[UNIX](../Page/UNIX.md "wikilink")統合ライブラリ、[データベース](../Page/データベース.md "wikilink")接続ライブラリ、[セキュリティスタック](../Page/コンピュータセキュリティ.md "wikilink")、[XMLスキーマ言語](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")[RelaxNG](https://ja.wikipedia.org/wiki/RelaxNG "wikilink")など、汎用的な.NET Framework向けの巨大ライブラリプロジェクトとしての側面もある。

### マイクロソフト互換スタック

マイクロソフト互換スタックは、Windowsの.NETアプリケーションを他のオペレーティングシステムで利用するための機能を提供する。例えば、[ADO.NET](../Page/ADO.NET.md "wikilink")や[ASP.NET](../Page/ASP.NET.md "wikilink")、[Windows Formsなどの実装が含まれる](../Page/Windows_Forms.md "wikilink")。

ASP.NETへの対応については、[XSPというC](https://ja.wikipedia.org/wiki/XSP_\(Webサーバ\) "wikilink")\#で作られた独自のシンプルなウェブサーバ（アプリケーションサーバ）により実現している。

Windows Formsへの対応については、[Wine](../Page/Wine.md "wikilink")との協力により開発が行われている。

2017年12月時点では、[Windows Presentation Foundation](../Page/Windows_Presentation_Foundation.md "wikilink") (WPF) を実装する予定は無いとしている\[13\]。Xamarin.Formsによって提供される[XAML開発環境は](../Page/Extensible_Application_Markup_Language.md "wikilink")、WPF/[Silverlight](https://ja.wikipedia.org/wiki/Silverlight "wikilink")/[WinRTとは互換性がない](https://ja.wikipedia.org/wiki/Windowsランタイム "wikilink")。

## 主な対応ソフト

  - [MonoDevelop](https://ja.wikipedia.org/wiki/MonoDevelop "wikilink")
  - [Beagle](../Page/Beagle.md "wikilink")
  - [Banshee](https://ja.wikipedia.org/wiki/Banshee "wikilink")

## 出典

## 関連項目

  - [GNOME](../Page/GNOME.md "wikilink")
  - [IKVM.NET](../Page/IKVM.NET.md "wikilink") - [Java仮想マシン](../Page/Java仮想マシン.md "wikilink")をMonoフレームワーク上で実現するサブプロジェクト。
  - [ノベル](https://ja.wikipedia.org/wiki/ノベル "wikilink")
  - [Ximian](https://ja.wikipedia.org/wiki/Ximian "wikilink")
  - [Xamarin](https://ja.wikipedia.org/wiki/Xamarin "wikilink")

## 外部リンク

  -

{{.NET}}

[Category:.NET_Frameworkの実装](https://ja.wikipedia.org/wiki/Category:.NET_Frameworkの実装 "wikilink") [Category:仮想機械](https://ja.wikipedia.org/wiki/Category:仮想機械 "wikilink") [Category:2004年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2004年のソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  [Supported Platforms | Mono](http://www.mono-project.com/docs/about-mono/supported-platforms/)
2.  [.NET Core とオープン ソース](https://msdn.microsoft.com/ja-jp/library/dn878908.aspx)
3.  [「Mono 4.0」リリース、オープンソース化された.NET関連コードを初めて採用 | OSDN Magazine](https://mag.osdn.jp/15/05/08/095100)
4.
5.  [Mono 4.0.0 Release Notes](http://www.mono-project.com/docs/about-mono/releases/4.0.0/)
6.
7.
8.
9.
10. ["What does the name "Mono" mean?"](http://www.mono-project.com/FAQ:_General)
11. [ECMA-334 ドキュメント （C\# 言語仕様）](http://www.ecma-international.org/publications/standards/Ecma-334.htm)
12. [ECMA-335 ドキュメント (CLI)](http://www.ecma-international.org/publications/standards/Ecma-335.htm)
13. [Compatibility - Mono](http://www.mono-project.com/Compatibility)