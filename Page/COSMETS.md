> この記事は[COSMETS](https://ja.wikipedia.org/wiki/COSMETS)から翻訳されています。


**COSMETS**（コスメッツ、Computer System for Meteorological Services）とは、[気象庁](../Page/気象庁.md "wikilink")の気象資料総合システム（気象観測データを解析し、予測するシステム）のこと。ADESS（気象資料自動編集中継装置:Automated Data Editing and Switching System の略）とNAPS（数値解析予報システム:Numerical Analysis and Prediction System の略）部分に分かれる。もともとはADESS部分と、数値演算予報部分とで個別に扱われていたが、1980年代に統合して呼ばれるようになった。

## 沿革

  - [1959年](../Page/1959年.md "wikilink")6月 - 数値解析予報システム (NAPS) を運用開始\[1\]
  - [1967年](../Page/1967年.md "wikilink") - 第2世代数値解析予報システム (NAPS2) を運用開始\[2\]
  - [1973年](../Page/1973年.md "wikilink") - 第3世代数値解析予報システム (NAPS3) を運用開始\[3\]
  - [1982年](../Page/1982年.md "wikilink") - 第4世代数値解析予報システム (NAPS4) を運用開始\[4\]
  - [1967年](../Page/1967年.md "wikilink") - 第5世代数値解析予報システム (NAPS5) を運用開始\[5\]
  - [1996年](../Page/1996年.md "wikilink") - 第6世代数値解析予報システム (NAPS6) を運用開始\[6\]
  - [2001年](../Page/2001年.md "wikilink")[3月1日](../Page/3月1日.md "wikilink") - 第7世代数値解析予報システム (NAPS7) を運用開始\[7\]
  - [2006年](../Page/2006年.md "wikilink")[3月1日](../Page/3月1日.md "wikilink") - 第8世代数値解析予報システム (NAPS8) を運用開始\[8\]
  - [2012年](../Page/2012年.md "wikilink")[6月5日](https://ja.wikipedia.org/wiki/6月5日 "wikilink") - 第9世代数値解析予報システム (NAPS9) を運用開始\[9\]
  - [2018年](../Page/2018年.md "wikilink")[6月5日](https://ja.wikipedia.org/wiki/6月5日 "wikilink") - 第10世代数値解析予報システム (NAPS10) を運用開始\[10\]

## 経緯

### ADESSの経緯

当初、[東芝](../Page/東芝.md "wikilink")のメインフレームを利用していたが、その後、東芝のメインフレーム撤退に伴い、[日本電気](../Page/日本電気.md "wikilink")に移管された。日本電気移管後は、同社製のメインフレーム（[ACOS-6](../Page/ACOS-6.md "wikilink")シリーズ（C-ADESS V まで）→ACOS-4シリーズ）とミニコンピュータ（MSシリーズ）、その後はUNIXサーバ ([UP4800](../Page/UP4800.md "wikilink"), [UX/4800](https://ja.wikipedia.org/wiki/UX/4800 "wikilink")) を使用し、リアルタイムクラスでのサービスデーモンの運用など、SVR4.2MPの機能を活用した機能を提供していた。 ADESSにおいて、COSMETSの一部となる部分はC-ADESSと呼ばれ、日本全国の集配信および、国際通信系(GTS)の中心となっていた。 そのほかに各管区気象台が対応する部分としてL-ADESSがあった（これはCOSMETSの一部ではない）。

2005年の更新では、C-ADESSとL-ADESSを一本化し、東西2つのシステムとし、再構成している。西日本部分については、2008年3月に稼働した。 また、提供ベンダもNECから富士通に切り替え、汎用機を廃してUNIXサーバとPCサーバによるシステムに変更された。

### NAPSの経緯

当初はM-200Hのようなメインフレームで構成されていたが、その後スーパーコンピュータに置き換えられた。[1988年](../Page/1988年.md "wikilink")に[日立製作所](../Page/日立製作所.md "wikilink")のSRシリーズを使用して構築、その後SRシリーズで更新されている。1992年に更新する際、システムの電力容量が気象庁本庁舎で耐えられない電力容量を要する結果になったことから、COSMETSのコアシステムは、清瀬にある気象衛星センター内に移設、以後コアシステムは、清瀬で運用されている。 [2001年](../Page/2001年.md "wikilink")にNAPS部分は、当時の最新SRシリーズ機SR8000（理論ピーク性能：768G[FLOPS](../Page/FLOPS.md "wikilink")）が稼動し、気象予測の予測範囲時間が3時間から6時間と倍増した。

当時、数値演算部分の演算性能では世界3指に入るシステムと広報されたが、当時の他国（カナダ/アメリカなど）システムは更改期を目前としたもので、比較する意味の無い値であった。

さらに、近年の気象予測の予測精度への不満により、早々の置き換えを切望されていたが、[2006年](../Page/2006年.md "wikilink")3月1日にやっと旧SR8000がSR11000と置き換えられ、理論ピーク性能21.5TFLOPSと大幅に性能向上した。さらに、[2012年](../Page/2012年.md "wikilink")にはSR16000/M1に、[2018年](../Page/2018年.md "wikilink")にはCray XC50を主系とするシステムに置き換えられた。

<table>
<caption>NAPS 各世代の諸元[11]</caption>
<thead>
<tr class="header">
<th><p>世代</p></th>
<th><p>運用開始</p></th>
<th><p>受注者</p></th>
<th><p>機種</p></th>
<th><p>理論最大性能</p></th>
<th><p>主記憶容量</p></th>
<th><p>ディスク容量</p></th>
<th><p>消費電力</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>NAPS</p></td>
<td><p>1959年</p></td>
<td><p>IBM</p></td>
<td><p>IBM 704</p></td>
<td><p>12 キロ<a href="../Page/FLOPS.md" title="wikilink">FLOPS</a></p></td>
<td><p>―</p></td>
<td><p>―</p></td>
<td><p>―</p></td>
</tr>
<tr class="even">
<td><p>NAPS2</p></td>
<td><p>1967年</p></td>
<td><p>日立製作所</p></td>
<td><p>Hitachi HITAC 5020</p></td>
<td><p>307 キロFLOPS</p></td>
<td><p>―</p></td>
<td><p>―</p></td>
<td><p>―</p></td>
</tr>
<tr class="odd">
<td><p>NAPS3</p></td>
<td><p>1973年</p></td>
<td><p>日立製作所</p></td>
<td><p>Hitachi HITAC 8800</p></td>
<td><p>4.55 メガFLOPS</p></td>
<td><p>―</p></td>
<td><p>―</p></td>
<td><p>―</p></td>
</tr>
<tr class="even">
<td><p>NAPS4</p></td>
<td><p>1982年</p></td>
<td><p>日立製作所</p></td>
<td><p>Hitachi HITAC M-200H</p></td>
<td><p>23.8 メガFLOPS</p></td>
<td><p>―</p></td>
<td><p>―</p></td>
<td><p>―</p></td>
</tr>
<tr class="odd">
<td><p>NAPS5</p></td>
<td><p>1987年</p></td>
<td><p>日立製作所</p></td>
<td><p>Hitachi HITAC S-810</p></td>
<td><p>630 メガFLOPS</p></td>
<td><p>―</p></td>
<td><p>―</p></td>
<td><p>―</p></td>
</tr>
<tr class="even">
<td><p>NAPS6</p></td>
<td><p>1996年</p></td>
<td><p>日立製作所</p></td>
<td><p>Hitachi S-3800</p></td>
<td><p>32 ギガFLOPS</p></td>
<td><p>―</p></td>
<td><p>―</p></td>
<td><p>―</p></td>
</tr>
<tr class="odd">
<td><p>NAPS7</p></td>
<td><p>2001年3月</p></td>
<td><p>日立製作所</p></td>
<td><p>Hitachi SR8000/E1 (80ノード)</p></td>
<td><p>768 ギガFLOPS</p></td>
<td><p>640 ギガ<a href="../Page/バイト_(情報).md" title="wikilink">バイト</a></p></td>
<td><p>2.7 テラバイト</p></td>
<td><p>―</p></td>
</tr>
<tr class="even">
<td><p>NAPS8</p></td>
<td><p>2006年3月</p></td>
<td><p>日立製作所</p></td>
<td><p>Hitachi SR11000/K1 (80ノード×2) (数値予報)</p></td>
<td><p>21.5 テラFLOPS<br />
(10.75 テラFLOPS×2)</p></td>
<td><p>10 テラバイト<br />
(5 テラバイト×2)</p></td>
<td><p>18.6 テラバイト</p></td>
<td><p>―</p></td>
</tr>
<tr class="odd">
<td><p>2005年3月</p></td>
<td><p>Hitachi SR11000/J1 (50ノード) (衛星データ処理)</p></td>
<td><p>6.08 テラFLOPS</p></td>
<td><p>3.1 テラバイト</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>NAPS9</p></td>
<td><p>2012年6月</p></td>
<td><p>日立製作所</p></td>
<td><p>Hitachi SR16000/M1</p></td>
<td><p>847 テラFLOPS</p></td>
<td><p>108 テラバイト</p></td>
<td><p>348 テラバイト</p></td>
<td><p>1,969 kVA</p></td>
</tr>
<tr class="odd">
<td><p>NAPS10</p></td>
<td><p>2018年6月</p></td>
<td><p>日立製作所</p></td>
<td><p>Cray XC50</p></td>
<td><p>18 ペタFLOPS<br />
(18,166 テラFLOPS)</p></td>
<td><p>528 テラバイト</p></td>
<td><p>10.6 ペタバイト<br />
(10,608 テラバイト)</p></td>
<td><p>4,107 kVA</p></td>
</tr>
</tbody>
</table>

## 脚注

## 関連項目

  - [数値予報](../Page/数値予報.md "wikilink")

[Category:気象事業](https://ja.wikipedia.org/wiki/Category:気象事業 "wikilink") [Category:情報システム](https://ja.wikipedia.org/wiki/Category:情報システム "wikilink") [Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink") [Category:計算科学](https://ja.wikipedia.org/wiki/Category:計算科学 "wikilink")

1.  [「気象予測」を支える 日立グループのスーパーコンピュータ技術](http://www.hitachihyoron.com/jp/pdf/2009/12/2009_12_04.pdf) 日立評論 2009年12月号
2.
3.
4.
5.
6.
7.  [最新鋭スーパーコンピュータの導入について](http://www.jma.go.jp/jma/press/0011/22a/mate.pdf)、気象庁
8.  [スーパーコンピュータの更新及び数値予報等の改善について](http://www.jma.go.jp/jma/press/0602/23a/suchiyohokaizen.html)、気象庁
9.  [新しいスーパーコンピュータシステムの運用開始について](http://www.jma.go.jp/jma/press/1205/24c/20120524_naps_renewal.html)、気象庁
10. [新しいスーパーコンピュータの運用を開始します](http://www.jma.go.jp/jma/press/1805/16b/20180516_hpc_renewal.html)、気象庁
11.