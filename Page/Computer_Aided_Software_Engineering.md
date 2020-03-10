> この記事は[Computer Aided Software Engineering](https://ja.wikipedia.org/wiki/Computer_Aided_Software_Engineering)から翻訳されています。


[Umbrello_1.png](https://ja.wikipedia.org/wiki/File:Umbrello_1.png "fig:Umbrello_1.png") **Computer Aided Software Engineering** (略: **CASE**)とは、[ソフトウェア開発やソフトウェアの保守に](../Page/ソフトウェア工学.md "wikilink")[ソフトウェアツール](https://ja.wikipedia.org/wiki/ソフトウェアツール "wikilink")を利用すること。そのようなツールを**CASEツール**と呼ぶ。

## 概要

ソフトウェア開発のあらゆる工程でソフトウェアツールを利用でき、また様々なツールを使用したソフトウェア開発は CASE ([アクロニム](https://ja.wikipedia.org/wiki/アクロニム "wikilink")でケースと読まれる)と呼ぶことができる。CASEツールには、プロジェクト管理ソフトウェア、ビジネス分析・機能分析ツール、システム設計ツール、コード格納ツール、[コンパイラ](../Page/コンパイラ.md "wikilink")、変換ツール、テストツールなどが含まれる。

しかし、一般に CASEツールと称されているのは分析および設計に関するツールであり、設計情報からソフトウェア製品の一部（または全部）を自動生成する機能を備えるものが多い。そのようなツールから[Jackson Structured Programmingのような開発手法や](https://ja.wikipedia.org/wiki/Jackson_Structured_Programming "wikilink")、 Edward Yourdon, Chris Gane, Trish Sarson といった研究者が提唱するソフトウェアモデリング技法が生まれた。この狭い意味では、例えばデータベース製品に適用されるCASEツールの機能として、以下のようなものが一般的である。

  - ビジネス、実世界のプロセスとデータフローのモデリング
  - [実体関連図](https://ja.wikipedia.org/wiki/実体関連モデル "wikilink")（entity-relationship diagram）の形式での[データモデル](https://ja.wikipedia.org/wiki/データモデル "wikilink")の開発
  - プロセスおよび関数仕様の開発
  - [データベース](../Page/データベース.md "wikilink")生成用[SQL](../Page/SQL.md "wikilink")と[ストアドプロシージャ](https://ja.wikipedia.org/wiki/ストアドプロシージャ "wikilink")の製造

## 歴史

CASE という用語は 1982年、[ミシガン州](../Page/ミシガン州.md "wikilink")[サウスフィールドの](https://ja.wikipedia.org/wiki/サウスフィールド_\(ミシガン州\) "wikilink") Nastec Corporation というソフトウェア企業が考案したものである。同社のグラフィックおよびテキストの統合エディター GraphiText を指す言葉として使われた。GraphiText はマイクロコンピュータ向けでは最初期の[ハイパーリンク](../Page/ハイパーリンク.md "wikilink")によるテキスト文字列の相互参照を実現していた。現在の Webページリンクの先駆けのひとつである。GraphiText の後継製品 DesignAid はソフトウェアやシステムの設計図を論理的かつ意味論的に評価し、[データ辞書](https://ja.wikipedia.org/wiki/データ辞書 "wikilink")を作成するソフトウェアである。続いて Cambridge Technologies 社が Excelerator で市場に参入。DesignAid が Convergent Technologies 社や[バロース](https://ja.wikipedia.org/wiki/バロース "wikilink")のミニコンピュータで動作したのに対して、Excelerator は [IBM PC/ATで動作した](https://ja.wikipedia.org/wiki/IBM_PC/AT "wikilink")。当時のパーソナルコンピュータはミニコンピュータに比較してネットワーク機能とデータベース機能が貧弱ではあったが、それ以上にパソコンでのCASEツールには魅力があり、Excelerator は人気となった。その後すぐにKnowledgeWare、[テキサス・インスツルメンツ](https://ja.wikipedia.org/wiki/テキサス・インスツルメンツ "wikilink")といった企業がCASE市場に参入することとなる。

初期の CASEツールは[ソフトウェア設計](https://ja.wikipedia.org/wiki/ソフトウェア設計 "wikilink")をグラフィカルに表現したり、それを分析するものが主流であった。プログラム設計に関するものとして、Excelerator・ADW がある。データ設計に関するものとして、[Bachman](../Page/チャールズ・バックマン.md "wikilink")・IEW・IEF などがある。DesignAid はプログラムとデータの両方を扱うだけでなく、プログラム生成ツール Transform を備えていた。これは、Nastec 社が Transform Logic Corporation を支配下に置いて得た製品である。1984年、Nastec 社はプロジェクト管理や製品構成管理を中心とした LifeCycle Manager を開発した。LifeCycle Manager の初期のコンセプトはシステム開発手法とプロジェクト管理システムの結合にあった。

従来型のCASEツールは1990年代初期にピークを迎えた。当時、[IBM](../Page/IBM.md "wikilink")は以下のような協力ソフトウェア企業と共に [AD/Cycle](https://ja.wikipedia.org/wiki/AD/Cycle "wikilink") を発表した。これはソフトウェアのライフサイクル全体をカバーするツールを集約したものである。

  - KnowledgeWare 社: IEW, ADW
  - [テキサス・インスツルメンツ](https://ja.wikipedia.org/wiki/テキサス・インスツルメンツ "wikilink") 社: IEF
  - Nastec 社: DesignAid, LifeCycle Manager

メインフレームの凋落に伴い、AD/Cycle などに代表されるCASEツールから今日の主流CASEツールへの市場の転換がなされた。興味深いことに1990年代初期のCASE市場を占めていた製品のほとんどは、[CAが買収した](https://ja.wikipedia.org/wiki/CA_\(企業\) "wikilink") (IEW, IEF, ADW, Cayenne, LBMS など)。

## CASE ツール

現在では、以下のような機能を持つソフトウェアが一般に CASE ツールとされている。

  - [ソースコード生成](https://ja.wikipedia.org/wiki/ソースコード生成 "wikilink")ツール
  - [UMLエディタ](../Page/統一モデリング言語.md "wikilink")、または類似製品
  - [リファクタリングツール](../Page/リファクタリング_\(プログラミング\).md "wikilink")
  - [QVT](../Page/QVT.md "wikilink") または[モデル変換](../Page/モデル変換.md "wikilink")ツール
  - [構成管理](../Page/構成管理.md "wikilink")ツール（[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")を含む）

CASE ツールはコードを出力するだけではない。様々なシステム分析や[SSADM](../Page/SSADM.md "wikilink")のような設計手法に基づく出力をも生成する。例えば、以下のようなものがある。

  - [データベーススキーマ](https://ja.wikipedia.org/wiki/スキーマ "wikilink")
  - [データフロー図](../Page/データフロー図.md "wikilink")
  - [実体関連図](https://ja.wikipedia.org/wiki/実体関連モデル "wikilink")
  - プログラム仕様
  - ユーザー向け文書

CASEツールを以下の2種類に分類することもある:

  - **上流CASEツール**: ソフトウェアの分析・設計工程に関するツール群（図作成ツール・報告書作成ツール・分析ツールなど）
  - **下流CASEツール**: データベーススキーマ生成ツール・プログラム生成ツール・実装ツール・テストツール・[構成管理](../Page/構成管理.md "wikilink")など

## 関連項目

  - [統一モデリング言語](../Page/統一モデリング言語.md "wikilink") (UML)
  - [RAD](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")
  - [4GL](https://ja.wikipedia.org/wiki/4GL "wikilink")
  - [モデル駆動型アーキテクチャ](../Page/モデル駆動型アーキテクチャ.md "wikilink")
  - [ドメインモデリング](https://ja.wikipedia.org/wiki/ドメインモデリング "wikilink")
  - [モデリング言語](../Page/モデリング言語.md "wikilink")

## 外部リンク

  - [Definition and discussion](http://www.sei.cmu.edu/legacy/case/case_whatis.html) カーネギーメロン大学ソフトウェア工学研究所
  - [CASE Tools](http://case-tools.org) CASEツールのディレクトリ（英語）
  - [CASE tool index](http://www.cs.queensu.ca/Software-Engineering/tools.html) - 非常に詳細なリスト

[Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:ソフトウェア開発工程](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発工程 "wikilink")