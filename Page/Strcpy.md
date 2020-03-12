> この記事は[Strcpy](https://ja.wikipedia.org/wiki/Strcpy)から翻訳されています。


**strcpy**は、指定したアドレスに指定した文字列をコピーする[C言語](../Page/C言語.md "wikilink")の[関数である](../Page/サブルーチン.md "wikilink")。 [標準Cライブラリ](../Page/標準Cライブラリ.md "wikilink")の文字列操作関数群が宣言されている[ヘッダーファイル](https://ja.wikipedia.org/wiki/ヘッダーファイル "wikilink") `string.h` に含まれる。 **ストリングコピー**などと呼ばれることが多い。

## 形式

``` c
#include <string.h>
char *strcpy(char *strDest, const char *strSrc);
```

## 機能

strDestが指す[配列](../Page/配列.md "wikilink")に、strSrcが指す文字列をコピーする。コピー元とコピー先が重なる場合の動作は、定義されない。

戻り値としてstrDestの値を返す。つまりコピー後の文字列を返すことになる。

## 使用例

strcpyを使用して文字列をコピーし、コピー先の文字列を[printf](https://ja.wikipedia.org/wiki/printf "wikilink")を使って表示する例。

``` c
#include <stdio.h> /* printfを使用するためのinclude */
#include <string.h> /* strcpyを使用するためのinclude */

int main(int argc, char **argv)
{
    char strSrc[12] = "ABCDEFGHIJ\n"; /* コピー元の文字列 */
    char strDest[12]; /* コピー先の文字列 */

    /* strDestにstrSrcの内容をコピーする */
    strcpy(strDest, strSrc);

    /* printfを使ってstrDestの内容を表示 */
    printf("%s", strDest);

    return 0;
}
```

## 実装例

strcpyを自前で定義する場合は、以下の様にする。

``` c
char *StrCpy(char *s1, const char *s2) /* strcpyと区別するため、大文字 */
{
    char *p = s1;
    while(*s1++ = *s2++); /* 代入結果が終端文字(0x00)になるまで代入し続ける */
    return p;
}
```

## バッファオーバーランの危険性と対策

strcpyはコピー先のバッファの長さを関知しない。もしコピー元の文字列の長さがコピー先のバッファの長さよりも大きい場合は、[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")によってメモリが破壊されたり、プログラムが異常動作したり、クラッシュしたりする危険性がある。簡単な対策として、冗長になるが事前に領域長計算を実行する例を示す。

``` c
char dst[80];
const size_t bufsize = sizeof(dst); /* 固定長char配列の要素数を求める */
const char* src = "abc 123";
const size_t srclen = strlen(src);
if (srclen + 1 <= bufsize) /* 1は終端NUL文字用 */
{
    strcpy(dst, src);
    /* 以下でも可能だが、さらに冗長となるだけで意味はない。 */
    /*strncpy(dst, src, srclen + 1);*/ /* +1は最後に終端NUL文字を付加するために必要 */
}
```

字数制限付き文字列コピー関数として[strncpy](https://ja.wikipedia.org/wiki/strncpy "wikilink")も存在するが、書き込み先のバッファサイズを指定できるわけではないので、やはりstrcpy同様の危険性を持つことに変わりはない。

代替として、標準ライブラリの一部ではないが[strlcpy](https://ja.wikipedia.org/wiki/strlcpy "wikilink")やstrcpy_sを使用することのできる処理系もある。 そのほか、単純な文字列コピー用途としてはややオーバースペックではあるが、snprintfを使用する方法もある。

## 関連項目

  - [strlcpy](https://ja.wikipedia.org/wiki/strlcpy "wikilink")

## 外部リンク

  -
[Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink")