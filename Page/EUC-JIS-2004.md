> この記事は[EUC-JIS-2004](https://ja.wikipedia.org/wiki/EUC-JIS-2004)から翻訳されています。


**EUC-JIS-2004**は、日本の文字を符号化するために使われる[文字コード](../Page/文字コード.md "wikilink")である。[JIS X 0213の符号化方式のひとつである](../Page/JIS_X_0213.md "wikilink")。JIS X 0213:2004の附属書3で定義されている。

以下のようなコード値の割り当てによって、[ASCII](../Page/ASCII.md "wikilink")とJIS X 0213、および[JIS X 0201片仮名を混在させる符号化方式である](https://ja.wikipedia.org/wiki/JIS_X_0201 "wikilink")。

  - コード値0x20から0x7FまではASCII (厳密には[ISO/IEC 646](https://ja.wikipedia.org/wiki/ISO/IEC_646 "wikilink") 国際基準版) を用いる。
  - コード値0xA1から0xFEまでは、2バイトを用いてJIS X 0213の第1面を表現する。この部分はJIS X 0208の上位互換である。
  - 0x8Fに続く2バイト文字1文字分 (0xA1から0xFEまでの2バイト) は、JIS X 0213の第2面の文字である。
  - 0x8Eに続く1文字分 (0xA1から0xFEまで) は、JIS X 0201片仮名を表す。

[ISO/IEC 2022の言葉で言えば](https://ja.wikipedia.org/wiki/ISO/IEC_2022 "wikilink")、G0にASCII、G1にJIS X 0213第1面、G2にJIS X 0201片仮名、G3にJIS X 0213第2面を指示した状態で、GLにG0、GRにG1を呼び出して運用するものである。G2を使うためにSS2、G3を使うためにSS3を用いる。

この符号化方式の[EUC-JP](../Page/EUC-JP.md "wikilink")との違いは、[JIS X 0208の代わりにJIS](../Page/JIS_X_0208.md "wikilink") X 0213第1面を用いることと、[JIS X 0212補助漢字の代わりにJIS](../Page/JIS_X_0212.md "wikilink") X 0213第2面を用いることである。JIS X 0213第1面はJIS X 0208の上位互換であり、またEUC-JPにおける補助漢字は実態としてほとんど使われていないため、既存のEUC-JPの文書はほとんどの場合そのままEUC-JIS-2004の文書として扱うことができる。

なお、この符号化方式はJIS X 0213の初版 (2000年) ではEUC-JISX0213と命名されていた。2004年改正におけるUCS互換漢字10文字の有無だけが異なるが、大きな違いではないためEUC-JIS-2004と同一視されることもある。

## 関連項目

  - [Extended Unix Code](../Page/Extended_Unix_Code.md "wikilink")
  - [ISO-2022-JP-2004](https://ja.wikipedia.org/wiki/ISO-2022-JP-2004 "wikilink")
  - [Shift JIS-2004](../Page/Shift_JIS-2004.md "wikilink")

[Category:日本語用の文字コード](https://ja.wikipedia.org/wiki/Category:日本語用の文字コード "wikilink")