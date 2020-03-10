> この記事は[CICS](https://ja.wikipedia.org/wiki/CICS)から翻訳されています。


**CICS** (**Customer Information Control System**)　は、[IBM](../Page/IBM.md "wikilink")が開発・販売している、[メインフレーム](../Page/メインフレーム.md "wikilink")を中心とした[トランザクション処理](https://ja.wikipedia.org/wiki/トランザクション処理 "wikilink")用の[ミドルウェア](https://ja.wikipedia.org/wiki/ミドルウェア "wikilink")である。

## 概要

CICSは、[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink") などの下で稼動する、[オンラインシステム](https://ja.wikipedia.org/wiki/オンラインシステム "wikilink")・[バッチ処理](https://ja.wikipedia.org/wiki/バッチ処理 "wikilink")両方に向けてデザインされたトランザクション処理システムである。

大量トランザクションの安定した処理や信頼性に加え、徹底したロギングにより、障害発生時にも処理中トランザクションの大多数の回復・整合性保持を行う。更にオプションのXRF構成の場合は、障害発生時に処理中のトランザクションの大多数を、ユーザーに障害発生を意識させる(クライアントにエラーを返す)ことなく、代替サーバに引継ぐ事ができる。

CICSは[データベース管理システム](../Page/データベース管理システム.md "wikilink") (DBMS) として、階層型の[IMS](../Page/IMS.md "wikilink")-DB、または[関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink") (RDBMS) の[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")と組み合わせる事ができる。

近年では[Webアプリケーションサーバ](https://ja.wikipedia.org/wiki/Webアプリケーションサーバ "wikilink")によるトランザクション処理が幅広く普及しているが、CICSは特にミッションクリティカルな用途の他、[Webアプリケーションサーバ](https://ja.wikipedia.org/wiki/Webアプリケーションサーバ "wikilink")から接続されるバックエンドの基幹業務の中核部分としても、[2015年](../Page/2015年.md "wikilink")現在でも使用されている。

同様のトランザクション機能をIBM AIX、Linux、Windows等の分散系OSプラットフォームで提供するミドルウェアとして、IBM TXSeries for Multiplatforms が存在する。

## 構成

CICSファミリーは以下で構成される。

  - CICS Transaction Server (CICS TS)
      - CICS の中核 堅牢なトランザクション処理を提供
  - TXSeries for Multiplatforms
      - [Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")および[オープン系](https://ja.wikipedia.org/wiki/オープン系 "wikilink") UNIX OS で CICS トランザクション処理を実現
      - V8.1は、[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](../Page/Linux.md "wikilink")で稼動
  - CICSクライアント
      - CICS Transaction Gateway (CTG)
          - 分散処理において[WebSphere Application Serverなど](../Page/WebSphere_Application_Server.md "wikilink")[アプリケーションサーバ](../Page/アプリケーションサーバ.md "wikilink")上のアプリケーションと CICS/TXSeries との連携を行う為の通信ゲートウェイ
      - CICS Universal Client (CUC)
          - CICS アプリケーションに単一のユーザー・アクセスを提供(CTGのサブセット的位置付け)
      - 3270系の表示装置や印刷装置
      - Webクライアント (J2EE Connecter Architecture など)

## バージョン

  - [1969年](https://ja.wikipedia.org/wiki/1969年 "wikilink") CICS誕生
  - [1988年](../Page/1988年.md "wikilink") CICS/MVS 2.1 (XRFサポート)
  - [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink") CICS Transaction Server に改称
  - [1999年](../Page/1999年.md "wikilink") CICS Transaction Server 1.3 （[Java](https://ja.wikipedia.org/wiki/Java "wikilink")サポート、CICS Webサポート(CWS)）
  - [2007年](../Page/2007年.md "wikilink") CICS Transaction Server 3.2 （[Webサービス](https://ja.wikipedia.org/wiki/Webサービス "wikilink")強化）
  - [2009年](../Page/2009年.md "wikilink") CICS Transaction Server 4.1 （イベント処理のサポート、CICS Explorerなど）
  - [2011年](../Page/2011年.md "wikilink") CICS Transaction Server 4.2 （新しいシステム・イベント、新しい[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")の [Java](https://ja.wikipedia.org/wiki/Java "wikilink")ランタイム環境など）
  - [2012年](../Page/2012年.md "wikilink") CICS Transaction Server 5.1 （Liberty/モバイルによるアジリティ向上と基盤強化）
  - [2014年](../Page/2014年.md "wikilink") CICS Transaction Server 5.2 （更なるサービスアジリティ向上とクラウド・イネーブルメント）\[1\]
  - [2015年](../Page/2015年.md "wikilink") CICS Transaction Server 5.3\[2\]

## 詳細

CICSオンライントランザクションシステムを利用すると、[System zなどIBMの大型コンピュータ](https://ja.wikipedia.org/wiki/System_z "wikilink")（[メインフレーム](../Page/メインフレーム.md "wikilink")）上で、数千トランザクション毎秒の[オンライントランザクション処理が可能となり](../Page/トランザクション.md "wikilink")、大企業から中規模企業に至る企業における中核システムの役割を担うことができる。CICS上で稼働する[アプリケーションプログラムを作成するために](../Page/アプリケーションソフトウェア.md "wikilink")、[プログラミング言語](../Page/プログラミング言語.md "wikilink")として、[COBOL](../Page/COBOL.md "wikilink")、[PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")、[C](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")、[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")、[REXX](https://ja.wikipedia.org/wiki/REXX "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")などが利用できる。

CICSオンライントランザクションシステム上で動く業務アプリケーションプログラムには、CICSによりトランザクションIDが割り振られる。CICSアプリケーションの画面は、マップという単位でCICSにより管理される。このマップを経由して、エンドユーザー入力のデータがプログラムに渡される。CICSの画面の文字表示では、高輝度ハイライト、さまざまな色、点滅などが利用できる。

マップがCOBOLを通してどのように送られるかを、以下に示す。

`EXEC CICS`
`    SEND MAPSET(MPS1) MAP(MP1)`
`END-EXEC.`

CICSは[銀行](../Page/銀行.md "wikilink")の[現金自動預け払い機](../Page/現金自動預け払い機.md "wikilink")、流通、[信販](https://ja.wikipedia.org/wiki/信販 "wikilink")、[航空会社](../Page/航空会社.md "wikilink")の予約システム、工場の生産管理システムなどさまざまなオンライントランザクションシステムで使われている。

一般的な位置付けは、銀行など金融業界で求められる超高度なオンラインシステムのプラットホームとしての[IMS TMに次ぐ](../Page/IMS.md "wikilink")、高度な信頼性かつ運用経済性が求められるオンライントランザクションシステムのプラットホームとして利用されている。

CICSは当初アメリカの[公益事業](https://ja.wikipedia.org/wiki/公益事業 "wikilink")ユーティリティー業界（電力・ガス・水道）のために[イリノイ州](../Page/イリノイ州.md "wikilink")デプレーン（[Des Plaines](https://ja.wikipedia.org/wiki/:en:Des_Plaines,_Illinois "wikilink")）にあった営業部門の開発グループで1966年から開発され、1968年に別の名称で発表された。その後[パロアルトのIBM開発部門で開発が続いて](https://ja.wikipedia.org/wiki/パロアルト_\(カリフォルニア州\) "wikilink")、正式にCICSとして発表されたのは[1969年](https://ja.wikipedia.org/wiki/1969年 "wikilink")[7月8日](https://ja.wikipedia.org/wiki/7月8日 "wikilink")のことで、[IMS](../Page/IMS.md "wikilink")の登場後間もないときのことである。[1974年](../Page/1974年.md "wikilink")には[IMS](../Page/IMS.md "wikilink")に注力するために開発中止が決定されたが、折よく[IBMハーズレイ](https://ja.wikipedia.org/wiki/IBMハーズレイ "wikilink")開発研究所（[IBM Hursley](https://ja.wikipedia.org/wiki/:en:IBM_Hursley "wikilink")、[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")）で[PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")コンパイラーの開発を終了した人員に拾われて開発が続き、今でもそこでメンテナンス・開発がされている。

[1980年代](../Page/1980年代.md "wikilink")から[1990年代](../Page/1990年代.md "wikilink")、CICSの一部は、[アントニー・ホーア](../Page/アントニー・ホーア.md "wikilink")の指揮の下、[Oxford University Computing Laboratoryとの](https://ja.wikipedia.org/wiki/w:Oxford_University_Computing_Laboratory "wikilink")[コラボレーション](https://ja.wikipedia.org/wiki/コラボレーション "wikilink")で、[Z言語](https://ja.wikipedia.org/wiki/Z言語 "wikilink")を使って整えられた。

近年は、CICSの拡張は[Webサービス](https://ja.wikipedia.org/wiki/Webサービス "wikilink")や[Enterprise JavaBeans](../Page/Enterprise_JavaBeans.md "wikilink") (EJB) のサポートを含む。2007年リリースされたバージョンは、「CICS Transaction Server Version 3.2 for z/OS」であり、[COBOL](../Page/COBOL.md "wikilink")、[C](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")、[PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")などの言語が利用でき、また[Webサービス](https://ja.wikipedia.org/wiki/Webサービス "wikilink")をサポートしている。

## 脚注

<references />

## 関連項目

  - [トランザクションモニター](../Page/トランザクションモニター.md "wikilink")
      - [IMS](../Page/IMS.md "wikilink") - CICSとIMS-DBの組み合わせが可能
      - [WebSphere](../Page/WebSphere.md "wikilink")
  - [IBM 3270](https://ja.wikipedia.org/wiki/IBM_3270 "wikilink") - CICS端末として定義可能
  - メインフレーム市場の競合製品
      - [AIM](../Page/AIM.md "wikilink") - [富士通](../Page/富士通.md "wikilink")
      - [XDM](https://ja.wikipedia.org/wiki/XDM_\(データベース\) "wikilink") - [日立製作所](../Page/日立製作所.md "wikilink")
      - [VIS](../Page/VIS_\(汎用機\).md "wikilink") - [NEC](../Page/日本電気.md "wikilink")

## 外部リンク

  - [製品ページ - 日本IBM](http://www-03.ibm.com/software/products/ja/cics-tserver-zos)
  - [CICS - IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/ja/SSGMGV/welcome.html)

[Category:トランザクションモニター](https://ja.wikipedia.org/wiki/Category:トランザクションモニター "wikilink") [Category:IBMのソフトウェア](https://ja.wikipedia.org/wiki/Category:IBMのソフトウェア "wikilink") [Category:形式手法](https://ja.wikipedia.org/wiki/Category:形式手法 "wikilink")

1.  [IBM CICS Transaction Server for z/OS V5.2 は、サービスの俊敏性、運用効率、およびクラウド・イネーブルメントを新たなレベルへ進化させます - IBM](http://www-01.ibm.com/common/ssi/cgi-bin/ssialias?infotype=an&subtype=ca&appname=gpateam&supplier=760&letternum=JAJPJP14-0134)
2.  [IBM CICS Transaction Server for z/OS V5.3 は、サービスの俊敏性、運用効率、クラウド・イネーブルメントを DevOps により進化させます](http://www-01.ibm.com/common/ssi/ShowDoc.wss?docURL=/common/ssi/rep_ca/3/760/JAJPJP15-0493/index.html&lang=ja&request_locale=ja)