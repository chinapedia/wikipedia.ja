> この記事は[UTF-32](https://ja.wikipedia.org/wiki/UTF-32)から翻訳されています。


**UTF-32**（および**UCS-4**、[\#歴史](https://ja.wikipedia.org/wiki/#歴史 "wikilink")を参照）は、[Unicode](../Page/Unicode.md "wikilink")の各[符号位置に](https://ja.wikipedia.org/wiki/符号点 "wikilink")[32ビット](../Page/32ビット.md "wikilink")符号単位一つだけを使う、固定長のUnicodeの符号化形式及び符号化スキーム（[文字符号化方式\#文字符号化形式と文字符号化スキーム](https://ja.wikipedia.org/wiki/文字符号化方式#文字符号化形式と文字符号化スキーム "wikilink")）である。他のUTF（）はすべて符号位置によって符号単位列の長さが変化する可変長であるため、UTF-32はもっとも単純なUTFであるとみなせる。

UTF-32は、[テキストファイル](../Page/テキストファイル.md "wikilink")で使用されることは少なく、主にシステムの[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")上での管理や、符号位置の数で管理する[データベース](../Page/データベース.md "wikilink")などで使用される。

## 概要

一般にシステムが文字を扱う場合には、必要な1つの符号位置にアクセスすることで文字情報（グリフの形状や文字の持つ意味など）を取得する。UTF-32の場合は対象の1領域のみアクセスすることで対象となる文字情報を得ることができるが、可変長のUnicode形式では1つの符号位置を特定するために複数回のアクセスが必要となる。そのため、アクセス対象のメモリ上に配置する場合には固定長であるUTF-32が使用されることがある。

昨今のデータベースでは、バイト数ではなく、符号位置の数で領域を確保できる型を利用できる。符号位置数の型では他のUnicode形式では固定のバイト数を確保できないが、UTF-32の場合にはバイト数が固定であるため物理サイズをディスク上に確保することが可能である。

データのサイズで見た場合、他の文字符号化スキームと比較するとサイズは大きくなる。また文字列の表示幅の計算も、非常に限られた場合を除いて全く簡単にはならない。なぜならば「固定幅」フォントを使った場合でさえ、一つの文字位置に対して複数の符号位置が存在するかもしれない（[結合文字](https://ja.wikipedia.org/wiki/結合文字 "wikilink")など）し、一つの符号位置に対して複数の文字位置を使うかもしれない（[CJKV](../Page/CJKV.md "wikilink")漢字など）。結合文字があるので、エディタは1つの符号位置を編集時の一単位とみなすこともできない。

これらの理由からデータの交換などの場合にはUTF-32はほとんど使われず、[UTF-8](../Page/UTF-8.md "wikilink")や[UTF-16](../Page/UTF-16.md "wikilink")がUnicode文書の通常の符号化スキームとして使われている。

なお、特定の文字がUnicodeでどの符号位置になるかをテキストで表現する場合には、U+10001などのようにUTF-32で扱った場合の16進数表記が使用されることがほとんどである。

テキスト形式で扱う場合、UTF-32は先頭に[バイト順マーク](https://ja.wikipedia.org/wiki/バイト順マーク "wikilink") (BOM) をつける。先頭の4バイトの並びが FF FE 00 00 ならリトルエンディアンとなり、00 00 FE FF ならビッグエンディアンとなる。

プログラム言語においてはUTF-32は[大文字](../Page/大文字.md "wikilink")の[U](../Page/U.md "wikilink")を利用することが多く、[C言語](../Page/C言語.md "wikilink")([C11](https://ja.wikipedia.org/wiki/C11 "wikilink"))、[C++](../Page/C++.md "wikilink")([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))などでは文字列の前に置くことでUTF-32で処理されるようになる。

## 歴史

最初の[ISO/IEC 10646規格は](https://ja.wikipedia.org/wiki/ISO/IEC_10646 "wikilink")**UCS-4**と呼ばれる[31ビット](https://ja.wikipedia.org/wiki/31ビット "wikilink")の**符号化[文字集合](../Page/文字集合.md "wikilink")**（UTF（符号化形式/符号化スキーム）ではなくUCSであることに注意）を定義していた。この形式では、UCSに含まれるおのおのの符号化された[文字は](../Page/キャラクタ_\(コンピュータ\).md "wikilink")32ビットで扱いやすい、0〜7FFFFFFFの[符号位置で表現される](https://ja.wikipedia.org/wiki/符号点 "wikilink")。

[最上位ビット](https://ja.wikipedia.org/wiki/最上位ビット "wikilink")が1になる値を避け、32ビットではなく31ビットとしたのは、これをコンピュータの内部表現として使用した場合に、最上位ビットが1のコードをエスケープなどの目的に使い、[ISO/IEC 2022などUnicodeないしISO](https://ja.wikipedia.org/wiki/ISO/IEC_2022 "wikilink") 10646と異なるコード体系のための内部表現と共用するといった便宜のためである。参考として、4バイトコードで最上位ビットが1のコードを使うものに[GB 18030がある](../Page/GB_18030.md "wikilink")。

1114112個(= 2<sup>20</sup>+2<sup>16</sup>)の符号位置を持ち、そのため十六進で10FFFFまでしか必要としないUnicode符号空間のすべてを表現するのに、UCS-4は十分である。比較的小さな符号位置の集合へのマッピングのためにそのように大きな符号空間を予約するのは浪費だと考える者がいるので、新しい符号化形式UTF-32が提案された。UTF-32はUCS-4の部分集合で、32ビットの符号値を0から10FFFFの符号空間の範囲でのみ使用する。

UTF-32は最初はUCS-4規格の部分集合だったが、[ISO/IEC JTC 1/SC 2](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1/SC_2 "wikilink")/WG 2の方針と手続きの文書は、すべての将来の文字割り当てはBMPか最初の14の[追加面](https://ja.wikipedia.org/wiki/追加面 "wikilink")に制限され、[私用面](https://ja.wikipedia.org/wiki/私用面 "wikilink")のうち、0群のE0からFF（E00000 〜 FFFFFF）の面と、60から7Fまでの群（60000000 〜 7FFFFFFF）の面は削除されたと述べている。

## 参考資料

用語の日本語表記は原則として次にならった。

## 関連項目

  - [Unicode\#エンコーディング（符号化方式）](https://ja.wikipedia.org/wiki/Unicode#エンコーディング（符号化方式） "wikilink")

## 外部リンク

  - [The Unicode Standard 4.1, chapter 3](http://www.unicode.org/versions/Unicode4.0.0/ch03.pdf) - §3.10, D43-D45にUTF-32の公式な定義
  - [Unicode Standard Annex \#19](http://www.unicode.org/reports/tr19/tr19-9.html) - Unicode 3.xにおけるUTF-32の公式な定義（2001年3月; 最終更新2002年3月）
  - [Registration of new charsets: UTF-32, UTF-32BE, UTF-32LE](http://mail.apps.ietf.org/ietf/charsets/msg01095.html) - UTF-32がIANA charset登録簿に追加されたことの告知（2002年4月）

[Category:Unicode](https://ja.wikipedia.org/wiki/Category:Unicode "wikilink") [Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink")