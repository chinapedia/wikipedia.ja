> この記事は[IBM漢字システム](https://ja.wikipedia.org/wiki/IBM漢字システム)から翻訳されています。


**IBM漢字情報処理システム**（アイビーエムかんじじょうほうしょりシステム）は[IBM](../Page/IBM.md "wikilink")[メインフレーム](../Page/メインフレーム.md "wikilink")で日本語を処理するためのシステム。初版は[1971年](https://ja.wikipedia.org/wiki/1971年 "wikilink")に発表され、その後中型機IBM [System/34](https://ja.wikipedia.org/wiki/System/34 "wikilink")や、[IBM 5550](https://ja.wikipedia.org/wiki/マルチステーション5550 "wikilink")、[DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")などに拡張された。IBM漢字コードはIBMのメインフレームで使われる[漢字コード](https://ja.wikipedia.org/wiki/漢字コード "wikilink")で、後にIBM 5550、DOS/Vでも使用された。

## 概要

IBM漢字情報処理システムは、複数回に分割して順次整備された。[1970年](../Page/1970年.md "wikilink")の[大阪万博で技術の一端が公開され](../Page/日本万国博覧会.md "wikilink")、1971年に初めて正式発表された\[1\] \[2\] \[3\]。

  - [IBM 5924](https://ja.wikipedia.org/wiki/キーパンチ#IBM_5924 "wikilink") 漢字穿孔機 ([IBM 029の大改造](https://ja.wikipedia.org/wiki/キーパンチ#IBM_029 "wikilink"))
  - [IBM 2245](../Page/IBM_2245.md "wikilink") 漢字印刷機
  - IBM [System/360](https://ja.wikipedia.org/wiki/System/360 "wikilink")-[System/370](https://ja.wikipedia.org/wiki/System/370 "wikilink") [OS/VS](https://ja.wikipedia.org/wiki/OS/VS "wikilink") & [DOS/VSE](https://ja.wikipedia.org/wiki/DOS/VSE "wikilink") プログラミング・サポート

漢字穿孔機は、左手で15シフトを操作し、右手で各シフトに対する240文字から選択して2950種の文字を[IBMカードに穿孔する](../Page/パンチカード.md "wikilink")。従来の[IBM](../Page/IBM.md "wikilink")[メインフレーム](../Page/メインフレーム.md "wikilink")は英数字と半角カタカナのみで処理されており、本システムが一万字余の日本語を処理する基礎となる。以後システムの開発が継続され、1979年9月に日本語処理の一般化\[4\]が整う。

ハードウェア

  - [オフライン](https://ja.wikipedia.org/wiki/オフライン "wikilink")入出力
      - [IBM 5924](https://ja.wikipedia.org/wiki/キーパンチ#IBM_5924 "wikilink") T01 漢字穿孔機([IBM 029](https://ja.wikipedia.org/wiki/:en:IBM_029 "wikilink") 穿孔機の12シフトキー漢字キーボード付き）
  - [オンライン](../Page/オンライン.md "wikilink")[端末](../Page/端末.md "wikilink")
      - [IBM 3270](../Page/IBM_3270.md "wikilink") [サブシステム](https://ja.wikipedia.org/wiki/サブシステム "wikilink")
          - IBM 3274 model 52C 制御装置（漢字処理機能付き）
          - IBM 3278 model 52 表示装置（12シフトキー漢字キーボード付き）
          - IBM 3273 model 52 インクジェット・プリンター
  - システム・プリンター
      - [IBM 3800](https://ja.wikipedia.org/wiki/IBM_3800 "wikilink")-2 印刷サブシステム

漢字サポート・ソフトウェア

  - [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")
      - [OS/VS](https://ja.wikipedia.org/wiki/OS/VS "wikilink")
      - [DOS/VSE](https://ja.wikipedia.org/wiki/DOS/VSE "wikilink")
      - [IBM 8100 DPPX](https://ja.wikipedia.org/wiki/:en:IBM_8100_DPPX "wikilink")
  - [プログラミング言語](../Page/プログラミング言語.md "wikilink")
      - [COBOL](../Page/COBOL.md "wikilink")
      - [PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")
  - [DBCS](https://ja.wikipedia.org/wiki/DBCS "wikilink")サポート
      - [IMS](../Page/IMS.md "wikilink")
      - [CICS](../Page/CICS.md "wikilink")
  - [ユーティリティソフトウェア](../Page/ユーティリティソフトウェア.md "wikilink")

これらはすべて標準製品で、IBM 029のみが特殊製品（[RPQ](https://ja.wikipedia.org/wiki/:en:RPQ "wikilink")）であった。

全体の計画・設計、日本語の文字コード配分、文字のデザイン、メッセージの翻訳などは主に[日本IBM](https://ja.wikipedia.org/wiki/日本IBM "wikilink")の[藤沢研究所が開発し](https://ja.wikipedia.org/wiki/IBM大和事業所 "wikilink")、米国のIBM[エンディコット研究所](https://ja.wikipedia.org/wiki/エンディコット_\(ニューヨーク州\) "wikilink")（IBM 029）、[ポケプシー研究所](https://ja.wikipedia.org/wiki/ポキプシー_\(ニューヨーク州の町\) "wikilink")（OS/VS）、[キングストン研究所](https://ja.wikipedia.org/wiki/キングストン_\(ニューヨーク州\) "wikilink")（IBM 3270、DPPX）、サンタテレザ研究所（IMS）、[英国のハーズレイ研究所](https://ja.wikipedia.org/wiki/IBMハーズレイ "wikilink")（CICS）、ドイツの[ボェブリンゲン研究所](../Page/ベーブリンゲン.md "wikilink")（DOS/VSE）など\[5\]も協力した。

のちも開発は継続され、以下が販売された。

  - [IBM 5250表示装置によるIBM](../Page/IBM_5250.md "wikilink") [System/34](https://ja.wikipedia.org/wiki/System/34 "wikilink") 漢字システム（1979年10月）
  - IBM 3273-053 漢字印刷機（1981年）
  - IBM 3200 漢字印刷機（1982年）
  - [IBM 3270](../Page/IBM_3270.md "wikilink")[エミュレーション](https://ja.wikipedia.org/wiki/エミュレーション "wikilink")・[IBM 5250エミュレーション](../Page/IBM_5250.md "wikilink")
      - [マルチステーション5550](https://ja.wikipedia.org/wiki/マルチステーション5550 "wikilink")（1984年）
      - [DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")（1991年）

## 競合

当時の日本の[メインフレーム](../Page/メインフレーム.md "wikilink")各社は日本語処理の開発で互いに競っていたが、[日本語コードの標準を作成する作業では協力していた](https://ja.wikipedia.org/wiki/文字コード#ベンダごとの文字コード "wikilink")。

  - [富士通](../Page/富士通.md "wikilink")の[JEF](https://ja.wikipedia.org/wiki/JEF漢字コード "wikilink")（Japanese processing Extended Feature）
  - [NEC](https://ja.wikipedia.org/wiki/NEC "wikilink")の[JIPS](../Page/JIPS.md "wikilink")（Japanese Information Processing System）
  - [日立](https://ja.wikipedia.org/wiki/日立 "wikilink")の[KEIS](https://ja.wikipedia.org/wiki/KEIS "wikilink")（Kanji processing Extended Information System）

## 影響

のちに[韓国語](https://ja.wikipedia.org/wiki/韓国語 "wikilink")、[中国語](https://ja.wikipedia.org/wiki/中国語 "wikilink")・[繁体字](../Page/繁体字.md "wikilink")（[台湾](https://ja.wikipedia.org/wiki/台湾 "wikilink")）、中国語・[簡体字](https://ja.wikipedia.org/wiki/簡体字 "wikilink")（[中国](../Page/中国.md "wikilink")）で、同様な言語処理システムが開発された。

## IBM漢字コード

IBM漢字コードはIBM漢字システムが使用している文字コードであり、IBM日本語文字セットと呼ばれることもある。[JISC](https://ja.wikipedia.org/wiki/JISC "wikilink")（[日本工業標準調査会](https://ja.wikipedia.org/wiki/日本工業標準調査会 "wikilink")）が[JIS C 6226](https://ja.wikipedia.org/wiki/JIS_C_6226 "wikilink"):1978を策定する前に作られており、この漢字表の1972年4月作成の版がJIS C 6226:1978の制定に当たって参考にされたとする「調査対象漢字表一覧」に含まれている\[6\]。そのため、JIS C 6226-1978と含まれる文字の種類が共通する部分が多いとはいえ異なる部分が存在しており、共通して含まれる文字についてもその並べ方は当時のメインフレームで通常使用されていた[EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink")をベースにしたものであるため全く異なっており、例えば非漢字部分の英小文字、英大文字、数字、カタカナ、ひらがなの大小関係は以下のようにそれぞれのコードで全く異なっている（比較のため[Unicode](../Page/Unicode.md "wikilink")での同様の大小関係も示す）。

  - IBM漢字コード 英小文字＜英大文字＜数字＜カタカナ＜ひらがな
  - JISコード 数字＜英大文字＜英小文字＜ひらがな＜カタカナ
  - Unicode ひらがな＜カタカナ＜数字＜英小文字＜英大文字

そのため本コードではJISの「区点」によって漢字の位置を指し示すことができず、JISコードと[シフトJIS](https://ja.wikipedia.org/wiki/シフトJIS "wikilink")コード間のコード変換のような「計算による変換」ができないため、本コードとJISコードやシフトJISコード間でのコード変換をするためには変換表（またはそれに相当する機能）が必要になる。

当初制定された後、JIS C 6226:1978の制定および同規格の改正などに伴って何度か改訂版が作られた。本コードに含まれていなかったが後に制定された[JIS X 0208に含まれている漢字については](../Page/JIS_X_0208.md "wikilink")、改訂版で拾い上げて後から追加登録されている。JIS X 0208の改定に伴って追加された文字も同様に追加されている。逆に本コードに含まれているがJIS X 0208に含まれていないものは、[ベンダ選定拡張漢字の一つとして](https://ja.wikipedia.org/wiki/拡張漢字#ベンダ選定拡張漢字 "wikilink")[マイクロソフト標準キャラクタセット](../Page/マイクロソフト標準キャラクタセット.md "wikilink")において[IBM拡張文字として取り込まれ](https://ja.wikipedia.org/wiki/Microsoftコードページ932#IBM拡張文字 "wikilink")、[外字](../Page/外字.md "wikilink")領域を使用する形でIBM製のパソコンで使用することができ、後に[Windowsを使用するパソコンで広く使用できるようになった](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。これらの文字の中には、後から[JIS X 0212](../Page/JIS_X_0212.md "wikilink")、[JIS X 0213](../Page/JIS_X_0213.md "wikilink")、[Unicode](../Page/Unicode.md "wikilink")で制定された文字もある。なお、これらの文字のいくつかは、公的規格に含まれている文字だけを入れる方針で作成されつつあったISO/IEC 10646へ[ISO/IEC JTC1/SC2の会議に](https://ja.wikipedia.org/wiki/ISO/IEC_JTC1/SC2 "wikilink")[カナダ](https://ja.wikipedia.org/wiki/カナダ "wikilink")の代表として出ていたIBMの社員が追加を提案することによって同規格に入ったため、「カナダ文字」\[7\]\[8\]または「カナダ漢字」\[9\]と呼ばれることがある。

<table>
<caption><strong>IBM漢字コードとその他のコードの対照例</strong></caption>
<thead>
<tr class="header">
<th><p>文字</p></th>
<th><p>IBM漢字<br />
コード</p></th>
<th><p>JIS<br />
コード</p></th>
<th><p>シフトJIS<br />
コード</p></th>
<th><p>拡張X0208<br />
区-点</p></th>
<th><p>X0213<br />
面-区-点</p></th>
<th><p>Unicode</p></th>
<th><p>区分</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>空白</p></td>
<td><p>64</p></td>
<td><p>2121</p></td>
<td><p>8140</p></td>
<td><p>01-01</p></td>
<td><p>1-01-01</p></td>
<td><p>U+3000</p></td>
<td><p><a href="../Page/スペース.md" title="wikilink">空白</a></p></td>
</tr>
<tr class="even">
<td><p>=</p></td>
<td><p>638</p></td>
<td><p>2161</p></td>
<td><p>8181</p></td>
<td><p>01-65</p></td>
<td><p>1-01-65</p></td>
<td><p>U+FF1D</p></td>
<td><p><a href="../Page/記号.md" title="wikilink">特殊記号</a></p></td>
</tr>
<tr class="odd">
<td><p>a</p></td>
<td><p>641</p></td>
<td><p>2361</p></td>
<td><p>8281</p></td>
<td><p>03-65</p></td>
<td><p>1-03-65</p></td>
<td><p>U+FF41</p></td>
<td><p><a href="../Page/小文字.md" title="wikilink">英小文字</a></p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p>705</p></td>
<td><p>2341</p></td>
<td><p>8260</p></td>
<td><p>03-33</p></td>
<td><p>1-03-33</p></td>
<td><p>U+FF21</p></td>
<td><p><a href="../Page/大文字.md" title="wikilink">英大文字</a></p></td>
</tr>
<tr class="odd">
<td><p>0</p></td>
<td><p>752</p></td>
<td><p>2330</p></td>
<td><p>824F</p></td>
<td><p>03-16</p></td>
<td><p>1-03-16</p></td>
<td><p>U+FF10</p></td>
<td><p><a href="../Page/数字.md" title="wikilink">数字</a></p></td>
</tr>
<tr class="even">
<td><p>ア</p></td>
<td><p>897</p></td>
<td><p>2522</p></td>
<td><p>8341</p></td>
<td><p>05-02</p></td>
<td><p>1-05-02</p></td>
<td><p>U+30A2</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/カタカナ" title="wikilink">カタカナ</a></p></td>
</tr>
<tr class="odd">
<td><p>あ</p></td>
<td><p>1153</p></td>
<td><p>2422</p></td>
<td><p>82A0</p></td>
<td><p>04-02</p></td>
<td><p>1-04-02</p></td>
<td><p>U+3042</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ひらがな" title="wikilink">ひらがな</a></p></td>
</tr>
<tr class="even">
<td><p>漢</p></td>
<td><p>3928</p></td>
<td><p>3441</p></td>
<td><p>8ABF</p></td>
<td><p>20-33</p></td>
<td><p>1-20-33</p></td>
<td><p>U+6F22</p></td>
<td><p>第一水準漢字</p></td>
</tr>
<tr class="odd">
<td><p>弌</p></td>
<td><p>5697</p></td>
<td><p>5021</p></td>
<td><p>989F</p></td>
<td><p>48-01</p></td>
<td><p>1-48-01</p></td>
<td><p>U+5F0C</p></td>
<td><p>第二水準漢字</p></td>
</tr>
<tr class="even">
<td><p>匤</p></td>
<td><p>5995</p></td>
<td><p>936B</p></td>
<td><p>FA8B</p></td>
<td><p>115-75</p></td>
<td><p>2-03-46</p></td>
<td><p>U+5324</p></td>
<td><p>IBM拡張漢字</p></td>
</tr>
<tr class="odd">
<td><p>鸙</p></td>
<td><p>10238</p></td>
<td><p>972B</p></td>
<td><p>FC4A</p></td>
<td><p>119-11</p></td>
<td><p>2-94-47</p></td>
<td><p>U+9E19</p></td>
<td><p>IBM拡張漢字</p></td>
</tr>
</tbody>
</table>

## 参考文献

  - IBM マルチステーション 5550 漢字コード一覧表, 日本アイ・ビー・エム株式会社 (1983), N:GC18-2040-1 （なお2013年現在（以降）日本IBMからの『漢字コード一覧表』の提供は終了している\[10\]）

## 脚注

## 関連項目

  - [日本IBM](https://ja.wikipedia.org/wiki/日本IBM "wikilink")
  - [文字コード](../Page/文字コード.md "wikilink")
  - [JIPS](../Page/JIPS.md "wikilink") ([NEC](https://ja.wikipedia.org/wiki/NEC "wikilink"))、[KEIS](https://ja.wikipedia.org/wiki/KEIS "wikilink") ([日立製作所](../Page/日立製作所.md "wikilink"))、[JEF](https://ja.wikipedia.org/wiki/JEF "wikilink") ([富士通](../Page/富士通.md "wikilink")}
  - IBM [マルチステーション5550](https://ja.wikipedia.org/wiki/マルチステーション5550 "wikilink")、[DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")
  - IBM [ODPS](https://ja.wikipedia.org/wiki/ODPS "wikilink") - IBM統合オフィスシステム
  - [List of IBM products](https://ja.wikipedia.org/wiki/:en:List_of_IBM_products "wikilink")
  - [IBM拡張文字](https://ja.wikipedia.org/wiki/IBM拡張文字 "wikilink")

## 外部リンク

  - [漢字コードのお話 IBMユーザ研究会](http://www.uken.or.jp/ibminfo/Systems/08.shtml)



[Category:日本語用の文字コード](https://ja.wikipedia.org/wiki/Category:日本語用の文字コード "wikilink") [Category:IBM](https://ja.wikipedia.org/wiki/Category:IBM "wikilink")

1.  諏訪秀策、「[新製品・新技術紹介 IBM漢字情報処理システム](https://doi.org/10.1241/johokanri.14.464)」 『情報管理』 1971年 14巻 7号 p.464-468, , 国立研究開発法人 科学技術振興機構
2.  安岡孝一、安岡素子「IBM漢字情報処理システム」『文字符号の歴史 欧米と日本編』共立出版、2006年2月10日、pp. 119-123。 ISBN 4-320-12102-3
3.  "IBM History of Far Eastern Languages in Computing, in 3 Parts" in IEEE Annals of the History of Computing, Volume 27 Number 1 ( January - March, 2005 )
4.  K. Hensch, Research and Development in IBM, History of Far Eastern Languages in Computing, 2nd private edition, Roehm TYPOfactory GmbH, Sindelfingen, Germany, 2004. ISBN 3-937267-03-4 (Available from Amazon.com, etc.)
5.  同上
6.  「JIS X 0208:1997 7ビットおよび8ビットの2バイト情報交換用符号化漢字集合」の解説
7.  加藤弘一「JIS拡張漢字と漢字統合の亀裂」『[図解雑学](https://ja.wikipedia.org/wiki/図解雑学シリーズ "wikilink") 文字コード』[ナツメ社](https://ja.wikipedia.org/wiki/ナツメ社 "wikilink")、2002年8月15日、p. 170。 ISBN 4-8163-3243-X
8.  「多言語情報処理の社会学 4．国家の意思と企業の意志」山崎正和・西垣通編岡田朋之ほか『文化としてのIT革命』晶文社、2000年10月。 ISBN 4-7949-6462-5
9.  樋浦秀樹「“カナダに漢字を使う少数民族が\!? Unicodeをめぐる不思議なものがたり”」『月刊ASCII』アスキー、第24巻第7号（通号第277号）、2000年7月、pp. 169-170。
10. [IBM ダイヤルIBM FAQ : 漢字コード一覧表を入手したい / 文書番号 : t0027E983](http://www-06.ibm.com/jp/domino02/services/dialqa/cicfaq.nsf/All/t0027E983)