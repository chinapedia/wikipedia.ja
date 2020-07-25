> この記事は[Windows API](https://ja.wikipedia.org/wiki/Windows_API)から翻訳されています。


**Windows API**（**ウィンドウズ エーピーアイ**）とは、[Microsoft Windowsの](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[システムコール](../Page/システムコール.md "wikilink")用[APIのこと](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。特に32ビットプロセッサで動作する[Windows 95以降や](../Page/Microsoft_Windows_95.md "wikilink")[Windows NTで利用できるものはWin](../Page/Microsoft_Windows_NT.md "wikilink")32 APIと呼ばれる。また、それらのWindowsにおけるWin32 APIの実装をWin32と呼ぶ。

## 概要

Windows上で動作するアプリケーションにとって、Windows APIはWindowsの各機能にアクセスするための接点である。そのため、Windows上で動作するアプリケーションを作成できる様々なプログラミング言語・開発環境においてWindows APIを使用する手段が提供されている。特にCとC++では、[Windows SDKにより](../Page/Microsoft_Windows_SDK.md "wikilink")、\<windows.h\>をはじめとする多数の[ヘッダーファイルが公開されている](../Page/ヘッダファイル.md "wikilink")。また、多くの開発環境で、Windows APIを基にしたより高水準の[フレームワーク](https://ja.wikipedia.org/wiki/フレームワーク "wikilink")が構築されている。これらを通じて、直接・間接にすべてのWindowsアプリケーションはWindows APIを使用している。

Windows APIに属する各APIは、主にDLLからの関数またはCOMインターフェイスとして機能を公開している。関数の[呼出規約](https://ja.wikipedia.org/wiki/呼出規約 "wikilink")は原則としてstdcallを採用する (Win32の場合) など統一されたインターフェイスで多数のプログラミング言語からの使用を容易なものとしている。

## 分類

Windows APIの中核となる機能はKernel、User、GDIに分けられる\[1\]。当初は、それぞれKERNEL.EXE (モードによってはKRNL286.EXE、KRNL386.EXE)、USER.EXE、GDI.EXEに実装されていた。32ビット化されて以降は、KERNEL32.DLL、USER32.DLL、GDI32.DLLに実装されている。Windows 7の新カーネル、[MinWin](https://ja.wikipedia.org/wiki/MinWin "wikilink")では、"Virtual DLL"の仕組みが導入され、インターフェイス互換性を維持したうえで実装の整理が行なわれている\[2\] \[3\]。

  - Kernel
    [ファイルシステム](../Page/ファイルシステム.md "wikilink")、[デバイス](https://ja.wikipedia.org/wiki/デバイス "wikilink")、[プロセス](../Page/プロセス.md "wikilink")、[スレッド](../Page/スレッド_\(コンピュータ\).md "wikilink")、[レジストリ](../Page/レジストリ.md "wikilink")、[例外処理](../Page/例外処理.md "wikilink")など基盤となる機能
  - User
    ウィンドウの処理、[ボタンやスクロールバーなどといった基本的な](../Page/ボタン_\(GUI\).md "wikilink")[コントロール](../Page/ウィジェット_\(GUI\).md "wikilink")、マウス・キーボード入力、その他[グラフィカルユーザーインターフェイス](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") (GUI) に関わる機能。
  - [GDI](../Page/Graphics_Device_Interface.md "wikilink")
    ディスプレイ・プリンタをはじめとした出力装置への描画機能

現在では、これだけに留まらず、多数のDLLから無数の機能が公開されている。現在、マイクロソフトのドキュメントでは次のように分類している\[4\]。

  - Administration and Management
  - Diagnostics
  - Graphics and Multimedia
  - Networking
  - Security
  - System Services
  - Windows User Interface

なお、この分類では、KernelはDiagnosticsとSystem ServicesそしてSecurityに跨って属し、UserはWindows User Interface、GDIはGraphics and Multimediaに属する。

### グラフィックとマルチメディア

#### DirectX

マイクロソフトは[Windows 95](https://ja.wikipedia.org/wiki/Windows_95 "wikilink")/[Windows NT](https://ja.wikipedia.org/wiki/Windows_NT "wikilink") 4以降、全てのWindowsに[DirectXを用意している](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")。DirectXは主に[ゲームと](../Page/コンピュータゲーム.md "wikilink")[マルチメディア](../Page/マルチメディア.md "wikilink")のためのAPIであるが、[Windows Vista以降はDirectX](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink") GraphicsがGDIに代わってOSのグラフィックス描画の基盤として昇格されている。DirectX APIのうちのいくつかは、ゲームコンソールである[Xbox](../Page/Xbox_\(ゲーム機\).md "wikilink")、[Xbox 360](../Page/Xbox_360.md "wikilink")、[Xbox Oneと共通になっている](https://ja.wikipedia.org/wiki/Xbox_One "wikilink")。

  - [Direct3D](../Page/Direct3D.md "wikilink")
    OpenGLの置き換えとして[3D](../Page/3次元コンピュータグラフィックス.md "wikilink") [グラフィックスアクセラレータ](https://ja.wikipedia.org/wiki/グラフィックスアクセラレータ "wikilink")の操作。
  - [DirectDraw](../Page/DirectDraw.md "wikilink")
    [2D](../Page/2次元コンピュータグラフィックス.md "wikilink") [グラフィックスアクセラレータ](https://ja.wikipedia.org/wiki/グラフィックスアクセラレータ "wikilink")の操作。DirectX 8.0以降、DirectDrawの機能はDirect3Dに吸収された。
  - DirectX Graphics
    DirectX 8.0以降に導入された名称で、Direct3DおよびDirectDrawの統合を意味するものだったが\[5\]、DirectX 11以降はDXGI/Direct3D/Direct2D/DirectWrite/DirectCompositionの総称となっている\[6\]。
  - [DXGI](https://ja.wikipedia.org/wiki/DXGI "wikilink") (DirectX Graphics Infrastructure)
    Direct3D 10以降、DirectX Graphicsから比較的変化の緩やかな部分はDXGIとしてDirect3Dから分離された。
  - [Direct2D](https://ja.wikipedia.org/wiki/Direct2D "wikilink")
    Direct3D上に構築された高レベル2D描画用API。[GDI+](https://ja.wikipedia.org/wiki/GDI+ "wikilink")の置き換えとなる。
  - [DirectWrite](https://ja.wikipedia.org/wiki/DirectWrite "wikilink")
    テキストおよび[フォント](../Page/フォント.md "wikilink")／フォント[グリフ](https://ja.wikipedia.org/wiki/グリフ "wikilink")を扱う。
  - [DirectSound](../Page/DirectSound.md "wikilink")
    低水準なハードウェア（主にサウンドカード）への操作。
  -
    DirectSoundの上位に位置し、音楽（メディアファイルの再生など）を扱う。
  - DirectX Audio
    DirectX 8.0以降に導入された名称で、DirectSoundおよびDirectMusicの統合を意味するものだったが\[7\]、DirectX 9以降は[X3DAudio](https://ja.wikipedia.org/wiki/X3DAudio "wikilink")/[XAudio2](https://ja.wikipedia.org/wiki/XAudio2 "wikilink")/[XACT](../Page/XACT.md "wikilink")/DirectSoundなどの総称となっている\[8\]。
  - [DirectInput](../Page/DirectInput.md "wikilink")
    ジョイパッドや[ゲームパッド](../Page/ゲームパッド.md "wikilink")からの入力、および[フォースフィードバック](https://ja.wikipedia.org/wiki/フォースフィードバック "wikilink")を扱う。
  - [XInput](https://ja.wikipedia.org/wiki/XInput "wikilink")
    [Xbox 360コントローラーをWindows上で使えるようにするAPI](../Page/Xbox_360.md "wikilink")。
  -
    ネットワークなどを介した通信。
  - [DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")
    汎用的なマルチメディアパイプラインシステム。

DirectX APIはWindows APIの中でも変化が激しいAPIのひとつで、Direct3D RM、DirectDraw、DirectSound、DirectInput、DirectPlay、およびDirectMusicはWindows Vista以降完全な互換機能が用意されず、一部を除いて廃止あるいは代替APIに吸収されている\[9\]。

#### 動画・音声

  - [Video for Windows](https://ja.wikipedia.org/wiki/Video_for_Windows "wikilink")、 (MCI) や[WinMM](https://ja.wikipedia.org/wiki/WinMM "wikilink")などのWindowsマルチメディアAPI \[10\] \[11\]
  - [DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")
  - [Media Foundation](../Page/Media_Foundation.md "wikilink")
  - [Core Audio](https://ja.wikipedia.org/wiki/Core_Audio_\(Windows\) "wikilink")

#### OpenGL

  -
    [OpenGL](../Page/OpenGL.md "wikilink")とWindows (GDI) との連携部分を担当するAPIである。各関数名は接頭辞`wgl`で始まり、`<wingdi.h>`で宣言されている。なお、Windows SDKに付属するOpenGLヘッダーおよびライブラリにはOpenGL 1.1までの関数しか定義されておらず、したがってOpenGL 1.2以降の機能を使うためには、Khronosから最新のOpenGLヘッダーをダウンロードしたのち、WGLの`wglGetProcAddress()`関数を用いてハードウェアベンダーが提供するOpenGL ICD (Installable Client Driver) の関数エントリポイントをアプリケーション実行時に取得するなどの作業が必要となる\[12\]。

### ネットワーク・インターネット

  - [Winsock](../Page/Winsock.md "wikilink")

  - [NetBIOS](https://ja.wikipedia.org/wiki/NetBIOS "wikilink")

  - [MSRPC](https://ja.wikipedia.org/wiki/DCE/RPC "wikilink")

  - [Trident](../Page/Trident.md "wikilink"): IEコンポーネント ([MSHTML](https://ja.wikipedia.org/wiki/MSHTML "wikilink"))

  -
  - [WinINet](https://ja.wikipedia.org/wiki/Microsoft_Windows_Internet "wikilink")

### コンポーネント技術

  - [Component Object Model](../Page/Component_Object_Model.md "wikilink") (COM)
  - [Microsoft Transaction Server](../Page/Microsoft_Transaction_Server.md "wikilink") (MTS), [Distributed Component Object Model](../Page/Distributed_Component_Object_Model.md "wikilink") (DCOM)
  - [Object Linking and Embedding](../Page/Object_Linking_and_Embedding.md "wikilink") (OLE), [ActiveX](../Page/ActiveX.md "wikilink"), [OLEオートメーション](https://ja.wikipedia.org/wiki/OLEオートメーション "wikilink")

### ネイティブAPI

[ネイティブAPI](https://ja.wikipedia.org/wiki/ネイティブAPI "wikilink")は、[Windows NT系においてWindows](../Page/Windows_NT系.md "wikilink") APIより下位層のAPIである。NT系では、NTネイティブAPI上にサブシステムとしてWin32 APIが実装されている。ただし、DirectXやGDIなどは、ネイティブAPIを介せずに、より下位に位置するカーネルと直接やり取りを行う。

### .NET Frameworkとの関係

Windowsで動作する[.NET Frameworkは](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、基本的にWin32 APIを用いて実装されている。例えば[Windows Formsおよび](../Page/Windows_Forms.md "wikilink")[Windows Presentation Foundation](../Page/Windows_Presentation_Foundation.md "wikilink") (WPF) はそれぞれGDI/GDI+あるいはDirect3Dを利用したGUIアプリケーションのフレームワークでり、Win32 APIとの相互運用性も確保されている。

かつて、「[Windows Vista以降](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、WinFX (.NET Framework 3.0) がWindows APIに代わってネイティブAPIになる（WinFXが最も低水準なAPIとなりWindows APIはそのラッパーとなる）」とアナウンスされたことがあったが、結局撤回され、Windows Vista製品版では従来通りWindows APIがネイティブなAPIとなっている。

## 実装

Windows APIは名前からも類推できるとおり、主に[Microsoft Windowsに実装されている](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。その実装はWindowsのバージョン毎に少なからず違いが存在する。たとえばWin32の場合、Win32c、Win32sではごく一部を除き[Unicode](../Page/Unicode.md "wikilink")に対応していない、[セキュリティ対策のアクセス制限が実装されていないなどといった違いが挙げられる](../Page/コンピュータセキュリティ.md "wikilink")。そしてそれは大きく次のように分類することができる。

### Win16

Win16は、16ビットプログラム用の実装である。ただし、Win16という語自体はWin32が登場してから用いられるようになった[レトロニム](../Page/レトロニム.md "wikilink")である\[13\]。Win16は大きく2種類に分けられる。

  - Windows 1.0からWindows 3.1までおよびWindows 95/98/Me（[9x系](../Page/Windows_9x系.md "wikilink")）の実装。
  - **WOW ([Windows on Windows](https://ja.wikipedia.org/wiki/Windows_on_Windows "wikilink"))**: [Windows NTによるWin](https://ja.wikipedia.org/wiki/Windows_NT "wikilink")16サブシステムによる実装。

### Win32

Win32は、32ビットプログラム用の実装である。次のように分けられる。

  - Win32
    狭義のWin32は、[NT系の実装を指す](../Page/Windows_NT系.md "wikilink")。

  - Win32c
    [9x系の実装](../Page/Windows_9x系.md "wikilink")。'c'は「compatibility」（互換）の頭文字である。しかし、では9xの実装も区別なくWin32と呼ぶ\[14\]。

  - [Win32s](../Page/Win32s.md "wikilink")
    [Windows 3.1用の実装](../Page/Microsoft_Windows_3.x.md "wikilink")。's'は「subset」（[サブセット](../Page/部分集合.md "wikilink")）の頭文字である。Windows 3.1には搭載されておらず、別途入手・[インストール](../Page/インストール.md "wikilink")する必要がある。

  - Win32 for Windows CE<ref> {{Cite web

|date=1997-04-01 |url=<http://www.microsoft.com/presspass/press/1997/apr97/cpdc%20%20pr.mspx> |title=Microsoft Announces Visual C++ for Windows CE |language=英語 |publisher=マイクロソフト |accessdate=2009-01-30 }}</ref>

  -
    [Windows CEの実装](https://ja.wikipedia.org/wiki/Windows_CE "wikilink")。[文字コード](../Page/文字コード.md "wikilink")に[Unicode](../Page/Unicode.md "wikilink")のみを使用するなどの点が特徴的である。
  - [WOW64](../Page/WOW64.md "wikilink") (Windows on Windows 64)
    Win64上でWin32をエミュレーションするサブシステムによる実装。

Windows NTが[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")以外の[アーキテクチャに移植されたことに伴い](../Page/コンピュータ・アーキテクチャ.md "wikilink")、Win32は各種アーキテクチャ向けに移植されている\[15\]。また、Windows NTではないが、かつてMacintosh用のWin32も存在し、Microsoft Visual C++ 4.0 Cross-Development Edition for Macintoshとして[クロスコンパイラ](../Page/クロスコンパイラ.md "wikilink")とともに発売されていた\[16\]。これらアーキテクチャの異なるWin32の間には[ソースコード](../Page/ソースコード.md "wikilink")上での互換性がある。

### Win64

Win64は、[64ビット](../Page/64ビット.md "wikilink")プログラム用の実装である。、[IA-64](../Page/IA-64.md "wikilink")及び[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")用の2種類の実装が存在する。Windows 10では[ARM64](https://ja.wikipedia.org/wiki/ARM64 "wikilink")の将来的なサポートが計画されている\[17\] \[18\]。

### WinRT

[Windows 8で導入された](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")[Windowsストア](https://ja.wikipedia.org/wiki/Windowsストア "wikilink")アプリ (Modern UIアプリケーション) を開発するためのCOM拡張による高レベルAPI。後継となる[Windows 10で導入された](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")[ユニバーサルWindowsプラットフォーム](https://ja.wikipedia.org/wiki/ユニバーサルWindowsプラットフォーム "wikilink") (UWP) アプリケーションの開発におけるベースAPIにもなっている。

### マイクロソフト以外による実装

Windows APIの仕様は[Windows SDKのドキュメントや](../Page/Microsoft_Windows_SDK.md "wikilink")[MSDN ライブラリで公開されており](https://ja.wikipedia.org/wiki/MSDN_ライブラリ "wikilink")、それを基にしたMicrosoft Windows以外のWindows APIの実装が存在する。

  - [Wine](../Page/Wine.md "wikilink")
  - [ReactOS](../Page/ReactOS.md "wikilink")
  - [HX DOS Extender](https://ja.wikipedia.org/wiki/HX_DOS_Extender "wikilink")

## 詳細

### Unicode対応

<table>
<caption>各Win32が実装しているAPI</caption>
<thead>
<tr class="header">
<th></th>
<th><p>Win 9x</p></th>
<th><p>Win NT</p></th>
<th><p>Win CE</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>W</p></td>
<td><p>一部対応</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

Windows NT系では当初から[Unicode](../Page/Unicode.md "wikilink")が用いられている一方、Unicodeに対応していないWin16と互換性を取るために、Win32 APIから同じAPIに対して[マルチバイト文字](../Page/マルチバイト文字.md "wikilink")版とUnicode版の2つを用意し、C/C++のマクロを駆使してコンパイル時にどちらを使うか選択できる仕組みが採用されている\[19\]。なお、Unicodeの符号化には当初[UCS-2](https://ja.wikipedia.org/wiki/UCS-2 "wikilink")、Windows 2000から正式に[UTF-16](../Page/UTF-16.md "wikilink")が用いられている\[20\]。

具体的には、文字および文字列の関わる[関数](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")・[構造体](../Page/構造体.md "wikilink")について、マルチバイト文字（Windowsコードページに基づく、日本語環境であれば[コードページ932](../Page/Microsoftコードページ932.md "wikilink")）とUnicode (UTF-16) のどちらを与えることもできるように、2つの関数・構造体などが準備されている。その場合、マルチバイト文字列を与えるべき関数・構造体は末尾に「A」を付け、ワイド文字列を与えるべき関数・構造体は末尾に「W」を付けて区別している。例えば、Win16のMessageBox関数に対して、Win32ではMessageBoxAとMessageBoxWという2つの関数が用意されている。そして、プリプロセッサ識別子UNICODEの定義の有無によって切り替えが行われる。

``` c
#ifdef UNICODE
#define MessageBox MessageBoxW
#else
#define MessageBox MessageBoxA
#endif
```

さらに、文字型に対しても同様にCHAR (charのtypedef) とWCHAR (wchar_tのtypedef) をUNICODEの定義で切り替えるTCHAR型などや、ナロー文字列定数・リテラルとワイド文字列定数・リテラルを切り替えるTEXTマクロが存在する。

``` c
#ifdef UNICODE
#define TEXT(s) L ## s
typedef WCHAR TCHAR;
#else
#define TEXT(s) s
typedef CHAR TCHAR;
#endif
```

これらを適切に用いると、1つのソースコードからコンパイル時のオプションによってマルチバイト文字を用いる実行プログラムとワイド文字を用いる実行プログラムの2種類が作成できる。以下はその例である。

``` c
#include <windows.h>
int WINAPI WinMain(HINSTANCE hInst, HINSTANCE hInstPrev, LPSTR lpszCommandLine, int nCmdShow)
{
    MessageBox(NULL, TEXT("Hello, world"), TEXT("App"), MB_OK);
    return 0;
}
```

なお、Windows NT系におけるA版のAPI関数は、Unicodeとの変換を行いW版を呼び出すラッパーとなっている\[21\]。

このプレフィックスのAはANSI、WはWideを意味する\[22\]。ANSIは、Windowsコードページの一部がANSI規格のドラフトを元にしたことに由来する\[23\]。[ワイド文字](../Page/ワイド文字.md "wikilink") (wchar_t) はC/C++の用語であるが、Windows用のC/C++処理系において、ワイド文字は大抵UCS-2またはUTF-16として実装されている。また、OLE関係では、Win32ですべてUnicode化され、A/Wの区別が存在しない。

なお、[Windows 9x系では](../Page/Windows_9x系.md "wikilink")、Unicode版APIは一部しか実装されていない\[24\]。ただし、[Microsoft Layer for Unicodeを利用することにより](../Page/Microsoft_Layer_for_Unicode.md "wikilink")、ほぼすべてのUnicode版APIが使用可能になる\[25\]。また、Windows CEでは、逆にUnicode版APIしか実装していない。NT系でも、Unicodeを前提とした仕様変更が行われたり\[26\]、Theme APIなど新しいAPIでA/Wの2種を用意せずUnicodeを用いるものだけを用意したりするなど、徐々にUnicodeへ傾斜する傾向にある。

## 歴史

Windows APIの歴史は、もちろんWindows自体の歴史と切り離せない関係にある。常に、Windowsに新機能が搭載されれば、それを[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")から使用するための新しくAPIが追加され、新しいSDKが公開されることの繰り返しである（もちろん、[デバイスドライバー](https://ja.wikipedia.org/wiki/デバイスドライバー "wikilink")らに対応を迫るものは、DDK/[WDKで公開される](../Page/Windows_Driver_Kit.md "wikilink")）。

Windows APIの歴史上、最も大きな変革はWindows NTに伴うWin32の登場だった。ポインタとハンドルも32ビット化されたこと、[Unicode](../Page/Unicode.md "wikilink")への対応が図られたことが大きな変化である。

なお、は緩やかに64ビットへの移行が進んでいる。Win64では、ポインタおよびハンドルは64ビット化されているが、それ以外では16ビットから32ビットへの移行時のような大きな変化はない。なお、64ビット版Windowsでは32ビットアプリケーションとの相互運用性を確保するため、ハンドルの上位32ビットを使用する仕組みとなっており、ウィンドウ (HWND) などのユーザーオブジェクトハンドル、ブラシ (HBRUSH) やペン (HPEN) などのGDIオブジェクトハンドル、そしてミューテックス、セマフォ、ファイルなどの名前付きオブジェクトハンドルを32ビット/64ビットアプリケーション間で共有し、プロセス間通信に利用することができる\[27\]。また、64ビット版Windowsでは[WOW64](../Page/WOW64.md "wikilink")により32ビットアプリケーションを実行できるが、16ビットアプリケーションを実行することはできない\[28\] \[29\]。

## 批判

Windows APIはWin16を拡張して32ビット、64ビット化されたという歴史がある。そのため度重なる機能の追加により、高度に複雑化しその習得が困難と化しているという問題がある\[30\]。

また、度重なるバージョンアップによりコンポーネントの互換性を失ってしまうことによる[DLL地獄](../Page/DLL地獄.md "wikilink") (DLL Hell) の発生を招いている。

## ラッパーライブラリ

Windows APIは比較的低水準であるため、高水準な[インターフェイスを持たせるための様々なラッパーが数多く存在する](../Page/インタフェース_\(情報技術\).md "wikilink")。主なものは次のとおり。

### マイクロソフト

  - [Microsoft Foundation Class](../Page/Microsoft_Foundation_Class.md "wikilink") (MFC)
    C++クラスによるWindows APIのラッパー。
  - [Active Template Library](../Page/Active_Template_Library.md "wikilink") (ATL)
    C++テンプレートによる[COMのラッパー](../Page/Component_Object_Model.md "wikilink")。
  - [Windows Template Library](../Page/Windows_Template_Library.md "wikilink") (WTL)
    ATLの拡張として作られた軽量のWindows APIのラッパー。は[CPLに基づく](../Page/Common_Public_License.md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")となっている。

### ボーランド

  - [Object Windows Library](https://ja.wikipedia.org/wiki/Object_Windows_Library "wikilink") (OWL)
    MFCと同時期に公開され、より[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")に作られたラッパー。
  - [Visual Component Library](../Page/Visual_Component_Library.md "wikilink") (VCL)
    [ボーランド](../Page/ボーランド.md "wikilink")がその後に作った[Delphi](../Page/Delphi.md "wikilink")によるラッパー。

[.NET FrameworkにもWindows](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") APIをラップした部分が存在する。

## 脚注

## 関連項目

  - [Component Object Model](../Page/Component_Object_Model.md "wikilink") (COM)
  - [Object Linking and Embedding](../Page/Object_Linking_and_Embedding.md "wikilink") (OLE)
  - [DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")
  - [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")

## 参考文献

  - Charles Petzold著　『プログラミングWindows第5版〈上〉』　アスキー、2000年。ISBN 4756136001
  - Charles Petzold著　『プログラミングWindows第5版〈下〉』　アスキー、2000年。ISBN 475613601X
  - Jeffrey Richter著　『Advanced Windows 改訂第4版』　アスキー、2001年。ISBN 4756138055

## 外部リンク

  - [Windows API (Windows) - MSDN Library](http://msdn.microsoft.com/en-us/library/cc433218.aspx)

[Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink")

1.
2.  [ASCII.jp：MinWinとVirtual DLLで変わるWindowsカーネル (1/2)｜あなたの知らないWindows](http://ascii.jp/elem/000/000/506/506852/)
3.  [ASCII.jp：ARM版Windows 8実現の布石となったWindows 7の「MinWin」 (3/4)｜基礎から覚える 最新OSのアーキテクチャー](http://ascii.jp/elem/000/000/682/682103/index-3.html)
4.
5.  [DirectX 8.0 の紹介](https://msdn.microsoft.com/ja-jp/library/dd148689.aspx)
6.  [Getting Started with DirectX Graphics (Windows)](https://msdn.microsoft.com/en-us/library/windows/desktop/hh309467.aspx)
7.  [DirectX 8.0 の紹介](https://msdn.microsoft.com/ja-jp/library/dd148689.aspx)
8.  [オーディオのリファレンス](https://msdn.microsoft.com/ja-jp/library/cc308058.aspx)
9.  [DirectX に関してよく寄せられる質問](https://msdn.microsoft.com/ja-jp/library/ee416788.aspx)
10. [Windows マルチメディア](https://msdn.microsoft.com/ja-jp/library/cc428426.aspx)
11. [Windows Multimedia (Windows)](https://msdn.microsoft.com/en-us/library/dd743883.aspx)
12. [OpenGL - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/opengl/opengl)
13.
14.
15.
16.
17. [Microsoft、ARM64対応のデスクトップ版Windows 10を計画か - エキサイトニュース](http://www.excite.co.jp/News/it_g/20160117/Slashdot_16_01_16_227229.html)
18. Windows SDK 10にはARM64用のインポートライブラリファイルなどが含まれている。
19.
20.
21.
22.
23.
24.
25.
26.
27. [Interprocess Communication Between 32-bit and 64-bit Applications (Windows)](https://msdn.microsoft.com/en-us/library/aa384203.aspx)
28. [32 ビット アプリケーションの実行 (Windows)](https://msdn.microsoft.com/ja-jp/library/aa384249.aspx)
29. [64bit Windows時代到来：第3回　アプリケーションの互換性 (1/3) - ＠IT](http://www.atmarkit.co.jp/ait/articles/1007/29/news109.html)
30.