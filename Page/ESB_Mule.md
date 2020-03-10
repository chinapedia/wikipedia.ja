> この記事は[ESB Mule](https://ja.wikipedia.org/wiki/ESB_Mule)から翻訳されています。


**ESB Mule**は、米MuleSoft社が開発・サポートしている、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で開発された[オープンソース](../Page/オープンソース.md "wikilink")のアプリケーション統合/連携用のフレームワークである。

IBM WebSphereのような多くの商用[ESB](https://ja.wikipedia.org/wiki/ESB "wikilink")（エンタープライズ・サービス・バス）と以下の点が異なる：

1.  ESB Muleは、開発者が修正・拡張できる[コンポーネント](https://ja.wikipedia.org/wiki/コンポーネント "wikilink")集である。ただし、配布されているダウンロード・ファイルには標準で多くのコンポーネントが同梱されている他に開発者コミュニティが充実しているために、標準のコンポーネントを使って多くのシステムを連携することができる。
2.  ESB MuleはWebサービス/SOAPを前提にしておらずfile://, FTP, HTTP(REST),JMS,SMTP等を使うことが可能である。連携はグラフィカルエディタMule Studioを利用して記述するか、Javaやスクリプト言語を使用して記述する。
3.  修正及び拡張できる、多くのアプリケーション連携用のクラスが公開されている。未対応な機能を要する場合は、提供されているクラスを修正／拡張して開発することができる。全てを独自で開発するよりも、提供される部品を修正／拡張することで、開発コストを削減し、開発期間を短縮する。なお、実績ある標準クラスを使うことで、テスト期間を短縮し、信頼性を向上する。
4.  **ピア・ツ・ピア構成**が可能。1台のサーバ構成も可能であるが、システムの信頼性と性能を重視する場合はサーバ毎にESB Mule用の[ライブラリ](../Page/ライブラリ.md "wikilink")をインストールする構成が可能である。無償のコミュニティ版では、サーバ数による価格費用は発生しない。
5.  ESB MuleをSOA的な開発で使うことは可能だが、SOAを前提としない。また、ESB Muleを使ったからSOAということにはならない。
6.  ESB Muleにはファイル, データベース, 業務アプリケーションと連携するプロバイダが提供されているために、DSP（データ・サービス・プロバイダ）として利用することも可能である。

[SOA](https://ja.wikipedia.org/wiki/SOA "wikilink")（Service Oriented Architecture）や[ROA](https://ja.wikipedia.org/wiki/ROA "wikilink")（Resource Oriented Architecture）の基盤として使う他に、Hulftのようなシステム間のデータ連携ツールの簡易版として使うこともできる。アプリケーション連携用としてSAP、Salesforce、SugarCRM、SWIFT、SMTP、POP3等のアダプタも提供されている他に、メッセージの分割・結合、データ暗号・解読、データ構造変換などの標準コンポーネントも提供されている。ファイル転送の起動も、ディレクトリのポーリング、トリガー、スケジューリングなどで行うように設定できる。

MuleSoft社からは無償とコミュニティ版と有償のエンタープライズ版が提供されている。コミュニティ版としてESB Muleとサービス・構成リポジトリ／レジストリMule Galaxyが公開されている。エンタープライズ版にはMuleを一括管理するための管理コンソールMule Management Consoleが同梱されているが、一般の小中規模システムであればコミュニティ版で十分利用することができる。 高性能・軽量であり、豊富なプロトコル・アダプタを提供しているために、海外では[Walmart.com](http://www.walmart.com),[Leap Frog](http://www.leapfrog.com/en/shop.html)や金融業界での豊富な実績がある。

## システム構成

ESB Muleは特にシステム構成の制限を設けていないため、以下のようなシステム構成が可能である：

1.  性能、性能、セキュリティを重視する場合は、各アプリケーション・サーバにESB Muleをセットアップして通信定義をするピア・ツ・ピア構成にすることもできる：
      -
        [ファイル:MulePeer2peer.jpg](https://ja.wikipedia.org/wiki/ファイル:MulePeer2peer.jpg "wikilink")
2.  通信設定をリポジトリや共有サーバに置く構成も可能：
      -
        [ファイル:MuleRepository.jpg](https://ja.wikipedia.org/wiki/ファイル:MuleRepository.jpg "wikilink")
3.  他ESBのように、集中サーバ構成の構成も可能：
      -
        [ファイル:MuleCentral.jpg](https://ja.wikipedia.org/wiki/ファイル:MuleCentral.jpg "wikilink")

## アーキテクチャ

ESB Muleのアーキテクチャは以下の3項目を特徴としている：

1.  ESB MuleはGregor Hohpe著「エンタープライズ統合パターン」で定義されている基本パターンに基づいて設計されている。
2.  [SEDA](../Page/SEDA.md "wikilink")を利用している。
3.  内部コンポーネントの生成に、外部DIコンテナを使うことができる。

[ファイル:Mule-overview.jpg](https://ja.wikipedia.org/wiki/ファイル:Mule-overview.jpg "wikilink")

開発者のRoss Masonはイギリスの証券システム用の開発を行っていて、システム連携に類似したプログラムを開発していることに気が付いた。Gregor Hohpe著「エンタープライズ統合パターン」を参照して、繰り返して開発を行って来た、プログラムを整理して、ESB Muleのアーキテクチャを考えた。

アプリケーション連携を行うプログラムは以下の部品に分別できる：

1.  アプリケーションのアドレスを特定する受信エンドポイント
2.  データを受け取る受信レシーバー
3.  特定のレシーバーと特定のトランスフォーマーを対応付ける受信コネクタ
4.  データ形式を変換する受信トランスフォーマー
5.  データのルーティング制御するルータ
6.  データにビジネス処理を行うUMOコンポーネント
7.  ビジネス処理を行った後のデータの形式を、送信先用のデータ形式に変換する送信トランスフォーマー
8.  特定の送信トランスフォーマーと特性のディスパッチャを対応付ける送信コネクタ
9.  データを送信するディスパッチャ
10. 送信先のアプリケーション用にアドレスを指定する送信エンドポイント

このように通信処理を分裂することにより、各部品の入れ替えを疎結合に行えるようにする。例えば、ローカル・ファイル・システムからファイルを読み込み、ファイルに書き出す処理を、メールを送信するように設定を変換することができる。

なお、レシーバー、コネクタ、トランスフォーマー及びディスパッチャー、コネクタ、トランスフォーマーの集まりをプロバイダ又はアダプタと言う。例えばSAPやSalesforceと接続するためにはアプリケーションのAPI、データ形式、通信プロトコルが決められているために、SAPアダプタ及びSalesforceアダプタが提供されている。しかし、Oracleデータベースに接続する場合は、APIとプロトコールがJDBCでAPIとプロトコルが定められているが、データ型は不明なために汎用的なOracle用アダプタはなく、開発者がトランスフォーマーを作成する必要がある。

これらのESB Muleのコンポーネントは[POJO](https://ja.wikipedia.org/wiki/POJO "wikilink")である。ESB MuleはPOJOの管理を行うが、生成は[SpringFramework](https://ja.wikipedia.org/wiki/SpringFramework "wikilink")のような外部DIコンテナを使うこともできる。この場合は、SpringFrameworkの設定でESB Muleの設定も行うことができる。

## 競合製品

オープンソースSOAソリューションとしては、元米IBM研究所で多くのWS-\*仕様を作成したメンバーが設立した[wso2](http://wso2.com/)が主な競合相手である。相互の社長のブログにも言い争いが書き込まれている。

## 歴史

  - 2013年4月: Mule ESB 3.4.0を公開
  - 2009年9月: 開発元MuleSource社がMuleSoft社に社名変更
  - 2008年4月：ESB Mule2.0コミュニティ版を公開
  - 2008年1月：REST型サービス・リポジトリ／レジストリMule Galaxyを発表
  - 2008年1月：日本Mule開発者グループにより日本語ページを正式に公開し、グループとしてESB Muleのローカライゼーションを行うことにした。
  - 2007年：XFireの開発者がMuleSourceの社員となり、SOAガバナンス・ツールGalaxyの開発を始める。
  - 2007年5月：：米ベンチャーキャピタル会社Lightspeed Venture Partnersから1250万ドルの資金を調達する。
  - 2006年10月：米ベンチャーキャピタル会社Hummer Winblad Venture PartnersとMorgenthalerから400万ドルの資金を調達する。
  - 2006年7月：Ross MasonとDave Rosenbergが組み、米サンフランシスコにベンチャー会社MuleSourceを設立する。Ross MasonがCTOとなり、Dave RosenbergがCEOとなる。
  - 2005年：HOzawaにより、ESB Muleをローカライズして日本語環境で動作できるようした。
  - 2003年：システム統合に多く使われるコンポーネントを繰り返して開発するのに飽きて、Ross MasonがMuleの開発を始める。Muleと名前を付けた理由は、ロバのように体力を使う面白くない作業を行うソフトウエアであるためである。
  - 2001年：システム間のデータ連携を行う度に繰り返される「Donkey Work」（単純の力仕事）を削減するために、Ross Masonがロンドン投資銀行向けにESB Muleの原型を開発する。

## ツール

  - Mule Studio Mule ESBの連携フロー記述、データマッピングを支援するためのグラフィカルエディタ。
  - Mule Management Console 運用監視をウェブ画面から行うことができるツール。

## 類似製品

  - [wso2](http://wso2.com/)
  - [Apache ServiceMix](http://servicemix.apache.org/)
  - [Cape Clear](https://ja.wikipedia.org/wiki/Cape_Clear_\(ソフトウエア会社\) "wikilink")
  - Celtix (オープンソース)
  - [E2E Bridge](http://www.E2EBridge.com) (独自)
  - [IONA Artix](https://ja.wikipedia.org/wiki/IONA_Technologies "wikilink") (独自)
  - [OpenESB](https://ja.wikipedia.org/wiki/OpenESB "wikilink") (オープンソース)
  - Sonic ESB (プロプライエタリ)

## 受賞

2007年：米InfoWorld誌のオープンソース・ミドルウエアに選定

## 外部リンク

  - [Mule コミュニティサイト](http://www.mulesoft.org/)
  - [MuleSoft社のサイト](http://mulesoft.com/)

[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:Java_enterprise_platform](https://ja.wikipedia.org/wiki/Category:Java_enterprise_platform "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:システムソフトウェア](https://ja.wikipedia.org/wiki/Category:システムソフトウェア "wikilink")