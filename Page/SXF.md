> この記事は[SXF](https://ja.wikipedia.org/wiki/SXF)から翻訳されています。


**SXF**（エス・エックス・エフ）は、CADデータ交換標準コンソーシアム (SCADEC) が提唱する、異なる[CAD](../Page/CAD.md "wikilink")間でデータをやりとりする際に使用する中間ファイル形式である。**S**cadec data e**X**change **F**ormatの略。[図面](../Page/図面.md "wikilink")の[電子納品](https://ja.wikipedia.org/wiki/電子納品 "wikilink")における標準ファイルとして扱われる。

## 概要

[国土交通省](../Page/国土交通省.md "wikilink")の主導で、1999年3月に設立されたCADデータ交換標準コンソーシアム (SCADEC) が開発。

[STEPの規格の一つであり](../Page/ISO_10303.md "wikilink")、「Part21 交換構造のクリアテキスト符号化 (Clear text encoding of the exchange structure) 」に準拠している。

SXFは、レベル1からレベル4までが存在し、うちレベル1と2は開発が完了している。

  - レベル1 画面(紙)上で、図面表示が正確に再現できること。
  - レベル2 2次元CAD製図データの要求を十分満たし、再利用時における使い勝手が確保されること。
  - レベル3 レベル4の仕様策定過程で必要とされる幾何部分の仕様。
  - レベル4 STEP/AP202の製図機能だけではなく、[建設](../Page/建設.md "wikilink")分野特有の情報も付け加え、3次元も対象とするプロダクトデータの利用ができること。

物理ファイルはSFC(フィーチャコメントファイル)とP21(STEPファイル)の2種類がある。 P21はSTEP/AP202に準拠した国際的に通用する形式。SFC(Scadec Feature Comment file)はCADデータ交換用の形式で、P21よりもファイルサイズが小さい。

仕様は公開されており、下記リンクから仕様書が入手できるほか、[C言語](../Page/C言語.md "wikilink")で扱える共通ライブラリも存在する。

現在、多くのCADでSXFへの対応が進められているが、CADアプリケーションの仕様等の問題で、必ずしもデータを同じように扱えるとは限らない。このため一部組織では検定を行い、出力SXFの品質認証を行なっている。

## 関連項目

  - [オープンCADフォーマット評議会](https://ja.wikipedia.org/wiki/オープンCADフォーマット評議会 "wikilink")
  - [SXF技術者検定試験](https://ja.wikipedia.org/wiki/SXF技術者検定試験 "wikilink")

## 外部リンク

  - [CADデータ交換標準開発 (JACIC)](http://www.cals.jacic.or.jp/cad/)
  - [オープンCADフォーマット協議会](http://www.ocf.or.jp/)
  - [OCF最新動向ブログ](https://blog.goo.ne.jp/ocf-blog)
  - [CALS/EC 電子納品に関する要領・基準](http://www.cals-ed.go.jp/)

[Category:CADファイルフォーマット](https://ja.wikipedia.org/wiki/Category:CADファイルフォーマット "wikilink") [Category:建設](https://ja.wikipedia.org/wiki/Category:建設 "wikilink") [Category:国土交通省](https://ja.wikipedia.org/wiki/Category:国土交通省 "wikilink")