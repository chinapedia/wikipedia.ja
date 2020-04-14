> この記事は[ネイティブXMLデータベース](https://ja.wikipedia.org/wiki/ネイティブXMLデータベース)から翻訳されています。


**ネイティブXMLデータベース**とは、[XML文書をその構造のまま格納](../Page/Extensible_Markup_Language.md "wikilink")・操作を行うことができる[XMLデータベース](../Page/XMLデータベース.md "wikilink")である。それによりXMLが本来持つ「ツリー構造」、「メタ情報管理」という優位性を最大限活用することができる。**NXD**と略されることもある。

## 特徴

### 関係データベースと比較

いったん[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")のテーブルのような2次元表にマッピングして格納することなく、XML文書構造の規定範囲であればどのような構造もそのまま格納する。このため、関係データベース等では実現できない、[スキーマ](https://ja.wikipedia.org/wiki/スキーマ "wikilink")定義を伴わないデータの格納・利用が可能となる利点を持つものもある。

最近では第一世代・第二世代という分類とスキーマ型、スキーマレス型という2つの方向から分類することが多い。

  - 第一世代
      - スキーマ型
          - [Tamino](https://ja.wikipedia.org/wiki/Tamino "wikilink")
      - スキーマレス型
          - [Cyber Luxeon](https://ja.wikipedia.org/wiki/Cyber_Luxeon "wikilink")
          - [EsTerra](https://ja.wikipedia.org/wiki/EsTerra "wikilink")
  - 第二世代
      - スキーマ型
      - スキーマレス型
          - [BaseX](https://ja.wikipedia.org/wiki/BaseX "wikilink")
          - [NeoCore](../Page/NeoCore.md "wikilink")
          - [TX1](https://ja.wikipedia.org/wiki/TX1 "wikilink")

### 開発方式の統一

XML文書をそのままの形式で扱うため、アプリケーションでデータを扱うときのValueObjectや、[SOAPによる](../Page/SOAP_\(プロトコル\).md "wikilink")[Webサービス](../Page/Webサービス.md "wikilink")、XSLT+FOPによるコンテンツ生成等、同一のデータ設計方式でアプリケーションシステムを統一することで開発・運用効率が期待できる。

## 課題

### 性能

ネイティブXMLデータベースが出現した当初（第一世代）はその処理性能が問題となることが多かった。現在は各ベンダーとも独自の格納構造・検索技術を導入し、それを補いつつある。

### データベース利用からソリューション活用へ

かつては大規模基幹系システムで利用されるDBMSの座を目指した動きがあったが、すでに市場へ導入されているRDBMSと正面きって対抗するのではなく、[ソリューション](https://ja.wikipedia.org/wiki/ソリューション "wikilink")の構成製品のひとつとして、もしくはパッケージ組み込みのためのストレージ管理を担当するユニットとして活用されることで市場を確保しようと試みている。 代表的なジャンルでは、[EAI](https://ja.wikipedia.org/wiki/EAI "wikilink")のようにシステム間連携を行う場合のメッセージキューとして用いられるなど。

### 今後

XMLがコモディティー化した現在、XMLを活用したシステムは増大してきている。特に注目されているのがSOX法に代表されるドキュメント管理の領域である。今後のドキュメント管理はXMLが主体になることは間違いなく、文書構造をそのまま利用できるXMLデータベースは成長するであろう。 また、マイクロソフト2007 Office systemが標準の保存形式としてXMLを採用することもドキュメント管理の分野でXMLデータベースが成長する要因であろう。

## 関連項目

  - [XMLデータベース](../Page/XMLデータベース.md "wikilink")

[en:XML database\#Native XML databases](https://ja.wikipedia.org/wiki/en:XML_database#Native_XML_databases "wikilink") [fr:Base XML native](https://ja.wikipedia.org/wiki/fr:Base_XML_native "wikilink")

[Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink")