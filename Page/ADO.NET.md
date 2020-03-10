> この記事は[ADO.NET](https://ja.wikipedia.org/wiki/ADO.NET)から翻訳されています。


**ADO.NET**は[マイクロソフト](../Page/マイクロソフト.md "wikilink")が提供する、[.NET Frameworkで様々な形式のデータへアクセスする機能を提供する](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")コンポーネントの集合である\[1\]。

## 概要　

従来の[ActiveX Data Objects](https://ja.wikipedia.org/wiki/ActiveX_Data_Objects "wikilink") (ADO) を[.NET Framework環境で動作させるための](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[APIとして提供された](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。ADOを機能強化したものではなく、.NET Frameworkの[クラスライブラリの一部を構成する](../Page/ライブラリ.md "wikilink")、全く新規なアーキテクチャに基づいた製品である。

従来のADOと比較した主な特徴は下記の通り\[2\]。

  - 非同期データセット - [データベース](../Page/データベース.md "wikilink")から引き出したデータを、メモリ上に保存しておくことができる。高速な処理ができ、処理中にデータベースサーバと接続し続ける必要がない。
  - XMLの採用 - ソフトウェア間で[SOAPを利用し](../Page/SOAP_\(プロトコル\).md "wikilink")、データ転送形式に[XMLを使用することにより](../Page/Extensible_Markup_Language.md "wikilink")、他の環境との親和性が高くなる。
  - ADO.NET Data Provider - データベースや[XMLなど複数の異なるデータソースに属するデータを共通のデータ表現で扱うことができる](../Page/Extensible_Markup_Language.md "wikilink")。

## 構成

ADO.NETは.NET Frameworkのクラスライブラリの一部であり、以下の2つの構成に区分される。

  - .NET データプロバイダ
    データベースへの接続、[SQL](../Page/SQL.md "wikilink")文の発行、検索結果の取得といった基本機能の提供
  - DataSetコレクション（非接続型クラス）
    データベースから読み取ったデータをメモリ上に保持する仕組みの提供

## ADO.NET Data Provider

| データプロバイダ                                | 供給元                                                          | 備考                                                                                                               |
| --------------------------------------- | ------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------- |
| .NET Framework Data Provider for OLE DB | [マイクロソフト](../Page/マイクロソフト.md "wikilink")（.NET同梱）             | 汎用。サポートの打ち切りが進む。<ref name="sqlsvoledb_v110" >{{Cite web                                                          |
| .NET Framework Data Provider for ODBC   | マイクロソフト（.NET同梱）                                              | 業界標準のインターフェイスで、[WOSA](https://ja.wikipedia.org/wiki/WOSA "wikilink")のコンポーネント<ref name="odbcsummary" > {{Cite web |
| .NET Framework Data Provider for Oracle | マイクロソフト（.NET同梱）                                              | [Oracle](../Page/Oracle_Database.md "wikilink") データ ソースに対応。<ref name="dotnetdp_v110" >{{Cite web                 |
| Oracle Data Provider for .NET           | [オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink") | [1](http://www.oracle.com/technetwork/topics/dotnet/index-085163.html)                                           |
| ADO.NET Driver for MySQL                | [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")      | [2](http://www.mysql.com/products/connector/)                                                                    |

## 脚注

## 参考リンク

{{.NET}}

[Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink")

1.
2.