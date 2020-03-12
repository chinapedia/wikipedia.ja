> この記事は[Apache Solr](https://ja.wikipedia.org/wiki/Apache_Solr)から翻訳されています。


**Solr**（ソーラー）は、[オープンソース](../Page/オープンソース.md "wikilink")の[全文検索](../Page/全文検索.md "wikilink")システム。[Apacheソフトウェア財団](../Page/Apacheソフトウェア財団.md "wikilink")の[Lucene](https://ja.wikipedia.org/wiki/Lucene "wikilink")プロジェクトのサブプロジェクトとして開発されている。

## 概要

全文検索エンジンライブラリ[Lucene](https://ja.wikipedia.org/wiki/Lucene "wikilink")をベースに、管理画面やキャッシュ機構を取り入れたアプリケーション。

機能上の特徴は、検索結果にファセットと呼ばれる検索結果を特定の軸で[クラスタリング](../Page/クラスタリング.md "wikilink")、それぞれの件数情報を付加することができること。商用の検索エンジンでもこの機能があるものは少ない。

構造上の特徴は、内部はいくつかの[コンポーネント](https://ja.wikipedia.org/wiki/コンポーネント "wikilink")に分かれ、各所にプラグイン機構を持っているため拡張性に優れる、また、さまざまなキャッシュを持つことからより多くの検索クエリを捌けるようになっていること。

なお、v1.3になって追加された[DataImportHandler](http://wiki.apache.org/solr/DataImportHandler) (DIH) という追加機能（contribに収録）を使うと、[Oracleをはじめ](../Page/Oracle_Database.md "wikilink")[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")などのデータベースから、[JDBC](../Page/JDBC.md "wikilink")を通じて直接、（検索したい）文書データを取り込む機能が備わり、より便利になった。

## 開発

2007年01月にインキュベータレベル（プロジェクトがひとり立ちして運営できるように支援されるレベル）から卒業し、現在は[Lucene](https://ja.wikipedia.org/wiki/Lucene "wikilink")のサブプロジェクトとして活動を行っている。

2007年6月6日(水)にv1.2が公開され、現在は2008年9月17日(水)に公開されたv1.3より日本人もコミッタとして参加、2バイト文字対応や半角カナへの対応などが積極的に進められている。

## 事例

日本国外では小中規模のニュースサイトだけでなく、超大規模なソーシャルニュースサイト[Digg](../Page/Digg.md "wikilink")や、[インターネットアーカイブ](../Page/インターネットアーカイブ.md "wikilink")などで利用されている。IBM WatsonのRetrieve and RankやMicrosoft AzureのLog Analytics、SAPのHybrisやSalesforceの検索機能など大手ベンダーも利用している。日本国内では[SHOOTI](https://ja.wikipedia.org/wiki/SHOOTI "wikilink")において約2億のWebページのインデキシングに利用されている。

  - [アスベル](https://ja.wikipedia.org/wiki/アスベル "wikilink") : VMwareで動く 仮想化検索アプライアンス
  - [FileBlog](https://ja.wikipedia.org/wiki/FileBlog "wikilink") : Windowsファイルサーバ向け、Web文書共有・検索・属性管理システム
  - [RONDHUIT Solrサブスクリプション](https://ja.wikipedia.org/wiki/RONDHUIT_Solrサブスクリプション "wikilink") : Lucene/Solrプロジェクトの日本人コミッタが起業したロンウイット社が提供するSolrのサポートと日本語関連追加機能を実装したパッケージ
  - [SMART/InSight G2 Open](https://ja.wikipedia.org/wiki/SMART/InSight_G2_Open "wikilink") : スマートインサイト社のサーチアプリケーション。Solrを使い複数のデータベースやファイルサーバ、Webなどを統合し、検索することができる。また結果もグラフィックで表示され、絞り込み検索で目的とする情報を検索する。
  - [Neuron](https://ja.wikipedia.org/wiki/Neuron "wikilink") : ブレインズテクノロジー社のエンタープライズサーチ。Solrベースで企業内文書の高速検索に対応　　

## 脚注

<references/>

## 外部リンク

  - [Solr(本家)](http://lucene.apache.org/solr/)
  - [Solr(wiki)](http://wiki.apache.org/solr/)
  - [Solr(開発者)](http://lucene.apache.org/solr/who.html)
  - [Solr(事例集)](http://wiki.apache.org/solr/PublicServers)
  - [ロンウイット社](https://www.rondhuit.com/)

[Category:全文検索](https://ja.wikipedia.org/wiki/Category:全文検索 "wikilink") [Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")