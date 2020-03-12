> この記事は[ABNF](https://ja.wikipedia.org/wiki/ABNF)から翻訳されています。


**ABNF**（**Augmented Backus–Naur form**）は、[バッカス・ナウア記法](../Page/バッカス・ナウア記法.md "wikilink") (BNF) の拡張の一種。構文規則や生成規則はBNFとは異なる。[通信プロトコル](../Page/通信プロトコル.md "wikilink")などの言語の形式体系を記述する[メタ言語](https://ja.wikipedia.org/wiki/メタ言語 "wikilink")として開発された。RFC 5234 で文書化されており、[IETF](../Page/Internet_Engineering_Task_Force.md "wikilink") が通信プロトコルを定義する際によく使っている。**拡張バッカス・ナウア記法**とも呼ばれるが、[EBNF](../Page/EBNF.md "wikilink")（Extended Backus-Naur Form）も同じ訳語となるため、区別するためあえて **ABNF** としている。

RFC 5234 は、RFC 4234およびRFC 2234 に存在した問題を修正し置換したものである。

## 概要

ABNFの記述は以下のような生成規則群からなる。

``` abnf
rule = definition ; comment CR LF
```

ここで、rule は大文字小文字が区別される[非終端記号](https://ja.wikipedia.org/wiki/非終端記号 "wikilink")、definition はその rule を定義する記号列、comment は文書化のためのコメントである。最後尾には必ず `CR` と `LF` による[改行コード](../Page/改行コード.md "wikilink")が付属する。

規則名は大文字小文字を区別しない。<rulename> も <RULENAME> も <rUlENamE> も同じ規則を参照している。規則名はいわゆるアルファベット文字で始まり、その後にアルファベット、数字、ハイフンが続く。

山括弧（`<`と`>`）は規則名を囲むのに必要とはされていない。しかし、規則名を識別しやすいように山括弧で囲むことが多い。

ABNF は 7ビットASCIIで符号化され、最上位の8ビット目はゼロに設定される。

## 終端記号の値

[終端記号は](../Page/終端記号と非終端記号.md "wikilink")1つ以上の文字コードで表される。

文字コードは、パーセント記号“`%`”とそれに続く基数を表す文字（b = 2進、d = 10進、x = 16進）、さらに値で示される。文字列は値を “`.`”で連結することで表される。例えば、復帰コードは `%d13` または `%x0D` で示される。復帰コードの後に改行コードが続く場合、連結を使って `%d13.10` などと表される。

リテラルテキストは引用符 (`"`) で囲まれた文字列を使って表される。これら文字列は大文字小文字が区別されず、文字セットとしては US-ASCII が使われる。従って、“abc”という文字列は、“abc”、“Abc”、“aBc”、“abC”、“ABc”、“AbC”、“aBC”、“ABC”とマッチする。大文字小文字を区別したい場合、文字コードを上述の記法で指定するかRFC 7405で導入された“%s”プレフィクスを使用するかする必要がある。“aBc”という大文字小文字の組合せを表したい場合、`%d97 %d66 %d99`あるいは`%s"aBc"` とする。

## オペレータ

### 空白

空白は定義内の各要素を区切るのに使われる。

### 連結

  -
    `Rule1 Rule2`

規則名を並べることで規則が定義される。

“aba”にマッチする文字列を定義するには、次のような規則群を使用する。

1.  `fu = %x61 ; a`
2.  `bar = %x62 ; b`
3.  `mumble = fu bar fu`

### 択一

  -
    `Rule1 / Rule2`

規則名を斜線 (“`/`”) で区切って並べることで選択肢型の規則が定義される。

規則 <fu> か、規則 <bar> のどちらでもよいという規則は次のように記述される。

  -
    `fubar = fu / bar`

### 選択肢追加

  -
    `Rule1 =/ Rule2`

規則名と定義の間に “`=/`” を置くことで規則に選択肢を追加できる。

  -
    `ruleset = alt1 / alt2 / alt3 / alt4 / alt5`

という規則は次の規則群と等価である。

1.  `ruleset = alt1 / alt2`
2.  `ruleset =/ alt3`
3.  `ruleset =/ alt4 / alt5`

### 値の範囲指定

  -
    `%c##-##`

数値範囲はハイフン (“`-`”) で指定される。

  -
    `OCTAL = "0" / "1" / "2" / "3" / "4" / "5" / "6" / "7"`

という規則は、次の規則と等価である。

  -
    `OCTAL = %x30-37`

### グループ化

  -
    `(Rule1 Rule2)`

定義内で複数の要素を括弧でくくることにより、規則のグループ化がなされる。

“elem fubar snafu”または“elem tarfu snafu”にマッチする規則は次のようになる。

  -
    `group = elem (fubar / tarfu) snafu`

“elem fubar”または“tarfu snafu”にマッチする規則は次のどちらでもよい。

  - `group = elem fubar / tarfu snafu`
  - `group = (elem fubar) / (tarfu snafu)`

### 変数の反復

  -
    `n*nRule`

要素の繰り返しには <a>`*`<b>`element` という形式が使われる。<a> の部分はオプションで最小反復回数を示し、省略した場合 0 である。<b> の部分はオプションで最大反復回数を示し、省略した場合無限の反復となる。

`*element` は0回以上の任意回の反復、`1*element` は1回以上の任意回の反復、`2*3element` は2回か3回の反復を表す。

### 特定回数の反復

  -
    `nRule`

反復回数を指定するには <a>`element` という形式を用いる。これは <a>`*`<a>`element` と等価である。

`2DIGIT` は2桁の数、`3DIGIT` は3桁の数を表す。DIGIT は後述する中核規則で定義されている。

### オプション

  -
    `[Rule]`

オプション要素は次のいずれかで示すことができる。

  - `[fubar snafu]`
  - `*1(fubar snafu)`
  - `0*1(fubar snafu)`

### コメント

  -
    `; comment`

コメントはセミコロン (“`;`”) から行末までである。

### オペレータの優先順位

以上のオペレータの優先順位は次の通り（上にあるほど優先される）。

1.  文字列、名前の形成
2.  コメント
3.  値の範囲
4.  反復
5.  グループ化、オプション
6.  連結
7.  択一

択一オペレータを連結と共に使うと解釈が混乱する可能性があるため、グループ化で優先順位を明示することが推奨される。

### 中核規則

ABNF には、以下の中核規則（core rules）が定義されている。

| 規則名    | 形式定義                                      | 意味                      |
| ------ | ----------------------------------------- | ----------------------- |
| ALPHA  | %x41-5A / %x61-7A                         | ASCIIの大文字と小文字 (A-Z a-z) |
| DIGIT  | %x30-39                                   | 十進数字 (0-9)              |
| HEXDIG | DIGIT / "A" / "B" / "C" / "D" / "E" / "F" | 16進数字 (0-9 A-F a-f)     |
| DQUOTE | %x22                                      | 二重引用符                   |
| SP     | %x20                                      | 空白                      |
| HTAB   | %x09                                      | 水平タブ                    |
| WSP    | SP / HTAB                                 | 空白と水平タブ                 |
| LWSP   | \*(WSP / CRLF WSP)                        | 線型空白（改行も含む）             |
| VCHAR  | %x21-7E                                   | 印字される文字                 |
| CHAR   | %x01-7F                                   | NUL 以外の任意の7ビットASCII文字   |
| OCTET  | %x00-FF                                   | 8ビットのデータ                |
| CTL    | %x00-1F / %x7F                            | 制御文字                    |
| CR     | %x0D                                      | 復帰コード                   |
| LF     | %x0A                                      | 改行コード                   |
| CRLF   | CR LF                                     | インターネットの標準改行コード         |
| BIT    | "0" / "1"                                 |                         |
|        |                                           |                         |

## 例

[バッカス・ナウア記法](../Page/バッカス・ナウア記法.md "wikilink") (BNF) のページにもあったアメリカ合衆国での住所表記の例を ABNF で表した例である。

``` abnf
postal-address   = name-part street zip-part

name-part        = *(personal-part SP) last-name [SP suffix] CRLF
name-part        =/ personal-part CRLF

personal-part    = first-name / (initial ".")
first-name       = *ALPHA
initial          = ALPHA
last-name        = *ALPHA
suffix           = ("Jr." / "Sr." / 1*("I" / "V" / "X"))

street           = [apt SP] house-num SP street-name CRLF
apt              = 1*4DIGIT
house-num        = 1*8(DIGIT / ALPHA)
street-name      = 1*VCHAR

zip-part         = town-name "," SP state 1*2SP zip-code CRLF
town-name        = 1*(ALPHA / SP)
state            = 2ALPHA
zip-code         = 5DIGIT ["-" 4DIGIT]
```

## 参考文献

  - RFC 7405 Case-Sensitive String Support in ABNF
  - RFC 5234 Augmented BNF for Syntax Specifications: ABNF
  - RFC 4234 Augmented BNF for Syntax Specifications: ABNF (Obsolete)
  - RFC 2234 Augmented BNF for Syntax Specifications: ABNF (Obsolete)

[Category:形式言語](https://ja.wikipedia.org/wiki/Category:形式言語 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")