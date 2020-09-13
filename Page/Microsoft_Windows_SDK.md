> この記事は[Microsoft Windows SDK](https://ja.wikipedia.org/wiki/Microsoft_Windows_SDK)から翻訳されています。


**Microsoft Windows SDK**（**マイクロソフト ウィンドウズ エスディーケー**）とは、[Microsoft Windowsで動作する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")を作成するために[マイクロソフト](../Page/マイクロソフト.md "wikilink")が無料で公開している[ソフトウェア開発キット](../Page/ソフトウェア開発キット.md "wikilink") (SDK) である。[Windows APIを利用するために必要な](../Page/Windows_API.md "wikilink")[ヘッダファイル](../Page/ヘッダファイル.md "wikilink")、[ライブラリ](../Page/ライブラリ.md "wikilink")、[ツール](https://ja.wikipedia.org/wiki/ツールソフトウェア "wikilink")、サンプルを含んでいる。

[Windows Vistaリリース前はMicrosoft](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") Platform SDKという名称であったが、Platform SDKと[.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") SDKを統合し、Windows SDKとなった。

## Windowsバージョンとの関連

新バージョンのWindowsで提供される新機能を使った[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")（新しいWindows APIあるいは[COMコンポーネントを使ったソフトウェア](../Page/Component_Object_Model.md "wikilink")）を開発する場合、基本的に対応する[C](../Page/C言語.md "wikilink") / [C++](../Page/C++.md "wikilink")言語用ヘッダファイルや[DLLインポートライブラリなどが含まれる新しいWindows](../Page/ダイナミックリンクライブラリ.md "wikilink") SDKを使用することになる。ヘッダファイルをインクルードする前に、`WINVER`などのターゲット環境のバージョン番号を表すマクロシンボルを適切に定義することで、新しいWindows API関数や新しい構造体が使用できるようになる。逆に、新しいSDKで古い実行環境をサポートする場合も、同様にマクロシンボルを適切に定義してAPIバージョンを制限する必要がある。古いバージョンのWindowsもターゲットに含めつつ、新しいバージョンのWindows上では新機能を使いたい場合、`GetProcAddress()`を使ってシステムDLLから新しいAPI関数のエントリポイントを動的に取得するなどの方法を採る\[1\]。

コンパイラやSDKのバージョンによっては、古いバージョンのWindowsを実行環境としてサポートしない\[2\]。例えばWindows 10 SDKでは、Windows 7 SP1以降を対象としたコードの記述をサポートする\[3\]。

また、マイクロソフトが提供しているソフトウェア[統合開発環境](../Page/統合開発環境.md "wikilink")である[Visual Studioには](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")、標準でWindows SDKが含まれているが、こちらは基本的に単体で提供されているSDKのサブセットやマイナーチェンジであり、単体版と比較してサンプルやツール類の一部が含まれていないことがある。なお、対応する単体版のSDKを使用するようにVisual Studioを設定することも可能である。

## 64ビット対応

バージョン7.1までのPlatform/Windows SDKには、[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")と[IA-64](../Page/IA-64.md "wikilink")コードを出力するVisual C++コンパイラがそれぞれ含まれている。コマンドプロンプトから使用するほか、[Visual C++ 2010](../Page/Microsoft_Visual_C++.md "wikilink") Express Editionと併せて用いることも可能である。

[Visual C++ 2005が公開されるまで](../Page/Microsoft_Visual_C++.md "wikilink")、Platform SDKが64ビット用Visual C++コンパイラを入手する唯一の手段であった。また、標準ライブラリの[64ビット](../Page/64ビット.md "wikilink")版も付属し、Visual C++ 6付属ライブラリの[IA-64](../Page/IA-64.md "wikilink")版は2003年2月に公開された版から、[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")版は[Windows Server 2003に対応したPlatform](../Page/Microsoft_Windows_Server_2003.md "wikilink") SDKの版から付属している。なお、両者共にマイクロソフトへ連絡するとVisual C++ .NET 2003付属ライブラリの64ビット版を取り寄せることができる。

Windows 10では64ビット版[ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink") (ARM64) にも対応しており、[UWPアプリ](https://ja.wikipedia.org/wiki/Universal_Windows_Platform "wikilink")/デスクトップアプリともにARM64の命令セットにネイティブ対応している。ARM64アプリケーション開発にはVisual Studio 2017 (15.9) 以降と対応SDKが必要となる\[4\]\[5\]。

## DirectX SDKとの関連

[Windows 7](../Page/Microsoft_Windows_7.md "wikilink") までは、Windows用マルチメディアAPIセットである[DirectXの開発キット](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")「**DirectX SDK**」は、Windows SDKとは別に提供されていたが、一部のヘッダやインポートライブラリ（[Direct3D](../Page/Direct3D.md "wikilink")、[Direct2D](https://ja.wikipedia.org/wiki/Direct2D "wikilink")、[DirectInput](../Page/DirectInput.md "wikilink")、[XInputなど](https://ja.wikipedia.org/wiki/DirectInput#XInput "wikilink")）はWindows SDKにも含まれるため、DirectX SDKなしでも一応DirectX APIを利用した開発は可能となっていた。ただし、ファイルのバージョンが最新のDirectX SDKに含まれるものと比べて古く（例えばWindows SDK 7.1のD3DCommon.hはDirectX SDK June 2010のそれよりも古く、定義されていないシンボルが多数ある）、また「D3DX（Direct3D 拡張ライブラリ）」のようなユーティリティライブラリ、および開発用の各種ツール類（スタンドアロンの[HLSL](https://ja.wikipedia.org/wiki/HLSL "wikilink")コンパイラやテクスチャ編集ツールなど）は含まれていなかった。

2005年4月、[DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")がDirectX SDKからPlatform SDKへ移管された。そのときからDirectShowのサンプルもPlatform SDK（Windows SDK）に収録されているが、これをビルドするには依然としてDirectX SDKが必要である。

[Windows 8](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink") および [Windows RT](https://ja.wikipedia.org/wiki/Windows_RT "wikilink") 用の[Windowsストア](https://ja.wikipedia.org/wiki/Windowsストア "wikilink")アプリ開発もできるようになった Windows SDK バージョン 8.0 以降は、DirectX SDK は Windows SDK に統合された。DirectX 関連ツール類もリニューアルされたものが Visual Studio 2012 以降に統合されているが、D3DX ライブラリは廃止されている。そのほか、かつて DirectX SDK に含まれていた  や [XACT](../Page/XACT.md "wikilink") (XACT3) なども、Windows SDK 8.0 には含まれていない\[6\]。また、以前のバージョンでは種々のサンプルコードがSDKパッケージに含まれていたが、8.0以降は[MSDN](https://ja.wikipedia.org/wiki/MSDN "wikilink")および[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")に移管されている。

## その他

  - バージョン6.2.6000まで日本語版が提供されていた\[7\]。
  - Visual C++ 6.0に対応した最後のPlatform SDKは2003年2月のリリースである\[8\]。現在はダウンロードでは提供されておらず、CDの注文が必要である\[9\]。

上記いずれとも、[MSDNサブスクリプションの会員ならダウンロード可能である](../Page/Microsoft_Developer_Network.md "wikilink")\[10\]。

## 関連項目

  - [Windows API](../Page/Windows_API.md "wikilink")
  - [ソフトウェア開発キット](../Page/ソフトウェア開発キット.md "wikilink") (SDK)
  - [Windows Driver Kit](../Page/Windows_Driver_Kit.md "wikilink")

## 脚注

[Category:プログラミング](https://ja.wikipedia.org/wiki/Category:プログラミング "wikilink") [Category:マイクロソフトの開発ツール](https://ja.wikipedia.org/wiki/Category:マイクロソフトの開発ツール "wikilink") [Category:ソフトウェア開発キット](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発キット "wikilink")

1.  [GetProcAddress | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/build/getprocaddress)
2.  [Update WINVER and _WIN32_WINNT | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/porting/modifying-winver-and-win32-winnt)
3.  [How to: Use the Windows 10 SDK in a Windows Desktop application | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/windows/how-to-use-the-windows-10-sdk-in-a-windows-desktop-application)
4.  [Windows 10 on ARM - UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/porting/apps-on-arm)
5.  [Official support for Windows 10 on ARM development - Windows Developer Blog](https://blogs.windows.com/windowsdeveloper/2018/11/15/official-support-for-windows-10-on-arm-development/)
6.  [DirectX SDKs of a certain age | Games for Windows and the DirectX SDK blog](https://walbourn.github.io/directx-sdks-of-a-certain-age/)
7.  [Windows Vista™ および .NET Framework 3.0 ランタイム コンポーネント用 Microsoft® Windows® Software Development Kit](https://web.archive.org/web/20160911123644/https://www.microsoft.com/ja-jp/download/details.aspx?id=30950)（2016年9月11日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")）
8.  [Windows Server 2003 PSDK Full Download with Local Install](https://web.archive.org/web/20100207051646/http://www.microsoft.com:80/msdownload/platformsdk/sdkupdate/psdk-full.htm)（2010年2月7日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")）
9.  [Windows Server 2003 SP1 Platform SDK ISO Install](http://www.microsoft.com/downloads/details.aspx?familyid=D8EECD75-1FC4-49E5-BC66-9DA2B03D9B92&displaylang=en)のSystem Requirements - Development Toolsの項参照
10.