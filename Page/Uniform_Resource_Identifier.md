> この記事は[Uniform Resource Identifier](https://ja.wikipedia.org/wiki/Uniform_Resource_Identifier)から翻訳されています。


**Uniform Resource Identifier**（ユニフォーム リソース アイデンティファイア、**URI**）または**統一資源識別子**\[1\]（とういつしげんしきべつし）は、一定の書式によって[リソース](https://ja.wikipedia.org/wiki/リソース_\(WWW\) "wikilink")（資源）を指し示す[識別子](../Page/識別子.md "wikilink")。[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")8月に RFC 2396 として規定され、[2005年](../Page/2005年.md "wikilink")1月に RFC 3986 として改定された。URI は[Uniform Resource Locator](../Page/Uniform_Resource_Locator.md "wikilink") (URL) の考え方を拡張したものである。

URI は [http](../Page/Hypertext_Transfer_Protocol.md "wikilink")/[https](../Page/HTTPS.md "wikilink") や [ftp](../Page/File_Transfer_Protocol.md "wikilink") などのスキームで始まり、コロン (:) による区切りのあとにスキームごとに定義された書式によってリソースを示す。また、URIによって示されるリソースはコンピュータが扱うデータに限らず、人や会社、書籍などを示すことも可能である。

URIスキームは[IANAによって登録されたものが公式なものとされている](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")。その一方で、 [javascript](../Page/JavaScript.md "wikilink") のように未登録ではあるが広く使われているスキームも存在する。

## URL と URN

[URI_Venn_Diagram.svg](https://ja.wikipedia.org/wiki/File:URI_Venn_Diagram.svg "fig:URI_Venn_Diagram.svg") URI には、以下の2つのサブセットがある。

  - [Uniform Resource Locator](../Page/Uniform_Resource_Locator.md "wikilink") (URL)
    リソースの「場所」を識別する。ネットワーク内の位置を示してリソースを同定する。
  - [Uniform Resource Name](https://ja.wikipedia.org/wiki/Uniform_Resource_Name "wikilink") (URN)
    リソースの「名前」を識別する。もしネットワーク上にリソースが無くなっても、一意で永続的な識別を行えるようにする。例えば <urn:ietf:rfc:2648> というURNは、RFC 2648への参照を示す。

2001年、[W3CはRFC](../Page/World_Wide_Web_Consortium.md "wikilink") 3305\[2\]内で、上記の考え方を古典的な見解とした。ここで示されたW3Cの新たな考え方により、従来のURLとURNとはすべてURIと呼ばれることになった。URLやURNといった語はW3Cによって非公式な表現とされた。

2012年、[WHATWG](https://ja.wikipedia.org/wiki/WHATWG "wikilink")によって[URL Standard](https://url.spec.whatwg.org/)の開発が開始された。URL Standardでは、目標の1つとしてRFC 3986 (URI)とRFC 3987 (IRI)を過去のものにすることを掲げている\[3\]\[4\]。また、従来のURIやIRIを区別する必要が無いとして、すべてURLの語を用いている。さらに、W3Cでも、このURL Standardのスナップショットをワーキンググループノートとして公開している。

## 関連項目

  - [Extensible Resource Identifier](../Page/Extensible_Resource_Identifier.md "wikilink") (XRI)
  - [Internationalized Resource Identifier](../Page/Internationalized_Resource_Identifier.md "wikilink") (IRI)
  - [短縮URI](https://ja.wikipedia.org/wiki/短縮URI "wikilink") (CURIE)
  - [Uniform Resource Locator](../Page/Uniform_Resource_Locator.md "wikilink") (URL)
  - [Uniform Resource Name](https://ja.wikipedia.org/wiki/Uniform_Resource_Name "wikilink") (URN)
  - [名前空間](../Page/名前空間.md "wikilink")
  - [パーセントエンコーディング](../Page/パーセントエンコーディング.md "wikilink")

## 参考資料

  - RFC 2396 - Uniform Resource Identifiers (URI): Generic Syntax (旧)
      - [TS X 0097:2004](http://www.y-adagio.com/public/standards/tr_uri_2396/rfc2396-toc.htm) - 統一資源識別子(URI) 共通構文 標準仕様書(TS)
  - RFC 3986 - Uniform Resource Identifier (URI): Generic Syntax
  - RFC 7320 - URI Design and Ownership
  - [URL Standard](https://url.spec.whatwg.org/)
      - [URL Standard 日本語訳](https://triple-underscore.github.io/URL-ja.html)
      - [URL W3C Working Group Note](https://www.w3.org/TR/url/)
  - [URI Schemes](https://www.iana.org/assignments/uri-schemes/uri-schemes.xhtml) - [IANAのURIスキーム登録簿](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")

## 脚注

[Category:識別子](https://ja.wikipedia.org/wiki/Category:識別子 "wikilink") [Category:Uniform_Resource_Locator](https://ja.wikipedia.org/wiki/Category:Uniform_Resource_Locator "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.   9頁
2.  RFC 3305 - [URIs, URLs, and URNs: Clarifications and Recommendations 1.0](http://www.w3.org/TR/2001/NOTE-uri-clarification-20010921/)
3.
4.