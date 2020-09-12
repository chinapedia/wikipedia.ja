> この記事は[OpenRC](https://ja.wikipedia.org/wiki/OpenRC)から翻訳されています。


[UNIX](../Page/UNIX.md "wikilink")系のシステムで、**OpenRC**は依存関係ベースの[init](https://ja.wikipedia.org/wiki/init "wikilink")システムである。[systemd](https://ja.wikipedia.org/wiki/systemd "wikilink")に移行したディストリビューションの、initシステムの代替選択肢\[1\]\[2\]\[3\]であり、[NetBSD](../Page/NetBSD.md "wikilink")と[Gentoo](https://ja.wikipedia.org/wiki/Gentoo "wikilink")で活躍する開発者、Roy Marplesによって開発された\[4\]\[5\]。

OpenRCは[TrueOS](../Page/TrueOS.md "wikilink")\[6\]、[Gentoo Linux](../Page/Gentoo_Linux.md "wikilink")、[Alpine Linuxや他のUnix系システムにおいてデフォルトのinitシステムであり](https://ja.wikipedia.org/wiki/Alpine_Linux "wikilink")、[Devuan](https://ja.wikipedia.org/wiki/Devuan "wikilink")\[7\]などのシステムではオプションとして提供されている。

## 設計

OpenRCのコア部分は、依存関係の管理とinitスクリプトの解析を行う。OpenRCはランレベルをスキャンし、依存関係のグラフを作り、必要なサービスのスクリプトを開始する。スクリプトが開始されたあとはOpenRCは退出する。デフォルトでは、OpenRCは改変されたバージョンのstart-stop-daemonをデーモン管理に用いている\[8\]。

initスクリプトは、SysVinitで用いられるものと同様であるが、その作成の簡素化のため、いくつかの機能が提供されている。スクリプトは、start()、stop()、status()の状態が推定され、システムはデフォルトの機能を作るために既に宣言された変数を用いる\[9\]。依存機能は、SysVinitにおけるLSBヘッダーによってなされる他のサービスへの依存関係の宣言に用いられる。設定と動作機構は、conf.dディレクトリ中の設定ファイルとinit.dディレクトリ中のinitファイルに分離されている。

Openrc-initは最初、バージョン0.25において/sbin/initのオプションの代替物として登場した。SysVinitやBusyboxなどの他のinitもサポートされている\[10\]。

Supervise-daemonは、バージョン0.21において、OpenRCに監査機能を提供するために登場した。この機能はinitスクリプト中でデーモンの開始とモニタリングのために有効化される。runit\[11\]やs6\[12\]など他のデーモン監査もサポートされている。

## 機能

  - Linux、TrueOS、FreeBSD、NetBSDで移植可能
  - 並行したサービスの起動（デフォルトではオフになっている）
  - 依存関係ベースの起動
  - cgroups経由でのプロセスの分離\[13\]
  - サービスごとのリソースの制限（ulimit）
  - コードと設定の分離（init.d/conf.d）
  - 拡張可能な起動スクリプト
  - 状態の把握が可能なinitスクリプト
  - [Samba](../Page/Samba.md "wikilink")や[NFS](https://ja.wikipedia.org/wiki/NFS "wikilink")など複数のコンポーネントを開始する複雑なinitスクリプト
  - 自動による依存関係の計算と、サービスのオーダリング
  - モジュール化されたアーキテクチャとオプションのコンポーネントの分離（Cronやsyslogなど）
  - 高速で柔軟なネットワークの利用（VPNやブリッジなどを含む）
  - デバッグモード

## 脚注

## 外部リンク

  -
  - [gentoo.org Gitレポジトリ](https://gitweb.gentoo.org/proj/openrc.git)

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10. [OpenRC](http://wiki.gentoo.org/wiki/OpenRC)
11.
12.
13.