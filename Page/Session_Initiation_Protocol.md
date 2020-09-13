> この記事は[Session Initiation Protocol](https://ja.wikipedia.org/wiki/Session_Initiation_Protocol)から翻訳されています。


**Session Initiation Protocol**（**セッション イニシエーション プロトコル**、**SIP**、**セッション確立プロトコル**）とは 2 つ以上のクライアント間で[セッション](../Page/セッション.md "wikilink")を確立するための [IETF](../Page/Internet_Engineering_Task_Force.md "wikilink") 標準の[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。[IP電話](../Page/IP電話.md "wikilink")の呼制御などに利用されている。

## 概要

SIP は [H.323](../Page/H.323.md "wikilink") に代わる汎用のセッション制御プロトコルとして DynamicSoft（当時） の J. Rosenberg らを中心に開発された（ここでいう“セッション”とは [OSI参照モデル](../Page/OSI参照モデル.md "wikilink") で規定される第5層とは異なる）。現在の主な用途は電話、[テレビ電話](../Page/テレビ電話.md "wikilink")や[インスタント・メッセージングのような双方向のリアルタイム通信である](../Page/インスタントメッセンジャー.md "wikilink")。このようなリアルタイム通信においては基本的に通信者は対等であり、[サーバ](../Page/サーバ.md "wikilink")と[クライアントというような役割分担は存在しない](../Page/クライアント_\(コンピュータ\).md "wikilink")。SIP においてはこれを、両者がサーバとクライアントの機能をあわせもつというかたちで表現している。すなわち、SIP は [HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink") (ハイパーテキスト転送プロトコル) をもとにしてつくられたので基本的には 要求-応答型 のプロトコルだが、要求者 (後述の UAC) がクライアントであり、応答者 (後述の UAS) がサーバであるが、両者がこれら両方の役割を演じることができる。

HTTP においてはその下層のプロトコルとして高信頼な [TCP](../Page/Transmission_Control_Protocol.md "wikilink") を使用することが前提とされているが、SIPでは [UDP](../Page/User_Datagram_Protocol.md "wikilink") を元に設計されている。しかし、商用では信頼性のため後に拡張された [TCP](../Page/Transmission_Control_Protocol.md "wikilink") が使用される場合が多い。SIP はセキュリティやプライバシーを守るための機能拡張も備える。

## 特徴

同じ、リアルタイム・[マルチメディア](../Page/マルチメディア.md "wikilink")・データ通信プロトコルの[H.323](../Page/H.323.md "wikilink")と比較すると、以下の点が特徴である。

  - セッションの開始・変更・終了のみを行うため単純である。
  - [HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink") 1.1に似た[テキスト](../Page/テキスト.md "wikilink")ベース・メッセージ・フォーマットであるため、[ソフトウェア](../Page/ソフトウェア.md "wikilink")の機能の追加・拡張が容易である。
  - インターネットアーキテクチャで電話などのセッションをコントロールするためのプロトコルである。従来の電話の制御はネットワークの中心にある交換機による集中制御方式で実現されており、端末側で簡単にサービスを追加できない方式であった。これに対してインターネットアーキテクチャでは、ネットワークは情報を伝達する仕組みに徹し、端末側でサービスを任意に追加できるアーキテクチャである。SIPで電話の仕組みを作ることにより、インターネットと同様に、ユーザが端末側で自由に電話サービス（[映像](https://ja.wikipedia.org/wiki/映像 "wikilink")系も含む）を追加することが可能となる。ちなみにH.323はIPで電話、映像などの接続制御を行うための規約であるが、集中制御型の信号方式であるため、従来の交換機のアーキテクチャと同じである。

<!-- end list -->

  - [VoIP](../Page/VoIP.md "wikilink")の通信プロトコルとしてSIPを使用する場合、音声などのストリーミング送受信には[RTP](../Page/Real-time_Transport_Protocol.md "wikilink")/[RTCP](../Page/Real-time_Transport_Control_Protocol.md "wikilink")、制御を行うデータ送受信ホスト・ポートの制御には [Session Description Protocol](../Page/Session_Description_Protocol.md "wikilink") (SDP) を使用することが一般的である。

<!-- end list -->

  - SIPメッセージの送受信を行う[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")として、標準で5060が規定されている。SIPメッセージのヘッダ部内でホストと共に記述可能な[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")が省略される場合、5060を指定することと同義となる。

## ユーザーエージェント

[ユーザーエージェント](../Page/ユーザーエージェント.md "wikilink") (UA : User Agent) は、SIP リクエストを処理する論理的なエンティティであり、つぎの 2 個の要素から構成される。

  - ユーザーエージェント・[クライアント](../Page/クライアント_\(コンピュータ\).md "wikilink") (UAC : User Agent Client) - SIP リクエストを生成・送信し、応答を受信・処理するUA。
  - ユーザーエージェント・[サーバ](../Page/サーバ.md "wikilink") (UAS : User Agent Server) - SIP リクエストを受信・処理し、応答を生成・送信するUA。

従来のレガシーな電話システムに置き換えると、SIP サーバが交換機の代わりになるように見える。しかし、SIP のサービスの主導権を持っているのはユーザーエージェント (UA) であり、SIP サーバは UA からの依頼により、認証と電話番号解決を行うだけの一種の代理人 (Proxy) である。発側の UA がサービスを要求し、着側の UA がサービスを提供するという関係であり、これはインターネットのブラウザと WEB サーバの関係と同じである。これらの機能は共に UA が提供する。発側の機能を UAC (UA Client)、着側の機能を UAS（UA Server）という。つまり、SIP の電話機は発信するときはクライアント (UAC) として振る舞い、着信するときはサーバ (UAS) として振舞う。

## SIP サーバ

[SIP-registration-flow.png](https://ja.wikipedia.org/wiki/File:SIP-registration-flow.png "fig:SIP-registration-flow.png") [SIP_call_flow_between_UA,_Redirect_Server,_Proxy_and_UA.png](https://ja.wikipedia.org/wiki/File:SIP_call_flow_between_UA,_Redirect_Server,_Proxy_and_UA.png "fig:SIP_call_flow_between_UA,_Redirect_Server,_Proxy_and_UA.png") [SIP-B2BUA-call-flow.png](https://ja.wikipedia.org/wiki/File:SIP-B2BUA-call-flow.png "fig:SIP-B2BUA-call-flow.png")

SIP サーバは、SIP リクエストを処理する SIP エンティティである。UA 同士は直接 SIP のメッセージを交換することができるが、通常は SIP サーバ (SIP [プロキシ](../Page/プロキシ.md "wikilink")サーバ) を介してメッセージ交換する。これは、SIP プロキシサーバを介することによって SIP URI から IP アドレスを求める操作（[DNSサーバで](../Page/Domain_Name_System.md "wikilink")[ホスト名](../Page/ホスト名.md "wikilink")を[IPアドレス](../Page/IPアドレス.md "wikilink")を求めるのと同じような操作）を UA が行う必要がなくなり、通信相手が移動するなどして IP アドレスが変化してもそれを意識せずに通信することができるからである。

SIP サーバの次の各機能をそれぞれ物理的に別にしても 1 つにまとめても良い。

  - [プロキシ](../Page/プロキシ.md "wikilink")・サーバ (Proxy Server) - SIP メッセージの転送 (ルーティング) を行うサーバ。SIP ヘッダに含まれる受信先アドレスをキーとして場所サーバへの問い合わせを行って受信先の IP アドレスを求め、それに基づいてメッセージの転送先を決定する。転送先は受信先の IP アドレスであるか、または他のプロキシ・サーバである。このメッセージ・ルーティングの方法は SMTP によるメールのルーティングと同じである。
  - リダイレクト・サーバ (Redirect Server) - SIP リクエストの次の転送先を解決し、その転送先を応答で送信するサーバ。
  - 登録サーバ (Registrar) - UA からのメッセージに基づいてそのコンタクトアドレス (SIP URI と IP アドレスの対) を場所サーバに登録するサーバ。ユーザエージェントがネットワークに接続されると、ある間隔で REGISTER メッセージを送出する。REGISTER メッセージは SIP プロキシサーバ経由でレジストラに送られ、これに基づいてレジストラが上記の登録をおこなう。すなわち、レジストラへの入力は SIP メッセージ (REGISTER) である。
  - 場所サーバ (Location Server) - UA が存在するネットワーク上の場所を管理するデータベース管理サーバ。SIP URI と IP アドレスの対をレジストラから受け取って登録し、登録情報に基づいて SIP プロキシサーバからの問い合わせに返答する。場所サーバの入出力は SIP メッセージではない。

従来の交換機の付加サービスにおいて着信に自動応答して音声メッセージを流したりする機能を提供するサーバは厳密には SIP サーバではなくてユーザエージェントである。すなわち、SIP の UAS（User Agent Server）の集合体として構成されている。

## SIP におけるユーザアドレスとその構造

SIP において電話番号に相当するものが **SIP URI** (Uniform Resource Identifier) であり、[メールアドレスと](https://ja.wikipedia.org/wiki/メールアドレスと "wikilink")同様に 名前@ドメイン という形式をしている (ただし、SIP URI であることを示すために先頭に sip: が付けられる)。SIP URI の例を挙げる。

<sip:bob@biloxi.example.com>

SIP URI は特定のひとや端末を表すとは限らない。複数のひとや端末を1つのグループとして、1つの SIP URI で表すこともできる。これは、電話番号でいえば代表番号を用意するに相当する。 たとえば、受信先に個を特定するアドレスが指定された場合、指定された相手が故障中など通信不能であれば接続できないが、グループ・アドレスが指定された場合、そのグループの中に故障中のものがあっても、他の通信可能なものを選んで接続することができる。

## SIP における標準的なシーケンス

下図のシーケンスは SIP サーバを経由しない (またはそれが省略された) Alice と Bob との会話の標準的なシーケンスである。

`  Alice                     Bob `
`    |                        | `
`    |       INVITE F1        | `
`    |----------------------->| `
`    |    180 Ringing F2      | `
`    |<-----------------------| `
`    |                        | `
`    |       200 OK F3        | `
`    |<-----------------------| `
`    |         ACK F4         | `
`    |----------------------->| `
`    |   Both Way RTP Media   | `
`    |<======================>| `
`    |                        | `
`    |         BYE F5         | `
`    |<-----------------------| `
`    |       200 OK F6        | `
`    |----------------------->| `
`    |                        | `

Alice が ACK メッセージを送信したあと、Bob から BYE メッセージを受信するまで RTP メディアによる双方向の通信がつづいている (上図の "Both Way RTP Media")。

SIP サーバを経由するシーケンスの例を下図にあげる (RFC 3261 から引用)。ここでは atlanta.com と biloxi.com にある 2 個の SIP プロキシを経由して Alice と Bob とのあいだでメッセージを交換している。これらのプロキシが INVITE メッセージを受信した直後に 100 Trying 応答をかえしていることを除けば、これらのプロキシはメッセージを中継しているだけである。

`                    atlanta.com  ...biloxi.com`
`                .     proxy              proxy     .`
`              .                                      .`
`      Alice's  ......................................... Bob's`
`     softphone                                        SIP Phone`
`        |                |                |                |`
`        |    INVITE F1   |                |                |`
`        |--------------->|    INVITE F2   |                |`
`        |  100 Trying F3 |--------------->|    INVITE F4   |`
`        |<---------------|  100 Trying F5 |--------------->|`
`        |                |<-------------- | 180 Ringing F6 |`
`        |                | 180 Ringing F7 |<---------------|`
`        | 180 Ringing F8 |<---------------|     200 OK F9  |`
`        |<---------------|    200 OK F10  |<---------------|`
`        |    200 OK F11  |<---------------|                |`
`        |<---------------|                |                |`
`        |                       ACK F12                    |`
`        |------------------------------------------------->|`
`        |                   Media Session                  |`
`        |<================================================>|`
`        |                       BYE F13                    |`
`        |<-------------------------------------------------|`
`        |                     200 OK F14                   |`
`        |------------------------------------------------->|`
`        |                                                  |`

## 関連項目

  - [VoIP](../Page/VoIP.md "wikilink")
  - [IP電話](../Page/IP電話.md "wikilink")
  - [MGCP](https://ja.wikipedia.org/wiki/MGCP "wikilink")、[Media Gateway Control Protocol](https://ja.wikipedia.org/wiki/Media_Gateway_Control_Protocol "wikilink")
  - [NOTASIP](https://ja.wikipedia.org/wiki/NOTASIP "wikilink")
  - [Asterisk (PBX)](../Page/Asterisk_\(PBX\).md "wikilink")
  - [IPマルチメディアサブシステム](https://ja.wikipedia.org/wiki/IPマルチメディアサブシステム "wikilink")

## 外部リンク

  - RFC 3261 - Session Initiation Protocol
  - RFC 4566 - Session Description Protocol
  - [SIP Working Group](http://www.ietf.org/html.charters/sip-charter.html) - IETF
  - [SIP Protocol Overview](http://www.en.voipforo.com/SIP/SIP_architecture.php)

[Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink")