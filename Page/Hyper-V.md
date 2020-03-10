> この記事は[Hyper-V](https://ja.wikipedia.org/wiki/Hyper-V)から翻訳されています。


**Hyper-V**（ハイパーV、はいぱーぶい）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が提供する[ハイパーバイザ](../Page/ハイパーバイザ.md "wikilink")ベースの[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")向け[仮想化](../Page/仮想化.md "wikilink")システムで、1台の[コンピュータ](../Page/コンピュータ.md "wikilink")（[サーバ](../Page/サーバ.md "wikilink")）で複数の[仮想機械](../Page/仮想機械.md "wikilink")を実現する。

開発当初は **Windows Server Virtualization**、又は[コードネーム](../Page/コードネーム.md "wikilink")である **Viridian** の名称が用いられた\[1\]\[2\]。

## 概要

[Virtual Server](../Page/Microsoft_Virtual_Server.md "wikilink") を置き換える形で、当初の Hyper-V は [Windows Server 2008](../Page/Microsoft_Windows_Server_2008.md "wikilink") の x64 エディションの1機能としてベータ版が出荷され、Windows Update 等を通して正式版が[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[6月26日](../Page/6月26日.md "wikilink")に公開された\[3\]。その後も Hyper-V は [Windows Server](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") 等の一機能として提供され続け、[Windows Server 2008 R2](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2008_R2 "wikilink") には Hyper-V 2.0 が、[Windows Server 2012](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2012 "wikilink") には Hyper-V 3.0 が搭載されている。

当初、Hyper-V 機能はクライアントOSに搭載されなかったが、[Windows 8 Pro、およびWindows 8 Enterprise](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink") 以降では [Windows Virtual PC](https://ja.wikipedia.org/wiki/Windows_Virtual_PC "wikilink") に代わって Hyper-V 機能が搭載された（基本的にx64版専用だがx86版はリモート管理ツールのHyper-V マネージャーのみ対応となる）。これらは従前のサーバー向けと区別して「クライアント Hyper-V」と呼称される\[4\]\[5\]。

Hyper-V の管理や設定変更には、Hyper-V 機能を有効にした Windows Server に直接ログオンして行う方法と、リモートで行う方法がある。リモート管理するには Windows Server、もしくはHyper-Vリモート管理ツールがインストールされたクライアントOS（[Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、および[Windows 7](../Page/Microsoft_Windows_7.md "wikilink")）、またはx64版・x86版を問わずHyper-V マネージャーを有効にしたPro以上のエディションのWindows 8/8.1、およびWindows 10が必要になる。また、Core サーバの MMC ポインティングのリダイレクトによる[リモートデスクトップ](https://ja.wikipedia.org/wiki/リモートデスクトップ "wikilink")もしくはリモートサーバを用いることができる。

### 無償版の扱い

Hyper-V の無償版として **Hyper-V Server** が存在する。これは、Hyper-V 機能のみを利用できるように大半の機能が制限された、Server Core をベースとした [Windows Server](../Page/Windows_Server.md "wikilink") である\[6\]。

無償で提供されている Hyper-V Server は[コマンドラインインタフェース (CLI)](../Page/キャラクタユーザインタフェース.md "wikilink") に限定されている。Hyper-V 機能を実行・管理する[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") の設定は、ログオン後に起動する[シェル](../Page/シェル.md "wikilink")の[コマンドを用いる](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")。Hyper-V Server 2008 からはテキストベースの[メニューが用意されているため](https://ja.wikipedia.org/wiki/メニュー_\(コンピュータ\) "wikilink")、初期設定が行いやすくなっている。

最初の Hyper-V Server は、[Windows Server 2008](../Page/Microsoft_Windows_Server_2008.md "wikilink") のラインナップの1つとして、「Windows Server 2008 Hyper-V」の名称で2008年[8月1日](../Page/8月1日.md "wikilink")にリリースされた。その後、マイクロソフトは Windows Server 2008 R2のリリースに合わせて「Microsoft Hyper-V Server 2008 R2」を、Windows Server 2012 のリリースに合わせて「Microsoft Hyper-V Server 2012」をリリースしている。

## アーキテクチャ

[275px](https://ja.wikipedia.org/wiki/ファイル:Viridian_Architecture.svg "wikilink") Hyper-Vは[パーティション](https://ja.wikipedia.org/wiki/パーティション "wikilink")による隔離をサポートする。パーティションは隔離を実現するための論理ユニットで、OSのハイパーバイザーによりサポートされる。ハイパーバイザーの[インスタンス](../Page/インスタンス.md "wikilink")は少なくとも1個のWindows Server 2008が動作する親パーティションを持つ。仮想化スタックは親パーティションの中で動作し、[ハードウェア](../Page/ハードウェア.md "wikilink")へ直にアクセスする。親パーティションはゲストOSを動作させる子パーティションを生成する。親パーティションは子パーティションをhypercall APIを用いて作成する。hypercall APIはHyper-Vを操作する[APIである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

仮想化パーティションは物理プロセッサへのアクセスを持たず、[割り込みをハンドルすることもない](../Page/割り込み_\(コンピュータ\).md "wikilink")。そのかわり、プロセッサの仮想的なビューを持ち、ゲストの仮想アドレスで動作するということである。（ハイパーバイザーの設定に依存するが）丸ごとの仮想アドレス空間を必要としない。ハイパーバイザーはそれぞれのパーティションへ、プロセッサのサブセットを選択的に公開することができる。ハイパーバイザーはプロセッサの割り込みをハンドルし、論理同期割り込みコントローラ (SynIC) を使ってそれぞれのパーティションにリダイレクトする。Hyper-Vはゲスト側の仮想アドレス空間からのアドレス変換をIOMMU (I/O Memory Management Unit) を用いてハードウェアアクセラレーションできる。IOMMUは[CPU](../Page/CPU.md "wikilink")により使われるメモリ管理ハードウェアから独立して操作する。

子パーティションはハードウェアリソースを直アクセスしない。そのかわり、仮想デバイスという概念でリソースの仮想的なビューを持つ。仮想デバイスに要求すると、VMBusを経由して親パーティションのデバイスにリダイレクトされる。リクエストはそこで管理される。VMBusはパーティション間の通信を可能にする論理的なチャンネルである。レスポンスも同様にVMBusを経由してリダイレクトされる。もし親パーティションのデバイスが仮想デバイスでもあるなら、親パーティションやより遠くに、物理デバイスへのアクセスできるところまでリダイレクトされる。親パーティションは仮想化サービスプロバイダ (Virtualization Service Provider) を実行する。それはVMBusを接続し、子パーティションからのデバイスのアクセス要求をハンドルする。子パーティションの仮想デバイスは内部で仮想サービスクライアント (Virtualization Service Client) を実行する。それはVMBusを経由して親パーティションのVSPへリクエストをリダイレクトする。この全体のプロセスはゲストOSに透過的である。

仮想デバイスはEnlightened I/Oと名づけられたWindows Server Virtualizationの特徴をうまく利用することができる。Enlightened I/Oはストレージ、ネットワーク、グラフィックの各サブシステムやそれ以外をサポートする。Enlightened I/OはVMBusをダイレクトに利用できるSCSIに似た高レベル通信プロトコルを用いた仮想化向けの実装に特化しており、デバイスのエミュレーション層をバイパスすることができる。それにより、Hyper-V下のゲストOSは他の[エミュレーションされたハードウェアを用いたOSに比べより高速に動作する](../Page/エミュレータ.md "wikilink")。これにより通信はより効率的になるが、ゲストOSもEnlightened I/Oをサポートする必要がある。当初はWindows Server 2008、Windows Vista、[SUSE Linux Enterprise Serverのみが標準でEnlightened](https://ja.wikipedia.org/wiki/SUSE_Linux_Enterprise_Server "wikilink") I/Oをサポートしていたが、後からLinux用のドライバがGPLで公開されるようになった\[7\]\[8\]。

## バージョンと搭載製品

<table>
<thead>
<tr class="header">
<th><p>環境バージョン</p></th>
<th><p>汎用OS版</p></th>
<th><p>専用無償OS版</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.0</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Windows_Server_2008" title="wikilink">Windows Server 2008</a> 64ビット版</p></td>
<td><p>Hyper-V Server 2008</p></td>
<td><p>OS本体発売（2008年<a href="../Page/2月27日.md" title="wikilink">2月27日</a>）に遅れて同年6月26日リリース。</p></td>
</tr>
<tr class="even">
<td><p>2.0</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Windows_Server_2008_R2" title="wikilink">Windows Server 2008 R2</a></p></td>
<td><p>Hyper-V Server 2008 R2</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.0</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Windows_Server_2008_R2" title="wikilink">Windows Server 2008 R2 SP1</a></p></td>
<td><p>Hyper-V Server 2008 R2 SP1</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>4.0</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2012" title="wikilink">Windows Server 2012</a>,<br />
<a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_8" title="wikilink">Windows 8 Pro</a>(x64),<br />
<a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_8" title="wikilink">Windows 8 Enterprise</a>(x64)</p></td>
<td><p>Hyper-V Server 2012</p></td>
<td><p>このバージョンより新たにVHDXが導入される。</p></td>
</tr>
<tr class="odd">
<td><p>5.0</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2012" title="wikilink">Windows Server 2012 R2</a>,<br />
<a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_8#Windows_8.1" title="wikilink">Windows 8.1 Pro</a>(x64),<br />
<a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_8#Windows_8.1" title="wikilink">Windows 8.1 Enterprise</a>(x64)</p></td>
<td><p>Hyper-V Server 2012 R2</p></td>
<td><p>このバージョンより新たにコピー&amp;ペースト、オーディオ再生/録音、USBデバイスの各サポート（ただしゲストOSがWindows 8.1 Pro/Enterprise(各x64/x86)、およびWindows 10 Pro/Education/Enterprise(各x64/x86)、Windows Server 2012 R2、Windows Server 2016の場合のみ）など、ホスト - ゲスト間の連携機能「拡張セッションモード」に対応しており、Windows 7の上位エディション（Professional、およびEnterprise、Ultimate）に搭載されていた<a href="https://ja.wikipedia.org/wiki/Microsoft_Virtual_PC" title="wikilink">Virtual PCの機能とほぼ同等になり</a>、使い勝手が向上している[9]。<br />
エミュレートデバイスを全廃した第二世代仮想マシンの導入。</p></td>
</tr>
<tr class="even">
<td><p>6.2</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_10" title="wikilink">Windows 10 Pro</a>(x64),<br />
<a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_10" title="wikilink">Windows 10 Education</a>(x64),<br />
<a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_10" title="wikilink">Windows 10 Enterprise</a>(x64)</p></td>
<td></td>
<td><p>従来のHyper-Vで管理する仮想マシンの構成ファイルはXML形式などで記述されていたが、Windows 10/Windows Server 2016/Hyper-V Server 2016に搭載されるHyper-Vでは新しくバイナリ形式になり、アクセス速度や耐障害性などが向上している。Windows 10/Windows Server 2016/Hyper-V Server 2016専用のHyper-Vは従来のバージョンでも扱えるがバージョン6に変換するとWindows 10専用となり従来のHyper-Vでは管理不可能となり当然、バージョン5に書き戻すことも不可能となる[10]。<br />
動的なNICやメモリサイズの変更、および統合ソフトウエアのWindows Updateによる自動更新、Linuxでのセキュアブートなどのサポートに対応。</p></td>
</tr>
<tr class="odd">
<td><p>7.0以降</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2016" title="wikilink">Windows Server 2016</a><br />
<a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_10" title="wikilink">Windows 10 Pro（Ver. 1511以降）</a>(x64),<br />
<a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_10" title="wikilink">Windows 10 Education（Ver. 1511以降）</a>(x64),<br />
<a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_10" title="wikilink">Windows 10 Pro Education</a>(x64)<br />
<a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_10" title="wikilink">Windows 10 Enterprise（Ver. 1511以降）</a>(x64)</p></td>
<td><p>Hyper-V Server 2016</p></td>
<td><p>このバージョンより仮想マシン上で仮想マシンが動く「<strong>Nested Hyper-V</strong>」が搭載される[11]。</p></td>
</tr>
</tbody>
</table>

## システム要件

1.  Windows Server 2008 Standard/Enterprise/Datacenter x64版が動作する64ビットのCPU
2.  ハードウェア支援付きの仮想化。仮想化オプションを含んだCPUで利用できる。とりわけ[Intel VTや](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink")[AMD-V](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink")（SLAT(EPT)機能必須）
3.  [NXビット](https://ja.wikipedia.org/wiki/NXビット "wikilink")互換のCPUが利用可能でハードウェアData Execution Prevention (DEP) が有効になっていなければならない。
4.  最低2GBのメインメモリ（各々の仮想OSは自身のメモリを必要とする。そして現実的にはそれ以上必要になる）
5.  Windows 2008 Standard (64 Bit) Hyper-V Coreはおよそ3GB以上のディスク空き容量（インストール容量）
6.  Windows 2008 Standard (64 Bit) Hyper-V full GUI productはおよそ8GB以上のディスク空き容量（インストール容量）

スタンドアロン版のHyper-VサーバーはWindows Server 2008のインストールの必要は無く、最小メモリは1GBでディスク必要容量は2GBである。

<table>
<caption>Hyper-V Server (専用無償版OS) のシステム要件</caption>
<thead>
<tr class="header">
<th></th>
<th><p>2008[12]</p></th>
<th><p>2008R2[13][14]</p></th>
<th><p>2012[15][16]</p></th>
<th><p>2016</p></th>
<th><p>2019</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>プロセッサ</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/x64" title="wikilink">x64</a>アーキテクチャ互換であり<br />
<a href="../Page/インテル_バーチャライゼーション・テクノロジー.md" title="wikilink">Intel-VTまたは</a><a href="https://ja.wikipedia.org/wiki/AMD-V" title="wikilink">AMD-V</a>有効かつ<br />
<a href="https://ja.wikipedia.org/wiki/データ実行防止" title="wikilink">ハードウェア Data Execution Prevention</a> (DEP) 有効かつ<br />
Second Level Address Translation（SLAT）が必須</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>最低1.0GHz（推奨2.0GHz以上）<br />
最大4基24論理プロセッサ</p></td>
<td><p>最低1.4GHz（推奨2.0GHz以上）<br />
最大8基64論理プロセッサ</p></td>
<td><p>最低1.4GHz<br />
最大320論理プロセッサ</p></td>
<td><p>最低1.4Ghz</p></td>
<td><p>最低1.4Ghz</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ホストOS用メモリ</p></td>
<td><p>最低1.0GB（推奨2.0GB以上）</p></td>
<td><p>最低1.0GB（推奨2.0GB以上）</p></td>
<td><p>最低512MB[17]</p></td>
<td><p>最低512MB</p></td>
<td><p>最低512MB</p></td>
</tr>
<tr class="even">
<td><p>全体メモリ</p></td>
<td><p>最大32GB</p></td>
<td><p>最大1TB</p></td>
<td><p>最大4TB</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ホストOS用ストレージ</p></td>
<td><p>最低3.25GB＋ページファイル分</p></td>
<td><p>最低8GB（推奨20GB以上）</p></td>
<td></td>
<td></td>
<td><p>最小32 GB（ATA、PATA、IDE、EIDEは利用不可）</p></td>
</tr>
<tr class="even">
<td><p>光学ドライブ</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/DVD-ROM" title="wikilink">DVD-ROM</a>ドライブ</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ネットワークアダプタ</p></td>
<td></td>
<td><p>最低1つ（推奨2つ以上）</p></td>
<td></td>
<td><p>ギガビット以上の処理能力があるイーサネット アダプター</p>
<p>PCI Express アーキテクチャの仕様への準拠</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>ディスプレイ</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/SVGA" title="wikilink">SVGA</a>以上の解像度</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>他</p></td>
<td></td>
<td><p>キーボード及びポインティングデバイス</p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## システム仕様

Windows 2008 Standard (64 Bit) Hyper-V full GUI or Coreは

1.  31GBまでのメモリを仮想ホストに割り当てることができる。付け加えて1GBをHyper-V 親OSが必要とする[2](http://msdn.microsoft.com/en-us/library/aa366778.aspx#physical_memory_limits_windows_server_2008)。
2.  4プロセッサまでサポートする（1プロセッサにつき1/2/4コア）
3.  128個のゲストOSをサポートする[3](http://www.microsoft.com/servers/hyper-v-server/overview.mspx)。
4.  32ビット (x86) および64ビット (x64) のゲストOSをサポートする。

## エミュレーション環境

全てのクライアントHyper-V、およびHyper-V Serverは同一環境である。

  - [Intel 82443BX](https://ja.wikipedia.org/wiki/Intel_440BX "wikilink") チップセット

## サポートされるゲストOS

<table>
<caption>公式にサポートされているゲストOS</caption>
<thead>
<tr class="header">
<th></th>
<th><p>(参考)<br />
VS2005<br />
SP1[18][19][20]</p></th>
<th><p>1.0[21][22]</p></th>
<th><p>2.0 / 3.0[23][24][25][26][27]</p></th>
<th><p>4.0[28][29][30][31][32]</p></th>
<th><p>5.0[33][34][35][36][37]</p></th>
<th><p>6.0以降[38][39][40][41]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Windows Server 2016</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="even">
<td><p>Windows Server 2012 R2</p></td>
<td></td>
<td></td>
<td></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="odd">
<td><p>Windows Server 2012</p></td>
<td></td>
<td></td>
<td></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="even">
<td><p>Windows Home Server 2011</p></td>
<td></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="odd">
<td><p>Windows Multipoint Server 2011</p></td>
<td></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="even">
<td><p>Windows Small Business Server 2011</p></td>
<td></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="odd">
<td><p>Windows Server 2008 R2</p></td>
<td></td>
<td><p>○SP1</p></td>
<td><p>○SP1</p></td>
<td><p>○SP1</p></td>
<td><p>○SP1</p></td>
<td><p>○SP1</p></td>
</tr>
<tr class="even">
<td><p>Windows Server 2008</p></td>
<td></td>
<td><p>○SP2</p></td>
<td><p>○SP2</p></td>
<td><p>○SP2</p></td>
<td><p>○SP2</p></td>
<td><p>○SP2</p></td>
</tr>
<tr class="odd">
<td><p>Windows Server 2003 R2</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○SP2</p></td>
<td><p>○SP2</p></td>
<td><p>○SP2</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Windows Server 2003</p></td>
<td><p>○</p></td>
<td><p>○SP2</p></td>
<td><p>○SP2</p></td>
<td><p>○SP2</p></td>
<td><p>○SP2</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Windows 2000 Server (Server, Advanced Server)</p></td>
<td><p>○</p></td>
<td><p>○SP4</p></td>
<td><p>○SP4</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Windows NT Server 4</p></td>
<td><p>○SP6a</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Windows 10 (Home、およびSを除く全エディション（x86,x64）)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="even">
<td><p>Windows 8.1 (Enterprise,Pro（x86,x64）)</p></td>
<td></td>
<td></td>
<td></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="odd">
<td><p>Windows 8 (Enterprise,Pro（x86,x64）)</p></td>
<td></td>
<td></td>
<td></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="even">
<td><p>Windows 7 (Enterprise,Ultimate,Professional（x86,x64）)</p></td>
<td></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="odd">
<td><p>Windows Vista (Enterprise,Ultimate,business（x86,x64）)</p></td>
<td></td>
<td><p>○SP1</p></td>
<td><p>○SP2</p></td>
<td><p>○SP2</p></td>
<td><p>○SP2</p></td>
<td><p>○SP2</p></td>
</tr>
<tr class="even">
<td><p>Windows XP (Professional（x86）)</p></td>
<td><p>○SP2</p></td>
<td><p>○SP2</p></td>
<td><p>○SP2</p></td>
<td><p>○SP2</p></td>
<td><p>○SP3</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>CentOS 7</p></td>
<td></td>
<td></td>
<td><p>○7.0-7.2</p></td>
<td><p>○7.0-7.2</p></td>
<td><p>○7.0-7.2</p></td>
<td><p>○7.0-7.2</p></td>
</tr>
<tr class="even">
<td><p>CentOS 6</p></td>
<td></td>
<td></td>
<td><p>○6.0-6.7</p></td>
<td><p>○6.0-6.7</p></td>
<td><p>○6.0-6.7</p></td>
<td><p>○6.0-6.7</p></td>
</tr>
<tr class="odd">
<td><p>CentOS 5</p></td>
<td></td>
<td></td>
<td><p>○5.5-5.11</p></td>
<td><p>○5.5-5.11</p></td>
<td><p>○5.5-5.11</p></td>
<td><p>○5.5-5.11</p></td>
</tr>
<tr class="even">
<td><p>Red Hat Enterprise Linux 7</p></td>
<td></td>
<td></td>
<td><p>○7.0-7.2</p></td>
<td><p>○7.0-7.2</p></td>
<td><p>○7.0-7.2</p></td>
<td><p>○7.0-7.2</p></td>
</tr>
<tr class="odd">
<td><p>Red Hat Enterprise Linux 6</p></td>
<td></td>
<td></td>
<td><p>○6.0-6.7</p></td>
<td><p>○6.0-6.7</p></td>
<td><p>○6.0-6.7</p></td>
<td><p>○6.0-6.7</p></td>
</tr>
<tr class="even">
<td><p>Red Hat Enterprise Linux 5</p></td>
<td><p>○5.0</p></td>
<td></td>
<td><p>○5.5-5.11</p></td>
<td><p>○5.5-5.11</p></td>
<td><p>○5.5-5.11</p></td>
<td><p>○5.5-5.11</p></td>
</tr>
<tr class="odd">
<td><p>Red Hat Enterprise Linux 4</p></td>
<td><p>○4.0</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Red Hat Enterprise Linux 3</p></td>
<td><p>○3.0</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Red Hat Enterprise Linux 2</p></td>
<td><p>○2.1</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Red Hat Linux 9</p></td>
<td><p>○9.0</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Debian 8</p></td>
<td></td>
<td></td>
<td><p>○8.0-8.2</p></td>
<td><p>○8.0-8.2</p></td>
<td><p>○8.0-8.2</p></td>
<td><p>○8.0-8.2</p></td>
</tr>
<tr class="even">
<td><p>Debian 7</p></td>
<td></td>
<td></td>
<td><p>○7.0-7.9</p></td>
<td><p>○7.0-7.9</p></td>
<td><p>○7.0-7.9</p></td>
<td><p>○7.0-7.9</p></td>
</tr>
<tr class="odd">
<td><p>SUSE Linux Enterprise Server 12</p></td>
<td></td>
<td></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="even">
<td><p>SUSE Linux Enterprise Server 11</p></td>
<td></td>
<td></td>
<td><p>○SP2-SP4</p></td>
<td><p>○SP2-SP4</p></td>
<td><p>○SP2-SP4</p></td>
<td><p>○</p></td>
</tr>
<tr class="odd">
<td><p>SUSE Linux Enterprise Server 10</p></td>
<td></td>
<td><p>○SP1</p></td>
<td><p>○SP4</p></td>
<td><p>○SP4</p></td>
<td><p>○</p></td>
<td><p>○</p></td>
</tr>
<tr class="even">
<td><p>SUSE Linux Enterprise Server 9</p></td>
<td><p>○</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>SUSE Linux 10</p></td>
<td><p>○10.0-10.2</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>SUSE Linux 9</p></td>
<td><p>○9.3</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Ubuntu 15</p></td>
<td></td>
<td></td>
<td><p>○15.4,15.10</p></td>
<td><p>○15.4,15.10</p></td>
<td><p>○15.4,15.10</p></td>
<td><p>○15.4,15.10</p></td>
</tr>
<tr class="even">
<td><p>Ubuntu 14</p></td>
<td></td>
<td></td>
<td><p>○14.04</p></td>
<td><p>○14.04</p></td>
<td><p>○14.04</p></td>
<td><p>○14.04</p></td>
</tr>
<tr class="odd">
<td><p>Ubuntu 12</p></td>
<td></td>
<td></td>
<td><p>○12.04</p></td>
<td><p>○12.04</p></td>
<td><p>○12.04</p></td>
<td><p>○12.04</p></td>
</tr>
<tr class="even">
<td><p>FreeBSD 10</p></td>
<td></td>
<td></td>
<td><p>○10-10.2</p></td>
<td><p>○10-10.2</p></td>
<td><p>○10-10.2</p></td>
<td><p>○10-10.2</p></td>
</tr>
<tr class="odd">
<td><p>FreeBSD 9</p></td>
<td></td>
<td></td>
<td><p>○9.1-9.3</p></td>
<td><p>○9.1-9.3</p></td>
<td><p>○9.1-9.3</p></td>
<td><p>○9.1-9.3</p></td>
</tr>
<tr class="even">
<td><p>FreeBSD 8</p></td>
<td></td>
<td></td>
<td><p>○8.4</p></td>
<td><p>○8.4</p></td>
<td><p>○8.4</p></td>
<td><p>○8.4</p></td>
</tr>
</tbody>
</table>

Windows Server 2008ゲストおよびWindows HPC Server 2008、Windows 7は1-、2-、4-wayの [SMPに設定することが可能で](../Page/対称型マルチプロセッシング.md "wikilink"), Windows Server 2003およびWindows Vistaでは1-、2-wayのSMP、[SUSE Linux](https://ja.wikipedia.org/wiki/SUSE_Linux "wikilink") を除くその他のゲストOSは1-wayのみである \[42\]。他のゲストOS、例えば[Ubuntu Linux](https://ja.wikipedia.org/wiki/Ubuntu_Linux "wikilink") 6.06/6.10/7.10 あるいは [Fedora](../Page/Fedora.md "wikilink") 8/9 などはサポートされないが、これらが動作したという報告が上げられている \[43\]\[44\]\[45\]。

[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")製の[デスクトップ仮想化](https://ja.wikipedia.org/wiki/デスクトップ仮想化 "wikilink") (VDI) 製品が使用可能である。[Citrix](../Page/シトリックス・システムズ.md "wikilink") XenDesktopおよび [Ericom](https://ja.wikipedia.org/wiki/Ericom "wikilink") PowerTerm WebConnectはデータセンターに設置されたデスクトップ仮想マシンをホストし集中管理する能力を提供する。デスクトップ仮想マシンはユーザーにフルスペックのPCデスクトップ環境を提供する。

*Enlightened I/O*付きのゲストOSおよびハイパーバイザーに対応したカーネル、例えばWindows Server 2008、Windows Vista SP1、およびCitrix XenServerや SISE から計画されているものなどは、ホストのリソースをよりよく利用できるだろう。ホストのリソースはVSCドライバーによってこれらのゲストOSからVSPにVMバスを通して直接通信される \[46\]。Non-enlightenedなOSはエミュレートされたI/Oで動作する \[47\]。 しかしながら、*integration components*（VSCドライバーを含む）はWindows Server 2003 SP2、Windows XP SP3、Windows Vista SP1、Linuxから利用でき、より高いパフォーマンスを獲得できる。

[Xenを有効にしたLinuxゲストはHyper](https://ja.wikipedia.org/wiki/Xen_\(仮想化ソフトウェア\) "wikilink")-Vによって[準仮想化](../Page/準仮想化.md "wikilink")が可能である。現在、[SUSE Linux Enterprise Server](https://ja.wikipedia.org/wiki/SUSE_Linux_Enterprise_Server "wikilink") 10,11,12 x86およびx64 Editionがこの方法においてマイクロソフトから公式にサポートされている\[48\]が、Xenを有効にしたLinuxはSUSE Linuxに限らず動作すると考えられる。2008年2月、[レッドハット](../Page/レッドハット.md "wikilink")とマイクロソフトは、それぞれのOSにおけるハイパーバイザー相互運用性についての仮想化の契約にサインした。これによって[Red Hat Enterprise Linux](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux "wikilink") 5は公式にHyper-Vでサポートされる \[49\]。

## VHD ファイルの Virtual Server 2005 と Virtual PC 2004/2007 との互換性

Hyper-Vを始めとして[Virtual Server](../Page/Microsoft_Virtual_Server.md "wikilink") 2005、[Virtual PC](https://ja.wikipedia.org/wiki/Microsoft_Virtual_PC "wikilink") 2004/2007等の製品はゲストOSを1つの[VHDファイルに保存することができる](https://ja.wikipedia.org/wiki/VHD_\(ファイルフォーマット\) "wikilink")。このファイルはゲストOS全体を格納しているものの、他のファイルによって「アンドゥ情報」などを構成することもできる。

Virtual Server 2005、Virtual PC 2004/2007による古い VHDファイルは Windows 2008 Hyper-V Serverでコピーし、使用することができる。しかし、古い『Virtual PC 統合コンポーネント』は移転の際に取り除く必要がある。移転したゲストOSはHyper-Vを使って構成し、開始された後、仮想ハードウェアの変更が検出されるだろう。『 Hyper-V 統合サービス( 又は Integration Services ) 』（Virtual PC 統合コンポーネントに類似した機能）をインストールすることで5つのサービスの形でパフォーマンスを向上させる。ゲストOSのビデオ表示およびネットワークカードの新しいドライバも共にインストールされる。結果として最近のバージョンのWindowsでは再[アクティベーション](https://ja.wikipedia.org/wiki/アクティベーション "wikilink")、およびプロダクトキーの再発行が必要となる。

## 参照

## 関連項目

  - [仮想化](../Page/仮想化.md "wikilink")
  - [Microsoft Windows Server 2008](../Page/Microsoft_Windows_Server_2008.md "wikilink")
  - [Microsoft Windows Server 2008 R2](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2008_R2 "wikilink")
  - [Microsoft Windows Server 2012](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2012 "wikilink")
  - [Microsoft Windows Server 2016](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2016 "wikilink")
  - [Microsoft Windows Server 2019](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2019 "wikilink")
  - [Microsoft Virtual Server](../Page/Microsoft_Virtual_Server.md "wikilink")
  - [Microsoft Virtual PC](https://ja.wikipedia.org/wiki/Microsoft_Virtual_PC "wikilink")

## 書籍

  -
## 外部リンク

  - [Hyper-V 仮想化 マイクロソフト公式技術情報](http://technet.microsoft.com/ja-jp/virtualization/default.aspx)
  - [Microsoft Hyper-V Server 2008](http://www.microsoft.com/japan/servers/hyper-v-server/)
  - [Hyper-V Functional Specification](http://www.microsoft.com/downloads/details.aspx?FamilyID=91e2e518-c62c-4ff2-8e50-3a37ea4100f5&displaylang=en)
  - [WinHEC 2006 Presentation Slides](http://blogs.technet.com/virtualization/archive/2006/06/14/WinHEC-2006-Slides.aspx)
  - [Core Scenarios and Key features of Hyper-V](http://www.microsoft.com/windowsserver2008/en/us/virtualization-consolidation.aspx)
  - [Windows Virtualization team blog](http://blogs.technet.com/virtualization/)
  - [Microsoft Virtualization](http://www.microsoft.com/japan/virtualization/default.mspx) Microsoft
  - [Windows Server 2008 Hyper-V FAQ](http://www.microsoft.com/japan/servers/hyper-v-server/faq.mspx)
  - [Dutch Windows Virtualization and Hyper-V team blog](http://hyper-v.nu/blogs/)
  - [Virtualization and Security: What does it mean for me? - Microsoft TechNet Video](http://www.microsoft.com/emea/spotlight/sessionh.aspx?videoid=991)

[Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.  [山市良の「企業ユーザーはここに注目しよう！Windows 8.1の新機能」 ― 第1回 コピー＆ペースト、オーディオ再生／録音、USBデバイスなどホスト－ゲスト間の連携 Windows 8.1で「クライアントHyper-V」はこう改善された](http://ascii.jp/elem/000/000/821/821822/) - ASCII.jp（[KADOKAWA](https://ja.wikipedia.org/wiki/KADOKAWA "wikilink")） 2013年9月6日。
10.
11.
12. <http://www.computerworld.jp/topics/560/157149>
13. <http://www.microsoft.com/ja-jp/download/details.aspx?id=3512>
14. <http://technet.microsoft.com/en-us/library/ee815295.aspx>
15. [1](http://technet.microsoft.com/en-us/library/jj647784)
16. <http://jp.fujitsu.com/platform/server/primergy/software/windows/os/wins2012/hv/>
17. フットプリントを小さくしたため、必須物理メモリ量が前バージョンより少ない
18. <http://technet.microsoft.com/ja-jp/windowsserver/gg675975>
19. <http://technet.microsoft.com/ja-jp/windowsserver/gg605270>
20. <http://support.microsoft.com/kb/867572/en>
21. Windows Server 2008 の Hyper-V インストール手順書 (MS-WORD) - Microsoft
22. <http://technet.microsoft.com/ja-jp/library/cc794868.aspx>
23.
24. <https://technet.microsoft.com/en-us/library/dn531026.aspx>
25. <https://technet.microsoft.com/en-us/library/dn531027.aspx>
26. <https://technet.microsoft.com/en-us/library/dn614985.aspx>
27. <https://technet.microsoft.com/en-us/library/dn531029.aspx>
28.
29.
30.
31.
32. <https://technet.microsoft.com/ja-jp/library/dn792028.aspx>
33.
34.
35.
36.
37. <https://technet.microsoft.com/ja-jp/library/dn792027.aspx>
38.
39.
40.
41. <https://msdn.microsoft.com/virtualization/hyperv_on_windows/about/supported_guest_os>
42. [Supported Guest OS on Windows Server 2008 Hyper-V](http://www.microsoft.com/windowsserver2008/en/us/hyperv-supported-guest-os.aspx)
43. [Installing Fedora Core 8 on Hyper-V](http://blogs.msdn.com/virtual_pc_guy/archive/2007/12/31/installing-fedora-core-8-on-hyper-v.aspx)
44. [First Look: Fedora 9 Alpha, Running in Hyper-V Beta: CRN](http://www.crn.com/software/206106715)
45. [Install Ubuntu 7.10 on Hyper-V](http://www.haiders.net/post/Install-Ubuntu-710-on-Hyper-V.aspx)
46. [Hyper-V solution overview](http://www.brianmadden.com/content/article/Microsoft-Windows-Server-2008--Hyper-V-solution-overview)
47. [Microsoft's Hyper-V: why all the fuss?](http://reviews.zdnet.co.uk/software/os/0,1000001098,39352929,00.htm)
48. [Microsoft Hyper-V To Flaunt Advanced Virtualization Features](http://www.informationweek.com/news/software/server_virtualization/showArticle.jhtml?articleID=207401993)
49. [Microsoft and Red Hat sign virtualization pact](http://blogs.zdnet.com/microsoft/?p=2046)