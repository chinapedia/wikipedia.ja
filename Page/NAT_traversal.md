> この記事は[NAT traversal](https://ja.wikipedia.org/wiki/NAT_traversal)から翻訳されています。


**NAT traversal**（NATトラバーサル）は、[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")[ネットワークにおいて](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")[NAT機器を用いた上で](../Page/ネットワークアドレス変換.md "wikilink")、複数ホスト間のネットワーク接続を確立する際に生じる問題を解決するために設計されたアルゴリズムである。ちなみに、NAT traversalはNAT通過を意味し、**NAT越え**とも呼ばれる。

例えば、[P2P](https://ja.wikipedia.org/wiki/P2P "wikilink")や[VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink")などのホスト間通信を行うアプリケーションが、相手側のNAT機器を用いたプライベートネットワークに属するホストを直接指定できない、すなわち、NATを通過できないといった問題がある。 通常は、[IPsec](https://ja.wikipedia.org/wiki/IPsec "wikilink")[VPN](https://ja.wikipedia.org/wiki/VPN "wikilink")クライアントがESPパケット\[1\]にNATの通過をさせるためにNAT-Tが用いられる。

NAT traversal技術には多くの種類がある。しかし、NATの機能が標準化されていない為に、全ての場合において動作するNAT traversal技術は存在しない。多くのNAT traversal技術は、グローバルIPアドレスを持つパブリックサーバを必要とする。[TURN](https://ja.wikipedia.org/wiki/TURN "wikilink")などは、サーバがすべてのデータを中継する方法であり、帯域コストを増やし、遅延を増加させることにより、VoIPアプリケーションに弊害をもたらす。一方、[STUN](https://ja.wikipedia.org/wiki/STUN "wikilink")などは、コネクションを確立するときにのみ、サーバを使用する方法である。

NATの振舞いに基づく多くの技術は、端末間の透過性を損ない、企業におけるセキュリティポリシー(Enterprise Security Policies)を保ち難くする。企業のセキュリティ管理者は、セキュリティポリシーを守ることができるように、NATでパケットの検閲を行いながらNAT traversalを可能にするような、NATとファイアウォールの両者が共存する技術を選ぶ。この点から、最も将来性のあるIETFの標準は、[Realm-Specific IP](https://ja.wikipedia.org/wiki/Realm-Specific_IP "wikilink") (RSIP)と[Middlebox](https://ja.wikipedia.org/wiki/Middlebox "wikilink") Communications (MIDCOM)だといえる。[Universal Plug and Play](https://ja.wikipedia.org/wiki/Universal_Plug_and_Play "wikilink") (UPnP)は、小型ゲートウェイの製造業者によって幅広くサポートされているので、家庭や[SOHO](https://ja.wikipedia.org/wiki/SOHO "wikilink")に容易に導入することができる。その一方で、最も古いNAT制御のためのプロトコルである[SOCKS](https://ja.wikipedia.org/wiki/SOCKS "wikilink")は、今も有効であり幅広く利用可能である。

## NAT traversal問題

NAT機器は内部ネットワークから外部ネットワークに向けたリクエストのソースアドレスを変更し、変更後のアドレスに対する応答を受け取る。これにより、内部ネットワークに属する複数のホストが、その数より少ない外部[IPアドレス](../Page/IPアドレス.md "wikilink")を使用して外部ネットワークと通信することを可能にする。しかし、応答は変更後のアドレスに対するものである為に、NAT機器は、応答が内部ネットワークに属するホストのうちのどれに対して行われているものかを特定できない。このため、例えば内部ネットワークに属するホストが外部ネットワークに対して、サーバとして動作することを妨げるという問題が生じる。インターネットを使用する多くのホームユーザは、内部ネットワークに属するホストをサーバとして動作させる必要が無いか、あるいは、静的NATマッピングが使用できる為に、この問題はホームユーザに通常は関係しなかった。しかし例えば、[BitTorrent](https://ja.wikipedia.org/wiki/BitTorrent "wikilink")や[Gnutella](../Page/Gnutella.md "wikilink")などの[P2P](https://ja.wikipedia.org/wiki/P2P "wikilink")によるファイル共有アプリケーションや、[Skype](https://ja.wikipedia.org/wiki/Skype "wikilink")などの[VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink")アプリケーションは、サーバのように動作することをクライアントに要求するが、NAT機器が外部ネットワークから内部ネットワークへのリクエストを適切な内部ホストに関連付けられない為に、このようなアプリケーションの機能に問題が生じる。

## NAT traversalとIPsec

[IPsec](https://ja.wikipedia.org/wiki/IPsec "wikilink")が、[NAT](https://ja.wikipedia.org/wiki/NAT "wikilink")を通過し正常に機能するためには、以下が[ファイアウォール](../Page/ファイアウォール.md "wikilink")上で許可される必要がある。

  - Internet Key Exchange (IKE) - User Datagram Protocol (UDP) ポート500
  - Encapsulating Security Payload (ESP) - Internet Protocol (IP) 50
  - IPsec NAT-T - UDP ポート4500

多くの家庭用ルータでは、IPsecパススルーを有効とすることによりこれらが実現される。

議論の余地のあるセキュリティ問題のために、Windows XP SP2 は、初期設定ではNAT-Tを無効とするよう変更された。 このため、家庭でPCを使用するほとんどのユーザは、PC環境の設定変更を行わない限り、IPsecを使用することができない。 NATを使用したシステム同士が通信を行うためにNAT-Tを有効とするには、以下のレジストリキーを追加し、値AssumeUDPEncapsulationContextOnSendRuleを2に設定する必要がある\[2\]。

  - HKEY_LOCAL_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\IPsec (Windows XP)
  - HKEY_LOCAL_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\PolicyAgent (Windows Vista以降)

IPsec NAT-Tパッチは、Windows 2000、Windows NT、Windows 98でも利用できる。

NAT-TとIPsecとの使用は、システム間で[日和見暗号化](https://ja.wikipedia.org/wiki/日和見暗号化 "wikilink")([:en:Opportunistic encryption](https://ja.wikipedia.org/wiki/:en:Opportunistic_encryption "wikilink"))を可能とする。それにより、NATの内側にあるシステムが随時安全な接続を要求し確立することを、NAT-Tは可能にする。

ローカルIPアドレスを払い出すNAT実装装置がパススルー可能なIPsecの本数はそのNAT実装装置が持つグローバルIPアドレスの数と同数である(例えばグローバルIPアドレスを一つしかもたない家庭用ブロードバンドルータは一つのIPsecしかパススルーできない)。これはローカルIPアドレス用のヘッダ自体がIPsecで暗号化されるためである。

## 関連項目

### NAT traversalに関連するプロトコル、及びそれに基づく技術

  - [Simple Traversal of UDP over NATs](https://ja.wikipedia.org/wiki/STUN "wikilink") (STUN)
  - [Traversal Using Relay NAT](https://ja.wikipedia.org/wiki/Traversal_Using_Relay_NAT "wikilink") (TURN)
  - [NAT-T](https://ja.wikipedia.org/wiki/NAT-T "wikilink") Negotiation of NAT-Traversal in the IKE
  - [Teredo トンネリング](https://ja.wikipedia.org/wiki/Teredo_トンネリング "wikilink") - [IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")接続の提供のためにNATトラバーサル技術を使用する。
  - [Session Border Controller](https://ja.wikipedia.org/wiki/Session_Border_Controller "wikilink") (SBC)

### NATの動作に基づくNAT traversalの技術

  - [Realm-Specific IP](https://ja.wikipedia.org/wiki/Realm-Specific_IP "wikilink") (RSIP)
  - [Middlebox](https://ja.wikipedia.org/wiki/Middlebox "wikilink") Communications (MIDCOM)
  - [SOCKS](https://ja.wikipedia.org/wiki/SOCKS "wikilink")
  - [NAT Port Mapping Protocol](https://ja.wikipedia.org/wiki/NAT_Port_Mapping_Protocol "wikilink") (NAT PMP)
  - [Universal Plug and Play](https://ja.wikipedia.org/wiki/Universal_Plug_and_Play "wikilink") (UPnP)
  - [Application Layer Gateway](https://ja.wikipedia.org/wiki/Application_Layer_Gateway "wikilink") (ALG)
  - [UDPホールパンチング](https://ja.wikipedia.org/wiki/UDPホールパンチング "wikilink")

### 複数の技術を含むNAT traversalの技術

  - [Interactive Connectivity Establishment](https://ja.wikipedia.org/wiki/Interactive_Connectivity_Establishment "wikilink") (ICE)

## 外部リンク

  - [Cornell University - Characterization and Measurement of TCP Traversal through NATs and Firewalls](http://nutss.gforge.cis.cornell.edu/pub/imc05-tcpnat/)
  - [Columbia University - An Analysis of the Skype Peer-to-Peer Internet Telephony](http://www1.cs.columbia.edu/~library/TR-repository/reports/reports-2004/cucs-039-04.pdf)
  - [Peer to peer communication across Network Address Translators (UDP Hole Punching):](http://www.brynosaurus.com/pub/net/p2pnat/)
  - [NAT-Traversal Test](http://gex.cs.uni-tuebingen.de)
  - [zConf.com](http://66.147.227.218/Zconf/4.html) - Understanding NAT Traversal

## 関連 RFC

  - RFC 1579 - Firewall Friendly FTP
  - RFC 2663 - IP Network Address Translator (NAT) Terminology and Considerations
  - RFC 2709 - Security Model with Tunnel-mode IPsec for NAT Domains
  - RFC 2993 - Architectural Implications of NAT
  - RFC 3027 - Protocol Complications with the IP Network Address Translator (NAT)
  - RFC 3235 - Network Address Translator (NAT)-Friendly Application Design Guidelines
  - RFC 3947 - Negotiation of NAT-Traversal in the IKE
  - RFC 5128 - State of Peer-to-Peer (P2P) Communication across Network Address Translators (NATs)

[Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:ネットワークアドレス変換](https://ja.wikipedia.org/wiki/Category:ネットワークアドレス変換 "wikilink")

1.  Encapsulating Security Payload - ペイロードを暗号化してカプセル化
2.