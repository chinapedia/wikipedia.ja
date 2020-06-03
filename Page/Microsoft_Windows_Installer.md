> この記事は[Microsoft Windows Installer](https://ja.wikipedia.org/wiki/Microsoft_Windows_Installer)から翻訳されています。


[Windows Me](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink"){{-}}[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink"){{-}}[Windows Server 2003](../Page/Microsoft_Windows_Server_2003.md "wikilink"){{-}}[Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink"){{-}}[Windows Server 2008](../Page/Microsoft_Windows_Server_2008.md "wikilink"){{-}}[Windows 7](../Page/Microsoft_Windows_7.md "wikilink"){{-}}[Windows Server 2008 R2](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2008#Windows_Server_2008_R2 "wikilink") | also_available_for = [Windows 95](../Page/Microsoft_Windows_95.md "wikilink"){{-}}[Windows 98](../Page/Microsoft_Windows_98.md "wikilink"){{-}}[Windows NT 4.0](../Page/Microsoft_Windows_NT.md "wikilink") | related_components = }}

**Windows Installer**は、[Windowsで](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")の[インストール](../Page/インストール.md "wikilink")・メンテナンス・削除を行うエンジンである。[コードネーム](../Page/コードネーム.md "wikilink")は**Darwin**。以前は**Microsoft Installer**と呼ばれていた。**インストールパッケージ** (installation package) には、インストール処理に関する情報とインストールされるファイルとがパッケージングされている。インストールパッケージのデフォルトのファイル[拡張子](../Page/拡張子.md "wikilink")が"MSI"であることから**MSIファイル**とも呼ばれる。インストールパッケージは内部的には数十個のリレーショナルデータベースのテーブルからなる[OLE構造化ストレージファイル](https://ja.wikipedia.org/wiki/OLE構造化ストレージファイル "wikilink")である\[1\]。Windows Installerには以前の[Setup APIと比較して多くの改善点が見られる](https://ja.wikipedia.org/wiki/Setup_API "wikilink")。例えば、[GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[フレームワーク](https://ja.wikipedia.org/wiki/フレームワーク "wikilink")、アンインストールシーケンスの自動生成、デプロイメント機能の強化、Windows Installerを他の実行可能形式のインストーラフレームワーク（[InstallShield](../Page/InstallShield.md "wikilink")、[WISE](https://ja.wikipedia.org/wiki/Wise_Solutions,_Inc. "wikilink")（後のバージョンは Windows Installerベースになっている）、[NSISなど](https://ja.wikipedia.org/wiki/Nullsoft_Scriptable_Install_System "wikilink")）と置き換えられるようにしたこと、等が挙げられる。

[マイクロソフト](../Page/マイクロソフト.md "wikilink")は[サードパーティー](../Page/サードパーティー.md "wikilink")に対しWindows Installerをインストーラフレームワークのベースとすることを推奨している。これは、インストーラの動作をWindows Installerに合わせることで、インストールされた製品のデータベースの一貫性を保つためである。Windows Installerの機能であるロールバックやバージョン管理が正しく行われるためには、内部データベースの一貫性が保たれている必要がある。

## パッケージの論理構造

パッケージが持つことのできる最も大きな単位が**プロダクト** (product) である。パッケージは複数のプロダクトのインストール情報を格納できる。プロダクトは全世界で一意な識別子である[GUID](../Page/GUID.md "wikilink")（PackageCodeプロパティ）で識別される。また、Windows Installerはプロダクト間の依存性については関与しない。プロダクトは複数の「コンポーネント」からなり、また複数のコンポーネントを「機能」という単位でまとめることができる。

### プロダクト (product)

単独で動作する一つのプログラム（または、プログラムの集合）をプロダクトと呼ぶ。たとえば、Microsoft Officeなどの単一プロダクトがWindows Installerのプロダクトとなる。\[2\]プロダクトも全世界で一意な識別子である[GUID](../Page/GUID.md "wikilink")（ProductCodeプロパティ）で識別される。プロダクトとパッケージとは別の単位で、一つのMSIパッケージで複数のプロダクトをインストールすることが可能である。たとえば、あるプログラムのフランス語版と英語版とを一つのMSIでインストールできるようにする場合、各言語版のプログラムは別々のプロダクトとなる。

### コンポーネント (component)

**コンポーネント** (component) はプロダクトを構成する最小単位である。Windows Installerはコンポーネント単位でインストール・アンインストール処理を行う（すなわち、あるコンポーネントの一部をインストールするような設定は行えない）。コンポーネントは[ファイル](../Page/ファイル_\(コンピュータ\).md "wikilink")、[ディレクトリ](../Page/ディレクトリ.md "wikilink")、[COMコンポーネント](../Page/Component_Object_Model.md "wikilink")、[レジストリ](../Page/レジストリ.md "wikilink")キー、ショートカット、およびその他のデータを含むことができる。インストーラを起動したユーザーが直接コンポーネントを操作することはできない。

コンポーネントも、全世界で一意な識別子である[GUID](../Page/GUID.md "wikilink")で識別される。これは、一つのコンポーネントを、一つのパッケージ内の複数の機能から、もしくは、複数のパッケージから共有できることを意味する。このような共有コンポーネントのことを[マージモジュール](https://ja.wikipedia.org/wiki/マージモジュール "wikilink")と呼ぶ（この仕組みが正しく動作するためには、各コンポーネント間に重複した内容があってはならない）。

### キーパス (key path)

**キーパス** (key path) はパッケージの製作者がそのパッケージに必須であると指定したファイル等のことである。キーパスにはファイル、レジストリキー、[ODBCデータソースが指定できる](../Page/Open_Database_Connectivity.md "wikilink")。キーパスにはファイルを指定するのが一般的であるため、*キーファイル*とも呼ばれる。コンポーネントが持つことのできるキーパスは1つだけで、コンポーネントのキーパスを明示しなかった場合は、コンポーネントのインストール先のディレクトリがキーパスとなる。MSIベースのアプリケーションが起動されると、Windows Installerはキーパスに指定されたファイルやレジストリキーが存在するかチェックする。チェックの結果とMSIパッケージの情報との間に不整合があった場合（例えばキーファイルが削除されていた場合）、関連する機能の再インストールが行われる。このプロセスは*自動修復機能*と呼ばれる。複数のコンポーネントが同じキーパスを持つことはできない。

### 機能 (feature)

**機能** (feature) はコンポーネントを階層的にまとめた構造である。一つの機能は複数のコンポーネントからなる。また、機能の中に機能を入れ子にすることもでき、他の機能に含まれる機能を*サブ機能*(subfeature)と呼ぶ。ほとんどソフトウェアでは、パッケージは単一の機能からなる。大規模なインストールプログラムでは通常、実行時に*カスタムセットアップ*ダイアログが表示され、ユーザがインストール・アンインストールする機能を選択できるようにしている。

機能の単位はパッケージの作成者が決定する。例えばワープロプログラムであれば、メインの実行プログラム、ヘルプファイル、オプションとしてスペルチェッカー等がそれぞれ一つの機能となる。

## セットアップのフェーズ

### UIシーケンス

UIシーケンスでは、インストール先のシステムの状態を取得し、インストールウィザードを表示し、インストールのオプションをユーザーに選択させる。

ただし、UIシーケンス中では、システムに対する変更は一切行われない。これには以下の3つの理由がある。

1.  MSIパッケージはquietモードで実行できなければならない。quietモードではGUIは全く表示されず、通常UIシーケンスで指定する情報はすべてコマンドラインから指定される。よって、ユーザインタフェース中で行われるすべてのアクションは、quietモードでは実行されない。quietモードでのインストールを行うには、コマンドラインからmsiexec.exeを**/qn**（または**/qb**、**/qr**）オプション付きで実行する。
2.  同様に、[コントロールパネルの](https://ja.wikipedia.org/wiki/コントロールパネル_\(Windows\) "wikilink")[アプリケーションの追加と削除](https://ja.wikipedia.org/wiki/アプリケーションの追加と削除 "wikilink")で*削除*ボタンを押下した場合にはアンインストーラが実行されるが、ここでもインストール時にUIシーケンスで行われたすべてのアクションは実行されない。
3.  システムに変更を加えるアクションをUIシーケンス中で実行した場合、Elevated Privileges機能で昇格した権限ではなく、インストーラを実行したユーザの権限でシステムへの変更処理が実行されてしまう。これについては以降のセクションで述べる。

UIシーケンス中で行われるアクションと表示される[ダイアログボックス](../Page/ダイアログボックス.md "wikilink")はInstallUISequenceテーブル中に定義される。似たようなテーブルとしてAdminUISequenceテーブルがあり、ここでは管理インストールで実行されるアクションと表示されるダイアログボックスが定義される。

### 実行シーケンス

典型的なMSIインストールウィザードでは、*完了*または*インストール*ボタンを押下すると実行シーケンスが実行され、コンポーネントの実際のインストールが行われる。実行フェーズではシステムに変更が加えられる一方、ユーザインタフェースは一切表示されない。

実行フェーズは次の2つのステップに分けて実行される。:

  - *即時実行モード*: このステップでは、Windows Installerは、ユーザもしくはアプリケーションからプロダクトのインストール・アンインストールに必要な命令を受け取る。リクエストが発行されると**アクション** (action) の**シーケンス** (sequence) が実行され、データベース内の情報から、遅延実行モードで行うべき処理を記述したスクリプトが内部的に構築される。

<!-- end list -->

  - *遅延実行モード*: このステップでは、即時実行モードで構築されたスクリプトが実行される。スクリプトはWindows Installerサービスが動作しているアカウント（LocalSystemアカウント）で実行される。これは、セットアップ処理を起動する方法が多岐にわたるためである。たとえば、非特権ユーザーがインストールを行う場合は特権ユーザへの昇格が必要になる（なお、特権ユーザへ昇格してインストールを行うには、パッケージがLocal administratorによってデプロイされているか、システム管理者が[グループポリシー](https://ja.wikipedia.org/wiki/グループポリシー "wikilink")でパッケージをアドバタイズしている必要がある）。

通常のインストールで実行されるアクションのシーケンスはInstallExecuteSequenceテーブルに格納される。同様に、管理インストールで実行されるアクションはAdminExecuteSequenceテーブルに、アドバタイズされたパッケージのインストールで実行されるアクションはAdvtExecuteSequenceテーブルに格納される。

### ロールバック

遅延実行シーケンススクリプトの実行中にエラーが発生した場合や、ユーザーの操作によって処理がキャンセルされた場合、その時点までに行われたアクションはロールバックされ、システムは元の状態に復元される。Windows Installerの標準アクションは実行時に自動的にロールバックスクリプトへの書き込みを行っており、ロールバック処理ではそのスクリプトが実行される。パッケージの作者がシステムに変更を加えるカスタムアクションを作成する場合は、対応するロールバックアクションも作成する必要がある。アンインストール用アクションにも同様にロールバック用のアクションが必要になる。このメカニズムによって、アンインストールが失敗した場合には再インストールが行われるという少し奇妙な処理が行われる。

## その他の機能

### アドバタイズ

Windows Installerでは、製品を**アドバタイズ** (advertise) することもできる。製品がアドバタイズされると、ユーザーからは製品がインストールされたように見えるが、実際のインストールは製品が初めて起動されるとき（スタートメニューからの起動、関連付けられたファイルを開く、アドバタイズにより設定されたCOMクラスを呼び出す等）に実行される。パッケージのアドバタイズを行うには、グループポリシーまたはその他のデプロイメント機構を使用するか、msiexec.exeを**/jm**（すべてのユーザに対してアドバタイズ）または**/ju**（現在のユーザに対してアドバタイズ）オプション付きで実行する。

### オンデマンドでのインストール

アドバタイズと同様に、オンデマンドでのインストールに指定された**機能**はユーザーが使用しようとした時点で初めてインストールされる。

### 管理インストール

管理インストールでは非圧縮の状態の製品のイメージが作成される。この機能は、主にアプリケーションをネットワークドライブからインストールまたは実行する際に用いられる。管理用インストールでは、通常のインストールとは異なり、ショートカットの作成・COMサーバの登録・「プログラムの追加と削除」への追加は行われない。管理用インストールは、展開したインストール用ソースから機能を実行する場合にしばしば使用される。

管理インストールはWindows Installerのパッチを作成する場合にも使用される。これは、バイナリファイルの差分を得るために、古いバージョンと新しいバージョンの展開済みイメージが必要になるためである。管理インストールを行うには、msiexec.exeを**/a**オプション付きで実行する。

### その他

Windows Installerでは、アプリケーションをネットワーク共有から直接実行することができる。ローカルへのコピーは不要であり (**run from source**)、以下の処理が可能である。

  - 壊れたインストールの修復。破壊・削除されたファイルやレジストリエントリをリストアする。
  - コンポーネント識別子からのパスの解決。アプリケーションへのファイルパスの[ハードコーディング](https://ja.wikipedia.org/wiki/ハードコーディング "wikilink")を不要にする。
  - ネイティブでサポートされた**パッチ**（**.mspファイル**）と、**transforms**または**.mstファイル**を使用したパッケージのデータベースの操作によるパッケージのカスタマイズ。

また、ブラックボックス部分が非常に少ない点も、他のWindows用インストーラフレームワークと比較して特筆すべき違いである。すべてのAPIとコマンドラインオプションのドキュメントが提供されている。パッケージの内容は、無償のツールや自作のプログラムから自由に閲覧・編集できる。この点は、プロプライエタリであり、弱い暗号であるとはいえ暗号化されたパッケージを使用するInstallShieldとは対照的である。ファイルアーカイブのフォーマットは[CAB](../Page/CAB.md "wikilink")であり、ドキュメントも豊富に提供されている。

### Windows Vista

[Windows Vistaに同梱されているWindows](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") Installer 4.0には、[UACと連携するための機能が盛り込まれている](../Page/ユーザーアカウント制御.md "wikilink")。MSIパッケージを管理者権限が不要であるとマークすれば、ユーザは管理者資格情報のプロンプトを表示せずにパッケージをインストールできる。Windows Installerと再起動マネージャの連動も可能である。アプリケーションやシステムコンポーネントのインストールおよび更新を「フル」ユーザインタフェースモードで行うときは、影響を受けるアプリケーションのうちシャットダウンできるもののリストが表示され、ファイルが更新された後に再起動することができる。サイレントモードでは、インストーラのアクションによってアプリケーションは自動的に再起動される。システムサービスやトレイアプリケーションも同様に再起動が可能である。

## 診断ログ

Windows Installerは強力な診断用ツールとして詳細なロギング機能をサポートしている。ロギングは次の方法で有効化できる。

  - **コマンドライン**

<!-- end list -->

  -
    MSIパッケージをコマンドラインからインストールする場合、`/L`オプションを指定するとロギングが有効になる。例えば、以下のコマンドはPackage.msiをインストールし、詳細なログを`c:\Package.log`に出力する。
    `msiexec /i Package.msi /l*v c:\Package.log`

<!-- end list -->

  - **Windows レジストリ**

<!-- end list -->

  -
    レジストリに次の値を設定すると詳細なロギングが有効になる。
    `キー: HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\Installer`
    `名前: Logging`
    `種類: REG_SZ`
    `データ: voicewarmup`

ログは`MSI###.log`（"\#\#\#" はランダムに決定される一意な識別子）という名前でユーザーの*Temp*ディレクトリに保存される（'temp' ディレクトリはユーザーごとに別々で、環境変数%temp%で表される）。

  - **グループポリシー**

<!-- end list -->

  -
    以下の[グループポリシー](https://ja.wikipedia.org/wiki/グループポリシー "wikilink")の設定で複数のシステムにおけるロギングを管理することができる。
    `コンピュータの構成 -> 管理テンプレート -> Windowsコンポーネント -> Windows インストーラ -> ロギング`

<!-- end list -->

  - **WindowsインストーラAPI**

<!-- end list -->

  -
    自作のプログラムからMSIパッケージのインストールを行う場合、`MsiEnableLog`関数でログファイルの作成とロギングレベルの設定が行える。設定は呼び出し側のプロセスが生きている間のみ有効である。

<!-- end list -->

  - **MsiLoggingプロパティ**

<!-- end list -->

  -
    Windowsインストーラ4.0ではMsiLoggingプロパティが導入された。これはフラグのリストで、どの情報をログに残すかを表す。フラグはmsiexec.exeの`/L`オプションで指定したり、ロギングポリシーの設定で使用するものと同様である。MsiLoggingを使用すると、MsiLogFileLocationプロパティにログファイルの場所がセットされる。

冗長なログはWindowsインストーラの問題を診断するには便利だが、とても長く、訓練なしに読むのは難しい。ログから問題の個所を簡単に見つけ出すには、テキストエディタ（たとえば [メモ帳](../Page/メモ帳.md "wikilink")）でログファイルを開き、"Return Value 3"という文字列を検索する。この文字列は通常、致命的なエラーが発生した場所の近くで出力される。また、Windows Installer SDKでWiLogUtlというツールが提供されている。これはWindowsインストーラのログファイルをパースし注釈を付けてくれる。

ログファイルにデバッグ情報を出力する場合は、コマンドラインか、またはレジストリの`Logging`の値に*x*を指定する。例えば、以下のコマンドはPackage.msiをインストールし、デバッグ情報を含む詳細なログを`c:\Package.log`に出力する。

  -
    `msiexec /i Package.msi /l*vx c:\Package.log`

## ICE による検証

マイクロソフトは、MSIデータベースの潜在的な問題を検出するInternal Consistency Evaluators (ICE) を提供している。ICEのルールはCUBファイルにまとめられている。これは必要最低限の内容のみを含むMSIファイルで、ターゲットのMSIデータベースを検証し、警告またはエラーを出力するカスタムアクションを含んでいる。ICEによる検証はPlatform SDKのツールであるOrcaとmsival2から行える。また、各種オーサリング環境に付属の検証用ツールからも行える。

ICE のルールは、例えば次のようなものである。

  - ICE09: システムフォルダに格納されるすべてのコンポーネントがPermanentとしてマークされているか検証する。
  - ICE24: 製品コード、製品バージョン、製品の言語のフォーマットが適切か検証する。
  - ICE33: Registryテーブルに、他のテーブル（Class, Extension, Verbなど）に格納すべきデータが含まれていないか検証する。

リリースプロセスにおいて、ICEの警告とエラーを処置することは重要なステップである。

インストール処理では、インストールに先立ってMSIパッケージのコピーがテンポラリフォルダに作成される。これは、パッケージがローカルにある場合でも行われる。インストールパッケージがローカライズされている場合、InstallShield製品はMSIパッケージの追加のコピーをテンポラリフォルダに作成する。

パッケージビルダが「オンデマンドでのインストール」もしくは「修復」機能を使用するよう設定した場合、パッケージ全体（ローカライゼーションメッセージは除く）とスタブのMSIパッケージが`%WinDir%\Installer`ディレクトリにコピーされる。

グループポリシーによって、インストールの全操作をログに取るよう設定できるが、このログは Windows のテンポラリディレクトリに作成される。このログファイルは、大きなパッケージに対して最も冗長なログを取得した場合、数十メガバイトにもなる。ログファイルは診断には便利だが、ユーザがインストーラに関係した操作（インストール、アンインストール、変更、修復、パッチ）を頻繁に行う場合、ログによるスペースの消費は馬鹿にならない。ロギングポリシーはデフォルトでは無効になっているが、顧客によるインストールプログラムのデバッグの補助のために、セットアップのブートストラッププログラムがロギングを有効にしている場合もある。

MSIインストールファイルのサイズは同等の`.zip`や`.rar`（または自己解凍形式の `.exe`）ファイルよりも大きくなる傾向にある。これは、強力な圧縮アルゴリズムを使用していないためである。

## バージョン

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>提供日</p></th>
<th><p>標準提供</p></th>
<th><p>追加提供</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.0</p></td>
<td><p>1999年</p></td>
<td></td>
<td><p><a href="../Page/Microsoft_Windows_95.md" title="wikilink">Windows 95</a>,<br />
<a href="../Page/Microsoft_Windows_98.md" title="wikilink">Windows 98</a>,<br />
<a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_NT_4.0" title="wikilink">Windows NT 4.0</a> (x86, Alpha)</p></td>
</tr>
<tr class="even">
<td><p>1.1</p></td>
<td><p>2000年</p></td>
<td><p><a href="../Page/Microsoft_Windows_2000.md" title="wikilink">Windows 2000</a> RTM, SP1, SP2</p></td>
<td><p>Windows 95,<br />
Windows 98,<br />
Windows NT 4.0 SP6 (x86)</p></td>
</tr>
<tr class="odd">
<td><p>1.2</p></td>
<td><p>2000年</p></td>
<td><p><a href="../Page/Microsoft_Windows_Millennium_Edition.md" title="wikilink">Windows Me</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2.0</p></td>
<td><p>2001年</p></td>
<td><p><a href="../Page/Microsoft_Windows_XP.md" title="wikilink">Windows XP</a> RTM, SP1,<br />
Windows 2000 SP3, SP4,<br />
<a href="../Page/Microsoft_Windows_Server_2003.md" title="wikilink">Windows Server 2003</a> RTM</p></td>
<td><p>Windows 95,<br />
Windows 98,<br />
Windows Me,<br />
Windows NT 4.0 SP6 (x86),<br />
Windows 2000 RTM, SP1, SP2</p></td>
</tr>
<tr class="odd">
<td><p>3.0</p></td>
<td><p>2004年</p></td>
<td><p>Windows XP SP2</p></td>
<td><p>Windows 2000 SP3, SP4<br />
Windows XP RTM, SP1</p></td>
</tr>
<tr class="even">
<td><p>3.1</p></td>
<td><p>2005年</p></td>
<td><p>Windows XP SP3,<br />
Windows Server 2003 SP1, SP2</p></td>
<td><p>Windows 2000 SP3, SP4<br />
Windows XP RTM, SP1, SP2,<br />
Windows Server 2003 RTM</p></td>
</tr>
<tr class="odd">
<td><p>4.0</p></td>
<td><p>2006年</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista" title="wikilink">Windows Vista</a> RTM, SP1,<br />
<a href="../Page/Microsoft_Windows_Server_2008.md" title="wikilink">Windows Server 2008</a> RTM</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>4.5</p></td>
<td><p>2008年</p></td>
<td><p>Windows Vista SP2,<br />
Windows Server 2008 SP2</p></td>
<td><p>Windows XP SP2, SP3,<br />
Windows Server 2003 SP1, SP2<br />
Windows Vista RTM, SP1,<br />
Windows Server 2008 RTM</p></td>
</tr>
<tr class="odd">
<td><p>5.0</p></td>
<td><p>2009年</p></td>
<td><p><a href="../Page/Microsoft_Windows_7.md" title="wikilink">Windows 7</a> RTM,<br />
<a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2008_R2" title="wikilink">Windows Server 2008 R2</a> RTM</p></td>
<td></td>
</tr>
</tbody>
</table>

## 再配布

Windows Installerは再配布が可能である。以下のサイトからダウンロードできる。

  - 3.0 - [Windows Installer 3.0 Redistributable](https://www.microsoft.com/ja-jp/download/details.aspx?id=16821)
  - 3.1 - [Windows Installer 3.1 Redistributable (v2)](https://www.microsoft.com/ja-jp/download/details.aspx?id=25)
  - 4.5 - [Windows Installer 4.5 Redistributable - 日本語](https://www.microsoft.com/ja-jp/download/details.aspx?id=8483)

## 脚注

<references />

## 関連項目

  - [WiX](../Page/WiX.md "wikilink")はマイクロソフトのオープンソースツールで、XMLファイルからMSIファイルをビルドするのに使用される。
  - [Scriptlogic](https://ja.wikipedia.org/wiki/Scriptlogic "wikilink")
  - [Windows SDK](https://ja.wikipedia.org/wiki/Windows_SDK "wikilink")
  - [:Category:システムソフトウェア](https://ja.wikipedia.org/wiki/Category:システムソフトウェア "wikilink")

## 外部リンク

  - [Windows インストーラ テクノロジの概要](http://support.microsoft.com/kb/310598/ja)
  - [Windows Installer 4.0 for Windows Vista and Windows Server 2008](http://msdn2.microsoft.com/en-us/library/aa372808.aspx)
  - MSDNの[Windows Installer Team Blog](http://blogs.msdn.com/windows_installer_team/)
  - [WiX](http://sourceforge.net/projects/wix/)
  - [InstallSite.org](http://www.installsite.org/)

[Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:パッケージ管理システム](https://ja.wikipedia.org/wiki/Category:パッケージ管理システム "wikilink")

1.  インストール・アンインストールの詳細なログを見ると、SQLが発行されていることが分かる。
2.   (**Web Archive**)