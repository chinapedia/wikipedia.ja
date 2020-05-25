> この記事は[Datagram Congestion Control Protocol](https://ja.wikipedia.org/wiki/Datagram_Congestion_Control_Protocol)から翻訳されています。


**Datagram Congestion Control Protocol**（データグラム コンジェスチョン コントロール プロトコル、**DCCP**）は、メッセージ指向の[トランスポートプロトコルである](https://ja.wikipedia.org/wiki/トランスポート層#トランスポート・プロトコル "wikilink")。DCCPは信頼性のあるコネクションの確立、切断、[ECN](https://ja.wikipedia.org/wiki/Explicit_Congestion_Notifcation "wikilink")（明示的輻輳通知）、[輻輳制御](https://ja.wikipedia.org/wiki/輻輳制御 "wikilink")、特徴的なネゴシエーションを実装している。2006年3月にIETFによって RFC 4340（[proposed standard](../Page/インターネット標準.md "wikilink")）として発行された。Linuxでは、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink") 2.6.14でDCCPの最初のリリースが実装され、それ以降のリリースでも開発が続いている。

DCCPは、アプリケーション層ではなくトランスポート層で輻輳制御機構を提供する。DCCPは、[TCPのようなフローベースの考え方を可能にするが](../Page/Transmission_Control_Protocol.md "wikilink")、信頼性や正しい順序を保証しない。また、[SCTPのような複数のストリームで順序指定の配送を提供しない](../Page/Stream_Control_Transmission_Protocol.md "wikilink")。

[輻輳回避だけでなく信頼性のある順序指定の配送を提供するがためにデータが使い物にならなくなるような](https://ja.wikipedia.org/wiki/輻輳#パケット網における輻輳 "wikilink")、タイミングの制約があるようなアプリケーションにとってDCCPは有益である。このようなアプリケーションでは、TCPで妥協するか、[UDPを使って](../Page/User_Datagram_Protocol.md "wikilink")、独自の輻輳制御機構を実装するしかなかった（あるいは輻輳制御をまったくしなかった）。

DCCP接続はデータのトラフィックとは別にACK（acknowledgement）トラフィックを含む。ACKは送信者に対して、送信者のパケットが受信者に届いたか、パケットはECNがマークされていたかを通知する。ACKは輻輳制御機構が要求する程度の信頼性（完全な信頼性たり得る）で転送される。

DCCPはオプションとして、パケットIDに対応する（TCPのようにバイトIDに対応するのではなく）とても長い（48 bit）のシーケンス番号を持つ。この長いシーケンス番号は、「コネクションへのDCCP-Resetsの挿入などの、いくつかのBlind Attack」からの防御を意図している\[1\]。

## 実装

2008年6月現在、最低でも2つのDCCP実装が活発に保守開発されている。

Linuxカーネル上のDCCP実装は、カーネル2.6.14で初めてコミットされた。 この実装についての情報は[Net:DCCP - The Linux Foundation](http://www.linuxfoundation.org/en/Net:DCCP)で提供されている。

[dccp-tp](http://www.phelan-4.com/dccp-tp/)は、ポータブルなDCCP実装として設計されている。

## 関連項目

  - [トランスポート・プロトコルの比較](https://ja.wikipedia.org/wiki/トランスポート層#トランスポート・プロトコルの比較 "wikilink")
  - [Datagram Transport Layer Security](https://ja.wikipedia.org/wiki/Datagram_Transport_Layer_Security "wikilink")

## 出典

## 外部リンク

  - RFC 4340 - Datagram Congestion Control Protocol
  - RFC 4341 - Profile for Datagram Congestion Control Protocol (DCCP)Congestion Control ID 2: TCP-like Congestion Control
  - RFC 4342 - Profile for Datagram Congestion Control Protocol (DCCP)Congestion Control ID 3: TCP-Friendly Rate Control (TFRC)
  - [DCCP page from one of DCCP authors](http://www.read.cs.ucla.edu/dccp/)
  - [DCCP support in Linux](http://linux-net.osdl.org/index.php/DCCP)

[Category:トランスポート層プロトコル](https://ja.wikipedia.org/wiki/Category:トランスポート層プロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.  [RFC 4340 section 7.6](http://tools.ietf.org/html/rfc4340#section-7.6)