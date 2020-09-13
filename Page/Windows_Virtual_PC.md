> この記事は[Windows Virtual PC](https://ja.wikipedia.org/wiki/Windows_Virtual_PC)から翻訳されています。


**Windows Virtual PC**（**ウィンドウズ バーチャル ピーシー**）とは、[Windows上に](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")の[仮想PC環境を構築する](../Page/仮想機械.md "wikilink")[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")である。本項では先代のソフトウェアである**Microsoft Virtual PC**を含めて述べる。

## 概要

[コネクティクス](https://ja.wikipedia.org/wiki/コネクティクス "wikilink")が[Macintosh](../Page/Macintosh.md "wikilink")向けに開発し、後にWindows、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")にも移植された。マイクロソフトが2003年にコネクティクスより当製品部門および関連特許などを買収し、引き続き開発と提供をしている。

[2006年](../Page/2006年.md "wikilink")7月、Virtual PC 2004 SP1から無償提供になり\[1\] 、同年8月にMacintosh向けの提供が終了した\[2\] 。

2009年[10月19日](../Page/10月19日.md "wikilink")には[Windows 7のリリースに合わせ](../Page/Microsoft_Windows_7.md "wikilink")、ホスト[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) がWindows 7のみの「Windows Virtual PC」\[3\] と、それに対応する\[4\] \[5\] 仮想環境「**[XP Mode](https://ja.wikipedia.org/wiki/Microsoft_Windows_7#Windows_XP_Mode "wikilink")**」\[6\]（[Windows XP Professional SP3に幾つかの専用コンポーネントを追加した](../Page/Microsoft_Windows_XP.md "wikilink")、Windows Virtual PC用仮想PCイメージ）が公開された。この**Windows Virtual PC**は、Microsoft Virtual PCの実質的な後継ソフトウェアである。

## 特徴

Virtual PCは、ハードウェアとしてのPC環境を仮想的に構築する。OSを仮想的に動作させるタイプではないため、PCで動作するOSであれば基本的にゲストOSとしてインストールすることができる。開発がマイクロソフトになってからは公開時の最新版を含むWindowsや[MS-DOS](../Page/MS-DOS.md "wikilink")をゲストOSとしてサポートするようになっている。

決められたPC環境をソフトウェアで[エミュレート](https://ja.wikipedia.org/wiki/エミュレート "wikilink")するため、処理速度は物理環境より多少劣る。Virtual PC 2007からはCPUに組み込まれたハードウェア仮想化支援機能を利用できるようになっている。旧型の[ビデオチップをエミュレーションしているため](../Page/Graphics_Processing_Unit.md "wikilink")[Direct3D](../Page/Direct3D.md "wikilink")や[OpenGL](../Page/OpenGL.md "wikilink")には対応しない。ただし、後述のVirtual Machine統合コンポーネントによってグラフィックス性能が向上し、Windows Virtual PC以降では[Windows Vista以降においてWindows](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") Aeroに対応する。

ネットワーク設定は、ホスト環境の物理インターフェイスへの直接接続、ホスト環境のIPアドレスを共有する[NAT](../Page/ネットワークアドレス変換.md "wikilink")、ゲスト環境内部で連結する内部ネットワークの3種類からいずれかを指定し仮想ネットワークデバイスを作成することで行う。1つの仮想PCに対し、仮想ネットワークデバイスは最大4つ用意されている。

### エミュレーション環境

全てのVirtual PC は、同一環境である。

  - [Intel](https://ja.wikipedia.org/wiki/インテル "wikilink") [Pentium II](../Page/Pentium_II.md "wikilink") プロセッサーと、[Intel 440BX](../Page/Intel_440BX.md "wikilink") チップセット
  - [SVGA](https://ja.wikipedia.org/wiki/SVGA "wikilink") [VESA](../Page/VESA.md "wikilink") グラフィック （4 MB または 16 MB の [VRAM](../Page/VRAM.md "wikilink") サイズの [S3 Trio 32 PCI](../Page/S3_Trio.md "wikilink")）
  - [Creative](../Page/クリエイティブテクノロジー.md "wikilink") [Sound Blaster](../Page/Sound_Blaster.md "wikilink") 16 ISA PnP サウンド チップ
  - [DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") 21041 または DEC 21140 のイーサネット チップ

### Virtual Machine 統合コンポーネント

ゲスト OS (Windows) をインストール後、統合コンポーネントをインストールすることにより、ホスト環境とゲスト環境で幾つかの機能を共有することができる。

  - ゲストOS のパフォーマンスの向上
  - マウスの統合
  - 最適化されたビデオ ドライバーの使用
  - 動的なスクリーン解像度の使用
  - ホスト側との時刻同期
  - クリップボードの共有
  - ホスト-ゲスト間の[ドラッグ アンド ドロップ](../Page/ドラッグ・アンド・ドロップ.md "wikilink") （Virtual PC 2007 まで対応）
  - ホスト-ゲスト間のフォルダーの共有
  - USB デバイスのゲストOS での使用 （Windows Virtual PC で対応）
  - アプリケーションのシームレス化（ゲストOS 上のアプリケーション画面をホストOS に表示する機能。Windows Virtual PC で対応）

## ホストOSとゲストOSの対応

Virtual PC 2007 において、ホストOS の64ビット対応が行われた。しかしながら、ゲストOS の64ビット対応は行われていない。マイクロソフトの仮想化製品では[クライアントHyper-V](../Page/Hyper-V.md "wikilink") (Hyper-V Server、[Windows Server 2008](../Page/Microsoft_Windows_Server_2008.md "wikilink")、[Windows Server 2008 R2](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2008_R2 "wikilink")、[Windows Server 2012/2012 R2](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2012 "wikilink")、[Windows Server 2016](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2016 "wikilink")、[Windows 8.x Pro/Enterprise](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")、[HomeとSを除くWindows 10全エディション](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")。いずれも64ビット専用) で64ビットのゲストOS がサポートされている。

<table>
<tbody>
<tr class="odd">
<td><table>
<thead>
<tr class="header">
<th></th>
<th><p>Virtual PC 2004</p></th>
<th><p>Virtual PC 2007</p></th>
<th><p>Windows Virtual PC</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Operating system</p></td>
<td><p>ホスト</p></td>
<td><p>ゲスト</p></td>
<td><p>ホスト</p></td>
</tr>
<tr class="even">
<td><p>32 ビット</p></td>
<td><p>64 ビット</p></td>
<td><p>32 ビット</p></td>
<td><p>32 ビット</p></td>
</tr>
<tr class="odd">
<td><p>Windows Server 2016</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Windows 10 Enterprise / Enterprise LTSB</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Windows 10 Education / Pro Education</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Windows 10 Pro</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Windows 10 S</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Windows 10 Home</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Windows Server 2012 / 2012 R2</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Windows 8 / 8.1 Enterprise</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Windows 8 / 8.1 Pro</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Windows 8 / 8.1</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Windows 7 Ultimate</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
</tr>
<tr class="even">
<td><p>Windows 7 Enterprise</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
</tr>
<tr class="odd">
<td><p>Windows 7 Professional</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
</tr>
<tr class="even">
<td><p>Windows 7 Home Premium</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
</tr>
<tr class="odd">
<td><p>Windows 7 Home Basic</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
</tr>
<tr class="even">
<td><p>Windows 7 Starter</p></td>
<td><p>×</p></td>
<td><p>N/A</p></td>
<td><p>×</p></td>
</tr>
<tr class="odd">
<td><p>Windows Server 2008 Standard</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
</tr>
<tr class="even">
<td><p>Windows Vista Ultimate</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
</tr>
<tr class="odd">
<td><p>Windows Vista Enterprise</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
</tr>
<tr class="even">
<td><p>Windows Vista Business</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
</tr>
<tr class="odd">
<td><p>Windows Vista Home Premium</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
</tr>
<tr class="even">
<td><p>Windows Vista Home Basic</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
<td><p>×</p></td>
</tr>
<tr class="odd">
<td><p>Windows Vista Starter</p></td>
<td><p>×</p></td>
<td><p>N/A</p></td>
<td><p>×</p></td>
</tr>
<tr class="even">
<td><p>Windows Server 2003 Standard | x64</p></td>
<td></td>
<td><p>×</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Windows XP Professional | x64</p></td>
<td></td>
<td><p>×</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Windows XP Tablet PC Edition</p></td>
<td></td>
<td><p>N/A</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Windows XP Media Center Edition</p></td>
<td><p>×</p></td>
<td><p>N/A</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Windows XP Home Edition</p></td>
<td><p>×</p></td>
<td><p>N/A</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Windows XP Starter Edition</p></td>
<td><p>×</p></td>
<td><p>N/A</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Windows 2000 Server</p></td>
<td><p>×</p></td>
<td><p>N/A</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Windows 2000 Professional</p></td>
<td></td>
<td><p>N/A</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Windows Me</p></td>
<td><p>×</p></td>
<td><p>N/A</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Windows 98 Second Edition</p></td>
<td><p>×</p></td>
<td><p>N/A</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Windows 98</p></td>
<td><p>×</p></td>
<td><p>N/A</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Windows 95</p></td>
<td><p>×</p></td>
<td><p>N/A</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Windows NT 4.0 Workstation</p></td>
<td><p>×</p></td>
<td><p>N/A</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Windows NT 3.51 Workstation</p></td>
<td><p>×</p></td>
<td><p>N/A</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Windows NT 3.1, NT 3.5 (Workstation)</p></td>
<td><p>×</p></td>
<td><p>N/A</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>OS/2</p></td>
<td><p>×</p></td>
<td><p>N/A</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>16 ビット</p></td>
<td><p>16 ビット</p></td>
<td><p>16 ビット</p></td>
</tr>
<tr class="odd">
<td><p>Windows 3.1</p></td>
<td><p>×</p></td>
<td></td>
<td><p>×</p></td>
</tr>
<tr class="even">
<td><p>MS-DOS 6.22</p></td>
<td><p>×</p></td>
<td></td>
<td><p>×</p></td>
</tr>
</tbody>
</table></td>
<td><table>
<tbody>
<tr class="odd">
<td><p>表の説明</p></td>
</tr>
<tr class="even">
<td><p>マイクロソフトのサポート</p></td>
</tr>
<tr class="odd">
<td><p>○</p></td>
</tr>
<tr class="even">
<td><p>×</p></td>
</tr>
<tr class="odd">
<td><p>N/A</p></td>
</tr>
<tr class="even">
<td><p>機能</p></td>
</tr>
<tr class="odd">
<td></td>
</tr>
<tr class="even">
<td></td>
</tr>
<tr class="odd">
<td></td>
</tr>
<tr class="even">
<td><p><em>(grey)</em></p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

1.  Virtual PC 2007 SP1が必要。また、Windows VistaからWindows 7へ上書きによるアップグレードを実行する場合、一旦Virtual PCをホストPC上からアンインストール（削除）する必要がある。

2.  2008年1月のWindows Vistaのソフトウェア ライセンス条項の改訂により、Home PremiumとHome BasicのゲストOSとして使用が可能となった。

3.  Virtual PC 2007 SP1用の修正プログラム (KB958162)\[7\] をインストールする。

4.  Windows Aero は使用できない。

5.  Windows Virtual PC の統合コンポーネントは、Windows XP Professional SP3と、Windows Vista Business SP1以降、Windows Vista Enterprise SP1以降、Windows Vista Ultimate SP1以降、Windows 7 Professional、Windows 7 Enterprise、Windows 7 Ultimateのみインストールできる。

6.  以前のバージョンと互換性があるため、ある程度動作する。Virtual PC 2007 では、MS-DOS 6.22、Windows 95、Windows 98、Windows Me、Windows NT 4.0 Workstationの正式な対応を終了した。

7.  Virtual PC 2004 SP1が必要。

## ホストOS上でのシステム条件

### Virtual PC 2007 SP1 日本語版

次の条件を満たす必要がある（----技術概要\[8\]15ページまたはシステム要件\[9\]参照）。

  - L2キャッシュを搭載した400MHz以上（1GHzを推奨）のプロセッサを備える[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")互換または[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")互換で[PentiumII](https://ja.wikipedia.org/wiki/PentiumII "wikilink")または[Athlon](../Page/Athlon.md "wikilink")以降のCPU\[10\] （Virtual PC 2007以降ではマルチコアCPUでも実行可能であるが、ゲスト側では基本的に1つのCPUとして認識される　ホスト側では複数のコアに分散されて処理される）
  - メモリ
      - 使用する予定のゲストOSの要件に、使用する予定のホストOSのメモリ要件を合わせた量。複数のゲストOSを同時に使用する予定がある場合、同時に実行する必要があるゲストOSの全ての合計。
  - CD-ROMドライブまたはDVDドライブ
  - Super VGA (800×600)以上の解像度を持ったモニタ
  - キーボードおよび マイクロソフトマウスまたは互換性のあるポインティングデバイス

### Windows Virtual PC 日本語版

次の条件を満たす必要がある（----システム要件\[11\]参照）。

  - Windows 7(Starter以外のエディション)
  - [Intel VTや](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink")[AMD-V (AMD Virtualization)などの仮想化支援機能に対応したCPUを搭載し](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink")、System BIOSで有効化されていること（KB977206\[12\] の修正プログラムをインストールすれば、この条件は不要となる）。
  - メモリ 2GB（推奨）
  - 20MBのハードディスク容量（他に、ゲスト用の容量が必要）

## 脚注

### 注釈

### 出典

## 関連項目

  - [VHD (ファイルフォーマット)](https://ja.wikipedia.org/wiki/VHD_\(ファイルフォーマット\) "wikilink")
  - [x86仮想化](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink")
      - [Hyper-V](../Page/Hyper-V.md "wikilink")
      - [VirtualBox](../Page/VirtualBox.md "wikilink")
      - [VMware](../Page/VMware.md "wikilink")

## 外部リンク

  - [Download Virtual PC 2007 技術概要](https://www.microsoft.com/ja-jp/download/details.aspx?id=6984) — Microsoftダウンロードセンター

[Category:マイクロソフトのソフトウェア](https://ja.wikipedia.org/wiki/Category:マイクロソフトのソフトウェア "wikilink") [Category:Windowsのソフトウェア](https://ja.wikipedia.org/wiki/Category:Windowsのソフトウェア "wikilink") [Category:エミュレーションソフトウェア](https://ja.wikipedia.org/wiki/Category:エミュレーションソフトウェア "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink") [Category:1997年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1997年のソフトウェア "wikilink")

1.
2.
3.
4.  Windows 7 Professional、Enterprise、Ultimateのみ利用可能(ただしHome Premiumでも選択肢でProfessional以上にすればインストールして使用することは可能)。
5.  Windows Virtual PC専用ではなく、他の仮想化ソフトウェアでの利用もライセンス上認められている。
6.
7.  [Virtual PC 2007 Service Pack 1 用の修正プログラム ロールアップ パッケージ (2009 年 2 月 20 日) について](http://support.microsoft.com/kb/958162)
8.
9.
10. Virtual PC 2007のダウンロードページに記載されているProcessor欄より。この制限の為400MHz以上でも動作対象外のプロセッサ([K6-2](https://ja.wikipedia.org/wiki/K6-2 "wikilink")等)が存在する。
11.
12. [Windows 7 を実行しているコンピューター上の Windows Virtual PC での Windows XP Mode のハードウェア支援による仮想化に関するエラー メッセージ](http://support.microsoft.com/kb/977206/ja)