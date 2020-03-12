> この記事は[CODASYL](https://ja.wikipedia.org/wiki/CODASYL)から翻訳されています。


**CODASYL**（）は主として多くのコンピュータで利用できる標準[プログラミング言語](../Page/プログラミング言語.md "wikilink")の開発を推進することを目的として組織され、[COBOL](../Page/COBOL.md "wikilink")の標準規格のメンテナンスと、[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")以前のデータベースのモデリングなどといった活動を行った[データ処理](../Page/データ処理.md "wikilink")業界の団体である。日本語では「コダシル」と読む。

## 概要

は1959年に組織された。メンバーは[データ処理](../Page/データ処理.md "wikilink")に関係する業界と米国の政府機関の人間であった。その大きな目標は、データシステム分析･設計・実装の効率化の推進であった。数年にわたって各種言語について作業したが、具体的な標準化はなされず、標準化作業は[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")に引き継がれた。

1965年、 はリスト処理部会\[1\]を結成した。このグループはレコード集合の処理を言語の拡張として開発することを目的としていた。名称は[チャールズ・バックマン](../Page/チャールズ・バックマン.md "wikilink")の IDS\[2\]システム（プロジェクトの技術的な出発点）でレコード間の関係をポインタでレコード同士を連結すること（つまりリスト）で管理していたことから来ている。1967年、同グループはデータベース作業班\[3\] (DBTG) と改称し、1968年1月に同グループはレポート\[4\]を発表した。1969年10月、DBTG は[ネットワーク型データモデル](../Page/ネットワーク型データモデル.md "wikilink")の言語仕様を発表し、これが一般に  データモデルと呼ばれるようになった。この仕様はいくつかの言語を定義している。ひとつの[データ記述言語](https://ja.wikipedia.org/wiki/データ定義言語 "wikilink")(DDL)は[データベース](../Page/データベース.md "wikilink")の[論理スキーマ](https://ja.wikipedia.org/wiki/論理スキーマ "wikilink")を定義し、別のDDLがデータベースのアプリケーションビューを定義するサブスキーマを生成する。そして[データ操作言語](https://ja.wikipedia.org/wiki/データ操作言語 "wikilink")(DML)で[データベース](../Page/データベース.md "wikilink")を操作する機能を  に組み込む際の仕様を定義している。この仕様はCOBOLに照準を合わせていたが、（DDLとDMLを分離したことから）言語とは独立した[データベース](../Page/データベース.md "wikilink")という概念が生まれる元となり、[IBM](../Page/IBM.md "wikilink") はそれを利用して [PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink") を COBOL の後継として宣伝した。

1971年、[プログラミング言語](../Page/プログラミング言語.md "wikilink")からの独立性を求める声が強くなり、組織は再編され、DDL の開発はデータ記述言語委員会\[5\]が受け持ち、 の方は  言語委員会\[6\]が受け持つようになった。後世から見れば、この分割がよくない結果を生んだ。両者の仕様策定は同期されることなく独自に行われ、ベンダーはその差異に悩まされることになる。結果として、実装された製品間で非互換が発生することとなった。

いくつかのベンダーがDBTG仕様に（大まかに）準拠したデータベース製品を実装した。主なものは以下の通り:

  - (IDS/2) - [ハネウェル](../Page/ハネウェル.md "wikilink")

  - (IDMS) - Cullinet

  - DMS-1100 - [UNIVAC](../Page/UNIVAC.md "wikilink")

  - DBMS32 - [DEC](https://ja.wikipedia.org/wiki/デジタル・イクイップメント・コーポレーション "wikilink")

（当時の名称は ）は[グッドリッチ](../Page/グッドリッチ.md "wikilink")から技術を導入した。 は後に[コンピュータ・アソシエイツ](https://ja.wikipedia.org/wiki/CA_\(企業\) "wikilink")(CA)に買収されるが、CAは2006年現在も IDMS の後継製品を販売している。

の委員会の一部は現在も活動しているが、CODASYL 自体は既に存在しない。 に関する記録は[チャールズ・バベッジ研究所](https://ja.wikipedia.org/wiki/チャールズ・バベッジ研究所 "wikilink")が保管しており、同研究所のウェブサイトで見ることができる。

1980年代に[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")が注目されるようになると共に  の活動は減退していった。

## 参考文献

  - *The Codasyl Approach to Data Base Management.* T. William Olle. Wiley, 1978. ISBN 0-471-99579-7.
  - The Codasyl Model. J. S. Knowles and D. M. R. Bell, in *Databases - Role and Structure*, ed. P. M. Stocker, P. M. D. Gray, and M. P. Atkinson, CUP, 1984. ISBN 0-521-25430-2

## 脚注

<references/>

## 関連項目

  - [ナビゲーショナルデータベース](../Page/ナビゲーショナルデータベース.md "wikilink")

## 外部リンク

  - [Charles Babbage Institute](http://www.cbi.umn.edu/)

[Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink") [Category:コンピュータ史](https://ja.wikipedia.org/wiki/Category:コンピュータ史 "wikilink") [Category:COBOL](https://ja.wikipedia.org/wiki/Category:COBOL "wikilink")

1.
2.
3.
4.
5.
6.