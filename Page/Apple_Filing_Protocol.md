> この記事は[Apple Filing Protocol](https://ja.wikipedia.org/wiki/Apple_Filing_Protocol)から翻訳されています。


**Apple Filing Protocol**（または**AppleTalk Filing Protocol**、**AFP**）は、[アップルが開発した](../Page/アップル_\(企業\).md "wikilink")、[Classic Mac OS](../Page/Classic_Mac_OS.md "wikilink") / [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")の[ファイル共有](../Page/ファイル共有.md "wikilink") ([AppleShare](https://ja.wikipedia.org/wiki/AppleShare "wikilink")) のためのプロトコルである。初期は[AppleTalk](https://ja.wikipedia.org/wiki/AppleTalk "wikilink")の複数のプロトコルのうちのひとつとして存在した。 AFP 2.2以降ではAppleTalkではなく[TCP/IP上で動くプロトコル](../Page/インターネット・プロトコル・スイート.md "wikilink") (AFP over TCP) になっている。

## 概要

Classic Mac OSやmacOSは、「パーソナルファイル共有」または単に「ファイル共有」の設定を行なえば、AFPサーバとして動作させることができる。ただし、同時接続10ユーザ迄、10ボリューム迄、10フォルダ迄といった制限がある\[1\]。Classic Mac OSでは別途購入のソフトウェアAppleShareをインストールすることで大規模なAFPサーバとして動作させることができた。macOSの場合は、サーバ版である[macOS Serverにて大規模AFPサーバを構成できる](https://ja.wikipedia.org/wiki/macOS_Server "wikilink")。

こうしたAFPによるファイル共有のことをAppleShareと呼ぶ場合がある。

[Mac OS X v10.5以降ではバックアップのためのソフトウェア](../Page/Mac_OS_X_v10.5.md "wikilink")[Time Machineが追加されたが](../Page/Time_Machine_\(ソフトウェア\).md "wikilink")、これを使ってネットワーク上のドライブにバックアップする場合、通常はAFPが利用される\[2\]。

Mac以外でもAFPを実装するソフトウェアがいくつかあり、異なるOSとの間でファイル共有を実現することができる。これの具体例に関しては下の「実装例」に記述する。

極めて古いMacはAppleTalkのAFPのみをサポートするため、最近のTCP/IPのみのAFPサーバには接続できない。また、その逆に最近のMacは極めて古いAFPサーバに接続できないという問題がある。しかしながら、AppleTalk自体が過去のものになりつつあるため、近年はさほど問題視されない。

Classic Mac OSのローカル[ファイルシステム](../Page/ファイルシステム.md "wikilink")である[HFSや](../Page/Hierarchical_File_System.md "wikilink")[HFS+は](https://ja.wikipedia.org/wiki/HFS_Plus "wikilink")、独自のファイル属性や[リソースフォーク](../Page/リソースフォーク.md "wikilink")、タイプ/クリエータ等を有しており、Mac OSの仕様変更、仕様拡張と共に進化してきた。AFPもこれと同等の機能を提供するために度重なるバージョンアップを繰り返してきている。

Mac OS 9迄は、AFPがOS標準サポートの唯一のファイル共有サービスであったが、macOSではAFPの他に、[SMB (CIFS)](https://ja.wikipedia.org/wiki/Common_Internet_File_System "wikilink")、[NFS](https://ja.wikipedia.org/wiki/Network_File_System "wikilink")、[FTP](../Page/File_Transfer_Protocol.md "wikilink")、[WebDAV](../Page/WebDAV.md "wikilink")といったさまざまなファイルサービスも利用できるようになった。しかし、これらを用いた場合、HFSやHFS+独自のメタデータは欠落するか、または[AppleDouble Header Fileとして別ファイルで扱われることになる](../Page/AppleSingle.md "wikilink")（このファイル名は「._」で始まる）。このため、AFPはmacOSにとって重要な意味をもつファイル共有プロトコルと言えた。

しかしながら、macOSのSMBのサーバ及びクライアント機能の実装も改良が続けられ、メタデータは[代替データストリームとして保存できるようになった](https://ja.wikipedia.org/wiki/フォーク_\(ファイルシステム\) "wikilink")。[OS X MavericksはSMB](https://ja.wikipedia.org/wiki/OS_X_Mavericks "wikilink")2の機能を実装し、AFPよりもSMB2を優先するようになった。ただしTime Machineに関してはAFPのままである。

Mac OS以外の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) でAFPを実装する場合、HFS、HFS+特有の情報をどのようにして保存するかが問題となる。 [Windows Server 2003迄のバージョンのSFM](../Page/Microsoft_Windows_Server_2003.md "wikilink") (Service for Macintosh) では[NTFSの](../Page/NT_File_System.md "wikilink")[代替データストリームを用いていたが](https://ja.wikipedia.org/wiki/フォーク_\(ファイルシステム\) "wikilink")、[Windows Server 2008以降ではSFM自体が廃止されている](../Page/Microsoft_Windows_Server_2008.md "wikilink")。[UNIX](../Page/UNIX.md "wikilink")上でAFPを実装する[netatalk](https://ja.wikipedia.org/wiki/netatalk "wikilink")では、.AppleDoubleという名称のディレクトリをつくり、この中に[AppleDouble Header fileを保存する仕様である](../Page/AppleSingle.md "wikilink")。データフォークのみを扱う実装も実在する。

## 歴史

### AFP 1.0

リリースされなかった。

### AFP 1.1/2.0

初期のClassic Mac OSでは、ネットワーク機能は[AppleTalk](https://ja.wikipedia.org/wiki/AppleTalk "wikilink")と呼ばれる独自のプロトコル群を用いていた。これについては書籍「Inside AppleTalk\[3\]」や「Inside Macintosh\[4\]」に各種仕様が載っている。 AFP 1.1および2.0はこれに載っているプロトコルのひとつであった。この時点での正式名称は**AppleTalk Filing Protocol**である。

### AFP 2.1/2.2

AFP 2.1および2.2はアップルによるドキュメント「AppleTalk Filing Protocol Version 2.1 and 2.2\[5\]」で仕様が公開されている。 [AppleTalk](https://ja.wikipedia.org/wiki/AppleTalk "wikilink")と[TCP/IPの両方をサポートする](../Page/インターネット・プロトコル・スイート.md "wikilink")。AFP 2.1がAppleTalkベースであり、AFP 2.2がTCP/IPベースである。TCP上でAFPを使うための[Data Stream Interface](https://ja.wikipedia.org/wiki/Data_Stream_Interface "wikilink") (DSI) の仕様もこの文書に載っている。

AFP 2.1では、サーバメッセージ (FPGetSrvrMsg)、ファイルID (FPCreateID, FPDeleteID, FPResolveID, FPExchangeFiles)、ファイル名検索 (FPCatSearch) といったコマンドが追加され、ファイルのアクセス権の概念が導入された。また、ユーザ認証方法 (UAM) として双方向乱数交換 (Two-Way Random Number Exchange) が導入された。

AFP 2.2ではTCP/IPのサポートのためにサーバ情報取得 (FPGetSrvrInfo)、ボリューム情報取得 (FPGetVolParms, FPOpenVOL) が拡張されている。

### AFP 2.3

AFP 2.3は、クライアントがスリープに入ることをサーバに通知するコマンド (FPZzzzz) が追加されたのみである。

### AFP 3.x

現在のアップルのドキュメント\[6\]\[7\]は、主にmacOSのためのAFP 3.xを解説している。

ついにAppleTalkのサポートがなくなり、TCP/IPベースのみとなった。AFPは**Apple Filing Protocol**の略とされ、AppleTalkという名称が削除された格好である。

AFP 3.0では、UNIXスタイルのPOSIXパーミッションモデル、Unicodeファイル名 (AFPName) のサポートが追加され、最大共有数と最大ファイルサイズ（2GiB以上）が拡張された。

AFP 3.1では、ディレクトリリストの拡張 (FPEnumerateExt2)、サーバおよびクライアントのクラッシュへの対応、再接続への対応、ユーザ認証方法の追加 (Kerberos, DHX2,R econnect)、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")対応、Unicodeサーバ名等が追加されている。

AFP 3.2では、ACL対応 (FPAccess, FPGetACL, FPSetACL)、拡張属性 (FPGetExtAttr, FPListExtAttrs, FPRemoveExtAttr)、Time Machine対応 (FPSyncDir, FPSyncFork)、ファイル名の大文字小文字を区別する拡張 (kCaseSensitive) 等が追加された。

AFP 3.3では、サーバからの返答をキャッシュする機能 (AFP Replay Cache) が追加された。

AFP 3.4では、任意の名前の拡張属性が存在しなかった場合のエラーコードが変更されたのみである。

## OSI参照モデル

AppleTalkベースとTCP/IPベースの差異は、OSI参照モデルを適用すると理解しやすい。

AppleTalkの場合、AFP over ASP over ATP over DDPという構造となる。

TCP/IPの場合、AFP over DSI over TCP over IPという構造となる。つまりASPをDSIに置き換えることにより、AppleTalkとの差異を吸収した。DSIのデフォルトのポート番号は548であり、[IANAではこのポートにafpovertcpというキーワードを与えている](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")。ポート番号は変更することもできる。AppleTalkベースと区別するためにAFP over TCPと称する場合もある。

## ファイル名の扱い

AFPでは、3種類の[ファイル名](../Page/ファイル名.md "wikilink")を扱うことができる。

  - Short Name（[MS-DOS](../Page/MS-DOS.md "wikilink")互換の8.3形式、AFP 1.1以降）
  - Long Name（[HFS互換の](../Page/Hierarchical_File_System.md "wikilink")31バイト制限、AFP 1.1以降）
  - AFPName（実質的に長さ制限なし、AFP 3.0以降）

Short NameとLong Nameは最初のAFP 1.1から定義されているが、現在Short Nameをサポートする実装は稀であろう。

Mac OS 9迄はファイル名に31バイトの制限があり、一般には「短いファイル名」と呼ばれているが、仕様上は「Long Name」であることに注意されたい。ファイル名に使われる[文字コード](../Page/文字コード.md "wikilink")はMac OSの言語によって異なる。日本語版のMac OS（或は[漢字Talk](https://ja.wikipedia.org/wiki/漢字Talk "wikilink")）では[MacJapanese](../Page/MacJapanese.md "wikilink")が使われる。

macOSのためのAFP 3.xでは、AFPNameが使えるようになった。ファイル名に使われる文字コードは[Unicode](../Page/Unicode.md "wikilink")であるため、さまざまな言語を混ぜて使うことができる。31バイトを越えることができるため、一般に「長いファイル名」と呼ばれるのはこれである。

ファイル名に使えない文字は[制御文字](../Page/制御文字.md "wikilink")NULLと[コロン「:」の](https://ja.wikipedia.org/wiki/コロン_\(記号\) "wikilink")2文字である。

大文字小文字の区別は元々なかったが、AFP 3.2から区別する機能も追加された。

## 非公開コマンド

AFPでは各コマンドに番号を与えており、アップルのサイトで公開されている文書で確認できる。

[Mac OS X v10.5以降は](../Page/Mac_OS_X_v10.5.md "wikilink")76という番号が振られたコマンドを発行するが、これは[Spotlight](https://ja.wikipedia.org/wiki/Spotlight "wikilink")のためのFPSpotlightRPCというコマンドであることだけが公開されている。アップルのプライベートなコマンドであり詳細は非公開である。

## AFPサーバのブラウジング

AFPサーバのブラウジングは、AFPとは別のプロトコルで行なわれる。

初期はAppleTalkのNBP (Name Binding Protocol) を用いて行なわれた。NBP over AppleTalkにてサーバを発見し、AFP over AppleTalkでファイル共有を実現したわけである。

その後、AFPがTCP/IPに移植されたため、NBPにてサーバを発見してからAFP over TCPで接続することが可能になった。

更にTCP/IPのポート427を用いる[Service Location Protocol](../Page/サービス・ロケーション・プロトコル.md "wikilink") (SLP) でブラウジングが可能となった。この時点でAppleTalkの必要性が薄らいだわけである。

[Mac OS X v10.2以降では](../Page/Mac_OS_X_v10.2.md "wikilink")[Bonjour](../Page/Bonjour.md "wikilink") (Zeroconf) が導入された。[Mac OS X v10.5ではAppleTalkとSLPによるAFPサーバのブラウジング機能が削除され](../Page/Mac_OS_X_v10.5.md "wikilink")、Bonjourのみで可能となっている。

こうしたプロトコルの変更の結果、新しいMacから古いMacが発見できない、またはその逆といった問題が発生する。この場合は[IPアドレス](../Page/IPアドレス.md "wikilink")や[hostnameを直接指定することで接続ができる](../Page/ホスト名.md "wikilink")。

## 実装例

  - [AppleShare](https://ja.wikipedia.org/wiki/AppleShare "wikilink") - Classic Mac OS用の製品
  - パーソナルファイル共有 - Classic Mac OSおよびmacOSの標準機能
  - macOS Server - 標準機能
  - [Microsoft Windows Server](../Page/Windows_Server.md "wikilink") - Service for Macintosh (SFM)
  - [NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink")
  - PC MACLAN - [ディアイティ社](http://www.dit.co.jp/)によるWindows用AFPサーバ/クライアント
  - HELIOS UB+ (EtherShare) - [HELIOS社](http://www.helios.de/)によるファイル・プリントサーバ
  - [CAP (Columbia AppleTalk Package)](https://ja.wikipedia.org/wiki/Columbia_AppleTalk_Package "wikilink") - [Unix系](../Page/Unix系.md "wikilink")OS用オープンソースAppleTalkソフト
  - [netatalk](https://ja.wikipedia.org/wiki/netatalk "wikilink") - Unix系OS用オープンソースAFPサーバ
  - [afpfs-ng](http://sourceforge.net/projects/afpfs-ng) - Unix系OS用オープンソースAFPクライアント
  - [ExtremeZ-IP](http://www.grouplogic.com/products/extreme/overview.cfm) - Windows用AFPサーバ
  - [jaffer](http://giantlaser.com/jaffer/) - JavaによるAFPサーバ

## 参照

<references />

## 関連項目

  - [AppleTalk](https://ja.wikipedia.org/wiki/AppleTalk "wikilink")
  - [TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")
  - [通信プロトコル](../Page/通信プロトコル.md "wikilink")
  - [CAP](https://ja.wikipedia.org/wiki/Columbia_AppleTalk_Package "wikilink")
  - [netatalk](https://ja.wikipedia.org/wiki/netatalk "wikilink")

[Category:アップルのソフトウェア](https://ja.wikipedia.org/wiki/Category:アップルのソフトウェア "wikilink") [Category:Mac_OS](https://ja.wikipedia.org/wiki/Category:Mac_OS "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:プレゼンテーション層プロトコル](https://ja.wikipedia.org/wiki/Category:プレゼンテーション層プロトコル "wikilink")

1.  [Mac OS 8 and 9: パーソナルファイル共有のユーザ制限](http://support.apple.com/kb/TA25650?viewlocale=ja_JP)
2.  [Time Machine Network Interface Specification (TMNIS)](http://developer.apple.com/mac/library/documentation/NetworkingInternetWeb/Conceptual/TimeMachineNetworkInterfaceSpecification/Introduction/Introduction.html)
3.  [Inside AppleTalk Second Edition (pdf)](http://developer.apple.com/MacOs/opentransport/docs/dev/Inside_AppleTalk.pdf)
4.  [Inside Macintosh: Networking / Chapter 9 - AppleTalk Filing Protocol (AFP)](http://developer.apple.com/documentation/mac/Networking/Networking-223.html)
5.  [AppleTalk Filing Protocol Version 2.1 and 2.2 (pdf)](http://developer.apple.com/MacOs/opentransport/docs/dev/AFP_21_22.pdf)
6.  [Apple Filing Protocol Programming Guide](http://developer.apple.com/documentation/Networking/Conceptual/AFP/)
7.  [Apple Filing Protocol Reference](http://developer.apple.com/documentation/Networking/Reference/AFP_Reference/)