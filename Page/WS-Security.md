> この記事は[WS-Security](https://ja.wikipedia.org/wiki/WS-Security)から翻訳されています。


**WS-Security**（*Web Services Security*、**WSS**）は、[Webサービス](https://ja.wikipedia.org/wiki/Webサービス "wikilink")にセキュリティを適用する手段を提供する[通信プロトコル](../Page/通信プロトコル.md "wikilink")。2004年4月19日、[OASISが](https://ja.wikipedia.org/wiki/OASIS_\(組織\) "wikilink") WS-Security 1.0 規格を公開した。2006年2月17日には 1.1 版がリリースされている。

[IBM](../Page/IBM.md "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")、[ベリサイン](https://ja.wikipedia.org/wiki/ベリサイン "wikilink")の開発したプロトコルに基づき、OASISが規格として標準化した。Webサービスメッセージングにおいて、どのように完全性と機密性を保持するかという仕様が含まれる。[SAMLと](https://ja.wikipedia.org/wiki/Security_Assertion_Markup_Language "wikilink")[ケルベロス認証](https://ja.wikipedia.org/wiki/ケルベロス認証 "wikilink")と[X.509](https://ja.wikipedia.org/wiki/X.509 "wikilink")などの認証フォーマットを使用している。

WS-Security は、[SOAPメッセージに署名を付与し](../Page/SOAP_\(プロトコル\).md "wikilink")、ヘッダを暗号化する方式を記述している。さらに、X.509 認証やケルベロス認証のようなバイナリセキュリティトークンをメッセージに付与する方式も記述されている。

WS-Security では、[アプリケーション層](https://ja.wikipedia.org/wiki/アプリケーション層 "wikilink")で動作するSOAPメッセージのヘッダにセキュリティ機能を導入している。つまり、エンドツーエンドのセキュリティを保証できる。

## 代替手法

ポイントツーポイントでは、Webサービスの[機密](https://ja.wikipedia.org/wiki/機密 "wikilink")と[データ完全性](../Page/データ完全性.md "wikilink")は [Transport Layer Security](../Page/Transport_Layer_Security.md "wikilink") (TLS) を使っても実現できる（[HTTPS](../Page/HTTPS.md "wikilink")など）。しかし、WS-Security はより広範囲な、いわゆるエンドツーエンドのセキュリティを提供する。

TLSを適用することで、鍵やメッセージ署名を送信前に[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")に符号化する必要がなくなり、オーバーヘッドが劇的に低減される。メッセージが[プロキシ](https://ja.wikipedia.org/wiki/プロキシ "wikilink")サーバを経由する場合、サーバはクライアントからではなくプロキシからの要求としてみるため、プロキシにクライアントの鍵と認証のコピーを与えて対応するか、そのサーバが信用する証明書を持つことで対応する。しかし、プロキシが関わっているためにエンドツーエンドのセキュリティとはならず、ポイントツーポイントのセキュリティとなる。

## 関連仕様

WS-Security に関連したドラフト仕様として、以下のものがある。

  - WS-SecureConversation
  - WS-Federation
  - WS-Authorization
  - [WS-Policy](https://ja.wikipedia.org/wiki/WS-Policy "wikilink")
  - WS-Trust
  - WS-Privacy
  - WS-Test

## 関連項目

  - [Webサービス](https://ja.wikipedia.org/wiki/Webサービス "wikilink")
  - [SAML](https://ja.wikipedia.org/wiki/Security_Assertion_Markup_Language "wikilink")
  - [X.509](https://ja.wikipedia.org/wiki/X.509 "wikilink")

## 外部リンク

  - [OASIS Web Services Security TC](http://www.oasis-open.org/committees/tc_home.php?wg_abbrev=wss) 規格文書のダウンロードリンクあり
  - [WS-Security Specification](http://www-128.ibm.com/developerworks/library/specification/ws-secure/)
  - [WS-I Basic Security Profile](http://www.ws-i.org/Profiles/BasicSecurityProfile-1.0.html)
  - [Web Services Security Documentation](http://www.cgisecurity.com/ws/)
  - [Web Service Security Patterns](http://msdn2.microsoft.com/en-us/library/aa480545.aspx)
  - [WSS4J](http://ws.apache.org/wss4j/) Apache による Java での WS-Security 実装
  - [Apache Rampart](http://ws.apache.org/rampart/) Apache Axis2 における Java での WS-Security 実装
  - [WSIT (Web Services Interoperability Technologies)](https://wsit.dev.java.net/) Javaプラットフォームと [Windows Communication Foundation](https://ja.wikipedia.org/wiki/Windows_Communication_Foundation "wikilink") (WCF) の間の相互運用を可能にする。

[Category:ウェブ技術](https://ja.wikipedia.org/wiki/Category:ウェブ技術 "wikilink") [Category:セキュリティソフト](https://ja.wikipedia.org/wiki/Category:セキュリティソフト "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink")