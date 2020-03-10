> この記事は[Nagios](https://ja.wikipedia.org/wiki/Nagios)から翻訳されています。


（ナギオス）は、[オープンソース](../Page/オープンソース.md "wikilink")の[コンピュータシステム](../Page/コンピュータシステム.md "wikilink")および[ネットワークの監視のための](../Page/ネットワーク監視.md "wikilink")[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")である。 は指定されたノードとサービスを監視し、問題が発生したり解決したりした時にユーザーに通知する。

当初 [NetSaint](http://www.netsaint.org) の名称で Ethan Galstad を中心として開発され、保守されている。また、各種[プラグイン](../Page/プラグイン.md "wikilink")は何人かの[ソフトウェア開発者](https://ja.wikipedia.org/wiki/ソフトウェア開発者 "wikilink")が活発に保守している。

当初 [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") 向けに開発されたが、現在ではその他の[UNIX](../Page/UNIX.md "wikilink")系[OSでも動作する](../Page/オペレーティングシステム.md "wikilink")。

は[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")の  バージョン 2 で[ライセンス](../Page/ライセンス.md "wikilink")提供されている。

## 概要

  - ネットワークサービスの監視（[SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")、[POP3](../Page/Post_Office_Protocol.md "wikilink")、[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[NNTP](../Page/Network_News_Transfer_Protocol.md "wikilink")、[ICMP](../Page/Internet_Control_Message_Protocol.md "wikilink")、[SNMP](../Page/Simple_Network_Management_Protocol.md "wikilink")、[FTP](../Page/File_Transfer_Protocol.md "wikilink")、[SSH](../Page/Secure_Shell.md "wikilink")）
  - ホストのリソース（[CPU](../Page/CPU.md "wikilink")負荷、[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")使用量、システムログ）の監視。大部分のOSを監視可能であり、 も [NRPE_NT](http://www.miwi-dv.com/nrpent) プラグインを使って監視可能。
  - その他プローブを使った監視（温度、アラームなど）。それぞれ専用のプラグインを使ってネットワーク経由で各種データを収集。
  - リモート監視には、[SSH](../Page/Secure_Shell.md "wikilink") か [SSL](../Page/Transport_Layer_Security.md "wikilink")[暗号](../Page/暗号.md "wikilink")トンネルを使う。
  - プラグインの設計は単純で、ユーザーは必要に応じて監視したい事象についてのプラグインを開発できる。プラグイン記述言語としては、、、、、、、 などが使える。
  - サービスの確認は並行して実施可能。
  - ホストのダウン状態の検出や到達可能性の検出のため、ホスト間の[階層構造](../Page/階層構造.md "wikilink")を定義することができる。
  - 問題発生時や解決時に指定された方法（[電子メール](../Page/電子メール.md "wikilink")、[無線呼び出し](../Page/無線呼び出し.md "wikilink")、[SMS](https://ja.wikipedia.org/wiki/ショートメッセージサービス "wikilink")、その他ユーザーがプラグインで実装した方法）で通知する。
  - 問題発生時にその解決のために機能するイベントハンドラを定義できる。
  - 自動[ログファイルローテーション](../Page/データログ.md "wikilink")
  - 監視ホストの[冗長化](../Page/冗長化.md "wikilink")実装をサポート
  - オプションでネットワーク状態、通知、履歴、ログファイルなどを閲覧できるウェブインタフェース

## 名称の由来

Ethan Galstad の公式サイトにある [FAQ](http://www.nagios.org/faqs/viewfaq.php?faq_id=2&expand=false&showdesc=true) によれば、N.A.G.I.O.S. は[再帰的頭字語](https://ja.wikipedia.org/wiki/再帰的頭字語 "wikilink")であり「」（Nagios は聖人の地位に固執しない）の略であるという。これは当初の名称「」にちなんだものである。「」 は[ギリシア語](https://ja.wikipedia.org/wiki/ギリシア語 "wikilink")「」のラテン翻字であり、聖人（）を意味する。

## 参考文献

  - Barth, Wolfgang; (2006年)「[](http://www.nostarch.com/frameset.php?startat=nagios)」 - No Starch Press ISBN 1-59327-070-4
  - Turnbull, James; (2006)「[](http://www.apress.com/book/bookDisplay.html?bID=10096)」 - San Francisco: Apress ISBN 1-59059-609-9
  - Josephsen, David; (2007年)「[](http://www.pearson.ch/Informatik/PrenticeHall/1471/9780132236935/Building_a_Monitoring_Infrastructure.aspx)」 - Prentice Hall ISBN 0-13-223693-1
  - Dondich, Taylor; (2006年)「[](http://www.oreilly.com/catalog/networknagios/index.html)」 - O'Reilly ISBN 0-596-52819-1

## 外部リンク

  - [公式サイト](http://www.nagios.org)
  - [Nagios Information Ja](http://nagios.x-trans.jp/naija/) - Nagios 公式ドキュメントの日本語訳プロジェクト

[Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:分散処理](https://ja.wikipedia.org/wiki/Category:分散処理 "wikilink") [Category:マルチエージェントシステム](https://ja.wikipedia.org/wiki/Category:マルチエージェントシステム "wikilink")