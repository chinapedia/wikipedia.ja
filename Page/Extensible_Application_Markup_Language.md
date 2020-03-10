> この記事は[Extensible Application Markup Language](https://ja.wikipedia.org/wiki/Extensible_Application_Markup_Language)から翻訳されています。


**Extensible Application Markup Language**（**XAML**、ザムルと発音する\[1\]）は、[オブジェクト](https://ja.wikipedia.org/wiki/オブジェクト "wikilink")や[プロパティ](../Page/プロパティ.md "wikilink")、あるいはそれらの関係や相互作用を定義するために用いられる[XMLベースの宣言的言語である](../Page/Extensible_Markup_Language.md "wikilink")。XAMLという略語はもともと「Extensible Avalon Markup Language」に由来していた。Avalonとは[Windows Presentation Foundation](https://ja.wikipedia.org/wiki/Windows_Presentation_Foundation "wikilink") (WPF) のコードネームである。

## 適用領域

XAMLは[.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 3.0以降のテクノロジーにおいて広範囲にわたって使われている。とりわけ、Windows Presentation Foundation (WPF) および [Silverlight](https://ja.wikipedia.org/wiki/Silverlight "wikilink")において[ユーザーインターフェイス要素や](../Page/ユーザインタフェース.md "wikilink")[データバインディング](https://ja.wikipedia.org/wiki/データバインディング "wikilink")、イベント処理、などを定義するために、また、[Windows Workflow Foundation](https://ja.wikipedia.org/wiki/Windows_Workflow_Foundation "wikilink") (WF) において[ワークフロー](https://ja.wikipedia.org/wiki/ワークフロー "wikilink")そのものを定義するために用いられる。なお、[Windows 8および](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")[Windows RTで利用できる](https://ja.wikipedia.org/wiki/Microsoft_Windows_RT "wikilink")[WinRT](https://ja.wikipedia.org/wiki/Windowsランタイム "wikilink") APIを使用した[Windowsストア](https://ja.wikipedia.org/wiki/Windowsストア "wikilink")アプリでは、.NETアプリケーションに限らず[C++](../Page/C++.md "wikilink")ネイティブアプリケーション\[2\]でもXAMLを使ってUIを構築することが可能となっている。後発の[Windows 10にて対応した](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")[ユニバーサルWindowsプラットフォーム](https://ja.wikipedia.org/wiki/ユニバーサルWindowsプラットフォーム "wikilink") (UWP) アプリもまたWinRTベースであり、XAMLを利用して開発する。[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")な.NETアプリケーション開発に利用可能な[Xamarin](https://ja.wikipedia.org/wiki/Xamarin "wikilink").Formsでは、UIの記述にXAMLを用いる。

これらのXAMLを利用するテクノロジー間で、個別のXAML要素の互換性については確保されておらず、名称が違っていたり、サポートされていなかったりする要素もあるが、いずれのフレームワークもほぼ同じ要領で開発できることが大きな利点となる。マイクロソフト固有のXAMLは主に[Windowsプラットフォームに特化したものだが](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、*XAML Standard*と呼ばれる標準化プロジェクトも立ち上げられている\[3\]\[4\]。

## WPFにおける仕様

XAMLにおける要素 (element) は[CLRにおけるオブジェクト](../Page/共通言語ランタイム.md "wikilink")[インスタンス](../Page/インスタンス.md "wikilink")に、属性 (attribute) はCLRにおけるプロパティやイベントに対応する。典型的には、XAMLファイルは[Microsoft Expression Blend](https://ja.wikipedia.org/wiki/Microsoft_Expression_Blend "wikilink")、[Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")、\[<https://docs.microsoft.com/ja-jp/previous-versions/dotnet/netframework-3.0/ms742398(v=vs.85>) XAMLPad\]のような開発ツールによって生成される。XAMLファイルは`.baml`ファイル（バイナリファイル）にコンパイルされ、[リソース](https://ja.wikipedia.org/wiki/リソース "wikilink")として.NET Frameworkアセンブリに含められる。実行時には、CLRがアセンブリのリソースから`.baml`ファイルを抽出・解析し、WPFのユーザーインターフェイス要素やワークフローを作成する。

WPFにおいては、XAMLは[Adobe Flashのように表現豊かなユーザーインターフェイスを記述することができる](../Page/Adobe_Flash.md "wikilink")。他のXMLベースのユーザーインターフェイス記述言語には[XUL](https://ja.wikipedia.org/wiki/XUL "wikilink")やがある。XAMLは単純な2Dグラフィックスだけでなく3Dオブジェクトも記述することが可能で、さらに回転・拡大縮小といった変形に加えて、アニメーションやその他の多彩な効果を表現することができる。

XAMLで記述可能なあらゆるものはまた、[C\#や](../Page/C_Sharp.md "wikilink")[VB .NETなどといった](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink").NET言語による[コードビハインド](https://ja.wikipedia.org/wiki/コードビハインド "wikilink")でも記述することができる。しかし、重要な相違点として、XAMLはXMLベースであるがゆえに、開発ツール（[RADツール](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")）の設計が容易であるという点が挙げられる。その結果、特にWPFにおいて、XAMLファイルを生成するためのさまざまなツールが開発されている。また、XMLであるために分析者・デザイナー・開発者がそれぞれの立場から製品に関与することが容易になっている。

## 脚注

## 関連項目

  - [XUL](https://ja.wikipedia.org/wiki/XUL "wikilink")
  - [Adobe Flash](../Page/Adobe_Flash.md "wikilink")
  - [レイアウトマネージャ](https://ja.wikipedia.org/wiki/レイアウトマネージャ "wikilink")
  - [Windows Presentation Foundation](https://ja.wikipedia.org/wiki/Windows_Presentation_Foundation "wikilink")
  - [Silverlight](https://ja.wikipedia.org/wiki/Silverlight "wikilink")
  - [Microsoft Expression Blend](https://ja.wikipedia.org/wiki/Microsoft_Expression_Blend "wikilink")
  - [Xamarin](https://ja.wikipedia.org/wiki/Xamarin "wikilink")

## 外部リンク

  - Intoroducing "Longhorn" for Developers 第3章 [コントロールとXAML](http://www.microsoft.com/japan/msdn/longhorn/introducing/longhornch03.asp)
  - MSDN Library [XAML Overview](http://msdn2.microsoft.com/en-us/library/ms752059.aspx)
  - [Download Extensible Application Markup Language (XAML) from Official Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=19600): 仕様書

{{.NET}}

[Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:ベクターグラフィックス・マークアップ言語](https://ja.wikipedia.org/wiki/Category:ベクターグラフィックス・マークアップ言語 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:コンピュータのユーザインタフェース](https://ja.wikipedia.org/wiki/Category:コンピュータのユーザインタフェース "wikilink") [Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.  [第1回　Hello Worldとテキスト・エディタで始めるXAML － ＠IT](http://www.atmarkit.co.jp/fdotnet/basics/xaml01/xaml01_01.html)
2.  通例、と呼ばれるマイクロソフト独自の拡張が施された言語を用いる。
3.  [Microsoft/xaml-standard: XAML Standard : a set of principles that drive XAML dialect alignment](https://github.com/Microsoft/xaml-standard)
4.  [XAML Standardとは：特集：Microsoftテクノロジーの現在と未来 - ＠IT](https://www.atmarkit.co.jp/ait/articles/1708/25/news021.html)