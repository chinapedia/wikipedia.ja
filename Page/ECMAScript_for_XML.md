> この記事は[ECMAScript for XML](https://ja.wikipedia.org/wiki/ECMAScript_for_XML)から翻訳されています。


**ECMAScript for XML**（**E4X**）は、[ECMAScript](../Page/ECMAScript.md "wikilink")（[ActionScript](../Page/ActionScript.md "wikilink")、[DMDScript](https://ja.wikipedia.org/wiki/DMDScript "wikilink")、[JavaScript](../Page/JavaScript.md "wikilink")、[JScript](../Page/JScript.md "wikilink") を含む）にネイティブの[XMLサポートを追加するプログラミング言語拡張である](../Page/Extensible_Markup_Language.md "wikilink")。その目的は、[DOMインタフェースの代替として](../Page/Document_Object_Model.md "wikilink")、単純な構文でXML文書にアクセスできるインタフェースを提供することである。E4Xがリリースされるまで、XMLへのアクセスには常にオブジェクトレベルが関与していた。E4XではXMLを文字や整数と同様の[プリミティブ型](../Page/プリミティブ型.md "wikilink")として扱う。そのため、アクセスが高速化され、サポートが容易になり、プログラムの構成要素（データ構造）としても扱いやすくなる。

E4Xは[Ecmaインターナショナル](../Page/Ecmaインターナショナル.md "wikilink")がとして標準化した。初版は2004年6月に公表され、第2版が2005年12月に公表された。

## 例

`var sales = `<sales vendor="John">
`    `<item type="peas" price="4" quantity="6"/>
`    `<item type="carrot" price="3" quantity="10"/>
`    `<item type="chips" price="5" quantity="3"/>
`  `</sales>`;`
` `
`alert( sales.item.(@type == "carrot").@quantity );`
`alert( sales.@vendor );`
`for each( var price in sales..@price ) {`
`  alert( price );`
`}`

## 実装

最初の実装は Terry Lucas と John Schneider が設計したもので、2002年2月にリリースされた[BEAシステムズ](../Page/BEAシステムズ.md "wikilink")の Weblogic Workshop 7.0 に含まれていた。BEAの実装は [Rhino](../Page/Rhino.md "wikilink") に基づくもので、E4X の標準化が完了する以前にリリースされている。リリース時、John Schneider は BEA の XML 拡張について[記事](https://web.archive.org/web/20080704153702/http://dev2dev.bea.com/pub/a/2002/09/JSchneider_XML.html)を書いた。E4X言語以前のリファレンス文書が現在も公開されている[1](http://e-docs.bea.com/workshop/docs70/help/guide/xmlmap/conHandlingXMLWithECMAScriptExtensions.html)。

E4Xは、[SpiderMonkey](https://ja.wikipedia.org/wiki/SpiderMonkey "wikilink")（[Gecko](../Page/Gecko.md "wikilink")の[JavaScriptエンジン](https://ja.wikipedia.org/wiki/JavaScriptエンジン "wikilink")）や Rhino（同じくMozilla用にJavaで書かれたJavaScriptエンジン）で実装されている。

[Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink") は Gecko ベースなので、E4X を使ったスクリプトを実行可能であった（バージョン1.5以降）が、Firefox 17から段階的に無効化され、同21で削除される予定である。\[1\]。なお、Firefox 1.5 で正しくスクリプトを実行するには、スクリプトの *type* 属性の最後に "`; e4x=1`" を追加する必要がある（例えば、<tt>

<script type="application/javascript; e4x=1">

</tt>）。

アドビの [ActionScript](../Page/ActionScript.md "wikilink") 3 でも E4X を完全サポートしている。これが公式にリリースされたのは、2006年の [Adobe Flex](https://ja.wikipedia.org/wiki/Adobe_Flex "wikilink") 2.0 と [Flash Player](../Page/Adobe_Flash.md "wikilink") 9 の一部としてである。他に、Flash CS3、[Adobe AIR](https://ja.wikipedia.org/wiki/Adobe_Integrated_Runtime "wikilink")、[Adobe Acrobat](../Page/Adobe_Acrobat.md "wikilink")/Reader（8.0以降）でもサポートされている。

[Aptana](../Page/Aptana.md "wikilink")の Jaxer Ajax アプリケーションサーバは、Mozilla のエンジンをサーバ側で使っているため、E4X に対応している。

[コンテンツ管理システム](../Page/コンテンツ管理システム.md "wikilink") (CMS) の [Alfresco](https://ja.wikipedia.org/wiki/Alfresco "wikilink") Community Edition 2.9B でも E4X をサポートしている。

## 批判

多くのE4X実装は、DOMノードとE4Xモデルの間で、インポート/エクスポートする手段を提供していない。

## 競合規格

### JSON

[JSONは](../Page/JavaScript_Object_Notation.md "wikilink") XML の代替となる可能性がある。JSON は XML に似たオブジェクト指向のデータ記述言語である。JSON は[ECMAScript](../Page/ECMAScript.md "wikilink")標準の一部であり、全ての標準に準拠した JavaScript エンジンで使える。E4X に比較するとクエリ機能が若干貧弱と言われている。これは、E4Xが1つのオブジェクトに複数のインデックスを付けられるのに対して、JSONでは1つのインデックスしか付けられないためである。

上掲の例を JSON を使った場合、次のようになる。

`var sales = {"vendor":"John","items":[`
`  {"type":"peas","price":"4","quantity":"6"},`
`  {"type":"carrot","price":"3","quantity":"10"},`
`  {"type":"chips","price":"5","quantity":"3"} ]};`
` `
`for( var i in sales.items) { if (sales.items[i].type=="carrot") alert( sales.items[i].quantity ); }`
`alert( sales.vendor );`
`for( var i in sales.items ) { alert( sales.items[i].price ); }`

## 脚注

## 外部リンク

  - [ECMA-357 ECMAScript for XML (E4X) Specification](https://www.ecma-international.org/publications/files/ECMA-ST-WITHDRAWN/Ecma-357.pdf)、[日本語試訳](http://www.ne.jp/asahi/nanto/moon/specs/ecma-357.html)
  - [Slides from 2005 E4X Presentation](http://developer.mozilla.org/presentations/xtech2005/e4x/) by [Brendan Eich](https://ja.wikipedia.org/wiki/ブレンダン・アイク "wikilink"), Mozilla Chief Architect
  - [E4X](https://developer.mozilla.org/en-US/docs/Archive/Web/E4X) at [Mozilla Developer Center](https://ja.wikipedia.org/wiki/Mozilla_Developer_Center "wikilink")。[日本語版](https://developer.mozilla.org/ja/docs/E4X)
  - [Introducing E4X](https://www.xml.com/pub/a/2007/11/28/introducing-e4x.html) at xml.com、E4X と JSON の比較
  - [Processing XML with E4X](https://developer.mozilla.org/en-US/docs/Archive/Web/E4X/Processing_XML_with_E4X) at Mozilla Developer Center

[Category:JavaScript](https://ja.wikipedia.org/wiki/Category:JavaScript "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:Ecma](https://ja.wikipedia.org/wiki/Category:Ecma "wikilink")

1.  [E4X | MDN](https://developer.mozilla.org/ja/docs/E4X)