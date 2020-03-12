> この記事は[Microsoft Foundation Class](https://ja.wikipedia.org/wiki/Microsoft_Foundation_Class)から翻訳されています。


**Microsoft Foundation Class** (**MFC**) は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が[Visual C++用に開発した](../Page/Microsoft_Visual_C++.md "wikilink")、[Windows用のアプリケーション構築のための](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[アプリケーションフレームワーク](../Page/アプリケーションフレームワーク.md "wikilink")（[クラスライブラリ](../Page/ライブラリ.md "wikilink")）である。[Active Template Library](../Page/Active_Template_Library.md "wikilink") (ATL) と同様に、[Visual Studioに同梱されるライブラリとなっている](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")。

ATL/MFCはもともと有償エディションの[Visual C++単体製品や](../Page/Microsoft_Visual_C++.md "wikilink")、有償エディションのVisual Studio製品のみに同梱されていたが、Visual Studio Communityエディションでは（ライセンス条件が厳しくなっているものの）無償でATL/MFCを利用できる。

## 概要

MFCでは、Windows[アプリケーションにおけるメッセージハンドラやウィンドウフレームワークなどの基礎的な部分をあらかじめパッケージ化したほか](../Page/アプリケーションソフトウェア.md "wikilink")、[GDIオブジェクト](../Page/Graphics_Device_Interface.md "wikilink")、デバイス コンテキスト、[スレッド](../Page/スレッド_\(コンピュータ\).md "wikilink")、[ソケット](../Page/ソケット_\(BSD\).md "wikilink")、[FTP](../Page/File_Transfer_Protocol.md "wikilink")/[HTTPなどのインターネットサービス](../Page/Hypertext_Transfer_Protocol.md "wikilink")、可変長の[文字列](../Page/文字列.md "wikilink")、[配列](../Page/配列.md "wikilink")や[リストといったコンテナなど](../Page/リスト_\(抽象データ型\).md "wikilink")、一般にアプリケーションでよく使われるような[クラスを備えている](../Page/クラス_\(コンピュータ\).md "wikilink")。

[SDKを使って](../Page/ソフトウェア開発キット.md "wikilink")[Windows APIを直接呼び出すのに比べ](../Page/Windows_API.md "wikilink")、Visual C++の統合環境との親和性が高く開発が容易になるという利点があるが、一方でMFCに過度に依存したプログラムを書くと他の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) への[移植が難しくなるといった問題もある](../Page/移植_\(ソフトウェア\).md "wikilink")。

MFCに似たライブラリとしては、[Windows Template Library](../Page/Windows_Template_Library.md "wikilink") (WTL) がある。

## 歴史

MFCは[1992年](../Page/1992年.md "wikilink")、[16ビット](../Page/16ビット.md "wikilink")バージョンのWindowsをターゲットとし、マイクロソフトの[C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink") 7.0とともに発売された。これは開発ツールの分野におけるシェアを高めようとしていたマイクロソフトの努力の一環であり、MFCはプログラミング言語C++の能力を知らしめるよう設計されていた。当時、C++は商用アプリケーションの開発においてCからの移行が始まったばかりであり、C/C++ 7.0はマイクロソフトのコンパイラとして初めてC++をサポートした。MFCは[Macintosh](../Page/Macintosh.md "wikilink")の（TCL、後に[シマンテック](../Page/シマンテック.md "wikilink")によって買収された）に大きく影響を受け、その構造の多くをTCLから受け継いでいた。

同時期、Borland Cコンパイラに対応した (OWL) が、競合製品として[ボーランド](../Page/ボーランド.md "wikilink")から販売されていた。OWLの設計はより厳密に[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")に準じていたので、一時期の間MFCよりも好評であった。しかし、Windowsへの機能追加とOWLのアップデートに時間差が生じてしまったので、OWLはシェアを失った。

Visual C++ 4.2においておよび[ActiveX](../Page/ActiveX.md "wikilink")などのインターネット関連のクラスが追加された後は、MFC自体に特に大きな変化がなく、Visual C++ 7.0 (Visual C++ .NET 2002) においてMFCとATLの一部が統合された程度にとどまっていたが、Visual C++ 2008 (Visual Studio 2008) へのサービスパック1適用時にインストールされる「MFC Feature Pack」において、MFCは大幅な進化を遂げている。具体的には、[Office](../Page/Microsoft_Office.md "wikilink") 2007風の[リボン インターフェイスを構築するための](https://ja.wikipedia.org/wiki/リボン_\(GUI\) "wikilink")"CMFCRibbon〜"で始まる名前を持つクラスや、Visual Studio 2005風のスマート ドッキング ウィンドウを実現するCDockablePaneクラスなど、100以上のクラスが追加されている。これらのクラスを利用する場合、開発者は基本的に、Feature Packインストール後にMFCアプリケーション ウィザードに追加されるリボンUIあるいはVisual Studio UIのテンプレートを選択して、自動生成されるフレームワークをベースにしてコーディングしていくことになる。ただし[.NET Frameworkによる開発とは異なり](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、[RADではなくコードベースでGUIを構築する必要があるため](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")、これらのクラスを使いこなすにはMFCプログラミングに精通していることが前提となる。なお、Windows 7 SDK (Windows SDK for Windows 7 and .NET Framework 3.5 SP1) にもリボン インターフェイスを実装するための「リボン フレームワーク」と呼ばれるAPI群が追加されているが、実質的に[COMコンポーネントを利用したAPIプログラミングであり](../Page/Component_Object_Model.md "wikilink")、さらにリボン フレームワークのコンポーネントが導入されているのは[Windows 7および](../Page/Microsoft_Windows_7.md "wikilink")[Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") SP2 Platform Update以降のOSであるため、ネイティブ（[アンマネージ](https://ja.wikipedia.org/wiki/.NET_Framework#用語 "wikilink")）のリボンUIアプリケーションの開発に関しては、MFCの選択は有力候補となり得る。

Visual C++ 2010 (Visual Studio 2010) においては、リボンUIを視覚的に編集する機能（リボン デザイナー）\[1\]がリソース エディタに追加されたほか、[Windows Vista以降のOSに実装されている](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")「タスク ダイアログ」や「再起動マネージャー」などを利用するための機能も追加されている\[2\]。高[DPI環境にも標準対応するようになった](https://ja.wikipedia.org/wiki/dpi "wikilink")（System DPI Aware）\[3\] 。また、Visual C++ 2010へのサービスパック1適用後\[4\]は、[Direct2D](https://ja.wikipedia.org/wiki/Direct2D "wikilink")\[5\]ラッパー\[6\]およびWindows Animation Manager\[7\]ラッパー\[8\]の機能（クラス ライブラリ）が追加される。

Visual C++ 2015では動的レイアウトにも対応する\[9\]など、.NET Frameworkとはまた違った方向の機能拡張が続けられている。

## 仕様

MFCが発売された時、マイクロソフトは[マクロの活用によってC](../Page/マクロ_\(コンピュータ用語\).md "wikilink")++の文法を拡張し、ウインドウメッセージ、[例外処理](../Page/例外処理.md "wikilink")、[実行時型情報](https://ja.wikipedia.org/wiki/実行時型情報 "wikilink")、クラスの動的インスタンス化などを管理していた（例外処理、実行時型情報などは当時のC++の言語仕様にも実装（コンパイラ）にも存在しなかった）。ウインドウメッセージのために構文に変化を加えたことは、不要な[仮想関数テーブル](https://ja.wikipedia.org/wiki/仮想関数テーブル "wikilink")の使用を避けることでメモリの消費量を抑える狙いがあった。さらに、構造がより具体的になり、Visual C++に付属する多様なツールがソースコード全体を解析することなく処理できるという効果もあった。メッセージ処理のマクロは、C++の仮想関数の代わりとなった。ただ、一部のマクロはコンパイラによる型チェックを無効化することがあるので、しばしばバグの原因となった。

MFCを使用することの主な利点は、Windows APIを利用したプログラム開発にオブジェクト指向プログラミングモデルを導入するという点である。もう一つは、Windowsのリソースに関連した一般的なデータ型に対するラッパーを提供するという点である。これらのラッパーを使用することで、リソース管理オブジェクトのスコープを出た時に自動的にリソースのハンドルを解放させることなどができる ([RAII](../Page/RAII.md "wikilink"))。さらに、MFCは[Model View Controllerモデルに基づいたアプリケーションを開発するための](../Page/Model_View_Controller.md "wikilink")*ドキュメント／ビュー* フレームワークを提供する。

マイクロソフトはC++標準化にあたって、多重継承について否定的な立場をとっていた。MFCもその理念に従い初期のMFCは多重継承を全く使用しておらず、オブジェクトとしての機能は基底クラスに、そして具体的な機能の実装は単純継承によって実装されている。これはオブジェクトが不要なメンバによって肥大化する事が無く、また不必要に修飾されていないので個々のクラスを理解する事が容易になっている。しかし、一部のクラスは多重継承（より近代的な実装ならばテンプレート）によって実装されるべき物も単純継承によって実装されており、これらは[統合開発環境](../Page/統合開発環境.md "wikilink")の支援なくしては扱えない難解な物になっている（後述のCViewやCDocumentもこれに含まれる）。

MFCの主な欠点は、多くのOSで利用できないという点である。[Mainsoft](https://ja.wikipedia.org/wiki/Mainsoft "wikilink")は[UNIX](../Page/UNIX.md "wikilink")で利用可能なMFCツールを開発した[1](http://www.mainsoft.com/solutions/vmw5_wp.aspx)。マイクロソフトは1990年代にMacintoshに対応したMFCを販売していたが、それ以降はMacintoshに対するVisual Studioのサポートは中止された。

また、Visual C++のC/C++ライブラリと同様に、ライブラリのバージョンごとにメモリ管理が異なるため、互いに異なるバージョンのMFCを使用したEXE-DLLプログラム間で[DLL境界を越えてMFCオブジェクト](../Page/ダイナミックリンクライブラリ.md "wikilink")・CRTオブジェクトをやりとりできないなど、バージョン間でのバイナリレベルの互換性が低くなっている\[10\]。そのため、旧バージョンのMFCを使って開発されたDLL（MFC拡張DLL）やスタティックライブラリを、新バージョンのMFCアプリケーションでそのまま利用することは基本的に不可能（その逆もまた然り）となっており、ソースコードからの再ビルドが必要となる。なお、非MFCアプリケーションや、異なるバージョンのMFCアプリケーションから、MFCを使って実装したコードを実行する場合、MFC標準DLLもしくはATL COMサーバーのプロジェクト形式を選択し、C言語関数形式のインターフェイスやCOMインターフェイスを作成してアプリケーション側に公開する必要がある。

MFCはあくまでWindows APIのラッパークラス群およびそれらを利用したフレームワークという位置付けのため、生産性の点では[Visual Basicや](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")[Visual C\#](../Page/Microsoft_Visual_C_Sharp.md "wikilink")、[Delphi](../Page/Delphi.md "wikilink")などの[RADツールに遠く及ばない](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")。また、C++言語の習得は比較的難しい部類に入るため、エンドユーザープログラミング（）の観点からも敬遠されがちである。しかし、そういったいくつかの問題点を抱えているにもかかわらず、MFCが未だ多くの企業や個人プログラマーに利用されているのは、実行速度や動作プラットフォーム、開発環境および開発言語の変更コストの問題などで旧来のネイティブコード資産を完全に[.NETに移行することが難しく](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、またWindowsアプリケーションにおいて凝った機能を実装しようとすると、Windows APIおよび[COMコンポーネントを直接操作するほうが却って楽であることが多く](../Page/Component_Object_Model.md "wikilink")、これらと親和性の高いMFCを選択せざるを得ないためである。

なお、Visual C++ .NETに搭載されている[マネージ拡張C++](https://ja.wikipedia.org/wiki/マネージ拡張C++ "wikilink")、あるいはVisual C++ 2005以降に搭載されている[C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")言語を利用することで、従来のMFCアプリケーションから.NET Frameworkのライブラリをシームレスに利用する、もしくはMFC標準DLLに実装されたMFCネイティブコードをマネージコードでラップすることで、C\#あるいはVB.NETのような.NET言語向けにクラスライブラリの形で公開する、といったハイブリッド開発・相互運用が可能となり、ネイティブコードとマネージコードの資産をともに活かすことができるようになる。しかし、マネージ拡張C++やC++/CLI言語を用いた開発はネイティブコードおよびマネージコード双方にまたがる知識が必要となるため、MFCのみを利用した場合、もしくは.NETのみを利用した場合と比べて難易度が高くなる。

## MFCの欠点に対する批判

  - CDocument, CView 等の基本的なクラスの仕様が難解である。Windowsメッセージ、コマンド、およびシェルといったWin32 APIの基本を理解していることが前提となる。
  - クラスは基本的に単一継承のみであるため、階層が深くなりがちである。また、friendクラスが多用されていることもあって直交性が低い。
  - ATLと共有する一部を除き、すべての関数\[11\]、構造体、クラス\[12\]および[列挙型](../Page/列挙型.md "wikilink")などがグローバル[名前空間](../Page/名前空間.md "wikilink")に存在し、さらに[マクロが多用されているため](../Page/マクロ_\(コンピュータ用語\).md "wikilink")、名前のコンフリクト（識別子の衝突、競合）が発生しやすく、また継承の階層構造がわかりにくい。なお、MFCシリアライズ機能を使用するクラスは、グローバル名前空間で定義しなくてはならない。
  - [実行時型情報](https://ja.wikipedia.org/wiki/実行時型情報 "wikilink")や[例外処理](../Page/例外処理.md "wikilink")機構などの一部の仕様は、独自の[マクロを使用した実装となっているため](../Page/マクロ_\(コンピュータ用語\).md "wikilink")、標準C++との統一感がない（標準C++の実行時型情報および例外処理機構との併用や共存は可能）。
  - [変数名に](../Page/変数_\(プログラミング\).md "wikilink")（16ビット時代からの）古い[システムハンガリアン記法](../Page/ハンガリアン記法.md "wikilink")\[13\] \[14\]を採用しているため、最新のコーディングスタイルに合わない。
  - Win32 API自体が拡張を繰り返した結果、APIとしての統一性に欠けるものとなったため、その薄いでしかないMFCでは隠蔽しきれない。
  - トレース用のDEBUG_NEW[マクロによるnewキーワードの置換など](../Page/マクロ_\(コンピュータ用語\).md "wikilink")、標準規格違反を犯している\[15\]。

## バージョン

MFCのバージョンは、バージョン6.0以降はその対応するVisual C++製品のバージョン番号と同じとなっている。なお、Visual C++コンパイラ自体は `_MSC_VER` という予約マクロによりバージョン番号が定義されるが、MFCでは `_MFC_VER` という予約マクロによりバージョン番号が定義される。これらはそれぞれ異なる内部数値になっているので、バージョンに応じてユーザープログラムコードを分岐したい場合は注意が必要となる。

Visual C++に同梱されるMFCのバージョン一覧を下記に示す。

| VC製品バージョン            | MFCバージョン              | _MFC_VER | 備考                                                                           |
| -------------------- | --------------------- | ---------- | ---------------------------------------------------------------------------- |
| Microsoft C/C++ 7.0  | MFC 1.0               | 0x0100     |                                                                              |
| Visual C++ 1.0       | MFC 2.0               | 0x0200     |                                                                              |
| Visual C++ 1.5       | MFC 2.5               | 0x0250     |                                                                              |
| Visual C++ 2.0       | MFC 3.0               | 0x0300     |                                                                              |
| Visual C++ 2.1       | MFC 3.1               | 0x0310     |                                                                              |
| Visual C++ 2.2       | MFC 3.2               | 0x0320     |                                                                              |
| Visual C++ 4.0       | MFC 4.0               | 0x0400     |                                                                              |
| Visual C++ 4.1       | MFC 4.1               | 0x0410     |                                                                              |
| Visual C++ 4.2       | MFC 4.2               | 0x0420     |                                                                              |
| Visual C++ 5.0       | MFC 4.21 (mfc42.dll)  | 0x0421     |                                                                              |
| Visual C++ 6.0       | MFC 6.0 (mfc42.dll)   | 0x0600     | Windows XP以降のOSに標準インストールされている。                                               |
| Visual C++ .NET 2002 | MFC 7.0 (mfc70.dll)   | 0x0700     | 通常アプリケーションの添付のみ。MS07-012\[16\]等セキュリティ問題も見つかっているが。                            |
| Visual C++ .NET 2003 | MFC 7.1 (mfc71.dll)   | 0x0710     | 通常アプリケーションの添付のみ。MS07-012等セキュリティ問題も見つかっているが。                                  |
| Visual C++ 2005      | MFC 8.0 (mfc80.dll)   | 0x0800     | サービスパックおよびセキュリティパッチの適用により、複数のバージョンがインストールされる。                                |
| Visual C++ 2008      | MFC 9.0 (mfc90.dll)   | 0x0900     | サービスパックおよびセキュリティパッチの適用により、複数のバージョンがインストールされる。                                |
| Visual C++ 2010      | MFC 10.0 (mfc100.dll) | 0x0A00     |                                                                              |
| Visual C++ 2012      | MFC 11.0 (mfc110.dll) | 0x0B00     |                                                                              |
| Visual C++ 2013      | MFC 12.0 (mfc120.dll) | 0x0C00     |                                                                              |
| Visual C++ 2015      | MFC 14.0 (mfc140.dll) | 0x0E00     |                                                                              |
| Visual C++ 2017      | MFC 14.0 (mfc140.dll) | 0x0E00     | Visual C++コンパイラの内部バージョン番号は14.1だが、CRTライブラリ同様にMFCの内部バージョン番号は14.0のまま据え置きとなっている。 |

Visual C++とMFCのバージョンの履歴

Visual C++ .NET 2003までは、C/C++ (CRT) およびMFCのランタイム ライブラリは開発環境のインストールとともにWindowsのシステム フォルダ（[%WinDir%](../Page/環境変数.md "wikilink")\\System32あるいは%WinDir%\\[SysWOW64](../Page/WOW64.md "wikilink")）にインストールされるようになっていた\[17\]が、Windows XP以降の場合、Visual C++ 2005および2008は[DLL地獄](../Page/DLL地獄.md "wikilink")を解消する目的で、%WinDir%\\WinSxS 以下の、amd64_microsoft.vc80.mfc_\*、ia64_microsoft.vc80.mfc_\*、x86_microsoft.vc80.mfc_\*などのフォルダに[Side-by-Sideアセンブリとしてインストールされるようになっている](https://ja.wikipedia.org/wiki/分離アプリケーションとSide-by-Sideアセンブリ "wikilink")。これにより、サービスパックを適用したランタイムをインストールしたり、ランタイムに[セキュリティパッチを適用したりすると](../Page/Microsoft_Update.md "wikilink")、旧バージョンのランタイムは上書きされず、新しいバージョンのランタイムが追加インストールされるため、複数の異なるバージョンが共存できる。なお、Visual C++ .NET 2003までは、MFCを使用するアプリケーションの実行プログラムの存在するフォルダにMFCランタイムをコピーして再配布すれば、MFCランタイムがインストールされていないエンドユーザー環境でも実行できていたが、Visual C++ 2005および2008ではこのようなSide-by-Sideアセンブリの形態をとるようになっているため、単純にコピーを添付するだけでは実行することができない。**Visual C++ 2005および2008を使用して作成されたMFCアプリケーションをエンドユーザー環境で実行する**ためには、下記の方法が存在する\[18\] \[19\]。

1.  エンドユーザー環境にVisual C++のランタイムパッケージを別途インストールする。
2.  アプリケーションをビルドする際、CRT/MFCをスタティックリンク（[静的リンク](https://ja.wikipedia.org/wiki/静的リンク "wikilink")）する。
3.  [アプリケーションマニフェストを使用してCRT](https://ja.wikipedia.org/wiki/分離アプリケーションとSide-by-Sideアセンブリ#マニフェスト "wikilink")/MFCランタイムを[プライベートアセンブリ化する](https://ja.wikipedia.org/wiki/分離アプリケーションとSide-by-Sideアセンブリ#プライベートアセンブリ "wikilink")（[Windows XP以降](../Page/Microsoft_Windows_XP.md "wikilink")）。

1番目の方法は、エンドユーザーの負担が増えるものの、セキュリティ面で最も安全な方法である。インストールされたランタイムDLL群は、Microsoft Updateなどによって提供されるセキュリティパッチの適用対象となる（ただし前述の通り、DLL自体はセキュリティパッチによって書き換えられるわけではない）。なお、エンドユーザーランタイムの[インストーラ](https://ja.wikipedia.org/wiki/インストーラ "wikilink")はマイクロソフトから無償提供されており、開発者による再配布も行なえるようになっている。 2番目の方法は、エンドユーザーの手間を減らせるが、アプリケーションビルド時のリンク時間が増加し、実行プログラムのファイルサイズが肥大化するという欠点がある\[20\]。また、セキュリティパッチ適用の対象外となる（ちなみに/clrオプションを有効にして.NETハイブリッドアプリケーションを作成する場合はそもそもCRT/MFCライブラリをスタティックリンクすることはできない）。 3番目の方法は、アプリケーションにMFCランタイムを同梱するための方法であり、スタティックリンクする場合と同様にエンドユーザーの手間を減らせる。

なお、Visual C++ 2010以降では、CRTおよびMFCランタイムのSide-by-Side配置方式は廃止され、再びVisual C++.NET 2003以前と同じようにWindowsシステム フォルダにインストールされるようになっている。サービスパックおよびセキュリティパッチが適用されると、システム フォルダ内のDLLファイル（mfc100.dllなど）が書き換えられる。

## MBCSとUnicode

MFCではアプリケーションのコンパイル＆ビルド時に設定・定義するMBCS/UNICODEシンボル情報に合わせて、それぞれMBCS版MFCライブラリと[Unicode](../Page/Unicode.md "wikilink")版MFCライブラリが暗黙的にリンクされて使用される。MBCS版とはANSIマルチバイト文字セット (Multibyte Character Set) \[21\]版のことで、例えば日本語版の場合[Shift_JIS](../Page/Shift_JIS.md "wikilink")（厳密には[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")[コードページ](../Page/コードページ.md "wikilink")932）に相当する。データの格納にはchar型およびその配列が主に使われる。Unicode版とはWindows用のUnicode対応版のことで、[UTF-16](../Page/UTF-16.md "wikilink")LEに相当する。データの格納にはwchar_t型およびその配列が主に使われる。WindowsではOSの内部文字コードがUTF-16LEのため、一般的にはアプリケーションの内部文字コードとして[UTF-8](../Page/UTF-8.md "wikilink")マルチバイトや[UTF-32](../Page/UTF-32.md "wikilink")が使われることは少ない。

MFCアプリケーション開発において、MBCSおよびUnicode両方のバージョンで動作するコードを記述する場合、一般的にはMBCS, _MBCS, UNICODE, _UNICODEなどのシンボル定義状況に応じてコンパイルするコードを分岐させることで対処する。MFC/ATL、標準C/C++ランタイムライブラリ (CRT) およびWin32 APIにはMBCS/Unicode両対応を容易にするためのマクロ\[22\]や、TCHAR, LPTSTR, LPCTSTR型およびCStringクラスといったヘルパーが用意されている。

Unicode文字列に対応したWindows OSは[Windows 2000およびWindows](../Page/Microsoft_Windows_2000.md "wikilink") XPからで[2](http://www.jagat.or.jp/story_memo_view.asp?StoryID=8154)、[Windows 9x系のOSではもともとUnicode非対応であり](../Page/Windows_9x系.md "wikilink")、歴史的にWindowsアプリケーション開発言語としてのC/C++は長らくMBCSを使用してきたが、国際化対応（Unicode対応）が求められるという時代の流れから、まずVisual Studio 2005ではプロジェクトの既定の設定がUnicodeとなり、さらにVisual Studio 2013からは、MBCS版MFC/ATLライブラリは非推奨となりインストーラに同梱されなくなった（Unicode版MFC/ATLライブラリのみ同梱）。なお、ライブラリのバイナリがIDEにバンドルされなくなっただけで、Visual Studio 2013向けMBCS版MFCライブラリのDLLバージョンはマイクロソフト社の公式サイトからダウンロードすることで取得できる。一方、Visual C++ 再頒布可能パッケージ（エンドユーザー向けリテールランタイム）には、2013以降も、引き続きMBCS版MFCランタイムDLLが含まれ、MBCS版MFCランタイムを顧客に再頒布するための追加の手順は必要ない。

なお、[Windows 8](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")/[Windows RTで導入された](https://ja.wikipedia.org/wiki/Microsoft_Windows_RT "wikilink")[Windowsストア](https://ja.wikipedia.org/wiki/Windowsストア "wikilink")アプリ（のち の[Windows 10における](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")[ユニバーサルWindowsプラットフォーム](https://ja.wikipedia.org/wiki/ユニバーサルWindowsプラットフォーム "wikilink")アプリ）は、[C\#などの](../Page/C_Sharp.md "wikilink").NET言語による開発のほか、というネイティブ拡張言語による開発も可能となっているが、ATLの一部は使用できるもののMFCは使用できない。また、Windowsストアアプリではマルチバイト文字・文字列のAPIが使えなくなっており、ASCIIもしくはUnicode文字・文字列のみが使用できる\[23\]。

## 脚注

## 関連項目

  - [Microsoft Visual C++](../Page/Microsoft_Visual_C++.md "wikilink")
  - [Windows API](../Page/Windows_API.md "wikilink")
  - [Active Template Library](../Page/Active_Template_Library.md "wikilink")
  - [Windows Template Library](../Page/Windows_Template_Library.md "wikilink")

## 外部リンク

  - [MFC リファレンス](http://msdn.microsoft.com/ja-jp/library/d06h2x6e.aspx)
  - [The latest supported Visual C++ downloads](https://support.microsoft.com/en-us/kb/2977003)

### 非公式

  - [猫でもわかるプログラミング MFC編](http://www.kumei.ne.jp/c_lang/indexmfc.html)
  - [Visual C++ 入門 (MFC)](http://mail2.nara-edu.ac.jp/~asait/visual_cpp/intro_cpp.htm)
  - [MFCトピック集](http://www.athomejp.com/goldfish/mfc/)
  - [VC++,MFCでのプログラミングでのTips集](http://www.crimson-systems.com/tips/index.html)
  - [VisualC++超入門](http://www006.upp.so-net.ne.jp/candynar/visualc/visualc_begin.htm)

[Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/Category:グラフィカルユーザインタフェース "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink")

1.  [リボン デザイナー (MFC)](http://msdn.microsoft.com/ja-jp/library/ee354408.aspx)
2.  [Visual C++ - Visual Studio 2010 の C++ と MFC での新機能の詳細](http://msdn.microsoft.com/ja-jp/magazine/ee336130.aspx)
3.  [MFC applications now default to being DPI-aware | Visual C++ Team Blog](https://web.archive.org/web/20190125192645/https://blogs.msdn.microsoft.com/vcblog/2010/03/11/mfc-applications-now-default-to-being-dpi-aware/), [Internet Archive](https://ja.wikipedia.org/wiki/Internet_Archive "wikilink")
4.  \[<https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/gg482719(v=vs.100>) MFC Additions for Visual Studio 2010 SP1 | Microsoft Docs\]
5.  [Direct2D (Windows)](http://msdn.microsoft.com/ja-jp/library/dd370990.aspx)
6.  [チュートリアル: MFC プロジェクトへの D2D オブジェクトの追加](https://msdn.microsoft.com/ja-jp/library/gg482848.aspx)
7.  [Windows Animation Manager (Windows)](http://msdn.microsoft.com/ja-jp/library/dd371981.aspx)
8.  [チュートリアル: MFC プロジェクトへのアニメーションの追加](https://msdn.microsoft.com/ja-jp/library/gg466500.aspx)
9.  [動的レイアウト](https://msdn.microsoft.com/ja-jp/library/mt270148.aspx)
10. [DLL の境界を越えて CRT オブジェクトを渡す場合に発生する可能性のあるエラー](https://msdn.microsoft.com/ja-jp/library/ms235460.aspx)
11. グローバル関数は、名前に通例 *Afx* プレフィックスが付けられているが、例外もある。[MFC Macros and Globals](https://msdn.microsoft.com/en-us/library/f2dch7fb.aspx)
12. クラス名は、名前に通例 *C* プレフィックスが付けられている。
13. [Making Wrong Code Look Wrong - Joel on Software](http://www.joelonsoftware.com/articles/Wrong.html)
14. [間違ったコードは間違って見えるようにする - The Joel on Software Translation Project](http://local.joelonsoftware.com/wiki/%E9%96%93%E9%81%95%E3%81%A3%E3%81%9F%E3%82%B3%E3%83%BC%E3%83%89%E3%81%AF%E9%96%93%E9%81%95%E3%81%A3%E3%81%A6%E8%A6%8B%E3%81%88%E3%82%8B%E3%82%88%E3%81%86%E3%81%AB%E3%81%99%E3%82%8B)
15. \[<https://web.archive.org/web/20140301090452/http://msdn.microsoft.com:80/ja-jp/library/cc440188(v=vs.71>).aspx Deep C++, 予約名 - MSDN\] / [Internet Archive](https://ja.wikipedia.org/wiki/Internet_Archive "wikilink")
16. [マイクロソフト セキュリティ情報 MS07-012 - 重要](https://technet.microsoft.com/library/security/ms07-012)
17. [Redistribution of the shared C runtime component in Visual C++](https://support.microsoft.com/en-us/kb/326922)
18. [Visual C++ - 配置例 (MSDN)](http://msdn.microsoft.com/ja-jp/library/ms235285.aspx)
19. [グローバルに提供される side-by-side アセンブリを適用しないアプリケーションは、マイクロソフトのソフトウェア更新プログラムで修正される問題に対して脆弱になる可能性がある](http://support.microsoft.com/kb/835322/ja-jp) マイクロソフト サポート オンライン
20. [テクニカル ノート 33: MFC の DLL バージョン (MSDN)](http://msdn.microsoft.com/ja-jp/library/hw85e4bb.aspx)
21. [Unicode とマルチバイト文字セット (MBCS: Multibyte Character Set) のサポート](https://msdn.microsoft.com/ja-jp/library/ey142t48.aspx)
22. CreateFileA()/CreateFileW() APIに対応するCreateFileマクロや、MBCS/Unicode文字列リテラルを切り替えるTEXT(), _T()マクロなど。
23. [Windows Store Apps, the Windows Runtime, and the C Run-Time](http://msdn.microsoft.com/en-us/Library/hh972425.aspx)