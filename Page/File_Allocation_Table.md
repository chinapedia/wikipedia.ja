> この記事は[File Allocation Table](https://ja.wikipedia.org/wiki/File_Allocation_Table)から翻訳されています。


**File Allocation Table** (ファイル・アロケーション・テーブル、**FAT**、) とは、[MS-DOS](../Page/MS-DOS.md "wikilink")の[ファイルシステム](../Page/ファイルシステム.md "wikilink")（および、その前身となったMicrosoft DISK-BASICのファイルシステム）における[ディスク内の](../Page/ディスクメディア.md "wikilink")[ファイルの位置情報などを記録するための領域である](../Page/ファイル_\(コンピュータ\).md "wikilink")。これが転じて現在では[MS-DOS](../Page/MS-DOS.md "wikilink")に採用されていたFATを用いるファイルシステムの名前としてFATファイルシステム、さらにそれを略してFATと呼ぶことも多い（なお後者でDISK-BASICのそれを指すことはまずない）。

## 概要

オリジナルのFile Allocation Tableは[1977年](../Page/1977年.md "wikilink")に、[ビル・ゲイツ](../Page/ビル・ゲイツ.md "wikilink")と[マーク・マクドナルド](https://ja.wikipedia.org/wiki/マーク・マクドナルド "wikilink")によって開発され、[DISK-BASIC](https://ja.wikipedia.org/wiki/DISK-BASIC "wikilink")の中のファイル管理仕様として採用された。

DISK-BASIC以降、MS-DOSのファイルシステムでもFATが採用され、MS-DOSがDOSとしての[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")を確立し、さらにその後[Windows NTで新しいファイルシステム](../Page/Microsoft_Windows_NT.md "wikilink")[NTFSを普及させた後も](../Page/NT_File_System.md "wikilink")、FATを採用したファイルシステムは使われ続けている。

MS-DOS以降は、[Windows Meまでの一般家庭向けの](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink")[OSの標準ファイルフォーマットとして使用されていた](../Page/オペレーティングシステム.md "wikilink")。[Windows NT系のOSでも使用可能であるが](../Page/Windows_NT系.md "wikilink")、他のWindowsからのアップグレードや[リムーバブルメディア](../Page/リムーバブルメディア.md "wikilink")のために用意されているものであり、[セキュリティなどの観点から必ずしも利用が推奨されておらず](../Page/コンピュータセキュリティ.md "wikilink")、FATを利用している状況下での動作制限も存在する。

[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")の時代の設計を元にしてあるため、ディスク総容量に対し管理領域が少なくて済む、高速にアクセスできるなどの利点があるが、その反面、堅牢でない、大容量ディスクでは非効率、拡張性に乏しい、ファイル名が8文字+[拡張子](../Page/拡張子.md "wikilink")3文字までしか扱えない（VFAT非対応の場合）、タイムスタンプが[ローカル時間](https://ja.wikipedia.org/wiki/ローカル時間 "wikilink")なので[タイムゾーン](https://ja.wikipedia.org/wiki/タイムゾーン "wikilink")をまたいで使ったり[夏時間](../Page/夏時間.md "wikilink")・冬時間が違ったりすると正しく（意図した）ファイル変更時刻が表示できないことがあるなど様々な欠点がある。それでも、その特徴と実装の容易さ、読み書きできる[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")が多いことから、フロッピーディスクや小容量[メモリーカード](../Page/メモリーカード.md "wikilink")用のファイルシステムとして依然使われ続けている。現在は[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")や[ビデオゲーム](https://ja.wikipedia.org/wiki/ビデオゲーム "wikilink")機などでも広く使われている。

FATは、クラスタ番号の管理[ビット](../Page/ビット.md "wikilink")数によって「FAT12」、「FAT16」、「FAT32」の3種類がある（なお、DISK-BASICでは8ビットであった）。Windowsでは、FAT32を除いてFATと表示している。また、俗に「FAT64」と言う記述を見かけることがあるが、これは「Windows NT系で使用可能なクラスタサイズが64[キロバイト](../Page/キロバイト.md "wikilink")のFAT16」\[1\]または「exFAT」\[2\]を示し、クラスタ番号のビット数を示すものでは無い。

上記のように[リムーバブルメディア](../Page/リムーバブルメディア.md "wikilink")の[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")としてはFAT16またはFAT32が多く使用されているが、ボリュームとファイルのサイズ制限が問題になっている。このほか種々の問題を解決するため、exFATが開発された。

なお、VFATとexFATを除いた仕様は国際規格として[ECMA](../Page/Ecmaインターナショナル.md "wikilink")-107と[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")/[IEC](../Page/国際電気標準会議.md "wikilink") 9293として標準化されている。日本ではJIS X 0605規格として登録されている。

## 仕様

[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")（後に[ハードディスクも](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")）の記録単位として[セクタがあり](https://ja.wikipedia.org/wiki/ディスクセクタ "wikilink")、1以上のセクタをまとめてクラスタとして管理する。FATは言わばクラスタ番号による巨大な一次元[配列](../Page/配列.md "wikilink")であり、ディスクの最初から最終までのクラスタ番号ごとに、そのクラスタが使用中なのか、空き領域なのか（または、システム予約領域、バッドクラスタ：エラー）などの状態を保持する。

そして、ディスク上の1つの[ファイルは](../Page/ファイル_\(コンピュータ\).md "wikilink")、1つ以上のクラスタの連鎖として管理される。すなわち、あるファイルの最初のクラスタ番号が[ディレクトリ](../Page/ディレクトリ.md "wikilink")・エントリに格納されており、ファイルの最初のデータはそのクラスタ番号の領域に格納されている。そして、最初のクラスタ番号に対応するFAT上のエントリは、その次に繋がるクラスタ番号を保持するか、またはそこが最終クラスタであるマークを保持している。

このように、FATはディスクの管理上、最重要なデータテーブルであり、もしこの情報が損なわれると、ディスク上のファイル等が正常に読み出せなくなってしまう。そのため、FATを実現しているファイルシステムでは、FATのテーブルの複数のコピーを保持するのが一般的である。

DISK-BASICの時代等は、FATはマウント命令によって主記憶に読み込まれて、ファイルの更新とともに主記憶上でだけ更新され、アンマウント命令によって初めてディスクへ書き戻されるのが一般的であった。これは、ファイルを更新するたびにFATに書き戻すことが無いよう、高速化を図った仕様ではあるが、他方、ユーザーのアンマウント命令の実行忘れにより、FATだけが古い状態のままになり、ファイルの不整合が生じてデータを損なう事故が多発した。

MS-DOS以降では、バッファリング・遅延書き込みにより、ディスクの最終書き込みまでにはFATを必ず自動的に書き戻す仕様になっているため、アクセスの途中にディスクを抜かない限りは、データ不整合が発生するおそれは殆どなくなり、マウント・アンマウントをユーザが意識することはなくなった（ただし、USB接続の大容量[リムーバブルメディア](../Page/リムーバブルメディア.md "wikilink")の普及により、遅延書き込みのフラッシュの保証のために、「ハードウェアの安全な取り外し」として再認識されるに至っている）。

## 実装

<table>
<tbody>
<tr class="odd">
<td></td>
<td><p>FAT12</p></td>
<td><p>FAT16</p></td>
<td><p>FAT32</p></td>
<td><p>exFAT</p></td>
</tr>
<tr class="even">
<td><p>開発者</p></td>
<td><p><a href="../Page/マイクロソフト.md" title="wikilink">マイクロソフト</a></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>正式名</p></td>
<td><p>File Allocation Table</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>（12ビット ver）</p></td>
<td><p>（16ビット ver）</p></td>
<td><p>（32ビット ver）</p></td>
<td><p>extended バージョン</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>導入</p></td>
<td><p><a href="../Page/1977年.md" title="wikilink">1977年</a>,<br />
(<a href="../Page/Microsoft_BASIC.md" title="wikilink">Microsoft Disk BASIC</a>)</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/1987年" title="wikilink">1987年</a><a href="../Page/11月.md" title="wikilink">11月</a>,<br />
(<a href="https://ja.wikipedia.org/wiki/Compaq" title="wikilink">Compaq</a> DOS 3.31)</p></td>
<td><p><a href="../Page/1996年.md" title="wikilink">1996年</a><a href="../Page/8月.md" title="wikilink">8月</a>,<br />
(<a href="../Page/Microsoft_Windows_95.md" title="wikilink">Windows 95</a> OSR2)</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_CE" title="wikilink">Windows Embedded CE 6.0</a></p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/パーティション.md" title="wikilink">パーティション</a><a href="../Page/識別子.md" title="wikilink">識別子</a></p></td>
<td><p><code>0x01</code> (<a href="../Page/マスターブートレコード.md" title="wikilink">MBR</a>)</p></td>
<td><p><code>0x04</code>, <code>0x06</code>, <code>0x0E</code> (MBR)</p></td>
<td><p><code>0x0B</code>, <code>0x0C</code> (MBR)<br />
<code>EBD0A0A2-B9E5-4433-87C0-68B6B72699C7</code> (<a href="../Page/GUIDパーティションテーブル.md" title="wikilink">GPT</a>)</p></td>
<td><p>0x07 (MBR) EBD0A0A2-B9E5-4433-87C0-68B6B72699C7 (GPT)</p></td>
</tr>
<tr class="odd">
<td><p>構造</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ディレクトリ</p></td>
<td><p>テーブル</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>領域管理</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/リンクリスト" title="wikilink">リンクリスト</a></p></td>
<td><p>リンクリスト、ビットマップ</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>不良ブロック</p></td>
<td><p>クラスタタグ</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>限度</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>最大ファイルサイズ</p></td>
<td><p>32<a href="https://ja.wikipedia.org/wiki/メビバイト" title="wikilink">MiB</a></p></td>
<td><p>2<a href="https://ja.wikipedia.org/wiki/ギビバイト" title="wikilink">GiB</a><br />
4<a href="https://ja.wikipedia.org/wiki/ギビバイト" title="wikilink">GiB</a> (NT)</p></td>
<td><p>4<a href="https://ja.wikipedia.org/wiki/ギビバイト" title="wikilink">GiB</a> - 1 <a href="../Page/バイト_(情報).md" title="wikilink">byte</a></p></td>
<td><p>16<a href="https://ja.wikipedia.org/wiki/エクスビバイト" title="wikilink">EiB</a></p></td>
</tr>
<tr class="odd">
<td><p>クラスタサイズ</p></td>
<td><p>512<a href="../Page/バイト_(情報).md" title="wikilink">byte</a> 〜 32<a href="https://ja.wikipedia.org/wiki/キビバイト" title="wikilink">KiB</a></p></td>
<td><p>512<a href="../Page/バイト_(情報).md" title="wikilink">byte</a> 〜 32<a href="https://ja.wikipedia.org/wiki/キビバイト" title="wikilink">KiB</a>（NT系では64<a href="https://ja.wikipedia.org/wiki/キビバイト" title="wikilink">KiB</a>）</p></td>
<td><p>512<a href="../Page/バイト_(情報).md" title="wikilink">byte</a> 〜 32<a href="https://ja.wikipedia.org/wiki/キビバイト" title="wikilink">KiB</a></p></td>
<td><p>512<a href="../Page/バイト_(情報).md" title="wikilink">byte</a> 〜 32<a href="https://ja.wikipedia.org/wiki/メビバイト" title="wikilink">MiB</a></p></td>
</tr>
<tr class="even">
<td><p>最大ファイル数</p></td>
<td><p>4,077</p></td>
<td><p>65,517</p></td>
<td><p>268,435,437</p></td>
<td><p>ディレクトリ毎に 2,796,202</p></td>
</tr>
<tr class="odd">
<td><p>最大ボリュームサイズ</p></td>
<td><p>32<a href="https://ja.wikipedia.org/wiki/メビバイト" title="wikilink">MiB</a></p></td>
<td><p>2<a href="https://ja.wikipedia.org/wiki/ギビバイト" title="wikilink">GiB</a><br />
<small>4<a href="https://ja.wikipedia.org/wiki/ギビバイト" title="wikilink">GiB</a> (NT)</small></p></td>
<td><p>2<a href="https://ja.wikipedia.org/wiki/テビバイト" title="wikilink">TiB</a><br />
<small>8<a href="https://ja.wikipedia.org/wiki/テビバイト" title="wikilink">TiB</a>（2<a href="https://ja.wikipedia.org/wiki/キビバイト" title="wikilink">KiBセクタ</a>）</p></td>
<td><p>TBU</p></td>
</tr>
<tr class="even">
<td><p>最大ファイル名長</p></td>
<td><p>8.3形式、または255文字</p></td>
<td><p>255文字</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>特徴</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>記録可能なタイムスタンプ</p></td>
<td><p>作成（精度は10ミリ秒）、修正（精度は2秒）、アクセス（精度は1日）<br />
<small>（長いファイル名がサポートされている時のみ、作成時間とアクセス日付が更新できる）</small></p></td>
<td><p>作成（精度は10ミリ秒）、修正（精度は10ミリ秒）、アクセス（精度は2秒）</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>日付範囲</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/1980年" title="wikilink">1980年</a><a href="../Page/1月1日.md" title="wikilink">1月1日</a> - <a href="https://ja.wikipedia.org/wiki/2107年" title="wikilink">2107年</a><a href="../Page/12月31日.md" title="wikilink">12月31日</a></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/フォーク_(ファイルシステム)" title="wikilink">フォーク</a></p></td>
<td><p>not natively</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>属性</p></td>
<td><p>読み取りのみ、隠し、システム、ボリュームラベル、サブディレクトリ、アーカイブ</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/ファイルパーミッション.md" title="wikilink">ファイルパーミッション</a></p></td>
<td><p>無し</p></td>
<td><p>実装により可<br />
（現在はWindows CE 6のみ）</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>透過的圧縮</p></td>
<td><p>ボリューム毎、<a href="https://ja.wikipedia.org/wiki/Stac_Electronics" title="wikilink">Stacker</a>、DoubleSpace (DriveSpace)</p></td>
<td><p>無し</p></td>
<td><p>無し</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>透過的暗号化</p></td>
<td><p><a href="../Page/DR-DOS.md" title="wikilink">DR-DOS</a>でのみボリューム毎</p></td>
<td><p>無し</p></td>
<td><p>無し</p></td>
<td></td>
</tr>
</tbody>
</table>

MS-DOS起源のFATファイルシステムの実装でも同様に、記憶ディスク上の[セクタはクラスタと呼ばれる単位にまとめられ](https://ja.wikipedia.org/wiki/ディスクセクタ "wikilink")、1クラスタ内のセクタはディスク上では物理的に連続している。

FATはディスク上では最初の方に配置している（ブートローダ、システムイメージの次あたり）。FATとは別に、ルート[ディレクトリ](../Page/ディレクトリ.md "wikilink")テーブルが存在する。これもFATの近傍に配置され、ルートディレクトリのディレクトリ・エントリを保持する。ディレクトリ・エントリは、ファイル名とファイルの属性、そのファイルを構成する最初のクラスタ番号を保持する。

なお、サブディレクトリ（サブフォルダ）は、ルートディレクトリ（およびサブディレクトリ）に存在する特殊なファイル・エントリとして実現される。すなわち、例えば*\\subdir* は、ルート (*\\*) ディレクトリーテーブルに*subdir*のディレクトリ・エントリが存在し、かつ、そのエントリが表現するファイルそのものをディレクトリテーブルと見なして処理する。サブディレクトリのサブディレクトリ（例：*\\subdir\\subdir*）も同様である。

ともかく、ディレクトリ・エントリに記録された先頭クラスタ番号と、その番号が指し示すFAT上のエントリを組み合わせることにより、1つのファイルが複数のクラスタにまたがって存在する状況を記録している。

なお、FAT上のエントリには、続きのクラスタ番号の他に、一部予約番号も記録される。それは以下の通りである（以下の数値はFAT16の場合）。

  - 0000h: 未使用クラスタである
  - 0001h: （予約）
  - FFF7h: 不良クラスタとしてマークされている
  - FFF8h - FFFFh: 最後のクラスタである

なお、FATの多重化数は2である。ただし、通常は、多重化FAT間の不整合が、自動で検出されることはなく、手動で検査・修復[プログラムを実行する必要がある](../Page/プログラム_\(コンピュータ\).md "wikilink")。

### FAT12

当初のFATファイルシステムは、現在はFAT12と呼ばれている。12ビットのクラスタ識別子を利用し、総クラスタ数は最大4084個である。クラスタサイズは512バイトから32[KiBまで使用することが出来る](https://ja.wikipedia.org/wiki/キビバイト "wikilink")。しかし、ボリュームの総セクタ数が16ビットで管理されているため、セクタサイズが512バイトの場合、ボリュームサイズは32[MiBまでとなる](https://ja.wikipedia.org/wiki/メビバイト "wikilink")。現在は主にフロッピーディスクのフォーマットとして残されている。

### FAT16

FAT16は、16ビットのクラスタ識別子を利用したFATで、総クラスタ数は最大65,524個である。クラスタサイズは512バイトから32KiB（NT系では64KiB）まで使用できる\[3\]。ボリュームサイズは2GiB（NT系では4GiB）までとなる。当初はボリュームの総セクタ数がFAT12と同様に16ビットで管理されていたため、セクタサイズが512バイトの場合、ボリュームサイズは32MiBまでであったが、Compaq DOS 3.31で総セクタ数を32ビットで管理するように拡張され、この制限は取り払われた\[4\]。

MS-DOSは4.0以降で32ビットの総セクタ数に対応したが、日本国内では[PC-98用のMS](../Page/PC-9800シリーズ.md "wikilink")-DOS 4.0は発売されず、32ビットセクタへの対応はMS-DOS 5.0まで待たされることとなった。代わりに、PC-98用のMS-DOS 3.3では、512バイトの物理セクタを4個まとめて2KiBの論理セクタとして扱うことで、128MiBまでのボリュームサイズに対応していた。また、[セイコーエプソン](../Page/セイコーエプソン.md "wikilink")が[PC-286](https://ja.wikipedia.org/wiki/PC-286 "wikilink")シリーズ用のMS-DOS4.01を発売しており、これをPC-9800シリーズで使うこともできた。

### VFAT

VFAT (Virtual FAT) は「長いファイル名」(Long File Name, LFN) をFAT (12/16/32)で扱えるようにする拡張である。LFNでは、[Windows NT 3.5](../Page/Microsoft_Windows_NT.md "wikilink")\[5\]および[Windows 95から実装された機能で](../Page/Microsoft_Windows_95.md "wikilink")、これにより最大255文字（[UTF-16](../Page/UTF-16.md "wikilink") LEで処理されるので1文字2バイト）までのファイル名を付与できる\[6\]（ただし、[Windows 9x系では実装上](../Page/Windows_9x系.md "wikilink")255バイトまでしか扱えない）。ファイルシステム上はディレクトリエントリの扱いが若干異なる程度で、[下位互換](https://ja.wikipedia.org/wiki/下位互換 "wikilink")性も不十分ながら保たれている。

VFATはFAT互換の[8.3](https://ja.wikipedia.org/wiki/8.3 "wikilink")形式の短いファイル名の直前のディレクトリエントリにボリュームラベルビットの立ったエントリが存在した場合、それがこのファイルの長いファイル名であると解釈する。そのため、従来のFATしかサポートしないOSからVFATを参照した場合には、短いファイル名のみが見えることとなり、一応のアクセスは可能となる。しかし、ファイルの書き込みを行ったり、MS-DOS時代のディレクトリエントリを最適化するプログラムや[ツールを使用した場合](https://ja.wikipedia.org/wiki/ツールソフトウェア "wikilink")、長いファイル名が破壊されてしまうため、[互換性](../Page/互換性.md "wikilink")が不十分であると言われている。

本稿ではVFATをLFNの拡張機能としているが、厳密にいうと、当初VFATとは[Windows 3.1から](../Page/Microsoft_Windows_3.x.md "wikilink")[Windows Meと引き継がれてきた](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink")[仮想デバイスドライバ](../Page/仮想デバイスドライバ.md "wikilink")の1つ (VFAT.VXD) を意味した。これは、（[プロテクトモード](../Page/プロテクトモード.md "wikilink")で動作する）Windows[アプリケーション上からMS](../Page/アプリケーションソフトウェア.md "wikilink")-DOSファイルをアクセスする時に、（[リアルモード](../Page/リアルモード.md "wikilink")で動作する）MS-DOSシステムを呼ばずに済むようにするためのものである。初期のVFATドライバ（Windows 95よりも前）では、LFNをサポートしていない。

### FAT32

FAT32は、Windows 95 OSR2で登場し、32ビット化されたFATである\[7\]。32ビットのクラスタ識別子を利用し管理するが、上位4ビット分は予約としており、28ビットでの管理となる。クラスタサイズは4KiBから32KiBまで使用できる。ボリュームサイズは理論上8TiBまでとなる\[8\]。しかし、ボリュームの総セクタ数を32ビットで管理（最大4,294,967,295）しているため、セクタサイズが512バイトの場合にボリュームサイズは2TiBに制限される。

クラスタは28ビットのため、論理上268,435,444個のクラスタを扱えるはずであるが、[スキャンディスク](../Page/スキャンディスク.md "wikilink")の実装上の問題で[Windows 9x系上では事実上](../Page/Windows_9x系.md "wikilink")4,177,920個のクラスタしか利用できない（32KiBクラスタ時、およそ124.55GiB）。なお、Windows 9x系に付属するパーティション作成ツールであるFDISKでは64GB以上のFAT32パーティションを作成できず、これに対応させる修正版が公開されている\[9\]\[10\]。

Windows NT系では[Windows 2000から利用可能となったが](../Page/Microsoft_Windows_2000.md "wikilink")、新規のフォーマット作業では意図的に32GiBまでの制限を設けている\[11\]。そのため、32GiBを超えるサイズのボリュームを作成するには、[サードパーティー](../Page/サードパーティー.md "wikilink")製のフォーマットツールを利用する必要がある。

### exFAT

exFAT (Extended File Allocation Table) は[Windows Embedded CE 6.0で導入された](https://ja.wikipedia.org/wiki/Microsoft_Windows_CE "wikilink")[フラッシュドライブ](https://ja.wikipedia.org/wiki/フラッシュドライブ "wikilink")向けに最適化された新しい規格のFATである（従来のFATとの互換性はない）。NTFSの使用がオーバーヘッドから適切ではない用途に向け開発された。Transaction-Safe FAT File System (TFAT) の活用も可能である。Windows Embedded CE 6.0の下では TFAT はexFAT 上でのみサポートされる\[12\]。Windows XPとVistaでも、後に使用可能になった。Windows XPでは更新プログラム（SP1以前は利用不可）、VistaはService Pack 1でexFAT対応が追加される\[13\]\[14\]。 4GiBまでであった1ファイルあたりのサイズ制限は撤廃され、16[EiBまで利用可能となる](https://ja.wikipedia.org/wiki/エクスビバイト "wikilink")。実装次第でNTFSの様なセキュリティ[ACLや](../Page/アクセス制御リスト.md "wikilink")[ジャーナルを備えることも可能となっている](https://ja.wikipedia.org/wiki/ジャーナルファイルシステム "wikilink")。また、8.3形式のファイル名は削除された。

## 脚注

## 関連項目

  - [NTFS](../Page/NT_File_System.md "wikilink")
  - [WinFS](../Page/WinFS.md "wikilink")
  - [Logical Block Addressing](https://ja.wikipedia.org/wiki/Logical_Block_Addressing "wikilink")
  - [マスターブートレコード](../Page/マスターブートレコード.md "wikilink")
  - [ブートセクタ](../Page/ブートセクタ.md "wikilink")
  - [SDメモリーカード](https://ja.wikipedia.org/wiki/SDメモリーカード "wikilink")
  - [メモリースティック](../Page/メモリースティック.md "wikilink")

## 外部リンク

  - [FAT32 File System Specification](https://msdn.microsoft.com/en-us/windows/hardware/gg463080.aspx)
  - [Embedded FAT File System](http://www.zeeis.com/fat-file-system/)
  - [ECMA-107 Volume and File Structure of Disk Cartridges for Information Interchange](http://www.ecma-international.org/publications/standards/Ecma-107.htm)
  - [KB154997:FAT32 ファイルシステムについて](http://support.microsoft.com/kb/154997/ja/)

[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:MS-DOS・Windows3.x・9x系](https://ja.wikipedia.org/wiki/Category:MS-DOS・Windows3.x・9x系 "wikilink") [Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:1977年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1977年のソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.