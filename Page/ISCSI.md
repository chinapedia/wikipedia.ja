> この記事は[ISCSI](https://ja.wikipedia.org/wiki/ISCSI)から翻訳されています。


[ISCSI_SAN_example.svg](https://ja.wikipedia.org/wiki/File:ISCSI_SAN_example.svg "fig:ISCSI_SAN_example.svg")  **Internet Small Computer System Interface** (**iSCSI、アイスカジー**) とは、[SCSIプロトコルを](../Page/Small_Computer_System_Interface.md "wikilink")[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")上で使用する規格である。[ファイバーチャネル](../Page/ファイバーチャネル.md "wikilink")よりも安価に[ストレージエリアネットワーク](../Page/ストレージエリアネットワーク.md "wikilink") (SAN) を構築出来る\[1\]。[2003年](../Page/2003年.md "wikilink")2月11日に[IETFによって](../Page/Internet_Engineering_Task_Force.md "wikilink")[RFCとして公表された](../Page/Request_for_Comments.md "wikilink")"公式な規格への提案" (Proposed standard) であり、SCSI-3標準の[トランスポート層](https://ja.wikipedia.org/wiki/トランスポート層 "wikilink")に相当する。[ギガビット・イーサネットが一般化した現在](https://ja.wikipedia.org/wiki/イーサネット#ギガビット・イーサネット "wikilink")、iSCSIベースのSANは十分高速・安価となり検討に値するものとなっている。

## 特徴

データ転送にTCP/IPを使う。[ストレージエリアネットワーク](../Page/ストレージエリアネットワーク.md "wikilink")(SAN)の基盤である[ファイバーチャネル](../Page/ファイバーチャネル.md "wikilink")と違い汎用な[イーサネット](../Page/イーサネット.md "wikilink")（またはTCP/IPが使用可能なネットワーク）があればよい。SANのコスト/互換性問題なしにメリットを享受できる。TCP/IPの[オーバヘッド](https://ja.wikipedia.org/wiki/オーバヘッド "wikilink")によりファイバーチャネルより性能が悪いという批判もある。しかし、[TCPオフロードエンジン](https://ja.wikipedia.org/wiki/オフロード_\(コンピュータ用語\)#TOE "wikilink") (TOE) のような新技術が影響を緩和する。市場は成長しており、ギガビットイーサネットや[10GbE](https://ja.wikipedia.org/wiki/10GbE "wikilink")の普及に伴い性能・使いやすさが向上している。ベンダーも [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")、SAN製品、ストレージシステムでiSCSIをサポートしてきている。従来のハードワイヤードのSCSIに比べ[セキュリティ](https://ja.wikipedia.org/wiki/セキュリティ "wikilink")・[可用性](https://ja.wikipedia.org/wiki/可用性 "wikilink")・[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")に優れている。既存のTCP/IP機材を流用できる優れた可搬性は設計開発段階からベンダーの注目を集めた。プロトコルの完成によってベンダーは直ちに製品を提供した。

## プロトコル階層

[ISCSI_Layers.gif](https://ja.wikipedia.org/wiki/File:ISCSI_Layers.gif "fig:ISCSI_Layers.gif") 下記の5層から構成される\[2\]。下位から順に、

  - [物理層](https://ja.wikipedia.org/wiki/物理層 "wikilink")、[リンク層](https://ja.wikipedia.org/wiki/データリンク層 "wikilink")

<!-- end list -->

  -
    [IEEE802.3](https://ja.wikipedia.org/wiki/IEEE_802 "wikilink") が使われる。これはイーサネットと同様のLANコネクタや物理現象が利用される事を意味する。[ファイバーチャネル・オーバー・イーサネット](https://ja.wikipedia.org/wiki/ファイバーチャネル・オーバー・イーサネット "wikilink")とは異なり10GbEは必須ではなく1GbEでも良い。

<!-- end list -->

  - IP層

<!-- end list -->

  -

    [ルーティング](../Page/ルーティング.md "wikilink")を可能にする。

<!-- end list -->

  - TCP層

<!-- end list -->

  -

    セッション保持や確実な[パケット](../Page/パケット.md "wikilink")到達を実現する。

<!-- end list -->

  - iSCSI層

<!-- end list -->

  -
    SCSI層からの[SCSIコマンド](https://ja.wikipedia.org/wiki/SCSIコマンド "wikilink")を受けiSCSI Protocol Data Unit (PDU)\[3\]を作成(カプセル化)し下位層へ渡す\[4\]。

<!-- end list -->

  - SCSI層

<!-- end list -->

  -
    SCSIコマンドが使われる事を意味する。

## 記憶装置

ホストはiSCSIイニシエータ ([Small Computer System Interface](../Page/Small_Computer_System_Interface.md "wikilink") 参照) をサポートしている必要がある。ホストはこれを使って遠隔にある[ディスクや](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")[テープのような対象記憶装置](https://ja.wikipedia.org/wiki/テープドライブ "wikilink") (target) に接続する。ドライバやアプリケーションから見れば記憶装置はローカルにSCSIで接続されているのと同じに見える。ホストやtargetが複数存在する複雑な環境は[ストレージエリアネットワーク](../Page/ストレージエリアネットワーク.md "wikilink")(SAN)となる。iSCSIは[ネットワークアタッチトストレージ](../Page/ネットワークアタッチトストレージ.md "wikilink") (NAS) とは異なる事に留意する。イーサネットを使うという点では共通であるが、NASは複数ホストからの同時アクセスを仲裁するためのソフトウェアを内蔵してファイル共有を行う役割でありiSCSIの目的(ストレージプールの共有)とは異なる。

## サポート状況

### イニシエータ

#### OSのサポート

| OS名                                                                                                           | リリース時期   | バージョン                                    |
| ------------------------------------------------------------------------------------------------------------- | -------- | ---------------------------------------- |
| [AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")                                                           | 2002年10月 | AIX 5.2                                  |
| [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")                                         | 2003年6月  | 2000, XP Pro, 2003, Vista,2008,7,2008 R2 |
| \! style="text-align:left; background:\#ececec" | [NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink") | 2003年8月  | NetWare 6.5                              |
| [HP-UX](../Page/HP-UX.md "wikilink")                                                                          | 2003年10月 | HP 11i v1, HP 11i v2                     |
| [Solaris](../Page/Solaris.md "wikilink")                                                                      | 2005年2月  | Solaris 10                               |
| [Linuxカーネル](../Page/Linuxカーネル.md "wikilink")                                                                  | 2005年6月  | 2.6.12                                   |
| [NetBSD](../Page/NetBSD.md "wikilink")                                                                        | 2007年12月 | 4.0                                      |
| [FreeBSD](../Page/FreeBSD.md "wikilink")                                                                      | 2008年2月  | 7.0                                      |
| [VMware ESX Server](../Page/VMware.md "wikilink")                                                             | 2006年6月  | 3.0.0                                    |

#### ソフトウェア

  - [Cisco](https://ja.wikipedia.org/wiki/シスコシステムズ "wikilink") iSCSI ドライバー - 最初期のソフトウェア iSCSI イニシエータのひとつ。[HP-UX](../Page/HP-UX.md "wikilink"), [AIX](https://ja.wikipedia.org/wiki/AIX "wikilink"), [Linux](../Page/Linux.md "wikilink"), [Solaris](../Page/Solaris.md "wikilink"), [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") NT4/2000 をサポート。 最近ではCisco SAN-OS の名称でファイバーチャネルも含めたSAN全般をサポートする体系に組み込まれている\[5\]。
  - [IBM](../Page/IBM.md "wikilink") iSCSI ソフトウェアイニシエータ for AIX - バージョン 5.2 (2002年10月) から対応
  - [FreeBSD](../Page/FreeBSD.md "wikilink") - バージョン 7.0 (2008年2月) から対応
  - [HP](../Page/ヒューレット・パッカード.md "wikilink") HP-UX iSCSI ソフトウェアイニシエータ\[6\]
  - Linux
      - Core-iSCSI - 商用の PyX イニシエータの GPL部分に基づくイニシエータ。Open-iSCSI の開発のために Linux-iSCSI の保守が停止した際にギャップを埋める目的で Linuxカーネル 2.6 向けに復活したプロジェクトである\[7\]。
      - Intel-iSCSI ([インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")) - 概念実証用にインテルからLinux向けにリリースされたiSCSIイニシエータとターゲット。(sourceforge上では削除済み？)
      - Linux-iSCSI - Cisco Linux iSCSI ドライバーに基づくイニシエータ。2005年4月現在Linux-iSCSI と Open-iSCSI の開発者は共同で作業して Open-iSCSI の強化に努めている\[8\]。3.xx シリーズは Linuxカーネル 2.4 をサポート。4.xx シリーズは Linuxカーネル 2.6 から 2.6.9 までをサポート。
      - Open-iSCSI - 最新のイニシエータであり2.6.11 以降をサポート。この開発のためLinux-iSCSI の開発は停止した\[9\]。
      - UNH-iSCSI - [ニューハンプシャー大学](https://ja.wikipedia.org/wiki/ニューハンプシャー大学 "wikilink") (UNH) によるイニシエータとターゲットの実装\[10\]。
  - [マイクロソフト](../Page/マイクロソフト.md "wikilink") iSCSI ソフトウェアイニシエータ for Microsoft Windows - [Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink"), [Windows XP Professional](../Page/Microsoft_Windows_XP.md "wikilink"), [Windows Server 2003](../Page/Microsoft_Windows_Server_2003.md "wikilink") をサポート。
  - [ノベル](../Page/ノベル_\(企業\).md "wikilink") iSCSI イニシエータ for [NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink") - Netware 6.5 で使用可能。
  - [サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink") Solaris iSCSI イニシエータ - Solaris 10 1/06 アップデートで使用可能。

#### ハードウエア

iSCSI[ホストバスアダプタ](https://ja.wikipedia.org/wiki/ホストバスアダプタ "wikilink") (HBA) はそれ自身にiSCSIプロトコルを実装している。OSからはSCSI HBAに見える。TOE [NICを持つものやiSCSI専用処理をオフロード出来るものもある](https://ja.wikipedia.org/wiki/ネットワークカード "wikilink")。遠隔のtargetディスクからOSをブートするために、[NVRAMを搭載しているものもある](../Page/不揮発性メモリ.md "wikilink")。以下のベンダーが主に開発している。

  - [アダプテック](../Page/アダプテック.md "wikilink")（生産終了）
  - [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")
  - [Alacritech](https://ja.wikipedia.org/wiki/Alacritech "wikilink")
  - [Qlogic](https://ja.wikipedia.org/wiki/Qlogic "wikilink")
  - [Brocade](https://ja.wikipedia.org/wiki/Brocade "wikilink") (旧 Silverback)

### ターゲット

ディスク製品が主である。[テープドライブ](https://ja.wikipedia.org/wiki/テープドライブ "wikilink")や[テープライブラリ](https://ja.wikipedia.org/wiki/テープライブラリ "wikilink")にも需要があるが、今のところサポートしている製品は限られている\[11\]。代わりに並列パラレルSCSIやファイバーチャネルを持つ装置にテープとiSCSIターゲットソフトウェアを搭載した製品がある。ターゲットは[仮想化](../Page/仮想化.md "wikilink")できる可能性がある。[仮想テープライブラリ](https://ja.wikipedia.org/wiki/テープライブラリ#仮想テープライブラリ "wikilink") (VTL) のように外から見えるターゲットの種別とは全く関係なく、内部の構造を自由に実装できる。仮想ターゲットでも装置筐体内で専用コントローラやソフトウェアを使う事で、iSCSIターゲットとして見せかける事が出来る。

#### ソフトウェア

  - Windows
      - [Microsoft iSCSI Software Target 3.3](http://www.microsoft.com/downloads/en/details.aspx?FamilyID=45105d7f-8c6c-4666-a305-c8189062a0d0)
      - [StarWind iSCSI SAN (Free Edition有り)](http://www.starwindsoftware.com/)
  - Linux
      - [LIO](http://www.linux-iscsi.org/) - Linux open source iSCSI target, kernel ≥2.6.37
      - [iSCSI Enterprise Target](http://iscsitarget.sourceforge.net/) - オープンソースの iSCSIターゲット実装（Linux用）
      - [iSCSI_Tape](http://sourceforge.net/projects/iscsitape/) - iSCSIターゲットの仮想[テープドライブ](https://ja.wikipedia.org/wiki/テープドライブ "wikilink")
      - [Linux SCSI target framework](http://stgt.sourceforge.net/)
      - [Generic SCSI Target Subsystem for Linux](http://scst.sourceforge.net/)
      - [MayaStor](http://www.pavitrasoft.com/products/mayastor.html)
  - [Solaris](../Page/Solaris.md "wikilink")
      - Solaris 10 ではshareiscsi。ただしユーザランド実装なので遅い。
      - Solaris 11、OpenSolarisではCOMSTAR。ZFSと連携し、高機能で高速。
  - [NetBSD](../Page/NetBSD.md "wikilink") 用ターゲットの [HOWTO](ftp://ftp.netbsd.org/pub/NetBSD/misc/agc/HOWTO-iSCSI-target.txt)
  - NetWare 6.5 には iSCSIターゲットのパッケージが含まれている。
  - POSIX
      - [Intel-iSCSI](http://www.sourceforge.net/projects/intel-iscsi)（[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")）
  - [FreeNAS](https://ja.wikipedia.org/wiki/FreeNAS "wikilink")

## 関連項目

  - [Small Computer System Interface](../Page/Small_Computer_System_Interface.md "wikilink") (SCSI)
  - [Fibre Channel Over IP](https://ja.wikipedia.org/wiki/Fibre_Channel_Over_IP "wikilink") (FCIP)
  - [Fibre Channel Over Ethernet](https://ja.wikipedia.org/wiki/ファイバーチャネル・オーバー・イーサネット "wikilink") (FCoE)
  - [:en:RDMA over Converged Ethernet](https://ja.wikipedia.org/wiki/:en:RDMA_over_Converged_Ethernet "wikilink") (RoCE)
  - [ATA over Ethernet](https://ja.wikipedia.org/wiki/ATA_over_Ethernet "wikilink") (ATAoE)

## 外部リンク

  - [絵で分かる iSCSI (ASCII.jp)](http://ascii.jp/elem/000/000/337/337508/)

### RFC

  - RFC 3720 - Internet Small Computer Systems Interface (iSCSI)
  - RFC 3721 - Internet Small Computer Systems Interface (iSCSI) Naming and Discovery
  - RFC 3722 - String Profile for Internet Small Computer Systems Interface (iSCSI) Names
  - RFC 3723 - Securing Block Storage Protocols over IP
  - RFC 3347 - Small Computer Systems Interface protocol over the Internet (iSCSI) Requirements and Design Considerations
  - RFC 3783 - Small Computer Systems Interface (SCSI) Command Ordering Considerations with iSCSI
  - RFC 3980 - T11 Network Address Authority (NAA) Naming Format for iSCSI Node Names
  - RFC 4018 - Finding Internet Small Computer Systems Interface (iSCSI) Targets and Name Servers by Using Service Location Protocol version 2 (SLPv2)
  - RFC 4173 - Bootstrapping Clients using the Internet Small Computer System Interface (iSCSI) Protocol
  - RFC 4544 - Definitions of Managed Objects for Internet Small Computer System Interface (iSCSI)
  - RFC 4850 - Declarative Public Extension Key for Internet Small Computer Systems Interface (iSCSI) Node Architecture
  - RFC 4939 - Definitions of Managed Objects for iSNS (Internet Storage Name Service)
  - RFC 5048 - Internet Small Computer System Interface (iSCSI) Corrections and Clarifications
  - RFC 5047 - DA: Datamover Architecture for the Internet Small Computer System Interface (iSCSI)
  - RFC 5046 - Internet Small Computer System Interface (iSCSI) Extensions for Remote Direct Memory Access (RDMA)
  - RFC 7143 - Internet Small Computer System Interface (iSCSI) Protocol (Consolidated)
  - RFC 7144 - Internet Small Computer System Interface (iSCSI) SCSI Features Update
  - RFC 7145 - Internet Small Computer System Interface (iSCSI) Extensions for the Remote Direct Memory Access (RDMA) Specification
  - RFC 7146 - Securing Block Storage Protocols over IP: RFC 3723 Requirements Update for IPsec v3
  - RFC 7147 - Definitions of Managed Objects for the Internet Small Computer System Interface (iSCSI)

## 脚注

[Category:補助記憶装置](https://ja.wikipedia.org/wiki/Category:補助記憶装置 "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  [iSCSIとは](http://www.fujitsu.com/jp/products/computing/storage/lib-f/tech/interface/iscsi/)
2.  [iSCSIプロトコル](http://www.snia-j.org/tech/nas/hakusho/hakusho2.html)
3.  [iSCSI PDU](http://www.santrainingblog.com/2010/09/iscsi-protocol-data-unit-pdu/)
4.  [iSCSI層](http://www.atmarkit.co.jp/fnetwork/tokusyuu/16iscsi/iscsi02.html)
5.  [1](http://www.cisco.com/japanese/warp/public/3/jp/product/hs/storage/mds9000/sosw/)
6.  [2](http://docs.hp.com/ja/5990-8154/ch04s24.html?jumpid=reg_R1002_JPJA)
7.  [3](http://www.kernel.org/pub/linux/utils/storage/iscsi)
8.  [4](http://Linux-iSCSI.sf.net)
9.  [5](http://www.open-iscsi.org/)
10. [6](http://unh-iscsi.sourceforge.net/)
11. [テープシステム iSCSIサポート](https://www.ibm.com/developerworks/community/blogs/InsideSystemStorage/entry/IBM_Announcements_for_Tape_and_CDM_May_2017?lang=en)