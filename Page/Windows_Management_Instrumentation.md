> この記事は[Windows Management Instrumentation](https://ja.wikipedia.org/wiki/Windows_Management_Instrumentation)から翻訳されています。


**Windows Management Instrumentation** (**WMI**) は、[Windows Driver Modelへの拡張の一種で](../Page/Windows_Driver_Model.md "wikilink")、システムの構成要素について情報収集と通知を行う[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) の[インタフェースを提供する](../Page/インタフェース_\(情報技術\).md "wikilink")。WMI は[Distributed Management Task Force](../Page/Distributed_Management_Task_Force.md "wikilink") (DMTF) の定めた [Web-Based Enterprise Management](../Page/Web-Based_Enterprise_Management.md "wikilink") (WBEM) と [Common Information Model](../Page/Common_Information_Model.md "wikilink") (CIM) 標準の[マイクロソフト](../Page/マイクロソフト.md "wikilink")による実装である。

WMI により、[Windowsを搭載した](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")や[サーバ](../Page/サーバ.md "wikilink")を[VBScript](../Page/VBScript.md "wikilink")や[PowerShellのような](https://ja.wikipedia.org/wiki/Windows_PowerShell "wikilink")[スクリプト言語](../Page/スクリプト言語.md "wikilink")で（ローカルでもリモートでも）管理できるようになる。WMIは[Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、[Windows Server 2003](../Page/Microsoft_Windows_Server_2003.md "wikilink")、[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink")、[Windows Me](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink")、[Windows 2000に最初から実装されている](../Page/Microsoft_Windows_2000.md "wikilink")。[Windows 95および](../Page/Microsoft_Windows_95.md "wikilink")[Windows 98向けのWMIはダウンロード可能である](../Page/Microsoft_Windows_98.md "wikilink")\[1\]。

また、マイクロソフトはWMIの[キャラクタユーザインタフェース](../Page/キャラクタユーザインタフェース.md "wikilink")として **Windows Management Instrumentation Command-line** (**WMIC**) を提供している\[2\]。

## WMIの目的

WMIの目的は、オープンな仕様の管理情報を提供することで、各種OS環境で動作する管理[アプリケーション群がそれら情報を共有できるようにすることである](../Page/アプリケーションソフトウェア.md "wikilink")。WMIでは[システム管理](../Page/システム管理.md "wikilink")標準を定め、[Desktop Management Interface](../Page/Desktop_Management_Interface.md "wikilink") (DMI) や[Simple Network Management Protocol](../Page/Simple_Network_Management_Protocol.md "wikilink") (SNMP) といった既存の管理標準との関連も定めている。WMIでは一様なモデルを提供することで他の標準を補っている。このモデルは、任意の情報源からの管理データを共通の方法でアクセスできる管理対象環境を表している。

## 概要

管理技法を統一して単純化するため、DMTFは統一的な方法で管理対象群を表現する[Common Information Model](../Page/Common_Information_Model.md "wikilink") (CIM) を定義した。CIMオブジェクトモデルは、全てのメーカー（[ハードウェア](../Page/ハードウェア.md "wikilink")、[ソフトウェア](../Page/ソフトウェア.md "wikilink")）が統一的に使える用語と意味論を用いた[オブジェクトデータベース](../Page/オブジェクトデータベース.md "wikilink")モデルである。このオブジェクトモデルはCIMリポジトリと呼ばれる[データベース](../Page/データベース.md "wikilink")に実装される。

CIMに基づき、WMIはDMTF標準をWindowsの各要素を表せるように拡張した実際の管理対象要素を含む。また、WMIは[COMにも対応しており](../Page/Component_Object_Model.md "wikilink")、COM対応の各種アプリケーションが管理情報を利用可能としている。

インストール処理の一部として、マイクロソフトのアプリケーションの多く（[Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")、[Exchange Server](https://ja.wikipedia.org/wiki/Exchange_Server "wikilink")、[Microsoft Office](../Page/Microsoft_Office.md "wikilink")、[Internet Explorer](../Page/Internet_Explorer.md "wikilink")、Host Integration Server、Automated Deployment Servicesなど）は標準のCIMを拡張して、それぞれの管理情報をCIMリポジトリに格納する。これを「WMIクラス」と呼び、属性と値の組で管理情報を保持し、メソッドによって何らかのアクションを実行できるようになっている。管理対象へのアクセスは「プロバイダ」と呼ばれるソフトウェアコンポーネントを使って行われる。プロバイダの実体は、[C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")で書かれたCOMオブジェクトを実装した[DLLである](../Page/ダイナミックリンクライブラリ.md "wikilink")。プロバイダは特定の管理情報にアクセスするよう設計されているため、CIMリポジトリは「ネームスペース」と呼ばれる領域に論理的に分割されている。各ネームスペースは特定の管理領域に関わるクラス群についてのプロバイダ群が含まれる（例えば、[Active DirectoryのためのRootDirectoryDAP](../Page/Active_Directory.md "wikilink")、SNMP情報のための RootSNMP、[Internet Information Services情報のためのRootMicrosoftIISv](../Page/Internet_Information_Services.md "wikilink")2など）。

CIMリポジトリ上の様々な管理情報を利用するため、WMIには[SQL](../Page/SQL.md "wikilink")風の言語であるWMI Query Language (WQL) が付属している。

## 開発プロセス

WMIはCIMとプロバイダ群によって管理対象を抽象化しているため、プロバイダの開発にはいくつかのステップが含まれる。主な4つのステップを以下に挙げる。

1.  ステップ1 - 管理対象モデルを作成
      - モデル定義
      - モデル実装
2.  ステップ2 - WMIプロバイダを作成
      - 実装すべきプロバイダの種類を決定
      - プロバイダのホスティングモデルを決定
      - ATLウィザードでプロバイダのテンプレートを作成
      - プロバイダのコードを実装
      - プロバイダを WMIとシステムに登録
3.  ステップ3 - プロバイダのテスト
4.  ステップ4 - 利用者サンプルコードを作成

## WMIプロバイダ

Windows NT 4.0 SP4のころ最初のWMI実装のリリースが行われて以来、マイクロソフトはWindowsにWMIプロバイダを着実に追加してきた。 Windows NT 4.0では、マイクロソフトは15のWMIプロバイダを実装していた。[Windows 2000リリース時にはOSの一部として](../Page/Microsoft_Windows_2000.md "wikilink")29のプロバイダが実装されていた。[Windows Server 2003リリース時には](../Page/Microsoft_Windows_Server_2003.md "wikilink")80のプロバイダが実装されている。[Windows Vistaでは新たなプロバイダが](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")13個追加されており\[3\]、全部で100近くのプロバイダが存在する。これにより、WMIはWindowsにおいて遍在する管理層としての地位を確立しつつある。

このような状況から、[IT](../Page/情報技術.md "wikilink")[システム管理](../Page/システム管理.md "wikilink")の分野ではWMIに基づいたスクリプトや自動化プロシージャの開発が盛んになっている。単なるスクリプトだけでなく、[MOM](https://ja.wikipedia.org/wiki/Microsoft_Operations_Manager "wikilink")、[SMS](../Page/Microsoft_Systems_Management_Server.md "wikilink")、ADS、[HP](../Page/ヒューレット・パッカード.md "wikilink") [OpenView](../Page/OpenView.md "wikilink") for Windows (HPOV)、[BMCソフトウェア](../Page/BMCソフトウェア.md "wikilink")、[CAなどがWMIに基づいて管理情報を提供](https://ja.wikipedia.org/wiki/CA_\(企業\) "wikilink")/操作するユーザインタフェースを管理ソフトウェアに追加している。これによりスクリプト作成ができない管理者も、特にWMIに関する知識を学ばなくともWMIを利用可能となっている。もちろんWMIはスクリプトによって操作可能であるため、スクリプトを使えた方が選択肢は広がる。

## 例

[.NET FrameworkにはWMIのマネージラッパー](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") (System.Management.dll) が用意されており、[System.Management.ManagementClass](https://docs.microsoft.com/ja-jp/dotnet/api/system.management.managementclass)[クラスがCIM管理クラスを表している](../Page/クラス_\(コンピュータ\).md "wikilink")。WMIクラスは、ディスクドライブなら[Win32_LogicalDisk](https://docs.microsoft.com/en-us/windows/desktop/cimwin32prov/win32-logicaldisk)、Notepad.exeのような実行中プログラムなら[Win32_Process](https://docs.microsoft.com/en-us/windows/desktop/cimwin32prov/win32-process)となる。

以下の例は、"MSNdis_80211_ServiceSetIdentifier" を使って、システムが現在接続している[Wi-Fi](../Page/Wi-Fi.md "wikilink")ネットワークの[SSID](https://ja.wikipedia.org/wiki/SSID "wikilink")を探す[C\#プログラムの](../Page/C_Sharp.md "wikilink")[コードである](../Page/ソースコード.md "wikilink")。

``` csharp
ManagementClass mc = new ManagementClass("root\\WMI", "MSNdis_80211_ServiceSetIdentifier", null);
ManagementObjectCollection moc = mc.GetInstances();

foreach (ManagementObject mo in moc)
{
    string wlanCard = (string)mo["InstanceName"];
    bool active = (bool)mo["Active"];
    byte[] ssid = (byte[])mo["Ndis80211SsId"];
}
```

## 参考文献

<references/>

## 外部リンク

  - [WMI at the Windows Hardware Developer Central](http://www.microsoft.com/whdc/system/pnppwr/wmi/default.mspx)
  - [CIM terminology](http://msdn2.microsoft.com/en-us/library/ms811530.aspx)
  - [WMI Overview and Background](http://msdn2.microsoft.com/en-us/library/ms811553.aspx)
  - [WMI and CIM overview](http://msdn2.microsoft.com/en-us/library/ms811552.aspx)
  - [How improved support for WMI makes PowerShell the best environment to use and script WMI](http://blogs.msdn.com/powershell/archive/2006/06/26/647038.aspx)
  - [Working with WMI providers to PowerShell](http://searchwincomputing.techtarget.com/generic/0,295582,sid68_gci1250536,00.html)

[Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:システム管理](https://ja.wikipedia.org/wiki/Category:システム管理 "wikilink") [Category:ネットワーク管理](https://ja.wikipedia.org/wiki/Category:ネットワーク管理 "wikilink") [Category:マネジメント・システム](https://ja.wikipedia.org/wiki/Category:マネジメント・システム "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.  [WMI Redistributable for Windows 95 and Windows 98](http://www.microsoft.com/downloads/details.aspx?familyid=98a4c5ba-337b-4e92-8c18-a63847760ea5&displaylang=en)
2.  [Description of WMIC](http://support.microsoft.com/kb/290216)
3.  [Windows Vista Client Manageability](http://download.microsoft.com/download/b/e/3/be37cbce-425e-45c2-a9f5-378026b5be81/04-d-WinMgmtTech-v03-TOURB-FINAL.ppt) パワーポイント文書