> この記事は[Multiple Document Interface](https://ja.wikipedia.org/wiki/Multiple_Document_Interface)から翻訳されています。


**MDI**、**Multiple Document Interface** （マルチ・ドキュメント・インタフェース）とは親[ウィンドウ](../Page/ウィンドウ.md "wikilink")内に複数の子ウィンドウを表示して管理する[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")方式である。従来の[SDI方式ではドキュメントごとにアプリケーションウィンドウを必要とするため](https://ja.wikipedia.org/wiki/Single_Document_Interface "wikilink")、複数のドキュメントを開く際はそれぞれにアプリケーションプロセスを起動しなければならず、メモリやリソースの消費が増えるという問題を解決するために開発された。SDIでは1つのドキュメントに対し、1つのアプリケーションウィンドウ（1つのトップレベルウィンドウ）を使用するが、MDIでは1つのドキュメントに対し、1つの子ウィンドウを使用する\[1\]。また、MDIのドキュメントウィンドウは親ウィンドウにロックおよびクリッピングされる。

既存のSDI形式の[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")をMDI化するには、設計に変更を加える必要がある。

[Microsoft OfficeはかつてSDIからMDI化したが](../Page/Microsoft_Office.md "wikilink")、その後は再びSDIが標準となり、MDIはオプションとしてサポートされるようになった。さらに後継のバージョンでは、SDIのみがサポートされるようになっている（厳密に言うとSDIではなく後述のMTIに相当する）。

## 問題点

一般的にMDIは開かれたウィンドウの管理が問題だとされる。SDIアプリケーションであれば[タスクバー](../Page/タスクバー.md "wikilink")などで開かれたウィンドウの情報を一覧できるが、MDIでは通常、子ウィンドウの一覧を確認するためにユーザーがメニューなどからウィンドウ一覧表示機能を実行しなければならない。そのためのMDIアプリケーションはこの問題を解決するため[タブ機能やタスクバーへの一覧表示機能を装備することでこの問題を解決するようになった](../Page/タブ_\(GUI\).md "wikilink")。多くのMDIアプリケーションは親ウインドウとの結合・子ウインドウ分離を一括で管理される。1つをMDI化しようとすれば全てがMDI化され、ひとつを親ウインドウと結合しようとすれば全てが親ウインドウと結合される。分離・結合を個別に管理するのは[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")などごく一部のアプリケーションのみである。MDIはタブ方式のアプリケーションと一緒くたにされる場合もあるようであり、実際タブ方式のアプリケーションと同じように使えるアプリケーションもあるが、通常タブ方式でウィンドウを管理するアプリケーションは個々を子ウィンドウ化してその大きさを変更するようなことはできない。[Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") 2010以降\[2\]\[3\]や、[タブブラウザ](../Page/タブブラウザ.md "wikilink")では、ドキュメント/ページを表示しているタブを切り離して独立ウィンドウ化することができる。

[マイクロソフト](../Page/マイクロソフト.md "wikilink")はMDI形式のアプリケーションを推奨していない\[4\]。また、[Microsoft Foundation Class](../Page/Microsoft_Foundation_Class.md "wikilink") (MFC) \[5\]や[Windows Forms](../Page/Windows_Forms.md "wikilink")\[6\]ではMDIがサポートされているものの、後発の[Windows Presentation Foundation](../Page/Windows_Presentation_Foundation.md "wikilink") (WPF) や[Windowsランタイム](https://ja.wikipedia.org/wiki/Windowsランタイム "wikilink")ではMDIがサポートされていない。

なお、タブ方式のインタフェースはTabbed Document Interface (TDI) と呼ばれる。

また、[SDIに似ているが](https://ja.wikipedia.org/wiki/Single_Document_Interface "wikilink")、1つのアプリケーション[プロセス](../Page/プロセス.md "wikilink")中で、親ウィンドウを持たない複数のトップレベルウィンドウを表示する形態をMultiple Top-level Interface (MTI) という。[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")は[Classic Mac OSから伝統的にこのスタイルのみを用いる](../Page/Classic_Mac_OS.md "wikilink")。MS Officeの新しいSDIもこの形式である。ドキュメントごとにプロセスを起動しないので、メモリやリソースの消費を抑えることができる。

## MDIを使用したアプリケーションの例

  - [Adobe Photoshop](../Page/Adobe_Photoshop.md "wikilink") (CS4以降はMDIではなくTDIが標準となった)
  - [Eudora](../Page/Eudora.md "wikilink")
  - [Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")（.NET以降はMDI/TDIが選択できるようになった\[7\]）
  - [Microsoft Word](../Page/Microsoft_Word.md "wikilink")（Word 2010までは「詳細設定」の「すべてのウィンドウをタスク バーに表示する」にてSDI/MDIの切り替えができたが、2013以降はSDIのみとなった）
  - [Microsoft Excel](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")（Excel 2010まで\[8\]）
  - [一太郎](../Page/一太郎.md "wikilink")
  - [Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")
  - [Sleipnir](../Page/Sleipnir.md "wikilink")
  - [PSPad](https://ja.wikipedia.org/wiki/PSPad "wikilink")

## 脚注

## 関連項目

  - [グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")
  - [Single Document Interface](https://ja.wikipedia.org/wiki/Single_Document_Interface "wikilink")
  - [タブ](../Page/タブ_\(GUI\).md "wikilink")
  - [タブブラウザ](../Page/タブブラウザ.md "wikilink")

[Category:ドキュメント・インタフェース](https://ja.wikipedia.org/wiki/Category:ドキュメント・インタフェース "wikilink") [Category:ユーザインタフェース技術](https://ja.wikipedia.org/wiki/Category:ユーザインタフェース技術 "wikilink") [Category:グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/Category:グラフィカルユーザインタフェース "wikilink")

1.  [MFCにおいて](../Page/Microsoft_Foundation_Class.md "wikilink")、1つのドキュメントに対して、複数のビューウィンドウを表示する「マルチビュー」という方式も存在するが、SDI/MDIの分類とは異なる。
2.  \[<https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/dd465268(v=vs.100>) What's New in the Visual Studio 2010 Editor | Microsoft Docs\]
3.  \[<https://docs.microsoft.com/ja-jp/previous-versions/visualstudio/visual-studio-2010/dd465268(v=vs.100>) Visual Studio 2010 エディターの新機能 | Microsoft Docs\]
4.  \[<https://docs.microsoft.com/ja-jp/previous-versions/technical-document/ms997581(v=msdn.10>) Microsoft Windows ユーザー エクスペリエンス FAQ | Microsoft Docs\]
5.  [Managing MDI Child Windows | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/mfc/managing-mdi-child-windows)
6.  [Multiple-Document Interface (MDI) Applications - Windows Forms | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/framework/winforms/advanced/multiple-document-interface-mdi-applications)
7.  \[<https://docs.microsoft.com/ja-jp/previous-versions/msdn/architecture-center/cc440057(v=vs.71>) Visual Studio .NET の紹介 | Microsoft Docs\]
8.  [Excel 2013 からのウィンドウ管理方法変更について – シングル ドキュメント インターフェイス (SDI) – Japan Office Developer Support Blog](https://blogs.msdn.microsoft.com/office_client_development_support_blog/2016/12/19/excel2013-changes-to-sdi/)