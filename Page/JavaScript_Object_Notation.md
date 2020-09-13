> この記事は[JavaScript Object Notation](https://ja.wikipedia.org/wiki/JavaScript_Object_Notation)から翻訳されています。


**JavaScript Object Notation**（**JSON**、ジェイソン）は[データ記述言語](../Page/データ記述言語.md "wikilink")の1つである。軽量なテキストベースのデータ交換用フォーマットであり[プログラミング言語](../Page/プログラミング言語.md "wikilink")を問わず利用できる\[1\]。名称と構文は[JavaScript](../Page/JavaScript.md "wikilink")におけるオブジェクトの表記法に由来する。

## 特徴

JSONは[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")などでよく使われているECMA-262, revision 3準拠のJavaScript\[2\] ([ECMAScript](../Page/ECMAScript.md "wikilink")) をベースとしている。[2006年](../Page/2006年.md "wikilink")[7月](https://ja.wikipedia.org/wiki/7月 "wikilink")にRFC 4627で仕様が規定され、その後、何度か改定され、[2017年](../Page/2017年.md "wikilink")[12月14日](../Page/12月14日.md "wikilink")\[3\]にIETF STD 90およびRFC 8259およびECMA-404 2nd editionが発表された。[MIMEタイプは](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink") `application/json`、[拡張子](../Page/拡張子.md "wikilink")はjsonとされた。

IETFおよびECMAの仕様の改定の歴史

  - [2006年](../Page/2006年.md "wikilink")[7月](https://ja.wikipedia.org/wiki/7月 "wikilink") - RFC 4627
  - [2013年](../Page/2013年.md "wikilink")[3月](https://ja.wikipedia.org/wiki/3月 "wikilink") - RFC 7158
  - [2013年](../Page/2013年.md "wikilink")[10月](https://ja.wikipedia.org/wiki/10月 "wikilink") - [ECMA-404 1st edition](http://www.ecma-international.org/publications/standards/Ecma-404-arch.htm)
  - [2014年](../Page/2014年.md "wikilink")[3月](https://ja.wikipedia.org/wiki/3月 "wikilink") - RFC 7159
  - [2017年](../Page/2017年.md "wikilink")[12月14日](../Page/12月14日.md "wikilink")\[4\] - RFC 8259および[IETF STD 90](https://tools.ietf.org/html/std90)および[ECMA-404 2nd edition](http://www.ecma-international.org/publications/standards/Ecma-404.htm)

JSONはJavaScriptにおけるオブジェクト表記法のサブセットであるが、JavaScriptでの利用に限られたものではない。

JSONは単純であるので、特に[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")の分野で利用が広がりつつある。JavaScriptでJSONをパースして読み込むには、文字列をJavaScriptのコードとして解釈させる [`eval`](https://ja.wikipedia.org/wiki/eval "wikilink") 関数を作用させるだけでよい（ただし、セキュリティ上の問題があるうえ、U+2028 LINE SEPARATOR と U+2029 PARAGRAPH SEPARATOR の扱いがJavaScriptと互換性が無いため、JSON専用のパース関数の `JSON.parse()` を利用するべきである）。このように、広く普及しているウェブブラウザ搭載言語であるJavaScriptで簡単に読み込めるため、Ajaxの開発者達から注目を浴びることになった。

JavaScript言語以外でも、ほとんどの言語においてJSONは単純な処理で書き出しや読み込みができる。そのため、JSONは異なる[プログラミング言語](../Page/プログラミング言語.md "wikilink")の間でのデータの受渡しには能率的である。[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")の場合において、ウェブ[クライアントでのJavaScriptとのデータの受渡しなどはその最たる活用例と言える](../Page/クライアント_\(コンピュータ\).md "wikilink")。[プロセス間通信](../Page/プロセス間通信.md "wikilink")、マシン間通信においても、[疎結合にするため](../Page/結合度.md "wikilink")、JSONで情報を受け渡しすることもある。

### JSONの発見

はJavaScriptのプログラマで、JSONを広めた一人だが、「The JSON Saga」と題したプレゼンテーション\[5\]中で「自分はJSONと名付けたが、考案者ではなく、それ自体は“自然に”存在していたもので、早い例としては1996年には[Netscape Navigatorでデータ交換用に使われていた](../Page/Netscape_Navigator_\(ネットスケープコミュニケーションズ\).md "wikilink")。だから“発見した”ということになるのだが、発見したのも自分が最初ではない」といったように述べている。以上のことを縮めて「JavaScriptのオブジェクト表記法からJSONが発見された。」と表現されている場合がある。

## 表記方法

JSONで表現する[データ型](../Page/データ型.md "wikilink")は以下の通りで、これらを組み合わせてデータを記述する\[6\]。`true`, `false`, `null` などは全て小文字でなくてはならない。

  - オブジェクト（順序づけされていないキーと値のペアの集まり。JSONでは[連想配列](../Page/連想配列.md "wikilink")と等価）
  - [配列](../Page/配列.md "wikilink")（データのシーケンス）
  - 数値（[整数](../Page/整数.md "wikilink")、[浮動小数点数](../Page/浮動小数点数.md "wikilink")）
  - 文字列（バックスラッシュによるエスケープシーケンス記法を含む、ダブルクォーテーション`"`でくくった文字列）
  - 真偽値（`true` と `false`）
  - `null`

数値は[10進法](https://ja.wikipedia.org/wiki/10進法 "wikilink")表記に限り、8進、16進法表記などはできない。また[浮動小数点数](../Page/浮動小数点数.md "wikilink")としては `1.0e-10` といった[指数表記](../Page/指数表記.md "wikilink")もできる。

文字列は（JSONそれ自体と同じく）[Unicode](../Page/Unicode.md "wikilink")文字列である。基本的にはJavaScriptの文字列リテラルと同様だが、囲むのにシングルクォートは使えない。バックスラッシュによるエスケープがある。

配列はゼロ個以上の値をコンマで区切って、角かっこでくくることで表現する。例えば以下のように表現する：

``` json
["milk", "bread", "eggs"]
```

オブジェクトはキーと値のペアをコロンで対にして、これらの対をコンマで区切ってゼロ個以上列挙し、全体を波かっこでくくることで表現する。例えば以下のように表現する：

``` json
{"name": "John Smith", "age": 33}
```

ここで注意することはキーとして使うデータ型は文字列に限ることである。したがって、

``` json
{name: "John Smith", age: 33}
```

という表記は許されない。この後者の表記はJavaScriptのオブジェクトの表記法としては正しいが、JSONとしては不正な表記である。

プログラム上で生成した文字列をJSONとして扱う場合、ダブルクォーテーション`"`を含む文字列を利用しなければいけないことに注意が必要である。なぜならコード上の`"`は文字列定義に利用される`"`であり、生成されるのはあくまで文字列`hello`であって文字列`"hello"`ではない。JSONの文字列型は後者であると定義されているので、以下のようにエラーを発生させる。利用時にはJSON生成関数（例 JavaScript: `JSON.stringify`）を利用する方がより安全である。

``` javascript
const invalidJSON = "hello";
const validJSON =  '"hello"';

JSON.parse(invalidJSON)
// Thrown:
// SyntaxError: Unexpected token h in JSON at position 0
JSON.parse(validJSON)
// 'hello'

// safe JSON generation
const output = JSON.stringify("hello")
output
// '"hello"'
```

### エンコーディング

RFC 8259より、閉じられたエコシステムで利用する場合を除き、文字コードは[UTF-8](../Page/UTF-8.md "wikilink")でエンコードすることが必須 (MUST) となっている。ネットワークでJSONを送信する場合は、[バイトオーダーマーク](https://ja.wikipedia.org/wiki/バイトオーダーマーク "wikilink")を先頭に付加してはいけない (MUST NOT)。

過去のIETFの仕様では、JSONテキストは[Unicode](../Page/Unicode.md "wikilink")でエンコードするとされていた (SHALL)。デフォルトのエンコーディングはUTF-8であった。なお、単独の文字列でない限り最初の2文字は必ず[ASCII](../Page/ASCII.md "wikilink")文字であるので、最初の4バイトを見ることにより、UTF-8、UTF-16LE、UTF-16BE、UTF-32LE、UTF-32BEのいずれの形式でエンコードされているか判別できた。

## AjaxにおけるJSONの利用

[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")において[XMLHttpRequest](../Page/XMLHttpRequest.md "wikilink")で非同期にJSONでのデータを受け取る例を示す：

### 古典的な例

``` javascript
var the_object;
var http_request = new XMLHttpRequest();
http_request.open( "GET", url, true );
http_request.onreadystatechange = function () {
    if ( http_request.readyState == 4 ) {
        if ( http_request.status == 200 ) {
            the_object = eval( "(" + http_request.responseText + ")" );
        } else {
            alert( "There was a problem with the URL." );
        }
        http_request = null;
    }
};
http_request.send(null);
```

### 新しい記法を利用した例

``` javascript
var the_object;
var http_request = new XMLHttpRequest();
http_request.open( "GET", url, true );
http_request.responseType = "json";
http_request.addEventListener ( "load", function ( ev ) {
    if ( ev.target.status == 200 ) {
        the_object = http_request.response;
    } else {
        alert( "There was a problem with the URL." );
    }
    delete http_request;
});
http_request.send(null);
```

ここでいずれも、`http_request` は[XMLHttpRequest](../Page/XMLHttpRequest.md "wikilink")オブジェクトであり、それを `url` にアクセスして返ってきたJSONで記述されたデータを `the_object` に格納される。いま、XMLHttpRequestを用いて実装をしたが、iframeなどの他の実装方法もある。また、[JavaScript](../Page/JavaScript.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")の[prototype.js](https://ja.wikipedia.org/wiki/prototype.js "wikilink")では[HTTPの](../Page/Hypertext_Transfer_Protocol.md "wikilink") `X-JSON` ヘッダを利用して簡単にJSONデータの受渡しができる。

## 他のデータ記述法との関係

  - [XML](../Page/Extensible_Markup_Language.md "wikilink")
    JSONはXMLと違って[マークアップ言語](../Page/マークアップ言語.md "wikilink")ではない。[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")から利用できるという点では共通している。また両者とも巨大な[バイナリ](../Page/バイナリ.md "wikilink")データを扱う仕組みがないことが共通している。
  - [YAML](../Page/YAML.md "wikilink")
    JSONはYAMLのサブセットと見なしてよい\[7\]。YAMLにはブロック形式とインライン形式（フロー形式）の表記法があるが、JSONは後者にさらに制約を加えたものと捉えることができる。例えば[Ruby](../Page/Ruby.md "wikilink")では以下のようにしてJSONをYAMLとして読み込むことができる：
    ``` ruby
    the_object = YAML.load('{"name": "John Smith", "age": 33}')
    ```
    YAML 1.1以前は、配列と連想配列の区切りをそれぞれ `,` のようにカンマ+スペースの形にすることでJSONの[スーパーセットとなったが](https://ja.wikipedia.org/wiki/上位互換 "wikilink")、YAML 1.2では区切り文字も互換となったため、正常なJSON文書においては公式に完全なスーパーセットとなった。僅かな相違点として、連想配列のキーがユニークであるべきことをJSONではSHOULDレベルで要請するのに対し、YAML 1.2ではMUSTレベルで要請している\[8\]為、該当する異常データのエラーハンドリングに違いが出る可能性はある。

## 実装

JSONは多くの[プログラミング言語](../Page/プログラミング言語.md "wikilink")で利用可能である。例えば、[ActionScript](../Page/ActionScript.md "wikilink"), [C](../Page/C言語.md "wikilink"), [C++](../Page/C++.md "wikilink"), [C\#](../Page/C_Sharp.md "wikilink"), [ColdFusion](../Page/ColdFusion.md "wikilink"), [Common Lisp](../Page/Common_Lisp.md "wikilink"), [Curl](../Page/Curl_\(プログラミング言語\).md "wikilink"), [D言語](../Page/D言語.md "wikilink"), [Delphi](../Page/Delphi.md "wikilink"), [E](https://ja.wikipedia.org/wiki/E言語 "wikilink"), [Erlang](../Page/Erlang.md "wikilink"), [Groovy](../Page/Groovy.md "wikilink"), [Haskell](../Page/Haskell.md "wikilink"), [Java](https://ja.wikipedia.org/wiki/Java "wikilink"), [JavaScript](../Page/JavaScript.md "wikilink") ([ECMAScript](../Page/ECMAScript.md "wikilink")), [Lisp](https://ja.wikipedia.org/wiki/LISP "wikilink"), [Lua](../Page/Lua.md "wikilink"), [ML](https://ja.wikipedia.org/wiki/プログラミング言語ML "wikilink"), [Objective-C](../Page/Objective-C.md "wikilink"), [Objective CAML](../Page/OCaml.md "wikilink"), [Perl](../Page/Perl.md "wikilink"), [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink"), [Python](../Page/Python.md "wikilink"), [R](../Page/R言語.md "wikilink"), [Rebol](https://ja.wikipedia.org/wiki/Rebol "wikilink"), [Ruby](../Page/Ruby.md "wikilink"), [Scala](../Page/Scala.md "wikilink"), [Squeak](../Page/Squeak.md "wikilink")など。

## 出典

## 関連項目

  - [Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")
  - [JSONP](https://ja.wikipedia.org/wiki/JSONP "wikilink")
  - [JSON Schema](https://ja.wikipedia.org/wiki/JSON_Schema "wikilink")
  - [JSON-RPC](https://ja.wikipedia.org/wiki/JSON-RPC "wikilink")
  - [JSON Web Token](https://ja.wikipedia.org/wiki/JSON_Web_Token "wikilink")
  - [MooTools](https://ja.wikipedia.org/wiki/MooTools "wikilink")
  - [コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")

## 外部リンク

  - [Introducing JSON](https://www.json.org/)
  - [JSONの紹介](https://www.json.org/json-ja.html)
  - [JSON Tools](https://www.yamlonline.com/) --Online
  - IETFの仕様書
      - [IETF STD 90](https://tools.ietf.org/html/std90) および RFC 8259
      - 古い廃止された仕様書
          - RFC 4627
          - RFC 7158
          - RFC 7159
  - [ECMA-404](https://www.ecma-international.org/publications/standards/Ecma-404.htm)

[Category:JSON](https://ja.wikipedia.org/wiki/Category:JSON "wikilink") [Category:データシリアライゼーションフォーマット](https://ja.wikipedia.org/wiki/Category:データシリアライゼーションフォーマット "wikilink") [Category:JavaScript](https://ja.wikipedia.org/wiki/Category:JavaScript "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:プログラミング言語の構文](https://ja.wikipedia.org/wiki/Category:プログラミング言語の構文 "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink")

1.  JSON is a lightweight, text-based, language-independent syntax for defining data interchange formats. [ECMA-404](http://www.ecma-international.org/publications/standards/Ecma-404.htm)
2.
3.  [ongoing by Tim Bray · The Last JSON Spec](https://www.tbray.org/ongoing/When/201x/2017/12/14/RFC-8259-STD-90)
4.
5.  [Douglas Crockford: The JSON Saga - YouTube](https://www.youtube.com/watch?v=-C-JoyNuQJs)
6.  A JSON value can be an object, array, number, string, true, false, or null. [ECMA-404](http://www.ecma-international.org/publications/standards/Ecma-404.htm)
7.
8.