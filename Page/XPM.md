> この記事は[XPM](https://ja.wikipedia.org/wiki/XPM)から翻訳されています。


**XPM** (X PixMap) は[X Window Systemで使用されるテキスト](../Page/X_Window_System.md "wikilink") ([ASCII](../Page/ASCII.md "wikilink")) の画像[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")である。[1989年](../Page/1989年.md "wikilink")INRIA（[フランス](https://ja.wikipedia.org/wiki/フランス "wikilink")国立電子計算機、制御研究所）のDaniel Dardailler と Colas Nahabooによって作られた。その後、Arnaud Le Horsにより拡張された。名前の通り[ピクセル](../Page/ピクセル.md "wikilink")（画素）による[ビットマップ画像](../Page/ビットマップ画像.md "wikilink")フォーマットである。主な用途は[アイコン](../Page/アイコン.md "wikilink")の画像の作成であり、透過色もサポートしている。文法は単純で[C言語](../Page/C言語.md "wikilink")の2次元文字[配列](../Page/配列.md "wikilink")定数形式で記述される。

## データ形式

内容は最初に大きさや色数、ホットスポットの定義部分、次に使用している色の定義部分があり最後に1ライン毎のピクセルの羅列が続く。 尚、色の指定は[X Window Systemなどで使用される色名又は](../Page/X_Window_System.md "wikilink")16進数で行なう。

以下にXPM形式の典型的な例を示す。

`/* XPM */`
`static char * roundb_xpm[] = {`
`/* width height ncolors cpp [x_hot y_hot] */`
`"13 13 5 2 7 7",`
`/* colors */`
`"  s none  m none  c none",`
`". s topShadowColor m white c lightblue",`
`"X s iconColor1 m black c black",`
`"o s bottomShadowColor m black c #646464646464",`
`"O s selectColor m white c red",`
`/* pixels */`
`"                          ",`
`"          . . .           ",`
`"      . . X X X o o       ",`
`"    . X X X X X X X o     ",`
`"    . X X X X X X X o     ",`
`"  . X X X X O X X X X o   ",`
`"  . X X X O O O X X X o   ",`
`"  . X X X X O X X X X o   ",`
`"    . X X X X X X X o     ",`
`"    . X X X X X X X o     ",`
`"      o o X X X o o       ",`
`"          o o o           ",`
`"                          "`
`}; `

## 外部リンク

  - [The XPM format and library](http://koala.ilog.fr/lehors/xpm.html)
  - [The XPM Story](http://www.w3.org/People/danield/xpm_story.html)
  - [Joker's INN](http://www.urban.ne.jp/home/kanemori/dotnet/img2xpm/index.html)  XPMデータについて視覚的で、分かりやすい解説がある。

[Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink")