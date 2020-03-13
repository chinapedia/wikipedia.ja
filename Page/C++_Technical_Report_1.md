> この記事は[C++ Technical Report 1](https://ja.wikipedia.org/wiki/C++_Technical_Report_1)から翻訳されています。


**C++ Technical Report 1** (**TR1**、Technical Report on C++ Library Extensions)は、**ISO/IEC TR 19768:2007**\[1\] の非公式名称で、[標準C++ライブラリ](../Page/標準C++ライブラリ.md "wikilink")の拡張についての標準規格である。これには[正規表現](../Page/正規表現.md "wikilink")、[スマートポインタ](https://ja.wikipedia.org/wiki/スマートポインタ "wikilink")、[ハッシュ表](../Page/ハッシュテーブル.md "wikilink")、[擬似乱数](../Page/擬似乱数.md "wikilink")生成器などが含まれている。TR1の目標は「拡張された標準C++ライブラリの使用方法について慣習を確立してほしい」とのことである\[2\]。

## 概要

TR1は 既に一部ないし全部を実装しているものもある。ちなみに、TR1のほとんどは[Boost](https://ja.wikipedia.org/wiki/Boost "wikilink")に含まれており、それが利用可能である。

TR1はC++のライブラリの拡張の全てではない。たとえば[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")では[スレッドに関するライブラリが含まれ](../Page/スレッド_\(コンピュータ\).md "wikilink")、言語機能自体の拡張（move semanticsやvariadic templatesの追加など）などSTL全体に機能増強が行われた。

なお、TR1で追加されたライブラリは、現標準ライブラリと区別するため、[名前空間](../Page/名前空間.md "wikilink") `std::tr1` に入れられている。しかし、C++11では名前空間 `std` に入れられた。

TR1にとってC++11は必須ではないが、現行のC++上で全て実装可能というわけでもない。例えば、型の[POD](https://ja.wikipedia.org/wiki/POD "wikilink")性を検査する関数`is_pod`の実装にあたって、現行のC++にはクラスがPODであることを判別する方法が無い。したがって、現在のC++処理系でのTR1実装は、コンパイラ独自の拡張機能を使用するか、あるいは擬似的な実現に留まる。この状況は、かつて一部コンパイラが[テンプレートの部分特殊化](../Page/テンプレートの部分特殊化.md "wikilink")に対応していなかった時代のSTLの擬似実装とよく似ている。

注意点としては、TR1はC++の仕様の一部ではないので、`std::tr1` 名前空間やTR1の機能に依存したコードは後々問題を起こす可能性がある。というのも、最近のドラフトであるn3225\[[http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2010/n3225.pdf\]では](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2010/n3225.pdf%5Dでは)<type_traits>で定義される `has_*` は`is_*` へ変更されている。また、`std::tr1` は次期標準の仕様にも**含まれない**ので注意されたい。

## 実装

次のような実装が存在する。

  - [Visual C++](../Page/Microsoft_Visual_C++.md "wikilink") 2008のFeature Pack\[3\]そしてその後に出たサービスパック1\[4\]
  - [libstdc++](https://ja.wikipedia.org/wiki/libstdc++ "wikilink")\[5\]
  - Boost\[6\]

## 内容

TR1には次のものが含まれている。

### 一般ユーティリティ

#### 参照ラッパ

  - Boost.Ref由来[2](http://www.boost.org/doc/html/ref.html)。
  - <functional>ヘッダに追加。 - `cref`, `ref`, `reference_wrapper`
  - [アルゴリズム](../Page/アルゴリズム.md "wikilink")や[関数オブジェクト](https://ja.wikipedia.org/wiki/関数オブジェクト "wikilink")に対して、値渡しではなく参照渡しを行うことができる。

#### [スマートポインタ](../Page/ガベージコレクション.md "wikilink")

  - Boost Smart Pointer libraryを基にしている [3](http://www.boost.org/libs/smart_ptr/smart_ptr.htm)。
  - <memory>ヘッダに追加。 - `shared_ptr`, `weak_ptr`, etc
  - より安全にメモリ管理を行うためのユーティリティ。[参照カウント](../Page/参照カウント.md "wikilink")に基づくスマートポインタである。

### [関数オブジェクト](https://ja.wikipedia.org/wiki/関数オブジェクト "wikilink")

<functional>ヘッダに4つのモジュールが追加。

#### function - [多態的関数ラッパ](../Page/ポリモーフィズム.md "wikilink")

  - Boost.Functionを基にしている[4](http://www.boost.org/doc/html/function.html)。

#### bind - 関数オブジェクトの束縛

  - Boost Bind libraryから採用された[5](http://www.boost.org/libs/bind/bind.html)。
  - 現標準の`std::bind1st`及び`std::bind2nd`をより一般化したもので、関数オブジェクトへ引数の[束縛を行う](https://ja.wikipedia.org/wiki/名前束縛 "wikilink")。

#### result_of - 関数の戻り値の型

  - Boostを基にしている。
  - 関数呼出式から、戻り値の型を決める機構。

#### mem_fn

  - Boost Mem Fn libraryを基にしている[6](http://www.boost.org/libs/bind/mem_fn.html)。
  - 現標準の`std::mem_fun`及び`std::mem_fun_ref`から機能向上したものである。
  - [メンバ関数](https://ja.wikipedia.org/wiki/メンバ関数 "wikilink")へのポインタを関数オブジェクトにする機構である。

### [メタプログラミング](../Page/メタプログラミング.md "wikilink")と型特性

  - 新しく<type_traits>ヘッダが追加。 - `is_pod`, `has_virtual_destructor`(C++11では`is_virtual_destructible`に変更), `remove_extent`, etc
  - Boost Type Traits libraryを基にしている[7](http://www.boost.org/libs/type_traits/doc/html/index.html)。
  - [データ型](../Page/データ型.md "wikilink")に関しての問い合わせを容易にすることによってメタプログラミングの支援をする。

### 数値計算

#### [擬似乱数](../Page/擬似乱数.md "wikilink")生成

  - 新しく<random>ヘッダが追加。 - `variate_generator`, [`mersenne_twister`](../Page/メルセンヌ・ツイスタ.md "wikilink"), `poisson_distribution`, etc
  - Boost Random Number Libraryを基にしている[8](http://www.boost.org/libs/random/)。

#### 数学関数

  - <cmath>/`<math.h>`ヘッダに追加。 - [`beta`](https://ja.wikipedia.org/wiki/ベータ関数_\(数学\) "wikilink"), [`legendre`](https://ja.wikipedia.org/wiki/ルジャンドル多項式 "wikilink"), etc
  - 各種数学関数。

### [コンテナ](../Page/コンテナ_\(データ型\).md "wikilink")

#### [タプル](../Page/タプル.md "wikilink")

  - 新しく<tuple>ヘッダが追加。 - `tuple`
  - Boost Tuple libraryを基にしている[9](http://www.boost.org/libs/tuple/doc/tuple_users_guide.html)。
  - およそ`std::pair`の拡張である。
  - さまざまなデータ型を混在できる容量固定のデータ構造である。

#### 容量固定[配列](../Page/配列.md "wikilink")

  - 新しく<array>ヘッダが追加。 - `array`
  - Boost Array libraryから採用された[10](http://www.boost.org/doc/html/array.html)。
  - 標準の`std::vector`のような動的配列とは全く逆の存在である。

#### [ハッシュテーブル](../Page/ハッシュテーブル.md "wikilink")

  - 新しく<unordered_set>, <unordered_map>ヘッダが追加。
  - 既存のライブラリを基にしたものではなく、新たに作られたものである。
  - 要素の参照は、大抵の場合[定数時間](https://ja.wikipedia.org/wiki/定数時間 "wikilink")で済むが、最悪の場合には[線形時間](../Page/線形時間.md "wikilink")かかる。
  - 名前が`hash_set`（SGI版STLに含まれるライブラリ）などでないが、標準の`set`,`map`はイテレータを用いて順序付けされた（[ソート](../Page/ソート.md "wikilink")された）要素アクセスが可能であるのに対し、`unordered_set`, `unordered_map`では不可能であることを示している。実装ではなくインターフェース（利用法）に由来した名前をつける発想である。

### 正規表現

  - 新たに<regex>ヘッダが追加。 - `regex`, `regex_match`, `regex_search`, `regex_replace`, etc
  - Boost Regex libraryを基にしている[11](http://www.boost.org/libs/regex/doc/html/index.html)。
  - [正規表現](../Page/正規表現.md "wikilink")による[パターンマッチング](../Page/パターンマッチング.md "wikilink")を行うライブラリ。

### C互換ライブラリ

[C++](../Page/C++.md "wikilink")は[C言語](../Page/C言語.md "wikilink")と互換になるように設計されているものの、現在C++は厳密な上位互換ではない。TR1はその溝を埋めるため<complex>, <locale>, <cmath>その他のヘッダに拡張を行っている。これによって[C99](../Page/C99.md "wikilink")とある程度は近づいたものの、C99の全てがTR1に含まれているわけではない。

## C++ Technical Report 2

C++ Technical Report 2 も作られたが\[7\]、正式に出版されることはなかった。

## 脚注

## 関連項目

  - [C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink") - TR1の内容が取り込まれたC++標準。
  - [C++14](https://ja.wikipedia.org/wiki/C++14 "wikilink")
  - [Boost](https://ja.wikipedia.org/wiki/Boost "wikilink") - TR1の一部のライブラリの基となっている。
  - [Standard Template Library](../Page/Standard_Template_Library.md "wikilink") - 現標準C++ライブラリの一部である。

## 参考文献

  - Peter Becker: "The C++ Standard Library Extensions: A Tutorial and Reference", 2006, ISBN 0321412990. TR1にも言及している。

## 外部リンク

  - <http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2005/n1836.pdf> - このドラフト文書のPDF
  - <http://aristeia.com/EC3E/TR1_info_frames.html> - [スコット・メイヤーズ](https://ja.wikipedia.org/wiki/スコット・メイヤーズ "wikilink") TR1 page, links to documents and articles

[Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink")

1.  [ISO/IEC TR 19768:2007](http://www.iso.org/iso/iso_catalogue/catalogue_ics/catalogue_detail_ics.htm?ics1=35&ics2=60&ics3=&csnumber=43289)
2.  [1](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2005/n1745.pdf)
3.
4.
5.
6.
7.  [TR2 call for proposals](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2005/n1810.html)