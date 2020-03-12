> この記事は[Simple Network Time Protocol](https://ja.wikipedia.org/wiki/Simple_Network_Time_Protocol)から翻訳されています。


**Simple Network Time Protocol**（シンプルネットワークタイムプロトコル、**SNTP**と略記）とは、[NTP](../Page/Network_Time_Protocol.md "wikilink")[パケット](../Page/パケット.md "wikilink")を利用した、簡単な[時計](../Page/時計.md "wikilink")補正[プロトコル](../Page/プロトコル.md "wikilink")である。

## 処理概要

SNTPのパケットは、RFC1305を抜粋し、RFC 1361, RFC 1769, RFC 2030 にて再定義される。このパケットを使用し、上位時計[サーバ](../Page/サーバ.md "wikilink")との通信にて、[オフセット](https://ja.wikipedia.org/wiki/オフセット "wikilink")を演算する。なお、時計反映処理はNTPも同様で定義されていないためプログラマーに依存する。その理由は、時計校正にはそのまま反映してよいものと、徐々に時計を近づける方法があり、運用されるシステムによって選択する必要があるためである。

## 時計精度と上限

### 時計精度

SNTPおよびNTPも同じパケット使用しているため、処理上はNTPタイムスタンプ形式の精度が内部精度となる（例：NTPタイムスタンプ形式）。

| オフセット | データサイズ     | 項目                          |
| ----- | ---------- | --------------------------- |
| 0     | 符号無し4バイト整数 | Seconds                     |
| \+4   | 符号無し4バイト整数 | Seconds Fraction (0-padded) |

上記より使用できる時計精度は200ピコ秒まで処理可能。

### 2036年問題

このパケットは[協定世界時](../Page/協定世界時.md "wikilink")(UTC)の[1900年](../Page/1900年.md "wikilink")[1月1日](../Page/1月1日.md "wikilink")0時からの経過秒数で送られている。データサイズは符号無し4バイト整数であるため最大経過秒数は4294967295秒までとなり、協定世界時の2036年2月7日午前6時28分16秒(日本時間では同日午後3時28分16秒)までとなる。そのため、[オーバーフローが発生するより前に継続を行うための何らかの対処が必要となる](https://ja.wikipedia.org/wiki/算術オーバーフロー "wikilink")。

RFC 4330には、最上位ビットが0の場合は時刻が2036年から[2104年](https://ja.wikipedia.org/wiki/2104年 "wikilink")の間であるとみなして、2036年2月7日6時28分16秒(UTC)を起点として計算することで2036年問題を回避する方法が記述されている\[1\]。

## 時計サーバとの伝送モードと同期について

### 伝送モード

SNTPおよびNTPを使用するには伝送モードの種類がある。NTPパケットには「Mode」と言われる3ビットのフィールドがある。多くのSNTPソフトは、サーバ・クライアントモードを使用して同期処理を行う。

<table>
<thead>
<tr class="header">
<th><p>mode値</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1,2</p></td>
<td><p>本来は時計サーバ同士の同期に使用。UNIX系OSのNTPサーバではpeer設定にて動作するモードである。</p></td>
</tr>
<tr class="even">
<td><p>3,4</p></td>
<td><p>時計サーバと時計クライアントの組合せで同期に使用。 UNIX系OSのNTPサーバではServer設定にて動作するモードである。 SNTPに使用するNTPDATEコマンドで使用される。 多くのSNTPクライアントではこの仕様が採用されている。</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>放送モードで<a href="../Page/ブロードキャスト.md" title="wikilink">ブロードキャスト</a>または<a href="../Page/マルチキャスト.md" title="wikilink">マルチキャスト</a>による同期方式である。 このモードは時計サーバより一方的にNTPパケット送信する。SNTPクライアント、NTPクライアントはこれを受信し、かつ推定遅延値を加算して時計を反映する。マルチキャストで使用可能なように<a href="../Page/IPv4.md" title="wikilink">IPv4</a>はRFC-1700、<a href="https://ja.wikipedia.org/wiki/IPv6" title="wikilink">IPv6</a>はRFC-2375にマルチキャストアドレスが割り当てられている。</p>
<ul>
<li>IPv4 : 224.0.1.1</li>
<li>IPv6 : FF0X:0:0:0:0:0:0:101</li>
</ul></td>
</tr>
<tr class="even">
<td><p>6,7</p></td>
<td><p>NTPの状態の参照、設定等に使用する伝送モードである。ntpq、ntpdcコマンドで使用する。RFC-1305のオプション機能として記述されるが、SNTPはこの機能を実装する必要はない。</p></td>
</tr>
</tbody>
</table>

NTPは基本的にすべてのモードをサポートする必要があるが、SNTPは規定がないため、どれを利用してもよく、どれか1つサポートすれば基本的にSNTPといえる。

### 同期

SNTPは1回の通信で時計反映処理に移行できる。一般的なソフトはstratum値が正常であること、閏秒指示子（Leap Indicator値）が正常であれば時計を信用する。ただし、時計校正条件はRFCに記述はない。

#### 関連RFC

  - RFC 1361 SNTP
  - RFC 1769 SNTP
  - RFC 2030 SNTP Version 4 for IPv4, IPv6 and OSI
  - RFC 4330 SNTP Version 4 for IPv4, IPv6 and OSI

## 脚注

## 関連項目

  - [Network Time Protocol](../Page/Network_Time_Protocol.md "wikilink")

[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:時間に関するネットワークソフト](https://ja.wikipedia.org/wiki/Category:時間に関するネットワークソフト "wikilink")

1.  RFC 4330