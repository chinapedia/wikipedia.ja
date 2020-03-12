> この記事は[Extensible Stylesheet Language](https://ja.wikipedia.org/wiki/Extensible_Stylesheet_Language)から翻訳されています。


**Extensible Stylesheet Language**（**XSL**; 拡張可能なスタイルシート言語）は、[XML文書から](../Page/Extensible_Markup_Language.md "wikilink")、[組版](../Page/組版.md "wikilink")などの変換を行うための[システム](../Page/システム.md "wikilink")で、複数の仕様から構成されている。

XSLを構成する仕様は次の3つである。元々は「Extensible Stylesheet Language」という名前の通り、スタイルシートに基づき組版処理などを行う目的で策定が始まったものだが、XSLTはXMLの変換用として汎用になるよう、XPathはXMLの木の要素の指定用として汎用になるよう、設計された。

  - XSL Transformations
    [XSL Transformations](../Page/XSL_Transformations.md "wikilink") (XSLT) は、XML文書を構造の異なるXML文書などに変換するための変換言語である。それ自身もXMLで記述する。
  - XML Path Language
    [XML Path Language](../Page/XML_Path_Language.md "wikilink") (XPath) は、XML文書の特定の部分（要素、属性、テキストなど）を指定する表現法である。XPathは、XSLTで処理対象のXML文書の特定部分を指定するために使われている。XPath自体は簡潔な構文であり、それ自身はXMLではない。
  - XSL Formatting Objects
    [XSL Formatting Objects](../Page/XSL_Formatting_Objects.md "wikilink") (XSL-FO) は、文書の[組版](../Page/組版.md "wikilink")（人間に理解しやすい形式）を記述する記述言語である。それ自身もXMLで記述する。

この3つの仕様は、[標準化団体](../Page/標準化団体_\(コンピュータと通信\).md "wikilink") [W3C](../Page/World_Wide_Web_Consortium.md "wikilink") (World Wide Web Consortium) で開発され勧告として公表されている。

## 歴史

XSLの歴史は、既存の [SGML](../Page/Standard_Generalized_Markup_Language.md "wikilink") 向けの[スタイルシート](../Page/スタイルシート.md "wikilink")である [DSSSL](../Page/Document_Style_Semantics_and_Specification_Language.md "wikilink") の機能、特に印刷と植字の機能を、[XMLに適用できるようにする開発作業から始まった](../Page/Extensible_Markup_Language.md "wikilink")。

  - 1997年12月から、[W3CのXSL作業部会の活動が始まった](../Page/World_Wide_Web_Consortium.md "wikilink")。XSL作業部会では、シャロン・アドラーとスティーブ・ジルズが共同議長を、[ジェームズ・クラークがエディタを](../Page/ジェームズ・クラーク_\(ソフトウェア技術者\).md "wikilink")、それぞれ務めた。ジェームズ・クラークは、XSLの非公式な主席設計者でもあった。また、クリス・リリーがW3Cスタッフの連絡役を務めた。
  - 1998年8月18日に、作業部会はXSL仕様の最初の作業ドラフトを公表した。
  - 1999年11月16日に、[XSLT](../Page/XSL_Transformations.md "wikilink") 1.0 と [XPath](../Page/XML_Path_Language.md "wikilink") 1.0 がW3Cから勧告として公表された。
  - 2001年10月15日に、XSL 1.0（[XSL-FOを含む](../Page/XSL_Formatting_Objects.md "wikilink")）がW3Cから勧告として公表された。
  - 2006年12月5日に、XSL 1.1（[XSL-FOを含む](../Page/XSL_Formatting_Objects.md "wikilink")）がW3Cから勧告として公表された。
  - 2007年1月23日に、XSLT 2.0 と XPath 2.0 がW3Cから勧告として公表された。
  - 2014年4月8日に、XPath 3.0 がW3Cから勧告として公表された。
  - 2017年3月21日に、XPath 3.1 がW3Cから勧告として公表された。
  - 2017年6月8日に、XSLT 3.0 がW3Cから勧告として公表された。

## XSLを構成する仕様

[thumb文書を](https://ja.wikipedia.org/wiki/ファイル:XSL.png "wikilink")[XSLT](../Page/XSL_Transformations.md "wikilink")/[XPathで変換して](../Page/XML_Path_Language.md "wikilink")[XSL-FO文書を生成し](../Page/XSL_Formatting_Objects.md "wikilink")、XSL-FO処理系によって人間に理解しやすい形式に変換する\]\]

### XSL Transformations

XSL Transformations (XSLT) は、[XML文書を構造の異なるXML文書などに変換する](../Page/Extensible_Markup_Language.md "wikilink")[変換言語](https://ja.wikipedia.org/wiki/変換言語 "wikilink")である。XMLの他、プレインテキストとして出力（ないし、そのように意図して設計すれば、何らかのXMLでない[形式言語](../Page/形式言語.md "wikilink")に従った形にも）できる。

XSL全体での位置づけとしては、任意のXSLから[XSL-FOへの変換に使う](../Page/XSL_Formatting_Objects.md "wikilink")。

現在、XSLT処理系の[実装](../Page/実装.md "wikilink")は、数多く開発されており、利用することができる。主な実装を次に示す。

  - [Saxon](https://ja.wikipedia.org/wiki/Saxon "wikilink") - [オープンソース](../Page/オープンソース.md "wikilink")の実装
  - [Apache Xalan](../Page/Apache_Xalan.md "wikilink") - [Apache XML](../Page/Apache_XML.md "wikilink") プロジェクトによるオープンソース実装
  - [ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")で利用されている実装
      - [MSXML](https://ja.wikipedia.org/wiki/MSXML "wikilink") - [Internet Explorer](../Page/Internet_Explorer.md "wikilink") で使われている
      - [TransforMiiX](https://ja.wikipedia.org/wiki/TransforMiiX "wikilink") - [Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")、[Mozilla](../Page/Mozilla.md "wikilink")、[Netscape](../Page/Netscapeシリーズ.md "wikilink") で使われている

### XPath

XML Path Language (XPath) は、[XML文書の特定の部分](../Page/Extensible_Markup_Language.md "wikilink")（要素、属性、テキストなど）を指定する表現法である。 XPath自体は簡潔な構文であり、XMLベースではない。 XPathは、[XSLTで処理対象のXML文書の特定部分を指定するために使われている他](../Page/XSL_Transformations.md "wikilink")、XSLT以外でも処理対象のXML文書の特定部分を指定するために使われている。

XPathをさらに拡張したような仕様を持つものとして[XQuery](../Page/XQuery.md "wikilink")がある。XQueryは、処理対象のXML文書の特定部分を検索する。

### XSL Formatting Objects

## 関連項目

  - [XML](../Page/Extensible_Markup_Language.md "wikilink")
  - [スタイルシート](../Page/スタイルシート.md "wikilink")
      - XSL
          - [XSLT](../Page/XSL_Transformations.md "wikilink")
          - [XPath](../Page/XML_Path_Language.md "wikilink")
          - [XSL-FO](../Page/XSL_Formatting_Objects.md "wikilink")
      - [DSSSL](../Page/Document_Style_Semantics_and_Specification_Language.md "wikilink")
      - [CSS](../Page/Cascading_Style_Sheets.md "wikilink")
  - [TeX](../Page/TeX.md "wikilink")
      - [LaTeX](../Page/LaTeX.md "wikilink")

## 外部リンク

  - [The Extensible Stylesheet Language Family (XSL)](http://www.w3.org/Style/XSL/) - [W3CのXSLのページ](../Page/World_Wide_Web_Consortium.md "wikilink")
  - [アンテナハウス](../Page/アンテナハウス.md "wikilink")社のページ（日本語）
      - [Antenna House XSL Formatter](http://www.antenna.co.jp/AHF/) - アンテナハウス社によるXSL-FOの商用処理系
      - [XSL-FO の基礎 第2版 - XML を組版するためのレイアウト仕様](http://www.antenna.co.jp/AHF/ahf_publication/index.html#fo-basis)
      - [スタイルシート開発の基礎 XML と FO で簡単な本を作ってみよう](http://www.antenna.co.jp/AHF/ahf_publication/index.html#XSLTTutorial)
  - [Extensible Stylesheet Language](http://xml.coverpages.org/xsl.html) - xml.coverpages.org
  - [What is XSL-FO?](http://www.xml.com/pub/a/2002/03/20/xsl-fo.html?page=1) - O'REILLY XML.com
  - [XML Focus Topics : CSS, XSL, XSL-FO](http://www.xml.org/xml/resources_focus_cssxslfo.shtml) - XML.org

<!-- end list -->

  - [xmlroff](http://xmlroff.sourceforge.net/) - [オープンソース](../Page/オープンソース.md "wikilink")の処理系
  - [Apache FOP](http://xmlgraphics.apache.org/fop/) - [Apache XML Graphics](../Page/Apache_XML_Graphics.md "wikilink") プロジェクトによるオープンソースの処理系。[PDF](../Page/Portable_Document_Format.md "wikilink")/[SVG](../Page/Scalable_Vector_Graphics.md "wikilink")/[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")などへの変換が可能

<!-- end list -->

  - [W3Cschools XSL Tutorial](http://www.w3schools.com/xsl/)

[Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:スタイルシート言語](https://ja.wikipedia.org/wiki/Category:スタイルシート言語 "wikilink")