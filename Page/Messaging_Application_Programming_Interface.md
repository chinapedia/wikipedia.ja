> この記事は[Messaging Application Programming Interface](https://ja.wikipedia.org/wiki/Messaging_Application_Programming_Interface)から翻訳されています。


**Messaging Application Programming Interface**（**MAPI**）は、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") の [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") に基づくメッセージングアーキテクチャであり [Component Object Model](../Page/Component_Object_Model.md "wikilink") である。クライアントプログラムは、MAPIを[呼び出すことで特定のメッセージングサーバにアクセスし](https://ja.wikipedia.org/wiki/遠隔手続き呼出し "wikilink")、メッセージング機能を実現することができる。MAPI は [Microsoft Outlook](https://ja.wikipedia.org/wiki/Microsoft_Outlook "wikilink") が [Microsoft Exchange Server](../Page/Microsoft_Exchange_Server.md "wikilink") との通信に使う独自[通信プロトコル](../Page/通信プロトコル.md "wikilink") **MAPI/RPC** と密接に関連している。

Extended MAPI は全機能を提供するが、Simple MAPI はそのサブセットである。これにより、メッセージの生成・管理、メールボックスの管理などが可能となる。Simple MAPI は [Outlook Express](https://ja.wikipedia.org/wiki/Outlook_Express "wikilink")/[Windows Mail](https://ja.wikipedia.org/wiki/Windows_Mail "wikilink") の一部として [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") に含まれているが、Extended MAPI は [Microsoft Outlook](https://ja.wikipedia.org/wiki/Microsoft_Outlook "wikilink") および [Microsoft Exchange Server](../Page/Microsoft_Exchange_Server.md "wikilink") の一部となっている。

Extended MAPI、Simple MAPI に加えて、*Common Messaging Calls* (CMC) API インタフェースやオブジェクトベースの *[CDO](https://ja.wikipedia.org/wiki/:en:Collaboration_Data_Objects "wikilink") Library* インタフェースを使うこともできる。これらは Extended MAPI に比べて扱いやすく単純である（Simple MAPI と CMC は Exchange 2003 で削除された）。

MAPI は[マイクロソフト](../Page/マイクロソフト.md "wikilink")が設計した。MS Mail 開発チームが結成されたのは[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")だが、メッセージング製品は[1991年](../Page/1991年.md "wikilink")に Consumers Coftware Inc を買収して同社の *Network Courier* を獲得したのが最初である。これを修正して MS PC Mail (Microsoft Mail for PC Networking) として販売した。MS PC Mail の基本APIは MAPI version 0 (MAPI0) と呼ばれていた。MAPI の機能は [X.400](../Page/X.400.md "wikilink") XAPIA 規格に緩やかに準拠している。

MAPI には[メール転送エージェント](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink")や[ディレクトリ・サービス](https://ja.wikipedia.org/wiki/ディレクトリ・サービス "wikilink")へのアクセス機能も含まれている。

## サービスプロバイダ・インタフェース

Extended MAPI インタフェースは、Outlook のようなクライアントアプリケーションがメッセージベースのサービスにアクセスするのにも使われる。例えば、マイクロソフト以外の電子メールサーバ製品にも「MAPIサービスプロバイダ」を名のり Outlook によるアクセスを可能とした製品がある。例えば、[Zimbra](https://ja.wikipedia.org/wiki/Zimbra "wikilink")、[HP OpenMail](https://ja.wikipedia.org/wiki/:en:HP_OpenMail "wikilink")、[IBM Lotus Notes](https://ja.wikipedia.org/wiki/Lotus_Notes "wikilink")、[Zarafa](https://ja.wikipedia.org/wiki/Zarafa "wikilink")、[Bynari](https://ja.wikipedia.org/wiki/Bynari "wikilink") などがある。

MAPI0にも一種のサービスプロバイダ・インタフェースがあった。マイクロソフトはこれを社内で[XENIX](../Page/XENIX.md "wikilink")ベースの電子メールシステムに MS Mail がアクセスするのに使っていた。

Extended MAPI は Outlook の主要な電子メールデータアクセス方法であり、[Microsoft Exchange Server](../Page/Microsoft_Exchange_Server.md "wikilink") には Outlook に同梱されている MAPI サービスプロバイダ経由でアクセスする。

## MAPI/RPC プロトコルの詳細

マイクロソフトは最近になって、MAPI/RPC プロトコルの完全な詳細を公開した\[<http://msdn.microsoft.com/en-us/library/cc307725(EXCHG.80>).aspx\]。

「MAPI プロトコル」は MAPI/RPC の別名である。時には、"Exchange RPC" とか "Outlook-Exchange Transport Protocol" とも呼ばれている。

## 外部リンク

  - [Messaging API](http://msdn.microsoft.com/en-us/library/ms529058.aspx) at MSDN Library
  - [OpenChange project](http://www.openchange.org/) - MAPIプロトコルの詳細や関連ツールがある。

[Category:電子メール](https://ja.wikipedia.org/wiki/Category:電子メール "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:電子メールのプロトコル](https://ja.wikipedia.org/wiki/Category:電子メールのプロトコル "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")