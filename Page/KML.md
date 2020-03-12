> この記事は[KML](https://ja.wikipedia.org/wiki/KML)から翻訳されています。


**KML**（ケイエムエル）は、アプリケーション・プログラムにおける三次元[地理空間情報](../Page/地理空間情報.md "wikilink")の表示の管理などを目的とした情報を[XMLで記述するものである](../Page/Extensible_Markup_Language.md "wikilink")。2008年4月にKML2.2版は、そのまま[Open Geospatial Consortium, Inc](https://ja.wikipedia.org/wiki/Open_Geospatial_Consortium,_Inc "wikilink") (OGC) という[地理情報システム](../Page/地理情報システム.md "wikilink")の[オープンソース](../Page/オープンソース.md "wikilink")化を目指す団体の規格にOGC KMLとして取り入れられた\[1\]。

## 名称の由来

KMLという名称は、もともと**Keyhole Markup Language**の[頭字語](../Page/頭字語.md "wikilink")だったが、OGCに採用された時点で略語ではない語という扱いになった。Keyholeは現在の[Google Earthの旧名称であり](https://ja.wikipedia.org/wiki/Google_Earth "wikilink")、その開発元がGoogle社と合併するまでの会社名でもある。Keyholeという名称は[偵察衛星](../Page/偵察衛星.md "wikilink")[コロナの型名](../Page/コロナ_\(人工衛星\).md "wikilink")(KH)にちなむ。

## KML文書

[XMLで](../Page/Extensible_Markup_Language.md "wikilink")、[Google Earthや](https://ja.wikipedia.org/wiki/Google_Earth "wikilink")[Google Maps](https://ja.wikipedia.org/wiki/Google_Maps "wikilink")、[Google Mobileで表示する要素](https://ja.wikipedia.org/wiki/Google_Mobile "wikilink")（目印、イメージ、ポリゴン、3次元モデル、説明など）を記述する。3次元モデルは[COLLADA](https://ja.wikipedia.org/wiki/COLLADA "wikilink")形式で記述することができる。各地点は、常に[右手系](https://ja.wikipedia.org/wiki/右手系 "wikilink")の[経緯度](https://ja.wikipedia.org/wiki/経緯度 "wikilink")情報を持つ。それ以外に、“カメラ・ビュー”を構成するのに必要な[ティルト](../Page/ティルト.md "wikilink")、カメラの向き、高度など、より詳細なデータを記述することもできる。KMLは[GMLと同様の文法構造を持つ](https://ja.wikipedia.org/wiki/Geography_Markup_Language "wikilink")[1](http://geoweb.blog.com/313918/)。ただしGoogle MapsやGoogle MobileではKMLで記述された情報の一部は表示することができない[2](http://maps.google.com/support/bin/answer.py?answer=41136&topic=1475)。Google Maps（およびそのAPI）では公開ウェブサイトに置いたKMLファイルの記述情報を表示できる。

ファイルとしては、プレーンなXMLの場合は .kml という[拡張子](../Page/拡張子.md "wikilink")を付ける他、[ZIPで圧縮した](../Page/データ圧縮.md "wikilink") .kmz という拡張子を付けるKMZファイルがある。KMZファイルは内容に、本体である "doc.kml" というファイル一つと、そのファイル中から参照するオーバレイ用のイメージ・ファイルやアイコン用のイメージファイルを含む。

KML文書の例：

``` xml
 <?xml version="1.0" encoding="UTF-8"?>
 <kml ns="http://earth.google.com/kml/2.0">
 <Placemark>
   <description>New York City</description>
   <name>New York City</name>
   <Point>
     <coordinates>-74.006393,40.714172,0</coordinates>
   </Point>
 </Placemark>
 </kml>
```

KMLの[MIMEタイプは](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink")*application/vnd.google-earth.kml+xml*であり、KMZは*application/vnd.google-earth.kmz*である。

## KMLにおける測地規準系

KMLは、座標の前提となる[測地基準系の定義をサポートしていない](../Page/測地系.md "wikilink")。したがって、[Geomatics（地理情報学？）や](https://ja.wikipedia.org/wiki/:en:Geomatics "wikilink")[測地学](../Page/測地学.md "wikilink")などの専門的な用途には用いることができない。

## パーサー

KMLおよびKMZをパース（解釈）し地図上に表示する機能がアプリケーションなどに備わっている。

  - [Google Earth](https://ja.wikipedia.org/wiki/Google_Earth "wikilink")（[衛星写真](https://ja.wikipedia.org/wiki/衛星写真 "wikilink")・[航空写真](https://ja.wikipedia.org/wiki/航空写真 "wikilink")の背景上に表示）
  - [Google Maps](https://ja.wikipedia.org/wiki/Google_Maps "wikilink")（機能限定がある。ファイルを公開サイトに置く必要がある。）
  - [OpenLayers](https://ja.wikipedia.org/wiki/OpenLayers "wikilink")（機能限定がある。KML。）

## KMLを使用するアプリケーション

  - [ArcGIS Explorer](https://ja.wikipedia.org/wiki/ArcGIS_Explorer "wikilink")
  - [Flickr](../Page/Flickr.md "wikilink")
  - [Google Earth](https://ja.wikipedia.org/wiki/Google_Earth "wikilink")
  - [Google Maps](https://ja.wikipedia.org/wiki/Google_Maps "wikilink")
  - [Google Mobile](https://ja.wikipedia.org/wiki/Google_Mobile "wikilink")
  - [Mapufacture](https://ja.wikipedia.org/wiki/Mapufacture "wikilink")
  - [Platial](https://ja.wikipedia.org/wiki/Platial "wikilink")
  - [NASA World Wind](../Page/NASA_World_Wind.md "wikilink")
  - [Yahoo\! Pipes](../Page/Yahoo!_Pipes.md "wikilink")

## 関連項目

  - [CityGML](https://ja.wikipedia.org/wiki/CityGML "wikilink")
  - [Geography Markup Language](https://ja.wikipedia.org/wiki/Geography_Markup_Language "wikilink")
  - [GPX](../Page/GPX.md "wikilink")
  - [カテゴリ (POI)](https://ja.wikipedia.org/wiki/カテゴリ_\(POI\) "wikilink")
  - [ウェイポイント](https://ja.wikipedia.org/wiki/ウェイポイント "wikilink")
  - [COLLADA](https://ja.wikipedia.org/wiki/COLLADA "wikilink")

## 外部リンク

  - [KML入門ドキュメント](https://developers.google.com/kml/documentation/?hl=ja)
  - [KML Developer Support group](http://groups.google.com/group/kml-support)
  - [KMLImporter](http://www.worldwindcentral.com/wiki/Add-on:KMLImporter) importing placemarks into [NASA World Wind](../Page/NASA_World_Wind.md "wikilink")
  - [Google Earth Connectivity Add-on](http://www.archicadwiki.com/Google_Earth_Connectivity_Add-on) for [ArchiCAD](../Page/ArchiCAD.md "wikilink") 9
  - [Validate your KML (Online or Offline\!)](http://googlemapsapi.blogspot.com/2007/06/validate-your-kml-online-or-offline.html), Google Maps API Blog.
  - [simplekml (Python用ライブラリ)](http://simplekml.readthedocs.org/)

## 脚注

<references/>

[Category:Keyhole_Markup_Language](https://ja.wikipedia.org/wiki/Category:Keyhole_Markup_Language "wikilink") [Category:GIS](https://ja.wikipedia.org/wiki/Category:GIS "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:Google](https://ja.wikipedia.org/wiki/Category:Google "wikilink") [Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink") [Category:Webマッピング](https://ja.wikipedia.org/wiki/Category:Webマッピング "wikilink")

1.  [OGC KML](http://www.opengeospatial.org/standards/kml/)