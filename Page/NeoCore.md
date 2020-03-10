> この記事は[NeoCore](https://ja.wikipedia.org/wiki/NeoCore)から翻訳されています。


**NeoCoreXMS**は、米国[Xpriori](https://ja.wikipedia.org/wiki/Xpriori "wikilink")社が開発した[XML](../Page/Extensible_Markup_Language.md "wikilink")[データベース](../Page/データベース.md "wikilink")である。

独自のDPP ([Digital Pattern Processing](https://ja.wikipedia.org/wiki/Digital_Pattern_Processing "wikilink")) 技術を用いてXMLドキュメントの格納・検索を行う。 [富士通](../Page/富士通.md "wikilink")の[Interstage Shunsaku Data Manager](https://ja.wikipedia.org/wiki/Interstage_Shunsaku_Data_Manager "wikilink")、東芝ソリューションのTX1などとともに第二世代XMLデータベースとも呼ばれる。

XMLDB「NeoCoreXMS」は、構造が一定ではないXMLデータの格納に最適な“やわらかい”データベース・エンジンである。国内出荷ライセンス数は550ライセンスを超え、国内46%のNo.1シェア（富士キメラ総研調べ）のXMLDB/XMLデータベースである。

## 特徴

NeoCoreXMSの特徴は独自のデジタルパターンプロセッシング（DPP）である。それにより

  - スキーマレス
  - 初期のXMLデータベースと比較し、大容量のデータ格納
  - 完全一致検索においてデータ量やXML構造に依存せず高速検索

を実現している。

XMLデータ格納時に、全ての要素、データ、そして要素内容（要素とそこに含まれるデータとの関連）に対して、インデックスを付与する（フルオートインデックス機能）。 そのため、新たな構造のXMLデータを格納、または構造の変更を行った直後においても、全ての項目に対し最高の検索パフォーマンスを実現する。全ての項目に対してインデックスを付与するにも関わらず、DPPによるインデックスデータの圧縮および内部データの正規化処理によって、データベースサイズ（フットプリントサイズ）が小さいことも大きな特徴である。データベースサイズは、理論上の最大値は元のXMLデータの2.5倍。一般的なデータにおける実効サイズは、元のXMLデータの1.5～2.0倍となる。

## 得意・不得意

ハッシュインデックスを利用しているため、完全一致の検索には強いが、前方一致、後方一致等は苦手である。半数以上がドキュメントで使用されているDBMSとしてはアプリケーションの作成方法に工夫が必要である。 また、スキーマレスではあるが、システム設計上正規化を行う必要があり、スキーマレスのメリットを生かしきれない。

## 歴史

1.  2002年11月 三井物産が日本国内総販売店契約を締結
2.  2007年4月 三井物産から三井物産セキュアディレクションに事業譲渡
3.  2007年10月 三井物産セキュアディレクションからサイバーテックに事業譲渡

## 利用分野

1.  Webカタログやパーツ管理、コンテンツ管理等のメタデータ管理
2.  [Adobe](https://ja.wikipedia.org/wiki/Adobe "wikilink") [InDesign](https://ja.wikipedia.org/wiki/InDesign "wikilink")を用いた自動組版
3.  [文書管理](../Page/文書管理システム.md "wikilink")
4.  電子カルテ

## 関連項目

  - [XML](../Page/Extensible_Markup_Language.md "wikilink")
  - 関係[データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")
  - [ディレクトリサービス](https://ja.wikipedia.org/wiki/ディレクトリサービス "wikilink")
  - [XPath](https://ja.wikipedia.org/wiki/XPath "wikilink")
  - [XQuery](https://ja.wikipedia.org/wiki/XQuery "wikilink")

## 外部リンク

  - [サイバーテック](http://www.cybertech.co.jp/)
  - [NeoCoreXMSホームページ](http://www.neocore.jp/)
  - [XMLDBJPホームページ](http://www.xmldb.jp/)

[Category:データベース管理システム](https://ja.wikipedia.org/wiki/Category:データベース管理システム "wikilink") [Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink")