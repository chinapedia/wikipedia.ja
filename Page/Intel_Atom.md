> この記事は[Intel Atom](https://ja.wikipedia.org/wiki/Intel_Atom)から翻訳されています。


**Intel Atom**（インテル アトム、以下 "Atom"）は、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が[設計](../Page/設計.md "wikilink")・[製造する](../Page/製造業.md "wikilink")、主に[携帯情報端末](../Page/携帯情報端末.md "wikilink") (PDA) や低価格[PC](../Page/パーソナルコンピュータ.md "wikilink")、[組込みシステム](https://ja.wikipedia.org/wiki/組込みシステム "wikilink")向けの[マイクロアーキテクチャ](../Page/マイクロアーキテクチャ.md "wikilink")及び[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")群である。

Atomは、インテルの製品分類でも特に低[消費電力](https://ja.wikipedia.org/wiki/消費電力 "wikilink")化が図られた[LPIAと呼ばれるカテゴリに属している](https://ja.wikipedia.org/wiki/インテル#LPIA "wikilink")。LPIA製品としては[マイクロアーキテクチャ](../Page/マイクロアーキテクチャ.md "wikilink")から新規に開発された初めての製品である。米国時間[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")3月2日に発表され、その年の夏から順次出荷されている。

近年は [Intel 64](https://ja.wikipedia.org/wiki/x64#Intel_64 "wikilink") に対応しているが、初期の製品に64ビット非対応で [IA-32](../Page/IA-32.md "wikilink") の物もあった。[メインストリーム](https://ja.wikipedia.org/wiki/メインストリーム "wikilink")の製品との[差別化](https://ja.wikipedia.org/wiki/差別化 "wikilink")のためか、64ビットと同時に[VTに対応したモデルは以前は無かったが](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink")、近年は[サーバ](../Page/サーバ.md "wikilink")向けとしてそのようなラインナップも現れた。

## 概要

過去には、インテルのモバイル・組込み向けプロセッサは[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")ではなく、[DECから買収した](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[StrongARM](../Page/StrongARM.md "wikilink")と、その発展型を[XScale](../Page/XScale.md "wikilink")[ブランド](../Page/ブランド.md "wikilink")で販売していた。XScaleは[携帯情報端末](../Page/携帯情報端末.md "wikilink")や[組込みシステム](https://ja.wikipedia.org/wiki/組込みシステム "wikilink")に採用され、多くの[Pocket PCで使われた](../Page/Pocket_PC.md "wikilink")。

当時のx86は、競合していた[ARMと比べて](../Page/ARMアーキテクチャ.md "wikilink")[回路規模や](https://ja.wikipedia.org/wiki/集積回路#プロセスルール "wikilink")[クロック](../Page/クロック.md "wikilink")周波数の高さから[消費電力](https://ja.wikipedia.org/wiki/消費電力 "wikilink")が大きく、[パッケージも大きかったため](../Page/パッケージ_\(電子部品\).md "wikilink")、小型化や低消費電力が求められるモバイル機器向けや組込み用途にはあまり採用されていなかった。しかし、[ソフトウェア](../Page/ソフトウェア.md "wikilink")の開発環境では、x86の豊富な[開発ツールや](https://ja.wikipedia.org/wiki/プログラミングツール "wikilink")[プログラミング技術者の層の厚さといった有利な面があり](../Page/プログラマ.md "wikilink")、その後の半導体[プロセスや](https://ja.wikipedia.org/wiki/集積回路#プロセス・ルール "wikilink")[マイクロアーキテクチャ](../Page/マイクロアーキテクチャ.md "wikilink")の改良などの性能向上によって低消費電力化や小型化が行われれば、[市場](../Page/市場.md "wikilink")に受け入れられる環境は整っていた。

[2007年](../Page/2007年.md "wikilink")4月、インテルはx86ベースで低消費電力という新しいカテゴリ「[LPIA](https://ja.wikipedia.org/wiki/インテル#LPIA "wikilink")」とその第一弾のプロセッサ「[A100](https://ja.wikipedia.org/wiki/Intel_A100 "wikilink")」を発表した\[1\]。内実としては、専用に大幅な新規開発を行ったものではなく、既に販売されていた[Pentium Mマイクロアーキテクチャの第](../Page/Pentium_M.md "wikilink")2世代にあたる[Celeron M](https://ja.wikipedia.org/wiki/Celeron#Celeron_M "wikilink")（コードネーム「[Dothan-512K](https://ja.wikipedia.org/wiki/Celeron#Dothan-512K_（ドタン512K） "wikilink")」、90 nmプロセス）そのものであり、周辺チップには既存の[ICH](https://ja.wikipedia.org/wiki/I/O_コントローラー・ハブ "wikilink")7から消費電力の大きい[PCI Express](../Page/PCI_Express.md "wikilink")[インタフェースを取り除くなどしたICH](../Page/インタフェース_\(情報技術\).md "wikilink")7Uが使われていたが、XScale部門を[マーベル・テクノロジー・グループ](https://ja.wikipedia.org/wiki/マーベル・テクノロジー・グループ "wikilink")に売却した\[2\]ことなどもあり、x86によるモバイル・組込み機器の発展の端緒となった。インテルはこれに続けて、Atomシリーズを展開した。

## マイクロアーキテクチャ

Atomでは以下の[マイクロアーキテクチャ](../Page/マイクロアーキテクチャ.md "wikilink")が使われる\[3\]。

[インテル チック・タックモデルのように](https://ja.wikipedia.org/wiki/インテル_チック・タック "wikilink")、機能強化を図る世代と単にシュリンクする世代を交互に繰返すという計画が発表されていたが、実際はそのようには推移していなく、Silvermont で機能強化が行われた。

<table>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>プロセスルール</p></th>
<th><p>採用</p></th>
<th><p>特徴</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Bonnell<br />
(ボンネル)</p></td>
<td><p>45nm</p></td>
<td><p>Diamondville, Menlow, Pine Trail, Moorestown, Oak Trail</p></td>
<td><p>In Order型、最大2コア</p></td>
</tr>
<tr class="even">
<td><p>Saltwell<br />
(ソルトウェル)</p></td>
<td><p>32nm</p></td>
<td><p>Cedar Trail, Centerton, Briarwood, Medfield, Clover Trail, Clover Trail+</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Silvermont<br />
(シルバーモント)</p></td>
<td><p>22nm</p></td>
<td><p>Avoton, Rangeley, Bay Trail, Merrifield, Moorefield</p></td>
<td><p><a href="../Page/アウト・オブ・オーダー実行.md" title="wikilink">Out of Order型</a>、最大8コア、<a href="https://ja.wikipedia.org/wiki/AES-NI" title="wikilink">AES-NI</a>、<a href="../Page/ストリーミングSIMD拡張命令.md" title="wikilink">SSE</a> 4.1/4.2</p></td>
</tr>
<tr class="even">
<td><p>Airmont<br />
(エアーモント)</p></td>
<td><p>14nm</p></td>
<td><p>Braswell, Cherry Trail</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Goldmont<br />
(ゴールドモント)</p></td>
<td><p>Apollo Lake, Denverton</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Goldmont Plus<br />
(ゴールドモントプラス)</p></td>
<td><p>Gemini Lake</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

2016年5月にGoldmontに基づくスマートフォン/タブレット向けのBroxtonの廃止が発表になり\[4\]、タブレットPC向けのWillow Trailも廃止になり\[5\]、Joule は発表から10ヶ月で製造終了した。

## Bonnell マイクロアーキテクチャ

第1世代のAtom向けマイクロアーキテクチャである。[実装](../Page/実装.md "wikilink")している[命令セット](../Page/命令セット.md "wikilink")は[Intel Core 2と互換であるとされ](../Page/Intel_Core_2.md "wikilink")、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")命令、[x87命令](../Page/Intel_8087.md "wikilink")、そして[MMX](../Page/MMX.md "wikilink")、[SSE](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE "wikilink")、[SSE2](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE2 "wikilink")、[SSE3](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE3 "wikilink")、[SSSE3などの拡張命令を搭載している](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSSE3 "wikilink")。製品により、[Intel 64や](https://ja.wikipedia.org/wiki/x64 "wikilink")[Intel VT](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink")、[ハイパースレッディング・テクノロジー](../Page/ハイパースレッディング・テクノロジー.md "wikilink")、[EIST](https://ja.wikipedia.org/wiki/Intel_SpeedStep_テクノロジ#拡張版_Intel_SpeedStep_テクノロジ_\(EIST\) "wikilink")、[NXビット](../Page/NXビット.md "wikilink")が利用可能な物もある。また、新しくディープパワーダウン (C6)、[スレッド別の低電力状態](../Page/スレッド_\(コンピュータ\).md "wikilink") (TCx)、CMOSバスモードなど電力管理機能が強化された\[6\]。 最初に出荷された製品は、[I/Oパッドを両サイドに配置した細長い長方形の](../Page/入出力.md "wikilink")[ダイ](../Page/ダイ.md "wikilink")・レイアウトで、製造効率が最も高いとされる正方形のダイ形状ではない。これは、ダイサイズの小さなプロセッサを[マルチコア](../Page/マルチコア.md "wikilink")化する際に有利であることから採用されたもので、その後、これを活かしたデュアルコア製品が追加された。

約4,700万個の[トランジスタ](../Page/トランジスタ.md "wikilink")により構成されており、これは当時のインテルのx86プロセッサの中では最も少ない。ダイサイズ25平方 mm未満であり、インテル史上最小のx86プロセッサとして登場した。製造には[リーク電流](../Page/リーク電流.md "wikilink")低減に有効とされる[ハフニウム](../Page/ハフニウム.md "wikilink")注入によるHigh-k（高誘電率）[ゲート絶縁膜](https://ja.wikipedia.org/wiki/ゲート絶縁膜 "wikilink")とメタルゲートによる45 nm[プロセス・ルールが採用されるなど](https://ja.wikipedia.org/wiki/集積回路#プロセス・ルール "wikilink")、省電力化が徹底されており、インテルのCPU史上最も低い[電圧](../Page/電圧.md "wikilink")で動作し、消費電力 は[VIA Eden](../Page/VIA_Eden.md "wikilink") と同等。電圧を高くすることで当面最大となる1.8G [Hz程度の動作周波数を確保し](../Page/ヘルツ.md "wikilink")、それに応じて[熱設計電力](../Page/熱設計電力.md "wikilink") (TDP) も0.6 W - 2.5 W程度と抑制された\[7\]。

刷新されたCPUコアでは電力消費低減のため、第1世代のBonnellは [アウト・オブ・オーダー実行](../Page/アウト・オブ・オーダー実行.md "wikilink")構造を捨て、イン・オーダー実行 の、比較的古いマイクロアーキテクチャに立ち返り、再設計された。

[2次キャッシュ](https://ja.wikipedia.org/wiki/2次キャッシュ "wikilink")の容量や[FSBの速度は](../Page/フロントサイドバス.md "wikilink")[Pentium 4-Mと同程度で](../Page/Pentium_4-M.md "wikilink")、実質的な処理速度でも、同クロックのWillamette・Northwoodの[Pentium 4やNorthwood](../Page/Pentium_4.md "wikilink")-256kの[Mobile Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")、Prescott-V (Prescott-256K) の[Celeron Dなどと同程度であるが](https://ja.wikipedia.org/wiki/Celeron_D "wikilink")、同クロックのZ530（[FSB](../Page/フロントサイドバス.md "wikilink")533MHz 1.6GHz TDP2.2W (HT)）とPentium 4-M（Northwood [FSB](../Page/フロントサイドバス.md "wikilink")400MHz 1.6GHz TDP46.8W）とで比較した場合、TDPは後者の約4.7%となり、エネルギー効率は格段に向上した。

このうち、[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")9月より出荷された330は、CPUパッケージに230を2個搭載させたデュアルコアモデルである\[8\]。330はまず[デスクトップパソコン](../Page/デスクトップパソコン.md "wikilink")（ネットトップ）において発売を開始、2009年6月にはネットブックへの搭載機種が発売された\[9\]。330搭載のネットトップについては消費電力が少なく、相応の性能があるため、主に超小型[ベアボーン](https://ja.wikipedia.org/wiki/ベアボーン "wikilink")やショップブランドパソコンとして発売されており、ファンレス製品もある。230と330に関しては、各社から[Mini-ITX](../Page/Mini-ITX.md "wikilink")や[マイクロATXのマザーボードに実装された状態で発売され](../Page/ATX.md "wikilink")、いずれも概ね1万円以下で入手可能である。CPUのみの交換はできないが、[自作デスクトップPCとして組み立てることが可能である](../Page/自作パソコン.md "wikilink")。

[2009年](../Page/2009年.md "wikilink")12月には、開発コードPine Trail-Dと呼ばれていた新型プロセッサD410、D510が発表された。これらの最大の特徴は、元来[ノースブリッジ](../Page/ノースブリッジ.md "wikilink")の機能だった[GPUとメモリコントローラーをCPUに統合した点にある](../Page/Graphics_Processing_Unit.md "wikilink")。これにより従来のAtomプラットフォームと比較し、平均消費電力は約20%低下したとされている\[10\]。また、従来[3D性能のもの足りなさが指摘されていたグラフィックは](../Page/3次元コンピュータグラフィックス.md "wikilink")、[GMA 950からGMA](https://ja.wikipedia.org/wiki/Intel_GMA#製品 "wikilink") 3150へと替わった。メモリスロットとメモリ総容量の少なさも解消されたことから[Windows 7に正式に対応している](../Page/Microsoft_Windows_7.md "wikilink")。2009年12月に発売された製品では、[DVIと](../Page/Digital_Visual_Interface.md "wikilink")[HDMI](https://ja.wikipedia.org/wiki/HDMI "wikilink")はサポートされていない。

### Centrino Atom

[ノートパソコン](../Page/ノートパソコン.md "wikilink")市場向けのインテルの製品ブランドの1つ[Centrino](../Page/Centrino.md "wikilink")と結び付けられた「Centrino Atom」（セントリーノ・アトム）という製品群は、低消費電力が求められるデジタル・モバイル機器などでの採用を想定していた。インテルの[ウェブサイト](../Page/ウェブサイト.md "wikilink")では、ノートパソコンと[PDAとの中間に位置する](../Page/携帯情報端末.md "wikilink")[ネットブック](https://ja.wikipedia.org/wiki/ネットブック "wikilink")や組込み機器向けとしている。CPUコアは[コードネーム](../Page/コードネーム.md "wikilink")「Bonnell」（ボンネル）と呼ばれている。Bonnellを採用した製品は複数公表されており、それぞれ対象とする市場が異なる\[11\]。

  - Silverthorne - MID（モバイル・インターネット・デバイス、Mobile Internet Device、2008年4月に米インテル社が示した新たなノートパソコンのカテゴリー）
  - Diamondville - [ネットブック](https://ja.wikipedia.org/wiki/ネットブック "wikilink")、[ネットトップ](https://ja.wikipedia.org/wiki/ネットトップ "wikilink")

Silverthorneと統合チップセット（コードネーム「Poulsbo」（ポルスボ）、System Controller Hub - SCH）を組み合わせたプラットホーム（コードネーム「Menlow」）には、インテル Centrino Atom プロセッサー・テクノロジー（Intel Centrino Atom processor technology、セントリーノ・アトム・プロセッサー・テクノロジー）というブランドネームが与えられた。しかし、2008年8月にはインテルが「Centrino Atom」ブランドの廃止を決定。「Atom」に一本化された\[12\]。

### ネットトップ・ネットブック向け

頭文字に"D"が付く製品は簡易用途デスクトップPC、いわゆるネットトップ向けである。一方"N"が付く製品はネットブック向けとなる。230と330は主にネットトップ向けだが、ネットブックにも搭載された。

#### Diamondville（ダイアモンドビル）

2008年3月に発表されたAtom第1世代の製品である。

| プロセッサーナンバー                                                                                               | 動作周波数    | コア/スレッド数 | FSB     | 2次キャッシュ  | [HT対応](../Page/ハイパースレッディング・テクノロジー.md "wikilink") | [64ビット対応](https://ja.wikipedia.org/wiki/x64 "wikilink") | [VT](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink") 対応 | [EIST](https://ja.wikipedia.org/wiki/Intel_SpeedStep_テクノロジ#拡張版_Intel_SpeedStep_テクノロジ_\(EIST\) "wikilink") | [TDP](../Page/熱設計電力.md "wikilink") | メモリ      |
| -------------------------------------------------------------------------------------------------------- | -------- | -------- | ------- | -------- | ------------------------------------------------ | ------------------------------------------------------- | ------------------------------------------------------ | --------------------------------------------------------------------------------------------------------- | ---------------------------------- | -------- |
| [230](http://ark.intel.com/ja/products/35635/Intel-Atom-Processor-230-512K-Cache-1_60-GHz-533-MHz-FSB)   | 1.60 GHz | 1C/2T    | 533 MHz | 512KB    | ○                                                | ○                                                       | ×                                                      | ×                                                                                                         | 4W                                 | DDR2-800 |
| [330](http://ark.intel.com/ja/products/35641/Intel-Atom-Processor-330-1M-Cache-1_60-GHz-533-MHz-FSB)     | 1.60 GHz | 2C/4T    | 533 MHz | 512KB x2 | ○                                                | ○                                                       | ×                                                      | ×                                                                                                         | 8W                                 | DDR2-800 |
| [N270](http://ark.intel.com/ja/products/36331/Intel-Atom-Processor-N270-512K-Cache-1_60-GHz-533-MHz-FSB) | 1.60 GHz | 1C/2T    | 533 MHz | 512KB    | ○                                                | ×                                                       | ×                                                      | ○                                                                                                         | 2.5W                               | DDR2-533 |
| [N280](http://ark.intel.com/ja/products/41411/Intel-Atom-Processor-N280-512K-Cache-1_66-GHz-667-MHz-FSB) | 1.66 GHz | 1C/2T    | 667 MHz | 512KB    | ○                                                | ×                                                       | ×                                                      | ○                                                                                                         | 2.5W                               | DDR2-667 |

#### Pine Trail（パイントレイル）

2009年5月に発表された。メモリコントローラーとグラフィックコアを統合したプロセッサ「Pineview」とチップセット「Tiger Point」を組み合わせたプラットフォーム。内蔵されたグラフィックコアは[GMA 3150](https://ja.wikipedia.org/wiki/GMA_3150 "wikilink")。[Blu-rayや](../Page/Blu-ray_Disc.md "wikilink")[H.264](../Page/H.264.md "wikilink")のアクセラレーションには対応していないので、それらにはBroadcomのCrystal HDなどの外部チップで対応することとなる。N475、N455、D525、D425はそれぞれN470、N450、D510、D410のDDR3対応版。

| プロセッサーナンバー                                                                                   | 動作周波数    | コア/スレッド数 | [DMI](https://ja.wikipedia.org/wiki/Direct_Media_Interface "wikilink") | 2次キャッシュ  | [HT対応](../Page/ハイパースレッディング・テクノロジー.md "wikilink") | [64ビット対応](https://ja.wikipedia.org/wiki/x64 "wikilink") | [VT](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink") 対応 | [EIST](https://ja.wikipedia.org/wiki/Intel_SpeedStep_テクノロジ#拡張版_Intel_SpeedStep_テクノロジ_\(EIST\) "wikilink") | [TDP](../Page/熱設計電力.md "wikilink") | メモリ      |
| -------------------------------------------------------------------------------------------- | -------- | -------- | ---------------------------------------------------------------------- | -------- | ------------------------------------------------ | ------------------------------------------------------- | ------------------------------------------------------ | --------------------------------------------------------------------------------------------------------- | ---------------------------------- | -------- |
| [D410](http://ark.intel.com/ja/products/43517/Intel-Atom-Processor-D410-512K-Cache-1_66-GHz) | 1.66 GHz | 1C/2T    | 2.5GT/s                                                                | 512KB    | ○                                                | ○                                                       | ×                                                      | ×                                                                                                         | 10W                                | DDR2-800 |
| [D425](http://ark.intel.com/ja/products/49489/Intel-Atom-processor-D425-512K-Cache-1_80-GHz) | 1.80 GHz | 1C/2T    | 2.5GT/s                                                                | 512KB    | ○                                                | ○                                                       | ×                                                      | ×                                                                                                         | 10W                                | DDR3-800 |
| [D510](http://ark.intel.com/ja/products/43098/Intel-Atom-Processor-D510-1M-Cache-1_66-GHz)   | 1.66 GHz | 2C/4T    | 2.5GT/s                                                                | 512KB x2 | ○                                                | ○                                                       | ×                                                      | ×                                                                                                         | 13W                                | DDR2-800 |
| [D525](http://ark.intel.com/ja/products/49490/Intel-Atom-processor-D525-1M-Cache-1_80-GHz)   | 1.80 GHz | 2C/4T    | 2.5GT/s                                                                | 512KB x2 | ○                                                | ○                                                       | ×                                                      | ×                                                                                                         | 13W                                | DDR3-800 |
| [N450](http://ark.intel.com/ja/products/42503/Intel-Atom-Processor-N450-512K-Cache-1_66-GHz) | 1.66 GHz | 1C/2T    | 2.5GT/s                                                                | 512KB    | ○                                                | ○                                                       | ×                                                      | ○                                                                                                         | 5.5W                               | DDR2-667 |
| [N455](http://ark.intel.com/ja/products/49491/Intel-Atom-processor-N455-512K-Cache-1_66-GHz) | 1.66 GHz | 1C/2T    | 2.5GT/s                                                                | 512KB    | ○                                                | ○                                                       | ×                                                      | ○                                                                                                         | 6.5W                               | DDR3-667 |
| [N470](http://ark.intel.com/ja/products/46467/Intel-Atom-Processor-N470-512K-Cache-1_83-GHz) | 1.83 GHz | 1C/2T    | 2.5GT/s                                                                | 512KB    | ○                                                | ○                                                       | ×                                                      | ○                                                                                                         | 6.5W                               | DDR2-667 |
| [N475](http://ark.intel.com/ja/products/49492/Intel-Atom-processor-N475-512K-Cache-1_83-GHz) | 1.83 GHz | 1C/2T    | 2.5GT/s                                                                | 512KB    | ○                                                | ○                                                       | ×                                                      | ○                                                                                                         | 6.5W                               | DDR3-667 |
| [N550](http://ark.intel.com/ja/products/50154/Intel-Atom-Processor-N550-1M-Cache-1_50-GHz)   | 1.50 GHz | 2C/4T    | 2.5GT/s                                                                | 512KB x2 | ○                                                | ○                                                       | ×                                                      | ○                                                                                                         | 8.5W                               | DDR3-667 |
| [N570](http://ark.intel.com/ja/products/55637/Intel-Atom-Processor-N570-1M-Cache-1_66-GHz)   | 1.66 GHz | 2C/4T    | 2.5GT/s                                                                | 512KB x2 | ○                                                | ○                                                       | ×                                                      | ○                                                                                                         | 8.5W                               | DDR3-667 |

### タブレットPC・超小型PC向け

#### Menlow（メンロー）

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[4月2日](../Page/4月2日.md "wikilink")発表。2011年5月20日が最終受注日で生産終了\[13\]。プロセスルールは45nm。

<table>
<thead>
<tr class="header">
<th><p>プロセッサーナンバー</p></th>
<th><p>動作周波数</p></th>
<th><p>コア/スレッド数</p></th>
<th><p><a href="../Page/フロントサイドバス.md" title="wikilink">FSB</a></p></th>
<th><p>2次キャッシュ</p></th>
<th><p><a href="../Page/ハイパースレッディング・テクノロジー.md" title="wikilink">HT対応</a></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">64ビット対応</a></p></th>
<th><p><a href="../Page/インテル_バーチャライゼーション・テクノロジー.md" title="wikilink">VT</a> 対応</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Intel_SpeedStep_テクノロジ#拡張版_Intel_SpeedStep_テクノロジ_(EIST)" title="wikilink">EIST</a></p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">TDP</a> (<a href="../Page/ハイパースレッディング・テクノロジー.md" title="wikilink">HT</a>)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/35472/Intel-Atom-Processor-Z500-512K-Cache-800-MHz-400-MHz-FSB">Z500</a></p></td>
<td><p>800 MHz</p></td>
<td><p>1C/2T</p></td>
<td><p>400 MHz</p></td>
<td><p>512KB</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>0.65W</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/35469/Intel-Atom-Processor-Z510-512K-Cache-1_10-GHz-400-MHz-FSB">Z510</a></p></td>
<td><p>1.10 GHz</p></td>
<td><p>1C/1T</p></td>
<td><p>400 MHz</p></td>
<td><p>512KB</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>2W</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/41175/Intel-Atom-Processor-Z510P-512K-Cache-1_10-GHz-400-MHz-FSB">Z510P</a></p></td>
<td><p>1.10 GHz</p></td>
<td><p>1C/2T</p></td>
<td><p>400 MHz</p></td>
<td><p>512KB</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>2.2W</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/41176/Intel-Atom-Processor-Z510PT-512K-Cache-1_10-GHz-400-MHz-FSB">Z510PT</a></p></td>
<td><p>1.10 GHz</p></td>
<td><p>1C/2T</p></td>
<td><p>400 MHz</p></td>
<td><p>512KB</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>2.2W</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/40740/Intel-Atom-Processor-Z515-512K-Cache-1_20-GHz-400-MHz-FSB">Z515</a></p></td>
<td><p>BPT[14]:1.20 GHz<br />
HFM[15]:800 MHz</p></td>
<td><p>1C/2T</p></td>
<td><p>400 MHz</p></td>
<td><p>512KB</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>BPT:1.4W<br />
HFM:0.65W</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/35466/Intel-Atom-Processor-Z520-512K-Cache-1_33-GHz-533-MHz-FSB">Z520</a></p></td>
<td><p>1.33 GHz</p></td>
<td><p>1C/2T</p></td>
<td><p>533 MHz</p></td>
<td><p>512KB</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>2W（2.2W）</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/41174/Intel-Atom-Processor-Z520PT-512K-Cache-1_33-GHz-533-MHz-FSB">Z520PT</a></p></td>
<td><p>1.33 GHz</p></td>
<td><p>1C/2T</p></td>
<td><p>533 MHz</p></td>
<td><p>512KB</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>2.2W</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/35463/Intel-Atom-Processor-Z530-512K-Cache-1_60-GHz-533-MHz-FSB">Z530</a></p></td>
<td><p>1.60 GHz</p></td>
<td><p>1C/2T</p></td>
<td><p>533 MHz</p></td>
<td><p>512KB</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>2W（2.2W）</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/41173/Intel-Atom-Processor-Z530P-512K-Cache-1_60-GHz-533-MHz-FSB">Z530P</a></p></td>
<td><p>1.60 GHz</p></td>
<td><p>1C/2T</p></td>
<td><p>533 MHz</p></td>
<td><p>512KB</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>2.2W</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/35460/Intel-Atom-Processor-Z540-512K-Cache-1_86-GHz-533-MHz-FSB">Z540</a></p></td>
<td><p>1.86 GHz</p></td>
<td><p>1C/2T</p></td>
<td><p>533 MHz</p></td>
<td><p>512KB</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>2.4W（2.64W）</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/40741/Intel-Atom-Processor-Z550-512K-Cache-2_00-GHz-533-MHz-FSB">Z550</a></p></td>
<td><p>2.00 GHz</p></td>
<td><p>1C/2T</p></td>
<td><p>533 MHz</p></td>
<td><p>512KB</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>2.4W（2.64W）</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/49669/Intel-Atom-Processor-Z560-512K-Cache-2_13-GHz-533-MHz-FSB">Z560</a></p></td>
<td><p>2.13 GHz</p></td>
<td><p>1C/2T</p></td>
<td><p>533 MHz</p></td>
<td><p>512KB</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>2.5W（2.75W）</p></td>
</tr>
</tbody>
</table>

#### Oak Trail（オークトレイル）

[2011年](../Page/2011年.md "wikilink")[4月11日](../Page/4月11日.md "wikilink")発表\[16\]、[タブレット](https://ja.wikipedia.org/wiki/タブレット "wikilink")PC向けで、Menlowの後継製品。開発コードネーム「Lincroft」ことAtom Z6xxと「Whitney Point」ことIntel SM35 Expressを組み合わせたプラットフォーム。Oak Trail向けプロセッサZ670も同時に発表された。プロセスルールは45nm。ネットブック向けのAtom N450に比べると消費電力は70%削減されている。[F-07C](https://ja.wikipedia.org/wiki/F-07C "wikilink")（[Windows 7搭載](https://ja.wikipedia.org/wiki/Windows_7 "wikilink")）ではZ650を 0.60GHz (LFM) で搭載している。 メモリは DDR2-800 64bit シングルチャネル（6.4 GB/s）、最大2GB。最大出力解像度は1366x768 (LVDS)。\[17\]

<table>
<thead>
<tr class="header">
<th><p>プロセッサーナンバー</p></th>
<th><p>動作周波数</p></th>
<th><p>コア/スレッド数</p></th>
<th><p><a href="../Page/フロントサイドバス.md" title="wikilink">FSB</a></p></th>
<th><p>2次キャッシュ</p></th>
<th><p><a href="../Page/ハイパースレッディング・テクノロジー.md" title="wikilink">HT対応</a></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">64ビット対応</a></p></th>
<th><p><a href="../Page/インテル_バーチャライゼーション・テクノロジー.md" title="wikilink">VT</a> 対応</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Intel_SpeedStep_テクノロジ#拡張版_Intel_SpeedStep_テクノロジ_(EIST)" title="wikilink">EIST</a></p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">TDP</a></p></th>
<th><p>GPU</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/55664/Intel-Atom-Processor-Z650-512K-Cache-1_20-GHz">Z650</a></p></td>
<td><p>1.20 GHz (HFM)</p></td>
<td><p>1C/2T</p></td>
<td></td>
<td><p>512KB</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>3.0W</p></td>
<td><p>PowerVR SGX 535 (400MHz)</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/55663/Intel-Atom-Processor-Z670-512K-Cache-1_50-GHz">Z670</a></p></td>
<td><p>1.50 GHz (HFM)<br />
0.60 GHz (LFM)</p></td>
<td><p>1C/2T</p></td>
<td><p>667MHz</p></td>
<td><p>512KB</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>3.0W</p></td>
<td><p>PowerVR SGX 535 (400MHz)</p></td>
</tr>
</tbody>
</table>

HFM = 最高周波数モード, LFM = 最低周波数モード。

### スマートフォン・タブレット向け

#### Moorestown（ムーアズタウン）

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[5月4日](https://ja.wikipedia.org/wiki/5月4日 "wikilink")発表。[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")のアプリケーションプロセッサへの採用が想定されている。コードネーム「Lincroft」ことZ6xxシリーズとコードネーム「Langwell」こと「Platform Controller Hub MP20」チップセットを組み合わせたプラットフォーム。プロセスルールは45nm。

| プロセッサーナンバー                                                                                   | 動作周波数 (バースト)        | コア/スレッド数 | 2次キャッシュ | [HT対応](../Page/ハイパースレッディング・テクノロジー.md "wikilink") | [64ビット対応](https://ja.wikipedia.org/wiki/x64 "wikilink") | [VT](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink") 対応 | [EIST](https://ja.wikipedia.org/wiki/Intel_SpeedStep_テクノロジ#拡張版_Intel_SpeedStep_テクノロジ_\(EIST\) "wikilink") | [TDP](../Page/熱設計電力.md "wikilink") |
| -------------------------------------------------------------------------------------------- | ------------------- | -------- | ------- | ------------------------------------------------ | ------------------------------------------------------- | ------------------------------------------------------ | --------------------------------------------------------------------------------------------------------- | ---------------------------------- |
| [Z600](http://ark.intel.com/ja/products/49656/Intel-Atom-Processor-Z600-512K-Cache-1_20-GHz) | 0.80 GHz (1.20 GHz) | 1C/2T    | 512KB   | ○                                                | ×                                                       | ×                                                      | ○                                                                                                         | 1.3W                               |
| Z605                                                                                         | 0.60 GHz (1.00 GHz) | 1C/2T    | 512KB   | ○                                                | ×                                                       | ×                                                      | ○                                                                                                         | 2.2W                               |
| Z610                                                                                         | 0.80 GHz (1.20 GHz) | 1C/2T    | 512KB   | ○                                                | ×                                                       | ×                                                      | ○                                                                                                         | 1.3W                               |
| Z612                                                                                         | 0.90 GHz (1.50 GHz) | 1C/2T    | 512KB   | ○                                                | ×                                                       | ×                                                      | ○                                                                                                         | 1.3W                               |
| [Z615](http://ark.intel.com/ja/products/49660/Intel-Atom-Processor-Z615-512K-Cache-1_60-GHz) | 1.20 GHz (1.60 GHz) | 1C/2T    | 512KB   | ○                                                | ×                                                       | ×                                                      | ○                                                                                                         | 2.2W                               |
| Z620                                                                                         | 0.90 GHz (1.50 GHz) | 1C/2T    | 512KB   | ○                                                | ×                                                       | ×                                                      | ○                                                                                                         | 1.3W                               |
| [Z625](http://ark.intel.com/ja/products/49662/Intel-Atom-Processor-Z625-512K-Cache-1_90-GHz) | 1.50 GHz (1.90 GHz) | 1C/2T    | 512KB   | ○                                                | ×                                                       | ×                                                      | ○                                                                                                         | 2.2W                               |

### 家電（セットトップボックスなど）向け

#### Canmore（キャンモア）

Canmoreは[セットトップボックス](../Page/セットトップボックス.md "wikilink")や[テレビ](../Page/テレビ.md "wikilink")向けの[システム・オン・チップ製品である](../Page/System-on-a-chip.md "wikilink")。Intel Media Processor CE3100。2008年後半に出荷予定\[18\]。

以下の機能を持つ。

  - [高精細度テレビジョン放送](https://ja.wikipedia.org/wiki/高精細度テレビジョン放送 "wikilink") (1080p) 対応
  - [7.1チャンネル音声](../Page/サラウンド.md "wikilink")
  - 3次元グラフィックス

#### Sodaville（ソーダヴィル）

Atom CE4100（開発コードネーム：Sodaville）は、家電向けシステム・オン・チップ製品で 45nm プロセスで製造され、[2009年](../Page/2009年.md "wikilink")[9月24日](../Page/9月24日.md "wikilink")にIDF Fall 2009で発表された\[19\]。CE4100 CE4130 CE4150の3製品が公表されている\[20\]。

| プロセッサーナンバー | 動作周波数    | GPU周波数 | 2次キャッシュ | A/Vキャプチャ |
| ---------- | -------- | ------ | ------- | -------- |
| CE4100     | 1.20 GHz | 200MHz | 512KB   | ×        |
| CE4130     | 1.20 GHz | 200MHz | 512KB   | ○        |
| CE4150     | 1.20 GHz | 400MHz | 512KB   | ○        |
| CE4170     | 1.60 GHz | 400MHz | 512KB   | ○        |

### 組込み機器向け

#### Embedded Menlow

組込み機器向けの、コードネーム「Embedded Menlow」（エンベデッド メンロー）もSilverthorneとPoulsboで構成される。組込み機器においては「同じものが長期間に渡り調達可能であり続ける事」が重要となるため、ライフサイクルサポートを7年としている点が異なる。

#### Tunnel Creek（トンネルクリーク）

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[11月22日](https://ja.wikipedia.org/wiki/11月22日 "wikilink")に米intel社はFPGAを組み込んだ"Intel Atom E600シリーズ"（開発コード名：Tunnel Creek）を発表した。本製品は、産業機械や移動用医療機器、高性能プログラマブル・ロジック・コントローラーといった組込み型コンピュータや、通信機器、視覚システム、VoIPデバイスの制御ユニットなどを主な適用対象としている。

末尾にTがつくのは産業向けで、それ以外は環境温度保証が0〜70℃であるのに対して、Tがつくのは-40〜85℃。末尾にCがつくのは、[Altera](../Page/アルテラ.md "wikilink") [FPGA](../Page/FPGA.md "wikilink")を統合してシングルパッケージにしたモデル。

組込み用途において、Atomプロセッサを使いながらさらにユーザが独自に設計したデジタル回路を用いる場合には、プログラマブルな集積回路を別チップにしてAtomと共に製品を組み上げる構成が一般的であったが、Intel社はAtomに[アルテラ](../Page/アルテラ.md "wikilink")社のFPGAを組み込みシングル・パッケージで提供することにした。AtomプロセッサとFPGAを同一パッケージで扱えることで、設計者は基板スペースが縮小できるだけでなく、設計そのものもより柔軟となり、小さな修正や変更はプログラムの入れ替えによって迅速・容易に設計変更できる。このため、開発コストと設計変更リスクが最小限に抑えられ、また部品在庫の縮減が可能で製造工程も簡素化できるとされる。また、本製品のサポートはIntel社だけに集約し、少なくとも7年間のサポートを行うとしている。

産業用および商用温度環境のサポートし、動作クロックは0.6-1.3GHz、TDP2.7W-3.6Wの製品が準備されている。E665CT、E645CT、E665C、E645Cという4品種が同日から60日以内の出荷であり、E625CTとE625C2製品が2011年第1四半期の出荷を予定している。価格は61〜106米[ドル](../Page/ドル.md "wikilink")（1000個時）を予定している\[21\]。

本シリーズのダイは「Lincroft」系統の改良版であるとされる\[22\]\[23\]。

| プロセッサーナンバー | 動作周波数   | コア数 | 2次キャッシュ | [HT対応](../Page/ハイパースレッディング・テクノロジー.md "wikilink") | [64ビット対応](https://ja.wikipedia.org/wiki/x64 "wikilink") | [VT](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink") 対応 | [EIST](https://ja.wikipedia.org/wiki/Intel_SpeedStep_テクノロジ#拡張版_Intel_SpeedStep_テクノロジ_\(EIST\) "wikilink") | [TDP](../Page/熱設計電力.md "wikilink") | メモリ      | FPGA |
| ---------- | ------- | --- | ------- | ------------------------------------------------ | ------------------------------------------------------- | ------------------------------------------------------ | --------------------------------------------------------------------------------------------------------- | ---------------------------------- | -------- | ---- |
| E620       | 0.6 GHz | 1コア | 512KB   | ○                                                | ×                                                       | ○                                                      | ○                                                                                                         | 2.7W                               | DDR2-800 | ×    |
| E620T      | 0.6 GHz | 1コア | 512KB   | ○                                                | ×                                                       | ○                                                      | ○                                                                                                         | 2.7W                               | DDR2-800 | ×    |
| E625C      | 0.6 GHz | 1コア | 512KB   | ○                                                | ×                                                       | ○                                                      | ○                                                                                                         | 7W                                 | DDR2-800 | ○    |
| E625CT     | 0.6 GHz | 1コア | 512KB   | ○                                                | ×                                                       | ○                                                      | ○                                                                                                         | 7W                                 | DDR2-800 | ○    |
| E640       | 1.0 GHz | 1コア | 512KB   | ○                                                | ×                                                       | ○                                                      | ○                                                                                                         | 3.6W                               | DDR2-800 | ×    |
| E640T      | 1.0 GHz | 1コア | 512KB   | ○                                                | ×                                                       | ○                                                      | ○                                                                                                         | 3.6W                               | DDR2-800 | ×    |
| E645C      | 1.0 GHz | 1コア | 512KB   | ○                                                | ×                                                       | ○                                                      | ○                                                                                                         | 7W                                 | DDR2-800 | ○    |
| E645CT     | 1.0 GHz | 1コア | 512KB   | ○                                                | ×                                                       | ○                                                      | ○                                                                                                         | 7W                                 | DDR2-800 | ○    |
| E660       | 1.3 GHz | 1コア | 512KB   | ○                                                | ×                                                       | ○                                                      | ○                                                                                                         | 3.6W                               | DDR2-800 | ×    |
| E660T      | 1.3 GHz | 1コア | 512KB   | ○                                                | ×                                                       | ○                                                      | ○                                                                                                         | 3.6W                               | DDR2-800 | ×    |
| E665C      | 1.3 GHz | 1コア | 512KB   | ○                                                | ×                                                       | ○                                                      | ○                                                                                                         | 7W                                 | DDR2-800 | ○    |
| E665CT     | 1.3 GHz | 1コア | 512KB   | ○                                                | ×                                                       | ○                                                      | ○                                                                                                         | 7W                                 | DDR2-800 | ○    |
| E680       | 1.6 GHz | 1コア | 512KB   | ○                                                | ×                                                       | ○                                                      | ○                                                                                                         | 3.9W                               | DDR2-800 | ×    |
| E680T      | 1.6 GHz | 1コア | 512KB   | ○                                                | ×                                                       | ○                                                      | ○                                                                                                         | 3.9W                               | DDR2-800 | ×    |

## Saltwell マイクロアーキテクチャ

第2世代のAtom向けマイクロアーキテクチャである。Bonnellを32nmプロセスルールに縮小したもの。2011年9月出荷開始。

### ネットトップ・ネットブック向け (Cedar Trail)

[2011年](../Page/2011年.md "wikilink")[9月](../Page/9月.md "wikilink")出荷開始。コードネームは Cedar Trail (シーダートレイル)

サポートされるOSはWindows（グラフィックはWindows 7以降）、Chrome OS、Ubuntu 12.04 LTS (32bit版のみ)、MeeGo。内蔵グラフィック機能はドライバレベルで32bit及びWindows 7/8/8.1しかサポートされない点に注意。Windows 8以降は7用のドライバを流用する形での対応となる。前述以外のLinuxディストリビューションやWindows Vista,Windows XP用のドライバは提供されておらず代用も不可能なため、これらのOSと組み合わせて使用する際には、ビデオカードの増設が必要である。32nmプロセスルール。Intel GMA 3600/3650 は [PowerVR](../Page/PowerVR.md "wikilink") SGX 545 ベース。 ※一般向けには公式にサポート外となっているが、組込み向けには「エンベデッド・メディア・グラフィックス・ドライバー(EMGD)」としてWindows XPもサポートされている。

<table>
<thead>
<tr class="header">
<th><p>プロセッサーナンバー</p></th>
<th><p>動作周波数</p></th>
<th><p>コア/スレッド数</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Direct_Media_Interface" title="wikilink">DMI</a></p></th>
<th><p>2次キャッシュ</p></th>
<th><p><a href="../Page/ハイパースレッディング・テクノロジー.md" title="wikilink">HT対応</a></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">64ビット対応</a></p></th>
<th><p><a href="../Page/インテル_バーチャライゼーション・テクノロジー.md" title="wikilink">VT</a> 対応</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Intel_SpeedStep_テクノロジ#拡張版_Intel_SpeedStep_テクノロジ_(EIST)" title="wikilink">EIST</a></p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">TDP</a></p></th>
<th><p>GPU</p></th>
<th><p>メモリ</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/59682/Intel-Atom-Processor-D2500-1M-Cache-1_86-GHz">D2500</a></p></td>
<td><p>1.86 GHz</p></td>
<td><p>2C/2T</p></td>
<td><p>2.5GT/s</p></td>
<td><p>512KB x2</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>10W</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Intel_GMA" title="wikilink">Intel GMA</a> 3600 (400MHz)</p></td>
<td><p>DDR3-1066<br />
シングルチャネル</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/65470/Intel-Atom-Processor-D2550-1M-Cache-1_86-GHz">D2550</a></p></td>
<td><p>1.86 GHz</p></td>
<td><p>2C/4T</p></td>
<td><p>2.5GT/s</p></td>
<td><p>512KB x2</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>10W</p></td>
<td><p>Intel GMA 3650 (640MHz)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>D2560</p></td>
<td><p>2.00 GHz</p></td>
<td><p>2C/4T</p></td>
<td><p>2.5GT/s</p></td>
<td><p>512KB x2</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>10W</p></td>
<td><p>Intel GMA 3650 (640MHz)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/59683/Intel-Atom-Processor-D2700-1M-Cache-2_13-GHz">D2700</a></p></td>
<td><p>2.13 GHz</p></td>
<td><p>2C/4T</p></td>
<td><p>2.5GT/s</p></td>
<td><p>512KB x2</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>10W</p></td>
<td><p>Intel GMA 3650 (640MHz)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/58916/Intel-Atom-Processor-N2600-1M-Cache-1_6-GHz">N2600</a></p></td>
<td><p>1.60 GHz</p></td>
<td><p>2C/4T</p></td>
<td><p>2.5GT/s</p></td>
<td><p>512KB x2</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>3.5W</p></td>
<td><p>Intel GMA 3600 (400MHz)</p></td>
<td><p>DDR3-800<br />
シングルチャネル</p></td>
</tr>
<tr class="even">
<td><p>N2650</p></td>
<td><p>1.70 GHz</p></td>
<td><p>2C/4T</p></td>
<td><p>2.5GT/s</p></td>
<td><p>512KB x2</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>3.6W</p></td>
<td><p>Intel GMA 3600 (400MHz)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/58917/Intel-Atom-Processor-N2800-1M-Cache-1_86-GHz">N2800</a></p></td>
<td><p>1.86 GHz</p></td>
<td><p>2C/4T</p></td>
<td><p>2.5GT/s</p></td>
<td><p>512KB x2</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>6.5W</p></td>
<td><p>Intel GMA 3650 (640MHz)</p></td>
<td><p>DDR3-1066<br />
シングルチャネル</p></td>
</tr>
<tr class="even">
<td><p>N2850</p></td>
<td><p>2.00 GHz</p></td>
<td><p>2C/4T</p></td>
<td><p>2.5GT/s</p></td>
<td><p>512KB x2</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>6.6W</p></td>
<td><p>Intel GMA 3650 (640MHz)</p></td>
<td></td>
</tr>
</tbody>
</table>

### タブレットPC・超小型PC向け (Clover Trail)

[2012年](../Page/2012年.md "wikilink")[9月27日](https://ja.wikipedia.org/wiki/9月27日 "wikilink")発表、タブレットPC向け（主に[Windows 8タブレットで採用](https://ja.wikipedia.org/wiki/Windows_8 "wikilink")）、Oak Trailの後継製品。コードネームは Clover Trail (クローバートレイル)。プロセスルールは、Medfieldと同様に32nm。Medfieldに比べてWindowsドライバのサポートなどに調整を加えた製品。メモリは LPDDR2-800 32bit デュアルチャネル（6.4GB/s）、最大2GB。DirectX 9.3, OpenVG 1.1, OpenGL 2.1, OpenGL ES 2.0 対応。\[24\]

<table>
<thead>
<tr class="header">
<th><p>プロセッサーナンバー</p></th>
<th><p>動作周波数</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>2次キャッシュ</p></th>
<th><p><a href="../Page/ハイパースレッディング・テクノロジー.md" title="wikilink">HT対応</a></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">64ビット対応</a></p></th>
<th><p><a href="../Page/インテル_バーチャライゼーション・テクノロジー.md" title="wikilink">VT</a> 対応</p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">TDP</a></p></th>
<th><p>GPU</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/70105/Intel-Atom-Processor-Z2760-1MB-Cache-1_80-GHz">Z2760</a></p></td>
<td><p>1.80 GHz (バースト)<br />
1.50 GHz (HFM)<br />
0.60 GHz (LFM)</p></td>
<td><p>2C/4T</p></td>
<td><p>512KB x2</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>1.7W</p></td>
<td><p><a href="../Page/PowerVR.md" title="wikilink">PowerVR</a> SGX 545 (533MHz)</p></td>
</tr>
</tbody>
</table>

### スマートフォン向け (Medfield, Lexington)

[2012年](../Page/2012年.md "wikilink")[1月10日](../Page/1月10日.md "wikilink")発表（Z2460）、スマートフォン向けで、Moorestownの後継製品。Saltwell マイクロアーキテクチャ。プロセスルールは32nm\[25\]。メモリは LPDDR2-400 32bit デュアルチャネル（3.2 GB/s）。コードネームは Medfield (メドフィールド)。Z2420はMedfieldに属するが低価格市場向けを想定しておりコードネームは Lexington (レキシントン) となる\[26\]。2.0GHz 時は750mW、0.1GHz時は50mW\[27\]。

<table>
<thead>
<tr class="header">
<th><p>プロセッサーナンバー</p></th>
<th><p>nowrap | 動作周波数 (バースト)</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>2次キャッシュ</p></th>
<th><p><a href="../Page/ハイパースレッディング・テクノロジー.md" title="wikilink">HT対応</a></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">64ビット対応</a></p></th>
<th><p><a href="../Page/インテル_バーチャライゼーション・テクノロジー.md" title="wikilink">VT</a> 対応</p></th>
<th><p>GPU</p></th>
<th><p>モデム</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Z2000</p></td>
<td><p>1.00 GHz (なし)</p></td>
<td><p>1C/1T</p></td>
<td><p>512KB</p></td>
<td><p>×</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>PowerVR SGX 540 (320MHz)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Z2420</p></td>
<td><p>1.20 GHz (なし)</p></td>
<td><p>1C/2T</p></td>
<td><p>512KB</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>PowerVR SGX 540 (400MHz)</p></td>
<td><p>XMM 6265<br />
(HSPA+)</p></td>
</tr>
<tr class="odd">
<td><p>Z2460</p></td>
<td><p>1.30 GHz (1.60GHz)</p></td>
<td><p>1C/2T</p></td>
<td><p>512KB</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>PowerVR SGX 540 (400MHz)</p></td>
<td><p>XMM 6260<br />
(HSPA+)</p></td>
</tr>
<tr class="even">
<td><p>Z2480</p></td>
<td><p>不明 (2.00GHz)</p></td>
<td><p>1C/2T</p></td>
<td><p>512KB</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>PowerVR SGX 540 (400MHz)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Z2610</p></td>
<td><p>1.30 GHz (1.60GHz)</p></td>
<td><p>1C/2T</p></td>
<td><p>512KB</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>×</p></td>
<td><p>PowerVR SGX 540 (400MHz)</p></td>
<td></td>
</tr>
</tbody>
</table>

### スマートフォン・タブレット向け (Clover Trail+)

[2013年](../Page/2013年.md "wikilink")[2月24日](https://ja.wikipedia.org/wiki/2月24日 "wikilink")発表、スマートフォン・タブレット向け、Medfieldの後継製品。コードネームは Clover Trail+ (クローバートレイルプラス)。SoCのコードネームは「Cloverview+」。Clover TrailのGPUをスマートフォン向けに変更したものだが、Medfieldに比べて消費電力で劣るようなことはない \[28\]。Saltwell マイクロアーキテクチャ。プロセスルールは32nm High-Kメタルゲート。最大出力解像度は 1920x1200。命令セットは32ビット。[Intel VT-x](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink") 対応。

<table>
<thead>
<tr class="header">
<th><p>プロセッサーナンバー</p></th>
<th><p>最高動作周波数</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>2次キャッシュ</p></th>
<th><p><a href="../Page/ハイパースレッディング・テクノロジー.md" title="wikilink">HT対応</a></p></th>
<th><p>GPU</p></th>
<th><p>メモリ</p></th>
<th><p>モデム</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/75203/Intel-Atom-Processor-Z2520-1MB-Cache-1_20-GHz">Z2520</a></p></td>
<td><p>1.20 GHz</p></td>
<td><p>2C/4T</p></td>
<td><p>512KB x2</p></td>
<td><p>○</p></td>
<td><p>PowerVR SGX 544MP2 (300MHz)</p></td>
<td><p>32ビットx2<br />
LPDDR2-1066<br />
8.528 GB/s</p></td>
<td><p>XMM 6360<br />
(HSPA+)</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/70101/Intel-Atom-Processor-Z2560-1MB-Cache-1_60-GHz">Z2560</a></p></td>
<td><p>1.60 GHz</p></td>
<td><p>PowerVR SGX 544MP2 (400MHz)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/70100/Intel-Atom-Processor-Z2580-1MB-Cache-2_00-GHz">Z2580</a></p></td>
<td><p>2.00 GHz</p></td>
<td><p>PowerVR SGX 544MP2 (533MHz)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### サーバー向け (Centerton, Briarwood)

[2012年](../Page/2012年.md "wikilink")[12月11日](../Page/12月11日.md "wikilink")発表。CloverTrailをベースとする低消費電力などに適したサーバー向けSoCである\[29\]。Centerton (センタートン) がサーバー向け、Briarwood (ブライアーウッド) がストレージ・通信機器向け。Saltwell マイクロアーキテクチャ。プロセスルールは32nm。メモリは DDR3-1333 シングルチャネル（10.66 GB/s）。[Intel 64](https://ja.wikipedia.org/wiki/Intel_64 "wikilink"), [Intel VT-x](https://ja.wikipedia.org/wiki/Intel_VT-x "wikilink"), [SSE](../Page/ストリーミングSIMD拡張命令.md "wikilink") 3 対応。

| プロセッサーナンバー                                                                                    | 動作周波数   | コア/スレッド数 | 2次キャッシュ | [HT対応](../Page/ハイパースレッディング・テクノロジー.md "wikilink") | [TDP](../Page/熱設計電力.md "wikilink") | 価格  |
| --------------------------------------------------------------------------------------------- | ------- | -------- | ------- | ------------------------------------------------ | ---------------------------------- | --- |
| [S1220](http://ark.intel.com/ja/products/71269/Intel-Atom-Processor-S1220-1MB-Cache-1_60-GHz) | 1.6 GHz | 2C/4T    | 512KBx2 | ○                                                | 8.1W                               | $54 |
| [S1240](http://ark.intel.com/ja/products/71268/Intel-Atom-Processor-S1240-1MB-Cache-1_60-GHz) | 1.6 GHz | 2C/4T    | 512KBx2 | ○                                                | 6.1W                               | $64 |
| [S1260](http://ark.intel.com/ja/products/71267/Intel-Atom-Processor-S1260-1MB-Cache-2_00-GHz) | 2.0 GHz | 2C/4T    | 512KBx2 | ○                                                | 8.5W                               | $64 |

Centerton（センタートン）

| プロセッサーナンバー                                                                                    | 動作周波数   | コア/スレッド数 | 2次キャッシュ | [HT対応](../Page/ハイパースレッディング・テクノロジー.md "wikilink") | [TDP](../Page/熱設計電力.md "wikilink") | 価格   |
| --------------------------------------------------------------------------------------------- | ------- | -------- | ------- | ------------------------------------------------ | ---------------------------------- | ---- |
| [S1269](http://ark.intel.com/ja/products/71272/Intel-Atom-Processor-S1269-1MB-Cache-1_60-GHz) | 1.6 GHz | 2C/4T    | 512KBx2 | ○                                                | 11.7W                              | $80  |
| [S1279](http://ark.intel.com/ja/products/71271/Intel-Atom-Processor-S1279-1MB-Cache-1_60-GHz) | 1.6 GHz | 2C/4T    | 512KBx2 | ○                                                | 13.1W                              | $103 |
| [S1289](http://ark.intel.com/ja/products/71270/Intel-Atom-Processor-S1289-1MB-Cache-2_00-GHz) | 2.0 GHz | 2C/4T    | 512KBx2 | ○                                                | 14.0W                              | $120 |

Briarwood（ブライアーウッド）

## Silvermont マイクロアーキテクチャ

第3世代のAtom向けマイクロアーキテクチャで、Atom向けとしては最初の機能強化版である。22nmプロセスルール。Intel VT-x や AES-NI 対応など、サーバ向けの機能が強化されている製品もある。デスクトップ・ネットブック向けのチップは Atom ブランドではなく [Celeron](../Page/Intel_Celeron.md "wikilink") や [Pentium](https://ja.wikipedia.org/wiki/Intel_Pentium_\(2010年\) "wikilink") のブランドで発売される。最初に発表された製品がサーバー向けで2013年9月4日発表。

Silvermontマイクロアーキテクチャは、Atomとしては初めてアウト・オブ・オーダー型の設計となった。命令デコード、リタイアは依然としてクロック当たり2命令であるが、整数×2、浮動小数点/SIMD×2、ロード/ストア×1の計5つの命令発行ポートを備え、クロック当たり最大5命令を順不同で発行可能である。これらの発行ポートは各々に独立したスケジューラ (リザベーション・ステーション) を備えており、Intelのマイクロプロセッサとしては[NetBurstマイクロアーキテクチャ](../Page/NetBurstマイクロアーキテクチャ.md "wikilink")以来の分散型のスケジューラを持つ構造となっている。従来のAtomマイクロアーキテクチャではロード+演算の型を持つCISC命令に対応するため、命令パイプラインの共通部分にL1Dキャッシュへのアクセス段を組み込み、キャッシュアクセスのレイテンシを隠蔽する構成を取っていたが、Silvermontではこれを廃し、独立したロード/ストアパイプをバックエンドに設けている。このため、パイプライン長は従来と比較して短くなり、整数演算命令における分岐ミス時のペナルティも13サイクルから10サイクルへと短くなっている。

5つのスケジューラのうち2つの整数スケジューラは完全なアウト・オブ・オーダーの実装になっており、オペランドが準備できた命令から発行可能である。一方で他の3つのスケジューラはプログラム順の発行しか許しておらず、スケジューラ内の最も旧い命令が発行されない限り他の命令の発行はできない。このため、浮動小数点演算/SIMD命令で順不同での発行が可能なのは、別のスケジューラに割り当てられた命令同士の組み合わせのみである。ロード/ストア命令に関してはスケジューラが1つしか存在しないため、同種の命令同士で順不同の発行は不可能であるが、可能な限り命令発行をブロックしないために2つの工夫が導入されている。1つはキャッシュミスに対するノンブロッキングな設計で、キャッシュミスが起きても最大8命令までは後続命令をブロックすること無く命令発行が可能である。もう1つはRehab Queueと呼ばれるサブ命令キューの設置で、[TLBミスやアドレス計算に必要な](../Page/トランスレーション・ルックアサイド・バッファ.md "wikilink")[オペランドが到着していない等の理由で命令が発行できない場合に](https://ja.wikipedia.org/wiki/被演算子 "wikilink")、このRehab Queueにスケジューラから命令を追い出すことができる。これらの工夫により、ロード/ストアパイプはインオーダ型のスケジューラ1つでも命令の"詰まり"による性能低下が起こりにくい設計になっている。

Silvermontは2つのコアと1 MBのL2キャッシュで1つのモジュールを構成しており、モジュール間はIntra-Die Interconnect (IDI) と呼ばれる[ポイント・ツー・ポイント](https://ja.wikipedia.org/wiki/ポイント・ツー・ポイント "wikilink")型のインターコネクトで結ばれる。従来は低速な[FSBがコア間通信やDRAMアクセスのボトルネックとなっていたが](../Page/フロントサイドバス.md "wikilink")、新アーキテクチャではこれを廃している。サーバ向けには最大8コア、タブレット/ネットブック向けには最大4コア、スマートフォン向けには最大2コアの構成が予定されている。いずれの場合も1コアで1スレッドを実行し、従来のように[ハイパースレッディング・テクノロジー](../Page/ハイパースレッディング・テクノロジー.md "wikilink")には対応しない。対応する命令セットはSSE4.1、SSE4.2、AES-NIなどが新たに加わっているが、2011年より同社の[Core系のプロセッサに搭載されている](../Page/Intel_Core.md "wikilink")[AVXには対応しない](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#Intel_AVX "wikilink")。

Intelは前世代の32 nmのSaltwellマイクロアーキテクチャと比較して、シングルスレッドではIPCが50 %程度改善し、同じ消費電力で性能は2倍になると主張している。また、マルチスレッドではSilvermontの4コアで2コア4スレッドの前世代と比較してピーク性能が2.8倍、同じ消費電力の場合は性能が2.5倍になると主張している。

### デスクトップPC向け (Bay Trail-D)

[2013年](../Page/2013年.md "wikilink")[11月](../Page/11月.md "wikilink")発表。Cedar Trailの後継として登場。[静音性](../Page/静音パソコン.md "wikilink")（[ファンレス構造](../Page/CPUの冷却装置.md "wikilink")）や省エネ性を重視したタワー型デスクトップやA4型ノートにも搭載されるようになり、以前よりも用途が広がった。Atom の名を冠さず、[Celeron](../Page/Intel_Celeron.md "wikilink") や [Pentium](https://ja.wikipedia.org/wiki/Intel_Pentium_\(2010年\) "wikilink") のブランドで発売される。

第3世代のAtom向けマイクロアーキテクチャSilvermontを搭載したCPU。22 nmプロセスルール。Intel VT-x や AES-NI 対応など、サーバ向けの機能も強化されている。Bay Trail-Dはデスクトップ向けでPentium J / Celeron J、Bay Trail-Mはノート向けでPentium N / Celeron Nとして販売される。

<table>
<caption>Bay Trail-D</caption>
<thead>
<tr class="header">
<th><p>プロセッサー<br />
ナンバー</p></th>
<th><p>CPU周波数<br />
(GHz)</p></th>
<th><p>CPUバースト<br />
(GHz)</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>キャッシュ</p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">TDP</a></p></th>
<th><p>メモリ</p></th>
<th><p>メモリ帯域<br />
(GB/s)</p></th>
<th><p>GPU<br />
EU数</p></th>
<th><p>GPU周波数<br />
(MHz)</p></th>
<th><p>GPUバースト<br />
(MHz)</p></th>
<th><p>発売時期</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/78868/Intel-Pentium-Processor-J2900-2M-Cache-up-to-2_67-GHz">Pentium J2900</a></p></td>
<td><p>2.41</p></td>
<td><p>2.66</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>10W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td></td>
<td><p>4</p></td>
<td><p>688</p></td>
<td><p>896</p></td>
<td><p>Q4'13</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/76529/Intel-Pentium-Processor-J2850-2M-Cache-2_41-GHz">Pentium J2850</a></p></td>
<td><p>2.41</p></td>
<td></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>10W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td></td>
<td><p>4</p></td>
<td><p>688</p></td>
<td><p>854</p></td>
<td><p>Q3'13</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/78867/Intel-Celeron-Processor-J1900-2M-Cache-up-to-2_42-GHz">Celeron J1900</a></p></td>
<td><p>2.0</p></td>
<td><p>2.41</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>10W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td></td>
<td><p>4</p></td>
<td><p>688</p></td>
<td><p>854</p></td>
<td><p>Q4'13</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/76530/Intel-Celeron-Processor-J1850-2M-Cache-2_00-GHz">Celeron J1850</a></p></td>
<td><p>2.0</p></td>
<td></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>10W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td></td>
<td><p>4</p></td>
<td><p>688</p></td>
<td><p>792</p></td>
<td><p>Q3'13</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/78866/Intel-Celeron-Processor-J1800-1M-Cache-up-to-2_58-GHz">Celeron J1800</a></p></td>
<td><p>2.41</p></td>
<td><p>2.58</p></td>
<td><p>2C/2T</p></td>
<td><p>1MB</p></td>
<td><p>10W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td></td>
<td><p>4</p></td>
<td><p>688</p></td>
<td><p>792</p></td>
<td><p>Q4'13</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/76531/Intel-Celeron-Processor-J1750-1M-Cache-2_41-GHz">Celeron J1750</a></p></td>
<td><p>2.41</p></td>
<td></td>
<td><p>2C/2T</p></td>
<td><p>1MB</p></td>
<td><p>10W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td></td>
<td><p>4</p></td>
<td><p>688</p></td>
<td><p>750</p></td>
<td><p>Q3'13</p></td>
</tr>
</tbody>
</table>

### ノートPC向け (Bay Trail-M)

[2013年](../Page/2013年.md "wikilink")[9月](../Page/9月.md "wikilink")発表。GPU は Intel HD Graphics。Intel NUCなどのミニPCでも使われている。

<table>
<caption>Bay Trail-M</caption>
<thead>
<tr class="header">
<th><p>プロセッサー<br />
ナンバー</p></th>
<th><p>CPU周波数<br />
(GHz)</p></th>
<th><p>CPUバースト<br />
(GHz)</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>キャッシュ</p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">TDP</a></p></th>
<th><p>メモリ</p></th>
<th><p>メモリ帯域<br />
(GB/s)</p></th>
<th><p>GPU<br />
EU数</p></th>
<th><p>GPU周波数<br />
(MHz)</p></th>
<th><p>GPUバースト<br />
(MHz)</p></th>
<th><p>発売時期</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/82105/Intel-Pentium-Processor-N3540-2M-Cache-up-to-2_66-GHz">Pentium N3540</a></p></td>
<td><p>2.16</p></td>
<td><p>2.66</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>7.5W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td><p>21.32</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>896</p></td>
<td><p>Q3'14</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/81074/Intel-Pentium-Processor-N3530-2M-Cache-up-to-2_58-GHz">Pentium N3530</a></p></td>
<td><p>2.16</p></td>
<td><p>2.58</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>7.5W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td><p>21.32</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>896</p></td>
<td><p>Q1'14</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/79049/Intel-Pentium-Processor-N3520-2M-Cache-up-to-2_42-GHz">Pentium N3520</a></p></td>
<td><p>2.16</p></td>
<td><p>2.42</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>7.5W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td><p>21.32</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>854</p></td>
<td><p>Q4'13</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/76751/Intel-Pentium-Processor-N3510-2M-Cache-2_00-GHz">Pentium N3510</a></p></td>
<td><p>2.00</p></td>
<td></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>7.5W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td><p>21.32</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>750</p></td>
<td><p>Q3'13</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/82104/Intel-Celeron-Processor-N2940-2M-Cache-up-to-2_25-GHz">Celeron N2940</a></p></td>
<td><p>1.83</p></td>
<td><p>2.25</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>7.5W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td><p>21.32</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>854</p></td>
<td><p>Q3'14</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/81073/Intel-Celeron-Processor-N2930-2M-Cache-up-to-2_16-GHz">Celeron N2930</a></p></td>
<td><p>1.83</p></td>
<td><p>2.16</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>7.5W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td><p>21.32</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>854</p></td>
<td><p>Q1'14</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/79053/Intel-Celeron-Processor-N2920-2M-Cache-up-to-2_00-GHz">Celeron N2920</a></p></td>
<td><p>1.86</p></td>
<td><p>2.00</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>7.5W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td><p>21.32</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>844</p></td>
<td><p>Q4'13</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/76752/Intel-Celeron-Processor-N2910-2M-Cache-1_60-GHz">Celeron N2910</a></p></td>
<td><p>1.60</p></td>
<td></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>7.5W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td><p>21.32</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>756</p></td>
<td><p>Q3'13</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/82103/Intel-Celeron-Processor-N2840-1M-Cache-up-to-2_58-GHz">Celeron N2840</a></p></td>
<td><p>2.16</p></td>
<td><p>2.58</p></td>
<td><p>2C/2T</p></td>
<td><p>1MB</p></td>
<td><p>7.5W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td><p>21.32</p></td>
<td><p>4</p></td>
<td><p>311</p></td>
<td><p>792</p></td>
<td><p>Q3'14</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/81071/Intel-Celeron-Processor-N2830-1M-Cache-up-to-2_41-GHz">Celeron N2830</a></p></td>
<td><p>2.16</p></td>
<td><p>2.41</p></td>
<td><p>2C/2T</p></td>
<td><p>1MB</p></td>
<td><p>7.5W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td><p>21.32</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>750</p></td>
<td><p>Q1'14</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/79052/Intel-Celeron-Processor-N2820-1M-Cache-up-to-2_39-GHz">Celeron N2820</a></p></td>
<td><p>2.13</p></td>
<td><p>2.39</p></td>
<td><p>2C/2T</p></td>
<td><p>1MB</p></td>
<td><p>7.5W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td><p>21.32</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>756</p></td>
<td><p>Q4'13</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/79051/Intel-Celeron-Processor-N2815-1M-Cache-up-to-2_13-GHz">Celeron N2815</a></p></td>
<td><p>1.86</p></td>
<td><p>2.13</p></td>
<td><p>2C/2T</p></td>
<td><p>1MB</p></td>
<td><p>7.5W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td><p>21.32</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>756</p></td>
<td><p>Q4'13</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/76753/Intel-Celeron-Processor-N2810-1M-Cache-2_00-GHz">Celeron N2810</a></p></td>
<td><p>2.00</p></td>
<td></td>
<td><p>2C/2T</p></td>
<td><p>1MB</p></td>
<td><p>7.5W</p></td>
<td><p>DDR3L-1333x2</p></td>
<td><p>21.32</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>756</p></td>
<td><p>Q3'13</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/82102/Intel-Celeron-Processor-N2808-1M-Cache-up-to-2_25-GHz">Celeron N2808</a></p></td>
<td><p>1.58</p></td>
<td><p>2.25</p></td>
<td><p>2C/2T</p></td>
<td><p>1MB</p></td>
<td><p>4.5W</p></td>
<td><p>DDR3L-1333x1</p></td>
<td><p>10.66</p></td>
<td><p>4</p></td>
<td><p>311</p></td>
<td><p>792</p></td>
<td><p>Q3'14</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/81072/Intel-Celeron-Processor-N2807-1M-Cache-up-to-2_16-GHz">Celeron N2807</a></p></td>
<td><p>1.58</p></td>
<td><p>2.16</p></td>
<td><p>2C/2T</p></td>
<td><p>1MB</p></td>
<td><p>4.3W</p></td>
<td><p>DDR3L-1333x1</p></td>
<td><p>10.66</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>750</p></td>
<td><p>Q1'14</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/79050/Intel-Celeron-Processor-N2806-1M-Cache-up-to-2_00-GHz">Celeron N2806</a></p></td>
<td><p>1.60</p></td>
<td><p>2.00</p></td>
<td><p>2C/2T</p></td>
<td><p>1MB</p></td>
<td><p>4.5W</p></td>
<td><p>DDR3L-1333x1</p></td>
<td><p>10.66</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>756</p></td>
<td><p>Q4'13</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/76754/Intel-Celeron-Processor-N2805-1M-Cache-1_46-GHz">Celeron N2805</a></p></td>
<td><p>1.46</p></td>
<td></td>
<td><p>2C/2T</p></td>
<td><p>1MB</p></td>
<td><p>4.3W</p></td>
<td><p>DDR3L-1333x1</p></td>
<td><p>10.66</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>667</p></td>
<td><p>Q3'13</p></td>
</tr>
</tbody>
</table>

### タブレットPC向け (Bay Trail-T)

[2013年](../Page/2013年.md "wikilink")[9月11日](../Page/9月11日.md "wikilink")発表。タブレットPC向け（Windows 8.1 や Android 対応）、Clover Trail の後継製品。Silvermont マイクロアーキテクチャ。プロセスルールは22nm。GPU は [PowerVR](../Page/PowerVR.md "wikilink") から第7世代 [Intel HD Graphics](https://ja.wikipedia.org/wiki/Intel_HD_Graphics "wikilink") (Ivy Bridge 世代) になり、DirectX 11, OpenGL 3.2, [OpenCL](../Page/OpenCL.md "wikilink") 1.2 に対応。[Intel 64](https://ja.wikipedia.org/wiki/Intel_64 "wikilink"), [Intel VT-x](https://ja.wikipedia.org/wiki/Intel_VT-x "wikilink"), [SSE](../Page/ストリーミングSIMD拡張命令.md "wikilink") 4.2 対応。H.263, H.264, VC1, Multiview Video Coding, VP8, Motion JPEG のハードウェアデコーダー、H.264 のハードウェアエンコーダー搭載。HDMI 1.4, DisplayPort 1.2, eDP 1.3, WiDi 出力対応。

<table>
<caption>Bay Trail-T</caption>
<thead>
<tr class="header">
<th><p>プロセッサー<br />
ナンバー</p></th>
<th><p>CPU周波数<br />
(GHz)</p></th>
<th><p>CPUバースト<br />
(GHz)</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>2次キャッシュ</p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">SDP</a></p></th>
<th><p>メモリ</p></th>
<th><p>メモリ帯域<br />
(GB/s)</p></th>
<th><p>GPU<br />
EU数</p></th>
<th><p>GPU周波数<br />
(MHz)</p></th>
<th><p>GPUバースト<br />
(MHz)</p></th>
<th><p>発売時期</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Z3680</p></td>
<td><p>1.33</p></td>
<td><p>2.00</p></td>
<td><p>2C/2T</p></td>
<td><p>1MB</p></td>
<td><p>2.0W</p></td>
<td><p>LPDDR3-1066x1</p></td>
<td><p>8.5</p></td>
<td><p>4</p></td>
<td><p>311</p></td>
<td><p>667</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Z3680D</p></td>
<td><p>1.33</p></td>
<td><p>2.00</p></td>
<td><p>2C/2T</p></td>
<td><p>1MB</p></td>
<td><p>2.4W</p></td>
<td><p>DDR3L-RS-1333x1</p></td>
<td><p>10.6</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>688</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/76759/Intel-Atom-Processor-Z3740-2M-Cache-up-to-1_86-GHz">Z3740</a></p></td>
<td><p>1.33</p></td>
<td><p>1.86</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2.0W</p></td>
<td><p>LPDDR3-1066x2</p></td>
<td><p>17.1</p></td>
<td><p>4</p></td>
<td><p>311</p></td>
<td><p>667</p></td>
<td><p>Q3'13</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/78416/Intel-Atom-Processor-Z3740D-2M-Cache-up-to-1_86-GHz">Z3740D</a></p></td>
<td><p>1.33</p></td>
<td><p>1.86</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2.2W</p></td>
<td><p>DDR3L-RS-1333x1</p></td>
<td><p>10.6</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>688</p></td>
<td><p>Q3'13</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/76760/Intel-Atom-Processor-Z3770-2M-Cache-up-to-2_39-GHz">Z3770</a></p></td>
<td><p>1.46</p></td>
<td><p>2.39</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2.0W</p></td>
<td><p>LPDDR3-1066x2</p></td>
<td><p>17.1</p></td>
<td><p>4</p></td>
<td><p>311</p></td>
<td><p>667</p></td>
<td><p>Q3'13</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/78415/Intel-Atom-Processor-Z3770D-2M-Cache-up-to-2_41-GHz">Z3770D</a></p></td>
<td><p>1.50</p></td>
<td><p>2.41</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2.2W</p></td>
<td><p>DDR3L-RS-1333x1</p></td>
<td><p>10.6</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>688</p></td>
<td><p>Q3'13</p></td>
</tr>
</tbody>
</table>

  - Bay Trail Refresh

[2014年](../Page/2014年.md "wikilink")[3月](https://ja.wikipedia.org/wiki/3月 "wikilink")発表。B2/B3 step (Z3xx0) から C0 step (Z3xx5, Z3xx6) に改良され GPU 周波数が向上している。

<table>
<caption>Bay Trail Refresh</caption>
<thead>
<tr class="header">
<th><p>プロセッサー<br />
ナンバー</p></th>
<th><p>CPU周波数<br />
(GHz)</p></th>
<th><p>CPUバースト<br />
(GHz)</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>2次キャッシュ</p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">SDP</a></p></th>
<th><p>メモリ</p></th>
<th><p>メモリ帯域<br />
(GB/s)</p></th>
<th><p>GPU<br />
EU数</p></th>
<th><p>GPU周波数<br />
(MHz)</p></th>
<th><p>GPUバースト<br />
(MHz)</p></th>
<th><p>発売時期</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/80272/Intel-Atom-Processor-Z3735D-2M-Cache-up-to-1_83-GHz">Z3735D</a></p></td>
<td><p>1.33</p></td>
<td><p>1.83</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2.2W</p></td>
<td><p>DDR3L-RS-1333x1</p></td>
<td><p>10.6</p></td>
<td><p>4</p></td>
<td><p>311</p></td>
<td><p>646</p></td>
<td><p>Q1'14</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/80273/Intel-Atom-Processor-Z3735E-2M-Cache-up-to-1_83-GHz">Z3735E</a></p></td>
<td><p>1.33</p></td>
<td><p>1.83</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2.2W</p></td>
<td><p>DDR3L-RS-1333x1</p></td>
<td><p>5.3</p></td>
<td><p>4</p></td>
<td><p>311</p></td>
<td><p>646</p></td>
<td><p>Q1'14</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/80274/Intel-Atom-Processor-Z3735F-2M-Cache-up-to-1_83-GHz">Z3735F</a></p></td>
<td><p>1.33</p></td>
<td><p>1.83</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2.2W</p></td>
<td><p>DDR3L-RS-1333x1</p></td>
<td><p>10.6</p></td>
<td><p>4</p></td>
<td><p>311</p></td>
<td><p>646</p></td>
<td><p>Q1'14</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/80275/Intel-Atom-Processor-Z3735G-2M-Cache-up-to-1_83-GHz">Z3735G</a></p></td>
<td><p>1.33</p></td>
<td><p>1.83</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2.2W</p></td>
<td><p>DDR3L-RS-1333x1</p></td>
<td><p>5.3</p></td>
<td><p>4</p></td>
<td><p>311</p></td>
<td><p>646</p></td>
<td><p>Q1'14</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/82115/Intel-Atom-Processor-Z3736F-2M-Cache-up-to-2_16-GHz">Z3736F</a></p></td>
<td><p>1.33</p></td>
<td><p>2.16</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2.2W</p></td>
<td><p>DDR3L-RS-1333x1</p></td>
<td><p>10.6</p></td>
<td><p>4</p></td>
<td><p>311</p></td>
<td><p>646</p></td>
<td><p>Q2'14</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/82116/Intel-Atom-Processor-Z3736G-2M-Cache-up-to-2_16-GHz">Z3736G</a></p></td>
<td><p>1.33</p></td>
<td><p>2.16</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2.2W</p></td>
<td><p>DDR3L-RS-1333x1</p></td>
<td><p>5.3</p></td>
<td><p>4</p></td>
<td><p>311</p></td>
<td><p>646</p></td>
<td><p>Q2'14</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/80270/Intel-Atom-Processor-Z3745-2M-Cache-up-to-1_86-GHz">Z3745</a></p></td>
<td><p>1.33</p></td>
<td><p>1.86</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2.0W</p></td>
<td><p>LPDDR3-1066x2</p></td>
<td><p>17.1</p></td>
<td><p>4</p></td>
<td><p>311</p></td>
<td><p>778</p></td>
<td><p>Q1'14</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/80271/Intel-Atom-Processor-Z3745D-2M-Cache-up-to-1_83-GHz">Z3745D</a></p></td>
<td><p>1.33</p></td>
<td><p>1.86</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2.2W</p></td>
<td><p>DDR3L-RS-1333x1</p></td>
<td><p>10.6</p></td>
<td><p>4</p></td>
<td><p>311</p></td>
<td><p>792</p></td>
<td><p>Q1'14</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/80268/Intel-Atom-Processor-Z3775-2M-Cache-up-to-2_39-GHz">Z3775</a></p></td>
<td><p>1.46</p></td>
<td><p>2.39</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2.0W</p></td>
<td><p>LPDDR3-1066x2</p></td>
<td><p>17.1</p></td>
<td><p>4</p></td>
<td><p>311</p></td>
<td><p>778</p></td>
<td><p>Q1'14</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/80269/Intel-Atom-Processor-Z3775D-2M-Cache-up-to-2_41-GHz">Z3775D</a></p></td>
<td><p>1.49</p></td>
<td><p>2.41</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2.2W</p></td>
<td><p>DDR3L-RS-1333x1</p></td>
<td><p>10.6</p></td>
<td><p>4</p></td>
<td><p>311</p></td>
<td><p>792</p></td>
<td><p>Q1'14</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/80888/Intel-Atom-Processor-Z3785-2M-Cache-up-to-2_41-GHz">Z3785</a></p></td>
<td><p>1.49</p></td>
<td><p>2.41</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2.2W</p></td>
<td><p>LPDDR3-1333x2</p></td>
<td><p>21.3</p></td>
<td><p>4</p></td>
<td><p>313</p></td>
<td><p>833</p></td>
<td><p>Q2'14</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/80267/Intel-Atom-Processor-Z3795-2M-Cache-up-to-2_39-GHz">Z3795</a></p></td>
<td><p>1.59</p></td>
<td><p>2.39</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2.0W</p></td>
<td><p>LPDDR3-1066x2</p></td>
<td><p>17.1</p></td>
<td><p>4</p></td>
<td><p>311</p></td>
<td><p>778</p></td>
<td><p>Q1'14</p></td>
</tr>
</tbody>
</table>

### スマートフォン/タブレット向け (Merrifield, Moorefield, SoFIA)

[2014年](../Page/2014年.md "wikilink")[2月24日](https://ja.wikipedia.org/wiki/2月24日 "wikilink")発表、スマートフォン/タブレット向け、Clover Trail+の後継製品。Silvermontマイクロアーキテクチャ。プロセスルールは22nm。Z34xx が Merrifield（メリーフィールド）、Z35xx が Moorefield（ムーアフィールド）。

<table>
<caption>Merrifield</caption>
<thead>
<tr class="header">
<th><p>プロセッサーナンバー</p></th>
<th><p>CPU周波数</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>2次キャッシュ</p></th>
<th><p>GPU</p></th>
<th><p>GPU周波数</p></th>
<th><p>メモリ</p></th>
<th><p>モデム</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/70103/Intel-Atom-Processor-Z3460-1MB-Cache-up-to-1_60-GHz">Z3460</a></p></td>
<td><p>1.60 GHz</p></td>
<td><p>2C/2T</p></td>
<td><p>1MB</p></td>
<td><p>PowerVR G6400</p></td>
<td><p>457MHz</p></td>
<td><p>LPDDR3-1066<br />
8.528 GB/s</p></td>
<td><p>XMM 7160 (LTE)</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/70102/Intel-Atom-Processor-Z3480-1MB-Cache-up-to-2_13-GHz">Z3480</a></p></td>
<td><p>2.13 GHz</p></td>
<td><p>533MHz</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<table>
<caption>Moorefield</caption>
<thead>
<tr class="header">
<th><p>プロセッサーナンバー</p></th>
<th><p>CPU周波数</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>2次キャッシュ</p></th>
<th><p>GPU</p></th>
<th><p>GPU周波数</p></th>
<th><p>メモリ</p></th>
<th><p>モデム</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/81195/Intel-Atom-Processor-Z3580-2M-Cache-up-to-2_33-GHz">Z3580</a></p></td>
<td><p>2.33 GHz</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>PowerVR G6430</p></td>
<td><p>533MHz</p></td>
<td><p>LPDDR3-1600<br />
12.8 GB/s</p></td>
<td><p>XMM 7160 (LTE)<br />
XMM 6360 (HSPA+)<br />
XMM 7260 (LTE-Advanced)</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/84324/Intel-Atom-Processor-Z3570-2M-Cache-up-to-2_00-GHz">Z3570</a></p></td>
<td><p>2.00 GHz</p></td>
<td><p>640MHz</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/81194/Intel-Atom-Processor-Z3560-2M-Cache-up-to-1_83-GHz?q=Z3560">Z3560</a></p></td>
<td><p>1.80 GHz</p></td>
<td><p>533MHz</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/84072/Intel-Atom-Processor-Z3530-2M-Cache-up-to-1_33-GHz">Z3530</a></p></td>
<td><p>1.33 GHz</p></td>
<td><p>457MHz</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

  - SoFIA (ソフィア)

[2015年](../Page/2015年.md "wikilink")[3月2日](../Page/3月2日.md "wikilink")発表\[30\]。プロセスルールは28nmであり、インテル社外の半導体製造事業者が製造\[31\]。[x64](https://ja.wikipedia.org/wiki/x64 "wikilink") 対応。このシリーズからモデル名がAtom x3/x5/x7の3種類に細分化され、そのうちAtom x3がこれに属する。

<table>
<caption>SoFIA</caption>
<thead>
<tr class="header">
<th><p>プロセッサーナンバー</p></th>
<th><p>CPU周波数</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>2次キャッシュ</p></th>
<th><p>GPU</p></th>
<th><p>GPU周波数</p></th>
<th><p>メモリ</p></th>
<th><p>モデム</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>x3-C3440</p></td>
<td><p>1.4 GHz</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>Mali T720 MP2</p></td>
<td></td>
<td><p>LPDDR2/3-1066 32bit x 1</p></td>
<td><p>LTE</p></td>
</tr>
<tr class="even">
<td><p>x3-C3230RK</p></td>
<td><p>1.2 GHz</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>Mali 450 MP4</p></td>
<td></td>
<td><p>LPDDR2/3-1066 32bit x 1<br />
DDR3/DDR3L-1333 16bit x 2</p></td>
<td><p>HSPA+</p></td>
</tr>
<tr class="odd">
<td><p>x3-C3230RK</p></td>
<td><p>1.0 GHz</p></td>
<td><p>2C/2T</p></td>
<td><p>1MB</p></td>
<td><p>Mali 400 MP2</p></td>
<td></td>
<td><p>LPDDR2-800 32bit x 1</p></td>
<td><p>HSPA+</p></td>
</tr>
</tbody>
</table>

### サーバー向け (Avoton)

[2013年](../Page/2013年.md "wikilink")[9月4日](../Page/9月4日.md "wikilink")発表。Avoton (アヴァトン) が一般サーバー向け、Rangeley (レンジレイ) がネットワーク機器組み込み向け。Rangeley の方が製品の提供期間が長い（組込み機器向けオプションあり）。Silvermont マイクロアーキテクチャ。メモリは DDR3-1600 デュアルチャンネル (25.6 GB/s)。搭載メモリの最大容量は16GB〜64GB。プロセスルールは22nm。[Intel 64](https://ja.wikipedia.org/wiki/Intel_64 "wikilink"), [Intel VT-x](https://ja.wikipedia.org/wiki/Intel_VT-x "wikilink"), [SSE](../Page/ストリーミングSIMD拡張命令.md "wikilink") 4.2, [AES-NI](https://ja.wikipedia.org/wiki/AES-NI "wikilink") 対応。Rangeley は C2338, C2358 以外はバースト・ブースト・テクノロジー非対応。

| プロセッサーナンバー                                                                                   | 動作周波数（バースト）       | コア/スレッド数 | 2次キャッシュ | [HT対応](../Page/ハイパースレッディング・テクノロジー.md "wikilink") | QuickAssistテクノロジー | [TDP](../Page/熱設計電力.md "wikilink") | 価格   |
| -------------------------------------------------------------------------------------------- | ----------------- | -------- | ------- | ------------------------------------------------ | ----------------- | ---------------------------------- | ---- |
| [C2350](http://ark.intel.com/ja/products/77977/Intel-Atom-Processor-C2350-1M-Cache-1_70-GHz) | 1.7 GHz (2.0 GHz) | 2C/2T    | 1 MB    | ×                                                | ×                 | 6W                                 | $43  |
| [C2530](http://ark.intel.com/ja/products/77980/Intel-Atom-Processor-C2530-2M-Cache-1_70-GHz) | 1.7 GHz (2.0 GHz) | 4C/4T    | 2 MB    | ×                                                | ×                 | 9W                                 | $70  |
| [C2550](http://ark.intel.com/ja/products/77982/Intel-Atom-Processor-C2550-2M-Cache-2_40-GHz) | 2.4 GHz (2.6 GHz) | 4C/4T    | 2 MB    | ×                                                | ×                 | 14W                                | $86  |
| [C2730](http://ark.intel.com/ja/products/77985/Intel-Atom-Processor-C2730-4M-Cache-1_70-GHz) | 1.7 GHz (2.0 GHz) | 8C/8T    | 4 MB    | ×                                                | ×                 | 12W                                | $150 |
| [C2750](http://ark.intel.com/ja/products/77987/Intel-Atom-Processor-C2750-4M-Cache-2_40-GHz) | 2.4 GHz (2.6 GHz) | 8C/8T    | 4 MB    | ×                                                | ×                 | 20W                                | $171 |

Avoton（アヴァトン）

### 組み込み向け (Rangeley)

| プロセッサーナンバー                                                                                    | 動作周波数（バースト）       | コア/スレッド数 | 2次キャッシュ | [HT対応](../Page/ハイパースレッディング・テクノロジー.md "wikilink") | QuickAssistテクノロジー | [TDP](../Page/熱設計電力.md "wikilink") | 価格   |
| --------------------------------------------------------------------------------------------- | ----------------- | -------- | ------- | ------------------------------------------------ | ----------------- | ---------------------------------- | ---- |
| [C2308](http://ark.intel.com/ja/products/81328/Intel-Atom-Processor-C2308-1M-Cache-1_25-GHz)  | 1.25 GHz          | 2C/2T    | 1 MB    | ×                                                | ○                 | 6W                                 |      |
| [C2316](http://ark.intel.com/ja/products/123003/Intel-Atom-Processor-C2316-1M-Cache-1_50-GHz) | 1.5 GHz           | 2C/2T    | 1 MB    | ×                                                | ○                 | 7W                                 |      |
| [C2338](http://ark.intel.com/ja/products/77976/Intel-Atom-Processor-C2338-1M-Cache-1_70-GHz)  | 1.7 GHz (2.0 GHz) | 2C/2T    | 1 MB    | ×                                                | ×                 | 7W                                 |      |
| [C2358](http://ark.intel.com/ja/products/77978/Intel-Atom-Processor-C2358-1M-Cache-1_70-GHz)  | 1.7 GHz (2.0 GHz) | 2C/2T    | 1 MB    | ×                                                | ○                 | 7W                                 |      |
| [C2508](http://ark.intel.com/ja/products/81270/Intel-Atom-Processor-C2508-2M-Cache-1_25-GHz)  | 1.25 GHz          | 4C/4T    | 2 MB    | ×                                                | ○                 | 9.5W                               |      |
| [C2516](http://ark.intel.com/ja/products/123004/Intel-Atom-Processor-C2516-2M-Cache-1_40-GHz) | 1.4 GHz           | 4C/4T    | 2 MB    | ×                                                | ○                 | 10W                                |      |
| [C2518](http://ark.intel.com/ja/products/77979/Intel-Atom-Processor-C2518-2M-Cache-1_70-GHz)  | 1.7 GHz           | 4C/4T    | 2 MB    | ×                                                | ×                 | 13W                                | $75  |
| [C2538](http://ark.intel.com/ja/products/77981/Intel-Atom-Processor-C2538-2M-Cache-2_40-GHz)  | 2.4 GHz           | 4C/4T    | 2 MB    | ×                                                | ×                 | 15W                                |      |
| [C2558](http://ark.intel.com/ja/products/77983/Intel-Atom-Processor-C2558-2M-Cache-2_40-GHz)  | 2.4 GHz           | 4C/4T    | 2 MB    | ×                                                | ○                 | 15W                                | $86  |
| [C2718](http://ark.intel.com/ja/products/77984/Intel-Atom-Processor-C2718-4M-Cache-2_00-GHz)  | 2.0 GHz           | 8C/8T    | 4 MB    | ×                                                | ×                 | 20W                                |      |
| [C2738](http://ark.intel.com/ja/products/77986/Intel-Atom-Processor-C2738-4M-Cache-2_40-GHz)  | 2.4 GHz           | 8C/8T    | 4 MB    | ×                                                | ×                 | 20W                                |      |
| [C2758](http://ark.intel.com/ja/products/77988/Intel-Atom-Processor-C2758-4M-Cache-2_40-GHz)  | 2.4 GHz           | 8C/8T    | 4 MB    | ×                                                | ○                 | 20W                                | $171 |

Rangeley（レンジレイ）

## Airmont マイクロアーキテクチャ

第4世代のAtom向けマイクロアーキテクチャで、[2015年](../Page/2015年.md "wikilink")[3月2日](../Page/3月2日.md "wikilink")発表。プロセスルールは14nm。GPU は第8世代 [Intel HD Graphics](https://ja.wikipedia.org/wiki/Intel_HD_Graphics "wikilink") (Broadwell 世代) 。

### デスクトップ・ノートPC向け (Braswell)

[2015年](../Page/2015年.md "wikilink")[4月7日](../Page/4月7日.md "wikilink")発表\[32\]。デスクトップ・ノートPC向け。Bay Trailの後継製品。コードネーム Braswell (ブラスウェル)。Jが付いているのがデスクトップPC用、Nが付いているのがノートPC用。当初はデスクトップ・ノート共通としてNシリーズのみが発売されたが、後にデスクトップ専用のJシリーズが追加された。

<table>
<caption>Braswell</caption>
<thead>
<tr class="header">
<th><p>プロセッサー<br />
ナンバー</p></th>
<th><p>CPU周波数<br />
(GHz)</p></th>
<th><p>CPUバースト<br />
(GHz)</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>キャッシュ</p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">TDP</a></p></th>
<th><p>メモリ</p></th>
<th><p>メモリ帯域<br />
(GB/s)</p></th>
<th><p>GPU<br />
EU数</p></th>
<th><p>GPU周波数<br />
(MHz)</p></th>
<th><p>GPUバースト<br />
(MHz)</p></th>
<th><p>発売時期</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/87261/Intel-Pentium-Processor-N3700-2M-Cache-up-to-2_40-GHz">Pentium N3700</a></p></td>
<td><p>1.6</p></td>
<td><p>2.4</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>6W</p></td>
<td><p>DDR3L-1600x2</p></td>
<td><p>25.6</p></td>
<td><p>16</p></td>
<td><p>400</p></td>
<td><p>700</p></td>
<td><p>Q1'15</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/91830/Intel-Pentium-Processor-N3710-2M-Cache-up-to-2_56-GHz">Pentium N3710</a></p></td>
<td><p>1.6</p></td>
<td><p>2.56</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>6W</p></td>
<td><p>DDR3L-1600x2</p></td>
<td><p>25.6</p></td>
<td><p>16</p></td>
<td><p>400</p></td>
<td><p>700</p></td>
<td><p>Q1'16</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/91532/Intel-Pentium-Processor-J3710-2M-Cache-up-to-2_64-GHz">Pentium J3710</a></p></td>
<td><p>1.6</p></td>
<td><p>2.64</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>6.5W</p></td>
<td><p>DDR3L-1600x2</p></td>
<td><p>25.6</p></td>
<td><p>16</p></td>
<td><p>400</p></td>
<td><p>740</p></td>
<td><p>Q1'16</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/87259/Intel-Celeron-Processor-N3000-2M-Cache-up-to-2_08-GHz">Celeron N3000</a></p></td>
<td><p>1.04</p></td>
<td><p>2.08</p></td>
<td><p>2C/2T</p></td>
<td><p>2MB</p></td>
<td><p>4W</p></td>
<td><p>DDR3L-1600x2</p></td>
<td><p>25.6</p></td>
<td><p>12</p></td>
<td><p>320</p></td>
<td><p>600</p></td>
<td><p>Q1'15</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/87257/Intel-Celeron-Processor-N3050-2M-Cache-up-to-2_16-GHz">Celeron N3050</a></p></td>
<td><p>1.6</p></td>
<td><p>2.16</p></td>
<td><p>2C/2T</p></td>
<td><p>2MB</p></td>
<td><p>6W</p></td>
<td><p>DDR3L-1600x2</p></td>
<td><p>25.6</p></td>
<td><p>12</p></td>
<td><p>320</p></td>
<td><p>600</p></td>
<td><p>Q1'15</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/87258/Intel-Celeron-Processor-N3150-2M-Cache-up-to-2_08-GHz">Celeron N3150</a></p></td>
<td><p>1.6</p></td>
<td><p>2.08</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>6W</p></td>
<td><p>DDR3L-1600x2</p></td>
<td><p>25.6</p></td>
<td><p>12</p></td>
<td><p>320</p></td>
<td><p>640</p></td>
<td><p>Q1'15</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/91710/Intel-Celeron-Processor-N3010-2M-Cache-up-to-2_24-GHz">Celeron N3010</a></p></td>
<td><p>1.06</p></td>
<td><p>2.24</p></td>
<td><p>2C/2T</p></td>
<td><p>2MB</p></td>
<td><p>4W</p></td>
<td><p>DDR3L-1600x2</p></td>
<td><p>25.6</p></td>
<td><p>12</p></td>
<td><p>320</p></td>
<td><p>600</p></td>
<td><p>Q1'16</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/91831/Intel-Celeron-Processor-N3160-2M-Cache-up-to-2_24-GHz">Celeron N3160</a></p></td>
<td><p>1.6</p></td>
<td><p>2.24</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>6W</p></td>
<td><p>DDR3L-1600x2</p></td>
<td><p>25.6</p></td>
<td><p>12</p></td>
<td><p>320</p></td>
<td><p>640</p></td>
<td><p>Q1'16</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/91832/Intel-Celeron-Processor-N3060-2M-Cache-up-to-2_48-GHz">Celeron N3060</a></p></td>
<td><p>1.6</p></td>
<td><p>2.48</p></td>
<td><p>2C/2T</p></td>
<td><p>2MB</p></td>
<td><p>6W</p></td>
<td><p>DDR3L-1600x2</p></td>
<td><p>25.6</p></td>
<td><p>12</p></td>
<td><p>320</p></td>
<td><p>600</p></td>
<td><p>Q1'16</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/91533/Intel-Celeron-Processor-J3160-2M-Cache-up-to-2_24-GHz">Celeron J3160</a></p></td>
<td><p>1.6</p></td>
<td><p>2.24</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>6W</p></td>
<td><p>DDR3L-1600x2</p></td>
<td><p>25.6</p></td>
<td><p>12</p></td>
<td><p>320</p></td>
<td><p>700</p></td>
<td><p>Q1'16</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/91534/Intel-Celeron-Processor-J3060-2M-Cache-up-to-2_48-GHz">Celeron J3060</a></p></td>
<td><p>1.6</p></td>
<td><p>2.48</p></td>
<td><p>2C/2T</p></td>
<td><p>2MB</p></td>
<td><p>6W</p></td>
<td><p>DDR3L-1600x2</p></td>
<td><p>25.6</p></td>
<td><p>12</p></td>
<td><p>320</p></td>
<td><p>700</p></td>
<td><p>Q1'16</p></td>
</tr>
</tbody>
</table>

### 組み込み向け (Braswell)

<table>
<caption>Braswell</caption>
<thead>
<tr class="header">
<th><p>プロセッサー<br />
ナンバー</p></th>
<th><p>CPU周波数<br />
(GHz)</p></th>
<th><p>CPUバースト<br />
(GHz)</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>キャッシュ</p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">TDP</a></p></th>
<th><p>メモリ</p></th>
<th><p>メモリ帯域<br />
(GB/s)</p></th>
<th><p>GPU<br />
EU数</p></th>
<th><p>GPU周波数<br />
(MHz)</p></th>
<th><p>GPUバースト<br />
(MHz)</p></th>
<th><p>発売時期</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/92124/Intel-Atom-Processor-x5-E8000-2M-Cache-up-to-2_00-GHz">x5-E8000</a></p></td>
<td><p>1.04</p></td>
<td><p>2.0</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>5W</p></td>
<td><p>DDR3L-1600x2</p></td>
<td><p>25.6</p></td>
<td><p>12</p></td>
<td><p>320</p></td>
<td></td>
<td><p>Q1'16</p></td>
</tr>
</tbody>
</table>

### タブレットPC向け (Cherry Trail)

[2015年](../Page/2015年.md "wikilink")[3月2日](../Page/3月2日.md "wikilink")発表\[33\]。タブレットPC向け。Bay Trailの後継製品。コードネーム Cherry Trail (チェリートレイル)。このシリーズではモデル名がAtom x3/x5/x7の3種類に細分化され、そのうちAtom x5とx7がこれに属する。

<table>
<caption>Cherry Trail</caption>
<thead>
<tr class="header">
<th><p>プロセッサー<br />
ナンバー</p></th>
<th><p>CPU周波数<br />
(GHz)</p></th>
<th><p>CPUバースト<br />
(GHz)</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>キャッシュ</p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">SDP</a></p></th>
<th><p>メモリ</p></th>
<th><p>メモリ帯域<br />
(GB/s)</p></th>
<th><p>GPU<br />
EU数</p></th>
<th><p>GPU周波数<br />
(MHz)</p></th>
<th><p>GPUバースト<br />
(MHz)</p></th>
<th><p>発売時期</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/85475/Intel-Atom-x7-Z8700-Processor-2M-Cache-up-to-2_40-GHz">x7-Z8700</a></p></td>
<td><p>1.6</p></td>
<td><p>2.4</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2W</p></td>
<td><p>LPDDR3-1600 x 2</p></td>
<td><p>25.6</p></td>
<td><p>16</p></td>
<td><p>200</p></td>
<td><p>600</p></td>
<td><p>Q1'15</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/93362/Intel-Atom-x7-Z8750-Processor-2M-Cache-up-to-2_56-GHz">x7-Z8750</a></p></td>
<td><p>1.6</p></td>
<td><p>2.56</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2W</p></td>
<td><p>LPDDR3-1600 x 2</p></td>
<td><p>25.6</p></td>
<td><p>16</p></td>
<td><p>200</p></td>
<td><p>600</p></td>
<td><p>Q1'16</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/85474/Intel-Atom-x5-Z8500-Processor-2M-Cache-up-to-2_24-GHz?q=Intel%C2%AE%20Atom%E2%84%A2%20x5-Z8500%20Processor%20%282M%20Cache,%20up%20to%202.24%20GHz%29">x5-Z8500</a></p></td>
<td><p>1.44</p></td>
<td><p>2.24</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2W</p></td>
<td><p>LPDDR3-1600 x 2</p></td>
<td><p>25.6</p></td>
<td><p>12</p></td>
<td><p>200</p></td>
<td><p>600</p></td>
<td><p>Q1'15</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/87383/Intel-Atom-x5-Z8300-Processor-2M-Cache-up-to-1_84-GHz">x5-Z8300</a></p></td>
<td><p>1.44</p></td>
<td><p>1.84</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2W</p></td>
<td><p>DDR3L-RS-1600 x 1</p></td>
<td><p>12.8</p></td>
<td><p>12</p></td>
<td><p>200</p></td>
<td><p>500</p></td>
<td><p>Q2'15</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/91564/Intel-Atom-x5-Z8330-Processor-2M-Cache-up-to-1_92-GHz">x5-Z8330</a></p></td>
<td><p>1.44</p></td>
<td><p>1.92</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2W</p></td>
<td><p>DDR3L-RS-1600 x 1</p></td>
<td><p>12.8</p></td>
<td><p>12</p></td>
<td><p>200</p></td>
<td><p>500</p></td>
<td><p>Q1'16</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/93361/Intel-Atom-x5-Z8350-Processor-2M-Cache-up-to-1_92-GHz">x5-Z8350</a></p></td>
<td><p>1.44</p></td>
<td><p>1.92</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2W</p></td>
<td><p>DDR3L-RS-1600 x 1</p></td>
<td><p>12.8</p></td>
<td><p>12</p></td>
<td><p>200</p></td>
<td><p>500</p></td>
<td><p>Q1'16</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/93360/Intel-Atom-x5-Z8550-Processor-2M-Cache-up-to-2_40-GHz">x5-Z8550</a></p></td>
<td><p>1.44</p></td>
<td><p>2.4</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>2W</p></td>
<td><p>DDR3L-RS-1600 x 2</p></td>
<td><p>25.6</p></td>
<td><p>12</p></td>
<td><p>200</p></td>
<td><p>600</p></td>
<td><p>Q1'16</p></td>
</tr>
</tbody>
</table>

## Goldmont マイクロアーキテクチャ

第5世代のAtom向けマイクロアーキテクチャで、[2016年](../Page/2016年.md "wikilink")[9月1日](../Page/9月1日.md "wikilink")発表。プロセスルールは14nm。GPU は第9世代 [Intel HD Graphics](https://ja.wikipedia.org/wiki/Intel_HD_Graphics "wikilink") (Skylake 世代) 。

### デスクトップ・ノートPC向け (Apollo Lake)

Jが付いているのがデスクトップ用、Nが付いているのがノートPC用。

<table>
<caption>Apollo Lake（アポロレイク）</caption>
<thead>
<tr class="header">
<th><p>プロセッサー<br />
ナンバー</p></th>
<th><p>CPU周波数<br />
(GHz)</p></th>
<th><p>CPUバースト<br />
(GHz)</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>キャッシュ</p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">TDP</a></p></th>
<th><p>メモリ</p></th>
<th><p>メモリ帯域<br />
(GB/s)</p></th>
<th><p>GPU<br />
EU数</p></th>
<th><p>GPU周波数<br />
(MHz)</p></th>
<th><p>GPUバースト<br />
(MHz)</p></th>
<th><p>発売時期</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/95591/Intel-Pentium-Processor-J4205-2M-Cache-up-to-2_6-GHz">Pentium J4205</a></p></td>
<td><p>1.5</p></td>
<td><p>2.6</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>10W</p></td>
<td><p>DDR3L/LPDDR3-1866x2, LPDDR4-2400x2</p></td>
<td><p>29.8, 38.4</p></td>
<td><p>18</p></td>
<td><p>250</p></td>
<td><p>800</p></td>
<td><p>Q3'16</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/95594/Intel-Celeron-Processor-J3455-2M-Cache-up-to-2_3-GHz">Celeron J3455</a></p></td>
<td><p>1.5</p></td>
<td><p>2.3</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>10W</p></td>
<td><p>DDR3L/LPDDR3-1866x2, LPDDR4-2400x2</p></td>
<td><p>29.8, 38.4</p></td>
<td><p>12</p></td>
<td><p>250</p></td>
<td><p>750</p></td>
<td><p>Q3'16</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/95597/Intel-Celeron-Processor-J3355-2M-Cache-up-to-2_5-GHz">Celeron J3355</a></p></td>
<td><p>2.0</p></td>
<td><p>2.5</p></td>
<td><p>2C/2T</p></td>
<td><p>2MB</p></td>
<td><p>10W</p></td>
<td><p>DDR3L/LPDDR3-1866x2, LPDDR4-2400x2</p></td>
<td><p>29.8, 38.4</p></td>
<td><p>12</p></td>
<td><p>250</p></td>
<td><p>700</p></td>
<td><p>Q3'16</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/95592/Intel-Pentium-Processor-N4200-2M-Cache-up-to-2_5-GHz">Pentium N4200</a></p></td>
<td><p>1.1</p></td>
<td><p>2.5</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>6W</p></td>
<td><p>DDR3L/LPDDR3-1866x2, LPDDR4-2400x2</p></td>
<td><p>29.8, 38.4</p></td>
<td><p>18</p></td>
<td><p>200</p></td>
<td><p>750</p></td>
<td><p>Q3'16</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/95596/Intel-Celeron-Processor-N3450-2M-Cache-up-to-2_2-GHz">Celeron N3450</a></p></td>
<td><p>1.1</p></td>
<td><p>2.2</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>6W</p></td>
<td><p>DDR3L/LPDDR3-1866x2, LPDDR4-2400x2</p></td>
<td><p>29.8, 38.4</p></td>
<td><p>12</p></td>
<td><p>200</p></td>
<td><p>700</p></td>
<td><p>Q3'16</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/95598/Intel-Celeron-Processor-N3350-2M-Cache-up-to-2_4-GHz">Celeron N3350</a></p></td>
<td><p>1.1</p></td>
<td><p>2.4</p></td>
<td><p>2C/2T</p></td>
<td><p>2MB</p></td>
<td><p>6W</p></td>
<td><p>DDR3L/LPDDR3-1866x2, LPDDR4-2400x2</p></td>
<td><p>29.8, 38.4</p></td>
<td><p>12</p></td>
<td><p>200</p></td>
<td><p>650</p></td>
<td><p>Q3'16</p></td>
</tr>
</tbody>
</table>

### 組み込み向け (Apollo Lake)

<table>
<caption>Apollo Lake（アポロレイク）</caption>
<thead>
<tr class="header">
<th><p>プロセッサー<br />
ナンバー</p></th>
<th><p>CPU周波数<br />
(GHz)</p></th>
<th><p>CPUバースト<br />
(GHz)</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>キャッシュ</p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">TDP</a></p></th>
<th><p>メモリ</p></th>
<th><p>メモリ帯域<br />
(GB/s)</p></th>
<th><p>GPU<br />
EU数</p></th>
<th><p>GPU周波数<br />
(MHz)</p></th>
<th><p>GPUバースト<br />
(MHz)</p></th>
<th><p>発売時期</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/96488/Intel-Atom-x7-E3950-Processor-2M-Cache-up-to-2_00-GHz">x7-E3950</a></p></td>
<td><p>1.6</p></td>
<td><p>2.0</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>12W</p></td>
<td><p>DDR3L-1866, LPDDR4-2400</p></td>
<td><p>29.8, 38.4</p></td>
<td><p>18</p></td>
<td><p>500</p></td>
<td><p>650</p></td>
<td><p>Q4'16</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/96485/Intel-Atom-x5-E3940-Processor-2M-Cache-up-to-1_80-GHz">x5-E3940</a></p></td>
<td><p>1.6</p></td>
<td><p>1.8</p></td>
<td><p>4C/4T</p></td>
<td><p>2MB</p></td>
<td><p>9.5W</p></td>
<td><p>DDR3L-1866, LPDDR4-2133</p></td>
<td><p>29.8, 34.1</p></td>
<td><p>12</p></td>
<td><p>400</p></td>
<td><p>600</p></td>
<td><p>Q4'16</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/96486/Intel-Atom-x5-E3930-Processor-2M-Cache-up-to-1_80-GHz">x5-E3930</a></p></td>
<td><p>1.3</p></td>
<td><p>1.8</p></td>
<td><p>2C/2T</p></td>
<td><p>2MB</p></td>
<td><p>6.5W</p></td>
<td><p>DDR3L-1866, LPDDR4-2133</p></td>
<td><p>29.8, 34.1</p></td>
<td><p>12</p></td>
<td><p>400</p></td>
<td><p>550</p></td>
<td><p>Q4'16</p></td>
</tr>
</tbody>
</table>

### 組み込み向け (Joule)

2016年8月に発表し、2017年6月16日に製造終了。

<table>
<caption>Joule（ジョール）</caption>
<thead>
<tr class="header">
<th><p>プロセッサー<br />
ナンバー</p></th>
<th><p>CPU周波数<br />
(GHz)</p></th>
<th><p>CPUバースト<br />
(GHz)</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>キャッシュ</p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">TDP</a></p></th>
<th><p>メモリ</p></th>
<th><p>メモリ帯域<br />
(GB/s)</p></th>
<th><p>GPU<br />
EU数</p></th>
<th><p>GPU周波数<br />
(MHz)</p></th>
<th><p>GPUバースト<br />
(MHz)</p></th>
<th><p>発売時期</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/96414/Intel-Joule-570x-Developer-Kit">Joule 570x</a><br />
(Atom T5700)</p></td>
<td><p>1.7</p></td>
<td><p>2.4</p></td>
<td><p>4C/4T</p></td>
<td><p>4MB</p></td>
<td></td>
<td><p>LPDDR4 x4</p></td>
<td><p>25.6</p></td>
<td><p>18</p></td>
<td><p>450</p></td>
<td><p>650</p></td>
<td><p>Q3'16</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/96415/Intel-Joule-550x-Developer-Kit">Joule 550x</a><br />
(Atom T5500)</p></td>
<td><p>1.5</p></td>
<td></td>
<td><p>4C/4T</p></td>
<td><p>4MB</p></td>
<td></td>
<td><p>LPDDR4 x4</p></td>
<td><p>25.6</p></td>
<td><p>12</p></td>
<td><p>300</p></td>
<td></td>
<td><p>Q4'16</p></td>
</tr>
</tbody>
</table>

### サーバー向け (Denverton)

GPU無し。

<table>
<caption>Denverton（デンバートン）</caption>
<thead>
<tr class="header">
<th><p>プロセッサー<br />
ナンバー</p></th>
<th><p>CPU周波数<br />
(GHz)</p></th>
<th><p>CPUバースト<br />
(GHz)</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>キャッシュ</p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">TDP</a></p></th>
<th><p>メモリ</p></th>
<th><p>メモリ帯域<br />
(GB/s)</p></th>
<th><p>発売時期</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/97935/Intel-Atom-Processor-C3308-4M-Cache-up-to-2_10-GHz">C3308</a></p></td>
<td><p>1.6</p></td>
<td><p>2.1</p></td>
<td><p>2C/2T</p></td>
<td><p>4MB</p></td>
<td><p>9.5W</p></td>
<td><p>DDR4-1866</p></td>
<td></td>
<td><p>Q3'17</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/97928/Intel-Atom-Processor-C3338-4M-Cache-up-to-2_20-GHz">C3338</a></p></td>
<td><p>1.5</p></td>
<td><p>2.2</p></td>
<td><p>2C/2T</p></td>
<td><p>4MB</p></td>
<td><p>9W</p></td>
<td><p>DDR4-1866</p></td>
<td></td>
<td><p>Q1'17</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/97930/Intel-Atom-Processor-C3508-8M-Cache-up-to-1_60-GHz">C3508</a></p></td>
<td><p>1.6</p></td>
<td><p>1.6</p></td>
<td><p>4C/4T</p></td>
<td><p>8MB</p></td>
<td><p>11.25W</p></td>
<td><p>DDR4-1866</p></td>
<td></td>
<td><p>Q3'17</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/97929/Intel-Atom-Processor-C3538-8M-Cache-up-to-2_10-GHz">C3538</a></p></td>
<td><p>2.1</p></td>
<td><p>2.1</p></td>
<td><p>4C/4T</p></td>
<td><p>8MB</p></td>
<td><p>15W</p></td>
<td><p>DDR4-1866</p></td>
<td></td>
<td><p>Q3'17</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/97937/Intel-Atom-Processor-C3558-8M-Cache-up-to-2_20-GHz">C3558</a></p></td>
<td><p>2.2</p></td>
<td><p>2.2</p></td>
<td><p>4C/4T</p></td>
<td><p>8MB</p></td>
<td><p>16W</p></td>
<td><p>DDR4-1866</p></td>
<td></td>
<td><p>Q3'17</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/97934/Intel-Atom-Processor-C3708-16M-Cache-up-to-1_70-GHz">C3708</a></p></td>
<td><p>1.7</p></td>
<td><p>1.7</p></td>
<td><p>8C/8T</p></td>
<td><p>16MB</p></td>
<td><p>17W</p></td>
<td><p>DDR4-2133</p></td>
<td></td>
<td><p>Q3'17</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/97938/Intel-Atom-Processor-C3750-16M-Cache-up-to-2_40-GHz">C3750</a></p></td>
<td><p>2.2</p></td>
<td><p>2.4</p></td>
<td><p>8C/8T</p></td>
<td><p>16MB</p></td>
<td><p>21W</p></td>
<td><p>DDR4-2133</p></td>
<td></td>
<td><p>Q3'17</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/97926/Intel-Atom-Processor-C3758-16M-Cache-up-to-2_20-GHz">C3758</a></p></td>
<td><p>2.2</p></td>
<td><p>2.2</p></td>
<td><p>8C/8T</p></td>
<td><p>16MB</p></td>
<td><p>25W</p></td>
<td><p>DDR4-2133</p></td>
<td></td>
<td><p>Q3'17</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/97939/Intel-Atom-Processor-C3808-12M-Cache-up-to-2_0-GHz">C3808</a></p></td>
<td><p>2.0</p></td>
<td><p>2.0</p></td>
<td><p>12C/12T</p></td>
<td><p>12MB</p></td>
<td><p>25W</p></td>
<td><p>DDR4-2133</p></td>
<td></td>
<td><p>Q3'17</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/97932/Intel-Atom-Processor-C3850-12M-Cache-up-to-2_40-GHz">C3850</a></p></td>
<td><p>2.1</p></td>
<td><p>2.4</p></td>
<td><p>12C/12T</p></td>
<td><p>12MB</p></td>
<td><p>25W</p></td>
<td><p>DDR4-2400</p></td>
<td></td>
<td><p>Q3'17</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/97936/Intel-Atom-Processor-C3858-12M-Cache-up-to-2_0-GHz">C3858</a></p></td>
<td><p>2.0</p></td>
<td><p>2.0</p></td>
<td><p>12C/12T</p></td>
<td><p>12MB</p></td>
<td><p>25W</p></td>
<td><p>DDR4-2400</p></td>
<td></td>
<td><p>Q3'17</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/97931/Intel-Atom-Processor-C3830-12M-Cache-up-to-2_30-GHz">C3830</a></p></td>
<td><p>1.9</p></td>
<td><p>2.3</p></td>
<td><p>12C/12T</p></td>
<td><p>12MB</p></td>
<td><p>21W</p></td>
<td><p>DDR4-2133</p></td>
<td></td>
<td><p>Q3'17</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/97940/Intel-Atom-Processor-C3950-16M-Cache-up-to-2_20-GHz">C3950</a></p></td>
<td><p>1.7</p></td>
<td><p>2.2</p></td>
<td><p>16C/16T</p></td>
<td><p>16MB</p></td>
<td><p>24W</p></td>
<td><p>DDR4-2400</p></td>
<td></td>
<td><p>Q3'17</p></td>
</tr>
<tr class="even">
<td><p><a href="http://ark.intel.com/ja/products/97933/Intel-Atom-Processor-C3955-16M-Cache-up-to-2_40-GHz">C3955</a></p></td>
<td><p>2.1</p></td>
<td><p>2.4</p></td>
<td><p>16C/16T</p></td>
<td><p>16MB</p></td>
<td><p>32W</p></td>
<td><p>DDR4-2400</p></td>
<td></td>
<td><p>Q3'17</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://ark.intel.com/ja/products/97927/Intel-Atom-Processor-C3958-16M-Cache-up-to-2_0-GHz">C3958</a></p></td>
<td><p>2.0</p></td>
<td><p>2.0</p></td>
<td><p>16C/16T</p></td>
<td><p>16MB</p></td>
<td><p>31W</p></td>
<td><p>DDR4-2400</p></td>
<td></td>
<td><p>Q3'17</p></td>
</tr>
</tbody>
</table>

## Goldmont Plus マイクロアーキテクチャ

第6世代のAtom向けマイクロアーキテクチャで、[2017年](../Page/2017年.md "wikilink")[12月11日](../Page/12月11日.md "wikilink")発表。プロセスルールは14nm。GPU は第9.5世代 [Intel HD Graphics](https://ja.wikipedia.org/wiki/Intel_HD_Graphics "wikilink") (Kaby Lake 世代) 。

### デスクトップ・ノートPC向け (Gemini Lake)

Jが付いているのがデスクトップ用、Nが付いているのがノートPC用。

<table>
<caption>Gemini Lake（ジェミニレイク）</caption>
<thead>
<tr class="header">
<th><p>プロセッサー<br />
ナンバー</p></th>
<th><p>CPU周波数<br />
(GHz)</p></th>
<th><p>CPUバースト<br />
(GHz)</p></th>
<th><p>コア/スレッド数</p></th>
<th><p>キャッシュ</p></th>
<th><p><a href="../Page/熱設計電力.md" title="wikilink">TDP</a></p></th>
<th><p>メモリ</p></th>
<th><p>メモリ帯域<br />
(GB/s)</p></th>
<th><p>GPU<br />
EU数</p></th>
<th><p>GPU周波数<br />
(MHz)</p></th>
<th><p>GPUバースト<br />
(MHz)</p></th>
<th><p>発売時期</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ark.intel.com/ja/products/128984/Intel-Pentium-Silver-Processor-J5005-4M-Cache-up-to-2_80-GHz">Pentium Silver J5005</a></p></td>
<td><p>1.5</p></td>
<td><p>2.8</p></td>
<td><p>4C/4T</p></td>
<td><p>4MB</p></td>
<td><p>10W</p></td>
<td><p>DDR4/LPDDR4-2400</p></td>
<td></td>
<td></td>
<td><p>250</p></td>
<td><p>800</p></td>
<td><p>Q4'17</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ark.intel.com/ja/products/128990/Intel-Pentium-Silver-Processor-N5000-4M-Cache-up-to-2_70-GHz">Pentium Silver N5000</a></p></td>
<td><p>1.1</p></td>
<td><p>2.7</p></td>
<td><p>4C/4T</p></td>
<td><p>4MB</p></td>
<td><p>6W</p></td>
<td><p>DDR4/LPDDR4-2400</p></td>
<td></td>
<td></td>
<td><p>200</p></td>
<td><p>750</p></td>
<td><p>Q4'17</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ark.intel.com/ja/products/128989/Intel-Celeron-Processor-J4105-4M-Cache-up-to-2_50-GHz">Celeron J4105</a></p></td>
<td><p>1.5</p></td>
<td><p>2.5</p></td>
<td><p>4C/4T</p></td>
<td><p>4MB</p></td>
<td><p>10W</p></td>
<td><p>DDR4/LPDDR4-2400</p></td>
<td></td>
<td></td>
<td><p>250</p></td>
<td><p>750</p></td>
<td><p>Q4'17</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ark.intel.com/ja/products/128992/Intel-Celeron-Processor-J4005-4M-Cache-up-to-2_70-GHz">Celeron J4005</a></p></td>
<td><p>2.0</p></td>
<td><p>2.7</p></td>
<td><p>2C/2T</p></td>
<td><p>4MB</p></td>
<td><p>10W</p></td>
<td><p>DDR4/LPDDR4-2400</p></td>
<td></td>
<td></td>
<td><p>250</p></td>
<td><p>700</p></td>
<td><p>Q4'17</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ark.intel.com/ja/products/128983/Intel-Celeron-Processor-N4100-4M-Cache-up-to-2_40-GHz">Celeron N4100</a></p></td>
<td><p>1.1</p></td>
<td><p>2.4</p></td>
<td><p>4C/4T</p></td>
<td><p>4MB</p></td>
<td><p>6W</p></td>
<td><p>DDR4/LPDDR4-2400</p></td>
<td></td>
<td></td>
<td><p>200</p></td>
<td><p>700</p></td>
<td><p>Q4'17</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ark.intel.com/ja/products/128988/Intel-Celeron-Processor-N4000-4M-Cache-up-to-2_60-GHz">Celeron N4000</a></p></td>
<td><p>1.1</p></td>
<td><p>2.6</p></td>
<td><p>2C/2T</p></td>
<td><p>4MB</p></td>
<td><p>6W</p></td>
<td><p>DDR4/LPDDR4-2400</p></td>
<td></td>
<td></td>
<td><p>200</p></td>
<td><p>650</p></td>
<td><p>Q4'17</p></td>
</tr>
</tbody>
</table>

## 脚注

## 関連項目

  - [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")
  - [Ultra-Mobile PC](../Page/Ultra-Mobile_PC.md "wikilink")
  - [System-on-a-chip](../Page/System-on-a-chip.md "wikilink")
  - [Intel Core 2](../Page/Intel_Core_2.md "wikilink")
  - [ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")
  - [NVIDIA ION](https://ja.wikipedia.org/wiki/NVIDIA_ION "wikilink")

## 外部リンク

  - [Atomホームページ](http://www.intel.co.jp/content/www/jp/ja/processors/atom/atom-processor.html)
  - [Atomホームページ](http://www.intel.com/content/www/us/en/processors/atom/atom-processor.html)

[Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink")

1.
2.
3.  [Intel、22nm世代のAtom CPUコア「Silvermont」の詳細を公表](http://pc.watch.impress.co.jp/docs/column/ubiq/20130507_598283.html)
4.  [Atomシリーズを終了：Intel、モバイル向けSoC事業を廃止 (1/3) - EE Times Japan](http://eetimes.jp/ee/articles/1605/06/news060.html)
5.  [Intel Quietly Launches Apollo Lake SoC: Goldmont CPU, 6 SKUs, 6 & 10 Watts](http://www.anandtech.com/show/10635/intel-quietly-launches-apollo-lake-soc)
6.  [Intel Atom Processor Z5xx Series Datasheet](http://download.intel.com/design/chipsets/embedded/datashts/319535.pdf) - Apr 2008 Intel
7.  [IEEE Spectrum: The High-k Solution](http://spectrum.ieee.org/oct07/5553/6) - Mark T. Bohr, Robert S. Chau, Tahir Ghani, and Kaizad Mistry - 2008
8.  [疑似クアッドコアのAtom 330、消費電力が上昇：ニュース](http://pc.nikkeibp.co.jp/article/news/20080922/1008163/)
9.  [【特別企画】台湾ネットブック開発者インタビュー MSI編](http://pc.watch.impress.co.jp/docs/2008/0917/netbook01.htm)
10. インテル (2009年12月21日).
11. [Technology@Intel · Deciphering Intel codewords for Mobile Internet Devices (MIDs)](http://blogs.intel.com/technology/2008/04/deciphering_intel_codewords_fo.php)
12.
13. [【PC Watch】 Intel、Atom ZやUS15Xなどを2011年5月に生産終了](http://pc.watch.impress.co.jp/docs/news/20101104_404455.html)
14. BPT - Intel Burst Performance Technology
15. High frequency mode
16. [【PC Watch】 Intel、タブレット向けプロセッサ「Atom Z670」を発表](http://pc.watch.impress.co.jp/docs/news/20110412_438993.html)
17. [Intel Atom Processor Z6xx Series Datasheet](http://www.intel.co.jp/content/dam/www/public/us/en/documents/datasheets/atom-z6xx-datasheet.pdf)
18. [日経BP](http://itpro.nikkeibp.co.jp/article/NEWS/20080109/290673/)
19.
20.
21. [intel社のページ](http://newsroom.intel.com/community/intel_newsroom/blog/2010/11/22/intel-expands-customer-choice-with-first-configurable-intel-atom-based-processor?cid=rss-258152-c1-262280)
22. [インプレス PC.watch「後藤弘茂のWeekly海外ニュース」](http://pc.watch.impress.co.jp/docs/column/kaigai/20100421_362519.html)
23. 従来"“Stellarton"と呼ばれていたコアがE665CT、E645CT、E665C、E645に用いられるという情報がある。[1](http://www.techpowerup.com/135023/Intel-Expands-Customer-Choice-with-First-Configurable-Intel-Atom-based-Processor.html)
24. [Intel Atom Processor Z2760 Datasheet](http://www.intel.com/content/dam/www/public/us/en/documents/product-briefs/atom-z2760-datasheet.pdf)
25. [MWC2011 IntelがAtom系列の32nm品「Medfield」のサンプル出荷を開始 - ニュース：ITpro](http://itpro.nikkeibp.co.jp/article/NEWS/20110215/357203/)
26.
27. [Intel Atom Microarchitecture for Tables and Smartphones](http://cache-www.intel.com/cd/00/00/51/61/516193_516193.pdf)
28.
29. [【仮想化道場】 サーバー向けのAtomプロセッサが登場、2013年はマイクロサーバー元年となるか？ -クラウド Watch](http://cloud.watch.impress.co.jp/docs/column/virtual/20121213_578476.html)
30. [【イベントレポート】Intel、3G/LTE統合型SoC「Atom x3 C3000」シリーズ - PC Watch](http://pc.watch.impress.co.jp/docs/news/event/20150302_690696.html)
31. [Intel，「Atom x7」「Atom x5」「Atom x3」の概要を発表。タブレット向けのAtom x7＆x5は「Cherry Trail＋第8世代グラフィックス」に - 4Gamer.net](http://www.4gamer.net/games/293/G029300/20150302049/)
32. [Intel Marks 30 Years in China with New Products, Investments and Collaborations](http://newsroom.intel.com/community/intel_newsroom/blog/2015/04/07/intel-marks-30-years-in-china-with-new-products-investments-and-collaborations)
33. [【イベントレポート】Intel、14nmのCherry TrailをAtom x7/x5として正式発表 ～GPUが大幅に性能向上 - PC Watch](http://pc.watch.impress.co.jp/docs/news/event/20150302_690736.html)