> この記事は[EbXML Core Components](https://ja.wikipedia.org/wiki/EbXML_Core_Components)から翻訳されています。


**ebXML Core Components**（**CC**, コアコンポーネント、コア構成要素）は、企業間[電子商取引](../Page/電子商取引.md "wikilink")でやりとりする電子伝票を構成する要素のモデルである。[ebXML](https://ja.wikipedia.org/wiki/ebXML "wikilink")の標準のひとつであり、[UN/CEFACT](https://ja.wikipedia.org/wiki/UN/CEFACT "wikilink")において標準化が行われている。

企業間電子商取引においては、業界ごと、あるいは業務ごとに異なる伝票（例えば「注文」「請求」等）が用いられる。だがそうした伝票を構成する要素には、業務や業界をまたがって共通に使われるものがある。例えば、「住所」という項目は様々な伝票の中に現れる。そうした共通の要素を括り出して、新たな伝票の設計の際に再利用できるようにすることがコア構成要素の基本的な発想である。

コア構成要素は抽象的なモデルであり、[XMLや](../Page/Extensible_Markup_Language.md "wikilink")[EDIFACT](https://ja.wikipedia.org/wiki/EDIFACT "wikilink")といった具体的な構文からは独立である。コア構成要素で設計したモデルを実際にコンピュータで処理可能な形式にするには、何らかの規則で変換する必要がある。XMLの場合には、XML設計規則 (Naming and Design Rules) によって、コア構成要素に基づいた[XML Schemaを設計する](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")。XML設計規則は、UN/CEFACT ATGによるものと[OASISの](https://ja.wikipedia.org/wiki/OASIS_\(組織\) "wikilink")[UBL](https://ja.wikipedia.org/wiki/UBL "wikilink")技術委員会によるものとが公開されている。

コア構成要素の[メタモデル](../Page/メタモデル.md "wikilink")、つまりコア構成要素という概念自体の定義は、**Core Components Technical Specification**（**CCTS**, コア構成要素技術仕様）に記述されている。CCTSはUN/CEFACT TMGが開発しており、[ISOによってISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")/TS 15000-5として承認されている。

CCTSのメタモデルでは、**Core Component**（**CC**, コア構成要素）と **Business Information Entity**（**BIE**, ビジネス情報項目）というふたつの概念が中心となる。前者は特定の業務文脈に依存しない、いわば無色の概念である（例えば「住所」）。一方後者のBIEは、CCを元にして、業務上の文脈を付加した概念であり（例えば「配送先住所」）、最終的にXMLの要素として表現されるのはBIEである。

したがって、コア構成要素の方式に則って業務伝票を設計する作業では、既存のCCを元にBIEを定義することが中心となる。再利用可能なCCのライブラリはUN/CEFACT Core Components Libraryとして公開されている。これは各種業界から寄せられた情報項目を元に作成されたものである。

## UMLとの対応

CCならびにBIEはモデル要素のタイプによって細分化される。これらは[UML](../Page/統一モデリング言語.md "wikilink")[クラス図](https://ja.wikipedia.org/wiki/クラス図 "wikilink")の構成要素と概ね対応させることができる。

  - Aggregate Core Component (ACC)、Aggregate Business Information Entity (ABIE) - クラスに対応
  - Basic Core Component (BCC)、Basic Business Information Entity (BBIE) - クラスの属性に対応
  - Core Component Type (CCT)、Data Type (DT) - 属性の型に対応
  - Association Core Component (ASCC)、Association Business Information Entity (ASBIE) - クラス間の関連に対応

このような対応関係のため、コア構成要素のモデルを図示するのにしばしばUMLクラス図が使われる。

## 関連項目

  - [Universal Business Language](https://ja.wikipedia.org/wiki/Universal_Business_Language "wikilink") (CCTSに基づいたモデルのXMLによる実装)

## 外部リンク

  - [Core Components Technical Specification Version 2.01](http://www.unece.org/cefact/ebxml/CCTS_V2-01_Final.pdf)
  - [UN/CEFACT TMG](http://www.untmg.org/)
  - [UN/CEFACT ATG](http://www.disa.org/cefact-groups/atg/)

[Category:電子商取引](https://ja.wikipedia.org/wiki/Category:電子商取引 "wikilink")