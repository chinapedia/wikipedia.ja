> この記事は[JavaC++](https://ja.wikipedia.org/wiki/JavaC++)から翻訳されています。


**JavaとC++の比較**（ジャバとシープラスプラスのひかく）の記事では、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")と[C++](../Page/C++.md "wikilink")の比較について説明する。

## 設計思想

C++とJavaとの違いは、それら言語の歴史から辿ることができる。

  - **C++**は[C言語](../Page/C言語.md "wikilink")の派生規格であり、[手続き型プログラミング](../Page/手続き型プログラミング.md "wikilink")言語に[クラス](../Page/クラス_\(コンピュータ\).md "wikilink")（抽象データ型）を導入し、[静的型付け](https://ja.wikipedia.org/wiki/静的型付け "wikilink")[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")を実現するために開発された。C言語の設計思想を維持・継承し、C言語の利点（[機械語](../Page/機械語.md "wikilink")や[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")に準ずる高速性やハードウェア操作性など）を一切損なわないようにしているため、他のオブジェクト指向言語に比べてコードの実行効率や柔軟性を重視している反面、安全性は犠牲になっている。
  - **Java**は当初、[組み込みシステム](../Page/組み込みシステム.md "wikilink")上で[ネットワークコンピューティング](https://ja.wikipedia.org/wiki/ネットワークコンピューティング "wikilink")に対応 (support) するために開発された。Javaは[移植性](../Page/移植性.md "wikilink")があり、[セキュアであり](../Page/コンピュータセキュリティ.md "wikilink")、[マルチスレッド対応であり](../Page/スレッド_\(コンピュータ\).md "wikilink")、[分散であり](../Page/分散コンピューティング.md "wikilink")、そしてC++よりも単純 (simple) になるように設計された。Javaの文法はC/C++[プログラマ](../Page/プログラマ.md "wikilink")に馴染みやすいものが選ばれたが、C/C++との直接的な互換性は維持されていない。

C++とJavaは開発の目的が異なるため、両者の[方針と](../Page/法則.md "wikilink")[トレードオフ](../Page/トレードオフ.md "wikilink")に違いが生じている。

  -
    {| class="wikitable"

\! **C++** \!\! **Java** |- | ネイティブコード || マネージコード |- | Cの (部分的な) 上位互換 || C/C++との互換性はない |- | プログラマを信頼する || プログラマを守る |- | ハードウェアに近い低レベル（下位レベル）機能を操作できる || メモリを抽象化した型やオブジェクトを通してのみアクセス可能 |- | 簡潔な表現 || 明確な表現 |- | 明示的な型破壊を許可 || [型安全性](https://ja.wikipedia.org/wiki/型安全性 "wikilink") |- | [マルチパラダイム](https://ja.wikipedia.org/wiki/マルチパラダイムプログラミング言語 "wikilink")（[手続き型](../Page/手続き型プログラミング.md "wikilink")、[オブジェクト指向](../Page/オブジェクト指向プログラミング.md "wikilink")、[総称型](../Page/ジェネリックプログラミング.md "wikilink")、[関数型](https://ja.wikipedia.org/wiki/関数型プログラミング "wikilink")） || オブジェクト指向、総称型、関数型 |- | [演算子](../Page/演算子.md "wikilink")[多重定義](../Page/多重定義.md "wikilink") || 演算子の効果は[不変](../Page/イミュータブル.md "wikilink") |- | 限られた範囲の標準ライブラリ || （GUI、ネットワーク、マルチスレッドを含む）機能豊富で容易に使用できる標準ライブラリ |- | 組み込み、パーソナルコンピュータ、ワークステーション|| 業務システム（Webフロントエンド、Webバックエンド）、携帯端末 |}

C言語とC++は相互運用性が確保されており、C++からCのライブラリ（[関数群](../Page/サブルーチン.md "wikilink")）を直接利用することが可能になっている。なお、2018年現在のC/C++最新規格はそれぞれ[C11および](https://ja.wikipedia.org/wiki/C11_\(C言語\) "wikilink")[C++17](https://ja.wikipedia.org/wiki/C++17 "wikilink")だが、双方に独自の追加仕様が重ねられており、C言語に対する完全な上位互換性はなくなっている。ただし、互いの差異を埋めて互換性を向上するための機能追加もなされている。

また、JavaはC/C++との互換性はないが、[Scala](../Page/Scala.md "wikilink")や[Kotlin](https://ja.wikipedia.org/wiki/Kotlin "wikilink")、[Groovy](../Page/Groovy.md "wikilink")といった後発の[Java仮想マシン](../Page/Java仮想マシン.md "wikilink") (JVM) ベースの[ABI互換言語との間で相互運用が可能になっている](../Page/Application_Binary_Interface.md "wikilink")。

## 言語の特徴

### 文法

  - Java[文法](../Page/文法.md "wikilink")はシンプルな[LALRパーサによって解析できる](../Page/LALR法.md "wikilink")[文脈自由文法](../Page/文脈自由文法.md "wikilink")である。C++の構文解析は、それよりも複雑である。例えば、`Foo<1>(3);`は、Fooが変数であれば比較シーケンスであるが、Fooが[クラスのテンプレート名であれば](../Page/クラス_\(コンピュータ\).md "wikilink")[オブジェクトを生成する](../Page/オブジェクト_\(プログラミング\).md "wikilink")。
  - C++では[名前空間](../Page/名前空間.md "wikilink")レベルの定数、[変数](../Page/変数_\(プログラミング\).md "wikilink")、[関数が認められている](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")。Javaでは、宣言は[クラスや](../Page/クラス_\(コンピュータ\).md "wikilink")[インタフェースの中に書かなければならない](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")。
  - C++の[`const`](https://ja.wikipedia.org/wiki/const "wikilink")は、「論理的に読み取り専用データである」ことを示す。Javaの`final`は、「変数が再び割り当てられない」ことを示す。`const int`と`final int`など、基本型にとってはこれらは概ね等価であるが、C++では変数および定数の宣言時初期化もしくは定義時初期化が必要であるのに対し、Javaでは初期化が一回だけ実行されるという条件が満たされればよい。また、C++のポインタ自身に対する`const`修飾は、Javaの参照に対する`final`修飾と同じ意味を持つ。
  - [C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")では、コンパイル時に値が決まる定数式 (constant expression) すなわち[リテラル](../Page/リテラル.md "wikilink")を表す`constexpr`修飾子をサポートするようになった\[1\]。Javaでは通例`static final`[フィールドで定数を定義する](../Page/フィールド_\(計算機科学\).md "wikilink")。

<table>
<thead>
<tr class="header">
<th><p><strong>C++</strong></p></th>
<th><p><strong>Java</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><div class="sourceCode" id="cb1"><pre class="sourceCode cpp"><code class="sourceCode cpp"><span id="cb1-1"><a href="#cb1-1"></a><span class="at">const</span> <span class="dt">int</span> n = <span class="dv">100</span>; <span class="co">// 値型。</span></span>
<span id="cb1-2"><a href="#cb1-2"></a>n = <span class="dv">0</span>; <span class="co">// 誤り。</span></span>
<span id="cb1-3"><a href="#cb1-3"></a><span class="kw">struct</span> Rectangle { <span class="dt">int</span> x, y, width, height; };</span>
<span id="cb1-4"><a href="#cb1-4"></a>Rectangle *<span class="at">const</span> p = <span class="kw">new</span> Rectangle(); <span class="co">// ポインタ自身を変更不能とする。</span></span>
<span id="cb1-5"><a href="#cb1-5"></a>p = <span class="kw">new</span> Rectangle(); <span class="co">// 誤り。</span></span>
<span id="cb1-6"><a href="#cb1-6"></a>p-&gt;x = <span class="dv">5</span>; <span class="co">// 正しい。p は依然として同じ Rectangle を参照している。</span></span>
<span id="cb1-7"><a href="#cb1-7"></a><span class="kw">delete</span> p;</span></code></pre></div>
<div class="sourceCode" id="cb2"><pre class="sourceCode cpp"><code class="sourceCode cpp"><span id="cb2-1"><a href="#cb2-1"></a><span class="at">const</span> Rectangle* p = <span class="kw">new</span> Rectangle(); <span class="co">// ポインタの参照先を変更不能とする。</span></span>
<span id="cb2-2"><a href="#cb2-2"></a><span class="kw">delete</span> p;</span>
<span id="cb2-3"><a href="#cb2-3"></a>p = <span class="kw">new</span> Rectangle(); <span class="co">// 正しい。</span></span>
<span id="cb2-4"><a href="#cb2-4"></a>p-&gt;x = <span class="dv">5</span>; <span class="co">// 誤り。</span></span>
<span id="cb2-5"><a href="#cb2-5"></a><span class="at">const</span> Rectangle&amp; r = *p;</span>
<span id="cb2-6"><a href="#cb2-6"></a>r = Rectangle(); <span class="co">// 誤り。</span></span>
<span id="cb2-7"><a href="#cb2-7"></a>r.x = <span class="dv">5</span>; <span class="co">// 誤り。</span></span>
<span id="cb2-8"><a href="#cb2-8"></a><span class="kw">delete</span> p;</span></code></pre></div>
<div class="sourceCode" id="cb3"><pre class="sourceCode cpp"><code class="sourceCode cpp"><span id="cb3-1"><a href="#cb3-1"></a><span class="at">const</span> Rectangle r = Rectangle(); <span class="co">// 値型。</span></span>
<span id="cb3-2"><a href="#cb3-2"></a>r = Rectangle(); <span class="co">// 誤り。</span></span>
<span id="cb3-3"><a href="#cb3-3"></a>r.x = <span class="dv">5</span>; <span class="co">// 誤り。r は Rectangle 型の定数。</span></span></code></pre></div></td>
<td><div class="sourceCode" id="cb4"><pre class="sourceCode java"><code class="sourceCode java"><span id="cb4-1"><a href="#cb4-1"></a><span class="dt">final</span> <span class="dt">int</span> n = <span class="dv">100</span>; <span class="co">// プリミティブ型。</span></span>
<span id="cb4-2"><a href="#cb4-2"></a>n = <span class="dv">0</span>; <span class="co">// 誤り。</span></span>
<span id="cb4-3"><a href="#cb4-3"></a><span class="kw">class</span> <span class="bu">Rectangle</span> { <span class="dt">int</span> x, y, width, height; };</span>
<span id="cb4-4"><a href="#cb4-4"></a><span class="dt">final</span> <span class="bu">Rectangle</span> r = <span class="kw">new</span> <span class="bu">Rectangle</span>(); <span class="co">// 参照型。</span></span>
<span id="cb4-5"><a href="#cb4-5"></a>r = <span class="kw">new</span> <span class="bu">Rectangle</span>(); <span class="co">// 誤り。</span></span>
<span id="cb4-6"><a href="#cb4-6"></a>r.<span class="fu">x</span> = <span class="dv">5</span>; <span class="co">// 正しい。r は依然として同じ Rectangle を参照している。</span></span></code></pre></div>
<div class="sourceCode" id="cb5"><pre class="sourceCode java"><code class="sourceCode java"><span id="cb5-1"><a href="#cb5-1"></a><span class="dt">final</span> <span class="dt">int</span> n;</span>
<span id="cb5-2"><a href="#cb5-2"></a><span class="dt">final</span> <span class="bu">Rectangle</span> r;</span>
<span id="cb5-3"><a href="#cb5-3"></a>n = <span class="dv">100</span>; <span class="co">// 正しい。</span></span>
<span id="cb5-4"><a href="#cb5-4"></a>r = <span class="kw">new</span> <span class="bu">Rectangle</span>(); <span class="co">// 正しい。</span></span></code></pre></div></td>
</tr>
</tbody>
</table>

  - C++においてconst修飾されたメンバ関数は、関数内でメンバ変数を変更することができなくなる。Javaには相当機能はない。
  - Javaにおいてfinal修飾されたメソッドは派生クラスで[オーバーライド](../Page/オーバーライド.md "wikilink")できなくなる。また、final修飾されたクラスは派生クラスを定義できなくなる。なお、[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")ではJavaのようにメンバ関数のオーバーライドや派生クラスの定義を禁止するfinal修飾子が追加された。
  - C++は[goto文](https://ja.wikipedia.org/wiki/goto文 "wikilink")をサポートする。Javaはサポートしないが、[ラベル付break文と](https://ja.wikipedia.org/wiki/break文 "wikilink")[ラベル付continue文で](https://ja.wikipedia.org/wiki/continue文 "wikilink")、構造上やや`goto`ライクな機能を提供する。実際には、Javaは、コードを読みやすくするため、[構造化制御フローを強要する](../Page/制御構造.md "wikilink")。
  - C++はJavaが持たないやや低レベルな機能を提供する。C++には、特有のメモリ記憶位置や低レベル[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")コンポーネントを書くために必要なタスクを操るのに役立つ[ポインタがある](../Page/ポインタ_\(プログラミング\).md "wikilink")。同様にして、多くのC++コンパイラは[インラインアセンブラ](https://ja.wikipedia.org/wiki/インラインアセンブラ "wikilink")をサポートする。Javaでは、そのようなコードは全て外部ライブラリに配置し、[Java Native Interfaceを通してアクセスしなければならない](../Page/Java_Native_Interface.md "wikilink")。そのため、呼び出しのたびに、大きなオーバーヘッドが発生する。

### 意味論

  - C++は[Cとの互換性を保つため組込型の暗黙な](../Page/C言語.md "wikilink")[型変換](../Page/型変換.md "wikilink")をある程度許可しているが、大抵のコンパイラでは警告を出す。また、[複合型の暗黙型変換も定義できる](../Page/データ型.md "wikilink")。一方、Javaでは暗黙な変換としてネイティブ型の[精度が大きくなる型変換](../Page/精度_\(算術\).md "wikilink")（[拡張変換](https://ja.wikipedia.org/wiki/拡張変換 "wikilink")）のみを許可する。他の変換は文法的に明示的な[キャストを要求する](../Page/型変換.md "wikilink")。
      - この影響はJavaとC++双方にある条件式（`if`、`while`と`for`の脱出条件）にも現れる。条件式の型はbooleanであることが期待されるが、intからbooleanへの精度が狭められる暗黙的型変換（[縮小変換](https://ja.wikipedia.org/wiki/縮小変換 "wikilink")）が無いため、`if (a = 5)`のようなコードは、Javaではコンパイルエラーになる。これは、`if (a == 5)`の[ミスタイプに対する対策となるが](../Page/誤植.md "wikilink")、`if (x)`のようなコードをC++からJavaへ移植する際には型変換を明示することになる分、冗長になってしまう。
  - 関数の引数を渡すとき、C++は[参照渡し](https://ja.wikipedia.org/wiki/参照渡し "wikilink")と[値渡し](https://ja.wikipedia.org/wiki/値渡し "wikilink")両方をサポートする。Javaではすべての引数は値渡しであるが、オブジェクト（非[プリミティブ変数](../Page/プリミティブ型.md "wikilink")）の引数は[参照になり](../Page/参照_\(情報工学\).md "wikilink")、これは間接参照が言語に備わっていることを意味する。
  - Javaのプリミティブ型は大きさと値の範囲が指定されている。一方、C++の組み込み型は最小限度が定められているものの、正確な大きさは定められておらず、環境によって異なる。また同じコンパイラでもバージョンが違えば型の大きさが異なることもあるし、コンパイラの設定で変更可能な場合もある。C++で値の範囲が指定されていないとは、仮に同じ16ビット整数だとしても、ある環境では[2の補数](../Page/2の補数.md "wikilink")で\[-32768, 32767\]、別の環境では[1の補数](https://ja.wikipedia.org/wiki/1の補数 "wikilink")で\[-32767, 32767\]の範囲になるという例があるということである。[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")ではサイズと内部表現が規定された整数型（`std::int32_t`など）がオプションとして追加された。
      - Javaの[文字型](https://ja.wikipedia.org/wiki/文字型 "wikilink")`char`は、内部表現が[UTF-16](../Page/UTF-16.md "wikilink")であることが規定されている。[文字列](../Page/文字列.md "wikilink")を表現するクラスとして、が用意されている。一方、C++の文字型には`char`と`wchar_t`（[ワイド文字](../Page/ワイド文字.md "wikilink")）の2種類が存在し、それぞれの文字列クラスとして`std::string`および`std::wstring`が定義されているが、文字型の幅（ビット数）や内部表現は[プラットフォームに依存する](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。規定されているのは`char`のサイズが1バイト (`sizeof(char) == 1`) ということのみである。さらに、1バイトのビット数が規定されておらず、8ビット以上であればよい、という制約しかない。例えば、`char`が[シングルバイト文字](https://ja.wikipedia.org/wiki/シングルバイト文字 "wikilink")であったとしても、[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")であるとはかぎらないし、[マルチバイト文字](../Page/マルチバイト文字.md "wikilink")であったとしても、日本語環境で[Shift_JIS](../Page/Shift_JIS.md "wikilink")あるいは[EUC-JP](../Page/EUC-JP.md "wikilink")が使われたり、中国語環境で[GB 2312あるいは](../Page/GB_2312.md "wikilink")[Big5](../Page/Big5.md "wikilink")が使われたり、もしくは[UTF-8](../Page/UTF-8.md "wikilink")であったりしてもかまわない。また、`wchar_t`の内部表現は、[UTF-16](../Page/UTF-16.md "wikilink")もしくは[UTF-32](../Page/UTF-32.md "wikilink")であってもかまわないし、あるいは[Unicode](../Page/Unicode.md "wikilink")と無関係の内部表現であってもかまわない。[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")では[UTF-16](../Page/UTF-16.md "wikilink")/[UTF-32](../Page/UTF-32.md "wikilink")専用の文字型`char16_t`/`char32_t`と文字列クラス`std::u16string`/`std::u32string`が追加された。
      - Javaの文字列リテラルはString型のオブジェクトである。C++の文字列リテラルは[ヌル終端文字列](https://ja.wikipedia.org/wiki/ヌル終端文字列 "wikilink")をぴったり格納する固定長配列型である。
  - C++の浮動小数点数の丸め誤差と精度と演算はプラットフォームに依存する。Javaは異なるプラットフォームでの一貫した結果を保証する[高精度浮動小数点モデルを提供しているが](https://ja.wikipedia.org/wiki/strictfp "wikilink")、通常は最適な浮動小数点演算性能を得るためにより大雑把な演算モードが使われる。
  - C++では[ポインタを使ってメモリアドレスを直接操作できる](../Page/ポインタ_\(プログラミング\).md "wikilink")。Javaはメモリアドレスを直接操作できるポインタを持っていない（オブジェクトの参照と配列参照だけはポインタを持っているが、どちらもメモリアドレスの直接アクセスを許可しない）。C++ではポインタへのポインタを定義できるが、Javaではオブジェクトアクセスにだけ参照を用いる。
  - どちらの言語も配列は固定の長さをもつ。C++の配列はメモリ空間上のオブジェクトの連続であり、配列自身をオブジェクトのように扱うことはできない（[第一級オブジェクト](../Page/第一級オブジェクト.md "wikilink")ではない）。通例、C言語のように配列先頭要素へのポインタを用いて配列の受け渡しを行うが、C++ではサイズの指定された固定長配列への参照を定義することもできる。配列範囲外アクセスはチェックされない。なお、[構造体](../Page/構造体.md "wikilink")あるいはクラスでラップするか、[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")で追加された標準ライブラリに含まれる`std::array`を用いることで、固定長配列を第一級オブジェクトとして扱うことができる。Javaの配列は第一級オブジェクトであるが、配列の一部分のみを参照するサブ配列は定義できず、インデックス範囲を別途指定する必要がある。また、配列範囲外アクセスのチェックが強制される。
  - C++では[関数へのポインタ](../Page/関数へのポインタ.md "wikilink")（あるいは関数への参照）によって、関数あるいはメンバ関数を間接参照することができる。また、ポインタによって[関数オブジェクト](https://ja.wikipedia.org/wiki/関数オブジェクト "wikilink")を指す方法もある。Java 7以前では代替方法としてインタフェースを利用するしかなかったが、Java 8ではメソッド参照の機能が追加された。
  - C++ではプログラマが演算子を[多重定義](../Page/多重定義.md "wikilink")できる（[利用者定義演算子](https://ja.wikipedia.org/wiki/利用者定義演算子 "wikilink")）。Javaは演算子多重定義をサポートしない。文字列型に対してのみ、[文字列連結](https://ja.wikipedia.org/wiki/文字列連結 "wikilink")が可能な演算子`+`と`+=`が予め用意されているだけである。
  - Javaは[リフレクションや任意に新しいコードを](../Page/リフレクション_\(情報工学\).md "wikilink")[動的ロードする機能をサポートする標準](../Page/動的リンク.md "wikilink")[APIを持つ](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。
  - Javaは1.5以降で[ジェネリクスをサポートする](../Page/ジェネリックプログラミング.md "wikilink")。C++は[テンプレートによりジェネリックプログラミングをサポートする](../Page/テンプレート_\(プログラミング\).md "wikilink")。
  - JavaとC++はいずれも、ネイティブ型（これらも"基本型"または"組込型"として知られる）とユーザー定義型（これも"複合型"として知られる）を区別する。Javaでは、ネイティブ型は値としての意味しかなく、複合型は参照としての意味だけを持つ。C++では、すべての型が値としての意味を持つが、任意の型の参照を作ることが可能である。
  - C++は任意のクラスの[多重継承](https://ja.wikipedia.org/wiki/多重継承 "wikilink")をサポートする。また、状態の多重継承にまつわる問題を回避するための機構として、[仮想継承](https://ja.wikipedia.org/wiki/仮想継承 "wikilink")をサポートする。Javaは型の多重継承を[インタフェースによりサポートするが](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")、実装は単一継承のみをサポートする。Javaでは、サブクラスはただ1つのスーパークラスからのみ派生することができるが、クラスは複数のインタフェースを実装することができる。なお、Java 8ではインタフェースのデフォルトメソッドにより、実装の多重継承をサポートするようになったが、状態の多重継承は依然としてサポートしない。
  - Javaはインタフェースとクラスを明確に区別している。C++では、純粋仮想関数（抽象メソッドにあたる）を並べたクラスでインタフェースを表現し、複数のインタフェースの実装は多重継承によって模倣される。
  - Javaは[マルチスレッドをサポートした標準ライブラリと言語機能を持つ](../Page/スレッド_\(コンピュータ\).md "wikilink")。`synchronized` [Java予約語はマルチスレッドアプリケーションをサポートするシンプルでセキュアな](https://ja.wikipedia.org/wiki/予約語_\(Java\) "wikilink")[相互排他ロック（Mutex）を提供するが](../Page/ミューテックス.md "wikilink")、synchronized セクションは[LIFO](https://ja.wikipedia.org/wiki/LIFO "wikilink")オーダーで残されなければならない。Java 1.5では[並行プログラミング](https://ja.wikipedia.org/wiki/並行プログラミング "wikilink")のためのライブラリが強化され、クラスをはじめとする、柔軟なMutexロックメカニズムを提供するための明示的な同期オブジェクトなどもサポートするようになった。一方、C++では長らくスレッドが標準化されていなかったため、プラットフォームごとのスレッド機能を使うか、[Boost](https://ja.wikipedia.org/wiki/Boost "wikilink") C++ライブラリなどを利用する必要があったが、[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")でスレッドが標準化された。

### リソース管理

  - Javaは自動[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")を必要とする。C++のメモリ管理は普通、手動で行われるか、[スマートポインタ](https://ja.wikipedia.org/wiki/スマートポインタ "wikilink")を通して行われる。C++でガベージコレクションを実装することも不可能ではないが、標準規格で要求されているわけではなく、実際には滅多に使われない。また、C++ではオブジェクトを再配置できないが、一般にオブジェクトの再配置が可能であれば、明示に解放するスタイルより空間と時間効率が良くなることが知られている。
      - C++でのスマートポインタは、主に[参照カウント](../Page/参照カウント.md "wikilink")が用いられる。その場合、循環参照の注意が必要という欠点がある。
  - メモリ割り当ては、C++では任意に可能だが、Javaはオブジェクトインスタンス化を通してのみ可能である。Javaでは、バイト配列を作ることで任意のブロック割り当てを再現できる。もっとも、Javaの[配列](../Page/配列.md "wikilink")もオブジェクトである。
  - JavaとC++はリソース管理に異なる手法を用いる。Javaは主にガベージコレクションに頼り、メモリの再利用だけができ、他のリソースは最後まで回収されないかもしれない。だが、C++は主に[RAII](../Page/RAII.md "wikilink") (Resource Acquisition Is Initialization) というイディオムに頼る。これは2つの言語間の以下のような様々な違いに現れている。
      - C++では、複合型も組込型同様スタックに割り当てられ、[スコープ](../Page/スコープ.md "wikilink")から外れると共に破棄される。Javaでは、複合型は常に[ヒープ](../Page/ヒープ.md "wikilink")に割り当てられ、ガベージコレクタによって回収される（これはあくまで概念上の話で、実装上は[エスケープ解析](https://ja.wikipedia.org/wiki/エスケープ解析 "wikilink")最適化でスタックにオブジェクトを割り当てる仮想マシンもある）。
      - C++は[デストラクタ](../Page/デストラクタ.md "wikilink")を持っているが、Javaは[ファイナライザ](https://ja.wikipedia.org/wiki/ファイナライザ "wikilink")を持っている。双方はオブジェクトの解放時に優先的に呼び出されるが、それらは重大性が異なる。
          - C++オブジェクトのデストラクタは、オブジェクトが解放されるときに必ず呼び出される（ようにコンパイラは実装しなければならない）。例外が投げられたときでも、スタック上のオブジェクトは、スタックの巻き戻し（アンワインド）に伴ってデストラクタが呼ばれる。また、デストラクタは定義さえすれば、利用する側に特別な記述は不要である。このことを利用して確実なリソースの解放を行うのが広義のRAIIである。
          - Javaでは、オブジェクト解放はガベージコレクタによって暗黙のうちに解放される。Javaオブジェクトのファイナライザは、最後にアクセスされた後と、実際に解放される前に、ときどき[非同期](https://ja.wikipedia.org/wiki/非同期 "wikilink")に呼び出されるが、決して何も起こらないかも知れない。ファイナライザを要求するオブジェクトはごくわずかにすぎない。ファイナライザは解放状態を優先するオブジェクトの多少の[クリーンナップ](../Page/クリーンナップ.md "wikilink")を保証しなければならないオブジェクトによって要求されるだけであり、だいたいはJVM外のリソースへ放出される。Javaでは安全な同期によるリソース解放は、try/finally文を構築して明示的に行われなければならない。
      - C++では、時として[dangling pointer](https://ja.wikipedia.org/wiki/dangling_pointer "wikilink")（破棄されたオブジェクトを参照するポインタ）が存在してしまう。dangling pointerを間接参照するときは、基本的にプログラムのバグである。Javaでは、ガベージコレクタは参照されているオブジェクトは解放しない。
      - C++では初期化されていない[プリミティブなオブジェクトを持つことが可能である](../Page/プリミティブ型.md "wikilink")。Javaでは、初期化が強制される。
      - C++では、領域を割り当てられたが到達不能であるオブジェクトが発生してしまうことがある。[到達不能オブジェクト](https://ja.wikipedia.org/wiki/到達不能オブジェクト "wikilink")とは、それへの到達可能な参照が全く存在しないオブジェクトのことである。到達不能オブジェクトは解放(破棄)することができず、[メモリリーク](../Page/メモリリーク.md "wikilink")を引き起こす。それとは対照的に、Javaではオブジェクトは、それがユーザープログラムによって到達不可能になる「までに」ガベージコレクタによって解放される (注: 異なる到達可能性の「強さ」を考慮に入れた、Javaのガベージコレクタとともに働く、「[弱い参照](../Page/弱い参照.md "wikilink")」がサポートされている)。
      - Javaでは非メモリリソースをリークしないように注意深く解放コードを逐一書く必要がある（ただしJava 7のtry-with-resources文により、ある程度緩和されている）。一方でC++では、前述のRAIIによってリークしにくい例外安全なコードを書きやすくなっている。

### ライブラリ

JavaはC++と比べ[標準ライブラリ](https://ja.wikipedia.org/wiki/標準ライブラリ "wikilink")の提供する範囲が広い。[標準C++ライブラリ](../Page/標準C++ライブラリ.md "wikilink")は[文字列](../Page/文字列.md "wikilink")、[コンテナ](../Page/コンテナ_\(データ型\).md "wikilink")、[IOストリームのような比較的一般的な目的のコンポーネントだけを提供する](../Page/ストリーム_\(プログラミング\).md "wikilink")。[Java標準ライブラリは](../Page/Java_Platform,_Standard_Edition.md "wikilink")[ネットワーキング](../Page/コンピュータネットワーク.md "wikilink")、[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、[XML処理](../Page/Extensible_Markup_Language.md "wikilink")、[ロギング](https://ja.wikipedia.org/wiki/ロギング "wikilink")、[データベース](../Page/データベース.md "wikilink")アクセス、[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")やそのほか様々な領域のコンポーネントを含む。このような機能は、C++では[サードパーティー](../Page/サードパーティー.md "wikilink")製のライブラリやOS固有のAPIによって実現されていることが多いが、どんな環境でも用意されているとは限らない。

C++はCに対する部分的な上位互換性を持つため、（多くの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の[APIのような](../Page/アプリケーションプログラミングインタフェース.md "wikilink")）Cライブラリも直接使用できる。Javaでは、そのような環境固有のライブラリで提供される機能の多くが、[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")でリッチな標準ライブラリで提供される。その一方で、Javaからネイティブなオペレーティングシステムやハードウェア機能に直接アクセスするには、[Java Native Interfaceを使用する必要がある](../Page/Java_Native_Interface.md "wikilink")。

### ランタイム

  - C++は通常、[機械語](../Page/機械語.md "wikilink")に直接コンパイルされてから、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")およびCPUによって直接実行される。Javaは通常[バイトコード](../Page/バイトコード.md "wikilink")にコンパイルされてから[Java仮想マシン](../Page/Java仮想マシン.md "wikilink") (JVM) が[インタプリタ](../Page/インタプリタ.md "wikilink")でバイトコードを解釈するか、または[JITがバイトコードをマシンコードにコンパイルしつつ実行される](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")。理論上、[動的再コンパイル](https://ja.wikipedia.org/wiki/動的再コンパイル "wikilink")はどの言語でも使うことができる（しかしJavaのほうが向いている）が、現在のところ、どちらの言語でも動的に再コンパイルされることは稀である。
  - 強制によらない表現力のため、C++の多くのエラー要因（範囲外チェックされない配列アクセス、未使用ポインタ、型の不一致など）はコンパイル時または実行時の不適当なオーバーヘッド無しに信頼できるチェックを行えない。このため、低レベル[バッファオーバフロー](https://ja.wikipedia.org/wiki/バッファオーバフロー "wikilink")、[ページフォールト](../Page/ページフォールト.md "wikilink")、[セグメンテーションフォルトを導いてしまう](../Page/セグメンテーション違反.md "wikilink")。標準やサードパーティーのライブラリがそのようなエラーを避けることを助ける高水準な([動的配列](https://ja.wikipedia.org/wiki/動的配列 "wikilink")、[リスト](../Page/リスト_\(抽象データ型\).md "wikilink")、[マップのような](../Page/連想配列.md "wikilink"))抽象概念を提供している。一方、Javaではそのようなエラーは単純に起こすことも、[JVMに検出されることも無く](../Page/Java仮想マシン.md "wikilink")、[例外によってアプリケーションに報告される](../Page/例外処理.md "wikilink")。
  - Javaは、配列アクセスの[境界チェック](https://ja.wikipedia.org/wiki/境界チェック "wikilink")を行い、そして領域外にアクセスすることが判明したときに明確な振る舞い（例外の送出）を要求する。これにより、一般に実行が低速になる代わりに不安定さの源が除去される。ただし、[コンパイラ解析](https://ja.wikipedia.org/wiki/コンパイラ解析 "wikilink")で不必要な境界チェックが消去される場合もある。C++はネイティブな配列の配列外アクセスの振る舞いを要求しないため、通常は境界チェックしないのが一般的である。ただし`std::vector`のようなC++標準ライブラリでは、`at()`メンバ関数の使用という形で、境界チェック付きアクセスを任意に選択できる。要約すると、Javaの配列は「常に安全で、厳しく強いられる、可能な限り高速」だがC++のネイティブ配列は「常に高速、完全に強制されない、潜在的に危険」ということである。

### その他

  - JavaとC++では多くのソースファイルでコードを分割するために異なる方法を使用する。Javaはすべてのプログラム定義でファイル名とパスが影響する[パッケージシステムを使用する](../Page/パッケージ_\(Java\).md "wikilink")。Javaでは、コンパイラは実行可能[クラスファイルをインポートする](https://ja.wikipedia.org/wiki/Javaクラスファイル "wikilink")。C++はソースファイル間で宣言を分割する[ヘッダファイル](../Page/ヘッダファイル.md "wikilink")の[ソースコード](../Page/ソースコード.md "wikilink")包含システムおよび[名前空間](../Page/名前空間.md "wikilink")を使用する。（参考: [importとincludeの比較](https://ja.wikipedia.org/wiki/importとincludeの比較 "wikilink")）
  - コンパイルされた[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")ファイルは通常、C++コンパイラの出力する機械語のコードファイルよりも小さい。第一に、[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")は通常、ネイティブな[機械語](../Page/機械語.md "wikilink")よりもコンパクトである。第二に、C++のテンプレートやマクロが類似コードの重複を発生させやすいことが挙げられる。第三に、Javaは常に標準ライブラリを[動的リンクするため](https://ja.wikipedia.org/wiki/ライブラリ#動的リンク "wikilink")、標準ライブラリのコードを出力に含まないということが挙げられる。反面、Javaバイトコードを翻訳実行する環境（JVMやJIT）が要求される。
  - C++コンパイラは、Javaにはない、言葉通りの[プリプロセッシング](../Page/プリプロセッサ.md "wikilink")（前処理）の段階があることが特徴的である。これを用いるために、Javaユーザーの中には、ビルドプロセスにプリプロセッサを付加する者がいる。
  - 双方の言語は、[配列](../Page/配列.md "wikilink")が固定サイズである。Javaでは、配列は第一級オブジェクトであるが、C++では配列はベースとなるオブジェクトの連続した領域であり、最初の要素と随意的な配列の長さをポインタを使って参照しているに過ぎない。Javaでは、配列は境界チェックされ、長さもわかっているが、C++では配列を連続した領域として扱うだけである。C++とJava双方は、リサイズ、サイズ保存できるコンテナクラス (それぞれ、**std::vector** と または) を提供している。
  - Javaの除算と[剰余演算子は](../Page/除法.md "wikilink")0を切り捨てるよう正しく定義されている。C++は、これらの演算子が0を切り捨てるか「マイナス無限大に切り捨てる」かを明確に指定しない。Javaでは、`-3 / 2`は常に`-1`となる。一方、C++ではプラットフォームに依存し、-1を返すかも知れないし-2を返すかも知れない。[C99](../Page/C99.md "wikilink")および[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")はJavaと同じように除算の仕様を定義しており、すべてのaとb (b \!= 0) で`(a/b)*b + (a%b) == a`を保証する。古いC/C++規格にこの保証がない理由は、仮にCPUの除算命令がこのような定義でなかったとしても、C/C++の除算を直接CPUの除算命令にコンパイルできるようにするためである。ただし、古いC/C++でも標準ライブラリの`div()`関数 (\<stdlib.h\>/<cstdlib>) を用いれば常に`-3 / 2`の商として`-1`という結果を得られる。

## パフォーマンス

このセクションでは、WindowsやLinuxのような一般的なOSでのC++とJava相互の演算パフォーマンスを比較する。

Javaの初期バージョンは、C++のような静的コンパイルされる言語に比べ著しく性能が低かった。これは、C++ではソースコードはハードウェアが直接に解釈できる機械語にコンパイルされるのに対し、Javaでは共通の（ハードウェアに依存しない）仮想機械語であるJavaバイトコードにコンパイルされ、それをJava仮想マシンがインタプリタ的に実行していたからである。例として、

<table>
<thead>
<tr class="header">
<th><p>Java/C++構文</p></th>
<th><p>C++が生成したコード</p></th>
<th><p>Javaが生成したコード</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>vector[i]++;</p></td>
<td><pre><code>mov edx,[ebp+4h]
mov eax,[ebp+1Ch]
inc dword ptr [edx+eax*4]</code></pre></td>
<td><pre><code>aload_1
iload_2
dup2
iaload
iconst_1
iadd
iastore</code></pre></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

のように、ソースコードレベルでは同様な命令でも、Javaバイトコードの方がネイティブな機械語よりも長くなる傾向にある (C++によるコードでは、3行目でロード、インクリメント、保存が1命令で行われており、短く済んでいる)。

しかし、Javaは長期稼働するサーバやデスクトップのために[ジャストインタイム(JIT)](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink") コンパイラテクノロジを発展させ、それがC++との性能差を縮めるであろうと言われている。JITコンパイルとは、Javaバイトコードをインタプリタ的に実行するのではなく、実行時にネイティブな機械語にコンパイルしてから実行する方式である。

以下は、JavaはC++よりも高速であるという研究\[2\]の主張の一部である。

  - CおよびC++では、「なんでも指せる」というポインタの性質が最適化を難しくしている（ただしこの問題は[C99](../Page/C99.md "wikilink")のrestrictキーワードによって回避できる）。
  - Javaでは新たに確保されたメモリが[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")によって物理的に連続した領域に集められるので、アクセスする際に[キャッシュミスが起こりにくい](../Page/キャッシュメモリ.md "wikilink")。
  - 実行時コンパイルはそれがどのプロセッサの上で実行されるか、どのコードを実行するかが解っているため、各CPUに特化したコードを生成したり、高い[分岐予測](../Page/分岐予測.md "wikilink")精度を実現したりできる（[ホットスポット](../Page/HotSpot.md "wikilink")）。

一般的に、Javaは、メモリ確保やファイルI/Oのような演算においてはC++より性能がよいが、算術演算や三角関数計算ではC++の方が優れた徴候を示す。\[3\] 数値演算について述べると、Javaは新しいバージョンで大きく進歩しているものの、浮動小数点数を様々なプラットフォームで再現するためのオーバーヘッド等により、未だにC++やFortranより遅い\[4\]。

## 脚注

## 外部リンク

  - [Object Oriented Memory Management: Java vs. C++](http://task3.cc/98/object-oriented-memory-management)
  - [How Java Differs from C](http://www.ora.com/catalog/javanut/excerpt/index.html#except) — excerpt from [Java in a Nutshell](https://ja.wikipedia.org/wiki/Java_in_a_Nutshell "wikilink") by [David Flanagan](https://ja.wikipedia.org/wiki/David_Flanagan "wikilink")
  - [Java vs. C++ resource management comparison](http://www.fatalmind.com/papers/java_vs_cplusplus/resource.html) - Comprehensive paper with examples
  - [Why Java Will Always Be Slower than C++](http://www.jelovic.com/articles/why_java_is_slow.htm) - "Java is high performance. By high performance we mean adequate. By adequate we mean slow." - Mr. Bunny

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink") [Category:ソフトウェアの比較](https://ja.wikipedia.org/wiki/Category:ソフトウェアの比較 "wikilink")

1.  [constexpr - cpprefjp C++日本語リファレンス](https://cpprefjp.github.io/lang/cpp11/constexpr.html)
2.  ["Performance of Java versus C++"](http://www.idiom.com/~zilla/Computer/javaCbenchmark.html) by J.P. Lewis and Ulrich Neuman, USC, Jan. 2003 (updated 2004)
3.  ["Microbenchmarking C++, C\# and Java"](http://www.ddj.com/184401976) by Thomas Bruckschlegel, Dr. Dobbs, June 17, 2005
4.  ["Java and Numerical Computing"](http://www.javagrande.org/leapforward/cacm-ron.pdf) by Ronald F. Boisvert, José Moreira, Michael Philippsen and Roldan Pozo, NIST, Dec 2000