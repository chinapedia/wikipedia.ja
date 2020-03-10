> この記事は[DDR2 SDRAM](https://ja.wikipedia.org/wiki/DDR2_SDRAM)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Corsair_CM2X1024-6400C5DHX_20080221.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:1GB_DDR2_SO-DIMM.png "wikilink") **DDR2 SDRAM** (Double-Data-Rate2 Synchronous Dynamic Random Access Memory) は、半導体[集積回路](../Page/集積回路.md "wikilink")で構成される[DRAMの規格の一種である](../Page/Dynamic_Random_Access_Memory.md "wikilink")。

4ビットの[プリフェッチ](https://ja.wikipedia.org/wiki/プリフェッチ "wikilink")機能（CPUがデータを必要とする前にメモリから先読みして取り出す機能）をもつ。内部クロックの2倍の外部クロックを用いるため、クロックの等倍で動作する[DDR SDRAMの](https://ja.wikipedia.org/wiki/DDR_SDRAM "wikilink")2倍、[SDRAM](https://ja.wikipedia.org/wiki/SDRAM "wikilink")の4倍のデータ転送速度が理論上得られる。パーソナルコンピュータにおいて2005年〜2009年頃（[Pentium 4後期](../Page/Pentium_4.md "wikilink")〜[Intel Core 2](https://ja.wikipedia.org/wiki/Intel_Core_2 "wikilink")）の主要なメインメモリとして、携帯電話においては2011年から（Cortex-A9など）用いられている。

## 仕様

[thumb](https://ja.wikipedia.org/wiki/ファイル:Desktop_DDR_Memory_Comparison.svg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Laptop_SODIMM_DDR_Memory_Comparison_V2.svg "wikilink") DDR2 SDRAMにはメモリチップとメモリモジュールの2つの規格が存在し、メモリチップ規格は最大動作**周波数**、モジュール規格は搭載メモリチップの（すなわちメモリモジュールとしての）**転送速度**を示している。以下、バス幅64ビットの場合の表。パソコンで使われるDDR2はシングルチャンネルは64ビットをさすが、携帯電話などで使われるLPDDR2はバス幅32ビットがシングルチャネルを指すことに注意。

<table>
<thead>
<tr class="header">
<th><p>チップ規格</p></th>
<th><p>モジュール<br />
規格</p></th>
<th><p>メモリクロック<br />
<small>(MHz)</small></p></th>
<th><p>バスクロック<br />
<small>(MHz)</small></p></th>
<th><p>転送速度<br />
<small>(GB/秒)</small></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DDR2-400</p></td>
<td><p>PC2-3200</p></td>
<td><p>100</p></td>
<td><p>200</p></td>
<td><p>3.200</p></td>
</tr>
<tr class="even">
<td><p>DDR2-533</p></td>
<td><p>PC2-4200</p></td>
<td><p>133</p></td>
<td><p>266</p></td>
<td><p>4.267</p></td>
</tr>
<tr class="odd">
<td><p>DDR2-667</p></td>
<td><p>PC2-5300</p></td>
<td><p>166</p></td>
<td><p>333</p></td>
<td><p>5.333</p></td>
</tr>
<tr class="even">
<td><p>DDR2-800</p></td>
<td><p>PC2-6400</p></td>
<td><p>200</p></td>
<td><p>400</p></td>
<td><p>6.400</p></td>
</tr>
<tr class="odd">
<td><p>DDR2-900</p></td>
<td><p>PC2-7200</p></td>
<td><p>225</p></td>
<td><p>450</p></td>
<td><p>7.200</p></td>
</tr>
<tr class="even">
<td><p>DDR2-1000</p></td>
<td><p>PC2-8000</p></td>
<td><p>250</p></td>
<td><p>500</p></td>
<td><p>8.000</p></td>
</tr>
<tr class="odd">
<td><p>DDR2-1066</p></td>
<td><p>PC2-8500</p></td>
<td><p>266</p></td>
<td><p>533</p></td>
<td><p>8.533</p></td>
</tr>
<tr class="even">
<td><p>DDR2-1150</p></td>
<td><p>PC2-9200</p></td>
<td><p>287</p></td>
<td><p>575</p></td>
<td><p>9.200</p></td>
</tr>
<tr class="odd">
<td><p>DDR2-1200</p></td>
<td><p>PC2-9600</p></td>
<td><p>300</p></td>
<td><p>600</p></td>
<td><p>9.600</p></td>
</tr>
</tbody>
</table>

チップ「DDR2-800」モジュール「PC2-6400」以降（数字が大きいものほど新しい）は、チップ規格の「DDR2-1066」を除き[JEDEC](https://ja.wikipedia.org/wiki/JEDEC "wikilink")で規格制定されていない独自仕様である。

## 低電圧版

通常の DDR2 は 1.8V 駆動。

  - **LV-DDR2** (**DDR2L**) - 1.5V
  - **LPDDR2** - 1.2V

## モジュール

モジュールの動作電源電圧は、用いるメモリチップの[リーク電流](https://ja.wikipedia.org/wiki/リーク電流 "wikilink")が減少したことが可能にした（従前規格であるDDR SDRAMの2.5V/2.6Vに比してより低い）1.8Vであり、これの副次効果として高い[スルー・レート](https://ja.wikipedia.org/wiki/スルー・レート "wikilink")と消費[電力](../Page/電力.md "wikilink")の低減、それによる[発熱](https://ja.wikipedia.org/wiki/発熱 "wikilink")の減少が得られた。動作電源電圧の差異からDDR SDRAMモジュールとの互換性はない。

### 日本における市場動向

[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")用途のものは、2004年から出回り始め、2006年以降、市場で主流のメモリモジュール規格となった。[Pentium 4後期から](../Page/Pentium_4.md "wikilink")[Core 2あたりまで使われていた](https://ja.wikipedia.org/wiki/Core_2 "wikilink")。Core 2 の FSB は最高でも 1600MHz (12.8GB/s) だったため、DDR2-800 をデュアルチャンネル構成で用いる(12.8GB/s)ことで十分であった。2009年では容量あたりの販売価格が非常に安いメモリであったが、後継の規格として一層の高速動作・消費電力低減を実現した[DDR3 SDRAMが](https://ja.wikipedia.org/wiki/DDR3_SDRAM "wikilink")2007年から市場に出回り始め、2010年には[自作パソコン](https://ja.wikipedia.org/wiki/自作パソコン "wikilink")向けマザーボードの新作ラインアップはほぼ完全にDDR3 SDRAMに移行した。

## 関連項目

  - [レイテンシ](https://ja.wikipedia.org/wiki/レイテンシ "wikilink") (CAS-TRCD-TRP-TRAS)
  - [JEDEC](https://ja.wikipedia.org/wiki/JEDEC "wikilink")

[de:DDR-SDRAM\#DDR2-SDRAM](https://ja.wikipedia.org/wiki/de:DDR-SDRAM#DDR2-SDRAM "wikilink") [fi:DRAM\#DDR2 SDRAM](https://ja.wikipedia.org/wiki/fi:DRAM#DDR2_SDRAM "wikilink")

[Category:半導体メモリ](https://ja.wikipedia.org/wiki/Category:半導体メモリ "wikilink") [Category:コンピュータバス規格](https://ja.wikipedia.org/wiki/Category:コンピュータバス規格 "wikilink")