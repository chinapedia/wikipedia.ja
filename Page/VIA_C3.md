> この記事は[VIA C3](https://ja.wikipedia.org/wiki/VIA_C3)から翻訳されています。


**VIA C3**（ヴィア シースリー）は、[台湾](https://ja.wikipedia.org/wiki/台湾 "wikilink")[VIA Technologies](../Page/VIA_Technologies.md "wikilink") (VIA) が開発した[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")用[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")[アーキテクチャの](../Page/コンピュータ・アーキテクチャ.md "wikilink")[CPU](../Page/CPU.md "wikilink")であり、C3はかつて**Cyrix III**（サイリックス・スリー）という名で販売されていた。C3・CyrixIIIともにVIAが[IDT](../Page/IDT.md "wikilink")から買収した[WinChip](../Page/WinChip.md "wikilink")シリーズの設計を行っていた[セントールテクノロジー](https://ja.wikipedia.org/wiki/セントールテクノロジー "wikilink")のコアをベースとしている。[2005年](../Page/2005年.md "wikilink")後継製品として**[VIA C7](../Page/VIA_C7.md "wikilink")**（シー・セブン）が発表された。

本項ではVIA C3およびVIA CyrixIIIについて記述する。

## Cyrix III

[thumb](https://ja.wikipedia.org/wiki/画像:Via_cyrixiii_samuel1_600mhz.jpg "wikilink") **Cyrix III**（サイリックス スリー）はVIAが[2000年](../Page/2000年.md "wikilink")に発表した同社初のCPU製品である。

当初はVIAが[ナショナル セミコンダクターから買収した](../Page/ナショナル_セミコンダクター.md "wikilink")[Cyrixチームの設計によるJoshua搭載製品でのデビューを発表していたが](../Page/サイリックス.md "wikilink")、実際に発売された製品ではアナウンスが無かったにも関わらずVIAが同じくIDTから買収したCentaurチームによるSamuelコア搭載製品となっていた。 WinChipシリーズをベースとしているにも関わらず**Cyrix**のブランドを引き続き採用したことに対し、VIAではCPUメーカーとして実績を持つCyrixブランドを活用するためと述べている。

ローエンドPC市場をターゲットとしており、当初はx86CPU市場において10%のシェアの獲得を目指すとしていたが、大手PCメーカーで採用されることは無かった。後述のSamuel2コア搭載製品以降はC3に製品ブランドが変更され、CyrixIIIは終了した。

### Samuel (C5A)

**Samuel**（サミュエル）はWinChip 4コアをベースとして開発され、VIAが最初に市場に投入したCPUコアである。後に投入されたSamuel2との区別の為、Samuel1コアと呼称される場合もある。

Samuelは[L2キャッシュ](../Page/L2キャッシュ.md "wikilink")を搭載せず、[浮動小数点数](../Page/浮動小数点数.md "wikilink")演算装置 ([FPU](../Page/FPU.md "wikilink")) は動作[クロック](../Page/クロック.md "wikilink")の半分のクロック周波数で動作していた。また、マルチメディア拡張命令として[3DNow\!](../Page/3DNow!.md "wikilink")をサポートするが、[MMX](../Page/MMX.md "wikilink")ユニットでMMX命令と3DNow\!命令の処理を行っているため、一度にどちらかの命令しか処理できない。そのため、コア全体のパフォーマンスは他の競合製品と比べて劣っていた。

0.18μmプロセスで製造され、少ない[トランジスタ](../Page/トランジスタ.md "wikilink")数で構成されているためダイサイズが小さく、配線もワイヤーボンディングを採用している。このため、競合製品に対し安価かつ低消費電力を実現できるという点をメリットとしており、省電力技術**Long Haul**もサポートする。 Samuelコアを搭載したCPUは **Cyrix III**のブランドで販売されたが、後にはSamuelコアを搭載しながらVIA C3のプリントがされた製品も出回った。

### Joshua

**Joshua**（ヨシュア）はGobiコアをベースとして開発されていたCPUコアである。 ナショナルセミコンダクターの0.18μmプロセスで製造され、2.2Vのコア電圧で動作する。7段のパイプラインに加え、64KBのL1キャッシュと256KBのL2キャッシュを搭載。マルチメディア拡張命令として3DNow\!をサポートする。

対応プラットフォームは[FSB](../Page/フロントサイドバス.md "wikilink")133MHzの[Socket 370互換であるとされ](https://ja.wikipedia.org/wiki/Socket_370 "wikilink")、旧[サイリックス](../Page/サイリックス.md "wikilink")の製品同様に性能指標は実クロックで表記ではなく[PRレート](https://ja.wikipedia.org/wiki/PRレート "wikilink")の採用を予定していた。

JoshuaのキャンセルについてはCyrixチームメンバの大量離職や、実クロックの高い製品を望んだVIAの戦略などの噂が存在するが、正式な発表は一切されておらず不明である。Joshua以降、Cyrixチームによる製品は発表されていない。

## C3

[thumb](https://ja.wikipedia.org/wiki/画像:Via_c3_ezra_866amhz.jpg "wikilink") **C3**はVIAが[2001年](../Page/2001年.md "wikilink")に発表したCPU製品である。CyrixIIIの後継製品であり、VIA Cシリーズのファーストモデルとなる。CyrixIIIの特徴をほぼ引き継いでいるが、コアの改良に伴う基本性能向上や、低発熱・低消費電力である点やC3を搭載して発売された[Mini-ITX](../Page/Mini-ITX.md "wikilink")プラットフォームが[自作PC](https://ja.wikipedia.org/wiki/自作PC "wikilink")市場および組込市場で評価されるようになり、x86 CPU市場において一定の地位を築くことに成功した。

C3は[2006年](../Page/2006年.md "wikilink")[3月](https://ja.wikipedia.org/wiki/3月 "wikilink")インテルとのP6バスライセンス契約が完了したことに伴い製造終了しており、後継製品としてVIA独自のV4バスを採用したC7に移行している。

C3をアピールするキャッチコピーとして**Cool Processing**がアピールされていた。

### Samuel2 (C5B)

**Samuel2**（サミュエル ツー）は、Samuelを0.15μmにシュリンクし64kBのL2キャッシュを追加した製品である。またLongHaulもv2に改良されている。従来のCyrixIIIでは基本的に3.0倍から8.0倍までの動作倍率設定しか持たなかったが、C3では最高12.0倍まで引き上げられた。

追加されたL2キャッシュは小容量であるもののL1キャッシュとの排他式であるため[Celeronに比べてL](https://ja.wikipedia.org/wiki/Celeron#Pentium_II、Pentium_III世代のCeleron（P6_Celeron） "wikilink")2キャッシュを高効率での使用が可能である。このため、整数演算を多用するオフィス系のアプリケーションなどでは競合製品に対抗できるようになった。しかし、半分のクロック周波数で動作するFPUなどは変わらず、全体のパフォーマンスとしては競合製品に及ばなかった。

VIAはこのSamuel2の製品投入の頃にブランド名を**C3**に変更した。ただしSamuel2のサンプルが登場した時に従来のSamuelとは異なる新たなマーキングデザインに変更されたにもかかわらず"Cyrix III"と小さくプリントされており、当初はSamuel2のブランド名はCyrix IIIで変わらないと説明されていた\[1\]。その後このデザインがSamuelにも逆輸入されていることから、コアの変更とマーキングのデザイン変更は特に関係が無かったと考えられている\[2\]。その一方で、Samuel2の正式出荷前に"C3"という新たなブランド名が発表されており、初期ロットのSamuel2(Cyrix III)はマーキングデザインを"C3"の表記に変更する時間が無かったとも解釈されている\[3\]。

### Ezra (C5C)

**Ezra**（エズラ）はSamuel2の製造プロセスを0.13μmにシュリンクした製品である。微細化に伴いコア電圧が1.35Vに引き下げられ、動作クロックの向上が図られた。ただしダイサイズはSamuel2から変更されていない。特に大きな変更がないためか、名称がSamuel2(C5B)からEzra(C5C)に変更されているにも関わらずCPUIDはSamuel2が670，Ezraが678で、MODEL IDは7のまま変わらっておらず、STEPPING IDのみ0から8に変更されている。

[菓子箱を意匠したリテールパッケージ](https://akiba-pc.watch.impress.co.jp/hotline/20010915/c3kan.html)が販売され話題となった。

### Ezra-T (C5M/C5N)

**Ezra-T**（エズラ・ティー）はEzraのシステムバスをPentium III([Tualatin](https://ja.wikipedia.org/wiki/Pentium_III#第三世代“テュアラティン”_\(Tualatin\) "wikilink"))で採用されている[AGTLに対応させた製品である](https://ja.wikipedia.org/wiki/GTL_\(デジタル回路\) "wikilink")。CPGAパッケージの製品では表面にキャパシタが追加される変更が行われた。それ以外の大きな変更は無い。

内部的にはLongHaulもバージョンアップしており、新たに追加されたMSR 0x110Aを使った新機能はPowerSaverと名付けられた。設定可能なBFが4bit (BF0 - BF3) から5bit (BF0 - BF4) に拡張されており、最高で16.0倍まで動作倍率の設定が可能になった。

### Nehemiah

**Nehemiah**（ネヘミア、またはニアマイア）はSamuelコアのマイナーチェンジであり続けた従来製品から大幅に改良が行われたC3プロセッサのコアである。単にNehemiahと呼称されるコアは複数のモデルが存在する。

[後述のように](https://ja.wikipedia.org/wiki/#脆弱性 "wikilink")、2018年になって脆弱性が発見された。ただ、Nehemiahコアは組み込み機器としての利用が主流であり、影響は限定的と見られている\[4\]。

#### C5XL

[thumb](https://ja.wikipedia.org/wiki/画像:VIA_C3_C5XL_CPGA.jpg "wikilink") **C5XL**はNehamiahコアとして最初に投入された製品であり、変更点として以下が挙げられる。

  - [パイプラインステージ数を](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")12から16に増加
  - FPUのフルスピード化
  - [3DNow\!](../Page/3DNow!.md "wikilink")のサポートを廃止し、[SSEユニットを搭載](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE "wikilink")。これによりMMXとSSEの同時処理が可能となった。
  - L2キャッシュを4ウェイ[セットアソシエイティブから](https://ja.wikipedia.org/wiki/キャッシュメモリ#構成 "wikilink")16ウェイセットアソシエイティブに変更
  - 2つのハードウェア[乱数発生器の追加](../Page/乱数列.md "wikilink")。複数のfree running発振器を組み合わせて[量子](https://ja.wikipedia.org/wiki/量子 "wikilink")的な振る舞いを持つビット列を生成させている。\[5\]
  - Ezra-TまでのコアがサポートしていなかったCMOV命令を追加しi686完全互換化。
  - 従来のLongHaulとの互換性を廃止し、省電力機能はPowerSaverに一本化。動作倍率の設定は3.0倍と3.5倍が廃止され、最低動作倍率が4.0倍に底上げされた。

また、CPGAパッケージの製品ではEzra-Tよりもさらに[キャパシタが追加され](../Page/コンデンサ.md "wikilink")、マーキングされるロゴデザインも若干の変更がされた。しかしその後、アナウンスが無いままキャパシタがEzra-Tと同じ数に戻された。

#### C5P

[thumb](https://ja.wikipedia.org/wiki/画像:VIA_Processor_Miniaturization_image.jpg "wikilink") **C5P** はC5XLの改良モデルであり、C5XLから以下の改良が施されている。

  - [APIC](../Page/APIC.md "wikilink")に対応し、デュアルCPUが可能となった。VIAからはNehemiahを2個搭載した製品も[発売された。](http://www.watch.impress.co.jp/akiba/hotline/20050917/etc_vt310dp.html)
  - 200MHz [FSBのサポート](../Page/フロントサイドバス.md "wikilink")
  - ハードウェア[AES高速化機能](../Page/Advanced_Encryption_Standard.md "wikilink")**Pad Lock**のサポート
  - コア電圧を0.90 - 1.00への引き下げ
  - ダイサイズ47[mm<sup>2</sup>の](https://ja.wikipedia.org/wiki/平方ミリメートル "wikilink")[BGAパッケージ](https://ja.wikipedia.org/wiki/集積回路#BGA_\(Ball_Grid_Array\) "wikilink")
  - パッケージサイズが15mm×15mmのnanoBGAパッケージ

nanoBGAパッケージは、サイズゆえに配線の取り回しが難しく、nanoBGA対応[マザーボード](../Page/マザーボード.md "wikilink")を小規模なメーカーが設計するのに問題があり製造中止になった。

#### C5X

VIAは当初、Nehemiah世代のC3の上位モデルとして**C5X**の投入も予定していた。 これは、C5XLでの改良に加えて、命令デコード，[MMX](../Page/MMX.md "wikilink")ユニット，[SSEユニット](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE "wikilink")，整数演算ユニットの複数命令同時処理を可能とし、L2キャッシュを256kB 16ウェイセットアソシエイティブに増加させる予定であったが、C5Xはキャンセルされ製品が発売されることはなかった。

## 派生品

[thumb](https://ja.wikipedia.org/wiki/画像:Via_c3e_ezrat_933amhz.jpg "wikilink")

### Eden / C3-E

**Eden**（エデン）および**C3-E**（シースリー・イー）はBGAパッケージを採用した組込み向け製品のブランド名である。コア自体はいずれもC3プロセッサと同等で共通であるが、ファンレスのものを特にEdenプロセッサと称している。  なおEdenのブランド自体は、C3後継のC7コアを用いた組込み向けファンレス製品にも引き続き使用されている。

### Cyrix III Mobile

**Cyrix III Mobile**（サイリックススリー・モバイル）はSamuelコアのCyrixIIIをベースとして[2000年](../Page/2000年.md "wikilink")に発表されたモバイルCPU。プラットフォームには[Socket 370を採用し](https://ja.wikipedia.org/wiki/Socket_370 "wikilink")、省電力技術Long HaulによりPerformance ModeとPower Saving Modeの切替が可能であり、CyrixIIIより50%の消費電力削減と小型化を実現したとされたが、採用例は確認されていない。

### Mobile C3

**Mobile C3**（モバイル・シースリー）はEzraコアをベースとして[2001年](../Page/2001年.md "wikilink")に発表されたモバイルCPU。デスクトップ向けと共通の[Socket 370対応CPGAパッケージを採用した製品の他にEBGAパッケージおよびMicroPGAパッケージを採用した製品の](https://ja.wikipedia.org/wiki/Socket_370 "wikilink")3種が存在し、コア電圧もデスクトップ版より低く抑えられている。一部の台湾メーカー製ノートPCで採用された。

### Antaur / C3-M

**Antaur**（アンター）はC5XL Nehemiahをベースとして[2003年](../Page/2003年.md "wikilink")に発表されたモバイルCPU。高さを1.5mmに抑えたEBGAパッケージでの1GHz版のみ提供された。デスクトップ版よりコア電圧を抑えるとともに省電力技術として**PowerSave 2.0**を搭載しており、[TDPは](../Page/熱設計電力.md "wikilink")11wとなっている。一部の台湾メーカー製ノートPCで採用された。

Antaurは[2005年](../Page/2005年.md "wikilink")にVIAのブランド再編に伴い**C3-M**（シースリー・エム）に改称された。

### CoreFusion

**[CoreFusion](http://www.via.com.tw/en/products/processors/luke/)**（コアフュージョン）は、C3プロセッサと[ノースブリッジ](../Page/ノースブリッジ.md "wikilink")を統合したワンチップ化した製品である。パフォーマンスメリットは無いが、サイズや重量、消費電力を重視する市場向けの製品である。 CLE266を統合した**Mark**（マーク）と、CN400を統合した**Luke**（ルーク）がラインナップされている。

### 1Giga Pro

**1Giga Pro**（ワンギガ・プロ）は[2002年](../Page/2002年.md "wikilink")に[PC Chipsから発売された](https://ja.wikipedia.org/wiki/PC_Chips "wikilink")[マザーボード](../Page/マザーボード.md "wikilink")に搭載されていたEBGA版Samuel2コアC3の[OEM](../Page/OEM.md "wikilink")版CPUである。\[6\]**1Giga**とネーミングされているが、実際には733MHzで駆動している。

## 仕様表

<table>
<thead>
<tr class="header">
<th><p>Processor</p></th>
<th><p>VIA Code</p></th>
<th><p>Centaur Code</p></th>
<th><p>周波数<br />
(MHz)</p></th>
<th><p>FSB<br />
(MHz)</p></th>
<th><p>L1<br />
キャッシュ<br />
(kB)</p></th>
<th><p>L2<br />
キャッシュ<br />
(kB)</p></th>
<th><p>FPU<br />
動作周波数</p></th>
<th><p>パイプライン<br />
ステージ数</p></th>
<th><p>Max TDP<br />
(W)</p></th>
<th><p>コア電圧<br />
(V)</p></th>
<th><p>製造プロセス<br />
(nm)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CyrixIII</p></td>
<td><p>Joshua</p></td>
<td><p>―</p></td>
<td><p>(PR)433-533</p></td>
<td><p>66/100/133</p></td>
<td><p>64</p></td>
<td><p>256</p></td>
<td><p>100%</p></td>
<td><p>7</p></td>
<td><p>不明</p></td>
<td><p>2.2</p></td>
<td><p>180</p></td>
</tr>
<tr class="even">
<td><p>CyrixIII</p></td>
<td><p>Samuel</p></td>
<td><p>C5A</p></td>
<td><p>500-667</p></td>
<td><p>100/133</p></td>
<td><p>128</p></td>
<td><p>0</p></td>
<td><p>50%</p></td>
<td><p>12</p></td>
<td><p>8.5</p></td>
<td><p>1.9-2.0</p></td>
<td><p>180 Al</p></td>
</tr>
<tr class="odd">
<td><p>C3</p></td>
<td><p>Samuel2</p></td>
<td><p>C5B</p></td>
<td><p>700-800</p></td>
<td><p>100/133</p></td>
<td><p>128</p></td>
<td><p>64</p></td>
<td><p>50%</p></td>
<td><p>12</p></td>
<td><p>12</p></td>
<td><p>1.6-1.65</p></td>
<td><p>150 Al</p></td>
</tr>
<tr class="even">
<td><p>C3</p></td>
<td><p>Ezra</p></td>
<td><p>C5C</p></td>
<td><p>800-950</p></td>
<td><p>100/133</p></td>
<td><p>128</p></td>
<td><p>64</p></td>
<td><p>50%</p></td>
<td><p>12</p></td>
<td><p>15</p></td>
<td><p>1.35</p></td>
<td><p>150/130 Al</p></td>
</tr>
<tr class="odd">
<td><p>C3</p></td>
<td><p>Ezra-T</p></td>
<td><p>C5M</p></td>
<td><p>800-950</p></td>
<td><p>100/133</p></td>
<td><p>128</p></td>
<td><p>64</p></td>
<td><p>50%</p></td>
<td><p>12</p></td>
<td><p>15</p></td>
<td><p>1.35</p></td>
<td><p>150/130 Cu</p></td>
</tr>
<tr class="even">
<td><p>C3</p></td>
<td><p>Ezra-T</p></td>
<td><p>C5N</p></td>
<td><p>800-1000</p></td>
<td><p>100/133</p></td>
<td><p>128</p></td>
<td><p>64</p></td>
<td><p>50%</p></td>
<td><p>12</p></td>
<td><p>15</p></td>
<td><p>1.35</p></td>
<td><p>130 Cu</p></td>
</tr>
<tr class="odd">
<td><p>(C3)</p></td>
<td><p>Nehemiah</p></td>
<td><p>C5X</p></td>
<td><p>1-1.4 GHz</p></td>
<td><p>133</p></td>
<td><p>128</p></td>
<td><p>256</p></td>
<td><p>100%</p></td>
<td><p>16</p></td>
<td><p>20</p></td>
<td><p>1.4-1.45</p></td>
<td><p>130 Cu</p></td>
</tr>
<tr class="even">
<td><p>C3</p></td>
<td><p>Nehemiah</p></td>
<td><p>C5XL</p></td>
<td><p>1-1.4 GHz</p></td>
<td><p>133</p></td>
<td><p>128</p></td>
<td><p>64</p></td>
<td><p>100%</p></td>
<td><p>16</p></td>
<td><p>20</p></td>
<td><p>1.4-1.45</p></td>
<td><p>130 Cu</p></td>
</tr>
<tr class="odd">
<td><p>C3</p></td>
<td><p>Nehemiah</p></td>
<td><p>C5P</p></td>
<td><p>1-1.4 GHz</p></td>
<td><p>133/200</p></td>
<td><p>128</p></td>
<td><p>64</p></td>
<td><p>100%</p></td>
<td><p>16</p></td>
<td><p>20</p></td>
<td><p>1.4-1.45</p></td>
<td><p>130 Cu</p></td>
</tr>
</tbody>
</table>

## CyrixIII/C3シリーズの設計思想

CyrixIIIおよびC3は、競合製品よりも絶対的な性能やクロックでは劣るが、それよりもはるかに小さく、安価に製造でき、かつ[省電力であることを特徴としている](../Page/省エネルギー.md "wikilink")。このことによって組み込みシステム市場にアピールする製品となった。

  - メモリ性能は多くのベンチマークで性能を左右する要因であるので、VIAプロセッサは様々な機能強化の中でも、大きなL1キャッシュと大きなTLB、積極的な[プリフェッチ](../Page/プリフェッチ.md "wikilink")を実装している。これらの機能はVIA独自のものではないが、ダイサイズを抑えるためにメモリアクセスを最適化する機能を削減していない。 128kBあるL1キャッシュは常にCentaur/VIA設計の一つの特徴となっている。

<!-- end list -->

  - クロック周波数は、一般的な言葉では1サイクル当たりに処理できる命令数が増加する以上のものとして捉えられている。[アウト・オブ・オーダー実行](../Page/アウト・オブ・オーダー実行.md "wikilink")のような複雑な機能の実装を選択していない。これは、複雑な論理を実装するためにクロック周波数の向上が難しく、また、余分なダイサイズ増加や消費電力の増加などのデメリットがあり、その割にいくつかの種類のアプリケーションではほとんどパフォーマンスは上がらないからである。後にIntelが開発した[Atomも](../Page/Intel_Atom.md "wikilink")、同様の設計思想を踏襲している。

<!-- end list -->

  - パイプラインは、x86命令の中でもよく使われる[レジスタ](../Page/レジスタ_\(コンピュータ\).md "wikilink") - メモリ間、メモリ - レジスタ間の形式の命令は、1クロックで実行できるように調整されている。いくつかのよく使われる命令は、他のx86プロセッサと比較して少ないクロック数で実行する。

<!-- end list -->

  - あまり使われないx86命令は[マイクロコードで実装されるか他の命令で](../Page/マイクロプログラム方式.md "wikilink")[エミュレートされている](../Page/エミュレータ_\(コンピュータ\).md "wikilink")。これによりダイサイズが節約でき、消費電力が抑えられている。実際に使われている主要なアプリケーションでの影響は最小限である。

<!-- end list -->

  - これらの設計方針は元々の[RISC](../Page/RISC.md "wikilink")の主張から派生したものである。つまり、より小さな命令セット、よりよい最適化がCPU全体の性能を速くすることにつながる。

<!-- end list -->

  - C3/CyrixIIIは互換CPUであるにもかかわらず、Samuel2コア以降ではL1より少ないL2キャッシュ搭載という、Intel純正CPUには存在しなかったキャッシュ構成を取っている。しかしデータシートによればSamuel2以降でも「*互換性のために (For compatibility,)*」L2キャッシュ非搭載を示す L2 Hardware Disable ビットが常に立っており、結果的にBIOS側から判断されるキャッシュ構成は[CovingtonコアのCeleronと似た状態になっている](https://ja.wikipedia.org/wiki/Intel_Celeron#Covington "wikilink")。

## CyrixIII/C3シリーズの採用例

CyrixIIIは小規模PCメーカーの低価格機種で採用したモデルも発表されている\[7\]ものの、大規模な採用例はVIA自身も発表しておらず、プロセッサ市場における存在感は極めて希薄であった。

ブランド名がC3に変更されて以降も大手メーカーのPC製品に採用された例は無かったが、[ウォルマート](../Page/ウォルマート.md "wikilink")\[8\]や[イーヤマ](https://ja.wikipedia.org/wiki/イーヤマ "wikilink")\[9\]といった量販系企業の超低価格PCに採用されるなどし、メーカー製PC市場でもある程度の存在感は示した。

また組込市場では、[ソニー](../Page/ソニー.md "wikilink")の[ブロードバンドルーター](../Page/ルーター.md "wikilink")\[10\]や[富士通](../Page/富士通.md "wikilink")の[シンクライアント](../Page/シンクライアント.md "wikilink")\[11\]、[日立製作所](../Page/日立製作所.md "wikilink")のHDDビデオレコーダ\[12\]などに採用された。

C3によってVIAは大手メーカーとの採用実績を作り、CPUビジネスを軌道に乗せることに成功した。

## CyrixIII/C3のエピソード

x86 CPU市場では新規参入となるVIAでは他社製品ではあまり見かけないユニークな動きが見られることがしばしばある。以下に例を挙げる。

### 発表内容と製品仕様の違い

  - Cyrix IIIはCyrixチームのJoshuaコアを搭載した製品として正式に発表されたが、実際に登場したCyrix IIIではCentaurチームのSamuelコアが搭載されていた。
  - Samuel2コアを搭載するC3はヒートスプレッダ無しのCPGAパッケージ製品として発表されたが、実際に登場したC3は当初CyrixIIIと全く同じヒートスプレッダ付のパッケージで、しかもCyrixIIIのマーキングがされていた。この為、667MHzなどSamuelとSamuel2で重複するクロックモデルにおいては、区別の為にSamuel2コアの製品には667**A**MHzというように、クロックにAを付与する措置が取られた。その後、マーキングはC3に変更されたがパッケージはCyrixIIIと同じものが使用され続けた。
  - Ezraコアを搭載するC3 800AMHzはコア電圧1.30Vとして発表されていたが、実際に登場した製品はコア電圧1.35Vであった。また正式なリテールパッケージ品にも関わらず初期のロットでは[エンジニアリングサンプル](https://ja.wikipedia.org/wiki/エンジニアリングサンプル "wikilink")品が使用されていた。
  - Ezraコアの発表当時、800MHzなど一部のクロックモデルではSamuel2とEzraが重複するため、区別の為にEzraコアの製品には800**A**MHzというように、クロックにAを付与することで区別すると発表した。しかし実際にはその後も大量に流通したSamuel2 の800MHz版においても800**A**MHzの表記が使用され、コア電圧を確認しないと区別できない状態となった。

### その他

  - 最初に発表されたCyrixチーム設計のJoshuaを搭載したCyrixIIIのイメージから、CyrixIII/C3はCyrixの流れの製品であると紹介されることが多かった。実際に広く流通した製品はCyrixIII/C3ともに全て、Centaur設計のWinChipの流れを汲む製品である。
  - Ezraコア以降のパッケージでは裏面にブリッジが追加され、このブリッジのオープン・クローズを操作することでFSBやクロック倍率を自由に操作することが可能である。
  - Ezraコアでは3種の缶パッケージが存在する。最初に登場したのは菓子缶をイメージし原材料名や内容量、「食べられません」などの注意書きをもじった日本語版のパッケージだが、後によりシンプルになった英語版のパッケージに変更された。また[2002 FIFAワールドカップをイメージした缶パッケージが存在する](../Page/2002_FIFAワールドカップ.md "wikilink")。Nehemiah以降では英語版パッケージのみが使用された。
  - 組込向けのEBGA製品について当初はファンレス製品をEDEN、ファン冷却必要な製品をC3-Eとすると発表していた。しかし市場ではどちらもEDENとして扱われることが非常に多く、混乱が見られた。
  - EzraコアのC3ではCPUクーラーを外した状態で負荷をかけ続けるデモムービーがWebで公開された。競合製品が数秒でフリーズしたのに対し、C3は24時間以上の稼動を続け話題となった。
  - 当初発売されたC5XL Nehemiah製品は表面のキャパシタがEzra-Tより増加されていたが、後にアナウンス無くEzra-Tと同じに戻された。その為、一部ショップではC5XL Nehemiahの製品をEzra-Tと誤認するなどの混乱を生じた。

## 脆弱性

2018年8月、C3のNehemiahコアにおいて[バックドア](../Page/バックドア.md "wikilink")の脆弱性が発見されたことが報告された\[13\]\[14\]。

CyrixIII/C3にはもともとx86コアとは別に、非x86の独自[コプロセッサ](../Page/コプロセッサ.md "wikilink")が内蔵されている。そちらを操作する隠し命令セット「Alternative Instruction Set(AIS)」を利用することで、本来は高度な権限処理を伴うはずの命令を一般的な命令として実行することが可能になり、権限レベルの昇格などが行えてしまうと言われている。こうした機能は本来デバッグやテスト目的で用意されているものだが、その詳細は守秘義務を伴うもので、一般ユーザーには公開されていなかった。バックドアの発見はその機能を利用したものと考えられている\[15\]。

C3においてMSR 0x1107\[16\]として用意されているFEATURE CONTROL REGISTER　(FCR)のビット0がトリガとなってAISが利用可能になる（実際に利用するためには、さらに起動命令を送る必要がある\[17\]）。詳細は伏せられているものの、データシートにはFCRのbit0がAIS関連機能である旨の記載はあり、この機能そのものはC5系コアであればもともと存在していたものである。ただし、このとき報告された脆弱性はNehemiahコアだけであるとされており、その他のコアで同様の問題は発生しないのか、単に見つかっていないだけなのかは不明である。

## 脚注

### 注釈

### 出典

## 関連項目

  - [VIA Technologies](../Page/VIA_Technologies.md "wikilink")
  - [VIA Eden](../Page/VIA_Eden.md "wikilink")
  - [WinChip](../Page/WinChip.md "wikilink")
  - [サイリックス](../Page/サイリックス.md "wikilink")
  - [Geode](../Page/Geode.md "wikilink")
  - [組み込みシステム](../Page/組み込みシステム.md "wikilink")

## 外部リンク

  - [VIA](http://www.viatech.co.jp/jp/index.jsp) - [VIAのプロセッサ](http://www.viatech.co.jp/jp/products/processors/)

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")

1.
2.
3.
4.
5.  [ハードウェア乱数発生器の詳細な解説](http://www.via.com.tw/en/downloads/whitepapers/initiatives/padlock/evaluation_padlock_rng.pdf)
6.  [C3相当のコアを搭載する新CPU“1Giga Pro”オンボードのマザーが発売](http://akiba.ascii24.com/akiba/news/2002/01/19/632873-000.html)
7.  [関東電子、69,800円のCyrix III 550MHz搭載PC](http://pc.watch.impress.co.jp/docs/article/20010105/logitec.htm)
8.  [「VIA C3＋LindowsOS」で、デスクトップPCが破格の$199に](https://news.mynavi.jp/news/2002/08/31/50.html)
9.  [KDV939EW/2カタログ](http://www.iiyama.co.jp/support/download/pdf/KDC%2BKDV_2002_10050A.pdf)
10. [ソニー ブロードバンドAVルータ「HN-RT1」](http://bb.watch.impress.co.jp/column/review/2003/04/09/)
11. [FMV-TC5210](http://www.fmworld.net/biz/fmv/product/hard/vtc0610/5210/)
12. [日立、400GB HDD搭載ハイブリッドレコーダ「WOOO」](http://av.watch.impress.co.jp/docs/20040415/hitachi2.htm)
13.
14.
15.
16. CyrixIII/C3の前身のIDT [WinChip](../Page/WinChip.md "wikilink")においては、ほぼ同機能のFCRレジスタがMSR 0x107に存在する。データシートに記載は無いものの、CyrixIII/C3でも互換性がある様子で、FCRはMSR 0x1107とMSR 0x107のどちらからでもアクセスできる。このため0x107を使っても同様のことができる可能性がある。なおWinChipについては、データシートによればFCRのbit 0が"Reserved"となっており、同様の機能 (AIS) が存在するのかどうかは不明。
17.