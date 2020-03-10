> この記事は[Multipurpose Internet Mail Extensions](https://ja.wikipedia.org/wiki/Multipurpose_Internet_Mail_Extensions)から翻訳されています。


（**多目的インターネットメール拡張**）は、規格上[US-ASCIIの](https://ja.wikipedia.org/wiki/ASCII "wikilink")[テキストしか使用できない](../Page/プレーンテキスト.md "wikilink")[インターネット](../Page/インターネット.md "wikilink")の[電子メール](../Page/電子メール.md "wikilink")でさまざまなフォーマット（書式）を扱えるようにする規格である。通常は**MIME**（マイム）と略される。RFC 2045、RFC 2046、RFC 2047、RFC 4288、RFC 4289\[1\]、RFC 2049 で規定されている。

## 概要

インターネットでメールの書式を定めている RFC 5322 (旧 RFC 822、RFC 2822)では、[英数字](https://ja.wikipedia.org/wiki/英数字 "wikilink")といくつかの記号を7 ビットで表現する「US-ASCII」と呼ばれる文字コードを利用し、1行あたり1000 バイト(改行を含む)のテキストデータしか許していない。そのため、規格に不適合になるような長い行、US-ASCIIだけで表現できない文字や、[バイナリ](../Page/バイナリ.md "wikilink")データ、[画像](../Page/画像.md "wikilink")、[音声](https://ja.wikipedia.org/wiki/音声 "wikilink")などの非文字データを利用することができなかった。

MIMEはこれらのデータを取り扱うために新しくいくつかのヘッダを定義し、かつUS-ASCII上でさまざまなデータタイプを表現するための[符号化方式](../Page/符号化方式.md "wikilink")を規定している。

RFC 5322 (旧 RFC 822、RFC 2822)では1 通のメールで1つの本文しか扱うことができないが、MIMEでは本文を分割して複数のコンテンツを扱うことができるようにした。これを**マルチパート**と呼ぶ。MIMEヘッダには、MIMEメッセージヘッダとMIMEパートヘッダの二つがある。MIMEメッセージヘッダはメッセージ全体に適用され、MIMEパートヘッダはマルチパートメッセージの各部分に適用される。マルチパートにより、1つのメールに複数の種類のファイルを扱うことができるようになった。

また、[HTTPにおけるデータの伝送に関しても](../Page/Hypertext_Transfer_Protocol.md "wikilink")、MIMEの枠組みが援用されている。

## MIMEで導入されたヘッダ

### MIME-Version

従来のRFC 5322 (RFC 822, RFC 2822) 準拠のメッセージとの区別、あるいは将来MIMEが拡張されたときにバージョンを区別するためのヘッダ。現在は1.0のみが規定されている。

`Mime-Version: 1.0`

### Content-Type

このメッセージ中のデータの種類を指定する。 一般的な書式は次の通り。

`Content-Type: `*`type`*`/`*`subtype`*`; `*`parameter`*

*type*は大分類となるデータの種類を指定する。*subtype*にはより詳細な形式を指定する。*parameter*は追加の情報を指定するもので、複数指定できる。電子メールメッセージにおいて使われる例を以下に示す。

  - `text/plain; charset=iso-2022-jp; format=flowed; delsp=yes`（[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")、[ISO-2022-JP](../Page/ISO-2022-JP.md "wikilink")、RFC 3676 で規定されるflowedおよびdelspの文字列折り返し処理を適用）
  - `text/html; charset=UTF-8`（[HTMLテキスト](../Page/HyperText_Markup_Language.md "wikilink")、[UTF-8](../Page/UTF-8.md "wikilink")）
  - `multipart/alternative`（[HTMLメールにおいて](https://ja.wikipedia.org/wiki/HTML電子メール "wikilink")、HTMLによるメッセージと同等のプレーンテキストによるメッセージを用意する場合のように、同じ情報を異なる形式で表したマルチパート）

*type*毎に未知の*subtype*の扱いが規定されており、受信側は自分の扱えない*subtype*であっても最低限の取り扱いが可能となる。`text` の場合は `text/plain`、`application/octet-stream`、`multipart` の場合は `multipart/mixed` である。`application`、`image`、`audio`、`video`などは、未知の*subtype*について`application/octet-stream`として扱うよう規定している。

### `Content-Transfer-Encoding`

MIMEではUS-ASCIIだけでなくデータのさまざまな符号化方法の指定がこのヘッダで可能になっている。 書式は以下の通り。

`Content-Transfer-Encoding: `*`mechanism`*

*mechanism*として、`7bit`、`8bit`、`binary`、`quoted-printable`、`base64` が指定できる。一般的に利用できるのは `7bit`、`quoted-printable`、`base64` であり、`8bit`、`binary` は一定の条件を満たす場合しか利用できない。

#### `7bit`

デフォルト値。7 ビットのテキストを表す。`Content-Transfer-Encoding` ヘッダフィールドを省略した場合は、この `7bit` を指定したのと同じ意味となる。US-ASCIIや[ISO-2022-JP](../Page/ISO-2022-JP.md "wikilink")は確実に7 ビットのテキストであるため、これにあたる。

#### `8bit`

8 ビットのテキストを表す。 RFC 5322 (旧RFC 822、RFC 2822)は7 ビットのテキストを前提としており、この8bitは意図的に違反するものである。メールを転送するための[SMTPは基本的に](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")7 ビットのテキストしか転送できないため、このエンコーディングを用いることはできない。RFC 1652で定義されるSMTPの拡張(ESMTP)の**8BITMIME**を用いるか、8 ビットを許容するような全く別のプロトコルを用いた場合のみ、利用が可能である。

#### `binary`

データがテキストではなくバイナリであることを表す。RFC 5322 (旧RFC 822、RFC 2822)はテキストを前提としており、このbinaryは意図的に違反するものである。SMTPは基本的に行単位でデータを扱うため、行の概念すらないバイナリは転送できない。RFC 3030で定義されるESMTPの1つである**BINARYMIME**を用いるか、バイナリを許容するような全く別のプロトコルを用いた場合のみ、利用が可能である。

#### `quoted-printable`

US-ASCIIに存在する文字はそのまま使い、存在しない文字などを `=`*HH*のような形で符号化する。ここで、*HH* には文字のコードを大文字の16進数で指定する。その他、以下のような規則がある。

  - `=` 自体は `=3D` となる。
  - 行末に空白がある場合、伝送の過程で失われるおそれがあるため、`=20` としてこれを保存する。
  - エンコードの過程で行を折り返す（改行を挿入する）場合、`=` と改行の組み合わせを挿入し、もともとあった改行と区別できるようにする。

ヨーロッパ系の言語では、多くの文字がUS-ASCIIと同一で一部に独自の文字を使っているものが多い。 この場合に `quoted-printable` を用いると、US-ASCIIはそのままの文字を使用しているので、データがほとんど大きくならず、`quoted-pritable` 対応プログラムを使わなくても、大体の内容が読めるという利点がある。 しかし通常のバイナリデータや、[Shift_JIS](../Page/Shift_JIS.md "wikilink")や[EUC-JP](../Page/EUC-JP.md "wikilink")といった仮名漢字などの非ヨーロッパ系の文字のテキストデータに `quoted-printable` を適用した場合は、[base64](https://ja.wikipedia.org/wiki/base64 "wikilink")を使用した場合よりも大幅にデータが大きくなる。

#### `base64`

3[オクテット](../Page/8ビット.md "wikilink")（24 ビット）を6 ビットずつ4つに分割し、各6 ビットの値に対してそれぞれUS-ASCIIの64 文字（英字52 文字、数字10 文字、「+」、「/」）を割り当てる符号化方式。

この符号化によって、[SMTPなどUS](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")-ASCIIしか許されていない通信路でもバイナリデータを交換できるメリットはあるが、データ容量は約33%増加する。

## ヘッダでの非US-ASCII 文字の扱い

上記のヘッダの導入によって、body部のデータタイプや符号化方式は指定できるようになったが、このままではヘッダ部は相変わらずUS-ASCIIしか利用できない。MIMEではRFC 2047やRFC 2231によって、ヘッダ部分での非US-ASCII文字の扱いを規定している。RFC 2047によれば、

`=?`*`charset`*`?`*`encoding`*`?`*`encoded-text`*`?=`

という形式により、[文字コード](../Page/文字コード.md "wikilink")系が*charset*、[符号化方法が](../Page/符号化方式.md "wikilink")*encoding*で、*encoded-text*と符号化された単語を表現できる。*charset*は `Content-Type:text/plain` における `charset` パラメータで指定するのと同じ、[IANAに登録された文字列を用いる](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")。*encoding* は `Q` または `B`（大文字でも小文字でもよい）であり、前者はほぼ `quoted-printable` と同じ符号化方法、後者は `base64`を用いることを表す。

  - RFC 2047では、「`"`」で囲まれた中でこのような符号化された単語を解釈することはできない、とされている。したがって、「`"=?ISO-2022-JP?B?GyRCRnxLXDhsGyhC?="`」は「`=?ISO-2022-JP?B?GyRCRnxLXDhsGyhC?=`」と解釈しなければならず、これを「日本語」と解釈することは、規格違反となる。しかし、[Microsoft Outlook Expressなど](https://ja.wikipedia.org/wiki/Outlook_Express "wikilink")、一部の[MUAがこのような誤った符号化を実装してそれが普及してしまったため](../Page/電子メールクライアント.md "wikilink")、それを規格違反と知っているMUAの作者も、それに対応することを余儀なくされている。

<!-- end list -->

  - RFC 2231では、MIMEパラメータの値に非US-ASCII文字を指定する方法を規定している。これによれば、[添付ファイル](https://ja.wikipedia.org/wiki/添付ファイル "wikilink")名など、MIMEパラメータの値としての「`ISO-2022-JP''%1B$BF|K%5C8l%1B%28B`」を「日本語」と解釈することができる\[2\]。また、RFC 5322に適合しない長さの文字列を短く分割して指定する方法も規定している。

## 脚注

## 関連項目

  - [拡張子](../Page/拡張子.md "wikilink")
  - [電子メール](../Page/電子メール.md "wikilink")
  - [SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink") (Simple Mail Transfer Protocol)
  - [MHTML](../Page/MHTML.md "wikilink") (MIME Encapsulation of Aggregate HTML Documents)
  - [S/MIME](https://ja.wikipedia.org/wiki/S/MIME "wikilink") (Secure / Multipurpose Internet Mail Extensions)

[Category:電子メールのプロトコル](https://ja.wikipedia.org/wiki/Category:電子メールのプロトコル "wikilink") [Category:Hypertext_Transfer_Protocol](https://ja.wikipedia.org/wiki/Category:Hypertext_Transfer_Protocol "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.  旧RFC 2048。
2.  「`''`」は、二重引用符ではなく、2 個の単引用符である。