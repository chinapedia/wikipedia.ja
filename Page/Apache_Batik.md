> この記事は[Apache Batik](https://ja.wikipedia.org/wiki/Apache_Batik)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:svg.svg "wikilink") (SVG) で記述された[ベクトル画像](https://ja.wikipedia.org/wiki/ベクトル画像 "wikilink")\]\]

**Apache Batik**（アパッチ・バティック）は、[Scalable Vector Graphics](../Page/Scalable_Vector_Graphics.md "wikilink") (SVG) で記述された[ベクトル画像](https://ja.wikipedia.org/wiki/ベクトル画像 "wikilink")を、描画、生成、編集するために使うことができる、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の[ライブラリ](../Page/ライブラリ.md "wikilink")であり、[Apache XML Graphicsプロジェクトにより開発されている](../Page/Apache_XML_Graphics.md "wikilink")。[Apacheライセンス](https://ja.wikipedia.org/wiki/Apacheライセンス "wikilink")による[オープンソース](../Page/オープンソース.md "wikilink")の[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。SVGは、2次元のベクトル画像を記述するための[XMLに準拠した](../Page/Extensible_Markup_Language.md "wikilink")[マークアップ言語](../Page/マークアップ言語.md "wikilink")である。

このライブラリの名前は、[バティック](https://ja.wikipedia.org/wiki/バティック "wikilink") (インドネシア、マレーシア特産のろうけつ染め) に由来する。

## 概要

Apache Batikは、次の機能を提供する複数の核となる[モジュール](https://ja.wikipedia.org/wiki/モジュール "wikilink")を提供する。

  - SVG画像データを描画する。
  - SVG画像データを編集・修整する。
  - SVG画像データを何らかのラスタ[画像形式に変換する](https://ja.wikipedia.org/wiki/画像ファイルフォーマット "wikilink")。[PNG](../Page/Portable_Network_Graphics.md "wikilink")、[JPEG](../Page/JPEG.md "wikilink")、[TIFFなどの形式への変換が可能である](../Page/Tagged_Image_File_Format.md "wikilink")。
  - [Windows Metafile](../Page/Windows_Metafile.md "wikilink") (WMF) 形式の画像をSVG画像データに変換する ( Windows Metafile の形式は、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") の[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")で使われるベクトル画像の形式である) 。
  - SVG画像データでのスクリプティングとユーザイベントを管理する。

Batik の配布物には、すぐに使うことができるSquiggleという名称のSVG[ブラウザ](https://ja.wikipedia.org/wiki/ブラウザ "wikilink")が同梱されている。このSVGブラウザは、先述のモジュールを利用している。

Apache Batik は、現在ある [SVG 1.1](http://www.w3.org/TR/SVG11/) [ライブラリ](../Page/ライブラリ.md "wikilink")のなかで標準仕様に最も忠実に準拠したライブラリの1つである。[1](http://xmlgraphics.apache.org/batik/status.html) \[1\]

最新の 1.7beta1 バージョン [3](http://www.apache.org/dist/xmlgraphics/batik/README.txt) は、2007年3月30日に公開されたが、 [SVGアニメーション](http://www.hcn.zaq.ne.jp/___/REC-SVG11-20030114/animate.html#AnimateElementsIntro)機能\[2\]をほぼ完全に実装しており、[SVG 1.2](http://www.w3.org/TR/2004/WD-SVG12-20041027/) 2004年10月下旬の作業ドラフトで規定しているいくつかの機能も実装している 。

## 脚注

<references/>

## 関連項目

  - [Scalable Vector Graphics](../Page/Scalable_Vector_Graphics.md "wikilink") (SVG)
  - [Synchronized Multimedia Integration Language](../Page/Synchronized_Multimedia_Integration_Language.md "wikilink") (SMIL)
  - sXBL : SVG名前空間に属さない要素に対して、表示方法や対話的な振る舞いを定義する仕組み ([:en:sXBL](https://ja.wikipedia.org/wiki/:en:sXBL "wikilink"))

## 外部リンク

  - [Apache Batik プロジェクト](http://xmlgraphics.apache.org/batik/)
  - [日本 Apache XML プロジェクト](http://jpfop.sourceforge.net/jaxml/)
  - [BatikのsXBL実装の現在の状況](http://wiki.apache.org/xmlgraphics-batik/SupportedSVG12Features)

[Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink") [Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:画像処理ソフト](https://ja.wikipedia.org/wiki/Category:画像処理ソフト "wikilink") [Category:グラフィックライブラリ](https://ja.wikipedia.org/wiki/Category:グラフィックライブラリ "wikilink")

1.  最新の 1.7beta1 バージョンを使っての公式のSVGテストで92%以上の成績であった。 [2](http://www.codedread.com/svg-support.php)
2.  SVGアニメーションはSVG画像データへの[SMILデータの埋め込みにより実行する](../Page/Synchronized_Multimedia_Integration_Language.md "wikilink")。