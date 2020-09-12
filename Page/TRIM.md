> この記事は[TRIM](https://ja.wikipedia.org/wiki/TRIM)から翻訳されています。


**TRIMコマンド** （ ATAコマンドセット:**TRIM** 、 [SCSIコマンド](https://ja.wikipedia.org/wiki/SCSIコマンド "wikilink")セット:**UNMAP**）は、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")から[ソリッドステートドライブ](../Page/ソリッドステートドライブ.md "wikilink")（SSD）の未使用領域を内部的に消去するために用いられるコマンドである\[1\]。

SSDの登場から間もなくTRIMコマンドが登場した。 SSDへのハードウェア的な操作は、従来のハードディスクドライブとは大きく異なるため、オペレーティングシステムから削除やフォーマットなどの操作を従来通り行った場合に、書き込み操作で予期せず段階的なパフォーマンス低下が発生した\[2\]。TRIMの実行により、SSDは[ガベージコレクションをより効率的に処理できる](https://ja.wikipedia.org/wiki/ライトアンプリフィケーション "wikilink")。実行しない場合は、書き込み動作が遅延する可能性がある\[3\]。

一部のドライブにおいては、工場出荷状態にリセットするツールは、TRIMの導入前から存在していたが、ドライブ上のすべてのデータも削除されるため、使用中に最適化のために使用することは現実的ではない\[4\] 。また、2014年までには多くのSSDに対し、TRIMとは独立して機能する、バックグラウンドガベージコレクションメカニズムが搭載されるようになった。これにより、TRIMをサポートしていないOSでもパフォーマンスが維持できるようになったが、 [ライトアンプリフィケーション](https://ja.wikipedia.org/wiki/ライトアンプリフィケーション "wikilink")が発生しやすくなる上、フラッシュセルが摩耗しやすくなる欠点が存在した\[5\]。

## 背景

多くの[ファイルシステム](../Page/ファイルシステム.md "wikilink")では削除操作を処理する場合、データブロックに「未使用」のフラグを立てる\[6\] \[7\]。これにより、いずれのストレージメディアでもどの領域が本当に使用中であるかに関わらず、空きスペースとして領域を使用できる。上書き操作とは異なり、削除操作時においては、データを含むセクターへの物理的な書き込みは行われない。一般的なSSDにおいては、未使用の領域のリストを含むファイルシステム構造を処理せず，そのまま書き込み動作を行うため、メディア側では領域が使用可能になったことは認識されない。 これにより、[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")などでは、削除されたファイルを復元するツールが利用できるようになっている \[8\]。つまり、いずれのメディアの場合でも、未使用領域を使用したという場合でも上書き操作が行われている可能性が存在する。 磁気ディスクの場合、空のセクターへの書き込みと上書き操作に相違はないが、一部のSSDは機能の実装が最低レベルであるため、上書きは完全未使用の領域にデータを書き込む場合に比べて大きなオーバーヘッドを生じ、書き込みパフォーマンスを損なう可能性がある \[9\]。

SSDは、通常4〜16 [kiB単位でグループ化されたフラッシュメモリのセルにデータを格納し](https://ja.wikipedia.org/wiki/キビバイト "wikilink")、通常それを128〜512ページのブロックにグループ化する\[10\] 。[NANDフラッシュメモリセルの場合](../Page/フラッシュメモリ.md "wikilink")、領域が完全に空の場合にのみ書き込み操作が実行できる。データが残存している可能性がある場合、書き込み操作の前に領域を消去する必要がある。SSDへの書き込み操作はページ単位で実行できるが、ハードウェアの制限により、消去は常にブロック全体に対して実行される\[11\]。よって、SSDの空の領域への書き込み操作は非常に高速だが、以前に使用された領域を上書きする必要がある場合、遅延が発生する。 再度書き込む前にページ内のセルの消去が必要となるが、消去できるのはブロック全体であるので、上書きすると読み取り-消去-変更-書き込みサイクルが実行される \[12\]。削除対象のブロックに存在するデータ全体が一旦キャッシュに保存され、ブロック全体を消去し、上書きされた部分がキャッシュに書き込まれる。その後、更新されたブロック全体をフラッシュメディアに書き込む。この現象は[ライトアンプリフィケーション](https://ja.wikipedia.org/wiki/ライトアンプリフィケーション "wikilink")として知られている\[13\] \[14\]。

## 操作

TRIMコマンドを使用すると、オペレーティングシステムは、使用しなくなったページをSSDに通知できる。ファイル削除操作の場合、オペレーティングシステムはファイルのセクターを空き領域としてマークし、TRIMコマンドをSSDに送信する。その後新しいデータを書き込むときににSSDはブロックの内容を保持しないため、書き込み量を少なくすることとなり、書き込みスループットが高くなる。よって、寿命を延ばすことが期待できる。

ただし、SSDによってコマンドの実装方法が異なるため、得られるパフォーマンスが異なる場合がある\[15\] \[16\]。

TRIMはSSDに[LBA領域を無効としてマークするように指示し](https://ja.wikipedia.org/wiki/Logical_Block_Addressing "wikilink")、その後に領域の読み取りを行ったとしても意味のあるデータを返さなくなる。非常に短い間、データが依然としてフラッシュメモリ内に存在する可能性があるが、TRIMコマンドが発行されてガベージコレクションが実行された後は、専門家でさえデータを回復できる可能性はほぼないとされている\[17\]。

## 実装

### オペレーティングシステムでのサポート

TRIMコマンドの発行は、サポートされているオペレーティングシステムでのみ実行される。以下の表は、オペレーティングシステムと、コマンドをサポートする最初のバージョンを示している。さらに、ATA規格にTRIMコマンドが追加されるよりも前に設計された古いSSDでは、ファームウェアの更新が必要となる。更新されていない場合、新しいコマンドは無視されます。ただし、すべての古いSSDでTRIMコマンドをサポートするアップデートが準備されているわけではない。

空き領域を正しく理解しているプログラムだけが安全にコマンドを発行できるため、TRIMのサポートは、ファイルシステムドライバーによっても異なる。

<table>
<colgroup>
<col style="width: 15%" />
<col style="width: 15%" />
<col style="width: 70%" />
</colgroup>
<thead>
<tr class="header">
<th><p>オペレーティング・システム</p></th>
<th><p>サポート開始</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/DragonFly_BSD.md" title="wikilink">DragonFly BSD</a></p></td>
<td><p><span style="display:none">2011-05</span> 2011年5月[18]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/FreeBSD.md" title="wikilink">FreeBSD</a></p></td>
<td><p><span style="display:none">2010-07</span> 8.1 – 2010年7月[19]</p></td>
<td><p>バージョン8.1でブロックデバイスレイヤーに追加。<a href="../Page/Unix_File_System.md" title="wikilink">UFSに対しては</a>8.3および9で追加[20] 、<a href="../Page/ZFS.md" title="wikilink">ZFS</a>に対しては9.2で追加[21][22]。ソフトウェア<a href="../Page/RAID.md" title="wikilink">RAID</a>環境へは10で対応[23]。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/NetBSD.md" title="wikilink">NetBSD</a></p></td>
<td><p><span style="display:none">2012-10</span> 2012年10月[24]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Linuxカーネル.md" title="wikilink">Linux</a></p></td>
<td><p><span style="display:none">2008-12-25</span> 2.6.28–25 2008年12月[25]</p></td>
<td><p>2.6.28でFTL <a href="../Page/フラッシュメモリ.md" title="wikilink">NANDフラッシュデバイス初期サポートが追加</a>。 ATA TRIMコマンドのサポートは、2.6.33で追加[26]。 トリムを自動的に発行できるファイルシステムは、 <a href="../Page/Ext4.md" title="wikilink">Ext4</a>[27] 、<a href="https://ja.wikipedia.org/wiki/Btrfs" title="wikilink">Btrfs</a>[28]、<a href="../Page/File_Allocation_Table.md" title="wikilink">FAT</a>、GFS2、<a href="../Page/ジャーナリングファイルシステム.md" title="wikilink">JFS</a>[29]、<a href="../Page/XFS.md" title="wikilink">XFS</a>[30]、および<a href="https://ja.wikipedia.org/wiki/NTFS-3G" title="wikilink">NTFS-3G</a>。</p>
<p>一部のディストリビューションでは、パフォーマンスの問題[31]により、自動実行をデフォルトで無効にし、スケジュール化で対応している[32]。<a href="../Page/Ext3.md" title="wikilink">Ext3</a>、<a href="https://ja.wikipedia.org/wiki/NILFS" title="wikilink">NILFS</a>2、および<a href="https://ja.wikipedia.org/wiki/OCFS" title="wikilink">OCFS</a>2では、オフラインでのTRIMを実行する<a href="https://ja.wikipedia.org/wiki/ioctl" title="wikilink">ioctl</a>が用いられる。仕様ではTRIM実行範囲のリストが必要だが、カーネル3.0では、単一の範囲でのみ呼び出されるため、実行が遅い[33]。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/macOS" title="wikilink">macOS</a></p></td>
<td><p><span style="display:none">2011-06-23</span> 10.6.8(2011年6月23日)[34]</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Advanced_Host_Controller_Interface" title="wikilink">AHCIブロックデバイスドライバーは</a>、10.6.6（10J3210）でTRIMのサポート有無を表示する機能を搭載した[35] が、IOStorageFamilyおよび<a href="../Page/HFS_Plus.md" title="wikilink">HFS Plusファイルシステムを介してTRIMを実行できるようになった</a>10.6.8までは使用できなかった。 10.10.4以前では、AppleブランドのSSDに対してのみネイティブでTRIMが有効となっていた。ただし、サードパーティのユーティリティを使用して、他社製のSSDに対しても機能を有効化できる。 Yosemiteへのアップデートにより、古いサードパーティのTRIMドライバーが使用できなくなった[36]が、Yosemiteでも動作する更新されたドライバーは存在している[37] [38]。<a href="https://support.apple.com/en-us/HT204928">アップデート10.10.4</a>で、コマンドラインユーティリティのtrimforceから他社製SSDに対してもTRIMを有効化できるようになった[39]。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows" title="wikilink">Microsoft Windows</a></p></td>
<td><p><span style="display:none">2009–10</span> <a href="https://ja.wikipedia.org/wiki/Windows_7" title="wikilink">Windows 7</a>・<a href="https://ja.wikipedia.org/wiki/Windows_Server_2008_R2" title="wikilink">Windows Server 2008 R2</a> – 2009年10月[40] [41]</p></td>
<td><p>Windows 7は当初、 <a href="../Page/Advanced_Technology_Attachment.md" title="wikilink">パラレルATAおよび</a><a href="https://ja.wikipedia.org/wiki/シリアルATA" title="wikilink">シリアルATA</a>を含むATアタッチメントファミリのドライブに対してのみTRIMをサポートし、デバイス自体がコマンドを受け入れる場合でも、Storport PCI-Express SSDなどのデバイスに対してはサポートしていなかった[42]。ネイティブのMicrosoftドライバーでは、TRIMコマンドはWindows 7の<a href="https://ja.wikipedia.org/wiki/Advanced_Host_Controller_Interface" title="wikilink">AHCIおよびレガシーIDE</a> / ATAモードで動作することが確認されている[43]。Windows 8以降では、<a href="https://ja.wikipedia.org/wiki/NVM_Express" title="wikilink">NVMeによるPCI</a> Express SSDのトリムと、（UASP）などのSCSIドライバースタックを使用するデバイスに対しての、TRIMコマンドと同様のunmapコマンドをサポートする。 Windows 7に対しては、<a href="https://support.microsoft.com/kb/2990941">KB2990941</a>のアップデートをDISMを利用しセットアップ時に組み込むことにより、 を追加できる。 TRIMは<a href="https://ja.wikipedia.org/wiki/ReFS" title="wikilink">ReFS</a>と<a href="../Page/NT_File_System.md" title="wikilink">NTFSでサポートされており</a>、無効化するためのDisableDeleteNotifyスイッチも実装されている[44]。他のファイルシステムに対しての実装は、複数ソース間で情報が一致していない。</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/OpenSolaris.md" title="wikilink">OpenSolaris</a></p></td>
<td><p><span style="display:none">2010-07</span> 2010年7月[45]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Android.md" title="wikilink">Android</a></p></td>
<td><p><span style="display:none">2013から7</span> 4.3 [46] - 2013年7月24日[47]</p></td>
<td><p>デバイスが1時間以上アイドル状態で、80％以上充電されている場合（充電器に接続されている場合は30％以上）、24時間ごとに最大1回<code>fstrimを</code>自動的に実行する。</p></td>
</tr>
</tbody>
</table>

### RAIDへの問題

, TRIMコマンドへのサポートはほとんどすべてのハードウェア[RAID](../Page/RAID.md "wikilink")においては実装されていない。しかし、ソフトウェアRAID の場合はサポートされている場合がある。

#### Windows

[Windows 10では](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")、RAIDボリュームの構成時に「ドライブの最適化」のオプションを使用することで、SSDを含むRAIDボリュームでもTRIMをサポートする。

#### macOS

macOSの標準RAIDドライバーはTRIMをサポートしていない。この問題は、少なくとも10.7からmacOS 10.12.xまでのすべてのバージョンで該当する。

アップル以外製SSDでのTRIMサポートを含むサードパーティのSoftRAID®アプリケーションを使用する場合、TRIMはRAID（0、1、4、5、10）ボリュームでサポートされる。ただし、ターミナルコマンド「sudo trimforce enable」を使用して明示的に有効にする必要がある。

#### Linux

TRIMは、Linuxカーネル内のにおいて、2011年1月以降のリリースで使用可能となった。これは、BIOSによる「偽のハードウェアRAID」へのサポートであり、RAID上にあるファイルシステムからのTRIMリクエストを透過的に処理する\[48\]。

Linuxの汎用ソフトウェアRAIDシステムであるでは、システムがファイルシステムでmdtrimユーティリティを定期的に実行するように構成されている場合、RAID 1上でバッチベース（ファイル削除時実行）のTRIMを試験的にサポートしている\[49\]。Red Hat Enterprise Linux 6.5以降などのLinuxの新しいバージョンでは、mdraidは、単なるバッチジョブとしてではなく、実際にTRIMコマンドをリアルタイムで渡すことをサポートしている\[50\]。

しかし、[Red HatはソフトウェアRAIDのうち](../Page/レッドハット.md "wikilink")1、4、5、6を使用しないことを推奨しており、理由として、ほとんどのRAID管理ユーティリティ（Linuxにおけるなど ）での初期化時にデバイスのすべてのブロックに書き込み処理を行い、チェックサム（またはRAID 1/10の場合はドライブ間の検証）が適切に動作することを確認するためである。これにより、SSDにおいてはスペア領域以外のすべてのブロックが使用中の場合、パフォーマンスが大幅に低下する\[51\]。

一方、Red Hatは、TRIM（Linux用語では「破棄」）をサポートしており、LVMユーティリティは作成時にすべてのブロックに対する書き込み処理を行わないため、SSD上のLVM RAIDに対してはRAID 1またはRAID 10を使用することを推奨している\[52\]。

2010年3月、ユーザー間でIntel Rapid Storage Technology（RST）9.6ドライバーがRAIDボリュームでTRIMをサポートしていると信じられるようになったが、Intelは後にTRIMが[AHCIモードとRAIDモードのBIOS設定でサポートされるが](https://ja.wikipedia.org/wiki/Advanced_Host_Controller_Interface "wikilink")，RAIDボリュームの一部として使用される場合はサポートしないことを明らかにした\[53\]。

2012年8月の時点で、IntelはRapid Storage Technology（RST）11.2ドライバーを搭載した7シリーズのチップセットがMicrosoft Windows 7におけるRAID 0のTRIMをサポートしていることを確認している\[54\]。Intelは6シリーズチップセットのサポートを確認していないが、RAID 0ボリュームでのTRIMは、変更されたRAIDオプションROMを使用することで、Z68、P67、X79のチップセットで動作することが示されている\[55\]。6シリーズチップセットで公式にサポートされていない理由として、技術的なものではなく、検証コスト\[56\]ないし消費者にアップグレードを促す目的\[57\]であると推測されている。

X79チップセットを備えたマザーボードにおいてオプションROMを変更しなくても問題ない場合は、製造元がROMスイッチを追加した場合である。BIOSとUEFIの内部にRST ROMとRST-E ROMの両方があれば、RST-E ROMの代わりにRST ROMを使用して、TRIMを機能させることが可能となる\[58\]。Intelは、ROMと同じバージョンのドライバーを使用することで最高のパフォーマンスが得られると述べている。たとえば、BIOS・UEFIに11.0.0.0mオプションROMがある場合、11.xバージョンのドライバーを使用する必要がある\[59\]。

### サポートされていないファイルシステムでの有効化

ファイルシステムが自動的にTRIMをサポートしない場合でも、一部のユーティリティではTRIMコマンドを手動で送信できる。通常、ユーティリティが使用されていないブロックを判別し、リストをコマンドとしてドライブに渡す。このようなユーティリティは、複数のメーカーが提供している（例： Intel\[60\]、G.Skill\[61\] ）。また、一般的なユーティリティ（例：Linuxのv9.17以降の"wiper"\[62\] \[63\]、mdtrim）としても提供されている。hdparmとmdtrimはいずれも、ファイルシステムに大きなファイルを割り当て、割り当てられている物理的な場所を解決することにより、空きブロックを検索する。

## ハードウェアサポート

### ATA

TRIMコマンドの仕様\[64\]は、 [国際情報技術標準委員会](https://ja.wikipedia.org/wiki/情報技術規格国際委員会 "wikilink") （INCITS）の技術委員会T13が主導する[ATアタッチメント](../Page/Advanced_Technology_Attachment.md "wikilink") （ATA）インターフェイス標準の一部として標準化されている\[65\]。TRIMは、ドラフトACS-2仕様のDATA SET MANAGEMENTコマンド（opcode 06h）で実装されている\[66\]。また、ATA規格は、パラレル（IDE、PATA）・シリアル（SATA）の両方でサポートされている。

オリジナルのATA TRIMコマンドの欠点は、キューに入れられないコマンドとして定義されていたため、キューに入れられた読み取りおよび書き込み操作の通常のワークロードと簡単に混在させることができない点であった。 SATA 3.1では、これを修正するためにキューに入れられたTRIMコマンドが導入された\[67\]。

ATA IDENTIFY DEVICEコマンドから返されるSATAワード69および169により定義される、複数種のTRIMコマンドが存在する。

  - 非決定的TRIM：TRIM後の[論理ブロックアドレス](https://ja.wikipedia.org/wiki/Logical_Block_Addressing "wikilink") （LBA）への読み取りコマンドで、異なるデータを返す場合がある。
  - 確定的TRIM（DRAT）：TRIM後のLBAへの読み取りコマンドは、同じデータを返すか、確定的となる。
  - TRIM後の確定的読み取りゼロ（RZAT）：TRIM後のLBAへのすべての読み取りコマンドはゼロを返す。

SATAワード105には、ドライブがサポートできるDATA SET MANAGEMENTコマンドごとの512バイトブロックの最大数を示す追加情報が存在する。 通常、これはデフォルトで8または4 kBとなっているが、多くのドライブでは1として、TRIMのMicrosoft Windowsハードウェア要件に存在する、コマンド完了時間が20ミリ秒または8ミリ秒×LBA範囲エントリ数のいずれか以上かつ600ミリ秒未満でなければならないという条件を満たすようにしている\[68\]。

個々のLBA範囲はLBA範囲エントリと呼ばれ、8バイトで表現される。LBA自体は、LBA範囲エントリの最初の6バイトで表され、範囲長が残りの2バイトで表されている。範囲長のビットがすべてゼロの場合、LBA範囲エントリはパディングとして破棄される\[69\]。つまり、1回のTRIM範囲で最大で32 MBの64倍すなわち2GBが指定される。デバイスがSATAワード105で8をサポートしている場合、1回のTRIM（DATA SET MANAGEMENT）コマンドで16 GBをトリムできることとなる。

### SCSI

[SCSIでは](../Page/Small_Computer_System_Interface.md "wikilink")、TRIMと同一内容であるUNMAPコマンド、およびUNMAPフラグが設定されたWRITE SAMEコマンド（10および16バリアント）が存在する\[70\]。

### SD/MMC

[MultiMediaCardおよび](../Page/マルチメディアカード.md "wikilink")[SD](https://ja.wikipedia.org/wiki/SDメモリーカード "wikilink") ERASE（CMD38）コマンドは、ATAでのTRIMコマンドと同様の機能を提供するが、消去されたブロックをその後0または1で上書きする必要がある。eMMC 4.5では、破棄されたブロックの内容が不確定と見なすことができる点でTRIMコマンドにより類似した「破棄」サブオペレーションを定義した。

### NVM Express

[NVM Expressコマンドセットでは](https://ja.wikipedia.org/wiki/NVM_Express "wikilink")、ホストの意図を一連のブロック範囲のストレージデバイスに示めすための汎用のコマンドが存在する。その操作の1つである*deallocateコマンド*はTRIMを実行することと同義である。また、*deallocate*コマンド実行へのヒントを提供し、ディスクがゼロをトリミングして返すことを可能にする*Write Zeroes*コマンドも存在する。

## 短所

  - 暗号化が使用されている場合、TRIMコマンドを使用すると、使用されているブロックと使用されていないブロックに関する情報が明らかにってしまう\[71\]。
  - オリジナルのTRIMコマンドは、 [T13小委員会によって非キューコマンドとして定義されていたため](https://ja.wikipedia.org/wiki/情報技術規格国際委員会 "wikilink")、たとえば各ファイルシステムの削除コマンドの後に送信された場合など、不注意に使用すると、大量の実行ペナルティが発生する可能性がある。非キューコマンドの性質上、デバイスドライバは、未解決のコマンドがすべて完了するのを待機し、TRIMコマンドを発行してから、通常のコマンドを再開する必要がある。SSDのファームウェアによっては、TRIMが完了するまでにかなりの時間がかかってしまい、[ガベージコレクションサイクルがトリガーされる場合もある](https://ja.wikipedia.org/wiki/ライトアンプリフィケーション "wikilink")。このペナルティは、システムの使用率が最小になるようなバッチジョブをスケジュールすることにより、ファイルの削除ごとにトリミングするのではなく、定期的にバッチTRIMを実行することで最小限に抑えられる。このTRIMの欠点は、Queued TRIMコマンドの導入により、[シリアルATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")リビジョン3.1で改善した\[72\]\[73\]。
  - Queued TRIMへのサポートを誤ってシステムに通知しているか、実装に重大なバグがあるドライブファームウェアにより、いくつかのデバイス、特にMicronとCrucialのM500\[74\]およびSamsungの840および850シリーズなどで深刻なデータ破損を引き起こすとされている\[75\]。

以下のデバイスは、Linuxカーネルのでブラックリストに登録されており、非キューTRIMコマンド（）の送信を強制される\[76\]。

  - Micron/Crucial M500 (すべてのファームウェア)
  - Micron M510 (ファームウェアバージョン MU01)
  - Micron/Crucial M550 (ファームウェアバージョン MU01)
  - Crucial MX100 (ファームウェアバージョン MU01)
  - Samsung 840/850 シリーズ(すべてのファームウェア)

また、このファイルは、TRIMが発行されたときに誤ったブロックがデータを失う原因となるため、SuperSSpeed S238をTRIMコマンドへのブラックリストに載せている\[77\]\[78\]。

には、サブシステムのメンテナーがDRATフラグとRZATフラグ（`ATA_HORKAGE_ZERO_AFTER_TRIM`）を確実に認識しているSSDを列挙しているホワイトリストもある。 ホワイトリストに登録されているドライブは以下の通りである\[79\]。

  - Crucial SSD
  - Intel SSD 510を除くIntel SSD
  - Micron SSD
  - Samsung SSD
  - Seagate SSD\[80\]

## 関連項目

  - [データ残留](https://ja.wikipedia.org/wiki/データの完全消去 "wikilink")

## 参考文献

## 外部リンク

  - [*From write() down to flash chips*](https://web.archive.org/web/20100227234254/http://www.devwhy.com/blog/2009/8/4/from-write-down-to-the-flash-chips.html) – An explanation on how the TRIM command lets SSDs erase data not used by the filesystem
  - [*TRIM Command White Paper*](http://www.maximumpc.com/article/features/white_paper_trim_command) – A white paper explaining the command's purpose and actions
  - Fusion-io Patent ["Apparatus, system, and method for redundant write caching"](https://www.google.com/patents/US8706968?dq=%22Fusion-io%22+trim&hl=en&sa=X&ei=ZNWlU4ugOc_doAShvoHwCQ&ved=0CCsQ6AEwAjgU)

[Category:コンピュータ](https://ja.wikipedia.org/wiki/Category:コンピュータ "wikilink")

1.
2.
3.  Shimpi, Anand Lal. (18 March 2009). p. 10.
4.  Shimpi, Anand Lal. (18 March 2009). p. 11.
5.
6.
7.  Shimpi, Anand Lal. (18 March 2009). p. 7.
8.
9.
10.
11. Shimpi, Anand Lal. (18 March 2009). p. 5.
12. Shimpi, Anand Lal. (18 March 2009). p. 8.
13.
14.
15. Shimpi, Anand Lal. (18 March 2009). p. 10.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.
35.
36.
37.
38.
39.
40.
41.
42. [Geoff Gasior (2012)](http://techreport.com/articles.x/22663) OCZ's RevoDrive 3 X2 240GB solid-state drive
43.
44.
45.
46.
47. ["Android 4.3 announced, rolling out to Nexus devices today"](https://www.theverge.com/2013/7/24/4550234/android-4-3-announcement).*[The Verge](https://ja.wikipedia.org/wiki/The_Verge_\(website\) "wikilink")*. 24 July 2013. Retrieved 24 July 2013.
48.
49.
50.
51.
52.
53.
54.
55.
56.
57.
58.
59.
60.
61.
62.
63.
64.  (draft specification T13/e07154r6)
65.
66.
67.
68.
69.
70.
71.
72. <http://www.sata-io.org/technology/6Gbdetails.asp>
73.
74.
75.
76.
77.
78.
79.
80.