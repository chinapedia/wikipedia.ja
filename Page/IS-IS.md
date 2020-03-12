> この記事は[IS-IS](https://ja.wikipedia.org/wiki/IS-IS)から翻訳されています。


**IS-IS**（Intermediate System to Intermediate System、アイエスアイエス、あるいはアイエストゥアイエス）とは[ルーティング](../Page/ルーティング.md "wikilink")[プロトコルの一種である](../Page/通信プロトコル.md "wikilink")。

## 概要

[自律システム](../Page/自律システム_\(インターネット\).md "wikilink") (AS) 内の[ルーティング](../Page/ルーティング.md "wikilink")を行う[Interior Gateway Protocol](../Page/Interior_Gateway_Protocol.md "wikilink")（IGP）の[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。

IS-ISは[国際標準化機構](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")（ISO）が策定した[開放型システム間相互接続](https://ja.wikipedia.org/wiki/開放型システム間相互接続 "wikilink")（OSI）のネットワーク層における[コネクションレス型通信](https://ja.wikipedia.org/wiki/コネクションレス型通信 "wikilink")サービスである [CLNS](https://ja.wikipedia.org/wiki/CLNS "wikilink")（Connectionless Network Service) 上の[IGPとして開発された](../Page/Interior_Gateway_Protocol.md "wikilink")[ルーティングプロトコル](https://ja.wikipedia.org/wiki/ルーティングプロトコル "wikilink")である。

プロトコルの内容としては[OSPFと同様の](https://ja.wikipedia.org/wiki/オープン・ショーテスト・パス・ファースト "wikilink")[リンクステート型](https://ja.wikipedia.org/wiki/ルーティング#LSA "wikilink")（LSA）のルーティングを行う。 元々OSPFは初期のIS-ISを参考にして作られており両者には類似点が多く含まれる。

代表的なものとして、

  - ともに[リンクステート型](https://ja.wikipedia.org/wiki/ルーティング#LSA "wikilink")（LSA）のルーティングを行う[リンクステート型ルーティングプロトコル](https://ja.wikipedia.org/wiki/リンクステート型ルーティングプロトコル "wikilink")（リンク状態型ルーティング）である。経路探索に[ダイクストラ法](../Page/ダイクストラ法.md "wikilink")を用いて[スパニングツリー](https://ja.wikipedia.org/wiki/スパニングツリー "wikilink")生成することで経路を決定する。
  - 両者とも[エリア](https://ja.wikipedia.org/wiki/エリア "wikilink")の概念を持ち大規模なネットワーク構成に強いという利点がある。
  - [Helloパケット](https://ja.wikipedia.org/wiki/Helloパケット "wikilink")を一定の間隔で送信し隣接する[ルーター](../Page/ルーター.md "wikilink")の[生存確認](https://ja.wikipedia.org/wiki/生存確認 "wikilink")を行う。

相違点としてはエリアの概念の違いや隣接関係の持ち方の違いが挙げられる。 OSPFではネットワークを複数のエリアに分割する際に[バックボーンエリア](https://ja.wikipedia.org/wiki/バックボーンエリア "wikilink")を設定しそのエリアを介して間接的に接続を行うのに対し IS-IS ではバックボーンエリアはなく各エリア内のルーティングを行うルータをL1ルータ、エリア間のルーティングを行うルータをL2ルータとして、L1/L2 両方に属するルータを介して送受信される。

隣接関係の持ち方は IS-ISは OSPF の DR と同様に最もプライオリティ値が高いルータを指名ルータに選出する。 IS-ISでの指名ルータはDIS (Designated Intermdeiate System) と呼ばれる。 ただし OSPF はリンクステート情報が変更されたとき変更情報を持つルータが DRに通知し DRが全ての隣接ルータにリンクステート情報を転送するのに対し、IS-IS ではリンクステート情報の変更が起きた場合、変更情報を持つルータが全ての隣接ルータに情報を送信し、DIS は[経路障害](https://ja.wikipedia.org/wiki/経路障害 "wikilink")等の何らかの理由で隣接ルータ同士のリンクステート情報に差異が出来たときに同期をとる目的で使用される。 OSPF は DR がダウンしたときの影響が大きいため DR の予備として BDR が選出され、DRダウン時には即座に BDR がDRと交替されるが、IS-IS では DIS の予備は選出されない。 この性質のため OSPF では DR が交替するのは基本的に DR に障害が発生したときのみであり、より高いプライオリティ値を持つルータが後から追加されても、そのルータが DR になることができないという問題点を持つのに対し IS-IS では DIS はより DIS にふさわしいルータが接続されたらその場で交替を行うことができる。

## Integrated IS-IS

IS-ISはもともとOSIのためのルーティングプロトコルであり、[インターネット](../Page/インターネット.md "wikilink")で使用されている[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")上での使用を前提とはしていない。 しかしIS-IS はそれ自体では評価も高いルーティングプロトコルであり、またOSIプロトコルスイートの制定当時 OSI陣営は TCP/IP から OSIプロトコルスイートへの移行のために既存の技術から OSIの規格にスムーズに移行する必要性があった。 このため自然と IS-IS を TCP/IP 上でも使用したいという要望が高まった。 これを受けて CLNS上でも IP上でも機能するように改良した規格が新たに発表された。 これが Integrated IS-IS（統合IS-IS）である。このプロトコルは[IPアドレス](../Page/IPアドレス.md "wikilink")を[MACアドレス](../Page/MACアドレス.md "wikilink")と同様の端末の識別用のアドレスとして使用し、ルーティング自体は CLNS独自のアドレスである [NSAP](https://ja.wikipedia.org/wiki/NSAP "wikilink")（Network Service Access Point)を使用して行うという方法が取られている。

OSI は TCP/IP に取って代わることはできずに撤退したため、OSIで策定されたほとんどのプロトコルは使われなくなったにもかかわらず IS-IS はこの Integrated IS-IS として現在も一部のシステムで使用されている。 [IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")に対する対応も[IETFにより策定され](../Page/Internet_Engineering_Task_Force.md "wikilink")、2008年10月に正式に公開された。

## 主なRFC

  - RFC 1142（1990年2月）、IS-ISのプロトコルの内容の規定
  - RFC 1195（1990年12月）、Integrated IS-ISの規定
  - RFC 5308（2008年10月）、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")への対応

## 関連項目

  - [ルーティングプロトコル](https://ja.wikipedia.org/wiki/ルーティングプロトコル "wikilink")
  - [IEEE 802.1aq](https://ja.wikipedia.org/wiki/IEEE_802.1aq "wikilink") (Shortest Path Bridging)
  - [Open Shortest Path First](../Page/Open_Shortest_Path_First.md "wikilink")

## 参考文献

  - 久米原 栄、『IPルーティング入門』、[ソフトバンククリエイティブ](https://ja.wikipedia.org/wiki/ソフトバンククリエイティブ "wikilink")、2007年、ISBN 978-4-7973-3743-3

[Category:ルーティングプロトコル](https://ja.wikipedia.org/wiki/Category:ルーティングプロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")