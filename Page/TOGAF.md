> この記事は[TOGAF](https://ja.wikipedia.org/wiki/TOGAF)から翻訳されています。


**TOGAF**（）は、[エンタープライズアーキテクチャ](../Page/エンタープライズアーキテクチャ.md "wikilink")の[フレームワーク](https://ja.wikipedia.org/wiki/フレームワーク "wikilink")の1つであり、[情報アーキテクチャ](../Page/情報アーキテクチャ.md "wikilink")の設計・計画・実装・管理の包括的アプローチを提供する。アーキテクチャは、ビジネス、アプリケーション、データ、テクノロジーの4段階あるいは4領域にモデル化されている。基盤アーキテクチャにより、アーキテクチャ実装チームは現状と将来の状態を描くことが可能となる。

## アーキテクチャとアーキテクチャ・フレームワークの定義

[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")/[IEEE](../Page/IEEE.md "wikilink") Std [1471-2000](../Page/IEEE_1471.md "wikilink") によれば、（ソフトウェア中心のシステムの）アーキテクチャとは「システムの基盤であり、コンポーネント群、コンポーネント間の相互関係と環境との関係、設計と改良を管理する原則により構成される」ものである。

しかし、TOGAF ではアーキテクチャを「システムの形式記述、あるいはシステムのコンポーネントレベルの実装を補助する詳細な計画」または「コンポーネント群の構造、それらの関係、設計と改良を常に管理制御する原則とガイドライン」であるとされている。

アーキテクチャ・フレームワークは、広範囲の各種アーキテクチャを開発するのに使えるツール群を意味する。アーキテクチャ・フレームワークは以下のような特徴を備える。

  - 情報システムを構成要素群で定義するための方法論を記述する。
  - 構成要素がどう組合わせられるかを示す。
  - ツール群を含む。
  - 共通語彙を提供する。
  - 推奨標準のリストを含む。
  - 構成要素の実装に使用可能な製品のリストを含む。

TOGAF はこのような特徴を持つアーキテクチャ・フレームワークである。

## エンタープライズアーキテクチャの領域

TOGAF のサポートするアーキテクチャ領域は以下の4つである。

1.  エンタープライズ・ビジネス・アーキテクチャ: ビジネス戦略、管理、組織、主要な[ビジネスプロセス](../Page/ビジネスプロセス.md "wikilink")を定義する。
2.  アプリケーション・アーキテクチャ: 展開すべき個々のアプリケーションシステムの青写真を提供し、アプリケーションシステム間の連携、その組織の主要なビジネスプロセスとアプリケーションシステムとの関係を定義する。
3.  データ・アーキテクチャ: 組織の論理的および物理的データ資産の構造を記述し、それに関連するデータ管理リソースを記述する。
4.  テクノロジー・アーキテクチャ: 中心となるミッションクリティカルなアプリケーションの配備をサポートするためのソフトウェア基盤を記述する。

## アーキテクチャ構築手法

アーキテクチャ構築手法（Architecture Development Method、ADM）は、その組織のビジネスや情報技術の必要性に応じたエンタープライズアーキテクチャを開発するのに適用される。その組織の必要性に応じて調整され、その後アーキテクチャ計画立案活動を管理する際に使用される。

アーキテクチャ開発の流れの概念図は[Architecture Development Cycle](http://www.opengroup.org/architecture/togaf8-doc/arch/Figures/adm.gif)にある。

このプロセスは反復的で周期的である。各段階で要求仕様が検証される。フェーズCはデータ・アーキテクチャとアプリケーション・アーキテクチャの一種の結合に関連する。

BとCの間で、追加の明確化を挿入することができ、それにより完全な[情報アーキテクチャ](../Page/情報アーキテクチャ.md "wikilink")を提供する。

[パフォーマンスエンジニアリング](https://ja.wikipedia.org/wiki/パフォーマンスエンジニアリング "wikilink")の手法が要求分析フェーズ、ビジネス・アーキテクチャのフェーズ、情報システムアーキテクチャのフェーズ、テクノロジー・アーキテクチャのフェーズのそれぞれに適用される。情報システムアーキテクチャのフェーズでは、データ・アーキテクチャとアプリケーション・アーキテクチャの両方に適用される。

## 企業連続体

企業連続体（Enterprise Continuum）とは、ある組織で利用可能な全アーキテクチャ資産の「仮想リポジトリ（virtual repository）」である。それには、アーキテクチャ的モデル、アーキテクチャ的パターン、アーキテクチャ記述などの生産物が含まれる。それらはその組織内に存在する場合もあるし、広くIT業界全体に存在する場合もある。企業連続体とは、企業の様々なレベルでのアーキテクチャ群などを一貫性を持って扱うということを示している。

企業連続体は、アーキテクチャ連続体とソリューション連続体から構成される。アーキテクチャ連続体は再利用可能なアーキテクチャ資産を意味し、その企業が利用可能な情報システム（群）の規則・表現・関連などを含む。ソリューション連続体は再利用可能なソリューション構成要素を定義することにより、アーキテクチャ連続体の実装を説明するものである。

## The Open Group

TOGAF は [The Open Group](../Page/The_Open_Group.md "wikilink") の [Architecture Forum](http://www.opengroup.org/architecture/) が開発し、1990年代半ばごろから改良し続けてきたものである。最新版 8.1.1 は [TOGAF 8.1 Enterprise Edition](http://www.opengroup.org/bookstore/catalog/g063.htm) にある。同フォーラムは TOGAF 9 に取り組んでいる。TOGAF 9 に向けてのテーマは次の通りである。

  - 企業、文化、権利保有者
  - アーキテクチャ創造
  - アーキテクチャに基づく転換
  - アーキテクチャの具体化
  - アーキテクチャ管理と制御

[The Open Group](../Page/The_Open_Group.md "wikilink") は TOGAF の非商用目的での組織内での利用については無料で TOGAF を提供している。

## 出版物

  - [TOGAF 8.1.1 Enterprise Edition in a book format](http://www.opengroup.org/bookstore/catalog/g063.htm)
  - [Guide to Security Architecture in TOGAF ADM](http://www.opengroup.org/bookstore/catalog/w055.htm) （セキュリティに関する補足）
  - [TOGAF/MDA Mapping](http://www.opengroup.org/bookstore/catalog/w054.htm)（[OMGの](../Page/Object_Management_Group.md "wikilink")[モデル駆動型アーキテクチャ](../Page/モデル駆動型アーキテクチャ.md "wikilink")(MDA)とのマッピング）

## 関連項目

  - [エンタープライズアーキテクチャ](../Page/エンタープライズアーキテクチャ.md "wikilink")

## 外部リンク

  - [TOGAF 8.1.1 Online](http://www.opengroup.org/architecture/togaf8-doc/arch/)
  - [TOGAF FAQs](http://www.opengroup.org/architecture/togaf8-doc/arch/p1/togaf_faq.htm)
  - [TOGAF Certification program](http://www.opengroup.org/certification/togaf-home.html)
  - [Tools for architecture development](http://www.opengroup.org/architecture/tools-arch-dev.htm)
  - [EAとTOGAF](http://www.mizuho-ir.co.jp/publication/column/2005/ea050607.html) みずほ情報総研コラム

[Category:情報学](https://ja.wikipedia.org/wiki/Category:情報学 "wikilink") [Category:科学的方法](https://ja.wikipedia.org/wiki/Category:科学的方法 "wikilink")