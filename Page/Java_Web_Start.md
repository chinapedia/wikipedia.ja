> この記事は[Java Web Start](https://ja.wikipedia.org/wiki/Java_Web_Start)から翻訳されています。


**Java Web Start**（ジャバウェブスタート）は[Java](https://ja.wikipedia.org/wiki/Java "wikilink")製[アプリケーションを](../Page/アプリケーションソフトウェア.md "wikilink")[ウェブサーバ](https://ja.wikipedia.org/wiki/ウェブサーバ "wikilink")などから自動[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")、自動[インストール](../Page/インストール.md "wikilink")、自動[アップデート](https://ja.wikipedia.org/wiki/アップデート "wikilink")して、[サンドボックス上にて実行可能な仕組み](../Page/サンドボックス_\(セキュリティ\).md "wikilink")。Java 5\[1\]〜10に搭載され、Java 9\[2\]にて廃止予定（deprecated）となり、Java 11で廃止された\[3\]。

## 概要

[Swing](../Page/Swing.md "wikilink") [APIなどで記述された](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[GUIアプリケーションを実行できる](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。問題点が多いために[Flashよりも劣ると言われる](../Page/Adobe_Flash.md "wikilink")[Javaアプレット](../Page/Javaアプレット.md "wikilink")の代替[リッチクライアント](https://ja.wikipedia.org/wiki/リッチクライアント "wikilink")と言われている。

たとえば、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")でJava Web Startに対応した[Javaアプリケーション](https://ja.wikipedia.org/wiki/Javaアプリケーション "wikilink")へのリンクをクリックすると、[Javaアプレット](../Page/Javaアプレット.md "wikilink")のようなブラウザ埋め込み型ではなく[メディアプレーヤー](../Page/メディアプレーヤー.md "wikilink")などの外部アプリケーションのようにJava Web Startが起動する。Java Web Startがインストールされていないときは、Java Web Startソフトウェア（Java Web Startの管理・実行ソフトウェア）が自動ダウンロード、自動インストールされる。[JREがインストールされていないときは](../Page/Java_Runtime_Environment.md "wikilink")、それも自動的にインストールされる。さらに、[JRE](../Page/Java_Runtime_Environment.md "wikilink")、Java Web Startそれぞれのバージョンが古いときは自動的にアップデートされる。また、Java Web Start対応Javaアプリケーションが古く、最新バージョンがサーバにアップロードされている場合は、実行前の事前確認により自動的にアップデートされる。

なお、Java Web Start対応Javaアプリケーションはローカルマシンに保存される。よって、二回目以降の起動は、ダウンロードなどが不要となり高速に起動できる。

現在のJava Web Start は[OSとの協調動作も行なわれる](../Page/オペレーティングシステム.md "wikilink")。たとえば、[Windowsにおいて](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")「プログラムの追加と削除」を利用したJava Web Startアプリケーションのアンインストールが可能である。また、プログラムメニューや[デスクトップへのショートカットアイコンの作成なども行なわれる](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")。

## 実装

開発者はJNLP拡張子をつけた特別な[XML](../Page/Extensible_Markup_Language.md "wikilink")[ファイルを作る](../Page/ファイル_\(コンピュータ\).md "wikilink")（JNLPファイル）。このファイルはアプリケーションの要求事項、コードの場所、パラメータ、および（もしあれば）追加的な権限を指定したものだ。ブラウザはこのファイルを他のファイルと同様にダウンロードし、（その[MIMEタイプ](https://ja.wikipedia.org/wiki/MIMEタイプ "wikilink")として指定された`application/x-java-jnlp-file`に従って）それをWeb Startツールで開く。Web Startツールは、必要なすべてのリソースをダウンロードし、アプリケーションを起動する。

Java Web Startは[`javax.jnlp`](http://java.sun.com/products/javawebstart/docs/javadoc/index.html)[パッケージ内の一連の](../Page/パッケージ_\(Java\).md "wikilink")[クラス群を提供している](../Page/クラス_\(コンピュータ\).md "wikilink")。これらがアプリケーションに対して様々なサービスを提供する。これらのサービスのほとんどをSun社が設計した。その目的は、アプリケーションの動作を許可された操作の範囲内に制限しつつ、注意深く制御された範囲内のリソース（たとえばファイルや、システムクリップボードなど）にはアクセスを許可することにある。

[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")は2001年3月にWeb Startのバージョン1.0を導入した\[4\]。一方、[64ビット](../Page/64ビット.md "wikilink")版Windowsへのサポートは、（64ビット版Javaが最初に使えるようになった時よりも後になって）Java 6のみで追加された\[5\]。[J2SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") 1.4 以降、Web Startは[Java実行環境](../Page/Java_Runtime_Environment.md "wikilink")（Java Runtime Environment、JRE）に`javaws`という名前でデフォルトで入ってくるようになったので、コンピュータ管理者は、Web Startを別途インストールする必要はもはやなくなった。

## Java Network Launching Protocol (JNLP)

プログラマーたちは **Java Network Launching Protocol** (**JNLP**)の同義語として"Web Start"という用語を使うことが多い。 JNLPプロトコルは、Java Web Startアプリケーションをどのように起動するかを指定するためのものであり、XMLスキーマで定義されている。JNLPは起動メカニズムをどのように正確に実装するかを定義する規約の集まりで構成されている。JNLPファイルは[JARファイルの場所](../Page/JAR_\(ファイルフォーマット\).md "wikilink")、アプリケーションのメインクラス名、その他のパラメータなどの情報を含んでいる。適切に設定されたブラウザはJNLPファイルをJREに渡し、するとJREがそのアプリケーションをユーザーのマシン上にダウンロードし、その実行を開始する。JNLP規約の開発は [Java Community ProcessのJSR](../Page/Java_Community_Process.md "wikilink") 56で行われた。最初の1.0版リリース以降、何度か保守リリースが行われている。

Web Startの重要な機能として、ユーザがJavaをインストールしていない場合には自動的にJREをダウンロードしてインストールする機能、またプログラムを実行させるべきJREのバージョンをプログラマーが指定できる機能などがある。ダウンロードしたプログラムは、ローカルに保持したキャッシュから実行されるため、ユーザーは、そのプログラムを実行するためにインターネットに接続し続ける必要はない。ソフトウェアのアップデートはウェブからダウンロードされ、ユーザーがインターネットに接続している時に利用可能になるので、デプロイの負担を軽減できる。

いかなるコンピュータでも単純にJNLPクライアント（最も一般的にはJava Web Start）をインストールすることによりJNLPを使うことができる。このインストールも自動的に行わせることができるので、エンドユーザがJavaアプリケーションを最初に実行した時、クライアントのランチャーがダウンロードしてインストールするのをユーザーはみていればよい。

JNLPは [HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")/[HTMLがウェブのために働くのと似た働きをする](../Page/HyperText_Markup_Language.md "wikilink")。HTTP/HTMLの仕組みでは、ユーザーがウェブのリンクをクリックすると、ウェブブラウザはURLをウェブサーバに送り、ウェブサーバがHTMLファイルを返してきて、ブラウザがHTMLで書かれたウェブページを表示する。次にブラウザはこのファイルが参照しているリソース（画像、CSSなど）を要求し、十分な情報を受け取ったら最終的にページを表示する。全てのリソースのダウンロードが終わる前にページの表示が始まる場合も多い。ページのレイアウトに不可欠ではない（画像のような）いくつかのリソースは、後で追加してもよい。

JNLPは、ウェブブラウザがウェブページを表示する上記の方式を模倣している。つまり、JNLPクライアントがJavaアプリを「表示」する。ユーザがウェブのリンクをクリックすると、ブラウザはURLをウェブサーバーに送り、ウェブサーバーは指定されたアプリの（HTMLファイルではなく）JNLPファイルを返す。JNLPクライアントはこのファイルを解釈し、指定されたリソース（jarファイル群）を要求し、必要な全てのリソースを取得できるまで待ってから、アプリを起動する。JNLPファイルはいくつかのリソースを「lazy」（遅延）指定する事ができる。これは、アプリ起動のためにそれらのリソースは必要ではないので、後でアプリがそれらを要求した時に取得すればいいことをJNLPクライアントに対して示す指定である。

## JNLPファイルの例

アプレットを起動するための単純なJNLPファイルの例を下に示す。この例では、コードベース、ソース、メインクラスとウィンドウサイズを指定している。JNLPファイルは、このような形で必要な情報を全て書き込んであり、それによって自己完結的にアプリを起動できるようになっている。この例では特別な権限を要求していないので、このコードは[サンドボックス内で実行されることになる](../Page/サンドボックス_\(セキュリティ\).md "wikilink")。また、このJNLPは、このアプリがオフラインで実行できること（キャッシュ済であれば）、またバックグラウンド・プロセスでアップデートされるべきことを指定している。

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<jnlp spec="1.0+" codebase="http://ultrastudio.org/upload" href="">
    <information>
        <title>Launch applet with Web Start</title>
        <vendor>Foo Bar Inc.</vendor>
        <offline-allowed/>
    </information>
    <resources>
        <j2se version="1.5+" href="http://java.sun.com/products/autodl/j2se"/>
        <jar href="Ray-2.3-4ca60e46-0956-3f22-983c-e3ed986dfd03.jar" main="true" />
    </resources>
    <applet-desc name="Ray diagram applet" main-class="raydiagramsapplet.Main" width="300" height="200">
    </applet-desc>
  <update check="background"/>
</jnlp>
```

## Pack200 圧縮

Java Web Startアプリケーションの大きさを減らすために、サン・マイクロシステムズはJava 1.5.0において[Pack200](https://ja.wikipedia.org/wiki/Pack200 "wikilink")という圧縮方式を導入した。この圧縮方式では、大きなjarファイルがjavaクラスだけを含む場合、そのjarファイルを元の9分の1の大きさまで圧縮できる\[6\]。

Java Web Startが最初に登場したときはPack200をサポートしていたが、当初はこの機能をセットアップするために、サーバ側の協力と、ある程度の専門技術が必要であった。サン・マイクロシステムズが Java SE 6u10を導入したとき、Pack200サポートはサーバ側の特別なサポートの必要なしに使えるようになった。アプリケーション開発者はこの機能の有効/無効をJNLPファイルの中で設定できる。

遅い接続条件の下では、Pack200はアプリケーションの起動時間とダウンロード時間の性能を加速させる。

## 署名付き Web Start アプリ

デフォルト設定で Java Web Startアプリは「制限付き」で実行される。つまり、アプリはローカルファイルのようなある種のシステムリソースにはアクセス権がない。しかし、アプリ配布側がJDK付属の`jarsigner`ツールで Web Startアプリに署名しておき、ユーザ側がこの署名を受け入れて使うことに同意すれば、これらの制約を取り払うことができる。

## [MIMEタイプ](https://ja.wikipedia.org/wiki/MIMEタイプ "wikilink")における拡張子

  - .[jnlp](https://ja.wikipedia.org/wiki/jnlp "wikilink")

## 作り方

Java Web Start対応Javaアプリケーションを作るには、作成した[Swing](../Page/Swing.md "wikilink")アプリケーションに、Java Web Startの仕様に従って記述されたXML形式のファイル（拡張子\*.jnlpファイル）を追加して[ウェブサーバに](../Page/Webサーバ.md "wikilink")[アップロード](../Page/アップロード.md "wikilink")する。

## 類似技術

類似技術として[マイクロソフト](../Page/マイクロソフト.md "wikilink")が後発で開発した[ClickOnce](https://ja.wikipedia.org/wiki/ClickOnce "wikilink")（[ノータッチデプロイメント](https://ja.wikipedia.org/wiki/ノータッチデプロイメント "wikilink")）がある。

## 参考文献

## 外部リンク

  - [Sun's Java Web Start product page](http://java.sun.com/products/javawebstart/)
  - [Deploying Software with JNLP and Java Web Start](http://java.sun.com/developer/technicalArticles/Programming/jnlp/)
  - [Java Web Start Architecture JNLP Specification & API Documentation](http://java.sun.com/products/javawebstart/download-spec.html)
  - [JSR 56](http://www.jcp.org/en/jsr/detail?id=56) (JNLP 1.0, 1.5 and 6.0)
  - [Startdirectory Connect and Work](http://www.connectandwork.com/external)
  - [Java Web Start tutorial](https://archive.is/20130102062339/http://articles.techrepublic.com.com/5100-3513-6120125.html)
  - [Getting Started with Java Web Start](http://today.java.net/pub/a/today/2005/08/11/webstart.html)

[Category:ウェブ開発](https://ja.wikipedia.org/wiki/Category:ウェブ開発 "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:サン・マイクロシステムズ](https://ja.wikipedia.org/wiki/Category:サン・マイクロシステムズ "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink")

1.  [What is Java Web Start and how is it launched?](https://www.java.com/en/download/faq/java_webstart.xml)
2.  [Deprecated APIs, Features, and Options](http://www.oracle.com/technetwork/java/javase/9-deprecated-features-3745636.html)
3.  [Java Client Roadmap Update - An Oracle White Paper March 2018](http://www.oracle.com/technetwork/java/javase/javaclientroadmapupdate2018mar-4414431.pdf)
4.  [Java Web Start 1.0 press release](http://www.sun.com/smi/Press/sunflash/2001-03/sunflash.20010314.1.html)
5.  [Bug ID 4802695, Support 64-bit Java Plug-in and Java webstart on Windows/Linux on AMD64](http://bugs.sun.com/view_bug.do?bug_id=4802695)
6.  [Pack200 and Compression for Network Deployment](http://java.sun.com/javase/6/docs/technotes/guides/deployment/deployment-guide/pack200.html#pack200_compression)