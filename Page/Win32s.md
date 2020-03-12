> この記事は[Win32s](https://ja.wikipedia.org/wiki/Win32s)から翻訳されています。


**Win32s**（うぃん・さんにー・えす / うぃん・さんじゅうに・えす）とは、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発及び配布した、32ビット版[Windows用](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[APIである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")「[Win32](../Page/Windows_API.md "wikilink")」のうち、[Windows 3.1で使用されるAPIである](https://ja.wikipedia.org/wiki/Windows_3.1 "wikilink")「[Win16](https://ja.wikipedia.org/wiki/Win16 "wikilink")」と共用できるものを抜き出して[サブセット](https://ja.wikipedia.org/wiki/サブセット "wikilink")としたものである。32ビット[CPU](../Page/CPU.md "wikilink")が要求され、Windows 3.1未満では使用できない。

これを用いることにより、一部のWin32対応アプリケーションがWindows 3.1でも動作させることが可能となる。ただし動くのはWindows 3.1の制約を意識して作られたプログラム（おおむねWindows 3.1が主流の頃に作られたもの）にほぼ限られ、Windows 95の登場以降はWindows3.1でそのまま動く32ビットアプリケーションは次第に見られなくなっていった。

## 概要

Windows 3.1ではもともと16ビットのAPIが使われていたが、やがて登場した[Windows NTで](../Page/Microsoft_Windows_NT.md "wikilink")32ビットのAPIが備えられ、「Win32」と呼ばれた。これを受け、従来の16ビットAPIは「Win16」と呼ばれるようになった。

その後Windows 3.1から32ビットアプリケーションが中心となる[Windows 95へのバージョンアップが迫る中で](https://ja.wikipedia.org/wiki/Windows_95 "wikilink")、ソフトウェアベンダーが大きな変更なしにWindows 95への移行を行えるよう、Win32の中でWin16と共通した部分のみがWin32sとしてまとめられ、そのAPIと[ライブラリ](../Page/ライブラリ.md "wikilink")が無料配布された。Windows 95では互換性を保持するためWin16ベースのアプリケーションも動作は可能であったが、制約が大きくOSをフリーズさせやすくする恐れがあったため、マイクロソフトはアプリケーションの32ビット化を推奨した。

## 衰退

16ビットOSではメモリアドレスが64KB（2の16乗）までしか一回で表現できないことから、Windows 3.1当時のWindowsプログラマはそれ以上のメモリを「一度には」扱うことができず、処理を分けて少しずつメモリを使わなくてはならないなどの制限に縛られていた。Win32sはAPIが32ビット化しただけであり、Windows 3.1上で動く以上はそうした制限を引きずっていた。一方で32ビットOSではこのような制限を気にせずプログラムが組めることが大きな利点だったことから、Windows 95の登場はプログラマにとってたいへん歓迎され、95登場後はWin32sへの関心は急速に失われていった\[1\]。

実際にWindows 95が普及すると、Win32s (Windows 3.1) の制限を順守するようなプログラムは作られなくなり、プログラマやソフトウエアベンダも95専用アプリケーションに急速にシフトしていった。その結果Windows 3.1は急速に衰退し、Win32sもその役割を終えた。

## 付録

Win32sインストール後の動作確認用アプリケーションとして、32ビット版[フリーセル](../Page/フリーセル.md "wikilink")が付属していた。（インストールは任意）

## 脚注・出典

## 関連項目

  - [Windows 3.1](https://ja.wikipedia.org/wiki/Windows_3.1 "wikilink")
  - [Windows 95](https://ja.wikipedia.org/wiki/Windows_95 "wikilink")
  - [Win16](https://ja.wikipedia.org/wiki/Win16 "wikilink")
  - [Win32](https://ja.wikipedia.org/wiki/Win32 "wikilink")
  - [フリーセル](../Page/フリーセル.md "wikilink")

## 外部リンク

  - [Win32Sの詳細情報 : Vector](http://rd.vector.co.jp/soft/maker/ms/se015046.html)

[de:Windows Application Programming Interface\#Win32s](https://ja.wikipedia.org/wiki/de:Windows_Application_Programming_Interface#Win32s "wikilink")

[Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink")

1.  （[立ち読み用PDF「第一章 Windowsの概念の紹介」](http://ascii.asciimw.jp/pb/bookmart/pdf/47561/4756117945.pdf)）