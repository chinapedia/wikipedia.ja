> この記事は[Wine](https://ja.wikipedia.org/wiki/Wine)から翻訳されています。


**Wine** （ワイン）は、[オープンソース](../Page/オープンソース.md "wikilink")の [Windows API](../Page/Windows_API.md "wikilink") 実装を通じて、主として[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")[アーキテクチャ上の](../Page/コンピュータ・アーキテクチャ.md "wikilink")[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") ([POSIX](../Page/POSIX.md "wikilink")準拠OS) において[Windows用](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[アプリケーションをネイティブ動作させることを目標とする](../Page/アプリケーションソフトウェア.md "wikilink")[プログラム群である](../Page/プログラム_\(コンピュータ\).md "wikilink")。

[X Window Systemを利用して](../Page/X_Window_System.md "wikilink")、[16ビット](../Page/16ビット.md "wikilink")・[32ビット](../Page/32ビット.md "wikilink")・[64ビット](../Page/64ビット.md "wikilink")Windows向け[GUIアプリケーションを動作させることができるほか](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、[MS-DOS](../Page/MS-DOS.md "wikilink")用アプリケーションも動作する。x86上の[Linux](../Page/Linux.md "wikilink")環境を中心に開発されているので、[Solaris](../Page/Solaris.md "wikilink") 、[FreeBSD](../Page/FreeBSD.md "wikilink") 、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")など、他のOSにも移植されているが、それらの環境下では問題が発生する可能性は比較的高い。原理上、[カーネル](../Page/カーネル.md "wikilink")レベルの[スレッドに対応しているOSであることが必要である](../Page/スレッド_\(コンピュータ\).md "wikilink")\[1\]。

名称は、もともとは[頭字語](../Page/頭字語.md "wikilink")であることを意識して、大文字でWINEと表記していたことがあったが、現在はWineと表記するのが正式である\[2\]。"**WIN**dows **E**mulator" に由来すると説明されることもあるが、**W**ine **I**s **N**ot an **E**mulator に由来するという、一見してジョークとも取れる、前者とは矛盾する説明がなされることもあり、これは技術的理由による。詳しくは後述する。

ライセンスに[LGPLを採用している](../Page/GNU_Lesser_General_Public_License.md "wikilink")\[3\]。[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。

かつては[BSDライセンス](../Page/BSDライセンス.md "wikilink")を採用していた。

## 概要

[thumb](https://ja.wikipedia.org/wiki/ファイル:Media_Player_Classic-6.4.8.3_on_Wine.png "wikilink") バージョン 6.4.8.3\]\] Wine以外にLinux上でWindowsアプリケーションを動作させる方法としては、[Xenや](../Page/Xen_\(仮想化ソフトウェア\).md "wikilink")[VMware](../Page/VMware.md "wikilink")など、[仮想マシンを構築するものが代表的である](../Page/仮想機械.md "wikilink")。Wineはそれらとは異なり、[互換レイヤー](../Page/互換レイヤー.md "wikilink")として動作する。つまり、Windowsプログラムが要求する[DLLの代替品を供給し](../Page/ダイナミックリンクライブラリ.md "wikilink")、また [Windows NT](../Page/Windows_NT系.md "wikilink")[カーネル](../Page/カーネル.md "wikilink")の[プロセス](../Page/プロセス.md "wikilink")を再現することによって、Windowsプログラムをネイティブ動作させる。簡単に言えばWineは、Linux上でWindowsを動作させているのではなく、LinuxにWindowsと同じ挙動をさせているのである。したがってWineでWindowsプログラムを動作させる上では、Windowsのコピーもライセンスも必要ではない\[4\]。ただし、Wineのエミュレーションライブラリが不完全な場合にはWindowsのDLLを利用することで解決できる場合がある\[5\]が、その場合にはWineを動作させるコンピュータにWindowsのコピーとライセンスが必要である。

ところで、Wineという名称は "**W**ine" **I**s **N**ot an **E**mulator を略した[再帰的頭字語](../Page/再帰的頭字語.md "wikilink")であるとも説明される\[6\]。[DOSBox](https://ja.wikipedia.org/wiki/DOSBox "wikilink")やzsnesのような典型的なエミュレータと異なり、Wineは基本的にはCPUエミュレーションを行っていない。そのため通常この種のエミュレータに発生する、オリジナル環境と比べた著しいパフォーマンス低下がWineには見られない。このことを強調する開発者の立場から、そのような説明がなされる。実際、アプリケーションによってはWindows上より高速に動作することもあるという\[7\]。同じく基本的にはCPUエミュレーションを行わない、x86上の仮想マシンにインストールしたWindows環境と比べても、そのような実行速度は優れたものである。しかし、その代償としてプロジェクト規模が巨大化したWineは、人的資源の不足のため本来実装されるべき機能が依然として完全には提供されていない\[8\]。そのため再現性は仮想マシン上にインストールしたWindowsと比べて大きく劣る。高速化よりはむしろ再現性の向上を第一の目標として開発されている。 なお、ドライバは対応しない。カーネルモードドライバが多く、カーネルモードでの実行が必要なため。\[9\]

Wineに含まれるWindows API実装はWinelibと呼ばれ、これを用いてWindowsプログラムのソースコードから[プラットフォームネイティブな](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")[バイナリ](../Page/バイナリ.md "wikilink")（[実行ファイル](../Page/実行ファイル.md "wikilink")やDLL）を[ビルドすることも可能である](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink")。しかしながら、x86環境では付属するバイナリローダー（wineコマンド）から[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")済みバイナリを起動すればよく、実用上は実行速度にも大きな差はない。非x86環境でWindowsバイナリを実行するためには、[QEMU](../Page/QEMU.md "wikilink")などを[CPU](../Page/CPU.md "wikilink")[エミュレータ](../Page/エミュレータ.md "wikilink")として利用可能\[10\]だが、低速である。

## 歴史

[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の[PWI](https://ja.wikipedia.org/wiki/PWI "wikilink") (Public Windows Initiative) や[Wabi](https://ja.wikipedia.org/wiki/Wabi "wikilink")\[11\]（Windows API の[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")ソフトウェアによる完全代替を目指したもの）の影響を受け、ボブ・アムスタッドとエリック・ヤングデイルによりWindowsアプリケーションを[Linux](../Page/Linux.md "wikilink")上で動作させることを目的としてWineプロジェクトは[1993年](../Page/1993年.md "wikilink")にネットニュース上で創始された\[12\]。当初は[Windows 3.1用](../Page/Microsoft_Windows_3.x.md "wikilink")（16 ビット）アプリケーションに主眼を置いたが、現在は 32ビット中心に開発されている。[1994年](../Page/1994年.md "wikilink")以降はアレクサンダー・ジュリアードがプロジェクトリーダーを務めている\[13\]。

プロジェクトは困難を極め、なかなか[互換性](../Page/互換性.md "wikilink")が高まらなかった。特に [1990年代](../Page/1990年代.md "wikilink")は、日本語環境においてアプリケーションが思うように動かせない状況が続き、Wineのインストールや動作にもそれなりのスキルが必要とされていた。

Wineプロジェクトに着目した[コーレル](../Page/コーレル.md "wikilink")などの支援によって一時的に状況は好転したが、[マイクロソフト](../Page/マイクロソフト.md "wikilink")のコーレルへの大規模投資が原因となって、この支援は中止された\[14\]。

現在はCodeWeaversがジュリアードらを雇っている\[15\]。また、[Google](../Page/Google.md "wikilink")はLinux版[Picasa](../Page/Picasa.md "wikilink")でWineを利用し、Wineの開発を支援している\[16\]。

  - [2005年](../Page/2005年.md "wikilink")[10月25日](../Page/10月25日.md "wikilink") - 最初の[ベータ版](../Page/ベータ版.md "wikilink")となったバージョン 0.9 がリリース。
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[5月9日](../Page/5月9日.md "wikilink") - 最初のリリース候補版 (1.0-rc1) がリリース。
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[6月17日](../Page/6月17日.md "wikilink") - Wine 1.0がリリース\[17\]。
  - [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[5月21日](../Page/5月21日.md "wikilink")Wine 1.2のリリース候補版 (1.2-rc1) がリリース\[18\]。
  - [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[7月16日](../Page/7月16日.md "wikilink") - Wine 1.2がリリース\[19\]。
  - [2012年](../Page/2012年.md "wikilink")[5月7日](../Page/5月7日.md "wikilink") - Wine 1.4がリリース\[20\]。
  - [2013年](../Page/2013年.md "wikilink")[7月18日](../Page/7月18日.md "wikilink") - Wine 1.6がリリース\[21\]。
  - [2015年](../Page/2015年.md "wikilink")[12月19日](https://ja.wikipedia.org/wiki/12月19日 "wikilink") - Wine 1.8がリリース\[22\]。
  - [2017年](../Page/2017年.md "wikilink")[1月24日](../Page/1月24日.md "wikilink") - Wine 2.0がリリース。[Microsoft Office 2013のオンラインアクティベーション](https://ja.wikipedia.org/wiki/Microsoft_Office_2013 "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")において64bitアプリケーションの起動などが新たにサポートされた\[23\]。
  - [2018年](../Page/2018年.md "wikilink")[1月18日](../Page/1月18日.md "wikilink") - Wine 3.0がリリース。[Direct3D](../Page/Direct3D.md "wikilink") 10および11などが新たにサポートされた\[24\]。
  - [2019年](../Page/2019年.md "wikilink")[1月22日](../Page/1月22日.md "wikilink") - Wine 4.0がリリース。[Vulkan](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink") 1.0、Direct3D 12などが新たにサポートされた\[25\]。
  - [2020年](../Page/2020年.md "wikilink")[1月21日](../Page/1月21日.md "wikilink") - Wine 5.0がリリース。[マルチモニター](../Page/マルチモニター.md "wikilink")、Vulkan 1.1などが新たにサポートされた\[26\]。

## 対応アプリケーション

WineにおけるWindowsアプリケーションの動作状態は [Wine アプリケーションデータベース (AppDB)](http://appdb.winehq.org/index.php) で調べることができる。Wine AppDBではWineユーザからの動作報告がデータベース化されており、アプリケーションが動作状況の良い順に "**Platinum**"、"**Gold**"、"**Silver**"、"**Bronze**"、"**Garbage**" で格付けされている\[27\]。一般にWineのバージョン毎に格付けが変わる。

Wine 1.0で

  - [Adobe Photoshop](../Page/Adobe_Photoshop.md "wikilink") CS2体験版
  - [Microsoft PowerPoint](../Page/Microsoft_PowerPoint.md "wikilink") Viewer 97と2003
  - [Microsoft Word](../Page/Microsoft_Word.md "wikilink") Viewer 97と2003
  - [Microsoft Excel](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink") Viewer 97と2003

がリリース基準に使われた\[28\]こともあり、Wine 1.0ではこれらのアプリケーションが問題なく動作すると報告されている\[29\]\[30\]\[31\]\[32\]。

補足しておくと、Wineに[DirectXのランタイムをインストールするのは非推奨である](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")。これはDirectXが直接ハードウェアをコントロールすることがあるため、Windowsそのものが存在しているわけではないWine環境においては、CPUやGPUといったハードウェアを破壊しかねない可能性があるためである。また、Wineが搭載しているDirectXのランタイムで大抵のアプリケーションは動く。

## 付属プログラム

Wineには*wine*コマンドを中心として様々なプログラムやツールが含まれている\[33\]。

  - wine:一般に Wineがインストールされた環境でWindowsプログラムを起動するにはEXEファイルをダブルクリックすればよい。しかし、場合によっては[デバッグ](../Page/デバッグ.md "wikilink")などの目的で[コマンドラインからプログラムを起動させたいことがある](../Page/コマンドラインインタプリタ.md "wikilink")。wineはこのようなときに用いるコマンドで、引数にWindowsプログラムを指定する。
    Wine設定 (winecfg):Wine全体の設定を[GUIで行うためのプログラムである](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。
    Wine File (winefile):[MDI](../Page/Multiple_Document_Interface.md "wikilink") 型の[ファイルマネージャ](../Page/ファイルマネージャ.md "wikilink")であり、[Windows Explorer](../Page/Windows_Explorer.md "wikilink") に対応する（見た目としては[Windows 3.xのファイルマネージャに近い](../Page/Microsoft_Windows_3.x.md "wikilink")）。コマンドラインから`wine explorer`と入力することでも起動する。
    Wine Application Uninstaller (uninstaller):GUIでプログラムをアンインストールするためのツールであり、Windowsの「プログラムの変更と削除」に対応する。
    regedit:GUIで[レジストリ](../Page/レジストリ.md "wikilink")を編集するためのプログラムであり、同名のWindows付属プログラムに対応する。

[コマンドプロンプト](../Page/コマンドプロンプト.md "wikilink") (cmd)、[メモ帳](../Page/メモ帳.md "wikilink") (notepad)、[タスクマネージャ](https://ja.wikipedia.org/wiki/タスクマネージャ "wikilink") (taskmgr)、[マインスイーパ](../Page/マインスイーパ.md "wikilink") (winemine) や[ワードパッド](../Page/ワードパッド.md "wikilink") (wordpad) [コントロールパネル](https://ja.wikipedia.org/wiki/コントロールパネル "wikilink") (control) なども含まれている。コマンドラインから起動する場合、cmd、taskmgr、wordpad、controlなど一部のプログラムについては、wineコマンドの引数としてプログラム名を指定して起動する。例えば、ワードパッドを起動するには[仮想端末](https://ja.wikipedia.org/wiki/仮想端末 "wikilink")から

`$ wine wordpad`

と入力する。なお $ は [Bash](../Page/Bash.md "wikilink") 等の[シェル](../Page/シェル.md "wikilink")におけるプロンプトである。

### Wine Tools

Wine ToolsはWineに含まれるツール群である。これらはWindows型実行可能ファイルではなく、[Perl](../Page/Perl.md "wikilink")や[C言語](../Page/C言語.md "wikilink")などで記述された[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")ネイティブプログラムである。

  - Wine Server (wineserver):WineにおいてWindowsのカーネルプロセスを再現するためのプログラム。
    Wine Message Compiler(wmc):メッセージファイル(.mc)をコンパイルするプログラム。
    Wine C and C++ MinGW Compatible Compiler (winegcc):Linux上でMinGWの互換コンパイルを可能にするための[gcc](https://ja.wikipedia.org/wiki/gcc "wikilink")の実装。
    Wine Interface Definition Language ([IDL](../Page/インタフェース記述言語.md "wikilink")) compiler (wild):IDLで記述されたインターフェースをコンパイルするプログラム。
    Wine DLL Tool (winedump):DLLを解析し、インポート/エクスポートされている関数を調べ、スペックファイル(.spec)を生成するためのプログラム。
    Wine Maker (winemaker):WindowsのプロジェクトをWine向けにコンパイルするプログラム。
    Wine Console (wineconsole):コマンドラインインターフェースのWindowsソフトウェアを実行するためのプログラム。

## ディレクトリ

Wineやアプリケーションの[EXEファイルや](../Page/EXEフォーマット.md "wikilink")[レジストリ](../Page/レジストリ.md "wikilink")などは[ホームディレクトリ](../Page/ホームディレクトリ.md "wikilink")内の.wineディレクトリ下に保存される。保存先は[環境変数](../Page/環境変数.md "wikilink")WINEPREFIXを設定することで変更できる\[34\]。かつてWineの設定ファイルとしてconfigというファイルがあったが、[2005年](../Page/2005年.md "wikilink")に廃止され\[35\]現在は[拡張子](../Page/拡張子.md "wikilink")がregのファイルに設定が保存されるようになっている。

アプリケーションのデスクトップエントリファイルやアイコンなどはホームディレクトリ下の

  - .config/menus/applications-merged
  - .local/share/applications/wine
  - .local/share/desktop-directories
  - .local/share/icons

にインストールされる\[36\]。これらのディレクトリにインストールされるファイルは[GNOME](../Page/GNOME.md "wikilink")や[KDE](../Page/KDE.md "wikilink")などでメニューに使われる。

## デバッグ

Wineは[環境変数](../Page/環境変数.md "wikilink")WINEDEBUGを使用することで、様々なデバッグが行える。\[37\]

構文

`$export WINEDEBUG=[ クラス ][+|-] チャンネル [,[ クラス2 ][+|-] チャンネル2 ]`

\[ クラス \] にはwarn、err、fixme、traceのいずれかを指定する。また、\[ +|- \]の指定によってチャンネルの入れるか入れないかを切り替える。

チャンネルにはrelay、dll、heap、allなどがある。詳しくは\[38\]のList of Debug Channelsの章を参照。

例

`$WINEDEBUG=warn+all,+relay`

全ての警告メッセージを表示する。すべての中継メッセージを表示する。

この環境変数の指定によって特定のdllの関数がどのような引数で呼び出されているか、どこでどのような関数が完全に実装されていないかが分かる。

## Wineに似た他のプロジェクト

  - CodeWeavers - アメリカの会社で、Windows向けのブラウザ用プラグインソフトを[Linux](../Page/Linux.md "wikilink")上で動作させるCodeWeavers Pluginなどを開発・販売している。Wineベース。また、Windowsアプリケーションを動作させる[CrossOver](https://ja.wikipedia.org/wiki/CrossOver "wikilink") Linuxという製品や、macOS上でWin32アプリケーションを動作させるCrossOver Macを出荷している。
  - [cedega](https://ja.wikipedia.org/wiki/cedega "wikilink") - [TransGaming Technologies](http://www.transgaming.com/)のWineの改良版プロジェクト。Wineよりも先に[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")に対応していたのが特徴。Windows用ゲームを[Linux](../Page/Linux.md "wikilink")上で動かすことを主目的にしていた。
  - [ReactOS](../Page/ReactOS.md "wikilink") - [Windows NTとバイナリレベル](../Page/Microsoft_Windows_NT.md "wikilink")・ドライバレベルでの互換性を確保することを目標とした、[オープンソース](../Page/オープンソース.md "wikilink")プロジェクト。Wineとも協力して開発を進めている。

## Wine 用のツール

  - Wine-Doors - [GNOME](../Page/GNOME.md "wikilink")デスクトップ用のアプリケーション管理ツールであり、Wineに機能を追加する。Wine-Doorsは [WineTools](http://www.von-thadden.de/Joachim/WineTools/) の代りとなるもので、WineToolsの機能を改善し、より現代的な設計アプローチのもとでWineToolsのアイディアを発展させることを狙いとしている。
  - WineBot - [apt](../Page/APT.md "wikilink") / [dpkg](https://ja.wikipedia.org/wiki/dpkg "wikilink") / [rpmのようなネイティブなLinux](../Page/RPM_Package_Manager.md "wikilink")[パッケージマネージャと同様の方法で動作するようなアプリケーション管理ツールである](../Page/パッケージ管理システム.md "wikilink")。このプロジェクトの狙いは特定のアプリケーションをインストールするのに必要な[ハックを追跡するための](../Page/ハッキング.md "wikilink")[プラットフォームと](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")、Wine プロジェクトの自動[退行テストの](https://ja.wikipedia.org/wiki/ソフトウェアテスト#回帰テスト（リグレッションテスト） "wikilink")[フレームワークを提供することに加え](../Page/アプリケーションフレームワーク.md "wikilink")、Wine-Doorsとのデータ[互換性](../Page/互換性.md "wikilink")をもたせることにある。
  - [WineTricks](http://wiki.winehq.org/winetricks) - Wineを正しく動作させるのに必要で基本的な[コンポーネントをインストールするための](../Page/ソフトウェアコンポーネント.md "wikilink")[スクリプトである](../Page/スクリプト言語.md "wikilink")。これを使えば[QuickTime](../Page/QuickTime.md "wikilink")、[Windows Media Player](../Page/Windows_Media_Player.md "wikilink")、 [.NET Frameworkや](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")の[ランタイムライブラリ](../Page/ランタイムライブラリ.md "wikilink")などが簡単にインストールできる。
  - IEs4Linux - バージョン5から6までの[Internet Explorer](../Page/Internet_Explorer.md "wikilink") (IE) をインストールするための[ユーティリティであり](../Page/ユーティリティソフトウェア.md "wikilink")、まもなくIE7もサポートされる予定である。現在IE7の[エンジンはユーザが選択したときにのみインストールされる](https://ja.wikipedia.org/wiki/HTMLレンダリングエンジン "wikilink")（[ベータ段階](../Page/ベータ版.md "wikilink")）。ただしIEのライセンスの関係上、一部のバージョンのIEに関してWine上で使用することはライセンス違反となる可能性が高い\[39\]。また、それ以外のバージョンでもWindowsのライセンスが必須\[40\]である。
  - [WineLocale](http://code.google.com/p/winelocale/) - Windowsプログラムの中には[日本語](../Page/日本語.md "wikilink")や中国語、韓国語などで使われることのある非[Unicode](../Page/Unicode.md "wikilink")の[文字コード](../Page/文字コード.md "wikilink")のサポートを必要とするものがある。 WineLocaleはこのようなプログラムをWineで動作させるための拡張ユーティリティである。[Ubuntu](../Page/Ubuntu.md "wikilink")のフォーラムにこのツールを使うための[ドキュメントがいくつかある](../Page/文書.md "wikilink")\[41\]。
  - [PlayOnLinux](https://ja.wikipedia.org/wiki/PlayOnLinux "wikilink") - Wineを使ってWindowsのゲームのインストールを簡単にするためのアプリケーション。特別な設定が必要なゲームに対して適用するスクリプトのオンライン[データベース](../Page/データベース.md "wikilink")を使っている。ゲームがデータベースに無ければ、手動インストールもできる。ゲーム以外のプログラムもインストールでき、あるプログラムが他のプログラムに干渉することを避け隔離するため個々のプログラムは異なるコンテナ（[環境変数](../Page/環境変数.md "wikilink")の WINEPREFIX）に置かれる。これは[CrossOver Officeのbottlesが動作する方法と同じである](https://ja.wikipedia.org/wiki/CrossOver_Office "wikilink")。

## Wineを利用しているソフトウェア

  - [CrossOver](http://www.codeweavers.com/products/) - Intel Mac、Linux上でWindowsアプリケーションを利用するためのソフトウェア。あらかじめ動作を保証するアプリケーションを提示しており、そのアプリケーションに関してはドライバのインストールなどテクニカルな設定を行う必要が無い。場合によってはある程度テクニカルな設定を行う必要があるが、保証しないアプリケーションに関しても概ね動作する。多くのドライバを必要とするWindows専用のゲームソフトウェアをIntel Mac、Linux上で動かす事を主眼に据えたGamesバージョンも存在する。
  - [MikuInstaller](http://mikuinstaller.sourceforge.jp/) - IntelベースのMacintoshにWindows用のDAWソフトである [初音ミク](../Page/初音ミク.md "wikilink") をインストールするための環境パッケージ。Wineや[CrossOver](https://ja.wikipedia.org/wiki/CrossOver "wikilink")のソースコードの一部を利用している。 [初音ミク](../Page/初音ミク.md "wikilink")をインストールするためのソフトと謳われているものの、書き換えなくても実行できるソフトがある可能性が示唆されておりまた同梱のWineを書き換えることで様々なアプリケーションをMacネイティブで実行できるともしている。なお、現在開発は中止されている。
  - [Pipelight](http://fds-team.de/cms/articles/2013-08/pipelight-using-silverlight-in-linux-browsers.html) - Wineを使い、[Flash Playerや](https://ja.wikipedia.org/wiki/Flash_Player "wikilink")[Microsoft SilverlightなどのWindows以外のOS向けのプラグインが提供されていないものを使用可能にするプロジェクト](../Page/Microsoft_Silverlight.md "wikilink")。
  - [ReactOS](../Page/ReactOS.md "wikilink") - カーネルドライバーを除くWindowsシステムライブラリの実装に用いられる。
  - [VirtualBox](../Page/VirtualBox.md "wikilink") - 一部のDirect3D操作にWineのソースコードを使用。
  - [Parallels Desktop for Mac](../Page/Parallels_Desktop_for_Mac.md "wikilink") - DirectXの操作にWineのソースコードを使用。

## 参照

[Darling](https://ja.wikipedia.org/wiki/Darling_\(ソフトウェア\) "wikilink") - Wineと同様にOSXのコードをオープンソース実装しようというプロジェクト。

## 脚注

### 注釈

### 出典

## 関連項目

  - [Windows API](../Page/Windows_API.md "wikilink")
  - [DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")
  - [ソフトウェア特許](../Page/ソフトウェア特許.md "wikilink")
  - [Bash on Ubuntu on Windows](https://ja.wikipedia.org/wiki/Windows_Subsystem_for_Linux "wikilink")
  - [EasyWine](https://ja.wikipedia.org/wiki/EasyWine "wikilink") - OSX対応のWine。

## 外部リンク

  - [Wine HQ](https://www.winehq.org/)
  - [公式 Wine フォーラム](https://forum.winehq.org/)
  - [Wine アプリケーションデータベース](https://appdb.winehq.org/)
  - [Wine ニュースグループ](news://comp.emulators.ms-windows.wine)（[Google ウェブインターフェイス](http://groups.google.com/group/comp.emulators.ms-windows.wine)）

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:システムソフトウェア](https://ja.wikipedia.org/wiki/Category:システムソフトウェア "wikilink") [Category:1993年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1993年のソフトウェア "wikilink")

1.  [Under what hardware platform(s) and operating system(s) will Wine(Lib) run?](http://www.winehq.org/site/docs/wine-faq/index#UNDER-WHAT-PLATFORMS-WILL-WINE-RUN)
2.  [Why do some people write WINE and not Wine?](http://wiki.winehq.org/FAQ#head-8b4fbbe473bd0d51d936bcf298f5b7f0e8d25f2e)
3.  [Wine License](http://www.winehq.org/site/license)
4.  [Do I need to have a DOS partition on my system to use Wine?](http://www.winehq.org/site/docs/wine-faq/index#DO-I-NEED-TO-HAVE-A-DOS-PARTITION)
5.  [My program doesn't work, what can I do?](http://www.winehq.org/site/docs/wine-faq/index#MY-APP-DOESNT-WORK-WHAT-CAN-I-DO)
6.  [Does Wine emulate a full computer?](http://www.winehq.org/site/docs/wine-faq/index#IS-WINE-AN-EMULATOR)
7.  [Does Wine emulate a full computer?](http://www.winehq.org/site/docs/wine-faq/index#IS-WINE-AN-EMULATOR)
8.  [Win API Stats](http://www.winehq.org/winapi_stats)
9.  [1](http://wiki.winehq.org/FAQ#head-8021e00ae87d4fbfb607739af82bdb621b9d9366)
10. [Wine の起動](http://www.h7.dion.ne.jp/~qemu-win/qemu-doc-ja.html#SEC49)
11. [Wine project status](http://groups.google.com/group/comp.windows.x.i386unix/browse_thread/thread/88fbd87c0ae2e48f/5003eb8ed33ae522)
12. [WABI available on Linux or not](http://groups.google.com/group/comp.os.linux.misc/msg/daa52d28ff44919f)
13.
14. [That's all folks: Corel leaves Open Source behind](http://www.linux.com/articles/21411)
15. [People - Alexandre Julliard](http://www.codeweavers.com/about/people/alexandre/)
16. [Google Sponsors Wine Improvements](http://google-opensource.blogspot.com/2008/02/google-sponsors-wine-improvements.html)
17. [Wine Release Plan](http://wiki.winehq.org/WineReleasePlan)
18. [2](http://www.winehq.org/news/2010052101)
19. [3](http://www.winehq.org/announce/1.2)
20. [4](http://www.winehq.org/announce/1.2)
21. [5](http://www.winehq.org/announce/1.6)
22. [6](http://www.winehq.org/announce/1.8)
23. [7](http://www.winehq.org/announce/2.0)
24. [8](http://www.winehq.org/announce/3.0)
25. [9](http://www.winehq.org/announce/4.0)
26. [10](http://www.winehq.org/announce/5.0)
27. [Maintainer Rating Definitions](http://appdb.winehq.org/help/?sTopic=maintainer_ratings)
28. [Wine 1.0 Release Criteria](http://wiki.winehq.org/WineReleaseCriteria)
29. [Wine AppDB - Photoshop](http://appdb.winehq.org/objectManager.php?sClass=application&iId=17)
30. [Wine AppDB - Powerpoint Viewer](http://appdb.winehq.org/objectManager.php?sClass=application&iId=724)
31. [Wine AppDB - Word Viewer](http://appdb.winehq.org/objectManager.php?sClass=application&iId=202)
32. [Wine AppDB - Excel Viewer](http://appdb.winehq.org/objectManager.php?sClass=application&iId=929)
33. [ListofCommands](http://wiki.winehq.org/ListofCommands)
34. [wine の man ページ](http://www.winehq.org/site/docs/wine)
35. \[<http://www.winehq.org/?issue=281#The%20config%20File%20Has%20Died>\! The config File Has Died\!\]
36. [How do I uninstall Windows applications?](http://wiki.winehq.org/FAQ#head-9893ae50079ca7a959258f0bc9a17aaf2e69b391)
37. [11](http://wiki.winehq.org/DebugChannels)
38. [12](http://wiki.winehq.org/DebugChannels)
39. 例えばIE6 [Service Pack](../Page/拡張パック.md "wikilink") 1の[EULAには](../Page/ライセンス.md "wikilink")「本OSコンポーネントは、該当するOS製品の既存の機能をアップデート、またはこれに追加もしくは代替するためにのみ提供されています。」という一文があり、Windowsのアップグレードとしてのみ使用できる。
40. 例えばIE7の[EULAには](../Page/ライセンス.md "wikilink")「お客様は、マイクロソフト Windows XP SP2 and Windows Server 2003 SP1 ソフトウェアの有効なライセンス取得済みの複製 (以下「本ソフトウェア」といいます) ごとに、本追加物の複製 1 部を使用できます。」という一文があり、Windowsのライセンスと同等とみなしている。
41. [HOWTO: CJK in Wine (Chinese, Japanese & Korean)](http://ubuntuforums.org/showthread.php?t=383628)