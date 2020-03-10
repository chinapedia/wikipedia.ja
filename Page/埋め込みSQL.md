> この記事は[SQL](https://ja.wikipedia.org/wiki/SQL)から翻訳されています。


**埋め込みSQL**（うめこみ-、）は、[C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")、[COBOL](../Page/COBOL.md "wikilink")、[FORTRAN](../Page/FORTRAN.md "wikilink")、[Pascal](../Page/Pascal.md "wikilink")、[Ada](../Page/Ada.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink") ([SQLJ](../Page/SQLJ.md "wikilink")) といった[手続き型プログラミング](../Page/手続き型プログラミング.md "wikilink")に、[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")(RDBMS)を操作するための[SQL](../Page/SQL.md "wikilink")を組み込む手法であり、プログラマはソースコード内部に埋め込みSQLステートメントを直接記述することができるようになる。「組み込みSQL」とも呼ばれる。

SQL標準規格のSQL86([1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink"))において、COBOL、FORTRAN、PL/Iなどへの埋め込みSQL文の仕様、SQL89([1989年](../Page/1989年.md "wikilink"))において、C言語への埋め込みSQL文の仕様がそれぞれ策定された。

埋め込みSQLステートメントはコンパイル実行前にSQL[プリプロセッサ](../Page/プリプロセッサ.md "wikilink")によって前処理される。

[Oracleデータベースに対する埋め込みSQLのプリプロセッサとして](../Page/Oracle_Database.md "wikilink")[Pro\*C/C++](https://ja.wikipedia.org/wiki/Pro*C/C++ "wikilink")が普及しているが、他に、Pro\*COBOL、Pro\*FORTRAN、Pro\*Pascal、SQL\*Module などがある。他データベース製品では [Sybase](../Page/Sybase.md "wikilink") や [PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink") ([ECPG](https://ja.wikipedia.org/wiki/ECPG "wikilink")) がC言語への埋め込みをサポートしている。

## サポートするデータベース

### [Oracle Database](../Page/Oracle_Database.md "wikilink")

  - Ada : Pro\*Ada のサポートは Oracle 7.3 で打ち切られ、Oracle 8 以降は SQL\*Module で置き換えられた。しかしそれ以降更新されていない。<ref>{{cite web

|url=<http://download.oracle.com/docs/cd/B10501_01/server.920/a96530/migcompa.htm#1010868> |title=Ada Support in Version 8 |work=Oracle9i Database Migration, Release 2 (9.2), Chapter 5. Compatibility and Interoperability |publisher=[オラクル (企業)](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink") |accessdate=2008-07-14 }}</ref> SQL\*Module では埋め込みSQLとして異なるプログラミング方式をモジュール言語として用いる。SQL\*Module は Ada83 をサポートする。

  - C/C++ : Pro\*C は Oracle 8 より Pro\*C/C++ となった。Pro\*C/C++ は Oracle Database 11*g* でサポートされている。
    COBOL : Pro\*COBOL Oracle Database 11*g* でサポートされている。
    Fortran : Pro\*FORTRAN は Oracle 8 以降更新されていないが、バグ修正は継続して行われている\[1\]
    Pascal : Pro\*Pascal は Oracle 8 以降更新されていない。\[2\]
    PL/I : Pro\*PL/I は Oracle 8 以降更新されていないが、ドキュメントには記載されている。<ref name="langalts">{{cite web

|url=<http://download.oracle.com/docs/cd/A64702_01/doc/server.805/a58232/ch01.htm#505> |title=Language Alternatives |work=Pro\*COBOL Precompiler Programmer's Guide, Release 8.0, Chapter 1. Introduction |publisher=[オラクル (企業)](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink") |accessdate=2008-07-14 }}</ref>

### [PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")

  - C/C++
    ECPG として PostgreSQL 6.3 以降でサポートされている。C++ のサポートは限定的で、正常に処理できない構文が存在する。

## 参考文献

<references/>

## 外部リンク

  - [Introduction to Pro\*C Embedded SQL](http://infolab.stanford.edu/%7Eullman/fcdb/oracle/or-proc.html)
  - [Embedded SQL with Pro\*C](http://www.oreillynet.com/pub/a/databases/2006/12/07/embedded-sql-with-pro-c.html)
  - [SQL\*Module for Ada Programmer's Guide, Release 8.0](http://tahiti.oracle.com/pls/db92/db92.show_toc?partno=a58231)
  - [ECPG - C言語による埋め込みSQL](http://www.postgresql.jp/document/current/html/ecpg.html) (PostgreSQL)

[Category:SQL](https://ja.wikipedia.org/wiki/Category:SQL "wikilink") [Category:問い合わせ言語](https://ja.wikipedia.org/wiki/Category:問い合わせ言語 "wikilink")

1.
2.