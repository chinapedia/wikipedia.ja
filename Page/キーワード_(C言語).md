> この記事は[ \(C\)](https://ja.wikipedia.org/wiki/_\(C\))から翻訳されています。


この項では、[C言語](../Page/C言語.md "wikilink")の**キーワード**に関して説明する。

この項目は、プログラムの細かい説明には立ち入らず、他の言語と比較できるような説明を目的としている。ISO/IEC 9899 に沿って記載する。なお、[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")の[K\&R第](https://ja.wikipedia.org/wiki/プログラミング言語C "wikilink")1版にはキーワードの記載が無かったが、[1988年](../Page/1988年.md "wikilink")の第2版では付録A2.4に「キーワード（[予約語](../Page/予約語.md "wikilink")）」がある。

## Cのキーワードの特徴

キーワード数は以下の通り。

  - [K\&R第](https://ja.wikipedia.org/wiki/プログラミング言語C "wikilink")2版 (1988): 32
  - C89: 32
  - [C99](../Page/C99.md "wikilink"): 37。_Bool, _Complex, _Imaginary, inline, restrict が追加。
  - [C11](https://ja.wikipedia.org/wiki/C11_\(C言語\) "wikilink"): 44。_Alignas, _Atomic, _Generic, _Noreturn, _Static_assert, _Thread_local, alignof が追加。

[プリミティブ型](../Page/プリミティブ型.md "wikilink")、分岐 ([if](../Page/If文.md "wikilink"), [switch](../Page/Switch文.md "wikilink"))、反復 ([for](../Page/For文.md "wikilink"), [while](../Page/While文.md "wikilink")) などの基本的な語は、[C++](../Page/C++.md "wikilink")でもほぼそのまま取り入れられている。

## 型に関するキーワード

C++とほぼ共通の語を使用している。

### [整数型](../Page/整数型.md "wikilink")

  - , , , ,
    C99以降では、long は2つ続けて long long とすることで、64[ビット](../Page/ビット.md "wikilink")以上の精度をもつ1つの型を表す。C99で加わった_Bool型も一種の整数型として扱われ、またtrueやfalseはキーワードではなく、stdbool.hで定義されるマクロである。

### 符号の有無

  - ,
    signed および unsigned は、整数型の前後に付加することによって符号の有無を指定する。

### 浮動小数点型

  - ,
    double は long と組み合わせて long double 型を表す際にも使用する。

### [複素数](../Page/複素数.md "wikilink")型

  - ,
    C99にて標準化。_Imaginary は厳密には複素数型ではなく虚数型であり、すべての処理系でサポートされるわけではない。これらは直前に浮動小数点型を伴って精度を指定する。

記述例:

``` c
double _Complex z = 1.2 + 3.4 * I;
```

### [構造体](../Page/構造体.md "wikilink")・[共用体](https://ja.wikipedia.org/wiki/共用体 "wikilink")・[列挙体](../Page/列挙型.md "wikilink")

  - , ,
    これらは、タグ名を伴ってユーザ定義の型を定義するのに使用する。

記述例:

``` c
struct my_type
{
  int a;
  double b;
};
```

### 型修飾子

  - , ,
    volatile はコンパイラの最適化を抑止する。
    const はオブジェクトが書き換えられないことを明示する。
    restrict はオブジェクトへのアクセスが常にその[ポインタを用いて行われることを明示する](../Page/ポインタ_\(プログラミング\).md "wikilink")。C99にて標準化。

### 記憶クラス指定子

  - , , ,
    auto は宣言したブロック内のみで有効。[関数が終了すると消滅](../Page/サブルーチン.md "wikilink")。記憶クラス指定子を省略した場合[デフォルトでautoとなる](../Page/デフォルト_\(コンピュータ\).md "wikilink")。そのため実際上使用されていない。[B言語](../Page/B言語.md "wikilink")のauto指定子との互換を意識したもの。

    extern は他のモジュール内で定義されている名前を参照する際に使う。

    static は関数内と関数外で意味が違う。関数内では静的変数の定義で、autoとは異なり関数が終了しても消滅せず、再び同じ関数を呼び出した場合は前回の値がそのまま残っている。関数外では可視性の制限で、static宣言した変数や関数は他のモジュールから参照できない。

    register は変数の記憶領域を[CPU](../Page/CPU.md "wikilink")のレジスタに割り当てる（必ずしも割り当てられるわけではない）。それ以外はautoと同じ。

  -

    型に別名を付ける。これは構文上は記憶クラス指定子に分類されるが、記憶クラスと直接関係はない。

### その他の型

  - [void](https://ja.wikipedia.org/wiki/void_\(コンピュータ\) "wikilink")
    引数や返却値のない[関数で使用する](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")。また、特定の型を指さない[ポインタ型にも使用する](../Page/ポインタ_\(プログラミング\).md "wikilink")。

記述例:

``` c
void func(void);

int a;
void *p = &a;
```

## 制御構造

制御に関する語もC++とほぼ共通であるが、Cには[例外処理](../Page/例外処理.md "wikilink")に関する語（try, catch, throw等）は存在しない。

### [条件分岐](../Page/分岐命令.md "wikilink")

  - ,
    , ,

### [繰返し](../Page/ループ_\(プログラミング\).md "wikilink")

  - , ,

### 分岐

  -
    ラベルの位置に分岐する。
  -
    ループの先頭に戻る。
  -
    ループのブロックから抜け出す。
  -
    関数から抜け出す。返却値のあるものは値を返す。

## マルチスレッド

  - ,
    C11にて追加

## [アライメント](https://ja.wikipedia.org/wiki/データ構造アライメント "wikilink")

  - ,
    C11にて追加

## その他

### [インライン関数](../Page/インライン関数.md "wikilink")

  -
    C99にて標準化。関数指示子に使用することで、[関数を](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")[インライン展開](../Page/インライン展開.md "wikilink")するためのヒントをコンパイラに与える。

### 演算子

  -
    式、またはかっこでくくった型名をオペランドに取る単項演算子として使用する。

### アサート

  -
    C11にて追加。静的[表明](../Page/表明.md "wikilink")を提供する。

### 型ジェネリック

  -
    C11にて追加

### 関数指定子

  -
    C11にて追加。関数が return しない（呼び出し元に戻らない）ことを指定。

## 関連項目

  - [キーワード (C++)](../Page/キーワード_\(C++\).md "wikilink")
  - [CとC++の演算子](https://ja.wikipedia.org/wiki/CとC++の演算子 "wikilink")

[Category:プログラミング言語の構文](https://ja.wikipedia.org/wiki/Category:プログラミング言語の構文 "wikilink") [Category:C言語](https://ja.wikipedia.org/wiki/Category:C言語 "wikilink")