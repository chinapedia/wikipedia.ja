> この記事は[GRAPE](https://ja.wikipedia.org/wiki/GRAPE)から翻訳されています。


**GRAPE**（グレープ）は、[東京大学](https://ja.wikipedia.org/wiki/東京大学 "wikilink")総合文化研究科に所属していた[杉本大一郎](../Page/杉本大一郎.md "wikilink")（現：[放送大学](https://ja.wikipedia.org/wiki/放送大学 "wikilink")）、[戎崎俊一](../Page/戎崎俊一.md "wikilink")（現：[理化学研究所](https://ja.wikipedia.org/wiki/理化学研究所 "wikilink")）、[牧野淳一郎](../Page/牧野淳一郎.md "wikilink")（現：[国立天文台](../Page/国立天文台.md "wikilink")）、[伊藤智義](../Page/伊藤智義.md "wikilink")（現：[千葉大学](https://ja.wikipedia.org/wiki/千葉大学 "wikilink")）、[泰地真弘人](https://ja.wikipedia.org/wiki/泰地真弘人 "wikilink")（現：[理化学研究所](https://ja.wikipedia.org/wiki/理化学研究所 "wikilink")）らによって開発された多体問題[専用計算機](https://ja.wikipedia.org/wiki/専用計算機 "wikilink")である。GRAPE では[重力](../Page/重力.md "wikilink")[多体問題](../Page/多体問題.md "wikilink")の[計算量の大部分を占める重力相互作用の計算を専用の](https://ja.wikipedia.org/wiki/計算複雑性理論 "wikilink")[パイプラインを組み込んだ](../Page/パイプライン処理.md "wikilink")[ハードウェア](../Page/ハードウェア.md "wikilink")で高速に処理する。GRAPE の名前は **GRA**vity Pi**PE** の略称に由来する。

## 目的

GRAPE の目的は、[球状星団](../Page/球状星団.md "wikilink")や[銀河](../Page/銀河.md "wikilink")、[銀河団](../Page/銀河団.md "wikilink")といった多数の[恒星](../Page/恒星.md "wikilink")からなる[天体](../Page/天体.md "wikilink")の時間進化や動力学を数値的に[シミュレーション](../Page/シミュレーション.md "wikilink")することであった。このような天体には、球状星団で約10<sup>4-5</sup>個、銀河では約10<sup>10-12</sup>個という膨大な個数の恒星が含まれている。恒星の間に働く[万有引力](../Page/万有引力.md "wikilink")は到達距離の典型的スケールを持たない逆2乗力であるため、このような重力多体系の数値シミュレーションを行なうには個々の星の間に働く重力を全て計算する必要がある。一般に、N個の粒子からなる多体系では任意の2粒子の組み合わせの個数は N<sup>2</sup> に比例するため、多体系の数値計算では粒子の位置から粒子間相互作用を求める計算が計算量全体の大部分を占める。そのため、GRAPE が開発された1980年代終わりには当時の最高速の[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")でも N=1000 体程度以上の計算を実用的な計算時間で行なうのは困難だった。

そこで GRAPE は、*O*(N<sup>2</sup>) の計算量を要する粒子間相互作用の部分のみを専用ハードウェアを用いて計算することで[多体問題](../Page/多体問題.md "wikilink")の計算速度を飛躍的に加速させる、という発想に基づいて開発された。

## アーキテクチャ

一般に、[重力](../Page/重力.md "wikilink")多体系の時間発展の計算は以下のようなステップで行なわれる。

1.  粒子 i が粒子 j から受ける重力 \(\mathbf{F}_{ij}\) を計算する。
2.  \(\mathbf{F}_{ij}\) を j について積算し、粒子 i が受ける重力の総和 \(\mathbf{F}_{i}\) を求める。
3.  \(\mathbf{F}_{i}\) を運動方程式に代入して、粒子 i の加速度 \(\mathbf{a}_{i}\) を求める。
4.  \(\mathbf{a}_{i}\) を用いて時間積分を行い、粒子 i の位置 \(\mathbf{r}_{i}\) と 速度 \(\mathbf{v}_{i}\) を更新する。
5.  以上を全粒子について繰り返す。
6.  以上を時間ステップごとに繰り返す。

GRAPE はこの計算ステップのうち最も[計算量の多いステップ](https://ja.wikipedia.org/wiki/計算複雑性理論 "wikilink") 1と2 の計算のみを行ない、これ以外の計算は GRAPE が接続された汎用的な[ワークステーション](../Page/ワークステーション.md "wikilink")などが行なう。

GRAPE の基本的な[アーキテクチャは単純である](../Page/コンピュータ・アーキテクチャ.md "wikilink")。粒子 i と粒子 j の位置ベクトル \(\mathbf{r}_{i}\), \(\mathbf{r}_{j}\) と質量 \(m_i\), \(m_j\) を入力として与え、ニュートンの[万有引力](../Page/万有引力.md "wikilink")の法則：

  -
    \(\mathbf{F}_{ij} = - G \frac{m_i m_j}{|\mathbf{r}_i - \mathbf{r}_j|^3} (\mathbf{r}_i - \mathbf{r}_j)\)

から粒子間に働く重力 \(\mathbf{F}_{ij}\) を求めて出力する。この際、重力の計算を逐次的に行なわず、方程式に含まれる位置座標同士の減算、2乗、加算といった各演算を行なう[演算器](https://ja.wikipedia.org/wiki/演算器 "wikilink")を直列に並べて[パイプラインを組み](../Page/パイプライン処理.md "wikilink")、パイプラインの最終段で最終結果 \(\mathbf{F}_{ij}\) が出力されるようになっているのが GRAPE の本質的特徴である。万有引力の計算には約30ステップの演算が必要なので逐次処理では結果を得るのに約30[クロック](../Page/クロック.md "wikilink")を要するが、GRAPE では1クロックごとに重力が計算されて次々と得られることになる。実際にはパイプラインを複数並列化することで計算をさらに加速している。

## 歴史

### 概略

専用設計の[パイプラインハードウェアにより多体計算を力任せに行なうというアイデアは](../Page/パイプライン処理.md "wikilink")[1988年](../Page/1988年.md "wikilink")に[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")の[国立天文台](../Page/国立天文台.md "wikilink")の[近田義広](../Page/近田義広.md "wikilink")によって最初に提唱された。近田は1980年代に[電波望遠鏡](../Page/電波望遠鏡.md "wikilink")を用いた[開口合成](../Page/開口合成.md "wikilink")観測のデータ解析用計算機として同様のアイデアに基づく[デジタル分光計](../Page/FX型デジタル分光相関器.md "wikilink") を開発し、100G[OPS](https://ja.wikipedia.org/wiki/OPS "wikilink") の演算速度を達成していた。

近田のアイデアを聞いた[東京大学](https://ja.wikipedia.org/wiki/東京大学 "wikilink")教養学部[宇宙地球科学教室の](https://ja.wikipedia.org/wiki/駒場宇宙地球部会 "wikilink")[杉本大一郎](../Page/杉本大一郎.md "wikilink")が中心となって重力[多体問題](../Page/多体問題.md "wikilink")専用[計算機の開発が始まり](../Page/コンピュータ.md "wikilink")、[1989年](../Page/1989年.md "wikilink")9月に最初の **GRAPE-1** が完成した。GRAPE-1 はユニバーサル基板上に各演算器の [IC](../Page/集積回路.md "wikilink") や [ROM](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink") を配置し[ワイヤラッピング](../Page/ワイヤラッピング.md "wikilink")で結線した試作機で開発費用は約20万円だった。GRAPE-1 では簡略化のためにデータ幅を8[ビット](../Page/ビット.md "wikilink")とし、全ての演算を [ROM](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink") のテーブル参照で済ませるようにした。[銀河](../Page/銀河.md "wikilink")など、[二体緩和](https://ja.wikipedia.org/wiki/二体緩和 "wikilink")時間が[宇宙年齢](https://ja.wikipedia.org/wiki/宇宙年齢 "wikilink")より長いような無衝突系のシミュレーションは8ビットの精度でも十分に可能なため、GRAPE-1 は試作機でありながら実際の[天文学](../Page/天文学.md "wikilink")の研究にも役に立つ性能を有していた。その理論性能は 240[M](../Page/メガ.md "wikilink")[FLOPS](../Page/FLOPS.md "wikilink") 相当で、実効性能でも1万体の計算で約160MFLOPS に達した。

[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")5月には汎用の計算機と同様の[単精度](https://ja.wikipedia.org/wiki/単精度 "wikilink")32[ビット](../Page/ビット.md "wikilink")及び[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink")64ビットの計算が可能な **GRAPE-2** が完成した。理論性能は約40MFLOPSだった。これ以降、GRAPE シリーズでは型番が奇数の機種が精度を限定したタイプ、偶数の機種が高精度計算に用いられるタイプとして開発されている。

[1991年](../Page/1991年.md "wikilink")の **GRAPE-3** では重力計算パイプライン回路が[専用 LSI](../Page/ASIC.md "wikilink") 化され、理論性能は約15GFLOPSに達した。

[1993年](../Page/1993年.md "wikilink")には GRAPE-2 の後継となる高精度型計算機の **HARP-1** が開発された。HARP は **H**ermite **A**ccelerato**R** **P**ipe の略称で、多体問題の時間積分法にエルミート積分法（[エルミート補間](https://ja.wikipedia.org/wiki/エルミート補間 "wikilink")多項式を用いた[予測子・修正子法](https://ja.wikipedia.org/wiki/予測子・修正子法 "wikilink")）を用いることを想定し、粒子の[加速度](../Page/加速度.md "wikilink")だけでなく加速度の時間微分 (\(\dot{a}\)) もハードウェアで計算するものである。これによって球状星団や銀河中心核といった緩和時間の短い衝突系の問題を高速に解くことができるようになった。

[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")には HARP-1 の後継となる **GRAPE-4** が完成した。GRAPE-4 では重力計算パイプラインだけでなく時間積分の予測子の計算も専用 LSI でハードウェア化されている。最大構成では約 1.08 TFLOPS の理論計算性能に達し、実用的科学技術計算で[テラ](../Page/テラ.md "wikilink")フロップス (TFLOPS) を超えた世界最初の計算機となった。GRAPE-4 は1995年、[1996年](../Page/1996年.md "wikilink")の[ゴードン・ベル賞](../Page/ゴードン・ベル賞.md "wikilink")を受賞した。

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")には GRAPE-3 の後継機である **GRAPE-5** が完成した。GRAPE-5 ではクロック周波数が 80MHz まで高速化された。GRAPE-5 は宇宙論的構造形成の計算で 1MFLOPS 当たり $7 という価格性能比を達成し、[1999年](../Page/1999年.md "wikilink")のゴードン・ベル賞価格性能比部門賞を受賞した。

[2002年](../Page/2002年.md "wikilink")には GRAPE-4 の後継機である **GRAPE-6** が完成した。GRAPE-6 は最大構成の GRAPE-4 とほぼ同等の性能を持つプロセッサボード64枚から構成され、ボード4枚ごとに [Linux](../Page/Linux.md "wikilink") で稼動するホスト [PC](../Page/パーソナルコンピュータ.md "wikilink")（パーソナルコンピュータ）が付き、PC 間は[ギガビット・イーサネットで接続されていた](https://ja.wikipedia.org/wiki/イーサネット#ギガビット・イーサネット "wikilink")。理論性能は 64TFLOPS に達した。GRAPE-6 は開発中の[2000年](../Page/2000年.md "wikilink")、[2001年](../Page/2001年.md "wikilink")にゴードン・ベル賞を受賞し、2002年には最大構成で実効計算性能 29.5TFLOPS を達成してゴードン・ベル賞ファイナリストに選出された。[2003年](../Page/2003年.md "wikilink")には 33.4TFLOPS で三たびゴードン・ベル賞を受賞した。

[2006年](../Page/2006年.md "wikilink")には **GRAPE-7** が完成した。GRAPE-7 は PROGRAPE と GRAPE-5 の流れをくむ機種であり、内部回路を書き換え可能な [FPGA](../Page/FPGA.md "wikilink") を1 - 7個搭載している（構成による）。現在のところ内部回路としては GRAPE-5 と同等のパイプラインが完成しており、最大構成モデルにこのパイプラインを実装した場合の動作は理論性能 364GFLOPS 相当まで確認されている。[2006年](../Page/2006年.md "wikilink")に宇宙論的構造形成の計算で 1GFLOPS 当たり $105 という価格性能比を達成し、同年のゴードン・ベル賞価格性能比部門ファイナリストに選出された。

[2006年](../Page/2006年.md "wikilink")11月、**GRAPE-DR**(Greatly Reduced Array of Processor Element with Data Reduction)の開発成功に関して報道発表を行った\[1\]。GRAPE-DRは汎用性を持ち、様々なプログラムを実行できる。 [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")6月、GRAPE-DRは、省エネ志向のスパコンとして電力当たりの演算性能の高さが評価され、「Little Green500 List」で世界一位とされた\[2\]\[3\]\[4\]。

[2011年](../Page/2011年.md "wikilink")現在、国立天文台と[高エネルギー加速器研究機構](../Page/高エネルギー加速器研究機構.md "wikilink")の共同研究で、ストラクチャードASICを用いて四倍精度浮動小数点計算が行えるプロセッサ**GRAPE-MP**の開発、実装を進めている\[5\]。ファインマンループ積分、重力多体系の計算が動作しており、四倍精度計算で約1200MFLOPSの理論性能を有する。さらに、六倍精度浮動小数点計算が行える**GRAPE-MP6**の開発も進めている\[6\]

[2012年](../Page/2012年.md "wikilink")3月、東京工業大学と一橋大学の研究グループが**GRAPE-8**を発表\[7\]。ASICとFPGAの中間的なストラクチャードASICを使用し、コストを抑えることに成功した。またボード単体で20.9Gflops/W、システム全体で6.5Gflops/Wの高い電力性能比を達成した。

[2013年](../Page/2013年.md "wikilink")12月、GRAPE-7の後継機として開発された**GRAPE-9**が発表された。内部回路を書き換え可能な [FPGA](../Page/FPGA.md "wikilink") を8個もしくは16個搭載している。

### GRAPE シリーズ

2012年までに開発された GRAPE シリーズの一覧は以下の通りである。

<table>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>完成年</p></th>
<th><p>理論演算性能</p></th>
<th><p>研究補助等</p></th>
<th><p>クロック周波数</p></th>
<th><p>I/F</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GRAPE-1</p></td>
<td><p>1989年</p></td>
<td><p>240<a href="../Page/メガ.md" title="wikilink">M</a><a href="../Page/FLOPS.md" title="wikilink">FLOPS</a></p></td>
<td><p>一般研究費の一部</p></td>
<td><p>8MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/GPIB" title="wikilink">GPIB</a></p></td>
<td><p>試作機</p></td>
</tr>
<tr class="even">
<td><p>GRAPE-2</p></td>
<td><p>1990年</p></td>
<td><p>40MFLOPS</p></td>
<td><p>一般研究費の一部</p></td>
<td><p>4MHz</p></td>
<td><p><a href="../Page/VMEバス.md" title="wikilink">VME</a></p></td>
<td><p>初の高精度（<a href="https://ja.wikipedia.org/wiki/倍精度" title="wikilink">倍精度</a>）型</p></td>
</tr>
<tr class="odd">
<td><p>GRAPE-3</p></td>
<td><p>1991年</p></td>
<td><p>15<a href="../Page/ギガ.md" title="wikilink">GFLOPS</a><br />
(300MFLOPS/chip)</p></td>
<td><p><a href="../Page/富士ゼロックス.md" title="wikilink">富士ゼロックス</a>電子技術研究所</p></td>
<td><p>10MHz</p></td>
<td><p><a href="../Page/VMEバス.md" title="wikilink">VME</a></p></td>
<td><p>フルカスタムLSI化(National Semiconductor社においてASIC化)。後にプリント基板化した GRAPE-3A (20MHz) も開発。</p></td>
</tr>
<tr class="even">
<td><p>GRAPE-4</p></td>
<td><p>1995年</p></td>
<td><p>1.08<a href="../Page/テラ.md" title="wikilink">TFLOPS</a><br />
(640MFLOPS/chip)</p></td>
<td><p><a href="../Page/文部科学省.md" title="wikilink">文部省科研費特別推進研究</a></p></td>
<td><p>16MHz</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/TURBOchannel" title="wikilink">TURBOchannel</a> / <a href="../Page/Peripheral_Component_Interconnect.md" title="wikilink">PCI</a></p></td>
<td><p>TURBOchannelは、当時、研究室で使えるEWSがVAXStationだったため。PCIは後から追加。</p></td>
</tr>
<tr class="odd">
<td><p>GRAPE-5</p></td>
<td><p>1998年</p></td>
<td><p>1TFLOPS<br />
(5GFLOPS/chip)</p></td>
<td><p><a href="../Page/文部科学省.md" title="wikilink">文部省科研費特別推進研究</a></p></td>
<td><p>80MHz</p></td>
<td><p>PCI</p></td>
<td><p>GRAPE-3の改良型。</p></td>
</tr>
<tr class="even">
<td><p>GRAPE-6</p></td>
<td><p>2002年</p></td>
<td><p>64TFLOPS<br />
(31GFLOPS/chip)</p></td>
<td><p><a href="../Page/日本学術振興会.md" title="wikilink">日本学術振興会</a>未来開拓学術研究</p></td>
<td><p>90MHz</p></td>
<td><p>PCI / <a href="https://ja.wikipedia.org/wiki/LVDS" title="wikilink">LVDS</a><br />
ホスト間: <a href="../Page/イーサネット.md" title="wikilink">GbE</a></p></td>
<td><p>ASICチップを増強して速度向上を行う。2008年9月20日をもって製造を終了、在庫限りで販売も終了する。</p></td>
</tr>
<tr class="odd">
<td><p>GRAPE-7</p></td>
<td><p>2006年</p></td>
<td><p>600GFLOPS<br />
(100GFLOPS/chip)</p></td>
<td><p><a href="../Page/日本学術振興会.md" title="wikilink">日本学術振興会</a>未来開拓学術研究</p></td>
<td><p>100MHz/133MHz</p></td>
<td><p><a href="../Page/PCI-X.md" title="wikilink">PCI-X</a> (64bit 100MHz/133MHz)</p></td>
<td><p><a href="../Page/FPGA.md" title="wikilink">FPGA</a>を使用。内部回路を書き換え可能。演算性能と動作周波数は、GRAPE-5と同等のパイプラインを書き込んだ場合のおおまかな目安。<a href="http://www.kfcr.jp/">KFCR</a>社より製品化。</p></td>
</tr>
<tr class="even">
<td><p>GRAPE-DR</p></td>
<td><p>2008年</p></td>
<td><p>単精度(409.6GFLOPS/chip)<br />
倍精度<br />
(204.8GFLOPS/chip)[8]</p></td>
<td><p><a href="../Page/文部科学省.md" title="wikilink">文部科学省</a>科学技術振興調整費、<a href="../Page/NTTコミュニケーションズ.md" title="wikilink">NTTコミュニケーションズ</a>、<a href="../Page/富士通.md" title="wikilink">富士通</a></p></td>
<td><p>400MHz</p></td>
<td><p>PCI-X (64bit 133MHz),PCIe</p></td>
<td><p>高性能<a href="https://ja.wikipedia.org/wiki/グリッドコンピュータ" title="wikilink">グリッド計算機として多数のシステムとの連携も視野に入れたシステム</a>。GRAPE-7の<a href="../Page/FPGA.md" title="wikilink">FPGA</a>を<a href="../Page/ASIC.md" title="wikilink">ASIC</a>にして、より高密度高性能化を行う。[9] GRAPE-DRプロジェクトは、高速専用線インターネット接続と高速GRAPEチップの構築を主にしたプロジェクトである。2010年6月、電力当たりの演算性能が評価され、The Green500 Listで世界一位とされる[10][11][12]。KFCR社より製品化。</p></td>
</tr>
<tr class="odd">
<td><p>GRAPE-8</p></td>
<td><p>2012年</p></td>
<td><p>960GFLOPS<br />
(480GFLOPS/chip)</p></td>
<td><p>文部科学省科学研究費補助金</p></td>
<td><p>250MHz</p></td>
<td><p>PCIe</p></td>
<td><p>再び専用機。プロセッサにeASIC社のストラクチャードASIC、PCIe制御にFPGAを使用。</p></td>
</tr>
<tr class="even">
<td><p>GRAPE-9</p></td>
<td><p>2013年</p></td>
<td><p>12Tflops<br />
(750GFLOPS/chip)</p></td>
<td><p>？</p></td>
<td><p>？</p></td>
<td><p>PCIe</p></td>
<td><p><a href="../Page/FPGA.md" title="wikilink">FPGA</a>を使用。演算性能は、GRAPE-5と同等のパイプラインを書き込んだ場合の目標値。<a href="http://www.kfcr.jp/">KFCR</a>社より製品化。</p></td>
</tr>
</tbody>
</table>

## GRAPE から派生した専用計算機

GRAPE プロジェクトをきっかけとして、専用[パイプラインによる計算の高速化という](../Page/パイプライン処理.md "wikilink") GRAPE の基本概念を継承した様々な専用計算機が開発されている。

### 分子動力学用計算機

GRAPE アーキテクチャの応用例の中でも重要なものは、GRAPE のハードウェアを[分子動力学](https://ja.wikipedia.org/wiki/分子動力学 "wikilink") (MD) に応用した計算機である。水中の[蛋白質](https://ja.wikipedia.org/wiki/蛋白質 "wikilink")の MD シミュレーションでは蛋白質[分子](../Page/分子.md "wikilink")を構成する各[原子](https://ja.wikipedia.org/wiki/原子 "wikilink")や媒質となる[水](../Page/水.md "wikilink")分子の[水素](https://ja.wikipedia.org/wiki/水素 "wikilink")・[酸素](../Page/酸素.md "wikilink")原子の間に働く[分子間力](../Page/分子間力.md "wikilink")・[クーロン力](https://ja.wikipedia.org/wiki/クーロン力 "wikilink")などの相互作用を大量に計算する必要がある。MD で扱うこの種の相互作用は全て[万有引力](../Page/万有引力.md "wikilink")と同様の[中心力](../Page/中心力.md "wikilink")であるため、GRAPE の[パイプラインを修正することで](../Page/パイプライン処理.md "wikilink") MD の計算にも応用が可能となる。

このようにして[1992年](../Page/1992年.md "wikilink")に、GRAPE-2 を MD にも使えるように改良した **GRAPE-2A** が開発された。GRAPE-2A は 180[M](../Page/メガ.md "wikilink")[FLOPS](../Page/FLOPS.md "wikilink") の理論性能を持っていた。[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")にはこの後継として回路を [ASIC](../Page/ASIC.md "wikilink") 化した **MD-GRAPE** が作られた。その後は[東京大学](https://ja.wikipedia.org/wiki/東京大学 "wikilink")から[理化学研究所](https://ja.wikipedia.org/wiki/理化学研究所 "wikilink")に移った[戎崎俊一](../Page/戎崎俊一.md "wikilink")を中心とするグループで改良が行なわれ、[2002年](../Page/2002年.md "wikilink")には理論性能 75[TFLOPS](../Page/テラ.md "wikilink") の **MDM** が開発された。

GRAPE-2A/MD-GRAPE の系譜を引く分子動力学用計算機の一覧は以下の通りである。

| 名称                                                              | 完成年   | 理論演算性能                                                               | プロセッサ                                                 | 備考                                                                                |
| --------------------------------------------------------------- | ----- | -------------------------------------------------------------------- | ----------------------------------------------------- | --------------------------------------------------------------------------------- |
| GRAPE-2A                                                        | 1993年 | 200[M](../Page/メガ.md "wikilink")[FLOPS](../Page/FLOPS.md "wikilink") |                                                       | GRAPE-2 の改良型                                                                      |
| MD-GRAPE                                                        | 1995年 | 4.2GFLOPS                                                            | 専用[ASIC](../Page/ASIC.md "wikilink")                  | [分子動力学](https://ja.wikipedia.org/wiki/分子動力学 "wikilink")用に改良されたGRAPEチップを搭載         |
| MDGRAPE-2                                                       | 1999年 | 16GFLOPS                                                             | 専用ASIC                                                | 独自開発のMDMチップとWINEチップを搭載                                                            |
| [MDGRAPE-3](https://ja.wikipedia.org/wiki/MDGRAPE-3 "wikilink") | 2005年 | 33[GFLOPS](../Page/ギガ.md "wikilink")                                 | 専用ASIC                                                | MDMチップとWINEチップを統合し、1チップ化                                                          |
| MDM                                                             | 2000年 | 78[TFLOPS](../Page/テラ.md "wikilink")                                 | 専用ASIC                                                | MDGRAPE-2の超並列機                                                                    |
| Protein Explorer                                                | 2006年 | 1[PFLOPS](https://ja.wikipedia.org/wiki/ペタ "wikilink")               | 専用ASIC                                                | MDGRAPE-3の超並列機                                                                    |
| MDGRAPE-4                                                       | 2014年 | 2.5[TFLOPS](../Page/テラ.md "wikilink")                                | 専用ASIC                                                |                                                                                   |
| MDGRAPE-4A                                                      | 2019年 | 1.3PFLOPS                                                            | 専用[SoC](https://ja.wikipedia.org/wiki/SoC "wikilink") | [RISC-V](https://ja.wikipedia.org/wiki/RISC-V "wikilink")ベースの512チップ構成\[13\]\[14\] |

### WINE

[1993年](../Page/1993年.md "wikilink")には[周期的境界条件](../Page/周期的境界条件.md "wikilink")の下での[重力](../Page/重力.md "wikilink")・[クーロン力](https://ja.wikipedia.org/wiki/クーロンの法則 "wikilink")[多体問題](../Page/多体問題.md "wikilink")の計算を行なう専用[計算機](../Page/コンピュータ.md "wikilink") **WINE** (**W**ave space **IN**tegrator for **E**wald method) が開発された。WINE は周期境界条件の下での[中心力](../Page/中心力.md "wikilink")の厳密解を求める[エヴァルト法の](../Page/エバルトの方法.md "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")を専用[パイプラインで実装したものである](../Page/パイプライン処理.md "wikilink")。WINE は MD や[宇宙の大規模構造](../Page/宇宙の大規模構造.md "wikilink")のシミュレーションなど、周期境界条件を用いる多体問題に活用された。また[理化学研究所](https://ja.wikipedia.org/wiki/理化学研究所 "wikilink") （理研）の MDM ではシステムの一部として WINE の回路を1チップに集積した WINE-2 チップを周期境界の計算に用いている。

### PROGRAPE

1990年代後半になると回路を再構成できる [FPGA](../Page/FPGA.md "wikilink") のゲート数の多い製品が安価に入手できるようになり、[ASIC](../Page/ASIC.md "wikilink") として実装していた GRAPE の[パイプラインを](../Page/パイプライン処理.md "wikilink") FPGA 上に実装できるようになった。そこで[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に GRAPE-3 相当の回路を FPGA で実現した **PROGRAPE-1** (**PRO**grammable **GRAPE**) が開発された。PROGRAPE-1 は 16MHz で動作し、理論性能は 0.96 GFLOPS だった。PROGRAPE では FPGA を使用しているため、解くべき問題に応じてパイプラインを自由に再構成でき、幅広い問題に利用できる利点を持つ。2006年現在、PROGRAPE シリーズの最新機種は[理化学研究所](https://ja.wikipedia.org/wiki/理化学研究所 "wikilink")（理研）で開発されている **PROGRAPE-4** で、理論性能は 243.2[G](../Page/ギガ.md "wikilink")[FLOPS](../Page/FLOPS.md "wikilink") に達している。

## 成果

GRAPE は理論[天文学](../Page/天文学.md "wikilink")の内、多体問題における様々な分野のシミュレーションに用いられることとなり、多くの科学的成果をもたらしてきた。また、専用機として開発してきたため、GRAPE は汎用の[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")に対して常に 1/10 から 1/100 の開発予算で同程度またはそれ以上の計算性能を達成することが出来た。設計資料に基づく、GRAPE ボードの多くは企業によって量産化され、[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")国内だけでなく世界各国の天文学の研究室に販売されている。GRAPE で行なわれているシミュレーションの例としては以下のような問題が挙げられる。

  - [球状星団](../Page/球状星団.md "wikilink")の[重力](../Page/重力.md "wikilink")[熱力学](../Page/熱力学.md "wikilink")的進化
  - [銀河](../Page/銀河.md "wikilink")の動力学的進化
  - 銀河の衝突・合体
  - 大質量[ブラックホール](../Page/ブラックホール.md "wikilink")を持つ銀河中心核の構造
  - [銀河団](../Page/銀河団.md "wikilink")の動力学的進化
  - [宇宙論的大規模構造形成](../Page/宇宙の大規模構造.md "wikilink")
  - [原始惑星系円盤](../Page/原始惑星系円盤.md "wikilink")での[惑星](../Page/惑星.md "wikilink")形成
  - [ジャイアント・インパクトに伴う](../Page/ジャイアント・インパクト説.md "wikilink")[月](https://ja.wikipedia.org/wiki/月 "wikilink")の形成
  - 惑星の[環の構造](../Page/環_\(天体\).md "wikilink")・進化

## 参考文献

  -
  -
  -
  -
  -
  -
  -
  -
  -
他

## 関連項目

### 研究分野

  - [計算科学](../Page/計算科学.md "wikilink") - [物理学](../Page/物理学.md "wikilink")
  - [天文学](../Page/天文学.md "wikilink") - [宇宙物理学](https://ja.wikipedia.org/wiki/宇宙物理学 "wikilink") - [シミュレーション天文学](../Page/シミュレーション天文学.md "wikilink")

### 技術要素

  - [スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink") - [シミュレーション](../Page/シミュレーション.md "wikilink")
  - [ASIC](../Page/ASIC.md "wikilink") - [FPGA](../Page/FPGA.md "wikilink")

### 関連研究

  - [スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink") - [PACS](https://ja.wikipedia.org/wiki/PACS "wikilink")

## 脚注

<div class="references-small">

<references />

</div>

## 外部リンク

  - [GRAPEプロジェクト](http://jun.artcompsci.org/grape/)

  - [GRAPE-DRプロジェクト](http://grape-dr.adm.s.u-tokyo.ac.jp/)

  -
[Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink") [Category:コンピュータアーキテクチャ](https://ja.wikipedia.org/wiki/Category:コンピュータアーキテクチャ "wikilink") [Category:計算科学](https://ja.wikipedia.org/wiki/Category:計算科学 "wikilink")

1.  [「世界最高速のスーパーコンピュータ用プロセッサチップ開発に成功　－　ペタフロップス実現へ大きな一歩　－」](http://grape-dr.adm.s.u-tokyo.ac.jp/press-release20061106/)
2.  [THE GREEN500 List - June 2010](http://www.green500.org/lists/2010/06/little/list.php)
3.  [PC Watch (2010年 7月 7日)：東大・国立天文台の「GRAPE-DR」が電力効率世界一を達成 7月6日 発表](http://pc.watch.impress.co.jp/docs/news/20100707_379021.html)
4.  [マイコミジャーナル：NAOJのスパコン - 「Green 500」で世界トップクラスの電力効率を実現](https://news.mynavi.jp/news/2010/07/07/001/?rt=na)
5.  [Hiroshi Daisaka, Naohito Nakasato, Junichiro Makino, Fukuko Yuasa and Tadashi Ishikawa: GRAPE-MP: An SIMD Accelerator Board for Multi-precision Arithmetic](https://doi.org/10.1016/j.procs.2011.04.093)
6.  [平成22年度学融合推進センター学融合研究事業 成果報告書](http://center.soken.ac.jp/project/koubo/2010/s61umn00000028f5-att/s61umn00000028gy.pdf)。
7.  <http://www.hyoka.koho.titech.ac.jp/eprd/recently/research/research.php?id=271>
8.  [K\&F Computing Research 製品情報 : 科学技術計算向け加速ボード GRAPE-DR](http://www.kfcr.jp/grapedr.html)
9.  [東大、1チップで512G FLOPSを達成する512コアプロセッサ](http://pc.watch.impress.co.jp/docs/2006/1106/tokyou.htm)
10.
11.
12.
13.
14.