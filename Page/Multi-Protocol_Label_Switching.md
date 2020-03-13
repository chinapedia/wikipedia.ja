> この記事は[Multi-Protocol Label Switching](https://ja.wikipedia.org/wiki/Multi-Protocol_Label_Switching)から翻訳されています。


**Multi-Protocol Label Switching** (**MPLS**) とは、[フレームや](https://ja.wikipedia.org/wiki/フレーム_\(ネットワーク\) "wikilink")[パケット](../Page/パケット.md "wikilink")の前方に[ラベル](../Page/ラベル.md "wikilink")と呼ばれる識別子を付加して転送を行うことにより、通信の高速化や機能の付加を図る技術である。 当初、[ルーター](../Page/ルーター.md "wikilink")によるパケット転送処理の高速化を実現する技術として登場したが、ルーターの[ハードウェア](../Page/ハードウェア.md "wikilink")化に伴い高速化の利点は薄れ、変わって様々な機能の実現手段として注目されている。MPLSによって実現される機能として、[Virtual Private Network](../Page/Virtual_Private_Network.md "wikilink") (VPN) や[Quality of Service](../Page/Quality_of_Service.md "wikilink") (QoS) などが有る。

## 概要

MPLSでは、Label Switched Path (**LSP**) と呼ばれるパスを構成し、通信を行う。 LSPは経路の片方だけのパスであり、両方向の経路のパスで通信を行う場合はLSPが2つ必要になる。

MPLSはOSI7層構造の第2層 (L2; Layer 2) データリンクレイヤ (Data Link Layer) と、第3層 (L3; Layer 3) ネットワークレイヤ (Network Layer) の中間に位置することになるため、「レイヤ2.5」と呼ばれることもある。 MPLSを伝送するデータリンクレイヤとしては、[イーサネット](../Page/イーサネット.md "wikilink") (Ethernet)、[Asynchronous Transfer Mode](../Page/Asynchronous_Transfer_Mode.md "wikilink") (ATM)、POS (Packet over [SDH](https://ja.wikipedia.org/wiki/SDH "wikilink")/[SONET](https://ja.wikipedia.org/wiki/Synchronous_Optical_Network "wikilink")) などがある。 MPLS上に伝送される通信プロトコル/フォーマット(クライアントプロトコル)としては、[IPパケット](../Page/Internet_Protocol.md "wikilink")、イーサネット、[PPPなどがある](../Page/Point-to-Point_Protocol.md "wikilink")。イーサネット、PPPなどの多種のレイヤ2ネットワークを構成する手法は、Any Transport over MPLS (AToM)とも呼ばれる。

EoMPLS (Ethernet over MPLS) により、広域でイーサネットネットワークを構成可能なため、広域イーサネットサービスのバックボーンとして使用されることもある。また、MPLS上に[インターネットエクスチェンジ](../Page/インターネットエクスチェンジ.md "wikilink") (IX) を実現するサービスも実用化されている。

## 動作

MPLSをサポートする通信装置は、**LSR** (Label Switch Router) と呼ばれる。MPLS網のエッジに位置する装置を**LER** (Label Edge Router) と呼び区別する場合もある。

MPLSでは、ルーティングとフォワーディングが明確に区別されており、ルーティングに関しては基本的に従来の[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")で用いられていた[Interior Gateway Protocol](../Page/Interior_Gateway_Protocol.md "wikilink") (IGP) を使用する。

フォワーディングは、ラベル交換 (Label Swapping) を伴う転送となる。Label Swappingでは、入力インターフェイスから到着したパケットのラベルを、別のラベルに入れ替え (Swap) し、出力インターフェイスへ送出する。 この際の入力インターフェイス/入力ラベルのペアと、出力インターフェイス/出力ラベルのペアの対応表はラベルテーブル (Label Table) と呼ばれ後述のラベル配布プロトコルによって各LSRに配布される。

ラベル階層を多層化し、LSPを多層化することもできる。

なお、ラベル交換によるフォワーディングはMPLSの最も理解しやすい一面であり、これをもってMPLSと説明されることもある。MPLSの開発当初は、最長一致 (longest match) が必要で、[ルーティングテーブル](../Page/ルーティングテーブル.md "wikilink")のエントリ数により処理時間が増大するIPアドレスベースでの次ホップ検索よりも、完全一致で事足りるMPLSラベル検索の方が処理が簡潔になり、高速転送が実現できるという目論見があった。しかし、TCAM（三値[連想メモリ](../Page/連想メモリ.md "wikilink") : Ternary Content Addressable Memory）の利用により、IPアドレスの最長一致もエントリ数に係らず固定時間での処理が可能となったため、IP転送に比べ、高速転送という優位性は無くなった。しかし（少なくとも現在の）MPLSの利点は、後述の付加機能にある。

ルーティング情報が行き渡った後、[Label Distribution Protocol](https://ja.wikipedia.org/wiki/Label_Distribution_Protocol "wikilink") (LDP) や[Resource Reservation Protocol](../Page/Resource_Reservation_Protocol.md "wikilink") (RSVP) 等のラベル配布プロトコルを用いてラベル情報を配布する。 RSVPは元々はQoS用のリソース予約プロトコルであるが、拡張を施し、MPLSのラベル配布に流用している。 LDPはプレフィックスベースのラベル配布であり、IGPで得られたルーティングテーブルとラベルテーブルを一致させることを基本とする。 RSVPはトンネルベースのラベル配布であり、IGPで得られたネットワークトポロジ上に、LSPによるトンネルを構成することを基本とする。

ラベル配布の前には、 I-BGP ([Border Gateway Protocol](../Page/Border_Gateway_Protocol.md "wikilink")) や[Open Shortest Path First](../Page/Open_Shortest_Path_First.md "wikilink") (OSPF)、[IS-IS](../Page/IS-IS.md "wikilink")、[Routing Information Protocol](../Page/Routing_Information_Protocol.md "wikilink") (RIP) などのIGPによって、MPLSドメイン内のルーティングテーブルが全てのノードで一貫性が保たれていることを前提としている。ドメイン内のルーティングをOSPFで行い、他AS ([Autonomous System](../Page/自律システム_\(インターネット\).md "wikilink")) などの外部ドメインの情報をI-BGPによりボーダールーター間でやりとりするのが一般的であろう。

## 付加機能

MPLSによって、パケット網に付加される機能は以下のようなものがある。

### 到達性の制御

MPLSはIPより下のレイヤとなるため、MPLS上に構成されるIPネットワークの到達性(Reachablity)を完全に制御することができる。つまり、一つのMPLSネットワーク上に、複数の、互いに到達性の無いIPネットワークを構成することができる。これらのIPネットワーク間には到達性がないため、通信が混ざり合うことがなく、高い機密性が保たれる。また各々のIPネットワーク毎にIPアドレス空間が独立であるため、IPアドレスの衝突が起こらない。これらの特性により、IP-VPNが実現されている。

この到達性の制御は、MPLS上に構築される、どのようなパケット網に対しても効果を発揮する。 つまり、MPLS上にイーサネット網を構築する、VPLS（後述）や、これから出てくるかもしれない新規のパケット網においても、MPLSのレベルで到達性を制御することができる。

### 障害回復機能

FRR (Fast ReRoute) を使うことで、MPLSネットワーク上で50msec以下での障害回復が実現される。 RFC4427 "Recovery (Protection and Restoration) Terminology form GMPLS" によると、 障害回復 (Recovery) には、Protection、つまり事前に予備のネットワーク資源を確保しておく方式と、 Restoration、つまり事前の資源確保を行わない方式が含まれる。 FRRによる障害回復はProtectionに当たる。

FRRでは、保護対象となるPrimary LSPの経路上の障害が発生する可能性のある個所(ノード、リンク)を迂回するような、Protection用のLSP (Detour LSP) を張っておく。この際、Primary LSPからDetour LSPへ分岐するノードをPLR (Point of Local Repair)、Detour LSPがPrimary LSPへ再度合流するノードをMP (Merge Point) と呼ぶ。 MPでは、Primary LSP用のラベル、Detour LSP用のラベルの双方を受け取ることができるようにしておく。 このような準備をしておくことで、PLR-MP間で障害が発生した場合、PLRでの送信インターフェイス、送信ラベルを、それぞれPrimary LSP用のものから、Detour LSP用のものに切り替えるだけで、障害回復が達成される。

なにをもって、障害のトリガとするかは、実装にゆだねられるが、POSの場合はSDH/SONETのアラーム、イーサネットの場合にはリンクダウンアラーム、その他一般的にはRSVP Helloによる検出などがある。

10GbE WAN-PHYの場合は、イーサネットではあるが、SDH/SONETの10Gbps信号 (STM-64/OC-192) にマッピングされるため、SDH/SONETの機能による障害検知が可能である。

光のGbE (1000Base-SX/LX) でも、8B10B符号化の副産物である、帯域外の信号を用いて、高速なリンクダウンの検出を可能としている。

なお、このFRRと同等の機能を、MPLSではない[IP網](https://ja.wikipedia.org/wiki/IP網 "wikilink")に実装しようとする動き (IP-FRR) もある。RFC 5714などを参照のこと。

### 多種のネットワークの集約

MPLSでは多種のクライアントプロトコルを伝送することができるため、IP網以外のパケット網をMPLS網の上に集約 (Convergence) させることができる。 それが、前述のAToMのコンセプトにつながっている。

現在、広く実用となっているものとしては、Ethernet over MPLS (EoMPLS) がある。

PWE3 (Pseudo Wire Emulation Edge to Edge) はMPLSネットワーク上に仮想的なPoint-to-Pointのイーサネット専用線を構成する。 VPLS (Virtual Private Line Service) はMPLSネットワーク上に仮想的なイーサネットスイッチを作り出すことができる。 PWE3もVPLSもEoMPLS（広義のEoMPLS）の一形態と言えるが、PWE3を単にEoMPLS(狭義のEoMPLS)と言うこともある。 また、それぞれの主な提唱者の名前から、PWE3をmartini、VPLSをkompellaと呼ぶこともある（それぞれ、Luca Martiniと、Kireeti Kompella）。

PWE3をMPLS網の上以外にも拡張して使うというアイディアもある (Dry-martini)。

### トラフィック・エンジニアリング

MPLSでは、LSPの通る経路を明示的に (Explicitに) 指定することにより、LSPの経路を自由に制御することができる。この機能を適用することで、トラフィックの分散を図ることができる。 また、MPLSノード (LSR)によっては、LSP単位で、帯域確保や、帯域制限、優先制御などの各種QoS制御をおこなうことができる。

MPLSではOSPFやRSVP、LDPなどの制御プロトコルのパケットが、通常の通信のパケットと同じ回線を通る。この方式は手軽に構成できる反面、輻輳（通信量過多）や回線異常が直接的にネットワーク制御に影響を及ぼすため、ネットワークの安定性に劣る。MPLS-TEではOSPFやRSVP、LDPに拡張を施すことにより、 制御対象のネットワーク(通常のデータが通るネットワーク)とは別の回線で制御を行うことが可能となった。拡張されたプロトコルは、それぞれ、OSPF-TE、RSVP-TE、CR-LDP となる。

### マルチキャスト

一部の装置は、Point-to-Multi-pointのLSPを張ることができる (P-MP LSP)。 P-MP LSPにより、前述の各種トラフィックエンジニアリング機能を使うことや、マルチキャスト経路の把握が容易となるため、今後の[IPマルチキャスト](https://ja.wikipedia.org/wiki/IPマルチキャスト "wikilink")の普及に寄与することが期待される。

## GMPLS

MPLSではラベルスタックという明示的なラベル識別子を各データグラム内に記述する。ルーティングやラベル配布などのアーキテクチャは、これがSDH/SONETにおけるタイムスロット位置や、WDM通信における光の波長のような、「暗黙的なラベル」であっても通用する、との考えのもとに[Generalized Multi-Protocol Label Switching](../Page/Generalized_Multi-Protocol_Label_Switching.md "wikilink") (GMPLS) へと拡張されている。

GMPLSの発足当初は、光クロスコネクト（OXC; optical cross connect、またはPXC; Photonic cross connect）がその制御の主な対象として議論されていた。 OXCとPXCの使い分けは明確ではないが、完全に光で、つまりアナログ的に処理するものをPXC、一旦電気信号に変換し、[デジタル](../Page/デジタル.md "wikilink")的に処理するものをOXCと呼ぶ傾向がみられる。

しかし、2006年現在、GFP/VCAT/LCASといった次世代SDH/SONET（もしくはOTN）機能を搭載し、IP (POS)、イーサネット、[ファイバーチャネル](../Page/ファイバーチャネル.md "wikilink")、InfiniBandなど多様なプロトコルを柔軟に収容、伝送、経路制御する装置群が台頭しつつある。 これらの装置群は、MSSP (Multi Service Switching Platform)/MSTP (Multi Service Transport Platform)/MSPP (Multi Service Provisioning Platform) と呼ばれ、その機能の違いにより区別される。3つを総称してMSxPと呼ぶこともある。 MSTPの中にはROADM (Reconfigurable Optical Add/Drop Multiplexer) やPXCの機能を統合したものもある。 現時点でも同一メーカーのMSxP間ではGMPLSを使用することが一般的であり、今後は、MSxPがGMPLSの主な担い手となるのではないかと予想される。

GMPLSは、MPLSを拡大した考え方であり、GMPLSはMPLSを内包する。GMPLSにより拡張されたSDH/SONETなどのいわゆる伝送ノード (Transport Node) への制御性を、伝送網 (Transport Network) 内に閉じて利用するという考え方もあり、これは (Transport-MPLS) と呼ばれる。 T-MPLSでは、従来のMPLS網との連携は考えず、伝送網の管理のみにGMPLSアーキテクチャを利用する。

### L1 VPN

## 関連項目

  - [IS-IS](../Page/IS-IS.md "wikilink")
  - [IEEE 802.1aq](https://ja.wikipedia.org/wiki/IEEE_802.1aq "wikilink") - [Shortest Path Bridging (SPB)](https://ja.wikipedia.org/wiki/Shortest_Path_Bridging "wikilink")

## 関連する標準化文書

  - RFC 3031 (Multiprotocol Label Switching Architecture) ではMPLSのアーキテクチャについて述べられている。NHLFE (Next Hop Label Forwarding Entry) や、ILM (Incoming Label Map)、FEC (Forwarding Equivalence Class) などのMPLSを構成する重要な概念についての説明がなされている。
  - RFC 3032 (MPLS Label Stack Encoding) では、ラベルスタック (Label stack) の構造が定義されている。

[Category:トンネリング](https://ja.wikipedia.org/wiki/Category:トンネリング "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink")