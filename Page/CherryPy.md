> この記事は[CherryPy](https://ja.wikipedia.org/wiki/CherryPy)から翻訳されています。


**CherryPy** は、[Python](../Page/Python.md "wikilink")プログラミング言語を用いた[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")の[Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")である。

[HTTPプロトコルを](../Page/Hypertext_Transfer_Protocol.md "wikilink")[(Adapterで)ラップすることによる](https://ja.wikipedia.org/wiki/デザインパターン "wikilink")[Webアプリケーション](https://ja.wikipedia.org/wiki/Webアプリケーション "wikilink")の[素早い開発を目的として設計されている](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")。しかし、低レベルの位置にとどまり、[RFC](../Page/Request_for_Comments.md "wikilink")[2616](http://www.faqs.org/rfcs/rfc2616.html)で定義されている以上の機能は提供しない。

CherryPy は Web サーバそのものとして動作することもでき、また([Apache](../Page/Apache_HTTP_Server.md "wikilink") 2 などを含む)[WSGI環境であれば](../Page/Web_Server_Gateway_Interface.md "wikilink")、外部から起動させることもできる。CherryPy は、出力を表示させるためのテンプレートや、バックエンドへのアクセス、認証プロトコルなどの処理は行わない。フレームワークは、7つの関数をもつ簡潔な[インタフェースからなるフィルターによって拡張可能である](../Page/インタフェース_\(情報技術\).md "wikilink")。これらは、リクエスト/レスポンス処理中の定義された場所で呼び出される。

## Python インターフェイス

プロジェクトの創設者[Remi Delonの目的の一つが](https://ja.wikipedia.org/wiki/Remi_Delon "wikilink")、CherryPy を可能な限り[Pythonらしくすることであった](https://ja.wikipedia.org/wiki/pythonic "wikilink")。これにより開発者がこのフレームワークを標準の Python モジュールとして使用することができ、（技術的な観点からは）アプリケーションが web 用であることを忘れることができる。

たとえば、よくある [Hello World](https://ja.wikipedia.org/wiki/Hello_World "wikilink") は CherryPy 3 では以下のようになる:

``` python
import cherrypy

class HelloWorld(object):
    def index(self):
        return "Hello World!"
    index.exposed = True

cherrypy.quickstart(HelloWorld())
```

## 関連書籍

  - *[CherryPy Essentials: Rapid Python Web Application Development](http://www.cherrypyessentials.com/)*, First Edition (March 2007), ISBN 978-1-904811-84-8

## 関連項目

  - [CherryTemplate](https://ja.wikipedia.org/wiki/CherryTemplate "wikilink") - CherryPy 向けのテンプレート言語
  - [TurboGears](../Page/TurboGears.md "wikilink") - CherryPy は TurboGears の主要コンポーネントである

## 外部リンク

  - [CherryPy website](http://cherrypy.org)
  - [Documentation](http://cherrypy.org/wiki/TableOfContents)
  - [Feeds about CherryPy](http://planet.cherrypy.org/)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink") [Category:Python](https://ja.wikipedia.org/wiki/Category:Python "wikilink") [Category:ウェブアプリケーション](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーション "wikilink")