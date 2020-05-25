> この記事は[CJK互換漢字](https://ja.wikipedia.org/wiki/CJK互換漢字)から翻訳されています。


**CJK互換漢字**（シージェーケーごかんかんじ、）は、[Unicode](../Page/Unicode.md "wikilink")の[ブロックの一つであり](https://ja.wikipedia.org/wiki/ブロック_\(Unicode\) "wikilink")、Unicodeの[統合規則に従うなら本来](../Page/包摂_\(文字コード\).md "wikilink")[CJK統合漢字](../Page/CJK統合漢字.md "wikilink")に統合されるはずであるが、既存の[文字コード](../Page/文字コード.md "wikilink")との[互換性](../Page/互換性.md "wikilink")のためUnicodeに収録された[互換文字の一種である](../Page/Unicodeの互換文字.md "wikilink")。

## 内訳

文字コード順ではなく、登録された順に紹介する。

  - F900 - U+FA0B
    [韓国の](../Page/大韓民国.md "wikilink")[文字コード](../Page/文字コード.md "wikilink")規格[KS X 1001](../Page/KS_X_1001.md "wikilink")（収録当時の規格番号はKS C 5601）に含まれる重複漢字との[往復変換](https://ja.wikipedia.org/wiki/往復変換 "wikilink")を保証するために収録された[漢字](../Page/漢字.md "wikilink")。
    KS X 1001では漢字を[韓国語での辞書順に配列しているが](../Page/朝鮮語.md "wikilink")、一部の漢字には複数の読みが存在する。KS X 1001は同じ形でも複数の読みを持つ漢字は分離して収録しているため、これらは統合されて統合漢字に収録された。
    韓国はこれらの文字に対して[原規格分離](https://ja.wikipedia.org/wiki/原規格分離 "wikilink")を主張しなかったが、往復変換を保証できなくては困るとした[ユニコードコンソーシアム](../Page/ユニコードコンソーシアム.md "wikilink")の代表からの要求により、互換漢字として収録された\[1\]。この範囲の内、U+F91D（欄）、U+F928（廊）、U+F929（朗）、U+F936（虜）、U+F970（殺）、U+F9D0（類）、U+F9DC（隆）は、IBM拡張漢字およびJIS X 0213と共有している。

<!-- end list -->

  - U+FA0C - U+FA0D
    [台湾](https://ja.wikipedia.org/wiki/台湾 "wikilink")の文字コード[Big5](../Page/Big5.md "wikilink")に誤って重複して収録された2文字に対応する漢字。
  - U+FA0E - U+FA2D
    [IBM拡張漢字のうち](https://ja.wikipedia.org/wiki/Microsoftコードページ932#CP932の誕生から統合まで "wikilink")、CJK統合漢字のブロックに収録されなかったもの。[IRGを経由する漢字の通常の登録提案を経ずに](https://ja.wikipedia.org/wiki/Ideographic_Rapporteur_Group "wikilink")、[カナダ](https://ja.wikipedia.org/wiki/カナダ "wikilink")からの提案として[ISO/IEC 10646に収録されたため](https://ja.wikipedia.org/wiki/ISO/IEC_10646 "wikilink")、「カナダ漢字」と呼ばれることがある\[2\]。この範囲の漢字のうち12文字は、CJK統合漢字ブロック内に同一とみなせる（統合できる）文字が存在しないため実際にはCJK統合漢字とされている。なお、U+FA11（）はU+5D0E（崎）、U+FA14（）はU+6B05（欅）およびU+6989（）、U+FA1F（）はU+81C8（臈）にそれぞれ統合漢字ブロックの異体字を持つが、字体差が大きいとみなされ統合の範疇とされていない。逆にU+FA20（蘒）は、U+8612（蘒）と字体差が大きい（草冠と禾偏を取った部分が「亀」か「龜」かで、画数差が5画ある。）にもかかわらず統合されており、互換漢字となっている。[異体字セレクタ](../Page/異体字セレクタ.md "wikilink")の方もU+8612を親字としてU+FA20の字形が規定されている。また、後にCJK統合漢字拡張BブロックのU+27EAFにU+FA23と同じものが登録されたが、これはU+FA23を統合漢字扱いすると決めた後に登録されたため、誤って重複登録されたことになる。
  - U+2F800 - U+2FA1D
    台湾の文字コード規格[CNS 11643はUnicodeと包摂規準が大きく異なるため](https://ja.wikipedia.org/wiki/CNS_11643 "wikilink")、Unicodeでは統合される漢字の多数が別々に収録されている。それらの文字との互換性を確保するために収録された文字の一群。Unicode 3.1で追加。
    数が多いため、[BMP外](../Page/基本多言語面.md "wikilink")（[追加漢字面](https://ja.wikipedia.org/wiki/追加漢字面 "wikilink")）に新たなブロックを作成して収録された。

<!-- end list -->

  - U+FA30 - U+FA6A
    [日本](https://ja.wikipedia.org/wiki/日本 "wikilink")の文字コード規格[JIS X 0213において人名許容](../Page/JIS_X_0213.md "wikilink")・康煕別掲と呼ばれる漢字の一群と互換性を確保するために収録されたもの。Unicode 3.2で追加。これらは当初から原規格であった[JIS X 0208では](../Page/JIS_X_0208.md "wikilink")[包摂されていたため](../Page/包摂_\(文字コード\).md "wikilink")、Unicodeでもたまたま他国の規格に含まれていたものを除いて統合されていた。
  - U+FA70 - U+FAD9
    [北朝鮮の文字コード規格](../Page/朝鮮民主主義人民共和国.md "wikilink")[KPS 9566および](../Page/KPS_9566.md "wikilink")[KPS 10721に収録されている漢字との互換性を確保するために収録された漢字の一群](https://ja.wikipedia.org/wiki/KPS_10721 "wikilink")。Unicode 4.1で追加。
  - U+FA6B - U+FA6D
    日本の[データ放送](../Page/データ放送.md "wikilink")規格[ARIB STD-B24で使われる文字コードに収録されている独自の漢字](../Page/Broadcast_Markup_Language.md "wikilink")（[ARIB外字](https://ja.wikipedia.org/wiki/ARIB外字 "wikilink")）のうち、既存の漢字に包摂されていると考えられるもの\[3\]。Unicode 5.2で追加\[4\]。
  - U+FA2E - U+FA2F
    U+F900 - U+FA0Bで定義されたうち2字（U+F92CおよびU+F9B8）に誤りがあり、それを修正するためにUnicode 6.1で収録された。

### コード順

| コード範囲           | 内容                                         | 関連国および地域                 |
| --------------- | ------------------------------------------ | ------------------------ |
| U+F900 - U+FA0B | Pronunciation variants from KS X 1001:1998 | 大韓民国、（日本、香港、朝鮮民主主義人民共和国） |
| U+FA0C - U+FA0D | Duplicate characters from Big 5            | 台湾                       |
| U+FA0E - U+FA2D | The IBM 32 compatibility ideographs        | 日本、（中華人民共和国）             |
| U+FA2E - U+FA2F | Korean compatibility ideographs            | 大韓民国                     |
| U+FA30 - U+FA6A | JIS X 0213 compatibility ideographs        | 日本                       |
| U+FA6B - U+FA6D | ARIB compatibility ideographs              | 日本                       |
| U+FA70 - U+FAD9 | DPRK compatibility ideographs              | 朝鮮民主主義人民共和国              |

## CJK互換漢字ブロックにあるCJK統合漢字

CJK互換漢字[ブロックにCJK統合漢字が](https://ja.wikipedia.org/wiki/ブロック_\(Unicode\) "wikilink")12文字ある。

<table>
<thead>
<tr class="header">
<th><p>符号位置</p></th>
<th><p>文字</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>U+FA0E</p></td>
<td></td>
<td><p>通用日本文字集合</p></td>
</tr>
<tr class="even">
<td><p>U+FA0F</p></td>
<td></td>
<td><p>JIS2004拡張漢字集合（第3水準漢字）</p></td>
</tr>
<tr class="odd">
<td><p>U+FA11</p></td>
<td></td>
<td><p>JIS2004拡張漢字集合（第3水準漢字）<br />
（0x8DE8）の異体字</p></td>
</tr>
<tr class="even">
<td><p>U+FA13</p></td>
<td></td>
<td><p>JIS2004拡張漢字集合（第4水準漢字）</p></td>
</tr>
<tr class="odd">
<td><p>U+FA14</p></td>
<td></td>
<td><p>JIS2004拡張漢字集合（第3水準漢字）<br />
（0x9F4F）の異体字</p></td>
</tr>
<tr class="even">
<td><p>U+FA1F</p></td>
<td></td>
<td><p>JIS2004拡張漢字集合（第3水準漢字）<br />
（0xE464）の異体字</p></td>
</tr>
<tr class="odd">
<td><p>U+FA21</p></td>
<td></td>
<td><p>JIS2004拡張漢字集合（第4水準漢字）</p></td>
</tr>
<tr class="even">
<td><p>U+FA23</p></td>
<td></td>
<td><p>通用日本文字集合<br />
重複登録（U+27EAF）</p></td>
</tr>
<tr class="odd">
<td><p>U+FA24</p></td>
<td></td>
<td><p>JIS2004拡張漢字集合（第4水準漢字）</p></td>
</tr>
<tr class="even">
<td><p>U+FA27</p></td>
<td></td>
<td><p>通用日本文字集合</p></td>
</tr>
<tr class="odd">
<td><p>U+FA28</p></td>
<td></td>
<td><p>通用日本文字集合</p></td>
</tr>
<tr class="even">
<td><p>U+FA29</p></td>
<td></td>
<td><p>通用日本文字集合</p></td>
</tr>
</tbody>
</table>

## CJK互換漢字ブロックにある定義誤り

CJK互換漢字ブロックにある定義誤りの文字で削除され、再定義されている。

| 符号位置   | 文字 | 備考          |
| ------ | -- | ----------- |
| U+F92C | 郎  | U+FA2Eで再定義  |
| U+F9B8 | 隸  | U+FA2Fで再定義  |
| U+FAD4 | 䀹  | U+2F949で再定義 |

## 日本語処理における問題点

CJK互換漢字はその名前にもかかわらずCJK統合漢字と[互換等価ではなく](https://ja.wikipedia.org/wiki/Unicodeの等価性#互換等価 "wikilink")[正準等価であり](https://ja.wikipedia.org/wiki/Unicodeの等価性#正準等価 "wikilink")、互いに区別されることを期待してはならない\[5\]。このため4種類の[正規化のいずれを採用してもCJK統合漢字に分解](../Page/Unicode正規化.md "wikilink")（変換）されてしまい、日本の人名処理などにおいて要求されることのある一部の[人名用漢字](../Page/人名用漢字.md "wikilink")などの区別が、Unicodeの[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")上で保証されるとは限らない。

一部にCJK互換漢字の等価性を正準等価から互換等価に変えるべきであるという主張があるが\[6\]、Unicodeでは[JIS X 0213用の互換漢字の一部は新たに収録せず](../Page/JIS_X_0213.md "wikilink")、既存の[KS X 1001互換文字用の領域などに収録されていた文字を流用している](../Page/KS_X_1001.md "wikilink")。このため日本語だけの都合で等価性を変えることはできない。またUnicodeには正規化の[安定性の原則](https://ja.wikipedia.org/wiki/安定性の原則 "wikilink")があり\[7\]、その意味でも等価性の変更は現実的ではない。

一方[濁点](../Page/濁点.md "wikilink")・[半濁点](../Page/半濁点.md "wikilink")を合成済みの[仮名文字](../Page/仮名_\(文字\).md "wikilink")（たとえば「が」）は、仮名文字に合成用濁点・半濁点を続けた文字の組み合わせ（たとえば「か」+「　゙」）と同一視する需要がある。このため単純に正規化を行わなければ済む問題でもない。

[アップルはこのジレンマを解決するため](../Page/アップル_\(企業\).md "wikilink")、CJK互換漢字を正規化から除外した新しい正規化形式の追加をUTC（Unicode Technical Committee, Unicode技術委員会）に提案したが、否決された\[8\]。そこでアップルはCJK互換漢字を含む一部の文字が分解されない独自の正規化形式を定め、自社の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")に導入している\[9\]。

[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")は[日本語](../Page/日本語.md "wikilink")の[組版](../Page/組版.md "wikilink")処理において必要とされる可能性がある字体の区別をCJK互換漢字に頼らずUnicodeのプレーンテキスト上で維持するために、[Adobe-Japan1](../Page/Adobe-Japan1.md "wikilink")-6の異体字集合をUnicodeの漢字字形データベース (Ideographic Variation Database) に登録申請し\[10\]、[2007年](../Page/2007年.md "wikilink")[12月14日](../Page/12月14日.md "wikilink")に登録された\[11\]（詳細は[異体字セレクタ](../Page/異体字セレクタ.md "wikilink")を参照）。

2013年9月制定のUnicode6.3ではこれとは別に[基本多言語面](../Page/基本多言語面.md "wikilink")の異体字セレクタを使用するStandardized Variantsとして、互換漢字用の異体字セレクタが登録された\[12\]。互換漢字ブロックおよびその補助集合にある統合漢字扱いする12字を除く1002文字全てを含んでいる。字形でなくKS X 1001の読みの違いによる重複収録やBig5の誤って重複収録されたものに対応する互換漢字も登録されている。\[13\]

## JIS X 0213用の互換漢字一覧

以下にJIS X 0213用の互換漢字の一覧を示す。\[14\]

| 互換漢字              | 正規化後の代表字 |
| ----------------- | -------- |
| 面区点               | Unicode  |
| KS X 1001由来の互換漢字  |          |
| 1-86-27           | U+F91D   |
| 1-84-14           | U+F928   |
| 1-85-46           | U+F929   |
| 1-91-47           | U+F936   |
| 1-86-41           | U+F970   |
| 1-94-04           | U+F9D0   |
| 1-93-61           | U+F9DC   |
| IBM拡張漢字由来の互換漢字    |          |
| 1-15-43           | U+FA0F   |
| 1-15-55           | U+FA10   |
| 1-47-82           | U+FA11   |
| 2-14-89           | U+FA13   |
| 1-85-90           | U+FA14   |
| 1-87-58           | U+FA15   |
| 1-87-79           | U+FA16   |
| 1-89-28           | U+FA19   |
| 1-89-29           | U+FA1A   |
| 1-89-33           | U+FA1B   |
| 1-91-26           | U+FA1F   |
| 2-87-24           | U+FA20   |
| 2-87-37           | U+FA21   |
| 1-92-14           | U+FA22   |
| 2-89-78           | U+FA24   |
| 1-92-74           | U+FA26   |
| JIS X 0213由来の互換漢字 |          |
| 1-14-24           | U+FA30   |
| 1-14-41           | U+FA31   |
| 1-14-48           | U+FA32   |
| 1-14-67           | U+FA33   |
| 1-14-72           | U+FA34   |
| 1-14-78           | U+FA35   |
| 1-15-12           | U+FA36   |
| 1-15-15           | U+FA37   |
| 1-15-22           | U+FA38   |
| 1-15-58           | U+FA39   |
| 1-15-62           | U+FA3A   |
| 1-47-65           | U+FA3B   |
| 1-47-66           | U+FA3C   |
| 1-84-48           | U+FA3D   |
| 1-84-60           | U+FA3E   |
| 1-84-62           | U+FA3F   |
| 1-84-65           | U+FA40   |
| 1-85-08           | U+FA41   |
| 1-85-11           | U+FA42   |
| 1-85-35           | U+FA43   |
| 1-85-69           | U+FA44   |
| 1-86-73           | U+FA45   |
| 1-86-87           | U+FA46   |
| 1-87-05           | U+FA47   |
| 1-87-53           | U+FA48   |
| 2-80-09           | U+FA49   |
| 1-88-05           | U+FA4A   |
| 1-89-07           | U+FA4B   |
| 1-89-19           | U+FA4C   |
| 1-89-20           | U+FA4D   |
| 1-89-23           | U+FA4E   |
| 1-89-24           | U+FA4F   |
| 1-89-25           | U+FA50   |
| 1-89-27           | U+FA51   |
| 1-89-31           | U+FA52   |
| 1-89-32           | U+FA53   |
| 1-89-45           | U+FA54   |
| 1-89-49           | U+FA55   |
| 1-89-68           | U+FA56   |
| 1-90-14           | U+FA57   |
| 2-84-48           | U+FA58   |
| 1-90-19           | U+FA59   |
| 1-90-26           | U+FA5A   |
| 1-90-36           | U+FA5B   |
| 1-90-56           | U+FA5C   |
| 2-85-84           | U+FA5D   |
| 2-85-85           | U+FA5E   |
| 1-91-07           | U+FA5F   |
| 1-91-79           | U+FA60   |
| 1-91-89           | U+FA61   |
| 1-92-15           | U+FA62   |
| 1-92-16           | U+FA63   |
| 1-92-24           | U+FA64   |
| 1-92-29           | U+FA65   |
| 2-89-73           | U+FA66   |
| 1-92-57           | U+FA67   |
| 1-93-67           | U+FA68   |
| 1-93-86           | U+FA69   |
| 1-93-91           | U+FA6A   |

## 日本文字（JIS X 0213以外）の互換漢字一覧

日本文字の文字集合の内、JIS X 0213に含まれないCJK互換漢字の一覧を以下に示す。

| 互換漢字           | 正規化後の代表字 |
| -------------- | -------- |
| 面区点            | Unicode  |
| IBM拡張漢字由来の互換漢字 |          |
| \-             | U+FA0E   |
| \-             | U+FA12   |
| \-             | U+FA17   |
| \-             | U+FA18   |
| \-             | U+FA1C   |
| \-             | U+FA1D   |
| \-             | U+FA1E   |
| \-             | U+FA23   |
| \-             | U+FA25   |
| \-             | U+FA27   |
| \-             | U+FA28   |
| \-             | U+FA29   |
| \-             | U+FA2A   |
| \-             | U+FA2B   |
| \-             | U+FA2C   |
| \-             | U+FA2D   |
| ARIB外字由来の互換漢字  |          |
| \-             | U+FA6B   |
| \-             | U+FA6C   |
| \-             | U+FA6D   |

### 游明朝で入力可能な互換漢字

[文字コード表 (Windows)](../Page/文字コード表_\(Windows\).md "wikilink")（charmap.exe）でフォントを[游明朝とし](https://ja.wikipedia.org/wiki/游書体#游明朝体 "wikilink")、入力可能なCJK互換漢字として以下の文字が追加されている。

  - (U+F909)、(U+F91F)、(U+F95F)、(U+F983)、(U+F992)、(U+F993)、(U+F999)、(U+F99A)、(U+F9A2)、(U+F9C3)、(U+F9EC)、(U+FA03)

## KS X 1001由来の互換漢字一覧

上述のようにKS X 1001には同じ形でも複数の読みを持つ268文字が重複して符号化されており、それらはUnicodeでは互換漢字として収録された。この268文字のうち、208文字は漢字語の先頭に現れる漢字の特別な読み方（頭音法則）に対応する。例えば[盧武鉉](../Page/盧武鉉.md "wikilink")元大統領の「盧」の文字は元来は「ロ」（）と発音し、これはKS X 1001の54区52点 (U+76E7) になるが、語頭に限り「ノ」（）と発音し、これはKS X 1001の50区38点 (U+F933) に対応する。以下にKS X 1001の互換漢字の一覧を示す\[15\]。

| 代表字    | 互換漢字    |
| ------ | ------- |
| 区点     | Unicode |
| 42-25  | U+8CC8  |
| 43-29  | U+964D  |
| 44-24  | U+898B  |
| 44-58  | U+66F4  |
| 44-88  | U+5951  |
| 45-90  | U+4E32  |
| 46-09  | U+5ED3  |
| 47-03  | U+53E5  |
| 47-47  | U+9F9C  |
| 48-24  | U+F908  |
| 49-34  | U+8C48  |
| 49-49  | U+91D1  |
| 49-57  | U+62CF  |
| 49-71  | U+8AFE  |
| 50-15  | U+5948  |
| 50-19  | U+5973  |
| 50-20  | U+5E74  |
| 50-21  | U+649A  |
| 50-22  | U+79CA  |
| 50-23  | U+5FF5  |
| 50-26  | U+637B  |
| 50-27  | U+5BE7  |
| 71-12  | U+F9AA  |
| 50-33  | U+6012  |
| 50-67  | U+5C3F  |
| 50-78  | U+677B  |
| 50-79  | U+7D10  |
| 50-90  | U+6CE5  |
| 50-91  | U+533F  |
| 50-92  | U+6EBA  |
| 50-94  | U+8336  |
| 51-01  | U+4E39  |
| 51-56  | U+7CD6  |
| 51-75  | U+5B85  |
| 51-88  | U+5EA6  |
| 52-33  | U+8B80  |
| 52-55  | U+6D1E  |
| 52-90  | U+5587  |
| 52-91  | U+61F6  |
| 52-93  | U+7669  |
| 52-94  | U+7F85  |
| 53-01  | U+863F  |
| 53-02  | U+87BA  |
| 53-03  | U+88F8  |
| 53-04  | U+908F  |
| 53-06  | U+6D1B  |
| 53-07  | U+70D9  |
| 53-08  | U+73DE  |
| 53-10  | U+843D  |
| 53-12  | U+916A  |
| 53-13  | U+99F1  |
| 53-15  | U+4E82  |
| 53-16  | U+5375  |
| 53-17  | U+6B04  |
| 53-20  | U+721B  |
| 53-21  | U+862D  |
| 53-22  | U+9E1E  |
| 53-25  | U+5D50  |
| 53-29  | U+6FEB  |
| 53-32  | U+85CD  |
| 53-33  | U+8964  |
| 53-35  | U+62C9  |
| 53-36  | U+81D8  |
| 53-37  | U+881F  |
| 53-38  | U+5ECA  |
| 53-39  | U+6717  |
| 53-40  | U+6D6A  |
| 53-41  | U+72FC  |
| 53-45  | U+90DE  |
| U+FA2E | 郞       |
| 53-46  | U+4F86  |
| 53-50  | U+51B7  |
| 53-51  | U+63A0  |
| 53-52  | U+7565  |
| 53-53  | U+4EAE  |
| 53-55  | U+5169  |
| 53-56  | U+51C9  |
| 53-57  | U+6881  |
| 53-61  | U+7CE7  |
| 53-62  | U+826F  |
| 53-63  | U+8AD2  |
| 53-65  | U+91CF  |
| 53-68  | U+52F5  |
| 53-69  | U+5442  |
| 53-70  | U+5EEC  |
| 53-73  | U+65C5  |
| 53-75  | U+6FFE  |
| 53-76  | U+792A  |
| 53-79  | U+95AD  |
| 53-81  | U+9A6A  |
| 53-82  | U+9E97  |
| 53-83  | U+9ECE  |
| 53-84  | U+529B  |
| 53-85  | U+66C6  |
| 53-86  | U+6B77  |
| 53-89  | U+8F62  |
| 53-91  | U+6190  |
| 53-92  | U+6200  |
| 53-94  | U+6F23  |
| 54-01  | U+7149  |
| 54-02  | U+7489  |
| 54-03  | U+7DF4  |
| 54-04  | U+806F  |
| 54-05  | U+84EE  |
| 54-06  | U+8F26  |
| 54-07  | U+9023  |
| 54-08  | U+934A  |
| 54-10  | U+5217  |
| 54-11  | U+52A3  |
| 54-13  | U+70C8  |
| 54-14  | U+88C2  |
| 54-15  | U+5EC9  |
| 54-17  | U+6BAE  |
| 54-19  | U+7C3E  |
| 54-20  | U+7375  |
| 54-21  | U+4EE4  |
| 54-23  | U+56F9  |
| 54-26  | U+5DBA  |
| 54-27  | U+601C  |
| 54-28  | U+73B2  |
| 54-30  | U+7F9A  |
| 54-32  | U+8046  |
| 54-34  | U+9234  |
| 54-35  | U+96F6  |
| 54-36  | U+9748  |
| 54-37  | U+9818  |
| 54-39  | U+4F8B  |
| 54-41  | U+79AE  |
| 54-42  | U+91B4  |
| 54-43  | U+96B7  |
| U+FA2F | 隷       |
| 54-44  | U+52DE  |
| 54-47  | U+64C4  |
| 54-48  | U+6AD3  |
| 54-51  | U+7210  |
| 54-52  | U+76E7  |
| 54-53  | U+8001  |
| 54-54  | U+8606  |
| 54-55  | U+865C  |
| 54-56  | U+8DEF  |
| 54-58  | U+9732  |
| 54-59  | U+9B6F  |
| 54-60  | U+9DFA  |
| 54-62  | U+788C  |
| 54-63  | U+797F  |
| 54-64  | U+7DA0  |
| 54-65  | U+83C9  |
| 54-66  | U+9304  |
| 54-67  | U+9E7F  |
| 54-69  | U+8AD6  |
| 54-70  | U+58DF  |
| 54-71  | U+5F04  |
| 54-75  | U+7C60  |
| 54-76  | U+807E  |
| 54-79  | U+7262  |
| 54-80  | U+78CA  |
| 54-81  | U+8CC2  |
| 54-84  | U+96F7  |
| 54-85  | U+4E86  |
| 54-86  | U+50DA  |
| 54-87  | U+5BEE  |
| 54-89  | U+6599  |
| 54-90  | U+71CE  |
| 54-91  | U+7642  |
| 54-94  | U+84FC  |
| 55-01  | U+907C  |
| 55-03  | U+9F8D  |
| 55-04  | U+58D8  |
| 55-06  | U+5C62  |
| 55-07  | U+6A13  |
| 55-08  | U+6DDA  |
| 55-09  | U+6F0F  |
| 55-11  | U+7D2F  |
| 55-12  | U+7E37  |
| 55-16  | U+964B  |
| 55-17  | U+5289  |
| 55-19  | U+67F3  |
| 55-21  | U+6D41  |
| 55-22  | U+6E9C  |
| 55-24  | U+7409  |
| 55-26  | U+7559  |
| 55-28  | U+786B  |
| 55-30  | U+985E  |
| 55-31  | U+516D  |
| 55-32  | U+622E  |
| 55-33  | U+9678  |
| 55-35  | U+502B  |
| 55-36  | U+5D19  |
| 55-37  | U+6DEA  |
| 55-39  | U+8F2A  |
| 55-40  | U+5F8B  |
| 55-41  | U+6144  |
| 55-42  | U+6817  |
| 55-44  | U+9686  |
| 55-45  | U+52D2  |
| 55-46  | U+808B  |
| 55-47  | U+51DC  |
| 55-48  | U+51CC  |
| 55-50  | U+7A1C  |
| 55-51  | U+7DBE  |
| 55-52  | U+83F1  |
| 55-53  | U+9675  |
| 55-55  | U+5229  |
| 55-57  | U+540F  |
| 55-59  | U+5C65  |
| 55-61  | U+674E  |
| 55-62  | U+68A8  |
| 55-66  | U+7406  |
| 55-69  | U+75E2  |
| 55-71  | U+7F79  |
| 55-74  | U+88CF  |
| 55-75  | U+88E1  |
| 55-76  | U+91CC  |
| 55-78  | U+96E2  |
| 55-80  | U+541D  |
| 55-82  | U+71D0  |
| 55-83  | U+7498  |
| 55-84  | U+85FA  |
| 55-86  | U+96A3  |
| 55-87  | U+9C57  |
| 55-88  | U+9E9F  |
| 55-89  | U+6797  |
| 55-90  | U+6DCB  |
| 55-92  | U+81E8  |
| 56-01  | U+7ACB  |
| 56-02  | U+7B20  |
| 56-03  | U+7C92  |
| 58-82  | U+78FB  |
| 60-54  | U+5FA9  |
| 60-63  | U+8F3B  |
| 60-84  | U+4E0D  |
| 61-33  | U+5317  |
| 63-15  | U+6BBA  |
| 63-50  | U+72C0  |
| 63-61  | U+585E  |
| 63-67  | U+7D22  |
| 64-67  | U+8AAA  |
| 70-82  | U+F9A1  |
| 64-93  | U+7701  |
| 65-67  | U+7387  |
| 75-50  | U+F9DB  |
| 66-06  | U+6578  |
| 67-06  | U+62FE  |
| 67-59  | U+8B58  |
| 68-07  | U+4EC0  |
| 68-34  | U+60E1  |
| 68-37  | U+6A02  |
| 53-05  | U+F95C  |
| 72-89  | U+F9BF  |
| 69-20  | U+82E5  |
| 70-22  | U+6613  |
| 71-08  | U+8449  |
| 72-54  | U+962E  |
| 76-22  | U+7570  |
| 76-54  | U+54BD  |
| 77-09  | U+523A  |
| 77-19  | U+7099  |
| 79-23  | U+5207  |
| 82-67  | U+8FB0  |
| 83-19  | U+8ECA  |
| 83-49  | U+53C3  |
| 84-12  | U+62D3  |
| 86-56  | U+6C88  |
| 88-21  | U+4FBF  |
| 88-76  | U+66B4  |
| 89-18  | U+6CCC  |
| 90-28  | U+884C  |
| 91-09  | U+7469  |
| 92-33  | U+6ED1  |
| 93-27  | U+6688  |

## 文字コード表

## 履歴

以下の表に挙げられているUnicode関連のドキュメントには、このブロックの特定の文字を定義する目的とプロセスが記録されている。

<table>
<thead>
<tr class="header">
<th><p><a href="https://ja.wikipedia.org/wiki/Unicode#ユニコードのバージョン" title="wikilink">バージョン</a></p></th>
<th></th>
<th><p>文字数</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/情報技術規格国際委員会" title="wikilink">L2</a> ID</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1/SC_2" title="wikilink">WG2</a> ID</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Ideographic_Rapporteur_Group" title="wikilink">IRG</a> ID</p></th>
<th><p>ドキュメント</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.0.1</p></td>
<td><p>U+F900..FA2D</p></td>
<td><p>302</p></td>
<td></td>
<td></td>
<td></td>
<td><p>(to be determined)</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2667.pdf">N2667</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n3525.pdf">N3525</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n3590.pdf">N3590</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n4111.pdf">N4111</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.2</p></td>
<td><p>U+FA30..FA6A</p></td>
<td><p>59</p></td>
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n1935.doc">N1935</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2095.pdf">N2095</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2142.doc">N2142</a></p></td>
<td><p>N710</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2197.pdf">N2197</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2221r.pdf">N2221R</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2273.rtf">N2273</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2295.pdf">N2295</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4.1</p></td>
<td><p>U+FA70..FAD9</p></td>
<td><p>106</p></td>
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2254.pdf">N2254R</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2375.pdf">N2375</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2375.pdf">N2375</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2478.doc">N2478</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2493.doc">N2493</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2541.doc">N2541</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2540.pdf">N2540</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2566.pdf">N2566</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2572.pdf">N2572</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2573.doc">N2573</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2569.pdf">N2569</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2569.pdf">N2569R</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2776r.pdf">N2776</a></p></td>
<td><p>N1062</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n2924.pdf">N2924R</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n3899.pdf">N3899</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n4111.pdf">N4111</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>5.2</p></td>
<td><p>U+FA6B..FA6D</p></td>
<td><p>3</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n3318.pdf">N3318R</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>6.1</p></td>
<td><p>U+FA2E..FA2F</p></td>
<td><p>2</p></td>
<td></td>
<td><p><a href="http://std.dkuug.dk/jtc1/sc2/wg2/docs/n3747.pdf">N3747</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
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

## 脚注

## 参考資料

用語の日本語表記は原則として次にならった。

## 関連項目

  - [CJK統合漢字](../Page/CJK統合漢字.md "wikilink")
  - [Unicodeの互換文字](../Page/Unicodeの互換文字.md "wikilink")
  - [Template:拡張漢字](https://ja.wikipedia.org/wiki/Template:拡張漢字 "wikilink")

[Category:Unicodeのブロック](https://ja.wikipedia.org/wiki/Category:Unicodeのブロック "wikilink") [Category:漢字](https://ja.wikipedia.org/wiki/Category:漢字 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.