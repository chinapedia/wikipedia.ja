> この記事は[JavaOS](https://ja.wikipedia.org/wiki/JavaOS)から翻訳されています。


**JavaOS**（ジャバOS）は基礎コンポーネントとして[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")を搭載した[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である。[サン・マイクロシステム](https://ja.wikipedia.org/wiki/サン・マイクロシステム "wikilink")によって開発されている。[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")や[Unixライクなシステムが主に](../Page/Unix系.md "wikilink")[C言語](../Page/C言語.md "wikilink")で書かれていることに対し、JavaOSは[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で書かれている。

2006年現在、サンはJavaOSを[レガシーシステム](https://ja.wikipedia.org/wiki/レガシーシステム "wikilink")と見なしている（[未来の節を参照](https://ja.wikipedia.org/wiki/#未来 "wikilink")）。

## マイクロカーネル

システムはハードウェアアーキテクチャネイティブな[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")をベースとしている。

以下が、カーネルを実行できるプラットフォームである。

  - [ARM](../Page/ARMアーキテクチャ.md "wikilink")
  - [PowerPC](../Page/PowerPC.md "wikilink")
  - [RISC](../Page/RISC.md "wikilink")
  - [SPARC](../Page/SPARC.md "wikilink")
  - [StrongARM](../Page/StrongARM.md "wikilink")
  - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")

## 仮想マシン

Java仮想マシンはマイクロカーネルの上で走る。

## ドライバ

すべての[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")はJavaで書かれ、仮想マシンによって実行される。

## ウィンドウシステム

[AWT](https://ja.wikipedia.org/wiki/Abstract_Windowing_Toolkit "wikilink") [APIを実装している](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[グラフィックスと](../Page/コンピュータグラフィックス.md "wikilink")[ウィンドウシステム](../Page/ウィンドウシステム.md "wikilink")もまたJavaで書かれている。

## 応用

JavaOSは[組み込みシステム](../Page/組み込みシステム.md "wikilink")の上で実行し、[セットトップボックス](../Page/セットトップボックス.md "wikilink")、[ネットワーキング基盤](../Page/コンピュータネットワーク.md "wikilink")、[ATMのような機器での応用を意図して設計されていた](../Page/現金自動預け払い機.md "wikilink")。また、[JavaStation](https://ja.wikipedia.org/wiki/JavaStation "wikilink")に搭載されているオペレーティングシステムでもあった。

## 未来

サンは今、公式にJavaOSを[レガシーシステム](https://ja.wikipedia.org/wiki/レガシーシステム "wikilink")と見なしており、[Java MEへの移行を推奨している](../Page/Java_Platform,_Micro_Edition.md "wikilink")\[1\]。Java ME は [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") の集合体であり、何らかのOS上で実行されるものでそれ自体はOSではないため、完全な置換にはなっていない。

## 脚注

<references/>

## 関連項目

  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
  - [JNode](https://ja.wikipedia.org/wiki/JNode "wikilink") ほとんどJavaで書かれ、Javaプログラムをネイティブのように走らせるOSを開発している、アクティブなプロジェクト。
  - [Inferno](https://ja.wikipedia.org/wiki/Inferno_\(オペレーティングシステム\) "wikilink")

## 外部リンク

  - [Inside the IBM JavaOS Project](http://www.itmweb.com/f031098.htm)
  - [JavaOS Architecture presentation from Sun](http://java.sun.com/javaone/sessions/slides/TT04/startit.html)
  - [Press release announcing JavaOS](http://onesearch.sun.com/search/clickthru?qt=JavaSoft&url=http%3A%2F%2Fwww.sun.com%2Fsmi%2FPress%2Fsunflash%2F1996-05%2Fsunflash.960529.11819.html&pathInfo=%2Fonesearch%2Findex.jsp&hitNum=6&col=all-filtered) (May 29, 1996)

[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:組み込みオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:組み込みオペレーティングシステム "wikilink") [Category:サン・マイクロシステムズ](https://ja.wikipedia.org/wiki/Category:サン・マイクロシステムズ "wikilink") [Category:オブジェクト指向OS](https://ja.wikipedia.org/wiki/Category:オブジェクト指向OS "wikilink")

1.