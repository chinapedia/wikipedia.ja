> この記事は[Exterior Gateway Protocol](https://ja.wikipedia.org/wiki/Exterior_Gateway_Protocol)から翻訳されています。


**Exterior Gateway Protocol** (EGP) は、[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")の[ルーティングプロトコル](https://ja.wikipedia.org/wiki/ルーティングプロトコル "wikilink")の一つ。

## 概要

[自律システム](../Page/自律システム_\(インターネット\).md "wikilink") (AS) 間の[ルーティング](../Page/ルーティング.md "wikilink")を行うExterior Gateway Protocol (EGP) の[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。

EGPと[BGPの総称としては](../Page/Border_Gateway_Protocol.md "wikilink")**EGPs**と表記する。1984年にRFCとして提案され、1980年代後半にAS間の経路制御に利用されていた。最短経路制御を行うディスタンスベクタ型のルーティングアルゴリズムを採用した。経路収束が遅く、自律システムの管理者の意思でインターネット上を流れるトラフィックの経路をコントロールするポリシーベースルーティングが不可能であった。BGPの提案以後はEGPは急速にBGPに取って代わられた。そのため、1990年代に入る頃には既に使用されなくなっていた。

## 総称としてのEGP

[IGPs](../Page/Interior_Gateway_Protocol.md "wikilink")（[OSPF](https://ja.wikipedia.org/wiki/OSPF "wikilink")、[IS-IS](../Page/IS-IS.md "wikilink")、[EIGRP](https://ja.wikipedia.org/wiki/EIGRP "wikilink")など）は、『ここからあるネットワークへ到達するには、どの**ルータ**を経由してパケットを配送するべきか』に着目してルートの制御を行っている。しかし、いくら大規模ネットワークに対応できる前述のIGPsでも、ルータ単位の制御では、現在の[インターネット](../Page/インターネット.md "wikilink")のような膨大なネットワークを管理することは、[ルーティングテーブル](../Page/ルーティングテーブル.md "wikilink")の[計算量](https://ja.wikipedia.org/wiki/計算量 "wikilink")や[データベース](../Page/データベース.md "wikilink")が巨大化するため非常に困難である。

そこで、インターネットをいくつかの単位に分割して管理するアイデアが考案された。この管理単位は自律システム（Autonomous System、AS）と呼ばれ、外部からは1つのネットワークとして扱われる。IGPsがこのAS内でルーティングを行うのに対し、EGPsではAS間のルーティングを司る。すなわち、『ここからあるネットワークに行くには、どの**ネットワーク**にパケットを転送する』かを主題としたルート制御を行う。

1980年代中頃までは[EGPが利用されていたが](https://ja.wikipedia.org/wiki/#単体のルーティングプロトコルとしてのEGP "wikilink")、現在では主にBGPが利用される。

## 単体のルーティングプロトコルとしてのEGP

## EGPの関連規約

  - RFC 904 - Exterior Gateway Protocol Formal Specification

## 脚注

## 参考文献

  -
## 関連項目

  - [Border Gateway Protocol](../Page/Border_Gateway_Protocol.md "wikilink") (BGP)
  - [Interior Gateway Protocol](../Page/Interior_Gateway_Protocol.md "wikilink") (IGP)

[Category:ルーティングプロトコル](https://ja.wikipedia.org/wiki/Category:ルーティングプロトコル "wikilink") [Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")