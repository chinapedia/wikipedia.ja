> この記事は[リソース \(Windows\)](https://ja.wikipedia.org/wiki/リソース_\(Windows\))から翻訳されています。


**リソース** (resource) とは、[計算リソースのことであるが](../Page/計算資源.md "wikilink")、[Microsoft Windowsの用語としては](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、ある種のリソースのことを意味する。

Windowsでリソースと呼ばれるものには、「リソース」と「システムリソース」がある。

## リソース

リソースは、[実行ファイル](../Page/実行ファイル.md "wikilink")（EXE）や[ダイナミックリンクライブラリ](../Page/ダイナミックリンクライブラリ.md "wikilink")（DLL）に埋め込まれた読み込み専用の[データ](../Page/データ.md "wikilink")である。

[Windows APIには全てのアプリケーションのリソースに簡単にアクセスする方法を提供している](../Page/Windows_API.md "wikilink")。

### 種類

各リソースは型と名前を持ち、どちらも数値識別子か文字列である。

Windows には予め定義されたリソースの型として以下のものがある。

  - [カーソル](../Page/カーソル.md "wikilink")およびアニメーション動作するカーソル
  - [アイコン](../Page/アイコン.md "wikilink")
  - [ビットマップ](https://ja.wikipedia.org/wiki/ビットマップ "wikilink")
  - [ダイアログボックス](../Page/ダイアログボックス.md "wikilink")のテンプレート
  - [フォント](../Page/フォント.md "wikilink")
  - [HTML文書](../Page/HyperText_Markup_Language.md "wikilink")
  - [文字列](../Page/文字列.md "wikilink")とメッセージテンプレート
  - バージョン情報

プログラマはリソースの型を新たに定義することもできる。

### 使用法

Windows がプログラムファイルに対応して表示するアイコンは EXE ファイル内の最初のアイコンリソースである。EXEファイル内にアイコンリソースがない場合、標準のアイコンが表示される。

EXEファイルやDLLファイルに埋め込まれたリソースを編集できるエディタがいくつかある。一般にアプリケーション内の文字列を別の言語に変換するのに使ったり、アイコンやビットマップを変更するのに使ったりする。

### リソース・エディタ

  - [XN Resource Editor](http://www.wilsonc.demon.co.uk/d10resourceeditor.htm) ([オープンソース](../Page/オープンソース.md "wikilink"))
  - [Resource Hacker](http://www.angusj.com/resourcehacker/) ([フリーウェア](../Page/フリーウェア.md "wikilink"))
  - [Sato Icon Changer](https://ja.wikipedia.org/wiki/Sato_Icon_Changer "wikilink") ([フリーウェア](../Page/フリーウェア.md "wikilink")、アイコンリソースのみ変更可)
  - [Resource Tuner](http://www.heaventools.com/) ([シェアウェア](../Page/シェアウェア.md "wikilink"))

## システムリソース

システムリソースとは[Windowsおよびアプリケーションが使用するKERNELリソース](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、USERリソース、GDIリソースと呼ばれるメモリ領域のことである。アプリケーションを管理するのがKERNELリソース、[ダイアログボックス](../Page/ダイアログボックス.md "wikilink")やウインドウなどの情報を格納するのがUSERリソース、フォントやビットマップ、アイコンなどの情報を格納するのがGDIリソースである。一般に起動しているアプリケーションが多いと使用するシステムリソースも多くなる。システムリソースの残量として表示されるのはいずれかの少ない方の容量でリソース不足になるとウインドウを開くことが出来なくなったりフリーズなどの不具合が発生する。

システムリソースという用語は16ビットOSである[Windows 3.x系で初めて登場した](https://ja.wikipedia.org/wiki/Windows_3.x "wikilink")。[Windows 3.0ではUSERとGDIの](https://ja.wikipedia.org/wiki/Windows_3.0 "wikilink")２つのリソースがありそれぞれ64KBのサイズであった。このサイズは16ビットCPUの1つのセグメントの大きさでありパフォーマンス上の理由でこのサイズとなった。しばしば勘違いされるがシステムリソースはWindowsで導入されたものであり64KBの制限はパフォーマンスを考慮した設計上の理由であるため[MS-DOS](../Page/MS-DOS.md "wikilink")やその互換性による制限ではない。[Windows 3.1では容量不足の問題を解決するためUSERが](https://ja.wikipedia.org/wiki/Windows_3.1 "wikilink")128KBに拡張され利用方法の工夫でより少ないシステムリソースを使用するように改善された。

32ビットOSである[Windows 9x系ではシステムリソースの](../Page/Windows_9x系.md "wikilink")32ビット化され、2つのUSERリソースと1つのGDIリソースがそれぞれ2MB、合計で6MBの容量となった。しかし32ビットのシステムリソースは32ビットWindowsアプリケーションでしか使えず、16ビットWindowsアプリケーションと一部のOSの機能は互換性の理由で容量の少ない16ビットのシステムリソースを使用するため、多くのメモリを搭載していたとしても依然としてリソース不足になることがことがあった。つまり[Windows 9x系で問題となるリソース不足は](../Page/Windows_9x系.md "wikilink")16ビットのシステムリソース不足のことである。\[1\]

[Windows NT系のOSではシステムリソースは存在せず](../Page/Windows_NT系.md "wikilink")、同等の役目をするのは[デスクトップヒープ](../Page/デスクトップヒープ.md "wikilink")もしくはデスクトップアプリケーションヒープである。

### ツール

  - [リソースメーター](https://ja.wikipedia.org/wiki/リソースメーター "wikilink")

[Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:MS-DOS・Windows3.x・9x系](https://ja.wikipedia.org/wiki/Category:MS-DOS・Windows3.x・9x系 "wikilink")

1.  [Windowsのシステムリソース解説 Back to the 1999](https://xwin2.typepad.jp/xwin2weblog/2008/09/windows-back-to.html)