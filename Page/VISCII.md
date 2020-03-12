> この記事は[VISCII](https://ja.wikipedia.org/wiki/VISCII)から翻訳されています。


**Vietnamese Standard Code for Information Interchange** (情報交換用ベトナム語標準符号、**VISCII**) は[ベトナム語アルファベット](../Page/クオック・グー.md "wikilink")、[約物](../Page/約物.md "wikilink")、およびその他の[書記素](../Page/書記素.md "wikilink")からなる[文字コード](../Page/文字コード.md "wikilink")である。ベトナム語は伝統的な[拡張ASCII](../Page/拡張ASCII.md "wikilink")文字コードを作るには多少多い (134文字) 文字とダイアクリティカルマークの組み合わせを必要とする。この解決策は本質的に3通り存在する。

1.  可変長の符号化を使用する
2.  [Windows-1258](https://ja.wikipedia.org/wiki/Windows-1258 "wikilink")のように、[合成可能なダイアクリティカルマークを使用する](https://ja.wikipedia.org/wiki/結合文字 "wikilink")
3.  ASCIIの何かを置き換える

VISCIIは最後の選択肢を採用し、最も問題が少なそうな (たとえば、アプリケーションが認識して特殊な動作をすることがもっともありそうにない) 6文字の[C0制御符号](https://ja.wikipedia.org/wiki/C0とC1制御符号 "wikilink") (STX, ENQ, ACK, DC4, EM, および RS) を6文字の最も使用頻度が低い大文字とダイアクリティカルマークの組み合わせで置き換えた。これはVISCIIテキストを処理するプログラムがそれらの制御符号を使っていた場合問題になりうるが、他の2つの解決策のどちらよりも単純である。しかしながら、記号、上付き文字、方向付き引用符、正しいダッシュのような、アクセント付き文字以外ものを収容する空きはまったくない。

VISCIIは、他のベトナム語固有の文字コードと同様、[Unicode](../Page/Unicode.md "wikilink")の採用によって使われなくなりつつある。

## コードページのレイアウト

<table style="width:1000%;">
<colgroup>
<col style="width: 40%" />
<col style="width: 60%" />
<col style="width: 60%" />
<col style="width: 60%" />
<col style="width: 60%" />
<col style="width: 60%" />
<col style="width: 60%" />
<col style="width: 60%" />
<col style="width: 60%" />
<col style="width: 60%" />
<col style="width: 60%" />
<col style="width: 60%" />
<col style="width: 60%" />
<col style="width: 60%" />
<col style="width: 60%" />
<col style="width: 60%" />
<col style="width: 60%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p>.0</p></td>
<td><p>.1</p></td>
<td><p>.2</p></td>
<td><p>.3</p></td>
<td><p>.4</p></td>
<td><p>.5</p></td>
<td><p>.6</p></td>
<td><p>.7</p></td>
<td><p>.8</p></td>
<td><p>.9</p></td>
<td><p>.A</p></td>
<td><p>.B</p></td>
<td><p>.C</p></td>
<td><p>.D</p></td>
<td><p>.E</p></td>
<td><p>.F</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
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
<td></td>
<td></td>
<td></td>
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
<td></td>
<td></td>
<td></td>
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
<td></td>
<td></td>
<td></td>
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
<td></td>
<td></td>
<td></td>
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
<td></td>
<td></td>
<td></td>
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
<td></td>
<td></td>
<td></td>
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
<td></td>
<td></td>
<td></td>
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
<td></td>
<td></td>
<td></td>
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
<td></td>
<td></td>
<td></td>
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
<td></td>
<td></td>
<td></td>
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
<td></td>
<td></td>
<td></td>
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
<td></td>
<td></td>
<td></td>
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
<td></td>
<td></td>
<td></td>
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
<td></td>
<td></td>
<td></td>
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
<td></td>
<td></td>
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

## 外部リンク

  - RFC 1456 - Conventions for Encoding the Vietnamese Language (ベトナム語符号化の規約、英語)
  - [Vietnamese-Standard Working Group](http://www.vietstd.org/) (ベトナム規格作業部会、英語)
  - [Viet-Std Report 1992](http://www.vnet.org/vietstd/report/rep92.htm) (英語)
  - [AnGiang Software](http://www.xmlunify.com/angiang_ss1.htm) (英語)

[Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink") [Category:ベトナム語](https://ja.wikipedia.org/wiki/Category:ベトナム語 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")