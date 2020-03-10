> この記事は[Filesystem in Userspace](https://ja.wikipedia.org/wiki/Filesystem_in_Userspace)から翻訳されています。


**Filesystem in Userspace** (**FUSE**) は[Unix系](../Page/Unix系.md "wikilink")コンピュータ[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")用の[ソフトウェアインタフェースである](../Page/インタフェース_\(情報技術\).md "wikilink")。権限を持たないユーザが[カーネル](../Page/カーネル.md "wikilink")コードを修正することなく独自の[ファイルシステム](../Page/ファイルシステム.md "wikilink")を作成できる機能を提供する。これは、ファイルシステムのコードを[ユーザ空間で実行することでなされるもので](https://ja.wikipedia.org/wiki/アドレス空間#ユーザ空間 "wikilink")、その際FUSEモジュールは実際のカーネルインタフェースへの「橋渡し」しか提供しない。

FUSEは[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であり、[GNU General Public Licenseと](../Page/GNU_General_Public_License.md "wikilink")[GNU Lesser General Public Licenseに基づきリリースされている](../Page/GNU_Lesser_General_Public_License.md "wikilink")。FUSEのシステムは元々[A Virtual Filesystem](http://sourceforge.net/projects/avf) (AVFS) の一部だったが、[SourceForge.net](https://ja.wikipedia.org/wiki/SourceForge.net "wikilink")上で独立したプロジェクトとして分離された。

FUSEは[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink") ([PUFFS](https://ja.wikipedia.org/wiki/Pass-to-Userspace_Framework_File_System "wikilink"))、[DragonFly BSD](https://ja.wikipedia.org/wiki/DragonFly_BSD "wikilink") (PUFFS)、[OpenSolaris](https://ja.wikipedia.org/wiki/OpenSolaris "wikilink")、、[Android](../Page/Android.md "wikilink")、および[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")で利用できる\[1\]。FUSEはメインストリーム[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")ツリーに、カーネルバージョン2.6.14から公式にマージされた\[2\]。

[ISCライセンス](https://ja.wikipedia.org/wiki/ISCライセンス "wikilink")に基づきSylvestre Gallonが再実装したFUSEが[2013年](../Page/2013年.md "wikilink")[5月](https://ja.wikipedia.org/wiki/5月 "wikilink")にリリースされ\[3\]、同年[6月](../Page/6月.md "wikilink")に[OpenBSD](../Page/OpenBSD.md "wikilink")へと組み込まれた\[4\]。

## 仮想ファイルシステム

FUSEは[仮想ファイルシステム](https://ja.wikipedia.org/wiki/仮想ファイルシステム "wikilink")を書くために特に有用である。ディスクに対してデータを読み書きすることを基本とした伝統的なファイルシステムとは異なり、仮想ファイルシステムは実際にデータをファイルシステムに保存しない。それらは既存のファイルシステムやストレージデバイスのビューや翻訳として振舞う。

原則として、FUSE実装で利用可能なリソースはどれでもファイルシステムとしてエクスポート可能である。

## 移植

  - [FreeBSD用のFUSE](http://web.archive.org/web/20070411043200/http://fuse4bsd.creo.hu:80/)
  - [Fuse4X](http://fuse4x.org/)はmacOSへのFUSE移植（現在はOSXFuseへ統合）である。
  - [MacFUSE](http://code.google.com/p/macfuse/)はmacOSへの古いFUSE移植であるが、既にメンテナンスは終了している。
  - [OSXFuse](http://osxfuse.github.com/)はmacOSへのFUSE移植で、MacFUSEの後継である。
  - Windowsユーザモードファイルシステムライブラリである[Dokan](https://ja.wikipedia.org/wiki/Dokan "wikilink")と[fuse4win](http://hg.sharesource.org/fuse4win)はWindows用のFUSE APIである。
  - NetBSDは6.0より基盤システムによる[FUSEのサポート](http://netbsd.gw.com/cgi-bin/man-cgi?perfused+8+NetBSD-6.0)を開始した。
  - [MINIX 3はバージョン](https://ja.wikipedia.org/wiki/MINIX_3 "wikilink")3.2.0より基盤システムに[FUSEのサポート](http://wiki.minix3.org/doku.php?id=releases:3.2.0:start)を開始した。

## 利用例

  - [copy-fuse](https://github.com/copy-app/copy-fuse/) : Copy.comに保存されたファイルへのアクセス用の[Python](../Page/Python.md "wikilink") FUSEレイヤー。

  - [Wuala](../Page/Wuala.md "wikilink") : マルチプラットフォームで[Java](https://ja.wikipedia.org/wiki/Java "wikilink")ベースのOS統合[分散ファイルシステム](https://ja.wikipedia.org/wiki/分散ファイルシステム "wikilink")。ファイルシステム統合にFUSE、MacFUSE、および[Callback File System](http://www.eldos.com/cbfs/)のいずれかを使う。さらにファイルシステムに加え、Javaが動作する[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")からアクセス可能な、Javaベースのアプリケーションも統合する。

  - : [WebDAV](../Page/WebDAV.md "wikilink")、[SFTP](https://ja.wikipedia.org/wiki/SSH_File_Transfer_Protocol "wikilink")、[FTP](../Page/File_Transfer_Protocol.md "wikilink")、[FTPS](https://ja.wikipedia.org/wiki/FTPS "wikilink")、および[Amazon S3を実装する商用ファイルシステム](https://ja.wikipedia.org/wiki/Amazon_Simple_Storage_Service "wikilink")。

  - [jSYS](http://www.izysoftware.com/products/jsys/) : FUSEを利用したユーザ空間におけるjailsと仮想ファイルシステムを作成する商用ソフトウェア。

  - [Transmit](https://ja.wikipedia.org/wiki/Transmit "wikilink") : [MacFUSE](http://code.google.com/p/macfuse/)を通じてWebDAV、SFTP、FTP、およびAmazon S3サーバをFinder内のディスクとしてマウントできる機能も追加する商用FTPクライアント。

  - : FUSEを用いてSFTP/FTP/S3/Swiftを実装した商用ファイルシステム。

  - [VolatileFS](http://www.izysoftware.com/products/volatilefs/) : FUSEを利用した商用RAMディスク。

  - [GlusterFS](https://ja.wikipedia.org/wiki/GlusterFS "wikilink") : 数[ペタバイト](https://ja.wikipedia.org/wiki/ペタバイト "wikilink")までスケールアップ可能なクラスタ分散ファイルシステム。

  - : [SSH経由でリモートファイルシステムへのアクセスを提供する](../Page/Secure_Shell.md "wikilink")。

  -
  - [GmailFS](https://ja.wikipedia.org/wiki/GmailFS "wikilink") : [Gmail](https://ja.wikipedia.org/wiki/Gmail "wikilink")のメールとしてデータを保存するファイルシステム。

  - GAEDrive : [Google App Engineベースのネットワークストレージ](https://ja.wikipedia.org/wiki/Google_App_Engine "wikilink")。

  - [gae-filestore](http://code.google.com/p/gae-filestore/) : Google App Engineの仮想ファイルシステムライブラリ。

  - [GVfs](https://ja.wikipedia.org/wiki/GVfs "wikilink") : [GNOME](../Page/GNOME.md "wikilink")用仮想ファイルシステム。

  - [EncFS](https://ja.wikipedia.org/wiki/EncFS "wikilink") : 暗号化仮想ファイルシステム。

  - [NTFS-3G](https://ja.wikipedia.org/wiki/NTFS-3G "wikilink")と[Captive NTFS](https://ja.wikipedia.org/wiki/Captive_NTFS "wikilink") : [NTFSファイルシステムへのアクセスを可能にする](../Page/NT_File_System.md "wikilink")。

  - [fuse-exfat](https://github.com/relan/exfat) : オープンソースの[exFAT](https://ja.wikipedia.org/wiki/exFAT "wikilink")ファイルシステムの実装。ファイルシステムの作成と読み書きが可能。

  - [exFAT](http://code.google.com/p/exfat) : [マイクロソフト](../Page/マイクロソフト.md "wikilink")製で、exFATファイルシステムへの読み書きが可能となる。

  - [WikipediaFS](https://ja.wikipedia.org/wiki/WikipediaFS "wikilink") : Wikipediaの記事を実際のファイルのように参照し編集する。

  - [Lustre (ファイルシステム)](https://ja.wikipedia.org/wiki/Lustre_\(ファイルシステム\) "wikilink") : [サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")によるクラスタファイルシステム。FUSEを使ってユーザ空間で実行することが可能であり、FreeBSDへも移植されている\[5\]。ただしLustreの[ZFS](https://ja.wikipedia.org/wiki/ZFS "wikilink")-Linux移植版はユーザ空間内でZFSのDMU (Data Management Unit) を起動する\[6\]。

  -
  - [LoggedFS](http://loggedfs.sourceforge.net/) : ファイルシステムアクセスのロギング。

  - [HDFS](https://ja.wikipedia.org/wiki/Apache_Hadoop#Hadoop_Distributed_File_System_\(HDFS\) "wikilink") : [FUSE bindings](http://wiki.apache.org/hadoop/MountableHDFS)が[Hadoop分散ファイルシステム用に存在する](https://ja.wikipedia.org/wiki/Apache_Hadoop "wikilink")。

  - [mtpfs](http://www.adebenham.com/mtpfs/) : Creative Zen music playersのような[MTPデバイスをマウントする](https://ja.wikipedia.org/wiki/Media_Transfer_Protocol "wikilink")。

  - Sector File System : のSectorは大量の商品コンピュータ用に設計された分散ファイルシステムである。Sectorはマウント可能なローカルファイルシステムインタフェースを提供するためにFUSEを使う。

  - CurlFtpFS : [FTP](../Page/File_Transfer_Protocol.md "wikilink")/[SFTPロケーションにアクセスするためのファイルシステム](https://ja.wikipedia.org/wiki/SSH_File_Transfer_Protocol "wikilink")。

  - [fuse-ext2](http://sourceforge.net/projects/fuse-ext2/) : [オープンソース](../Page/オープンソース.md "wikilink")の[ext2](https://ja.wikipedia.org/wiki/ext2 "wikilink")/[ext3](https://ja.wikipedia.org/wiki/ext3 "wikilink")ファイルシステム。[MacFuse](http://code.google.com/p/macfuse/)を利用して[Mac OS X v10.4以降をサポートする](../Page/Mac_OS_X_v10.4.md "wikilink") ([Universal Binary](https://ja.wikipedia.org/wiki/Universal_Binary "wikilink"))。

  - [Lessfs](http://www.lessfs.com/) : インラインのLinux用データ重複除外ファイルシステム。[LZOやQuickLZの圧縮および暗号化をサポートする](https://ja.wikipedia.org/wiki/Lempel-Ziv-Oberhumer "wikilink")。

  - （旧名 Kosmos filesystem）: FUSEを通じてマウントすることで、既存のLinuxユーティリティでCloudStoreへの通信できるようにとなる。

  - [SoundCloudFS](http://www.gurudigitalsolutions.com/projects/soundcloudfs) : LinuxシステムをSoundCloud streamsへマウントするためのオープンソースファイルシステム。ユーザがソフトウェアを選んでファイルを開くことが可能である。

  - (MooseFS) : 1つのリソースとして見える複数のサーバを拡張する、ペタバイトのデータを保存可能なオープンソース分散[フォールトトレラントファイルシステム](https://ja.wikipedia.org/wiki/フォールトトレラント設計 "wikilink")。

  - 　NagusFS : [Nagios](../Page/Nagios.md "wikilink")サービスのファイルシステム表現。

  - [NagiosFS](http://sourceforge.net/apps/mediawiki/fuse/index.php?title=NetworkFileSystems#NagiosFS) : 値をリモートでモニタリングするファイルシステム表現。

  - [CassandraFS](https://code.launchpad.net/cassandrafs) : Cassandra (cassandra.apache.org) 上のファイルシステム。

  - [ZFS](https://ja.wikipedia.org/wiki/ZFS "wikilink") : [ZFS-Fuse-Linux 実装](http://zfs-fuse.net/)

  - [fuse-zip](http://code.google.com/p/fuse-zip/) : ファイルシステムとしてzipファイルを利用できる（書き込みをサポートする）。

  - [OWFS](http://www.owfs.org) : ファイルシステムディレクトリ構造を通じて[1-Wire](https://ja.wikipedia.org/wiki/1-Wire "wikilink")デバイスへのアクセスを提供するOne-Wireファイルシステム。

  - [TrueCrypt](../Page/TrueCrypt.md "wikilink") : on-the-fly暗号化 (OTFE) を利用したソフトウェアアプリケーション。暗号化パーティションや完全なストレージデバイスの中だけではなく、ファイルの中にも仮想的な暗号化ディスクを作成できる。

  - [s3fs-FuseOverAmazonS3](http://code.google.com/p/s3fs/) : Amazon S3に裏打ちされたFUSEベースファイルシステム。ローカルファイルシステムの読み書き用にバケットをマウントする。ファイルやフォルダをネイティブにかつAWS上に透過的に保存する。

  - [s3fs-c](https://github.com/tongwang/s3fs-c) : Amazon S3に裏打ちされたファイルシステム。s3fsからフォークされAWS Management Consoleのような他のS3クライアントと互換性を保つよう書き換えられている。

  - [LR|FS](http://www.formal.ie/fs) : [Adobe Lightroom](http://www.adobe.com/products/photoshoplightroom/)カタログ用のmacOSファイルシステム。MacFuseが必要。

  - [boxfs](http://code.google.com/p/boxfs/) : [box.net](https://ja.wikipedia.org/wiki/box.net "wikilink")アカウント上のファイルにアクセスするためのファイルシステム。

  - [remotefs](http://remotefs.sourceforge.net/) : ホームNASで利用するために設計されたネットワークファイルシステム。

  - [virtualbox-fuse](http://packages.ubuntu.com/search?keywords=virtualbox-fuse) : Virtualbox VDIイメージのマウントが可能となる。

  - [UsiFe](http://www.cse.iitd.ac.in/~srsarangi/software.html) : イントラファイルの暗号化を可能とする、柔軟性のあるファイルシステム。ファイルの一部を選んで暗号化と復号を行い、それらを表示できる。

  - [PyMMBfuse](http://projects.tlspu.com/PyMMB) : PyMMBプロジェクト用FUSEドライバ。MMCフラッシュカード上のBBC Microcomputeディスクイメージへのアクセスが可能となる。

  - [djmount](http://djmount.sourceforge.net) : UPnP AVデバイスのメディアコンテンツをマウントする。

## 関連項目

  - [9P](https://ja.wikipedia.org/wiki/9P "wikilink") - Plan 9オペレーティングシステム由来のファイルプロトコルで、FUSEよりも先に産みだされ同様の機能を数多く提供する。
  - [Installable File System](https://ja.wikipedia.org/wiki/Installable_File_System "wikilink")

## 脚注

## 外部リンク

  -
  - [Develop your own filesystem with FUSE](http://www.ibm.com/developerworks/linux/library/l-fuse/) - Sumit Singhによる。

  - [List of FUSE filesystems](http://apps.sourceforge.net/mediawiki/fuse/index.php?title=FileSystems)

  - [Crossmeta](http://www.crossmeta.org/redmine) FUSE Kernel for Windows is a true port of Fuse 2.8

  - [Callback File System](http://www.eldos.com/cbfs/) - このSDKにより開発者がユーザモードでWindows用の仮想ファイルシステムを作成できるようになる。

  - [Documentation/filesystems/fuse.txt](http://lxr.linux.no/#linux+v2.6.34/Documentation/filesystems/fuse.txt) - Linuxソースツリーのドキュメント。

[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  <http://osxfuse.github.io/>
2.  <http://www.linux.com/archive/feature/47839>
3.  <http://openbsd.7691.n7.nabble.com/Fuse-and-sshfs-support-for-OpenBSD-td224422.html>
4.  <http://marc.info/?l=openbsd-cvs&m=137027468819965>
5.
6.