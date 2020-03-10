> この記事は[Portable Executable](https://ja.wikipedia.org/wiki/Portable_Executable)から翻訳されています。


**Portable Executable**（**PE**）は、主に32ビットおよび[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")版の[Microsoft Windows上で使用される](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[実行ファイル](https://ja.wikipedia.org/wiki/実行ファイル "wikilink") (EXE)、[オブジェクトファイル](https://ja.wikipedia.org/wiki/オブジェクトファイル "wikilink")、[DLL](https://ja.wikipedia.org/wiki/DLL "wikilink")、SYS ([デバイスドライバ](../Page/デバイスドライバ.md "wikilink"))、FON フォントファイル等の[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")である。PEフォーマットは実行コードを管理するためにWindows OSローダが必要とする情報をカプセル化するデータ構造である。エクステンシブル・ファームウェア・インターフェイス([EFI](https://ja.wikipedia.org/wiki/UEFI "wikilink"))の仕様ではPEをEFI環境における標準の実行形式としている\[1\]。このため[UEFI](https://ja.wikipedia.org/wiki/UEFI "wikilink")アプリケーションや[.NETアプリケーションのバイナリフォーマットとしても使用されている](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。マイクロソフト製OSとの[マルチブート](https://ja.wikipedia.org/wiki/マルチブート "wikilink")環境の構築を容易にする目的で、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")、[x86-64](https://ja.wikipedia.org/wiki/x64 "wikilink")、[ARMアーキテクチャ](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")における[Linuxカーネル実行ファイル](https://ja.wikipedia.org/wiki/vmlinux "wikilink")（EFI Boot Stub）\[2\]や[ブートローダ](https://ja.wikipedia.org/wiki/ブートローダ "wikilink")など、非Windows系OSのシステムファイルの一部でも用いられている。

Windows NT オペレーティングシステムでは、PEは[IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink")、[IA-64](https://ja.wikipedia.org/wiki/IA-64 "wikilink")、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")、[x86-64](https://ja.wikipedia.org/wiki/x64 "wikilink") (AMD64/Intel 64)、[ARM](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink") および ARM64 [命令セットアーキテクチャ](https://ja.wikipedia.org/wiki/命令セットアーキテクチャ "wikilink") (ISA)がサポートされている。[Windows 2000以前のWindows](https://ja.wikipedia.org/wiki/Windows_2000 "wikilink") NTでは[MIPS](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ "wikilink")、 [Alphaおよび](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")[PowerPC](../Page/PowerPC.md "wikilink")命令セットアーキテクチャがサポートされていた。PEは[Windows CEでも利用されていたため](https://ja.wikipedia.org/wiki/Windows_CE "wikilink")、MIPSのいくつかの種類、[ARM](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink") ([Thumbを含む](https://ja.wikipedia.org/wiki/ARMアーキテクチャ#Thumb "wikilink"))、[SuperH](../Page/SuperH.md "wikilink")命令セットアーキテクチャでもサポートが継続されている\[3\]。

さまざまな[CPU](../Page/CPU.md "wikilink")アーキテクチャに対応するため、内部に判別用のフラグを持っている。実行時に[DLLを動的にリンクし](../Page/ダイナミックリンクライブラリ.md "wikilink")、コンポーネントレベルでのバグフィックス、互換性の維持が行われるようになっている。また、[リソース領域に](https://ja.wikipedia.org/wiki/リソース_\(Windows\) "wikilink")[アイコン](../Page/アイコン.md "wikilink")等を格納でき、[GUI上で表示された場合アイコンがグラフィカルに表示され](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink")、ソフトウェアが容易に判別できるようにできる。

PEと似たフォーマットとして[ELFファイル](https://ja.wikipedia.org/wiki/Executable_and_Linkable_Format "wikilink") ([Linux](../Page/Linux.md "wikilink")や[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")で利用) や [Mach-O](https://ja.wikipedia.org/wiki/Mach-O "wikilink") ([macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")や[iOS](https://ja.wikipedia.org/wiki/iOS "wikilink")で利用)がある。

## 歴史

マイクロソフトはWindows NT 3.1オペレーティングシステムの登場とともにPEフォーマットに移行した。Windows 95/98/ME や Windows 3.1x上の[Win32s](../Page/Win32s.md "wikilink")をはじめとする、その後のWindowsはすべてPEをサポートしている。[DOS](https://ja.wikipedia.org/wiki/DOS "wikilink")とNTシステムの[EXEフォーマット](https://ja.wikipedia.org/wiki/EXEフォーマット "wikilink")との互換性を持たせるため、PE/COFFヘッダーには[MS-DOS](../Page/MS-DOS.md "wikilink")プログラムがバイナリの先頭に組み込まれている。PEバイナリをMS-DOS上で起動させると、そのMS-DOSプログラムのほうが実行される。特に指定の無い場合、「This program cannot be run in DOS mode.」のような「DOSでは実行できない」というメッセージが表示するだけのプログラムが組み込まれる\[4\]。MS-DOSプログラムの後ろに、PE固有の識別子と、[COFFに似たデータ構造があり](https://ja.wikipedia.org/wiki/Common_Object_File_Format "wikilink")、MS-DOSヘッダによってそのオフセットが指されている。

引き続き[ファットバイナリ](https://ja.wikipedia.org/wiki/ファットバイナリ "wikilink")の形式である。PEは.NET PE形式や、PE32+ (もしくはPE+)と呼ばれる64ビットバージョン、およびWindows CE形式など、Windowsプラットフォームの変更にも対応し続けている。

## 対応する命令セットアーキテクチャ

  - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")：i386以降の[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")および互換[CPU](../Page/CPU.md "wikilink")のアーキテクチャ。PEにおいては、その中でも32ビットのコードを対象としている。x86を対象とするWindowsアプリケーションが格納されたPEは、x86版、[x86-64版](https://ja.wikipedia.org/wiki/x64 "wikilink")、[IA-64](https://ja.wikipedia.org/wiki/IA-64 "wikilink")版Windowsで直接実行できる。[ARM版Windowsにおいてはエミュレーションによって実行できる](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")。[Windows NT 4.0においては](https://ja.wikipedia.org/wiki/Microsoft_Windows_NT_4.0 "wikilink")、[Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")、[MIPS](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ "wikilink")、[PowerPC](../Page/PowerPC.md "wikilink")版においてエミュレータが存在した\[5\]。Xboxにおいては、ビルド途中の中間形式として採用されている\[6\]。i386版のUEFIアプリケーションの記述にも用いられている。
  - [x86-64](https://ja.wikipedia.org/wiki/x64 "wikilink"): 64ビット対応のx86命令。x64版Windowsで実行できる。x86-64版のUEFIアプリケーションの記述にも用いられている。
  - [IA-64](https://ja.wikipedia.org/wiki/IA-64 "wikilink")
  - [Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink"): Alphaプロセッサ上で動作する[Windows NTでのみ実行できる](../Page/Microsoft_Windows_NT.md "wikilink")。Alpha版Windowsはすでに開発が終了している。
  - [MIPS](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ "wikilink"): [Windows CE](https://ja.wikipedia.org/wiki/Windows_CE "wikilink")、Windows NTでサポートされていた。
  - [PowerPC](../Page/PowerPC.md "wikilink"): PowerPC版Windows NTでのみ実行できる。Xbox 360でも内部的な形式として用いられている\[7\]。
  - [SH-3/4](../Page/SuperH.md "wikilink"): Windows CEがサポートするアーキテクチャ。
  - [ARM](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink"): Windows CE、[Windows RT](https://ja.wikipedia.org/wiki/Microsoft_Windows_RT "wikilink")、[Windows 10でサポートされている](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")。
  - AArch64 (ARM64): [Windows 10でサポートされている](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")。

## 技術的詳細

## 他のオペレーティングシステムでの利用状況

PEフォーマットはWindowsとのバイナリ互換を謳っている[ReactOS](https://ja.wikipedia.org/wiki/ReactOS "wikilink")でも利用されている。過去には[SkyOS](https://ja.wikipedia.org/wiki/SkyOS "wikilink")や[BeOS](../Page/BeOS.md "wikilink") R3等いくつかのオペレーティングシステムで利用されていたが、SkyOSもBeOSも最終的には[ELFへ移行した](https://ja.wikipedia.org/wiki/Executable_and_Linkable_Format "wikilink")。

[Mono開発環境はMicrosoft](../Page/Mono_\(ソフトウェア\).md "wikilink") [.NET Frameworkとのバイナリ互換を謳っており](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、マイクロソフトの実装と同じPEフォーマットを利用している。

[x86](https://ja.wikipedia.org/wiki/x86 "wikilink") [Unix系](https://ja.wikipedia.org/wiki/Unix-like "wikilink") オペレーティングシステムでは、Windowsバイナリ(PEフォーマット)は[Wine](https://ja.wikipedia.org/wiki/Wine "wikilink")を通して実行できる。[HX DOS ExtenderもDOS](https://ja.wikipedia.org/wiki/HX_DOS_Extender "wikilink") 32ビットバイナリにPEフォーマットを利用しており、一部の既存WindowsバイナリをDOSで実行できるため、DOS版[Wine](https://ja.wikipedia.org/wiki/Wine "wikilink")として利用できる。

[IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink")と[x86-64の](https://ja.wikipedia.org/wiki/x64 "wikilink")[Linux](../Page/Linux.md "wikilink")では、[Windowsの](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[DLL](https://ja.wikipedia.org/wiki/DLL "wikilink")をloadlibraryで利用できる\[8\]。

[Mac OS X 10.5はPEファイルの読み込みと解析が可能だが](https://ja.wikipedia.org/wiki/Mac_OS_X_10.5 "wikilink")、Windowsとバイナリ互換はない\[9\]。

[UEFI](https://ja.wikipedia.org/wiki/UEFI "wikilink")とEFIファームウェアはPEとWindows [ABIをアプリケーションで使っている](../Page/Application_Binary_Interface.md "wikilink")。

## 脚注

## 関連項目

  - [EXE](https://ja.wikipedia.org/wiki/EXEフォーマット "wikilink")
  - [Executable and Linkable Format](https://ja.wikipedia.org/wiki/Executable_and_Linkable_Format "wikilink")
  - [Mach-O](https://ja.wikipedia.org/wiki/Mach-O "wikilink")
  - [a.out](https://ja.wikipedia.org/wiki/a.out "wikilink")
  - [実行可能ファイルフォーマットの比較](https://ja.wikipedia.org/wiki/実行可能ファイルフォーマットの比較 "wikilink")
  - [実行ファイル圧縮](https://ja.wikipedia.org/wiki/実行ファイル圧縮 "wikilink")
  - [アプリケーション仮想化](https://ja.wikipedia.org/wiki/アプリケーション仮想化 "wikilink")

## 外部リンク

  - [Windows実行可能形式](https://code.google.com/archive/p/corkami/wikis/PE101.wiki)
  - [S.S'S HOMEPAGE - 逆アセのスス乂 - MSDN技術資料（PE形式の解説）](http://www.interq.or.jp/chubu/r6/reasm/PE_FORMAT/intro.html)
  - [PECOFF仕様書(英語)](https://docs.microsoft.com/en-us/windows/win32/debug/pe-format)

[Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:オブジェクトファイルフォーマット](https://ja.wikipedia.org/wiki/Category:オブジェクトファイルフォーマット "wikilink")

1.  ,p.18のノートに「このイメージ形式を選択することでUEFIイメージにThumbおよびThumb-2命令セットを含めつつEFIインターフェイス自身をARMモードにする」とある。
2.
3.
4.
5.
6.
7.
8.  <https://github.com/taviso/loadlibrary>
9.