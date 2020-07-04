> この記事は[System Center Operations Manager](https://ja.wikipedia.org/wiki/System_Center_Operations_Manager)から翻訳されています。


**System Center Operations Manager**(SCOM) は[マイクロソフト](../Page/マイクロソフト.md "wikilink")による[Windowsシステムを対象とした性能およびイベント監視製品である](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。従来は **Microsoft Operations Manager**(MOM) と称していた。

ネットワークで接続された複数の[コンピュータ](../Page/コンピュータ.md "wikilink")を監視できる。[Active Directory](../Page/Active_Directory.md "wikilink")、[Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")、[Microsoft Exchange Server](../Page/Microsoft_Exchange_Server.md "wikilink") といった Microsoft Server 製品や SCOM 自身を SCOM で監視可能である。イギリスの企業 Serverware Group plc が開発した SeNTry ELM という[ネットワーク管理](../Page/ネットワーク管理.md "wikilink")システムがベースとなっている\[1\]。[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[6月](../Page/6月.md "wikilink")、その[知的財産権](../Page/知的財産権.md "wikilink")が Mission Critical Software, inc. に買い取られ\[2\]、同社が[NetIQ](http://www.netiq.com/solutions/services/default.asp) と合併し\[3\]、その後 Attachmate に買収された。

## 基本概念

基本的な考え方は、「エージェント」と呼ばれる小さなソフトウェアを監視対象のコンピュータ上に置く。エージェントはコンピュータをいくつかの観点で監視する。例えば、Windows Event Log を通して、そのコンピュータ上のアプリケーションが発生する警報やイベントを監視する。警報を検出すると、エージェントはそれを SCOM サーバにフォワードする。SCOM サーバにはデータベースが付属しており、警報の履歴がそこに格納されている。SCOM サーバは受け取った警報にフィルタリング規則を適用し、その規則に従って人間に通知したり（電子メール、ポケットベルなど）、警報の原因解決のための何らかの[ワークフロー](../Page/ワークフロー.md "wikilink")を起動したりする。

SCOM では、特定の監視対象アプリケーション向けのフィルタリング規則群を *management pack* と呼ぶ。マイクロソフトや他のソフトウェアベンダーが各製品についての management pack を提供するが、SCOM にはユーザーがそれを編集したり新たに作成できる機能もある。エージェントのインストール、監視対象コンピュータの設定、management pack 作成にはアドミニストレータ権限が必要だが、警報履歴は一般ユーザーでも参照可能である。

複数の SCOM サーバを連携させ、Windows ドメインやネットワーク境界を越えて監視することもできる。[Webサービス](../Page/Webサービス.md "wikilink")を利用して、他のネットワーク管理アプリケーションと警報情報をやり取りすることもできる。

## コマンドシェル

Operations Manager 2007 では、新たにコマンドシェルと呼ばれる[コマンドラインインタフェースが導入された](../Page/キャラクタユーザインタフェース.md "wikilink")。[Windows PowerShellをカスタマイズしたもので](https://ja.wikipedia.org/wiki/Windows_PowerShell "wikilink")、Operations Manager のデータにアクセスし、操作することができる\[4\]。Windows PowerShell と同様、[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")と [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 2.0 に基づいている。PowerShell よりもコマンドや機能が拡張されており、Operations Manager の操作を自動化できる\[5\]。

## バージョン

  - Microsoft Operations Manager 2000
  - Microsoft Operations Manager 2005
      - Microsoft Operations Manager 2005 Service Pack 1
  - System Center Operations Manager 2007
  - System Center 2012 Operations Manager
  - System Center 2012 R2 Operations Manager
  - System Center 2016 Operations Manager
  - System Center Operations Manager 2019

## 関連項目

  - [Microsoft Servers](../Page/Microsoft_Servers.md "wikilink")
  - [Microsoft System Center](../Page/Microsoft_Servers.md "wikilink")
  - [Microsoft Systems Management Server](../Page/Microsoft_Systems_Management_Server.md "wikilink")

## 脚注

## 参考文献

  -
## 外部リンク

  - [Microsoft System Center Operations Manager マイクロソフト 公式技術情報](http://technet.microsoft.com/ja-jp/systemcenter/om/default)
  - [Microsoft System Center Operations Manager 2007 R2 評価版のダウンロード](http://technet.microsoft.com/ja-jp/bb738014)
  - [Operations Manager 製品ホーム](http://www.microsoft.com/japan/mom/default.mspx)
  - [System Center Operations Manager 2007](http://www.microsoft.com/systemcenter/opsmgr/default.mspx)
  - [MOM についての Microsoft Tech Net ガイド](http://technet.microsoft.com/ja-jp/opsmgr/bb498231.aspx)
  - [Microsoft Operations Manager SDK](http://msdn2.microsoft.com/en-us/library/aa505337.aspx) (*in [MSDN](../Page/Microsoft_Developer_Network.md "wikilink")*)
  - [Official Blog: System Center Operations Manager Command Shell](http://blogs.msdn.com/scshell/default.aspx)
  - [MOM and System Center site](http://www.contoso.se)
  - [Authoring Guide for System Center Operations Manager 2007](http://www.authormps.com)

[Category:Microsoft_server_technology](https://ja.wikipedia.org/wiki/Category:Microsoft_server_technology "wikilink")

1.
2.
3.
4.
5.