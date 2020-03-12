> この記事は[MacJapanese](https://ja.wikipedia.org/wiki/MacJapanese)から翻訳されています。


**MacJapanese** または **Mac OS Japanese** は、[アップルが](../Page/アップル_\(企業\).md "wikilink") [Shift_JIS](../Page/Shift_JIS.md "wikilink") を独自に拡張した[文字コード](../Page/文字コード.md "wikilink")である。

主に[Classic Mac OSのバージョン](../Page/Classic_Mac_OS.md "wikilink") 7.1からバージョン 9.*x*までの間で利用された。

## 対応する文字コード

MacJapaneseは[IANAによって登録されていない](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")。そのため RFC 2045 の [§ 6.3](http://tools.ietf.org/html/rfc2045#section-6.3) に従って、[XML](../Page/Extensible_Markup_Language.md "wikilink")、[MIMEなどでは](../Page/Multipurpose_Internet_Mail_Extensions.md "wikilink") "**x-Mac-Japanese**" という[文字列](../Page/文字列.md "wikilink")がこの文字コードの名前として使われている（アップル製である[iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")もこの名前を認識する\[1\]）。

また、MacJapaneseを[Unicode](../Page/Unicode.md "wikilink")にマッピング（対応付け）した上で、Unicode用の[文字符号化方式](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink")（[UTF-16](../Page/UTF-16.md "wikilink")、[UTF-8](../Page/UTF-8.md "wikilink")など）を使って符号化する方法もあり、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")のファイル名などにはこの方法が使われている。ただし、MacJapanese固有の文字を私用領域 (Private Use Area) のU+F860、U+F861、U+F862、U+F87A、U+F87E、U+F87Fを使って表現するので、macOS以外の環境との互換性は無い。

## 歴史

## 文字セット

以下、「0x」を数字の先頭に付けた[十六進法表記を用いて各文字のコードを表す](https://ja.wikipedia.org/wiki/十六進記数法 "wikilink")。

### 1バイト

0x00から0x7Fまでと0xA1から0xDFまでの部分（いわゆる[半角](https://ja.wikipedia.org/wiki/半角 "wikilink")文字の部分）は[JIS X 0201に準ずる](https://ja.wikipedia.org/wiki/JIS_X_0201 "wikilink")。ただし0x7Eには[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")に倣ってU+7Eの[チルダ](../Page/チルダ.md "wikilink")が割り当てられている。

次の記号が追加されている。

  - 0x80 …… U+5C reverse solidus (= backslash)、半角[バックスラッシュ](../Page/バックスラッシュ.md "wikilink")「」（[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink") の0x5Cと同じ）
  - 0xA0 …… U+A0 no-break space、[ノーブレークスペース](../Page/ノーブレークスペース.md "wikilink") (NBSP)
  - 0xFD …… U+A9 copyright sign、[著作権記号](https://ja.wikipedia.org/wiki/著作権記号 "wikilink")「」（○で囲まれた「C」）
  - 0xFE …… U+2122 trade mark sign、商標記号「」（「」）
  - 0xFF …… halfwidth horizontal ellipsis、半角の欧文用三点[リーダー](../Page/リーダー_\(記号\).md "wikilink")（半角幅の「」）

### 2バイト

2バイトで表される文字（いわゆる[全角](https://ja.wikipedia.org/wiki/全角 "wikilink")文字）は、[JIS X 0208](../Page/JIS_X_0208.md "wikilink")-1990 を基にしている。さらに0x8540から0x886Dに「Apple標準システム外字」（記号など）が、0xEB41から0xED96までに縦書き用の文字が追加されている。Apple標準システム外字のうちUnicodeに対応している文字には次のようなものがある。

#### Apple標準システム外字

<table>
<caption><a href="../Page/丸数字.md" title="wikilink">丸附き数字</a>・黒丸附き数字</caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>○で囲まれた1</p></td>
<td><p> </p></td>
<td></td>
<td><p>○で囲まれた11</p></td>
<td><p> </p></td>
<td></td>
<td><p>●で囲まれた白抜きの1</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>○で囲まれた2</p></td>
<td></td>
<td><p>○で囲まれた12</p></td>
<td></td>
<td><p>●で囲まれた白抜きの2</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>○で囲まれた3</p></td>
<td></td>
<td><p>○で囲まれた13</p></td>
<td></td>
<td><p>●で囲まれた白抜きの3</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>○で囲まれた4</p></td>
<td></td>
<td><p>○で囲まれた14</p></td>
<td></td>
<td><p>●で囲まれた白抜きの4</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>○で囲まれた5</p></td>
<td></td>
<td><p>○で囲まれた15</p></td>
<td></td>
<td><p>●で囲まれた白抜きの5</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>○で囲まれた6</p></td>
<td></td>
<td><p>○で囲まれた16</p></td>
<td></td>
<td><p>●で囲まれた白抜きの6</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>○で囲まれた7</p></td>
<td></td>
<td><p>○で囲まれた17</p></td>
<td></td>
<td><p>●で囲まれた白抜きの7</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>○で囲まれた8</p></td>
<td></td>
<td><p>○で囲まれた18</p></td>
<td></td>
<td><p>●で囲まれた白抜きの8</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>○で囲まれた9</p></td>
<td></td>
<td><p>○で囲まれた19</p></td>
<td></td>
<td><p>●で囲まれた白抜きの9</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>○で囲まれた10</p></td>
<td></td>
<td><p>○で囲まれた20</p></td>
<td><p> </p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<table>
<caption>丸括弧附き数字</caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>(1)</p></td>
<td><p> </p></td>
<td></td>
<td><p>(5)</p></td>
<td><p> </p></td>
<td></td>
<td><p>(9)</p></td>
<td><p> </p></td>
<td></td>
<td><p>(13)</p></td>
<td><p> </p></td>
<td></td>
<td><p>(17)</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>(2)</p></td>
<td></td>
<td><p>(6)</p></td>
<td></td>
<td><p>(10)</p></td>
<td></td>
<td><p>(14)</p></td>
<td></td>
<td><p>(18)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>(3)</p></td>
<td></td>
<td><p>(7)</p></td>
<td></td>
<td><p>(11)</p></td>
<td></td>
<td><p>(15)</p></td>
<td></td>
<td><p>(19)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>(4)</p></td>
<td></td>
<td><p>(8)</p></td>
<td></td>
<td><p>(12)</p></td>
<td></td>
<td><p>(16)</p></td>
<td></td>
<td><p>(20)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<table>
<caption>ドット附き数字</caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>1.</p></td>
<td><p> </p></td>
<td></td>
<td><p>4.</p></td>
<td><p> </p></td>
<td></td>
<td><p>7.</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>2.</p></td>
<td></td>
<td><p>5.</p></td>
<td></td>
<td><p>8.</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>3.</p></td>
<td></td>
<td><p>6.</p></td>
<td></td>
<td><p>9.</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<table>
<caption>大文字および小文字の<a href="../Page/ローマ数字.md" title="wikilink">ローマ数字</a></caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>I</p></td>
<td><p> </p></td>
<td></td>
<td><p>V</p></td>
<td><p> </p></td>
<td></td>
<td><p>IX</p></td>
<td><p> </p></td>
<td></td>
<td><p>i</p></td>
<td><p> </p></td>
<td></td>
<td><p>v</p></td>
<td><p> </p></td>
<td></td>
<td><p>ix</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>II</p></td>
<td></td>
<td><p>VI</p></td>
<td></td>
<td><p>X</p></td>
<td></td>
<td><p>ii</p></td>
<td></td>
<td><p>vi</p></td>
<td></td>
<td><p>x</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>III</p></td>
<td></td>
<td><p>VII</p></td>
<td></td>
<td><p>XI</p></td>
<td></td>
<td><p>iii</p></td>
<td></td>
<td><p>vii</p></td>
<td></td>
<td><p>xi</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>IV</p></td>
<td></td>
<td><p>VIII</p></td>
<td></td>
<td><p>XII</p></td>
<td></td>
<td><p>iv</p></td>
<td></td>
<td><p>viii</p></td>
<td></td>
<td><p>xii</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<table>
<caption>丸括弧附きアルファベット小文字</caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>(a)</p></td>
<td><p> </p></td>
<td></td>
<td><p>(e)</p></td>
<td><p> </p></td>
<td></td>
<td><p>(i)</p></td>
<td><p> </p></td>
<td></td>
<td><p>(m)</p></td>
<td><p> </p></td>
<td></td>
<td><p>(q)</p></td>
<td><p> </p></td>
<td></td>
<td><p>(u)</p></td>
<td><p> </p></td>
<td></td>
<td><p>(y)</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>(b)</p></td>
<td></td>
<td><p>(f)</p></td>
<td></td>
<td><p>(j)</p></td>
<td></td>
<td><p>(n)</p></td>
<td></td>
<td><p>(r)</p></td>
<td></td>
<td><p>(v)</p></td>
<td></td>
<td><p>(z)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>(c)</p></td>
<td></td>
<td><p>(g)</p></td>
<td></td>
<td><p>(k)</p></td>
<td></td>
<td><p>(o)</p></td>
<td></td>
<td><p>(s)</p></td>
<td></td>
<td><p>(w)</p></td>
<td><p> </p></td>
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
<td><p>(d)</p></td>
<td></td>
<td><p>(h)</p></td>
<td></td>
<td><p>(l)</p></td>
<td></td>
<td><p>(p)</p></td>
<td></td>
<td><p>(t)</p></td>
<td></td>
<td><p>(x)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<table>
<caption>単位記号</caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>mm</p></td>
<td><p> </p></td>
<td></td>
<td><p>cm</p></td>
<td><p> </p></td>
<td></td>
<td><p>km</p></td>
<td><p> </p></td>
<td></td>
<td><p>ml</p></td>
<td><p> </p></td>
<td></td>
<td><p>ms</p></td>
<td><p> </p></td>
<td></td>
<td><p>°F</p></td>
<td><p> </p></td>
<td></td>
<td><p>KB</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>mm</p></td>
<td></td>
<td><p>cm</p></td>
<td></td>
<td><p>mg</p></td>
<td></td>
<td><p>dl</p></td>
<td></td>
<td><p>μs</p></td>
<td></td>
<td><p>mb</p></td>
<td></td>
<td><p>MB</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>m</p></td>
<td></td>
<td><p>cm</p></td>
<td></td>
<td><p>kg</p></td>
<td></td>
<td><p>l</p></td>
<td></td>
<td><p>ns</p></td>
<td></td>
<td><p>HP</p></td>
<td></td>
<td><p>GB</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>m</p></td>
<td></td>
<td><p>km</p></td>
<td></td>
<td><p>cc</p></td>
<td></td>
<td><p>kl</p></td>
<td></td>
<td><p>ps</p></td>
<td></td>
<td><p>Hz</p></td>
<td><p> </p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<table>
<caption>アルファベットの組文字</caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>No.</p></td>
<td><p> </p></td>
<td></td>
<td><p>K.K.</p></td>
<td><p> </p></td>
<td></td>
<td><p>TEL</p></td>
</tr>
</tbody>
</table>

<table>
<caption><a href="../Page/スート.md" title="wikilink">スート</a>（トランプ記号）</caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>スペード記号</p></td>
<td><p> </p></td>
<td></td>
<td><p>白抜きスペード記号</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>ハート記号</p></td>
<td></td>
<td><p>白抜きハート記号</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>ダイヤ記号</p></td>
<td></td>
<td><p>白抜きダイヤ記号</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>クローバー記号</p></td>
<td></td>
<td><p>白抜きクローバー記号</p></td>
<td></td>
</tr>
</tbody>
</table>

<table>
<caption>その他記号</caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p><a href="../Page/顔郵便マーク.md" title="wikilink">顔郵便マーク</a></p></td>
<td><p> </p></td>
<td></td>
<td><p>黒電話</p></td>
<td><p> </p></td>
<td></td>
<td><p>旧 <a href="https://ja.wikipedia.org/wiki/JISマーク" title="wikilink">JISマーク</a></p></td>
</tr>
</tbody>
</table>

<table>
<caption>矢印記号</caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>指さし矢印上</p></td>
<td><p> </p></td>
<td></td>
<td><p>白抜き矢印上</p></td>
<td><p> </p></td>
<td></td>
<td><p>↑↓</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>指さし矢印下</p></td>
<td></td>
<td><p>白抜き矢印下</p></td>
<td></td>
<td><p>→<br />
←</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>指さし矢印左</p></td>
<td></td>
<td><p>白抜き矢印左</p></td>
<td></td>
<td><p>←<br />
→</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>指さし矢印右</p></td>
<td></td>
<td><p>白抜き矢印右</p></td>
<td><p> </p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<table>
<caption>丸括弧附き漢字</caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>（日）</p></td>
<td><p> </p></td>
<td></td>
<td><p>（金）</p></td>
<td><p> </p></td>
<td></td>
<td><p>（至）</p></td>
<td><p> </p></td>
<td></td>
<td><p>（名）</p></td>
<td><p> </p></td>
<td></td>
<td><p>（特）</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>（月）</p></td>
<td></td>
<td><p>（土）</p></td>
<td></td>
<td><p>（代）</p></td>
<td></td>
<td><p>（有）</p></td>
<td></td>
<td><p>（監）</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>（火）</p></td>
<td></td>
<td><p>（祭）</p></td>
<td></td>
<td><p>（呼）</p></td>
<td></td>
<td><p>（学）</p></td>
<td></td>
<td><p>（企）</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>（水）</p></td>
<td></td>
<td><p>（祝）</p></td>
<td></td>
<td><p>（株）</p></td>
<td></td>
<td><p>（財）</p></td>
<td></td>
<td><p>（協）</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>（木）</p></td>
<td></td>
<td><p>（自）</p></td>
<td></td>
<td><p>（資）</p></td>
<td></td>
<td><p>（社）</p></td>
<td></td>
<td><p>（労）</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<table>
<caption><a href="https://ja.wikipedia.org/wiki/囲み文字" title="wikilink">囲み文字</a></caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>○で囲まれた上</p></td>
<td><p> </p></td>
<td></td>
<td><p>○で囲まれた左</p></td>
<td><p> </p></td>
<td></td>
<td><p>○で囲まれた財</p></td>
<td><p> </p></td>
<td></td>
<td><p>○で囲まれた印</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>○で囲まれた中</p></td>
<td></td>
<td><p>○で囲まれた右</p></td>
<td></td>
<td><p>○で囲まれた優</p></td>
<td></td>
<td><p>○で囲まれた秘</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>○で囲まれた下</p></td>
<td></td>
<td><p>○で囲まれた医</p></td>
<td></td>
<td><p>○で囲まれた労</p></td>
<td><p> </p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<table>
<caption><a href="../Page/組文字.md" title="wikilink">組文字</a></caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>ミリ</p></td>
<td><p> </p></td>
<td></td>
<td><p>ヘクタール</p></td>
<td><p> </p></td>
<td></td>
<td><p>ミリバール</p></td>
<td><p> </p></td>
<td></td>
<td><p>ハイツ</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>キロ</p></td>
<td></td>
<td><p>リットル</p></td>
<td></td>
<td><p>ページ</p></td>
<td></td>
<td><p>ビル</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>センチ</p></td>
<td></td>
<td><p>ワット</p></td>
<td></td>
<td><p>アパート</p></td>
<td></td>
<td><p>フィート</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>メートル</p></td>
<td></td>
<td><p>カロリー</p></td>
<td></td>
<td><p>インチ</p></td>
<td></td>
<td><p>ヘルツ</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>グラム</p></td>
<td></td>
<td><p>ドル</p></td>
<td></td>
<td><p>キログラム</p></td>
<td></td>
<td><p>ホーン</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>トン</p></td>
<td></td>
<td><p>セント</p></td>
<td></td>
<td><p>キロメートル</p></td>
<td></td>
<td><p>マンション</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>アール</p></td>
<td></td>
<td><p>パーセント</p></td>
<td></td>
<td><p>コーポ</p></td>
<td></td>
<td><p>ヤード</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/株式会社" title="wikilink">株式会社</a></p></td>
<td><p> </p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<table>
<caption>数学記号</caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>閉曲線積分<br />
（閉路積分・周回積分）記号</p></td>
<td><p> </p></td>
<td></td>
<td><p>直角記号</p></td>
<td><p> </p></td>
<td></td>
<td><p>直角三角形</p></td>
</tr>
</tbody>
</table>

<table>
<caption><a href="../Page/引用符.md" title="wikilink">引用符</a></caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>始めダブルミニュート<br />
日本語用の「“」</p></td>
<td><p> </p></td>
<td></td>
<td><p>終わりダブルミニュート<br />
日本語用の「”」</p></td>
</tr>
</tbody>
</table>

<table>
<caption><a href="../Page/濁点.md" title="wikilink">濁点</a>附きのひらがな・カタカナ</caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>表記</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>う゛</p></td>
<td><p> </p></td>
<td></td>
<td><p>ワ゛</p></td>
<td><p> </p></td>
<td></td>
<td><p>ヰ゛</p></td>
<td><p> </p></td>
<td></td>
<td><p>ヱ゛</p></td>
<td><p> </p></td>
<td></td>
<td><p>ヲ゛</p></td>
</tr>
</tbody>
</table>

#### 縦書き用の文字

縦書き用文字には、[括弧](../Page/括弧.md "wikilink")などの記号を回転させたものと、[句読点](../Page/句読点.md "wikilink")と[小書きの仮名を右上に寄せたものがある](../Page/捨て仮名.md "wikilink")。「」（二点リーダ）、「」（三点リーダ）、「」「」（括弧）、「」「」（すみ付き括弧）など。三点リーダは U+FE19 に収録されているが、MacJapaneseのコードポイントとは異なり、互換性はない。

これらは、[DTP](../Page/DTP.md "wikilink")などの縦書きに対応したアプリケーションで縦書き表示をする際に、本来の文字コードを変換して[QuickDraw](../Page/QuickDraw.md "wikilink")の描画[APIに渡すために使われたものである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。通常、情報交換に使われることはない。

## 他の文字コードとの対応

全角文字に関しては、縦書き用文字を別にすると、次のように区分できる。

### 区分1

[NEC特殊文字にある文字](https://ja.wikipedia.org/wiki/Microsoftコードページ932#NEC特殊文字 "wikilink")。73字。

シフト符号化表現で符号化すると、MacJapaneseと [Windows-31J](../Page/Microsoftコードページ932.md "wikilink")、[Shift_JIS-2004](../Page/Shift_JIS-2004.md "wikilink") とでは別のコードポイントが与えられているために、[機種依存文字](../Page/機種依存文字.md "wikilink")として[文字化け](../Page/文字化け.md "wikilink")の原因となる。例えば「」（○で囲まれた「12」）は Windows-31J や Shift_JIS-2004 では 0x874B に割り当てられているが、MacJapanese においては 0x874B に「」（「（代）」）が割り当てられているといった具合である。[Unicode](../Page/Unicode.md "wikilink") においては同じコードポイントが与えられているため、文字化けは発生しない。

### 区分2

NEC特殊文字になく、[JIS X 0213](../Page/JIS_X_0213.md "wikilink") にはある文字。53字。

区分1と同じく、[Shift_JIS-2004](../Page/Shift_JIS-2004.md "wikilink") で表現するとMacJapaneseとは別のコードポイントが割り当てられているため、文字化けの原因となる。

### 区分3

NEC特殊文字にも JIS X 0213 にもなく、[Unicode](../Page/Unicode.md "wikilink")にはある文字。109字。

Unicodeのエンコーディング（[UTF-16](../Page/UTF-16.md "wikilink")、[UTF-8](../Page/UTF-8.md "wikilink")など）を用い、対応する文字の[グリフ](https://ja.wikipedia.org/wiki/グリフ "wikilink")が存在するフォントを利用すれば、正常に情報交換することができる。仮にMacJapaneseを用いて情報交換し、Unicode に変換しようとした場合には、「Unicode と MacJapanese の変換テーブル」を使わないと変換することができない。

### 区分4

NEC特殊文字にも JIS X 0213 にも[Unicode](../Page/Unicode.md "wikilink")にもないが、Unicodeでは文字合成で表せる文字。3字。

[囲み文字](https://ja.wikipedia.org/wiki/囲み文字 "wikilink")であり、記号用ダイアクリティカルマークU+20DDを用いた文字合成で表現するか、[CSS](../Page/CSS.md "wikilink")の [OpenType](../Page/OpenType.md "wikilink") feature tag で表現する。そのため、対応していないOS・フォントやアプリケーションで表示しようとしても、合成されるべきところが合成されずに表示される\[2\]。文字一覧を下記に記す。文字のうち、左は文字合成、右はCSSの OpenType feature tag を使用したもの。

<table>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p><a href="../Page/Unicode.md" title="wikilink">Unicode</a></p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>Unicode</p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>Unicode</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>大</p></td>
<td><p>U+5927<br />
U+20DD</p></td>
<td><p>○で囲まれた大[3]</p></td>
<td><p> </p></td>
<td></td>
<td><p>小</p></td>
<td><p>U+5C0F<br />
U+20DD</p></td>
<td><p>○で囲まれた小[4]</p></td>
<td><p> </p></td>
<td></td>
</tr>
</tbody>
</table>

### 区分5

NEC特殊文字にも JIS X 0213 にもUnicodeにもないが、同型・同用途の文字がUnicodeにある文字。7字。

Unicodeのエンコーディングと対応するフォントを用いて情報交換することはできるが、コードポイントは別であり、MacJapanese との互換性はない\[5\]。なお、MacJapanese で入力\[6\]した場合に Unicode へ変換するならば区分7に準ずる。Unicode のコードポイントにある同型の文字一覧を下記に記す。文字が2種類あるものは、左はUnicode、右はCSSの OpenType feature tag を使用したもの。

<table>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p><a href="../Page/Unicode.md" title="wikilink">Unicode</a></p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>Unicode</p></th>
<th><p>内容・表記</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>U+2B06</p></td>
<td><p>黒塗り矢印上[7]</p></td>
<td><p> </p></td>
<td></td>
<td><p>0</p></td>
<td><p>U+1F100</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>U+2B07</p></td>
<td><p>黒塗り矢印下[8]</p></td>
<td></td>
<td><p>FAX</p></td>
<td><p>U+213B</p></td>
<td><p>組文字・FAX[9]</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>U+2B05</p></td>
<td><p>黒塗り矢印左[10]</p></td>
<td></td>
<td><p>⇆</p></td>
<td><p>U+21F5</p></td>
<td><p>↓↑[11]</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>U+27A1</p></td>
<td><p>黒塗り矢印右[12]</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### 区分6

NEC特殊文字にも JIS X 0213 にもUnicodeにもないが、同型の別字が JIS X 0213 やUnicodeにある文字。2字。

区分5と同様に、別のコードポイントに同型の文字があるもの。この同型の文字は、MacJapaneseおよびJIS X 0213やUnicodeに収録されている。共に全角ラテン文字と同型。なお、MacJapanese で入力した場合に Unicode へ変換するならば区分7に準ずる。Unicode のコードポイントにある同型の文字一覧を下記に記す。

<table>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p><a href="../Page/Unicode.md" title="wikilink">Unicode</a></p></th>
<th><p>内容 (mac)</p></th>
<th><p>内容 (Unicode)</p></th>
<th><p> </p></th>
<th><p>文字</p></th>
<th><p>Unicode</p></th>
<th><p>内容 (mac)</p></th>
<th><p>内容 (Unicode)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>U+217F</p></td>
<td><p>メートル記号</p></td>
<td><p>ローマ数字小文字1000</p></td>
<td><p> </p></td>
<td></td>
<td><p>U+210A</p></td>
<td><p>グラム記号</p></td>
<td><p>スクリプト体小文字g（実数記号）</p></td>
</tr>
</tbody>
</table>

### 区分7

NEC特殊文字にも JIS X 0213 にもUnicodeにもなく、同型・同用途の文字もUnicodeにない文字。9字。

文字合成を行なったり[異体字](https://ja.wikipedia.org/wiki/異体字 "wikilink")タグを利用したりして表現することになる。そのためにUnicodeの私的領域であるU+F860、U+F861、U+F862、U+F87A、U+F87E、U+F87Fを使っている。したがって、MacJapaneseに対応していないフォントやアプリケーションで表示しようとしても、合成されるべきところが合成されずに表示されたり、異体字となったりする\[13\]。記号一覧を下記に記す。記号が2種類あるものは、右はCSSの OpenType feature tag を使用したもの。

<table>
<thead>
<tr class="header">
<th><p>記号</p></th>
<th><p>Unicode表記</p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>記号</p></th>
<th><p>Unicode表記</p></th>
<th><p>内容</p></th>
<th><p> </p></th>
<th><p>記号</p></th>
<th><p>Unicode表記</p></th>
<th><p>内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><table>
<tbody>
<tr class="odd">
<td><p>有</p></td>
<td><p>限</p></td>
</tr>
<tr class="even">
<td><p>会</p></td>
<td><p>社</p></td>
</tr>
</tbody>
</table></td>
<td></td>
<td><p>U+F862<br />
U+6709<br />
U+9650<br />
U+4F1A<br />
U+793E</p></td>
<td><p>組文字・<a href="../Page/有限会社.md" title="wikilink">有限会社</a></p></td>
<td><p> </p></td>
<td><p>XIII</p></td>
<td><p>U+F862<br />
U+0058<br />
U+0049<br />
U+0049<br />
U+0049</p></td>
<td><p>ローマ数字13大文字</p></td>
<td><p> </p></td>
<td><p>xiii</p></td>
<td><p>U+F862<br />
U+0078<br />
U+0069<br />
U+0069<br />
U+0069</p></td>
</tr>
<tr class="even">
<td><table>
<tbody>
<tr class="odd">
<td><p>財</p></td>
<td><p>団</p></td>
</tr>
<tr class="even">
<td><p>法</p></td>
<td><p>人</p></td>
</tr>
</tbody>
</table></td>
<td></td>
<td><p>U+F862<br />
U+8CA1<br />
U+56E3<br />
U+6CD5<br />
U+4EBA</p></td>
<td><p>組文字・<a href="../Page/財団法人.md" title="wikilink">財団法人</a></p></td>
<td><p>XIV</p></td>
<td><p>U+F861<br />
U+0058<br />
U+0049<br />
U+0056</p></td>
<td><p>ローマ数字14大文字</p></td>
<td><p>xiv</p></td>
<td><p>U+F861<br />
U+0078<br />
U+0069<br />
U+0076</p></td>
<td><p>ローマ数字14小文字</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>TB</p></td>
<td></td>
<td><p>U+F860<br />
U+0054<br />
U+0042</p></td>
<td><p>単位・テラバイト</p></td>
<td><p>XV</p></td>
<td><p>U+F860<br />
U+0058<br />
U+0056</p></td>
<td><p>ローマ数字15大文字</p></td>
<td><p>xv</p></td>
<td><p>U+F860<br />
U+0078<br />
U+0076</p></td>
<td><p>ローマ数字15小文字</p></td>
<td></td>
</tr>
</tbody>
</table>

## macOS での対応

[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")においては、MacJapaneseは「Shift_JIS (Mac)」（文字パレット）あるいは「日本語 (Mac OS)」（[テキストエディット](https://ja.wikipedia.org/wiki/TextEdit "wikilink")）と表現される。

また、macOS附属のフォントでは[OsakaのみがMacJapaneseに完全対応している](../Page/Osaka_\(書体\).md "wikilink")。[ヒラギノ](../Page/ヒラギノ.md "wikilink")はUnicodeと[CIDに対応しているため](../Page/CID_\(文字コード\).md "wikilink")、Unicodeを扱えるアプリケーション上ではUnicodeに対応する文字が存在しない18字（上記の区分5〜7 ）を除いてMacJapaneseの文字を表示できる。一方、CID を扱えるアプリケーション上でヒラギノを使う場合には、halfwidth horizontal ellipsis （半角三点リーダー）以外の文字を全て表示できる。

## iPod での対応

## 脚注

## 関連項目

  - [文字コード](../Page/文字コード.md "wikilink")

  - [JIS X 0208](../Page/JIS_X_0208.md "wikilink")

  - [Shift_JIS](../Page/Shift_JIS.md "wikilink")

  - [Microsoftコードページ932](../Page/Microsoftコードページ932.md "wikilink")

  - [Unicode](../Page/Unicode.md "wikilink")

  - [囲み文字](https://ja.wikipedia.org/wiki/囲み文字 "wikilink")

  - [ARIB外字](https://ja.wikipedia.org/wiki/ARIB外字 "wikilink")

  -
## 外部リンク

  - [Map (external version) from Mac OS Japanese encoding to Unicode 2.1 and later.](http://unicode.org/Public/MAPPINGS/VENDORS/APPLE/JAPANESE.TXT)
  - [JIS漢字コード　97年改正の概要と将来展望](http://software.nikkeibp.co.jp/software/special/jiscode/nc.html) (Apple標準システム外字の一覧あり)

[Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink") [Category:Classic_Mac_OS](https://ja.wikipedia.org/wiki/Category:Classic_Mac_OS "wikilink") [Category:Unicodeに存在しない文字](https://ja.wikipedia.org/wiki/Category:Unicodeに存在しない文字 "wikilink") [Category:日本語用の文字コード](https://ja.wikipedia.org/wiki/Category:日本語用の文字コード "wikilink")

1.  [iPod 2.0: 日本語、韓国語、繁体字中国語、簡体字中国語で作成されたテキストファイルを表示する方法](http://docs.info.apple.com/article.html?artnum=61894)
2.  [Classic Mac OS](../Page/Classic_Mac_OS.md "wikilink")・[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") であれば標準の環境なら正しく表示されるが、[Windowsでは合成に対応したフォントが少ないのが現状](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。無料導入できるものは[和田研フォントをベースにしたものがあり](https://ja.wikipedia.org/wiki/和田研フォント#和田研細丸ゴシック "wikilink")、[和田研細丸ゴシック Wiki - SourceForge.JP](http://sourceforge.jp/projects/jis2004/wiki/FrontPage)の下部にて「和田研細丸ゴシックProN」がダウンロード可能。他にも、[にしき的フォント](http://hwm3.gyao.ne.jp/shiroi-niwatori/nishiki-teki.htm)にある手書きのポップ体「Nishiki-teki」が対応している。
3.
4.
5.  Unicodeで[ARIB外字](https://ja.wikipedia.org/wiki/ARIB外字 "wikilink")を扱えるフォントなどが表示に対応している。無料導入できるものは[和田研フォントをベースにしたものがあり](https://ja.wikipedia.org/wiki/和田研フォント#和田研細丸ゴシック "wikilink")、[和田研細丸ゴシック Wiki - SourceForge.JP](http://sourceforge.jp/projects/jis2004/wiki/FrontPage)の下部にて「和田研細丸ゴシック2004絵文字、和田研中丸ゴシック2004絵文字」がダウンロード可能。旧バージョンの「和田研細丸ゴシック2004ARIB、和田研中丸ゴシック2004ARIB」も対応。
6.  macOSでは通常の変換でリストに出てこないため、過去の文章との互換性を保つ目的と思われる。
7.
8.
9.
10.
11. 無料で導入できるフォントで表示に対応しているものは、[Y.Oz Vox](http://yozvox.web.infoseek.co.jp/)にある「YOzFont」や、Unicodeフォントの「Code2000」、[にしき的フォント](http://hwm3.gyao.ne.jp/shiroi-niwatori/nishiki-teki.htm)にある手書きのポップ体「Nishiki-teki」などがある。
12.
13.