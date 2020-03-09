> この記事は[Cygwin](https://ja.wikipedia.org/wiki/Cygwin)から翻訳されています。


**Cygwin**（シグウィン）は、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")上に[UNIX](../Page/UNIX.md "wikilink")ライクな環境を提供する互換レイヤーである。[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。

## 特徴

**[UNIX](../Page/UNIX.md "wikilink")的な操作体系を持つが、[エミュレータではなく](../Page/エミュレータ_\(コンピュータ\).md "wikilink")[互換レイヤー](https://ja.wikipedia.org/wiki/互換レイヤー "wikilink")である。**[POSIX](https://ja.wikipedia.org/wiki/POSIX "wikilink")に準拠するシステムコール と [Windows API](https://ja.wikipedia.org/wiki/Windows_API "wikilink") の間のAPI互換を行っている。その結果として、UNIX環境上のツール群をWindows上に再コンパイルのみで移植することを可能にしている。API互換機能は[ランタイムライブラリ](../Page/ランタイムライブラリ.md "wikilink")「Cygwin1.dll」が担っている。

Cygwin1.dllランタイムライブラリが、[POSIX](https://ja.wikipedia.org/wiki/POSIX "wikilink")の[システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")と同等の機能を提供しており、それぞれのプログラムはこれを動的にリンクすることでUNIX上とほぼ同じ動作が可能になる。また、このライブラリの存在により、Cygwin用として提供されていない他のUNIX用プログラムのソースコードも、従来の様な大幅な変更無しにWindows用にコンパイルすることが可能である。

ランタイムライブラリにて、[Unix System V由来の](https://ja.wikipedia.org/wiki/Unix_System_V "wikilink")[IPCを利用するアプリケーションのために](../Page/プロセス間通信.md "wikilink")、サービス（NTサービス）を用意している。現在Cygwinに付属している[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")は、このサービスが提供する共有[バッファ](https://ja.wikipedia.org/wiki/バッファ "wikilink")や[セマフォ](https://ja.wikipedia.org/wiki/セマフォ "wikilink")を利用して動作する。PostgreSQL自身は、バージョン8.0以降ではCygwin依存から脱却し、全面的にWin32ネイティブにソースの書き換えが行われている。

[Xサーバとして](../Page/X_Window_System.md "wikilink")[Cygwin/X](https://ja.wikipedia.org/wiki/Cygwin/X "wikilink")が提供されている。

マイクロソフトはWindows Server 2012より[UNIXベースアプリケーション用サブシステムを非推奨とし](https://ja.wikipedia.org/wiki/Microsoft_Windows_Services_for_UNIX "wikilink")、代替手段の一つとしてCygwinのPOSIXエミュレーションモードを紹介している\[1\]。

## 脚注

## 関連項目

  - [MinGW](https://ja.wikipedia.org/wiki/MinGW "wikilink")
  - [Windows Subsystem for Linux](https://ja.wikipedia.org/wiki/Windows_Subsystem_for_Linux "wikilink") - Windows純正のLinuxサブシステム
  - [Interix](https://ja.wikipedia.org/wiki/Interix "wikilink") ([Services for UNIX](https://ja.wikipedia.org/wiki/Services_for_UNIX "wikilink"))
  - [coLinux](https://ja.wikipedia.org/wiki/Cooperative_Linux "wikilink") - LinuxカーネルをWindowsアプリケーションとして動作させる
  - [シグナスソリューションズ](https://ja.wikipedia.org/wiki/シグナスソリューションズ "wikilink")
  - [Wine](https://ja.wikipedia.org/wiki/Wine "wikilink") - Cygwinとは逆に、[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")OSでWindowsアプリケーションを動作させる
  - [XonWindows3](https://ja.wikipedia.org/wiki/XonWindows3 "wikilink")
  - [仮想化](https://ja.wikipedia.org/wiki/仮想化 "wikilink")

## 外部リンク

  -

  - [Cygwin情報](http://www.jaist.ac.jp/~fujieda/cygwin/)

  - [Using Cygwin.](http://sohda.net/cygwin/)

  - [Life with Cygwin](http://www.oki-osk.jp/esc/cygwin.html)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:エミュレーションソフトウェア](https://ja.wikipedia.org/wiki/Category:エミュレーションソフトウェア "wikilink") [Category:システム管理](https://ja.wikipedia.org/wiki/Category:システム管理 "wikilink")

1.