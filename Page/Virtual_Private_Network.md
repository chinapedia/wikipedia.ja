> この記事は[Virtual Private Network](https://ja.wikipedia.org/wiki/Virtual_Private_Network)から翻訳されています。


[Virtual_Private_Network_overview.svg](https://ja.wikipedia.org/wiki/File:Virtual_Private_Network_overview.svg "fig:Virtual_Private_Network_overview.svg") **Virtual Private Network**（バーチャル プライベート ネットワーク、**VPN**）は、[インターネット](../Page/インターネット.md "wikilink")（本来は公衆網である）に跨って、[プライベートネットワーク](https://ja.wikipedia.org/wiki/プライベートネットワーク "wikilink")を拡張する技術、およびそのネットワークである。VPNによって、[イントラネット](../Page/イントラネット.md "wikilink")などのプライベートネットワークが、本来公的なネットワークであるインターネットに跨って、まるで各プライベートネットワーク間が[専用線](../Page/専用線.md "wikilink")で接続されているかのような、機能的、セキュリティ的、管理上のポリシーの恩恵などが、管理者や利用者に対し実現される。

仮想プライベートネットワーク、仮想専用線とも呼ばれる。

VPNは2つの拠点間に、仮想的に「直接的な接続」を構築することで実現できる。専用線ではなくインターネットを経由しながら機密性を保つため、IPベースの通信の上に、専用の接続方法や[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")を乗せている。また、近年はインターネットではなく少し広がりの小さい多数の加入者で帯域共用する閉域網を利用し、そのような接続を実現する技術、もしくは[電気通信事業者](../Page/電気通信事業者.md "wikilink")のサービスもVPNと呼ばれている。後者を指して特にPPVPN（Provider Provisioned Virtual Private Networks）と呼ぶこともある。

## 概要

VPNは、インターネットや多人数が利用する閉域網を介して、暗号化やトラフィック制御技術により、プライベートネットワーク間が、あたかも専用線接続されているかのような\[1\]状況を実現するものである。

一言でVPNと言っても、様々なプロトコルが利用されるため、そのオプションによって様々な利用が可能である。VPN=暗号化技術という誤解が多いが、それは利用するプロトコルやオプションによって異なる。VPNで利用されるプロトコルには、[SSH](../Page/Secure_Shell.md "wikilink")/[TLS](../Page/Transport_Layer_Security.md "wikilink")（SSL）/[IPsec](../Page/IPsec.md "wikilink")/[PPTP](https://ja.wikipedia.org/wiki/Point_to_Point_Tunneling_Protocol "wikilink")/[L2TP](../Page/Layer_2_Tunneling_Protocol.md "wikilink")/[L2F](https://ja.wikipedia.org/wiki/L2F "wikilink")/[MPLSなどがある](../Page/Multi-Protocol_Label_Switching.md "wikilink")。

またもともとは、グローバルなインターネット（the Internet）を介するものであったが、近年の電気通信インフラの形態の傾向などから、[IP網](https://ja.wikipedia.org/wiki/IP網 "wikilink")（特に[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")網のことが多い）ではあるが、[通信キャリア](https://ja.wikipedia.org/wiki/通信キャリア "wikilink")の閉域網内から外に出ないで実現されているVPNも運用されるようになってきている。

またトンネリングの形態として、IPパケットを融通する、いわゆる「レイヤ3」で実現する方法と、[イーサネット](../Page/イーサネット.md "wikilink")の[フレーム等を融通する](https://ja.wikipedia.org/wiki/フレーム_\(ネットワーク\) "wikilink")、いわゆる「レイヤ2」で実現する方法がある。またそれぞれで、接続の両端点となっている両拠点のそれぞれのノードが「同一のノードに見える」のか、別のノードになるのか、といった違いがある。

レイヤ3かレイヤ2かの違いは、それぞれで可能なことと不可能なことがあり、運用上の要件などから、どちらを採用するか決定する。

## 種類

### インターネットVPN

IPsecやPPTP、[SoftEther](../Page/SoftEther.md "wikilink")などを利用することで、インターネットを介した複数の拠点間で[暗号](../Page/暗号.md "wikilink")化データを[カプセリング・トンネリングし通信を行い](../Page/トンネリング.md "wikilink")、通信データの改竄・窃用\[2\]を抑えながら通信を行うことが可能となる。

インターネットVPNには、拠点の[LAN同士が接続する](../Page/Local_Area_Network.md "wikilink")「**LAN型VPN**（サイト間VPN、site-to-site VPNとも）」と、[ノートPCや](../Page/ノートパソコン.md "wikilink")[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")などにインストールしたVPNクライアントソフトを利用し、拠点のLANに接続する「**リモートアクセス型VPN**」がある。

また、TLSを利用した**[SSL-VPN](../Page/SSL-VPN.md "wikilink")**も、その手軽さから注目されている。

インターネットVPNは、IP-VPNと比較すると以下のようなメリット・デメリットがある。

  - メリット
      - アクセス回線にインターネットを利用することから生じるメリット
          - 通信回線のコストを抑えることが可能。インターネット接続さえあればVPNを終端できる装置やソフトウェアを導入することで、[インターネットサービスプロバイダ](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink") (ISP)など電気通信事業者から提供される閉域網を介さず、自前でVPN網を構築することも可能である。
          - リモート型VPNの場合、出先からでも[ダイヤルアップ接続](../Page/ダイヤルアップ接続.md "wikilink")や[公衆無線LAN](../Page/公衆無線LAN.md "wikilink")など何らかの形でインターネットへのアクセスが可能であれば、拠点のLANへアクセスすることが可能となる。
  - デメリット
      - [クライアントのアクセス数の増減で機器のパフォーマンスが求められるため](../Page/クライアント_\(コンピュータ\).md "wikilink")、利用スケールにあわせた機器の選択が重要である。
      - 実効通信速度や安定性は、利用しているインターネット網に依存するため場合によっては不安定となる。
      - 暗号化を施しているとは言え、グローバルなインターネット経由である為、SSLなどの暗号の強度を除いて通信の安全性を担保するものがない。

また完全にオープンなインターネットではなく、特定ISPのインターネット網上のみで通信が完結するタイプのインターネットVPNもISPからサービスとして提供されている。

### 専用の閉域網によるVPN

企業などの信頼性の要求される通信網を構築するには、拠点間に帯域保証の専用通信回線を占有してきたが、これを第三者が侵入・傍聴・改竄しにくくする技術により帯域共有型の安価な閉域網で実現しようというものがこのタイプのVPNと言える。

#### IP-VPN

[MPLS対応のルータなどを使用し](../Page/Multi-Protocol_Label_Switching.md "wikilink")、インターネットとは別に構成された[IP網](https://ja.wikipedia.org/wiki/IP網 "wikilink")で、VPNを構成する通信事業者のVPNサービスはIP-VPNと呼ばれることが多い。IP上に構築される専用線網であるが、従来の専用線に比べ低コストでの利用が可能である。ISPの閉域網（=外部公開されていない通信網）を利用することでの安全性は確保されるが、その信頼度はサービス提供者に委ねる形となるため、ラベル技術や暗号化技術でセキュリティを確保する形での専用線利用となる。

通信経路は網内で他のユーザと共有している為[ベストエフォート](../Page/ベストエフォート.md "wikilink")の傾向にあり、データの通信速度を厳密に保証しかねるがインターネットVPNのような極端な通信速度の低下はほとんど無いと言える。また、オプションで帯域保証を提供しているISPもある。

VPNに関しての機器の導入・管理をユーザ側で行う必要が無いため、導入や運用保守が容易な点も、IP-VPNの特徴の一つである。利用する際は、[BGP対応の](../Page/Border_Gateway_Protocol.md "wikilink")[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")が推奨されるが、インターフェースさえ合わせればユーザの好みでルータを選択できる。

#### 専用通信回線との違い

専用線（専用通信回線）は導入コスト及びランニングコストが高価であるが、接続性及び帯域が[SLAによって保証されており](https://ja.wikipedia.org/wiki/Service_Level_Agreement "wikilink")、安定性を考えると専用線を選択する企業も多い。専用線ではアクセス回線に合わせ、ルータのインターフェースを選択するだけで対向間の接続が可能であるが、インターネットVPNの場合は、VPN対応のルータ及び専用機、専用クライアントソフトが必要である。

管理や運用保守に関してはVPNが不利であるが、回線コスト（ランニングコスト）や自由度でVPNが圧倒的に勝っているため、現在専用線からの移行（リプレース）が多く行われている。

### レイヤ2 VPN

[広域イーサネット](../Page/広域イーサネット.md "wikilink")は[イーサネット](../Page/イーサネット.md "wikilink")（レイヤ2）通信が提供されており、利用するプロトコルがIPに依存しないため、LANと同じ感覚で利用可能である。

これと比較して、レイヤ3パケットのトンネリング通信のみをサポートするVPN技術（IPsecやGRE等）を用いたVPNの場合は、あらかじめ利用するサービスやプロトコルを考慮しながらネットワークの構築が行われ、構築後のサービスやプロトコルの変更では、VPN機器の変更が必要となる。

レイヤ2（イーサネット）パケットのトンネリング通信や[ブリッジ接続](../Page/ブリッジ接続.md "wikilink")などをサポートしているVPN技術を用いることにより、前述した広域イーサネットのメリットと同等のことを実現でき、インターネットVPNを用いて安価に構築することができる。

特に、[仮想LANカード](../Page/仮想LANカード.md "wikilink")と[仮想HUB](https://ja.wikipedia.org/wiki/仮想HUB "wikilink")および既存の物理的なLANをVPNプロトコルで接続し、その上で[ブリッジ接続](../Page/ブリッジ接続.md "wikilink")する手法により、広域イーサネットと同様に、既存の[スイッチングハブ](../Page/スイッチングハブ.md "wikilink")や[レイヤ3スイッチ](../Page/レイヤ3スイッチ.md "wikilink")が使用されているLAN同士をVPN接続することができる。遠隔地の拠点間で[VoIP](../Page/VoIP.md "wikilink")や[テレビ会議システムなどを利用する場合も](../Page/ビデオ会議.md "wikilink")、同一のイーサネットセグメント上にある機器とみなすことができるので、より容易・確実に利用可能となるメリットがある。

さらに、LANに対してイーサネットのレイヤでリモートアクセスすることが可能になる。

## モード

### トランスポートモード

トランスポートモードでは[データの暗号化を](https://ja.wikipedia.org/wiki/ペイロード_\(コンピュータ\) "wikilink")、クライアントが直接行う。すべての通信でデータは暗号化されているが、[IPヘッダ](https://ja.wikipedia.org/wiki/IPヘッダ "wikilink")の暗号化は行われない。

すべてのクライアントにVPNソフトウェアをインストールする必要があるが、モバイル端末からのアクセスなどには利用しやすい。

### トンネルモード

トンネルモードでは、暗号化処理を専用の[ゲートウェイ](https://ja.wikipedia.org/wiki/ゲートウェイ "wikilink")（VPNゲートウェイ）で行う。クライアントは、暗号化されていないデータに受信クライアントあてのIPヘッダを付与し、VPNゲートウェイへ送信する。VPNゲートウェイ間の通信では、データ及び受信クライアントあてのIPヘッダはカプセル化され、受信側VPNゲートウェイへのIPヘッダを付与して通信するため、拠点間通信でのIPヘッダの安全性を確保することができる。

拠点間通信でのみ利用可能となり、また、ローカルネットワーク内の通信は暗号化されない。

## 経路制御

トンネリング・プロトコルは[PPP](../Page/Point-to-Point_Protocol.md "wikilink")[トポロジーに使用される](https://ja.wikipedia.org/wiki/ネットワーク構成 "wikilink")。このトポロジーは一般にVPNと考えられてはいない。なぜなら、VPNはネットワークノードの任意なそして変化する集合をサポートすることが期待されているからである。ほとんどのルーターの実装がソフトウェアで定義されたトンネル・インターフェイスをサポートするので、顧客によって構築されたVPNは多くの場合単なるトンネルの集合によって構成され、従来の[ルーティングプロトコル](https://ja.wikipedia.org/wiki/ルーティングプロトコル "wikilink")はこれらのトンネルを通って走ることとなる。[PPVPN](https://ja.wikipedia.org/wiki/PPVPN "wikilink")はしかしながら複数のVPNの共存をサポートする必要がある。これらのVPNは同じ[サービスプロバイダー](https://ja.wikipedia.org/wiki/サービスプロバイダー "wikilink")によって運用されるが、お互いから隔離されている。

## 管理権限の立場的な関係

[IETFが分類するVPNは様々なものがあるが](../Page/Internet_Engineering_Task_Force.md "wikilink")、中には[VLANのように](../Page/Virtual_Local_Area_Network.md "wikilink")、例えば[IEEE 802委員会](../Page/IEEE_802.md "wikilink")、すなわちワークグループ802.1（アーキテクチャ）といった他の機構の標準化責任のものもある。当初は、Telecommunication Service Provider（TSP）が提供しているWANリンクが単一企業内のネットワークノード同士を相互に接続していた。LANの出現と同時に、企業が認めた連絡線を用いたネットワークノード同士が相互接続できるようになった。初期のWANは[専用線](../Page/専用線.md "wikilink")や[フレームリレー](../Page/フレームリレー.md "wikilink")といったレイヤー2多重化サービス、[ARPANET](../Page/ARPANET.md "wikilink")、[インターネット](../Page/インターネット.md "wikilink")などのIPベースの第3層ネットワーク\[3\]、軍事IPネットワーク（[NIPRNet](https://ja.wikipedia.org/wiki/NIPRNet "wikilink")、[SIPRNet](https://ja.wikipedia.org/wiki/SIPRNet "wikilink")、[JWICS](https://ja.wikipedia.org/wiki/JWICS "wikilink") 他）を利用しているうちに一般的な相互接続メディアとなった。VPNは[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")上で定義され始めた。ノード間を相互接続するためには、管理の技術よりむしろ関係に基づいて様々なVPNを真っ先に見分けることが有用であった。いったん関係が定義されれば、違った技術がセキュリティやサービスの質といった要求に応じて用いられることがあった。

## VPNで利用される技術・手法

  - [IPsec](../Page/IPsec.md "wikilink")
  - [SSL-VPN](../Page/SSL-VPN.md "wikilink")
  - [仮想HUB](https://ja.wikipedia.org/wiki/仮想HUB "wikilink")
  - [仮想LANカード](../Page/仮想LANカード.md "wikilink")
  - [ブリッジ接続](../Page/ブリッジ接続.md "wikilink")

### レイヤ2 VPN技術

  - [Point to Point Tunneling Protocol](https://ja.wikipedia.org/wiki/Point_to_Point_Tunneling_Protocol "wikilink")（PPTP）
  - [Layer 2 Tunneling Protocol](../Page/Layer_2_Tunneling_Protocol.md "wikilink")（L2TP）
  - [OpenVPN](../Page/OpenVPN.md "wikilink")（レイヤ3 IPルーティングも可能）
  - [PacketiX VPN](../Page/PacketiX_VPN.md "wikilink")（レイヤ3 IPルーティングも可能）
  - [SoftEther](../Page/SoftEther.md "wikilink")（レイヤ3 IPルーティングも可能）
  - [TinyVPN](https://ja.wikipedia.org/wiki/TinyVPN "wikilink")

### レイヤ3 VPN技術

  - [Hamachi](../Page/Hamachi.md "wikilink")
  - [IPsec](../Page/IPsec.md "wikilink")
  - [WireGuard](../Page/WireGuard.md "wikilink")

### レイヤ4以上のVPN技術

  - [SSH](../Page/Secure_Shell.md "wikilink")

## 脚注

## 参考文献

  -
## 関連項目

  - [専用線](../Page/専用線.md "wikilink")
  - [広域イーサネット](../Page/広域イーサネット.md "wikilink")
  - [中国のネット検閲](../Page/中国のネット検閲.md "wikilink") - [グレート・ファイアウォール](https://ja.wikipedia.org/wiki/グレート・ファイアウォール "wikilink")
  - [Tor](../Page/Tor.md "wikilink")

[Category:VPN](https://ja.wikipedia.org/wiki/Category:VPN "wikilink") [Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink") [Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink")

1.  通信するにあたって、[セキュリティ上の懸念がない](../Page/コンピュータセキュリティ.md "wikilink")（あるいは少ない）
2.  盗聴自体を防ぐ術はないし、実際に、暗号化されていても[ディープ・パケット・インスペクション](https://ja.wikipedia.org/wiki/ディープ・パケット・インスペクション "wikilink")等によって、暗号化された通信からなんとか特徴を検出しようと、セキュリティ業者や[グレート・ファイアウォール](https://ja.wikipedia.org/wiki/グレート・ファイアウォール "wikilink")の運用者は躍起である。
3.  IPベースVPN、RFC 2764