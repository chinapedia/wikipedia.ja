> この記事は[Apache Mesos](https://ja.wikipedia.org/wiki/Apache_Mesos)から翻訳されています。


**Apache Mesos**は、[コンピュータ・クラスタを管理するための](../Page/コンピュータ・クラスター.md "wikilink")[オープンソースプロジェクトである](../Page/オープンソースソフトウェア.md "wikilink")。[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")で開発された。

## 歴史

当初、MesosはUC Berkeley RAD Labの研究プロジェクトとしてPhDの学生だったBenjamin Hindman、Andy Konwinski、と、教授のにより始められた。学生たちは、が教えていた授業のプロジェクトとして開発を始めた。始めは*Nexus*という名前だったが、他の大学のプロジェクトと名称がかぶっていたため、Mesosという名前に変更された\[1\]。

2009年のHotCloud '09において、Andy Konwinskiによって（まだNexusという名前で）Mesosに関する初めての論文投稿と発表が行われた\[2\]。 その後、2011年の[Usenix](../Page/USENIX.md "wikilink") Symposium on Networked Systems Design and Implementationのカンファレンスにおいて、Zahariaによりより成熟したプロジェクトになっていることが発表された。このとき投稿された論文は、"Mesos: A Platform for Fine-Grained Resource Sharing in the Data Center" by Benjamin Hindman, Andy Konwinski, Zaharia, , Anthony D. Joseph, , , である\[3\]。

2016年7月27日、[Apache Software Foundationはバージョン](../Page/Apacheソフトウェア財団.md "wikilink")1の公開を発表した\[4\]。このバージョンでは、[Docker](https://ja.wikipedia.org/wiki/Docker "wikilink")、[rkt](https://ja.wikipedia.org/wiki/Container_Linux "wikilink")、[appcのインスタンスを集中的に供給する機能が追加された](https://ja.wikipedia.org/wiki/Container_Linux "wikilink")\[5\]。

## 技術

MesosはLinuxの[cgroups](https://ja.wikipedia.org/wiki/cgroups "wikilink")を活用することで、[CPU](../Page/CPU.md "wikilink")、[メモリ](../Page/仮想記憶.md "wikilink")、[I/O](../Page/入出力.md "wikilink")、[ファイルシステム](../Page/ファイルシステム.md "wikilink")の隔離（isolation）を実現している\[6\]。

Mesosは[Google](../Page/Google.md "wikilink")のサービスを管理・分散処理するためにGoogle内部でプライベートに使用されている、[Borgスケジューラと比較できる](../Page/Borg_\(クラスタマネージャ\).md "wikilink")\[7\]。

### Apache Aurora

は、長期間の実行サービスとcronジョブのためのMesosフレームワークである。Twitterが2010年に開発し、2013年後半にオープンソース化された\[8\]。数万ノードのサーバーにスケールすることができ、サービスの設定に[ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink")（DSL）を使用するなど、Borgとの類似点を多く持っている\[9\]\[10\]。

### Chronos

Chronosは、ジョブ間の依存関係を宣言できる、柔軟な分散cron-likeシステムである\[11\]。

### Marathon

Marathonは、数千台の物理サーバーにスケールする[platform as a serviceまたは](../Page/Platform_as_a_Service.md "wikilink")[オーケストレーションシステムを促進するためのものである](../Page/オーケストレーション_\(コンピュータ\).md "wikilink")。完全な[RESTベースのシステムであり](../Page/Representational_State_Transfer.md "wikilink")、[canary-styleのデプロイとデプロイ](https://ja.wikipedia.org/wiki/フィーチャートグル "wikilink")・トポトジを可能にする。プログラミング言語[Scala](../Page/Scala.md "wikilink")で書かれている\[12\]。

## ユーザー

ソーシャル・ネットワーキングサイトのTwitterは、HindmanがTwitterエンジニアのグループで発表した後の2010年から、MesosとApache Auroraを使用し始めた\[13\]。

Airbnbは、2013年7月から、[Apache Hadoopや](https://ja.wikipedia.org/wiki/Apache_Hadoop "wikilink")[Apache Sparkなどのデータ処理システムを実行するためにMesosを使用していると話している](https://ja.wikipedia.org/wiki/Apache_Spark "wikilink")\[14\]。

2014年4月、インターネットオークションサイトの[eBay](https://ja.wikipedia.org/wiki/eBay "wikilink")は、Mesosを[継続的インテグレーション](https://ja.wikipedia.org/wiki/継続的インテグレーション "wikilink")を開発者ごとに実行できるようにするために使用していると発表した。カスタムのMesosプラグインを使用することで、開発者自身がプライベートの[Jenkins](https://ja.wikipedia.org/wiki/Jenkins "wikilink")インスタンスを起動できるようになったと説明している\[15\]。

2015年4月、[Appleは](../Page/アップル_\(企業\).md "wikilink")、[Siri](https://ja.wikipedia.org/wiki/Siri "wikilink")が独自のMesos frameworkのJarvisを使用していることを発表した\[16\]。

2015年8月、[VerizonはデータセンターのサービスのオーケストレーションにMesosphereのDC](../Page/ベライゾン・コミュニケーションズ.md "wikilink")/OSを選択したと発表した\[17\]。

2015年11月、[Yelp](https://ja.wikipedia.org/wiki/Yelp "wikilink")はMesosとMarathonを1.5年間本番サービスで使用していることを発表した\[18\]。

## 商用サポート

ソフトウェアスタートアップのは、Apache Mesosに基づいた[分散オペレーティングシステム](https://ja.wikipedia.org/wiki/分散オペレーティングシステム "wikilink")であるを販売している\[19\]。 2015年9月、[Microsoftは](../Page/マイクロソフト.md "wikilink")、Mesosphereとの商業パートナーシップを結び、[Microsoft Azure向けのコンテナスケジューラとコンテナオーケストレーションサービスを構築することを発表した](https://ja.wikipedia.org/wiki/Microsoft_Azure "wikilink")\[20\]。2015年10月、[Oracleは](../Page/オラクル_\(企業\).md "wikilink")、[Oracle Container Cloud ServiceでのMesosに対するサポートを発表した](https://ja.wikipedia.org/wiki/Oracle_Cloud "wikilink")\[21\]。

## 関連項目

  -
  -
## 出典

## 外部リンク

  -
[Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.