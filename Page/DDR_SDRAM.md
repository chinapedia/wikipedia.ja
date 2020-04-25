> この記事は[DDR SDRAM](https://ja.wikipedia.org/wiki/DDR_SDRAM)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Kingston_KVR400X64C3A-1G_20051111.jpg "wikilink") **DDR SDRAM** (Double-Data-Rate SDRAM)は、[SDRAM](../Page/SDRAM.md "wikilink")の一種で、クロックの立ち上がり/立ち下がりの両方を使うことで、片エッジのみ使用する（SDRの）SDRAMの倍速（Double-Data-Rate）でデータを転送する。また、その規格のひとつで最初のもの。[DDR2が後継である](../Page/DDR2_SDRAM.md "wikilink")。

DDR規格のプリフェッチバッファの深さ（depth）は2(ビット)である。

後継のDDR2にとって代わられるまで、パーソナルコンピュータにおいて2001年〜2005年頃（[Pentium 3後期](https://ja.wikipedia.org/wiki/Pentium_3 "wikilink")〜[Pentium 4前期](../Page/Pentium_4.md "wikilink")）の主要なメインメモリとして、携帯電話においては2007年〜2011年頃（ARM11やCortex-A8など）に用いられていた。

DDR SDRAMのメモリにはメモリチップとメモリモジュールの2つの規格が存在し、メモリチップ規格はチップの最大動作周波数、メモリモジュール規格はモジュールと機器間の最大転送速度を示している。

## 普及背景

20世紀末、[Intelは当初](https://ja.wikipedia.org/wiki/インテル "wikilink")、SDR SDRAMの次世代のメモリ規格をRambusの[RDRAM](../Page/RDRAM.md "wikilink")と目していた。1999年11月15日には初の対応[チップセット](../Page/チップセット.md "wikilink")[Intel 820を発表している](../Page/Intel_820.md "wikilink")。しかしRDRAMは、一筆書き配線などのエレガントな設計といった長所もあるものの、[Rambus社の特許で固められており](https://ja.wikipedia.org/wiki/ラムバス "wikilink")、勝手な改良が行えないことや製造に際しRambus社への特許料が発生するなど、メモリメーカーにとっては旨みが少ない、などの短所もまたあった。

価格の問題やIntel 820チップセットの製品回収にまで至った不具合、さらにはそのエレガントな設計の代償として未使用のメモリスロットに配線を終端まで接続させるためのダミーのモジュールが必要であるなどの利便性の悪さなどもあり、RDRAMのデスクトップ[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")用としての普及はつまづくことになった。[AMDはDDR](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") SDRAMを支持し、後にIntelもデスクトップPC/AT互換機用としてはRDRAMを断念したことで、DDR SDRAMがSDR SDRAMの次世代のメモリとなった。

## メモリチップの規格

最大動作周波数の違いによって分けられ、"DDR-"に続く3桁の数字で示される。この3桁数値はクロックの立ち上がり/立ち下がりを合わせた周波数(Double-Data-Rate)を示しており、実クロック（メモリバスクロック、2001年から2005年頃のパーソナルコンピュータにおいては[FSBクロックと同意](../Page/フロントサイドバス.md "wikilink")）はそれぞれの周波数の半分になる。

## メモリモジュールの規格

メモリモジュールは64bit構成であり、64bitは8Byteである。例えば333MHzで動作するPC2700の場合、毎秒2667[MByte](../Page/メガ.md "wikilink")(= 2.667[GByte](../Page/ギガ.md "wikilink")/sec)のデータ転送が行われる。それぞれの規格の名称はデータ転送速度に由来し、表記の4桁数値はGByte/secの小数点以下第2位を四捨五入したのちに小数点を取り除いた2桁へ、末尾にゼロ2桁を付したものである。

## 仕様

<table>
<thead>
<tr class="header">
<th><p>メモリチップ規格</p></th>
<th><p>メモリモジュール<br />
規格</p></th>
<th><p>最大動作周波数<br />
<small>(MHz)</small></p></th>
<th><p>加えることができる最大バスクロック周波数<br />
<small>(MHz)</small></p></th>
<th><p>最大転送速度<br />
<small>(GB/秒)</small></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DDR200</p></td>
<td><p>PC1600</p></td>
<td><p>200</p></td>
<td><p>100</p></td>
<td><p>1.600</p></td>
</tr>
<tr class="even">
<td><p>DDR266</p></td>
<td><p>PC2100</p></td>
<td><p>266</p></td>
<td><p>133</p></td>
<td><p>2.133</p></td>
</tr>
<tr class="odd">
<td><p>DDR333</p></td>
<td><p>PC2700</p></td>
<td><p>333</p></td>
<td><p>167</p></td>
<td><p>2.667</p></td>
</tr>
<tr class="even">
<td><p>DDR400</p></td>
<td><p>PC3200</p></td>
<td><p>400</p></td>
<td><p>200</p></td>
<td><p>3.200</p></td>
</tr>
<tr class="odd">
<td><p>DDR466</p></td>
<td><p>PC3700</p></td>
<td><p>466</p></td>
<td><p>233</p></td>
<td><p>3.733</p></td>
</tr>
<tr class="even">
<td><p>DDR500</p></td>
<td><p>PC4000</p></td>
<td><p>500</p></td>
<td><p>250</p></td>
<td><p>4.000</p></td>
</tr>
<tr class="odd">
<td><p>DDR533</p></td>
<td><p>PC4200</p></td>
<td><p>533</p></td>
<td><p>267</p></td>
<td><p>4.267</p></td>
</tr>
<tr class="even">
<td><p>DDR550</p></td>
<td><p>PC4400</p></td>
<td><p>550</p></td>
<td><p>275</p></td>
<td><p>4.400</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 後継規格

DDR SDRAMから派生した、更に低電圧・高クロック動作の[DDR2 SDRAMが](../Page/DDR2_SDRAM.md "wikilink")2004年頃から市場に出回り始め、2006年には市場で主流の規格となった。2003年には更に派生した[GDDR3](../Page/GDDR3.md "wikilink")（後述のDDR3 SDRAMとは別の規格である点に注意）を搭載した[ビデオカード](../Page/ビデオカード.md "wikilink")が出荷され、2006年には[DDR3 SDRAMの量産も開始されている](../Page/DDR3_SDRAM.md "wikilink")。

## 関連項目

  - [コンピュータ略語一覧](../Page/コンピュータ略語一覧.md "wikilink")

[el:Μνήμη τυχαίας προσπέλασης\#Τύποι μνήμης RAM](https://ja.wikipedia.org/wiki/el:Μνήμη_τυχαίας_προσπέλασης#Τύποι_μνήμης_RAM "wikilink") [fi:DRAM\#DDR SDRAM](https://ja.wikipedia.org/wiki/fi:DRAM#DDR_SDRAM "wikilink")

[Category:SDRAM](https://ja.wikipedia.org/wiki/Category:SDRAM "wikilink") [Category:コンピュータバス](https://ja.wikipedia.org/wiki/Category:コンピュータバス "wikilink")