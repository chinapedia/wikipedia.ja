> この記事は[Ping of death](https://ja.wikipedia.org/wiki/Ping_of_death)から翻訳されています。


**ping of death**（しばしば**PoD**と略記される）とは、規格外や悪意のある[ping](https://ja.wikipedia.org/wiki/ping "wikilink")を送りつけることによる、コンピュータシステムへの攻撃の一種である。

通常であればping[パケット](../Page/パケット.md "wikilink")のサイズは56[バイト](../Page/バイト_\(情報\).md "wikilink")（[IPヘッダ](https://ja.wikipedia.org/wiki/IPヘッダ "wikilink")を入れて64バイト）である。また、[Internet Protocolを規定しているRFC](../Page/Internet_Protocol.md "wikilink") 791では、（pingを含む）全ての[IPv4](../Page/IPv4.md "wikilink")パケットの最大サイズは65,535バイトと規定しており、多くのコンピュータシステムは最大パケットサイズを超える大きさのpingパケットを適切に処理できるように設計されていない\[1\]。しかし、[IPフラグメントの仕様の欠陥をついて最大サイズを超える大きさのpingを送信することができ](https://ja.wikipedia.org/wiki/IPフラグメンテーション "wikilink")、これを受信したコンピュータで[バッファオーバーフロー](https://ja.wikipedia.org/wiki/バッファオーバーフロー "wikilink")が発生して、システムが[クラッシュする可能性がある](https://ja.wikipedia.org/wiki/クラッシュ_\(コンピュータ\) "wikilink")。

[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")の初期の実装では、このバグは悪用されやすく、[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")、[Linux](../Page/Linux.md "wikilink")、[Macintosh](../Page/Macintosh.md "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、および周辺機器を含む様々なシステムに影響を及ぼす可能性がある。[ファイアウォール](../Page/ファイアウォール.md "wikilink")などでping of deathへの対策が施されるようになると、pingを利用したと呼ばれる別の種類の攻撃が行われるようになった。これは、通常のトラフィックがシステムに到達できないほど多くのping requestを対象のコンピュータに送りつける、[DoS攻撃](../Page/DoS攻撃.md "wikilink")の一種である。

## 詳細な説明

RFC 791で定義されているように、IPヘッダを含むIPv4パケットの最大パケット長は65,535(=2<sup>16</sup> − 1)バイトである。これは、IPヘッダにおけるパケット長を格納するフィールドが16ビット幅であることによる制限である。

IPの基礎となる[データリンク層](../Page/データリンク層.md "wikilink")では、ほとんどの場合に、MTU([Maximum Transmission Unit](../Page/Maximum_Transmission_Unit.md "wikilink"))として最大フレームサイズに制限が設けられている。[イーサネット](../Page/イーサネット.md "wikilink")では、MTUは通常1500バイトである。この場合、MTUを超える大きなIPパケットは、MTU以下のサイズの複数のIPパケットに分割される（これを[フラグメントという](https://ja.wikipedia.org/wiki/IPフラグメンテーション "wikilink")）。受信側では、分割されたパケットから元のIPパケットを再構成する。

フラグメントが実行されるとき、それぞれの分割されたパケットは、元のIPパケットのどの部分であるかの情報を運ぶ必要がある。この情報は、IPヘッダのFragment Offsetフィールドに保持されている。このフィールドは13ビット長で、元のIPパケット内の現在のIPフラグメント内のデータのオフセットを含む。オフセットは8バイト単位で与えられる。これにより、最大オフセットは65,528(=(2<sup>13</sup>-1)×8)まで可能になる。これに20バイトのIPヘッダを追加すると、最大長は65,548バイトになり、最大パケット長を超える。これは、最大のオフセット値を持つIPフラグメントパケットに含まれるデータが7バイト以下でなければ、最大パケット長の制限を超えてしまうことを意味する。悪意のあるユーザーは、最大のオフセット値を持つIPフラグメントパケットに8バイト以上のデータ（物理層で許容されるサイズ以上）を送信し、攻撃に利用する。このようなパケットを受信したコンピュータでは、IPフラグメントパケットを再構成したときに、65,535バイトより大きいIPパケットが生成されることになる。 これは、受信側のコンピュータで受信パケットに割り当てたメモリバッファを[オーバーフローさせ](https://ja.wikipedia.org/wiki/バッファオーバーフロー "wikilink")、様々な問題を引き起こす可能性がある。

上記の説明から明らかなように、これはIPフラグメントの再構成プロセスにおける問題であり、pingや[ICMPに限らず](../Page/Internet_Control_Message_Protocol.md "wikilink")、IPを利用するあらゆるタイプのプロトコル（[TCP](../Page/Transmission_Control_Protocol.md "wikilink")、[UDP](../Page/User_Datagram_Protocol.md "wikilink")、[IGMPなど](../Page/Internet_Group_Management_Protocol.md "wikilink")）で起こり得る。

対策として、再構成プロセスにチェック機構を追加する手法がある。各着信IPフラグメントパケットについて、IPヘッダ内の"Fragment Offset"フィールドと"Total length"フィールドの合計値が65,535以下であることを確認する。合計値が大きければ、そのパケットは無効であり、IPフラグメントは無視される。このチェックは、バグが修正されていないホストを保護するために、一部の[ファイアウォール](../Page/ファイアウォール.md "wikilink")で実行されている。別の対策として、パケットの再構成に65,535バイトを超えるメモリバッファを割り当てる方法もあるが、これはRFCで規定されている以上のパケットの受信を許可することになり、仕様に反する。

### IPv6のping of death

2013年、[Microsoft Windowsで](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")のping of deathの脆弱性が発見された。不正な形式の受信した[ICMPv6](https://ja.wikipedia.org/wiki/ICMPv6 "wikilink")パケットを処理するときに、Windows TCP/IPスタックがメモリ割り当てを正しく処理しなかったため、リモートからサービス拒否が起こる可能性がある。この脆弱性は2013年8月にMS13-065で修正された\[2\]\[3\]。この脆弱性に対するはCVE-2013-3183である\[4\]。

## 関連項目

  -
  - [Land攻撃](https://ja.wikipedia.org/wiki/Land攻撃 "wikilink")

  -
  -
  - [Smurf攻撃](https://ja.wikipedia.org/wiki/Smurf攻撃 "wikilink")

## 脚注

## 外部リンク

  -
  - [Ping of death at Insecure.Org](http://insecure.org/sploits/ping-o-death.html)

[Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:DoS攻撃](https://ja.wikipedia.org/wiki/Category:DoS攻撃 "wikilink")

1.
2.
3.
4.