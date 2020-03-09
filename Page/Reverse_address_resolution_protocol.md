> この記事は[Reverse address resolution protocol](https://ja.wikipedia.org/wiki/Reverse_address_resolution_protocol)から翻訳されています。


**Reverse address resolution protocol**(逆アドレス解決プロトコル、略称：**RARP**、リバースARP)は、機器の物理アドレス([MACアドレス](https://ja.wikipedia.org/wiki/MACアドレス "wikilink"))から[IPアドレス](../Page/IPアドレス.md "wikilink")を取得するための[プロトコル](../Page/プロトコル.md "wikilink")である。

## 概要

機器は自らのMACアドレスを[ブロードキャスト](https://ja.wikipedia.org/wiki/ブロードキャスト "wikilink")し(RARPリクエスト)、それに対してRARPサーバが応答してIPアドレスを配布する。そのため、**RARPサーバ**は必須である。RARPサーバにはMACアドレスとそれに対応するIPアドレスを登録してある。

[データリンク層](https://ja.wikipedia.org/wiki/データリンク層 "wikilink")に属する。

IPを要求してきた機器に渡せるのはIPアドレスのみで、サブネットマスク、デフォルトゲートウェイ、DNSサーバーのアドレスなどは渡せない。また、データリンク層の技術なのでルータを越えて利用できない。さらに、RARPサーバーには事前に要求機器のMACアドレスを登録しておく必要があり、柔軟性に欠ける。このため、近年では同機能でより高機能なDHCPなどにより代替されることが多い。

## 関連項目

  - [ARP](../Page/Address_Resolution_Protocol.md "wikilink")(Address Resolution Protocol) - [IPアドレス](../Page/IPアドレス.md "wikilink")から[MACアドレス](https://ja.wikipedia.org/wiki/MACアドレス "wikilink")に変換する[プロトコル](../Page/プロトコル.md "wikilink")

## 関連RFC

  - [A Reverse Address Resolution Protocol](https://tools.ietf.org/html/rfc903) (RFC 903)

[Category:リンク層プロトコル](https://ja.wikipedia.org/wiki/Category:リンク層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")