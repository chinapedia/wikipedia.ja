> この記事は[MACアドレス](https://ja.wikipedia.org/wiki/MACアドレス)から翻訳されています。


**MACアドレス**（マック・アドレス、）とは、[ネットワーク上で](../Page/コンピュータネットワーク.md "wikilink")、各[ノードを識別するために設定されている](https://ja.wikipedia.org/wiki/ノード_\(ネットワーク\) "wikilink")[LANカード](https://ja.wikipedia.org/wiki/LANカード "wikilink")などのネットワーク機器の[ハードウェア](../Page/ハードウェア.md "wikilink")に（原則として）一意に割り当てられる物理アドレスである。[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")でいえば、第2層（[データリンク層](../Page/データリンク層.md "wikilink")）[Media Access Controlのアドレスにあたる](../Page/媒体アクセス制御.md "wikilink")。

## 概要

[Windowsの](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[コマンドプロンプト](../Page/コマンドプロンプト.md "wikilink")ではPhysical Addressと表記されており、単に**物理アドレス**と呼ばれたり**Node ID**（ノードID）の別名でも呼ばれたりすることがある。

[イーサネット](../Page/イーサネット.md "wikilink")の場合、48[ビット](../Page/ビット.md "wikilink")（EUI-48）の符号である。MACアドレスの表現には、04-A3-43-5F-43-23や32:61:3C:4E:B6:05といった[オクテットで区切り](https://ja.wikipedia.org/wiki/オクテット_\(コンピュータ\) "wikilink")16進数表現を用いる。 このMACアドレスの6つのオクテットのうち、最初の3オクテットがベンダーID部、次の1オクテットが機種ID、最後の2オクテットがシリアルIDとなることが一般的である。この場合、上位4オクテットでネットワーク機器の機種名まで特定可能である。

## グローバルアドレスとローカルアドレス

先頭[オクテットのビット](../Page/8ビット.md "wikilink")0x02がグローバルアドレスとローカルアドレスを識別するビットで、GLビットと呼ばれる。OFFであればグローバルアドレス、ONであればローカルアドレスであることを示している。また、先頭オクテットのビット0x01がユニキャストとマルチキャストを識別するビットで、IGビットと呼ばれる。詳細は、英文記事の[MAC address\#Address detailsを参照](https://ja.wikipedia.org/wiki/:en:MAC_address#Address_details "wikilink")。

グローバルアドレスの場合、世界中のMACアドレスの管理を行なっている[IEEE](../Page/IEEE.md "wikilink")に料金を支払って、割り当てと登録を受けている。上位3オクテットは**OUI**（Organizationally Unique Identifier）と呼ばれる\[1\]。**OUI**を割り当てられた各製造者は下位3オクテットを独自に重複しないように割り当てており、1つのOUIの割り当てを受けることで1677万7216個の製品に個別のMACアドレスが割り振れる。この仕組みにより、原則として、MACアドレスは世界中で唯一の番号となる。IEEEではOUIの登録データをWebで検索できるようにしている。

[IPv4](../Page/IPv4.md "wikilink")では、MACアドレスと[IPアドレス](../Page/IPアドレス.md "wikilink")の相互変換には、[ARPや](../Page/Address_Resolution_Protocol.md "wikilink")[RARPという](../Page/Reverse_address_resolution_protocol.md "wikilink")[プロトコルを用いる](../Page/通信プロトコル.md "wikilink")。[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")では、MACアドレスと[IPアドレスの相互変換には](https://ja.wikipedia.org/wiki/IPv6アドレス "wikilink")、[ICMPv6で規定されている](../Page/Internet_Control_Message_Protocol_for_IPv6.md "wikilink")[近隣探索プロトコル](../Page/近隣探索プロトコル.md "wikilink")（Neighbor discovery, NDP）を用いる。

## 変更と重複

MACアドレスは物理アドレスと呼ばれるが、ソフトウェアの設定により変更可能なネットワーク機器も存在する。また、[仮想マシン](https://ja.wikipedia.org/wiki/仮想マシン "wikilink")などでは任意の値に変更できる場合もある。このため、[無線LAN](../Page/無線LAN.md "wikilink")などの情報セキュリティの確保のために、MACアドレス・フィルタリングを利用する場合、ブラックリストによる防御は突破される可能性がある。

このようにMACアドレスは変更可能なため、MACアドレスが重複することがある。MACアドレスが重複すると正常な通信ができない。

また、[DHCPなど](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")、MACアドレスを装置の識別に使用する場合もMACアドレスが重複すると意図しない動作となることがある。特に管理用途でMACアドレスを使う場合は、同一セグメントに限らず重複が問題となることがある。

## 枯渇の可能性

MACアドレスが有限の符号である以上、理論的には枯渇というものが考えられる。しかし、[IPアドレス枯渇問題](../Page/IPアドレス枯渇問題.md "wikilink")などで話題になる[IPv4](../Page/IPv4.md "wikilink")と違い、MACアドレスは2<sup>48</sup>=281,474,976,710,656個（IGビット/GLビットを除外すると2<sup>46</sup>=70,368,744,177,664≒70兆個）と多いことなどにより、2012年時点では差し迫った問題にはなっていない。

## MACアドレステーブル

[L2スイッチ](https://ja.wikipedia.org/wiki/L2スイッチ "wikilink")などの通信機器では、通信機器のポートと、そのポートに接続される相手の通信機器のMACアドレスのマッピング情報を「**MACアドレステーブル**」に保存している。

## 出典

<references />

## 関連項目

  - [ARP](../Page/Address_Resolution_Protocol.md "wikilink")
  - [媒体アクセス制御](../Page/媒体アクセス制御.md "wikilink")
  - [World Wide Name](https://ja.wikipedia.org/wiki/World_Wide_Name "wikilink")
  - [イーサネット](../Page/イーサネット.md "wikilink")
  - [ルーター](../Page/ルーター.md "wikilink")
  - [ブリッジ (ネットワーク機器)](../Page/ブリッジ_\(ネットワーク機器\).md "wikilink")

## 外部リンク

  - [IEEE OUI検索ページ](http://standards.ieee.org/develop/regauth/oui/public.html)
  - [NICベンダーID一覧](http://hp.vector.co.jp/authors/VA007619/NICID.Htm) - 非公式なOUIを含む一覧。本文にあるようにIEEEに登録されていないOUIというものが存在する、そのような厄介なベンダ製のNICを調査するためのリスト。

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:ネットワークのアドレス](https://ja.wikipedia.org/wiki/Category:ネットワークのアドレス "wikilink")

1.  [日経NETWORK](https://ja.wikipedia.org/wiki/日経NETWORK "wikilink") 2006年9月号「ネットワークの基礎 MACアドレス」p.82