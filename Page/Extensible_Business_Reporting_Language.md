> この記事は[Extensible Business Reporting Language](https://ja.wikipedia.org/wiki/Extensible_Business_Reporting_Language)から翻訳されています。


**XBRL**()は、**拡張可能な事業報告言語**の意で、[財務諸表](../Page/財務諸表.md "wikilink")などのビジネスレポートを[電子文書](../Page/電子文書.md "wikilink")化することでそれらの作成の効率化や比較・分析などの二次利用を目的として、[XMLの規格をベースに作られた](../Page/Extensible_Markup_Language.md "wikilink")[言語である](../Page/マークアップ言語.md "wikilink")。

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に[米国の](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[米国公認会計士協会](https://ja.wikipedia.org/wiki/米国公認会計士協会 "wikilink")(AICPA)の支持で**XBRL** 1.0が作られて、世界的に普及を始めたことが始まりである。

[国内では](https://ja.wikipedia.org/wiki/日本 "wikilink")[日本公認会計士協会](../Page/日本公認会計士協会.md "wikilink")(JICPA)等が中心となって設立した[XBRL Japanが作成](https://ja.wikipedia.org/wiki/XBRL_Japan "wikilink")・普及・啓蒙活動を行っており、[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[7月20日](../Page/7月20日.md "wikilink")に[JIS](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink")(JIS X 7206)化された。

**XBRL**はレポートの項目・科目そのものと項目・科目間の[関係を](https://ja.wikipedia.org/wiki/関係_\(データベース\) "wikilink")[定義](https://ja.wikipedia.org/wiki/定義 "wikilink")した[語彙](https://ja.wikipedia.org/wiki/語彙 "wikilink")[辞書である](../Page/辞典.md "wikilink")[タクソノミーと実際の](../Page/分類学.md "wikilink")[値の](../Page/値_\(情報工学\).md "wikilink")[集合](../Page/集合.md "wikilink")である[インスタンス](../Page/インスタンス.md "wikilink")の3要素から構成される。

## 仕様

### XBRL 1.0

[構造](../Page/構造.md "wikilink")は[DTDを用いて](../Page/Document_Type_Definition.md "wikilink")[定義](https://ja.wikipedia.org/wiki/定義 "wikilink")されている。

### XBRL 2.0

本[仕様](../Page/仕様.md "wikilink")は[2001年](../Page/2001年.md "wikilink")[12月14日](../Page/12月14日.md "wikilink")に[標準化](../Page/標準化.md "wikilink")された。 [構造](../Page/構造.md "wikilink")には、[DTDを廃止して](../Page/Document_Type_Definition.md "wikilink")、[XML Schema](https://ja.wikipedia.org/wiki/XML_Schema "wikilink") 1.0を用いている。

**XBRL** 1.0に比べて大幅に[仕様](../Page/仕様.md "wikilink")が改造されており、以下の仕様が活用されている。

  - [XML Schema](https://ja.wikipedia.org/wiki/XML_Schema "wikilink") 1.0
      - [Namespaces in XML](https://ja.wikipedia.org/wiki/Extensible_Markup_Language#XML名前空間 "wikilink") 1.0
  - [XLink](../Page/XLink.md "wikilink") 1.0

また、[タクソノミーは以下のデータを](../Page/分類学.md "wikilink")[XLink](../Page/XLink.md "wikilink")を用いて[定義](https://ja.wikipedia.org/wiki/定義 "wikilink")する事になっている。

  - 名称(勘定科目名)
  - 計算
  - 表示順序
  - 構造(タグ同士の関係)
  - 参照

### XBRL 2.1

[2003年](../Page/2003年.md "wikilink")[12月31日](../Page/12月31日.md "wikilink")に[標準化](../Page/標準化.md "wikilink")された。[JIS](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink") X 7206はこの[仕様](../Page/仕様.md "wikilink")を翻訳したものである。

## XBRLに対応した代表的なシステム

  - [e-Tax](https://ja.wikipedia.org/wiki/e-Tax "wikilink") - 国税電子申告・納税システム([国税庁](../Page/国税庁.md "wikilink")運営)
      - [ZAIMON](https://ja.wikipedia.org/wiki/ZAIMON "wikilink") - [e-Tax](https://ja.wikipedia.org/wiki/e-Tax "wikilink")に提出済の[税務申告データを](../Page/租税.md "wikilink")[金融機関](../Page/金融機関.md "wikilink")へ提出するためのサービス([NTTデータ](../Page/NTTデータ.md "wikilink")運営)
  - [EDINET](../Page/EDINET.md "wikilink") - [金融商品取引法](../Page/金融商品取引法.md "wikilink")に基づく[開示](../Page/情報公開.md "wikilink")[文書](../Page/文書.md "wikilink")の閲覧システム([金融庁](../Page/金融庁.md "wikilink")運営)
      - [TDnet](https://ja.wikipedia.org/wiki/TDnet "wikilink") - 全[国の](https://ja.wikipedia.org/wiki/日本 "wikilink")[証券取引所](https://ja.wikipedia.org/wiki/証券取引所 "wikilink")に[上場](../Page/上場.md "wikilink")している[会社](../Page/会社.md "wikilink")の開示[情報](https://ja.wikipedia.org/wiki/情報 "wikilink")等の閲覧システム([東京証券取引所](../Page/東京証券取引所.md "wikilink")運営)

## 関連項目

  - [XML](../Page/Extensible_Markup_Language.md "wikilink")
  - [XLink](../Page/XLink.md "wikilink")
  - [DTD](../Page/Document_Type_Definition.md "wikilink")
  - [米国公認会計士協会](https://ja.wikipedia.org/wiki/米国公認会計士協会 "wikilink")
  - [日本公認会計士協会](../Page/日本公認会計士協会.md "wikilink")
  - [MetaMoJi](https://ja.wikipedia.org/wiki/MetaMoJi "wikilink")

## 外部リンク

  - [XBRL | An international standard language for communicating business data simply and quickly](http://www.xbrl.org/home)
  - [一般社団法人 XBRL Japan - XBRL Japan Inc. -](https://www.xbrl.or.jp/index.php)
  - \[<https://www.xbrl.or.jp/modules/pico1/index.php?content_id=7>　ちょっと教えてXBRL　日本公認会計士協会作成のアニメ- \]
  - \[<https://www.xbrl.or.jp/modules/pico1/index.php?content_id=21>　知らなかった！こんなに便利なXBRL GL　　XBRL GLの解説アニメ　XBRL Japan作成 - \]

## 注釈・出典

<references/>

[Category:インベスター・リレーションズ](https://ja.wikipedia.org/wiki/Category:インベスター・リレーションズ "wikilink") [Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:ビジネスソフト](https://ja.wikipedia.org/wiki/Category:ビジネスソフト "wikilink") [Category:財務諸表](https://ja.wikipedia.org/wiki/Category:財務諸表 "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")