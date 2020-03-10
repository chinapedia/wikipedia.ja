> この記事は[Microsoft Compiled HTML Help](https://ja.wikipedia.org/wiki/Microsoft_Compiled_HTML_Help)から翻訳されています。


**Microsoft Compiled HTML Help**は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")に[Microsoft WinHelp形式の後継として開発](https://ja.wikipedia.org/wiki/Microsoft_WinHelp "wikilink")・リリースした独自の[オンラインヘルプ](https://ja.wikipedia.org/wiki/オンラインヘルプ "wikilink")ファイル形式である。[Windows 98](../Page/Microsoft_Windows_98.md "wikilink") のリリースで最初に導入され、[Windows XPや](../Page/Microsoft_Windows_XP.md "wikilink")[Windows Vistaでもサポートされ続けている](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。ファイル[拡張子](../Page/拡張子.md "wikilink")は **CHM** (".chm")。

HTML Helpのファイルは、[ヘルプ作成ツール](https://ja.wikipedia.org/wiki/ヘルプ作成ツール "wikilink")で作成される。[マイクロソフト](../Page/マイクロソフト.md "wikilink")は[Windowsのバージョンアップに合わせてHTML](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") Help Workshopもリリースし、フリーにダウンロード可能としている。他にも[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")から様々なヘルプ作成ツールがリリースされている。

電子書籍ビューワMicrosoft Reader .LITファイル形式は、基本的に HTML Helpの**CHM**形式から派生したものである。

[2002年](../Page/2002年.md "wikilink")、マイクロソフトはCHM形式に関連したセキュリティ問題を公表し、パッチを公開した[1](http://www.winwriters.com/security.htm)。その後、マイクロソフトはCHM形式を止めて新たなヘルプ形式であるに移行する方針とし、Windows Vistaでそれを採用している。

## 歴史

  - 1996年2月 - [マイクロソフト](../Page/マイクロソフト.md "wikilink")が、WinHelpの開発停止と新たなHTML Help標準の開発を発表
  - 1997年8月 - HTML Help 1.0 (HH 1.0) が[Internet Explorer](../Page/Internet_Explorer.md "wikilink") 4の一部としてリリースされた
  - 1998年2月 - HTML Help 1.1aが[Windows 98の一部としてリリースされた](../Page/Microsoft_Windows_98.md "wikilink")
  - 2000年1月 - HTML Help 1.3が[Windows 2000の一部としてリリースされた](../Page/Microsoft_Windows_2000.md "wikilink")
  - 2000年7月 - HTML Help 1.32がInternet Explorer 5.5と[Windows MEの一部としてリリースされた](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink")
  - 2001年10月 - HTML Help 1.33がInternet Explorer 6と[Windows XPの一部としてリリースされた](../Page/Microsoft_Windows_XP.md "wikilink")
  - 2001年3月 - WritersUAにおいて、マイクロソフトが新たなプラットフォームとしてHelp 2 （HTMLベース）を発表
  - 2003年1月 - マイクロソフトがHelp 2を汎用ヘルププラットフォームとしてはリリースしないことを決定

## ファイル形式

[HTMLのサブセットで書かれたページ群と](../Page/HyperText_Markup_Language.md "wikilink")[ハイパーリンク](../Page/ハイパーリンク.md "wikilink")化された目次で構成される。CHM形式は読むことに最適化されており、検索性能が強化されている。複数のファイルをまとめて[LZX](https://ja.wikipedia.org/wiki/LZX "wikilink")で圧縮する。多くのCHMブラウザは、ヘルプファイル本体を表示すると同時に目次を表示できるようになっている。

ファイルの先頭には "ITSF" という文字列がASCIIで入っている（"Info-Tech Storage Format" の略）。ファイル形式は[リバースエンジニアリング](https://ja.wikipedia.org/wiki/リバースエンジニアリング "wikilink")によって一部が明らかになっており、[container](http://www.speakeasy.org/~russotto/chm/chmformat.html) や [internal files](http://chmspec.nongnu.org/latest/) といった仕様が公開されている。

Windows上では、このヘルプファイルを`hhc.exe`で[コンパイルできる](../Page/コンパイラ.md "wikilink")。これは、HTML Help Workshopの一部として無料で入手可能。

[オープンソース](../Page/オープンソース.md "wikilink")でCHMファイルを読めるツールもあるが（例えば [xCHM](http://xchm.sourceforge.net), [KchmViewer](http://www.kchmviewer.net/), [GnoCHM](http://gnochm.sourceforge.net/), [Chmox for OS X](http://chmox.sourceforge.net/), [Chamonix for OS X](http://sourceforge.net/projects/chamonix/)）、Windows自身の持つ機能を完備したものはなく、特にCHMファイルを作成する機能を持つものはない。

## 利点

  - 通常のHTMLよりもファイルサイズが小さい
  - HTMLのもつフォーマットオプションにより、テキスト表現が豊かである
  - 全文検索が可能
  - 複数の CHMファイルを共通の目次や索引を持つ1つのファイルに統合可能
  - 多言語文字を含む目次やトピックフォルダを生成できる

## 応用

当初、ヘルプファイル向けに作られた形式だったが、その後他の用途にも使われている。HTMLの複数のページをコンパクトにまとめ、アーカイブ状態でブラウズ可能であることから、[電子書籍](../Page/電子書籍.md "wikilink")に応用された。人によっては、個人的なメモをこの形式で残す場合もある。というのも、階層構造化された文書で検索も高速という利点があるためである。[Firefox](https://ja.wikipedia.org/wiki/Firefox "wikilink")の拡張でCHMファイルを見ることができるものもある[2](https://addons.mozilla.org/firefox/3235/)。

## HTMLの抽出

Windowsでは、CHMファイルから HTML部分を以下のコマンドで抜き出すことができる。

`hh.exe -decompile `*`extracted`*` `*`filename.chm`*

これにより、*`filename.chm`*に含まれている HTMLファイル群が *`extracted`*というディレクトリ配下に展開される。

[APT](https://ja.wikipedia.org/wiki/APT "wikilink")をパッケージングツールとしている[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")の場合、CHMからHTMLを抜き出すには、以下のようにすればよい（1つ目のコマンドは[Debian](../Page/Debian.md "wikilink")向け）。

` # apt-get install libchm-bin`
` $ extract_chmLib tero.chm tero/`

Windows以外で使える同様のツールとして、[CHM Tools Package](http://www.speakeasy.org/~russotto/chm/)がある。

## 出典

## 外部リンク

  - [GNU Savannah Unofficial HTML Help Specification](http://savannah.nongnu.org/projects/chmspec)
  - [HTML Help Web Page on MSDN](http://msdn2.microsoft.com/en-us/library/bb267846.aspx)
  - \[<http://msdn2.microsoft.com/en-us/library/bb165722(VS.80>).aspx Microsoft Help 2 Reference\] (part of Visual Studio SDK for VS7.1 and VS8.0)
  - [History of HTML Help](http://www.helpware.net/htmlhelp/hh_info.htm)
  - [chmview](http://trexinc.sourceforge.net/chmview.php)
  - [Typical solutions for problems with accessing and displaying CHM files](http://www.drexplain.com/press/chm-files-the-page-cannot-be-displayed-error/)
  - [A free, open CHM to PDF converter for Linux/Unix](http://code.google.com/p/chm2pdf/)

[Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink") [Category:ハイパーテキスト](https://ja.wikipedia.org/wiki/Category:ハイパーテキスト "wikilink")