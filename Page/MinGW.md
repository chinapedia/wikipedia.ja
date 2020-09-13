> この記事は[MinGW](https://ja.wikipedia.org/wiki/MinGW)から翻訳されています。


**MinGW**（ミン・ジー・ダブリュー、**Min**imalist **G**NU for **W**indows）は[GNU](../Page/GNU.md "wikilink")[ツールチェーンの](https://ja.wikipedia.org/wiki/GNUツールチェーン "wikilink")[Windows移植版である](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。MinGWは[Windows APIのための](../Page/Windows_API.md "wikilink")[ヘッダファイル](../Page/ヘッダファイル.md "wikilink")を含んでおり、[フリーの](../Page/フリーソフトウェア.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")である[GCCを](../Page/GNUコンパイラコレクション.md "wikilink")、 Windowsアプリケーションの開発のために利用できる。

MinGWプロジェクトでは、32bit環境向けの2つの主要なパッケージを開発、配布している。Windows環境に移植されたGCCは、[コマンドラインから使用することも](../Page/Cmd.exe.md "wikilink")、[IDEへ統合することもできる](../Page/統合開発環境.md "wikilink")。もう1つの[MSYS](../Page/MSYS.md "wikilink") (*minimal system*) は軽量のUNIX風シェル環境であり、[端末エミュレータ](../Page/端末エミュレータ.md "wikilink")の[rxvt](https://ja.wikipedia.org/wiki/rxvt "wikilink")と、開発ツールの[autoconfを実行可能にするための](../Page/Autotools.md "wikilink")[POSIX](../Page/POSIX.md "wikilink")コマンド群とが含まれている。

この2つのパッケージは、[Cygwin](../Page/Cygwin.md "wikilink")からフォークして誕生した。CygwinではWindowsの機能性を犠牲にすることで、より機能的なUnix風環境を提供している。なお、どちらのパッケージも[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")で、Win32APIを利用するためのヘッダファイルは[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")で提供されており、GNUツールの移植版はGPLである。MinGWの個々のGNUツール及びMSYSは、MinGWの公式サイトより入手可能である。

また、派生プロジェクトとしてが存在する。

## 名称の由来

MinGWの名称は*Minimalist [GNU](../Page/GNU.md "wikilink") for Windows*（Windowsのための最小限度のGNUの意）を表す。*Win32* APIの為のヘッダーを提供するので*Mingw32*とも呼ばれる。*MinGW*の規範となる発音は未だ決定されていないが、一般的には、"*ming wee*", "*min gee double-u*", "*ming double-u*" または "*min gnu*" などのように発音されている。

## 特徴

MinGWと[MSYS](../Page/MSYS.md "wikilink")を両方合わせても小さく、それ自身で完結可能な環境であり、リムーバブル・メディアから使用することが可能である。その際に、コンピュータ上の[レジストリ](../Page/レジストリ.md "wikilink")やファイルに影響を与えない。一方、Cygwinはより多くの機能を提供するために、インストールとその後の管理が複雑である。

さらに、MinGWは[Linux](../Page/Linux.md "wikilink")上など異なる[OSでの](../Page/オペレーティングシステム.md "wikilink")[クロスコンパイル](https://ja.wikipedia.org/wiki/クロスコンパイル "wikilink")にも対応している。このため、MSYSがインストールされたWindowsを利用せずに、Windows用のアプリケーションを開発できる。

## Cygwinとの比較

MinGWはCygwin 1.3.3から[フォークした](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")。Cygwin、MinGWいずれもUnixソフトウェアのWindowsへの移植に使用されるが、異なる方針を採っている。CygwinはWindows上に、Linuxや他のUNIXシステムに見られるような、完全なPOSIX層を提供することを目標にしており、互換性のために必要であれば性能も犠牲にしている。一方でMinGWはフリーのコンパイラと各種ツールのみを提供し、性能を重視している。

アプリケーション移植の観点で見ると、MinGWはPOSIX APIを提供していない。このため、Cygwinでコンパイル可能だがMinGWでは不可能なUnixアプリケーションが存在する。具体的には、特定のPOSIXの機能を要求する、又は、POSIX環境中で実行されることを前提とするアプリケーションが当てはまる。この問題を回避しMinGWで動かすためには、cygwin1.dll内の関数を直接利用する方法または、、[SDL](../Page/SDL.md "wikilink")、[wxWidgets](https://ja.wikipedia.org/wiki/wxWidgets "wikilink")、[Qt](../Page/Qt.md "wikilink")、[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")あるいは[gnulib](https://ja.wikipedia.org/wiki/gnulib "wikilink")のようなプラットフォーム非依存のライブラリを使用してアプリケーションを作成する必要がある。そのほかの移植時の注意点として、MinGWでは、ネットワークプログラミングの read/write を、recv/send に置き換える必要がある。これは、Windowsでのsocketの実装が[Winsock](../Page/Winsock.md "wikilink")であり、POSIXと異なるためである。このため、単なるツールチェーンとして提供されているMinGWでは、この修正は今後とも必要である\[1\]\[2\]。

この違いは、MinGWとcygwinで、libcライブラリ、[標準Cライブラリ](../Page/標準Cライブラリ.md "wikilink")をはじめとして、異なるライブラリを使用しているためである。MinGWでは、Microsoftから直接提供されるライブラリmsvcrt.dllを用いている。しかし、Cygwinでは、POSIX互換の為に[DLL](../Page/ダイナミックリンクライブラリ.md "wikilink") (cygwin1.dll) を独自に導入して解決している。Cygwinでは、独自ライブラリを用いているため、ランタイムライブラリのライセンスによる制限を受ける\[3\]。なお、MinGWでも、MSYSのライブラリ（msys-1.0.dllやmsys-z.dll）をリンクしている場合、これらのランタイムライブラリライセンスによる制限 (GPL) を受ける\[4\]。

なお、CygwinでMinGW用プログラムの開発が可能であった。CygwinのGCCは gcc-3 まではオプション "-mno-cygwin" を渡すと、MinGWのヘッダファイルとランタイムライブラリを用いてバイナリが作成された。gcc-4 からは現在のところこのオプションは削除されている。 その代わりとして Cygwin 用の GCC とは別に MinGW 用の GCC がクロス開発用のコンパイラの一つとして提供されるようになった。2020年4月現在の Cygwin (64bit 版) 収録パッケージでは、gcc-core が Cygwin 用、mingw64-x86_64-gcc-core が MinGW用である（正確には派生プロジェクトMingw-w64である）。Cygwin 用 GCC が /usr/bin/gcc.exe であるのに対して、MinGW 用 GCC は /usr/bin/x86_64-w64-mingw32-gcc.exe のようにコマンド名のプレフィックスとして"x86_64-w64-mingw32-" が付く。その他の付随するツールチェイン(cpp や ld など)も同様である。Autotools による configure && make を行う際は、configure に --host=x86_64-w64-mingw32 オプションを与えることで Mingw-w64 によるビルドを行うことができる。

ライブラリの依存関係は、"objdump -p ファイル名" で見ることができる。

## クロス開発環境

MinGWのバイナリは、Linux上でも開発することができる。Linuxの場合、[Wine](../Page/Wine.md "wikilink")を使ってテストを行うことが簡便である。なお、[RPMファイルは](https://ja.wikipedia.org/wiki/RPM_\(ファイルフォーマット\) "wikilink")、次のページから取得することができる。\[[http://mirzam.it.vu.nl/mingw/\]なお](http://mirzam.it.vu.nl/mingw/%5Dなお)、[Fedora](../Page/Fedora.md "wikilink")では、以下のSIGが立ち上がっている。\[[https://fedoraproject.org/wiki/SIGs/MinGW\]クロスコンパイル環境でドライバを作るための注意点などは、以下の記事も参考になる](https://fedoraproject.org/wiki/SIGs/MinGW%5Dクロスコンパイル環境でドライバを作るための注意点などは、以下の記事も参考になる)。[1](http://strdup.livejournal.com/34596.html)

## MinGWで作成出来るアプリケーション

  - [Git](../Page/Git.md "wikilink")（[分散バージョン管理システム](https://ja.wikipedia.org/wiki/分散バージョン管理システム "wikilink")）
  - Windows PV driver for Xen（準仮想ドライバ）
  - Source Navigator（統合開発環境・ソース解析ツール）
  - Ecere SDK（C言語上位互換オブジェクト指向言語である[eC言語](https://ja.wikipedia.org/wiki/:en:eC_\(programming_language\) "wikilink")、統合開発環境、[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")や3Dライブラリなどを中心に構成されたクロスプラットホームのソフトウェア開発キット）

## 64ビット向け開発環境

MinGWプロジェクトでは[64ビット](../Page/64ビット.md "wikilink")環境向けのコンパイラセットは提供されていない。

64ビット向け開発環境は、mingw.org から2007年にフォークしたMingw-w64\[5\]と、MinGWプロジェクトのMSYSを組み合わせれば構築できる。

## そのほか

MinGWの開発環境としては、MSYSが標準であるが、そのほかに、[Eclipseや](../Page/Eclipse_\(統合開発環境\).md "wikilink")[DOSプロンプト](../Page/DOSプロンプト.md "wikilink")、[CLionで開発することもできる](https://ja.wikipedia.org/wiki/CLion\(統合開発環境\) "wikilink")。

[Intel Threading Building Blocksも](https://ja.wikipedia.org/wiki/Intel_Threading_Building_Blocks "wikilink")、将来的には、MinGWでコンパイルできる見込みである\[6\]。

## 関連項目

  - [GNUコンパイラコレクション](../Page/GNUコンパイラコレクション.md "wikilink")（GCC）
  - [Cygwin](../Page/Cygwin.md "wikilink")
  - [TDM-GCC](https://ja.wikipedia.org/wiki/TDM-GCC "wikilink")
  - [Interix](https://ja.wikipedia.org/wiki/Interix "wikilink")
  - [Microsoft Windows Services for UNIX](../Page/Microsoft_Windows_Services_for_UNIX.md "wikilink")(SFU), Subsystem for UNIX-based Applications(SUA)

## 出典

## 外部リンク

  - [MinGW Home](http://www.mingw.org/)
      - [MinGW FAQ](http://www.mingw.org/wiki/FAQ)
      - [GCC status](http://www.mingw.org/MinGWiki/index.php/GccStatus)
  - [MinGW OSDN Home](https://ja.osdn.net/projects/mingw/)
  - [SourceForge Project Of The Month (September 2005)](https://sourceforge.net/blog/potm-2005-09/)
  - [MinGW FAQ](http://www.sixnine.net/cygwin/translation/mingw-doc/mingwfaq.html)
  - ["-mno-cygwin" -- Building MinGW executables using Cygwin](http://www.sixnine.net/cygwin/translation/devel/mno-cygwin-howto.html)
  - [MinGW RSS](https://osdn.net/projects/mingw/releases/rss)

### 環境構築事例

  - [VideoLANの場合](https://wiki.videolan.org/Win32CompileMSYS)

[Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:1998年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1998年のソフトウェア "wikilink")

1.  [Winsock Functions (Windows)](http://msdn2.microsoft.com/en-us/library/ms741394.aspx) Microsoft Developer Network
2.  [\[Mingw-users\] about fprintf stderr support on mingw](http://sourceforge.net/mailarchive/forum.php?thread_name=c9b6d9a50803190317v104f46bcxde295e0b782c4a4e%40mail.gmail.com&forum_name=mingw-users) MinGW - Minimalist GNU for Windows / Mailing Lists
3.  [Cygwin Licensing Terms](http://cygwin.com/licensing.html)
4.  [FAQ | MinGW](http://www.mingw.org/wiki/FAQ)
5.  [Mingw-w64 - GCC for Windows 64 & 32 bits](https://mingw-w64.org/)
6.  [2](http://softwarecommunity.intel.com/isn/Community/en-US/forums/thread/30250439.aspx)