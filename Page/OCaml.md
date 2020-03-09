> この記事は[OCaml](https://ja.wikipedia.org/wiki/OCaml)から翻訳されています。


**OCaml**（ 、オーキャムル、オーキャメル）は、フランスの  が開発した[プログラミング言語MLの方言とその実装である](../Page/ML_\(プログラミング言語\).md "wikilink")。MLの各要素に加え、オブジェクト指向的要素の追加が特長である。かつては  という名前で、その略として  と広く呼ばれていたが、正式に  に改名された\[1\]。

## 概要

もとはCamlという名前の、MLの方言の処理系実装、および言語であった。この名前はcategorical abstract machine languageの頭字語である。クラスや[継承など](https://ja.wikipedia.org/wiki/継承_\(プログラミング\) "wikilink")[クラスベース](https://ja.wikipedia.org/wiki/クラスベース "wikilink")[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")の言語機能が追加され Objective Camlという名前になり、その後、略称だったOCamlを正式な名前とした。ウェブサイトの概要説明では「OCamlはCaml派生の言語の中で最も知られたものである」\[2\]としている。もとの処理系も配布され続けており、Caml Lightという名前になっている。英語ではCamlはcamel（ラクダ）と同様に発音されており、アイコン等にもラクダを使っている。

MLの特徴の他に、関数型とオブジェクト指向の両方を併せもつことが特徴的である。ただしそのため、オブジェクト指向を利用した破壊的操作を伴うプログラムがかなり容易に書けてしまう。また、多相バリアント型という特殊なバリアント型により（通常のバリアント型については[代数的データ型](https://ja.wikipedia.org/wiki/代数的データ型 "wikilink")を参照のこと）、サブセットとスーパーセットの関係になっているバリアント型などを記述できるなどといった特徴もある。

処理系としての特徴は、関数型言語としてはかなり高速に動作することが挙げられ、[gccでコンパイルされた](https://ja.wikipedia.org/wiki/GNUコンパイラコレクション "wikilink")[C言語](../Page/C言語.md "wikilink")と互角かやや遅い程度と言われる\[3\]。

関数型言語としては比較的アプリケーションの数が多く、例えば[MediaWiki](https://ja.wikipedia.org/wiki/MediaWiki "wikilink")において[TeX](../Page/TeX.md "wikilink")の記述から[HTML](https://ja.wikipedia.org/wiki/HyperText_Markup_Language "wikilink")、[MathML](https://ja.wikipedia.org/wiki/MathML "wikilink")および画像の数式を生成するプログラムもOCamlで記述されている\[4\]。

##

は、 の前身であるMLの方言とその実装である。現在も  という名前で\[5\]配布され続けている。

### MinCaml

MinCamlは、[ペンシルベニア大学](https://ja.wikipedia.org/wiki/ペンシルベニア大学 "wikilink")（当時）の[住井英二郎](https://ja.wikipedia.org/wiki/住井英二郎 "wikilink")がOCamlで実装した、Caml似のMLの小型版である。同作者により、[コンパイラ](../Page/コンパイラ.md "wikilink")が OCaml 自身で書かれている。MinCaml は、[2004年](https://ja.wikipedia.org/wiki/2004年 "wikilink")度の[未踏ソフトウェア創造事業に採択された](https://ja.wikipedia.org/wiki/情報処理推進機構 "wikilink")。

MinCaml コンパイラは教育目的での利用を主眼としている。わずか2000行前後のコードで書かれており、実装されている機能はMLのサブセットである。バックエンドは[SPARC](https://ja.wikipedia.org/wiki/SPARC "wikilink")と[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")に対応しており、ある程度の学習をすれば比較的容易に改造を行うことができる（実際、有志によって[PowerPC](https://ja.wikipedia.org/wiki/PowerPC "wikilink")用に出力できるバージョンも提供されている。バックエンドを[LLVMに置き換えた例も報告されている](https://ja.wikipedia.org/wiki/Low_Level_Virtual_Machine "wikilink")\[6\]。）。実際に[東京大学](https://ja.wikipedia.org/wiki/東京大学 "wikilink")理学部情報科学科などで教育目的に利用され、国内における OCaml および関数型言語の普及と理解に一定の役割を果たしている。

  - [速攻MinCamlコンパイラ概説](http://min-caml.sourceforge.net/) - MinCamlの配布・解説（`SourceForge.net`）

### Moscow ML

CamlやOCamlのような方言ではなく、SML（[Standard ML](https://ja.wikipedia.org/wiki/Standard_ML "wikilink")）の処理系の実装にCaml Light利用している。完全なSMLを実装する。

### その他

など、研究用の改造のベースとして、規模の大きくなった  ではなく（）を利用する例がみられる。

## プログラム例

以下の例は、プログラム自体としてはMLと比べ特別なものでもないし、オブジェクト指向を活用したものでもないが、を含む  では旧来のMLや  からの記法や演算子や名前の変更が多く、簡単なプログラムでもそのままではエラーになるものが多いので、ここでは  のコードを示す。

特徴として、型推論の活用により、多くの場合に型の宣言が必要なく、一部の静的型付き言語にありがちな煩雑さがないことが挙げられる。

###

の例を示す。以下のプログラム `hello.ml` は、

``` ocaml
print_endline "Hello world!";;
```

以下のようにして[バイトコード](https://ja.wikipedia.org/wiki/バイトコード "wikilink")に[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")される。

``` sh
$ ocamlc hello.ml -o hello
```

以下が実行結果である。

``` sh
$ ./hello
Hello world!
$
```

### クイックソート

[クイックソート](https://ja.wikipedia.org/wiki/クイックソート "wikilink")のコード例を示す。MLは多くの関数型言語と同様、[再帰](https://ja.wikipedia.org/wiki/再帰 "wikilink")処理に秀でる。また、 などにも見られるパターンマッチの機能がここでも使われている。

``` ocaml
let rec quicksort = function
   | [] -> []
   | pivot :: rest ->
       let is_less x = x < pivot in
       let left, right = List.partition is_less rest in
       quicksort left @ [pivot] @ quicksort right
```

### チャーチ数

以下は、[ラムダ計算](https://ja.wikipedia.org/wiki/ラムダ計算 "wikilink")の教科書などに見られる、[自然数](https://ja.wikipedia.org/wiki/自然数 "wikilink")のチャーチ符号化のコード例である。

``` ocaml
let zero f x = x
let succ n f x = f (n f x)
let one = succ zero
let two = succ (succ zero)
let add n1 n2 f x = n1 f (n2 f x)
let to_int n = n (fun k -> k+1) 0
let _ = print (add (succ two) two)
```

チャーチ数nは、[高階関数](https://ja.wikipedia.org/wiki/高階関数 "wikilink")として表され、関数fと値xを受け取りxにn回fを適用する関数として定義されている。チャーチ数nを自然数nに変換するには、チャーチ数（実体は関数）に、[インクリメント](https://ja.wikipedia.org/wiki/インクリメント "wikilink")する関数と初期値0を渡せばよい。MLは関数型言語であるため、数学的なプログラミングの理論そのままに、記述することができる。

##  で書かれたソフトウェア

  - [FFTW](https://ja.wikipedia.org/wiki/FFTW "wikilink") – [離散フーリエ変換](https://ja.wikipedia.org/wiki/離散フーリエ変換 "wikilink")を高速に行う[高速フーリエ変換](https://ja.wikipedia.org/wiki/高速フーリエ変換 "wikilink")の[ライブラリ](https://ja.wikipedia.org/wiki/ライブラリ "wikilink")。[C言語](../Page/C言語.md "wikilink")のコードを出力する`genfft` という OCaml プログラムが使われている。

  - – 二つのディレクトリのファイルを比較し同期をとるプログラム。

  - –  用の  クライアント。

  - – マルチプラットフォームの、フリーの家系図ソフトウェア。

  - – [オープンソース](../Page/オープンソース.md "wikilink")のプログラミング言語およびコンパイラ実装。

  - – [C言語](../Page/C言語.md "wikilink")のプログラムを解析するためのフレームワーク。

  - \- [INRIA](https://ja.wikipedia.org/wiki/INRIA "wikilink")で開発されている定理支援証明系言語。

  - Flow - [JavaScript](https://ja.wikipedia.org/wiki/JavaScript "wikilink")の静的型チェッカー。[Facebook](https://ja.wikipedia.org/wiki/Facebook "wikilink")により開発されている。

  - \- 自己進化型のスマート・コントラクト プラットフォーム。XTZ を仮想通貨とする。

## 参考文献

  -
  -
## 脚注

## 関連項目

  -
  - [F Sharp](https://ja.wikipedia.org/wiki/F_Sharp "wikilink")

## 外部リンク

  -
  - [ 入門](http://www.fos.kuis.kyoto-u.ac.jp/~t-sekiym/classes/isle4/mltext/ocaml.html)

  - [ プログラミング入門](http://www.i.kyushu-u.ac.jp/~bannai/ocaml-intro/intro.html)

  - [](http://web.yl.is.s.u-tokyo.ac.jp/~ganat/ocaml/ocaml.html)

  - [`OCaml.JP`](http://ocaml.jp/)

<!-- end list -->

  - [チュートリアル](http://www.ocaml-tutorial.org/ja)
  - [](http://ocamldt.free.fr/)
  - [](http://pleac.sourceforge.net/pleac_ocaml/index.html)

[Category:関数型言語](https://ja.wikipedia.org/wiki/Category:関数型言語 "wikilink") [Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink")

1.  <https://caml.inria.fr/ocaml/name.en.html>
2.
3.
4.  [Texvc - MediaWiki](https://www.mediawiki.org/wiki/Texvc)
5.  正確には名前だけでなく、新しい手法で再実装されたもので、 より  のほうが古くからある。
6.  <https://mzp.hatenablog.com/entry/2013/05/08/214712>