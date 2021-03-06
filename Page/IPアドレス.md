> この記事は[IPアドレス](https://ja.wikipedia.org/wiki/IPアドレス)から翻訳されています。


**IPアドレス**（アイピーアドレス、）とは、[IPにおいて](../Page/Internet_Protocol.md "wikilink")[パケット](../Page/パケット.md "wikilink")を送受信する機器を判別するための番号である。

## 概説

IPアドレスは、[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")上の[情報機器](../Page/情報機器.md "wikilink")を識別するために指定するネットワーク層における識別用の番号である。データリンク層のMACアドレスを物理アドレスということに対応して、論理アドレスとも呼ばれる。IPのバージョン（[IPv4](../Page/IPv4.md "wikilink")と[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")）に応じて、IPv4のIPアドレス（[IPv4アドレス](https://ja.wikipedia.org/wiki/IPv4アドレス "wikilink")）とIPv6のIPアドレス（[IPv6アドレス](https://ja.wikipedia.org/wiki/IPv6アドレス "wikilink")）とがある。当初RFC 791でIPを定義した際に、IPが現在のIPv4に当たるもののみであったことから、狭義では、単にIPアドレスと呼称した場合にIPv4のIPアドレスを意味する場合がある。

IPアドレスは、IPv4では32bit、IPv6では128bitの数値である。この数値のうち、MSB（[最上位ビット](https://ja.wikipedia.org/wiki/最上位ビット "wikilink")）に近い側をネットワーク部、LSB（[最下位ビット](../Page/最下位ビット.md "wikilink")）に近い側をホスト部として区別する。ネットワーク部がネットワークを指定し、ホスト部がそのネットワーク内の機器を指定する。ネットワーク部とホスト部の区別には[サブネットマスク](../Page/サブネットマスク.md "wikilink")を用いる。

## 表記

[thumbに変換し](https://ja.wikipedia.org/wiki/ファイル:Ipv4_address_ja.svg "wikilink")、8桁の数字（8ビット）で1バイトとなる。その8ビットが4つに区切られ、合計で32ビット（= 4バイト）となっている。 \]\]  IPv4のIPアドレスの表記法には以下の規則がある。*IPv6については[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")および[IPv6アドレス](https://ja.wikipedia.org/wiki/IPv6アドレス "wikilink")の記事で取り扱う。*

  - 通常は、ドット付き十進表記\[1\]あるいはドットアドレス\[2\]と呼ばれる0-255の数字4組（8ビット × 4 = 32ビット）を[ドット](../Page/ドット.md "wikilink")で繋いだ記法で表記される。
      - （例）192.168.0.1

`gethostbyname()` や `inet_aton()` など、IPアドレスを解釈する実装の一部では以下のような表記も許している。

  - 数字が3組のときは、3番目は16ビットと解釈される。
      - （例）192.168.1 (= 192.168.0.1)
  - 数字が2組のときは、2組目は24ビットと解釈される。
      - （例）192.11010049 (= 192.168.0.1、**168** × 256<sup>2</sup> + **0** × 256 + **1** = 11010049)
  - ドットがないときは、単一の32ビット数と解釈される。ロングIPアドレスなどとも呼ばれる。
      - （例）3232235521 (= 192.168.0.1、**192** × 256<sup>3</sup> + **168** × 256<sup>2</sup> + **0** × 256 + **1** = 3232235521)
  - 各数字は0xを前置すると16進数、0を前置すると8進と解釈される。
      - （例）`0xC0A80001` (= 192.168.0.1)
      - （例）`0xC0.0250.1` (= 192.168.0.1、(C0→192、250→168))

これらの表記は、URL Standardで[URLの一部分として定義されている](../Page/Uniform_Resource_Locator.md "wikilink")\[3\]\[4\]。ただし、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) やアプリケーション（例：[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")ソフト）、ネットワーク機器等によっては利用できないことがある。また悪意のある者が[フィッシングサイトなどのURLを偽装するために用いる場合もあるので](../Page/フィッシング_\(詐欺\).md "wikilink")、注意が必要である。

## アドレスクラス

IPアドレスは、次の5つのアドレスクラスに分かれている。

| クラス  | アドレス範囲                      | 用途（先頭ビットの値）                                                                                                                                                                      |
| ---- | --------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| クラスA | 0.0.0.0 - 127.255.255.255   | [ネットワークアドレス長は](https://ja.wikipedia.org/wiki/サブネットマスク#ネットワークアドレス "wikilink")8ビット、[ホストアドレス長は](https://ja.wikipedia.org/wiki/サブネットマスク#ホストアドレス "wikilink")24ビット。RFC 791で規定。（0-で始まる） |
| クラスB | 128.0.0.0 - 191.255.255.255 | ネットワークアドレス長は16ビット、ホストアドレス長も16ビット。RFC 791で規定。（10-で始まる）                                                                                                                            |
| クラスC | 192.0.0.0 - 223.255.255.255 | ネットワークアドレス長は24ビット、ホストアドレス長は8ビット。RFC 791で規定。（110-で始まる）                                                                                                                            |
| クラスD | 224.0.0.0 - 239.255.255.255 | [IPマルチキャスト](https://ja.wikipedia.org/wiki/IPマルチキャスト "wikilink")専用。RFC 1112で規定。（1110-で始まる）                                                                                        |
| クラスE | 240.0.0.0 - 255.255.255.255 | 将来の使用のために予約されている。RFC 1112で規定。（1111-で始まる）                                                                                                                                         |

クラスAからクラスCまでは、ネットワーク部とホスト部の境界が8ビット単位で区分けされている。クラスAはネットワーク部が短く（8ビット）、ホスト部が長い（24ビット）。すなわち、多くの機器を保有する大組織や多くの顧客を有する大規模な[インターネットサービスプロバイダ](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink") (ISP) に割り当てるのに適している。クラスCはその逆である。これは、日本の[電話番号](../Page/電話番号.md "wikilink")において[東京](../Page/東京.md "wikilink")などの人口が多い地域には03のような短い[市外局番](../Page/市外局番.md "wikilink")が割り当てられ、人口の少ない地域には長い市外局番が割り当てられているのと同じである。クラスAが約1,677万台、クラスBが65,534台、クラスCが254台のホストを接続できる。

しかし、アドレスクラスを用いたIPアドレス割り当てには問題が生じた。ほとんどのネットワーク（たとえばインターネットサービスプロバイダ）ではクラスAでは大きすぎ、クラスCでは小さすぎたため割り当ての要求がクラスBに集中したのである。クラスBの割り当てを受けたネットワークの中には65,534台のホスト（インターネットサービスプロバイダであれば接続ユーザー数）を同時にすべて接続することがまれであるネットワークも存在し、IPアドレスが無駄に消費されることになった。そこで現在ではアドレスクラスを使わず、ネットワーク部とホスト部の境界を8ビット単位に固定せずに細分化する可変長[サブネットマスク](../Page/サブネットマスク.md "wikilink")やCIDR ([Classless Inter-Domain Routing](https://ja.wikipedia.org/wiki/Classless_Inter-Domain_Routing "wikilink")) の使用が一般化している。

IPアドレスの割り当て範囲を示すために、IPアドレスの末尾に「/」（[スラッシュ](../Page/スラッシュ_\(記号\).md "wikilink")）とともにネットワークアドレス長を付記して表すことも多い。IPv4の場合、MSB側からのビット数でネットワークアドレス長を表す。例えば192.168.0.0/24の表記の場合、ネットワーク部はMSBから24ビットで残り8ビットがホスト部となる。アドレスクラスでなく可変長サブネットマスクを使用した場合、ネットワークアドレス長の数字は必ずしも8の倍数にはならないことになる。

### CIDR表

「CIDR」は、「サイダー」と読む。

を用いることで、192.168.1.0-192.168.1.255という複数のIPアドレスを範囲指定させることができる。活用方法としては、ウィキペディアで行われている[広域ブロックといった特定の範囲内のIPアドレスを持つ利用者の編集ブロックなどがある](https://ja.wikipedia.org/wiki/Wikipedia:広域ブロック "wikilink")。

例えば69.208.0.0を含むIPアドレス群の場合、CIDRと開始アドレス及び終了アドレスの関係は以下のようになる。

| CIDR              | 開始アドレス     | 終了アドレス          | 含まれるアドレス数     | 二進法表記したアドレス数                                                        |
| ----------------- | ---------- | --------------- | ------------- | ------------------------------------------------------------------- |
| 69.208.0.0**/0**  | 0.0.0.0    | 255.255.255.255 | 4,294,967,296 | \*\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\* |
| 69.208.0.0**/1**  | 0.0.0.0    | 127.255.255.255 | 2,147,483,648 | 0\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\*  |
| 69.208.0.0**/4**  | 64.0.0.0   | 79.255.255.255  | 268,435,456   | 0100\*\*\*\*.\*\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\*     |
| 69.208.0.0**/8**  | 69.0.0.0   | 69.255.255.255  | 16,777,216    | 01000101.\*\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\*         |
| 69.208.0.0**/11** | 69.192.0.0 | 69.223.255.255  | 2,097,152     | 01000101.110\*\*\*\*\*.\*\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\*            |
| 69.208.0.0**/12** | 69.208.0.0 | 69.223.255.255  | 1,048,576     | 01000101.1101\*\*\*\*.\*\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\*             |
| 69.208.0.0**/13** | 69.208.0.0 | 69.215.255.255  | 524,288       | 01000101.11010\*\*\*.\*\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\*              |
| 69.208.0.0**/14** | 69.208.0.0 | 69.211.255.255  | 262,144       | 01000101.110100\*\*.\*\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\*               |
| 69.208.0.0**/15** | 69.208.0.0 | 69.209.255.255  | 131,072       | 01000101.1101000\*.\*\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\*                |
| 69.208.0.0**/16** | 69.208.0.0 | 69.208.255.255  | 65,536        | 01000101.11010000.\*\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\*                 |
| 69.208.0.0**/17** | 69.208.0.0 | 69.208.127.255  | 32,768        | 01000101.11010000.0\*\*\*\*\*\*\*.\*\*\*\*\*\*\*\*                  |
| 69.208.0.0**/18** | 69.208.0.0 | 69.208.63.255   | 16,384        | 01000101.11010000.00\*\*\*\*\*\*.\*\*\*\*\*\*\*\*                   |
| 69.208.0.0**/19** | 69.208.0.0 | 69.208.31.255   | 8,192         | 01000101.11010000.000\*\*\*\*\*.\*\*\*\*\*\*\*\*                    |
| 69.208.0.0**/20** | 69.208.0.0 | 69.208.15.255   | 4,096         | 01000101.11010000.0000\*\*\*\*.\*\*\*\*\*\*\*\*                     |
| 69.208.0.0**/21** | 69.208.0.0 | 69.208.7.255    | 2,048         | 01000101.11010000.00000\*\*\*.\*\*\*\*\*\*\*\*                      |
| 69.208.0.0**/22** | 69.208.0.0 | 69.208.3.255    | 1,024         | 01000101.11010000.000000\*\*.\*\*\*\*\*\*\*\*                       |
| 69.208.0.0**/23** | 69.208.0.0 | 69.208.1.255    | 512           | 01000101.11010000.0000000\*.\*\*\*\*\*\*\*\*                        |
| 69.208.0.0**/24** | 69.208.0.0 | 69.208.0.255    | 256           | 01000101.11010000.00000000.\*\*\*\*\*\*\*\*                         |
| 69.208.0.0**/25** | 69.208.0.0 | 69.208.0.127    | 128           | 01000101.11010000.00000000.0\*\*\*\*\*\*\*                          |
| 69.208.0.0**/26** | 69.208.0.0 | 69.208.0.63     | 64            | 01000101.11010000.00000000.00\*\*\*\*\*\*                           |
| 69.208.0.0**/27** | 69.208.0.0 | 69.208.0.31     | 32            | 01000101.11010000.00000000.000\*\*\*\*\*                            |
| 69.208.0.0**/28** | 69.208.0.0 | 69.208.0.15     | 16            | 01000101.11010000.00000000.0000\*\*\*\*                             |
| 69.208.0.0**/29** | 69.208.0.0 | 69.208.0.7      | 8             | 01000101.11010000.00000000.00000\*\*\*                              |
| 69.208.0.0**/30** | 69.208.0.0 | 69.208.0.3      | 4             | 01000101.11010000.00000000.000000\*\*                               |
| 69.208.0.0**/31** | 69.208.0.0 | 69.208.0.1      | 2             | 01000101.11010000.00000000.0000000\*                                |
| 69.208.0.0**/32** | 69.208.0.0 | 69.208.0.0      | 1             | 01000101.11010000.00000000.00000000                                 |

  - 表の見方の例
      - 69.208.0.0/16は、69.208.0.0から69.208.255.255までの65,536アドレス範囲を含む。
      - 69.208.0.0/24は、69.208.0.0から69.208.0.255までの256アドレス範囲を含む。

## スコープ

通信可能な範囲のことをスコープという。IPアドレスは、それぞれにスコープが決められている。（→[一覧](https://ja.wikipedia.org/wiki/IPv4#予約アドレス一覧 "wikilink")）

### グローバルIPアドレス

後述するプライベートIPアドレス、リンクローカルアドレス、特殊用途のIPアドレスなどを除いたIPアドレスは「グローバルIPアドレス」と呼び、インターネットの接続用に利用され、重複が発生しないように管理される。そのため、[ICANN](../Page/ICANN.md "wikilink")を頂点とした階層的な委譲関係によって、世界的な管理が行われている。

通常、パソコンや[ルーター](../Page/ルーター.md "wikilink")などをインターネットに接続すると、[ISPに割り振られているグローバルIPアドレスの中の](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")1つがパソコンなどに割り当てられる。

### プライベートIPアドレス

プライベートIPアドレス（ローカルIPアドレス）は、[プライベートネットワーク](https://ja.wikipedia.org/wiki/プライベートネットワーク "wikilink")（外部から利用できない社内[LANなど](../Page/Local_Area_Network.md "wikilink")）のアドレスとして使うことができる。異なるプライベートネットワークを相互接続して[ルーティング](../Page/ルーティング.md "wikilink")することも可能である。

プライベートIPアドレスとして、次のアドレス空間が予約されている。ネットワークの規模に応じて、使い分ける必要がある。

| クラス        | 範囲                            | サブネットマスク    | アドレス数                              |
| ---------- | ----------------------------- | ----------- | ---------------------------------- |
| クラスA       | 10.0.0.0 - 10.255.255.255     | 255.0.0.0   | 16,777,216 (16,777,216 × 1 subnet) |
| クラスB × 16  | 172.16.0.0 - 172.31.255.255   | 255.240.0.0 | 1,048,576 (65,536 × 16 subnet)     |
| クラスC × 256 | 192.168.0.0 - 192.168.255.255 | 255.255.0.0 | 65,536 (256 × 256 subnet)          |

### リンクローカルアドレス

[WindowsなどではIPアドレスが設定されておらず](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、DHCPサーバも見付からない場合には自動的に169.254で始まるクラスBのIPアドレスが振られる（[APIPA](../Page/APIPA.md "wikilink")という機能）。これはリンクローカルアドレスと呼ばれ単一のLAN内での通信に使うことができるが、[ルーティング](../Page/ルーティング.md "wikilink")ができないなどプライベートアドレスとは異なるものである。

### プライベートIPアドレスとインターネット

プライベートIPアドレスとグローバルIPアドレスを相互変換することにより、インターネットに接続することができる。その方法として、NAPT（実装としては[IPマスカレードやipfwなど](../Page/ネットワークアドレス変換.md "wikilink")）や[プロキシ](../Page/プロキシ.md "wikilink")サーバがある。

[インターネット接続サービスによってはインターネットに接続する機器にグローバルIPアドレスではなく](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")、このプライベートIPアドレスを割り当てることもある\[5\]。

プライベートIPアドレスとこれに関する仕組みによって、グローバルIPアドレスを多量に消費することなくインターネットに接続できる機器を増やすことができる。

### ISP Shared Address

2012年4月にRFC 6598として発行したインターネットサービスプロバイダ (ISP) が契約者に貸し出すIPアドレスで、範囲は100.64.0.0/10。

ISP Shared Addressは、個々のISPのネットワーク内でのみ使用可能なIPアドレスで、[キャリアグレードNAT](https://ja.wikipedia.org/wiki/キャリアグレードNAT "wikilink") (CGN) によりISP Shared AddressとグローバルIPアドレスを相互変換することにより、インターネットに接続することができる。

[IPアドレス枯渇問題](../Page/IPアドレス枯渇問題.md "wikilink")により、契約者が増加しても、ISPが契約者に貸し出すグローバルIPアドレスを新規に獲得できなくなった。

しかし、ISPが契約者にプライベートIPアドレスを割り当てると、該当するIPアドレスを契約者のローカルネットワーク内で使用できなくなる。例えば、NTTが提供する[フレッツ](../Page/フレッツ.md "wikilink")の地域IP網においてプライベートIPアドレス (10.0.0.0/8) を使用しているため、[フレッツ](../Page/フレッツ.md "wikilink")の利用者がプライベートIPアドレス (10.0.0.0/8) をローカルネットワーク内で使用できない。

そこで、ISP Shared Addressの導入により、ISPはISP Shared Addressを使用し、ISPの契約者は、任意のプライベートIPアドレスが使用できるようになる。

なお、/10というアドレス範囲は、東京地域を網羅するISPがISP Shared Addressを導入するには、/10程度のアドレス範囲が必要であるという、日本からの提案がベースになっている。

## 特殊用途のIPアドレス

一部のアドレスおよびブロックは、特殊な用途に使われる。それぞれのスコープに応じて、通常、機器に割り振るべきではない。詳細は[IPv4\#予約アドレス一覧](https://ja.wikipedia.org/wiki/IPv4#予約アドレス一覧 "wikilink")を参照のこと。

## IPアドレスの付与

グローバルIPアドレスは、まずインターネットレジストリ（[APNICや](../Page/Asia-Pacific_Network_Information_Centre.md "wikilink")[JPNICなど](../Page/日本ネットワークインフォメーションセンター.md "wikilink")）から[ISPにまとまった単位で付与される](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")。これを**割り振り** (allocation) という。ISPは末端の利用者（個人、法人など）に対して、利用契約に基づいてIPアドレスを払い出す。これを**割り当て** (assignment) という。かつて一部の[大学](../Page/大学.md "wikilink")やIT企業が非営利でインターネットを支えていた時代には、レジストリからこれらの組織に直接割り当てられる例が多かったが、今日では商用ISPが発達したため、新規の割り当てではそのような例は少ない。インターネットレジストリにもIANA→RIR (Regional Internet Registry) →NIR (National Internet Registry) →LIR (Local Internet Registry) といった階層構造が存在する\[6\]。

個人契約者の場合、グローバルIPアドレス1個を動的に割り当てる（接続ごとにIPアドレスが変わることがある）ものがほとんどである。ただしISPや契約プランによってはプライベートIPアドレスやISP Shared Addressを割り当てるもの（[CATV接続に多い](../Page/ケーブルテレビ.md "wikilink")）、グローバルIPアドレス1個を固定で割り当てるもの、複数のグローバルIPアドレスを固定で割り当てるものもある。割り当ての[通信プロトコル](../Page/通信プロトコル.md "wikilink")は[ダイヤルアップ接続](../Page/ダイヤルアップ接続.md "wikilink")では[PPP](../Page/Point-to-Point_Protocol.md "wikilink")、[ADSL](../Page/ADSL.md "wikilink")・[FTTH](../Page/FTTH.md "wikilink")などでは[PPPoE](../Page/PPPoE.md "wikilink")、CATVや[公衆無線LAN](../Page/公衆無線LAN.md "wikilink")（ホットスポット）では[DHCPによることが一般的である](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")。

法人契約の場合は[DNSや](../Page/DNSサーバ.md "wikilink")[メールなどの各種](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")[サーバ](../Page/サーバ.md "wikilink")を運用するケースが多いこと、[VPN（仮想専用網）等による取引先等とのデータのやりとりにおいて](../Page/Virtual_Private_Network.md "wikilink")、IPアドレスによる認証やアクセス制限があることなどの理由により、複数（多いのは4個から16個程度）のグローバルIPアドレスを固定で割り当てる契約が一般的である。

なお、家庭内や組織内でのプライベートIPアドレスの割り当てはDHCP（専用サーバの他、一般向けのいわゆるブロードバンドルーターに実装されている）によることが一般的である。ただし、サーバやルーターのLAN側など固定IPアドレスを必要とするものや、割り当てを厳密に管理したい場合には固定IPアドレスの割り当てが行われる。

## IPアドレスと個人情報

近年、個人情報保護や[セキュリティの観点からIPアドレスは](../Page/コンピュータセキュリティ.md "wikilink")[個人情報](../Page/個人情報.md "wikilink")ではないのか、IPアドレスから個人情報やプライバシーを暴露されるのではないかといった懸念が多く見られるようになってきている。ただし、IPアドレスは公開されうるものであり、インターネットの仕組みはそれを前提として構築されている。また、通常(訴訟などではない時)はIPアドレスが分かった所で住所などは分からない。

### IPアドレスから分かること

[TCP/IPを用いた通信では](../Page/インターネット・プロトコル・スイート.md "wikilink")、常に自分のIPアドレスが通信相手に伝達される。例外として通信経路に[ゲートウェイ](../Page/ゲートウェイ.md "wikilink")（[プロキシ](../Page/プロキシ.md "wikilink")サーバ等）がある場合にはゲートウェイのIPアドレスが伝達されるが、これもゲートウェイには自分のIPアドレスが伝達される。

このIPアドレスから情報を得るには[WHOIS](../Page/WHOIS.md "wikilink")や[DNSを用いる](../Page/Domain_Name_System.md "wikilink")。WHOISはIPアドレスを割り振られている[ネットワーク管理者](https://ja.wikipedia.org/wiki/ネットワーク管理者 "wikilink")に関する情報を得られ、DNSはIPアドレスからホスト名を得られる。これらによって得られる情報のうち、登録組織名やホスト名から接続元の場所が得られる。大抵は[プロバイダ名と地域が分る程度だが](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")、会社や大学に割り振られている場合には接続元の住所が得られる事もある。

上記以外の個人情報（氏名・詳細な住所・電話番号・メールアドレスなど）をIPアドレスのみから知ることは、ISP等から個人情報と接続記録が漏洩しない限り不可能である。したがって、IPアドレスを記録・公開してもそれが現実空間において即詳細な個人情報の暴露につながるわけではない。つまり、[ワンクリック詐欺などのサイトで](https://ja.wikipedia.org/wiki/ワンクリック契約 "wikilink")、接続元のIPアドレスを表示して金銭を騙しとろうとしても、実際には、賠償請求訴訟に至らない限りサイト側は接続元の詳細な住所までは分からない。

一方で、利用者が犯罪を犯した場合はこの限りではない。[BBSの管理者やプロバイダなどのインターネットサービス提供管理者は](../Page/電子掲示板.md "wikilink")、利用者のアクセス記録を一定期間保持することが義務付けられている。日本の場合には、[特定電気通信役務提供者の損害賠償責任の制限及び発信者情報の開示に関する法律](../Page/特定電気通信役務提供者の損害賠償責任の制限及び発信者情報の開示に関する法律.md "wikilink")（プロバイダ責任制限法）で規定されている。例えば、ユーザーが殺人予告の脅迫行為や名誉毀損など何らかの損害賠償請求をされる行為ないし違法行為を犯した場合、警察ないし損害賠償請求の原告から裁判所に開示請求が出され、裁判所の許可によってそのIPアドレスを割り振られているプロバイダに連絡が入り、法的措置に基づいてIPアドレスを含むアクセスログとそれに伴う個人情報を開示するようプロバイダに請求する。従って個人間ではIPアドレスで個人情報を取り出すことは不可能だが、警察への告訴や民事訴訟などの手続きなどを経ると当該IPアドレスを使用した個人を割り出すことができる。またIPアドレスを使用した者の情報はプロバイダによって調べられるので、仮にあるIPアドレスを使用した者が何らかの不正を行ったことをそのIPアドレスから判明するプロバイダに通報するとプロバイダは基本的には内規に基づいて利用停止などの措置を執ることがある。

なお、刑事告訴や民事訴訟に至らないまでも、インターネット上でBBSや[ウィキ](../Page/ウィキ.md "wikilink")などのサービスを提供している団体が、迷惑行為や違法行為を行っている者に対して、IPアドレスで行為を制限することがある。 上記のように特定捜査権の無いユーザーが現実世界での個人情報を特定する事はほぼ不可能である。ただし、インターネット世界においてはIPアドレスは個人ユーザーのパソコンまたは個人契約のサーバを特定する物であり、[掲示板や](../Page/電子掲示板.md "wikilink")[ウィキペディア](../Page/ウィキペディア.md "wikilink")の投稿記録、ブログや各ホームページサーバー等で配布している[アクセス解析](../Page/アクセス解析.md "wikilink")を採用しているサイトには、来訪者のIPアドレスが残される。その為、来訪日時を調べる事が可能である。また、[掲示板](../Page/掲示板.md "wikilink")や[チャット](../Page/チャット.md "wikilink")などではあらかじめ特定のIPアドレスを指定する事で、対象となるIPアドレスの閲覧や投稿をブロックすることが可能である。なお、動的IPアドレスの場合、無関係なユーザーにも影響がある。また、固定IPアドレスにおいては、同一LAN内で複数ユーザーが利用している場合には、同一LAN内の全てのユーザーが対象となってしまう。

## IPアドレス枯渇問題

2019年3月現在、特殊な用途のものを除く、すべての[IPv4](../Page/IPv4.md "wikilink")のグローバルアドレスを誰かに割り当てた状態になりつつある。すなわちIPv4のグローバルアドレスに空きがなく、インターネット上に公開するIP機器の増設が不可能になるという問題が発生している。不動産に例えると、これまでは新規分譲で土地が提供されて建物を建築できていたが、分譲する土地がなくなったために、既存の建物が建っている土地を地上げして再開発しない限り新たな建物を建てられなくなった状態である。

2017年2月15日 LACNICのIPv4アドレス在庫が/11ブロック以下となり、AFRINICを除く4つのRIRでIPv4アドレス在庫枯渇の最終段階になった\[7\]。

この枯渇問題の対策として、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")の普及が進められている。

## 脚注

### 注釈

### 出典

## 関連項目

  - [IPv6アドレス](https://ja.wikipedia.org/wiki/IPv6アドレス "wikilink")
  - [IPアドレス枯渇問題](../Page/IPアドレス枯渇問題.md "wikilink")
  - [IPv4](../Page/IPv4.md "wikilink")
  - [IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")
  - [グローバルIPアドレス（クラスA）](https://ja.wikipedia.org/wiki/:en:List_of_assigned_/8_IP_address_blocks "wikilink")
  - [Domain Name System](../Page/Domain_Name_System.md "wikilink") (DNS)
  - [ホスト名](../Page/ホスト名.md "wikilink")（[ドメイン名](../Page/ドメイン名.md "wikilink")）
  - [Dynamic Host Configuration Protocol](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink") (DHCP)
  - [MACアドレス](../Page/MACアドレス.md "wikilink")
  - [ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")
  - [Mobile IP](../Page/Mobile_IP.md "wikilink")
  - [サブアロケーション](../Page/サブアロケーション.md "wikilink")
  - [アサインメントウィンドウ](https://ja.wikipedia.org/wiki/アサインメントウィンドウ "wikilink")

## 外部リンク

  - [IANA IPv4 Address Space Registry](https://www.iana.org/assignments/ipv4-address-space/ipv4-address-space.xhtml)
  - [日本におけるインターネット資源管理の歴史 | JPNIC](https://www.nic.ad.jp/timeline/20th/)

[Category:IPアドレス](https://ja.wikipedia.org/wiki/Category:IPアドレス "wikilink") [Category:Internet_Protocol](https://ja.wikipedia.org/wiki/Category:Internet_Protocol "wikilink")

1.
2.
3.
4.
5.
6.  「[インターネット用語1分解説 - 割り振り (Allocation)、割り当て (Assignment) とは](http://www.nic.ad.jp/ja/basics/terms/allocation-assignment.html)」『JPNIC News & Views』8巻（2002年1月15日）、日本ネットワークインフォメーションセンター。
7.