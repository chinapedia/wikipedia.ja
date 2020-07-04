> この記事は[XMLBeans](https://ja.wikipedia.org/wiki/XMLBeans)から翻訳されています。


{{ Infobox_Software | 名称 = Apache XMLBeans | 開発元 = [Apacheソフトウェア財団](../Page/Apacheソフトウェア財団.md "wikilink") | 最新版 = 3.0.2 | 最新版発表日 =  | 対応プラットフォーム = [クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink") | 種別 = [XMLデータバインディング](https://ja.wikipedia.org/wiki/XMLデータバインディング "wikilink") | ライセンス = [Apache License](../Page/Apache_License.md "wikilink") 2.0 | 公式サイト = <http://xmlbeans.apache.org> }}

**XMLBeans**（エックスエムエルビーンズ）は、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")と[XMLデータバインディング](https://ja.wikipedia.org/wiki/XMLデータバインディング "wikilink")との変換を行うフレームワーク。[Apacheソフトウェア財団](../Page/Apacheソフトウェア財団.md "wikilink")の[XMLプロジェクトの一部である](../Page/Extensible_Markup_Language.md "wikilink")。2013年6月に開発を一旦終了したが、その後[Apache POIプロジェクトの一部として](../Page/Apache_POI.md "wikilink")2018年6月に開発が再開された\[1\]。

## 概要

XMLBeans は、Java が扱いやすい形でXMLの全ての能力へのアクセスを可能にするツールである。すなわち、XMLと [XML Schema](https://ja.wikipedia.org/wiki/XML_Schema "wikilink") の表現能力の豊かさと機能を利用し、それらの機能を可能な限り自然な形でJava言語とその型付き構成要素にマッピングする。XMLBeans は XML Schema を使って Java インタフェースとクラスをコンパイルし、その生成物を使ってXMLインスタンスデータのアクセスと変更を行う。XMLBeans を使うと、新たなインタフェースやクラスを使うのと同じ感覚でXMLインスタンスデータにアクセスできる。XMLインスタンスデータへのアクセスを提供する以外に、[XML Infoset](https://ja.wikipedia.org/wiki/XML_Information_Set "wikilink") への完全なアクセスを可能にするAPIを備え、XML Schema Object モデルを通して XML Schema 自体への[リフレクションも可能にする](../Page/リフレクション_\(情報工学\).md "wikilink")。

### 他との違い

  - [XML Schema](https://ja.wikipedia.org/wiki/XML_Schema "wikilink") 完全サポート
    XMLBeans は XML Schema を完全サポートしており、対応するJavaクラスは XML Schema の主な機能を全て提供する。この種の技術では、必要な機能をサポートしていないことが多く、非常に重要な特徴である。また、XML Schema 向けアプリケーションの構築に際して XML Schema の全能力を活用するようにでき、サブセットに制限されることがない。
  - 完全な [XML Infoset](https://ja.wikipedia.org/wiki/XML_Information_Set "wikilink") 再現性
    XMLインスタンスをアンマーシャリングしたとき、完全な XML Inforset が保持され、開発者が利用できる。XML のサブセットは容易に Java で表現できない部分があるため、これは重要である。例えば、要素の順序やコメントがアプリケーションによっては必要になるかもしれない。

### 目的

XMLBeans の主な目的は、ストリーミング以外の（メモリ上の）あらゆるXMLプログラミングで利用可能なものを構築することであった。XML Schema をコンパイルしてJavaクラスを生成したいとき

1.  あらゆる Schema について XMLBeans が利用可能であり、
2.  任意の必要なレベルのXMLへのアクセスを得ることができ、別々のツールを使う必要がない。

### API

以上のような目的を達成するため、XMLBeans は以下の3つの[APIを提供している](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

  - XmlObject
    XML Schema から生成されるJavaクラスは全て XmlObject を継承する。これにより、XMLに定義されている各要素について強く型付けされたゲッターとセッターを提供する。複合型の要素は XmlObject のインスタンスである。例えば、getCustomer が返す CustomerType は実際には XmlObject クラスを継承したクラス（のインスタンス）である。単純型の場合は通常のJavaのデータ型のゲッターとセッターになる。例えば、getName が String クラスのインスタンスを返すなど。
  - XmlCursor
    任意の XmlObject のインスタンスから XmlCursor クラスのインスタンスを得ることができる。これを使って、XML Inforset に直接アクセスできる。カーソルはXMLインスタンスでの位置を表現している。カーソルは文字単位やトークン単位など任意の細かさで前後に移動可能である。
  - SchemaType
    基になっているスキーマメタ情報へのアクセスを提供するクラス。例えば、ある XML Schema のサンプルインスタンスを生成したい場合や、ある要素がとりうる値を列挙したい場合などに利用できる。

これらは全て、性能を考慮して構築されている。XMLBeans は一般に非常に性能がよいと言われている。

## 例

以下は、国を表現したXMLスキーマ定義の簡単な例である。

``` xml
 <?xml version="1.0" encoding="UTF-8"?>
 <xs:schema targetNamespace="http://www.openuri.org/domain/country/v1"
            xmlns:tns="http://www.openuri.org/domain/country/v1"
            xmlns:xs="http://www.w3.org/2001/XMLSchema"
            elementFormDefault="qualified"
            attributeFormDefault="unqualified"
            version="1.0">
   <xs:element name="Country" type="tns:Country"/>
   <xs:complexType name="Country">
     <xs:sequence>
       <xs:element name="Name" type="xs:string"/>
       <xs:element name="Population" type="xs:int"/>
       <xs:element name="Iso" type="tns:Iso"/>
     </xs:sequence>
   </xs:complexType>
   <xs:complexType name="Iso">
     <xs:annotation><xs:documentation>ISO 3166</xs:documentation></xs:annotation>
     <xs:sequence>
       <xs:element name="Alpha2" type="tns:IsoAlpha2"/>
       <xs:element name="Alpha3" type="tns:IsoAlpha3"/>
       <xs:element name="CountryCode" type="tns:IsoCountryCode"/>
     </xs:sequence>
   </xs:complexType>
   <xs:simpleType name="IsoCountryCode">
     <xs:restriction base="xs:int">
       <xs:totalDigits value="3"/>
     </xs:restriction>
   </xs:simpleType>
   <xs:simpleType name="IsoAlpha2">
     <xs:restriction base="xs:string">
       <xs:pattern value="[A-Z]{2}"/>
       <xs:whiteSpace value="collapse"/>
     </xs:restriction>
   </xs:simpleType>
   <xs:simpleType name="IsoAlpha3">
     <xs:restriction base="xs:string">
       <xs:pattern value="[A-Z]{3}"/>
       <xs:whiteSpace value="collapse"/>
     </xs:restriction>
   </xs:simpleType>
 </xs:schema>
```

このスキーマをXMLBeanクラスに（例えば [Antを使って](../Page/Apache_Ant.md "wikilink")）コンパイルすると、スキーマ定義に従ったXMLデータを容易に生成・操作できるコードが生成される。以下のJavaコードは、XML文書の生成と評価の様子を簡単に示したものである。

``` java
 import org.openuri.domain.country.v1.Country;
 import org.openuri.domain.country.v1.Iso;
 public class CountrySample
 {
   public static void main(String[] args) {
     Country country = Country. Factory.newInstance();
     country.setName("Denmark");
     country.setPopulation(5450661);  // wikipedia より :-)
     // country XMLBean を XML として表示
     System.out.println(country.xmlText());
     // 文書が妥当かチェック - "Document is invalid" と表示するだろう
     // オブジェクトに必要な Iso 子要素が生成されていないため
     System.out.println ("Document is " + (country.validate() ? "valid" : "invalid"));
     // 複合型 Iso の子要素を追加し、文書を妥当なものにする
     Iso iso = country.addNewIso();
     iso.setAlpha2("DK");
     iso.setAlpha3("DNK");
     iso.setCountryCode(208);
     // country XMLBean を XML として表示
     System.out.println(country.xmlText());
     // 文書が妥当かチェック - "Document is valid" と表示されるだろう
     System.out.println ("Document is " + (country.validate() ? "valid" : "invalid"));
   }
 }
```

## 歴史

David Bau は[BEAシステムズ](../Page/BEAシステムズ.md "wikilink")在籍時（現在は[Google](../Page/Google.md "wikilink")勤務）に XMLBeans プロジェクトを開始した。彼はそのツールの主任設計者であり、チームを率いて XMLBeans 1.0 を設計・実装した。

XMLBeans は、BEA [WebLogic](https://ja.wikipedia.org/wiki/WebLogic "wikilink") にかつて含まれていたXMLバインディングツール XMLMaps を基盤としていた。XMBeans は当初 BEA WebLogic Workshop Framework というプロプライエタリな製品の一部として開発された。しかし2003年1月27日に初めて発表された当初から、BEA はこれを[オープン標準](../Page/オープン標準.md "wikilink")にしたいと表明していた。その時点では、BEAが標準化をどの団体に任せるかは明らかではなかったが、2003年中にApacheソフトウェア財団への寄贈が行われた。

  - 2003年1月27日: BEA が XMLBeans 技術プレビューとして公表。
  - 2003年9月24日: BEA が XMLBeans をApacheソフトウェア財団に寄贈。[Apache Incubator](https://ja.wikipedia.org/wiki/Apache_Incubator "wikilink") プロジェクトの一部となる。
  - 2004年4月23日: XMLBeans Version 1.0.2 リリース。 Incubator プロジェクトからの最初のリリース。
  - 2004年6月25日: XMLBeans は Apache Incubator プロジェクトからトップレベルプロジェクトの1つに昇格。
  - 2005年6月30日: XMLBeans Version 2.0 リリース
  - 2005年11月16日: XMLBeans Version 2.1 リリース
  - 2006年6月23日: XMLBeans Version 2.2 リリース
  - 2007年6月1日: XMLBeans Version 2.3 リリース
  - 2008年7月8日: XMLBeans Version 2.4 リリース
  - 2009年12月14日: XMLBeans Version 2.5 リリース
  - 2012年8月14日: XMLBeans Version 2.6 リリース
  - 2013年6月: 開発を終了
  - 2018年6月: 開発を再開
  - 2018年6月29日: XMLBeans Version 3.0 リリース

## 関連項目

  - [Java Architecture for XML Binding](../Page/Java_Architecture_for_XML_Binding.md "wikilink") (JAXB)

## 脚注

## 外部リンク

  - [プロジェクト公式サイト](http://xmlbeans.apache.org/)
  - [XMLBeans resources](http://xmlbeans.apache.org/resources/index.html)
  - [The Apache XML project](http://xml.apache.org/)
  - [XMLBean Ant task](http://xmlbeans.apache.org/docs/2.0.0/guide/antXmlbean.html)
  - [XML Binding Resources - xbeans of popular schemas](http://xmlbeans.googlepages.com/)

[Category:Java開発ツール](https://ja.wikipedia.org/wiki/Category:Java開発ツール "wikilink") [Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink")

1.  [Apache XMLBeans - The Apache Attic](http://attic.apache.org/projects/xmlbeans.html)