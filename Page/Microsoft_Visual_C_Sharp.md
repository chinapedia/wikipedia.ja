> この記事は[Microsoft Visual C Sharp](https://ja.wikipedia.org/wiki/Microsoft_Visual_C_Sharp)から翻訳されています。


**Visual C\#**は[マイクロソフト](../Page/マイクロソフト.md "wikilink")による[C\#言語処理系の実装であり](../Page/C_Sharp.md "wikilink")、[Visual Studioファミリーに含まれるC](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")\#専用の[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) である。バージョン2010まではVisual C\#単体のExpressエディション製品も存在したが、2012以降はすべてのエディションにおいてVisual Studioに統合されている。

## 概要

[C\#は](../Page/C_Sharp.md "wikilink")[.NET Frameworkによる開発を最も効率よく行える言語として](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、マイクロソフトによって開発された[仮想マシンベースの](../Page/仮想機械.md "wikilink")[高級言語](https://ja.wikipedia.org/wiki/高級言語 "wikilink")である。Visual C\#は、[WindowsでC](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")\#による開発を行うための[統合開発環境](../Page/統合開発環境.md "wikilink")である。なお、C\#で記述したコードはコンパイラによって一旦プラットフォームに依存しない[中間言語](../Page/中間言語.md "wikilink")にコンパイルされるため、Windows以外であっても動作環境が存在すればプログラムは動作する。例えば、[Xbox 360には](../Page/Xbox_360.md "wikilink")[.NET Compact Frameworkに相当するランタイムが実装されているため](../Page/.NET_Compact_Framework.md "wikilink")、[XNA](../Page/Microsoft_XNA.md "wikilink") Game Studioを使用することで、専用の開発キットを持たない一般の開発者がXbox 360で動作するゲームを開発することが可能となっている（マイクロソフトはXNA用の開発言語として、Visual C\#を使用することを推奨している）。

なお、マイクロソフト以外によるC\#コード実行基盤の例として、[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")な.NET Framework互換実装を提供する[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトの[Monoが存在する](../Page/Mono_\(ソフトウェア\).md "wikilink")。またMonoに対応したIDEとして[MonoDevelop](https://ja.wikipedia.org/wiki/MonoDevelop "wikilink")が存在する。

Visual Studio 2015では、これまで独立して存在したC\#コンパイラとVB.NETコンパイラが再設計され、Roslynと呼ばれるコンパイラレイヤーとして構築し直された。Roslynによって制御用APIが提供され、IDEとの統合などが図られている\[1\] \[2\] \[3\]。

## 開発可能なプロジェクト

Visual C\#は多数の開発プロジェクト形式に対応している。Visual C\# 2015における主な対応プロジェクトは下記である。

  - [コンソールアプリケーション](https://ja.wikipedia.org/wiki/コンソールアプリケーション "wikilink")
  - [Windows Formsアプリケーション](../Page/Windows_Forms.md "wikilink")
  - [WPFアプリケーション](../Page/Windows_Presentation_Foundation.md "wikilink")
  - [Windowsストア](https://ja.wikipedia.org/wiki/Windowsストア "wikilink")アプリ（[Windows 8.1](https://ja.wikipedia.org/wiki/Microsoft_Windows_8.1 "wikilink")/[Windows RT 8.1](https://ja.wikipedia.org/wiki/Microsoft_Windows_RT_8.1 "wikilink") 向けもしくは[UWPアプリ](https://ja.wikipedia.org/wiki/ユニバーサルWindowsプラットフォーム "wikilink")）
  - [ASP.NET](../Page/ASP.NET.md "wikilink") [Webアプリケーション](https://ja.wikipedia.org/wiki/Webアプリケーション "wikilink")
  - [Silverlightアプリケーション](../Page/Microsoft_Silverlight.md "wikilink")
  - [WCFサービスアプリケーション](../Page/Windows_Communication_Foundation.md "wikilink")
  - [Microsoft Officeアドイン](../Page/Microsoft_Office.md "wikilink")
  - [Azureモバイルサービス](https://ja.wikipedia.org/wiki/Microsoft_Azure "wikilink")
  - [Android](../Page/Android.md "wikilink")/[iOS向けアプリケーション](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")

その他にも、.NET/[WinRT対応の](https://ja.wikipedia.org/wiki/Windowsランタイム "wikilink")[クラスライブラリ](../Page/クラス_\(コンピュータ\).md "wikilink") ([DLL](https://ja.wikipedia.org/wiki/DLL "wikilink")) やコンポーネントの開発、および[単体テスト](../Page/単体テスト.md "wikilink")プロジェクトの生成にも対応している。

## 姉妹言語

  - [Visual Basic .NET](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink") (VB.NET)
    [Visual Basic](../Page/Visual_Basic.md "wikilink") 6.0 の後継として開発された、.NET Framework対応言語およびその処理系。
  - [C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")
    [C++](../Page/C++.md "wikilink")を.NET Frameworkに対応させた言語。処理系として[Visual C++が存在する](https://ja.wikipedia.org/wiki/Visual_C++ "wikilink")。
  - [F\#](../Page/F_Sharp.md "wikilink")
    .NET Framework対応の[関数型言語](../Page/関数型言語.md "wikilink")。処理系として[Visual F\#が存在する](https://ja.wikipedia.org/wiki/Microsoft_Visual_F_Sharp "wikilink")。
  - [IronPython](../Page/IronPython.md "wikilink")
    [インタラクティブシェル](https://ja.wikipedia.org/wiki/インタラクティブシェル "wikilink")機能を持った[スクリプト](../Page/スクリプト.md "wikilink")言語である[Python](../Page/Python.md "wikilink")の.NET Framworkによる実装。
    IronPython 自体は C\# で記述されている。
  - [Windows PowerShell](https://ja.wikipedia.org/wiki/Windows_PowerShell "wikilink")
    [Windows Script Host](https://ja.wikipedia.org/wiki/Windows_Script_Host "wikilink") の後継として開発された [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 対応の[インタラクティブシェル](https://ja.wikipedia.org/wiki/インタラクティブシェル "wikilink")機能を持った[スクリプト言語](../Page/スクリプト言語.md "wikilink")。

## 関連項目

  - [C\#](../Page/C_Sharp.md "wikilink")
  - [Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")
  - [SharpDevelop](../Page/SharpDevelop.md "wikilink")

## 脚注

[Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:Microsoft_Visual_Studio](https://ja.wikipedia.org/wiki/Category:Microsoft_Visual_Studio "wikilink") [Category:C_Sharp](https://ja.wikipedia.org/wiki/Category:C_Sharp "wikilink")

1.  [働くプログラマ - Roslyn 登場](https://msdn.microsoft.com/ja-jp/magazine/dn818501.aspx)
2.  [オープン ソース化の旅: Roslyn の 1 年目の試行錯誤とその成果 - Visual Studio 日本チーム ブログ - Site Home - MSDN Blogs](http://blogs.msdn.com/b/visualstudio_jpn/archive/2015/04/06/a-journey-through-open-source-the-trials-and-triumphs-in-roslyn-s-first-year-of-open-source.aspx)
3.  [Visual Studio 2015の新機能“Roslyn”とは - Build Insider](http://www.buildinsider.net/enterprise/roslyn/01)