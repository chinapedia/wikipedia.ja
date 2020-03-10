> この記事は[Internationalized Resource Identifier](https://ja.wikipedia.org/wiki/Internationalized_Resource_Identifier)から翻訳されています。


**Internationalized Resource Identifier**（**IRI**）とは、[Uniform Resource Identifier](../Page/Uniform_Resource_Identifier.md "wikilink") (URI) を拡張したものである（URI自身も [Uniform Resource Locator](../Page/Uniform_Resource_Locator.md "wikilink") (URL) を拡張したもの）。**国際化資源（リソース）識別子**とも。URI では[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")文字セットのサブセットに制限されていたが、IRI は [Universal Character Set](https://ja.wikipedia.org/wiki/ISO/IEC_10646 "wikilink") (Unicode/[ISO 10646](https://ja.wikipedia.org/wiki/ISO/IEC_10646 "wikilink")) を含むことができ、漢字、仮名文字、ハングル、キリル文字などを使うことができる。

RFC 3987 で定義されている。

## 利点

URI を多言語対応させることで、ラテンアルファベットに不案内なユーザーにもわかりやすくなり、[Unicode](../Page/Unicode.md "wikilink")の入力が難しくないと仮定すれば、[URIシステムへのアクセス可能性が広がる](../Page/Uniform_Resource_Identifier.md "wikilink")。

## 欠点

IRI と [ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink") の URI の混合は、実際には別のサイトであるにも関わらず、あるサイトにいるかのように錯覚させることができ、[フィッシング詐欺が容易になる](https://ja.wikipedia.org/wiki/フィッシング_\(詐欺\) "wikilink")。例えば、www.[ebay](https://ja.wikipedia.org/wiki/EBay "wikilink").com や www.[paypal](https://ja.wikipedia.org/wiki/PayPal "wikilink").com の "[a](https://ja.wikipedia.org/wiki/a "wikilink")" を見た目が似ていて異なる文字コードの文字([キリル文字](../Page/キリル文字.md "wikilink")の"[а](https://ja.wikipedia.org/wiki/а "wikilink")"など)に置換し、そのIRIを不正なサイトを指すように設定する。

現在の[キーボードでは](https://ja.wikipedia.org/wiki/キーボード_\(コンピュータ\) "wikilink")、他の言語のWebリソースへのアクセスは非常に難しい。逆に、[オープンソース](../Page/オープンソース.md "wikilink")のプログラム（それ以外も）はそのような問題を避けるため、[ラテン文字](../Page/ラテン文字.md "wikilink")のみで書かれることが多い。

## 関連項目

  - [XRI](../Page/Extensible_Resource_Identifier.md "wikilink") (Extensible Resource Identifier)
  - [国際化ドメイン名](../Page/国際化ドメイン名.md "wikilink") (IDN)
  - [Punycode](../Page/Punycode.md "wikilink")

## 外部リンク

  - [IRI](http://annevankesteren.nl/2005/02/iri)
  - [An Introduction to Multilingual Web Addresses](http://www.w3.org/International/articles/idn-and-iri/)

[Category:識別子](https://ja.wikipedia.org/wiki/Category:識別子 "wikilink") [Category:Uniform_Resource_Locator](https://ja.wikipedia.org/wiki/Category:Uniform_Resource_Locator "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")