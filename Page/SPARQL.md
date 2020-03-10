> この記事は[SPARQL](https://ja.wikipedia.org/wiki/SPARQL)から翻訳されています。


**SPARQL**（スパークル\[1\]、**SPARQL Protocol and RDF Query Language**の[再帰的頭字語](https://ja.wikipedia.org/wiki/再帰的頭字語 "wikilink")）は、[RDF問合せ言語](https://ja.wikipedia.org/wiki/RDF問合せ言語 "wikilink")の１つである。RDF問合せ言語は、[Resource Description Framework (RDF)](../Page/Resource_Description_Framework.md "wikilink") で記述された[XMLやTurtleなどのRDFデータのリソースを取り扱うための](../Page/Extensible_Markup_Language.md "wikilink")[コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")である。

SPARQL は、[クエリ](https://ja.wikipedia.org/wiki/クエリ "wikilink")の基本的な[パターン](https://ja.wikipedia.org/wiki/パターン "wikilink")である[論理積](../Page/論理積.md "wikilink")や[論理和](../Page/論理和.md "wikilink")をはじめ、文字列操作やフィルターなどのその他のパターンを指定可能であり\[2\]、[Python](../Page/Python.md "wikilink")や[Ruby](../Page/Ruby.md "wikilink")などの[プログラミング言語](../Page/プログラミング言語.md "wikilink")でSPARQLを利用できるライブラリが存在する\[3\]。

[ティム・バーナーズ＝リー](../Page/ティム・バーナーズ＝リー.md "wikilink")は2006年5月のインタビューで「SPARQL によって大きな違いが生まれるだろう」と述べている\[4\]。

## 例

次のSPARQLクエリは、アフリカ諸国の首都のリストを返す。

``` sparql
PREFIX abc: <http://mynamespace.com/exampleOntologie#>
SELECT ?capital ?country
WHERE {
  ?x abc:cityname ?capital.
  ?y abc:countryname ?country.
  ?x abc:isCapitalOf ?y.
  ?y abc:isInContinent abc:africa.
}
```

変数は頭に "?" を付けることで表される（"$" でもよい）。?capital と ?country がクエリ結果として返される（SELECTの部分）。SPARQL のクエリプロセッサはその全てについて4つの RDF トリプルのパターンにマッチするものを選ぶ（WHEREの部分）。[URI](../Page/Uniform_Resource_Identifier.md "wikilink") を毎回フルに記述すると読みにくくなるので、"abc" というプレフィックスが "http://mynamespace.com/exampleOntologie\#" を表すようになっている（PREFIXの部分）。

## 標準化

SPARQL は [World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink") (W3C) の *RDF Data Access Working Group* (DAWG) によって標準化された。

W3C勧告に至る過程は以下の通りである

1.  2006年4月 勧告候補
2.  2006年10月 2つの問題により草案に戻される\[5\]
3.  2007年6月 SPARQL 1.0 再び勧告候補\[6\]
4.  2008年1月15日 SPARQL 1.0 W3C勧告\[7\]
5.  2013年3月21日 SPARQL 1.1 W3C勧告\[8\]

## SPARQL Endpoint

SPARQL Endpointは、SPARQLによるリソースの検索や分析の機能を提供するインタフェースである。

### 代表的な日本国内のSPARQL Endpoint

  - [DBpedia Japanese](http://ja.dbpedia.org/): <http://ja.dbpedia.org/sparql>
  - 文献検索システム[I-Scover](https://ja.wikipedia.org/wiki/I-Scover "wikilink"): <https://i-scover-api.ieice.org/iscover/api/sparql>
  - [J-GLOBAL knowledge](https://stirdf.jglobal.jst.go.jp/): <https://stirdf.jglobal.jst.go.jp/sparql>
  - [ジャパンサーチ](https://jpsearch.go.jp/): <https://jpsearch.go.jp/rdf/sparql/>

## 脚注

## 関連項目

  - [DBペディア](https://ja.wikipedia.org/wiki/DBペディア "wikilink")
  - [ウィキデータ](https://ja.wikipedia.org/wiki/ウィキデータ "wikilink")

## 外部リンク

### 書籍

  -
### 仕様、記事、チュートリアル

  - [SPARQLの主な特徴](http://www.w3.org/2004/Talks/1124-orf-sw/slide16-0.html)
  - [W3C RDF Data Access Working Group](http://www.w3.org/2001/sw/DataAccess/)
  - [XML.com: Introducing SPARQL: Querying the Semantic Web](http://www.xml.com/pub/a/2005/11/16/introducing-sparql-querying-semantic-web-tutorial.html)
  - [SPARQL Query language](http://www.w3.org/TR/sparql11-overview/)
  - [SPARQL Query Languageの日本語版](http://www.asahi-net.or.jp/~ax2s-kmtn/internet/rdf/REC-sparql11-overview-20130321.html)
  - [SPARQL Protocol](http://www.w3.org/TR/rdf-sparql-protocol/)
  - [SPARQL Protocolの日本語版](http://www.asahi-net.or.jp/~ax2s-kmtn/internet/rdf/rdf-sparql-protocol.html)
  - [SPARQL Query XML Results Format](http://www.w3.org/TR/rdf-sparql-XMLres/)
  - [SPARQL Query XML Results Formatの日本語版](http://www.asahi-net.or.jp/~ax2s-kmtn/internet/rdf/rdf-sparql-xmlres.html)
  - [SPARQL Frequently Asked Questions](http://thefigtrees.net/lee/sw/sparql-faq)
  - [SPARQL Tutorial on the Jena/ARQ site](http://jena.sourceforge.net/ARQ/Tutorial/index.html)

### ツールサポート

  - [AllegroGraph RDFStore](http://www.franz.com/products/allegrograph/)
  - [Protégé](http://protege.stanford.edu/)
  - [RDF api for PHP](http://sites.wiwiss.fu-berlin.de/suhl/bizer/rdfapi/)
  - [TopBraid Composer](http://www.topbraidcomposer.com)

### SPARQLクエリサービス・エンドポイント

  - [Pellet OWL Reasoner](http://pellet.owldl.com/)
  - [ARC](http://b4mad.net/sparqs/)
  - [SPARQLer](http://sparql.org/sparql.html)
  - [Virtuoso Universal Server](http://demo.openlinksw.com/sparql)
  - [DBpedia](http://DBpedia.org/sparql)

### SPARQLデモ

  - [SPARQL Calendar Demo](http://esw.w3.org/topic/SparqlCalendarDemo)
  - [SPARQL & Web Clipboard Demo](http://www.sparqlets.org/clipboard/demo)

[Category:問い合わせ言語](https://ja.wikipedia.org/wiki/Category:問い合わせ言語 "wikilink") [Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:World_Wide_Web](https://ja.wikipedia.org/wiki/Category:World_Wide_Web "wikilink") [Category:セマンティック・ウェブ](https://ja.wikipedia.org/wiki/Category:セマンティック・ウェブ "wikilink")

1.
2.
3.
4.
5.
6.  <http://www.w3.org/blog/SW/2007/06/15/sparql_is_a_candidate_recommendation>
7.  [W3C Semantic Web Activity News - SPARQL is a Recommendation](http://www.w3.org/blog/SW/2008/01/15/sparql_is_a_recommendation)
8.