> この記事は[XQuery](https://ja.wikipedia.org/wiki/XQuery)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:XML_languages.svg "wikilink") **XQuery**は、[静的型付け](https://ja.wikipedia.org/wiki/静的型付け "wikilink")機能を（実装依存の機能として）持つ[XMLデータ問合せの為の](../Page/Extensible_Markup_Language.md "wikilink")[問い合わせ言語](https://ja.wikipedia.org/wiki/問い合わせ言語 "wikilink")であり、[チューリング完全](../Page/チューリング完全.md "wikilink")な[関数型言語](../Page/関数型言語.md "wikilink")でもある。 [XPathの目的が木の節点を指し示す](../Page/XML_Path_Language.md "wikilink")（アドレッシング）ことであるのに対して、XQueryの目的はXMLデータソースのための照会機能を提供することである。

[関係モデル](../Page/関係モデル.md "wikilink") （[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")） における関係問合せが、数学的背景を有する[関係代数演算ないし](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\) "wikilink")[関係論理](../Page/関係論理.md "wikilink")演算に基づくように、XQuery問合せには[形式意味論](../Page/形式意味論.md "wikilink")が与えられている。

XQueryは**Quilt**と呼ばれる言語をベースに設計されているが、他にもXPath 1.0, [SQL](../Page/SQL.md "wikilink")、XQL、[OQL](https://ja.wikipedia.org/wiki/オブジェクト問い合わせ言語 "wikilink")、XML-QL、[MLといった言語の影響を受けている](https://ja.wikipedia.org/wiki/プログラミング言語ML "wikilink")。 2007年1月23日にXQuery 1.0の[W3Cでの標準化作業が終了し](../Page/World_Wide_Web_Consortium.md "wikilink")、勧告（）となった。その後はXQuery 3.0が2014年4月8日、XQuery 3.1が2017年3月21日に勧告された。

## XPath 1.0とXQuery 1.0 (XPath 2.0)

XQuery 1.0は[XPath](../Page/XML_Path_Language.md "wikilink") 2.0の拡張である。XPath 2.0でもXQuery 1.0でも構文的に正しく、かつ正常に実行される式は、いずれの言語でも同じ結果を返す。 一方で、XPath 1.0とXQueryのサブセットであるXPath 2.0とは、基本的性質に違いがある。 XPath 1.0では問合せ結果が重複のないノード集合と定義される一方で、XPath 2.0での問合せ結果は順序を持ち、値の重複を許すシーケンスである。 ただし、XPath 2.0にはXPath 1.0に対する後方互換性モードがオプションとして存在し、このオプションを利用することができる環境においては XPath 2.0でもXPath 1.0と同じ結果を得ることができる。

## 関連項目

  - [XML](../Page/Extensible_Markup_Language.md "wikilink")
  - [XPath](../Page/XML_Path_Language.md "wikilink")
  - [XSLT](../Page/XSL_Transformations.md "wikilink")
  - [OQL](https://ja.wikipedia.org/wiki/オブジェクト問い合わせ言語 "wikilink") ([オブジェクト問い合わせ言語](https://ja.wikipedia.org/wiki/オブジェクト問い合わせ言語 "wikilink"))
  - [SQL](../Page/SQL.md "wikilink")
  - [XMLデータベース](../Page/XMLデータベース.md "wikilink")
      - [ネイティブXMLデータベース](../Page/ネイティブXMLデータベース.md "wikilink")
  - [コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")
      - [プログラミング言語](../Page/プログラミング言語.md "wikilink")
          - [宣言型言語](https://ja.wikipedia.org/wiki/宣言型言語 "wikilink")
              - [関数型言語](../Page/関数型言語.md "wikilink")
      - [問い合わせ言語](https://ja.wikipedia.org/wiki/問い合わせ言語 "wikilink")

## 外部リンク

  - [Don ChamberlinによるXQueryの解説記事(Web Archive)](https://web.archive.org/web/20070119210131/http://www-06.ibm.com/jp/software/data/developer/library/techdoc/pdf/ii_sysjournal04.pdf)
  - [XQueryチュートリアル(@IT)](http://www.atmarkit.co.jp/fxml/tanpatsu/19quip/quip01.html)
  - [XQuery from the Experts: Influences on the design of XQuery](http://www-128.ibm.com/developerworks/xml/library/x-xqbook.html)

### 関連リソース

  - [xquery cover page](https://www.w3.org/TR/xquery/all/)
  - [XQuery 1.0: An XML Query Language (Second Edition)](https://www.w3.org/TR/2010/REC-xquery-20101214/) - W3C勧告
  - [XQuery 3.0: An XML Query Language](https://www.w3.org/TR/xquery-30/) - W3C勧告
  - [XQuery 3.1: An XML Query Language](https://www.w3.org/TR/xquery-31/) - W3C勧告
  - [XQuery 1.0 and XPath 2.0 Formal Semantics](http://www.w3.org/TR/xquery-semantics/)
  - [XQuery 1.0 and XPath 2.0 Data Model (XDM)](http://www.w3.org/TR/xpath-datamodel/)
  - [XQuery 1.0 and XPath 2.0 Functions and Operators](http://www.w3.org/TR/xquery-operators/)
  - [XSLT 2.0 and XQuery 1.0 Serialization](http://www.w3.org/TR/xslt-xquery-serialization/)
  - [Building a Tokenizer for XPath or XQuery](http://www.w3.org/TR/xquery-xpath-parsing/)
  - [XML Query Use Cases](http://www.w3.org/TR/xquery-use-cases/)
  - [XML Query Test Suite](http://www.w3.org/XML/Query/test-suite/)
  - [XQuery Update Facility](http://www.w3.org/TR/xqupdate/)
  - [XQuery 1.0 and XPath 2.0 Full-Text](http://www.w3.org/TR/xquery-full-text/)
  - [XQuery 1.0 and XPath 2.0 Functions and Operators Error Codes Namespace](http://www.w3.org/2005/xqt-errors/)
  - [XQuery 1.0 Grammar Test Page](http://www.w3.org/2005/qt-applets/xqueryApplet.html)
  - [XQuery implementations](http://www.w3.org/XML/Query/)
  - [JSR 225: XQuery API for JavaTM (XQJ)](http://jcp.org/en/jsr/detail?id=225)

[Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:関数型言語](https://ja.wikipedia.org/wiki/Category:関数型言語 "wikilink") [Category:問い合わせ言語](https://ja.wikipedia.org/wiki/Category:問い合わせ言語 "wikilink")