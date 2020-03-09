> この記事は[FLOPS](https://ja.wikipedia.org/wiki/FLOPS)から翻訳されています。


| 換算表                                                    |
| ------------------------------------------------------ |
| 接頭辞                                                    |
| [ヨタ](https://ja.wikipedia.org/wiki/ヨタ "wikilink")(Y)   |
| [ゼタ](https://ja.wikipedia.org/wiki/ゼタ "wikilink")(Z)   |
| [エクサ](https://ja.wikipedia.org/wiki/エクサ "wikilink")(E) |
| [ペタ](https://ja.wikipedia.org/wiki/ペタ "wikilink")(P)   |
| [テラ](https://ja.wikipedia.org/wiki/テラ "wikilink")(T)   |
| [メガ](https://ja.wikipedia.org/wiki/メガ "wikilink")(M)   |

**FLOPS**（フロップス、***Fl**oating-point **O**perations **P**er **S**econd*）は[コンピュータ](../Page/コンピュータ.md "wikilink")の[性能](https://ja.wikipedia.org/wiki/性能 "wikilink")[指標](https://ja.wikipedia.org/wiki/指標 "wikilink")の一つ。

## 概要

FLoating point number Operations Per Secondの名称が示す通り、**1秒間に[浮動小数点演算](https://ja.wikipedia.org/wiki/浮動小数点演算 "wikilink")が何回できるか**の指標値ひいては性能値の事を指す。

ハードウェアの仕様として用いられるのは理論値であるが、[ベンチマーク](https://ja.wikipedia.org/wiki/ベンチマーク "wikilink")ソフトなどの計測から導き出される計測値は、理論値からは原則的に下がる。その為、理論値だけでなく、「理論的に算出された値の何%で実際の[プログラムが動作するか](https://ja.wikipedia.org/wiki/プログラム_\(コンピュータ\) "wikilink")」ということが重要になる（実測値）。実際の値が理論値に近いほど、より効率的なコンピュータだと考えられるからである。

[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")（以下PCと表記）向けの[CPU](../Page/CPU.md "wikilink")や[GPU](https://ja.wikipedia.org/wiki/GPU "wikilink")メーカーは、計算[ノード](https://ja.wikipedia.org/wiki/ノード "wikilink")としては単一のノードとなるので通常理論値で発表する（理論値がほぼそのまま実効値となる）が、一般的に並列方式[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")（以下スパコンと表記）では多数の計算ノードの[クラスタ](https://ja.wikipedia.org/wiki/クラスタ "wikilink")として構築されるため、実際の計算能力を理論値に近づけるには高度な運用能力が必要であり、理論値ではなく [LINPACK](https://ja.wikipedia.org/wiki/LINPACK "wikilink") [ベンチマーク](https://ja.wikipedia.org/wiki/ベンチマーク "wikilink")での実測値がよく使われている。

[2016年](https://ja.wikipedia.org/wiki/2016年 "wikilink")前後の時点において、普及している家庭用のPCのCPUはGFLOPS、スパコンの世界1位はPFLOPSの単位であるが、[ムーアの法則](../Page/ムーアの法則.md "wikilink")にそって高速化が進んでおり、[2018年](https://ja.wikipedia.org/wiki/2018年 "wikilink")に並列度1億でLINPACK性能値はEFLOPSの単位に到達すると予想されている\[1\]。[2000年](../Page/2000年.md "wikilink")頃からの理論値ではPCとスパコンの比例値は、おおよそ1万倍の差で推移している。

2019年6月現在世界最高速のスパコンは[Summitで](https://ja.wikipedia.org/wiki/Summit_\(スーパーコンピュータ\) "wikilink")200PFLOPSとなっている\[2\]。

## 代表的なハードウェアの浮動小数点数演算能力

### PC (Intel)

<table>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>コア数</p></th>
<th><p>クロック</p></th>
<th><p>FLOPS（倍精度）</p></th>
<th><p>理論値/実測値</p></th>
<th><p>理論値の計算式</p></th>
<th><p>参照</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Intel_Pentium_(1993年)" title="wikilink">Pentium</a></p></td>
<td><p>1コア</p></td>
<td><p>300MHz</p></td>
<td><p>300 MFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>1 FLOPS/Clock × 300MHz</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Pentium_II" title="wikilink">Pentium II</a></p></td>
<td><p>1コア</p></td>
<td><p>450MHz</p></td>
<td><p>450 MFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>1 FLOPS/Clock × 450MHz</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Pentium_III" title="wikilink">Pentium III</a></p></td>
<td><p>1コア</p></td>
<td><p>1.4GHz</p></td>
<td><p>2.1 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>1.5 FLOPS/Clock × 1.4GHz</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Pentium_M" title="wikilink">Pentium M</a></p></td>
<td><p>1コア</p></td>
<td><p>2.26GHz</p></td>
<td><p>3.39 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>1.5 FLOPS/Clock × 2.26GHz</p></td>
<td><p>[3]</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Pentium_4.md" title="wikilink">Pentium 4</a></p></td>
<td><p>1コア</p></td>
<td><p>3.8GHz</p></td>
<td><p>7.6 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>2 FLOPS/Clock × 3.8GHz</p></td>
<td><p>[4]</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Pentium_D" title="wikilink">Pentium D</a></p></td>
<td><p>2コア</p></td>
<td><p>3.6GHz</p></td>
<td><p>14.4 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>2 FLOPS/Clock × 3.6GHz × 2コア</p></td>
<td><p>[5]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Intel_Atom" title="wikilink">Intel Atom</a><br />
(Bonnell)</p></td>
<td><p>2コア</p></td>
<td><p>1.8GHz</p></td>
<td><p>5.4 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>1.5 FLOPS/Clock × 1.8GHz × 2コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Core_Solo" title="wikilink">Core Solo</a></p></td>
<td><p>1コア</p></td>
<td><p>1.83GHz</p></td>
<td><p>2.75 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>1.5 FLOPS/Clock × 1.83GHz</p></td>
<td><p>[6]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Core_Duo" title="wikilink">Core Duo</a></p></td>
<td><p>2コア</p></td>
<td><p>2.33GHz</p></td>
<td><p>6.99 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>1.5 FLOPS/Clock × 2.33GHz × 2コア</p></td>
<td><p>[7]</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Core_2_Duo" title="wikilink">Core 2 Duo</a></p></td>
<td><p>2コア</p></td>
<td><p>3.33GHz</p></td>
<td><p>26.64 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>4 FLOPS/Clock × 3.33GHz × 2コア</p></td>
<td><p>[8]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Core_2_Extreme" title="wikilink">Core 2 Extreme</a></p></td>
<td><p>4コア</p></td>
<td><p>3.2GHz</p></td>
<td><p>51.2 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>4 FLOPS/Clock × 3.2GHz × 4コア</p></td>
<td><p>[9]</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Core_i7" title="wikilink">Core i7</a><br />
(<a href="https://ja.wikipedia.org/wiki/Nehalem" title="wikilink">Nehalem</a>)</p></td>
<td><p>4コア</p></td>
<td><p>3.33GHz</p></td>
<td><p>53.28 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>4 FLOPS/Clock × 3.33GHz × 4コア</p></td>
<td><p>[10]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Core_i7" title="wikilink">Core i7</a><br />
(<a href="https://ja.wikipedia.org/wiki/Westmere" title="wikilink">Westmere</a>)</p></td>
<td><p>6コア</p></td>
<td><p>3.46GHz</p></td>
<td><p>83.04 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>4 FLOPS/Clock × 3.46GHz × 6コア</p></td>
<td><p>[11]</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Core_i7" title="wikilink">Core i7</a><br />
(<a href="https://ja.wikipedia.org/wiki/Sandy_Bridge" title="wikilink">Sandy Bridge</a>)</p></td>
<td><p>6コア</p></td>
<td><p>3.3GHz</p></td>
<td><p>158.4 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>8 FLOPS/Clock × 3.3GHz × 6コア</p></td>
<td><p>[12][13]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Core_i7" title="wikilink">Core i7</a><br />
(<a href="https://ja.wikipedia.org/wiki/Haswell" title="wikilink">Haswell</a>)</p></td>
<td><p>8コア</p></td>
<td><p>3.0 GHz (ベース)<br />
3.5 GHz (ターボ)</p></td>
<td><p>384 GFLOPS (ベース)<br />
448 GFLOPS (ターボ)</p></td>
<td><p>理論値</p></td>
<td><p>16 FLOPS/Clock × 3.0 GHz × 8コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Core_i7" title="wikilink">Core i7</a><br />
(<a href="https://ja.wikipedia.org/wiki/Broadwellマイクロアーキテクチャ" title="wikilink">Broadwell</a>)</p></td>
<td><p>10コア</p></td>
<td><p>3.0 GHz (ベース)<br />
3.5 GHz (ターボ)</p></td>
<td><p>480 GFLOPS (ベース)<br />
560 GFLOPS (ターボ)</p></td>
<td><p>理論値</p></td>
<td><p>16 FLOPS/Clock × 3.0 GHz × 10コア</p></td>
<td></td>
</tr>
</tbody>
</table>

Core 2 Duoより1クロックで [SSE](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令 "wikilink") で加算と乗算が計算できる\[14\]ようになり128ビット幅だと倍精度で 4 FLOPS/クロック。Sandy Bridgeより搭載した Intel AVXは256ビット幅なので8FLOPS/クロック。Intel AVX 2はFMA命令の導入により1サイクルで2つのFMAが実行できる\[15\]ので16FLOPS/クロック。単精度だと、これらの演算回数は2倍\[16\]。Atomは1クロックで1つのSSE加算命令が、2クロックで1つのSSE乗算命令が実行できる\[17\]ため、合計すると倍精度で3FLOPS/クロックとなる。

### サーバ (Intel)

<table>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>コア数</p></th>
<th><p>クロック</p></th>
<th><p>FLOPS（倍精度）</p></th>
<th><p>理論値/実測値</p></th>
<th><p>理論値の計算式</p></th>
<th><p>参照</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Xeon<br />
(<a href="https://ja.wikipedia.org/wiki/Nehalem" title="wikilink">Nehalem</a>)</p></td>
<td><p>8コア</p></td>
<td><p>2.26 GHz</p></td>
<td><p>72.32 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>4 FLOPS/Clock × 2.26 GHz × 8コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xeon<br />
(<a href="https://ja.wikipedia.org/wiki/Westmere" title="wikilink">Westmere</a>)</p></td>
<td><p>10コア</p></td>
<td><p>2.4 GHz</p></td>
<td><p>96 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>4 FLOPS/Clock × 2.4 GHz × 10コア</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Xeon<br />
(<a href="https://ja.wikipedia.org/wiki/Sandy_Bridge" title="wikilink">Sandy Bridge</a>)</p></td>
<td><p>8コア</p></td>
<td><p>3.1 GHz</p></td>
<td><p>198.4 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>8 FLOPS/Clock × 3.1 GHz × 8コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xeon<br />
(<a href="https://ja.wikipedia.org/wiki/Ivy_Bridge" title="wikilink">Ivy Bridge</a>)</p></td>
<td><p>15コア</p></td>
<td><p>2.8 GHz</p></td>
<td><p>336 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>8 FLOPS/Clock × 2.8 GHz × 15コア</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Xeon<br />
(<a href="https://ja.wikipedia.org/wiki/Haswell" title="wikilink">Haswell</a>)</p></td>
<td><p>18コア</p></td>
<td><p>2.3 GHz</p></td>
<td><p>662.4 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>16 FLOPS/Clock × 2.3 GHz × 18コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Xeon<br />
(<a href="https://ja.wikipedia.org/wiki/Broadwellマイクロアーキテクチャ" title="wikilink">Broadwell</a>)</p></td>
<td><p>24コア</p></td>
<td><p>2.2 GHz(ベース)<br />
3.4 GHz(ターボ)</p></td>
<td><p>0.845 TFLOPS(ベース)<br />
1.306 TFLOPS(ターボ)</p></td>
<td><p>理論値</p></td>
<td><p>16 FLOPS/Clock × 3.4 GHz × 24コア</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Xeon_Phi" title="wikilink">Xeon Phi</a><br />
(Knights Corner)</p></td>
<td><p>61コア</p></td>
<td><p>1.238 GHz(ベース)<br />
1.33 GHz(ターボ)</p></td>
<td><p>1.208 TFLOPS(ベース)<br />
1.298 TFLOPS(ターボ)</p></td>
<td><p>理論値</p></td>
<td><p>16 FLOPS/Clock × 1.33 GHz × 61コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Xeon_Phi" title="wikilink">Xeon Phi</a><br />
(Knights Landing)</p></td>
<td><p>72コア</p></td>
<td><p>1.5 GHz(ベース)<br />
1.7 GHz(ターボ)</p></td>
<td><p>3.456 TFLOPS(ベース)<br />
3.917 TFLOPS(ターボ)</p></td>
<td><p>理論値</p></td>
<td><p>32 FLOPS/Clock × 1.7 GHz × 72コア</p></td>
<td></td>
</tr>
</tbody>
</table>

### PC/Server (AMD)

<table>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>コア数</p></th>
<th><p>クロック</p></th>
<th><p>FLOPS（倍精度）</p></th>
<th><p>理論値/実測値</p></th>
<th><p>理論値の計算式</p></th>
<th><p>参照</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/AMD_Phenom_II" title="wikilink">Phenom II</a><br />
(X4 980 Black Edition)</p></td>
<td><p>4コア</p></td>
<td><p>3.7GHz</p></td>
<td><p>59.2 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>4 FLOPS/Clock × 3.7GHz × 4コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/AMD_Phenom_II" title="wikilink">Phenom II</a><br />
(X6 1100T Black Edition)</p></td>
<td><p>6コア</p></td>
<td><p>3.3GHz</p></td>
<td><p>79.2 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>4 FLOPS/Clock × 3.3GHz × 6コア</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>AMD Fusion E Series<br />
(<a href="https://ja.wikipedia.org/wiki/Bobcat_(マイクロアーキテクチャ)" title="wikilink">Bobcat</a>)</p></td>
<td><p>2コア</p></td>
<td><p>1.65GHz</p></td>
<td><p>6.6 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>2 FLOPS/Clock × 1.65GHz × 2コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>AMD Opteron<br />
(<a href="https://ja.wikipedia.org/wiki/Opteron#Magny-Cours_.28K10.2C_rev_D1.29" title="wikilink">Magny-Cours</a>)</p></td>
<td><p>12コア</p></td>
<td><p>2.5GHz</p></td>
<td><p>120 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>4 FLOPS/Clock × 2.5GHz × 12コア</p></td>
<td><p>[18]</p></td>
</tr>
<tr class="odd">
<td><p>AMD FX<br />
(<a href="https://ja.wikipedia.org/wiki/Bulldozer_(マイクロアーキテクチャ)" title="wikilink">Bulldozer</a>)</p></td>
<td><p>8コア/4モジュール</p></td>
<td><p>3.9GHz</p></td>
<td><p>124.8 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>8 FLOPS/Clock × 3.9GHz × 4モジュール</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>AMD Opteron<br />
(<a href="https://ja.wikipedia.org/wiki/Opteron#Interlagos.2FValencia_.28Bulldozer.29" title="wikilink">Interlagos</a>)</p></td>
<td><p>16コア/8モジュール</p></td>
<td><p>3.1GHz</p></td>
<td><p>198.4 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>8 FLOPS/Clock × 3.1GHz × 8モジュール</p></td>
<td></td>
</tr>
</tbody>
</table>

Bulldozer は1モジュールにつき2つの128ビット積和演算器があり、倍精度は2つのFMA命令を同時実行することにより 8 FLOPS/Cycle。

### [ARM](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")

<table>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>コア数</p></th>
<th><p>クロック</p></th>
<th><p>FLOPS</p></th>
<th><p>理論値/実測値</p></th>
<th><p>理論値の計算式</p></th>
<th><p>参照</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ARM11</p></td>
<td><p>1コア</p></td>
<td><p>700MHz</p></td>
<td><p>単精度：700 MFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：1 FLOPS/Clock × 700MHz</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM Cortex-A8</p></td>
<td><p>1コア</p></td>
<td><p>1GHz</p></td>
<td><p>単精度：4 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：4 FLOPS/Clock × 1GHz</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM Cortex-A9</p></td>
<td><p>4コア</p></td>
<td><p>1.5GHz</p></td>
<td><p>単精度：24 GFLOPS<br />
倍精度：9 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：4 FLOPS/Clock × 1.5GHz × 4コア<br />
倍精度：1.5 FLOPS/Clock × 1.5GHz × 4コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM Cortex-A15</p></td>
<td><p>4コア</p></td>
<td><p>2.0GHz</p></td>
<td><p>単精度：64 GFLOPS<br />
倍精度：16 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：8 FLOPS/Clock × 2.0GHz × 4コア<br />
倍精度：2 FLOPS/Clock × 2.0GHz × 4コア</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM Cortex-A57</p></td>
<td><p>4コア</p></td>
<td><p>2.8GHz</p></td>
<td><p>単精度：89.6 GFLOPS<br />
倍精度：44.8 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：8 FLOPS/Clock × 2.8GHz × 4コア<br />
倍精度：4 FLOPS/Clock × 2.8GHz × 4コア</p></td>
<td></td>
</tr>
</tbody>
</table>

  - [NetWalker](https://ja.wikipedia.org/wiki/NetWalker "wikilink") PC-Z1: CPU 3.2GFLOPS(ARM Cortex-A8 800MHz,SIMD), 0.64GFLOPS(同VFP)

ARM NEON はCortex-A15までは倍精度が扱えなく、単精度のみ\[19\]。ARM NEON は 128ビット幅で単精度だと 4 FLOPS/Cycle だが、Cortex-A15 は FMA があるので 8 FLOPS/Cycle。

倍精度は、Cortex-A9 は VFPv3 により、2 cycle で足し算2回、乗算1回、合計3演算できるので、1.5 FLOPS/Cycle。Cortex-A15 は VFPv4 により、1 cycle で1回 FMA が計算できるので、2 FLOPS/Cycle。Cortex-A57より、NEONでも倍精度が扱えるようになる。

### ゲーム機

  - [ゲームキューブ](../Page/ニンテンドーゲームキューブ.md "wikilink"): 13GFLOPS （ピーク時/システム全体）\[20\]
  - [ドリームキャスト](../Page/ドリームキャスト.md "wikilink"): 1.4GFLOPS
  - [Xbox](../Page/Xbox_\(ゲーム機\).md "wikilink"): 1.5GFLOPS
  - [Xbox 360](https://ja.wikipedia.org/wiki/Xbox_360 "wikilink"): 115.2GFLOPS（[Xenon](https://ja.wikipedia.org/wiki/Xenon "wikilink")(マイクロプロセッサ)単体）\[21\]、240GFLOPS（[Xenos GPU単体](https://ja.wikipedia.org/wiki/Xbox_360#GPU "wikilink")）\[22\]、1TFLOPS （システム全体）:但し詳しい内訳は不明\[23\]
  - [PlayStation Portable](https://ja.wikipedia.org/wiki/PlayStation_Portable "wikilink"): CPU 2.6GFLOPS / 9.6GFLOPS（ピーク時/システム全体）
  - [PlayStation 2](https://ja.wikipedia.org/wiki/PlayStation_2 "wikilink"): 6.2GFLOPS（[Emotion Engine単体](https://ja.wikipedia.org/wiki/Emotion_Engine "wikilink")）\[24\]
  - [PlayStation 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink"): 218GFLOPS（[Cell Broadband Engine単体](https://ja.wikipedia.org/wiki/Cell_Broadband_Engine "wikilink")）\[25\]、224GFLOPS （[RSX単体](https://ja.wikipedia.org/wiki/PlayStation_3#仕様 "wikilink")）\[26\]、2TFLOPS （システム全体）:但し詳しい内訳は不明\[27\]
  - [PlayStation 4](https://ja.wikipedia.org/wiki/PlayStation_4 "wikilink"): 1.84TFLOPS（GPU単体）\[28\]

### スーパーコンピュータ

<table>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>FLOPS</p></th>
<th><p>理論値/実測値</p></th>
<th><p>システム概要</p></th>
<th><p>参照</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/ENIAC" title="wikilink">ENIAC</a></p></td>
<td><p>300FLOPS</p></td>
<td></td>
<td><p>1946年完成</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/CRAY-1" title="wikilink">CRAY-1</a></p></td>
<td><p>160MFLOPS</p></td>
<td><p>倍精度, 理論ピーク性能値</p></td>
<td><p>1976年初号機納入</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/ディープ・ブルー_(コンピュータ)" title="wikilink">ディープ・ブルー</a></p></td>
<td><p>11.38GFLOPS</p></td>
<td></td>
<td><p>1989年開発開始、1997年チェス世界チャンピオンと対戦し、勝利</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/地球シミュレータ.md" title="wikilink">地球シミュレータ</a><br />
（第1世代）</p></td>
<td><p>35.86TFLOPS</p></td>
<td><p>倍精度, LINPACK実測値</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/TOP500" title="wikilink">TOP500</a> Jun 2002 1位</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/TSUBAME" title="wikilink">TSUBAME</a> 1.2</p></td>
<td><p>87.01TFLOPS</p></td>
<td><p>倍精度, LINPACK実測値</p></td>
<td><p>TOP500 Jun 2009 41位</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/T2Kオープンスパコン" title="wikilink">T2Kオープンスパコン</a></p></td>
<td><p>101.74TFLOPS</p></td>
<td><p>倍精度, LINPACK実測値</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>地球シミュレータ<br />
（第2世代）</p></td>
<td><p>122.4TFLOPS</p></td>
<td></td>
<td><p>TOP500 Jun 2009 16位</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GPUクラスタ<br />
（<a href="https://ja.wikipedia.org/wiki/長崎大学" title="wikilink">長崎大学</a>、<a href="https://ja.wikipedia.org/wiki/濱田剛" title="wikilink">濱田剛</a>ら）</p></td>
<td><p>158TFLOPS</p></td>
<td></td>
<td></td>
<td><p>[29]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Blue_Gene" title="wikilink">Blue Gene/L</a></p></td>
<td><p>478.2TFLOPS</p></td>
<td></td>
<td><p>TOP500 Nov 2007 1位</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Roadrunner" title="wikilink">IBM Roadrunner</a></p></td>
<td><p>1.105PFLOPS</p></td>
<td><p>倍精度, LINPACK実測値</p></td>
<td><p>TOP500 Jun 2008 1位</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/TSUBAME" title="wikilink">TSUBAME</a> 2.0</p></td>
<td><p>1.192PFLOPS</p></td>
<td><p>倍精度, LINPACK実測値</p></td>
<td><p>TOP500 Nov 2011 4位<br />
Xeon + NVIDIA Tesla</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/天河一号" title="wikilink">天河一号</a>A</p></td>
<td><p>2.566PFLOPS</p></td>
<td><p>倍精度, LINPACK実測値</p></td>
<td><p>TOP500 Nov 2010 1位<br />
理論値 4.701 PFLOPS。実行効率 54.6%<br />
Xeon + NVIDIA Tesla</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/TSUBAME" title="wikilink">TSUBAME</a> 2.5</p></td>
<td><p>2.843PFLOPS</p></td>
<td><p>倍精度, LINPACK実測値</p></td>
<td><p>TOP500 Nov 2013 11位 , <a href="https://ja.wikipedia.org/wiki/Green500" title="wikilink">Green500</a> 6位<br />
理論値 5.609 PFLOPS。実行効率 50.7%<br />
Xeon + NVIDIA Tesla</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/京_(スーパーコンピュータ)" title="wikilink">京</a></p></td>
<td><p>10.510PFLOPS</p></td>
<td><p>倍精度, LINPACK実測値</p></td>
<td><p>TOP500 Jun 2011 1位 実行効率 93.2%[30] - CPU数88,128個, 理論値 11,280,384 GFLOPS (=128 GFLOPS×88,128)</p></td>
<td><p>[31][32]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/IBM_Sequoia" title="wikilink">IBM Sequoia</a></p></td>
<td><p>17.172PFLOPS</p></td>
<td><p>倍精度, LINPACK実測値</p></td>
<td><p>TOP500 Nov 2012 1位<br />
理論値 20.133 PFLOPS。実行効率 85.3%<br />
PowerPC A2</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/天河二号" title="wikilink">天河二号</a></p></td>
<td><p>61.445PFLOPS</p></td>
<td><p>倍精度, LINPACK実測値</p></td>
<td><p>TOP500 Jun 2013 1位<br />
理論値 100.679 PFLOPS。実行効率 61.0%<br />
Xeon E5-2692v2 + Xeon Phi 31S1P</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/神威・太湖之光" title="wikilink">神威太湖之光</a></p></td>
<td><p>93.01PFLOPS</p></td>
<td></td>
<td><p>TOP500 Jun 2016 1位<br />
理論値 125.436 PFLOPS。実行効率 74.1%<br />
SW26010, Sunway</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Summit_(スーパーコンピュータ)" title="wikilink">Summit</a></p></td>
<td><p>143.5PFLOPS</p></td>
<td></td>
<td><p>TOP500 Jun 2018 1位<br />
理論値 200.795 PFLOPS。実行効率 71.4%<br />
Power9 22C, Mellanox dual-rail EDR InfiniBand</p></td>
<td></td>
</tr>
</tbody>
</table>

### [分散コンピューティング](../Page/分散コンピューティング.md "wikilink")

<table>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>FLOPS</p></th>
<th><p>日付</p></th>
<th><p>参加台数</p></th>
<th><p>Active率</p></th>
<th><p>参照</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Berkeley_Open_Infrastructure_for_Network_Computing" title="wikilink">BOINC</a></p></td>
<td><p>2,958.992TFLOPS</p></td>
<td><p>2009年12月6日</p></td>
<td></td>
<td></td>
<td><p>[33]</p></td>
</tr>
<tr class="even">
<td><p>8,563.365TFLOPS</p></td>
<td><p>2013年12月26日</p></td>
<td><p>986,613台</p></td>
<td><p>8.51%</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>161,081.587TFLOPS</p></td>
<td><p>2015年2月3日</p></td>
<td><p>376,688台</p></td>
<td><p>3.54%</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>160,760.027TFLOPS</p></td>
<td><p>2017年3月14日</p></td>
<td><p>739,507台</p></td>
<td><p>4.79%</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/SETI@home" title="wikilink">SETI@home</a><br />
(BOINCに含む)</p></td>
<td><p>658.210TFLOPS</p></td>
<td><p>2013年12月26日</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>731.599TFLOPS</p></td>
<td><p>2009年12月6日</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/United_Devices" title="wikilink">UD Agent</a></p></td>
<td><p>65TFLOPS</p></td>
<td><p>2001年10月01日</p></td>
<td><p>約96万台</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Folding@Home" title="wikilink">Folding@Home</a></p></td>
<td><p>約4,273TFLOPS</p></td>
<td><p>2008年11月22日</p></td>
<td><p>Active 353,966 CPU<br />
(参加約355万台)</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5.427PFLOPS</p></td>
<td><p>2012年03月23日</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### [グラフィックスカード](https://ja.wikipedia.org/wiki/グラフィックスカード "wikilink")

単精度の積和算を 2 FLOPS/Clock で行える。

#### NVIDIA

  - [GeForce 8600 GTS](https://ja.wikipedia.org/wiki/NVIDIA_GeForce#GeForce_8600_Series "wikilink"): 92.8GFLOPS / 139GFLOPS（積和算 / 積和算、積算合計）
  - [GeForce 8800 GT](https://ja.wikipedia.org/wiki/NVIDIA_GeForce#GeForce_8800_Series "wikilink"): 336GFLOPS / 504GFLOPS（積和算 / 積和算、積算合計）
  - [GeForce 9600 GT](https://ja.wikipedia.org/wiki/NVIDIA_GeForce#GeForce_9600_Series "wikilink"): 208GFLOPS / 312GFLOPS（積和算 / 積和算、積算合計）
  - [GeForce 9800 GTX+](https://ja.wikipedia.org/wiki/NVIDIA_GeForce#GeForce_9800_Series "wikilink"): 470GFLOPS / 705GFLOPS（積和算 / 積和算、積算合計）
  - [GeForce GTX 280](https://ja.wikipedia.org/wiki/NVIDIA_GeForce#GeForce_GTX_Series "wikilink"): 622GFLOPS / 933GFLOPS（積和算 / 積和算、積算合計）\[34\]\[35\]

<table>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>コア数</p></th>
<th><p>クロック</p></th>
<th><p>FLOPS</p></th>
<th><p>理論値/実測値</p></th>
<th><p>理論値の計算式</p></th>
<th><p>参照</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GeForce GTX 480</p></td>
<td><p>480</p></td>
<td><p>1401 MHz</p></td>
<td><p>単精度：1.345 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 1401 MHz × 480コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 580</p></td>
<td><p>512</p></td>
<td><p>1544 MHz</p></td>
<td><p>単精度：1.581 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 1544 MHz × 512コア</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 590<br />
(2GPU合計)</p></td>
<td><p>1024</p></td>
<td><p>1214 MHz</p></td>
<td><p>単精度：2.488 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 1214 MHz × 1024コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 680</p></td>
<td><p>1536</p></td>
<td><p>1006 MHz</p></td>
<td><p>単精度：3.090 TFLOPS<br />
倍精度：129 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 1006 MHz × 1536コア<br />
倍精度：1/12 FLOPS/Clock × 1006 MHz × 1536コア</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 690<br />
(2GPU合計)</p></td>
<td><p>3072</p></td>
<td><p>915 MHz</p></td>
<td><p>単精度：5.621 TFLOPS<br />
倍精度：234 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 915 MHz × 3072コア<br />
倍精度：1/12 FLOPS/Clock × 915 MHz × 3072コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 780 Ti<br />
Special Black Edition</p></td>
<td><p>2880</p></td>
<td><p>1000 MHz</p></td>
<td><p>単精度：5.76 TFLOPS<br />
倍精度：240 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 1000 MHz × 2880コア<br />
倍精度：1/12 FLOPS/Clock × 1000 MHz × 2880コア</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX TITAN X</p></td>
<td><p>3072</p></td>
<td><p>1000 MHz</p></td>
<td><p>単精度：6.144 TFLOPS<br />
倍精度：192 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 1000 MHz × 3072コア<br />
倍精度：1/16 FLOPS/Clock × 1000MHz × 3072コア</p></td>
<td><p>[36]</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX TITAN Z<br />
(2GPU合計)</p></td>
<td><p>5760</p></td>
<td><p>705 MHz</p></td>
<td><p>単精度：8.12 TFLOPS<br />
倍精度：2.71 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 705 MHz × 5760コア<br />
倍精度：2/3 FLOPS/Clock × 705 MHz × 5760コア</p></td>
<td><p>[37]</p></td>
</tr>
<tr class="odd">
<td><p>GeForce GTX 980</p></td>
<td><p>2048</p></td>
<td><p>1126 MHz</p></td>
<td><p>単精度：4.612 TFLOPS<br />
倍精度：144 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 1126 MHz × 2048コア<br />
倍精度：1/16 FLOPS/Clock × 1126 MHz × 2048コア</p></td>
<td><p>[38]</p></td>
</tr>
<tr class="even">
<td><p>GeForce GTX 1080</p></td>
<td><p>2560</p></td>
<td><p>1733 MHz</p></td>
<td><p>単精度：8.872 TFLOPS<br />
倍精度：138 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 1733 MHz × 2560コア<br />
倍精度：1/32 FLOPS/Clock × 1733 MHz × 2560コア</p></td>
<td><p>[39]</p></td>
</tr>
</tbody>
</table>

#### AMD

<table>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>コア数</p></th>
<th><p>クロック</p></th>
<th><p>FLOPS</p></th>
<th><p>理論値/実測値</p></th>
<th><p>理論値の計算式</p></th>
<th><p>参照</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Radeon HD 3650</p></td>
<td><p>120</p></td>
<td><p>725MHz</p></td>
<td><p>単精度：174 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 725MHz × 120コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Radeon HD 3870</p></td>
<td><p>320</p></td>
<td><p>825MHz</p></td>
<td><p>単精度：496 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 825MHz × 320コア</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Radeon HD 4670</p></td>
<td><p>320</p></td>
<td><p>750MHz</p></td>
<td><p>単精度：480 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 750MHz × 320コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Radeon HD 4870</p></td>
<td><p>800</p></td>
<td><p>750MHz</p></td>
<td><p>単精度：1.2 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 750MHz × 800コア</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Radeon HD 5870</p></td>
<td><p>1600</p></td>
<td><p>850MHz</p></td>
<td><p>単精度：2.72 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 850MHz × 1600コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Radeon HD 5970<br />
(2GPU合計)</p></td>
<td><p>3200</p></td>
<td><p>725MHz</p></td>
<td><p>単精度：4.64 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 725MHz × 3200コア</p></td>
<td><p>[40]</p></td>
</tr>
<tr class="odd">
<td><p>Radeon HD 6970</p></td>
<td><p>1536</p></td>
<td><p>880MHz</p></td>
<td><p>単精度：2.703 TFLOPS<br />
倍精度：0.676 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 880MHz × 1536コア<br />
倍精度：0.5 FLOPS/Clock × 880MHz × 1536コア</p></td>
<td><p>[41]</p></td>
</tr>
<tr class="even">
<td><p>Radeon HD 6990<br />
(2GPU合計)</p></td>
<td><p>3072</p></td>
<td><p>830 MHz</p></td>
<td><p>単精度：5.1 TFLOPS<br />
倍精度：1.275 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 830 MHz × 3072コア<br />
倍精度：0.5 FLOPS/Clock × 830MHz × 3072コア</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Radeon HD 7970<br />
GHz Edition</p></td>
<td><p>2048</p></td>
<td><p>1.05 GHz</p></td>
<td><p>単精度：4.301 TFLOPS<br />
倍精度：1.075 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 1.05 GHz × 2048コア<br />
倍精度：0.5 FLOPS/Clock × 1.05 GHz × 2048コア</p></td>
<td><p>[42][43]</p></td>
</tr>
<tr class="even">
<td><p>Radeon HD 7990<br />
(2GPU合計)</p></td>
<td><p>4096</p></td>
<td><p>1.0 GHz</p></td>
<td><p>単精度：8.192 TFLOPS<br />
倍精度：2.048 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 1.0 GHz × 4096コア<br />
倍精度：0.5 FLOPS/Clock × 1.0 GHz × 4096コア</p></td>
<td><p>[44]</p></td>
</tr>
<tr class="odd">
<td><p>Radeon R9 290X</p></td>
<td><p>2816</p></td>
<td><p>1.0 GHz</p></td>
<td><p>単精度：5.632 TFLOPS<br />
倍精度：1.408 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 1.0 GHz × 2816コア<br />
倍精度：0.5 FLOPS/Clock × 1.0 GHz × 2816コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Radeon R9 295X2<br />
(2GPU合計)</p></td>
<td><p>5632</p></td>
<td><p>1.018 GHz</p></td>
<td><p>単精度：11.467 TFLOPS<br />
倍精度：2.867 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 1.018 GHz × 5632コア<br />
倍精度：0.5 FLOPS/Clock × 1.018 GHz × 5632コア</p></td>
<td></td>
</tr>
</tbody>
</table>

ハイエンドでは倍精度(fp64)は 0.5 FLOPS/Cycle であるが、ミドルレンジ以下は 0.125 FLOPS/Cycle\[45\] であったり、倍精度の計算が出来なかったりする。

#### Intel

<table>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/実行ユニット" title="wikilink">EU数</a></p></th>
<th><p>クロック</p></th>
<th><p>FLOPS</p></th>
<th><p>理論値/実測値</p></th>
<th><p>理論値の計算式</p></th>
<th><p>参照</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Intel_GMA" title="wikilink">Intel GMA</a> X4500</p></td>
<td><p>10</p></td>
<td><p>800MHz</p></td>
<td><p>単精度：32 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：4 FLOPS/Clock × 10EU × 800MHz</p></td>
<td><p>[46]</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Intel_HD_Graphics" title="wikilink">Intel HD Graphics</a> (Clarkdale)</p></td>
<td><p>12</p></td>
<td><p>900MHz</p></td>
<td><p>単精度：43.2 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：4 FLOPS/Clock × 12EU × 900MHz</p></td>
<td><p>[47]</p></td>
</tr>
<tr class="odd">
<td><p>Intel HD Graphics 3000</p></td>
<td><p>12</p></td>
<td><p>1.35GHz (Max)</p></td>
<td><p>単精度：129.6 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：8 FLOPS/Clock × 12EU × 1.35GHz</p></td>
<td><p>[48]</p></td>
</tr>
<tr class="even">
<td><p>Intel HD Graphics 4000</p></td>
<td><p>16</p></td>
<td><p>1.35GHz (Max)</p></td>
<td><p>単精度：345.6 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：16 FLOPS/Clock × 16EU × 1.35GHz</p></td>
<td><p>[49]</p></td>
</tr>
<tr class="odd">
<td><p>Intel HD Graphics (<a href="https://ja.wikipedia.org/wiki/Haswellマイクロアーキテクチャ" title="wikilink">Haswell</a>)</p></td>
<td><p>10</p></td>
<td><p>1.2GHz (Max)</p></td>
<td><p>単精度：192 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：16 FLOPS/Clock × 10EU × 1.2GHz</p></td>
<td><p>[50]</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Intel_HD_Graphics" title="wikilink">Intel Iris Pro Graphics</a> 5200</p></td>
<td><p>40</p></td>
<td><p>1.3GHz (Max)</p></td>
<td><p>単精度：832 GFLOPS<br />
倍精度：208 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：16 FLOPS/Clock × 40EU × 1.3GHz<br />
倍精度：4 FLOPS/Clock × 40EU × 1.3GHz</p></td>
<td><p>[51]</p></td>
</tr>
<tr class="odd">
<td><p>Iris Pro Graphics 6200</p></td>
<td><p>48</p></td>
<td><p>1.15GHz (Max)</p></td>
<td><p>単精度：883 GFLOPS<br />
倍精度：220.8 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：16 FLOPS/Clock × 48EU × 1.15GHz<br />
倍精度：4 FLOPS/Clock × 48EU × 1.15GHz</p></td>
<td><p>[52]</p></td>
</tr>
<tr class="even">
<td><p>Intel HD Graphics 530<br />
(<a href="https://ja.wikipedia.org/wiki/Skylakeマイクロアーキテクチャ" title="wikilink">Skylake</a>)</p></td>
<td><p>24</p></td>
<td><p>1.15GHz (Max)</p></td>
<td><p>単精度：441.6 GFLOPS<br />
倍精度：110.4 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：16 FLOPS/Clock × 24EU × 1.15GHz<br />
倍精度：4 FLOPS/Clock × 24EU × 1.15GHz</p></td>
<td><p>[53]</p></td>
</tr>
</tbody>
</table>

HD Graphicsの各EUは4-way SIMDの演算器を備えており、1命令で4並列の単精度浮動小数点演算が可能である。Sandy Bridgeより前の世代では1クロックでEUあたり1つの加算もしくは乗算命令を実行可能で、4FLOPS/EU。Sandy Bridge世代では1クロックでEUあたり1つのFMA命令を実行可能で、8FLOPS/EU。Ivy Bridge世代以降は1クロックでEUあたり2つのFMA命令を実行可能で、16FLOPS/EUとなる。

#### Qualcomm [Snapdragon](https://ja.wikipedia.org/wiki/Snapdragon "wikilink")

<table>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>ALU数</p></th>
<th><p>クロック</p></th>
<th><p>FLOPS（単精度）</p></th>
<th><p>理論値/実測値</p></th>
<th><p>理論値の計算式</p></th>
<th><p>参照</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Adreno" title="wikilink">Adreno</a> 200</p></td>
<td><p>8</p></td>
<td><p>245MHz</p></td>
<td><p>3.92 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>2 FLOPS/ALU × 245MHz × 8ALU</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Adreno 203<br />
Adreno 205</p></td>
<td><p>16</p></td>
<td><p>245MHz</p></td>
<td><p>7.84 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>2 FLOPS/ALU × 245MHz × 16ALU</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Adreno 220</p></td>
<td><p>32</p></td>
<td><p>266MHz</p></td>
<td><p>17.0 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>2 FLOPS/ALU × 266MHz × 32ALU</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Adreno 225</p></td>
<td><p>32</p></td>
<td><p>400MHz</p></td>
<td><p>25.6 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>2 FLOPS/ALU × 400MHz × 32ALU</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Adreno 320<br />
(Snapdragon S4 Pro)</p></td>
<td><p>64</p></td>
<td><p>400MHz</p></td>
<td><p>57 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>2.25 FLOPS/ALU × 400MHz × 64ALU</p></td>
<td><p>[54]</p></td>
</tr>
<tr class="even">
<td><p>Adreno 320<br />
(Snapdragon 600)</p></td>
<td><p>96</p></td>
<td><p>400MHz</p></td>
<td><p>86.4 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>2.25 FLOPS/ALU × 400MHz × 96ALU</p></td>
<td><p>[55]</p></td>
</tr>
<tr class="odd">
<td><p>Adreno 330<br />
(Snapdragon 800)</p></td>
<td><p>128</p></td>
<td><p>450MHz</p></td>
<td><p>129.6 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>2.25 FLOPS/ALU × 450MHz × 128ALU</p></td>
<td><p>[56]</p></td>
</tr>
<tr class="even">
<td><p>Adreno 430<br />
(Snapdragon 810)</p></td>
<td><p>288</p></td>
<td><p>500MHz</p></td>
<td><p>324 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>2.25 FLOPS/ALU × 500MHz × 288ALU</p></td>
<td></td>
</tr>
</tbody>
</table>

#### Apple (iPhone & iPad)

<table>
<thead>
<tr class="header">
<th><p>チップセット</p></th>
<th><p>GPU コア / クラスタ</p></th>
<th><p>GPU MHz</p></th>
<th><p>FLOPS</p></th>
<th><p>デバイス</p></th>
<th><p>GPU モデルと理論値の計算式</p></th>
<th><p>参照</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Apple A4</p></td>
<td><center>
<p>1 Core</p>
</center></td>
<td><center>
<p>200MHz</p>
</center></td>
<td><center>
<p>1.6 GFLOPS</p>
</center></td>
<td><center>
<p>iPhone 4</p>
</center></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PowerVR" title="wikilink">PowerVR</a> SGX535 @ 200 MHz (2vec4) 4 x 2 х 0.200 = 1.6 GFLOPS</p></td>
<td><p>[57]</p></td>
</tr>
<tr class="even">
<td><center>
<p>250MHz</p>
</center></td>
<td><center>
<p>2 GFLOPS</p>
</center></td>
<td><center>
<p>iPad</p>
</center></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PowerVR" title="wikilink">PowerVR</a> SGX535 @ 250 MHz (2vec4) 4 x 2 х 0.250 = 2 GFLOPS</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Apple A5</p></td>
<td><center>
<p>2 Cores</p>
</center></td>
<td><center>
<p>200MHz</p>
</center></td>
<td><center>
<p>14.4 GFLOPS</p>
</center></td>
<td><center>
<p>iPhone 4S</p>
</center></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PowerVR" title="wikilink">PowerVR</a> SGX543MP2 (dual-core) @ 250 MHz 2vec4 + 1 scalar: 4х2+1=9 * 8 х 0.200 х 9 = 14.4 GFLOPS</p></td>
<td><p>[58]</p></td>
</tr>
<tr class="even">
<td><center>
<p>250MHz</p>
</center></td>
<td><center>
<p>18 GFLOPS</p>
</center></td>
<td><center>
<p>iPad 2</p>
</center></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PowerVR" title="wikilink">PowerVR</a> SGX543MP2 (dual-core) @ 200 MHz 2vec4 + 1 scalar: 4х2+1=9 * 8 х 0.200 х 9 = 18 GFLOPS</p></td>
<td><p>[59]</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Apple A5X</p></td>
<td><center>
<p>4 Cores</p>
</center></td>
<td><center>
<p>250MHz</p>
</center></td>
<td><center>
<p>36 GFLOPS</p>
</center></td>
<td><center>
<p>iPad 3</p>
</center></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PowerVR" title="wikilink">PowerVR</a> SGX543MP4 (quad-core) @ 250 MHz 2vec4 + 1 scalar: 4х2+1=9 * 16 х 0.250 х 9 = 36 GFLOPS</p></td>
<td><p>[60]</p></td>
</tr>
<tr class="even">
<td><p>Apple A6</p></td>
<td><center>
<p>3 Cores</p>
</center></td>
<td><center>
<p>250MHz</p>
</center></td>
<td><center>
<p>27 GFLOPS</p>
</center></td>
<td><center>
<p>iPhone 5</p>
</center></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PowerVR" title="wikilink">PowerVR</a> SGX543MP3 (tri-core) @ 250 MHz 2vec4 + 1 scalar: 4х2+1=9 * 12 х 0.250 х 9 = 27 GFLOPS</p></td>
<td><p>[61]</p></td>
</tr>
<tr class="odd">
<td><p>Apple A6X</p></td>
<td><center>
<p>4 Cores</p>
</center></td>
<td><center>
<p>280MHz</p>
</center></td>
<td><center>
<p>80 GFLOPS</p>
</center></td>
<td><center>
<p>iPad 4</p>
</center></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PowerVR" title="wikilink">PowerVR</a> SGX554MP4 (quad-core) @ 280 MHz 2vec4 + 1 scalar: 4х2+1=9 * 32 х 0.280 х 9 = 80 GFLOPS</p></td>
<td><p>[62]</p></td>
</tr>
<tr class="even">
<td><p>Apple A7</p></td>
<td><center>
<p>4 Clusters</p>
</center></td>
<td><center>
<p>450MHz</p>
</center></td>
<td><center>
<p>115.2 GFLOPS</p>
</center></td>
<td><center>
<p>iPhone 5S</p>
</center></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PowerVR" title="wikilink">PowerVR</a> G6430 (quad-clusters) @ 450 MHz 64 USC x 4 Clusters x 0.450 = 115.2 GFLOPS</p></td>
<td><p>[63]</p></td>
</tr>
<tr class="odd">
<td><center>
<p>533MHz</p>
</center></td>
<td><center>
<p>136.4 GFLOPS</p>
</center></td>
<td><center>
<p>iPad Air</p>
</center></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PowerVR" title="wikilink">PowerVR</a> G6430 (quad-clusters) @ 533 MHz 64 USC x 4 Clusters x 0.533 = 136.4 GFLOPS</p></td>
<td><p>[64]</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Apple A8</p></td>
<td><center>
<p>4 Clusters</p>
</center></td>
<td><center>
<p>450MHz</p>
</center></td>
<td><center>
<p>115.2 GFLOPS</p>
</center></td>
<td><center>
<p>iPhone 6</p>
</center></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PowerVR" title="wikilink">PowerVR</a> G6450 (quad-clusters) @ 450 MHz 64 USC x 4 Clusters x 0.450 = 115.2 GFLOPS</p></td>
<td><p>[65]</p></td>
</tr>
<tr class="odd">
<td><p>Apple A8X</p></td>
<td><center>
<p>8 Clusters</p>
</center></td>
<td><center>
<p>450MHz</p>
</center></td>
<td><center>
<p>230.4 GFLOPS</p>
</center></td>
<td><center>
<p>iPad Air 2</p>
</center></td>
<td><p><a href="https://ja.wikipedia.org/wiki/PowerVR" title="wikilink">PowerVR</a> GXA6850 @ 450 MHz 64 USC x 8 Clusters x 0.450 = 230.4 GFLOPS</p></td>
<td><p>[66][67]</p></td>
</tr>
</tbody>
</table>

#### Texas Instruments OMAP

| 名称              | コア数 | クロック   | FLOPS（単精度） | 理論値/実測値 | 理論値の計算式                   | 参照 |
| --------------- | --- | ------ | ---------- | ------- | ------------------------- | -- |
| PowerVR SGX 540 | 4   | 384MHz | 6.1 GFLOPS | 理論値     | 4 FLOPS/コア × 384MHz × 4コア |    |

#### NVIDIA Tegra

| 名称       | ALU数 | クロック    | FLOPS（単精度）    | 理論値/実測値 | 理論値の計算式                       | 参照           |
| -------- | ---- | ------- | ------------- | ------- | ----------------------------- | ------------ |
| Tegra 2  | 8    | 333MHz  | 5.6 GFLOPS    | 理論値     | 2 FLOPS/ALU × 333MHz × 8ALU   |              |
| Tegra 3  | 12   | 500MHz  | 12.48 GFLOPS  | 理論値     | 2 FLOPS/ALU × 520MHz × 12ALU  | \[68\]\[69\] |
| Tegra 4i | 60   | 660MHz  | 79.2 GFLOPS   | 理論値     | 2 FLOPS/ALU × 660MHz × 60ALU  | \[70\]       |
| Tegra 4  | 72   | 672MHz  | 96.768 GFLOPS | 理論値     | 2 FLOPS/ALU × 672MHz × 72ALU  | \[71\]       |
| Tegra K1 | 192  | 950MHz  | 365 GFLOPS    | 理論値     | 2 FLOPS/ALU × 950MHz × 192ALU |              |
| Tegra X1 | 256  | 1.0 GHz | 512 GFLOPS    | 理論値     | 2 FLOPS/ALU × 1.0GHz × 256ALU | \[72\]       |

#### Samsung [Exynos](https://ja.wikipedia.org/wiki/Exynos "wikilink")

| 名称                   | コア数 | クロック   | FLOPS（単精度）   | 理論値/実測値 | 理論値の計算式                                                                                         | 参照     |
| -------------------- | --- | ------ | ------------ | ------- | ----------------------------------------------------------------------------------------------- | ------ |
| Exynos 3             | 1   | 200MHz | 3.2 GFLOPS   | 理論値     | 16 FLOPS × 200MHz                                                                               |        |
| Exynos 4 Dual (45nm) | 4   | 266MHz | 9.6 GFLOPS   | 理論値     | 9 FLOPS/コア × 266MHz × 4コア                                                                       |        |
| Exynos 4 Dual (32nm) | 4   | 400MHz | 14.4 GFLOPS  | 理論値     | 9 FLOPS/コア × 400MHz × 4コア                                                                       |        |
| Exynos 4 Quad        | 4   | 440MHz | 15.84 GFLOPS | 理論値     | 9 FLOPS/コア × 440MHz × 4コア                                                                       |        |
| Exynos 5 Dual        | 4   | 533MHz | 72.5 GFLOPS  | 理論値     | Mali T604 MP4 (quad-core) @ 533MHz \* 16FP + 1 TMU = 17 x 2 ALU x 4 Core x 0.533= 72.488 GFLOPS | \[73\] |
| Exynos 5410 Octa     | 3   | 533MHz | 51.2 GFLOPS  | 理論値     | PowerVR SGX544MP3 (tri-core) @ 533MHz \* 2vec4=8 \* 12 х 0.533 х 8 = 51.2 GFLOPS                |        |
| Exynos 5420 Octa     | 6   | 533MHz | 102.4 GFLOPS | 理論値     | Mali T628 MP6 (six-core) @ 533MHz \* 16FP x 2 ALU x 6 Core x 0.533 = 102.4 GFLOPS               | \[74\] |

### GPUアクセラレーター

<table>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>コア数</p></th>
<th><p>クロック</p></th>
<th><p>FLOPS</p></th>
<th><p>理論値/実測値</p></th>
<th><p>理論値の計算式</p></th>
<th><p>参照</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/NVIDIA_Tesla" title="wikilink">NVIDIA Tesla</a> C870</p></td>
<td><p>128</p></td>
<td><p>1.35 GHz</p></td>
<td><p>単精度：345.6 GFLOPS<br />
倍精度：不可</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 1.35 GHz × 128コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>NVIDIA Tesla C1060</p></td>
<td><p>240</p></td>
<td><p>1.3 GHz</p></td>
<td><p>単精度：622 GFLOPS<br />
倍精度：78 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 1.3 GHz × 240コア<br />
倍精度：1/4 FLOPS/Clock × 1.3 GHz × 240コア</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>NVIDIA Tesla C2070</p></td>
<td><p>448</p></td>
<td><p>1.15 GHz</p></td>
<td><p>単精度：1.03 TFLOPS<br />
倍精度：0.515 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 1.15 GHz × 448コア<br />
倍精度：1 FLOPS/Clock × 1.15 GHz × 448コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>NVIDIA Tesla K10<br />
(2GPU合計)</p></td>
<td><p>3072</p></td>
<td><p>745 MHz</p></td>
<td><p>単精度：4.58 TFLOPS<br />
倍精度：0.19 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 745 MHz × 3072コア<br />
倍精度：1/12 FLOPS/Clock × 745 MHz × 3072コア</p></td>
<td><p>[75]</p></td>
</tr>
<tr class="odd">
<td><p>NVIDIA Tesla K20</p></td>
<td><p>2496</p></td>
<td><p>706 MHz</p></td>
<td><p>単精度：3.52 TFLOPS<br />
倍精度：1.17 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 706 MHz × 2496コア<br />
倍精度：2/3 FLOPS/Clock × 706 MHz × 2496コア</p></td>
<td><p>[76]</p></td>
</tr>
<tr class="even">
<td><p>NVIDIA Tesla K40</p></td>
<td><p>2880</p></td>
<td><p>745 MHz</p></td>
<td><p>単精度：4.29 TFLOPS<br />
倍精度：1.43 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 745 MHz × 2880コア<br />
倍精度：2/3 FLOPS/Clock × 745 MHz × 2880コア</p></td>
<td><p>[77]</p></td>
</tr>
<tr class="odd">
<td><p>NVIDIA Tesla K80<br />
(2GPU合計)</p></td>
<td><p>4992</p></td>
<td><p>562 MHz</p></td>
<td><p>単精度：5.61 TFLOPS<br />
倍精度：1.87 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>単精度：2 FLOPS/Clock × 562 MHz × 4992コア<br />
倍精度：2/3 FLOPS/Clock × 562 MHz × 4992コア</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/AMD_FirePro" title="wikilink">AMD FirePro</a> S9150</p></td>
<td><p>2816</p></td>
<td></td>
<td><p>単精度：5.07 TFLOPS<br />
倍精度：2.53 TFLOPS</p></td>
<td><p>理論値</p></td>
<td></td>
<td><p>[78]</p></td>
</tr>
<tr class="odd">
<td><p>AMD FirePro S9170</p></td>
<td><p>2816</p></td>
<td></td>
<td><p>単精度：5.24 TFLOPS<br />
倍精度：2.62 TFLOPS</p></td>
<td><p>理論値</p></td>
<td></td>
<td><p>[79]</p></td>
</tr>
</tbody>
</table>

### FPGA

<table>
<caption><a href="https://ja.wikipedia.org/wiki/アルテラ" title="wikilink">アルテラ</a></caption>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>クロック</p></th>
<th><p>FLOPS<br />
(単精度、積和算)</p></th>
<th><p>理論値/実測値</p></th>
<th><p>理論値の計算式</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Stratix IV</p></td>
<td><p>445 MHz</p></td>
<td><p>理論値 245 GFLOPS<br />
実測値 171 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>64x64の行列のかけ算1つで128個のDSPを消費し、24.45 GFLOPS。DSP は最大1288個なので、244.5 GFLOPS。FPGAでは整数の積和算は1クロックで計算できるが、GPUとは異なり浮動小数点のかけ算は 445MHz 動作で11クロック必要[80][81]。それに対して、GPUは1クロックで行える。</p></td>
</tr>
<tr class="even">
<td><p>Stratix V</p></td>
<td><p>388 MHz</p></td>
<td><p>1.568 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>2048 multiplier / 64 * 49 GFLOPS (388 MHz) = 1.568 TFLOPS[82]。単精度の乗算には 27x27 の multiplier が単精度浮動小数点数あたり 64 個必要。</p></td>
</tr>
<tr class="odd">
<td><p>Stratix 10</p></td>
<td><p>1 GHz</p></td>
<td><p>10 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>2 FLOPS * 5000 DSP * 1 GHz = 10 TFLOPS[83]。</p></td>
</tr>
</tbody>
</table>

<table>
<caption><a href="https://ja.wikipedia.org/wiki/ザイリンクス" title="wikilink">ザイリンクス</a></caption>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>クロック</p></th>
<th><p>FLOPS<br />
(単精度)</p></th>
<th><p>理論値/実測値</p></th>
<th><p>理論値の計算式</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Virtex-5 SX240T</p></td>
<td></td>
<td><p>162.52 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>[84][85]</p></td>
</tr>
<tr class="even">
<td><p>Virtex-6 SX475T</p></td>
<td></td>
<td><p>450 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>[86]</p></td>
</tr>
<tr class="odd">
<td><p>Virtex-7</p></td>
<td></td>
<td><p>833 GFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>[87]</p></td>
</tr>
<tr class="even">
<td><p>Virtex UltraScale</p></td>
<td></td>
<td><p>1.739 TFLOPS</p></td>
<td><p>理論値</p></td>
<td><p>[88]</p></td>
</tr>
</tbody>
</table>

## 脚注

<references/>

## 関連項目

  - [MIPS](https://ja.wikipedia.org/wiki/MIPS "wikilink")
  - [TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")

## 外部リンク

  - [TOP500 スーパーコンピュータランキング](http://www.top500.org/)
      - [TOP500 List 2014/11](http://www.top500.org/list/2014/11)

[Category:ベンチマーク](https://ja.wikipedia.org/wiki/Category:ベンチマーク "wikilink") [Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink")

1.  [【レポート】ポスト「京」コンピュータはどうなるのか (1) 次世代スパコンの開発開始で米国に遅れをとっている日本 | エンタープライズ | マイコミジャーナル](https://news.mynavi.jp/articles/2011/07/05/post_kcomputer/index.html)
2.  [スパコン世界ランク、米3連覇　日本は「ABCI」8位が最高](https://www.itmedia.co.jp/news/spv/1906/18/news057.html)
3.  [Intel® microprocessor export compliance metrics](http://www.intel.com/support/processors/sb/CS-028241.htm)
4.
5.
6.
7.
8.
9.
10.
11.
12.
13. [PetaFLOPS for the Common Man- Pt 3 In the next few yrs what could PetaFLOPS Systems Look Like - The Dell TechCenter](http://www.delltechcenter.com/page/PetaFLOPS+for+the+Common+Man-+Pt+3+In+the+next+few+yrs+what+could+PetaFLOPS+Systems+Look++Like)
14.
15. [Intel's Haswell Architecture Analyzed: Building a New PC and a New Intel](http://www.anandtech.com/show/6355/intels-haswell-architecture/8)
16. [IDF Beijingで公開されたHaswellの省電力&オーバークロック機能 - PC Watch](http://pc.watch.impress.co.jp/docs/column/kaigai/20130417_596202.html)
17. Agner Fog, [The microarchitecture of Intel, AMD and VIA CPUs](http://www.agner.org/optimize/)
18.
19. [5.5.2. NEON データ型および VFP データ型 - ARM](http://infocenter.arm.com/help/index.jsp?topic=/com.arm.doc.dui0204ij/CIHDIBDG.html)
20. [ATIのグラフィックスチップ技術が「Nintendo GAMECUBE」に採用（マイコミジャーナル）](https://news.mynavi.jp/news/2000/08/25/14.html)
21. <http://pc.watch.impress.co.jp/docs/2005/0514/kaigai178.htm>
22. <http://pc.watch.impress.co.jp/docs/2005/0701/kaigai195.htm>
23. [マイクロソフト、「Xbox 360」ハードウェア編 丸山嘉浩氏「日本で成功しなければ成功したと言えない」 GAME watch 2005/05/13](http://game.watch.impress.co.jp/docs/20050513/xbox2.htm)
24.
25. <http://pc.watch.impress.co.jp/docs/2005/0518/kaigai180.htm>
26. <http://www.4gamer.net/games/990/G999024/20130224001/>
27. [PlayStation.com(Japan)](http://www.jp.playstation.com/info/release/nr_20050517_ps3.html)
28.
29.
30. [【森山和道の「ヒトと機械の境界面」】 スパコン「京」を使う「次世代生命体統合シミュレーション」とは](http://pc.watch.impress.co.jp/docs/column/kyokai/20110627_456393.html)
31. [【レポート】「京」コンピュータが京速を達成 - Top500の首位堅持に期待 - エンタープライズ - マイコミジャーナル](https://news.mynavi.jp/articles/2011/11/03/kei_linpack/)
32. [「京」が第37回TOP500ランキングにおいて世界第一位を獲得！](http://www.nsc.riken.jp/K/diary.html)
33. [BOINC STATS - BOINC combined](http://boincstats.com/en/stats/-1/project/detail)
34. [ゲームを超えるミッションとは──NVIDIAが「GT200」にこめたGPUの可能性 (2/3) - ITmedia +D PC USER](http://plusd.itmedia.co.jp/pcuser/articles/0806/19/news047_2.html)
35. [GeForce GTX 200 GPU Technical Brief](http://www.nvidia.com/docs/IO/55506/GeForce_GTX_200_GPU_Technical_Brief.pdf)
36. [【レビュー】Maxwellのモンスター、「GeForce GTX TITAN X」をベンチマーク - PC Watch](http://pc.watch.impress.co.jp/docs/topic/review/20150318_693058.html)
37. [2999ドルの超弩級グラフィックボード『GeForce GTX TITAN Z』登場 - 週アスPLUS](http://weekly.ascii.jp/elem/000/000/209/209686/)
38. [【後藤弘茂のWeekly海外ニュース】高い電力性能比を実現した「Geforce GTX 980」の秘密 - PC Watch](http://pc.watch.impress.co.jp/docs/column/kaigai/20140919_667569.html)
39. <http://www.4gamer.net/games/251/G025177/20160516073/>
40.
41.
42. [GPUアーキテクチャ刷新のサイクル変化が産んだ「Radeon HD 7990」](http://pc.watch.impress.co.jp/docs/column/kaigai/20130424_597160.html)
43. [AMD Radeon HD 7970 GHz Edition Review: Battling For The Performance Crown](http://www.anandtech.com/show/6025/radeon-hd-7970-ghz-edition-review-catching-up-to-gtx-680)
44.
45. [AMD’s Annual GPU Rebadge: Radeon HD 8000 Series for OEMs](http://www.anandtech.com/show/6570/amds-annual-gpu-rebadge-radeon-hd-8000-series-for-oems)
46.
47.
48. [Intel HD Graphics DirectX Developer's Guide (Sandy Bridge)](https://software.intel.com/sites/default/files/m/d/4/1/d/8/Sandy_Bridge_Intel_HD_Graphics_DirectX_Developer_s_Guide_2dot9dot6.pdf) PDF
49.
50. [DirectX Developer’s Guide for Intel® Processor Graphics Maximizing Graphics Performance on 4th Generation Intel® Core™ Processors](https://software.intel.com/sites/default/files/4th_Generation_Core_Graphics_Developers_Guide_Final.pdf) PDF
51. [The Compute Architecture of Intel® Processor Graphics Gen7.5](https://software.intel.com/sites/default/files/managed/f3/13/Compute_Architecture_of_Intel_Processor_Graphics_Gen7dot5_Aug2014.pdf) PDF
52. [The Compute Architecture of Intel® Processor Graphics Gen8](https://software.intel.com/sites/default/files/Compute%20Architecture%20of%20Intel%20Processor%20Graphics%20Gen8.pdf) PDF
53. [The Compute Architecture of Intel® Processor Graphics Gen9](https://software.intel.com/sites/default/files/managed/c5/9a/The-Compute-Architecture-of-Intel-Processor-Graphics-Gen9-v1d0.pdf) PDF
54. [359gsm.com - Qualcomm Snapdragon 800 & Adreno 330](http://www.359gsm.com/forum/viewtopic.php?f=127&t=13152&start=0&st=0&sk=t&sd=a)
55. [359gsm.com - Qualcomm Snapdragon 800 & Adreno 330](http://www.359gsm.com/forum/viewtopic.php?f=127&t=13152&start=0&st=0&sk=t&sd=a)
56. [359gsm.com - Qualcomm Snapdragon 800 & Adreno 330](http://www.359gsm.com/forum/viewtopic.php?f=127&t=13152&start=0&st=0&sk=t&sd=a)
57. [AnandTech - The iPhone 5 Performance Preview](http://www.anandtech.com/show/6324/the-iphone-5-performance-preview)
58. [359gsm.com - Apple GPU GFLOPS PowerVR Series5 SGXMP](http://www.359gsm.com/forum/viewtopic.php?f=127&t=13396)
59. [359gsm.com - Apple GPU GFLOPS PowerVR Series5 SGXMP](http://www.359gsm.com/forum/viewtopic.php?f=127&t=13396)
60. [359gsm.com - Apple GPU GFLOPS PowerVR Series5 SGXMP](http://www.359gsm.com/forum/viewtopic.php?f=127&t=13396)
61. [359gsm.com - Apple GPU GFLOPS PowerVR Series5 SGXMP](http://www.359gsm.com/forum/viewtopic.php?f=127&t=13396)
62. [359gsm.com - Apple A6X & PowerVR SGX554](http://www.359gsm.com/forum/viewtopic.php?f=127&t=12844)
63. [359gsm.com - Apple A7 & PowerVR G6430](http://www.359gsm.com/forum/viewtopic.php?f=127&t=13972)
64. [359gsm.com - Apple A7 & PowerVR G6430](http://www.359gsm.com/forum/viewtopic.php?f=127&t=13972)
65. [Apple A8 SoC - NotebookCheck.net Tech](http://www.notebookcheck.net/Apple-A8-SoC.127992.0.html)
66. [AnandTech | Apple A8X’s GPU - GXA6850, Even Better Than I Thought](http://www.anandtech.com/show/8716/apple-a8xs-gpu-gxa6850-even-better-than-i-thought)
67. [Apple A8X iPad SoC - NotebookCheck.net Tech](http://www.notebookcheck.net/Apple-A8X-iPad-SoC.128403.0.html)
68. [AnandTech - Analysis of the new Apple iPad](http://www.anandtech.com/Show/Index/5663?cPage=5&all=False&sort=0&page=1&slug=analysis-of-the-new-apple-ipad)
69.
70. [【レポート】NVIDIA、Tegra 4の詳細をついに公開 - CPUだけでなくGPUも大規模アーキテクチャ変更と明らかに (3) より高性能な製造プロセスを利用するTegra 4i - パソコン - マイナビニュース](http://news.mynavi.jp/articles/2013/02/25/tegra4/002.html)
71. [【後藤弘茂のWeekly海外ニュース】NVIDIAがMWCに合わせて「Tegra 4/4i」の詳細を明らかに](http://pc.watch.impress.co.jp/docs/column/kaigai/20130225_589158.html)
72. [AnandTech | NVIDIA Tegra X1 Preview & Architecture Analysis](http://www.anandtech.com/show/8811/nvidia-tegra-x1-preview/2)
73. [Enjoy the Ultimate WQXGA Solution with Exynos 5 Dual](http://www.samsung.com/global/business/semiconductor/minisite/Exynos/data/Enjoy_the_Ultimate_WQXGA_Solution_with_Exynos_5_Dual_WP.pdf)
74. [359gsm.com - Samsung Exynos 5420 & ARM Mali T628 MP6](http://www.359gsm.com/forum/viewtopic.php?f=127&t=13942&p=27561#p27561)
75. [Tesla Kepler Family Product Overview - Nvidia](http://www.nvidia.co.jp/content/tesla/pdf/NVIDIA-Tesla-Kepler-Family-Datasheet.pdf)
76.
77.
78. [AMD claims supercomputing GPU performance crown with FirePro S9150](http://www.pcworld.com/article/2462240/amd-claims-supercomputing-gpu-performance-crown-with-firepro-s9150.html)
79. [AMD FirePro S9170 Server GPU](http://www.amd.com/en-us/products/graphics/server/s9170)
80. [アルテラ浮動小数点メガファンクション](http://www.altera.co.jp/products/ip/dsp/arithmetic/m-alt-float-point.html)
81. [浮動小数点メガファンクション ユーザーガイド](http://www.altera.co.jp/literature/ug/ug_altfp_mfug.pdf)
82. [Achieving One TeraFLOPS with 28nm FPGA](https://www.altera.com/content/dam/altera-www/global/zh_CN/pdfs/literature/wp/wp-01142-teraflops.pdf)
83. [ピーク浮動小数点性能の本質 - ALTERA](https://www.altera.co.jp/ja_JP/pdfs/literature/wp/wp-01222-understanding-peak-floating-point-performance-claims_j.pdf)
84.
85. [Revaluating FPGAs for 64-bit Floating-Point Calculations](http://www.hpcwire.com/hpcwire/2008-05-14/revaluating_fpgas_for_64-bit_floating-point_calculations.html)
86. [FPGAを用いた高性能コンピューティング](http://japan.xilinx.com/support/documentation/white_papers/j_wp375_HPC_Using_FPGAs.pdf)
87.
88. [DSP - Xilinx](http://japan.xilinx.com/products/technology/dsp.html)