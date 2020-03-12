> この記事は[EbXML Message Service](https://ja.wikipedia.org/wiki/EbXML_Message_Service)から翻訳されています。


**ebXML Message Service** (**ebMS**) は、[ebXML](https://ja.wikipedia.org/wiki/ebXML "wikilink")の仕様のひとつで、企業間[電子商取引](../Page/電子商取引.md "wikilink")でやりとりするメッセージをインターネットを通じて伝送するための仕様である。[OASIS](../Page/OASIS_\(組織\).md "wikilink") ebXML Messaging Services技術委員会で仕様策定が行われている。

ebMSは[SOAPをベースとしており](../Page/SOAP_\(プロトコル\).md "wikilink")、企業間電子商取引に求められる安全性や信頼性をインターネット上で確保するための機構を追加している。とりわけ特徴的なのは、メッセージが確実に通信相手に届いたかどうかを保証する**信頼性通信** (reliable messaging) である。受領通知、リトライ、重複除去といった仕組みを組み合わせて信頼性を実現する仕様を定めている。この機構は[Webサービス](../Page/Webサービス.md "wikilink")で同様の信頼性を実現する仕様[WS-Reliability](https://ja.wikipedia.org/wiki/WS-Reliability "wikilink")の元になった。

ebMSバージョン2.0 (2002年) はOASIS標準として承認されたのち、[ISOに提出されてISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")/TS 15000-2として承認された。

2007年にOASIS標準となったebMSバージョン3.0では、クライアント・サーバ型の通信を実現するプル型メッセージングを新たに盛り込んだ。これにより、自社にサーバを設置できない中小企業などへの導入が容易になると期待されている。そのほか、Webサービス仕様との整合性を高めており、これまでebMSが独自に定めていた機構をWS-\*仕様群の組合せによって実現するよう改められている。

## 相互運用性テスト

ebMSについては、異なるベンダの製品間での相互運用性テストが世界各地で行われている。企業組織の枠を越えて確実なメッセージ交換を行わなければならない企業間電子商取引の性質上、このようなテストが求められたといえよう。以下のテストに用いられたebMSのバージョンはいずれも2.0である。

  - 北米: Drummond Group Inc.が実施 ([プレスリリース](http://www.drummondgroup.com/html-v2/pr_10-01-02.html))
  - 日本: ECOMが実施 ([プレスリリース](http://www.ecom.jp/pressrelease/20020930_semi.html))
  - アジア: ebXMLアジア委員会が実施 ([プレスリリース](http://www.ecom.jp/pressrelease/20040603/20040603.html))
  - 欧州: CEN, ISSS, eBESが実施

## 外部リンク

  - [OASIS ebXML Messaging Services TC](http://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ebxml-msg)
  - [ebXML Message Service Specification Version 2.0](http://www.ebxml.org/specs/ebMS2.pdf)
  - [ebXML Message Service 3.0仕様](http://www.oasis-open.org/specs/index.php#ebxmlmsgv3)

[en:EbXML Messaging Services](https://ja.wikipedia.org/wiki/en:EbXML_Messaging_Services "wikilink")

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink")