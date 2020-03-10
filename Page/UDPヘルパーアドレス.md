> この記事は[UDP](https://ja.wikipedia.org/wiki/UDP)から翻訳されています。


**UDPヘルパーアドレス**とは、クライアントとサーバが異なる[サブネット](https://ja.wikipedia.org/wiki/サブネット "wikilink")に属する場合に[ブロードキャスト](../Page/ブロードキャスト.md "wikilink")パケットを中継する際に設定する、[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")の特別な設定。主にエンタープライズ環境で各サブネットにサーバを設置するコストを節約する用途に用いられる。

## 使用例

ネットワークでは各ホストがユニークなIPアドレスを持っている。隣り合ったアドレスのグループは同一サブネットと呼ばれる。各クライアントにIPアドレスを割り振る方法には[DHCPがあり](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")、通常はサブネット毎にDHCPサーバが設置される。

しかしながら、サブネットの異なるネットワークに対してもDHCPにてアドレスを割り振りたい場合も存在するが、大抵のルータはブロードキャストパケットをサブネットを跨いで中継しない。これはDHCPのような重要なネットワークサービスの運用にあたって問題となる。

この解決のため、UDPヘルパーアドレスをルータに設定し、PCからのブロードキャストパケットをDHCPサーバに転送する方法が用いられる。するとDHCPサーバは設定された範囲からIPアドレスを１つ選び、そのアドレスで応答する。この際にDHCPサーバはそのIPアドレスを記憶しておき、再びクライアントがブロードキャストで応答した際、IPアドレスのリースを実行する。

また、ヘルパーアドレスも異なるサブネットを跨いで[UDPパケットが転送されるため](../Page/User_Datagram_Protocol.md "wikilink")、UDPヘルパーアドレスはサブネットの異なる２台のサーバマシン間で通信を行うために作成されることがある。

## 実装例

[シスコ製品では](https://ja.wikipedia.org/wiki/シスコシステムズ "wikilink")、この機能はルーティングソフトウエア Version.10から実装された。\[1\] この機能を利用するためのコマンドは `ip helper-address` と `ip forward-protocol` になる。

Syntax Description:

`ip helper-address [`**`vrf``   `*`name`***` | `**`global`**`] `*`address`*` [`**`redundancy`**` `*`vrg-name`*`]`
`no ip helper-address `**`[vrf``   `*`name`*`   ``|``   ``global]`**` `*`address`*` [`**`redundancy`**` `***`vrg-name`***`] `

**vrf *name***

`(Optional) Enables VPN routing and forwarding (VRF) instance and VRF name. `

**global**

`(Optional) Configures a global routing table. `

***address***

`Destination broadcast or host address to be used when forwarding UDP broadcasts. There can be more than one helper address per interface. `

**redundancy *vrg-name***

`(Optional) Defines the VRG group name.`

## 特記事項

UDPヘルパーアドレスの使用は[Windowsのネットワーク設定に影響を及ぼすことがある](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。 [Microsoft's](../Page/マイクロソフト.md "wikilink") knowledge base を参照のこと。\[2\]

マイクロソフトによると、この問題はシスコルータのデフォルト設定がPort137,138を利用するために生じている。これらのポートは[NetBIOS](https://ja.wikipedia.org/wiki/NetBIOS "wikilink")がネットワーク設定のために利用しているので、ブロードキャストにおいて混信を招く場合があるためである。

## 参考文献

<div class="references-small">

<references/>

</div>

[Category:インターネット技術](https://ja.wikipedia.org/wiki/Category:インターネット技術 "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink")

1.  [Redirect: Internal Technical Support ITS](http://www.cisco.com/univercd/cc/td/doc/product/software/ios121/121cgcr/ip_r/iprprt1/1rdipadr.htm#wp1018606)
2.  [UDP broadcast forwarding by Cisco's IP Helper](http://support.microsoft.com/kb/190930)