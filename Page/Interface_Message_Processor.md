> この記事は[Interface Message Processor](https://ja.wikipedia.org/wiki/Interface_Message_Processor)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:ARPANET_first_router.jpg "wikilink") **Interface Message Processor**（IMP）は、[ネットワーク](../Page/ネットワーク.md "wikilink")間の[パケット](../Page/パケット.md "wikilink")転送を行う装置である。現在の[インターネット](../Page/インターネット.md "wikilink")の根幹を成す[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")の原型に当たるものである。

## 歴史

現在の[インターネット](../Page/インターネット.md "wikilink")の起源に当たる、[1969年](https://ja.wikipedia.org/wiki/1969年 "wikilink")の[ARPANET](../Page/ARPANET.md "wikilink")誕生において、重要な役割を果たした。

1960年代初頭のポール・バランのパケット通信に関する種々の研究成果を受けて、1967年4月にARPAで行われたARPANET Design Sessionにおいて、IMPのアイデアに関する最初の議論が行われ、1969年にARPANETの開発に参加していたローレンス・ロバーツやBBN社のボブ・カーン達により開発された。パケット転送の機構は[ストアアンドフォワード](../Page/ストアアンドフォワード.md "wikilink")型として設計された。また、各ルータは2秒毎に経路情報を送信し、最小のトランジットタイムを持つ経路を評価すると共に、0.5秒毎に経路表を各送信先までのトランジットタイムを最小にするように更新する、動的なルーティング・アルゴリズムも実装された\[1\]。このアルゴリズムもポール・バランが考案したものである。

1969年のIMPの発明後、NCPと呼ばれるプロトコル・スタックの試作が行われた\[2\]。1969年10月29日におけるIMPを用いた通信成功により、世界で初めて異なる組織のネットワークが相互接続され、ARPANETの概念が実証された。この実験が行われた当時のARPANETは極めて脆弱なシステムであり、最初に送信する予定のLOGINという文字列のうち、LとOを伝達し終えた瞬間にシステムがクラッシュしてしまった。1970年にはNCPが本格運用が可能な状態にまで完成された\[3\]。

[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")1月1日には高機能化とスタックの構造の整理を目的とした、[NCPから](../Page/Network_Control_Program.md "wikilink")[TCP/IPへの移行が完了した](../Page/インターネット・プロトコル・スイート.md "wikilink")<ref>J. Postel, <https://www.rfc-editor.org/info/rfc791>, STD 5

RFC 791 Internet Protocol, September 1981. </ref><ref>J. Postel, <https://www.rfc-editor.org/info/rfc801>, RFC 801

NCP/TCP transition plan, November 1981. </ref>。[Internet Protocolが運用され始めたこの時から](../Page/Internet_Protocol.md "wikilink")、技術的な意味でのインターネットが始まったと言える。

1982年にはARPANETにおいて実行されるルーティングプロトコルが、最小のホップ数を持つ経路を計算するディスタンスベクタ型のGGPへと移行し\[4\]、1984年には同じくディスタンスベクタ型の[EGP](https://ja.wikipedia.org/wiki/EGP "wikilink")に移行し<ref>J. Postel, <https://www.rfc-editor.org/info/rfc890>, RFC 890

Exterior Gateway Protocol implementation schedule, February 1984. </ref>、1989年からは各組織のネットワーク管理者のポリシーを反映可能なパスベクタ型の[BGP](https://ja.wikipedia.org/wiki/BGP "wikilink")に移行した\[5\]。

[1981年](../Page/1981年.md "wikilink")に[ARPANET](../Page/ARPANET.md "wikilink")に接続できない学術機関向けに[CSNET](https://ja.wikipedia.org/wiki/CSNET "wikilink")が構築された。[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")にセキュリティ上の都合で、軍用インターネットバックボーンである[MILNET](https://ja.wikipedia.org/wiki/MILNET "wikilink")が[ARPANET](../Page/ARPANET.md "wikilink")から切り出される形で独立した。[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に新規に構築された[NSFNETのシェア増加と共に](../Page/全米科学財団ネットワーク.md "wikilink")[ARPANET](../Page/ARPANET.md "wikilink")が縮小され、新しい[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")の導入と共に、実運用されているIMPの台数も減少して行った。[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")には[NSFNETのシェア増加を理由として](../Page/全米科学財団ネットワーク.md "wikilink")[ARPANET](../Page/ARPANET.md "wikilink")が廃止され、[ARPANET](../Page/ARPANET.md "wikilink")で運用されていた極少数のIMPは、廃棄されるか、[MILNET](https://ja.wikipedia.org/wiki/MILNET "wikilink")に移管されることになった。

## 1号機

IMPの1号機は[1969年](https://ja.wikipedia.org/wiki/1969年 "wikilink")に、[ハネウェル](../Page/ハネウェル.md "wikilink")の[ミニコンピュータ](../Page/ミニコンピュータ.md "wikilink")・DDP516をベースとして開発された。開発の中心となったのは、当時[ARPA](../Page/国防高等研究計画局.md "wikilink")（防衛高等研究計画局）でパケット通信網の研究を行っていた[ローレンス・ロバーツ](https://ja.wikipedia.org/wiki/ローレンス・ロバーツ "wikilink")、[BBN社の](../Page/BBNテクノロジーズ.md "wikilink")[ボブ・カーンら](../Page/ロバート・カーン.md "wikilink")。ARPANETの開発趣旨（軍事要求）から防爆型の筐体を採用したことで外観は[金庫](../Page/金庫.md "wikilink")に似ており、外寸は家庭用大型[冷蔵庫](https://ja.wikipedia.org/wiki/冷蔵庫 "wikilink")に近い。

1号機は[カリフォルニア大学ロサンゼルス校](../Page/カリフォルニア大学ロサンゼルス校.md "wikilink") (UCLA)の[レナード・クラインロック](https://ja.wikipedia.org/wiki/レナード・クラインロック "wikilink")教授の研究室に設置され、現在もUCLAの図書館に保存されている。

## 参考文献

<references />

## 関連項目

  - [:en:Interface Message Processor](https://ja.wikipedia.org/wiki/:en:Interface_Message_Processor "wikilink")
  - [インターネット](../Page/インターネット.md "wikilink")

<!-- end list -->

  - [ルータ](../Page/ルーター.md "wikilink")

[Category:インターネットの歴史](https://ja.wikipedia.org/wiki/Category:インターネットの歴史 "wikilink") [Category:ネットワークハードウェア](https://ja.wikipedia.org/wiki/Category:ネットワークハードウェア "wikilink")

1.  F. E. HEART, R. E. KAHN, S. 1\\II. ORNSTEIN, W. R. CROWTHER and D. C. WALDEN, <http://dl.acm.org/citation.cfm?id=1477021>, The interface message processor for the ARPA computer network, Spring Joint Computer Conference, 1970.
2.  J. Newkirk, M. Kraley, J. Postel, S.D. Crockerm, <https://www.rfc-editor.org/info/rfc55>, RFC 55 Prototypical implementation of the NCP, June 1970.
3.  R. Kalin, <https://www.rfc-editor.org/info/rfc60>, RFC 60 A Simplified NCP Protocol, July 1970
4.  R.M. Hinden, A. Sheltzer, <https://www.rfc-editor.org/info/rfc823>, RFC 823 DARPA Internet gateway, September 1982.
5.  K. Lougheed, Y. Rekhter, <https://www.rfc-editor.org/info/rfc1105>, RFC 1105 Border Gateway Protocol (BGP), June 1989