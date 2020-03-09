> この記事は[Document Object Model](https://ja.wikipedia.org/wiki/Document_Object_Model)から翻訳されています。


**Document Object Model**（**DOM**、）は、マークアップがなされたリソース（**Document**）をリソース要素（**Object**）の木構造（**Model**）で表現し操作可能にする仕組み、またそのモデルである。

DOMは、[HTML文書や](https://ja.wikipedia.org/wiki/HyperText_Markup_Language "wikilink")[XML文書](../Page/Extensible_Markup_Language.md "wikilink")（あるいはより単純なマークアップされた文章など）をオブジェクトの木構造モデルで表現することで、ドキュメントをプログラムから操作・利用することを可能にする仕組みである\[1\]。Documentの種類、操作に用いるプログラミング言語の種類に依存しない仕様である\[2\]。

[WHATWG](https://ja.wikipedia.org/wiki/WHATWG "wikilink")がLiving Standardとして定義している。WHATWG以前は[W3Cが仕様を策定しており](../Page/World_Wide_Web_Consortium.md "wikilink")、Level 1からLevel 4まで勧告している。

XMLを読み込むAPIである[SAXと異なり](https://ja.wikipedia.org/wiki/Simple_API_for_XML "wikilink")、XMLデータを[ツリー構造](https://ja.wikipedia.org/wiki/ツリー構造 "wikilink")として扱う事ができる。ただし、通常の場合対象のXML文書を全て読み込んでからの扱いを前提とするため、動作速度が遅かったり、メモリーの使用量が大きくなるといった欠点もある。

DOMの実装は各メーカーに委ねられており、DOMを実装した[XMLパーサ](https://ja.wikipedia.org/wiki/XMLパーサ "wikilink")が各メーカーから提供されている。

## 概要

DOMは、マークアップがなされたリソース（**Document**）をリソース要素（**Object**）の木構造（**Model**）で表現し操作可能にする。

### 対象: Document

DOMはDocument（**マークアップがなされた**あらゆるリソース: 日記から論文、インタラクティブなWebアプリまで）を対象とする\[3\]。マークアップとは文章（例: \`これは文章です\`）の一部を意味づけしたり構造を示したりするために付与される文字列であり（例: \`<主語>これは</主語><述語>文章です</述語>\`）、すなわちDOMはマークアップによる構造をもったリソースを対象としている。

### 表現: Object木モデル

DOMはDocumentをObjectの木構造として表現する。Document内にはマークアップによって区切られるまとまりがあり、各まとまりを特定種の**オブジェクト**で表現する（例: <主語>これは</主語> = 主語オブジェクト)。DOMにおいてオブジェクトは総称して***Node***と呼ばれる\[4\]。Nodesは入れ子構造をとるため、これを木構造（親Nodeと子Nodeの入れ子構造）でモデル化できる。このようにDOMはマークアップされたまとまり/オブジェクトの木構造モデルによってドキュメントを表現する。

### 例

以下はDOMを説明する文章に、各部分が意味する内容をマークアップしたものである。

``` html
<!--マークアップがなされたリソース-->
<タイトル>DOMとはなにか</タイトル>
<本文><1行概要>DOMとはドキュメントをオブジェクトの木構造を示したものである。</1行概要><詳細>すなわちマークアップがなされたリソースを要素オブジェクトの入れ子構造でモデル化したものである。オブジェクトの例として<リスト>Element</リスト><リスト>Text</リスト><リスト>Comment</リスト>が挙げられる。</詳細></本文>
```

このDocumentを木構造として表現すると以下のようになる。

``` html
<!--木構造で表現されたリソース-->
<タイトル>DOMとはなにか</タイトル>
<本文>
    <1行概要>
        DOMとはドキュメントをオブジェクトの木構造を示したものである。
    </1行概要>
    <詳細>
        すなわちマークアップがなされたリソースを要素オブジェクトの入れ子構造でモデル化したものである。
        オブジェクトの例として
        <リスト>Element</リスト>
        <リスト>Text</リスト>
        <リスト>Comment</リスト>
        が挙げられる。
    </詳細>
</本文>
```

さらに各要素をObjectとして表現することでDOMのnode tree表現が以下のように得られる。 [代替文=DOM node tree](https://ja.wikipedia.org/wiki/ファイル:Nodetree.png "wikilink") nodeはプログラムからアクセス可能なオブジェクトであり、このDOMで定義されるnode treeを操作することでDocumentをプログラムから操作できる。例えば新しいnodeを追加したり、特定のnodeを検索して内容を得たりする（一行概要のTextを取得する）ことが可能になる。

## 他技術との関係

DOMはその起源からしてHTMLをはじめとする[Web技術との関わりが非常に深い](https://ja.wikipedia.org/wiki/Webプログラミング "wikilink")。現在ではより一般化された"ドキュメント"を木構造として扱う仕様として定義されている。

### HTML

[HTMLは](https://ja.wikipedia.org/wiki/HyperText_Markup_Language "wikilink")「ハイパーテキスト**マークアップ**言語」の名が示す通り[マークアップされたリソースであり](https://ja.wikipedia.org/wiki/マークアップ言語 "wikilink")、DOMの対象ドキュメントとして扱える。[WebブラウザはDOMを実装することでHTMLを解釈](../Page/ウェブブラウザ.md "wikilink")・表示し、またJavaScript等のプログラミング言語からの操作を可能にしている。

一方あくまでDOMはHTMLと切り離された仕様である。<button>などの[HTML要素](https://ja.wikipedia.org/wiki/HTML要素 "wikilink")は**HTML仕様で**その振る舞い（click可能という振る舞いなど）や属性等を含むDOM Interfaceが定義されている。DOM仕様は個別要素の振る舞いには一切ふれず、Objectをどう木構造として扱うかのみを定義している。

### JavaScript

DOMの目的の1つはドキュメントを[プログラムから解釈](https://ja.wikipedia.org/wiki/プログラム_\(コンピュータ\) "wikilink")・操作可能にすることである。[JavaScript](../Page/JavaScript.md "wikilink")が[Webブラウザ用スクリプト言語として誕生した背景から](../Page/ウェブブラウザ.md "wikilink")、JavaScriptとDOMには密接な関係がある\[5\]。WebブラウザはDOMを実装し`document`オブジェクトなどを介することで、JavaScriptに対してDOMへのアクセスを提供している。いわゆる[WebアプリはHTMLで書かれたドキュメントをDOMによって操作可能にしJavaScriptでアプリケーションとしての動作を実現している](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")。

一方あくまでDOMはJavaScript（ECMAScript）と切り離された仕様である。JavaScriptは[Node.js](https://ja.wikipedia.org/wiki/Node.js "wikilink")をはじめとした非ブラウザ（DOM非存在下）で完全に動作し、実際に広く利用されている。JavaScriptの視点からみたDOMの操作は、単なる`document`objectの操作であり、JavaScript仕様におけるObjectの操作に過ぎない。またDOMはあくまで言語に依存しないinterface仕様であり、実際にJavaScript以外の言語によるDOMの操作がおこなわれている。

## 仕様

2019年現在、DOMの仕様はWHATWG DOM Living Standardによって管理・改訂されている。

### WHATWG DOM Living Standard

最新のDOMを定義している仕様である。node tree（"The DOM"）に関わる仕様のみではなく、DOM Event等の仕様もDOM Living Standardで定義されている。

  - [DOM Living Standard](https://dom.spec.whatwg.org/)
      - [DOM Standard （“DOM4”） 日本語訳](https://triple-underscore.github.io/DOM4-ja.html)

### W3C勧告

W3Cによって、Level 1からLevel 4まで勧告されており、XML文書を扱う「Core」、HTML文書を扱う「HTML」等のモジュールに分かれている。

また、正式な仕様ではないが、Level 1 以前からある各ブラウザの独自実装を DOM Level 0 と呼称する場合がある\[6\]。

#### Level 1

  - [Document Object Model (DOM) Level 1 Specification](http://www.w3.org/TR/REC-DOM-Level-1/) ([日本語訳](http://www.doraneko.org/misc/dom10/19981001/cover.html))
      - [XML](../Page/Extensible_Markup_Language.md "wikilink") 1.0を扱う基本的メソッド「Core」と、[HTML](https://ja.wikipedia.org/wiki/HyperText_Markup_Language "wikilink") 4.0xに関する「HTML」からなる。

#### Level 2

  - [Document Object Model (DOM) Level 2 Core Specification](http://www.w3.org/TR/DOM-Level-2-Core/)
      - [XML](../Page/Extensible_Markup_Language.md "wikilink") 1.0を扱う基本的メソッドと、名前空間に関する拡張
  - [Document Object Model (DOM) Level 2 HTML Specification](http://www.w3.org/TR/DOM-Level-2-HTML/)
      - [HTML](https://ja.wikipedia.org/wiki/HyperText_Markup_Language "wikilink") 4.0xに関する拡張と、[XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink") 1.0のサポート
  - [Document Object Model (DOM) Level 2 Views Specification](http://www.w3.org/TR/DOM-Level-2-Views/)
      - [ビュー](../Page/ビュー.md "wikilink")に関する拡張
  - [Document Object Model (DOM) Level 2 Style Specification](http://www.w3.org/TR/DOM-Level-2-Style/)
      - [スタイルシート](https://ja.wikipedia.org/wiki/スタイルシート "wikilink")（[CSS及びCSS](../Page/Cascading_Style_Sheets.md "wikilink") Level2）に関する拡張
  - [Document Object Model (DOM) Level 2 Events Specification](http://www.w3.org/TR/DOM-Level-2-Events/)
      - [イベント](https://ja.wikipedia.org/wiki/イベント_\(プログラミング\) "wikilink")（[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")イベント、[マウスイベント](https://ja.wikipedia.org/wiki/マウス_\(コンピュータ\) "wikilink")、DOMツリーの変化に伴うイベント、HTML 4.01のイベント）に関する拡張
  - [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://www.w3.org/TR/DOM-Level-2-Traversal-Range/)
      - DOMツリーの横断と、DOMツリーの操作範囲に関する拡張

#### Level 3

  - [Document Object Model (DOM) Level 3 Core Specification](http://www.w3.org/TR/DOM-Level-3-Core/)
      - [XML](../Page/Extensible_Markup_Language.md "wikilink") 1.0を扱う基本的メソッドと、名前空間に関する拡張。
  - [Document Object Model (DOM) Level 3 Load and Save Specification](http://www.w3.org/TR/DOM-Level-3-LS/)
      - DOMツリーの読み書き
  - [Document Object Model (DOM) Level 3 Validation Specification](http://www.w3.org/TR/DOM-Level-3-Val/)
      - DOMツリーに含まれるスキーマ定義の編集

#### Level 4

DOM Level 4は、すでに活動を開始していたWHAWG DOM Living Standardの当時の版のスナップショットと言えるものである。

  - [W3C DOM4](https://www.w3.org/TR/2015/REC-dom-20151119/)

## 参照

## 関連

  - [SAX](https://ja.wikipedia.org/wiki/Simple_API_for_XML "wikilink")
  - [ダイナミックHTML](https://ja.wikipedia.org/wiki/ダイナミックHTML "wikilink")

## 外部リンク

  - [Document Object Model (DOM) Specifications](http://www.w3.org/DOM/DOMTR) - W3C
  - [DOM について](http://www.mozilla-japan.org/docs/dom/about/)
  - [Gecko DOM Reference](http://www.mozilla.org/docs/dom/domref/)
  - [DOM Central](http://devedge.netscape.com/central/dom/) - Netscape DevEdge

[Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:構文解析_(プログラミング)](https://ja.wikipedia.org/wiki/Category:構文解析_\(プログラミング\) "wikilink") [Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:HTML](https://ja.wikipedia.org/wiki/Category:HTML "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")

1.  APIと言われることが多いが、一応APIではない。Document Object Model (DOM) Level 1 Specification
2.  Abstract. DOM defines a platform-neutral model for events, aborting activities, and node trees. [DOM Living Standard.](https://dom.spec.whatwg.org/)
3.  In this specification, the term "document" is used for any markup-based resource, ranging from short static documents to long essays or reports with rich multimedia, as well as to fully-fledged interactive applications. [DOM Living Standard](https://dom.spec.whatwg.org/#introduction-to-the-dom)
4.  `Document`, `DocumentType`, `DocumentFragment`, `Element`, `Text`, `ProcessingInstruction`, and `Comment` objects (simply called <dfn>nodes</dfn>) participate in a tree, [DOM Living Standard](https://dom.spec.whatwg.org/#concept-node)
5.  初期には JavaScript と DOM は強く結びついていましたが、最終的には別々の存在ととして発展しました。 [DOM の紹介 - DOM と JavaScript. MDN Web Docs](https://developer.mozilla.org/ja/docs/Web/API/Document_Object_Model/Introduction#DOM_and_JavaScript)
6.  山田祥寛『JavaScript 本格入門』P.254