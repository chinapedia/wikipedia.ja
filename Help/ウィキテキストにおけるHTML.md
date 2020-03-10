> この記事は[Help:HTML](https://ja.wikipedia.org/wiki/Help:HTML)から翻訳されています。


**記事編集時の[ウィキテキストの中での](https://ja.wikipedia.org/wiki/Wikipedia:ガイドブック_執筆する#既存の記事を編集するには "wikilink")[HTMLの使用](../Page/HyperText_Markup_Language.md "wikilink")**について解説します。HTMLにおける[HTML要素](../Page/HTML要素.md "wikilink")・属性のうち許容されている一部が使えます。それ以外ではそのまま表示されてしまいます。ウィキペディアでは一部の要素はHTMLの仕様とは振る舞いが異なります。またウィキペディアでは、出典を示すのに用いる`ref`要素など独自のウィキテキスト言語の要素が用意されています。

HTMLを使えば、ウィキテキスト言語でカバーできていないこともできます。`id`属性を利用してリンク先として指定したりといったこともできます\[1\]。

一方で、ウィキペディアではHTML要素の大部分をウィキテキスト言語で簡易的に記述できます。ウィキペディアで使用しているウィキテキスト言語によるマークアップ（ウィキマークアップ）については[Help:ページの編集などをご覧ください](https://ja.wikipedia.org/wiki/Help:ページの編集 "wikilink")。

## 使用できるHTML

次のHTML要素のみが使用できます\[2\]。

  - `abbr`
  - `b`
  - `bdi`
  - `bdo`
  - `blockquote`
  - `br`
  - `caption`
  - `cite`
  - `code`
  - `data`
  - `dd`
  - `del`
  - `dfn`
  - `div`
  - `dl`
  - `dt`
  - `em`
  - `h1`
  - `h2`
  - `h3`
  - `h4`
  - `h5`
  - `h6`
  - `hr`
  - `i`
  - `ins`
  - `kbd`
  - `li`
  - `mark`
  - `ol`
  - `p`
  - `pre`
  - `q`
  - `rb`
  - `rp`
  - `rt`
  - `ruby`
  - `s`
  - `samp`
  - `small`
  - `span`
  - `strong`
  - `sub`
  - `table`
  - `td`
  - `th`
  - `time`
  - `tr`
  - `u`
  - `var`
  - `wbr`

以下は、使用できますが[HTML5](https://ja.wikipedia.org/wiki/HTML5 "wikilink")で廃止された要素であり、ウィキペディアは最終的にHTML5で出力されるため使うべきではありません。代替方法は[:en:Wikipedia:HTML5](https://ja.wikipedia.org/wiki/:en:Wikipedia:HTML5 "wikilink")を参照。

  - `big`
  - `center`
  - `font`
  - `strike`
  - `tt`

上記のHTML要素について簡単に解説します。「〇〇に相当」と書かれている部分はウィキマークアップです。他の編集者との共同作業を円滑にするため、通常はHTMLではなくウィキマークアップを用いてください。

  - 見出し
    セクション編集ができないなど、違いについては[\#見出し](https://ja.wikipedia.org/wiki/#見出し "wikilink")節を参照。

      -  : 「ページ名」と同じレベルの見出しが生成されますので**実際には使用しないでください**。
         : `== 見出し ==`に相当。
         : `=== 見出し ===`に相当。
         : `==== 見出し ====`に相当。
         : `===== 見出し =====`に相当。
         : `====== 見出し ======`に相当。

  - 文字装飾

:;  : 強勢を示す（<em>sampleサンプル</em>）。

:;  : 重要性を示す（<strong>sampleサンプル</strong>）。

:;  : 他と区別したい文字。イタリック体。`''文字列''` に相当（<i>sampleサンプル</i>）。

:;  : 他と区別したい文字。ボールド体。`'''文字列'''` に相当（<b>sampleサンプル</b>）。

:;  : タイプライター体。**廃止**（代替：）。

:;  : サイズを大きく。**廃止**（代替：）。

:;  : 細目。サイズを小さく（代替：）（<small>sampleサンプル</small>）。でも同様。

:;  : 下付き文字（<sub>サンプル</sub>）。

:;  : 上付き文字（<sup>サンプル</sup>）。

:;  : 削除部分を示す（~~サンプル~~）。

:;  : 正しくなくなったことを示す（<s>サンプル</s>）。

:;  : 取り消し線を引く。**廃止**（代替：）。

:;  : 挿入部分を示す（<ins>サンプル</ins>）。

:;  : 下線を引く\[3\]。非推奨（代替：）（<u>サンプル</u>）。を使用するとよい。

:;  : フォントについて指定する。**廃止**（代替：など）。

:;  : ソースコードを示す（`サンプル`）。でも同様。

:;  : 変数を示す（<var>サンプル</var>）。でも同様。

:;  : 整形済みテキスト。ソースのまま表示する。ウィキテキスト中の先頭が空白で始まる行にほぼ相当。HTMLとの違いについては[\#Pre](https://ja.wikipedia.org/wiki/#Pre "wikilink")節を参照。

  -

  - レイアウト

:;  : パラグラフ。ウィキテキスト中の2回改行に相当。

:;  : インラインについてスタイル指定や言語の指定。`class` ・ CSS の `style` や `lang` などと併用。

:;  : ブロックについてスタイル指定。`class` や CSS の `style` などと併用。

:;  : 強制改行。主に表中での改行に使用する。なお、`<br>``</br>``<br/>` `<br />` は HTML ソースが生成される際にすべて `<br />` となりますので、どれを利用しても結果は同じです。これをどちらかに直すだけの編集はお控えください\[4\]。

:;  : テキストの中央揃え。**廃止**（代替： ）。を使用するとよい。

:;  : 段落の引用。

:;  : 出典・参照先。

:;  : 行中の引用。

:;  : セクション内での話題の区切りを示す。水平線。`----` に相当。

  -

  - リスト・箇条書き

:;  : 説明/定義リスト。次の  とあわせて `;` に相当。

:;  : 説明/定義する語。

:;  : 説明/定義する内容。`:` に相当。

:;  : 番号付き箇条書き。 とあわせて `#` に相当。

:;  : 番号なし箇条書き。 とあわせて `*` に相当。

:;  : 箇条書きの各項目。

  -

  - ルビ
    [Wikipedia:表記ガイドではこれらの要素の使用は](https://ja.wikipedia.org/wiki/Wikipedia:表記ガイド#読み仮名の要否 "wikilink")、表組みや情報テンプレート、囲みの引用文などの限られた状況下でのみ認めています。これら以外の場合は丸括弧を使って「漢字（かんじ）」とそのまま入力するか、・を使ってください。

      -  : ルビの開始/終了。
         : ルビの対象文字列。HTML5では不要。
         : ルビ。

        ルビ表示未対応の環境においてインラインに表示するルビを囲む記号。

  - 表

:;  : 表の外枠。開始は`{|`、終了は`|}` に相当。

:;  : 表のキャプション。`|+` に相当。

:;  : 横1列を定義する。`|-` に相当。

:;  : 見出しセル。`!` に相当。

:;  : データセル。`|` に相当。

  -

  - コメントアウト

:;  : `文字列` の部分をコメントアウト。

## 使用できないHTML

[\#使用できるHTML](https://ja.wikipedia.org/wiki/#使用できるHTML "wikilink")節で挙げられた以外のHTML要素はそのまま表示されます。

例えば、A要素（アンカー）を使った外部リンクは使用できません。以下のようになります。

<table>
<tbody>
<tr class="odd">
<td><p>マークアップ</p></td>
<td><pre class="moin"><code>&lt;a href=&quot;https://meta.wikimedia.org/&quot;&gt;メタウィキメディア・メインページ&lt;/a&gt;</code></pre></td>
</tr>
<tr class="even">
<td><p>表示結果</p></td>
<td><p><a href="https://meta.wikimedia.org/">メタウィキメディア・メインページ</a></p></td>
</tr>
<tr class="odd">
<td><p>生成されるソースコード</p></td>
<td><div class="sourceCode" id="cb2"><pre class="sourceCode html"><code class="sourceCode html"><span id="cb2-1"><a href="#cb2-1"></a><span class="kw">&lt;a</span><span class="ot"> href=</span><span class="st">&quot;</span><span class="er">&lt;</span><span class="st">a class=&quot;</span><span class="er">external</span><span class="ot"> free</span><span class="er">&quot;</span><span class="ot"> href=</span><span class="st">&quot;https://meta.wikimedia.org/&quot;</span><span class="kw">&gt;</span>https://meta.wikimedia.org/<span class="kw">&lt;/a&gt;</span>&quot;&gt;メタウィキメディア・メインページ<span class="kw">&lt;/a&gt;&lt;/td&gt;</span></span></code></pre></div></td>
</tr>
</tbody>
</table>

おそらく執筆者の意図と異なる結果となります。これはソースコードでおそらく上記のように変換されてしまうためです。

外部リンクのためには、かわりに角括弧で囲むウィキテキスト言語のマークアップを用います。

<table>
<caption>ウィキペディアにおける正しいマークアップ</caption>
<tbody>
<tr class="odd">
<td><p>マークアップ</p></td>
<td><pre class="moin"><code>[https://meta.wikimedia.org/ メタウィキメディア・メインページ]</code></pre></td>
</tr>
<tr class="even">
<td><p>表示結果</p></td>
<td><p><a href="https://meta.wikimedia.org/">メタウィキメディア・メインページ</a></p></td>
</tr>
<tr class="odd">
<td><p>生成されるソースコード</p></td>
<td><div class="sourceCode" id="cb2"><pre class="sourceCode html"><code class="sourceCode html"><span id="cb2-1"><a href="#cb2-1"></a><span class="kw">&lt;a</span><span class="ot"> class=</span><span class="st">&quot;external text&quot;</span><span class="ot"> href=</span><span class="st">&quot;https://meta.wikimedia.org/&quot;</span><span class="kw">&gt;</span>メタウィキメディア・メインページ<span class="kw">&lt;/a&gt;</span></span></code></pre></div></td>
</tr>
</tbody>
</table>

## 個別の注意

### 見出し

`<h1>`から`<h6>`までの見出し要素は、ウィキテキスト言語における`=`を使用したマークアップと同じほぼ表示結果となります。また同様に[目次にも表示されます](https://ja.wikipedia.org/wiki/#toctitle "wikilink")。違いは、「\[編集\]」リンクが付属していないことです。これを利用することで、特定のセクションからはセクション編集ができないようにすることが可能です。

以下のように記述すると。

``` html
<h4>サンプルの見出し（4レベル）</h4>
```

表示結果は次のようになります。

<h4>

サンプルの見出し（4レベル）

</h4>

### スタイル指定

<span> は行中のテキストのスタイルなどを指定する要素で、この要素の使用が推奨されます。<font> も同じことができる効果をもつ古くからある要素ですが、現在では HTML の仕様を策定している [World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink")(W3C) により非推奨となっています。

例えば以下2つの記述は、同じ表示結果が得られます。

``` html5
<span style="color:red">赤い</span>文字
```

``` html5
<font color="red">赤い</font>文字
```

<code>

<div>

</code> はブロック単位でスタイルを指定する要素です。

なお多くの場合には <code>

<div>

</code> や <span> を使ってスタイル指定をせずとも、既に用意された要素を使うほうが利用者に対して親切です。スタイルの指定に対応していない古いブラウザや、読み上げソフトを使用している場合などでも、執筆者の強調の意図が伝わります。

例えば、文中の言葉を強調したいときには、その文字列が強調されていることを明示する `<strong>` や `<em>`\[5\]といった要素が用意されています。

ウィキテキスト言語では `'''`で囲むことで強調要素が作成されます。見栄えも統一されるため、最初にウィキテキスト言語でも記述できないか考慮してください。

### Pre

ウィキテキスト中の `<pre>` 要素は、HTMLとは異なった振る舞いをします。要素で囲まれたテキストは、HTMLのように改行や空白が維持されますが、かつタグも見た通りに表示されます。これは、ウィキペディアでは、処理の途中でウィキテキスト言語の `<nowiki>` が組み合わさるためです。

以下のように記述すると、結果はその次のようになります。

``` html
<pre>This word is <b>bold</b>.    [[ウィキペディア|ウィキペディア]]の URL は[https://ja.wikipedia.org] です。{{PAGENAME}} </pre>
```

表示結果（注・囲いなどウィキペディアによるスタイルの指定も反映され表示されたものが実際の表示結果です）:

    This word is <b>bold</b>.    [[ウィキペディア|ウィキペディア]]の URL は[https://ja.wikipedia.org] です。{{PAGENAME}}

HTMLの `<pre>` 要素のような表示結果を得たい場合には、ウィキペディアでは行頭に半角スペースを入れてください。タグ等は展開しつつ改行や空白などをソース通りに維持したテキストを表示させたい場合です。以下のように記述します。

``` html
 This word is <b>bold</b>.    [[ウィキペディア|ウィキペディア]]の URL は[https://ja.wikipedia.org] です。{{PAGENAME}}
```

表示結果（上の表示結果の注に同じ）:

`This word is `<b>`bold`</b>`.    `[`ウィキペディア`](https://ja.wikipedia.org/wiki/ウィキペディア "wikilink")の` URL は`[`1`](https://ja.wikipedia.org)` です。`

### コメント

ウィキテキスト中で を使ったHTMLのコメントは、生成されたHTMLコード中にはいっさい現れません\[6\]。

### 属性

大部分の要素には `style` 属性があります。例えば

``` html5
<div style="font-size:80%">
これは<span style="color:red">赤い</span>テキストです。
</div>
```

は次を生成します。

<div style="font-size:80%">

これは<span style="color:red">赤い</span>テキストです。

</div>

また大部分の要素は、クラス（`class`）と ID を指定できます。クラスはスタイルシートと連動して、指定部分のスタイルを指定します。例えば

``` html5
<div class="infobox">インフォボックスの例</div>
```

<div class="infobox">

インフォボックスの例

</div>

は右のように生成されます。これは、 `infobox` クラスが [Mediawiki:Common.css](https://ja.wikipedia.org/wiki/MediaWiki:Common.css "wikilink") の記述によって右端揃えの浮動ボックスとして定義されているからです。

クラスと ID はJavaScriptのコードからHTML要素を参照するときにも使えます。例としてがあります。

他にも、例えば `title` 属性が利用できます。

``` html5
海抜<span title="6.1 km" style="border-bottom:1px dotted">20000 ft</span>
```

は次のように生成されます（点線の下線部の上にカーソルを置いた時のポップアップを指定しています）。

海抜<span title="6.1 km" style="border-bottom:1px dotted;">20000 ft</span>

## 例外

[MediaWiki名前空間にあるページの一部](https://ja.wikipedia.org/wiki/Help:名前空間 "wikilink")（ボタンのラベルなど）ではHTMLが使えません。タグがそのまま表示されます。

他方で純粋なHTML コードとして認識されるものもあり、その場合 HTMLしか使えず、ウィキテキスト言語はHTMLに変換されません。

サイト全体の CSS および JS スタイルシートおよび利用者指定の CSS や JS スタイルシート（[Help:外装の詳細設定参照](https://ja.wikipedia.org/wiki/Help:外装の詳細設定 "wikilink")）のページを表示すると、自動的に `<pre>` タグで囲まれているような体裁で表示されます。

## ウィキペディア独自の要素

HTML 要素以外にも、MediaWikiで使える`<` `>`で囲んだ要素があります。以下に代表的なものを紹介します。

### ref

`<ref> 文字列 </ref>`

[脚注を作ります](https://ja.wikipedia.org/wiki/Help:脚注 "wikilink")。`<references />`とセットで使います。[Help:脚注参照](https://ja.wikipedia.org/wiki/Help:脚注 "wikilink")。

### nowiki

` <nowiki> 文字列  `</nowiki>

HTMLタグ、ウィキマークアップを全て無効化します。

### gallery

`<gallery> 画像ファイル名|文字列 </gallery>`

画像を並べて描画します。横幅は自動的に折り返され閲覧環境に依存しません。[Help:画像の表示\#ギャラリー参照](https://ja.wikipedia.org/wiki/Help:画像の表示#ギャラリー "wikilink")。

### imagemap

画像をクリックした位置によって異なるリンク先を指定できます。[Help:画像の表示\#クリッカブル画像です](https://ja.wikipedia.org/wiki/Help:画像の表示#クリッカブル画像 "wikilink")。

### poem

`<poem> 文字列 </poem>`

詩や歌詞などの引用に用います。HTMLソース生成の際、`<div class="poem"></div>`で囲まれ、ウィキテキストの各行毎に自動的に`<br />`が付加されます。

### score

楽譜を描画します。[Help:Scoreです](https://ja.wikipedia.org/wiki/Help:Score "wikilink")。

### math, math chem, ce

数式や化学式を描画します。[:en:Help:Displaying a formula](https://ja.wikipedia.org/wiki/:en:Help:Displaying_a_formula "wikilink")あるいは[m:ヘルプ:数式の書き方を参照してください](https://ja.wikipedia.org/wiki/m:Help:Displaying_a_formula/ja "wikilink")。

### timeline

時系列の図を描画します。[mw:Extension:EasyTimeline](https://ja.wikipedia.org/wiki/mw:Extension:EasyTimeline "wikilink")です。

### includeonly, noinclude, onlyinclude

テンプレート呼び出しをする時に呼び出し部分や非呼び出し部分を指定する要素です。[Help:テンプレート参照](https://ja.wikipedia.org/wiki/Help:テンプレート "wikilink")。

### syntaxhighlight / source

[GeSHi 構文ハイライト機能](http://qbnz.com/highlighter/)を利用してプログラミング言語などをみやすく表示する要素です。長らく `<source>` が使われてきましたが、このタグを使用するプログラミング言語を表示する際に不都合なため、同じ意味を持つ要素 `<syntaxhighlight>` が追加されました\[7\]。 `lang=` 言語を指定して使います。

例：

``` xml
<syntaxhighlight lang="Java">
public class HelloWorld
  {
  public static void main (String [] args)
    {
    // Java言語の HelloWorld プログラム
    System.out .println ("Hello, World.") ;
    }
  }
</syntaxhighlight>
```

結果：

``` Java
public class HelloWorld
  {
  public static void main (String [] args)
    {
    // Java言語の HelloWorld プログラム
    System.out .println ("Hello, World.") ;
    }
  }
```

`lang=` で指定できるプログラミング言語等は、以下で示す約140言語です（2009年6月現在）。サポートされていない言語を指定した場合、または言語指定がない <code>

    </code>（および <code><source></code>）を使用した場合、使用したページが[[:Category:構文ハイライトエラーがあるページ|:Category:構文ハイライトエラーがあるページ]]へ登録されます。最新情報は編集画面に <code><nowiki><syntaxhighlight>

</nowiki></code> と打ち込めば表示されます。

ほかに次のパラメータが指定できます。

  - `line` と書くとソースの行番号が出力されます。
  - `start=`<var>`整数`</var> は開始行番号を指定します。
  - `highlight=`<var>`整数`</var> は強調する行を指定します。
  - `enclose=`<var>`値`</var> は囲みのスタイルを指定します。値には "none", "div", "pre" のいずれかが指定できます。"pre" がデフォルトです。ただし、拡張機能の更新に伴い、枠線が表示されなくなりました（[bugzilla:10967](https://ja.wikipedia.org/wiki/bugzilla:10967 "wikilink")・[bugzilla:19416](https://ja.wikipedia.org/wiki/bugzilla:19416 "wikilink")参照）。 "none" は地の文に埋め込み、"div" はテキストを折り返します。
  - `strict` と書くと厳密モード (strict mode) で出力されます。

下の例は

``` xml
<syntaxhighlight lang="html5" line start="3" highlight="2-4, 6">
```

と指定したものです。

``` html5 numberLines
<div style="font-size:80%">
これは<span style="color:red">赤い</span>テキスト<br />です。
これは<span style="color:red">赤い</span>テキスト<br />です。
これは<span style="color:red">赤い</span>テキスト<br />です。
</div>
<hr />
```

下の例は

``` xml
<syntaxhighlight lang="html5" enclose="div">
```

と指定したものです。

``` html5
<div style="font-size:80%">
これは<span style="color:red">赤い</span>テキスト<br />です。
これは<span style="color:red">赤い</span>テキスト<br />です。
これは<span style="color:red">赤い</span>テキスト<br />です。
</div>
<hr />
```

下の例は

``` xml
<syntaxhighlight lang="html5" enclose="none">
```

と指定したものです。

``` html5
<div style="font-size:80%">
これは<span style="color:red">赤い</span>テキスト<br />です。
これは<span style="color:red">赤い</span>テキスト<br />です。
これは<span style="color:red">赤い</span>テキスト<br />です。
</div>
<hr />
```

なお、[MediaWiki:Geshi.css](https://ja.wikipedia.org/wiki/MediaWiki:Geshi.css "wikilink") にて専用のクラスを指定できます。また、ユーザーCSS では div と span (enclose=none にしている場合用） に[セレクター](../Page/Cascading_Style_Sheets.md "wikilink")（.mw-geshi）が使用できます。

より詳しくは[mw:Extension:SyntaxHighlight GeSHiを参照してください](https://ja.wikipedia.org/wiki/mw:Extension:SyntaxHighlight_GeSHi "wikilink")。

また、専用のテンプレートであるが用意されています。

### テンプレート引数をタグで囲むためには

テンプレートの引数をXML風タグで囲んでテンプレート呼び出しをするとうまく機能しません。この時には `{{#tag:}}` を使用することで、この問題を回避できます。

## 注釈

<references group="注釈" />

## 関連項目

  - [特別:テンプレートを展開](https://ja.wikipedia.org/wiki/特別:テンプレートを展開 "wikilink")

<!-- end list -->

1.  [Help:セクション\#セクションへのリンクを参照](https://ja.wikipedia.org/wiki/Help:セクション#セクションへのリンク "wikilink")。
2.  ウィキペディアの利用している[MediaWiki](https://ja.wikipedia.org/wiki/Help:MediaWiki "wikilink") の [Sanitizer.php](https://doc.wikimedia.org/mediawiki-core/master/php/Sanitizer_8php_source.html)に記述されています。
3.  u要素はHTML5では発音しない注記を示します。例えばスペルミスの箇所や中国語内での固有名詞の箇所など、本来とは異なった表記であることを明示する場合に使用します。
4.  `<br>` を `<br />` になおす*だけ*の編集や、他の利用者に対してどちらかを使うように注意することは無意味ですのでやめてください。気になる方は、[Wikipedia:サンドボックスで試し](https://ja.wikipedia.org/wiki/Wikipedia:サンドボックス "wikilink")、ブラウザでソースを表示してみてください。
5.  em は emphasized = 強調されたの略。
6.  次の括弧内の`<!-- コメントアウトしました -->`という文字列がどうなっているか、ブラウザのソースを表示する機能を利用して確認してみてください。確認用括弧「 」 。
7.  [rev:50696](https://ja.wikipedia.org/wiki/rev:50696 "wikilink")(MediaWiki)