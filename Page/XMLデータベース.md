> この記事は[XMLデータベース](https://ja.wikipedia.org/wiki/XMLデータベース)から翻訳されています。


**XMLデータベース**とは、[XMLを扱うための機能を持つ](../Page/Extensible_Markup_Language.md "wikilink")[データベース](../Page/データベース.md "wikilink")である。

狭義ではXMLの[ツリー構造](https://ja.wikipedia.org/wiki/ツリー構造 "wikilink")をそのままデータ構造として持つ物を言うが、実際は伝統的な[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")にXMLを格納するものや、単に[テキストファイル](../Page/テキストファイル.md "wikilink")としてXMLを格納するものなど様々である。現在では[XPath](../Page/XML_Path_Language.md "wikilink")、[XQuery](../Page/XQuery.md "wikilink")で検索するデータベースをXMLデータベースと呼ぶことが多い。

現在でも広く用いられている[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")では、一度作成された[データ構造](../Page/データ構造.md "wikilink")を運用中に変更することが一般的に困難なのに対し、XMLデータベースは非常に拡張性が高い。それはXMLの仕様がスキーマを必須としておらずWell-formed（整形式）の形態を認めているからである。そのため、完全に仕様が決まりきらないで開発を進めたり、途中でデータ構造が変化することを前提としたシステムを比較的容易に構築することができる。

現在の実用上の問題は、[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")における[SQL](../Page/SQL.md "wikilink")のような統一規格がないことであったが、最近XMLDBの検索はXPath、XQueryで行うXML:DB規格が策定され、NeoCoreXMS、TX1を初めとする各社によって採用されはじめている。

また、性能上の問題も普及を妨げていたが、それは大きく改善されつつあり、[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")も[ハードウェア](../Page/ハードウェア.md "wikilink")や[アルゴリズム](../Page/アルゴリズム.md "wikilink")の開発によって性能上の問題を克服してきた歴史を持つため、XMLデータベースも同様の発展を遂げることが期待される。

[Oracle Database](../Page/Oracle_Database.md "wikilink")、[IBM](../Page/IBM.md "wikilink") [DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")、[Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink") などの[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")でもXPath、XQueryで検索する機能を実装しており、XMLデータを格納するデータベース製品の選択肢が増えている。一方で、XMLのデータ量や階層構造の深さやパフォーマンス要件によっては、メーカーからベンチマークテストの結果を入手するなどしてXMLデータベース・[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")のいずれを採用するかは慎重に製品を選定する必要がある。

## 代表的なXMLDB

  - [BaseX](https://ja.wikipedia.org/wiki/BaseX "wikilink")
    XPath/XQuery、全文検索をサポートした[オープンソース](../Page/オープンソース.md "wikilink")のXMLDB。
  - [Cyber Luxeon](https://ja.wikipedia.org/wiki/Cyber_Luxeon "wikilink")
    [オブジェクトデータベース](../Page/オブジェクトデータベース.md "wikilink") ObjectStore をコアエンジンとしたXMLDB。
  - [DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink") 9 pureXML (RDB)
    米国[IBM](../Page/IBM.md "wikilink")社が開発・販売している、[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink") 9 のpureXML機能。
  - [EsTerra](https://ja.wikipedia.org/wiki/EsTerra "wikilink")
    日本産XMLDB。スキーマレス、高速動作、テラバイト級をセールスポイントとしている。
  - [NeoCore XMS](../Page/NeoCore.md "wikilink")
    独自のDigital Pattern Processingによる「超高速」「やわらかい」が特徴である。
  - [Oracle XML DB](https://ja.wikipedia.org/wiki/Oracle_XML_DB "wikilink") (RDB)
    米国[Oracle社が開発](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")・販売している、[Oracle DatabaseのXMLDB機能](../Page/Oracle_Database.md "wikilink")。
  - [Tamino](https://ja.wikipedia.org/wiki/Tamino "wikilink")
    ドイツ [Software AG](https://ja.wikipedia.org/wiki/Software_AG "wikilink") 社が開発した、世界で最も売れているXMLDB。
  - [TX1](https://ja.wikipedia.org/wiki/TX1 "wikilink")
    [東芝デジタルソリューションズ](../Page/東芝デジタルソリューションズ.md "wikilink")が販売しているXMLDB。
  - [Xindice](https://ja.wikipedia.org/wiki/Xindice "wikilink")
    [Apache XMLプロジェクトで開発されている](../Page/Apache_XML.md "wikilink")[ネイティブXMLデータベース](../Page/ネイティブXMLデータベース.md "wikilink")。2011年8月より[Apache Atticに移管されました](https://ja.wikipedia.org/wiki/Apache_Attic "wikilink")。

## 関連項目

  - [XML](../Page/Extensible_Markup_Language.md "wikilink")
  - [XPath](../Page/XML_Path_Language.md "wikilink")
  - [XQuery](../Page/XQuery.md "wikilink")
  - [関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")
  - [ディレクトリサービス](https://ja.wikipedia.org/wiki/ディレクトリサービス "wikilink")
  - [永続データ構造](../Page/永続データ構造.md "wikilink")

[Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink") [Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:データモデリング](https://ja.wikipedia.org/wiki/Category:データモデリング "wikilink")