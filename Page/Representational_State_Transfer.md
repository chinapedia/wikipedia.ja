> この記事は[Representational State Transfer](https://ja.wikipedia.org/wiki/Representational_State_Transfer)から翻訳されています。


**Representational State Transfer** (**REST**) は、APIの定義に使用されるアーキテクチャスタイル\[1\]であり、同時に[ウェブのような分散](../Page/World_Wide_Web.md "wikilink")[ハイパーメディア](https://ja.wikipedia.org/wiki/ハイパーメディア "wikilink")システムのための[ソフトウェアアーキテクチャ](../Page/ソフトウェアアーキテクチャ.md "wikilink")のスタイルのひとつでもある。この語は[HTTPプロトコル規格の主要著者の一人である](../Page/Hypertext_Transfer_Protocol.md "wikilink")がウェブについて書いた2000年の博士論文で初めて現れ、ネットワーキングコミュニティの中ですぐに広く使われることになった。

RESTは、初めは[アーキテクチャの原則と制約の集まり](../Page/コンピュータ・アーキテクチャ.md "wikilink")（後述）を指していたが、次第に、[XMLやHTTPを使った簡易なウェブベースの](../Page/Extensible_Markup_Language.md "wikilink")[インタフェースのうち](../Page/インタフェース_\(情報技術\).md "wikilink")、[Webサービス](../Page/Webサービス.md "wikilink")の[SOAP](../Page/SOAP_\(プロトコル\).md "wikilink")[プロトコルのようなMEP](../Page/通信プロトコル.md "wikilink")（*Message Exchange Pattern*; SOAPノード相互のメッセージ交換のパターンを確立するための雛型）ベースの特別な抽象化をしないもののことを、大まかに意味する用語として使われるようになった。RESTは次に述べるように2つのやや異なる意味で使われている。

  - フィールディングのRESTアーキテクチャスタイルの原則に合わせたWebサービスシステム 。
  - [遠隔手続き呼出し](../Page/遠隔手続き呼出し.md "wikilink") (RPC) スタイルに合わせた簡易なXML + HTTPインタフェースを採用したシステム（SOAPは使わない） 。

RESTはこのように2つのやや異なる意味で使われているため、技術的な議論の中で混乱を引き起こすことがある。 ただし、RPCはRESTの実例とはいえない。

フィールディングのREST原則に従うシステムは、しばしば*RESTful*といわれる。RESTをとても熱心に支持する人々は自らのことを*RESTafarians*と呼ぶ。ちなみに、この呼称は「[ラスタファリアン](../Page/ラスタファリ運動.md "wikilink")」（）のもじりである。

## 原則

RESTを支持する人々は、ウェブの[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")と成長は、次に述べるような、いくつかのキーとなる設計原則の結果であると論じる。

  - ステートレスなクライアント/サーバプロトコル
    HTTPメッセージの一つ一つが、そのリクエスト（メッセージ）を理解するために必要な全ての情報を含む。そのため、[クライアントも](../Page/クライアント_\(コンピュータ\).md "wikilink")[サーバ](../Page/サーバ.md "wikilink")も、メッセージ間におけるセッションの状態を記憶しておく必要がない。ただし実際には、多くのHTTPベースの[アプリケーションは](../Page/アプリケーションソフトウェア.md "wikilink")[クッキーやその他の仕掛けを使ってセッションの状態を管理している](../Page/HTTP_cookie.md "wikilink")（URLリライティングのような一部のセッション管理手法を使うシステムは、RESTfulではない）。
  - すべての情報（リソース）に適用できる「よく定義された操作」のセット
    HTTP では操作（メソッド）の小さなセットが定義されている。最も重要なのは "GET"、"POST"、"PUT"、"DELETE" である。これらはデータ[永続化](https://ja.wikipedia.org/wiki/永続化 "wikilink")に要求される[CRUD](../Page/CRUD.md "wikilink")と比較されることがある。もっとも "POST" に関してはCRUDにはぴったり対応していない。
  - [リソースを一意に識別する](https://ja.wikipedia.org/wiki/リソース_\(WWW\) "wikilink")「汎用的な構文」
    RESTfulなシステムでは、すべてのリソースは[Uniform Resource Identifier](../Page/Uniform_Resource_Identifier.md "wikilink") (URI) で表される一意的な（ユニークな）アドレスを持つ。
  - アプリケーションの情報と状態遷移の両方を扱うことができる「ハイパーメディアの使用」
    RESTシステムでは、多くの場合、[HTML文書またはXML文書を使う](../Page/HyperText_Markup_Language.md "wikilink")。こうした文書に情報およびその他のリソースへのリンクを含める。こうすることにより、あるRESTリソースから他のRESTリソースを参照したい場合は単にリンクを辿るだけでよい。レジストリなどの他の基盤的な機能を使う必要はない。

## リソース

REST において重要な概念は、「[リソース](https://ja.wikipedia.org/wiki/リソース_\(WWW\) "wikilink")」(情報の断片) である。個々のリソースは、グローバルな識別子 ([URI](../Page/Uniform_Resource_Identifier.md "wikilink")) により参照することができる。リソースに対する操作は次のようにして行われる。

  - ネットワークの「コンポーネント」(クライアントやサーバ) が、標準化されたインタフェース ([HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")) により通信する。
  - ネットワークを介してリソースの「表現」（）を交換する（実際にはファイルがアップロード・ダウンロードされる）。

しかし実際のところこうしたリソース操作は議論の対象となっている。一部の人々には「リソース」と「表現」とを区別することは観念的すぎるとの意見がある。ただし [RDFコミュニティでは](../Page/Resource_Description_Framework.md "wikilink")、リソースと表現の区別は、一般的に行われている。

さまざまな「コネクタ」（クライアント、サーバ、[キャッシュ](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")、[トンネル](../Page/トンネリング.md "wikilink") など）がリクエストを仲介することができる。ただしコネクタは過去のリクエストを参照せずに仲介することができなければならない。

  -
    これは REST の原則を構成する「レイヤリング」と呼ばれる制約である。レイヤリングは、情報アーキテクチャやネットワークアーキテクチャの他の多くの部分にも見られる一般的な設計原則でもある。

こうすることで、RESTアプリケーションは、次の2つの情報を認識することで、リソースを扱うことが可能である。

  - リソース識別子
  - 要求されたリクエスト

アプリケーションと実際の情報を持つサーバとの間にある他のものについて意識する必要はない。つまりアプリケーションは、[キャッシュや](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")[プロキシ](../Page/プロキシ.md "wikilink")、[ゲートウェイ](../Page/ゲートウェイ.md "wikilink")、[ファイアウォール](../Page/ファイアウォール.md "wikilink")、[トンネルなどの有無を意識する必要は無い](../Page/トンネリング.md "wikilink")。

ただしアプリケーションは、返された情報（表現）のフォーマットを理解できる必要がある。そのフォーマットは、多くの場合は何らかのHTMLかXMLの文書であるが、場合によっては画像やその他のコンテンツであることもある。

## REST対RPC

RESTな[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")は、[遠隔手続き呼出し](../Page/遠隔手続き呼出し.md "wikilink") (RPC) アプリケーションとは異なる設計面のアプローチを必要とする。RPCでは、プロトコル操作（動詞）の多様性を重視する。RPCアプリケーションが定義する操作の例を次に示す。

`getUser()`
`addUser()`
`removeUser()`
`updateUser()`
`getLocation()`
`addLocation()`
`removeLocation()`
`updateLocation()`
`listUsers()`
`listLocations()`
`findLocation()`
`findUser()`

一方RESTでは、リソース（名詞）の多様性を重視する。RESTアプリケーションが定義するリソースの型の例を次に示す。

` User {}`
` Location {}`

それぞれのリソースは、`http://www.example.org/locations/us/ny/new_york_city` のような固有の[URIを持つ](../Page/Uniform_Resource_Identifier.md "wikilink")。このリソースを扱うクライアントは標準の[HTTPメソッドを使う](../Page/Hypertext_Transfer_Protocol.md "wikilink")。例えば、

  - HTTP GETを使ってリソースのコピーをダウンロードする。
  - 更新したコピーをHTTP PUTによりアップロードする。
  - HTTP DELETEによりそのリソースの全ての表現を削除する。

なお、それぞれのリソースが固有のURIを持っているので、キャッシュ、コピー、ブックマークすることが簡単にできることに注意してほしい。HTTP POSTは一般に副作用のあるアクションに対して使われる。たとえば購入の注文を行ったり、コレクションに情報を追加したりするために使われる。

一例として、次のような[XML形式のユーザーのデータを扱うことを考える](../Page/Extensible_Markup_Language.md "wikilink")。

``` xml
<user>
 <name>Jane User</name>
 <gender>female</gender>
 <location href="http://www.example.org/locations/us/ny/new_york_city">
  New York City, NY, US
 </location>
</user>
```

ユーザーのlocation（住所）を更新するためには、RESTクライアントはまず上記のXMLデータをHTTP GETによりダウンロードする。それからXMLデータのlocationを変更して、HTTP PUTによりアップロードする。

HTTPのメソッドが、リソースを発見するための標準的なメソッドをすべて提供してはいないことに注意してほしい。

  -
    RPCの上記の例における `list*()` や `find*()` に相当する、HTTP LISTやFINDのようなメソッドはHTTPでは規定していない。

RESTは、その代わりに、扱う対象とするコレクションや検索結果の集合を、別の型の「リソース」として扱うことで問題に対処する。アプリケーション設計者は、リソースの検索や一覧取得のために状況に応じてそのURIやURIパターンを知っておく必要がある。

いくつかの例を示す。

  - `http://www.example.org/locations/us/ny/`というURIへのHTTP GETリクエストは、ニューヨーク各地の情報をもつXMLファイルへのリンクの一覧を返す。
  - `http://www.example.org/users?surname=Michaels`というURIへのHTTP GETリクエストは、"Michaels" の姓をもつ全てのユーザーへのリンクの一覧を返す。

RESTは、このようなアクションをどのように行うかについてのいくつかの手がかりを提供する。この手がかりは、RESTの原則を構成する制約の一つ「アプリケーション状態のエンジンとしてのハイパーメディア」から得られる。この制約から導かれる実現手段の一つは、パラメタつきのリクエストに対しては、フォーム言語（HTMLフォームなど）を使うことである。

[A9.com](https://ja.wikipedia.org/wiki/A9.com "wikilink")の[OpenSearch](../Page/OpenSearch.md "wikilink")イニシアチブは、RESTを使った検索の標準化作業を行っている。具体的には、[RDF](../Page/Resource_Description_Framework.md "wikilink")、[XTM](https://ja.wikipedia.org/wiki/Topic_Map "wikilink")、[Atom](../Page/Atom_\(ウェブコンテンツ配信\).md "wikilink")、[RSS](../Page/RSS.md "wikilink")（方言を含む）、リンクを扱うための[XLink](../Page/XLink.md "wikilink")と組み合わせた簡単な構造のXML ([Plain Old XML](https://ja.wikipedia.org/wiki/Plain_Old_XML "wikilink"); POX) を含む一般的なフォーマットをRESTシステムで使うことにより、情報を発見するための規格の策定である。

## 公開されている実装

RESTはかなり広い意味で定義されているので、広義に捉えると非常に多くの数のRESTfulアプリケーション（HTTP GETリクエストによりアクセス可能なすべてのもの）がウェブ上に存在すると考えることができる。RESTを、一般的な[Webサービス](../Page/Webサービス.md "wikilink")やRPCスタイルとは異なるものとして狭義に捉えても、RESTは公開されたウェブ上の随所に見つけることができる。

  - [ブロゴスフィア](../Page/ブロゴスフィア.md "wikilink")――[ウェブログの世界](../Page/ブログ.md "wikilink")――の大部分はRESTベースである。ブログでは、他のリソースへのリンクの一覧を含む[XMLファイルを](../Page/Extensible_Markup_Language.md "wikilink")（[RSS](../Page/RSS.md "wikilink") 2.0、RSS 1.0、[Atomフォーマットで](../Page/Atom_\(ウェブコンテンツ配信\).md "wikilink")）ダウンロードする。
  - [Amazon.com](../Page/Amazon.com.md "wikilink")は[デベロッパーインターフェイス](http://www.amazon.com/gp/aws/landing.html)を、RESTバージョンと[SOAPバージョンの両方で提供している](../Page/SOAP_\(プロトコル\).md "wikilink")（RESTバージョンがトラフィックの大部分を占めている）。
  - [eBay](https://ja.wikipedia.org/wiki/eBay "wikilink")はREST[デベロッパーインターフェイス](http://developer.ebay.com/rest/)を提供している。
  - [カナダ](https://ja.wikipedia.org/wiki/カナダ "wikilink")政府の["Seniors Canad On-line"](http://www.seniors.gc.ca/index.jsp) プロジェクトはRESTインターフェイスを提供している（[説明](http://www.megginson.com/blogs/quoderat/archives/2005/03/09/public-rest-application-seniors-canada-online/)）。
  - BloglinesはREST[デベロッパーインターフェイス](http://bloglines.com/services/)を提供している。
  - [Yahoo\!](../Page/Yahoo!.md "wikilink")はREST [デベロッパーインターフェイス](http://developer.yahoo.com)を提供している。
  - OpenomyはRESTベースのオンラインファイルストレージシステムである。
  - [Ruby on RailsにおけるURLルーティングでは](../Page/Ruby_on_Rails.md "wikilink")、[MVC](../Page/Model_View_Controller.md "wikilink")[デザインパターンを使うことにより](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")、RESTfulアプリケーション設計を支援する。
  - [Zope](../Page/Zope.md "wikilink")のオブジェクト出版システム。
  - [ASP.NET](../Page/ASP.NET.md "wikilink")における[ASP.NET WebAPIは](https://ja.wikipedia.org/wiki/ASP.NET_WevAPI "wikilink")、RESTfulなAPIを、通常のRPCメソッド実装とほぼ同様の簡便さで記述する事を可能とする。また、[ASP.NET MVC Frameworkを使用して](https://ja.wikipedia.org/wiki/ASP.NET_MVC_Framework "wikilink")、従来のMVC構造を使用した実装もサポートする。

同様のものが他にも多く提供されているとみられる。

なお、上記の多くのものは完全にRESTfulというわけではない。つまり、それらは REST の全てのアーキテクチャの制約に従っているわけではない。とはいえ、どれもRESTから刺激を受けたものであり、RESTのほとんどのアーキテクチャの制約の重要性を認識している。特に統一的なインタフェースの制約についてはそうである。これらのサービスは[「偶然によるRESTful](http://www.markbaker.ca/2002/09/Blog/2005/04/14#2005-04-amazon-next)」と呼ばれることがある。

## 関連項目

  - [Plain Old XML](https://ja.wikipedia.org/wiki/Plain_Old_XML "wikilink")

<!-- end list -->

  - [Webサービス](../Page/Webサービス.md "wikilink")

<!-- end list -->

  - [Ruby on Rails](../Page/Ruby_on_Rails.md "wikilink")
  - [Atom (ウェブコンテンツ配信)\#Atom Publishing Protocol](https://ja.wikipedia.org/wiki/Atom_\(ウェブコンテンツ配信\)#Atom_Publishing_Protocol "wikilink") - RESTに準拠したアプリケーションプロトコル

## 脚注

## 外部リンク

  - [Architectural Styles and the Design of Network-based Software Architectures, Chapter 5](http://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm) - フィールディング が REST の考え方を最初に述べた論文
  - [RESTwiki](http://rest.blueoxen.net/cgi-bin/wiki.pl?FrontPage)
      - [RESTwiki: a short summary of REST](http://rest.blueoxen.net/cgi-bin/wiki.pl?ShortSummaryOfRest)
  - [rest-discuss Yahoo\! Group](http://groups.yahoo.com/group/rest-discuss/)
  - [Paul Prescod's REST Resources](http://www.prescod.net/rest/)
  - ["What is SOA and REST Web services ..."](http://webservices.xml.com/pub/a/ws/2003/09/30/soa.html)
  - [A9's Open Search](http://opensearch.a9.com/)
  - [Constructing or Traversing URIs?](http://www.xml.com/pub/a/2005/04/06/restful.html) - 「アプリケーション状態のエンジンとしてのハイパーメディア」の制約の意味を論じる記事
  - [Building Web Services the REST Way](http://www.xfront.com/REST-Web-Services.html)
  - [How I explained REST to my wife...](http://naeblis.cx/rtomayko/2004/12/12/rest-to-my-wife)

[Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink") [Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:World_Wide_Web](https://ja.wikipedia.org/wiki/Category:World_Wide_Web "wikilink") [Category:ソフトウェアアーキテクチャ](https://ja.wikipedia.org/wiki/Category:ソフトウェアアーキテクチャ "wikilink")

1.  ウィリアム・スターリングス『Foundations of Modern Networking: SDN, NFV, QoE, IoT, and Cloud』Addison-Wesley Professional、2015年 ISBN 0134175395