> この記事は[BlackBerry Enterprise Service](https://ja.wikipedia.org/wiki/BlackBerry_Enterprise_Service)から翻訳されています。


**BlackBerry Enterprise Service**（ブラックベリーエンタープライズサービス）は、[カナダ](https://ja.wikipedia.org/wiki/カナダ "wikilink")の[ブラックベリーが提供する](https://ja.wikipedia.org/wiki/ブラックベリー_\(企業\) "wikilink")[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")・[BlackBerry](https://ja.wikipedia.org/wiki/BlackBerry "wikilink")の企業向けサービス。

**BlackBerryサービス全般は「[BlackBerry](https://ja.wikipedia.org/wiki/BlackBerry "wikilink")」を参照**

## 概要

BlackBerry端末で、企業が設置する[IBM](../Page/IBM.md "wikilink")の[Lotus Notesや](https://ja.wikipedia.org/wiki/Lotus_Notes "wikilink")[Microsoft Exchange Server](../Page/Microsoft_Exchange_Server.md "wikilink")・[Novell GroupWiseの](../Page/Novell_GroupWise.md "wikilink")[メールの送受信](../Page/電子メール.md "wikilink")、[PIM](https://ja.wikipedia.org/wiki/Personal_Information_Manager "wikilink")（アドレス帳、スケジューラー、Todo、ドキュメント等）との同期を図ることができる。ユーザー側は特に端末をさわらなくても、[プッシュ型電子メール](https://ja.wikipedia.org/wiki/プッシュ型電子メール "wikilink")でメールが着信したり、スケジュールが更新される。クライアント側で接続する際の細かい設定を行う必要なく、セキュアな社内アクセスができるため、欧米の多くの企業、官公庁で利用されている。これらの仕組みを構築するためには[BlackBerry Enterprise Server](https://ja.wikipedia.org/wiki/BlackBerry_Enterprise_Server "wikilink") (BES) という[ミドルウェア](https://ja.wikipedia.org/wiki/ミドルウェア "wikilink")を設置する。\[1\]企業のメールがPush Email着信することや、通信の[セキュリティー](https://ja.wikipedia.org/wiki/セキュリティー "wikilink")の高さから、海外では多くの企業や[政府機関](https://ja.wikipedia.org/wiki/政府機関 "wikilink")などが利用している。 サーバからはITポリシーといわれる条件を端末にリモートで割り当てることができる。 [BlackBerry Enterprise Server](https://ja.wikipedia.org/wiki/BlackBerry_Enterprise_Server "wikilink") (BES) としての開発は停止されているが、2015年9月に買収した[グッド・テクノロジー](https://ja.wikipedia.org/wiki/グッド・テクノロジー "wikilink")社の同機能製品を統合し、2016年12月より[BlackBerry Unified Endpoint Management](https://ja.wikipedia.org/wiki/BlackBerry_Unified_Endpoint_Management "wikilink") (BlackBerry UEM) と改称して開発・提供が継続されている\[2\]。

### 日本での展開

日本では2006年9月よりBlackBerry Enterprise Server及びBlackBerry端末 (8707h) の提供が[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")より開始されている。\[3\]発売当初は端末もサーバも英語版だけであったが、現在は双方とも日本語版が提供されている。

2015年9月7日、同業の法人向けモバイル管理大手[グッド・テクノロジー](https://ja.wikipedia.org/wiki/グッド・テクノロジー "wikilink")社の買収合意を発表\[4\]。NTTドコモはBlackBerryブランドとして[グッド・テクノロジー](https://ja.wikipedia.org/wiki/グッド・テクノロジー "wikilink")社の[モバイル端末管理ソリューションの販売を継続している](https://ja.wikipedia.org/wiki/Mobile_Device_Management "wikilink")\[5\]。

2015年11月30日をもって旧BlackBerry Enterprise Serverについては新規受付を終了し、2017年3月31日限りでサービスを終了する予定である\[6\]。

2016年7月27日、日本で法人向けソフトウェア事業の再開を発表している\[7\]。

#### 日本語対応バージョン

  - 4.1.4J
  - 4.1.6
  - 4.1.7
  - 5.0.1
  - 5.0.2

| 日本語版動作確認環境                   |
| ---------------------------- |
| 項目                           |
| BlackBerry　Enterprise Server |
| Microsoft Exchange           |
| グループウェア                      |
| IBM Notes Domino             |
| グループウェア                      |

#### BlackBerry Internet Service

  -
    BlackBerry Enterprise Serviceは、[Microsoft Exchange Serverや](../Page/Microsoft_Exchange_Server.md "wikilink")[Lotus Domino導入企業向けのソリューションであるが](https://ja.wikipedia.org/wiki/Lotus_Domino "wikilink")、[中小企業](../Page/中小企業.md "wikilink")、個人向けサービスとして[POP](../Page/Post_Office_Protocol.md "wikilink")、[IMAPメールのプッシュメール送受信が特徴の](../Page/Internet_Message_Access_Protocol.md "wikilink")[BlackBerry Internet Service](../Page/BlackBerry_Internet_Service.md "wikilink") (BIS) も2008年8月より日本でも利用可能となった。

#### BlackBerry Dual Service

  -
    更にBlackBerry Enterprise Serviceと[BlackBerry Internet Serviceが](../Page/BlackBerry_Internet_Service.md "wikilink")1台の端末で両方使えるサービスであるBlackBerry Dual Serviceも2008年9月より開始されている。

## BlackBerry Enterprise Server

このサービスを利用するためにはBlackBerry Enterprise Server (BES) というミドルウェアを[Exchange Serverや](https://ja.wikipedia.org/wiki/Exchange_Server "wikilink")[Lotus Domino等](https://ja.wikipedia.org/wiki/Lotus_Domino "wikilink")[グループウェア](../Page/グループウェア.md "wikilink")サーバと同じセグメント上に設置する必要がある。BlackBerry Enterprise Serverは各グループウェアサーバと常に同期をとり、各クライアントであるBlackBerry端末にメールの配信、スケジュール等の[PIMの同期をおこなう](https://ja.wikipedia.org/wiki/Personal_Information_Manager "wikilink")。BlackBerry Enterprise Serverはメールの配信、PIMの同期、のほかに[データベース](../Page/データベース.md "wikilink")との同期、[添付ファイル](https://ja.wikipedia.org/wiki/添付ファイル "wikilink")の保存等、機能ごとに付加分散させることもできる。2008年9月時点での最新バージョンはｖ4.1.6で[60日間のトライアル版](http://smartphone.nttdocomo.co.jp/support/dl.html)がある。

### サーバ・クライアント間の通信

BlackBerry Enterprise ServerとBlackBerry端末の間インターネットや、各通信キャリアのパケット網を経由するが[3DES](https://ja.wikipedia.org/wiki/3DES "wikilink")や[AESでの暗号化通信をかけて通信を行うためセキュアな通信を行うことができる](../Page/Advanced_Encryption_Standard.md "wikilink")。

  - 通信経路
    BlackBerry端末⇔（パケット網）⇔通信キャリア⇔（専用線等）⇔[ブラックベリー](https://ja.wikipedia.org/wiki/ブラックベリー_\(企業\) "wikilink")⇔（インターネット）⇔BES⇔（LAN「[mapi](https://ja.wikipedia.org/wiki/mapi "wikilink")等」）⇔[グループウェア](../Page/グループウェア.md "wikilink")サーバ

### アクティベーション

BlackBerry端末からBlackBerry Enterprise Serverを経由してグループウェアへのアクセス、メールの送受信をおこなうには、BlackBerry端末側で[アクティベーション](https://ja.wikipedia.org/wiki/アクティベーション "wikilink")（端末のアクティブ化）を行う必要がある。これはBESの管理者が[クライアントのメールアドレスに紐づいたパスワードを発行し](../Page/クライアント_\(コンピュータ\).md "wikilink")、端末にそのメールアドレスとパスワードを入力することによりアクティベーションを行う。アクティベーションは無線を使って行う方法と、サーバと直接[USBケーブルと接続する方法](../Page/ユニバーサル・シリアル・バス.md "wikilink")、サーバーと同一ネットワーク内のPCとBlackBerry端末をUSBで接続する方法の3パターンがある。クライアント端末はアクティベーションを実行するだけで、自動的にBlackBerry Enterprise Serverにアクセスし、メールの送受信やPIMの同期ができるようになる。

### サーバの機能

## 特徴

### メールの送受信

Lotus NotesやMicrosoft Exchange Serverのメールの送受信が可能。メールがメールサーバに着信すると、BlackBerry Enterprise ServerがBlackBerry端末にメールをプッシュで配信する。またBlackBerry端末でメールを送信すると、送信の履歴がLotus Notes、Microsoft Exchange Serverのメールクライアントにも残る。メールの添付ファイルは一度BESの側に蓄積され、BlackBerry端末から要求があった際に送信する。送信する際も、\[添付ファイルのページ毎に送信することも可能である。メールの添付ファイルは[Word](../Page/Microsoft_Word.md "wikilink")、[Excel](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")、[PDF](../Page/Portable_Document_Format.md "wikilink")、[PowerPoint](https://ja.wikipedia.org/wiki/Microsoft_PowerPoint "wikilink")、[JPEG](../Page/JPEG.md "wikilink")、[tiff](https://ja.wikipedia.org/wiki/tiff "wikilink")、[png](https://ja.wikipedia.org/wiki/png "wikilink")、[gif](https://ja.wikipedia.org/wiki/gif "wikilink")、[bmp](https://ja.wikipedia.org/wiki/bmp "wikilink")等の閲覧が可能で、機種によっては[Documents To Goというアプリケーションを利用してWord](https://ja.wikipedia.org/wiki/Documents_To_Go "wikilink")、Excelの編集も可能\[8\]である。

### PIM同期

Lotus NotesやMicrosoft Exchange Serverのアドレス帳、スケジューラー、ToDo、ドキュメントとの同期を行うことができる。BlackBerry端末から、グループ内の人の会議招集を実施することも可能。同期を取る際リモートだけでなく、クライアントPCとUSBケーブルを利用して同期をとることも可能である。

### ITポリシー

  -
    サーバー側からBlackBerry端末に対し、端末毎、グループ毎に機能を制限することができる。（[SMS](https://ja.wikipedia.org/wiki/SMS "wikilink")を使わせない、通話をさせない、[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")アプリをインストールさせない等）

### セキュリティー

  - 暗号化
    BESか端末までの通信は[3DES](../Page/トリプルDES.md "wikilink")、[AES等で暗号化をかけており](../Page/Advanced_Encryption_Standard.md "wikilink")、その通信を傍受することは、現状不可能とされている。
  - 遠隔制御
    BlackBerry端末を紛失した際など、BlackBerry Enterprise Server (BES) から遠隔で端末の通信をとめたり、リモートワイプという、端末の遠隔での[初期化](https://ja.wikipedia.org/wiki/初期化 "wikilink")を実施することができる。

## BlackBerry Enterprise Server Express

BlackBerry Enterprise Server Express は[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")8月にRIMから提供されたBlackBerry Enterprise Serverが無料で利用できるアプリケーションとなる。日本語にも対応している。

無料であるため、有料版にくらべある程度の制限があるが基本的な機能は同とである。また2010年8月時点ではMicrosoft Exchange ServerとMicrosoft Small Business Serverでのみの利用に限られていたが、2010年11月からはLotus Domino版の提供も開始された。

制限として、利用人数が専用サーバでは 2000人強、またはプライマリメールサーバ2では75名までとなる。
冗長化構成がとれない（もともと4.1.7以前でもとれない）、ITポリシーが75種類に制限される。\[9\] \[10\]

## 脚注

## 外部リンク

  - [リサーチ・イン・モーション (RIM) 日本語サイト](http://ap.blackberry.com/jpn/)
  - [BlackBerry Enterprise Server (RIM) 英語サイト](http://na.blackberry.com/eng/services/server/)
  - [NTTドコモBlackBerryサイト](http://smartphone.nttdocomo.co.jp)

[Category:携帯電話ブラウジング](https://ja.wikipedia.org/wiki/Category:携帯電話ブラウジング "wikilink") [Category:アプリケーションソフト_(製品)](https://ja.wikipedia.org/wiki/Category:アプリケーションソフト_\(製品\) "wikilink") [Category:BlackBerry](https://ja.wikipedia.org/wiki/Category:BlackBerry "wikilink")

1.  <http://smartphone.nttdocomo.co.jp/corporation/index.html> ドコモスマートフォンサイトBES
2.  [- Unveiling a Comprehensive Mobile-Security Platform for the Enterprise of Things - 米BlackBerryサイト(英文)](http://blogs.blackberry.com/2016/12/unveiling-a-comprehensive-mobile-security-platform-for-the-enterprise-of-things/)
3.  <http://smartphone.nttdocomo.co.jp/product/index.html> NTTドコモスマートフォンサイトBlackBerry端末
4.  [BlackBerry、過去の訴訟相手を買収へ　法人モバイル管理を強化 -＜2015年9月7日＞日経ITPro](http://itpro.nikkeibp.co.jp/atcl/news/15/090702895/)
5.  [Good Work - NTTドコモ法人向けサイト](http://www.docomo.biz/html/service/good_for_enterprise/)
6.  [「ブラックベリーサービス」の新規受付停止及びサービス終了について](https://www.nttdocomo.co.jp/info/notice/page/150528_00_m.html)
7.  [BlackBerry、日本で法人向けソフトウェア事業を再始動 -＜2016年7月27日＞ビジネスネットワーク.jp](http://businessnetwork.jp/Detail/tabid/65/artid/4738/Default.aspx)
8.  <http://www.dataviz.com/products/documentstogo/blackberry/> Documents To Go For BlackBerry
9.  <http://ap.blackberry.com/jpn/software/business/server/express/> BlackBerry Enterprise Server Express
10. [ブラックベリーサーバチャート表](http://ap.blackberry.com/jpn/software/business/server/express/RIM816_ComparisonChart_2_JP.pdf)