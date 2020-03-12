> この記事は[Internet Control Message Protocol for IPv6](https://ja.wikipedia.org/wiki/Internet_Control_Message_Protocol_for_IPv6)から翻訳されています。


**Internet Control Message Protocol for IPv6**（**ICMPv6**）は[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")で用いられる[ICMP](https://ja.wikipedia.org/wiki/ICMP "wikilink")プロトコルである。

## 概要

IPv6ではICMPv6の枠組みを利用して、アドレス解決やアドレス重複検出などにも利用し、type番号もICMP(IPv4)のものとは違う番号が定義し直されているので、[IPv4](../Page/IPv4.md "wikilink")のICMPとは異なる新しいプロトコルとして定義されている。[プロトコル番号](https://ja.wikipedia.org/wiki/プロトコル番号 "wikilink")は58。RFC 4443 によって規定されている。

## パケットフォーマット

パケットフォーマット自体はICMPと同一。

| Bit offset | 0–7          | 8–15 | 16–31    |
| ---------- | ------------ | ---- | -------- |
| **0**      | Type         | Code | Checksum |
| **32**     | Message body |      |          |
|            |              |      |          |

ICMPv6 [パケット](../Page/パケット.md "wikilink")

各type毎にoptionが定義されることがある。

## TypeとCode

typeはエラー通知は127以下、そうでないものは128以上の値が定義される。

<table>
<thead>
<tr class="header">
<th style="text-align: center;"><p>Type</p></th>
<th style="text-align: center;"><p>Code</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: center;"><p>値</p></td>
<td style="text-align: center;"><p>意味</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>ICMPv6エラーメッセージ</p></td>
<td style="text-align: center;"></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>1</p></td>
<td style="text-align: center;"><p>Destination Unreachable<br />
（宛先不達）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>1</p></td>
<td style="text-align: center;"><p>communication with destination administratively prohibited</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>2</p></td>
<td style="text-align: center;"><p>beyond scope of source address</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>3</p></td>
<td style="text-align: center;"><p>address unreachable</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>4</p></td>
<td style="text-align: center;"><p>port unreachable</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>5</p></td>
<td style="text-align: center;"><p>source address failed ingress/egress policy</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>6</p></td>
<td style="text-align: center;"><p>reject route to destination</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>7</p></td>
<td style="text-align: center;"><p>Error in Source Routing Header</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>2</p></td>
<td style="text-align: center;"><p>Packet too Big<br />
（<a href="https://ja.wikipedia.org/wiki/IPフラグメンテーション" title="wikilink">パケット過大</a>）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>3</p></td>
<td style="text-align: center;"><p>Time Exceeded<br />
（<a href="../Page/Time_to_live.md" title="wikilink">時間切れ</a>）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>1</p></td>
<td style="text-align: center;"><p>fragment reassembly time exceeded</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>4</p></td>
<td style="text-align: center;"><p>Parameter Problem<br />
（パラメータ異常）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>1</p></td>
<td style="text-align: center;"><p>unrecognized Next Header type encountered</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>2</p></td>
<td style="text-align: center;"><p>unrecognized IPv6 option encountered</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>100</p></td>
<td style="text-align: center;"><p>Private experimentation<br />
（プライベートな実験）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>101</p></td>
<td style="text-align: center;"><p>Private experimentation<br />
（プライベートな実験）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>127</p></td>
<td style="text-align: center;"><p>Reserved for expansion of ICMPv6 error messages<br />
（ICMPv6エラーメッセージ拡張用の予約）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>ICMPv6情報メッセージ</p></td>
<td style="text-align: center;"></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>128</p></td>
<td style="text-align: center;"><p>Echo Request<br />
（<a href="../Page/Ping.md" title="wikilink">エコー要求</a>）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>129</p></td>
<td style="text-align: center;"><p>Echo Reply<br />
（<a href="../Page/Ping.md" title="wikilink">エコー応答</a>）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>130</p></td>
<td style="text-align: center;"><p>Multicast Listener Query<br />
（マルチキャストリスナクエリー）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>131</p></td>
<td style="text-align: center;"><p>Multicast Listener Report<br />
（マルチキャストリスナレポート）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>132</p></td>
<td style="text-align: center;"><p>Multicast Listener Done<br />
（マルチキャストリスナダン）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>133</p></td>
<td style="text-align: center;"><p>router solicitation (<a href="https://ja.wikipedia.org/wiki/Neighbor_Discovery_Protocol" title="wikilink">NDP</a>)<br />
（ルータ要請）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>134</p></td>
<td style="text-align: center;"><p>router advertisement (NDP)<br />
（ルータ広告）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>135</p></td>
<td style="text-align: center;"><p>Neighbor solicitation (NDP)<br />
（近隣要請）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>136</p></td>
<td style="text-align: center;"><p>Neighbor advertisement (NDP)<br />
（近隣広告）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>137</p></td>
<td style="text-align: center;"><p>redirect (NDP)<br />
（リダイレクト）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>138</p></td>
<td style="text-align: center;"><p>Router Renumber<br />
（ルータリナンバ）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>1</p></td>
<td style="text-align: center;"><p>Router Renumbering Result</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>255</p></td>
<td style="text-align: center;"><p>Sequence Number Reset</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>139</p></td>
<td style="text-align: center;"><p>ICMP Node Information Query<br />
（ICMPノード情報問い合わせ）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>1</p></td>
<td style="text-align: center;"><p>The Data field contains a name which is the Subject of this Query, or is empty, as in the case of a NOOP.</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>2</p></td>
<td style="text-align: center;"><p>The Data field contains an IPv4 address which is the Subject of this Query.</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>140</p></td>
<td style="text-align: center;"><p>ICMP Node Information Reply<br />
（ICMPノード情報応答）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>1</p></td>
<td style="text-align: center;"><p>The Responder refuses to supply the answer. The Reply Data field will be empty.</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>2</p></td>
<td style="text-align: center;"><p>The Qtype of the Query is unknown to the Responder. The Reply Data field will be empty.</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>141</p></td>
<td style="text-align: center;"><p>Inverse Neighbor Discovery Solicitation Message<br />
（逆近隣探索要請）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>142</p></td>
<td style="text-align: center;"><p>Inverse Neighbor Discovery Advertisement Message<br />
（逆近隣探索広告）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>143</p></td>
<td style="text-align: center;"><p>MLDv2 Multicast Listener Report (RFC 3810)<br />
（<a href="https://ja.wikipedia.org/wiki/Multicast_Listener_Discovery" title="wikilink">MLDv2マルチキャストリスナレポート</a>）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>144</p></td>
<td style="text-align: center;"><p>Home Agent Address Discovery Request Message<br />
（ホームエージェントアドレス発見要求）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>145</p></td>
<td style="text-align: center;"><p>Home Agent Address Discovery Reply Message<br />
（ホームエージェントアドレス発見応答）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>146</p></td>
<td style="text-align: center;"><p>Mobile Prefix Solicitation<br />
（モバイルプリフィックス要請）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>147</p></td>
<td style="text-align: center;"><p>Mobile Prefix Advertisement<br />
（モバイルプリフィックス広告）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>148</p></td>
<td style="text-align: center;"><p>Certification Path Solicitation (<a href="https://ja.wikipedia.org/wiki/Secure_Neighbor_Discovery_Protocol" title="wikilink">SEND</a>)<br />
（証明書パス要請）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>149</p></td>
<td style="text-align: center;"><p>Certification Path Advertisement (SEND)<br />
（証明書パス広告）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>151</p></td>
<td style="text-align: center;"><p>Multicast Router Advertisement (<a href="https://ja.wikipedia.org/wiki/Multicast_router_discovery" title="wikilink">MRD</a>)<br />
（マルチキャストルータ広告）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>152</p></td>
<td style="text-align: center;"><p>Multicast Router Solicitation (MRD)<br />
（マルチキャストルータ要請）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>153</p></td>
<td style="text-align: center;"><p>Multicast Router Termination (MRD)<br />
（マルチキャストルータ終了）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>155</p></td>
<td style="text-align: center;"><p>RPL Control Message<br />
（RPL制御メッセージ）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>200</p></td>
<td style="text-align: center;"><p>Private experimentation<br />
（プライベートな実験）</p></td>
</tr>
<tr class="even">
<td style="text-align: center;"><p>201</p></td>
<td style="text-align: center;"><p>Private experimentation<br />
（プライベートな実験）</p></td>
</tr>
<tr class="odd">
<td style="text-align: center;"><p>255</p></td>
<td style="text-align: center;"><p>Reserved for expansion of ICMPv6 informational messages<br />
（ICMPv6情報メッセージ拡張用の予約）</p></td>
</tr>
</tbody>
</table>

上記は全てのtypeを網羅したものではない。完全なリストは[IANA: ICMPv6 Parameters](http://www.iana.org/assignments/icmpv6-parameters)を参照のこと。

## エラー通知

ICMPと同様にパケット配送中に発生したエラーを通知する。

## 近隣探索 (Neighbor discovery)

[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink") では [IPアドレス](../Page/IPアドレス.md "wikilink")から [MACアドレス](../Page/MACアドレス.md "wikilink")を取得するために、IPv4 の [ARP](../Page/Address_Resolution_Protocol.md "wikilink") のような別のプロトコルを定義するのではなく、ICMPv6 の枠組み（NDP、Neighbor Discovery）を用いてアドレス解決を行う。アドレス解決をしたい[ノードは](https://ja.wikipedia.org/wiki/ノード_\(ネットワーク\) "wikilink")[ペイロードに解決したいIPアドレスを格納して](https://ja.wikipedia.org/wiki/ペイロード_\(コンピュータ\) "wikilink")、全ノード宛[マルチキャスト](../Page/マルチキャスト.md "wikilink")アドレスに IPv4 の ARP request に相当する Neighbor Solicitation (NS) パケットを送信し、それに答えるべきノードは、Target linklayer address option に自ノードの MAC アドレスを格納した Neighbor Advertisement (NA) を送信してアドレス解決を行う。 RFC 4861 で規定されている。

## Multicast Listener Discovery

MLD。[IPv4](../Page/IPv4.md "wikilink")の[Internet Group Management Protocol](../Page/Internet_Group_Management_Protocol.md "wikilink")（IGMP）に相当する機能。

## ルータ広告

ルータ広告自体は ICMP でも定義されている (RFC 1256) が、IPv6 では DHCP などのようなアドレス割当用サーバがなくても、ノードが自力でアドレスを設定する (ステートレスアドレス自動設定 (RFC 4862)) 手段を提供するために、積極的にこのルータ広告が利用されている。 これも広い意味での Neighbor Discovery であり、RFC 4861 で規定されている。

## 重複アドレス検出

アドレスを手動で設定したり、ステートレスアドレス自動設定でつけた場合は、そのアドレスの一意性を確認できないので、重複アドレス検出 (Duplicate Address Detection; DAD) で、その一意性を確認する。 RFC 4862 Section 5.4 で規定されている

あるノードにアドレスがつけられると、そのアドレスは 'TENTATIVE' という状態になり、アドレスの重複検出を行う。これは target アドレスにその重複検出をするアドレスを入れた、アドレス解決で利用される近隣要請 (Neighbor Solicitation) を送出するものである。 もし、既にそのアドレスを使っているノードがあれば近隣広告 (Neighbor Advertisement; NA) を返すので、アドレスの重複が検出できる。 1 秒以内に NA が返ってこないと、そのアドレスは重複無しと判断され、利用可能アドレスとなる。

## パスMTU探索 (Path MTU Discovery)

IPv6のパケット断片化は配送中のルータではなく、送信元のみで行われるので、送信元は配送される全経路で通過できるパケットのサイズ(パス[MTU](../Page/Maximum_Transmission_Unit.md "wikilink"))を知らなければならない。これを行うのがパスMTU探索である。 RFC 1981で規定されている。

あるノードから送信されるパケットは、そのインタフェースのMTU値などなるべく大きな値のMTU値を用いて送信される。途中のルータで転送先のインタフェースのMTU値がそのパケットより小さければ、そのルータは送信元に「パケット過大(Packet too big)」エラーを返す。このとき送信可能なMTU値も返されるので、送信元はその値でパケットをフラグメントして再び送信する。これを繰り返すことで、送信元は送信先まで到達可能なMTU値(パスMTU)を知ることができ、以降は始めからその値でフラグメントして送信することができるようになる。

## ノード情報問い合わせ

IPv6ノードに対して、直接そのノードのノード名、アドレスなどを問い合わせをするプロトコルである。 RFC 4620 では、ノード名(FQDN)、[IPv6アドレス](https://ja.wikipedia.org/wiki/IPv6アドレス "wikilink")、[IPv4アドレス](https://ja.wikipedia.org/wiki/IPv4アドレス "wikilink")の問い合わせプロトコルについて規定している。

[Category:IPv6](https://ja.wikipedia.org/wiki/Category:IPv6 "wikilink") [Category:インターネット層プロトコル](https://ja.wikipedia.org/wiki/Category:インターネット層プロトコル "wikilink") [Category:ネットワーク層プロトコル](https://ja.wikipedia.org/wiki/Category:ネットワーク層プロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")