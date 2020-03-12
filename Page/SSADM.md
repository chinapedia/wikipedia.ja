> この記事は[SSADM](https://ja.wikipedia.org/wiki/SSADM)から翻訳されています。


**SSADM**（Structured Systems Analysis and Design Method、構造化システム分析・設計手法）とは、[情報システム](../Page/情報システム.md "wikilink")の分析と設計の手法の一種。[イギリス政府の商務庁](../Page/イギリスの政治.md "wikilink")（の下部組織のCCTA）が政府内での技術利用のために1980年から策定している。その名称（SSADM、Structured Systems Analysis and Design Method）はイギリス商務庁の[登録商標](https://ja.wikipedia.org/wiki/登録商標 "wikilink")である。

## 概要

[システム設計の方法論は](../Page/システム工学.md "wikilink")[ソフトウェア工学](../Page/ソフトウェア工学.md "wikilink")の一分野であり、情報に関する各種活動のフレームワークを提供することによってコンピュータシステムが特定の目的に使えるようにする。

SSADM は[ウォーターフォール・モデル](../Page/ウォーターフォール・モデル.md "wikilink")の一種であり、厳密な文書を各工程で作成することを特徴とする。これは[RADのような手法とは対極に位置する](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")。

SSADMは具体的な体系であり、様々な開発手法の研究成果を取り入れている。主要開発メンバーは以下の通り:

  - Peter Checkland: [システムズシンキング](https://ja.wikipedia.org/wiki/システムズシンキング "wikilink")の一種である Soft Systems Methodology の開発者
  - Larry Constantine: 構造化設計の研究者で[データフロー図](../Page/データフロー図.md "wikilink")の発明者
  - Wayne Stevens: 構造化設計の研究者\[1\]
  - Chris Gane と Trish Sarson: *Structured Systems Analysis: Tools and Techniques* の著者
  - [エドワード・ヨードン](../Page/エドワード・ヨードン.md "wikilink"): [構造化プログラミング](../Page/構造化プログラミング.md "wikilink")におけるヨードン法の開発者
  - Michael A. Jackson: [Jackson Structured Programming](https://ja.wikipedia.org/wiki/Jackson_Structured_Programming "wikilink") の開発者
  - [トム・デマルコ](https://ja.wikipedia.org/wiki/トム・デマルコ "wikilink"): 『構造化分析とシステム仕様』 （ISBN 4-8227-1004-1） の著者

## 工程

SSADMでは、分析・文書化・設計を以下のような工程で行う:

### 現状システムの分析

実現可能性工程とも呼ぶ。高い抽象レベルで現状を分析する。[データフロー図](../Page/データフロー図.md "wikilink")を使って現状のシステムがどのように動作しているのかを明らかにし、問題を明確化する。この工程には以下のような段階が存在する:

  - ビジネス活動モデルの開発。ビジネス活動のモデルを構築する。ビジネスのイベントと規則を洗い出して新たな自動化システムの仕様作成の入力とする。
  - [要求仕様](../Page/要求仕様.md "wikilink")の調査と定義。新システムで解決すべき現状の問題点を特定する。また、新システムで新たに提供されるサービスを定義する。
  - 現状の処理の調査。現状のサービスにおける情報の流れを調査し、データフローモデルで表す。この段階では現状のシステムのデータフローモデルを作成するだけで、ここに何らかの改善を加えたりはしない。
  - 現状のデータの調査。現状どのようにデータが収集され保存されているかを調査し、システムデータの構造を特定し記述する。この段階のデータに関するモデルも現状のシステムに関するものである。
  - 現状のサービスの論理的観点の抽出。現状のシステムの問題点を洗い出すため、その論理的観点を構築する。

### 概要ビジネス仕様

要求仕様分析工程とも呼ぶ。この工程は2段階に分けられる。第一段階は現状の環境の調査である。ここではシステム要求仕様を特定し、現状のビジネス環境をモデル化する。モデリングには、データフロー図やLDS（Logical Data Structure）が使われる。第二段階では、6種類の BSO（Bussiness Systems Option）を定義し、そのうちの1つを選んで使用する。以下のような活動がこの工程に含まれる:

  - BSOの定義: 要求仕様を満足し、ユーザーが選択可能なソリューションの選択肢を定義する。
  - BSOの選択: BSOをユーザーに対してプレゼンテーションし、いずれかを選択してもらう。この選択によって後の工程で開発されるシステムの概略が定義される。

### 詳細ビジネス仕様

要求仕様記述工程とも呼ぶ。経営側が正しく判断できるようにいくつかのビジネス選択肢を用意する。各選択肢には特定の開発/実装によって実現される機能と範囲を記述する。それらには[ワークプレイスモデル](https://ja.wikipedia.org/wiki/ワークプレイスモデル "wikilink")、[論理データモデル](https://ja.wikipedia.org/wiki/論理データモデル "wikilink")、[データフロー図](../Page/データフロー図.md "wikilink")などの技術文書が添えられる。財政面やリスク査定、実装の概要なども必要とされる。この工程には以下の活動が含まれる:

  - 要求されるシステム処理の定義。選択されたBSOに従って要求仕様を改訂し、データフローで要求されるシステムを記述し、新システム内でのユーザーの役割を定義する。
  - 要求されるデータモデルの開発。このステップは上記と並行して行われる。現状の論理データモデルを選択されたBSOに従って拡張する。
  - システム機能の抽出。上記2つと並行して、イベントを抽出し、機能の更新と新たな機能の定義を行う。また、各機能のサービスレベルを定義する。
  - ユーザージョブ仕様の開発。[ワークプレイスモデル](https://ja.wikipedia.org/wiki/ワークプレイスモデル "wikilink")を構築し、ユーザーの役割を理解するための文書を作成する。
  - 要求されるデータモデルの詳細化。[関係モデル](../Page/関係モデル.md "wikilink")に従って論理データモデルの品質を改善する（正規化とも呼ばれる）。
  - 仕様記述プロトタイプの開発。ユーザーへのデモンストレーションのためのアニメーション的なものをシステムの特定の機能について作成する。ユーザーにシステムの要求仕様を正しく理解してもらうのが目的であり、ユーザーインターフェイスに関する追加の要求をその時点で受け付ける。
  - 処理仕様の開発。システムの処理についての仕様を詳細化する。
  - システムの目的の確認。ユーザーの要求がこれまでの工程に正しく反映されているかを確認する工程であり、これの完了をもって次の工程へと進む。

### 論理データ設計

論理システム仕様工程とも呼ぶ。技術的に実現可能な選択を行う。開発/実装環境がこれまでの選択に基づいて決定される。以下のような作業が含まれる:

  - TSO（Technical Specification Option）の定義。定義された機能の物理実装において実現可能な手法を特定する。技術環境の観点でこれまでの要求仕様の様々な面を検証する。
  - TSOの選択。TSO をユーザーにプレゼンテーションし、選択してもらう。

### 論理プロセス設計

論理システム仕様工程とも呼ぶ。論理設計とプロセスを更新する。ダイアログもここで決定される。以下のような作業が含まれる:

  - ユーザーダイアログの定義。対話型インターフェイスで必要となるダイアログを定義し、ナビゲーションが必要であればそれも決定する。
  - 更新処理の定義。各イベントで必要となるデータベース更新の仕様を完成させ、それぞれのエラー処理も決定する。
  - 問合せ処理の定義。データベースへの問合せ処理の仕様を完成させ、それぞれのエラー処理も決定する。

### 物理設計

物理的なデータとプロセスの設計工程である。これまでに選択された言語やプラットフォームに応じて設計する。以下の作業が含まれる:

  - 物理設計の準備
      - 実装環境の規則を学ぶ。
      - 詳細な要求仕様のレビュー
      - 設計手法の計画立案
  - 機能仕様を完成させる。
  - データとプロセスの設計を順次行う。

## 技法

SSADMで使われている重要な技法として以下の3つがある:

  - 論理[データモデリング](https://ja.wikipedia.org/wiki/データモデリング "wikilink")。設計対象システムのデータ要求仕様を特定し、モデル化し、文書化する工程。データは実体（情報を記録しなければならない事物）と関連（実体間の関係）に分けられる。
  - データフローモデリング。情報システムでどのようにデータが移動するかを特定し、モデル化し、文書化する工程。プロセス（データを変換する活動）、データ格納域、外部実体（システムとデータをやり取りする外部の実態）、データフロー（データが流れる経路）を扱う。
  - 実体行動モデリング。各実体に影響を与えるイベントやそのイベントの発生順序などを特定し、モデル化し、文書化する工程。

## 歴史

  - **1980年** - Central Computer and Telecommunications Agency (CCTA) により、各種分析・設計手法が評価された。
  - **1981年** - 最終的に5つの候補から LBMS 法が選ばれた。
  - **1983年** - SSADM を今後すべての情報システム開発に適用することが決定された。
  - **1984年** - SSADM Version 2 をリリース。
  - **1986年** - SSADM Version 3 をリリース。NCC対応。
  - **1988年** - SSADM Certificate of Proficiency を開始。SSADM をオープンな標準としてプロモート。
  - **1989年** - Euromethod への歩み寄り。CASE製品認証スキーマ開始。
  - **1990年** - SSADM Version 4 リリース。
  - **1993年** - SSADM V4 Standard and Tools Conformance Scheme リリース。
  - **1995年** - SSADM V4+ 発表、V4.2 リリース

## 脚注

<references/>

## 参考文献

  - [トム・デマルコ](https://ja.wikipedia.org/wiki/トム・デマルコ "wikilink")、『構造化分析とシステム仕様』、日経BP出版センター、1994年 ISBN 4-8227-1004-1
  - DeMarco, Tom. *Structured Analysis and System Specification.* ISBN 0-13-854380-1.

## 外部リンク

  - [*What is SSADM?* at *webopedia.com*](http://www.webopedia.com/TERM/S/SSADM.html)
  - [*SSADM Version 4.2 Structural Standards* at the *Office of the Government Chief Information Officer (OGCIO) of the Government of the Hong Kong Special Administrative Region*](http://www.ogcio.gov.hk/eng/prodev/es3.htm)
  - [SSADM Diagram Examples](http://www.smartdraw.com/examples/view/index.aspx?catID=.Examples.SmartDraw.Software_Design.SSADM_Diagrams)
  - [*Introduction to Methodologies and SSADM*](http://www.comp.glam.ac.uk/pages/staff/tdhutchings/chapter4.html)
  - [Structured Analysis Wiki](http://www.yourdon.com/strucanalysis/wiki/index.php?title=Introduction)

[Category:ソフトウェア工学](https://ja.wikipedia.org/wiki/Category:ソフトウェア工学 "wikilink") [Category:ダイアグラム](https://ja.wikipedia.org/wiki/Category:ダイアグラム "wikilink")

1.  W. Stevens, G. Myers, L. Constantine, "Structured Design", IBM Systems Journal, 13 (2), 115-139, 1974.