> この記事は[Windows Workflow Foundation](https://ja.wikipedia.org/wiki/Windows_Workflow_Foundation)から翻訳されています。


**Windows Workflow Foundation**（**WF**）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の技術であり、[ワークフロー](../Page/ワークフロー.md "wikilink")を定義・実行・管理する。この技術は [.NET Framework 3.0](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") の一部であり、[Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") に含まれている。また、[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") SP2 および [Windows Server 2003](../Page/Microsoft_Windows_Server_2003.md "wikilink") にもインストール可能である。

## ワークフロー編集

ワークフローの構造を記述する言語としては、[XMLベースの](../Page/Extensible_Markup_Language.md "wikilink")[XAMLがよく使われている](../Page/Extensible_Application_Markup_Language.md "wikilink")。しかし、任意の .NET 用言語（[VB.NET](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink")、[C\#](../Page/C_Sharp.md "wikilink")、[C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink") など）のコードでワークフローを表現することが可能である。

ワークフローは「アクティビティ」から構成される。開発者は固有のアクティビティを書くことができ、それをワークフローに使用する。WF には汎用のアクティビティとしていくつかの制御構造が用意されている。

Windows Workflow Foundation の拡張セットが [Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") 2005 でサポートされている。それには、ビジュアル・ワークフロー・デザイナーやワークフローの[デバッグ](../Page/デバッグ.md "wikilink")も可能なビジュアル・デバッガ、ワークフロー用のプロジェクトシステムが含まれる。

## ワークフローの実行管理

.NET Framework 3.0 ワークフロー・ランタイムは、ワークフローの実行と管理を行うファシリティであり、任意の[CLRアプリケーションドメイン](../Page/共通言語ランタイム.md "wikilink")（Windows Service として、Console Service として、Web Application として）で実行される。

ホストは、[シリアライズ](../Page/シリアライズ.md "wikilink")などのサービスも必要に応じて提供する。ワークフローのインスタンスのイベント（アイドルとなった、停止したなど）を契機として捉えることもできる。

### ワークフローとの通信

WFワークフローには、外界と通信するためのメソッドとイベントのインタフェースが定義されている。[ホストアプリケーション](https://ja.wikipedia.org/wiki/ホストアプリケーション "wikilink")はワークフローを実行するまえに環境を設定し、それらインタフェースを実装したオブジェクトを提供する。

それらインタフェースを実装したオブジェクトがイベントを発生させると、対応するワークフローがそれに反応し、データを受け渡す。

インタフェース上のメソッドはホストとの通信のためにワークフローから呼び出される。

## Windows Workflow Foundationが使用されている製品

  - [Microsoft Office SharePoint Server](https://ja.wikipedia.org/wiki/Microsoft_Office_SharePoint_Server "wikilink") 2007バージョンから使用されている。
  - [Microsoft Speech Server](https://ja.wikipedia.org/wiki/Microsoft_Speech_Server "wikilink") 2007バージョンから使用されている。
  - [Microsoft Dynamics CRM](https://ja.wikipedia.org/wiki/Microsoft_CRM "wikilink") 4.0バージョンから使用されている。
  - [Microsoft BizTalk Server](https://ja.wikipedia.org/wiki/Microsoft_BizTalk_Server "wikilink") 2006バージョンから使用されている。

## 参考文献

  - *Essential Windows Workflow Foundation*, Dharma Shukla/Bob Schmidt, Addison-Wesley Professional, [2006年](../Page/2006年.md "wikilink")[10月13日](../Page/10月13日.md "wikilink"). ISBN 0-321-39983-8
  - *Foundations of WF ISBN 1-59059-718-4*, Brian R. Myers, Apress, [2006年](../Page/2006年.md "wikilink")[10月23日](../Page/10月23日.md "wikilink"). ISBN 1-59059-718-4
  - *Pro WF: Windows Workflow in .NET 3.0*, Bruce Bukovics, Apress, [2007年](../Page/2007年.md "wikilink")[2月19日](../Page/2月19日.md "wikilink"). ISBN 1-59059-778-8
  - *Professional Windows Workflow Foundation ISBN 0-470-05386-0*, Todd Kitta, Wrox, [2007年](../Page/2007年.md "wikilink")[3月12日](../Page/3月12日.md "wikilink"). ISBN 0-470-05386-0
  - *Microsoft Windows Workflow Foundation Step by Step*, Kenn Scribner, Microsoft Press, [2007年](../Page/2007年.md "wikilink")[2月28日](../Page/2月28日.md "wikilink"). ISBN 0-7356-2335-X

## 外部リンク

  - [MSDN Library: Windows Workflow Foundation](http://msdn2.microsoft.com/ja-jp/library/ms735967.aspx)

{{.NET}}

[Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink")