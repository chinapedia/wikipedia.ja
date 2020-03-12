> この記事は[Rand](https://ja.wikipedia.org/wiki/Rand)から翻訳されています。


**rand**は、引き続く呼び出しが[擬似乱数](../Page/擬似乱数.md "wikilink")列を返すような[関数に付けられる名前である](../Page/サブルーチン.md "wikilink")。**ランド**、**ランダム**と呼ばれている。以下、主に[標準Cライブラリ](../Page/標準Cライブラリ.md "wikilink")のそれについて説明する。

## 概要

以下、基本的に[C99](../Page/C99.md "wikilink")に従う。

[C言語](../Page/C言語.md "wikilink")の[ヘッダーファイル](https://ja.wikipedia.org/wiki/ヘッダーファイル "wikilink") stdlib.h で宣言されている、0以上かつ[定数](../Page/定数.md "wikilink")`RAND_MAX`以下（数学で使う「以上」「以下」であり両端を含む）の[整数](../Page/整数.md "wikilink")値を返す[関数である](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")。標準ではマルチスレッドについて触れられておらず、[POSIX](../Page/POSIX.md "wikilink")ではスレッドセーフに実装することを要求していない\[1\]。

また、標準は、randが生成すべき乱数列の品質など、乱数列の乱数性については何も言及していない。当然[移植性](../Page/移植性.md "wikilink")は保証されない。

## 初期化

randの引き続く呼び出しが返す乱数列はsrandで初期化される。srandを呼び出さずにrandを使った場合は、最初に引数を1としてsrandを呼び出した場合と同じように動作しなければならない。srandに相当するステートメントが、一部の[BASIC](../Page/BASIC.md "wikilink")でRANDOMIZEという名前であったため**ランダマイズ**と呼ばれることもあるが、「 (種子)」を与えているだけで、何かをランダムにしているわけではない。

実行ごとに異なる乱数列を生成するために、簡便な手法としては時刻などが使われる（後述のコード例を参照）。暗号などの応用では外部から予測が不可能（ないし十分に困難）な方法を使わなければならない。逆に、シミュレーションを再現するなどの用途では、同じ乱数シードを使用して同じ乱数列を返すようにする。

srandは乱数**列**に種子を与え初期化するものであるから、randを使用する度にsrandを呼んだりするのは、誤った用法である。

## randの問題点

古いrandの実装が生成する乱数列は、問題があるものがほとんどだったことが指摘されている\[2\]。のライブラリでは問題があるものはが、標準の規格書で示された実装例があまり良いものではなかったことや、古いライブラリと同じコードが使われ続けているものもまだあることから、注意を要する。

前述の規格書に示された例をはじめ、randの実装に[線形合同法](../Page/線形合同法.md "wikilink")が使われていることがあるので、線形合同法の欠点に注意する必要がある。詳細は[線形合同法\#短所](https://ja.wikipedia.org/wiki/線形合同法#短所 "wikilink")を参照すること。

ライブラリによっては、標準外だがより高品質のrandom、rand48等が用意されていることがある。本格的な用途には、[メルセンヌ・ツイスタ](../Page/メルセンヌ・ツイスタ.md "wikilink")等のより良い生成法を検討すべきである。

## srandとシードの問題点

srand()にtime()等で得た現在時刻 (秒単位) を渡して初期化する方法はよく見かけるが、srandの実装によってはシード値が近いとrandによって生成される乱数も相関性の高い値が出力されるものがある。つまり下記例のような実装方法を採るプログラムを起動してから数秒後に同じプログラムを起動すると最初のうちは同じ乱数列を得る可能性が高い。これを回避するためにはtimeで得た値を[ハッシュ関数](../Page/ハッシュ関数.md "wikilink")に通してからsrandに渡す、もしくはsrandを呼び出した後のrandは数十〜数百回読み飛ばすなどの対策が必要である。また言うまでもなく同じロジックを採用したプログラムが同一時刻に起動されるなどしてsrandが同一の値で初期化された場合は以降全く同じ乱数列を得ることになる。

## 形式

``` c
#include <stdlib.h>
int rand(void);
void srand(unsigned);
```

## コード例

``` c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main(void)
{
    int a;
    srand((unsigned int) time(0)); /* 現在時刻を取得して乱数シードを初期化する。 */
    a = (int)((rand() / ((double) RAND_MAX + 1.0)) * 10); /* [0, 9] の範囲の値のいずれかが返る。 */
    printf("%d", a);
    return 0;
}
```

出力結果の例:

`8`

特定の範囲で乱数を求めたいときには`a = rand() % 10`とする方法も広く知られているが、線形合同法などの下位ビットの乱数としての品質が低い生成法に備えるため、上記のコード例のように上位にあるビットを利用することが推奨されている\[3\]。とはいえ両コードともrandの質とは関係なく分布に偏りが発生する方法であり注意が必要である。

## 参考文献

## 外部リンク

  -
  - [Boost Random Number Library](http://www.boost.org/libs/random/) - [Boost](https://ja.wikipedia.org/wiki/Boost "wikilink") [C++](../Page/C++.md "wikilink")ライブラリのひとつ。様々な乱数アルゴリズムを使うことができる。

  - [Boost Random Number Library (cppll)](https://boostjp.github.io/archive/boost_docs/libs/random.html) - cppllによる上記の翻訳

[Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink") [Category:乱数](https://ja.wikipedia.org/wiki/Category:乱数 "wikilink")

1.  <http://pubs.opengroup.org/onlinepubs/009695399/functions/rand.html>
2.  [Random number generators: good ones are hard to find](http://dl.acm.org/citation.cfm?id=63042)
3.