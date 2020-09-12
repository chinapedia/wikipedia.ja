> この記事は[Databricks](https://ja.wikipedia.org/wiki/Databricks)から翻訳されています。


**Databricks**は、[Apache Sparkの生みの親であるマテイ](https://ja.wikipedia.org/wiki/Apache_Spark "wikilink")・ザハリアと共に、アリ・ゴディシが2013年に設立した企業である。[AI](../Page/AI.md "wikilink")/[機械学習](../Page/機械学習.md "wikilink")をはじめとする[ビッグデータ](https://ja.wikipedia.org/wiki/ビッグデータ "wikilink")を扱うためのデータ基盤として、データサイエンスと機械学習の領域に強みがある。2021年に上場予定と言われている[ユニコーン企業](https://ja.wikipedia.org/wiki/ユニコーン企業 "wikilink")\[1\]。世界で約5,000社のユーザー、テクノロジー販売パートナーは約450社となっている\[2\]。

2020年[ガートナー](../Page/ガートナー.md "wikilink")「[マジッククアドラント](https://ja.wikipedia.org/wiki/マジッククアドラント "wikilink")」において、データサイエンスおよび機械学習プラットフォーム部門のリーダーとして評価されている\[3\]。

[Apache Sparkや](https://ja.wikipedia.org/wiki/Apache_Spark "wikilink")[Delta Lake](https://ja.wikipedia.org/wiki/Delta_Lake "wikilink")、[MLflow](https://ja.wikipedia.org/wiki/MLflow "wikilink")といった自社ソフト（もしくは創業メンバーが過去に開発したソフト）を組み合わせ、大規模なデータエンジニアリングとコラボレーション型データサイエンスのためのクラウドプラットフォームを開発しており、開発したソフトウェアの多くをオープンソース化し、オープンソースコミュニティとして維持していることもDatabricksの特徴である。

日本法人はデータブリックス・ジャパン株式会社。

## 創業メンバー

  - Ali Ghodsi, CEO, カリフォルニア大学バークレー校非常勤教授
  - Andy Konwinski、元バークレー大学博士課程の学生でApache Sparkのコミッター
  - Scott Shenker, Board Member, カリフォルニア大学バークレー校教授、Niciraの共同設立者で元CEO
  - Ion Stoica、カリフォルニア大学バークレー校教授、エグゼクティブチェアマン、Convivaの共同設立者兼CTO
  - Patrick Wendell、元バークレー校博士課程の学生でApache Sparkのコミッター
  - Reynold Xin, バークレー校の元博士課程の学生でApache Sparkのコミッター
  - Matei Zaharia, カリフォルニア大学バークレー校のPh.D.候補生時代にApache Sparkを作成し、現在はスタンフォード大学の教授

## 沿革

2013年9月、DatabricksはAndreessen Horowitzから1390万ドルを調達したことを発表し、GoogleのMapReduceシステムに代わるものを提供することを目指していると述べた\[4\]\[5\] 同社は2014年に3300万ドル、2016年に6000万ドル、2017年に1億4000万ドル、2019年（2月）に2億5000万ドル\[6\]、2019年（10月）に4億ドルを追加調達した\[7\]。

## 主な製品

### [Apache Spark](https://databricks.com/jp/spark/about)

ビッグデータと機械学習のための非常に高速なオープンソースのクラスタコンピューティングフレームワークである。Sparkのインタフェースを使うと、暗黙のデータ並列性と耐故障性を備えたクラスタ全体をプログラミングできる。Scala, Java, Python, R用のハイレベルなAPIや、データ分析用の一般的なコンピュテーショングラフをサポートする最適化エンジンを提供する。SQLやDataFrames向けのSpark SQL, 機械学習向けのMLlib, グラフ処理向けのGraphX, ストリーミング処理向けの Structured Streamingも提供する\[8\]。

### [Delta Lake](https://delta.io/)

オープンソースのストレージレイヤー。非構造化、構造化、半構造化データも全て一括して格納する次世代型のデータレイク・データウェアハウスである。Apache Sparkや他ビッグデータエンジンに対して、拡張性やACIDトランザクション機能を提供する。

### [MLflow](https://mlflow.org/)

オープンソースのプラットフォーム。実験、再現性確認、デプロイメント、一元的なモデルのレジストリーなどの機械学習のライフサイクルの管理を容易にする。

### [Koalas](https://koalas.readthedocs.io/en/latest/#)

オープンソースプロジェクト。panda DataFrame APIをApache Spark上に実装することで、データサイエンティストがビックデータを扱う際の生産性を向上する。

### [Pandas](https://pandas.pydata.org/)

プログラミング言語Pythonにおいて、データ解析を支援する機能を提供するライブラリである。特に、数表および時系列データを操作するためのデータ構造と演算を提供する。

## 脚注

1.
2.  <https://it.impress.co.jp/articles/-/19496>
3.  <https://databricks.com/jp/blog/2020/02/17/databricks-named-leader-in-gartner-magic-quadrant-for-data-science-and-machine-learning-platforms.html>
4.  <https://gigaom.com/2013/09/25/databricks-raises-14m-from-andreessen-horowitz-wants-to-take-on-mapreduce-with-spark/>
5.  <http://radar.oreilly.com/2013/09/databricks-aims-to-build-next-generation-analytic-tools-for-big-data.html>
6.  <https://databricks.com/company/newsroom/press-releases/databricks-250-million-funding-supports-explosive-growth-and-global-demand-for-unified-analytics-brings-valuation-to-2-75-billion>
7.  <https://techcrunch.com/2019/10/22/databricks-announces-400m-round-on-6-2b-valuation-as-analytics-platform-continues-to-grow/?guccounter=1&guce_referrer=aHR0cHM6Ly9lbi53aWtpcGVkaWEub3JnLw&guce_referrer_sig=AQAAAHel91F6Bdmi8j8V7Ey7_b7sjHcg1Djf5k6BU0HNNmjOOWPvcz209vZtb9zqBANxh9dhTsi4H59a4Bs9ACCQqvjT5veKWNV5JqamAsHsRn9481pIHv2m2vK3qy7rIg8AxR-PBJNrM2tb9bt5o7tfDA4Up6onLROJv2z-9b3FP712>
8.  [Apache Spark](https://ja.wikipedia.org/wiki/Apache_Spark "wikilink")