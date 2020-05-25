> この記事は[Unicode正規化](https://ja.wikipedia.org/wiki/Unicode正規化)から翻訳されています。


**[Unicode](../Page/Unicode.md "wikilink")正規化**（ユニコードせいきか、）とは、[等価な文字や文字の並びを統一的な内部表現に変換することでテキストの比較を容易にする](../Page/Unicodeの等価性.md "wikilink")、[テキスト正規化](https://ja.wikipedia.org/wiki/テキスト正規化 "wikilink")処理の一種である。一般に、正規化はテキストの文字列を検索や整列のために比較（照合、）するときに重要である\[1\]。

## 合成と分解

Unicodeの正規化手段の基礎は、文字の合成と分解という概念である。文字の合成とは、基底文字と[結合文字](https://ja.wikipedia.org/wiki/結合文字 "wikilink")の組み合わせによる結合文字列を、単一の符号位置である[合成済み文字](https://ja.wikipedia.org/wiki/合成済み文字 "wikilink")にする手続きである。たとえば、基底文字 n と結合文字 \~ の組み合わせを単独の ñ 文字に変換する、仮名文字と濁点の結合文字の組み合わせを単独の濁点つき仮名とするなど。分解はその逆で、合成済み文字を結合文字列にする。分解は単一の符号位置を別の単一の符号位置に変換することもある。

Unicodeは[等価性と呼ばれるものに基づいて文字を合成](../Page/Unicodeの等価性.md "wikilink")・分解する。Unicodeには2種類の等価性がある。1つは正準（）と呼ばれ、機能的に等しく視覚的にも識別不可能であるべき文字を識別する。もう1つは互換文字（）と呼ばれ、視覚的に異なり意味的にも異なるかもしれないものを識別する。詳細は[Unicodeの等価性](../Page/Unicodeの等価性.md "wikilink")と[Unicodeの互換文字](../Page/Unicodeの互換文字.md "wikilink")の記事を参照。

## 正規化形式

Unicode標準附属書UAX\#15では正規化に関して4種類の正規化形式を定義している。

<table>
<caption>正規化形式の一覧</caption>
<thead>
<tr class="header">
<th><p>名称（英語）</p></th>
<th><p>日本語名称</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>NFD</strong><br />
<em>Normalization Form Canonical Decomposition</em></p></td>
<td><p><strong></strong></p></td>
<td><p>文字は<a href="https://ja.wikipedia.org/wiki/Unicodeの等価性#正準等価" title="wikilink">正準等価性によって分解される</a>。</p></td>
</tr>
<tr class="even">
<td><p><strong>NFC</strong><br />
<em>Normalization Form Canonical Composition</em></p></td>
<td><p><strong></strong></p></td>
<td><p>文字は正準等価性によって分解され、再度合成される。結果として文字の並びが変換前と変わることもありうる。</p></td>
</tr>
<tr class="odd">
<td><p><strong>NFKD</strong><br />
<em>Normalization Form Compatibility Decomposition</em></p></td>
<td><p><strong></strong></p></td>
<td><p>文字は<a href="https://ja.wikipedia.org/wiki/Unicodeの等価性#互換等価" title="wikilink">互換等価性によって分解される</a>。</p></td>
</tr>
<tr class="even">
<td><p><strong>NFKC</strong><br />
<em>Normalization Form Compatibility Composition</em></p></td>
<td><p><strong></strong></p></td>
<td><p>文字は互換等価性によって分解され、正準等価性によって再度合成される。</p></td>
</tr>
</tbody>
</table>

上記の手法はすべて、文字の並びが正規化前にすでに分解されている場合も含め、分解された文字の出現順序を標準化する。これらは文字数が変化しなくても、文字や文字の並びを等価な文字やその並びに置き換えることがある。これらは正規化に要求されている符号化の一貫性を達成するために行われる。

## 各種OSでの採用状況

  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")のファイルシステム[HFS+](https://ja.wikipedia.org/wiki/HFS+ "wikilink")ではNFDの変種が用いられる（U+2000〜U+2FFF、U+F900〜U+FAFF、U+2F800〜U+2FAFFは分解されない）。

## 用語の日本語訳

ここでは日本語表記を原則として [Unicode Terminology English - Japanese](http://www.unicode.org/terminology/term_en_ja.html) にならっている。ただし、Combining Character Sequenceの公式日本語訳である「結合文字の並び」は日本語として誤解を与える可能性があるので、そのためあえて「結合文字列」と表記している。

## 脚注

## 関連項目

  - [Unicode](../Page/Unicode.md "wikilink")
  - [Unicodeの等価性](../Page/Unicodeの等価性.md "wikilink")
  - [Unicodeの互換文字](../Page/Unicodeの互換文字.md "wikilink")
  - [合成済み文字](https://ja.wikipedia.org/wiki/合成済み文字 "wikilink")
  - [合字](../Page/合字.md "wikilink")

## 外部リンク

  - [Unicode Standard Annex \#15: Unicode Normalization Forms](http://www.unicode.org/reports/tr15/)
  - [utf8proc: A library for normalization of Unicode texts](http://www.flexiguided.de/publications.utf8proc.en.html)

[ru:Юникод\#Алгоритмы нормализации](https://ja.wikipedia.org/wiki/ru:Юникод#Алгоритмы_нормализации "wikilink")

[Category:Unicode](https://ja.wikipedia.org/wiki/Category:Unicode "wikilink") [Category:Unicodeのアルゴリズム](https://ja.wikipedia.org/wiki/Category:Unicodeのアルゴリズム "wikilink")

1.  Unicodeの照合仕様は、正規化形式仕様とは別に、Unicode Technical Standard \#10 "Unicode Collation Algorithm" で定義される。