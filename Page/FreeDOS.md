> この記事は[FreeDOS](https://ja.wikipedia.org/wiki/FreeDOS)から翻訳されています。


**FreeDOS** は、[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")のための[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) である。 [MS-DOS](../Page/MS-DOS.md "wikilink")互換の自由な代替環境などを目的として作られた。現在の最新バージョンは2016年12月25日に公開された1.2である\[1\]。

多くのハードウェアをサポートしており、1981年発売の旧式[IBM PCをはじめ](../Page/IBM_PC.md "wikilink")、最新の[Intel Core i7](https://ja.wikipedia.org/wiki/Intel_Core_i7 "wikilink") CPUや各種組み込み機器上でも動作する。MS-DOSと同様に、FreeDOSは[カーネル](../Page/カーネル.md "wikilink")を介した[ディスクおよび](../Page/ディスクメディア.md "wikilink")[ファイルシステム](../Page/ファイルシステム.md "wikilink")へのアクセスおよび、簡易[メモリ管理](../Page/メモリ管理.md "wikilink")機能を提供している。[GUIは搭載されていないが](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、[OpenGEMがGUIとして推奨されている](https://ja.wikipedia.org/wiki/Graphical_Environment_Manager "wikilink")。MS-DOS同様、[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")または[ハードディスクから起動することができ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")、[ROMからの起動もサポートされている](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")。MS-DOSとは異なり、[CD-ROM](../Page/CD-ROM.md "wikilink")からも起動できる。FreeDOSは[GNU GPLのもとでライセンスされている](../Page/GNU_General_Public_License.md "wikilink")[オープンソースソフトウェア](../Page/オープンソースソフトウェア.md "wikilink")であり、誰でもロイヤリティを払うことなしに自由に独自のディストリビューションを作成し、配布することができる。

## 歴史

FreeDOSプロジェクトは、[マイクロソフト](../Page/マイクロソフト.md "wikilink")がMS-DOSの販売中止を発表した[1994年](../Page/1994年.md "wikilink")[6月26日](../Page/6月26日.md "wikilink")に、[ジム・ホールによって開始された](https://ja.wikipedia.org/wiki/ジム・ホール_\(プログラマ\) "wikilink")。彼はオープンソースの代替DOSを開発する声明を発表し、数週間のうちにパット・ヴィリアーニ（"patv", 互換カーネル「DOS-C」の作者。1954-2011）やティム・ノーマン他が参加した。その後、彼ら自身が書いたコードや当時他から利用可能だったコードを集め、カーネル本体や[シェル](../Page/シェル.md "wikilink") ([COMMAND.COM](../Page/COMMAND.COM.md "wikilink"))、基本的なユーティリティなどが作成された。バージョン1.0 は[2006年](../Page/2006年.md "wikilink")[9月3日](https://ja.wikipedia.org/wiki/9月3日 "wikilink")、バージョン1.2は[2016年](../Page/2016年.md "wikilink")[12月25日](../Page/12月25日.md "wikilink")にリリースされた。

そのままでの利用者は少ないが、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")のビジネス向けPCで「OS無しモデル」を選択すると、動作確認用としてプリインストールされる、AsusのOS無しモデルでも同様に動作確認用にプリインストールされるなど、ホビーユースや古い機種の維持以外にも利用されている。

[FreeDOSの公式ウェブサイト](http://www.freedos.org/)からは、リリースやソースファイルなど、全てのプロジェクト関連ファイルがダウンロードできる。

## MS-DOSとの関係

FreeDOSは、

FreeDOSはいくつかの点でMS-DOSよりも改善されており、例えば国際化や省電力管理、統合化された[ASPIなど](../Page/Advanced_SCSI_Programming_Interface.md "wikilink")、マイクロソフトがMS-DOSのサポートを打ち切った当時には存在していなかった新しい標準規格や技術に対応している。またマイクロソフトからスタンドアローンで出ているMS-DOS (バージョン6.22まで)では公式にサポートされていなかった[LBAと](https://ja.wikipedia.org/wiki/Logical_Block_Addressing "wikilink")[FAT32ファイルシステム](../Page/File_Allocation_Table.md "wikilink") (FAT32からの起動も含む) もサポートしている。

## 互換性

### 一般

MS-DOS用に書かれたほとんどのアプリケーションはFreeDOSでも動作する。[実行ファイル](../Page/実行ファイル.md "wikilink")形式としては、以下のものがサポートされている:

  - 旧式の .COM [実行形式](../Page/実行ファイル.md "wikilink")
  - 標準的な 16ビット .EXE 実行形式
  - [ボーランド](../Page/ボーランド.md "wikilink")による[16ビット](../Page/16ビット.md "wikilink")のDOS プロテクト・モード・インターフェイス ([DPMI](../Page/DPMI.md "wikilink")) 実行形式
  - 以下の[DOSエクステンダ](../Page/DOSエクステンダ.md "wikilink")を使用した [32ビット](../Page/32ビット.md "wikilink") DPMI実行形式:
      - DOS/32A
      - Causeway
      - DOS/4GW
      - GO32/CWSDPMI
      - その他

またHX DOS Extenderを使用することにより、多くの Win32コンソールアプリケーションや、[QEMU](../Page/QEMU.md "wikilink")や[Bochs](../Page/Bochs.md "wikilink")などいくつかの[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")プログラムも FreeDOS 上で動作する。

#### Windows 1.0 から 3.xx まで

FreeDOS上ではWindows 1.0および2.0 がそのまま動作する。しかし[i386プロセッサをサポートしたWindows](../Page/Intel_80386.md "wikilink") 3.xリリースを「386エンハンスド・モード」で走らせることはできない。Windows 3.0はリアルモードあるいはスタンダード・モードで走らせることができ、それ以降のWindows 3.xリリースはスタンダード・モードでのみ動作する。[Windows for Workgroups 3.11ではスタンダード](https://ja.wikipedia.org/wiki/Windows_for_Workgroups_3.11 "wikilink")・モードのサポートが打ち切られたためそのままでは FreeDOS上で動かすことはできないが、FreeDOS 用の`himem.exe`および`emm386.exe`をそれぞれWindowsに付属している`himem.sys`と[`emm386.exe`](../Page/EMM386.md "wikilink")に置き換えれば動かすことができる。\[2\]

#### Windows 9x および Windows Me

[Windows 95](../Page/Microsoft_Windows_95.md "wikilink")、[98および](../Page/Microsoft_Windows_98.md "wikilink")[MeはDOSベースのWindowsだが](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink")、これらのOSはMS-DOSに似てはいるものの独自の[ブートローダ](https://ja.wikipedia.org/wiki/ブートローダ "wikilink")上で動作し、Windowsシステムと一体化している。そのためWindows 95、98およびMEをFreeDOS上で動作させることはできない。しかしこれらのシステムとは独立にFreeDOSをインストールすることはでき、その場合はFreeDOS付属の`METAKERN`プログラムや、[LILO](../Page/LILO.md "wikilink")や[GRUBなどの](../Page/GNU_GRUB.md "wikilink")[ブートマネージャ](https://ja.wikipedia.org/wiki/ブートマネージャ "wikilink")を利用する。

#### Windows NT/2000/XP/2003 および ReactOS

[Windows NT系のオペレーティングシステム](../Page/Windows_NT系.md "wikilink")（[Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink")、[XPおよび](../Page/Microsoft_Windows_XP.md "wikilink")[2003](https://ja.wikipedia.org/wiki/Microsoft_Windows_2003 "wikilink")）は [MS-DOS](../Page/MS-DOS.md "wikilink") をシステムの核として使っていない。これらのシステムではMS-DOSおよび以前のバージョンのWindowsで使われていた [FATファイルシステムを使うこともできるが](../Page/File_Allocation_Table.md "wikilink")、今ではこれらのシステムは既定のファイルシステムとして[NTFSを使用している](../Page/NT_File_System.md "wikilink")。これらのシステムがFATを使っている場合、FreeDOSは同じパーティション上で共存できるが、NTFSを使っている場合は別々のパーティションにしなければならない。この場合、FreeDOS[カーネル](../Page/カーネル.md "wikilink")は[Windows NT Boot Loader設定ファイルの](../Page/NTLDR.md "wikilink")`boot.ini`か、あるいは[ReactOS](../Page/ReactOS.md "wikilink")の`freeldr.ini`を設定することで起動できる。

### 日本語の扱い

FreeDOS はおもに英語圏で開発されているため、日本語表示に必要なソフトウェアを含んでいない。[FreeDOS/Vページ](http://dos.minashiro.net/)では、FreeDOSを改造して日本語を扱う方法が紹介されている。 ただし、2006年6月11日以降、事実上メンテナンスが停止している。

## 脚注

<references/>

[Category:MS-DOS](https://ja.wikipedia.org/wiki/Category:MS-DOS "wikilink") [Category:フリーソフトウェアOS](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアOS "wikilink")

1.  <http://news.mynavi.jp/news/2016/12/27/067/>
2.  例外としてWindows for Workgroups 3.11はデバッグモードをサポートしておりこれをFreeDOS上でも動かすことができるが、このモードは以前のWindows標準モードよりもさらに制限されたものになっている。