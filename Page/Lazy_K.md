> この記事は[Lazy K](https://ja.wikipedia.org/wiki/Lazy_K)から翻訳されています。


（れいじーけー）は組み込み関数が3つしかない、純粋[関数型言語](../Page/関数型言語.md "wikilink")である。似た言語として、同じような表記をする、非純粋関数型言語であるがある。

## 概要

純粋関数型言語として、[チューリング完全](https://ja.wikipedia.org/wiki/チューリング完全 "wikilink")でありながら、絶対必要なエッセンスだけを抜き出したプログラミング言語である。[遅延評価](https://ja.wikipedia.org/wiki/遅延評価 "wikilink")を行う。使用するにも、処理系を実装するにも、[コンビネータ論理](https://ja.wikipedia.org/wiki/コンビネータ論理 "wikilink")の知識が必要である。

標準入力をプログラムである関数の引数として受け取る。ただし、標準入力は1バイトごとのの**スコットエンコードされたリスト**としてエンコードされ、出力も同様に1バイトごとのチャーチ数の**スコットエンコードされたリスト**となる。

にて  を実装した場合、 で  を実装した場合に比べて約1/10のソースサイズで収まる。

## 組み込み関数

の表記法を用いる。

  - `I x = x`
  - `K x y = x`
  - `S x y z = (x z) (y z)`

なお、`I` は `S` と `K` を用いて `I = SKK` と表せる。

記法では、`i=λx.xSK=S(SI(KS))(KK)` を唯一の組み込み関数として使用する。

## 表記法

ソースコードの表記方法として、4種類用意されている。それらを混在させてコーディングすることができる。

  - [コンビネータ算法様式](https://ja.wikipedia.org/wiki/:en:SKI_combinator_calculus "wikilink") - `SI(K(KI))`

  - 様式 - ``` ``si`k`ki ```

  - 様式

  - 様式

## 外部リンク

  - [The Lazy K Programming Language](https://tromp.github.io/cl/lazy-k.html)
  - [翻訳:プログラミング言語 ](http://e.tir.jp/wiliki?%cb%dd%cc%f5%3a%a5%d7%a5%ed%a5%b0%a5%e9%a5%df%a5%f3%a5%b0%b8%c0%b8%ecLazy_K)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:関数型言語](https://ja.wikipedia.org/wiki/Category:関数型言語 "wikilink")