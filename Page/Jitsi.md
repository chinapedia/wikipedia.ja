> この記事は[Jitsi](https://ja.wikipedia.org/wiki/Jitsi)から翻訳されています。


[サムネイル](https://ja.wikipedia.org/wiki/ファイル:Jitsi_Meet_Vido_Call.jpg "wikilink")

**Jitsi**は[フリーかつオープンソースで](https://ja.wikipedia.org/wiki/FLOSS "wikilink")、、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](../Page/Linux.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Android](../Page/Android.md "wikilink")といった[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")向けの[音声](../Page/VoIP.md "wikilink")（VoIP）、[ビデオカンファレンス](../Page/テレビ電話.md "wikilink")、[インスタントメッセージ](../Page/インスタントメッセージ.md "wikilink")アプリケーションのコレクションである\[1\]\[2\]\[3\]。JitsiプロジェクトはJitsi Desktop（旧称：[SIP](../Page/Session_Initiation_Protocol.md "wikilink") Communicator）の開発から始まった。[WebRTC](https://ja.wikipedia.org/wiki/WebRTC "wikilink")の普及に伴いプロジェクトチームはウェブペースの複数人ビデオ会話を実現するJitsi Video Bridgeの開発に集中するようになった。その後、チームは完全なビデオカンファレンスアプリケーションであるJitsi Meetを追加し、ウェブ、Android、iOSクライアントが利用可能になった。Jitsiは、Jitsi Meetをmeet.jit.siでホストしており、コミュニティは無料で利用できる。その他に開発しているプロジェクトとしては、Jigasi、lib-jitsi-meet、Jidesha、Jitsiがある\[4\]\[5\]\[6\]。

Jitsiは、NLnet Foundation\[7\]\[8\]、[ストラスブール大学](../Page/ストラスブール大学.md "wikilink")、Region of Alsace\[9\]など様々な機関から支援を受けており、[Google Summer of Codeプログラムにも複数回参加している](https://ja.wikipedia.org/wiki/Google_Summer_of_Code "wikilink")\[10\]\[11\]。

## Jitsiの主なプロジェクト

Jitsiは2020年4月現在、[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")で103個のリポジトリがオープンソースで公開されている。主なプロジェクトには以下のものがある\[12\]。

  - **Jitsi Meet** – Debian/Ubuntuサーバーで簡単にインストールできるように設計されたビデオ会議サーバー
  - **Jitsi Videobridge** – 複数人参加会議を動作させるWebRTCのSelective Forwarding Unitエンジン
  - **Jigasi** - 標準のSIPクライアントが、Jitsi VideobridgeでホストされたJitsi Meet会議に参加することを可能にするサーバーサイド・アプリケーション
  - **lib-jitsi-meet** - Jitsi MeetのためにカスタマイズされたUIを提供する低レベルのJavaScript API
  - **Jidesha** – Jitsi Meetのための[Google Chrome拡張機能](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")
  - **Jitsi** – 音声、ビデオ、チャットでのコミュニケーションを可能にする、SIP、XMPP/Jabber、AIM/ICQ、IRCプロトコルをサポートするプログラム

### Jitsi Meet

オープンソースのJavaScript WebRTCアプリケーションであり、ビデオ会議に使うことができる。Android、macOS、Windows、Linuxに対応している。デスクトップ画面やプレゼンテーションを共有でき、リンクで新しいメンバーをビデオ会議に招待できる。ブラウザで直接、またはアプリケーションをダウンロードして利用できる\[13\]\[14\]。

**Jitsi Meetの主な特徴**

  - 暗号化通信（[セキュア通信](../Page/セキュア通信.md "wikilink")）
  - [クライアントソフトウェアのインストールが不要](../Page/クライアント_\(コンピュータ\).md "wikilink")\[15\]

|                                                                      |                                                                                      |
| -------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| [代替文=](https://ja.wikipedia.org/wiki/ファイル:Jitsi_Meet.png "wikilink") | [代替文=](https://ja.wikipedia.org/wiki/ファイル:Jitsi_Meet_Vidoe_confrence.png "wikilink") |

### Jitsi Videobridge

複数ユーザーのビデオ通信を可能にするWebRTCをサポートするビデオ会議プログラムである。Selective Forwarding Unit（SFU）を利用して選択されたストリームだけを他のビデオ会議通話の参加ユーザーに転送するため、CPUの性能はパフォーマンスにそれほど重要ではない\[16\]\[17\]。

### Jitsi Desktop

Jitsiからは、Jitsi Video Bridge Selective Forwarding Unit（SFU）や、ウェブ会議アプリケーションのJitsi Meetなど、いくつかの姉妹プロジェクトが生まれた。これらの他のJitsiプロジェクトがよく知られるようになるにつれて、混同を防ぐために、Jitsiクライアントアプリケーションは**Jitsi Desktop**としてリブランディングされた。

プロジェクトは当初から[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")をサポートしていたため、主に実験的なツールとして使われていた\[18\]\[19\]。時が経つにつれ、プロジェクトは多くのメンバーを集め、[SIP](https://ja.wikipedia.org/wiki/SIP "wikilink")以外のプロトコルのサポートも追加されていった。

**機能**[サムネイルJitsiは](https://ja.wikipedia.org/wiki/ファイル:Confcall.png "wikilink")、[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、Linux、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[BSD](../Page/BSD.md "wikilink")のような[Unix系](../Page/Unix系.md "wikilink")システムを含む複数の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")をサポートしている。スマートフォン向けにはiOSとAndroidをサポートしており、iOS向けアプリは[Apple Storeで](../Page/Apple_Store.md "wikilink")、Android向けアプリは[Google Play Storeおよび](https://ja.wikipedia.org/wiki/Google_Play_Store "wikilink")[F-Droid](https://ja.wikipedia.org/wiki/F-Droid "wikilink")上でダウンロードできる\[20\]。Jitsi Desktopがサポートする機能には以下のものがある\[21\]。

  - （attendedおよびblind）

<!-- end list -->

  - 自動退席

  - 自動再接続

  - 自動応答と自動転送

  - 通話の録音

  - とを利用した通話の暗号化

  - 会議通話

  - [ICEプロトコルを使用した直接のメディア接続の確立](https://ja.wikipedia.org/wiki/Interactive_Connectivity_Establishment "wikilink")

  - デスクトップ画面のストリーミング

  - マスターパスワードを利用した暗号化パスワードの保存

  - [XMPP](https://ja.wikipedia.org/wiki/XMPP "wikilink")、[AIM](../Page/AOL_Instant_Messenger.md "wikilink")/[ICQ](../Page/ICQ.md "wikilink")、[Windows Live Messenger](../Page/Windows_Live_メッセンジャー.md "wikilink")、[YIMに対するファイル転送](../Page/Yahoo!_Messenger.md "wikilink")

  - （エンド・トゥ・エンドの暗号化）を利用したインスタントメッセージの暗号化

  - [SIPおよび](../Page/Session_Initiation_Protocol.md "wikilink")[XMPP](https://ja.wikipedia.org/wiki/XMPP "wikilink")への[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")のサポート

  - [TURN](https://ja.wikipedia.org/wiki/TURN "wikilink")プロトコルを利用したメディアのリレー

  - （RFC 3842）

  - ビデオエンコーディングに[H.264および](https://ja.wikipedia.org/wiki/H.264/MPEG-4_AVC "wikilink")[H.263](../Page/H.263.md "wikilink")または[VP8](https://ja.wikipedia.org/wiki/VP8 "wikilink")を使用した、[SIPおよび](../Page/Session_Initiation_Protocol.md "wikilink")[XMPPのための音声およびビデオ会話](../Page/Extensible_Messaging_and_Presence_Protocol.md "wikilink")\[22\]

  - 、[G.722](https://ja.wikipedia.org/wiki/G.722 "wikilink")、[Speex](../Page/Speex.md "wikilink")、[Opusを使用した](https://ja.wikipedia.org/wiki/Opus_\(音声圧縮\) "wikilink")\[23\]

  - SIP INFO、[RTP](../Page/Real-time_Transport_Protocol.md "wikilink")（RFC 2833/RFC 4733）、In-bandを使用したのサポート

  - [mDNS](https://ja.wikipedia.org/wiki/:en:Multicast_DNS "wikilink")/[DNS-SDによる](https://ja.wikipedia.org/wiki/:en:DNS-SD "wikilink")[Zeroconf](https://ja.wikipedia.org/wiki/Zeroconf#アップルのプロトコル:_マルチキャストDNS/DNS-SD "wikilink")（[Appleの](../Page/アップル_\(企業\).md "wikilink")[Bonjour](../Page/Bonjour.md "wikilink")を使用）

  - [DNSSEC](https://ja.wikipedia.org/wiki/DNS_Security_Extensions "wikilink")

  - グループビデオ会議のサポート（Jitsi Videobridge）\[24\]

  - SILKおよびOpusコーデックを使用した\[25\]\[26\]

## 関連項目

  -
  -
  -
  -
  -
  - [Wowza Streaming Engine](https://ja.wikipedia.org/wiki/Wowza_Streaming_Engine "wikilink")

  - [Session Initiation Protocol](../Page/Session_Initiation_Protocol.md "wikilink")

## 出典

## 外部リンク

  -
[Category:VoIPのソフトウェア](https://ja.wikipedia.org/wiki/Category:VoIPのソフトウェア "wikilink") [Category:2003年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2003年のソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.
3.
4.   The Kamailio SIP Server Project|website=www.kamailio.org|language=en-US|accessdate=2018-08-04}}
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.  VoIP Review|date=2018-01-28|work=VoIP Review|access-date=2018-07-23|language=en-US}}
15.  Me and my Shadow|website=myshadow.org|language=en|access-date=2018-08-06}}
16.
17.
18.
19.
20.
21. [Jitsi feature list](https://jitsi.org/index.php/Main/Features) with information on supported protocols
22.
23.
24.
25.
26.