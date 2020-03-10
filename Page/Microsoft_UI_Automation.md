> この記事は[Microsoft UI Automation](https://ja.wikipedia.org/wiki/Microsoft_UI_Automation)から翻訳されています。


**[Microsoft](https://ja.wikipedia.org/wiki/Microsoft "wikilink") UI Automation (UIA)** (マイクロソフト・ユーアイ・オートメーション) は他のアプリケーションのユーザインターフェイス (UI) 要素を識別して操作するための[アプリケーションプログラミングインターフェイス](https://ja.wikipedia.org/wiki/アプリケーションプログラミングインターフェイス "wikilink") (API)である\[1\]\[2\]。

UIA は[ユーザインターフェイス](https://ja.wikipedia.org/wiki/ユーザインターフェイス "wikilink")の[アクセシビリティの提供を目標としており](../Page/コンピュータアクセシビリティ.md "wikilink")、 の後継である。また、[グラフィカルユーザインターフェイス](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェイス "wikilink")(GUI)の[テスト自動化](https://ja.wikipedia.org/wiki/テスト自動化 "wikilink")を容易にし、多くのテスト自動化ツールが基礎にするエンジンでもある。[RPAツールも](https://ja.wikipedia.org/wiki/ロボティック・プロセス・オートメーション "wikilink")[ビジネスプロセス](../Page/ビジネスプロセス.md "wikilink")で使われるアプリケーションの自動化に利用している。 UIAのプロパティプロバイダは [Win32](https://ja.wikipedia.org/wiki/Win32 "wikilink") と [.NET](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") のプログラムもサポートする。

UIAの最新仕様は Microsoft UI Automation [Community Promise Specification](https://ja.wikipedia.org/wiki/Microsoft_Open_Specification_Promise "wikilink") の一部となっている。マイクロソフトは Microsoft Windows プラットフォーム以外への移植はデザイン目標の一つであると主張しており、[Mono](../Page/Mono_\(ソフトウェア\).md "wikilink") にも移植された\[3\]。

## 歴史

[2005年](../Page/2005年.md "wikilink")に、マイクロソフトは  フレームワークの後継として UIA をリリースした。

[マネージド](https://ja.wikipedia.org/wiki/マネージドコード "wikilink") UI Automation APIは[.NET Framework 3.0の一部としてリリースされた](https://ja.wikipedia.org/wiki/.NET_Framework_3.0 "wikilink")。 ネイティブ UI Automation API (プロバイダ)は[Windows Vista と Windows Server 2008 SDK](../Page/Microsoft_Windows_SDK.md "wikilink") に含まれており、.NET Frameworkと一緒にも配布された。

UIA は Windows Automation API 3.0 の一部として Windows 7 に同梱され、個別ダウンロードとして Windows XP、Windows Vista、Windows Server 2003/2008 向けに提供された\[4\]。

## 目的

MSAA の後継として UIA では以下のことを目指している。

  - 対象となるアプリケーションの[プロセス](../Page/プロセス.md "wikilink")にクライアントを[フックしなくても](../Page/フック_\(プログラミング\).md "wikilink")、クライアントの効率的なパフォーマンスを実現する。
  - UI について、より多くの情報を提供する。
  - MSAA と共存し、利用するがMSAAに存在した課題は継承しない。
  - MSAA に代わる単純な実装を提供する。

## 技術的概要

## 利用できるオペレーティングシステム

UIA は当初 Windows Vista と Windows Server 2008 で利用でき、その後 Windows XP と Windows Server 2003 でも .NET Framework 3.0 の一部として利用可能となった。[Windows 7](https://ja.wikipedia.org/wiki/Windows_7 "wikilink") 等、以降のすべての Windows バージョンに統合された\[5\]。

Windows プラットフォーム以外には、Olive プロジェクト (.NET Framework のサポートを約束している　Mono coreのアドオンライブラリ一式) が WPF (`PresentationFramework` および `WindowsBase`) と UI Automation のサブセットを同梱した\[6\]。

ノベルによる Mono アクセシビリティプロジェクトは Mono フレームワークを対象とした UIA プロバイダとクライアントの実装である。加えて、このプロジェクトは Accessibility Toolkit (ATK) for Linux assistive technologies (ATs) との橋渡しとなっている。ノベルは UIA-based ATs との橋渡しを行うことで、ATK を実装するアプリケーションと関われるようにしている\[7\]。

## 関連テクノロジと相互運用

  - **[Microsoft Active Accessibility](https://ja.wikipedia.org/wiki/Microsoft_Active_Accessibility "wikilink") (MSAA)**: UIA は MSAA の後継である。しかし MSAA に依存するアプリケーションがまだ存在するため、UIA アプリケーションと MSAA アプリケーションの橋渡しが行われ、2つの API の間で情報共有が可能である。MSAA-to-UIA プロキシと UIA-to-MSAA ブリッジが開発された。前者は MSAA の情報を元に UIA クライアント API で利用可能とするコンポーネントである。後者は MSAA を使うクライアントアプリケーションが UIA を実装するアプリケーションにアクセスできるようにする仕組みである\[8\]。
  - [Accessible Rich Internet Applications](https://ja.wikipedia.org/wiki/Accessible_Rich_Internet_Applications "wikilink") **(ARIA)**: UIA の `AriaRole` および `AriaProperties` プロパティは HTML 要素 (ウェブブラウザによりオートメーション要素としてアクセス可能となる)に対応する ARIA 属性値へのアクセスを可能とする。ARIA 属性から UIA への一般的なマッピングも利用できる\[9\]。
  - **Windows Automation API**: Windows 7 より、マイクロソフトはアクセシビリティテクノロジーを Windows Automation API と呼ばれるフレームワークにパッケージした。MSAA も UIA もこのフレームワークの一部となった。旧バージョンの Windows については KB971513 を参照\[10\]。
  - **Mono アクセシビリティプロジェクト**: [2007年](../Page/2007年.md "wikilink")[11月7日](../Page/11月7日.md "wikilink")にマイクロソフトと[ノベルは相互運用性に関する合意完了後](https://ja.wikipedia.org/wiki/Novell "wikilink")、アクセシビリティ機能の拡張についてアナウンスを行った\[11\]\[12\]。特に、UIA フレームワークが [Linux Accessibility Toolkit](https://ja.wikipedia.org/wiki/Accessibility_Toolkit "wikilink") (ATK) 等の既存の [Linux](../Page/Linux.md "wikilink") アクセシビリティプロジェクトと一緒に動作するよう、ノベルがオープンソースのアダプタを開発し、[SUSE](https://ja.wikipedia.org/wiki/SUSE_Linux "wikilink") [Linux Enterprise Desktop](../Page/SUSE_Linux_Enterprise_Desktop.md "wikilink")、[Red Hat](https://ja.wikipedia.org/wiki/Red_Hat "wikilink") [Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink")、[Ubuntu Linuxと一緒にリリースされることがアナウンスされた](../Page/Ubuntu.md "wikilink")。これにより UIA は最終的にクロスプラットフォームとなった。

## 脚注

## 関連項目

  - [UI Automation Control Types](https://docs.microsoft.com/ja-jp/windows/win32/winauto/uiauto-supportinguiautocontroltypes)
  - [UI Automation Control Patterns](https://docs.microsoft.com/ja-jp/windows/win32/winauto/uiauto-implementinguiautocontrolpatterns)
  - [UI Automation Control Properties](https://docs.microsoft.com/ja-jp/windows/win32/winauto/uiauto-propertiesoverview)
  - [UI Automation Events](https://docs.microsoft.com/ja-jp/windows/win32/winauto/uiauto-eventsoverview)

## 外部リンク

  - [UIオートメーションの概要](https://docs.microsoft.com/ja-jp/dotnet/framework/ui-automation/ui-automation-overvie)
  - [UIオートメーションのススメ](https://docs.microsoft.com/ja-jp/archive/blogs/japan_platform_sdkwindows_sdk_support_team_blog/ui-automation)
  - [UI Automation Verify (UIA Verify) Test Automation Framework](http://www.codeplex.com/UIAutomationVerify)
  - [UI Automation PowerShell Extensions](http://uiautomation.codeplex.com)
  - [TestStack/White](https://white.codeplex.com)

[Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:アクセシビリティAPI](https://ja.wikipedia.org/wiki/Category:アクセシビリティAPI "wikilink")

1.  Darryl K. Taft: [Microsoft Promotes Cross-Platform Accessibility Tech](http://www.eweek.com/article2/0,1895,1892089,00.asp), EWeek (2005-11-28), accessed 2007-02-07.
2.  Microsoft: [Microsoft's New Accessibility Model To Be Offered as Cross-Platform Solution for Industry](http://www.microsoft.com/enable/at/uia.aspx), accessed 2007-02-06.
3.  Microsoft Developer Network: [UI Automation Specification and Community Promise](http://msdn.microsoft.com/en-us/windows/bb892133)
4.  [Description of the Windows Automation API](http://support.microsoft.com/kb/971513/)
5.  Microsoft: \[<http://msdn.microsoft.com/en-us/library/ee684076(v=vs.85>).aspx UI Automation Overview\], accessed 2007-02-07.
6.  Mono: [Olive](http://www.mono-project.com/Olive).
7.  Miguel de Icaza and Philippe Cohen: [Mono, Mainsoft and Cross-Platform Enterprise Development](http://opensource.sys-con.com/read/318852.htm), Enterprise Open Source Magazine (2007-01-14), accessed 2007-02-07.
8.  Microsoft Developer Network (MSDN): \[<http://msdn.microsoft.com/en-us/library/ee671585(v=vs.85>).aspx Microsoft, UI Automation and Microsoft Active Accessibility\], accessed 2007-02-07.
9.
10. KB971513: [Windows Automation API download](http://support.microsoft.com/kb/971513)
11. Microsoft: [Microsoft and Novell Celebrate Year of Interoperability, Expand Collaboration Agreement](http://www.microsoft.com/presspass/press/2007/nov07/11-07MSNovell1YearPR.mspx).
12. [Mono Accessibility Project Homepage](http://www.mono-project.com/Accessibility).