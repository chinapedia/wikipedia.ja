> この記事は[GNU Binutils](https://ja.wikipedia.org/wiki/GNU_Binutils)から翻訳されています。


**[GNU](../Page/GNU.md "wikilink") Binutils**または**binutils**は、さまざまなオブジェクトフォーマットを含む[オブジェクトファイル](../Page/オブジェクトファイル.md "wikilink")を扱うための[プログラミングツール](https://ja.wikipedia.org/wiki/プログラミングツール "wikilink")である。わかりやすくいうと、GNUが提供しているツールのうち、[バイナリ](../Page/バイナリ.md "wikilink")のプログラミングを実装するための関するツールであり\[1\]、そのため[クロスアセンブラとして活用できる](https://ja.wikipedia.org/wiki/アセンブリ言語#クロスアセンブラとメタアセンブラ "wikilink")。現在のバージョンは、[シグナスソリューションズ](../Page/シグナスソリューションズ.md "wikilink")（[レッドハット](../Page/レッドハット.md "wikilink")に買収された）によって[BFDライブラリ](https://ja.wikipedia.org/wiki/BFDライブラリ "wikilink")を使用して書かれた。binutilsの典型的な使われ方は、[GCC](../Page/GNUコンパイラコレクション.md "wikilink")、[make](https://ja.wikipedia.org/wiki/make "wikilink")、[GDBなどの補助である](../Page/GNUデバッガ.md "wikilink")。

## コマンド

binutilsは以下のコマンドを含む:

  - `addr2line` - プログラム内のアドレスをファイル名と行番号に変換する
  - [`ar`](https://ja.wikipedia.org/wiki/ar_\(UNIX\) "wikilink") - [アーカイブ](../Page/アーカイブ.md "wikilink")の作成、変更、および展開
  - `as` - [GNUアセンブラ](https://ja.wikipedia.org/wiki/GNUアセンブラ "wikilink")
  - `c++filt` - [C++](../Page/C++.md "wikilink")シンボルの[デマングルを行う](../Page/名前修飾.md "wikilink")
  - `elfedit`
  - `gprof` - コール・グラフ (call graph) の[プロファイルを表示する](https://ja.wikipedia.org/wiki/プロファイラ "wikilink")
  - `ld` - [リンカ](../Page/リンケージエディタ.md "wikilink")
  - [`nm`](https://ja.wikipedia.org/wiki/nm_\(UNIX\) "wikilink") - オブジェクトファイルに含まれるシンボル(クラス、関数など)を表示する
  - `objcopy` - オブジェクトファイルをコピーする、オブジェクトフォーマットの変換を行う
  - `objdump` - オブジェクトファイルのダンプ情報を表示する
  - `ranlib` - アーカイブのインデックスを作成する
  - `readelf` - [ELFファイルの中身を表示する](../Page/Executable_and_Linkable_Format.md "wikilink")
  - `size` - セクションの大きさとその合計をリストする
  - `strings` - 表示可能な文字列をリストする
  - `strip` - オブジェクトファイル中のシンボルを除去する

元々binutilsのパッケージは少数のユーティリティから構成されていたが、後に関連性の高さからリンカとアセンブラ（2.5以降）も含まれるようになった。

## BFDとlibopcodes

個々のbinutilsコマンドは単純な機能しかもたない。これらを組み合わせカプセル化したものとして、BFD (Binary File Descriptor) やlibopcodesライブラリがある。

最初のBFDバージョンは、David Henkel-WallaceとSteve Chamberlainによって書かれた。過去には、Ken RaeburnとIan Lance Taylorがメンテナンスを行っていた。2005年以降はNick Cliftonがメンテナンスしている。

## 参考文献など

<references/>

## 外部リンク

  - [GNU Binutils](https://www.gnu.org/software/binutils/)（公式サイト）
  - [Documentation for binutils](http://sourceware.org/binutils/docs/)

[Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  伊藤剛浩・川田裕貴『独自CPUで学ぶコンピュータの仕組み』、2016年3月20日 第1版 第1刷 発行、237ページ