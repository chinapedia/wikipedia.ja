> この記事は[TRON](https://ja.wikipedia.org/wiki/TRON)から翻訳されています。


**TRONコード**（トロンコード）とは、[TRONプロジェクト](../Page/TRONプロジェクト.md "wikilink")で使用されている[文字コード](../Page/文字コード.md "wikilink")である。TRON多国語言語環境の初期論文は[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")に発表され（「TAD言語環境と多国語対応」）、以来主に[BTRON](../Page/BTRON.md "wikilink")で利用されてきた。

## 特徴

単体で「TRONコード」という文字コードがあるわけではなく、TAD（TRON Application Databus）という、TRONの実身/仮身モデルをサポートするデータフォーマットの一部である\[1\]。[GTプロジェクトのように](../Page/GT書体.md "wikilink")、TRONプロジェクトで独自に文字の蒐集をおこない[文字集合](../Page/文字集合.md "wikilink")も作成しているが、TRONコードは基本的に、既存の文字集合をそのまま取り込むフレームワークとして設計されている。

特に漢字について、[Unicode](../Page/Unicode.md "wikilink")の[CJK統合漢字](../Page/CJK統合漢字.md "wikilink")のHan unification（[w:Han unification](https://ja.wikipedia.org/wiki/w:Han_unification "wikilink")）のように統合を行ったりせず、JISの各漢字の他[GB 2312や](../Page/GB_2312.md "wikilink")[KS X 1001や](../Page/KS_X_1001.md "wikilink")[CNS 11643を](https://ja.wikipedia.org/wiki/CNS_11643 "wikilink")、そのまま空間として割り当てていることが特徴である。

変わったところでは[トンパ文字](../Page/トンパ文字.md "wikilink")や[SF作品中の架空文字である](https://ja.wikipedia.org/wiki/サイエンス・フィクション "wikilink")[アーヴ文字などもコードを割り当てられている](../Page/アース_\(文字\).md "wikilink")。

## 仕様

### コード体系

TRONコードは、2バイト単位をベースとしている。0000～FFFFの空間を4個のゾーンに分け（詳細は後述）、1面あたり48,400の[符号点](https://ja.wikipedia.org/wiki/符号点 "wikilink")がある。任意長に拡張可能なエスケープシーケンスにより、面を切り替えることができるので、規格上はいくらでも文字を割り当てられる。以下にTRONコードの構成を示す。

<table>
<thead>
<tr class="header">
<th></th>
<th><p>第1バイト</p></th>
<th><p>第2バイト</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>制御コード</p></td>
<td><p>0x00</p></td>
<td><p>0x00 - 0xFE</p></td>
</tr>
<tr class="even">
<td><p>文字コード</p></td>
<td><p>0x21 - 0x7E<br />
0x80 - 0xFD</p></td>
<td><p>0x21 - 0x7E<br />
0x80 - 0xFD</p></td>
</tr>
<tr class="odd">
<td><p>言語切り替え</p></td>
<td><p>0xFE</p></td>
<td><p>0x21 - 0x7E<br />
0x80 - 0xFE</p></td>
</tr>
<tr class="even">
<td><p>特殊コード</p></td>
<td><p>0xFF</p></td>
<td><p>0x21 - 0xFE</p></td>
</tr>
<tr class="odd">
<td><p>エスケープ</p></td>
<td><p>0xFF</p></td>
<td><p>0x80 - 0xFE</p></td>
</tr>
<tr class="even">
<td><p>EOF</p></td>
<td><p>0xFF</p></td>
<td><p>0xFF</p></td>
</tr>
</tbody>
</table>

なお、[ISO/IEC 646など](https://ja.wikipedia.org/wiki/ISO/IEC_646 "wikilink")、8ビット系コードとの互換は、「TRON1バイト文字コード」\[2\]「Eゾーン」\[3\]などとして一部の資料に言及が見られるが、制御コード以外は実装されていない。

### 詳細

Aゾーンは2121 - 7E7E、Bゾーンは8021 - FD7E、Cゾーンは2180 - 7EFD、Dゾーンは8080 - FDFDである。

**[TRONコード第2面2100 - 21FF番の表](../Page/TRONコード一覧_2-2100_-_2-21FF.md "wikilink")**を参照されたい。この領域は[GT書体](../Page/GT書体.md "wikilink")が収録されている。2100から2120までは制御などに掛かる未使用領域であり、実際の文字領域は2121から開始される。217Fは未使用であるが、続く2180からの収録文字はそれまでの系列の文字とは異なる。2121から217Eまでは「」の部に関連した「[16px](https://ja.wikipedia.org/wiki/ファイル:TRON_2-246B.gif "wikilink")（[16px](https://ja.wikipedia.org/wiki/ファイル:TRON_2-2464.gif "wikilink")）」を含む文字群が収録されている。一方、2180からは「[16px](https://ja.wikipedia.org/wiki/ファイル:TRON_2-FC6F.gif "wikilink")」を部首とする文字群の領域である。

ほかの文字コードではこうした配列になることは少ないが、ゾーンという概念を持つTRONコードでは第1バイトが同じであっても連続するコードの中で分断されるという現象が生じる。なお、上記の例ではAゾーンとCゾーンの隣接によるものであり、第2面217E番の「[16px](https://ja.wikipedia.org/wiki/ファイル:TRON_2-217E.gif "wikilink")」に続く文字は第2面2221番「[16px](https://ja.wikipedia.org/wiki/ファイル:TRON_2-2221.gif "wikilink")」から再び続行される。**[TRONコード第2面2200 - 22FF番の表](../Page/TRONコード一覧_2-2200_-_2-22FF.md "wikilink")**を参照。

### スクリプト構成

上記の通り、標準では31面150万文字の登録が可能であるが、2006年10月27日時点で割り当てられているのは、9面18万文字である。各スクリプトの構成は以下の通りである。

| 面番号       | 構成                                                                                                                                                                                                                                                                        |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 第1面       | JIS [X0208](../Page/JIS_X_0208.md "wikilink")、[X0213](../Page/JIS_X_0213.md "wikilink")、[X0212](../Page/JIS_X_0212.md "wikilink")、[GB 2312](../Page/GB_2312.md "wikilink")、[KS X 1001](../Page/KS_X_1001.md "wikilink")、[点字](https://ja.wikipedia.org/wiki/点字 "wikilink") |
| 第2 - 3面   | [GT書体](../Page/GT書体.md "wikilink")                                                                                                                                                                                                                                        |
| 第4 - 5面   | 予約                                                                                                                                                                                                                                                                        |
| 第6面       | [Big5](../Page/Big5.md "wikilink")                                                                                                                                                                                                                                        |
| 第7面       | 予約                                                                                                                                                                                                                                                                        |
| 第8面       | 大漢和辞典収録文字                                                                                                                                                                                                                                                                 |
| 第9面       | 大漢和辞典収録文字、記号類                                                                                                                                                                                                                                                             |
| 第10面      | 中国伝承文字、少数民族文字等                                                                                                                                                                                                                                                            |
| 第11 - 15面 | 欠番                                                                                                                                                                                                                                                                        |
| 第16 - 17面 | Unicode(漢字及び[ハングル](https://ja.wikipedia.org/wiki/ハングル "wikilink")は含まない)                                                                                                                                                                                                   |
| 第18 - 21面 | 予約                                                                                                                                                                                                                                                                        |
| 第22 - 23面 | 中国拡張文字[GB18030](https://ja.wikipedia.org/wiki/GB18030 "wikilink")                                                                                                                                                                                                         |
| 第24 - 31面 | 予約                                                                                                                                                                                                                                                                        |

### 収録文字種

上述の通り、スクリプトとしては9面が現状定義されているが、各スクリプトの内部に複数の文字種が混在して収められている。このため、TRONコードに登録された文字種は9種より多く39種を数える。以下に、TRONコードに収録済の文字種を示す。

<table>
<thead>
<tr class="header">
<th><p>文字種</p></th>
<th><p><a href="../Page/文字集合.md" title="wikilink">文字集合</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JIS第一・第二水準・第三・<br />
第四水準・補助漢字</p></td>
<td><p>JIS <a href="../Page/JIS_X_0208.md" title="wikilink">X 0208</a> <a href="../Page/JIS_X_0213.md" title="wikilink">X 0213</a> <a href="../Page/JIS_X_0212.md" title="wikilink">X 0212</a></p></td>
</tr>
<tr class="even">
<td><p>韓国語(漢字,ハングル)</p></td>
<td><p><a href="../Page/KS_X_1001.md" title="wikilink">KS X 1001</a></p></td>
</tr>
<tr class="odd">
<td><p>中国語(簡体字)</p></td>
<td><p><a href="../Page/GB_2312.md" title="wikilink">GB 2312</a></p></td>
</tr>
<tr class="even">
<td><p>中国語(伝統字,繁体字)</p></td>
<td><p><a href="../Page/Big5.md" title="wikilink">Big5</a></p></td>
</tr>
<tr class="odd">
<td><p>中国語(拡張文字)</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/GB18030" title="wikilink">GB18030</a></p></td>
</tr>
<tr class="even">
<td><p>六点点字</p></td>
<td><p>Unicode 3.0</p></td>
</tr>
<tr class="odd">
<td><p>八点点字</p></td>
<td><p>Unicode 3.0</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/iモード絵文字" title="wikilink">iモード絵文字</a></p></td>
<td><p>Unicode 6.0 (企業のロゴマーク等を除く)</p></td>
</tr>
<tr class="odd">
<td><p>ホツマ文字</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>陰陽五行文字</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/GT書体.md" title="wikilink">GT書体</a>フォント</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/大漢和辞典.md" title="wikilink">大漢和辞典</a>収録文字</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/トンパ文字.md" title="wikilink">トンパ文字</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>記号</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="odd">
<td><p>数学･技術記号</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="even">
<td><p>通貨記号</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="odd">
<td><p>IPA発音記号</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="even">
<td><p>句読点類</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="odd">
<td><p>ラテン</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="even">
<td><p>ギリシャ</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="odd">
<td><p>キリル</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="even">
<td><p>アルメニア</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="odd">
<td><p>ヘブライ</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="even">
<td><p>アラビア</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="odd">
<td><p>デーヴァナーガリ</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="even">
<td><p>ベンガル</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="odd">
<td><p>グルムキー</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="even">
<td><p>グジャラティ</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="odd">
<td><p>オリヤ</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="even">
<td><p>タミール</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="odd">
<td><p>テルグ</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="even">
<td><p>カンナダ</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="odd">
<td><p>マラヤーラム</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="even">
<td><p>タイ</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="odd">
<td><p>ラオス</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="even">
<td><p>チベット</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="odd">
<td><p>グルジア</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="even">
<td><p>かな･漢文記号</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="odd">
<td><p>CJK用共通記号</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/ハングル" title="wikilink">ハングル</a>字母等</p></td>
<td><p>Unicode 2.0</p></td>
</tr>
</tbody>
</table>

### 多言語と多文字

以上の仕様により、多様な文字種を含む文章をデータにできる。しかし、表示にはまた別の問題が存在する。

文字の綴り方は言語によって異なり、[漢字文化圏](../Page/漢字文化圏.md "wikilink")より複雑な規則を持つ言語も多い。BTRONでは、言語層・スクリプト層・文字属層・フォント層というレイヤを想定しているが、現状では実装されていない。このため実装では、インド系の文字の結合処理・[アラビア語](../Page/アラビア語.md "wikilink")や[ヘブライ語](../Page/ヘブライ語.md "wikilink")の右から左への記述順など、いずれもまともに可視化できない。[トンパ文字](../Page/トンパ文字.md "wikilink")が実装されているものの、ため、必ずしもトンパを綴れると言える環境でもない。こうした指摘もあることから、TRONコードは多言語ではなく多文字に過ぎないと評する向きもある。

## 歴史

コード体系に示した通り、TRONコード自体は当初から多くの文字コードを扱える様設計されていたが、[1999年](../Page/1999年.md "wikilink")に[超漢字](../Page/超漢字.md "wikilink")が発売されるまでは、第1面のみが使用される状況が続いた。これを「**とりあえず多言語**」と呼び、第1面には「**とりあえず多言語面**」という別名が付けられた。多言語とはいうものの漢字文化圏である3か国の文字セットを纏めたものではあり、前述のように日本の文字セットである[JIS X 0212](../Page/JIS_X_0212.md "wikilink")、中国の[GB 2312](../Page/GB_2312.md "wikilink")、韓国の[KS X 1001](../Page/KS_X_1001.md "wikilink")、および[点字](https://ja.wikipedia.org/wiki/点字 "wikilink")が含まれる。

なお「TAD言語環境と多国語対応」では「言語指定コード」というもので言語を切り替える、という構想が示されているが、現状で使用されている切り替えコードは言語指定コードではなく「スクリプト切り替えコード」だとされている（「TRONの多国語言語環境の仕様」, 『TRONWARE』Vol. 50, p. 47）。

[超漢字](../Page/超漢字.md "wikilink")では、[Big5](../Page/Big5.md "wikilink")や[今昔文字鏡](../Page/今昔文字鏡.md "wikilink")が収録され、一気に収録文字数が増えた。その後、TRON文字収録センタが発足し、[トンパ文字](../Page/トンパ文字.md "wikilink")や[アーヴ文字等の文字種までが収められるまでになったが](../Page/アース_\(文字\).md "wikilink")、一方で[GT書体](../Page/GT書体.md "wikilink")との絡み及びライセンスの問題が表面化し、[今昔文字鏡](../Page/今昔文字鏡.md "wikilink")がTRONコードから削除される事態を招いた（第11 - 第15面までの5面が欠番として空けられているのはこの影響である）。パーソナルメディアは超漢字3において、文字鏡研究会により今昔文字鏡フォントの使用許諾契約書が改訂され今昔文字鏡文字の文字コード変換が制限され、またエーアイ・ネットから今昔文字鏡フォントの配布ライセンスが得られず独自の互換変換表の作成も承諾されなかったとしている\[4\]。

## 関連項目

  - [TRONプロジェクト](../Page/TRONプロジェクト.md "wikilink")
  - [超漢字](../Page/超漢字.md "wikilink")
  - [今昔文字鏡](../Page/今昔文字鏡.md "wikilink")
  - [大漢和辞典](../Page/大漢和辞典.md "wikilink")
  - [GT書体](../Page/GT書体.md "wikilink")
  - [住民基本台帳収録変体仮名](../Page/住民基本台帳収録変体仮名.md "wikilink")
  - [おとど](../Page/たいと.md "wikilink")（[24px](https://ja.wikipedia.org/wiki/画像:Taito_s.png "wikilink")）
  - [TRONコード一覧 2-2100 - 2-21FF](../Page/TRONコード一覧_2-2100_-_2-21FF.md "wikilink")
  - [TRONコード一覧 2-2200 - 2-22FF](../Page/TRONコード一覧_2-2200_-_2-22FF.md "wikilink")
  - [TRONコード一覧 2-2300 - 2-23FF](../Page/TRONコード一覧_2-2300_-_2-23FF.md "wikilink")
  - [TRONコード一覧 2-2400 - 2-24FF](../Page/TRONコード一覧_2-2400_-_2-24FF.md "wikilink")

## 出典

## 外部リンク

  - [BTRON3仕様書](http://www.chokanji.com/developer/doc/btron3/index.html)
  - [TRON文字収録センター](http://charcenter.t-engine.org/)
  - [超漢字](http://www.chokanji.com/)
  - [GT明朝](http://www.l.u-tokyo.ac.jp/KanjiWEB/00_cover.html)
  - [今昔文字鏡](http://www.mojikyo.gr.jp/)

[Category:TRONコード](https://ja.wikipedia.org/wiki/Category:TRONコード "wikilink") [Category:Unicodeに存在しない文字](https://ja.wikipedia.org/wiki/Category:Unicodeに存在しない文字 "wikilink")

1.  <http://www.chokanji.com/developer/doc/btron3/shared_data/index.html>
2.  『TRONプロジェクト '87-'88』p. 143
3.  『TRONWARE』Vol. 36, p. 13
4.  [超漢字３と今昔文字鏡文字に関するご質問](http://www.chokanji.com/support/ck4/ck3ans/konjyaku.html)