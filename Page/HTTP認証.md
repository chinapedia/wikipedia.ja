> この記事は[HTTP認証](https://ja.wikipedia.org/wiki/HTTP認証)から翻訳されています。


**HTTP認証**とは、[HTTPの通信の中で](../Page/Hypertext_Transfer_Protocol.md "wikilink")[認証](../Page/認証.md "wikilink")を行うことである。オリジンまたは[プロキシ](../Page/プロキシ.md "wikilink")サーバーに対して[認証](../Page/認証.md "wikilink")を行う枠組みがで規定されており、通常これを用いることをHTTP認証という。

## ステータス・レスポンス

このRFCでは、以下のものが追加で定義されている。

  - オリジンとの認証処理
      - ステータスコード401 Unauthorized
      - HTTPレスポンスヘッダーWWW-Authenticate
      - HTTPリクエストヘッダーAuthorization
  - プロキシサーバーとの認証処理
      - ステータスコード407 Proxy Authentication Required
      - HTTPレスポンスヘッダーProxy-Authenticate
      - HTTPリクエストヘッダーProxy-Authorization

なお、認証は通ったものの、[アクセス制御](../Page/アクセス制御.md "wikilink")として対象の[リソースへのアクセスが許可されていない場合は](https://ja.wikipedia.org/wiki/リソース_\(WWW\) "wikilink")、応答として[403 Forbiddenを用いる](https://ja.wikipedia.org/wiki/HTTP_403 "wikilink")。

## 認証スキーム

前述のリクエストヘッダー・レスポンスヘッダーの上で、様々な認証方式を使用できる。個々の認証方式を認証スキーム(authentication scheme)と呼ぶ。

例えば以下のような認証スキームが存在する。

  - Basic
    [Basic認証](../Page/Basic認証.md "wikilink")。
  - Digest
    [Digest認証](../Page/Digest認証.md "wikilink")。
  - Bearer
    [Bearerトークン](https://ja.wikipedia.org/wiki/Bearerトークン "wikilink")を用いるベアラー認証。
  - Negotiate
    ネゴシエート認証。による。で規定。

認証スキームは[IANAが](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")[Hypertext Transfer Protocol (HTTP) Authentication Scheme Registry](https://www.iana.org/assignments/http-authschemes/http-authschemes.xhtml)として管理している。一方で、NTLM\[1\]やAWS4-HMAC-SHA256\[2\]のように登録されずに使われているものもある。

## 関連項目

  - [Basic認証](../Page/Basic認証.md "wikilink")
  - [Digest認証](../Page/Digest認証.md "wikilink")

## 脚注

## 外部リンク

  - : Hypertext Transfer Protocol (HTTP/1.1): Authentication

  - [Hypertext Transfer Protocol (HTTP) Authentication Scheme Registry](https://www.iana.org/assignments/http-authschemes/http-authschemes.xhtml)

  - [HTTP 認証 - HTTP | MDN](https://developer.mozilla.org/ja/docs/Web/HTTP/Authentication)

[Category:Hypertext_Transfer_Protocol](https://ja.wikipedia.org/wiki/Category:Hypertext_Transfer_Protocol "wikilink") [Category:認証技術](https://ja.wikipedia.org/wiki/Category:認証技術 "wikilink") [Category:ウェブ技術](https://ja.wikipedia.org/wiki/Category:ウェブ技術 "wikilink")

1.  [\[MS-NTHT\]: NTLM Over HTTP Protocol](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-ntht/f09cf6e1-529e-403b-a8a5-7368ee096a6a)
2.  [署名バージョン 4 を使用してAWS リクエストに署名する - AWS 全般のリファレンス](https://docs.aws.amazon.com/ja_jp/general/latest/gr/sigv4_signing.html)