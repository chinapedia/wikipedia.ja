> この記事は[Java API for XML Processing](https://ja.wikipedia.org/wiki/Java_API_for_XML_Processing)から翻訳されています。


**Java API for XML Processing**（**JAXP**）は、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で[XMLを扱うための](../Page/Extensible_Markup_Language.md "wikilink")[APIのひとつ](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。XML文書の妥当性検証や[構文解析](../Page/構文解析.md "wikilink")のための[インタフェースを提供する](../Page/インタフェース_\(情報技術\).md "wikilink")。次の2つの基本的な構文解析インタフェースを備える。

  - [Document Object Modelによる構文解析インタフェース](../Page/Document_Object_Model.md "wikilink") (**DOM**インタフェース)
  - [Simple API for XMLによる構文解析インタフェース](../Page/Simple_API_for_XML.md "wikilink")（**SAX**インタフェース）

JAXP 1.4からは、3番目のインタフェースが追加されている。

  - [Streaming API for XMLによる構文解析インタフェース](https://ja.wikipedia.org/wiki/Streaming_API_for_XML "wikilink")（**StAX**インタフェース、JSR 173）

JAXPは、構文解析インタフェースに加え、XML文書のデータや構造の変換を行うための[XSLTインタフェースも提供している](../Page/XSL_Transformations.md "wikilink")。JAXPは、[Java Community Processの下でJSR](https://ja.wikipedia.org/wiki/Java_Community_Process "wikilink") 5（JAXP 1.0）、JSR 63（JAXP 1.1と1.2）、JSR 206（JAXP 1.3と1.4）として開発された。[2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink")現在の最新バージョンは1.4。[J2SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") 1.4以降はJAXPの実装を含むようになり、J2SE 5.0はJAXP 1.3の実装を、Java SE 6はJAXP1.4の実装を含んでいる。

## DOMインタフェース

おそらく最も理解しやすいのがDOMインタフェースであろう。XML文書全体を構文解析し、文書内のすべての要素に相当するメモリ内表現を、[Document Object Model(DOM) Level 2 Core Specification](http://www.w3.org/TR/2000/REC-DOM-Level-2-Core-20001113)で規定されたモデルに基づく[クラスで構築する](../Page/クラス_\(コンピュータ\).md "wikilink")。

DOMパーサー（構文解析機）は、メモリ上に`Document`表現を構築 (build) するので、`DocumentBuilder`と呼ばれる。は、により生成される。`DocumentBuilder`は、XML文書内の全ノードを含んだ[木構造の](../Page/木構造_\(データ構造\).md "wikilink")[インスタンス](../Page/インスタンス.md "wikilink")を生成する。木構造内の各ノードは、インタフェースを実装している。ノードには、XML文書内のデータ型を表すいろいろなノードタイプがある。最も重要なノードタイプとして、次のようなものがある。

  - 要素（element）ノード。属性（attribute）を持つ場合がある。
  - テキスト（text）ノード。要素の開始タグと終了タグの間に記述されたテキストを表す。

全ノードタイプの一覧は、[Javaパッケージ](../Page/パッケージ_\(Java\).md "wikilink")の[Javadoc](https://ja.wikipedia.org/wiki/Javadoc "wikilink")を参照のこと。

## SAXインタフェース

SAXパーサーはと呼ばれ、によって生成される。DOMパーサーと違い、SAXパーサーはメモリ内にXML文書の表現を作らないので、より高速でメモリ使用量が少ない。その代わりに、SAXパーサーは、[コールバックを呼び出す](https://ja.wikipedia.org/wiki/コールバック_\(情報工学\) "wikilink")、すなわち、あらかじめパーサーに渡しておいた[インスタンス](../Page/インスタンス.md "wikilink")の[メソッドを呼び出すことで](https://ja.wikipedia.org/wiki/メソッド_\(計算機科学\) "wikilink")、XML文書の構造を[クライアントに通知する](../Page/クライアントサイド.md "wikilink")。

`DefaultHandler`クラスは、、、の各インタフェースを実装している。ほとんどのクライアントは、`ContentHandler`インタフェースで定義されたメソッドを使うことになる。これらのメソッドは、XML文書内の対応する要素をSAXパーサーが見つけたときに呼び出される。SAXインタフェースの中でもっとも重要なメソッドとして、次のようなものがある。

  - `startDocument()`と`endDocument()`メソッド。XML文書の先頭と末尾で呼び出される。
  - `startElement()` and `endElement()`メソッド。要素の開始地点と終了地点で呼び出される。
  - `characters()`メソッド。要素の開始タグと終了タグの間にあるテキストデータで呼び出される。

クライアントは、`DefaultHandler`のサブクラスでこれらのメソッドを[オーバーライド](https://ja.wikipedia.org/wiki/オーバーライド "wikilink")してデータを処理する。処理の中でデータをデータベースに保存したり、ストリームに書き出したりすることもある。

## XSLTインタフェース

[XSLTは](../Page/XSL_Transformations.md "wikilink")、XML文書を別の形式のデータに変換できる。

[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")