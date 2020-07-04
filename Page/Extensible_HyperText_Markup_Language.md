> この記事は[Extensible HyperText Markup Language](https://ja.wikipedia.org/wiki/Extensible_HyperText_Markup_Language)から翻訳されています。


**Extensible HyperText Markup Language**（エクステンシブル ハイパーテキスト マークアップ ランゲージ）、略記・略称：**XHTML** （エックスエイチティーエムエル）は、[SGMLで定義されていた](../Page/Standard_Generalized_Markup_Language.md "wikilink")[HTMLを](../Page/HyperText_Markup_Language.md "wikilink")[XMLの文法で定義しなおした](../Page/Extensible_Markup_Language.md "wikilink")[マークアップ言語](../Page/マークアップ言語.md "wikilink")である。その仕様はHTMLと同じく[W3Cによって勧告されていた](../Page/World_Wide_Web_Consortium.md "wikilink")。しかし[2007年](../Page/2007年.md "wikilink")にW3C HTML WGを設立すると[WHATWGとの共同作業を行い](../Page/Web_Hypertext_Application_Technology_Working_Group.md "wikilink")、[2009年](../Page/2009年.md "wikilink")、W3Cは開発を正式に中止した。HTML5はXMLの書式に従わずとも[MathMLや](../Page/Mathematical_Markup_Language.md "wikilink")[SVGなどを埋め込むことが可能である](../Page/Scalable_Vector_Graphics.md "wikilink")。

上述の通りXHTMLは開発が中止されており、この記事には古い内容を多分に含んでいる。しかしながら、HTMLを解釈するユーザーエージェント（[Webブラウザなど](../Page/ウェブブラウザ.md "wikilink")）は、引き続きサポートしている。

なお、「e**X**tensible **H**yper**T**ext **M**arkup **L**anguage の略である」とされることがあるが、これは間違いであり、**X**は**Ex**の発音を表している\[1\]。

## HTMLとの相違点

XHTMLはXMLアプリケーションである。よって、XMLの文法に従うために、HTMLと異なる部分が存在する。以下は、主な文法上の相違点とソースのサンプルである。

  - XML宣言を書く
    XML文書であるため、文書の頭にXML宣言を書くことが奨励されている。[文字コード](../Page/文字コード.md "wikilink")については、[UTF-8](../Page/UTF-8.md "wikilink")ないし[UTF-16](../Page/UTF-16.md "wikilink")の場合や[HTTPなどのプロトコルで文字コードが指定されている場合は省略可能であるが](../Page/Hypertext_Transfer_Protocol.md "wikilink")、常に付与することが推奨される。

<!-- end list -->

    <?xml version="1.0" encoding="UTF-8"?>

  - 要素名・属性名は小文字で書く
    XMLでは大文字・小文字が厳密に区別される。XHTML勧告の場合、要素名・属性名は全て小文字でのみ定義されていることから、要素名・属性名は共にすべて小文字で表記しなければならない（なお、属性値はこの限りではない）。

<!-- end list -->

    正: <p id="iroha">色は匂へど 散りぬるを</p>
    正: <p id="IROHA">色は匂へど 散りぬるを</p>
    誤: <p ID="iroha">色は匂へど 散りぬるを</p>
    誤: <P id="iroha">色は匂へど 散りぬるを</P>
    誤: <P ID="iroha">色は匂へど 散りぬるを</P>

  - 要素の終了タグを書く
    要素は必ず開始タグと終了タグを備えていなければならない（終了タグの省略は許されない）。

<!-- end list -->

    正: <p>色は匂へど 散りぬるを</p><p>我が世誰ぞ 常ならん</p>
    誤: <p>色は匂へど 散りぬるを<p>我が世誰ぞ 常ならん

  - 空要素の終了タグも書く
    空要素についても同様に終了タグを付与するか、開始タグの末尾を「/\>」としなければならない。
      - 終了タグを付与する \<br\>\</br\> という表記の場合は、タグの間に空白類文字すら含めてはいけない。また、後方互換性のために \<br\>\</br\> ではなく、\<br /\> と表記することが推奨されている\[2\]。
      - XMLを解釈できない古い[UAで](../Page/ユーザーエージェント.md "wikilink") \<br/\> という表記に対し、"br/" を要素名とみなし無視してしまう可能性があることを考慮し、XHTMLでは \<br /\> のようにスラッシュの前に半角スペースを先行させる表記が一般的である。

<!-- end list -->

    正: <em>色は匂へど 散りぬるを</em><br />（推奨）
    正: <em>色は匂へど 散りぬるを</em><br/>
    正: <em>色は匂へど 散りぬるを</em><br></br>
    誤: <em>色は匂へど 散りぬるを</em><br>
    誤: <em>色は匂へど 散りぬるを</em><br> </br>

  - 属性値はダブルクォーテーションで囲む
    属性値はすべて " " （ダブルクォーテーション）ないし ' '（シングルクォーテーション）で囲まなければならない。

<!-- end list -->

    正: <input type="text" size="8" />
    正: <input type='text' size='8' />
    正: <input type="text" size='8' />
    誤: <input type=text size=8 />

  - 属性名を省略せず書く
    属性名を省略してはならない。なお、これらを属性値の省略という例が存在するが正しいとはいえない。

<!-- end list -->

    正: <input type="checkbox" checked="checked" />
    誤: <input type="checkbox" checked />

  - 推奨されるメディアタイプ
    推奨されるメディアタイプが「text/html」から「application/xhtml+xml」に変更された<ref>W3C Note: XHTML

Media Types \<<http://www.w3.org/TR/xhtml-media-types>\></ref>。また、HTMLで従来使用されていたtext/htmlは、XHTML1.1以降では非推奨となっている。

    <meta http-equiv="Content-Type" content="application/xhtml+xml; charset=Shift_JIS" />

メディアタイプがapplication/xhtml+xmlの場合、meta要素のhttp-equiv属性の使用は非推奨となる\[3\]。代わりに[HTTPのヘッダでメディアタイプを指示することが必要となる](../Page/Hypertext_Transfer_Protocol.md "wikilink")。

[HTML要素\#HTML構文とXML構文との違い](https://ja.wikipedia.org/wiki/HTML要素#HTML構文とXML構文との違い "wikilink")も参照されたし。

## 歴史

### XHTML 1.0

HTML 4.01をXMLにて再定義したもので、HTML 4.01と同様にStrict、Transitional、Framesetという3種類の[DTDが存在する](../Page/Document_Type_Definition.md "wikilink")。

[2000年](../Page/2000年.md "wikilink")[1月26日](../Page/1月26日.md "wikilink")に勧告となり、[2002年](../Page/2002年.md "wikilink")[8月1日](../Page/8月1日.md "wikilink")に改訂版であるSecond Editionが勧告された。

### XHTML Basic

XHTMLのサブセットで、PDAや携帯電話などの小規模な端末を含む、より広域の環境のための仕様である。[2000年](../Page/2000年.md "wikilink")[12月19日](https://ja.wikipedia.org/wiki/12月19日 "wikilink")にXHTML Basic 1.0が勧告された。

その後、[OMA](https://ja.wikipedia.org/wiki/OMA "wikilink")が策定する[XHTML Mobile Profileとの不整合を解消する目的で策定された](../Page/XHTML_Mobile_Profile.md "wikilink") XHTML Basic 1.1が[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[7月29日](../Page/7月29日.md "wikilink")に勧告された。

Basic1.1では、Basic1.0から次のような変更が行われている。

  - target属性やscript/style要素、style属性の追加
  - [XForms](../Page/XForms.md "wikilink")よりinputmode属性の追加

### XHTML Modularization (Modularization of XHTML, M12n)

XHTMLをその要素の目的や役割ごとに分割し、フレームワーク化したもの。XHTML 1.1やXHTML 2.0は、M12nをベースに構築されている。バージョン1.0が[2001年](../Page/2001年.md "wikilink")[4月10日](../Page/4月10日.md "wikilink")に、バージョン1.1が2008年10月にそれぞれ勧告された。2009年7月現在、バージョン2.0が草案の段階にある。 1.0から1.1ではXML Schemaへの対応などが変更点となった。

### XHTML 1.1

機能がモジュール化されたXHTML。XHTML 1.0からの主な違いは、次の通りである。

  - 機能がモジュール化され、カスタマイズ性が向上した。
  - HTML 4.0以来複数あったスキーマが、従来のStrictスキーマの思想を基としたスキーマ1つのみとなった。
  - [ルビ](../Page/ルビ.md "wikilink")モジュールが導入された。

[2001年](../Page/2001年.md "wikilink")[5月31日](../Page/5月31日.md "wikilink")に仕様が勧告となった。 2010年11月23日にXHTML 1.1 Second Editionが勧告された。エラッタの修正とXML Schemaへの対応が主な変更点となる。

### XHTML 1.2

策定中であるXHTML Role ModuleやAccess Module、WAI-ARIAの語彙を組み込んだ新しいプロファイルとして策定予定。

### XHTML 2.0

XHTML Familyの次期バージョンとして策定されていたが、W3Cは2009年07月03日に策定の打ち切りを決定し、今後は[HTML5](../Page/HTML5.md "wikilink")にリソースを注ぐものとした。理由として、XHTML 2.0の市場はHTML5に比べて非常に小さいことがあげられている。

### XHTML5(最終草案)

HTML5をXML記法で記述したものをXHTML5と呼ぶ。

HTML5をXML記法で記述するための仕様も、HTML5仕様の中で定義されている。そのため、XHTML5はHTML5のサブセットである。 しかし、HTML5の仕様ではXML記法とHTML記法の間には違いが多く、単に「HTML5」「HTML5ドキュメント」と言う場合には、HTML記法によるもののみを指すことが多い。そのため、実用上はXHTML5はHTML5と別のものとして扱われることがある。

以下にHTML記法とXML記法の違いをいくつか挙げる。

  - HTML記法の場合は要素名は固定だが、XML記法の場合は要素の名前空間が "<http://www.w3.org/1999/xhtml>" に属していれば接頭辞付きが許される（XHTML1.x以前には、[文書型宣言](https://ja.wikipedia.org/wiki/文書型宣言 "wikilink")にモジュールを追加することで接頭辞を付けることを可能としていたが、基本的には許されなかった）
  - HTML記法では限定的なSVG, MathMLの拡張しか行えないが、XML記法では名前空間を用いて制限なく拡張ができる（以下の例ではxml:id属性を利用している）
  - 従来のHTML/XHTMLで許されていたDTDを用いた[文字参照](../Page/文字参照.md "wikilink")が不可能となった。

上記のような違いによってHTML文法と見た目が大きく異なるXHTML文書として、以下のような例が考えられる。

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<!-- これは妥当なXHTML5文書。ただしHTML記法との互換性はない -->

<?xml-stylesheet type="text/css" href="test.css"?><!-- 左のようなXML処理命令も書ける -->

<!-- この場合、ルート要素がxhtml:htmlのため、通常のHTML5のように "<!DOCTYPE html>" という文書型宣言は行えない -->

<xhtml:html xmlns:xhtml="http://www.w3.org/1999/xhtml">
  <xhtml:head>
    <xhtml:title xml:id="title">XML名前空間を用いた拡張例（xml:id）</xhtml:title>
    <xhtml:script><![CDATA[ ... ]]></xhtml:script>
  </xhtml:head>
  <xhtml:body>
    <xhtml:p> ... </xhtml:p>
  </xhtml:body>
</xhtml:html>
```

なお、HTML5、XHTML5の正式名称には、アルファベットと数字の間にスペースを含まない。

## 関連項目

  - [HTML](../Page/HyperText_Markup_Language.md "wikilink")
  - [SGML](../Page/Standard_Generalized_Markup_Language.md "wikilink")
  - [XML](../Page/Extensible_Markup_Language.md "wikilink")
  - [CSS](../Page/Cascading_Style_Sheets.md "wikilink")
  - [EBML](https://ja.wikipedia.org/wiki/Extensible_Binary_Meta_Language "wikilink")
  - [XHTML MP](https://ja.wikipedia.org/wiki/XHTML_MP "wikilink")

## 脚注

## 外部リンク

  - [XHTML 1.0 The Extensible HyperText Markup Language](http://www.w3.org/TR/xhtml1)
  - [XHTML Basic 1.1](http://www.w3.org/TR/2008/REC-xhtml-basic-20080729/)
  - [XHTML Basic](http://www.w3.org/TR/xhtml-basic/)
  - [XHTML 1.1 - Module-based XHTML](http://www.w3.org/TR/xhtml11/)
  - [XHTML 2.0 (Working Draft)](http://www.w3.org/TR/xhtml2/)
  - [W3C](http://www.w3.org/)

[Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:HTML](https://ja.wikipedia.org/wiki/Category:HTML "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink")

1.  ["XML stands for Extensible Markup Language. The X is for the first syllable of Extensible. eXtensible is a spelling error."](http://lists.xml.org/archives/xml-dev/200802/msg00313.html)
2.  [C. HTML Compatibility Guidelines](http://www.w3.org/TR/xhtml1/#C_2)
3.  [XHTML Media Types](http://www.w3.org/TR/2002/NOTE-xhtml-media-types-20020801/#application-xhtml-xml) - [W3C](https://ja.wikipedia.org/wiki/W3C "wikilink") Note、2002年8月1日（2013年12月5日閲覧）。