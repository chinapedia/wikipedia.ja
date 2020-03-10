> この記事は[Web Server Gateway Interface](https://ja.wikipedia.org/wiki/Web_Server_Gateway_Interface)から翻訳されています。


**Web Server Gateway Interface (WSGI; ウィスキー)** は、プログラミング言語[Python](../Page/Python.md "wikilink")において、[Webサーバ](../Page/Webサーバ.md "wikilink")と[Webアプリケーション](https://ja.wikipedia.org/wiki/Webアプリケーション "wikilink")（もしくは[Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")）を接続するための、標準化された[インタフェース定義である](../Page/インタフェース_\(情報技術\).md "wikilink")。また、WSGIから着想を得て、他の言語でも同様のインタフェースが作られた。

## 基本的な発想

過去において、Pythonに多種の[Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")が存在することは、PythonでWebアプリケーションを開発しようとする者にとって問題になっていた。というのも、Webアプリケーションフレームワークを選択することによって、使用できる[Webサーバ](../Page/Webサーバ.md "wikilink")が制限されてしまったり、その逆の制限が発生したりしたためである。Pythonで書かれたWebアプリケーションは、FastCGI, mod_python, CGI, さらにはWebサーバ独自のAPIを使ったものなど、様々な方法で実装されていた。

この問題を解決するためにWSGIが考案された。WSGIは、Pythonにおける、WebアプリケーションとWebサーバを接続する標準仕様を定めるものであり、これによって、WSGIに対応したWebアプリケーション（やフレームワーク）は、WSGIに対応した任意のWebサーバ上で運用できるようになる。つまり、アプリケーション側がWSGIに対応していれば、アプリケーションのコードに修正を加えることなく、WSGI対応サーバを自由に選択することができ、高い[可搬性](https://ja.wikipedia.org/wiki/可搬性 "wikilink")（ポータビリティ）が得られる。

## 仕様の概要

WSGIには二つの側 — サーバ側とアプリケーション側が存在する。WSGIは、リクエスト情報・レスポンスヘッダ・レスポンス本文を、両者の間でどのようにやりとりするかをPythonのAPIとして定義している。

Webサーバにリクエストが来ると、次のような流れでやりとりが行なわれる：

1.  サーバ側が、クライアントからリクエストを受ける。
2.  サーバ側は、アプリケーション側がエントリポイントとして提供するcallableオブジェクト（関数やクラスインスタンスなど `__call__` が定義されたオブジェクト）を呼び出して、その引数として環境変数と1つのコールバック用callableオブジェクトを渡す。
3.  アプリケーション側は、このコールバック用callableオブジェクトを呼び出すことでステータスコードとレスポンスヘッダをサーバ側に伝え、さらに本文を生成するiterableオブジェクト（イテレータやリストなど）を戻り値として返す。
4.  サーバ側は、これらを用いてクライアントへのレスポンスを生成する。

WSGIは[ミドルウェア](https://ja.wikipedia.org/wiki/ミドルウェア "wikilink")の考え方も提供できる。WSGIミドルウェアは、サーバ側とアプリケーション側のWSGIインタフェースを実装しているため、WSGIサーバとWSGIアプリケーションの"中間に"挿入できる。ミドルウェアはサーバーの視点からはアプリケーションとして振る舞い、アプリケーションの視点からはサーバーとして振る舞う。

"ミドルウェア"は、例えば以下のような機能を提供できる:

  - 目標の URL にもとづき、[環境変数](https://ja.wikipedia.org/wiki/環境変数 "wikilink")を適宜変更し、リクエストを別のアプリケーションのオブジェクトに回送する
  - 複数のアプリケーション（やフレームワーク）が同じ[プロセス](../Page/プロセス.md "wikilink")の中に同居して動作できるようにする
  - リクエストとレスポンスをネットワーク上で転送することによる[負荷分散と遠隔処理](../Page/サーバロードバランス.md "wikilink")
  - コンテンツの後処理の実行 — XSLスタイルシートを適用するなど

## WSGIアプリケーションの例

既存のWSGI対応フレームワークを使用する場合は意識する必要はないが、ゼロからWSGIアプリケーションを作る場合は以下の例（[Hello Worldアプリケーション](https://ja.wikipedia.org/wiki/Hello_World "wikilink")）のようにする：

``` python
def application(environ, start_response):
    start_response('200 OK', [('Content-Type', 'text/plain')])
    yield b'Hello World\n'
```

解説:

  - WSGIアプリケーションは、callableオブジェクト (`__call__`が定義されたオブジェクト) として定義する（この例では `application` 関数）。このオブジェクトが呼び出される際、引数 `environ` としてCGIと同様の環境変数が渡され、引数 `start_response` として、ステータスコードとレスポンスヘッダを受け取るcallableオブジェクトが渡される。
  - `start_response` を呼び出して、ステータスコードとレスポンスヘッダを設定する。
  - WSGIアプリケーションの戻り値は、本文を生成するiteratableオブジェクトである必要がある。この例ではPythonのジェネレータ機能を使ってそれを実現している。

## WSGI 互換のWebアプリケーションフレームワーク

WSGIをサポートする[Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")は多数存在する。その一例を示す:

  - [BlueBream](https://ja.wikipedia.org/wiki/BlueBream "wikilink")
  - [Bottle](https://ja.wikipedia.org/wiki/Bottle "wikilink")
  - [CherryPy](https://ja.wikipedia.org/wiki/CherryPy "wikilink")
  - [Django](../Page/Django.md "wikilink")
  - [Flask](https://ja.wikipedia.org/wiki/Flask "wikilink")
  - [Google App Engine](https://ja.wikipedia.org/wiki/Google_App_Engine "wikilink")
  - [Pylons](../Page/Pylons.md "wikilink")
  - [Pyramid](https://ja.wikipedia.org/wiki/Pyramid "wikilink")
  - [Tornado](https://ja.wikipedia.org/wiki/Tornado_HTTP_Server "wikilink") ([www.tornadoweb.org](http://www.tornadoweb.org/))
  - [Trac](../Page/Trac.md "wikilink") ([trac.edgewall.org](http://trac.edgewall.org/))
  - [TurboGears](../Page/TurboGears.md "wikilink")
  - [web.py](https://ja.wikipedia.org/wiki/web.py "wikilink") [1](http://webpy.org/)
  - [web2py](https://ja.wikipedia.org/wiki/web2py "wikilink")
  - [Werkzeug](https://ja.wikipedia.org/wiki/Werkzeug "wikilink")
  - [Zope](../Page/Zope.md "wikilink") (バージョン3以降)

## WSGI対応サーバ

WSGIサーバ（WSGIアプリケーションコンテナ）は、WSGIアプリケーションを常駐させ、[HTTPクライアントからリクエストを受け取るごとに](../Page/Hypertext_Transfer_Protocol.md "wikilink")、WSGIアプリケーションのcallableオブジェクトを呼び出す。これによって、クライアントからのリクエストがアプリケーションに転送される。

WSGIアプリケーションコンテナの例としては、[uWSGI](https://ja.wikipedia.org/wiki/uWSGI "wikilink"), [Gunicorn](https://ja.wikipedia.org/wiki/Gunicorn "wikilink"), [Apache](https://ja.wikipedia.org/wiki/Apache "wikilink")モジュール ([mod_wsgi](https://ja.wikipedia.org/wiki/mod_wsgi "wikilink"), [mod_python](https://ja.wikipedia.org/wiki/mod_python "wikilink")など), [Microsoft IIS](../Page/Internet_Information_Services.md "wikilink")（[isapi-wsgi](http://code.google.com/p/isapi-wsgi/), [PyISAPIe](http://pyisapie.sourceforge.net/), [ASPゲートウェイを使用](../Page/Active_Server_Pages.md "wikilink")）などがある。

さらに、WSGIアプリケーションをラップすることで、[FastCGI](https://ja.wikipedia.org/wiki/FastCGI "wikilink")や[SCGI](https://ja.wikipedia.org/wiki/SCGI "wikilink")環境で動作させることもできるし、古典的な[CGIとして動作させることもできる](../Page/Common_Gateway_Interface.md "wikilink")（例えば、Python標準ライブラリに含まれる`wsgiref.handlers.CGIHandler`が利用できる）。

## 他のプログラミング言語への影響

WSGIから着想を得て、他のプログラミング言語にも同様のインターフェイスが作られた。以下はその一例である。

  - [PSGI](https://ja.wikipedia.org/wiki/PSGI "wikilink") ([Perl](../Page/Perl.md "wikilink") Web Server Gateway Interface)
  - [Rack](https://ja.wikipedia.org/wiki/Rack "wikilink") ([Ruby](../Page/Ruby.md "wikilink") Web Server Interface)
  - [SCGI](https://ja.wikipedia.org/wiki/SCGI "wikilink")
  - [Ring](https://ja.wikipedia.org/wiki/Ring "wikilink") ([Clojure](https://ja.wikipedia.org/wiki/Clojure "wikilink"))
  - [WAI](https://hackage.haskell.org/package/wai) ([Haskell](../Page/Haskell.md "wikilink"), Web Application Interface)

## WSGIとPython 3

Python 3において文字列とバイト列が分離されたことはWSGIにとって問題となった。HTTPヘッダのデータはテキストとして扱われたりバイナリとして扱われたりするが、WSGIはヘッダデータを文字列として扱っている。Python 2ではテキストもバイナリも「文字列」として扱っていたためこれで問題がなかったが、Python 3ではバイナリはbytes型で扱うことになり、「文字列」とはUnicode文字列のことを表すようになった。この問題に対処した更新版のWSGI仕様は、PEP 3333として公開されている。

再考されたWSGI仕様として [Web3](https://ja.wikipedia.org/wiki/Web3 "wikilink") というものも提案されており、こちらはPEP 444 として公開されている。Web3は、互換性のないWSGIの派生であり、Python 2.6以降および3.1以降で動作するように設計されている。

## 外部リンク

  - [PEP 333 -- Python Web Server Gateway Interface v1.0](https://www.python.org/dev/peps/pep-0333/) インターフェイス標準の最初の定義(英語)
  - [PEP 333: Python Web Server Gateway Interface v1.0](https://knzm.readthedocs.io/en/latest/pep-0333-ja.html) (日本語訳)
  - [PEP 3333 -- Python Web Server Gateway Interface v1.0.1](https://www.python.org/dev/peps/pep-3333/) インターフェイス標準の定義(英語)
  - [PEP 3333: Python Web Server Gateway Interface v1.0.1](https://knzm.readthedocs.io/en/latest/pep-3333-ja.html) (日本語訳)
  - [WSGI のすべてにわたる分かりやすい wiki(英語)](http://wsgi.org/)

[Category:Python](https://ja.wikipedia.org/wiki/Category:Python "wikilink") [Category:ウェブ技術](https://ja.wikipedia.org/wiki/Category:ウェブ技術 "wikilink")