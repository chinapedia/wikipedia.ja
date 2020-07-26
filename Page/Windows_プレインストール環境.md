> この記事は[Windows プレインストール環境](https://ja.wikipedia.org/wiki/Windows_プレインストール環境)から翻訳されています。


**Microsoft Windows プレインストール環境** (Windows Preinstallation Environment, **Windows PE**, **WinPE**) は、大手企業などが多数台の[ワークステーション](../Page/ワークステーション.md "wikilink")や[サーバ](../Page/サーバ.md "wikilink")へ[Windowsをインストールするための](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、軽量版Windowsである。またPCメーカーが製造過程で自社製PCに[OEM](../Page/OEM.md "wikilink")版Windowsをプレインストールするためにも利用される。

軽量であるがゆえ[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")のみならず[コンパクトディスク](../Page/コンパクトディスク.md "wikilink")や[USBメモリからも](../Page/USBフラッシュドライブ.md "wikilink")[ブート](../Page/ブート.md "wikilink")でき、[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")からブートできた[MS-DOS](../Page/MS-DOS.md "wikilink")に変わるOSの選択肢の1つとして利用可能である。

## 概要

WinPEは当初、Microsoft Windows[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")をインストールするプラットフォームとしてのみ利用することを意図していた。後のバージョンは下記のような目的のためのプラットフォームに発展した。

  - 大企業でのワークステーションやサーバへのWindowsインストール
  - PCメーカーがエンドユーザーに販売するワークステーションやサーバへのOEM版Windowsプレインストール
  - 大手PCメーカーの修理部門や、その他Windowsリカバリーを行いたい場面で使用される、リカバリープラットフォーム

<!-- end list -->

  -

      -
        システム診断時や回復インストール時にユーザーが使用するユーティリティOSとして、MS-DOS（[NTFSが扱えない](../Page/NT_File_System.md "wikilink")）からの置き換え。
        起動CD/DVDは、開発テスト技術者やシステム管理者のためのリカバリーCD/DVDとしてカスタマイズ可能である。インターネットを利用できるそれらの人々は目的に合わせ異なるサードパーティアプリケーションを含むWinPEの起動CD/DVDを作成することが多い。

<!-- end list -->

  - [サードパーティー](../Page/サードパーティー.md "wikilink")製Windowsユーティリティ（例えば[Symantec Ghost](http://www.symantec.com/ja/jp/enterprise/products/overview.jsp?pcid=1025&pvid=865_1)）のプラットフォーム

## 歴代バージョン

以下のバージョンの存在が知られている。最小必要メモリ容量が次第に大きくなり、バージョン2.0では512MBに近づいた。現行版のバージョンは5.1であり、Windows 8.1の[カーネル](../Page/カーネル.md "wikilink")をベースとしている。

### Windows PE 1.0

[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") Professionalの初期バージョンを元にした構築作業を要する。

### Windows PE 1.1

Windows XP Professional Service Pack 1 (SP1)を元にした構築作業を要する。

### Windows PE 1.2

[Windows Server 2003ファミリーを元にした構築作業を要する](../Page/Microsoft_Windows_Server_2003.md "wikilink")。

### Windows PE 2004 (1.5)

Windows XP Professional Service Pack 2 (SP2)を元にした構築作業を要する。

### Windows PE 2005 (1.6)

Windows Server 2003 Service Pack 1 (SP1)を元にした構築作業を要する。

### Windows PE 2.0

[Windows Vistaを元に構築された](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。

このバージョン以降と以前のバージョンに比して以下の特徴がある。

  - ツールキットのインストーラ自体からファイルが生成されるため、ソースDVD（元となるWindowsのインストールディスク）をもはや要求してこない。代わりに、ダウンロードサイズが以前は60MB程であったが当版から900MBに増加した。
  - [WMI](https://ja.wikipedia.org/wiki/WMI "wikilink")アクセス、[Windows Scripting Host](https://ja.wikipedia.org/wiki/Windows_Scripting_Host "wikilink") (WSH)、追加ドライバ、他の[32ビット](../Page/32ビット.md "wikilink")アプリケーション（または[64ビット](../Page/64ビット.md "wikilink")版のための64ビットのアプリ）といったような、様々なプラグインを含む起動イメージを作成するよう変更可能である。
  - 当版から以降、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の製品であるBDD 2007を利用することにより、起動環境を生成する手順の全体に渡って、（古いシステムのユーザーになじみ深い）コマンドラインツールを排除した。
  - 再書き込み可能なRAMディスクを利用可能（WinPE 1.xバージョンは書き込みできないRAMディスクを利用していた）であり、USBメモリのような追加の周辺機器をホットプラグで利用可能である。

### Windows PE 2.1

[Windows Server 2008を元に構築され](../Page/Microsoft_Windows_Server_2008.md "wikilink")、Windows Vista SP1と同じコードを基盤としている。

### Windows PE 3.0

[Windows Server 2008 R2ないし](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2008_R2 "wikilink")[Windows 7と同じコードを基盤として構築されている](../Page/Microsoft_Windows_7.md "wikilink")。

### Windows PE 3.1

Windows 7 Service Pack 1 (SP1)を元に構築された。

3.0に対する更新としてリリースされておりインストーラーは含まれておらず、手動で上書きして使用する\[1\]。

### Windows PE 4.0

[Windows Server 2012ないし](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2012 "wikilink")[Windows 8と同じコードを基盤として構築されている](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")。

### Windows PE 5.0

[Windows Server 2012 R2ないし](https://ja.wikipedia.org/wiki/Microsoft_Windows_Server_2012_R2 "wikilink")[Windows 8.1と同じコードを基盤として構築されている](https://ja.wikipedia.org/wiki/Microsoft_Windows_8.1 "wikilink")。このバージョンよりWindows VistaとWindows Server 2008の展開をサポートしない。

### Windows PE 5.1

Windows PE 5.0にWindows 8.1 Updateを適用したもの\[2\]。Windows ADK 8.1 Updateには引き続きWindows PE 5.0が含まれている。

### Windows PE for Windows 10

[Windows 10と同じコードを基盤として構築されている](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")。Windows as a Serviceに基づくWindows 10のリリースと同時期に相当する更新がリリースされる。

  - 10.0.10240.16384

バージョン1507相当。

  - 10.0.10586.0

バージョン1511相当。

  - 10.0.14393.0

バージョン1607相当。

  - 10.0.15063.0

バージョン1703相当。

  - 10.0.16299.0

バージョン1709相当。

## 関連項目

  - [プラットフォーム (コンピューティング)](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")
  - [BartPE](../Page/BartPE.md "wikilink") - WinPEのサードパーティー版と言える。
  - [Windows 回復環境](https://ja.wikipedia.org/wiki/Windows_回復環境 "wikilink") (WinRE) - Windows PEをベースにした、回復用のオペレーティングシステム

## 脚注

[Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:パッケージ管理システム](https://ja.wikipedia.org/wiki/Category:パッケージ管理システム "wikilink")

1.  [Windows 7 用自動インストール キット Readme](http://technet.microsoft.com/ja-jp/library/dd349350)
2.