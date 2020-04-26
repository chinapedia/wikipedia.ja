> この記事は[HTTP 404](https://ja.wikipedia.org/wiki/HTTP_404)から翻訳されています。


**HTTP 404**、またはエラーメッセージ **Not Found**（「未検出」「見つかりません」の意）は、[HTTPステータスコード](../Page/HTTPステータスコード.md "wikilink")の一つ。クライアントがサーバに接続できたものの、クライアントの要求に該当するもの (ウェブページ等) をサーバが見つけられなかったことを示すもの。また、要求に応えられない理由をごまかすためにも使われる。

[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")が表示する「サーバが見つかりません」のようなメッセージは、サーバとの接続に失敗したことを表すもので、404とは別である。

## 概要

HTTPを使って通信を行うとき、ブラウザーによる[HTML文書](../Page/HyperText_Markup_Language.md "wikilink")（ウェブページ）などの要求に対して、サーバーは応答を返すように求められる。応答には、数値によるステータスコードと電子メールのようなヘッダーと本文が含まれる。ステータスコード404では、最初の「4」がクライアント側のエラー（URLのミスタイプなど）を表し、続く「04」がエラーの種類を表す。こうしたHTTPの3桁のコードは、[FTPや](../Page/File_Transfer_Protocol.md "wikilink")[NNTP](https://ja.wikipedia.org/wiki/NNTP "wikilink")のようなHTTP以前からあるプロトコルに似ている。

この数字は[WWWが発明された](../Page/World_Wide_Web.md "wikilink")[欧州原子核研究機構](../Page/欧州原子核研究機構.md "wikilink")（CERN）の404という部屋番号にちなんで付けられたという[都市伝説](../Page/都市伝説.md "wikilink")があるが、実際にはCERNには404という部屋はない\[1\]。

ステータスコードの数字にはたいてい英語のテキスト\[2\]が加えられる。404の場合は「Not Found」である。サーバーは通常、404の応答とともに「404 File not found」のように数字とメッセージを記述した短いページを送信する。日本語では「ファイルが見つかりません」「ページが見つかりません」のような記述になる。サーバーアプリケーションのデフォルトのメッセージを使わずに、404用のページをカスタマイズしているサーバーも多い。たとえば[Apache HTTP Serverでは](../Page/Apache_HTTP_Server.md "wikilink")、.htaccessファイルやhttpd.confを書き換えるとそうしたカスタマイズができる。

[Internet Explorer](../Page/Internet_Explorer.md "wikilink")（IE6以前）では、512バイト以下の場合は送信された404用のページを表示せずに、代わりに「親切な」エラーページを表示する。この動作を変えるには、「インターネットオプション」の「詳細設定」で「HTTP[エラーメッセージ](https://ja.wikipedia.org/wiki/エラーメッセージ "wikilink")を簡易表示する」のチェックをはずす。

404は、サーバー上のページが移動されたり削除されたりしたときにも送られることがある。しかし本来、移動された場合は「301 Moved Permanently」、削除されたときは「410 Gone」を返すべきである。ただ、301や410を返すには特別な設定が必要なので、多くのウェブサイトはそうした設定をしていない。

WWWでは404の表示をしょっちゅう目にするため、404は"人や物が見つからないこと"を意味する[新語](../Page/新語.md "wikilink")となった。ユーモラスな404ページを作ることが流行ったり、いろいろな404ページを集めることだけを目的にしたサイトが作られたりしている。

## ソフト404

ウェブサイトの中には、「ファイルが見つからない」ことを示すために、成功を表すステータスコード「200 OK」とともにウェブページを送るものもある。これは「ソフト[404](../Page/404.md "wikilink")」と呼ばれている。ソフト404の問題は、リンクが切れているかどうかを自動的に調べられないことである。ソフト404を判別する方法はBar-Yossefなどが発表している\[3\]。

## 関連項目

  - [HTTPステータスコード](../Page/HTTPステータスコード.md "wikilink")
  - [リンク切れ](../Page/リンク切れ.md "wikilink")
  - [エラーメッセージ](https://ja.wikipedia.org/wiki/エラーメッセージ "wikilink")

## 脚注

<references />

## 外部リンク

  - [ErrorDocument ディレクティブ](https://httpd.apache.org/docs/2.0/mod/core.html#errordocument) - Apache 2.0の設定方法
  - [The Perfect 404](https://alistapart.com/article/perfect404/) - 404ページの作り方（英語）
  - [404 Research Lab](https://404lab.com/) - さまざまな404メッセージ（英語）

[Category:HTTPステータスコード](https://ja.wikipedia.org/wiki/Category:HTTPステータスコード "wikilink")

1.  <http://www.plinko.net/404/history.asp#2>
2.  RFC 2616の6.1.1節にしたがえば、このテキストは空でもよい。制御文字以外の文字と水平タブと半角スペースを含むことができるとする文字の規定はあるが、言語の規定はない。
3.  [Sic Transit Gloria Telae: Towards an Understanding of the Web’s Decay](http://www2004.org/proceedings/docs/1p328.pdf) PDF (232 KiB), §3, submitted to the 13th World Wide Web Conference in New York City, 2004年5月17日-22日( (WWW 2004).