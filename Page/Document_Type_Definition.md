> この記事は[Document Type Definition](https://ja.wikipedia.org/wiki/Document_Type_Definition)から翻訳されています。


**Document Type Definition**（文書型定義、**DTD**）とは、[マークアップ言語](../Page/マークアップ言語.md "wikilink")の[SGMLおよび](../Page/Standard_Generalized_Markup_Language.md "wikilink")[XMLにおいて](../Page/Extensible_Markup_Language.md "wikilink")、文書構造（文書型）を定義するための[スキーマ言語](https://ja.wikipedia.org/wiki/スキーマ言語 "wikilink")の一つである。

DTDでは、SGMLやXMLの文書内に記述することができる要素やその発生順序、発生回数、要素がもつ属性、属性の型などを記述することができる。

他のスキーマ言語と同様に、DTDにおいても、文書構造を厳密に定義することによって、SGMLやXMLの技術を利用する際の、処理の正確性や安全性を高めることができる。SGMLやXMLの文書処理を支援する[ライブラリ](../Page/ライブラリ.md "wikilink")の多くは、SGMLやXMLの文書がDTDによる文書構造に従っているかどうかを検証する機能を備えている。

もともとはSGMLのスキーマ言語として開発され、SGMLから派生したXMLにおいても、スキーマ言語として採用されている。例えば、SGMLの応用技術である[HTMLや](../Page/HyperText_Markup_Language.md "wikilink")、XMLの応用技術である [XHTMLでは](../Page/Extensible_HyperText_Markup_Language.md "wikilink")、DTDによって文書構造が定義されている。

現在では、XML技術を利用する場合には、スキーマ言語としてDTDを採用するケースは少なくなる傾向にある。XMLが勧告された後、DTDに対してはいくつかの欠点（XMLの文法とは異なる文法を採用していることや、[XML名前空間](https://ja.wikipedia.org/wiki/XML名前空間 "wikilink")に対応していないことなど）が問題として指摘されてきたためである。そのため、XML技術は広く普及したものの、DTDの欠点が XML技術を柔軟に活用する際の障害の一つとなっていた。

この問題を解決するために、新たなスキーマ言語として[RELAX NGや](https://ja.wikipedia.org/wiki/RELAX_NG "wikilink")[W3C](../Page/World_Wide_Web_Consortium.md "wikilink") [XML Schemaなどが開発され](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")、それらを採用する事例が増えている。

## DTDの構造

DTDは、**要素型宣言**、**属性リスト宣言**、**エンティティ宣言**（または、**実体参照宣言**）、**記法宣言**により構成される。

### 要素型宣言

対象の[SGML](../Page/Standard_Generalized_Markup_Language.md "wikilink")/[XML文書において使用する要素を宣言し](../Page/Extensible_Markup_Language.md "wikilink")、その要素の名前、関連する要素との親子関係および出現順序を定義する。

`<!ELEMENT `*`要素名`*` `*`構成要素`*`>`

このとき、要素名は、対象の要素の名前であり、構成要素は、以下の種類に分けられる。

#### EMPTY

対象要素に子要素が存在しない場合（例えば、後述する属性のみの場合など）に指定する。

``` dtd
<!ELEMENT foo1 EMPTY>
```

#### ANY

対象要素配下に任意の要素、任意のデータが格納される場合に指定する。

``` dtd
<!ELEMENT foo2 ANY>
```

#### 子要素

対象要素配下の子要素の順番および出現回数を指定する。

``` dtd
<!ELEMENT foo1 (bar1,(bar2|bar3)*)>
```

### 属性リスト宣言

対象のSGML/XML文書の要素が持つ属性の型やデフォルト値を定義する

`<!ATTLIST `*`要素名`*` `*`属性名`*` `*`属性値の候補、または型`*` `*`デフォルト値`*`>`

例えば、俳優の出身地域を属性として定義する場合、以下のような属性リストが考えられる。

`<!ATTLIST 俳優 出身地域 (北海道|東北|関東|甲信越|東海|北陸|近畿|四国|九州|沖縄) "関東">`
`...`
<俳優 出身地域="東海">`俳優A`</俳優>

### エンティティ宣言、記法宣言

エンティティ宣言は、対象のSGML/XML文書内に記述できるエンティティ参照について定義する。SGML/XML文書内でエンティティ参照を記述すると、DTDのエンティティ宣言にしたがって、文字列を置換したり、外部ファイルの内容を埋め込むことができる。

``` dtd
<!ENTITY greeting "こんにちは">
<!ENTITY external-file SYSTEM "external.xml">
```

記法宣言は、対象のSGML/XML文書内から参照する外部ファイルの種類 (例えばJPEGなど) を指定する。

## DTDの例

簡単なDTDの例を示す。

``` dtd
<!ELEMENT firstName (#PCDATA)>
<!ELEMENT secondName (#PCDATA)>
<!ELEMENT info ANY>
<!ELEMENT data (firstName,secondName,info?)>
<!ELEMENT myDocument (data)*>
<!ATTLIST data age CDATA #IMPLIED>
```

このDTDでは以下の内容が記述されている。

  - 第1行: `firstName`要素を宣言している。この要素は内容として文字列データをもつ。
  - 第2行: `secondName`要素を宣言している。内容として文字列データをもつ。
  - 第3行: `info`要素を宣言している。内容として、このDTDで宣言された任意の要素や文字列データを、もつことができる。
  - 第4行: `data`要素を宣言している。内容として`firstName`、`secondName`、`info`の各要素をもつ。要素の出現順序はこの順番でなければならない（例えば `firstName` の前に`secondName`が出現してはならない）。`?` はオプショナルであることを示す。`info`要素は`secondName`要素の後に、出現しても良いし出現しなくても良い。
  - 第5行: `myDocument`要素を宣言している。内容として0個からn個の`data`要素をもつ。
  - 第6行: `data`要素の属性リスト宣言をしている。`data`要素は`age`属性をもつ。`age`属性は文字列データであり、省略することが可能である。

このDTDに従って作成したXML文書の例

``` xml
 <?xml version="1.0" encoding="UTF-8"?>
 <!DOCTYPE myDocument SYSTEM "example.dtd">
 <myDocument>
   <data age="29">
     <firstName>Fred</firstName>
     <secondName>Bloggs</secondName>
   </data>
   <data>
     <firstName>Tony</firstName>
     <secondName>Blair</secondName>
     <info>PM of UK</info>
   </data>
 </myDocument>
```

## 関連項目

  - [コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")
      - [データ記述言語](https://ja.wikipedia.org/wiki/データ記述言語 "wikilink")
          - [仕様記述言語](https://ja.wikipedia.org/wiki/仕様記述言語 "wikilink")
              - [スキーマ言語](https://ja.wikipedia.org/wiki/スキーマ言語 "wikilink")
  - [文書型宣言](https://ja.wikipedia.org/wiki/文書型宣言 "wikilink")

[Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:データモデリング](https://ja.wikipedia.org/wiki/Category:データモデリング "wikilink") [Category:メタデータ](https://ja.wikipedia.org/wiki/Category:メタデータ "wikilink")