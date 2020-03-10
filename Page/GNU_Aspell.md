> この記事は[GNU Aspell](https://ja.wikipedia.org/wiki/GNU_Aspell)から翻訳されています。


**GNU Aspell** は、[Ispell](https://ja.wikipedia.org/wiki/Ispell "wikilink") の後継として開発された[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")の[スペルチェッカ](../Page/スペルチェッカ.md "wikilink")。[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")による標準スペルチェッカである。他の[UNIX](../Page/UNIX.md "wikilink")系[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")や [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") にも移植されている。プログラム本体は [GNU Lesser General Public License](../Page/GNU_Lesser_General_Public_License.md "wikilink") (GNU LGPL) でライセンスされており、関連文書は [GNU Free Documentation License](../Page/GNU_Free_Documentation_License.md "wikilink") (GNU FDL) でライセンスされている。約70の[言語](../Page/言語.md "wikilink")の辞書が用意されている。主メンテナーは Kevin Atkinson。

GNU Aspell登場後に[Hunspell](https://ja.wikipedia.org/wiki/Hunspell "wikilink")が登場し、新規のオープンソース・ソフトウェア開発においてはHunspellを組み込む事が主流になったため、GNU Aspellの存在感は薄くなって来ている。

## Ispell との比較

Ispell と比較すると、Aspell では UTF-8 で書かれた文書のチェックにも特別な辞書が不要である。また、Aspell はその時の[ロケール](https://ja.wikipedia.org/wiki/ロケール "wikilink")に最適な設定で動作する。他にも、同時に複数の辞書を利用可能で、複数の Aspell プロセスが同時に個人辞書を利用できるようになっている。しかし、Ispell がUNIXの一般的なファイルを扱うコマンドのように動作する（すなわち、`ispell スペル誤りのあるテキストファイル名`）のに対して、Aspell では別のコマンド行オプションを必要とし、'--help' オプションの内容が高度すぎて一般利用者には理解が困難である。Aspell には、例として次のような使い方がある。

  - 対話的にテキストファイルのスペルをチェックする:

`aspell check ファイル名 `

  - 単語（と 改行 または Control-D）を書くと、同音の単語を表示する:

`aspell soundslike`

## 他のアプリケーションとの連携

[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")\[1\]、[Pidgin](https://ja.wikipedia.org/wiki/Pidgin "wikilink")、[AbiWord](https://ja.wikipedia.org/wiki/AbiWord "wikilink")、TEA text editor、[LyX](../Page/LyX.md "wikilink")、[gedit](https://ja.wikipedia.org/wiki/gedit "wikilink") などで Aspell をスペルチェッカとして利用している。 また、C言語で記述したアプリケーションからは呼び出すことが出来る。それ以外の対応言語としては、Perl, Ruby, PHPに対応している。Perlの場合、Text::Aspellを用い、Rubyの場合、Raspellを用い、PHPの場合Pspellインターフェースを用いる。

## 関連項目

  - [Enchant](https://ja.wikipedia.org/wiki/Enchant "wikilink")
  - [Hunspell](https://ja.wikipedia.org/wiki/Hunspell "wikilink")
  - [Ispell](https://ja.wikipedia.org/wiki/Ispell "wikilink")

## 脚注

## 外部リンク

  - [Aspell Homepage](http://aspell.net/)
  - [GNU Aspell download page](ftp://ftp.gnu.org/gnu/aspell/) （[FTPリンク](../Page/File_Transfer_Protocol.md "wikilink")）
  - [Aspell and UTF-8/Unicode](http://lists.freedesktop.org/pipermail/utf-8/2004-February/000005.html)
  - [GNU Aspell summary page](http://savannah.gnu.org/projects/aspell/) at [GNU Savannah](https://ja.wikipedia.org/wiki/GNU_Savannah "wikilink")
  - [Mac OS X interface for Aspell](http://cocoaspell.leuski.net/)
  - [Aspell](https://texwiki.texjp.org/?Aspell) TeX Wiki
  - [欧文スペルチェッカー GNU Aspell](http://nanasi.jp/articles/others/aspell.html) 名無しのvim使い

[Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.