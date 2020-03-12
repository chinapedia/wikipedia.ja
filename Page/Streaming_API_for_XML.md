> この記事は[Streaming API for XML](https://ja.wikipedia.org/wiki/Streaming_API_for_XML)から翻訳されています。


**Streaming API for XML**（**StAX**）は、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で[XML文書を読み書きするための](../Page/Extensible_Markup_Language.md "wikilink")[APIである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

従来のXML APIは、次のどちらかである。

  - ツリーベース - 文書全体がツリー構造でメモリに読み込まれ、呼び出し元アプリケーションはランダムアクセスできる。
  - イベントベース - 文書内に出現したエンティティごとに、登録されたアプリケーションがイベントを受け取る。

これらはそれぞれに利点がある。前者（例えば[DOM](../Page/Document_Object_Model.md "wikilink")）は文書へのランダムアクセスが可能であり、後者（例えば[SAX](../Page/Simple_API_for_XML.md "wikilink")）は使用メモリが少なくより高速に動作する場合が多い。

この2つは対極に位置するアクセス手法であると言える。ツリーベースのAPIは制約のないランダムアクセスとデータの操作が可能である一方、イベントベースのAPIは文書を1回スキャンするだけである。

StAXは、その中間の手法として設計された。StAXの考え方では、プログラムの操作点は文書内のある地点を指すカーソルである。アプリケーションがカーソルを進めるということは、必要に応じて自分がパーサーから情報を取り出すことになる（pull型）。これはSAXのようなイベントベースのAPIとは異なる。SAXではパーサーがアプリケーションにデータを送りつけるので（push型）、アプリケーション側が文書内の位置を追跡しなければならない場合は必要に応じてイベントとイベントの間で状態を保持しておく必要がある。

## 起源

StAXは、互換性のない多数のpull型XML APIにその起源を持つ。これらAPIのうち最も有名なXMLPULLの作者（Stefan HausteinとAleksandr Slominski）と、その他のAPIの作者である[BEAシステムズ](../Page/BEAシステムズ.md "wikilink")や[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")、[サン](../Page/サン・マイクロシステムズ.md "wikilink")、[Breeze Factor](http://www.breezefactor.com/)、[ジェームズ・クラークの協働により誕生した](../Page/ジェームズ・クラーク_\(ソフトウェア技術者\).md "wikilink")。

## 例

JSR-173の最終仕様、V1.0より（フェアユースに基づき使用）

以下、引用:

  -
    下記のJava APIは、カーソルの手法でXMLを読むための主要なメソッドである。

<code>

>
>
>     // Java
>     public interface XMLStreamReader {
>       public int next() throws XMLStreamException;
>       public boolean hasNext() throws XMLStreamException;
>       public String getText();
>       public String getLocalName();
>       public String getNamespaceURI();
>       // ...以下のメソッドは省略
>     }

</code>

  -
    書き込み用のAPIは、イベントベースのAPIにおける“StartElement”と“EndElement”に対応するメソッドを持っている。

<code>

>
>
>     // Java
>     public interface XMLStreamWriter {
>       public void writeStartElement(String localName) throws XMLStreamException;
>       public void writeEndElement() throws XMLStreamException;
>       public void writeCharacters(String text) throws XMLStreamException;
>       // ...以下のメソッドは省略
>     }

</code>

  -
    5.3.1 XMLStreamReader
    この例では、InputFactoryをどのようにインスタンス化し、Readerを生成してXML文書中の要素を繰り返し処理するかを示す。

<code>

>
>
>     XMLInputFactory f = XMLInputFactory.newInstance();
>     XMLStreamReader r = f.createXMLStreamReader(... );
>     while (r.hasNext()) {
>         r.next();
>     }

</code>

## 実装

  - <http://stax.codehaus.org/> リファレンス実装
  - [Woodstox](http://woodstox.codehaus.org) オープンソースのStAX実装
  - <https://sjsxp.dev.java.net> サンのStAX実装

## 関連項目

JavaでXMLを構文解析するための他の方法としては、以下のものがある。

  - [VTD-XML](https://ja.wikipedia.org/wiki/VTD-XML "wikilink") ランダムアクセスと[XPathをサポートする新しい非抽出型XML処理モデル](../Page/XML_Path_Language.md "wikilink")
  - [DOM](../Page/Document_Object_Model.md "wikilink") Document Object Model
  - [JAXB](../Page/Java_Architecture_for_XML_Binding.md "wikilink") Java XML Binding API
  - [SAX](../Page/Simple_API_for_XML.md "wikilink") push方式のXML API
  - [Javolution](https://ja.wikipedia.org/wiki/Javolution "wikilink") は、StAXに似たリアルタイムの[実装](http://www.javolution.org/api/javolution/xml/stream/package-summary.html)を提供する。（Stringといった）オブジェクトを生成せずに済み、メモリ使用量やガベージコレクションにも悪影響がない（注: 普通のStAX実装でオブジェクトの生成を減らすためには、ルックアップテーブルを用意して頻繁に使用されるStringオブジェクトを取り出し、再利用する必要がある）。

[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")