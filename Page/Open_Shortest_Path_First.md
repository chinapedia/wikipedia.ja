> この記事は[Open Shortest Path First](https://ja.wikipedia.org/wiki/Open_Shortest_Path_First)から翻訳されています。


**Open Shortest Path First** (オープン・ショーテスト・パス・ファースト、略称：**OSPF**) は、小規模から大規模のネットワーク向けのリンクステート型[ルーティングプロトコル](https://ja.wikipedia.org/wiki/ルーティングプロトコル "wikilink")である。

## 概要

[自律システム](../Page/自律システム_\(インターネット\).md "wikilink") (AS) 内の[ルーティング](../Page/ルーティング.md "wikilink")を行う[Interior Gateway Protocol](../Page/Interior_Gateway_Protocol.md "wikilink")（IGP）の[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。 （対して、[自律システム](../Page/自律システム_\(インターネット\).md "wikilink") (AS) 間のルーティングを行う[通信プロトコル](../Page/通信プロトコル.md "wikilink")は[BGP4などの](../Page/Border_Gateway_Protocol.md "wikilink")[EGPである](../Page/Exterior_Gateway_Protocol.md "wikilink")）

[RIPにおける制約を解消するために](https://ja.wikipedia.org/wiki/ルーティング・インフォメーション・プロトコル "wikilink")[IETFにおいて提唱され](../Page/Internet_Engineering_Task_Force.md "wikilink")、スタティック・ルーティングやRIPでは実現できなかった冗長経路構成を容易に実現できる。

OSPFは、[リンクステート型](https://ja.wikipedia.org/wiki/ルーティング#LSA "wikilink")（LSA）の[ルーティング](../Page/ルーティング.md "wikilink")を行う[リンクステート型ルーティングプロトコル](https://ja.wikipedia.org/wiki/リンクステート型ルーティングプロトコル "wikilink")（リンク状態型ルーティング）である。 各ルータは隣接するルータとリンクしてアドバタイズ(周囲に通知)することで[ネットワーク・トポロジー](../Page/ネットワーク・トポロジー.md "wikilink")の[データベース](../Page/データベース.md "wikilink")を構築し、[ダイクストラのアルゴリズムで最短経路ツリーを](../Page/ダイクストラ法.md "wikilink")「**コスト**」という距離（メトリック）の単位で計算して[ルーティング・テーブル](https://ja.wikipedia.org/wiki/ルーティング・テーブル "wikilink")を作成する。

ネットワーク規模の増大に対処するため、OSPFはネットワークを複数のエリアに分割することを可能としており、フラッディングや経路計算をエリアごとに効率よく実現できる。 エリア間の通信は**エリア境界ルータ** (area border router; ABR) を介して行われ、エリア間のルーティングは特定のバックボーン・エリアが中継することで実現される。 またルーティング情報更新の負荷を軽減するため、セグメントごとに**代表ルータ** (designated router; DR) と**バックアップ代表ルータ** (backup designated router; BDR) が選出されハブとして働く。

OSPFv2は[IPv4](../Page/IPv4.md "wikilink")、OSPFv3は[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")にそれぞれ対応している。\[1\]

## 主なRFC

  - RFC 1131 (1989年) - 最初の標準化提案
  - RFC 1584 (1994年) - OSPF マルチキャスト拡張 (MOSPF)
  - RFC 2328 (1998年) - OSPFv2、STD 54 に
  - RFC 3101 (2003年) - OSPF NSSA オプション
  - RFC 3630 (2003年) - OSPF-TE
  - RFC 5340 (2008年) - OSPFv3、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")対応（RFC 2740(1999年)のアップデート）

その他多くの関連RFCがある。

## 出典

<references />

## 関連項目

  - [ルーティングプロトコル](https://ja.wikipedia.org/wiki/ルーティングプロトコル "wikilink")
  - [IS-IS](../Page/IS-IS.md "wikilink")
  - [IEEE 802.1aq](https://ja.wikipedia.org/wiki/IEEE_802.1aq "wikilink") - [Shortest Path Bridging (SPB)](https://ja.wikipedia.org/wiki/Shortest_Path_Bridging "wikilink")
  - [最短経路問題](../Page/最短経路問題.md "wikilink")

## 外部リンク

  - [IETF OSPF WG](http://www.ietf.org/html.charters/ospf-charter.html)
  - [シスコシステムズ](../Page/シスコシステムズ.md "wikilink")、[OSPF デザイン ガイド](http://www.cisco.com/cisco/web/support/JP/102/1020/1020646_1-j.html)

[Category:ルーティングプロトコル](https://ja.wikipedia.org/wiki/Category:ルーティングプロトコル "wikilink") [Category:リンク層プロトコル](https://ja.wikipedia.org/wiki/Category:リンク層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.