> この記事は[Apache XML](https://ja.wikipedia.org/wiki/Apache_XML)から翻訳されています。


**Apache XML** (アパッチ・エックスエムエル) プロジェクトは、[XMLに関連した](../Page/Extensible_Markup_Language.md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の[ソフトウェア](../Page/ソフトウェア.md "wikilink")を開発することなどを目的とした団体であり、[Apacheソフトウェア財団](../Page/Apacheソフトウェア財団.md "wikilink")が主催するプロジェクトの一つである。

Apache XMLプロジェクトが開発するソフトウェアは、Apacheソフトウェア財団の他のプロジェクトと同様に、[Apacheライセンスのもとで提供されている](../Page/Apache_License.md "wikilink")。Apache XMLプロジェクトは複数のサブプロジェクトをもっていた。

2012年4月12日にプロジェクトは終了し、[Apache Atticに移管された](https://ja.wikipedia.org/wiki/Apache_Attic "wikilink")。

## サブプロジェクトの一覧

### 活動中

  - [Xerces](../Page/Apache_Xerces.md "wikilink") : XMLプロセサ ([XMLパーサ](https://ja.wikipedia.org/wiki/XMLパーサ "wikilink")) 。[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、および [C++](../Page/C++.md "wikilink")、[Perl](../Page/Perl.md "wikilink")で実装されたものがそれぞれ提供されている。[DOMと](../Page/Document_Object_Model.md "wikilink")[SAXを実装している](../Page/Simple_API_for_XML.md "wikilink")。現在では、Apache XML プロジェクトから独立して、トップレベルプロジェクトとなっている。[IBM](../Page/IBM.md "wikilink") から寄贈された XML4J という実装がもとになっているが、現在のバージョンは全て新規に開発し直された。
    [Xalan](../Page/Apache_Xalan.md "wikilink") : [XSLT](../Page/XSL_Transformations.md "wikilink") の[スタイルシート](../Page/スタイルシート.md "wikilink")の処理系で、[XPathの機能も実装している](../Page/XML_Path_Language.md "wikilink")。JavaとC++で実装されたものがそれぞれ提供されている。現在では、Apache XML プロジェクトから独立して、トップレベルプロジェクトとなっている。IBM/[Lotusから寄贈されたLotusXSLという実装がもとになっている](../Page/ロータス_\(ソフトウェア\).md "wikilink")。
    [FOP](../Page/Apache_FOP.md "wikilink") : [XSL-FOの](../Page/XSL_Formatting_Objects.md "wikilink")[組版](../Page/組版.md "wikilink")を行う処理系。Java で実装されている。XSL-FO のXML文書を、コンピュータの画面に表示したり、[PDFなどの形式に変換したり](../Page/Portable_Document_Format.md "wikilink")、プリンタに直接印刷したりすることができる。[Apache XML Graphicsで開発が継続されている](../Page/Apache_XML_Graphics.md "wikilink")。
    Forrest : [Apache Cocoon上で利用できる](../Page/Apache_Cocoon.md "wikilink")、標準規格に基づいた文書の処理・出版を行うためのフレームワーク。
    XML-Security : XMLデータのための[電子署名](../Page/電子署名.md "wikilink")と[暗号](../Page/暗号.md "wikilink")化のセキュリティ機能を提供する ( [XML Signature](https://ja.wikipedia.org/wiki/XML署名 "wikilink") と [XML Encryption](https://ja.wikipedia.org/wiki/XML暗号化 "wikilink") の実装) 。JavaとC++で実装されたものがそれぞれ提供されている。
    XML Commons : Apache XML プロジェクトで共通に使う機能(プログラムコード)を提供する。また、Apache XMLプロジェクト共通のガイドラインを作成している。
    [Batik](../Page/Apache_Batik.md "wikilink") : [SVGの表示](../Page/Scalable_Vector_Graphics.md "wikilink")・編集・ほかの[画像](../Page/画像.md "wikilink")[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")への変換などの機能を提供するツールおよびJava[ライブラリ](../Page/ライブラリ.md "wikilink")。[Apache XML Graphicsで開発が継続されている](../Page/Apache_XML_Graphics.md "wikilink")。

### Webサービス関連

  - [Axis](../Page/Apache_Axis.md "wikilink") : [Webサービス](../Page/Webサービス.md "wikilink")の[プロトコル](../Page/通信プロトコル.md "wikilink")、[SOAP](../Page/SOAP_\(プロトコル\).md "wikilink") の現在の実装。[WSDL関連の機能も備えている](../Page/Web_Services_Description_Language.md "wikilink")。JavaとC++で実装されたものがそれぞれ提供されている。後述のSOAPサブプロジェクトの後継である。
    SOAP : SOAP の古い実装。IBMから寄贈されたSOAP4Jという実装がもとになっている。これからSOAPを使うプロジェクトを始める場合には、このSOAP実装を使うことは望ましくない。前述のAxisを使うことが望ましい。
    XML-RPC : XML-RPC ([HTTP上でXMLデータをやりとりして](../Page/Hypertext_Transfer_Protocol.md "wikilink")[遠隔手続き呼出し](../Page/遠隔手続き呼出し.md "wikilink") (RPC) を実現するプロトコル) のJavaによる実装。
    WSIF : 簡易にWebサービスを呼び出すことができるJava API。

### 活動停止

  - AxKit : [Apache HTTP Server](../Page/Apache_HTTP_Server.md "wikilink")（[Webサーバ](../Page/Webサーバ.md "wikilink")）のmod_perlで利用できる、XML技術を使ったウェブ出版[フレームワーク](https://ja.wikipedia.org/wiki/フレームワーク "wikilink")。
    Crimson : Javaで実装されたXMLプロセサ (XMLパーサ) 。サン・マイクロシステムズから寄贈された。
    Xang : [ECMAScript](../Page/ECMAScript.md "wikilink") ([JavaScript](../Page/JavaScript.md "wikilink")) による動的な[ウェブページ](../Page/ウェブページ.md "wikilink")を短期間で開発できるフレームワーク。
    Xindice : [ネイティブXMLデータベース](../Page/ネイティブXMLデータベース.md "wikilink")の実装。
    [XMLBeans](https://ja.wikipedia.org/wiki/XMLBeans "wikilink") : XML文書とJavaのバインディングを行うツール。[XML Schemaのスキーマが記述されたファイルをもとに](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")、Javaの[ソースコード](../Page/ソースコード.md "wikilink")を自動生成する（[JavaBeans](../Page/JavaBeans.md "wikilink")準拠）。
    JaxMe : XML文書とJavaのバインディングを行うツール。[JAXBの実装](../Page/Java_Architecture_for_XML_Binding.md "wikilink")。

## 外部リンク

  - [Apache XML プロジェクト](http://xml.apache.org/)
  - [Apache Xerces プロジェクト](http://xerces.apache.org/)
  - [Apache Xalan プロジェクト](http://xalan.apache.org/)
  - [Apache XML Graphics プロジェクト](http://xmlgraphics.apache.org/)
  - [Apache Web Services プロジェクト](http://ws.apache.org/)
  - [日本ApacheXMLプロジェクト](http://jpfop.sourceforge.net/jaxml/)

[Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink")