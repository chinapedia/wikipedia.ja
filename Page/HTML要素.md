> この記事は[HTML](https://ja.wikipedia.org/wiki/HTML)から翻訳されています。


**HTML要素**（HTMLようそ、）の記事では、[HTML文書を構成する各種の要素を解説する](../Page/HyperText_Markup_Language.md "wikilink")。なお、一般に「HTML要素」と言った場合、HTML文書において「html」というタグ名のルート要素を指すことが多い。

## 要素の構成

例）

``` html4strict
<strong>強調部分です。</strong>
```

要素 (element) は、開始タグ (Start-tag)・内容 (Content)・終了タグ (End-tag) の3つから構成される\[1\]。要素は**`<`**と**`>`**で囲まれる開始タグで始まり、**`</`**と**`>`**で囲まれる終了タグで終わる。開始タグと終了タグではさまれた部分が内容となる。また開始タグ内に、任意個の、属性 (attribute) と属性値 (value) のペアを含むことができる。

「要素」と「タグ」はこのような関係にあり、明確に区別し、用語も明確に使い分ける必要がある。

また、XMLでは、開始タグや終了タグとは別に、空要素のための空要素タグ (Empty-Element Tags)が規程されている。空要素タグは**`<`**と**`/>`**で囲まれ、内容を持たない。意味は**`<elem></elem>`**のように記述された場合と基本的には全く同じに扱われる（ツール類の実装によっては、内部では識別しているものもある）。

### HTML構文とXML構文との違い

HTMLを表記するための構文は、独自のHTML構文とXMLアプリケーションであるXML構文に大別される。HTML構文は、HTML 2～4.01までの間[SGMLアプリケーションとして定義されていた](../Page/Standard_Generalized_Markup_Language.md "wikilink")。しかし、現実にはウェブブラウザのほとんどでSGMLとして処理されることはなく、そのためSGMLであることをやめて独自に構文を定義するようになった\[2\]\[3\]。もう一方のXML構文は[XHTML](https://ja.wikipedia.org/wiki/XHTML "wikilink")に由来する。

HTML構文とXML構文の相違は以下のようになる。

#### タグの省略

##### HTML

一部の開始タグ・終了タグは省略可能と定義されている\[4\]\[5\]。また、空要素 (void elements)と指定されている要素では開始タグのみを記述し、終了タグを書いてはならない\[6\]\[7\]。

HTML 4.01までは、SGMLの省略タグ機構によって同様のタグの省略が認められていた。

##### XML

XMLはタグの省略は不可能である。そのため、XMLアプリケーションであるXML構文では空要素を表現する場合、次のうちどちらかを用いる必要がある。

  - 空要素タグを使い「`<要素名 />`」や「`<要素名/>`」を使う。
  - 開始タグの直後に終了タグを記述する（「`<要素名></要素名>`」）。

なお、古いユーザエージェントのためには、前者のうち「`/>`」の前にスペースを入れる記述が推奨されている\[8\]。

#### 属性の省略

##### HTML

属性に関して次のような省略が可能である。

  - 属性値に以下の文字を含まない場合、属性値を括る引用符が省略可能\[9\]\[10\]。
      - ASCII空白文字
      - U+0022 二重引用符
      - U+0027 アポストロフィー
      - U+003D 等号
      - U+003C 不等号(より小)
      - U+003E 不等号(より大)
      - U+0060 グレイヴ・アクセント
  - 空属性: 属性名が択一式である場合に属性名が省略可能。

##### XML

XHL構文では、HTML構文で許されていた属性に関する省略は不可能である。これはXMLの特徴に因る。

## HTML要素一覧

### 基本的な構造を表す要素

  - `html`
    HTML文書の[ルート](../Page/ルート.md "wikilink")要素 (document root element)。
  - `head`
    HTML文書のヘッダ部分 (document head) を指定する要素。HTML文書自身に関する情報（例：タイトルやスタイルシートに関する情報など）を指定できる。
  - `body`
    HTML文書の本体部分 (document body) を指定する要素。

HTML文書は、ヘッダ部分と本体部分の2つに分けることができる。2007年11月現在で有効なスキーマでは、ルート要素であるhtml要素の直下にはhead要素、body要素をこの順で1つずつだけ取ることができる。

HTML文書は次のような構造となる。

``` html4strict
<html>
  <head>
    head要素以下に取ることができる要素群。
    title要素などをはじめとしたそのHTML文書自身に関する情報からなる。
  </head>
  <body>
    body要素以下に取ることができる要素群。
    HTML文書の本文となる情報を記述する。
  </body>
</html>
```

### ヘッダ内に記述可能な要素

  - `title`
    タイトル (document title) を指定する。多くの[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")実装系では、[タイトルバー](https://ja.wikipedia.org/wiki/タイトルバー "wikilink")に表示される。例えば、このページのタイトルは "HTML要素 - Wikipedia" である。
    HTML文書で唯一**必須かつ省略のできない**要素。
  - `base`
    相対パスの基準URL (document base URI) をhref属性で指定する。

#### ヘッダ内で複数記述できる要素 (repeatable head elements)

  - `link`
    自分自身とhref属性で指定したファイルとの関係をrel属性で定義する。
    rel属性はHTML4.01で有効なものには *alternate, stylesheet, start, next, prev, contents, index, glossary, copyright, chapter, section, subsection, appendix, help, bookmark*があり、他に使われるものとして、*shortcut icon*がある。
  - `meta`
    文書の情報 (generic metainformation) を定義する。
  - `object`
    埋め込みオブジェクト (generic embedded object) であることを示す。大抵の場合はインライン要素として使用する。data属性に[URI](https://ja.wikipedia.org/wiki/URI "wikilink")、type属性に[MIMEタイプ](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink")(image/gif等)を指定することで[FLASHや音楽など様々な種類のオブジェクトを出力する事ができる](../Page/Adobe_Flash.md "wikilink")。
    内容には代替（オブジェクト要素も可）を記述する。例えば一番外からオブジェクト要素 (FLASH)、オブジェクト要素（画像）、説明文、のように入れ子にするとFLASHの利用できない環境では画像が、FLASHと画像の利用できない環境では説明文が出力される。これはimg要素等の[alt属性](https://ja.wikipedia.org/wiki/alt属性 "wikilink")と比べると**高性能な代替システム**であるが、これに対応しない[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")も少なくない。
  - `param`
    プロパティ値の設定 (named property value) を行う。object要素で使用する[メディア](../Page/メディア.md "wikilink")に対しての初期値を設定するために使用する。
    内容は空で終了タグは存在しない。
  - `style`
    スタイル情報 (style info) を記述する。
    type属性の記述が必要（text/css等）。
  - `script`
    スクリプト (script statements) を記述する。
    type属性（text/javascriptなど）とmeta要素でスクリプトタイプの宣言が必要。

### 文書の更新情報を示す要素

  - `ins`
    追加された文書 (inserted text) であることを示す。
    datetime属性に追加日時を記載できる。
  - `del`
    削除された文書 (deleted text) であることを示す。
    datetime属性に削除日時を記載できる。

### ブロックレベル要素

  - `p`
    段落 (paragraph) を構成する。
  - `blockquote`
    引用文 (long quotation) であることを示す。
    ウェブブラウザによっては[インデント](https://ja.wikipedia.org/wiki/インデント "wikilink")して表示することがあるが、この要素はあくまで引用目的に用いるべきであり、単にインデントするために用いるのは好ましくない。また、内容にクォーテーションマーク（「"」 や 「'」）を用いるのは避けるほうが良い。
    cite属性で引用元・出典を明示することができる。
  - `pre`
    整形済みテキスト (preformatted text) の節であることを示す。
    内容にはインライン要素を含める事もできるがimg、object、big、small、sub、sup要素は使用できない。
    ウェブブラウザのサイズによる折り返しがされなくなるため、[リキッドレイアウト](https://ja.wikipedia.org/wiki/リキッドレイアウト "wikilink")を行うには不向き。
  - `div`
    ブロックレベルでのスタイルコンテナ。
    この要素自体に意味は無い。文書の構造を示すときや、既存の要素には含められない物の代用要素として使用する。
  - `noscript`
    [スクリプト](../Page/スクリプト.md "wikilink")が動作しない環境での代替コンテンツ (alternate content container for non script-based rendering) であることを示す。スクリプトが動作する環境では無視される。
    代替となりうる[コンテンツ](../Page/コンテンツ.md "wikilink")を示す要素である。
  - `hr`
    水平線 (horizontal rule) を示す。内容は空で終了タグは存在しない。
  - `address`
    著者の情報・連絡方法 (information on author) を示す。
    メールアドレスを記述するのが一般的。ただし、address要素内のメールアドレスが[メールアドレス検索ロボット](https://ja.wikipedia.org/wiki/メールアドレス検索ロボット "wikilink")の標的になり[スパムメールなどの被害に遭う可能性もある](../Page/スパム_\(メール\).md "wikilink")。
  - `form`
    コントロール要素を纏めた入れ物であることを示す(interactive form)。
    action属性が必須で、入力されたデータの処理を行うURIを指定する。
  - `fieldset`
    フォームコントロールのグループ (form control group) を示す。
    関連したフォームコントロールを記述することで利便性を高めることが出来る。
  - `legend`
    fieldset要素の表題 (fieldset legend) を示す。

以下にfieldset要素とlegend要素の記述例を示す。

``` html4strict
<form action="http://...">
  <fieldset>
    <legend>名前</legend>
    <label>姓:<input type="text"></label>
    <label>名:<input type="text"></label>
  </fieldset>
  <fieldset>
    <legend>住所</legend>
    <label>県:<input type="text"></label>
    <label>市:<input type="text"></label>
  </fieldset>
</form>
```

#### 見出し (heading)

  - `h1`〜`h6`
    文章の見出し (heading) を示す。h1が最上位の見出しで、h6が最下位の見出し。

#### リスト (list)

  - `ul`
    順序なしリスト (unordered list) を示す。一つ以上のli要素を含む必要がある。
  - `ol`
    順序付きリスト (ordered list) を示す。一つ以上のli要素を含む必要がある。
  - `li`
    リストの項目 (list items) を示す。ブロック要素を含められるため、入れ子のリストを作成することもできる。
  - `dl`
    定義のリスト (definition list) であることを示す。dt要素かdd要素を1つ以上含む必要がある。
  - `dt`
    定義する用語 (definition term) であることを示す。
  - `dd`
    定義の説明 (definition description) であることを示す。

#### 表を構成する要素

表形式のデータを表す要素群。その特性から[レイアウトに使用されることがあるが](https://ja.wikipedia.org/wiki/ウェブデザイン "wikilink")**間違いである**。

また正しく[マークアップ](https://ja.wikipedia.org/wiki/マークアップ "wikilink")する為には（他の要素に比べ）多少の知識を要する。これは[音声ブラウザ](https://ja.wikipedia.org/wiki/音声ブラウザ "wikilink")の挙動など、[アクセシビリティ](https://ja.wikipedia.org/wiki/アクセシビリティ "wikilink")を考慮した場合に制約が多いため。

  - `table`
    表 (table) を構成する要素の大枠を示す。summary属性に表の要約・解説を記述する。
    内容の要素には細かく順番が規定されていて以下の通りである。
    0個か1個のcaption要素、0個以上のcolgroup要素とcol要素、0個以上のthead要素、0個以上のtfoot要素、1個以上のtbody要素。
  - `caption`
    表題 (table caption) を示す。table要素の直下に記述する。
  - `thead`、`tfoot`、`tbody`
    それぞれ[ヘッダ](https://ja.wikipedia.org/wiki/ヘッダ "wikilink") (table header)、[フッタ](https://ja.wikipedia.org/wiki/フッタ "wikilink") (table footer)、本体 (table body) で、表内での節 (table section) を示す。
    内容はtr要素のみで、1つ以上の記述が必要である。また、各要素内においての列の数は等しくなくてはならない。
  - `colgroup`
    構造的な列のグループ (table column group) を示す。
    グループ化させるには2つの方法があり、span属性で列数を指定する方法かcol属性を列数分記述する方法である。
  - `col`
    列のグループ (table column) を示す。
    colgroup要素と違い、**構造的なグループを示さず**、スタイルの指定を主としたグループ化を行う。
    span属性でグループ化する列数を指定する。内容は空で終了タグは存在しない。
  - `tr`
    表内の行 (table row)を示す。
    内容に1つ以上のth要素かtd要素が必要。
  - `th`、`td`
    それぞれ、ヘッダのセル (table header cell)、データのセル (table data cell) を示す。
    視覚系でない[ユーザーエージェント](../Page/ユーザーエージェント.md "wikilink")に対応する為にいくつかの整形方法がある。

<!-- end list -->

  - ヘッダ要素のid属性と、データ要素のheaders属性を結びつける (同じ値を指定する)。これによって音声ブラウザではヘッダとデータの内容を交互に読み上げることが出来る。
  - 上記の省略系といえるscope属性を用いる。ヘッダ属性にcolを指定することで縦方向・rowを指定することで横方向のデータと結びつけることが出来る。
  - ヘッダ要素にabbr属性で短縮系を指定する。例えば、ヘッダ要素の内容が"価格（円）"等の場合、逐一読み上げるのは冗長になる。abbr属性が"価格"となっていれば、「価格100」等と読み上げられ、冗長さは解消される。

以下にtable要素の記述例を示す。

``` html4strict
<table summary="取り扱い商品の一覧表。商品ごとに価格・備考を表記する。" border="1">
  <capthion>商品一覧</capthion>
  <colgroup class="head" span="1"></colgroup>
  <colgroup class="data" span="2"></colgroup>
  <thead>
    <tr>
      <th id="t1">商品名</th>
      <th id="t2" abbr="価格">価格（円）</th>
      <th id="t3" abbr="備考">備考（産地・在庫など）</th>
    </tr>
  </thead>
  <tbody>
    <tr><td headers="t1">りんご</td><td headers="t2">100</td><td headers="t3">青森産</td></tr>
    <tr><td headers="t1">みかん</td><td headers="t2">150</td><td headers="t3">在庫無し</td></tr>
  </tbody>
</table>
```

### インライン要素

#### 物理要素 (fontstyle)

見た目を定義する要素。[スタイルシート](../Page/スタイルシート.md "wikilink")で代替が可能。

  - `i`
    文字を斜体 (italic) にする。（例：*html*）
  - `b`
    文字を太字 (bold) にする。（例：**html**）
  - `u`
    文字に下線 (underline) を引く。（例：<span style="text-decoration:underline;">html</span>）[CSSで代用可能で非推奨](../Page/Cascading_Style_Sheets.md "wikilink")
  - `s`
    `strike`
    文字に中央線 (strike-through) を引く。（例：<s>html</s>, ）CSSで代用可能で非推奨
  - `big`
    文字を大きく(large)する。（例：<span style="font-size:120%;">html</span>）
  - `small`
    文字を小さく(small)する。（例：<span style="font-size:90%;">html</span>）

#### 論理要素 (phrase)

論理的な意味を表現する要素。

  - `em`
    強調 (Indicates emphasis) する。（例：*html*）
  - `strong`
    強く強調 (Indicates stronger emphasis) する。（例：**html**）
  - `dfn`
    定義された用語 (defining) を示す。
  - `code`
    [プログラムなどのソースコード](../Page/プログラム_\(コンピュータ\).md "wikilink") (computer code) を示す。
  - `samp`
    プログラムなどによる出力のサンプル (sample output from programs, scripts, etc.) を示す。
  - `kbd`
    ユーザが入力する文字 (text to be entered by the user) を示す。
    [アプリケーションの](../Page/アプリケーションソフトウェア.md "wikilink")[チュートリアル](https://ja.wikipedia.org/wiki/チュートリアル "wikilink")などでユーザが自由に入力できる箇所であることを示す際などに用いる。
  - `var`
    プログラムなどに用いる変数 (variable or program argument) を示す。
  - `cite`
    出典 (citation or a reference) を示す
  - `abbr`
    略語 (abbreviated form) を示す。
    title属性に略さない状態の語を明示することができる。
  - `acronym`
    頭字語 (acronym) を示す。
    abbr要素と同様に、title属性に略さない状態の語を明示することができる。

#### 特別な要素 (special)

  - `a`
    アンカー (anchor) であることを示す。href属性にリンク先[URI](https://ja.wikipedia.org/wiki/URI "wikilink")を指定し[ハイパーリンク](../Page/ハイパーリンク.md "wikilink")を作成する。

    内容には[リンク](../Page/リンク.md "wikilink")先の概要を表記する。**内容だけを見てリンク先が判断できること**が望ましく、「[ここをクリック](https://ja.wikipedia.org/wiki/ここをクリック "wikilink")」等は使うべきでないとされる。内容が冗長になる場合はtitle属性で説明を付加することができる。

    accesskey属性で[ショートカットキー](https://ja.wikipedia.org/wiki/ショートカットキー "wikilink")を設定することができ、[ユーザビリティ](https://ja.wikipedia.org/wiki/ユーザビリティ "wikilink")の向上が期待できる。

  - `audio`

    音声再生。但し、ファイルによっては対応コーデックを導入しないと再生が実現できない場合がある。詳細は上記の内部リンクを参照。

  - `canvas`

    解像度に依存したビットマップキャンバスを表示。グラフやゲーム用の表示画像を描画することができる。[HTML5](https://ja.wikipedia.org/wiki/HTML5 "wikilink")で導入予定であり、主要ブラウザではすでに実装済み。Internet Explorer 向けに、[Adobe Flashや](../Page/Adobe_Flash.md "wikilink")[VML](https://ja.wikipedia.org/wiki/VML "wikilink")などを使い、canvas タグを実現するライブラリがある。

  - `img`
    埋め込み画像 (Embedded image) であることを示す。src属性にURIを指定し画像を表示させる。内容は空で終了タグは存在しない。

    **[alt属性](https://ja.wikipedia.org/wiki/alt属性 "wikilink")で画像の説明を記述**することが**必要**である。これは画像に対応できないユーザーのため。単にレイアウト用の画像（[スペーサー画像](https://ja.wikipedia.org/wiki/スペーサー画像 "wikilink")等）の場合にはaltは空にする。また「画像が表示できません」や「画像」と言った代替テキストはユーザにとっては有用でなく、「犬の写真」など簡素な説明や「飼い犬のポチが…」など情景が把握できる説明が有用である。説明が長文になる場合longdesc属性にURIを指定し、説明の文書を示す事もできる。

    他のドメインの画像を指定することも可能であるため、[著作権](../Page/著作権.md "wikilink")の観点から問題視されることもある（詳細は[無断リンク](../Page/無断リンク.md "wikilink")の項目を参照）。

  - `video`

    動画再生。前者のaudio要素と同様、ファイルによっては対応コーデックを導入しないと再生が実現できない場合がある。

## コメント

  -
    [コメントは](../Page/コメント_\(コンピュータ\).md "wikilink")、文書ソースの任意の場所に追加することができる。たとえば doctype の前にもコメントを記入できる。しかし、他のタグ内に入れることはできない。ただし、doctype の前に空白文字以外の文字があると、Internet Explorer 6 は [ブラウザの互換モードでその文書をひらく仕様になっている](https://ja.wikipedia.org/wiki/互換モード#Webブラウザの互換モード "wikilink")。

コメント内の文字は、ブラウザによって処理（表示）されないで無視される。 コメントは[入れ子構造](https://ja.wikipedia.org/wiki/入れ子構造 "wikilink")できない。

## AttributeとProperty

HTML要素の振る舞いを取得・変更するには***Attribute***を介した手法と***Property***を介した手法が存在する。AttributeとPropertyは互いの変更が反映されるように定義されている場合が多いが、必ずしもそうとは限らない（各HTML要素の定義による）。

### 定義

HTMLの要素（*Elements*）は**をもつ\[11\]\[12\]。また*Elements*はWeb IDLで記述される*DOM interface*をもち、その中にWeb IDLの**をもつ\[13\]\[14\]。2つのattributesを呼び分けるために、前者のHTML *attributes*は*****、後者の*WebIDL *attributeは****と呼ばれる*\[15\]。JavaScriptはWeb IDLで書かれた*DOM interface*を実装することでWebページの操作を可能にしており、その際*IDL attributes*はJavaScript object **properties**として実装されるため、しばしば俗称としてContent attributesは****、IDL attributesは****と呼ばれる\[16\]。

| spec         | formal name        | formal alt. name | informal name      |
| ------------ | ------------------ | ---------------- | ------------------ |
| {{font color | \#CEF2F2|HTML}}    | attributes       | Content attributes |
| {{font color | \#F2CEF2|Web IDL}} | attributes       | IDL attributes     |

Table. HTML attributesとWeb IDL attributes

歴史的理由・言語的制約などにより、対応するattributeとpropertyは必ずしも名前が一致しない。例えば*class* attributeは*className* propertyと対応する。大半のattribute-propertyは名前が一致しているが、一致しているか否かに法則はなく、逐一仕様書を確認する必要がある。

### リフレクション

このようにHTML要素にはattribute（Content attribute）とproperty（IDL attribute）の2つの側面がある。あるattributeを変更したとき、対応するpropertyにも変更が反映されないとアクセスする方法によって得られる結果に矛盾が生じてしまう。それを防ぐために、いくつかのpropertyは対応するattributeを反映（***reflect***）する、と定義されている\[17\]。reflectされるか否かは要素ごとにきまり、統一されたルールはない\[18\]。

## 参考

  - [W3C HTML 4.01 Specification](http://www.w3.org/TR/1999/REC-html401-19991224/)
  - [HTML Living Standard](https://html.spec.whatwg.org/multipage/)
      - [HTML Living Standard 日本語訳](https://momdo.github.io/html/)

## 脚注

<references/>

[Category:HTML](https://ja.wikipedia.org/wiki/Category:HTML "wikilink")

1.  開始タグ・終了タグをあわせて**HTMLタグ**（もしくは**タグ**）と呼ぶこともあるが仕様で定められた表現ではない。
2.
3.
4.
5.
6.
7.
8.  [XHTML 1.0 The Extensible HyperText Markup Language HTML C. Compatibility Guidelines](https://www.w3.org/TR/xhtml1/#C_2)
9.
10.
11. 3.2.4.1 Attributes [1](https://html.spec.whatwg.org/multipage/dom.html#attributes)
12. Content attributes /n A normative list of attributes that may be specified on the element [2](https://html.spec.whatwg.org/multipage/dom.html#concept-element-attributes)
13. 2.1.9 Dependencies / **Web IDL** / The IDL fragments in this specification must be interpreted as required for conforming IDL fragments, as described in *Web IDL*. [3](https://html.spec.whatwg.org/#dependencies)
14. A normative definition of a DOM interface that such elements must implement. [4](https://html.spec.whatwg.org/#concept-element-dom)
15. they are referred to as <dfn>content attributes</dfn> for HTML and XML attributes, and <dfn>IDL attributes</dfn> for those defined on IDL interfaces. [HTML Living Standards](https://html.spec.whatwg.org/#dependencies)
16. The IDL attribute is also known as a JavaScript property. [MDN web docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes#Content_versus_IDL_attributes)
17. Some IDL attributes are defined to <dfn>reflect</dfn> a particular content attribute. [5](https://html.spec.whatwg.org/multipage/common-dom-interfaces.html#reflect)
18. Unfortunately, there are no clear rules and the way IDL attributes behave in conjunction with their corresponding content attributes depends on the attribute. [6](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes#Content_versus_IDL_attributes)