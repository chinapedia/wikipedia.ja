> この記事は[Internet Group Management Protocol](https://ja.wikipedia.org/wiki/Internet_Group_Management_Protocol)から翻訳されています。


**Internet Group Management Protocol** (**IGMP**) とは、[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")上で[マルチキャスト](../Page/マルチキャスト.md "wikilink")（特定の一対多または多対多通信）を行うために、マルチキャストに参加する[ホスト](https://ja.wikipedia.org/wiki/ホスト "wikilink")のグループを設定し、ネットワークに通知するための[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。マルチキャストは、動画や音楽の[ストリーミング](../Page/ストリーミング.md "wikilink")など、同時に多数のホストへ同一のデータを送信するときに通信を効率化する技術である。

IGMPは[IPv4](../Page/IPv4.md "wikilink")ネットワーク向けのマルチキャストプロトコルであり、[インターネット・プロトコル](../Page/Internet_Protocol.md "wikilink") (IP) 上に直に実装されている。一方、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")では同様の役割を担う[Multicast Listener Discovery](https://ja.wikipedia.org/wiki/Multicast_Listener_Discovery "wikilink") (MLD) が[ICMPv6](https://ja.wikipedia.org/wiki/ICMPv6 "wikilink")上に実装されている。

## 設計

[IGMP_basic_architecture.png](https://ja.wikipedia.org/wiki/File:IGMP_basic_architecture.png "fig:IGMP_basic_architecture.png")

  - グループアドレスはローカルネットワークで割り当てた専用のグループアドレスか、アプリケーションごとに[IANAによって割り当てられた](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")[グローバルアドレス](https://ja.wikipedia.org/wiki/グローバルIPアドレス "wikilink")、もしくはPIM-SSMのために割り当てられたグローバルアドレス（詳しくは[\#Membership Query パケットを参照](https://ja.wikipedia.org/wiki/#Membership_Query_パケット "wikilink")）を用いる。
  - 受信側ホストは、参加するグループのアドレスをIGMPパケットによって最寄りの[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")へ通知する。
  - 送信側ホストは、自身のユニキャストアドレス発・グループアドレス宛の[パケット](../Page/パケット.md "wikilink")を、最寄りの[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")に[UDP](https://ja.wikipedia.org/wiki/UDP "wikilink")などで送信する。
  - [ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")は、グループの参加しているホストの属しているネットワーク(LANセグメント)すべてに[パケット](../Page/パケット.md "wikilink")が行き渡るように、[パケット](../Page/パケット.md "wikilink")を転送する。具体的なルータ間の伝送経路は、[Protocol-Independent Multicastや](https://ja.wikipedia.org/wiki/Protocol-Independent_Multicast "wikilink")[DVMRP](https://ja.wikipedia.org/wiki/DVMRP "wikilink")などの[プロトコル](../Page/プロトコル.md "wikilink")によって管理される。[ユニキャスト](https://ja.wikipedia.org/wiki/ユニキャスト "wikilink")用の[アドレステーブル](https://ja.wikipedia.org/wiki/アドレステーブル "wikilink")とは別個のアドレステーブルが使われる。
  - 受信側ルータからホストの間の[L2スイッチ](https://ja.wikipedia.org/wiki/L2スイッチ "wikilink")は、グループアドレス宛のパケットをブロードキャストする。ただし、スイッチを通過するIGMPパケットを認識し、どのホストがどのグループに参加しているかを記憶すること (**IGMP snooping**) ができるL2スイッチは、グループへ参加しているホストのあるノードへのみパケットを転送することができ、不必要な帯域を浪費しないですむ。
  - [IPマルチキャスト](https://ja.wikipedia.org/wiki/IPマルチキャスト "wikilink")では、[TCPによってパケットの到達を確認することはできない](../Page/Transmission_Control_Protocol.md "wikilink")。品質の高いネットワークを用いるか、品質を管理する仕組みを別途用意する必要がある。

## 標準

IGMP は [Internet Engineering Task Force](../Page/Internet_Engineering_Task_Force.md "wikilink") (IETF) によって定められ、[Request for Comments](../Page/Request_for_Comments.md "wikilink") (RFC) として公開されている。 \[1\] 2011年現在IGMPv3が最新の規格である。IGMPv2ではグループからの離脱を通知する方法が追加され、IGMPv3では指定されたIPアドレスからのみマルチキャストを受信する方法 (PIM-SSMへの対応)などが追加された。

## ホストとルータの実装

IGMPに[ホスト](https://ja.wikipedia.org/wiki/ホスト "wikilink")として対応している[OSには](../Page/オペレーティングシステム.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")や[Linux](../Page/Linux.md "wikilink")、[Microsoft Windowsなどがある](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。 IGMPに[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")として対応しているルーティングプログラムには、[mrouted](https://ja.wikipedia.org/wiki/mrouted "wikilink") (Linux), [XORP](https://ja.wikipedia.org/wiki/XORP "wikilink"), [Quagga](https://ja.wikipedia.org/wiki/Quagga "wikilink")などがある。

## セキュリティ

IGMPは一般的なアプリケーションで用いられるほど普及しておらず、またWindowsでは[DoS攻撃](../Page/DoS攻撃.md "wikilink")に利用される可能性のある脆弱性が過去に発見されたことがある\[2\]\[3\]\[4\]ため、およびIGMPには認証機構が無いために、攻撃者がマルチキャストを用いて帯域を占有するDoS攻撃を行う恐れがある\[5\]ためか、。

## プロトコルの詳細

技術的詳細については、RFC\[6\]をご覧ください。

IGMPで定義されるパケットは三種類である。

  - **Membership Query** (Type 0x11)
    ホストがマルチキャストのグループへ参加するときにルータに送信される。参加しているグループの最新の状態を知りたいときにも送信される。
  - **Membership Report** (Type 0x12 (IGMPv1), Type 0x16 (v2), Type 0x22 (v3))
    Membership QueryやLeave Groupの返答として、ホストの参加しているグループの状態をルータが通知するパケット。
  - **Leave Group** (Type 0x17)
    グループからの離脱をルータに通知するパケット。

### Membership Query パケット

| bit offset | 0–3           | 4        | 5–7                                    | 8–15 | 16–31         |
| ---------- | ------------- | -------- | -------------------------------------- | ---- | ------------- |
| 0          | パケットの型 (0x11) | 応答時間の締切り | [チェックサム](../Page/チェックサム.md "wikilink") |      |               |
| 32         | グループのアドレス     |          |                                        |      |               |
| 64         | 予約領域 (0)      | S        | QRV                                    | QQIC | ソースアドレスの数 (N) |
| 96         | ソースアドレス \[1\] |          |                                        |      |               |
| 128        | ソースアドレス \[2\] |          |                                        |      |               |
|            | . . .         |          |                                        |      |               |
|            | ソースアドレス \[N\] |          |                                        |      |               |

IGMPv3 Membership Query パケット

64ビット以降はIGMPv3以降で新たに付け加えられた。

ある特定のホストが送信するマルチキャストのパケットのみを受信したい場合、グループアドレスにPIM-SSM用グローバルアドレスに割り当てられた範囲の中からIPアドレスを一つ指定し、ソースアドレスに送信元ホストのIPアドレスを指定する。この機能とPIM-SSMを併用することで、ホスト毎にグループアドレスをあらかじめ割り当てることなく、疎なマルチキャスティング（ネットワークのノード数に比べて、マルチキャストチャンネル一つあたりの受信ノードが少ない場合）においても効率的な伝送ができる。

この機能を使わない場合は、ソースアドレスの数に0を指定する。この場合、参加するグループアドレス宛のパケットは送信元ホストに関わらず、全てのパケットが受信される。

### Membership Report パケット

| bit offset | 0–7             | 8–15                 | 16–31                                  |
| ---------- | --------------- | -------------------- | -------------------------------------- |
| 0          | パケットの型          | 予約領域 (0)             | [チェックサム](../Page/チェックサム.md "wikilink") |
| 32         | 予約領域 (0)        | ホストが参加しているグループの数 (N) |                                        |
| 64         | グループ\[1\]への参加状態 |                      |                                        |
|            | . . .           |                      |                                        |
|            | グループ\[2\]への参加状態 |                      |                                        |
|            | . . .           |                      |                                        |
|            | . . .           |                      |                                        |
|            | グループ\[N\]への参加状態 |                      |                                        |
|            | . . .           |                      |                                        |
|            |                 |                      |                                        |

IGMP Membership Report パケット

### Leave Group パケット

| bit offset | 0–7           | 8–15     | 16–31                                  |
| ---------- | ------------- | -------- | -------------------------------------- |
| 0          | パケットの型 (0x17) | 応答時間の締切り | [チェックサム](../Page/チェックサム.md "wikilink") |
| 32         | グループのアドレス     |          |                                        |

IGMP Leave Group パケット

## 普及

IPv4やIPv6のマルチキャストは、[専用網](https://ja.wikipedia.org/wiki/専用網 "wikilink")では[IP放送](../Page/IP放送.md "wikilink")のためのネットワークとして商業的に利用されている。

[インターネット](../Page/インターネット.md "wikilink") (the Internet) では、構成しているネットワークのルータがマルチキャストに対応したものに置き換わることはなかった。IPv6網では、ネットワーク機器は当初からすべてMLDに対応しているが、[ISP間レベルでのマルチキャスト経路の構成は実験的に行われているだけである](https://ja.wikipedia.org/wiki/Internet_Service_Provider "wikilink")。

## 脚注

[Category:インターネット層プロトコル](https://ja.wikipedia.org/wiki/Category:インターネット層プロトコル "wikilink") [Category:ネットワーク層プロトコル](https://ja.wikipedia.org/wiki/Category:ネットワーク層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  [RFC 1112](http://www.ietf.org/rfc/rfc1112.txt) (IGMPv1), [RFC 2236](http://www.ietf.org/rfc/rfc2236.txt) (IGMPv2), [RFC 3376](http://www.ietf.org/rfc/rfc3376.txt) (IGMPv3), [RFC 4604](http://www.ietf.org/rfc/rfc4604.txt) (IGMPv3, MLDv2のソースリストとPIM-SSMの対応)
2.  Spoofed [IGMP report denial of service](http://www.securityfocus.com/bid/5020/info) vulnerability.
3.  [Fragmented IGMP packet](http://support.microsoft.com/default.aspx?scid=kb;en-us;238329&sd=tech) may promote "Denial of Service" attack.
4.  Microsoft Security Bulletin MS06-007: [Vulnerability in TCP/IP Could Allow Denial of Service (913446)](http://www.microsoft.com/technet/security/Bulletin/MS06-007.mspx).
5.  [IGMP Security Problem Statement and Requirements](http://www.securemulticast.org/GSEC/gsec3_ietf53_SecureIGMP1.pdf#search=%22igmp%20attacks%22).
6.