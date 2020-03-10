> この記事は[Universal Business Language](https://ja.wikipedia.org/wiki/Universal_Business_Language)から翻訳されています。


**Universal Business Language** (**UBL**) は、企業間[電子商取引](../Page/電子商取引.md "wikilink")のために定義された[XML形式の電子伝票の](../Page/Extensible_Markup_Language.md "wikilink")[仕様](../Page/仕様.md "wikilink")である。[OASISで標準化が行われている](https://ja.wikipedia.org/wiki/OASIS_\(組織\) "wikilink")。Commerce One社による[xCBL](https://ja.wikipedia.org/wiki/xCBL "wikilink") 3.0をベースに開発された。

通常、企業間電子商取引の伝票定義は業界ごとに行われているが、「注文」「請求」など似通ったものも少なくない。業界ごとに似たような伝票の定義を開発・維持するコストを抑えるため、UBLは業種に依存しない汎用の伝票を定義する。

UBLバージョン1.0 (2004年) では、以下の8種類の伝票を定義している。

  - Order
  - Order Response Simple
  - Order Response (detailed)
  - Order Change
  - Order Cancellation
  - Despatch Advice
  - Receipt Advice
  - Invoice

UBLバージョン2.0 (2006年) では、さらに23種類の伝票が追加された。追加された伝票には、カタログ交換、見積り、支払いなどの業務で使われるものが含まれている。

UBLの伝票の構文的な定義は[XMLスキーマによって記述されている](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")。 また、伝票のモデルは[ebXML CCTSに則って定義されている](https://ja.wikipedia.org/wiki/ebXML_Core_Components "wikilink")。CCTSベースのモデルからXMLスキーマ定義を作成するにあたっては、UBL用のXML設計規則 (UBL Naming and Design Rules) を定めている。これは[UN/CEFACT](https://ja.wikipedia.org/wiki/UN/CEFACT "wikilink")による同種のXML設計規則とは異なるものになっている。UBLのXMLスキーマ設計の特徴は、要素 (element) とその型 (complexType) とが共にグローバルに定義されていることで、このような形態はGarden of Edenと呼ばれている。

現在 (2017年7月) の最新版はUBL 2.1。UBL2.2を2017年12月、UBL2.3を2019年12月リリース目標で開発中\[1\]。中小企業向けにUBL 1.0 Small Business Subsetという[サブセットを開発して実装を容易にしようとする動きもある](../Page/部分集合.md "wikilink")。また、伝票の項目定義は英語が原文だが、これを各国語に翻訳する活動があり、現在は日本語・中国語 (簡体字・繁体字)・韓国語・スペイン語の各言語に翻訳されている。

UBLと同種の仕様として[OAGIS](https://ja.wikipedia.org/wiki/OAGIS "wikilink")があるが、両者は別個に活動している。

## 脚注

## 外部リンク

  - [OASIS Universal Business Language (UBL) TC](http://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)
  - [UBL 1.0仕様書](http://docs.oasis-open.org/ubl/cd-UBL-1.0/)
  - [UBL 2.0仕様書](http://docs.oasis-open.org/ubl/os-UBL-2.0/UBL-2.0.html)
  - [UBL 2.1仕様書](http://docs.oasis-open.org/ubl/os-UBL-2.1/UBL-2.1.html)

[Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:電子商取引](https://ja.wikipedia.org/wiki/Category:電子商取引 "wikilink")

1.