> この記事は[OpenVZ](https://ja.wikipedia.org/wiki/OpenVZ)から翻訳されています。


**OpenVZ**（オープンブイジー）は、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")をベースに開発された [Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink") (RHEL) 用の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) レベルの[サーバ](../Page/サーバ.md "wikilink")[仮想化](../Page/仮想化.md "wikilink")ソフト。

[Parallels Virtuozzo Containers](../Page/Parallels_Virtuozzo_Containers.md "wikilink") for Linuxのオープンソース版であり、1つの物理サーバ上に複数の独立したLinuxインスタンスを作成することができる。ただし、Linuxカーネルをすべてのインスタンスで共有するため、[Linux](../Page/Linux.md "wikilink")以外の環境（[Windowsなど](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")）を動作させることはできない。

## 特徴

[ハイパーバイザ](../Page/ハイパーバイザ.md "wikilink")型（ハードウェアレベル）の仮想化ソフトである[VMware](../Page/VMware.md "wikilink")や[Xenに比べて](../Page/Xen_\(仮想化ソフトウェア\).md "wikilink")[オーバーヘッド](https://ja.wikipedia.org/wiki/オーバーヘッド "wikilink")が少ないとされ、稼動させる環境数で勝っている。より高密度化できるため、[バーチャル・プライベート・サーバ](../Page/バーチャル・プライベート・サーバ.md "wikilink") (VPS) での使用において、コストダウンをはかることができる。

チェックポイントとライブマイグレーションにも対応している。ゲストOS（コンテナ）が稼働中のまま、別のマシンに移すことができる。simfsを利用した場合、メモリの内容などのみが保存され、[ファイルシステム](../Page/ファイルシステム.md "wikilink")の内容は保存されないが、ファイルシステムにploopを使った場合は[スナップショットを取ることができ](../Page/スナップショット_\(ファイルシステム\).md "wikilink")、その場合、ファイルシステムの内容を復元したり、変更差分だけを管理したりできる。

RHEL 5版では、[仮想メモリ単位でしかメモリの制限をかけられなかったが](../Page/仮想記憶.md "wikilink")、RHEL 6でLinux カーネル 2.6.32になり、[cgroups](https://ja.wikipedia.org/wiki/cgroups "wikilink")の開発が進み、VSwap\[1\] が使えるようになり、物理メモリやスワップメモリでも制限をかけられるようになった。コンテナ内で物理メモリが枯渇し、スワップメモリを使い始めても、ホストの物理メモリが余っている場合は、実際にはすぐにディスクへの書き出しが始まるわけではなく、人工的にコンテナの速度を遅くしスワップアウトをエミュレートし、本当にホストの物理メモリが枯渇したときに初めてディスクへの書き出しが始まる。

## 対応OS

公式には[Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink") (RHEL) にのみ対応している。RHELクローンの[CentOS](../Page/CentOS.md "wikilink")でも動作し、[Parallels Virtuozzo Containersの方ではCentOSも公式にサポートしている](../Page/Parallels_Virtuozzo_Containers.md "wikilink")。Linuxカーネルを改造しているため、ディストリビューションおよびそのバージョンに強く依存している。

[Ubuntu](../Page/Ubuntu.md "wikilink") 10.04または[Debian](../Page/Debian.md "wikilink") 6.0にインストールするには、RPMファイルをdebに変換することで可能\[2\]\[3\]。 元々のDebian 5.0、6.0ではパッケージに含まれているが、サポートが技術的に困難であるという理由から、Debian 7.0 ではパッケージを廃止予定\[4\]。Debianから派生している[Ubuntu](../Page/Ubuntu.md "wikilink")では8.04は含まれているが、10.04ではパッケージに含まれていない\[5\]。

ゲストOSの方は、主要な[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")に一通り対応している。

## カーネル

OpenVZの[カーネル](../Page/カーネル.md "wikilink")はLinuxカーネルをOpenVZコンテナをサポートするように修正を加えたものである。修正されたカーネルは仮想化、コンテナ同士の隔離、リソース管理、チェックポイントの機能を持つ。

### 仮想化と隔離

それぞれのコンテナは別々に分離されていて、大旨、隔離された物理サーバのように動く。以下の物をそれぞれ隔離して所有している。

  - ファイル
    システムライブラリ、アプリケーション、仮想化された/procや/sys、仮想化されたロックなど。
  - ユーザーとグループ
    それぞれのコンテナは独自のrootユーザーを持ち、ユーザーやグループは独立している。
  - プロセスツリー
    それぞれのコンテナは独立したプロセスを持ち、[プロセス](../Page/プロセス.md "wikilink")はinitの子プロセスとなっている。プロセスID (PID) は仮想化されており、init PIDはちゃんと1になっている。
  - ネットワーク
    ネットワークデバイスは仮想化されていて、固有の[IPアドレス](../Page/IPアドレス.md "wikilink")を持っていて、[iptables](https://ja.wikipedia.org/wiki/iptables "wikilink") やルーティングは独自のを持てる。
  - デバイス
    必要ならば、コンテナは[ネットワーク](../Page/コンピュータネットワーク.md "wikilink")[インタフェース](../Page/インタフェース_\(情報技術\).md "wikilink")、[シリアルポート](../Page/シリアルポート.md "wikilink")、ディスク[パーティション](../Page/パーティション.md "wikilink")などリアルデバイスにアクセスすることが出来る。
  - IPCオブジェクト
    共有メモリ、[セマフォ](../Page/セマフォ.md "wikilink")、[メッセージパッシングなども独立している](../Page/メッセージ_\(コンピュータ\).md "wikilink")。

## リソース管理

OpenVZのリソース管理は、ディスククォータ、[CPU](../Page/CPU.md "wikilink")スケジューラー、I/Oスケジューラー、ユーザービーンカウンタからなる。これらのリソースはコンテナが実行中に再起動することなしに変更することが可能。

### ディスククォータ

各コンテナは個別のディスククォータを持ち、ディスクブロック数とinode数（大旨、ファイル数になる）で管理される。コンテナ内では、標準的なツールでユーザーごとやグループごとにディスククォータをかけることも出来る。

### CPUスケジューラー

OpenVZのCPU スケジューラーは公平なスケジューリング戦略を2段階で実装している。

第1段階では、コンテナごとのcpuunit値に基づいて、スケジューラはCPUタイムスライスをどのコンテナに割り振るか決める。第2段階では、標準のLinuxのスケジューラがコンテナ内のどのプロセスを実行するか、Linuxのプロセス優先順位に基づいて決める。

コンテナごとに異なるcpuunit値を割り振ることが出来る。CPU利用時間はcpuunit値に比例して分配される。

全CPU 時間の10% など、厳密に限界値を設定することも出来る。

### I/Oスケジューラー

上記のCPUスケジューラー同様、OpenVZではI/O スケジューラーも同様に2段階で行っている。Jens AxboeのCFQ (Completely Fair Queuing) I/Oスケジューラーを利用している。

それぞれのコンテナはI/Oの優先順位を持っていて、利用可能なI/O帯域をその優先順位に基づいて分配する。それ故、一つのコンテナがI/Oを使い果たすということは出来なくなっている。ただし、simfsを使用した場合、ホスト側の[ext4](https://ja.wikipedia.org/wiki/ext4 "wikilink")などのジャーナリングがボトルネックとなって公平に分配できない場合がある。

### ユーザービーンカウンタ

ユーザービーンカウンタはコンテナごとに設定され、最低値と上限値を設定する。21項目ある。あらゆる側面で設定可能であり、コンテナがシステムリソースを使い果たすことを制限することが出来る。

以下は項目一覧。

  - 主要なパラメータ
      - numproc - プロセス数
      - numtcpsock - TCPソケット数
      - numothersock - TCP以外のソケット数
      - vmguarpages
  - 二次的なパラメータ
      - kmemsize - カーネル内のスワップ不可能メモリサイズ
      - tcpsndbuf - TCP送信バッファ
      - tcprcvbuf - TCP受信バッファ
      - othersockbuf - 他のソケットのバッファ
      - dgramrcvbuf - データグラム (UDP) 受信バッファ
      - oomguarpages
      - privvmpages
  - 補助的なパラメータ
      - lockedpages - スワップされないメモリ
      - shmpages - 共有メモリ
      - physpages - 物理メモリサイズ
      - numfile - オープンファイル数
      - numflock - ファイルロック数
      - numpty - pty数
      - numsiginfo - siginfo数
      - dcachesize
      - numiptent - NETFILTER (IPパケットフィルタリング)数
      - swappages - スワップメモリサイズ

## ライセンス

OpenVZは、[GPLバージョン](../Page/GNU_General_Public_License.md "wikilink")2に基づいて配布されている。同技術を使用した商用ソフトとして[パラレルス](../Page/パラレルス.md "wikilink")が販売する[Parallels Virtuozzo Containers](../Page/Parallels_Virtuozzo_Containers.md "wikilink") for Linuxがある。

## 脚注

<references />

## 関連項目

  - [Parallels Virtuozzo Containers](../Page/Parallels_Virtuozzo_Containers.md "wikilink")
  - [Parallels Workstation](../Page/Parallels_Workstation.md "wikilink"), [Parallels Desktop](https://ja.wikipedia.org/wiki/Parallels_Desktop "wikilink")
  - [Xen](../Page/Xen_\(仮想化ソフトウェア\).md "wikilink")
  - [libvirt](https://ja.wikipedia.org/wiki/libvirt "wikilink")
  - [LXC](https://ja.wikipedia.org/wiki/LXC "wikilink")
  - [Linux-VServer](../Page/Linux-VServer.md "wikilink")

## 外部リンク

  - [OpenVZ公式サイト](http://openvz.org/)

[Category:エミュレーションソフトウェア](https://ja.wikipedia.org/wiki/Category:エミュレーションソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")

1.  [VSwap - OpenVZ Linux Containers Wiki](http://wiki.openvz.org/VSwap)
2.  [Install kernel from RPM on Ubuntu 10.04 - OpenVZ Linux Containers Wiki](http://wiki.openvz.org/Install_kernel_from_RPM_on_Ubuntu_10.04)
3.  [Install kernel from RPM on Debian 6.0 - OpenVZ Linux Containers Wiki](http://wiki.openvz.org/Install_kernel_from_RPM_on_Debian_6.0)
4.  [Bug\#642380: Cannot chkpnt (live migrate) VEs - linux.debian.kernel](http://groups.google.com/group/linux.debian.kernel/msg/f640f1ca643d7dd7)
5.  [OpenVZ - Community Ubuntu Documentation](https://help.ubuntu.com/community/OpenVZ)