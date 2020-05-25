> この記事は[BigTable](https://ja.wikipedia.org/wiki/BigTable)から翻訳されています。


**Bigtable**（ビッグテーブル）とは、[Google](../Page/Google.md "wikilink")の大規模な[サーバ](../Page/サーバ.md "wikilink")上の大量のデータを管理するために設計された、[データ圧縮](../Page/データ圧縮.md "wikilink")機能を持つ高性能な[NoSQL](https://ja.wikipedia.org/wiki/NoSQL "wikilink")型の[プロプライエタリ](https://ja.wikipedia.org/wiki/プロプライエタリ "wikilink")のデータストレージシステムである。[Google File System](https://ja.wikipedia.org/wiki/Google_File_System "wikilink")、[分散ロックマネージャ](https://ja.wikipedia.org/wiki/分散ロックマネージャ "wikilink")の1種であるChubby Lock Service、SSTable（に似たログ構造化ストレージ）、その他のいくつかのGoogleの技術を活用して構築されている。2015年5月6日、パブリックバージョンのBigtableが、[Google Cloud Platformのサービスの](https://ja.wikipedia.org/wiki/Google_Cloud_Platform "wikilink")1つとして公開された。Bigtableは[Google Cloud Datastoreのバックエンドとしても利用されている](https://ja.wikipedia.org/wiki/Google_Cloud_Datastore "wikilink")\[1\]\[2\]。

## 歴史

[2004年](../Page/2004年.md "wikilink")から開発が始まり\[3\]、2006年には設計が論文として公開された\[4\]。

[MapReduce](https://ja.wikipedia.org/wiki/MapReduce "wikilink")（BigTableに格納されたデータの生成や修正にしばしば使われている）\[5\]、Google Reader\[6\]、[Google マップ](../Page/Google_マップ.md "wikilink")\[7\]、Google Print、My Search History、[Google Earth](https://ja.wikipedia.org/wiki/Google_Earth "wikilink")、[Blogger](../Page/Blogger.md "wikilink")、Google Code hosting、[Orkut](../Page/Orkut.md "wikilink")\[8\] 、[YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink")\[9\]のようないくつものアプリケーションを支えている。

Googleが自社でデータベースを開発した理由はコスト、スケーラビリティ、パフォーマンス特性のより良いコントロールなどであるとされる\[10\]。

Googleの[Spanner](https://ja.wikipedia.org/wiki/Spanner_\(データベース\) "wikilink") RDBMSは、各テーブルの[2相コミット](../Page/2相コミット.md "wikilink")ごとに[Paxosグループを持つBigtableの実装上にレイヤーを作っている](https://ja.wikipedia.org/wiki/Paxosアルゴリズム "wikilink")。は、Spannerを用いて[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")に依存する実装を置き換えるために作られた\[11\]。

## 技術

BigTableは高速で超大規模な[列指向DBMSである](https://ja.wikipedia.org/wiki/列指向データベース管理システム "wikilink")。行ではなく、列からの高速な読み込みに焦点を当てている。BigTableは数百から数千台のサーバの[ペタバイト](https://ja.wikipedia.org/wiki/ペタバイト "wikilink")までのデータを扱い、システムにサーバを簡単に増設して、再設定なしにそれらのリソースを自動的に利用し始めるように設計されている\[12\] 。

各テーブルは多次元である。1つ1つのフィールドはその時点のスナップショットを持ち、バージョニングを行う事が出来る。テーブルはGFSに最適化されており、大きなテーブルは複数の*Tablet segment*（タブレットセグメント）に自動的に[分割される](https://ja.wikipedia.org/wiki/分割_\(データベース\) "wikilink")。分割はタブレットが200[メガバイト](../Page/メガバイト.md "wikilink")のサイズになるように行の境界で行われる。サイズが特定の限界を超える兆候が見られた場合、テーブルはBMDiffとZippyアルゴリズムを使用して圧縮される。これらは[LZWより圧縮率で劣るが](../Page/Lempel–Ziv–Welch.md "wikilink")、計算量で勝っている。

タブレットのGFS内の位置（サーバのIPとPort）は、「META1」タブレットと呼ばれる複数の特別なタブレットにデータベースエントリとして記録されている。META1タブレットは1つだけある「META0」タブレットを照会する事で作成される。「META0」タブレットは通常は１つのマシンを占有している。「META1」タブレットの位置に関してクライアントから頻繁に問い合わせを受けるからである。「META1」タブレットはそれ自体が、実際のデータの位置についての答えを持っている。GFSマスターサーバのように、META0は通常はボトルネックにはならない。META1の位置を発見・送信する為に必要なプロセッサ時間と帯域はごく僅かである。クライアントは積極的に位置をキャッシュして、照会を必要最低限にするからである。

## 他の実装

[Hadoop](https://ja.wikipedia.org/wiki/Hadoop "wikilink")プロジェクトは、BigTableの現在の実装を目指して改良を加えられている。[HBase](https://ja.wikipedia.org/wiki/HBase "wikilink")と呼ばれている。

> "Just as Bigtable leverages the distributed data storage provided by the Google File System, Hbase will provide Bigtable-like capabilities on top of Hadoop."

  - [Hypertable](https://ja.wikipedia.org/wiki/Hypertable "wikilink")

## 関連事項

  - [Google App Engine](https://ja.wikipedia.org/wiki/Google_App_Engine "wikilink")
  - [MapReduce](https://ja.wikipedia.org/wiki/MapReduce "wikilink")
  - [Spanner (データベース)](https://ja.wikipedia.org/wiki/Spanner_\(データベース\) "wikilink")
  - [列指向データベース管理システム](https://ja.wikipedia.org/wiki/列指向データベース管理システム "wikilink")
  - [エラー忘却型コンピューティング](https://ja.wikipedia.org/wiki/エラー忘却型コンピューティング "wikilink")

## 参考文献

<references/>

## 外部リンク

  - [丸山先生レクチャーシリーズ第3回リポート：クラウドのデータサービスを掘り下げる](http://www.itmedia.co.jp/enterprise/articles/0901/26/news022.html)（ITmedia）
      - [講演資料](http://stream.itmedia.co.jp/enterprise/pdf/pdf_13_1231755243.pdf)

[Category:Google](https://ja.wikipedia.org/wiki/Category:Google "wikilink") [Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink")

1.
2.
3.  "First an overview. BigTable has been in development since early 2004 and has been in active use for about eight months (about February 2005)." [Google's BigTable](http://andrewhitchcock.org/?post=214)
4.
5.  "Bigtable can be used with MapReduce, a framework for running large-scale parallel computations developed at Google. We have written a set of wrappers that allow a Bigtable to be used both as an input source and as an output target for MapReduce job". pg 3 of "Bigtable: A Distributed Storage System for Structured Data", 2006
6.  "Reader is using Google's BigTable in order to create a haven for what is likely to be a massive trove of items." [Official Google Reader](http://googlereader.blogspot.com/2005/10/google-reader-two-weeks.html) blog.
7.  "There are currently around 100 cells for services such as Print, Search History, Maps, and Orkut." [Google's BigTable](http://andrewhitchcock.org/?post=214)
8.
9.  "Their new solution for thumbnails is to use Google’s BigTable, which provides high performance for a large number of rows, fault tolerance, caching, etc. This is a nice (and rare?) example of actual synergy in an acquisition." [YouTube Scalability Talk](http://kylecordes.com/2007/07/12/youtube-scalability/)
10. "We have described Bigtable, a distributed system for storing structured data at Google....Our users like the performance and high availability provided by the Bigtable implementation, and that they can scale the capacity of their clusters by simply adding more machines to the system as their resource demands change over time...Finally, we have found that there are significant advantages to building our own storage solution at Google. We have gotten a substantial amount of flexibility from designing our own data model for Bigtable." from the Conclusion of "Bigtable: A Distributed Storage System for Structured Data", 2006
11. .
12. \*["Database War Stories \#7: Google File System and BigTable"](http://radar.oreilly.com/archives/2006/05/database_war_stories_7_google.html)