> この記事は[Basic認証](https://ja.wikipedia.org/wiki/Basic認証)から翻訳されています。


**Basic認証**（ベーシックにんしょう、）とは、[HTTPで定義される](../Page/Hypertext_Transfer_Protocol.md "wikilink")[認証](../Page/認証.md "wikilink")方式の一つ。**基本認証**と呼ばれることも。

Basic認証では、ユーザ名と[パスワード](../Page/パスワード.md "wikilink")の組みを[コロン](../Page/コロン_\(記号\).md "wikilink") ":" でつなぎ、[Base64](../Page/Base64.md "wikilink")でエンコードして送信する。このため、盗聴や改竄が簡単であるという欠点を持つが、ほぼ全ての[Webサーバ](../Page/Webサーバ.md "wikilink")およびブラウザで対応しているため、広く使われている。

盗聴や改竄を防ぐため、後に[Digest認証](../Page/Digest認証.md "wikilink")というユーザ名とパスワードを[MD5](../Page/MD5.md "wikilink")でハッシュ化して送る方法が考えられた。

## 通信の流れ

典型的なBasic認証におけるHTTPクライアントとHTTPサーバの間の通信を紹介する。 だいたいの流れは以下のようになる。

1.  クライアントは認証が必要なページをリクエストする。しかし、通常ここではユーザ名とパスワードを送っていない。なぜならばクライアントはそのページが認証を必要とするか否かを知らないためである。
2.  サーバは401レスポンスコードを返し、認証領域 (authentication realm) や認証方式 (Basic認証) に関する情報をクライアントに知らせる。
3.  それを受けたクライアントは、認証領域（通常は、アクセスしているコンピュータやシステムの簡単な説明）をユーザに提示して、ユーザ名とパスワードの入力を求める。ユーザはここでキャンセルすることもできる。
4.  ユーザによりユーザ名とパスワードが入力されると、クライアントはリクエストに認証ヘッダを追加して再度送信する。
5.  認証に成功すると、サーバは認証の必要なページのリクエストを処理する。一方、ユーザ名やパスワードが間違っていた時には、サーバは再び401レスポンスコードを返す。それによりクライアントは再びユーザにユーザ名とパスワードの入力を求める。

## 例

以下に、認証に成功した場合の例を示す。（番号は上記「通信の流れ」と対応させてある）

**1.認証を伴わないリクエスト**:

``` http
GET /private/index.html HTTP/1.1
Host: example.com
```

**2.認証が必要であることを示すサーバのレスポンス**:

``` http
HTTP/1.1 401 Authorization Required
Date: Wed, 11 May 2005 07:50:26 GMT
Server: Apache/1.3.33 (Unix)
WWW-Authenticate: Basic realm="SECRET AREA"
Connection: close
Transfer-Encoding: chunked
Content-Type: text/html; charset=iso-8859-1

 (ここに人間が読めるエラーメッセージが入る)
```

**3.（クライアントによる提示、およびユーザによる入力）**:

`＜通信は行われない＞`

**4.認証を伴うリクエスト** (ユーザ名 "Aladdin"、パスワード "open sesame"):

``` http
GET /private/index.html HTTP/1.1
Host: example.com
Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ{{=}}{{=}}
```

**5.サーバのレスポンス**

``` http
HTTP/1.1 200 OK
Date: Wed, 11 May 2005 07:50:26 GMT
(以下略)
```

## 関連項目

  - [Base64](../Page/Base64.md "wikilink")
  - [Digest認証](../Page/Digest認証.md "wikilink")

## 外部リンク

  - RFC 7235 - Hypertext Transfer Protocol (HTTP/1.1): Authentication
  - RFC 7617 - The 'Basic' HTTP Authentication Scheme
  - 旧式となった規定
      - RFC 1945 - Hypertext Transfer Protocol -- HTTP/1.0
      - RFC 2616 - Hypertext Transfer Protocol -- HTTP/1.1
  - RFC 2617 - HTTP Authentication: Basic and Digest Access Authentication

[Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:Hypertext_Transfer_Protocol](https://ja.wikipedia.org/wiki/Category:Hypertext_Transfer_Protocol "wikilink")