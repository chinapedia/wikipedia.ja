> この記事は[MS-DOS Shell](https://ja.wikipedia.org/wiki/MS-DOS_Shell)から翻訳されています。


**DOSシェル**(どすシェル、)は、[MS-DOS](../Page/MS-DOS.md "wikilink")および[IBM DOS (PC DOS)のバージョン](https://ja.wikipedia.org/wiki/IBM_PC_DOS "wikilink")4から標準搭載された[ファイルマネージャ](https://ja.wikipedia.org/wiki/ファイルマネージャ "wikilink")。名称はIBM DOS版では「DOSシェル」、MS-DOS版では「**MS-DOSシェル**」（）。

## 概要

DOSシェルは[1988年](../Page/1988年.md "wikilink")のDOS 4.0より、以下のDOSに標準搭載された。

  - DOSシェル - IBM DOS 4.0 ～ PC DOS 2000
  - MS-DOSシェル - MS-DOS 4.0 ～ MS-DOS 6.22

DOS 4.0は[IBM](../Page/IBM.md "wikilink")主導で開発され、[マイクロソフト](../Page/マイクロソフト.md "wikilink")経由で各社に[OEM](../Page/OEM.md "wikilink")供給された。DOS 5.0迄はIBMとマイクロソフトは[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の共同開発契約が存在した。

DOSシェルはキャラクタモードおよびグラフィックモードの画面表示を持ち、プログラムの起動や簡単なファイル操作が行える。両モードともキーボードでもマウスでも操作できる。DOSシェルはDOSに簡単な[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")を提供した。

DOSシェルの画面は、デフォルトでは上部にファイル操作の画面があり、下部にプログラム起動用の「メイン」画面がある。ファイル操作画面では、ドライブの選択、ファイルのオープン（実行）・コピー・削除などの[ディスク操作を行うことができる](../Page/ディスクメディア.md "wikilink")。「メイン」画面は、予め登録したプログラムを、画面上の操作（カーソルキーとエンターキー、またはマウス）で起動できる。プログラムランチャーであり、タスクスイッチャである。DOSシェルから呼び出されたプログラム類は[チャイルドプロセス](https://ja.wikipedia.org/wiki/チャイルドプロセス "wikilink")として動作し、[シングルタスク](https://ja.wikipedia.org/wiki/シングルタスク "wikilink")である。

32ビット [CPU](../Page/CPU.md "wikilink")での稼働中は、[仮想86モード](../Page/仮想86モード.md "wikilink")によって、複数のアプリケーションを起動させたままAlt + Tab（[PC-9800](../Page/PC-9800シリーズ.md "wikilink")/[9821シリーズの場合Graph](../Page/PC-9821シリーズ.md "wikilink") + Tab）キーによって切り替えることもできた。この場合は、特定のアプリケーションがアクティブな間、他のアプリケーションは動作を停止してしまう疑似[マルチタスク](../Page/マルチタスク.md "wikilink")である。

DOSシェルの画面・機能・操作性は、[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")の[Microsoft Windows 2.0](../Page/Microsoft_Windows_2.0.md "wikilink")、および[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")の[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")バージョン1.1のプレゼンテーションマネージャ(PM)と酷似しているが、理由は、この3製品は[IBM](../Page/IBM.md "wikilink") [SAAのCUA](../Page/Systems_Application_Architecture.md "wikilink")'87 準拠のためである。

## 影響

IBM DOS (PC DOS) では、DOSシェルはバージョン4.0以降の全バージョン（日本での[DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")を含む）に搭載され、DOSインストール後は標準のシェルとして起動される。これはDOS全体の最終版である[PC DOS 2000まで続いた](https://ja.wikipedia.org/wiki/MS-DOS#PC_DOS_2000（IBM版） "wikilink")。

[Config.sys](https://ja.wikipedia.org/wiki/Config.sys "wikilink")から**Shell=DOSSHELL.EXE**との記述を削除（コメントアウト）すれば、従来の[COMMAND.COM](../Page/COMMAND.COM.md "wikilink")を標準の[シェル](../Page/シェル.md "wikilink")とする事もできる。またIBM自身も含めた各PCメーカーが、差別化のため独自のシェルが標準起動する事も多かった。

しかし、MS-DOS、特に日本では、DOSシェルは以下の理由により普及せず、標準のシェルとされる事はほとんど無かった。

  - [コンベンショナルメモリ](https://ja.wikipedia.org/wiki/コンベンショナルメモリ "wikilink")を圧迫しフリーエリアがわずかしか得られない（日本では、[日本語入力システム](../Page/日本語入力システム.md "wikilink")が必要なため、起動しないアプリケーションが多かった）
  - バージョン4はIBM主導で開発された影響もあり、国産PCメーカーの大半はバージョン3を使い続けた
  - 日本ではMS-DOS環境で[ファンクションキー](../Page/ファンクションキー.md "wikilink")を多用するアプリケーションやツールが多く、本格的なグラフィック環境は1990年の[Microsoft Windows 3.0まで主流とならなかった](https://ja.wikipedia.org/wiki/Microsoft_Windows_3.0 "wikilink")

[1993年](../Page/1993年.md "wikilink")のMS-DOSバージョン6では、DOSシェルは標準ディスクセットから除外された。（IBMとマイクロソフトのOS共同開発契約はバージョン5までである。）ただし日本では、[日本電気](../Page/日本電気.md "wikilink")が販売した[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")用と[セイコーエプソン](../Page/セイコーエプソン.md "wikilink")が発売した[EPSON PC用MS](https://ja.wikipedia.org/wiki/EPSON_PC "wikilink")-DOSバージョン6.2では標準ディスクセットに付属していた。

## 関連項目

  - [MS-DOS](../Page/MS-DOS.md "wikilink")
  - [Systems Application Architecture](../Page/Systems_Application_Architecture.md "wikilink")
  - [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")

## 外部リンク

  - (下から２画面目に、インストール直後のDOSシェルの画面がある）

[Category:MS-DOS・Windows3.x・9x系](https://ja.wikipedia.org/wiki/Category:MS-DOS・Windows3.x・9x系 "wikilink") [Category:コンピュータのユーザインタフェース](https://ja.wikipedia.org/wiki/Category:コンピュータのユーザインタフェース "wikilink") [Category:ファイルマネージャ](https://ja.wikipedia.org/wiki/Category:ファイルマネージャ "wikilink")