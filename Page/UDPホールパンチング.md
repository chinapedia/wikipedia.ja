> この記事は[UDP](https://ja.wikipedia.org/wiki/UDP)から翻訳されています。


**UDPホールパンチング**（[英](../Page/英語.md "wikilink"): **UDP hole punching**）とは、典型的な [NAT traversal](../Page/NAT_traversal.md "wikilink") 技術の1つ。

## 概要

[UDPホールパンチングによる](../Page/User_Datagram_Protocol.md "wikilink") [NAT](../Page/ネットワークアドレス変換.md "wikilink") traversal とは、NAT を使ったプライベートネットワーク内にあるホスト同士が[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")経由で双方向のUDPコネクションを確立する手法である。NAT には様々なものがあって動作仕様が標準化されていないため、あらゆる NAT で機能するわけではない。

NATの背後にある各ホストは、典型的には [STUN](https://ja.wikipedia.org/wiki/STUN "wikilink") や [ICE](https://ja.wikipedia.org/wiki/Interactive_Connectivity_Establishment "wikilink") を用いて通信相手との間に存在するNATの公開アドレスを取得する。この過程では、公開のアドレス空間にある第3の既知のサーバに一旦接続することでUDPポートマッピングと相手方のUDP状態を確立し、以後はパケットが違うホストから来ていても NATデバイスが状態を維持するだろうと期待して、直接的な通信に切り換える。通常、UDP状態は数十秒～数分以内に失効してクローズされてしまうので、UDPホールパンチングでは定期的な keep-alive パケットの送出が併用され、これによってNATが持つUDP状態マシンの寿命を延長する。

大企業内でよく使われている対称型[NAT](../Page/ネットワークアドレス変換.md "wikilink")（双方向NAT）では、UDPホールパンチングは機能しない。対称型NATでは、既知のSTUNサーバに対するコネクションに関連するNATマッピングは、既知のサーバからの受信にしか使えないよう制限されているので、既知のサーバ側から見えるNATマッピングはエンドポイントにとって役に立たないからである。

より精巧な方法として、双方のホストが互いに複数回ずつ送信を試みる方法がある。制限付きコーンNATでは、他のホストからの最初のパケットはブロックされる。しかしこれによって相手マシンにパケットを送ったという記録がNATデバイスに残り、以後その相手方IPアドレスとポート番号からのパケットはNATを通されるようになる。この技法は[P2Pソフトウェアや](../Page/Peer_to_Peer.md "wikilink")[VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink")通話で広く使われており、UDP 上で[VPN接続を確立する際にも応用できる](../Page/Virtual_Private_Network.md "wikilink")。同様の技法を[TCPコネクションにも適用する場合があるが](../Page/Transmission_Control_Protocol.md "wikilink")、成功率は遥かに低くなる。何故なら、TCPではコネクションのストリームは応用プログラムではなくホスト OS が制御しており、順序番号がランダムに生成されるので、順序番号を検査するような NAT デバイスは、パケットを既存のコネクションに結び付けることが出来ずに破棄してしまうからである。

## アルゴリズム

AとBというホストが、それぞれのプライベートネットワークにあるとする。N1とN2はそれぞれのNATデバイスである。SはグローバルIPアドレスを持つパブリックサーバである。

1.  A と B は S との UDP 通信を開始する。NATデバイス N1 と N2 は UDP 変換状態を作成し、一時的な外部ポート番号を割り当てる。
2.  S はそれらのポート番号を A と B にリレーして通知する。
3.  A と B は相手のNATデバイスと通知されたポート番号で直接通信する。NAT デバイスはそれ以前に生成されていた変換状態を使い、A および B の間でパケットの送受信が可能になる。

## 関連項目

  - [STUN](https://ja.wikipedia.org/wiki/STUN "wikilink")
  - [Hamachi](https://ja.wikipedia.org/wiki/Hamachi "wikilink")
  - [Freenet](../Page/Freenet.md "wikilink")
  - [Real Time Media Flow Protocol](https://ja.wikipedia.org/wiki/Real_Time_Media_Flow_Protocol "wikilink")

## 外部リンク

  - [Peer-to-Peer Communication Across Network Address Translators](http://www.brynosaurus.com/pub/net/p2pnat/), [PDF版](http://www.brynosaurus.com/pub/net/p2pnat.pdf)
  - [STUNT](http://nutss.gforge.cis.cornell.edu/stunt.php)
  - [Network Address Translation and Peer-to-Peer Applications (NATP2P)](http://pdos.csail.mit.edu/~baford/nat/draft-ford-natp2p-00.txt)
  - [How Skype & Co. get round firewalls](http://www.heise-online.co.uk/security/How-Skype-Co-get-round-firewalls--/features/82481) - SkypeでのUDPホールパンチングの使い方の簡単な説明
  - [通信網を脅かすSkypeの仕組み、わかりやすく解剖\!](http://www.atmarkit.co.jp/fnetwork/rensai/5minskype/03.html) アットマーク・アイティ（江原顕雄 2006年10月19日）
  - [NAT support for peer-to-peer games: a proposal](http://www.hasenstein.com/HyperNews/get/linux-ip-nat/97.html)

[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink")