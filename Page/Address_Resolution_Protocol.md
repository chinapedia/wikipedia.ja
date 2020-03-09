> この記事は[Address Resolution Protocol](https://ja.wikipedia.org/wiki/Address_Resolution_Protocol)から翻訳されています。


**Address Resolution Protocol** (アドレス解決プロトコル、略称：**ARP**、アープ)は、与えられた[インターネット層](https://ja.wikipedia.org/wiki/インターネット層 "wikilink")アドレス（一般的には[IPv4アドレス](https://ja.wikipedia.org/wiki/IPv4アドレス "wikilink")）に対応する[リンク層](https://ja.wikipedia.org/wiki/リンク層 "wikilink")アドレス（[MACアドレス](https://ja.wikipedia.org/wiki/MACアドレス "wikilink")など）を発見するために使用される[通信プロトコル](https://ja.wikipedia.org/wiki/通信プロトコル "wikilink")である。この対応付けは、[インターネット・プロトコル・スイート](https://ja.wikipedia.org/wiki/インターネット・プロトコル・スイート "wikilink")における重要な機能である。ARPは、1982年に RFC 826 \[1\]（[インターネット標準](https://ja.wikipedia.org/wiki/インターネット標準 "wikilink") STD 37）で定義され、その後 RFC 5227, RFC 5494 により内容のエンハンスが行われている。

ARPは、ネットワーク層技術とデータリンク層技術の様々な組み合わせで実装されている。[IEEE 802標準を使用した](https://ja.wikipedia.org/wiki/IEEE_802 "wikilink")[IPv4](https://ja.wikipedia.org/wiki/IPv4 "wikilink")、、[DECnet](https://ja.wikipedia.org/wiki/DECnet "wikilink")、(PUP)、および、[FDDI](https://ja.wikipedia.org/wiki/Fiber_distributed_data_interface "wikilink")、[X.25](https://ja.wikipedia.org/wiki/X.25 "wikilink")、[フレームリレー](https://ja.wikipedia.org/wiki/フレームリレー "wikilink")、[ATMなどである](https://ja.wikipedia.org/wiki/Asynchronous_Transfer_Mode "wikilink")。[IEEE 802.3](https://ja.wikipedia.org/wiki/IEEE_802.3 "wikilink")（[イーサネット](../Page/イーサネット.md "wikilink")）および[IEEE 802.11](https://ja.wikipedia.org/wiki/IEEE_802.11 "wikilink")（[無線LAN](../Page/無線LAN.md "wikilink")）上の[IPv4](https://ja.wikipedia.org/wiki/IPv4 "wikilink")が最も一般的な使用法である。

[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")ネットワークでは、ARPの機能は[ICMPv6](https://ja.wikipedia.org/wiki/ICMPv6 "wikilink")の[近隣探索プロトコル](https://ja.wikipedia.org/wiki/近隣探索プロトコル "wikilink")(NDP)によって提供される。

## 操作範囲

ARPはであり、メッセージがリンク層プロトコルによって[カプセル化される](https://ja.wikipedia.org/wiki/カプセル化_\(通信\) "wikilink")。単一のサブネットワークの内部のみで通信され、ルータを越えてルーティングされることはない。この特性のため、ARPは[インターネットプロトコルスイート](https://ja.wikipedia.org/wiki/インターネットプロトコルスイート "wikilink")の[リンク層](https://ja.wikipedia.org/wiki/リンク層 "wikilink")に配置される\[2\]。

## パケット構造

ARPは、1つのアドレスのみの解決要求または応答を含む単純なメッセージフォーマットを使用する。ARPメッセージのサイズは、リンク層とネットワーク層のアドレスサイズによって異なる。[メッセージヘッダで](https://ja.wikipedia.org/wiki/ヘッダ_\(コンピュータ\) "wikilink")、各層で使用されているネットワークの種類とそれぞれのアドレスのサイズを指定する。メッセージヘッダには、要求（1）と応答（2）のどちらかであるかを示すオペレーションコードが含まれる。パケットのペイロードは、送信側ホストと受信側ホストそれぞれのハードウェアアドレスとプロトコルアドレス、計4つのアドレスで構成されている

イーサネット上で実行されているIPv4ネットワークの場合のARPパケットの構造を次の表に示す。この例では、パケットには送信元ハードウェアアドレス(SHA)と送信先ハードウェアアドレス(THA)用の48ビットフィールドと、対応する送信元プロトコルアドレス(SPA)と送信先プロトコルアドレス(TPA)用の32ビットフィールドがある。この場合のARPパケットサイズは28バイトである。

|               |               |                                                                     |      |   |   |   |   |   |   |    |    |    |    |       |
| ------------- | ------------- | ------------------------------------------------------------------- | ---- | - | - | - | - | - | - | -- | -- | -- | -- | ----- |
| 0             | 1             | 2                                                                   | 3    | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14～41 |
| イーサネット宛先アドレス  | イーサネット送信元アドレス | [フレームタイプ](https://ja.wikipedia.org/wiki/フレーム_\(ネットワーク\) "wikilink") | 下図参照 |   |   |   |   |   |   |    |    |    |    |       |
| **イーサネットヘッダ** | **ARPの要求と応答** |                                                                     |      |   |   |   |   |   |   |    |    |    |    |       |

| Octet offset | 0                   | 1                  |
| ------------ | ------------------- | ------------------ |
| 0            | ハードウェアタイプ(HTYPE)    |                    |
| 2            | プロトコルタイプ(PTYPE)     |                    |
| 4            | ハードウェアアドレスサイズ(HLEN) | プロトコルアドレスサイズ(PLEN) |
| 6            | オペレーション(OPER)       |                    |
| 8            | 送信元ハードウェアアドレス(SHA)  |                    |
| 10           |                     |                    |
| 12           |                     |                    |
| 14           | 送信元プロトコルアドレス(SPA)   |                    |
| 16           |                     |                    |
| 18           | 送信先ハードウェアアドレス(THA)  |                    |
| 20           |                     |                    |
| 22           |                     |                    |
| 24           | 送信先プロトコルアドレス(TPA)   |                    |
| 26           |                     |                    |

[Internet Protocol](../Page/Internet_Protocol.md "wikilink") ([IPv4](https://ja.wikipedia.org/wiki/IPv4 "wikilink")) [イーサネット](../Page/イーサネット.md "wikilink") ARP [パケット](https://ja.wikipedia.org/wiki/パケット "wikilink")

  - ハードウェアタイプ (HTYPE): ネットワーク[プロトコル](../Page/プロトコル.md "wikilink")の種類。[イーサネット](../Page/イーサネット.md "wikilink")の場合は1。
    プロトコルタイプ (PTYPE): ARPリクエスト要求が意図するインターネットプロトコル。[IPv4](https://ja.wikipedia.org/wiki/IPv4 "wikilink")の場合、0x0800以降の値。使用される値は、[EtherType](https://ja.wikipedia.org/wiki/EtherType "wikilink")のものを流用する\[3\]\[4\]\[5\]。
    ハードウェア長 (HLEN): [オクテットによるハードウェアアドレスの長さ](https://ja.wikipedia.org/wiki/オクテット_\(コンピュータ\) "wikilink")。イーサネットアドレス（[MACアドレス](https://ja.wikipedia.org/wiki/MACアドレス "wikilink")）のサイズは6。
    プロトコル長 (PLEN): 上位層の[プロトコル](../Page/プロトコル.md "wikilink")（PTYPEに指定された上位層プロトコル）が使用する[オクテットによるアドレス](https://ja.wikipedia.org/wiki/オクテット_\(コンピュータ\) "wikilink")。IPv4のアドレスサイズは4。
    オペレーション : 送信者が実行している動作。1は要求、2は返信。
    送信元ハードウェアアドレス (SHA): 送信側のメディアアドレス（Media address、[MACアドレス](https://ja.wikipedia.org/wiki/MACアドレス "wikilink")）。ARPリクエストでは、要求を送信するホストのアドレスを示す。ARP応答では、要求が探していたホストのアドレスを示す。（必ずしも、仮想メディアのように応答するホストのアドレスではない。）スイッチはMACアドレスを学習するが、このフィールドに注意を払っていないことに注意が必要である。ARP [PDUは](https://ja.wikipedia.org/wiki/Protocol_Data_Unit "wikilink")、[イーサネットフレーム](https://ja.wikipedia.org/wiki/イーサネットフレーム "wikilink")にカプセル化され、[データリンク層](https://ja.wikipedia.org/wiki/データリンク層 "wikilink")（第2層）のデバイスが調べる。
    送信元プロトコルアドレス (SPA): 送信元のインターネットワークアドレス（internetwork address、[IPアドレス](../Page/IPアドレス.md "wikilink")）。
    送信先ハードウェアアドレス (THA): 受信側のメディアアドレス（Media address、[MACアドレス](https://ja.wikipedia.org/wiki/MACアドレス "wikilink")）。ARPリクエストでは、このフィールドは無視する。ARP応答では、このフィールドは、ARPリクエストを送信した[ホストのアドレスを示す](https://ja.wikipedia.org/wiki/ホスト_\(ネットワーク\) "wikilink")。
    送信先プロトコルアドレス (TPA): 送信先のインターネットワークアドレス（internetwork address、[IPアドレス](../Page/IPアドレス.md "wikilink")）。

ARPプロトコルのパラメータ値は [Internet Assigned Numbers Authority](../Page/Internet_Assigned_Numbers_Authority.md "wikilink") (IANA) によって標準化され、維持されている.\[6\]。

ARPの[EtherType](https://ja.wikipedia.org/wiki/EtherType "wikilink")は0x0806である。これは、イーサネットヘッダ内で使用されてペイロードがARPパケットであることを示すものであり、カプセル化されるARPパケット内に含まれるPTYPEとは別である。

## 動作

送信元は、送信元のIPアドレス・MACアドレスと送信先のIPアドレスを格納したARPリクエスト（送信先のMACアドレスはALL0）を[ブロードキャスト](https://ja.wikipedia.org/wiki/ブロードキャスト "wikilink")で送信する。ARPリクエストを受信した各[ノードは](https://ja.wikipedia.org/wiki/ノード_\(ネットワーク\) "wikilink")、格納された送信先IPアドレスが自身のIPアドレスと同一であれば、自身のMACアドレスを格納したARPリプライを送信元に返信する。

### ARPキャッシュ

効率を上げるため、多くの機器では一度取得したIPアドレスとMACアドレス間のマッピング情報を**ARPテーブル**に**ARPキャッシュ**として保持する。BSD Unix に由来する TCP/IP スタックを実装した機器の多くは、タイムアウト値として 1200秒（20分）を採用している。また、[Ciscoの機器ではタイムアウトのデフォルト値として](https://ja.wikipedia.org/wiki/シスコシステムズ "wikilink")14400秒（4時間）を採用している。キャッシュ情報は[TCP/IPがサポートされた](https://ja.wikipedia.org/wiki/インターネット・プロトコル・スイート "wikilink")[Windowsであれば](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[コマンドプロンプト](https://ja.wikipedia.org/wiki/コマンドプロンプト "wikilink")から *arp -a* と入力すれば一覧が見られ、キャッシュ情報はハイフンで分割された6つの16進数で表示される。

## ARPプローブ

**ARPプローブ**(ARP probe)とは、送信者IPアドレス(SPA)をALL0にしたARPリクエストである。この用語は、IPv4 Address Conflict Detection（IPv4アドレス競合検出）仕様( RFC 5227 )で使用されている。この仕様を実装しているホストは、IPv4アドレスの使用を開始する前に（手動設定、DHCP、またはその他の手段でIPアドレスを受信したかどうかにかかわらず）、ARPプローブパケットをブロードキャストで送信して、アドレスが既に使用中かどうかを確認する必要がある\[7\]。

## ARPアナウンスメント

ARPは、単純なアナウンスプロトコルとしても使用できる。これは、送信者のIPアドレスまたはMACアドレスが変更されたときに、他のホストのハードウェアアドレスのマッピングを更新するために使用される。このアナウンスメントは[gratuitous ARP](https://ja.wikipedia.org/wiki/gratuitous_ARP "wikilink")(GARP)メッセージとも呼ばれ、通常、送信先ハードウェアアドレス(THA)をALL0に設定し、送信元プロトコルアドレスを送信先プロトコルアドレスに格納した(TPA=SPA)ARPリクエストパケットであり、ブロードキャストで送信される。また、送信先アドレスと送信元アドレスの両方に送信元アドレスを格納(TPA=SPA、THA=SHA)したARPリプライをブロードキャストで送信したものもARPアナウンスメントとして使用される。

gratuitous ARPは、ARPリクエスト・ARPリプライのどちらも規格に規定されている正規の手法である\[8\]\[9\]が、ARPリクエストを使用するほうが望ましい\[10\]。デバイスによっては、どちらかのGARPを使用するように設定されているものもある\[11\]。

ARPアナウンスは応答を求めることを目的としていない。パケットを受信した他のホストに対し、ARPテーブル内のキャッシュエントリを更新させることを目的としている。ARPの規格では、ARPテーブルがアドレスフィールドから更新される時のみオペレーションコードを解釈することと規定しているので、オペレーションコードは要求と応答のどちらでも良い\[12\]\[13\]\[14\]。

多くのオペレーティングシステムは、起動時にGratuitous ARPを実行する。これは、仮に電源を落としている間に[ネットワークカード](https://ja.wikipedia.org/wiki/ネットワークカード "wikilink")が変更されていた場合に、他のホストのARPキャッシュテーブルにIPアドレスと以前のMACアドレスとのマッピングが残っていると問題が起こるためである。

## ARPメディエーション

**ARPメディエーション**(ARP mediation)とは、接続した回線で異なるアドレス解決プロトコルが使用されている場合（例えば、一方の端が[イーサネット](../Page/イーサネット.md "wikilink")で、もう一方の端が[フレームリレー](https://ja.wikipedia.org/wiki/フレームリレー "wikilink")であるような場合）、Virtual Private Wire Service(VPWS)を介してレイヤ2アドレスを解決するプロセスである。[IPv4](https://ja.wikipedia.org/wiki/IPv4 "wikilink")では、各(PE)デバイスは、ローカルに接続されている(CE)デバイスのIPアドレスを検出し、そのIPアドレスを対応するリモートPEデバイスに配布する。その後、各PEデバイスは、リモートCEデバイスのIPアドレスとローカルPEデバイスのハードウェアアドレスを使用してローカルのARPリクエストに応答する。[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")では、各PEデバイスはローカルとリモートの両方のCEデバイスのIPアドレスを検出し、次にローカルの[近隣探索](https://ja.wikipedia.org/wiki/近隣探索プロトコル "wikilink")(ND)パケットと逆近隣探索(IND)パケットを代行受信し、それらをリモートPEデバイスに転送する\[15\]。

## Inverse ARP

**Inverse Address Resolution Protocol**（**Inverse ARP**、**InARP**）は、[データリンク層](https://ja.wikipedia.org/wiki/データリンク層 "wikilink")（レイヤ2）アドレスから他のノードの[ネットワーク層](https://ja.wikipedia.org/wiki/ネットワーク層 "wikilink")アドレス（IPアドレスなど）を取得するために使用される。これは主に[フレームリレー](https://ja.wikipedia.org/wiki/フレームリレー "wikilink")（）やATMで使用される。これらのネットワークでは、仮想回線のレイヤ2アドレスはレイヤ2シグナリングから取得されることがあり、その仮想回線を使用する前に対応するレイヤ3アドレスを使用できるようにする必要がある\[16\]。

ARPはレイヤ3アドレスをレイヤ2アドレスに変換するので、InARPはその逆と表現することができる。InARPはARPのプロトコル拡張として実装されている。ARPと同じパケットフォーマットを使用するが、オペレーションコードは異なる。

## Reverse ARP

[Reverse Address Resolution Protocol](https://ja.wikipedia.org/wiki/Reverse_Address_Resolution_Protocol "wikilink")（Reverse ARP、RARP）は、InARPと同様にレイヤ2アドレスをレイヤ3アドレスに変換するために使用する。ただし、InARPでは、要求側は別のノードのレイヤ3アドレスを照会するのに対し、RARPはアドレス設定の際に要求側自体のレイヤ3アドレスを取得するために使用される。RARPは現在ではほぼ使用されていない。RARPは[BOOTP](https://ja.wikipedia.org/wiki/BOOTP "wikilink")に置き換えられ、BOOTPも後に[DHCPに置き換えられている](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")\[17\]。

## ARPスプーフィングとプロキシARP

[ARP_Spoofing.svg](https://ja.wikipedia.org/wiki/File:ARP_Spoofing.svg "fig:ARP_Spoofing.svg")攻撃が成功した場合、攻撃者は[中間者攻撃](https://ja.wikipedia.org/wiki/中間者攻撃 "wikilink")を行うことができる。\]\]  ARPにはネットワーク上のARPリプライを認証する方法がなく、ARPリプライは必要なレイヤ2アドレスを持つシステム以外のシステムから送信される可能性もある。プロキシARP(Proxy ARP)は、ネットワークの設計の一部として、他のネットワークにARP要求があった場合に[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")がホストに代わって回答する仕組みであり、[NAT環境下において使用される例が多い](https://ja.wikipedia.org/wiki/ネットワークアドレス変換 "wikilink")。これに対して、ARPスプーフィング(ARP spoofing)は、そのシステム宛てのデータを傍受する目的で、別のシステムのアドレスに対するARPリクエストに応答するものである。ARPスプーフィングを使用して、悪意のあるユーザがネットワーク上の他のユーザーに対して[中間者攻撃](https://ja.wikipedia.org/wiki/中間者攻撃 "wikilink")や[DoS攻撃](https://ja.wikipedia.org/wiki/DoS攻撃 "wikilink")を行う可能性がある。ARP自体にはこのような攻撃からの保護方法は提供されておらず、ARPスプーフィング攻撃を検出して対策するための様々なソフトウェアが存在する\[18\]。

## ARPの代替

それぞれのコンピュータは、レイヤ3アドレス（[IPアドレス](../Page/IPアドレス.md "wikilink")など）とレイヤ2アドレス（[イーサネット](../Page/イーサネット.md "wikilink")[MACアドレス](https://ja.wikipedia.org/wiki/MACアドレス "wikilink")など）のマッピングのデータベースを維持する。これは、主にローカルネットワークリンクからのARPパケットの受信によって維持されることから、このデータベースは一般に「ARPキャッシュ」と呼ばれる。伝統的には、静的な設定ファイル\[19\]や一元管理されたリストなど、このテーブルを管理するために他の方法も使われていた。

少なくとも1980年代以降\[20\]、ネットワーク接続のできるコンピュータは、このテーブルを表示したり操作したりするための'arp'というユーティリティを持っている\[21\]\[22\]\[23\]。

## ARPスタッフィング

ネットワークカメラ\[24\]やネットワーク配電装置\[25\]などのユーザインタフェースのない組み込みシステムでは、「ARPスタッフィング」(ARP stuffing)を使って初期ネットワーク接続を行うことができる。ただし、この仕組みはARPは関係ないので、これは不適切な名称である。

ARPスタッフィングは、コンシューマデバイスのネットワーク管理、特にイーサネットデバイスのIPアドレスの割り当てにおける以下のような問題の解決策である。

1.  ユーザは、DHCPなどのアドレス割り当てプロトコルを制御することができない。
2.  デバイスは、それを設定するためのユーザーインターフェースを持っていない。
3.  適切なIPアドレスがないため、ユーザのコンピュータは通信ができない。

採用された解決策は以下の通りである。

  - ユーザのコンピュータは、アドレステーブルに手動で入力（*stuffed* = 詰め込まれる）されたIPアドレスを持っている（通常はarpコマンドを使用し、MACアドレスをデバイスのラベルから取得する）。
  - コンピュータは特殊なパケットをデバイスに送信する。通常は、デフォルト以外のサイズの[ping](https://ja.wikipedia.org/wiki/ping "wikilink")パケットである。
  - デバイスはこのIPアドレスを採用する。
  - その後、ユーザは[telnet](https://ja.wikipedia.org/wiki/telnet "wikilink")や[Webプロトコルで通信して設定を完了する](https://ja.wikipedia.org/wiki/HTTP "wikilink")。

ARPスタッフィングを使用するデバイスは通常、攻撃に対して脆弱であるため、デバイスが正常に動作しているときはこのプロセスを無効にする。

## 標準文書

  - \- Ethernet Address Resolution Protocol, Internet Standard STD 37.

  - \- Reverse Address Resolution Protocol, Internet Standard STD 38.

  - \- Inverse Address Resolution Protocol, draft standard

  - \- IPv4 Address Conflict Detection, proposed standard

## 関連項目

  - [ARPスプーフィング](https://ja.wikipedia.org/wiki/ARPスプーフィング "wikilink")

  - [Reverse address resolution protocol](https://ja.wikipedia.org/wiki/Reverse_address_resolution_protocol "wikilink")(RARP、リバースARP) - [MACアドレス](https://ja.wikipedia.org/wiki/MACアドレス "wikilink")から[IPアドレス](../Page/IPアドレス.md "wikilink")に変換する[プロトコル](../Page/プロトコル.md "wikilink")

  - [Gratuitous ARP](https://ja.wikipedia.org/wiki/Gratuitous_ARP "wikilink") - ARP[パケット](https://ja.wikipedia.org/wiki/パケット "wikilink")の送信元[ホスト自身の](https://ja.wikipedia.org/wiki/ホスト_\(ネットワーク\) "wikilink")[IPアドレス](../Page/IPアドレス.md "wikilink")に対するARP

  - [ブリッジ](https://ja.wikipedia.org/wiki/ブリッジ_\(ネットワーク機器\) "wikilink")

  - [レイヤ3スイッチ](https://ja.wikipedia.org/wiki/レイヤ3スイッチ "wikilink")

  - [近隣探索プロトコル](https://ja.wikipedia.org/wiki/近隣探索プロトコル "wikilink")

  - \- [ルーター](https://ja.wikipedia.org/wiki/ルーター "wikilink")などが代理で[IPアドレス](../Page/IPアドレス.md "wikilink")を回答する仕組み

## 脚注

## 外部リンク

  - [RFC826 "An Ethernet Address Resolution Protocol"](http://www.ietf.org/rfc/rfc826.txt) ([日本語訳](http://www.f4.dion.ne.jp/~adem/rfc/rfc826.euc.txt))
  - [RFC5227 "IPv4 Address Conflict Detection"](http://www.ietf.org/rfc/rfc5227.txt) ([日本語訳](http://www.kasai.fm/wiki/rfc5227jp))
  - [RFC5494 IANA Allocation Guidelines for the Address Resolution Protocol (ARP)](http://www.ietf.org/rfc/rfc5494.txt)
  - [ARP Sequence Diagram (pdf)](http://www.eventhelix.com/RealtimeMantra/Networking/Arp.pdf)
  - [Gratuitous ARP](http://wiki.wireshark.org/Gratuitous_ARP)
  - [ARP-SK ARP traffic generation tools](https://web.archive.org/web/20090903074149/http://sid.rstack.org/arp-sk/)
  - [Sample Capture file from WireSharkWiki](http://wiki.wireshark.org/SampleCaptures#head-2fb4a82886c1d8c722134b44461e22e5f7f54b32)

[Category:リンク層プロトコル](https://ja.wikipedia.org/wiki/Category:リンク層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.
2.
3.  \[//www.iana.org/assignments/arp-parameters/arp-parameters.xhtml IANA ARP - "Protocol Type"\]
4.  [IANA - Ethertype values](https://www.iana.org/assignments/ethernet-numbers/ethernet-numbers.xhtml)
5.
6.
7.
8.
9.
10.
11.
12. [Gratuitous ARP in DHCP vs. IPv4 ACD Draft](http://www1.ietf.org/mail-archive/web/dhcwg/current/msg03797.html)
13. [RFC 2002 Section 4.6](http://tools.ietf.org/html/rfc2002#section-4.6)
14. [RFC 2131 DHCP – Last lines of Section 4.4.1](http://tools.ietf.org/html/rfc2131#section-4.4.1)
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.