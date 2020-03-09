> この記事は[Hypertext Transfer Protocol](https://ja.wikipedia.org/wiki/Hypertext_Transfer_Protocol)から翻訳されています。


**Hypertext Transfer Protocol** （[ハイパーテキスト](https://ja.wikipedia.org/wiki/ハイパーテキスト "wikilink")・トランスファー・プロトコル、略称 **HTTP**）とは、[Webブラウザが](../Page/ウェブブラウザ.md "wikilink")[Webサーバ](https://ja.wikipedia.org/wiki/Webサーバ "wikilink")と通信する際に主として使用する[通信プロトコル](https://ja.wikipedia.org/wiki/通信プロトコル "wikilink")であり、[インターネット・プロトコル・スイート](https://ja.wikipedia.org/wiki/インターネット・プロトコル・スイート "wikilink")のメンバである。[HTMLなどのテキストによって記述された](https://ja.wikipedia.org/wiki/HyperText_Markup_Language "wikilink")[Webページ等の](https://ja.wikipedia.org/wiki/ウェブページ "wikilink")[コンテンツ](https://ja.wikipedia.org/wiki/コンテンツ "wikilink")の送受信に用いられる。

## 概要

[HTML](https://ja.wikipedia.org/wiki/HyperText_Markup_Language "wikilink") (HyperText Markup Language) や [XML](https://ja.wikipedia.org/wiki/Extensible_Markup_Language "wikilink") (Extensible Markup Language) によって記述された[ハイパーテキスト](https://ja.wikipedia.org/wiki/ハイパーテキスト "wikilink")の転送を主な目的としているが、それ以外にも、[バイナリ](https://ja.wikipedia.org/wiki/バイナリ "wikilink")形式の画像、音声を含め、様々なデータを扱うことが可能である。トランスポート・プロトコルとして[TCPを使用する](https://ja.wikipedia.org/wiki/Transmission_Control_Protocol "wikilink")。

HTTPはリクエスト-レスポンス型のプロトコルであり、クライアントがサーバにリクエストメッセージを送信する。 基本的な考え方は非常に単純で、「何を」「どうして」欲しいのかを伝える。[URL](https://ja.wikipedia.org/wiki/URL "wikilink")が「何を」、メソッドが「どうして」に当たる。 サーバはこれにレスポンスメッセージを返し、基本的にこの時点で初期状態に戻る。つまり、サーバはクライアントの状態を保存しない。

[World Wide WebにおけるWebページなどの](https://ja.wikipedia.org/wiki/World_Wide_Web "wikilink")[リソースは](https://ja.wikipedia.org/wiki/リソース_\(WWW\) "wikilink")、[Uniform Resource Identifierによって指定される](https://ja.wikipedia.org/wiki/Uniform_Resource_Identifier "wikilink")。HTTP を使用してリソースにアクセスするときは、http: が先頭についた URL を使用する。下にURL の例を挙げる。

<http://www.example.co.jp/~test/samples/index.html>

最初のHTTP/0.9ではURLを指定してコンテントをダウンロードするのみの簡単なやりとりであったが、HTTP/1.0で改良された。

  - リクエストのセマンティクスを指定する、様々なリクエストメソッドが追加された。POSTを使って、アップロード（クライアントからサーバへのデータの転送）が可能になった。
  - [NNTPや](https://ja.wikipedia.org/wiki/Network_News_Transfer_Protocol "wikilink")[SMTPのような各種ヘッダが定義され](https://ja.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol "wikilink")、[HTTP cookieなどの利用が可能になった](https://ja.wikipedia.org/wiki/HTTP_cookie "wikilink")。

HTTP/1.1では複数データを効率よく転送するための持続的接続や、[プロキシ](https://ja.wikipedia.org/wiki/プロキシ "wikilink")の利用等も想定した仕様になった。

このほかの点を箇条書きで示す。

  - [ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")[80](https://ja.wikipedia.org/wiki/80 "wikilink")を[デフォルトとして使用する](https://ja.wikipedia.org/wiki/デフォルト_\(コンピュータ\) "wikilink")。
  - [TLSで暗号化され](https://ja.wikipedia.org/wiki/Transport_Layer_Security "wikilink")、セキュリティを確保したHTTPは、**[HTTPS](https://ja.wikipedia.org/wiki/HTTPS "wikilink")**と呼ばれる（httpsは実際には[URIスキームの](https://ja.wikipedia.org/wiki/Uniform_Resource_Identifier "wikilink")1つであり、実際のプロトコルには**HTTP over SSL/TLS**が用いられる）。
  - HTTP は基本的にサーバが状態を保持しない (stateless) プロトコルだが、[データベース](../Page/データベース.md "wikilink")などを使用する[Webアプリケーションにおいては状態保持が必要だったため](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")、いわゆる [Cookie](https://ja.wikipedia.org/wiki/HTTP_cookie "wikilink")（クッキー）とよばれる機構が [Netscape Communications Corporation](https://ja.wikipedia.org/wiki/ネットスケープコミュニケーションズ "wikilink") によって導入された。Cookie を使用することによって状態を管理し、"セッション" を維持することが可能になる。
  - HTTPの拡張プロトコルとして[WebDAV](https://ja.wikipedia.org/wiki/WebDAV "wikilink")がある。
  - [UPnPでは](https://ja.wikipedia.org/wiki/Universal_Plug_and_Play "wikilink")、HTTPをUDP上で使用するHTTPUや、[マルチキャスト](https://ja.wikipedia.org/wiki/マルチキャスト "wikilink")で使用する**HTTPMU**が規定された。
  - 行末文字はCRLFで、[インターネット・プロトコル・スイート](https://ja.wikipedia.org/wiki/インターネット・プロトコル・スイート "wikilink")において[アプリケーション層](https://ja.wikipedia.org/wiki/アプリケーション層 "wikilink")に属する他の多くのプロトコルと同じである。

## 歴史

[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")の物理学者[ティム・バーナーズ＝リー](https://ja.wikipedia.org/wiki/ティム・バーナーズ＝リー "wikilink")は[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")末、[ロバート・カイリュー](https://ja.wikipedia.org/wiki/ロバート・カイリュー "wikilink")と共に初のWebブラウザとWebサーバを作成した。ブラウザには通信をするためのプロトコルが必要だったので、二人はHTTPの最初期のバージョンを設計した。

以来インターネットの大部分をHTTP通信が占めるようになり、[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")にはインターネット上の通信の75%がHTTPによるものになった。

最初期のHTTP/0.9の仕様書は紙に印刷すれば1枚で済むような非常に簡素なドキュメントであったが、2度のバージョンアップを経たHTTP/1.1の仕様書は実に176ページ近くの分量に膨れあがった。

### HTTP/0.9

[1991年](https://ja.wikipedia.org/wiki/1991年 "wikilink")に最初にドキュメント化されたバージョン\[1\]。メソッドは GET しかなかった。レスポンスは単純にドキュメントの内容を返してコネクションを切断するだけで、レスポンスコードの規定もない。下記は、HTTP/0.9 のリクエストの例。

`GET /index.html`

### HTTP/1.0

[1996年](https://ja.wikipedia.org/wiki/1996年 "wikilink")[5月](https://ja.wikipedia.org/wiki/5月 "wikilink")に RFC 1945 として発表された。仕様が RFC で扱われるようになった。メソッドに POST など GET 以外のものが増えた。レスポンスはヘッダーがつくようになり、ステータスコードを含めるようになった。HTTP/0.9 と区別するため、リクエストプロトコルにバージョンを含めることになった。

<dl>

<dt>

HTTP/1.0のリクエスト

</dt>

<dd>

``` http
GET /index.html HTTP/1.0
```

</dd>

### HTTP/1.1

[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")[1月](https://ja.wikipedia.org/wiki/1月 "wikilink")に RFC 2068 として初版が発表された。その後、2回改訂された。RFC 7230 から RFC 7235 で規定されている。かつては RFC 2616 が HTTP/1.1 を規定していたため、こちらもよく参照されている。

[名前ベースバーチャルホストをサポートした](https://ja.wikipedia.org/wiki/バーチャルホスト "wikilink")。インターネット人気に伴い多くの企業がWebサイトを持ち始めたが、当時はまだまだ企業が自前のWebサーバを運用するのは人員、効率の問題で難しく、[ISPのサーバでホスティングをしていた](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")。また、一社ごとに専用サーバを用意するほどのことでもないため、一台のサーバで複数のWebサイトを運用していた。

しかし、IPアドレスのみで相手を特定するHTTP/1.0はこれに対応できなかった。例えば、ある1台のサーバに foo.example.com と bar.example.com という二つの[仮想Webサーバがあり](https://ja.wikipedia.org/wiki/バーチャルホスト "wikilink")、クライアントは http://foo.example.com/index.html にアクセスしたいとする。この場合はDNSサーバに foo.example.com のIPアドレスを問い合わせ、次にそのIPアドレスを使って該当サーバにアクセスし、GET index.html を要求することになる。しかし同じサーバ上にある bar.example.comもIPアドレスは同じであり、もし両方の仮想サーバに index.html というファイルが存在すれば、クライアントがどちらにアクセスしようとしているのか、判別できない。

対策としてはそれぞれにIPアドレスを付与する方法もあるが、IPv4の資源を無駄にすることになる。この問題を解決するため、Hostヘッダが追加された。

<dt>

HTTP/1.1のリクエスト

</dt>

<dd>

``` http
GET /index.html HTTP/1.1
Host: foo.example.com
```

</dd>

</dl>

### HTTP/2

HTTP/2の目標はHTTP/1.1のトランザクション・セマンティクスとの完全な後方互換性を維持したまま非同期な接続の[多重化](https://ja.wikipedia.org/wiki/多重化 "wikilink")、ヘッダ[圧縮](https://ja.wikipedia.org/wiki/データ圧縮 "wikilink")、リクエストとレスポンスの[パイプライン化を実現することである](https://ja.wikipedia.org/wiki/HTTPパイプライン "wikilink")。[Google](https://ja.wikipedia.org/wiki/Google "wikilink")によって立ち上げられ\[2\]、Googleのブラウザーである[Chromeだけではなく](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")、他にも、[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")、[Firefox](https://ja.wikipedia.org/wiki/Firefox "wikilink")、[Amazon Silk等が対応しているHTTP互換のプロトコル](https://ja.wikipedia.org/wiki/Amazon_Silk "wikilink")[SPDY](https://ja.wikipedia.org/wiki/SPDY "wikilink")の人気が高まっていることに対応するために開発された\[3\]。

### HTTP/3

HTTP-over-QUIC（hq）として[IETFが開発していた新たな](https://ja.wikipedia.org/wiki/Internet_Engineering_Task_Force "wikilink")[通信プロトコル](https://ja.wikipedia.org/wiki/通信プロトコル "wikilink")が、HTTP/3へと改名される。\[4\] IETFが策定を進めている[QUIC](https://ja.wikipedia.org/wiki/QUIC "wikilink")は[トランスポート層](https://ja.wikipedia.org/wiki/トランスポート層 "wikilink")におけるプロトコルの名称であり、アプリケーション層プロトコルであるHTTP-over-QUICとの区別を明確にするため、このような名称変更に至った。\[5\]

HTTP/2と比べ、多重化するストリームの取り扱いが下位層のQUICへ移行したこと\[6\]、を回避するためのヘッダ圧縮の変更（HTTP/3用にQPACKが開発されている）\[7\]などの差異がある。

## 動作

### 通信の開始

他のプロトコル同様、クライアント側とサーバ側では役割が大きく異なる。HTTP通信を開始できるのはクライアント側のみである。

クライアント側がサーバにリクエストを送り、サーバがクライアントにレスポンスを返すのが最も典型的なHTTPのやりとりである。

### 接続

システム間でメッセージをやりとりするにはTCP接続を確立させる必要がある。

HTTP/0.9ではクライアントのリクエストごとにTCP接続を確立させる必要があった。これは当時のWebサイトがシンプルなテキストベースであることが多かったためである。近年ではJavaScriptやアニメーション画像など、多数のオブジェクトが埋め込まれたWebサイトが一般的となってきており、これらのオブジェクトを取得するたびにTCP接続を確立するのはサーバやネットワークに大きな負担を強いるため、1回のTCP接続で、複数のHTTPリクエスト・レスポンスをやり取りする持続的接続がHTTP/1.0の拡張として導入された。その後、HTTP/1.1では、持続的接続がデフォルトとなった。すなわち、何も指定しなければ持続的接続となり、持続的接続を望まなければヘッダーフィールドにConnection: closeを追加する仕様となっている。

### パイプライン

クライアントは前のリクエストに対するサーバの応答を待たずに別のリクエストを発行できる。

## メソッド

HTTPでは8つのメソッドが定義されている。ただし、実際のHTTP通信ではGETとPOSTメソッドだけで殆どを占める。

| メソッド    | HTTP/0.9 | HTTP/1.0 | HTTP/1.1 |
| ------- | -------- | -------- | -------- |
| GET     | ○        | ○        | ○        |
| POST    |          | ○        | ○        |
| PUT     |          | △        | ○        |
| HEAD    |          | ○        | ○        |
| DELETE  |          | △        | ○        |
| OPTIONS |          |          | ○        |
| TRACE   |          |          | ○        |
| CONNECT |          |          | ○        |

HTTPメソッドの一覧

  - GET
    指定されたURIのリソースを取り出す。HTTPの最も基本的な動作で、HTTP/0.9では唯一のメソッド。
  - POST
    GETとは反対にクライアントがサーバにデータを送信する。Webフォームや[電子掲示板](https://ja.wikipedia.org/wiki/電子掲示板 "wikilink")への投稿などで使用される。GETの場合と同じく、サーバはクライアントにデータを返すことができる。
  - PUT
    指定したURIにリソースを保存する。URIが指し示すリソースが存在しない場合は、サーバはそのURIにリソースを作成する。画像のアップロードなどが代表的。
  - DELETE
    指定したURIのリソースを削除する。
  - OPTIONS
    サーバを調査する。例えば、サーバがサポートしているHTTPバージョンなどを知ることができる。
  - HEAD
    GETと似ているが、サーバはHTTPヘッダのみ返す。クライアントはWebページを取得せずともそのWebページが存在するかどうかを知ることができる。例えばWebページのリンク先が生きているか、データを全て取得することなく検証することができる。
  - TRACE
    サーバまでのネットワーク経路をチェックする。サーバは受け取ったメッセージのそれ自体をレスポンスのデータにコピーして応答する。WindowsのTracertやUNIXのTracerouteとよく似た動作。
  - CONNECT
    TCPトンネルを接続する。暗号化したメッセージをプロキシサーバを経由して転送する際に用いる。当初、[ネットスケープコミュニケーションズ](https://ja.wikipedia.org/wiki/ネットスケープコミュニケーションズ "wikilink")によって考案されたものがIETFドラフト[Tunneling TCP based protocols through Web proxy servers](https://tools.ietf.org/html/draft-luotonen-web-proxy-tunneling-01)として公開され\[8\]、RFC 2817 に取り込まれた。その後、RFC 7230 で定義が更新されている\[9\]。

HTTPの仕様以外で定義しているメソッドは、IANAのHypertext Transfer Protocol (HTTP) Method Registry\[10\]で管理されている。WebDavで使用するものや、 RFC 5789 のなどがある。

## サーバの連携

### バーチャルホスト

上記参照

### リダイレクト

別のURIに対して再度のメソッド実行を要求する機能である。301 Movedや303 See Otherなどのリダイレクトを指示するステータスコードとURIを受け取り、クライアントはこのURIに再度メソッドを実行する。

### クッキー

## HTTPメッセージ

リクエストとレスポンスでやり取りされるデータは、HTTPメッセージと呼ばれる。 リクエストメッセージはリクエスト行・ヘッダーフィールド・ボディで構成され、レスポンスメッセージは、ステータス行・ヘッダーフィールド・ボディで構成される。ヘッダーフィールドとボディは空となる場合もある。

下にもっとも単純なクライアントとサーバ(www.google.co.jp:80)とのやり取りの例を挙げる。

**クライアントのリクエスト**:

``` http
GET / HTTP/1.0
```

この例では、リクエスト行のみで、ヘッダーフィールドとボディは空となっている。 リクエスト行はメソッド、URI、HTTPバージョンの3つの要素から構成され、それぞれスペースで区切られる。 メソッドは`GET`、URIは「/」、HTTPバージョンは1.0である。

`GET`はリソースを取得するためのメソッドであり、URIの「/」はルートリソースを対象にしたリクエストであることを示している。

**サーバのレスポンス**:

``` http
HTTP/1.0 200 OK
Cache-Control: private
Content-Type: text/html
Set-Cookie: PREF=ID=72c1ca72230dea65:LD=ja:TM=1113132863:LM=1113132863:S=nNO7MIp
W2o7Cqeu_; expires=Sun, 17-Jan-2038 19:14:07 GMT; path=/; domain=.google.co.jp
Server: GWS/2.1
Date: Sun, 10 Apr 2005 11:34:23 GMT
Connection: Close

<html><head><meta http-equiv="content-type" content="text/html; charset=Shift_JI
 S"><title>Google</title><style><!-- 
……以下省略 -->
```

先頭のステータス行はHTTPバージョン、ステータスコード、メッセージから構成される。 ステータスコードの「200」は処理の成功を表し、これを補足するメッセージが「OK」である。

2行目以降にヘッダフィールドが続く。 さらに空行を挟んで、レスポンスボディとなる。

## HTTPヘッダフィールド

ヘッダの各要素は

    フィールド名: 内容

のペアで構成される。 ブラウザの情報を表す`User-Agent`、使用候補言語を表す`Accept-Language`、他ページへのリンクを辿った場合にそのリンク元ページの[URLを表す](https://ja.wikipedia.org/wiki/Uniform_Resource_Locator "wikilink")`Referer`などが代表的なフィールドである。

なお、リクエスト時の`Host`ヘッダはHTTP/1.1では必須であるが、HTTP/1.0ではなくてもよい。 ただし、サーバが[バーチャルホスト](https://ja.wikipedia.org/wiki/バーチャルホスト "wikilink")を利用している場合は、`Host`ヘッダがないとリソース取得に失敗するので、たとえHTTP/1.0を使用していても`Host`ヘッダを付加しなければならない。

### HTTPヘッダフィールドの一覧

| ヘッダ                                                               | 概要                                                                                  | HTTP/0.9 | HTTP/1.0 | HTTP/1.1 |
| ----------------------------------------------------------------- | ----------------------------------------------------------------------------------- | -------- | -------- | -------- |
| Accept                                                            | クライアントの受け入れ可能コンテンツタイプを示す                                                            |          | ○        | ○        |
| Accept-Charset                                                    | クライアントの受け入れ可能文字セットを示す                                                               |          | ○        | ○        |
| Accept-Encoding                                                   | クライアントの受け入れ可能文字エンコーディングを示す                                                          |          | ○        | ○        |
| Accept-Language                                                   | クライアントの受け入れ可能言語を示す                                                                  |          | ○        | ○        |
| Authorization                                                     | クライアントの認証情報を示す                                                                      |          | ○        | ○        |
| [Cookie](https://ja.wikipedia.org/wiki/HTTP_cookie "wikilink")    | クライアントの状態管理情報をサーバに返す                                                                |          |          |          |
| Cookie2                                                           | HTTP/1.1のSet-Cookie2ヘッダの受け入れ可能をサーバに知らせる                                             |          |          |          |
| Expect                                                            | クライアントがサーバに期待する動作を示す                                                                |          |          | ○        |
| From                                                              | リクエスト発行者個人の情報を示す。一般的に電子メールアドレスを使用する                                                 |          | ○        | ○        |
| Host                                                              | 要求しているオブジェクトがあるホストを示す                                                               |          |          | ○        |
| If-Match                                                          | [if文](https://ja.wikipedia.org/wiki/if文 "wikilink")を用い条件が真の場合のみリクエストを処理するようサーバに要求する |          |          | ○        |
| If-None-Match                                                     | If-Matchの逆で条件が真でない場合のみリクエストを処理する要求                                                  |          |          | ○        |
| If-Range                                                          | 条件が真の場合のみ指定したオブジェクトの範囲を返すようサーバに要求する                                                 |          |          | ○        |
| If-Modified-Since                                                 | 指定日時以降にオブジェクトが変更されている場合のみリクエストを処理するよう要求する                                           |          | ○        | ○        |
| If-Unmodified-Since                                               | If-Modified-Sinceの逆で真でないときのみ実行する                                                    |          |          | ○        |
| Max-Forwards                                                      | リクエストの中間システム経由数を最大いくつまでかを指定する                                                       |          |          | ○        |
| Proxy-Authorization                                               | クライアントがプロキシサーバに対して自身の認証を行う                                                          |          |          | ○        |
| Range                                                             | オブジェクト全体でなくリソースの一部を要求する                                                             |          |          | ○        |
| [Referer](https://ja.wikipedia.org/wiki/HTTPリファラ "wikilink")      | リクエストの出所を示す。一般的にはユーザの辿ったWebページのURLが用いられる                                            |          | ○        | ○        |
| TE                                                                | レスポンスの受け入れ可能転送エンコーディングを示す                                                           |          |          | ○        |
| [User-Agent](https://ja.wikipedia.org/wiki/ユーザーエージェント "wikilink") | クライアントのWebブラウザなどの情報を示す                                                              |          | ○        | ○        |

リクエストヘッダ

| ヘッダ                                                        | 概要                                         | HTTP/0.9 | HTTP/1.0 | HTTP/1.1 |
| ---------------------------------------------------------- | ------------------------------------------ | -------- | -------- | -------- |
| Accept-Ranges                                              | オブジェクトの一部に対するリクエストをサーバが受け入れ可能か示す           |          |          | ○        |
| Age                                                        | オブジェクトの経過時間を秒単位で返す                         |          |          | ○        |
| [ETag](https://ja.wikipedia.org/wiki/HTTP_ETag "wikilink") | オブジェクトのエンティティタグ値を示す                        |          |          | ○        |
| Location                                                   | オブジェクトの場所を示す                               |          | ○        | ○        |
| Proxy-Authenticate                                         | プロキシサーバがクライアントに認証を要求するときに用いる               |          |          | ○        |
| Retry-After                                                | リクエストの再試行をいつ行うかをクライアントに通知する                |          | ○        | ○        |
| Server                                                     | サーバのベンダー名、バージョン番号を示す                       |          | ○        | ○        |
| Set-Cookie2                                                | サーバがクライアントにCookieを送信するときに用いる               |          |          |          |
| Vary                                                       | サーバがレスポンス内容を決定する際にリクエストURI以外に用いたヘッダのリストを示す |          |          | ○        |
| WWW-Authenticate                                           | クライアントに対してリクエストの再発行を要求する。認証情報も含まれる         |          | ○        | ○        |

レスポンスヘッダ

| ヘッダ               | 概要                                       | HTTP/0.9 | HTTP/1.0 | HTTP/1.1 |
| ----------------- | ---------------------------------------- | -------- | -------- | -------- |
| Cache-Control     | メッセージの経由する中間キャッシュの動作を指示する                |          |          | ○        |
| Connection        | 中間システムが転送すべきでないヘッダのリストを示す                |          | ○        | ○        |
| Date              | メッセージの作成日時を示す                            |          | ○        | ○        |
| Pragma            | メッセージに関する追加情報を示す                         |          | ○        | ○        |
| Trailer           | メッセージボディの後に追加のヘッダーが表れることを示す              |          |          | ○        |
| Transfer-Encoding | クライアントの転送を目的としたオブジェクトのエンコーディングを示す        |          |          | ○        |
| Upgrade           | 通信相手に別のプロトコルにアップデートするよう要求する              |          |          | ○        |
| Via               | プロキシサーバ等中継地点を示す。                         |          |          | ○        |
| Warning           | メッセージに関する追加情報を示す。通常はキャッシュの問題を警告するときに使われる |          |          | ○        |

一般ヘッダ

| ヘッダ              | 概要                        | HTTP/0.9 | HTTP/1.0 | HTTP/1.1 |
| ---------------- | ------------------------- | -------- | -------- | -------- |
| Allow            | オブジェクトがサポートするHTTPメソッドを示す  |          | ○        | ○        |
| Content-Encoding | オブジェクトのエンコーディングを示す        |          | ○        | ○        |
| Content-Language | オブジェクトの言語（人間の言語）を示す       |          | ○        | ○        |
| Content-Length   | オブジェクトのサイズをバイト単位で示す       |          | ○        | ○        |
| Content-Location | オブジェクトの場所を示す              |          |          | ○        |
| Content-MD5      | オブジェクトのメッセージダイジェストを運ぶ     |          |          | △        |
| Content-Range    | メッセージボディで運ばれるオブジェクトの範囲を示す |          |          | ○        |
| Content-Type     | オブジェクトのタイプを示す             |          | ○        | ○        |
| Expires          | オブジェクトの有効期限の日時を示す         |          | ○        | ○        |
| Last-Modified    | オブジェクトが最後に変更された日時を示す      |          | ○        | ○        |

エンティティヘッダ

  - Accept
    サーバのレスポンスに含まれるメッセージボディで受け入れることが出来る[コンテンツタイプと各コンテンツタイプの相対的な優先度を指定するリクエストヘッダ](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink")。指定できるコンテンツタイプは[IANAによって定義されている](https://ja.wikipedia.org/wiki/Internet_Assigned_Numbers_Authority "wikilink")。

<!-- end list -->

``` http
Accept: text/plain; q=0.5, text/html,
    text/x-dvi; q=0.8, text/x-c
```

  -
    上記のようにAcceptヘッダには行をわけて複数のコンテンツタイプを指定できる。上記の例はいずれの4のコンテンツタイプのいずれも受け入れ可能であることを示す。0.5や0.8といった数字は品質係数で0〜1の範囲の数値である。数値の指定がなければ1.0となる。
      - text/plain; q=0.5
      - text/html
      - text/x-dvi; q=0.8
      - text/x-c

<!-- end list -->

  - Accept-Charset
    レスポンスで返されるメッセージボディの[文字コード](https://ja.wikipedia.org/wiki/文字コード "wikilink")を指定するリクエストヘッダ。Acceptと同じく複数指定でき品質係数も設定できる。定義済み文字セットはIANAが管理している。

<!-- end list -->

    Accept-Charset: UTF-8, *; q=0.8

  -
    この例だとクライアントは[UTF-8](https://ja.wikipedia.org/wiki/UTF-8 "wikilink")を優先的に希望しているが他の文字セットとの相対優先度0.8で受け入れている。ただしサーバからのレスポンスのHTTPヘッダそのものの文字コードは常にISO-8859-1である。

<!-- end list -->

  - Accept-Encoding
    クライアントが受信できるメッセージボディのエンコーディングを指定する。

<!-- end list -->

    Accept-Encoding: gzip, deflate

  -
    この例ではクライアントは[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")、または[zlib](https://ja.wikipedia.org/wiki/zlib "wikilink")フォーマットに対応している。ただし必ずしもここで指定されたエンコーディングでメッセージボディが返ってくるとは限らない。
    Accept-Encodingで指定可能なエンコーディングは、IANAがHTTP Content Coding Registryとして管理されている\[11\]。

<!-- end list -->

  - Accept-Language
    レスポンスの言語（人間の言語）に対する優先度を指定する。言語の指定には[IETF言語タグ](https://ja.wikipedia.org/wiki/IETF言語タグ "wikilink")を用いる。書き方は他のAccept-群と変わらず。

<!-- end list -->

    Accept-Language: en-gb, en; q=0.8

  -
    上記の例はまず[イギリス英語](https://ja.wikipedia.org/wiki/イギリス英語 "wikilink")を要求し、利用できない場合はその他の英語を要求する。

<!-- end list -->

  - Accept-Ranges
    Acceptで始まる他のヘッダフィールドと違いレスポンスヘッダである。現在の仕様では2つの指定方法しかない。

<!-- end list -->

  - Age
    リソースの推定経過時間を表示するレスポンスヘッダ。キャッシュサーバーはAgeヘッダの値からキャッシュしたリソースが有効かどうかを判定する。

<!-- end list -->

  - Allow

<!-- end list -->

  - Authentication-info
    ユーザ認証のやりとりの最後で用いられる、成功したレスポンスのサーバが含めることの出来るレスポンスヘッダ。

<!-- end list -->

  - Authorization
    サーバに対するクライアント自身の認証を行うことが出来る。

<!-- end list -->

  - Cache-Control
    キャッシングの動作を指定するためのマスターヘッダ。

<!-- end list -->

  - Connection

<!-- end list -->

  - Content-Encoding

<!-- end list -->

  - Content-Language
    リソースの表現に用いられる言語の明示に使われる。言語の指定はAccept-Languageヘッダと同じ。

<!-- end list -->

  - Content-Length

<!-- end list -->

  - Content-Location

<!-- end list -->

  - Content-MD5
    メッセージボディが変更されず宛先に届いたことの保証に用いる。[MD5](https://ja.wikipedia.org/wiki/MD5 "wikilink")によるハッシュ値をヘッダー値に記載する。ただし悪意の改ざんに対しては当然MD5も改ざんされるのであまり機能はしない。どちらかといえば偶発的な変更の保証をしている。RFC 7231 で廃止された。

<!-- end list -->

  - Content-Range
    ダウンロードの再開に用いられる。

<!-- end list -->

  - Content-Type

<!-- end list -->

  -
    メッセージボディに含まれるオブジェクトタイプを示す。次の例はリソースがテキストファイル、文字セットはISO-8859-4を使用していることを示している。

<!-- end list -->

    Content-Type: text/plain; Charset=ISO-8859-4

  - Cookie

    クライアントがHTTP状態管理を望む場合にサーバから受け取ったクッキーを以後のリクエストに次の例のようなヘッダを付加する。

<!-- end list -->

    Cookie: $Version="1"; NAME="VALUE";
            $Path="/shopping"; $domain="www.shop.com"+
            $Port="80"

  -
    $VersionはHTTPのバージョン、NAMEはクッキーの名前である。$から始まるクッキー名は使用が禁止されている。

<!-- end list -->

  - Cookie2
    基本的にCookieヘッダとCookie2ヘッダは別物である。

<!-- end list -->

  - Date
    サーバがメッセージを生成した日時を示す。リソースの更新日時を示すLast-Modifiedヘッダとは別である。

<!-- end list -->

  -
    HTTP/1.1では次のような形式を用いる。これはRFC 7231の7.1.1.1. Date/Time Formatsで定義されている。HTTP/1.1の以前の版であるRFC 2616では、日時の形式の定義にRFC 1123を参照していた（内容は同等である）。

<!-- end list -->

    Date: Sun, 06, Nov 1994 08:49:37 GMT

  -
    HTTP仕様ではレスポンスに`Date`ヘッダを含めることを求めている。ただしレスポンスのステータスがサーバエラーの場合には`Date`ヘッダは返らない。

<!-- end list -->

  - [ETag](https://ja.wikipedia.org/wiki/HTTP_ETag "wikilink")
    主にキャッシングのパフォーマンスを向上する目的で使われる。

<!-- end list -->

  - Expect
    サーバに対して特定の動作の期待を知らせる。用途としてはクライアントがサーバに対して*100 Continue*ステータスを返すことを期待する場合に使われる。

<!-- end list -->

    Expect: 100-continue

  -
    サーバが期待に応じられない場合は*417 Expectation Failed*を返す。クライアントがいくつかのプロキシ経由で通信している場合、各プロキシサーバはExpectヘッダの一切の修正を許されない。

<!-- end list -->

  - Expires
    オブジェクトの有効期限を示す。このヘッダで指定された日時までキャッシュはレスポンスのコピーを保持し、リクエストに対するレスポンスとして返すことができる。サーバがオブジェクトのキャッシュを望まない場合には`Expires`ヘッダに過去の日時を設定することが多い。仕様では1年以上先の日時は設定できない。

<!-- end list -->

    Expires: Thu, 28 Aug 2010 16:00:00 GMT

  -
    `Cache-Control`ヘッダの`max-age`ディレクティブは`Expires`ヘッダより優先されるため注意が必要である。

<!-- end list -->

  - From
    リクエストを発行したユーザを特定することが出来る。1990年代では電子メールアドレスを設定することが多かったが、[迷惑メールの問題もあり現在では殆ど使われていない](https://ja.wikipedia.org/wiki/スパム_\(メール\) "wikilink")。

<!-- end list -->

    From: user@example.com

  - Host
    主にレンタルサーバのサポートを目的としてHTTP/1.1で導入された。現在ではHostヘッダを利用できない場合、レンタルサーバのWebサイトとまともな通信ができないと言ってよい（詳細は[HTTP\#歴史を参照](https://ja.wikipedia.org/wiki/HTTP#HTTP.2F1.1 "wikilink")）。

<!-- end list -->

  - If-Match
    ETagが一致した場合のみ、メソッドを実行するようにサーバに要求する。例えばウィキペディアを編集する際、記事のソースを取得し、書き換える際の間に別のユーザが既に編集していないかを判断するときなどに用いられる。

<!-- end list -->

1.  利用者：AがHTTPの記事を取得。`ETag`は1234。
2.  利用者：BがHTTPの記事を取得。`ETag`は1234。
3.  利用者：AがHTTPの`ETag`を再度取得。先ほど取得した`ETag: 1234`と現在の`ETag: 1234`が一致。
4.  利用者：AがHTTPの記事を編集。`ETag`は1256になる。
5.  利用者：BがHTTPのETagを再度取得。先ほど取得した`ETag`と現在のETagはマッチせず。
6.  サーバは利用者：Bの書き込みを拒否。

<!-- end list -->

  - If-Modified-Since
    指定日時以降にオブジェクトが変更されている場合のみ、メソッドを実行するようにサーバに要求する。通信量の削減に効果がある。

<!-- end list -->

  - If-None-Match
    `If-Match`の逆で、ETagが一致しない場合のみの実行を要求する。

<!-- end list -->

  - If-Range
    クライアントがキャッシュにオブジェクトの一部分を持っている場合にパフォーマンスを向上できる。

<!-- end list -->

  - If-Unmodified-Since
    `If-Modified-Since`の逆で、指定時刻以降に変更がない場合のみの実行を要求する。

<!-- end list -->

  - Last-Modified
    レスポンスでオブジェクトの最終更新日時を示す。リクエスト時の`If-Modified-Since`ヘッダと組み合わせることで、効率的な通信が可能になる。

<!-- end list -->

  - Location
    サーバがクライアントにリダイレクト先URLを知らせる際に用いられる。一般的にステータスコードが3xx代のレスポンスと共に使われるが*201 Created*のレスポンスでも使うことができる。`Content-Location`ヘッダと名前が似ているが全く関係のない別のヘッダであるため注意。

<!-- end list -->

  - Max-Forwards
    プロキシサーバ等を経由する際の最大ホップ数を指定する。二重ループなどでサーバから応答が得られない場合の問題解決の際、`OPTION`メソッドや`TRACE`メソッドと共に用いられる。

## HTTPステータスコード

ステータスコードはサーバからのレスポンスで、リクエストの結果を通知する。3桁の数字から成り、おおまかな分類として、1xxは「情報」、2xxは「成功」、3xxは「リダイレクト」、4xxは「クライアントエラー」、5xxは「サーバエラー」を示す。

## セキュリティ技術

### Basic認証

HTTP/1.1で定義されている最も単純なセキュリティ技術である。「基本認証を用いるくらいならなにも使わない方がまし」と主張する人もいる\[12\]。[平文](https://ja.wikipedia.org/wiki/平文 "wikilink")で認証情報を送信する仕組みでおるため、TLS (HTTPS)など安全を確保した通信路での利用が望ましい。通常サーバはステータスコード401で応答する。

### Digest認証

## 関連項目

  - [HTTP/2](https://ja.wikipedia.org/wiki/HTTP/2 "wikilink")
  - [HTTPステータスコード](https://ja.wikipedia.org/wiki/HTTPステータスコード "wikilink")
  - [FTP](https://ja.wikipedia.org/wiki/File_Transfer_Protocol "wikilink")
  - [WebDAV](https://ja.wikipedia.org/wiki/WebDAV "wikilink")
  - [Webサーバ](https://ja.wikipedia.org/wiki/Webサーバ "wikilink")
  - [ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")
  - [アプリケーションサーバ](https://ja.wikipedia.org/wiki/アプリケーションサーバ "wikilink")
  - [Representational State Transfer](https://ja.wikipedia.org/wiki/Representational_State_Transfer "wikilink") (REST)
  - [HTTPヘッダ・インジェクション](https://ja.wikipedia.org/wiki/HTTPヘッダ・インジェクション "wikilink")
  - [Hyper Text Coffee Pot Control Protocol](https://ja.wikipedia.org/wiki/Hyper_Text_Coffee_Pot_Control_Protocol "wikilink")
  - [バーチャルホスト](https://ja.wikipedia.org/wiki/バーチャルホスト "wikilink")

## 参照

## 外部リンク

  - RFC 7540 - Hypertext Transfer Protocol Version 2 (HTTP/2)
  - RFC 7230 - Hypertext Transfer Protocol (HTTP/1.1): Message Syntax and Routing
      - [HTTP/1.1 — RFC 7230 〜 7235 — 日本語訳](https://triple-underscore.github.io/RFC723X-ja.html)
  - RFC 7231 - Hypertext Transfer Protocol (HTTP/1.1): Semantics and Content
  - RFC 7232 - Hypertext Transfer Protocol (HTTP/1.1): Conditional Requests
  - RFC 7233 - Hypertext Transfer Protocol (HTTP/1.1): Range Requests
  - RFC 7234 - Hypertext Transfer Protocol (HTTP/1.1): Caching
  - RFC 7235 - Hypertext Transfer Protocol (HTTP/1.1): Authentication
  - RFC 2818 - HTTP Over TLS
  - RFC 2817 - Upgrading to TLS Within HTTP/1.1
  - RFC 2616 - HTTP/1.1（RFC 2068の改訂版，RFC 7230 から RFC 7235 によって obsolete）
      - [ハイパーテキスト転送プロトコル -- HTTP/1.1](https://triple-underscore.github.io/RFC2616-ja.html)
  - RFC 2068 - HTTP/1.1（初版，RFC 2616 によって obsolete）
      - [TS X 0085:2004](http://www.y-adagio.com/public/standards/tr_http11_2068/toc.htm) - ハイパテキスト転送プロトコル HTTP/1.1 日本標準仕様書(TS X 0085:2004)
  - RFC 1945 - HTTP/1.0
  - [The HTTP Protocol As Implemented In W3](https://www.w3.org/Protocols/HTTP/AsImplemented.html) - HTTP/0.9

[Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:Hypertext_Transfer_Protocol](https://ja.wikipedia.org/wiki/Category:Hypertext_Transfer_Protocol "wikilink")

1.  [The HTTP Protocol As Implemented In W3](https://www.w3.org/Protocols/HTTP/AsImplemented.html)
2.
3.
4.
5.  [IETF Meetingの資料スライド](https://github.com/quicwg/wg-materials/tree/master/ietf103)
6.
7.
8.
9.
10. [Hypertext Transfer Protocol (HTTP) Method Registry](https://www.iana.org/assignments/http-methods/http-methods.xhtml)
11. [HTTP Content Coding Registry](https://www.iana.org/assignments/http-parameters/http-parameters.xhtml#content-coding)
12. 『HTTPプロトコル―セキュア&スケーラブルなWeb開発』 Stephen Thomas 著、葛西 重夫 訳、ソフトバンクパブリッシング