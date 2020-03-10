> この記事は[Shift JIS-2004](https://ja.wikipedia.org/wiki/Shift_JIS-2004)から翻訳されています。


**Shift_JIS-2004**は、日本の文字を符号化するのに使われる[文字コード](../Page/文字コード.md "wikilink")である。[JIS X 0213の符号化方式のひとつである](../Page/JIS_X_0213.md "wikilink")。JIS X 0213:2004の附属書1で定義されている。

[JIS X 0208の符号化方式のひとつである](../Page/JIS_X_0208.md "wikilink")[Shift_JIS](../Page/Shift_JIS.md "wikilink")と同様に、[JIS X 0201の](https://ja.wikipedia.org/wiki/JIS_X_0201 "wikilink")1バイト文字とJIS X 0213の2バイト文字とを組み合わせて運用する符号化方式である。Shift_JISの上位互換となっている。

JIS X 0213には94文字×94文字の**面**が2つあるが、JIS X 0208の上位互換である第1面はShift_JISの第1バイト0xEFまでの範囲に収まる。面区点番号からShift_JIS-2004のバイト値を求める際、この範囲までの計算方法はShift_JISと同じである。Shift_JIS-2004ではさらに、第2面 (第4水準漢字) を収録するために、第1バイト0xF0から0xFCまでの範囲を用いる。2面で、区番号が1, 3, 4, 5, 8, 12, 13, 14, 15 のときは、第1バイトは (区番号 + 0x1DF) ÷ 2 − (区番号 ÷ 8) × 3 となる。区番号が78から94までのときは、第1バイトは (区番号 + 0x19B) ÷ 2 となる。こうしてJIS X 0213の11,233文字全てを2バイトで表現する。

なお、JIS X 0213の初版 (2000年) では、この符号化方式はShift_JISX0213と命名されていた。2004年改正で追加されたUCS互換漢字10文字の有無だけが異なるが、大きな違いではないためShift_JIS-2004と同一視されることもある。

## 構造

Shift_JISでは空き領域や未使用であった場所に文字が追加されている。

## 計算方法

\[s_1 = \begin{cases} \left \lfloor \frac{k + 257}{2} \right \rfloor & \mbox{if } m = 1 \mbox{ and } 1 \le k \le 62 \\
                           \left \lfloor \frac{k + 385}{2} \right \rfloor & \mbox{if } m = 1 \mbox{ and } 63 \le k \le 94 \\
                           \left \lfloor \frac{k + 479}{2} \right \rfloor - \left \lfloor \frac{k}{8} \right \rfloor \times 3 & \mbox{if } m = 2 \mbox{ and } k = 1, 3, 4, 5, 8, 12, 13, 14, 15 \\
                           \left \lfloor \frac{k + 411}{2} \right \rfloor & \mbox{if } m = 2 \mbox{ and } 78 \le k \le 94             \end{cases}\]

\[s_2 = \begin{cases} t + 63 & \mbox{if } k \mbox{ is odd and } 1 \le t \le 63 \\
                           t + 64 & \mbox{if } k \mbox{ is odd and } 64 \le t \le 94 \\
                           t + 158 & \mbox{if } k \mbox{ is even }
             \end{cases}\]

面区点番号からShift_JIS-2004の第1・第2バイトは以下の通り求められます。\[1\]

面番号を m、区番号を k、点番号を t とする。また、記号 ÷ は整数除算 (小数点以下切捨て)を表す。

第1バイト(S1)は、以下による:

1.  m = 1 で 1 ≦ k ≦ 62 のとき, S1 = (k + 0x101) ÷ 2.
2.  m = 1 で 63 ≦ k ≦ 94 のとき, S1 = (k + 0x181) ÷ 2.
3.  m = 2 で, k = 1, 3, 4, 5, 8, 12, 13, 14, 15 のとき, S1 = (k + 0x1df) ÷ 2 － (k ÷ 8) × 3.
4.  m = 2 で, 78 ≦ k ≦ 94 のとき, S1 = (k + 0x19b) ÷ 2.

第2バイト(S2)は、以下による:

1.  k が奇数の場合:
    1.  1 ≦ t ≦ 63 のとき, S2 = t + 0x3f.
    2.  64 ≦ t ≦ 94 のとき, S2 = t + 0x40.
2.  k が偶数の場合, S2 = t + 0x9e.

## Windows-31Jとの非互換

Shift_JIS-2004は、Windows-31Jとは併用できない符号化方式である。

<table>
<thead>
<tr class="header">
<th><p>Shift_JIS</p></th>
<th><p>Windows-31J</p></th>
<th><p>Shift_JIS-2004</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JIS X 0208</p></td>
<td><p>JIS X 0208</p></td>
<td><p>JIS X 0213に含まれる。</p></td>
</tr>
<tr class="even">
<td><p>未定義</p></td>
<td><p>NEC特殊文字</p></td>
<td><p>(0x8740 - 0x879C) JIS X 0213に含まれる。<br />
ただし、重複分は削除されている（「≒」「≡」「∫」「Σ」「√」「⊥」「∠」「∵」「∩」「∪」）。<br />
「∑ (N-ARY SUMMATION)」はギリシャ大文字シグマ「Σ」で代用。<br />
また、同領域に追加されている文字がある（「Ⅺ」「Ⅻ」）。</p></td>
</tr>
<tr class="odd">
<td><p>未定義</p></td>
<td><p>NEC選定IBM拡張文字</p></td>
<td><p>(0xED40 - 0xEEFC)は、JIS X 0213の1面で使用されており、併用できない。</p></td>
</tr>
<tr class="even">
<td><p>未定義</p></td>
<td><p>ユーザー定義外字領域</p></td>
<td><p>(0xF040 - 0xF9FC)は、JIS X 0213の2面で使用されており、併用できない。</p></td>
</tr>
<tr class="odd">
<td><p>未定義</p></td>
<td><p>IBM拡張文字</p></td>
<td><p>(0xFA40 - 0xFC4B)は、JIS X 0213の2面で使用されており、併用できない。</p></td>
</tr>
</tbody>
</table>

## 関連項目

  - [Shift_JIS](../Page/Shift_JIS.md "wikilink")
  - [EUC-JIS-2004](https://ja.wikipedia.org/wiki/EUC-JIS-2004 "wikilink")
  - [ISO-2022-JP-2004](https://ja.wikipedia.org/wiki/ISO-2022-JP-2004 "wikilink")
  - [JIS X 0213](../Page/JIS_X_0213.md "wikilink")
      - [JIS X 0213非漢字一覧](https://ja.wikipedia.org/wiki/JIS_X_0213非漢字一覧 "wikilink")
      - [JIS X 0213漢字一覧の1面](https://ja.wikipedia.org/wiki/JIS_X_0213漢字一覧の1面 "wikilink")
      - [JIS X 0213漢字一覧の2面](https://ja.wikipedia.org/wiki/JIS_X_0213漢字一覧の2面 "wikilink")

## 脚注

## 外部リンク

  - [JIS X 0213の代表的な符号化方式](http://www.asahi-net.or.jp/~wq6k-yn/code/enc-x0213.html)
  - [文字コード表 - 日本語 (シフト JIS) - shift_jis2004 - UIC](https://uic.jp/charset/show/shiftjis2004/)

[Category:日本語用の文字コード](https://ja.wikipedia.org/wiki/Category:日本語用の文字コード "wikilink")

1.   Hexadecimal numbers in the source have been converted to decimal for display.