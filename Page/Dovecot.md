> この記事は[Dovecot](https://ja.wikipedia.org/wiki/Dovecot)から翻訳されています。


**Dovecot**（ダヴコット）とは、[Unix系](../Page/Unix系.md "wikilink")の[OS上で動作する](../Page/オペレーティングシステム.md "wikilink")、[IMAPと](../Page/Internet_Message_Access_Protocol.md "wikilink")[POP3の](../Page/Post_Office_Protocol.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")である。[セキュアなシステムを意識した設計方針をとり](https://ja.wikipedia.org/wiki/情報セキュリティ "wikilink")、らによって開発・公開されている。

[Courier-MTA](https://ja.wikipedia.org/wiki/Courier-MTA "wikilink")や[UW IMAPに変わり](https://ja.wikipedia.org/wiki/:en:UW_IMAP "wikilink")、標準的な地位を占めるようになっている。IMAPサーバとしては、その過半数を占めているという記事\[1\]もある。[Mac OS X Server v10.6では](https://ja.wikipedia.org/wiki/macOS_Server#Mac_OS_X_Server_v10.6 "wikilink")、標準のPOP3/IMAPサーバーとして従来の[Cyrus IMAPから置き換えられた](../Page/Cyrus_IMAP_server.md "wikilink")\[2\]。

## 概要

  - POP3/IMAP4rev1に完全に対応する。また、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")の通信や[STARTTLS](https://ja.wikipedia.org/wiki/STARTTLS "wikilink")を含む[SSL暗号化にも対応する](../Page/Transport_Layer_Security.md "wikilink")。
  - [UNIX](../Page/UNIX.md "wikilink")標準として使われていた[mbox](https://ja.wikipedia.org/wiki/mbox "wikilink")形式や、IMAPで標準的に使われる[Maildir](https://ja.wikipedia.org/wiki/Maildir "wikilink")形式などのフォーマットにも対応しながら、インデックス化することで高速に動作させることができる。
  - [Postfix](../Page/Postfix.md "wikilink")（2.3以降）や[Exim](https://ja.wikipedia.org/wiki/Exim "wikilink")（4.64以降）などの[MTAに対し](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink")、[SMTP認証のバックエンドとして動作することが可能である](https://ja.wikipedia.org/wiki/SMTP-AUTH "wikilink")。
  - [NFS](https://ja.wikipedia.org/wiki/NFS "wikilink")上でも動作する。
  - [プラグイン](../Page/プラグイン.md "wikilink")で様々に拡張できる。

## 脚注

<references />

## 外部リンク

  - [Dovecot公式サイト](http://www.dovecot.org/)
  - [OX Dovecot株式会社公式サイト](http://www.dovecot.co.jp/)

[Category:メール配送エージェント](https://ja.wikipedia.org/wiki/Category:メール配送エージェント "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.  <https://support.apple.com/kb/PH8695>