> この記事は[WebOTX](https://ja.wikipedia.org/wiki/WebOTX)から翻訳されています。


**WebOTX**は[日本電気](../Page/日本電気.md "wikilink")(NEC)が提供するサービス実行基盤で、[NGNや](https://ja.wikipedia.org/wiki/Next_Generation_Network "wikilink")[ユビキタス](https://ja.wikipedia.org/wiki/ユビキタス "wikilink")領域に対する機能の提供を目指している。 OTXは、Open Technology eXtensions を表している。 マスコットは、忍者。最新のバージョンは10.2である(2019年3月現在)

## WebOTXの構成

1.  サービスコンポーネント
      - WebOTX SIP Call Control
      - WebOTX RFID Manager
      - WebOTX Speech Recognition
      - WebOTX Text to Speech
2.  サービスインテグレーション
      - WebOTX Portal
      - WebOTX Enterprise Service Bus
      - WebOTX Process Conductor
      - WebOTX Service Repository
      - WebOTX OLF/TP Adapter
3.  アプリケーションサーバ
      - WebOTX Application Server
      - WebOTX Batch Server
      - WebOTX SIP Application Server
      - WebOTX Parallel Stream Monitor

## Application Server

[アプリケーションサーバ](https://ja.wikipedia.org/wiki/アプリケーションサーバ "wikilink")では、システムの形態、規模に対応して４つのEditionが存在する。

| Edition            | 規模 | 特徴                          |
| ------------------ | -- | --------------------------- |
| Web Edition        | 小  | Webサーバ、Webコンテナ、Webサービス      |
| Standard-J Edition | ↑  | EJBコンテナ、JMSサーバ、J2EE準拠       |
| Standard Edition   | ↓  | OLTPモニタ、C++・COBOLアプリケーション対応 |
| Enterprise Edition | 大  | クラスタ機能                      |
|                    |    |                             |

V8.1以前のEdition体系

| Edition            | 規模 | 特徴                                     |
| ------------------ | -- | -------------------------------------- |
| Express Edition    | 小  | Webサーバ、Webコンテナ、Webサービス、J2EEコンテナ、J2EE準拠 |
| Foundation Edition | ↑  | Standard Editionの機能制限版                 |
| Standard Edition   | ↓  | OLTPモニタ、C++・COBOLアプリケーション対応            |
| Enterprise Edition | 大  | クラスタ機能                                 |
|                    |    |                                        |

V8.2以降のEdition体系

運用管理ツールとして、コマンドラインベースとFlashを利用したブラウザベースのものが用意されている。 Webサーバは[Apacheを利用し](../Page/Apache_HTTP_Server.md "wikilink")、[Webコンテナ](../Page/Webコンテナ.md "wikilink")は[Tomcatを利用している](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink")。[EJBコンテナ等は独自に機能強化している](../Page/Enterprise_JavaBeans.md "wikilink")。

## Application Serverの歴史

| Ver | リリース日       | 特徴                                                               |
| --- | ----------- | ---------------------------------------------------------------- |
| 1   | 1998年       | WebcomputingアプリケーションサーバEnterprise版の構成要素としてリリース。CORBA実行基盤         |
| 2   | 1999年10月1日  | CORBA2.2完全準拠(POA：PortableObjectAdapter対応)。IIOP1.1対応。Java2動作サポート。 |
| 3   | 2000年11月1日  | CORBA2.3完全準拠。JSP開発・実行環境の提供。VISコネクタの提供。                           |
| 4   | 2001年11月28日 | SOAP1.1準拠、UDDI1.0準拠、モバイル対応                                       |
| 5   | 2002年11月27日 | 「CORBAプロバイダ」の提供,J2EE 1.3仕様に準拠,CORBA 2.6仕様への対応                    |
| 6   | 2004年8月26日  | 電子署名付加機能の提供、J2EE 1.4仕様に準拠                                        |
| 7   | 2007年7月2日   | 運用環境のVista対応。Linux対応。64ビットOSサポート。                                |
| 8   | 2008年6月24日  | JavaEE5対応、WindowsServer2008サポート                                  |
| 9   | 2013年5月30日  | JavaEE6対応、インメモリデータグリッドサポート、ライセンス体系変更                             |
| 10  | 2017年10月17日 | JavaEE7対応、Dockerサポート、複数バージョンインストール対応                             |
|     |             |                                                                  |

## SIP Application Server

WebOTX SIP Application Server は、V7.1で新たに追加された。拡張製品。 JSR116で規定されたSIP Server API1.0をサポートし、RFC3261で規定されたSIP(Session Initiation Protocol)実行環境を提供している。

## Enterprise Service Bus

WebOTX Enterprise Service Bus は WebOTX Application Server とは別個の製品であり、WebOTX Applicaton Server 上でのみ動作可能である。システム間の連携をSOAPなどで実現するためのハブシステム。 既存のACOS上で構築されているサービスを呼び出すためのアダプタが用意されている。 高信頼なマルチプロセス動作や、JBI 1.0に準拠していることを特徴とする。

## Batch Server

WebOTX Batch Serverは、Spring Batch の実行基盤で常駐JavaVMから起動される。WebSAM JobCenterと連携したジョブスケジュールが可能。

## 外部リンク

  - [WebOTX - NEC](http://www.nec.co.jp/WebOTX/)

## 関連項目

  - [Java Platform, Enterprise Edition](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")
  - [アプリケーションサーバ](https://ja.wikipedia.org/wiki/アプリケーションサーバ "wikilink")
  - [Java Servlet](../Page/Java_Servlet.md "wikilink")
  - [JavaServer Pages](../Page/JavaServer_Pages.md "wikilink")
  - [Session Initiation Protocol](https://ja.wikipedia.org/wiki/Session_Initiation_Protocol "wikilink")
  - [ESB](https://ja.wikipedia.org/wiki/ESB "wikilink")(Enterprise Service Bus)
  - [Spring Batch](https://ja.wikipedia.org/wiki/Spring_Batch "wikilink")

[Category:日本電気の製品](https://ja.wikipedia.org/wiki/Category:日本電気の製品 "wikilink")