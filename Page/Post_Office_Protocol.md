> この記事は[Post Office Protocol](https://ja.wikipedia.org/wiki/Post_Office_Protocol)から翻訳されています。


**Post Office Protocol**（ポスト オフィス プロトコル、**POP**）は、電子メールで使われる[プロトコル](../Page/プロトコル.md "wikilink")（通信規約）のひとつ。ユーザが[メールサーバ](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")から自分のメールを取り出す時に使用する、メール受信用プロトコル。現在は、改良されたPOP3 (POP Version 3) が使用されている。

## 概要

電子メールは、いつ・誰から送られてくるか分からない。しかし、ユーザが自分のコンピュータを常にインターネットに接続してメールを受信できるように待機させておく必要はない。これは、[インターネットサービスプロバイダ](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink") (ISP) や企業ネットワーク内にメールを配達・受信するためのメールサーバが設置されており、メールサーバが常にメールを受信できるように待機しているからである。メールサーバにメールが届いた後に、ユーザがメールサーバからメールを取り出して、自分のコンピュータに取り込めばよい。この時に使われるプロトコルがPOPである。この作業は、郵便局（メールサーバ）に届けられた手紙をユーザーが郵便局へ取りに行く作業に似ている。メールサーバにメールが届いているかどうかもPOPで確かめることができる。

POPのユーザ認証機能をメール送信時の送信者認証に使用することがあり、これを[POP before SMTPと言う](https://ja.wikipedia.org/wiki/POP_before_SMTP "wikilink")。

通常使用するTCPポート番号は、POP2では109番、POP3では110番を使用する。

## ユーザの認証方法

認証方法として、[平文](https://ja.wikipedia.org/wiki/平文 "wikilink")のUSER/PASS [認証](../Page/認証.md "wikilink")が広く用いられているが、サーバ/クライアント双方が対応していれば、オプションコマンドである APOP（RFC 1460から追加）や拡張機能である [SASL](https://ja.wikipedia.org/wiki/SASL "wikilink")メカニズムを利用したAUTHコマンドなどを用いて[認証](../Page/認証.md "wikilink")を暗号化し、パスワード漏洩を防止することができる。

ただし、それらを用いても[認証](../Page/認証.md "wikilink")の部分のみを暗号化したものであって、その他のメールのヘッダや本文などの内容は[平文](https://ja.wikipedia.org/wiki/平文 "wikilink")のままである。このため、[TLSを用いてすべてを暗号化することが推奨されている](https://ja.wikipedia.org/wiki/Transport_Layer_Security "wikilink")。

## IPAの勧告

APOPで暗号化された中身の解析については[電気通信大学](https://ja.wikipedia.org/wiki/電気通信大学 "wikilink")([情報理工学部](https://ja.wikipedia.org/wiki/情報理工学部 "wikilink")・大学院情報理工学研究科)の太田和夫[教授](https://ja.wikipedia.org/wiki/教授 "wikilink")の研究グループが解析を成功させた\[1\]\[2\]\[3\]。この脆弱性は[MD5](https://ja.wikipedia.org/wiki/MD5 "wikilink")[ハッシュ](https://ja.wikipedia.org/wiki/ハッシュ "wikilink")方式をAPOPにおいて不適切に用いていることによるプロトコル（通信手順）上の問題であり、現時点で根本的な対策方法は存在しない。そのため、内容を漏洩させないためには[STARTTLS](https://ja.wikipedia.org/wiki/STARTTLS "wikilink")や[POP over SSL](https://ja.wikipedia.org/wiki/POP_over_SSL "wikilink")（ポート番号は995番）などを利用して[SSLで通信し](https://ja.wikipedia.org/wiki/Secure_Sockets_Layer "wikilink")、ネットワーク経路を暗号化する必要がある。

なお、MD5そのものについても、[アメリカ合衆国政府](https://ja.wikipedia.org/wiki/アメリカ合衆国政府 "wikilink")（[NIST（アメリカ国立標準技術研究所）](https://ja.wikipedia.org/wiki/アメリカ国立標準技術研究所 "wikilink")）及び日本の[CRYPTREC](https://ja.wikipedia.org/wiki/CRYPTREC "wikilink")（暗号技術評価プロジェクト）では推奨から外されており、その点でもAPOPの利用は勧められない。

## 暗号化

[Transport Layer Security](https://ja.wikipedia.org/wiki/Transport_Layer_Security "wikilink") (TLS)で暗号化して通信する方式として、POP3S (Implicit TLS)と[STARTTLS](https://ja.wikipedia.org/wiki/STARTTLS "wikilink")が規定されている。POP3Sではポート995番を用いる。

## RFC

  - RFC 3206 - SYS and AUTH POP Response Codes
  - RFC 2595 - Using TLS with IMAP, POP3 and ACAP
  - RFC 2449 - POP3 Extension Mechanism
  - RFC 2384 - POP URL Scheme
  - RFC 2195 - IMAP/POP AUTHorize Extension for Simple Challenge/Response
  - RFC 1957 - Some Observations on Implementations of POP3
  - RFC 1939 - **Post Office Protocol - Version 3**
  - RFC 1734 - POP3 AUTHentication command
  - RFC 1725 - Post Office Protocol - Version 3 *（RFC 1939で改訂）*
  - RFC 1460 - Post Office Protocol - Version 3 *（RFC 1725で改訂）*
  - RFC 1225 - Post Office Protocol - Version 3 *（RFC 1460で改訂）*
  - RFC 1081 - Post Office Protocol - Version 3 *（RFC 1225で改訂）*
  - RFC 937 - POST OFFICE PROTOCOL - VERSION 2
  - RFC 918 - POST OFFICE PROTOCOL *（RFC 937で改訂）*

## 脚注

## 関連項目

  - [SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")
  - [IMAP](https://ja.wikipedia.org/wiki/Internet_Message_Access_Protocol "wikilink")
  - [S/MIME & POP3](http://www.pop3component.net/)

[Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:電子メールのプロトコル](https://ja.wikipedia.org/wiki/Category:電子メールのプロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  [IPA:APOP方式におけるセキュリティ上の弱点（脆弱性）の注意喚起について](http://www.ipa.go.jp/security/vuln/200704_APOP.html)
2.  [情報処理推進機構：セキュリティセンター：脆弱性関連情報取扱い：脆弱性関連情報の調査結果 JVN\#19445002 APOP におけるパスワード漏えいの脆弱性](http://www.ipa.go.jp/security/vuln/documents/2007/JVN_19445002.html)
3.