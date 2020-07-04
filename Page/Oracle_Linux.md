> この記事は[Oracle Linux](https://ja.wikipedia.org/wiki/Oracle_Linux)から翻訳されています。


**Oracle Linux**は、[オラクルによる](../Page/オラクル_\(企業\).md "wikilink")[Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink") (RHEL) をベースとした[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")(RHELクローン)の一つ。

## 概要

[CentOS](../Page/CentOS.md "wikilink")と同じようにRHELから商標やロゴの差し替えを行い、再構築したディストリビューションで、RHELとの互換を目標としている。Oracle製品に最適化したUnbreakable Enterprise Kernel(UEK)が利用できる。Oracle Unbreakable Linuxサポートプログラムにより比較的安価な価格で有償サポートを提供する。また、サポートサービスの利用を希望しない場合は、ユーザー登録を行うだけで無料で利用することも可能である。

[Oracle DatabaseやWeblogic](../Page/Oracle_Database.md "wikilink") Server などの自社製品の運用環境を提供することが目的の多くを占めており、同社のサーバー製品のExadataに採用されている。

一般的な意味では、[レッドハット](../Page/レッドハット.md "wikilink")による有償ディストリビューションRHELと、RHELをベースにしRHELとの互換環境を無償で実現しようとする[CentOS](../Page/CentOS.md "wikilink")や[Scientific Linuxなどのディストリビューションの間を埋める製品として](../Page/Scientific_Linux.md "wikilink")、RHELと同じバージョンや操作は必要だが安価なサポートを求める企業などを対象にしている。

なお、RHELではサポートされている[IA-64](../Page/IA-64.md "wikilink")アーキテクチャや[PowerPC](../Page/PowerPC.md "wikilink")アーキテクチャ向けのサポートは提供されておらず、[i386や](../Page/Intel_80386.md "wikilink")[x86-64といったPCアーキテクチャ向けのみに限られている](https://ja.wikipedia.org/wiki/x64 "wikilink")。また、CentOSなどとは異なり、デスクトップ向けのアプリケーションも標準ではインストールされないため、デスクトップ用途で利用する場合は、該当するパッケージを手動でインストールする必要がある。

## RHELとの互換性

オラクルは、Oracle Linuxを2つの異なった[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")とともに配布している。

  - *Red Hat Compatible Kernel*（RHCK） - RHELで配布されているのと同一のカーネル
  - *Unbreakable Enterprise Kernel*（UEK\[1\]） - より新しいメインラインのLinuxカーネルのバージョンを基にしている。オラクル自身による、[OLTP](https://ja.wikipedia.org/wiki/OLTP "wikilink")、[InfiniBand](../Page/InfiniBand.md "wikilink")、[SSD](../Page/SSD.md "wikilink")ディスクへのアクセス、[NUMA](../Page/NUMA.md "wikilink")最適化、RDS、asysn I/O、OCFS2、ネットワークなどに対する強化が加えられている\[2\]。

オラクルは、Unbreakable Enterprise Kernelは完全にRHELと互換性があると宣伝している。オラクルは、これはオラクルの[ミドルウェア](../Page/ミドルウェア.md "wikilink")やサードパーティの[RHEL](https://ja.wikipedia.org/wiki/RHEL "wikilink")認定アプリケーションをインストールし、実行することを許すとするが、どのようなリファレンスやサードパーティによる文書も提供されていない\[3\]。

## バージョン履歴

  - Oracle Linux 8, 8.1
  - Oracle Linux 7, 7.1, 7.2, 7.3, 7.4, 7.5, 7.6, 7.7\[4\]
  - Oracle Linux 6, 6.1, 6.2, 6.3, 6.4, 6.5, 6.6, 6.7, 6.8, 6.9\[5\]
  - Oracle Enterprise Linux 5, 5.1, 5.2, 5.3, 5.4, 5.5, 5.6, 5.7, 5.8, 5.9, 5.10, 5.11\[6\]
  - Oracle Unbreakable Linux 4.5, 4.6, 4.7, 4.8, 4.9\[7\]

## レッドハットの反応

Oracle Enterprise LinuxはRHELと直接競合する製品で、レッドハットから多くの顧客が流れる事が危惧された\[8\]。 これに対しレッドハットは、オラクルのEnterprise LinuxはRHELと完全な互換性がない事を発表し、オラクルに乗り換える場合の問題点を公表し対抗した\[9\]。

## 脚注

<div class="references-small">

<references responsive="" />

</div>

## 外部リンク

  - [Oracle Linux](https://www.oracle.com/jp/linux/index.html)

  -

[Category:オラクル](https://ja.wikipedia.org/wiki/Category:オラクル "wikilink") [Category:Linuxディストリビューション](https://ja.wikipedia.org/wiki/Category:Linuxディストリビューション "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.  [Oracle Linux with Oracle's Unbreakable Enterprise Kernel](http://www.oracle.com/us/technologies/linux/unbreakable-enterprise-kernel-ds-173416.pdf)
3.
4.  [Release Notes for Oracle Linux 7](http://docs.oracle.com/cd/E52668_01/E53499/html/index.html)
5.  [Index of /el6/docs](http://oss.oracle.com/el6/docs/)
6.  [Index of /el5/docs](http://oss.oracle.com/el5/docs/)
7.  [Index of /el4/docs](http://oss.oracle.com/el4/docs/)
8.  [ITmedia エンタープライズ：Red Hatを葬り去る？OracleがLinux自体のサポートに乗り出す](http://www.itmedia.co.jp/enterprise/articles/0610/26/news026.html)
9.  <http://www.jp.redhat.com/rhel/real/>