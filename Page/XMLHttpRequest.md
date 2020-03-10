> この記事は[XMLHttpRequest](https://ja.wikipedia.org/wiki/XMLHttpRequest)から翻訳されています。


**XMLHttpRequest** (XHR) は、[JavaScript](../Page/JavaScript.md "wikilink")などの[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")搭載の[スクリプト言語](../Page/スクリプト言語.md "wikilink")で[サーバ](../Page/サーバ.md "wikilink")との[HTTP通信を行うための](../Page/Hypertext_Transfer_Protocol.md "wikilink")、組み込み[オブジェクト](https://ja.wikipedia.org/wiki/オブジェクト "wikilink")（[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")）である。

すでに読み込んだページからさらにHTTPリクエストを発することができ、ページ遷移することなしにデータを送受信できる[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")の基幹技術である。

XMLHttpRequestを利用したWebアプリケーションは非常に多く存在し、例として、[Google マップ](https://ja.wikipedia.org/wiki/Google_マップ "wikilink")、[Facebook](../Page/Facebook.md "wikilink")などが挙げられる。

## 歴史

XMLHttpRequestは、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が[Outlook Web Access](../Page/Outlook_Web_Access.md "wikilink") 2000の[ダイナミックHTML](../Page/ダイナミックHTML.md "wikilink")によるウェブインターフェースに活用するため、[1999年](../Page/1999年.md "wikilink")公開の[Internet Explorer](../Page/Internet_Explorer.md "wikilink") 5において[ActiveX](../Page/ActiveX.md "wikilink")オブジェクトとして実装したのが始まりである\[1\]。その後、[2001年](../Page/2001年.md "wikilink")に[Mozilla](../Page/Mozilla.md "wikilink")プロジェクトがこれと互換性のある組み込みオブジェクトをMozilla 0.9.7および[Netscape](../Page/Netscapeシリーズ.md "wikilink") 7で実装し、[アップルも](../Page/アップル_\(企業\).md "wikilink")[2004年](../Page/2004年.md "wikilink")に[Safari](../Page/Safari.md "wikilink") 1.2でMozillaと同様の組み込みオブジェクトを実装し始めた\[2\]。

このように徐々にInternet Explorer以外のブラウザにも実装されていったXMLHttpRequestは、[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")に[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")によって一躍有名になった。[オペラ・ソフトウェア](https://ja.wikipedia.org/wiki/オペラ・ソフトウェア "wikilink")も同年、組み込みオブジェクトとしてXMLHttpRequestを実装した[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink") 8をリリースするなど、XMLHttpRequestはスクリプトの実行環境がある多くのブラウザで実装された。また[マイクロソフト](../Page/マイクロソフト.md "wikilink")は[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")リリースのInternet Explorer 7で、ユーザーがActiveXを無効にしていてもAjaxアプリケーションを利用できるよう、XMLHttpRequestを組み込みオブジェクトとして標準実装した\[3\]。

ウェブブラウザで実装されている[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")となったことから、W3Cで仕様の標準化が進められ、[XMLHttpRequest Level 1](https://www.w3.org/TR/XMLHttpRequest/)および[XMLHttpRequest Level 2](https://www.w3.org/TR/XMLHttpRequest2/)の策定が始まった。その後、2014年11月18日に Level 2 が廃止され、Level 1 に統合された。また、今後の仕様策定は [WHATWG](https://ja.wikipedia.org/wiki/WHATWG "wikilink") で議論することになった\[4\]。

それ以降、WHATWGの[XMLHttpRequest Living Standard](https://xhr.spec.whatwg.org/)が仕様として扱われている。

## オブジェクトの構成

以下のAPIは、全ての主要なブラウザの最新版ではいずれも実装されている。

  - [メソッド](https://ja.wikipedia.org/wiki/メソッド "wikilink")
      - abort
      - getAllResponseHeaders
      - getResponseHeader
      - open
      - overrideMimeType
      - send
      - setRequestHeader
  - イベントハンドラ
      - onloadstart
      - onprogress
      - onabort
      - onerror
      - onload
      - ontimeout
      - onloadend
      - onreadystatechange
  - [プロパティ](../Page/プロパティ.md "wikilink")
      - readyState
          - 0 = UNSENT
          - 1 = OPENED
          - 2 = HEADERS_RECEIVED
          - 3 = LOADING
          - 4 = DONE
      - response
      - responseText
      - responseType
      - responseXML
      - status
      - statusText
      - timeout
      - upload
      - withCredentials

## 利用法

### オブジェクトの作成

Internet Explorer 5および6ではActiveXオブジェクトでしか存在しないため、以下のようなフォールバックコードが多用される。

``` javascript
var xhr;
if (XMLHttpRequest) {
  // 組み込みオブジェクトとして定義されていればそれを利用
  xhr = new XMLHttpRequest();
} else {
  // さもなくばActiveXオブジェクトを利用
  try {
    xhr = new ActiveXObject('MSXML2.XMLHTTP.6.0');
  } catch (e) {
    try {
      xhr = new ActiveXObject('MSXML2.XMLHTTP.3.0');
    } catch (e) {
      try {
        xhr = new ActiveXObject('MSXML2.XMLHTTP');
      } catch (e) {
        alert("ActiveXを有効にしてください");
      }
    }
  }
}
```

MSXMLのどのバージョンを利用するかについて、マイクロソフトのXMLチームはベストとして6.0、代替として3.0を推奨している\[5\]。

また、見やすさと利便性を考慮してこのようなコードも使われる。 関数化により簡単に扱えるようにし、 return文は関数を終了する働きを持っていることを利用して見やすさを向上させている。

``` javascript
function createXMLHttpRequest(){
    if(window.XMLHttpRequest){return new XMLHttpRequest()}
    if(window.ActiveXObject){
        try{return new ActiveXObject("Msxml2.XMLHTTP.6.0")}catch(e){}
        try{return new ActiveXObject("Msxml2.XMLHTTP.3.0")}catch(e){}
        try{return new ActiveXObject("Microsoft.XMLHTTP")}catch(e){}

    }
    return false;
};
```

さらに、このように圧縮したコードを書くこともできる。

``` javascript
function createXMLHttpRequest(a,e,i){
    if(XMLHttpRequest){return new XMLHttpRequest()}
    if(ActiveXObject){a="Msxml2.XMLHTTP.";a=["Microsoft.XMLHTTP",a+"3.0",a+"6.0"];
    for(i=3;i--;){try{return new ActiveXObject(a[i])}catch(e){}}
    }return !1
};
```

### GET

``` javascript
xhr.onreadystatechange = function() {
  if (xhr.readyState == 4) { // DONE
    if (xhr.status == 200) { // OK
      alert(xhr.responseText);
    } else {
      alert("status = " + xhr.status);
    }
  }
}
xhr.open("GET", "hoge.txt");
xhr.send();
```

### POST

``` javascript
xhr.onreadystatechange = function() {
  if (xhr.readyState == 4) { // DONE
    if (xhr.status == 200) { // OK
      alert(xhr.responseText);
    } else {
      alert("status = " + xhr.status);
    }
  }
}
xhr.open("POST", "hoge.cgi");
xhr.setRequestHeader("Content-Type" , "application/x-www-form-urlencoded");
xhr.send("a=b&c=d");
```

## クロスドメイン

通信はセキュリティ上の理由により[同一生成元ポリシー](https://ja.wikipedia.org/wiki/同一生成元ポリシー "wikilink")によって制限され、基本的には、XMLHttpRequestは同一ドメイン（正確には同一生成元）としか通信ができない。 しかし、XMLHttpRequest Level 2には、異なるドメインと通信する機能が追加になっており、Firefox 3.5以降、Google Chrome、Safari 4以降で利用可能である。また、Internet Explorer 8には、非標準の XDomainRequest があり、似たようなことが可能である。

クロスドメインを認めるには、サーバー側のHTTPレスポンスヘッダーに追加が必要であり、例えば、`Access-Control-Allow-Origin: *`と書くと全てのドメインからのアクセスが許可される。Access-Control-Allow-Origin は Internet Explorer を含め全てのクロスドメイン対応ブラウザで使える。W3Cの仕様は、Cross-Origin Resource Sharing にて規定されている。

また、Firefox では POST などで、text/plain など以外の Content-Type をクロスドメインで送信する場合、OPTIONS を使いプレフライトが行われる\[6\]。

また、ブラウザの拡張機能などでは特別に制限を受けずに通信を行える機能が用意されている場合もある。

## ストリーミング

readyState が 3 (LOADING) の状態で、基本的には、受信途中の通信内容を取ることができるので、そのことを使うと、受信ストリーミングが使用できる。ただし、各ブラウザで以下の制限事項がある\[7\]。

1.  Internet ExplorerのXMLHttpRequestはreadyStateが3の状態では、内容がとれなく、Internet Explorer 8用のXDomainRequestを使用する必要があり、加えて、最初に2KBのダミーデータをサーバーから送る必要がある。Internet Explorer 7 以前では、ストリーミングは使えない。
2.  Google Chrome はバージョン6現在、readyStateが3の状態に移行するために、Content-Type: application/octet-stream とするか、1024バイト以上のデータをサーバーから送る必要がある\[8\]。
3.  Opera 以外のブラウザでは、ブラウザ側でデータを受け取るたびに onreadystatechange が発生するが、Opera 11.0 では発生しないので、定期的にresponseTextの内容を見に行く必要がある。

## ロングポーリング

HTTPの接続を張りっぱなしにしておいて、サーバーから情報を送りたいときに初めてレスポンスを返すことをロングポーリングと呼ぶ。[Comet](https://ja.wikipedia.org/wiki/Comet "wikilink")の実装に使われる。利用時に以下の注意点がある。

1.  ブラウザのHTTP接続のタイムアウト（30秒など）があるため、接続が切れたら、接続し直すロジックが必要である。
2.  サーバー当たりの同時接続数が、初期設定では、Internet Explorer 8以降や Internet Explorer 以外の主要ブラウザでは6\[9\]、Internet Explorer 7以前では2に制限されているため、複数のロングポーリングをこの制限まで同時に行うと、新たにサーバーに接続できなくなる。ダイアルアップ接続の場合、Internet Explorer 8でも同時接続数は2に制限されている。
3.  HTTPの接続が終了するまでサーバーが終了できなかったり、接続ごとにスレッドを作成し、同時接続数が多いとそれがメモリなどのリソースを大量に消費するなどの問題があるため、ロングポーリングに対応したサーバー側の実装方法が必要である。例えばJavaの場合は、Jettyならば独自のContinuationクラス、Apache Tomcatならば独自のCometProcessorクラスなど、Servlet 3.0ならばHTTPServletRequestにstartAsync()が用意されていて、それらのロングポーリング用のAPIを活用することが望ましい。

なおこれらの問題を根本的に解決することを目的として、現在IETF・W3C他では代替プロトコルとして[WebSocket](https://ja.wikipedia.org/wiki/WebSocket "wikilink")の標準化作業を進めている。

## 脚注

<references/>

## 関連項目

  - [Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")
  - [Extensible Markup Language](../Page/Extensible_Markup_Language.md "wikilink")
  - [Hypertext Transfer Protocol](../Page/Hypertext_Transfer_Protocol.md "wikilink")
  - [WebSocket](https://ja.wikipedia.org/wiki/WebSocket "wikilink")
  - [Outlook Web Access](../Page/Outlook_Web_Access.md "wikilink")

## 外部リンク

### 仕様

  - [XMLHttpRequest Level 1](http://www.w3.org/TR/XMLHttpRequest/) - W3C Working Draft
  - [XMLHttpRequest Level 2](http://www.w3.org/TR/XMLHttpRequest2/) - 廃止され Level 1 に統合された
  - [XMLHttpRequest Living Standard](https://xhr.spec.whatwg.org/) - [WHATWG](https://ja.wikipedia.org/wiki/WHATWG "wikilink")
      - [XMLHttpRequest Standard （日本語訳）](https://triple-underscore.github.io/XHR-ja.html)
  - [Cross-Origin Resource Sharing](http://www.w3.org/TR/cors/)
  - [Progress Events 1.0](http://www.w3.org/TR/progress-events/)

### ブラウザ側の解説

  - [MSDN ライブラリ](https://ja.wikipedia.org/wiki/MSDN_ライブラリ "wikilink")
      - [XMLHttpRequest Object](http://msdn.microsoft.com/ja-jp/library/ms535874.aspx)
      - [XDomainRequest Object](http://msdn.microsoft.com/ja-jp/library/cc288060.aspx)
      - [IXMLHTTPRequest](http://msdn.microsoft.com/ja-jp/library/ms759148.aspx)
  - [XMLHttpRequest](https://developer.mozilla.org/ja/XMLHttpRequest) - [Mozilla Developer Center](https://ja.wikipedia.org/wiki/Mozilla_Developer_Center "wikilink")
  - [オペラのXMLHttpRequest ("Ajax") サポート](http://jp.opera.com/docs/specs/presto22/xmlhttprequest/)
  - [Dynamic HTMLとXML：XMLHttpRequestオブジェクト](http://developer.apple.com/jp/internet/webcontent/xmlhttpreq.html) - [Apple Developer Connection](../Page/Apple_Developer_Connection.md "wikilink")

[Category:World_Wide_Web](https://ja.wikipedia.org/wiki/Category:World_Wide_Web "wikilink") [Category:Hypertext_Transfer_Protocol](https://ja.wikipedia.org/wiki/Category:Hypertext_Transfer_Protocol "wikilink")

1.  "[Outlook Web Access - A catalyst for web evolution](https://blogs.technet.microsoft.com/exchange/2005/06/21/outlook-web-access-a-catalyst-for-web-evolution/)" *[You Had Me At EHLO...](https://blogs.technet.microsoft.com/exchange/)*, Jim Van Eaton, 2005年6月21日
2.  "[Dynamic HTMLとXML：XMLHttpRequestオブジェクト](http://developer.apple.com/jp/internet/webcontent/xmlhttpreq.html)" *[Apple Developer Connection](http://developer.apple.com/jp/)*, Apple, 2005年6月24日
3.  "[IE7 - XMLHttpRequest の標準サポート](http://www.exconn.net/Blogs/windows/archive/2006/03/09/7564.aspx)", [ウィンドウズ開発統括部](http://www.exconn.net/Blogs/windows/), [及川卓也](https://ja.wikipedia.org/wiki/及川卓也 "wikilink"), 2006年3月9日
4.  [XMLHttpRequest Level 2 W3C Working Group Note](http://www.w3.org/TR/XMLHttpRequest2/)
5.
6.
7.  [COMET Streaming in Internet Explorer - EricLaw's IEInternals - Site Home - MSDN Blogs](http://blogs.msdn.com/b/ieinternals/archive/2010/04/06/comet-streaming-in-internet-explorer-with-xmlhttprequest-and-xdomainrequest.aspx)
8.  [Issue 2016 - chromium - Chrome stalls XHRs in order to sniff mime-type - Project Hosting on Google Code](http://code.google.com/p/chromium/issues/detail?id=2016#c41)
9.  [Network - Browserscope](http://www.browserscope.org/?category=network)