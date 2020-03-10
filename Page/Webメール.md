> この記事は[Web](https://ja.wikipedia.org/wiki/Web)から翻訳されています。


**Webメール**（ウェブメール）は[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")を通じてアクセスする、[Webアプリケーションの](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")（メール[ユーザーエージェント](../Page/ユーザーエージェント.md "wikilink")・電子メールクライアント）である。クライアントのPCにウェブブラウザ以外のソフトウェアのインストールや設定が不要であるため手軽に利用できる。[フリーメールサービス](../Page/フリーメールサービス.md "wikilink")などで提供されるほか、Webメールシステムを構築するサーバソフトウェアも公開されている。クライアントであるウェブブラウザとサーバはほとんどの場合セキュリティ上の理由から、[HTTPS](../Page/HTTPS.md "wikilink")（Hypertext Transfer Protocol over Secure Socket Layer）スキームを使用して通信を行う。

## 特徴

クライアントの環境としてウェブブラウザ以外のソフトウェアを必要としない。メールアドレスやログインID、パスワードを覚えるだけでよく、[POP3や](../Page/Post_Office_Protocol.md "wikilink")、[IMAP4](../Page/Internet_Message_Access_Protocol.md "wikilink")、[SMTPなどの細かい設定が不要である](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")。そのため、複数で共有しているコンピュータなど設定を変更することのできないクライアントからも利用可能である。

ローカルにメールを保存しないため、コンピュータをリプレイスした場合でもデータの移行が不要である反面、障害やメンテナンスによるサーバの停止、およびネットワークに接続できない場合など、受信済みのメールの閲覧も不可能となる。これは同じくサーバ側にメールを保存するIMAP4サーバと同様の短所である。

## Webメールサービス

Webメールサービスは[フリーメールサービス](../Page/フリーメールサービス.md "wikilink")で用いられることが多いが、[インターネット接続サービスのメールサービスでも利用者の利便性を考慮してPOP](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")3、SMTP、IMAP4などとともに採用しているところも多い。

Webメールを採用しているフリーメールサービスには、[Yahoo\!メール](../Page/Yahoo!メール.md "wikilink")、[Gmail](../Page/Gmail.md "wikilink")、[Outlook.com](https://ja.wikipedia.org/wiki/Outlook.com "wikilink")などがある。これらのフリーメールサービスではサーバがダウンしてデータが消失しても責任を負わない、などの免責事項を設けていることが多い。またプロバイダや[ポータルサイト](../Page/ポータルサイト.md "wikilink")のメールを携帯電話のWebメールで利用するといったものは近年ではあたりまえのように存在するが、それとは正反対に、[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")の[iモードメール](https://ja.wikipedia.org/wiki/iモードメール "wikilink")を、自宅のPCや[android](https://ja.wikipedia.org/wiki/android "wikilink")、[Windows Mobile](../Page/Windows_Mobile.md "wikilink")、[BlackBerry](../Page/BlackBerry.md "wikilink")といった[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")のWebメールで送受信できるサービスとして[iモード.net](https://ja.wikipedia.org/wiki/iモード.net "wikilink")といったものもある。同様のサービスは[KDDI](../Page/KDDI.md "wikilink")も[au one メールという名称で](https://ja.wikipedia.org/wiki/au_one_メール "wikilink")2013年9月30日まで利用者に提供していた。

### 機能

大半のWebメールサービスは一般的な電子メールクライアントと同様、受信メールを条件により任意の[フォルダ](https://ja.wikipedia.org/wiki/フォルダ "wikilink")や[ゴミ箱に振り分けるフィルタ](https://ja.wikipedia.org/wiki/ごみ箱_\(GUI\) "wikilink")、アドレス帳などの機能を持っている。Webメールサービスによっては、 [コンピュータウイルス](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")の自動駆除、[スパムのフィルタリング機能などを提供している](../Page/スパム_\(メール\).md "wikilink")。

### 規制

企業や学校、図書館などの公共機関によってはWebメールの私的使用による[個人情報](../Page/個人情報.md "wikilink")や、機密文書の持ち出し（メールへの添付）による情報漏洩、[コンピュータウイルス](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")感染などのトラブルを防ぐため、[サーバ](../Page/サーバ.md "wikilink")に[フィルタリング](https://ja.wikipedia.org/wiki/フィルタリング "wikilink")を導入し、フリーメールサービスを含めたWebメール全般にアクセスできないようにしているところがある。

## Webメールソフトウェア

Webメールを構築するためのさまざまなソフトウェアが公開されている。既存のPOP3、IMAP、SMTPなどのサーバにWebメールインターフェイスを追加するもの、自前で[メール転送エージェント](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink")を含んだサーバをもつもの、[グループウェア](../Page/グループウェア.md "wikilink")や[コンテンツ管理システム](../Page/コンテンツ管理システム.md "wikilink")などの一部として提供されるものなどがある。

### 主な実装

  - [Microsoft Exchange Server](../Page/Microsoft_Exchange_Server.md "wikilink") - [マイクロソフト](../Page/マイクロソフト.md "wikilink")から発売されているグループウェアの[Outlook Web Access](../Page/Outlook_Web_Access.md "wikilink")。
  - [Ipswitch IMail Server](https://ja.wikipedia.org/wiki/Ipswitch_IMail_Server "wikilink") - POP3、IMAP、SMTP、Webメール、[アンチウイルス](https://ja.wikipedia.org/wiki/アンチウイルス "wikilink")ソフトウェアなどをオールインワンにした商用のソフトウェア。[Windowsに対応](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。
  - [Internet Messaging Program](https://ja.wikipedia.org/wiki/Internet_Messaging_Program "wikilink") - IMAP4、SMTPサーバにアクセスするためのフリーのWebメールソフトウェア。[PHPで実装されている](../Page/PHP_\(プログラミング言語\).md "wikilink")。
  - [SquirrelMail](https://ja.wikipedia.org/wiki/SquirrelMail "wikilink") - IMAP4、SMTPサーバにアクセスするためのフリーのWebメールソフトウェア。PHPで実装されている。
  - [RoundCube](https://ja.wikipedia.org/wiki/RoundCube "wikilink") - IMAP4、SMTPサーバ対応。PHPで実装されており、[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")技術を利用しているのが特徴
  - [AtMail](https://ja.wikipedia.org/wiki/AtMail "wikilink") - IMAP4対応。RoundCube同様、Ajax技術を利用しているのが特徴。
  - [rainloop](https://www.rainloop.net/) - IMAP4対応。

### 携帯端末向け実装

  - [mobileimap](https://ja.wikipedia.org/wiki/mobileimap "wikilink") - IMAP、SMTPに対応した携帯端末向けフリーのWebメール。別にウェブサーバを必要とするCGIやPHPによる実装とは異なり、プログラム自体が[samba](https://ja.wikipedia.org/wiki/samba "wikilink")におけるswatのように[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")[デーモンとして動作する](../Page/デーモン_\(ソフトウェア\).md "wikilink")。
  - [WebMailClient2 for Keitai](https://ja.wikipedia.org/wiki/WebMailClient2_for_Keitai "wikilink") - POP3、IMAP、SMTPに対応した携帯端末向けフリーのWebメール。[Perl](../Page/Perl.md "wikilink")による実装。今のところ、日本語のみに対応。

## 関連項目

  - [電子メールクライアント](../Page/電子メールクライアント.md "wikilink")
  - [電子メール](../Page/電子メール.md "wikilink")
  - [メールマガジン](../Page/メールマガジン.md "wikilink")
  - [スパム (メール)](../Page/スパム_\(メール\).md "wikilink")

## 外部リンク

  - [SquirrelMail](http://www.squirrelmail.org/)
  - [RoundCube](https://roundcube.net/)
  - [IMP Webmail Client](http://www.horde.org/imp/)

[Category:電子メール](https://ja.wikipedia.org/wiki/Category:電子メール "wikilink")