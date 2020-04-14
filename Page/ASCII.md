> この記事は[ASCII](https://ja.wikipedia.org/wiki/ASCII)から翻訳されています。


（アスキー、）は、現代[英語](../Page/英語.md "wikilink")や[西ヨーロッパ言語](https://ja.wikipedia.org/wiki/西ヨーロッパ言語 "wikilink")で使われる[ラテン文字](../Page/ラテン文字.md "wikilink")を中心とした[文字コード](../Page/文字コード.md "wikilink")。これは[コンピュータ](../Page/コンピュータ.md "wikilink")その他の通信機器において最もよく使われているものである。

## 概要

は、7桁の[2進数](https://ja.wikipedia.org/wiki/2進数 "wikilink")で表すことのできる[整数](../Page/整数.md "wikilink")の数値のそれぞれに、大小の[ラテン文字](../Page/ラテン文字.md "wikilink")や[数字](../Page/数字.md "wikilink")、英文でよく使われる[約物](../Page/約物.md "wikilink")などを割り当てた[文字コード](../Page/文字コード.md "wikilink")である。[1963年](../Page/1963年.md "wikilink")[6月17日](../Page/6月17日.md "wikilink")に、（ASA、後の）によって制定された。当時の規格番号は ASA X3.4 、現在の規格番号は  である。

は[ISO標準](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")7[ビット](../Page/ビット.md "wikilink")文字コード[ISO/IEC 646の元となり](https://ja.wikipedia.org/wiki/ISO/IEC_646 "wikilink")、後に8ビット文字コードである[ISO/IEC 8859が主流となって以降](https://ja.wikipedia.org/wiki/ISO/IEC_8859 "wikilink")、世界中で使用されている様々な文字の[符号化方式](../Page/符号化方式.md "wikilink")の多くは、で使用されていない128番以降の部分に、その他の文字を割り当てたものである。

他の文字コードと同じく、は[整数](../Page/整数.md "wikilink")で表されるデジタルデータと[文字集合](../Page/文字集合.md "wikilink")とが対応づけられた[コードである](../Page/符号.md "wikilink")。このコードに従い、文字等を整数に変換することで、通信、文字情報の処理や保存を行うのが容易になる。や互換コードは、ほとんど全ての[コンピュータ](../Page/コンピュータ.md "wikilink")（特に[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")や[ワークステーション](../Page/ワークステーション.md "wikilink")）で扱うことができる。では、「`US-ASCII`」とするのが望ましい。

は7ビットコードである。つまり、情報を表すのに7桁の2進数（10進数では0〜127）を用いる。が規格化された頃ですら、ほとんどのコンピュータの扱う最少単位の[バイトは](../Page/バイト_\(情報\).md "wikilink")8ビットである[オクテットであった](../Page/8ビット.md "wikilink")。そのため8ビット目は通信におけるエラーチェック用の[パリティ](../Page/パリティ.md "wikilink")ビットとして用いられていた。21世紀初頭においても、互換性を維持する目的で、7ビットコードが正式で、8ビット目は使用できない規格がいくつか存在する。

は[テキスト](../Page/テキスト.md "wikilink")の文書構造や見た目に関する情報を（基本的に文字コードとしては）持たない（垂直タブや改頁はそういったものの一種と考えられなくもないが、「制御コード」となっている）。そのような情報は[マークアップ言語](../Page/マークアップ言語.md "wikilink")などを使用することで補うことができる。

ASCIIの構成は次のようになっている。

| コード範囲（16進） | 内容                                                    |
| ---------- | ----------------------------------------------------- |
| 00-1F      | 制御文字                                                  |
| 20         | 空白                                                    |
| 21-7E      | [図形文字](https://ja.wikipedia.org/wiki/図形文字 "wikilink") |
| 7F         | 制御文字（DEL）                                             |

## ASCII制御文字

初めの32文字（10進数で0-31）はでは[制御文字](../Page/制御文字.md "wikilink")として予約されている。基本的にはこれらの制御文字は表示するための文字ではなく、[モニタ](https://ja.wikipedia.org/wiki/モニタ "wikilink")や[プリンタなどの機器を制御するために用いられる](https://ja.wikipedia.org/wiki/プリンター "wikilink")。例えば、 10（10進）は （改行）を表しプリンタの紙送りなどに用いる、 27 はエスケープを表す。

127（全てのビットがオン、つまり、2進数で1111111）は、（[削除文字](https://ja.wikipedia.org/wiki/削除文字 "wikilink")） として知られる制御文字である。この記号が現れた場合、その部分のデータが消去されていることを示す。この制御文字だけ先頭部分になく最後にある理由は、[パンチテープへの記録は上書きが出来ないため](../Page/紙テープ.md "wikilink")、削除する際には全てに穴を空けることで対応できるというところからきている（1111111は全てに穴の開いた状態を示す）。また、 0（全てのビットがオフ、つまり2進数で0000000）は  あるいは[ヌル文字](https://ja.wikipedia.org/wiki/ヌル文字 "wikilink")と呼ばれ、 と同様に多くのコンピュータシステムでは無視される。これは、仮にパンチテープと反対に1を0に変えることでデータを記録し、かつ上書きが不可能な媒体が存在する場合でも対応できるようにしているのである。

コードの多くは、データ転送プロトコルで用いられる。（例：ヘッディング開始、テキスト開始、テキスト終了など）

セパレータは[磁気テープ](../Page/磁気テープ.md "wikilink")への保存のために設計された。

や  は、プリンタのような処理の遅いデバイスにおいて、データを失うことがないように情報の流れを制御するために用いることがある。

<table>
<thead>
<tr class="header">
<th><p>2進</p></th>
<th><p>8進</p></th>
<th><p>10進</p></th>
<th><p>16進</p></th>
<th><p>略語</p></th>
<th><p>図形表現</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/キャレット記法" title="wikilink">CS</a></p></th>
<th><p><a href="../Page/エスケープシーケンス.md" title="wikilink">エスケープシーケンス</a></p></th>
<th><p>名前/意味</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>000 0000</p></td>
<td><p>000</p></td>
<td><p>0</p></td>
<td><p>00</p></td>
<td><p>NUL</p></td>
<td></td>
<td><p>^@</p></td>
<td><p>\0</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ヌル文字" title="wikilink">ヌル文字</a></p></td>
</tr>
<tr class="even">
<td><p>000 0001</p></td>
<td><p>001</p></td>
<td><p>1</p></td>
<td><p>01</p></td>
<td><p>SOH</p></td>
<td></td>
<td><p>^A</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ヘッディング開始" title="wikilink">ヘッディング開始</a></p></td>
</tr>
<tr class="odd">
<td><p>000 0010</p></td>
<td><p>002</p></td>
<td><p>2</p></td>
<td><p>02</p></td>
<td><p>STX</p></td>
<td></td>
<td><p>^B</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/テキスト開始" title="wikilink">テキスト開始</a></p></td>
</tr>
<tr class="even">
<td><p>000 0011</p></td>
<td><p>003</p></td>
<td><p>3</p></td>
<td><p>03</p></td>
<td><p>ETX</p></td>
<td></td>
<td><p>^C</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/テキスト終結文字" title="wikilink">テキスト終了</a></p></td>
</tr>
<tr class="odd">
<td><p>000 0100</p></td>
<td><p>004</p></td>
<td><p>4</p></td>
<td><p>04</p></td>
<td><p>EOT</p></td>
<td></td>
<td><p>^D</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/伝送終了" title="wikilink">伝送終了</a></p></td>
</tr>
<tr class="even">
<td><p>000 0101</p></td>
<td><p>005</p></td>
<td><p>5</p></td>
<td><p>05</p></td>
<td><p>ENQ</p></td>
<td></td>
<td><p>^E</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/問い合わせ文字" title="wikilink">問い合わせ</a></p></td>
</tr>
<tr class="odd">
<td><p>000 0110</p></td>
<td><p>006</p></td>
<td><p>6</p></td>
<td><p>06</p></td>
<td><p>ACK</p></td>
<td></td>
<td><p>^F</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/肯定応答" title="wikilink">肯定応答</a></p></td>
</tr>
<tr class="even">
<td><p>000 0111</p></td>
<td><p>007</p></td>
<td><p>7</p></td>
<td><p>07</p></td>
<td><p>BEL</p></td>
<td></td>
<td><p>^G</p></td>
<td><p>\a</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ベル文字" title="wikilink">ベル</a></p></td>
</tr>
<tr class="odd">
<td><p>000 1000</p></td>
<td><p>010</p></td>
<td><p>8</p></td>
<td><p>08</p></td>
<td><p>BS</p></td>
<td></td>
<td><p>^H</p></td>
<td><p>\b</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/バックスペースキー" title="wikilink">後退</a></p></td>
</tr>
<tr class="even">
<td><p>000 1001</p></td>
<td><p>011</p></td>
<td><p>9</p></td>
<td><p>09</p></td>
<td><p>HT</p></td>
<td></td>
<td><p>^I</p></td>
<td><p>\t</p></td>
<td><p><a href="../Page/タブキー.md" title="wikilink">水平タブ</a></p></td>
</tr>
<tr class="odd">
<td><p>000 1010</p></td>
<td><p>012</p></td>
<td><p>10</p></td>
<td><p>0A</p></td>
<td><p>LF</p></td>
<td></td>
<td><p>^J</p></td>
<td><p>\n</p></td>
<td><p><a href="../Page/改行コード.md" title="wikilink">改行</a></p></td>
</tr>
<tr class="even">
<td><p>000 1011</p></td>
<td><p>013</p></td>
<td><p>11</p></td>
<td><p>0B</p></td>
<td><p>VT</p></td>
<td></td>
<td><p>^K</p></td>
<td><p>\v</p></td>
<td><p><a href="../Page/タブキー.md" title="wikilink">垂直タブ</a></p></td>
</tr>
<tr class="odd">
<td><p>000 1100</p></td>
<td><p>014</p></td>
<td><p>12</p></td>
<td><p>0C</p></td>
<td><p>FF</p></td>
<td></td>
<td><p>^L</p></td>
<td><p>\f</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/書式送り" title="wikilink">書式送り</a></p></td>
</tr>
<tr class="even">
<td><p>000 1101</p></td>
<td><p>015</p></td>
<td><p>13</p></td>
<td><p>0D</p></td>
<td><p>CR</p></td>
<td></td>
<td><p>^M</p></td>
<td><p>\r</p></td>
<td><p><a href="../Page/改行コード.md" title="wikilink">復帰</a></p></td>
</tr>
<tr class="odd">
<td><p>000 1110</p></td>
<td><p>016</p></td>
<td><p>14</p></td>
<td><p>0E</p></td>
<td><p>SO</p></td>
<td></td>
<td><p>^N</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/シフトアウト" title="wikilink">シフトアウト</a></p></td>
</tr>
<tr class="even">
<td><p>000 1111</p></td>
<td><p>017</p></td>
<td><p>15</p></td>
<td><p>0F</p></td>
<td><p>SI</p></td>
<td></td>
<td><p>^O</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/シフトイン" title="wikilink">シフトイン</a></p></td>
</tr>
<tr class="odd">
<td><p>001 0000</p></td>
<td><p>020</p></td>
<td><p>16</p></td>
<td><p>10</p></td>
<td><p>DLE</p></td>
<td></td>
<td><p>^P</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/伝送制御拡張" title="wikilink">伝送制御拡張</a></p></td>
</tr>
<tr class="even">
<td><p>001 0001</p></td>
<td><p>021</p></td>
<td><p>17</p></td>
<td><p>11</p></td>
<td><p>DC1</p></td>
<td></td>
<td><p>^Q</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/装置制御1" title="wikilink">装置制御1</a>、<a href="https://ja.wikipedia.org/wiki/ソフトウェアフロー制御" title="wikilink">XON</a></p></td>
</tr>
<tr class="odd">
<td><p>001 0010</p></td>
<td><p>022</p></td>
<td><p>18</p></td>
<td><p>12</p></td>
<td><p>DC2</p></td>
<td></td>
<td><p>^R</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/装置制御2" title="wikilink">装置制御2</a></p></td>
</tr>
<tr class="even">
<td><p>001 0011</p></td>
<td><p>023</p></td>
<td><p>19</p></td>
<td><p>13</p></td>
<td><p>DC3</p></td>
<td></td>
<td><p>^S</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/装置制御3" title="wikilink">装置制御3</a>、<a href="https://ja.wikipedia.org/wiki/ソフトウェアフロー制御" title="wikilink">XOFF</a></p></td>
</tr>
<tr class="odd">
<td><p>001 0100</p></td>
<td><p>024</p></td>
<td><p>20</p></td>
<td><p>14</p></td>
<td><p>DC4</p></td>
<td></td>
<td><p>^T</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/装置制御4" title="wikilink">装置制御4</a></p></td>
</tr>
<tr class="even">
<td><p>001 0101</p></td>
<td><p>025</p></td>
<td><p>21</p></td>
<td><p>15</p></td>
<td><p>NAK</p></td>
<td></td>
<td><p>^U</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/否定応答" title="wikilink">否定応答</a></p></td>
</tr>
<tr class="odd">
<td><p>001 0110</p></td>
<td><p>026</p></td>
<td><p>22</p></td>
<td><p>16</p></td>
<td><p>SYN</p></td>
<td></td>
<td><p>^V</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/同期文字" title="wikilink">同期信号</a></p></td>
</tr>
<tr class="even">
<td><p>001 0111</p></td>
<td><p>027</p></td>
<td><p>23</p></td>
<td><p>17</p></td>
<td><p>ETB</p></td>
<td></td>
<td><p>^W</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/伝送ブロック終結" title="wikilink">伝送ブロック終結</a></p></td>
</tr>
<tr class="odd">
<td><p>001 1000</p></td>
<td><p>030</p></td>
<td><p>24</p></td>
<td><p>18</p></td>
<td><p>CAN</p></td>
<td></td>
<td><p>^X</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/キャンセル文字" title="wikilink">取消</a></p></td>
</tr>
<tr class="even">
<td><p>001 1001</p></td>
<td><p>031</p></td>
<td><p>25</p></td>
<td><p>19</p></td>
<td><p>EM</p></td>
<td></td>
<td><p>^Y</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/媒体終端" title="wikilink">媒体終端</a></p></td>
</tr>
<tr class="odd">
<td><p>001 1010</p></td>
<td><p>032</p></td>
<td><p>26</p></td>
<td><p>1A</p></td>
<td><p>SUB</p></td>
<td></td>
<td><p>^Z</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/置換文字" title="wikilink">置換</a></p></td>
</tr>
<tr class="even">
<td><p>001 1011</p></td>
<td><p>033</p></td>
<td><p>27</p></td>
<td><p>1B</p></td>
<td><p>ESC</p></td>
<td></td>
<td><p>^[</p></td>
<td><p>\e</p></td>
<td><p><a href="../Page/エスケープ文字.md" title="wikilink">エスケープ</a></p></td>
</tr>
<tr class="odd">
<td><p>001 1100</p></td>
<td><p>034</p></td>
<td><p>28</p></td>
<td><p>1C</p></td>
<td><p>FS</p></td>
<td></td>
<td><p>^\</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ファイル分離標識" title="wikilink">ファイル分離標識</a></p></td>
</tr>
<tr class="even">
<td><p>001 1101</p></td>
<td><p>035</p></td>
<td><p>29</p></td>
<td><p>1D</p></td>
<td><p>GS</p></td>
<td></td>
<td><p>^]</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/グループ分離標識" title="wikilink">グループ分離標識</a></p></td>
</tr>
<tr class="odd">
<td><p>001 1110</p></td>
<td><p>036</p></td>
<td><p>30</p></td>
<td><p>1E</p></td>
<td><p>RS</p></td>
<td></td>
<td><p>^^</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/レコード分離標識" title="wikilink">レコード分離標識</a></p></td>
</tr>
<tr class="even">
<td><p>001 1111</p></td>
<td><p>037</p></td>
<td><p>31</p></td>
<td><p>1F</p></td>
<td><p>US</p></td>
<td></td>
<td><p>^_</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ユニット分離標識" title="wikilink">ユニット分離標識</a></p></td>
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
</tr>
<tr class="even">
<td><p>111 1111</p></td>
<td><p>177</p></td>
<td><p>127</p></td>
<td><p>7F</p></td>
<td><p>DEL</p></td>
<td></td>
<td><p>^?</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/削除文字" title="wikilink">抹消</a></p></td>
</tr>
</tbody>
</table>

## ASCII印字可能文字

ASCII 32は、空白文字である。キーボードのスペースキーから入力でき、語と語の間に空白を表示する。 ASCII 33〜126は印刷可能な文字 (printable characters) であり、半角英数の数字、句読点や記号を表す。若い順から[エクスクラメーションマーク](https://ja.wikipedia.org/wiki/エクスクラメーションマーク "wikilink")、[ダブルクオーテーション](https://ja.wikipedia.org/wiki/ダブルクオーテーション "wikilink")、…と続き、ラテン文字大文字の前に数字と大半の半角[約物](../Page/約物.md "wikilink")、大文字と小文字の間、ラテン文字小文字の後にも数種類の半角約物が割り当てられている。

下の図では、16進数・10進数・8進数の順でASCIIコードの値を示す。

大文字のASCII値に32を加えると小文字に変換することができる。この変換は、2進法では、6ビット目に1をセットするだけでよい。また、数字から48を減じれば、対応する値が得られる。この変換は、5ビット目及び6ビット目に0をセットするか、あるいは単純に上位4ビットを無視するだけでもよい。なお、印字可能文字のうち「@」から始まる32文字については、ASCII値を64減じて対応する制御文字を求め、この制御文字を「コントロール+」（）という前置表現を付けた印字可能文字で表記する慣習がある。

この制御文字の表記方法は、キーボード上の印字可能文字キーを制御文字の送出に用いていた機器の名残りであると考えられる（7ビット目を0にセットする専用キー（[Ctrlキー](https://ja.wikipedia.org/wiki/Ctrlキー "wikilink")）を、印字可能文字キーと同時に押して制御文字を送出）。

  - が `^@`

  - が `^[`

  - が `^\`

  - が `^]`

  - が `^^`

  - が `^_`

  - が `^?`

## 参考文献

  - 「」（1963年6月17日制定、1986年3月26日最終改正、2002年1月15日規格番号変更）

## 関連項目

  - [JIS X 0201](https://ja.wikipedia.org/wiki/JIS_X_0201 "wikilink")

[Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink") [Category:プレゼンテーション層プロトコル](https://ja.wikipedia.org/wiki/Category:プレゼンテーション層プロトコル "wikilink")