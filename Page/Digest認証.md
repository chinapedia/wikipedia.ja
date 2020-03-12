> この記事は[Digest](https://ja.wikipedia.org/wiki/Digest)から翻訳されています。


**Digest認証**（ダイジェストにんしょう）とは、HTTPの認証方法の一つ。ユーザ名と[パスワード](../Page/パスワード.md "wikilink")を[MD5](../Page/MD5.md "wikilink")でハッシュ（ダイジェスト）化して送る。[Basic認証](../Page/Basic認証.md "wikilink")では防げなかった[盗聴](../Page/盗聴.md "wikilink")や[改竄](../Page/改竄.md "wikilink")を防ぐために考案された。

## 例

典型的なDigest認証におけるHTTPクライアントとHTTPサーバの間の通信を紹介する。

だいたいの流れは以下のようになる。

1.  クライアントは認証が必要なページをリクエストする。しかし、通常ここではユーザ名とパスワードを送っていない。なぜならばクライアントはそのページが認証を必要とするか否かを知らないためである。
2.  サーバは401レスポンスコードを返し、認証領域 (realm) や認証方式（Digest）に関する情報をクライアントに返す。このとき、[ランダム](../Page/ランダム.md "wikilink")な文字列（[nonce](https://ja.wikipedia.org/wiki/nonce "wikilink")）も返される。
3.  それを受けたクライアントは、認証領域（通常は、アクセスしているサーバやシステムなどの簡単な説明）をユーザに提示して、ユーザ名とパスワードの入力を求める。ユーザはここでキャンセルすることもできる。
4.  ユーザによりユーザ名とパスワードが入力されると、クライアントはnonceとは別のランダムな文字列（cnonce）を生成する。そして、ユーザ名とパスワードとこれら2つのランダムな文字列などを使ってハッシュ文字列（response）を生成する。
5.  クライアントはサーバから送られた認証に関する情報とともに、ユーザ名とresponseをサーバに送信する。
6.  サーバ側では、クライアントから送られてきたランダムな文字列（nonce、cnonce）などとサーバに格納されているハッシュ化されたパスワードから、正解のハッシュを計算する。
7.  この計算値とクライアントから送られてきたresponseとが一致する場合は、認証が成功し、サーバはコンテンツを返す。不一致の場合は再び401レスポンスコードが返され、それによりクライアントは再びユーザにユーザ名とパスワードの入力を求める。

ユーザ名とパスワードの具体的な計算は以下のようになる。なお、ここでは認証[アルゴリズム](../Page/アルゴリズム.md "wikilink")が[MD5](../Page/MD5.md "wikilink")の時の計算方法を示す。

**クライアントが計算するresponseは以下のようにして求められる**：

`A1 = ユーザ名 ":" realm ":" パスワード`
`A2 = HTTPのメソッド ":" コンテンツの`[`URI`](https://ja.wikipedia.org/wiki/URI "wikilink")
`response = MD5( MD5(A1) ":" nonce ":" nc ":" cnonce ":" qop ":" MD5(A2) )`

**サーバ側では、**MD5(A1) をあらかじめ計算し格納してある。nonce,nc,cnonce,qopとHTTPのメソッド（GETなど）とコンテンツのURIはクライアントから送られてくるので、サーバ側でもresponseの正解を計算できる。

## 関連項目

  - [Basic認証](../Page/Basic認証.md "wikilink")
  - [MD5](../Page/MD5.md "wikilink")

## 外部リンク

  - RFC 7616 - HTTP Digest Access Authentication
  - 旧式となった規定
      - RFC 2069 - An Extension to HTTP: Digest Access Authentication
      - RFC 2617 - HTTP Authentication: Basic and Digest Access Authentication
  - RFC 3310 - Hypertext Transfer Protocol (HTTP) Digest Authentication Using Authentication and Key Agreement (AKA)

[Category:Hypertext_Transfer_Protocol](https://ja.wikipedia.org/wiki/Category:Hypertext_Transfer_Protocol "wikilink") [Category:暗号化プロトコル](https://ja.wikipedia.org/wiki/Category:暗号化プロトコル "wikilink") [Category:ハッシュ関数](https://ja.wikipedia.org/wiki/Category:ハッシュ関数 "wikilink")