> この記事は[SunOS](https://ja.wikipedia.org/wiki/SunOS)から翻訳されています。


**SunOS**は[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")（サン）が4.1c[BSD](../Page/BSD.md "wikilink")をベースとして開発した[UNIX](../Page/UNIX.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) の一種である。後に[Solaris](../Page/Solaris.md "wikilink")と名を変えSunOSはOSの[カーネル](../Page/カーネル.md "wikilink")の名称となっている。

## 歴史

[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")、BSDの創始者であり同開発グループの中心メンバーであった[Bill Joyがサンを設立するにあたり](../Page/ビル・ジョイ.md "wikilink")、新たに開発したOSであり、4.1cBSDがベースとなっている。SunOSは[NISや](https://ja.wikipedia.org/wiki/ネットワーク・インフォメーション・サービス "wikilink")[NFSなどの今日のUNIXシステムにおいて標準となった技術を次々に実装して着実にバージョンアップを重ねていった](../Page/Network_File_System.md "wikilink")。

1987年、サンと[AT\&T](../Page/AT&T.md "wikilink")は提携し、標準のUNIXシステムの開発を進める事を発表した。その後、1989年にAT\&TからAT\&T [System V](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink") Release 4の発表、そしてSolaris 1.1.2 (SunOS 4.1.4) を最後にSystem Vへと全面移行することとなった。System Vに移行したSolaris 2.x以後では、カーネルの名称はSunOS 5.xとなった。

| **SunOS バージョン**      | **リリース時期**   | **[コードベース](https://ja.wikipedia.org/wiki/コードベース "wikilink")**                                                                            | 解説                                                                                                                                                                                                              |
| -------------------- | ------------ | ---------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Sun UNIX 0.7**     | 1982年        | [UniSoft](https://ja.wikipedia.org/wiki/UniSoft "wikilink") [UNIX v7](../Page/Version_7_Unix.md "wikilink")\[1\]                         | [MC68000](../Page/MC68000.md "wikilink")ベースのSun-1システムに同梱                                                                                                                                                        |
| **SunOS 1.0**        | 1983年        | rowspan = "3" |4.1BSD                                                                                                                    | [MC68010](https://ja.wikipedia.org/wiki/MC68010 "wikilink")ベースのSun-1および[Sun-2](../Page/Sun-2.md "wikilink")システムをサポート                                                                                            |
| **SunOS 1.1**\[2\]   | 1984年4月      |                                                                                                                                          |                                                                                                                                                                                                                 |
| **SunOS 1.2**\[3\]   | 1985年1月      |                                                                                                                                          |                                                                                                                                                                                                                 |
| **SunOS 2.0**        | 1985年5月\[4\] | 4.2BSD                                                                                                                                   | [仮想ファイルシステム](../Page/仮想ファイルシステム.md "wikilink") (VFS) と[NFSプロトコルの導入](../Page/Network_File_System.md "wikilink")                                                                                                  |
| **SunOS 3.0**        | 1986年2月\[5\] | 4.2BSD + [System V](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink") IPC                                                          | [MC68020](https://ja.wikipedia.org/wiki/MC68020 "wikilink")ベースの[Sun-3](../Page/Sun-3.md "wikilink")シリーズ対応。オプションでSystem Vのユーティリティと開発用ライブラリが付属。                                                                   |
| **SunOS 3.2**        | 1986年9月\[6\] | rowspan = "2" | 3.0に4.3BSDの一部機能を追加                                                                                                       | [Sun-4](../Page/Sun-4.md "wikilink") シリーズ対応。                                                                                                                                                                    |
| **SunOS 3.5**        | 1988年1月      |                                                                                                                                          |                                                                                                                                                                                                                 |
| **SunOS 4.0**        | 1988年12月     | rowspan = "17" | 4.3BSD + System V IPC                                                                                                   | 新[仮想記憶](../Page/仮想記憶.md "wikilink")システム、[動的リンクライブラリ](../Page/ライブラリ.md "wikilink")、自動マウント機能、System V [STREAMS](../Page/STREAMS.md "wikilink") I/O。[Sun386i](https://ja.wikipedia.org/wiki/Sun386i "wikilink")対応。 |
| **SunOS 4.0.1**      | 1988年        |                                                                                                                                          |                                                                                                                                                                                                                 |
| **SunOS 4.0.2**      | 1989年9月      | Sun386i向けのみ                                                                                                                              |                                                                                                                                                                                                                 |
| **SunOS 4.0.3**      | 1989年5月      |                                                                                                                                          |                                                                                                                                                                                                                 |
| **SunOS 4.0.3c**     | 1989年6月      | [SPARCstation 1](https://ja.wikipedia.org/wiki/SPARCstation_1 "wikilink") (Sun-4c) 向けのみ                                                  |                                                                                                                                                                                                                 |
| **SunOS 4.1**        | 1990年3月      |                                                                                                                                          |                                                                                                                                                                                                                 |
| **SunOS 4.1e**       | 1991年4月      | Sun-4e向けのみ                                                                                                                               |                                                                                                                                                                                                                 |
| **SunOS 4.1.1**      | 1990年3月      | [OpenWindows](https://ja.wikipedia.org/wiki/OpenWindows "wikilink") 2.0を同梱                                                               |                                                                                                                                                                                                                 |
| **SunOS 4.1.1B**     | 1991年2月      |                                                                                                                                          |                                                                                                                                                                                                                 |
| **SunOS 4.1.1.1**    | 1991年7月      |                                                                                                                                          |                                                                                                                                                                                                                 |
| **SunOS 4.1.1_U1**  | 1991年11月     | Sun-3/3x向けのみ                                                                                                                             |                                                                                                                                                                                                                 |
| **SunOS 4.1.2**      | 1991年12月     | [マルチプロセッシング](https://ja.wikipedia.org/wiki/マルチプロセッシング "wikilink") (SPARCserver 600MP) 対応。初の[CD-ROM](../Page/CD-ROM.md "wikilink")のみのリリース |                                                                                                                                                                                                                 |
| **SunOS 4.1.3**      | 1992年8月      |                                                                                                                                          |                                                                                                                                                                                                                 |
| **SunOS 4.1.3C**     | 1993年11月     | SPARCclassic/SPARCstation LX向けのみ                                                                                                         |                                                                                                                                                                                                                 |
| **SunOS 4.1.3_U1**  | 1993年12月     |                                                                                                                                          |                                                                                                                                                                                                                 |
| **SunOS 4.1.3_U1B** | 1994年2月      | [Y2K対応](../Page/2000年問題.md "wikilink")                                                                                                   |                                                                                                                                                                                                                 |
| **SunOS 4.1.4**      | 1994年11月     | SunOS 4の最後のリリース                                                                                                                          |                                                                                                                                                                                                                 |
| **SunOS 5.*x***      | 1992年6月 -    | [SVR4](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink")                                                                           | [Solaris](../Page/Solaris.md "wikilink")を参照                                                                                                                                                                     |

SunOS 1と2は[Sun-2](../Page/Sun-2.md "wikilink")シリーズをサポートしており、[Sun-1](../Page/Sun-1.md "wikilink")の[CPU](../Page/CPU.md "wikilink")基板を（[MC68010](https://ja.wikipedia.org/wiki/MC68010 "wikilink")に）アップグレードしたSun-2も含んでいた。SunOS 3はSun-2とSun-3シリーズ ([MC68020](https://ja.wikipedia.org/wiki/MC68020 "wikilink")) をサポートしていた。SunOS 4はSun-2（4.0.3まで）、Sun-3（4.1.1まで）、[Sun386i](https://ja.wikipedia.org/wiki/Sun386i "wikilink")（4.0、4.0.1、4.0.2のみ）、Sun-4 ([SPARC](../Page/SPARC.md "wikilink")) アーキテクチャをサポートしていた。SunOS 4はSPARCプロセッサを完全サポートした最初のリリースだったが、Sun-4システムはSunOS 3.2でも一部サポートされていた。

SunOS 4.1.2はサン初の[マルチプロセッシング](https://ja.wikipedia.org/wiki/マルチプロセッシング "wikilink")マシンである [sun4mアーキテクチャをサポートした](../Page/Sun-4.md "wikilink") (SPARCserver 600MP)。カーネルは1つの[ロックしかなく](../Page/ロック_\(情報工学\).md "wikilink")、1度に1つのCPUだけがカーネルを実行できる方式であった。

最後のリリースは1994年の4.1.4 (Solaris 1.1.2) である。[sun4](https://ja.wikipedia.org/wiki/SPARCstation "wikilink")、[sun4c](https://ja.wikipedia.org/wiki/SPARCstation "wikilink")、[sun4mはサポートされていたが](https://ja.wikipedia.org/wiki/SPARCstation "wikilink")、[sun4dはサポートされていない](https://ja.wikipedia.org/wiki/SPARCstation "wikilink")。

SunOS 4.1.3および4.1.4は[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[12月27日](../Page/12月27日.md "wikilink")まで出荷され続けた。保守サポートは[2003年](../Page/2003年.md "wikilink")[9月30日](../Page/9月30日.md "wikilink")に終了した。

## "SunOS" と "Solaris"

[thumb](https://ja.wikipedia.org/wiki/ファイル:SunOS_4.1.1_P1270750.jpg "wikilink") 1987年、AT\&Tとサンは、当時最も一般的なUNIXであった[BSD](../Page/BSD.md "wikilink")（SunOS固有の機能も含む）と[System Vと](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink")[XENIX](../Page/XENIX.md "wikilink")を統合する共同プロジェクトの開始を発表した。その成果が[System V Release 4](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink") (SVR4) である\[7\]。

[1991年](../Page/1991年.md "wikilink")[9月4日](../Page/9月4日.md "wikilink")、サンは次のOSメジャーリリースはBSDのコードベースからSVR4ベースへの切り替えを行うことを発表した。このリリースを社内では**SunOS 5**と呼んでいたが、対外的にはこの時点から**Solaris**の呼称を使い始めた。また、このブランド名はSunOSだけを指すのではなく、[OpenWindows](https://ja.wikipedia.org/wiki/OpenWindows "wikilink")デスクトップ環境と[Open Network Computing](../Page/Open_Network_Computing_Remote_Procedure_Call.md "wikilink") (ONC) 機能を包含したものだとした。

SVR4ベースのOSは翌年まで大量出荷されないと見られていたが、サンは既存のSunOS 4（およびOpenWindows）にもSolarisの名前を使い始めた。例えば、SunOS 4.1.1は**Solaris 1.0**と改称され、SunOS 5.0は**Solaris 2.0**の一部とされた。SunOS 4.1.*x*は1994年までリリースが継続され、それぞれにSolaris 1.xという名称も付与された。バージョン番号の対応は単純ではない。以下に対応表を示す。

<table>
<caption><strong>SunOS 4.1.<em>x</em> / Solaris 1.<em>x</em> / OpenWindowsリリース対応</strong></caption>
<thead>
<tr class="header">
<th><p>SunOSバージョン</p></th>
<th><p>Solarisバージョン</p></th>
<th><p>OpenWindowsバージョン</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>4.1.1<br />
4.1.1B<br />
4.1.1.1</p></td>
<td><p>1.0</p></td>
<td><p>2.0</p></td>
</tr>
<tr class="even">
<td><p>4.1.2</p></td>
<td><p>1.0.1</p></td>
<td><p>2.0</p></td>
</tr>
<tr class="odd">
<td><p>4.1.3</p></td>
<td><p>1.1 SMCC Version A</p></td>
<td><p>3.0</p></td>
</tr>
<tr class="even">
<td><p>4.1.3C</p></td>
<td><p>1.1C</p></td>
<td><p>3.0</p></td>
</tr>
<tr class="odd">
<td><p>4.1.3_U1</p></td>
<td><p>1.1.1</p></td>
<td><p>3.0_U1</p></td>
</tr>
<tr class="even">
<td><p>4.1.3_U1B</p></td>
<td><p>1.1.1B</p></td>
<td><p>3.0_U1B</p></td>
</tr>
<tr class="odd">
<td><p>4.1.4</p></td>
<td><p>1.1.2</p></td>
<td><p>3.0_414</p></td>
</tr>
</tbody>
</table>

SunOS 5はSolarisとして認知されているが、OS立ち上げ時などはSunOS 5の名称が表示されたり、[uname](https://ja.wikipedia.org/wiki/uname "wikilink")コマンドの出力や[manページ](https://ja.wikipedia.org/wiki/manページ "wikilink")のフッターなどにも古い名称が見られた。

SunOS 5.x以降は、Solarisのバージョン番号との対応は単純で、マイナー番号が同じになっている。例えば**Solaris 2.4**はSunOS 5.4に対応する。しかし、Solaris 2.6 以降、"2." が表示されなくなり、従来のマイナー番号だけが表示されるようになった。したがって、**[Solaris 10](../Page/Solaris.md "wikilink")**はSunOS 5.10に対応する。

## ユーザインタフェース

初期の SunOS に同梱された[GUI環境は](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、SunTools（後の[SunView](https://ja.wikipedia.org/wiki/SunView "wikilink")）と[NeWS](../Page/NeWS.md "wikilink")である。1989年、サンは[OPEN LOOK準拠の](https://ja.wikipedia.org/wiki/OPEN_LOOK "wikilink")[X11ベースの環境である](../Page/X_Window_System.md "wikilink")[OpenWindows](https://ja.wikipedia.org/wiki/OpenWindows "wikilink")をリリースした。これにはSunViewとNeWSのアプリケーションサポート機能も含まれている。OpenWindowsはSunOS 4.1.1でデフォルトのGUIとなった。

## 脚注

## 関連項目

  - [BSDの子孫](../Page/BSDの子孫.md "wikilink")
  - [UNIX戦争](../Page/UNIX戦争.md "wikilink")

## 外部リンク

  - [The Sun Hardware Reference (Overview)](http://www.sunhelp.org/faq/sunref1.html)
  - [SunOS & Solaris Version History](http://www.ocf.berkeley.edu/solaris/versions)
  - [*An Introduction to Solaris* — a sample chapter from *Solaris Internals: Core Kernel Architecture* by Jim Mauro & Richard McDougall, Prentice-Hall, 2000. (PDF)](http://www.informit.com/content/images/0130224960/samplechapter/0130224960.pdf)
  - [Info on SunOS from OSdata](http://www.osdata.com/oses/sunos.htm) (last updated February 17, 2002)
  - [Initial Solaris announcement](http://ftp.lanet.lv/ftp/sun-info/sunflash/1991/Sep/33.01.solaris)

[Category:System_V](https://ja.wikipedia.org/wiki/Category:System_V "wikilink") [Category:BSD](https://ja.wikipedia.org/wiki/Category:BSD "wikilink") [Category:サン・マイクロシステムズ](https://ja.wikipedia.org/wiki/Category:サン・マイクロシステムズ "wikilink") [Category:1983年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1983年のソフトウェア "wikilink")

1.
2.   SunOS 1.1、1.2、2.0、3.0、3.2のリリース時期の出典
3.
4.
5.
6.
7.