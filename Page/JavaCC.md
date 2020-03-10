> この記事は[JavaCC](https://ja.wikipedia.org/wiki/JavaCC)から翻訳されています。


**JavaCC** (Java Compiler Compiler) は、[オープンソース](../Page/オープンソース.md "wikilink")の[Java](https://ja.wikipedia.org/wiki/Java "wikilink")向けの[パーサジェネレータ](https://ja.wikipedia.org/wiki/パーサジェネレータ "wikilink")である。 JavaCCは、[yacc](https://ja.wikipedia.org/wiki/yacc "wikilink")と同様に[拡張BNFを入力としてとる](../Page/EBNF.md "wikilink")。yaccとの違いは生成されるパーサがJavaの[ソースコード](../Page/ソースコード.md "wikilink")だということである。 しかしながら、yaccとは異なり、JavaCCは[トップダウンのパーサを構築する](../Page/トップダウン構文解析.md "wikilink")、そのため、[LL](../Page/LL法.md "wikilink") (K) クラスの文法にしか対応していない（厳密にいうと[左再帰](../Page/左再帰.md "wikilink")は使えない）。

JavaCCに付属するJJTreeというツールを利用することで、[構文木](https://ja.wikipedia.org/wiki/構文木 "wikilink")を生成することができる。

JavaCCは[BSDライセンスが適用されている](https://ja.wikipedia.org/wiki/BSD_License "wikilink")。

## 歴史

[1996年](../Page/1996年.md "wikilink")に、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")からJackというパーサ生成ツールが公開された。 Jackの開発者たちはMatamataという会社を設立し、ツールの名前をJavaCCに改定した。 その後、MatamataはWebGainの一部となったが、WebGainは活動を停止し、JavaCCは現在のサイトに移管された。

## 関連項目

  - [ANTLR](../Page/ANTLR.md "wikilink")
  - [SableCC](https://ja.wikipedia.org/wiki/SableCC "wikilink")
  - [Coco/R](https://ja.wikipedia.org/wiki/Coco/R "wikilink")

## 外部リンク

  -
  - [JavaCC Tutorial](http://www.engr.mun.ca/~theo/JavaCC-Tutorial/)

  - [JavaCC FAQ](http://www.engr.mun.ca/~theo/JavaCC-FAQ/)

[Category:パーサジェネレータ](https://ja.wikipedia.org/wiki/Category:パーサジェネレータ "wikilink") [Category:Java開発ツール](https://ja.wikipedia.org/wiki/Category:Java開発ツール "wikilink")