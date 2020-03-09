> この記事は[Internet Message Access Protocol](https://ja.wikipedia.org/wiki/Internet_Message_Access_Protocol)から翻訳されています。


**Internet Message Access Protocol**（インターネット メッセージ アクセス プロトコル、**IMAP**(アイマップ)） は、[メールサーバ](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")上の[電子メール](../Page/電子メール.md "wikilink")にアクセスし操作するための[プロトコル](../Page/プロトコル.md "wikilink")。クライアントとサーバが[TCPを用いて通信する場合](../Page/Transmission_Control_Protocol.md "wikilink")、通常サーバー側はIMAP4では[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")143番、IMAP over [SSL](https://ja.wikipedia.org/wiki/Transport_Layer_Security "wikilink")(IMAPS)では993番を利用する。

## 概要

[POP](../Page/Post_Office_Protocol.md "wikilink") はユーザが利用中のサーバからクライアントにメールをダウンロードし、ダウンロードがすんだメールはサーバから削除することを標準的な利用形態とするのに対し、IMAP はメールをメールサーバ上に保存したまま管理する（RFC 1733 参照）。この特性により、[Webメール](https://ja.wikipedia.org/wiki/Webメール "wikilink")や複数のコンピュータから同一[アカウント](https://ja.wikipedia.org/wiki/アカウント "wikilink")のメールを読む場合に、メールの未読状態等の属性やメールフォルダの構成等が一元的に管理できる利点がある。もともとはオリジナルであるIMAPが開発されたが、IMAP2、IMAP3、IMAP2bisなどが作られ、現在IMAPと呼ぶときにはIMAP4を指すことが通常である。プロトコルの仕様が複雑であったためあまり広く普及しなかったが、[Netscape](../Page/Netscapeシリーズ.md "wikilink") や [Internet Explorer](../Page/Internet_Explorer.md "wikilink") に標準で含まれているメールソフトが IMAP4 に対応し、また相互接続試験やプロトコルの様々な改訂・拡張により相互運用性が高まったため、利用者が広がった。

## POPとの比較

POPは以下の利点と欠点を持つ。

  - POPプロトコルは常時接続ではないネットワークアクセスにおいて有利である。
  - ユーザーはメールのローカルコピーを取得し、メールをオフラインで読むことができる。
  - メールフォルダは[MUAより管理されプロトコルには含まれていない](https://ja.wikipedia.org/wiki/電子メールクライアント "wikilink")。
  - 通常、メールはサーバから取得された直後に削除する。すなわちサーバは未読のメールだけ保持しておけばよいので、サーバ側の保存容量は少なくて済む。
  - 複数の端末からメールを取得すると、別の端末でダウンロードしたローカルコピーにアクセスできない。
  - メールをサーバに保存する手段がない。
  - メールを取得する際にメールの一部のみを取得する手段がオプションとなっている。

IMAPはPOPの利点を生かしつつ欠点を解消している。

  - IMAPプロトコルはオンライン・オフラインいずれでも利用できる。
  - オフライン操作はMUA側でトランザクションログとして保存し、サーバに接続した時点でコミットすることで反映できる。
  - 通常、メールはサーバに常時保存される。ローカルコピーを取得した時点でサーバから削除することもできる（ただし基本的にサーバ側の保存容量は増加する）。
  - 複数の端末からメール状態を一元管理することができる。複数の端末で同じメールを読むことができる。
  - メールフォルダはプロトコルの一部として標準化されており、メールソフトの種類に関係なくフォルダを管理できる。
  - メールの一部のみを取得できる。ヘッダのみの取得、マルチパートのテキスト部分のみの取得といった操作が可能。
  - メールをサーバに保存する手段がある。フォルダ全体のスナップショットを別のサーバに転送することもできる。
  - メッセージの検索をサーバ側で行わせることができ、クライアント側の負荷減少に寄与できる。
  - IMAP4より古いIMAPはリモート実行によるプロトコルの複雑さとセキュリティ上の懸念があった。IMAP4では改善された。
  - メールサーバはメールのオリジナルを管理しなければならない。大規模システムでは莫大な量のメール管理が必要となる。

## IMAPの採用例

### サーバ

  - [Courier-IMAP](https://ja.wikipedia.org/wiki/Courier-MTA "wikilink")
  - [UW IMAP](http://www.washington.edu/imap/)
  - [Cyrus IMAP server](https://ja.wikipedia.org/wiki/Cyrus_IMAP_server "wikilink")
  - [Dovecot](https://ja.wikipedia.org/wiki/Dovecot "wikilink")

### クライアント

  - [メール](https://ja.wikipedia.org/wiki/メール_\(アップル\) "wikilink") (アップル社)
  - [Becky\! Internet Mail](https://ja.wikipedia.org/wiki/Becky!_Internet_Mail "wikilink")
  - [Eudora](https://ja.wikipedia.org/wiki/Eudora "wikilink")
  - [Gaucho Internet Mailer](https://ja.wikipedia.org/wiki/Gaucho_Internet_Mailer "wikilink")
  - [Gnus](https://ja.wikipedia.org/wiki/Gnus "wikilink")
  - [Mew](https://ja.wikipedia.org/wiki/Mew "wikilink")
  - [Microsoft Entourage](https://ja.wikipedia.org/wiki/Microsoft_Entourage "wikilink")
  - [Microsoft Outlook Express](https://ja.wikipedia.org/wiki/Microsoft_Outlook_Express "wikilink")
  - [Microsoft Outlook](https://ja.wikipedia.org/wiki/Microsoft_Outlook "wikilink")
  - [Mozilla Thunderbird](https://ja.wikipedia.org/wiki/Mozilla_Thunderbird "wikilink")
  - [Mutt](https://ja.wikipedia.org/wiki/Mutt "wikilink")
  - [Opera](https://ja.wikipedia.org/wiki/Opera "wikilink") M2
  - [Shuriken Pro4](https://ja.wikipedia.org/wiki/Shuriken "wikilink")
  - [Sylpheed](https://ja.wikipedia.org/wiki/Sylpheed "wikilink")
  - [Winbiff](https://ja.wikipedia.org/wiki/Winbiff "wikilink")
  - [Wanderlust](https://ja.wikipedia.org/wiki/Wanderlust "wikilink")
  - [秀丸メール](https://ja.wikipedia.org/wiki/秀丸メール "wikilink")

### ウェブメールクライアント

  - [RoundCube](https://ja.wikipedia.org/wiki/RoundCube "wikilink")
  - [SquirrelMail](https://ja.wikipedia.org/wiki/SquirrelMail "wikilink")

### サービス

  - [MobileMe](https://ja.wikipedia.org/wiki/MobileMe "wikilink") - [アップル](https://ja.wikipedia.org/wiki/アップル_\(企業\) "wikilink")
  - [AIM Mail](https://ja.wikipedia.org/wiki/AIM_Mail "wikilink") - [AOL](https://ja.wikipedia.org/wiki/AOL "wikilink")
  - [Gmail](https://ja.wikipedia.org/wiki/Gmail "wikilink") - [Google](https://ja.wikipedia.org/wiki/Google "wikilink")
  - [Outlook.com](https://ja.wikipedia.org/wiki/Outlook.com "wikilink") - [マイクロソフト](../Page/マイクロソフト.md "wikilink")

## RFC

  - RFC 5464 - The IMAP METADATA Extension
  - RFC 5258 - Internet Message Access Protocol version 4 - LIST Command Extensions
  - RFC 5257 - Internet Message Access Protocol - ANNOTATE Extension
  - RFC 5256 - Internet Message Access Protocol - SORT and THREAD Extensions
  - RFC 5255 - Internet Message Access Protocol Internationalization
  - RFC 5182 - IMAP Extension for Referencing the Last SEARCH Result
  - RFC 5162 - IMAP4 Extensions for Quick Mailbox Resynchronization
  - RFC 5161 - The IMAP ENABLE Extension
  - RFC 5092 - IMAP URL Scheme
  - RFC 5032 - WITHIN Search Extension to the IMAP Protocol
  - RFC 4978 - The IMAP COMPRESS Extension
  - RFC 4959 - IMAP Extension for [Simple Authentication and Security Layer](https://ja.wikipedia.org/wiki/Simple_Authentication_and_Security_Layer "wikilink") (SASL) Initial Client Response
  - RFC 4731 - IMAP4 Extension to SEARCH Command for Controlling What Kind of Information Is Returned
  - RFC 4551 - IMAP Extension for Conditional STORE Operation or Quick Flag Changes Resynchronization
  - RFC 4550 - Internet Email to Support Diverse Service Environments (Lemonade) Profile
  - RFC 4549 - Synchronization Operations for Disconnected IMAP4 Clients
  - RFC 4469 - Internet Message Access Protocol (IMAP) CATENATE Extension *([日本語訳](http://www.kasai.fm/wiki/imap_cat))*
  - RFC 4468 - Message Submission BURL Extension
  - RFC 4467 - Internet Message Access Protocol (IMAP) - URLAUTH Extension
  - RFC 4466 - Collected Extensions to IMAP4 ABNF
  - RFC 4416 - Goals for Internet Messaging to Support Diverse Service Environments
  - RFC 4315 - Internet Message Access Protocol (IMAP) - UIDPLUS extension
  - RFC 4314 - IMAP4 Access Control List (ACL) Extension
  - RFC 3691 - IMAP UNSELECT command
  - RFC 3516 - IMAP4 Binary Content Extension
  - RFC 3503 - Message Disposition Notification (MDN) profile for IMAP
  - RFC 3502 - IMAP MULTIAPPEND Extension
  - RFC 3501 - **INTERNET MESSAGE ACCESS PROTOCOL - VERSION 4rev1**
  - RFC 3348 - IMAP4 Child Mailbox Extension
  - RFC 2971 - IMAP4 ID extension
  - RFC 2683 - IMAP Implementation Recommendations
  - RFC 2595 - Using TLS with IMAP4, POP3 and ACAP
  - RFC 2359 - IMAP4 UIDPLUS extension *(RFC 4315によって改訂)*

<!-- end list -->

  - RFC 2342 - IMAP4 Namespace
  - RFC 2221 - IMAP4 Login Referrals
  - RFC 2195 - IMAP/POP AUTHorize Extension for Simple Challenge/Response
  - RFC 2193 - IMAP4 Mailbox Referrals
  - RFC 2192 - IMAP URL Scheme *(RFC 5092によって改訂)*
  - RFC 2180 - IMAP4 Multi-Accessed Mailbox Practice
  - RFC 2177 - IMAP4 IDLE command
  - RFC 2095 - IMAP/POP AUTHorize Extension for Simple Challenge/Response *(RFC 2195によって改訂)*
  - RFC 2088 - IMAP4 non-synchronizing literals
  - RFC 2087 - IMAP4 QUOTA extension
  - RFC 2086 - IMAP4 ACL extension *(RFC 4314によって改訂)*

<!-- end list -->

  - RFC 2061 - IMAP4 COMPATIBILITY WITH IMAP2BIS
  - RFC 2060 - INTERNET MESSAGE ACCESS PROTOCOL - VERSION 4rev1 *(RFC 3501によって改訂)*
  - RFC 1733 - DISTRIBUTED ELECTRONIC MAIL MODELS IN IMAP4
  - RFC 1732 - IMAP4 COMPATIBILITY WITH IMAP2 AND IMAP2BIS
  - RFC 1731 - IMAP4 Authentication Mechanisms
  - RFC 1730 - INTERNET MESSAGE ACCESS PROTOCOL - VERSION 4 *(RFC 2060によって改訂)*
  - RFC 1203 - INTERACTIVE MAIL ACCESS PROTOCOL - VERSION 3
  - RFC 1176 - INTERACTIVE MAIL ACCESS PROTOCOL - VERSION 2
  - RFC 1064 - INTERACTIVE MAIL ACCESS PROTOCOL - VERSION 2 *(RFC 1176, RFC 1203によって改訂)*

## 関連項目

  - [ACAP](https://ja.wikipedia.org/wiki/Application_Configuration_Access_Protocol "wikilink")
  - [POP3](https://ja.wikipedia.org/wiki/POP3 "wikilink")
  - [SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")
  - [プッシュ型電子メール](https://ja.wikipedia.org/wiki/プッシュ型電子メール "wikilink")
  - [修正UTF-7](https://ja.wikipedia.org/wiki/UTF-7#修正UTF-7 "wikilink")

[Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:電子メールのプロトコル](https://ja.wikipedia.org/wiki/Category:電子メールのプロトコル "wikilink")