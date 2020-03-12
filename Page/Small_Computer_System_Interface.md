> この記事は[Small Computer System Interface](https://ja.wikipedia.org/wiki/Small_Computer_System_Interface)から翻訳されています。


****（スモールコンピュータシステムインタフェース、**小型計算機システムインタフェース**）、略して**** （スカジー）は、主に[周辺機器](../Page/周辺機器.md "wikilink")と[コンピュータ](../Page/コンピュータ.md "wikilink")などの[ハードウェア](../Page/ハードウェア.md "wikilink")間のデータのやりとりを行う[インタフェース規格の一つである](../Page/インタフェース_\(情報技術\).md "wikilink")。SCSIを使用可能にするインタフェース装置をSCSIインタフェースと呼ぶ。[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")（米国規格協会）によって規格化されている。

## 歴史

[パソコンや](../Page/パーソナルコンピュータ.md "wikilink")[ワークステーション](../Page/ワークステーション.md "wikilink")と[周辺機器](../Page/周辺機器.md "wikilink")との接続[インタフェースとして](../Page/インタフェース_\(情報技術\).md "wikilink")、[シュガートのSASI](../Page/シュガートアソシエイツ.md "wikilink") (Shugart Associates System Interface) を拡張し、[ANSIによって規格化された](../Page/米国国家規格協会.md "wikilink")[バス型のインタフェースである](../Page/バス_\(コンピュータ\).md "wikilink")。[8ビット](../Page/8ビット.md "wikilink")または[16ビット](../Page/16ビット.md "wikilink")の[パラレルインタフェース](https://ja.wikipedia.org/wiki/バス_\(コンピュータ\)#パラレルバス "wikilink")。Ultra SCSIでは[シリアル型もある](https://ja.wikipedia.org/wiki/シリアル通信 "wikilink")。後述の大型のコネクタ・バス等は近年その役目を終えたが、SCSI規格自体は物理的な仕様のみならずデバイス間の[通信プロトコル](../Page/通信プロトコル.md "wikilink")も規定している。実際に現在普及している高速規格である[ATA](../Page/Advanced_Technology_Attachment.md "wikilink")、[SATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")、[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")、[IEEE 1394](../Page/IEEE_1394.md "wikilink")、[ファイバチャネル](https://ja.wikipedia.org/wiki/ファイバチャネル "wikilink")上では[SCSIコマンド](https://ja.wikipedia.org/wiki/SCSIコマンド "wikilink")が未だにやり取りされている。

## 概要

### SCSIバスの基本

SCSI[バスは](../Page/バス_\(コンピュータ\).md "wikilink")、周辺機器を接続するインタフェースではあるが、コンピュータと周辺機器という、主従関係ではなく、各機器が対等の動作をすることを基本として設計されている。[入出力](../Page/入出力.md "wikilink")要求を行なう要求を出す機器（イニシエータ）から実際の動作を受ける機器（ターゲット）に対して指示を行ない、その結果を返す、という形で動作する。

一般には、インタフェース1台に複数のSCSI機器を接続するものであると認識されているが、実際には複数台のパソコンで1台のディスクを共有するなどの構成も可能な仕組みになっている。すなわち、イニシエータは1つのバス上に複数の機器が存在してもよい。しかし、実際には、コンピュータがバス上の唯一のイニシエータで、各周辺機器（ディスクやテープ装置など）はターゲットとしてのみ動くのが普通である。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Wikipedia-scsi01.png "wikilink")

図中、SCSIバスから各機器のコントローラや[ホストバスアダプタ](https://ja.wikipedia.org/wiki/ホストバスアダプタ "wikilink")までの接続線をスタブと呼称し、規格上は各々の機器につき15cmまでが許容されている。また、SCSIバス上での機器の間隔は25cm以上が推奨されている。

SCSIはバス形式ではあるが、各機器を数珠つなぎで繋いでいくため、[ヒナギク](../Page/ヒナギク.md "wikilink")の花輪になぞらえ「[デイジーチェーン](https://ja.wikipedia.org/wiki/デイジーチェーン "wikilink")接続」とも言われる。各機器は1つのSCSIバスに接続しなければならない。また、バスの両端には信号の反射を防ぐため、ターミネータを接続しなければならない。なお、[ターミネータは](https://ja.wikipedia.org/wiki/#ターミネータ "wikilink")、必ずしもバス終端に接続されるわけではなく、ホストバスアダプタやSCSI機器に内蔵される場合もある。

SCSIバスに接続する各機器はSCSIデバイスと呼ばれる。各々0から7（または15）までの番号で区別される。この番号のことをSCSI IDという。通常、SCSI機器は各々、明示的にSCSI IDを設定しなければならないが、SCAMという拡張仕様を用いることで、自動的に設定することも可能である。

SCSI IDは、7→0、15→8の順にバス使用優先権が割り振られるため、コントローラのIDは7に、処理が遅くバスを頻繁に開放する機器（[テープドライブ](../Page/テープドライブ.md "wikilink")や[CD-ROM](../Page/CD-ROM.md "wikilink")等）に優先順位の高い番号を割り当てる。

また、各々のSCSIデバイスは、さらにユニットを8つまで持つことができる。これをロジカルユニットという。各ロジカルユニットには番号がつけられる。この番号のことをLUN () という。ロジカルユニットは、1つのデバイスで複数の媒体を持つことができる多連装CD-ROM装置や、ディスクアレイ装置、多連装テープ装置などで使われる。

  - 注）ディスクアレイ装置の場合、LUNではなく、[RAID](../Page/RAID.md "wikilink")コントローラを介して内部に別のSCSIバスを用意しそこに[HDDを接続する実装が殆どである](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")。

もっとも、一般向けの機器でこれを用いているのは[PD](../Page/Phase-change_Dual.md "wikilink")、[DVD-RAM](../Page/DVD-RAM.md "wikilink")、多連装CD-ROMドライブ程度であるため通常の使用においてはまず気にする必要は無い。

### SCSI装置の区分

SCSI装置はいくつかの種類ごとに[カテゴリ](../Page/カテゴリ.md "wikilink")分けされる。たとえば、ディスク装置、テープ装置などであり、それぞれのカテゴリごとに利用できるコマンド類が定義される。これは、ディスクはランダムアクセスできるが、テープは[シーケンシャルアクセス](../Page/シーケンシャルアクセス.md "wikilink")しかできないため、ランダムアクセスのコマンドは定義しようにもできないからである。

### SCSIのバス幅

並列（パラレル）SCSIでは、8ビット幅 (NARROW) では50芯、16ビット幅 (WIDE) では68芯のケーブルを用い、各機器をバス接続する。バスの両端には[終端抵抗](../Page/終端抵抗.md "wikilink")（ターミネータ）が必要である。NARROWでは8台、WIDEでは16台のSCSI機器を接続できる。ただしインタフェースボードがIDを一つ消費するので、実際に接続可能な機器はNARROWで7台、WIDEで15台となる。

なお、SCSI-2の16/[32ビット](../Page/32ビット.md "wikilink")WIDEはNARROWにケーブルをもう1本追加するものであったためまったく普及せず、Ultra SCSIで廃止され、新たに16bit WIDEが規定された。 通常、WIDEといえばUltra SCSIの16bit WIDEを指す。

## 規格

### 規格の基本

[thumb製SCSI](https://ja.wikipedia.org/wiki/ファイル:Scsiboard01.jpg "wikilink")-2インタフェースボード\]\] [thumb製](https://ja.wikipedia.org/wiki/ファイル:Buffalo_IFC-SCD2.jpg "wikilink")[PCカード](../Page/PCカード.md "wikilink")形SCSI-2インタフェース\]\] SCSIは何度か規格を更新し、速度の向上や機能の追加が行われている。

  - SCSI-1
    [1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")にANSIにて制定された最初の規格。HVD（電圧差動型）もこの時点で制定されている。
  - CCS ()
    SCSI-1制定後、色々と開発されたHDD以外の製品などの制御方式を統一するために業界が制定したコマンドセット。ANSIとは無関係である。
  - SCSI-2
    [1989年](../Page/1989年.md "wikilink")にANSIで制定。CCSをベースに、Fast10、16bit/32bit WIDE（要オプションケーブル）、ケーブル、[ターミネータの抵抗値](https://ja.wikipedia.org/wiki/#ターミネータ "wikilink")、コネクタ形状、[パリティ](../Page/パリティ.md "wikilink")の必須化、記憶装置以外の周辺機器（[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")、[スキャナ](../Page/スキャナ.md "wikilink")等）の接続機能等が規格化された。
  - Ultra SCSI
    [1992年](../Page/1992年.md "wikilink")にANSIで制定。WIDEの再定義、シリアルSCSI、Fast20等、包括的に様々な仕様が定義された。これ以降の機能追加 (Ultra2、U160、U320) はUltra SCSIの改訂と言う形で行われている。

SCSI-1や2という規格名より、Narrow SCSI、Fast SCSI、Wide SCSIなどという名称のほうが一般的である。またUltra SCSIの事をSCSI-2の次の規格のためSCSI-3だと良く勘違いされるが、実際にはSCSI-3という規格は存在せずUltra SCSIというのが規格の正式な名称である。

SCSIには、転送速度やバス幅以外にも電圧、伝送方式による違いがあり、現状、**SE**（シングルエンド）、**HVD**（ハイボルテージディファレンシャル）、**LVD**（低電圧差動型：ローボルテージディファレンシャル）の3種類の機器が流通している。SEとLVDに関してはピン互換性があり、また、電気的に相互に接続する事が可能となるよう設計されているが、HVDについては、電気的互換性が考慮されていないため、誤って接続すると機器の故障の原因となるので注意を要する。

<table>
<caption><strong>規格一覧</strong></caption>
<thead>
<tr class="header">
<th><p>規格群</p></th>
<th><p>規格</p></th>
<th><p>省略形</p></th>
<th><p>周波数</p></th>
<th><p>速度<br />
(MB/s)</p></th>
<th><p>バス幅</p></th>
<th><p>最大バス長</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>LVD</p></td>
<td><p>SE</p></td>
<td><p>HVD</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>SCSI-1</p></td>
<td><p>SCSI</p></td>
<td></td>
<td><p>5MHz</p></td>
<td><p>5</p></td>
<td><p>8bit</p></td>
<td></td>
<td><p>6m</p></td>
</tr>
<tr class="odd">
<td><p>SCSI-2</p></td>
<td><p>Fast10</p></td>
<td></td>
<td><p>10MHz</p></td>
<td><p>10</p></td>
<td><p>8bit</p></td>
<td></td>
<td><p>3m</p></td>
</tr>
<tr class="even">
<td><p>SCSI-2</p></td>
<td></td>
<td></td>
<td><p>10MHz</p></td>
<td><p>20</p></td>
<td><p>16bit</p></td>
<td></td>
<td><p>3m</p></td>
</tr>
<tr class="odd">
<td><p>SCSI-2</p></td>
<td></td>
<td></td>
<td><p>10MHz</p></td>
<td><p>40</p></td>
<td><p>32bit</p></td>
<td></td>
<td><p>3m</p></td>
</tr>
<tr class="even">
<td><p>Ultra SCSI</p></td>
<td><p>Ultra/Fast20</p></td>
<td><p>U</p></td>
<td><p>20MHz</p></td>
<td><p>20</p></td>
<td><p>8bit</p></td>
<td></td>
<td><p>1.5m</p></td>
</tr>
<tr class="odd">
<td><p>Ultra SCSI</p></td>
<td><p>Ultra Wide</p></td>
<td><p>UW</p></td>
<td><p>20MHz</p></td>
<td><p>40</p></td>
<td><p>16bit</p></td>
<td></td>
<td><p>1.5m</p></td>
</tr>
<tr class="even">
<td><p>Ultra SCSI</p></td>
<td><p>Ultra2</p></td>
<td><p>U2</p></td>
<td><p>40MHz</p></td>
<td><p>40</p></td>
<td><p>8bit</p></td>
<td><p>12m</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Ultra SCSI</p></td>
<td><p>Wide Ultra2</p></td>
<td><p>U2W</p></td>
<td><p>40MHz</p></td>
<td><p>80</p></td>
<td><p>16bit</p></td>
<td><p>12m</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Ultra SCSI</p></td>
<td><p>Ultra160</p></td>
<td><p>U160</p></td>
<td><p>40MHz DDR</p></td>
<td><p>160</p></td>
<td><p>16bit</p></td>
<td><p>12m</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Ultra SCSI</p></td>
<td><p>Ultra320</p></td>
<td><p>U320</p></td>
<td><p>80MHz DDR</p></td>
<td><p>320</p></td>
<td><p>16bit</p></td>
<td><p>12m</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Ultra SCSI</p></td>
<td><p>Ultra640</p></td>
<td><p>U640</p></td>
<td><p>160MHz DDR</p></td>
<td><p>640</p></td>
<td><p>16bit</p></td>
<td><p>12m</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Ultra SCSI</p></td>
<td><p>Ultra1280</p></td>
<td></td>
<td><p>160MHz PAM-4</p></td>
<td><p>1280</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Ultra SCSI</p></td>
<td><p>Ultra2560、Ultra5120</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Ultra SCSI</p></td>
<td><p>Ultra327680</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

また、パラレルSCSIの開発はU640（製品化はU320まで）で終了し、次世代のSCSIはシリアル ([Serial Attached SCSI](../Page/Serial_Attached_SCSI.md "wikilink"), SAS) で一本化される事になっている。

### コネクタ

[thumb](https://ja.wikipedia.org/wiki/ファイル:SCSI_50pin.jpg "wikilink") 内部接続コネクタはSCSI-1時代には規格化されており、SCSI-2で追加されたWide規格においては、SCSI-1からの8ビット幅の50ピンケーブル（Aコネクタ）と、オプションの68ピンケーブル（Bコネクタ）を併用する必要があった。 Ultra SCSIにてWideの再定義を行い、68ピンケーブル（Pコネクタ）一本で16bitWideが使用可能になった。32bitWideを使用するときはもう一本68ピンケーブル（Qコネクタ）を併用する必要があったが、1つのバスに多くの機器を（しかもケーブル2本使用してまで）接続する必要も現実問題として無く（32bit規格は理論上32台のデバイスをサポートしている）、転送速度のアドバンテージもLVD化により薄れ、LVD規格では32bit規格はドロップされた。

SCSI外部機器がケーブルの接続に使用するコネクタは、SCSI-2/Ultra SCSIで規格化され、NarrowはD-Sub 50pin ハーフピッチコネクタ、Ultra SCSIの16ビットWideは内部接続と同じ D-Sub 68pin ハーフピッチコネクタに固定用の螺子を追加した物が使用される。ただ、ピン形状やコネクタ形状、螺子穴の位置は規格化されているが、それを覆うコネクタカバー部の厚さと螺子の切り方（インチ螺子なのかJIS螺子なのか）には規定が無く、機器と干渉する場合もある。

また、RAIDカードや複数チャネルを持つコントローラは狭いスロットカバーに複数のWideケーブルを接続出来るようにする為、超高密度68pinコネクタを採用している。

SCSI-1時代には、内部接続コネクタ形状のみ規格化されていたため、一般的には[セントロニクスコネクタと同様なベローズ形状のフルピッチの](../Page/IEEE_1284.md "wikilink")50ピンコネクタが使用されていたが、[アップルの](../Page/アップル_\(企業\).md "wikilink")[Macintosh](../Page/Macintosh.md "wikilink")やIO-MEGAのZipドライブでは[RS-232](../Page/RS-232.md "wikilink")Cと同じD-SUB 25pinが、また、[日本電気](../Page/日本電気.md "wikilink") (NEC) の[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")では、ベローズ形状をシュリンクしたSCSI-2のそれと同サイズのコネクタを採用している。NECの[EWS4800](../Page/EWS4800.md "wikilink")シリーズはこれに加え、ケーブル側コネクタの外周部に2つの突起があり、機器側のマイクロスイッチでケーブルが接続されているか否かを判断する仕組みが追加されている。このため、一般のSCSI機器にEWS4800用のSCSI機器は接続出来ない（逆は可能）。

### ターミネータ

[thumb](https://ja.wikipedia.org/wiki/ファイル:SCSI_Terminator_50pin.jpg "wikilink") **ターミネータ**（, [終端抵抗](../Page/終端抵抗.md "wikilink")）には外部に接続するもの、SCSI機器内部のコントローラ基板上にあるものの二種類がある。また、動作方式としてパッシブターミネータとアクティブターミネータがある。

パッシブターミネータは単に抵抗をバスラインに接続するだけである。一方アクティブターミネータは、抵抗だけでなく、[能動素子](https://ja.wikipedia.org/wiki/能動素子 "wikilink")を使っている。SCSI-2以降はアクティブターミネータの使用が必須であり、その回路はSCSIの規格書に記載されている。

## SCSI機器の動向

日本でも各種パソコンや[ワークステーション](../Page/ワークステーション.md "wikilink")（[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")、[FMRシリーズ](../Page/FMRシリーズ.md "wikilink")/[FM TOWNS](../Page/FM_TOWNS.md "wikilink")、[X68000](https://ja.wikipedia.org/wiki/X68000 "wikilink")や、また、日本国内で販売された[Macintosh](../Page/Macintosh.md "wikilink")、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")など）で[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink") (HDD) や[イメージスキャナ](../Page/イメージスキャナ.md "wikilink")、[CD-ROM](../Page/CD-ROM.md "wikilink")、[MOなどを接続する高速インタフェースとして使われてきた](https://ja.wikipedia.org/wiki/MO_\(記憶媒体\) "wikilink")。PC-9800シリーズやMacintoshではSCSIが記憶装置や入出力装置の標準インタフェースとなっており、PC-9800シリーズではSCSI接続したMOディスクからも起動が可能であった。また、MacintoshではSCSI接続した本体を外付けハードディスクとして利用する、**ターゲットディスクモード**と呼ばれる仕様（接続先から起動も可能な仕様になっていた）も用意されている。FM TOWNSも登場時はSCSIを標準搭載としていた。これらの機種のように[フロッピーディスクドライブ](https://ja.wikipedia.org/wiki/フロッピーディスクドライブ "wikilink")とHDDのいずれからも[システムの起動に失敗した場合に](../Page/ブート.md "wikilink")、SCSI接続機器から「第三の選択肢」としてシステム起動を試みることができる仕様となっていたものもあり、当時潤沢ではなかったシステム資源を有効活用する面でも重要な選択肢として活躍した。

その一方で[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")では、内蔵HDDは歴史的に[ST-506](../Page/ST-506.md "wikilink")を始祖とする[IDEが主流であり](https://ja.wikipedia.org/wiki/Advanced_Technology_Attachment#IDE "wikilink")、主に外付けCD-ROMやMO等の接続の為に使用されていただけだった。CD-ROMについてはコスト削減のため、内蔵化され、[SoundBlaster](https://ja.wikipedia.org/wiki/SoundBlaster "wikilink")の[MKEや](https://ja.wikipedia.org/wiki/松下寿電子工業 "wikilink")[ミツミ](../Page/ミツミ電機.md "wikilink")、[ソニー](../Page/ソニー.md "wikilink")の独自接続規格を経て[1996年](../Page/1996年.md "wikilink")頃からは[ATAPIによる接続が主流となった](../Page/Advanced_Technology_Attachment.md "wikilink")。また2002年以降は順次シリアル伝送による規格への置換が進んでおり、パーソナルコンピューター向けでは[シリアルATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")、サーバー向けでは[Serial Attached SCSI](../Page/Serial_Attached_SCSI.md "wikilink") (SAS) への置換が進んでいる。

MOやイメージスキャナなど、外付けの周辺機器についても、[2000年](../Page/2000年.md "wikilink")頃から[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink") 1.1（さらに[2002年](../Page/2002年.md "wikilink")頃からは、より転送速度が速いUSB 2.0）や[IEEE 1394に取って代わられた状況である](../Page/IEEE_1394.md "wikilink")。

Macintosh（特に[iMac](https://ja.wikipedia.org/wiki/iMac "wikilink")以降）でも同様に、HDDやCD-ROMといった内蔵機器はIDE、MOやイメージスキャナなどの外付け機器はUSBやIEEE 1394に置き換わっている。ターゲットディスクモードも、IEEE 1394でサポートされている。

高速な処理速度が強く求められる[サーバ](../Page/サーバ.md "wikilink")用途では、[CPU](../Page/CPU.md "wikilink")への負荷を抑えられることから、現在でもSCSI接続のハードディスクが主に用いられている。この場合、故障に対する耐性を高める目的で、[冗長性を持たせるため](../Page/冗長化.md "wikilink")[RAID](../Page/RAID.md "wikilink")構成（RAID1、あるいはRAID5）として用いられることが多い。

また一般用途でも、日常的にアクセスする外付けHDDを増設する場合、USBやIEEE1394はバスパワー供給の干渉で論理的に切断される現象がまれに発生するため、これを嫌ってSCSIを採用するユーザも少なからずいる。この場合、現在はSCSI用のHDDが非常に高価なため、[ATA](../Page/Advanced_Technology_Attachment.md "wikilink")、[シリアルATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")のHDDをSCSIに接続する為の変換基板（**ATA-SCSIブリッジ**、**S・ATA-SCSIブリッジ**）が使用されることが多い。

複数のイニシエータを持つことが出来る事から、コンピュータクラスタのストレージ用バスとして使われている。ストレージを共有することで個々のストレージへのアクセスをモニタするオーバーヘッドを削減し、異常事態が生じて[フェイルオーバー](https://ja.wikipedia.org/wiki/フェイルオーバー "wikilink")する時は最終状態が保存されているストレージにアクセスできるため瞬時にクラスタ構成要素を切り離したり代替する事ができた。これはIEEE 1394にも引き継がれている。

一般向けでもSCSIのハードディスクが多用されていた時代には 、ドライブユニットはIDEと同じで、制御基板のみ差し替えていた製品が多くを占めていたが、近年のSCSIハードディスクは（SCSI規格そのものによる優位性ではないが）サーバでの使用を前提とした専用設計となり、小口径プラッタ採用によるシーク速度性能の向上や、信頼性確保の為、IDEハードディスクとは文字通り桁違いの[平均故障時間を実現している](https://ja.wikipedia.org/wiki/Mean_Time_To_Failure "wikilink")。

近年ではSCSIという規格名称を冠した製品を見かける機会は以前と比べて減少しているが、SCSIのデータ伝送プロトコルを応用した規格として、前述の SAS (Serial Attached SCSI)、UASP ([USB Attached SCSI Protocol](https://ja.wikipedia.org/wiki/USB_Attached_SCSI_Protocol "wikilink"))の対応製品が、また[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")技術の進展にともない、SCSI機器をIPネットワーク経由で接続するための [iSCSI](https://ja.wikipedia.org/wiki/iSCSI "wikilink")という規格が[IETFにおいて標準化されている](../Page/Internet_Engineering_Task_Force.md "wikilink")。従来の[ストレージエリアネットワーク](../Page/ストレージエリアネットワーク.md "wikilink") (SAN) ではファイバチャネルが使われることが多かったが、コストが高くなりがちである、[ファイバチャネル](https://ja.wikipedia.org/wiki/ファイバチャネル "wikilink")に精通した技術者が少ない、などの問題点があった。これに対し、IPネットワーク機器は広く普及しており、IP ネットワーク技術に関連した技術者も多いことから、iSCSIをベースとしたSANも普及をみせている。

## 補足

  - 「SCSIインタフェース」というインタフェースが[二重になったような言い方をされることがある](../Page/RAS症候群.md "wikilink")。これは「SCSIという規格に合致したインタフェース機器」という意味で解釈すれば、必ずしも間違いではないが、混乱を避けるには「SCSIカード」「SCSI端子（ポート）」などと言う。
  - SCSIのインタフェースカードは[Host Bus Adapter](https://ja.wikipedia.org/wiki/ホストバスアダプタ "wikilink") (HBA) と呼ばれる。これはストレージシステムにおいて、ディスク側にもアダプターが実装されることもあり、ホスト (PC) 側のアダプターであることを明示する必要があるからである。
  - SCSIは、[ホットスワップ](../Page/ホットスワップ.md "wikilink")（電源投入後の脱着）に対応しておらず、起動後に機器を繋いでも認識されない。認識させる為にはコンピュータの再起動が必要であり、外部周辺機器でホットスワップにも対応している、USBやIEEE 1394に取って代わられたひとつの要因と言える。
  - SCSIの規格としては、接続さえしておけばホストアダプタ側の電源投入後も機器側のコネクト／ディスコネクトが可能となっている。ただし[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) 又は[ドライバが対応している必要がある](../Page/デバイスドライバ.md "wikilink")。たとえば[Windows 95以降であればOS起動後にHDDの電源を入れても](../Page/Microsoft_Windows_95.md "wikilink")、デバイスマネージャからデバイスの更新操作を行えば再スキャンが行われ再設定される。
  - [2006年](../Page/2006年.md "wikilink")現在、日本国内で販売されている一般向けのSCSI機器は、HDDのベアドライブを除けば、IDE→SCSI変換基板を介したものがほとんどである。ある意味、初期の[ST-506](../Page/ST-506.md "wikilink")+変換基板の時代に回帰したとも言える。
  - NECの超並列コンピュータ Cenju の外部SCSIコネクタは一部配線が間違えて接続されているため、最初の機器を接続する場合、専用のケーブルを購入しなければならない。
  - PC-9800シリーズの初期の純正SCSIボード (PC-9801-55) において、NEC製以外のHDDを接続すると認識しないという処置がされており、たちの悪いプロテクトであると一般に思われている。しかしこれは、当時SCSIの代替セクタの解釈にゆれがあり、他社製HDDをつなぐとトラブルが起きる可能性があるため、やむなくとられた措置である。とはいえ、このために純正ボードがリファレンスとして機能せず、[サードパーティー](../Page/サードパーティー.md "wikilink")のHDDは自社のSCSIボードとのセット販売が主流となり、互換性をめぐる混乱（HDDを他社のボードにつなぎかえるとジオメトリの違いにより[パーティション](../Page/パーティション.md "wikilink")が認識されない）を引き起こす遠因となったことは否定できない。[55ボード問題を参照](https://ja.wikipedia.org/wiki/PC-9800シリーズ#55ボード問題 "wikilink")。
  - PC-9800シリーズにおける純正インタフェースボードが、SASIのものとSCSIのもので別々のコントローラを使用していて非互換であるため、日本においてはSASIとSCSIは別物であると考えられている事が多い（これは、同様にPC-9800シリーズ、FMRシリーズとその上位互換であるFM TOWNSで、当初IDEに専用のI/Oが定義されず、ソフトウェア上はSASIの上位互換として処理する事で導入された経緯もある）。しかし実際には、元々SASIを大幅に拡張した上で規格化したものがSCSIであり、SCSIはSASIの上位互換規格となっている。このため、プロトコルシーケンスを全てソフトウェアで実現する原始的なSASIコントローラの場合、ソフトウェア次第ではSCSIデバイスを接続することも不可能では無い。実際、PC-9800シリーズ用SASIボードにSCSIのHDDを接続するためのドライバソフトは存在する。また、X68000でも、SCSIインタフェース搭載以前の機種で、本来はSASIのインタフェースに対し、SCSIプロトコルをソフトウェア的に実装し、接続を実現したSxSIというドライバが存在する。またSCSI普及初期には、一部サードパーティー製SCSIボードにSASIのHDDが使用可能なものがあったり、SCSI/SASIを切り替えて使えるHDDなども存在した。

## 関連項目

  - [SCSIコマンド](https://ja.wikipedia.org/wiki/SCSIコマンド "wikilink")
  - [iSCSI](https://ja.wikipedia.org/wiki/iSCSI "wikilink")
  - [ATA](../Page/Advanced_Technology_Attachment.md "wikilink")
      - [IDE](https://ja.wikipedia.org/wiki/Advanced_Technology_Attachment#IDE "wikilink")
      - [ATAPI](https://ja.wikipedia.org/wiki/Advanced_Technology_Attachment#ATAPI "wikilink")
  - [シリアルATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")
  - [SASI](https://ja.wikipedia.org/wiki/SASI "wikilink")
  - [ST-506](../Page/ST-506.md "wikilink")
  - [ESDI](https://ja.wikipedia.org/wiki/Enhanced_Small_Disk_Interface "wikilink")
  - [RAID](../Page/RAID.md "wikilink")
  - [Serial Attached SCSI](../Page/Serial_Attached_SCSI.md "wikilink")
  - [ファイバチャネル](https://ja.wikipedia.org/wiki/ファイバチャネル "wikilink")
  - [FireWire](../Page/IEEE_1394.md "wikilink")
  - [転送速度](https://ja.wikipedia.org/wiki/転送速度 "wikilink")

## 外部リンク

  - [困った時：SCSIケーブル・変換アダプタのいろいろ（写真付）](http://www.sanwa.co.jp/product/cable/scsi/index.html)
  - [T10 Technical Committee](http://www.t10.org/)
  - [SCSI Trade Association](http://www.scsita.org/)
  - [幻となった次世代のパラレルSCSI規格 Ultra640編](http://pc.watch.impress.co.jp/docs/2003/0630/it005.htm)

[Category:インタフェース規格](https://ja.wikipedia.org/wiki/Category:インタフェース規格 "wikilink")