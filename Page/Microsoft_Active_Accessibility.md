> この記事は[Microsoft Active Accessibility](https://ja.wikipedia.org/wiki/Microsoft_Active_Accessibility)から翻訳されています。


**Microsoft Active Accessibility** (**MSAA**) は、ユーザーインターフェイスのアクセシビリティのための[アプリケーションプログラミングインターフェイス](../Page/アプリケーションプログラミングインタフェース.md "wikilink") （API）である。 MSAAは、1997年にMicrosoft [Windows 95プラットフォームの追加機能として導入された](../Page/Microsoft_Windows_95.md "wikilink")。 MSAAにより、 [支援技術](https://ja.wikipedia.org/wiki/支援技術 "wikilink") （AT）製品がアプリケーション（またはオペレーティングシステム）の標準およびカスタム[ユーザーインターフェイス](../Page/ユーザインタフェース.md "wikilink") （UI）要素とやり取りし、アプリケーションのUI要素にアクセス、識別、および操作できるようになる。 支援技術製品はMSAA対応のアプリケーションと連携して、身体的または認知的困難を持つ障碍者が、対応アプリケーションをより使いやすくするよう支援する。 支援技術製品の例としては、視力障害のあるユーザー向けのスクリーンリーダー、身体的障害のあるユーザー向けのスクリーンキーボード、聴覚障害のあるユーザー向けのナレーターなどがある。 MSAAは、自動テストツール、[RPA](https://ja.wikipedia.org/wiki/RPA "wikilink")やコンピュータベースのトレーニングアプリケーションでも使用される。

MSAAの最新版は、[Microsoft UI Automation](../Page/Microsoft_UI_Automation.md "wikilink") Community Promise仕様の一部に含まれる。

## 歴史

Active Accessibilityは当初*OLE Accessibility*\[1\]と呼ばれ、これは`oleacc.dll`といったバイナリファイルや、定義と宣言を含むヘッダーファイル`oleacc.h`などの名前に反映されている。 1996年3月にはマイクロソフトはActiveXのブランド名を前面に押し出す施策の一環として、OLE AccessibilityはActiveX Accessibility（AXAとも呼ばれる）に改名され、1996年3月にサンフランシスコで開催されたMicrosoft Professional Developers Conferenceで発表された。 その後、ActiveXブランドはインターネット固有のテクノロジーに集約され、ActiveX AccessibilityはActive Accessibility、短縮名MSAAとなった。

MSAAは、1997年4月にMicrosoft Active Accessibility Software Developers Kit（SDK）バージョン1.0の一部として提供された。 SDKには、ドキュメント、プログラミングライブラリ、サンプルソースコード、および再配布可能キット（RDK）が含まれており、支援技術の提供ベンダーが製品に含めることができた。 RDKには、Microsoft [Windows 95用の更新されたオペレーティングシステムコンポーネントが含まれていた](../Page/Microsoft_Windows_95.md "wikilink")。 [Windows 98および](../Page/Microsoft_Windows_98.md "wikilink")[Windows NT 4.0](https://ja.wikipedia.org/wiki/Microsoft_Windows_NT_4.0 "wikilink") [Service Pack](../Page/サービスパック.md "wikilink") 4以降、MSAAはWindowsプラットフォームのすべてのバージョンに組み込まれており、その後定期的に更新されている。

Windowsと支援技術アプリケーションのプログラムによる連携は、これまでMSAAを通じて行われてきた。 ただし、新しいアプリケーションでは、 [Windows Vistaおよび](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")[NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 3.0で導入された[Microsoft UI Automation](../Page/Microsoft_UI_Automation.md "wikilink") (UIA) を使用するようになった[。](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")

## バージョン履歴

今までに次のActive Accessibilityバージョンがリリースされた\[2\]。

| バージョン | 説明                                                                                                                                                                                                                                                                     |
| ----- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1.0   | Windows 95用の追加機能として最初のバージョンをリリース。 RDKは、英語版OSでのみサポートされた。（1997）                                                                                                                                                                                                          |
| 1.1   | [Windows 98に同梱された](../Page/Microsoft_Windows_98.md "wikilink")。                                                                                                                                                                                                        |
| 1.2.x | 英語版Windowsとローカライズ版Windowsの両方で利用可能になったMSAAの最初のバージョン。 （1998）                                                                                                                                                                                                             |
| 1.3.x | より多くの言語でサポートされた。言語リソースを格納するサテライト[DLL](../Page/ダイナミックリンクライブラリ.md "wikilink") (oleaccrc.dll) が導入された。 その後、Windows NT 4.0 Service Pack 6以降、Windows 98、Windows 2000、およびWindows Meに統合された。 （1999）                                                                             |
| 2.0   | MSAAの最初のメジャーバージョンアップ。Dynamics AnnotationとMSAA Textのサポートが追加された。 このバージョンは[Windows XPに統合された](../Page/Microsoft_Windows_XP.md "wikilink")。 以降のバージョンのWindowsには、MSAAフレームワークにマイナーな改訂が行われた。 バージョン2.0の再配布可能キットは、2003年に古いプラットフォーム（Windows 95、98、2000、Me、NT）で利用可能になった。（2000–2008） |
| 3.0   | MSAAおよびUI Automation (UIA) はWindows プラットフォームアクセシビリティAPIであるWindows Automation API 3.0の一部となった。 Windows Automation APIはWindows 7に含まれ、Windows VistaおよびXPでも利用可能となった。（2009）                                                                                                  |

## 目的

MSAAは、基盤となるオペレーティングシステムやアプリケーションと、支援技術製品の間の、シームレスな通信メカニズムを可能にするために開発された。

MSAAのプログラム上の目標は、Windowsコントロールが、名前、画面上の場所、コントロールの種類などの基本情報、および表示/非表示や、有効/無効の状態、選択済みなどの状態情報を公開できるようにすることである。

## 技術的概要

## 利用できるオペレーティングシステム

MSAAは当初、Windows 95の追加機能としてリリースされた。 以降のすべてのバージョンのWindowsに同梱されている。

## 関連テクノロジ

**[Microsoft UI Automation](../Page/Microsoft_UI_Automation.md "wikilink") （UIA）** ：MSAAの後継は、UI Automation (UIA) である。しかし MSAA に依存するアプリケーションがまだ存在するため、UIA アプリケーションと MSAA アプリケーションの橋渡しが行われ、2つの API の間で情報共有が可能である。MSAA-to-UIA プロキシと UIA-to-MSAA ブリッジが開発された。前者は MSAA の情報を元に UIA クライアント API で利用可能とするコンポーネントである。後者は MSAA を使うクライアントアプリケーションが UIA を実装するアプリケーションにアクセスできるようにする仕組みである。

**[Accessible Rich Internet Applications](https://ja.wikipedia.org/wiki/Accessible_Rich_Internet_Applications "wikilink")** （WAI-ARIA）：ARIA 属性から UIA への一般的なマッピングも利用できる\[3\]。

**[IAccessible2](https://ja.wikipedia.org/wiki/IAccessible2 "wikilink")** ：MSAAの機能をベースにしている。 IAccessible2はMSAAの実装活用し、追加機能を提供する。

**Windows Automation API** ：Windows 7 より、マイクロソフトはアクセシビリティテクノロジーを Windows Automation API と呼ばれるフレームワークにパッケージした。MSAA も UIA もこのフレームワークの一部となった。

## Microsoft Active Accessibilityの実装

Active Accessibilityは、Windows 95以降のすべてのバージョンで開発者が利用できる。 最初に導入されて以来、MSAAは、Microsoft [Internet Explorer](../Page/Internet_Explorer.md "wikilink")、[Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")、[Microsoft Officeなど](../Page/Microsoft_Office.md "wikilink")、多くのビジネスおよびコンシューマアプリケーションのUIへのプログラムによるアクセスを行う方法として使用された。 スクリーンリーダー、画面拡大鏡、[重度障害者用意思伝達装置](../Page/重度障害者用意思伝達装置.md "wikilink")などのアクセシビリティツールに加えて、このテクノロジーはQuickTest Pro、Functional Tester、SilkTestなどの[テスト自動化](https://ja.wikipedia.org/wiki/テスト自動化 "wikilink")ソフトウェアでも使用されている。

MSAAを実装しているアプリケーションおよび支援技術製品は、マイクロソフトアクセシビリティサイトまたは支援技術情報Webサイトで検索できる\[4\] \[5\] \[6\]。

## 参考文献

<references />

## 外部リンク

  -
  - [アクセシビリティに対するマイクロソフトの取り組みの歴史](http://www.microsoft.com/enable/microsoft/history.aspx)

  - [UIアクセシビリティチェック](http://www.codeplex.com/AccCheck)

  - [UIA検証](http://www.codeplex.com/UIAutomationVerify/)

  - [実際のアクセシビリティのプロファイル](http://www.microsoft.com/enable/profiles/default.aspx)

  - [アクセシビリティ開発センター](http://msdn.microsoft.com/en-us/accessibility/default.aspx)

[Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:アクセシビリティAPI](https://ja.wikipedia.org/wiki/Category:アクセシビリティAPI "wikilink")

1.  [NFB-RD Mailing List February 1996](http://www.nfbcal.org/nfb-rd/0954.html), "OLAE \[sic\] accessibility"
2.  \[<https://msdn.microsoft.com/en-us/library/dd373654(VS.85>).aspx Supported Platforms: Active Accessibility - MSDN\]
3.  Microsoft Developer Network (MSDN): [UI Automation Specification](http://msdn.microsoft.com/en-us/accessibility/bb892135.aspx)
4.  Microsoft: [Accessibility in Microsoft Products](http://www.microsoft.com/enable/products/default.aspx).
5.  Microsoft: [History of Microsoft's Commitment to Accessibility](http://www.microsoft.com/enable/microsoft/history.aspx).
6.  Trace Center: [Assistive Technology Information Links](http://trace.wisc.edu/resources/at-resources.php) .