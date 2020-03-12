> この記事は[Microsoft Windows Server 2008](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2008)から翻訳されています。


**Windows Server 2008** （ウィンドウズ サーバー ）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発・提供する[Windows Server 2003の後継となる](../Page/Microsoft_Windows_Server_2003.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")向け[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS)。

Windows Server 2008の[コードネーム](../Page/コードネーム.md "wikilink")は**Windows Server Codename "Longhorn"**あるいは俗に**Longhorn Server**とも呼ばれていた。[Windows Vistaをベースに開発されている](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。

2007年5月16日、正式名称をMicrosoft Windows Server 2008と発表。製品版は米国で[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[2月27日](../Page/2月27日.md "wikilink")に提供を開始した。日本では[4月15日](../Page/4月15日.md "wikilink")から提供開始。

## サポートするプラットフォーム

Windows Server 2008は64ビット（[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")および[IA-64](../Page/IA-64.md "wikilink")）環境を主軸にしているが、32ビット ([x86](https://ja.wikipedia.org/wiki/x86 "wikilink")) 環境もサポートしている。次バージョンの[Windows Server 2008 R2では](https://ja.wikipedia.org/wiki/Windows_Server_2008_R2 "wikilink")64ビット環境のみのサポートとなり、x86環境には非対応となった為、Windows Server 2008が32ビット環境に対応した最後のサーバー用Windowsとなった。\[1\]

## エディション

  - Windows Server 2008 Standard (x86, x64)
  - Windows Server 2008 Standard without Hyper-V (x86, x64)
  - Windows Server 2008 Enterprise (x86, x64)
  - Windows Server 2008 Enterprise without Hyper-V (x86, x64)
  - Windows Server 2008 Datacenter (x86, x64)
  - Windows Server 2008 Datacenter without Hyper-V (x86, x64)
  - Windows Server 2008 for Itanium-based Systems
  - Windows Web Server 2008
  - Windows HPC Server 2008 (x64)
  - Windows Storage Server 2008 (x86, x64)
  - Windows Small Business Server 2008 (x64)
  - Windows Essential Small Business Server 2008 (x64)
  - Windows Server 2008 Foundation (x64)

## 特徴

  - Server Core
    Server Coreとしてインストールすると、主に[コマンド プロンプトがユーザーとの対話の](https://ja.wikipedia.org/wiki/cmd.exe "wikilink")[インタフェースになる](../Page/インタフェース_\(情報技術\).md "wikilink")。要望が多かったりしたものなどはウィンドウを表示して使える。Server Core は、[Active Directoryの](../Page/Active_Directory.md "wikilink")[ドメインコントローラ](../Page/ドメインコントローラ.md "wikilink")、[DNSサーバ](../Page/Domain_Name_System.md "wikilink")、[DHCPサーバ](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")、[ファイルサーバ](../Page/ファイルサーバ.md "wikilink")、[Windows Media サーバ](https://ja.wikipedia.org/wiki/Windows_Media "wikilink")、[Webサーバ](../Page/Webサーバ.md "wikilink")、Hyper-V サーバー等として機能する。[Windows Explorerがインストールされないため](../Page/Windows_Explorer.md "wikilink")[Internet Explorer等がインストールされず](../Page/Internet_Explorer.md "wikilink")、また[.NET Frameworkも](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[GUIが前提の](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")が含まれているためインストールされない。Server Core は、ユーザーが直接操作するような環境ではなく、インフラストラクチャとして配置するサーバーに最も有効である。Server Core でインストールされたコンピュータは、リモート コンピュータで [MMC](https://ja.wikipedia.org/wiki/Microsoft_管理コンソール "wikilink") を使って管理する。また、インストールされるコンポーネントがより少なくなることで、より攻撃される面が少ない。

  - Hyper-V

<!-- end list -->

  -
    Hyper-Vとは、[仮想マシンモニタである](../Page/仮想機械.md "wikilink")。[Intel VT](../Page/インテル_バーチャライゼーション・テクノロジー.md "wikilink") や [AMD Virtualization](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink") といった[CPU](../Page/CPU.md "wikilink")の[仮想化](../Page/仮想化.md "wikilink")支援機能を利用し、1台のサーバマシンで複数のOSの実行を実現する。Windows Server 2008の他に、Windows Server 2003と[Windows 2000 Serverおよび](../Page/Microsoft_Windows_2000.md "wikilink")[Linux](../Page/Linux.md "wikilink")が、Hyper-V 上での実行対象としてサポートされる。x64用のみの提供となっている。
  - EFIのサポート
    従来の[BIOSに替わる](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")[UEFIのサポート](../Page/Unified_Extensible_Firmware_Interface.md "wikilink")（64ビット環境のみ）。
  - Active Directory
    Active Directoryに登録されるユーザ名の[ふりがな](https://ja.wikipedia.org/wiki/ふりがな "wikilink")への対応やロールが強化される。
  - Windows PowerShell
    Windows Server 2008から標準で[Windows PowerShellが搭載される](https://ja.wikipedia.org/wiki/Windows_PowerShell "wikilink")。[コマンド プロンプトや](https://ja.wikipedia.org/wiki/cmd.exe "wikilink")[Windows Scripting Hostに置き換わるコマンドラインベースの管理ツール](https://ja.wikipedia.org/wiki/Windows_Scripting_Host "wikilink")。Windows PowerShellを利用するには、.NET Frameworkをインストールする必要がある。
  - ターミナル サービス
    ターミナル サービスはいくつかの機能が追加された。[RDP](../Page/Remote_Desktop_Protocol.md "wikilink") 6.1をインストールしているWindows Server 2008やWindows Vista SP1、Windows XP SP3は標準で対応し、Windows Vistaはサービスパック 1への更新で、Windows XP SP2やWindows Server 2003 SP1以降のシステムはRDP 6.1をWindows Updateでインストールすることにより対応する。サーバー上にある1つのアプリケーションの共有、またそのゲートウェイ サービス、クライアント側のプリンタの共有ということが可能となった。
  - その他
    [IIS (Internet Information Services)](../Page/Internet_Information_Services.md "wikilink") 7.0
    [Remote Installation Servicesの後継となるWindows展開サービス](https://ja.wikipedia.org/wiki/Remote_Installation_Services "wikilink")
    WIM (Windows Image Format) を用いたセットアップと配置
    OSの完全なコンポーネント化
    Windows Vistaの[グループポリシー](https://ja.wikipedia.org/wiki/グループポリシー "wikilink")に対応
    [SMB](../Page/Server_Message_Block.md "wikilink") 2.0の実装によるNTベースのSMB利用環境に対応
    [ケルベロス認証](../Page/ケルベロス認証.md "wikilink")の256ビット[AESのサポート](../Page/Advanced_Encryption_Standard.md "wikilink")
    [iSNSのサポート](https://ja.wikipedia.org/wiki/Internet_Storage_Name_Service "wikilink")
    [Secure Socket Tunneling Protocolのサポート](https://ja.wikipedia.org/wiki/w:en:Secure_Socket_Tunneling_Protocol "wikilink")
    Self-healing NTFSという[NTFSの強化](../Page/NT_File_System.md "wikilink")
    DHCPv6等の[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")環境への対応

一部の機能は Windows Server 2003 でもサポートされる。

## 脚注

## 関連項目

  - [Microsoft Servers](../Page/Microsoft_Servers.md "wikilink")
  - [Xen (仮想化ソフトウェア)](../Page/Xen_\(仮想化ソフトウェア\).md "wikilink")

## 外部リンク

  -
  - [Windows Server Tech Center](http://technet.microsoft.com/ja-jp/windowsserver)

  - [システム要件](http://technet.microsoft.com/ja-jp/windowsserver/bb414778.aspx)

[Category:Windows_Server](https://ja.wikipedia.org/wiki/Category:Windows_Server "wikilink") [Category:2008年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2008年のソフトウェア "wikilink")

1.