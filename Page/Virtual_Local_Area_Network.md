> この記事は[Virtual Local Area Network](https://ja.wikipedia.org/wiki/Virtual_Local_Area_Network)から翻訳されています。


**Virtual Local Area Network**(バーチャル・ローカル・エリア・ネットワーク、**VLAN**、仮想LAN)は、[スイッチなどのネットワーク機器の機能により](../Page/スイッチングハブ.md "wikilink")、物理的な接続形態とは別に仮想的な[ネットワークを構成することである](../Page/コンピュータネットワーク.md "wikilink")。スイッチの接続ポートや[MACアドレス](../Page/MACアドレス.md "wikilink")、[プロトコル](../Page/プロトコル.md "wikilink")などに応じて、端末のグループ化を実現する。

## 概要

近年、VLANの用途は多様化しているが、最も多いVLANの用途としては[レイヤ3スイッチ](../Page/レイヤ3スイッチ.md "wikilink")を用いて、スイッチを[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")としたネットワークを構成しているものなどがある。主にブロードキャスト・ドメインの分割による通信帯域の有効活用を目的として利用される事が多いが、大企業などではスイッチを用いて部門毎にVLANを設けることでネットワークを分割し、アクセスを制限するなどネットワーク[セキュリティ対策手段としての用途もある](../Page/コンピュータセキュリティ.md "wikilink")。

## VLANの方式

  - **ポートベースVLAN** : [スイッチの接続ポート番号により所属するVLANグループを識別する方式](../Page/スイッチングハブ.md "wikilink")。

<!-- end list -->

  - **MACベースVLAN** : 端末のMACアドレスにより所属するVLANグループを識別する方式。

<!-- end list -->

  - **サブネットベースVLAN** : 端末のIPアドレスにより所属するVLANグループを識別する方式。

<!-- end list -->

  - **プロトコルベースVLAN** : [IP](../Page/Internet_Protocol.md "wikilink")、[IPX](https://ja.wikipedia.org/wiki/Internetwork_Packet_Exchange "wikilink")、[AppleTalk](../Page/AppleTalk.md "wikilink")などの[ネットワークプロトコル](https://ja.wikipedia.org/wiki/ネットワークプロトコル "wikilink")によりVLANグループを識別する方式。

<!-- end list -->

  - **タグVLAN** : イーサーネットフレームに付加された短い固定長のタグによりVLANグループを識別する方式。タグを付加することにより、フレームに自身が所属するVLANの識別情報を持たせるという、[IEEE](../Page/IEEE.md "wikilink")で[802.1Qとして標準化された](https://ja.wikipedia.org/wiki/IEEE_802.1Q "wikilink")[通信プロトコル](../Page/通信プロトコル.md "wikilink")に準拠している。これにより、一つの通信ポートで複数の異なるVLANを通信させることが可能になる。主に複数のスイッチングハブにわたってVLANを構成したりする為に用いられる。但し、フレームにタグが付くため、最大フレーム長が長くなり、タグ付きの[フレームを通過させるだけの機器も](../Page/パケット.md "wikilink")、この通常より大きなフレームに対応していなければならない。1回線で複数のタグVLANの[パケット](../Page/パケット.md "wikilink")を通信する接続を「**トランク接続**」と言う。

<!-- end list -->

  - **マルチプルVLAN** : 通常のポートベースVLANに加え、マルチプルポートと呼ばれるポートを設定する事が可能な方式。マルチプルポートはポートベースで設定した全てのVLANグループがオーバーラップしており、全てのVLANグループと通信可能である。タグVLANと異なる点は、アップリンクの接続先がVLAN非対応の端末でも使用可能という点である。

## リンクの種類

  - **アクセスリンク** : 端末を接続するための1つのVLANにしか属していないポートを利用したリンクである。
  - **トランクリンク** : 複数のタグVLANに属するサーバやルーターを接続するリンク（ポート）である。

## 参考文献

  -
## 関連項目

  - [Local Area Network](../Page/Local_Area_Network.md "wikilink")
  - [Shortest Path Bridging](https://ja.wikipedia.org/wiki/Shortest_Path_Bridging "wikilink") ([IEEE 802.1aq](https://ja.wikipedia.org/wiki/IEEE_802.1aq "wikilink")) 4096から16000000 VLANを拡張
  - [レイヤ3スイッチ](../Page/レイヤ3スイッチ.md "wikilink")

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")