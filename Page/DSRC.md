> この記事は[DSRC](https://ja.wikipedia.org/wiki/DSRC)から翻訳されています。


**DSRC**（）とは、車両との無線通信に特化して設計された5.8GHz帯の[ISMバンド](../Page/ISMバンド.md "wikilink")を用いた一方向、または双方向の無線通信技術。**専用狭域通信**あるいは**狭域通信**と呼ばれる。

## 概要

DSRCの特徴として、[アンテナ](../Page/アンテナ.md "wikilink")の[指向性](../Page/指向性.md "wikilink")と高精度なキャリアセンスにより、通信エリアを意図的に狭くコントロールしている。[高度道路交通システム](../Page/高度道路交通システム.md "wikilink")（）で利用されており、路側機と車載器の間の通信でドライバーへ様々なサービスが提供されている。

DSRCの通信プロトコルは7層のOSI(Open System Interconnection、開放型システム間相互接続)の中で高速走行時での通信を考慮して第3-6層が存在せず、[物理層](https://ja.wikipedia.org/wiki/物理層 "wikilink")・[データリンク層](https://ja.wikipedia.org/wiki/データリンク層 "wikilink")・[応用層](https://ja.wikipedia.org/wiki/応用層 "wikilink")の3層から構成されている\[1\]。 日本においては、[ARIB](https://ja.wikipedia.org/wiki/ARIB "wikilink") STD-T75「狭域通信（DSRC）システム標準規格」により、相互接続性が確保されている。また、基地局設置のガイドラインとしてRC-003が策定されている。変調方式として[ASK方式とπ](https://ja.wikipedia.org/wiki/振幅偏移変調 "wikilink")/4シフト[QPSK](https://ja.wikipedia.org/wiki/QPSK "wikilink")方式の2種類があり、ASK方式では1Mbps、π/4シフトQPSK方式では4Mbpsの通信速度を実現している\[2\]。

ARIB STD-T75で規定されているDSRCは、固定長フレームから構成される[時分割多元接続](https://ja.wikipedia.org/wiki/時分割多元接続 "wikilink") (TDMA)方式が採用され、一つの狭い通信領域においても、複数の車両が存在することを想定して確実で効率的な通信を行うために一定間隔でタイムスロットを設けて送信タイミングを制御する[スロッテドアロハ方式を採用する](https://ja.wikipedia.org/wiki/ALOHA#Slotted_ALOHA "wikilink")\[3\]。さらに[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")などの通信環境に接続したり、アプリケーションをより使いやすくしたりするための仕様としてASL（Applica-tion Sub-Layer）とDSRC基本アプリケーションインタフェースがあり、ASLはARIB STD-T88として規格化されている\[4\]。

ASK方式を使用したシステムとしては[ETC](../Page/ETC.md "wikilink")がある。π/4シフトQPSK方式では、[VICS](https://ja.wikipedia.org/wiki/VICS "wikilink")などのETC2.0（旧：ITSスポットサービス）に使用されているほか、ガソリンスタンドや駐車場などでのキャッシュレス決済、インターネット接続、物流管理などへの利用も期待されており、実用化や本格運用に向けた検討が進められている。

<table>
<caption>DSRCの電波規格[5]</caption>
<thead>
<tr class="header">
<th><p>項 目</p></th>
<th><p>規 格</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>周波数帯</p></td>
<td><p>5.8GHz帯、14ch （チャネル）</p></td>
</tr>
<tr class="even">
<td><p>通信方式</p></td>
<td><p>アクティブ方式</p></td>
</tr>
<tr class="odd">
<td><p>変調方式</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ASK" title="wikilink">ASK</a>、<a href="https://ja.wikipedia.org/wiki/QPSK" title="wikilink">QPSK</a></p></td>
</tr>
<tr class="even">
<td><p>変調信号速度</p></td>
<td><p>1Mbps（ASK）、4Mbps（QPSK） 占有周波数帯域 4.4MHz以下/ch</p></td>
</tr>
<tr class="odd">
<td><p>周波数間隔</p></td>
<td><p>5MHz</p></td>
</tr>
<tr class="even">
<td><p>送信出力</p></td>
<td><p>路側機；300mW以下（伝送距離30m以上）<br />
10mW以下（伝送距離30m以下）<br />
車載器；10mW以下</p></td>
</tr>
</tbody>
</table>

<table>
<caption>日米欧のDSRC規格[6]</caption>
<thead>
<tr class="header">
<th><p>　</p></th>
<th><p>日本</p></th>
<th><p>欧州</p></th>
<th><p>アメリカ</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>規格名</p></td>
<td><p>ARIB STD-T75</p></td>
<td><p>CEN EN12253等</p></td>
<td><p>IEEE 802.11p</p></td>
</tr>
<tr class="even">
<td><p>周波数帯</p></td>
<td><p>5.8GHz</p></td>
<td><p>5.9GHz</p></td>
<td><p>5.9GHz</p></td>
</tr>
<tr class="odd">
<td><p>通信速度</p></td>
<td><p>アクティブ</p></td>
<td><p>パッシブ</p></td>
<td><p>アクティブ</p></td>
</tr>
<tr class="even">
<td><p>伝送速度</p></td>
<td><p>1 or 4Mbps</p></td>
<td><p>下り；0.5Mbps<br />
上り；0.25Mbps</p></td>
<td><p>3-27Mbps</p></td>
</tr>
<tr class="odd">
<td><p>通信同時性</p></td>
<td><p>路側；全二重 or 半二重<br />
車載；半二重</p></td>
<td><p>半二重</p></td>
<td><p>半二重</p></td>
</tr>
</tbody>
</table>

## ETC2.0

このサービスを利用して、ETC2.0渋滞情報サービスが提供されている。主に[高速道路](../Page/高速道路.md "wikilink")で使用可能。

## 日本における周波数

路側機送信：5775, 5780, 5785, 5790, 5795, 5800, 5805 MHz　占有周波数帯幅：4.4MHz

車載器送信：5815, 5820, 5825, 5830, 5835, 5840, 5845 MHz　占有周波数帯幅：4.4MHz

## 脚注

## 関連項目

  - [ETC](../Page/ETC.md "wikilink")

## 外部リンク

  - [ITS-TEA｜(一財)ITSサービス高度化機構](https://www.its-tea.or.jp/)

[Category:通信](https://ja.wikipedia.org/wiki/Category:通信 "wikilink") [Category:通信工学](https://ja.wikipedia.org/wiki/Category:通信工学 "wikilink")

1.
2.
3.
4.
5.
6.