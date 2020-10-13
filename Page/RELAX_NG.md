> この記事は[RELAX NG](https://ja.wikipedia.org/wiki/RELAX_NG)から翻訳されています。


**RELAX NG** （リラクシング、RELAX Next Generation） は、[マークアップ言語](../Page/マークアップ言語.md "wikilink")[XMLの](../Page/Extensible_Markup_Language.md "wikilink")[スキーマ言語](../Page/スキーマ言語.md "wikilink")の一つである。RELAX NG で記述された[スキーマは](../Page/スキーマ_\(データベース\).md "wikilink")、XML文書の構造と内容のパターンを定義する。RELAX NG で記述されたスキーマは、それ自身がXML文書である。RELAX NG でスキーマをXML文書として記述する方法を、[XML構文という](https://ja.wikipedia.org/wiki/#XML構文 "wikilink")。しかし RELAX NG では、スキーマをXML構文ではない簡潔な[短縮構文](https://ja.wikipedia.org/wiki/#短縮構文 "wikilink") (Compact Syntax) で記述することもできる\[1\]。つまり RELAX NG では、XML構文でスキーマを記述しても良いし、短縮構文でスキーマを記述しても良い。RELAX NG は、[W3C](../Page/World_Wide_Web_Consortium.md "wikilink") [XML Schema](https://ja.wikipedia.org/wiki/XML_Schema "wikilink") と比べて仕様が簡潔である。RELAX NG は、[ジェームズ・クラークと](../Page/ジェームズ・クラーク_\(ソフトウェア技術者\).md "wikilink")[村田真](../Page/村田真.md "wikilink")が共同で設計した。2001年12月に、[OASISの](../Page/OASIS_\(組織\).md "wikilink") RELAX NG 技術委員会が、RELAX NG の仕様を標準として策定した\[2\]\[3\]。2003年に、[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")/[IEC](../Page/国際電気標準会議.md "wikilink") 19757-2 ([文書スキーマ定義言語](../Page/文書スキーマ定義言語.md "wikilink") 第2部 正規文法に基づく妥当性検証) として策定し、2008年に改定している\[4\]。

## 背景

[マークアップ言語](../Page/マークアップ言語.md "wikilink") [SGML](../Page/Standard_Generalized_Markup_Language.md "wikilink") から使われてきた[スキーマ言語](../Page/スキーマ言語.md "wikilink")であった [DTD](../Page/Document_Type_Definition.md "wikilink") は、[XMLで使う際には](../Page/Extensible_Markup_Language.md "wikilink")、XMLの構文規則を満たしていないなど、様々な問題を有していた。そのため、[W3C](../Page/World_Wide_Web_Consortium.md "wikilink") によって [XML Schema](https://ja.wikipedia.org/wiki/XML_Schema "wikilink") が開発されたが、標準化に時間がかかり、また標準化のために巨大化・複雑化しすぎたとの批判から、独自にスキーマ言語を開発する動きが出た。

[村田真](../Page/村田真.md "wikilink")などの人々は、 [Regular Language description for XML](https://ja.wikipedia.org/wiki/Regular_Language_description_for_XML "wikilink") (RELAX) を開発した。[ジェームズ・クラークは](../Page/ジェームズ・クラーク_\(ソフトウェア技術者\).md "wikilink")、[TREX](https://ja.wikipedia.org/wiki/TREX "wikilink") (Tree Regular Expressions for XML) を開発した。クラークと村田は、RELAX NG を、TREX と RELAX Core に基づいて、この2つのスキーマ言語を統合する形で設計した。

## RELAX NG で記述されたスキーマを使う例

一冊の書籍 (book) を記述するための簡単な[XML文書のためのスキーマを定義することを](../Page/Extensible_Markup_Language.md "wikilink")、考える。一冊の書籍は、一つもしくは複数の (one or more) ページ (page) の並びとして定義される。おのおののページは、テキスト (text) のみを含む。一冊の書籍を記述するXML文書インスタンスの例を次に示す。

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<book>
  <page>これは1ページです。</page>
  <page>これは2ページです。</page>
</book>
```

### XML構文

RELAX NG を使ったスキーマは、他の要素の定義を含めたルート要素を定義することにより、[入れ子構造で記述することができる](../Page/ネスティング.md "wikilink")。要素の定義自身に、パターンの定義を埋め込むことができる。この方法を使って、書籍のXML文書のスキーマをXML構文で次のように記述することができる。

``` xml
<element name="book" ns="http://relaxng.org/ns/structure/1.0">
   <oneOrMore>
      <element name="page">
         <text/>
      </element>
   </oneOrMore>
</element>
```

入れ子構造では、深い階層構造をもつXML文書については扱いにくく、また[再帰的](https://ja.wikipedia.org/wiki/再帰的 "wikilink")な要素を定義することはできない。このため、RELAX NGを使った多くのスキーマでは「名前付パターン」定義への参照を使う。名前付パターンの定義は、スキーマ内で名前付パターンへの参照とは分離して記述される。次に示す「フラットなスキーマ」では、先述のスキーマの例と全く同じマークアップを正確に定義する。

``` xml
<grammar ns="http://relaxng.org/ns/structure/1.0">
   <start>
      <element name="book">
         <oneOrMore>
            <ref name="page"/>
         </oneOrMore>
      </element>
   </start>
   <define name="page">
      <element name="page">
         <text/>
      </element>
   </define>
</grammar>
```

### 短縮構文

RELAX NG 短縮構文は、XMLに準拠しない形式である。短縮構文は、同等なXML構文のスキーマに正確に変換することが可能であり、また逆にXML構文のスキーマから同等な短縮構文のスキーマに正確に変換することが可能である。つまりXML構文と短縮構文は、構造および意味的に一対一に対応している。これは、Simple Outline XML (SOX; [:en:Simple Outline XML](https://ja.wikipedia.org/wiki/:en:Simple_Outline_XML "wikilink")) とXMLの関係と同様である。短縮構文は、[DTDの構文と多くの機能を共有している](../Page/Document_Type_Definition.md "wikilink")。以下に入れ子構造の短縮構文によるスキーマの例を示す。

``` rnc
element book
{
    element page { text }+
}
```

また上記のスキーマは、名前付パターンを使って以下のようにも定義できる。

``` rnc
start = element book { page+ }
page = element page { text }
```

これらふたつのスキーマは意味的に同等である。

## W3C XML Schema との比較

RELAX NG の仕様は、[W3C](../Page/World_Wide_Web_Consortium.md "wikilink") [XML Schema](https://ja.wikipedia.org/wiki/XML_Schema "wikilink") の仕様とほぼ同じ時期に設計された。XML Schema が策定された2001年の時点では、RELAX NG よりも XML Schema の方が、より多くの技術者に名前を知られており、より多くの[オープンソース](../Page/オープンソース.md "wikilink")および商用の妥当性検証器 (バリデータ) やエディタが実装されていた。しかしその後、RELAX NG はこのスキーマ戦争を順調に戦い抜き、[XMLを扱う多くの](../Page/Extensible_Markup_Language.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")でサポートされるようになっている。[DocBook](../Page/DocBook.md "wikilink")、[TEIガイドライン](https://ja.wikipedia.org/wiki/Text_Encoding_Initiative "wikilink")、[OpenDocument](../Page/OpenDocument.md "wikilink")のような広く使われている文書指向の[マークアップ言語](../Page/マークアップ言語.md "wikilink")は、RELAX NG を第一のスキーマとして採用している。

RELAX NG と W3C XML Schema は、多くの機能を共有している。この2つの現代的なスキーマ言語は、従来使われてきた[DTDとは](../Page/Document_Type_Definition.md "wikilink")、多くの面で異なっている。RELAX NG と XML Schema がともにもつ機能としては、次のようなものがある。

  - 充実した[データ型](../Page/データ型.md "wikilink")
  - [正規表現](../Page/正規表現.md "wikilink")のサポート
  - [XML名前空間](https://ja.wikipedia.org/wiki/XML名前空間 "wikilink")のサポート
  - 複雑な構造の定義への参照機能

## ファイル名の接尾辞 (拡張子)

非公式的な慣習として、RELAX NG のXML構文で記述されたスキーマは、ファイルの名称の接尾辞 ([拡張子](../Page/拡張子.md "wikilink")) として ".rng" が使われている。短縮構文のスキーマのファイル名の接尾辞は、".rnc" が使われている。

## 妥当性検証器の実装

RELAX NG の妥当性検証器 (バリデータ) の[実装](../Page/実装.md "wikilink")として利用可能なものの一部を示す。いずれも[オープンソース](../Page/オープンソース.md "wikilink")の[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。

  - Jing - [ジェームズ・クラーク](../Page/ジェームズ・クラーク_\(ソフトウェア技術者\).md "wikilink")

  - Sun Multi-Schema Validator (MSV) - [サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")、川口耕介

  - \- [GNOME](../Page/GNOME.md "wikilink")プロジェクト

## 関連項目

  - [生け垣オートマトン](https://ja.wikipedia.org/wiki/生け垣オートマトン "wikilink")
  - [スキーマ言語](../Page/スキーマ言語.md "wikilink")
  - [Document Type Definition](../Page/Document_Type_Definition.md "wikilink") (DTD、文書型定義)
  - [Regular Language description for XML](https://ja.wikipedia.org/wiki/Regular_Language_description_for_XML "wikilink") (RELAX)
  - [TREX](https://ja.wikipedia.org/wiki/TREX "wikilink") (Tree Regular Expressions for XML)

<!-- end list -->

  - [文書スキーマ定義言語](../Page/文書スキーマ定義言語.md "wikilink") (DSDL)
  - [スキマトロン](../Page/スキマトロン.md "wikilink")
  - [W3C](../Page/World_Wide_Web_Consortium.md "wikilink") [XML Schema](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")

## 注釈・出典

<references/>

## 外部リンク

  - [RELAX NG ホームページ](http://www.relaxng.org/)
  - [RELAX NG 仕様書](http://www.asahi-net.or.jp/~eb2m-mrt/relaxngjis/jaspec-20011203.html)
  - [RELAX NG 日本語ポータル](http://fortunecat.sourceforge.net/)
  - [RELAX NG 入門 (XML構文)](http://www.kohsuke.org/relaxng/tutorial.ja.html)
  - [RELAX NG 入門 (短縮構文)](http://relaxng.org/compact-tutorial-20030326.html)
  - ["The Design of RELAX NG"](http://www.thaiopensource.com/relaxng/design.html) - [ジェームズ・クラーク](../Page/ジェームズ・クラーク_\(ソフトウェア技術者\).md "wikilink")
  - [XML文書の構造を設計するためのデザインパターン](http://www.xmlpatterns.com/)
  - [RELAX NG Book](http://books.xmlschemata.org/relaxng/) - Eric van der Vlist, [GNU Free Documentation Licenseのもとで公開](../Page/GNU_Free_Documentation_License.md "wikilink")
  - [Relax NG Reference](http://www.zvon.org/xxl/RelaxNG/Output/) - ZVON
  - [RELAX NG Java community projects](https://relax-ng.dev.java.net/) - java.net

### 妥当性検証器の実装のリンク

  - [Jing](http://www.thaiopensource.com/relaxng/jing.html) - [ジェームズ・クラーク](../Page/ジェームズ・クラーク_\(ソフトウェア技術者\).md "wikilink")
  - [Sun Multi-Schema Validator (MSV)](https://msv.dev.java.net/) - [オープンソース](../Page/オープンソース.md "wikilink")、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")、川口耕介
  - [Relax NG Compact Syntax validator](http://sourceforge.net/projects/rnv/) -- オープンソースの C プログラム

[Category:ISO/IEC標準](https://ja.wikipedia.org/wiki/Category:ISO/IEC標準 "wikilink") [Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:データモデリング](https://ja.wikipedia.org/wiki/Category:データモデリング "wikilink")

1.  [RELAX NG Compact Syntax](http://www.oasis-open.org/committees/relax-ng/compact-20021121.html)
2.  [RELAX NG Specification](http://www.oasis-open.org/committees/relax-ng/spec-20011203.html)
3.  [RELAX NG Technical Committee](http://www.oasis-open.org/committees/tc_home.php?wg_abbrev=relax-ng)
4.  ISO/IEC 19757-2:2008 Information technology - Document Schema Definition Language (DSDL) - Part 2: Regular-grammar-based validation - RELAX NG <https://www.iso.org/standard/52348.html>