> この記事は[Apache POI](https://ja.wikipedia.org/wiki/Apache_POI)から翻訳されています。


{{ Infobox_Software | name = Apache POI | logo = | screenshot = | caption = | developer = [Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Apacheソフトウェア財団 "wikilink") | latest release version = 4.1.1 | latest release date = \[1\] | latest_preview_version = | latest_preview_date = | operating_system = [クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink") | programming_language = [Java](https://ja.wikipedia.org/wiki/Java "wikilink") | genre = [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") | license = [Apache License](https://ja.wikipedia.org/wiki/Apache_License "wikilink") 2.0 | website = <https://poi.apache.org/> }} ****（アパッチ・ポイまたはピーオーアイ）は[Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Apacheソフトウェア財団 "wikilink")のプロジェクトで、[Wordや](../Page/Microsoft_Word.md "wikilink")[Excelといった](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")[Microsoft Office形式の](../Page/Microsoft_Office.md "wikilink")[ファイルを読み書きできる](../Page/ファイル_\(コンピュータ\).md "wikilink")100% [Java](https://ja.wikipedia.org/wiki/Java "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")として提供されている。

## 名称の由来

POIという名称は、Microsoft Officeの[ファイル形式を](../Page/ファイルフォーマット.md "wikilink")[リバースエンジニアリング](https://ja.wikipedia.org/wiki/リバースエンジニアリング "wikilink")した際、その形式が意図的に、しかも中途半端に分かりにくくされていたため、皮肉を込めて "" (質の悪い難読な実装) と呼んだものの[頭字語](../Page/頭字語.md "wikilink")に端を発している。このようにユーモラスな正式名称を当てはめる方法はかつていろいろなサブプロジェクトに見られたが、ユーモアを不適切と捉えるビジネス界への進出を意識し、公式ウェブページからは削除されている。もうひとつの由来は、ハワイの珍味**[Poi](https://ja.wikipedia.org/wiki/ポイ_\(料理\) "wikilink")**から来た。[ハワイ人](https://ja.wikipedia.org/wiki/ハワイ人 "wikilink")がこれを食べ続けると巨人になるとも言われている。

## Office Open XMLのサポート

バージョン3.5からISO/IEC 29500 [Office Open XML形式のファイルに対応している](https://ja.wikipedia.org/wiki/Office_Open_XML "wikilink")。 OOXMLへの対応は、Sourcesenseが貢献している\[2\]。 Sourcesenseは、前記の貢献をするための[マイクロソフト](../Page/マイクロソフト.md "wikilink")から委託を受けた[オープンソース](../Page/オープンソース.md "wikilink")企業である\[3\]。 この関係は論争を促し、一部のPOI参加者は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[Open Specification Promiseに関するPOI](https://ja.wikipedia.org/wiki/Microsoft_Open_Specification_Promise "wikilink") OOXMLの特許保護を問う者もいる。

## サブコンポーネント

Apache POIプロジェクトは、次のようなサブコンポーネントから成る。

  - POIFS () - Microsoft [OLE](../Page/Object_Linking_and_Embedding.md "wikilink") 2複合ドキュメント形式を読み書きするコンポーネント。すべてのMicrosoft OfficeファイルはOLE 2ファイルであるため、POIFSは他のPOI構成要素の基礎となっている。そのためPOIFSは、明示的にPOIで書かれたモジュール以外にも、さまざまな種類のファイルを読むのに使われている。
  - HSSF () - Microsoft Excel (XLS) 形式のファイルを扱う。Excel 97以降のファイルを読み書きできる。このファイル形式は、BIFF 8形式として知られている。フィルターやビューを含むシートを開けない。
  - XSSF () - Office Open XML Workbook形式のファイルを扱う。Excel 2007で採用されたOOXML形式のファイルを読み書きできる。
  - HWPF () - Microsoft Word (DOC) 形式のファイルを扱う。Word 97以降のファイルを読み書きできる。Word 95以前の形式も限定的に読むことができる。
  - XWPF () - Office Open XML Document形式のファイルを扱う。Word 2007で採用されたOOXML形式のファイルを読み書きできる。
  - HSLF () - [Microsoft PowerPoint](https://ja.wikipedia.org/wiki/Microsoft_PowerPoint "wikilink") (PPT) 形式のファイルを扱う。PowerPoint 97以降のファイルを読み書きできる。
  - XSLF () - Office Open XML Presentation形式のファイルを扱う。PowerPoint 2007で採用されたOOXML形式のファイルを読み書きできる。
  - HPSF () - Microsoft Officeのドキュメントサマリーを読むコンポーネント。ドキュメントサマリーとは、主にOfficeアプリケーションの[メニューバーから](https://ja.wikipedia.org/wiki/メニュー_\(コンピュータ\) "wikilink")「ファイル」→「プロパティ」で見られる情報のこと。
  - HDGF () - [Microsoft Visio形式のファイルを扱う](https://ja.wikipedia.org/wiki/Microsoft_Visio "wikilink")。現在は読み取りのみ可能。
  - HPBF () - [Microsoft Publisher形式のファイルを扱う](https://ja.wikipedia.org/wiki/Microsoft_Publisher "wikilink")。現在は開発初期段階にあって、ファイル内の一部の読み取りに限られている。
  - HSMF () - [Microsoft Outlook](../Page/Microsoft_Outlook.md "wikilink") (MSG) 形式のファイルを扱う。現在はファイルの読み取りのみ可能。

POIライブラリは、[Ruby](../Page/Ruby.md "wikilink")の拡張としても提供されている。

## サブプロジェクト

  - [XMLBeans](https://ja.wikipedia.org/wiki/XMLBeans "wikilink") : JavaとXMLデータバインディングとの変換を行うフレームワーク。。

## 脚注

<references/>

## 関連項目

  - [Apache Jakarta Project](https://ja.wikipedia.org/wiki/Jakarta_Project "wikilink")
  - [XMLBeans](https://ja.wikipedia.org/wiki/XMLBeans "wikilink")
  - [Microsoft Excel](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")
  - [Microsoft Word](../Page/Microsoft_Word.md "wikilink")
  - [Microsoft PowerPoint](https://ja.wikipedia.org/wiki/Microsoft_PowerPoint "wikilink")
  - [Microsoft Outlook](../Page/Microsoft_Outlook.md "wikilink")
  - [Microsoft Visio](https://ja.wikipedia.org/wiki/Microsoft_Visio "wikilink")
  - [Microsoft Publisher](https://ja.wikipedia.org/wiki/Microsoft_Publisher "wikilink")
  - [Office Open XML](https://ja.wikipedia.org/wiki/Office_Open_XML "wikilink")

## 外部リンク

  -
  -
[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:コンピュータのユーザインタフェース](https://ja.wikipedia.org/wiki/Category:コンピュータのユーザインタフェース "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink")

1.
2.
3.