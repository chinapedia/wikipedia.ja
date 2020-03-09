> この記事は[Punycode](https://ja.wikipedia.org/wiki/Punycode)から翻訳されています。


（ピュニコード、プニコード）とは、[国際化ドメイン名](../Page/国際化ドメイン名.md "wikilink")で使われる[文字](https://ja.wikipedia.org/wiki/文字 "wikilink")[符号化方式](../Page/符号化方式.md "wikilink")で、RFC 3492 で定義されている。 で書かれた文字列を[DNSで使用可能な](../Page/Domain_Name_System.md "wikilink")、アルファベット（大文字小文字を区別しない）、数字、ハイフンのみの文字列に変換する。

## 概要

ドメイン名として  を使用する際は、ピリオド（`.`）で区切られたドメイン名の階層レベルごとにプレフィックスとして「`xn--`」を使用し、エンコードされた文字列を続ける。大文字と小文字は区別されない。

<table>
<thead>
<tr class="header">
<th><p>可読なドメイン名</p></th>
<th><p>でのドメイン名</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><code>ドメイン名例.jp</code></p></td>
<td><p><code>xn--eckwd4c7cu47r2wf.jp</code></p></td>
</tr>
<tr class="even">
<td><p><code>ウィキペディア.ドメイン名例.jp</code></p></td>
<td><p><code>xn--cckbak0byl6e.xn--eckwd4c7cu47r2wf.jp</code></p></td>
</tr>
<tr class="odd">
<td><p><code>例え.テスト</code></p></td>
<td><p><code>xn--r8jz45g.xn--zckzah</code></p></td>
</tr>
</tbody>
</table>

## エンコーディング手順

この節では  のエンコーディング手順を、「」\[1\]がどのようにして「`bcher-kva`」と変換されるかを例にとって説明する。

### 文字の分離

最初に入力文字列中にあるすべての基本文字（[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")）を残し、基本文字以外の文字は飛ばす。基本文字以外の文字がある場合は、最後に区切り文字（ハイフン）を追加する。

| 入力文字列     | 処理後      |
| --------- | -------- |
| `bücher`  | `bcher-` |
| `日本Japan` | `Japan-` |

### 非文字の挿入をコード番号としてエンコード

次のエンコーディング手順を理解するために、先にデコーダの動作を理解する必要がある。デコーダは2つの状態変数 *i* と *n* を持つ[オートマトンである](https://ja.wikipedia.org/wiki/有限オートマトン "wikilink")。 *i* は分離した後のASCII文字列への挿入位置を表し、その範囲は0 (文字列の先頭への挿入を表す) からASCII文字列の長さ (文字列の末尾への挿入を表す) である。従ってこの例では0 - 5となる。*n*は挿入する文字のコードポイントである。

*i* は0から始まり、*n* は128 (非ASCII文字の最初のコードポイント) から始まる。状態遷移は[単調であり](https://ja.wikipedia.org/wiki/単調関数 "wikilink")、遷移すると *i* が1だけ増加する。ただし *i* がすでに最大値の場合は *n* を1増加し、*i* は0に戻る。つまり挿入するべき箇所がなくなると、挿入すべき文字が1つ後の物となる。

デコーダが文字を挿入する前に、スキップすべき挿入可能位置がいくつあるかを数値化したものがエンコーダによって生成されるコード番号である。"ü"のUnicodeコードポイントはU+00FC, 10進数で表すと252である。よって ü の字を文字列の1文字目の後ろに挿入するには、"bcher"の中に6か所ある挿入ポイントに、üより前にある124 (251 - 127 = 124) 種類の非ASCII文字が挿入されるのをスキップし、さらに0文字目 (つまり文字列の先頭) にüが挿入されるのをスキップする必要がある。したがって、デコーダには必要な1文字を挿入するために、(124 × 6) + 1 = 745回の非ASCII文字挿入をスキップするよう、デコーダに伝える必要がある。

### コード番号をASCII文字列として再変換

Punycodeはこのコード番号を表すために[リトルエンディアンの一般化可変長整数を使用する](https://ja.wikipedia.org/wiki/エンディアン "wikilink")。例としてコード番号745を「kva」と表す方法を示す。

一般化可変長整数では、各々の桁に異なる[閾値](https://ja.wikipedia.org/wiki/閾値 "wikilink")を設け、これより小さい数字の表れる桁を最大桁とすることで数字列の区切りを決める。Punycodeで用いられるリトルエンディアンの場合、小さい桁から表記されるため、先読みなしで任意の桁数の数字を表記できる。

Punycodeの場合は各桁に使える数字として36種の文字を使用する。アルファベット（大文字小文字を区別しない）の'a'から'z'が0から25を表し、数字の'0'から'9'が26から35を表す (このため後述する式に出てくる底baseは36となる)。

| 10進数 | 0 | 1 | 2 | 3 | … | 24 | 25 | 26 | … | 34 | 35 |
| ---- | - | - | - | - | - | -- | -- | -- | - | -- | -- |
| 36値化 | a | b | c | d | … | y  | z  | 0  | … | 8  | 9  |

したがって「kva」は「10 21 0」を表す。ここで閾値は (1 1 26) であるとする。最初の桁 (**k**つまり**10**) の重みは1である。1桁目は1 - 35までの範囲の値をとるため、2桁目の重みは35となる。2桁目 (**v**) は同様に1 - 35の範囲の値をとるため、3桁目 (**a**つまり**0**) の重みは35 × 35 = 1225である。また、3桁目の値**0**は3桁目の閾値**26**よりも小さいため、ここで1つ目の数字列は終了であることがわかる。したがって「kva」は10 × 1 + 21 × 35 + 0 × 1225 = 745を表していることがわかる。

各桁の重みw(j)および閾値t(j)の値は以下の式で計算される。

\[w(0) = 1\]

\[w(j) = w(j-1) \times ( base - t(j-1) )\]

\[t(j) = base \times ( j + 1 ) - bias\] (ただしt(j)はt_min以下ならt_min、t_max以上ならt_max)

2つ目の文字を挿入する際にはさらにエンコードされたコード番号を繋げていけばよいが、挿入の度にbiasの値が調節され、各桁の閾値と重みが変わることに注意する必要がある。biasの値が変わらない範囲であれば単純に追加するだけでよい。例えば"bücher"に2つ目の特殊文字を挿入しようとすると、前述のとおりデコーダは前に戻れないため、最初の挿入可能位置は"büücher"で、コード"bcher-kvaa"となる。次の挿入可能位置は"bücüher"で"bcher-kvab"となる。同様に続き"bücherü"は"bcher-kvae"となり、次に来るのは"ýbücher"で"bcher-kvaf"である。

## 脚注

<references />

## 関連項目

  - [国際化ドメイン名](../Page/国際化ドメイン名.md "wikilink")

  -
## 外部サイト

  - RFC 3492
  - [Online Punycode/IDN Decoder/Encoder](https://www.motobit.com/util/punycode-decoder-encoder.asp)
  - [IDN Library—Libidn](https://www.gnu.org/software/libidn/GNU)
  - [ICU IDNA Demonstration](http://demo.icu-project.org/icu-bin/idnbrowser) An online demonstration of how [ICU](https://ja.wikipedia.org/wiki/International_Components_for_Unicode "wikilink") performs IDN operations
  - [Punycode for Domains](http://punycode.bluerider.com/idn/) Convert Unicode to Punycode
  - [List of TLDs considered by the Mozilla developers to have an effective anti-spoofing policy for name registration](https://www.mozilla.org/en-US/about/governance/policies/security-group/tld-idn/)
  - [日本語JPドメイン名のPunycode変換・逆変換 - 日本語.jp](https://punycode.jp/)
  - [Punycoder - the Punycode converter (IDN converter) 🔧](https://www.punycoder.com/)

[Category:Unicode](https://ja.wikipedia.org/wiki/Category:Unicode "wikilink") [Category:国際化ドメイン名](https://ja.wikipedia.org/wiki/Category:国際化ドメイン名 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  [ドイツ語](../Page/ドイツ語.md "wikilink")で「書籍」（複数形）を意味する。