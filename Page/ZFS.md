> この記事は[ZFS](https://ja.wikipedia.org/wiki/ZFS)から翻訳されています。


**ZFS**は、主に[オラクルの](../Page/オラクル_\(企業\).md "wikilink")[Solaris](../Page/Solaris.md "wikilink")上で実装されている[128ビット](https://ja.wikipedia.org/wiki/128ビット "wikilink")・アドレッシングを特徴とする[ファイルシステム](../Page/ファイルシステム.md "wikilink")。今までSolaris (SunOS) で用いられてきた [Unix File System](../Page/Unix_File_System.md "wikilink") (UFS) の次世代ファイルシステムと位置づけられている。名称は*Zettabyte File System*に由来する\[1\]が、現在は何の略称でもないとされる\[2\]。

## 概要

[2004年](../Page/2004年.md "wikilink")[9月](../Page/9月.md "wikilink")にアナウンスがあり、[2005年](../Page/2005年.md "wikilink")[11月](../Page/11月.md "wikilink")リリースのOpenSolaris build 27で実装が公開された。 "[Common Development and Distribution License](../Page/Common_Development_and_Distribution_License.md "wikilink")" (CDDL) のもと、[オープンソース](../Page/オープンソース.md "wikilink")で開発されている。

特徴として以下の項目が挙げられる。

  - [チェックサム](../Page/チェックサム.md "wikilink")が[64ビット](../Page/64ビット.md "wikilink")化された
  - [コピーオンライト](../Page/コピーオンライト.md "wikilink")の実装
  - ボリュームマネージャが必要なく、ボリュームの構成が容易にできるようになった
  - ディスクの違い（容量、種類）を吸収する仮想ボリューム（ストレージプールと呼称）をサポート
  - ストレージプールの作成・フォーマット・マウントがコマンド一行ですむ
  - ファイルシステム自身が[RAID](../Page/RAID.md "wikilink")機能を持つ

またSolaris10 11/06版より以下の機能が加わった。

  - [RAID](../Page/RAID.md "wikilink")-Z2（ダブルパリティによるRAID-6相当の機能）
  - [ホットスペア](https://ja.wikipedia.org/wiki/ホットスペア "wikilink")
  - クローンプロモーション（アクティブなZFS領域を複製と置換を容易にする機能）
  - 再帰的スナップショットコマンドの簡素化オプション

以下に記載されていない機能追加として、Oracle Solaris Solaris SRU 11.2.8.4.0などより、Persistant L2ARC (ブートをまたがるL2ARCの内容の再利用）が追加されている（他の環境での実装状況を記載する必要あり） 。

以降の追加機能は下記のバージョン番号を参照。

### バージョン番号

利用可能な形式と特徴を指定するために、新機能が導入されるに従ってZPoolとZFSのバージョン番号が増える。バージョン番号の一覧は以下の通り\[3\]。（\[\]内はサポートしている[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")）

  - 1 Initial ZFS version \[Supported by Solaris 10 06/06\]
  - 2 Ditto blocks (replicated metadata) \[Supported by Solaris 10 06/06 build 09\]
  - 3 Hot spares and double parity RAID-Z \[Supported by Solaris 10 11/06\]
  - 4 zpool history \[Supported by Solaris 10 08/07\]
  - 5 Compression using the gzip algorithm
  - 6 bootfs pool property \[Supported by FreeBSD 7.0\]
  - 7 Separate intent log devices
  - 8 Delegated administration \[Supported by Solaris 10 10/08\]
  - 9 refquota and refreservation properties
  - 10 Cache devices
  - 11 Improved scrub performance
  - 12 Snapshot properties
  - 13 snapused property \[Supported by OpenSolaris 2008.11, FreeBSD 8.0\]
  - 14 passthrough-x aclinherit \[Supported by OpenSolaris 2009.06, FreeBSD 8.1\]
  - 15 user/group space accounting \[Supported by Solaris 10 10/09, FreeBSD 8.2, FreeBSD 8-STABLE\]
  - 16 stmf property support
  - 17 Triple-parity RAID-Z
  - 18 Snapshot user holds
  - 19 Log device removal
  - 20 Compression using zle (zero-length encoding)
  - 21 Deduplication
  - 22 Received properties \[Supported by Solaris 10 9/10\]
  - 23 Slim ZIL
  - 24 System attributes
  - 25 Improved scrub stats
  - 26 Improved snapshot deletion performance
  - 27 Improved snapshot creation performance
  - 28 Multiple vdev replacements \[Supported by FreeBSD 9-CURRENT\]
  - 29 RAID-Z/mirror hybrid allocator \[Supported by Solaris 10 8/11\]
  - 30 ZFS data set encryption
  - 31 Improved 'zfs list' performance \[Supported by Solaris 11 Express b151a\]
  - 32 One MB blocksize
  - 33 Improved share support \[Supported by Solaris 11 EA b173\]
  - 34 Sharing with inheritance \[Oracle Solaris 11.1 or later\]
  - 35 Sequential resilver \[Oracle Solaris 11.2 or later\]
  - 36 Efficient log block allocation \[Oracle Solaris 11.3 or later\]
  - 37 lz4 compression
  - 38 xcopy with encryption \[Oracle Solaris 11.4 or later\]
  - 39 reduce resilver restart
  - 40 Deduplication 2
  - 41 Asynchronous dataset destroy
  - 42 Support for reguid
  - 43 RAID-Z enhancements and cloud device support
  - 44 Device Removal

今、自分のシステムでどのバージョンまでサポートしているか知りたい場合はzpool upgrade -vで確認できる。

## 訴訟合戦

[2007年](../Page/2007年.md "wikilink")[9月](../Page/9月.md "wikilink")、[ネットアップ](../Page/ネットアップ.md "wikilink")がZFSは自社の特許を侵害しているとして、開発した[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")を訴えた。[10月](https://ja.wikipedia.org/wiki/10月 "wikilink")にサン・マイクロシステムズは特許は無効と反訴。互いの経営者同士が自らの[ブログ](../Page/ブログ.md "wikilink")で応酬を繰り広げていたが、サンがオラクルに買収された後の[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[9月9日](../Page/9月9日.md "wikilink")、訴訟取り下げで合意した。

## キャパシティ

128ビット・アドレッシングで主な制限は以下の通り。

  - 16[エクサ](https://ja.wikipedia.org/wiki/エクサ "wikilink")[バイト](../Page/バイト_\(情報\).md "wikilink") — ファイルシステムの最大値
  - 16エクサバイト — 1ファイルの最大値

## プラットホーム

  - [Solaris](../Page/Solaris.md "wikilink")（10 6/06以降）
    10/08版よりブートパーティションとしても作成可能になった。

<!-- end list -->

  - [OpenSolaris](../Page/OpenSolaris.md "wikilink")→[OpenIndiana](https://ja.wikipedia.org/wiki/OpenIndiana "wikilink")
    [SPARC](../Page/SPARC.md "wikilink")及び[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")版のOpenSolaris build 27以降で動作する。2008.05版よりデフォルトファイルシステム。
    OpenIndianaは初期リリースoi_148からデフォルトファイルシステムである。

このほか、SunOS系列（[Illumos](https://ja.wikipedia.org/wiki/Illumos "wikilink")系統含む）ディストリビューションでもサポートされている。

### 移植

CDDLでライセンスされるオープンソースであり、Solaris系以外の[Unix系](../Page/Unix系.md "wikilink")オペレーティングシステムにも移植が進んでいる。

  - [FreeBSD](../Page/FreeBSD.md "wikilink")
    [x64](https://ja.wikipedia.org/wiki/x64 "wikilink")の9.0-RELEASEでZFS v28をサポートしている。[IA-32](../Page/IA-32.md "wikilink")でも一応動作するが、実用的に使うのは難しい（[カーネル](../Page/カーネル.md "wikilink")が多量のメモリを必要とするが、32ビット空間の限界がある等）。2011年2月28日時点ではカーネル側の未サポートが理由でiSCSIを経由した共有ZVOLs機能 (zfs set shareiscsi) は実現されていない。また10.x以降は[AFT](https://ja.wikipedia.org/wiki/AFT "wikilink")（4KB/セクタ）を自動的に認識してZFS poolを作成するようになった。
  - [NetBSD](../Page/NetBSD.md "wikilink")
    2007年の [Google Summer of Code](https://ja.wikipedia.org/wiki/Google_Summer_of_Code "wikilink") で開発が始められたが、2016年時点でメンテナンスされていない\[4\]。
  - [Mac OS X](https://ja.wikipedia.org/wiki/macOS "wikilink")
    [10.5 Leopardより搭載されているが](../Page/Mac_OS_X_v10.5.md "wikilink")、初期リリースの10.5.0では読み込みのみの対応にとどまる。[10.6 Snow Leopard](../Page/Mac_OS_X_v10.6.md "wikilink") では、サーバ版で標準対応することが発表されていたものの10.6.1 リリースでも実現せず、結局[アップルはZFSプロジェクトを停止した](../Page/アップル_\(企業\).md "wikilink")\[5\]。[Btrfs](https://ja.wikipedia.org/wiki/Btrfs "wikilink")を開発中のオラクルによるサン・マイクロシステムズ買収に伴いZFSの将来が不透明になったためと報じられている。ただしアップルの援助が止まっただけであり、プロジェクト自体はGoogle Codeにホスティングを移して、細々とではあるが続いている[1](http://code.google.com/p/maczfs/)。
  - [Linux](../Page/Linux.md "wikilink")
    CDDLがGPLに抵触するというライセンスの問題があり、また、ZFSの権利を保有するオラクルの姿勢を踏まえ、Linuxの生みの親[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")がカーネルへマージしない姿勢を表明している為\[6\]、Linuxではカーネル空間に統合された手法での利用は出来ない。
    [FUSEというユーザー空間のファイルシステムドライバを利用する形での実装例は存在しているが](../Page/Filesystem_in_Userspace.md "wikilink")、ユーザー空間の実装であるため、一部の機能は制限される。この実装は2006年のGoogle Summer Codeから始まっている。zfs-fuseの名称で、[Red Hat Enterprise LinuxのEPELや](../Page/Red_Hat_Enterprise_Linux.md "wikilink")[Ubuntu](../Page/Ubuntu.md "wikilink") 10.04以降など各種[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")に含まれている。
    2010年頃から別個に2本のネイティブポート版開発プロジェクトが動いており、そのうちKQ infotechのパッケージは[POSIX](../Page/POSIX.md "wikilink")準拠である。
    また**ZFS on Linux**と呼ばれるプロジェクトも進行しており\[7\]、[Debian](../Page/Debian.md "wikilink") / [CentOS](../Page/CentOS.md "wikilink") / [Ubuntu](../Page/Ubuntu.md "wikilink") / [Fedora](../Page/Fedora.md "wikilink")などといったLinuxディストビューションでZFSを用いることができる。
    Ubuntu 16.04にてZFSを正式採用することが発表された\[8\]。

## 脚注

## 外部リンク

  - [OpenSolaris Community Group zfs Pages](http://hub.opensolaris.org/bin/view/Community+Group+zfs)
  - [Solaris 10ファイルシステムZFS誕生エピソード『心を解き放て！』](http://jp.sun.com/communities/0612/feature01.html)
  - [ZFS - FreeBSD Wiki](http://wiki.freebsd.org/ZFS)
  - [Native ZFS for Linux](http://zfsonlinux.org/)
  - [OpenZFS](http://www.open-zfs.org/wiki/Main_Page)

[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:サン・マイクロシステムズ](https://ja.wikipedia.org/wiki/Category:サン・マイクロシステムズ "wikilink") [Category:2005年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2005年のソフトウェア "wikilink")

1.  [You say zeta, I say zetta (Jeff Bonwick's Blog)](https://blogs.oracle.com/bonwick/en_US/entry/you_say_zeta_i_say)
2.  [ZFS FAQ (Community Group zfs.faq) - XWiki](http://hub.opensolaris.org/bin/view/Community+Group+zfs/faq#HWhatdoesZFSstandfor)
3.
4.
5.  [](http://www.osnews.com/story/22388/Apple_Shuts_Down_Mac_OS_X_ZFS_Project)
6.  [Don't use ZFS ―Linus，ZFSをマージしない姿勢をあらためて強調](https://gihyo.jp/admin/clip/01/linux_dt/202001/10)
7.  <http://zfsonlinux.org/>
8.  <http://blog.dustinkirkland.com/2016/02/zfs-is-fs-for-containers-in-ubuntu-1604.html>