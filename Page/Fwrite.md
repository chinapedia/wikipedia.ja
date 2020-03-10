> この記事は[Fwrite](https://ja.wikipedia.org/wiki/Fwrite)から翻訳されています。


**fwrite**は、[C言語](../Page/C言語.md "wikilink")の標準入出力[ヘッダーファイル](https://ja.wikipedia.org/wiki/ヘッダーファイル "wikilink") \<stdio.h\> で宣言されている[関数である](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")。 主に、バイナリ形式のファイル出力に使われる。

## 形式

``` c
#include <stdio.h>
size_t fwrite(void *buf, size_t size, size_t nmemb, FILE* stream);
```

戻り値は書き込んだ項目数である。 `buf`に格納されている大きさ`size`の最大`nmemb`個の要素を`stream`の指すストリームに書き込む。 もし`stream`がテキストモードで開かれていれば、[改行コード](https://ja.wikipedia.org/wiki/改行コード "wikilink")CRはCR+LFに置換される。 ただしその場合でも戻り値に影響はない。

## コード例

ユーザーの入力を受け取り、バイナリモードで sample.dat に書き込んだ後、読み込んで表示する。

``` c
#include <stdio.h>
#include <stdlib.h>

int main(void)
{
    FILE* fp;
    double v;
    size_t len;

    printf("実数を入力してください\n");
    scanf("%lf", &v);

    /* sample.dat への書き込み */
    fp = fopen("sample.dat", "wb");
    if (fp == NULL) {
        fprintf(stderr, "sample.datを開けません\n");
        exit(-1);
    }
    len = fwrite(&v, sizeof(double), 1, fp);
    if (len != 1) {
        fprintf(stderr, "sample.datへの書き込み失敗\n");
        exit(-1);
    }
    fclose(fp);

    /* sample.dat からの読み込み */
    fp = fopen("sample.dat", "rb");
    if (fp == NULL) {
        fprintf(stderr, "sample.datを開けません\n");
        exit(-1);
    }
    len = fread(&v, sizeof(double), 1, fp);
    if (len != 1) {
        fprintf(stderr, "sample.datからの読み込み失敗\n");
        exit(-1);
    }
    fclose(fp);
    printf("読み取った値:%f\n", v);

    return 0;
}
```

## 関連項目

  - [fread](https://ja.wikipedia.org/wiki/fread "wikilink")

## 外部リンク

  -
[en:C file input/output\#fwrite](https://ja.wikipedia.org/wiki/en:C_file_input/output#fwrite "wikilink")

[Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink")