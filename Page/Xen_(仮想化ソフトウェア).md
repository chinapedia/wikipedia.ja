> この記事は[Xen \(\)](https://ja.wikipedia.org/wiki/Xen_\(\))から翻訳されています。


**Xen**（ゼン）は、[仮想マシンモニタの一つ](../Page/ハイパーバイザ.md "wikilink")。一つの[ハードウェア](../Page/ハードウェア.md "wikilink")を用いて、複数の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) を[並列実行](../Page/並列化.md "wikilink")・制御するサービスを提供する。

## 概要

Xenは、[ケンブリッジ大学](../Page/ケンブリッジ大学.md "wikilink")のComputer Laboratoryにおいて最初のバージョンが開発された。2010年より、XenコミュニティはXenを[GPLv2ライセンスの下で](../Page/GNU_General_Public_License.md "wikilink")、フリーソフトウェアとして開発・メンテナンスしている。Xenは、[IA-32](../Page/IA-32.md "wikilink")、[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")、[IA-64](../Page/IA-64.md "wikilink")、そして[ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")において利用が可能である。

Xenでは、仮想マシンの実行単位をドメインと呼ぶ。Xenシステムにおいて、Xen[ハイパーバイザ](../Page/ハイパーバイザ.md "wikilink")は最も低い特権層で動作する、中核となる[ソフトウェア](../Page/ソフトウェア.md "wikilink")である\[1\]。Xenハイパーバイザ階層は一つまたは複数のゲストOSをサポートし、物理[CPU](../Page/CPU.md "wikilink")に対してのスケジューリングを行う。最初のゲストOSは、Xenの専門用語において「*ドメイン 0* (*dom0*)」と呼ぶ。これは標準において、ハイパーバイザが起動する時に自動的に実行され、特別な管理特権と、全ての物理ハードウェアへの直接アクセスを受け持つ。システム管理者は、追加された全てのゲストOSに対して、dom0を通してログインすることができる。このときの管理対象を、Xenの専門用語において「*ドメインU*」(*domU*)と呼び、ドメインUは*user domains*を意味する。

ドメイン0となるOSには、一般的に[Linux](../Page/Linux.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")の修正版が用いられる。なお、従来Linuxにおいても[カーネル](../Page/カーネル.md "wikilink")の修正が必要であったが、Linux kernel 2.6.23においてXenがmain lineに統合されている\[2\]。これ以降のバージョンにおいてkernelの修正は必要なくなっている。

ドメインUは、[完全仮想化](https://ja.wikipedia.org/wiki/完全仮想化 "wikilink")または[準仮想化](../Page/準仮想化.md "wikilink")において利用可能なオペレーティングシステムに違いがある。ホスト[プロセッサ](../Page/プロセッサ.md "wikilink")が[Intel VT-xや](https://ja.wikipedia.org/wiki/Intel_VT-x "wikilink")[AMD-Vのような](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink")[x86仮想化支援機能を有する場合には](https://ja.wikipedia.org/wiki/X86仮想化#ハードウェア仮想化支援 "wikilink")、未修正の[オープンソース](../Page/オープンソース.md "wikilink")、あるいは[Microsoft Windowsのような](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[プロプライエタリなOSのコピーが完全仮想化された状態で動作する](../Page/プロプライエタリ・ソフトウェア.md "wikilink")\[3\]。修正が行われているOSは、拡張サポートのための特殊なドライバを併用して準仮想化されるのがXenの特徴である。

現在では、XenSourceは[シトリックス・システムズ](../Page/シトリックス・システムズ.md "wikilink")の仮想化事業部門として統合されており、製品版の開発・販売を担っている。

## 歴史

Xenのオリジナルは、**XenSource, Inc**の創立者であり[ケンブリッジ大学](../Page/ケンブリッジ大学.md "wikilink")の上級講師であるが率いる、ケンブリッジ大学の研究プロジェクトである。XenSourceは、フリーソフトウェア・プロジェクトによる開発と、エンタープライズ版を販売し、一般へのXenの最初の公開は2003年に行われた。

シトリックス・システムズは2007年8月15日にXenSourceの買収を発表し、シトリックス・ブランドに合わせてXenSourceの製品名を次の通り変更した:

  - XenExpress : 過去の"XenServer Express Edition" と "XenServer OEM Edition" （組み込み向けのハイパーバイザ）
  - XenServer : 過去の "XenServer Standard Edition"
  - XenEnterprise 過去の "XenServer Enterprise Edition"

後に、製品名はXenServer（フリー）、Essentials for XenServer Enterprise、そしてEssentials for XenServer Platinumに変更されている。

2007年10月25日、シトリックス・システムズはXenSourceの買収を完了し\[4\]、Xenプロジェクトを <http://www.xen.org/> に移動した。これに伴って、11月頃にはシトリックス・システムズ、[IBM](../Page/IBM.md "wikilink")、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")、[ノベル](../Page/ノベル_\(企業\).md "wikilink")、 [レッドハット](../Page/レッドハット.md "wikilink")、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")\[5\]、[オラクルをメンバーとして](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")、**Xen Project Advisory Board** (**Xen AB**)\[6\] を公表している。

2010年の春には、製品名が次のように改められている:

  - XenServer（無償版）
  - XenServer Advanced Edition
  - XenServer Enterprise Edition
  - XenServer Platinum Edition

### リリース履歴

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース日</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.0</p></td>
<td><p>2003-10-02[7][8]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2.0</p></td>
<td><p>2004-11-05[9]</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.0</p></td>
<td><p>2005-12-05[10][11]</p></td>
<td><ul>
<li><a href="../Page/インテル_バーチャライゼーション・テクノロジー.md" title="wikilink">Intel VT-x仮想化支援をサポート</a></li>
<li><a href="../Page/IA-64.md" title="wikilink">IA-64</a>アーキテクチャをサポート</li>
</ul>
<p>加えて、3.0.4のリリースにおいて次の機能が加えられた:</p>
<ul>
<li><a href="https://ja.wikipedia.org/wiki/x86仮想化" title="wikilink">AMD SVM仮想化拡張をサポート</a>[12]</li>
<li><a href="../Page/PowerPC.md" title="wikilink">PowerPC</a>アーキテクチャをサポート[13]</li>
<li>準仮想化ゲストに対してグラフィカルフレームバッファをサポート[14]</li>
</ul></td>
</tr>
<tr class="even">
<td><p>3.1</p></td>
<td><p>2007-05-18[15]</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.2</p></td>
<td><p>2008-01-17[16]</p></td>
<td><p>ホストシステムに<a href="../Page/Peripheral_Component_Interconnect.md" title="wikilink">PCIパススルーと</a><a href="../Page/Advanced_Configuration_and_Power_Interface.md" title="wikilink">ACPI</a> S3スタンバイモードをサポート</p></td>
</tr>
<tr class="even">
<td><p>3.3</p></td>
<td><p>2008-08-24[17]</p></td>
<td><p>PCIパススルーとパワーマネジメントに関する改良</p></td>
</tr>
<tr class="odd">
<td><p>3.4</p></td>
<td><p>2009-05-18[18]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>4.0</p></td>
<td><p>2010-04-07[19]</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4.1</p></td>
<td><p>2011-03-25[20]</p></td>
<td><p>ホストの最大物理メモリが5TBにアップ [21]</p></td>
</tr>
<tr class="even">
<td><p>4.2</p></td>
<td><p>2012-09-17[22]</p></td>
<td><ul>
<li>ホストの最大物理CPU数が4095にアップ</li>
<li>PVゲストの最大CPU数が512にアップ</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>4.3</p></td>
<td><p>2013-07-09[23]</p></td>
<td><ul>
<li>ARMアーキテクチャの実験的サポート</li>
<li>Open vSwitchのサポート</li>
</ul></td>
</tr>
<tr class="even">
<td><p>4.4</p></td>
<td><p>2014-03-10[24]</p></td>
<td><ul>
<li>ARMアーキテクチャの正式サポート</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>4.5</p></td>
<td><p>2015-01-15[25]</p></td>
<td><ul>
<li>43種類の新機能の追加</li>
<li>コードが全面的に見直され、約78000行が追加、約141000行が削除された</li>
</ul></td>
</tr>
<tr class="even">
<td><p>4.6</p></td>
<td><p>2015-10-13[26]</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4.7</p></td>
<td><p>2016-05-23[27]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>4.8</p></td>
<td><p>2016-12-05[28]</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4.9</p></td>
<td><p>2017-05-28[29]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>4.10</p></td>
<td><p>2017-12-12[30]</p></td>
<td></td>
</tr>
</tbody>
</table>

## 利点

Xenは、他の仮想マシンに共通する以下の利点を提供する。

  - 可用性の向上 : 動作中の仮想マシンをほぼ瞬時に別ハードウェアに移動すること（[マイグレーション](https://ja.wikipedia.org/wiki/データ移行 "wikilink")）ができるため、ハードウェアのメンテナンスやアップグレードがサービスを停止せずに行える。
    柔軟性の向上 : 仮想マシン間でCPUやメモリなどの資源配分を指定することで、ニーズに応じて適切な資源を無駄なく割り当て活用できる。
    運用コストの低下 : サーバ群において、他のサーバに環境を構築するのが容易である。
    セキュリティの向上 : 仮想マシン環境は互いに隔離されており、ある仮想マシンで動作する有害なソフトウェアがほかの環境や仮想マシンモニタに悪影響を与えることはできない。

また、Xenは準仮想化手法も採用しており、完全仮想化のそれにくらべより小さい[オーバーヘッド](https://ja.wikipedia.org/wiki/オーバーヘッド "wikilink")を実現している。

## Xenの特徴

### 仮想化モデル

#### 準仮想化 (ParaVirtualization)

Xenは[準仮想化](../Page/準仮想化.md "wikilink")と呼ばれる実装手法を標準採用している。 実在のハードウェアを完全にエミュレートする代わりに、仮想マシン環境を実現するのに都合の良い仮想的なハードウェアを再定義する。 この仮想ハードウェアは、実在のハードウェアに似ているが、操作をするためにはハイパーバイザコールを呼び出す必要がある。 Xenはこのハイパーバイザコールの要求に応じて、仮想マシン環境に変更を加える。

この実装手法はエミュレーションのオーバーヘッドを最小限に抑えることができるため、性能面で大きなアドバンテージがあるが、 OSをXen仮想ハードウェア上に移植する必要がある。

#### 完全仮想化 (FullVirtualization)

Xenはハードウェアの完全仮想化機能も提供している。この機能を利用すると、実ハードウェア用に用意されたOSをそのままXen上で動作させることが可能となる。Xenでは、完全仮想化されたドメインを*HVMドメイン* (*Hardware Virtual Machine*) と呼ぶ。

この完全仮想化機能が提供する仮想マシン環境内のOSは、特権モードで動作し完全に物理ハードウェアを支配しているかのように振る舞う。実際には、仮想マシン側のOSが仮想ハードウェアを制御する命令を実行したとき、仮想ハードウェアがそれを検出し、例外のようなものが発生してXenに制御を渡す。制御を渡されたXenは、OSが行おうとした処理を分析し、仮想ハードウェアの動作をエミュレートする。完全仮想化の環境は、準仮想化方式に比べると、エミュレーションのためのコストが大きくなるが、ソフトウェアをユーザの手で変更することが難しいWindowsなどのOSも動作させることができる。

エミュレーションのオーバヘッドを最小限に抑えるために、[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")のみ準仮想化されたものを用いることも可能である。

### デバイスドライバのモデル

Xen自体は[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")を持たず、ドメイン0上のOSが物理デバイスの制御を行う。 この仕組みにより、そのOSが動作するハードウェアであればどこでもXenによる仮想マシン環境を利用できる。

## 動作するOS

2009年6月現在、[Linux](../Page/Linux.md "wikilink")、[MINIX](../Page/MINIX.md "wikilink")、[Plan 9 from Bell Labs](../Page/Plan_9_from_Bell_Labs.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[OpenSolaris](../Page/OpenSolaris.md "wikilink")、[NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink")、[GNU/Hurd/Mach](../Page/GNU_Hurd.md "wikilink")、[OZONEがXenの上で動作する](https://ja.wikipedia.org/wiki/OZONE_\(オペレーティングシステム\) "wikilink")。

## 動作環境

多くの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")が標準でXenを含んでいる。[Fedora Core 4以降](https://ja.wikipedia.org/wiki/Fedora_Core "wikilink")、[Xenoppix](../Page/KNOPPIX.md "wikilink")、[SUSE Linux 10.0](../Page/SUSE.md "wikilink")、[Debian Etch](../Page/Debian.md "wikilink")、[RHEL5](../Page/Red_Hat_Enterprise_Linux.md "wikilink")、[Ubuntu](../Page/Ubuntu.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")などでサポートされている。また[Solaris](../Page/Solaris.md "wikilink")/[OpenSolaris](../Page/OpenSolaris.md "wikilink")にも移植されている\[31\]。

Xen3.0.2は[P6](../Page/P6マイクロアーキテクチャ.md "wikilink") (Pentium Pro) 以上のCPUで動作する。（一部のモバイル向けCPUはPAE非対応のため動作しない）

完全仮想化機能を用いるためには[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")製の[Intel VT対応CPU](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink")、もしくは[AMDの](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[AMD-V対応CPUが必要となる](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink")。他に、サポートしているプラットフォームとしては、[IA-64](../Page/IA-64.md "wikilink")や[PowerPC](../Page/PowerPC.md "wikilink")上でも稼動する。

### Hyper-Vとの関係

XenSourceと[マイクロソフト](../Page/マイクロソフト.md "wikilink")は[ハイパーバイザ](../Page/ハイパーバイザ.md "wikilink")形式の仮想化システムに関し、共同開発を行っており、Xenと[Hyper-V](../Page/Hyper-V.md "wikilink")は共に同一の仮想化コアを用いている。両者はそれぞれ独自の各種用語を用いているが、その主な違いは、実ハードウェアのサポートを受け持つXenで言うところのDOM0に標準搭載されている管理用OSが主にライセンスの関係\[32\]で、Xenでは[Linux](../Page/Linux.md "wikilink")であり、Hyper-Vでは[Windows Server 2008である程度である](../Page/Microsoft_Windows_Server_2008.md "wikilink")。このため、XenとHyper-Vの上で動作する対応OSは同一である\[33\]。また、両者の仮想ディスクも相互運用が可能となっており、Xenで運用している仮想マシンをHyper-Vに、Hyper-Vで運用している仮想マシンをXenに移行といった事が特に意識せず可能となっている。

## 脚注

## 参考文献

  -
## 関連項目

  - [仮想機械](../Page/仮想機械.md "wikilink")
  - [リングプロテクション](../Page/リングプロテクション.md "wikilink")
  - [x86仮想化](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink")

## 外部リンク

  - [Computer Laboratory - Xen virtual machine monitor](http://www.cl.cam.ac.uk/Research/SRG/netos/xen/)
      - Xenの開発元となったケンブリッジ大学のプロジェクト。
  - [Welcome to xen.org, home of the Xen hypervisor, the powerful open source industry standard for virtualization.](http://www.xen.org/)
      - 現在の開発拠点。Xen のパッケージやソースコード、構築済み仮想マシンを提供している。
  - [XenSource](http://www.citrixxenserver.com/Pages/default.aspx)

<!-- end list -->

  - Xenをベースとしたハイパーバイザー
      - [Oracle VM](http://www.oracle.com/jp/technologies/virtualization/overview/index.html)
      - [Sun xVM Server](http://www.sun.com/software/products/xvm/index.jsp)
      - [Citrix XenServer](http://www.citrix.co.jp/products/xenser.html)
  - WindowsPVドライバー
      - [XenWindowsGPLPVドライバwiki](http://wiki.xensource.com/xenwiki/XenWindowsGplPv)
      - [WindowsPVドライバーバイナリ](http://www.meadowcourt.org/downloads/)

<!-- end list -->

  - メーリングリスト
      - 日本語のXen
          - [メーリングリスト登録](http://lists.xensource.com/mailman/listinfo/xen-japanese)
          - [メーリングリストリリース](http://blog.xen.org/index.php/2008/12/08/new-mailing-list-xen-japaneselistsxensourcecom/)

[Category:エミュレーションソフトウェア](https://ja.wikipedia.org/wiki/Category:エミュレーションソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink") [Category:2003年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2003年のソフトウェア "wikilink")

1.  [Xen 3.0 User Manual](http://www.cl.cam.ac.uk/research/srg/netos/xen/readmes/user/user.html)
2.
3.  [Xen OS Compatibility](http://wiki.xensource.com/xenwiki/OSCompatibility)
4.
5.  現在ではオラクルに買収されている。
6.
7.  [Xen /   Xen high-performance x86 virtualization](https://sourceforge.net/p/xen/mailman/message/5533663/)
8.  [The first stable Xen release ](https://lwn.net/Articles/52033/)
9.  [Xen 2.0 released ](https://lwn.net/Articles/109789/)
10. [Xen 3.0 released ](https://lwn.net/Articles/162841/)
11. [XenSource: Press Releases](http://web.archive.org/web/20051210024853/http://www2.getxen.com/news/pr120505b.html)
12. <http://lists.xensource.com/archives/cgi-bin/mesg.cgi?a=xen-users&i=A95E2296287EAD4EB592B5DEEFCE0E9D4BA296%40liverpoolst.ad.cl.cam.ac.uk>
13. [ Xen 3.0.3 released\! - Xen Source](http://old-list-archives.xenproject.org/archives/html/xen-devel/2006-10/msg00733.html)
14. [ FW: Xen 3.0.4 released\! - Xen Source](http://old-list-archives.xenproject.org/archives/html/xen-devel/2006-12/msg00889.html)
15. <http://lists.xensource.com/archives/html/xen-announce/2007-05/msg00002.html>
16. <http://vmblog.com/archive/2008/01/17/xen-3-2-0-officially-released.aspx>
17. <http://www.h-online.com/newsticker/news/item/Xen-3-3-0-hypervisor-ready-for-download-737027.html>
18. <http://community.citrix.com/display/ocb/2009/05/18/Xen.org+Announces+Release+of+Xen+3.4+Hypervisor>
19. <http://www.h-online.com/open/news/item/Virtualisation-Xen-is-looking-to-catch-up-by-releasing-version-4-974405.html>
20. <http://blog.xen.org/index.php/2011/03/25/xen-4-1-releases/>
21. <http://wiki.xen.org/wiki/Xen_Release_Features>
22. <http://blog.xen.org/index.php/2012/09/17/xen-4-2-0-released/>
23. <http://blog.xen.org/index.php/2013/07/09/xen-4-3-0-released/>
24. <http://blog.xen.org/index.php/2014/03/10/xen-4-4-released/>
25. <https://blog.xenproject.org/2015/01/15/less-is-more-in-the-new-xen-project-4-5-release/>
26. <http://wiki.xenproject.org/wiki/Xen_Project_4.6_Release_Notes>
27. <https://wiki.xenproject.org/wiki/Xen_Project_4.7_Release_Notes>
28. <https://wiki.xenproject.org/wiki/Xen_Project_4.8_Release_Notes>
29. <https://wiki.xenproject.org/wiki/Xen_Project_4.9_Release_Notes>
30. <https://wiki.xenproject.org/wiki/Xen_Project_4.10_Release_Notes>
31. [Xen at OpenSolaris.org](http://www.opensolaris.org/os/community/xen/)
32. [XenSource買収も事前に相談、MSとシトリックスの関係とは － ＠IT](http://www.atmarkit.co.jp/news/200805/21/citrix.html)
33. [マイクロソフトと XenSource が、Windows Server “Longhorn” Virtualization に向けた相互運用テクノロジを共同開発](http://www.microsoft.com/japan/presspass/detail.aspx?newsid=2766)