> この記事は[XML Metadata Interchange](https://ja.wikipedia.org/wiki/XML_Metadata_Interchange)から翻訳されています。


**XML Metadata Interchange**（**XMI**）とは、[Extensible Markup Language (XML)を使って](../Page/Extensible_Markup_Language.md "wikilink")[メタデータ](https://ja.wikipedia.org/wiki/メタデータ "wikilink")情報を交換する標準規格であり、[OMGが策定した](https://ja.wikipedia.org/wiki/Object_Management_Group "wikilink")。[Meta-Object Facility (MOF)で表現できるメタモデルに従うメタデータを扱うことができる](../Page/Meta-Object_Facility.md "wikilink")。XMIの典型的な利用法として、[UMLモデルの交換形式としての利用があるが](../Page/統一モデリング言語.md "wikilink")、他の言語のモデル（メタモデル）のシリアライズにも使うことができる。

## 概要

OMG のモデリングについての考え方では、データは抽象モデルと具体的モデルに分割される。抽象モデルは意味的情報を表現し、具体的モデルは視覚的な図を表現する。抽象モデルは MOF に基づいた UML や [SysML](../Page/Systems_Modeling_Language.md "wikilink") のようなモデリング言語のインスタンスである。図に関しては Diagram Interchange（DI、XMI\[DI\]）という標準規格を用いる。現在のところモデリングツールの各ベンダー間での XMI 実装にはいくつかの非互換があり、抽象モデルのデータの交換にすら非互換がある。Diagram Interchange を使った例は今のところほとんど存在しない。つまり、UMLツール間で XMI によるファイル交換は実現していない。

XML Metadata Interchange (XMI) の目的の1つとして、分散異機種混在環境での UMLベースのモデリングツールと MOFベースのメタデータ・リポジトリの間でのメタデータ交換がある。[モデル駆動工学](../Page/モデル駆動工学.md "wikilink")では XMI がモデリングツールとソフトウェア生成ツールの間のモデル交換媒体として一般に使われている。

XMI には以下の4つの業界標準が組み込まれている:

  - [XML](../Page/Extensible_Markup_Language.md "wikilink") - eXtensible Markup Language、[W3C標準](../Page/World_Wide_Web_Consortium.md "wikilink")。
  - [UML](../Page/統一モデリング言語.md "wikilink") - Unified Modeling Language、[OMGのモデリング標準](https://ja.wikipedia.org/wiki/Object_Management_Group "wikilink")。
  - [MOF](../Page/Meta-Object_Facility.md "wikilink") - Meta Object Facility、[OMGの](https://ja.wikipedia.org/wiki/Object_Management_Group "wikilink")[メタモデル](../Page/メタモデル.md "wikilink")記述用言語。
  - MOF Mapping to XMI

これら4つの標準が XMI に統合されることにより、分散システムのツール開発者がオブジェクトモデルや他のメタデータを共有できるようにすることを意図している。

XMI にはいくつかのバージョン（1.0, 1.1, 1.2, 2.0, 2.1）がある。2.x は 1.x から大幅に変更されている。

[メタデータ](https://ja.wikipedia.org/wiki/メタデータ "wikilink")を表現するための XML 標準は他にもある。最も新しいものとしては [Web Ontology Language (OWL)](https://ja.wikipedia.org/wiki/OWL "wikilink") がある。OWL は[Resource Description Framework (RDF)に基づいている](../Page/Resource_Description_Framework.md "wikilink")。

XMI は国際標準として採用された。

  -
    [ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")/[IEC](https://ja.wikipedia.org/wiki/国際電気標準会議 "wikilink") 19503:2005 Information technology -- XML Metadata Interchange (XMI)

## 関連項目

  - [OWL](https://ja.wikipedia.org/wiki/OWL "wikilink")（Web Ontology Language）
  - [ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink") (DSL)
  - [ドメイン固有モデリング](../Page/ドメイン固有モデリング.md "wikilink") (DSM)
  - [モデルベーステスト](../Page/モデルベーステスト.md "wikilink") (MBT)
  - [メタモデル](../Page/メタモデル.md "wikilink")
  - [モデル変換言語](../Page/モデル変換言語.md "wikilink")
  - [MOF](../Page/Meta-Object_Facility.md "wikilink")
  - [QVT](https://ja.wikipedia.org/wiki/QVT "wikilink")
  - [OCL](https://ja.wikipedia.org/wiki/Object_Constraint_Language "wikilink")
  - [VIATRA](https://ja.wikipedia.org/wiki/VIATRA "wikilink")
  - [ATL](https://ja.wikipedia.org/wiki/ATLAS_Transformation_Language "wikilink")
  - [Common Warehouse Metamodel](https://ja.wikipedia.org/wiki/Common_Warehouse_Metamodel "wikilink")(CWM)
  - [Eclipse Modeling Framework](https://ja.wikipedia.org/wiki/Eclipse_Modeling_Framework "wikilink") (EMF)

## 外部リンク

  - [OMG XMI Specification](http://www.omg.org/technology/documents/formal/xmi.htm)

[Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:統一モデリング言語](https://ja.wikipedia.org/wiki/Category:統一モデリング言語 "wikilink") [Category:ISO/IEC標準](https://ja.wikipedia.org/wiki/Category:ISO/IEC標準 "wikilink") [Category:システムモデリング言語](https://ja.wikipedia.org/wiki/Category:システムモデリング言語 "wikilink") [Category:メタデータ](https://ja.wikipedia.org/wiki/Category:メタデータ "wikilink")