> この記事は[HP-GL](https://ja.wikipedia.org/wiki/HP-GL)から翻訳されています。


**HP-GL** または **HPGL** とは、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")の[プロッタ](https://ja.wikipedia.org/wiki/プロッタ "wikilink")で使われていた初期のプリンタ制御言語である。 の略。後に、ほとんどすべてのプロッタの標準となった。なおプロッタメーカー独自の拡張仕様も存在する。

2文字のコードとオプションパラメータからなる。たとえば、次のような文字列を送れば、ページに円弧が描かれる。

`AA100,100,50;`

これは、*Arc Absolute* （絶対位置の円弧）を意味し、ページの (100,100) を中心座標とする円弧を現在のペン位置から反時計周りに50度描く。4番目のオプションパラメータ（この例では使っていない）は円弧の分解能で、デフォルトは5度である。

典型的な HP-GL ファイルでは、いくつかのセットアップコマンドで始まり、一連の長いグラフィックスコマンドが続く。たとえば次のようになる。最後のセミコロン記号は区切り文字で、コマンドの区切りを示す。

| コマンド                       | 意味                                        |
| -------------------------- | ----------------------------------------- |
| IN;                        | 初期化して、プロット処理を開始                           |
| IP;                        | 初期位置（原点）の設定。ここではデフォルトの (0,0)              |
| SC0,100,0,100;             | ページの X と Y の両方向へ 0-100 のスケールとする           |
| SP1;                       | ペン 1 を選択                                  |
| PU0,0;                     | 次の動作に備えてペンを開始位置に移動                        |
| PD100,0,100,100,0,100,0,0; | ペンを下げて指定座標へ移動（ページの周囲に四角形を描く）              |
| PU50,50;                   | ペンを上げて (50,50) へ移動                        |
| CI25;                      | 半径 25 の円を描く                               |
| SS;                        | 標準フォントを選択                                 |
| DT\*,1;                    | テキストの区切りをアスタリスクに設定し、それを印刷させない（ 1 は「真」の意味） |
| PU20,80;                   | ペンを上げて (20,80) へ移動                        |
| LBHello World\*;           | 文字を描く                                     |

HP-GL ファイルの例

座標系は、それらのプロッタのうちの1つがサポートできる最小単位に基づき、25 [µm](../Page/マイクロメートル.md "wikilink") （つまり 1/40[mm](../Page/ミリメートル.md "wikilink")、1/1016[インチ](../Page/インチ.md "wikilink")）に定められた。座標空間は正または負の[浮動小数点数](../Page/浮動小数点数.md "wikilink")で、厳密には±2<sup>30</sup>である。[座標原点](https://ja.wikipedia.org/wiki/座標原点 "wikilink")は小型プロッタにおいて盤面の左下、大型プロッタ（HP-GL II）において盤面の中央にある。

## マニュアル

  -
  -
## 外部リンク

  - [Hewlett Packard Graphics Language Commands](http://www.sxlist.com/techref/language/hpgl/commands.htm)
  - [HPGL Overview](http://cstep.luberth.com/hpgl.htm)
  - [Converter from HPGL (LGPL Licence)](http://hpgs.berlios.de/)
  - [PLT Viewer Homepage](http://www.pltviewer.com/) A quick PLT and HPGL viewer, converter and editor with powerful printing system.

[Category:ページ記述言語](https://ja.wikipedia.org/wiki/Category:ページ記述言語 "wikilink") [Category:ベクターグラフィックス](https://ja.wikipedia.org/wiki/Category:ベクターグラフィックス "wikilink") [Category:ヒューレット・パッカードの製品](https://ja.wikipedia.org/wiki/Category:ヒューレット・パッカードの製品 "wikilink")