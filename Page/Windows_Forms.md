> この記事は[Windows Forms](https://ja.wikipedia.org/wiki/Windows_Forms)から翻訳されています。


**Windows Forms**は[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[.NET Frameworkに含まれる](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[グラフィカルユーザーインターフェイス](https://ja.wikipedia.org/wiki/グラフィカルユーザーインターフェイス "wikilink")[APIの名称である](https://ja.wikipedia.org/wiki/アプリケーションプログラミングインターフェイス "wikilink")。日本語版の公式ドキュメント（旧[MSDNライブラリ](../Page/Microsoft_Developer_Network.md "wikilink")）では「Windowsフォーム」と表記されている\[1\]。「WinForms」と略記されることもある\[2\]。

## 概要

Windows Formsは[Windows API](../Page/Windows_API.md "wikilink")（[GDI](../Page/Graphics_Device_Interface.md "wikilink")/[GDI+](https://ja.wikipedia.org/wiki/Graphics_Device_Interface#GDI+ "wikilink")）を[マネージコード](../Page/マネージコード.md "wikilink")でラップし、[Windowsの](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[ユーザーインターフェイス](https://ja.wikipedia.org/wiki/ユーザーインターフェイス "wikilink")要素へのアクセスを提供するフレームワークである。従来から[Visual C++用に提供されていた](https://ja.wikipedia.org/wiki/Visual_C++ "wikilink")、複雑なネイティブ[C++](../Page/C++.md "wikilink")ベースの[MFCや](../Page/Microsoft_Foundation_Class.md "wikilink")、旧[Visual Basic](../Page/Visual_Basic.md "wikilink")（VB6）のフォームにとって代わるものとされる一方で、Windows Formsは[MVCモデルを提供していない](../Page/Model_View_Controller.md "wikilink")。また、[シェル](../Page/シェル.md "wikilink")関連など一部のAPIに関してはラッパーが存在しないので、それらをWindows Formsで利用するためには[C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")言語でラッパーアセンブリを作成するか、あるいは[P/Invoke](https://ja.wikipedia.org/wiki/P/Invoke "wikilink")などの手法を用いる必要がある。そのほか、MFCアプリケーションからWindows Formsコントロールを利用するなどのシナリオを想定した相互運用機能も用意されている\[3\]\[4\]。

Windows Formsアプリケーション開発に[Visual Studioを利用することで](https://ja.wikipedia.org/wiki/Visual_Studio "wikilink")、.NET以前の[Visual Basicや](../Page/Visual_Basic.md "wikilink")[Delphi](../Page/Delphi.md "wikilink")のように、GUI（フォームデザイナー）で簡単かつ効率的に画面作成やGUI部品の詳細な設定を行なうことができる（[RAD](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")）。これは、GUI部品の簡単な配置や簡単な設定までしかできないWin32/MFCのダイアログ エディターとは大きく異なる。作成したウィンドウ情報は、リソースファイルに変換されるのではなく、Visual Studio [IDEによって直接](../Page/統合開発環境.md "wikilink")[C\#や](../Page/C_Sharp.md "wikilink")[Visual Basic .NETなどのソースコードに変換して出力される](../Page/Visual_Basic_.NET.md "wikilink")（コード ビハインド）。マネージ言語は[IDEとの親和性が高く](../Page/統合開発環境.md "wikilink")、Windows Formsによって生産性の高いGUIアプリケーション開発環境が提供される。

なお、Windows Formsのターゲット環境はデスクトップ アプリケーションであり、ブラウザで動作するWebアプリケーションを開発するには[ASP.NET](../Page/ASP.NET.md "wikilink")などを利用することになる。

## コード例

[C\#によるWindows](../Page/C_Sharp.md "wikilink") Formsを使用した[Hello worldプログラムの例である](../Page/Hello_world.md "wikilink")。ここで、`System.Windows.Forms`がWindows Formsの名前空間を表す。

``` csharp
using System;
using System.Windows.Forms;

public class HelloWorld
{
    [STAThread]
    public static void Main()
    {
        Form form = new Form();
        form.Text = "Hello world!";
        Application.Run(form);
    }
}
```

## 互換実装

マイクロソフトによるWindows専用の.NET Frameworkベース公式実装のほか、[Monoによる互換実装](../Page/Mono_\(ソフトウェア\).md "wikilink")（通称WinForms）が存在する\[5\]。MonoのWinFormsは.NET 1.1/2.0互換の実装を提供するが、2017年現在の開発状況はメンテナンスフェイズとなっている。

## 課題と将来性

Windows Formsは.NET Framework 1.0のリリースとともに登場したが、.NET 2.0で機能追加\[6\]や仕様変更がなされた後は大きな変化がない。後発のデスクトップアプリケーションフレームワークである[WPFに比べると](../Page/Windows_Presentation_Foundation.md "wikilink")、[マルチタッチ](https://ja.wikipedia.org/wiki/マルチタッチ "wikilink")やDPI Aware\[7\]\[8\]などに標準で対応していないなど、最新の技術動向は反映されにくい傾向にある。.NET 4.5.1, .NET 4.5.2, .NET 4.6, .NET 4.7ではそれぞれ高DPI環境下でのWindows Formsコントロールのリサイズに関する機能が徐々に拡張・改善されているが、既定ではなく[オプトイン](https://ja.wikipedia.org/wiki/オプトイン "wikilink")である\[9\]\[10\]。

また、Visual C++にはバージョン2010までWindows Formsのアプリケーションプロジェクトテンプレートが存在していたが、バージョン2012以降は削除されている。もともとVisual C++においてマネージコンポーネントであるWindows Formsを扱うにはC++/CLI言語を使用する必要があったが、C++/CLIはマネージコードとアンマネージコードの相互運用を行なう[グルー言語](../Page/グルー言語.md "wikilink")用途としてのみ使用することが推奨されている\[11\]。

しかし、後継となるWPFはMFCやWindows Formsの完全なスーパーセットではなく、一部は同等機能が用意されていない。Win32/MFCやWindows Formsで作成されたコード資産を再利用するため、WPFアプリケーションでもWin32/MFCやWindows Formsとの連携を行なうシナリオを想定した相互運用機能が用意されている\[12\]\[13\]\[14\]\[15\]。

[.NET Core](https://ja.wikipedia.org/wiki/.NET_Core "wikilink") 3.0では、Windows版限定ではあるがWPFとともにWindows Formsが実装された\[16\]。[.NET Frameworkのメジャーアップデートは](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")4.8で最後となるが、メンテナンスは継続される。

## 脚注

## 関連項目

  - [基本クラスライブラリ](https://ja.wikipedia.org/wiki/基本クラスライブラリ "wikilink")
  - [Visual Component Library](../Page/Visual_Component_Library.md "wikilink")
  - [Windows Presentation Foundation](../Page/Windows_Presentation_Foundation.md "wikilink")

{{.NET}}

[Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink") [Category:ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/Category:ウィジェット・ツールキット "wikilink")

1.  \[<https://docs.microsoft.com/ja-jp/previous-versions/visualstudio/visual-studio-2008/dd30h2yb(v=vs.90>) Windows フォーム | Microsoft Docs\]
2.  [Windowsフォーム開発に最適なコンポーネントセット - ComponentOne Studio for WinForms | グレープシティ コンポーネント製品](http://c1.grapecity.com/superproducts/studiowinforms/)
3.  [Using a Windows Form User Control in MFC | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/dotnet/using-a-windows-form-user-control-in-mfc)
4.  \[<https://docs.microsoft.com/ja-jp/previous-versions/visualstudio/visual-studio-2008/ahdd1h97(v=vs.90>) MFC での Windows フォーム ユーザー コントロールの使用 | Microsoft Docs\]
5.  [WinForms | Mono](http://www.mono-project.com/docs/gui/winforms/)
6.  [＠IT：特集 .NET Framework 2.0のWindowsフォーム新機能（前編）](http://www.atmarkit.co.jp/fdotnet/special/win20review01/win20review01_01.html)
7.  [アプリの高DPI(High DPI)対応について 第2回 ～ アプリケーションの高DPIへの対応レベル ～ – 田中達彦のブログ](https://blogs.msdn.microsoft.com/ttanaka/2014/07/24/dpihigh-dpi-2-12398/)
8.  [Windows フォーム アプリの DPI Aware への変更 言語: XML](https://code.msdn.microsoft.com/windowsapps/Windows-DPI-Aware-e758cbbb)
9.  [アプリの高DPI(High DPI)対応について 第1回 ～ 高DPIとは ～ – 田中達彦のブログ](https://blogs.msdn.microsoft.com/ttanaka/2014/07/16/dpihigh-dpi-1-dpi/)
10. [What's new in the .NET Framework | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/framework/whats-new/index)
11. [Visual Studio 2012、2013 で Visual C++ の Windows フォーム アプリケーション テンプレートが削除され、新規に作成できない](https://support.microsoft.com/ja-jp/kb/3001686)
12. [WPF and Win32 Interoperation | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation)
13. [Walkthrough: Hosting a Windows Forms Control in WPF | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/framework/wpf/advanced/walkthrough-hosting-a-windows-forms-control-in-wpf)
14. \[<https://docs.microsoft.com/ja-jp/previous-versions/dotnet/netframework-3.5/ms742522(v=vs.90>) WPF と Win32 の相互運用性に関する概要 | Microsoft Docs\]
15. \[<https://docs.microsoft.com/ja-jp/previous-versions/dotnet/netframework-3.5/ms751761(v=vs.90>) チュートリアル : Windows Presentation Foundation での Windows フォーム コントロールのホスト | Microsoft Docs\]
16. [Windows Forms アプリを .NET Core 3.0 に移植する - .NET Core | Microsoft Docs](https://docs.microsoft.com/ja-jp/dotnet/core/porting/winforms)