> この記事は[WiX](https://ja.wikipedia.org/wiki/WiX)から翻訳されています。


**Windows Installer XML toolset**（ウィックス）は、[XML](../Page/Extensible_Markup_Language.md "wikilink") ドキュメントから [Windows Installer](https://ja.wikipedia.org/wiki/Windows_Installer "wikilink") (MSI) パッケージを作成するための[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")のツールセットである。WiX はコマンドラインベースの環境をサポートしている。これにより、MSI（または MSM）パッケージを[ビルドする作業をビルドプロセスに統合することができるようになっている](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink")。リリース元は[マイクロソフト](../Page/マイクロソフト.md "wikilink")で、ライセンスは[オープンソース](../Page/オープンソース.md "wikilink")ライセンスである [Common Public License](../Page/Common_Public_License.md "wikilink") である。

## 内部構造

WiX はいくつかのコンポーネントで構成されている。コンポーネントの名前は "wick(s)" （ロウソクの芯）という単語に対する言葉遊びから来ている。\[1\]

### Candle

Candle は[コンパイラ](../Page/コンパイラ.md "wikilink")で、XMLドキュメントをコンパイルし、シンボルとシンボルへのリファレンスを含むオブジェクトファイルを生成する。

### Light

Light は[リンカ](../Page/リンケージエディタ.md "wikilink") で、オブジェクトファイルを受け取り、オブジェクトファイル中のリファレンスと、他のオブジェクトファイル中のシンボルとを適切にリンクする。また、バイナリファイルをまとめ、パッケージングし、MSI（または MSM）ファイルを生成する処理も行う。

### Lit

Lit はライブラリ操作用のツールで、複数のオブジェクトファイルを結合して、Light でパースできるライブラリに変換するのに使われる。

### Dark

Dark は逆コンパイラで、MSI または MSM ファイルを受け取り、そのパッケージを表す XML ドキュメントを生成する。

### Tallow/Heat

Tallow はディレクトリツリーをトラバースし WiX ファイルリストを生成するツールである。Tallow を使うと WiX の「フラグメント」を作ることができる。フラグメントは、コンパイル時に他の WiX ソースへ組み込むことができる。WiX 3.0 では、Tallow はより全般的な「収穫用」ツールである Heat で置き換えられる予定である。Tallow には非公式のバージョンである Mallow \[2\] もある。Mallow には、同期機能と、より改善されたコンポーネントID生成機能が付け加えられている。

## 履歴

2004年4月5日、WiX はマイクロソフトのソフトウェアで初めて、外部で制定されたオープンソースライセンスである [Common Public License](../Page/Common_Public_License.md "wikilink") の下でリリースされた。また、マイクロソフトで初めて外部 ([SourceForge.net](../Page/SourceForge.net.md "wikilink")) でホストされたシェアードソースプロジェクトでもある。

WiX の原作者で中心的な開発者である Rob Mensching は、空き時間を使って WiX の開発を行っていた。リリース時、Mensching は「オープンソースコミュニティとはどういうものか、マイクロソフト内部の人間の多くが理解していると私には思えない。私はサンプルを提供することでこの理解を高めたい」と発言している。

2006年には、マイクロソフトの様々な製品事業部から集まった数人が Mensching と共に WiX の開発を行った。彼らは週1回、勤務時間後に集まり、開発の成果を持ち寄り、プログラムを書いた。[Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink") や [Microsoft Office 2007](https://ja.wikipedia.org/wiki/Microsoft_Office_2007 "wikilink") は WiX でパッケージングされている。

2007年には WiX 2.0 は安定版と見なせるようになり、品質も製品レベルになった。今後 WiX 2.0 の開発は行われない。

2009年7月4日、WiX 3.0 は製品品質になったと見なされた。

アクティブな WiX ユーザのメーリングリストとしては [1](http://wixtoolset.org/documentation/mailinglist/) がある。

## 参考文献

  - [Slashdot](https://ja.wikipedia.org/wiki/Slashdot "wikilink") の記事（Steve Mallett [2](http://steve.osdir.com/) による）, 2004年4月24日参照、URL <https://developers.slashdot.org/story/04/04/23/2229232/wix-project-lead-interviewed-on-cpl-licensing>
  - [MSDN](https://ja.wikipedia.org/wiki/MSDN "wikilink") Blog の記事（Rob Mensching [3](http://blogs.gotdotnet.com/robmen/) による）2004年4月24日参照、URL <https://blogs.msdn.microsoft.com/robmen/2004/04/05/windows-installer-xml-wix-toolset-has-released-as-open-source-on-sourceforge-net/>
  - スライド "Introduction to WiX"（Hüsnü Kaplan [4](http://installworld.com/content/view/12/53/) による）、URL <http://installworld.com/content/view/12/53/>

<references />

## 外部リンク

  -

  -
  - [CodePlex のプロジェクト ページ](http://wix.codeplex.com/)

  -

  - [Rob Mensching へのインタビュー](http://osdir.com/Article380.phtml)

  - [WiX Toolset Tutorial](https://www.firegiant.com/wix/tutorial/)  - [日本語訳](http://wix-tutorial-ja.github.io/)

  - [Microsoft's Channel 9 による WiX チームへのビデオインタビュー](https://channel9.msdn.com/Blogs/scobleizer/Wix-team-The-most-used-piece-of-software-at-Microsoft-and-its-open-source)

### 関連ツール

  - [オープンソースの WiX XML ソースコード用エディタ WixEdit](http://wixedit.sourceforge.net/)
  - [WiXAware, WiX をターゲットとした Windows Installer のオーサリングソフト、商用](http://www.wixaware.com/)
  - [Factory, WiX 互換性のあるセットアップビルダ、商用](https://www.indigorose.com/msi-factory/Setup)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:マイクロソフトの開発ツール](https://ja.wikipedia.org/wiki/Category:マイクロソフトの開発ツール "wikilink")

1.  <http://blogs.msdn.com/robmen/archive/2005/12/22/506760.aspx>
2.  <http://www.infozoom.de/download/Mallow.zip>.