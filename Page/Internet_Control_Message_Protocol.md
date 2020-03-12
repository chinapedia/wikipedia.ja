> この記事は[Internet Control Message Protocol](https://ja.wikipedia.org/wiki/Internet_Control_Message_Protocol)から翻訳されています。


**Internet Control Message Protocol**（インターネット制御通知プロトコル、ICMP）とは、通信処理で使われる[プロトコル](../Page/プロトコル.md "wikilink")のひとつで、[Internet Protocolのデータグラム処理における誤りの通知や通信に関する情報の通知などのために使用される](../Page/Internet_Protocol.md "wikilink")。ICMPに関するICMP通知は、通知が無限ループに陥るのを防ぐために送られない。

[IPv4](../Page/IPv4.md "wikilink")（Internet Protocol version 4）のための ICMP (ICMPv4) は RFC 792 によって規定され、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")（Internet Protocol version 6）のための ICMP ([ICMPv6](../Page/Internet_Control_Message_Protocol_for_IPv6.md "wikilink")) は RFC 4443 によって規定されている。ICMP は TCP、UDP などと同様にInternet Protocolの上位のプロトコルであるが、Internet Protocolと同様の[インターネット層](https://ja.wikipedia.org/wiki/インターネット層 "wikilink")のプロトコルであるかのような特別の処理をされる。

ICMPを利用しているツールに[ping](https://ja.wikipedia.org/wiki/ping "wikilink")や[traceroute](https://ja.wikipedia.org/wiki/traceroute "wikilink")\[1\]などがある。

## 通知書式

ICMPヘッダは以下のようにMACヘッダ・IPヘッダの後ろにある。

`  +------------+-----------+-------------+-----------`
`  | `[`MACヘッダ`](../Page/媒体アクセス制御.md "wikilink")`  | `[`IPヘッダ`](../Page/Internet_Protocol.md "wikilink")`  | ICMPヘッダ  | データ...`
`  +------------+-----------+-------------+-----------`

### ICMPヘッダ

ICMPヘッダは一般的に以下の通りとなる。

<table>
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
<td><p>タイプ</p></td>
<td><p>コード</p></td>
<td><p><a href="../Page/チェックサム.md" title="wikilink">チェックサム</a></p></td>
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

データグラムのデータ部分の最初の[オクテットはICMPタイプフィールドであり](https://ja.wikipedia.org/wiki/オクテット_\(コンピュータ\) "wikilink")、このフィールドの値は、以降のICMP通知の書式を決定する。「未使用」とラベル付けされているフィールドは今後の拡張のために予約されており、送信時には0を入れなければならないが、受信者はこれらのフィールドを（チェックサムに含めることを除いて）使用すべきではない。チェックサムは、ICMPヘッダの先頭から（すなわちタイプから）データの末尾までを対象に、16ビット単位で算出される。チェックサムフィールド自身も計算対象に入っているが、計算時には0として扱う。バイト数が奇数の場合は末尾に0のバイトがあるものとして計算する。

また、いくつかのタイプでは、ICMP通知が発生する原因となった元データグラムの先頭部分をコピーしている。この種のタイプは以下の形式をとる。

<table>
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
<td><p>タイプ</p></td>
<td><p>コード</p></td>
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
<td><p>未使用</p></td>
<td><p>長さ</p></td>
<td><p>未使用</p></td>
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
<td><p>IPヘッダ + 元データグラムの先頭部分<br />
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

RFC 792では長さフィールドは未使用で、元データグラムの先頭部分は64[ビット](../Page/ビット.md "wikilink")（8オクテット）と決まっていた。その後RFC 1812およびRFC 4443において、MTUの最小限として保障されるサイズ（IPv4は576オクテット、IPv6は1280オクテット）まで拡張された。RFC 4884において長さフィールドが追加され、この可変長領域の長さを32ビット単位で記述することになった。

ICMP通知は基礎的なIPヘッダーを使用して送られる。個々の型式記述の下で違った形で言及されない限り、ICMPヘッダに先行するIPヘッダーフィールドの値は以下の通りとなる。

  - バージョン
    4

  - IHL
    32ビット[ワード](../Page/ワード.md "wikilink")でのインターネット・ヘッダー長である。

  - サービスの形式
    0

  - 合計長
    オクテット単位での、インターネット・ヘッダーとデータの合計の長さである。識別、フラグ、断片化オフセット、断片化の中で使用される。

  - 存在回数
    存在保持回数ともいい、このフィールドはデータグラムが処理されるマシンを通る度に1ずつ減らされる。そのためこのフィールドの値は少なくともこのデータグラムが通るゲートウェイの数と同じ大きさでなければならない。

  - プロトコル
    ICMP = 1

  - ヘッダー・チェックサム

  - 送信元アドレス
    ICMP通知を構成する[ゲートウェイ](https://ja.wikipedia.org/wiki/ゲートウェイ "wikilink")か[ホストの](https://ja.wikipedia.org/wiki/ホスト_\(ネットワーク\) "wikilink")[アドレスである](../Page/IPアドレス.md "wikilink")。違った形で言及されない限り、これは何らかのゲートウェイのアドレスとなる。

  - 宛先アドレス
    通知が送られるべきゲートウェイかホストのアドレスである。

## 通知の種類

以下の種類がある。

<table>
<caption>制御メッセージ一覧[2][3]</caption>
<thead>
<tr class="header">
<th><p>Type</p></th>
<th><p>Code</p></th>
<th><p>状態</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0 - <a href="https://ja.wikipedia.org/wiki/ICMP_Echo_Reply" title="wikilink">Echo Reply Message</a>（エコー応答通知）</p></td>
<td><p>0</p></td>
<td></td>
<td><p>Echo応答(<a href="https://ja.wikipedia.org/wiki/ping" title="wikilink">ping</a>)</p></td>
</tr>
<tr class="even">
<td><p>1 および 2</p></td>
<td></td>
<td><p>未割当</p></td>
<td><p><em>予約済み</em></p></td>
</tr>
<tr class="odd">
<td><p>3 - <a href="https://ja.wikipedia.org/wiki/ICMP_Destination_Unreachable" title="wikilink">Destination Unreachable Message</a><br />
（宛先到達不可能通知）</p></td>
<td><p>0</p></td>
<td></td>
<td><p>Destination network unreachable</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td></td>
<td><p>Destination host unreachable</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td></td>
<td><p>Destination protocol unreachable</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>3</p></td>
<td></td>
<td><p>Destination port unreachable</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4</p></td>
<td></td>
<td><p>Fragmentation required, and <a href="https://ja.wikipedia.org/wiki/IPv4_packet" title="wikilink">DF flag</a> set</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td></td>
<td><p>Source route failed</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>6</p></td>
<td></td>
<td><p>Destination network unknown</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>7</p></td>
<td></td>
<td><p>Destination host unknown</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>8</p></td>
<td></td>
<td><p>Source host isolated</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>9</p></td>
<td></td>
<td><p>Network administratively prohibited</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>10</p></td>
<td></td>
<td><p>Host administratively prohibited</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>11</p></td>
<td></td>
<td><p>Network unreachable for TOS</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>12</p></td>
<td></td>
<td><p>Host unreachable for TOS</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>13</p></td>
<td></td>
<td><p>Communication administratively prohibited</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>14</p></td>
<td></td>
<td><p>Host Precedence Violation</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>15</p></td>
<td></td>
<td><p>Precedence cutoff in effect</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4 - <a href="https://ja.wikipedia.org/wiki/ICMP_Source_Quench" title="wikilink">Source Quench Message</a><br />
（送出抑制要求通知）</p></td>
<td><p>0</p></td>
<td><p>非推奨</p></td>
<td><p>Source quench (congestion control)</p></td>
</tr>
<tr class="even">
<td><p>5 - <a href="https://ja.wikipedia.org/wiki/ICMP_Redirect" title="wikilink">Redirect Message</a><br />
（経路変更要求通知）</p></td>
<td><p>0</p></td>
<td></td>
<td><p>Redirect Datagram for the Network</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td></td>
<td><p>Redirect Datagram for the Host</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td></td>
<td><p>Redirect Datagram for the TOS &amp; network</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td></td>
<td><p>Redirect Datagram for the TOS &amp; host</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td></td>
<td><p>非推奨</p></td>
<td><p>Alternate Host Address</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td></td>
<td><p>未割当</p></td>
<td><p><em>予約済み</em></p></td>
</tr>
<tr class="even">
<td><p>8 - <a href="https://ja.wikipedia.org/wiki/ICMP_Echo" title="wikilink">Echo Message</a>（エコー要求通知）</p></td>
<td><p>0</p></td>
<td></td>
<td><p>Echo request (used to ping)</p></td>
</tr>
<tr class="odd">
<td><p>9 - <a href="https://ja.wikipedia.org/wiki/ICMP_Router_Advertisement" title="wikilink">Router Advertisement Message</a>（ルーター広告通知）</p></td>
<td><p>0</p></td>
<td></td>
<td><p>Router Advertisement</p></td>
</tr>
<tr class="even">
<td><p>10 - <a href="https://ja.wikipedia.org/wiki/ICMP_Router_Solicitation" title="wikilink">Router Solicitation Message</a>（ルーター要請通知）</p></td>
<td><p>0</p></td>
<td></td>
<td><p>Router discovery/selection/solicitation</p></td>
</tr>
<tr class="odd">
<td><p>11 - <a href="https://ja.wikipedia.org/wiki/ICMP_Time_Exceeded" title="wikilink">Time Exceeded Message</a>（時間切れ通知）<br />
</p></td>
<td><p>0</p></td>
<td></td>
<td><p>TTL expired in transit</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td></td>
<td><p>Fragment reassembly time exceeded</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>12 - <a href="https://ja.wikipedia.org/wiki/ICMP_Parameter_Problem" title="wikilink">Parameter Problem Message</a>（不正引数通知）</p></td>
<td><p>0</p></td>
<td></td>
<td><p>Pointer indicates the error</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td></td>
<td><p>Missing a required option</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td></td>
<td><p>Bad length</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>13 - <a href="https://ja.wikipedia.org/wiki/ICMP_Timestamp" title="wikilink">Timestamp Message</a><br />
（タイムスタンプ要求通知）</p></td>
<td><p>0</p></td>
<td></td>
<td><p>Timestamp</p></td>
</tr>
<tr class="odd">
<td><p>14 - <a href="https://ja.wikipedia.org/wiki/ICMP_Timestamp_Reply" title="wikilink">Timestamp Reply Message</a><br />
（タイムスタンプ応答通知）</p></td>
<td><p>0</p></td>
<td></td>
<td><p>Timestamp reply</p></td>
</tr>
<tr class="even">
<td><p>15 - <a href="https://ja.wikipedia.org/wiki/ICMP_Information_Request" title="wikilink">Information Request Message</a>（情報要求通知）</p></td>
<td><p>0</p></td>
<td><p>非推奨</p></td>
<td><p>Information Request</p></td>
</tr>
<tr class="odd">
<td><p>16 - <a href="https://ja.wikipedia.org/wiki/ICMP_Information_Reply" title="wikilink">Information Reply Message</a>（情報応答通知）</p></td>
<td><p>0</p></td>
<td><p>非推奨</p></td>
<td><p>Information Reply</p></td>
</tr>
<tr class="even">
<td><p>17 - <a href="https://ja.wikipedia.org/wiki/ICMP_Address_Mask_Request" title="wikilink">Address Mask Request Message</a><br />
（アドレスマスク要求通知）</p></td>
<td><p>0</p></td>
<td><p>非推奨</p></td>
<td><p>Address Mask Request</p></td>
</tr>
<tr class="odd">
<td><p>18 - <a href="https://ja.wikipedia.org/wiki/ICMP_Address_Mask_Reply" title="wikilink">Address Mask Reply Message</a><br />
（アドレスマスク応答通知）</p></td>
<td><p>0</p></td>
<td><p>非推奨</p></td>
<td><p>Address Mask Reply</p></td>
</tr>
<tr class="even">
<td><p>19</p></td>
<td></td>
<td><p>予約済み</p></td>
<td><p>セキュリティ向けに<em>予約済み</em></p></td>
</tr>
<tr class="odd">
<td><p>20 through 29</p></td>
<td></td>
<td><p>予約済み</p></td>
<td><p>robustness experiment向けに<em>予約済み</em></p></td>
</tr>
<tr class="even">
<td><p>30 <a href="../Page/Traceroute.md" title="wikilink">Traceroute</a></p></td>
<td><p>0</p></td>
<td><p>非推奨</p></td>
<td><p>Information Request</p></td>
</tr>
<tr class="odd">
<td><p>31</p></td>
<td></td>
<td><p>非推奨</p></td>
<td><p>Datagram Conversion Error</p></td>
</tr>
<tr class="even">
<td><p>32</p></td>
<td></td>
<td><p>非推奨</p></td>
<td><p>Mobile Host Redirect</p></td>
</tr>
<tr class="odd">
<td><p>33</p></td>
<td></td>
<td><p>非推奨</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Where-Are-You" title="wikilink">Where-Are-You</a> (originally meant for <a href="https://ja.wikipedia.org/wiki/IPv6" title="wikilink">IPv6</a>)</p></td>
</tr>
<tr class="even">
<td><p>34</p></td>
<td></td>
<td><p>非推奨</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Where-Are-You" title="wikilink">Here-I-Am</a> (originally meant for IPv6)</p></td>
</tr>
<tr class="odd">
<td><p>35</p></td>
<td></td>
<td><p>非推奨</p></td>
<td><p>Mobile Registration Request</p></td>
</tr>
<tr class="even">
<td><p>36</p></td>
<td></td>
<td><p>非推奨</p></td>
<td><p>Mobile Registration Reply</p></td>
</tr>
<tr class="odd">
<td><p>37</p></td>
<td></td>
<td><p>非推奨</p></td>
<td><p>Domain Name Request</p></td>
</tr>
<tr class="even">
<td><p>38</p></td>
<td></td>
<td><p>非推奨</p></td>
<td><p>Domain Name Reply</p></td>
</tr>
<tr class="odd">
<td><p>39</p></td>
<td></td>
<td><p>非推奨</p></td>
<td><p>SKIP Algorithm Discovery Protocol, <a href="https://ja.wikipedia.org/wiki/Simple_Key-Management_for_Internet_Protocol" title="wikilink">Simple Key-Management for Internet Protocol</a></p></td>
</tr>
<tr class="even">
<td><p>40</p></td>
<td></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Photuris_(protocol)" title="wikilink">Photuris</a>, Security failures</p></td>
</tr>
<tr class="odd">
<td><p>41</p></td>
<td></td>
<td><p>実験的</p></td>
<td><p>ICMP for experimental mobility protocols such as <a href="https://ja.wikipedia.org/wiki/Seamoby" title="wikilink">Seamoby</a> [RFC4065]</p></td>
</tr>
<tr class="even">
<td><p>42 から 252</p></td>
<td></td>
<td><p>未割当</p></td>
<td><p><em>予約済み</em></p></td>
</tr>
<tr class="odd">
<td><p>253</p></td>
<td></td>
<td><p>未割当</p></td>
<td><p>RFC3692-style Experiment 1 (RFC 4727)</p></td>
</tr>
<tr class="even">
<td><p>254</p></td>
<td></td>
<td><p>未割当l</p></td>
<td><p>RFC3692-style Experiment 2 (RFC 4727)</p></td>
</tr>
<tr class="odd">
<td><p>255</p></td>
<td></td>
<td><p>予約済み</p></td>
<td><p>予約済み</p></td>
</tr>
</tbody>
</table>

### Echo Message（エコー要求通知）・Echo Reply Message（エコー応答通知）

<table>
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
<td><p>タイプ（0または8）</p></td>
<td><p>コード (0)</p></td>
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
<td><p>識別子</p></td>
<td><p>シーケンス番号</p></td>
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
<td><p>データ（可変長）<br />
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

エコー要求はタイプ=8で送信される。現在のところ定義されているコードは0だけである。識別子は送信元で適当な値を決める。要求したプロセスのプロセスIDなどが使われる。シーケンス番号は、同じ識別子で繰り返しエコー要求を送信した場合の通し番号である。

宛先となっているホストがエコー要求を受け取ると、発信元と宛先のアドレスを入れ替え、タイプを0（エコー応答）に書き換え、チェックサムを再計算する。識別子とシーケンス番号はエコー要求で指定された値をそのまま返し、どの要求に対応する応答なのかを発信元で判別する際に使う。また、データフィールドも要求の内容をそのまま返す。

ネットワーク診断用コマンド[ping](https://ja.wikipedia.org/wiki/ping "wikilink")は、このEcho / Echo Replyメッセージを使っている。

### Destination Unreachable Message（宛先到達不可能通知）

<table>
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
<td><p>タイプ (3)</p></td>
<td><p>コード</p></td>
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
<td><p>未使用</p></td>
<td><p>長さ</p></td>
<td><p>次Hopの<a href="../Page/Maximum_Transmission_Unit.md" title="wikilink">MTU</a></p></td>
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
<td><p>IPヘッダ + 元データのデータグラムの先頭部分<br />
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

コードは状況に応じて以下の値をとる。

  - 0 - ネットワーク到達不能
  - 1 - ホスト到達不能
  - 2 - プロトコル到達不能
  - 3 - ポート到達不能
  - 4 - 断片化が必要だがDFフラグが設定されている
  - 5 - 送信元ルーティング失敗

RFC 1122において、以下のコードが追加されている。

  - 6 - 宛先ネットワーク不明
  - 7 - 宛先ホスト不明
  - 8 - 発信元ホストが孤立している
  - 9 - 宛先ネットワークとの通信が管理上禁止
  - 10 - 宛先ホストとの通信が管理上禁止
  - 11 - [Type of Serviceに対してネットワーク到達不能](https://ja.wikipedia.org/wiki/Type_of_Service "wikilink")
  - 12 - Type of Serviceに対してホスト到達不能

さらにRFC 1812では、以下のコードが追加されている。

  - 13 - 通信が管理上禁止
  - 14 - ホスト優先度違反
  - 15 - 優先度が低すぎる

コード9および10は特殊な用途のために定義されており、通常のルーターは13を発生させるよう求めている。

次Hopの[MTUはRFC](../Page/Maximum_Transmission_Unit.md "wikilink") 1191で導入された。コード=4のときに設定され、[経路MTU探索](https://ja.wikipedia.org/wiki/経路MTU探索 "wikilink")のために使われる。タイプ=3、コード=4のICMPパケットを[ファイアウォール](../Page/ファイアウォール.md "wikilink")等でフィルタしてしまうと、経路MTU探索ブラックホールと呼ばれる問題が発生する。

### Source Quench Message（送出抑制要求通知）

<table>
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
<td><p>タイプ (4)</p></td>
<td><p>コード (0)</p></td>
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
<td><p>未使用</p></td>
<td><p>長さ</p></td>
<td><p>未使用</p></td>
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
<td><p>IPヘッダ + 元データのデータグラムの先頭部分<br />
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

受信能力を超えた早さでデータグラムが届き、破棄してしまったことを通知する。ゲートウェイおよび宛先ホストのどちらでも発生する可能性がある。

### Redirect Message（経路変更要求通知）

<table>
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
<td><p>タイプ (5)</p></td>
<td><p>コード</p></td>
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
<td><p>ゲートウェイのIPアドレス</p></td>
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
<td><p>IPヘッダ + 元データのデータグラムの先頭部分<br />
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

ゲートウェイから送信元に対して、今後は他のゲートウェイを使うよう指示する。元のデータグラムも破棄せずに転送する。経路変更要求ICMPメッセージを受け取ったホストはルーティングテーブルに追記し、該当する次のデータグラムからは指示されたゲートウェイへ送るようになる。

コードは以下の値をとる。

  - 0 - ネットワークに関する経路変更要求
  - 1 - ホストに関する経路変更要求
  - 2 - Type of Serviceとネットワークに関する経路変更要求
  - 3 - Type of Serviceとホストに関する経路変更要求

### Router Advertisement Message（ルーター広告通知）

<table>
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
<td><p>タイプ (9)</p></td>
<td><p>コード (0)</p></td>
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
<td><p>ルーターアドレス数</p></td>
<td><p>1エントリあたりの長さ</p></td>
<td><p>有効期限</p></td>
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
<td><p>ルーターアドレスその1</p></td>
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
<td><p>優先度その1</p></td>
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
<td><p>ルーターアドレスその2</p></td>
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
<td><p>優先度その2</p></td>
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
<td><p>…<br />
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

Router Advertisement Messageおよび次のRouter Solicitation Messageは、RFC 1256で追加された。

デフォルトゲートウェイのアドレスを通知する。ルーターアドレス数で指定した数だけ列挙することができ、優先度（[2の補数](../Page/2の補数.md "wikilink")表現による符号付き32ビット整数）が大きいものほど優先度が高い。1アドレスあたりの長さは32ビット単位で指定し、このバージョンの形式では2（すなわち1エントリあたり64ビット）となる。有効期限は応答時点からの秒単位で指定する。

### Router Solicitation Message（ルーター要請通知）

| 0        | 1       | 2      | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 | 27 | 28 | 29 | 30 | 31 |
| -------- | ------- | ------ | - | - | - | - | - | - | - | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| タイプ (10) | コード (0) | チェックサム |   |   |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| 未使用      |         |        |   |   |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |

### Time Exceeded Message（時間切れ通知）

<table>
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
<td><p>タイプ (11)</p></td>
<td><p>コード</p></td>
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
<td><p>未使用</p></td>
<td><p>長さ</p></td>
<td><p>未使用</p></td>
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
<td><p>IPヘッダ + 元データのデータグラムの先頭部分<br />
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

コード0は、IPヘッダの[Time to live](../Page/Time_to_live.md "wikilink")（TTL；存在回数）が0になっても宛先ホストに到達しなかったことを通知する。コード1は、断片の再統合を行う際、制限時間内に断片が揃わなかったことを通知する。

ネットワーク診断用コマンド[traceroute](https://ja.wikipedia.org/wiki/traceroute "wikilink")は、TTLを1から順に増やして行き、各中継点からの時間切れ通知から経路を調べる。

### Parameter Problem Message（不正引数通知）

<table>
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
<td><p>タイプ (12)</p></td>
<td><p>コード (0)</p></td>
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
<td><p>ポインタ</p></td>
<td><p>長さ</p></td>
<td><p>未使用</p></td>
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
<td><p>IPヘッダ + 元データのデータグラムの先頭部分<br />
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

パラメータに問題があって、元のデータグラムを破棄したことを通知する。ポインタは元データのうち問題となった箇所を、先頭からのオクテット数で指定する。

### Timestamp Message（タイムスタンプ要求通知）・Timestamp Reply Message（タイムスタンプ応答通知）

| 0            | 1       | 2      | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 | 27 | 28 | 29 | 30 | 31 |
| ------------ | ------- | ------ | - | - | - | - | - | - | - | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| タイプ（13または14） | コード (0) | チェックサム |   |   |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| 識別子          | シーケンス番号 |        |   |   |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| 起点タイムスタンプ    |         |        |   |   |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| 受信タイムスタンプ    |         |        |   |   |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| 送信タイムスタンプ    |         |        |   |   |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |

タイムスタンプ要求はタイプ=13で送信される。現在のところ定義されているコードは0だけである。識別子およびシーケンス番号はエコー要求と同じ要領で使う。起点タイムスタンプには要求時のタイムスタンプを、[UTC](../Page/協定世界時.md "wikilink") 0:00からの経過ミリ秒で設定する。日付は含まれておらず、毎日0に戻ることに注意。

宛先となったホストはタイムスタンプ要求を受け取ると、タイプ=14で応答する。識別子、シーケンス番号、起点タイムスタンプは、要求にセットされていた値をそのままコピーする。また要求を受信した際のタイムスタンプを受信タイムスタンプに、応答を送信する際のタイムスタンプを送信タイムスタンプにセットする。

要求を送信したホストは、応答を受信した際のタイムスタンプと、格納されている起点タイムスタンプを比較することで、往復に要した時間を知ることができる。

### Information Request Message（情報要求通知）・Information Reply Message（情報応答通知）

| 0            | 1       | 2      | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 | 27 | 28 | 29 | 30 | 31 |
| ------------ | ------- | ------ | - | - | - | - | - | - | - | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| タイプ（15または16） | コード (0) | チェックサム |   |   |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| 識別子          | シーケンス番号 |        |   |   |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |

タイプ=15の情報要求通知はアドレス0に対して送られる。要求を受信した各ホストおよびゲートウェイは、タイプ=16の情報応答通知を返す。

### Address Mask Request Message（アドレスマスク要求通知）・Address Mask Reply Message（アドレスマスク応答通知）

| 0            | 1       | 2      | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 | 27 | 28 | 29 | 30 | 31 |
| ------------ | ------- | ------ | - | - | - | - | - | - | - | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| タイプ（17または18） | コード (0) | チェックサム |   |   |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| 識別子          | シーケンス番号 |        |   |   |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| アドレスマスク      |         |        |   |   |   |   |   |   |   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |

Address Mask Request MessageおよびAddress Mask Reply Messageは、RFC 950で追加された。

## 脚注

## 参考文献

  -
## 関連項目

  - [Internet Control Message Protocol for IPv6](../Page/Internet_Control_Message_Protocol_for_IPv6.md "wikilink")

## 外部リンク

  - RFC 792 - Internet Control Message Protocol
  - RFC 950 - Internet Standard Subnetting Procedure
  - RFC 1122 - Requirements for Internet Hosts -- Communication Layers
  - RFC 1191 - Path MTU Discovery
  - RFC 1256 - ICMP Router Discovery Messages
  - RFC 1812 - Requirements for IP Version 4 Routers
  - RFC 4884 - Extended ICMP to Support Multi-Part Messages

[Category:インターネット層プロトコル](https://ja.wikipedia.org/wiki/Category:インターネット層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:ネットワーク層プロトコル](https://ja.wikipedia.org/wiki/Category:ネットワーク層プロトコル "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.  [traceroute](https://ja.wikipedia.org/wiki/traceroute "wikilink")は、ICMPではなく[UDPを使った実装もある](../Page/User_Datagram_Protocol.md "wikilink")。
2.
3.  *Computer Networking - A Top-Down Approach* by Kurose and Ross