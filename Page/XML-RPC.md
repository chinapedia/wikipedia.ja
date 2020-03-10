> この記事は[XML-RPC](https://ja.wikipedia.org/wiki/XML-RPC)から翻訳されています。


**XML-RPC**とは、[遠隔手続き呼出し](https://ja.wikipedia.org/wiki/遠隔手続き呼出し "wikilink") (RPC) プロトコルの一種であり、エンコード（符号化）に[XMLを採用し](../Page/Extensible_Markup_Language.md "wikilink")、転送機構に[HTTPを採用している](../Page/Hypertext_Transfer_Protocol.md "wikilink")。非常に単純なプロトコルで、少数の[データ型](https://ja.wikipedia.org/wiki/データ型 "wikilink")やコマンドだけを定義しているだけであり、その仕様は2枚の紙にまとめられる。これは多くのRPCシステムが膨大な量の規格を規定し、実装に多量のプログラミングを要することに比べると、際立った特徴と言える。

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")、ユーザーランド・ソフトウェアが[マイクロソフト](../Page/マイクロソフト.md "wikilink")と共同で開発した。その後、これに新たな機能を追加したものが[SOAPへと発展した](../Page/SOAP_\(プロトコル\).md "wikilink")。しかし、SOAP よりも単純で扱いやすいXML-RPCを好む人もいる。

類似の RPCプロトコルとして [JSON-RPC](https://ja.wikipedia.org/wiki/JSON-RPC "wikilink") がある。

## データ型

<table>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>タグ使用例</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>array</p></td>
<td><p><array><br />
<code>  </code><data><br />
<code>    </code><value><i4><code>1404</code></i4></value><br />
<code>    </code><value><string><code>Something here</code></string></value><br />
<code>    </code><value><i4><code>1</code></i4></value><br />
<code>  </code></data><br />
</array></p></td>
<td><p>値の配列。キーは格納しない。</p></td>
</tr>
<tr class="even">
<td><p>base64</p></td>
<td><p><base64><code>eW91IGNhbid0IHJlYWQgdGhpcyE=</code></base64></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Base64" title="wikilink">Base64</a>でエンコードされたバイナリデータ</p></td>
</tr>
<tr class="odd">
<td><p>boolean</p></td>
<td><p><boolean><code>1</code></boolean></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ブーリアン型" title="wikilink">ブーリアン型</a>の論理値（0または1）</p></td>
</tr>
<tr class="even">
<td><p>date/time</p></td>
<td><p><code>&lt;dateTime.iso8601&gt;19980717T14:08:55&lt;/dateTime.iso8601&gt;</code></p></td>
<td><p>日付と時刻</p></td>
</tr>
<tr class="odd">
<td><p>double</p></td>
<td><p><double><code>-12.53</code></double></p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/倍精度" title="wikilink">倍精度</a><a href="../Page/浮動小数点数.md" title="wikilink">浮動小数点数</a></p></td>
</tr>
<tr class="even">
<td><p>integer</p></td>
<td><p><i4><code>42</code></i4></p>
<p>または</p>
<p><int><code>42</code></int></p></td>
<td><p><a href="../Page/整数.md" title="wikilink">整数</a></p></td>
</tr>
<tr class="odd">
<td><p>string</p></td>
<td><p><string><code>Hello world!</code></string></p></td>
<td><p>文字列。<a href="../Page/Extensible_Markup_Language.md" title="wikilink">XMLのエンコード規則に従う</a>。</p></td>
</tr>
<tr class="even">
<td><p>struct</p></td>
<td><p><struct><br />
<code>  </code><member><br />
<code>    </code><name><code>foo</code></name><br />
<code>    </code><value><i4><code>1</code></i4></value><br />
<code>  </code></member><br />
<code>  </code><member><br />
<code>    </code><name><code>bar</code></name><br />
<code>    </code><value><i4><code>2</code></i4></value><br />
<code>  </code></member><br />
</struct></p></td>
<td><p>キーを含む値の配列。</p></td>
</tr>
<tr class="odd">
<td><p>nil</p></td>
<td><p><nil/></p></td>
<td><p>NULL値の識別用。XML-RPC の<a href="http://ontosys.com/xml-rpc/extensions.php">拡張</a></p></td>
</tr>
</tbody>
</table>

## 例

XML-RPC要求の典型例を以下に示す。

<?xml version="1.0"?>

<methodCall>
`  `<methodName>`examples.getStateName`</methodName>
`  `<params>
`    `<param>
`        `<value><i4>`40`</i4></value>
`    `</param>
`  `</params>
</methodCall>

XML-RPC応答の典型例を以下に示す。

<?xml version="1.0"?>

<methodResponse>
`  `<params>
`    `<param>
`        `<value><string>`South Dakota`</string></value>
`    `</param>
`  `</params>
</methodResponse>

XML-RPCフォールトの典型例を以下に示す。

<?xml version="1.0"?>

<methodResponse>
`  `<fault>
`    `<value>
`      `<struct>
`        `<member>
`          `<name>`faultCode`</name>
`          `<value><int>`4`</int></value>
`        `</member>
`        `<member>
`          `<name>`faultString`</name>
`          `<value><string>`Too many parameters.`</string></value>
`        `</member>
`      `</struct>
`    `</value>
`  `</fault>
</methodResponse>

## 関連項目

  - [Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")
  - [ソフトウェアコンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")
  - [OPML](https://ja.wikipedia.org/wiki/OPML "wikilink")
  - [Webサービス](https://ja.wikipedia.org/wiki/Webサービス "wikilink")
  - [WDDX](https://ja.wikipedia.org/wiki/WDDX "wikilink")

## 外部リンク

  - [XML-RPC Homepage](http://www.xmlrpc.com/)
  - [Forum](http://groups.yahoo.com/group/xml-rpc/)
  - [Tutorials](http://www.xml.com/pub/rg/XML_RPC_Tutorials)
  - [Technology Reports](http://xml.coverpages.org/xml-rpc.html)
  - [Citations from CiteSeer](http://citeseer.org/cs?q=XML+and+RPC)
  - [XEP-0009: Jabber-RPC](http://xmpp.org/extensions/xep-0009.html) [XMPPプロトコル上のXML](https://ja.wikipedia.org/wiki/Extensible_Messaging_and_Presence_Protocol "wikilink")-RPC
  - [pyJabberXMLRPC](http://gdr.geekhood.net/gdrwpl/jxmlrpc.php): Python用（Jabber上のXML-RPC）
  - [Secure Apache XML-RPC](http://members.fortunecity.com/neptune42/xmlrpc/index.htm)
  - [RemObjects SDK](http://www.remobjects.com/ro) [SOAPなどへのXML](../Page/SOAP_\(プロトコル\).md "wikilink")-RPC対応
  - [RealThinClient SDK](http://www.realthinclient.com): Delphi/C++用
  - [XML-RPC in Flash ActionScript 2.0](http://xmlrpcflash.mattism.com)
  - [XML-RPC.NET](http://www.xml-rpc.net): .NET用
  - [Redstone XML-PRC Library](http://xmlrpc.sourceforge.net/) Java用オープンソースライブラリ

[Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:遠隔手続き呼出し](https://ja.wikipedia.org/wiki/Category:遠隔手続き呼出し "wikilink") [Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink")