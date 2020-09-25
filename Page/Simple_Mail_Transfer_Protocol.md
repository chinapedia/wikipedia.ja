> この記事は[Simple Mail Transfer Protocol](https://ja.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol)から翻訳されています。


**Simple Mail Transfer Protocol**（シンプル メール トランスファー プロトコル、**SMTP**）または**簡易メール転送プロトコル**は、[インターネット](../Page/インターネット.md "wikilink")で[電子メール](../Page/電子メール.md "wikilink")を転送する[プロトコル](../Page/プロトコル.md "wikilink")である。通常 [ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink") 25 を利用する。 転送先のサーバを特定するために、[DNS](../Page/Domain_Name_System.md "wikilink") の [MXレコード](https://ja.wikipedia.org/wiki/MXレコード "wikilink")が使われる。RFC 5321 で[標準化](../Page/標準化.md "wikilink")されている。

## 概要

SMTPは[IETFにおいて](../Page/Internet_Engineering_Task_Force.md "wikilink")[標準化](../Page/標準化.md "wikilink")されたメール転送のためのプロトコルである。[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")9月にメール転送プロトコル（Mail Transfer Protocol）という名称のプロトコルが RFC 772 において提案され、2回の改訂を経て[1982年](../Page/1982年.md "wikilink")8月に簡易メール転送プロトコル（SMTP）という名称で RFC 821/ STD0010 \[1\] として標準になった。

その後 [2001年](../Page/2001年.md "wikilink")4月に SMTPは他のRFCの内容もあわせて改訂され、RFC 2821\[2\] として提案標準（Proposed Standard）になった。RFC 821 から約20年を経て改訂版が発行されたのは、おもにインターネットの普及にともなって様々なメール拡張機能が実装され、それらをささえる部分を整理する必要があったからである。[サーバ](../Page/サーバ.md "wikilink")外からの攻撃や、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")のアドレスにも対応できるよう、また[SPF](../Page/Sender_Policy_Framework.md "wikilink")（[Sender Policy Framework](../Page/Sender_Policy_Framework.md "wikilink")、RFC 4408）、[DKIM](../Page/ドメインキー・アイデンティファイド・メール.md "wikilink")（[DomainKeys Identified Mail](../Page/ドメインキー・アイデンティファイド・メール.md "wikilink")、RFC 4871）などにも対応すべく [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")10月に再度改訂（RFC 5321）\[3\]された。

SMTP は[メールサーバ](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")間の転送だけでなく、[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")からメールサーバにメールを送信するときにも使われる。この2つを元々は区別していなかったが[スパムなどを防ぐために現在では配送](../Page/スパム_\(メール\).md "wikilink")(transfer)と提出(submission)として分けて考え、メール配送の通信ではポート番号25をそのまま使うが、メール提出ではポート番号587で認証を必須とし暗号化する場合が多い。ポート番号25に接続しようとしても、ほとんどの[インターネットサービスプロバイダ](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")が[ブロックしている](../Page/Outbound_Port_25_Blocking.md "wikilink")。またポート番号587や[TLSで暗号化した場合のポート番号](../Page/Transport_Layer_Security.md "wikilink")465をSubmissionポートという\[4\]。

SMTPは本来[テキスト](../Page/テキスト.md "wikilink")ベースのプロトコルであり、全ての要求/応答メッセージやメールデータが7[ビット](../Page/ビット.md "wikilink")[ASCII](../Page/ASCII.md "wikilink")でなければならないという制限があったが、英語以外の言語やバイナリファイルを扱う需要があった。そのため、電子メールに[MIMEという規格がつくられ](../Page/Multipurpose_Internet_Mail_Extensions.md "wikilink")、SMTP自体にも8ビットで伝送する拡張が標準化された。

## プロトコル

SMTPにおいてはサーバとクライアントの役割が明確に分離されている。RFC 5321によれば、それらは下図のように記述される。

[SMTPにおけるサーバとクライアントの役割.png](https://ja.wikipedia.org/wiki/File:SMTPにおけるサーバとクライアントの役割.png "fig:SMTPにおけるサーバとクライアントの役割.png")

SMTPではクライアントがサーバに接続するとただちにサーバ - クライアント間に "SMTP [セッション](../Page/セッション.md "wikilink")" が確立され、その後、両者の間で[FTPのような対話型で](../Page/File_Transfer_Protocol.md "wikilink")[コマンド](https://ja.wikipedia.org/wiki/コマンド "wikilink")やそれに対する応答やメールがやりとりされる。セッションの終了のためにはQUITコマンドが使用されるが、この点においてもFTPとの同様である。

コマンドは`EHLO`, `HELO`, `MAIL`, `RCPT`, `DATA`, `RSET`, `NOOP`, `QUIT`, `VRFY`などで、空白で区切られた引数がひとつまたは複数続く場合がある。標準のコマンドでは全て4文字ASCIIである。応答は3桁の応答コードで同様に引数が続く場合がある。また、人間が読むための応答コードに対応する文字列が続く場合があるが、SMTPクライアントは応答コードのみによって動作を決定しなければならない。メールデータは<CRLF>で、1行が<CRLF>を含め1000バイトを超えないように区切られる。また、コマンドと引数はメールアドレスの@より前のローカルパートを除き大文字小文字は区別されない。

応答が複数行になる場合は以下のように最終行以外は3桁の応答コードの直後にハイフンをつけ、テキストを続ける。最終行は3桁の応答コードの直後にスペースをつけ、テキストを続ける。

`250-First line`
`250-Second line`
`250-234 Text beginning with numbers`
`250 The last line`

各行の応答コードは同じでなければならない。

SMTPにおいてはトランスポート・プロトコルとして通常 [TCP](../Page/Transmission_Control_Protocol.md "wikilink") が使用されるが、それに限定されることはない。

### コマンド

**EHLO**(拡張HELLO)または**HELO**(HELLO)コマンドはSMTPサーバーにSMTPクライアントのドメイン名を知らせる。クライアントはEHLOコマンドを使うべきだが、古いサーバーはEHLOコマンドに対応せずエラーを返す。その場合はHELOコマンドを使用しても良い。完全修飾ドメイン名を引数に取る。

**MAIL**コマンドは電子メールをSMTPサーバーへ送る一連のメールトランザクションを開始する。引数に'FROM:\<*エラーを報告するのに使用される送信元メールアドレス*\>'を取る。

**RCPT**(RECIPIENT)コマンドは電子メールの宛先を指定する。宛先が複数の場合は複数回コマンドを実行する。引数に'TO:\<*宛先メールアドレス*\>'を取る。

**DATA**コマンドはメールデータをSMTPサーバに渡す。引数は許されず、DATAコマンドの直後に改行し、メールデータを何行か続ける。'.'のみの行が現れたらメールデータの終了を示し、メールトランザクションも終了する。もとのデータにピリオドのみの行があっても正しく動作するように行の先頭がピリオドであれば追加で行頭にピリオドを付加し、SMTPサーバーは受け取ったら取り除く。また、メールトランザクションはMAIL、RCPT、DATAの順で実行されなければならない。

**QUIT**コマンドは接続を終了する。クライアントがQUITコマンドを送信したらサーバーは応答コード`221`を返し接続を閉じる。引数は許されない。

**RSET**(RESET)コマンドは現在のメールトランザクションを中止する。引数は許されない。

**NOOP**(NO OPERATION)コマンドは何もしない。SMTPサーバーは必ず`250 OK`を返す。引数があっても無視される。

**HELP**コマンドはヘルプを表示する。引数に対応するかはソフトウェアによる。

その他、**VRFY**、**EXPN**コマンドがあるが、スパマーに利用されるため現在では殆どの場合利用不可とし`252`を返すか、認証されたユーザーのみ利用できるようにしている。VRFY, EXPN, HELP, NOOP, RSET, QUITコマンドはいつ実行されても良い。HELPとEXPNコマンドへの対応は任意であり実装されていないこともある。

### 応答コード

200番台は成功を表す。

300番台はコマンドは受け入れられたが追加の情報を待っていることを表す。DATAコマンドへの応答に354が使われる。

400番台は一時的エラーを表す。

500番台は永続的エラーを表す。

  - 211 System status, or system help reply (HELPコマンドの応答)
  - 214 Help message (HELPコマンドの応答)
  - 220 <domain> Service ready (接続後の応答メッセージ)
  - 221 <domain> Service closing transmission channel (QUITコマンドの応答)
  - 250 Requested mail action okay, completed (EHLO, HELO, MAIL, RCPT, DATA, RSET, VRFY, EXPN, NOOPコマンドの応答)
  - 251 User not local; will forward to <forward-path> (RCPT, VRFYコマンドの応答)
  - 252 Cannot VRFY user, but will accept message and attempt delivery (VRFY, EXPNコマンドの応答)
  - 354 Start mail input; end with <CRLF>.<CRLF> (DATAコマンドの応答)
  - 421 <domain> Service not available, closing transmission channel (全てのコマンドの応答)
  - 450 Requested mail action not taken: mailbox unavailable (RCPT, DATAコマンドの応答)
  - 451 Requested action aborted: local error in processing (MAIL, RCPT, DATAコマンドの応答)
  - 452 Requested action not taken: insufficient system storage (MAIL, RCPT, DATAコマンドの応答)
  - 455 Server unable to accommodate parameters (MAIL, RCPTコマンドの応答)
  - 500 Syntax error, command unrecognized (全てのコマンドの応答)
  - 501 Syntax error in parameters or arguments (全てのコマンドの応答)
  - 502 Command not implemented (EHLO, VRFY, EXPN, HELPコマンドの応答)
  - 503 Bad sequence of commands (MAIL, RCPT, DATAコマンドの応答)
  - 504 Command parameter not implemented (EHLO, HELO, VRFY, EXPN, HELPコマンドの応答)
  - 550 Requested action not taken: mailbox unavailable (EHLO, HELO, MAIL, RCPT, DATA, VRFY, EXPNコマンドの応答)

### 例

bob@example.com から alice@foo.com へメールを送る場合。

`# クライアントがサーバーへの接続を開く`
` `` # 挨拶応答。サーバーがfoo.comであることを示す。`
` # クライアントがexample.comであることを示す。`
` `
` # 送信元`
` `
` # 宛先`
` `

` `
` # メールデータの開始`








` # メールデータの終了`
` `

` `
`# サーバーが接続を閉じる`

### トレース情報

SMTPサーバーはDATAコマンドでメールデータを渡され、メールトランザクションが終了したら必ず先頭にReceivedヘッダフィールドを追加しなければならない。すでにReceived行があっても、書き換えたり削除したり順番を替えたりしてはならない。Receivedヘッダフィールドは

`Received:`
`FROM `<ドメイン名>` (`<IPアドレス>`)`
`BY `<ドメイン名>` (`<IPアドレス>`)`
`VIA <トランスポートプロトコル(TCPなど)>`
`WITH ESMTP(またはSMTP)`
`ID <RFC 5322のメッセージID>`
`FOR `<メールアドレス>
`<日時(RFC 5322形式)>`

の情報で構成される。ここでは改行しているが実際は改行ではなくスペースで区切られる。FROM節はEHLOコマンドで示された送信元ドメイン名とTCP接続から判明する送信元のIPアドレスとを両方含むべきである。VIA, WITH, ID, FOR節は任意である。

また、SMTPサーバーはメールの最終配送を行う場合、先頭にReturn-pathヘッダフィールドを追加しなければならない。Return-pathヘッダフィールドはMAILコマンドの<送信元メールアドレス>を挿入する。SMTP環境から出ていく時、SMTPの送信元メールアドレス情報が失われないようにするためである。この、エラーを報告するのに使用される送信元メールアドレスは実際の送信者のメールアドレスと異なることも可能である。

### メーリングリストとエイリアス

RFCではSMTP実装はメーリングリストとエイリアスをサポートすべきとされている。エイリアスとはメールアドレスの別名で本当のメールアドレスに置換してから処理される。メーリングリストとは複数のメールアドレスを指す擬似的なメールアドレスで、設定されている複数のメールアドレスに展開されて届けられる。

## 拡張

SMTP拡張としては以下のようなものがある。

### 8BITMIME拡張

8ビットで配送を行うことを可能にする拡張。行は<CRLF>で1000オクテットを超えないように区切られ、ドットのみの行でDATAの終わりを示す点は変わらないため、バイナリの配送を可能にするものではなく、8ビット文字コードを意図したものである。

### CHUNKING拡張とBINARYMIME拡張

CHUNKING拡張はDATAコマンドの代わりにBDATコマンドを使う。引数にオクテットサイズを取り、その後送られたデータをその長さだけ受け入れる。そのためドットのみの行で終わりを示す必要はない。また、複数回のBDATコマンドに分けることも可能である。その時のために、BDATコマンドの2つ目の引数に「LAST」を指定したら今回でデータの送信が終了することを示す。

BINARYMIME拡張はバイナリの配送を可能にする拡張。CHUNKING拡張と合わせて使用したときにのみ使うことが出来る。

### SIZE拡張

巨大なメールデータをサーバーに送っている時、SMTPサーバー側の制限を超えてから失敗を応答されるのは回線・時間・リソースの無駄であるため、実際にデータを送る前にクライアント側がサーバーのサイズ制限を知ることが出来るようにする拡張。

### PIPELINING拡張

宛先が複数あるときなどに毎回応答を待ってから次のコマンドを送信するのは時間がかかるため、連続してコマンドを送信するための拡張。

## ユーザー認証

### SMTP-AUTH

前述のSMTP標準にはユーザー[認証](../Page/認証.md "wikilink")機構が含まれていないが、インターネットの普及に伴ってその必要に迫られたため [SASL](https://ja.wikipedia.org/wiki/Simple_Authentication_and_Security_Layer "wikilink") メカニズムを利用した認証機構が RFC 2554 - SMTP Service Extension for Authentication（SMTP-AUTH）として標準化された。この標準の最新文書は RFC 4954 である。

### POP before SMTP

SMTP-AUTH 標準化以前に普及したユーザー制限方法。メール送信する前にメール受信([POP3](../Page/Post_Office_Protocol.md "wikilink") の [ログイン](https://ja.wikipedia.org/wiki/ログイン "wikilink"))を要求するため、こう呼ばれる。RFC 2476 - Message Submission において、クライアントを制限する方法の一つに挙げられたもの。

## 暗号化

SMTPの暗号化にはFTPなどの他のテキストベースプロトコルと同様に途中から暗号化を開始する[STARTTLS](https://ja.wikipedia.org/wiki/STARTTLS "wikilink")と最初から暗号化する[SMTPS](https://ja.wikipedia.org/wiki/SMTPS "wikilink")の2種類がある。SMTPSの場合はポート番号を同じには出来ないため、465を使う。

## 関連するRFC

  - RFC 821 - 廃止→ RFC 5321
  - RFC 822 - 廃止→ RFC 5322
  - RFC 974 - 廃止→ RFC 5321
  - RFC 1123 - Requirements for Internet Hosts—Application and Support (STD 3)
  - RFC 1652 - 廃止→ RFC 6152
  - RFC 1653 - 廃止→ RFC 1870
  - RFC 1830 - 廃止→ RFC 3030
  - RFC 1869 - 廃止→ RFC 5321
  - RFC 1870 - SIZE拡張について
  - RFC 1891 - 廃止→ RFC 3461
  - RFC 1893 - 廃止→ RFC 3463
  - RFC 1894 - 廃止→ RFC 3464
  - RFC 2476 - 廃止→ RFC 6409
  - RFC 2487 - 廃止→ RFC 3207
  - RFC 2505 - Anti-Spam Recommendations for SMTP MTAs (BCP 30)
  - RFC 2554 - 廃止→ RFC 4954
  - RFC 2821 - 廃止→ RFC 5321
  - RFC 2822 - 廃止→ RFC 5322
  - RFC 2920 - PIPELINING拡張について
  - RFC 3030 - CHUNKING拡張とBINARYMIME拡張について
  - RFC 3207 - SMTP Service Extension for Secure SMTP over Transport Layer Security
  - RFC 3461 - SMTP Service Extension for Delivery Status Notifications (updated by RFC 3798)
  - RFC 3462 - 廃止→ RFC 6522
  - RFC 3463 - Enhanced Status Codes for SMTP (updated by RFC 5248)
  - RFC 3464 - An Extensible Message Format for Delivery Status Notifications
  - RFC 3798 - Message Disposition Notification (updates RFC 3461)
  - RFC 3834 - Recommendations for Automatic Responses to Electronic Mail
  - RFC 4408 - Sender Policy Framework (SPF) Authorizing Use of Domains in E-Mail, Version 1
  - RFC 4409 - 廃止→ RFC 6409
  - RFC 4871 - 廃止→ RFC 6376
  - RFC 4952 - Overview and Framework for Internationalized Email (updated by RFC 5336)
  - RFC 4954 - SMTP Service Extension for Authentication (updates RFC 3463, updated by RFC 5248)
  - RFC 5068 - Email Submission Operations: Access and Accountability Requirements (BCP 134)
  - RFC 5248 - A Registry for SMTP Enhanced Mail System Status Codes (BCP 138) (updates RFC 3463)
  - RFC 5321 - The Simple Mail Transfer Protocol (updates RFC 1123)
  - RFC 5322 - Internet Message Format
  - RFC 5336 - 廃止→ RFC 6531
  - RFC 5504 - Downgrading Mechanism for Email Address Internationalization
  - RFC 5672 - 廃止→ RFC 6376
  - RFC 6152 - 8BITMIME拡張について
  - RFC 6376 - DomainKeys Identified Mail (DKIM) Signatures
  - RFC 6409 - Message Submission for Mail (STD 72)
  - RFC 6522 - The Multipart/Report Content Type for the Reporting of Mail System Administrative Messages
  - RFC 6531 - SMTP Extension for Internationalized Email Addresses
  - RFC 7504 - SMTP 521 and 556 Reply Codes
  - RFC 8314 - Cleartext Considered Obsolete: Use of Transport Layer Security (TLS) for Email Submission and Access

## 脚注

<references/>

## 関連項目

  - [Outbound Port 25 Blocking](../Page/Outbound_Port_25_Blocking.md "wikilink")
  - [POP3](../Page/Post_Office_Protocol.md "wikilink")
  - [IMAP](../Page/Internet_Message_Access_Protocol.md "wikilink")
  - [スパム (メール)](../Page/スパム_\(メール\).md "wikilink")（いわゆる迷惑メール）
  - [:en:List of mail server software](https://ja.wikipedia.org/wiki/:en:List_of_mail_server_software "wikilink")

[Category:電子メールのプロトコル](https://ja.wikipedia.org/wiki/Category:電子メールのプロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink")

1.  J. B. Postel著: Simple Mail Transfer Protocol
2.  J. Klensin 編: Simple Mail Transfer Protocol
3.  J. Klensin 編: Simple Mail Transfer Protocol
4.