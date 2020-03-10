> この記事は[Ruby Document format](https://ja.wikipedia.org/wiki/Ruby_Document_format)から翻訳されています。


**RD**（**Ruby Document format**）は[ドキュメント](../Page/文書.md "wikilink")[フォーマットの](../Page/ファイルフォーマット.md "wikilink")1つで、[Ruby](../Page/Ruby.md "wikilink")スクリプトに埋め込み可能であるため、Ruby関連のドキュメントによく使用される。[Wiki文法に似た](../Page/ウィキ.md "wikilink")[マークアップを持ち](../Page/マークアップ言語.md "wikilink")、[HTMLなどよりも簡潔に記述できる](../Page/HyperText_Markup_Language.md "wikilink")。

## マークアップ

Rubyスクリプトに埋め込む場合は`=begin`と`=end`で囲んだ部分に記述する。

### 見出し

RDで見出しは次のように記述する。

`  `
` =最大見出し`
` ==大見出し`
` 段落1`
` ===中見出し`
` 段落2`
` ====中小見出し`
` 段落3`
` +小見出し`
` 段落4`
` ++最小見出し`
` 段落5`

出力されるHTMLはほぼ以下のようなものである。

``` html
 <h1>最大見出し</h1>
 <h2>大見出し</h2>
 <p>段落1</p>
 <h3>中見出し</h3>
 <p>段落2</p>
 <h4>中小見出し</h4>
 <p>段落3</p>
 <h5>小見出し</h5>
 <p>段落4</p>
 <h6>最小見出し</h6>
 <p>段落5</p>
```

### 箇条書き

`  `
` * 順序の無い箇条書き。`
` `
` * 続き。改行があってもよい。`
`   * 入れ子にすることができる。`
` `
` (1) 順序つきの箇条書き`
` (2) 続き`
`     * 違う種類の箇条書き`
` `
` :HTML`
`   HyperText Markup Language の略。`
` :RD`
`   Ruby Document format の略。`

上のRDはほぼ以下のように変換される。

``` html
 <ul>
   <li>順序の無い箇条書き。</li>
   <li>2つめの項目。改行があってもよい。
     <ul>
       <li>入れ子にすることができる。</li>
     </ul>
   </li>
 </ul>
 <ol>
   <li>順序つきの箇条書き</li>
   <li>続き
     <ul>
       <li>違う種類の箇条書き</li>
     </ul>
   </li>
 </ol>
 <dl>
   <dt>HTML</dt>
   <dd>HyperText Markup Language の略。</dd>
   <dt>RD</dt>
   <dd>Ruby Document format の略。</dd>
 </dl>
```

項目が入れ子になるかどうかは、[字下げ](../Page/字下げ.md "wikilink")の深さ（[スペース](../Page/スペース.md "wikilink")の数）が等しいかどうかで判定される。

## 関連項目

  - [RDoc](https://ja.wikipedia.org/wiki/RDoc "wikilink")
  - [コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")
      - [データ記述言語](https://ja.wikipedia.org/wiki/データ記述言語 "wikilink")
          - [マークアップ言語](../Page/マークアップ言語.md "wikilink")
              - [軽量マークアップ言語](../Page/軽量マークアップ言語.md "wikilink")

## 外部リンク

  - [RDtool - RD formatter](https://uwabami.github.io/software/rdtool/index.html)

[Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:Ruby](https://ja.wikipedia.org/wiki/Category:Ruby "wikilink")