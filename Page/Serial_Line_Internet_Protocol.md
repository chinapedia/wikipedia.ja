> この記事は[Serial Line Internet Protocol](https://ja.wikipedia.org/wiki/Serial_Line_Internet_Protocol)から翻訳されています。


**Serial Line Internet Protocol**（シリアル回線IP）は、ほとんどのコンピュータに内蔵されていた[シリアルポート](../Page/シリアルポート.md "wikilink")から[インターネット](../Page/インターネット.md "wikilink")などの[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")ネットワークに[電話回線](https://ja.wikipedia.org/wiki/電話回線 "wikilink")など（シリアル通信回線）の低速回線を通じて一時的に接続するための[プロトコルである](../Page/通信プロトコル.md "wikilink")。略称**SLIP**（スリップ）。

[1984年](../Page/1984年.md "wikilink")に[アメリカ](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")3Comの[リック･アダムス](https://ja.wikipedia.org/wiki/リック･アダムス "wikilink")が[BSD](../Page/BSD.md "wikilink")4.2に実装しRFC1055として標準化された。

しかしSLIPは[チェックサム](../Page/チェックサム.md "wikilink")（[イーサネット](../Page/イーサネット.md "wikilink")の[CRCなど](../Page/巡回冗長検査.md "wikilink")）などの誤り検出機構がないため、ノイズの発生しやすい回線で転送中のデータが破壊されても[リンク層](../Page/リンク層.md "wikilink")で誤りを検出できない欠点があり、上位層での検出作業が必要となる。

かつては遠隔地から[ダイアルアップ](https://ja.wikipedia.org/wiki/ダイアルアップ "wikilink")して[Telnet](../Page/Telnet.md "wikilink")などに多く使用されていたが、ネットワーク層にIPしか利用できず、上記の欠点などセキュリティも低いため、現在では[PPPに取って代わられている](../Page/Point-to-Point_Protocol.md "wikilink")。

## CSLIP

**Compressed SLIP**（圧縮SLIP、通称：**CSLIP**）は上記SLIPの欠点を改善するためにRFC1144で定義されたSLIPの新しいバージョンである。現在殆どのSLIPの実装はCSLIPをサポートしている。

## 関連項目

  - [コンピュータネットワーク](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")
  - [Point-to-Point Protocol](../Page/Point-to-Point_Protocol.md "wikilink")

[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:リンク層プロトコル](https://ja.wikipedia.org/wiki/Category:リンク層プロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")