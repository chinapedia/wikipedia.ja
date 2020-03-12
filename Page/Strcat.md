> この記事は[Strcat](https://ja.wikipedia.org/wiki/Strcat)から翻訳されています。


**strcat**は、ある[文字列](../Page/文字列.md "wikilink")に別の文字列を[連結](https://ja.wikipedia.org/wiki/文字列結合 "wikilink") (concatenate) する[C言語](../Page/C言語.md "wikilink")の[関数である](../Page/サブルーチン.md "wikilink")。 [標準Cライブラリ](../Page/標準Cライブラリ.md "wikilink")の文字列操作関数群が宣言されている[ヘッダーファイル](https://ja.wikipedia.org/wiki/ヘッダーファイル "wikilink") `string.h` に含まれる。

## 書式

``` c
#include <string.h>
char *strcat(char *s1, const char *s2);
```

## 機能

s2が指す文字列を、s1が指す[配列](../Page/配列.md "wikilink")の最後に連結する。戻り値は、s1の値である。また、コピー先とコピー元が重なる場合の動作は未定義とする。

## 実装例

``` c
char *StrCat(char *s1, const char *s2)
{
    char *p = s1;
    while(*s1++);           /* s1を最後まで進める */
    while(*s1++ = *s2++);   /* s2をコピーする */
    return p;
}
```

## バッファオーバーランの危険性と対策

strcatは、先程示した実装例を見ても分かる通り、s1の容量については一切関知しない。よって、s1の指す配列の範囲を越えて、s2が書き込まれてしまう[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")の恐れがある。バッファオーバーランによってメモリが破壊されたり、プログラムが異常動作したり、クラッシュしたりする危険性がある。簡単な対策として、冗長になるが事前に領域長計算を実行する例を示す。

``` c
char s1[80] = "filename";
const size_t bufsize = sizeof(s1); /* 固定長char配列の要素数を求める */
const size_t s1len = strlen(s1);
const char* s2 = ".exe";
const size_t s2len = strlen(s2);
if (s1len + s2len + 1 <= bufsize) /* 1は終端NUL文字用 */
{
    strcat(s1, s2);
    /* 以下でも可能だが、さらに冗長となるだけで意味はない。 */
    /*strncat(s1, s2, s2len);*/
}
```

上の例では、事前に`char`型配列`s1`全体のバッファサイズすなわち要素数と、使用済み領域の長さおよび書き込みに必要な領域の長さを比較することによって、配列の空きの容量を超えた書き込み（バッファオーバーラン）を防ぐことができる。なお、さらに異常系や汎用目的を考慮するならば、`s1`の内容が未初期化で終端NUL文字が含まれていない場合や、`s1len + s2len + 1`が[算術オーバーフロー](https://ja.wikipedia.org/wiki/算術オーバーフロー "wikilink")を起こしてしまう場合への対処も必要となってくる。

ただし、バッファオーバーランを防止するための事前領域長計算は、余分な時間的オーバーヘッドや複雑さを伴う。 字数制限付き文字列連結関数として[strncat](https://ja.wikipedia.org/wiki/strncat "wikilink")も存在するが、書き込み先のバッファサイズを指定できるわけではないので、やはりstrcat同様の危険性を持つことに変わりはない。

代替として、標準ライブラリの一部ではないが[strlcat](https://ja.wikipedia.org/wiki/strlcat "wikilink")やstrcat_sを使用することのできる処理系もある。 そのほか、単純な文字列連結用途としてはややオーバースペックではあるが、snprintfを使用する方法もある。

## 関連項目

  - [strlcat](https://ja.wikipedia.org/wiki/strlcat "wikilink")

## 外部リンク

  -
[en:Strcat](https://ja.wikipedia.org/wiki/en:Strcat "wikilink")

[Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink")