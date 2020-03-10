> この記事は[Server Message Block](https://ja.wikipedia.org/wiki/Server_Message_Block)から翻訳されています。


**Server Message Block** (**SMB**) は、主に[Windowsを中心とした環境で](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[LANを通じて](../Page/Local_Area_Network.md "wikilink")[ファイル共有](https://ja.wikipedia.org/wiki/ファイル共有 "wikilink")やプリンタ共有などに使用される[通信プロトコル](../Page/通信プロトコル.md "wikilink")の総称。[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")では第7層[アプリケーション層](https://ja.wikipedia.org/wiki/アプリケーション層 "wikilink")に該当する。認証つき[プロセス間通信](../Page/プロセス間通信.md "wikilink")機構としても動作する。

下位層のプロトコルとして[NetBEUI](https://ja.wikipedia.org/wiki/NetBEUI "wikilink")を使用していた時代には、[サブネット](https://ja.wikipedia.org/wiki/サブネット "wikilink")を越える[ルーティング](https://ja.wikipedia.org/wiki/ルーティング "wikilink")はできず、中大規模のネットワークには向かないとされたが、や、[NetBIOS](https://ja.wikipedia.org/wiki/NetBIOS "wikilink")も必要としない**CIFS**（**Common Internet File System**）により、大規模ネットワークでも使用可能となっている。

## 歴史

### SMB/CIFS/SMB1

2015年現在では、SMB 1.0以前のものを明確には区別せずにダイアレクト（方言）として扱うことが一般的である\[1\]\[2\]。「SMB1/CIFS」などとまとめて表記することも多い。また、下記のSMB 1.0以前の説明は2015年現在のマイクロソフトの説明に従って記載しているが、マイクロソフトは過去には下記とは矛盾する説明をしていたこともあったため\[3\]、注意が必要である。

#### 初期のSMB

SMBは1982年に[IBM](../Page/IBM.md "wikilink")のBarry Feigenbaumが設計した\[4\]。[DOSのローカルファイルアクセス用](../Page/DOS_\(OS\).md "wikilink")「[割り込み](../Page/割り込み_\(コンピュータ\).md "wikilink") 33」(21h) をネットワーク上のファイルシステム向けに変えることを目標としていた。[マイクロソフト](../Page/マイクロソフト.md "wikilink")はこれにかなりの機能追加や修正を施した。1990年ごろ、マイクロソフトはSMBプロトコルを[スリーコム](https://ja.wikipedia.org/wiki/スリーコム "wikilink")と共同開発していた [LAN Manager製品に組み込んだ](https://ja.wikipedia.org/wiki/LAN_Manager "wikilink")。さらにその後の[Windows製品でもSMBプロトコルに機能を追加していった](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

#### CIFS

マイクロソフトは[1996年](../Page/1996年.md "wikilink")にSMBをCommon Internet File System (CIFS) と改称し\[5\]、Windows NT 3.51、Windows NT 4.0、Windows 98に搭載し\[6\]、さらなる機能追加を行った。例えば、[シンボリックリンク](https://ja.wikipedia.org/wiki/シンボリックリンク "wikilink")、[ハードリンク](https://ja.wikipedia.org/wiki/ハードリンク "wikilink")、より大きなファイルの操作、[NetBIOS](https://ja.wikipedia.org/wiki/NetBIOS "wikilink")を使わずにTCPポート445番で直接接続する方式（実験的な試みであり、さらなる改良が必要だった）などへの対応である。また、認証プロトコルである [NTLMv1](https://ja.wikipedia.org/wiki/NT_LAN_Manager "wikilink")（もともとのSMB仕様では、IBMのLAN Managerのパスワードを使うことになっていて、そこから生まれたプロトコル）では[DESを間違った形で使っていたため](../Page/Data_Encryption_Standard.md "wikilink")、[NTLMv2を追加した](https://ja.wikipedia.org/wiki/NT_LAN_Manager "wikilink")。さらに、NT 4.0のドメインログイン用プロトコルでは、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")以外では40ビットの暗号を使っている（128ビットの暗号は[輸出規制されていたため](https://ja.wikipedia.org/wiki/アメリカ合衆国からの暗号の輸出規制 "wikilink")）。ダイアレクトは「NT LM 0.12」を使用する。

[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")がを発表したころ、1997年、マイクロソフトは部分的仕様をいくつか[インターネットドラフト](https://ja.wikipedia.org/wiki/インターネットドラフト "wikilink")として[IETFに提出した](../Page/Internet_Engineering_Task_Force.md "wikilink")<ref name = "IETF">\* [Common Internet File System Protocol (CIFS/1.0)](http://www.tools.ietf.org/html/draft-heizer-cifs-v1-spec)

  - [CIFS Logon and Pass Through Authentication](http://www.tools.ietf.org/html/draft-leach-cifs-logon-spec)
  - [CIFS/E Browser Protocol](http://www.tools.ietf.org/html/draft-leach-cifs-browser-spec)
  - [CIFS Printing Specification](http://www.tools.ietf.org/html/draft-leach-cifs-print-spec)
  - [CIFS Remote Administration Protocol](http://www.tools.ietf.org/html/draft-leach-cifs-rap-spec)
  - [A Common Internet File System (CIFS/1.0) Protocol](http://www.tools.ietf.org/html/draft-leach-cifs-v1-spec)

</ref>が、いずれも1998年までに有効期限切れとなっている。

#### SMB 1.0

2000年、[マイクロソフト](../Page/マイクロソフト.md "wikilink")は名称をSMBに戻し\[7\]、SMB 1.0(SMB1)として[Windows 2000で導入した](../Page/Microsoft_Windows_2000.md "wikilink")。Kerberos認証やActive Directoryに対応した\[8\]。また、ダイレクトホスティングSMBと呼ばれる[TCP上で直接動作させる機能も導入された](../Page/Transmission_Control_Protocol.md "wikilink")（その場合サーバがTCPポート445番で待機\[9\]）。ダイアレクトはCIFSと同じ「NT LM 0.12」を使用するため、技術的にはCIFSと区別されない。

#### 終焉

その後の技術の進化の結果、SMB1は暗号化強度の面や通信効率の面からも好ましくないとされるようになる。

2012年、マイクロソフトはStorage Developer ConferenceでSMB1を無効化することを技術者たちに提案した\[10\]。

2013年、マイクロソフトはWindows Server 2012 R2以降のOSではSMB1を使用することを非推奨と定義し\[11\]、速やかに新しい技術への移行を促した。

2014年、マイクロソフトは期限を明確にはしていないものの、将来のWindowsでは機能を削除する方針であることを公表した。

2016年、マイクロソフトは改めて速やかにSMB1の使用を停止するよう呼び掛けた\[12\]。

2017年1月、アメリカ国土安全保障省の配下組織US-CERTは、セキュリティ対策のベストプラクティスとして、SMB1の無効化を呼び掛けた\[13\]。

2017年9月5日、[Linux kernel](../Page/Linuxカーネル.md "wikilink") 4.13において既定のプロトコルをSMB3とし、SMB1を無効化した\[14\]\[15\]。

2017年9月、マイクロソフトはWindows 10 Version1709でSMB1を初期状態では無効とした\[16\]。ただし、セキュリティ上推奨されていないものの、必要であれば設定を変更することで有効化できる\[17\]。

### SMB 2.0

マイクロソフトは2006年、SMBの新バージョン SMB 2.0 (SMB2) を[Windows Vistaで導入した](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")\[18\]。

SMB2では、コマンド/サブコマンドの種類が100以上あったものを19にまとめ、プロトコルのやりとりを集約した\[19\]。[パイプライン化機構があり](https://ja.wikipedia.org/wiki/パイプライン処理 "wikilink")、前の要求への応答を受け取る前に次の要求を送信できる。

複雑な動作を1つの要求にまとめることができ、クライアントとサーバ間のやり取りの回数を劇的に減らすことができ、結果として性能が向上する\[20\]。従来のSMBプロトコルにも同様な機能がありAndXと呼ばれていたが、マイクロソフトのクライアントは滅多にAndXを使わなかった。

SMB2ではより大きなバッファをサポートしており、大きなファイルの転送や高速なネットワークでの性能向上が見込まれる\[21\]。

また、「永続性ファイルハンドル」と呼ばれるものを導入している。これは、ネットワーク接続が切れてもSMBサーバとのコネクションが継続できるようにするもので、無線LANなど接続が切れやすい環境で新たなセッションを構築する必要をなくす。

SMB2は[シンボリックリンク](https://ja.wikipedia.org/wiki/シンボリックリンク "wikilink")もサポートしている。他にもファイル属性のキャッシング、HMAC SHA-256ハッシュアルゴリズムによるメッセージ署名強化、ユーザー数・共有ファイル数などが増加した際のスケーラビリティ強化などの拡張がなされている\[22\]。

従来のSMBプロトコルは16ビットで各種サイズを表していた。SMB2ではそれらの多くを32ビットや64ビットに拡張しており、[ファイルハンドル](https://ja.wikipedia.org/wiki/ファイルハンドル "wikilink")の場合は16バイトとしている。

Windows Vistaとそれ以降のオペレーティングシステムでは、通信相手もWindows Vistaかそれ以降であれば、SMB2を使って通信する。SMB2をサポートしない従来のWindowsなどとの通信には引き続きSMB1が使われる。

SMB2はマイクロソフトにとって具体的に次のような利益をもたらした。

1.  知的財産権の明確化。従来のSMBは[IBM](../Page/IBM.md "wikilink")がもともと設計したもので、Windows以外にも[XENIX](../Page/XENIX.md "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")、[VMS](https://ja.wikipedia.org/wiki/OpenVMS "wikilink") (Pathworks) などにも採用されている。[X/Open](https://ja.wikipedia.org/wiki/X/Open "wikilink")が部分的に標準化したり、[IETFにもインターネットドラフトとして提出された](../Page/Internet_Engineering_Task_Force.md "wikilink")。このため、知的財産所有権の所在は曖昧だった\[23\]。SMB2.0以降はすべてMicrosoftが作成している。
2.  過去の資産との決別。従来のSMBのコードは非常に様々なSMBクライアントやサーバに対応する必要があった。このためプロトコルにはオプション部分が多数存在する（長いファイル名を扱えるか否かなど）。また、コマンドの応答として様々なレベルの情報を扱う。さらに[Unicode](../Page/Unicode.md "wikilink")対応は後から追加されている。SMB2のコードは従来のものより大幅に単純化されている（例えば、Unicodeサポートが前提なので、Unicodeでない場合を扱うコードは不要）。そのため、SMB2は少なくともマイクロソフトによる互換性テストを大幅に削減した（当初はWindows Vistaのクライアントとサーバのみの評価で済んだ）。

### SMB 2.1

Windows 7とWindows Server 2008 R2で搭載された。SMB 2.0と比べてさらにファイル転送の速度が向上、特に複数のクライアントから同時にアクセスされた際は約3.5倍の向上が図られている\[24\]。

### SMB 3.0

Windows 8とWindows Server 2012で搭載された。SMB ダイレクト、SMB マルチチャネル、SMB 暗号化などの機能が追加された\[25\]。開発段階ではSMB2.2と呼ばれていた\[26\]。

### SMB 3.0.2

Windows 8.1とWindows Server 2012 R2で搭載された。透過フェイルオーバー使用時の自動リバランス、SMB ダイレクトの性能向上などの更新にとどまる\[27\]。

### SMB 3.1.1

Windows 10で搭載された。認証の[耐タンパー性能](https://ja.wikipedia.org/wiki/耐タンパー性能 "wikilink")の向上とSMB暗号化使用時のAES-128-GCMの追加が含まれる。

## 構造

### クライアント-サーバ方式

SMBは[Peer to Peer方式の動作をし](../Page/Peer_to_Peer.md "wikilink")、[クライアントが何らかの要求を送ると](../Page/クライアント_\(コンピュータ\).md "wikilink")、サーバがそれに対応して応答する。SMBプロトコルの一部は特に[ファイルシステム](../Page/ファイルシステム.md "wikilink")へのアクセスを扱っており、クライアントは[ファイルサーバ](../Page/ファイルサーバ.md "wikilink")との通信にその部分を使う。しかし、SMBプロトコルには[プロセス間通信](../Page/プロセス間通信.md "wikilink") (IPC) に特化した部分もある。SMBプロトコルはローカルなサブネットでの使用に最適化したが、インターネット経由で他のサブネットとの間でSMBを使うこともできる。Windowsのファイル共有やプリンタ共有に関わる[エクスプロイト](https://ja.wikipedia.org/wiki/エクスプロイト "wikilink")は、そのような使用法を主なターゲットとしている。

SMBサーバはファイルシステムや他の[リソースに](../Page/計算資源.md "wikilink")、ネットワーク上のクライアントがアクセスできるようにする。クライアントはサーバ上の共有ファイルシステムやプリンタにアクセスする。このような用法・機能としてはSMBは最も有名で最も広く使われている。しかし、SMBのファイルサーバとしての面には、[NTドメインを構成するプロトコル群が重要であり](../Page/ドメインコントローラ.md "wikilink")、それらによって少なくともNT式のドメインベースの[認証](../Page/認証.md "wikilink")を提供している。NTドメインプロトコルはSMBのIPCである[名前付きパイプ](../Page/名前付きパイプ.md "wikilink")のためだけに[MSRPCサービスを提供し](https://ja.wikipedia.org/wiki/DCE/RPC "wikilink")、SMBサーバの実装のほとんどはリソースへのユーザーアクセスの妥当性を検証するのにNTドメインの認証を使う。

### 性能問題

SMBプロトコルでは、各クライアントが自身の存在を知らせるためにサブネット全体に[ブロードキャスト](../Page/ブロードキャスト.md "wikilink")するため、ネットワークの[帯域幅](../Page/帯域幅.md "wikilink")を占有しすぎると思われている。しかし、実はSMB自体はブロードキャストを使わない。SMBと結び付けられているブロードキャスト問題は、実際にはNetBIOSの[サービス・ロケーション・プロトコル](../Page/サービス・ロケーション・プロトコル.md "wikilink")のせいである。デフォルトでは、WindowsのサーバはNetBIOSを使ってサービスの告知と発見を行う。NetBIOSは特定ホスト上で利用可能なサービスを一定間隔でブロードキャストすることで機能する。ホストが20台以下のネットワークではそのような設定でも十分だが、それ以上にホスト台数が増えるとブロードキャストのトラフィックが問題を生じるようになる。NetBIOS Name Server (NBNS) を適切に実装すると、この問題を緩和できる。例えば[Windows Internet Naming Service](https://ja.wikipedia.org/wiki/Windows_Internet_Naming_Service "wikilink") (WINS) はマイクロソフトのネットワーク環境では適切な解決策を提供する。WINSはサービス要求の集中管理と登録のためのシステムを提供するが、ネットワークの設計と保守がより複雑化する。マイクロソフトは、[Active Directory環境での](https://ja.wikipedia.org/wiki/Active_Directory "wikilink")[ダイナミックDNSの利用を推奨している](https://ja.wikipedia.org/wiki/ダイナミックドメインネームシステム "wikilink")。

ネットワークを設計する際には、SMBプロトコルの性能は[レイテンシ](../Page/レイテンシ.md "wikilink")に大きく影響されることを考慮しなければならない。SMBを使って[ディレクトリ](../Page/ディレクトリ.md "wikilink")を渡り歩いてファイルを探すような操作をしたとき、このレイテンシの影響が見た目にも明らかになる。例えば[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")経由の[VPNコネクションではレイテンシが大きくなることが多く](../Page/Virtual_Private_Network.md "wikilink")、そのような環境ではディレクトリの中身（ファイル一覧）がなかなか表示されないということになる。

## 実装

以下の一覧は、SMBクライアント、SMBサーバ、SMBプロトコルの各種拡張（Network Neighborhood スイートやNTドメインスイートなど）である。以下に示したのは主なもので、拡張版、再実装版、移植版などは省いている。

  - [Samba](https://ja.wikipedia.org/wiki/Samba "wikilink")は、SMBプロトコルとマイクロソフトの拡張を[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")として再実装したもの。SMBサーバ機能とコマンドラインのSMBクライアント機能がある。
  - [Linuxカーネル](../Page/Linuxカーネル.md "wikilink")には[仮想ファイルシステム](https://ja.wikipedia.org/wiki/仮想ファイルシステム "wikilink") (VFS) を使ったSMBクライアントの実装が2つあり（smbfsとcifs）、SMBサーバ上のファイルに標準のファイルシステムAPI経由でアクセスできる。[fuseカーネルモジュールとユーザー空間のfusesmbを使ってSMBクライアント機能を実現することもできる](https://ja.wikipedia.org/wiki/Filesystem_in_Userspace "wikilink")。
  - [NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink") version 6以降では、CIFSサーバ機能を実装している。
  - [FreeBSD](../Page/FreeBSD.md "wikilink")にはVFSを使ったSMBクライアント実装としてsmbfsがある。
  - [NetBSD](../Page/NetBSD.md "wikilink")と[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")にはそれぞれのVFSを使ったSMBクライアント実装としてsmbfsがある（元はFreeBSDのsmbfsを移植）。
  - [Solaris](../Page/Solaris.md "wikilink")には、macOSのsmbfsを基にした[CIFS client for Solaris](http://opensolaris.org/os/project/smbfs/)というプロジェクトがある。
  - [OpenSolaris](https://ja.wikipedia.org/wiki/OpenSolaris "wikilink")は2007年10月、カーネル内にCIFSサーバ機能を実装した\[28\]
  - 小型[NASサーバ](../Page/ネットワークアタッチトストレージ.md "wikilink")[FreeNAS](https://ja.wikipedia.org/wiki/FreeNAS "wikilink")は、[FreeBSD](../Page/FreeBSD.md "wikilink")ベースで、CIFS/Sambaもサポートしている。[EMCコーポレーション](https://ja.wikipedia.org/wiki/EMCコーポレーション "wikilink")、[ネットアップ](../Page/ネットアップ.md "wikilink")といったストレージ企業各社もSMBサーバの実装を行っている。
  - Advanced Server for Unix (AS/U) は[UNIX](../Page/UNIX.md "wikilink")向けにWindows NT 3.51のSMBサーバ機能を移植したもので、[AT\&T](../Page/AT&T.md "wikilink")がマイクロソフトからライセンス提供を受け、主なUNIXベンダーにライセンス提供した。サン・マイクロシステムズは、Advanced Server for UnixをSolarisに移植した Solaris PC NetLink（コード名 Cascade）を製品化している。
  - [コンテンツ管理システム](https://ja.wikipedia.org/wiki/コンテンツ管理システム "wikilink")[Alfresco](https://ja.wikipedia.org/wiki/Alfresco "wikilink")には、SMBサーバの[Java](https://ja.wikipedia.org/wiki/Java "wikilink")による実装JLANが含まれている。
  - [JCIFS](http://jcifs.samba.org)はJavaによるSMBクライアント実装
  - [RTSMB](http://www.ebsembeddedsoftware.com)は[組み込みシステム](../Page/組み込みシステム.md "wikilink")用のCIFS/SMB実装。
  - [Visuality Systems NQ CIFS](http://cifs.com/jp)は[組み込みシステム](../Page/組み込みシステム.md "wikilink")用のCIFS/SMB実装。SMB1.0/SMB2.0/SMB3.0対応。[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[VxWorks](../Page/VxWorks.md "wikilink")、 Integrity、 [iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")、 [Android](../Page/Android.md "wikilink")といった多くの[RTOSに移植されている](../Page/リアルタイムオペレーティングシステム.md "wikilink")。
  - [AzSmb](http://members.inode.at/anton.zechner/az/AzSmb.en.htm)は、[組み込みシステム](../Page/組み込みシステム.md "wikilink")用の小型SMBサーバである。GPLもしくは商用ライセンスで提供されている。
  - [File System for SMB/CIFS/Windows(R)](https://github.com/yoichiro/chromeos-filesystem-cifs)はChromeOS向けのSMBクライアント実装。JavaScriptで書かれている。

## 脚注・出典

## 関連項目

  - [ファイル共有](https://ja.wikipedia.org/wiki/ファイル共有 "wikilink")
  - [NetBEUI](https://ja.wikipedia.org/wiki/NetBEUI "wikilink")
  - [AppleTalk](https://ja.wikipedia.org/wiki/AppleTalk "wikilink")
  - [Network File System](https://ja.wikipedia.org/wiki/Network_File_System "wikilink") (NFS)
  - [Samba](https://ja.wikipedia.org/wiki/Samba "wikilink")

## 外部リンク

  - [Windows Protocols](https://msdn.microsoft.com/en-us/library/cc216517.aspx) - マイクロソフトのMSDN Open Protocol Site

  - [\[MS-CIFS\]: Common Internet File System (CIFS) Protocol](https://msdn.microsoft.com/en-us/library/ee442092.aspx) - draft-leach-cifs-v1-spec-02.txt の改訂版

  - [\[MS-SMB\]: Server Message Block (SMB) Protocol](https://msdn.microsoft.com/en-us/library/cc246231.aspx) - MS-CIFSへのマイクロソフトによる拡張仕様

  - [\[MS-SMB2\]: Server Message Block (SMB) Protocol Versions 2 and 3](https://msdn.microsoft.com/en-us/library/cc246482.aspx) - SMB2/3プロトコルの仕様

  - [\[MS-SMBD\]: SMB2 Remote Direct Memory Access (RDMA) Transport Protocol](https://msdn.microsoft.com/en-us/library/hh536346.aspx) - SMBダイレクトの仕様

  - [\[MS-FSSO\]: File Access Services System Overview](https://msdn.microsoft.com/en-us/library/ee392367.aspx) - Windows File Access Services Systemの機能、ファイルサービスを必要とするシステムやアプリケーションとどのようにやり取りするか、設定や管理を行うシステムとどのようにやり取りするかを記述

  - [Download details: Common Internet File System (CIFS) File Access Protocol](https://web.archive.org/web/20040922021742/http://www.microsoft.com/downloads/details.aspx?FamilyID=c4adb584-7ff0-4acf-bd91-5f7708adb23c&displaylang=en) - マイクロソフトによる技術詳細

  - [Implementing CIFS](http://ubiqx.org/cifs/)

  - [Samba development information](http://devel.samba.org/)

  -
[Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink")

1.
2.
3.
4.  [SMB｜CIFS NQ｜製品情報｜アイティアクセス株式会社](http://www.itaccess.co.jp/products/cifs_nq/smb/index.html)
5.
6.  [ファイル共有プロトコル、SMBとCIFSの違いを正しく理解できていますか？（前編）：その知識、ホントに正しい？ Windowsにまつわる都市伝説（23） - ＠IT](http://www.atmarkit.co.jp/ait/articles/1501/19/news092.html)
7.
8.  [第7回　ファイル共有プロトコルSMBの概要：Windowsネットワークの基礎 - ＠IT](http://www.atmarkit.co.jp/ait/articles/1507/02/news026.html)
9.
10.
11. [Features Removed or Deprecated in Windows Server 2012 R2 | Microsoft Docs](https://technet.microsoft.com/en-us/library/dn303411.aspx)
12.
13.
14.
15.
16. [SMBv1 is not installed by default in Windows 10 version 1709 and Windows Server version 1709 and later versions](https://support.microsoft.com/en-us/help/4034314/smbv1-is-not-installed-windows-10-and-windows-server-version-1709)
17.
18.
19.
20. [マイクロソフト、VistaとServer 2008で実現するメリットを解説](http://pc.watch.impress.co.jp/docs/2008/0404/ms.htm)
21.
22. [SMB2, a complete redesign of the main remote file protocol for Windows](http://blogs.technet.com/josebda/archive/2008/12/05/smb2-a-complete-redesign-of-the-main-remote-file-protocol-for-windows.aspx)
23.
24.
25.
26.
27.
28. [Project CIFS Server - Introduction](http://www.opensolaris.org/os/project/cifs-server/)