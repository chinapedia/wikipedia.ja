> この記事は[Bootstrap Protocol](https://ja.wikipedia.org/wiki/Bootstrap_Protocol)から翻訳されています。


**Bootstrap Protocol**（ブートストラップ プロトコル、**BOOTP**）は、[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")に接続された[クライアント](https://ja.wikipedia.org/wiki/クライアント "wikilink")が、[IPアドレス](../Page/IPアドレス.md "wikilink")や[ホスト名](../Page/ホスト名.md "wikilink")、[サブネットマスク](../Page/サブネットマスク.md "wikilink")等を自動的に取得するための[プロトコル](../Page/プロトコル.md "wikilink")である。元々は RFC 951 で定義された。主に、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")が[ブート](../Page/ブート.md "wikilink")（起動）する際に用いられる。

## 概要

ネットワークに接続されているコンピュータの電源を入れてオペレーティングシステムを起動すると、システムソフトウェアはBOOTPメッセージをネットワークに[ブロードキャスト](../Page/ブロードキャスト.md "wikilink")で送信し、IPアドレスの割り当てを要求する。BOOTP設定サーバは、要求に基づいて、管理者によって設定されたアドレスプールからIPアドレスを割り当てる。

BOOTPは転送プロトコルとして[UDPを使用する](../Page/User_Datagram_Protocol.md "wikilink")。サーバがクライアントの要求を受信するために[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")67を、クライアントがサーバからの応答を受信するためにポート番号68が使用される。なお、これらのポート番号は[DHCPと同じである](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")。BOOTPは[IPv4](../Page/IPv4.md "wikilink")でのみ動作する。

歴史的に、BOOTPはIPアドレスの割り当てのほか、[UNIX系](https://ja.wikipedia.org/wiki/UNIX系 "wikilink")のでのネットワーク上での場所を取得するのにも使用された。企業では、これを使用して、事前に設定されたクライアントのブートイメージを新しく導入したPCにロールアウトした。

ネットワークカードの製造元は、当初は初期のネットワーク接続を確立するためにブート用の[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")を用意する必要があったが、後にインターフェイスカードの[BIOS](https://ja.wikipedia.org/wiki/BIOS "wikilink")やオンボードネットワークアダプタを備えたシステムボードにプロトコルを組み込み、直接ネットワークブートを行うことが可能となった。

BOOTPにリースの機能を追加した[Dynamic Host Configuration Protocol](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")(DHCP)によりBOOTPは置き換えられているが、BOOTPの一部はDHCPプロトコルにサービスを提供するために使用される。DHCPサーバは、従来のBOOTP機能も提供する。

## 歴史

BOOTPは、1985年9月に公開された RFC 951 で最初に定義された。これは、1984年6月に RFC 903 で公開された[Reverse address resolution protocol](../Page/Reverse_address_resolution_protocol.md "wikilink")（逆アドレス解決プロトコル、RARP）を置き換えるものだった。RARPをBOOTPに置き換えることになったのは、RARPが[リンク層](../Page/リンク層.md "wikilink")プロトコルだったからである。このため、多くのサーバープラットフォームでの実装が困難となり、かつ、サーバを個々の[サブネット](https://ja.wikipedia.org/wiki/サブネット "wikilink")に配置する必要があったためである。

BOOTPは、標準IPルーティングを使用してローカルネットワークからBOOTPパケットを転送するリレーエージェントの技術を導入し、これによって1つのBOOTPサーバで多数のサブネット上のホストにサービスを提供できるようになった\[1\]。

## 動作

### クライアントとサーバが同じネットワーク上にある場合

BOOTPサーバ側では、[MACアドレス](../Page/MACアドレス.md "wikilink")とIPアドレス・ホスト名の対応表を事前に用意する。ネットワークに接続された機器は自らのMACアドレスを[ブロードキャスト](../Page/ブロードキャスト.md "wikilink")し、これを受け取ったBOOTPサーバが、対応表に従ってIPアドレスを配布する。DHCPのような動的なIPアドレスの配布は行えない。

1.  BOOTPサーバはUDPポート67でパッシブオープンコマンドを発行し、クライアントを待ち受ける。
2.  クライアントは起動時にポート68でアクティブオープンコマンドを発行する。このメッセージはUDPユーザデータグラムにカプセル化されており、UDPユーザデータグラムはIPデータグラムにカプセル化されている。クライアントは送信元アドレスにオール0(0.0.0.0)、宛先アドレスにオール1(255.255.255.255)を使用する。
3.  サーバはクライアントのMACアドレスから割り当てるべきIPアドレスを認識する。サーバは、送信元ポート67・宛先ポート68のブロードキャストまたはユニキャストのUDPメッセージで応答する。

### クライアントとサーバが異なるネットワーク上にある場合

BOOTPリクエストの問題は、リクエストがブロードキャストで送信されることある。ブロードキャストのIPデータグラムはルータによって破棄されるため、ルータを通過することができない（異なるサブネットへ送信できない）。この問題を解決するために、リレーエージェントが導入された。ホストまたはルータは、リレーエージェントとして動作するようにアプリケーション層で設定できる。以下に、リレーエージェントの動作を示す。

1.  リレーエージェントはBOOTPサーバのユニキャストアドレスを知っており、ポート67でブロードキャストメッセージを待ち受ける。
2.  リレーエージェントがブロードキャストパケットを受信すると、メッセージをユニキャストデータグラムにカプセル化し、BOOTPサーバに要求を送信する。
3.  ユニキャストのパケットはルータを通過することができ、パケットがBOOTPサーバに到達する。BOOPサーバはリレーエージェント宛に応答を送信する。
4.  BOOPサーバからの応答を受け取ったリレーエージェントは、それをクライアントに送る。

## IETF標準ドキュメント

| RFC \#   | タイトル                                                                         | 発行日      | 廃止・更新                                                                 |
| -------- | ---------------------------------------------------------------------------- | -------- | --------------------------------------------------------------------- |
| RFC 3942 | Reclassifying Dynamic Host Configuration Protocol version 4 (DHCPv4) Options | 2004年11月 | RFC 2132 を更新                                                          |
| RFC 2132 | DHCP Options and BOOTP Vendor Extensions                                     | 1997年3月  | RFC 1533 を廃止。 RFC 3442, RFC 3942, RFC 4361, RFC 4833, RFC 5494 により更新。 |
| RFC 1542 | Clarifications and Extensions for the Bootstrap Protocol                     | 1993年10月 | RFC 1532 を廃止。 RFC 951 を更新。                                            |
| RFC 1534 | Interoperation Between DHCP and BOOTP                                        | 1993年10月 |                                                                       |
| RFC 1533 | DHCP Options and BOOTP Vendor Extensions                                     | 1993年10月 | RFC 1497, RFC 1395, RFC 1084, RFC 1048 を廃止。 RFC 2132 により廃止。           |
| RFC 1532 | Clarifications and Extensions for the Bootstrap Protocol                     | 1993年10月 | RFC 1542 により廃止。RFC 951 を更新。                                           |
| RFC 1497 | BOOTP Vendor Information Extensions                                          | 1993年8月  | RFC 1395, RFC 1084, RFC 1048 を廃止。RFC 1533 により廃止。 RFC 951 を更新。         |
| RFC 1395 | BOOTP Vendor Information Extensions                                          | 1993年1月  | RFC 1084, RFC 1048 を廃止。 RFC 1497, RFC 1533 により廃止。 RFC 951 を更新。        |
| RFC 1084 | BOOTP vendor information extensions                                          | 1988年12月 | RFC 1048 を廃止。 RFC 1395, RFC 1497, RFC 1533 により廃止。                     |
| RFC 1048 | BOOTP vendor information extensions                                          | 1988年2月  | RFC 1084, RFC 1395, RFC 1497, RFC 1533 により廃止。                         |
| RFC 951  | Bootstrap Protocol                                                           | 1985年9月  | RFC 1395, RFC 1497, RFC 1532, RFC 1542, RFC 5494 により更新。               |
|          |                                                                              |          |                                                                       |

## 関連項目

  - [Dynamic Host Configuration Protocol](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink") (DHCP)

  - [Preboot Execution Environment](../Page/Preboot_Execution_Environment.md "wikilink") (PXE)

  - (RIPL)

  - [UDPヘルパーアドレス](../Page/UDPヘルパーアドレス.md "wikilink")

  - (BSDP)

## 脚注

## 外部リンク

  - RFC 951 - BOOTSTRAP PROTOCOL (BOOTP)
  - [BOOTP Sequence Diagram](http://www.eventhelix.com/RealtimeMantra/Networking/Bootp.pdf) (PDF)
  - [Multicast BOOTP for configuring a network device](http://mbootp.sourceforge.net/)

[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:ネットワークブート](https://ja.wikipedia.org/wiki/Category:ネットワークブート "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.