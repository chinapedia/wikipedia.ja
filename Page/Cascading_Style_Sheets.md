> この記事は[Cascading Style Sheets](https://ja.wikipedia.org/wiki/Cascading_Style_Sheets)から翻訳されています。


**Cascading Style Sheets**（CSS、カスケーディング・スタイル・シート、カスケード・スタイル・シート、）は、[HTML](../Page/HyperText_Markup_Language.md "wikilink") や [XML](../Page/Extensible_Markup_Language.md "wikilink") の要素をどのように修飾（表示）するかを指示する仕様の一つで、[World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink") (W3C) がとりまとめ[勧告する](https://ja.wikipedia.org/wiki/W3C勧告 "wikilink")。文書の*構造*と*体裁*を[分離させるという理念を実現するために提唱された](../Page/関心の分離.md "wikilink")[スタイルシート](../Page/スタイルシート.md "wikilink")の具体的な仕様の一つ。

CSSはHTMLで表現可能と考えられるデザインの大部分を実現できる要素を取り入れつつ、新たなデザイン機能を備える。以下の点を特徴とする。

  - ページを表示するメディアに合わせてスタイルシートを切り替えることで、メディアごとに表示を変化させることができる。
  - [ユーザーエージェント](../Page/ユーザーエージェント.md "wikilink")（多くの場合[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")）、[ウェブサイト](../Page/ウェブサイト.md "wikilink")制作者、ユーザがそれぞれ定義したCSSのもたらす効果を重ね合わせる（カスケードする）ことができる。\[1\]

CSSは、[1994年](../Page/1994年.md "wikilink")に[WWW生誕の地である](../Page/World_Wide_Web.md "wikilink")[CERNに勤務する](../Page/欧州原子核研究機構.md "wikilink")[ホーコン・ウィウム・リー](../Page/ホーコン・ウィウム・リー.md "wikilink")により提唱された。

## 記述

スタイルの情報は読み込む内容（作成者スタイルシート）やユーザーエージェントの設定（ユーザースタイルシート）の2か所に記載できる。ユーザーエージェントも独自のスタイル（デフォルトスタイルシート）を持っている。

作成者スタイルシートはマークアップ文書の中に直接記述するか、別文書として読み込ませる形で利用される。CSSの利便性を最大限発揮するために、別文書として読み込ませる事が推奨されている。

### 記述方法

ここではCSS Level 2について説明する。CSSの文法は異なるレベル間でも後方互換性を持つように設計されており、例えばCSS Level 1で書かれたスタイルシートを CSS Level 2として扱うことも可能である（ただし一部に解釈の相違などに伴う非互換部分も存在する）。CSSでは要素にスタイルを与えるため、次のような仕様が定められている。

以下のCSS断片を例にとる。

``` css
p#id { color : #ff3300 }
```

  - "{" から "}" までの部分を**宣言ブロック**という
  - "p\#id" を**セレクタ**（選択子）といい、スタイルが適用される対象をしめす
  - 宣言ブロックとセレクタを合わせて**規則集合**という
  - "color : \#ff3300" 部分を**宣言**という
  - 宣言の内、":" より前（上例では "color"）を**プロパティ**（特性）という
  - 宣言の内、":" より後（上例では "\#ff3300"）を**値**という

上例の CSS 断片を適用すると宣言している文書のうち、セレクタが指定しているものと一致する部位（HTML 文書においては要素、要素の親子関係、特定のクラス、ID など）に、宣言ブロック内の宣言が適用される。宣言は、「プロパティ:値」か、「空（何も記述しない）」のどちらかで構成され、プロパティ、":"、値の前後には空白文字（スペース、タブ、改行など）を自由に入れられ、また";"で区切ることにより宣言を並べて書くことができる。

上例は HTML 文書に適用する場合、「id という ID を持った p 要素の文字色を赤FF(=255)、緑33(=51)、青0にせよ」という指定を意味する。

``` css
color : #ff3300;
width : 35%
```

``` css
color : "#0033ff";
width : '53%'
```

このような宣言があったとき、後者二つは""や''を付したために不正である。なぜなら、""や''で囲ったものは文字列として扱われ、colorプロパティが取りうる色の値（\#rrggbb、rgb(\[0-255\],\[0-255\],\[0-255\])、または、blackやredなどのキーワードなど）ではないからである。

``` css
p#id { color: #ff3300 }
p#id { font-size: 24px }
```

は、

``` css
p#id { color: #ff3300; font-size: 24px }
```

と等価である。;は前者のように宣言をセレクタに一つずつ書いてあるのを、ひとつのセレクタのブロックで記述するときに宣言を分けるのに使う。そのため、必ずしも宣言に;をつけるのを強制するものではない。

セレクタは、実装レベルの高いブラウザならばどの属性であってもCSSを適用することが可能であり、この場合IDに関する属性セレクタであるので、\#idは\[id="id"\]と等価である。セレクタの簡単なマッチングが可能である。 そのほかHTMLタグに対する適用、文書構造からみた子・兄妹構造へ適用するセレクタ、更にはリンクや動的な表現・言語に関する疑似クラス(:link、:hover、:lang)などがある。

### 優先順位

CSSは必ずしも一つのところで一意に指定できず、そのため指定内容の衝突を避けるために優先順位がユーザーエージェントによって計算される。その結果は、以下のような条件により算出される。

  - 作成者スタイルシートはユーザースタイルシートより優先される
  - デフォルトスタイルシートは他のスタイルシートを優先する
  - 最重要指定されている宣言はユーザースタイルシートが作成者スタイルシートより優先される（CSS1では逆）
  - 外部から読み込んだものは読み込んだ先とまとめて扱う
  - 詳細度によって整理する
      - そのセレクタ内で指定先を一意に決められるもの（IDの類）が多い方を優先する
      - IDの類による優先順位が同じ場合は、属性や擬似クラスの数が多い方を優先する
      - それでも優先順位が決まらない場合は、要素の数が多い方を優先する
  - これでもまだ優先順位が同一の場合、作成者スタイルシートにおいて以下の順で優先する
    1.  インラインのもの
    2.  外部からのもの
  - HTMLのalign属性など、CSS以外によるスタイルの指定は、それと等価なCSSによるスタイル指定が製作者スタイルシートの先頭にあるものとして扱う。ただし、これらの詳細度は最も低いものとする（CSS1においては要素名による指定を一つだけ含むセレクタと同じ詳細度）

記載可能な方法の詳細は次の通りで、一般的に優先される順位で並び替えている（CSS2で最重要指定の優先順位の仕様が変更されている、勧告6章4）。

1.  ユーザスタイルシート中で最重要指定された宣言 - ユーザーエージェントの設定のスタイルの中で\!importantを宣言に付加する
2.  作成者スタイルシート中で最重要指定された宣言 - 作成者が内容に付随させたスタイル中で\!importantを宣言に付加する。
3.  作成者スタイルシート中の通常の宣言
4.  ユーザースタイルシート中の通常の宣言
5.  デフォルトスタイルシートの宣言

作成者スタイルシートの記述方法による優先順位は以下の通り。

1.  特定の要素にスタイルを記述する
2.  HTMLやXMLのヘッダ部にそのページ全体を対象にスタイルを定義する
3.  CSSのみを記述した外部ファイルを用意し、HTMLファイルのヘッダ部からリンクを張ってスタイルを参照させる

## 勧告等

CSSの仕様にはレベルという段階があり、2011年11月段階で、Level 1 から Level 4 までの仕様が公開されている。

### Cascading Style Sheets, level 1 (CSS1), 勧告 1996年12月

  - [フォント](../Page/フォント.md "wikilink")[プロパティ](../Page/プロパティ.md "wikilink")
  - [色](../Page/色.md "wikilink")および[背景](../Page/背景.md "wikilink")のプロパティ
  - [テキスト](../Page/テキスト.md "wikilink")プロパティ
      - 語間の調整
      - 行寄せ
  - ボックスプロパティ
      - マージン
      - ボーダー
      - パディング
  - 類別プロパティ
      - 表示
      - リスト

**ボックスモデルの参考図**

<div style="border:1px dotted #999999;background-color:#ffffff;width:21em;padding:1em;">

マージン

<div style="border:1px solid #4d8ca5;background-color:#6cb5df;width:19em;padding:1em;">

ボーダー

<div style="border:1px solid #4d8ca5;background-color:#00f3f3;width:17em;padding:1em;">

パディング

<div style="border:1px solid #4d8ca5;background-color:#00f3f3;width:15em;padding:1em;">

内容

</div>

パディング

</div>

ボーダー

</div>

マージン

</div>

ボックスに**width**属性を設定したとき、[W3C](../Page/World_Wide_Web_Consortium.md "wikilink") のボックスのモデルでは内容の横幅であると解釈される。そしてパディングとボーダー分の横幅は要素の横幅に追加される。

他方[マイクロソフト](../Page/マイクロソフト.md "wikilink")のボックスのモデルでは width 属性は内容の横幅とパディングとボーダー分を足したもの、すなわち要素全ての横幅になる\[2\]。そのためInternet Explorer5.5以下と6.0以上およびInternet Explorer以外のWebブラウザでの表示を近づけるためには、パディングとボーダーを0にする、もしくは[CSSハック](https://ja.wikipedia.org/wiki/CSSハック "wikilink")を使う必要がある。

Internet Explorer 6 では DOCTYPE が正確ならば標準準拠モードに移行できる（ただXMLやXHTMLの場合、XML宣言を仕様通り書くと[過去互換モードでレンダリングされるバグがある](https://ja.wikipedia.org/wiki/互換モード "wikilink")）。

### Cascading Style Sheets, level 2 (CSS2), 勧告 1998年5月

CSS2 は CSS1 の上位互換。幾つかの概念の追加・拡大・改訂が行われた。

具体的には表示媒体（モニターや TV、紙媒体など）によって自動的にスタイルシートを変更できるようにし、それに附随して[音声ブラウザ](https://ja.wikipedia.org/wiki/音声ブラウザ "wikilink")への対応、印刷媒体への対応が行われ、フォントなどの表示機能の拡張や、ボックスの概念の修正などが行われた。

ただし2002年頃以降に発表されたCSS対応UAで、これを仕様と見なしているものは存在せず、実質的に、CSS2.1に仕様としての役割を委ねた形になっている。CSS2勧告の仕様書にアクセスすると、CSS2は管理されておらず、仕様の参照や実装はCSS 2.1を基にせよと奨励する注意書きがある。

### Cascading Style Sheets, level 2 revision 1 (CSS 2.1), 勧告 2011年6月

CSS2の改訂版。CSS2仕様書の定義が不明瞭であったことから各ユーザーエージェントのCSS2実装に非互換が生じたことから、曖昧な記述を明確にするといった改訂が行われた。また、text-shadowプロパティのように、CSS2で策定されていながら長い間実装が行われなかったもの、displayプロパティのrun-in値のように、複数のユーザーエージェントで相互運用性を確保できなかった機能は削除されている。それらはCSS3以降のレベルで定義され直すことになる。

CSSの実装に際してベンダは、2002年頃からCSS2.1を基本仕様と見なしている。

### Cascading Style Sheets, level 3 (CSS3)

CSS3以降ではCSS 2.1を中核とし、新たな機能の追加や改良を[モジュール](../Page/モジュール.md "wikilink")とすることで実現するものとする\[3\]。ユーザーエージェントは各モジュールへ対応するか否かを自由に選択できるようになる他、縦方向の書字や、HTML以外の規格にまで関与した内容となっている。2018年7月現在で勧告されているモジュールは以下の通り。

<table>
<caption>Summary of main module-specifications[4]</caption>
<thead>
<tr class="header">
<th><p>Module</p></th>
<th><p>Specification title</p></th>
<th><p>Status</p></th>
<th><p>Date</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><samp>css3-background</samp></p></td>
<td><p><a href="http://www.w3.org/TR/css3-background/">CSS Backgrounds and Borders Module Level 3</a> </p></td>
<td><p><em>Candidate</em> Rec.</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><samp>css3-box</samp></p></td>
<td><p><a href="http://www.w3.org/TR/css3-box">CSS basic box model</a></p></td>
<td><p>Working <em>Draft</em>,</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><samp>css-cascade-3</samp></p></td>
<td><p><a href="http://www.w3.org/TR/css-cascade-3/">CSS Cascading and Inheritance Level 3</a> </p></td>
<td><p><em>Candidate</em> Rec.</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><samp>css3-color</samp></p></td>
<td><p><a href="http://www.w3.org/TR/css3-color">CSS Color Module Level 3</a></p></td>
<td><p><em>Recommendation</em></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><samp>css3-content</samp></p></td>
<td><p><a href="http://www.w3.org/TR/css-content-3/">CSS3 Generated and Replaced Content Module</a> </p></td>
<td><p>Working <em>Draft</em></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><samp>css-fonts-3</samp></p></td>
<td><p><a href="http://www.w3.org/TR/css-fonts-3/">CSS Fonts Module Level 3</a></p></td>
<td><p><em>Candidate</em> Rec.</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><samp>css3-gcpm</samp></p></td>
<td><p><a href="http://www.w3.org/TR/css-gcpm-3/">CSS Generated Content for Paged Media Module</a></p></td>
<td><p>Working <em>Draft</em></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><samp>css3-layout</samp></p></td>
<td><p><a href="http://www.w3.org/TR/css-template-3/">CSS Template Layout Module</a></p></td>
<td><p><em>Note</em></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><samp>css3-mediaqueries</samp> </p></td>
<td><p><a href="http://www.w3.org/TR/css3-mediaqueries/">Media Queries</a></p></td>
<td><p><em>Recommendation</em></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><samp>mediaqueries-4</samp> </p></td>
<td><p><a href="https://www.w3.org/TR/mediaqueries-4/">Media Queries Level 4</a></p></td>
<td><p><em>Candidate</em> Rec.</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><samp>css3-multicol</samp> </p></td>
<td><p><a href="https://www.w3.org/TR/css-multicol-1/">Multi-column Layout Module Level 1</a></p></td>
<td><p>Working <em>Draft</em></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><samp>css3-page</samp></p></td>
<td><p><a href="http://www.w3.org/TR/css3-page/">CSS Paged Media Module Level 3</a></p></td>
<td><p>Working <em>Draft</em></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><samp>selectors-3</samp></p></td>
<td><p><a href="http://www.w3.org/TR/css3-selectors/">Selectors Level 3</a></p></td>
<td><p><em>Candidate</em> Rec.</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><samp>selectors-4</samp></p></td>
<td><p><a href="https://www.w3.org/TR/selectors-4/">Selectors Level 4</a></p></td>
<td><p>Working <em>Draft</em></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><samp>css3-ui</samp></p></td>
<td><p><a href="http://www.w3.org/TR/css-ui-3/">CSS Basic User Interface Module Level 3 (CSS3 UI)</a></p></td>
<td><p><em>Recommendation</em></p></td>
<td></td>
</tr>
</tbody>
</table>

### Cascading Style Sheets, Level 4 (CSS4)

CSS4はモジュール化されたため、単一の統合された仕様は存在せず、「Level 4」モジュールの総称となる。

Level 4モジュールで追加される機能は、Level 3モジュールで未定義だった新しい機能のほか、草案に一度含まれながら、相互運用性を十分に確保出来ず仕様から省かれた機能からなる。

未だに勧告候補に至っていないLevel 3モジュールが存在する中、既にLevel 4モジュールの公開草案がいくつか公開されている。

## 脚注

### 注釈

### 出典

<references />

## 関連項目

  - [スタイルシート](../Page/スタイルシート.md "wikilink")
      - [XSL](../Page/Extensible_Stylesheet_Language.md "wikilink")
      - [DSSSL](../Page/Document_Style_Semantics_and_Specification_Language.md "wikilink")
  - [リキッドデザイン](https://ja.wikipedia.org/wiki/リキッドデザイン "wikilink")
  - [ホーコン・ウィウム・リー](../Page/ホーコン・ウィウム・リー.md "wikilink")
  - CSSの拡張
      - [LESS](https://ja.wikipedia.org/wiki/LESS "wikilink")
      - [Sass](https://ja.wikipedia.org/wiki/Sass "wikilink")

## 外部リンク

  - W3C
      - [Cascading Style Sheets home page](http://www.w3.org/Style/CSS/)
      - [Cascading Style Sheets, level 1 (CSS1)](http://www.w3.org/TR/REC-CSS1/)
      - [Cascading Style Sheets, level 2 (CSS2)](http://www.w3.org/TR/2008/REC-CSS2-20080411/)
      - [Cascading Style Sheets, level 2 revision 1 (CSS2.1)](http://www.w3.org/TR/CSS2/)
      - [Cascading Style Sheets (CSS) Snapshots](http://www.w3.org/TR/CSS/)
      - [CSS current work & how to participate](http://www.w3.org/Style/CSS/current-work)
  - 勧告・ノートの非公式日本語訳
      - [段階スタイルシート 水準1(CSS1) 標準情報(TR) TR X 0011:1998](http://www.y-adagio.com/public/standards/css1/toc.htm)
      - [段階スタイルシート 水準2(CSS2) 標準情報(TR) TR X 0032:2000](http://www.y-adagio.com/public/standards/tr_css2/toc.html)
      - [CSS2勧告邦訳について](http://www.swlab.it.okayama-u.ac.jp/man/rec-css2/)
      - [CSS2.1勧告の日本語訳について](http://momdo.s35.xrea.com/web-html-test/spec/CSS21/)
      - [セレクタ Level 3](http://standards.mitsue.co.jp/resources/w3c/TR/css3-selectors/)
      - [CSS 名前空間モジュール](http://standards.mitsue.co.jp/resources/w3c/TR/css3-namespace/)
      - [CSS カラーモジュール Level 3](http://standards.mitsue.co.jp/resources/w3c/TR/css3-color/)
      - [CSS スナップショット 2010](http://standards.mitsue.co.jp/resources/w3c/TR/css-2010/)
  - ウェブブラウザ
      - [MSDN Library - Cascading Style Sheets](http://msdn.microsoft.com/ja-jp/library/ms531205.aspx)
      - [CSS - MDC](https://developer.mozilla.org/ja/css)
  - その他
      - [W3C CSS 検証サービス](http://jigsaw.w3.org/css-validator/)
      - [CSS2 tests by Peter-Paul Koch](http://www.quirksmode.org/)
      - [Box model hack](http://www.tantek.com/CSS/Examples/boxmodelhack.html)
      - [Another box model workaround](http://webfx.eae.net/dhtml/boxsizing/boxsizing.html)
      - [CSS Panic Guide](http://thenoodleincident.com/tutorials/css/) - a fast resource
      - [CSS-discus wiki](http://css-discuss.incutio.com/) - A wiki dedicated to CSS
      - [Acid2 Test](http://webstandards.org/act/acid2/test.html)

[mk:CSS селектори](https://ja.wikipedia.org/wiki/mk:CSS_селектори "wikilink")

[Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:World_Wide_Web](https://ja.wikipedia.org/wiki/Category:World_Wide_Web "wikilink") [Category:スタイルシート言語](https://ja.wikipedia.org/wiki/Category:スタイルシート言語 "wikilink") [Category:HTML](https://ja.wikipedia.org/wiki/Category:HTML "wikilink")

1.  ただし拡張・修正の続いている CSS 仕様の全てを完全に実装しているユーザーエージェントは事実上皆無といってよく、実際シェアで多数を占めるユーザエージェントは部分対応にすぎない。しかし実用上支障のないレベルの実装はされてきており、なおかつ表現の互換性についても考慮されてきている。
2.  [:en:Internet Explorer box model bug](https://ja.wikipedia.org/wiki/:en:Internet_Explorer_box_model_bug "wikilink")
3.  [§2.1 CSS Levels, 『CSS Snapshot 2015』](http://www.w3.org/TR/CSS/#css-levels) [W3C](https://ja.wikipedia.org/wiki/W3C "wikilink")
4.