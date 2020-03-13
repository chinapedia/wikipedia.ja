> この記事は[IPv4](https://ja.wikipedia.org/wiki/IPv4)から翻訳されています。


**Internet Protocol version 4**（インターネットプロトコルバージョン4）、**IPv4**（アイピーブイ4）は、[Internet Protocolの一種で](../Page/Internet_Protocol.md "wikilink")、[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")において[ネットワーク層](../Page/ネットワーク層.md "wikilink")に位置付けられる[プロトコル](../Page/プロトコル.md "wikilink")である。

転送の単位である[パケット](../Page/パケット.md "wikilink")の経路選択と、その断片化と再構築を主な機能とする。[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")の基本機能として[インターネット](../Page/インターネット.md "wikilink")などで世界中広く用いられている。

## パケット

IPパケットの先頭には必ずIPヘッダが付加され、それにより経路選択などのIPの機能が実現されている。IPヘッダは12のフィールドと拡張情報（オプション）から成り立っている。拡張情報を含まないIPヘッダ長は20[オクテットである](https://ja.wikipedia.org/wiki/オクテット_\(コンピュータ\) "wikilink")。

以下にパケット形式図とそれぞれの領域の役割などを記す。

<table>
<caption><strong>パケット形式図</strong></caption>
<thead>
<tr class="header">
<th><p>0</p></th>
<th><p>1</p></th>
<th><p>2</p></th>
<th><p>3</p></th>
<th><p>4</p></th>
<th><p>5</p></th>
<th><p>6</p></th>
<th><p>7</p></th>
<th><p>8</p></th>
<th><p>9</p></th>
<th><p>10</p></th>
<th><p>11</p></th>
<th><p>12</p></th>
<th><p>13</p></th>
<th><p>14</p></th>
<th><p>15</p></th>
<th><p>16</p></th>
<th><p>17</p></th>
<th><p>18</p></th>
<th><p>19</p></th>
<th><p>20</p></th>
<th><p>21</p></th>
<th><p>22</p></th>
<th><p>23</p></th>
<th><p>24</p></th>
<th><p>25</p></th>
<th><p>26</p></th>
<th><p>27</p></th>
<th><p>28</p></th>
<th><p>29</p></th>
<th><p>30</p></th>
<th><p>31</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>バージョン</p></td>
<td><p>ヘッダ長</p></td>
<td><p>サービス種別</p></td>
<td><p>全長</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>識別子</p></td>
<td><p>フラグ</p></td>
<td><p>断片位置</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>生存時間</p></td>
<td><p>プロトコル</p></td>
<td><p>チェックサム</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>送信元アドレス</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>宛先アドレス</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>拡張情報</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>データ<br />
<br />
</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

  - **バージョン**（**Version**）　IPのバージョンであり、IPv4の場合は4が格納される。
  - **ヘッダ長**（**Internet Header Length**、**IHL**）　IPヘッダの長さで、4オクテット単位で表される。この値によりデータの開始位置を知ることができる。通常は「5」が入る。

| 0   | 1   | 2   | 3   | 4  | 5 | 6 | 7 |
| --- | --- | --- | --- | -- | - | - | - |
| 優先度 | 遅延度 | 転送量 | 信頼性 | 予備 |   |   |   |

**サービス種別**

  - **サービス種別**（**[Type of Service](https://ja.wikipedia.org/wiki/Type_of_Service "wikilink")**、**ToS**、優先順位）　パケットが転送される際に重視するサービスを指定する。ただし、ルータの実装においてパケットごとにサービスを区別することは容易ではない。送信元が全てを重視とする設定を行う場合や、ネットワークの運用方針によっては境界に位置するルータが値を書き換える場合もある。**優先度**はパケットの優先度を8段階で示す。パケットの送信[待ち行列を](../Page/キュー_\(コンピュータ\).md "wikilink")8個用いて実現する実装もある。**遅延度**はパケットを早く宛先へと到達させることを求める。**転送量**はパケットを多く宛先へと到達させることを求める。**信頼性**はパケットを失わず宛先へと到達させることを求める（このような処理を[QoSと呼ぶ](../Page/Quality_of_Service.md "wikilink")）。[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")の[IPv6パケット](https://ja.wikipedia.org/wiki/IPv6パケット "wikilink")では、サービス種別の代わりに「フローラベル」（Flow Label）が定義されている。
  - **全長**（**Total Length**）　IPヘッダを含むパケットの全長をオクテット単位で表したもの。最大は65,535オクテット。
  - **識別子**（**Identification**、**識別番号とも**）　パケットの送信元が一意な値を格納する。断片化したパケットの復元に用いられる。パケットを転送するルータがデータを分割したときにバラバラになった複数のパケットを同一のものと判断する。

| 0  | 1  | 2  |
| -- | -- | -- |
| 予備 | 禁止 | 継続 |

**フラグ**

  - **[フラグ](../Page/フラグ_\(コンピュータ\).md "wikilink")**（**Various Control Flags**）　断片化の制御に用いる。ビット0は予備であり常に0。ビット1は1の場合に断片化の禁止を意味する。ビット2は1の場合に断片化された後続のパケットが存在するパケットであることを意味し、0の場合は後続のパケットが存在しないことを意味する。
  - **断片位置**（**Fragment Offset**）　[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")などがパケットを断片化した際に、その位置を8オクテット単位で格納する。断片化したパケットの復元に用いられる。以上の識別子、フラグ、断片位置の情報から[フラグメントを行うことができる](../Page/フラグメンテーション.md "wikilink")。
  - **[生存時間](../Page/Time_to_live.md "wikilink")**（**Time to Live**、**TTL**）　パケットの余命を示す値である。送信元はパケットが経由できるルータ数の上限を設定し、ルータはパケットを転送するごとに値を一つ減らし、値が0になるとパケットは破棄される。パケットがネットワーク上で無限に巡回する問題を防ぐ効果がある。TTLは8ビットのため0〜255の値をセットできる。
  - **プロトコル**（**Protocol**）　[TCPなどの上位プロトコルを示す](../Page/Transmission_Control_Protocol.md "wikilink")[プロトコル番号](https://ja.wikipedia.org/wiki/プロトコル番号 "wikilink")が設定される。パケットの宛先である装置がパケットを受信すると、この値を用いて上位プロトコルを識別し、その実装へ[ペイロードを渡す](https://ja.wikipedia.org/wiki/ペイロード_\(コンピュータ\) "wikilink")。主に使われるプロトコルには、[ICMP](https://ja.wikipedia.org/wiki/ICMP "wikilink")、[TCP](../Page/Transmission_Control_Protocol.md "wikilink")、[UDP](../Page/User_Datagram_Protocol.md "wikilink")、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")、[EIGRP](https://ja.wikipedia.org/wiki/EIGRP "wikilink")、[OSPF](https://ja.wikipedia.org/wiki/OSPF "wikilink")が挙げられる。
  - **[チェックサム](../Page/チェックサム.md "wikilink")**（**検査合計**、**Header Checksum**）　IPヘッダの誤り検査に用いられる。転送ごとに生存時間の値が変わるため、ルータはチェックサムも転送ごとに再計算する必要がある。データ部分に関してはTCPなどの上位層に任せ、IPパケットのヘッダのチェックサムの対象はヘッダ部分だけである。また、IPパケットのチェックサムフィールドは設定必須の項目なので省略できない。[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")ではチェックサムフィールドはなくなった。
  - **送信元アドレス**（**Source Address**）　[パケット](../Page/パケット.md "wikilink")の送信元[IPアドレス](../Page/IPアドレス.md "wikilink")が設定される。
  - **宛先アドレス**（**Destination Address**）　[パケット](../Page/パケット.md "wikilink")の送信先[IPアドレス](../Page/IPアドレス.md "wikilink")が設定される。
  - **拡張情報**（**Options**）　可変長の拡張情報が32ビット単位で設定される。めったに使用されることがないが、セキュリティ、ルーズソースルーティング/ストリクトソースルーティング、レコードルート、インターネットタイムスタンプなどの情報が埋め込まれる。可変長のため0を足す[パディング](https://ja.wikipedia.org/wiki/パディング "wikilink")を必要とする。
  - **データ**　パケットが伝達すべきペイロードである。

## アドレス

IPで用いられる32ビットのアドレスは**[IPアドレス](../Page/IPアドレス.md "wikilink")**と呼ばれ、IPアドレスは**[ネットワークアドレス](https://ja.wikipedia.org/wiki/ネットワークアドレス "wikilink")**と**[ホストアドレス](https://ja.wikipedia.org/wiki/ホストアドレス "wikilink")**に分けて用いられる。

RFC 791において、[ネットワークアドレス](https://ja.wikipedia.org/wiki/ネットワークアドレス "wikilink")と[ホストアドレス](https://ja.wikipedia.org/wiki/ホストアドレス "wikilink")の境界は、IPアドレスの先頭のビット列で定められ、境界の位置によりIPアドレスは**クラス**（**class**）として分類された。

| クラス | 0 | 1      | 2      | 3         | 4   | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 | 27 | 28 | 29 | 30 | 31 |
| --- | - | ------ | ------ | --------- | --- | - | - | - | - | - | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| a   | 0 | ネットワーク | ホスト    |           |     |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| b   | 1 | 0      | ネットワーク | ホスト       |     |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| c   | 1 | 1      | 0      | ネットワーク    | ホスト |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
|     | 1 | 1      | 1      | 拡張アドレスモード |     |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |

しかしRFC 791の方式は、[ホストアドレス](https://ja.wikipedia.org/wiki/ホストアドレス "wikilink")の割り当て数が、クラスaでは16777215、クラスbでは65535にものぼる。これほどの膨大な数のホストを収容するネットワークは一般に存在せず、アドレスの利用に無駄を生じた。そこでRFC 950において**[サブネット](https://ja.wikipedia.org/wiki/サブネット "wikilink")**（**subnet**）が定められた。サブネットは[ホストアドレス](https://ja.wikipedia.org/wiki/ホストアドレス "wikilink")の一部を**アドレスマスク**（**address mask**）を用いて分割することにより得られ、ある[ネットワークアドレス](https://ja.wikipedia.org/wiki/ネットワークアドレス "wikilink")を与えられた組織内において、更にネットワークを分割するために用いられる。

|         | 0 | 1 | 2      | 3     | 4   | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 | 27 | 28 | 29 | 30 | 31 |
| ------- | - | - | ------ | ----- | --- | - | - | - | - | - | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
|         | 1 | 0 | ネットワーク | サブネット | ホスト |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| アドレスマスク | 1 | 1 | 1      | 1     | 1   | 1 | 1 | 1 | 1 | 1 | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |

RFC 1597においては、ある組織内で私的に用いられる下記の**[プライベートアドレス](https://ja.wikipedia.org/wiki/プライベートネットワーク "wikilink")**が定められた。

  - 10.0.0.0〜10.255.255.255（10.0.0.0/8）
  - 172.16.0.0〜172.31.255.255（172.16.0.0/12）
  - 192.168.0.0〜192.168.255.255（192.168.0.0/16）

上記のアドレス以外は**グローバルアドレス**とも呼ばれるようになる。

### 予約アドレス一覧

\[1\]

| アドレス            | 種別                                                                                                                         | 規約              |
| --------------- | -------------------------------------------------------------------------------------------------------------------------- | --------------- |
| 0.0.0.0/8       | Current network (only valid as source address)                                                                             | RFC 1122        |
| 10.0.0.0/8      | プライベートアドレス                                                                                                                 | RFC 1918        |
| 100.64.0.0/10   | ISP Shared Address                                                                                                         | RFC 6598        |
| 127.0.0.0/8     | [ローカルホストアドレス](../Page/Localhost.md "wikilink")                                                                             | RFC 1122        |
| 169.254.0.0/16  | LINKLOCALアドレス（[APIPA](../Page/APIPA.md "wikilink")用）                                                                       | RFC 3927        |
| 172.16.0.0/12   | プライベートアドレス                                                                                                                 | RFC 1918        |
| 192.0.0.0/24    | IETF Protocol Assignments                                                                                                  | RFC 5736        |
| 192.0.2.0/24    | ドキュメント記述用アドレス                                                                                                              | RFC 5737        |
| 192.88.99.0/24  | [6to4](https://ja.wikipedia.org/wiki/6to4 "wikilink") [IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")からIPv4への変換方式の一つ | RFC 3068        |
| 192.168.0.0/16  | プライベートアドレス                                                                                                                 | RFC 1918        |
| 198.18.0.0/15   | ネットワーク性能試験                                                                                                                 | RFC 2544        |
| 198.51.100.0/24 | ドキュメント記述用アドレス                                                                                                              | RFC 5737        |
| 203.0.113.0/24  | ドキュメント記述用アドレス                                                                                                              | RFC 5737        |
| 224.0.0.0/4     | [マルチキャスト](https://ja.wikipedia.org/wiki/IPマルチキャスト "wikilink")（クラスD）                                                        | RFC 3171        |
| 240.0.0.0/4     | 予約（クラスE）                                                                                                                   | RFC 1112        |
| 255.255.255.255 | ブロードキャスト                                                                                                                   | RFC 919,RFC 922 |
|                 |                                                                                                                            |                 |

  - 14.0.0.0/8は、Public data networkのために予約されていたが(RFC 1700)、2008年2月に予約は解除された\[2\]。
  - 24.0.0.0/8は、ケーブルテレビネットワークのために予約されていたが(RFC 3330)、2010年5月現在では予約は解除されている\[3\]。
  - 39.0.0.0/8は、Class A Subnet Experimentとして予約されていたが(RFC 1797)、2010年5月現在では予約は解除されている\[4\]。
  - 128.0.0.0/16は、RFC 3330において予約されていたが、2010年5月現在では予約は解除されている\[5\]。
  - 191.255.0.0/16は、RFC 3330において予約されていたが、2010年5月現在では予約は解除されている\[6\]。
  - 223.255.255.0/24は、RFC 3330において予約されていたが、2010年5月現在では予約は解除されている\[7\]。

## 経路選択

**[ルーティング](../Page/ルーティング.md "wikilink")**（**routing**）とも呼ばれ、パケットを宛先へと転送する機能である。この機能は[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")に集約され、多くのホストはデフォルト経路としてルータのアドレスを記述するスタイルを取ることが多い。

<table>
<tbody>
<tr class="odd">
<td><p><strong>ネットワーク構成図</strong></p></td>
</tr>
<tr class="even">
<td><div style="border:1px solid black;float:right;position:relative;width:300px;height:200px;font-size:12px">
<div style="position:absolute;top:010px;left:110px;width:080px;height:040px;border:1px solid black;text-align:center;">
</div>
<div style="position:absolute;top:050px;left:152px;text-align:right;">
<p>192.168.1.2</p>
</div>
<div style="position:absolute;top:073px;left:110px;text-align:right;">
<p>ether0</p>
</div>
<div style="position:absolute;top:073px;left:152px;text-align:right;">
<p>192.168.1.1</p>
</div>
<div style="position:absolute;top:050px;left:150px;width:001px;height:040px;background:black">
</div>
<div style="position:absolute;top:090px;left:110px;width:080px;height:040px;border:1px solid black;text-align:center;">
<p>127.0.0.1<br />
loopback</p>
</div>
<div style="position:absolute;top:130px;left:110px;text-align:right;">
<p>ether1</p>
</div>
<div style="position:absolute;top:130px;left:152px;text-align:right;">
<p>10.1.1.1</p>
</div>
<div style="position:absolute;top:150px;left:020px;width:080px;height:040px;border:1px solid black;text-align:center;">
</div>
<div style="position:absolute;top:150px;left:200px;width:080px;height:040px;border:1px solid black;text-align:center;">
</div>
<div style="position:absolute;top:130px;left:150px;width:001px;height:040px;background:black">
</div>
<div style="position:absolute;top:170px;left:100px;width:100px;height:001px;font-size:0px;background:black">
</div>
<div style="position:absolute;top:170px;left:102px;text-align:right;">
<p>10.1.1.2</p>
</div>
<div style="position:absolute;top:170px;left:153px;text-align:right;">
<p>10.1.1.3</p>
</div>
<div style="position:absolute;top:110px;left:060px;width:001px;height:040px;background:black">
</div>
<div style="position:absolute;top:083px;left:030px;text-align:right;">
<p>172.16/16</p>
</div>
</div></td>
</tr>
<tr class="odd">
<td><table>
<caption>経路表</caption>
<thead>
<tr class="header">
<th><p>destination</p></th>
<th><p>nexthop</p></th>
<th><p>interface</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>default</p></td>
<td><p>192.168.1.2</p></td>
<td><p>ether0</p></td>
</tr>
<tr class="even">
<td><p>192.168.1.1/32</p></td>
<td><p>127.0.0.1</p></td>
<td><p>loopback</p></td>
</tr>
<tr class="odd">
<td><p>192.168.1.2/32</p></td>
<td><p>192.168.1.2</p></td>
<td><p>ether0</p></td>
</tr>
<tr class="even">
<td><p>10.1.1.1/32</p></td>
<td><p>127.0.0.1</p></td>
<td><p>loopback</p></td>
</tr>
<tr class="odd">
<td><p>10.1.1.2/32</p></td>
<td><p>10.1.1.2</p></td>
<td><p>ether1</p></td>
</tr>
<tr class="even">
<td><p>10.1.1.3/32</p></td>
<td><p>10.1.1.3</p></td>
<td><p>ether1</p></td>
</tr>
<tr class="odd">
<td><p>172.16/16</p></td>
<td><p>10.1.1.2</p></td>
<td><p>ether1</p></td>
</tr>
<tr class="even">
<td><p>10.255.255.255/32</p></td>
<td><p>10.1.1.1</p></td>
<td><p>ether1</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

ルータは**経路表**（**[ルーティングテーブル](../Page/ルーティングテーブル.md "wikilink")**、**routing table**）に基づき経路選択を行う。あるネットワークの構成図とその中心に位置するルータの経路表を右に示す。図中において中心のルータは二つの送受信口を持っており、上の口はether0と名付けられアドレスは192.168.1.1が割り振られている。下の口はether1と名付けられアドレスは10.1.1.1が割り振られている。ルータ内部においてloopbackとはルータ自身を示す送受信口であり、127.0.0.1はルータ自身を現すアドレスである。表中においてdestinationは宛先、nexthopは転送先、interfaceは送信口を意味する（アドレスの記法については「[IPアドレス](../Page/IPアドレス.md "wikilink")」を参照）。

このルータがパケットを受信した際の動作を解説する。192.168.1.1宛のパケットを受信すると、ルータは経路表の宛先を検索し、192.168.1.1/32の行を見つけ、その転送先はルータ自身であることから、自身に宛てられたパケットであることを判別する。192.168.1.2宛のパケットを受信すると、ルータは経路表を検索し、ether0から192.168.1.2に向けてパケットを送出する。10.1.1.2宛のパケットを受信すると、同様にether1から10.1.1.2に向けてパケットを送出する。 172.16.1.1宛のパケットを受信すると、ルータは最長一致する172.16/16の行を見つけ、10.1.1.2が172.16.1.1へと至る経路であると判別し、ether1から10.1.1.2に向けてパケットを送出する。 10.255.255.255宛のパケットを受信する。このアドレスはブロードキャストアドレスと呼ばれ、10/8のネットワークに接続された全ての装置を宛先とするアドレスである。ether1から10/8のネットワークに接続された全ての装置に向けてパケットを送出する。 7.7.7.7宛のパケットを受信する。このアドレスは経路表には存在しないため、defaultの行に最長一致し、ネクストホップである192.168.1.2に向かってパケットを送出する。192.168.1.2は[デフォルトゲートウェイ](https://ja.wikipedia.org/wiki/デフォルトゲートウェイ "wikilink")や[デフォルトルート](https://ja.wikipedia.org/wiki/デフォルトルート "wikilink")などと呼ばれ、通常は端末から見てより中心に位置するルータが設定される。

経路表の構築はルータの管理者が手動で設定する場合と、[RIP](https://ja.wikipedia.org/wiki/ルーティング・インフォメーション・プロトコル "wikilink")、[OSPFなどの](https://ja.wikipedia.org/wiki/オープン・ショーテスト・パス・ファースト "wikilink")[ルーティングプロトコル](https://ja.wikipedia.org/wiki/ルーティングプロトコル "wikilink")を用いて自動で設定する場合がある。前者は静的経路、後者は動的経路などとも呼ばれる。経路表は[パソコンなどにも存在し](../Page/パーソナルコンピュータ.md "wikilink")、[Windowsであれば](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")「route print」、[UNIX](../Page/UNIX.md "wikilink")系であれば「[netstat](https://ja.wikipedia.org/wiki/netstat "wikilink") -r」または「[ip](https://ja.wikipedia.org/wiki/:en:iproute2 "wikilink") route」で見ることができる。

## 断片化と再構築

[プロトコル](../Page/プロトコル.md "wikilink")が転送する単位の最大長を、**[MTU](../Page/Maximum_Transmission_Unit.md "wikilink")**（**最大転送単位**、**Max Transfer Unit**）と呼ぶ。IPパケットの最大長は65535[オクテットであるが](../Page/8ビット.md "wikilink")、IPパケットを伝送すべき[データリンク層](../Page/データリンク層.md "wikilink")のMTUは、IPの最大長と比べると短い場合が多く、例えば通常の[イーサネット](../Page/イーサネット.md "wikilink")のMTUは1500オクテットである。

**断片化**（英語：**Fragmentation**、**フラグメント化**、**フラグメンテーション**とも呼ばれる\[8\]\[9\]）は、IPパケットがパケットを送出する[伝送路](../Page/伝送路.md "wikilink")のMTUよりも長い場合に発生する。断片化を行う装置はIPパケットを伝送路のMTUに収まる長さに分割し、分割されたパケットのIPヘッダは、全長が分割された長さになり、断片位置には分割された位置が記され、最後のパケット以外は継続フラグが設定される。識別子は分割された全てのパケットに分割前のパケットのそれが写される。

断片化したパケットの**再構築**（英語：**Reassembly**、**再構成**とも呼ばれる\[10\]）は、パケットの宛先である装置が行う。ある識別子を持つパケットの断片を受信した宛先は、さらに同じ識別子を持つパケットの断片を受信し、それぞれの断片位置から断片化前のパケットを再構築する。

IPヘッダのフラグの禁止ビットを設定すれば、パケットの断片化を禁止できる。この場合は断片化の代わりに[ICMP](https://ja.wikipedia.org/wiki/ICMP "wikilink")の宛先到達不可通知がパケットの送信元に返される。送信元はこれを利用して宛先に至る経路の最小MTUを調査することも可能である。パケットの長さを1オクテットずつ減らし、宛先到達不可通知が返らなくなる長さを調べればよい。

断片化は帯域やルータの負荷に無駄（オーバーヘッド）を生じ、スループットの低下となるため好まれない。[経路MTU探索](https://ja.wikipedia.org/wiki/経路MTU探索 "wikilink")を行いMTUを調整するとよい。なお、IPv6では経路上のルータで断片化・再構築を行うことはなく、送信ホストのみで行われる。

## IPv4アドレスの枯渇

IPv4のグローバルアドレスが枯渇してしまい、新規にIPv4のグローバルアドレスを割り当てることができなくなるため、インターネット上に公開されたIP機器を増設することが不可能になる問題である。既にIANA([Internet Assigned Numbers Authority](../Page/Internet_Assigned_Numbers_Authority.md "wikilink"))の管理するIPv4アドレスは[2011年](../Page/2011年.md "wikilink")[2月3日](../Page/2月3日.md "wikilink")に枯渇した。また、各RIR([地域インターネットレジストリ](../Page/地域インターネットレジストリ.md "wikilink"))の管理するアドレスも早いところでは2011年4月下旬までには枯渇すると予想されている\[11\]\[12\]。

この枯渇問題の対策として、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")の普及が進められている。

## RFC仕様

  - RFC 791 - Internet Protocol
  - RFC 950 - Internet Standard Subnetting Procedure
  - RFC 1112 - Host Extensions for IP Multicasting
  - RFC 1518 - An Architecture for IP Address Allocation with [CIDR](https://ja.wikipedia.org/wiki/CIDR "wikilink")
  - RFC 1519 - Classless Inter-Domain Routing (CIDR): an Address Assignment and Aggregation Strategy
  - RFC 1597 - Address Allocation for Private Internets
  - RFC 1817 - CIDR and Classful Routing
  - RFC 2101 - IPv4 Address Behaviour Today

## 脚注

## 関連項目

  - [Request for Comments](../Page/Request_for_Comments.md "wikilink")（RFC）
  - [Internet Protocol](../Page/Internet_Protocol.md "wikilink")
  - [キャリアグレードNAT](https://ja.wikipedia.org/wiki/キャリアグレードNAT "wikilink")
  - [IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")

[Category:インターネット層プロトコル](https://ja.wikipedia.org/wiki/Category:インターネット層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink")

1.  [IANA IPv4 Address Space Registry](http://www.iana.org/assignments/ipv4-address-space/ipv4-address-space.xml)
2.  RFC 5735
3.
4.
5.
6.
7.
8.   - フラグメント化と呼ばれる例。
9.   - フラグメンテーションと呼ばれる例。
10.  - 再構成と呼ばれる例。
11. [IPv4 Address Report](http://ipv4.potaroo.net/)
12. [IPv4アドレスの在庫枯渇に関して](http://www.nic.ad.jp/ja/ip/ipv4pool/) - 社団法人日本ネットワークインフォメーションセンター(JPNIC)