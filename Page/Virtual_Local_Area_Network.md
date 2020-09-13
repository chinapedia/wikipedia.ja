> この記事は[Virtual Local Area Network](https://ja.wikipedia.org/wiki/Virtual_Local_Area_Network)から翻訳されています。


**Virtual Local Area Network**(バーチャル・ローカル・エリア・ネットワーク、**VLAN**、仮想LAN)は、[LANスイッチ](../Page/LANスイッチ.md "wikilink")([レイヤ2スイッチ](https://ja.wikipedia.org/wiki/レイヤ2スイッチ "wikilink"))などのネットワーク機器の機能により、物理的な接続形態とは別に仮想的に[LAN](https://ja.wikipedia.org/wiki/LAN "wikilink")セグメントを構成することである。スイッチの接続ポートや[MACアドレス](../Page/MACアドレス.md "wikilink")、[プロトコル](../Page/プロトコル.md "wikilink")などに応じて、LANセグメントの分離を実現する。

## 概要

VLANを構成する目的は

  - ネットワークの大規模化に対してブロードキャスト・ドメインを分割することで通信帯域を確保する
  - 部署・用途に応じてLANセグメントを分離し、アクセスを制限することでネットワーク[セキュリティを確保する](../Page/コンピュータセキュリティ.md "wikilink")

ことである。 VLAN間は[レイヤ3スイッチ](../Page/レイヤ3スイッチ.md "wikilink")などを用いてルーティングすることでトラフィックを疎通させる。

## VLANの方式

  - **ポートベースVLAN**
      -
        [スイッチの接続ポートによりLANセグメントを分離する方式である](../Page/スイッチングハブ.md "wikilink")。

<!-- end list -->

  - **MACベースVLAN**
      -
        接続される機器の[MACアドレス](../Page/MACアドレス.md "wikilink")により所属するLANセグメントを分離する方式である。

<!-- end list -->

  - **サブネットベースVLAN**
      -
        接続される機器のIPアドレスのサブネットによりLANセグメントを分離する方式である。

<!-- end list -->

  - **プロトコルベースVLAN**
      -
        [IP](../Page/Internet_Protocol.md "wikilink")、[IPX](https://ja.wikipedia.org/wiki/Internetwork_Packet_Exchange "wikilink")、[AppleTalk](../Page/AppleTalk.md "wikilink")などの[ネットワークプロトコル](https://ja.wikipedia.org/wiki/ネットワークプロトコル "wikilink")によりLANセグメントを分離する方式である。Ethernet IIまたはIEEE 802.3x-1997におけるEther Type値を参照してイーサネットから見た上位レイヤのプロトコルを識別する。

<!-- end list -->

  - **タグVLAN**
      -
        詳細は[IEEE 802.1Qを参照のこと](https://ja.wikipedia.org/wiki/IEEE_802.1Q "wikilink")。
        イーサネットヘッダのSource MACとEthner Type/Sizeの間に識別タグ(VLANタグ)を挿入し、これによりLANセグメントを分離する方式である。[IEEE 802.1Qで規定されている](https://ja.wikipedia.org/wiki/IEEE_802.1Q "wikilink")。 これにより、一つの通信ポートで複数の異なるVLANを通信させることが可能になる。主に複数のLANスイッチにわたってVLANを構成したりする為に用いられる。但し、フレームにタグが付くため、最大フレーム長が長くなり、タグ付きの[フレームを通過させるだけの機器も](../Page/パケット.md "wikilink")、この通常より大きなフレームに対応していなければならない。1回線で複数のタグVLANの[パケット](../Page/パケット.md "wikilink")を通信する接続を「**トランク接続**」と言う。

<!-- end list -->

  - **マルチプルVLAN**
      -
        通常のポートベースVLANに加え、マルチプルポートと呼ばれるポートを設定する事が可能な方式。マルチプルポートはポートベースで設定した全てのVLANグループがオーバーラップしており、全てのVLANグループと通信可能である。タグVLANと異なる点は、アップリンクの接続先がVLAN非対応の端末でも使用可能という点である。

## リンクの種類

  - **アクセスリンク** : 端末を接続するための1つのVLANにしか属していないポートを利用したリンクである。
  - **トランクリンク** : 複数のタグVLANに属するサーバやルーターを接続するリンク（ポート）である。

## 参考文献

  -
## 関連項目

  - [Local Area Network](../Page/Local_Area_Network.md "wikilink")
  - [LANスイッチ](../Page/LANスイッチ.md "wikilink")
  - [レイヤ2スイッチ](https://ja.wikipedia.org/wiki/レイヤ2スイッチ "wikilink")
  - [レイヤ3スイッチ](../Page/レイヤ3スイッチ.md "wikilink")
  - [Shortest Path Bridging](https://ja.wikipedia.org/wiki/Shortest_Path_Bridging "wikilink") ([IEEE 802.1aq](https://ja.wikipedia.org/wiki/IEEE_802.1aq "wikilink")) 4096から16000000 VLANを拡張

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")