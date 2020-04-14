> この記事は[Webプログラミング](https://ja.wikipedia.org/wiki/Webプログラミング)から翻訳されています。


**Webプログラミング**（ウェブプログラミング）とは、[World Wide Webで使われる](../Page/World_Wide_Web.md "wikilink")[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")の[プログラミング](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")、Web[ソフトウェア開発](../Page/ソフトウェア開発.md "wikilink")を行うことである。また、この作業を行う人間をWeb[プログラマ](../Page/プログラマ.md "wikilink")、Web[エンジニア](https://ja.wikipedia.org/wiki/エンジニア "wikilink")、Web開発者、Web[ディベロッパー](https://ja.wikipedia.org/wiki/ディベロッパー "wikilink")と呼ぶ。

## 概要

Webプログラミングでは、[サーバ](../Page/サーバ.md "wikilink")側で動作する[プログラムと](../Page/プログラム_\(コンピュータ\).md "wikilink")[クライアント側で動作するプログラムの両方を開発しなければならない](../Page/クライアント_\(コンピュータ\).md "wikilink")。\[1\]それぞれの側のプログラムで利用される技術は異なり、さらに[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")を採用するプログラムであれば、サーバ側・クライアント側のプログラムが複雑に連携して機能を実現するので、それぞれの側のプログラムを別々に開発することが難しく、プログラマには両方の側で用いられる技術を深く習得することが求められる。

サーバ側でのプログラミングは、[ウェブサーバ上で動く](../Page/Webサーバ.md "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")を用いて行われる。このプログラミングは「サーバ・サイド・プログラミング」とも呼ばれる。例としてサーバサイトにつかう言語と環境として[CGI](../Page/Common_Gateway_Interface.md "wikilink") + [Perl](../Page/Perl.md "wikilink")や[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、[Java Servlet](../Page/Java_Servlet.md "wikilink") + [JSP](../Page/JavaServer_Pages.md "wikilink") + [Enterprise JavaBeans](../Page/Enterprise_JavaBeans.md "wikilink") + [Spring Framework](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink") + [Apache Struts](../Page/Apache_Struts.md "wikilink")([Java EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink"))、[.NET](https://ja.wikipedia.org/wiki/.NET "wikilink")([ASP.NET](../Page/Active_Server_Pages.md "wikilink")([C\#](../Page/C_Sharp.md "wikilink"),[VB.NET](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink")))などが挙げられる。

クライアント側のプログラミングは、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")の解釈できる[プログラミング言語](../Page/プログラミング言語.md "wikilink")を用いて行われる。しかしながら[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")はウェブで公開された文書の閲覧に比重が置かれたプログラムであり、必ずしも恵まれたプログラムの実行環境ではないことが多い。

従ってクライアント側のプログラミングは困難となりがちである。これを省力化するためのライブラリが様々に用意されており、例として[JavaServer Facesの部品として利用可能なライブラリ](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink")[AjaxFaces](http://www.ajaxfaces.com/)、[JSPカスタムタグライブラリとして導入できる](../Page/JavaServer_Pages.md "wikilink")[AjaxTags](http://struts.sourceforge.net/ajaxtags/index.html)、JSP, JSF両方で利用可能な[AjaxAnywhere](http://struts.sourceforge.net/ajaxtags/index.html)等がある。なお、これらはいずれも[AJAX](https://ja.wikipedia.org/wiki/AJAX "wikilink")を実現するライブラリで、これらを用いることで[JavaScript](../Page/JavaScript.md "wikilink")等によるクライアントサイドのコードの開発に比重を置くことなく、リッチな[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")を開発できることが期待できる。

## サーバサイドとクライアントサイドにおけるプログラミングの違い

### サーバサイド

サーバサイドでのプログラミングには次のような特徴がある。

アクセスが殺到しやすい[ウェブサイト](../Page/ウェブサイト.md "wikilink")ではデータベースに高い負荷がかかりがちであるため、その解決のために[DBMSの知識が](../Page/データベース管理システム.md "wikilink")[ソフトウェア開発](../Page/ソフトウェア開発.md "wikilink")において求められることが多い。さらに[金融](../Page/金融.md "wikilink")系や[基幹系](https://ja.wikipedia.org/wiki/基幹系 "wikilink")業務や[B2Bなど](https://ja.wikipedia.org/wiki/企業間取引 "wikilink")[ミッションクリティカル](https://ja.wikipedia.org/wiki/ミッションクリティカル "wikilink")な領域での開発では[フロントエンド](../Page/フロントエンド.md "wikilink")だけでなく[バックエンド](https://ja.wikipedia.org/wiki/バックエンド "wikilink")の開発も行うため[UNIX](../Page/UNIX.md "wikilink")や[サーバ](../Page/サーバ.md "wikilink")、[ネットワーク](../Page/コンピュータネットワーク.md "wikilink")、[セキュリティ](../Page/コンピュータセキュリティ.md "wikilink")、[計算機科学](../Page/計算機科学.md "wikilink")、[ソフトウェア工学](../Page/ソフトウェア工学.md "wikilink")の知識が求められる事が多い\[2\]。

またサーバサイドのプログラムでは多くの場合、複数ユーザの操作に応じた処理が同一プロセスのメモリ空間上で行われるので、ユーザごとに適切にメモリ上の情報が分離されるよう意識してプログラミングしなければならない。この変数がもし銀行口座の預金残高などに使われていた場合、その事態は[顧客](https://ja.wikipedia.org/wiki/顧客 "wikilink")や[エンドユーザー](../Page/エンドユーザー.md "wikilink")からの信用を徹底的に失うほど非常に深刻なものとなる。

### クライアントサイド

[クライアントサイド](../Page/クライアントサイド.md "wikilink")でのプログラミングは、[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")([JavaScript](../Page/JavaScript.md "wikilink") + [XML](../Page/Extensible_Markup_Language.md "wikilink"))のように[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")上で動く[プログラミング言語](../Page/プログラミング言語.md "wikilink")を用いて行われるケースもあるが、近年では[リッチクライアント](https://ja.wikipedia.org/wiki/リッチクライアント "wikilink")が登場し、ウェブブラウザのかわりにブラウザ依存を避けられる[Java Web Startや](../Page/Java_Web_Start.md "wikilink")[ClickOnce](https://ja.wikipedia.org/wiki/ClickOnce "wikilink")や[Adobe Flashを使うケースも増えている](../Page/Adobe_Flash.md "wikilink")。

JavaScriptを用いる場合、ウェブブラウザには様々な実装系があるため\[3\]、クライアント側のでプログラミングを行うためには、複数の実装系に精通している必要があった。 しかし、JavaScriptに使用されている[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")が[Google Mapsに実装されることで脚光を浴びるにつれて](../Page/Google_マップ.md "wikilink")、[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")に使用する（prototype.jsなどの）[ライブラリ](../Page/ライブラリ.md "wikilink")が、ブラウザ依存しにくいように設計されるようになってきた。Ajaxのライブラリ、[フレームワークを使いこなしていれば複数の実装系依存に拘る必要は無くなってきている](../Page/アプリケーションフレームワーク.md "wikilink")。

従来では、Web開発における[クライアントサイド](../Page/クライアントサイド.md "wikilink")といえば、[Webデザイナが](../Page/ウェブデザイナー.md "wikilink")[HTMLと小規模な](../Page/HyperText_Markup_Language.md "wikilink")[JavaScript](../Page/JavaScript.md "wikilink")や[Adobe Flashで作られたサイトを開発する程度のものであったため](../Page/Adobe_Flash.md "wikilink")、[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")の習得についてほとんど意識する必要がなかった。しかし端末[ハードウェア](../Page/ハードウェア.md "wikilink")の性能が向上し、[HTMLクライアント](https://ja.wikipedia.org/wiki/HTMLクライアント "wikilink")の限界と不満が叫ばれるようになってゆき、[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")と[リッチクライアント](https://ja.wikipedia.org/wiki/リッチクライアント "wikilink")が注目されるにつれて、クライアントサイドでも[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")を習得する必要性が高まってきた。[リッチクライアント](https://ja.wikipedia.org/wiki/リッチクライアント "wikilink")に使用する技術の一つである[Swing](../Page/Swing.md "wikilink")などによる[GUI開発ではオブジェクト指向プログラミングは](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、[ファットクライアント](https://ja.wikipedia.org/wiki/ファットクライアント "wikilink")、[スタンドアロンアプリケーション](https://ja.wikipedia.org/wiki/スタンドアロンアプリケーション "wikilink")時代から必須のものである。また[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")のフレームワークの多くはオブジェクト指向プログラミングで設計されている\[4\]。

ウェブブラウザは[ウィンドウシステム](../Page/ウィンドウシステム.md "wikilink")や[ウィジェット・ツールキット](../Page/ウィジェット・ツールキット.md "wikilink")とは異なり、アプリケーションが[GUIを実現できるようにする事を元来の目的とするプログラムではなく](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、Web上のHTML文書などを閲覧することを主な目的とするプログラムなので、そのプログラム上で良いGUIを実現するには様々な工夫が求められる。その工夫の例としてAjaxや[リッチクライアント](https://ja.wikipedia.org/wiki/リッチクライアント "wikilink")がある。

#### リッチクライアント

[HTMLクライアント](https://ja.wikipedia.org/wiki/HTMLクライアント "wikilink")の欠点を補うために、HTMLクライアントと[クライアントサーバシステムで使われてきた](https://ja.wikipedia.org/wiki/サーバ#クライアント・サーバ・モデル "wikilink")[ファットクライアント](https://ja.wikipedia.org/wiki/ファットクライアント "wikilink")との中間に位置する[リッチクライアント](https://ja.wikipedia.org/wiki/リッチクライアント "wikilink")も注目されている。リッチクライアントとして挙げられるものは、[Java Web Start](../Page/Java_Web_Start.md "wikilink")、[.NET](https://ja.wikipedia.org/wiki/.NET "wikilink")の[ClickOnce](https://ja.wikipedia.org/wiki/ClickOnce "wikilink")、[Adobeの](../Page/アドビシステムズ.md "wikilink")[AIRなどがある](https://ja.wikipedia.org/wiki/Adobe_Integrated_Runtime "wikilink")。これらの登場により、クライアントサイドの開発は一変しつつある。

## 脚注

<references/>

## 関連項目

  - [Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")
  - [JavaScript](../Page/JavaScript.md "wikilink")
  - [CGI](../Page/Common_Gateway_Interface.md "wikilink")
  - [Java Servlet](../Page/Java_Servlet.md "wikilink")
  - [JavaServer Pages](../Page/JavaServer_Pages.md "wikilink")
  - [JavaServer Faces](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink")
  - [Java Web Start](../Page/Java_Web_Start.md "wikilink")
  - [Swing](../Page/Swing.md "wikilink")
  - [Java Platform, Standard Edition](../Page/Java_Platform,_Standard_Edition.md "wikilink")(Java SE)
  - [Java Platform, Enterprise Edition](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")(Java EE)
  - [PHP (プログラミング言語)](../Page/PHP_\(プログラミング言語\).md "wikilink")
  - [ASP](../Page/Active_Server_Pages.md "wikilink")
  - [ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")
  - [Webアプリケーションフレームワーク](../Page/Webアプリケーションフレームワーク.md "wikilink")
  - [ポータルサイト](../Page/ポータルサイト.md "wikilink")
  - [コードキャンプ](https://ja.wikipedia.org/wiki/コードキャンプ "wikilink")

[Category:プログラミング](https://ja.wikipedia.org/wiki/Category:プログラミング "wikilink") [Category:World_Wide_Web](https://ja.wikipedia.org/wiki/Category:World_Wide_Web "wikilink") [Category:ウェブ開発](https://ja.wikipedia.org/wiki/Category:ウェブ開発 "wikilink") [Category:ウェブデザイン](https://ja.wikipedia.org/wiki/Category:ウェブデザイン "wikilink") [Category:ウェブサイトの構成](https://ja.wikipedia.org/wiki/Category:ウェブサイトの構成 "wikilink")

1.  [HTMLによる](../Page/HyperText_Markup_Language.md "wikilink")[ウェブページ](../Page/ウェブページ.md "wikilink")の記述は[プログラミングではなく](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")[ウェブデザイン](../Page/ウェブデザイン.md "wikilink")とされることも多いが、HTMLはグラフィックデザインだけではなくクライアントからサーバへの通信内容をも定義する等、その境目はあまり明確ではない。
2.  この場合、Web開発は[フロントエンド](../Page/フロントエンド.md "wikilink")だけに力を注いでいるため、[ソフトウェア開発](../Page/ソフトウェア開発.md "wikilink")全体の氷山の一角に過ぎないケースがある。そのためにこのような開発のことをWeb開発とは呼ばないことがある。
3.  ウェブブラウザのバージョンの違いによるバグの有無もあるが、そもそも実装系によって仕様が違うこともある。
4.  今では主にAjaxに使われているJavaScriptは従来、オブジェクト指向言語ではないと誤解されていた。