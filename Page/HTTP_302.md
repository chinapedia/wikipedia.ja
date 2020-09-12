> この記事は[HTTP 302](https://ja.wikipedia.org/wiki/HTTP_302)から翻訳されています。


**[HTTPレスポンス](../Page/Hypertext_Transfer_Protocol.md "wikilink")[ステータスコード](../Page/HTTPステータスコード.md "wikilink")302Found**は、 [URLリダイレクトを実行する一般的な方法](../Page/リダイレクト_\(HTTP\).md "wikilink")。 HTTP/1.0 仕様 (RFC 1945) は当初このコードを定義し、「Found」ではなく「Moved Temporarily」という説明文を与えていた。

このステータスコードを含むHTTP応答は、ヘッダーフィールドロケーションに[URLを追加で提供する](../Page/Uniform_Resource_Locator.md "wikilink")。これは、[ユーザーエージェント](../Page/ユーザーエージェント.md "wikilink")(例えばWebブラウザ)に対して、ロケーションフィールドで指定された新しいURLへの2回目のリクエストを行うように招待するものである。最終的には、新しいURLへのリダイレクトが行われる。

多くのWebブラウザーは本来であるべきリクエストのタイプをGETに変更するなどの標準に違反する方法で実装した\[1\]。このため、HTTP / 1.1（ RFC 2616)は新しいステータスコード303と[307を追加することによって](../Page/HTTPステータスコード.md "wikilink")2つの動作を明確にし、303は要求タイプの変更をGETに義務付け、307は最初に送信されたままの要求タイプを保持するようにしている。この曖昧性の解消によって明確化されたにもかかわらず、HTTP/1.1 仕様を実装していないブラウザとの互換性を維持するために302フレームワークは302は依然ウェブフレームワークで採用されている\[2\]。

## 例

クライアントのリクエスト：

``` http numberLines
GET /index.html HTTP/1.1
Host: www.example.com
```

サーバーの応答：

``` http numberLines
HTTP/1.1 302 Found
Location: http://www.iana.org/domains/example/
```

## 関連項目

  - [HTTPステータスコード](../Page/HTTPステータスコード.md "wikilink")

## 参考文献

[Category:HTTPステータスコード](https://ja.wikipedia.org/wiki/Category:HTTPステータスコード "wikilink") [Category:Hypertext_Transfer_Protocol](https://ja.wikipedia.org/wiki/Category:Hypertext_Transfer_Protocol "wikilink")

1.
2.