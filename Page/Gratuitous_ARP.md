> この記事は[Gratuitous ARP](https://ja.wikipedia.org/wiki/Gratuitous_ARP)から翻訳されています。


**Gratuitous ARP** (**GARP**)は[ARPの一つで](../Page/Address_Resolution_Protocol.md "wikilink")、ARP[パケット](../Page/パケット.md "wikilink")の送信元[ホスト自身の](https://ja.wikipedia.org/wiki/ホスト_\(ネットワーク\) "wikilink")[IPアドレス](../Page/IPアドレス.md "wikilink")に対するARP（[IPアドレス](../Page/IPアドレス.md "wikilink")に対応する[MACアドレス](../Page/MACアドレス.md "wikilink")の取得）である。

主に、[ホストに](https://ja.wikipedia.org/wiki/ホスト_\(ネットワーク\) "wikilink")[IPアドレス](../Page/IPアドレス.md "wikilink")を割り当てる際に、他のホストがすでに同じIPアドレスを使用していないか確認したり、相手の通信機器の[ARPテーブル](https://ja.wikipedia.org/wiki/ARPテーブル "wikilink")に送信元ホストのIPアドレスとMACアドレスを追加させるために使用する。（[DHCP](https://ja.wikipedia.org/wiki/DHCP "wikilink")により[IPアドレス](../Page/IPアドレス.md "wikilink")を配布された後、当該IPアドレスが既に利用されていないかを確認する場合に用いる）ARP本来の目的である相手の接続機器の[IPアドレス](../Page/IPアドレス.md "wikilink")に対する[MACアドレス](../Page/MACアドレス.md "wikilink")の取得のために使用するわけではない。

通常のARPパケットと異なっている点は Target Protocol AddressフィールドがARPパケットを送出したホストに割り当てられたもの、もしくは割り当てられようとしているものが設定されている点である。 Sender Protocol Addressフィールドは Target Protocol Addressフィールドと同じIPアドレスが設定されていることが多いが、必ずこのようになっているわけではない。

もし、IPアドレスを設定する際に他のホストが既に同じIPアドレスを持っていると、そのホストがARP Operation がARP RequestであるGratuitous ARPを受信した際にGratuitous ARPを送信したホストに対してARP Replyを返送する。そのため、この Gratuitous ARPに対する返信の有無でIPアドレスの重複を確認することができる。

また、[VRRPや](../Page/Virtual_Router_Redundancy_Protocol.md "wikilink")[Mobile IPでもGratuitous](../Page/Mobile_IP.md "wikilink") ARPが使用されるが、これはIPアドレスの重複確認ではなく同一セグメント上のネットワーク機器上のARPキャッシュやL3テーブルを更新することでIPアドレスと機器の対応関係の更新を強制的におこなわせることを目的としている。

なお、Gratuitous ARPではARPパケットのOperation フィールドにARP RequestとARP Replyのいずれも用いることができるが、アドレス重複確認を目的としてGratuitous ARPを使用する際にはARP Requestが用いられることが多い。

## 関連項目

  - [ARP](../Page/Address_Resolution_Protocol.md "wikilink")(Address Resolution Protocol) - [IPアドレス](../Page/IPアドレス.md "wikilink")から[MACアドレス](../Page/MACアドレス.md "wikilink")に変換する[プロトコル](../Page/プロトコル.md "wikilink")
  - [Mobile IP](../Page/Mobile_IP.md "wikilink")
  - [VRRP](../Page/Virtual_Router_Redundancy_Protocol.md "wikilink")

## 外部リンク

  - [RFC5227 "IPv4 Address Conflict Detection"](http://www.ietf.org/rfc/rfc5227.txt) ([日本語訳](http://www.kasai.fm/wiki/rfc5227jp))

[Category:リンク層プロトコル](https://ja.wikipedia.org/wiki/Category:リンク層プロトコル "wikilink")