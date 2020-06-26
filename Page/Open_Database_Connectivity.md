> この記事は[Open Database Connectivity](https://ja.wikipedia.org/wiki/Open_Database_Connectivity)から翻訳されています。


**Open Database Connectivity** (**ODBC**) は、[関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink") (RDBMS) にアクセスするための共通[インタフェース](../Page/インタフェース_\(情報技術\).md "wikilink") ([API](../Page/アプリケーションプログラミングインタフェース.md "wikilink"))である。

データへのアクセスを統一化することを目的としており、たとえばクライアント／サーバ型ではない[Microsoft Accessの管理するデータベースファイル](../Page/Microsoft_Access.md "wikilink") (MDB) や、そもそもRDBMSではない[CSVファイルへのアクセスなども](../Page/Comma-Separated_Values.md "wikilink")、それに対応するODBCドライバがあれば、他の一般的なデータベースへのアクセスするのと同様な方法で利用することが可能になる。

ODBCは、主に[Windows上で利用されることが多いが](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](../Page/Linux.md "wikilink")、[UNIX](../Page/UNIX.md "wikilink")などで利用されるケースもある。

## 概要

従来、データベースアプリケーションは、RDBMSベンダーが製品とともに配布するユーティリティや埋め込みSQLにより開発されてきたが、[C言語](../Page/C言語.md "wikilink")上のAPIレベルで統一したインターフェイスとしてデータベースに接続するためのAPIをまとめたのが、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が1992年に発表した「ODBC」である。

その後、ODBC3.0では、[X/Open](https://ja.wikipedia.org/wiki/X/Open "wikilink")[コンソーシアム](../Page/コンソーシアム.md "wikilink")と[ISOで進められていた標準化にあわせることとなり](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")、これは1995年に「[SQL/CLI](../Page/Call_Level_Interface.md "wikilink")」として[SQL](../Page/SQL.md "wikilink")標準の一部となった。

X/OpenとISOが進めていたSQL/CLIは、ODBCの有用性から業界標準となったODBCを標準規格化するための試みであり、それにマイクロソフトが同調した形で標準化がなされた経緯がある。そのため、ODBCもしくはSQL/CLIは多くのRDBMSでサポートされており、且つ、ODBCはほとんどの場合でSQL/CLIのスーパーセットとなっている。

建前上は、ODBCを利用することにより、データベースの各ベンダ固有のインターフェースを抽象化し統一的にアクセスできるようになるはずだが、単純なケースはともかく、実際にはSQLの文法が各ベンダによって方言があるように、接続以外の問題でデータベースごとの仕様（例えばロック）や特性を理解する必要がなくなるわけではない。

## バージョンの歴史

バージョンの歴史:\[1\]

  - 1.0: 1992年9月にリリース\[2\]
  - 2.0:  1994
  - 2.5
  - 3.0:  1995, IntersolvのJohn Goodson と IBMのFrank Pellow ・Paul Cotton が重要なインプットをODBC 3.0に提供した\[3\]
  - 3.5:  1997
  - 3.8:  2009, Windows 7と共に\[4\]

## 近年の状況

最近ではWindowsにおいてもC言語によってODBCを直接利用することは少なくなっており、[Visual Basic](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink") (VB)などでは、[COMとしてVBから直接扱えるADO](../Page/Component_Object_Model.md "wikilink") ([ActiveX Data Objects](https://ja.wikipedia.org/wiki/ActiveX_Data_Objects "wikilink"))の下部[レイヤーの選択肢の](../Page/階層構造.md "wikilink")1つとして利用される事が多い。（ADOは、ODBCに代わり[OLE DBと呼ばれるプロバイダを選択することでデータベース固有の接続方法を抽象化するが](https://ja.wikipedia.org/wiki/OLE_DB "wikilink")、既存のODBCとの接続のためのラップである「OLE DB Provider for ODBC」を使うこともできる。）

しかし、一方で、[SQL Server 2014以降では](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")[OLE DBは今後更新されず](https://ja.wikipedia.org/wiki/OLE_DB "wikilink")、汎用的な接続方法としてはODBCに回帰する方向性も示されている。\[5\]\[6\]

[.NET FrameworkではADOと同じような考え方であるが](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、マネージド環境となるため、これらのプロバイダは一新されている。ただし、従来の[OLE DBも使えるため](https://ja.wikipedia.org/wiki/OLE_DB "wikilink")、OLE DBを経由したODBCへのアクセスは今日でも利用可能ではある。SQL Serverは当然として[オラクルなどの大手RDBMSベンダは](../Page/オラクル_\(企業\).md "wikilink").NET Framework用のプロバイダ、もしくはOLE DBプロバイダを提供しており、あえてODBCを経由しなければならないケースは少ないと考えられる。

[Java](https://ja.wikipedia.org/wiki/Java "wikilink")では、かつては[JDBC](../Page/JDBC.md "wikilink")が扱うデータベース・ドライバとしてType1[ドライバ](../Page/デバイスドライバ.md "wikilink")（JDBC-ODBCブリッジ）としてJDBCの下層の物理ドライバに使われており、まだJavaに対応していないデータベースに接続する場合などの手段として使われる場合もあったが、今日では多くのデータベースがJDBCドライバを出しており、ODBCを経由させる必要性はほとんどなくなった\[7\]。

このため、JDBC-ODBCブリッジはJava7では非推奨となり、Java8では標準から削除された。\[8\]

## 外部リンク

  - [Microsoft Universal Data Access](http://www.microsoft.com/japan/msdn/data/)
  - [Online definition of CLI](https://publications.opengroup.org/c451) at the Open Groups webpage

## 脚注

### 注釈

### 出典

<references/>

[Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink")

1.
2.
3.  Microsoft Corporation. Microsoft ODBC 3.0 Programmer's Reference and SDK Guide, Volume 1. Microsoft Press. February 1997. (ISBN 978-1572315167)
4.
5.  <http://msdn.microsoft.com/ja-jp/library/cc280510.aspx>
6.  <http://blogs.technet.com/b/dataplatforminsider/archive/2011/08/29/microsoft-aligning-with-odbc.aspx>
7.  SQL Serverでさえ、JDBCドライバを出している
8.  <http://docs.oracle.com/javase/7/docs/technotes/guides/jdbc/bridge.html>