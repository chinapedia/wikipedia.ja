> この記事は[Winsock](https://ja.wikipedia.org/wiki/Winsock)から翻訳されています。


**Winsock** (**Windows Sockets API**, **WSA**) は、[Windowsにおいて](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[ネットワーク](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")が[ネットワークサービス](../Page/プロトコルスタック.md "wikilink")（特に[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")）にアクセスする方法を定義した技術仕様である。Windows 上の[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")クライアントアプリケーション（[FTPクライアントや](../Page/File_Transfer_Protocol.md "wikilink") Gopherクライアント）と[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")プロトコルスタックとの標準インタフェースを定義している。その名称は[BSD](../Page/BSD.md "wikilink")系[UNIX](../Page/UNIX.md "wikilink")でプログラム間の通信に使われた[ソケットと呼ばれる](https://ja.wikipedia.org/wiki/ソケット_\(BSD\) "wikilink")[APIモデルに基づいている](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。winsock.dll という[DLLファイルはWSAインタフェースの主要部分を提供するものであったため](../Page/ダイナミックリンクライブラリ.md "wikilink")、このAPIを Winsock という略称で呼ぶことには開発者側の抵抗があったし、ユーザー側にも多くの混乱があった。ユーザーは winsock.dll さえあれば、TCP/IP プロトコルが完全にサポートされるのだと誤解していることが多かった。

## 背景

初期のマイクロソフトのオペレーティングシステム（[MS-DOS](../Page/MS-DOS.md "wikilink")も[Windowsも](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")）は、ネットワーク機能が貧弱で、[NetBIOS](https://ja.wikipedia.org/wiki/NetBIOS "wikilink")/[NetBEUI](https://ja.wikipedia.org/wiki/NetBEUI "wikilink")を主に使っていた。これは階層化されていない、ルーティング不可能なネットワーク機能であり、[IBM](../Page/IBM.md "wikilink") の NetBIOS をマイクロソフトが実装したものであった。特に当時、マイクロソフトは[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")を完全に無視していた。数々の大学グループ（[MIT](../Page/マサチューセッツ工科大学.md "wikilink")）や商用ベンダー（[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")他）がMS-DOS用TCP/IPを開発し、ハードウェアに同梱するなどして販売していた。Windows がリリースされると、さらに Windows 向け TCP/IP を提供するベンダーが増えていった。しかし、マイクロソフトは相変わらず機能の貧弱な製品を提供していた。

これらベンダーの製品の弱点は、それぞれ独自の[APIを採用していた点である](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink")。また、メモリ使用量（当時、640KBもあれば大容量とされていた）や、複数のプロトコルを並行してサポートする方法がない点も問題だった。特に最後の問題点は重要であった。当時のネットワーク環境はベンダー毎に異なり（例えば、DECのDECnet、[ノベルの](../Page/ノベル_\(企業\).md "wikilink")[Netware](https://ja.wikipedia.org/wiki/Netware "wikilink")、Banyan Vines、IBM Lan Manager など）、それぞれ違ったプロトコルを使っていた（例えば、ノベルは IPX/SPX、IBM は NetBIOS API ベースのプロトコル、マイクロソフトは NetBEUI Frames Protocol）。従って、ユーザーが複数のネットワークサービスに接続するには、複数のブート構成を用意し、使いたいサービスに合わせて立ち上げ直して、対応するプロトコルを使えるようにする必要があった。さらにプログラミングモデルが統一されていないため、任意のベンダーのTCP/IP実装で動作するネットワークアプリケーションの開発は非常に困難であった。何らかの「標準化」が必要であることは明らかであった。

当時既にPCネットワークの分野での標準化はいくつも進められていた。[アメリカ空軍](https://ja.wikipedia.org/wiki/アメリカ空軍 "wikilink")の支援で行われた標準化として RFC 1001 と RFC 1002 がある。これは TCP/IP 上の NetBIOS 実装であり、**NBT** (NetBIOS over TCP/IP) と呼ばれた。次に FTP Software 社が中心となって進められた [Crynwr packet driver](http://www.crynwr.com/) がある。これは、上述したメモリ使用量の問題を[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で実装することで回避し、ネットワークカードの割り込みを独占しないことで複数プロトコルの同時サポート問題にも対応した。同様の試みとしてノベルのODI ([Open Data-Link Interface](https://ja.wikipedia.org/wiki/Open_Data-Link_Interface "wikilink")) やマイクロソフトのNDIS ([Network Driver Interface Specification](../Page/Network_Driver_Interface_Specification.md "wikilink")) といったAPIがある。これらはTCP/IPも含めたプロトコルスタックの完全な実装ではない点が重要である。従って、例えば Crynwr の Russ Nelson が開発した **QVT** や **WinQVT** はDECのVT220端末エミュレータだが、どちらもアプリケーション内にTCP/IPスタックを持っていた。packet driver と同時に使うことが可能で、例えばノベルの[IPX/SPX](https://ja.wikipedia.org/wiki/IPX/SPX "wikilink")で[NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink")のファイルサーバにアクセスすると同時に、DECの[VMSにTCP](https://ja.wikipedia.org/wiki/OpenVMS "wikilink")/IP経由でアクセスすることが可能であった。明らかにこのような環境がこのプロジェクトの目指したものであり、例えばパリの[OECDなどでそのような使われ方をしていた](https://ja.wikipedia.org/wiki/経済協力開発機構 "wikilink")。

Windows Sockets API を提案したのは JSB Software の Martin Hall であり、1991年10月、[CompuServe](https://ja.wikipedia.org/wiki/CompuServe "wikilink")での[電子掲示板](https://ja.wikipedia.org/wiki/電子掲示板 "wikilink")での議論が最初であった。仕様の第1版を編集したのは Martin Hall、Mark Towfiq（Microdyne、後にサン・マイクロシステムズ）、Geoff Arnold（サン・マイクロシステムズ）、Henry Sanders と J Allard（[マイクロソフト](../Page/マイクロソフト.md "wikilink")）らである。著作権や知的所有権について議論があり、[IETF](../Page/Internet_Engineering_Task_Force.md "wikilink") を通すとか非営利団体を結成するといった議論がなされた。結局、単純に著作権は5人がそれぞれ所有することとなった。後に J Allard はマイクロソフト社内に大きなオフィスを与えられ、そこで ACK と NACK と名づけたイグアナを飼った。

## 技術

Windows Socket API 仕様は2つのインタフェースを定義している。1つは[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")開発者が利用する[APIであり](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、もう1つはネットワークソフトウェア開発者が新たなプロトコルモジュールをシステムに追加する際に利用する[SPIである](https://ja.wikipedia.org/wiki/サービス・プロバイダ・インターフェース "wikilink")。API は準拠アプリケーションが Winsock に準拠して実装された任意のプロトコルを使って動作可能であることを保証する。SPI は準拠プロトコルモジュールを Windows に追加可能であることと、任意のAPI準拠アプリケーションから利用可能となることを保証する。リリース当初、複数プロトコルサポートが必須だったため、このような保証は重要だったが、今では学問的興味から語られるだけである。Windows Socket version 2.0 には [IPX/SPX](https://ja.wikipedia.org/wiki/IPX/SPX "wikilink") で使われる機能も含まれているが、Winsock 2.0 リリース当時から既に廃れつつあるプロトコルであり、今ではこれを使うものはほとんどないだろう。[マイクロソフト](../Page/マイクロソフト.md "wikilink")は最近の Windows には必ず高品質な[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")スタックを実装しており、その代替となる有力な製品も存在しない。さらに言えば、TCP/IP 以外のプロトコルを実装しなければならない強い動機も存在しない。

Windows Sockets はバークレーの[ソケットに基づいているが](https://ja.wikipedia.org/wiki/ソケット_\(BSD\) "wikilink")、Windows の標準プログラミングモデルに対応するために機能を追加している。Winsock はソケットのほとんどの機能をカバーしているが、Windows と [UNIX](../Page/UNIX.md "wikilink") の根本的な違いからどうしても避けられない差異も生じている（とは言っても、[STREAMS](https://ja.wikipedia.org/wiki/STREAMS "wikilink")との差異に比べれば、ずっとソケットに近い）。APIに含まれる全ての関数名の頭には`WSA`が付く。例えばホスト名参照の `WSAGetHostByName()` などである。BSDソケットからの拡張で特筆すべきは、「ノンブロッキング」（非同期）ソケットである（通常の関数名の前に `WSAAsync` を付け、`WSAAsyncGetHostByName()` などとする）。

設計目標は、[UNIX](../Page/UNIX.md "wikilink")から Windows へのソケットベースのアプリケーションの移植を容易にすることであった。新たに Windows 向けに書かれるプログラムにとって、そのAPIが十分かどうかはあまり考慮されなかった。このため、Winsock には移植のために設計された要素がいくつか含まれている。例えば、[UNIX](../Page/UNIX.md "wikilink")アプリケーションでは、ネットワークのエラーも[標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")の関数内のエラーも同じ `errno` で表される。これは Windows にはない機能であるため、Winsock はそのための関数 `WSAGetLastError()` でエラー情報が得られるようにした。このような機能は役立つものの、アプリケーションの移植はなかなか困難だった。多くの[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")アプリケーションは、仮想端末とか[fork](https://ja.wikipedia.org/wiki/fork "wikilink")システムコールといった[UNIX](../Page/UNIX.md "wikilink")のシステム固有機能を使って実装されており、そのような機能を Windows で再現するのが困難だったのである。しかし、間もなく移植よりも Windows 独自のアプリケーション開発の方が主流となっていった。

## 仕様

  - Version 1.0 （1992年6月）
    Winsock の基本定義。BSDのソケットのインタフェースをかなり忠実に守っており、既存アプリケーションの移植性を考慮している。Windows固有の拡張が若干あり、主にメッセージ通知による非同期操作に関するものである。文書ではTCP/IPに制限してはいないが、具体的に言及されているプロトコルはTCPとUDPだけであった。ほとんどのベンダーはTCP/IPだけをサポートしたが、[DECは](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") DECnet もサポートしていた。
  - Verison 1.1 （1993年1月）
    細かな修正と仕様の分類。重要な変更点としては、`gethostname()` 関数を追加した点が挙げられる。
  - Winsock 2
    Winsock 1.1 との互換性を維持しつつ拡張している。プロトコルに独立した名前解決法をサポート。イベント通知や完了ルーチンによる非同期操作サポート。階層型プロトコル実装サポート。[マルチキャスト](../Page/マルチキャスト.md "wikilink")。[Quality of Service](https://ja.wikipedia.org/wiki/Quality_of_Service "wikilink")。複数プロトコルサポートも公式化され、[IPX/SPX](https://ja.wikipedia.org/wiki/IPX/SPX "wikilink")と[DECnet](https://ja.wikipedia.org/wiki/DECnet "wikilink")が明記された。プロセス間でのソケット共有、コネクションの条件付き受理、ソケットグループ処理などが可能となった。Winsock 1.x とは大幅な違いがあるが、Winsock 1.1 API とのソース互換とバイナリ互換を保っている。他にも Service Provider Interface (SPI) API や [Layered Service Provider](https://ja.wikipedia.org/wiki/Layered_Service_Provider "wikilink") (LSP) がサポートされた。
  - Version 2.0.x （1994年3月以降）
    内部ドラフト。標準として公開されたものではない。
  - Version 2.1.0 （1996年1月）
    Winsock 2 としての最初の公開版。
  - Version 2.2.0 （1996年5月）
    細かな修正、明確化、使用方法の追記など。16ビット Windows アプリケーションサポートを削除した。
  - Version 2.2.1 （1997年5月）、Version 2.2.2 （1997年8月）
    細かな機能強化。ネットワーク構成やシステム構成の変化に関して問い合わせたり、通知を受け付ける機構を追加した。

[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")対応は[Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink")（2000年12月）で、RFC 2553 （後に RFC 3493 に置換）に基づいて行われ、[Windows XPの](../Page/Microsoft_Windows_XP.md "wikilink") Winsock の一部となっている。

## 実装

### マイクロソフト

  - マイクロソフトは Winsock 1.0 の実装を提供しなかった。
  - Winsock 1.1 は Windows for Workgroups のアドオンパッケージとして提供された。また、[Windows 95](../Page/Microsoft_Windows_95.md "wikilink") と [Windows NT](../Page/Microsoft_Windows_NT.md "wikilink") 3.x では最初から必須コンポーネントとして導入された。
  - Winsock 2 は Windows 95 のアドオンパッケージとして提供された\[1\]。[Windows 98および](../Page/Microsoft_Windows_98.md "wikilink") NT 4.0 以降は必須コンポーネントとして導入されている。Windows 3.x や NT 3.x 向けに Winsock 2 が提供されることはなかった。
  - Winsock 2.x は新たなWindowsのリリース時点や[サービスパック](../Page/サービスパック.md "wikilink")の形で提供されている。
  - Winsock 2 は [Layered Service Provider](https://ja.wikipedia.org/wiki/Layered_Service_Provider "wikilink") (LSP) と呼ばれる機構で拡張可能である。Winsock LSP はペアレンタル制御、Webコンテンツのフィルタリング、[QoSなどに使われている](https://ja.wikipedia.org/wiki/Quality_of_Service "wikilink")。全ての Provider の階層順位は Winsock Catalog で管理される。かつて、バグのある LSP を削除すると Winsock Catalog が破壊されてネットワークが全く使えなくなるという問題があった。Windows XP SP2、Windows Server 2003 SP1、およびその後の Windows では、LSP をアンインストールしても自動修復できるようになっている。

### 他の実装

  - Winsock 準拠の TCP/IP スタックを提供するベンダーとしては、[スリーコム](https://ja.wikipedia.org/wiki/スリーコム "wikilink")、Beame & Whiteside、DEC、Distinct、FTP Software、Frontier、[IBM](../Page/IBM.md "wikilink")、Microdyne、NetManage、[ノベル](../Page/ノベル_\(企業\).md "wikilink")、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")、Trumpet Software International などがある。
  - Trumpet Winsock は数少ない Winsock 1.0 の実装であり、Windows 3.0 にインストール可能であった。Trumpet は Windows 3.x 向け Winsock の[シェアウェア](../Page/シェアウェア.md "wikilink")版でも知られている。2008年2月以降はTattam Software EnterprisesがTrumpet の知的所有権を有している\[2\]。

## 参考文献

  - Aboba, Bernard D., comp.protocols.tcp-ip.ibmpc, Frequently Asked Questions, 1993. Usenet: <news:news.answers>.

## 脚注

## 関連項目

  - [ソケット (BSD)](https://ja.wikipedia.org/wiki/ソケット_\(BSD\) "wikilink")

## 外部リンク

  - [Windows Sockets](http://www.noviway.com/Code/Winsock.aspx) - Winsock のオープンソース実装(リンク切れ)
  - [Windows Sockets](http://web.archive.org/web/20090207062209/http://noviway.com/Code/Winsock.aspx) - Winsock のオープンソース実装(上記リンクの2009年2月のスナップショット)
  - [Sockets FAQ](http://www.faqs.org/faqs/windows/winsock-faq) - Windows Sockets FAQ

### Microsoft

  - [MSDNライブラリ - Winsock2 Reference](https://msdn.microsoft.com/en-us/library/ms741416.aspx)
  - [MSDNライブラリ - Winsock2 Home](https://msdn.microsoft.com/en-us/library/ms740673.aspx)
  - [Porting Berkley Socket programs to Winsock](https://msdn.microsoft.com/en-us/library/ms740096.aspx)
  - [Brief History of Microsoft on the Web](https://www.microsoft.com/misc/features/features_flshbk.htm)

### その他

  - [WinSock Development Information](http://www.sockets.com/)
  - [Winsock Programmer's FAQ](http://tangentsoft.net/wskfaq/)
  - [Komodia Inc. free open-source windows based Winsock library](http://www.komodia.com/index.php?page=newtools.html)

[Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink")

1.
2.  [Tattam Software Enterprises 公式サイト](http://www.trumpet.com.au/)