> この記事は[Cocoa](https://ja.wikipedia.org/wiki/Cocoa)から翻訳されています。


**Cocoa**は、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")用の[アプリケーションを構築するための](../Page/アプリケーションソフトウェア.md "wikilink")[フレームワーク](../Page/アプリケーションフレームワーク.md "wikilink") ([API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")) であり、macOSのアプリケーション開発環境の中で主要な物\[1\]の一つ。

[NeXTSTEP](../Page/NEXTSTEP.md "wikilink") ([OPENSTEP](../Page/OPENSTEP.md "wikilink")) のAPIをベースとしており、macOS向けのネイティブ・アプリケーションを構築するのに適している。逆に、これまでの[Classic Mac OS](../Page/Classic_Mac_OS.md "wikilink")（Mac OS 9.xまでのMac OS）向けのアプリケーションを構築する目的で使用することはできない。

一般に、Cocoaを利用したアプリケーションを構築する場合、[アップルから提供される統合開発環境である](../Page/アップル_\(企業\).md "wikilink")[Xcode](../Page/Xcode.md "wikilink")（Project Builderの後継）及び [Interface Builderを使用する](../Page/Interface_Builder.md "wikilink")。なお、[iOSの主要フレームワークである](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")[Cocoa Touchは](https://ja.wikipedia.org/wiki/Cocoa_Touch "wikilink")、Cocoaをタッチインターフェースを前提に作り直したもので、開発環境もほぼ同様のものを用いる。

## アーキテクチャ

Cocoaは[Objective-C](../Page/Objective-C.md "wikilink")をコア言語とする[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")フレームワークである。

[OS機能や](../Page/オペレーティングシステム.md "wikilink")[コレクション](../Page/コンテナ_\(データ型\).md "wikilink")[クラスなどをまとめたサービス層であるFoundationと](../Page/クラス_\(コンピュータ\).md "wikilink")、主に[GUIパーツの集合であるAppKitの二層構造を成し](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink")、狭義ではこの二つをCocoaフレームワークと呼ぶ。厳密な区分ではないが、AddressBook APIなど、周辺サービスを提供するObjective-Cで記述されたフレームワークを広義にCocoaと呼ぶこともある。

基本構造は[MVCアーキテクチャで](../Page/Model_View_Controller.md "wikilink")、他に[委譲](../Page/委譲.md "wikilink")（デリゲート）、ファクトリ、[Chain of Responsibility パターンなどが多用される](../Page/Chain_of_Responsibility_パターン.md "wikilink")。抽象度の高い下位サービスと柔軟なViewの組み合わせが特に強力で、そのままの利用から高度なカスタマイズまで幅広い適応力を持っている。[Mac OS X v10.3ではM](../Page/Mac_OS_X_v10.3.md "wikilink")-V間の同期を自動化する[Cocoa Binding](https://ja.wikipedia.org/wiki/Cocoa_Binding "wikilink")（Controller層）、[Mac OS X v10.4ではモデリングを自動化する](../Page/Mac_OS_X_v10.4.md "wikilink")[Core Dataが実装され](https://ja.wikipedia.org/wiki/Core_Data "wikilink")、さらに記述の抽象度は上がっている。

Cocoaそれ自体は純粋な機能セットであり、Objective-C実行環境との通信を確立すれば他の[言語からも利用が可能になる](../Page/プログラミング言語.md "wikilink")。これにより現在では[Java](https://ja.wikipedia.org/wiki/Java "wikilink")/[Perl](../Page/Perl.md "wikilink")/[Ruby](../Page/Ruby.md "wikilink")/[Python](../Page/Python.md "wikilink")/[Common Lispなど](../Page/Common_Lisp.md "wikilink")、各種の[コンパイラ](../Page/コンパイラ.md "wikilink")・[スクリプト言語](../Page/スクリプト言語.md "wikilink")との言語ブリッジが確立している(これらの言語内でクラスを定義してObjective-C側から呼び出すことも可能である)。しかし[Cや](../Page/C言語.md "wikilink")[C++](../Page/C++.md "wikilink")からは直接 Cocoa を使うことはできないため、macOSでは旧来のC/C++プログラマのためにCocoaとほとんど等価な機能をもった[Carbon](../Page/Carbon.md "wikilink") APIも用意されている。

## その他

Cocoaはコードネーム『Rhapsody』での[Yellow Boxにあたる](https://ja.wikipedia.org/wiki/Yellow_Box "wikilink")。

NEXTSTEP由来のCocoaは旧Mac OSの[Toolbox](https://ja.wikipedia.org/wiki/Toolbox "wikilink") API由来の[Carbon](../Page/Carbon.md "wikilink")と必ずしも対立するものではない。Carbon APIをラッピングした物、[Core Foundationとして共有基盤へ実装を移した物など](../Page/Core_Foundation.md "wikilink")、単純にインタフェースとしてCocoa側に出現する物も少なくない(ただし、Objective-Cは一般にCよりも柔軟性に優れており、インタフェースの差違は大きい)

## 脚注

<references/>

## 関連項目

  - [GNUstep](../Page/GNUstep.md "wikilink")

[Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")

1.  他に[Carbon](../Page/Carbon.md "wikilink")、[POSIX](../Page/POSIX.md "wikilink")、[X11](../Page/X_Window_System.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")がある