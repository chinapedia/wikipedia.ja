> この記事は[WebSphere Application Server](https://ja.wikipedia.org/wiki/WebSphere_Application_Server)から翻訳されています。


**WebSphere Application Server** (ウェブスフィア・アプリケーション・サーバー、**WAS**、ワズ)は、[IBM](../Page/IBM.md "wikilink")が開発・販売する、[Java EE対応の](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")[アプリケーションサーバ](https://ja.wikipedia.org/wiki/アプリケーションサーバ "wikilink")（[ミドルウェア](https://ja.wikipedia.org/wiki/ミドルウェア "wikilink")）であり、IBMソフトウェアの[WebSphere](../Page/WebSphere.md "wikilink")ブランドの中核をなす製品でもある。

## 概要

WASは[J2EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")、[XML](../Page/Extensible_Markup_Language.md "wikilink")、[Webサービス](https://ja.wikipedia.org/wiki/Webサービス "wikilink")といったオープンな標準で構築されている。世界各地のIBMの研究部門で WebSphere のランタイム製品や開発ツールが作られている。

特徴として[メインフレーム](../Page/メインフレーム.md "wikilink")版 (WebSphere Application Server for [z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")) から、[Windowsまでのスケーラビリティと](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、大規模システムを含む多数の実績と信頼性が挙げられている。

WASはその他のアプリケーションサーバ同様に、HTTPトランスポートチャネルを持っているため、単独でWEBサーバー機能を提供可能だが、プラグインを利用することで[Webサーバ](../Page/Webサーバ.md "wikilink")のバックエンドとしても動作可能である。 以下のWebサーバをサポートする。

  - [Apache HTTP Server](../Page/Apache_HTTP_Server.md "wikilink")
  - [Netscape Enterprise Server](https://ja.wikipedia.org/wiki/Netscape_Enterprise_Server "wikilink")
  - Microsoft [Internet Information Services](../Page/Internet_Information_Services.md "wikilink") (IIS)
  - [IBM HTTP Server](https://ja.wikipedia.org/wiki/IBM_HTTP_Server "wikilink") (IHS) （[i5/OS用](https://ja.wikipedia.org/wiki/OS/400 "wikilink")、[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")用、[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")/[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")/[Solaris](../Page/Solaris.md "wikilink")/[Windows用](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")）

製品パッケージは、各プラットフォームごとに機能の範囲により複数のパッケージがあるが、主なものには以下がある。

  - WebSphere Application Server（Base版）- WAS本体（[IBM HTTP Server](https://ja.wikipedia.org/wiki/IBM_HTTP_Server "wikilink")(IHS)同梱）
  - WebSphere Application Server Express（Express版）- Base版と機能は同等であるが、プラットフォームやライセンス条件に制限がある
  - WebSphere Application Server Network Deployment（ND版）- Base版にクラスタ対応（Edgeコンポーネント、セッション共有、Deployment Managerなど）を追加したもの
  - WebSphere Application Server Community Edition（通称 WAS-CE（ワズ・シー・イー））- Apache Geronimoベースの無償で軽量な J2EE™ 準拠のアプリケーション・サーバー

## バージョン

最初のベータ版は *Servlet Express* と呼ばれていた。

  - バージョン 1 （1998年6月）
    [Java Servletエンジンに基づく実装](../Page/Java_Servlet.md "wikilink")
  - バージョン 2 （1999年4月）
    [Java Beansと](https://ja.wikipedia.org/wiki/Java_Beans "wikilink")[CORBAをサポート](../Page/Common_Object_Request_Broker_Architecture.md "wikilink")。[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")サポート。Standard Edition (SE) と Advanced Edition (AE) がある。
  - バージョン 3 （1999年11月30日）
    [JDK](../Page/Java_Development_Kit.md "wikilink") 1.1.6〜1.1.8およびJ2EE 1.0準拠。J2EE 1.0に各種拡張を施している。[OS/400](https://ja.wikipedia.org/wiki/OS/400 "wikilink")（現在のi5/OS）と[OS/390](https://ja.wikipedia.org/wiki/OS/390 "wikilink")（現在のz/OS）を追加サポートしたが、v5.xまでz/OSバージョンは全く別のコードベースであった。SE/AEに加えて、Enterprise Edition (EE) が追加された。
  - バージョン 3.5 （2000年7月26日）
    ベースとなる実行環境を[JDK](../Page/Java_Development_Kit.md "wikilink") 1.2.2 にバージョンアップ。
  - バージョン 4
    J2EE 1.2準拠。Advanced Edition single (AEs) と Developer Edition (AEd) が追加された。AEs と AEd はクラスター構成では動作できないバージョン（AEd は開発用途限定）。
  - バージョン 5 （2002年11月19日）
    J2EE 1.3準拠。コードベースが一新され、プラットフォーム間で共通のコードベースを使うようになり、パーソナルコンピュータからメインフレームまで同じコードが使われている。[XMLファイルによる構成リポジトリ](../Page/Extensible_Markup_Language.md "wikilink")。**Deployment Server**と呼ばれるサービスに構成のマスターコピーがあり、各ノードがそこからコピーすべきものを指定するファイルを持っている。[Java Message Service](../Page/Java_Message_Service.md "wikilink") (JMS) サーバ機能が組み込まれており、これは [WebSphere MQ](../Page/WebSphere_MQ.md "wikilink") 5.3 の機能限定版である。
  - バージョン 5.1 （2004年4月）
    JDKが1.4.2にアップデートされ、[Java Tclに加えて](https://ja.wikipedia.org/wiki/Java_Tcl "wikilink")[Jython](https://ja.wikipedia.org/wiki/Jython "wikilink")をスクリプト言語として採用。
  - バージョン 6 （2004年12月）
    [J2EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink") 1.4準拠。セキュリティが強化されている（[WS-Security](https://ja.wikipedia.org/wiki/WS-Security "wikilink")など）。
  - バージョン 6.1 （2006年5月）
    Java Standard Edition 1.5サポート。[JSR](https://ja.wikipedia.org/wiki/Java_Community_Process "wikilink") 160、JSR 168をサポート。[SIPサーブレット](https://ja.wikipedia.org/wiki/Session_Initiation_Protocol "wikilink")。JSF[ウィジェット](https://ja.wikipedia.org/wiki/ウィジェット "wikilink")ライブラリ。世代別GCなどが提供される新しいVM - J9 JVM。
  - WebServices Feature Pack （2006年10月）
    ベータ版として配布された。既存のWebSphere 6.1上で機能する。[StAX](../Page/Streaming_API_for_XML.md "wikilink")、[WS-Addressing](https://ja.wikipedia.org/wiki/WS-Addressing "wikilink")、[JAXB](https://ja.wikipedia.org/wiki/JAXB "wikilink")、[SOAPメッセージ転送最適化機構](../Page/SOAP_\(プロトコル\).md "wikilink") (MTOM) などを（一部は限定的に）サポート。
  - バージョン 7.0 （2008年9月）
    Java 6.0。Java EE 5.0認定。
  - バージョン 8.0 （2011年6月）
    Java 6.0。Java EE 6.0準拠。Javaバッチ。
  - バージョン 8.5 （2012年6月）
    Java 7.0。軽量で高速起動可能な新しい環境Liberty Profile。アプリケーション・エディション管理機能。
  - バージョン 9.0 （2016年6月）
    Java 8.0。Java EE 7.0認定。
    Libertyランタイムは、2018年6月リリースの、18.0.0.2で、Java EE 8準拠。\[1\]

## 脚注

## 関連項目

  - [Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")
  - [アプリケーションサーバ](https://ja.wikipedia.org/wiki/アプリケーションサーバ "wikilink")

## 外部リンク

  - [IBM WebSphere Application Server詳細](https://www.ibm.com/jp-ja/marketplace/java-ee-runtime)
  - [IBM マーケットプレイス](https://www.ibm.com/jp-ja/products)
  - [IBM ソフトウェア](https://www.ibm.com/software/jp/)
  - [IBM 無料評価版](https://www.ibm.com/software/jp/info/trials/)
  - [WebSphere Application Server - IBM Knowledge Center](http://www.ibm.com/support/knowledgecenter/ja/SSEQTP/mapfiles/product_welcome_was.html)
  - [Recommended updates for WebSphere Application Server - IBM](http://www-1.ibm.com/support/docview.wss?rs=180&context=SSEQTP&uid=swg27004980)

[Category:ウェブアプリケーション](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーション "wikilink") [Category:Java_enterprise_platform](https://ja.wikipedia.org/wiki/Category:Java_enterprise_platform "wikilink") [Category:IBMのソフトウェア](https://ja.wikipedia.org/wiki/Category:IBMのソフトウェア "wikilink") [Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink")

1.