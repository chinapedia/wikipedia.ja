> この記事は[NTLDR](https://ja.wikipedia.org/wiki/NTLDR)から翻訳されています。


**NTLDR**（NT Loader）は過去の[Windows NT系における標準の](../Page/Windows_NT系.md "wikilink")[ブートローダ](https://ja.wikipedia.org/wiki/ブートローダ "wikilink")である。

## 概要

NTLDRはWindows NT系のブートローダであり、[Windows NT](../Page/Microsoft_Windows_NT.md "wikilink")/[2000](../Page/Microsoft_Windows_2000.md "wikilink")/[XP](../Page/Microsoft_Windows_XP.md "wikilink")/[Server 2003に付属した](../Page/Microsoft_Windows_Server_2003.md "wikilink")。

それより新しい[Windows Vistaおよびそれ以降はNTLDRの代わりに](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")[Windows Boot Managerが用いられている](https://ja.wikipedia.org/wiki/Windows_Boot_Manager "wikilink")。

NTLDRはプライマリ[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")かブート可能\[1\]なリムーバブルメディア（CD-ROM/USBメモリ/FDDなど）から起動することができる。もちろん、NTLDRはWindows NT系の[OSばかりではなく](../Page/オペレーティングシステム.md "wikilink")、[Windows 9x系や](../Page/Windows_9x系.md "wikilink")[PC-UNIX](https://ja.wikipedia.org/wiki/PC-UNIX "wikilink")（[Linux](../Page/Linux.md "wikilink")/[FreeBSD](../Page/FreeBSD.md "wikilink")など）などのWindows NT以外のOSも[パーティション](../Page/パーティション.md "wikilink")などを設定することにより起動することができる。NTLDRを使用するためには起動ドライブの[ルートディレクトリ](../Page/ルートディレクトリ.md "wikilink")に最低でも、NTLDRとBoot.iniを必要とする。また、NT系OSはそれに加えて、ntdetect.comも必要である。さらに、[日本語](../Page/日本語.md "wikilink")版を含む[東アジア](../Page/東アジア.md "wikilink")言語バージョンの Windows では Bootfont.bin が必要である\[2\]。

## 起動の順序

NTLDRは以下のようにOSを呼び出す。

1.  [マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")を32Bitモードに切り替える
2.  [ファイルシステム](../Page/ファイルシステム.md "wikilink")にアクセスする
3.  Boot.iniを読み込み、もし2種類以上OSが記述されていればブートメニューを出す。
4.  ブートメニューで選択されたOSがNT系以外のOSならば、NTLDRは記述されたファイルに起動を任せ、役割を終える。
      - ファイル名が指定されていない場合、BOOTSECT.DOSという名前のファイルが使用される。
      - /win95または/win95dosオプションが指定されている場合、[Windows 9x系と](../Page/Windows_9x系.md "wikilink")[DOS](../Page/DOS_\(OS\).md "wikilink")（[MS-DOS](../Page/MS-DOS.md "wikilink")または[PC DOS](https://ja.wikipedia.org/wiki/IBM_PC_DOS "wikilink")）とのマルチブートのための処理が実行される\[3\]。
5.  ブートメニューで選択されたOSがNT系のOSならば、NTLDRはntdetect.comを実行し、ハードウェアの情報収集をする。
6.  Windows NT系の[カーネル](../Page/カーネル.md "wikilink")である[ntoskrnl.exe](https://ja.wikipedia.org/wiki/ntoskrnl.exe "wikilink")を実行し、ntdetect.comで集めた情報を渡す。

## Boot.ini

NTLDRは\[operating systems\]の項目に2つ以上記述されていた場合、OSの選択画面を提示する。それを記述するファイルがBoot.iniである。

### Boot.iniの例

`[boot loader]`
`timeout=30`
`default=multi(0)disk(0)rdisk(0)partition(2)\WINDOWS`
`[operating systems]`
`multi(0)disk(0)rdisk(0)partition(2)\WINDOWS="Microsoft Windows XP Professional" /fastdetect`
`C:\bootsect.dos="Microsoft Windows 98"`

timeoutの値の単位は秒で、NTLDRのメニュー表示時間を設定できる。

### NT系OSの制御機能

NTLDRはNT系のOSのセーフモード起動なども制御している。使用されるオプションは以下のとおりである。

  - /3gb
  - /basevideo
  - /baudrate=nnn
  - /bootlog
  - /burnmemory
  - /crashdebug
  - /debug
  - /debugport=comx
  - /fastdetect
  - /maxmem=nn
  - /nodebug
  - /noexecute=optin ([DEP](../Page/データ実行防止.md "wikilink"))
  - /noguiboot
  - /nopae
  - /noserialmice:comx
  - /numproc
  - /onecpu
  - /pae
  - /pcilock
  - /safeboot
  - /safeboot:dsrepair
  - /safeboot:minimal
  - /safeboot:minimal(alternateshell)
  - /safeboot:network
  - /usepmtimer
  - /sos
  - /win95
  - /win95dos
  - /year

## 脚注

<references />

## 関連項目

  - [Windows NT](../Page/Microsoft_Windows_NT.md "wikilink")
  - [Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink")
  - [Windows XP](../Page/Microsoft_Windows_XP.md "wikilink")

## 外部リンク

  - [Windows XP および Windows Server 2003 の Boot.ini ファイルで使用可能なスイッチ オプション](http://support.microsoft.com/kb/833721/ja)

[Category:Windows_NT系](https://ja.wikipedia.org/wiki/Category:Windows_NT系 "wikilink") [Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:ブート](https://ja.wikipedia.org/wiki/Category:ブート "wikilink")

1.  [Basic Input/Output Systemの対応が必要](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")
2.  [マイクロソフト　サポート　オンライン](http://support.microsoft.com/kb/919529/ja)　2011年1月29日閲覧
3.