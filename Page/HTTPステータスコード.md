> この記事は[HTTPステータスコード](https://ja.wikipedia.org/wiki/HTTPステータスコード)から翻訳されています。


**HTTPステータスコード**は、[HTTPにおいて](../Page/Hypertext_Transfer_Protocol.md "wikilink")[Webサーバ](../Page/Webサーバ.md "wikilink")からのレスポンスの意味を表現する3桁の数字からなるコードである。等によって定義され、[IANAがHTTP](../Page/Internet_Assigned_Numbers_Authority.md "wikilink") Status Code Registryとして管理している。以下に一覧を示す。

## 1xx Informational 情報

リクエストは受け取られた。処理は継続される。

  - 100 Continue
    **継続**。クライアントはリクエストを継続できる。サーバがリクエストの最初の部分を受け取り、まだ拒否していないことを示す。
    例として、クライアントがExpect: 100-continueヘッダをつけたリクエストを行い、それをサーバが受理した場合に返される。
  - 101 Switching Protocols
    **プロトコル切替**。サーバはリクエストを理解し、遂行のためにプロトコルの切り替えを要求している。
  - 102 Processing
    **処理中**。[WebDAV](../Page/WebDAV.md "wikilink")の拡張ステータスコード。処理が継続されて行われていることを示す。
  - 103 Early Hints (RFC 8297)
    **早期のヒント**。最終的なレスポンスヘッダが確定する前に、予想されるヘッダを伝達する。Linkレスポンスヘッダと組み合わせて、関連するリソースの先読み・プッシュ配信に利用することが想定されている。

## 2xx Success 成功

リクエストは受け取られ、理解され、受理された。

  - 200 OK
    **OK**。リクエストは成功し、レスポンスとともに要求に応じた情報が返される。
    [ブラウザ](https://ja.wikipedia.org/wiki/ブラウザ "wikilink")でページが正しく表示された場合は、ほとんどがこのステータスコードを返している。
  - 201 Created
    **作成**。リクエストは完了し、新たに作成されたリソースのURIが返される。
    例: PUTメソッドでリソースを作成するリクエストを行ったとき、そのリクエストが完了した場合に返される。
  - 202 Accepted
    **受理**。リクエストは受理されたが、処理は完了していない。
    例: PUTメソッドでリソースを作成するリクエストを行ったとき、サーバがリクエストを受理したものの、リソースの作成が完了していない場合に返される。[バッチ処理](../Page/バッチ処理.md "wikilink")向け。
  - 203 Non-Authoritative Information
    **信頼できない情報**。オリジナルのデータではなく、ローカルやプロキシ等からの情報であることを示す。
  - 204 No Content
    **内容なし**。リクエストを受理したが、返すべきレスポンスエンティティが存在しない場合に返される。
    例: POSTメソッドで[フォームの内容を送信したが](../Page/フォーム_\(ウェブ\).md "wikilink")、ウェブブラウザの画面を更新しない場合に返される。
  - 205 Reset Content
    **内容のリセット**。リクエストを受理し、[ユーザエージェント](https://ja.wikipedia.org/wiki/ユーザエージェント "wikilink")の画面をリセットする場合に返される。
    例: POSTメソッドでフォームの内容を送信した後、ウェブブラウザの画面を初期状態に戻す場合に返される。
  - 206 Partial Content
    **部分的内容**。部分的GETリクエストを受理したときに、返される。
    例: ダウンロードツール等で分割ダウンロードを行った場合や、レジュームを行った場合に返される。
  - 207 Multi-Status
    **複数のステータス**。WebDAVの拡張ステータスコード。
  - 208 Already Reported
    **既に報告**。WebDAVの拡張ステータスコード。
  - 226 IM Used
    **IM使用**。[Delta encoding in HTTPの拡張ステータスコード](https://ja.wikipedia.org/wiki/Delta_encoding_in_HTTP "wikilink")。

## 3xx Redirection リダイレクション

リクエストを完了させるために、追加的な処理が必要。

  - 300 Multiple Choices
    **複数の選択**。リクエストしたリソースが複数存在し、ユーザやユーザーエージェントに選択肢を提示するときに返される。
    具体例として、W3Cの <https://www.w3.org/TR/xhtml11/DTD/xhtml11.html>
  - 301 Moved Permanently
    **恒久的に移動した**。リクエストしたリソースが恒久的に移動されているときに返される。Location:ヘッダに移動先のURLが示されている。
    ウェブサイトが移転した場合などに用いる\[1\]。ウェブサイト移転の特殊な場合として、HTTPからHTTPSへの移転も該当する\[2\]。
    そのほか、ファイルではなく[ディレクトリ](../Page/ディレクトリ.md "wikilink")に対応するURLの末尾に*/*を書かずにアクセスした場合に返される。具体例として、https://www.w3.org/TR （ただし近年のウェブブラウザは*/*の脱落を自動的に補完するため、エラーは通常表示されない）。
  - 302 Found
    **発見した**。リクエストしたリソースが一時的に移動されているときに返される。Location:ヘッダに移動先のURLが示されている。
    元々は**Moved Temporarily**（一時的に移動した）で、本来はリクエストしたリソースが一時的にそのURLに**存在せず**、別のURLにある場合に使用するステータスコードであった。しかし、例えば掲示板やWikiなどで投稿後にウェブブラウザに対して他のURLに転送させたいときにもこのコードが使用されるようになったため、302はFoundになり、新たに303・307が作成された。
  - 303 See Other
    **他を参照せよ**。リクエストに対するレスポンスが他のURLに存在するときに返される。Location:ヘッダに移動先のURLが示されている。Location:ヘッダで指示されるリソースに対してGETでリクエストしなければならない
    リクエストしたリソースは確かにそのURLにあるが、他のリソースをもってレスポンスとするような場合に使用する。302の説明で挙げたような、掲示板やWikiなどで投稿後にウェブブラウザに対して他のURLに転送させたいときに使われるべきコードとして導入された。
  - 304 Not Modified
    **未更新**。リクエストしたリソースは更新されていないことを示す。
    例として、 If-Modified-Since:ヘッダを使用したリクエストを行い、そのヘッダに示された時間以降に更新がなかった場合に返される。
  - 305 Use Proxy
    **プロキシを使用せよ**。レスポンスのLocation:ヘッダに示されるプロキシを使用してリクエストを行わなければならないことを示す。
  - 306 (Unused)
    **将来のために予約されている**。ステータスコードは前のバージョンの仕様書では使われていたが、もはや使われておらず、将来のために予約されているとされる。
    検討段階では、「Switch Proxy」というステータスコードが提案されていた\[3\]\[4\]。
  - 307 Temporary Redirect
    **一時的リダイレクト**。 リクエストメソッドを変更してはならない(例：元URLにPOSTメソッドによるリクエストならば移動先にもPOSTメソッドでリクエストしなければならない)
    リクエストしたリソースは一時的に移動されているときに返される。Location:ヘッダに移動先のURLが示されている。
    302の規格外な使用法が横行したため、302の本来の使用法を改めて定義したもの。
  - 308 Permanent Redirect
    **恒久的リダイレクト**。 リクエストメソッドを変更してはならない(例：元URLにPOSTメソッドによるリクエストならば移動先にもPOSTメソッドでリクエストしなければならない)
    リクエストしたリソースは恒久的に移動されているときに返される。Location:ヘッダに移動先のURLが示されている。
    301の規格外な使用法が横行したため、301の本来の使用法を改めて定義したもの。

## 4xx Client Error クライアントエラー

クライアントからのリクエストに誤りがあった。

  - 400 Bad Request
    **リクエストが不正である**。定義されていないメソッドを使うなど、クライアントのリクエストがおかしい場合に返される。
  -
    **認証が必要である**。[Basic認証](../Page/Basic認証.md "wikilink")や[Digest認証](../Page/Digest認証.md "wikilink")などを行うときに使用される。
    たいていのウェブブラウザは、レスポンスヘッダー`WWW-Authenticate`で処理可能な認証方式が指定されていれば、認証ダイアログを表示する。
  - 402 Payment Required
    **支払いが必要である**。現在は実装されておらず、将来のために予約されているとされる。
    Web Payments HTTP APIで利用が検討されていたものの\[5\]、Web Payments HTTP APIそのものの開発が中止されたため\[6\]、採用には至っていない。
  - [403 Forbidden](https://ja.wikipedia.org/wiki/HTTP_403 "wikilink")
    **禁止されている**。リソースにアクセスすることを拒否された。リクエストはしたが処理できないという意味。
    アクセス権がない場合や、ホストがアクセス禁止処分を受けた場合などに返される。
    例: 社内（[イントラネット](../Page/イントラネット.md "wikilink")）からのみアクセスできるページに社外からアクセスしようとした。
  - [404 Not Found](../Page/HTTP_404.md "wikilink")
    **未検出**。リソースが見つからなかった。
    単に、アクセス権がない場合などにも使用される。
  - 405 Method Not Allowed
    **許可されていないメソッド**。許可されていないメソッドを使用しようとした。
    例: POSTメソッドの使用が許されていない場所で、POSTメソッドを使用した場合に返される。
  - 406 Not Acceptable
    **受理できない**。Accept関連のヘッダに受理できない内容が含まれている場合に返される。
    例: サーバは英語か日本語しか受け付けられないが、リクエストのAccept-Language:ヘッダにzh（中国語）しか含まれていなかった。
    例: サーバはapplication/pdfを送信したかったが、リクエストのAccept:ヘッダにapplication/pdfが含まれていなかった。
    例: サーバはUTF-8の文章を送信したかったが、リクエストのAccept-Charset:ヘッダには、UTF-8が含まれていなかった。
  - 407 Proxy Authentication Required
    **[プロキシ](../Page/プロキシ.md "wikilink")認証が必要である**。プロキシの認証が必要な場合に返される。
  - 408 Request Timeout
    **リクエストタイムアウト**。リクエストが時間以内に完了していない場合に返される。
  - 409 Conflict
    **競合**。要求は現在のリソースと競合するので完了出来ない。
  - 410 Gone
    **消滅した**。リソースは恒久的に移動・消滅した。どこに行ったかもわからない。
    404 Not Foundと似ているが、こちらは二度と復活しない場合に使われる。ただし、このコードは特別に設定しないと提示できないため、リソースが消滅しても404コードを出すサイトが多い。
  - 411 Length Required
    **長さが必要**。Content-Length ヘッダがないのでサーバがアクセスを拒否した場合に返される。
  - 412 Precondition Failed
    **前提条件で失敗した**。前提条件が偽だった場合に返される。
    例: リクエストのIf-Unmodified-Since:ヘッダに書いた時刻より後に更新があった場合に返される。
  - 413 Payload Too Large (RFC 7231)
    **ペイロードが大きすぎる**。リクエストエンティティがサーバの許容範囲を超えている場合に返す。
    例: アップローダの上限を超えたデータを送信しようとした。
    RFC 2616以前では、**Request Entity Too Large**（リクエストエンティティが大きすぎる）と定められていた。
  - 414 URI Too Long (RFC 7231)
    **URIが大きすぎる**。URIが長過ぎるのでサーバが処理を拒否した場合に返す。
    例: 画像データのような大きなデータをGETメソッドで送ろうとし、URIが何10kBにもなった場合に返す（上限はサーバに依存する）。
    RFC 2616以前では、**Request-URI Too Long**（リクエストURIが大きすぎる）と定められていた。
  - 415 Unsupported Media Type
    **サポートしていないメディアタイプ**。指定された[メディアタイプ](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink")がサーバでサポートされていない場合に返す。
  - 416 Range Not Satisfiable (RFC 7233)
    **レンジは範囲外にある**。実リソースのサイズを超えるデータを要求した。
    たとえば、リソースのサイズが1024Byteしかないのに、1025Byteを取得しようとした場合などに返す。
    RFC 2616以前では、**Requested Range Not Satisfiable**（リクエストしたレンジは範囲外にある）と定められていた。
  - 417 Expectation Failed
    **Expectヘッダによる拡張が失敗**。その拡張はレスポンスできない。またはプロキシサーバは、次に到達するサーバがレスポンスできないと判断している。
    具体例として、Expect:ヘッダに100-continue以外の変なものを入れた場合や、そもそもサーバが100 Continueを扱えない場合に返す。
  - 418 I'm a teapot
    **私はティーポット**。[HTCPCP/1.0の拡張ステータスコード](../Page/Hyper_Text_Coffee_Pot_Control_Protocol.md "wikilink")。
    [ティーポット](https://ja.wikipedia.org/wiki/ティーポット "wikilink")に[コーヒー](https://ja.wikipedia.org/wiki/コーヒー "wikilink")を淹れさせようとして、拒否された場合に返すとされる、[ジョーク](../Page/ジョーク.md "wikilink")のコードである。2017年にこれを除去しようという動きがあったが、反対運動が起こったため、418は正式に「予約済み」となった。
  - 421 Misdirected Request (RFC 7540)
    **誤ったリクエスト**。
  - 422 Unprocessable Entity
    **処理できないエンティティ**。WebDAVの拡張ステータスコード。[RESTにおいて](../Page/Representational_State_Transfer.md "wikilink")、入力値の検証の失敗（バリデーションエラー）を伝える目的で使用する場合もある\[7\]\[8\]。
  - 423 Locked
    **ロックされている**。WebDAVの拡張ステータスコード。リクエストしたリソースがロックされている場合に返す。
  - 424 Failed Dependency
    **依存関係で失敗**。WebDAVの拡張ステータスコード。
  - 425 Too Early (RFC 8470)
    **Early dataを受け入れない**。[TLS 1.3のearly](../Page/Transport_Layer_Security.md "wikilink") dataオプションが使用された場合（セッション再開で0-RTTのリクエスト送信）など、[リプレイ攻撃が可能な方法で送信されたリクエストに対して](https://ja.wikipedia.org/wiki/反射攻撃 "wikilink")、これを拒絶することを伝達する。クライアントは新規にTLS接続を確立し、再度リクエストを送るべきである。
  - 426 Upgrade Required
    **アップグレード要求**。当初、RFC 2817 Upgrading to TLS Within HTTP/1.1で定義され、その後HTTPそのもののRFCの一部である RFC 7231 に取り込まれている。
  - 428 Precondition Required (RFC 6585)
    **事前条件が必要**。条件付きリクエストでなければならない場合に返される。
  - 429 Too Many Requests (RFC 6585)
    **要求が多すぎる**。短時間に大量の要求を送信してきたため、サーバーが処理を拒否する場合に返される。
  - 431 Request Header Fields Too Large (RFC 6585)
    **リクエストヘッダーフィールドが大きすぎる**。リクエストヘッダーフィールドのデータ量が多いため、サーバーが処理を拒否する場合に返される。
  - [451 Unavailable For Legal Reasons](https://ja.wikipedia.org/wiki/HTTP_451 "wikilink")
    **法的理由により利用不可**。403 Forbiddenから派生したステータスコード。

## 5xx Server Error サーバエラー

サーバがリクエストの処理に失敗した。

  - 500 Internal Server Error
    **サーバ内部エラー**。サーバ内部にエラーが発生した場合に返される。
    例として、[CGIとして動作させているプログラムに文法エラーがあったり](../Page/Common_Gateway_Interface.md "wikilink")、設定に誤りがあった場合などに返される。
  - 501 Not Implemented
    **実装されていない**。実装されていないメソッドを使用した。
    例として、WebDAVが実装されていないサーバに対してWebDAVで使用するメソッド（MOVEやCOPY）を使用した場合に返される。
  - 502 Bad Gateway
    **不正なゲートウェイ**。ゲートウェイ・プロキシサーバは不正な要求を受け取り、これを拒否した。
  - [503 Service Unavailable](https://ja.wikipedia.org/wiki/HTTP_503 "wikilink")
    **サービス利用不可**。サービスが一時的に過負荷やメンテナンスで使用不可能である。
    例として、アクセスが殺到して処理不能に陥った場合に返される。
  - 504 Gateway Timeout
    **ゲートウェイタイムアウト**。ゲートウェイ・プロキシサーバはURIから推測されるサーバからの適切な[レスポンスがなくタイムアウトした](https://ja.wikipedia.org/wiki/レスポンスタイム "wikilink")。
  - 505 HTTP Version Not Supported
    **サポートしていないHTTPバージョン**。リクエストがサポートされていないHTTPバージョンである場合に返される。
  - 506 Variant Also Negotiates
    [Transparent Content Negotiation in HTTPで定義されている拡張ステータスコード](https://ja.wikipedia.org/wiki/Transparent_Content_Negotiation_in_HTTP "wikilink")。
  - 507 Insufficient Storage
    **容量不足**。WebDAVの拡張ステータスコード。リクエストを処理するために必要なストレージの容量が足りない場合に返される。
  - 508 Loop Detected
    **ループを検出**。WebDAVの拡張ステータスコード。
  - 510 Not Extended
    **拡張できない**。[An HTTP Extension Frameworkで定義されている拡張ステータスコード](https://ja.wikipedia.org/wiki/An_HTTP_Extension_Framework "wikilink")。
  - 511 Network Authentication Required (RFC 6585)
    **ネットワークに対する認証が必要**。での使用を意図している。

## 脚注

## 外部リンク

  - [Hypertext Transfer Protocol (HTTP) Status Code Registry](https://www.iana.org/assignments/http-status-codes/http-status-codes.xhtml) (IANA)
  - RFC 1945 - Hypertext Transfer Protocol -- HTTP/1.0
  - RFC 2068 - Hypertext Transfer Protocol -- HTTP/1.1
  - RFC 2616 - Hypertext Transfer Protocol -- HTTP/1.1 （RFC2068の改訂版）
  - RFC 2518 - HTTP Extensions for Distributed Authoring -- WEBDAV
  - RFC 3229 - Delta encoding in HTTP
  - RFC 2324 - Hyper Text Coffee Pot Control Protocol (HTCPCP/1.0)
  - RFC 2817 - Upgrading to TLS Within HTTP/1.1
  - RFC 2295 - Transparent Content Negotiation in HTTP
  - RFC 2774 - An HTTP Extension Framework
  - RFC 6585 - Additional HTTP Status Codes
  - RFC 7231 - Hypertext Transfer Protocol (HTTP/1.1): Semantics and Content
  - RFC 7233 - Hypertext Transfer Protocol (HTTP/1.1): Range Requests
  - RFC 7725 - An HTTP Status Code to Report Legal Obstacles
  - RFC 8297 - An HTTP Status Code for Indicating Hints
  - [Studying HTTP HTTP Status Code](https://web.archive.org/web/20150213010711/http://www.eonet.ne.jp/~h-hash/status_code.html) - 日本語の解説

[Category:HTTPステータスコード](https://ja.wikipedia.org/wiki/Category:HTTPステータスコード "wikilink") [Category:コンピュータ関連の一覧](https://ja.wikipedia.org/wiki/Category:コンピュータ関連の一覧 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.