> この記事は[Fgets](https://ja.wikipedia.org/wiki/Fgets)から翻訳されています。


**fgets** は[C言語](../Page/C言語.md "wikilink")の[標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")における、標準入出力ヘッダー（\<stdio.h\>）で宣言されている FILE[ポインタから](../Page/ポインタ_\(プログラミング\).md "wikilink")1行分の[文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")を取り出す入力[関数である](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")。

## 形式

stdio.h で fgets は以下のような形式で宣言されている。

``` c
char *fgets(char *s, int n, FILE *stream)
```

fgets は stream が示すファイルから改行（'\\n'）または n-1 バイト目まで文字を読み込み、引数で渡された s に格納する。この n-1 バイトの中には改行自体も含まれる。その後文字列の末尾に終端記号 '\\0' を付与する。[戻り値](https://ja.wikipedia.org/wiki/戻り値 "wikilink")は stream の先頭が [EOF](https://ja.wikipedia.org/wiki/EOF "wikilink") だった場合もしくは途中でエラーが起こった場合は NULL、それ以外の場合は s である。

名称から [gets](https://ja.wikipedia.org/wiki/gets "wikilink")のファイル読み込み版のように思われるが、fgets は gets と異なり引数に最大読み込み文字数を指定する。また gets は末尾の改行を終端記号に置き換えるのに対し、fgets は改行の後ろに終端記号を付与するという点が異なる。

## gets や scanf の代替として用いる場合

fgets は本来ファイルから文字列を取り出すことを目的とした関数であるが、最大文字列数を引数に指定する事ができるため[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")が発生しにくく、また入力された文字数が最大文字数を超えた場合でも末尾に終端記号が付与されることが保証されている等、標準Cライブラリの中ではかなり[セキュア](https://ja.wikipedia.org/wiki/セキュア "wikilink")な構造となっているといえる。

これに対し、[標準入力](https://ja.wikipedia.org/wiki/標準入力 "wikilink")用に用意されている関数の中で fgets と同様の機能を実現するものとして[gets](https://ja.wikipedia.org/wiki/gets "wikilink")や[scanf](https://ja.wikipedia.org/wiki/scanf "wikilink")があるが、[gets](https://ja.wikipedia.org/wiki/gets "wikilink")は最大文字数を指定できないためバッファオーバーランが防ぐ手段が存在せず、[scanf](https://ja.wikipedia.org/wiki/scanf "wikilink")は文字幅指定できるが省略可能であるため開発者のミスで書き忘れる危険性がある等、安全性に問題点を持つものが多い。

このため fgets を標準入力用の関数として gets や scanf の代替として用いることが推奨されている\[1\]\[2\]。ただし、fgets を標準入力関数の代替として用いる場合は下記に宣べるような点に注意しなければならない。

### 改行文字の扱い

fgets は gets や scanf と異なり改行文字も 1文字として数える。このため scanf や gets を fgets に置き換える場合に改行文字を除去する処理を加えておかなければ元のコードと同一の動作となる保証は無い。実際に入力データを[fopen](https://ja.wikipedia.org/wiki/fopen "wikilink")や[system](https://ja.wikipedia.org/wiki/system "wikilink")等の関数のパラメータとして渡す場合では文字列は末尾に改行文字があるとエラーとなる。

### 最大文字数を超えた入力に対する対処

gets 関数は改行文字が入力されるまで標準入力を読み続けるため、入力終了後に[ストリーム上に文字が残る事は無い](https://ja.wikipedia.org/wiki/ストリーム_\(プログラミング\) "wikilink")、しかし fgets に置き換えた場合最大文字数を超えた入力が行われた場合、n バイト以降は入力ストリームにそのまま残されてしまい、後から別の入力を行うときに誤作動を起こす可能性がある。

scanf では代入抑止を使用することで入力ストリームをクリアする方法がある（[参照](https://ja.wikipedia.org/wiki/scanf#バッファオーバーラン "wikilink")）が、fgets にはそのような機能は無いため別途入力ストリームをクリアする処理を追加する必要がある。

また fgets で最大文字数を超える入力があった場合には、戻り値はエラーを返しては来ないので、入力された文字列に改行文字が含まれるかどうかで判断する必要がある。

### getsを置き換える例

実際に gets を fgets に置き換える場合は上記の事を考慮しなければならない、ここでは実際に gets を fgets に置き換える例を示す。具体的には gets を使用した以下のようなコードがあるとする、

``` c
char a[20];

if (gets(a) == NULL) {
    // エラー処理
}
```

この時このコードを fgets に置き換えて、その後の処理に影響を与えないようにする場合は以下のようになる、

``` c
char a[20];

if (fgets(a, 20, stdin) == NULL) {
    // エラー処理
}

// 改行文字が含まれているかの確認
if (strchr(a, '\n') != NULL) {
    // 改行文字を終端記号に置換する
    a[strlen(a) - 1] = '\0';
} else {
    // 入力ストリームをクリアする
    while(getchar() != '\n');
}
```

入力ストリームは改行文字を読むまで [getchar](https://ja.wikipedia.org/wiki/getchar "wikilink")関数を繰り返して呼び出すことで実現している。ちなみに本格的にセキュリティを考慮する場合には上記のコードにさらにストリームクリア時にエラーが発生した場合などの処理も加える必要があるが本稿の趣旨と外れるのでここでは割愛する。

### sscanf との連携

fgets は文字列を読み込む関数なので、当然ながら scanf の数値入力に対してそのまま置き換えることは出来ない。このような場合は fgets でまず文字列として取り込んだ後、[sscanfを用いて入力することで置き換えることが出来る](https://ja.wikipedia.org/wiki/scanf#関連する関数 "wikilink")。例えば

``` c
int i;

if (scanf("%d", &i) != 1) {
    // エラー処理
}
```

となるようなコードは

``` c
int i;
char temp[128]; // サイズはとりあえず適当に置いておく

fgets(temp, 128, stdin);
// バッファクリアの処理は省略

if (sscanf(temp, "%d", &i) != 1) {
    // エラー処理
}
```

とすることで置き換えることが出来る。ただし、このように置き換えた場合には読み込むバッファの長さが十分であるという事を考慮しなければならない。また複数の数値を読み込む書式ではエラー処理のパターンが異なる（[scanf\#異常な入力が行われた時の処理](https://ja.wikipedia.org/wiki/scanf#異常な入力が行われた時の処理 "wikilink")を参照）ため、その事を十分認識しておく必要がある。

## 関連項目

  - [標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")
  - [gets](https://ja.wikipedia.org/wiki/gets "wikilink")
  - [fputs](https://ja.wikipedia.org/wiki/fputs "wikilink")
  - [scanf](https://ja.wikipedia.org/wiki/scanf "wikilink")

## 脚注

## 外部リンク

  -
[Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink")

1.
2.  <http://www.kouno.jp/home/c_faq/c12.html#20>