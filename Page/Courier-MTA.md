> この記事は[Courier-MTA](https://ja.wikipedia.org/wiki/Courier-MTA)から翻訳されています。


**Courier-MTA**(クーリエエムティーエー、単に**Courier**と呼ばれる場合もある)は、[メールサーバ](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")を構築する際に必要になるであろう[SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")/[POP3](https://ja.wikipedia.org/wiki/POP3 "wikilink")/[IMAP4](https://ja.wikipedia.org/wiki/IMAP4 "wikilink")などを軸に、[電子メール](../Page/電子メール.md "wikilink")を扱う上で必要と思われる機能を各種取りそろえた[オープンソース](../Page/オープンソース.md "wikilink")の統合メール環境であり、[POSIX](../Page/POSIX.md "wikilink")の仕様に沿った環境であれば[OSを問わずに動作させることができる](../Page/オペレーティングシステム.md "wikilink")。

また、プロジェクトの巨大化により[MTAの範疇を大幅に超えたため](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink")、公式サイトも含め、「**Courier Mail Server**」という呼称が一般的となってきている。

## 概要

[qmail](https://ja.wikipedia.org/wiki/qmail "wikilink")が1.03を最後に更新されなくなっていたことをうけ、qmailの利用者が集まるコミュニティサイト上で、qmailの堅牢性と、より簡便なメールサーバを求める人々により開発が始まった。このため、Courier-MTAでは[Maildir](https://ja.wikipedia.org/wiki/Maildir "wikilink")形式のメールボックスや、インストール直後のオープンリレー禁止など、基本的な部分の多くにおいてqmailの実装方針に倣ったものとなっている。また、Courier-MTA標準の設定ファイルのほかに、qmailの設定ファイルである.qmail形式にも対応している。

Courier-MTAは、その名前に「[MTA](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink")」と名乗っているが、メールフィルタリングを司るCourier-Maildropや[メーリングリスト](../Page/メーリングリスト.md "wikilink")を司るCourier-MLMを筆頭に、[MUAであるテキスト](../Page/電子メールクライアント.md "wikilink")[コンソール](../Page/コンソール.md "wikilink")用のCourier-Coneや[ウェブメール](https://ja.wikipedia.org/wiki/ウェブメール "wikilink")を司るCourier-Webmailなど、電子メールというキーワードに関わるありとあらゆるものが一つに詰め込まれている。これらの[プログラム群は単体での利用も可能であり](../Page/プログラム_\(コンピュータ\).md "wikilink")、世間一般では[IMAP4](https://ja.wikipedia.org/wiki/IMAP4 "wikilink")を司る。

## 認証システム

各種電子メール[プロトコル](../Page/プロトコル.md "wikilink")ごとに独自のプログラムを個別に用意した場合などに煩雑になりがちな認証システムを一本化する目的で、各種認証システムへのラッパーとなるCourier-Authlibと、その中枢を担い、上位プログラムの統一された入り口となる「Courier-Authdaemon」という[デーモンプログラムにより](../Page/デーモン_\(ソフトウェア\).md "wikilink")、Courier-MTAの認証システムは一元的に扱うことができる。認証に用いるアカウント情報保持には、独自形式のファイルを用いる方法の他にも、LDAPディレクトリサービスやBerkeley DB、MySQL、PostgreSQLといった各種データベースを用いるためのプラグインライブラリも標準で用意されており、これらを利用することで大規模なシステムにも簡便に対応可能である。

## Courier Mail Serverのパッケージ構成物

### Courier

コアパッケージ。

### Courier Authentication Library

通称Authlib。 Courierの認証を包括するラッパーライブラリ。 このライブラリのインターフェイスに併せた実体プラグインを用意することによって、非常に容易にMySQLやPostgreSQL、LDAPなどを認証バックエンドとすることができる。

### Courier Unicode Library

### Courier Analog

メールの送受信ログを解析するソフトウェアである。

### Courier-IMAP

IMAP4サーバーである。

### SqWebMail

WebメールCGIである。 Apacheなどにホスティングして使用する。

### maildrop

メールフィルタリングを司るソフトウェア。

### courier-sox

Socks5プロクシクライアントを構築するためのライブラリ。 もともとはCourier本体がSocks5をサポートするために開発されたものだが、汎用性が極めて高いため単体パッケージとなった。

### Cone

テキストベースの電子メールクライアント。 各種UNIXのコンソール上で動作する。

### sysconftool

## 脚注

<references/>

## 関連項目

  - [qmail](https://ja.wikipedia.org/wiki/qmail "wikilink")
  - [Sendmail](../Page/Sendmail.md "wikilink")
  - [Postfix](../Page/Postfix.md "wikilink")

## 外部リンク

  - [Courier-MTAホームページ](http://www.courier-mta.org/) (英語)
  - [Courier-MTAホームページ](http://www.courier-mta.info/) (日本語)

[Category:メール転送エージェント](https://ja.wikipedia.org/wiki/Category:メール転送エージェント "wikilink") [Category:メール配送エージェント](https://ja.wikipedia.org/wiki/Category:メール配送エージェント "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")