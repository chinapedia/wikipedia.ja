> この記事は[Base64](https://ja.wikipedia.org/wiki/Base64)から翻訳されています。


**Base64**は、[データ](../Page/データ.md "wikilink")を64種類の印字可能な[英数字](https://ja.wikipedia.org/wiki/英数字 "wikilink")のみを用いて、それ以外の文字を扱うことの出来ない通信環境にて[マルチバイト文字](../Page/マルチバイト文字.md "wikilink")や[バイナリ](../Page/バイナリ.md "wikilink")データを扱うための[エンコード](../Page/エンコード.md "wikilink")方式である。[MIMEによって規定されていて](https://ja.wikipedia.org/wiki/Multipurpose_Internet_Mail_Extensions "wikilink")、7ビットのデータしか扱うことの出来ない[電子メール](../Page/電子メール.md "wikilink")にて広く利用されている。具体的には、`A`–`Z`, `a`–`z`, `0`–`9` までの62文字と、記号2つ (`+`, `/`)、さらにパディング（余った部分を詰める）のための記号として `=` が用いられる。この変換によって、データ量は4/3（約133%）になる\[1\]。また、MIMEの基準では76文字ごとに[改行コード](https://ja.wikipedia.org/wiki/改行コード "wikilink")が入るため、この分の2バイトを計算に入れるとデータ量は約137%となる\[2\]。

## 変換形式

Base64変換の手順を以下に挙げる。

1.  元データを6ビットずつに分割。（6ビットに満たない分は0を追加して6ビットにする）
2.  各6ビットの値を変換表を使って4文字ずつ変換。（4文字に満たない分は `=` 記号を追加して4文字にする）

### 変換例

1.  元データ
      - 文字列: "ABCDEFG"
      - 16進表現: 41, 42, 43, 44, 45, 46, 47
      - 2進表現: 0100 0001, 0100 0010, 0100 0011, 0100 0100, 0100 0101, 0100 0110, 0100 0111
2.  6ビットずつに分割
      - 010000 010100 001001 000011 010001 000100 010101 000110 010001 11
3.  2ビット余るので、4ビット分0を追加して6ビットにする
      - 010000 010100 001001 000011 010001 000100 010101 000110 010001 110000
4.  変換表により、4文字ずつ変換
      - "QUJD", "REVG", "Rw"
5.  2文字余るので、2文字分 = 記号を追加して4文字にする
      - "QUJD", "REVG", "Rw=="
6.  Base64文字列
      - "QUJDREVGRw=="

### 変換表

| 10進 | 2進     | 文字  |  | 10進 | 2進     | 文字  |  | 10進 | 2進     | 文字  |  | 10進 | 2進     | 文字  |
| --- | ------ | --- |  | --- | ------ | --- |  | --- | ------ | --- |  | --- | ------ | --- |
| 0   | 000000 | `A` |  | 16  | 010000 | `Q` |  | 32  | 100000 | `g` |  | 48  | 110000 | `w` |
| 1   | 000001 | `B` |  | 17  | 010001 | `R` |  | 33  | 100001 | `h` |  | 49  | 110001 | `x` |
| 2   | 000010 | `C` |  | 18  | 010010 | `S` |  | 34  | 100010 | `i` |  | 50  | 110010 | `y` |
| 3   | 000011 | `D` |  | 19  | 010011 | `T` |  | 35  | 100011 | `j` |  | 51  | 110011 | `z` |
| 4   | 000100 | `E` |  | 20  | 010100 | `U` |  | 36  | 100100 | `k` |  | 52  | 110100 | `0` |
| 5   | 000101 | `F` |  | 21  | 010101 | `V` |  | 37  | 100101 | `l` |  | 53  | 110101 | `1` |
| 6   | 000110 | `G` |  | 22  | 010110 | `W` |  | 38  | 100110 | `m` |  | 54  | 110110 | `2` |
| 7   | 000111 | `H` |  | 23  | 010111 | `X` |  | 39  | 100111 | `n` |  | 55  | 110111 | `3` |
| 8   | 001000 | `I` |  | 24  | 011000 | `Y` |  | 40  | 101000 | `o` |  | 56  | 111000 | `4` |
| 9   | 001001 | `J` |  | 25  | 011001 | `Z` |  | 41  | 101001 | `p` |  | 57  | 111001 | `5` |
| 10  | 001010 | `K` |  | 26  | 011010 | `a` |  | 42  | 101010 | `q` |  | 58  | 111010 | `6` |
| 11  | 001011 | `L` |  | 27  | 011011 | `b` |  | 43  | 101011 | `r` |  | 59  | 111011 | `7` |
| 12  | 001100 | `M` |  | 28  | 011100 | `c` |  | 44  | 101100 | `s` |  | 60  | 111100 | `8` |
| 13  | 001101 | `N` |  | 29  | 011101 | `d` |  | 45  | 101101 | `t` |  | 61  | 111101 | `9` |
| 14  | 001110 | `O` |  | 30  | 011110 | `e` |  | 46  | 101110 | `u` |  | 62  | 111110 | `+` |
| 15  | 001111 | `P` |  | 31  | 011111 | `f` |  | 47  | 101111 | `v` |  | 63  | 111111 | `/` |

## 主な利用例

### 電子メール

[電子メール](../Page/電子メール.md "wikilink")では、[SMTPなどの制約により](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")、7ビット文字列以外をやり取りすることは出来ない。そのため、添付ファイルなどのバイナリ形式のデータを送信する際に標準的に利用されている。

### Basic認証

[HTTPヘッダでは](../Page/Hypertext_Transfer_Protocol.md "wikilink")、特殊記号を使用することが出来ないため、ユーザー名とパスワードをコロン (`:`) で区切ってBase64エンコードした文字列が[Basic認証](https://ja.wikipedia.org/wiki/Basic認証 "wikilink")に用いられている。

### 電子掲示板

[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")上の[電子掲示板](../Page/電子掲示板.md "wikilink")では、文字列以外のバイナリデータの書き込みは基本的に不可能である。そこで、[画像](../Page/画像.md "wikilink")やテキスト文章を[圧縮したファイルなどをやり取りするために](../Page/データ圧縮.md "wikilink")、この形式が使用されることがある。

## 問題点

このエンコードをするとデータ量が大きく増加するため、特に大きなファイルの送受信などをする場合は、電子メール以外の手段を利用したほうが格段に速い場合がある。また、英文の中に特殊文字が混じっているテキスト文章などは、特殊文字だけをエンコードした方がデータ効率が良く、デコードを行わなくても大体のデータが読めると言う利点がある。（[Quoted-printable](https://ja.wikipedia.org/wiki/Quoted-printable "wikilink")参照）

## 変形版

[URLにBase](../Page/Uniform_Resource_Locator.md "wikilink")64を含ませると、`+` と `/` が問題を引き起こすことがある。これらの文字がURLで特別な意味を持つために `%XX` の形にエスケープする必要が生じるためである。 他にも、`+` と `/` が特別な意味をもつ個所（[正規表現](../Page/正規表現.md "wikilink")など）やその使用が制限される個所（[XMLなど](../Page/Extensible_Markup_Language.md "wikilink")）でBase64を用いるときには、この二文字のかわりに `!`、`-`、`.` 等を用いることがある。

<table>
<thead>
<tr class="header">
<th><p>変形</p></th>
<th><p>62番目の文字</p></th>
<th><p>63番目の文字</p></th>
<th><p>パディング</p></th>
<th><p>1行が固定長か</p></th>
<th><p>行の最大長</p></th>
<th><p>改行文字</p></th>
<th><p>指定された文字以外を使えるかどうか</p></th>
<th><p>行のチェックサム</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>オリジナルの Privacy-Enhanced Mail (PEM) の Base64<br />
(RFC 1421, deprecated)</p></td>
<td><p><code>+</code></p></td>
<td><p><code>/</code></p></td>
<td><p>nowrap| <code>=</code><br />
(必須)</p></td>
<td><p>はい<br />
(最終行を除く)</p></td>
<td><p>64</p></td>
<td><p>CR+LF</p></td>
<td><p>禁止</p></td>
<td><p>(なし)</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Multipurpose_Internet_Mail_Extensions" title="wikilink">MIME</a> の Base64 転送エンコーディング<br />
(RFC 2045)</p></td>
<td><p><code>+</code></p></td>
<td><p><code>/</code></p></td>
<td><p><code>=</code><br />
(必須)</p></td>
<td><p>いいえ<br />
(可変)</p></td>
<td><p>76</p></td>
<td><p>CR+LF</p></td>
<td><p>許可<br />
(破棄される)</p></td>
<td><p>(なし)</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/RFC_3548" title="wikilink">RFC 3548</a> や <a href="https://ja.wikipedia.org/wiki/#RFC_4648" title="wikilink">RFC 4648</a> の標準の 'Base64' エンコーディング</p></td>
<td><p><code>+</code></p></td>
<td><p><code>/</code></p></td>
<td><p><code>=</code><br />
(必須)</p></td>
<td><p>はい<br />
(最終行を除く)</p></td>
<td><p>64 または 76<br />
(改行が必要な場合のみ)</p></td>
<td><p>CR+LF<br />
(改行が必要な場合のみ)</p></td>
<td><p>禁止</p></td>
<td><p>(なし)</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/OpenPGP" title="wikilink">OpenPGP</a>用「Radix-64」<br />
(RFC 4880)</p></td>
<td><p><code>+</code></p></td>
<td><p><code>/</code></p></td>
<td><p><code>=</code><br />
(必須)</p></td>
<td><p>いいえ<br />
(可変)</p></td>
<td><p>76</p></td>
<td><p>CR+LF</p></td>
<td><p>禁止</p></td>
<td><p>24ビットCRC<br />
(Radix-64-encoded, including one <em>pad</em> character)</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/UTF-7" title="wikilink">UTF-7</a> のための変形 Base64<br />
(RFC 1642, obsoleted)</p></td>
<td><p><code>+</code></p></td>
<td><p><code>/</code></p></td>
<td><p>(なし)</p></td>
<td><p>いいえ<br />
(可変)</p></td>
<td><p>(なし)</p></td>
<td><p>(なし)</p></td>
<td><p>禁止</p></td>
<td><p>(なし)</p></td>
</tr>
<tr class="even">
<td><p>ファイル名のための変形 Base64<br />
(非標準)</p></td>
<td><p><code>+</code></p></td>
<td><p><code>-</code></p></td>
<td><p>(なし)</p></td>
<td><p>いいえ<br />
(可変)</p></td>
<td><p>(ファイルシステムの限界、一般には255)</p></td>
<td><p>(なし)</p></td>
<td><p>禁止</p></td>
<td><p>(なし)</p></td>
</tr>
<tr class="odd">
<td><p>URLアプリケーションのための変形 Base64<br />
('base64url' encoding)</p></td>
<td><p><code>-</code></p></td>
<td><p><code>_</code></p></td>
<td><p>(なし)</p></td>
<td><p>いいえ<br />
(可変)</p></td>
<td><p>アプリケーション依存</p></td>
<td><p>(なし)</p></td>
<td><p>禁止</p></td>
<td><p>(なし)</p></td>
</tr>
<tr class="even">
<td><p>XML名前トークン向け修正Base64<br />
(<em>Nmtoken</em>)</p></td>
<td><p><code>.</code></p></td>
<td><p><code>-</code></p></td>
<td><p>(なし)</p></td>
<td><p>いいえ<br />
(可変)</p></td>
<td><p>XML パーサー依存</p></td>
<td><p>(なし)</p></td>
<td><p>禁止</p></td>
<td><p>(なし)</p></td>
</tr>
<tr class="odd">
<td><p>XML識別子向け修正Base64<br />
(<em>Name</em>)</p></td>
<td><p><code>_</code></p></td>
<td><p><code>:</code></p></td>
<td><p>(なし)</p></td>
<td><p>いいえ<br />
(可変)</p></td>
<td><p>XML パーサー依存</p></td>
<td><p>(なし)</p></td>
<td><p>禁止</p></td>
<td><p>(なし)</p></td>
</tr>
<tr class="even">
<td><p>プログラム識別子向け修正Base64<br />
（変種1，非標準）</p></td>
<td><p><code>_</code></p></td>
<td><p><code>-</code></p></td>
<td><p>(なし)</p></td>
<td><p>いいえ<br />
(可変)</p></td>
<td><p>言語・システム依存</p></td>
<td><p>(なし)</p></td>
<td><p>禁止</p></td>
<td><p>(なし)</p></td>
</tr>
<tr class="odd">
<td><p>プログラム識別子向け修正Base64<br />
（変種2，非標準）</p></td>
<td><p><code>.</code></p></td>
<td><p><code>_</code></p></td>
<td><p>(なし)</p></td>
<td><p>いいえ<br />
(可変)</p></td>
<td><p>言語・システム依存</p></td>
<td><p>(なし)</p></td>
<td><p>禁止</p></td>
<td><p>(なし)</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/正規表現.md" title="wikilink">正規表現</a>のための変形 Base64<br />
(非標準)</p></td>
<td><p><code>!</code></p></td>
<td><p><code>-</code></p></td>
<td><p>nowrap| (なし)</p></td>
<td><p>nowrap| いいえ<br />
(可変)</p></td>
<td><p>アプリケーション依存</p></td>
<td><p>(なし)</p></td>
<td><p>禁止</p></td>
<td><p>(なし)</p></td>
</tr>
</tbody>
</table>

## 脚注

## 関連項目

  - [URLエンコード](https://ja.wikipedia.org/wiki/URLエンコード "wikilink")
  - [uuencode](https://ja.wikipedia.org/wiki/uuencode "wikilink")
  - [BinHex](../Page/BinHex.md "wikilink")
  - [ish](https://ja.wikipedia.org/wiki/ish "wikilink")

## 外部リンク

  - [The Base16, Base32, and Base64 Data Encodings](https://tools.ietf.org/html/rfc3548) - [IETF](https://ja.wikipedia.org/wiki/IETF "wikilink")による規格書（英語）。RFC 3548。
      - [ベース64とベース32とベース16コード化](http://www5d.biglobe.ne.jp/~stssk/rfc/rfc3548j.html) - 上記の参考和訳。
  - [The Base16, Base32, and Base64 Data Encodings](https://tools.ietf.org/html/rfc4648) - [IETF](https://ja.wikipedia.org/wiki/IETF "wikilink")による規格書（英語）。RFC 4648。
      - [ベース64とベース32とベース16コード化](http://www5d.biglobe.ne.jp/~stssk/rfc/rfc4648j.html) - 上記の参考和訳。

[Category:電子メールのプロトコル](https://ja.wikipedia.org/wiki/Category:電子メールのプロトコル "wikilink") [Category:ネットニュース](https://ja.wikipedia.org/wiki/Category:ネットニュース "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:データシリアライゼーションフォーマット](https://ja.wikipedia.org/wiki/Category:データシリアライゼーションフォーマット "wikilink")

1.  元データを6ビット区切りにし、6ビットのそれぞれを印字可能な64文字の内の1文字に置き換える。その1文字1文字は8ビットなので、元の6ビットを8ビットで表現するわけである。なのでデータ量は8/6つまり4/3となる。
2.  Base64エンコード後の1文字は、元のデータの6ビットを表現しているので、Base64エンコード後が76文字ということは、元のデータは、76 × 6ビット = 456ビット = 57バイトである。57バイトを76 + 2 = 78バイトで表現しているので、データ量は78 ÷ 57 ≒ 1.37 = 137%となる。