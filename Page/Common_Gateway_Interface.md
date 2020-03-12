> この記事は[Common Gateway Interface](https://ja.wikipedia.org/wiki/Common_Gateway_Interface)から翻訳されています。


**Common Gateway Interface**（コモン・ゲートウェイ・インタフェース、**CGI**）は、[ウェブサーバ上でユーザ](../Page/Webサーバ.md "wikilink")[プログラムを動作させるための仕組み](../Page/プログラム_\(コンピュータ\).md "wikilink")。現存する多くのウェブサーバプログラムはCGIの機能を利用することができる。

ウェブサーバプログラムの機能の主体は、あらかじめ用意された情報を利用者（[クライアント](../Page/クライアント_\(コンピュータ\).md "wikilink")）の要求に応じて送り返すことである。そのためサーバプログラム単体では情報をその場で動的に生成してクライアントに送信するような仕組みを作ることはできなかった。 そこでサーバプログラムから他のプログラムを呼び出し、その処理結果をクライアントに送信する方法が考案された。それを実現するためのサーバプログラムと外部プログラムとの連携法の取り決めが CGI である。

CGI は環境変数や標準入出力の扱える[プログラミング言語](../Page/プログラミング言語.md "wikilink")で扱うことができる。

代表的なアプリケーションには、[電子掲示板](../Page/電子掲示板.md "wikilink")、[アクセスカウンタ](https://ja.wikipedia.org/wiki/アクセスカウンタ "wikilink")、[ウィキ](../Page/ウィキ.md "wikilink")や[ブログ](../Page/ブログ.md "wikilink")システムなどがある。

## 仕様

CGI の仕様は[NCSA](https://ja.wikipedia.org/wiki/NCSA "wikilink")により最初に定義・実装（[NCSA HTTPdにおいて](../Page/NCSA_HTTPd.md "wikilink")）され、現在の最新版はCGI1.1である。[2004年](../Page/2004年.md "wikilink")にRFC 3875となった。

CGI は、典型的には以下のような動作を期待される。CGIを経由して実行されるプログラムのことを、**CGIプログラム**と呼ぶ。

  - CGIプログラムはウェブサーバがクライアントからのリクエストに応じて起動する。
      -
        典型的には、ウェブサーバの公開領域に置かれたプログラムに対応する[URIへのリクエストがあると](../Page/Uniform_Resource_Identifier.md "wikilink")、サーバはそのCGIプログラムをCGIの取り決めに従って呼び出す。
  - CGIプログラムへの情報の入力は、コマンドライン[引数](../Page/引数.md "wikilink")、[環境変数](../Page/環境変数.md "wikilink")、[標準入力](https://ja.wikipedia.org/wiki/標準入力 "wikilink")によって行われる。
      - ウェブサーバがCGIプログラムを呼び出す時点でいくつかの環境変数を定義することが定められている。
      - 特に、クライアントがサーバに要求したURIのうち、検索文字列(Query String)部が環境変数 `QUERY_STRING` に設定されるので、これは[HTMLフォームからGETメソッドで入力を受けるのに便利である](../Page/HyperText_Markup_Language.md "wikilink")。
      - `QUERY_STRING` に文字「`=`」が含まれない場合は、サーバは `QUERY_STRING` の内容をコマンドライン引数としてCGIプログラムに渡す。これはHTMLの`ISINDEX`要素を用いて送信された情報を扱うのに便利である。
      - クライアントからのHTTPリクエストのボディ部はCGIプログラム標準入力に流し込まれる。また、その入力の長さが環境変数 `CONTENT_LENGTH` に設定されている。これはHTMLフォームから `POST` メソッドで入力を受けるのに便利である。
      - CGIプログラムに対応する仮想パスの後に、更に余分のパスが続いた場合、その情報は環境変数 `PATH_INFO` に格納され `PATH_INFO` をウェブサーバの仮想パスと解釈した際に対応すべき物理パスが環境変数 `PATH_TRANSLATED` に格納される。この方式もまたCGIプログラムにユーザー側からパラメータを渡す目的でよく用いられる。
  - プログラムが[標準出力](https://ja.wikipedia.org/wiki/標準出力 "wikilink")に出力したデータは、ウェブサーバを経由してクライアントに送られる。このデータは正当な[HTTPヘッダで始まらなければならない](https://ja.wikipedia.org/wiki/Hypertext_Transfer_Protocol#HTTPヘッダフィールド "wikilink")。
  - ただし、いくつかの特別なヘッダフィールドは「サーバディレクティブ」として解釈され、ウェブサーバの挙動（ステータスコードなど）に影響を与える。これ以外の全てのヘッダフィールドはそのままクライアントに送信される。

現在のウェブではHTMLが中心的な役割を果たしているので、CGIプログラムはHTMLを出力するケースが圧倒的に多い。

  - 画像データなどを出力することもある（これは[アクセスカウンタ](https://ja.wikipedia.org/wiki/アクセスカウンタ "wikilink")などを作る際に使われる）。

## CGI以外の手法

近年では、ウェブサーバから外部のプログラムを呼び出すという負荷の大きい動作を避け、ウェブサーバの一部として[インタプリタ](../Page/インタプリタ.md "wikilink")を常時起動させておくことにより性能を向上させた [mod_perlや](../Page/Perl.md "wikilink")、[PSGI](https://ja.wikipedia.org/wiki/PSGI "wikilink")([Perl](../Page/Perl.md "wikilink"))、[mod_php](../Page/PHP_\(プログラミング言語\).md "wikilink")、[FastCGI](https://ja.wikipedia.org/wiki/FastCGI "wikilink")、[WSGI](../Page/Web_Server_Gateway_Interface.md "wikilink")([Python](../Page/Python.md "wikilink")) などのインタフェース・実装が一般的である。

このため、比較的新しいウェブサーバアプリケーションでは、CGIを直接動作させる機能を持たないものも存在する。

  - [Nginx](https://ja.wikipedia.org/wiki/Nginx "wikilink"): [FCGI Wrap](https://www.nginx.com/resources/wiki/start/topics/examples/fcgiwrap/)により、FastCGIとして動作させる。
  - h2o: [fastcgi-cgi](https://h2o.examp1e.net/configure/cgi.html)により、FastCGIとして動作させる。
  - OpenBSD httpd: [slowcgi](https://man.openbsd.org/slowcgi.8)により、FastCGIとして動作させる。

## 関連項目

  - [CGIゲーム](../Page/CGIゲーム.md "wikilink")

## 参考文献

  - [The CGI Specification(archive.org)](http://web.archive.org/web/20070809114039/hoohoo.ncsa.uiuc.edu/cgi/interface.html)
  - RFC 3875 The Common Gateway Interface (CGI) Version 1.1
  - RFC 1630 Universal Resource Identifiers in WWW
  - RFC 2616 Hypertext Transfer Protocol -- HTTP/1.1

[Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:ウェブ技術](https://ja.wikipedia.org/wiki/Category:ウェブ技術 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")