> この記事は[YAWL](https://ja.wikipedia.org/wiki/YAWL)から翻訳されています。


**YAWL**（**Yet Another Workflow Language**）は、[ワークフローパターン](https://ja.wikipedia.org/wiki/ワークフローパターン "wikilink")に基づいた[ワークフロー](../Page/ワークフロー.md "wikilink")言語の一種。実行エンジンやグラフィックエディタなどのソフトウェアシステムでサポートされている。この言語とそのサポートシステムを最初に開発したのは、[アイントホーヘン工科大学](https://ja.wikipedia.org/wiki/アイントホーヘン工科大学 "wikilink")と[クイーンズランド科学技術大学](https://ja.wikipedia.org/wiki/クイーンズランド科学技術大学 "wikilink")の研究者らであった。その後、[インターコンチネンタルホテルズグループ](../Page/インターコンチネンタルホテルズグループ.md "wikilink")、[first:telecom](http://www.firsttelecom.com/)、[ATOS Worldline](http://www.atosworldline.com) といった企業が参加するようになり、YAWL は[オープンソース](../Page/オープンソース.md "wikilink")ソフトウェアとして [LGPL](../Page/GNU_Lesser_General_Public_License.md "wikilink") ライセンスで提供されるようになった。

## 概要

YAWL 開発の動機は、ほとんど全てのワークフローパターンをサポートし、形式的意味を与えるワークフロー言語を定義することであった。[ペトリネット](../Page/ペトリネット.md "wikilink")がほとんどのワークフローパターンをほぼ描けると思われたため、YAWL の設計者らはペトリネットを出発点とし、これに形式的な拡張として、OR-合流（or-join）、取り消し集合（cancellation sets）、複数インスタンス活動（multi-instance activities）という三つの構成要素を加えた。これらの拡張によって、ペトリネットでは直接描けなかった5種類のワークフローパターン（*synchronizing merge*, *discriminator*, *N-out-of-M join*, *multiple instance with no a priori runtime knowledge*, *cancel case*）が描けるようになった。

さらに YAWL ではペトリネットの構文的要素も拡張して他のワークフローパターンも直観的に描けるようにした。*simple choice* (xor-split)、*simple merge* (xor-join)、*multiple choice* (or-split) である。言語の設計において、ペトリネットへの拡張の一部は難解であったり、通常のペトリネットに戻せないものであることが判明した。結果として、YAWL の形式意味論は単なるペトリネットではなく、一種のラベル付き[状態遷移系](../Page/状態遷移系.md "wikilink")の定義となっている。YAWL が形式意味論に基づいているという事実により、YAWL プロセスの解析技法を実装可能となった。特に YAWL システムには静的解析ツール WofYAWL がある。

## YAWL と BPEL

YAWL は [BPEL](../Page/BPEL.md "wikilink") の代替とされることもある。BPEL の最大の利点は、それが[IT業界の標準化委員会で策定されたものであるという点である](../Page/情報技術.md "wikilink")。そのため BPEL をサポートするツールは多数存在する一方、YAWL は1つの実装しか（今のところ）存在しない。また、BPEL のサブセットの形式的意味論によって、[ペトリネット](../Page/ペトリネット.md "wikilink")、[プロセス代数](https://ja.wikipedia.org/wiki/プロセス代数 "wikilink")、[有限オートマトン](../Page/有限オートマトン.md "wikilink")といった各種形式定義が描けることが示されている。これにより、BPEL にも YAWL システムと同様の機能を持つ静的解析ツールが開発できることが示された。

一方、標準の BPEL は人間の行う作業をサポートできないと指摘されている。BPEL エンジンにはそのようなタスクも描けるよう拡張されたものが既に存在するが、そのような拡張はまだ標準化されていない。対照的に、YAWL は[Webサービス](../Page/Webサービス.md "wikilink")標準に基づいたワークリストサービスのための統合されたインタフェースを提供する。このインタフェースによって開発者は、必要に応じて人間のタスクもサポートするワークリストサービスを構築できる。さらに、YAWL にはデフォルトで数種類の人間のタスクの割り当てと制御をサポートするワークリストサービスが含まれている。

YAWL のもう1つの利点はワークフローパターンのサポートだが、BPEL 2.0 で新たに追加される構成要素により、その差は小さくなると予想される。

## 機能

  - 幅広いワークフローパターンをサポート
  - 並行性の強力な理論であるペトリネットを拡張
  - YAWL（制御フロー）言語は、文法も意味論も形式的に定義されている。
  - 構築時にワークフロー解析をサポート
  - 永続性、自動的な世代管理、ワークフロー管理をサポート
  - ワークレット（worklet）と Ripple Down Rules (RDR) に基づいて動的ワークフローを扱える。
  - 洗練された拡張の開発を容易にするサービス指向アーキテクチャ
  - 時間的観点のサポート
  - XML技術（[XML Schema](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")、[XPath](../Page/XML_Path_Language.md "wikilink")、[XQuery](../Page/XQuery.md "wikilink")）に基づいたデータパースペクティブのサポート
  - ワークリストサービス・インタフェースによるリソースパースペクティブのサポート

## 関連項目

  - [ビジネスプロセス管理](../Page/ビジネスプロセス管理.md "wikilink")

## 外部リンク

  - [公式サイト（英語）](http://yawlfoundation.org/)
  - [Workflow Patterns](http://www.workflowpatterns.com/)
  - [SF.net homepage](http://www.sourceforge.net/projects/yawl/)
  - [BPM Center](http://www.bpmcenter.org/)

[Category:経営学](https://ja.wikipedia.org/wiki/Category:経営学 "wikilink") [Category:プロジェクトマネジメントソフト](https://ja.wikipedia.org/wiki/Category:プロジェクトマネジメントソフト "wikilink") [Category:ペトリネット](https://ja.wikipedia.org/wiki/Category:ペトリネット "wikilink") [Category:モデリング言語](https://ja.wikipedia.org/wiki/Category:モデリング言語 "wikilink")