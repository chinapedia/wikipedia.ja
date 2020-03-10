> この記事は[Java Architecture for XML Binding](https://ja.wikipedia.org/wiki/Java_Architecture_for_XML_Binding)から翻訳されています。


**Java Architecture for XML Binding**（**JAXB**）は、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の[クラスを](../Page/クラス_\(コンピュータ\).md "wikilink") [XMLで表現可能にする仕様である](../Page/Extensible_Markup_Language.md "wikilink")。JAXB には主に2つの機能がある。すなわち、Java の[オブジェクトを](../Page/オブジェクト_\(プログラミング\).md "wikilink") XML に[シリアライズ](../Page/シリアライズ.md "wikilink")することと、逆に XML から Java オブジェクトにデシリアライズすることである。言い換えれば、JAXB はメモリ上のデータを XML 形式に変換して保存することができ、そのためにプログラム内の各クラスにXMLロード/セーブルーチンを実装する必要がない。

JAXB は仕様が複雑で頻繁に変更される場合に特に便利である。その場合、Java の定義の変更に合わせて [XML Schema](https://ja.wikipedia.org/wiki/XML_Schema "wikilink") の定義を更新することは、時間もかかるしバグを作りこみやすい作業となる。

JAXB は [Java EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink") の [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") の一種であり、[Java Web Services Development Pack](https://ja.wikipedia.org/wiki/Java_Web_Services_Development_Pack "wikilink") (JWSDP) の一部でもある。[WSIT](https://ja.wikipedia.org/wiki/Web_Services_Interoperability_Technology "wikilink") の基盤の一部にもなっている。JAXB は Java SE version 1.6 にも含まれている。

JAXB 1.0 は、[Java Community Process](https://ja.wikipedia.org/wiki/Java_Community_Process "wikilink") の JSR 31 において2003年に開発された。続いて2006年、JAXB 2.0 が JSR 222 において開発され、2017年9月にMaintenance Release 3がリリースされている\[1\]。[リファレンス実装](https://ja.wikipedia.org/wiki/リファレンス実装 "wikilink")は java.net に[CDDL](https://ja.wikipedia.org/wiki/CDDL "wikilink")ライセンスで公開されている。

## 利用

"xjc" ツールは、[XML Schemaや他のスキーマファイル形式](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")（Java 1.6 では、[RELAX NG](https://ja.wikipedia.org/wiki/RELAX_NG "wikilink")、XML [DTD](../Page/Document_Type_Definition.md "wikilink") が実験的にサポートされている）をクラス表現に変換するのに使われる。クラス群は、javax.xml.bind.annotation.\* の名前空間（例えば @XmlRootElement や @XmlElement）から[アノテーション](https://ja.wikipedia.org/wiki/アノテーション "wikilink")を使ってマークアップされる。XML リストシーケンスは、java.util.List の属性を使って表現される。マーシャルとアンマーシャルを行うコードは JAXBContext のインスタンスを通して生成される。

さらに、JAXB には "schemagen" ツールがある。これは基本的に "xjc" の逆を行うもので、アノテーション付きのクラス群のコードから XML Schema を生成する。

## データ型の既定バインディング

Java のデータ型の種類は XML Schema のものより豊富である。以下の表は JAXB において、XML のデータ型をどのように Java のデータ型にマッピングしているかを示したものである。

| XML Schema 型      | Java データ型                               |
| ----------------- | --------------------------------------- |
| xsd:string        | java.lang.String                        |
| xsd:integer       | java.math.BigInteger                    |
| xsd:int           | int                                     |
| xsd:long          | long                                    |
| xsd:short         | short                                   |
| xsd:decimal       | java.math.BigDecimal                    |
| xsd:float         | float                                   |
| xsd:double        | double                                  |
| xsd:boolean       | boolean                                 |
| xsd:byte          | byte                                    |
| xsd:QName         | javax.xml.namespace.QName               |
| xsd:dateTime      | javax.xml.datatype.XMLGregorianCalendar |
| xsd:base64Binary  | byte\[\]                                |
| xsd:hexBinary     | byte\[\]                                |
| xsd:unsignedInt   | long                                    |
| xsd:unsignedShort | int                                     |
| xsd:unsignedByte  | short                                   |
| xsd:time          | javax.xml.datatype.XMLGregorianCalendar |
| xsd:date          | javax.xml.datatype.XMLGregorianCalendar |
| xsd:g             | javax.xml.datatype.XMLGregorianCalendar |
| xsd:anySimpleType | java.lang.Object                        |
| xsd:anySimpleType | java.lang.String                        |
| xsd:duration      | javax.xml.datatype.Duration             |
| xsd:NOTATION      | javax.xml.namespace.QName               |
|                   |                                         |

## 脚注

## 関連項目

  - [XMLBeans](https://ja.wikipedia.org/wiki/XMLBeans "wikilink") – [Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Apacheソフトウェア財団 "wikilink")による JAXB と類似・関連する技術

## 参考文献

  - [Generate an XML Document from an Object Model with JAXB 2](http://www.devx.com/Java/Article/34069)

## 外部リンク

  - [JAXB home page](https://jaxb.dev.java.net/) on Project [GlassFish](https://ja.wikipedia.org/wiki/GlassFish "wikilink")
  - [従来の JAXB home page](http://java.sun.com/xml/jaxb/index.jsp)
  - [JaxMe](http://ws.apache.org/jaxme/) – [Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Apacheソフトウェア財団 "wikilink")による JAXB の[オープンソース](../Page/オープンソース.md "wikilink")実装
  - [EclipseLink MOXy](http://www.eclipse.org/eclipselink/) – [Eclipse Foundationによる](https://ja.wikipedia.org/wiki/Eclipse_Foundation "wikilink") JAXB の[オープンソース](../Page/オープンソース.md "wikilink")実装
  - [JSR 222](http://www.jcp.org/en/jsr/detail?id=222) (JAXB 2.0)
  - [JSR 31](http://www.jcp.org/en/jsr/detail?id=31) (JAXB 1.0)
  - [JAXB chapter of the Java EE 5 Tutorial](http://java.sun.com/javaee/5/docs/tutorial/doc/bnazf.html)
  - [JAXB Wizard](http://wiki.netbeans.org/wiki/view/JAXBWizard/)

[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink")

1.