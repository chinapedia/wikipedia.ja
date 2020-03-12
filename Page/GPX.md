> この記事は[GPX](https://ja.wikipedia.org/wiki/GPX)から翻訳されています。


**GPX**（ジーピーエックス、**GPS eXchange Format**）は、[GPS](../Page/グローバル・ポジショニング・システム.md "wikilink")/[GNSS装置やGPS](../Page/衛星測位システム.md "wikilink")/GNSSソフトウェアなど、アプリケーション間でGPS/GNSSのデータをやりとりするためのデータフォーマットである。GPXは、[XML Schemaベースでデザインされており](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")、[ウェイポイント](https://ja.wikipedia.org/wiki/ウェイポイント "wikilink")や[軌跡](https://ja.wikipedia.org/wiki/軌跡 "wikilink")、ルートなどを記述する。

## データの種類

GPXにおいては、順序関係を持たない地点の集まり（例えばイングランドの地方都市や、ニューヨークの超高層ビル群など）は、個別の[ウェイポイント](https://ja.wikipedia.org/wiki/ウェイポイント "wikilink")の集まりと考える。 一方、順序づけられた地点の集まりは、[軌跡](https://ja.wikipedia.org/wiki/軌跡 "wikilink")あるいはルートとして表現される。 概念上は、人が通った場所を記録したのが軌跡で、これから通るであろう場所を提案するのがルートということになる。 したがって、例えば、軌跡の各地点には[タイムスタンプ](https://ja.wikipedia.org/wiki/タイムスタンプ "wikilink")がある場合がある（なぜなら、記録する場合には、どこにいたか、ということと*いつ*そこにそこにいたか、を記録するからである）が、ルートは単なる提案に過ぎず、場合によっては誰もそこを通過したことがないかもしれないので、各地点のタイムスタンプが提供されることはありそうにない。

GPXファイルに必要な最小限のプロパティは、単一のポイントの緯度経度情報である。 それ以外の情報はすべて任意である。

## 関連項目

  - [カテゴリー (POI)](https://ja.wikipedia.org/wiki/カテゴリー_\(POI\) "wikilink")
  - [Exchangeable image file format](../Page/Exchangeable_image_file_format.md "wikilink")
  - [Geography Markup Language](https://ja.wikipedia.org/wiki/Geography_Markup_Language "wikilink")
  - [KML](../Page/KML.md "wikilink")（[Google Earthで使用できる](https://ja.wikipedia.org/wiki/Google_Earth "wikilink")）
  - [UTC](../Page/協定世界時.md "wikilink")

## 外部リンク

  - [Official GPX web site](https://www.topografix.com/gpx.asp)
  - [TierraWiki](http://www.phenqavis.org/): Project to build an digital database for outdoor activities using GPS data.
  - [Create GPX files for free on-line under GFDL](http://gps.pcwize.com/gpx_generator.php)
  - [GPX POI](https://www.gps-data-team.com/poi/) - GPS POI zone with GPX formated free POI files

[Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:GPS](https://ja.wikipedia.org/wiki/Category:GPS "wikilink") [Category:衛星測位システム](https://ja.wikipedia.org/wiki/Category:衛星測位システム "wikilink")