> この記事は[JJY](https://ja.wikipedia.org/wiki/JJY)から翻訳されています。


**JJY**（ジェイ・ジェイ・ワイ）とは、[日本標準時](../Page/日本標準時.md "wikilink")を送信する[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")の[無線局](https://ja.wikipedia.org/wiki/無線局 "wikilink")である\[1\]。[総務省](../Page/総務省.md "wikilink")所管の[国立研究開発法人](https://ja.wikipedia.org/wiki/国立研究開発法人 "wikilink")[情報通信研究機構](../Page/情報通信研究機構.md "wikilink")（NICT）が運用している\[2\]。

JJYは[呼出符号](https://ja.wikipedia.org/wiki/呼出符号 "wikilink")（コールサイン）であるが、無線局そのものも指す。

## 概要

[電波法](../Page/電波法.md "wikilink")令上の[無線局](https://ja.wikipedia.org/wiki/無線局 "wikilink")の種別は[標準周波数局](https://ja.wikipedia.org/wiki/標準周波数局 "wikilink")である。原則として常時運用しているが、[メンテナンス](../Page/メンテナンス.md "wikilink")や[落雷](../Page/落雷.md "wikilink")などで[停波](../Page/停波.md "wikilink")することがある。周波数偏差などの情報はNICTより随時アナウンスされており、高精度な[周波数](../Page/周波数.md "wikilink")の基準として利用できる。また時刻の情報がタイムコードとして重畳されており、これを利用することにより[時計](../Page/時計.md "wikilink")の時刻を自動で調整することができる。従前は[短波](../Page/短波.md "wikilink")も使用していたが、[2001年](../Page/2001年.md "wikilink")[3月31日](../Page/3月31日.md "wikilink")正午以降は[長波](../Page/長波.md "wikilink")のみを使用している。

送信所は[福島県](../Page/福島県.md "wikilink")[田村市](../Page/田村市.md "wikilink")都路町の**[おおたかどや山標準電波送信所](https://ja.wikipedia.org/wiki/おおたかどや山標準電波送信所 "wikilink")**（周波数40[kHz](https://ja.wikipedia.org/wiki/キロヘルツ "wikilink")・[空中線電力](../Page/空中線電力.md "wikilink")50[kW](https://ja.wikipedia.org/wiki/キロワット "wikilink")・）、および[佐賀県](../Page/佐賀県.md "wikilink")[佐賀市](https://ja.wikipedia.org/wiki/佐賀市 "wikilink")[富士町の](../Page/富士町_\(佐賀県\).md "wikilink")**[はがね山標準電波送信所](../Page/はがね山標準電波送信所.md "wikilink")**（周波数60kHz・空中線電力50kW・）の2ヵ所に設けられている\[3\]。最初に[大鷹鳥谷山](https://ja.wikipedia.org/wiki/大鷹鳥谷山 "wikilink")（おおたかどややま）の送信所が[1999年](../Page/1999年.md "wikilink")[6月10日](../Page/6月10日.md "wikilink")に設けられ、その後、西日本地域への安定供給や大鷹鳥谷山局の補完を目的に[羽金山](../Page/羽金山.md "wikilink")（はがねやま）の送信所が2001年[10月1日](../Page/10月1日.md "wikilink")に置局された\[4\]。

### 送信内容

多くの長波報時局と同様に、JJYの信号にはタイムコードが重畳されている。1秒ごとに1ビットの情報を送信し、1分間（60ビット）で1セットの情報が送信される。日本国内で販売されている[電波時計](../Page/電波時計.md "wikilink")は上記いずれかの電波を受信し、時刻を自動的に調整する仕組みになっている（[電波時計](../Page/電波時計.md "wikilink")の項も参照）。

各秒のタイムコードの信号には、以下の3通りがある。ここで、「高出力」は定格の空中線電力、「低出力」はその10%の出力を意味する。

  - 0ビット - 0.8秒高出力の後、0.2秒低出力
  - 1ビット - 0.5秒高出力の後、0.5秒低出力
  - ポジションマーカー - 0.2秒高出力の後、0.8秒低出力

毎分0秒にマーカー、9、19、29、39、49の各秒および次の0秒の1秒前（通常は59秒。[うるう秒](https://ja.wikipedia.org/wiki/うるう秒 "wikilink")の場合は58秒または60秒）にポジションマーカーが送信される。残りの53ビットで時刻の情報を表す。[日本標準時](../Page/日本標準時.md "wikilink")（JST）による0秒のマーカを送信した時点の分、時、1月1日からの通算日（1月1日を1とする）、年（[西暦](../Page/西暦.md "wikilink")下2桁）、曜日は、それぞれの桁ごとに[二進数に変換する](../Page/二進法.md "wikilink")「[二進化十進表現](../Page/二進化十進表現.md "wikilink")」（BCD）で表現される。例えば、"23"は"0010 0011"と表される。[うるう秒の有無を通知するビットもあり](../Page/閏秒.md "wikilink")、うるう秒の挿入・削除が行われる月（UTCにおける月）の初日から、うるう秒の挿入・削除が行われるまで通知される。なお、日本には[夏時間](../Page/夏時間.md "wikilink")がないが、夏時間の有無を表すビットも用意されている。

タイムコードのフォーマットを以下に示す\[5\]\[6\]。最初の35秒はと同じであるが、それ以降は大きく異なっている。WWWBにある[DUT1](https://ja.wikipedia.org/wiki/DUT1 "wikilink")（[世界時](../Page/世界時.md "wikilink")（UT1）と[協定世界時](../Page/協定世界時.md "wikilink")（UTC）の差）の情報が省かれており、逆にWWVBにない曜日の情報や[パリティビット](../Page/パリティビット.md "wikilink")が加えられている。

ここで、"Weight"はそのビットの「重み付け」であり、1になっているビットの重み付けを全て加算すると、表したい数値になる。

<table>
<thead>
<tr class="header">
<th><p>Bit</p></th>
<th><p>Weight</p></th>
<th><p>意味</p></th>
<th><p> </p></th>
<th><p>Bit</p></th>
<th><p>Weight</p></th>
<th><p>意味</p></th>
<th><p> </p></th>
<th><p>Bit</p></th>
<th><p>Weight</p></th>
<th><p>意味</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>:00</p></td>
<td><p>M</p></td>
<td><p>マーカー<br />
分の開始を表す</p></td>
<td><p>:20</p></td>
<td><p>0</p></td>
<td><p>（未使用。常に0）</p></td>
<td><p>:40</p></td>
<td><p>SU2</p></td>
<td><p>（現行では未使用。常に0）<br />
（将来拡張のための予備:夏時間実施中のとき1）</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>:01</p></td>
<td><p>40</p></td>
<td><p>分</p></td>
<td><p>:21</p></td>
<td><p>0</p></td>
<td><p>:41</p></td>
<td><p>80</p></td>
<td><p>年</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>:02</p></td>
<td><p>20</p></td>
<td><p>:22</p></td>
<td><p>200</p></td>
<td><p>通算日<br />
1月1日=1<br />
平年の12月31日=365<br />
閏年の12月31日=366</p></td>
<td><p>:42</p></td>
<td><p>40</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>:03</p></td>
<td><p>10</p></td>
<td><p>:23</p></td>
<td><p>100</p></td>
<td><p>:43</p></td>
<td><p>20</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>:04</p></td>
<td><p>0</p></td>
<td><p>:24</p></td>
<td><p>0</p></td>
<td><p>:44</p></td>
<td><p>10</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>:05</p></td>
<td><p>8</p></td>
<td><p>:25</p></td>
<td><p>80</p></td>
<td><p>:45</p></td>
<td><p>8</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>:06</p></td>
<td><p>4</p></td>
<td><p>:26</p></td>
<td><p>40</p></td>
<td><p>:46</p></td>
<td><p>4</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>:07</p></td>
<td><p>2</p></td>
<td><p>:27</p></td>
<td><p>20</p></td>
<td><p>:47</p></td>
<td><p>2</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>:08</p></td>
<td><p>1</p></td>
<td><p>:28</p></td>
<td><p>10</p></td>
<td><p>:48</p></td>
<td><p>1</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>:09</p></td>
<td><p>P1</p></td>
<td><p>ポジションマーカー</p></td>
<td><p>:29</p></td>
<td><p>P3</p></td>
<td><p>:49</p></td>
<td><p>P5</p></td>
<td><p>ポジションマーカー</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>:10</p></td>
<td><p>0</p></td>
<td><p>（未使用。常に0）</p></td>
<td><p>:30</p></td>
<td><p>8</p></td>
<td><p>:50</p></td>
<td><p>4</p></td>
<td><p>曜日<br />
日曜日=0、土曜日=6</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>:11</p></td>
<td><p>0</p></td>
<td><p>:31</p></td>
<td><p>4</p></td>
<td><p>:51</p></td>
<td><p>2</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>:12</p></td>
<td><p>20</p></td>
<td><p>時</p></td>
<td><p>:32</p></td>
<td><p>2</p></td>
<td><p>:52</p></td>
<td><p>1</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>:13</p></td>
<td><p>10</p></td>
<td><p>:33</p></td>
<td><p>1</p></td>
<td><p>:53</p></td>
<td><p>LS1</p></td>
<td><p>月末にうるう秒が実施されることを示すビット</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>:14</p></td>
<td><p>0</p></td>
<td><p>:34</p></td>
<td><p>0</p></td>
<td><p>（未使用。常に0）</p></td>
<td><p>:54</p></td>
<td><p>LS2</p></td>
<td><p>うるう秒の種別。挿入=1、削除=0</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>:15</p></td>
<td><p>8</p></td>
<td><p>:35</p></td>
<td><p>0</p></td>
<td><p>:55</p></td>
<td><p>0</p></td>
<td><p>（未使用。常に0）</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>:16</p></td>
<td><p>4</p></td>
<td><p>:36</p></td>
<td><p>PA1</p></td>
<td><p>時のビット（:12–:18）の<a href="../Page/パリティビット.md" title="wikilink">偶数パリティ</a></p></td>
<td><p>:56</p></td>
<td><p>0</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>:17</p></td>
<td><p>2</p></td>
<td><p>:37</p></td>
<td><p>PA2</p></td>
<td><p>分のビット（:01–:08）の偶数パリティ</p></td>
<td><p>:57</p></td>
<td><p>0</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>:18</p></td>
<td><p>1</p></td>
<td><p>:38</p></td>
<td><p>SU1</p></td>
<td><p>（現行では未使用。常に0）<br />
（将来拡張のための予備:6日以内に夏時間開始または終了のとき1）</p></td>
<td><p>:58</p></td>
<td><p>0</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>:19</p></td>
<td><p>P2</p></td>
<td><p>ポジションマーカー</p></td>
<td><p>:39</p></td>
<td><p>P4</p></td>
<td><p>ポジションマーカー</p></td>
<td><p>:59</p></td>
<td><p>P0</p></td>
<td><p>ポジションマーカー</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

P0は常に分の最後である。うるう秒が挿入される場合、P0の前に0ビットが挿入され、P0は60秒に送信される。LS1とLS2は普段は0である。

1時間に2回、毎時15分と45分には、最後の20秒に普段とは違うコードが送される。40 - 48秒に、呼出符号"JJY"が[モールス符号](../Page/モールス符号.md "wikilink")で2回送信される。50 - 55秒の6ビットで、停波予告が通知される。年、曜日、うるう秒情報は送信しない\[7\]。

| Bit       | Weight        | 意味        |
| --------- | ------------- | --------- |
| :39       | P4            | ポジションマーカー |
| :40 - :48 | モールス符号による呼出符号 |           |
| :49       | P5            | ポジションマーカー |
| :50       | ST1           | 停波開始予告    |
| :51       | ST2           |           |
| :52       | ST3           |           |
| :53       | ST4           | 停波期間予告    |
| :54       | ST5           |           |
| :55       | ST6           |           |
| :56       | 0             | （未使用。常に0） |
| :57       | 0             |           |
| :58       | 0             |           |
| :59       | P0            | ポジションマーカー |

ST1 - ST3は、何日または何時間後に停波の予定があるかを表す。

| ST1 | ST2 | ST3 | 意味          |
| --- | --- | --- | ----------- |
| 0   | 0   | 0   | 停波予定なし      |
| 0   | 0   | 1   | 7日以内に停波     |
| 0   | 1   | 0   | 3 - 6日以内に停波 |
| 0   | 1   | 1   | 2日以内に停波     |
| 1   | 0   | 0   | 24時間以内に停波   |
| 1   | 0   | 1   | 12時間以内に停波   |
| 1   | 1   | 0   | 2時間以内に停波    |

ST4が1の場合は、停波が昼間のみであることを意味する。0の場合は終日停波すること（または停波予定なし）を意味する。

ST5とST6は、停波の期間を表す。

| ST5 | ST6 | 意味          |
| --- | --- | ----------- |
| 0   | 0   | 停波の予定なし     |
| 0   | 1   | 7日以上または期間未定 |
| 1   | 0   | 2 - 6日      |
| 1   | 1   | 2日未満        |

停波の予定がない場合は、STビットは全て0になる。

## 以前の運用形態

### 短波JJY

2001年3月31日に廃止された短波のJJYは、[1940年](../Page/1940年.md "wikilink")[1月30日](../Page/1月30日.md "wikilink")に[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")・[WWVに続いて世界で](https://ja.wikipedia.org/wiki/w:WWV_\(radio_station\) "wikilink")2番目の短波標準電波局として、[千葉県](../Page/千葉県.md "wikilink")[千葉郡](../Page/千葉郡.md "wikilink")[検見川町](https://ja.wikipedia.org/wiki/検見川町 "wikilink")（現・千葉市[花見川区](../Page/花見川区.md "wikilink")検見川町）に開設された。以来、短波を使った標準無線局と位置付けられた。その後、[1949年](../Page/1949年.md "wikilink")に東京都[北多摩郡](../Page/北多摩郡.md "wikilink")[小金井町](../Page/小金井市.md "wikilink")（現・東京都小金井市）に移転した。昭和40年代頃から、周辺の宅地化に伴い電波障害などの弊害が顕著になったことや小金井市[緑町にある庁舎にあった周波数標準部の同市](https://ja.wikipedia.org/wiki/緑町_\(小金井市\) "wikilink")[貫井北町](https://ja.wikipedia.org/wiki/貫井北町 "wikilink")への移転（[1974年](../Page/1974年.md "wikilink")6月から[1975年](../Page/1975年.md "wikilink")1月にかけて実施）などにより、[1977年](../Page/1977年.md "wikilink")[12月1日](../Page/12月1日.md "wikilink")からは[茨城県](../Page/茨城県.md "wikilink")[猿島郡](../Page/猿島郡.md "wikilink")[三和町](../Page/三和町_\(茨城県\).md "wikilink")（現・[古河市](../Page/古河市.md "wikilink")）の[NTT名崎送信所からの送信となり次の周波数で発信していた](https://ja.wikipedia.org/wiki/名崎送信所 "wikilink")。

#### 周波数

  - 2.5[MHz](https://ja.wikipedia.org/wiki/メガヘルツ "wikilink")
  - 5MHz
  - 8MHz
  - 10MHz
  - 15MHz

上記のうち8MHz波以外は近隣地域の標準電波と周波数が同じであり、[西日本](../Page/西日本.md "wikilink")地域を中心に日中でも[混信](../Page/混信.md "wikilink")の影響を免れられなかった。廃止時まで運用されていたのは3波（5/8/10MHz）である。

#### 送信内容

送信内容は、数度変更されている。以下に、停波前直近の送信内容を記述する。

電波は短波ラジオで受信でき、内容としては以下の組み合わせがずっと流れていた。ただし毎時35分0秒から39分0秒までは諸外国の標準周波数局との較正作業の為に停止していた。

  - 1秒毎のコッコッという信号音（周波数1600[Hz](../Page/ヘルツ.md "wikilink")、毎正秒から5ミリ秒間）
  - 毎時10分毎（00・10・20・30・40・50分）の前半（x0分0.045秒からx4分58.960秒まで）に連続的なピーという信号音（周波数1000Hz、毎正秒の45ミリ秒後から960ミリ秒後まで。毎分59秒の時間帯を除く）
  - 1分毎のポーという信号音（分予告信号：周波数600Hz、毎分59.045秒から59.700秒まで。うるう秒がある場合は1.000秒前後する）

[世界時](../Page/世界時.md "wikilink")（UT1）から[協定世界時](../Page/協定世界時.md "wikilink")（UTC）を引いた時刻差([DUT1](https://ja.wikipedia.org/wiki/DUT1 "wikilink"))の予測値も0.1秒の精度で以下の形式により通報された。

  - 予測値により以下の1600Hz秒信号を40ミリ秒引き伸ばし、毎正秒から45ミリ秒間とする（*n*を1≦*n*≦8の[自然数](../Page/自然数.md "wikilink")とする）
      - \+0.1×*n*秒の場合 - 毎分1秒から*n*秒まで
      - −0.1×*n*秒の場合 - 毎分9秒から8+*n*秒まで
  - 予測値が0.0秒の場合 - 1600Hz秒信号は本則どおり5ミリ秒間とする

毎時10分毎のポーという信号音の前（x9分30秒からx9分52秒まで）には上記の信号音に重ねてモールス信号（信号音周波数1000Hz）の「JJY JJY hhmm（[24時制](https://ja.wikipedia.org/wiki/24時制 "wikilink")の時・分を4桁数字に符号化したもの。例として9時00分は「0900」、16時30分は「1630」）」が流れ、続いて女声の合成音声で「JJY、JJY、○時、○分、JST」とアナウンスがあり、最後に電波警報（モールス信号で伝播状態のステータスを5回続けて）が流された。

  - N - ノーマル：伝播状態が正常である
  - U - アンステーブル（不安定）：伝播状態に異常（[磁気嵐](../Page/磁気嵐.md "wikilink")、[Eスポなど](../Page/スポラディックE層.md "wikilink")）が発生する可能性がある
  - W - ワーニング：伝播状態に異常が発生している

時計の修正に限らず、正確な周波数であることを利用してアナログ式短波受信機での受信の手助けになっていた。また[アマチュア無線](https://ja.wikipedia.org/wiki/アマチュア無線 "wikilink")機等の短波無線機での周波数表示の較正にも利用された（ダブルビート法で[マーカー発振器](https://ja.wikipedia.org/wiki/マーカー発振器 "wikilink")を較正、正しく調整されたこのマーカーで更に周波数表示器を修正）。

## テレホンJJY

  -
    一般の電話回線を利用した日本標準時・協定世界時提供サービス「テレホンJJY」（TEL-JJY）も行っている。精度は±1ms。なお利用には[パソコン通信](../Page/パソコン通信.md "wikilink")用のアナログ[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")、もしくはテレホンJJYに対応した専用機器が必要。パソコン通信・[ファクシミリ](https://ja.wikipedia.org/wiki/ファクシミリ "wikilink")の利用者減少によってアナログモデムが入手困難になってきていたり、4800bps以上の高速通信には対応していなかったり、さらに高精度なものが必要とされているため、2016年5月26日からNTT東日本・西日本の光電話回線網を使用した「光テレホンJJY」の試験サービスが行われ、2019年2月1日から本格運用を開始している。
    テレホンJJYは、2024年3月末にサービス終了予定\[8\]。
    NTT東日本・西日本の時報（117番）の校正や、公共交通機関・放送局の標準時計の校正などで使用されており\[9\]、2018年2月の時点で月に16万回以上のアクセスがある\[10\]。

## 参考文献

  -
## 脚注

## 関連項目

  - [情報通信研究機構](../Page/情報通信研究機構.md "wikilink")
  - [標準周波数局](https://ja.wikipedia.org/wiki/標準周波数局 "wikilink")
  - [標準電波](../Page/標準電波.md "wikilink")
  - [電波時計](../Page/電波時計.md "wikilink")

## 外部リンク

  - [情報通信研究機構・日本標準時グループ](http://jjy.nict.go.jp/index.html)（[年表 - WebArchive](http://web.archive.org/web/20040228093549/http://jjy.crl.go.jp/Data-room/chrono_table.html)）

  - [標準電波](http://www.jarl.org/Japanese/7_Technical/lib1/jjy.htm)（[日本アマチュア無線連盟](../Page/日本アマチュア無線連盟.md "wikilink")）

  -
  - [標準時報局 JJY](http://ogino.c.ooco.jp/bcl/jjy.htm)（個人サイト）

  - [名崎無線送信所研究サイト](http://x680.x0.com/nazaki-tx1/WEB/INDEX1.htm)（個人サイト）

[Category:日本の時間](https://ja.wikipedia.org/wiki/Category:日本の時間 "wikilink") [Category:無線局](https://ja.wikipedia.org/wiki/Category:無線局 "wikilink") [Category:登録商標](https://ja.wikipedia.org/wiki/Category:登録商標 "wikilink") [Category:標準時](https://ja.wikipedia.org/wiki/Category:標準時 "wikilink") [Category:呼出符号](https://ja.wikipedia.org/wiki/Category:呼出符号 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.