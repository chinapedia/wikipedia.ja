> この記事は[純LISP](https://ja.wikipedia.org/wiki/純LISP)から翻訳されています。


**純**（じゅんりすぷ、）とは、コンピュータ・プログラミング言語  のうち、ごく基本的な要素だけからなる方言の一種。1960年の[ジョン・マッカーシー](../Page/ジョン・マッカーシー.md "wikilink")の論文「」で示された\[1\]。基本的な関数とプリミティブのみしかないが、その言語の[インタプリタ](../Page/インタプリタ.md "wikilink")をその言語で記述できるという性質を持っている。なお、論文とほぼ同時期に発表された、最初の  の実装である  は約90個の組み込み関数があり、純ではない。

## 概要

純LISPには2種のデータ型「アトム」と「ペア」、及び、関数はそれらを操作する5つの基本的な関数が存在する。

  - 「ペア」はデータのペアを表現する。要素 A と B からなるペアは `(A . B)` のように表され、再帰的に連結することで任意のデータ構造を表現できる。便宜上 `(A B C)` を `(A . (B . (C . nil)))` というようなリスト的な構造の略記とみなす。
  - 「アトム」はペアではないものである。上記 `nil` はリスト的な構造の終端を示すアトムである。他に真値Tもアトムである。
  - 注: ペアのことをリストと言うこともあるが、`nil` を「空リスト」と考えると「ペアではないがリストではある」というややこしい点があるため、リストという表現はここでは可能な限り避ける。

5つの関数とは、

<table>
<thead>
<tr class="header">
<th><p>関数</p></th>
<th><p>説明</p></th>
<th><p>記号的説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><code>atom</code></p></td>
<td><p>値がアトムなら <code>T</code> を返す。</p></td>
<td><p><code>atom[(A B)]</code> → <code>nil</code>、<br />
<code>atom[nil]</code> → <code>T</code></p></td>
</tr>
<tr class="even">
<td><p><code>eq</code></p></td>
<td><p>二つの値が同一のものなら <code>T</code> を返す。</p></td>
<td><p><code>eq[A;A]</code> → <code>T</code></p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/CARとCDR" title="wikilink"><code>car</code></a></p></td>
<td><p>ペアの左値をとり出す。</p></td>
<td><p><code>car[(A . B)]</code> → <code>A</code></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/CARとCDR" title="wikilink"><code>cdr</code></a></p></td>
<td><p>ペアの右値をとり出す。</p></td>
<td><p><code>cdr[(A . B)]</code> → <code>B</code></p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Cons_(Lisp)" title="wikilink"><code>cons</code></a></p></td>
<td><p>ペアを作る。</p></td>
<td><p><code>cons[A;B]</code> → <code>(A . B)</code></p></td>
</tr>
</tbody>
</table>

以上のデータと関数の他に下記の特殊形式\[2\]など（関数ではない）が必要である。

  - `cond`または`if`
  - `quote`
  - `lambda`
  - `define`

以上の道具立てにより、自分自身を解釈実行できるeval（超循環評価器）を理論上構成できることをマッカーシーは示した。これはある意味で、**万能[チューリングマシン](../Page/チューリングマシン.md "wikilink")**の構成と同様のことを行っており、現代的な見方からは一種の[操作的意味論](../Page/操作的意味論.md "wikilink")を与えたものとも言える。そのevalを[ポール・グレアム](../Page/ポール・グレアム.md "wikilink")が  流に書き直したサンプルがある\[3\]。また、このevalをそのままコンピュータプログラムとして実装すればLisp[インタプリタ](../Page/インタプリタ.md "wikilink")になると指摘し実装してみせたのはマッカーシー本人ではなくSteve Russell（[:en:Steve Russell](https://ja.wikipedia.org/wiki/:en:Steve_Russell "wikilink")）だった、というエピソードがある\[4\]。

なお、cons, car, cdr を次のように lambda を使って定義することも不可能ではないので（単純さのための便宜上Schemeで書いている）、

``` scheme
(define (my-cons a d) (lambda (f) (f a d)))
(define (my-car ad) (ad (lambda (a d) a)))
(define (my-cdr ad) (ad (lambda (a d) d)))
```

以上で説明したものが「最小」であるわけではないが、前述の5関数はLispで一般に最も多用されるリストの操作において公理のようなものと見ることができるため\[5\]、基本関数と呼ばれることがある。

## その他

論文中で理論的可能性として示されたものであるが、変数のスコープがいわゆる[動的スコープ](../Page/動的スコープ.md "wikilink")であることなどは、こんにちでは一種のバグのようなものとして扱われることもある（理論的には[静的スコープ](../Page/静的スコープ.md "wikilink")のほうが色々な意味で整合的である）。Lispの発展の過程で「FUNARG問題」などとしてその性質が論じられた。Lispkit Lisp（[:en:Lispkit Lisp](https://ja.wikipedia.org/wiki/:en:Lispkit_Lisp "wikilink")）などの実装を指してPure Lispとされることもある（なお、Lispkit Lispは静的スコープである）。

## 脚注

<references/>

## 外部リンク

  - \- ジョン・マッカーシーが最初に純  を導入した論文

  - [ プログラマーズマニュアル](http://history.siam.org/sup/Fox_1960_LISP.pdf)

[Category:LISP](https://ja.wikipedia.org/wiki/Category:LISP "wikilink")

1.  なお、論文における記述をはじめとして、初期のLispの実装は動的スコープで、（実は、世間でしばしば言われる評判とは異なって）理論的なそういった綺麗ではない点もあるにはある（理論的には静的（レキシカル）スコープのほうが整合性がある）。これは後に、実は、望んでいたものはレキシカルスコープだったのだが、得られたものは動的スコープだったのだ（ In modern terminology, lexical scoping was wanted, and dynamic scoping was obtained. <http://www-formal.stanford.edu/jmc/history/lisp/node4.html> より）、と自ら述べている。
2.
3.  （`lambda` は `defun` により暗黙のうちに使われている）
4.  <http://www-formal.stanford.edu/jmc/history/lisp/node3.html> より「S.R. Russell noticed that eval could serve as an interpreter for LISP, promptly hand coded it, and we now had a programming language with an interpreter.」
5.  『初めての人のためのLISP ［増補改訂版］』p. 55