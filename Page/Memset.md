> この記事は[Memset](https://ja.wikipedia.org/wiki/Memset)から翻訳されています。


**memset**とは、\<string.h\> (文字列操作関数群) または\<memory.h\>で定義されている[C言語](../Page/C言語.md "wikilink")の[関数である](https://ja.wikipedia.org/wiki/サブルーチン#関数 "wikilink")。

指定されたポインタが指すオブジェクトの先頭から、指定されたバイト数分に、指定した文字データを書き込むはたらきをする。 つまり、ポインタが指しているメモリブロック先頭から指定されたサイズの連続領域において、1バイトごとに文字をセットする。

## 形式

``` c
#include <string.h>
void *memset(void *buf, int c, size_t n);
```

`buf`は`unsigned char *`型に[キャストされる](../Page/型変換.md "wikilink")。`c`は`unsigned char`型にキャストされる。

## 利用例

次の例は、[char型](https://ja.wikipedia.org/wiki/整数型#文字型 "wikilink")[配列](../Page/配列.md "wikilink")（文字列）を文字`'@'`で埋めるプログラムである。

``` c
#include <stdio.h>
#include <string.h>

#define STR_BUF_SIZE 10

int main(void) {
    char a[STR_BUF_SIZE];
    memset(a, '@', STR_BUF_SIZE); /* 配列の要素全てを文字'@'で埋める */
    a[STR_BUF_SIZE - 1] = '\0';
    printf("a = \"%s\"\n", a);
    return 0;
}
```

配列や[構造体](../Page/構造体.md "wikilink")のメモリブロックをゼロで埋める際は、以下の様に`memset`を用いる。

``` c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define STR_BUF_SIZE 100

int main(void) {
    char *s = NULL;
    s = (char*)calloc(STR_BUF_SIZE, sizeof(char));
    strcpy(s, "password1");
    printf("s = \"%s\"\n", s);
    /* メモリ領域から古いパスワードの痕跡を完全にクリアして空文字列化する。 */
    memset(s, 0, STR_BUF_SIZE);
    /* 新しいパスワードをコピーする。 */
    strcpy(s, "pass2");
    printf("s = \"%s\"\n", s);
    /* 単純にゼロ終端文字列で空文字列を実現する場合、先頭にNUL文字を代入するか、空文字列をコピーするだけでもよいが、痕跡が残る。 */
#if 0
    s[0] = '\0';
#else
    strcpy(s, "");
#endif
    printf("s = \"%s\"\n", s);
    printf("s[1] = '%c'\n", s[1]);
    memset(s, 0, STR_BUF_SIZE);
    free(s);
    return 0;
}
```

ただしmemset呼び出しはコンパイラ最適化によって除去されることもある。機密性の高い情報をメモリからクリアするなど、セキュリティ脆弱性の解消を目的とする場合は、[C11オプション関数のmemset](https://ja.wikipedia.org/wiki/C11_\(C言語\) "wikilink")_sや、[Windows APIのSecureZeroMemoryなどを使用する](https://ja.wikipedia.org/wiki/Windows_API "wikilink")。

## 実装例

memsetを自前で定義したい場合は、以下の様に実装する。

``` c
/* memsetと区別するため、大文字を使用 */
void *MemSet(void *buf, int c, size_t num) {
    unsigned char *ptr = (unsigned char *)buf;
    const unsigned char ch = c;

    while (num--)
        *ptr++ = ch;

    return buf;
}
```

## 関連項目

  - [C言語](../Page/C言語.md "wikilink")
  - [標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")
  - [プログラミング言語](../Page/プログラミング言語.md "wikilink")

## 外部リンク

  -
[Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink")