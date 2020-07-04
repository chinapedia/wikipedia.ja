> この記事は[Flake](https://ja.wikipedia.org/wiki/Flake)から翻訳されています。


**Flake**はリリース予定の[KOffice](https://ja.wikipedia.org/wiki/KOffice "wikilink") 2に使われているプログラミング[ライブラリ](../Page/ライブラリ.md "wikilink")である。Flakeでは「形」（Shape）に関する基本的な概念が規定される予定である。あるShapeはエンドユーザーには画像もしくはテキストといったコンテンツとして現れる。Shapeは四角や円などの形式をとることができ、Shapeは描画それ自体に関するものであるため、そこにはどのような種類のメディアでも含むことができる。現在、KOfficeの全てのコンポーネントに対してFlakeを最大限使用するための作業が進められている \[1\]。

## 機能

Flakeの機能は、コンテンツを表示するShapeと、コンテンツもしくはユーザーインターフェイスを取り扱うToolsに分けられる。Shapeはコンテンツの種類に応じて作られる。例えば、テキストShapeはKWordにおいて[.txt](https://ja.wikipedia.org/wiki/.txt "wikilink")と[.odt](https://ja.wikipedia.org/wiki/.odt "wikilink")フォーマットを扱うのに対し、KChartのShapeは[.odc](https://ja.wikipedia.org/wiki/.odc "wikilink")のような表に関連したドキュメントのみをサポートする。ShapeはToolsのセットとパッケージ化するためコンテンツとユーザーインターフェイスのエレメントを取り扱うことが出来る。こうすることでアプリケーションに必要な機能を加え、また他のアプリケーションのShapeを簡単に埋め込むことが可能となる。Shapeは必要なときに他のShapeを読み込むことが出来る。例えばある画像が文書ドキュメントに含まれていて、その画像を扱う際にはイメージShapeが読み込まれるようになる。

FlakeはKOffice 1シリーズにおける、ウィジェットを基にした埋め込みの後継的な機能である。埋め込み型ウィジェットには以下のような欠点があった。すなわちウィジェットは常に四角形でなくてはならないこと、回転することが出来ないこと、そしてピクセルで測られていたことである。これら3つの欠点は全てFlakeによって解決される予定である。埋め込まれたドキュメントデータを拡大縮小したり、回転したり歪めたりというようにあらゆる形式をとれる。単位にはミリメートルなどが使われる。またFlakeは拡張性などいくつかの分野で元のデザインを改良しているところがある。例えば、GoogleのSummer of Code 2007において、Marijn Kruisselbrinkは[記譜法](../Page/記譜法.md "wikilink")のShapeとToolsをベースにした[MusicXML](../Page/MusicXML.md "wikilink")を発表した\[2\]。あるShapeに対し他のShapeの位置を認識させることが可能であり、例えば、画像をテキストの上に移動させることによってそのテキストを画像の周りに動的に配置することが出来る\[3\]。またShapeはグループ化することも可能であり、そうすることで複数のShapeが1つのShapeとして振舞うことが出来るようになる\[4\]。

## KOffice

[KOffice](https://ja.wikipedia.org/wiki/KOffice "wikilink")の各コンポーネントにおいて、Flakeは以下に挙げるような機能を有すると見られている\[5\]。

  - [KWord](../Page/KWord.md "wikilink") - テキストをShapeとして扱う。
  - [KSpread](https://ja.wikipedia.org/wiki/KSpread "wikilink") - 複数のセルを1つのShapeにまとめる。
  - [KPresenter](https://ja.wikipedia.org/wiki/KPresenter "wikilink") - Flakeの一部となる。
  - [Kivio](https://ja.wikipedia.org/wiki/Kivio "wikilink") - Flakeの一部となる。
  - [Karbon14](https://ja.wikipedia.org/wiki/Karbon14 "wikilink") - ベクタ画像を発展的に扱う。
  - [Krita](../Page/Krita.md "wikilink") - レイヤーを含めて画像をShapeとして扱う。
  - [KChart](https://ja.wikipedia.org/wiki/KChart "wikilink") - 1つのグラフを1つのShapeとして扱う。
  - [KFormula](https://ja.wikipedia.org/wiki/KFormula "wikilink") - 1つの公式を1つのShapeとして扱う。
  - [Kexi](https://ja.wikipedia.org/wiki/Kexi "wikilink") - データを[KWord](../Page/KWord.md "wikilink")や[KSpread](https://ja.wikipedia.org/wiki/KSpread "wikilink")に組み入れる。
  - [KPlato](https://ja.wikipedia.org/wiki/KPlato "wikilink") - 各工程をShapeとして扱う。

## 脚注

<references/>

## 関連項目

  - [KDE](../Page/KDE.md "wikilink")
  - [KOffice](https://ja.wikipedia.org/wiki/KOffice "wikilink")

[Category:KDE](https://ja.wikipedia.org/wiki/Category:KDE "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink")

1.  [The KOffice Project - Release Goals for KOffice 2.0](http://www.koffice.org/developer/releasegoals2.0.php)
2.  [Pencils Down for KOffice Summer of Code Students\!](http://dot.kde.org/1188249220/)
3.  [The Road to KDE 4: New KOffice Technologies](http://dot.kde.org/1168284615/)
4.  [Flake - KOffice](http://wiki.koffice.org/index.php?title=Flake)
5.  [Flake - KOffice](http://wiki.koffice.org/index.php?title=Flake#Design_talk)