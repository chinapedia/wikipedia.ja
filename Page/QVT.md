> この記事は[QVT](https://ja.wikipedia.org/wiki/QVT)から翻訳されています。


**QVT**（Queries/Views/Transformations）とは、[Object Management Groupが定義した](../Page/Object_Management_Group.md "wikilink")[モデル駆動型アーキテクチャ](../Page/モデル駆動型アーキテクチャ.md "wikilink")における[モデル変換](../Page/モデル変換.md "wikilink")の標準である。[Meta-Object Facility](../Page/Meta-Object_Facility.md "wikilink")(MOF)に関連する標準であることから、**MOF QVT** とも呼ばれる。

## 解説

モデル変換とは、メタモデル MMa に準拠したモデル Ma を[メタモデル](../Page/メタモデル.md "wikilink") MMb に準拠したモデル Mb に変換するプロセスである。MMa=MMb であれば、その変換を**内発的**（endogeneous）といい、そうでなければ**外発的**（exogeneous）という。モデル変換はモデル駆動型アーキテクチャ(MDA)において重要な役割を担う。このため、OMG は [MOF](../Page/Meta-Object_Facility.md "wikilink") **Query/Views/Transformations** の RFP（Request for proposal）を発行し、MDA 関連の推奨規格（[UML](../Page/統一モデリング言語.md "wikilink")、MOF、[OCLなど](../Page/Object_Constraint_Language.md "wikilink")）に互換性のある標準を求めた。いくつかの企業や研究機関がこれに応じ、3年をかけて共同提案が策定され、標準として承認された。

現在では、QVT標準に準拠したオープンソースも含めたいくつかの製品がある。QVT はソースモデルからターゲットモデルへの変換の標準的手法を定義している。標準の中にはいくつかのアイデアが含まれている。その1つとして、ソースおよびターゲットモデルが MOF のメタモデルに準拠することを推奨している。また、変換プログラム自身も MOF のメタモデルに準拠したモデルであるとしている。これはつまり、QVT の抽象構文は MOF 2.0 のメタモデルに従うべきだということを意味する。

実際の標準は、やや複雑な構成となっている。まず、QVT 言語は OCL 2.0 標準を統合し、命令型 OCL への拡張を行っている。さらに、QVT は *QVT/Relations*、*QVT/Core*、*QVT/OperationalMapping* という3つの[ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink")を定義し、これらの言語が階層型アーキテクチャを構成している。Relations と Core は宣言型言語であり、それぞれ抽象化レベルが異なる。また、それらの間には規範的な対応関係が定義されている。Relations 言語はテキスト表現に加え、グラフィカルに定義された厳密な文法を持つ。QVT/OperationalMapping 言語は[命令型言語](https://ja.wikipedia.org/wiki/命令型言語 "wikilink")であり、QVT/Relations と QVT/Core の拡張となっている。QVT/OperationalMapping 言語の文法は一般的な命令型言語の構文によく似ている（ループ、条件など）。

また、*QVT/BlackBox* という機構で他の言語（[XSLT](../Page/XSL_Transformations.md "wikilink")、[XQuery](../Page/XQuery.md "wikilink")）で表現された変換機能を呼び出すようになっており、これも仕様の重要な部分を占める。これは特に既存の QVT 以外のライブラリを統合する際に重要となる。

今のところ、QVT ではモデルからモデルへの変換しか扱っておらず、そのモデルも MOF 2.0 のメタモデルに対応したものだけである。各種文書（[XML](../Page/Extensible_Markup_Language.md "wikilink")、[SQL](../Page/SQL.md "wikilink")など）とモデルの間の変換は、QVT の範囲にはないが、いずれ標準化される可能性はある。それらは他の[ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink")を MDA の枠内で扱えるようにするものと見ることができる。

## 実装

  - **[M2M](https://ja.wikipedia.org/wiki/M2M_\(Eclipse\) "wikilink")** - OMG QVT 標準の Eclipse による実装。M2Mは、[ATL](../Page/ATLAS_Transformation_Language.md "wikilink")、Compuware社による宣言型QVTの実装、Borlandによる命令型QVTの実装、から構成される。

命令型QVT(QVT-OperationalMapping) :

  - **[Borland Together](https://ja.wikipedia.org/wiki/Borland_Together "wikilink")** - Eclipse M2M へ提供されるコンポーネント。一部 QVTに準拠。
  - **[SmartQVT](https://ja.wikipedia.org/wiki/SmartQVT "wikilink")** - オープンソースのQVT命令型言語（France-Telecom Lannion、フランス）。

宣言型QVT(QVT-Relations) :

  - [ModelMorf](http://www.tcs-trddc.com/ModelMorf/index.htm) - [タタ・コンサルタンシー・サービシズ](../Page/タタ・コンサルタンシー・サービシズ.md "wikilink")の子会社 [TRDDC](http://www.tcs-trddc.com) による変換エンジン。独自仕様だが部分的に QVT 準拠。オープンソースではない。
  - [medini QVT](http://projects.ikv.de/qvt) - ベルリンの[ikv++](http://www.ikv.de)社による宣言型QVT(QVT-relations)の実装。入力補間機能付きのエディタとデバッガを含むEclipseのベースのRCPとなっている。非営利目的の利用は無料。

宣言型QVT(QVT-Core) :

  - [OptimalJ](https://ja.wikipedia.org/wiki/OptimalJ "wikilink"): Compuware社はOptimalJ version 3.4でQVT-Coreの初期仕様を実装している。
  - [MTF](http://www.alphaworks.ibm.com/tech/mtf) - IBM による 部分的に QVT 互換となっているモデル変換のプロトタイプ。オープンソースだが、Eclipse 上では動作しない。

QVTに似た言語 ：

  - **[Tefkat](https://ja.wikipedia.org/wiki/Tefkat "wikilink")** - QVT に似たオープンソースの言語。
  - **[ATL](../Page/ATLAS_Transformation_Language.md "wikilink")** - QVT 風の変換言語とエンジン。多数のユーザーがおり、オープンソースの変換ライブラリも豊富。

## 批判

QVT は OMG 推奨の標準規格だが、以下のような欠点を批判されている:

1.  **曖昧な要求仕様**。QVT の主要な要求仕様は[プラットフォーム独立モデル](https://ja.wikipedia.org/wiki/プラットフォーム独立モデル "wikilink")(PIM)から[プラットフォーム特化モデル](https://ja.wikipedia.org/wiki/プラットフォーム特化モデル "wikilink")(PSM)への変換である。しかし、OMG の MDAガイドにはPIMやPSMの具体的な定義がされておらず、QVT の要求仕様は非常に曖昧なままとなっている。
2.  **適用範囲の制限**。QVT は[MOF](https://ja.wikipedia.org/wiki/MOF "wikilink") モデルから MOF モデルへの変換のみである。MOF モデルの業界への浸透度の低さから、QVT をそのまま実装しても利用できる場面が制限される。実際に広く利用されるようになるには、モデルからテキストへの変換とテキストからモデルへの変換をサポートする必要がある。
3.  **時期尚早な標準化**。これまでの所、このような手法が産業界で大規模に使われた例がない。この時点で標準として膨大な推奨仕様を策定するのは無謀であるとの見方もある。策定を急いだのは、[W3C](../Page/World_Wide_Web_Consortium.md "wikilink") の XMLベースの標準である [XSLT](../Page/XSL_Transformations.md "wikilink") や [XQuery](../Page/XQuery.md "wikilink") に対抗するためと言われている。
4.  **委員会による定義**。QVT はいくつかのパートナー企業から持ち寄った部分を繋ぎ合わせたものである。このような委員会型仕様策定の弊害は QVT に限らない。

これらの批判のいくつかは、将来QVT実装が広く使われるようになれば、問題ではなくなる。そうなって初めて XSLT や XQuery と対抗できるようになるだろう。

## 関連項目

  - [モデル駆動工学](../Page/モデル駆動工学.md "wikilink") (MDE)
  - [モデル駆動型アーキテクチャ](../Page/モデル駆動型アーキテクチャ.md "wikilink") (MDA): MDE の OMG 版
  - [ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink") (DSL)
  - [Meta-Object Facility](../Page/Meta-Object_Facility.md "wikilink") (MOF): メタモデル記述用言語
  - [Object Constraint Language](../Page/Object_Constraint_Language.md "wikilink") (OCL): モデル制約（クエリ）言語
  - [モデル変換](../Page/モデル変換.md "wikilink")
  - [モデル変換言語](../Page/モデル変換言語.md "wikilink")
  - [メタモデル](../Page/メタモデル.md "wikilink")

## 参考文献

  - *The MDA Journal: Model Driven Architecture Straight From The Masters*
  - *Model Driven Architecture: Applying MDA to Enterprise Computing*, David S. Frankel, John Wiley & Sons, ISBN 0-471-31920-1

## 外部リンク

  - Object Management Group: *Model-Driven Architecture - Vision, Standards And Emerging Technologies*. Web版 [.pdf](http://www.omg.org/mda/mda_files/Model-Driven_Architecture.pdf)
  - Obect Management Group: *MDA Guide Version 1.0.1*. Web版 [.pdf](http://www.omg.org/docs/omg/03-06-01.pdf)
  - Brown, A: *An Introduction to Model Driven Architecture*. In: The Rational Edge, Feb. 2004 (IBM developerWorks eZine). Web版 [.html](http://www-128.ibm.com/developerworks/rational/library/3100.html) （3本のシリーズ記事の1つめ）
  - Bézivin, J: *From Object Composition to Model Transformation with the MDA*. In: TOOLS-USA'01. Web版 [.pdf](http://www.sciences.univ-nantes.fr/info/lrsg/Recherche/mda/TOOLS.USA.pdf)
  - Bohlen, M: *QVT and multi metamodel transformation in MDA*. Web版 [.pdf （英）](http://galaxy.andromda.org/jira/secure/attachment/10780/QVT+article+mbohlen+2006.pdf), [（独）](http://galaxy.andromda.org/jira/secure/attachment/10744/bohlen_OS_02_06_k4.pdf)
  - Wagelaar, D: *MDE Case Study: Using Model Transformations for UML and DSLs*. Web版 [.pdf](http://ssel.vub.ac.be/Members/DennisWagelaar/docs/uml1cs-pres.pdf)
  - Czarnecki, K, and Helsen, S : *Classification of Model Transformation Approaches.* In: Proceedings of the [OOPSLA](https://ja.wikipedia.org/wiki/OOPSLA "wikilink")'03 Workshop on the Generative Techniques in the Context Of Model-Driven Architecture. Anaheim (CA, USA). Web版 [.pdf](http://www.swen.uwaterloo.ca/~kczarnec/ECE750T7/czarnecki_helsen.pdf)
  - ModelBaset.net. *MDA Tools*. [Webサイト](http://www.modelbased.net/mda_tools.html)
  - ATL on Eclipsepedia [1](http://wiki.eclipse.org/index.php/ATL)
  - Gronmo, R, and Oldevik, J : *An Empirical Study of the UML Model Transformation Tool (UMT)*. In: INTEROP-ESA'05, Feb. 2005. Web版 [.pdf](http://interop-esa05.unige.ch/INTEROP/Proceedings/IndustrialPresentations/Gronmo.pdf)
  - Portal site *MDA and Model Transformation*: [site access](http://www.model-transformation.org/)

[Category:ソフトウェア工学](https://ja.wikipedia.org/wiki/Category:ソフトウェア工学 "wikilink") [Category:システム](https://ja.wikipedia.org/wiki/Category:システム "wikilink") [Category:統一モデリング言語](https://ja.wikipedia.org/wiki/Category:統一モデリング言語 "wikilink") [Category:コンピュータ言語](https://ja.wikipedia.org/wiki/Category:コンピュータ言語 "wikilink")