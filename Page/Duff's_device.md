> この記事は[Duff\'s device](https://ja.wikipedia.org/wiki/Duff\'s_device)から翻訳されています。


**Duff's Device**（ダフスデバイス）とは、[C言語](../Page/C言語.md "wikilink")での可変長の連続的コピーを[ループ展開](https://ja.wikipedia.org/wiki/ループ展開 "wikilink")により[最適化](../Page/最適化_\(情報工学\).md "wikilink")[実装](https://ja.wikipedia.org/wiki/実装 "wikilink")するときに直面する端数の問題を解決するための手法である。

C言語の[switch-case文が持つフォールスルーを利用して](https://ja.wikipedia.org/wiki/switch文 "wikilink")、[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で行われる技巧をC言語で実現している。[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")11月、[ルーカスフィルム](https://ja.wikipedia.org/wiki/ルーカスフィルム "wikilink")で働いていたトム・ダフが発見した。

## 背景問題

ループ展開は、ループのための分岐回数を減らす技法である。指定されるループ回数が不明な場合、ループ展開すると回数が合わない場合が出てくるので、ループの途中にジャンプすることで調整する。例えば、8回ぶんのループを展開した場合、指定されたループ回数が8で割り切れないなら、その回数を8で割った剰余のぶんだけ処理を実行する位置にジャンプさせる。

ダフはそのような最適化を検討していてCでの技法を発見した。

## 本来のバージョン

連続コピーを普通にコーディングすると以下のようになる。

``` c
do {                          /* count > 0 と仮定 */
  *to = *from++;              /* ''to'' はインクリメントされていない */
} while (--count > 0);
```

ダフの本来の意図は[メモリマップされた周辺機器の出力レジスタへのコピーだったため](https://ja.wikipedia.org/wiki/メモリマップドI/O "wikilink")、`to` が[インクリメント](../Page/インクリメント.md "wikilink")されていない。

これを最適化するにあたり、ダフは、switch 文と do ループを組み合わせた構造によってループ展開ができると気づいた。

``` c
send(to, from, count)
register short *to, *from;
register count;
{
    register n = (count + 7) / 8;
    switch(count % 8) {
    case 0: do {    *to = *from++;
    case 7:     *to = *from++;
    case 6:     *to = *from++;
    case 5:     *to = *from++;
    case 4:     *to = *from++;
    case 3:     *to = *from++;
    case 2:     *to = *from++;
    case 1:     *to = *from++;
        } while(--n > 0);
    }
}
```

Duff's device は、8に限らずどのようなサイズのループ展開にも応用可能である。

## なぜ機能するのか

このアルゴリズム自体は[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")でコピーの際に比較と分岐を最小限にする手法として以前から使われていたが、Duff's Device はこれを C言語で実現した。このコーディングは次に挙げる2つのCの性質から、完全に有効で正当なCのコーディングである。

1.  C言語におけるswitch文の定義が緩やかである点。Duff's device が考案された当時のC言語の仕様は『[プログラミング言語C](https://ja.wikipedia.org/wiki/プログラミング言語C "wikilink")』に書かれていたもので、caseラベルの後には文法的に正しければどんな文も置くことができる仕様になっていた。そして、break文がないということはフォールスルーを望んでいることを意味する。
2.  C言語では、ループの途中にジャンプして入ることが可能である。

なお、最適化前のコード例のコメントにある通り、このコードでは `count` が正であることを前提としている。

## 性能

多くのコンパイラはswitch文を[ジャンプテーブルに最適化するので](../Page/テーブルジャンプ.md "wikilink")、アセンブリ言語での実装と変わらない性能をC言語で実装できる。C言語の case ラベルでの フォールスルー特性は長年に渡って議論となってきた。ダフは「このコードはその議論に何らかの影響を与えるだろう。しかし、それがどちらの立場になるのかはわからない」と述べている\[1\]。

単純なループよりこのコードが高速である主要因は[ループ展開](https://ja.wikipedia.org/wiki/ループ展開 "wikilink")によるものである。ループ展開によりループの終了条件の比較回数が減少する。switch/case 文はコピーすべき文字数の残りが展開されたコピー回数と必ずしも一致しないときの調整のために存在する（この例では、8バイトぶんのコピーが展開されている。したがって switch/case 文 は残りバイト数が 1 から 7 の時に自動的に調整する）。また分岐回数が減っていることも[パイプライン処理](https://ja.wikipedia.org/wiki/パイプライン処理 "wikilink")を行う[プロセッサ](../Page/プロセッサ.md "wikilink")においては、[パイプラインストールを起こす機会を少なくし高速化に貢献する](https://ja.wikipedia.org/wiki/パイプライン処理#制御ハザード "wikilink")。

このような剰余の自動処理は全てのシステムやコンパイラで最良な手段となるわけではない。場合によってはループを2つに分けたり（1つのループは展開されていて大部分のコピーを行い、2つめのループで残りのコピーを行う）、ループ展開をやめる方が高速である。コンパイラがこのコードを正しく最適化するかどうかも問題であるが、一部の[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")ではパイプラインや分岐予測がうまく働かないという指摘もある。かつて[XFree86](../Page/XFree86.md "wikilink")は Duff's device を多用していたが、バージョン4.0でそれらループ展開の大部分を排除して展開前の小さなループに戻すことで、キャッシュヒット率を向上させ性能を向上させたことがある\[2\]。したがって、このコードを使う前にいくつか[ベンチマーク](../Page/ベンチマーク.md "wikilink")を行って、対象アーキテクチャの対象コンパイラの対象最適化レベルで最も性能の良いコードを選ぶ方がよいだろう。

## ストロヴストルップのバージョン

本来のコードは（メモリにマップされた）1個のレジスタへのコピーであった。メモリからメモリへのコピーをするには `to` ポインタを以下のようにインクリメントしなければならない。

``` c
*to++ = *from++;
```

この修正版のコードは、[ビャーネ・ストロヴストルップ](../Page/ビャーネ・ストロヴストルップ.md "wikilink")の著書 ** で「このコードは何をしている？」という練習問題として登場した。これは初心者がメモリマップされた出力レジスタを知らない可能性があると判断したためだろう。しかし、このバージョンのコードはそれほど有用ではない。というのも[標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")には十分に最適化されたメモリコピー関数 (`memcpy`) が用意されているからである。そちらのコードの方がアーキテクチャ依存の最適化を施していて、ずっと高速に動作する\[3\]\[4\]。

## 脚注

## 関連書籍

  - [Stroustrup, Bjarne](../Page/ビャーネ・ストロヴストルップ.md "wikilink"), *The C++ Programming Language, Third Edition*. Addison-Wesley, ISBN 0-201-88954-4

  - [Kernighan, Brian](../Page/ブライアン・カーニハン.md "wikilink") and [Dennis Ritchie](../Page/デニス・リッチー.md "wikilink"), *[The C Programming Language](https://ja.wikipedia.org/wiki/プログラミング言語C "wikilink")*.

  -
## 外部リンク

  - [C言語FAQ20.35"ダフのデバイス(Duff's Device)"とは。](http://www.kouno.jp/home/c_faq/c20.html#35)
  - [Description and original mail by Duff at Lysator](http://www.lysator.liu.se/c/duffs-device.html)
  - [Wikipedia's example annotated at Stack Overflow](http://stackoverflow.com/questions/514118/514289#514289)
  - [Explanation from c-faq.com](http://c-faq.com/misc/duffexpln.html)
  - [Article at Dr.Dobb's Journal](http://drdobbs.com/web-development/184406208)
  - [Article at FOLDOC](http://foldoc.org/Duff's+device)
  - [Article at the Jargon File](http://www.catb.org/~esr/jargon/html/D/Duffs-device.html)
  - [Article at CodeMaestro](http://www.codemaestro.com/reviews/review00000102.html)
  - [Google copy of original USENET post](http://groups.google.com/group/net.lang.c/msg/66008138e07aa94c)
  - [Simon Tatham's coroutines in C](http://www.chiark.greenend.org.uk/~sgtatham/coroutines.html) 似たようなトリックを用いている

[Category:C言語](https://ja.wikipedia.org/wiki/Category:C言語 "wikilink") [Category:制御構造](https://ja.wikipedia.org/wiki/Category:制御構造 "wikilink") [Category:エポニム](https://ja.wikipedia.org/wiki/Category:エポニム "wikilink") [Category:プログラミング言語のトピック](https://ja.wikipedia.org/wiki/Category:プログラミング言語のトピック "wikilink")

1.  [Duff's device from FOLDOC](http://foldoc.org/index.cgi?Duff%27s+device)
2.  [Ted Tso on XFree86 and performance, Linux Kernel Archive ML](http://lkml.indiana.edu/hypermail/linux/kernel/0008.2/0171.html)
3.
4.