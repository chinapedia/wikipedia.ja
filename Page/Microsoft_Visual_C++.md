> この記事は[Microsoft Visual C++](https://ja.wikipedia.org/wiki/Microsoft_Visual_C++)から翻訳されています。


**Visual C++** （マイクロソフト ビジュアル シープラスプラス；マイクロソフト ヴィジュアル シープラスプラス）とは[マイクロソフト](../Page/マイクロソフト.md "wikilink")製の[C](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")、[C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")用[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) であり、[コンパイラ](../Page/コンパイラ.md "wikilink")や[デバッガ](../Page/デバッガ.md "wikilink")を含む。通称**VC**あるいは**VC++**、**MSVC**など。前身は**Microsoft C/C++**などがある。

## 概要

事実上の[Windowsの標準開発環境であり](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、その最適化性能は非常に高い。さらに、Visual C++ 7.1 (.NET 2003) からは標準C++規格への準拠度も高いことで知られている。同じバージョンでもいくつかのエディションが存在し、以前は上位エディションしか最適化をサポートしていなかったが、Visual C++ 2005から基本的な最適化は全てのエディションにおいて行えるようになった。（2005で導入されたプロファイリングに基づく最適化 (PGO) は上位エディションのみでサポートされている）

Visual C++ 2005以降は[Visual Basicや](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")[Visual C\#などの他の開発言語と統合された](../Page/Microsoft_Visual_C_Sharp.md "wikilink")[Visual Studioのパッケージとして販売されている](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")。Visual C++ .NET 2003までは言語別製品として販売されていたが、2005以降は行なわれていない。販売されているVisual Studioパッケージから機能を制限した無料版のVisual C++ Express Editionが入手できる。

"Visual"という名称が付けられているが、[Visual Basicなどと違って](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")[RADではなく](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")、基本的には[Windows SDK](../Page/Microsoft_Windows_SDK.md "wikilink") ([Windows API](../Page/Windows_API.md "wikilink")) や[MFCを使用してコードベースのプログラムを作成することになる](../Page/Microsoft_Foundation_Class.md "wikilink")（ただしリソースエディタを用いることで、ダイアログウィンドウやメニューの外観デザインのみを視覚的に行うことは以前からできた）。MFCはC++専用クラスライブラリであり、[アプリケーションフレームワーク](../Page/アプリケーションフレームワーク.md "wikilink")の役目も担っているが、基本的にWindows APIの薄い[ラッパーでしかないため](https://ja.wikipedia.org/wiki/ラッパークラス "wikilink")、生産性の点で[Visual Basicや](../Page/Visual_Basic.md "wikilink")[Delphi](../Page/Delphi.md "wikilink")のようなRADに及ばない。しかし、Visual C++ 7.0 (.NET 2002) 以降は、後述するマネージ拡張C++あるいはC++/CLIを使用して[Windows Formsアプリケーション](../Page/Windows_Forms.md "wikilink")（もしくはWindows Formsコンポーネント）を開発する場合に限って、フォームエディタを始めとした[Visual C\#や](../Page/Microsoft_Visual_C_Sharp.md "wikilink")[VB.NETのようなRAD環境を使用できる](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink")。また、Visual C++ 11.0 (2012) 以降は、後述するC++/CXを使用して[Windowsストア](https://ja.wikipedia.org/wiki/Windowsストア "wikilink")アプリを開発する場合、[XAMLエディタを始めとしたRAD環境を使用できる](../Page/Extensible_Application_Markup_Language.md "wikilink")。

また、旧来のWin32/MFCアプリケーション（もしくは[DLL](../Page/ダイナミックリンクライブラリ.md "wikilink")）に[共通言語基盤](../Page/共通言語基盤.md "wikilink") (CLI) のサポートを追加することで、[.NET Frameworkのクラスライブラリを併用するハイブリッド開発も行なえる](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。これにより、例えばVisual C\#/VB.NETで.NET基本クラスライブラリを使って開発したロジックライブラリや、Windows Forms/[WPFを使って開発した](../Page/Windows_Presentation_Foundation.md "wikilink")[GUI部品を](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、Win32/MFCアプリケーションで利用する、という相互運用が（制約付きではあるが）可能となっている。

Visual C++ 8.0 (2005) 以降は[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")命令の生成に対応している。付属するコンパイラには、コンパイラが動作する環境と同じネイティブコードを生成するものと、32bit (x86) 環境で動作して 64bit ([x64](https://ja.wikipedia.org/wiki/x64 "wikilink")または[IA-64](../Page/IA-64.md "wikilink")) ネイティブコードを出力するもの (クロスコンパイラ) がある。32ビット ([x86](https://ja.wikipedia.org/wiki/x86 "wikilink")) 環境上であっても[クロスコンパイル](https://ja.wikipedia.org/wiki/クロスコンパイル "wikilink")することができる。Visual C++ 11.0 (2012) 以降は[ARMプロセッサ向けのコード生成にも対応している](../Page/ARMアーキテクチャ.md "wikilink")。

Windows用マルチメディアコンポーネントである[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")を使用してアプリケーション開発を行う場合に必要となるヘッダーファイルなどは[Windows SDKに含まれているが](https://ja.wikipedia.org/wiki/Windows_SDK "wikilink")、DirectX API は主にVisual C++シリーズで利用されることを前提に開発されているため、親和性が非常に高い。なお、Windows SDK 7.1までは最新のDirectX APIや各種ツール類を使用する場合は単独のDirectX SDK（単独の最終バージョンはJune 2010となっている）を別途インストールする必要があったが、Windows SDK 8.0以降は（D3DXライブラリなどの一部を除いて）最新のヘッダーおよびインポートライブラリファイルや各種ツール類がWindows SDKに含まれるようになった。

Visual Studio 2015では、[Android](../Page/Android.md "wikilink")および[iOS向けのモバイルアプリケーションを開発できるようになった](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")。ビルドシステムとして[MSBuild](https://ja.wikipedia.org/wiki/MSBuild "wikilink")が使われるが、コンパイラはMSVCではなく[Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")が使われる。

## 言語

Visual C++のコンパイラは、C, C++, C++/CLI, C++/CXのソースコードを入力に受け付ける。

C言語規格に関しては、Visual C++ 9.0 (2008) SP1の時点では[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink") C89 ([ISO](https://ja.wikipedia.org/wiki/ISO "wikilink") C90, ISO/IEC 9899:1990) 対応\[1\]であり、[C99](../Page/C99.md "wikilink")や[C11には対応していない](https://ja.wikipedia.org/wiki/C11_\(C言語\) "wikilink")（`//`で始まるコメントやlong long intなどは言語拡張としてサポートされている）。Visual C++ 2013では、全てではないが[C99](../Page/C99.md "wikilink")の関数の大半を追加した\[2\]。

C++言語規格に関しては、Visual C++ 9.0 (2008) SP1の時点でC++98 (ISO/IEC 14882:1998) 規格に対応している\[3\]。Visual C++ 10.0 (2010) では、auto、decltype、[ラムダ式](https://ja.wikipedia.org/wiki/ラムダ式 "wikilink")、[rvalue reference（右辺値参照）](https://ja.wikipedia.org/wiki/C++11#右辺値参照とムーブコンストラクタ "wikilink")、static_assert、nullptrなど、[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")規格で追加された機能を一部規格制定に先行して実装した\[4\]。Visual C++ 11.0 (2012) では、Strongly typed enums、Forward declared enums、Standard-layout and trivial types、Range-based for-loop などのC++11規格を実装した\[5\]。Visual C++ 12.0 (2013) では、Initializer lists、Alias templates、Delegating constructors、Raw string literals などのC++11規格を追加実装した\[6\]。Visual C++ 14.0 (2015) では、constexpr、Unicode string literalsなどのC++11規格を追加実装し、またBinary literalsなどの[C++14](https://ja.wikipedia.org/wiki/C++14 "wikilink")規格を一部実装した\[7\]。Visual Studio 2017 15.0のVisual C++ 14.1 (2017) では、C++14規格の追加機能をすべてサポートしたが、C++11規格の一部がサポートされていない\[8\]。Visual Studio 2017 15.7において[C++17](https://ja.wikipedia.org/wiki/C++17 "wikilink")規格の追加機能をすべてサポートしたが、C++11規格のうちC99プリプロセッサ ([N1653](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2004/n1653.htm)) がサポートされていない\[9\]\[10\]\[11\]。また、`__cplusplus`の定義値は既定で`199711L`となっているが、コンパイルオプション`/Zc:__cplusplus`を指定することで、C++言語標準モード設定に応じて`201402L`などに変化する\[12\]。

### 主なコンパイラの拡張

  - [インラインアセンブラ](https://ja.wikipedia.org/wiki/インラインアセンブラ "wikilink")
    _asmや__asmキーワードによる記述。C++の標準規格で定められているasm文には対応していない。x64/IA64では使用できず、別途アセンブラで記述するか組込関数で代替する。
  - コンパイラCOM対応
    \#importディレクティブ及び追加のクラス・関数など。
  - 属性
    マイクロソフトインターフェイス定義言語[MIDLの属性を直接C](https://ja.wikipedia.org/wiki/インタフェース定義言語 "wikilink")++ソースコードに記述する機能。なお、マネージ拡張C++、C++/CLI、およびC++/CXの属性も同様の構文を使用する。
  - [OpenMP](../Page/OpenMP.md "wikilink")
    Visual C++ 2005からOpen MP 2.0に対応している\[13\]。2010まではProfessional以上のエディションでのみ使用可能となっていたが\[14\]\[15\]\[16\]、2012ではExpressを含む全エディションで使用が可能となった\[17\]。
  - ネイティブC++でのC++/CLI構文の使用
    for each\[18\]及びoverride, abstract, sealed\[19\]。このうち、overrideは[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")のoverrideと同様の構文である。また、sealedは[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")のfinalキーワードに相当する（sealed自体はさらにもとを辿ればマイクロソフト発のプログラム言語[C\#からの由来である](../Page/C_Sharp.md "wikilink")）。Visual C++ 2012では、sealed、finalのうちどちらでも使うことができるが、標準C++クラスにはfinalを、C++/CXのrefクラス（Windowsランタイムクラス）にはsealedを使うことが推奨されている\[20\]。
  - Type Traits対応
    __is_podキーワードなど\[21\]。
  - .NET/WinRT対応
    後述する。
  - その他
    __declspec、[呼出規約](https://ja.wikipedia.org/wiki/呼出規約 "wikilink")の指定、[プロパティ](../Page/プロパティ.md "wikilink")構文（__declspec(property)）、[構造化例外処理](https://ja.wikipedia.org/wiki/構造化例外処理 "wikilink")、\#pragmaディレクティブ、SAL注釈\[22\]など。

### 主なライブラリの拡張

  - 追加のCRT関数
    MS-DOS時代に由来するもの、[POSIX](../Page/POSIX.md "wikilink")互換のもの、セキュリティ強化のためのものなど

  - コンパイラ組込関数
    [MMX](../Page/MMX.md "wikilink"), [SSE](../Page/ストリーミングSIMD拡張命令.md "wikilink"), [SSE2やその他CPU命令に対応するもの](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE2 "wikilink")

  - stdext名前空間
    hash_map, hash_setなど

  - msclr名前空間
    C++マネージ拡張およびC++/CLI用の追加ライブラリ \[23\]

  - [STL/CLR](https://ja.wikipedia.org/wiki/STL/CLR "wikilink")
    C++/CLIでの[STL風のライブラリ](../Page/Standard_Template_Library.md "wikilink") \[24\]

  - 同時実行ランタイム (Concurrency Runtime)

    などから構成される、C++11ベースの並列処理ライブラリ \[25\]

  - [C++ AMP](https://ja.wikipedia.org/wiki/C++_AMP "wikilink")
    [GPU](https://ja.wikipedia.org/wiki/GPU "wikilink")などのアクセラレータを使った並列処理ライブラリ（言語拡張を含む）\[26\]

特に、Visual C++ 2005では[バッファオーバーフロー](https://ja.wikipedia.org/wiki/バッファオーバーフロー "wikilink")や[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")での安全性の向上のため、大幅なライブラリの拡張が行われた\[27\]\[28\]。Cの関数にはstrcpyに対してstrcpy_sのように末尾に_sを追加した名称のものが該当し、その大半はISO Cの標準化委員会へTR 24731として提案されている。また、C++でも_sを付けたメンバ関数の追加（std::basic_istream::readに対して_Read_sのように）や範囲チェック付イテレータ\[29\]などの追加が行われている。

なお、Visual C++ 2008にService Pack 1 (SP1) を適用すると、[C++0x](https://ja.wikipedia.org/wiki/C++0x "wikilink") [TR1対応ライブラリや](https://ja.wikipedia.org/wiki/Technical_Report_1 "wikilink")、MFCでのVisual Studio風スマートドッキングウィンドウおよび[Office](../Page/Microsoft_Office.md "wikilink") 2007風[リボンインターフェイス作成のための拡張パッケージ](https://ja.wikipedia.org/wiki/リボン_\(GUI\) "wikilink")（MFC Feature Pack）が追加される\[30\]。また、Visual C++ 2010にSP1を適用すると、[Direct2D](https://ja.wikipedia.org/wiki/Direct2D "wikilink")やWindows Animation ManagerのMFC用ラッパークラスが追加される\[31\]。

### マネージ拡張C++

**マネージ拡張C++** (**Managed Extensions for C++**、**Managed C++**) は[.NET Frameworkに対応したアプリケーションを作成するため](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、C++を共通言語仕様[CLSに準拠させるために独自の拡張を施したものであり](https://ja.wikipedia.org/wiki/共通言語仕様 "wikilink")\[32\]、Visual C++ .NET 2002以降に搭載されている。これに対し従来のC++をマネージ拡張C++と区別する際には**ネイティブC++** (もしくは**アンマネージC++**) と呼ぶ\[33\]。1つのアプリケーション内にマネージ拡張C++とネイティブC++のコードを混在\[34\]させることも可能であり、従来のC++で書かれたコードを徐々に.NETへ移行したり、あるいは他の.NET言語からC++で作られたライブラリを使用したり、C++コードから.NET Frameworkのクラスライブラリを活用するなどといったこと（相互運用）を可能にしている（[グルー言語](../Page/グルー言語.md "wikilink")）。後継となるC++/CLIの登場により、マネージ拡張C++の使用は推奨されなくなっている\[35\]。Visual C++ 2005-2013では、非推奨ではあるが互換性維持のため従来のマネージ拡張C++のソースコードもコンパイルオプション「/clr:oldSyntax」を指定することでコンパイルできる\[36\]が、Visual C++ 2015で廃止された。

### C++/CLI

C++/CLIは（文法に不明瞭な部分のあった）マネージ拡張C++に代わる、[CLSを満たすC](https://ja.wikipedia.org/wiki/共通言語仕様 "wikilink")++を基にしたプログラミング言語であり、Visual C++ 2005以降に搭載されている。なおC++/CLI環境では、従来のC++は**アンマネージ**ではなく**ネイティブ**と形容される。

### C++/CX

C++/CX (component extensions) は、Windowsストアアプリ ([UWPアプリ](https://ja.wikipedia.org/wiki/ユニバーサルWindowsプラットフォーム "wikilink")) で使用される[Windowsランタイム](https://ja.wikipedia.org/wiki/Windowsランタイム "wikilink") (WinRT) ライブラリを効率よく利用するために、C++11規格をベースとして拡張されたプログラミング言語であり、Visual C++ 2012以降に搭載されている。なお、言語構文は前述のC++/CLIとよく似ているが、C++/CXはC++/CLIとは違ってマネージ言語ではなく、ネイティブ拡張である。そのため、従来のネイティブC/C++用コードやCRTライブラリはほぼそのまま利用できるが、.NET Frameworkを直接扱うことはできない。また、C++/CLIとは同一ソースコード内に共存できない。Windowsランタイムコンポーネント (.winmd) を通じてC\#やVB.NETと相互運用することができる。

### C++/WinRT

Visual Studio 2015 Update 3以降では、C++/CX言語拡張を使わずに、と呼ばれる拡張ライブラリを用いてUWPアプリを開発することも可能となっている\[37\]。C++/WinRTは[C++17](https://ja.wikipedia.org/wiki/C++17 "wikilink")準拠コンパイラを必要とする\[38\]。

### その他の機能・特徴

32ビット/64ビット向けのVisual C++では、C/C++のlong double型は互換性のためだけに残されており、80ビットの[拡張倍精度や](../Page/IEEE_754.md "wikilink")128ビットの四倍精度をサポートしない\[39\]。

Visual C++ 2005以降は/archコンパイルオプションによって、コンパイラ（オプティマイザ）は必要に応じて浮動小数演算にFPUでなく[SSE](../Page/ストリーミングSIMD拡張命令.md "wikilink")/SSE2を使ったコードを出力できるようになるが、x64のようにすべての浮動小数演算命令がSSE2になるとは限らない\[40\]。また、Visual C++ 2010以降は[AVX](https://ja.wikipedia.org/wiki/AVX "wikilink")命令の使用もサポートしている。Visual C++ 2013 Update 2以降はAVX2命令の使用もサポートしている\[41\]。

## 無料版

Visual C++はエディションによってサポートする機能に違いがあるが、プログラミング初心者やアップグレード検討者向けに、Windows用クラスライブラリなどが付属しない無料版がマイクロソフトによって公開されている。無料版といえど、バージョンアップのたびに標準サポートされる機能が追加されており、VC 2005以降ではIDEの[Intellisenseやデバッガなどの基本機能はStandardエディション以上の有料版と変わらず](../Page/インテリセンス.md "wikilink")、簡単なアプリケーションやライブラリを作成するには必要十分といえる。なおExpressエディションの提供はバージョン2013までとなり、以降はCommunityエディションに統合される予定\[42\]だったが、その後撤回され、Visual Studio 2015においてもExpressエディションが提供されることになった\[43\]。

  - Visual C++ ToolKit 2003
    [2003年](../Page/2003年.md "wikilink")にプロフェッショナル版と同等の最適化機能のある[コンパイラ](../Page/コンパイラ.md "wikilink")（IDEではない）が無料で提供された。ただし、それ以前から.NET Framework SDKにスタンダード版相当のコンパイラ（最適化機能無し）が付属していた。なお、後述するVisual C++ 2005 Express Editionの公開に伴って、現在はこちらの公開は終了している。

  - Visual C++ 2005 Express Edition
    [2005年](../Page/2005年.md "wikilink")12月からIDEが付いて無料で公開され、[2009年](../Page/2009年.md "wikilink")3月31日に配布を終了した。マイクロソフトがIDE製品の正式版を無料で公開したのはeMbedded Visual Toolsに続いてこれが2作目である。なお、[MFCと](../Page/Microsoft_Foundation_Class.md "wikilink")[ATLは付属していない](../Page/Active_Template_Library.md "wikilink")。また、[Windows APIを用いたプログラムを作成するには別途](../Page/Windows_API.md "wikilink")[Windows SDKをインストールする必要がある](../Page/Microsoft_Windows_SDK.md "wikilink")。

  - Visual C++ 2008 Express Edition
    [2007年](../Page/2007年.md "wikilink")[12月18日](../Page/12月18日.md "wikilink")公開。ATLやMFCが付属しない点はVisual C++ 2005 Express Editionと同じであるが、Windows SDKが標準で同梱されるようになり、Win32アプリケーションの開発に必要なWindows SDKを別途用意する必要がなくなった。

  - Microsoft Visual C++ Compiler for Python 2.7
    Windows版[Python](../Page/Python.md "wikilink")の拡張モジュールのバイナリパッケージはPythonのバージョンとCランライムライブラリのバージョンに強い依存関係があり、それに対応するために配布されている。VC++ 2008のコンパイラに相当し、IDEは付属しない。

  - Visual C++ 2010 Express
    [2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[4月28日](../Page/4月28日.md "wikilink")公開。Visual C++ ソリューションおよびプロジェクトがXMLベースのMSBuildを使用してビルドするようになり、他のVisual Studio言語で使用されるビルドシステムと同じになった。

  - Visual Studio Express 2012 for Windows 8
    Visual Studio Express 2012 for Windows Desktop
    [2012年](../Page/2012年.md "wikilink")[9月12日](../Page/9月12日.md "wikilink")公開。今バージョンではVisual C++単独の製品は無くなり[C\#](../Page/Microsoft_Visual_C_Sharp.md "wikilink")、[VB.NETと共にインストールされる](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink")。

  - Visual Studio Express 2013 for Windows
    Visual Studio Express 2013 for Windows Desktop
    [2013年](../Page/2013年.md "wikilink")[10月17日](../Page/10月17日.md "wikilink")公開。

  - Visual Studio Community 2013
    [2014年](../Page/2014年.md "wikilink")[11月13日](../Page/11月13日.md "wikilink")公開\[44\]。Expressエディションと比較して利用規約は厳しくなっているが、機能的にはProfessional版と同等。これまで有償版でしか使えなかったMFC、ATLも付属する。

  - Visual Studio Express 2015 for Windows
    Visual Studio Express 2015 for Desktop
    Visual Studio Community 2015
    [2015年](../Page/2015年.md "wikilink")[7月20日](../Page/7月20日.md "wikilink")公開\[45\]。

  - Visual C++ Build Tools 2015
    VC++ 2015のコンパイラに相当する。IDEは付属しないがATLとMFCが付属している。

  - Visual Studio Community 2017
    Visual C++ Build Tools 2017
    Visual Studio Express 2017 for Windows Desktop
    Build Tools for Visual Studio 2019

ほかにも、バージョン7.1までの [Windows SDK](../Page/Microsoft_Windows_SDK.md "wikilink") (旧Platform SDK) とバージョン7.1までの[Windows Driver KitにもVisual](../Page/Windows_Driver_Kit.md "wikilink") C++コンパイラが付属していた。 またバージョン10 1511のWindows Driver KitからはEnterprise Windows Driver Kitと呼ばれるコンパイラ等が付属するバージョンのWDKの配布が再開された。

Visual C++ Build Toolsは、ビルドサーバーや継続的インテグレーション (CI) 等、GUIを使用せずバッチ処理的にビルドを行う環境での使用を意図されたものである。統合開発環境を含む通常のVisual Studioを補完する製品という位置付けであり、Visual Studioの正規ユーザーが使用することが前提になっている。

## 製品バージョンと内部バージョン

Visual C++の製品バージョンは、バージョン6.0までは内部バージョンと同じ番号が付けられていたが、2002以降は内部バージョンではなくリリース予定年を冠するようになった。なお、Visual C++にはコンパイラのバージョンを表す `_MSC_VER` および `_MSC_FULL_VER` という[プリプロセッサ](../Page/プリプロセッサ.md "wikilink") シンボルが存在する\[46\]が、これはVisual C++の前身である[MS-DOS](../Page/MS-DOS.md "wikilink")用C/C++コンパイラ（通称MS-C）からの通し番号となっており、コンパイラ本体である **cl.exe** のファイルバージョンを表している。（このようにユーザーを混乱させかねない複数のバージョン表記は、Windowsと共通するものがある。）

<table>
<caption>Visual C++バージョンの履歴</caption>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th><p>製品バージョン</p></th>
<th><p>内部バージョン</p></th>
<th><p>_MSC_VER</p></th>
<th></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>C Compiler 1.0</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>100</p></td>
<td></td>
<td><p>Latice Cを元にした <a href="../Page/MS-DOS.md" title="wikilink">MS-DOS</a>用コンパイラ。K&amp;R未対応。</p></td>
</tr>
<tr class="even">
<td><p>C Compiler 2.0</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>200</p></td>
<td></td>
<td><p>Large Model 対応。</p></td>
</tr>
<tr class="odd">
<td><p>C Compiler 3.0</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>300</p></td>
<td><p>1985年</p></td>
<td><p>K&amp;R対応。</p></td>
</tr>
<tr class="even">
<td><p>C Compiler 4.0</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>400</p></td>
<td></td>
<td><p>オプティマイズ強化。ソースレベルデバッガのCodeViewを付属。</p></td>
</tr>
<tr class="odd">
<td><p>C Compiler 5.0</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>500</p></td>
<td><p>1987年</p></td>
<td><p>ループオプティマイズ。Huge Model対応。廉価版としてQuick C 1.0</p></td>
</tr>
<tr class="even">
<td><p>C Compiler 5.1</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td></td>
<td></td>
<td><p>OS/2 1.0対応。廉価版として Quick C 2.0 (1989)</p></td>
</tr>
<tr class="odd">
<td><p>C Compiler 6.0</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>600</p></td>
<td><p>1989年</p></td>
<td><p>Windowsプログラミングには別途SDKが必要。</p></td>
</tr>
<tr class="even">
<td><p>C/C++ Compiler 7.0</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>700</p></td>
<td><p>1992年</p></td>
<td><p>MFCが付属した最初のバージョン。</p></td>
</tr>
<tr class="odd">
<td><p>Visual C++ 1.0</p></td>
<td><p>1.0</p></td>
<td><p>1.0</p></td>
<td><p>800</p></td>
<td><p>1993年</p></td>
<td><p>32ビット対応。</p></td>
</tr>
<tr class="even">
<td><p>Visual C++ 1.5</p></td>
<td><p>1.5</p></td>
<td><p>1.5</p></td>
<td><p>800</p></td>
<td><p>1993年</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Visual C++ 1.51</p></td>
<td><p>1.51</p></td>
<td><p>1.51</p></td>
<td><p>800</p></td>
<td></td>
<td><p>Visual C++ 2.0/4.0Pro日本語版に付属。</p></td>
</tr>
<tr class="even">
<td><p>Visual C++ 1.52c</p></td>
<td><p>1.52</p></td>
<td><p>1.52c</p></td>
<td><p>800</p></td>
<td></td>
<td><p>英語版のみ。MS-DOS/Win16バイナリ（プログラム）を作成できる最終バージョン。</p></td>
</tr>
<tr class="odd">
<td><p>Visual C++ 2.0</p></td>
<td><p>2.0</p></td>
<td><p>2.0</p></td>
<td><p>900</p></td>
<td><p>1995年</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Windows_NT" title="wikilink">Windows NT対応</a>。32ビット専用。</p></td>
</tr>
<tr class="even">
<td><p>Visual C++ 2.1</p></td>
<td><p>2.1</p></td>
<td><p>2.1</p></td>
<td><p>900</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Visual C++ 2.2</p></td>
<td><p>2.2</p></td>
<td><p>2.2</p></td>
<td><p>900</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Visual C++ 4.0</p></td>
<td><p>4.0</p></td>
<td><p>4.0</p></td>
<td><p>1000</p></td>
<td><p>1996年</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Windows_95" title="wikilink">Windows 95対応</a></p></td>
</tr>
<tr class="odd">
<td><p>Visual C++ 4.1</p></td>
<td><p>4.1</p></td>
<td><p>4.1</p></td>
<td><p>1010</p></td>
<td><p>1996年</p></td>
<td><p><a href="../Page/Win32s.md" title="wikilink">Win32s</a>で動作するWin32バイナリ（プログラム）を作成できる最後のバージョン。</p></td>
</tr>
<tr class="even">
<td><p>Visual C++ 4.2</p></td>
<td><p>4.2</p></td>
<td><p>4.2</p></td>
<td><p>1020</p></td>
<td><p>1996年</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Visual C++ 5.0</p></td>
<td><p>5.0</p></td>
<td><p>5.0</p></td>
<td><p>1100</p></td>
<td><p>1997年</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Visual C++ 6.0</p></td>
<td><p>6.0</p></td>
<td><p>6.0</p></td>
<td><p>1200</p></td>
<td><p>1998年</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>2002</p></td>
<td><p>7.0</p></td>
<td><p>1300</p></td>
<td><p>2002年</p></td>
<td><p>マネージ拡張C++のサポート追加。</p></td>
</tr>
<tr class="even">
<td><p>Visual C++.NET 2003</p></td>
<td><p>2003</p></td>
<td><p>7.1</p></td>
<td><p>1310</p></td>
<td><p>2003年</p></td>
<td><p>Windows 95で動作するWin32バイナリ（プログラム）を作成できる最後のバージョン。この製品までは既定の文字コード設定が「マルチバイト文字列を使用する」になっている。</p></td>
</tr>
<tr class="odd">
<td><p>Visual C++ 2005</p></td>
<td><p>2005</p></td>
<td><p>8.0</p></td>
<td><p>1400</p></td>
<td><p>2005年</p></td>
<td><p>Windows 98/Me/NT4で動作するWin32バイナリ（プログラム）を作成できる最後のバージョン。この製品以降は既定で「Unicode文字列を使用する」に変更されている。C++/CLIのサポート追加。上位エディションでコード分析<code>/analyze</code>が使えるようになった[47]。</p></td>
</tr>
<tr class="even">
<td><p>Visual C++ 2008</p></td>
<td><p>2008</p></td>
<td><p>9.0</p></td>
<td><p>1500</p></td>
<td><p>2007年</p></td>
<td><p>Windows 2000で動作するWin32バイナリ（プログラム）を作成できる最後のバージョン[48]。<br />
<a href="../Page/IA-64.md" title="wikilink">IA-64</a>で動作するMFCを使うWin64バイナリ（プログラム）を作成できる最後のバージョン[49]。</p></td>
</tr>
<tr class="odd">
<td><p>Visual C++ 2010</p></td>
<td><p>2010</p></td>
<td><p>10.0</p></td>
<td><p>1600</p></td>
<td><p>2010年</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/C++0x" title="wikilink">C++0x</a>へ部分的に対応。<a href="../Page/IA-64.md" title="wikilink">IA-64</a>で動作するWin64バイナリ（プログラム）を作成できる最後のバージョン[50]。なお、Visual C++ 2010ではC++/CLI言語の<a href="../Page/インテリセンス.md" title="wikilink">インテリセンス</a>機能が動作しない。</p></td>
</tr>
<tr class="even">
<td><p>Visual C++ 2012</p></td>
<td><p>2012</p></td>
<td><p>11.0</p></td>
<td><p>1700</p></td>
<td><p>2012年</p></td>
<td><p>（C++0xでなく）<a href="https://ja.wikipedia.org/wiki/C++11" title="wikilink">C++11</a>へ部分的に対応開始。ただし__cplusplusの定義内容は199711L（C++98を表す）のまま。Windowsストアアプリ対応（WinRT、C++/CX）。C++/CLI言語のインテリセンスの復活。コード生成に関して SSE2 までの拡張命令の使用（/arch:SSE2）がデフォルトになった[51][52][53]。DirectXグラフィックス診断機能（Graphics Diagnostics）の追加。下位エディションでもコード分析が使えるようになった。</p></td>
</tr>
<tr class="odd">
<td><p>Visual C++ 2013</p></td>
<td><p>2013</p></td>
<td><p>12.0</p></td>
<td><p>1800</p></td>
<td><p>2013年</p></td>
<td><p>C++11対応の強化。C99の大半に対応。MFC/ATLのマルチバイト版はバンドルされなくなった[54]。マネージ拡張C++のコンパイルオプション (/clr:OldSyntax) を使用できる最後のバージョン。</p></td>
</tr>
<tr class="even">
<td><p>Visual C++ 2015</p></td>
<td><p>2015</p></td>
<td><p>14.0</p></td>
<td><p>1900</p></td>
<td><p>2015年</p></td>
<td><p>C++11/C++14対応の強化。リファクタリング機能の実験的サポート[55]。</p></td>
</tr>
<tr class="odd">
<td><p>Visual C++ 2017</p></td>
<td><p>2017</p></td>
<td><p>14.1</p></td>
<td><p>1910[56]</p></td>
<td><p>2017年</p></td>
<td><p>C++11/C++14/C++17対応の強化。<a href="https://ja.wikipedia.org/wiki/CMake" title="wikilink">CMake</a>対応の追加など[57]。Windows XPで動作するバイナリを作成できる最後のバージョン[58]。</p></td>
</tr>
<tr class="even">
<td><p>Visual C++ 2019</p></td>
<td><p>2019</p></td>
<td><p>14.2</p></td>
<td><p>1920[59]</p></td>
<td><p>2019年</p></td>
<td><p>C++20対応の強化。OpenMP 4.0 SIMDベクトル化の実験的サポート[60][61]。C++ IntelliCodeが付属[62]。Visual Studio 2017で実験的に追加された[63]エディター内C++コード分析の正式サポート[64]。</p></td>
</tr>
</tbody>
</table>

## ランタイムライブラリの互換性

Visual C++ (以下VC) のCRT (C Runtime) ライブラリは、コンパイルオプションによって[静的リンク](https://ja.wikipedia.org/wiki/静的リンク "wikilink")あるいは[動的リンク](../Page/動的リンク.md "wikilink")を選択することができる\[65\]。[DLLおよびEXEにVCランタイムを動的リンクする場合](../Page/ダイナミックリンクライブラリ.md "wikilink")、DLL/EXE自体のファイルサイズを削減できるなどのメリットがあるが、アプリケーションの実行にはVCバージョンごとのランタイムライブラリモジュールが実行環境に必要となる（例えばVC2010の場合は msvcr100.dll や msvcp100.dll など）。MFC/CLR/OpenMP/C++ AMPを利用して作成されたDLL/EXEの場合はさらにそれぞれのランタイムライブラリが必要となる。エンドユーザー環境向けにVCランタイムライブラリの再頒布可能 (redistributable) パッケージがインストーラー形式で提供されているが、このインストーラーにはデバッグバージョンのライブラリは含まれない。Windowsのバージョンによっては、特定のバージョンのVCランタイムのサブセットがシステムコンポーネントとしてプリインストールされている。

VCのランタイムライブラリは、バージョンごとにCRTオブジェクトのメモリ管理がなされていた。そのため、異なるバージョンのVC間でDLL境界を越えてCRTオブジェクトの寿命を管理することはできなかった。例えば古いバージョンのVCで作成されたDLL内で[malloc](https://ja.wikipedia.org/wiki/malloc "wikilink")/[newしたオブジェクトを](https://ja.wikipedia.org/wiki/new演算子 "wikilink")、新しいバージョンのVCで作成されたアプリケーションでfree/deleteしたり、逆に新しいVCで作成されたDLL内でmalloc/newしたオブジェクトを、古いVCで作成されたアプリケーションでfree/deleteしたりすることは、ヒープ破壊などの実行時エラーや未定義動作を招く原因となる\[66\]。メモリの確保と解放はモジュールごとに閉じていなければならず、モジュール外に確保と解放の処理を公開するためにはDLL関数によるラッピングが必要となる。

VC2015ではUniversal CRTが導入され、またVC2017およびVC2019ではランタイムに破壊的変更がなくVC2015との互換性があるため、一定の条件が満たされればDLL境界を越えてCRTオブジェクトの寿命を管理することができる\[67\]\[68\]\[69\]\[70\]。Windows 10の場合、Universal CRTはシステムコンポーネントとして標準インストールされているが、それよりも前のバージョンのWindowsでは[Windows Updateや再頒布可能パッケージによるシステムディレクトリへのインストール](https://ja.wikipedia.org/wiki/Windows_Update "wikilink")（集中配置）、あるいはアプリケーションごとのローカル配置などの手段を利用する必要がある\[71\]\[72\]\[73\]\[74\]\[75\]\[76\]。

## 脚注

## 関連項目

  - [Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")
  - [Microsoft Foundation Class](../Page/Microsoft_Foundation_Class.md "wikilink")
  - [Active Template Library](../Page/Active_Template_Library.md "wikilink")

## 外部リンク

  - [Visual C++ のドキュメント | Microsoft Docs](https://docs.microsoft.com/ja-jp/cpp/)
  - [C および C++ コーディング ツール | Visual Studio](https://www.visualstudio.com/ja/vs/cplusplus/)
  - [MSDN Code Recipe：サンプルコード集](https://code.msdn.microsoft.com/site/search?f%5B0%5D.Type=ProgrammingLanguage&f%5B0%5D.Value=C%2B%2B&f%5B0%5D.Text=C%2B%2B&sortBy=Date)

[Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink") [Category:Microsoft_Visual_Studio](https://ja.wikipedia.org/wiki/Category:Microsoft_Visual_Studio "wikilink") [Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink") [Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink")

1.  [ANSI Conformance](http://msdn.microsoft.com/en-us/library/02y9a5ye.aspx)
2.  [C99 library support in Visual Studio 2013 - Visual C++ Team Blog - Site Home - MSDN Blogs](http://blogs.msdn.com/b/vcblog/archive/2013/07/19/c99-library-support-in-visual-studio-2013.aspx)
3.
4.  [Visual C++ 2010 の新機能](http://msdn.microsoft.com/ja-jp/library/dd465215.aspx)
5.  [C++11 Features in Visual C++ 11](http://blogs.msdn.com/b/vcblog/archive/2011/09/12/10209291.aspx)
6.  [Support For C++11 Features (Modern C++)](http://msdn.microsoft.com/en-us/library/hh567368.aspx)
7.  [C++11/14/17 Features In VS 2015 RTM - Visual C++ Team Blog - Site Home - MSDN Blogs](http://blogs.msdn.com/b/vcblog/archive/2015/06/19/c-11-14-17-features-in-vs-2015-rtm.aspx)
8.  [Visual Studio 2017 リリース ノート](https://www.visualstudio.com/ja-jp/news/releasenotes/vs2017-relnotes-v15.0)
9.  [Visual C++ Language Conformance | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/visual-cpp-language-conformance)
10. [Announcing: MSVC Conforms to the C++ Standard | Visual C++ Team Blog](https://blogs.msdn.microsoft.com/vcblog/2018/05/07/announcing-msvc-conforms-to-the-c-standard/)
11. [コンパイラの実装状況 - cpprefjp C++日本語リファレンス](https://cpprefjp.github.io/implementation-status.html)
12. [MSVC now correctly reports __cplusplus | Visual C++ Team Blog](https://blogs.msdn.microsoft.com/vcblog/2018/04/09/msvc-now-correctly-reports-__cplusplus/)
13. \[<http://msdn2.microsoft.com/ja-jp/library/tt15eb9t(VS.80>).aspx Visual C++ の OpenMP\]
14. \[<http://msdn.microsoft.com/en-us/library/hs24szh9(VS.80>).aspx Visual C++ Editions (2005)\]
15. \[<http://msdn.microsoft.com/en-us/library/hs24szh9(VS.90>).aspx Visual C++ Editions (2008)\]
16. \[<http://msdn.microsoft.com/en-us/library/hs24szh9(VS.100>).aspx Visual C++ Editions (2010)\]
17. [Visual C++ Tools and Templates in Visual Studio Editions](http://msdn.microsoft.com/en-us/library/hs24szh9%28VS.110%29.aspx)
18. [How to: Iterate Over STL Collection with for each](http://msdn2.microsoft.com/en-us/library/ms177203.aspx)
19. [How to: Declare Override Specifiers in Native Compilations](http://msdn2.microsoft.com/en-us/library/z8ew2153.aspx)
20. [sealed (C++ Component Extensions)](https://msdn.microsoft.com/en-us/library/0w2w91tf.aspx)
21. [Compiler Support for Type Traits](http://msdn.microsoft.com/en-us/library/ms177194.aspx)
22. [SAL注釈](http://msdn.microsoft.com/ja-jp/library/ms235402.aspx)
23. [msclr 名前空間](https://msdn.microsoft.com/ja-jp/library/ms235643.aspx)
24. [STL/CLR ライブラリ リファレンス](https://msdn.microsoft.com/ja-jp/library/bb385954.aspx)
25. [同時実行ランタイム](https://msdn.microsoft.com/ja-jp/library/dd504870.aspx)
26. [C++ AMP (C++ Accelerated Massive Parallelism)](https://msdn.microsoft.com/en-us/library/hh265137.aspx)
27. \[<http://msdn.microsoft.com/ja-jp/library/8ef0s5kh(VS.80>).aspx CRTのセキュリティ強化\]
28. \[<http://msdn.microsoft.com/en-us/library/aa985872(VS.80>).aspx Safe Libraries: Standard C++ Library\]
29. \[<http://msdn.microsoft.com/en-us/library/aa985965(VS.80>).aspx Checked Iterators\]
30. [Visual C++ 2008 用の MFC Feature Pack](http://msdn.microsoft.com/ja-jp/library/bb982354.aspx)
31. [Visual Studio 2010 SP1 用の MFC の追加](https://msdn.microsoft.com/ja-jp/library/gg482719%28v=vs.100%29.aspx)
32. [C++ マネージ拡張プログラミング (C++)](https://msdn.microsoft.com/ja-jp/library/ms384255%28v=vs.71%29.aspx)
33. [ネイティブ C++ アプリケーションの再頒布](https://msdn.microsoft.com/ja-jp/library/aa984514%28v=vs.71%29.aspx)
34. [混在 (ネイティブおよびマネージ) アセンブリ](https://msdn.microsoft.com/ja-jp/library/x0w2664k.aspx)
35. [/clr (共通言語ランタイムのコンパイル)](https://msdn.microsoft.com/ja-jp/library/k8d11d4s.aspx)
36. [/clr (共通言語ランタイムのコンパイル) (C++)](https://msdn.microsoft.com/ja-jp/library/k8d11d4s%28v=vs.80%29.aspx)
37. [C++ - C++/WinRT の紹介](https://msdn.microsoft.com/ja-jp/magazine/mt745094.aspx)
38. [Introduction to C++/WinRT - Windows UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)
39. [Long Double 型](http://msdn.microsoft.com/ja-jp/library/9cx8xs15%28v=vs.100%29.aspx)
40. [/arch (x86) | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/build/reference/arch-x86)
41.
42. [Microsoft、“Professional”相当の無償版「Visual Studio Community 2013」を公開 - 窓の杜](http://www.forest.impress.co.jp/docs/news/20141113_675880.html)
43. [Visual Studio 2015 の製品ラインアップを発表 - Visual Studio 日本チーム ブログ - Site Home - MSDN Blogs](http://blogs.msdn.com/b/visualstudio_jpn/archive/2015/03/31/announcing-the-visual-studio-2015-product-line.aspx)
44. [ニュース - MSが「Visual Studio Community」を発表、無償でAndroid/iOSアプリも開発可能：ITpro](http://itpro.nikkeibp.co.jp/atcl/news/14/111401910/)
45. [Microsoft、統合開発環境「Visual Studio 2015」を正式公開 - 窓の杜](http://www.forest.impress.co.jp/docs/news/20150721_712630.html)
46. [定義済みマクロ](https://msdn.microsoft.com/ja-jp/library/b0084kay.aspx)
47. [Visual C++ 2003 ～ 2015 の新機能 | Microsoft Docs](https://docs.microsoft.com/ja-jp/cpp/porting/visual-cpp-what-s-new-2003-through-2015)
48.
49.
50.
51. コンパイラの判断によって32bit版アプリケーションでも SSE2 命令が使われる可能性がある。
52. \[<https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2012/bb531344(v=vs.110>) Breaking Changes in Visual C++ | Microsoft Docs\]
53. [浮動小数点の移行に関する問題 | Microsoft Docs](https://docs.microsoft.com/ja-jp/cpp/porting/floating-point-migration-issues)
54. [Unicode とマルチバイト文字セット (MBCS: Multibyte Character Set) のサポート](http://msdn.microsoft.com/ja-jp/Library/ey142t48%28VS.120%29.aspx)
55. [Visual Studio 2015 における Visual C++ の新機能](https://msdn.microsoft.com/ja-jp/library/hh409293%28v=vs.140%29.aspx)
56. Visual Studioのアップデートに伴い、`_MSC_VER`の最下位の桁も更新されるようになっている。
57. [Visual Studio 2017 (バージョン 15.0) リリース ノート](https://www.visualstudio.com/ja-jp/news/releasenotes/vs2017-relnotes-v15.0)
58. [Visual Studio 2019 プレビューでの非推奨の C++ 機能 | Microsoft Docs](https://docs.microsoft.com/ja-jp/cpp/porting/features-deprecated-in-visual-studio?view=vs-2019)
59.
60. [SIMD Extension to C++ OpenMP in Visual Studio | C++ Team Blog](https://devblogs.microsoft.com/cppblog/simd-extension-to-c-openmp-in-visual-studio/)
61. [/openmp (Enable OpenMP Support) | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/build/reference/openmp-enable-openmp-2-0-support?view=vs-2019)
62. [Visual Studio 2019 リリース ノート | Microsoft Docs](https://docs.microsoft.com/ja-jp/visualstudio/releases/2019/release-notes)
63. [New, experimental code analysis features in Visual Studio 2017 15.8 Preview 3 | C++ Team Blog](https://devblogs.microsoft.com/cppblog/new-experimental-code-analysis-features-in-visual-studio-2017-15-8-preview-3/)
64. [In-editor code analysis in Visual Studio 2019 Preview 2 | C++ Team Blog](https://devblogs.microsoft.com/cppblog/in-editor-code-analysis-in-visual-studio-2019-preview-2/)
65. [/MD, -MT, -LD (Use Run-Time Library) | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/build/reference/md-mt-ld-use-run-time-library)
66. [Potential Errors Passing CRT Objects Across DLL Boundaries | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/c-runtime-library/potential-errors-passing-crt-objects-across-dll-boundaries)
67. [C++ Binary Compatibility between Visual Studio 2015 and Visual Studio 2019 | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/porting/binary-compat-2015-2017?view=vs-2019)
68. [Visual C++ change history 2003 - 2015 | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/porting/visual-cpp-change-history-2003-2015)
69. [CRT ライブラリの機能 | Microsoft Docs](https://docs.microsoft.com/ja-jp/cpp/c-runtime-library/crt-library-features)
70. [Universal CRT へのコードのアップグレード | Microsoft Docs](https://docs.microsoft.com/ja-jp/cpp/porting/upgrade-your-code-to-the-universal-crt)
71. [Visual C++ 2015 以降のバージョンの再頒布可能パッケージにおけるインストールの前提条件 – Visual Studio サポート チーム blog](https://blogs.msdn.microsoft.com/jpvsblog/2018/02/27/ucrt-prerequisite/)
72. [Visual C++ 2015 アプリケーションでの CRT ローカル配置について – Visual Studio サポート チーム blog](https://blogs.msdn.microsoft.com/jpvsblog/2016/08/04/ucrt_local_deployment/)
73. [Introducing the Universal CRT | C++ Team Blog](https://devblogs.microsoft.com/cppblog/introducing-the-universal-crt/)
74. [Universal CRT deployment | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/windows/universal-crt-deployment)
75. [最新のサポートされる Visual C++ のダウンロード](https://support.microsoft.com/ja-jp/help/2977003/the-latest-supported-visual-c-downloads)
76. [Windows での汎用の C ランタイムの更新プログラム](https://support.microsoft.com/ja-jp/help/2999226/update-for-universal-c-runtime-in-windows)