> この記事は[Web Services Description Language](https://ja.wikipedia.org/wiki/Web_Services_Description_Language)から翻訳されています。


**Web Services Description Language** (WSDL ウィズダル) とは、[Webサービス](../Page/Webサービス.md "wikilink")記述言語の意で、[SOAPによるXML](../Page/SOAP_\(プロトコル\).md "wikilink") Webサービスの[インタフェースを記述する](../Page/インタフェース_\(情報技術\).md "wikilink")[インタフェース記述言語](../Page/インタフェース記述言語.md "wikilink")。通常その表現には[XMLを使う](../Page/Extensible_Markup_Language.md "wikilink")。WSDLは、サービスの呼出方法、それが期待するパラメータ群、それが返すデータ型について、機械可読な形式の記述を提供する。従って、その目的は[プログラミング言語](../Page/プログラミング言語.md "wikilink")における[メソッド](../Page/メソッド_\(計算機科学\).md "wikilink")・[シグネチャ](https://ja.wikipedia.org/wiki/シグネチャ "wikilink")の役割に似ている。

WSDLの現在のバージョンはWSDL 2.0である。省略語WSDLにおけるDの意味はバージョン1.1当時の「Definition」から変更されている。

**関連文書に多数の混乱があるため、まず、必ず[WS-IのBasic](../Page/Web_Services_Interoperability.md "wikilink") Profileの「5. Service Description」\[1\]を熟読すべきである。**

## 説明

[WSDL_11vs20.png](https://ja.wikipedia.org/wiki/File:WSDL_11vs20.png "fig:WSDL_11vs20.png")

WSDLはサービスをネットワーク上の「endpoint」または「port」の集合として記述する。この目的を果たす文書の仕様としてWSDL仕様は一つの[XML](../Page/Extensible_Markup_Language.md "wikilink")[フォーマットを提供する](../Page/ファイルフォーマット.md "wikilink")。「port」や「message」の抽象的な定義は、それらの具体的な仕様や実体とは分離されている。それにより、これらの定義の再利用も可能になっている。「port」とは、[ネットワークアドレス](https://ja.wikipedia.org/wiki/ネットワークアドレス "wikilink")を再利用可能な「binding」で対応づけることにより定義され、「port」の集団として「service」が定義される。「message」とは交換されるデータを抽象的に表現した言い方であり、「port type」とはサポートされている「operation」の抽象的な集団である。特定の「port type」のための具象的なプロトコルとデータ形式の仕様が再利用可能な「binding」を構成し、そこで「operation」と「message」が具象的な[ネットワークプロトコルとメッセージ形式に対応づけられる](../Page/通信プロトコル.md "wikilink")。このようにして、WSDLはWebサービスへの公開インタフェースを記述する。

WSDLはSOAPと[XMLスキーマと組み合わせて](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")、[インターネット](../Page/インターネット.md "wikilink")上にWebサービスを提供するために使われることが多い。Webサービスに接続するクライアント側のプログラムはWSDLファイルを読んで、そのサーバでどのような操作が可能なのかを知ることができる。利用される何らかの特殊な[データ型](../Page/データ型.md "wikilink")もWSDLファイル内にXMLスキーマの形で埋め込まれている。するとクライアントはSOAPを使ってWSDLファイル内に挙げられている操作の内の一つを実際に呼び出すことが出来る（例えばHTTP上でXMLを交換する)。

WSDL仕様の現在のバージョンは2.0である。; バージョン 1.1は [W3Cの推奨を受けていなかったが](../Page/World_Wide_Web_Consortium.md "wikilink")、バージョン2.0 は[W3C勧告](https://ja.wikipedia.org/wiki/W3C勧告 "wikilink")である\[2\]。 WSDL 1.2 が WSDL 2.0 に名称変更された。その理由はWSDL 1.1とは本質的に異なるからである。

（バージョン1.1当時のGETとPOSTだけでなく）全ての[HTTPリクエストメソッド](https://ja.wikipedia.org/wiki/Hypertext_Transfer_Protocol#メソッド "wikilink") を受け付けることで、WSDL 2.0仕様は[RESTfulなウェブサービスのよりよくサポートでき](../Page/Representational_State_Transfer.md "wikilink")、実装するのもより簡単になった\[3\]\[4\]。

### 用語

| WSDL 1.1用語 | WSDL 2.0用語 | 説明                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ---------- | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Service    | Service    | Webベースのプロトコルに公開されているシステム機能群の集合                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Port       | Endpoint   | Webサービスへのアドレスまたはコネクション・ポイントを定義したもの。単純なHTTPのURL文字列で表すのが一般的である。                                                                                                                                                                                                                                                                                                                                                                                        |
| Binding    | Binding    | インタフェースを指定し、SOAPの結合スタイル (binding style) ([RPC](../Page/遠隔手続き呼出し.md "wikilink")/Document) とトランスポート（SOAPプロトコル）を定義するもの。binding節はoperationも定義する。                                                                                                                                                                                                                                                                                                         |
| PortType   | Interface  | Webサービス、実行可能な操作や、その操作を実行するために使われるメッセージを定義したもの。                                                                                                                                                                                                                                                                                                                                                                                                       |
| Operation  | Operation  | SOAPアクション、およびメッセージのエンコード方法（例えば「literal」など）を定義したもの。operationは伝統的なプログラミング言語におけるメソッドや関数呼び出しのようなものである。                                                                                                                                                                                                                                                                                                                                                   |
| Message    | なし         | 典型的に、一つのmessageは一つのoperationと対応している。messageはoperationを実行するのに必要な情報を含む。各messageは一つ或いは複数の論理的部分により構成される。各部分はmessage-typing属性と対応している。message name属性は全messageの中での一意な名前を提供する。part name属性は、それを含むmessage内の各partの中での一意な名前を提供する。各partはmessageの論理的な構成要素を記述したものである。RPC bindingでは、bindingはpartに関するbinding固有の情報を指定するためにpartの名前を参照してよい。一つのpartはmessage内の一つのパラメータを表せる：bindingがpartの実際の意味を定義する。MessageはWSDL 2.0では廃止された。WSDL 2.0ではXMLスキーマ型で入出力本体を定義し、faultsは単純に直接参照される。 |
| Types      | Types      | データを記述したもの。XMLスキーマ言語（[XSDとしても知られる](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")）を使う。                                                                                                                                                                                                                                                                                                                                                         |

## WSDLファイル サンプル

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<definitions ns="http://www.w3.org/ns/wsdl"
             xmlns:tns="http://www.tmsws.com/wsdl20sample"
             xmlns:whttp="http://schemas.xmlsoap.org/wsdl/http/"
             xmlns:wsoap="http://schemas.xmlsoap.org/wsdl/soap/"
             targetNamespace="http://www.tmsws.com/wsdl20sample">

<!-- Abstract type -->
   <types>
      <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema"
                ns="http://www.tmsws.com/wsdl20sample"
                targetNamespace="http://www.example.com/wsdl20sample">

         <xs:element name="request"> ... </xs:element>
         <xs:element name="response"> ... </xs:element>
      </xs:schema>
   </types>

<!-- Abstract interfaces -->
   <interface name="Interface1">
      <fault name="Error1" element="tns:response"/>
      <operation name="Get" pattern="http://www.w3.org/ns/wsdl/in-out">
         <input messageLabel="In" element="tns:request"/>
         <output messageLabel="Out" element="tns:response"/>
      </operation>
   </interface>

<!-- Concrete Binding Over HTTP -->
   <binding name="HttpBinding" interface="tns:Interface1"
            type="http://www.w3.org/ns/wsdl/http">
      <operation ref="tns:Get" whttp:method="GET"/>
   </binding>

<!-- Concrete Binding with SOAP-->
   <binding name="SoapBinding" interface="tns:Interface1"
            type="http://www.w3.org/ns/wsdl/soap"
            wsoap:protocol="http://www.w3.org/2003/05/soap/bindings/HTTP/"
            wsoap:mepDefault="http://www.w3.org/2003/05/soap/mep/request-response">
      <operation ref="tns:Get" />
   </binding>

<!-- Web Service offering endpoints for both bindings-->
   <service name="Service1" interface="tns:Interface1">
      <endpoint name="HttpEndpoint"
                binding="tns:HttpBinding"
                address="http://www.example.com/rest/"/>
      <endpoint name="SoapEndpoint"
                binding="tns:SoapBinding"
                address="http://www.example.com/soap/"/>
   </service>
</definitions>
```

## 関連技術

  - [SOAP (プロトコル)](../Page/SOAP_\(プロトコル\).md "wikilink")
  - [Webサービス](../Page/Webサービス.md "wikilink")
  - [UDDI](https://ja.wikipedia.org/wiki/UDDI "wikilink")
  - [Extensible Markup Language](../Page/Extensible_Markup_Language.md "wikilink") (XML)
  - [Web Services Interoperability](../Page/Web_Services_Interoperability.md "wikilink") (WS-I)

## 外部リンク

<references/>

[Category:Webサービス](https://ja.wikipedia.org/wiki/Category:Webサービス "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.  [WS-I Basic Profile, 5. Service Description](http://www.ws-i.org/Profiles/Basic/2003-08/BasicProfile-1.0a-ja.html#description)
2.
3.
4.