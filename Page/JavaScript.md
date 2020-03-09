> この記事は[JavaScript](https://ja.wikipedia.org/wiki/JavaScript)から翻訳されています。


**JavaScript**（ジャバスクリプト）とは、[プログラミング言語](../Page/プログラミング言語.md "wikilink")のひとつである。[Java](https://ja.wikipedia.org/wiki/Java "wikilink")と名前が似ているが、全く異なるプログラミング言語である（後述の[\#歴史](https://ja.wikipedia.org/wiki/#歴史 "wikilink")を参照）。

JavaScriptは[プロトタイプベース](https://ja.wikipedia.org/wiki/プロトタイプベース "wikilink")の[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")[スクリプト言語](https://ja.wikipedia.org/wiki/スクリプト言語 "wikilink")であるが、[クラス](https://ja.wikipedia.org/wiki/クラス "wikilink")などの[クラスベース](https://ja.wikipedia.org/wiki/クラスベース "wikilink")に見られる機能も取り込んでいる。

[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")上で動作し動的な[ウェブサイト](https://ja.wikipedia.org/wiki/ウェブサイト "wikilink")構築や[リッチインターネットアプリケーション](https://ja.wikipedia.org/wiki/リッチインターネットアプリケーション "wikilink")の開発に用いられる。また、[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")以降は[node.js](https://ja.wikipedia.org/wiki/node.js "wikilink")などのサーバサイドJavaScript実行環境や各種ライブラリの充実により、。

## 概要

**JavaScript**という言葉は狭義には[Mozillaが仕様を策定し実装しているスクリプト言語を指す](https://ja.wikipedia.org/wiki/Mozilla_Foundation "wikilink")。このスクリプト言語は[Ecmaインターナショナル](https://ja.wikipedia.org/wiki/Ecmaインターナショナル "wikilink")で[ECMAScript](https://ja.wikipedia.org/wiki/ECMAScript "wikilink") (ECMA-262) として標準化されており、多くのウェブブラウザ等はこの標準化されたECMAScriptを実装している。たとえば、[マイクロソフト](https://ja.wikipedia.org/wiki/マイクロソフト "wikilink")による実装は[JScript](https://ja.wikipedia.org/wiki/JScript "wikilink")と呼ぶ。

一般的に**JavaScript**という言葉が使われるときはこのようなさまざまなECMAScriptの実装も含んだ幅広い意味で使われるので、どちらの意味でJavaScriptという言葉が使われているかは文脈で判断する必要がある\[1\]。

ECMAScriptは仕様自体に独自の拡張を条件付きで認める記述があり\[2\]、現在主要なブラウザが実装しているスクリプト言語はすべてECMAScriptに準拠していることになる。広義の意味でこれをJavaScriptと呼ぶ場合、主要なブラウザが実装しているスクリプト言語はマイクロソフトや[Google](https://ja.wikipedia.org/wiki/Google "wikilink")、[アップルの実装も含めてJavaScriptである](https://ja.wikipedia.org/wiki/アップル_\(企業\) "wikilink")。

なお、ウェブブラウザでよく実装されている[APIである](https://ja.wikipedia.org/wiki/アプリケーションプログラミングインタフェース "wikilink")[DOM](https://ja.wikipedia.org/wiki/Document_Object_Model "wikilink") (Document Object Model) はECMAScriptの仕様の一部ではないので、DOMの準拠の有無はECMAScriptの準拠の有無とは関係ない。

## プログラミング言語としての特徴

JavaScriptは[プロトタイプベース](https://ja.wikipedia.org/wiki/プロトタイプベース "wikilink")の[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")プログラミング言語で、それに分類される言語同様、静的にクラスを定義すること無くオブジェクトを利用する\[3\]。多くの場合は[C言語](../Page/C言語.md "wikilink")に似た[手続き型言語](https://ja.wikipedia.org/wiki/手続き型言語 "wikilink")のようなスタイルで書かれるが、[第一級関数](https://ja.wikipedia.org/wiki/第一級関数 "wikilink")をサポートしており関数を[第一級オブジェクト](https://ja.wikipedia.org/wiki/第一級オブジェクト "wikilink")として扱えるなど、[関数型言語](../Page/関数型言語.md "wikilink")の性質も持ち合わせている。そのような柔軟な設計から、いくつかの[アプリケーションでは](https://ja.wikipedia.org/wiki/アプリケーションソフトウェア "wikilink")[マクロ言語](https://ja.wikipedia.org/wiki/マクロ言語 "wikilink")としても採用されている。例えば[Adobe Acrobatは](https://ja.wikipedia.org/wiki/Adobe_Acrobat "wikilink")、JavaScriptによるマクロ機能を搭載している。

成立の経緯（[\#歴史](https://ja.wikipedia.org/wiki/#歴史 "wikilink")を参照）から、当初は処理系の間の互換性に難があり、[Prototype JavaScript Frameworkなどのライブラリがそれらの違いを吸収することで解決が図られた](https://ja.wikipedia.org/wiki/Prototype_JavaScript_Framework "wikilink")。

[Aptana](https://ja.wikipedia.org/wiki/Aptana "wikilink")や[Eclipse](https://ja.wikipedia.org/wiki/Eclipse_\(統合開発環境\) "wikilink")、[NetBeans](https://ja.wikipedia.org/wiki/NetBeans "wikilink")、[IntelliJ IDEAなどの統合開発環境はJavaScriptをサポートしており](https://ja.wikipedia.org/wiki/IntelliJ_IDEA "wikilink")、大規模開発が可能になっている。さらに[Ext JSなどの本格的な](https://ja.wikipedia.org/wiki/Ext_JS "wikilink")[GUIライブラリの登場により](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、デスクトップアプリケーションと遜色ないユーザインタフェースの構築が可能になった。

JavaScriptプログラムのための各種のAPIが[W3Cや](https://ja.wikipedia.org/wiki/World_Wide_Web_Consortium "wikilink")[WHATWGにより策定されており](https://ja.wikipedia.org/wiki/Web_Hypertext_Application_Technology_Working_Group "wikilink")、[クライアント・サーバ間の通信のための](https://ja.wikipedia.org/wiki/クライアントサーバモデル "wikilink")[XMLHttpRequest](https://ja.wikipedia.org/wiki/XMLHttpRequest "wikilink")や[WebSocket](https://ja.wikipedia.org/wiki/WebSocket "wikilink")、[マルチスレッド実行のための](https://ja.wikipedia.org/wiki/スレッド_\(コンピュータ\) "wikilink")[Web Workerなどが利用可能となっている](https://ja.wikipedia.org/wiki/Web_Worker "wikilink")。

一方、プロトタイプベースの言語は[クラスベース](https://ja.wikipedia.org/wiki/クラスベース "wikilink")に比較して少数派であり、[CoffeeScript](https://ja.wikipedia.org/wiki/CoffeeScript "wikilink")を筆頭に、いわゆるAltJSと呼ばれる、クラスベースを採用した言語が開発され、これらはJavaScriptに[トランスパイル](https://ja.wikipedia.org/wiki/トランスパイル "wikilink")して使用する。

## 歴史

### 誕生

JavaScriptは[ネットスケープコミュニケーションズ](../Page/ネットスケープコミュニケーションズ.md "wikilink")の[ブレンダン・アイク](https://ja.wikipedia.org/wiki/ブレンダン・アイク "wikilink")によって開発され、[Netscape Navigator](https://ja.wikipedia.org/wiki/Netscape_Navigator_\(ネットスケープコミュニケーションズ\) "wikilink") 2.0で実装された。開発当初は*LiveScript*と呼ばれていたが、[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")に[サン・マイクロシステムズ](https://ja.wikipedia.org/wiki/サン・マイクロシステムズ "wikilink")（現・[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")）が開発したプログラミング言語**Java**が当時大きな注目を浴びており、ネットスケープとサン・マイクロシステムズが業務提携していた事もあったため、**JavaScript**という名前に変更された\[4\]\[5\]。最初の[JavaScriptエンジン](https://ja.wikipedia.org/wiki/JavaScriptエンジン "wikilink")はブレンダン・アイクによりNetscape Navigatorのために作成されたものであった。このエンジンは[SpiderMonkey](https://ja.wikipedia.org/wiki/SpiderMonkey "wikilink")と呼ばれており、[C言語](../Page/C言語.md "wikilink")で実装されていた。また、全て[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で記述されたJavaScriptエンジンである[Rhino](https://ja.wikipedia.org/wiki/Rhino "wikilink")も同じくNetscapeのNorris Boyd（後にGoogleに移籍）らにより作成された。

[1996年](../Page/1996年.md "wikilink")に[マイクロソフト](https://ja.wikipedia.org/wiki/マイクロソフト "wikilink")の[Internet Explorer](https://ja.wikipedia.org/wiki/Internet_Explorer "wikilink") 3.0に搭載されるようになると、その手軽さからJavaScriptは急速に普及していく。[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")、通信に関する標準を策定する国際団体EcmaインターナショナルによってJavaScriptの中核的な仕様が**ECMAScript**として標準化され\[6\]、多くのウェブブラウザで利用できるようになった。

ネットスケープは、ウェブアプリケーション開発言語として自社のサーバ製品に実装したLiveWire JavaScriptも発表したが\[7\]、こちらはあまり普及しなかった。

JavaScriptの登場初期は、ブラウザベンダー間で言語仕様の独自拡張が行われていたため、ブラウザ間の互換性が極めて低かった。ECMAScriptの策定以降は実装間の互換性は向上し、[DOMなど関連仕様の実装に関する互換性も高くなっていった](https://ja.wikipedia.org/wiki/Document_Object_Model "wikilink")。

### 発展

市場のブラウザ間互換性がある程度確立された[2000年](../Page/2000年.md "wikilink")頃には、[Google](https://ja.wikipedia.org/wiki/Google "wikilink")や[Amazon等の大手企業もJavaScriptを積極的に利用し始めた](https://ja.wikipedia.org/wiki/Amazon.com "wikilink")。[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")、マイクロソフトが開発したJavaScriptの非同期通信を利用した技術に[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")という名前が付けられたことによって、高機能なウェブアプリケーション開発言語の一つとして再び注目を集めた。初期にAjaxを利用した代表的なアプリケーションとして、[Google マップ](https://ja.wikipedia.org/wiki/Google_マップ "wikilink")\[[http://maps.google.co.jp/\]や](http://maps.google.co.jp/%5Dや)[Amazon Diamond Search](https://ja.wikipedia.org/wiki/Amazon_Diamond_Search "wikilink")\[[http://www.amazon.com/gp/gsl/search/finder/\]などがある](http://www.amazon.com/gp/gsl/search/finder/%5Dなどがある)。

また、JavaScriptはウェブブラウザの拡張機能を開発するための言語としても使われるようになった。当初は拡張機能用のAPIが統一されていなかったが、互換性を高めようとする動きがある\[8\]。

当初は[インタプリタ](../Page/インタプリタ.md "wikilink")方式で実行されることが一般的であったためJavaScriptの実行速度はさほど速くなかったが、現在では[JITコンパイルなどを利用した各種の最適化がなされており](https://ja.wikipedia.org/wiki/実行時コンパイラ "wikilink")、各ウェブブラウザのベンダーともに高速化を図ってしのぎを削っている。さらには、この高速化を受ける形で、[Node.js](https://ja.wikipedia.org/wiki/Node.js "wikilink")のように[サーバサイドでもJavaScriptを使う動きが見られるようになった](https://ja.wikipedia.org/wiki/サーバーサイド・スクリプト "wikilink")。

### JavaScript 2.0

次世代のJavaScriptとして“JavaScript 2.0”を作ろうとした動きは2度あったが、いずれもまとまらなかった。

1度目はECMAScript 3が完成したのち2000年から2003年にかけて発生したが、ネットスケープとマイクロソフトの対立でまとまらなかった。当時ネットスケープが提案していた案は[アドビの](https://ja.wikipedia.org/wiki/アドビシステムズ "wikilink")[ActionScript](https://ja.wikipedia.org/wiki/ActionScript "wikilink") 2.0に引き継がれ、マイクロソフトの案は[JScript .NETへと引き継がれた](https://ja.wikipedia.org/wiki/JScript#JScript_.NET "wikilink")。

その後もネットスケープ及び[Mozilla FoundationはECMAScriptの策定に並行してJavaScriptを拡張し](https://ja.wikipedia.org/wiki/Mozilla_Foundation "wikilink")、JavaScript 1.x系列としてバージョンアップを繰り返していた。ECMAScript側ではECMAScript 4の策定が1999年以降進められており\[9\]、2006年の時点で[Mozilla Foundationはこれに基づいてJavaScript](https://ja.wikipedia.org/wiki/Mozilla_Foundation "wikilink") 2.0を作成することを表明していた。MozillaはECMAScript 4の策定にあたって、[Python](../Page/Python.md "wikilink")の文法を一部取り込んだ案を提案しており、自身でもこれを実装していた\[10\]。

しかしその後、ECMAScriptの標準化作業がMozilla、Adobe、Opera、Googleらが推すECMAScript 4と、Microsoft、Yahoo\!らが推すECMAScript 3.1に事実上分裂してしまった影響から、2008年8月に大きな方針転換があり、ECMAScript 4は破棄され後者がECMAScript 5として2009年に標準化された。ECMAScript 4に入る予定だった機能は新たに発足した「**ECMAScript Harmony**」に先送りとなった\[11\]。これは後にECMAScript 2015として標準化が完了した。

なお、ECMAScript 5が標準化されて以降、MozillaのJavaScript実装はECMAScriptへの準拠を謳うようになった\[12\]ためバージョン番号での呼称は行われなくなり、JavaScript 2.0は[死語となった](https://ja.wikipedia.org/wiki/廃語 "wikilink")。

## 文法

### 基本的な文法

JavaScriptの[変数は](https://ja.wikipedia.org/wiki/変数_\(プログラミング\) "wikilink") `var`\[13\], `let`\[14\]および`const`\[15\] キーワードを使用して宣言できる。

``` javascript
var x; // 変数xの宣言。値が未指定のため、特殊な値である undefined が入った状態となる。
var y = 2; // 変数yの宣言。同時に 2 が代入される。
```

上記例の[スラッシュ](../Page/スラッシュ_\(記号\).md "wikilink")2文字以降は[コメントである](https://ja.wikipedia.org/wiki/コメント_\(コンピュータ\) "wikilink")。

JavaScriptは言語仕様に[I/Oが組み込まれておらず](https://ja.wikipedia.org/wiki/入出力 "wikilink")、それらは実行環境により提供される。ECMAScript 5.1の仕様では以下のように言及されている。\[16\]

> この仕様の中では外部データの入力または計算結果の出力は供給しない。
> (… indeed, there are no provisions in this specification for input of external data or output of computed results.)

しかし、ほとんどの実行環境はConsole Standard\[17\]で規定されている `console` オブジェクトを持っており\[18\]、そこにコンソール出力を行える。以下に最小の[Hello worldプログラムを示す](https://ja.wikipedia.org/wiki/Hello_world "wikilink")。

``` javascript
console.log("Hello World!");
```

[再帰](https://ja.wikipedia.org/wiki/再帰 "wikilink")関数は以下のように書ける。

``` javascript
function factorial(n) {
    if (n == 0) {
        return 1;
    }
    return n * factorial(n - 1);
}
```

[無名関数](https://ja.wikipedia.org/wiki/無名関数 "wikilink")（またはラムダ式）の構文と[クロージャ](https://ja.wikipedia.org/wiki/クロージャ "wikilink")の例は以下である。

``` javascript
// ECMAScript 5以前の記法
var displayClosure = function() {
    let count = 0;
    // ECMAScript 2015以降で可能な記法
    return ()=> {
        return ++count;
    };
}
var inc = displayClosure();
inc(); // 1 が返る
inc(); // 2 が返る
inc(); // 3 が返る
```

[可変長引数](https://ja.wikipedia.org/wiki/可変長引数 "wikilink")は以下のように記述する\[19\]。

``` javascript
var sum = function(...args) {
    let x = 0;
    for (const v of args) {
        x += v;
    }
    return x;
}
sum(1, 2, 3); // 6 が返る
```

(IIFE) の例。関数を用いることで変数を[クロージャ](https://ja.wikipedia.org/wiki/クロージャ "wikilink")に閉じ込めることができる。

``` JavaScript
var v;
v = 1;
var getValue = (function(v) {
  return function() {return v;};
})(v);

v = 2;

getValue(); // 1 が返る
```

### 複雑な例

以下のサンプルコードは、様々なJavaScriptの機能を示したものである。

``` javascript
"use strict"; // strictモードの宣言
/* 2つの数値の最小公倍数を求める */
function LCMCalculator(x, y) { // コンストラクタ関数
    const checkInt = (x)=> { // 入れ子の関数
        if (x % 1 !== 0) {
            throw new TypeError(x + " is not an integer"); // 例外のスロー
        }
        return x;
    };
    //   行末のセミコロンは省略可能な場合があるが、省略は推奨されない。
    this.a = checkInt(x)
    this.b = checkInt(y);
}
// オブジェクトのプロトタイプはコンストラクタ関数の prototype プロパティに格納する
LCMCalculator.prototype = { // オブジェクトリテラル
    constructor: LCMCalculator, // このようにプロトタイプを上書きする場合は、
                                // constructorプロパティにコンストラクタ関数名を再指定する
    gcd: function () { // 最大公約数を計算するメソッド
        // 「ユークリッドの互除法」アルゴリズムで計算
        let a = Math.abs(this.a), b = Math.abs(this.b);
        if (a < b) {
            // 変数の入れ替え
            const t = b;
            b = a;
            a = t;
        }
        while (b !== 0) {
            const t = b;
            b = a % b;
            a = t;
        }
        // 最大公約数の計算は一度でよいため、自分自身を計算済みの結果を返すメソッドで再定義（上書き）する。
        // （これにより LCMCalculator.prototype.gcd の代わりに this.gcd が呼ばれるようになる。
        //   ただし、計算後にプロパティ a や b が変更されてしまうと、結果は誤りとなる。）
        // なお 'gcd' === "gcd", this['gcd'] === this.gcd である。
        this['gcd'] = function () {
            return a;
        };
        return a;
    },
    lcm : function () { // 最小公倍数を計算するメソッド
        // 変数名は、オブジェクトのプロパティと衝突しない。例）lcm は this.lcm とは異なる。
        // 以下では、浮動小数の精度の問題を避けるために this.a * this.b としていない。
        const lcm = this.a/this.gcd()*this.b;
        // 最小公倍数の計算も一度でよいため、自分自身を計算済みの結果を返すメソッドで再定義（上書き）する。
        this.lcm = function () {
            return lcm;
        };
        return lcm;
    },
    toString: function () { // toStringはオブジェクトを文字列に変換するときに呼ばれるメソッド。
        // テンプレート文字列により文字列中に値を埋め込むことができる。
        return `LCMCalculator: a = ${this.a}, b = ${this.b}`;
    }
};

// 汎用の出力関数の定義。この実装はWebブラウザ上でのみ動作する。
function output(x) {
    document.body.appendChild(document.createTextNode(x));
    document.body.appendChild(document.createElement('br'));
}

// 無名関数はさまざまな書き方が可能
[[25,_55],_[21,_56],_[22,_58],_[28,_56|25, 55], [21, 56], [22, 58], [28, 56]].map(([a, b])=> new LCMCalculator(a, b)) // 配列リテラル + マッピング関数
.sort((a, b)=> a.lcm() - b.lcm()) // 指定した比較関数を用いたソート
.forEach(obj=> {
    output(obj + ", gcd = " + obj.gcd() + ", lcm = " + obj.lcm());
});
```

上記コードをウェブブラウザ上で実行すると、以下の結果が表示される。

``` html4strict
LCMCalculator: a = 28, b = 56, gcd = 28, lcm = 56
LCMCalculator: a = 21, b = 56, gcd = 7, lcm = 168
LCMCalculator: a = 25, b = 55, gcd = 5, lcm = 275
LCMCalculator: a = 22, b = 58, gcd = 2, lcm = 638
```

## JavaScriptの利用

### Webページでの利用

JavaScriptの最も歴史の長い使用法は[HTMLページにクライアント側のふるまいを持たせることである](https://ja.wikipedia.org/wiki/HyperText_Markup_Language "wikilink")。これは当初は[ダイナミックHTML](https://ja.wikipedia.org/wiki/ダイナミックHTML "wikilink") (DHTML) として知られていた。JavaScriptはHTMLに直接埋め込まれまたは別のファイルからインクルードされ、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")上のJavaScript実行環境で動作する。ウェブブラウザは通常、[Document Object Model](https://ja.wikipedia.org/wiki/Document_Object_Model "wikilink") (DOM) を扱うためのホストオブジェクトを提供する。

JavaScriptの使用例としては、以下のようなものがある。

  - ページの再読み込みなしで新しいコンテンツを読み込むまたはサーバーに投稿する（[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")。例えば、SNSでページを離れることなく新しい投稿を表示することができる）。

  - ゲームなどの動的なコンテンツを提供する。

  - データをサーバーに送信せずに[フォーム入力値の](https://ja.wikipedia.org/wiki/フォーム_\(ウェブ\) "wikilink")を行う。

  - や、[パーソナライゼーション](https://ja.wikipedia.org/wiki/パーソナライゼーション "wikilink")などのためにユーザーの閲覧情報を収集する。\[20\]

JavaScriptはユーザーのブラウザ上で動作できることから、ユーザーの操作に対して素早く反応することができ、アプリケーションをよりレスポンシブにすることができる。さらにJavaScriptはHTML単独では対応できない操作、例えばキー入力などにも応答することができる。[Gmail](https://ja.wikipedia.org/wiki/Gmail "wikilink")のようなアプリケーションでは、JavaScriptでUIロジックを実装し、さらにJavaScriptでサーバーから情報（例えばeメールのメッセージ）を取得することで、こうしたメリットを享受している。このような利点から[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")は大きなトレンドとなった。

JavaScriptは主要ウェブブラウザの大半でサポートされている唯一の言語であることから、意図されたことではなかったが、様々な言語やフレームワークの[コンパイル先の出力言語となっている](../Page/コンパイラ.md "wikilink")\[21\]。動的な言語であることからパフォーマンスが制限されるにも関わらず、JavaScriptエンジンの性能向上によりこうした言語は予想外の発展を見せている。

#### 例

以下はJavaScriptとDOMを含むWebページのごく単純な例である。

``` html5
<!DOCTYPE html>
<html>
    <meta charset="utf-8">
    <title>単純な例</title>

    <body>
        <h1 id="header">これはJavaScriptです</h1>

        <script>
            document.body.appendChild(document.createTextNode('Hello World!'));

            var h1 = document.getElementById('header'); // id='header'の<h1>要素の参照を取得。
            h1 = document.getElementsByTagName('h1')[0]; // または<h1>要素を全て取得してそこから先頭を取得。
        </script>

        <noscript>表示中のブラウザはJavaScriptをサポートしていないか、OFFになっています。</noscript>
    </body>
</html>
```

### その他の環境での利用

ウェブブラウザ以外のJavaScript実行環境も存在する（を参照）。[データベース](../Page/データベース.md "wikilink")や[Webサーバー](https://ja.wikipedia.org/wiki/Webサーバー "wikilink")に組み込まれ、それらのAPIや[HTTPリクエストやレスポンスのアクセスが提供されているものもある](../Page/Hypertext_Transfer_Protocol.md "wikilink")。

また、[Node.js](https://ja.wikipedia.org/wiki/Node.js "wikilink")のように[OSの機能](../Page/オペレーティングシステム.md "wikilink")（[ネットワーク](https://ja.wikipedia.org/wiki/ネットワーク "wikilink")や[ファイルシステム](https://ja.wikipedia.org/wiki/ファイルシステム "wikilink")など）にアクセスできる環境も存在する。加えて[Electronなどの](https://ja.wikipedia.org/wiki/Electron_\(ソフトウェア\) "wikilink")[アプリケーションフレームワーク](https://ja.wikipedia.org/wiki/アプリケーションフレームワーク "wikilink")の登場により、[Atomなどのアプリケーションが広まりつつある](https://ja.wikipedia.org/wiki/Atom_\(テキストエディタ\) "wikilink")。

## バージョンとブラウザの対応表

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>日付</p></th>
<th><p>規格</p></th>
<th><p>Netscape<br />
Navigator</p></th>
<th><p>Mozilla<br />
Firefox</p></th>
<th><p>Internet<br />
Explorer</p></th>
<th><p>Opera</p></th>
<th><p>Safari</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.0</p></td>
<td><p>1996年3月</p></td>
<td></td>
<td><p>2.0</p></td>
<td></td>
<td><p>3.0</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.1</p></td>
<td><p>1996年8月</p></td>
<td></td>
<td><p>3.0</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.2</p></td>
<td><p>1997年7月</p></td>
<td></td>
<td><p>4.0-4.05</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.3</p></td>
<td><p>1998年10月</p></td>
<td><p>ECMA-262 1<sup>st</sup> edition / ECMA-262 2<sup>nd</sup> edition</p></td>
<td><p>4.06-4.7x</p></td>
<td></td>
<td><p>4.0</p></td>
<td><p>5.0</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.4</p></td>
<td></td>
<td></td>
<td><p>Netscape<br />
Server</p></td>
<td></td>
<td></td>
<td><p>6.0</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.5</p></td>
<td><p>2000年11月</p></td>
<td><p>ECMA-262 3<sup>rd</sup> edition</p></td>
<td><p>6.0</p></td>
<td><p>1.0</p></td>
<td><p>5.5 (JScript 5.5),<br />
6.0 (JScript 5.6),<br />
7.0 (JScript 5.7),<br />
8.0 (JScript 6.0)</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.6</p></td>
<td><p>2005年11月</p></td>
<td><p>1.5 + Array extras + Array and String generics + E4X</p></td>
<td><p>7.0-8.0</p></td>
<td><p>1.5</p></td>
<td></td>
<td><p>7.0-9.0</p></td>
<td><p>3.0, 3.1</p></td>
</tr>
<tr class="even">
<td><p>1.7</p></td>
<td><p>2006年10月</p></td>
<td><p>1.6 + Pythonic generators + Iterators + let</p></td>
<td></td>
<td><p>2.0</p></td>
<td></td>
<td></td>
<td><p>3.2-5.1</p></td>
</tr>
<tr class="odd">
<td><p>1.8</p></td>
<td><p>2008年7月</p></td>
<td><p>1.7 + Generator expressions + Expression closures</p></td>
<td></td>
<td><p>3.0</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.8.1</p></td>
<td></td>
<td><p>1.8 + Minor Updates</p></td>
<td></td>
<td><p>3.5</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1.9</p></td>
<td></td>
<td><p>1.8.1 + <a href="https://ja.wikipedia.org/wiki/ECMAScript" title="wikilink">ECMAScript</a> 5[22] Compliance</p></td>
<td></td>
<td><p>4.0-11.0</p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

\[23\]

## JavaScriptライブラリ

代表的なJavaScriptライブラリは以下のとおり。

  - [AngularJS](https://ja.wikipedia.org/wiki/AngularJS "wikilink")

  - [Backbone.js](https://ja.wikipedia.org/wiki/Backbone.js "wikilink")

  - [Dojo Toolkit](https://ja.wikipedia.org/wiki/Dojo_Toolkit "wikilink")

  - [Express.js](https://ja.wikipedia.org/wiki/Express.js "wikilink")

  - [Ext JS](https://ja.wikipedia.org/wiki/Ext_JS "wikilink")

  - [Google Web Toolkit](https://ja.wikipedia.org/wiki/Google_Web_Toolkit "wikilink") (GWT)

  - [Impact](https://ja.wikipedia.org/wiki/Impact "wikilink")

  - [jQuery](https://ja.wikipedia.org/wiki/jQuery "wikilink")

  - [MochiKit](https://ja.wikipedia.org/wiki/MochiKit "wikilink")

  - [MooTools](https://ja.wikipedia.org/wiki/MooTools "wikilink")

  - [Prototype JavaScript Framework](https://ja.wikipedia.org/wiki/Prototype_JavaScript_Framework "wikilink") (prototype.js)

  - [QUnit](https://ja.wikipedia.org/wiki/QUnit "wikilink")

  -
  - [WinJS](https://ja.wikipedia.org/wiki/WinJS "wikilink")

  - [React](https://ja.wikipedia.org/wiki/React "wikilink")

  - [Vue.js](https://ja.wikipedia.org/wiki/Vue.js "wikilink")

### Vanilla JS

ライブラリを使用しないJavaScriptは[Vanilla](https://ja.wikipedia.org/wiki/バニラ_\(ソフトウェア\) "wikilink") JSと称されることがある。

## 脚注

## 関連項目

  - [ECMAScript](https://ja.wikipedia.org/wiki/ECMAScript "wikilink")
      - [ActionScript](https://ja.wikipedia.org/wiki/ActionScript "wikilink")
      - [JScript](https://ja.wikipedia.org/wiki/JScript "wikilink")
  - [Document Object Model](https://ja.wikipedia.org/wiki/Document_Object_Model "wikilink") (DOM) - [ダイナミックHTML](https://ja.wikipedia.org/wiki/ダイナミックHTML "wikilink") - [スタイルシート](https://ja.wikipedia.org/wiki/スタイルシート "wikilink")
  - [Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")
  - [サーバーサイド・スクリプト](https://ja.wikipedia.org/wiki/サーバーサイド・スクリプト "wikilink")
  - [JavaScript Object Notation](https://ja.wikipedia.org/wiki/JavaScript_Object_Notation "wikilink") (JSON) - JavaScriptにおけるオブジェクトの記法をベースとした軽量な[データ記述言語](https://ja.wikipedia.org/wiki/データ記述言語 "wikilink")。
  - [JSONP](https://ja.wikipedia.org/wiki/JSONP "wikilink")
  - [ブックマークレット](https://ja.wikipedia.org/wiki/ブックマークレット "wikilink")
  - [VBScript](https://ja.wikipedia.org/wiki/VBScript "wikilink")
  - [ActiveX](https://ja.wikipedia.org/wiki/ActiveX "wikilink")
  - [:Category:JavaScriptを生成する言語も参照](https://ja.wikipedia.org/wiki/Category:JavaScriptを生成する言語 "wikilink")。

## 外部リンク

  - 英語
      - [Standard ECMA-262](https://www.ecma-international.org/publications/standards/Ecma-262.htm)
      - [JavaScript - MDC](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
  - 日本語
      - [JScript](https://msdn.microsoft.com/ja-jp/library/cc427807.aspx) - Microsoft
      - [JavaScript - MDC](https://developer.mozilla.org/ja/docs/Web/JavaScript) - Mozilla

[Category:JavaScript](https://ja.wikipedia.org/wiki/Category:JavaScript "wikilink") [Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink") [Category:ウェブ開発](https://ja.wikipedia.org/wiki/Category:ウェブ開発 "wikilink") [Category:ウェブサイトの構成](https://ja.wikipedia.org/wiki/Category:ウェブサイトの構成 "wikilink")

1.  JavaScript 第5版（[オライリー・ジャパン](https://ja.wikipedia.org/wiki/オライリー・ジャパン "wikilink")、2007）P2。
2.  [ECMA-262 第5版 2.Conformance](https://www.ecma-international.org/ecma-262/5.1/index.html#sec-2)
3.  新しい（ES2015以降）JavaScriptではクラスの構文によりプロトタイプを意識せずに[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")プログラミングをすることが可能になったが、言語設計は[プロトタイプベース](https://ja.wikipedia.org/wiki/プロトタイプベース "wikilink")の設計を維持している。
4.
5.
6.  ECMA 262, ISO/IEC 16262, JIS X 3060
7.
8.  [WebExtensions](https://developer.mozilla.org/ja/Add-ons/WebExtensions), [Browser Extensions](https://browserext.github.io/browserext/)
9.  [ECMAScript® 2017 Language Specification (ECMA-262, 8th edition, June 2017)](https://www.ecma-international.org/ecma-262/8.0/index.html) Introduction
10.
11. [JavaScript 2.0はECMAScript 3.1ベースに、ECMAScript 4は譲歩](https://news.mynavi.jp/news/2008/08/18/027/index.html) - マイコミジャーナル
12. [Mozilla における ECMAScript 5 のサポート](https://developer.mozilla.org/ja/docs/Web/JavaScript/ECMAScript_5_support_in_Mozilla)
13.
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