> この記事は[Intel C++ Compiler](https://ja.wikipedia.org/wiki/Intel_C++_Compiler)から翻訳されています。


**Intel C++ Compiler** （**インテル シープラスプラス コンパイラ**）とは[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が開発・販売している[C言語](../Page/C言語.md "wikilink")および[C++](../Page/C++.md "wikilink")用の[コンパイラ](../Page/コンパイラ.md "wikilink")である。日本での販売・サポートはXLsoftが行なっている。略称は**ICC**、あるいは**ICL**（それぞれ、Linux/macOS用およびWindows用コンパイラの実行プログラム名にもとづいている）。

## 概要

[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が自社の発売する[CPU](../Page/CPU.md "wikilink")の性能を最大限発揮するために開発したコンパイラである。CPUの開発元が自ら開発しただけあって高い最適化能力を誇り、最新のCPUへの[命令セット](../Page/命令セット.md "wikilink")への対応も非常に早い。主に[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")/[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")アーキテクチャをサポートする。バージョン11.1までは[IA-64](../Page/IA-64.md "wikilink") ([Itanium](../Page/Itanium.md "wikilink")) をサポートするが、バージョン12.0以降ではサポートされない\[1\]。バージョン11.1においては、次世代256ビット命令である[Intel AVXや](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#Intel_AVX "wikilink")、米国標準暗号方式である[AES命令セットがサポートされた](../Page/Advanced_Encryption_Standard.md "wikilink")。バージョン12.1において、AVX2命令がサポートされた\[2\]。

最適化性能の面では、特に[SIMD](../Page/SIMD.md "wikilink")命令を使用した自動ベクタライズ機能が優秀であり、。ただし、自動化といってもコンパイラが判断可能であるような限定的な状況でしか適用されず、[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")や組み込み関数を使って手動で慎重にベクタライズされたコードの実行速度にはかなわないことが多い。

他にもプロファイル計測用バイナリを出力し、実際に運用することによりコードの実行状況のデータを収集し、それを元に最適化するプロファイリング機能や、[OpenMP](../Page/OpenMP.md "wikilink")による自動[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")化にも対応している。バージョン11からは1パッケージで多言語対応となった。

実行に必要な[ライブラリ](../Page/ライブラリ.md "wikilink")や[リンカなどは付属していないため](../Page/リンケージエディタ.md "wikilink")、他のコンパイラの環境に寄生した形で実行される。[Windowsでは](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Microsoft Visual Studioが](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")、[Linux](../Page/Linux.md "wikilink")では[GCCが必要である](../Page/GNUコンパイラコレクション.md "wikilink")。基本的には[コンソールアプリケーション](https://ja.wikipedia.org/wiki/コンソールアプリケーション "wikilink")であるが Visual Studio 向けの[プラグイン](../Page/プラグイン.md "wikilink")が存在するため[統合開発環境](../Page/統合開発環境.md "wikilink")でも利用が可能である。 コンソールでの利用＝コマンドラインツールとしての利用のみであれば、無料版である[Visual C++ Express Editionがホスト環境として利用可能である](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio_Express "wikilink")。なお、Visual Studio 2010 Expressまでは、[IA-32](../Page/IA-32.md "wikilink")をターゲットとする場合は追加のSDKインストールは不要だが、[Intel 64をターゲットとする場合は別途追加の](https://ja.wikipedia.org/wiki/Intel_64 "wikilink")[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")開発用SDKをインストールする必要があった（Visual Studio Express 2012 for Windows Desktop以降は追加のインストールは不要になっている）。

30日無料の評価版があり、使用日期限以外の機能制限は存在しない。正規のライセンスを購入すればそのまま製品版として使用できる。ライセンスには1年間のアップデート入手の権利があり、ライセンス停止後に最新版をダウンロードしてきても使用できないが停止前にリリースされたバージョンはそのまま継続使用できる。ライセンスは更新することによってアップデート入手の権利を保持し続けることが可能である。なお、Linux版では非商用目的に限り無償で使用できるバージョンが公開されている\[3\]。

その性能の高さから特に画像処理、映像、音声・音響関係で使用される場合が多い。

なお、開発環境としてのWindows VistaおよびWindows Server 2003のサポートはバージョン14.0で終了した。

## 言語規格サポート

### C言語

[C99](../Page/C99.md "wikilink")\[4\]と[C11](https://ja.wikipedia.org/wiki/C11_\(C言語\) "wikilink")\[5\]の対応リストが公開されている。バージョン18.0でC11にほぼ対応している。

### C++

[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")\[6\]\[7\]、[C++14](https://ja.wikipedia.org/wiki/C++14 "wikilink")\[8\]、[C++17](https://ja.wikipedia.org/wiki/C++17 "wikilink")\[9\]の対応リストが公開されている。バージョン15.0でC++11にほぼ対応している。バージョン19.0において、[C++14](https://ja.wikipedia.org/wiki/C++14 "wikilink")を完全サポートし、[C++17](https://ja.wikipedia.org/wiki/C++17 "wikilink")の大部分をサポートしている。

なお、[Visual C++コンパイラでサポートされている](../Page/Microsoft_Visual_C++.md "wikilink")[C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")やおよび[C++ AMPの機能は使用できない](https://ja.wikipedia.org/wiki/C++_AMP "wikilink")。また、[Windowsストア](https://ja.wikipedia.org/wiki/Windowsストア "wikilink")アプリの開発にも使用できない。

### OpenMP

[OpenMP](../Page/OpenMP.md "wikilink")規格はバージョン12.1においてOpenMP 3.1をサポートしている。また、バージョン14.0においてOpenMP 4.0の機能を一部サポートしている\[10\]。バージョン19.0においてOpenMP 4.5およびOpenMP 5.0の一部をサポートしている。

そのほか、並列化のためのC/C++言語拡張としてCilk Plusをサポートしていたが、バージョン18.0で非推奨 (deprecated) となった。

## 付属のインテル製ライブラリ

Intel C++ Compiler 11.1 プロフェッショナル エディションには、下記のインテル純正の高性能ライブラリが付属する。

  - [Intel Integrated Performance Primitives](https://ja.wikipedia.org/wiki/Intel_Integrated_Performance_Primitives "wikilink") (IPP) - [画像処理](../Page/画像処理.md "wikilink")・[信号処理](https://ja.wikipedia.org/wiki/信号処理 "wikilink")・動画処理などに最適化された[マルチメディア](../Page/マルチメディア.md "wikilink")用ライブラリ
  - [Intel Threading Building Blocks](https://ja.wikipedia.org/wiki/Intel_Threading_Building_Blocks "wikilink") (TBB) - スレッドセーフ化されたコンテナや同期クラスを含む並列化用C++テンプレートライブラリ
  - [Intel Math Kernel Library](https://ja.wikipedia.org/wiki/Math_Kernel_Library "wikilink") (MKL) - [BLAS](https://ja.wikipedia.org/wiki/Basic_Linear_Algebra_Subprograms "wikilink")、[LAPACK](../Page/LAPACK.md "wikilink")、[FFTなどの高度な演算処理用に最適化された数学ライブラリ](../Page/高速フーリエ変換.md "wikilink")

Intel C++ Compiler バージョン10までは、上記ライブラリが付属しないスタンダード エディションが存在したが、バージョン11からはインテルの方針により、プロフェッショナル エディションのみの提供となっている。また、バージョン12以降の販売製品の名称はIntel C++ Compilerではなく、これらのライブラリを含めたスイート製品として**Intel C++ Composer XE**という名称が使われるようになっていたが、さらに[Intel Parallel Studio](https://ja.wikipedia.org/wiki/Intel_Parallel_Studio "wikilink")（開発ツール類を含む総合スイート製品）のバージョン2015以降は、「Intel Parallel Studio XE Composer Edition for C++」以上の製品エディションにIntel C++ Compilerが含まれる形となった。

なお、これらの各ライブラリは単体製品での販売も行なわれている。Intel C++ Compilerを使用せず、Visual C++コンパイラなどとIPP/TBB/MKLを組み合わせて使用することも可能である。

## 注意点・問題点

バージョン8から実行開始時のCPUチェックで[AMDのCPUを認識しないようになったため](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")、AMDのCPUでは出力バイナリの実行性能が劣ってしまう場合がある。。この問題はCPUチェック処理を独自に記述し、リンク時に強制的に上書きすることで回避することが可能である。

またデフォルトの設定では高速化のため[浮動小数点処理で自動的に](../Page/浮動小数点数.md "wikilink")[SSEを使用するようになっている](../Page/ストリーミングSIMD拡張命令.md "wikilink")。そのため[FPU](../Page/FPU.md "wikilink")を使用した場合とでは処理結果に差異が生ずる場合がある。精度重視の設定でコンパイルすることによりFPUを使用するコードを生成することが可能だが速度の方は遅くなってしまう。

コンパイルオプションでマルチCPU対応バイナリを出力することが可能だが、その分コードサイズが増大する傾向がある。

また、Intel C++ Compilerによって出力されたバイナリ（プログラム）の実行時に、Intel C++ Compiler独自の[DLLや](../Page/ダイナミックリンクライブラリ.md "wikilink")[共有ライブラリ](https://ja.wikipedia.org/wiki/共有ライブラリ "wikilink")が必要となる場合がある（明示的にOpenMPあるいはIPPライブラリを使用していなくても、特定の最適化オプションを有効にすることで、OpenMPあるいはIPPが暗黙的にリンクされる場合がある）。インテルからはランタイムライブラリ（libiomp5md.dllなどを含むパッケージ）が無償配布されているが、[Microsoft Visual C++のランタイムとは違って一般の](../Page/Microsoft_Visual_C++.md "wikilink")[エンドユーザー](../Page/エンドユーザー.md "wikilink")には公開されておらず、開発者自らがアプリケーションに添付するなどして再配布することになる\[11\]。しかし、これに留意せずランタイムの再配布や添付を行なわない開発者が多いため、エンドユーザーがプログラムを実行できない症例が多く報告されている\[12\]\[13\]\[14\]。この点に関してはライブラリを[静的リンク](https://ja.wikipedia.org/wiki/静的リンク "wikilink")することによりコードサイズは増大するがランタイムを必要としないコードを生成することが可能であるが、IPPなどにおいてSIMD拡張命令を使用した高速なバージョンの関数を使用するためには、プロセッサの対応状況を調べるための初期化関数（ippInit()関数）を別途呼び出す必要がある。また、スタティックライブラリ版のIntel OpenMPはIPP 7.0までの提供となっているため、以降のバージョンではOpenMPランタイムの[動的リンク](../Page/動的リンク.md "wikilink")が必須となる\[15\]。

## 脚注

<references/>

## 関連項目

  - [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")
  - [Microsoft Visual C++](../Page/Microsoft_Visual_C++.md "wikilink")
  - [Intel Parallel Studio](https://ja.wikipedia.org/wiki/Intel_Parallel_Studio "wikilink")
  - [OpenMP](../Page/OpenMP.md "wikilink")

## 外部リンク

  - [Intel](http://www.intel.com/index.htm)
  - [XLsoft](http://www.xlsoft.com/jp/index.html)
  - [インテル C++ コンパイラー 10.1 Windows 版リリースノート](http://www.xlsoft.com/jp/products/intel/compilers/ccw/10.1/Release_Notes.htm)

[Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink") [Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink") [Category:インテル](https://ja.wikipedia.org/wiki/Category:インテル "wikilink")

1.  [インテル® C++ Composer XE 2011 Windows\* 版インストール・ガイドおよびリリースノート - w_ccompxe_2011.7.258_Release_Notes_ja_JP.pdf](http://registrationcenter-download.intel.com/akdlm/irc_nas/2371/w_ccompxe_2011.7.258_Release_Notes_ja_JP.pdf)
2.  [インテル・コンパイラー12.1でサポートされたAVX2向けオプション | 最適化フォーラム | フォーラム | iSUS](http://www.isus.jp/forum/forum_optimize/%E3%82%A4%E3%83%B3%E3%83%86%E3%83%AB%E3%83%BB%E3%82%B3%E3%83%B3%E3%83%91%E3%82%A4%E3%83%A9%E3%83%BC12-1%E3%81%A7%E3%82%B5%E3%83%9D%E3%83%BC%E3%83%88%E3%81%95%E3%82%8C%E3%81%9Favx2%E5%90%91%E3%81%91/)
3.
4.  [C99 Support in Intel® C++ Compiler | Intel® Software](https://software.intel.com/en-us/articles/c99-support-in-intel-c-compiler)
5.  [C11 Support in Intel C++ Compiler | Intel® Software](https://software.intel.com/en-us/articles/c11-support-in-intel-c-compiler)
6.  [C++11 Features Supported by Intel® C++ Compiler | Intel® Software](https://software.intel.com/en-us/articles/c0x-features-supported-by-intel-c-compiler)
7.  [インテル® C++ コンパイラーでサポートされる C++11 の機能 | iSUS](https://www.isus.jp/products/c-compilers/c0x-features-supported-by-intel-c-compiler/)
8.  [C++14 Features Supported by Intel® C++ Compiler | Intel® Software](https://software.intel.com/en-us/articles/c14-features-supported-by-intel-c-compiler)
9.  [C++17 Features Supported by Intel® C++ Compiler | Intel® Software](https://software.intel.com/en-us/articles/c17-features-supported-by-intel-c-compiler)
10. [OpenMP\* 4.0 Features in Intel C++ Composer XE 2013 | Intel® Developer Zone](http://software.intel.com/en-us/articles/openmp-40-features-in-intel-c-composer-xe-2013)
11. [libiomp5md.dll と OpenMP](http://phreeqc.blogspot.jp/2011/11/libiomp5mddll-openmp.html)
12. [Hydrogenaudio Forums \> Flac compression through EAC not working](http://www.hydrogenaudio.org/forums//lofiversion/index.php/t19129.html%3Cbr%20/t51918.html)
13. [Hydrogenaudio Forums \> Cool Edit Pro 2.0 + Vorbis](http://www.hydrogenaudio.org/forums//lofiversion/index.php/t19129.html%3Cbr%20/t3303.html)
14. [WinAmp gives error whe loading AAC plugin - Hydrogenaudio Forums](http://www.hydrogenaudio.org/forums/index.php?showtopic=11747)
15.