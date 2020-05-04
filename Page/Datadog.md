> この記事は[Datadog](https://ja.wikipedia.org/wiki/Datadog)から翻訳されています。


[サムネイル](https://ja.wikipedia.org/wiki/ファイル:DatadogGoogleCloudSummit.jpg "wikilink") **Datadog（データドッグ）**はクラウド時代の監視アプリケーションサービス。[SaaS](../Page/SaaS.md "wikilink")ベースのデータ分析プラットフォームを介してサーバー、データベース、ツール、およびサービスの監視を提供している。

## 技術

Datadogは、2018年2月28日にリリースされたメジャーバージョン6.0.0以降、[Goベースのエージェントを使用しており](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink")、ゼロから書き直された。\[1\] 以前は[Python](../Page/Python.md "wikilink")ベースで、\[2\] 2009年に[Server Density](https://ja.wikipedia.org/wiki/:en:Server_Density "wikilink") （以前はBoxed Iceと呼ばれていた）のためにDavid Mytton \[3\]によって作成されたオリジナルから分岐した。SaaSシステムのバックエンドには、[D3](https://ja.wikipedia.org/wiki/D3.js "wikilink")、[Apache Cassandra](https://ja.wikipedia.org/wiki/Apache_Cassandra "wikilink")、Kafka、[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")などを含む多くの[オープンソースおよび](../Page/オープンソースソフトウェア.md "wikilink")[クローズドソース技術を使用して構築されている](../Page/プロプライエタリ・ソフトウェア.md "wikilink")。\[4\]

2014年、Datadogのサポート対象プラットフォームは、[Amazon Web Services](https://ja.wikipedia.org/wiki/Amazon_Web_Services "wikilink") （AWS）、[Microsoft Azure](https://ja.wikipedia.org/wiki/Microsoft_Azure "wikilink")、[Google Cloud Platform](https://ja.wikipedia.org/wiki/Google_Cloud_Platform "wikilink")、[Red Hat](../Page/レッドハット.md "wikilink") [OpenShift](https://ja.wikipedia.org/wiki/OpenShift "wikilink")などの複数のクラウドサービスプロバイダーに拡大された。2019年現在、同社は350を超える統合を最初から使える状態で提供している。

## 歴史

Datadogは、Wireless Generationで同僚として働いていたOlivier PomelとAlexisLê-Quôcによって2010年に設立された\[5\]。WirelessCorporationがNewsCorpに買収された後、2人は、相反する目的で作業することが多い開発者とシステム管理者チームとの間の摩擦を軽減できる製品を提供しようと試みた。

彼らは、Datadogをダッシュボード、アラート、およびメトリクスの視覚化を備えたクラウドインフラストラクチャ監視サービスとして構築した。クラウドの採用が増加するにつれて、Datadogは急速に成長し、Amazon Web Services（AWS）、Microsoft Azure、Google Cloud Platform、Red Hat OpenShift、[OpenStack](https://ja.wikipedia.org/wiki/OpenStack "wikilink")などのサービスプロバイダーをカバーするために製品提供を拡大した。\[6\]

2015年、DatadogはMortar Dataの買収を発表し\[7\]、チームに加え、Datadogのプラットフォームにデータおよび分析機能を追加した。その年、Datadogはパリに研究開発オフィスも開設した。\[8\]

2016年、Datadogはニューヨーク市の本社をニューヨークタイムズビルのワンフロアに移転し、成長するチームを支えた\[9\]。Datadogは2016年にApplication Performance Monitoring(APM)のベータリリースを発表し\[10\]、フルスタック監視ソリューションを初めて提供した。2017年現在、同社の従業員は300人近くとなり、その大部分は米国（マンハッタン、ボストン、ボルチモアにオフィス）にあり、パリに新しいR＆D施設があった。\[11\]

Datadogは過去に他の管理プラットフォームを買収している。2017年に、パリを拠点とするLogmatic.ioを買収した。これは、オンラインサービスを監視およびトラブルシューティングするために、ログのクエリと視覚化を行うプラットフォームに依存しないサービスである。\[12\] 2019年、AIベースのアプリケーションテストプラットフォームであるMadumboがDatadogに参加した。\[13\]

2019年、Datadogは東京に日本法人、Datadog Japan合同会社（データドッグ ジャパン）を設立した。\[14\]

## 資金調達

2017年の時点で、Datadogは5ラウンドの資金調達を行い、合計1億4,790万ドルを調達した。\[15\] 2010年、Datadogはシードラウンドを開始し、NYC Seed、Contour Venture Partners、IA Ventures、Jerry Neumann、Alex Payneなどが参加した。2012年には、Index VenturesとRTP Venturesが共同で行うシリーズAラウンド620万ドルを調達した。\[16\] 2014年Datadogは、OpenViewのベンチャーパートナーによる$ 15MのシリーズBの調達をした。\[17\]ラウンド2015年インデックス・ベンチャーズが率いる$ 31MシリーズCに続き、\[18\] Datadogは、ICONIQ Capitalが率いる9450万ドルのシリーズDラウンドを2016年に開示した。\[19\]その年のニューヨーク市の企業にとって最大の資金調達ラウンドの1つである。\[20\]

## 製品

[サムネイル](https://ja.wikipedia.org/wiki/ファイル:Datadog_high-level_architecture.svg "wikilink") Datadogは、開発者と運用チームがクラウド、サーバー、アプリ、サービス、メトリックスなどのインフラストラクチャ全体をすべて1か所で確認できるようにする。これには、チームの特定のニーズに合わせてカスタマイズできるリアルタイムのインタラクティブダッシュボード、メトリックとイベントの全文検索機能、チームが表面化したインサイトを使用して共同作業できるようにする共有ツールとディスカッションツール、重要な問題のターゲットアラート、および独自のインフラストラクチャに対応するためのAPIアクセスが含まれる。

また、Datadogはさまざまなクラウド、オンプレミス、および開発者向けソフトウェアツールとすぐに統合できるため、Datadogのサービスを採用しても、確立されたチームワークフローの変更や中断の必要はない。

## 受賞歴

Datadogは、ForbesのCloud 100 \[21\]に掲載されており、デロイトの2016 Fast 500 Listで北米で最も急成長している企業のトップ10にランクされた。\[22\] 2015年\[23\]と2016年の両方で\[24\] CrainはDatadogをニューヨーク市の働きがいのある職場100に挙げた。Datadogは、Wealthfrontの2017年のキャリア立ち上げ企業リスト\[25\]およびBusiness Insiderの51のエンタープライズスタートアップにも掲載され、2017年にあなたのキャリアを賭けている。 BuiltInは、ボストンで2019年に働く5番目のトップ企業に選定した。\[26\]

## 脚注

## 外部リンク

  - [Datadog日本語公式サイト](https://www.datadoghq.com/ja/)
  - [CrunchbaseのDatadog](http://www.crunchbase.com/company/datadog)
  - [451 Research：DatadogがCラウンドで3,100万ドルを調達し、次の成長の波に資金を提供](https://451research.com/report-short?entityId=84188)
  - [451 Research：Datadogは、Mortar Dataの買収により分析機能を拡張](https://451research.com/report-short?entityId=84321)
  - [リアルタイムデータ分析：Datadogで学んだ教訓](https://docs.google.com/presentation/d/1yxcg4DdC-Uss1zh_lhtSWXICn7g-5udJN0XaV2oRaj4/pub?start=false&loop=false&delayms=3000)

[Category:NASDAQ上場企業](https://ja.wikipedia.org/wiki/Category:NASDAQ上場企業 "wikilink") [Category:2019年上場の企業](https://ja.wikipedia.org/wiki/Category:2019年上場の企業 "wikilink") [Category:2010年開設のウェブサイト](https://ja.wikipedia.org/wiki/Category:2010年開設のウェブサイト "wikilink") [Category:アメリカ合衆国のコンピュータ企業](https://ja.wikipedia.org/wiki/Category:アメリカ合衆国のコンピュータ企業 "wikilink") [Category:未査読の翻訳があるページ](https://ja.wikipedia.org/wiki/Category:未査読の翻訳があるページ "wikilink")

1.  GitHub, ["Datadog / datadog-agent."](https://github.com/DataDog/datadog-agent) Retrieved June 6, 2018.
2.  GitHub, ["Datadog / dd-agent."](https://github.com/DataDog/dd-agent) Retrieved February 20, 2015.
3.
4.  Hakka Labs, Alexis Lê-Quôc, ["Realtime Data Analytics at Datadog."](https://www.hakkalabs.co/articles/realtime-data-analytics-at-datadog) January 9, 2014. Retrieved February 20, 2015
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
15. <https://www.crunchbase.com/organization/datadog#/entity>
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.