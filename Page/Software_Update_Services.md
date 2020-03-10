> この記事は[Software Update Services](https://ja.wikipedia.org/wiki/Software_Update_Services)から翻訳されています。


**Software Update Services**（ソフトウェアアップデートサービス）（以下SUS）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が2002年6月24日にリリースしたWindowsの更新プログラム配布アプリケーションである。MicrosoftのWWWサイトからダウンロード可能であったが、2007年7月10日をもってサポートが終了した\[1\]。後継製品として、[Windows Server Update Servicesがある](https://ja.wikipedia.org/wiki/Windows_Server_Update_Services "wikilink")。

## 機能

マイクロソフトが[Microsoft Updateを通じて提供するWindows関連の各種更新プログラムを](https://ja.wikipedia.org/wiki/Microsoft_Update "wikilink")、 [Local Area Network内のSUSサーバにダウンロードして保管し](../Page/Local_Area_Network.md "wikilink")、クライアントPCで実行する自動更新からのリクエストに応じて更新プログラムを提供する、 [クライアントサーバモデルである](https://ja.wikipedia.org/wiki/クライアント・サーバシステム "wikilink")。

SUSサーバは、サーバ内に保存した更新プログラムの一覧をWWW管理コンソール画面経由で管理者に提示し、管理者からインストールを承認された更新プログラムのみをクライアントPCに提供する。

クライアントPCは、[グループポリシー](https://ja.wikipedia.org/wiki/グループポリシー "wikilink")または[レジストリ](../Page/レジストリ.md "wikilink")の設定によって指定されたSUSサーバに対して、指定された間隔（既定はおよそ22時間おき）でアクセスし、自身が必要とする更新プログラムのうち、インストールを許可されたものだけを選択的にダウンロードしてインストールを行う。

## インストール要件

### サーバ

マイクロソフトが提示する、SUSサーバのインストール要件は以下の通りである。ハードウェアについては、 15,000台をサポートするハードウェアである\[2\]。

  - ソフトウェア
      - Windows 2000 Server Service Pack 2 (SP2)以上、あるいはWindows Server 2003 各エディション
      - Microsoft IIS 5.0 以降
      - Microsoft Inernet Explorer 5.5 以降
  - ハードウェア
      - Pentium-III 700MHz以上のCPU
      - 512MB以上のRAM
      - ハードディスク空容量6GB以上（セットアップおよびセキュリティパッケージ用）

### クライアント

SUSは、クライアントとして自動更新クライアントを使用する。

  - Windows 2000 SP2（ただし、現実的には自動更新が含まれるSP3以降）
  - Windows XP
  - Windows Server 2003

## SUSの欠点

SUSはクライアントPCに対して、大がかりな変更（クライアント・アプリケーションのインストールなど）を行わずに更新プログラムの配布を可能にした無償の製品という点で画期的であったが、機能的には以下の不備があった。これらを克服するためには、[SMSなどの有償製品を導入するか](https://ja.wikipedia.org/wiki/Microsoft_Systems_Management_Server "wikilink")、[WSUSという後継製品を待つ必要があった](https://ja.wikipedia.org/wiki/Windows_Server_Update_Services "wikilink")。

  - 一律な更新ファイルの配布
    更新プログラムはインストールを承認するか、未承認のままにするか二者択一であり、クライアントPCの配置や利用状況を判断して承認状態を変更することはできなかったため、単一のSUSサーバから配布できる更新ファイルの組み合わせは1種類だけであった。配布する更新ファイルの組み合わせを複数にしたければ、SUSサーバ自体を複数設置して異なる承認状態を設定する必要があった。
  - 更新ファイルのインストール状態
    SUSは更新ファイルの適用結果の分析機能を省略したため、更新プログラムがクライアントPCにインストールされたのかどうかはSUSサーバに集積された統計情報のファイルを解析する以外になく、解析ツールも提供されなかった。クライアントPCが更新プログラムをインストールしたかどうかを正確に判断するためには、クライアントPC上のWindows Update.logファイルおよび更新されたシステムファイルを解析する必要があった。
  - Windows限定の更新ファイル
    SUSで配布できる更新プログラムは、WindowsとInternet Explorerに関するセキュリティ修正プログラム、もしくはService Pack類に限られた。そのため、例えばOfficeアプリケーションにセキュリティ修正プログラムがリリースされた場合、手動でダウンロードしてインストールするか、ユーザにOffice Updateを実施してもらう必要があった。

## 脚注

<references/>

## 外部リンク

  - [Software pdate Services](http://www.microsoft.com/japan/windowsserversystem/sus/) （マイクロソフト）

[en:Windows Server Update Services\#History](https://ja.wikipedia.org/wiki/en:Windows_Server_Update_Services#History "wikilink") [ko:윈도 서버 업데이트 서비스\#역사](https://ja.wikipedia.org/wiki/ko:윈도_서버_업데이트_서비스#역사 "wikilink")

[Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink")

1.  [Microsoft Software Update Services 1.0 のサポート ライフサイクル](http://support.microsoft.com/default.aspx?scid=kb;ja;905682)
2.  Microsoft, "Microsoft Software Update Services の展開（展開についてのホワイト ペーパー）" 2003年1月、P.9