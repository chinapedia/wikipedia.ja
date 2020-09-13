> この記事は[Hello world](https://ja.wikipedia.org/wiki/Hello_world)から翻訳されています。


[HelloWorld_Maktivism_ComputerProgramming_LEDs.jpg](https://ja.wikipedia.org/wiki/File:HelloWorld_Maktivism_ComputerProgramming_LEDs.jpg "fig:HelloWorld_Maktivism_ComputerProgramming_LEDs.jpg")ライトの[発光](../Page/発光.md "wikilink")を用いた"Hello, World\!"の表示\]\]

**Hello world**（ハロー・ワールド）は、画面に「Hello, world\!」やそれに類する文字列を表示する[プログラムの通称である](../Page/プログラム_\(コンピュータ\).md "wikilink")。多くの[プログラミング言語](../Page/プログラミング言語.md "wikilink")において非常に単純なプログラムであり、[プログラミング言語](../Page/プログラミング言語.md "wikilink")の入門書で、プログラムを動かすためのプログラミング言語の基本文法の解説例として提示される。

## 利用目的

ハロー・ワールドは伝統的にプログラミング言語をプログラム初心者に紹介するために使われる。また、ハロー・ワールドはプログラミング言語が正しくインストールされていること、およびプログラミング言語の使用方法を理解するための健全性テスト ([Sanity Test](https://ja.wikipedia.org/wiki/:en:Sanity_check "wikilink"))にも使用される。

『[プログラミング言語C](https://ja.wikipedia.org/wiki/プログラミング言語C "wikilink")』（第2版）では、初めに「新しいプログラミング言語を学ぶ唯一の道は、それでプログラムを書いてみることである」との考えが示され、プログラムを入力して実行し、出力を確認することを習得すれば、言語の他の要素を学ぶことは容易だと訓示される。そして、「hello,world という単語を印字せよ」との例題が示される。この例題について、まずプログラムのソースコードが示され、次にUNIXにおける典型的なコンパイル・実行方法が例示される。そして、このプログラムの詳細が解説される\[1\]。

大抵のプログラミング言語の入門書では、このプログラムを作ることを最初の例題としており、ほとんどの場合、新しくプログラミング言語を習得する際に最初に作るのがこのプログラムである。そのため、「世界一有名なプログラム」と呼ばれることもある。

## 歴史

[Hello_World_Brian_Kernighan_1974.jpg](https://ja.wikipedia.org/wiki/File:Hello_World_Brian_Kernighan_1974.jpg "fig:Hello_World_Brian_Kernighan_1974.jpg")による"Hello, world"プログラム (1978)\]\]

プログラミングできる[コンピュータ](../Page/コンピュータ.md "wikilink")の開発以来、小さなテストプログラムは存在してきたが、テスト文言として「Hello, World\!」を使う習慣は[ブライアン・カーニハン](../Page/ブライアン・カーニハン.md "wikilink")と[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")による著書「[プログラミング言語C](https://ja.wikipedia.org/wiki/プログラミング言語C "wikilink")」（1978年）\[2\]のC言語バージョンから始まったと言われている。同著書のプログラム例は`hello, world`（大文字なし、感嘆符なし）を[標準出力に出力する](https://ja.wikipedia.org/wiki/標準ストリーム "wikilink")。この例は[ブライアン・カーニハン](../Page/ブライアン・カーニハン.md "wikilink")がまとめた[ベル研究所](../Page/ベル研究所.md "wikilink")の内部資料「Programming in C: A Tutorial」（1974年）\[3\]を継承したものである。

``` c
#include <stdio.h>

main( )
{
  printf("hello, world\n");
}
```

C言語バージョンの以前にはカーニハンの前著「」（1973年）での例があったが、存在が知られている最初のバージョンのプログラムは外部変数を説明するための例だった。プログラムはターミナルに改行を含む`hello, world!`を出力するものだった。B言語では文字数の長さがASCII文字の4文字までという制限があったため、文言は複数の文字列に分割されていた。前節の例はターミナルに`hi!`を出力するもので、`hello, world!`という文言はそれを表す為に複数の文字列を必要とする少し長い挨拶文として紹介された。

``` c
main(){
  extrn a,b,c;
  putchar(a); putchar(b); putchar(c); putchar('!*n');
}

a 'hell';
b 'o, w';
c 'orld';
```

`hello, world`の起源は[BCPL](../Page/BCPL.md "wikilink")（1967年）であるとも言われている。この主張はBCPLの発明者[ブライアン・カーニハン](../Page/ブライアン・カーニハン.md "wikilink")と[マーティン・リチャーズ](https://ja.wikipedia.org/wiki/マーティン・リチャーズ "wikilink")の[アーカイブ](../Page/アーカイブ.md "wikilink")ノートに依るものである。

モダンな言語においてHello Worldは洗練された変化を遂げている。例えば、[Go言語は多言語対応プログラムを紹介し](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink")\[4\]、[Sun](../Page/サン・マイクロシステムズ.md "wikilink") [Java](https://ja.wikipedia.org/wiki/Java "wikilink")は[SVG](https://ja.wikipedia.org/wiki/SVG "wikilink")で文言を表し\[5\]、[XL言語は](https://ja.wikipedia.org/wiki/XL_\(プログラミング言語\) "wikilink")3Dグラフィックの地球で見せている\[6\] 。`hello, world`の出力には、[Perl](../Page/Perl.md "wikilink")、[Python](../Page/Python.md "wikilink")、[Rubyのような言語では一行だけを必要とするかもしれないが](https://ja.wikipedia.org/wiki/Ruby_\(代表的なトピック\) "wikilink")、一方で低レベルのアセンブリ言語では数十行の命令を必要とする。とエリオット・ソロウェイは、グラフィックスやサウンドがテキストより簡単に操作できるようになり、「Hello, World\!」のテスト文言が過去のものとなる可能性があることを示唆している。

## 種類

[PSP-Homebrew.jpeg](https://ja.wikipedia.org/wiki/File:PSP-Homebrew.jpeg "fig:PSP-Homebrew.jpeg")の[実証実験のためのハロー](../Page/概念実証.md "wikilink")・ワールド\]\] この文言は[句読点や](../Page/約物.md "wikilink")[頭文字](https://ja.wikipedia.org/wiki/頭文字 "wikilink")の異なる多数の種類が存在している。その種類は[コンマ](../Page/コンマ.md "wikilink")「,」や[感嘆符](../Page/感嘆符.md "wikilink")「\!」の有無、頭文字の「H」および「W」が大文字かどうかを含む。いくつかの大文字のみサポートするシステム上の言語では「HELLO WORLD」のように異なる形式の実装を強制し、[難解プログラミング言語](https://ja.wikipedia.org/wiki/難解プログラミング言語 "wikilink")でのハロー・ワールドはわずかに修正された文字列を出力する。「」以外の文言でも良いので、同様の意味で「」が用いられることもあり、[日本語プログラミング言語](https://ja.wikipedia.org/wiki/日本語プログラミング言語 "wikilink")では「Hello World」を直訳した「こんにちは世界」が用いられることもある。

利用目的にも異なる種類がある。[Lisp](https://ja.wikipedia.org/wiki/Lisp "wikilink")・[ML](../Page/ML.md "wikilink")・[Haskell](../Page/Haskell.md "wikilink")のような[関数型プログラミング言語](https://ja.wikipedia.org/wiki/関数型プログラミング言語 "wikilink")では、[再起手法を強調する関数型プログラミングの実例として利用されることがある](https://ja.wikipedia.org/wiki/再帰#再帰呼び出し "wikilink")。一方で、オリジナルの例は副作用を伴った[純粋関数型言語に違反した入出力の例として見られる](../Page/関数型言語.md "wikilink")。[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")・[C言語](../Page/C言語.md "wikilink")・[VHDL](../Page/VHDL.md "wikilink")のような組み込みで使われる言語では、文言を出力することが追加のコンポーネントや他機器との連携なしでは難しい、もしくは、その手法が存在しないことの例として用いられる。[マイクロコンピュータ](../Page/マイクロコンピュータ.md "wikilink") (マイコン)・[FPGA](../Page/FPGA.md "wikilink")・[CPLD](../Page/CPLD.md "wikilink")などの機器では、制御間隔と機器連携を実験するLEDの発光（[Lチカ](https://ja.wikipedia.org/wiki/Lチカ "wikilink")）が文言出力の代わりに利用される。

[Debian](../Page/Debian.md "wikilink")と[Ubuntu](../Page/Ubuntu.md "wikilink")は[apt](https://ja.wikipedia.org/wiki/apt "wikilink")パッケージシステムでハロー・ワールドプログラムを提供している。利用者は`apt-get install hello`と入力すると依存ソフトウェアと一緒に同プログラムがインストールされる。それ自身には意味はないが、そのプログラムが[健全性テスト](https://ja.wikipedia.org/wiki/健全性テスト "wikilink")を提供すると同時に、初心者にパッケージのインストール方法を伝えるシンプルな例となる。しかし、開発者にとってはより重要な利便性があり、手作業だったりdebhelperを使っての[debパッケージの作り方の良い例であり](https://ja.wikipedia.org/wiki/deb_\(ファイルフォーマット\) "wikilink")、[GNU Helloを使ったバージョンは](https://ja.wikipedia.org/wiki/GNU_Hello "wikilink")[GNU](../Page/GNU.md "wikilink")プログラムの書き方の例となる。

## 脚注

## 外部リンク

  - [](http://cm.bell-labs.com/cm/cs/who/dmr/btut.html) —  の初出とされるB.カーニハンによるB言語チュートリアル(1973)
  - [](http://www.ariel.com.au/jokes/The_Evolution_of_a_Programmer.html) - プログラミング技術向上による変化（冗談サイト）
  - [](http://www.gnu.org/software/hello/) - [{{langによる実装](../Page/GNUプロジェクト.md "wikilink")。コーディングスタイルや、プロジェクトメンテナンスのサンプルとして運用されている。

[Category:プログラミング・フォークロア](https://ja.wikipedia.org/wiki/Category:プログラミング・フォークロア "wikilink") [Category:アプリケーションソフト](https://ja.wikipedia.org/wiki/Category:アプリケーションソフト "wikilink")

1.  『プログラミング言語C 第2版』（訳書訂正版）「第1章 やさしい入門」
2.
3.
4.  [A Tutorial for the Go Programming Language.](http://golang.org/doc/go_tutorial.html#tmp_20)  The Go Programming Language. Retrieved July 26, 2011.
5.
6.