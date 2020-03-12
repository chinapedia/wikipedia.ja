> この記事は[WebSphere MQ](https://ja.wikipedia.org/wiki/WebSphere_MQ)から翻訳されています。


**IBM MQ**は、[IBM](../Page/IBM.md "wikilink")が開発・販売する[メッセージングミドルウェアである](../Page/メッセージ指向ミドルウェア.md "wikilink")。1992年に**MQSeries**の名称で登場し、2002年に[WebSphere](../Page/WebSphere.md "wikilink")ブランドに組み込まれ**WebSphre MQ**と改名され、2014年に現在のIBM MQと改名された。[メッセージキュー](../Page/メッセージキュー.md "wikilink")方式の信頼性が高く非同期通信も可能なマルチプラットフォーム対応の[メッセージ](../Page/メッセージ.md "wikilink")通信を提供する。このためシステム連携のためのメッセージング・[ミドルウェア](../Page/ミドルウェア.md "wikilink")として使用される場合が多い。

## 歴史

  - MQSeriesリリース前
      - [1964年](../Page/1964年.md "wikilink") [System/360](https://ja.wikipedia.org/wiki/System/360 "wikilink")がリリースされたとき、BTAM と QTAM（Basic and Queued Telecommunication Access Methods）が通信手法として提供された。
      - [1971年](https://ja.wikipedia.org/wiki/1971年 "wikilink") TSO（Time-Sharing Option）と共に TCAM（Telecommunication Access Method）が登場。
      - [1971年](https://ja.wikipedia.org/wiki/1971年 "wikilink")12月 [CICS](../Page/CICS.md "wikilink")とTCAMの連携が発表され、[1972年](../Page/1972年.md "wikilink")12月にリリース。

<!-- end list -->

  - MQSeries時代
      - [1993年](../Page/1993年.md "wikilink") MQSeries V1（メッセージ・キューイング。TCAM の機能を IBM 以外のプラットフォームでも使えるよう拡張した）
      - [1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink") MQSeries V2（分散系プラットフォームへの拡張、トリガリング、コード変換、プライオリティ、Non-Persistentメッセージ）
      - [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink") MQSeries V5.0（メッセージサイズ拡張、[C++](../Page/C++.md "wikilink")や[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のサポート ）
      - [1999年](../Page/1999年.md "wikilink") MQSeries V5.1（クラスタリング（MQクラスター）、[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")管理ツール（MQエクスプローラ） ）
      - [2001年](../Page/2001年.md "wikilink") MQSeries V5.2（パフォーマンス改善、[Linux](../Page/Linux.md "wikilink")のサポート）

<!-- end list -->

  - WebSphere MQ時代
      - [2002年](../Page/2002年.md "wikilink") WebSphere MQ V5.3（MQSeries から名称変更、SSLサポート）
      - [2004年](../Page/2004年.md "wikilink") [王立工学アカデミー](https://ja.wikipedia.org/wiki/王立工学アカデミー "wikilink")\[[http://www.raeng.co.uk\]から](http://www.raeng.co.uk%5Dから) MacRobert 賞[1](http://www.raeng.co.uk/prizes/macrobert/%5Dを授与された%5Bhttp://www.raeng.co.uk/prizes/macrobert/winners/win2004.htm)。
      - [2005年](../Page/2005年.md "wikilink") WebSphere MQ V6（[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")対応、[Eclipseベースの](../Page/Eclipse_\(統合開発環境\).md "wikilink")[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")）
      - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")4月 WebSphere MQ V7.0（パブリッシュ/サブスクライブ・メッセージングおよび[JMSの拡張](../Page/Java_Message_Service.md "wikilink")）
      - [2014年](../Page/2014年.md "wikilink")3月 IBM MQ V8.0
      - [2016年](../Page/2016年.md "wikilink")6月 IBM MQ V9.0\[1\]

## 機能

WebSphere MQ は各種プラットフォームでの時間を保証したメッセージ配信を行う。メッセージ交換の信頼性と堅牢性を強化し、メッセージを失わないことを保証する。

MQ は時間に依存しないアーキテクチャを構成する機構も提供する。メッセージをあるアプリケーションから別のアプリケーションに送信するとき、相手のアプリケーションがその時点で動作していなくてもよい。受信側アプリケーションが動作していないときにメッセージが送られた場合、キューマネージャが受信側が問い合わせてくるまでそれを保持しておく。メッセージの順序性は[FIFO](../Page/FIFO.md "wikilink")順で保持される。これは WebSphere MQ のキューマネージャに限った機能ではない。

通信相手のアーキテクチャの違いを WebSphere MQ で変換することによって対応することができる。例えば、[ビッグエンディアンから](https://ja.wikipedia.org/wiki/エンディアン "wikilink")[リトルエンディアンへの変換や](https://ja.wikipedia.org/wiki/エンディアン "wikilink")[EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink")から[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")への変換である。これは、"Exits" と呼ばれるアプリケーションコードで実行される。Exits はキューマネージャ上で動作し、必要に応じてデータ変換を行う。

WebSphere MQ は他のアプリケーションを起動するためのメッセージを受け付けて起動を実施できる。これによりメッセージ駆動型アーキテクチャを実現できる。

## 通信

WebSphere MQ の中核となるのは「キューマネージャ」(**MQ Manager**、**MQM**)である。キューマネージャは記憶装置を操作し、タイミング問題を扱い、アプリケーション起動を行い、その他のデータの転送には直接関係しない機能を持っている。

キューマネージャは、同じホスト上で動作するソフトウェアとは **Bindings** と呼ばれるコネクションを持ち、ネットワーク経由では他のホスト上のソフトウェアとの間で **Client** と呼ばれるコネクションを持つ。同じホスト上のソフトウェアと Client コネクションで繋げることもできる。Bindings の方が高速だが Client の方が堅牢であり、アプリケーションの設計を容易に変更可能である。

キューマネージャ間の通信は **Channel** と呼ばれる別のプログラムが担当する。Channel はキューマネージャと同じホスト上で動作し、ネットワーク経由のデータ送受信を受け持つ。TCP/IP のネットワークでは、Channel は特定のポートでデータの送受信を行う。

Client コネクションでアプリケーションとキューマネージャ間の通信を行うプログラムは Listener と呼ばれる。Listener はアプリケーションから見たキューマネージャのネットワークインタフェースとなっている。TCP/IP ネットワークでは、Listener は特定ポート上で "listen" する（パケット受信を待ち受けること）。

## メッセージ指向ミドルウェア (MOM)

メッセージのキューイングは2つの部分からなる。

  - **メッセージ**とは、[バイナリ](../Page/バイナリ.md "wikilink")または[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")のデータの集合体であり、関係するプログラムにとって意味のある内容である。[通信プロトコル](../Page/通信プロトコル.md "wikilink")としては、ルーティングなどの情報が転送前にメッセージに付与され、受信先アプリケーションに到達する前にそれら情報が捨てられ、メッセージだけが届けられる。
  - **メッセージキュー**とは、アプリケーション内でメッセージを格納するオブジェクトである。

「キューマネージャ」は MOM に必ずあるわけではないが、WebSphere MQ では必要不可欠であり、メッセージキューの論理的コンテナを提供するシステムサービスであると共に、「メッセージチャンネル」を経由してメッセージを他のキューに転送する役割を持つ。

この技術の利点は以下の通り。

  - メッセージは[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")のような純粋な[パケット](../Page/パケット.md "wikilink")通信による転送に依存しない。このため、送受信を行うアプリケーション同士の[結合度](../Page/結合度.md "wikilink")が弱く、非同期な運用も可能である。
  - メッセージは一度しか送られない。ネットワーク上の問題は全てキューマネージャが対応する。

## API

WebSphere MQ の機能を利用する方法はいくつもある。IBM がサポートする [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") として以下のものがある。

  - IBM Message Queue Interface (MQI) : [C言語](../Page/C言語.md "wikilink")、[COBOL](../Page/COBOL.md "wikilink")、[PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")
  - Java 向けには J2EE で標準化された [JMS](../Page/Java_Message_Service.md "wikilink") もある。
  - C/C++ と .NET 向けの XMS[2](http://www-128.ibm.com/developerworks/websphere/library/techarticles/0509_phillips/0509_phillips.html)

IBMがサポートする以外にも各種APIが存在する。例えば、[モルガン・スタンレー](../Page/モルガン・スタンレー.md "wikilink")が開発した[Perl](../Page/Perl.md "wikilink")用インタフェースが[CPAN](../Page/CPAN.md "wikilink")から入手可能である。[3](http://search.cpan.org/~hbiersma/MQSeries-1.23/MQSeries.pm)

## 出典

<references />

## 外部リンク

  - [IBM マーケットプレイス](https://www.ibm.com/jp-ja/products)
  - [IBM ソフトウェア](https://www.ibm.com/software/jp/)
  - [IBM 無料評価版](https://www.ibm.com/software/jp/info/trials/)
  - [IBM Knowledge Center - MQ概要 - V8.0](https://www.ibm.com/support/knowledgecenter/ja/SSFKSJ_8.0.0/com.ibm.mq.pro.doc/q001020_.htm)

[Category:分散処理](https://ja.wikipedia.org/wiki/Category:分散処理 "wikilink") [Category:システムソフトウェア](https://ja.wikipedia.org/wiki/Category:システムソフトウェア "wikilink") [Category:IBMのソフトウェア](https://ja.wikipedia.org/wiki/Category:IBMのソフトウェア "wikilink")

1.  [IBM MQ V9.0 delivers new, more flexible delivery and support options, enhanced encryption configurations, self-service enhancements, and updates to managed file transfer capabilities](http://www-01.ibm.com/common/ssi/cgi-bin/ssialias?subtype=ca&infotype=an&appname=iSource&supplier=897&letternum=ENUS216-153)