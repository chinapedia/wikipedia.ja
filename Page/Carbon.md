> この記事は[Carbon](https://ja.wikipedia.org/wiki/Carbon)から翻訳されています。


**Carbon**（カーボン）は、[Classic Mac OSの](../Page/Classic_Mac_OS.md "wikilink")[Toolbox](https://ja.wikipedia.org/wiki/Toolbox "wikilink") [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") (Application Programming Interface) を[Mac OS X用に整理](https://ja.wikipedia.org/wiki/macOS "wikilink")・移植した[APIであり](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、Classic Mac OS用アプリケーションをMac OS X向けに移植しやすくするために開発された。

## 概要

[QuickTime](../Page/QuickTime.md "wikilink")チームがAPIをMac OS Xに移植するために互換レイヤーを作成したものが元型となっている。それが[スティーブ・ジョブズ](../Page/スティーブ・ジョブズ.md "wikilink")の目に留まり、汎用の互換フレームワークのアイディアとして採用された。Toolbox APIの中で明らかにレガシーなもの、あまり使われていないものを廃し、また内部構造が[32ビット](../Page/32ビット.md "wikilink")を前提として再設計されている（Toolboxは[16ビット](../Page/16ビット.md "wikilink")コードで、[PowerPC](../Page/PowerPC.md "wikilink")の性能の足枷となっていた）。

Carbon APIを利用した[アプリケーションのことを](../Page/アプリケーションソフトウェア.md "wikilink")**Carbonアプリケーション**と呼ぶ。[Cocoa](../Page/Cocoa.md "wikilink")は同じ Mac OS Xに搭載されているほぼ等価な機能をもつ API であるが、Cocoa APIを使うためには[Objective-C](../Page/Objective-C.md "wikilink")のコードを書かなければならないのに対して、Carbon API は旧来のインターフェイスを持っておりC/C++からも使うことができる。基本的にToolboxとソースコード互換を目指しており、単に移植を行なうだけであれば、それほど大きな設計変更は必要ない。

Carbonアプリケーションには、

  - 一つのバイナリでMac OS XでもClassic Mac OSでも実行できる『**PEF Carbon**』
  - Mac OS X専用の『**[Mach-O](https://ja.wikipedia.org/wiki/Mach-O "wikilink") Carbon**』

の2種類が存在する。 PEFとは[Preferred Executable Formatのこと](https://ja.wikipedia.org/wiki/Preferred_Executable_Format "wikilink")。CFM（Code Fragment Manager） Carbonともいう。PEFは従来から使用されてきたフォーマットであるため、新旧両方の[Mac OSで動かせる](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")。

Mach-O CarbonはMac OS X用に最適化されているのでCFM Carbonより幾分高速に動作する 。また、[Quartz](../Page/Quartz.md "wikilink")をはじめとするMac OS X特有の[APIを利用するためには](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、Mach-O形式が最も適する。このフォーマットはdyldとも呼ばれる。 Mac OS Xが普及してしばらくはCFM Carbonが大半だったが、開発環境が最適化されていくにつれてMach-O Carbonがほとんどとなってきた。（[Xcode](../Page/Xcode.md "wikilink")の利用による）Mach-O化は[Universal Binary化には必須である](https://ja.wikipedia.org/wiki/Universal_Binary "wikilink")。

※CFMやMach-Oは[ABI](../Page/Application_Binary_Interface.md "wikilink") (Application Binary Interface) のことで、[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") (Application Programming Interface) とは無関係。

Carbonにより、旧来のMac OSのアプリケーションのMac OS Xへの移植が容易になり、新旧両方のオペレーティングシステムでアプリケーションの実行が出来るため、最も普及している。CarbonアプリケーションはMac OS Xにもネイティブになり、その多大なる恩恵を受けることが出来る。 ただし、CFM Carbonのアプリケーションでも、実行にはCarbonLibと呼ばれる[機能拡張書類](https://ja.wikipedia.org/wiki/機能拡張書類 "wikilink")が必要であり、これがなければ旧来のMac OSでは動作しない。逆に言えば、CarbonLibがあればMac OS 8.6から最新のMac OS X上で実行できるようになる。

CFM Carbonでは一つのプログラムで新旧両方のOSで実行できるが、CarbonLibが欠かせない。Mach-O Carbonは、一つのプログラムだけの場合、Mac OS X以外では実行できない。これらの欠点を補うため、Mac OS 9から導入された[アプリケーションパッケージ](../Page/アプリケーションパッケージ.md "wikilink")を利用して一つの[フォルダ](https://ja.wikipedia.org/wiki/フォルダ "wikilink")の中に CarbonアプリケーションとClassicアプリケーション（Mac OS 9まででしか動作しないアプリケーション）の両方を入れ、一つの[アプリケーションのように見せかけ](../Page/アプリケーションソフトウェア.md "wikilink")、新旧両方のOSで確実に実行できるようにすることがある。

なお、NeXTSTEP由来のCocoaは旧Mac OSのToolbox API由来のCarbonと必ずしも対立するものではない。Mac OS Xでは、CarbonベースのライブラリをラップしてCocoaアプリケーションとして実装したもの、Cocoaベースのコンポーネントが組み込まれたCarbonアプリケーションなど、様々な実装形態のソフトウェアが存在し、両APIは密接な相互依存関係にある。

## 現状と将来

当初の[アップルの説明では](../Page/アップル_\(企業\).md "wikilink")、Carbonに対応したアプリケーションは、CarbonLibをインストールしたMac OS 9とMac OS Xで（それぞれのOSに特有の機能を除けば）同じように動作可能というものであった。しかし実際には、CarbonLibには問題も多く、デベロッパはMac OS 9とMac OS X用にコードを書き分けねばならない場面も多かった。そのため、Mac OS Xへの移行も完了した今日では、Mac OS 9とMac OS Xの両方で動作可能な実行環境としてのCarbonは役目を終えたとも言える。

[Mac OS X v10.2から](../Page/Mac_OS_X_v10.2.md "wikilink")[Mac OS X v10.4にかけて](../Page/Mac_OS_X_v10.4.md "wikilink")、CarbonはCocoaを模したHIObject(カスタムコントロールを作成するための機能セット)の導入や、Mac OS X全体の共有基盤といえる[Core Foundationとの互換性強化など](../Page/Core_Foundation.md "wikilink")、Cocoa同等の開発基盤として、徐々に構造の近代化が計られた。

しかしながら[Mac OS X v10.5での](../Page/Mac_OS_X_v10.5.md "wikilink")[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")対応はUI部分が見送られ\[1\]、64ビット完全対応にはCocoaへの移行が必須となるなど、アップルはGUI[フロントエンド](../Page/フロントエンド.md "wikilink")としてのCarbonを徐々にフェードアウトさせ、Cocoaをメインとする姿勢を強めている。[Mac OS X v10.6では従来Carbonベースだった](../Page/Mac_OS_X_v10.6.md "wikilink")[QuickTime](../Page/QuickTime.md "wikilink")と[Finder](../Page/Finder.md "wikilink")がCocoaで作り直されている。将来的にはMac OS XにおけるCarbon APIは[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")の共有基盤を担う低レベルレイヤーとして位置づけられていくことになるとみられる。

なおMac OS XはPowerPC CPUのみならず、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")CPU上へも移植された。[Intel Mac版Mac](../Page/Intel_Mac.md "wikilink") OS XではCFM Carbonのアプリケーションはネイティブには動作せず、[OS X Lionで廃止された](https://ja.wikipedia.org/wiki/Mac_OS_X_Lion "wikilink")[Rosetta](../Page/Rosetta.md "wikilink")と呼ばれる環境の上で動作していた。Intel Mac版Mac OS Xが登場した頃は、CocoaアプリケーションとMach-O Carbonアプリケーションは再コンパイルすることでネイティブに動作するとされていた。[macOS Catalinaでは](https://ja.wikipedia.org/wiki/macOS_Catalina "wikilink")、32bitアプリケーションは動作しない為、CarbonアプリケーションはCocoaでの作り直しが必要であり、Cocoaアプリケーションも64bit化が必須である。

## 脚注

<references />

[Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")

1.  [Choosing a Development Path for Your Carbon User Interface](http://developer.apple.com/documentation/Carbon/Conceptual/Carbon64BitGuide/PortingTo64Bit/chapter_4_section_5.html)