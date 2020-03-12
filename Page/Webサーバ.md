> この記事は[Web](https://ja.wikipedia.org/wiki/Web)から翻訳されています。


**Webサーバ**（ウェブサーバ、英:）は、[HTTPに則り](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[クライアント](../Page/クライアント_\(コンピュータ\).md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")の[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")に対して、[HTMLやオブジェクト](../Page/HyperText_Markup_Language.md "wikilink")（[画像](../Page/画像.md "wikilink")など）の表示を提供するサービスプログラム及び、そのサービスが動作する[サーバ](../Page/サーバ.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")を指す。 広義には、クライアントソフトウェアとHTTPによる通信を行うプログラム及びコンピュータ。

## 実装

クライアントである[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")の[URLにて指示された](../Page/Uniform_Resource_Locator.md "wikilink")、Webサーバ内に存在するHTMLドキュメントの各種情報を、クライアントから接続されたHTTPに則った[TCP/IP](../Page/インターネット・プロトコル・スイート.md "wikilink")[ソケットストリーム](../Page/ソケット_\(BSD\).md "wikilink")（HTTPコネクションと呼ぶ）に送信する。多くの場合、クライアントのウェブブラウザとの間に複数の[コネクション](https://ja.wikipedia.org/wiki/コネクション "wikilink")を張り、HTMLドキュメントとその配下の個々の情報ファイル（画像ファイル情報など）を並列して送り、処理時間を短縮してサービスを提供している。

また、HTMLドキュメントに各種処理を組み込み、[CGI](../Page/Common_Gateway_Interface.md "wikilink")[スクリプト](../Page/スクリプト.md "wikilink")や[Java Servlet](../Page/Java_Servlet.md "wikilink")（サーバ側で実行される[Java](https://ja.wikipedia.org/wiki/Java "wikilink")プログラム）と呼ばれるWeb画面に連動した動的処理を行う事が可能である。CGI処理においては[Perl](../Page/Perl.md "wikilink")・[Ruby](https://ja.wikipedia.org/wiki/Ruby_\(代表的なトピック\) "wikilink")・[PHPなどの](../Page/PHP_\(プログラミング言語\).md "wikilink")[スクリプト言語](../Page/スクリプト言語.md "wikilink")によって開発されることが多い。

Java Servletにおいては、Javaによる動的処理の負荷を分散するため、Java Servletを処理する機能を別サーバに切り出し、Webアプリケーションサーバとして、垂直分散（スケールアウト）する事も一般化している。

大規模なWebサービスを提供する場合、同じサービスを提供するWebサーバを並列して設置し、[ロードバランサ](https://ja.wikipedia.org/wiki/ロードバランサ "wikilink")と呼ばれる各種ロジック（[ラウンドロビン方式や処理中の負荷を計測して割り当てるサーバを決定するものや](../Page/ラウンドロビン・スケジューリング.md "wikilink")、サーバの性能を考慮して重み付けをする方式などが存在する）によりWebサーバへの処理を振り分ける装置を、Webサーバ群の前に置く事が多い。

これにより、Webサービスを提供する際のサーバ故障に対する可用性・信頼性を確保する（[疎結合クラスター](https://ja.wikipedia.org/wiki/疎結合クラスター "wikilink")の一種と定義される）。

また、不特定多数のウェブブラウザ（クライアント）との接続を行うため、一般的にWebサーバ及びWebアプリケーションサーバには[DNSサーバとの連動設定を組み込む](../Page/Domain_Name_System.md "wikilink")。

## 歴史

[Cobalt_Qube_3_Front.jpg](https://ja.wikipedia.org/wiki/File:Cobalt_Qube_3_Front.jpg "fig:Cobalt_Qube_3_Front.jpg")のSOHO向けWebサーバ
Sun Cobalt Qube 3（2002年）\]\]

  - [1989年](../Page/1989年.md "wikilink")
      - [欧州原子核研究機構](../Page/欧州原子核研究機構.md "wikilink") (CERN) に在籍していた[ティム・バーナーズ＝リー](../Page/ティム・バーナーズ＝リー.md "wikilink")が「Information Management: A Proposal（情報管理：提案）」を執筆。彼が以前から持っていたWebシステムの素案を目に見える形で提案した。
  - [1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")[11月](../Page/11月.md "wikilink")
      - World Wide Web をより具体化した提案書を発表。1990年[11月13日](../Page/11月13日.md "wikilink")から開発が開始。
  - [1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")[12月](https://ja.wikipedia.org/wiki/12月 "wikilink")〜[1991年](../Page/1991年.md "wikilink")[1月](https://ja.wikipedia.org/wiki/1月 "wikilink")
      - 現Webサーバ群の基になるHTTPサーバ『[CERN httpd](https://ja.wikipedia.org/wiki/CERN_httpd "wikilink")』と各種ツールをクリスマス休暇中に作成し、最初のWebページ展開（[BSD](../Page/BSD.md "wikilink")系[OSである](../Page/オペレーティングシステム.md "wikilink")[NEXTSTEP](../Page/NEXTSTEP.md "wikilink")／[NeXT](../Page/NeXT.md "wikilink")ワークステーションに実装）。
  - 1991年[8月](../Page/8月.md "wikilink")
      - Webサーバとラインベースのウェブブラウザによるプロジェクト成果の要約をニュースグループに投稿。これがWWWとWebサーバのデビューとなった。
  - [1992年](../Page/1992年.md "wikilink")とそれ以降
      - [イリノイ大学](../Page/イリノイ大学.md "wikilink")の[米国立スーパーコンピュータ応用研究所](../Page/米国立スーパーコンピュータ応用研究所.md "wikilink")(NCSA)の[ロバート・マックール](https://ja.wikipedia.org/wiki/ロバート・マックール "wikilink")らが、CERN httpdに続く2番目の実装となる『[NCSA HTTPd](../Page/NCSA_HTTPd.md "wikilink")』を開発、また同じくNCSAの学生であった[マーク・アンドリーセン](../Page/マーク・アンドリーセン.md "wikilink")らが、画像も表示できるウェブブラウザ[NCSA Mosaicを開発し](../Page/NCSA_Mosaic.md "wikilink")、一般に急速に広まった。
      - この時点では、Webサーバの主役は『CERN httpd』や『NCSA HTTPd』であった。しかし、改修が進まないという不満が募り、NCSA HTTPdに修正を加えるためのパッチ (patch) を集積するプロジェクトが始まった。その際、プロジェクトに Apache Group という名前を付け、開始したため、そのNCSA HTTPdのメンテを主（当初）とした派生版である[Apache HTTP Serverの誕生につながり](../Page/Apache_HTTP_Server.md "wikilink")、主役を移すことになった。

2015年時点においては、Apache及びその派生版である各ベンダのHTTP Serverが市場の4割、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[IISが市場の](../Page/Internet_Information_Services.md "wikilink")3割、[nginx](https://ja.wikipedia.org/wiki/nginx "wikilink")が2割弱を占める\[1\]。

元々、Webサーバは[UNIX](../Page/UNIX.md "wikilink")上で開発され発展してきた経緯もあり、当初から[オープン系サーバと言われるUNIXサーバや](../Page/オープンシステム_\(コンピュータ\).md "wikilink")[Windows系サーバにより実装](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")・提供されるのが普通である。ただし、システム構成上の都合により、[HTTPや](../Page/Hypertext_Transfer_Protocol.md "wikilink")[FTP](../Page/File_Transfer_Protocol.md "wikilink")、[TCP/IPが利用可能な](../Page/インターネット・プロトコル・スイート.md "wikilink")[汎用コンピュータにて動作させる場合もある](../Page/メインフレーム.md "wikilink")。

## 現在の代表的な実装

[LAMP_software_bundle.svg](https://ja.wikipedia.org/wiki/File:LAMP_software_bundle.svg "fig:LAMP_software_bundle.svg") software bundle (here additionally with [Squid](../Page/Squid_\(ソフトウェア\).md "wikilink")). A high performance and high-availability solution for a hostile environment\]\]

  - [Apache HTTP Server](../Page/Apache_HTTP_Server.md "wikilink")
  - [CERN httpd](https://ja.wikipedia.org/wiki/CERN_httpd "wikilink")
  - [NCSA HTTPd](../Page/NCSA_HTTPd.md "wikilink")
  - [Internet Information Services](../Page/Internet_Information_Services.md "wikilink")
  - [AN HTTPD](../Page/AN_HTTPD.md "wikilink")
  - [04webserver](http://www.soft3304.net/04WebServer/)
  - [lighttpd](https://ja.wikipedia.org/wiki/lighttpd "wikilink")
  - [Cherokee (web server)](https://ja.wikipedia.org/wiki/Cherokee_\(web_server\) "wikilink")
  - [Hiawatha Webserver](http://www.hiawatha-webserver.org/) [（英語版)](https://ja.wikipedia.org/wiki/:en:Hiawatha_webserver "wikilink")
  - [thttpd](https://ja.wikipedia.org/wiki/thttpd "wikilink")
  - [RaidenHTTPD](https://ja.wikipedia.org/wiki/RaidenHTTPD "wikilink")
  - [nginx](https://ja.wikipedia.org/wiki/nginx "wikilink")
  - [Zope](../Page/Zope.md "wikilink")

他

## 個別の製品の特徴

  - Oracle HTTP Server
      - [RDBMSベンダである](../Page/関係データベース管理システム.md "wikilink")[オラクルが提供するWebサーバ](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink") (Oracle HTTP Server) においては、[Java EEを使用した](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")[Webアプリケーションサーバと連携して](../Page/アプリケーションサーバ.md "wikilink")、HTMLドキュメント内にデータベースに検索を行わせるための[SQL](../Page/SQL.md "wikilink")文を直接記述し、データベースからデータをHTMLベースで呼び出して加工する事が可能となっている。

## 脚注

## 関連項目

  - [インターネット](../Page/インターネット.md "wikilink")
  - [ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")
  - [アプリケーションサーバ](../Page/アプリケーションサーバ.md "wikilink")
  - [コンテンツ管理システム](../Page/コンテンツ管理システム.md "wikilink") (CMS)
  - [ホスティングサーバ](../Page/ホスティングサーバ.md "wikilink")
  - [FTPサーバ](../Page/FTPサーバ.md "wikilink")
  - [ドメインネームサーバ](https://ja.wikipedia.org/wiki/ドメインネームサーバ "wikilink")
  - [サーバ](../Page/サーバ.md "wikilink")
  - [バーチャルホスト](../Page/バーチャルホスト.md "wikilink")
  - [Server Side Includes](https://ja.wikipedia.org/wiki/Server_Side_Includes "wikilink") (SSI)
  - [帯域幅調整](../Page/帯域幅調整.md "wikilink") - [トラフィックシェーピング](https://ja.wikipedia.org/wiki/トラフィックシェーピング "wikilink")
  - [サーバログ](https://ja.wikipedia.org/wiki/サーバログ "wikilink")

[Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:サーバ](https://ja.wikipedia.org/wiki/Category:サーバ "wikilink") [Category:World_Wide_Web](https://ja.wikipedia.org/wiki/Category:World_Wide_Web "wikilink") [Category:アプリケーションソフト](https://ja.wikipedia.org/wiki/Category:アプリケーションソフト "wikilink")

1.  [November 2015 Web Server Survey](http://news.netcraft.com/archives/2015/11/16/november-2015-web-server-survey.html) netcraft