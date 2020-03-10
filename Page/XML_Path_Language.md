> この記事は[XML Path Language](https://ja.wikipedia.org/wiki/XML_Path_Language)から翻訳されています。


[300px文書に](https://ja.wikipedia.org/wiki/画像:XPath_example.svg "wikilink") XPath の式を適用したイメージ\]\] [thumb](https://ja.wikipedia.org/wiki/画像:XML_languages.svg "wikilink") **XML Path Language** （**XPath**（エックスパス）） は、[マークアップ言語](../Page/マークアップ言語.md "wikilink") [XML](../Page/Extensible_Markup_Language.md "wikilink") に準拠した文書の特定の部分を指定する言語構文である。XPath自体は簡潔な構文 （式言語） であり、（XML関係にありがちな\[1\]）XMLベースのマークアップ言語ではない。[標準化団体](https://ja.wikipedia.org/wiki/標準化団体_\(コンピュータと通信\) "wikilink") [W3C](../Page/World_Wide_Web_Consortium.md "wikilink") (World Wide Web Consortium) で開発され、1999年11月16日に XML Path Language (XPath) 1.0 が [XSL Transformations](../Page/XSL_Transformations.md "wikilink") (XSLT) 1.0 と同時に勧告として公表された\[2\]\[3\]。XPathは、XSLT と XSL-FO とともに [XSL](../Page/Extensible_Stylesheet_Language.md "wikilink") の構成要素である。2007年1月23日、W3C で XPath 1.0 の次期バージョンが制定され、[XPath 2.0](https://ja.wikipedia.org/wiki/#XPath_2.0 "wikilink") が XSLT 2.0 と同時に勧告された。2014年4月8日に XPath 3.0、2017年3月21日に XPath 3.1 が勧告された。他に、XPathを拡張したようなものとして [XQuery](../Page/XQuery.md "wikilink") がある。

XPathは、XML文書中から必要な要素群（サブセット）を取り出す、などといった用途に使うものとして、急速に受け入れられていった。なお、もともとはXPathは、[XSL](../Page/Extensible_Stylesheet_Language.md "wikilink") ([XSLT](../Page/XSL_Transformations.md "wikilink")) と [XPointer](https://ja.wikipedia.org/wiki/XPointer "wikilink") に共通する構文と振る舞いのモデルを目標としていた。

XSLTでは、XML文書内の処理対象などの指定に、XPathを使用する。一般に、XSLT処理系を[実装](https://ja.wikipedia.org/wiki/実装 "wikilink")するには、XPath処理系のライブラリなどを利用してXPathを取り扱う必要がある。

日本では[日本工業規格](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink")（JIS）に、JIS X 4160 として XPath 1.0 の翻訳版がある。

## データモデル

XPathの[データモデル](https://ja.wikipedia.org/wiki/データモデル "wikilink")では、[XML文書はルートノードを頂点とするノードの](../Page/Extensible_Markup_Language.md "wikilink")[木構造であり](../Page/木構造_\(データ構造\).md "wikilink")、以下の7種類のノードから構成される （参考: [XML](../Page/Extensible_Markup_Language.md "wikilink")） 。

  - ルートノード
  - 要素ノード
  - テキストノード
  - 属性ノード
  - 名前空間ノード
  - 処理命令ノード
  - コメントノード

## ロケーションパス

XPathで最も一般的な式は、ロケーションパスである。ロケーションパスにより、[XML文書のあるノード](../Page/Extensible_Markup_Language.md "wikilink")（現在のコンテクストノード）を基準として、別のノードもしくは複数のノード（ノード集合）が指定される（指定されるノードが0個すなわち1個も存在しない場合もある）。

ロケーションパスは、1つまたは複数のロケーションステップの並びとして記述される。複数のロケーションステップでロケーションパスが記述される場合、各ロケーションステップは`/`により区切られる。

### ロケーションステップ

ロケーションパスを構成する各ロケーションステップは、次の3つの要素から構成される。

  - [軸](https://ja.wikipedia.org/wiki/#軸 "wikilink") ()
  - [ノードテスト](https://ja.wikipedia.org/wiki/#ノードテスト "wikilink")()
  - [述語](https://ja.wikipedia.org/wiki/#述語 "wikilink") ()

ロケーションステップは次の2種類の構文を使って記述することができる。

  - [省略構文](https://ja.wikipedia.org/wiki/#省略構文 "wikilink")
    簡潔でXPathの式を読みやすく書きやすく記述することができる。直観的で多くの場合親しみやすい文字列と構文で記述する。
  - [完全な構文](https://ja.wikipedia.org/wiki/#完全な構文 "wikilink")
    省略構文と比べて記述が冗長ではあるが、省略構文より多くのオプションを指定することができ、またXPath式を注意深く読む際には省略構文より説明的に記述していることがXPath式の正確な理解に役立つ。

### 省略構文

省略構文は簡潔な構文であり、よく使われる多くの既定値を使い省略してロケーションステップを記述することができる。

省略構文による簡単なロケーションパスの記述例を示す。

  -
    `/A/B/C`

この例では、先頭が`/`となっている絶対パスであり、0個以上の`C`要素を選択する。 選択された`C`要素は`B`要素の子要素()であり、その`B`要素は`A`要素の子要素であり、`A`要素はそのXML文書のルート要素である。

XPathの構文は、[URI](../Page/Uniform_Resource_Identifier.md "wikilink")()の構文や[ファイルパスの構文に似せて](../Page/ファイル_\(コンピュータ\).md "wikilink")、設計されている。

省略構文では、先の例より複雑な式を記述することもできる。ただし完全な構文と比べると記述能力は制限される。

  - 既定の`child`軸以外にもいくつかの[軸](https://ja.wikipedia.org/wiki/#軸 "wikilink")（`attribute`軸、`descendant-or-self`軸、`self`軸、`parent`軸）を指定することができる。
  - 簡明なノード名による指定以外の[ノードテストを指定することができる](https://ja.wikipedia.org/wiki/#ノードテスト "wikilink")。
  - どのロケーションステップにも角括弧`[`と`]`を後ろにつけて[述語を指定することができる](https://ja.wikipedia.org/wiki/#述語 "wikilink")。

少し複雑なロケーションパスの例を示す。

  -
    `A//B/*[1]`

この例は、先頭が`/`となっていない相対パスであり、任意の名前の(`*`)最初の要素(`[1]`)を選択する。 選択された「最初の要素」は`B`要素の子要素(`/`)であり、その`B`要素は`A`要素の直接的または間接的な子要素（子孫要素、`//`）であり、その`A`要素は現在のコンテクストノードの子要素である。

省略構文の一覧と正式な定義については後の[\#完全な構文と省略構文の対応関係](https://ja.wikipedia.org/wiki/#完全な構文と省略構文の対応関係 "wikilink")の節で示す。

### 完全な構文

完全な構文の一般式は以下の形となる。

  -
    `/軸方向::名前空間:ノードテスト[述語]/～～`

先の[\#省略構文](https://ja.wikipedia.org/wiki/#省略構文 "wikilink")の節で示した2つの例を、省略しない完全な構文によって書き直すと次のようになる。

  -
    `/child::A/child::B/child::C`
    `child::A/descendant-or-self::node()/child::B/child::*[1]`

このように完全な構文で記述されたロケーションパスの各ロケーションステップにおいては、

  - [軸を](https://ja.wikipedia.org/wiki/#軸 "wikilink")`child`や`descendant-or-self`のように明示的に指定する。
  - 軸の指定に続けて`::`を記述し、さらに[ノードテストを](https://ja.wikipedia.org/wiki/#ノードテスト "wikilink")`A`や`node()`、`*`のように記述する。
  - 省略構文と同様に、ノードテストの指定に続けて角括弧`[`と`]`を後ろにつけて[述語を指定することができる](https://ja.wikipedia.org/wiki/#述語 "wikilink")。

### 軸

[ロケーションステップの軸の記述は](https://ja.wikipedia.org/wiki/#ロケーションステップ "wikilink")、XML文書の[木構造において](../Page/木構造_\(データ構造\).md "wikilink")、方向を指定する。XPath仕様で定義されている13種類の軸（[\#完全な構文](https://ja.wikipedia.org/wiki/#完全な構文 "wikilink")）を示す。

  - `child`
    コンテクストノードの子ノード
  - `descendant`
    コンテクストノードの子孫ノード
  - `parent`
    コンテクストノードの親ノード
  - `ancestor`
    コンテクストノードの祖先ノード
  - `following-sibling`
    コンテクストノードの兄弟ノードのうち後方のノード
  - `preceding-sibling`
    コンテクストノードの兄弟ノードのうち前方のノード
  - `following`
    XML文書の文書順でコンテクストノードより後方にある全てのノード
  - `preceding`
    XML文書の文書順でコンテクストノードより前方にある全てのノード
  - `attribute`
    コンテクストノードが要素の場合、その属性ノード
  - `namespace`
    コンテクストノードが要素の場合、その名前空間ノード
  - `self`
    コンテクストノード自身
  - `descendant-or-self`
    コンテクストノード自身とコンテクストノードの子孫ノード
  - `ancestor-or-self`
    コンテクストノード自身とコンテクストノードの祖先ノード

[省略構文で](https://ja.wikipedia.org/wiki/#省略構文 "wikilink")`attribute`軸を使う例を示す。

  -
    `//a/@href`

この例では、`href`属性ノードの集合を選択する。 選択された `href`属性ノードは、XML文書内のいずれかの`a`要素ノードに属している。

`self`軸は、後述する[述語の中でその述語の直前のノードテストで選択されたノードを記述するためによく使われる](https://ja.wikipedia.org/wiki/#述語 "wikilink")。 例を示す。

  -
    `h3[.='関連項目']`

この例では、カレントノードの子ノードであり、かつ内容のテキスト`'関連項目'`をもつ`h3`要素が選択される。

### ノードテスト

[ロケーションステップのノードテストは](https://ja.wikipedia.org/wiki/#ロケーションステップ "wikilink")、式もしくは特定のノード名によって記述される。 例えば、名前空間接頭辞`gs`が定義されているXML文書で、`//gs:enquiry`とノードテストが記述された場合、`gs`名前空間下の`enquiry`をノード名とする全てのノードの集合が、このノードテストの指定の対象となる。

ノードテストの書式を示す\[4\]。

  - 名前
    「名前空間接頭辞:名前」という書式でもよく、`attribute`軸と`namespace`軸以外の軸の場合は、その名前をもつ全ての要素ノードを指定する。`attribute軸`の場合はその名前の全ての属性ノードを指定し、`namespace軸`の場合は名前空間ノードを指定する。
  - `text()`
    全てのテキスト（文字列）ノードを指定する。例: <k>`こんにちは`</k>の中の`'こんにちは'`
  - `comment()`
    全てのXMLコメントノードを指定する。例: `<!-- コメント -->`
  - `processing-instruction()`
    全てのXML処理命令ノードを指定する。例: <code>
    <?xsl-stylesheet href="article.css" ?>
    </code>
    `processing-instruction(処理命令ターゲット)`という書式での記述も可能であり、この例の場合は`processing-instruction('xsl-stylesheet')`と記述すると指定対象となる。
  - `node()`
    全てのノードを指定する。
  - `*`
    主ノード型の全てのノードを指定する。ここで主ノード型とは、`attribute`軸と`namespace`軸以外の軸の場合は要素ノードを意味し、`attribute`軸の場合は属性ノードを、`namespace`軸の場合は名前空間ノードを、それぞれ意味する。
  - 名前空間接頭辞:\*
    名前空間接頭辞が示す名前空間に属する全ての主ノード型のノードを指定する。

### 完全な構文と省略構文の対応関係

[ロケーションステップの](https://ja.wikipedia.org/wiki/#ロケーションステップ "wikilink")[完全な構文と](https://ja.wikipedia.org/wiki/#完全な構文 "wikilink")[省略構文の対応関係を次に示す](https://ja.wikipedia.org/wiki/#省略構文 "wikilink")\[5\]\[6\]。

| 完全な構文                          | 省略構文         | 説明                          |
| ------------------------------ | ------------ | --------------------------- |
| `child::`                      | （省略して何も書かない） | コンテクストノードの子ノード              |
| `attribute::`                  | `@`          | コンテクストノードが要素の場合、その属性ノード     |
| `/descendant-or-self::node()/` | `//`         | コンテクストノード自身とコンテクストノードの子孫ノード |
| `self::node()`                 | `.`          | コンテクストノード自身                 |
| `parent::node()`               | `..`         | コンテクストノードの親ノード              |

### 述語

[ロケーションステップでは](https://ja.wikipedia.org/wiki/#ロケーションステップ "wikilink")、[ノードテストの後に](https://ja.wikipedia.org/wiki/#ノードテスト "wikilink")、角括弧でくくる述語で複雑な式を記述して、ノードテストで指定されたノード集合を絞り込むことができる。 ノード集合を絞り込む必要が無い場合は、述語は記述しない。

簡単な例を示す。

  -
    `//a[@href='help.php']`

この例では、`[@href='help.php']`の部分が述語である。 このXPath式は、`href`属性をもち、かつその属性値が`'help.php'`である、全ての`a`要素ノードを指定する。

先の例では述語の数は1つであったが、ロケーションパスを構成するロケーションステップごとに、複数の述語を指定することができる。 すなわち、絞り込み条件を複数重ねて指定することができる。 指定できる述語の数に制限は無い。

述語は、その述語を含むロケーションステップのコンテクストを変更することは無い。 その直前のノードテストで指定されたノード集合がそのロケーションステップのコンテクストであり、述語が指定されることでコンテクストが変更されることは無い。

複雑な例を示す。

  -
    `//a[@href='help.php'][name(..)='div'][../@class='header']/@target`

この例は、`a`要素の`target`属性の値を指定する。 ただし、このXPath式の最初のロケーションステップには3つの述語が記述されており、`a`要素のうち

  - `a`要素の`href`属性の値が`'help.php'`であり、
  - また、`a`要素の親要素の要素名が`div`であり、
  - また、親要素(`div`)の`class`属性の値が`'header'`である、

`a`要素のみが、最初のロケーションステップの指定対象となる。 最終的には、最初のロケーションステップで絞り込まれて指定対象となった`a`要素の`target`属性が指定されることになる。

## データ型と演算子、関数

XPath 1.0 で規定されている[データ型](https://ja.wikipedia.org/wiki/データ型 "wikilink")と[演算子](../Page/演算子.md "wikilink")、[関数を説明する](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")。

データ型は次の4種類が定義されている。

  - ノード集合 （node-set; 順序づけられていないノードの集合）
  - 文字列 (string)
  - 数値 （number; [浮動小数点数](../Page/浮動小数点数.md "wikilink")）
  - 論理型 (boolean)

### 演算子

| 演算子   | 備考                                                |
| ----- | ------------------------------------------------- |
| `/`   | 先述。                                               |
| `//`  | 先述。                                               |
| `\|`  | 2つのノード集合の和集合のノード集合を返す。                            |
| `and` | 論理積                                               |
| `or`  | 論理和                                               |
| `+`   | 足し算                                               |
| `-`   | 引き算                                               |
| `*`   | 掛け算                                               |
| `div` | [IEEE 754に基づく割り算](../Page/IEEE_754.md "wikilink") |
| `mod` | 剰余                                                |
| `=`   | 等価                                                |
| `!=`  | 等価でない                                             |
| `<`   | 小なり                                               |
| `<=`  | 小なりまたは等価                                          |
| `>=`  | 大なりまたは等価                                          |
| `>`   | 大なり                                               |

### 関数

#### 文字列を扱う関数

| 関数名                | 備考                                           |
| ------------------ | -------------------------------------------- |
| `concat`           | 与えられた文字列を連結した文字列を返す。                         |
| `substring`        | 指定された範囲の部分文字列を返す。                            |
| `contains`         | 指定された文字列が部分文字列として含まれる場合に真値を返し、それ以外の場合に偽値を返す。 |
| `starts-with`      | 指定された文字列が先頭の部分文字列である場合に真値を返し、それ以外の場合に偽値を返す。  |
| `ends-with`        | 指定された文字列が末尾の部分文字列である場合に真値を返し、それ以外の場合に偽値を返す。  |
| `substring-before` | 指定された文字列よりも前にある部分文字列を返す。                     |
| `substring-after`  | 指定された文字列よりも後ろにある部分文字列を返す。                    |
| `translate`        |                                              |
| `normalize-space`  |                                              |
| `string-length`    | 文字列の長さを返す。                                   |

#### 数値を扱う関数

| 関数名       | 備考     |
| --------- | ------ |
| `sum`     | 総和を返す  |
| `round`   | 四捨五入関数 |
| `floor`   | 床関数    |
| `ceiling` | 天井関数   |

#### ノードの情報を扱う関数

| 関数名             | 備考             |
| --------------- | -------------- |
| `name`          | 名前空間付きの要素名を返す。 |
| `local-name`    | 名前空間なしの要素名を返す。 |
| `namespace-uri` | 名前空間のURIを返す。   |
| `position`      |                |
| `last`          |                |

#### データ型を変換する関数

| 関数名       | 備考 |
| --------- | -- |
| `string`  |    |
| `number`  |    |
| `boolean` |    |

比較的よく使われる関数については、次の節以降で少し詳しく述べる。 完全な定義は、[W3Cの勧告](http://www.w3.org/TR/xpath)[(日本語訳)](http://www.infoteria.com/jp/contents/xml-data/REC-xpath-19991116-jpn.htm)を参照。

XPathの式は、丸括弧の`(`と`)`で括りグループ化して評価順序を明記することができる。

[述語には演算子を使った式を含めることができる](https://ja.wikipedia.org/wiki/#述語 "wikilink")。論理式 (論理値を返す式) は、 `and` 演算子や `or` 演算子でつなげることや、`not`関数の引数にすることができる。 文字列 (string) には[Unicode](../Page/Unicode.md "wikilink")の文字を含めることができる。 述語で演算子を使う例を示す。

  - `//item[@price >= 2*@discount]`

この例では、`price` 属性の数値が `discount` 属性の数値の2倍以上である `item` 要素の集合を選択する。

演算子`|`は、述語の内部でも、述語の外部でも、ノード集合の和を求めるために使うことができる。述語の外部で`|`演算子を使う例を示す。

  - `v[x or y] | w[z]`

この例では、一つのノード集合を返す。返されるノード集合は、処理中のコンテクストにおいて、子要素として `x` 要素もしくは `y` 要素をもつ `v` 要素の集合と、子要素として `z` 要素をもつ `w` 要素の集合の、和集合である。

### ノード集合関数

  - *number* `position()`
    評価中のコンテクストノードの位置を数値で返す （兄弟ノードにおける位置） 。
  - *number* `count(`*node-set*`)`
    引数のノード集合 （もしくはノード集合を返す式） のノードの数を返す。
  - *node-set* `id(`*object*`)`
    引数のオブジェクトの文字列値をID型の属性値としてもつノードの集合を返す。
  - *string* `name(`*node-set?*`)`
    引数として渡されたノード集合の最初のノードの名前を返す （ノードが要素の場合は要素名、属性の場合は属性名） 。

### 文字列関数

  - *string* `string(`*object?*`)`
    XPathで規定されている4種類の[データ型](https://ja.wikipedia.org/wiki/データ型 "wikilink")を引数としてとることができ、仕様で定められた変換規則によって文字列に変換する。引数としてXPath式も渡すことができる。
  - *number* `string-length(`*string?*`)`
    引数として渡す文字列の長さ （文字の数） を返す。
  - *string* `substring(`*string*`,`*number*`,`*number?*`)`
    引数として渡す文字列の部分文字列を返す。
  - *string* `concat(`*string*`,`*string*`,`*string\**`)`
    引数として渡す複数の文字列を連結して返す。
  - *boolean* `contains(`*string1*`,`*string2*`)`
    引数の文字列 *`string1`* に文字列 *`string2`* が含まれていた場合には`true`関数が返すのと同じ値を返す。含まれていなかった場合は`false`関数が返すのと同じ値を返す。
  - *string* `normalize-space(`*string?*`)`
    引数の文字列を正規化して返す。すなわち、文字列の前後の空白文字を除去し、さらに除去後の文字列中に連続して現れる空白文字を一つの空白で置き換えた文字列を、返す。

### 論理関数

  - *boolean* `not(`*boolean*`)`
    引数の論理値の逆の値を返す。

### 数値関数

  - *number* `sum(`*node-set*`)`
    引数として渡されたノード集合の各ノードの文字列値を、仕様で定められた変換規則にしたがって数値に変換し、合計した値を返す。

## 例

次のXML文書でXPathを例示して説明する。

``` xml
<?xml version="1.0" encoding="utf-8"?>
<document>
    <!-- XML文書 -->
    <chapter title="第1章">
        <paragraph>段落</paragraph>
        <paragraph>次の段落</paragraph>
        <paragraph>さらに次の段落</paragraph>
        <paragraph>最後の段落</paragraph>
    </chapter>
    <chapter title="第2章">
        <paragraph>段落</paragraph>
    </chapter>
</document>
```

  - `/document` : ルート要素 `document` を選択する。
  - `/*` : 名前を限定せずにルート要素を選択する。この場合は同じく `document` が選択される（XML文書は必ず一つのルート要素をもつ）
  - `/document/chapter` : `document` 要素の子要素である全ての `chapter` 要素を選択する。
  - `/document/chapter[1]` : `document` 要素の子要素のうち1番目の `chapter` 要素を選択する。
  - `//paragraph` : 文書内の全ての `paragraph` 要素を選択する。
  - `//chapter[@title="第1章"]/paragraph` : `title` 属性の値が "第1章" である `chapter` 要素の子要素である全ての `paragraph` 要素を選択する。

## XPath 2.0

XPath 2.0 は2007年1月23日に[標準化団体](https://ja.wikipedia.org/wiki/標準化団体_\(コンピュータと通信\) "wikilink") [W3C](../Page/World_Wide_Web_Consortium.md "wikilink") で勧告された。 [XQuery](../Page/XQuery.md "wikilink") 1.0 は XPath 2.0 の拡張である。 また XPath 2.0 は [XSLT](../Page/XSL_Transformations.md "wikilink") 2.0 でも採用されている。

XPath 2.0 仕様は、1.0 と比べて大規模になっており非常に多くの機能が規定されている。 そのうち特に重要な変更は、多様な[データ型](https://ja.wikipedia.org/wiki/データ型 "wikilink")を扱えるようになったことである。 XPath 2.0 では、[スキーマ言語](https://ja.wikipedia.org/wiki/スキーマ言語 "wikilink") [XML Schema](https://ja.wikipedia.org/wiki/XML_Schema "wikilink") で規定されている組み込みのアトミックデータ型と、スキーマで定義されたユーザ定義型を、扱うことができる。 あらゆる値は、シーケンスとして扱われる。 一つの文字列値やノードは、シーケンスに含まれる要素の一つと位置づけられる。 XPath 1.0 のノード集合は、XPath 2.0 では何らかの順序をもつシーケンスに、置き換わる。 多様な型を扱うために、XPath 2.0 では[関数と](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")[演算子](../Page/演算子.md "wikilink")が大幅に拡張される。

XPath 2.0 は XQuery 1.0 のサブセットとなっている。 XPath 2.0 は XQuery 1.0 の構文のパス式を構成する。 XQuery 1.0 の FLWOR と呼ばれる式においては、`for` 句の構成要素となる。

## XPath 3.0

2014年4月8日に XPath 3.0 が勧告された。[XQuery](../Page/XQuery.md "wikilink") 3.0 は XPath 3.0 の拡張である。

## 実装

### Java

`javax.xml.xpath`\[7\] パッケージがあり、XPath 1.0 が実装されている。`XPathFactory.newInstance().newXPath()` にて、XPath のインスタンスを作ることができ、`XPath.evaluate()` にて XPath を評価できる。

### JavaScript

HTML ではなく、一般の XML に関しては、[XMLHttpRequest](https://ja.wikipedia.org/wiki/XMLHttpRequest "wikilink") を使うと DOM木を作ることができ、どちらに対しても XPath が使える。[Internet Explorer](../Page/Internet_Explorer.md "wikilink") の場合は、`XMLDomNode.selectNodes()`\[8\] にて XPath が使える。Internet Explorer 以外のブラウザでは、DOM Level 3 XPath の仕様通り、`XPathEvaluator.evaluate()`\[9\] にて、XPath が扱える。

現在では、ブラウザ標準で XPath が使えるが、2007年くらいまでは、JavaScript で実装した XPath が作られていて、 JavaScript-XPath\[10\]やGoogle AJAXSLT\[11\]などが XPath を実装している。

### XSLT処理系

XSLTでもノードの指定に XPath を用いる。XSLT処理系には以下のようなものがある。

  - ウェブブラウザ: や  などのウェブブラウザでは、`xml-stylesheet`処理命令が中に書かれたXML文書を表示する場合、そのXML文書を指定されたXSLプログラムで処理して得られるXML文書を画面に表示する。
    xsltproc: に搭載された XSLT 処理系である。

## 関連項目

  - [XML](../Page/Extensible_Markup_Language.md "wikilink")
  - [XSL](../Page/Extensible_Stylesheet_Language.md "wikilink")
      - [XSLT](../Page/XSL_Transformations.md "wikilink") (XSL Transformations)

<!-- end list -->

  - [XQuery](../Page/XQuery.md "wikilink")

<!-- end list -->

  - [XML Schema](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")

## 脚注

## 参考文献

  - 株式会社日本ユニテック、中山幹敏、奥井康弘 ほか『改訂版 標準XML完全解説（下）』技術評論社、2001年、ISBN 4-7741-1302-6
  - [XPath 1.0 仕様（英語）](http://www.w3.org/TR/xpath) - [W3C](../Page/World_Wide_Web_Consortium.md "wikilink") (World Wide Web Consortium)

## 外部リンク

  - [XML Path Language (XPath) Version 1.0](http://www.w3.org/TR/xpath/) - [W3C勧告](https://ja.wikipedia.org/wiki/W3C勧告 "wikilink")

      - [XPath 1.0 仕様](http://www.doraneko.org/xml/xpath10/19991116/Overview.html) - どら猫本舗（非公式日本語訳）

<!-- end list -->

  - [XML Path Language (XPath) 2.0](http://www.w3.org/TR/xpath20/) - [W3C勧告](https://ja.wikipedia.org/wiki/W3C勧告 "wikilink")

  - [XML Path Language (XPath) 3.0](http://www.w3.org/TR/xpath-30/) - [W3C勧告](https://ja.wikipedia.org/wiki/W3C勧告 "wikilink")

  - [XML Path Language (XPath) 3.1](http://www.w3.org/TR/xpath-31/) - [W3C勧告](https://ja.wikipedia.org/wiki/W3C勧告 "wikilink")

  - [XPathの書き方の基本](http://www.atmarkit.co.jp/fxml/tanpatsu/10xslt/xslt02.html) - ＠IT（アットマーク・アイティ）

  - [XPath tutorial](http://www.w3schools.com/xpath/default.asp)

  - [Another tutorial](http://www.zvon.org/xxl/XPathTutorial/General/examples.html)

  - [Practice XPath queries](http://www.activsoftware.com/xml/xpath/)

[he:XSL\#XPath](https://ja.wikipedia.org/wiki/he:XSL#XPath "wikilink")

[Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:問い合わせ言語](https://ja.wikipedia.org/wiki/Category:問い合わせ言語 "wikilink")

1.  同じ記法のせいで混乱の元になりやすい
2.  [XPath 1.0 仕様 (英語)](http://www.w3.org/TR/xpath) - [W3C](../Page/World_Wide_Web_Consortium.md "wikilink") (World Wide Web Consortium)
3.  W3C の XPath 1.0 作業部会では、[ジェームズ・クラークとスティーヴン](../Page/ジェームズ・クラーク_\(ソフトウェア技術者\).md "wikilink")・ディローズが共同でエディタを務めた。また XSLT 1.0 作業部会では、ジェームズ・クラークがエディタを務めた。
4.  (株)日本ユニテックほか、2001年、p.66
5.
6.  (株)日本ユニテックほか、2001年、p.67
7.  [javax.xml.xpath (Java Platform SE 6)](http://download.oracle.com/javase/6/docs/api/javax/xml/xpath/package-summary.html)
8.  [selectNodes Method](http://msdn.microsoft.com/ja-jp/library/ms754523.aspx)
9.  [evaluate - Document Object Model XPath](http://www.w3.org/TR/DOM-Level-3-XPath/xpath.html#XPathEvaluator-evaluate)
10. [JavaScript-XPath](http://coderepos.org/share/wiki/JavaScript-XPath)
11. [Google AJAXSLT](http://goog-ajaxslt.sourceforge.net/)