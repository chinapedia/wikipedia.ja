> この記事は[GBK](https://ja.wikipedia.org/wiki/GBK)から翻訳されています。


**GBK** は、[中華人民共和国](../Page/中華人民共和国.md "wikilink")で使われている[簡体字](https://ja.wikipedia.org/wiki/簡体字 "wikilink")用の[文字コード](../Page/文字コード.md "wikilink") [GB 2312](../Page/GB_2312.md "wikilink") の拡張である。正式にはという。[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")12月に国家技術監督局標準化司と電子工業部科技与質量監督司が発布・実施した「技術規範指導性文件（文件＝文書）」であり、正式な規格ではない。

**GB**は**国家規格** (Guójiā Biāozhǔn, ) を、**K**が**拡張** (Kuòzhǎn, ) を表す。GBKは古い規格GB 2312に繁体字のみならず1981年にGB 2312が制定された後で簡化された漢字も拡張している。GBKの登場によって、[首相職である](https://ja.wikipedia.org/wiki/中国の首相 "wikilink")[国務院総理](../Page/国務院総理.md "wikilink")を務めた[朱鎔基](../Page/朱鎔基.md "wikilink")（）の名前に含まれる「」の文字など、かつては表現不可能だった一部の人名が表現可能になった。

## 歴史

1993年、[中国大陸](../Page/中国大陸.md "wikilink")、[台湾](https://ja.wikipedia.org/wiki/台湾 "wikilink")、[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")および[韓国で使われる](../Page/大韓民国.md "wikilink")2万0902字を含んだ[Unicode](../Page/Unicode.md "wikilink") 1.1規格が公開された。これに続き、中国はUnicode 1.1と等価な国家規格であるGB 13000.1-93を公開した。

GBKの文字集合は 1993年に[GB 2312](../Page/GB_2312.md "wikilink")-80の拡張として定義されたが、GB 2312で未使用のコードポイントを利用してGB 13000.1-93の文字も含んでいた。このためGBKはGB 2312に対して上位互換である。

[MicrosoftはGBKを](../Page/マイクロソフト.md "wikilink")[Windows 95でコードページ](../Page/Microsoft_Windows_95.md "wikilink")936として定義した。GBKが公式規格になったことは一度もないが、Windows 95が広く使われるようになったことによりGBKは[事実上の標準となった](../Page/デファクトスタンダード.md "wikilink")。GBKはUnicode 1.1およびGB 13000.1-93で定義されている全ての漢字を含んでいたが、それらとは異なる符号表を使っていた。GBKの基本的な存在意義は、単にGB 2312-80とGB 13000.1-93の落差の橋渡しであった。

[2000年](../Page/2000年.md "wikilink")、[GB 18030](../Page/GB_18030.md "wikilink")-2000規格が公開されてGBKを置き替えたが、まだ互換性は保たれている。GB 18030は定義されている漢字の数を増やし、4バイト文字空間の実装によって使用可能な文字数を拡張した。

## 符号化方式

文字は1バイトか2バイトで符号化される。`00`–`7F`の範囲にあるバイトは1バイトで、[ASCII](../Page/ASCII.md "wikilink") にあるものと同じ意味を持つ。厳密に言うと、96 の文字と32の制御符号がこの範囲にある。

上位ビットが立てられたバイトは2バイト文字の第1バイトであることを示す。おおざっぱに言うと、第1バイトの範囲は`81`–`FE`であり（すなわち、`80`と`FF`は含まず）、第2バイトは一部の領域は`40`–`FE`に、他の領域が`80`–`FE`にある。

より具体的には、以下の範囲のバイトが定義されている:

| 範囲       | 第1バイト     | 第2バイト               | コードポイント | 文字     |
| -------- | --------- | ------------------- | ------- | ------ |
| 水準 GBK/1 | `A1`–`A9` | `A1`–`FE`           | 846     | 717    |
| 水準 GBK/2 | `B0`–`F7` | `A1`–`FE`           | 6,768   | 6,763  |
| 水準 GBK/3 | `81`–`A0` | `40`–`FE` (`7F`を除く) | 6,080   | 6,080  |
| 水準 GBK/4 | `AA`–`FE` | `40`–`A0` (`7F`を除く) | 8,160   | 8,160  |
| 水準 GBK/5 | `A8`–`A9` | `40`–`A0` (`7F`を除く) | 192     | 166    |
| 利用者定義    | `AA`–`AF` | `A1`–`FE`           | 564     |        |
| 利用者定義    | `F8`–`FE` | `A1`–`FE`           | 658     |        |
| 利用者定義    | `A1`–`A7` | `40`–`A0` (`7F`を除く) | 672     |        |
| 合計:      |           |                     | 23,940  | 21,886 |

GBKの文字符号化範囲

2バイト符号で表現可能な64K空間すべてを以下の図に示す。緑と黄色の領域がGBKに割り当てられたコードポイントであり、赤が利用者定義文字用である。色付きでない領域は不正なバイトの組み合わせである。 [thumb](https://ja.wikipedia.org/wiki/ファイル:GBK_encoding_ja.svg "wikilink")

## 他の文字コードとの関係

前節にGBK/1およびGBK/2として示された領域は、単にGB 2312-80を通常の方法で符号化したものである。GB 2312（より正確にはそのEUC-CNによる符号化）は、[ISO/IEC 2022](https://ja.wikipedia.org/wiki/ISO/IEC_2022 "wikilink") でGRに呼び出された他のあらゆる94²文字集合と同様、`A1`–`FE` の範囲からバイトの対を取る。これは上図において右下の区画に相当する。しかし、GB 2312は`AA`–`AF`と`F8`–`FE` にある区には手を付けず、いかなるコードポイントも割り当てていない。

GBKはこの領域に拡張を追加した。この二者の違う部分は利用者定義領域によって埋められている。

より重要なこととして、GBKはバイトの範囲を拡張した。ISO/IEC 2022 のGR領域に持てる文字の数には94² = 8,836字の制限がある。[図形文字](https://ja.wikipedia.org/wiki/図形文字 "wikilink")用と制御文字用に厳格な範囲を与えるという ISO/IEC 2022 のモデルは放棄するが、下位バイトは1バイト文字であり上位バイトの対が文字を示すという機能を残すことにより、潜在的に128² = 16,384の符号位置を使えるようになった。GBKはその一部を採用し、範囲を`A1`–`FE` （バイトごとに94の選択肢がある）から、第1バイトは `81`–`FE` （126 の選択肢）へ、第2バイトは `40`–`FE` （191 の選択肢） へ拡張した。

マイクロソフトのコードページ936は通常GBKであると考えられている。GBKと同じ範囲のバイトを使い、比較してみても同じ割り当てがなされているように見える。コードページ936は、GBKに収録されている 2万1886 字のうち95字をUnicodeの私用領域に割り当てている\[1\]\[2\]。これらはGBKが制定された時点でUnicodeに収録されていなかった文字である。

GBKの後継であるGB 18030-2000は、第2バイトとして使用可能な残りの範囲を使って、さらに使用可能なコードポイントの数を拡張しているが、GBKを部分集合として残している。

## 脚注

## 外部リンク

  - [MicrosoftのGBK用の参照ページ](http://www.microsoft.com/globaldev/reference/dbcs/936.mspx)
  - [GBKからUnicodeへのマッピング](http://www.unicode.org/Public/MAPPINGS/VENDORS/MICSFT/WINDOWS/CP936.TXT) 注意: Microsoft typographyの表に含まれていた私用領域との対応は含まれていない。
  - [GBK符号表](http://www.khngai.com/chinese/charmap/tblgbk.php?page=0) 注意: これは使用可能な符号空間を、2カ所を除きすべて示しているため合計は3万2256グリフになり（3万2352 と、図に示されていない暗黙の1バイトASCII符号）、2万3940 や 2万1886 より多い。
  - [GBKとGB 2312からGB 18030への進化](http://web.archive.org/web/20120825155118/http://developers.sun.com/dev/gadc/technicalpublications/articles/gb18030.html)（2012年8月25日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")）
  - [GBK(5)](http://h30097.www3.hp.com/docs/base_doc/DOCUMENTATION/V51_HTML/MAN/MAN5/0020____.HTM) [HP](../Page/ヒューレット・パッカード.md "wikilink") 社の[manページ](https://ja.wikipedia.org/wiki/manページ "wikilink")に、文字範囲に関する優れた説明がある。

[Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink") [Category:中国の規格](https://ja.wikipedia.org/wiki/Category:中国の規格 "wikilink") [Category:中国語](https://ja.wikipedia.org/wiki/Category:中国語 "wikilink")

1.
2.  \-[Microsoft typography](http://www.microsoft.com/typography/default.mspx)の[Character sets and codepages](http://www.microsoft.com/typography/unicode/cscp.htm)にかつて存在したGBKとUnicodeの間の変換表。