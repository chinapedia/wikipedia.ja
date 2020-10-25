> この記事は[Meta-Object Facility](https://ja.wikipedia.org/wiki/Meta-Object_Facility)から翻訳されています。


[M0-m3.png](https://ja.wikipedia.org/wiki/File:M0-m3.png "fig:M0-m3.png") **Meta-Object Facility**（**MOF**）とは、[OMGの定めた](../Page/Object_Management_Group.md "wikilink")[モデル駆動工学](../Page/モデル駆動工学.md "wikilink")のための標準規格である。公式ページは[OMG's MetaObject Facility](http://www.omg.org/mof/)。

## 概要

MOFは[統一モデリング言語](../Page/統一モデリング言語.md "wikilink") (UML) を起源としている。OMGがUMLの標準化を行った際に、モデルの厳密な定義を行う手段として、MOFを導入した。MOFは4階層のアーキテクチャとして設計されている。理解を容易にするために、M1層より説明しよう。M1層で定義されるモデルは、通常のUMLモデルなど、普通にソフトウェアの設計等で用いられるモデルである。UMLのクラスなどがここに含まれる。その下位に当たるM0 層は、M1層のインスタンスである。M1層のUMLクラスから実行時に生成される個々のインスタンス等がこれに該当する。上位のM2層は、「UML 自身の構造の定義」が含まれる(このM2層を指して[メタモデル](../Page/メタモデル.md "wikilink")と呼ぶことが多い）。例えば、UMLのクラスには複数のフィールドやメソッドがあり、クラス間には様々な種類のリレーション（アソシエーションやアグリゲーション等）が存在している。これらは「UML自身の構造」の一部である。M2層を用いることで、このようなUMLモデルの構造の厳密な定義を行うことが可能になる。さらに、MOFの導入により、OMGはUML以外の（[CWM](https://ja.wikipedia.org/wiki/CWM "wikilink")や[SysML](https://ja.wikipedia.org/wiki/SysML "wikilink")等）のモデルを定義する手段を手に入れることにもなった。最上位のM3層は、メタ-メタモデルと呼ばれ、（UMLではなく）MOF自身の構造を定義する。

MOFとUMLは良く似ているため、MOFメタモデルは通常UMLのクラス図としてモデル化される。MOFをサポートする標準として[XMIがある](../Page/XML_Metadata_Interchange.md "wikilink")。XMIを用いて、M3/M2/M1層のモデルをXMLベースの形式で交換することが可能となる。さらにMOFでは、モデルやメタモデルを生成・操作する手段としてJava言語インタフェース[JMIを定義している](https://ja.wikipedia.org/wiki/Java_Metadata_Interface "wikilink")（MOF1.4までは、[CORBA](https://ja.wikipedia.org/wiki/CORBA "wikilink") [IDL](https://ja.wikipedia.org/wiki/IDL "wikilink") インターフェイスも定義されていたが、MOF2.0からは削除された）。

MOFは「閉じた」メタモデリング・アーキテクチャである。なぜならば、M3モデルはM3モデル自身で定義されており、M3層を定義するために外部の定義を必要としないからである。また、MOFは「厳密な」メタモデリング・アーキテクチャでもある。各層の各モデル要素は上位層のモデル定義に厳密に対応している。MOFは、言語やデータの構造の[抽象構文](https://ja.wikipedia.org/wiki/抽象構文 "wikilink")を定義する手段を提供する。メタモデル定義においてMOFが果たす役割は、プログラミング言語の構文定義において[EBNF](../Page/EBNF.md "wikilink")が果たす役割と全く同じである。MOFはメタモデル定義のための[ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink") (DSL) と捉えることができ、これはちょうどEBNFが構文定義のためのDSLであるのと同じである。EBNFと同様、MOFはMOF自身で定義できる（これがM3層の定義となる）。

MOFは[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")でなじみのあるクラスを用いて構造を定義する(ただし、ここで用いるクラス **MOF::Classes** であり、UML で用いる**UML::Classes** とは厳密には異なる）。これによりメタレベルにおける概念（モデル要素）とその構造を定義する。しかし、MOFで定義されるモデルが[UMLのようなオブジェクト指向型のメタモデルに限定されるわけではない](../Page/統一モデリング言語.md "wikilink")。オブジェクト指向型でないメタモデルも定義可能である（例えば、[関係モデル](../Page/関係モデル.md "wikilink")、[ペトリネット](../Page/ペトリネット.md "wikilink")や[Webサービス](../Page/Webサービス.md "wikilink")のメタモデルなど）。

2008年2月現在、OMG は2種類の MOF を定義している:

  - **EMOF**: Essential MOF（基本MOF）
  - **CMOF**: Complete MOF（完全MOF）

**ECore**という派生仕様が **Eclipse Modeling Framework** で定義されているが、これはほぼOMGのEMOFに相当する。

他の関連仕様として[OCLがある](../Page/Object_Constraint_Language.md "wikilink")。これは[述語論理](../Page/述語論理.md "wikilink")を使用してモデルの制限や問合せを定義する形式言語の仕様である。

また、重要な新たな標準として[QVT](../Page/QVT.md "wikilink")がある。これはOCLの拡張であり、MOFベースのモデルの変換方法を記述する手段を提供するものである。（[モデル変換言語](../Page/モデル変換言語.md "wikilink")参照）。

MOFは国際標準規格となっている:

  - [ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")/[IEC](../Page/国際電気標準会議.md "wikilink") 19502:2005 Information technology -- Meta Object Facility (MOF)

## 参考文献

  - [Ralph Sobek, MOF Specifications Documents](http://www.irit.fr/~Ralph.Sobek/neptune/mof_2_0.shtml)
  - [Jean Bezivin - On the Unification Power of Models](http://www.sciences.univ-nantes.fr/lina/atl/www/papers/OnTheUnificationPowerOfModels.pdf). Software and System Modeling (SoSym) 4(2):171--188.
  - [Johannes Ernst - What is meta-modeling?](http://www.metamodel.com/staticpages/index.php?page=20021010231056977)
  - [Johannes Ernst - What are the differences between a vocabulary, a taxonomy, a thesaurus, an ontology, and a meta-model?](http://www.metamodel.com/article.php?story=20030115211223271)
  - [Anna Gerber and Kerry Raymond. MOF to EMF and Back Again.](http://portal.acm.org/ft_gateway.cfm?id=965673&type=pdf)

## 関連項目

  - [メタモデル](../Page/メタモデル.md "wikilink")
  - [ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink")
  - [モデル駆動型アーキテクチャ](../Page/モデル駆動型アーキテクチャ.md "wikilink")
  - [モデル駆動工学](../Page/モデル駆動工学.md "wikilink")
  - [統一モデリング言語](../Page/統一モデリング言語.md "wikilink")
  - [CWM](../Page/Common_Warehouse_Metamodel.md "wikilink")
  - [XMI](../Page/XML_Metadata_Interchange.md "wikilink")
  - [QVT](../Page/QVT.md "wikilink")
  - [プラットフォーム独立モデル](https://ja.wikipedia.org/wiki/プラットフォーム独立モデル "wikilink") (PIM)
  - [プラットフォーム特化モデル](https://ja.wikipedia.org/wiki/プラットフォーム特化モデル "wikilink") (PSM)
  - [メタデータ](../Page/メタデータ.md "wikilink")

## 外部リンク

  - [Object Management Group](http://www.omg.org)
  - [OMG's MetaObject Facility](http://www.omg.org/mof/)

[Category:ソフトウェア工学](https://ja.wikipedia.org/wiki/Category:ソフトウェア工学 "wikilink") [Category:仕様記述言語](https://ja.wikipedia.org/wiki/Category:仕様記述言語 "wikilink") [Category:データモデリング](https://ja.wikipedia.org/wiki/Category:データモデリング "wikilink") [Category:統一モデリング言語](https://ja.wikipedia.org/wiki/Category:統一モデリング言語 "wikilink") [Category:ISO/IEC標準](https://ja.wikipedia.org/wiki/Category:ISO/IEC標準 "wikilink")