> この記事は[Open vSwitch](https://ja.wikipedia.org/wiki/Open_vSwitch)から翻訳されています。


**Open vSwitch(OVS)**は、分散仮想[マルチレイヤスイッチの](../Page/レイヤ4スイッチ.md "wikilink")[オープンソース実装である](../Page/オープンソースソフトウェア.md "wikilink")。 Open vSwitch の主な目的は、 [ハードウェア仮想化](https://ja.wikipedia.org/wiki/ハードウェア仮想化 "wikilink")環境に[スイッチングスタックを提供すると同時に](../Page/スイッチングハブ.md "wikilink")、 [コンピューターネットワークで使用される複数のプロトコルと標準をサポートすることである](../Page/コンピュータネットワーク.md "wikilink")\[1\]。

このプロジェクトの[ソースコード](../Page/ソースコード.md "wikilink")は、 [Apache License 2.0ライセンスに基づいて配布されている](../Page/Apache_License.md "wikilink")。

## 概要

[右仮想ネットワークスイッチとして展開され](https://ja.wikipedia.org/wiki/ファイル:Distributed_Open_vSwitch_instance.svg "wikilink")、複数の物理サーバに透過的に分散されたOpen vSwitch\[2\] \]\] Open vSwitch は、 [仮想多層](../Page/仮想化.md "wikilink")[ネットワークスイッチのソフトウェア実装であり](../Page/スイッチングハブ.md "wikilink")、プログラムによる拡張を通じて効果的なネットワーク自動化を可能にするように設計されており、標準の管理[インタフェースや](../Page/インタフェース_\(情報技術\).md "wikilink")、[NetFlow](https://ja.wikipedia.org/wiki/NetFlow "wikilink")、[sFlow](https://ja.wikipedia.org/wiki/sFlow "wikilink")、SPAN、[RSPAN](https://ja.wikipedia.org/wiki/ポートミラーリング "wikilink")、[CLI](../Page/キャラクタユーザインタフェース.md "wikilink")、[LACP](https://ja.wikipedia.org/wiki/リンクアグリゲーション "wikilink")、[802.1ag](https://ja.wikipedia.org/wiki/802.1ag "wikilink") 等のプロトコルをサポートしている。さらに、Open vSwitch は、[VMware](../Page/VMware.md "wikilink") vNetwork 分散vswitch または[Cisco](../Page/シスコシステムズ.md "wikilink") Nexus 1000Vと同様に、基盤となるサーバ[アーキテクチャを抽象化する方法でクロスサーバスイッチを作成できるようにすることで](../Page/コンピュータ・アーキテクチャ.md "wikilink")、複数の物理サーバ間で透過的な分散をサポートするように設計されている\[3\]\[4\]\[5\]。

Open vSwitch は、[仮想マシン](../Page/仮想機械.md "wikilink")(VM)[ハイパーバイザ](../Page/ハイパーバイザ.md "wikilink")内で実行されるソフトウェアベースのネットワークスイッチおよび専用スイッチングハードウェアの制御スタックとして動作できる。そのため、複数の仮想化プラットフォーム、スイッチングチップセット、およびネットワーク[ハードウェアアクセラレータに](../Page/ハードウェアアクセラレーション.md "wikilink")[移植された](../Page/移植_\(ソフトウェア\).md "wikilink")\[6\]。バージョン6.0以降の[Citrix XenServer仮想化プラットフォーム](https://ja.wikipedia.org/wiki/Citrix_XenServer "wikilink")\[7\]と、XAPI 管理ツールスタックを介した[Xen クラウドプラットフォームのデフォルトのネットワークスイッチである](../Page/Xen_\(仮想化ソフトウェア\).md "wikilink")\[8\]。また、[Xen](../Page/Xen_\(仮想化ソフトウェア\).md "wikilink")、[Linux](../Page/Linux.md "wikilink") [KVM](https://ja.wikipedia.org/wiki/Kernel-based_Virtual_Machine "wikilink")、[Proxmox VE](https://ja.wikipedia.org/wiki/Proxmox_VE_\(仮想化プラットフォーム\) "wikilink")、[VirtualBox](../Page/VirtualBox.md "wikilink")[ハイパーバイザ](../Page/ハイパーバイザ.md "wikilink")をサポートし、[Hyper-V](../Page/Hyper-V.md "wikilink")へのポートも利用できる\[9\]。また、[OpenStack](https://ja.wikipedia.org/wiki/OpenStack "wikilink")、[openQRM](https://ja.wikipedia.org/wiki/OpenQRM "wikilink")、[OpenNebula](https://ja.wikipedia.org/wiki/OpenNebula "wikilink")と[oVirt](https://ja.wikipedia.org/wiki/OVirt "wikilink") 等の様々な統合された[クラウドコンピューティング](https://ja.wikipedia.org/wiki/クラウドコンピューティング "wikilink")を含むソフトウェアプラットフォームおよび仮想化管理システムを持つ\[10\]\[11\]。

Open vSwitch の[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")実装は、2012年3月18日にリリースされたカーネルバージョン3.3の[カーネルメインラインにマージされた](../Page/Linuxカーネル.md "wikilink")\[12\]\[13\]。[Debian](../Page/Debian.md "wikilink")、[Fedora](../Page/Fedora.md "wikilink")、[openSUSE](https://ja.wikipedia.org/wiki/openSUSE "wikilink")、[Ubuntu](../Page/Ubuntu.md "wikilink")の公式Linuxディストリビューションで利用可能である\[14\]。2014年1月、[FreeBSD](../Page/FreeBSD.md "wikilink")と[NetBSD](../Page/NetBSD.md "wikilink")の実装も利用でき、[NetBSD](../Page/NetBSD.md "wikilink")の実装は完全な[ユーザ空間で動作する](https://ja.wikipedia.org/wiki/ユーザー空間 "wikilink")\[15\]\[16\]\[17\]。

Open vSwitch のソースコードの大部分は、[プラットフォームに依存しない](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")[C言語](../Page/C言語.md "wikilink")で記述されているため、さまざまな環境への[移植が容易である](../Page/移植_\(ソフトウェア\).md "wikilink")。ソースコードは、[Apache License 2.0の下でライセンスされている](../Page/Apache_License.md "wikilink")\[18\]。

## 機能

、Open vSwitch によって提供される機能を次に示す\[19\]\[20\]:

  - [NetFlow](https://ja.wikipedia.org/wiki/NetFlow "wikilink")、[sFlow](https://ja.wikipedia.org/wiki/sFlow "wikilink")、 [IPフロー情報エクスポート](https://ja.wikipedia.org/wiki/IPフロー情報のエクスポート "wikilink")(IPFIX)、[スイッチドポートアナライザ](https://ja.wikipedia.org/wiki/ポートミラーリング "wikilink")(SPAN)、[リモートスイッチドポートアナライザ](https://ja.wikipedia.org/wiki/ポートミラーリング "wikilink")(RSPAN)、および[Generic Routing Encapsulation](https://ja.wikipedia.org/wiki/ジェネリックルーティングカプセル化 "wikilink")(GRE)を使用してトンネルされた[ポートミラーを介した](https://ja.wikipedia.org/wiki/ポートミラーリング "wikilink")、仮想マシン間の公開された通信
  - [リンクアグリゲーション](https://ja.wikipedia.org/wiki/リンクアグリゲーション "wikilink")によるリンクアグリゲーション管理プロトコル(LACP、[IEEE 802.1AX](https://ja.wikipedia.org/wiki/リンクアグリゲーション "wikilink")-2008）
  - ネットワークパーティショニング用の標準の[802.1Q](https://ja.wikipedia.org/wiki/IEEE_802.1Q "wikilink")[仮想LAN](../Page/Virtual_Local_Area_Network.md "wikilink")(VLAN)モデルによる[トランキング](https://ja.wikipedia.org/wiki/トランキング "wikilink")をサポート
  - [インターネットグループ管理プロトコル](../Page/Internet_Group_Management_Protocol.md "wikilink")(IGMP)のバージョン1、2、3を使用した[マルチキャストスヌーピングのサポート](https://ja.wikipedia.org/wiki/IGMPスヌーピング "wikilink")
  - [Shortest Path Bridging Media Access Control](https://ja.wikipedia.org/wiki/IEEE_802.1aq "wikilink")(SPBM)のサポート、および[Link Layer Discovery Protocol](https://ja.wikipedia.org/wiki/リンク層発見プロトコル "wikilink")(LLDP)関連の基本サポート
  - Bidirectional Forwarding Detection(BFD)および[802.1ag](https://ja.wikipedia.org/wiki/802.1ag "wikilink")リンクモニタリングのサポート
  - [スパニングツリープロトコル](../Page/スパニングツリープロトコル.md "wikilink")(STP、[IEEE 802.1D](https://ja.wikipedia.org/wiki/IEEE_802.1D "wikilink")-1998)および[高速スパニングツリープロトコル](../Page/スパニングツリープロトコル.md "wikilink")(RSTP、[IEEE 802.1D](https://ja.wikipedia.org/wiki/IEEE_802.1D "wikilink")-2004)のサポート
  - さまざまなアプリケーション、ユーザ、またはデータ[トラフィックフローに対するきめ細かな](https://ja.wikipedia.org/wiki/フロー（コンピューターネットワーク） "wikilink")[QoS制御](../Page/Quality_of_Service.md "wikilink")
  - [階層的フェアサービスカーブ](https://ja.wikipedia.org/wiki/階層的公正サービス曲線 "wikilink") (HFSC)[キューイング規則](https://ja.wikipedia.org/wiki/ネットワーク・スケジューラ "wikilink")(qdisc)のサポート
  - [仮想マシン](../Page/仮想機械.md "wikilink")(VM)[インタフェースレベルでの](../Page/インタフェース_\(情報技術\).md "wikilink")[トラフィックポリシング](https://ja.wikipedia.org/wiki/トラフィックポリシング（通信） "wikilink")
  - [ネットワークインターフェイスコントローラ](../Page/ネットワークカード.md "wikilink")(NIC)[ボンディング](https://ja.wikipedia.org/wiki/リンクアグリゲーション "wikilink")、[MACソースアドレス](../Page/媒体アクセス制御.md "wikilink")、アクティブバックアップ、および[レイヤー4](../Page/トランスポート層.md "wikilink")[ハッシュによる](../Page/ハッシュ関数.md "wikilink")[サーバロードバランシング](../Page/サーバロードバランス.md "wikilink")
  - さまざまな仮想化関連の拡張機能を含む、[OpenFlow](https://ja.wikipedia.org/wiki/OpenFlow "wikilink")プロトコルのサポート
  - 完全な[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")サポート
  - [Generic Routing Encapsulation](https://ja.wikipedia.org/wiki/ジェネリックルーティングカプセル化 "wikilink")(GRE)、[Virtual Extensible LAN](../Page/Virtual_Extensible_LAN.md "wikilink")(VXLAN)、ステートレストランスポートトンネリング(STT)、Geneve 等の複数の[トンネリング](../Page/トンネリング.md "wikilink")プロトコルのサポート、および[インターネットプロトコルセキュリティ](../Page/IPsec.md "wikilink")(IPsec)レイヤの追加サポート
  - [C言語](../Page/C言語.md "wikilink")および[Python](../Page/Python.md "wikilink")プログラミング言語用の既存の[バインディングを備えたリモート構成プロトコル](../Page/束縛_\(情報工学\).md "wikilink")
  - [カーネル空間または](https://ja.wikipedia.org/wiki/ユーザー空間 "wikilink")[ユーザ空間にパケット転送エンジンを実装し](https://ja.wikipedia.org/wiki/ユーザー空間 "wikilink")、[カーネル空間を離れることなく転送されたパケットの大部分を処理し](https://ja.wikipedia.org/wiki/ユーザー空間 "wikilink")、[マルチスレッド](../Page/スレッド_\(コンピュータ\).md "wikilink")[カーネル空間と](https://ja.wikipedia.org/wiki/ユーザー空間 "wikilink")[ユーザ空間](https://ja.wikipedia.org/wiki/ユーザー空間 "wikilink")[コンポーネントを使用することにより](../Page/ソフトウェアコンポーネント.md "wikilink")、柔軟性を向上させ、パフォーマンスを向上させる\[21\]\[22\]
  - フローキャッシュエンジンを備えたマルチテーブル転送パイプライン
  - 転送レイヤーの抽象化により、Open vSwitch を新しいソフトウェアおよびハードウェア[プラットフォームに簡単に](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")[移植できる](../Page/移植_\(ソフトウェア\).md "wikilink")

## 参考

  - [分散オーバーレイ仮想イーサネット](https://ja.wikipedia.org/wiki/分散オーバーレイ仮想イーサネット "wikilink")(DOVE)
  - [LANスイッチング](../Page/スイッチングハブ.md "wikilink")
  - [ネットワーク機能仮想化](https://ja.wikipedia.org/wiki/ネットワーク機能仮想化 "wikilink")(NFV)
  - [オーバーレイトランスポート仮想化](https://ja.wikipedia.org/wiki/オーバーレイトランスポート仮想化 "wikilink")(OTV)
  - [ソフトウェア定義ネットワーク](https://ja.wikipedia.org/wiki/Software_Defined_Networking "wikilink")(SDN)

## 脚注

## 外部リンク

  -
  - 、2013年12月15日

  - , 2013年11月8日

  - [OVN, Bringing Native Virtual Networking to OVS](http://networkheresy.com/2015/01/13/ovn-bringing-native-virtual-networking-to-ovs/), 2015年1月13日, by Justin Pettit, Ben Pfaff, Chris Wright, and Madhu Venugopal

  - [Open Virtual Network (OVN) Proposed Architecture](https://web.archive.org/web/20151110133423/http://openvswitch.org/pipermail/dev/2015-January/050380.html), 2015年1月13日、by Ben Pfaff

  - [6WIND Announces Open vSwitch Acceleration for Red Hat Enterprise Linux OpenStack Platform](http://www.prweb.com/releases/2014/04/prweb11768622.htm), 2014年4月16日

  - [Going With the Flow：Google's Secret Switch to the Next Wave of Networking](https://www.wired.com/2012/04/going-with-the-flow-google/) ,*[Wired](../Page/WIRED_\(雑誌\).md "wikilink")* , 2012年4月17日, by Steven Levy

  - [Performance Characteristics of Virtual Switching](http://www.net.in.tum.de/fileadmin/bibtex/publications/papers/Open-vSwitch-CloudNet-14.pdf), [IEEE](../Page/IEEE.md "wikilink"), 2014, by Paul Emmerich, Daniel Raumer, Florian Wohlfart, Georg Carle

[Category:フリーソフトウェア](https://ja.wikipedia.org/wiki/Category:フリーソフトウェア "wikilink") [Category:プログラミング言語別ソフトウェア](https://ja.wikipedia.org/wiki/Category:プログラミング言語別ソフトウェア "wikilink") [Category:C言語](https://ja.wikipedia.org/wiki/Category:C言語 "wikilink") [Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink")

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
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.