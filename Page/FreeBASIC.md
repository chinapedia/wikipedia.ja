> この記事は[FreeBASIC](https://ja.wikipedia.org/wiki/FreeBASIC)から翻訳されています。


**FreeBASIC**は、[フリーで](../Page/フリーソフトウェア.md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")（[GPL](../Page/GNU_General_Public_License.md "wikilink")）の32ビット[BASIC](../Page/BASIC.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")であり、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[DOSのプロテクトモード](../Page/DOS_\(OS\).md "wikilink")（[DOSエクステンダ](../Page/DOSエクステンダ.md "wikilink")）、[Linux](../Page/Linux.md "wikilink")、[Xbox](../Page/Xbox_\(ゲーム機\).md "wikilink") 向けの実行ファイルを生成する。FreeBASIC は[セルフホスティング](../Page/セルフホスティング.md "wikilink")コンパイラであり、コンパイラ本体は約12万行のソースコードで構成されている（ライブラリは含まない）。

[GNU Binutils](../Page/GNU_Binutils.md "wikilink") を[バックエンド](https://ja.wikipedia.org/wiki/バックエンド "wikilink")として利用し、コンソール用実行ファイルとグラフィカル/[GUI用実行ファイルを生成する](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。ライブラリは静的リンクと動的リンクの両方に対応している。FreeBASIC はCライブラリと一部のC++ライブラリを利用できる。これを利用すると、C言語だけでなく他の言語のライブラリを使ったり、作成したりすることも可能である。

## 構文

FreeBASIC は[BASIC](../Page/BASIC.md "wikilink")の構文を可能な限り守っており、特に [QuickBASIC](../Page/QuickBASIC.md "wikilink") に近い構文になっている。そして、同時に最新のコーディング技術も取り入れている。標準の[手続き型としての機能に加えて](../Page/手続き型プログラミング.md "wikilink")、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")的な[データ型](../Page/データ型.md "wikilink")や[オブジェクトの考え方を導入し](../Page/オブジェクト_\(プログラミング\).md "wikilink")、[演算子や関数のオーバーロード](../Page/多重定義.md "wikilink")、[名前空間](../Page/名前空間.md "wikilink")といった機能が追加されている。

FreeBASIC では、行末を改行コードか[コロンで表す](../Page/コロン_\(記号\).md "wikilink")。このため、C言語の[セミコロン](../Page/セミコロン.md "wikilink")のような特別な行末記号は必須ではない。改行するまでに複数行のコードを書く場合に、コロンで区切る。

コメントは行単位のものとブロック単位のものがあり、行単位のコメントはシングルクオート (') で開始され、ブロックコメントは /' で開始して、'/ で終了となり、途中に改行コードがあってもよい。

### 互換性

QuickBASIC の後継を意図しているため、構文の変更は最近のユーティリティを使うためや、最新のプログラミング機能の追加のためにのみ行われている。QuickBASIC互換を厳密に保ちたい場合や、[GCC準拠にしたい場合には](../Page/GNUコンパイラコレクション.md "wikilink")、*-lang* オプションを使う。

  - *-lang fb* とすれば、FreeBASIC の最新機能が全て利用可能である。
  - *-lang deprecated* とすれば、前のバージョンの FreeBASIC に互換な構文が使える。バージョンアップで以前との互換性がなくなっている場合があるため、直前のバージョンを最新バージョンに移植したい場合に使う。
  - *-lang qb* とすれば、可能な限り QuickBASIC 互換の構文を使える。QuickBASIC との互換性を損なうような新機能は使えない。

### Hello, World\!

``` freebasic
print "Hello, World!"
sleep
```

## グラフィックス・ライブラリ

FreeBASIC には、QuickBASIC互換の組み込みの2次元グラフィックスライブラリがあり、基本的な描画（矩形、直線、円など）や[BitBltが可能で](../Page/Bit_Block_Transfer.md "wikilink")、同時にQuickBASICには無かった機能も追加されている。ライブラリ自体はOSから独立しており、コードは可搬性がある。

グラフィックスライブラリは組み込みだが、FBgfx *Screen* コマンドを使って使用を宣言しないと使えない。[OpenGL](../Page/OpenGL.md "wikilink") やプラットフォームのGUIに従ったウィンドウ生成はライブラリとして別にある。

## 今後の開発予定

FreeBASIC は[GNUコンパイラコレクション](../Page/GNUコンパイラコレクション.md "wikilink")のフロントエンドとなることを目標として開発が続いている\[1\]。それにより、[C++](../Page/C++.md "wikilink")などの[オブジェクト指向プログラミング言語](https://ja.wikipedia.org/wiki/オブジェクト指向プログラミング言語 "wikilink")の持つ機能が利用可能となり、様々なシステム上で動作し、最新の[コンパイラ最適化](../Page/コンパイラ最適化.md "wikilink")技法を活用できるようになる。

バージョン 0.17 でオブジェクト指向プログラミング機能が導入され、[データ型](../Page/データ型.md "wikilink")と[構造体](../Page/構造体.md "wikilink")が追加された。

## 脚注

## 外部リンク

  - [公式サイト](https://www.freebasic.net/)
  - [公式フォーラム](https://www.freebasic.net/forum)
  - [SourceForgeでのホームページ](http://sourceforge.net/projects/fbc/)
  - [FreeBASIC wiki](http://www.freebasic.net/wiki/)
  - [Freebasic - On the Go](http://www.hmcsoft.org/p/fbotg.php/)
  - [FreeBASIC 日本語マニュアル](http://makoto-watanabe.main.jp/freebasic/)
  - [Windows用GUIライブラリ](http://makoto-watanabe.main.jp/freebasic/Window9/W9S.html)
  - [ミラーサイト](https://github.com/freebasic/fbc)
  - [web上で確認出来るサイト](https://www.jdoodle.com/execute-freebasic-online)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink")

1.