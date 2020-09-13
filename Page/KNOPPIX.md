> この記事は[KNOPPIX](https://ja.wikipedia.org/wiki/KNOPPIX)から翻訳されています。


**KNOPPIX**（クノーピクス\[1\]、ノピックス）とは、[CD-ROM](../Page/CD-ROM.md "wikilink")または[DVD-ROM](https://ja.wikipedia.org/wiki/DVD-ROM "wikilink")から起動することが可能な[Debian](../Page/Debian.md "wikilink")ベースの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")。

## 概要

[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")のKlaus KnopperがDebianパッケージを元に開発しているものが原型となる。一枚のCD/DVD/USBメモリなどのリムーバブルメディアから起動できる[Live CDとして利用することを基本としていることが特徴](../Page/Live_CD.md "wikilink")。

当初はCD版のみの提供だったが、収録希望のアプリケーションの数が増えるに伴いCD-ROMの容量では不足するため、正式な同時リリース決定の前に二度ほどDVDイメージの頒布も行われている。Version 4.0で開発者のKlaus KnopperがDVD-ROM版とCD-ROM版をほぼ同時に提供することを決定した。CD-ROM版を"light"（軽量版）、DVD-ROM版を"maxi"（大容量版）と位置付け、DVD版では更に多くのアプリケーションが標準で利用可能となっている。4.0版（DVD版）は[2005年](../Page/2005年.md "wikilink")[6月22日](../Page/6月22日.md "wikilink")にLinuxTagで配布された。Version 7.2でCD-ROM版の提供を終了し、DVD-ROM版に一本化された。

Live CDとしての利用が前提であるため、[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")にOSを[インストール](../Page/インストール.md "wikilink")する必要がなく、初期状態ではハードディスクに変更を加えずに[Linux](../Page/Linux.md "wikilink")を稼働させ、さまざまなコマンドやアプリケーションを使うことができる。 これらの特性から、ハードディスクに障害が発生している場合に仮のシステムとして起動させ、ハードディスクの診断や他のメディアなどへのデータをサルベージするなどの作業にも使用可能である。

また、パソコンに接続されたハードウエアを数多くサポートし自動的に認識する能力に優れていることも特徴の1つで、例えばユーザーはビデオ・カードの種類などを指定する必要がなく、直ちにGUIを利用可能となる。ネットワークについても[DHCP環境にあれば](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")、[LANにつながっているだけで自動的に接続設定がおこなう](../Page/Local_Area_Network.md "wikilink")。ネットワークに繋がれば、必要なファイルなどは[http](https://ja.wikipedia.org/wiki/http "wikilink"), [ftp](https://ja.wikipedia.org/wiki/ftp "wikilink")などで保存できるためハードディスクなどがなくても困らない。

基本的に1CD/1DVD[ブータブル](../Page/ブート.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")であるが、[LibreOffice](https://ja.wikipedia.org/wiki/LibreOffice "wikilink")などの[アプリケーションソフト](https://ja.wikipedia.org/wiki/アプリケーションソフト "wikilink")が付属している。CD/DVDから起動するため、標準では書き込み（[データ](../Page/データ.md "wikilink")の変更）を行うことができるユーザのホーム・[ディレクトリ](../Page/ディレクトリ.md "wikilink")などが[RAMディスク](../Page/RAMディスク.md "wikilink")上に置かれており、パソコンの[再起動](../Page/再起動.md "wikilink")や[シャットダウン](../Page/シャットダウン.md "wikilink")で保存したデータは消えてしまう。

しかし、それらを[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")、可搬式の[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")、[USBメモリ](https://ja.wikipedia.org/wiki/USBメモリ "wikilink")などに保存することもできる。そのため国外の旅行先でも、CD-ROMから起動できるパソコンを借りることによって、自国語環境の元で簡単な仕事を行うこともできる。

データの書き換えができないCD/DVDに起動に必要な要素がすべて格納されているため、起動中にどのような状態になっても再起動すれば元に戻る、という特徴がある。この特徴を生かし、不特定多数がパソコンを共有する公共の場に置かれる[キオスク端末](https://ja.wikipedia.org/wiki/キオスク端末 "wikilink")や、学校教育などでの使用が考えられている。

また、最近OSで流行している[3Dデスクトップ](https://ja.wikipedia.org/wiki/3Dデスクトップ "wikilink")の搭載に対応するため、5.1から、3Dデスクトップ環境[Beryl](../Page/Beryl.md "wikilink")、5.3.1からはその後継の[Compiz Fusionが搭載された](../Page/Compiz_Fusion.md "wikilink")。

## KNOPPIXの特徴

CDやDVDから起動できることが、最大の特徴であるKNOPPIXだが、バージョンごとに新たな技術的試みが取り込まれていることも、KNOPPIXの特徴となっている。

### UnionFS / aufs

KNOPPIX3.8.1からは、[UnionFS](https://ja.wikipedia.org/wiki/UnionFS "wikilink")というファイルシステムが採用されており、本来書き込むことができないはずのCD-ROMに対し、仮想的にファイルを書き込むことができるようになった。 これにより、一時的にではあるが、それまで不可能だったパッケージの追加などがおこなえるようになった。

KNOPPIX5.1からは安定性向上のため、unionfsに替わり、[aufs](https://ja.wikipedia.org/wiki/aufs "wikilink")(another unionfs)が採用されている。

### 各種エミュレータの搭載

KNOPPIXには各種エミュレーション用ソフトウエア（[エミュレータ](../Page/エミュレータ.md "wikilink")）が搭載されており、最もエミュレータが利用しやすいOSのひとつとなっている。[QEMU](../Page/QEMU.md "wikilink")はKNOPPIX上、もしくは[Windows上でKNOPPIXを起動でき](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Cooperative LinuxをWindowsにインストールすることで](../Page/Cooperative_Linux.md "wikilink")、Windows上の一ウインドウとしてKNOPPIXが動作する。[Xenと組み合わせた版であるXenoppixでは](../Page/Xen_\(仮想化ソフトウェア\).md "wikilink")、KNOPPIX上で[Plan 9や](../Page/Plan_9_from_Bell_Labs.md "wikilink")[NetBSD](../Page/NetBSD.md "wikilink")が利用できる。

### CD/DVD以外からの起動

KNOPPIXはCD/DVDから起動させるのが一般的であるが、多彩な起動方法が選択できることも特徴のひとつで、CD/DVDに格納されたイメージをハードディスクにインストールしてしまい、通常のLinuxディストリビューションの様にハードディスクから起動することも可能である。

KNOPPIX5.1以降には、KNOPPIXをUSBフラッシュメモリから起動させるためのスクリプトmkbootdevが追加されており、1GBのUSBフラッシュメモリを使用すればCD版のすべての機能を利用することができるようになっている。 また、公式対応以前にも、USBフラッシュメモリ起動の試みは、[USB-KNOPPIX](https://ja.wikipedia.org/wiki/USB-KNOPPIX "wikilink")など、各所でおこなわれていた。

そのほか[コンパクトフラッシュ](../Page/コンパクトフラッシュ.md "wikilink")からの起動や、サーバを用意して、ネットワークからのPXEブート、またHTTPポートを使用して必要なイメージをネットワークから取得して起動する方法も選択できるようになっている（HTTP-FUSE-KNOPPIX）。

## バージョン

[KNOPPIX_booting.png](https://ja.wikipedia.org/wiki/File:KNOPPIX_booting.png "fig:KNOPPIX_booting.png") [Knoppix.JPG](https://ja.wikipedia.org/wiki/File:Knoppix.JPG "fig:Knoppix.JPG") [Knoppix_7.2_640x480.png](https://ja.wikipedia.org/wiki/File:Knoppix_7.2_640x480.png "fig:Knoppix_7.2_640x480.png")|right\]\]

<table>
<caption>Knoppix 更新歴</caption>
<thead>
<tr class="header">
<th><p>Version</p></th>
<th><p>公開</p></th>
<th><p>CD</p></th>
<th><p>DVD</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.4</p></td>
<td><p>2000-09-30</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.6</p></td>
<td><p>2001-04-26</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2.1</p></td>
<td><p>2002-03-14</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2.2</p></td>
<td><p>2002-05-14</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.1</p></td>
<td><p>2002-10-01</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.2</p></td>
<td><p>2003-06-16</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.3</p></td>
<td><p>2003-09-22</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.4</p></td>
<td><p>2004-05-17</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.5 <a href="https://ja.wikipedia.org/wiki/LinuxTag" title="wikilink">LinuxTag</a>-Version</p></td>
<td><p>2004-06</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.6</p></td>
<td><p>2004-08-16</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.7</p></td>
<td><p>2004-12-09</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.8 <a href="../Page/CeBIT.md" title="wikilink">CeBIT</a>-Version</p></td>
<td><p>2005-02-28</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.8.1</p></td>
<td><p>2005-04-08</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.8.2[2]</p></td>
<td><p>2005-05-12</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.9</p></td>
<td><p>2005-06-01</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>4.0 LinuxTag-Version</p></td>
<td><p>2005-06-22</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4.0 updated</p></td>
<td><p>2005-08-16</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>4.0.2</p></td>
<td><p>2005-09-23</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5.0 CeBIT-Version</p></td>
<td><p>2006-02-25</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>5.0.1</p></td>
<td><p>2006-06-02</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5.1.0</p></td>
<td><p>2006-12-30</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>5.1.1</p></td>
<td><p>2007-01-04</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5.2 CeBIT-Version</p></td>
<td><p>2007-03</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>5.3 CeBIT-Version</p></td>
<td><p>2008-02-12</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5.3.1</p></td>
<td><p>2008-03-26</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ADRIANE</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>6.0.0</p></td>
<td><p>2009-01-28</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>6.0.1</p></td>
<td><p>2009-02-08</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>6.1 CeBIT-Version</p></td>
<td><p>2009-02-25</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>6.2 / ADRIANE 1.2</p></td>
<td><p>2009-11-18</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>6.2.1</p></td>
<td><p>2010-01-31</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>6.3 CeBIT-Version</p></td>
<td><p>2010-03-02</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>6.4.3</p></td>
<td><p>2010-12-20</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>6.4.4</p></td>
<td><p>2011-02-01</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>6.5 CeBIT-Version</p></td>
<td><p>2011-03</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>6.7.0</p></td>
<td><p>2011-08-03</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>6.7.1</p></td>
<td><p>2011-09-16</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>7.0.1</p></td>
<td><p>2012-05-24</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>7.0.2</p></td>
<td><p>2012-05-30</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>7.0.3</p></td>
<td><p>2012-07-01</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>7.0.4</p></td>
<td><p>2012-08-20</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>7.0.5</p></td>
<td><p>2012-12-21</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>7.2.0</p></td>
<td><p>2013-06-24</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>7.4.0</p></td>
<td><p>2014-08-07</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>7.4.1</p></td>
<td><p>2014-09-15</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>7.4.2</p></td>
<td><p>2014-09-28</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>7.5 CeBIT-Version</p></td>
<td><p>2015-03-16</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>7.6.0</p></td>
<td><p>2015-11-21</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>7.6.1</p></td>
<td><p>2016-01-16</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>7.7.0 CeBIT-Version</p></td>
<td><p>2016-03-14</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>7.7.1</p></td>
<td><p>2016-10-27</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>8.0.0 CeBIT-Version</p></td>
<td><p>2017-03-24</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>8.1.0</p></td>
<td><p>2017-09-27</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>8.2.0</p></td>
<td><p>2018-05-16</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>8.3.0 (DELUG-DVD)</p></td>
<td><p>2018-06-07</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>8.5.0 Linux-Magazin/ Linux-User Edition</p></td>
<td><p>2019-03-14</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>8.6.0</p></td>
<td><p>2019-08-08</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>8.6.1</p></td>
<td><p>2019-11-22</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>9.0</p></td>
<td><p>2020-03-05</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 日本語版

かつて日本国内では[独立行政法人](../Page/独立行政法人.md "wikilink")[産業技術総合研究所](../Page/産業技術総合研究所.md "wikilink")によって、日本語化をはじめとする日本の国情にあわせたローカライゼーションや、様々な機能を追加したものが本家とは別途に開発、配布されていたが、現在ではそのプロジェクトは解散している。

なお2020年現在の時点で、本家のKNOPPIXには日本語のロケールも追加されているので日本語での利用も一応可能になっているが、初期状態ではドイツ語版か英語版であることや、日本語入力用IMEなどの積極的なサポートが無いことなどにより追加設定の手間が必要である。

### 産業技術総合研究所版の独自機能

日本語版ではInstall2WinというWindowsパソコンにKNOPPIXをインストールして[マルチブート](../Page/マルチブート.md "wikilink")環境を構築することによってハードディスクからKNOPPIXが起動できるようにする機能が搭載されている。ただしこの機能は、上述の[インストール機能よりインストールされるOSの操作は](https://ja.wikipedia.org/wiki/#CD/DVD以外からの起動 "wikilink")、LiveCDのOSに近い。だが、上述の機能ではKNOPPIXではなく、Debianがインストールされる。

また、日本語版では[教育ソフト](https://ja.wikipedia.org/wiki/教育ソフト "wikilink")を収録した、KNOPPIX Eduや[KNOPPIX/Mathが開発されている](https://ja.wikipedia.org/wiki/MathLibre "wikilink")（注：2020年の時点でKNOPPIX/MATHの開発は終了して[MathLibre](https://ja.wikipedia.org/wiki/MathLibre "wikilink")へと移行している）。

バージョン6から[LCAT](https://ja.wikipedia.org/wiki/LCAT "wikilink")(Live CD Acceleration Tool kit)と呼ばれる機能が追加された。 これは、[Live CDから起動する際に読み込まれるデータの配置を最適化することによりCDのピックアップの移動を抑えて起動時間を短縮する機能であるが](../Page/Live_CD.md "wikilink")、機能単体のプロジェクトも存在する\[3\]。 産業技術総合研究所による日本語版の開発、並びに頒布は既に終了しており、7.0.2が最終版となっている。プロジェクトの閉鎖に伴い2015年4月に公式サイトは閉鎖された\[4\]。

## 派生版

[KnoppixFamilyTree1210.svg](https://ja.wikipedia.org/wiki/File:KnoppixFamilyTree1210.svg "fig:KnoppixFamilyTree1210.svg") [KNOPPIXの派生品一覧に掲載](https://ja.wikipedia.org/wiki/:en:List_of_Linux_distributions#Knoppix-based "wikilink")。

| 配布版                                                        | 説明                                                                                                                |
| ---------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| [Damn Small Linux](../Page/Damn_Small_Linux.md "wikilink") | 名刺大の[CDやUSB](../Page/コンパクトディスク.md "wikilink") pendrive向けの軽量なKNOPPIX[Live CD](../Page/Live_CD.md "wikilink")。開発停止。 |

### その他の派生版

※すべて[侵入テスト用かつ開発停止](https://ja.wikipedia.org/wiki/ペネトレーションテスト "wikilink")。

  - Whoppix - ver.2系まで。BackTrackの前身。
  - Auditor Security Collection - BackTrackの前身。
  - [BackTrack](https://ja.wikipedia.org/wiki/BackTrack "wikilink") - ver.3まで

### 日本発の派生版

*[日本のLinux開発](https://ja.wikipedia.org/wiki/日本のLinux開発 "wikilink")も参照。*

  - Xenoppix - KNOPPIXに[Xenを搭載したディストリビューション](../Page/Xen_\(仮想化ソフトウェア\).md "wikilink")。
  - [Regret](https://ja.wikipedia.org/wiki/Regret_\(Linuxディストリビューション\) "wikilink") - KNOPPIX派生のディストリビューション。

## 脚注

## 外部リンク

  -
  -

  - [MathLibre Project の公式ウェブサイト](http://www.mathlibre.org/index-ja.html) ※ KNOPPIX/MATH の後継プロジェクト

## 関連項目

  - [Linuxディストリビューションの比較](../Page/Linuxディストリビューションの比較.md "wikilink")
  - [Linuxライブディストリビューションの比較](../Page/Linuxライブディストリビューションの比較.md "wikilink")
  - [1CD Linux](https://ja.wikipedia.org/wiki/1CD_Linux "wikilink")
  - [Puppy Linux](../Page/Puppy_Linux.md "wikilink")

[Category:Debian派生ディストリビューション](https://ja.wikipedia.org/wiki/Category:Debian派生ディストリビューション "wikilink") [Category:LiveCD](https://ja.wikipedia.org/wiki/Category:LiveCD "wikilink")

1.  日本語版を配布していた産業技術総合研究所による表記。
2.  [Introduction to Knoppix | PCMag.com](https://www.pcmag.com/article2/0,2817,1819549,00.asp)
3.  [LCAT(Live CD Acceleration Tool kit)](https://osdn.jp/projects/lcat/)
4.  [KNOPPIX 日本語版](http://www.risec.aist.go.jp/project/knoppix/)(リンク切れ)