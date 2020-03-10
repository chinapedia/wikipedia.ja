> この記事は[Windows Server Update Services](https://ja.wikipedia.org/wiki/Windows_Server_Update_Services)から翻訳されています。


**Windows Server Update Services**（ウィンドウズサーバーアップデートサービス、以下WSUS ダブルサス）は、[Microsoft社が提供する](../Page/マイクロソフト.md "wikilink")[更新プログラム適用制御用の](../Page/パッチ.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")・[アプリケーションである](../Page/アプリケーションソフトウェア.md "wikilink")。

## リリース履歴

  - WSUS 2.0（2005年8月15日）
  - WSUS 2.0 SP1（2006年6月1日）
  - WSUS 3.0（2007年5月30日）
  - WSUS 3.0 SP1（2008年2月7日）
  - WSUS 3.0 SP2（2009年8月25日）
  - WSUS 4.0（2012年10月26日） - Windows Server 2012に内包
  - WSUS 6.3（2013年10月18日） - Windows Server 2012 R2に内包
  - WSUS 10（2016年9月26日） - Windows Server 2016に内包。Windows Server 2019では同じくバージョン10であるが、ビルド番号が2016と異なる。\[1\]

WSUS 2.0は[Software Update Servicesの後継製品であり](../Page/Software_Update_Services.md "wikilink")、配布可能な更新プログラムの種類やクライアントPCの管理能力が大幅に強化されている。2007年6月1日をもってサポートが終了し、WSUS 2.0 SP1も2009年4月30日でサポートが終了した\[2\]。

[2013年](../Page/2013年.md "wikilink")現在の最新版はWSUS 3.0 SP2で、WSUS 2.0 SP1に対して、プラットホームとして[Windows 2000 Serverがサポートされない](../Page/Microsoft_Windows_2000.md "wikilink")、管理画面が[WEBから](../Page/ウェブページ.md "wikilink")[MMCに変更された](https://ja.wikipedia.org/wiki/Microsoft_管理コンソール "wikilink")、管理画面がWSUSのサーバ機能と分離された、レポート機能を大幅に充実させた、承認状態を簡略化したなど、かなりの変更が盛り込まれている。

## 機能

Microsoftが提供する、Windows OSやアプリケーションの更新プログラム、デバイスドライバ等（以降「更新プログラム」と表記する）を クライアントPCの「自動更新」コンポーネントを利用して配布する、[クライアント・サーバ・モデルのアプリケーションである](../Page/クライアントサーバモデル.md "wikilink")。

WSUSのサーバ・コンポーネントをインストールしたサーバ機を「WSUSサーバ」と呼称し、[Microsoft Updateサーバよりダウンロードした更新プログラムをWSUSサーバ内に保管する事が可能である](https://ja.wikipedia.org/wiki/Microsoft_Update "wikilink")。更新プログラムの情報（メタデータ）は、定期的または手動でMicrosoft UpdateサーバとWSUSサーバ間で同期が取られており、WSUSの管理者は、同期されたメタデータを元に更新プログラムをクライアントPCに布するか否かを設定する。インストールの承認時に適用期限（インストール期日）を指定する事も可能である。

WSUSは更新プログラムを「配布」すると説明されていることが多いが、正確にはWSUSサーバに蓄積された更新プログラムを、クライアントPCから能動的に取得しに来る「プル」方式である。

クライアントPCは、[グループポリシー](https://ja.wikipedia.org/wiki/グループポリシー "wikilink")またはレジストリによって指定されたWSUSサーバに対して、指定された時間間隔（既定値は約22時間間隔）でアクセスし、自身に適用可能な更新プログラムのうち、管理者によってインストールを承認されたものを認識するとともに、ローカルにダウンロードする。ダウンロードのタイミングは指定できない。

ローカルにダウンロード済みで、すぐにも適用可能な更新プログラムは、グループポリシーまたはレジストリのスケジュール設定に従って、自動または手動で適用される。スケジュール指定による自動インストールの場合でも、クライアントPCに管理者ユーザーがログオン中であれば、更新プログラムが適用可能であることを通知される。

更新プログラムの適用が完了すると、クライアントPCは適用ステータスをWSUSサーバ（グループポリシーの設定では「イントラネット統計サーバ」という）に報告する。WSUSサーバでは、このステータス報告をもとに更新プログラムやクライアントPCごとのレポートを作成する。

更新プログラムのダウンロードはBackground Intelligent Transfer Service (BITS) が実行しており、利用可能なネットワーク帯域に応じて回線がパンクしないように、また更新データの配布によって回線を独占し、ネットワークが使用不可になるような状況にならないように、通信量が自動的に調整される。

### 更新プログラムの承認

WSUS管理者は、管理コンソール上で更新プログラムをどのように配布するか制御する事ができる。配布を許可する場合、更新プログラムに対して「承認」の作業を行う事が必要になる。WSUS 2.0 (SP1) においては、承認には以下の4つの状態がある。

  - インストール
    更新プログラムをクライアントPCがインストールする事を許可する承認状態である。クライアントPCは、この承認状態が指定されている更新プログラムのみダウンロードとインストールを行う。
  - 検出のみ
    クライアントPCに対して、更新プログラムの存在は公開するが、更新プログラムのダウンロードや適用は許可しない承認状態である。クライアントPCは、自身が必要とする更新プログラムの存在を検出してWSUSサーバに報告する。インストール済みの更新プログラムや、様々な理由でインストールが不要な更新プログラムも併せて通知される。
  - 削除
    クライアントPCに対して、更新プログラムの削除（アンインストール）を強制する承認状態である。更新プログラムがアンインストールをサポートしている必要があるが、更新プログラムの依存関係が保てなくなるため、事実上削除が正式にサポートされた更新プログラムはない。
  - 拒否
    検出を拒否する承認状態である。更新プログラムを「拒否」にすると、WSUSの管理コンソールにおいても通常は表示されなくなる。

更新プログラムは当初「未承認」の状態にあるが、WSUSサーバの「自動承認」オプションの設定により、更新プログラムの種類別に自動的に「検出のみ」または「インストール」状態に設定できる。WSUS 2.0 (SP1) サーバの既定のインストールでは、以下の2種類の更新プログラムについて自動的に「検出のみ」のステータスになるようになっている。

  - 重要な更新
  - セキュリティ問題の修正プログラム

WSUS 3.0およびWSUS 3.0 SP1では、未承認状態の既定値が「検出のみ」の承認状態となり、承認状態は「インストール」「削除」「拒否」の3状態に整理・統合されている。また、自動承認オプションが強化されており、「製品」「クラス」「コンピュータ・グループ」に応じてインストールまたは拒否状態を設定できる。

### クライアントPCのグループ分け

WSUSでは、クライアントPCを「コンピュータ・グループ」という任意の管理グループに分類して、グループ毎に更新プログラムの承認を行う事が可能である。コンピュータ・グループの登録とグループ分けは、管理画面で管理者が手動で行うか、グループポリシーまたはレジストリによってクライアントPCに対して設定することで行う。

コンピュータ・グループによって、きめ細かな更新プログラムの適用管理が可能になる。例えば、更新プログラムをまず適用試験用のPCに適用して評価を行い、安全を確認した後に一般のクライアントPCに対して配布する、といった適用制御が容易に可能になる。

### レポート

クライアントPCから報告されるステータス情報やWSUSサーバ自身のステータス情報を元に、WSUS 3.0 (SP1) では、次の7種類のレポートを作成できる。レポート作成機能は、外部コンポーネントである「Microsoft Report Viewer 2005」（またはSP1）を使用しており、作成したレポートは[Microsoft Excelのブック型式や](https://ja.wikipedia.org/wiki/Excel "wikilink")[Portable Document Format型式のファイルに出力可能である](https://ja.wikipedia.org/wiki/PDF "wikilink")。

  - 更新レポート
    更新プログラム毎に、クライアントPCの適用状況を表示する。
      - 更新の状態の概要
      - 更新の詳細な状態
      - 更新の状態（表形式）
  - コンピュータレポート
    クライアントPC毎に、更新プログラムの適用状況を表示する。
      - コンピュータの状態の概要
      - コンピュータの詳細な状態
      - コンピュータの状態（表形式）
  - 同期レポート
    WSUS 3.0サーバの、過去のMicrosoft Updateとの同期結果についてレポートを表示する。

### 配布可能な製品と更新プログラムのクラス

WSUSでは、制御する更新プログラムの対象製品と種類（クラス）、言語を任意に選択できる。選択されなかった製品または種類、言語の更新プログラムは、メタデータも含めてMicrosoft Updateサーバからダウンロードされる事はない。

#### 製品

以下の製品に対する更新プログラムを配布する事ができる（2008年7月末日現在）。ただし、WSUS 2.0 (SP1) では、WSUSサーバのインストール直後はWindowsの一部製品しか選択できないので、インストール後にMicrosoft Updateサーバと同期を取ってWSUSを更新する必要がある。WSUS 3.0 (SP1) においては、インストール後に自動起動する「WSUSサーバ設定ウィザード」での操作によって最新の製品とクラスの一覧をダウンロードする。

  - Computer Cluster Pack
  - Exchange (2000以降)
  - Expression
  - Forefront
  - Internet Security and Accelaration Server (2004以降)
  - Microsoft Codename Max
  - Microsoft Core XML Services
  - Microsoft System Center Data Protection Manager (2006以降)
  - Network Monitor
  - Office Communication Server (2007以降)
  - Office (2002以降)
  - SDK Components
  - Silverlight
  - SQL Server (2000以降)
  - System Center Virtual Machine Manager (2007以降)
  - System Management Server (2003以降)
  - Virtual Server (Virtual PC 2004以降、Virtual Server 2005以降)
  - Visual Studio (2005以降)
  - Windows Live
  - Windows Small Business Server (2003以降)
  - Windows (2000以降)
  - Zune

#### クラス

以下の種類の更新プログラムを配布する事ができる（2008年7月末日現在）。

  - Feature Packs : 新しく公開された機能。通常は時期リリース製品に含まれる。
  - Service Packs
  - セキュリティ問題の修正プログラム : 製品のセキュリティホールを修正する更新プログラム。
  - ツール : ユーティリティ類
  - ドライバ : デバイスドライバ
  - 更新 : 重要性が低く、セキュリティに関連しない不具合を修正するための更新プログラム。
  - 修正プログラム集 : 複数の[ホットフィックス](https://ja.wikipedia.org/wiki/ホットフィックス "wikilink")やセキュリティ修正プログラムなどを集約した更新プログラム。
  - 重要な更新 : 重要性が高く、セキュリティに関連しない不具合を修正するための更新プログラム。
  - 定義自動更新プログラム : [Windows DefenderやForefront](https://ja.wikipedia.org/wiki/Windows_Defender "wikilink") Client Securityなどの定義ファイル。

## インストール要件

### サーバ

基本的にそれほどハイスペックなハードウェアは要求されないが、WSUSサーバの[トポロジ](https://ja.wikipedia.org/wiki/トポロジ "wikilink")によっては、かなりのポテンシャルを要求される。[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")容量は旧版のSUSと比べるとより多くの空き容量が必要となっている。

Microsoft社が提示する、WSUS 3.0 (SP2) サーバの要件は以下の通り\[3\]。

  - ソフトウェア
      - Windows Server 2003 Service Pack 1 (SP1) 以上の各エディション、あるいはWindows Server 2008の各エディション（いずれも32ビット版と64ビット版の両方をサポート）
      - [Microsoft IIS](../Page/Internet_Information_Services.md "wikilink") 6.0 以上
      - [Microsoft .NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 2.0
      - Microsoft 管理コンソール 3.0
      - Microsoft Report Viewer 再頒布可能パッケージ 2008
  - ハードウェア
      - システム[パーティション](../Page/パーティション.md "wikilink")に1GB以上の空き領域
      - WSUSのコンテンツ保存用に20GB以上の空き領域（推奨30GB）
      - WMSDEインストール先ボリュームに2GB以上の空き領域

### クライアント

WSUS用のクライアントは、以下のOS\[4\]で自動更新機能が有効になっており、かつネットワークに接続されている必要がある。自動更新クライアントはWSUSサーバに接続することで自動的に自分自身を更新するため、ユーザが特別な作業を行う必要はない。

  - Microsoft Windows 2000 Service Pack 4 (SP4) の各エディション
  - Microsoft Windows XP Professional
  - Microsoft Windows Server 2003 Service Pack 2 (SP2) 以降の各エディション
  - Microsoft Windows Vistaの各エディション
  - Microsoft Windows Server 2008 Service Pack 1 (SP1) 以降の各エディション
  - Microsoft Windows 7の各エディション

### 管理コンソール

WSUSではWSUSサーバと管理コンソールが分離されており、クライアントPCに管理コンソールのみをインストールしてリモート管理が可能である。管理コンソール実行用のクライアントの要件は以下の通り\[5\]。

  - Microsoft Windows XP Service Pack 2 (SP2) 以降の各エディション
  - Microsoft Windows Server 2003 Service Pack 2 (SP2) 以降の各エディション
  - Microsoft Windows Vistaの各エディション
  - Microsoft Windows Server 2008の各エディション

## 使用環境

一般的に、企業などインターネットに接続する回線に対して複数のPCが接続されている環境で利用される。特に、以下のような環境のネットワークでは有効に機能する。

  - インターネット接続回線の帯域に対して、PCの台数が多い
  - 組織内のルールや独自アプリケーションなどの存在のため、PCに対して無条件にMicrosoftが提供する更新プログラムをインストールすることが出来ない
  - 更新プログラムの適用状況を監査する必要がある

一般的なコンシューマユーザのような、PCから直接インターネットに接続する環境ではあまり利用価値がないが、家庭内でもLANを組んで複数のPCが存在するような場合、インターネット接続回線の帯域節約などを目的として導入することには価値がある。ただし、Windows Serverおよび適切な数量の[CALが必要であること](https://ja.wikipedia.org/wiki/クライアントアクセスライセンス "wikilink")、クライアントPCがWSUSサーバを参照するために、グループポリシー（[Active Directoryのグループポリシーまたはローカルグループポリシー](https://ja.wikipedia.org/wiki/Active_Directory "wikilink")）またはレジストリの編集を行う必要があることから、家庭内ではハードルが高い。

## 関連項目

  - [Internet Information Services](../Page/Internet_Information_Services.md "wikilink")

## 脚注

<references/>

## 外部リンク

  - [Windows Server Update Services ホーム](http://technet.microsoft.com/ja-jp/wsus/bb466189.aspx)(マイクロソフト)
  - [WSUS TechNet フォーラム](http://social.technet.microsoft.com/Forums/ja-JP/wsusja/threads)
  - [WSUS.DE](http://www.wsus.de) Microsoft CLIP Community

[Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:Microsoft_server_technology](https://ja.wikipedia.org/wiki/Category:Microsoft_server_technology "wikilink")

1.  <https://social.technet.microsoft.com/Forums/windowsserver/en-US/8a00d47c-f473-4295-9108-1677eeb59648/>
2.
3.
4.
5.