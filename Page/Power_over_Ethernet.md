> この記事は[Power over Ethernet](https://ja.wikipedia.org/wiki/Power_over_Ethernet)から翻訳されています。


**Power over Ethernet** (PoE) は、[イーサネット](../Page/イーサネット.md "wikilink")の配線で利用される[ツイストペアケーブル](../Page/ツイストペアケーブル.md "wikilink")を通じてデータと[電力](../Page/電力.md "wikilink")を同時に供給する技術。

## 概要

主に、[Webカメラ](../Page/Webカメラ.md "wikilink")、[スイッチングハブ](../Page/スイッチングハブ.md "wikilink")、[無線LAN](../Page/無線LAN.md "wikilink")[アクセスポイント](../Page/アクセスポイント_\(無線LAN\).md "wikilink")、[IP電話機](https://ja.wikipedia.org/wiki/IP電話機 "wikilink")など、電力供給の困難な場所に設置された機器で利用される。[2003年](../Page/2003年.md "wikilink")6月に**IEEE 802.3af**として標準化され、その後拡張規格として**IEEE 802.3at**-2009（通称PoE+）、**IEEE 802.3bt**-2018（通称PoE++）が標準化されており、いずれも下位互換性を持つ。

給電側機器を「**PSE**」（Power sourcing equipment）、受電側機器を「**PD**」（Powered device）と呼ぶ。基本的にはPoEに対応した機器同士でなければ利用できないが、給電ユニット（PoEインジェクタ）や受電ユニットといった外部機器を併設する事により、PoE非対応の機器でも電力供給の恩恵を受けることができる。

### 運用上の注意

ツイストペアケーブルによる電源供給という特性から、一般にPoEでは以下の点に注意を要する。

1.  [活線挿抜](https://ja.wikipedia.org/wiki/活線挿抜 "wikilink")をすると接合部の放電により火花が発生し、機器トラブルや故障のおそれがある。[イーサネット](../Page/イーサネット.md "wikilink")も[ツイストペアケーブル](../Page/ツイストペアケーブル.md "wikilink")による活線挿抜を積極的には認めていない。
2.  規格に回路保護が盛り込まれておらず、これを実装しない製品では異常電圧発生時に大きな弱点となる。LANポート内のパルストランスの中点からPoEの電源回路へ直接接続されるため、PSE・PDのいずれのPoE機器においても屋外使用または屋外から引き込んだケーブルの接続を行うと、[雷サージ](../Page/雷サージ.md "wikilink")などにより異常電圧が機器電源部を直撃し、容易に損傷する。

特に日本における[内線規程](../Page/内線規程.md "wikilink")では、電力線（強電流回路）と信号線（弱電流回路）が区別されている。海外においては[TN-C接地や](https://ja.wikipedia.org/wiki/接地#TN "wikilink")[TN-S接地が多く用いられているが](https://ja.wikipedia.org/wiki/接地#TN "wikilink")、日本では信号線は一般に[TT接地が標準であるため](https://ja.wikipedia.org/wiki/接地#TT "wikilink")[等電位ボンディング](https://ja.wikipedia.org/wiki/等電位ボンディング "wikilink")が難しく、PoE機器を始めとする通信機器が壊れやすい環境であることに留意する必要がある\[1\]。

## 標準規格の実装

IEEE 802.3af, IEEE 802.3at, IEEE 802.3btで標準化された仕様を概説する。以降ではそれぞれaf, at, btと略記する。

### 給電タイプ

供給する電力量によってタイプ1～4が規定されている。

<table>
<thead>
<tr class="header">
<th><p>項目</p></th>
<th><p>タイプ1</p></th>
<th><p>タイプ2</p></th>
<th><p>タイプ3</p></th>
<th><p>タイプ4</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>対応規格</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>最大給電</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>最大受電</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>給電電圧</p></td>
<td><p>[2]</p></td>
<td><p>[3]</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>受電電圧</p></td>
<td><p>[4]</p></td>
<td><p>[5]</p></td>
<td><p>[6]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>最大電流 I<sub>max</sub></p></td>
<td><p>[7]</p></td>
<td><p>[8]</p></td>
<td><p>(1ペアあたり)[9]</p></td>
<td><p>(1ペアあたり)[10]</p></td>
</tr>
<tr class="odd">
<td><p>給電クラス</p></td>
<td><p>クラス1～3</p></td>
<td><p>クラス1～4</p></td>
<td><p>クラス1～6</p></td>
<td><p>クラス1～8</p></td>
</tr>
<tr class="even">
<td><p>使用ケーブル</p></td>
<td><p>Cat3, <a href="../Page/カテゴリー5ケーブル.md" title="wikilink">Cat5</a>[11]</p></td>
<td><p><a href="../Page/カテゴリー5ケーブル.md" title="wikilink">Cat5</a></p></td>
<td><p><a href="../Page/カテゴリー5ケーブル.md" title="wikilink">Cat5</a></p></td>
<td><p><a href="../Page/カテゴリー5ケーブル.md" title="wikilink">Cat5</a></p></td>
</tr>
<tr class="odd">
<td><p>ケーブル給電ピン</p></td>
<td><p>モードA, B</p></td>
<td><p>モードA, B</p></td>
<td><p>モードA, B, 4PPoE</p></td>
<td><p>4PPoE</p></td>
</tr>
</tbody>
</table>

### 給電クラス

接続開始時に、PSEは接続機器のシグネチャ抵抗によりPDに接続されたことを検出する。PDはPSEのシグネチャ検出時に自身の要求電力を以下のように分類電流として通知する（タイプ2以上は2度にわたって通知）。PSEはこれをクラスに分類し、その要求電力に合わせて給電を開始する\[12\]。

| | クラス | 分類電流                   | PD受電電力          | PSE給電電力 | 規格                 |
| ----- | ---------------------- | --------------- | ------- | ------------------ |
| 0     | 0 ～ 5 mA               | 0.44 ～ 13.0 W   | 15.4 W  | af, at, bt (デフォルト) |
| 1     | 8 ～ 13 mA              | 0.44 ～ 3.84 W   | 4.0 W   | af, at, bt (タイプ1)  |
| 2     | 16 ～ 21 mA             | 3.84 ～ 6.49 W   | 7.0 W   | af, at, bt (タイプ1)  |
| 3     | 25 ～ 31 mA             | 6.49 ～ 12.95 W  | 15.4 W  | af, at, bt (タイプ1)  |
| 4     | 35 ～ 45 mA             | 12.95 ～ 25.50 W | 30.0 W  | at, bt (タイプ2)      |
| 5     | 36 ～ 44 mA, 1 ～ 4 mA   | 40 W            | 45.0 W  | bt (タイプ3)          |
| 6     | 36 ～ 44 mA, 9 ～ 12 mA  | 51 W            | 60.0 W  | bt (タイプ3)          |
| 7     | 36 ～ 44 mA, 17 ～ 20 mA | 62 W            | 75.0 W  | bt (タイプ4)          |
| 8     | 36 ～ 44 mA, 26 ～ 30 mA | 71.3 W          | 99 W    | bt (タイプ4)          |
|       |                        |                 |         |                    |

このほかにタイプ2～4では[LLDP](https://ja.wikipedia.org/wiki/LLDP "wikilink")を使用した要求電力の通知方法も提供されており、0.1W刻みでの給電制御も可能となっている。

### ケーブル給電ピン

[ツイストペアケーブル](../Page/ツイストペアケーブル.md "wikilink")の8ピンのうち、給電に使用されるピンによって、以下の3つの方式が規定されている。

| 方式名称            | 給電ピン              | 備考                                                                                                                 |
| --------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------ |
| オルタナティブA (モードA) | 1・2・3・6番ピンを給電に用いる | [10BASE-T](../Page/10メガビット・イーサネット.md "wikilink")/[100BASE-TXでは](../Page/100メガビット・イーサネット.md "wikilink")4ピンのみでPoEできる |
| オルタナティブB (モードB) | 4・5・7・8番ピンを給電に用いる |                                                                                                                    |
| 4ペアPoE (4PPoE)  | すべてのピンを給電に用いる     | btのタイプ3・4のみ                                                                                                        |
|                 |                   |                                                                                                                    |

給電ピン選択とデータ通信用ピンとの関連は歴史的な経緯によるもので、いずれの方式であっても[10BASE-T](../Page/10メガビット・イーサネット.md "wikilink")・[100BASE-TX](../Page/100メガビット・イーサネット.md "wikilink")・[1000BASE-T](https://ja.wikipedia.org/wiki/1000BASE-T "wikilink")・[2.5GBASE-T](https://ja.wikipedia.org/wiki/マルチギガビット・イーサネット "wikilink")・[5GBASE-T](https://ja.wikipedia.org/wiki/マルチギガビット・イーサネット "wikilink")・[10GBASE-T](https://ja.wikipedia.org/wiki/10GBASE-T "wikilink")で利用可能である。給電側機器はいずれかをサポートしていればよいが、受電側機器は少なくともType A, Bのいずれからも受電できることが要求される。

## 非標準規格の実装

[シスコシステムズ](../Page/シスコシステムズ.md "wikilink")は、Universal Power Over Ethernet (UPoE) を2011年に発表、2014年に実装している。1ポートの4ペアすべてを給電に使用し最大60W給電を可能としている。

## 出典

## 関連項目

  - [HomePlug Powerline Alliance](../Page/HomePlug_Powerline_Alliance.md "wikilink")

[Category:IEEE_802](https://ja.wikipedia.org/wiki/Category:IEEE_802 "wikilink") [Category:ネットワークハードウェア](https://ja.wikipedia.org/wiki/Category:ネットワークハードウェア "wikilink") [Category:電源回路](https://ja.wikipedia.org/wiki/Category:電源回路 "wikilink") [Category:電力](https://ja.wikipedia.org/wiki/Category:電力 "wikilink")

1.  [CIAJ「雷過電圧に対する通信機器の保護ガイドライン CES-0040-2」](https://www.ciaj.or.jp/ciaj-wp/wp-content/uploads_sec/2014/06/CES_0040_2.pdf)
2.  IEEE 802.3at-2009 Table 33-11
3.
4.  IEEE 802.3at-2009 Table 33-18
5.
6.  IEEE 802.3bt Table 145-1
7.  IEEE 802.3at-2009 Table 33-1
8.
9.
10.
11. IEEE 802.3at-2009, clause 33.1.1c
12. IEEE 802.3at-2009, table 33-18