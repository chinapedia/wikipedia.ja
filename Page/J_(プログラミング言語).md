> この記事は[J \(プログラミング言語\)](https://ja.wikipedia.org/wiki/J_\(プログラミング言語\))から翻訳されています。


**J**はプログラミング言語の一種で、正式名称はアルファベット1文字の「J」だが[C言語](../Page/C言語.md "wikilink")と同様、「J言語」と一般には呼ばれている。

## 概要

Jは[1989年](../Page/1989年.md "wikilink")、[APL](../Page/APL.md "wikilink")の提案者でもある[ケネス・アイバーソン](../Page/ケネス・アイバーソン.md "wikilink")によりAPLの後継として提案された。APLは数式の表記、特に[配列](../Page/配列.md "wikilink")の処理に優れており、多くの計算式を極めて単純に表記できる利点を持っていたが、ギリシャ文字やその他の特殊記号を使用するため、利用には[フォント](../Page/フォント.md "wikilink")の設定など特殊な環境の準備が必要があり、[可読性](../Page/可読性.md "wikilink")の低さもあって普及には至らなかった。

JはAPLの反省をふまえて、APLと同様の計算を通常の[ASCII](../Page/ASCII.md "wikilink")コードのみで使用できるようにした。この際、[ジョン・バッカス](../Page/ジョン・バッカス.md "wikilink")による[FP言語](https://ja.wikipedia.org/wiki/FP_\(プログラミング言語\) "wikilink")・というの影響を受けている（バッカスによるふたつの言語はAPLの影響を受けている）。さらにAPLにあった「作用子」による演算子の合成といった機能が、より拡張強化されている。これらの機能によりAPLのような表記の問題は解消された。しかし、 例えば、APLでは

  -

と表記するのが、Jでは

  -

となるなど、変数と演算子の区別がつきにくくなり、可読性が落ちている。

## データ型と記法（直値）

### 種類

#### 型

Jのデータ型は他の言語のような[整数](../Page/整数.md "wikilink")、[浮動小数点数](../Page/浮動小数点数.md "wikilink")、[文字列](../Page/文字列.md "wikilink")の他に[有理数](https://ja.wikipedia.org/wiki/有理数 "wikilink")や[複素数](../Page/複素数.md "wikilink")などもある。

#### 直値

以上の型の基本的な[直値](https://ja.wikipedia.org/wiki/直値 "wikilink")・記法の他、数値は任意の底（基数）nでの表記（n進法）の記法がある。

なお、以下では型と記法の識別を完全に欠いて説明しているので注意。

### 整数

整数の表記は基本的には他の言語と同じである、しかしJでは負の数はではなくを用いる。さらにを単体で使用すると「無限」として処理される。

<table>
<thead>
<tr class="header">
<th><p>式</p></th>
<th><p>評価後の値</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>（）</p></td>
</tr>
<tr class="even">
<td><p>（）</p></td>
<td><p>（）</p></td>
</tr>
</tbody>
</table>

### 浮動小数点数

浮動小数点数の表記も基本的には他の言語と同じである。ただし J では "."（ピリオド）が演算子に大きな影響を与えるため ".5" のような表記（他言語では0.5として処理される）は許されない。数字の間に "e" を入れる指数表示は他言語同様 J でも実装されている（例  → ）。

### 有理数

有理数はと表記する。（例  → を意味する）

### 複素数

複素数はと表記する。この他にも・と表記するとそれに対応する複素数を返す。

<table>
<thead>
<tr class="header">
<th><p>表記</p></th>
<th><p>意味</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
</tr>
</tbody>
</table>

### n進法

任意の底（基数）nによるn進法での数値は、という表記する。基底は小数点を含んでもかまわない。

<table>
<thead>
<tr class="header">
<th><p>表記</p></th>
<th><p>意味</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 演算子の種類

JはAPLの特殊文字を全てASCIIコードを組み合わせた[演算子](../Page/演算子.md "wikilink")として扱うため、膨大な数の演算子を持つ。具体的には演算子の後にコロンやピリオドを加えると別の演算子として扱われる。またAPL同様、演算子を[前置記法](https://ja.wikipedia.org/wiki/前置記法 "wikilink")として使う場合と[中置記法](../Page/中置記法.md "wikilink")として使う場合にかなりはっきりとした意味の違いを持たせている。

一例を以下の表で表す、Jの演算は通常は算術演算子として扱うが、[被演算子](https://ja.wikipedia.org/wiki/被演算子 "wikilink")が1または0の場合は論理演算として扱われる。

<table>
<thead>
<tr class="header">
<th><p>演算子</p></th>
<th><p>前置記法として使用する場合</p></th>
<th><p>中置記法として使用する場合</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/共役複素数" title="wikilink">共役複素数</a>を返す。</p></td>
<td><p>足し算</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>2倍にする。</p></td>
<td><p>(論理演算)<a href="../Page/否定論理和.md" title="wikilink">否定論理和</a>を返す。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><a href="../Page/複素数.md" title="wikilink">複素数</a>の実数部と虚数部を分離して<a href="https://ja.wikipedia.org/wiki/線形リスト" title="wikilink">リストの形式で返す</a>。</p></td>
<td><p><a href="../Page/最大公約数.md" title="wikilink">最大公約数</a>（論理演算の場合は<a href="../Page/論理和.md" title="wikilink">論理和</a>）を返す。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>符号（正なら 1、負なら 、零なら 0）を返す。</p></td>
<td><p>かけ算</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>2乗にする。</p></td>
<td><p>(論理演算)<a href="../Page/否定論理積.md" title="wikilink">否定論理積</a>を返す。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="../Page/複素数.md" title="wikilink">複素数</a>を<a href="https://ja.wikipedia.org/wiki/極座標" title="wikilink">極座標</a>に変更して<a href="https://ja.wikipedia.org/wiki/線形リスト" title="wikilink">リストの形式で返す</a>。</p></td>
<td><p><a href="../Page/最小公倍数.md" title="wikilink">最小公倍数</a>（論理演算の場合は<a href="../Page/論理積.md" title="wikilink">論理積</a>）を返す。</p></td>
</tr>
</tbody>
</table>

また J での計算順序は APL と同様に右の演算子が優先される。例えば  はであり、が返される。

## 演算子の合成

J では演算子を並べることにより、複数の演算子を合成することができる。2つの演算子の合成規則を「フック」、3つの演算子の合成規則を「フォーク」、4つ以上の演算子の合成規則を「トレイン」と呼ぶ。

## 脚注

## 外部リンク

  - [Jsoftware](http://jsoftware.com/) - J言語メインサイト

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")