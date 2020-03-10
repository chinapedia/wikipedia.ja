> この記事は[Windows](https://ja.wikipedia.org/wiki/Windows)から翻訳されています。


**Windowsサービス** (`WINDOWS SERVICE`) とは、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) で長時間動作し、ユーザーとのやりとり無しで特定機能を実行するものである。WindowsサービスはOSの[ブート](https://ja.wikipedia.org/wiki/ブート "wikilink")時に起動するよう設定でき、Windows が動作中はずっとバックグラウンドで動作する。あるいは、手動で要求したときに動作するようにも設定できる。[UNIX](../Page/UNIX.md "wikilink")の[デーモンに概念的には似ている](https://ja.wikipedia.org/wiki/デーモン_\(ソフトウェア\) "wikilink")。[Windowsタスクマネージャ](https://ja.wikipedia.org/wiki/Windowsタスクマネージャ "wikilink")のプロセス一覧で、ユーザー名が`SYSTEM`、`LOCAL SERVICE`、`NETWORK SERVICE`などと表示されている場合が多いが、任意のユーザーを指定することもできる。また、`SYSTEM`というユーザー名のプロセスが全てWindowsサービスというわけでもない。

## サービスの管理

Windowsサービスをインストールすると、そのサービスとしての起動の設定は、[コントロールパネル](https://ja.wikipedia.org/wiki/コントロールパネル_\(Windows\) "wikilink") ⇒ 管理ツール ⇒ サービスと選択していき（あるいはマイコンピュータを右クリックして管理を選択後左メニューの中にサービスがある）、そのウィンドウで行う。そのウィンドウではWindowsサービスの一覧が表示され、サービス名、説明、動作状態、スタートアップの種類などが表示されている。この画面か、右クリックで個々のサービスのプロパティを表示することで、以下のことが可能である。

  - サービスの起動・停止・一時停止・再起動
  - サービスのパラメータ指定
  - スタートアップの種類の設定。「自動」、「手動」、「無効」がある。
      - 「自動」: システム起動時にサービスを起動する。
      - 「手動」: ユーザーが要求したときに起動するか、アプリケーションから呼び出されたときに起動する（サービスの種類によって可能な場合がある）。
      - 「無効」: 完全に起動できないようにする。
      - 「自動（遅延開始）」: Windows Vista で新たに導入されたスタートアップ。ブート後、少し間をおいて起動することで、負荷集中によるブート遅延を防ぐ。
  - ログオン時のアカウントの変更
  - エラー発生時の回復の設定
  - サービス一覧を[CSVファイルまたはテキストファイルとしてエクスポートする](../Page/Comma-Separated_Values.md "wikilink")。

[Windows XP以降では](../Page/Microsoft_Windows_XP.md "wikilink")、上記以外に[MSConfig](https://ja.wikipedia.org/wiki/MSConfig "wikilink")（システム構成ユーティリティ）でも設定が可能である。ただし、MSConfigによる設定は次回立ち上げ時に有効となる。[Windows Vista以降では](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、Windowsタスクマネージャのサービスタブでもサービスの起動・停止が可能である。

## Windowsサービスの開発

Windows 側の[インタフェースは](../Page/インタフェース_\(情報技術\).md "wikilink")[サービスコントロールマネージャ](https://ja.wikipedia.org/wiki/サービスコントロールマネージャ "wikilink")と呼ばれ、サービスの起動/停止を管理する。そして、いくつかの[API呼び出しでサービス名や属性がサービスコントロールマネージャ内に登録される](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。一般にWindowsサービスには[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")は存在しないが、ユーザインタフェースを持たせることは可能で、それを使う場合そのサービスのプロパティの「ログオン」タブ画面で「デスクトップとの対話をサービスに許可」をチェックしなければならない。

## 関連項目

  - [デーモン (ソフトウェア)](https://ja.wikipedia.org/wiki/デーモン_\(ソフトウェア\) "wikilink")

## 外部リンク

  - [Microsoft Developer Network - Services](http://msdn2.microsoft.com/en-us/library/ms685141.aspx)
  - [Black Viper](http://www.blackviper.com) - custom services configuration website

[Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:サービス](https://ja.wikipedia.org/wiki/Category:サービス "wikilink")