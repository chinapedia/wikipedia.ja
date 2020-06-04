> この記事は[FastCGI](https://ja.wikipedia.org/wiki/FastCGI)から翻訳されています。


**FastCGI**とは、[Webサーバ](../Page/Webサーバ.md "wikilink")上でユーザ[プログラムを動作させるための](../Page/プログラム_\(コンピュータ\).md "wikilink")[インタフェース](https://ja.wikipedia.org/wiki/インタフェース "wikilink")仕様の一つである。[CGIの問題を解決するために](../Page/Common_Gateway_Interface.md "wikilink")社によって1990年代中頃に開発された\[1\]もので、仕様は公開されている。

## 概要(従来の[CGIの問題点](../Page/Common_Gateway_Interface.md "wikilink"))

[CGIは](../Page/Common_Gateway_Interface.md "wikilink")、外部アプリケーションを[Webサーバ](../Page/Webサーバ.md "wikilink")に接続するためのプロトコルである。CGIアプリケーションは個別の[プロセス](../Page/プロセス.md "wikilink")で実行され、各リクエストの開始時に作成され、終了時に破棄される。この「リクエスト毎に1つの新しいプロセス」モデルにより、CGIプログラムの実装が非常に簡単になるが、効率と[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")が制限される。高負荷では、プロセスの作成と破棄のための[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の[オーバーヘッド](https://ja.wikipedia.org/wiki/オーバーヘッド "wikilink")が大きくなる。また、CGIプロセスモデルは、[データベース](../Page/データベース.md "wikilink")接続の再利用、インメモリキャッシング等の[リソース再利用方法を制限する](../Page/計算資源.md "wikilink")。

## 歴史

CGIの[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")の欠点に対処するために、Open Market はFastCGI を開発し、1990年代中頃に最初に[Webサーバ](../Page/Webサーバ.md "wikilink")製品に導入した。Open Market は当初、[Webアプリケーションを開発するための](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")[Netscape独自のインプロセス](../Page/ネットスケープコミュニケーションズ.md "wikilink")[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")((NSAPI))に対する競争力のある対応としてFastCGIを開発した。 最初はOpen Market によって開発されたが、FastCGI は他のいくつかの[Webサーバ](../Page/Webサーバ.md "wikilink")メーカーによって実装された。ただし、そのアプローチは、サーバとサブプログラム間の通信を高速化および簡素化する他の方法と競合した。や等の[Apache HTTP Serverモジュールがほぼ同時期に登場し](../Page/Apache_HTTP_Server.md "wikilink")、急速に普及した。2019年現在、CGIを含むこれら様々な方法は引き続き使用されている。

## 詳細

リクエスト毎に新しいプロセスを作成する代わりに、FastCGI は永続的な[プロセス](../Page/プロセス.md "wikilink")を使用して一連のリクエストを処理する。これらの[プロセス](../Page/プロセス.md "wikilink")は、[Webサーバ](../Page/Webサーバ.md "wikilink")ではなくFastCGI サーバが所有している\[2\]。

受信リクエストを処理するために、[Webサーバ](../Page/Webサーバ.md "wikilink")は[環境変数](../Page/環境変数.md "wikilink")情報とページリクエストを、[UNIXドメインソケット](https://ja.wikipedia.org/wiki/UNIXドメインソケット "wikilink")、[名前付きパイプ](../Page/名前付きパイプ.md "wikilink")、または[伝送制御プロトコル](../Page/Transmission_Control_Protocol.md "wikilink")(TCP)接続のいずれかを介してFastCGI プロセスに送信する。応答は同じ接続を介して[プロセス](../Page/プロセス.md "wikilink")から[Webサーバ](../Page/Webサーバ.md "wikilink")に返され、[Webサーバ](../Page/Webサーバ.md "wikilink")はその応答を[エンドユーザに配信する](../Page/エンドユーザー.md "wikilink")。応答の最後に接続が閉じられる可能性があるが、[Webサーバ](../Page/Webサーバ.md "wikilink")とFastCGI サービスプロセスの両方が存続する\[3\]。

個々のFastCGI プロセスは、その存続期間中に多くの要求を処理できるため、要求毎の[プロセス](../Page/プロセス.md "wikilink")の作成と終了の[オーバーヘッド](https://ja.wikipedia.org/wiki/オーバーヘッド "wikilink")を回避できる。複数の要求を同時に処理するには、いくつかの方法がある。1つの接続を内部[多重化](../Page/多重化.md "wikilink")(つまり、1つの接続で複数の要求)を使用して行う、複数の接続を使用する、またはこれらの方法の組み合わせによる方法がある。複数のFastCGI サーバを構成できるため、安定性と[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")が向上する。

[Webサイトの管理者と](../Page/ウェブサイト.md "wikilink")[プログラマ](../Page/プログラマ.md "wikilink")は、FastCGI で[Webサーバ](../Page/Webサーバ.md "wikilink")から[Webアプリケーションを分離すると](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")、組み込み[インタプリタ](../Page/インタプリタ.md "wikilink")(や等)に比べて多くの利点がある。この分離により、サーバ[プロセス](../Page/プロセス.md "wikilink")とアプリケーション[プロセス](../Page/プロセス.md "wikilink")を個別に[再起動](../Page/再起動.md "wikilink")できる。これは、多忙な[Webサイトにとって重要な考慮事項である](../Page/ウェブサイト.md "wikilink")。また、[ISPやWebホスティング会社にとって重要な要件である](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")、アプリケーションごとのホスティングサービスセキュリティポリシーの実装も可能になる\[4\]。様々なタイプの着信要求を、それらのタイプの要求を効率的に処理するように装備されている特定のFastCGI サーバに配布できる。

## FastCGI を実装する[Webサーバ](../Page/Webサーバ.md "wikilink")

参考:

注: 特に明記しない限り、FastCGI 実装の完全性は不明

  - [Apache HTTP Server](../Page/Apache_HTTP_Server.md "wikilink")(部分的)

      - `mod_fcgid`\[5\]によって実装されている。この[モジュールは以前は](https://ja.wikipedia.org/wiki/モジュール#ソフトウェア "wikilink")[サードパーティだったが](../Page/サードパーティー.md "wikilink")、Chris Darroch によって統括された[2009年](../Page/2009年.md "wikilink")に[Apache Serverのサブプロジェクトとして](../Page/Apache_HTTP_Server.md "wikilink")[Apacheソフトウェア財団](../Page/Apacheソフトウェア財団.md "wikilink")(ASF)に寄贈された\[6\]。[UNIXドメインソケット](https://ja.wikipedia.org/wiki/UNIXドメインソケット "wikilink")のみをサポートし、TCP ソケットはサポートしない\[7\]。
      - [サードパーティのモジュール](../Page/サードパーティー.md "wikilink")`mod_fastcgi`も使用される。しばらくの間、このモジュールはApache 2.4.xで適切にコンパイルされなかった\[8\]。その問題は元のプロジェクトの[フォークで解決された](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")\[9\]。
      - 1つの接続を介したリクエストの多重化は、Apache 1.x 設計によって禁止されているため\[10\]、これはサポートされていない
      - Apache 2.4では、`mod_proxy_fcgi`\[11\]が追加され、TCP FastCGI サーバをサポートしている。

  - \[12\]

  - \[13\]

  - \[14\]

      - [ロードバランシングFastCGI](../Page/サーバロードバランス.md "wikilink") サポート
      - chroot されたFastCGI サーバをサポート

  - [Jetty](../Page/Jetty.md "wikilink")\[15\]

  -
  - [Lighttpd](../Page/Lighttpd.md "wikilink")\[16\]

  -
  - [Microsoft IIS](../Page/Internet_Information_Services.md "wikilink")\[17\]

  - [nginx](https://ja.wikipedia.org/wiki/nginx "wikilink")

  -
  - [Oracle iPlanet Web Server](https://ja.wikipedia.org/wiki/Oracle_iPlanet_Web_Server "wikilink")

  - [OpenBSD](../Page/OpenBSD.md "wikilink")の`httpd(8)`\[18\]

  - [Webサーバ](../Page/Webサーバ.md "wikilink")

  - [Webサーバ](../Page/Webサーバ.md "wikilink")および[Webアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")

  - [Webサーバ](../Page/Webサーバ.md "wikilink")

  - [Webサーバ](../Page/Webサーバ.md "wikilink")

  -
## [API言語バインディング](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink")

FastCGI は、ネットワークソケットをサポートする任意の言語で実装できる。「FastCGI はプロトコルであり、実装ではない」ため、1つの言語に強く拘束されていない。[アプリケーションプログラミングインターフェイス](https://ja.wikipedia.org/wiki/アプリケーションプログラミングインターフェイス "wikilink")(API)は、次のものに対して存在する\[19\]:

  - [Ada](../Page/Ada.md "wikilink")\[20\]

  - [Delphi](../Page/Delphi.md "wikilink"), [Lazarus](../Page/Lazarus.md "wikilink"), [Free Pascal](../Page/Free_Pascal.md "wikilink")\[21\]

  - [C言語](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")

  - [Chicken (Scheme)](https://ja.wikipedia.org/wiki/Chicken_\(Scheme\) "wikilink")

  - [Common Lisp](../Page/Common_Lisp.md "wikilink")\[22\]

  - [D言語](../Page/D言語.md "wikilink")

  - [Eiffel](../Page/Eiffel.md "wikilink")\[23\]

  - [Erlang](../Page/Erlang.md "wikilink")

  -
  - [Go](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink")

  - [Guile](https://ja.wikipedia.org/wiki/GNU_Guile "wikilink") Scheme

  - [Haskell](../Page/Haskell.md "wikilink")

  -
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")\[24\]\[25\]

  - [Lua](../Page/Lua.md "wikilink")

  - [node.js](https://ja.wikipedia.org/wiki/node.js "wikilink")\[26\]

  - [OCaml](../Page/OCaml.md "wikilink")

  - [Perl](../Page/Perl.md "wikilink")\[27\]

  - [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")(`php-fpm`経由\[28\]、\[29\])

  - [Python](../Page/Python.md "wikilink")

  - [Ruby](../Page/Ruby.md "wikilink")

  - [Rust](https://ja.wikipedia.org/wiki/Rust_\(プログラミング言語\) "wikilink")\[30\]

  -
  - [Smalltalk](../Page/Smalltalk.md "wikilink"): FasTalk および

  - [Tcl](https://ja.wikipedia.org/wiki/Tcl/Tk "wikilink")

  -
  - [Vala](https://ja.wikipedia.org/wiki/Vala "wikilink")([C言語](../Page/C言語.md "wikilink")バインディング)

  - [Xojo](../Page/Xojo.md "wikilink")(以前はRealbasic, REAL Studio)\[31\]

[Ruby on Rails](../Page/Ruby_on_Rails.md "wikilink"), [Catalyst](../Page/Catalyst_\(ソフトウェア\).md "wikilink"), [Django](../Page/Django.md "wikilink"), 、等の最近の[フレームワークでは](https://ja.wikipedia.org/wiki/ソフトウェアフレームワーク "wikilink")、組み込みインタープリタ(, , [mod_python](https://ja.wikipedia.org/wiki/mod_python "wikilink"), 等)、またはFastCGI を使用できる。

## 脚注

### 出典

## 関連項目

  - [CGI](../Page/Common_Gateway_Interface.md "wikilink")

## 外部リンク

  - 公式サイト: [FastCGI.com Archive](https://fastcgi-archives.github.io/)
      - 仕様: [FastCGI Specification](https://fastcgi-archives.github.io/FastCGI_Specification.html)
          - [セカンダリバックアップ](https://www.mit.edu/~yandros/doc/specs/fcgi-spec.html)
  - [README for mod_fastcgi](https://fastcgi-archives.github.io/mod_fastcgi/)
  - [mod_fcgid - FastCGI interface module for Apache 2 - The Apache HTTP Server Project](https://httpd.apache.org/mod_fcgid/)
  - [Installing PHP on Windows Vista with FastCGI | Microsoft Docs](https://docs.microsoft.com/en-us/iis/application-frameworks/install-and-configure-php-on-iis/installing-php-on-windows-vista-with-fastcgi)
  - [Proxy FastCGI Scheme Apache Module | “mod_proxy_fcgi” is an Apache v2.0 proxy sheme module that implement “fcgi:” scheme to handle reverse proxy protocole FastCGI.](https://zenprojects.github.io/Apache-Proxy-FastCGI-Module/)

[Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:ウェブ技術](https://ja.wikipedia.org/wiki/Category:ウェブ技術 "wikilink")

1.
2.   FastCGI|accessdate=2020/04/20|publisher=}}
3.   FastCGI|accessdate=2020/04/20|publisher=}}
4.   Linux Journal|accessdate=2020/04/20|publisher=}}
5.
6.
7.
8.
9.
10.
11.
12.
13.  Handler FastCGI {{\!}} Cherokee Documentation|accessdate=2020/04/21|publisher=}}
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.  HHVM|accessdate=2020/04/21|publisher=}}
30.
31.