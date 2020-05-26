> この記事は[Procfs](https://ja.wikipedia.org/wiki/Procfs)から翻訳されています。


**procfs**は、[Process](../Page/プロセス.md "wikilink") [Filesystem](../Page/ファイルシステム.md "wikilink") の略で、[Unix系](../Page/Unix系.md "wikilink")システムにある擬似ファイルシステム。主にプロセスに関する[カーネル](../Page/カーネル.md "wikilink")情報にアクセスする手段を提供する。procfs は実際のファイルシステムではないので、ディスクスペースを消費しないし、メモリもごくわずかしか消費しない。

通常、procfs は立ち上げ時に `/proc` ディレクトリにマウントされる。[Solaris](../Page/Solaris.md "wikilink")、[BSD](../Page/BSD.md "wikilink")、[Linux](../Page/Linux.md "wikilink")、[AIX](../Page/AIX.md "wikilink")、[QNX](../Page/QNX.md "wikilink")などでサポートされ、特にLinuxではプロセス関連以外のデータにも拡張されている（AIXのprocfsはLinuxベース）。procfs は機能を[カーネルモード](https://ja.wikipedia.org/wiki/カーネルモード "wikilink")から[ユーザーモード](https://ja.wikipedia.org/wiki/ユーザーモード "wikilink")に移すことに重要な役割を果たしている。例えば [GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")版の `ps`コマンドは全てのデータを procfs から得ており、特別なシステムコールを使用しない。

## 歴史

Tom J. Killian は [Version 8 Unix](../Page/Research_Unix.md "wikilink") 上に `/proc` を実装し\[1\]、[1984年](../Page/1984年.md "wikilink")6月、[USENIX](../Page/USENIX.md "wikilink")で *Processes as Files* という題の論文を発表した。これは、プロセスのトレースを行う *[ptrace](https://ja.wikipedia.org/wiki/ptrace "wikilink")* システムコールを置き換える目的で設計された。

Roger Faulkner と Ron Gomes は V8 `/proc` を [SVR4](https://ja.wikipedia.org/wiki/SVR4 "wikilink") に移植し、[1991年](../Page/1991年.md "wikilink")1月、USENIX で *The Process File System and Process Model in UNIX System V* という論文を発表した。この procfs は `ps`コマンドの実装に使える程度の機能を有するようになったが、procfs内のファイルには `read()`、`write()`、`ioctl()` といったシステムコールしか使えなかった。

[Plan 9で実装された](../Page/Plan_9_from_Bell_Labs.md "wikilink") procfs は V8 のものよりずっと進化していた。V8 の procfs では、あるプロセスに関する機能はひとつのファイルへの操作で実現されていた。Plan 9 は、それを複数のファイルに機能毎に分割し、procfs をよりファイルシステムらしくした。

[4.4BSDで実装された](../Page/BSD.md "wikilink") procfs はプロセス毎のサブディレクトリがあり、プロセスのメモリ、レジスタ、現在ステータスにアクセスすることができた。Solaris 2.6 の procfs もプロセス毎のディレクトリがあり、制御用の *ctl* ファイルが用意され、トレースやプロセス毎の操作ができるようになっていた。

## Linux

Linux では、procfs は動作中プロセスに関する情報を `/proc/`*[`PID`](../Page/プロセス識別子.md "wikilink")* というディレクトリで提供し、以下のような情報を提供する。

  - `/proc/`*`PID`*`/cmdline` - そのプロセスを起動した際のコマンド行文字列
  - `/proc/`*`PID`*`/cwd` - そのプロセスの[カレントディレクトリ](https://ja.wikipedia.org/wiki/カレントディレクトリ "wikilink")への[シンボリックリンク](../Page/ソフトリンク.md "wikilink")
  - `/proc/`*`PID`*`/environ` - そのプロセスの設定している環境変数とその中身
  - `/proc/`*`PID`*`/exe` - 元々の[実行ファイル](../Page/実行ファイル.md "wikilink")へのシンボリックリンク（もしあれば。プロセスは元々の実行ファイルが削除/移動された後も動作し続けることがある）
  - `/proc/`*`PID`*`/fd` - オープンしている[ファイル記述子](../Page/ファイル記述子.md "wikilink")に対応したシンボリックリンク群のあるディレクトリ
  - `/proc/`*`PID`*`/fdinfo` - オープンしているファイル記述子に対応したファイルの位置やフラグを記したファイル群があるディレクトリ
  - `/proc/`*`PID`*`/root` - そのプロセスにとってのルートディレクトリへのシンボリックリンク。通常は / だが、[chroot](https://ja.wikipedia.org/wiki/chroot "wikilink")している場合は異なる。
  - `/proc/`*`PID`*`/stat` - プロセスの状態についての情報（40個以上の値を含む。psコマンドはこのファイルから情報を得ている）
  - `/proc/`*`PID`*`/status` - プロセスの動作状態やメモリ使用状況についての基本情報
  - `/proc/`*`PID`*`/task` - そのプロセスを親プロセスとしている全プロセスへの[ハードリンク](../Page/ハードリンク.md "wikilink")を格納したディレクトリ
  - `/proc/`*`PID`*`/maps` - そのプロセスの仮想アドレス空間のマッピング状況（アドレス範囲とマッピングされているリソース）

特定のプロセスの[PIDは](../Page/プロセス識別子.md "wikilink")、[`pgrep`](https://ja.wikipedia.org/wiki/pgrep "wikilink")、[`pidof`](https://ja.wikipedia.org/wiki/pidof "wikilink")、[`ps`](../Page/Ps_\(UNIX\).md "wikilink") といったユーティリティで得られる。

``` bash
$ ls -l /proc/$(pgrep -n python)/fd        # 最近起動された `python' というプロセスの全ファイル識別子を一覧表示
samtala 0
lrwx------ 1 baldur baldur 64 2011-03-18 12:31 0 -> /dev/pts/3
lrwx------ 1 baldur baldur 64 2011-03-18 12:31 1 -> /dev/pts/3
lrwx------ 1 baldur baldur 64 2011-03-18 12:31 2 -> /dev/pts/3
$ readlink /proc/$(pgrep -n python)/exe    # 最近起動された `python' というプロセスの実行ファイルのパス名を表示
/usr/bin/python3.1
```

procfs では個々のプロセスとは直接関係しないシステム情報も提供するが、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink") 2.6 では大部分が別の擬似ファイルシステム *[sysfs](https://ja.wikipedia.org/wiki/sysfs "wikilink")* に分離移動されている（`/sys` にマウントされる）。

  - `/proc/acpi` または `/proc/apm` - パワーマネジメント関連情報
  - `/proc/buddyinfo` - [バディブロック・アルゴリズムに関する情報](https://ja.wikipedia.org/wiki/動的メモリ確保#バディブロック "wikilink")\[2\]
  - `/proc/bus` - [PCI](../Page/Peripheral_Component_Interconnect.md "wikilink")/[USBなどの情報](../Page/ユニバーサル・シリアル・バス.md "wikilink")。`/sys/bus` の方が情報が豊富。
  - `/proc/fb` - 利用可能なフレームバッファの一覧
  - `/proc/cmdline` - カーネルに渡されたブートオプション文字列
  - `/proc/cpuinfo` - [CPU](../Page/CPU.md "wikilink")に関する情報（ベンダー、CPUファミリ、機種、クロック周波数、キャッシュサイズ、コア数など）\[3\]。[BogoMips](../Page/BogoMips.md "wikilink")の値もあるが、実際の性能を反映しているとは言えない。
  - `/proc/devices` - メジャーデバイス番号とデバイスグループの一覧
  - `/proc/diskstats` - 各論理ディスクデバイスの統計情報
  - `/proc/filesystems` - カーネルがサポートしているファイルシステムの一覧
  - `/proc/interrupts`, `/proc/iomem`, `/proc/ioports`, `/proc/irq` - 各種システム資源についての詳細情報
  - `/proc/meminfo` - メモリ使用状況の概要情報
  - `/proc/modules` - 現在ロードされているカーネルモジュールに関する情報
  - `/proc/mounts` - 現在マウントされているデバイスとマウントポイントの一覧（/proc/self/mounts へのシンボリックリンク）
  - `/proc/net` - ネットワークの[プロトコルスタック](../Page/プロトコルスタック.md "wikilink")に関する情報
  - `/proc/partitions` - 存在する[パーティション](../Page/パーティション.md "wikilink")についての各種情報
  - `/proc/scsi` - [SCSIまたは](../Page/Small_Computer_System_Interface.md "wikilink")[RAID](../Page/RAID.md "wikilink")コントローラで接続されているデバイスに関する情報
  - `/proc/self` - 現在動作中のプロセス（/procを見ているプロセス）の `/proc/`*`PID`*`/` へのシンボリックリンク
  - `/proc/swaps` - 使用中のスワップ領域の一覧
  - `/proc/sys` - 動的に変更可能なカーネルオプションへのアクセスを提供。
  - `/proc/sysvipc` - 共有メモリなど[IPCに関する情報](../Page/プロセス間通信.md "wikilink")
  - `/proc/tty` - （擬似）端末に関する情報
  - `/proc/uptime` - システム起動からの時間とアイドル状態だった時間（秒）
  - `/proc/version` - カーネルのバージョン番号、（カーネルビルドに使われた）[gccのバージョン番号など](../Page/GNUコンパイラコレクション.md "wikilink")

procfs を使用する Linux 上のユーティリティは procps パッケージに収められており、利用するには procfs が /proc にマウントされていなければならない。

## \*BSD

  - FreeBSD 及び OpenBSD ではデフォルトで procfs はマウントされない\[4\]。
  - NetBSD 及び DragonFlyBSD ではマウントされるが、ファイル構造が異なる。

## 脚注

## 参考文献

  - [Unix 8th Edition proc(2) manual page](http://man.cat-v.org/unix_8th/4/proc) - 最初のprocfs
  - [Plan 9 procfs manual page](http://man.cat-v.org/plan_9/3/proc) - Plan 9 で拡張されたprocfs
  - [Linux Manual Pages Proc(5)](http://manpages.courier-mta.org/htmlman5/proc.5.html) Linux のprocfsのマニュアル
  - [Documentation/filesystems/proc.txt](http://kernel.org/doc/Documentation/filesystems/proc.txt) procfs についてのLinuxカーネル文書

## 外部リンク

  - [A brief history of /proc](https://blogs.oracle.com/eschrock/entry/the_power_of_proc) Eric Schrock's Weblog
  - [Access the Linux kernel using the Procfs](http://www.ibm.com/developerworks/library/l-proc.html) An IBM developerWorks article by M. Tim Jones
  - [Linux-Filesystem-Hierarchy](http://tldp.org/LDP/Linux-Filesystem-Hierarchy/html/proc.html) Linux Documentation Project
  - [Creating and using proc files - an article from the Real-Time Embedded blog](http://www.rt-embedded.com/blog/archives/creating-and-using-proc-files/)
  - [Using the proc filesystem](http://www.petur.eu/blog/?p=320) An article by Pétur I. Egilsson

[Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:OSのカーネル](https://ja.wikipedia.org/wiki/Category:OSのカーネル "wikilink") [Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink")

1.  [proc(4) manual page on Version 8 Unix](http://man.cat-v.org/unix_8th/4/proc)
2.  [3.2.2. /proc/buddyinfo](http://www.centos.org/docs/5/html/5.2/Deployment_Guide/s2-proc-buddyinfo.html) CentOS 5.2
3.
4.  [Why is procfs deprecated in favor of procstat?](http://lists.freebsd.org/pipermail/freebsd-fs/2011-February/010760.html)