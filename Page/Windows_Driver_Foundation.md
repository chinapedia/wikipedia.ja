> この記事は[Windows Driver Foundation](https://ja.wikipedia.org/wiki/Windows_Driver_Foundation)から翻訳されています。


**Windows Driver Foundation**（**WDF**）は、[Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink") 以降の Windows 向けの[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")開発のための[マイクロソフト](../Page/マイクロソフト.md "wikilink")製ツールセットである。

WDF を構成する主要ツールは [Kernel-Mode Driver Framework](https://ja.wikipedia.org/wiki/Kernel-Mode_Driver_Framework "wikilink") (KMDF) と [User-Mode Driver Framework](https://ja.wikipedia.org/wiki/User-Mode_Driver_Framework "wikilink") (UMDF) である。これらのツールキットは、Windows のドライバ開発のための新しい[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")モデルを提供する。フレームワークの主要な目標は "Conceptual Scalability"（概念的スケーラビリティ）であり、ドライバ開発者が少数の単純な概念を学ぶだけで簡単なドライバを書けるようになり、さらに学ぶに従ってより複雑な機能のドライバを書けるようになることを意味する。これは、単純なドライバを書く場合にも複雑な技術的詳細に精通している必要がある [Windows Driver Model](../Page/Windows_Driver_Model.md "wikilink") (WDM) とは著しく異なる。

Conceptual Scalability を実現する鍵の一部は、KMDF と UMDF が "opt-in" モデルだという点にある。このモデルでは、模範的なドライバのデフォルトの動作を拡張したり、オーバーライドすることが可能である。これは、WDM でドライバの動作のあらゆる面を開発者が書いて実装する必要があったのとは対照的である。

## 種類

このフレームワークには2つのバリエーションがある。

  - [Kernel-Mode Driver Framework](https://ja.wikipedia.org/wiki/Kernel-Mode_Driver_Framework "wikilink") - 標準的な[カーネルモード](https://ja.wikipedia.org/wiki/カーネルモード "wikilink")のデバイスドライバ作成のフレームワーク
  - [User-Mode Driver Framework](https://ja.wikipedia.org/wiki/User-Mode_Driver_Framework "wikilink") - [ユーザーモード](https://ja.wikipedia.org/wiki/ユーザーモード "wikilink")で動作可能なデバイスドライバ作成のフレームワーク

基盤となるプログラミングモデルは共通である。しかし、カーネルモードのフレームワークは[C言語](../Page/C言語.md "wikilink")のインタフェースを使い、ユーザーモードのフレームワークは[C++](../Page/C++.md "wikilink")のインタフェースに基づき、[COMの軽量版に基づいている](../Page/Component_Object_Model.md "wikilink")。

WDF にはドライバ開発者用の静的検証ツールも含まれている。これらツールは、よくあるコード上の問題やテストでは検出が難しいコード上の問題を特定することができる。

## ツール

  - [Static Driver Verifier](http://www.microsoft.com/japan/whdc/DevTools/tools/SDV.mspx) (SDV) - コードの呼び出し関係を検証する。複数の関数呼び出しや複数の操作にまたがった問題を検出できる。ドライバがほぼ完成した時点で利用できるよう設計されている。
  - [PREFast for Drivers](http://www.microsoft.com/japan/whdc/devtools/tools/prefast.mspx) (PFD) - SDV よりも浅い検証を行う。バッファオーバーランのチェックなど、よくある[バグ](../Page/バグ.md "wikilink")やドライバ特有のバグを検出する。個々の関数内のコードを扱うので、ドライバ開発の初期から利用できる。

## 外部リンク

  - [Windows Driver Foundation Homepage](http://www.microsoft.com/whdc/driver/wdf/default.mspx)
  - [Windows Driver Frameworks (Windows Drivers)](https://msdn.microsoft.com/en-us/Library/Windows/Hardware/ff557565.aspx)
  - [Windows Driver Kit](http://www.microsoft.com/whdc/devtools/WDK/default.mspx)
  - [Download kits and tools - Windows Hardware Dev Center](https://msdn.microsoft.com/en-US/windows/hardware/gg454513)
  - [OSR Online](http://www.osronline.com) WDF、KMDFなど Windows におけるドライバ開発に関する各種記事がある。
  - [Introducing Windows Driver Framework](http://www.wd-3.com/archive/FrameworkIntro.htm), by Walter Oney（Windowsドライバ開発の）
  - [Building and deploying a basic WDF Kernel Mode Driver](http://www.codeproject.com/system/wdf_kmdf_basic.asp), CodeProject
  - [Developing a WDF USB Kernel Mode Driver for the OSR USB FX2](http://www.codeproject.com/system/kmdf_osr_usb_fx2.asp), CodeProject

[Category:デバイスドライバ](https://ja.wikipedia.org/wiki/Category:デバイスドライバ "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink")