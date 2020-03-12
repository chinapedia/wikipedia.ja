> この記事は[PerfectDisk](https://ja.wikipedia.org/wiki/PerfectDisk)から翻訳されています。


**PerfectDisk**（パーフェクトディスク）は米Raxco SoftWareが開発している[Windows用](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[デフラグメンテーション](../Page/デフラグメンテーション.md "wikilink")ソフトである。

PerfectDisk 8 Proにて正式にWindowsVistaへの対応を果たした。2008年4月に発表されたPerfectDisk 2008では仮想環境であるVMware Workstation、VMware ServerのゲストOSにも対応した。 PerfectDisk 11からはSSDの最適化にも対応した。

## 概要

Windows標準搭載のデフラグ機能では不可能なシステムファイルや空き領域の最適化を行える強力なデフラグメンテーションソフトであり、標準デフラグ機能の完全版である[Diskeeper](../Page/Diskeeper.md "wikilink")と人気を2分するソフトウェアである。

WindowsはOS標準機能として簡易なデフラグメンテーションソフトを搭載しているが、動作に制限があるなど十分な機能とは言えない。そのためハイエンドユーザを中心に、より高機能なデフラグメンテーションソフトへのニーズがあり、それに応えるソフトウェアである。

PerfectDiskの開発元は米Raxco SoftWareであるが、日本ではネットジャパンがローカライズし販売を行っている。バージョン8よりネットジャパンのパーソナル向けブランドPowerXシリーズとして販売されている。バージョン10での対応OSはWindows Vista（32ビットおよび64ビット版の各エディション）、XP Home Edition/Professional（SP2以降）/Professional x64 Edition、2000 Professional（SP4以降）。また、アップデートによりWindows 7にも対応した。バージョン11での対応OSは、Windows 7 / Vista（32/64bit版の各エディション）Windows XP Home Edition/Professional（SP3以降）/ Professional x64 Edition（SP2以降）。このバージョンからWindows2000は非対応になった。

バージョン14で対応するファイルシステムは ReFS / FAT16 / FAT32 / NTFS / exFAT / Flash / USB / SSD Drives,and SAN/RAID/Mirrored Disks/Letter-less Drivesであり、バージョン14の（Raxco Softwareで発売している英語版の）プロダクト・レパートリーと各OSへの対応状況は、以下の通り。

  - PerfectDisk Pro…Windows10/8/8.1/7/Vista/XP,For Personal Users(3 PCまでのライセンスとTotal Home Licenseとで値段が若干異なる)
  - PerfectDisk Professional Business…Windows10/ 8/8.1/7/Vista/XP,For Business Users
  - PerfectDisk Home Server…Windows Home Server 2011 (WHS V2) and Server 2012 Essentials.
  - PerfectDisk Server…Physical Windows Server 2012/2012 R2/2008
  - PerfectDisk for vSphere…Windows guests running in a vSphere virtual environment
  - PerfectDisk Hyper-V…Windows guests running in a Hyper-V virtual environment

## 機能

  - SMART Placement最適化
    PerfectDisk独自の最適化方法。通常の断片化解消のほか、空き領域の結合、ファイルの書き換え頻度に応じて配置の変更を行い、以降の運用におけるファイルの断片化の発生を抑える。これによりドライブ上の断片化をほぼ完全に解消する。
  - 空き領域統合最適化
    通常の断片化解消と空き領域の結合は行うが、ファイルの配置の変更を省くことで最適化が短時間で終わるようにしたもの。
  - 最適化のみ
    通常の断片化解消のみを行い、更に最適化が短時間で終わるようにしたもの。
  - 単一ファイルの最適化
    指定したファイルのみを最適化する。特定のファイルをすぐに最適化したいときに使用する。
  - オフライン最適化
    ボリュームをアンマウントしてその場で、もしくはWindows起動時に最適化を行う。システムファイルの最適化に使用する。
  - AutoPilot
    スケジュールにしたがってデフラグの実行

[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:アプリケーションソフト_(製品)](https://ja.wikipedia.org/wiki/Category:アプリケーションソフト_\(製品\) "wikilink")