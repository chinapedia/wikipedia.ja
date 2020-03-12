> この記事は[Advanced Technology Attachment](https://ja.wikipedia.org/wiki/Advanced_Technology_Attachment)から翻訳されています。


**Advanced Technology Attachment**（アドバンスド テクノロジー アタッチメント、略号: **ATA**）は、[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink") (PC) と[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink") (HDD) 間の[インタフェースのひとつである](../Page/インタフェース_\(情報技術\).md "wikilink")。[1989年](../Page/1989年.md "wikilink")に制定され、[1990年代](../Page/1990年代.md "wikilink")に主流となっていた。

## 歴史

本節での容量の単位は、一般的な1024をキロ (KBytes) としているので、1000をキロ (KB) とするHDDメーカー（すなわちHDD単体に貼られたラベルの表記）と異なることに注意されたし。

### IDE

[PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")のハードディスクインタフェースは、当初[ST-506](../Page/ST-506.md "wikilink")、次いでST-506を高速化した[ESDIや](https://ja.wikipedia.org/wiki/Enhanced_Small_Disk_Interface "wikilink")[SCSI等が使用されていたが](../Page/Small_Computer_System_Interface.md "wikilink")、次第にST-506をインテリジェント化（ドライブとコントローラを統合）した[1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")に[コンパック](../Page/コンパック.md "wikilink")と[コナー・ペリフェラル](https://ja.wikipedia.org/wiki/コナー・ペリフェラル "wikilink")が開発した**IDE** (Integrated Drive Electronics) が大勢を占めるようになった。

その後、各社独自の拡張が行われ、互換性に問題が出てきたため、[1989年](../Page/1989年.md "wikilink")に各HDDメーカが共通仕様である**ATA** (AT Attachment interface) を制定し、[1994年](../Page/1994年.md "wikilink")に[ANSIでATA](../Page/米国国家規格協会.md "wikilink")-1として規格化された。

|            | HDD側     | BIOS側      | 小さい方      |
| ---------- | -------- | ---------- | --------- |
| シリンダ番号 (C) | 0～65535  | 0～**1023** | 0～1023    |
| ヘッド番号 (H)  | 0～**15** | 0～254      | 0～15      |
| セクタ番号 (S)  | 1～255    | 1～**63**   | 1～63      |
| 最大容量       | 128GB    | 7.8GB      | **504MB** |

IDE HDDのパラメータの制約

IDE HDDには、504Mバイト（512×1024×16×63 = 528,482,304バイト）を超える容量が認識されないという問題があった。これは「**504MBの壁**」といわれ、1993年頃までに発売されたPCではこの問題がある。HDD側のパラメータとPC/ATの[BIOS](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink") (INT 13H API) のパラメータのミスマッチに起因する。ただし、504MBの壁は、あくまでIDE HDDとPCのBIOSの組み合わせにより生じる問題であり、HDD側ではもっと大きな容量（理論上の最大値は128GB）のアドレッシングが可能である。すなわち、一般には「504MBを境にEIDE HDDとIDE HDDが分かれる」と思われている場合があるが、実はHDD側にはそのような区別はない。

### EIDE

**EIDE** (Enhanced IDE) とは、一般にIDE HDDの504MBの壁を超えるための規格として認識されているが、実際は以下のようなさまざまな拡張規格の総称である。[ウェスタン・デジタル](https://ja.wikipedia.org/wiki/ウェスタン・デジタル "wikilink")が提唱した。

  - 504MBの壁を超えるための拡張
      - [Logical Block Addressing](https://ja.wikipedia.org/wiki/Logical_Block_Addressing "wikilink") (LBA) の導入
      - CHSトランスレーション（いわゆるLARGEモード）の導入
  - ATAPIによる[CD-ROM](../Page/CD-ROM.md "wikilink")やリムーバブルディスクのサポート
  - 転送モードの追加による高速化
  - プライマリ/セカンダリポートの標準化による最大4台のデバイスのサポート

504MBの壁は、BIOSのCHS (Cylinder, Head, Sector) をIDEのCHSに直結させていることが原因なので、途中でうまく変換してやることにより回避できる。その手段として、LBAとCHSトランスレーションが導入された。

  - LBAは、BIOSからHDDに対するアドレッシングをCHSでなく単一の連番で行う（HDDが対応している必要がある）。
  - CHSトランスレーションは、BIOS内部でCHSの変換（たとえばHを2で割るかわりにCを2倍するなど）を行い、CHSの範囲を有効活用する（HDD側で対応することはない）。

なお、LBAはHDD側でCHSレジスタを読み替えることで実現されており、アドレッシング可能な範囲はほとんど変わっていない（28ビット）。すなわち、HDD側ではLBAに対応することでとくに容量上限を増やせるわけではない（厳密には、セクタ番号レジスタに0を指定できるようになるため、若干増える）。

### ATAPI

ATA Packet Interfaceの略で、日本語では「**アタピー**」と発声することが多い。 HDDなどの非ATAPIのATAデバイスでの通信のデータに相当する部分にSCSIと同等のパケット形式のコマンドを発行することにより、ATAコマンドより多くのコマンド種が必要なCD-ROMのようなHDD以外のデバイスの接続を可能とした規格。一般には、CD-ROM等をサポートしたIDEとして認識されている。当初SFF-8020という規格だったが、ATA/ATAPI-4でATA規格に統合された。

### 48bit LBA(BigDrive)

従来の28ビットLBAを[48ビット](https://ja.wikipedia.org/wiki/48ビット "wikilink")に拡張し、128[ペビバイト](https://ja.wikipedia.org/wiki/ペビバイト "wikilink")（140,737,488,355,328[KiB](https://ja.wikipedia.org/wiki/キビバイト "wikilink")）までの容量を扱えるようにした規格。ATA/ATAPI-6で採用された。BigDriveはMaxtor社（当時）が発表したATAの拡張規格につけた名前で、ATA規格では48bitLBAと呼ばれる。

HDDをリセットした直後は従来モード (28ビットLBA) で動作し、ホストよりコマンドで48bitLBAモードに切り替える。切り替えた後はアドレスレジスタの意味が変わり2度書き込むことで1つのアドレスと解釈されるようになる。

この規格に対応したHDDを未対応（28ビットLBA）の機器およびOSに接続すると、切り替えが発生しないため128[GiBのドライブとして動作する](https://ja.wikipedia.org/wiki/ギビバイト "wikilink")（**127GiBの壁**、おおよそ2002年以前に発売されたPCでこの壁がある）。

規格上、従来の28bitLBAのパラレルATAコントローラでも48BitLBAは使えるように考慮されているため、動作する[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")並びに[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")が対応していれば、全領域利用可能である。ただし、ブートデバイスとして利用する場合にはBIOS側が対応する必要があり、非対応の場合はブートストラップローダに加工するか、起動に必要なシステム/データがBIOSが管理できる領域に入っている必要がある。

### 規格のあゆみ

ATA/ATAPIの規格概要を以下に示す。

  - ATA-1（[1994年](../Page/1994年.md "wikilink")、[ANSI 旧規格 X3.221-1994](http://www.t13.org/Documents/UploadedDocuments/project/d0791r4c-ATA-1.pdf)）
    IDEの規格化
  - ATA-2（[1996年](../Page/1996年.md "wikilink")、[ANSI 旧規格 X3.279-1996](http://www.t13.org/Documents/UploadedDocuments/project/d0948r4c-ATA-2.pdf)）
    PIO 3,4 Multiword DMA 1,2追加による高速化
  - ATA-3（[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")、[ANSI 旧規格 X3.298-1997](http://www.t13.org/Documents/UploadedDocuments/project/d2008r7b-ATA-3.pdf)）
    Singleword DMAの削除、リムーバブルメディアのサポート、[S.M.A.R.T.対応](../Page/Self-Monitoring,_Analysis_and_Reporting_Technology.md "wikilink")。2.5インチHDD向け44ピンコネクタ規格制定
  - ATA/ATAPI-4（[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")、[ANSI INCITS 317-1998](http://www.t13.org/Documents/UploadedDocuments/project/d1153r18-ATA-ATAPI-4.pdf)）
    ATAPIの統合。スキャナ、プリンタ、メディアチェンジャー等SCSI準拠の多種デバイスのサポート。UltraDMA 0, 1, 2のサポート。[コンパクトフラッシュ](../Page/コンパクトフラッシュ.md "wikilink")向けコマンドのサポート
  - ATA/ATAPI-5（[2000年](../Page/2000年.md "wikilink")、[ANSI INCITS 340-2000](http://www.t13.org/Documents/UploadedDocuments/project/d1321r3-ATA-ATAPI-5.pdf)）
    UltraDMA 3, 4のサポート。80ピンケーブルの規格制定
  - ATA/ATAPI-6（[2002年](../Page/2002年.md "wikilink")、[ANSI INCITS 361-2002](http://www.t13.org/Documents/UploadedDocuments/project/d1410r3b-ATA-ATAPI-6.pdf)）
    UltraDMA 5、48bit LBA (Big Drive)のサポート
  - ATA/ATAPI-7（[2005年](../Page/2005年.md "wikilink")、ANSI INCITS 397-2005 [Vol 1](http://www.t13.org/Documents/UploadedDocuments/docs2007/D1532v1r4b-AT_Attachment_with_Packet_Interface_-_7_Volume_1.pdf) [Vol 2](http://www.t13.org/Documents/UploadedDocuments/docs2007/D1532v2r4b-AT_Attachment_with_Packet_Interface_-_7_Volume_2.pdf) [Vol 3](http://www.t13.org/Documents/UploadedDocuments/docs2007/D1532v3r4b-AT_Attachment_with_Packet_Interface_-_7_Volume_3.pdf)）
    UltraDMA 6のサポート。1.8、2.5インチHDDの3.3V規格定義。ストリーミング向けコマンドのサポート。シリアルATA1.0の仕様が追加。
  - ATA/ATAPI-8 コマンドセット（[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")、[ANSI INCITS 452-2008](http://www.t13.org/Documents/UploadedDocuments/docs2008/D1699r6a-ATA8-ACS.pdf)）
    ベリファイ付きWriteコマンド、疑似エラー発生コマンドのサポート。[ハイブリッドHDD](../Page/ハイブリッドHDD.md "wikilink")（[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")などの不揮発性キャッシュを搭載）向けコマンドのサポート
  - ATA-8
    伝送規格は審議中

## パラレルATA

### パラレルATAとは

[シリアルATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")が登場して以降、旧来の[パラレル通信](https://ja.wikipedia.org/wiki/パラレル通信 "wikilink")を行うATA規格を区別する[レトロニム](../Page/レトロニム.md "wikilink")であり、**正規の規格名称ではない**。しかし本節および本節の下層節では可読性向上の便宜を図るため、シリアルATA登場以前の規格を含めて「パラレルATA」と表記する。シリアルATA登場以前の規格は単にATAと称されていたが、それらをここではパラレルATAと記述していることに留意が必要。 [200px上にあるパラレルATAの接続端子](https://ja.wikipedia.org/wiki/ファイル:ATA_on_mainboard.jpg "wikilink")（最も下側）\]\] パラレルATAでは、ケーブル1本あたり、最大2台の機器が接続可能（[マスタースレーブ](https://ja.wikipedia.org/wiki/マスタースレーブ "wikilink")接続）である。リセット時などにマスター側の機器がスレーブ側の機器を制御するタイミングがあるが、基本的にはホストから独立して制御できる。

### ケーブル

[thumb](https://ja.wikipedia.org/wiki/ファイル:ATA_cables.jpg "wikilink") パラレルATAは規格制定当初40芯、Ultra DMA 66 (UDMA4) 以降は80芯40pinコネクターのフラットケーブル（またはリボンケーブル）を用いて接続し、ケーブル長は最大18インチ (45.7cm) と規定されている。80芯フラットケーブルを用いたものであってもコネクタのコンタクト（電気接点）の数は従前同様40である（[上位互換](https://ja.wikipedia.org/wiki/上位互換 "wikilink")）。

#### 80芯ケーブル

80芯ケーブルは、信号線とグラウンド線を交互に配置し、40芯ケーブルの伝送特性を改良したものである。使われるコネクタには、GND信号が偶数ピンまたは奇数ピンに割り当てられる二つの仕様があり、それぞれコネクタに刻印されている ODD GND または EVEN GND の文字列で区別することが出来る。多くの市販ケーブルや、製品としてPCに組み込まれているコネクタはODD GNDの物である。柔軟な配線取り回しや筐体内の気流改善を目的として使われるスマートケーブルは、シールド付き40芯（丸）ケーブルを使うため、「Ultra DMA 66 対応」を謳うものであっても80芯フラットケーブルの特性を保持できないことがあり障害の原因になることがある。80芯ケーブルではケーブル部はすべてフラットケーブルであり、40芯ケーブルの一部に見られたリボンケーブルを用いたものはリボンケーブル用80芯コネクタが製造されなかったことからケーブルアセンブリとしても製造されていない。

コネクタには色分けがあり、デバイス側から見た場合、全40Pinのコンタクトにおいて下記の違いがある。なお、20Pinは逆差し防止の為のピンであり、埋められていたり、接点が無いこともある。

  - 黒（マスター）:全ピンある。
  - 青（ホスト）:40芯ケーブルとの識別の為、34PinがケーブルではなくGNDに接続される。
  - 灰（スレーブ）:ケーブルセレクトの為、28Pinが存在しない。デバイス側ケーブル端から見て2番目に配される。製品に組み込み済みのものなどでは、全ピン結線の黒コネクタや青コネクタを用い、適宜ピンを抜いてケーブルセレクトを実装している製品もある。

#### ケーブルセレクト

80芯ケーブルには、ケーブルへの接続位置でマスタースレーブを設定するケーブルセレクトという機能が実装されている（40芯ケーブルではオプション扱いであった）。

  - 40芯ケーブルのケーブルセレクト

ケーブルセレクト対応の40芯ケーブルは実装手法が2種類あり、80芯ケーブル同様にスレーブデバイス用のコネクタから28Pinコンタクトを除去する方法と、フラットケーブルの途中でライン28を切断（切り欠く）手法があった。28Pinコンタクトを除去する方法は80芯ケーブル登場以降そのコネクタを流用したものであり、40芯ケーブルが主流であった頃の実装はケーブルのライン28を切断加工する方法がほとんどであった。このため残存する40芯ケーブルがケーブルセレクト対応であるか否かを判別する方法にケーブル外観から切断（欠損）部分を見つける方法が紹介される場合があるが、確実な判別方法ではない。また、後者のケーブルセレクト対応40芯ケーブルの場合、80芯ケーブルと異なりデバイス側ケーブル端がスレーブとなるので機器接続の際には注意が必要である。

### 転送モード

パラレルATAはその長い歴史を反映して数々の転送モードが存在する。

#### PIO転送モード

<table>
<caption>PIO モード一覧</caption>
<thead>
<tr class="header">
<th><p>モード</p></th>
<th><p>最大転送速度<br />
(MB/s)</p></th>
<th><p>制定された<br />
規格</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Mode 0</p></td>
<td><p>3.3</p></td>
<td><p>ATA</p></td>
</tr>
<tr class="even">
<td><p>Mode 1</p></td>
<td><p>5.2</p></td>
<td><p>ATA</p></td>
</tr>
<tr class="odd">
<td><p>Mode 2</p></td>
<td><p>8.3</p></td>
<td><p>ATA</p></td>
</tr>
<tr class="even">
<td><p>Mode 3</p></td>
<td><p>11.1</p></td>
<td><p>ATA-2</p></td>
</tr>
<tr class="odd">
<td><p>Mode 4</p></td>
<td><p>16.7</p></td>
<td><p>ATA-2</p></td>
</tr>
</tbody>
</table>

PIO (Programmed Input / Output) 転送モードは、CPUが直接IDEコントローラI/Oポートを経由してデータの送受信を行う。

5種類のモードが存在するが、基準となるクロック周波数が異なるだけである。 全てのATA機器は機器転送速度、転送モードのネゴシエートの為、PIO Mode 0をサポートする。

今日でも、速度を必要としない機器はこのモードのみをサポートする。

#### Singleword DMA転送モード

<table>
<caption>Singleword DMAモード一覧</caption>
<thead>
<tr class="header">
<th><p>モード</p></th>
<th><p>最大転送速度<br />
(MB/s)</p></th>
<th><p>制定された<br />
規格</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Mode 0</p></td>
<td><p>2.1</p></td>
<td><p>ATA</p></td>
</tr>
<tr class="even">
<td><p>Mode 1</p></td>
<td><p>4.2</p></td>
<td><p>ATA</p></td>
</tr>
<tr class="odd">
<td><p>Mode 2</p></td>
<td><p>8.3</p></td>
<td><p>ATA</p></td>
</tr>
</tbody>
</table>

Singleword DMAモードは、[IBM PC本体に搭載されていた](../Page/IBM_PC.md "wikilink")[8ビット](../Page/8ビット.md "wikilink")の[DMA転送が可能なDMAコントローラを用いて転送を行うことを想定したモードである](../Page/Direct_Memory_Access.md "wikilink")。これはATA/ATAPI-3規格において廃止されている。

#### Multiword DMA転送モード

<table>
<caption>Multiword DMAモード一覧</caption>
<thead>
<tr class="header">
<th><p>モード</p></th>
<th><p>最大転送速度<br />
(MB/s)</p></th>
<th><p>制定された<br />
規格</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Mode 0</p></td>
<td><p>4.16</p></td>
<td><p>ATA</p></td>
</tr>
<tr class="even">
<td><p>Mode 1</p></td>
<td><p>13.3</p></td>
<td><p>ATA-2</p></td>
</tr>
<tr class="odd">
<td><p>Mode 2</p></td>
<td><p>16.6</p></td>
<td><p>ATA-2</p></td>
</tr>
</tbody>
</table>

Multiword DMAモードは、PC/ATで拡張された[16ビット](../Page/16ビット.md "wikilink")のDMA転送が可能なDMAコントローラを用いて転送を行うことを想定したモードである。ハードディスクではUltra DMA規格化後はあまり使用されていないが、[光ディスク](../Page/光ディスク.md "wikilink")ドライブでは前述した[ATAPIの転送モードとして用いられることが多い](https://ja.wikipedia.org/wiki/#ATAPI "wikilink")。

#### Ultra DMA転送モード

<table>
<caption>UDMA モード一覧</caption>
<thead>
<tr class="header">
<th><p>モード</p></th>
<th><p>最大転送速度<br />
(MB/s)</p></th>
<th><p>制定された<br />
規格</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>UDMA 0</p></td>
<td><p>16.7</p></td>
<td><p>ATA-4</p></td>
</tr>
<tr class="even">
<td><p>UDMA 1</p></td>
<td><p>25.0</p></td>
<td><p>ATA-4</p></td>
</tr>
<tr class="odd">
<td><p>UDMA 2</p></td>
<td><p>33.3</p></td>
<td><p>ATA-4</p></td>
</tr>
<tr class="even">
<td><p>UDMA 3</p></td>
<td><p>44.4</p></td>
<td><p>ATA-5</p></td>
</tr>
<tr class="odd">
<td><p>UDMA 4</p></td>
<td><p>66.6</p></td>
<td><p>ATA-5</p></td>
</tr>
<tr class="even">
<td><p>UDMA 5</p></td>
<td><p>100.0</p></td>
<td><p>ATA-6</p></td>
</tr>
<tr class="odd">
<td><p>UDMA 6</p></td>
<td><p>133.3</p></td>
<td><p>ATA-7</p></td>
</tr>
<tr class="even">
<td><p>UDMA 7</p></td>
<td><p>166.6</p></td>
<td></td>
</tr>
</tbody>
</table>

Ultra DMA転送モードは、ATA/ATAPI-4以降で追加されたチップセットやUIDEコントローラカードに搭載された、専用の高速なDMAコントローラを使用して転送を行うモード。転送時のデータに[CRCを付加し](../Page/巡回冗長検査.md "wikilink")、信頼性を向上させている。

### その他

UDMA 6において、[32ビット](../Page/32ビット.md "wikilink") 33MHzの[PCIと同じ](../Page/Peripheral_Component_Interconnect.md "wikilink")、最大133Mbytes/secでの転送が可能となっているが、これは、あくまでもバスの転送帯域である。HDDに搭載されているキャッシュメモリからのデータを転送する時にのみ、額面通りの性能が発揮できるが、ほとんどの場合はハードディスクの読み出し速度が追従できない。 また、SCSIでは普通に用いられている、コマンド投入からデータ転送開始までの間、バスの開放を行い、バスの使用効率を上げる仕組み (Disconnect / Reconnect) は、ATA / ATAPI-6以降で規格化されているものの、実装されている機器はほとんど存在しないため、複数デバイスがある場合のスループットは数値から期待されるほどは高くないのが普通。

## シリアルATA

## 関連項目

  - [SASI](https://ja.wikipedia.org/wiki/SASI "wikilink")
  - [SCSI (Small Computer System Interface)](../Page/Small_Computer_System_Interface.md "wikilink")
  - [ST-506](../Page/ST-506.md "wikilink")
  - [ESDI](https://ja.wikipedia.org/wiki/Enhanced_Small_Disk_Interface "wikilink")
  - [シリアルATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")
  - [RAID](../Page/RAID.md "wikilink")
  - [ATA over Ethernet](https://ja.wikipedia.org/wiki/ATA_over_Ethernet "wikilink")
  - [転送速度](https://ja.wikipedia.org/wiki/転送速度 "wikilink")

## 外部リンク

### パラレルATA

  - [Overview and History of the IDE/ATA Interface](http://www.pcguide.com/ref/hdd/if/ide/over-c.html)
  - [Enhanced IDE/Fast-ATA/ATA-2 FAQ](http://www.faqs.org/faqs/pc-hardware-faq/enhanced-IDE/part1/)
  - [Hard Drive Size Barriers](http://www.dewassoc.com/kbase/hard_drives/hard_drive_size_barriers.htm)
  - [T13 Technical Standards Group](http://www.t13.org/)
  - [ATA IDE pinout](http://pinouts.ws/ata-ide-pinout.html)

### シリアルATA

  - [Serial ATA Working Group](http://www.serialata.org/)
  - [Tom's Hardware controller tests](http://www6.tomshardware.com/storage/20030204/index.html)

[Category:インタフェース規格](https://ja.wikipedia.org/wiki/Category:インタフェース規格 "wikilink")