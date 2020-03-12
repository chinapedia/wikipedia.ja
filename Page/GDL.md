> この記事は[GDL](https://ja.wikipedia.org/wiki/GDL)から翻訳されています。


**GDL**=Geometric Description Language(幾何記述言語)は、[ArchiCAD](../Page/ArchiCAD.md "wikilink")ライブラリオブジェクトの[プログラミング言語](../Page/プログラミング言語.md "wikilink")で、そのCADオブジェクトの[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")は**GSM**。

## 使用方法

GDLのオブジェクトは[AutoCAD](../Page/AutoCAD.md "wikilink")のブロックに似ている。ブロックと違う点はパラメトリックである事で、2次元と3次元の機能が連動しているため、断面図では側面、平面図では上面、3Dでは[投影図](../Page/投影図.md "wikilink")など、どの[視点](https://ja.wikipedia.org/wiki/視点 "wikilink")からも正確な表現を得ることができる。GDLスクリプトの主な役割は、ArchiCADのライブラリ部品を定義することで、3Dモデル、3Dモデルからの断面/立面および平面の投影、2Dシンボル、UI表示、リスト情報を定義できる。

[ArchiCAD](../Page/ArchiCAD.md "wikilink")の各バージョンには家具、窓、ドア、樹木、人物、車、建設部材などのデフォルトライブラリが含まれている。

詳細でパラメトリックなオブジェクトを販売している企業のウェブサイトもあり、樹木、人物などデフォルトライブラリには含まれていないような、より優れた多様なオブジェクトが提供されている。

## ライセンス

GDLは無償提供されており(ただしArchiCAD本体は有償)、[グラフィソフト](../Page/グラフィソフト.md "wikilink")社のLP_XMLConverterやGDL Web Plug-Inなどの無償ツールを使用して、GDLのオブジェクトライブラリの開発が可能。

## 技術情報

**GDL**プログラム言語は[BASIC](../Page/BASIC.md "wikilink")に似ており、同じような制御構文や変数論理を持っている。

GDLの2Dおよび3Dでは、全てのモデル要素がローカル[座標](../Page/座標.md "wikilink")にリンクしている。必要な位置に要素を配置するには、座標を必要な位置および向きに移動し、その後要素を生成する。座標に対する移動、回転、伸縮は、「[変換 (数学)](../Page/変換_\(数学\).md "wikilink")」と呼ばれる。変換は[スタック](../Page/スタック.md "wikilink")として保存され、さらに変換を行ったり、変換の一部を削除することも可能。

GDLは[下位互換](https://ja.wikipedia.org/wiki/下位互換 "wikilink")となっており、[ArchiCADライブラリ部品](https://ja.wikipedia.org/wiki/ArchiCADライブラリ部品 "wikilink")を作成したArchiCADの継続バージョンで開くことは可能だが、それ以前のバージョンで開くことはできない。

詳細な技術情報については、ArchiCAD最新版の「GDLリファレンスマニュアル」を参照。

## 関連項目

  - [ArchiCADライブラリ部品](https://ja.wikipedia.org/wiki/ArchiCADライブラリ部品 "wikilink")
  - [ArchiCAD](../Page/ArchiCAD.md "wikilink")
  - [グラフィソフト](../Page/グラフィソフト.md "wikilink")

## 外部リンク

  - [Graphisoft R\&D - 開発会社ハンガリー本社](http://www.graphisoft.com/)
  - [グラフィソフト ジャパン株式会社 - 開発会社日本支部](http://www.graphisoft.co.jp/)
  - [ArchiCAD Wiki](http://ja.archicadwiki.com/)
  - [オブジェクトデポジトリ(海外サイト)](http://archicad-talk.graphisoft.com/object_depository.php)

[Category:CADソフト](https://ja.wikipedia.org/wiki/Category:CADソフト "wikilink") [Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink") [Category:ドメイン固有言語](https://ja.wikipedia.org/wiki/Category:ドメイン固有言語 "wikilink")