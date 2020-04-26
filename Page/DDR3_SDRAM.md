> この記事は[DDR3 SDRAM](https://ja.wikipedia.org/wiki/DDR3_SDRAM)から翻訳されています。


[4GB_DDR3_SO-DIMM.jpg](https://ja.wikipedia.org/wiki/File:4GB_DDR3_SO-DIMM.jpg "fig:4GB_DDR3_SO-DIMM.jpg") **DDR3 SDRAM** (Double-Data-Rate3 Synchronous Dynamic Random Access Memory) は半導体[集積回路](../Page/集積回路.md "wikilink")で構成される[DRAMの規格の一種である](../Page/Dynamic_Random_Access_Memory.md "wikilink")。

2007年頃から[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")の[主記憶装置](../Page/主記憶装置.md "wikilink")などに用いられるようになり、2010年後半まで市場の主流として各種デバイスで用いられた。[スマートデバイス](https://ja.wikipedia.org/wiki/スマートデバイス "wikilink")などの組み込み向けとしても、2013年以降の高性能品（ARM Cortex-A15など）に使われるようになった。インテルは[Nehalemマイクロアーキテクチャ](https://ja.wikipedia.org/wiki/Nehalemマイクロアーキテクチャ "wikilink")（[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")）から使用している。

<div class="toclimit-3">

__TOC__

</div>

## 規格の概要

DDR3 SDRAMの規格として以下が定義されている。 DDR3 SDRAMのメモリにはチップ規格とモジュール規格の2つの規格が存在している。チップ規格はメモリチップの最大動作周波数を、モジュール規格はメモリモジュールの最大転送速度を示す\[1\]。 8ビットずつの[プリフェッチ](../Page/プリフェッチ.md "wikilink")（prefetch, CPUがデータを必要とする前に、メモリから先読みして取り出す）機能をそなえ、データ転送最大速度は理論上[DDR2 SDRAMの](../Page/DDR2_SDRAM.md "wikilink")2倍である。

また、動作電源電圧は、[DDR SDRAMの](../Page/DDR_SDRAM.md "wikilink")2.5V/2.6V、DDR2 SDRAMの1.8Vに対し、DDR3 SDRAMは1.5V、DDR3L SDRAMは1.35V動作となっており、より一層の消費電力の低減、低発熱が実現されている。

[2005年](../Page/2005年.md "wikilink")に、主に[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")や[サーバ](../Page/サーバ.md "wikilink")のメインメモリ用の規格として策定され、[2007年](../Page/2007年.md "wikilink")から市場に出回り始めた\[2\]。DDR3 SDRAMに最初に対応したチップセットは、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")では2007年中頃にリリースされた[3 Series](https://ja.wikipedia.org/wiki/インテル_チップセット#Intel_3_Series "wikilink")[チップセット](../Page/チップセット.md "wikilink")、[AMDでは](https://ja.wikipedia.org/wiki/Advanced_Micro_Devices "wikilink")[2009年](../Page/2009年.md "wikilink")第1[四半期](https://ja.wikipedia.org/wiki/四半期 "wikilink")にリリースされた[Socket AM3である](https://ja.wikipedia.org/wiki/Socket_AM3 "wikilink")。インテルの場合、主に [Core i](https://ja.wikipedia.org/wiki/Intel_Core_i7 "wikilink") シリーズのCPU世代から主流になったメモリ規格である。DDR3-1333×2 (21GB/s）や DDR3-1066×3 (25.6GB/s) という組み合わせから始まった。

発売当時はDDR2 SDRAMの値ごなれが進んでおり、それとの価格差が大きかったため\[3\]、当初DDR3専用だったインテル[プラットフォーム用チップセットも](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")、結局DDR2 SDRAMにも対応した。2010年には[Intel Core i7の登場](https://ja.wikipedia.org/wiki/Intel_Core_i7 "wikilink")（内蔵のメモリーコントローラがDDR3専用）や、AMDのSocket AM3の登場もあり、DDR3とDDR2の価格差は小さくなった。\[4\]

[2012年](../Page/2012年.md "wikilink")には低電圧・低消費電力仕様のLPDDR3が発表され、[2013年](../Page/2013年.md "wikilink")頃からLPDDR3を内蔵した[SoCを搭載した](../Page/System-on-a-chip.md "wikilink")[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")や[タブレットコンピュータ](https://ja.wikipedia.org/wiki/タブレットコンピュータ "wikilink")が市場に出回りはじめている。

後継として、[DDR4 SDRAMが予定されており](https://ja.wikipedia.org/wiki/DDR4_SDRAM "wikilink")、[2015年](../Page/2015年.md "wikilink")ごろから市場に出回ると予想され\[5\]、2017年にはDDR4が市場シェア50%を越え世代交代が進んでいった。

なお、[VRAM](../Page/VRAM.md "wikilink")用の[GDDR3](../Page/GDDR3.md "wikilink")と混同されやすいが別の規格であり、互換性はない。

### レイテンシ

典型的なSDRAMモジュールへのアクセスレイテンシを比較すると、JEDEC準拠のDDR2デバイスはCL=5、5-5-5-15であったが、DDR3標準では、DDR3-1066(CL=7、7-7-7-20)、DDR3-1333(CL=9、9-9-9-24)、DDR3-1600(CL=11、11-11-11-28)である。

DDR3のレイテンシの数値はDDR2より大きい。それはI/Oバスのクロックサイクルがより短いからである。実際の時間間隔はほぼ13 nsと、DDR2のレイテンシと似通っている。新しいプロセスルールで製造されるDDR3はさらに改善が見込まれる。

以前のメモリ世代と同じように、初期のバージョンのリリースの後に、より速いDDR3メモリも利用可能になった。 DDR3-2000メモリは9-9-9-28レイテンシ(9ns)がIntel Core i7が間に合うようリリースされた\[6\]。 CASレイテンシの9とは1000MHz(DDR3-2000)において9nsであり、CASレイテンシ9の667MHz(DDR3-1333)は13.5nsである。

例:

(**CAS** / **DATA RATE**) \* 2000 = X ns

(**9** / **1333**) \* 2000 = 13.5034 ns

## 拡張機能

インテルは拡張メモリプロファイル(eXtreme Memory Profile) ([XMP](https://ja.wikipedia.org/wiki/Serial_Presence_Detect#Extreme_Memory_Profile_\(XMP\) "wikilink")) の仕様を[2007年](../Page/2007年.md "wikilink")[3月23日](../Page/3月23日.md "wikilink")に公式に発表した。これはDDR3 SDRAMにおける伝統的なJEDEC [SPD仕様に対して](https://ja.wikipedia.org/wiki/Serial_Presence_Detect "wikilink")、オーバークロック動作のためのプロファイルを追加する規格である。\[7\]

## メモリモジュール

### JEDEC標準モジュール

<table>
<thead>
<tr class="header">
<th><p>チップ規格</p></th>
<th><p>モジュール規格</p></th>
<th><p>メモリクロック<br />
<small>(MHz)</small></p></th>
<th><p>バスクロック<br />
<small>(MHz)</small></p></th>
<th><p>転送速度<br />
<small>(GB/秒)</small></p></th>
<th><p>データ転送速度<br />
（サイクル）<br />
<small>(MHz)</small></p></th>
<th><p>データ転送速度<br />
（転送回数）<br />
<small>(MT/秒)</small></p></th>
<th><p>モジュールのデータ転送速度<br />
（64ビットデータ=8バイト（B）（1バイト＝8ビット））<br />
（MB = <span class="math inline">10<sup>6</sup></span>B、GB = <span class="math inline">10<sup>9</sup></span>B）</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DDR3-800</p></td>
<td><p>PC3-6400</p></td>
<td><p>100</p></td>
<td><p>400</p></td>
<td><p>6.400</p></td>
<td><p>800</p></td>
<td><p>800</p></td>
<td><p>800MHz × 8B = 6,400MB/秒 = 6.4GB/秒</p></td>
</tr>
<tr class="even">
<td><p>DDR3-1066</p></td>
<td><p>PC3-8500</p></td>
<td><p>133</p></td>
<td><p>533</p></td>
<td><p>8.533</p></td>
<td><p>1,066<span class="math inline">$\tfrac{2}{3}$</span></p></td>
<td><p>1,066<span class="math inline">$\tfrac{2}{3}$</span></p></td>
<td><p>1,066<span class="math inline">$\tfrac{2}{3}$</span>MHz × 8B ≒ 8,533MB/秒 = 8.533GB/秒</p></td>
</tr>
<tr class="odd">
<td><p>DDR3-1333</p></td>
<td><p>PC3-10600</p></td>
<td><p>166</p></td>
<td><p>667</p></td>
<td><p>10.667</p></td>
<td><p>1,333<span class="math inline">$\tfrac{1}{3}$</span></p></td>
<td><p>1,333<span class="math inline">$\tfrac{1}{3}$</span></p></td>
<td><p>1,333<span class="math inline">$\tfrac{1}{3}$</span>MHz × 8B ≒ 10,667MB/秒 = 10.667GB/秒</p></td>
</tr>
<tr class="even">
<td><p>DDR3-1600</p></td>
<td><p>PC3-12800</p></td>
<td><p>200</p></td>
<td><p>800</p></td>
<td><p>12.800</p></td>
<td><p>1,600</p></td>
<td><p>1,600</p></td>
<td><p>1,600MHz × 8B = 12,800MB/秒 = 12.8GB/秒</p></td>
</tr>
<tr class="odd">
<td><p>DDR3-1866</p></td>
<td><p>PC3-14900</p></td>
<td><p>233</p></td>
<td><p>933</p></td>
<td><p>14.933</p></td>
<td><p>1,866<span class="math inline">$\tfrac{2}{3}$</span></p></td>
<td><p>1,866<span class="math inline">$\tfrac{2}{3}$</span></p></td>
<td><p>1,866<span class="math inline">$\tfrac{2}{3}$</span>MHz × 8B ≒ 14,933MB/秒 = 14.933GB/秒</p></td>
</tr>
<tr class="even">
<td><p>DDR3-2133</p></td>
<td><p>PC3-17000</p></td>
<td><p>266</p></td>
<td><p>1066</p></td>
<td><p>17.067</p></td>
<td><p>2,133<span class="math inline">$\tfrac{1}{3}$</span></p></td>
<td><p>2,133<span class="math inline">$\tfrac{1}{3}$</span></p></td>
<td><p>2,133<span class="math inline">$\tfrac{1}{3}$</span>MHz × 8B ≒ 17,067MB/秒 = 17.067GB/秒</p></td>
</tr>
<tr class="odd">
<td><p>DDR3-2400</p></td>
<td><p>PC3-19200</p></td>
<td><p>300</p></td>
<td><p>1200</p></td>
<td><p>19.200</p></td>
<td><p>2,400</p></td>
<td><p>2,400</p></td>
<td><p>2,400MHz × 8B = 19,200MB/秒 = 19.2GB/秒</p></td>
</tr>
<tr class="even">
<td><p>DDR3-2666</p></td>
<td><p>PC3-21333</p></td>
<td><p>333</p></td>
<td><p>1333</p></td>
<td><p>21.333</p></td>
<td><p>2,666<span class="math inline">$\tfrac{2}{3}$</span></p></td>
<td><p>2,666<span class="math inline">$\tfrac{2}{3}$</span></p></td>
<td><p>2,666<span class="math inline">$\tfrac{2}{3}$</span>MHz × 8B ≒ 21,333MB/秒 = 21.333GB/秒</p></td>
</tr>
</tbody>
</table>

**注記:** 上のリストのうち、DDR3-2133までは[JEDEC](https://ja.wikipedia.org/wiki/JEDEC "wikilink")のJESD79-3Dによって標準化された\[8\]。これら以外のRAMデータレートはJEDECにより標準化されていない。非標準の高速モジュールは、製造元が耐性の高いメモリチップを選別し、電圧を上げたものである。その中で高速なものでは、DDR3-2800がある\[9\]。

DDR3-xxxの「xxx」はDDRチップ自体のデータ転送レートを表す。それに対してPC3-yyyyの「yyyy」はDIMMモジュールの理論的な帯域幅（しばしば概数として丸められる）を示す。帯域幅は毎秒転送量を8倍して求められる。これは、DDR3メモリモジュールは64データビット幅を持ち、1バイトは8ビットであることから、1回ごとに8バイト転送されるからである。

DDR3にも、DDR2と同様に、帯域幅や容量に加えて、次のようなオプションの規格がある。

1.  [ECCの実装](https://ja.wikipedia.org/wiki/Dynamic_random_access_memory#Errors_and_error_correction "wikilink")。信頼性の向上のため、余分なデータバイトレーンを持つ。小規模なエラーは訂正され、大規模なエラーは検出される。ECC付きモジュールは、型式名に**ECC**もしくは**E**が付く。例えば『PC3-6400 ECC』または『PC3-8500E』である。\[10\]
2.  ["registered"により信号を安定させる](https://ja.wikipedia.org/wiki/Registered_memory "wikilink")。その結果、クロックレートおよびスロットあたりの容量も向上することがある。これは[registerチップに信号をバッファリングすることによる](https://ja.wikipedia.org/wiki/hardware_register "wikilink")。バッファリングされる分、余分なクロックを必要とし、レイテンシが増える。これらのモジュールの型式名は**R**が付く。対してノン・レジスタード（別名[unbuffered](https://ja.wikipedia.org/wiki/Unbuffered_memory "wikilink")) RAMを区別する必要があるときは、**U**を付ける。PC3-6400RはレジスタードなPC3-6400モジュールであり、PC3-6400R ECCはさらにECCが加えられている。
3.  [fully buffered](https://ja.wikipedia.org/wiki/Fully_Buffered_DIMM "wikilink")。これは形式名に**F**もしくは**FB**が加わる。他の種類とは[ノッチ](../Page/ノッチ.md "wikilink")の位置が異なる。これは、完全バッファ化モジュール (Fully buffered modules) はレジスタードモジュール用に作られた[マザーボード](../Page/マザーボード.md "wikilink")では使用できないため、モジュールの挿入を防ぐためである。

## 低電圧版

通常の DDR3 は 1.5V 駆動

  - **DDR3L** - 1.35V駆動
  - **DDR3U** - 1.25V駆動
  - **LPDDR3** - 1.2V駆動

## ピン名称と機能

以下にDDR3 SDRAMで用いられる78ボール[FBGA](https://ja.wikipedia.org/wiki/FBGA "wikilink") (x4/x8) , 96ボールFBGA (x16) パッケージのピンレイアウトの例を示す。RAS\#やCAS\#など\#が記載してあるピンは負論理で動作する。

[thumb](https://ja.wikipedia.org/wiki/ファイル:ddr3_sdram_fbga_package_top_view_jp.png "wikilink")

それぞれのピンの機能について説明する。

  - CK,CK\#
    クロック信号 (Clock)。DDR3 SDRAMが動作する基準であるタイミング決定を行う差動クロックを入力する。CKの上がりエッジとCK\#の下がりエッジの交点を基準にアドレスやコマンドを受け取り、CKとCK\#の交点を基準にデータ出力を行う。
  - CKE
    クロックイネーブル信号 (Clock Enable)。デバイスの入出力信号に対してクロックが有効か無効かを決定する。CKE入力がハイでクロックを有効、ローでクロックを無効になる。プリチャージパワーダウン (Precharge Power Down),セルフリフレッシュ (Self Refresh) またはアクティブパワーダウン (Active Power Down) 時にはCKEをローにする。
  - CS\#
    チップセレクト信号 (Chip Select)。CS\# ローでコマンド入力は有効、CS\#がハイでコマンド入力は無効。ただし動作中のコマンドはCS\#をハイにしても継続する。
  - ODT
    オンダイターミネーション信号 (On Die Termination:ODT)。ODTがハイで内蔵する終端抵抗が有効になる。ODTはDQ, DQS, DQS\#, DMTDQS\# NUDQS\#のみ供給され、それ以外の入力ピン (CKE, CS\#, RAS\#, CAS\#, WE\#, ODT, RESET\#, BA0-BA2 A0-A13) には供給されない。
  - RAS\#,CAS\#,WE\#
    ロウアドレスストローブ信号 (Row Address Strobe:RAS), カラムアドレスストローブ信号 (Column Address Strobe:CAS), およびライトイネーブル信号(Write Enable:WE)。DDR3 SDRAMの動作を決定するコマンドを入力する（後述のコマンド一覧参照）。
  - DM(DMU DML)
    データマスク信号 (Data Mask:DM)。ライト動作時、ハイのときのデータ入力はマスクされデバイスへ書き込まれない。x8デバイスでTDQSを有効にした場合、TDQSとして動作する (DMは無効)。
  - BA0-BA2
    バンクアドレス信号 (Bank Address)。 アクティブコマンド (Active) 時にリード/ライトするバンクを選択する。モードレジスタ (Mode Register) の種類 (MR0～MR3) を選択するためにも利用される。
  - A0-A13
    アドレス信号 (Address)。メモリアレイの読み書きしたいセル位置を特定するアドレスを入力する。 アクティブコマンド入力時にロウアドレス、リード/ライトコマンド入力時にバースト動作の先頭カラムアドレスを選択する。モードレジスタ設定にも用いられる。
  - A10/AP
    オートプリチャージ信号 (Auto Precharge)。リード/ライトコマンド時に指定するカラムアドレスはA0-A9,A11,A13で指定する。そのためリード/ライトコマンド入力時のA10はアドレス入力に使わない。代わりにA10はリード/ライト後にアクセスしているバンクに対して オートプリチャージを行うか(A10をハイ)、行わないか(A10 ロー)を指定するために用いられる。またプリチャージコマンド入力時にA10はプリチャージの対象バンクの選択に用いられる。A10 ローのときプリチャージはバンク一つに対してのみ行い、A10をハイのときプリチャージは全てのバンクに対して行われる。プリチャージの対象バンクはバンクアドレスで選択する。
  - A12/BC\#
    バーストチョップ (Burst Chop:BC) 信号。リード/ライトコマンド入力時バースト動作を4データ分で中断する（バーストチョップする）か (A12 ロー)、行わないか (A12をハイ) を選択する。
  - RESET\#
    リセット信号 (RESET)。リセットピンにローを入力するといつでもデバイスはリセット動作を行う。リセットピンがハイのときは何も行わない。通常動作中はリセットピンは安定してハイを維持する必要がある。リセットピンはCMOSレールトゥレール (Rail to Rail:ハイ/ローの電圧幅いっぱいに振る信号) で電源電圧VDDとグランド電圧VSSに対して80%でハイ、20%でローとなる。例えばVDDが1.5Vの場合は1.2Vでハイ、0.3Vでローとなる。
  - DQ
    データ信号。データの入出力を行う。
  - DQS DQS\#
    データストローブ信号 (Data Strobe)。データのリード/ライト のタイミングを指定する差動ストローブ信号。ライト時、DQSとDQS\#の交点をデータウインドウの中心を打ち抜くタイミングで信号を入力する。リード時、DQS、DQS\#のエッジはデータエッジと揃う。
  - TDQS TDQS\#
    ターミネーションデータストローブ (Termination Data Strobe)。x8 DRAMのみ有効。モードレジスタ (Mode Register) MR1でTDQS機能を有効にした場合、TDQS/TDQS\#はDQS/DQS\#に対する終端抵抗を提供する。TDQS機能が無効の場合、TDQSはデータマスクとして動作する。TDQS\#は使用されない。
  - NC
    未接続 (Non Connection)。
  - VDD
    電源供給。
  - VSS
    グランド。
  - VDDQ
    DQ用の電源供給。
  - VSSQ
    DQ用のグランド。
  - VREFDQ
    DQ用参照電圧(Vref)供給。
  - VREFCA
    コマンド・アドレス用参照電圧 (Vref) 供給。
  - ZQ
    ZQキャリブレーション (ZQ Calibration) 用参照電圧 (Vref) 供給。ZQピンは外部抵抗RZQ (240Ω±1%) を介してGNDに接続する。

## コマンドとオペレーション

## 電流スペックと測定条件

## 機能概略

  - DDR3 SDRAM コンポーネント
      - 非同期RESETピンの導入\[11\]
      - システムレベルフライト時間補正のサポート
      - On-DIMMミラーフレンドリーなDRAMのピンアウト
      - CWL(CASライトレイテンシ) per clock ピンの導入
      - On-die I/O キャリブレーションエンジン
      - READおよびWRITEキャリブレーション
  - DDR3 モジュール
      - Fly-by command/address/control bus with on-DIMM termination
      - 精密なキャリブレーションレジスタ
      - 後方**非**互換性
          - DDR3モジュールはDDR2ソケットにかみ合わない; DIMMモジュールやマザーボードにダメージを与えかねないため\[12\]
  - DDR2に対する長所
      - 広帯域によるパフォーマンスアップ。1600MT/sまで標準化される
      - ナノ秒レベルでレイテンシが改善される
      - 低消費電力でより高いパフォーマンスを発揮する（ノートパソコンではバッテリー稼働時間の向上が見込める）
      - 低消費電力に対する拡張機能
  - DDR2に対する欠点

<!-- end list -->

  -   - 一般的に、広帯域化、高クロック化すると消費電力が増大する。ただしDDR2→DDR3間に関しては高帯域化と同時に駆動電圧が引き下げられているため、全体としてほぼ同水準といえる。

## 市場に対する進出

2007年に開始されたDDR3であるが、インテルのブレインであるCarlos Weissenbergは2008年8月ロールアウト時の講演で、2009年終わりもしくは2010年初期までDDR2の需要に追いつかないだろうと語った\[13\] （同じ見通しは市場調査会社DRAMeXchangeが１年早い2007年4月に発表している\[14\]）。 DDR3の採用の増加は、新しいAMD[Phenom IIおよびインテル](https://ja.wikipedia.org/wiki/Phenom_II "wikilink")[Core i7プロセッサによる](https://ja.wikipedia.org/wiki/Core_i7 "wikilink")。これらはメモリコントローラーを内蔵しており、前者はDDR3を推奨し、後者は必須である。 2009年1月の[IDC](https://ja.wikipedia.org/wiki/IDC "wikilink")ではDDR3の販売が2009年のDRAM市場の29％を占め、2011年には72％になるだろうとしている\[15\]。

## 上位規格

2008年[サンフランシスコ](../Page/サンフランシスコ.md "wikilink")で開催された[Intel Developer Forumで明らかにされた話では](https://ja.wikipedia.org/wiki/Intel_Developer_Forum "wikilink")、DDR3の上位規格はDDR4であろうとのことであった\[16\]。現在設計段階であり、2012年にリリースされ、リリースされたときには1.5Vで動作するDDR3に比べ1.2Vもしくはそれ以下で動作するであろう\[17\]\[18\]。毎秒20億回のデータ転送が行えるだろうとした。

## 脚注

<references/>

## 関連項目

  - [デュアルチャネル](https://ja.wikipedia.org/wiki/デュアルチャネル "wikilink")
  - [トリプルチャネル](https://ja.wikipedia.org/wiki/トリプルチャネル "wikilink")
  - [クアッドチャネル](https://ja.wikipedia.org/wiki/クアッドチャネル "wikilink")
  - [デバイス帯域幅の一覧](../Page/デバイス帯域幅の一覧.md "wikilink")

## 外部リンク

  - [JEDEC](http://www.jedec.org)
  - [ハイニックス半導体 (Hynix Semiconductor)](http://www.hynix.com)
  - [華亜科技 (Inotera memories)](http://www.inotera.com)
  - [南亜科技 (Nanya Technology)](http://www.nanya.com)
  - [エルピーダメモリ株式会社 (Elpida Memory, Inc.)](http://www.elpida.com/ja)
  - [力晶半導体 (Powerchip Semiconductor Corp.)](http://www.psc.com.tw)
  - [キマンダ (Qimonda AG)](http://www.qimonda.com)
  - [サムスン電子 (Samsung Electronics)](http://www.samsung.com)
  - [マイクロン・テクノロジー (Micron Technology)](http://www.micron.com)

[de:DDR-SDRAM\#DDR3-SDRAM](https://ja.wikipedia.org/wiki/de:DDR-SDRAM#DDR3-SDRAM "wikilink") [fi:DRAM\#DDR3 SDRAM](https://ja.wikipedia.org/wiki/fi:DRAM#DDR3_SDRAM "wikilink")

[Category:SDRAM](https://ja.wikipedia.org/wiki/Category:SDRAM "wikilink") [Category:コンピュータバス](https://ja.wikipedia.org/wiki/Category:コンピュータバス "wikilink")

1.
2.
3.
4.
5.  [DDR4 not expected until 2015 - SemiAccurate](http://www.semiaccurate.com/2010/08/16/ddr4-not-expected-until-2015/)
6.
7.
8.  [1](http://www.jedec.org/standards-documents/docs/jesd-79-3d)
9.  [Elpida goes green with development of 50nm process DDR3 SDRAM](http://www.digitimes.com/news/a20081127PR202.html)
10. [2](http://h20000.www2.hp.com/bc/docs/support/SupportManual/c00256987/c00256987.pdf) Hewlett-Packard. Memory technology evolution: an overview of system memory technologies, page 18.
11.
12.
13.
14.
15.
16. [DDR4 PDF page 23](http://intel.wingateweb.com/US08/published/sessions/MASS006/SF08_MASS006_100s.pdf)
17. [Looking forward to DDR4](http://www.pcpro.co.uk/news/220257/idf-ddr3-wont-catch-up-with-ddr2-during-2009.html)
18. [DDR3 successor](http://www.heise-online.co.uk/news/IDF-DDR4-the-successor-to-DDR3-memory--/111367)