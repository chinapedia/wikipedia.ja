> この記事は[Wubi](https://ja.wikipedia.org/wiki/Wubi)から翻訳されています。


**Wubi** (**W**indows-based **Ub**untu **I**nstaller) は[Windows上で動作する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Ubuntu](../Page/Ubuntu.md "wikilink")公式の[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")インストーラー。UbuntuをWindowsの[ファイルシステム](../Page/ファイルシステム.md "wikilink")上に[インストール](../Page/インストール.md "wikilink")し、Ubuntuを利用することができる。[GPLで配布される](../Page/GNU_General_Public_License.md "wikilink")\[1\]。

## 概要

Wubiは独立したプロジェクトとして生まれ、バージョン7.04および7.10においては非公式にリリースされた\[2\]。 8.04からはUbuntu公式パッケージとなり、Ubuntu 8.04 alpha 5よりUbuntu LiveCDに同梱された\[3\]。WubiのみダウンロードしてUbuntuをインストールする場合は、WubiがUbuntu LiveCDのISOファイルのダウンロードを行い、そこからインストールを行うため、あらかじめLiveCDを用意する必要もなくなる。

プロジェクトの目標は、Ubuntuのインストール時に[パーティション](../Page/パーティション.md "wikilink")切り分けや[フォーマット](https://ja.wikipedia.org/wiki/フォーマット "wikilink")などで[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")上のデータを失うリスクを負うことなく、[Linux](../Page/Linux.md "wikilink")に慣れていないWindowsユーザーでもUbuntuを試せるようにすることである\[4\]。WubiはWindows上からUbuntuをアンインストールする事もできる。

WubiはWindowsブートメニューにUbuntu起動用エントリを追加する。UbuntuはWindowsファイルシステム上の1個のファイルとしてインストールされる（例: c:\\ubuntu\\disks\\root.disk）。このファイルはUbuntu側からは1個のディスクパーティションに見える\[5\]。WubiはまたスワップファイルもWindowsファイルシステム上に作成し（例: c:\\ubuntu\\disks\\swap.disk）、ホストOSの仮想メモリに追加する。このファイルはUbuntuからは増設メモリの様に見える\[6\]。

これは[仮想マシンではなく](../Page/仮想機械.md "wikilink")、[Topologilinux](https://ja.wikipedia.org/wiki/Topologilinux "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:Topologilinux "wikilink")) のように[ループバックデバイス](https://ja.wikipedia.org/wiki/ループバックデバイス "wikilink")（ディスクイメージ）上で独立して動作する。これはLinuxディストリビューションではなく、Ubuntuインストーラーである\[7\]。

WubiはUbuntuをLinux用のディスクパーティションに直接インストールしないが、[LVPM](https://ja.wikipedia.org/wiki/LVPM "wikilink") (Loopmounted Virtual Partition Manager) を使用して、Wubiで作成したUbuntu環境をLinux用ディスクパーティション（[USBフラッシュドライブを含む](https://ja.wikipedia.org/wiki/USBメモリ "wikilink")）から直接起動するネイティブ環境に移行できる\[8\]。このセットアップ方法の長所は利用者が直接ディスクパーティションにインストールする際のリスクを回避しつつ、OSやドライバの動作確認を行えることである。

インストールCDを利用せずに、標準インストールと同様にディスクパーティションにインストールする場合には[UNetbootin](https://ja.wikipedia.org/wiki/UNetbootin "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:UNetbootin "wikilink")) を使用する\[9\]。

関連したプロジェクトに、[Lubi](https://ja.wikipedia.org/wiki/Lubi "wikilink")がある。これはホストOSにWindowsの代わりにLinuxを使用するというものである\[10\]。[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")をホストに使用する[Mubi](https://ja.wikipedia.org/wiki/Mubi "wikilink")も将来サポートされる予定である\[11\]。

## デスクトップ

利用者はWubiインストール時に使用するデスクトップ環境に応じたUbuntu系ディストリビューションを選択する事ができる（[KDE](../Page/KDE.md "wikilink")であれば[Kubuntu](../Page/Kubuntu.md "wikilink")、[Xfce](../Page/Xfce.md "wikilink")であれば[Xubuntu](https://ja.wikipedia.org/wiki/Xubuntu "wikilink")）。通常のLinuxと同様にいずれのディストリビューションであっても他のデスクトップ環境を後でインストールすることにより、ログイン時にどのデスクトップ環境を使用するかを選択できる。

## 制限事項

  - [ハイバネーション](https://ja.wikipedia.org/wiki/ハイバネーション "wikilink")はサポートしていない\[12\]。
  - Wubiファイルシステムは通常のファイルシステムより、（電源プラグを抜くといったような）ハードリブートに対して脆弱である\[13\]。
  - WubiでUbuntuをWindowsと同じパーティションにインストールすると、[FAT32](https://ja.wikipedia.org/wiki/FAT32 "wikilink")/[NTFS](../Page/NT_File_System.md "wikilink") のファイル[フラグメンテーション](../Page/フラグメンテーション.md "wikilink")により、時間とともにUbuntuのパフォーマンスがわずかずつ劣化していく可能性がある。これはディスクの[デフラグメンテーション](../Page/デフラグメンテーション.md "wikilink")により緩和できる。

## 影響

Wubiは次の[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトの影響を受けている: [Debianインストーラ](https://ja.wikipedia.org/wiki/Debianインストーラ "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:Debian-Installer "wikilink")) 、[Migration-Assistant](https://ja.wikipedia.org/wiki/Migration-Assistant "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:Migration-Assistant "wikilink")) 、[Grub4Dos](https://ja.wikipedia.org/wiki/Grub4Dos "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:Grub4Dos "wikilink")) 、[NTFS-3G](https://ja.wikipedia.org/wiki/NTFS-3G "wikilink")、[NSIS](https://ja.wikipedia.org/wiki/NSIS "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:NSIS "wikilink")) および [Metalink](https://ja.wikipedia.org/wiki/Metalink "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:Metalink "wikilink"))。

## ハードウェアサポート

WubiおよびLubiは、8.04よりUbuntu i386（32ビット [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")）および [x64](https://ja.wikipedia.org/wiki/x64 "wikilink")版をサポートしている。

## 類似のプロジェクト

  - [andLinux](https://ja.wikipedia.org/wiki/andLinux "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:andLinux "wikilink")) : [Cooperative Linuxを利用してWindows上で動作する](../Page/Cooperative_Linux.md "wikilink")
  - [Topologilinux](https://ja.wikipedia.org/wiki/Topologilinux "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:Topologilinux "wikilink")) : Cooperative Linuxを利用してWindows上で動作する
  - [Instlux](https://ja.wikipedia.org/wiki/Instlux "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:Instlux "wikilink")) : [openSUSE](https://ja.wikipedia.org/wiki/openSUSE "wikilink") 10.3以降に含まれている\[14\]
  - [Win32-Loader](https://ja.wikipedia.org/wiki/Win32-Loader "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:Win32-loader_\(Debian\) "wikilink")) : [Debian](../Page/Debian.md "wikilink")のWindowsベースインストーラー。
  - [UNetbootin](https://ja.wikipedia.org/wiki/UNetbootin "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:UNetbootin "wikilink"))
  - [LinuxLive USB Creator](https://ja.wikipedia.org/wiki/LinuxLive_USB_Creator "wikilink") ([:en:LinuxLive USB Creator](https://ja.wikipedia.org/wiki/:en:LinuxLive_USB_Creator "wikilink"))

## 脚注

## 外部リンク

  - [Wubi 公式サイト](http://sourceforge.net/projects/wubi/)

[Category:Ubuntu](https://ja.wikipedia.org/wiki/Category:Ubuntu "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:システムソフトウェア](https://ja.wikipedia.org/wiki/Category:システムソフトウェア "wikilink")

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
14. [Instlux - openSUSE](http://en.opensuse.org/Instlux)