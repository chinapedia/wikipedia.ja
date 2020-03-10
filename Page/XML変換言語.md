> この記事は[XML](https://ja.wikipedia.org/wiki/XML)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/画像:XML_To_XML_Transformation.svg "wikilink") **XML変換言語**とは、[XML文書を入力とし](../Page/Extensible_Markup_Language.md "wikilink")、何らかの目的に適合したXML文書（に必ずしも限らない）を出力するような変換を行う[変換言語](https://ja.wikipedia.org/wiki/変換言語 "wikilink")である。

## XML から XML への変換

XML から XML への変換では、XML文書が出力される。このような変換を組み合わせると[XMLパイプライン](https://ja.wikipedia.org/wiki/XMLパイプライン "wikilink")が形成される。

## XML から XML 以外への変換

XML からデータへの変換では、何らかのバイトストリームが出力される。最も重要なものとしてXMLから[HTMLへの変換がある](../Page/HyperText_Markup_Language.md "wikilink")（HTML文書は必ずしもXML文書では**ない**）。

XSLTは、XML記述を基に、一般の[プログラミング言語](../Page/プログラミング言語.md "wikilink")のソースコードを生成する、といったことも行うことができるように設計されている。

## 実際の言語

  - [XSLT](../Page/XSL_Transformations.md "wikilink")
    最も有名なXML変換言語。XSLT 1.0 のW3C勧告は[1999年](../Page/1999年.md "wikilink")、[XPath](https://ja.wikipedia.org/wiki/XML_Path_Language "wikilink") 1.0 と共に公開され、それ以降広く実装されている。XSLT 2.0 は2007年1月にW3C勧告となり、[Saxon XSLT](https://ja.wikipedia.org/wiki/Saxon_XSLT "wikilink") のように既にそれを実装したソフトウェアも出回っている。
  - [XQuery](https://ja.wikipedia.org/wiki/XQuery "wikilink")
    名前に "query"（[クエリ](https://ja.wikipedia.org/wiki/クエリ "wikilink")）とあるが、汎用言語としての機能を持つ。[ゼロックス](../Page/ゼロックス.md "wikilink")のウェブプログラミングモデルを起源とし、[マイクロソフト](../Page/マイクロソフト.md "wikilink")、[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")、[IBM](../Page/IBM.md "wikilink")などが採用していた[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")だったが、W3C勧告として採用された。 XPath 2.0 に基づいている。XQuery のプログラムは XSLT と同様に[副作用がなく](https://ja.wikipedia.org/wiki/副作用_\(プログラム\) "wikilink")、機能的にもほぼ同じだが（変数や関数の宣言、W3Cスキーマ型を使った繰り返しなど）、文法は大きく異なる。XQuery はロジック駆動型であり、FOR、WHERE、関数合成（例えば fn:concat("
    <html>
    ", generate-body(), "
    </html>
    ")）などを使う。一方、XSLTはデータ駆動型であり、入力文書が条件を満たすとテンプレートが起動される形式であり、コードが書かれている順序に実行されるわけではない。
  - [STX](http://stx.sourceforge.net/)
    STX (Streaming Transformations for XML) は XSLT に触発された言語だが、ストリーミングを乱さないように変換をワンパスで行うよう設計されている。Javaによる実装 ([Joost](http://joost.sourceforge.net/)) と Perlによる実装 ([XML::STX](http://www.gingerall.com/charlie/ga/xml/p_stx.xml?s=org)) がある。
  - [XML Script](http://www.xmlscript.org/index.html)
    [Perl](../Page/Perl.md "wikilink") に触発された命令型スクリプト言語であり、XML の構文を使う。[XPath](https://ja.wikipedia.org/wiki/XML_Path_Language "wikilink") と同時に独自の DSLPath を入力木構造からノードを選択するのに使う。
  - [FXT](http://www2.informatik.tu-muenchen.de/~berlea/Fxt/)
    [Standard ML](../Page/ML_\(プログラミング言語\).md "wikilink") で実装された関数型XML変換ツール。
  - [XDuce](http://xduce.sourceforge.net/)
    XSLT に比較して文法が軽量化された型付き言語。実装は[MLで行われている](../Page/ML_\(プログラミング言語\).md "wikilink")。
  - [CDuce](http://www.cduce.org/)
    XDuce を汎用[関数型言語](../Page/関数型言語.md "wikilink")に拡張したもの。
  - [XStream](http://gallium.inria.fr/~frisch/xstream/)
    XML文書用の関数型変換言語。ストリーミングで使うことができ、入力文書の[構文解析](../Page/構文解析.md "wikilink")が完了する以前から出力を次の処理に渡すことが可能。場合によってはメモリに収まりきらない巨大なXML文書の変換も可能である。XStream のコンパイラは [CeCILL](https://ja.wikipedia.org/wiki/CeCILL "wikilink") という[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")のライセンスで提供されている。
  - [Xtatic](http://www.cis.upenn.edu/~bcpierce/xtatic/)
    XDuce の手法を [C\#](../Page/C_Sharp.md "wikilink") に適用したもの。
  - [HaXml](http://www.cs.york.ac.uk/fp/HaXml/)
    [Haskell](../Page/Haskell.md "wikilink")で書かれたXML変換のためのライブラリとツールの集まり。一貫性のある強力なアプローチである。[こちらのIBMの文書](http://www-106.ibm.com/developerworks/xml/library/x-matters14.html)も参照。新しい類似のソフトウェアとして [HXML](http://www.flightlab.com/~joe/hxml/) や Haskell XML Toolbox ([HXT](http://www.fh-wedel.de/~si/HXmlToolbox/)) がある。
  - [XMLambda](http://www.cartesianclosed.com/pub/xmlambda/)
    Erik Meijer と Mark Shields が[1999年](../Page/1999年.md "wikilink")の論文で解説した言語だが、実装したソフトウェアは存在しない。
  - [FleXML](http://flexml.sourceforge.net/)
    Kristofer Rose が実装したXML処理言語。XML [DTD](../Page/Document_Type_Definition.md "wikilink") に変換規則を追加する手法を採用している。

## 関連項目

  - [フィルタ](../Page/フィルタ_\(ソフトウェア\).md "wikilink")
  - [Webテンプレート](https://ja.wikipedia.org/wiki/Webテンプレート "wikilink")

[Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:コンピュータ言語](https://ja.wikipedia.org/wiki/Category:コンピュータ言語 "wikilink")