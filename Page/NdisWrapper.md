> この記事は[NdisWrapper](https://ja.wikipedia.org/wiki/NdisWrapper)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Ndisgtk.png "wikilink") **NdisWrapper** は、[無線LAN](../Page/無線LAN.md "wikilink")用の[ネットワークカード](https://ja.wikipedia.org/wiki/ネットワークカード "wikilink")に付属する[Windows向け](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")を[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")で使えるようにする[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。すなわち、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")にWindowsカーネルの一部機能と[NDISの](../Page/Network_Driver_Interface_Specification.md "wikilink")[APIの実装を](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[互換レイヤー](../Page/互換レイヤー.md "wikilink")として提供するソフトウェアである。多くの無線ネットワークカードベンダーは Linux 向けドライバをリリースしていないので、[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")には NdisWrapper が含まれていることが多い。

## 使い方

NdisWrapper は、Linux 上でネットワークカードの Windows 向けドライバを利用できるようにする。最低限、ドライバの inf ファイルと .sys ファイルが必要である。

例えば driver という名前のドライバがあるとする。ファイルとしては driver.inf と driver.sys があり、vendorid:productid は 0000:0000 であるとする。NdisWrapper はドライバを /etc/ndiswrapper/driver/ にインストールする。このフォルダには以下の3つのファイルがある。

  - 0000:0000.conf - inf ファイルから抜き出した情報が格納されている。
  - driver.inf - 本来の inf ファイル
  - driver.sys - 本来のドライバ本体

## グラフィカルなフロントエンド

NdisWrapper のグラフィカルな[フロントエンド](../Page/フロントエンド.md "wikilink")として、Ndisgtk や NdisConfig がある。これらを使うと、完全にグラフィカルな環境で NdisWrapper を使うことができる。

## 類似プログラム

類似のプログラムとして次のものがある。

### Linuxant DriverLoader (Linux)

[DriverLoader](http://www.linuxant.com/driverloader/) は NdisWrapper と同等の機能を提供する Linux 向け商用ツール

### Project Evil (BSD)

[FreeBSD](../Page/FreeBSD.md "wikilink") および [NetBSD](../Page/NetBSD.md "wikilink") ベースの同等プロジェクトとして **Project Evil** がある。NdisWrapper とほぼ同じ方法だが、[OpenBSD](../Page/OpenBSD.md "wikilink") は反[バイナリ・ブロブ](https://ja.wikipedia.org/wiki/バイナリ・ブロブ "wikilink")主義であるため Project Evil には参加していない。Project Evil には NdisWrapper の USB サポートなどの機能が存在しない。

## 関連項目

  - [OpenWrt](https://ja.wikipedia.org/wiki/OpenWrt "wikilink")

## 外部リンク

  - [NdisWrapper公式サイト](http://ndiswrapper.sourceforge.net/)
  - [ndisgtk](http://jak-linux.org/projects/ndisgtk/)
  - [NdisConfig](http://code.google.com/p/ndisconfig/)
  - [Project Evil: The Evil Continues](http://lists.freebsd.org/pipermail/freebsd-current/2004-January/019486.html), 2004年1月24日, [FreeBSD](../Page/FreeBSD.md "wikilink")メーリングリストより
  - [Too Evil, Too Furious](http://lists.freebsd.org/pipermail/freebsd-hardware/2005-April/002464.html), 2005年4月25日, [FreeBSD](../Page/FreeBSD.md "wikilink")メーリングリストより
  - [NetBSD NDIS Driver Port](http://netbsd-soc.sourceforge.net/projects/ndis/)

[Category:システムソフトウェア](https://ja.wikipedia.org/wiki/Category:システムソフトウェア "wikilink") [Category:デバイスドライバ](https://ja.wikipedia.org/wiki/Category:デバイスドライバ "wikilink")