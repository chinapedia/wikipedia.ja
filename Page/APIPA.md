> この記事は[APIPA](https://ja.wikipedia.org/wiki/APIPA)から翻訳されています。


**APIPA**（Automatic Private IP Addressing, エーピーアイピーエー）は、人手を介さず、ネットワーク機器間の交渉のみで[リンクローカルアドレス](https://ja.wikipedia.org/wiki/リンクローカルアドレス "wikilink")を自動的に割り当てる技術である。

通常、ネットワーク機器は手動で[IPアドレス](../Page/IPアドレス.md "wikilink")を設定するかもしくは[DHCPサーバより自動的に割り振られたアドレスが設定される](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")。しかし、これらを管理する人がいない、あるいは知識がない場合、自身のアドレスを設定する技術として開発された。この技術は小規模な閉じたネットワークを対象としている。

## リンクローカルアドレス

**リンクローカルアドレス**（[英](../Page/英語.md "wikilink"): link-local address）とは、ローカルネットワークの範囲内の通信または1対1のコネクションにおいてのみ使用することを意図されている[IPアドレス](../Page/IPアドレス.md "wikilink")である。ルーターはリンクローカルアドレスのついたパケットを転送しない。

リンクローカルアドレスは管理者が人手で割り当てるか、オペレーティングシステムの手続きによって割り当てる。ほとんどの場合、「ステートレスアドレス自動設定」を使って割り当てる。[IPv4](../Page/IPv4.md "wikilink")では\[1\]、外部に [Dynamic Host Configuration Protocol](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink") (DHCP) などのアドレス割り当て機構が存在しない場合や、そういった割り当て機構が失敗した場合にのみ、リンクローカルアドレスを割り当てる。[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")では\[2\]リンクローカルアドレスは必須であり、各種プロトコル部品の内部の動作で必要とされる。

[IPv4](../Page/IPv4.md "wikilink")のリンクローカルアドレスはアドレスブロック `169.254.0.0/16` に定義されている。RFC 5735 の中に**Link Local** Address Blockとして、このアドレスに関する規定がある。[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")では、プレフィックス `fe80::/64` が割り当てられている。

## IPv4の場合: APIPA

RFC 3927 において、 [Internet Engineering Task Force](../Page/Internet_Engineering_Task_Force.md "wikilink") は `169.254.1.0` から `169.254.254.255` までのアドレスブロックをIPv4でのリンクローカル用アドレスとして予約していた。リンクローカルアドレスは他のアドレス割り当て手段が利用可能でない場合、ホスト内部で「ステートレスアドレス自動設定」によってインタフェースに割り当てられる\[3\]。

RFC 3927 では例えば、リンクローカルアドレスとグローバルなルーター通過可能なアドレスを同一ホストに同時に設定するなど、異なるスコープ\[4\]での複数アドレスの同時使用に対して警告している。そのため、ホストはリンクローカルアドレスを割り当てる前にネットワーク上にDHCPサーバがないか、問い合わせる。[Windowsの実装ではAPIPAによる割り当ての前にDHCPでの接続を試みるため](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、起動に時間を要する場合がある。

自動アドレス設定処理 (APIPA) では、予約された範囲からランダムに候補アドレスを選択し、[Address Resolution Protocol](../Page/Address_Resolution_Protocol.md "wikilink") (ARP) 要求を[ブロードキャスト](../Page/ブロードキャスト.md "wikilink")してネットワーク上の他の機器に同じアドレスが使われていないか、確認する。ARPに応答があれば、候補IPアドレスがすでに使われていることがわかる。その場合、再びランダムに候補IPアドレスを選択し、同じことを繰り返す。この処理はARPパケットに応答がない場合に終了し、候補IPアドレスが使用可能となる。

リンクローカルアドレスが割り当てられた後、グローバルなルーター通過可能なアドレスや[プライベートなアドレスが利用可能になった際](https://ja.wikipedia.org/wiki/プライベートネットワーク "wikilink")、新たなコネクションにはリンクローカルアドレスよりもそれらの新しいアドレスを使うことが推奨されているが、リンクローカルアドレスによる通信が突然不可能になるわけではない\[5\]。

[マイクロソフト](../Page/マイクロソフト.md "wikilink")は、このアドレス自動設定技術を **Automatic Private IP Addressing** (**APIPA**) と呼んでいる\[6\]。一般には**AutoIP**と呼ばれることも多い。

## IPv6の場合

[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")では、アドレスブロック `fe80::/10` がリンクローカル・アドレッシング向けに予約されている\[7\]。実際にリンクローカルアドレスとして使われているのは、プレフィックス `fe80::/64` のアドレス群である\[8\]。それらは、自動（ステートレス）機構かステートフル（例えば、[DHCPv6](../Page/DHCPv6.md "wikilink")）機構で割り当てられる。

IPv4とは異なり、IPv6では使用中のネットワークインタフェースについて必ずリンクローカルアドレスを必要とし、別にルーター通過可能なアドレスなどが割り当てられていてもリンクローカルアドレスが必須である\[9\]。つまり、IPv6を使用するネットワークインタフェースには必ず複数の[IPv6アドレス](https://ja.wikipedia.org/wiki/IPv6アドレス "wikilink")が割り当てられている。リンクローカルアドレスは、[近隣探索プロトコル](../Page/近隣探索プロトコル.md "wikilink")のIPv6サブレイヤーや[DHCPv6](../Page/DHCPv6.md "wikilink")などのIPv6ベースのプロトコルで必要とされる。

IPv6では RFC 4862 に規定されている通り、「ステートレスアドレス自動設定」を[近隣探索プロトコル](../Page/近隣探索プロトコル.md "wikilink") (NDP) の一部として実行する\[10\]。そのアドレスは、そのインタフェースの[MACアドレス](../Page/MACアドレス.md "wikilink")とルーティングプレフィックスから構成される。

IPv6のリンクローカルアドレスの割り当てでは、他のスコープのアドレスとは異なり、このルーティングプレフィックスがリンク上に存在することが暗黙に前提とされている。

IPv6では追加のアドレス割り当て手段が提供されている。NDPのルーティングプレフィックス広告を通し、ルーターまたは専用サーバがそのリンクに接続している全インタフェースに設定情報を通知し、それによって受信した各インタフェースで追加のIPアドレス割り当てがなされ、ローカルまたはグローバルのルーティングに使われる。この場合、プレフィックスサーバは個々のホストでの割り当てをいちいち受信したり記録したりしないので、この処理もある意味でステートレスである。アドレスの一意性は、アドレス選択方式（RFC 4862 の場合はMACアドレス方式、RFC 4941 の場合はランダム方式）と重複アドレス検出 (DAD) アルゴリズムの組合わせにより、自動的に保証される。

## 脚注

### 注釈

### 出典

## 関連項目

  - [Zeroconf](https://ja.wikipedia.org/wiki/Zeroconf "wikilink")
  - [プライベートネットワーク](https://ja.wikipedia.org/wiki/プライベートネットワーク "wikilink")

[en:Link-local address](https://ja.wikipedia.org/wiki/en:Link-local_address "wikilink") [ru:Link-local address](https://ja.wikipedia.org/wiki/ru:Link-local_address "wikilink")

[Category:システム管理](https://ja.wikipedia.org/wiki/Category:システム管理 "wikilink") [Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink")

1.
2.  RFC 4291,*IP Version 6 Addressing Architecture*, R. Hinden, S. Deering, The Internet Society (February 2006)
3.  RFC 3927, *Dynamic Configuration of IPv4 Link-Local Addresses*, S. Cheshire, B. Aboba, E. Guttman, The Internet Society (May 2005)
4.  RFC 3927 section 1.9
5.  RFC 3927 section 2.6.1
6.
7.
8.  RFC 4291, section 2.5.6. *Link-Local IPv6 Unicast Addresses*
9.  RFC 4291, section 2.8. *A Node's Required Addresses*
10. RFC 4862, *IPv6 Stateless Address Autoconfiguration*, S. Thompson, T. Narten, T. Jinmei (September 2007)