> この記事は[Specials \(Unicode block\)](https://ja.wikipedia.org/wiki/Specials_\(Unicode_block\))から翻訳されています。


**Specials**([ATOK](../Page/ATOK.md "wikilink")では「特殊用途文字」と訳される)は、[Unicode](../Page/Unicode.md "wikilink")においてU + FFF0 〜 FFFFの[基本多言語面](../Page/基本多言語面.md "wikilink")の最後に割り当てられる短いブロックである。 これらの16個のコードポイントのうち、5個がUnicode 3.0以降に割り当てられている。

  - <templatestyles src="Mono/styles.css" />
  - <templatestyles src="Mono/styles.css" />  注釈文字の開始
  - <templatestyles src="Mono/styles.css" />  注釈ブロックの終わり
  - <templatestyles src="Mono/styles.css" /> <span id="OBJ"> </span> <span id="OBJ"><span class="smallcaps smallcaps-smaller" data-ve-ignore="true">OBJECT REPLACEMENT CHARACTER</span></span> [複合ドキュメントなど](../Page/複合文書.md "wikilink")、指定されていない別のオブジェクトのテキスト内を置換する記号<span id="OBJ"><span class="smallcaps smallcaps-smaller" data-ve-ignore="true">OBJECT REPLACEMENT CHARACTER</span></span>
  - <templatestyles src="Mono/styles.css" />  不明な文字、認識できない文字、表現できない文字を置き換えるために使用される
  - <templatestyles src="Mono/styles.css" />  非文字
  - <templatestyles src="Mono/styles.css" />  非文字

FFFEとFFFFは通常の意味で割り当てられていないが、[Unicode文字ではないことが保証されている](https://ja.wikipedia.org/wiki/Unicode文字のマッピング "wikilink")。これらはテキストの符号化を推測するために使用できる。これらの文字を含むテキストはすべて、正しく符号化されたUnicodeテキストではないとされる。Unicodeの 文字をUnicodeテキストの先頭に挿入して[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")を示すことができる。そのようなテキストを読み取り、0xFFFEに遭遇したプログラムは、次のすべての文字の符号の順序を切り替える必要があることを認識する。 <templatestyles src="Mono/styles.css" /> [サムネイル](https://ja.wikipedia.org/wiki/ファイル:Replacement_character.svg "wikilink") �（多くの場合、白い疑問符の付いた黒い菱形または空の四角）は、 [Unicode](../Page/Unicode.md "wikilink")規格の*Specials*においてコードポイントU + FFFDに割り当てられている記号であり、システムがデータ内の文字列を正しいシンボルにレンダリングできない場合の問題を示すために使用される。通常はデータが無効であるか、どの文字とも一致しない場合に表示される。

仮に、[UTF-8](../Page/UTF-8.md "wikilink")での入力を想定したテキストエディタで、[ISO-8859-1エンコード](https://ja.wikipedia.org/wiki/ISO/IEC_8859-1 "wikilink")（ `0x66 0xFC 0x72` ）でドイツ語の単語 "für"を含むテキストファイルを開いたとする。最初と最後のバイトは[ASCII](../Page/ASCII.md "wikilink")において有効なUTF-8エンコードであるが、中間のバイト（ `0xFC` ）はUTF-8で有効なバイトではない。したがって、テキストエディターはこのバイトを置換文字記号に置き換えて、有効なUnicode [コードポイント](https://ja.wikipedia.org/wiki/コードポイント "wikilink")の文字列を生成できる。このときf�rと表示される。さらに、正しく実装されていないテキストエディタにおいては、UTF-8形式に置換して保存される可能性がある。このときテキストファイルのデータは`0x66 0xEF 0xBF 0xBD 0x72`-8859-1となり、「fï¿1/2r」として表示される([文字化け](../Page/文字化け.md "wikilink")を参照)。置換はすべてのエラーで同じであるため、元の文字を復元することはできない。

## コード表

## 歴史

以下に示す文書群は、Specialsブロックに特定の文字を定義する目的と過程を示したものである。

<table>
<thead>
<tr class="header">
<th><p><a href="../Page/Unicode.md" title="wikilink">Version</a></p></th>
<th></th>
<th><p>Count</p></th>
<th><p><a href="../Page/ユニコードコンソーシアム.md" title="wikilink">UTC</a> ID</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/情報技術規格国際委員会" title="wikilink">L2</a> ID</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1/SC_2" title="wikilink">WG2</a> ID</p></th>
<th><p>Document</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.0.0</p></td>
<td><p>U+FFFD</p></td>
<td><p>1</p></td>
<td></td>
<td></td>
<td></td>
<td><p>(to be determined)</p></td>
</tr>
<tr class="even">
<td><p>U+FFFE..FFFF</p></td>
<td><p>2</p></td>
<td></td>
<td></td>
<td></td>
<td><p>(to be determined)</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p><a href="https://www.unicode.org/wg2/docs/n2369.doc">doc</a>)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p><a href="https://www.unicode.org/wg2/docs/n2403.pdf">N2403</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2.1</p></td>
<td><p>U+FFFC</p></td>
<td><p>1</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>N1365</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n1353.doc">N1353</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n1603.doc">N1603</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>N1681</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n1894_02n3188_fpdam%2018.pdf">N1894</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>3.0</p></td>
<td><p>U+FFF9..FFFB</p></td>
<td><p>3</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>N1727</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n1703w97.doc">N1703</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="https://www.unicode.org/L2/L1998/98281R.htm">html</a>)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p><a href="https://www.unicode.org/wg2/docs/n1861.pdf">N1861</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p><a href="https://www.unicode.org/wg2/docs/n1884.doc">doc</a>)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n1920_02n3210_text_pdam_30_addlatin.pdf">N1920</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p><a href="https://www.unicode.org/wg2/docs/n1903.htm">html</a>, <a href="https://www.unicode.org/wg2/docs/n1903w97.doc">doc</a>)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="https://www.unicode.org/L2/L1998/98419.doc">doc</a>)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><references group="lower-alpha" responsive="1">
</references></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 参照

  - [Unicode](../Page/Unicode.md "wikilink")文字

## 参考文献

<references group="" responsive="1">

</references>

<references group="" responsive="1">

</references>

[カテゴリ:Unicodeのブロック](https://ja.wikipedia.org/wiki/カテゴリ:Unicodeのブロック "wikilink")