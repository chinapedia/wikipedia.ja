> この記事は[SOAP \(プロトコル\)](https://ja.wikipedia.org/wiki/SOAP_\(プロトコル\))から翻訳されています。


**SOAP**（ソープ）は、[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")内の[Webサービス](../Page/Webサービス.md "wikilink")の実装において、構造化された情報を交換するための[通信プロトコル](../Page/通信プロトコル.md "wikilink")の仕様である。[拡張性](../Page/拡張性.md "wikilink")、[中立性](https://ja.wikipedia.org/wiki/ネットワーク中立性 "wikilink")、独立性を導入することを目的とする。[XML-RPC](../Page/XML-RPC.md "wikilink")から発展した、**XML [Webサービス](../Page/Webサービス.md "wikilink")**のための、[XMLベースの](../Page/Extensible_Markup_Language.md "wikilink")[RPCプロトコルである](../Page/遠隔手続き呼出し.md "wikilink")。

メッセージ形式として[XMLインフォメーションセットを使用する](https://ja.wikipedia.org/wiki/Extensible_Markup_Language#XMLインフォメーションセット "wikilink")。また、メッセージのネゴシエーションおよび伝送は[アプリケーション層](../Page/アプリケーション層.md "wikilink")のプロトコル（多くの場合[HTTPまたは](../Page/Hypertext_Transfer_Protocol.md "wikilink")[SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")）に依存する。

SOAPにより、全く異なる[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")（例えば[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")と[Linux](../Page/Linux.md "wikilink")）上で走っているプロセス間でも[XMLを使って意思疎通が可能になる](../Page/Extensible_Markup_Language.md "wikilink")。HTTPのようなWebプロトコルは全てのオペレーティングシステムにインストールされて走っているので、SOAPの仕組みを使えば、クライアントはその言語やプラットフォームが何であれ、ウェブサービスを起動してレスポンスを受け取ることが出来る。

元はSimple Object Access Protocolの[頭字語](../Page/頭字語.md "wikilink")とされていたが、現在は「何かの[頭字語](../Page/頭字語.md "wikilink")ではない」とされている\[1\]。

## 概要

拡張可能で分散的な[フレームワーク](https://ja.wikipedia.org/wiki/フレームワーク "wikilink")であり、[HTTP以外にも様々な](../Page/Hypertext_Transfer_Protocol.md "wikilink")[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")の[通信プロトコル](../Page/通信プロトコル.md "wikilink")で利用することができると主張され、[SMTPへのバインディングも示されているが](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")、実際上TCP/IP上のHTTP(S)以外の使用は現実的ではない。主要な実装として[Apache Axisがある](../Page/Apache_Axis.md "wikilink")。多くの実装の間で相互運用性に問題があるとして[WS-Iというコンソーシアムが作られたが](../Page/Web_Services_Interoperability.md "wikilink")、現在は[OASISの一部となっている](../Page/OASIS_\(組織\).md "wikilink")。

いくつかのSOAPメッセージを相互作用させることによってリモートプロシージャコールが実現できる、Webサービスに有効な手段の一つである、などと主張されている。

メッセージの表現に[XMLを使用する](../Page/Extensible_Markup_Language.md "wikilink")。メッセージはヘッダとボディから成る。ヘッダはオプショナルであり、[ルーティング](../Page/ルーティング.md "wikilink")や[セキュリティ](../Page/コンピュータセキュリティ.md "wikilink")、そして [トランザクション](../Page/トランザクション.md "wikilink")などのための情報といった[メタ情報を格納する](../Page/メタデータ.md "wikilink")。ボディは、主要な情報すなわち[ペイロードである](https://ja.wikipedia.org/wiki/ペイロード_\(コンピュータ\) "wikilink")。

相互運用性のためには[XML Schemaなどで](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")、なんらかのスキーマを定義することが望ましいであろう。また、[WSDLという記述言語がある](../Page/Web_Services_Description_Language.md "wikilink")。

「WS-\*」と総称される関連プロトコルが 多量にある。

## 特徴

SOAP はウェブサービスのための「Web services protocol stack」における「Messaging Protocol」層を提供する。SOAPはXMLを基盤とするプロトコルで、三つの部分で構成される：

  - 「envelope」(小包)。これはメッセージ構造を定義する<ref>

</ref>。また、どのようにこれを処理すべきかを定義する：

  - アプリケーションで定義されるデータ型のインスタンスを表現するためのエンコーディング規則
  - プロシージャ呼出しとレスポンスを表すための約束事

SOAPには三つの大きな特徴がある:

1.  *拡張性* (セキュリティや[WS-Addressing](../Page/WS-Addressing.md "wikilink")などは開発中の拡張機能である)
2.  *中立性* (SOAPは[HTTP](https://ja.wikipedia.org/wiki/HTTP "wikilink"), [SMTP](https://ja.wikipedia.org/wiki/SMTP "wikilink"), [TCP](../Page/Transmission_Control_Protocol.md "wikilink"), [UDP](https://ja.wikipedia.org/wiki/SOAP-over-UDP "wikilink"),[JMSなどのいかなるプロトコル上でも運用できる](../Page/Java_Message_Service.md "wikilink"))
3.  *独立性* (SOAPはいかなる[プログラミングモデル](https://ja.wikipedia.org/wiki/プログラミングモデル "wikilink")でも使える)

SOAPで出来ることの一例を挙げると、たとえば或るアプリケーションが、ウェブサービス（例えば不動産価格データベース）を利用可能なサーバに、検索条件パラメータを入れたSOAPリクエストを送ったとする。すると、そのサーバーはSOAPレスポンス（価格、場所、特徴などの検索結果データを書き込んだXML形式文書）を返してくる。返ってきたデータは標準化された機械処理可能な書式で来るので、それを受け取ったアプリケーションはそのデータを直接処理できる。

SOAPアーキテクチャには、次の幾つかのレイヤーのための仕様がある:

  - メッセージ形式
  - メッセージ交換パターン(Message Exchange Pattern : MEP)
  - 下層のトランスポートプロトコルとの結合
  - メッセージ処理モデル
  - プロトコル拡張性

## 仕様

[SOAP.svg](https://ja.wikipedia.org/wiki/File:SOAP.svg "fig:SOAP.svg")

SOAP仕様はメッセージングの枠組みを定義したもので、次の各部で構成される：

  - *[**SOAP processing model**](https://www.w3.org/TR/soap12-part1/#msgexchngmdl)* ：SOAPメッセージを処理するための規約を定義する
  - *[**SOAP extensibility model**](https://www.w3.org/TR/soap12-part1/#extensibility)* ：SOAP機能とSOAPモジュールの概念を定義する
  - *[**SOAP underlying protocol binding**](https://www.w3.org/TR/soap12-part1/#transpbindframew)* ：SOAPノード間でSOAPメッセージを交換するために用いる下層プロトコルへの結合を定義するための規約を示したフレームワーク。
  - ***[SOAP message construct](https://www.w3.org/TR/soap12-part1/#soapenv)*** ：SOAPメッセージの構造を定義する

## SOAPメッセージの例

一例として、あるクライアントが、ショッピングサイト（例示のための架空のものである）のサービスに商品IDを提示して商品の詳細を求めるリクエストメッセージはおおよそ以下のようになる。

``` xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
   <SOAP-ENV:Body>
     <getProductDetails ns="http://warehouse.example.com/ws">
       <productId>827635</productId>
     </getProductDetails>
   </SOAP-ENV:Body>
 </SOAP-ENV:Envelope>
```

これに対し、ショッピングサイトのサービス側の、要求に基づく商品データを含むレスポンスメッセージはおおよそ以下のようになる。

``` xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
   <SOAP-ENV:Body>
     <getProductDetailsResponse ns="http://warehouse.example.com/ws">
       <getProductDetailsResult>
         <productName>Toptimate 3-Piece Set</productName>
         <productId>827635</productId>
         <description>3-Piece luggage set.  Black Polyester.</description>
         <price>100.50</price>
         <inStock>true</inStock>
       </getProductDetailsResult>
     </getProductDetailsResponse>
   </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

## 関連項目

[SOAP.svg](https://ja.wikipedia.org/wiki/File:SOAP.svg "fig:SOAP.svg")

  - [WDDX](../Page/WDDX.md "wikilink")
  - [WS-Addressing](../Page/WS-Addressing.md "wikilink")

## 外部リンク

  - [SOAP Version 1.2](http://www.w3.org/TR/soap12-part0/) (W3C)

## 脚注

[Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:データシリアライゼーションフォーマット](https://ja.wikipedia.org/wiki/Category:データシリアライゼーションフォーマット "wikilink") [Category:遠隔手続き呼出し](https://ja.wikipedia.org/wiki/Category:遠隔手続き呼出し "wikilink")

1.  「In previous versions of this specification the SOAP name was an acronym. This is no longer the case.」（[SOAP Version 1.2 Part 1 : Messaging Framework (Second Edition)](http://www.w3.org/TR/soap12-part1/)より引用）。