> この記事は[AMD Phenom](https://ja.wikipedia.org/wiki/AMD_Phenom)から翻訳されています。


**Phenom** （フェノム）は、[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") が発表した[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")製品のブランドの一つ。

Phenomは[AMD K10](../Page/AMD_K10.md "wikilink") マイクロアーキテクチャに基づいたデスクトップ用プロセッサで、米国時間2007年11月19日に発表された。名前の由来は「驚異的な・目を見張る」といった意味の「Phenomenal」より。稀に「ペノム」とも呼称されるが、正しくは「フェノム」である\[1\]。2009年1月より [Phenom II](https://ja.wikipedia.org/wiki/AMD_Phenom_II "wikilink") を発売した。

## 登場までの経緯

Intel の [Core 2 Quad](https://ja.wikipedia.org/wiki/Intel_Core_2#Core_2_Quad_\(デスクトップ向け\) "wikilink") によるクアッドコア ブームの折、AMD にも早急にクアッドコア CPU の発売が求められていた。[Kentsfield](https://ja.wikipedia.org/wiki/Intel_Core_2#Core_2_Quad_\(デスクトップ向け\) "wikilink") がデュアルコアの 2ダイによる「なんちゃってクアッドコア」（インテル日本法人担当談）\[2\]であるのに対し、Phenom は 4つのコアを 1ダイに収めた「真のクアッドコア」「ネイティブクアッドコア」である点を強調。「Are you "ネイティブ"?」のキャッチコピーで、対抗感を滲ませていた\[3\]。

当初はクアッドコア製品が「Phenom X4」、デュアルコア製品が「Phenom X2」と名付けられていた。しかし、出荷直前の2007年9月に急遽トリプルコア製品をラインナップに加えると発表し、クアッドコア製品は「Phenom 9000」、トリプルコア製品は「Phenom 8000」、デュアルコア製品は開発中止となり、代わりに「Athlon X2 7x50」 (Kuma) が発表された。

この世界初の x86 トリプルコア採用 CPU はPhenom 9000 シリーズのコアを 1個無効化したものとされ、歩留まりが向上すると共に価格や消費電力が低下する点をセールスポイントとした。

## 発売後の現状

後発だけあって Core 2 Quad の対抗馬として大きく注目され、発売後は各種メディアでベンチマーク比較が数多く行われたが、その結果 Core 2 Quad を超えるものではないとする評価が多勢を占めた。要因としては、完全なマルチスレッド処理となっているアプリケーションやゲームがまだ僅かしかなく、Phenom が得意とする処理は従来プログラマーにとって避けるべき処理とされていたことや\[4\]、絶対的なクロック数の低さ、消費電力の高さなどが挙げられている。これにより、新製品にもかかわらず高値を付けることができず、TLB のエラッタ（後述）が発覚してからは更に値が下がる窮状となった。なお、このエラッタが解消された2008年3月からは、再び Phenom 9000 が Phenom X4 9000 に、Phenom 8000 が Phenom X3 8000 に改称された。

### TLBのエラッタ問題

K10 マイクロアーキテクチャでの最初のリビジョンである B2 では、全 CPU モデルで L2 キャッシュの不具合が原因で、L3 キャッシュ内容が特定の条件で破壊されるという、エラッタの存在が公表されている。L2 / L3 キャッシュと [Translation Lookaside Buffer](../Page/トランスレーション・ルックアサイド・バッファ.md "wikilink") (TLB) に関わる問題であり、最悪の場合、[OS](../Page/オペレーティングシステム.md "wikilink") がフリーズしたりデータが破損したりする可能性があるが、通常使用によるエラッタによっての問題の発生確率は低い\[5\]。

このエラッタを回避するには、[BIOS](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink") や OS によってモデル固有レジスタ (MSR; Model Specific Register) の設定で TLB のキャッシュを無効化するしかないが、TLB のキャッシュを無効化した場合はアプリケーション レベルで性能が 5% から 10% 低下する\[6\]。このエラッタは同じ K10 マイクロアーキテクチャを採用する Opteron でも発生し、[Barcelona](https://ja.wikipedia.org/wiki/Opteron#Barcelona（バルセロナ） "wikilink") の一時販売停止から大量出荷の延期に繋がると共に、高価格で販売できる新製品の出足を挫いた。

Phenom の発売後まもなく TLB のキャッシュを無効化するための MSR の変更を行うコードを含んだ BIOS や OS での対策が始まり、2008年3月からはエラッタを解消した B3 ステップが順次発売されている。通常、ステッピングの更新で[モデルナンバー](../Page/モデルナンバー.md "wikilink")が変更されることはないが、B3 ステップの Phenom はモデル ナンバーが 50 増加しており異例の差別化が図られた。

## ラインナップ

### Phenom X4

#### Agena (65nm SOI)

  - 4コア統合パッケージ
  - L1 キャッシュ: 64 + 64 KiB 各コア独立
  - L2 キャッシュ: 512 KiB 各コア独立
  - L3 キャッシュ: 2048 KiB 全コア共有
  - [Extended 3DNow\!](../Page/3DNow!.md "wikilink")、[SSE3](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE3 "wikilink")、[SSE4a](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE4a "wikilink")、[AMD64](https://ja.wikipedia.org/wiki/x64 "wikilink")、[Cool'n'Quiet](../Page/Cool'n'Quiet.md "wikilink")、[NXビット](../Page/NXビット.md "wikilink")、[AMD-V](https://ja.wikipedia.org/wiki/x86仮想化#AMD_virtualization_\(AMD-V\) "wikilink")
  - 対応ソケット: Socket AM2+

### Phenom X3

#### Toliman (65nm SOI)

  - 3コア統合パッケージ
  - L1 キャッシュ: 64 + 64 KiB 各コア独立
  - L2 キャッシュ: 512 KiB 各コア独立
  - L3 キャッシュ: 2048 KiB 全コア共有
  - [Extended 3DNow\!](../Page/3DNow!.md "wikilink")、[SSE3](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE3 "wikilink")、[SSE4a](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE4a "wikilink")、[AMD64](https://ja.wikipedia.org/wiki/x64 "wikilink")、[Cool'n'Quiet](../Page/Cool'n'Quiet.md "wikilink")、[NXビット](../Page/NXビット.md "wikilink")、[AMD-V](https://ja.wikipedia.org/wiki/x86仮想化#AMD_virtualization_\(AMD-V\) "wikilink")
  - 対応ソケット: Socket AM2+

### 一覧

<table>
<thead>
<tr class="header">
<th><p>モデル</p></th>
<th><p>動作周波数<br />
(GHz)</p></th>
<th><p>L2 キャッシュ<br />
(KiB)</p></th>
<th><p>L3 キャッシュ<br />
(MiB)</p></th>
<th><p>ステッピング</p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">TDP</a><br />
(W)</p></th>
<th><p><a href="../Page/HyperTransport.md" title="wikilink">HyperTransport</a><br />
</p></th>
<th><p>発売時期</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Phenom X4 9000 シリーズ (Agena)</strong></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Phenom X4 9950 Black Edition</p></td>
<td><p>2.60</p></td>
<td><p>512 x 4</p></td>
<td><p>2.0</p></td>
<td><p>B3</p></td>
<td><p>140/125</p></td>
<td><p>2000 MHz<br />
(4000 MT/s)</p></td>
<td><p>2008年7月/9月</p></td>
</tr>
<tr class="odd">
<td><p>Phenom X4 9850 Black Edition</p></td>
<td><p>2.50</p></td>
<td><p>512 x 4</p></td>
<td><p>2.0</p></td>
<td><p>B3</p></td>
<td><p>125</p></td>
<td><p>2000 MHz<br />
(4000 MT/s)</p></td>
<td><p>2008年3月</p></td>
</tr>
<tr class="even">
<td><p>Phenom X4 9750</p></td>
<td><p>2.40</p></td>
<td><p>512 x 4</p></td>
<td><p>2.0</p></td>
<td><p>B3</p></td>
<td><p>125/95</p></td>
<td><p>1800 MHz<br />
(3600 MT/s)</p></td>
<td><p>2008年3月</p></td>
</tr>
<tr class="odd">
<td><p>Phenom X4 9650</p></td>
<td><p>2.30</p></td>
<td><p>512 x 4</p></td>
<td><p>2.0</p></td>
<td><p>B3</p></td>
<td><p>95</p></td>
<td><p>1800 MHz<br />
(3600 MT/s)</p></td>
<td><p>2008年4月</p></td>
</tr>
<tr class="even">
<td><p>Phenom 9600</p></td>
<td><p>2.30</p></td>
<td><p>512 x 4</p></td>
<td><p>2.0</p></td>
<td><p>B2</p></td>
<td><p>95</p></td>
<td><p>1800 MHz<br />
(3600 MT/s)</p></td>
<td><p>2007年11月</p></td>
</tr>
<tr class="odd">
<td><p>Phenom 9600 Black Edition</p></td>
<td><p>2.30</p></td>
<td><p>512 x 4</p></td>
<td><p>2.0</p></td>
<td><p>B2</p></td>
<td><p>95</p></td>
<td><p>1800 MHz<br />
(3600 MT/s)</p></td>
<td><p>2007年12月</p></td>
</tr>
<tr class="even">
<td><p>Phenom X4 9550</p></td>
<td><p>2.20</p></td>
<td><p>512 x 4</p></td>
<td><p>2.0</p></td>
<td><p>B3</p></td>
<td><p>95</p></td>
<td><p>1800 MHz<br />
(3600 MT/s)</p></td>
<td><p>2008年4月</p></td>
</tr>
<tr class="odd">
<td><p>Phenom 9500</p></td>
<td><p>2.20</p></td>
<td><p>512 x 4</p></td>
<td><p>2.0</p></td>
<td><p>B2</p></td>
<td><p>95</p></td>
<td><p>1800 MHz<br />
(3600 MT/s)</p></td>
<td><p>2007年11月</p></td>
</tr>
<tr class="even">
<td><p>Phenom X4 9350e</p></td>
<td><p>2.00</p></td>
<td><p>512 x 4</p></td>
<td><p>2.0</p></td>
<td><p>B3</p></td>
<td><p>65</p></td>
<td><p>1800 MHz<br />
(3600 MT/s)</p></td>
<td><p>2008年7月</p></td>
</tr>
<tr class="odd">
<td><p>Phenom X4 9150e</p></td>
<td><p>1.80</p></td>
<td><p>512 x 4</p></td>
<td><p>2.0</p></td>
<td><p>B3</p></td>
<td><p>65</p></td>
<td><p>1600 MHz<br />
(3200 MT/s)</p></td>
<td><p>2008年7月</p></td>
</tr>
<tr class="even">
<td><p>Phenom X4 9100e</p></td>
<td><p>1.80</p></td>
<td><p>512 x 4</p></td>
<td><p>2.0</p></td>
<td><p>B2</p></td>
<td><p>65</p></td>
<td><p>1600 MHz<br />
(3200 MT/s)</p></td>
<td><p>2008年4月</p></td>
</tr>
<tr class="odd">
<td><p><strong>Phenom X3 8000 シリーズ (Toliman)</strong></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Phenom X3 8850 Black Edition</p></td>
<td><p>2.50</p></td>
<td><p>512 x 3</p></td>
<td><p>2.0</p></td>
<td><p>B3</p></td>
<td><p>95</p></td>
<td><p>1800 MHz<br />
(3600 MT/s)</p></td>
<td><p>2008年10月</p></td>
</tr>
<tr class="odd">
<td><p>Phenom X3 8750</p></td>
<td><p>2.40</p></td>
<td><p>512 x 3</p></td>
<td><p>2.0</p></td>
<td><p>B3</p></td>
<td><p>95</p></td>
<td><p>1800 MHz<br />
(3600 MT/s)</p></td>
<td><p>2008年4月</p></td>
</tr>
<tr class="even">
<td><p>Phenom X3 8700</p></td>
<td><p>2.40</p></td>
<td><p>512 x 3</p></td>
<td><p>2.0</p></td>
<td><p>B2</p></td>
<td><p>95</p></td>
<td><p>1800 MHz<br />
(3600 MT/s)</p></td>
<td><p>2008年3月</p></td>
</tr>
<tr class="odd">
<td><p>Phenom X3 8650</p></td>
<td><p>2.30</p></td>
<td><p>512 x 3</p></td>
<td><p>2.0</p></td>
<td><p>B3</p></td>
<td><p>95</p></td>
<td><p>1800 MHz<br />
(3600 MT/s)</p></td>
<td><p>2008年4月</p></td>
</tr>
<tr class="even">
<td><p>Phenom X3 8600</p></td>
<td><p>2.30</p></td>
<td><p>512 x 3</p></td>
<td><p>2.0</p></td>
<td><p>B2</p></td>
<td><p>95</p></td>
<td><p>1800 MHz<br />
(3600 MT/s)</p></td>
<td><p>2008年3月</p></td>
</tr>
<tr class="odd">
<td><p>Phenom X3 8450</p></td>
<td><p>2.10</p></td>
<td><p>512 x 3</p></td>
<td><p>2.0</p></td>
<td><p>B3</p></td>
<td><p>95</p></td>
<td><p>1800 MHz<br />
(3600 MT/s)</p></td>
<td><p>2008年4月</p></td>
</tr>
<tr class="even">
<td><p>Phenom X3 8450e</p></td>
<td><p>2.10</p></td>
<td><p>512 x 3</p></td>
<td><p>2.0</p></td>
<td><p>B3</p></td>
<td><p>65</p></td>
<td><p>1800 MHz<br />
(3600 MT/s)</p></td>
<td><p>2008年9月</p></td>
</tr>
<tr class="odd">
<td><p>Phenom X3 8400</p></td>
<td><p>2.10</p></td>
<td><p>512 x 3</p></td>
<td><p>2.0</p></td>
<td><p>B2</p></td>
<td><p>95</p></td>
<td><p>1800 MHz<br />
(3600 MT/s)</p></td>
<td><p>2008年3月</p></td>
</tr>
<tr class="even">
<td><p>Phenom X3 8250e</p></td>
<td><p>1.90</p></td>
<td><p>512 x 3</p></td>
<td><p>2.0</p></td>
<td><p>B3</p></td>
<td><p>65</p></td>
<td><p>1800 MHz<br />
(3600 MT/s)</p></td>
<td><p>2008年9月</p></td>
</tr>
</tbody>
</table>

## 脚注

<div class="references-small">

</div>

## 外部リンク

  - [AMD Phenom™](http://www.amd.com/jp-ja/Processors/ProductInformation/0,,30_118_15331,00.html)
  - [Revision Guide for AMD Family 10h Processors](http://www.amd.com/us-en/assets/content_type/white_papers_and_tech_docs/41322.pdf) - AMD によるエラッタに関する PDF ドキュメント

[Category:AMDのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:AMDのマイクロプロセッサ "wikilink")

1.  [ペノム【ぺのむ】](http://plusd.itmedia.co.jp/pcuser/articles/0802/22/news033.html) 古田雄介＆ITmedia アキバ取材班
2.
3.
4.
5.
6.