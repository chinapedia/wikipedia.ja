> この記事は[Microsoft SharePoint](https://ja.wikipedia.org/wiki/Microsoft_SharePoint)から翻訳されています。


**Microsoft SharePoint**とは、[マイクロソフト](../Page/マイクロソフト.md "wikilink")社が提供する、[コラボレーションや](../Page/グループウェア.md "wikilink")[ドキュメント管理等を行うための](../Page/文書管理システム.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")製品。SharePointを用いると、ユーザは共有されたワークスペースやドキュメントに対してウェブブラウザからアクセスできるほか、[Wiki](https://ja.wikipedia.org/wiki/Wiki "wikilink")や[ブログ](../Page/ブログ.md "wikilink")などのようなアプリケーションもホストすることができる。

利用者側の[インフラストラクチャー](https://ja.wikipedia.org/wiki/インフラストラクチャー "wikilink")上（[オンプレミス](https://ja.wikipedia.org/wiki/オンプレミス "wikilink")）で稼働させるエディション（後述）のほか、[マイクロソフト](../Page/マイクロソフト.md "wikilink")社の運営する SharePoint Online と呼ばれる[SaaS](https://ja.wikipedia.org/wiki/SaaS "wikilink")サービスも存在する\[1\]。

[Microsoft Office](../Page/Microsoft_Office.md "wikilink") ブランドに含まれる製品の一つでもある。

## 概要

SharePointの機能の多くは、Webパーツと呼ばれるものによって構成されている。たとえばタスクリストや電子会議室などをWebパーツとして作成することができる。

Microsoft SharePointのは3種類のエディションで提供されている。

  -

<!-- end list -->

  - Microsoft SharePoint Foundation (SPF)
  - Microsoft SharePoint Standard
  - Microsoft SharePoint Enterprise
      - Microsoft SharePoint StandardとMicrosoft SharePoint Enterpriseは、Microsoft SharePoint Server (SPS)によって提供されるエディションである。
      - Microsoft SharePoint Server (SPS)は、以前はSharePoint Portal Serverや[Microsoft Office SharePoint Server](https://ja.wikipedia.org/wiki/Microsoft_Office_SharePoint_Server "wikilink") (MOSS)という名称だった。

SharePointファミリーには、[Microsoft SharePoint Designerも含まれる](https://ja.wikipedia.org/wiki/Microsoft_SharePoint_Designer "wikilink")。

## SharePointファミリー

### Windows SharePoint Services (WSS)

[Windows SharePoint Services](https://ja.wikipedia.org/wiki/Windows_SharePoint_Services "wikilink")(**WSS**)は、[Windows Serverに無償で追加できるアドオンである](../Page/Windows_Server.md "wikilink")。WSSはHTTPとHTTPSをベースとして、ドキュメントの編集やバージョンの管理、またWikiやブログといったコラボレーションのための基盤を提供する。また、エンドユーザー向けの機能として、ワークフローやToDoリスト、アラート、電子会議室などの機能を持ったWebパーツと呼ばれるコンポーネントがあり、SharePointのページに組み込んで使用される。WSS 3.0はASP.NET 2.0を基盤として実装されている。WSSは以前は「SharePoint Team Services」と呼ばれていた。

SharePointが標準で持っているワークフローは、3段階のワークフローしかない。ほかの機能を持ったワークフローが必要な場合は、SharePoint DesignerやVisual Studioを使って開発することになる。WSS3.0におけるワークフローの主な制限は、ASP.NETで作成したページの代わりにInfoPath 2007を使用してフォームを作成できないということである。

### Microsoft Office SharePoint Server 2007 (MOSS 2007)

[Microsoft Office SharePoint Server](https://ja.wikipedia.org/wiki/Microsoft_Office_SharePoint_Server "wikilink") (**MOSS**) は、有償の[Microsoft Officeサーバースイートである](../Page/Microsoft_Office.md "wikilink")。MOSSはWSSの上で構築され、さらに多くの機能が追加されている。たとえばより詳細なドキュメント管理や[エンタープライズサーチ](../Page/エンタープライズサーチ.md "wikilink")の機能、ナビゲーション、[RSS](../Page/RSS.md "wikilink")のサポート、Microsoft Content Management Serverの後継として引き継いだ機能などである。MOSSのEnterprise Editionでは、Excelサービスやビジネスデータカタログなど、[ビジネスインテリジェンス](https://ja.wikipedia.org/wiki/ビジネスインテリジェンス "wikilink")の機能も含まれている。また、Microsoft Project Serverと連携してプロジェクトマネジメントを可能にしたり、PowerPointのスライドライブラリの機能が追加されるなど、特定のアプリケーションコンポーネントをインストールすることによってMicrosoft Officeの各製品と統合された環境が提供される。

2009年1月、Microsoftが起案・監修した[メール情報セキュリティ強化パック](https://ja.wikipedia.org/wiki/メール情報セキュリティ強化パック "wikilink")がリリース。開発した[ソフトバンク・テクノロジー](https://ja.wikipedia.org/wiki/ソフトバンク・テクノロジー "wikilink")のWebサイトから無償提供される。

### Microsoft Search Server

[Microsoft Search Server](https://ja.wikipedia.org/wiki/Microsoft_Search_Server "wikilink") (**MSS** : [en](https://ja.wikipedia.org/wiki/:en:Microsoft_Search_Server "wikilink"))は、マイクロソフトが提供する[エンタープライズサーチ](../Page/エンタープライズサーチ.md "wikilink")プラットフォームである。その検索機能は[Microsoft Office SharePoint Serverを基にしている](https://ja.wikipedia.org/wiki/Microsoft_Office_SharePoint_Server "wikilink")。MSSはそのクエリエンジンとインデックスを作成する基盤としてWindows サーチと同じものを使用している。MOSSの検索はドキュメントに埋め込まれたメタデータの検索機能を提供する。

<table>
<caption>各バージョンの仕様</caption>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>公開日</p></th>
<th><p>無償版<br />
(Express)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Search Server 2008</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/2008年" title="wikilink">2008年</a><a href="https://ja.wikipedia.org/wiki/3月" title="wikilink">3月</a></p></td>
<td><p>有り</p></td>
</tr>
<tr class="even">
<td><p>Search Server 2010</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/2010年" title="wikilink">2010年</a><a href="https://ja.wikipedia.org/wiki/5月" title="wikilink">5月</a></p></td>
<td><p>有り</p></td>
</tr>
</tbody>
</table>

無償版である Express エディションの機能は有償版と比べてもインデックスの作成数などに制限は設けられていないが、スタンドアロンの利用に制限されていて、クラスタにスケールアウトすることができない。

### Microsoft SharePoint Designer

[Microsoft SharePoint Designerは主にSharePointサイトやWSS上で動くエンドユーザ向けワークフローを作成する](https://ja.wikipedia.org/wiki/Microsoft_SharePoint_Designer "wikilink")[WYSIWYG](../Page/WYSIWYG.md "wikilink")[HTML エディタである](../Page/Webオーサリングツール.md "wikilink")。[レンダリングエンジン](https://ja.wikipedia.org/wiki/レンダリングエンジン "wikilink")は[Microsoft Expression Webなどのデザインツールや](https://ja.wikipedia.org/wiki/Microsoft_Expression_Web "wikilink")、[Visual Studio 2008](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio#Visual_Studio_2008 "wikilink")[IDEと共通である](../Page/統合開発環境.md "wikilink")。SharePoint Designerは[Microsoft FrontPageの後継製品とされている](https://ja.wikipedia.org/wiki/Microsoft_FrontPage "wikilink")。しかし、FrontPageにはSharePoint 2007やMOSSとの互換性はない。SharePoint Designerをサーバーにインストールする際はIISにFrontpageサーバー拡張が必要である。

### FAST Search Server for SharePoint (FS4SP)

[FAST Search Server for SharePoint](https://ja.wikipedia.org/wiki/FAST_Search_Server_for_SharePoint "wikilink") は、Microsoft SharePointに[FASTの](../Page/ファストサーチ_&_トランスファ.md "wikilink")[エンタープライズ検索機能を実装することで](../Page/エンタープライズサーチ.md "wikilink")、これまでにないイントラネット検索、人材の検索、および検索主導型アプリケーションのプラットフォームを実現している。

SharePoint 2013によって、FS4SPが提供する高度な検索機能はSharePointの標準機能として統合された。

## 関連項目

  - [:en:Collaborative Application Markup Language](https://ja.wikipedia.org/wiki/:en:Collaborative_Application_Markup_Language "wikilink")
  - [ブログパーツ](https://ja.wikipedia.org/wiki/ブログパーツ "wikilink")([:en:Web widget](https://ja.wikipedia.org/wiki/:en:Web_widget "wikilink"))
  - [:en:Enterprise portal](https://ja.wikipedia.org/wiki/:en:Enterprise_portal "wikilink")
  - [:en:Bulldog (Microsoft)](https://ja.wikipedia.org/wiki/:en:Bulldog_\(Microsoft\) "wikilink")
  - [Alfresco](https://ja.wikipedia.org/wiki/Alfresco "wikilink") - 類似のオープンソースソフトウエア
  - [Liferay](https://ja.wikipedia.org/wiki/Liferay "wikilink") - 類似のオープンソースソフトウエア

## 脚注

<div class="references-small">

<references />

</div>

## 外部リンク

  - [SharePoint](https://products.office.com/ja-jp/sharepoint/) マイクロソフト社 日本語・日本向けページ
  - [SharePoint ドキュメント | Microsoft Docs](https://docs.microsoft.com/ja-jp/sharepoint/) マイクロソフト社 開発者向け 日本語・日本向けページ

[Category:Microsoft_Office](https://ja.wikipedia.org/wiki/Category:Microsoft_Office "wikilink") [Category:Microsoft_server_technology](https://ja.wikipedia.org/wiki/Category:Microsoft_server_technology "wikilink") [Category:グループウェア](https://ja.wikipedia.org/wiki/Category:グループウェア "wikilink")

1.