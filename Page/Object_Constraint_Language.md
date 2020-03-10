> この記事は[Object Constraint Language](https://ja.wikipedia.org/wiki/Object_Constraint_Language)から翻訳されています。


**Object Constraint Language**（**OCL**）は、[統一モデリング言語](../Page/統一モデリング言語.md "wikilink") (UML) モデルに適用する規則を記述するための宣言型言語である。[IBM](../Page/IBM.md "wikilink")が開発し、UML標準の一部となった。初期のOCLは、単なるUMLの形式仕様記述言語としての拡張であったが、その後 UMLだけでなく [Object Management Group](https://ja.wikipedia.org/wiki/Object_Management_Group "wikilink") (OMG) の [Meta-Object Facility](../Page/Meta-Object_Facility.md "wikilink") (MOF) の[メタモデル](../Page/メタモデル.md "wikilink")全般を扱うようになった。Object Constraint Language (OCL) は Meta-Object Facility などのモデルやメタモデルについて、図表の形式では表現できない制約やクエリを表現することができる正確なテキスト言語である。OCL は OMG の[モデル変換](../Page/モデル変換.md "wikilink")に関する推奨標準 [QVT](../Page/QVT.md "wikilink") 仕様の一部となっている。他の多くの[モデル変換言語](../Page/モデル変換言語.md "wikilink")（[ATLなど](https://ja.wikipedia.org/wiki/ATLAS_Transformation_Language "wikilink")）も OCL に基づいて構築されている。

## 概要

OCL の元となったのは、第二世代のオブジェクト指向分析・設計手法 Syntropy である。OCL 1.4 で制約言語の仕様が追加された。OCL 2.0 では、汎用のオブジェクト・クエリ言語の定義を含むよう拡張された。

OCL 言語の構文は以下の4つに分けられる:

1.  コンテキスト - 文が正しいといえる状況の制限を定義する
2.  プロパティ - コンテキストの特性を表現する（例えば、コンテキストがクラスである場合、プロパティはその属性となる）
3.  オペレーション - プロパティを操作・修正する演算（算術演算や集合的演算）
4.  キーワード - 条件などを表現する（if、then、else、and、or、not、implies など）

## OCL と UML

OCL は[UMLを補うものであり](../Page/統一モデリング言語.md "wikilink")、自然言語の曖昧さを排していると同時に複雑な数学的記法を扱わなくてもよいという特徴がある。OCL は、図に基づいたモデルのためのナビゲーション言語でもある。

## OCL と MOF

OCL は、[MOFのメタ要素と表明を関連付けることで](../Page/Meta-Object_Facility.md "wikilink") MOF のモデルをより明確化する。

## OCL と QVT

[モデル駆動工学](../Page/モデル駆動工学.md "wikilink")や[モデル駆動型アーキテクチャ](../Page/モデル駆動型アーキテクチャ.md "wikilink") (MDA) では、[モデル変換](../Page/モデル変換.md "wikilink")の記法が重要となる。OMG はモデル変換の標準である[QVT](../Page/QVT.md "wikilink")（MOF/QVT）を定義した。[GReAT](https://ja.wikipedia.org/wiki/GReAT "wikilink")、[VIATRA](https://ja.wikipedia.org/wiki/VIATRA "wikilink")、[ATLといった](https://ja.wikipedia.org/wiki/ATLAS_Transformation_Language "wikilink")[モデル変換言語](../Page/モデル変換言語.md "wikilink")があるが、これらのQVT標準への対応レベルは様々である。これらの多くは OCL に基づいて構築されている。また、OCLのサポートは[QVT](../Page/QVT.md "wikilink")準拠の主要な条件である。

## 類似技術

ナビゲーション言語として見た場合、OCLは[XPathと対比することができる](https://ja.wikipedia.org/wiki/XML_Path_Language "wikilink")。XPath が [XMLツリーに対してナビゲーションを行うのに対して](../Page/Extensible_Markup_Language.md "wikilink")、OCL は MOFベースのモデルやメタモデル（つまり [XMIツリー](../Page/XML_Metadata_Interchange.md "wikilink")）に対してナビゲーションを行う。換言すれば、OCL と UML や MOF との関係と、XPath と XML の関係が似ているのである。モデルやメタモデルに副作用のない付加情報（制約など）を与えるモデル記述言語として見た場合、OCLと同様な役割を果たす言語として [Alloy](https://ja.wikipedia.org/wiki/Alloy_Analyzer "wikilink") などがある。

## 脚注

### 出典

## 参考文献

  - ヨシュ・ヴァルメル、アーネク・クレッペ、竹村司 (訳) 、『UML/MDAのためのオブジェクト制約言語OCL 第2版』、エスアイビー・アクセス、2004年、ISBN 978-4-434-05542-3

## 関連項目

  - [Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink") [GMT Project](http://www.eclipse.org/gmt/)
  - [MOF](../Page/Meta-Object_Facility.md "wikilink")
  - [MOF Queries/Views/Transformations](../Page/QVT.md "wikilink") (QVT)
  - [XMI](../Page/XML_Metadata_Interchange.md "wikilink")
  - [インテンショナルプログラミング](https://ja.wikipedia.org/wiki/インテンショナルプログラミング "wikilink") (IP)
  - [オブジェクト指向分析設計](https://ja.wikipedia.org/wiki/オブジェクト指向分析設計 "wikilink") (OOAD)
  - [コンピュータシミュレーション](https://ja.wikipedia.org/wiki/コンピュータシミュレーション "wikilink")
  - [ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink") (DSL)
  - [ドメイン固有モデリング](../Page/ドメイン固有モデリング.md "wikilink") (DSM)
  - [メタモデル](../Page/メタモデル.md "wikilink")
  - [メタデータ](https://ja.wikipedia.org/wiki/メタデータ "wikilink")
  - [モデルベーステスト](../Page/モデルベーステスト.md "wikilink") (MBT)
  - [モデル駆動型アーキテクチャ](../Page/モデル駆動型アーキテクチャ.md "wikilink") (MDA)
  - [モデル駆動工学](../Page/モデル駆動工学.md "wikilink") (MDE)
  - [モデル変換言語](../Page/モデル変換言語.md "wikilink") (MTL)
  - [モデリング言語](../Page/モデリング言語.md "wikilink")
  - [変換言語](https://ja.wikipedia.org/wiki/変換言語 "wikilink") (TL)
  - [XML変換言語](https://ja.wikipedia.org/wiki/XML変換言語 "wikilink") (XTL)

## 外部リンク

  - [OMG OCL specification page](http://www.omg.org/technology/documents/modeling_spec_catalog.htm#OCL)
  - [OCL page of Computer Science Dept. of CSUSB](http://www.csci.csusb.edu/dick/samples/ocl.html) （OCL 2.0 文法の概要）
  - [MIT paper "Some Shortcomings of OCL"](http://www.omg.org/docs/ad/99-12-05.pdf)
  - [OCL page of Klasse Objekten](http://www.klasse.nl/ocl/) （Octopus OCL checker と Java code generator、OCL関連書籍紹介など）
  - [Dresden OCL Toolkit](http://dresden-ocl.sourceforge.net/) （OCLツールキット）
  - [HOL-OCL](http://www.brucker.ch/projects/hol-ocl/) （OCL向けの対話型定理証明環境）
  - [OCL for Java tutorial on ParlezUML](http://www.parlezuml.com/tutorials/umlforjava/java_ocl.pdf)
  - [Article on using EMF's OCL in Java code](http://www.eclipse.org/articles/Article-EMF-Codegen-with-OCL/article.html)
  - [UML link page on cetus-links.org](http://www.cetus-links.org/oo_uml.html)

[Category:統一モデリング言語](https://ja.wikipedia.org/wiki/Category:統一モデリング言語 "wikilink") [Category:問い合わせ言語](https://ja.wikipedia.org/wiki/Category:問い合わせ言語 "wikilink") [Category:形式仕様記述言語](https://ja.wikipedia.org/wiki/Category:形式仕様記述言語 "wikilink")