> この記事は[Extensible Messaging and Presence Protocol](https://ja.wikipedia.org/wiki/Extensible_Messaging_and_Presence_Protocol)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:XMPP_logo.svg "wikilink")  **Extensible Messaging and Presence Protocol** (**XMPP**) (旧称 **Jabber**\[1\])は、[オープンソース](../Page/オープンソース.md "wikilink")の[インスタントメッセンジャー](../Page/インスタントメッセンジャー.md "wikilink")のプロトコルおよび、クライアント、サーバの総称である。

## 特徴

Jabber は Jabber 社が開発した [XML](../Page/Extensible_Markup_Language.md "wikilink") ベースの[プロトコル](../Page/プロトコル.md "wikilink")である **XMPP** を採用している。他のメジャーなインスタントメッセンジャーはその仕様もプロトコルも非公開となっているのが普通だが、Jabber はサーバもクライアントもオープンソースであり、その仕様は全て公開されている（[オープン標準](../Page/オープン標準.md "wikilink")）。そのため、たとえば[メールサーバ](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")と同じように、[ドメイン名](../Page/ドメイン名.md "wikilink")と[サーバ](../Page/サーバ.md "wikilink")さえあれば自分専用の XMPP サーバを立ち上げることができる。この点でほかのインスタントメッセージと異なる。

他の[インスタントメッセージングサービスの](../Page/インスタントメッセンジャー.md "wikilink")[ゲートウェイ](https://ja.wikipedia.org/wiki/ゲートウェイ "wikilink")となる機能も持つ。この機能を利用し、Jabber [クライアントから](../Page/クライアント_\(コンピュータ\).md "wikilink") [AOL Instant Messenger](https://ja.wikipedia.org/wiki/AOL_Instant_Messenger "wikilink")、[MSN Messenger](https://ja.wikipedia.org/wiki/MSN_Messenger "wikilink")(.NET Messenger Service)、[Yahoo\!メッセンジャー](https://ja.wikipedia.org/wiki/Yahoo!メッセンジャー "wikilink")、[IRC](https://ja.wikipedia.org/wiki/インターネット・リレー・チャット "wikilink")、[ICQ](https://ja.wikipedia.org/wiki/ICQ "wikilink") などのネットワークにメッセージを送ることができる。ただしサービスを提供している[サーバ](../Page/サーバ.md "wikilink")によっては、日本語が通らないこともある。

[Google Talk](https://ja.wikipedia.org/wiki/Google_Talk "wikilink") は、Jabber を核にしたものである。

## 歴史

は[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に Jabber テクノロジーに取り組み始め、1999年1月4日に  の最初のバージョンをリリースした\[2\]。初期の Jabber コミュニティはオープンソースソフトウェアに焦点を当てており、主に jabberd の開発をしていた（2000年5月にバージョン1.0、2000年10月にバージョン1.2、2001年2月にバージョン1.4を発表）が、一番の成果は XMPP プロトコルを作ったことである。

1999年から2000年に開発された初期の Jabber [プロトコル](../Page/プロトコル.md "wikilink")は XMPP の基礎となり、XMPP は RFC 3920 と RFC 3921 として公表されている。（IETF の XMPP Working Group による規格化の際に主に変わった部分は、伝送路の暗号化用に [TLS](../Page/Transport_Layer_Security.md "wikilink") の追加と認証用に [SASL](https://ja.wikipedia.org/wiki/Simple_Authentication_and_Security_Layer "wikilink") が追加されたところである。）XMPPはよく  の競合相手とみなされる。SIMPLE は [Session Initiation Protocol](https://ja.wikipedia.org/wiki/Session_Initiation_Protocol "wikilink") (SIP) プロトコルを基礎とする、インスタントメッセージングとプレゼンス通知の標準プロトコルである\[3\]\[4\]。

XMPP をベースにした最初の IM サービスは Jabber.org であり、1999年以降連続稼動していて XMPP のアカウントをフリーで提供している\[5\]。1999年から2006年2月まではサービスに jabberd を使用していたが、それ以降は  に移行した。（どちらも[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")のサーバアプリケーションである。）2010年1月には [Isode Ltd.](https://ja.wikipedia.org/wiki/Isode_Ltd. "wikilink") による[プロプライエタリ](https://ja.wikipedia.org/wiki/プロプライエタリ "wikilink")の M-Link へ移行する予定である\[6\]。

2005年8月に [Google](../Page/Google.md "wikilink") は [Google Talk](https://ja.wikipedia.org/wiki/Google_トーク "wikilink") を発表した。これは [VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink") と IM システムをあわせ持ち、インスタントメッセージングの機能に XMPP を使用していて、音声とファイル転送のシグナリングプロトコルのベースに XMPP を使用している。（最初のリリースにはサーバ間通信は含まれていなかったが、2006年1月17日にこの機能は有効になった。）\[7\]

2008年9月に[シスコシステムズ](https://ja.wikipedia.org/wiki/シスコシステムズ "wikilink")は Jabber, Inc. と商用プロダクトである Jabber XCP の開発者を買収した\[8\]。

2010年2月、ソーシャルネットワーキングサイトの [Facebook](../Page/Facebook.md "wikilink") は XMPP を通してチャット機能をサードパーティのアプリに開放した\[9\]。Facebook の開発者のサイトでは、次のように注意を呼びかけている。Facebook のチャットは内部で実際に XMPP サーバを稼働させているわけではなく、単にクライアントに XMPP のインターフェースを提供しているだけである。したがって、ユーザリストの編集など、サーバサイドの機能は XMPP 経由ではできないことがある\[10\]。

Google Talk だけでなく、多くの公共 IM サービスが XMPP を採用しており、Live Journal の LJ Talk\[11\] や Nokia の Ovi\[12\] などがそうである。さらに、企業の IM ソフトウェアプロダクトには、ネイティヴでは XMPP を使用できなくても XMPP へのゲートウェイを含むものがある。例えば、[IBM Lotus Sametime](https://ja.wikipedia.org/wiki/IBM_Lotus_Sametime "wikilink")\[13\]\[14\]や[Microsoft Office Communications Server](https://ja.wikipedia.org/wiki/Microsoft_Office_Communications_Server "wikilink") (OCS)\[15\]などである。

## 長所

  - 中央サーバを持たない : XMPP ネットワークの構造は[電子メール](../Page/電子メール.md "wikilink")に似ており、誰でも自分の XMPP サーバを立てることができるので、中央サーバが存在しない。
  - オープン標準 : XMPP はインスタントメッセージングサービスとプレゼンス技術として XMPP という名前で [IETF](../Page/Internet_Engineering_Task_Force.md "wikilink") により承認された。XMPP の仕様は RFC 3920 と RFC 3921 として公表されている。これらを実装するのにロイヤルティーは一切かからず、特定のベンダーに縛られることがない。
  - 歴史 : XMPP は1998年から利用されている。XMPP 標準のクライアント、サーバ、コンポーネント、ライブラリの実装は数多くあり、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")や Google などの大きな企業に支えられている。
  - セキュリティ : XMPP サーバは公共の XMPP ネットワークから切り離してもよく（例えば、会社でのイントラネットなど）、強固なセキュリティ（SASL や TLS を使用）が XMPP のコアに組み込まれている。伝送路の暗号化を促進するために、2009年10月30日までは[XMPP Standards Foundation](http://xmpp.org/)は[xmpp.net](http://xmpp.net/)に中間[認証局](https://ja.wikipedia.org/wiki/認証局 "wikilink")の設置も行っており、XMPP サーバの管理者にフリーの[デジタル証明書を提供していた](https://ja.wikipedia.org/wiki/公開鍵証明書 "wikilink")。また、PGPによるエンドツーエンドの暗号化にも対応している。
  - 柔軟性 : XMPP に加えてカスタムの機能を実装できる。相互運用性を保つために、一般的な拡張は XMPP Software Foundation により管理されている。IM 以上の機能を持つ XMPP アプリケーションとして、ネットワークマネージメント、コンテンツ配信、グループウェア、ファイル共有、ゲーム、リモートシステムの監視などがある。

## 短所

  - プレゼンスデータのオーバーヘッド : 一般にサーバ間通信の70パーセントがプレゼンスデータで\[16\]、そのうちの60パーセント近くが冗長であるので\[17\]、現在 XMPP はプレゼンスデータを複数のレシピエントへ転送する際に大きなオーバーヘッドがある。この問題を緩和する新しいプロトコルが考えられている。

<!-- end list -->

  - インバンドによるバイナリデータの転送は非効率 : XMPP は単一の長い XML ドキュメントとして符号化されるので、バイナリデータはインバンドで転送する前にまず Base64 でエンコードしなければならない。このため巨大なバイナリデータ（例えば、ファイル転送など）はアウトオブバンドで転送するのがもっとも良く、インバンドによる通信は制御用に用いる。最も良い例は XMPP の拡張プロトコルである（[XEP-0166](http://xmpp.org/extensions/xep-0166.html)）である。

## サーバの分散とアドレッシング

XMPP ネットワークは[クライアントサーバアーキテクチャを採用している](../Page/クライアントサーバモデル.md "wikilink")（クライアントは直接通信しない）が、中央サーバを持たない。権威ある中央サーバが存在しないように設計されており、これは[AOL Instant Messenger](https://ja.wikipedia.org/wiki/AOL_Instant_Messenger "wikilink") や [Windows Live メッセンジャーとは対照的である](https://ja.wikipedia.org/wiki/Windows_Live_メッセンジャー "wikilink")。jabber.org で動作している公共の XMPP サーバが存在しており、ここに多くのユーザが登録されているので、この点などでよく混乱されるが、誰でも自分のドメインで自分の XMPP サーバを立てることができる。XMPP の標準の[TCP](../Page/Transmission_Control_Protocol.md "wikilink") ポートは5222である。

ネットワーク上のすべてのユーザはユニークな Jabber ID（よく省略され JID と呼ばれる）を持つ。ID のリストを持つ中央サーバを不要にするため、JID は[メールアドレス](https://ja.wikipedia.org/wiki/メールアドレス "wikilink")のような構造を持っている。ユーザ名と、ユーザの存在するサーバのある[ドメイン名](../Page/ドメイン名.md "wikilink")があり、[アットマーク](../Page/単価記号.md "wikilink")（@）で仕切られる。例えば、username@example.com のようになる。

ひとりのユーザは複数の場所からログインするかも知れないので、クライアントでは更に追加でストリングを指定する。例えば、home、work、mobile など。このリソースで、ユーザのどのクライアントなのかを特定する。そしてこのリソースは、JID のあとにスラッシュに続けてリソース名を指定することで JID に含めることができる。リソースには優先度という数値を指定しても良い。例えば、あるユーザのモバイルアカウントの完全な JID は、username@example.com/mobile である。単に username@example.com に対して送られたメッセージはもっとも優先度の高いクライアントへ行くが、username@example.com/mobile に対して送られたものはモバイルクライアントのみへ行く。

## メッセージ転送の仕組み

*juliet@capulet.com* が *romeo@montague.net* へチャットをしたいとする。Juliet と Romeo はそれぞれ capulet.com と montague.net にアカウントを持っている。Juliet がタイプしてメッセージを送ると、一連のイベントが以下のように続く。

1.  Juliet のクライアントがメッセージを capulet.com のサーバへ送る。
      - capulet.com で montague.net がブロックされていると、メッセージは破棄される。
2.  capulet.comの サーバは montague.net へ向けてコネクションを張る。
      - montague.net で capulet.com がブロックされていると、メッセージは破棄される。
      - このとき Romeo が接続していなかったら、メッセージは後で送るために保存される。
3.  montague.net のサーバは Romeo にメッセージを送る。

|        |   |             |   |              |   |       |
| ------ | - | ----------- | - | ------------ | - | ----- |
| Juliet | → | capulet.com | → | montague.net | → | Romeo |

## 他のプロトコルへの接続

[Wie_ein_Jabber-Transport_funktioniert.svg](https://ja.wikipedia.org/wiki/File:Wie_ein_Jabber-Transport_funktioniert.svg "fig:Wie_ein_Jabber-Transport_funktioniert.svg") XMPP の他の便利な特徴はトランスポートである。ゲートウェイという名前でも知られていて、他のプロトコルを使うネットワークにアクセスすることが可能になる。インスタントメッセージングのプロトコルだけでなく、[SMS](https://ja.wikipedia.org/wiki/ショートメッセージサービス "wikilink") や[電子メール](../Page/電子メール.md "wikilink")などのプロトコルでも可能である。マルチプロトコル対応のクライアントと違って、リモートコンピュータで動作する特別なゲートウェイサービスを通して通信することで、サーバレベルでアクセス出来るようにしている。ユーザは、これらのゲートウェイのひとつにネットワークのログインに必要な情報を提供して「登録」する。すると、そのユーザは、XMPP のユーザと同じようにそのネットワークのユーザと通信できる。つまり、XMPP を完全にサポートしたクライアントであれば、ゲートウェイが存在するどんなネットワークのアクセスにも使えるということである。クライアントに一切コードを追加する必要がなく、クライアントが直接インターネットに接続できる必要もない。こういった機能は、使っているプロトコルの利用規約に違反する可能性があるが、国によって何カ国かでは、そのような利用規約は法的拘束力を持たない。

## 関連項目

  - RFC 3920 - Extensible Messaging and Presence Protocol (XMPP): Core
  - RFC 3921 - Extensible Messaging and Presence Protocol (XMPP): Instant Messaging and Presence
  - RFC 3922 - Mapping the Extensible Messaging and Presence Protocol (XMPP) to Common Presence and Instant Messaging (CPIM)
  - RFC 3923 - End-to-End Signing and Object Encryption for the Extensible Messaging and Presence Protocol (XMPP)

## 脚注

## 外部リンク

  - [XMPP Standards Foundation](http://xmpp.org/)
  - [XMPP Extensions](http://xmpp.org/extensions/)
  - [XMPP Software: Clients](http://xmpp.org/software/clients.shtml)
  - [XMPP Software: Servers](http://xmpp.org/software/servers.shtml)
  - [Open list of public XMPP servers](http://xmpp-servers.404.city)
  - [Jabber User Guide](http://archive.jabber.org/userguide/) - End user introduction to XMPP (archive)
  - [IETF Publishes XMPP RFCs](http://xmpp.org/xsf/press/2004-10-04.shtml)
  - [XMPP Case Studies](http://wiki.xmpp.org/web/XMPP_Case_Studies)
  - [Jabber.org (Free XMPP server of the XSF](http://www.jabber.org/)
  - [XMPP.JP](http://www.xmpp.jp/)

[Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:インスタントメッセンジャー](https://ja.wikipedia.org/wiki/Category:インスタントメッセンジャー "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.  [Jabber Inc. - About Us](http://www.jabber.com/CE/AboutUs)
2.  [Open Real Time Messaging System](http://tech.slashdot.org/article.pl?sid=99/01/04/1621211)
3.  "XMPP rises to face SIMPLE standard", Infoworld magazine, April 17, 2003 [XMPP rises to face SIMPLE standard](http://www.infoworld.com/d/developer-world/xmpp-rises-face-simple-standard-018)
4.  "XMPP vs SIMPLE: The race for messaging standards", Infoworld magazine, May 23, 2003 [Infoworld.com](http://www.infoworld.com/t/platforms/xmpp-vs-simple-race-messaging-standards-295)
5.  [Chatting Up the Chef](http://www.linuxjournal.com/article/6489) Linux Journal March 1, 2003 by Marcel Gagné
6.
7.
8.
9.
10.
11. [Question FAQ \#270](http://www.livejournal.com/support/faqbrowse.bml?faqid=270)
12. [Ovi Contacts](http://betalabs.nokia.com/betas/view/contacts-ovi)
13. "Lotus Sametime 7.5 Interoperates with AIM, Google Talk", eWeek, December 6, 2006 [Eweek.com](http://www.eweek.com/c/a/Messaging-and-Collaboration/Lotus-Sametime-75-Interoperates-with-AIM-Google-Talk/)
14. "Lotus ships gateway to integrate IM with AOL, Yahoo, Google", Network World, December 6, 2006 [Networkworld.com](http://www.networkworld.com/news/2006/120606-sametime-links-up-with-aim.html)
15. "Unified Communications: Uniting Communication Across Different Networks", Microsoft Press Release, October 1, 2009 [Microsoft.com](https://www.microsoft.com/Presspass/Features/2009/oct09/10-01UCInterop.mspx)
16. [\[Standards-JIG](http://mail.jabber.org/pipermail/standards/2006-May/011158.html) Distribution of stanza types\]
17. [\[Standards-JIG](http://mail.jabber.org/pipermail/standards/2006-May/011182.html) proto-JEP: Smart Presence Distribution\]