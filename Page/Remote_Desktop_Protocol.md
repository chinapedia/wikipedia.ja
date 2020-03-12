> この記事は[Remote Desktop Protocol](https://ja.wikipedia.org/wiki/Remote_Desktop_Protocol)から翻訳されています。


**Remote Desktop Protocol** （リモート デスクトップ プロトコル、**RDP**）は、[リモート デスクトップ サービス](https://ja.wikipedia.org/wiki/リモート_デスクトップ_サービス "wikilink")（**RDS**、旧称：ターミナル サービス）が稼動している[サーバ](../Page/サーバ.md "wikilink")に[クライアントが接続する](../Page/クライアント_\(コンピュータ\).md "wikilink")[リモートデスクトップ](https://ja.wikipedia.org/wiki/リモートデスクトップ "wikilink")の多重チャネル[プロトコル](../Page/プロトコル.md "wikilink")である。リモート デスクトップ接続（**RDC**、旧称：ターミナル サービス接続）として [TCP](../Page/Transmission_Control_Protocol.md "wikilink") ポート 3389 および [UDP](../Page/User_Datagram_Protocol.md "wikilink") ポート 3389 を使用して接続する。

## 特徴

RDP 5.2で以下の機能をサポートしている。

  - 24ビットの色表現のサポート（8{{·}}15{{·}}16 ビットもサポート）
  - 128ビットまでの RC4 暗号化のサポート
  - [TLS](../Page/Transport_Layer_Security.md "wikilink") のサポート（暗号化のみ）
  - ローカル上でリモート上のサウンド再生
  - ファイル システム リダイレクションのサポート
  - プリンタのサポート
  - [シリアルポート](../Page/シリアルポート.md "wikilink")と[パラレルポート](../Page/パラレルポート.md "wikilink")の接続をサポート
  - [クリップボード](../Page/クリップボード.md "wikilink")の共有

RDP 6.0では、以下の強化がされた。

  - シームレス ウィンドウのサポート
  - 32ビットカラーのサポート（Windows Server 2008 より24ビットが廃止になり、32ビットを代わりに使用する必要あり）
  - 1600×1200以上の画面解像度のサポート
  - TLS 1.0の暗号化に加えて認証もサポート
  - 複数モニタのサポート
  - 帯域幅の改善
  - [ClearType](../Page/ClearType.md "wikilink")やAero Glassテーマのサポート
  - [Windows Presentation Foundationアプリケーションのリモーティングのサポート](../Page/Windows_Presentation_Foundation.md "wikilink")
  - [IIS 7.0を通しての](../Page/Internet_Information_Services.md "wikilink")[HTTPS](../Page/HTTPS.md "wikilink")接続のサポート

RDP 7.1では、以下の強化がされた。

  - RemoteFX

## 歴史

RDPの前身は米国[シトリックス・システムズ](../Page/シトリックス・システムズ.md "wikilink")が開発した[WinFrameと呼ばれる技術である](https://ja.wikipedia.org/wiki/Citrix_WinFrame "wikilink")。WinFrameは、Windows NTを複数の端末から、複数のユーザが同時利用できるようにする拡張機能で、1995年に発表され、シトリックス・システムズの主力商品となった。

この「ターミナル サービス」は、WinFrame同様、複数のユーザが複数のクライアント端末からサーバとして動作しているWindows NT機に接続して利用できるサービスで、この機能によって、Windowsはリモートからも操作できるOSになった。「ターミナル サービス」は、その後「リモート デスクトップ」に名称を変更し、Windows XP以降ではOSの標準機能として組み込まれることになった。

RDPのバージョンはいきなり4.0から始まっていて、Windowsのバージョンに合わせている。

  - Version 4.0
    [ITU-T](../Page/ITU-T.md "wikilink")プロトコル (T.128) を基に、Windows NT 4.0 Terminal Serverのターミナル サービスとして搭載された。

  - Version 5.x

:;Version 5.0

::Windows 2000 Serverのターミナル サービスとして搭載され、ローカル プリンタのサポートやネットワーク帯域幅の使用の改善を行った。

:;Version 5.1

::Windows XPに搭載され、24ビット カラーのサポートやサウンドの再生をサポートした。

:;Version 5.2

  -

      -
        Windows Server 2003に搭載され、コンソールモード接続やセッション ディレクトリとローカル リソース マッピングをサポートした。

  - Version 6.x

:;Version 6.0

::Windows Vista, Windows XP SP2, Windows Server 2003 SP1/SP2, Windows Embededd CE 6.0 R2に搭載され、多くの機能強化が含まれた。ネットワークレベル認証、マルチモニタなど。

:;Version 6.1

  -

      -
        Windows Vista SP1, Windows Server 2008, Windows XP SP3に搭載された。「TS RemoteApp」{{·}}「TS Gateway」{{·}}「TS EasyPrint」機能が追加された。

  - Version 7.x

:;Version 7.0

::Windows 7, Windows Server 2008 R2に搭載された。本バージョンよりサーバ側の名称がターミナル サービスからリモート デスクトップ サービスに変更になった。デスクトップ コンポジションを Windows Vista Professional, Windows 7 Professionalやそれ以上で有効にすれば[Windows Aeroを利用できる](../Page/Windows_Aero.md "wikilink")。しかし、Windows AeroのAero GlassはWindows 8で廃止されたため、Windows Vista, 7でしか利用できない。また、Aero Glassはサーバ／クライアントが同じバージョンでないと利用できない\[1\]。また当初、[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")のクライアントレンダリングを行う計画があったが、リリース直前に廃止になった\[2\]。クライアントレンダリングしているのは、言葉の定義として動画のデコードはクライアントレンダリングに含めないとすると、RDP 4.0からやっている[GDIのクライアントレンダリングのみであり](../Page/Graphics_Device_Interface.md "wikilink")、それ以外は静止画や動画で転送している。

:;Version 7.1

  -

      -
        Windows 7 SP1, Windows Server 2008 R2 SP1に標準搭載された。RemoteFXが追加された。RemoteFXにより[Hyper-V](../Page/Hyper-V.md "wikilink")との組み合わせでGPU仮想化、USBリダイレクションが利用可能になった。

  - Version 8.x

:;Version 8.0

::[Windows 8や](https://ja.wikipedia.org/wiki/Windows_8 "wikilink")[Windows Server 2012から標準搭載](https://ja.wikipedia.org/wiki/Windows_Server_2012 "wikilink")。Windows 7 SP1, Windows Server 2008 R2 SP1もWindows Updateすることで利用可能。TCPに加えてUDP （ポート3389）も併用するようになった。パフォーマンスの改善。マルチタッチ対応などRemoteFXの強化\[3\]。

:;Version 8.1

  -

      -
        [Windows 8.1や](https://ja.wikipedia.org/wiki/Windows_8.1 "wikilink")[Windows Server 2012](https://ja.wikipedia.org/wiki/Windows_Server_2012 "wikilink") R2から標準搭載。Windows 7 SP1, Windows Server 2008 R2 SP1もWindows Updateすることで利用可能。

  - Version 10.x

:;Version 10.0

  -

      -
        [Windows 10に標準搭載](https://ja.wikipedia.org/wiki/Windows_10 "wikilink")。

## Windows Server のライセンス

リモートデスクトップを使用するには、基本的には以下の Windows Server のライセンスが必要である。括弧の意味は演算子の優先順位を表現する意味。

  - 仮想化なし：CAL + RDS CAL
  - 仮想化あり：CAL + RDS CAL + (VDA or SA)

なお、これらはWindows Serverのライセンスであり、RDP以外のプロトコルを使用しても必要。そして、上記のルールを基本に、様々な例外条項があり、複雑なため詳細はマイクロソフトのホームページを参照。

仮想化なしとは、リモート・セッションで使う場合のこと。仮想化ありとはHyper-V + RemoteFXなどで使用する場合の事。

略語の意味は以下の通り。

  - CAL: Client Access License
  - RDS: Remote Desktop Service
  - VDA: Virtual Desktop Access
  - SA: Service Assurance

## マイクロソフト以外による実装

RDPのクライアント、サーバにはマイクロソフト以外により開発されたサブセットの製品も多数存在する。一例としては、オープンソースのコマンドラインのクライアント[rdesktop](https://ja.wikipedia.org/wiki/rdesktop "wikilink")がLinux/Unix, またWindowsオペレーティングシステムに提供されている。GUIのクライアントも多数存在する。一例として [rdesktop](https://ja.wikipedia.org/wiki/rdesktop "wikilink")をベースにした [:en:tsclient](https://ja.wikipedia.org/wiki/:en:tsclient "wikilink") と [:en:KRDC](https://ja.wikipedia.org/wiki/:en:KRDC "wikilink")があり、Macintosh用には [CoRD](https://ja.wikipedia.org/wiki/CoRD "wikilink") がある\[4\]。Microsoft client for OS Xと異なり、CoRDはウインドウ1つにすべてのリモートセッションをタブで表示するようになっており、 [ZDNet](../Page/ZDNet.md "wikilink")のレビューでは混乱することが少ないと評価されている\[5\]。

別の2011年に行われたレビューでは CoRDの接続の安定性はマイクロソフトのOS Xクライアントに勝るとしている\[6\]。

2009年にrdesktopより分岐して[FreeRDP](https://ja.wikipedia.org/wiki/FreeRDP "wikilink")プロジェクトが立ち上がり、よりモジュラー化されたコードと、既知の各種問題の解決、および新機能の実装を目標に掲げた\[7\]。FreeRDPはコンソールアプリのクライアントxfreerdpを備え、RDP6で登場したシームレスウインドウを実装する。その他[GTK](https://ja.wikipedia.org/wiki/GTK "wikilink")アプリケーションの[:en:Remmina](https://ja.wikipedia.org/wiki/:en:Remmina "wikilink")\[8\]が存在する。

Remote Desktop Protocolのサーバのオープンソースな実装としては、Unix では[FreeRDP](https://ja.wikipedia.org/wiki/FreeRDP "wikilink") と[xrdp](https://ja.wikipedia.org/wiki/xrdp "wikilink")が存在する。Windowsのリモート デスクトップ クライアントからこのサーバに接続することもできる。プロプライエタリなRDPクライアント製品である[:en:rdpclient](https://ja.wikipedia.org/wiki/:en:rdpclient "wikilink")などは、スタンドアローンのアプリケーションとしても、クライアントのハードウェアに組み込む形態でも提供される。 新しいアクセス方式である、ブラウザー経由でのアクセスでは、[:en:2X_Software](https://ja.wikipedia.org/wiki/:en:2X_Software "wikilink")の2XApplicationServerおよび2X Clientという無料クライアントがある。

[2X Client](http://www.2x.com/rdp-client/)はUIにタブ切り替えを設けたクライアントで、独自のプロトコルによるサーバ「2X ApplicationServer」「2X SecureRemoteDesktop」と並んでMicrosoft RDPをサポートしている。2Xのサーバー製品を持たないユーザーも、RDPの接続については無償で利用することが出来る。

## RDPを使ったトリック

[VMware](../Page/VMware.md "wikilink")を使ってWindows（ホスト）上で別の仮想Windowsマシン（ゲスト）を走らせるとき、VMware上のゲストのデスクトップを直接使うよりこのゲストに同じホストからRDPでアクセスしたほうが画面更新が圧倒的に速いことがある。

## 関連項目

  - [リモートデスクトップ](https://ja.wikipedia.org/wiki/リモートデスクトップ "wikilink")
  - [リモート デスクトップ サービス](https://ja.wikipedia.org/wiki/リモート_デスクトップ_サービス "wikilink")
  - [rdesktop](https://ja.wikipedia.org/wiki/rdesktop "wikilink")
  - [FreeRDP](https://ja.wikipedia.org/wiki/FreeRDP "wikilink")
  - [xrdp](https://ja.wikipedia.org/wiki/xrdp "wikilink")
  - [Citrix WinFrame](https://ja.wikipedia.org/wiki/Citrix_WinFrame "wikilink")

## 参照

## 外部リンク

  - [Remote Desktop Services](http://technet.microsoft.com/ja-jp/library/cc770412.aspx) - [TechNet](https://ja.wikipedia.org/wiki/TechNet "wikilink")
  - \[<http://msdn.microsoft.com/en-us/library/bb892075(v=vs.85>).aspx Remote Desktop Services (Windows)\] - [MSDN](https://ja.wikipedia.org/wiki/MSDN "wikilink")
  - [MS-RDPBCGR: Remote Desktop Protocol: Basic Connectivity and Graphics Remoting](http://msdn.microsoft.com/en-us/library/cc240445.aspx) - プロトコルの仕様書
  - [RDP - The Wireshark Wiki](http://wiki.wireshark.org/RDP) - プロトコルの解析
  - [2X Software 日本語サイト 2X Software 日本語サイト](http://www.2x.com/ja/) 有償のサーバー製品、無償のクライアントを提供している
  - [2XApplicationServerXG](http://www.t4u.asia/product/2xas.html) 日本代理店 T4U株式会社
  - [Remmina](http://sourceforge.net/projects/remmina/) SourceForgeのプロジェクト
  - [FreeRDP](http://www.freerdp.com/) 公式サイト

[Category:Microsoft_server_technology](https://ja.wikipedia.org/wiki/Category:Microsoft_server_technology "wikilink") [Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:リモートデスクトップ](https://ja.wikipedia.org/wiki/Category:リモートデスクトップ "wikilink")

1.  [Aero Glass Remoting in Windows Server 2008 R2 - Remote Desktop Services (Terminal Services) Team Blog - Site Home - MSDN Blogs](http://blogs.msdn.com/b/rds/archive/2009/06/23/aero-glass-remoting-in-windows-server-2008-r2.aspx)
2.  [RDP 7 の変更 - 川西 裕幸のブログ - Site Home - MSDN Blogs](http://blogs.msdn.com/b/hiroyuk/archive/2009/06/26/9804555.aspx)
3.  [リモート デスクトップ プロトコル (RDP) 8.0 新機能と簡易パフォーマンス検証](http://download.microsoft.com/download/0/7/B/07BE7A3C-07B9-4173-B251-6865ADA98E5D/WS2012_RDP_Performance.pdf)
4.
5.
6.
7.  FreeRDPは、\*nuxにてWindowsサーバやワークステーションへのアクセスのため長年愛用されてきたrdesktopの後継である。FreeRDPの目標は、キーボード配列の拡充とWindows 6.0 (Vista/2008),6.1 (7/2008R2) で実装された新しいRDPプロトコルのサポートの2つである（READMEより）。
8.