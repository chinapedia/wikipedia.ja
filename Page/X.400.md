> この記事は[X.400](https://ja.wikipedia.org/wiki/X.400)から翻訳されています。


[ITU-T](../Page/ITU-T.md "wikilink") **X.400**シリーズ勧告 **Message Handling System**（**MHS**、**メッセージ通信処理システム**）は、[電子メール](../Page/電子メール.md "wikilink")についての標準を定めたものである。[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")の電子メールの標準として採用されることはなかったが、組織内で使用されたり、独自の商用電子メール製品で採用されたこともある。[OSIでは](https://ja.wikipedia.org/wiki/開放型システム間相互接続 "wikilink") **ISO/IEC 10021 Message-Oriented Text Interchange Systems**（**MOTIS**）という名前で標準化されている。MHSとMOTISは一部で細かい差はあるものの、技術的にほぼ同等である。

## 歴史

最初の X.400 勧告が公表されたのは 1984年（*Red Book*）、大幅に改版されたのが 1988年（*Blue Book*）である。1992年（*White Book*）にも改訂と新機能の追加が行われた。X.400 は OSI トランスポートサービス上で動作するよう設計されたが、RFC 1006 により[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")上で動作できるようになり、それが X.400 の一般的な利用方法となった。

[ISOとの共同で開発された](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink") X.400 シリーズ勧告は、電子メッセージの交換については[OSI標準プロトコル群を指定していた](https://ja.wikipedia.org/wiki/開放型システム間相互接続 "wikilink")。それに付随する F.400 シリーズ勧告では、MHS 上に構築される Message Handling Services を定義していると同時に、MHS と公衆サービス間のアクセスを定義している。1990年代末、[ITU-T](../Page/ITU-T.md "wikilink")は F.400 と X.400 を統合し、F.400/X.400 (06/1999) *Message handling system and service overview* という勧告を発表した。

X.400 シリーズ勧告は MHS の技術的観点を定義している。X.402 勧告（ISO/IEC 10021-2）は MHS のシステム全体のアーキテクチャを定義している。X.411（ISO/IEC 10021-4）はメッセージ転送サービス (MTS) とその機能コンポーネントである[メッセージ転送エージェント (MTA)を定義している](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink")。X.413（ISO/IEC 10021-5）はメッセージストアについて定義している。全ての ITU-T 勧告には、システムの実体や手続きを説明するための専門用語が定義されている。例えば、個人間でのメッセージ（電子メール）交換は、Interpersonal Messaging (IPM) とされている。一方、各取引業者のコンピュータ間で交換される電子構造化ビジネス文書（例えば、見積書、注文書など）は、[EDIプロトコルに分類されている](https://ja.wikipedia.org/wiki/電子データ交換 "wikilink")。

多くの[ISO標準はネットワークのアプリケーション層を扱っており](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")、X.400 は [SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink") と対抗することになった。X.400 は北米以外では特にEDIサービスの用途で盛んに実装された。北米でも軍関係や航空関係では X.400 が使われている。これは、X.400 で当初からセキュリティが考慮されていたためであり、SMTP が同等の機能（[S/MIME](https://ja.wikipedia.org/wiki/S/MIME "wikilink")、[PGP](https://ja.wikipedia.org/wiki/PGP "wikilink")、SMTP-TLS など）を実装するよりも早かったのである。同様の理由で、アプリケーション間のEDIメッセージ交換にも使われることがある。

メッセージ通信処理は、メッセージ転送とメッセージ記憶装置という2つの部分からなる分散情報処理である。ITU-T 勧告では、様々な通信タスクに関するプロトコルを定義している。例えば、P1 プロトコルは[MTA間の通信のみに使われる](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink")。P3 プロトコルは[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")とMTA間、P7 プロトコルは電子メールクライアントとメッセージ記憶装置間のプロトコルである。

1994年版では、P7 プロトコルの強化としてメッセージ記憶装置でのフォルダをサポートし、自動的なメッセージのフォルダ分類やリプライの対応付け、配送レポート、受信通知といった機能が提供された。

X.400 のメッセージコンテンツ標準は電子メールクライアント間の通信のために定義された。これらは、P1/P3/P7 をメッセージコンテンツ転送を提供する基盤として、その上の概念的プロトコルとしてモデル化されている。IPM（Interpersonal Messaging）のためのメッセージコンテンツ標準は X.420（ISO/IEC 10021-7）で定義されており、RedBook では P2 と呼ばれている。BlueBook での IPM の拡張版として content-type 22（P2 version 2）があり、非公式だが一般に P22 と呼ばれている。EDI のためのメッセージコンテンツ標準は F.435（ISO/IEC 10021-8）と X.435（ISO/IEC 10021-9）で定義されており、非公式に P35 と呼ばれている。音声メッセージコンテンツは F.440 と X.440 に定義されている。

X.400 の重要な機能として、構造化されたアドレス指定、[ASN.1によるマルチメディアコンテンツ](../Page/Abstract_Syntax_Notation_One.md "wikilink")（[MIME](https://ja.wikipedia.org/wiki/Multipurpose_Internet_Mail_Extensions "wikilink") に先行していて、より効率的だった）、統合セキュリティ機能がある。[ITUは](../Page/国際電気通信連合.md "wikilink")、X.400 のドメイン間リレーは各国の電話会社（公社）が行うものと考えていたため、X.400 と他の電話会社のサービス（[テレックス](https://ja.wikipedia.org/wiki/テレックス "wikilink")、[ファクシミリ](https://ja.wikipedia.org/wiki/ファクシミリ "wikilink")、物理的な郵便）との自動的な相互乗り入れが可能となるようなアドレスフィールドが導入された。ISO は後にオープンなルーティング標準として X.412（ISO/IEC 10021-10）と X.404（ISO/IEC 10021-11）を追加したが、X.400 の当初の想定の誤りと電話会社がそれを元に課金することもあって、X.400 が広く採用されるのを妨げる一因となった。

X.400 は、軍用（MMHS）と航空用（AMHS）に拡張されたバージョンが存在する。

## アドレス指定

X.400 のアドレスは次のようないくつかの部分から構成される。

  - C (Country name) - 国名
  - 主官庁管理領域（）- 通常、公衆メールサービス提供業者を指す
  - 私設管理領域（）- 私的管理ドメイン
  - O (Organization name) - 組織名
  - OU (Organizational Unit Names) - 部門名
  - G (Given name) - 名
  - I (Initials) - イニシャル
  - S (Surname) - 姓

標準自体には当初、電子メールのアドレスをどう書くか（例えば、名刺にどう印刷すべきか）が示されていなかった。RFC 1685 では 1993年の ITU-T 勧告ドラフト F.401 に基づいて符号化仕様を示した。それは、"G=Harald;S=Alvestrand;O=Uninett;P=Uninett;A=;C=no" といったような形式で、このようなアドレスのわかりにくさが X.400 が広まらなかった一因であるとも言われている。\[1\]

## 関連項目

  - [X.500](../Page/X.500.md "wikilink")
  - [標準化団体](https://ja.wikipedia.org/wiki/標準化団体 "wikilink")
  - [国際電気通信連合](../Page/国際電気通信連合.md "wikilink") (ITU)
  - [国際電気標準会議](https://ja.wikipedia.org/wiki/国際電気標準会議 "wikilink") (IEC)
  - [国際標準化機構](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink") (ISO)
  - [電子データ交換](https://ja.wikipedia.org/wiki/電子データ交換 "wikilink")

## 参考文献

  -
<!-- end list -->

  - 規格・標準

<!-- end list -->

  - [RFC 1615 - Migrating from X.400(84) to X.400(88)](http://www.faqs.org/rfcs/rfc1615.html)

  - [RFC 1649 - Operational Requirements for X.400 Management Domains in the GO-MHS Community](http://www.faqs.org/rfcs/rfc1649.html)

  -
## 脚注

## 外部リンク

  - [International Telecommunication Union - Telecommunication Std. Sector](http://www.itu.int/ITU-T/dbase/index.html) - ITU-T勧告のリスト
  - [International Electrotechnical Commission](http://www.iec.ch/helpline/sitetree/about/) - IECについて
  - [Sending Messages - Routing and Transport](http://www.windowsitlibrary.com/Content/519/06/1.html) - "The Battle Between SMTP and X.400" の節を参照
  - [Harald T. Alvestrand's X.400 FAQ](http://www.alvestrand.no/x400/index.html) - X.400 シリーズ標準に関する各種資料のリスト（最終更新は1995年）
  - [X400.org](http://www.x400.org/US/X400_Default.htm)

### X.400 標準

X.400 標準はITU-Tから無料で入手可能である。

  - [ITU-T Rec. F.400/X.400 | ISO/IEC 10021-1 Message handling system and service overview](http://www.itu.int/rec/T-REC-F.400-199906-I/en)
  - [ITU-T Rec. X.402 | ISO/IEC 10021-2 Message Handling Systems (MHS): Overall architecture](http://www.itu.int/rec/T-REC-X.402-199906-I/en)
  - [ITU-T Rec. X.411 | ISO/IEC 10021-4 Message Handling Systems (MHS): Message Transfer System: Abstract Service Definition and Procedures](http://www.itu.int/rec/T-REC-X.411-199906-I/en)
  - [ITU-T Rec. X.413 | ISO/IEC 10021-5 Message Handling Systems (MHS): Message store - Abstract service definition](http://www.itu.int/rec/T-REC-X.413-199906-I/en)
  - [ITU-T Rec. X.419 | ISO/IEC 10021-6 Message Handling Systems (MHS): Protocol specifications](http://www.itu.int/rec/T-REC-X.419-199906-I/en)
  - [ITU-T Rec. X.420 | ISO/IEC 10021-7 Message Handling Systems (MHS): Interpersonal Messaging System](http://www.itu.int/rec/T-REC-X.420-199906-I/en)
  - [ITU-T Rec. X.435 | ISO/IEC 10021-9 Message Handling Systems (MHS): Electronic data interchange messaging system](http://www.itu.int/rec/T-REC-X.435-199906-I/en)
  - [ITU-T Rec. X.412 | ISO/IEC 10021-10 Message Handling Systems (MHS): MHS routing](http://www.itu.int/rec/T-REC-X.412-199906-I/en)
  - [ITU-T Rec. X.404 | ISO/IEC 10021-11 Message Handling Systems (MHS): MHS routing - Guide for messaging systems managers](http://www.itu.int/rec/T-REC-X.404-199906-I/enn)

[Category:ISO/IEC標準](https://ja.wikipedia.org/wiki/Category:ISO/IEC標準 "wikilink") [Category:ITU-T勧告](https://ja.wikipedia.org/wiki/Category:ITU-T勧告 "wikilink") [Category:電子メール](https://ja.wikipedia.org/wiki/Category:電子メール "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink")

1.  <http://www.alvestrand.no/x400/debate/addressing.html>