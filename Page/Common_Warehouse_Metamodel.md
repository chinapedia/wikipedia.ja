> この記事は[Common Warehouse Metamodel](https://ja.wikipedia.org/wiki/Common_Warehouse_Metamodel)から翻訳されています。


**Common Warehouse Metamodel** (**CWM**) とは、[データウェアハウス](../Page/データウェアハウス.md "wikilink")における各種オブジェクト（[リレーショナル](../Page/関係モデル.md "wikilink")、非リレーショナル、多次元など）の[メタデータ](../Page/メタデータ.md "wikilink")のモデリングのための仕様である。[Object Management Group](../Page/Object_Management_Group.md "wikilink") (OMG) がリリースしており、"CWM" という用語の商標権も含めて OMG が権利を保有する[1](http://www.omg.org/legal/tm_list.htm)。

現在よく使われているバージョンは CWM v1.1 であり、補助的な仕様として CWM Metadata Interchange Patterns (MIP) でツール間の連携についてより詳細に規定している。

## 目的

CWM はウェアハウスツールやウェアハウスプラットフォーム、分散異機種混在環境でのウェアハウス・メタデータリポジトリなどの間でウェアハウスやビジネスインテリジェンスのメタデータを交換するためのインタフェースを規定する。CWM は以下の3つの標準に基づいている。

  - [UML](../Page/統一モデリング言語.md "wikilink") - 統一モデリング言語。OMG のモデリング標準
  - [MOF](../Page/Meta-Object_Facility.md "wikilink") - Meta-Object Facility。OMG の[モデル駆動工学](../Page/モデル駆動工学.md "wikilink")の標準
  - [XMI](../Page/XML_Metadata_Interchange.md "wikilink") - XML Metadata Interchange。OMG のメタデータ交換標準

CWM ではデータの由来をトレースすることができる。すなわち、データの生成された日時、手段、場所などを記述するためのオブジェクトが提供される。メタモデルのインスタンスは XMI 文書として交換される。

当初、CWM はローカルなデータ変換機能を規定していた。[QVT](../Page/QVT.md "wikilink") Final Adopted Specification [2](http://www.omg.org/docs/ptc/05-11-01.pdf) が CWM にどう影響するかは明らかでない。

## CWMツールの相互運用性

CWM準拠のツール間で連携がうまくできるかどうかは CWM の規定範囲外のことであるが、OMG はそういった問題に対応すべく、補助的な仕様として CWM Metadata Interchange Patterns [3](http://www.omg.org/mda/specs.htm#CWM) をリリースしている。

## 主なベンダー

  - **IKAN** : [CWD4ALL](http://www.cwd4all.com/)
  - **[SAS](../Page/SAS_Institute.md "wikilink")** : CWM 採用に積極的 [](http://www.sas.com/technologies/bi/appdev/base/metadatasrv_factsheet.pdf)
  - **[オラクル](../Page/オラクル_\(企業\).md "wikilink")** : Oracle Warehouse Builder
  - **[IBM](../Page/IBM.md "wikilink")**
  - **[Cognos](https://ja.wikipedia.org/wiki/Cognos "wikilink")** : CWM v1.0 までしかサポートしていないとも言われている。
  - **[Pentaho](https://ja.wikipedia.org/wiki/Pentaho "wikilink")** : XMIv1.1準拠のフリーソフトMetadataEditorを提供

## 関連項目

  - [ATL](../Page/ATLAS_Transformation_Language.md "wikilink")
  - [Meta-Object Facility](../Page/Meta-Object_Facility.md "wikilink") (MOF)
  - [OCL](../Page/Object_Constraint_Language.md "wikilink")
  - [QVT](../Page/QVT.md "wikilink")
  - [UML](../Page/統一モデリング言語.md "wikilink")
  - [VIATRA](https://ja.wikipedia.org/wiki/VIATRA "wikilink")
  - [XML Metadata Interchange](../Page/XML_Metadata_Interchange.md "wikilink") (XMI)
  - [XML](../Page/Extensible_Markup_Language.md "wikilink")
  - [データウェアハウス](../Page/データウェアハウス.md "wikilink")
  - [ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink") (DSL)
  - [ドメイン固有モデリング](../Page/ドメイン固有モデリング.md "wikilink") (DSM)
  - [メタデータ](../Page/メタデータ.md "wikilink")
  - [メタモデル](../Page/メタモデル.md "wikilink")
  - [モデルベーステスト](../Page/モデルベーステスト.md "wikilink") (MBT)
  - [モデル変換言語](../Page/モデル変換言語.md "wikilink")

## 参考文献

  - The Common Warehouse Metamodel: An Introduction to the standard for Data Warehouse Integration by John Poole, Dan Chang, Doublas Tolbert, and David Mellor, OMG Press, 2002 ISBN 0-471-20052-2

## 外部リンク

  - [CWM Forum website](http://www.cwmforum.org/)
  - [OMG CWM Technology](http://www.omg.org/technology/cwm/)
  - [OMG CWM Specification](http://www.omg.org/technology/cwm/)
  - [OMG技術 CWM](http://www.otij.org/omginfo/technology/primer/cwm.html) オブジェクトテクノロジー研究所

[Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink") [Category:データウェアハウス](https://ja.wikipedia.org/wiki/Category:データウェアハウス "wikilink")