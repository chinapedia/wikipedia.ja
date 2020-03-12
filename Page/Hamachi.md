> この記事は[Hamachi](https://ja.wikipedia.org/wiki/Hamachi)から翻訳されています。


**LogMeIn Hamachi**（ハマチ）は、[P2P技術を使用して](https://ja.wikipedia.org/wiki/ピア・ツー・ピア "wikilink")[VPN](https://ja.wikipedia.org/wiki/VPN "wikilink")（仮想プライベートネットワーク）を実現するソフトウェアである。[カナダ](https://ja.wikipedia.org/wiki/カナダ "wikilink")のLogMeIn社が開発し、クライアント数限定版が無料で公開されている。エンドユーザのPCにインストールされるクライアントソフトウェアと、ベンダーであるLogMeIn社によって管理されるサーバクラスタとからなる中央管理型のVPNシステムである。

このソフトは、[NAT](https://ja.wikipedia.org/wiki/NAT "wikilink")機器を利用するホスト同士の間においてもVPN接続を行えることが特徴である。Applied Networking社の仲介サーバでNAT機器のグローバルIPアドレスを交換することで、P2PによるVPN接続を行い、P2P接続が行えない場合は仲介サーバを経由してデータの送受信を行う。

公式サイトで「ゼロコンフィギュレーション（設定不要）」を謳っているとおり、インストールと僅かな設定のみでVPN接続を行うことができる。

Hamachiは 5ピア/ネットワーク、最大64ネットワークまで無料で使用できる。ただしHamachiを無人モードのサービスとして実行する場合は、有料の利用期間パッケージを購入しなければならない\[1\]。

## 概要

### 動作の仕組み

Hamachiをインストールすると、[仮想ネットワークインターフェイス](https://ja.wikipedia.org/wiki/仮想ネットワークインターフェイス "wikilink")が生成される。そのインターフェイスに送信された[IPおよび](../Page/Internet_Protocol.md "wikilink")[IPXパケットは](https://ja.wikipedia.org/wiki/IPX/SPX "wikilink")、実ネットワークの[UDPプロトコルを使用して相手ホストに転送される](../Page/User_Datagram_Protocol.md "wikilink")。これにより、既存の[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")の[ルーティング](../Page/ルーティング.md "wikilink")テーブルを用いてルーティングを行うことができる。

Hamachiを起動すると、まず、クライアントはサーバへの制御用接続を確立し維持する。クライアントとサーバとの間で認証が行われ、その後、他のメンバーとの間でネットワークの状態の同期が行われる。ネットワークのメンバーの参加状態が変化した時、サーバはそのメンバーに対して他のメンバーがトンネルを形成、或いは解除するよう指示する。メンバー間でトンネルを形成する時、サーバの補助を受けて、クライアントは[NAT通過](https://ja.wikipedia.org/wiki/NAT通過 "wikilink")技術を使用する。このNAT通過技術の詳細は公表されていないが、「全体の約95%のケースでうまくP2P接続を成立させる」とベンダーは主張する。このプロセスはNAT機器の特定の組合せでは働かず、NAPT通過が行えない場合、仲介サーバーによってトラフィックを中継する。

### 仮想インターフェース

HamachiクライアントをインストールしたPCの仮想ネットワークインタフェースには、[IPアドレス](../Page/IPアドレス.md "wikilink")が一意に割り当てられる。

割り当てられるアドレスは2012年11月19日以前は、5.0.0.0/8の範囲が使用された。しかし、この範囲は2010年の終わりに[RIPE NCCに割り当てられた](../Page/RIPE_NCC.md "wikilink")。また、この範囲は実際に公のインターネット上で利用され始めている。そのためHamachiは25.0.0.0/8の範囲に切り替えられた\[2\]。

25.0.0.0/8アドレスブロックからのアドレスは、クライアントが初めてシステムにログインするときに割り当てられ、その後はクライアントの公開[暗号鍵と関連付けられる](../Page/公開鍵暗号.md "wikilink")。クライアントがその暗号鍵を保持する限り、この最初に割り当てられたIPアドレスが固有のアドレスとして使用される。

### NATの内側（LAN側）にある2つのホストの接続

LAN側からWAN側に通信が開始される際、NAT機器はWAN側のIPアドレス:ポート番号を一時的にLAN側のIPアドレス:ポート番号に割り当てて双方向に通信を行う（[IPマスカレード](https://ja.wikipedia.org/wiki/IPマスカレード "wikilink")）。そのため、通常はWAN側からLAN側のホストに接続を確立できない。従って、2つのホストが互いに別のNATのLAN側にある場合は、どちらからも接続が確立できないため、直接通信することができない。

Hamachiは下記の方法を用いて、互いに別のNATを利用するホスト同士の直接通信を可能にしている。

NAT機器は、[LAN](https://ja.wikipedia.org/wiki/LAN "wikilink")側のホストから[WAN](https://ja.wikipedia.org/wiki/WAN "wikilink")側のホストへのUDPパケット送信が開始された際、WAN側に返信用の不定なポート番号を一時的に割り当てる。Hamachiが通信を開始する際は、以前に割り当てられたWAN側のポート番号から、次に割り当てられるポート番号をお互いに推測し、2つのホストが同時に推測した相手方のポート番号に向かって[UDPの送信を開始する](../Page/User_Datagram_Protocol.md "wikilink")。送受信が開始された後は、一定間隔で空のパケット（Keep Aliveパケット）を送り続け、タイムアウトにならないようにすることでその後の通信を継続する。

ポート番号の推測は、ほとんどのNAT機器がWAN側の返信用ポート番号を規則的に（たとえば1ずつ増やして）割り振る性質があることを利用している。従って、一部のNAT機器はHamachiを通さない物がある。

### セキュリティ

HamachiはVPN接続を構築するため、他のVPNと同様の危険性を持つ。具体的には、NAT機器や[ファイアウォール](../Page/ファイアウォール.md "wikilink")が迂回される為、リモートマシンのサービスの脆弱性による問題が発生する可能性がある。VPNを利用してLANのようにコンピュータを接続する場合、ファイアウォールなどのセキュリティの設定、管理はしっかりと行うべきである。

また、Hamachiが動作する為には、ベンダーによって運用される「仲介サーバー」が必要である。このサーバーは、ニックネーム、メンテナンスパスワード、静的に割り当てられた5.0.0.0/8 IPアドレス、及び、それらに関連付けられたユーザー認証トークンを保存する。全ての確立したトンネルに対して、サーバはユーザの本来のIPアドレス、確立時刻、継続時間、及び他の相互接続しているユーザーなどの情報を記録している可能性がある。

Hamachiは安全のために業界標準の強固なアルゴリズムを使用してデータを認証し、そのセキュリティアーキテクチャは公開されていると主張している。しかし、Hamachiのソースコードは公開されておらず、不特定多数による再検討は行えない。

Security Now\!podcastで、Steve GibsonはHamachiを「最新の、長い発展ベータ段階から出す準備ができた、超安全、軽量、高性能、非常に洗練された、マルチプラットフォーム、ピアツーピア、そして、自由な\!個人で扱えるVPNシステム」と言い、そして「システムのセキュリティアーキテクチャを完全に入念に検査した」と発言した。

次のエピソードはRandal Schwartzによる質問である。
「Hamachiは[オープンソース](../Page/オープンソース.md "wikilink")ではありません。我々はどうしてそれを信用できますか」「それは私が憂慮させられたものの一つで、私を憂慮させつづけています。私はおそらく最後はOpenVPN上に落ち着くつもりです。」「しかしHamachiは・・・。私はAlex Pankratovがこのシステムを本当に、彼が私に話したその通りに設計したと確信しています。彼はクラシックVPNのセキュリティにおける解決法、IPSecトンネルの実装に接した経験の年月を持ちます。私は、私が行った全面的なソース検査の実施不足については気を晴らせません。・・・それは現実的ではありません。それは確かに本当です。それでも・・・つまり、我々がWindowsを使うとき、我々はBillを信用します」「私はアレックスが私に真実を話したと確信します、しかし、私はその証明を持ちません」

## 脚注

## 関連項目

  - [UDPホールパンチング](../Page/UDPホールパンチング.md "wikilink")
  - [Simple traversal of UDP over NATs](https://ja.wikipedia.org/wiki/Simple_traversal_of_UDP_over_NATs "wikilink")（STUN）
  - [Traversal Using Relay NAT](https://ja.wikipedia.org/wiki/Traversal_Using_Relay_NAT "wikilink")（TURN）
  - [port restricted cone NAT](https://ja.wikipedia.org/wiki/port_restricted_cone_NAT "wikilink")

## 外部リンク

  - [公式サイト](http://www.hamachi.cc/)
  - [vpn.net](http://vpn.net/)
  - [LogMeIn, Inc./Hamachi公式サイト](https://secure.logmein.com/)

[Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink") [Category:P2P](https://ja.wikipedia.org/wiki/Category:P2P "wikilink") [Category:VPN](https://ja.wikipedia.org/wiki/Category:VPN "wikilink")

1.  [LogMeIn Hamachi の購入](https://secure.logmein.com/welcome/hamachi/vpn/pricing.aspx)、[LogMeIn](https://ja.wikipedia.org/wiki/LogMeIn "wikilink")、2014年2月26日閲覧
2.  [Changes to Hamachi on November 19th](http://b.logme.in/2012/11/07/changes-to-hamachi-on-november-19th/)、LogMeIn、2014年2月26日閲覧