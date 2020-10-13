> この記事は[Document Style Semantics and Specification Language](https://ja.wikipedia.org/wiki/Document_Style_Semantics_and_Specification_Language)から翻訳されています。


**Document Style Semantics and Specification Language** (**DSSSL**) は、[マークアップ言語](../Page/マークアップ言語.md "wikilink") [SGML](../Page/Standard_Generalized_Markup_Language.md "wikilink") もしくは [XML](../Page/Extensible_Markup_Language.md "wikilink") で記述された文書のための、[スタイルシート](../Page/スタイルシート.md "wikilink")言語の一つである。 DSSSL は「ディッセル」と読む。 DSSSL に含まれるうちの "expression language" は、プログラミング言語[Scheme](../Page/Scheme.md "wikilink")の[部分集合](../Page/部分集合.md "wikilink")をベースとしている。具体的には、Schemeのうちの副作用を取り除いた（side-effect free）関数的な（functional）機能だけから成る、Schemeの部分集合（subset of Scheme）だけを使っている。\[1\]\[2\] DSSSL の開発には、[ジェームズ・クラークなどの人々が関わった](../Page/ジェームズ・クラーク_\(ソフトウェア技術者\).md "wikilink")。 1996年に [ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")/[IEC](../Page/国際電気標準会議.md "wikilink") 10179:1996 として規格が定められた（対応する[日本工業規格](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink")は JIS X 4153）。

DSSSL を使うことにより、SGML文書やXML文書を、[TeX](../Page/TeX.md "wikilink")、[PDF](../Page/Portable_Document_Format.md "wikilink")、[HTML](../Page/HyperText_Markup_Language.md "wikilink")、[RTF](../Page/Rich_Text_Format.md "wikilink") などの、人間にとって読みやすいさまざまな形式に変換して、コンピュータの画面に表示することや紙に印刷することができる。 SGML文書やXML文書の内容は、[コンピュータ](../Page/コンピュータ.md "wikilink")の[ソフトウェア](../Page/ソフトウェア.md "wikilink")にとっては読みやすい構造であるが、人間にとってより読みやすい形式が望まれることがある。 DSSSL のような[スタイルシート](../Page/スタイルシート.md "wikilink")言語を使うことにより、SGML文書やXML文書を、人間にとって読みやすい[組版](../Page/組版.md "wikilink")された形式に変換することができる。

DSSSL がよく使われる用途の一つは、[DocBook](../Page/DocBook.md "wikilink")（文書を記述するための SGML/XML技術）で記述された文書の組版である。

DSSSL は、当初は SGML文書のためのスタイルシート言語として開発されたが、XML文書のスタイルシート言語としても、使うことができる。

現在では、DSSSL とは別のスタイルシート言語である [XSL](../Page/Extensible_Stylesheet_Language.md "wikilink") ([XSLT](../Page/XSL_Transformations.md "wikilink")、[XSL-FO](../Page/XSL_Formatting_Objects.md "wikilink")) や [CSS](../Page/Cascading_Style_Sheets.md "wikilink") が使われる事例が多くなっている。

XSL (XSLT、XSL-FO) は、DSSSL の技術をもとに開発された。

## DSSSL処理系の機能

DSSSL の処理系には次の 2つの機能がある。

1.  [SGML](../Page/Standard_Generalized_Markup_Language.md "wikilink") もしくは [XML](../Page/Extensible_Markup_Language.md "wikilink") の文書を、構造の異なる別の SGML/XML文書に変換する機能
2.  SGML/XML文書を人間に読みやすいように[組版](../Page/組版.md "wikilink")して、コンピュータの画面に表示したり紙に印刷することができるようにする機能

例えば、SGML/XML文書を、DSSSL処理系を使って、[TeX](../Page/TeX.md "wikilink")、[PDF](../Page/Portable_Document_Format.md "wikilink")、[HTML](../Page/HyperText_Markup_Language.md "wikilink")、[RTF](../Page/Rich_Text_Format.md "wikilink") などの形式のファイルに変換することができる (変換先として指定できるファイルの種類は、DSSSL処理系によって異なる)。

また組版機能を使わずに、SGML/XML文書を構造の異なる別の SGML/XML文書に変換するために、DSSSL処理系を使うことができる。

## DSSSL処理系の実装

DSSSL処理系には、商用のものとフリーのものとがある。 フリーの処理系としては、[ジェームズ・クラークが中心となって開発した](../Page/ジェームズ・クラーク_\(ソフトウェア技術者\).md "wikilink") Jade、およびそれから派生した OpenJade がある。

## 脚注

## 外部リンク

  - [DSSSL 規格の最終版](ftp://ftp.ornl.gov/pub/sgml/WG8/DSSSL/) - [README](../Page/リードミー.md "wikilink") ファイルの著作権の記述を確認してください
  - [DSSSL で記述したスタイルシートの例](http://www.prescod.net/xsl/slides/8.html)
  - [ジェームズ・クラークの DSSSL のウェブページ](http://www.jclark.com/dsssl/)
  - [Jade : フリーの DSSSL処理系](http://www.jclark.com/jade/) - ジェームズ・クラークが中心となって開発した
  - [OpenJade : フリーの DSSSL処理系](http://openjade.sourceforge.net/) - Jade から派生して開発されている
  - [NEXT SOLUTION : 日本のソフトウェア企業](http://www.nextsolution.co.jp/) - DSSSL の技術情報、商用の DSSSL処理系 (DSSSLprint、NEXTPublisher)
  - [JIS X 4153 Draft](http://www.y-adagio.com/public/standards/jis_dsssl/dsssl.htm)

[Category:ISO/IEC標準](https://ja.wikipedia.org/wiki/Category:ISO/IEC標準 "wikilink") [Category:スタイルシート言語](https://ja.wikipedia.org/wiki/Category:スタイルシート言語 "wikilink") [Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink") [Category:Scheme](https://ja.wikipedia.org/wiki/Category:Scheme "wikilink")

1.  <http://www.jclark.com/dsssl/split/dsssl-5.html>
2.  そのように極めて限定された部分集合ならば、Scheme以外の任意のLispの方言でも、議論はたいして違わない。