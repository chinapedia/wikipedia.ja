> この記事は[Layer 2 Tunneling Protocol](https://ja.wikipedia.org/wiki/Layer_2_Tunneling_Protocol)から翻訳されています。


**Layer 2 Tunneling Protocol** (**L2TP**) とは、[コンピュータネットワーク](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")において [Virtual Private Network](../Page/Virtual_Private_Network.md "wikilink") (VPN)をサポートするために用いられる[トンネリング](https://ja.wikipedia.org/wiki/トンネリング "wikilink")[プロトコル](../Page/プロトコル.md "wikilink")である。

## 概要

L2TP自体は[暗号](../Page/暗号.md "wikilink")化や秘匿性は提供しないため、[IPsec](https://ja.wikipedia.org/wiki/IPsec "wikilink")と併用されることが多い。プライバシー提供に関しては、L2TPはそのトンネル内部を通過する暗号化プロトコルに委ねる\[1\]。

L2TPは[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")の第2層[データリンク層](https://ja.wikipedia.org/wiki/データリンク層 "wikilink")のプロトコルである。 [UDPの](../Page/User_Datagram_Protocol.md "wikilink")1701番ポート\[2\]を用いる。

ペイロードとL2TPヘッダを含めたL2TPパケット全体は、UDP[データグラム](https://ja.wikipedia.org/wiki/データグラム "wikilink")として送られる。L2TPトンネル内にはPPPセッションを伝送することが一般的である。L2TPは秘密性や強力な認証をそれ自身では提供しない。IPsecが秘密性や認証、整合性を提供することによって、L2TPパケットを守るためによく用いられる。これら2つのプロトコルの組み合わせは、一般に*L2TP/IPsec*（後述）として知られている。

L2TPトンネルの両端は*LAC* (L2TP Access Concentrator)と*LNS* (L2TP Network Server)と呼ばれている。LACはLNSとの間のトンネルのイニシエーターであり、LNSは新しいトンネルの開始を待つ[サーバ](../Page/サーバ.md "wikilink")である。一度トンネルが確立されると、ピア間のネットワークトラフィックは、双方向性となる。さまざまの上位プロトコルがL2TPトンネル上を通過したときこのトンネルが通信に有用になる。これを容易にするため、*L2TP セッション*（または*call*）は、トンネル内で、PPPなどのそれぞれの上位プロトコルに対して確立される。LAC、LNSどちらからでもセッションを開始してよい。それぞれのセッションのトラフィックは、L2TPによって隔離され、1つのトンネルを利用して複数の仮想ネットワークを立ち上げる事が可能である。L2TPを実装するとき、[MTUを考慮しなければならない](../Page/Maximum_Transmission_Unit.md "wikilink")。

L2TPトンネル内において交換される[パケット](../Page/パケット.md "wikilink")はコントロールパケットとデータパケットに分類される。L2TPはコントロールパケットに信頼性を提供する。しかし、データパケットには信頼性は提供されない。もし信頼性を求めるなら、L2TPトンネルのそれぞれのセッションの中で動作するネストされたプロトコルによって提供される。

## 歴史

RFC 2661 が標準化候補の提案として[1999年](../Page/1999年.md "wikilink")に発表された。L2TPは元来、[PPPの為の](../Page/Point-to-Point_Protocol.md "wikilink")2つのトンネルプロトコル（[Ciscoの](https://ja.wikipedia.org/wiki/シスコシステムズ "wikilink")[L2F](https://ja.wikipedia.org/wiki/L2F "wikilink")と[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[PPTP](https://ja.wikipedia.org/wiki/Point_to_Point_Tunneling_Protocol "wikilink")）に起源を持つ。

このプロトコルの新しいバージョンであるL2TPv3は、RFC 3931が標準化候補の提案として[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")に発表された。L2TPv3は、さまざまなセキュリティ機能の付加、カプセル化の改善、単に[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")上のPPP以外の様々なデータリンク層プロトコル（[フレームリレー](https://ja.wikipedia.org/wiki/フレームリレー "wikilink")、[イーサネット](../Page/イーサネット.md "wikilink")、[ATMなど](../Page/Asynchronous_Transfer_Mode.md "wikilink")) を運ぶ能力を提供する。

## トンネリングモデル

L2TPトンネルは、PPPセッション全体にわたったり、2セグメントセッションの片方のセグメントのみにわたって張ることが出来る。 これは4つの異なるトンネリングモードによって表すことが出来る。つまり、

1.  任意トンネル
2.  必須トンネル - 着信呼
3.  必須トンネル - 発信呼
4.  L2TPマルチホップコネクション

任意トンネルモードでは、トンネルはユーザによってつくられ、一般的なL2TPの使用はLACクライアントと呼ばれるクライントを有効にする。ユーザはL2TPパケットを、LNSへ転送する[インターネットサービスプロバイダ](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink") (ISP)に送る。ISPはL2TPをサポートしている必要は無く、ただL2TPパケットをLACとLNSの間で転送できれば良い。LACクライアントは、事実上リモートクライアントと同様に同じシステム上に存在するL2TPトンネルのイニシエーターの働きをする。L2TPトンネルは、L2TPクライアントからLNSまでのPPPセッション全体に及ぶ。

必須トンネルモデルの着信呼では、トンネルはISPのLACとLNS[ホームゲートウェイ](https://ja.wikipedia.org/wiki/ホームゲートウェイ "wikilink")の間で作られる。企業はVPNを用いるリモートユーザに、会社のサーバにアクセスできるアカウントにログイン出来るようにする事ができる。結果的に、ユーザはPPPパケットを、ISP (LAC)でL2TPにカプセル化をしてトンネルでLNSに送る。必須トンネリングの場合、ISPはL2TPを受容できなければならない。このモデルではトンネルはISPとLNSの間のPPPセッションのセグメントのみで張られる。

必須トンネルモデルの着信呼では、ホームゲートウェイ (LNS)はISP (LAC)へトンネルを開始し（呼び出し発信）、PPPが有効になったリモートユーザであるクライアントにローカル呼び出しをするように、ISPへ指示する。このモデルはリモートPPP応答クライアントがISPと不変な既定の電話番号を持つケースの為に意図されたものである。このモデルは、インターネット上に存在する既定の会社が、ダイヤルアップ接続を必要とするリモートオフィスとコネクションを確立することを必要とするときに使われると期待されていた。

このモデルにおいて、トンネルはLSNとISPとの間のPPPセッションのセグメント間に渡ってのみ張られる。

L2TPマルチホップコネクションは、クライアントの代わりにLACやLNSがL2TPトラフィックをリダイレクトする方法である。マルチホップコネクションはL2TPマルチホップゲートウェイを用いて設立される。トンネルは、クライアントであるLACからL2TPマルチホップゲートウェイと、さらにL2TPマルチホップゲートウェイと相手方LNSとの間で設置されるもう一つのトンネルによって確立される。クライアントであるLACとLNSの間のL2TPトラフィックはゲートウェイを通過して相互にリダイレクトされる。

## L2TP/IPsec

L2TPの元々の機密性の欠如から、しばしばIPsecと一緒に実装される。これは*L2TP/IPsec*と呼ばれ、RFC 3193 によって標準化されている。L2TP/IPsec VPNを構築するための手順は以下の通りである。

一般的に、[IKE](https://ja.wikipedia.org/wiki/IPsec#IKE "wikilink") (Internet Key Exchange)を通してIPsecの[SA](https://ja.wikipedia.org/wiki/Security_Association "wikilink") (Security Association)を折衝する。これはUDPの500番ポート\[3\]で行われ、通常、共有の[パスワード](https://ja.wikipedia.org/wiki/パスワード "wikilink")（事前共有鍵、PSK）や[公開鍵](../Page/公開鍵暗号.md "wikilink")、[X.509](https://ja.wikipedia.org/wiki/X.509 "wikilink")証明書を両端で用いる。しかし他の鍵方式も存在する。 トランスポートモードの[ESP](https://ja.wikipedia.org/wiki/IPsec#ESP "wikilink") (Encapsulation Security Payload)通信の確立。ESPのIP[プロトコル番号](https://ja.wikipedia.org/wiki/プロトコル番号 "wikilink")は50である\[4\]。この時点で、安全なチャネルは確立できたがトンネリングは行われてはいない。 SAのエンドポイント間のL2TPトンネルのネゴシエーションと確立。パラメータの実際のネゴシエーションは上記のSAの安全なチャネルの上で、IPsec暗号化の下に行われる。L2TPはUDPの1701番ポート\[5\]を利用する。

プロセスが完了すれば、エンドポイント間のL2TPパケットはIPsecによって[カプセル化される](https://ja.wikipedia.org/wiki/カプセル化_\(通信\) "wikilink")。L2TPパケット自体はIPsecパケットの内側に包まれ隠されているので、内側のプライベートネットワークについての情報は暗号化されたパケットから得る事は不可能である。 さらに、両方のエンドポイント間にある[ファイアウォール](../Page/ファイアウォール.md "wikilink")のUDPの1701番ポート\[6\]を開ける必要はない。なぜなら、トンネル内部のパケットはIPsecデータが復号されトンネルから取り出されるまで処理されず、エンドポイントでのみ処理されるからである。

L2TP/IPsecにおける混同の可能性がある点は「トンネル」と「セキュアトンネル」という用語である。トンネルは一方のネットワークの手付かずのパケットを他方のネットワークに運ぶことを可能にするチャネルのことを言う。L2TP/IPsecの場合は、L2TP/PPPパケットがIP上で転送されることを可能とする。セキュアトンネルとは全てのデータの機密性が保証された接続のことを指す。L2TP/IPsecにおいては、最初にIPsecがセキュアトンネルを提供し、次にL2TPがトンネルを提供する。

## Windowsにおける実装

[Windows Vista以前のバージョンではL](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")2TPなしのIPsecの設定が非常に難しかった。マイクロソフトはIPsec VPN接続の設定を、[Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink")/[XP](../Page/Microsoft_Windows_XP.md "wikilink") ではマウスをクリックする回数を100回以上からVistaでは15回にまで容易にした。XPと比較してVistaでは、「VPNとは何か？」のように一般的でとても基礎的な情報ではあるが、少しだけ多いヘルプ情報もある。そのヘルプ情報では、L2TPなしのIPsecはモバイルリモートアクセスには不向きであるとされている。ヘルプ情報は、この用途にはL2TP/IPsecまたはPPTPを使用するように勧めている。

Windows VistaはL2TPを使用しないIPsecをより簡単に作成することを目的とする2つの新しい設定機能を提供する。 両方の説明を以下のセクションに述べた。

  - Windows Firewall with Advanced Security (WFwAS)と呼ばれる[MMCスナップインで](https://ja.wikipedia.org/wiki/Microsoft_管理コンソール "wikilink")、コントロールパネル＞管理ツールの中にある。
  - netsh advfirewall コマンドラインツール

これらの設定ユーティリティには問題がない訳ではなく、また不運にも、netsh advfirewallについてもWFwASのIPsecクライアントについても資料はほとんどない。上記の問題のひとつに[NATに対応しない点がある](../Page/ネットワークアドレス変換.md "wikilink")。もう一つの問題は、新しいVistaの設定ユーティリティにおいて、サーバが[IPアドレス](../Page/IPアドレス.md "wikilink")によって一意に明確でなければならない。サーバの[ホスト名](../Page/ホスト名.md "wikilink")は使われていては困り、そのため、もしIPsecサーバのIPアドレスが変わるなら、すべてのクライアントはこの新しいIPアドレスを知らされなければならない。([:en:DynDNS](https://ja.wikipedia.org/wiki/:en:DynDNS "wikilink")の様なユーティリティによるアドレスもまた、サーバを除外する)

## ADSLネットワークにおけるL2TP

L2TPは、しばしば[ADSL](../Page/ADSL.md "wikilink")終端接続性を転売するためのトンネリング手法として用いられる。L2TPトンネルはユーザと回線を提供されたISPの間に存在する。そのため、回線を提供している側のISPが伝送しているようには見えない。

## ケーブルネットワークにおけるL2TP

L2TPはケーブルプロバイダ（例えば[イスラエル](../Page/イスラエル.md "wikilink")のHOT）によって、終端接続性販売のためのトンネリング手法として用いられている。このL2TPトンネルはユーザとインターネット接続性を販売するISPとの間にある。そしてADSL同様に、接続性を販売した側のケーブルプロバイダが伝送しているようには見えない。

## 関連項目

  - [IPsec](https://ja.wikipedia.org/wiki/IPsec "wikilink")
  - [L2F](https://ja.wikipedia.org/wiki/L2F "wikilink") - Layer 2 Forwarding Protocol
  - [Point to Point Tunneling Protocol](https://ja.wikipedia.org/wiki/Point_to_Point_Tunneling_Protocol "wikilink") (PPTP) - PPPトンネリングプロトコル
  - [Point-to-Point Protocol](../Page/Point-to-Point_Protocol.md "wikilink")
  - [IEEE 802.1aq](https://ja.wikipedia.org/wiki/IEEE_802.1aq "wikilink") - Shortest Path Bridging
  - RFC 2661 - Layer Two Tunneling Protocol "L2TP"

## 脚注

## 外部リンク

  - RFC 2341 *Cisco Layer Two Forwarding (Protocol) "L2F"* (a predecessor to L2TP)
  - RFC 2637 *Point-to-Point Tunneling Protocol (PPTP)* (a predecessor to L2TP)
  - RFC 2661 *Layer Two Tunneling Protocol "L2TP"*
  - RFC 2809 *Implementation of L2TP Compulsory Tunneling via RADIUS*
  - RFC 2888 *Secure Remote Access with L2TP*
  - RFC 3070 *Layer Two Tunneling Protocol (L2TP) over Frame Relay*
  - RFC 3145 *L2TP Disconnect Cause Information*
  - RFC 3193 *Securing L2TP using IPsec*
  - RFC 3301 *Layer Two Tunnelling Protocol (L2TP): ATM access network*
  - RFC 3308 *Layer Two Tunneling Protocol (L2TP) Differentiated Services*
  - RFC 3355 *Layer Two Tunnelling Protocol (L2TP) Over ATM Adaptation Layer 5 (AAL5)*
  - RFC 3371 *Layer Two Tunneling Protocol "L2TP" Management Information Base*
  - RFC 3437 *Layer Two Tunneling Protocol Extensions for PPP Link Control Protocol Negotiation*
  - RFC 3438 *Layer Two Tunneling Protocol (L2TP) Internet Assigned Numbers: Internet Assigned Numbers Authority (IANA) Considerations Update*
  - RFC 3573 *Signaling of Modem-On-Hold status in Layer 2 Tunneling Protocol (L2TP)*
  - RFC 3817 *Layer 2 Tunneling Protocol (L2TP) Active Discovery Relay for PPP over Ethernet (PPPoE)*
  - RFC 3931 *Layer Two Tunneling Protocol - Version 3 (L2TPv3)*
  - RFC 4045 *Extensions to Support Efficient Carrying of Multicast Traffic in Layer-2 Tunneling Protocol (L2TP)*
  - RFC 4951 *Fail Over Extensions for Layer 2 Tunneling Protocol (L2TP) "failover"*

[Category:トンネリング](https://ja.wikipedia.org/wiki/Category:トンネリング "wikilink") [Category:リンク層プロトコル](https://ja.wikipedia.org/wiki/Category:リンク層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:VPN](https://ja.wikipedia.org/wiki/Category:VPN "wikilink")

1.  IETF (1999), RFC 2661
2.  [Service Name and Transport Protocol Port Number Registry](http://www.iana.org/assignments/service-names-port-numbers/)
3.
4.  [Protocol Numbers](http://www.iana.org/assignments/protocol-numbers/)
5.
6.