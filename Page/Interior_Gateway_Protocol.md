> この記事は[Interior Gateway Protocol](https://ja.wikipedia.org/wiki/Interior_Gateway_Protocol)から翻訳されています。


**Interior Gateway Protocol** (IGP) は、[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")において[AS内部での経路情報の交換に利用される](../Page/自律システム_\(インターネット\).md "wikilink")[ルーティングプロトコル](https://ja.wikipedia.org/wiki/ルーティングプロトコル "wikilink")の総称。ベンダーフリー実装である、[RIPや](https://ja.wikipedia.org/wiki/ルーティング・インフォメーション・プロトコル "wikilink")[OSPF](https://ja.wikipedia.org/wiki/オープン・ショーテスト・パス・ファースト "wikilink")、[IS-IS](../Page/IS-IS.md "wikilink")がある他、[シスコシステムズ](../Page/シスコシステムズ.md "wikilink")独自実装である[IGRP](https://ja.wikipedia.org/wiki/IGRP "wikilink")や[EIGRP](https://ja.wikipedia.org/wiki/EIGRP "wikilink")が利用されている。

## IGPの種類

### 距離ベクトル型ルーティングプロトコル

は「[ベルマン–フォード法](https://ja.wikipedia.org/wiki/ベルマン–フォード法 "wikilink")」（アルゴリズム）を使用する。 これらのプロトコルでは、各ルータは、完全な[ネットワーク・トポロジー](../Page/ネットワーク・トポロジー.md "wikilink")に関する情報を持たない。 これらは、ほかのルータとの距離値(DV: distance value)を計算してアドバタイズする。また、ほかのルータからも同様にアドバタイズを受信する。 これらのルーティングアドバタイズを受信すると、各ルータは、自身のルーティングテーブルに組み入れる。 次のアドバタイズサイクルでは、ルータはルーティングテーブルから更新された情報をアドバタイズする。 安定した値に各ルータのルーティングテーブルがするまで、このプロセスが継続される。

これらのプロトコルのは、収束が遅い欠点がある。

距離ベクトル型ルーティングプロトコルの例：

  - [Routing Information Protocol](../Page/Routing_Information_Protocol.md "wikilink") (RIP)
  - [Routing Information Protocol Version 2](https://ja.wikipedia.org/wiki/Routing_Information_Protocol#RIP_version_2 "wikilink") (RIPv2)
  - [Routing Information Protocol Next Generation](https://ja.wikipedia.org/wiki/Routing_Information_Protocol#RIPng "wikilink") (RIPng), [IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")のサポートとRIPバージョン2の延長
  - [Interior Gateway Routing Protocol](https://ja.wikipedia.org/wiki/Interior_Gateway_Routing_Protocol "wikilink") (IGRP)

### リンクステート型ルーティングプロトコル

では、各ルータは、完全な[ネットワーク・トポロジー](../Page/ネットワーク・トポロジー.md "wikilink")に関する情報を持っている。 各ルータは、独立してトポロジのローカルな情報を使用し、ネットワーク内のすべての可能な宛先に、各ルータからの最良のネクスト・ホップを計算する。 最良のネクスト・ホップの集合は、ルーティングテーブルを形成する。

これは、隣のルータと各ノードが共有してルーティングテーブルを作成する「距離ベクトル型ルーティングプロトコル」とは対照的である。 「リンクステート型ルーティングプロトコル」は、ノード間でやり取りされる唯一の情報は、接続マップを構築するために使用される情報である。

リンクステート型ルーティングプロトコルの例：

  - [Open Shortest Path First](../Page/Open_Shortest_Path_First.md "wikilink") (OSPF)
  - [Intermediate system to intermediate system](https://ja.wikipedia.org/wiki/Intermediate_system_to_intermediate_system "wikilink") (IS-IS)

### ハイブリッドルーティングプロトコル

ハイブリッドルーティングプロトコルは、「距離ベクトル型ルーティングプロトコル」および「リンクステート型ルーティングプロトコル」の両方の機能を持っている。 一例として、[Enhanced Interior Gateway Routing Protocol](https://ja.wikipedia.org/wiki/Enhanced_Interior_Gateway_Routing_Protocol "wikilink") (EIGRP)がある。

## 関連項目

  - [EGP](../Page/Exterior_Gateway_Protocol.md "wikilink")
  - [距離ベクトル型ルーティングプロトコル](https://ja.wikipedia.org/wiki/距離ベクトル型ルーティングプロトコル "wikilink")
  - [リンクステート型ルーティングプロトコル](https://ja.wikipedia.org/wiki/リンクステート型ルーティングプロトコル "wikilink")

[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:ルーティングプロトコル](https://ja.wikipedia.org/wiki/Category:ルーティングプロトコル "wikilink")