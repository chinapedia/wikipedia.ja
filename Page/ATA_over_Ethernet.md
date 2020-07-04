> この記事は[ATA over Ethernet](https://ja.wikipedia.org/wiki/ATA_over_Ethernet)から翻訳されています。


**ATA over Ethernet**（**ATAoE**、**AoE**）は、Brantley Coile Company[1](http://support.coraid.com/documents/AoEr11.pdf) が開発した[通信プロトコル](../Page/通信プロトコル.md "wikilink")であり、[ATAストレージ装置に](../Page/Advanced_Technology_Attachment.md "wikilink")[イーサネット](../Page/イーサネット.md "wikilink")経由でアクセスするもの。[ストレージエリアネットワーク](../Page/ストレージエリアネットワーク.md "wikilink")（SAN）を低価格の標準技術を使って構築できる。

ATAoE は[イーサネット](../Page/イーサネット.md "wikilink")上の一般の上位プロトコル（[IP](../Page/Internet_Protocol.md "wikilink")、[UDP](../Page/User_Datagram_Protocol.md "wikilink")、[TCP](../Page/Transmission_Control_Protocol.md "wikilink") など）を使わない。つまり、ATAoE は複数の[LANをまたがることはできず](../Page/Local_Area_Network.md "wikilink")、SANとしてのみ利用可能である。SANの別の方式である [iSCSI](https://ja.wikipedia.org/wiki/iSCSI "wikilink") は仕様書が257ページにも及ぶが、ATAoE の仕様書はわずか12ページである。

## OSでのサポート

ATAoEをサポートしている[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")として以下のものがある。

| OS名                                                                                        | 対応日付        | 対応リリース |
| ------------------------------------------------------------------------------------------ | ----------- | ------ |
| [Linuxカーネル](../Page/Linuxカーネル.md "wikilink") [2](http://support.coraid.com/support/linux/) | 2005年3月1日-- | 2.6.11 |
| [Solaris](../Page/Solaris.md "wikilink") [3](http://www.coraid.com/support/solaris/)       | 2007年8月20日  | 1.4    |
| [Plan 9](../Page/Plan_9_from_Bell_Labs.md "wikilink") [4](http://cm.bell-labs.com/plan9/)  | 2007年8月12日  | N/A    |
| [OpenBSD](../Page/OpenBSD.md "wikilink") [5](http://www.openbsd.org/)                      | 2007年11月25日 | 4.3    |

サードパーティ製品でのATAoEサポートとしては、以下のものがある。

  - Coraid \[[http://www.coraid.com/\]は](http://www.coraid.com/%5Dは)、[FreeBSD](../Page/FreeBSD.md "wikilink")向けの[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")を提供しており、現在のバージョンは Stacy D. Son [6](http://www.coraid.com/support/freebsd/) が保守している。
  - 2DegreesFrost [7](http://www.2degreesfrost.com/) は、Mac OS X (10.4) 向けの ATAoEサポートを提供している。
  - WinAoE [8](http://winaoe.org) はオープンソース（GPL）のWindows向けATAoEアクセスドライバであり、ディスクレスブートにも対応している（つまりブートディスクをイーサネット経由で接続）。
  - LayerWalker [9](http://www.layerwalker.com/) は、ATAoE技術をホームアプライアンスや周辺機器製品に導入している。

## ハードウェアでのサポート

Coraid [10](http://www.coraid.com/) は、ATAoE用[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink") EtherDrive を販売している。

LayerWalker [11](http://www.layerwalker.com/) はATAoEを中心とした miniSAN と呼ぶソリューションを2007年に発表した。

また、[vblade](http://sourceforge.net/projects/aoetools/) プログラムを使うと、Linux が動作するコンピュータのハードディスクをイーサネットで接続された他のコンピュータに ATAoE 用ドライブ（ターゲット）であるかのように見せることができる。vblade の実装は、ユーザー空間で実装されたものとLinux[カーネルモジュール](https://ja.wikipedia.org/wiki/カーネルモジュール "wikilink")として実装されたものの2種類がある。

## 関連する概念

ATAoE は単純なプロトコルだが、その可能性は大きい。それには、以下のような概念が関係してくる。

### ブロック・ストレージ

ATAoE は、[ATAコマンド群をサポートした](../Page/Advanced_Technology_Attachment.md "wikilink")[補助記憶装置](../Page/補助記憶装置.md "wikilink")の[セッション層](../Page/セッション層.md "wikilink")プロトコルである。ディスクの読み書きはブロックと呼ばれる固定サイズのデータ単位で行われる。ブロックサイズは512バイトで固定されている。

ATAoE は [ATAコマンドと](../Page/Advanced_Technology_Attachment.md "wikilink")（もしあれば）データがイーサネットのフレーム内でどのようにフォーマットされるかを指定している。従って、[イーサネット](../Page/イーサネット.md "wikilink")とATAoE用補助記憶装置の組合せは、通常の[ホストバスアダプタ](https://ja.wikipedia.org/wiki/ホストバスアダプタ "wikilink")とディスク装置とケーブルの置換となる。

#### ブロック・ストレージ上のファイルシステム

一般に、ハードディスクはその上で[ファイルシステム](../Page/ファイルシステム.md "wikilink")を構築して利用される。つまり、ハードディスクから見た唯一のユーザーはファイルシステムになる。[ext3](https://ja.wikipedia.org/wiki/ext3 "wikilink")、[XFS](../Page/XFS.md "wikilink")、[HFS+](../Page/HFS_Plus.md "wikilink")、[NTFS](../Page/NT_File_System.md "wikilink") といったファイルシステムは、そのような前提で設計されている。

ATAoE を使うと、[イーサネット](../Page/イーサネット.md "wikilink")には複数のコンピュータが接続されているため、この前提が崩れる可能性が生じる。従来型のファイルシステムではこれは危険であり、ファイルシステムの中身が壊れたり、OSがダウンする事態を引き起こす。

[クラスターファイルシステムは](../Page/コンピュータ・クラスター.md "wikilink")、あるブロックデバイスにアクセスできるコンピュータを1台に制限することで、これを回避する。複数のコンピュータが協調動作して安全にブロックデバイスを共有することを可能にする。

このようなクラスターファイルシステムの例として [GFS](https://ja.wikipedia.org/wiki/Global_File_System "wikilink") や [OCFS](https://ja.wikipedia.org/wiki/OCFS "wikilink")2 がある。

[ストレージエリアネットワーク](../Page/ストレージエリアネットワーク.md "wikilink")（SAN）のファイルシステムではこれとは異なった回避方法をとっているものもある。Tiger Technology Sarl[12](http://www.tiger-technology.com/) の MetaSAN では、NTFSなどの通常のファイルシステムを構築したディスクドライブを複数のコンピュータで共有可能であり、ATAoE もサポートしている。

#### ディスクドライブ

ATAoEのターゲットデバイスは、[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")またはホスト側からハードディスクのように見えるものである。これについては、以下の点が重要である。

  - アクセス性能は、ディスクのRPM(回転速度）、ヘッド移動速度（シークタイム）、磁気記録密度、ヘッドの位置あわせの正確さ、ディスク上のデータの配置、インタフェース技術などに依存する。
  - ランダムなディスクアクセス性能は、主にシークタイムで決定される。
      - ランダムアクセスはシーケンシャルアクセスの約100倍の時間がかかる\[1\]。
      - 単一ディスクのシーケンシャルアクセスは一般に 50-80 MB/s の性能である。
      - [RAID](../Page/RAID.md "wikilink")では、シーケンシャルアクセス性能もランダムアクセス性能も一般に向上する。
      - ホストOSとディスクファイルシステムは、ディスク性能を引き出すため、なるべくシーケンシャルにアクセスしようとする\[2\]。

### イーサネット

ATAoE では[イーサネット](../Page/イーサネット.md "wikilink")についての以下の点が重要である。

  - ATAoE のパケットでは、[MACアドレス](../Page/MACアドレス.md "wikilink")のみで発信元と送信先を示す。MACアドレスは[イーサネット](../Page/イーサネット.md "wikilink")のレベルで規定されているアドレスである。従って、単一のイーサネットがブロードキャストできる範囲でしか使えない。
  - 最近のハードウェアにはイーサネットでのフロー制御機能が備わっていて、再送をなるべくしないようにしている。
  - イーサネットのフレームは[巡回冗長検査](../Page/巡回冗長検査.md "wikilink")で完全性を保つようになっており、検査に通らないフレームは捨てられる。

## ATAoE の利点

[イーサネット](../Page/イーサネット.md "wikilink")を使ってブロックストレージにアクセスすると、以下のような利点がある。

  - ストレージ容量を追加するのが容易である。
  - 容量の上限は事実上存在しない。
  - アクセスはイーサネットの物理的な制限によって制御できる。そのLANが[インターネット](../Page/インターネット.md "wikilink")と接続していても、外部からATAoEのパケットを送り込むことはできない。
  - 一般的なハードウェアを使うことができる。
  - [バックアップ](../Page/バックアップ.md "wikilink")が容易にできる可能性がある。
  - データを複数のコンピュータで共有できる可能性がある。

## Config String

ATAoEターゲット（ストレージ）には、Config String と呼ばれる情報が付与される。これはディスクドライブそのものに格納される情報ではなく、インタフェース部にある不揮発性メモリに格納される。Config String は初期状態では長さゼロであり、その状態のときだけATAoEイニシエータが Config String を設定できる。これを使って、簡単な調停が行える。

## 関連項目

  - [HyperSCSI](https://ja.wikipedia.org/wiki/HyperSCSI "wikilink") - いわば SCSI over Ethernet
  - [iSCSI](https://ja.wikipedia.org/wiki/iSCSI "wikilink") - SCSI over TCP/IP
  - [Fiber Channel over Ethernet](https://ja.wikipedia.org/wiki/ファイバーチャネル・オーバー・イーサネット "wikilink")（FCoE）

## 脚注

## 外部リンク

  - 記事:
      - [ATA Over Ethernet: Putting Hard Drives on the LAN](http://www.linuxjournal.com/article/8149) — Linux Journal (28 April 2005)

      - — LinuxDevices.com (23 June 2004)

      - [The ATA over Ethernet (AoE) Protocol](http://www.linux-mag.com/id/2028/) — Linux Magazine (June 15th, 2005) 要ログイン
  - プロトコル:
      - [AoE protocol description](http://support.coraid.com/documents/AoEr11.pdf) ([PDF](../Page/Portable_Document_Format.md "wikilink") file)
      - [AoE protocol definition](http://www.coraid.com/RESOURCES/AoE-Protocol-Definition)
  - エミュレータとツール:
      - [ATA Over Ethernet Tools and vblade](http://sourceforge.net/projects/aoetools/) ユーザー空間版 vblade を含む。
      - [vblade, implemented as a kernel module](http://lpk.com.price.ru/~lelik/AoE/) ユーザー空間版より高速である。
      - [qaoed - Mulithreaded ATA over Ethernet storage target](http://pi.nxs.se/~wowie/qaoed.tgz/) ユーザー空間版
      - [Aoeserver - Mulithreaded ATA over Ethernet storage target](http://pi.nxs.se/~wowie/aoeserver/) カーネルモジュール版
  - Live CD:
      - [Slax Frodo with vblade and ATA Over Ethernet Tools](http://www.lbserver.org/aoe/) 評価やバックアップに利用できる。
  - ハウツー:
      - [Using ATA Over Ethernet On Debian Etch](http://www.howtoforge.com/ata_over_ethernet_debian_etch)

[Category:補助記憶装置](https://ja.wikipedia.org/wiki/Category:補助記憶装置 "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink")

1.
2.