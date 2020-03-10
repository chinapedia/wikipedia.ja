> この記事は[ANTLR](https://ja.wikipedia.org/wiki/ANTLR)から翻訳されています。


**ANTLR**（*ANother Tool for Language Recognition*）とは、[LL](../Page/LL法.md "wikilink")(\*)構文解析に基づく[パーサジェネレータ](https://ja.wikipedia.org/wiki/パーサジェネレータ "wikilink")である（バージョン3.xはLL(\*)、2.xまではLL(k)）。**PCCTS**（*Purdue Compiler Construction Tool Set*）の後継として1989年に開発され、現在も活発に開発が続いている。中心となっているのは、[サンフランシスコ大学](https://ja.wikipedia.org/wiki/サンフランシスコ大学 "wikilink")の Terence Parr 教授である。

ANTLR は[LR法](../Page/LR法.md "wikilink")に基づいたパーサジェネレータと競合関係にあり、"ANT(i)-LR"（反LR）と読めるのも偶然ではない。

ANTLR はパーサだけでなく[レキサーおよびツリーパーサも生成可能である](https://ja.wikipedia.org/wiki/字句解析器 "wikilink")。 文法の記述方法は、[EBNF](https://ja.wikipedia.org/wiki/EBNF "wikilink")に似た形式となっている。

4.7 現在、ANTLR は [Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[Python](../Page/Python.md "wikilink") (2と3)、[C\#](../Page/C_Sharp.md "wikilink")、[JavaScript](../Page/JavaScript.md "wikilink")、[Go](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink")、[Swift](https://ja.wikipedia.org/wiki/Swift_\(プログラミング言語\) "wikilink")、[C++](../Page/C++.md "wikilink")の[構文解析器](../Page/構文解析器.md "wikilink")のコードを生成できる。ANTLR は[BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")で提供されている。

## 理論的背景

理論的背景は、ANTLRのサイトにある論文

  - [LL(\*): The Foundation of the ANTLR Parser Generator](http://www.antlr.org/papers/LL-star-PLDI11.pdf)
  - [ANTLR: A Predicated-LL(k) Parser Generator](http://www.antlr.org/article/1055550346383/antlr.pdf)

などを参照されたい。

## 統合開発環境

[IntelliJ IDEA](https://ja.wikipedia.org/wiki/IntelliJ_IDEA "wikilink")、[Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink")、[NetBeans](https://ja.wikipedia.org/wiki/NetBeans "wikilink")、[Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") 向けに ANTLR の文法をサポートするプラグインがいくつか存在する。商用製品の ANTLR Studio for Eclipse や ANTLR 4 IDE などがある。

## 関連項目

  - [JavaCC](https://ja.wikipedia.org/wiki/JavaCC "wikilink")
  - [SableCC](https://ja.wikipedia.org/wiki/SableCC "wikilink")
  - [Coco/R](https://ja.wikipedia.org/wiki/Coco/R "wikilink")

## 外部リンク

  -
  - [GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")

      - [antlr/antlr4](https://github.com/antlr/antlr4)
      - [antlr/grammars-v4](https://github.com/antlr/grammars-v4)
      - [tunnelvisionlabs/antlr4cs](https://github.com/tunnelvisionlabs/antlr4cs)

  - IDE

      - [ANTLRWorks 2](http://tunnelvisionlabs.com/products/demo/antlrworks)
      - [JetBrains Plugin Repository :: ANTLR v4 grammar plugin](http://plugins.jetbrains.com/plugin/7358)
      - [ANTLR 4 IDE](https://github.com/jknack/antlr4ide)
      - [ANTLR Studio for Eclipse](http://www.placidsystems.com/antlrstudio.aspx)

  - [antlr/ANTLRWorksを使ってみる](http://www.pwv.co.jp/~take/TakeWiki/index.php?antlr%2FANTLRWorks%E3%82%92%E4%BD%BF%E3%81%A3%E3%81%A6%E3%81%BF%E3%82%8B)

  - [antlr/構文木を使った解析](http://www.pwv.co.jp/~take/TakeWiki/index.php?antlr%2F%E6%A7%8B%E6%96%87%E6%9C%A8%E3%82%92%E4%BD%BF%E3%81%A3%E3%81%9F%E8%A7%A3%E6%9E%90)

  - バーミンガム大学の [チュートリアル](http://supportweb.cs.bham.ac.uk/docs/tutorials/docsystem/build/tutorials/antlr/antlr.html)。ANTLR 2 を対象にしたものと思われる。

[Category:パーサジェネレータ](https://ja.wikipedia.org/wiki/Category:パーサジェネレータ "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:1992年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1992年のソフトウェア "wikilink")