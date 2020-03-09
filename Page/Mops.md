> この記事は[Mops](https://ja.wikipedia.org/wiki/Mops)から翻訳されています。


**Mops** (**M**ike's **o**bject oriented **p**rogramming **s**ystem、モップス) とは、 [Forth](../Page/Forth.md "wikilink") 言語をベースにした、[Macintosh](../Page/Macintosh.md "wikilink")向けの[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")開発環境。

## 概要

[1988年](../Page/1988年.md "wikilink")に[オーストラリア](https://ja.wikipedia.org/wiki/オーストラリア "wikilink")のプログラマであるマイケル・ホーア (Michael Hore) によって開発された。最初の核部分が[アセンブラで構築されたことをのぞけば](../Page/アセンブリ言語.md "wikilink")、Mops は当初からそれ自身の上で開発・改良されてきた。2016年現在も、リソース類以外は全て Mops 自身で開発されている。[フリーウェア](../Page/フリーウェア.md "wikilink")であり、ソースコードも公開されている。

Mops は、 Forth 言語に基づく比較的サイズが小さい核部分を、追加的ワード定義によって拡張することで生成されている。初期の Forth は[間接スレッディング方式による](https://ja.wikipedia.org/wiki/スレッデッドコード#間接スレッディング "wikilink")[インタープリタ](https://ja.wikipedia.org/wiki/インタープリタ "wikilink")によって実装されていたが、 Mops の核となるForth環境はサブルーチンスレッディングであり、最適化された[機械語](../Page/機械語.md "wikilink")を生成する[コンパイラ](../Page/コンパイラ.md "wikilink")を備えている。したがって Mops プログラムは機械語にコンパイルされた上で実行される。そのためプログラムの動作は高速である。他方で、インタープリタ方式の特徴である、コード断片を実行して動作を確認できるという機能を残しているため、迅速にソフトウェアを作る上でも有利である。

Mops ではロードされたプログラムを実行可能ファイルとして書き出すことができる。これによって、単独で実行可能な[アプリケーションを作ることもできる](../Page/アプリケーションソフトウェア.md "wikilink")。Mops では、この過程はインストールと呼ばれている。

2016年現在、[68k](https://ja.wikipedia.org/wiki/68k "wikilink") ネイティブで Macintosh Toolbox を利用する Mops 4.04 、 [PowerPC](../Page/PowerPC.md "wikilink") ネイティブで [Carbon](../Page/Carbon.md "wikilink") ライブラリを利用する PEF 32 ビットおよび Mach-O 32/64 ビットの PowerMops 6.2 、[X86-64](https://ja.wikipedia.org/wiki/x64 "wikilink") ネイティブで [Cocoa](../Page/Cocoa.md "wikilink") フレームワークを利用する iMops 2.x の三種類のバージョンが配布されている。

PowerMops まではホーアが開発してきたが、 iMops からは、長らく Mops のヘビーユーザーであり、かつドキュメントの日本語訳やバグ報告などを通して接点を得ている Nao Sakurada によって開発が継続されている。

## Mops のコード

Mops は [Forth](../Page/Forth.md "wikilink") をベースにしているため、コードの基本単位は「ワード」と呼ばれ、ワードは「ディクショナリ」に格納される。また、「データスタック」を利用しているため、引数とそれを受け取るワードの関係では[逆ポーランド記法](../Page/逆ポーランド記法.md "wikilink")により記述する。[オブジェクト指向言語](https://ja.wikipedia.org/wiki/オブジェクト指向言語 "wikilink")ではあるが、[手続き型言語](https://ja.wikipedia.org/wiki/手続き型言語 "wikilink")としても記述できる。

コードには[アセンブリコードを埋め込むこともでき](../Page/アセンブリ言語.md "wikilink")（[インラインアセンブラ](https://ja.wikipedia.org/wiki/インラインアセンブラ "wikilink")）、高度なプログラムを記述できる。 ただし、Mops内蔵のアセンブラでは、アセンブリコードも逆ポーランド記法で記述するようになっている。つまり、オペランド（高級言語でいう引数）が前、[オペコード](https://ja.wikipedia.org/wiki/オペコード "wikilink")（命令そのもの）が後ろにくる。これは、内蔵アセンブラもまた、Mopsでプログラムされ、Mops上で動作するプログラムだからでもある。

## 関連項目

  - [Forth](../Page/Forth.md "wikilink")

## 外部リンク

  - [Mops on the web](http://www.powermops.org/) - 公式ページ

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")