> この記事は[EUC-JP](https://ja.wikipedia.org/wiki/EUC-JP)から翻訳されています。


**EUC-JP**（**E**xtended **U**NIX **C**ode Packed Format for **J**a**p**anese、**日本語EUC**）は[UNIX](../Page/UNIX.md "wikilink")上で[日本語](../Page/日本語.md "wikilink")の文字を扱う場合に利用されてきた[文字コード](../Page/文字コード.md "wikilink")（[符号化方式](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink")）のひとつである。UNIX以外の[OS上で使われることもある](../Page/オペレーティングシステム.md "wikilink")。

[1980年代](../Page/1980年代.md "wikilink")前半、日本語UNIXシステム諮問委員会がUNIXで日本語を扱うための文字コードについて議論を行い、議論の結果をもとに[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")4月に同委員会から報告書が[AT\&T](../Page/AT&T.md "wikilink")に出され、AT\&Tにより定められたのがEUC-JPの起こりである。AT\&Tから、*[EUC](../Page/Extended_Unix_Code.md "wikilink")*（Extended UNIX Codeの略）として日本語に限らず[多言語](../Page/多言語.md "wikilink")に対応できるように定められ、EUCのうち日本語を扱うものを特にEUC-JPなどと呼ぶ。他に、[EUC-KR](https://ja.wikipedia.org/wiki/EUC-KR "wikilink")（韓国語）、[EUC-CN](https://ja.wikipedia.org/wiki/EUC-CN "wikilink")（簡体中国語）等がある。

EUCの[エンコード方式上に](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink")[ASCII](../Page/ASCII.md "wikilink")と[JIS X 0208文字集合を配置したもので](../Page/JIS_X_0208.md "wikilink")、[半角カナ](../Page/半角カナ.md "wikilink") ([JIS X 0201](https://ja.wikipedia.org/wiki/JIS_X_0201 "wikilink")) とJIS補助漢字 ([JIS X 0212](../Page/JIS_X_0212.md "wikilink")) も含むことができる。半角カナと補助漢字を使用しない場合は、JIS X 0208で規定されている符号化方式「国際基準版・漢字用8ビット符号」と同一となる。[ISO/IEC 2022に適合する](https://ja.wikipedia.org/wiki/ISO/IEC_2022 "wikilink")。

日本語文字は[JIS X 0208をGR領域に表現したものを基本としており](../Page/JIS_X_0208.md "wikilink")、2バイトで表現され、1バイト目、2バイト目ともに0x80 - 0xFFの範囲内にある。このため英数字と日本語文字の区別がしやすく、[プログラム上での扱いが楽である](../Page/プログラム_\(コンピュータ\).md "wikilink")。ただし、半角カナは[ISO-2022-JP](../Page/ISO-2022-JP.md "wikilink")や[Shift_JIS](../Page/Shift_JIS.md "wikilink")と異なり制御文字SS2（シングルシフトツー、0x8E）に続けて現れるので都合2バイト、補助漢字は制御文字SS3（シングルシフトスリー、0x8F）に続けて現れるので都合3バイトを要する。

[JIS X 0213](../Page/JIS_X_0213.md "wikilink"):2004に対応するEUCコードは[EUC-JIS-2004](../Page/EUC-JIS-2004.md "wikilink")（2000年初版時はEUC-JISX0213）。

UNIX系OSの標準的な文字エンコードとして使用されてきた。 日本語の8万字の文字鏡フォントを含む[今昔文字鏡](../Page/今昔文字鏡.md "wikilink")が出た1997年以降は、より多くの日本語を扱うことができるよう[UTF-8](../Page/UTF-8.md "wikilink"), [UTF-16](../Page/UTF-16.md "wikilink")を使用したシステムも普及している。

## EUC-JPの亜種

EUC-JPには亜種が存在する。二種類を以下に解説する。

**eucJP-ms**は、[オープン・グループ](https://ja.wikipedia.org/wiki/オープン・グループ "wikilink")及び[日本ベンダ協議会](https://ja.wikipedia.org/wiki/日本ベンダ協議会 "wikilink")が策定した文字符号化方式。実装例は[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink") v5.0以降等。

**CP51932**は[マイクロソフト](../Page/マイクロソフト.md "wikilink")が[Windowsで使用している](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Windows-31JのEUC](../Page/Microsoftコードページ932.md "wikilink")-JP互換表現。実装例は[Internet Explorer](../Page/Internet_Explorer.md "wikilink")4.0以降、[EmEditor](../Page/EmEditor.md "wikilink")、[秀丸エディタ](../Page/秀丸エディタ.md "wikilink")等。このコードは[NECの](../Page/日本電気.md "wikilink")[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")の漢字コード（9区から12区の特殊文字を除外したもの）を[GR](../Page/GR.md "wikilink")表現したような体裁を持つ。ただし、PC-9800シリーズの漢字コードは[JIS C 6226](https://ja.wikipedia.org/wiki/JIS_C_6226 "wikilink")-1978をベースにするのに対して、CP51932は[JIS X 0208](../Page/JIS_X_0208.md "wikilink")-1990をベースとする点が異なる。

<table>
<thead>
<tr class="header">
<th><p> </p></th>
<th><p>CP51932</p></th>
<th><p>eucJP-ms</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>面＆区番号</p></td>
<td><p>1バイト目</p></td>
<td><p>2バイト目</p></td>
</tr>
<tr class="even">
<td><p>JIS X 0208-1990<br />
(ひらがな・カタカナ等)</p></td>
<td><p>1面1区 - 8区</p></td>
<td><p>0xA1 - 0xA8</p></td>
</tr>
<tr class="odd">
<td><p>NEC特殊文字</p></td>
<td><p>1面13区</p></td>
<td><p>0xAD</p></td>
</tr>
<tr class="even">
<td><p>JIS X 0208-1990<br />
(第一・第二水準漢字)</p></td>
<td><p>1面14区 - 84区</p></td>
<td><p>0xB0 - 0xF4</p></td>
</tr>
<tr class="odd">
<td><p>NEC選定IBM拡張文字</p></td>
<td><p>1面89区 - 92区</p></td>
<td><p>0xF9 - 0xFC</p></td>
</tr>
<tr class="even">
<td><p>ユーザ定義文字<br />
(前半)</p></td>
<td><p>―</p></td>
<td><p>―</p></td>
</tr>
<tr class="odd">
<td><p>JIS X 0212-1990<br />
(前半)</p></td>
<td><p>2面1区 - 11区</p></td>
<td><p>0x8F</p></td>
</tr>
<tr class="even">
<td><p>JIS X 0212-1990<br />
(後半)</p></td>
<td><p>2面16区 - 77区</p></td>
<td><p>0xB0 - 0xED</p></td>
</tr>
<tr class="odd">
<td><p>IBM拡張文字<br />
(JIS X 0212 以外)</p></td>
<td><p>2面83区 - 84区</p></td>
<td><p>0xF3 - 0xF4</p></td>
</tr>
<tr class="even">
<td><p>ユーザ定義文字<br />
(後半)</p></td>
<td><p>2面85区 - 94区</p></td>
<td><p>0xF5 - 0xFE</p></td>
</tr>
</tbody>
</table>

## 参考文献

  - 中原康: 日本語処理技術, 電気学会雑誌, 第106巻, 第12号 (1986年12月), pp.1198-1202.
  - 小野芳彦: UNIXの日本語化の実現方法, 情報処理, Vol.27, No.12 (1986年12月), pp.1393-1400.
  - 中原康: 日本語EUCの定義と解説, Revision 1.7, UI-OSF-USLP共同技術資料 (1991年12月10日).

[de:Extended UNIX Coding\#EUC-JP](https://ja.wikipedia.org/wiki/de:Extended_UNIX_Coding#EUC-JP "wikilink") [en:Extended Unix Code\#EUC-JP](https://ja.wikipedia.org/wiki/en:Extended_Unix_Code#EUC-JP "wikilink") [fr:Extended Unix Coding\#EUC-JP](https://ja.wikipedia.org/wiki/fr:Extended_Unix_Coding#EUC-JP "wikilink") [zh:EUC\#EUC-JP](https://ja.wikipedia.org/wiki/zh:EUC#EUC-JP "wikilink")

[Category:日本語用の文字コード](https://ja.wikipedia.org/wiki/Category:日本語用の文字コード "wikilink")