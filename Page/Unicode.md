> この記事は[Unicode](https://ja.wikipedia.org/wiki/Unicode)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:New_Unicode_logo.svg "wikilink")  **Unicode**（ユニコード）は、[符号化文字集合](https://ja.wikipedia.org/wiki/符号化文字集合 "wikilink")や[文字符号化方式](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink")などを定めた、[文字コード](../Page/文字コード.md "wikilink")の業界規格である。文字集合（文字セット）が単一の[大規模文字セット](../Page/大規模文字セット.md "wikilink")であること（「Uni」という名はそれに由来する）などが特徴である。

[1980年代](../Page/1980年代.md "wikilink")に、[Starワークステーションの日本語化](../Page/Xerox_Star.md "wikilink") (J-Star) などを行った[ゼロックス](../Page/ゼロックス.md "wikilink")社が提唱し、[マイクロソフト](../Page/マイクロソフト.md "wikilink")、[アップル](../Page/アップル_\(企業\).md "wikilink")、[IBM](../Page/IBM.md "wikilink")、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")、[ジャストシステム](../Page/ジャストシステム.md "wikilink")などが参加する[ユニコードコンソーシアム](../Page/ユニコードコンソーシアム.md "wikilink")により作られた。国際規格の[ISO/IEC 10646とUnicode規格は同じ文字コード表になるように協調して策定されている](https://ja.wikipedia.org/wiki/ISO/IEC_10646 "wikilink")\[1\]。

## 概要

Unicode は世界で使われる全ての文字を共通の文字集合にて利用できるようにしようという考えで作られ、[Unix](../Page/UNIX.md "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Plan 9](../Page/Plan_9_from_Bell_Labs.md "wikilink")\[2\]、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")などで利用されている。現代の文字だけでなく古代の文字や歴史的な文字、数学記号、絵文字なども含む\[3\]。

Unicode以前の[文字コード](../Page/文字コード.md "wikilink")との相互運用性もある程度考慮されており、歴史上・実用上の識別が求められる場合には互換領域がとられ、元のコード→Unicode→元のコードというような変換（ラウンドトリップ変換）において、元通りに戻るよう配慮されている文字もある。しかし、正規の[JIS X 0208の範囲内であればトラブルは少ないが](../Page/JIS_X_0208.md "wikilink")、複数の文字集合が混在したり、[Shift_JIS](../Page/Shift_JIS.md "wikilink")の実態である[CP932や](../Page/Microsoftコードページ932.md "wikilink")[EUC-JPの亜種であるCP](https://ja.wikipedia.org/wiki/EUC-JP#EUC-JPの亜種 "wikilink")51932とeucJP-MSなど、対応が違うために文字化けを起こすことがある。

## Unicode文字符号化モデル

文字コードは、Unicode文字符号化モデル\[4\]によると以下の4段階に分けられる。

  - **抽象文字集合**（）：符号化の対象とする順序のない文字の集合。

<!-- end list -->

  - **符号化文字集合**（）：抽象文字集合を非負整数に対応させたもの。この非負整数の範囲を符号空間、各値を符号位置といい、抽象文字は対応後、符号化文字となる\[5\]。抽象文字は複数の符号化文字に対応されることもある\[6\]。

<!-- end list -->

  - **文字符号化形式**（）：符号化文字集合の非負整数を符号単位列に変換する方法。文字符号化形式はコンピュータ中に実際にデータとして文字を表現することを可能にする。

<!-- end list -->

  - **文字符号化方式**（）：符号単位列をバイト列に[直列化](https://ja.wikipedia.org/wiki/直列化 "wikilink")する方法。符号単位が8ビットより大きい場合は[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")が関係する。

その後バイト列を、[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")などで圧縮したり、7ビット伝送路に通すため[Base64](../Page/Base64.md "wikilink")、[Quoted-printable](https://ja.wikipedia.org/wiki/Quoted-printable "wikilink")などで変換することがあるが、これらは文字コードの範囲外である。

## 文字集合

Unicodeの文字集合の符号空間は0 - 10FFFF<sub>16</sub>で111万4112符号位置がある\[7\]。Unicode 12.1(2019年5月7日公表)では13万7929個(12%)の文字\[8\]が割り当てられ、65個を制御文字に使い、13万7468符号位置(12%)を私用文字として確保している。また、2048文字分をUTF-16のための代用符号位置に使用しており、加えて66の特別な符号位置は使われない。残りの83万6536符号位置(75%)は未使用である\[9\]。

文字を特定する場合にはUnicode符号位置や一意につけられた名前が使われる。例えば「a」はU+0061 (LATIN SMALL LETTER A)、「♪」はU+266A (EIGHTH NOTE)である。Unicode符号位置を文章中などに記す場合は "U+" の後に[十六進法](../Page/十六進法.md "wikilink")で符号位置を4桁から6桁続けることで表す。また、符号空間のうち代用符号位置を除く符号位置をUnicodeスカラ値という\[10\]。

収録されている文字は、各国で標準として規定されている文字集合や実際に使用されている文字を持ち寄り、委員会により取捨選択されている。日本の文字については当初より [JIS X 0201](https://ja.wikipedia.org/wiki/JIS_X_0201 "wikilink")、[JIS X 0208](../Page/JIS_X_0208.md "wikilink")、[JIS X 0212を](../Page/JIS_X_0212.md "wikilink")、Unicode 3.1 からは [JIS X 0213](../Page/JIS_X_0213.md "wikilink") の内容も収録している。

また収録において、元の各文字集合内で分離されている文字は尊重するが、異なる文字集合に同一の文字が収録されているとみなされるものは、同じ符号位置に割り当てる方針を取っている。この際に集合が膨大であるという理由で、漢字について、[中国](../Page/中国.md "wikilink")、[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")、[韓国の各規格の](../Page/大韓民国.md "wikilink")し[CJK統合漢字](../Page/CJK統合漢字.md "wikilink")としたことは大きな議論となった。

Unicodeに収録されている文字については、「[ブロックの一覧](https://ja.wikipedia.org/wiki/ブロック_\(Unicode\)#ブロックの一覧 "wikilink")」を参照。

## 文字符号化形式

Unicodeでは文字符号化形式として[UTF-8](../Page/UTF-8.md "wikilink")、[UTF-16](../Page/UTF-16.md "wikilink")、[UTF-32](../Page/UTF-32.md "wikilink")の3種類が定められている。

UTF-8は1符号化文字を1〜4符号単位で表す可変幅文字符号化形式で、1符号単位は8ビットである。

UTF-16は1符号化文字を1〜2符号単位で表す可変幅文字符号化形式で、1符号単位は16ビットである。[基本多言語面](../Page/基本多言語面.md "wikilink")の文字を符号単位一つで、その他の文字を[サロゲートペア](https://ja.wikipedia.org/wiki/#サロゲートペア "wikilink")（代用対）という仕組みを使い符号単位二つで表現する。

UTF-32は1符号化文字を1符号単位で表す固定幅文字符号化形式で、1符号単位は32ビットである。ただし、Unicodeの符号空間がU+10FFFFまでであるため、実際に使われるのは21ビットまでである。

|          | 00       | 01       | 02       | 03   | 04 | 05 | 06 | 07 | 08 | 09 | 0A | 0B | 0C | 0D | 0E | 0F |
| -------- | -------- | -------- | -------- | ---- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| UTF-8    | A        | Ω        | 語        | 😊    |    |    |    |    |    |    |    |    |    |    |    |    |
| 41       | CE       | A9       | E8       | AA   | 9E | F0 | 9F | 98 | 8A |    |    |    |    |    |    |    |
| UTF-16   | A        | Ω        | 語        | 😊    |    |    |    |    |    |    |    |    |    |    |    |    |
| 0041     | 03A9     | 8A9E     | D83D     | DE0A |    |    |    |    |    |    |    |    |    |    |    |    |
| UTF-32   | A        | Ω        | 語        | 😊    |    |    |    |    |    |    |    |    |    |    |    |    |
| 00000041 | 000003A9 | 00008A9E | 0001F60A |      |    |    |    |    |    |    |    |    |    |    |    |    |

各文字符号化形式の符号化例

## 文字符号化方式

<table>
<thead>
<tr class="header">
<th><p>文字符号化形式<br />
(CEF)</p></th>
<th><p>文字符号化方式<br />
(CES)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>UTF-8</p></td>
<td><p>UTF-8</p></td>
</tr>
<tr class="even">
<td><p>UTF-16</p></td>
<td><p>UTF-16</p></td>
</tr>
<tr class="odd">
<td><p>UTF-16BE</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>UTF-16LE</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>UTF-32</p></td>
<td><p>UTF-32</p></td>
</tr>
<tr class="even">
<td><p>UTF-32BE</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>UTF-32LE</p></td>
<td></td>
</tr>
</tbody>
</table>

Unicodeでは文字符号化方式として**UTF-8**、**UTF-16**、**UTF-16BE**、**UTF-16LE**、**UTF-32**、**UTF-32BE**、**UTF-32LE**の7種類が定められている。それぞれの符号化形式に対応する符号化方式は表の通り。

文字符号化形式との違いは、文字符号化形式がプログラム内部で文字を扱う場合に符号なし整数として文字を表現する方法なのに対し、文字符号化方式は入出力時にバイト列として表現する方法である。UTF-8は符号単位が8ビットであるため区別する意味はない。

<table>
<thead>
<tr class="header">
<th><p>文字符号化方式<br />
(CES)</p></th>
<th><p>エンディアン</p></th>
<th><p>BOMの付与</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>UTF-8</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>UTF-16</p></td>
<td><p>ビッグ/リトル</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>UTF-16BE</p></td>
<td><p>ビッグエンディアン</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>UTF-16LE</p></td>
<td><p>リトルエンディアン</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>UTF-32</p></td>
<td><p>ビッグ/リトル</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>UTF-32BE</p></td>
<td><p>ビッグエンディアン</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>UTF-32LE</p></td>
<td><p>リトルエンディアン</p></td>
<td></td>
</tr>
</tbody>
</table>

  - UTF-8

<!-- end list -->

  -
    可変長（1-4バイト）の8ビット符号単位で表現する文字符号化方式。ASCIIに対して[上位互換](https://ja.wikipedia.org/wiki/上位互換 "wikilink")となっており、文字の境界が明確である、UTF-16符号化方式やUTF-32符号化方式との変換・逆変換に際して乗除算などの高負荷処理が必要ない、などの特長を持ち、インターネットではもっとも一般的に利用されている。

    なお、UTF-8はもともと8ビットを符号単位とするため[BOM](https://ja.wikipedia.org/wiki/バイトオーダーマーク "wikilink")（バイト順マーク；後述）は必要ないが、UTF-8であることが識別できるよう、データストリームの先頭に EF BB BF（U+FEFFのUTF-8での表現）の3バイトが付与されることがある。UTF-8のBOMはバイト順を表すものではなく、UTF-16符号化方式等における「真の意味でのBOM」と同じコードポイントを利用しているがゆえに慣用的にこう呼ばれているに過ぎない。UTF-8でのBOMの使用は非推奨\[11\]。

  - UTF-16

<!-- end list -->

  -
    UTF-16符号化方式では、通常はファイルの先頭にバイト順マーク (BOM) が付与される。BOMとは、通信やファイルの読み書き等、8ビット単位の処理で[バイト順を識別するための印であり](https://ja.wikipedia.org/wiki/エンディアン "wikilink")、データストリームの先頭に付与される。値はU+FEFF。システムが読み込んだ先頭2バイトが FF FEならリトルエンディアン、FE FFならビッグエンディアンとして後に続く文書を処理する。

    RFC 2781 ではBOMが付いていないUTF-16文書はビッグエンディアンとして解釈することになっている。Windowsのメモ帳で作成した「Unicodeテキスト」はBOMが付与されるようになっている。ビッグエンディアンの符号化方式を**UTF-16BE**、リトルエンディアンの符号化方式を**UTF-16LE**として区別することもある。プロトコルもしくはアプリケーションの設定などの手段で符号化方式に**UTF-16BE**や**UTF-16LE**を指定している場合にはBOMを付与することは許容されない。Windows上の文書における「Unicodeテキスト」は特に明記のない場合、リトルエンディアンのUTF-16符号化方式のことを指す。TCP/IPネットワークでは、プロトコルヘッダやMIME等の手段で符号化方式が指定されずBOMも付与されない場合、ビッグエンディアンとして扱うと決められている。

  - UTF-32

<!-- end list -->

  -
    UTF-32符号化方式でもUTF-16符号化方式と同じく、ビッグエンディアンとリトルエンディアンが存在し、それぞれ**UTF-32BE**、**UTF-32LE**と呼ばれる。プロトコルもしくはアプリケーションの設定などの手段で符号化方式に**UTF-32BE**や**UTF-32LE**を指定している場合にはBOMを付与することは許容されない。
    単純な符号化方式であるが、テキストファイルなどではファイルのサイズが大きくなる（すべてBMPの文字からなる文章の場合はUTF-16符号化方式の2倍、すべてASCII文字の場合はASCII/UTF-8の4倍のサイズとなる）ため、ストレージ用として使われることは稀である。そのためか、[Microsoft Officeでの](../Page/Microsoft_Office.md "wikilink")「エンコードされたテキストファイル」の読み書きでは、Office 2016 でもいまだに符号化方式には対応していない。[フリーウェア](../Page/フリーウェア.md "wikilink")・[シェアウェア](../Page/シェアウェア.md "wikilink")の[テキストエディタ](../Page/テキストエディタ.md "wikilink")のうち多数の符号化方式に対応しているものでも、この符号化方式には対応していないものが存在する。
    ただし、すべてのUnicode文字を処理する場合には、すべての文字を単一の符号単位で表現したほうが処理に適するため、内部の処理ではUTF-32符号化形式（あるいはUCS-4）で扱うこともある。実例として、[Linux](../Page/Linux.md "wikilink") 上の[C言語](../Page/C言語.md "wikilink")環境では `wchar_t` は32ビット整数型である。
    UTF-16符号化方式などと同様にUTF-32符号化方式にもBOMがあり、データストリームの先頭に付される。先頭の4バイトがFF FE 00 00ならリトルエンディアン、00 00 FE FFならビッグエンディアンになる。UTF-16のリトルエンディアンとUTF-32のリトルエンディアンは最初の2バイトが等しいため、4バイトまで読んで判断する必要がある。

| UTF-8    | A  | Ω  | 語  | 😊  |    |
| -------- | -- | -- | -- | -- | -- |
| 41       | CE | A9 | E8 | AA | 9E |
| UTF-16BE | A  | Ω  | 語  | 😊  |    |
| 00       | 41 | 03 | A9 | 8A | 9E |
| UTF-16LE | A  | Ω  | 語  | 😊  |    |
| 41       | 00 | A9 | 03 | 9E | 8A |
| UTF-32BE | A  | Ω  | 語  | 😊  |    |
| 00       | 00 | 00 | 41 | 00 | 00 |
| UTF-32LE | A  | Ω  | 語  | 😊  |    |
| 41       | 00 | 00 | 00 | A9 | 03 |

各文字符号化方式の符号化例

### その他

  - UTF-7

<!-- end list -->

  -
    UTF-16で表したUnicodeを[Base64](../Page/Base64.md "wikilink")で変換して表す符号化方式。ただし、[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")のアルファベット範囲等についてはBase64に変換しない等、特殊な符号化方式を行う。RFC 2152で定められており、Unicode規格及びUnicodeの関連規格には含まれない。かつての[SMTP等のように](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")、7ビット単位でしかデータを扱えない通信方式を利用する場合を想定して作られている。ステートフルエンコーディングであり、運用上問題が多いため、現在ではこの方式は推奨されていない。Unicode文字を7ビット単位伝送通信にどうしても通さなければならない場合は、替わりにUTF-8をQuoted-printableあるいはBase64で変換するなどの方式が好ましい。


以下は[エイプリルフール](https://ja.wikipedia.org/wiki/エイプリルフール "wikilink")に公開された[ジョークRFCである](https://ja.wikipedia.org/wiki/Request_for_Comments#ジョークRFC "wikilink") (RFC 4042)。UTF-9に関しては同名の規格が実際に検討されていた（ただし、内容は大きく異なる）が、ドラフト段階で破棄されているため重複にはならない。

  - UTF-9
    可変長の9ビット符号単位で表現する符号化方式。1[バイトが](../Page/バイト_\(情報\).md "wikilink")[8ビット](../Page/8ビット.md "wikilink")（[オクテット](https://ja.wikipedia.org/wiki/オクテット_\(コンピュータ\) "wikilink")）ではなく9ビット（[ノネット](https://ja.wikipedia.org/wiki/ノネット "wikilink")）であるような環境での利用を想定している。UTF-8と比較した場合、Latin-1領域が1バイト、[CJK統合漢字](../Page/CJK統合漢字.md "wikilink")領域が2バイトで表現できる特長があり、データ量が少なくなる。[ワード](../Page/ワード.md "wikilink")長が9の倍数のコンピュータ（[PDP-10](../Page/PDP-10.md "wikilink")や[ACOS-6](../Page/ACOS-6.md "wikilink")など）であれば計算コストも低い。
  - UTF-18
    Unicode符号位置を単一の18ビット符号単位で表現する符号化方式。UTF-8に対するUTF-16のようなものだが、RFC公開時点のUnicodeで文字が定義されていた4つの[面](../Page/面_\(文字コード\).md "wikilink")（BMP、U+1xxxx、U+2xxxx、U+Exxxx）を余った2ビットで識別するため、[代用符号位置は使わない](https://ja.wikipedia.org/wiki/Unicode文字のマッピング#代用符号位置 "wikilink")。

以下はドラフト段階で破棄された規格案。

  - UTF-5
    [国際化ドメイン名](../Page/国際化ドメイン名.md "wikilink")での利用を想定し、0-9、A-Vの32文字で表現する文字符号化方式。国際化ドメイン名には[Punycode](../Page/Punycode.md "wikilink")が採用されたため、利用されていない。

<!-- end list -->

  - UTF-9
    可変長（1-5バイト）の8ビット符号単位で表現する文字符号化形式または文字符号化方式。ISO-8859-1に対して一部互換である。しかし、UTF-8が普及しつつあり、それと比べて欠点がいくつかあったため、破棄された。

## 拡張領域

1980年代の当初の構想では、Unicodeは16ビット固定長で、2<sup>16</sup> = 6万5536 個の符号位置に必要な全ての文字を収録する、というもくろみであった。しかし、Unicode 1.0公表後、拡張可能な空き領域2万字分を巡り、各国から文字追加要求が起こった。その内容は中国、日本、台湾、ベトナム、シンガポールの追加漢字約1万5千字、[古ハングル](https://ja.wikipedia.org/wiki/古ハングル "wikilink")約5千字、未登録言語の文字などである。このようにしてUnicodeの、16ビットの枠内に全世界の文字を収録するという計画は早々に破綻し、1996年のUnicode 2.0の時点で既に、文字集合の空間を16ビットから広げることが決まった。この時、それまでの16ビットを前提としてすでに設計されていたシステム（たとえば[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のchar型や、[Windows NT](https://ja.wikipedia.org/wiki/Windows_NT "wikilink")・[Windows 95のAPI](https://ja.wikipedia.org/wiki/Windows_95 "wikilink")）をなるべくそのままにしたまま、広げられた空間にある符号位置を表現する方法として、サロゲートペアが定義された。

### サロゲートペア

サロゲートペア(代用対)は16ビットUnicodeの領域1024文字分を2つ使い（前半 U+D800 〜 U+DBFF、後半 U+DC00 〜 U+DFFF）、各々1個ずつからなるペアで1024 × 1024 = 1,048,576文字を表す。これはちょうど16面分であり、第1面〜第16面（U+10000 〜 U+10FFFF）の文字をこれで表すこととした。加えて第0面（[基本多言語面](../Page/基本多言語面.md "wikilink")）も使用可能なので、Unicodeには合計で 1,048,576 + 65,536 - 2,048 = 111万2,064文字分の空間が確保されたことになる。Unicodeの符号空間が10FFFF<sub>16</sub>まで(サロゲート領域を除いて111万2064文字)とされているのはUTF-16が表現可能な限界だからである。

サロゲートはUnicodeの符号位置の U+10000 〜 U+10FFFF の範囲を16ビットユニットのペア（2つ）で表現する集合で、最初の16ビットユニットを前半サロゲートもしくはハイサロゲート、二番目を後半サロゲートもしくはローサロゲートと称する。ハイサロゲートは U+D800 〜 U+DBFF の範囲、ローサロゲートは U+DC00 〜 U+DFFF の範囲である。

サロゲートペアはUTF-16でのみ使われ\[12\]、UTF-8、UTF-32ではすべての符号位置を符号化できるためこのような特別な処理は必要ない。

#### コーディング

サロゲートのエンコーディングは、

`       $hi = ($uni - 0x10000) / 0x400 + 0xD800;`
`       $lo = ($uni - 0x10000) % 0x400 + 0xDC00;`

デコーディングは、

`       $uni = 0x10000 + ($hi - 0xD800) * 0x400 + ($lo - 0xDC00);`

となる。

**コード変換例**：

「[𠮷](https://ja.wikipedia.org/wiki/wikt:𠮷 "wikilink")」U+20BB7 (下の棒が長い「吉」。つちよし。) のエンコードを考えてみる。

` 0x20BB7 (``) から`
` 0x10000 (0001 0000 0000 0000 0000) を引くと、結果は`
` 0x10BB7 (``) となる。`
` `
`  これを上位10ビット値と下位10ビット値に分割する。`
` `` (``) + `` (``)`

`  ハイ（高位）サロゲートを形成するために上位ビットに0xD800を加える。`
` `` (``) + 1101 1000 0000 0000 (0xD800) = 1101 10`` (0xD842)`
` `
`  ロー（下位）サロゲートを形成するために下位ビットに0xDC00を加える。`
` `` (``) + 1101 1100 0000 0000 (0xDC00) = 1101 11`` (0xDFB7)`
` `
`  結果:`
` `` ``  （UTF-16 符号単位列）`
` `` ``（UTF-16BEでの符号化バイト列）`
` `` ``（UTF-16LEでの符号化バイト列）`

次の表は、この文字変換と他をまとめたものである。 色は、コードポイントからのビットがUTF-16バイトにどのように分配されるかを示した。 なお、UTF-16エンコーディングプロセスによって追加された追加ビットは黒で示されている。

<table>
<thead>
<tr class="header">
<th><p>文字<br />
（符号位置）</p></th>
<th><p>符号位置(2進数)</p></th>
<th><p>UTF-16<br />
符号単位列(2進数)</p></th>
<th><p>UTF-16<br />
符号単位列</p></th>
<th><p>UTF-16BE<br />
符号化バイト列</p></th>
<th><p>UTF-16LE<br />
符号化バイト列</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/$.md" title="wikilink">$</a></p></td>
<td><p><code>U+0024</code></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/€" title="wikilink">€</a></p></td>
<td><p><code>U+20AC</code></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/wikt:𠮷" title="wikilink">𠮷</a></p></td>
<td><p><code>U+20BB7</code></p></td>
<td><p></p></td>
<td><p><code>1101 10</code><code> 1101 11</code></p></td>
<td><p><code> </code></p></td>
<td><p><code> </code></p></td>
</tr>
<tr class="even">
<td><p>最大値</p></td>
<td><p><code>U+10FFFF</code></p></td>
<td><p></p></td>
<td><p><code>1101 10</code><code> 1101 11</code></p></td>
<td><p><code> </code></p></td>
<td><p><code> </code></p></td>
</tr>
</tbody>
</table>

## 面

一つの面は6万5536個の符号位置がある。

| 面    | 符号位置                  | 英語での名称                              | 略称  | 日本語での名称                                                     | 収録されている主な文字                                         |
| ---- | --------------------- | ----------------------------------- | --- | ----------------------------------------------------------- | --------------------------------------------------- |
| 第0面  | `U+0000 - U+FFFF`     | Basic Multilingual Plane            | BMP | [基本多言語面](../Page/基本多言語面.md "wikilink")                      | 基本的な文字。                                             |
| 第1面  | `U+10000 - U+1FFFF`   | Supplementary Multilingual Plane    | SMP | [追加多言語面](../Page/追加多言語面.md "wikilink")                      | 古代文字や記号・[絵文字](../Page/絵文字.md "wikilink")類など。        |
| 第2面  | `U+20000 - U+2FFFF`   | Supplementary Ideographic Plane     | SIP | [追加漢字面](https://ja.wikipedia.org/wiki/追加漢字面 "wikilink")     | 漢字専用領域。                                             |
| 第3面  | `U+30000 - U+3FFFF`   | Tertiary Ideographic Plane          | TIP | [第三漢字面](https://ja.wikipedia.org/wiki/第三漢字面 "wikilink")     | 追加漢字面に入りきらなかった漢字。また、将来的には古代漢字や甲骨文字などが収録される予定\[13\]。 |
| 第4面  | `U+40000 - U+4FFFF`   | 未使用（将来どのような目的で使用するのかすら決まっていない）。     |     |                                                             |                                                     |
| 第5面  | `U+50000 - U+5FFFF`   |                                     |     |                                                             |                                                     |
| 第6面  | `U+60000 - U+6FFFF`   |                                     |     |                                                             |                                                     |
| 第7面  | `U+70000 - U+7FFFF`   |                                     |     |                                                             |                                                     |
| 第8面  | `U+80000 - U+8FFFF`   |                                     |     |                                                             |                                                     |
| 第9面  | `U+90000 - U+9FFFF`   |                                     |     |                                                             |                                                     |
| 第10面 | `U+A0000 - U+AFFFF`   |                                     |     |                                                             |                                                     |
| 第11面 | `U+B0000 - U+BFFFF`   |                                     |     |                                                             |                                                     |
| 第12面 | `U+C0000 - U+CFFFF`   |                                     |     |                                                             |                                                     |
| 第13面 | `U+D0000 - U+DFFFF`   |                                     |     |                                                             |                                                     |
| 第14面 | `U+E0000 - U+EFFFF`   | Supplementary Special-purpose Plane | SSP | [追加特殊用途面](https://ja.wikipedia.org/wiki/追加特殊用途面 "wikilink") | 制御コード専用領域。                                          |
| 第15面 | `U+F0000 - U+FFFFF`   | Private Use Plane                   | PUP | [私用面](https://ja.wikipedia.org/wiki/私用面 "wikilink")         | BMPの U+E000 - U+F8FF の領域の拡張。                        |
| 第16面 | `U+100000 - U+10FFFF` |                                     |     |                                                             |                                                     |
|      |                       |                                     |     |                                                             |                                                     |

日本では2000年に[JIS X 0208を拡張する目的でJIS](../Page/JIS_X_0208.md "wikilink") X 0213（いわゆるJIS第3・第4水準）が制定されたが、この際、新たに採用された文字でUnicodeになかったものの一部は、BMPに収録できず、第2面への収録となった（Unicodeが最終的にJIS X 0213への対応を完了したのは[2002年](../Page/2002年.md "wikilink")である）。このため、JIS X 0213収録文字をUnicodeで完全にサポートするには、追加漢字面をサポートした[OS](../Page/オペレーティングシステム.md "wikilink")、[フォント](../Page/フォント.md "wikilink")、[アプリケーションが必要となる](../Page/アプリケーションソフトウェア.md "wikilink")。Shift_JISなど、Unicodeにて規定されるもの以外のエンコーディングを利用する場合であっても、JIS X 0213に対応するフォントやアプリケーションが必要である。

[常用漢字](../Page/常用漢字.md "wikilink")の[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")改定で追加された字のうち<span style="font-size:150%;">「」</span>はU+20B9Fで、追加漢字面に含まれる。そのため、改定後の常用漢字完全サポートを謳う場合、Unicodeに対応していて更にこの拡張領域にも対応している必要があると言える。ただ、現状ではこの字は、JIS X 0208に含まれる（＝当然、Unicode策定当初からBMPに収録されている）異体字の<span style="font-size:150%;">「叱」</span>(U+53F1) で代用されることが多い。

## 歴史

1984年、ISOの文字コード規格委員会 (ISO/TC 97/SC2) は文字セットの切り替えを行わずに世界中の文字を単一の文字集合として扱える文字コード規格 (ISO 10646) を作成することを決定し、専門の作業グループ (ISO/TC 97/SC 2/WG 2) を設置し、作業を始めていた。1980年代後半にはこの作業グループにおいてさまざまな提案が検討されている。1990年になって出来あがったISO/TC 97/SC 2/WG 2作成のISO 10646の初版ドラフト（[DIS 10646\#DIS 10646第1版](https://ja.wikipedia.org/wiki/DIS_10646#DIS_10646第1版 "wikilink")）では、漢字コードは32ビットで表現され、各国の漢字コードはそのまま入れることになった。しかし中国は漢字を各国でばらばらに符号化するのではなく、あくまで統一して扱うことを求めてこのドラフトには当初から反対しており、今後の漢字コードの方針を決めるため、WG 2は CJK-JRG (Joint Research Group) と呼ばれるグループを別途設置し、そこで引き続き検討することにした。

このような公的機関の動きとは別に、1987年頃から[Xerox](https://ja.wikipedia.org/wiki/Xerox "wikilink")のJoe BeckerとLee Collinsは、後にユニコードと呼ばれるようになる、世界中の文字を統一して扱える文字コードを開発していた。1989年9月には「Unicode Draft 1」が発表された。ここではその基本方針として、2オクテット（16ビット）固定長で全ての文字を扱えることを目指しており、そのために日本・中国・韓国の漢字を統一することで2万弱の漢字コードを入れ、さらに将来の拡張用に、3万程度の漢字の空き領域が別に用意されていた。このドラフトは少しずつ改良を加えられながら1990年4月にUnicode Draft 2、同年12月Unicode Final Draftとなった。さらに1991年1月にはこのUnicode Final Draftに賛同する企業によって、[ユニコードコンソーシアム](../Page/ユニコードコンソーシアム.md "wikilink")が設立された。

1991年6月、ISO/IEC 10646による4オクテット固定長コードを主体としたドラフト「DIS 10646第1版」は、2オクテット固定長コードであるUnicodeとの一本化を求める各国により否決され、ISO 10646とUnicodeの一本化が図られることになった。また中国およびUnicodeコンソーシアムの要請により、CJK-JRGにおいて、ISO 10646とUnicodeの一本化が図られることになった。CJK-JRGは各国の漢字コードに基づき独自の統合規準を定め、ISO 10646 / Unicode用の統合漢字コード表を作成することになった。CJK-JRGの会合は第1回が7月22日から24日にかけて東京で、第2回の会合が9月17日から19日にかけて北京で、第3回が11月25日から29日にかけて香港で開催された。これらの討議の結果、1991年末になって「ISO 10646＝Unicode」用の統合漢字コード表が Unified Repertoire and Ordering (URO) の第1版として完成した。

Unicodeの最初に印刷されたドキュメントであるUnicode 1.0は、統合漢字表の完成に先行して漢字部分を除いたUnicode 1.0, Vol.1が1991年10月に出版され、後に1992年になって漢字部分だけのUnicode 1.0, Vol.2が出版された。

1992年、CJK統合漢字URO第二版が完成し、これを取り込んだ（ただし、UROには若干の間違いが発見されており、それらの修正が行われている。）DIS 10646第2版が、5月30日の国際投票で可決された。

1993年5月1日 「ISO/IEC 10646-1: 1993 Universal Multiple-Octet Coded Character Set (UCS) -- Part 1: Architecture and basic Multilingual Plane」が制定される。同年翌6月にUnicode 1.0は ISO/IEC 10646-1:1993にあわせた変更を行いUnicode 1.1となり、以後ユニコードとISO/IEC 10646とは歩調を合わせて改訂されていくことになる。

### ユニコードのバージョン

ユニコードのバージョンは、メジャーバージョン (the major version)、マイナーバージョン (the minor version)、アップデートバージョン (the update version) の3つの部分から構成され、ピリオドでつなげて表示される\[14\]。ただし、マイナーバージョン及びアップデートバージョンについては0の場合には省略して表示されることもある。メジャーバージョンはレパートリーの追加のような重要な変更が行われたときに改定される。ユニコードのドキュメントは書籍形態と電子版ドキュメント形態の両方で公表され、どちらもユニコードについての正式なドキュメントであるとされている。新たなバージョンがリリースされたときは新たなドキュメントが公表されるが、書籍として刊行されるのはメジャーバージョンが改定された場合および重要なマイナーバージョンの改定があった場合のみである。書籍版のバージョン1.0は、2巻に分けて刊行され、統合漢字部分を除いた第1巻は1991年10月に、統合漢字部分の第2巻は1992年6月に刊行された。そのため第1巻のみのものをUnicode 1.0.0、第2巻を含めたものをUnicode 1.0.1と呼ぶことがある。

### 各バージョンとその特徴

ユニコードのそれぞれのバージョン番号とその制定年月日、収録文字数他の特徴は以下の通りである。

<table>
<thead>
<tr class="header">
<th><p>制定年月日</p></th>
<th><p>バージョン番号</p></th>
<th><p>収録文字数</p></th>
<th><p>概要</p></th>
<th><p>日本語における主要な追加文字</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1991年10月</p></td>
<td><p>Unicode 1.0.0 <ref name="unicode_components_1.0.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-1.0.0.html">http://www.unicode.org/versions/components-1.0.0.html</a></p></td>
<td><p>title=Components of The Unicode Standard Version 1.0.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td><p>1992年6月</p></td>
<td><p>Unicode 1.0.1 <ref name="unicode_components_1.0.1">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-1.0.1.html">http://www.unicode.org/versions/components-1.0.1.html</a></p></td>
<td><p>title=Components of The Unicode Standard Version 1.0.1</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="odd">
<td><p>1993年6月</p></td>
<td><p>Unicode 1.1.0 <ref name="unicode_components_1.1.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-1.1.0.html">http://www.unicode.org/versions/components-1.1.0.html</a></p></td>
<td><p>title=Components of The Unicode Standard Version 1.1.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td><p>1993年7月</p></td>
<td><p>Unicode 1.1.5 <ref name="unicode_components_1.1.5">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-1.1.5.html">http://www.unicode.org/versions/components-1.1.5.html</a></p></td>
<td><p>title=Components of The Unicode Standard Version 1.1.5</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="odd">
<td><p>1996年7月</p></td>
<td><p>Unicode 2.0.0 <ref name="unicode_components_2.0.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-2.0.0.html">http://www.unicode.org/versions/components-2.0.0.html</a></p></td>
<td><p>title=Components of The Unicode Standard Version 2.0.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td><p>1998年5月</p></td>
<td><p>Unicode 2.1.0 <ref name="unicode_components_2.1.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/Unicode2.1.0/">http://www.unicode.org/versions/Unicode2.1.0/</a></p></td>
<td><p>title=Unicode 2.1.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="odd">
<td><p>1998年5月</p></td>
<td><p>Unicode 2.1.2 <ref name="unicode_components_2.1.2">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-2.1.2.html">http://www.unicode.org/versions/components-2.1.2.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 2.1.2</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td><p>1998年8月</p></td>
<td><p>Unicode 2.1.5 <ref name="unicode_components_2.1.5">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-2.1.5.html">http://www.unicode.org/versions/components-2.1.5.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 2.1.5</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="odd">
<td><p>1998年10月</p></td>
<td><p>Unicode 2.1.8 <ref name="unicode_components_2.1.8">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-2.1.8.html">http://www.unicode.org/versions/components-2.1.8.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 2.1.8</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td><p>1999年4月</p></td>
<td><p>Unicode 2.1.9 <ref name="unicode_components_2.1.9">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-2.1.9.html">http://www.unicode.org/versions/components-2.1.9.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 2.1.9</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="odd">
<td><p>1999年9月</p></td>
<td><p>Unicode 3.0.0 <ref name="unicode_components_3.0.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-3.0.0.html">http://www.unicode.org/versions/components-3.0.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 3.0.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td><p>2000年8月</p></td>
<td><p>Unicode 3.0.1 <ref name="unicode_components_3.0.1">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-3.0.1.html">http://www.unicode.org/versions/components-3.0.1.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 3.0.1</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="odd">
<td><p>2001年3月</p></td>
<td><p>Unicode 3.1.0 <ref name="unicode_components_3.1.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-3.1.0.html">http://www.unicode.org/versions/components-3.1.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 3.1.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td><p>2001年8月</p></td>
<td><p>Unicode 3.1.1 <ref name="unicode_components_3.1.1">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-3.1.1.html">http://www.unicode.org/versions/components-3.1.1.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 3.1.1</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="odd">
<td><p>2002年3月</p></td>
<td><p>Unicode 3.2.0 <ref name="unicode_components_3.2.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-3.2.0.html">http://www.unicode.org/versions/components-3.2.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 3.2.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td><p>2003年4月</p></td>
<td><p>Unicode 4.0.0 <ref name="unicode_components_4.0.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-4.0.0.html">http://www.unicode.org/versions/components-4.0.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 4.0.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="odd">
<td><p>2004年5月</p></td>
<td><p>Unicode 4.0.1 <ref name="unicode_components_4.0.1">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-4.0.1.html">http://www.unicode.org/versions/components-4.0.1.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 4.0.1</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td><p>2005年3月31日</p></td>
<td><p>Unicode 4.1.0 <ref name="unicode_components_4.1.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-4.1.0.html">http://www.unicode.org/versions/components-4.1.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 4.1.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="odd">
<td><p>2006年7月14日</p></td>
<td><p>Unicode 5.0.0 <ref name="unicode_components_5.0.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-5.0.0.html">http://www.unicode.org/versions/components-5.0.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 5.0.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/2008年" title="wikilink">2008年</a>4月4日 <ref name="unicode_components_5.1.0">{{cite web</p></td>
<td><p>Unicode Consortium]]|url=<a href="http://www.unicode.org/versions/components-5.1.0.html">http://www.unicode.org/versions/components-5.1.0.html</a></p></td>
<td><p>title=Components of The Unicode Version 5.1.0</p></td>
<td><p>accessdate=2008-04-05 }}</ref></p></td>
<td><p>Unicode 5.1.0</p></td>
</tr>
<tr class="odd">
<td><p>2009年10月1日</p></td>
<td><p>Unicode 5.2.0 <ref name="unicode_components_5.2.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-5.2.0.html">http://www.unicode.org/versions/components-5.2.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 5.2.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>Unicode 6.0.0 <ref name="unicode_components_6.0.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-6.0.0.html">http://www.unicode.org/versions/components-6.0.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 6.0.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="odd">
<td><p>2012年1月31日</p></td>
<td><p>Unicode 6.1.0 <ref name="unicode_components_6.1.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-6.1.0.html">http://www.unicode.org/versions/components-6.1.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 6.1.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td><p>2012年9月26日</p></td>
<td><p>Unicode 6.2.0 <ref name="unicode_components_6.2.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-6.2.0.html">http://www.unicode.org/versions/components-6.2.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 6.2.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="odd">
<td><p>2013年9月30日</p></td>
<td><p>Unicode 6.3.0 <ref name="unicode_components_6.3.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-6.3.0.html">http://www.unicode.org/versions/components-6.3.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 6.3.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td><p>2014年6月16日</p></td>
<td><p>Unicode 7.0.0 <ref name="unicode_components_7.0.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-7.0.0.html">http://www.unicode.org/versions/components-7.0.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 7.0.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="odd">
<td><p>2015年6月17日</p></td>
<td><p>Unicode 8.0.0 <ref name="unicode_components_8.0.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-8.0.0.html">http://www.unicode.org/versions/components-8.0.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 8.0.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td><p>2016年6月21日</p></td>
<td><p>Unicode 9.0.0 <ref name="unicode_components_9.0.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-9.0.0.html">http://www.unicode.org/versions/components-9.0.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 9.0.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="odd">
<td><p>2017年6月20日</p></td>
<td><p><ref name="unicode_components_10.0.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-10.0.0.html">http://www.unicode.org/versions/components-10.0.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 10.0.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td><p>2018年6月5日</p></td>
<td><p>{{nowrap|Unicode 11.0.0 <ref name="unicode_components_11.0.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-11.0.0.html">http://www.unicode.org/versions/components-11.0.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 11.0.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="odd">
<td><p>2019年3月5日</p></td>
<td><p>Unicode 12.0.0 <ref name="unicode_components_12.0.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-12.0.0.html">http://www.unicode.org/versions/components-12.0.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 12.0.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td><p>2019年5月7日</p></td>
<td><p>Unicode 12.1.0 <ref name="unicode_components_12.1.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-12.1.0.html">http://www.unicode.org/versions/components-12.1.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 12.1.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="odd">
<td><p>2020年3月10日</p></td>
<td><p>Unicode 13.0.0 <ref name="unicode_components_13.0.0">{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/versions/components-13.0.0.html">http://www.unicode.org/versions/components-13.0.0.html</a></p></td>
<td><p>title= Components of The Unicode Standard Version 13.0.0</p></td>
<td><p>publisher= Unicode Consortium</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### 構成要素のバージョン

ユニコードのバージョンには、上記のような「ユニコードの規格全体に付けられたバージョン」の他に「ユニコードを構成する個々の要素の規格に付けられたバージョン」が存在する。これに該当するものとしては、ユニコードを構成する各面ごとに付けられたバージョンや、ユニコードに収録されないこととされたスクリプトのリスト (NOR = Not The Roadmap) に付けられたバージョン、規格の一部を構成するUnicode Technical Note（Unicode技術ノート）、Unicode Technical Report（Unicode技術報告）、Unicode Technical Standard（Unicode技術標準）のバージョンなどが存在する。

<table>
<thead>
<tr class="header">
<th><p>日付</p></th>
<th><p>全体<ref>{{Cite web</p></th>
<th><p>url=<a href="http://www.unicode.org/versions/enumeratedversions.html">http://www.unicode.org/versions/enumeratedversions.html</a></p></th>
<th><p>title=Enumerated Versions of The Unicode Standard</p></th>
<th><p>publisher= Unicode Consortium</p></th>
<th><p>language=English</p></th>
<th><p>date=2017-06-20</p></th>
<th><p>accessdate=2017-07-22 }}</ref></p></th>
<th><p><a href="../Page/基本多言語面.md" title="wikilink">BMP</a><ref>{{Cite web</p></th>
<th><p>url=<a href="http://www.unicode.org/roadmaps/bmp/index.html">http://www.unicode.org/roadmaps/bmp/index.html</a></p></th>
<th><p>title=Roadmap to the BMP</p></th>
<th><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></th>
<th><p>publisher= Unicode Consortium</p></th>
<th><p>language=English</p></th>
<th><p>date=2017-06-21</p></th>
<th><p>accessdate=2017-07-22 }}</ref></p></th>
<th><p><a href="../Page/追加多言語面.md" title="wikilink">SMP</a><ref>{{Cite web</p></th>
<th><p>url=<a href="http://www.unicode.org/roadmaps/smp/">http://www.unicode.org/roadmaps/smp/</a></p></th>
<th><p>title=Roadmap to the SMP</p></th>
<th><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></th>
<th><p>publisher= Unicode Consortium</p></th>
<th><p>language=English</p></th>
<th><p>date=2018-01-10</p></th>
<th><p>accessdate=2018-01-14 }}</ref></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/追加漢字面" title="wikilink">SIP</a><ref>{{Cite web</p></th>
<th><p>url=<a href="http://www.unicode.org/roadmaps/sip/">http://www.unicode.org/roadmaps/sip/</a></p></th>
<th><p>title=Roadmap to the SIP</p></th>
<th><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></th>
<th><p>publisher= Unicode Consortium</p></th>
<th><p>language=English</p></th>
<th><p>date=2017-06-21</p></th>
<th><p>accessdate=2017-07-22 }}</ref></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/第三漢字面" title="wikilink">TIP</a><ref>{{Cite web</p></th>
<th><p>url=<a href="http://www.unicode.org/roadmaps/tip/">http://www.unicode.org/roadmaps/tip/</a></p></th>
<th><p>title=Roadmap to the TIP</p></th>
<th><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></th>
<th><p>publisher= Unicode Consortium</p></th>
<th><p>language=English</p></th>
<th><p>date=2017-12-27</p></th>
<th><p>accessdate=2018-01-01 }}</ref></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/追加特殊用途面" title="wikilink">SSP</a><ref>{{Cite web</p></th>
<th><p>url=<a href="http://www.unicode.org/roadmaps/ssp/">http://www.unicode.org/roadmaps/ssp/</a></p></th>
<th><p>title=Roadmap to the SSP</p></th>
<th><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></th>
<th><p>publisher= Unicode Consortium</p></th>
<th><p>language=English</p></th>
<th><p>date=2017-06-21</p></th>
<th><p>accessdate=2017-07-22 }}</ref></p></th>
<th><p>NOR<ref>{{Cite web</p></th>
<th><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/">http://www.unicode.org/roadmaps/not-the-roadmap/</a></p></th>
<th><p>title=Roadmap to the NOR</p></th>
<th><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></th>
<th><p>publisher= Unicode Consortium</p></th>
<th><p>language=English</p></th>
<th><p>date=2017-06-21</p></th>
<th><p>accessdate=2017-07-22 }}</ref></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1991年10月</p></td>
<td><p>1.0.0[15]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>1992年6月</p></td>
<td><p>1.0.1[16]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1993年6月</p></td>
<td><p>1.1.0[17]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>1993年7月</p></td>
<td><p>1.1.5[18]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1996年7月</p></td>
<td><p>2.0.0[19]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>1998年5月</p></td>
<td><p>2.1.0[20]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1998年5月</p></td>
<td><p>2.1.2[21]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>1998年8月</p></td>
<td><p>2.1.5[22]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1998年10月</p></td>
<td><p>2.1.8[23]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>1999年4月</p></td>
<td><p>2.1.9[24]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1999年9月</p></td>
<td><p>3.0.0[25]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2000年8月</p></td>
<td><p>3.0.1[26]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2001年3月</p></td>
<td><p>3.1.0[27]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2001年8月</p></td>
<td><p>3.1.1[28]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2001年10月10日</p></td>
<td></td>
<td><p>3.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-3-0.html">http://www.unicode.org/roadmaps/bmp/bmp-3-0.html</a></p></td>
<td><p>title=Roadmap to the BMP 3.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2001-10-10</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>3.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-3-0.html">http://www.unicode.org/roadmaps/smp/smp-3-0.html</a></p></td>
<td><p>title=Roadmap to the SMP 3.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2001-10-10</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>3.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-3-0.html">http://www.unicode.org/roadmaps/sip/sip-3-0.html</a></p></td>
<td><p>title=Roadmap to the SIP 3.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2001-10-10</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td></td>
<td></td>
<td><p>1.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-1-0.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-1-0.html</a></p></td>
<td><p>title=Roadmap to the NOR 1.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2001-10-10</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2001年10月12日</p></td>
<td></td>
<td></td>
<td><p>3.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-3-1.html">http://www.unicode.org/roadmaps/smp/smp-3-1.html</a></p></td>
<td><p>title=Roadmap to the SMP 3.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2001-10-12</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2001年10月27日</p></td>
<td></td>
<td><p>3.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-3-1.html">http://www.unicode.org/roadmaps/bmp/bmp-3-1.html</a></p></td>
<td><p>title=Roadmap to the BMP 3.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2001-10-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2001年11月27日</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>3.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/ssp/ssp-3-0.html">http://www.unicode.org/roadmaps/ssp/ssp-3-0.html</a></p></td>
<td><p>title=Roadmap to the SSP 3.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2001-11-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2002年1月22日</p></td>
<td></td>
<td><p>3.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-3-2.html">http://www.unicode.org/roadmaps/bmp/bmp-3-2.html</a></p></td>
<td><p>title=Roadmap to the BMP 3.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2002-01-22</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td></td>
<td></td>
<td></td>
<td><p>3.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/ssp/ssp-3-1.html">http://www.unicode.org/roadmaps/ssp/ssp-3-1.html</a></p></td>
<td><p>title=Roadmap to the SSP 3.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2002-01-22</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
</tr>
<tr class="even">
<td><p>2002年1月29日</p></td>
<td></td>
<td><p>3.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-3-3.html">http://www.unicode.org/roadmaps/bmp/bmp-3-3.html</a></p></td>
<td><p>title=Roadmap to the BMP 3.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2002-01-29</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2002年2月5日</p></td>
<td></td>
<td><p>3.4<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-3-4.html">http://www.unicode.org/roadmaps/bmp/bmp-3-4.html</a></p></td>
<td><p>title=Roadmap to the BMP 3.4</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2002-02-05</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2002年3月</p></td>
<td><p>3.2.0[29]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2002年4月3日</p></td>
<td></td>
<td></td>
<td><p>3.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-3-2.html">http://www.unicode.org/roadmaps/smp/smp-3-2.html</a></p></td>
<td><p>title=Roadmap to the SMP 3.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2002-04-03</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2002年4月4日</p></td>
<td></td>
<td><p>3.5<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-3-5.html">http://www.unicode.org/roadmaps/bmp/bmp-3-5.html</a></p></td>
<td><p>title=Roadmap to the BMP 3.5</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2002-04-04</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2002年6月7日</p></td>
<td></td>
<td><p>3.6<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-3-6.html">http://www.unicode.org/roadmaps/bmp/bmp-3-6.html</a></p></td>
<td><p>title=Roadmap to the BMP 3.6</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2002-06-07</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>3.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-3-3.html">http://www.unicode.org/roadmaps/smp/smp-3-3.html</a></p></td>
<td><p>title=Roadmap to the SMP 3.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2002-06-07</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2002年6月23日</p></td>
<td></td>
<td><p>3.7<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-3-7.html">http://www.unicode.org/roadmaps/bmp/bmp-3-7.html</a></p></td>
<td><p>title=Roadmap to the BMP 3.7</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2002-06-23</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2002年10月2日</p></td>
<td></td>
<td><p>3.8<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-3-8.html">http://www.unicode.org/roadmaps/bmp/bmp-3-8.html</a></p></td>
<td><p>title=Roadmap to the BMP 3.8</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2002-10-02</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2002年10月28日</p></td>
<td></td>
<td><p>3.9<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-3-9.html">http://www.unicode.org/roadmaps/bmp/bmp-3-9.html</a></p></td>
<td><p>title=Roadmap to the BMP 3.9</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2002-10-28</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2002年11月11日</p></td>
<td></td>
<td></td>
<td></td>
<td><p>3.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-3-1.html">http://www.unicode.org/roadmaps/sip/sip-3-1.html</a></p></td>
<td><p>title=Roadmap to the SIP 3.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2002-11-11</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2002年12月3日</p></td>
<td></td>
<td><p>3.10<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-3-10.html">http://www.unicode.org/roadmaps/bmp/bmp-3-10.html</a></p></td>
<td><p>title=Roadmap to the BMP 3.10</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2002-12-03</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>3.4<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-3-4.html">http://www.unicode.org/roadmaps/smp/smp-3-4.html</a></p></td>
<td><p>title=Roadmap to the SMP 3.4</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2002-12-03</p></td>
<td><p>accessdate=2012-05-05 }}</ref><br />
3.5<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-3-5.html">http://www.unicode.org/roadmaps/smp/smp-3-5.html</a></p></td>
<td><p>title=Roadmap to the SMP 3.5</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2002-12-03</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2002年12月11日</p></td>
<td></td>
<td><p>3.11<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-3-11.html">http://www.unicode.org/roadmaps/bmp/bmp-3-11.html</a></p></td>
<td><p>title=Roadmap to the BMP 3.11</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2002-12-11</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2003年3月12日</p></td>
<td></td>
<td><p>3.12<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-3-12.html">http://www.unicode.org/roadmaps/bmp/bmp-3-12.html</a></p></td>
<td><p>title=Roadmap to the BMP 3.12</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-03-12</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>3.6<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-3-6.html">http://www.unicode.org/roadmaps/smp/smp-3-6.html</a></p></td>
<td><p>title=Roadmap to the SMP 3.6</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-03-12</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2003年3月15日</p></td>
<td></td>
<td></td>
<td><p>3.7<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-3-7.html">http://www.unicode.org/roadmaps/smp/smp-3-7.html</a></p></td>
<td><p>title=Roadmap to the SMP 3.7</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-03-15</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2003年4月</p></td>
<td><p>4.0.0[30]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2003年4月16日</p></td>
<td></td>
<td><p>4.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-0.html">http://www.unicode.org/roadmaps/bmp/bmp-4-0.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-04-16</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-0.html">http://www.unicode.org/roadmaps/smp/smp-4-0.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-04-16</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-4-0.html">http://www.unicode.org/roadmaps/sip/sip-4-0.html</a></p></td>
<td><p>title=Roadmap to the SIP 4.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-04-16</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td></td>
<td><p>4.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/ssp/ssp-4-0.html">http://www.unicode.org/roadmaps/ssp/ssp-4-0.html</a></p></td>
<td><p>title=Roadmap to the SSP 4.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-04-16</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-4-0.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-4-0.html</a></p></td>
<td><p>title=Roadmap to the NOR 4.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-04-16</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2003年5月4日</p></td>
<td></td>
<td><p>4.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-1.html">http://www.unicode.org/roadmaps/bmp/bmp-4-1.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-05-04</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2003年5月16日</p></td>
<td></td>
<td></td>
<td></td>
<td><p>4.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-4-1.html">http://www.unicode.org/roadmaps/sip/sip-4-1.html</a></p></td>
<td><p>title=Roadmap to the SIP 4.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-05-16</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2003年6月18日</p></td>
<td></td>
<td><p>4.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-2.html">http://www.unicode.org/roadmaps/bmp/bmp-4-2.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-06-18</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-1.html">http://www.unicode.org/roadmaps/smp/smp-4-1.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-06-18</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2003年7月15日</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>4.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/ssp/ssp-4-1.html">http://www.unicode.org/roadmaps/ssp/ssp-4-1.html</a></p></td>
<td><p>title=Roadmap to the SSP 4.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-07-15</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2003年8月19日</p></td>
<td></td>
<td><p>4.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-3.html">http://www.unicode.org/roadmaps/bmp/bmp-4-3.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-08-19</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2003年9月11日</p></td>
<td></td>
<td><p>4.4<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-4.html">http://www.unicode.org/roadmaps/bmp/bmp-4-4.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.4</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-09-11</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-2.html">http://www.unicode.org/roadmaps/smp/smp-4-2.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-09-11</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2003年9月20日</p></td>
<td></td>
<td><p>4.5<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-5.html">http://www.unicode.org/roadmaps/bmp/bmp-4-5.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.5</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-09-20</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2003年10月22日</p></td>
<td></td>
<td><p>4.6<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-6.html">http://www.unicode.org/roadmaps/bmp/bmp-4-6.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.6</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-10-22</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2003年10月31日</p></td>
<td></td>
<td></td>
<td><p>4.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-3.html">http://www.unicode.org/roadmaps/smp/smp-4-3.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-10-31</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2003年12月23日</p></td>
<td></td>
<td><p>4.7<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-7.html">http://www.unicode.org/roadmaps/bmp/bmp-4-7.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.7</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-12-23</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.4<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-4.html">http://www.unicode.org/roadmaps/smp/smp-4-4.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.4</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2003-12-23</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2004年5月</p></td>
<td><p>4.0.1[31]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2004年5月27日</p></td>
<td></td>
<td></td>
<td><p>4.5<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-5.html">http://www.unicode.org/roadmaps/smp/smp-4-5.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.5</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2004-05-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2004年6月24日</p></td>
<td></td>
<td><p>4.8<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-8.html">http://www.unicode.org/roadmaps/bmp/bmp-4-8.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.8</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2004-06-24</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.6<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-6.html">http://www.unicode.org/roadmaps/smp/smp-4-6.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.6</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2004-06-24</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2004年7月3日</p></td>
<td></td>
<td></td>
<td><p>4.7<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-7.html">http://www.unicode.org/roadmaps/smp/smp-4-7.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.7</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2004-07-03</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2004年12月1日</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>4.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-4-1.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-4-1.html</a></p></td>
<td><p>title=Roadmap to the NOR 4.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2004-12-01</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2005年1月27日</p></td>
<td></td>
<td></td>
<td></td>
<td><p>4.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-4-2.html">http://www.unicode.org/roadmaps/sip/sip-4-2.html</a></p></td>
<td><p>title=Roadmap to the SIP 4.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-01-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2005年1月28日</p></td>
<td></td>
<td><p>4.9<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-9.html">http://www.unicode.org/roadmaps/bmp/bmp-4-9.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.9</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-01-28</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.8<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-8.html">http://www.unicode.org/roadmaps/smp/smp-4-8.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.8</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-01-28</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2005年3月31日</p></td>
<td><p>4.1.0[32]</p></td>
<td><p>4.10<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-10.html">http://www.unicode.org/roadmaps/bmp/bmp-4-10.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.10</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-03-31</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.9<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-9.html">http://www.unicode.org/roadmaps/smp/smp-4-9.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.9</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-03-31</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2005年5月27日</p></td>
<td></td>
<td></td>
<td><p>4.10<ref>[{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-10.html">http://www.unicode.org/roadmaps/smp/smp-4-10.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.10</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-05-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td></td>
<td></td>
<td></td>
<td><p>4.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-4-2.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-4-2.html</a></p></td>
<td><p>title=Roadmap to the NOR 4.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-05-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2005年6月10日</p></td>
<td></td>
<td><p>4.11<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-11.html">http://www.unicode.org/roadmaps/bmp/bmp-4-11.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.11</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-06-10</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.11<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-11.html">http://www.unicode.org/roadmaps/smp/smp-4-11.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.11</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-06-10</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2005年6月27日</p></td>
<td></td>
<td><p>4.12<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-12.html">http://www.unicode.org/roadmaps/bmp/bmp-4-12.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.12</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-06-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.12<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-12.html">http://www.unicode.org/roadmaps/smp/smp-4-12.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.12</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-06-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-4-3.html">http://www.unicode.org/roadmaps/sip/sip-4-3.html</a></p></td>
<td><p>title=Roadmap to the SIP 4.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-06-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td></td>
<td><p>4.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/ssp-4-2.html">http://www.unicode.org/roadmaps/sip/ssp-4-2.html</a></p></td>
<td><p>title=Roadmap to the SSP 4.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-06-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-4-3.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-4-3.html</a></p></td>
<td><p>title=Roadmap to the NOR 4.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-06-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2005年8月1日</p></td>
<td></td>
<td><p>4.13<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-13.html">http://www.unicode.org/roadmaps/bmp/bmp-4-13.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.13</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-08-01</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.13<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-13.html">http://www.unicode.org/roadmaps/smp/smp-4-13.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.13</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-08-01</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2005年9月6日</p></td>
<td></td>
<td><p>4.14<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-14.html">http://www.unicode.org/roadmaps/bmp/bmp-4-14.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.14</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-09-06</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2005年9月14日</p></td>
<td></td>
<td><p>4.15<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-15.html">http://www.unicode.org/roadmaps/bmp/bmp-4-15.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.15</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-09-14</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2005年9月17日</p></td>
<td></td>
<td></td>
<td><p>4.14<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-14.html">http://www.unicode.org/roadmaps/smp/smp-4-14.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.14</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-09-17</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2005年9月19日</p></td>
<td></td>
<td><p>4.16<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-16.html">http://www.unicode.org/roadmaps/bmp/bmp-4-16.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.16</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-09-19</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2005年12月8日</p></td>
<td></td>
<td></td>
<td><p>4.15<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-15.html">http://www.unicode.org/roadmaps/smp/smp-4-15.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.15</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2005-12-08</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2006年1月11日</p></td>
<td></td>
<td><p>4.17<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-17.html">http://www.unicode.org/roadmaps/bmp/bmp-4-17.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.17</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2006-01-11</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.16<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/smp-4-16.html">http://www.unicode.org/roadmaps/bmp/smp-4-16.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.16</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2006-01-11</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2006年4月17日</p></td>
<td></td>
<td><p>4.18<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-4-18.html">http://www.unicode.org/roadmaps/bmp/bmp-4-18.html</a></p></td>
<td><p>title=Roadmap to the BMP 4.18</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2006-04-17</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.17<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-4-17.html">http://www.unicode.org/roadmaps/smp/smp-4-17.html</a></p></td>
<td><p>title=Roadmap to the SMP 4.17</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2006-04-17</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>4.4<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-4-4.html">http://www.unicode.org/roadmaps/sip/sip-4-4.html</a></p></td>
<td><p>title=Roadmap to the SIP 4.4</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2006-04-17</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2006年4月28日</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>4.4<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-4-4.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-4-4.html</a></p></td>
<td><p>title=Roadmap to the NOR 4.4</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2006-04-28</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2006年7月14日</p></td>
<td><p>5.0.0[33]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2006年9月21日</p></td>
<td></td>
<td><p>5.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-0.html">http://www.unicode.org/roadmaps/bmp/bmp-5-0.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2006-09-21</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-0.html">http://www.unicode.org/roadmaps/smp/smp-5-0.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2006-09-21</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-5-0.html">http://www.unicode.org/roadmaps/sip/sip-5-0.html</a></p></td>
<td><p>title=Roadmap to the SIP 5.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2006-09-21</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td></td>
<td><p>5.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/ssp/ssp-5-0.html">http://www.unicode.org/roadmaps/ssp/ssp-5-0.html</a></p></td>
<td><p>title=Roadmap to the SSP 5.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2006-09-21</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-5-0.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-5-0.html</a></p></td>
<td><p>title=Roadmap to the NOR 5.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2006-09-21</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2006年9月29日</p></td>
<td></td>
<td><p>5.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-0-1.html">http://www.unicode.org/roadmaps/bmp/bmp-5-0-1.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2006-09-29</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td></td>
<td><p>5.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-5-0-1.html">http://www.unicode.org/roadmaps/sip/sip-5-0-1.html</a></p></td>
<td><p>title=Roadmap to the SIP 5.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2006-09-29</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2007年3月14日</p></td>
<td></td>
<td></td>
<td><p>5.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-0-1.html">http://www.unicode.org/roadmaps/smp/smp-5-0-1.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2007-03-14</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2007年4月11日</p></td>
<td></td>
<td><p>5.0.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-0-2.html">http://www.unicode.org/roadmaps/bmp/bmp-5-0-2.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.0.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2007-04-11</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.0.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-0-2.html">http://www.unicode.org/roadmaps/smp/smp-5-0-2.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.0.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2007-04-11</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2007年5月5日</p></td>
<td></td>
<td><p>5.0.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-0-3.html">http://www.unicode.org/roadmaps/bmp/bmp-5-0-3.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.0.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2007-05-05</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.0.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-0-3.html">http://www.unicode.org/roadmaps/smp/smp-5-0-3.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.0.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2007-05-05</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2007年7月24日</p></td>
<td></td>
<td><p>5.0.4<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-0-4.html">http://www.unicode.org/roadmaps/bmp/bmp-5-0-4.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.0.4</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2007-07-24</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.0.4<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-0-4.html">http://www.unicode.org/roadmaps/smp/smp-5-0-4.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.0.4</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2007-07-24</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td></td>
<td></td>
<td></td>
<td><p>5.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-5-0-1.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-5-0-1.html</a></p></td>
<td><p>title=Roadmap to the NOR 5.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2007-07-24</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2007年8月22日</p></td>
<td></td>
<td><p>5.0.5<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-0-5.html">http://www.unicode.org/roadmaps/bmp/bmp-5-0-5.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.0.5</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2007-08-22</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2007年8月29日</p></td>
<td></td>
<td></td>
<td><p>5.0.5<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-0-5.html">http://www.unicode.org/roadmaps/smp/smp-5-0-5.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.0.5</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2007-08-29</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2008年1月15日</p></td>
<td></td>
<td></td>
<td><p>5.0.6<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-0-6.html">http://www.unicode.org/roadmaps/smp/smp-5-0-6.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.0.6</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-01-15</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2008年1月31日</p></td>
<td></td>
<td><p>5.0.6<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-0-6.html">http://www.unicode.org/roadmaps/bmp/bmp-5-0-6.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.0.6</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-01-31</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2008年2月14日</p></td>
<td></td>
<td><p>5.0.7<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-0-7.html">http://www.unicode.org/roadmaps/bmp/bmp-5-0-7.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.0.7</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-02-14</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.0.7<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-0-7.html">http://www.unicode.org/roadmaps/smp/smp-5-0-7.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.0.7</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-02-14</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2008年4月4日</p></td>
<td><p>5.1.0[34]</p></td>
<td><p>5.1.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-1-0.html">http://www.unicode.org/roadmaps/bmp/bmp-5-1-0.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.1.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-04-04</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.1.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-1-0.html">http://www.unicode.org/roadmaps/smp/smp-5-1-0.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.1.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-04-04</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.1.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-5-1-0.html">http://www.unicode.org/roadmaps/sip/sip-5-1-0.html</a></p></td>
<td><p>title=Roadmap to the SIP 5.1.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-04-04</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td></td>
<td><p>5.1.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/ssp/ssp-5-1-0.html">http://www.unicode.org/roadmaps/ssp/ssp-5-1-0.html</a></p></td>
<td><p>title=Roadmap to the SSP 5.1.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-04-04</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.1.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-5-1-0.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-5-1-0.html</a></p></td>
<td><p>title=Roadmap to the NOR 5.1.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-04-04</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2008年4月25日</p></td>
<td></td>
<td><p>5.1.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-1-1.html">http://www.unicode.org/roadmaps/bmp/bmp-5-1-1.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.1.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-04-25</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.1.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-1-1.html">http://www.unicode.org/roadmaps/smp/smp-5-1-1.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.1.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-04-25</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td></td>
<td><p>5.1.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/tip/tip-5-1-0.html">http://www.unicode.org/roadmaps/tip/tip-5-1-0.html</a></p></td>
<td><p>title=Roadmap to the TIP 5.1.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-04-25</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td></td>
<td><p>5.1.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-5-1-1.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-5-1-1.html</a></p></td>
<td><p>title=Roadmap to the NOR 5.1.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-04-25</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2008年8月12日</p></td>
<td></td>
<td><p>5.1.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-1-2.html">http://www.unicode.org/roadmaps/bmp/bmp-5-1-2.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.1.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-08-12</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.1.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-1-2.html">http://www.unicode.org/roadmaps/smp/smp-5-1-2.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.1.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-08-12</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2008年8月19日</p></td>
<td></td>
<td><p>5.1.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-1-3.html">http://www.unicode.org/roadmaps/bmp/bmp-5-1-3.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.1.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-08-19</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2008年10月17日</p></td>
<td></td>
<td><p>5.1.4<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-1-4.html">http://www.unicode.org/roadmaps/bmp/bmp-5-1-4.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.1.4</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-10-17</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.1.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-1-3.html">http://www.unicode.org/roadmaps/smp/smp-5-1-3.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.1.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-10-17</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td></td>
<td><p>5.1.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/tip/tip-5-1-1.html">http://www.unicode.org/roadmaps/tip/tip-5-1-1.html</a></p></td>
<td><p>title=Roadmap to the TIP 5.1.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2008-10-17</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2009年2月4日</p></td>
<td></td>
<td><p>5.1.5<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-1-5.html">http://www.unicode.org/roadmaps/bmp/bmp-5-1-5.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.1.5</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2009-02-04</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.1.4<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-1-4.html">http://www.unicode.org/roadmaps/smp/smp-5-1-4.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.1.4</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2009-02-04</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2009年2月26日</p></td>
<td></td>
<td></td>
<td></td>
<td><p>5.1.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-5-1-1.html">http://www.unicode.org/roadmaps/sip/sip-5-1-1.html</a></p></td>
<td><p>title=Roadmap to the SIP 5.1.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2009-02-26</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2009年4月22日</p></td>
<td></td>
<td></td>
<td></td>
<td><p>5.1.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-5-1-2.html">http://www.unicode.org/roadmaps/sip/sip-5-1-2.html</a></p></td>
<td><p>title=Roadmap to the SIP 5.1.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2009-04-22</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2009年4月24日</p></td>
<td></td>
<td></td>
<td><p>5.1.5<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-1-5.html">http://www.unicode.org/roadmaps/smp/smp-5-1-5.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.1.5</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2009-04-24</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2009年10月1日</p></td>
<td><p>5.2.0[35]</p></td>
<td><p>5.2.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-2-0.html">http://www.unicode.org/roadmaps/bmp/bmp-5-2-0.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.2.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2009-10-01</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.2.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-2-0.html">http://www.unicode.org/roadmaps/smp/smp-5-2-0.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.2.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2009-10-01</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.2.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-5-2-0.html">http://www.unicode.org/roadmaps/sip/sip-5-2-0.html</a></p></td>
<td><p>title=Roadmap to the SIP 5.2.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2009-10-01</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.2.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/tip/tip-5-2-0.html">http://www.unicode.org/roadmaps/tip/tip-5-2-0.html</a></p></td>
<td><p>title=Roadmap to the TIP 5.2.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2009-10-01</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.2.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/ssp/ssp-5-2-0.html">http://www.unicode.org/roadmaps/ssp/ssp-5-2-0.html</a></p></td>
<td><p>title=Roadmap to the SSP 5.2.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2009-10-01</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.2.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-5-2-0.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-5-2-0.html</a></p></td>
<td><p>title=Roadmap to the NOR 5.2.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2009-10-01</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2009年11月18日</p></td>
<td></td>
<td><p>5.2.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-2-1.html">http://www.unicode.org/roadmaps/bmp/bmp-5-2-1.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.2.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2009-11-18</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2010年2月5日</p></td>
<td></td>
<td></td>
<td><p>5.2.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-2-1.html">http://www.unicode.org/roadmaps/smp/smp-5-2-1.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.2.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2010-02-05</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2010年2月10日</p></td>
<td></td>
<td></td>
<td><p>5.2.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-2-2.html">http://www.unicode.org/roadmaps/smp/smp-5-2-2.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.2.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2010-02-10</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2010年2月23日</p></td>
<td></td>
<td></td>
<td><p>5.2.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-2-3.html">http://www.unicode.org/roadmaps/smp/smp-5-2-3.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.2.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2010-02-23</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2010年4月23日</p></td>
<td></td>
<td><p>5.2.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-5-2-2.html">http://www.unicode.org/roadmaps/bmp/bmp-5-2-2.html</a></p></td>
<td><p>title=Roadmap to the BMP 5.2.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2010-04-23</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>5.2.4<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-2-4.html">http://www.unicode.org/roadmaps/smp/smp-5-2-4.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.2.4</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2010-04-23</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2010年5月12日</p></td>
<td></td>
<td></td>
<td><p>5.2.5<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-2-5.html">http://www.unicode.org/roadmaps/smp/smp-5-2-5.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.2.5</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2010-05-12</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2010年6月24日</p></td>
<td></td>
<td></td>
<td><p>5.2.6<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-2-6.html">http://www.unicode.org/roadmaps/smp/smp-5-2-6.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.2.6</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2010-06-24</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2010年7月27日</p></td>
<td></td>
<td></td>
<td><p>5.2.7<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-5-2-7.html">http://www.unicode.org/roadmaps/smp/smp-5-2-7.html</a></p></td>
<td><p>title=Roadmap to the SMP 5.2.7</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2010-07-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2010年10月11日</p></td>
<td><p>6.0.0[36]</p></td>
<td><p>6.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-6-0-0.html">http://www.unicode.org/roadmaps/bmp/bmp-6-0-0.html</a></p></td>
<td><p>title=Roadmap to the BMP 6.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2010-10-11</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>6.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-0-0.html">http://www.unicode.org/roadmaps/smp/smp-6-0-0.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2010-10-11</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>6.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-6-0-0.html">http://www.unicode.org/roadmaps/sip/sip-6-0-0.html</a></p></td>
<td><p>title=Roadmap to the SIP 6.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2010-10-11</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>6.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/tip/tip-6-0-0.html">http://www.unicode.org/roadmaps/tip/tip-6-0-0.html</a></p></td>
<td><p>title=Roadmap to the TIP 6.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2010-10-11</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>6.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/ssp/ssp-6-0-0.html">http://www.unicode.org/roadmaps/ssp/ssp-6-0-0.html</a></p></td>
<td><p>title=Roadmap to the SSP 6.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2010-10-11</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>6.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-6-0-0.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-6-0-0.html</a></p></td>
<td><p>title=Roadmap to the NOR 6.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2010-10-11</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2010年12月6日</p></td>
<td></td>
<td></td>
<td><p>6.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-0-1.html">http://www.unicode.org/roadmaps/smp/smp-6-0-1.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2010-12-06</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2011年1月9日</p></td>
<td></td>
<td></td>
<td><p>6.0.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-0-2.html">http://www.unicode.org/roadmaps/smp/smp-6-0-2.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.0.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-01-09</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2011年1月14日</p></td>
<td></td>
<td><p>6.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-6-0-1.html">http://www.unicode.org/roadmaps/bmp/bmp-6-0-1.html</a></p></td>
<td><p>title=Roadmap to the BMP 6.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-01-14</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2011年1月27日</p></td>
<td></td>
<td><p>6.0.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-6-0-2.html">http://www.unicode.org/roadmaps/bmp/bmp-6-0-2.html</a></p></td>
<td><p>title=Roadmap to the BMP 6.0.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-01-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>6.0.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-0-3.html">http://www.unicode.org/roadmaps/smp/smp-6-0-3.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.0.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-01-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>6.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-6-0-1.html">http://www.unicode.org/roadmaps/sip/sip-6-0-1.html</a></p></td>
<td><p>title=Roadmap to the SIP 6.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-01-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>6.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/tip/tip-6-0-1.html">http://www.unicode.org/roadmaps/tip/tip-6-0-1.html</a></p></td>
<td><p>title=Roadmap to the TIP 6.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-01-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>6.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/ssp/ssp-6-0-1.html">http://www.unicode.org/roadmaps/ssp/ssp-6-0-1.html</a></p></td>
<td><p>title=Roadmap to the SSP 6.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-01-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>6.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-6-0-1.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-6-0-1.html</a></p></td>
<td><p>title=Roadmap to the NOR 6.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-01-27</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2011年3月18日</p></td>
<td></td>
<td></td>
<td><p>6.0.4<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-0-4.html">http://www.unicode.org/roadmaps/smp/smp-6-0-4.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.0.4</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-03-18</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2011年5月24日</p></td>
<td></td>
<td></td>
<td><p>6.0.5<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-0-5.html">http://www.unicode.org/roadmaps/smp/smp-6-0-5.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.0.5</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-05-24</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2011年6月23日</p></td>
<td></td>
<td><p>6.0.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-6-0-3.html">http://www.unicode.org/roadmaps/bmp/bmp-6-0-3.html</a></p></td>
<td><p>title=Roadmap to the BMP 6.0.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-06-23</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>6.0.6<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-0-6.html">http://www.unicode.org/roadmaps/smp/smp-6-0-6.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.0.6</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-06-23</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2011年8月1日</p></td>
<td></td>
<td></td>
<td><p>6.0.7<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-0-7.html">http://www.unicode.org/roadmaps/smp/smp-6-0-7.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.0.7</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-08-01</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2011年8月15日</p></td>
<td></td>
<td></td>
<td><p>6.0.8<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-0-8.html">http://www.unicode.org/roadmaps/smp/smp-6-0-8.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.0.8</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-08-15</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2011年8月24日</p></td>
<td></td>
<td></td>
<td><p>6.0.9<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-0-9.html">http://www.unicode.org/roadmaps/smp/smp-6-0-9.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.0.9</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-08-24</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2011年11月15日</p></td>
<td></td>
<td></td>
<td><p>6.0.10<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-0-10.html">http://www.unicode.org/roadmaps/smp/smp-6-0-10.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.0.10</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-11-15</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2011年11月29日</p></td>
<td></td>
<td></td>
<td><p>6.0.11<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-0-11.html">http://www.unicode.org/roadmaps/smp/smp-6-0-11.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.0.11</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-11-29</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2011年12月19日</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>6.0.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-6-0-2.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-6-0-2.html</a></p></td>
<td><p>title=Roadmap to the NOR 6.0.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2011-12-19</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2012年1月6日</p></td>
<td></td>
<td></td>
<td><p>6.0.12<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-0-12.html">http://www.unicode.org/roadmaps/smp/smp-6-0-12.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.0.12</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-01-06</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2012年1月31日</p></td>
<td><p>6.1.0[37]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2012年2月1日</p></td>
<td></td>
<td><p>6.1.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-6-1-0.html">http://www.unicode.org/roadmaps/bmp/bmp-6-1-0.html</a></p></td>
<td><p>title=Roadmap to the BMP 6.1.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-02-01</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>6.1.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-1-0.html">http://www.unicode.org/roadmaps/smp/smp-6-1-0.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.1.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-02-01</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>6.1.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-6-1-0.html">http://www.unicode.org/roadmaps/sip/sip-6-1-0.html</a></p></td>
<td><p>title=Roadmap to the SIP 6.1.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-02-01</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>6.1.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/tip/tip-6-1-0.html">http://www.unicode.org/roadmaps/tip/tip-6-1-0.html</a></p></td>
<td><p>title=Roadmap to the TIP 6.1.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-02-01</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>6.1.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/ssp/ssp-6-1-0.html">http://www.unicode.org/roadmaps/ssp/ssp-6-1-0.html</a></p></td>
<td><p>title=Roadmap to the SSP 6.1.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-02-01</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td><p>6.1.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-6-1-0.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-6-1-0.html</a></p></td>
<td><p>title=Roadmap to the NOR 6.1.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-02-01</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2012年2月15日</p></td>
<td></td>
<td></td>
<td><p>6.1.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-1-1.html">http://www.unicode.org/roadmaps/smp/smp-6-1-1.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.1.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-02-15</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2012年5月4日</p></td>
<td></td>
<td></td>
<td><p>6.1.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-1-2.html">http://www.unicode.org/roadmaps/smp/smp-6-1-2.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.1.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-05-04</p></td>
<td><p>accessdate=2012-05-05 }}</ref></p></td>
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
<td><p>2012年7月30日</p></td>
<td></td>
<td></td>
<td><p>6.1.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-1-3.html">http://www.unicode.org/roadmaps/smp/smp-6-1-3.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.1.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-07-30</p></td>
<td><p>accessdate=2012-08-01 }}</ref></p></td>
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
<td><p>2012年8月27日</p></td>
<td></td>
<td></td>
<td><p>6.1.4<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-1-4.html">http://www.unicode.org/roadmaps/smp/smp-6-1-4.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.1.4</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-08-27</p></td>
<td><p>accessdate=2012-08-29 }}</ref></p></td>
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
<td><p>2012年9月13日</p></td>
<td></td>
<td><p>6.1.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-6-1-1.html">http://www.unicode.org/roadmaps/bmp/bmp-6-1-1.html</a></p></td>
<td><p>title=Roadmap to the BMP 6.1.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-09-13</p></td>
<td><p>accessdate=2012-09-14 }}</ref></p></td>
<td><p>6.1.5<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-1-5.html">http://www.unicode.org/roadmaps/smp/smp-6-1-5.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.1.5</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-09-13</p></td>
<td><p>accessdate=2012-09-14 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2012年9月26日</p></td>
<td><p>6.2.0[38]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2012年9月27日</p></td>
<td></td>
<td><p>6.2.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-6-2-0.html">http://www.unicode.org/roadmaps/bmp/bmp-6-2-0.html</a></p></td>
<td><p>title=Roadmap to the BMP 6.2.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-09-27</p></td>
<td><p>accessdate=2012-09-28 }}</ref></p></td>
<td><p>6.2.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-2-0.html">http://www.unicode.org/roadmaps/smp/smp-6-2-0.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.2.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-09-27</p></td>
<td><p>accessdate=2012-09-28 }}</ref></p></td>
<td><p>6.2.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-6-2-0.html">http://www.unicode.org/roadmaps/sip/sip-6-2-0.html</a></p></td>
<td><p>title=Roadmap to the SIP 6.2.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-09-27</p></td>
<td><p>accessdate=2012-09-28 }}</ref></p></td>
<td><p>6.2.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/tip/tip-6-2-0.html">http://www.unicode.org/roadmaps/tip/tip-6-2-0.html</a></p></td>
<td><p>title=Roadmap to the TIP 6.2.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-09-27</p></td>
<td><p>accessdate=2012-09-28 }}</ref></p></td>
<td><p>6.2.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/ssp/ssp-6-2-0.html">http://www.unicode.org/roadmaps/ssp/ssp-6-2-0.html</a></p></td>
<td><p>title=Roadmap to the SSP 6.2.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-09-27</p></td>
<td><p>accessdate=2012-09-28 }}</ref></p></td>
<td><p>6.2.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-6-2-0.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-6-2-0.html</a></p></td>
<td><p>title=Roadmap to the NOR 6.2.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-09-27</p></td>
<td><p>accessdate=2012-09-28 }}</ref></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2012年10月16日</p></td>
<td></td>
<td></td>
<td><p>6.2.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-2-1.html">http://www.unicode.org/roadmaps/smp/smp-6-2-1.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.2.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-10-16</p></td>
<td><p>accessdate=2012-10-20 }}</ref></p></td>
<td><p>6.2.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-6-2-1.html">http://www.unicode.org/roadmaps/sip/sip-6-2-1.html</a></p></td>
<td><p>title=Roadmap to the SIP 6.2.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-10-16</p></td>
<td><p>accessdate=2012-10-20 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2012年12月2日</p></td>
<td></td>
<td></td>
<td><p>6.2.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-2-2.html">http://www.unicode.org/roadmaps/smp/smp-6-2-2.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.2.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-12-02</p></td>
<td><p>accessdate=2012-12-04 }}</ref></p></td>
<td><p>6.2.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-6-2-2.html">http://www.unicode.org/roadmaps/sip/sip-6-2-2.html</a></p></td>
<td><p>title=Roadmap to the SIP 6.2.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2012-12-02</p></td>
<td><p>accessdate=2012-12-04 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2013年3月19日</p></td>
<td></td>
<td></td>
<td><p>6.2.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-2-3.html">http://www.unicode.org/roadmaps/smp/smp-6-2-3.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.2.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2013-03-19</p></td>
<td><p>accessdate=2013-03-21 }}</ref></p></td>
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
<td><p>2013年5月4日</p></td>
<td></td>
<td></td>
<td><p>6.2.4<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-2-4.html">http://www.unicode.org/roadmaps/smp/smp-6-2-4.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.2.4</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2013-05-03</p></td>
<td><p>accessdate=2013-05-05 }}</ref></p></td>
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
<td><p>2013年5月23日</p></td>
<td></td>
<td></td>
<td><p>6.2.5<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-2-5.html">http://www.unicode.org/roadmaps/smp/smp-6-2-5.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.2.5</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2013-05-23</p></td>
<td><p>accessdate=2013-05-24 }}</ref></p></td>
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
<td><p>2013年7月24日</p></td>
<td></td>
<td></td>
<td><p>6.2.6<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-2-6.html">http://www.unicode.org/roadmaps/smp/smp-6-2-6.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.2.6</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2013-07-24</p></td>
<td><p>accessdate=2013-07-25 }}</ref></p></td>
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
<td><p>2013年9月30日</p></td>
<td><p>6.3.0[39]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2013年10月28日</p></td>
<td></td>
<td><p>6.3.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-6-3-0.html">http://www.unicode.org/roadmaps/bmp/bmp-6-3-0.html</a></p></td>
<td><p>title=Roadmap to the BMP 6.3.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2013-10-28</p></td>
<td><p>accessdate=2013-10-30 }}</ref></p></td>
<td><p>6.3.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-3-0.html">http://www.unicode.org/roadmaps/smp/smp-6-3-0.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.3.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2013-11-02</p></td>
<td><p>accessdate=2013-11-03 }}</ref></p></td>
<td><p>6.3.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-6-3-0.html">http://www.unicode.org/roadmaps/sip/sip-6-3-0.html</a></p></td>
<td><p>title=Roadmap to the SIP 6.3.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2013-10-28</p></td>
<td><p>accessdate=2013-10-30 }}</ref></p></td>
<td><p>6.3.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/tip/tip-6-3-0.html">http://www.unicode.org/roadmaps/tip/tip-6-3-0.html</a></p></td>
<td><p>title=Roadmap to the TIP 6.3.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2013-10-28</p></td>
<td><p>accessdate=2013-10-30 }}</ref></p></td>
<td><p>6.3.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/ssp/ssp-6-3-0.html">http://www.unicode.org/roadmaps/ssp/ssp-6-3-0.html</a></p></td>
<td><p>title=Roadmap to the SSP 6.3.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2013-10-28</p></td>
<td><p>accessdate=2013-10-30 }}</ref></p></td>
<td><p>6.3.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-6-3-0.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-6-3-0.html</a></p></td>
<td><p>title=Roadmap to the NOR 6.3.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2013-10-28</p></td>
<td><p>accessdate=2013-10-30 }}</ref></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2014年2月19日</p></td>
<td></td>
<td><p>6.3.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-6-3-1.html">http://www.unicode.org/roadmaps/bmp/bmp-6-3-1.html</a></p></td>
<td><p>title=Roadmap to the BMP 6.3.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2014-02-19</p></td>
<td><p>accessdate=2014-02-20 }}</ref></p></td>
<td><p>6.3.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-6-3-1.html">http://www.unicode.org/roadmaps/smp/smp-6-3-1.html</a></p></td>
<td><p>title=Roadmap to the SMP 6.3.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2014-02-19</p></td>
<td><p>accessdate=2014-02-20 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2014年6月16日</p></td>
<td><p>7.0.0[40]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2014年8月7日</p></td>
<td></td>
<td><p>7.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-7-0-0.html">http://www.unicode.org/roadmaps/bmp/bmp-7-0-0.html</a></p></td>
<td><p>title=Roadmap to the BMP 7.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2014-08-07</p></td>
<td><p>accessdate=2014-08-09 }}</ref></p></td>
<td><p>7.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-7-0-0.html">http://www.unicode.org/roadmaps/smp/smp-7-0-0.html</a></p></td>
<td><p>title=Roadmap to the SMP 7.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2014-08-07</p></td>
<td><p>accessdate=2014-08-09 }}</ref></p></td>
<td><p>7.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-7-0-0.html">http://www.unicode.org/roadmaps/sip/sip-7-0-0.html</a></p></td>
<td><p>title=Roadmap to the SIP 7.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2014-08-07</p></td>
<td><p>accessdate=2014-08-09 }}</ref></p></td>
<td><p>7.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/tip/tip-7-0-0.html">http://www.unicode.org/roadmaps/tip/tip-7-0-0.html</a></p></td>
<td><p>title=Roadmap to the TIP 7.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2014-08-07</p></td>
<td><p>accessdate=2014-08-09 }}</ref></p></td>
<td><p>7.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/ssp/ssp-7-0-0.html">http://www.unicode.org/roadmaps/ssp/ssp-7-0-0.html</a></p></td>
<td><p>title=Roadmap to the SSP 7.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2014-08-07</p></td>
<td><p>accessdate=2014-08-09 }}</ref></p></td>
<td><p>7.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-7-0-0.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-7-0-0.html</a></p></td>
<td><p>title=Roadmap to the NOR 7.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2014-08-07</p></td>
<td><p>accessdate=2014-08-09 }}</ref></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2014年9月18日</p></td>
<td></td>
<td><p>7.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-7-0-1.html">http://www.unicode.org/roadmaps/bmp/bmp-7-0-1.html</a></p></td>
<td><p>title=Roadmap to the BMP 7.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2014-09-18</p></td>
<td><p>accessdate=2014-09-28 }}</ref></p></td>
<td><p>7.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-7-0-1.html">http://www.unicode.org/roadmaps/smp/smp-7-0-1.html</a></p></td>
<td><p>title=Roadmap to the SMP 7.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2014-09-18</p></td>
<td><p>accessdate=2014-09-28 }}</ref></p></td>
<td><p>7.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-7-0-1.html">http://www.unicode.org/roadmaps/sip/sip-7-0-1.html</a></p></td>
<td><p>title=Roadmap to the SIP 7.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2014-09-18</p></td>
<td><p>accessdate=2014-09-28 }}</ref></p></td>
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
<td><p>2014年10月24日</p></td>
<td></td>
<td></td>
<td><p>7.0.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-7-0-2.html">http://www.unicode.org/roadmaps/smp/smp-7-0-2.html</a></p></td>
<td><p>title=Roadmap to the SMP 7.0.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2014-10-24</p></td>
<td><p>accessdate=2014-10-30 }}</ref></p></td>
<td><p>7.0.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-7-0-2.html">http://www.unicode.org/roadmaps/sip/sip-7-0-2.html</a></p></td>
<td><p>title=Roadmap to the SIP 7.0.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2014-10-24</p></td>
<td><p>accessdate=2014-10-26 }}</ref></p></td>
<td><p>7.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/tip/tip-7-0-1.html">http://www.unicode.org/roadmaps/tip/tip-7-0-1.html</a></p></td>
<td><p>title=Roadmap to the TIP 7.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2014-10-24</p></td>
<td><p>accessdate=2014-10-31 }}</ref></p></td>
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
<td><p>2015年3月26日</p></td>
<td></td>
<td><p>7.0.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-7-0-2.html">http://www.unicode.org/roadmaps/bmp/bmp-7-0-2.html</a></p></td>
<td><p>title=Roadmap to the BMP 7.0.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2015-03-26</p></td>
<td><p>accessdate=2015-03-28 }}</ref></p></td>
<td><p>7.0.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-7-0-3.html">http://www.unicode.org/roadmaps/smp/smp-7-0-3.html</a></p></td>
<td><p>title=Roadmap to the SMP 7.0.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2015-03-26</p></td>
<td><p>accessdate=2015-03-28 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2015年6月3日</p></td>
<td></td>
<td><p>7.0.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-7-0-3.html">http://www.unicode.org/roadmaps/bmp/bmp-7-0-3.html</a></p></td>
<td><p>title=Roadmap to the BMP 7.0.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2015-06-03</p></td>
<td><p>accessdate=2015-06-13 }}</ref></p></td>
<td><p>7.0.4<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-7-0-4.html">http://www.unicode.org/roadmaps/smp/smp-7-0-4.html</a></p></td>
<td><p>title=Roadmap to the SMP 7.0.4</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2015-06-03</p></td>
<td><p>accessdate=2015-06-13 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2015年6月17日</p></td>
<td><p>8.0.0[41]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2015年6月26日</p></td>
<td></td>
<td><p>8.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-8-0-0.html">http://www.unicode.org/roadmaps/bmp/bmp-8-0-0.html</a></p></td>
<td><p>title=Roadmap to the BMP 8.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2015-07-09</p></td>
<td><p>accessdate=2015-07-10 }}</ref></p></td>
<td><p>8.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-8-0-0.html">http://www.unicode.org/roadmaps/smp/smp-8-0-0.html</a></p></td>
<td><p>title=Roadmap to the SMP 8.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2015-07-09</p></td>
<td><p>accessdate=2015-07-10 }}</ref></p></td>
<td><p>8.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-8-0-0.html">http://www.unicode.org/roadmaps/sip/sip-8-0-0.html</a></p></td>
<td><p>title=Roadmap to the SIP 8.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2015-07-09</p></td>
<td><p>accessdate=2015-07-10 }}</ref></p></td>
<td><p>8.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/tip/tip-8-0-0.html">http://www.unicode.org/roadmaps/tip/tip-8-0-0.html</a></p></td>
<td><p>title=Roadmap to the TIP 8.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2015-07-09</p></td>
<td><p>accessdate=2015-07-10 }}</ref></p></td>
<td><p>8.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/ssp/ssp-8-0-0.html">http://www.unicode.org/roadmaps/ssp/ssp-8-0-0.html</a></p></td>
<td><p>title=Roadmap to the SSP 8.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2015-07-09</p></td>
<td><p>accessdate=2015-07-10 }}</ref></p></td>
<td><p>8.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-8-0-0.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-8-0-0.html</a></p></td>
<td><p>title=Roadmap to the NOR 8.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2015-07-09</p></td>
<td><p>accessdate=2015-07-10 }}</ref></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2015年8月17日</p></td>
<td></td>
<td></td>
<td><p>8.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-8-0-1.html">http://www.unicode.org/roadmaps/smp/smp-8-0-1.html</a></p></td>
<td><p>title=Roadmap to the SMP 8.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2015-08-17</p></td>
<td><p>accessdate=2015-08-22 }}</ref></p></td>
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
<td><p>2016年1月21日</p></td>
<td></td>
<td><p>8.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-8-0-1.html">http://www.unicode.org/roadmaps/bmp/bmp-8-0-1.html</a></p></td>
<td><p>title=Roadmap to the BMP 8.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2016-01-21</p></td>
<td><p>accessdate=2016-01-25 }}</ref></p></td>
<td><p>8.0.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-8-0-2.html">http://www.unicode.org/roadmaps/smp/smp-8-0-2.html</a></p></td>
<td><p>title=Roadmap to the SMP 8.0.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2016-01-21</p></td>
<td><p>accessdate=2016-01-25 }}</ref></p></td>
<td></td>
<td><p>8.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/tip/tip-8-0-1.html">http://www.unicode.org/roadmaps/tip/tip-8-0-1.html</a></p></td>
<td><p>title=Roadmap to the TIP 8.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2016-01-21</p></td>
<td><p>accessdate=2016-01-22 }}</ref></p></td>
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
<td><p>2016年2月3日</p></td>
<td></td>
<td></td>
<td><p>8.0.3<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-8-0-3.html">http://www.unicode.org/roadmaps/smp/smp-8-0-3.html</a></p></td>
<td><p>title=Roadmap to the SMP 8.0.3</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2016-02-03</p></td>
<td><p>accessdate=2016-02-05 }}</ref></p></td>
<td><p>8.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-8-0-1.html">http://www.unicode.org/roadmaps/sip/sip-8-0-1.html</a></p></td>
<td><p>title=Roadmap to the SIP 8.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2016-02-03</p></td>
<td><p>accessdate=2016-02-05 }}</ref></p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2016年5月3日</p></td>
<td></td>
<td><p>8.0.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-8-0-2.html">http://www.unicode.org/roadmaps/bmp/bmp-8-0-2.html</a></p></td>
<td><p>title=Roadmap to the BMP 8.0.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2016-05-03</p></td>
<td><p>accessdate=2016-06-13 }}</ref></p></td>
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
<td><p>2016年6月10日</p></td>
<td></td>
<td></td>
<td><p>8.0.4<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-8-0-4.html">http://www.unicode.org/roadmaps/smp/smp-8-0-4.html</a></p></td>
<td><p>title=Roadmap to the SMP 8.0.4</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2016-06-10</p></td>
<td><p>accessdate=2016-06-13 }}</ref></p></td>
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
<td><p>2016年6月21日</p></td>
<td><p>9.0.0[42]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>2016年6月23日</p></td>
<td></td>
<td><p>9.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-9-0-0.html">http://www.unicode.org/roadmaps/bmp/bmp-9-0-0.html</a></p></td>
<td><p>title=Roadmap to the BMP 9.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2016-06-23</p></td>
<td><p>accessdate=2016-06-25 }}</ref></p></td>
<td><p>9.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-9-0-0.html">http://www.unicode.org/roadmaps/smp/smp-9-0-0.html</a></p></td>
<td><p>title=Roadmap to the SMP 9.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2016-06-23</p></td>
<td><p>accessdate=2016-06-25 }}</ref></p></td>
<td><p>9.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-9-0-0.html">http://www.unicode.org/roadmaps/sip/sip-9-0-0.html</a></p></td>
<td><p>title=Roadmap to the SIP 9.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2016-06-23</p></td>
<td><p>accessdate=2016-06-25 }}</ref></p></td>
<td><p>9.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/tip/tip-9-0-0.html">http://www.unicode.org/roadmaps/tip/tip-9-0-0.html</a></p></td>
<td><p>title=Roadmap to the TIP 9.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2016-06-23</p></td>
<td><p>accessdate=2016-06-25 }}</ref></p></td>
<td><p>9.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/ssp/ssp-9-0-0.html">http://www.unicode.org/roadmaps/ssp/ssp-9-0-0.html</a></p></td>
<td><p>title=Roadmap to the SSP 9.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2016-06-23</p></td>
<td><p>accessdate=2016-06-25 }}</ref></p></td>
<td><p>9.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-9-0-0.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-9-0-0.html</a></p></td>
<td><p>title=Roadmap to the NOR 9.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2016-06-23</p></td>
<td><p>accessdate=2016-06-25 }}</ref></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2017年1月12日</p></td>
<td></td>
<td></td>
<td><p>9.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-9-0-1.html">http://www.unicode.org/roadmaps/smp/smp-9-0-1.html</a></p></td>
<td><p>title=Roadmap to the SMP 9.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2017-01-12</p></td>
<td><p>accessdate=2017-01-25 }}</ref></p></td>
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
<td><p>2017年5月24日</p></td>
<td></td>
<td><p>9.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-9-0-1.html">http://www.unicode.org/roadmaps/bmp/bmp-9-0-1.html</a></p></td>
<td><p>title=Roadmap to the BMP 9.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2017-05-24</p></td>
<td><p>accessdate=2017-05-28 }}</ref></p></td>
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
<td><p>2017年6月6日</p></td>
<td></td>
<td></td>
<td><p>9.0.2<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-9-0-2.html">http://www.unicode.org/roadmaps/smp/smp-9-0-2.html</a></p></td>
<td><p>title=Roadmap to the SMP 9.0.2</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2017-06-06</p></td>
<td><p>accessdate=2017-06-09 }}</ref></p></td>
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
<td><p>2017年6月20日</p></td>
<td><p>10.0.0[43]</p></td>
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
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>2017年6月21日</p></td>
<td></td>
<td><p>10.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/bmp/bmp-10-0-0.html">http://www.unicode.org/roadmaps/bmp/bmp-10-0-0.html</a></p></td>
<td><p>title=Roadmap to the BMP 10.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2017-06-21</p></td>
<td><p>accessdate=2017-07-22 }}</ref></p></td>
<td></td>
<td><p>10.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/sip/sip-10-0-0.html">http://www.unicode.org/roadmaps/sip/sip-10-0-0.html</a></p></td>
<td><p>title=Roadmap to the SIP 10.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2017-06-21</p></td>
<td><p>accessdate=2017-07-22 }}</ref></p></td>
<td><p>10.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/tip/tip-10-0-0.html">http://www.unicode.org/roadmaps/tip/tip-10-0-0.html</a></p></td>
<td><p>title=Roadmap to the TIP 10.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2017-06-21</p></td>
<td><p>accessdate=2017-07-22 }}</ref></p></td>
<td><p>10.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/ssp/ssp-10-0-0.html">http://www.unicode.org/roadmaps/ssp/ssp-10-0-0.html</a></p></td>
<td><p>title=Roadmap to the SSP 10.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2017-06-21</p></td>
<td><p>accessdate=2017-07-22 }}</ref></p></td>
<td><p>10.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-10-0-0.html">http://www.unicode.org/roadmaps/not-the-roadmap/not-the-roadmap-10-0-0.html</a></p></td>
<td><p>title=Roadmap to the NOR 10.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2017-06-21</p></td>
<td><p>accessdate=2017-07-22 }}</ref></p></td>
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
<td><p>2017年6月29日</p></td>
<td></td>
<td></td>
<td><p>10.0.0<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-10-0-0.html">http://www.unicode.org/roadmaps/smp/smp-10-0-0.html</a></p></td>
<td><p>title=Roadmap to the SMP 10.0.0</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2017-06-29</p></td>
<td><p>accessdate=2017-07-22 }}</ref></p></td>
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
<td><p>2017年12月27日</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>10.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/tip/tip-10-0-1.html">http://www.unicode.org/roadmaps/tip/tip-10-0-1.html</a></p></td>
<td><p>title=Roadmap to the TIP 10.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2017-12-27</p></td>
<td><p>accessdate=2018-01-01 }}</ref></p></td>
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
<td><p>2018年1月10日</p></td>
<td></td>
<td></td>
<td><p>10.0.1<ref>{{Cite web</p></td>
<td><p>url=<a href="http://www.unicode.org/roadmaps/smp/smp-10-0-1.html">http://www.unicode.org/roadmaps/smp/smp-10-0-1.html</a></p></td>
<td><p>title=Roadmap to the SMP 10.0.1</p></td>
<td><p>author= Michael Everson, Rick McGowan, Ken Whistler, V.S. Umamaheswaran</p></td>
<td><p>publisher= Unicode Consortium</p></td>
<td><p>language=English</p></td>
<td><p>date=2018-01-10</p></td>
<td><p>accessdate=2018-01-14 }}</ref></p></td>
<td></td>
<td></td>
<td></td>
<td><p>-</p></td>
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

## Unicodeの諸問題

### バージョンごとの非互換性

Unicodeは同一のコードでもバージョンが変わったとき完全に異なった文字を定義し直したことがある。

そのうち最大のものがUnicode 2.0での「[ハングルの大移動](https://ja.wikipedia.org/wiki/ハングル#Unicode "wikilink")」である。これはUnicode 1.1までで定義されていたハングルの領域を破棄し、新しいハングルの領域を別の位置に設定し、破棄された領域には別の文字の領域を割り当てることとなった。その後、Unicode 3.0では、従来ハングルが割り当てられていた領域にCJK統合漢字拡張A、ついでUnicode 4.0で六十四卦が割り当てられた。このように、Unicode 1.1以前でハングルを記述した文書とUnicode 2.0以降でCJK統合漢字拡張Aを記述した文書には互換性がない\[44\]。JCS委員長の[芝野耕司](../Page/芝野耕司.md "wikilink")はUnicodeに日本語の漢字を収録させる議論の中で、ハングル大移動について「韓国のとった滅茶苦茶な行動」と述べている\[45\]。

### 日本語環境でのUnicodeの諸問題

#### YEN SIGN 問題

[Shift_JIS](../Page/Shift_JIS.md "wikilink") では [JIS X 0201](https://ja.wikipedia.org/wiki/JIS_X_0201 "wikilink") における[円記号](../Page/円記号.md "wikilink") "¥" が 0x5C に置かれている。これを Unicode のマッピングに合わせると YEN SIGN (U+00A5) にマップされる。しかし、0x5C は [ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink") では[バックスラッシュ](../Page/バックスラッシュ.md "wikilink") "" に相当し、[C言語](../Page/C言語.md "wikilink")などで[エスケープ文字](../Page/エスケープ文字.md "wikilink")として使われる事から、この文字のコードを変更すると問題が起きる。極端な例として、0x5C が円記号とエスケープ文字の両方の目的で使われているケース（たとえば `printf("¥¥%d¥n", price);` など）も考えられる。

そのため、Unicode を利用するアプリケーションでは、U+007F 以下のコードに関しては移動させないという暗黙のルールができている。

そうなると、Unicode 環境では円記号がバックスラッシュの表示に変わってしまうように思われるが、これは日本語用の[フォント](../Page/フォント.md "wikilink")データの 0x5C の位置には円記号の字形を当ててしまうことで対処している。これによって、日本語環境での表示上は 0x5C の位置で円記号を用いることができる。

この問題は日本語環境に限ったことではない。もともと [ISO 646](https://ja.wikipedia.org/wiki/ISO_646 "wikilink") 上では、0x5C を含む数種の文字は自由領域（バリアント）として各国での定義を認めていた。そのため、日本語以外でも ASCII でバックスラッシュに相当するコードに異なる記号を当てているケースが多い。例えば、[韓国では](../Page/大韓民国.md "wikilink")[ウォン記号](https://ja.wikipedia.org/wiki/大韓民国ウォン "wikilink") (WON SIGN, U+20A9, "")、[デンマーク](https://ja.wikipedia.org/wiki/デンマーク "wikilink")や[ノルウェー](../Page/ノルウェー.md "wikilink")ではストローク付きO (LATIN CAPITAL LETTER O WITH STROKE, U+00D8, "") などである。（後者は後の時代には、0x5C はバックスラッシュのままとし、[ISO 8859](https://ja.wikipedia.org/wiki/ISO_8859 "wikilink") シリーズを用いることが一般化した。）

#### 波ダッシュ・全角チルダ問題

[JIS X 0221](../Page/JIS_X_0221.md "wikilink") 規定の JIS X 0208 と JIS X 0221 の対応表では、[波ダッシュ](../Page/波ダッシュ.md "wikilink")は WAVE DASH (U+301C, "") に対応させているが、[マイクロソフト](../Page/マイクロソフト.md "wikilink")は Windows の Shift_JIS と Unicode の変換テーブルを作成する際に、JIS X 0208 において 1 区 33 点に割り当てられている波ダッシュ "" を、Unicode における全角チルダ (FULLWIDTH TILDE, U+FF5E, "～") に割り当てたため不整合が生じる。この結果、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") 等の JIS X 0221 準拠の Shift_JIS ⇔ Unicode 変換テーブルをもつ処理系と Windows との間で Unicode データをやり取りする場合、文字化けを起こすことになる。そこで Windows 以外の OS 上で動くアプリケーションの中には、[CP932](../Page/Microsoftコードページ932.md "wikilink") という名前でマイクロソフト仕様の Shift_JIS コード体系を別途用意して対応しているケースが多い。この原因とされている Unicode 仕様書の例示字形の問題に関しては、[波ダッシュ\#Unicodeに関連する問題](https://ja.wikipedia.org/wiki/波ダッシュ#Unicodeに関連する問題 "wikilink")を参照すること。

上記に加え、マイクロソフト仕様は変換時にも問題が起こる文字を以下に示す。

<table>
<thead>
<tr class="header">
<th><p>JIS X 0208<br />
区点</p></th>
<th><p>Shift JIS</p></th>
<th><p>JIS X 0208<br />
日本語通用名称</p></th>
<th><p>SJISでデコード</p></th>
<th><p>MS932でデコード<br />
(マイクロソフト仕様)</p></th>
<th><p>関連記事</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1-29</p></td>
<td><p>0x815c</p></td>
<td><p>ダッシュ(全角)</p></td>
<td><p>(U+2014) EM DASH</p></td>
<td><p>(U+2015) HORIZONTAL BAR</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ダッシュ_(記号)#全角ダッシュのマッピング問題" title="wikilink">ダッシュ (記号)</a></p></td>
</tr>
<tr class="even">
<td><p>1-33</p></td>
<td><p>0x8160</p></td>
<td><p>波ダッシュ</p></td>
<td><p>(U+301C) WAVE DASH</p></td>
<td><p>(U+FF5E) FULLWIDTH TILDE</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/波ダッシュ#Unicodeに関連する問題" title="wikilink">波ダッシュ</a>、<a href="https://ja.wikipedia.org/wiki/チルダ#全角チルダ" title="wikilink">全角チルダ</a></p></td>
</tr>
<tr class="odd">
<td><p>1-34</p></td>
<td><p>0x8161</p></td>
<td><p>双柱</p></td>
<td><p>(U+2016) DOUBLE VERTICAL LINE</p></td>
<td><p>(U+2225) PARALLEL TO</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/双柱" title="wikilink">双柱</a>、<a href="https://ja.wikipedia.org/wiki/平行記号#文字コードにおける問題" title="wikilink">平行記号</a></p></td>
</tr>
<tr class="even">
<td><p>1-61</p></td>
<td><p>0x817c</p></td>
<td><p>負符号,減算記号</p></td>
<td><p>(U+2212) MINUS SIGN</p></td>
<td><p>(U+FF0D) FULLWIDTH HYPHEN-MINUS</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/プラス記号とマイナス記号#マイナス記号" title="wikilink">マイナス記号</a>、<a href="../Page/ハイフンマイナス.md" title="wikilink">ハイフンマイナス</a></p></td>
</tr>
<tr class="odd">
<td><p>1-81</p></td>
<td><p>0x8191</p></td>
<td><p>セント記号</p></td>
<td><p>(U+00A2) CENT SIGN</p></td>
<td><p>(U+FFE0) FULLWIDTH CENT SIGN</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/セント_(通貨)#符号位置" title="wikilink">セント (通貨)</a></p></td>
</tr>
<tr class="even">
<td><p>1-82</p></td>
<td><p>0x8192</p></td>
<td><p>ポンド記号</p></td>
<td><p>(U+00A3) POUND SIGN</p></td>
<td><p>(U+FFE1) FULLWIDTH POUND SIGN</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/£#コンピュータでの扱い" title="wikilink">£</a></p></td>
</tr>
<tr class="odd">
<td><p>2-44</p></td>
<td><p>0x81ca</p></td>
<td><p>否定</p></td>
<td><p>(U+00AC) NOT SIGN</p></td>
<td><p>(U+FFE2) FULLWIDTH NOT SIGN</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/否定記号" title="wikilink">否定記号</a></p></td>
</tr>
</tbody>
</table>

このうちセント・ポンド・否定については、IBMのメインフレームではShift_JISを拡張してこれらの半角版をコードポイント 0xFD-0xFF に割り当て、別途JIS X 0208からマップされた位置に全角版を収録していたため、WindowsをIBMメインフレームの端末として用いるケースを想定したといわれている

なお、[Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") や Microsoft Office 2007 に付属する IME パッドの文字一覧における JIS X 0213 の面区点の表示は、上記の文字についても JIS で規定されているものと同じマッピングを使用している\[46\]。

## ブロックの一覧

<table>
<thead>
<tr class="header">
<th><p>索引</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/Unicode一覧_0000-0FFF.md" title="wikilink">0000-0FFF</a><br />
<a href="../Page/Unicode一覧_1000-1FFF.md" title="wikilink">1000-1FFF</a><br />
<a href="../Page/Unicode一覧_2000-2FFF.md" title="wikilink">2000-2FFF</a><br />
<a href="../Page/Unicode一覧_3000-3FFF.md" title="wikilink">3000-3FFF</a><br />
<a href="../Page/Unicode一覧_4000-4FFF.md" title="wikilink">4000-4FFF</a><br />
<a href="../Page/Unicode一覧_5000-5FFF.md" title="wikilink">5000-5FFF</a><br />
<a href="../Page/Unicode一覧_6000-6FFF.md" title="wikilink">6000-6FFF</a><br />
<a href="../Page/Unicode一覧_7000-7FFF.md" title="wikilink">7000-7FFF</a><br />
<a href="../Page/Unicode一覧_8000-8FFF.md" title="wikilink">8000-8FFF</a><br />
<a href="../Page/Unicode一覧_9000-9FFF.md" title="wikilink">9000-9FFF</a><br />
<a href="../Page/Unicode一覧_A000-AFFF.md" title="wikilink">A000-AFFF</a><br />
<a href="../Page/Unicode一覧_B000-BFFF.md" title="wikilink">B000-BFFF</a><br />
<a href="../Page/Unicode一覧_C000-CFFF.md" title="wikilink">C000-CFFF</a><br />
<a href="../Page/Unicode一覧_D000-DFFF.md" title="wikilink">D000-DFFF</a><br />
<a href="../Page/Unicode一覧_E000-EFFF.md" title="wikilink">E000-EFFF</a><br />
<a href="../Page/Unicode一覧_F000-FFFF.md" title="wikilink">F000-FFFF</a></p></td>
</tr>
</tbody>
</table>

## 脚注

### 注釈

### 出典

## 参考文献

  - 用語の日本語表記は原則として次にならった。

  -
  -   -
      -
      - \- 付属：CD-ROM。

      - \- 付属：CD-ROM。

      - \- 付属：CD-ROM。

  - \- 原タイトル：*Unicode: a primer*。

  -
  -
  -
  -
  -
  -
## 関連項目

  - [ISO/IEC 10646](https://ja.wikipedia.org/wiki/ISO/IEC_10646 "wikilink")
  - [OpenType](../Page/OpenType.md "wikilink")
  - [Unicode一覧](https://ja.wikipedia.org/wiki/Unicode一覧 "wikilink")
  - [Unicode参照アルゴリズム](https://ja.wikipedia.org/wiki/Unicode参照アルゴリズム "wikilink")
  - [機種依存文字](../Page/機種依存文字.md "wikilink")
  - [国際化と地域化](../Page/国際化と地域化.md "wikilink")
  - [中西亮](../Page/中西亮.md "wikilink")
  - [文字コード](../Page/文字コード.md "wikilink")
  - [異体字セレクタ](../Page/異体字セレクタ.md "wikilink")

## 外部リンク

  - [The Unicode Consortium](https://www.unicode.org/)
  - [DecodeUnicode](https://decodeunicode.org/)
  - [BabelMap](https://www.babelstone.co.uk/Software/BabelMap.html) - Unicode Character Map for Windows

[\*](https://ja.wikipedia.org/wiki/カテゴリ:Unicode "wikilink")

1.
2.  UTF-8はPlan 9が由来
3.
4.
5.
6.
7.
8.  図形文字、書式文字。
9.
10.
11.
12.
13. 2019年3月現在では、古代漢字や甲骨文字はまだ1文字も収録されていない。
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.
35.
36.
37.
38.
39.
40.
41.
42.
43.
44. RFC 3629の[5. Versions of the standards](http://tools.ietf.org/html/rfc3629#section-5)でKorean mess（ハングル大移動）について、[8. MIME registration](http://tools.ietf.org/html/rfc3629#section-8)でUTF-8にバージョン指定がない理由についての言及がある。
45.
46.