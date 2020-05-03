> この記事は[Internet Information Services](https://ja.wikipedia.org/wiki/Internet_Information_Services)から翻訳されています。


**Microsoft Internet Information Services** (IIS) は、[Microsoft Windowsの標準](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Webサーバ](../Page/Webサーバ.md "wikilink")ー（[アプリケーションサーバ](../Page/アプリケーションサーバ.md "wikilink")ー）[サービス](../Page/サービス.md "wikilink")である。[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")/[HTTPS](../Page/HTTPS.md "wikilink")、[FTP](../Page/File_Transfer_Protocol.md "wikilink")、[SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")、[NNTP等の基本的なプロトコルはサポートしている](../Page/Network_News_Transfer_Protocol.md "wikilink")。クライアント版に付属するIISでは機能制限が行われている\[1\]。

もともとInternet Information Serverという名称で、[Windows NT](../Page/Microsoft_Windows_NT.md "wikilink") Server上で稼働する[アドオン](https://ja.wikipedia.org/wiki/アドオン "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")という位置付けであったが、[Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink") Server登場時にシステムの標準サービスに位置付けられ、現名称に改められた。

## 特徴

インストールした時点でIISの仕事は始まっており、指定されたフォルダにhtmlテキストを保存し、設定することでwebページの公開は可能である。またサーバ版の場合、[Windows Server Update Servicesや](../Page/Windows_Server_Update_Services.md "wikilink")、[Microsoft Exchange Server等のアプリケーションと関連付ける事で](../Page/Microsoft_Exchange_Server.md "wikilink")、サーバアプリケーションをブラウザ越しに、よりグラフィカルに設定させることが出来るため、ある意味[マイクロソフト](../Page/マイクロソフト.md "wikilink")を象徴するコンポーネントといえる。

かつてのバージョンでは、IIS自身にSMTPサーバ機能が付加されており、Windows Server 2003のPOP3サーバ機能と合わせて簡易なメールサーバを構成できた。これはIISのエラー情報を管理者に通知するための機能の応用であるため、Exchange Serverのように本格的なメールサーバを構築することは出来ない。なお、SMTPサーバ機能はIIS 7.0より削除された。

そのほか[バーチャルドメイン](https://ja.wikipedia.org/wiki/バーチャルドメイン "wikilink")等の機能も持つが、パーミッション（アクセス権限）設定が他のWebサーバソフトよりも複雑である。\[2\]

## バージョン

  - IIS 1.0
    [Windows NT 3.51](https://ja.wikipedia.org/wiki/Microsoft_Windows_NT#Windows_NT_3.51（1995年） "wikilink") のアドオンパックとして提供されたバージョンである\[3\]。
  - IIS 2.0
    [Windows NT 4.0](https://ja.wikipedia.org/wiki/Microsoft_Windows_NT_4.0 "wikilink") に付属するバージョンである。
  - IIS 3.0
    Windows NT 4.0 Service Pack 3 に付属するバージョンである。
  - IIS 4.0
    Windows NT 4.0 Option Pack に付属するバージョンである。
  - IIS 5.0
    [Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink") に付属するバージョンである。Windows 2000 のサーバー エディションでは OS インストール直後に標準で有効となっている。
  - IIS 5.1
    [Windows XP Professional](../Page/Microsoft_Windows_XP.md "wikilink") に付属するバージョンである。OS インストール直後は標準で有効となっていない。
  - IIS 6.0
    [Windows Server 2003](../Page/Microsoft_Windows_Server_2003.md "wikilink") と Windows XP Professional x64 Edition に付属するバージョンである。
    安全性の向上として IIS 5.0 では [Windows Server](../Page/Windows_Server.md "wikilink") のインストール完了直後から IIS が機能していたが、このバージョンから明示的にインストールしない限り無効化されている。また、全面的にソースコードが書き直された。
    アプリケーションを実行するためのワーカープロセスはアプリケーションごとにプロセスを独立させて動作させることが可能となり、高可用性なものとなった。
    アプリケーションコンポーネントはユーザーモードに残したまま、送受信を行うコンポーネントはカーネルモードに移された。カーネルモードでもキャッシュを行うなどにより、パフォーマンスが向上した。
    サーバー構成のメタデータは、それまでのバイナリ形式から [XML](../Page/Extensible_Markup_Language.md "wikilink") 形式に変更された。
  - IIS 7.0
    [Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") と [Windows Server 2008](../Page/Microsoft_Windows_Server_2008.md "wikilink") に付属するバージョンである。Windows Vista は Windows Vista Service Pack 1 で Windows Server 2008 と同じ [FastCGI](../Page/FastCGI.md "wikilink") に標準で対応したものに変更された。
    IIS の機能のモジュール化が行われた。
    Server Core インストールで IIS の機能を有効化させることができるが、静的 Web サイトのみ対応し、ASP.NET 等の動的 Web サイトを構築できない。
  - IIS 7.5
    [Windows 7](../Page/Microsoft_Windows_7.md "wikilink") と [Windows Server 2008 R2](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2008_R2 "wikilink") に付属するバージョンである。
    IIS とは切り離されて開発・提供されていたモジュール FTP 7.5 と WebDAV 7.5 が以前のそれらと置き換えられた。
    Server Core インストールで [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") を使用することが可能となったため、Server Core インストールでも ASP.NET の使用が可能となった。
  - IIS 8.0
    [Windows 8](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink") と [Windows Server 2012](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2012 "wikilink") に付属するバージョンである。
    単一の SSL 証明書ストアによる SSL 証明書配布と管理する機能や、指定要求数を越えた IP アドレスをブロックする機能、指定期間内に FTP ログイン失敗を繰り返した場合の FTP アクセスの制限する機能、[Server Name Indication](https://ja.wikipedia.org/wiki/Server_Name_Indication "wikilink") の機能らが追加された。[WebSocket](https://ja.wikipedia.org/wiki/WebSocket "wikilink") プロトコルに対応した。
    [NUMA](../Page/NUMA.md "wikilink") ハードウェアのサポートが行われることによりサーバー資源の効率化が可能となった。アプリケーション プールのサーバー資源の利用調整機能の強化が行われ、複数の Web サイトを単一のアプリケーション プールで展開した際のパフォーマンス低下の防止が可能となった。
    ワーカープロセスの[サンドボックス化などの安全性の向上が行われた](../Page/サンドボックス_\(セキュリティ\).md "wikilink")。
  - IIS 8.5
    [Windows 8.1](https://ja.wikipedia.org/wiki/Microsoft_Windows_8#Windows_8.1 "wikilink") と [Windows Server 2012 R2](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2012_R2 "wikilink") に付属するバージョンである。
    カスタマイズ可能な W3C ログ形式や Event Tracing for Windows の対応等のログ強化が行われた。
    従来までのアイドル状態のワーカープロセスを終了させる方式からページアウト化する方式に変更、サイトのアクティベーションの方式の変更等による初回アクセスのパフォーマンスの向上が行われる。
  - IIS 10.0
    [Windows 10](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink") と [Windows Server 2016](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2016 "wikilink") に付属するバージョンである。
    2015年2月に正式な仕様が発表された [HTTP/2](https://ja.wikipedia.org/wiki/HTTP/2 "wikilink") に対応する。

## IIS Express

IIS に比べて対応機能が少ない「ASP.NET 開発サーバー」 (Cassini) を利用せずに IIS の全機能を開発環境で使用するために公開された。ASP.NET 開発サーバーと同様に IIS のインストールが不要で、[localhost](https://ja.wikipedia.org/wiki/localhost "wikilink") 接続要求のみ受け付ける（ただし、設定すればlocalhost以外からの接続要求も受け付けることが出来る）。また、古いバージョンの OS でも新しい IIS の機能を使用することができる。

IIS 7.5 と同等の IIS Express 7.5、IIS 8.0 と同等の IIS Express 8.0 が公開されており、[Visual Studio 2010 Service Pack 1](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio#Visual_Studio_2010 "wikilink") で対応し\[4\]、[Visual Studio 2012](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio#Visual_Studio_2012 "wikilink") で ASP.NET 開発サーバーから置き換えられた\[5\]。

## セキュリティ

IIS は当初、多くのそして重大な[セキュリティホール](../Page/セキュリティホール.md "wikilink")が頻繁に発見された。過去には[Code Redや](../Page/Code_Red.md "wikilink")[Nimda](../Page/Nimda.md "wikilink")といった[ワームの蔓延により大規模な障害を引き起こした](../Page/ワーム_\(コンピュータ\).md "wikilink")。特にWindows 2000では標準で組み込まれるため被害を大きくした。

IIS 6.0において[アーキテクチャを過去のIISに比べ大幅に変更し](../Page/コンピュータ・アーキテクチャ.md "wikilink")、発表から2007年1月の間にわずか3つの脆弱性しか発見されないレベルまでセキュリティを向上させている。また、安全性確保のため初期状態ではインストールされないようになった。

マイクロソフトでは旧バージョンのIIS 4.0、IIS 5.0、IIS 5.1に対しては、セキュリティ対策用のツールとして「IIS Lockdown Wizard ツール」を配布し、セキュリティの向上を促している。

## 脚注

## 関連項目

  - [XSP (Webサーバ)](https://ja.wikipedia.org/wiki/XSP_\(Webサーバ\) "wikilink")

## 外部リンク

  -
  - [IIS 関連情報 | Technet](http://technet.microsoft.com/ja-jp/bb466129.aspx)

  - [IIS Lockdown Wizard 2.1 ツール (Microsoft Japan)](http://www.microsoft.com/japan/technet/security/tools/locktool.mspx)

[Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:FTPサーバ](https://ja.wikipedia.org/wiki/Category:FTPサーバ "wikilink") [Category:Microsoft_server_technology](https://ja.wikipedia.org/wiki/Category:Microsoft_server_technology "wikilink")

1.
2.  [NTFSの](../Page/NT_File_System.md "wikilink")[ACLなど](../Page/アクセス制御リスト.md "wikilink")、[Windows NT系システムでのパーミッション管理について一定の知識を要する](../Page/Windows_NT系.md "wikilink")。
3.
4.
5.