> この記事は[Windows Genuine Advantage](https://ja.wikipedia.org/wiki/Windows_Genuine_Advantage)から翻訳されています。


**Windows Genuine Advantage** （ウィンドウズ・ジェニュイン・アドバンテージ、略称**WGA**、**正規 Windows 推奨プログラム**とも）は一部の[Microsoft Windowsに関するサービス](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")（例えば [Microsoft Update](https://ja.wikipedia.org/wiki/Microsoft_Update "wikilink")）を利用する場合や、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が提供する一部のソフトウェアを[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")および[インストール](../Page/インストール.md "wikilink")するときに、そのWindowsが正規のコピーであることを確認するマイクロソフトの海賊版防止プログラムの一環である。

当初はWGAでの確認は任意であったが、[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[7月](https://ja.wikipedia.org/wiki/7月 "wikilink")から確認を義務付けられるようになった\[1\]。

## 特徴

WGAの確認プロセスは、関係するハードウェアに対して、Windowsとそのライセンスを確認するものである。

  - ダウンロード センターやMicrosoft Update (Windows Update) などでWindowsが正規品であることをチェックする[ActiveX](../Page/ActiveX.md "wikilink")コントロールをダウンロードすることによってWindowsが正規のコピーであることを確認することを要求される。Windowsが正規品であることの確認に成功すると、今後の確認のために特別なファイルをコンピューターに格納する。
  - 1度確認が成功すれば、以後、更新のダウンロードはそのまま行える。通常、ActiveXコントロールをダウンロードし直す必要はない。

Windowsが有効なライセンスを持つようでない場合は、WGAは特定の情報をユーザーに通知して、重要でない更新がマイクロソフトからダウンロードされるのを防ぐ。

  - [Windows Vista上で](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、WGAの確認が失敗すると、より大きな影響がある。正規品でない旨通知され続け、重要でない更新がダウンロードできなくなることに加えて、[Windows Aero](https://ja.wikipedia.org/wiki/Windows_Aero "wikilink")、[Windows Defenderと](https://ja.wikipedia.org/wiki/Windows_Defender "wikilink")[Windows ReadyBoostが使用できなくなる](https://ja.wikipedia.org/wiki/Windows_ReadyBoost "wikilink")。また、30日の猶予期間が与えられ、再認証を行わない場合は、「機能縮小モード」へ移行する。機能縮小モードでは、スタート メニューやデスクトップ アイコンが表示されず、デスクトップの背景は黒に変わる。[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")は使用できるが、インターネットへの接続はブロックされる。ログオンから1時間経つと、ユーザーは警告なくログオフされる。ただし、システムがシャットダウンするわけではなく、ユーザーは再度ログオンできる。機能縮小モードでも、コンピューターに保存された個人データにはアクセスできるようになっている。

## ソフトウェア

### WGA Validation Tool

ユーザーがWGAで確認を行うとき、「Windows Genuine Advantage」という名称の[Internet Explorerのアドオンがインストールされる](../Page/Internet_Explorer.md "wikilink")。以前はこのアドオンを「アドオンの管理」機能で無効にできた。WGAは、ライセンスが有効かどうか確認するために「確認コード」を生み出す「確認ツール」(GenuineCheck.exe) かActiveXコントロールを使う。どちらの方法にしろインターネット接続が必要になる。ユーザーが使用しているWindowsのコピーが正規品でないとWGAによって判定された場合でも、表面上正規品に見えるメディアからインストールされたものであれば（すなわちWindowsの正規品と見分けがつかない[CDと](../Page/コンパクトディスク.md "wikilink")[ホログラムをもった海賊版を](https://ja.wikipedia.org/wiki/ホログラフィー "wikilink")、海賊版と知らずにインストールした場合）、マイクロソフトはユーザーに正規品のCDを提供している。マイクロソフトは、Windowsの合法的な正規のコピーを購入したいが、有効なCDを持っていない者に、割引を提供している。正規品と確認されなくても重要なセキュリティー更新プログラムはダウンロードできるようになっている。

### WGA Notifications

[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[4月25日](../Page/4月25日.md "wikilink")から、マイクロソフトはユーザーへ「重要な更新」KB905474として「Windows Genuine Advantage Notifications」を提供し始めた\[2\]。海賊版を使用しているユーザーは起動時およびWindowsを使用している間、通知を受け続けるようになっているものである。もちろん、合法的なコピーをもつユーザーは、通知は受けない。2006年[5月23日](../Page/5月23日.md "wikilink")に、このプログラムを回避するいくつかの手口に対応するよう、マイクロソフトはプログラムをアップデートした。このプログラムは全言語で同時に更新されるわけではないため、一部の言語で提供されている実際のバージョンは最新のリリースではない可能性がある。[Windows XPの自動更新で](../Page/Microsoft_Windows_XP.md "wikilink")[2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink")[2月20日](../Page/2月20日.md "wikilink")から日本語をはじめとする22言語で開始した\[3\]。 なお[Windows VistaはWindows](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") Genuine Advantage Notificationsの仕組みが実装されているため、Windows Genuine Advantage Notificationsの対象になっていない。

### WGA Validation Library

マイクロソフトは、Windowsが正規のコピーであることを確認するために、「Windows Genuine Advantage Validation Library」をWindows Defender、Windows Internet Explorer 7、Windows Media Player 11のようないくつかの製品に同梱させている。

## WGAの回避

2005年[11月16日](https://ja.wikipedia.org/wiki/11月16日 "wikilink")に、マイクロソフトは[Mozilla Firefoxと他の](../Page/Mozilla_Firefox.md "wikilink")[Gecko](../Page/Gecko.md "wikilink")ベースの[ブラウザーからWGAでの確認を行うために](../Page/ウェブブラウザ.md "wikilink")、プラグインを公表した。しかし[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")のような他のNPAPIサポートのブラウザーでは未だ使えないため、批判を免れなかった。もう一つの回避方法は、「確認ツール」によって発生する有効な「確認コード」を用いてWGAを通すために、2005年[12月25日](../Page/12月25日.md "wikilink")に公表された。問題点としては、Windowsの正規のコピーを使っている一般のコンピューターから「確認ツール」を実行し、「確認コード」を記録し、海賊版のWindowsを使っている環境からその「確認コード」を入力することにより、WGAを行わずにダウンロードできることが挙げられる。2006年7月現在、マイクロソフトはこの手口を防ぐ方法を考案していない。WGAでの確認を通させたり、WGAを使わずにMicrosoft Updateなどを行うための回避方法は、様々な方法がインターネット上で示された。

## WGA Notificationsとファイアーウオール

たとえWindowsの基本的なプロセスでも、一部の[ファイアーウオールは](../Page/ファイアウォール.md "wikilink")、「wgatray.exe」のインターネットへのアクセスに警告を発するかもしれない。

## 収集される情報

WGAでは、次のような情報を収集される\[4\]。

  - [コンピュータ](../Page/コンピュータ.md "wikilink")の製造元とモデル
  - 使用している[オペレーティング システムと](../Page/オペレーティングシステム.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")の[バージョン](https://ja.wikipedia.org/wiki/バージョン "wikilink")情報
  - 地域と言語の設定
  - Windows Genuine Advantageによってコンピュータに割り当てられる一意の番号（[グローバル一意識別子](https://ja.wikipedia.org/wiki/GUID "wikilink")）
  - プロダクト IDとプロダクト キー
  - [BIOS](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink") 名、リビジョン番号、およびリビジョンの日付
  - ボリューム [シリアル番号](https://ja.wikipedia.org/wiki/シリアル番号 "wikilink")

## 批判

### 時限爆弾

たとえWGAがWindowsを完全に使えなくしないとしても、製品が正規品と判定されなかったならば、重要なもの以外の更新がマイクロソフトからダウンロードできなくなくなるという事実は、一部の者がWGAを「時限爆弾」と揶揄する原因となった。

### スパイウェア疑惑

Windows Genuine Advantage Notificationsは[スパイウェア](https://ja.wikipedia.org/wiki/スパイウェア "wikilink")のような振る舞いで批判された。マイクロソフトは振る舞い自体の存在は認めたが、それがスパイウェアに達することは否定した\[5\]。この後、マイクロソフトは毎日ではなく、Windows Genuine Advantage Notificationsが2週間おきに送信するだけに変更したという発表をした。マイクロソフトは、Windows Genuine Advantage Notificationsを削除する方法も示した。

### 擬陽性

WGAは、擬陽性（誤って、Windowsの正規のコピーを「正規でない」ものと判定している）を生むことがある。これには、それぞれ多くの理由がある。マイクロソフトは、問題に遭遇しているユーザーを助けるために、フォーラムを設立した。

### 擬陰性

他方で、Windows をインストールしていなくても [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") で動作させている [ies4Linux](http://www.tatanka.com.br/) と [Wine](https://ja.wikipedia.org/wiki/Wine "wikilink") で Internet Explorer を使えば、「正規マイクロソフト製品」ユーザであると認証され、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の公式サイトから特定のソフトウェアがダウンロードできることが2007年[6月18日](../Page/6月18日.md "wikilink")に明るみに出た\[6\]。

### トラブル

2007年[8月25日](../Page/8月25日.md "wikilink")、マイクロソフトのWGAサーバに問題が発生した。そして、Windows XPとWindows Vistaの正規品を「正規でない」と誤った結果を示した\[7\]。この問題は、およそ12時間後に解決された。マイクロソフトによると、「12,000足らずのシステムが、世界中で影響を受けた」とのことである。 類似した問題は2006年[10月5日](../Page/10月5日.md "wikilink")にも起こったが、それは広範囲にわたるものではなかったようである。

## Windows Activation Technologies

マイクロソフトは[2009年](../Page/2009年.md "wikilink")にWindows Genuine Advantageを「Windows Activation Technologies」（WAT）に改称すると発表した\[8\]（単数形で「～Technology」と表記されることもある）。Windows Vista以降にはこの名称で海賊版対策が提供され、Windows XP以前ではWGAの名称が引き続き使用される。

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")2月には[Windows 7用のWATのアップデート](https://ja.wikipedia.org/wiki/Microsoft_Windows_7 "wikilink")(KB971033)がリリースされ、3月からはWindows Update・Microsoft Updateでの自動配信が開始された。それまでに発見された70以上のアクティベーション回避プログラムを検出・除去する。

## 脚注

## 外部リンク

  - [正規の Microsoft ソフトウェア](http://www.microsoft.com/genuine/)
  - [Windows Genuine Advantage (正規 Windows 推奨プログラム) について](http://support.microsoft.com/kb/892130/ja)
  - [Windows XP で Windows Genuine Advantage (正規 Windows 推奨プログラム) 通知アプリケーションのパイロット版を無効にする方法またはアンインストールする方法](http://support.microsoft.com/kb/921914/ja)

[Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:著作権管理技術](https://ja.wikipedia.org/wiki/Category:著作権管理技術 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.  [MS、海賊版防止策を「Windows Activation Technologies」に改名](http://internet.watch.impress.co.jp/cda/news/2009/05/08/23357.html)、[インプレス](https://ja.wikipedia.org/wiki/インプレス "wikilink") INTERNET Watch、[2009年](../Page/2009年.md "wikilink")[5月8日](../Page/5月8日.md "wikilink")