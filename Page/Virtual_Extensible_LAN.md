> この記事は[Virtual Extensible LAN](https://ja.wikipedia.org/wiki/Virtual_Extensible_LAN)から翻訳されています。


**Virtual Extensible LAN**(**VXLAN**)とは、大規模な[クラウドコンピューティング](https://ja.wikipedia.org/wiki/クラウドコンピューティング "wikilink")導入に関連する[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")問題に対処しようとする[ネットワーク仮想化](https://ja.wikipedia.org/wiki/ネットワーク仮想化 "wikilink")技術である。[VLANのような](../Page/Virtual_Local_Area_Network.md "wikilink")[カプセル化技術を使用して](https://ja.wikipedia.org/wiki/カプセル化_\(通信\) "wikilink")、[IANA割り当てとしてUDPポート番号](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")4789番をデフォルトとして使用し、[OSI](../Page/OSI参照モデル.md "wikilink")[レイヤー2](../Page/データリンク層.md "wikilink")/[イーサネットフレーム](https://ja.wikipedia.org/wiki/イーサネットフレーム "wikilink")を[レイヤー4](../Page/トランスポート層.md "wikilink")/[UDPデータグラム内に](../Page/User_Datagram_Protocol.md "wikilink")[カプセル化する](https://ja.wikipedia.org/wiki/カプセル化_\(通信\) "wikilink")\[1\]。VXLAN トンネルを終端し、仮想または物理[スイッチポートのいずれかであるVXLAN](../Page/スイッチングハブ.md "wikilink") エンドポイントは、**VXLANトンネルエンドポイント**(**VTEP**)と呼ばれる\[2\]\[3\]。

VXLAN は、オーバーレイカプセル化プロトコルを標準化する取り組みの進化形である。これにより、最大約1600万の論理ネットワークの[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")が向上し、IPネットワーク全体での[レイヤー2隣接が可能になる](../Page/データリンク層.md "wikilink")。ヘッドエンドレプリケーション(HER)を使用した[マルチキャスト](../Page/マルチキャスト.md "wikilink")または[ユニキャスト](https://ja.wikipedia.org/wiki/ユニキャスト "wikilink")は、[ブロードキャスト](../Page/ブロードキャスト.md "wikilink")、[不明なユニキャスト](https://ja.wikipedia.org/wiki/ユニキャストフラッド "wikilink")、およびマルチキャスト(BUM)トラフィックをフラッディングするために使用される\[4\]。

VXLAN 仕様は、当初、[VMware](../Page/VMware.md "wikilink")、[Arista Networks](https://ja.wikipedia.org/wiki/アリスタネットワークス "wikilink")、および[Ciscoによって作成された](../Page/シスコシステムズ.md "wikilink")\[5\]\[6\] 。VXLAN は、[Huawei](../Page/ファーウェイ.md "wikilink")\[7\]、[Broadcom](../Page/ブロードコム.md "wikilink")、[Citrix](../Page/シトリックス・システムズ.md "wikilink")、[Pica8](https://ja.wikipedia.org/wiki/Pica8 "wikilink")、[Big Switch Networks](https://ja.wikipedia.org/wiki/大きなスイッチネットワーク "wikilink")、[Cumulus Networks](https://ja.wikipedia.org/wiki/積雲ネットワーク "wikilink")、[Dell EMC](../Page/Dell_EMC.md "wikilink")、[Ericsson](../Page/エリクソン.md "wikilink")、[Mellanox](https://ja.wikipedia.org/wiki/メラノックス "wikilink")\[8\]、[FreeBSD](../Page/FreeBSD.md "wikilink")\[9\]、[OpenBSD](../Page/OpenBSD.md "wikilink")\[10\]、[Red Hat](../Page/レッドハット.md "wikilink")\[11\]、 [Joyent](https://ja.wikipedia.org/wiki/Joyent "wikilink")、[ジュニパーネットワークス](../Page/ジュニパーネットワークス.md "wikilink")が技術支援している。

VXLAN はRFC 7348で[IETFによって正式に文書化された](../Page/Internet_Engineering_Task_Force.md "wikilink")。VXLAN はMAC-in-UDPパケット[カプセル化モードを使用して](https://ja.wikipedia.org/wiki/カプセル化_\(通信\) "wikilink")、オブジェクトの一部のコンポーネントへの直接アクセスを制限する\[12\]。

[Open vSwitchは](../Page/Open_vSwitch.md "wikilink")、VXLAN オーバーレイネットワークをサポートするソフトウェアベースの仮想[ネットワークスイッチの例である](../Page/スイッチングハブ.md "wikilink")。

## 参考

  - [Distributed Overlay Virtual Ethernet](https://ja.wikipedia.org/wiki/Distributed_Overlay_Virtual_Ethernet "wikilink") (DOVE)
  - [Ethernet VPN](https://ja.wikipedia.org/wiki/Ethernet_VPN "wikilink") (EVPN)
  - [GENEVE](https://ja.wikipedia.org/wiki/GENEVE "wikilink"), an industry effort to unify both VXLAN and NVGRE technologies
  - [Generic Routing Encapsulation](https://ja.wikipedia.org/wiki/Generic_Routing_Encapsulation "wikilink") (GRE)
  - [IEEE 802.1ad](https://ja.wikipedia.org/wiki/IEEE_802.1ad "wikilink"), an Ethernet networking standard, also known as provider bridging, Stacked VLANs, or simply QinQ.
  - [NVGRE](https://ja.wikipedia.org/wiki/NVGRE "wikilink"), a similar competing specification
  - [Overlay Transport Virtualization](https://ja.wikipedia.org/wiki/Overlay_Transport_Virtualization "wikilink") (OTV)
  - [Virtual LAN](https://ja.wikipedia.org/wiki/Virtual_LAN "wikilink") (VLAN)
  - [Layer 2 Tunneling Protocol](../Page/Layer_2_Tunneling_Protocol.md "wikilink") (L2TP)

## 脚注

## 外部リンク

  - [VXLANとは](https://www.infraexpert.com/study/virtual3.html)

  -
  - [VXLANの詳細: パート1](http://www.definethecloud.net/vxlan-deep-dive/)と[パート2](http://www.definethecloud.net/vxlan-deep-divepart-2/)、2012年11月、Joe Onisick著

[Category:トンネリング](https://ja.wikipedia.org/wiki/Category:トンネリング "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.