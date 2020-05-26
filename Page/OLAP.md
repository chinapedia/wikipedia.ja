> この記事は[OLAP](https://ja.wikipedia.org/wiki/OLAP)から翻訳されています。


**OLAP**は**online analytical processing**の略であり、複雑で分析的な問い合わせに素早く回答を行う方法のことである。 [ビジネスインテリジェンス](../Page/ビジネスインテリジェンス.md "wikilink")と呼ばれるより大きなカテゴリに属し、ビジネスインテリジェンスとはOLAP・[ETL](https://ja.wikipedia.org/wiki/Extract/Transform/Load "wikilink")・[リレーショナルレポーティング](https://ja.wikipedia.org/wiki/リレーショナルレポーティング "wikilink")・[データマイニング](../Page/データマイニング.md "wikilink")を含む概念である。 OLAPの典型的な用途は売上報告、市場分析、経営報告、[ビジネス業績管理](../Page/ビジネス業績管理.md "wikilink")（BPM）、予算作成、計画作成、財務諸表作成などである。

OLAPの主な特徴は以下の点にある。

  - 多次元データモデルを操作すること（[関係モデル](../Page/関係モデル.md "wikilink")ではなく）
  - 複雑、分析的でその場限りの問い合わせを行えること
  - 非常に高速であること（通常は5秒以内に結果を返す）

このような理由から、Nigel PendseはOLAPのコンセプトをより正確に表す言葉としてFASMI（Fast Analysis of Shared Multidimensional Information）を提案している。

## 機能

OLAPはまず[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")のスナップショットを取り、多次元データとして再構成する。その後、問い合わせを行うことができるようになる。複雑で膨大なデータへの問い合わせの場合、OLAPは関係データベースに同様の問い合わせを行う場合に比較して予め集計してあるデータを利用することで、きわめて短時間に処理を実施する。

この操作データからなるOLAPの構造は[OLAPキューブ](https://ja.wikipedia.org/wiki/OLAPキューブ "wikilink")と呼ばれている。キューブは[スタースキーマ](https://ja.wikipedia.org/wiki/スタースキーマ "wikilink")を形成するテーブルの一群からなり、中心には[ファクトテーブル](https://ja.wikipedia.org/wiki/ファクトテーブル "wikilink")が存在する。このファクトテーブルには問い合わせの中心的な事実が格納されており、複数のディメンジョンテーブルがここにリンクしている。このディメンジョンテーブルの中にどのように関係データを[集計](https://ja.wikipedia.org/wiki/集計 "wikilink")し分析できるのかが定義されている。ここで、元データをどのような階層構造で集計するのかによってありうる集計方法の数は変わってくる。

例えば、顧客は市・地域・国によって分類されるとすると、50市・8地域・2カ国に存在するデータであれば3階層・合計60項目のデータとなる。ここでこの顧客と製品との関係を見たいとすれば、例えば製品は250品目・20カテゴリ・3ファミリ・3部門であるとすると合計276項目のデータとなる。この二つのディメンジョンだけでも16,560ものありうる集計が発生してしまう。考慮されるべきデータが増えるにつれて集計の数はすぐに何百万もの数になってしまう。

集計の計算結果と元データは統合されてOLAPキューブとなる。原理的にはOLAPキューブは可能性のある問いに対する全ての答えを保持することができる。だが、潜在的な集計の数が余りに多いために前もって決められた物のみを完全に集計し、残りは要求に応じて集計する場合もある。

## OLAPの種類

基本的な概念からさらに踏み込むとOLAPは3種類存在する。多次元 (Multidimensional) OLAP ([MOLAP](https://ja.wikipedia.org/wiki/MOLAP "wikilink"))・関係 (Relational) OLAP ([ROLAP](https://ja.wikipedia.org/wiki/ROLAP "wikilink"))・ハイブリッド(Hybrid) OLAP ([HOLAP](https://ja.wikipedia.org/wiki/HOLAP "wikilink"))である。MOLAPは伝統的なOLAPの形式であり、単にOLAPと呼ばれる場合もある。MOLAPは集計用の特殊なデータベースを使用する。この中に特定の多次元データベースエンジンがあり、元データと集計値の両方を持つ次元軸の集まりとして必要なスキーマを作成する。これに対して、ROLAPは関係データベースに直接アクセスする。元データとディメンジョンテーブルは関係テーブルとして保持され、集計値を保持するために新しいテーブルが作成される。HOLAPでは元データは関係テーブルに保持され、集計値は多次元テーブルに保持される。

どの種類もそれなりの利点があるが、種類によって利点の詳細は異なってくる。MOLAPはデータが少ない場合に有利であり集計値を計算して返すのが速いが、大量のデータを作成してしまう欠点がある。ROLAPはよりスケーラブルであり最小の容量で済むが、前処理と問い合わせのパフォーマンスが悪くなってしまう。HOLAPは両者の中間と言えるが、前処理が速くスケーラビリティもある。OLAPを実装する際に困難なのは問い合わせを作成することである。つまり元データを選択しスキーマを構築する部分であるが、そのために大抵のOLAP製品では大量の事前に準備された問い合わせのライブラリを持っている。その他の問題としては元データの問題が挙げられる。元データは完全でかつ一貫性がなければならない。

## APIと問い合わせ言語

関係データベースにはSQLという標準化された問い合わせ言語や[ODBC](../Page/Open_Database_Connectivity.md "wikilink")・[JDBC](../Page/JDBC.md "wikilink")・[OLEDB](https://ja.wikipedia.org/wiki/OLEDB "wikilink")のように広く普及したAPIが存在するが、OLAPでは統一された規格は存在しない。最初の実務的な標準であるAPIは1997年の[マイクロソフト](../Page/マイクロソフト.md "wikilink")のOLEDB for OLAPであり、[MDX](https://ja.wikipedia.org/wiki/MDX "wikilink")問い合わせ言語をもたらした。これは複数のOLAPベンダがクライアントとサーバの両方に採用している。2001年マイクロソフトと[Hyperion Solutionsは分析記述用のXMLA](https://ja.wikipedia.org/wiki/:en:Hyperion_Solutions "wikilink") (XML for Analysis) を発表しており、ほとんどのベンダに採用されている。この標準は[MDX](https://ja.wikipedia.org/wiki/MDX "wikilink")を問い合わせ言語として使用しているため、[MDX](https://ja.wikipedia.org/wiki/MDX "wikilink")はOLAPの世界ではデファクトスタンダードとなった。

## 製品

OLAP問い合わせを実行できる最初の製品は1970年に発表されたIRIのExpressである（1995年に[オラクルに買収された](../Page/オラクル_\(企業\).md "wikilink")）。しかし当時はこの用語自体が存在せず、1993年に[Ted Codd](https://ja.wikipedia.org/wiki/Ted_Codd "wikilink")（リレーショナルデータベースの父と呼ばれる）により提唱された。しかしCodd氏の研究はArborに資金援助を受けており、さらにその会社は1年前に[Essbase](https://ja.wikipedia.org/wiki/:en:Essbase "wikilink")（Arborはその後[Hyperion Solutionsと合併](https://ja.wikipedia.org/wiki/:en:Hyperion_Solutions "wikilink")、さらに[Hyperion Solutionsは](https://ja.wikipedia.org/wiki/:en:Hyperion_Solution "wikilink")、オラクルが買収）というOLAP製品をリリースしていた。そのため、Codd氏の「Twelve laws of online analytical processing」は[Essbaseを参照していたことは明らかである](https://ja.wikipedia.org/wiki/:en:Essbase "wikilink")。

## 主な製品一覧

  - Brio Enterprise ：[Brio Technology](https://ja.wikipedia.org/wiki/:en:Brio_Technology "wikilink")
  - [Cognos](https://ja.wikipedia.org/wiki/Cognos "wikilink")
  - [DataNature](http://datanature.njk.co.jp)
  - [DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink") Cube Views：[IBM](../Page/IBM.md "wikilink")
  - [Dr.Sum](https://ja.wikipedia.org/wiki/Dr.Sum "wikilink")
  - Hyperion [Essbase](https://ja.wikipedia.org/wiki/:en:Essbase "wikilink")
  - [icCube](http://www.iccube.com)
  - [JasperReports Server](https://ja.wikipedia.org/wiki/JasperReports "wikilink")
  - [Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink") Analysis Services：マイクロソフト（以前は[Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink") OLAP Servicesと呼ばれていた）
  - [MicroStrategy](https://ja.wikipedia.org/wiki/MicroStrategy "wikilink")
  - Mondrian(オープンソース）
  - [OpenOLAP](https://ja.wikipedia.org/wiki/OpenOLAP "wikilink")
  - [OpenOLAP for MySQL](https://ja.wikipedia.org/wiki/OpenOLAP_for_MySQL "wikilink")
  - [Open Text Business Intelligence](http://www.samuraiz.co.jp/product/opentext/index.html) 低価格BIツール。（以前はBI Queryと呼ばれていた）
  - Oracle OLAP Server
  - [Pentaho](https://ja.wikipedia.org/wiki/Pentaho "wikilink")
  - [Sagent](https://ja.wikipedia.org/wiki/Sagent "wikilink")
  - [SAP Business Objects](https://ja.wikipedia.org/wiki/Business_Objects "wikilink"): [SAP](../Page/SAP_\(企業\).md "wikilink")
  - [SAP Business Warehouse](https://ja.wikipedia.org/wiki/Business_Warehouse "wikilink") (SAP BW)：[SAP](../Page/SAP_\(企業\).md "wikilink")
  - [SAP HANA](https://ja.wikipedia.org/wiki/SAP_HANA "wikilink"): [SAP](../Page/SAP_\(企業\).md "wikilink")
  - SAS OLAP Server : [SAS Institute](../Page/SAS_Institute.md "wikilink")
  - [WebFOCUS](https://ja.wikipedia.org/wiki/WebFOCUS "wikilink")：[Information Builders](https://ja.wikipedia.org/wiki/Information_Builders "wikilink")

BPM([Business performance management](https://ja.wikipedia.org/wiki/Business_performance_management "wikilink"))製品のベンダはOLAPで大きな地位を占めている。

## 外部リンク

  - [Dimensional Modeling and OLAP Tutorial](http://freedatawarehouse.com/tutorials/dmtutorial/Dimensional%20Modeling%20Tutorial.aspx)
  - [Data Warehousing and OLAP: A Research-Oriented Bibliography](http://www.ondelette.com/OLAP/dwbib.html)
  - [OLAP Report: In depth overview of all commercial OLAP products](http://www.olapreport.com)
  - [Microsoft OLAP information](http://www.mosha.com/msolap)
  - [Mondrian Java R-OLAP server](http://mondrian.sourceforge.net/)
  - [Lemur OLAP C++ Library](http://www.nongnu.org/lemur/) (実験的なGPLライブラリ)
  - [A chapter from Erik Thomsen's book *OLAP Solutions: Building Multidimensional Information Systems*, 2nd Edition](http://dev.hyperion.com/resource_library/articles/olap_solutions.cfm)
  - [Jaspersoft(日本語サイト)](http://jaspersoft.biz/)
  - [Pentaho BI suite](http://www.pentaho-partner.jp/)

[Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink") [Category:ITマネジメント](https://ja.wikipedia.org/wiki/Category:ITマネジメント "wikilink")