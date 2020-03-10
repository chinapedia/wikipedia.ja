> この記事は[Call Level Interface](https://ja.wikipedia.org/wiki/Call_Level_Interface)から翻訳されています。


**Call Level Interface**（**CLI**）とは、[The Open Groupが開発した](../Page/The_Open_Group.md "wikilink")[SQL](../Page/SQL.md "wikilink")ベースの[データベース管理システム](../Page/データベース管理システム.md "wikilink")のための[デ・ファクト](https://ja.wikipedia.org/wiki/デ・ファクト "wikilink")標準の[APIである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。[1990年代](../Page/1990年代.md "wikilink")初めに開発され、[C言語](../Page/C言語.md "wikilink")と[COBOL](../Page/COBOL.md "wikilink")についてのみ定義された。Call Level Interface は C や COBOL のプログラムが DBMS に対して SQL クエリをどのように送り、返ってきた[レコードセット](https://ja.wikipedia.org/wiki/レコードセット "wikilink")をアプリケーションがどのように扱うべきかを一貫性を持って定義している。

このインタフェースは The Open Group のオープン・アプリケーション標準である Common Application Environment の一部である。これは複数のベンダーが開発したプログラムが効率的に相互運用できることを目的としていた。SQL/CLI は、SQLデータベースにアクセスするための実装非依存の国際標準である。クライアント-サーバツール群はダイナミックリンクライブラリを通して容易にデータベースにアクセスでき、各種クライアント-サーバツールがサポートされている。

CLI 標準は [Open Database Connectivity](../Page/Open_Database_Connectivity.md "wikilink") (ODBC) 仕様の基盤となり、ODBC はベンダーを越えた透過的なデータベースアクセスを可能とした。ODBC の現在のバージョンは ODBC 3.52 で、これには後述するように[ISOと](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")[X/Open](https://ja.wikipedia.org/wiki/X/Open "wikilink")の標準規格からも機能が導入されている。

## 歴史

Call Level Interface の規格策定は、アメリカを中心とした SQL Access Group によって開始された。1992年、これが当初[マイクロソフト](../Page/マイクロソフト.md "wikilink")の ODBC API として発表され、マーケティングされた。CLI 仕様は 1993年に ISO と [ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink") の標準化委員会に送られた。この標準は書籍としての番号 ISBN 1-85912-081-4 が付与され、内部文書番号は C451 とされた。

ISO SQL/CLI は 1992年版 SQL 標準(SQL92)の補遺に収録された。最終的に、ISO 標準 ISO/IEC 9075-3:1995 Information technology -- Database languages -- SQL -- Part 3: Call-Level Interface (SQL/CLI) となった。現在の SQL/CLI は SQL3（1999年版仕様）もサポートしている。

1994年第四四半期、この標準の管理は[X/Open](https://ja.wikipedia.org/wiki/X/Open "wikilink")に移管され、さらに拡張と更新が行われた。X/Open CLI インタフェースは ISO [SQL](../Page/SQL.md "wikilink") CLI を包含する範囲の機能を持つ。

## 外部リンク

  - [Online definition of CLI](http://www.opengroup.org/products/publications/catalog/c451.htm) at The Open Group

[Category:SQL](https://ja.wikipedia.org/wiki/Category:SQL "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")