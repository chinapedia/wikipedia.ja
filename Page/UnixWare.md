> この記事は[UnixWare](https://ja.wikipedia.org/wiki/UnixWare)から翻訳されています。


**UnixWare**とは、発祥の[UNIX](../Page/UNIX.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である。Univelは[AT\&T](../Page/AT&T.md "wikilink")の[UNIX Systems Laboratories](https://ja.wikipedia.org/wiki/UNIX_Systems_Laboratories "wikilink") (USL) と[ノベルによって共同所有されていたベンチャーであり](../Page/ノベル_\(企業\).md "wikilink")、後にノベルに取り込まれた。さらに[Santa Cruz Operation](../Page/SCO.md "wikilink")、[カルデラシステム](../Page/SCO.md "wikilink")、[カルデラインターナショナルシステム](../Page/SCO.md "wikilink")、そして[The SCO Groupを経てUnXis](../Page/SCO.md "wikilink")（現在の[Xinuos](https://ja.wikipedia.org/wiki/Xinuos "wikilink")）に売却された。UnixWareは通常、[デスクトップ用よりも](../Page/デスクトップパソコン.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")用に配備される。UnixWareのバイナリ配布は[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")[アーキテクチャコンピュータで利用できる](../Page/コンピュータ・アーキテクチャ.md "wikilink")。UnixWareは主にサーバオペレーティングシステム用して販売されている\[1\]\[2\]。

## 歴史

### Univel（1991年 - 1993年）

[AT\&T](../Page/AT&T.md "wikilink")の[Unix System Laboratories](https://ja.wikipedia.org/wiki/Unix_System_Laboratories "wikilink") (USL) は、[SunOS](../Page/SunOS.md "wikilink")と[System Vを統合して](../Page/UNIX_System_V.md "wikilink")[SVR4という成果を成し遂げた後](../Page/UNIX_System_V.md "wikilink")、 "Destiny" という[コードネーム](../Page/コードネーム.md "wikilink")のUNIXのデスクトップバージョンを開発するため、ノベルとの合同会社であるUnivelを結成した\[3\]。

Destinyは[UNIX System V release 4.2カーネルをベースとした](https://ja.wikipedia.org/wiki/UNIX_System_V#SVR4.2 "wikilink")。[ウィンドウシステム](../Page/ウィンドウシステム.md "wikilink")用のツールキットとしてが採用され、これによりユーザーは実行時の[ルック・アンド・フィール](../Page/ルック・アンド・フィール.md "wikilink")を[OPEN LOOK風と](https://ja.wikipedia.org/wiki/OPEN_LOOK "wikilink")[Motif風のいずれか一方を選ぶことができた](../Page/Motif_\(GUI\).md "wikilink")。商用デスクトップハードウェア上のシステムをより堅牢にするため、SVR4で採用されていた[UFS](../Page/Unix_File_System.md "wikilink")[ファイルシステム](../Page/ファイルシステム.md "wikilink")に代わり[Veritas](../Page/VERITAS.md "wikilink") [VXFS](../Page/VERITAS_File_System.md "wikilink")[ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink")が採用された。UnixWareのネットワークは、[TCP/IPとノベルのNetWareプロトコル](../Page/インターネット・プロトコル・スイート.md "wikilink") ([IPX/SPX](https://ja.wikipedia.org/wiki/IPX/SPX "wikilink")) との相互運用を機能をサポートしていた。Destinyの開発当時、UNIXユーザーにとってTCP/IPは標準であったが、PCネットワークでNetWareをベースとすることはUNIXにおけるTCP/IP以上に普通であった\[4\]。

1992年にDestinyはUnixWare 1.0としてリリースされた。UnixWare 1.0は細分化されていたPC UNIX市場をUnixWareへと統合することを意図されていた。このシステムはマイクロソフトの[Windows NTよりも早く企業コンピュータ市場へと参入したが](../Page/Microsoft_Windows_NT.md "wikilink")、当時のオブザーバー達は、UnixWareはUNIXの「単なるもう一つのフレーバー」であり、ノベルが意味のある技術を結集したものというよりもむしろ自社のマーケティング戦略に巻き込むためのものだと気付いていた。UnixWareには、ノベルのIPXネットワークは含むがTCP/IPは含まない*Personal Edition*と、TCP/IPなどのサーバソフトウェアを搭載した*Advanced Server Edition*の2つのエディションが存在した。Personal Editionにはアクティブユーザーが2名までという制限があったが、Advanced Server Editionは無制限であった。UnixWare 1.0のコピーは約35,000個販売された\[5\]。

1993年にノベルはAT\&TからUSLを購入し、USLとUnivelを統合して新たにUnix Systems Groupとした\[6\]。

### ノベル（1993年 - 1995年）

1994年にノベルはUnixWare 1.1をリリースした。Personal EditionとAdvanced Server Editionの両方にTCP/IPが含まれていた\[7\]。MOTIF 1.2ランタイムライブラリは[COSEコンプライアンス用に含まれていた](../Page/Common_Open_Software_Environment.md "wikilink")。NUC (NetWare Unix Client) ソフトウェアは[NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink")サーバと統合するために含まれていた。[DOSと](../Page/DOS_\(OS\).md "wikilink")[Windows 3.1アプリケーションを起動できるよう](../Page/Microsoft_Windows_3.x.md "wikilink")、アプリケーションがPersonal EditionとAdvanced Server Editionの両方にインストールされていた。

後にノベルはバグフィックスバージョンである1.1.1、1.1.2、1.1.3、1.1.4をリリースした。最後の1.1.4は1995年6月19日にリリースされた\[8\]。

[OEM](../Page/OEM.md "wikilink")と開発者には1994年12月\[9\]に、市場には1995年3月\[10\]に、UnixWare 2.0の出荷が開始された。UnixWare 2.0は[UNIX System V release 4.2MPカーネルをベースとし](https://ja.wikipedia.org/wiki/UNIX_System_V#SVR4.2MP "wikilink")、[マルチプロセッシング](../Page/マルチプロセッシング.md "wikilink")のサポートが追加された。

PersonalとServerのどちらのエディションでも、Serverエディション用である**Processor Upgrade**ライセンスを追加で購入することが可能で、これにより2つのプロセッサを搭載したシステムをサポートしていた。サポートされていたマルチプロセッサシステムは、Intel MP 1.1 [SMPマシンやCorollary](../Page/対称型マルチプロセッシング.md "wikilink") C-busシステムなどであった。サポートするネットワークインタフェースの数を増やすために、[NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink") [ODIネットワークドライバをサポートした](https://ja.wikipedia.org/wiki/Open_Data-Link_Interface "wikilink")。このバージョンにには[UIスレッドライブラリだけでなく](https://ja.wikipedia.org/wiki/Unix_International "wikilink")、新機能として[POSIXスレッド](https://ja.wikipedia.org/wiki/POSIXスレッド "wikilink")ライブラリも含まれていた\[11\]。

SCOがUnixWareのライセンスを獲得するよりも前の1995年に、ノベルはNetWare 4.1とUnixWare 2.0の将来技術をベースとした "**SuperNOS**" を作成するプロジェクトも公表したが、実現することはなかった。代わって、1998年に[OpenLinux用にLinux上のNetWare](https://ja.wikipedia.org/wiki/Caldera_OpenLinux "wikilink") 4.10サーバがCaldera NetWare for Linuxとして提供された。そして2005年、遂にノベルの[Open Enterprise Serverがもたらされた](https://ja.wikipedia.org/wiki/Open_Enterprise_Server "wikilink")。

### Santa Cruz Operation（1995年 - 2001年）

1995年に (SCO) はノベルからUnixWareを獲得した\[12\]。この取引の正確な条件については訴訟となった（を参照）が、後に裁判所はノベルがUNIXの所有権を保持していると判断した。

SCOは譲渡が公になった際に、UnixWareと自社の[OpenServer](https://ja.wikipedia.org/wiki/OpenServer "wikilink") [SVR3.2をベースとしたOSとの統合を目標としていることを発表した](https://ja.wikipedia.org/wiki/UNIX_System_V#SVR3 "wikilink")\[13\]が、1996年にSCOはUnixWareの最初のリリースであるバージョン2.1をリリースした。UnixWare 2.1のリリース当時、SCOが提案したUnixWare/OpenServerの統合であるプロジェクト**Gemini**は1997年から利用可能となり、UnixWareの64ビットバージョンは1998年までは開発されることが公表されていた\[14\]。

物議をかもすこととなった変更点の1つとして、OpenServerと似たユーザーライセンスポリシーの採用があった。UnivelとノベルがリリースしていたUnixWareのユーザー数上限は、Personal Editionが2人、Server Editionは無制限であった。UnixWare 2.1ではServer Editionに含まれていたユーザーライセンス数の上限は5人までで、上限をそれ以上にしたい顧客は、10、25、100、500、または無制限のユーザーライセンス拡張を購入することができた\[15\]。

SCOはUnixWare 2.1のアップデートを3つリリースした。1996年にリリースされたUnixWare 2.1.1は、[Unix 95ブランディングを達成した](../Page/Single_UNIX_Specification.md "wikilink")\[16\]。1998年にUnixWare 2.1.2および2.1.3が利用可能となったが、これらは多数のバグをフィックスしたリリースである。

1998年に[コンパック](../Page/コンパック.md "wikilink")はUnixWare 2.1バージョンによる[ProLiantサーバで](https://ja.wikipedia.org/wiki/HP_ProLiant "wikilink")[クラスターを構成した](../Page/コンピュータ・クラスター.md "wikilink")、Integrity XCとして知られるパッケージをリリースした\[17\]。

1998年の初頭に、Geminiプロジェクトの最初の成果としてUnixWare 7が利用可能となった\[18\]。SCOはカーネルバージョンを[UNIX System V release 5と名付けた](https://ja.wikipedia.org/wiki/UNIX_System_V#SVR5 "wikilink")。このシステムは主にUnixWare 2.1をベースとしており、OpenServerネットワークドライバを利用できたため、OpenServer互換なドライバ用機能が搭載されていた。OpenServerにおけるシステム管理者の管理ユーティリティである**scoadmin**により、元々UnixWareに存在した**sysadm**ユーティリティは置き換えられた。UnixWare 7の主な新機能としては、マルチパスI/O、巨大ファイルおよび巨大ファイルシステム、大容量メモリシステムのサポートがあった\[19\]。

UnixWare 7では、旧バージョンのUnixWare由来の[XENIX](../Page/XENIX.md "wikilink")互換機能と、OpenServer由来のXENIX互換機能は両方とも削除された。これライセンスが理由であり、SVR3.2に含まれるコードの使用料をマイクロソフトへ払わないようにするためであった。

1999年にSCOはUnixWare 7.1をリリースした。UnixWare 7.1はエディションの数が増え、PersonalおよびServerの2つのエディションから、**Business**（5ユーザー）・**Department**（25ユーザー）・**Enterprise**（50ユーザー）の3つのエディションへと置き換えられた。UnixWare 7.1には[タランテラ製のWebTopアプリケーションが含まれていた](../Page/タランテラ_\(企業\).md "wikilink")\[20\]。

2000年にSCOはUnixWare 7.1.1をリリースし、同時に7.1.1とIP Single system image[クラスターパッケージもリリースした](../Page/コンピュータ・クラスター.md "wikilink")。この新しいパッケージは、初期のIntegrity XC製品がサポートするプロプライエタリなコンパックハードウェアだけではなく、でも利用することが可能で、さらにSCOから直接利用可能であった\[21\]。

### カルデラシステム・カルデラインターナショナル・SCOグループ（2000年 - 2011年）

2000年8月2日に (SCO) は、OpenServerやUnixWareの権利だけでなく、サーバソフトウェアとサービス部門も[カルデラシステムに売却することを公表した](../Page/SCO.md "wikilink")。2001年3月にカルデラシステムはカルデラインターナショナル (CII) となり、2001年5月にSCOの購入が完了した。Santa Cruz Operationの残りの部分であるタランテラ部門は、[タランテラ社と改名された](../Page/タランテラ_\(企業\).md "wikilink")。

カルデラインターナショナルによるUnixWareの最初のリリースは、OpenUNIX 8と改名された。このリリースはUnixWare 7.1.2となる予定のものであった。

カルデラインターナショナルはモバイル製品やサービスを含む製品ラインを広げた後、2002年8月に自社名をSCOグループに改名した。

改名したSCOグループはその後、以前のUnixWareブランドとそのバージョンリリースナンバリングを元に戻し、UnixWare 7.1.3\[22\]と7.1.4\[23\]をリリースした。それ以降はOpenUNIXのリリースはなく、OpenUNIX 8.1.2 (OU812) はリリースされなかった。SCOグループは引き続きUnixWareを維持し、定期的なメンテナンスアップデートとサポートを行っていた\[24\]。

2007年から2011年の間、SCOグループは一連の[法廷闘争に従事しており](https://ja.wikipedia.org/wiki/SCO・Linux論争 "wikilink")、2007年9月に[連邦倒産法第11章](../Page/連邦倒産法第11章.md "wikilink")の破産措置を申請した\[25\]。

2011年4月11日にUnXisはデラウェア州の破産裁判所による認定の後、SCOグループの営業資産および知的財産権を買収した\[26\]\[27\]。

その後SCOグループはTSGグループと改名し、SCOオペレーションはTSGオペレーションとなり\[28\]、2012年8月には連邦倒産法第11章から第7章への移行を申請した\[29\]。

### UnXisそしてXinuos（2011年 - 現在）

2011年にUnXisは、OpenServerだけでなくUnixWareの権利も買収した。

2013年6月にUnXisは[Xinuos](https://ja.wikipedia.org/wiki/Xinuos "wikilink")と改名し\[30\]、SCO UnixWare 7.1.4+という製品とそれによりできることについて公表した\[31\]。現在、UnixWare 7.1.4+は物理マシンと[仮想マシンの両方をサポートする](../Page/仮想機械.md "wikilink")。

## バージョン履歴

<table>
<thead>
<tr class="header">
<th><p>リリース日</p></th>
<th><p>バージョン</p></th>
<th><p>製造元</p></th>
<th><p>コードベース</p></th>
<th><p>カーネルバージョン</p></th>
<th><p>詳細</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1991</p></td>
<td><p>UnixWare 1.0</p></td>
<td></td>
<td><p>SVR4.2</p></td>
<td><p>1</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/#Personal" title="wikilink">Personal Edition</a>, <a href="https://ja.wikipedia.org/wiki/#Advanced_Server" title="wikilink">Advanced Server</a></p></td>
</tr>
<tr class="even">
<td><p>1993</p></td>
<td><p>UnixWare 1.1</p></td>
<td><p><a href="../Page/ノベル_(企業).md" title="wikilink">ノベル</a></p></td>
<td></td>
<td><p>1</p></td>
<td><p>Personal Edition, Advanced Server</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>UnixWare 1.1.1</p></td>
<td><p>ノベル</p></td>
<td></td>
<td><p>1</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>UnixWare 1.1.2</p></td>
<td><p>ノベル</p></td>
<td></td>
<td><p>1</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>UnixWare 1.1.3</p></td>
<td><p>ノベル</p></td>
<td></td>
<td><p>1</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>1995</p></td>
<td><p>UnixWare 2.0</p></td>
<td><p>ノベル</p></td>
<td><p>SVR4.2MP</p></td>
<td><p>2.1</p></td>
<td><p><a href="../Page/対称型マルチプロセッシング.md" title="wikilink">SMPのサポート</a></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>UnixWare 1.1.4</p></td>
<td><p>ノベル</p></td>
<td><p>SVR4.2</p></td>
<td><p>1</p></td>
<td><p>UnixWare 1の最後のリリース</p></td>
</tr>
<tr class="even">
<td><p>1996</p></td>
<td><p>UnixWare 2.1</p></td>
<td></td>
<td><p>SVR4.2MP</p></td>
<td><p>2.1</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>UnixWare 2.1.1</p></td>
<td><p>Santa Cruz Operation</p></td>
<td></td>
<td><p>2.1.1</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>UnixWare 2.1.2</p></td>
<td><p>Santa Cruz Operation</p></td>
<td></td>
<td><p>2.1.2</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1998</p></td>
<td><p>UnixWare 2.1.3</p></td>
<td><p>Santa Cruz Operation</p></td>
<td></td>
<td><p>2.1.3</p></td>
<td><p>UnixWare 2の最後のリリース</p></td>
</tr>
<tr class="even">
<td><p>1998</p></td>
<td><p>UnixWare 7</p></td>
<td><p>Santa Cruz Operation</p></td>
<td><p>SVR5</p></td>
<td><p>7.0.1</p></td>
<td><p>UnixWare 2とOpenServer 5を「統合」したもの</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>UnixWare 7.0.1</p></td>
<td><p>Santa Cruz Operation</p></td>
<td></td>
<td><p>7.0.1</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>1999</p></td>
<td><p>UnixWare 7.1.0</p></td>
<td><p>Santa Cruz Operation</p></td>
<td></td>
<td><p>7.1.0</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2000</p></td>
<td><p>UnixWare 7.1.1</p></td>
<td><p>Santa Cruz Operation</p></td>
<td></td>
<td><p>7.1.1</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2001</p></td>
<td><p>Open UNIX 8</p></td>
<td><p><a href="../Page/SCO.md" title="wikilink">カルデラインターナショナル</a></p></td>
<td></td>
<td><p>7.1.2</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2003</p></td>
<td><p>UnixWare 7.1.3</p></td>
<td><p><a href="../Page/SCO.md" title="wikilink">SCO</a>グループ</p></td>
<td></td>
<td><p>7.1.3</p></td>
<td><p>(SVR6) を参照</p></td>
</tr>
<tr class="even">
<td><p>2004</p></td>
<td><p>UnixWare 7.1.4</p></td>
<td><p>SCOグループ</p></td>
<td></td>
<td><p>7.1.4</p></td>
<td><p>このリリースからLinux Kernel Personalityは含まれなくなる[32]</p></td>
</tr>
<tr class="odd">
<td><p>2004</p></td>
<td><p>UnixWare 7.1.4 MP1</p></td>
<td><p>SCOグループ</p></td>
<td></td>
<td><p>7.1.4</p></td>
<td><p>Maintenance pack 1</p></td>
</tr>
<tr class="even">
<td><p>2005</p></td>
<td><p>UnixWare 7.1.4 MP2</p></td>
<td><p>SCOグループ</p></td>
<td></td>
<td><p>7.1.4</p></td>
<td><p>Maintenance pack 2</p></td>
</tr>
<tr class="odd">
<td><p>2006</p></td>
<td><p>UnixWare 7.1.4 MP3</p></td>
<td><p>SCOグループ</p></td>
<td></td>
<td><p>7.1.4</p></td>
<td><p>Maintenance pack 3</p></td>
</tr>
<tr class="even">
<td><p>2008</p></td>
<td><p>UnixWare 7.1.4 MP4</p></td>
<td><p>SCOグループ</p></td>
<td></td>
<td><p>7.1.4</p></td>
<td><p>Maintenance pack 4</p></td>
</tr>
<tr class="odd">
<td><p>2013</p></td>
<td><p>UnixWare 7.1.4+</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Xinuos" title="wikilink">Xinuos</a></p></td>
<td></td>
<td><p>7.1.4</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/VMware_ESXi" title="wikilink">VMware ESXiによる</a><a href="../Page/仮想化.md" title="wikilink">仮想化</a>のサポート[33]</p></td>
</tr>
<tr class="even">
<td><p>2015</p></td>
<td><p>UnixWare 7 Definitive</p></td>
<td><p>Xinuos</p></td>
<td></td>
<td><p>7.1.4</p></td>
<td><p>OpenServer 10の上位互換となる[34]</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## SCO Skunkwareとオープンソース

UnixWareには全てのバージョンに渡って、[BIND](../Page/BIND.md "wikilink")/[X11](../Page/X_Window_System.md "wikilink")/[Sendmail](../Page/Sendmail.md "wikilink")/[DHCP](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")/[Perl](../Page/Perl.md "wikilink")/[Tclなどの重要な](https://ja.wikipedia.org/wiki/Tcl/Tk "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")コンポーネントが含まれている。後のリリースには、[Apache](../Page/Apache_HTTP_Server.md "wikilink")、[OpenSSH](../Page/OpenSSH.md "wikilink")、および[Mozilla](../Page/Mozilla.md "wikilink")ソフトウェアなどの多数のオープンソースアプリケーションが追加でバンドルされるようになった\[35\]。

UnixWare以外のSCOオペレーティングシステムディストリビューションの全てのバージョンにおいても、サイトからフリーでダウンロード可能なオープンソースパッケージのセットが大量に存在している\[36\]\[37\]。

## 関連項目

  - [Caldera OpenLinux](https://ja.wikipedia.org/wiki/Caldera_OpenLinux "wikilink")

  -
  -
  - [SUSE Linux](https://ja.wikipedia.org/wiki/SUSE_Linux "wikilink")

## 脚注

## 外部リンク

  - [SCO UnixWare 7 / Caldera International OpenUNIX 8 FAQ](http://www.zenez.com/tmp/scouw7faq/cache/1.html)
  - [SCO UnixWare 7.1.4 Data Sheet (PDF)](http://www.sco.com/products/unixware714/SCO_UW714_Broch_final2004.qxd.pdf)
  - [Willows Software Readies an NT Killer](http://www.networkcomputing.com/606/606hreport3.html), [Willows Software](https://ja.wikipedia.org/wiki/Willows_Software "wikilink")
  - [SCO History - includes UnixWare release dates](https://web.archive.org/web/20031204183836/http://www.sco.com/company/history.html)
  - [SCO UnixWare 7.1.3 VMWare image](http://osvirtual.net/en/sco-unixware-7-1-3/) (from OSvirtual)

[Category:System_V](https://ja.wikipedia.org/wiki/Category:System_V "wikilink") [Category:1993年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1993年のソフトウェア "wikilink")

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
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25. [The SCO Group Files Chapter 11 to Protect Assets as It Addresses Potential Financial and Legal Challenges](http://ir.sco.com/releasedetail.cfm?ReleaseID=264124). The SCO Group, Inc. press release, September 14, 2007
26. ["UnXis Completes Purchase of SCO UNIX Assets"](http://www.unxisco.com/2011/04/11/unxis-completes-purchase-of-sco-unix-assets/), press release, April 11, 2011
27.
28.
29.
30.  Press Release - UnXis renamed Xinuos|url = [http://www.xinuos.com/xinuos/news/96-pr-unxis-renamed-xinuos|website](http://www.xinuos.com/xinuos/news/96-pr-unxis-renamed-xinuos%7Cwebsite) = www.Xinuos.com|access-date = September 11, 2015|first = Sean|last = Snyder}}
31.
32.
33.
34.
35.
36.
37.