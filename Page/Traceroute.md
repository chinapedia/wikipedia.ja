> この記事は[Traceroute](https://ja.wikipedia.org/wiki/Traceroute)から翻訳されています。


**traceroute**（トレース ルート）は[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")において、[ノードまでの経路情報を取得するツールである](https://ja.wikipedia.org/wiki/ノード_\(ネットワーク\) "wikilink")。 [インターネット](../Page/インターネット.md "wikilink")上で、2つのノード([パソコンや](../Page/パーソナルコンピュータ.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")など)が通信する場合、2つのノードの間には0個以上の[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")が存在する。 **traceroute**を利用することで、**traceroute**を実行したノードから指定したノードに到達するまでに、経由するルータのリストが得られる。

[Windowsの](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")**tracert**も同様のツールである。

## 原理

tracerouteは[TTLを](https://ja.wikipedia.org/wiki/Time_to_live "wikilink")1ずつ増やしながら[パケット](../Page/パケット.md "wikilink")を送信することで、経路情報を取得する。 TTLとはパケットの生存期間を表し、ルータを1つ経由することに1ずつ減算される。 ルータはTTLが2以上のパケットが届いた場合、TTLの値を1だけ小さくし次のルータへ転送する。 TTLが1のパケットが届いた場合、届いたパケットを破棄し[ICMP](../Page/Internet_Control_Message_Protocol.md "wikilink") time exceededパケットを送信者に返す。

tracerouteはまず、TTLを1にセットしたパケットを送信する。最初のルータに届いた時点でTTLがゼロになり、ICMP time exceededメッセージが戻ってくる。このメッセージの送信元アドレスを見れば、最初のルータの[IPアドレス](../Page/IPアドレス.md "wikilink")がわかる。次にTTLを2にセットして送信すると、今度は2番目のルータからICMP time exceededが戻ってくる。以降、TTLを3、4･･･と増やしていく事で、順にルータのIPアドレスを得る事ができる。

実際には、以上の作業を3回繰り返して行い、応答までの時間を表示する。 経由しているルータが応答せずタイムアウトが発生した場合は、\*マークを表示する。 tracerouteで得られる経路情報は往路のみである。反対側からの経路も同じとは限らない。

tracerouteが送信するパケットは原理上は何でも構わないが、一般的な**traceroute**の実装ではランダムなポート番号の[UDPデータグラムが使用される](../Page/User_Datagram_Protocol.md "wikilink")。Windowsの**tracert**では[ping](https://ja.wikipedia.org/wiki/ping "wikilink")と同じICMP Echo requestパケットを使用している。また、オプションスイッチによって使用するパケットを切り替えられる実装もある。

UDPを使用するtracerouteは、ポート番号が定まらないため[パケットフィルタリングを行っているネットワークでは利用が難しい面があり](../Page/ファイアウォール.md "wikilink")、特に[ファイアウォール](../Page/ファイアウォール.md "wikilink")がある場合は問題になりやすい。 また、最終的な宛先ノードにパケットが到達した際、ICMP Echo requestの場合は単にICMP Echo replyが返されるだけだが、UDPの場合は、たまたまそのポート番号が使われていた等で、期待した動作にならない事がある。

他方、ICMPを使用した実装は、ICMP Echo requestメッセージのTTL切れに対してICMP time exceededが発生する事を前提としている。[RFC](../Page/Request_for_Comments.md "wikilink")1812ではICMPがクエリとエラーに分けられ、クエリに対するエラーの送信は禁止されてはいないが、RFC792では単に「ICMPメッセージについてのICMPは送信しない」とされており、この記述には合致していない。現代ではほとんどの機器で動作するが、RFC792だけを見て実装された機器では期待通りに動かない可能性もある。

## 実行例

**traceroute**を[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")上で実行した結果を下記に示す。

<div style="background: #f8f8f8; border: 1px solid gray; padding: 0.5em; margin: 1em;">

<tt><poem> $ <u>traceroute ja.wikipedia.org</u> traceroute to ja.wikipedia.org (208.80.152.2), 30 hops max, 60 byte packets

`1  ntt.setup (192.168.1.1)  0.121 ms  0.134 ms  0.159 ms`
`2  118.23.8.17 (118.23.8.17)  6.037 ms  6.577 ms  7.064 ms`
`3  118.23.5.137 (118.23.5.137)  4.971 ms  5.388 ms  5.368 ms`
`4  122.1.164.213 (122.1.164.213)  7.556 ms  9.341 ms  11.167 ms`
`5  60.37.55.165 (60.37.55.165)  6.195 ms  6.151 ms  6.154 ms`
`6  60.37.27.89 (60.37.27.89)  6.470 ms  5.355 ms  5.761 ms`
`7  ae-5.r21.tokyjp01.jp.bb.gin.ntt.net (129.250.11.53)  5.790 ms  7.090 ms  6.670 ms`
`8  as-2.r21.snjsca04.us.bb.gin.ntt.net (129.250.4.44)  114.218 ms  113.157 ms  113.279 ms`
`9  equinixexchange.ir1.sanjose-ca.us.xo.net (206.223.116.85)  122.223 ms  122.167 ms  122.115 ms`

10 vb2001.rar3.la-ca.us.xo.net (207.88.13.110) 125.873 ms 132.449 ms 125.843 ms 11 vb15.rar3.dallas-tx.us.xo.net (207.88.12.45) 149.345 ms 149.826 ms 149.540 ms 12 207.88.14.42.ptr.us.xo.net (207.88.14.42) 182.000 ms 182.215 ms 181.906 ms 13 w006.z207088246.xo.cnc.net (207.88.246.6) 187.915 ms 187.107 ms 187.082 ms 14 rr.pmtpa.wikimedia.org (208.80.152.2) 186.903 ms 186.520 ms 186.758 ms </poem></tt>

</div>

## IPのレコード・ルートとの違い

tracerouteと似た目的のものに、pingプログラムのレコード・ルートオプションがある。これはtracerouteとは原理がまったく異なり、[IPパケットのオプションであるレコード](https://ja.wikipedia.org/wiki/IPv4 "wikilink")・ルート機能を活用したものである。パケットがルータを通過する際に、ルータ自身がパケットに自分のアドレスを書き込んでいく事で実現されている。

レコード・ルートにはいくつか欠点があり、それがtraceroute開発の動機となったといわれる。

  - 記録用のフィールドが小さく、往復で9個のルータしか記録できない。
  - そもそもIPの仕様においてオプションであり、ルータが対応していない事がある。
  - ルータだけでなく、Echo replyを返すホストも対応している必要がある。

tracerouteが広まった現代では、レコード・ルートオプションを持たないping実装も多い。

## 参考文献

  - W・リチャード・スティーヴンス、『詳解TCP/IP Vol.1プロトコル』、ピアソン・エデュケーション、[2000年](../Page/2000年.md "wikilink")、第7、8章
  - RFC792 『Internet Control Message Protocol』
  - RFC1812 『Requirements for IP Version 4 Routers』

## 関連項目

  - [Internet Control Message Protocol](../Page/Internet_Control_Message_Protocol.md "wikilink")
  - [Ping](../Page/Ping.md "wikilink")
  - [バン・ジェイコブソン](https://ja.wikipedia.org/wiki/バン・ジェイコブソン "wikilink")

## 外部リンク

  - [traceroute(1M)](https://docs.oracle.com/cd/E19109-01/tsolaris7/805-8077/6j7jhjsca/index.html) man page（Solaris 10 Reference Manual）
  - [traceroute コマンドによる経路制御情報の表示 Solaris のシステム管理 (IP サービス)](https://docs.oracle.com/cd/E24845_01/html/819-0380/ipv6-admintasks-72.html)
  - [Tracerouteチェック](https://mgt.jp/t/traceroute)

[Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink") [Category:ネットワーク・アナライザ](https://ja.wikipedia.org/wiki/Category:ネットワーク・アナライザ "wikilink") [Category:Windowsのコマンド](https://ja.wikipedia.org/wiki/Category:Windowsのコマンド "wikilink")