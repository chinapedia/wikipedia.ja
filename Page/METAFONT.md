> この記事は[METAFONT](https://ja.wikipedia.org/wiki/METAFONT)から翻訳されています。


**METAFONT**（**メタフォント**）は、[フォント](../Page/フォント.md "wikilink")作成用の[コンピュータ](../Page/コンピュータ.md "wikilink")[プログラムである](../Page/プログラム_\(コンピュータ\).md "wikilink")。組版システム [](../Page/TeX.md "wikilink") とともに[ドナルド・クヌース](../Page/ドナルド・クヌース.md "wikilink")により開発された。

## 概要

METAFONT は文字の形を描くプログラムソースファイルを読み込んで、[組版](../Page/組版.md "wikilink")用の情報（文字の大きさや[合字](../Page/合字.md "wikilink")などの情報）を持つフォントメトリックファイルと、文字の形の情報（グリフデータ）を持つビットマップフォントファイルを生成するシステムである。フォントファイルを生成する際にいくつかのパラメータを調整することで、同一のソースファイルから幾種ものフォントを生成することも可能であり、それが名称の由来にもなっている。生成する文字の輪郭には、[ベジェ曲線](../Page/ベジェ曲線.md "wikilink")が用いられる。

METAFONT は組版システム  とともに[ドナルド・クヌース](../Page/ドナルド・クヌース.md "wikilink")により開発された。組版処理をする際、フォントデザインに応じた合字や[カーニング](https://ja.wikipedia.org/wiki/カーニング "wikilink")などの情報が必要となる。 では数式組版などにも力点が置かれているが、その際はさらに豊富な組版情報をフォント自体が持つことが期待される。METAFONT は、そのような組版情報を持ったフォントを作成する必要から開発された。METAFONT は  と同様に[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であり、いくつかのプラットフォームに移植されている。

METAFONT で生成したフォントを他の形式（[Type1など](https://ja.wikipedia.org/wiki/PostScriptフォント#Type_1 "wikilink")）に変換するプログラムも開発されている。

また、METAFONT 用のプログラムと似た構文のプログラムで [PostScript](../Page/PostScript.md "wikilink") 形式の画像ファイルを生成できる [MetaPost](../Page/MetaPost.md "wikilink") も開発されている。

## プログラミング言語としての METAFONT

[プログラミング言語](../Page/プログラミング言語.md "wikilink")としては、METAFONT は以下のような特徴を持つ。

  - フォントメトリックファイルとフォントグリフファイルを生成する
  - フォント作成に特化した各種命令がある
  - 数学的な意味の[方程式](../Page/方程式.md "wikilink")がそのまま扱え、[連立一次方程式](https://ja.wikipedia.org/wiki/連立一次方程式 "wikilink")によって変数の値を与えることができる
  - [演算子](../Page/演算子.md "wikilink")の意味の変更までできる柔軟なカスタマイズ可能性を持つ

### プログラム例

簡単なサンプルプログラムとその出力を示す。

[thumb](https://ja.wikipedia.org/wiki/ファイル:metafont_sample_1.jpg "wikilink")

`1: beginchar(65,10pt#,10pt#,0pt#);`
`2: pickup pencircle xscaled 1.2pt yscaled 0.5pt rotated 120;`
`3: z1=(0.1w,0.75h);`
`4: z2-z1=whatever*(8,1);`
`5: x2=0.9w;`
`6: z3=(0.8w,0.1h);`
`7: draw z1--z2{z1-z2}..{z2-z1}z3;`
`8: labels(1,2,3);`
`9: endchar;`
`10: end.`
`行番号は説明のために付けてある。`

  - 1行目では文字の情報を定めている。この例では、[文字コード](../Page/文字コード.md "wikilink")65の文字を幅10pt, 高さ10pt, 深さ0pt（幅と高さが同じ値だが、引数はこの順）で作成することを宣言している。
  - 2行目では文字を描くのに用いる“ペン”を定義している。このペンは単位円を縦横異なる比率で拡大縮小してできる楕円を120度回転させたもので、次の図のような形を持つ。

[ファイル:metafont_sample_pen1.jpg](https://ja.wikipedia.org/wiki/ファイル:metafont_sample_pen1.jpg "wikilink")

  - 3行目から6行目までで3つの点の位置を定めている。3つの点はそれぞれ z1, z2, z3 で、図中では1,2,3とラベルを付けて表示してある。w と h の値は1行目の宣言によって決められて、この例では左下の座標が (0,0)、右下が (w,0)、右上が (w,h) 等となる。
  - z1 と z3 はそれぞれ3行目と6行目で明示的に決められる。
  - z2 の決め方に METAFONT の特徴がよく現れている。4行目の段階では「z1 から z2 へ向かう[ベクトル](../Page/ベクトル.md "wikilink")が (8,1) という成分を持つベクトルの何倍かになっている」ことだけが定義されている。続く5行目で z2 のx成分が明示的に与えられると、z2 の位置が自動的に決定される。METAFONT 内部では、4行目の段階で一次方程式が作られたのちに5行目と併せて解かれている。
  - 7行目で文字を描く。まず z1 から z2 へ直線を引き、z2 からは、z2 から z1 へと向かう方向へ線を引き始める。その線は滑らかな曲線を描きながら z3 へと向かうのだが、最終的に z3 へたどり着くときには z1 から z2 へと向かう方向を向くようにする。
  - 8行目では、3つの点にラベルを付けて表示させている。
  - 9行目で、1行目から続いた文字コード 65 の文字は終了する。さらに他のコードの文字を描きたければ1行目と同様に続けることもできる。
  - 10行目で1文字しかないこのフォントセットが終了する。

（他のプログラム例が[w:de:Metafont](https://ja.wikipedia.org/wiki/w:de:Metafont "wikilink")にも）

## 関連項目

  - [MetaPost](../Page/MetaPost.md "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:MetaPost "wikilink"))
  - [Computer Modern](https://ja.wikipedia.org/wiki/Computer_Modern "wikilink") METAFONTで作られた、標準のフォント。

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:DTP](https://ja.wikipedia.org/wiki/Category:DTP "wikilink") [Category:TeX](https://ja.wikipedia.org/wiki/Category:TeX "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:書体](https://ja.wikipedia.org/wiki/Category:書体 "wikilink") [Category:ドナルド・クヌース](https://ja.wikipedia.org/wiki/Category:ドナルド・クヌース "wikilink")