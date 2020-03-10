> この記事は[Real-time Transport Protocol](https://ja.wikipedia.org/wiki/Real-time_Transport_Protocol)から翻訳されています。


**Real-time Transport Protocol**（リアルタイム トランスポート プロトコル、**RTP**）は、[音声](https://ja.wikipedia.org/wiki/音声 "wikilink")や[動画](../Page/動画.md "wikilink")などのデータストリームをリアルタイムに配送するためのデータ[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。

## 概要

[RTSPや](../Page/Real_Time_Streaming_Protocol.md "wikilink")[H.323](https://ja.wikipedia.org/wiki/H.323 "wikilink")の[通信プロトコル](../Page/通信プロトコル.md "wikilink")のデータ部分に使用される。 ほぼ全ての[VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink")関連製品は、RTPを利用して、音声情報を[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")上へ送出している。 これは、リアルタイムストリームを運ぶためのプロトコルとして[IETF](../Page/Internet_Engineering_Task_Force.md "wikilink")、[ITUで標準化されている](../Page/国際電気通信連合.md "wikilink")。

RTPは、[UDPの](../Page/User_Datagram_Protocol.md "wikilink")[通信プロトコル](../Page/通信プロトコル.md "wikilink")（[TCPと違ってUDPのヘッダには](../Page/Transmission_Control_Protocol.md "wikilink")「シーケンス（順序）番号」の項目が存在しないため順序の組み立てができない）であるが、 RTP[パケット](../Page/パケット.md "wikilink")を受信した[ホストは](https://ja.wikipedia.org/wiki/ホスト_\(ネットワーク\) "wikilink")、RTPパケットのRTP用のヘッダーにある情報から各[パケット](../Page/パケット.md "wikilink")の時間の情報から時間的な関係を把握し、データを再生することができる。 RTPパケットも他のパケットと同様に、ネットワークを経由して転送されていく中で、喪失や、配送の遅れが起こる。 しかし、映像や音声のデータは、データの一部が欠けていても再生が可能であるため、データの受信側では、喪失や、配送の遅れたパケットは無視し、受信側が期待する時間に到着したパケットだけを利用してデータの再生を行うことができる。

[インターネット・プロトコル・スイート](../Page/インターネット・プロトコル・スイート.md "wikilink")の中でRTPを利用する場合は、RTPは[UDPをトランスポート層のプロトコルとして利用するが](../Page/User_Datagram_Protocol.md "wikilink")、トランスポート層のプロトコルにUDP以外の通信プロトコルを用いることができるようにも設計されている。

## パケットヘッダー

<table>
<caption>RTP packet header</caption>
<thead>
<tr class="header">
<th><p>Bit offset</p></th>
<th><p>0-1</p></th>
<th><p>2</p></th>
<th><p>3</p></th>
<th><p>4-7</p></th>
<th><p>8</p></th>
<th><p>9-15</p></th>
<th><p>16-31</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0</p></td>
<td><p>バージョン</p></td>
<td><p>P</p></td>
<td><p>X</p></td>
<td><p>CC</p></td>
<td><p>M</p></td>
<td><p>PT</p></td>
<td><p>順序番号</p></td>
</tr>
<tr class="even">
<td><p>32</p></td>
<td><p>タイムスタンプ</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>64</p></td>
<td><p>SSRC識別子</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>96</p></td>
<td><p>CSRC識別子<br />
...</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>96+32×CC</p></td>
<td><p>プロファイル固有の拡張ヘッダID</p></td>
<td><p>拡張ヘッダ長</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>128+32×CC</p></td>
<td><p>拡張ヘッダ<br />
...</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

RTPヘッダは、12バイトが最小サイズである。 ヘッダの後ろのオプションの拡張ヘッダは存在してもよい。\[1\]

## 出典・脚注

## 関連項目

  - [RTCP](../Page/Real-time_Transport_Control_Protocol.md "wikilink")
  - [MGCP](https://ja.wikipedia.org/wiki/MGCP "wikilink")
  - [遠隔会議](https://ja.wikipedia.org/wiki/遠隔会議 "wikilink")

## 外部リンク

  - RFC 3550 - A Transport Protocol for Real-Time Applications
  - RFC 3551 - RTP Profile for Audio and Video Conferences with Minimal Control

[Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink")

1.