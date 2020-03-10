> この記事は[Vector Markup Language](https://ja.wikipedia.org/wiki/Vector_Markup_Language)から翻訳されています。


**Vector Markup Language** （**VML**、ベクトルマークアップ言語） は、[ベクター画像を描画するための](https://ja.wikipedia.org/wiki/ベクターイメージ "wikilink") [XML](../Page/Extensible_Markup_Language.md "wikilink") 言語である。 VML は[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に [Microsoft](../Page/マイクロソフト.md "wikilink"), [Macromedia](../Page/マクロメディア.md "wikilink"), [HP](../Page/ヒューレット・パッカード.md "wikilink"), [Autodesk](https://ja.wikipedia.org/wiki/オートデスク "wikilink"), [Visio](https://ja.wikipedia.org/wiki/ビジオ_\(会社\) "wikilink") の 5 社によって [W3C](../Page/World_Wide_Web_Consortium.md "wikilink") に提出された。 その一方で [Adobe](../Page/アドビシステムズ.md "wikilink") や [Sun](../Page/サン・マイクロシステムズ.md "wikilink") など数社は、競合する仕様である [PGML](https://ja.wikipedia.org/wiki/Precision_Graphics_Markup_Language "wikilink") を提出した。\[1\] この 2 つの仕様は後に統合・改良され、その結果 [SVG](../Page/Scalable_Vector_Graphics.md "wikilink") が生まれた。

VML は W3C標準にはならなかったものの、[Internet Explorer](../Page/Internet_Explorer.md "wikilink") 5.0 以降及び [Microsoft Office](../Page/Microsoft_Office.md "wikilink") 2000 以降の製品に実装されている。

[Google マップや非](https://ja.wikipedia.org/wiki/Google_マップ "wikilink")[ActiveX](../Page/ActiveX.md "wikilink")型[電子国土Webシステム](https://ja.wikipedia.org/wiki/電子国土Webシステム "wikilink")のβ2版では、Internet Explorer 5.5 以降のブラウザでベクトル画像を描画する手段として VML を採用している。\[2\],\[3\]

## コード例

以下に、赤色で塗りつぶされた楕円を描画するコードの例を示す。

``` xml
<v:oval style="position:absolute; left:0; top:0;
               width:100pt; height:50pt"
               fillcolor="red">
</v:oval>
```

参考までに、SVG でこれと等価な図形を描くためのコードを以下に示す。

``` xml
<ellipse cx="50" cy="25" rx="50" ry="25" style="fill:red;"/>
```

## 注釈

## 関連項目

  - [Office Open XML](https://ja.wikipedia.org/wiki/Office_Open_XML "wikilink") （仕様の一部となっている）

## 外部リンク

  - [Macromedia、Microsoftなどが2次元グラフィックス記述言語「VML」をW3Cに提出](http://www.watch.impress.co.jp/internet/www/article/980529/vml.htm)
  - [Vector Markup Language (VML)](http://www.w3.org/TR/1998/NOTE-VML-19980513)
  - [Scalable Vector Graphics (SVG)](http://www.w3.org/Graphics/SVG/)

[Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink") [Category:ベクターグラフィックス](https://ja.wikipedia.org/wiki/Category:ベクターグラフィックス "wikilink")

1.  [PGML](http://www.w3.org/TR/1998/NOTE-PGML-19980410)
2.  [Google Maps](http://www.google.com/apis/maps/documentation/#XHTML_and_VML)
3.  [非ActiveX型電子国土Webシステムに関する技術情報（Ver.β2.0）](http://portal.cyberjapan.jp/nonactivex2.htm)