> この記事は[FlightGear](https://ja.wikipedia.org/wiki/FlightGear)から翻訳されています。


**FlightGear**（フライトギア）は、[オープンソース](../Page/オープンソース.md "wikilink")で開発され無料配布されている、クロスプラットフォームの[フライトシミュレータ](https://ja.wikipedia.org/wiki/フライトシミュレータ "wikilink")である。

## 歴史

[1990年代](../Page/1990年代.md "wikilink")、Curtis Olsenらは、無料で提供される2Dのフライトシミュレーションの開発を進めていた。それが形となったのは[1996年](../Page/1996年.md "wikilink")であったが、当時は[OpenGL](../Page/OpenGL.md "wikilink")に未対応であり、3Dのフライトシミュレーションでは無かった。しかし、2Dであることへの不満などから、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")には3Dグラフィックを用いたフライトシミュレーションの開発に転じ、これが現在のFlightGearの原型となっていた。[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[4月5日](../Page/4月5日.md "wikilink")には0.9.10、[2007年](../Page/2007年.md "wikilink")[12月17日](../Page/12月17日.md "wikilink")には1.0.0、[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[12月22日](../Page/12月22日.md "wikilink")には1.9.0、[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[2月25日](../Page/2月25日.md "wikilink")には2.0.0、[2013年](../Page/2013年.md "wikilink")[2月17日](../Page/2月17日.md "wikilink")には3.0.0と、大きなバージョンアップを行っている。

## 概要

### 機能

[rightのコックピット](https://ja.wikipedia.org/wiki/ファイル:FG-A-10.jpg "wikilink")\]\] FlightGearでは、全世界の[シーナリー](https://ja.wikipedia.org/wiki/シーナリー "wikilink")を開発・配布しており、ほぼ全世界の空港が使用できる。0.9.10からは、[空母](https://ja.wikipedia.org/wiki/空母 "wikilink")[ニミッツも使用可能となっている](../Page/ニミッツ_\(空母\).md "wikilink")。Windows版・Mac版に同梱されているシーナリーは[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")の[サンフランシスコ](../Page/サンフランシスコ.md "wikilink")とその周辺地域のみに限られており、後から配布サイトからシーナリーを追加する必要がある。Linuxでビルド済みパッケージを利用する場合、配布者によって「本体」と「ベースパッケージ（シーナリー+機体）」である場合と、両者を一つのパッケージで提供している場合がある。

航空機も同様で、初期データは限られたものとなっている。FlightGearでは航空機データは、民間機を中心に開発されているが、近年は軍用機やヘリコプターも増えつつある。しかし、[ドッグファイト](https://ja.wikipedia.org/wiki/ドッグファイト "wikilink")やコンバット機能などは装備されていない。ヘリコプターのフライトモデルはYASimを改造したものなどがあるが、現在はまだベータとなっている。

マルチプレイモードもあり、[Google マップを使用した航空地図で飛行状況を確認できるようになっている](https://ja.wikipedia.org/wiki/Google_マップ "wikilink")。1.0.0からは、他機とのチャットなどによる交信も可能となっている。

また、1.0.0からは[空中給油](https://ja.wikipedia.org/wiki/空中給油 "wikilink")が標準で可能となっている。[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")には山火事消火アドオン**Wildfire**も開発された。1.9.0からはマルチプレイ用の[航空管制](https://ja.wikipedia.org/wiki/航空管制 "wikilink")用の「機体データ」が作成された。ただし、他のプレイヤーが管制に従うとは限らず、またAI機の管制もできない。

### 開発

FlightGear本体は、[C++](../Page/C++.md "wikilink")を中心とした言語で記述されている。3Dグラフィックスは[OpenGL](../Page/OpenGL.md "wikilink")を使用しており、1.0.0まではライブラリに[PLIB](https://ja.wikipedia.org/wiki/PLIB "wikilink")を採用していた。しかし、1.9.0からは[OpenSceneGraph](https://ja.wikipedia.org/wiki/OpenSceneGraph "wikilink")に変更された。また、[nasal](https://ja.wikipedia.org/wiki/nasal "wikilink")スクリプトをサポートしており、機体の電装品の動作や、先述の空中給油、Wildfireなど、広範囲に利用されている。

航空機やビルディングなど3Dモデルのデータは、[Blender](../Page/Blender.md "wikilink")、[AC3D](https://ja.wikipedia.org/wiki/AC3D "wikilink")等を利用して、AC3D形式（.ac）で作成されている。またビルディングなど一部分は[SketchUp](https://ja.wikipedia.org/wiki/SketchUp "wikilink")を利用して作成される事もある。

また、上記の3Dモデルに貼り付けるテクスチャは、PLIBを採用していた1.0.0まではrgb形式に限られていたが、OpenSceneGraphを採用した1.9.0からはpng等も利用可能になった。

もともとFlightGear本体の開発は、プラットフォームごとで大部分が共通した機能で行われている。しかし、Mac版においては、もともとのバージョンの上、更にアップグレードが行われ、順次公開されている。

### フライトモデル

FlightGearの航空機は、フライトモデルと呼ばれる規則的な機体スペックを入力して作成されている。FlightGearで使用される主要なフライトモデルは、以下の4種類である。

  - YASim - [2002年](../Page/2002年.md "wikilink")の0.7.9から導入されたフライトモデル。幾何学シミュレーションによって構成される。現在は半分以上がYASimを使用して開発されている。
  - JSBSim - YASimとは対照的に、様々な引く結果の数値を入力して構成されるフライトモデル。より現実的な飛行を見せるが、入力されていない値での高機動飛行すると、非現実的な飛行に陥ることがある。1.9.0(正確には、2008年7月9日以降の開発版)では、気球や飛行船など、「空気よりも軽い気体」のシミュレーションも行えるようになった。
  - UIUC - [イリノイ大学](../Page/イリノイ大学.md "wikilink")で展開されたフライトモデル。
  - [UFO](https://ja.wikipedia.org/wiki/UFO "wikilink") - 空飛ぶ円盤を再現する。

過去には、LaRCsim、balloon等のフライトモデルが使用されていたが、UFO以外の上記3種に置き換えられ現在ではあまり使用されない。

## 外部リンク

  - [FlightGear Flight Simulator](http://www.flightgear.org/) - **公式サイト** (英語)
  - [FlightGear JP](http://flightgear.jpn.org/) - **公式サイト** (日本語)
  - [FlightGear for Mac](http://macflightgear.sourceforge.net/home/)
  - [FlightGear Community Pages](http://fgfs.i-net.hu/)
  - [UnitedFreeWorld.com](http://unitedfreeworld.com/livery.html)

[Category:フライトシミュレーション](https://ja.wikipedia.org/wiki/Category:フライトシミュレーション "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:1997年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1997年のソフトウェア "wikilink")