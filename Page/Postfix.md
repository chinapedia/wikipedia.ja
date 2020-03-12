> この記事は[Postfix](https://ja.wikipedia.org/wiki/Postfix)から翻訳されています。


**Postfix**（ポストフィックス）は[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")・[オープンソース](../Page/オープンソース.md "wikilink")ソフトウェアの[メール転送エージェント](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink")(MTA)である。先行して開発されていた[Sendmail](../Page/Sendmail.md "wikilink")との操作上の互換性を確保しつつ、管理・設定が容易で、高速・安全であることを指向して開発されている。完全にUNIX用のMTAシステムとして設計されているため、UNIX上の他の多くのソフトウェアと連携が必要となる場合がある。

[NetBSD](../Page/NetBSD.md "wikilink")、[macOS Serverなど](https://ja.wikipedia.org/wiki/macOS_Server "wikilink")、いくつかの[UNIX](../Page/UNIX.md "wikilink") / [Unix系](../Page/Unix系.md "wikilink")OSで標準のMTAとして採用されている。

ライセンスは[IBM Public License](https://ja.wikipedia.org/wiki/IBM_Public_License "wikilink") 1.0であったが、バージョン3.2.5以降では、[Eclipse Public License](https://ja.wikipedia.org/wiki/Eclipse_Public_License "wikilink") 2.0も選択できるようになった。

Postfixシステムは一つのプログラムではなく、複数のコアプログラムから成り立っている。

かつては**VMailer**および**IBM Secure Mailer**という名前であった。が[IBM](../Page/IBM.md "wikilink") [トーマス・J・ワトソン研究所](../Page/トーマス・J・ワトソン研究所.md "wikilink")で開発を開始し、現在も活発に開発が行われている。Postfixの最初のリリースは[1999年](../Page/1999年.md "wikilink")中頃に行われた。

2017年のE-Softによる調査では、外部からアクセス可能なメールサーバーとして、[Exim](https://ja.wikipedia.org/wiki/Exim "wikilink")に次ぐ34%のシェアを占めている\[1\]。

## 機能

  - [Transport Layer Security](../Page/Transport_Layer_Security.md "wikilink") (TLS)
  - 外部のプロセスを利用した[SMTPポリシーの強制やコンテンツフィルタリングが可能](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")
  - マッピングに複数の[データベース](../Page/データベース.md "wikilink")が利用可能。今のところ、[Berkeley DB](../Page/Berkeley_DB.md "wikilink")、[cdb](https://ja.wikipedia.org/wiki/cdb "wikilink")、[dbm](https://ja.wikipedia.org/wiki/dbm "wikilink")、[LDAP](../Page/Lightweight_Directory_Access_Protocol.md "wikilink")、[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")、[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")を利用可能
  - [mbox](https://ja.wikipedia.org/wiki/mbox "wikilink")スタイルのメールボックスおよび[Maildir](https://ja.wikipedia.org/wiki/Maildir "wikilink")スタイルのメールボックス、バーチャルドメインに対応
  - アドレス書き換え （エンベロープ、ヘッダー）、[VERP](https://ja.wikipedia.org/wiki/VERP "wikilink")、[SASL](https://ja.wikipedia.org/wiki/SASL "wikilink")を利用した[SMTP認証](https://ja.wikipedia.org/wiki/SMTP認証 "wikilink")などが可能
  - [Milter](https://ja.wikipedia.org/wiki/Milter "wikilink") [1](http://www.postfix-jp.info/trans-2.3/jhtml/MILTER_README.html) に対応
  - [Policyd-weight](https://ja.wikipedia.org/wiki/Policyd-weight "wikilink") を使用した[メールヘッダのチェックに対応](https://ja.wikipedia.org/wiki/電子メール#ヘッダ情報 "wikilink")。各種[DNSBL](../Page/DNSBL.md "wikilink")や[RFCへの準拠をチェックし](../Page/Request_for_Comments.md "wikilink")、[spamと判定したメールは本文を受信することなしにリジェクトすることで](../Page/スパム_\(メール\).md "wikilink")、サーバの負荷を緩和
  - [AIX](../Page/AIX.md "wikilink")、[BSD系OS](../Page/BSDの子孫.md "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink")、[IRIX](../Page/IRIX.md "wikilink")、[Linux](../Page/Linux.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[Tru64](https://ja.wikipedia.org/wiki/Tru64 "wikilink")でコンパイル可能。つまり、[C言語](../Page/C言語.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")を持ち、[POSIX](../Page/POSIX.md "wikilink")に準拠し、[BSDソケット](https://ja.wikipedia.org/wiki/BSDソケット "wikilink")を持つすべてのUNIX / Unix系OSでコンパイル可能

Postfixの強みは[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")攻撃に強いことと、大量の電子メールをさばけることである。 Postfixは異なった[デーモンが協調動作するネットワークで構成される](../Page/デーモン_\(ソフトウェア\).md "wikilink")。 そして、各々のデーモンには1つの仕事しかなく、必要最小限の権限でそれを行う。 こうすることで、デーモンが攻略されたとしても、その影響はそのデーモンだけに留まり、システム全体に影響が及ぶことはない。 実際、管理者権限を持つデーモンは（常に[バックグラウンドプロセス](https://ja.wikipedia.org/wiki/バックグラウンドプロセス "wikilink")となる）*master* 一つだけで、Postfixの外への書き込みや外部プロセスの起動を行うのも*local*、*virtual*、*pipe*だけなので、ほとんどのデーモンは[chroot](https://ja.wikipedia.org/wiki/chroot "wikilink")して動作させることができる。

## 構造

Postfixの構造については[Postfix アーキテクチャの概要](http://www.postfix-jp.info/trans-2.3/jhtml/OVERVIEW.html)が詳しい。メッセージキュー、コアプログラム、ユーティリティプログラム、ルックアップテーブル、設定ファイルなどから構成される。

## 基本的な設定

サイトごとの設定は[main.cf](http://www.postfix-jp.info/trans-2.3/jhtml/postconf.5.html)で、デーモンプロセスの設定は[master.cf](http://www.postfix-jp.info/trans-2.3/jhtml/master.5.html)で行う。 [Postfix 基本設定](http://www.postfix-jp.info/trans-2.3/jhtml/BASIC_CONFIGURATION_README.html)には、各々のサイトで設定すべき主な項目が示されている。

[Postfix 標準設定の例](http://www.postfix-jp.info/trans-2.3/jhtml/STANDARD_CONFIGURATION_README.html)には、一般的な環境における設定の例が示されている。

[Postfix アドレス書き換え](http://www.postfix-jp.info/trans-2.3/jhtml/ADDRESS_REWRITING_README.html)では、アドレス書き換えとメールのルーティングについて述べられている。日本語で利用可能なドキュメントの一覧は、[Postfixのぺーじ － 和訳ドキュメント (2.3.x)](http://www.postfix-jp.info/trans-2.3/)にある。

## 脚注

<references />

## 関連項目

  - [メール転送エージェント](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink") (MTA)
  - [Simple Mail Transfer Protocol](../Page/Simple_Mail_Transfer_Protocol.md "wikilink") (SMTP)
  - [Transport Layer Security](../Page/Transport_Layer_Security.md "wikilink") (TLS)

## 外部リンク

  - [Postfixオフィシャルサイト](http://www.postfix.org/)
  - [Postfixのぺーじ](http://www.postfix-jp.info/)

[Category:メール転送エージェント](https://ja.wikipedia.org/wiki/Category:メール転送エージェント "wikilink") [Category:1997年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1997年のソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.