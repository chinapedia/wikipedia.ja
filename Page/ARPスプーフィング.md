> この記事は[ARP](https://ja.wikipedia.org/wiki/ARP)から翻訳されています。


[ARP_Spoofing.svg](https://ja.wikipedia.org/wiki/File:ARP_Spoofing.svg "fig:ARP_Spoofing.svg")を変更できる\]\] **ARPスプーフィング**（アープスプーフィング）とは、[ARPプロトコルの応答を偽装することにより](../Page/Address_Resolution_Protocol.md "wikilink")、[LAN上で通信機器の](../Page/Local_Area_Network.md "wikilink")[なりすまし](https://ja.wikipedia.org/wiki/なりすまし "wikilink")を行う技法である。

## 概要

ARPとは、[イーサネット](../Page/イーサネット.md "wikilink")において、既知の[IPアドレス](../Page/IPアドレス.md "wikilink")から未知の[MACアドレス](../Page/MACアドレス.md "wikilink")を得るためのプロトコルである。

とあるIPアドレス宛に[パケット](../Page/パケット.md "wikilink")を送信したい場合、まず「このIPアドレスに対応する通信機器はどれか?」という質問を記述したARP要求が[ブロードキャスト](../Page/ブロードキャスト.md "wikilink")で発信され、該当する[ノードがARP応答で](https://ja.wikipedia.org/wiki/ノード_\(ネットワーク\) "wikilink")「そのIPアドレスに対応するMACアドレスは私である」と[ユニキャスト](https://ja.wikipedia.org/wiki/ユニキャスト "wikilink")で答える。これによりIPアドレスとMACアドレスの対応付けが実現し、以降はそのMACアドレスを宛先とする通信が行なわれることとなる。

イーサネットは、この仕組みによって作成されたARPテーブル(アドレス対照表)を信じる事で成り立っているので、このARPの応答を偽装することにより誤ったARPテーブルを覚え込ませてしまえば、異なる通信機器へパケットを流す事が可能となる。すなわち、機器のなりすましができてしまい特に[ルーター](../Page/ルーター.md "wikilink")になりすますとLANから[WANへの通信をことごとく](../Page/Wide_Area_Network.md "wikilink")[盗聴](https://ja.wikipedia.org/wiki/盗聴 "wikilink")することができることになる。

一般に、LANに使う[ハブに](https://ja.wikipedia.org/wiki/ハブ_\(ネットワーク機器\) "wikilink")、単純なハブではなくスイッチ/ブリッジ機能を持つものを導入すれば、盗聴に対して強固となると言われているが、上記の手法を用いれば、[スイッチド・ネットワーク](https://ja.wikipedia.org/wiki/スイッチド・ネットワーク "wikilink")においてもその危険性は存在する。

## 関連項目

  - [DNSスプーフィング](https://ja.wikipedia.org/wiki/DNSスプーフィング "wikilink")

  - [IPスプーフィング](https://ja.wikipedia.org/wiki/IPスプーフィング "wikilink")

  -
  -
[Category:詐称](https://ja.wikipedia.org/wiki/Category:詐称 "wikilink") [Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink")