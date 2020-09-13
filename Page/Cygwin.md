> この記事は[Cygwin](https://ja.wikipedia.org/wiki/Cygwin)から翻訳されています。


**Cygwin**（シグウィン）は、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")上に[UNIX](../Page/UNIX.md "wikilink")ライクな環境を提供する[互換レイヤー](../Page/互換レイヤー.md "wikilink")である。[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。Cygwinをインストールすることで、[OS](../Page/OS.md "wikilink")の差を吸収し、[Windows上で](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[UNIX](../Page/UNIX.md "wikilink")のソフトウェア資産を活かすことが可能となる。

## 特徴

**[UNIX](../Page/UNIX.md "wikilink")的な操作体系を提供するが、[仮想マシンではなく](../Page/仮想機械.md "wikilink")[互換レイヤー](../Page/互換レイヤー.md "wikilink")である。**Cygwinでは[POSIX](../Page/POSIX.md "wikilink")に準拠したUNIX[カーネル](../Page/カーネル.md "wikilink")を利用する代わりに、API変換を行ってWindowsカーネルを利用する方式を採っている。その結果として、UNIX環境上のツール群をWindows上に再コンパイルのみで移植することを可能にしている。[ランタイムライブラリ](../Page/ランタイムライブラリ.md "wikilink")「Cygwin1.dll」がAPI変換の中核を成しており、元々のUNIXアプリの外側でWindows APIへの適合を行っている。

Cygwin1.dllランタイムライブラリが、[POSIX](../Page/POSIX.md "wikilink")の[システムコール](../Page/システムコール.md "wikilink")と同等の機能を提供しており、それぞれのプログラムはこれを動的にリンクすることでUNIX上とほぼ同じ動作が可能になる。また、このライブラリの存在により、Cygwin用として提供されていない他のUNIX用プログラムのソースコードも、従来の様な大幅な変更無しにWindows用にコンパイルすることが可能である。

ランタイムライブラリにて、[Unix System V由来の](https://ja.wikipedia.org/wiki/Unix_System_V "wikilink")[IPCを利用するアプリケーションのために](../Page/プロセス間通信.md "wikilink")、サービス（NTサービス）を用意している。現在Cygwinに付属している[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")は、このサービスが提供する共有[バッファ](../Page/バッファ.md "wikilink")や[セマフォ](../Page/セマフォ.md "wikilink")を利用して動作する。PostgreSQL自身は、バージョン8.0以降ではCygwin依存から脱却し、全面的にWin32ネイティブにソースの書き換えが行われている。

[Xサーバとして](../Page/X_Window_System.md "wikilink")[Cygwin/X](https://ja.wikipedia.org/wiki/Cygwin/X "wikilink")が提供されている。

マイクロソフトはWindows Server 2012より[UNIXベースアプリケーション用サブシステムを非推奨とし](../Page/Microsoft_Windows_Services_for_UNIX.md "wikilink")、代替手段の一つとしてCygwinのPOSIXエミュレーションモードを紹介している\[1\]。

## 脚注

## 関連項目

  - [MinGW](../Page/MinGW.md "wikilink")
  - [Windows Subsystem for Linux](https://ja.wikipedia.org/wiki/Windows_Subsystem_for_Linux "wikilink") - Windows純正のLinuxサブシステム
  - [Interix](https://ja.wikipedia.org/wiki/Interix "wikilink") ([Services for UNIX](https://ja.wikipedia.org/wiki/Services_for_UNIX "wikilink"))
  - [coLinux](../Page/Cooperative_Linux.md "wikilink") - LinuxカーネルをWindowsアプリケーションとして動作させる
  - [シグナスソリューションズ](../Page/シグナスソリューションズ.md "wikilink")
  - [Wine](../Page/Wine.md "wikilink") - Cygwinとは逆に、[Unix系](../Page/Unix系.md "wikilink")OSでWindowsアプリケーションを動作させる
  - [XonWindows3](https://ja.wikipedia.org/wiki/XonWindows3 "wikilink")
  - [仮想化](../Page/仮想化.md "wikilink")

## 外部リンク

  -

  - [Cygwin情報](http://www.jaist.ac.jp/~fujieda/cygwin/)

  - [Using Cygwin.](http://sohda.net/cygwin/)

  - [Life with Cygwin](http://www.oki-osk.jp/esc/cygwin.html)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:エミュレーションソフトウェア](https://ja.wikipedia.org/wiki/Category:エミュレーションソフトウェア "wikilink") [Category:システム管理](https://ja.wikipedia.org/wiki/Category:システム管理 "wikilink")

1.