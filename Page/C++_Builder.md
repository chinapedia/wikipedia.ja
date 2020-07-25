> この記事は[C++ Builder](https://ja.wikipedia.org/wiki/C++_Builder)から翻訳されています。


**C++ Builder**（C++ビルダー）は、[エンバカデロ・テクノロジーズ](https://ja.wikipedia.org/wiki/エンバカデロ・テクノロジーズ "wikilink")の[C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) である。

同社の代表製品である「[Delphi](../Page/Delphi.md "wikilink")」のC/C++版とも言える[RADツールで](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")、[Delphi](../Page/Delphi.md "wikilink")と同様に構成部品を貼り付けていくような[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink") (UI) 設計を可能としている。

元々は[ボーランド](../Page/ボーランド.md "wikilink")（インプライズ）で開発され、[コードギア](../Page/コードギア.md "wikilink")へ移管、同社の買収に伴って現在へ至る。ボーランド社の時代は、****（ボーランド C++ビルダー; **BCB**）とも呼ばれていた。

## 概要

FireMonkey や **[Visual Component Library](../Page/Visual_Component_Library.md "wikilink")** (VCL) を利用するIDEを持つ[Delphi](../Page/Delphi.md "wikilink")のC++版である。C++[コンパイラ](../Page/コンパイラ.md "wikilink")には、そのための拡張が施されている。また統合開発環境は[Delphi](../Page/Delphi.md "wikilink")とほぼ同一である。

### 長所

  - [プログラムをC](../Page/プログラム_\(コンピュータ\).md "wikilink")/C++で書ける。
  - 単一のコードベース、単一のプロジェクトチームで[マルチプラットフォーム](../Page/クロスプラットフォーム.md "wikilink") ([Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink"), [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink"), [iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink"), [Android](../Page/Android.md "wikilink")) のサポートが実現できる。
  - [RADであり](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")、かつ[Visual Basicの様な](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")[ランタイムライブラリ](../Page/ランタイムライブラリ.md "wikilink")の別途配布も不要（[実行ファイル](../Page/実行ファイル.md "wikilink")に結合可能）である。
  - Qtなどと比べランタイムライブラリを結合しても実行ファイルは小さい。
  - dynamic_castの展開が[Visual C++と比較して高速である](../Page/Microsoft_Visual_C++.md "wikilink")\[1\]。
  - ANSI C、ISO C、[C99](../Page/C99.md "wikilink")、[C11](https://ja.wikipedia.org/wiki/C11_\(C言語\) "wikilink")、ISO C++、C++98、[C++0x TR1](../Page/C++_Technical_Report_1.md "wikilink")、そして[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")といったC/C++標準に準拠している。(XE 4)
  - プロパティのような[Delphi](../Page/Delphi.md "wikilink")由来の[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")言語向け拡張機能を使用でき、標準のC++よりも[GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[アプリケーション開発環境](../Page/アプリケーションソフトウェア.md "wikilink") (RAD) との親和性が高い。
  - 無料版がある。
  - 日本語版があり日本語ヘルプなどの日本語情報が充実している。

### 短所

  - 。

  - ランタイムライブラリを結合すると実行ファイルが大きくなる。（バージョン5の場合、最低でも500Kバイト程度）\<\!-- Visual C++でもライブラリをスタティックリンクすると相応にファイルサイズが増大するので、理不尽な増大でないかぎり特に短所と呼べるほどのものではないのでは？

何と比べて実行ファイルが大きくなる? むしろ小さいのが長所のはずだが。 --\>

  - [Windowsの開発環境としては](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") ([Visual C++](../Page/Microsoft_Visual_C++.md "wikilink")) よりもマイナーである。

  - 。

## 歴史

### C++ Builder 1から5まで

最初の C++ Builder は[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")[2月26日](../Page/2月26日.md "wikilink")にリリースされた (日本語版の出荷開始日は[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")[3月28日](../Page/3月28日.md "wikilink"))。[Delphi](../Page/Delphi.md "wikilink")とバージョン番号を合わせた結果、C++ Builder 2は欠番となっている。

### C++ Builder 6

[2001年](../Page/2001年.md "wikilink")。GUIライブラリにVCLに加えクロスプラットフォームの[Component Library for Cross Platform(CLX)を追加した](../Page/Component_Library_for_Cross_Platform.md "wikilink")。CLXはWindowsと[GNU/Linux](https://ja.wikipedia.org/wiki/GNU/Linux "wikilink")の二つのプラットフォームをサポートするがCLXを用いたGNU/Linuxの開発ができたのは別製品の[Kylix](../Page/Kylix.md "wikilink")のみ。CLXはC++ Builderではこのバージョンのみで以降のバージョンに採用されることはなかった。

### C++ BuilderX 路線

C++ Builderが使用するVCLは、[Delphi](../Page/Delphi.md "wikilink")において7、8、2005と進化した。また[Delphi](../Page/Delphi.md "wikilink")は、[リファクタリング機能などを備えた新統合開発環境](../Page/リファクタリング_\(プログラミング\).md "wikilink")「Galileo」に移行した。しかし、これらに対応するC++ Builderは発表されなかった。BorlandのC++統合開発環境は、従来のWindowsに加えて[Linux](../Page/Linux.md "wikilink")クライアントサイド市場を狙った「**Kylix3**」の失敗により、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")製の「**C++ BuilderX**」（シープラスプラスビルダーテン）が担うことになったからである。これはRADではなく、統合環境版のBorland C++ Compilerとも言うべきもので、[携帯電話](../Page/携帯電話.md "wikilink")などの組み込み、[サーバ](../Page/サーバ.md "wikilink")サイド市場を狙ったものである。結局、この路線は失敗に終わった。無償版の配布も終了した。

### 復興運動からTurbo C++まで

[2004年](../Page/2004年.md "wikilink")にC++ Builder ユーザは Paul Gustavson を中心として、ボーランドに公開質問状を送り、新製品の開発を促した。これに対して同社は「C++ Builderコミュニティへの公開書簡」\[2\]で、これを了承した。

[2005年](../Page/2005年.md "wikilink")[12月21日](../Page/12月21日.md "wikilink")に「Borland Developer Studio 2006」が発売された。これには約束どおり「C++ Builder 6」の後継製品である、「**C++ Builder 2006**」（内部バージョン: 10.0）が統合された。

[2006年](../Page/2006年.md "wikilink")に「Turbo C++」が発表された。これは「Borland Developer Studio 2006」上で他の言語と統合されていた「C++ Builder 2006」を単体化した物である。無料版も提供された。この無償公開版は、**Turbo C++ Explorer**（内部バージョン: 10.0）という名称にて同社のサイトより配布が行なわれていたが2009年8月26日に日本語版の頒布を終了した。Turbo C++は、C++ Builderとは異なり、プログラミング言語を1つだけしか選べない。

### C++ Builder 2007

[2007年](../Page/2007年.md "wikilink")[5月15日](../Page/5月15日.md "wikilink")に、「**C++ Builder 2007**」（内部バージョン: 11.0）が発表された。

[Windows Vistaに対応した](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。[2007年](../Page/2007年.md "wikilink")[9月6日](../Page/9月6日.md "wikilink")には、C++ Builder 2007 を含む統合版「CodeGear [RAD Studio](https://ja.wikipedia.org/wiki/RAD_Studio "wikilink") 2007」が発表された。

### C++ Builder 2009

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[8月26日](../Page/8月26日.md "wikilink")に「**C++ Builder 2009**」（コードネーム:Tiburón、内部バージョン: 12.0）が発表された。

C++ Builder 2009から文字列が全面的に[Unicode](../Page/Unicode.md "wikilink")文字列に置き換わった。

### C++ Builder 2010

[2009年](../Page/2009年.md "wikilink")[8月25日](../Page/8月25日.md "wikilink")に「**C++ Builder 2010**」（内部バージョン: 14.0）が発表された。

新しいIDE機能/デバッグツールにより開発をさらに効率化。コーディング作業やデバッグ作業をさらにスピードアップ可能である。タッチ対応アプリケーションの開発をサポート。タブレットやタッチパッド、POSやATM向けのアプリケーションをビジュアルに開発可能である。Firebirdサポート、DataSnapなど、広範なデータベース、アーキテクチャ、プロトコルに対応する。

### C++ Builder XE

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[9月2日](../Page/9月2日.md "wikilink")に「**C++ Builder XE**」（内部バージョン: 15.0）が発表された。

XEは「Cross Platform Edition」の略である。名称通りクロスプラットフォーム開発環境を目指して開発が進められたものの、不完全であったため見送られている。

[2011年](../Page/2011年.md "wikilink")[2月1日](../Page/2月1日.md "wikilink")にはStarterエディションが追加発表された。「Turbo C++」以来のエントリー向けエディションであり、無償ではないがコンポーネントのインストールが可能、1,000 USドルを超えない範囲であれば商用利用可能など、制限は大幅に緩和されている。ただし、Starterには旧C++ Builderのライセンスは付属しない。また、同時利用は同一サブネット内において5ライセンスまでとされている。このため教室での利用は向かないとされており、アカデミック版の提供はない。税別価格は18,000円だが、同社または他社の開発ツールユーザーは税別14,000円でアップグレードできる。[Delphi](../Page/Delphi.md "wikilink") Starterとの併用はできず、[RAD StudioにもStarterは提供されない](https://ja.wikipedia.org/wiki/RAD_Studio "wikilink")。

アカデミック版を除き、C++Builder 6、2007、2009、2010のライセンスが付属する\[3\]\[4\]。

### C++ Builder XE 2

[2011年](../Page/2011年.md "wikilink")[9月1日](../Page/9月1日.md "wikilink")に「**C++ Builder XE 2**」（内部バージョン: 16.0）が発表された。

新たに **FireMonkey** フレームワークを導入したことにより、HD や 3D に対応した高品質な[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink") (UI) の設計や、[Mac OS X](https://ja.wikipedia.org/wiki/macOS "wikilink") ([Intel x86](../Page/X86.md "wikilink")) 向けのマルチプラットフォームアプリケーションの開発が可能になった。また、製品エディションとしてEnterpriseとArchitectの間にUltimateが追加された。

搭載されるコンパイラはBCC32（Windows 32ビット）、BCCOSX (Mac OS X) の2つとなった。

Starterとアカデミック版を除き、C++Builder 6、2007、2009、2010、XE のライセンスが付属する。

### C++ Builder XE 3

[2012年](../Page/2012年.md "wikilink")[9月4日](../Page/9月4日.md "wikilink")に「**C++ Builder XE 3**」（内部バージョン: 17.0）が発表された\[5\]。

新たに「Metropolis UI」を導入したことにより、タッチ対応、ライブタイルサポートなどを搭載した[Windows 8デスクトップアプリケーションの開発が可能になった](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")。ただし[WinRTには対応しない](https://ja.wikipedia.org/wiki/Windowsランタイム "wikilink")

[2012年](../Page/2012年.md "wikilink")[12月10日](../Page/12月10日.md "wikilink")にリリースされたアップデートにより、[Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")、[LLVM](../Page/LLVM.md "wikilink")に対応した[64ビット](../Page/64ビット.md "wikilink")コンパイラが追加提供された\[6\]。ただし、[32ビット](../Page/32ビット.md "wikilink")コンパイラは従来通りBCC32なため、Win32 / Win64でソースコードに互換性がない事もあった。この問題の解消には後述する「[C++ Builder 10 Seattle](https://ja.wikipedia.org/wiki/#C++_Builder_10_Seattle "wikilink")」の登場を待たなくてはならなかった。

搭載されるコンパイラはBCC32（Windows 32ビット）、BCC64（Windows 64ビット / Clang）、BCCOSX (OS X) の3つとなった。

Starterとアカデミック版を除き、C++Builder 6、2007、2009、2010、XE、XE2 のライセンスが付属する。

### C++ Builder XE 4

[2013年](../Page/2013年.md "wikilink")[4月22日](../Page/4月22日.md "wikilink")に「**C++ Builder XE 4**」（内部バージョン: 18.0）が発表された\[7\]。

前バージョンのXE3 から7ヶ月でのバージョンアップとなったため XE3 からのバージョンアップ料金はキャンペーン価格ながら格安の 6,000円となった（Professional版の場合）。

Starterとアカデミック版を除き、C++Builder 6、2007、2009、2010、XE - XE3 のライセンスが付属する。

### C++ Builder XE 5

[2013年](../Page/2013年.md "wikilink")[9月12日](../Page/9月12日.md "wikilink")に「**C++ Builder XE 5**」（内部バージョン: 19.0）が発表された\[8\]。

[2013年](../Page/2013年.md "wikilink")[12月11日](../Page/12月11日.md "wikilink")にリリースされたアップデート2により、[iOS開発機能が導入された](https://ja.wikipedia.org/wiki/IOS_\(アップル\) "wikilink")\[9\]。Professional版でモバイル開発 (iOS) を行うには「**Mobile Add-On Pack**」を別途購入する必要がある。

搭載されるコンパイラはBCC32（Windows 32ビット）、BCC64（Windows 64ビット / Clang）、BCCOSX (OS X)、BCCIOSARM (iOS デバイス用 / Clang) の4つとなった。

Starter版を除き、C++Builder 6、2007、2009、2010、XE - XE4 のライセンスが付属する。

### C++ Builder XE 6

[2014年](../Page/2014年.md "wikilink")[4月16日](../Page/4月16日.md "wikilink")に「**C++ Builder XE 6**」（内部バージョン: 20.0）が発表された\[10\]。

このバージョンから対応プラットフォームに[Android](../Page/Android.md "wikilink")が追加された。これにより、Windows 7/8/8.1（32ビット/64ビット）、iOS (iPhone/iPad)、Android（Google Glassを含む）向けのアプリケーション開発が可能となった。モバイル開発 ([iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink") / Android) を行う場合、Professional版ではMobile Add-On Packを別途購入する必要がある。

搭載されるコンパイラはBCC32（Windows 32ビット）、BCC64（Windows 64ビット / Clang）、BCCOSX (OS X)、BCCIOSARM（iOS デバイス用 / Clang）, BCCAARM (Android / Clang) の5つとなった。

Starter版を除き、C++Builder 6、2007、2009、2010、XE - XE5 のライセンスが付属する。

### C++ Builder XE 7

[2014年](../Page/2014年.md "wikilink")[9月2日](../Page/9月2日.md "wikilink")に「**C++ Builder XE 7**」（内部バージョン: 21.0）が発表された\[11\]。

Starter版を除き、C++Builder 6、2007、2009、2010、XE - XE6 のライセンスが付属する。

### C++ Builder XE 8

[2015年](../Page/2015年.md "wikilink")[4月7日](../Page/4月7日.md "wikilink")に「**C++ Builder XE 8**」（内部バージョン: 22.0）が発表された\[12\]。

[iOSデバイス用](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")64ビットコンパイラが追加されている。モバイル開発 ([iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink") / [Android](../Page/Android.md "wikilink")) を行う場合、Professional版ではMobile Add-On Packを別途購入する必要がある。

搭載されるコンパイラはBCC32（Windows 32ビット）、BCC64（Windows 64ビット / Clang）、BCCOSX (OS X)、BCCIOSARM（iOSデバイス用32ビット / Clang）、BCCIOSARM64（iOSデバイス用64ビット / Clang）、BCCAARM (Android / Clang) の6つとなった。

Starter版を除き、C++Builder 6、2007、2009、2010、XE - XE7 のライセンスが付属する。

### C++ Builder 10 Seattle

[2015年](../Page/2015年.md "wikilink")[9月1日](../Page/9月1日.md "wikilink")に「**C++ Builder 10 Seattle**」（内部バージョン: 23.0）が発表された\[13\]。

[Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")ベースの新しいWin32用コンパイラが追加された。これにより、Win32 / Win64でほぼ同一のコードを書く事ができるようになった。従来のWin32用コンパイラであるBCC32も利用する事ができる。

搭載されるコンパイラはBCC32（Windows 32ビット）、BCC32C（Windows 32ビット / Clang）、BCC64（Windows 64ビット / Clang）、BCCOSX (OS X)、BCCIOSARM（iOS デバイス用 32ビット / Clang）、BCCIOSARM64（iOSデバイス用64ビット / Clang）、BCCAARM (Android / Clang) の7つとなった。

Starter版を除き、C++Builder 6、2007、2009、2010、XE - XE8 のライセンスが付属する。

### C++ Builder 10.1 Berlin

[2016年](../Page/2016年.md "wikilink")[4月20日](https://ja.wikipedia.org/wiki/4月20日 "wikilink")に「**C++ Builder 10.1 Berlin**」 (コードネーム: BigBen、内部バージョン: 24.0) が発表された\[14\]。

[Android](../Page/Android.md "wikilink") 6.0、[iOS](https://ja.wikipedia.org/wiki/IOS_\(アップル\) "wikilink") 10、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") 10.12 (Sierra) アプリケーション開発に対応。[FireMonkey](https://ja.wikipedia.org/wiki/FireMonkey "wikilink") のフォームデザイナも独立表示可能になった (デフォルトでは埋め込みデザイナ)。インストーラの改良により、インストールオプションによってはインストール時間が大幅に短縮されるようになった。このバージョンからUltimateエディションが廃止されている。

[2016年](../Page/2016年.md "wikilink")[8月22日](../Page/8月22日.md "wikilink")以降、Starter Edition が無償で入手できるようになっている\[15\]。[2006年](../Page/2006年.md "wikilink")の **Turbo C++ Explorer** 以来、10 年ぶりの無償版である。また、Starter Edition は Turbo Explorer とは異なり、複数のパーソナリティ (言語) が共存できるため、C++Builder と [Delphi](../Page/Delphi.md "wikilink") を同じ環境で利用する事が可能となっている。コンポーネントのインストールにも制限がない。

Starter 版を除き、C++Builder 6、2007、2009、2010、XE - XE8、10 Seattle のライセンスが付属する。

Update 2 で Windows 10 の Anniversary Update に正式対応したため、Update 2 には「**Anniversary Edition**」という名称がついている。

### C++ Builder 10.2 Tokyo

[2017年](../Page/2017年.md "wikilink")[3月22日](../Page/3月22日.md "wikilink")に「**C++ Builder 10.2 Tokyo**」（コードネーム: Godzilla、内部バージョン: 25.0）が発表された\[16\]。

[Clang](https://ja.wikipedia.org/wiki/Clang "wikilink") ベースのコンパイラにおいてパフォーマンスが向上している。また、インストーラの改良により、インストール時間が大幅に短縮されるようになった。

[2017年](../Page/2017年.md "wikilink")[12月13日](https://ja.wikipedia.org/wiki/12月13日 "wikilink")にリリースされた Release 2 (10.2.2) において、Enterprise 以上の SKU で **RAD Server** の単一サイト/単一サーバー配置ライセンスが含まれるようになった。

[2018年](../Page/2018年.md "wikilink")[3月14日](https://ja.wikipedia.org/wiki/3月14日 "wikilink")にリリースされた Release 3 において、Professional Edition にモバイルサポートが追加された。従来、Mobile Add-On Packとして別売されていたものが統合された形になる。また BCC32X という Win32用コマンドラインコンパイラが新たに追加された。これは下位互換性のためにコマンドラインインターフェイスが非互換だった BCC32C を他のコンパイラ (bcc64、bccios32、bccios64、bccaarm) と共通にしたものである。

搭載されるコンパイラはBCC32（Windows 32ビット）、BCC32C（Windows 32ビット / Clang）、BCC32X（Windows 32ビット / Clang）、BCC64（Windows 64ビット / Clang）、BCCOSX (OS X)、BCCIOSARM（iOS デバイス用 32ビット / Clang）、BCCIOSARM64（iOSデバイス用64ビット / Clang）、BCCAARM (Android / Clang) の8つとなった。

[2018年](../Page/2018年.md "wikilink")[7月19日](../Page/7月19日.md "wikilink")に、従来の Professional Edition 相当を無償化した「**C++Builder Community Edition**」がリリースされた。Windows 64bit, macOS, iOS, Android 向けの開発が可能となっている。無償版 Starter Edition とは異なり、「**Delphi Community Edition**」と同時にインストールする事はできない。

Starter / Community 版を除き、C++Builder 6、2007、2009、2010、XE - XE8、10 Seattle、10.1 Berlinのライセンスが付属する。

### C++ Builder 10.3 Rio

[2018年](../Page/2018年.md "wikilink")[11月22日](https://ja.wikipedia.org/wiki/11月22日 "wikilink")に「**C++ Builder 10.3 Rio**」（コードネーム: Carnival、内部バージョン: 26.0）が発表された\[17\]。同日、Community Edition も更新されている。

Starter Edition は廃止された。Professional Edition にあった別売の FireDAC Client/Server Add-on Pack も廃止され、フル機能の FireDAC を利用するためには Enterprise Edition 以上の SKU が必要となった。

Windows 用 [32ビット](../Page/32ビット.md "wikilink") コンパイラ (BCC32X, BCC32C) にて [C++17](https://ja.wikipedia.org/wiki/C%2B%2B17 "wikilink") をサポートするようになった。

[2019年](../Page/2019年.md "wikilink")[7月19日](../Page/7月19日.md "wikilink")にリリースされた Release 2 (10.3.2) において、Windows 用 [64ビット](../Page/64ビット.md "wikilink") コンパイラ (BCC64) にて [C++17](https://ja.wikipedia.org/wiki/C%2B%2B17 "wikilink") をサポートするようになった。[Language Server Protocol](https://ja.wikipedia.org/wiki/Language_Server_Protocol "wikilink") (LSP) に対応し、コード補完 (Code Insight) の性能が向上した。

Starter / Community 版を除き、C++ Builder 6、2007、2009、2010、XE - XE8、10 - 10.2 のライセンスが付属する。

### C++ Builder 10.4 Sydney

[2020年](../Page/2020年.md "wikilink")[5月27日](../Page/5月27日.md "wikilink")に「**C++ Builder 10.4 Sydney**」（コードネーム: Denali、内部バージョン: 27.0）が発表された\[18\]。同日の Community Edition リリースはなかった。

LLDBベースの新しいWin64 C++デバッガが追加された。数多くの C++ ライブラリが移植されており、追加で GetIt パッケージマネージャからもインストールできる。

macOS Catalina において32ビットアプリが動作しなくなったため、ターゲットプラットフォームから "macOS 32ビット" が選べなくなり、BCCOSX が付属しなくなった。同様に "iOS デバイス 32ビット" も選択できなくなっているが、BCCIOSARM は含まれている。これにより、C++ Builder による macOS 開発は macOS 64ビットコンパイラの登場を待たねばならなくなった。

搭載されるコンパイラはBCC32（Windows 32ビット）、BCC32C（Windows 32ビット / Clang）、BCC32X（Windows 32ビット / Clang）、BCC64（Windows 64ビット / Clang）、BCCIOSARM（iOS デバイス用 32ビット / Clang）、BCCIOSARM64（iOSデバイス用64ビット / Clang）、BCCAARM (Android 32ビット/ Clang) の7つとなった。

Community 版を除き、C++ Builder 6、2007、2009、2010、XE - XE8、10 - 10.3 のライセンスが付属する。

### 今後のC++Builder

今後、Linux ([64ビット](../Page/X64.md "wikilink")) コンパイラの追加を盛り込む予定であると、[2018年](../Page/2018年.md "wikilink")のロードマップにてアナウンスされている\[19\]。

## C++ Builder Community Edition

10.2 Tokyo より完全無料版の **Community Edition**\[20\] が提供されている。

有料の C++ Builder Professional と同等の機能を持ち、従来の Win32 アプリケーションのみならず Windows 64bit, macOS, iOS, Android の開発が可能となっている。

### 過去の無料版

  - C++ Builder X Personal が無料で提供されていた。
  - C++ Builder 2006 Update2 相当の Turbo C++ for Win32 Explorer が無料で提供されていた。
  - C++ Builder 10.1 Berlin から Starter Edition が無料で提供されていた。
  - C++ Builder 10.2 Tokyo から Community Edition が無料で提供されている。

## GUIライブラリ

### VCL (Visual Component Library)

C++ Builderの全バージョン、全てのエディションで採用されているWindows専用のGUIライブラリである。

  - 高機能でC++ BuilderのメインのGUIライブラリとして位置づけられる。
  - Windows専用だけあってWindows固有のプログラミングテクニックがそのまま通用することが多い。
  - XEからIEコンポーネント(TWebBrowserなど)の高度な処理に必要なATLライブラリが付属されなくなっている。
  - XE8までは2009または2010のバージョンからATLライブラリをコピーして使うことはできる。
  - VCLは[Delphi](../Page/Delphi.md "wikilink")([Object Pascal](../Page/Object_Pascal.md "wikilink"))で記述されている。

### FireMonkey

C++ BuilderではXE2から採用されているクロスプラットフォームのGUIライブラリである。

  - FMXとも呼ばれる。
  - Windows、Mac OS、Android、iOS(iPhone、iPad)と幅広く対応するがGNU/Linuxには対応しない。
  - VCLとの互換性が低く、VCL間の移植は困難。
  - VCLと比べると機能は十分とはいえずVCLの完全な代替にはならない。
  - VCLと比べるとWindows固有の機能を呼び出すことが難しい場合がある。
  - [Delphi](../Page/Delphi.md "wikilink") と異なり、C++ BuilderでiOSの開発をする場合はiOSシミュレーターが使えない (シミュレータ用コンパイラが存在しない)。
  - FireMonkeyは[Delphi](../Page/Delphi.md "wikilink")(Object Pascal)で記述されている。

### CLX (Component Library for Cross Platform)

[Microsoft WindowsとGNU](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")/Linuxのクロスプラットフォームの古いGUIライブラリである。

  - C++ Builder 6と[Delphi](../Page/Delphi.md "wikilink") 6とKylixの全バージョンで採用された。
  - 長らく前に開発は中止され現在のバージョンでは採用されていない。
  - 現在でも　Professional 以上の SKU の最新バージョンを購入することによりC++ Builder 6とCLXを入手することが可能。
  - QtベースのVCLライクなGUIライブラリであり、FireMonkeyと比べると格段とVCLとの互換性が高い。
  - VCLにない機能もあるため現在でもWindowsで使う利点がある。
  - VCLと比べるとWindows固有の機能を呼び出すことが難しい場合がある。
  - C++ Builder 6と[Delphi](../Page/Delphi.md "wikilink") 6のVCLは[Unicode](../Page/Unicode.md "wikilink")に全く対応していなかったがCLXは一部分ながら対応している。
  - C++ Builder 6とCLXの組み合わせで現在の最新Windows向けの開発も可能。
  - GNU/LinuxはKylix発売当時と現在では大きく仕様が変わっているためKylixで現在のGNU/Linux向けの開発はできない。
  - 従って現在はWindows専用のようになっておりクロスプラットフォーム性は失われている。
  - WindowsとGNU/Linuxではコンパイラが違いCLXの仕様も少し違っていたためKylixのC++とのソース互換性はそれほど高くなかった。
  - CLXのベース部分はQtでありQtはC++で作られている。

## その他

  - [2000年](../Page/2000年.md "wikilink")に **Borland C++ Compiler (BCC) 5.5** が公開された。これは[コンパイラ](../Page/コンパイラ.md "wikilink")、[リンケージエディタ](../Page/リンケージエディタ.md "wikilink")、標準ライブラリおよび[開発ツールの無料版である](https://ja.wikipedia.org/wiki/プログラミングツール "wikilink")。開発はRADではなく、コマンドラインから行う。当時、Windows用の無償のC/C++コンパイラは、ほかに[GCCほどしかなく](../Page/GNUコンパイラコレクション.md "wikilink")、Borland C++が広く知られることになった。BCC 5.5は 2018 年現在もエンバカデロのサイトから無償ダウンロードして使用できる\[21\]が、保証やサポートはなされていない。
  - C++ Builderのでは[MFCや](../Page/Microsoft_Foundation_Class.md "wikilink")[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")などもサポートしている。
  - バージョンやパッケージの種類によっては[Delphi](../Page/Delphi.md "wikilink")などの[CD-ROM](../Page/CD-ROM.md "wikilink")も付属する。
  - [Delphi](../Page/Delphi.md "wikilink")やC++Builderの開発者の一部は[マイクロソフト](../Page/マイクロソフト.md "wikilink")に移籍して、[Visual C\#などを開発している](../Page/Microsoft_Visual_C_Sharp.md "wikilink")。
  - [2016年](../Page/2016年.md "wikilink")に無償版である **Free C++ Compiler** が公開された。[Clang](https://ja.wikipedia.org/wiki/Clang "wikilink") ベースで、最新のものは [C++17](https://ja.wikipedia.org/wiki/C++17 "wikilink") に対応している\[22\]。
  - [2018年](../Page/2018年.md "wikilink")に無償版である **C++ Builder Community Edition** が公開された\[23\]。Professional Edition 相当。

## 脚注

<references />

## 関連項目

  - [Appmethod](https://ja.wikipedia.org/wiki/Appmethod "wikilink")
  - [C\#](../Page/C_Sharp.md "wikilink")
  - [C++](../Page/C++.md "wikilink")
  - [Delphi](../Page/Delphi.md "wikilink")
  - [Kylix](../Page/Kylix.md "wikilink")
  - [Rapid Application Development](../Page/Rapid_Application_Development.md "wikilink")
  - [RAD Studio](https://ja.wikipedia.org/wiki/RAD_Studio "wikilink")
  - [Turbo C](https://ja.wikipedia.org/wiki/Turbo_C "wikilink")
  - [Turbo Pascal](../Page/Turbo_Pascal.md "wikilink")
  - [エンバカデロ・テクノロジーズ](https://ja.wikipedia.org/wiki/エンバカデロ・テクノロジーズ "wikilink")
  - [コードギア](../Page/コードギア.md "wikilink")
  - [ボーランド](../Page/ボーランド.md "wikilink")

## 外部リンク

  - [Embarcadero Technologies](http://www.embarcadero.com/jp/)
      - [C++Builder from Embarcadero](http://www.embarcadero.com/jp/products/cbuilder)
      - [Turbo C++](http://www.turboexplorer.com/jp/cpp/)
      - [Borland C++ Compiler (BCC) 5.5](https://downloads.embarcadero.com/item/24778)
      - [Free C++ Compiler (BCC32C)](https://www.embarcadero.com/jp/free-tools/ccompiler)
      - [C++Builder Community Edition](https://embarcadero.com/jp/products/cbuilder/starter)

[Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink") [Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:コードギアの開発ツール](https://ja.wikipedia.org/wiki/Category:コードギアの開発ツール "wikilink")

1.
2.
3.  アップグレードした場合、元のバージョンと同じバージョンのライセンスの重複取得はできない。
4.  旧バージョンライセンスの取得は、購入180日以内に行う必要がある。
5.
6.  [EmbarcaderoがDelphiとC++ Builderをアップデートし、 HTML5 Builderをリリース。](http://www.infoq.com/jp/news/2012/09/Delphi)
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19. <https://community.embarcadero.com/article/news/16639-rad-studio-2018-8>
20.
21.
22.
23.