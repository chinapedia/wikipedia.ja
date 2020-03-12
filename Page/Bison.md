> この記事は[Bison](https://ja.wikipedia.org/wiki/Bison)から翻訳されています。


**Bison**（バイソン）とは[構文解析器](../Page/構文解析器.md "wikilink")を生成する[パーサジェネレータ](../Page/パーサジェネレータ.md "wikilink")の一種であり、[C](../Page/C言語.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")としての[GCCのサポートのために](../Page/GNUコンパイラコレクション.md "wikilink")開発された[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。

## 概要

Bison は [FLex](https://ja.wikipedia.org/wiki/FLex "wikilink") と共に[ローレンス・バークレー国立研究所](../Page/ローレンス・バークレー国立研究所.md "wikilink")の Vern Paxson が作成した。その仕様としては[Yacc](../Page/Yacc.md "wikilink")との上位互換を持っておりながら、多くの拡張機能が追加されており[リエントラント](../Page/リエントラント.md "wikilink")な[パーサ](https://ja.wikipedia.org/wiki/パーサ "wikilink")の生成などが行える。 もともとは、[C](../Page/C言語.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink")としての[GCCの](../Page/GNUコンパイラコレクション.md "wikilink")[フロントエンド](../Page/フロントエンド.md "wikilink")の[構文解析](../Page/構文解析.md "wikilink")用に作成されたソフトであるが現在GCC（バージョン4以降）はフロントエンドの構文解析を独自で行っており、Bison は主に単独の[プログラミング開発ツールとして使用されている](https://ja.wikipedia.org/wiki/プログラミングツール "wikilink")。

通常、[LALR法](../Page/LALR法.md "wikilink")に基づく構文解析器を生成するが、曖昧な文法については[GLR法](../Page/GLR法.md "wikilink")や[IELR法](https://ja.wikipedia.org/wiki/IELR法 "wikilink")に基づいた構文解析器を生成できる。

Barkeley Yaccなど、Bisonの他にもYaccとの上位互換性のあるソフトウェアがある \[1\]。

## 脚注

<references/>

## 関連項目

  - [Yacc](../Page/Yacc.md "wikilink")

## 外部リンク

  - [Bison（最新バージョン）マニュアル](http://www.gnu.org/software/bison/manual/)（英語）- gnu
  - [Bison 1.28](http://www.bookshelf.jp/texi/bison/bison-ja.html#SEC_Top)（マニュアルの日本語訳） - 石川直太氏訳
  - [Bison for Windows 2.4.1](http://gnuwin32.sourceforge.net/packages/bison.htm)（英語） - .sourceforge.net
  - [bison/flex(yacc/lex)について](http://hp.vector.co.jp/authors/VA022047/linux/bison.html) - Honkusaさん

[Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:パーサジェネレータ](https://ja.wikipedia.org/wiki/Category:パーサジェネレータ "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  Bisonの仕様のベースとなった「[Yacc](../Page/Yacc.md "wikilink")」の項を参照。