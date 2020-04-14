> この記事は[Abstract Syntax Notation One](https://ja.wikipedia.org/wiki/Abstract_Syntax_Notation_One)から翻訳されています。


**Abstract Syntax Notation One**（**ASN.1**）とは、[電気通信](../Page/電気通信.md "wikilink")や[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")での[データ構造](../Page/データ構造.md "wikilink")の表現・エンコード・転送・デコードを記述する標準的かつ柔軟な記法である。マシン固有の技法などに依存せず、曖昧さのない記述を可能とする形式規則を提供する。

[1984年](../Page/1984年.md "wikilink")、CCITT X.409: 1984 の一部として、[ISOと](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")[ITU-T](../Page/ITU-T.md "wikilink")が策定した。ASN.1 はその適用範囲の広さから、[1988年](../Page/1988年.md "wikilink")に **X.208** として独立することとなった。[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")、改訂版が **X.680** シリーズとなっている。

## データ転送における ASN.1

ASN.1 は情報の[抽象構文](https://ja.wikipedia.org/wiki/抽象構文 "wikilink")を定義するが、情報の符号化方法を限定するものではない。抽象構文をASN.1で記述されたデータを転送する際の ASN.1 符号化規則が各種用意されている。

ASN.1 の標準符号化規則として以下のものがある。

  - [Basic Encoding Rules](https://ja.wikipedia.org/wiki/:en:Basic_Encoding_Rules "wikilink") (BER)
  - [Canonical Encoding Rules](https://ja.wikipedia.org/wiki/:en:Canonical_Encoding_Rules "wikilink") (CER)
  - [Distinguished Encoding Rules](https://ja.wikipedia.org/wiki/:en:Distinguished_Encoding_Rules "wikilink") (DER)
  - [XML Encoding Rules](https://ja.wikipedia.org/wiki/:en:XML_Encoding_Rules "wikilink") (XER)
  - [Packed Encoding Rules](https://ja.wikipedia.org/wiki/:en:Packed_Encoding_Rules "wikilink") (PER)
  - [Generic String Encoding Rules](https://ja.wikipedia.org/wiki/:en:Generic_String_Encoding_Rules "wikilink") (GSER)

ASN.1記法と特定のASN.1符号化規則を使うことで、マシンのアーキテクチャや実装言語に依存しない形式で、ネットワーク上のアプリケーション間でやりとりするデータ構造を定めることができる。

[X.400](../Page/X.400.md "wikilink") [電子メール](../Page/電子メール.md "wikilink")、[X.500](../Page/X.500.md "wikilink") あるいは [LDAP](../Page/Lightweight_Directory_Access_Protocol.md "wikilink") [ディレクトリ・サービス](../Page/ディレクトリ・サービス.md "wikilink")、[H.323](../Page/H.323.md "wikilink")（[VoIP](../Page/VoIP.md "wikilink")）、[SNMP](../Page/Simple_Network_Management_Protocol.md "wikilink")、[BACnet](https://ja.wikipedia.org/wiki/BACnet "wikilink") といったアプリケーション層のプロトコルは ASN.1 を使って[Protocol Data Unitを規定する](../Page/Protocol_Data_Unit.md "wikilink")。[UMTS](https://ja.wikipedia.org/wiki/UMTS "wikilink")でも使われている。他にも ASN.1 の応用範囲は様々である[1](http://www.itu.int/en/ITU-T/asn1/Pages/Application-fields-of-ASN-1.aspx)。

## 例

ASN.1 記法で FooProtocol のデータ構造を定義したものを以下に示す。

これが Foo プロトコル作成者が公開する仕様となる。ASN.1 はプロトコルの手順（流れ）を定義しない。その部分は文章で説明される。

ここで、Foo プロトコル準拠のメッセージを他の誰かに送るとする。このメッセージ（[PDU](../Page/Protocol_Data_Unit.md "wikilink")）は以下のようになっている。

ASN.1 は、値とサイズの制限および拡張性をサポートする。上記仕様は次のように変更可能である。

この変更は trackingNumber が持つ値を 0 から 199 までに、questionNumbers が持つ値を 10 から 20 までに制限する。questions 配列のサイズは 0個から10個であり、answers 配列の数は 1個から10個である。anArray フィールドは 0 から 1000 までの範囲の整数が常に100 個である。上記中の '...' は拡張性マーカーであり、将来バージョンのFooHistoryメッセージ仕様にフィールドが追加される可能性があることを示す。このバージョンに準拠するシステムは、処理の対象はこのバージョンのフィールドのみであっても、将来バージョンのトランザクションを受信および転送できる必要がある。

優れた ASN.1 コンパイラは、トランザクションがこれらの制約に従っていることを自動的にチェックするソースコードを (C, C++, Java 等) で生成する。制約に違反するトランザクションは、アプリケーションから受理されず、送信もされない。このレイヤにおける制約管理は、アプリケーションを制約違反から守り、プロトコル仕様を非常にシンプルにする。それにより、リスクとコストが削減される。

このメッセージをネットワーク経由で送るには、これをビット列に符号化しなければならない。ASN.1 にはそのためのアルゴリズムが各種用意されていて、「符号化規則（encoding rule）」と呼ばれている。最も単純な規則は *Distinguished Encoding Rules* (*DER*) である。

Foo プロトコル仕様では、どの符号化規則を採用するかを明確に決めておかなければならない。それによって、Foo プロトコルのユーザー間で（例えば）DER を使うという共通認識ができる。

### DER による符号化例

上掲のデータ構造（制約と拡張性の無いもの）を DER 形式に符号化すると次のようになる。

<table>
<thead>
<tr class="header">
<th></th>
<th><p>タグ SEQUENCE</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>オクテット長</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>タグ INTEGER</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>オクテット長</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>値</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>タグ VisibleString</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>オクテット長</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>値（ASCII での "Anybody there?"）</p></td>
</tr>
</tbody>
</table>

すなわち、DER での符号化パターンは「[型-長さ-値](https://ja.wikipedia.org/wiki/Type-length-value "wikilink")」の組の羅列である。従って、符号化によって得られるのは以下の21オクテットのデータ列である。

  -

ASN.1 と DER の関わる範囲はここまでである。これを実際に転送する方法は ASN.1 とは無関係に決められる（つまり、[TCPを使おうと他のプロトコルを使おうと関係ない](../Page/Transmission_Control_Protocol.md "wikilink")）。受信側は受信したオクテット列を DER に従ってデコードできる。

### XER による符号化例

同じ ASN.1 データ構造を XER (*XML Encoding Rules*) で符号化し、人間にも読める形式にすることもできる。例の場合、以下の108オクテットになる。

### PER による符号化例

Packed Encoding Rules を使うと、以下のように 16 オクテット以内に符号化できる。

  -

## ASN.1 とその他のデータ構造定義

[通信プロトコル](../Page/通信プロトコル.md "wikilink")のメッセージを定義する場合、ASN.1 では主にバイナリ符号化規則が使われる。

他のインターネットでよく使われるアプリケーション層のプロトコル（[HTTPや](../Page/Hypertext_Transfer_Protocol.md "wikilink")[SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")）では、メッセージ定義にはタグと値が使われ、時には[ABNF](../Page/ABNF.md "wikilink")記法が使われる。それらの定義には符号化も含まれるが、テキストによる符号化である。

これら2つの手法はそれぞれに利点があり、議論が数多く行われてきた。ASN.1 の手法は効率がよいとされており、Packed Encoding Rules ではさらにコンパクトな符号化を実現できる。テキストを使った手法は実装が容易でデバッグが容易とされている（人間が符号化されたメッセージを読めるため）。[Megaco](https://ja.wikipedia.org/wiki/Megaco "wikilink")（H.248）プロトコルでは、どちらの符号化がよいかを決められず、ASN.1 に基づいた符号化と ABNF に基づいた符号化の両方が定義されている。

ASN.1 の XML Encoding Rules (XER) はこのギャップを埋めるべく、ASN.1 記法で定義された構造をテキスト符号化する方法を提供する。類似の Generic String Encoding Rules は特にユーザーとのやりとりのために定義された符号化規則である。

## ASN.1 の実際の利用

ASN.1 [コンパイラ](../Page/コンパイラ.md "wikilink")を使って、ASN.1 記法によるコードから、等価なデータ構造を表現する適当なコード（例えば[C言語](../Page/C言語.md "wikilink")のソースコード）を生成する場合もある。このコードとランタイムライブラリにより、符号化されたデータ構造と言語が理解できる表現の間で双方向の変換が可能となる。あるいは、人間の手でエンコード・デコードのルーチンを書く場合もある。

## 標準

ASN.1記法を説明した標準 ([free download from the ITU-T website](http://www.itu.int/ITU-T/studygroups/com17/languages/)):

  - ITU-T Rec. X.680 | ISO/IEC 8824-1
  - ITU-T Rec. X.681 | ISO/IEC 8824-2
  - ITU-T Rec. X.682 | ISO/IEC 8824-3
  - ITU-T Rec. X.683 | ISO/IEC 8824-4

ASN.1符号化規則を説明した標準 ([free download from the ITU-T website](http://www.itu.int/ITU-T/studygroups/com17/languages/)):

  - ITU-T Rec. X.690 | ISO/IEC 8825-1 (BER, CER and DER)
  - ITU-T Rec. X.691 | ISO/IEC 8825-2 (PER)
  - ITU-T Rec. X.693 | ISO/IEC 8825-4 (XER)
  - ITU-T Rec. X.694 | ISO/IEC 8825-5 (XSD mapping)
  - RFC 3641 (GSER)

対応する[日本工業規格](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink")

  - [JIS X 5603:1990 ASN.1仕様](https://www.jisc.go.jp/app/jis/general/GnrJISNumberNameSearchList?show&jisStdNo=X5603)
  - [JIS X 5604:1990 ASN.1基本符号化規則仕様](https://www.jisc.go.jp/app/jis/general/GnrDisuseJISStandardList?show&jisStdNo=X5604)（廃止）
  - [JIS X 5605](https://www.jisc.go.jp/app/jis/general/GnrDisuseJISStandardList?show&jisStdNo=X5605)（廃止）
      - JIS X 5605-1:1998 基本記法
      - JIS X 5605-2:1998 情報オブジェクト
      - JIS X 5605-3:1998 制約
      - JIS X 5605-4:1998 パラメータ化
  - [JIS X 5606](https://www.jisc.go.jp/app/jis/general/GnrDisuseJISStandardList?show&jisStdNo=X5606)（廃止）
      - JIS X 5606-1:1998 符号化規則（BER、CER、DER）
      - JIS X 5606-2:1998 符号化規則（PER）

## 関連項目

  - [TTCN](../Page/TTCN.md "wikilink")

## 参考文献

  - [Federal Standard 1037C](https://ja.wikipedia.org/wiki/:en:Federal_Standard_1037C "wikilink")
  - [MIL-STD-188](https://ja.wikipedia.org/wiki/:en:MIL-STD-188 "wikilink").
  - [Other references in French](http://asn1.elibel.tm.fr/fr/biblio/index.htm)

## 外部リンク

  - [The ASN.1 Consortium](http://www.asn1.org/)

  - [A comprehensive ASN.1 information site](http://asn1.elibel.tm.fr/)

  - [asn1c](http://lionet.info/asn1c/), ASN.1 のソースコードを[C言語](../Page/C言語.md "wikilink")のソースコードに変換するオープンソースのコンパイラ

  - [](https://www.marben-products.com/CCArea/asn1tools/free-online-asn1-decoder.html) Free online tool .

  - [pyasn1](http://pyasn1.sf.net): ASN.1 のデータ型とコーデックの[Python](../Page/Python.md "wikilink")による実装

  - [A Layman's Guide to a Subset of ASN.1, BER, and DER](http://luca.ntop.org/Teaching/Appunti/asn1.html): ASN.1, BER および DER の入門的文書

  - [BinaryNotes](http://bnotes.sf.net): オープンソースの ASN.1 フレームワーク。[Java](https://ja.wikipedia.org/wiki/Java "wikilink") および [.NET](https://ja.wikipedia.org/wiki/.NET "wikilink") 向け。

  -
  - [ASN.1概要](http://www5d.biglobe.ne.jp/~stssk/asn1/index.html)

[Category:ITU-T勧告](https://ja.wikipedia.org/wiki/Category:ITU-T勧告 "wikilink") [Category:コンピュータ言語](https://ja.wikipedia.org/wiki/Category:コンピュータ言語 "wikilink") [Category:データシリアライゼーションフォーマット](https://ja.wikipedia.org/wiki/Category:データシリアライゼーションフォーマット "wikilink")