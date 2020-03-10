> この記事は[Apache FOP](https://ja.wikipedia.org/wiki/Apache_FOP)から翻訳されています。


**Apache FOP**（アパッチ・エフオーピー）は、[組版](../Page/組版.md "wikilink")のための[XMLに準拠した](../Page/Extensible_Markup_Language.md "wikilink")[マークアップ言語](../Page/マークアップ言語.md "wikilink")である[XSL-FOの処理系の](https://ja.wikipedia.org/wiki/XSL_Formatting_Objects "wikilink")[実装](https://ja.wikipedia.org/wiki/実装 "wikilink")であり、[Apache XML Graphics](../Page/Apache_XML_Graphics.md "wikilink") プロジェクトにより開発されている。 なお "FOP" は **F**ormatting **O**bjects **P**rocessor の[頭字語](../Page/頭字語.md "wikilink")である。 [Apacheライセンス](https://ja.wikipedia.org/wiki/Apacheライセンス "wikilink")による[オープンソース](../Page/オープンソース.md "wikilink")の[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。 FOPは、[プログラミング言語](../Page/プログラミング言語.md "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で実装されている。 FOPを使うことで、XSL-FOに準拠したXML文書を[PDFファイルなどのファイル形式に変換したり](../Page/Portable_Document_Format.md "wikilink")、[コンピュータ](../Page/コンピュータ.md "wikilink")の画面や[プリンタに直接](https://ja.wikipedia.org/wiki/プリンター "wikilink")[出力](https://ja.wikipedia.org/wiki/出力 "wikilink")することができる。

バージョン 0.94 の[ソースコード](../Page/ソースコード.md "wikilink")は、以前の安定版バージョンである 0.20.5 から大幅なソースコードの書き直しが行われている。

Apache FOP の配布物には、[XSLTの処理系である](../Page/XSL_Transformations.md "wikilink") [Apache Xalan](https://ja.wikipedia.org/wiki/Apache_Xalan "wikilink") が同梱されている。

## FOPで扱うことができるXSL-FO埋め込み画像形式

Apache FOP は、多くの形式の画像ファイルを[XSL-FO文書に](https://ja.wikipedia.org/wiki/XSL_Formatting_Objects "wikilink") ( <fo:external-graphic> 要素を使うことにより) 埋め込んで扱うことができる。

Apache FOP が扱うことができる埋め込み画像の形式には次のようなものがある。

  - [SVG](../Page/Scalable_Vector_Graphics.md "wikilink")
  - [ビットマップ](../Page/Windows_bitmap.md "wikilink") (BMP)
  - [PostScript](../Page/PostScript.md "wikilink") ([EPSを扱うことができる](../Page/Encapsulated_PostScript.md "wikilink"))
  - [JPEG](../Page/JPEG.md "wikilink")
  - いくつかの [TIFF](../Page/Tagged_Image_File_Format.md "wikilink") 形式

## FOPで可能な出力形式

Apache FOP は次の形式で[XSL-FO文書を出力することができる](https://ja.wikipedia.org/wiki/XSL_Formatting_Objects "wikilink")。

  - [PDF](../Page/Portable_Document_Format.md "wikilink") (FOPでは最も良好な出力が得られる)
  - [プリンタへの直接出力](https://ja.wikipedia.org/wiki/プリンター "wikilink")
  - [コンピュータ](../Page/コンピュータ.md "wikilink")の画面への直接出力 (Java2D/[AWT](../Page/Abstract_Window_Toolkit.md "wikilink"))
  - [PostScript](../Page/PostScript.md "wikilink")
  - [PCL](https://ja.wikipedia.org/wiki/PCL "wikilink") ([Printer Command Language](https://ja.wikipedia.org/wiki/:en:Printer_Command_Language "wikilink"))
  - AFP ([Advanced Function Presentation](https://ja.wikipedia.org/wiki/:en:Advanced_Function_Presentation "wikilink"))
  - [RTF](https://ja.wikipedia.org/wiki/Rich_Text_Format "wikilink")
  - [テキストファイル](https://ja.wikipedia.org/wiki/テキストファイル "wikilink")
  - [XML](../Page/Extensible_Markup_Language.md "wikilink") (Area Tree XML)
  - [TIFF](../Page/Tagged_Image_File_Format.md "wikilink")
  - [PNG](../Page/Portable_Network_Graphics.md "wikilink")
  - MIF ([Maker Interchange Format](https://ja.wikipedia.org/wiki/:en:Maker_Interchange_Format "wikilink"))
  - [SVG](../Page/Scalable_Vector_Graphics.md "wikilink")

## 脚注

## 関連項目

  - [XSL Formatting Objects](https://ja.wikipedia.org/wiki/XSL_Formatting_Objects "wikilink") (XSL-FO)
  - [Extensible Stylesheet Language](https://ja.wikipedia.org/wiki/Extensible_Stylesheet_Language "wikilink") (XSL：拡張可能な[スタイルシート](../Page/スタイルシート.md "wikilink")言語)
  - [XSL Formatter](../Page/XSL_Formatter.md "wikilink") - [アンテナハウス](https://ja.wikipedia.org/wiki/アンテナハウス "wikilink")が開発・販売している商用のXSL-FO処理系

## 外部リンク

  - [Apache FOP プロジェクト](http://xmlgraphics.apache.org/fop/)
  - [XMLツールのコレクション](http://www.data2type.de/software/antillesxml) (ドイツ語)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink")