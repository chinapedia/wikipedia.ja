> この記事は[WS-Addressing](https://ja.wikipedia.org/wiki/WS-Addressing)から翻訳されています。


**WS-Addressing**（*Web Services Addressing*）は、[Webサービス](https://ja.wikipedia.org/wiki/Webサービス "wikilink")がアドレス指定情報をやりとりするための転送手段から独立した機構の仕様である。基本的に、Webサービスのエンドポイントへの参照をやりとりする構造と、特定のメッセージとアドレス指定情報を関連付けるメッセージアドレス指定情報群という2つの部分から構成される。

## 概要

[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")/[HTTPS](../Page/HTTPS.md "wikilink")上で転送される[SOAPメッセージは](../Page/SOAP_\(プロトコル\).md "wikilink")、正しいマシンに到達するためにHTTP/[TCP/IPに依存しており](../Page/インターネット・プロトコル・スイート.md "wikilink")、メッセージ外の情報を使うことで（すなわち、SoapAction HTTP ヘッダ）目的のマシンにメッセージが到達したことが分かるようになっている。このメッセージ外情報はHTTP特有のものである。したがって、HTTPに依存しないようにするには、そのメッセージ外情報をどうするかを考えなければならない。

WS-Addressing は、そのHTTP固有データを[XMLメッセージ自体に埋め込む標準化された方法である](../Page/Extensible_Markup_Language.md "wikilink")。下位層のプロトコルに依存することなくディスパッチ情報を転送可能にするため、標準SOAPヘッダにディスパッチメタデータを格納する。下位層プロトコルはそのメタデータを解読できるディスパッチャーにそのメッセージを送ればよい。メッセージがディスパッチャーに到達した時点で、ネットワークレベルの転送処理は完了する。

WS-Addressing は、応答を送るべき相手を示すエンドポイント・リファレンス (EPR) を含むSOAPヘッダ (wsa:ReplyTo) を指定することで、（HTTPから見れば）非同期なやり取りを実現する。応答を返すサービスプロバイダは、wsa:ReplyTo エンドポイントへの分離したコネクション上でその応答メッセージを転送する。これにより、SOAP要求/応答の持続時間とHTTP要求/応答の持続時間は切り離され、任意の時間だけ持続するやり取りが可能になる。特別な[URL](../Page/Uniform_Resource_Locator.md "wikilink") "<http://www.w3.org/2005/08/addressing/anonymous>" を使い、サービスプロバイダが "protocol specific back-channel"（SOAP/HTTP の場合、HTTP応答メッセージ）を応答の送信に使うべきであることを示す。

## エンドポイント・リファレンス

エンドポイント・リファレンス（Endpoint Reference、EPR）は、メッセージをWebサービスにアドレス指定する際に使える情報をカプセル化した[XML構造である](../Page/Extensible_Markup_Language.md "wikilink")。これには、メッセージの送信先アドレス、メッセージの転送経路指定に必要な任意の追加パラメータ（リファレンス・パラメータ）、オプションのサービスに関するメタデータ（[WSDLや](https://ja.wikipedia.org/wiki/Web_Services_Description_Language "wikilink")[WS-Policy](https://ja.wikipedia.org/wiki/WS-Policy "wikilink")など）が含まれる。

## メッセージアドレス指定情報

メッセージアドレス指定属性は、Webサービスにメッセージを伝達することに関連する以下のようなアドレス指定情報をやり取りする。

  - メッセージ送付先 [URI](../Page/Uniform_Resource_Identifier.md "wikilink")
  - ソース・エンドポイント - このメッセージをディスパッチしたサービスのエンドポイント (EPR)
  - リプライ・エンドポイント - 応答メッセージをディスパッチすべきエンドポイント (EPR)
  - フォールト・エンドポイント - フォールトメッセージをディスパッチすべきエンドポイント (EPR)
  - アクション - メッセージの意味を示す（メッセージの経路指定の補助となる）アクション値 [URI](../Page/Uniform_Resource_Identifier.md "wikilink")
  - ユニークなメッセージID [URI](../Page/Uniform_Resource_Identifier.md "wikilink")
  - 前のメッセージとの関係（2つの[URI](../Page/Uniform_Resource_Identifier.md "wikilink")）

## 歴史

WS-Addressing は当初、[マイクロソフト](../Page/マイクロソフト.md "wikilink")、[IBM](../Page/IBM.md "wikilink")、[BEA](../Page/BEAシステムズ.md "wikilink")、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")、[SAP](https://ja.wikipedia.org/wiki/SAP_AG "wikilink") が開発したもので、その後[W3Cでの標準化のために](../Page/World_Wide_Web_Consortium.md "wikilink")[提出された](http://www.w3.org/Submission/2004/SUBM-ws-addressing-20040810/)。W3C [WS-Addressing Working Group](http://www.w3.org/2002/ws/addr/) は、その標準化の過程で改良と拡張を行った。

WS-Addressing は現在以下の3部構成になっている。

  - エンドポイント・リファレンスとメッセージアドレス指定属性についての[中核](http://www.w3.org/TR/ws-addr-core)仕様
  - それら属性の[SOAPでの](../Page/SOAP_\(プロトコル\).md "wikilink")[バインディング](http://www.w3.org/TR/ws-addr-soap)

[メタデータ](http://www.w3.org/TR/2007/REC-ws-addr-metadata-20070904/)仕様。中核仕様で定義されている抽象属性の[WSDLを使った表現法](https://ja.wikipedia.org/wiki/Web_Services_Description_Language "wikilink")、WSDLメタデータをエンドポイント・リファレンスに含める方法、WebサービスがWS-Addressingをサポートしていることを[WS-Policy](https://ja.wikipedia.org/wiki/WS-Policy "wikilink")を使って示す方法。

[Web Services Policy Attachment for Endpoint Reference (WS-PAEPR)](http://www.w3.org/Submission/WS-PAEPR/) では、エンドポイント・リファレンスに[WS-Policy](https://ja.wikipedia.org/wiki/WS-Policy "wikilink")を含める機構と意味を解説している。WS-PAPER は W3C Member Submission （W3C会員が提出した技術文書）である。

## 外部リンク

  - [Web Services Addressing Working Group](http://www.w3.org/2002/ws/addr/)
  - [WS-Addressing - specification(IBM)](http://www-128.ibm.com/developerworks/library/specification/ws-add/)
  - [WS-Addressing - Submission Request to W3C](http://www.w3.org/Submission/2004/05/)
  - [Team Comment on the WS-Addressing Submission](http://www.w3.org/Submission/2004/05/Comment)

[Category:ウェブ技術](https://ja.wikipedia.org/wiki/Category:ウェブ技術 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink")