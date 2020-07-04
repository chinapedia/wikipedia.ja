> この記事は[Blackfin](https://ja.wikipedia.org/wiki/Blackfin)から翻訳されています。


**Blackfin** は、[デジタルシグナルプロセッサ](../Page/デジタルシグナルプロセッサ.md "wikilink")（DSP）機能を組み込んだ16/32ビット[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")ファミリであり、小型で省電力の[マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")として使われている。[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")を動作させ、同時に[H.264](../Page/H.264.md "wikilink")ビデオエンコーディングのような複雑な数値的タスクを並行して行う、低消費電力の統合[プロセッサアーキテクチャ](https://ja.wikipedia.org/wiki/プロセッサアーキテクチャ "wikilink")である。

開発キットがいくつか存在し、[Linuxもサポートされている](https://ja.wikipedia.org/wiki/μClinux "wikilink")。現在は、[アナログ・デバイセズ](https://ja.wikipedia.org/wiki/アナログ・デバイセズ "wikilink")が製造している。

## アーキテクチャ

Blackfin プロセッサは、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")とアナログ・デバイセズが共同開発した MSA（Micro Signal Architecture）という[SIMD](../Page/SIMD.md "wikilink")アーキテクチャに基づく32ビット[RISC](../Page/RISC.md "wikilink") [MCU](../Page/マイクロコントローラ.md "wikilink") プログラミングモデルを使用している。

Blackfin プロセッサアーキテクチャは2000年12月に発表され、2001年6月の Embedded Systems Conference で実物が初公開された。

Blackfin アーキテクチャは、アナログ・デバイセズの[SHARCアーキテクチャとインテルの](../Page/Super_Harvard_Architecture_Single-Chip_Computer.md "wikilink")[XScale](../Page/XScale.md "wikilink")アーキテクチャのそれぞれの長所を取り入れ、そこにデジタルシグナルプロセッサ機能とマイクロコントローラ機能を統合したものである。Blackfin/MSA と XScale/ARM や SHARC には様々な相違点があるが、統合によって性能とプログラム容易性が向上し、これまでのDSPやRISCにはない低消費電力を実現した。

Blackfin アーキテクチャを実装したCPUは各種あり、それぞれ特定の応用分野を想定している。Blackfin ファミリは下表の通りである。アナログ・デバイセズの製品一覧は[こちら](http://www.analog.com/processors/blackfin/overview/IST.html)にある。

<table>
<thead>
<tr class="header">
<th><p>プロセッサ<br />
ADSP-</p></th>
<th><p>最大 クロック<br />
(MHz)</p></th>
<th><p>コア数</p></th>
<th><p>命令 L1 SRAM/<br />
(cache)<br />
(KB)</p></th>
<th><p>データ L1 SRAM/<br />
(cache)<br />
scratch<br />
(KB)</p></th>
<th><p>L2 SRAM<br />
(KB)</p></th>
<th><p>オン<br />
チップ<br />
フラッシュ</p></th>
<th><p>ホスト ポート</p></th>
<th><p>コード セキュリティ</p></th>
<th><p><a href="../Page/イーサネット.md" title="wikilink">イーサネット<br />
MAC</a></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/SDメモリカード" title="wikilink">SD/<br />
SDIO</a></p></th>
<th><p>16-bit PPIs</p></th>
<th><p>18/24-bit PPIs</p></th>
<th><p><a href="../Page/SDRAM.md" title="wikilink">SDRAM</a></p></th>
<th><p><a href="../Page/ユニバーサル・シリアル・バス.md" title="wikilink">USB</a></p></th>
<th><p><a href="../Page/Advanced_Technology_Attachment.md" title="wikilink">ATAPI</a></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Controller_Area_Network" title="wikilink">CAN</a></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/I²C" title="wikilink">I²C</a> (TWI)</p></th>
<th><p><a href="../Page/シリアル・ペリフェラル・インタフェース.md" title="wikilink">SPI</a></p></th>
<th><p><a href="../Page/UART.md" title="wikilink">UART</a></p></th>
<th><p>SPORT</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/GPIO" title="wikilink">GPIO</a></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Media_Oriented_Systems_Transport" title="wikilink">MXVR</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BF522<sup>1</sup></p></td>
<td><p>600</p></td>
<td><p>1</p></td>
<td><p>64 (16)</p></td>
<td><p>64 (32)<br />
4</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>0</p></td>
<td><p>SDR<br />
x16</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>2</p></td>
<td><p>48 pins</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>BF525<sup>1</sup></p></td>
<td><p>600</p></td>
<td><p>1</p></td>
<td><p>64 (16)</p></td>
<td><p>64 (32)<br />
4</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>0</p></td>
<td><p>SDR<br />
x16</p></td>
<td><p>2.0<br />
<a href="../Page/USB_On-The-Go.md" title="wikilink">OTG</a></p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>2</p></td>
<td><p>48 pins</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>BF527<sup>1</sup></p></td>
<td><p>600</p></td>
<td><p>1</p></td>
<td><p>64 (16)</p></td>
<td><p>64 (32)<br />
4</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>1</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>0</p></td>
<td><p>SDR<br />
x16</p></td>
<td><p>2.0<br />
OTG</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>2</p></td>
<td><p>48 pins</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>BF542</p></td>
<td><p>600</p></td>
<td><p>1</p></td>
<td><p>64 (16)</p></td>
<td><p>64 (32)<br />
4</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>Yes</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>0</p></td>
<td><p>DDR<br />
x16</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>3</p></td>
<td><p>3</p></td>
<td><p>152 pins</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>BF544</p></td>
<td><p>533</p></td>
<td><p>1</p></td>
<td><p>64 (16)</p></td>
<td><p>64 (32)<br />
4</p></td>
<td><p>64</p></td>
<td><p>-</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>DDR<br />
x16</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>2</p></td>
<td><p>2</p></td>
<td><p>2</p></td>
<td><p>3</p></td>
<td><p>3</p></td>
<td><p>152 pins</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>BF548</p></td>
<td><p>600</p></td>
<td><p>1</p></td>
<td><p>64 (16)</p></td>
<td><p>64 (32)<br />
4</p></td>
<td><p>128</p></td>
<td><p>-</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>DDR<br />
x16</p></td>
<td><p>2.0<br />
OTG</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>2</p></td>
<td><p>3</p></td>
<td><p>4</p></td>
<td><p>4</p></td>
<td><p>152 pins</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>BF549</p></td>
<td><p>533</p></td>
<td><p>1</p></td>
<td><p>64 (16)</p></td>
<td><p>64 (32)<br />
4</p></td>
<td><p>128</p></td>
<td><p>-</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>DDR<br />
x16</p></td>
<td><p>2.0<br />
OTG</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>2</p></td>
<td><p>3</p></td>
<td><p>4</p></td>
<td><p>4</p></td>
<td><p>152 pins</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>BF531</p></td>
<td><p>400</p></td>
<td><p>1</p></td>
<td><p>32 (16)</p></td>
<td><p>16 (16)<br />
4</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>-</p></td>
<td><p>SDR<br />
x16</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>16</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>BF532</p></td>
<td><p>400</p></td>
<td><p>1</p></td>
<td><p>48 (16)</p></td>
<td><p>32 (32)<br />
4</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>-</p></td>
<td><p>SDR<br />
x16</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>16</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>BF533</p></td>
<td><p>600</p></td>
<td><p>1</p></td>
<td><p>80 (16)</p></td>
<td><p>64 (32)<br />
4</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>-</p></td>
<td><p>SDR<br />
x16</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>16</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>BF534</p></td>
<td><p>500</p></td>
<td><p>1</p></td>
<td><p>64 (16)</p></td>
<td><p>64 (32)<br />
4</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>-</p></td>
<td><p>SDR<br />
x16</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>48</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>BF536</p></td>
<td><p>500</p></td>
<td><p>1</p></td>
<td><p>64 (16)</p></td>
<td><p>32 (32)<br />
4</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>-</p></td>
<td><p>SDR<br />
x16</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>48</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>BF537</p></td>
<td><p>600</p></td>
<td><p>1</p></td>
<td><p>64 (16)</p></td>
<td><p>64 (32)<br />
4</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>-</p></td>
<td><p>SDR<br />
x16</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>48</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>BF538</p></td>
<td><p>500</p></td>
<td><p>1</p></td>
<td><p>80 (16)</p></td>
<td><p>64 (32)<br />
4</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>-</p></td>
<td><p>SDR<br />
x16</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>3</p></td>
<td><p>3</p></td>
<td><p>4</p></td>
<td><p>54</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>BF538F</p></td>
<td><p>500</p></td>
<td><p>1</p></td>
<td><p>80 (16)</p></td>
<td><p>64 (32)<br />
4</p></td>
<td><p>-</p></td>
<td><p>512<br />
1024</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>-</p></td>
<td><p>SDR<br />
x16</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>3</p></td>
<td><p>3</p></td>
<td><p>4</p></td>
<td><p>54</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p>BF539</p></td>
<td><p>500</p></td>
<td><p>1</p></td>
<td><p>80 (16)</p></td>
<td><p>64 (32)<br />
4</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>-</p></td>
<td><p>SDR<br />
x16</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>3</p></td>
<td><p>3</p></td>
<td><p>4</p></td>
<td><p>38</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>BF539F</p></td>
<td><p>500</p></td>
<td><p>1</p></td>
<td><p>80 (16)</p></td>
<td><p>64 (32)<br />
4</p></td>
<td><p>-</p></td>
<td><p>512<br />
1024</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>-</p></td>
<td><p>SDR<br />
x16</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>3</p></td>
<td><p>3</p></td>
<td><p>4</p></td>
<td><p>38</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>BF561</p></td>
<td><p>600</p></td>
<td><p>2</p></td>
<td><p>64 (16)<br />
per core</p></td>
<td><p>64 (32)<br />
4<br />
per core</p></td>
<td><p>128</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>2</p></td>
<td><p>-</p></td>
<td><p>SDR<br />
x32</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>48</p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p>BF535</p></td>
<td><p>350</p></td>
<td><p>1</p></td>
<td><p>16</p></td>
<td><p>32<br />
4</p></td>
<td><p>256</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>SDR<br />
x16</p></td>
<td><p>1.1</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>2</p></td>
<td><p>2</p></td>
<td><p>2</p></td>
<td><p>16</p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
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

<sup>1</sup> BF52xC ファミリには、48kHz、ステレオ音声[CODEC](../Page/コーデック.md "wikilink") (2x[ADCs](../Page/アナログ-デジタル変換回路.md "wikilink"), 2x[DACs](../Page/デジタル-アナログ変換回路.md "wikilink")) が内蔵されている。

上の表に付け加えると、Blackfin プロセッサには共通して以下の周辺機器が内蔵されている。

  - デバッグ/[JTAG](../Page/JTAG.md "wikilink")インタフェース
  - [リアルタイムクロック](../Page/リアルタイムクロック.md "wikilink")
  - コア電圧[スイッチング電源](../Page/スイッチング電源.md "wikilink")
  - [ウォッチドッグタイマー](../Page/ウォッチドッグタイマー.md "wikilink")
  - タイマー/[PWM](../Page/パルス幅変調.md "wikilink") 出力/PWM 入力ポート
  - コアタイマー（コアのクロック周波数で動作するタイマー）

## 機能

### コア機能

Blackfin のコアが何であるかは、見方によって異なる。

  - 一部の人にとっては、[デジタルシグナルプロセッサ](../Page/デジタルシグナルプロセッサ.md "wikilink")がコアである。16ビット[MACを](../Page/積和演算.md "wikilink")2個、40ビット[ALUを](https://ja.wikipedia.org/wiki/演算論理装置 "wikilink")2個、40ビット[バレルシフタ](../Page/バレルシフタ.md "wikilink")1個備えている。そのため、同時に3個の命令を実行できる（[コンパイラ最適化](../Page/コンパイラ最適化.md "wikilink")または[プログラマ](../Page/プログラマ.md "wikilink")の技量による）。
  - 他の人にとっては、新たな[RISC](../Page/RISC.md "wikilink")コアである。[メモリ保護機能](https://ja.wikipedia.org/wiki/メモリ保護機能 "wikilink")を持ち、[CPUモード](../Page/CPUモード.md "wikilink")（ユーザー、カーネル）があり、シングルサイクル・[オペコード](../Page/オペコード.md "wikilink")で、データキャッシュと命令キャッシュを内蔵し、ビット/バイト/ワードテスト命令があり、各種オンチップ周辺機器がある。

[ISAも高度な表現能力を有し](../Page/命令セット.md "wikilink")、アセンブラプログラマやコンパイラがハードウェア機能を利用してアルゴリズムを高度に最適化することを可能にしている。

### メモリとDMA

Blackfin はバイト単位のアドレス指定が可能な平坦なメモリ空間を使っている。内蔵L1メモリ、内蔵L2メモリ、外部メモリ、メモリマップされた制御レジスタ群などは、全てこの32ビットアドレス空間に存在している。

L1内蔵SRAMメモリは、[ハーバード・アーキテクチャ](../Page/ハーバード・アーキテクチャ.md "wikilink")であり、コアのクロック速度で動作する。命令メモリとデータメモリは、それぞれ独立してコアと専用メモリバスで接続されていて、コアとL1メモリ間では高速なデータ転送が可能となっている。

L1メモリは、命令とデータそれぞれ独立して[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")として使うこともできる。

一部のBlackfinプロセッサには64KBから256KBのL2メモリがある。このメモリはコアのクロック速度より遅い。L2メモリ上では命令とデータが混在可能である。

Blackfinプロセッサは外部メモリとして SDRAM、DDR-SDRAM、NORフラッシュ、NANDフラッシュ、SRAM をサポートしている。また、一部のBlackfinには ATAPI や SD/SDIO といったインタフェースがサポートされている。これらは、外部メモリ空間として数百メガバイトをサポート可能である。

コアとメモリシステムの組み合わせで[DMAエンジンを構成でき](../Page/Direct_Memory_Access.md "wikilink")、任意の[周辺機器](../Page/周辺機器.md "wikilink")と主メモリ（および外部メモリ）との間でやり取りが可能である。プロセッサは各周辺機器と専用のDMAチャンネルを持っていて、リアルタイムの動画エンコーディング/デコーディングなども可能とする程度の高い[スループット](../Page/スループット.md "wikilink")を提供している。

### マイクロコントローラとしての機能

Blackfinアーキテクチャは、マイクロプロセッサやマイクロコントローラに共通して見られる特徴を備えている。これによってBlackfinは商用またはオープンソースの各種オペレーティングシステムを効率的に実行できるようになっている。

  - メモリ保護ユニット（Memory Protection Unit、MPU）
    全てのBlackfinプロセッサに内蔵されている。MPUは、メモリ空間全体について保護とキャッシュ戦略を提供する。これによって、ThreadX、µC/OS-II、Linux といった[RTOSやカーネルが動作可能となっている](../Page/リアルタイムオペレーティングシステム.md "wikilink")。MPU はいわゆる[メモリ管理ユニット](../Page/メモリ管理ユニット.md "wikilink")（MMU）にあるようなアドレス変換機構は持たないため、[仮想記憶](../Page/仮想記憶.md "wikilink")やプロセス毎のアドレス空間はサポートしていない。このため、Blackfinでは仮想記憶を前提とした WinCE や QNX のようなOSはサポートできない。なお、Blackfin の文書には MPU を MMU と呼んでいるものが多いので注意が必要である。
  - ユーザー/スーパーバイザーモード
    Blackfinには、スーパーバイザー、ユーザー、エミュレーションの3つの[CPUモード](../Page/CPUモード.md "wikilink")がある。スーパーバイザーモードでは、全プロセッサリソースにアクセス可能である。しかし、ユーザーモードでは、システムリソースやメモリ領域を保護できる（MPUの機能を利用）。最近のOSでは、[カーネル](../Page/カーネル.md "wikilink")がスーパーバイザーモードで動作し、通常のスレッド/プロセスはユーザーモードで動作する。スレッドはクラッシュしたり、保護されたリソース（メモリ、周辺機器、その他）にアクセスしようとしたとき、例外が発生し、カーネルが問題のスレッド/プロセスを停止させる。
  - 可変長[RISC](../Page/RISC.md "wikilink")風命令セット
    Blackfinの命令は、16ビット、32ビット、64ビットのものがある。よく使われる制御命令は16ビットで、DSPなどの命令は32ビットや64ビットになっている。これによって、コード密度を高めている。Blackfinの命令セットには、動画や画像の圧縮・伸張アルゴリズムに使われるピクセル処理の補助となる media processing extensions が含まれている。

## 周辺機器

Blackfin プロセッサは、様々な周辺機器接続手段を有する。

  - [USB 2.0 OTG (On-The-Go)](../Page/USB_On-The-Go.md "wikilink")
  - [ATAPI](../Page/Advanced_Technology_Attachment.md "wikilink")
  - MXVR : MOST ([Media Oriented Systems Transport](https://ja.wikipedia.org/wiki/Media_Oriented_Systems_Transport "wikilink")) Network Interface Controller。MOST は SMSCの登録商標である。
  - PPI (Parallel Peripheral Interface) : パラレル入出力ポート。[LCD](https://ja.wikipedia.org/wiki/液晶ディスプレイ "wikilink")、ビデオエンコーダ（ビデオDAC）、ビデオデコーダ（ビデオADC）、[CMOSイメージセンサ](../Page/CMOSイメージセンサ.md "wikilink")、[CCDイメージセンサ](../Page/CCDイメージセンサ.md "wikilink")その他のデバイスを接続できる。PPIは最高65MHzまでの速度で動作し、8ビットから16ビット幅で構成可能である。
  - SPORT : 同期式の高速シリアルポート。[TDM](../Page/時分割多重化.md "wikilink")、I2S（Inter-IC Sound）などの転送モードをサポートし、ADC、DAC、他のプロセッサ、FPGA などと接続する。
  - [CAN](https://ja.wikipedia.org/wiki/Controller_Area_Network "wikilink") : 自動車や産業用エレクトロニクスでよく使われている広域かつ低速なシリアルバス。
  - [UART](../Page/UART.md "wikilink")（Universal Asynchronous Receiver Transmitter）: [RS-232](../Page/RS-232.md "wikilink")機器（PC、モデム、PC周辺機器など）、[MIDI](../Page/MIDI.md "wikilink")機器、[IrDA](../Page/IrDA.md "wikilink")機器との双方向通信を可能にする。
  - [SPI](../Page/シリアル・ペリフェラル・インタフェース.md "wikilink") : 組み込みシステム向けの高速シリアルバス。
  - [I²C](https://ja.wikipedia.org/wiki/I²C "wikilink") : 低速シリアルバス。

全ての周辺制御レジスタは通常のアドレス空間内に[メモリマップされているため](https://ja.wikipedia.org/wiki/メモリマップドI/O "wikilink")、設定は容易である。

## 開発ツール

アナログ・デバイセズは独自の[開発ツール](https://ja.wikipedia.org/wiki/プログラミングツール "wikilink") CROSSCORE（VisualDSP++）を提供しているが、それ以外にも Green Hills Software の MULTI IDE、Blackfin 向け[GNUコンパイラコレクション](../Page/GNUコンパイラコレクション.md "wikilink")、National Instruments の [LabVIEW](../Page/LabVIEW.md "wikilink") Embedded Module などがある。

## サポートOS

Blackfin をサポートする[OSを下表に示す](../Page/オペレーティングシステム.md "wikilink")。

| 名称                                                                        | 種類                                                              | 備考                                     |
| ------------------------------------------------------------------------- | --------------------------------------------------------------- | -------------------------------------- |
| [µClinuxディストリビューション](../Page/ΜClinux.md "wikilink")                       | オープンソース/[GPL](../Page/GNU_General_Public_License.md "wikilink") | 通常のLinuxカーネルに統合されており、各種アプリケーションがある。    |
| [ThreadX](http://www.rtos.com/page/product.php?id=2)                      | 商用                                                              |                                        |
| [Nucleus](../Page/Nucleus_RTOS.md "wikilink")                             | 商用                                                              |                                        |
| [Fusion RTOS](http://www.unicoi.com/fusion_rtos/fusion_rtos_blackfin.htm) | 商用                                                              |                                        |
| [µC/OS-II](http://www.micrium.com/products/rtos/kernel/rtos.html)         | 商用/ソース利用可能                                                      |                                        |
| [velOSity](http://www.ghs.com/products/velosity.html)                     | 商用                                                              |                                        |
| [INTEGRITY](http://www.ghs.com/products/rtos/integrity.html)              | 商用                                                              |                                        |
| [RTEMS](https://ja.wikipedia.org/wiki/RTEMS "wikilink")                   | オープンソース/[GPL](../Page/GNU_General_Public_License.md "wikilink") |                                        |
| [T2 SDE](http://www.t2-project.org/)                                      | オープンソース/[GPL](../Page/GNU_General_Public_License.md "wikilink") |                                        |
| VDK                                                                       | 商用                                                              | アナログ・デバイセズのリアルタイム・カーネル。VisualDSP++ に同梱 |
| [TOPPERS/JSP](http://www.toppers.jp/jsp-kernel.html)                      | オープンソース                                                         | μITRON4.0仕様                            |
|                                                                           |                                                                 |                                        |

Blackfin向けOS/RTOS/カーネル

## 外部リンク

  - [Blackfin processor ウェブサイト](http://www.analog.com/jp/processors-dsp/blackfin/products/index.html)
  - [blackfin.uclinux.org](http://blackfin.uclinux.org/) Blackfin 向けの Linux カーネルとオープンソースのツール群

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink") [Category:命令セットアーキテクチャ](https://ja.wikipedia.org/wiki/Category:命令セットアーキテクチャ "wikilink")