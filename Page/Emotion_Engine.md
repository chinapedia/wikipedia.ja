> この記事は[Emotion Engine](https://ja.wikipedia.org/wiki/Emotion_Engine)から翻訳されています。


**Emotion Engine**（エモーション エンジン、略称: **EE**）は、[ソニー・コンピュータエンタテインメント](https://ja.wikipedia.org/wiki/ソニー・コンピュータエンタテインメント "wikilink") (SCE) と[東芝](https://ja.wikipedia.org/wiki/東芝 "wikilink")によって開発され、主に[PlayStation 2向けに設計](https://ja.wikipedia.org/wiki/PlayStation_2 "wikilink")・使用された[MIPS](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ "wikilink") R5900ベースの[128ビット](https://ja.wikipedia.org/wiki/128ビット "wikilink")[RISC](../Page/RISC.md "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")である。実質的な後継は[PlayStation 3における](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")[Cell Broadband Engine](https://ja.wikipedia.org/wiki/Cell_Broadband_Engine "wikilink")。

本項では、同じくSCEによって開発され、PS2向けに設計・使用された[GPU](../Page/Graphics_Processing_Unit.md "wikilink")・**Graphics Synthesizer**（グラフィックス シンセサイザ、略称: **GS**）についても扱う。

この2つのチップはセットで使われる事が多く、当初は独立したチップであったが、のちにワンチップ化が行われた。

## 概要

CPUコアの浮動小数点演算ユニット ([FPU](../Page/FPU.md "wikilink")) 以外に、[VLIW](https://ja.wikipedia.org/wiki/VLIW "wikilink")を採用した2系統のベクトル演算ユニット (VU: Vector Unit) を搭載する。そのためFPU及び2系統のVUを合計した浮動小数点演算能力は、ピーク時で 6.2 G[FLOPS](../Page/FLOPS.md "wikilink") となった。

また、[DMA](../Page/Direct_Memory_Access.md "wikilink")[コントローラが統合されており](https://ja.wikipedia.org/wiki/メモリコントローラー "wikilink")、内部の各ユニットを128bitバスで接続した世界初\[1\]の完全な128ビットプロセッサでもある。

メインメモリとは、ラムバス社のDirect [RDRAM](../Page/RDRAM.md "wikilink")インターフェイス2チャネルにより3.2 GB/sのメモリ帯域で接続されている。また、イメージプロセッシングユニットと呼ばれる[MPEG-2](../Page/MPEG-2.md "wikilink")デコーダユニットを内蔵し、MPEG-2形式のビデオを単体で再生する能力を持つ。

PS2が発売される前の1999年、当時のSCE社長だった[久夛良木健](../Page/久夛良木健.md "wikilink")はこのチップをゲーム機での採用だけにとどまらずマルチメディアワークステーションにも活用する構想を明らかにしていた\[2\]が（詳しくは[\#GScube 16を参照](https://ja.wikipedia.org/wiki/#GScube_16 "wikilink")）、結果としてソニー製品としてはPS2と[PSX](../Page/PSX.md "wikilink")、[WEGA](https://ja.wikipedia.org/wiki/ベガ_\(テレビ\) "wikilink")\[3\]、[QUALIA](https://ja.wikipedia.org/wiki/QUALIA "wikilink") 005\[4\]以外での採用は特になかった。ちなみに久夛良木はPS3のCPUであるCell Broadband Engineでも同様の構想を明らかにしていた\[5\]。

また、[ナムコ](https://ja.wikipedia.org/wiki/ナムコ "wikilink")（ゲームメーカー）と[山佐](https://ja.wikipedia.org/wiki/山佐 "wikilink")（パチスロメーカー）がパチスロ用基板「P246」を共同開発する際、GSと共にEEも採用された。

初期のPS3にもPlayStation 2用ゲームソフトの[互換性](https://ja.wikipedia.org/wiki/互換性 "wikilink")を確保するためにEE+GSが搭載されている。その後GSしか搭載していない一部モデルを経てPS3におけるPS2ゲームソフトの互換性は廃止された。

### 各世代のEE、GSの比較表

<table>
<thead>
<tr class="header">
<th></th>
<th><p>EE#1[6]<br />
（試作）</p></th>
<th><p>EE#2[7]<br />
（SCPH-10000）</p></th>
<th><p>EE#3</p></th>
<th><p>EE#4</p></th>
<th><p>EE+GS<br />
（SCPH-70000）</p></th>
<th><p>EE+GS'<br />
（SCPH-79000以降）</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>チップ面積 (<a href="https://ja.wikipedia.org/wiki/平方ミリメートル" title="wikilink">mm<sup>2</sup></a>)</p></td>
<td><p>240</p></td>
<td><p>224</p></td>
<td><p>110</p></td>
<td><p>73</p></td>
<td><p>86</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>プロセスルール (nm)</p></td>
<td><p>colspan = 2 | 250[8]</p></td>
<td><p>180</p></td>
<td><p>150[9]</p></td>
<td><p>90</p></td>
<td><p>65</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>消費電力 (W)</p></td>
<td><p>15</p></td>
<td><p>18</p></td>
<td><p>colspan="2" </p></td>
<td><p>8.5</p></td>
<td><p>rowspan="2" </p></td>
<td></td>
</tr>
<tr class="even">
<td><p>トランジスタ数 (万)</p></td>
<td><p>1050</p></td>
<td><p>1350</p></td>
<td><p>colspan="2" </p></td>
<td><p>5350</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
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

|             | GS\#1 | GS\#2       | GS\#3       | GS\#4     | GS\#5 | GS\#6 |
| ----------- | ----- | ----------- | ----------- | --------- | ----- | ----- |
| チップ面積(mm2)  | 279   | 188         | 108         | 96        | 83    | 73    |
| プロセスルール(nm) | 250   | 180         | colspan="3" | 130\[10\] |       |       |
| トランジスタ数 (万) | 4300  | colspan="5" |             |           |       |       |
|             |       |             |             |           |       |       |

## Graphics Synthesizer

**Graphics Synthesizer**（グラフィックス シンセサイザ、略称: **GS**）は、SCEによって開発され、主にPS2向けに設計・使用された[GPU](../Page/Graphics_Processing_Unit.md "wikilink")。

### 概要

4[MBの](https://ja.wikipedia.org/wiki/メガバイト "wikilink")[DRAM](https://ja.wikipedia.org/wiki/DRAM "wikilink")を[混載](https://ja.wikipedia.org/wiki/eDRAM "wikilink")\[11\]したことによって、2560 bit（内訳は読み込み 1024 bit、書き込み 1024 bit、テクスチャ 512 bit）という超広帯域の[バス幅を備え](../Page/バス_\(コンピュータ\).md "wikilink")、合計48[GB](../Page/ギガバイト.md "wikilink")/秒という転送速度が特徴。 その他のスペックとしては、ピクセルエンジンと呼ばれるパイプラインを16基備え、147.456 MHzで動作する。なお集積トランジスタ数は4300万、250 nmプロセス製造でダイ面積が279 mm<sup>2</sup>となっており、発表当時としてはPC向けハイエンドチップの2倍以上の規模であった。

## GScube 16

**GScube 16**は、PS2アーキテクチャをベースにメインメモリを4倍の128MBにしたEmotion Engineと、混載メモリを32MBに増量した「Graphics Synthesizer I-32」をそれぞれ16基搭載した、グラフィックワークステーションのプロトタイプである。 形状は正方形で、上部にGSユニットの稼働状況を表すイルミネーションが搭載されている。単独で稼働するワークステーションではなく、ホストシステムを必要とする。

また、チップを64個並列に搭載した「GScube 64」や、さらにそれを拡張し[4000×2000ピクセルで](https://ja.wikipedia.org/wiki/4K解像度 "wikilink")120fpsでの映像出力が可能なワークステーションも予定されていた。

## 脚注

## 外部リンク

  - [SCE Emotion Engine プレスリリース](https://www.sie.com/content/dam/corporate/jp/corporate/release/pdf/990302_3.pdf)
  - [SCE Graphics Synthesizer プレスリリース](https://www.sie.com/content/dam/corporate/jp/corporate/release/pdf/990302_2.pdf)
  - [「次世代プレイステーション」の基本仕様を公開 国内発売はこの冬を予定](https://pc.watch.impress.co.jp/docs/article/990302/play.htm)、PC Watch、1999年3月2日
  - [PlayStation2の心臓Emotion Engineはこうなっている](https://pc.watch.impress.co.jp/docs/article/20000302/kaigai01.htm)、PC Watch、2000年3月2日
  - [SCEI、プレイステーション2エンジンを使ったリアルタイム映像制作システム「GScube」を技術参考出展](https://pc.watch.impress.co.jp/docs/article/20000726/gscube.htm)、PC Watch、2000年7月26日
  - [PlayStation 3の核となるCellは全く新しい概念のCPU](https://pc.watch.impress.co.jp/docs/2002/0325/kaigai02.htm)、PC Watch、2002年3月25日
  - [90nmプロセスの利点を生かした新世代PlayStation 2](https://pc.watch.impress.co.jp/docs/2004/0924/kaigai121.htm)、PC Watch、2004年9月24日
  - [ISSCCに次世代Cell B.E. 45nm版が登場 ～6GHz動作、電力を30%以上削減](https://pc.watch.impress.co.jp/docs/2008/0206/kaigai416.htm)、PC Watch、2008年2月6日

[Category:ソニー・コンピュータエンタテインメント](https://ja.wikipedia.org/wiki/Category:ソニー・コンピュータエンタテインメント "wikilink") [Category:東芝](https://ja.wikipedia.org/wiki/Category:東芝 "wikilink") [Category:MIPSのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:MIPSのマイクロプロセッサ "wikilink") [Category:PlayStation_2](https://ja.wikipedia.org/wiki/Category:PlayStation_2 "wikilink")

1.
2.  [PlayStation2ベースのワークステーションが登場\!](http://pc.watch.impress.co.jp/docs/article/991007/mpf4.htm)、PC Watch、1999年10月7日
3.  [テレビのさらなる高画質・高音質と新しい操作性を実現した＜ベガ＞HVXシリーズ 計6機種　発売](http://www.sony.jp/CorporateCruise/Press/200408/08-0819/)、ソニーマーケティング、2004年8月19日
4.  [世界初、感動の記憶色を再現する広色域LEDバックライト搭載の液晶テレビ 発売](http://www.sony.jp/CorporateCruise/Press/200408/08-0819B/)、ソニーマーケティング、2004年8月19日
5.  [IBM/SCE/ソニーのCellプロセッサワークステーション](http://pc.watch.impress.co.jp/docs/2004/0514/kaigai090.htm)、PC Watch、2004年5月14日
6.
7.  [Cell Broadband Engineへの20年と、 半導体産業・次の10年の展開](http://www.shmj.or.jp/dev_story/pdf/develop31.pdf)
8.  ゲート長は180nm
9.  [「積極的な半導体設備投資は“PS2のおかげ”」――ソニー、2000億円投資で次世代チップ「CELL」製造へ](http://www.itmedia.co.jp/news/0304/21/nj00_sony.html?print)ITmedia2003年4月21日
10.
11. 複数チップの組み合わせではなく、1枚のチップ内に混載されている。