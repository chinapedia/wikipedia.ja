> この記事は[Application Binary Interface](https://ja.wikipedia.org/wiki/Application_Binary_Interface)から翻訳されています。


**Application Binary Interface**（アプリケーション・バイナリー・インタフェース、**ABI**）とは、アプリケーション（ユーザ）[プログラムとシステム](../Page/プログラム_\(コンピュータ\).md "wikilink")（OSやライブラリ）との間の、[バイナリ](../Page/バイナリ.md "wikilink")レベルの[インタフェースである](../Page/インタフェース_\(情報技術\).md "wikilink")。また、アプリケーション相互間や、それらの部品（プラグイン等）とのバイナリインタフェースもある。

ABIは[アプリケーションプログラミングインタフェース](../Page/アプリケーションプログラミングインタフェース.md "wikilink") (API) とは異なる。APIは[ソースコード](../Page/ソースコード.md "wikilink")とライブラリ間のインタフェースを定義したものであり、同じAPIをサポートしたシステム間では同じソースコードを[コンパイルして利用できる](../Page/コンパイラ.md "wikilink")。一方、ABIは[オブジェクトコードレベルのインタフェースであり](https://ja.wikipedia.org/wiki/オブジェクトファイル "wikilink")、互換ABIをサポートするシステム間では同じ[実行ファイル](https://ja.wikipedia.org/wiki/実行ファイル "wikilink")を変更無しで動作させることができる。

## 概要

ABIには、以下のような定義が含まれる。

  - [CPU](../Page/CPU.md "wikilink") - [命令セット](https://ja.wikipedia.org/wiki/命令セット "wikilink")、[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")など。
  - データ - [データ型](https://ja.wikipedia.org/wiki/データ型 "wikilink")、大きさ、配置（[アラインメント](https://ja.wikipedia.org/wiki/データ構造アライメント "wikilink")）など。
  - [呼出規約](https://ja.wikipedia.org/wiki/呼出規約 "wikilink") - [関数の](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")[引数](../Page/引数.md "wikilink")がどのように渡され、リターン値がどのように渡されるかを定義したもの。
  - [システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink") - システムコール番号と具体的なシステムコールの仕組み。
  - 実行ファイルやライブラリの詳細な[フォーマット](https://ja.wikipedia.org/wiki/フォーマット "wikilink")（[UNIX](../Page/UNIX.md "wikilink")ならば、[COFFや](https://ja.wikipedia.org/wiki/Common_Object_File_Format "wikilink")[ELFなど](https://ja.wikipedia.org/wiki/Executable_and_Linking_Format "wikilink")）。

Intel Binary Compatibility Standard (iBCS) のような完全なABIでは\[1\]、OSが何であれ必要な共有ライブラリが存在するなどの前提条件が満たされていれば、そのABIをサポートしたシステム間でプログラム（実行ファイル）を全く修正せずに動作させることができる。

他のABIとして例えば[C++](../Page/C++.md "wikilink")の[名前修飾](https://ja.wikipedia.org/wiki/名前修飾 "wikilink")\[2\]や[例外の伝播](../Page/例外処理.md "wikilink")\[3\]や呼出規約があるが、あくまでも同じ[プラットフォーム上のコンパイラ間のABIであり](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")、プラットフォーム間の互換性までは要求されない。

## EABI

EABI (Embedded Application Binary Interface) とは、[組み込みシステム](../Page/組み込みシステム.md "wikilink")のソフトウェアについての[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")、データ型、レジスタ使用法、スタックフレームの構成、関数の引数渡し方法などについての規約を意味する。

あるEABIをサポートする[コンパイラ](../Page/コンパイラ.md "wikilink")で生成した[オブジェクトコードは](https://ja.wikipedia.org/wiki/オブジェクトファイル "wikilink")、同じEABIをサポートする別のコンパイラで生成したコードと互換性があり、コンパイラが異なっていても同じEABIに対応していればライブラリやオブジェクトコード間でリンク可能である。[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")でコードを書く場合でもEABIに準拠するように書けば、他のコードとのリンクが保証される。

EABIと汎用OS向けABIとの主な違いは、アプリケーションのコードでも特権命令の使用が許されている点、ダイナミックリンクが要求されない点（完全に不可能とされている場合もある）、メモリを節約するため[スタックフレーム](https://ja.wikipedia.org/wiki/スタックフレーム "wikilink")をなるべくコンパクトに構成している点が挙げられる\[4\]。

EABIが広く使われているCPUアーキテクチャとしては、[PowerPC](../Page/PowerPC.md "wikilink")\[5\]、[ARM](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")\[6\]、[MIPS](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ "wikilink")\[7\]がある。

EABIの選択は性能に影響することがある\[8\]\[9\]。

## ABI共通化の試みとその成果

[Unix系](../Page/Unix系.md "wikilink")OSでは、同じ[ハードウェア](../Page/ハードウェア.md "wikilink")プラットフォーム上で非互換な複数のOSが動作する。

例えば[RISC](../Page/RISC.md "wikilink")チップにおいては以下のような例がある。

  - [POWER系](../Page/POWER_\(マイクロプロセッサ\).md "wikilink") : [AIX](https://ja.wikipedia.org/wiki/AIX "wikilink") 5L / [Solaris](../Page/Solaris.md "wikilink")10g / [Linux](../Page/Linux.md "wikilink")等
  - [MIPS系](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ "wikilink") : [UX/4800](https://ja.wikipedia.org/wiki/UX/4800 "wikilink") / [Irix](https://ja.wikipedia.org/wiki/Irix "wikilink") 等
  - [Itanium](https://ja.wikipedia.org/wiki/Itanium "wikilink")系 : [HP-UX](../Page/HP-UX.md "wikilink") / [Linux](../Page/Linux.md "wikilink") 等

最も互換Unix系OSが多いのは、[IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink")系であろう。それらOS間でABIを定義して相互にアプリケーションが動作できるようにしようという試みがいくつかあった。しかし、そのような計画が成功したことはない。[Linux](../Page/Linux.md "wikilink")においては、[Linux Standard Base](../Page/Linux_Standard_Base.md "wikilink")（LSB）が同様の試みを行っている（LSBはABI以外にも多くの規定を試みている）。

一方、採用ベンダ数が多く、複数のUnix系OSが乱立していたMIPS系においては、何度もABIの共通化を目指した試みがなされている。

例えば、[1990年代](../Page/1990年代.md "wikilink")中盤〜後半にかけてUNIX[ワークステーション](../Page/ワークステーション.md "wikilink") / [サーバ](../Page/サーバ.md "wikilink")において、[MIPS系CPUを採用した](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ "wikilink")[NEC](../Page/日本電気.md "wikilink")([UX/4800](https://ja.wikipedia.org/wiki/UX/4800 "wikilink"))、Sony([NEWS](https://ja.wikipedia.org/wiki/NEWS_\(ソニー\) "wikilink"))、[住友電工](https://ja.wikipedia.org/wiki/住友電気工業 "wikilink")（[EWS4800](../Page/EWS4800.md "wikilink")などのNECからの[OEM](../Page/OEM.md "wikilink")品とSUMIStation）、日本タンデムコンピュータ（MIPS系だったNonStopServer）による[OCMP](https://ja.wikipedia.org/wiki/OCMP "wikilink") (Open Computing Environment for MIPS Platform) が定義され、シェアの維持など一定の成果を挙げた。OCMPはMIPS-ABIの日本語対応の側面と[APバス](https://ja.wikipedia.org/wiki/APバス "wikilink")の標準化による周辺[デバイス](https://ja.wikipedia.org/wiki/デバイス "wikilink")の共通化の側面がある。

## 脚注

## 関連項目

  - [プログラミング (コンピュータ)](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")
  - [バイナリ](../Page/バイナリ.md "wikilink")
  - [束縛 (情報工学)](https://ja.wikipedia.org/wiki/束縛_\(情報工学\) "wikilink")
  - [SWIG](https://ja.wikipedia.org/wiki/SWIG "wikilink")

## 外部リンク

  - [KDE Techbase Policies](http://techbase.kde.org/Policies/Binary_Compatibility_Issues_With_C++) - リリース毎にバイナリ互換性を失わないための（[いくつかの例](http://techbase.kde.org/Policies/Binary_Compatibility_Examples)を交えた）開発経験則のよい解説
  - [Mac OS X ABI Function Call Guide](http://developer.apple.com/mac/library/documentation/DeveloperTools/Conceptual/LowLevelABI/000-Introduction/introduction.html)
  - [Debian ARM EABI port](http://wiki.debian.org/ArmEabiPort)
  - [µClib: Motorola 8/16-bit embedded ABI](http://www.uclibc.org/)
  - [AMD64 (x86-64) Application Binary Interface](http://www.x86-64.org/documentation.html)
  - [Application Binary Interface (ABI) for the ARM Architecture](http://infocenter.arm.com/help/topic/com.arm.doc.ihi0036a/index.html)
  - [MIPS EABI documentation](http://www.cygwin.com/ml/binutils/2003-06/msg00436.html)
  - [Sun Studio 10 Compilers and the AMD64 ABI](http://developers.sun.com/solaris/articles/about_amd64_abi.html) - いくつかの主要ABIの比較と解説

[Category:プログラミング](https://ja.wikipedia.org/wiki/Category:プログラミング "wikilink") [Category:オペレーティングシステムの仕組み](https://ja.wikipedia.org/wiki/Category:オペレーティングシステムの仕組み "wikilink")

1.  [Intel Binary Compatibility Standard (iBCS)](http://www.everything2.com/index.pl?node=iBCS)
2.  [Itanium C++ ABI](http://www.codesourcery.com/cxx-abi/abi.html) (compatible with multiple architectures)
3.  [Itanium C++ ABI: Exception Handling](http://www.codesourcery.com/cxx-abi/abi-eh.html) (compatible with multiple architectures)
4.
5.  ["PowerPC Embedded Processors Application Note"](http://www.ibm.com/chips/techlib/techlib.nsf/techdocs/852569B20050FF77852569970071B0D6/$file/eabi_app.pdf)
6.  [EABI2](http://infocenter.arm.com/help/index.jsp?topic=/com.arm.doc.ihi0036b/index.html)
7.  [MIPS EABI](http://www.cygwin.com/ml/binutils/2003-06/msg00436.html)
8.
9.