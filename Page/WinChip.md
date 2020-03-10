> この記事は[WinChip](https://ja.wikipedia.org/wiki/WinChip)から翻訳されています。


**WinChip(**ウィンチップ)はかつて[IDT](https://ja.wikipedia.org/wiki/IDT "wikilink")社傘下であった[Centaur Technology社が開発した](https://ja.wikipedia.org/wiki/Centaur_Technology "wikilink")[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")[アーキテクチャの](../Page/コンピュータ・アーキテクチャ.md "wikilink")[CPU](../Page/CPU.md "wikilink")ブランドである。

製品化されたシリーズには WinChip C6、WinChip 2がある。その他WinChip 3、WinChip 4も計画されたが量産には至らなかった。

## 概要

外部とのインターフェースは[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")と同じ[Socket 7であり](https://ja.wikipedia.org/wiki/Socket_7 "wikilink")、[Cyrix](https://ja.wikipedia.org/wiki/Cyrix "wikilink") [6x86](https://ja.wikipedia.org/wiki/6x86 "wikilink")シリーズ、[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") [K5](https://ja.wikipedia.org/wiki/AMD_K5 "wikilink")/[K6シリーズに続く第](https://ja.wikipedia.org/wiki/AMD_K6 "wikilink")3のSocket7互換CPUと位置づけられる。先行2社がPentiumより高性能な（[Pentium IIに対抗しうる](../Page/Pentium_II.md "wikilink")）CPUを目指したのとは異なり、WinChipアーキテクチャはPentiumと同程度の性能を可能な限り低コストに実現することに重点が置かれている。 そのため、きわめてシンプルなアーキテクチャをとっており、Pentiumのような[スーパースカラ](https://ja.wikipedia.org/wiki/スーパースカラ "wikilink")アーキテクチャを採用せず1クロックあたり1命令しか実行できない（後述のとおりWinChip 2以降はMMX命令もしくは3DNow\!命令のみ、どちらかを2命令同時実行可能である）。このことからPentiumよりむしろ1世代前の[i486に近いと言われることもある](https://ja.wikipedia.org/wiki/Intel_486 "wikilink")\[1\]。 コア部分が[RISC](../Page/RISC.md "wikilink")方式になっており、各機械語命令を RISC 命令に変換してから実行する\[2\]が、使用頻度の高いx86命令のほとんどを単一のRISC命令に変換できるようにすることでレイテンシの低減を図っている。このことと64kBytes（命令32kBytes、データ32kBytes）という大容量の一次キャッシュの効果によって、同クロックのPentiumに匹敵する性能を発揮する。 内部構造が単純化されているため、他社の製品に比べて安価で消費電力が低いという特徴がある。 ただし[パイプラインが](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")5段と浅いため動作クロックを高めることは困難であった。 また初期の WinChip C6 から [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")のマルチメディア拡張命令セットである [MMX](https://ja.wikipedia.org/wiki/MMX "wikilink") に対応している。 しかし、動作クロック周波数が最大240MHzと低く、絶対的な性能が低いためメーカー製PCにはほとんど採用されなかった。

### アップグレードパーツとしての評価

WinChip 2AまでV<sub>core</sub>とV<sub>io</sub>を分離しない単一電源仕様（電圧は3.3V版と3.52V版の2種類がある）になっていたため、保障外ながら[Socket 5でも使用可能であった](https://ja.wikipedia.org/wiki/Socket_5 "wikilink")。また、Pentiumとの動作互換性が高く、Pentium以外のCPUを想定していない古い[BIOSでも動作することが多かった](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")（6x86やK6はBIOSによるサポートが前提であった）。 さらにマザーボード側で1.5倍に設定するとWinChipは4倍として認識するため、倍率設定に制限のある古いマザーボードでも利用可能であった。(WinChip2 rev.Aのみ3.5倍と認識する) このためPentium(P5系)の環境でも問題無く動作させられることが多く、値段が手ごろであったこともあって古いPCのアップグレードパーツとして人気があった。

## 各世代の製品

### WinChip C6

[Idt_winchip_c6_240mhz.jpg](https://ja.wikipedia.org/wiki/File:Idt_winchip_c6_240mhz.jpg "fig:Idt_winchip_c6_240mhz.jpg") [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")5月に発表された。

WinChip C6は整数演算に関しては同クロックのPentiumとほぼ同等の処理速度を発揮したが、[浮動小数点演算](https://ja.wikipedia.org/wiki/浮動小数点演算 "wikilink")に関してはFPU命令の一部しかパイプライン化されていないため、演算速度が劣っていた。またMMX命令にも対応するが実行ユニットが1個であるため、2命令を同時実行可能なMMX Pentiumと比較して処理能力は大きく劣っていた。

動作クロック周波数は180,200,225,240MHzの4種類がラインナップされた。内部クロック倍率は外部クロックの整数倍の設定しかないため、最上位の240MHz版では外部クロックを60MHzに落とさなければならず（60MHz×4）、Pentium 233MHz（66MHz×3.5）と比較してIO性能が低下するという問題があった。

### WinChip 2

[Idt_winchip_2a_pr200mhz.jpg](https://ja.wikipedia.org/wiki/File:Idt_winchip_2a_pr200mhz.jpg "fig:Idt_winchip_2a_pr200mhz.jpg") [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")5月に発表された。

WinChip 2ではWinChip C6の弱点であった浮動小数点演算とMMXに改良が加えられている\[3\]。浮動小数点演算に関しては[FPU](../Page/FPU.md "wikilink")を全てパイプライン化することによりスループットを向上させた。またMMX処理ユニットが増設され、2命令同時実行可能となっている（整数および浮動小数点演算命令は従来と同じく1命令ずつの処理となる）。またこのMMX処理ユニットはAMD [3DNow\!](https://ja.wikipedia.org/wiki/3DNow! "wikilink")命令にも対応するように拡張された。

これらの改良により、整数演算、浮動小数点演算、MMXのすべてに渡って同クロックのPentiumに匹敵する処理能力を発揮するようになった。

動作クロック周波数および内部クロック倍率に関してはWinChip C6と変わっておらず、240MHz版で外部クロックを60MHzに落とさなければならない問題はそのまま残された。266MHz版（66MHz×4）もアナウンスされていたが結局出荷されることはなかった。

[1999年](../Page/1999年.md "wikilink")にはマイナーチェンジ版である**WinChip2 Rev.A**（以下、WinChip2Aと表記）が発表された\[4\]。 WinChip2Aは外部クロック周波数100MHzの[Super Socket 7規格に対応し](https://ja.wikipedia.org/wiki/Super_Socket_7 "wikilink")、動作クロック倍率は0.5倍刻みの設定が可能になった。さらに2.33倍、3.33倍という変則的なクロック倍率もサポートしていた。

WinChip2Aでは従来の実クロック表示ではなくスピードグレード（[PRレーティングとほぼ同じもの](https://ja.wikipedia.org/wiki/サイリックス#PRレーティング "wikilink")）によるグレード表示がされており、最上位のWinChip2A-266は実クロック233MHz（100MHz×2.33）であり実クロックとグレード表示が一致しなくなった。

### 実現しなかったロードマップ

Centaur Technology社はWinChip 2A以降のロードマップとして以下のものを発表していた。

  - WinChip 2B - V<sub>core</sub>とV<sub>io</sub>を分離してV<sub>core</sub>を2.8Vに下げることにより低消費電力化を図る。
  - WinChip 3 - 一次キャッシュを128kBytes（命令64kBytes、データ64kBytes）に増量\[5\]、 V<sub>core</sub>が2.8Vのデスクトップ版と2.2Vのモバイル版を計画。
  - WinChip 4 - コアを大幅に変更し11段の[パイプラインや的中率の高い](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")[分岐予測](https://ja.wikipedia.org/wiki/分岐予測 "wikilink")機構を備え、動作クロック向上を図る。

しかし[1999年](../Page/1999年.md "wikilink")8月、Centaur Technology社が[台湾](https://ja.wikipedia.org/wiki/台湾 "wikilink")の [VIA Technologies](../Page/VIA_Technologies.md "wikilink") 社に売却されたため、これらの計画は販売されることなく中断し、WinChip 2の製造も中止された。その後 WinChip 4のコア部分は、VIA社の [C3](https://ja.wikipedia.org/wiki/VIA_C3 "wikilink") のコアとして使用されている。

## ラインナップ

<table>
<thead>
<tr class="header">
<th><p>Processor</p></th>
<th><p>周波数<br />
(P-Rate)</p></th>
<th><p>FSB</p></th>
<th><p>パッケージ</p></th>
<th><p>L1キャッシュ</p></th>
<th><p>FPU</p></th>
<th><p>拡張命令</p></th>
<th><p>パイプラインステージ</p></th>
<th><p>トランジスタ</p></th>
<th><p>製造プロセス</p></th>
<th><p>コア電圧</p></th>
<th><p>対応ソケット</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WinChip C6</p></td>
<td><p>180-240MHz</p></td>
<td><p>60, 66MHz</p></td>
<td><p>CPGA 296pin</p></td>
<td><p>64KB</p></td>
<td><p>50%</p></td>
<td><p>MMX</p></td>
<td><p>5(4)</p></td>
<td><p>540万</p></td>
<td><p>0.35μm</p></td>
<td><p>3.3 or 3.52<br />
(single)</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Socket_5" title="wikilink">Socket 5</a> or <a href="https://ja.wikipedia.org/wiki/Socket_7" title="wikilink">7</a></p></td>
</tr>
<tr class="even">
<td><p>WinChip 2</p></td>
<td><p>200-240MHz</p></td>
<td><p>60, 66, 75MHz</p></td>
<td><p>CPGA 296pin</p></td>
<td><p>64KB</p></td>
<td><p>50%</p></td>
<td><p>MMX, 3DNow!</p></td>
<td><p>5(4)</p></td>
<td><p>600万</p></td>
<td><p>0.35μm</p></td>
<td><p>3.3 or 3.52<br />
(single)</p></td>
<td><p>Socket 5 or 7</p></td>
</tr>
<tr class="odd">
<td><p>WinChip 2 rev.A</p></td>
<td><p>200-233MHz<br />
(PR200-266)</p></td>
<td><p>60, 66, 75, 100MHz</p></td>
<td><p>CPGA 296pin</p></td>
<td><p>64KB</p></td>
<td><p>50%</p></td>
<td><p>MMX, 3DNow!</p></td>
<td><p>5(4)</p></td>
<td><p>600万</p></td>
<td><p>0.25μm</p></td>
<td><p>3.3 or 3.52<br />
(single)</p></td>
<td><p>Socket 5 or 7</p></td>
</tr>
<tr class="even">
<td><p>(WinChip 2 rev.B)</p></td>
<td><p>200-233MHz<br />
(PR200-266)</p></td>
<td><p>60, 66, 75, 100MHz</p></td>
<td><p>BGA</p></td>
<td><p>64KB</p></td>
<td><p>50%</p></td>
<td><p>MMX, 3DNow!</p></td>
<td><p>5(4)</p></td>
<td><p>600万</p></td>
<td><p>0.25μm</p></td>
<td><p>2.8<br />
(dual)</p></td>
<td><p>―</p></td>
</tr>
<tr class="odd">
<td><p>(WinChip 3)</p></td>
<td><p>200-266MHz</p></td>
<td><p>―</p></td>
<td><p>CPGA 320pin, BGA, MobileModule</p></td>
<td><p>128KB</p></td>
<td><p>50%</p></td>
<td><p>MMX, 3DNow!</p></td>
<td><p>5(4)</p></td>
<td><p>1,020万</p></td>
<td><p>0.25μm</p></td>
<td><p>2.2-2.8<br />
(dual)</p></td>
<td><p>Socket 7</p></td>
</tr>
<tr class="even">
<td><p>(WinChip 4)</p></td>
<td><p>450-700MHz</p></td>
<td><p>100, 133MHz</p></td>
<td><p>CPGA 370pin</p></td>
<td><p>128KB</p></td>
<td><p>50%</p></td>
<td><p>MMX, 3DNow!</p></td>
<td><p>11</p></td>
<td><p>1,160万</p></td>
<td><p>0.25-0.18μm</p></td>
<td><p>―</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Socket_370" title="wikilink">Socket 370</a></p></td>
</tr>
</tbody>
</table>

## 脚注

## 関連項目

  - [VIA C3](https://ja.wikipedia.org/wiki/VIA_C3 "wikilink")
  - [Cyrix](https://ja.wikipedia.org/wiki/Cyrix "wikilink")
  - [RISC](../Page/RISC.md "wikilink")

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")

1.
2.
3.
4.
5.