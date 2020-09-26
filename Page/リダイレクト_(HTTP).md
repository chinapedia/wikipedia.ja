> この記事は[リダイレクト \(HTTP\)](https://ja.wikipedia.org/wiki/リダイレクト_\(HTTP\))から翻訳されています。


ウェブサイトにおける**リダイレクト**（）とは、[ウェブサイト](../Page/ウェブサイト.md "wikilink")の閲覧において、指定した[ウェブページ](../Page/ウェブページ.md "wikilink")から自動的に他のウェブページに転送されること。**URLリダイレクト**（URL redirection）とも言われる。

通常はウェブページの[URL](https://ja.wikipedia.org/wiki/URL "wikilink")が変わったときに、元のURLから新しいURLへ誘導するときに用いられる。[フィッシング詐欺サイトへの誘導などで用いられている場合もある](../Page/フィッシング_\(詐欺\).md "wikilink")。

## HTTPリダイレクト

HTTPヘッダにある[HTTPステータスコード](../Page/HTTPステータスコード.md "wikilink")にてリダイレクトの種類を伝え、Location:ヘッダで移動先を伝える。種類には301 Moved Permanently（恒久的な移転）や302 Found（発見）などがある。[Webサーバ](../Page/Webサーバ.md "wikilink")の設定ファイル（[Apacheの場合](../Page/Apache_HTTP_Server.md "wikilink")、httpd.confファイルや[.htaccess](../Page/.htaccess.md "wikilink")ファイル）や、[CGIなどで指定できる](../Page/Common_Gateway_Interface.md "wikilink")。

## metaタグによるリダイレクト

HTML文書の head要素内に meta要素の http-equiv属性の値に "refresh" を記述する。content属性で文書を読み込んでから何秒後に転送させるかを指定する。HTTPステータスコードはリダイレクトなしで直接アクセスした場合と同様のコードが返される。

  - metaタグ記述例

    ``` html
    <meta http-equiv="Refresh" content="3; url=http://www.example.com/">
    ```

    と設定すると、3秒後に`http://www.example.com/`へ自動転送される。

    content="3"の3の部分が転送までの時間を意味する。

  - クローラーの解釈
    各種検索サイトのクローラーの解釈は，それぞれ異なるので注意が必要である。0秒の場合、[Yahoo\! JAPANの場合は](../Page/Yahoo!_JAPAN.md "wikilink")301リダイレクト（永久的なリダイレクト）と扱われる\[1\] 。[Google検索](https://ja.wikipedia.org/wiki/Google検索 "wikilink")の場合はサーバサイドで301リダイレクトの使用を奨めている\[2\]。

## クライアントスクリプトによるリダイレクト

[JavaScript](../Page/JavaScript.md "wikilink")等の[クライアントスクリプトを用いて](../Page/クライアント_\(コンピュータ\).md "wikilink")、自動でページ遷移する処理を記述することで、転送をする方法。locationまたはlocation.hrefへの代入などの方法がある\[3\]。

セキュリティなどの理由でスクリプトの実行を許可していない[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")では、転送されない。また、HTTPレスポンスではリダイレクトなしで直接アクセスした場合と同様のステータスコードが返されるため、検索エンジンなどの[クローラ](../Page/クローラ.md "wikilink")に移転したことが伝わらない場合もある。

## 目的

## 実装

## サービス

## セキュリティ上の問題

## 関連項目

  - [リンク腐敗](../Page/リンク切れ.md "wikilink")

## 参考文献

## 外部リンク

  - [ファイルシステムの場所へのURLのマッピング](http://httpd.apache.org/docs/1.3/urlmapping.html)
  - [JavaScriptリダイレクトスパムの分類](http://www2007.org/workshops/paper_115.pdf) （Microsoft Live Labs）
  - [URLリダイレクタ](http://projects.webappsec.org/URL-Redirector-Abuse)の[セキュリティ脆弱性](http://projects.webappsec.org/URL-Redirector-Abuse) Webアプリケーションセキュリティコンソーシアムの脅威の分類

[Category:インターネット用語](https://ja.wikipedia.org/wiki/Category:インターネット用語 "wikilink") [Category:インターネット検索](https://ja.wikipedia.org/wiki/Category:インターネット検索 "wikilink") [Category:Uniform_Resource_Locator](https://ja.wikipedia.org/wiki/Category:Uniform_Resource_Locator "wikilink")

1.
2.
3.