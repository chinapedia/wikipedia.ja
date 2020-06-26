> この記事は[B言語](https://ja.wikipedia.org/wiki/B言語)から翻訳されています。


**B言語**（**ビーげんご**）は、[AT\&Tベル研究所の](../Page/ベル研究所.md "wikilink")[ケン・トンプソン](../Page/ケン・トンプソン.md "wikilink") (Ken Thompson) によって開発された[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。ケン・トンプソンが[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")（Dennis Ritchie）監修の元で設計し、1969年頃に登場した\[1\]。

## 特徴

**B言語**は再帰に対応し、非数値型に対応し、特定の機種に依存しない言語であり、OSや他の言語などを開発するための言語として設計された\[2\] 。データ型を持たない言語で、ハードのCPUレジスタに対応した[ワード](../Page/ワード.md "wikilink")型1種類に依存し、どのようなビット長のCPUにも対応できた。文脈によりワードは[整数](../Page/整数.md "wikilink")または[アドレスとして扱われた](../Page/メモリアドレス.md "wikilink")。[ASCII](../Page/ASCII.md "wikilink")コードが一般的になり、当時ベル研究所にも[DEC PDP-11が導入され](../Page/PDP-11.md "wikilink")、文字データ型のサポートが重要になった。B言語のような型がない言語の仕様は欠点とみなされるようになり、トンプソンとリッチーは言語を拡張して内部型とユーザー定義型をサポートし、その言語は[C言語](../Page/C言語.md "wikilink")となった。

B言語で記述された[プログラムは](../Page/プログラム_\(コンピュータ\).md "wikilink")、[コンパイラ](../Page/コンパイラ.md "wikilink")によって[中間コード](https://ja.wikipedia.org/wiki/中間コード "wikilink")に変換され、実行には[インタプリタ](../Page/インタプリタ.md "wikilink")を必要とした。実行時に[インタプリタ](../Page/インタプリタ.md "wikilink")によって逐次処理されるため、実行速度は極めて遅かった。ただし[PDP-7](../Page/PDP-7.md "wikilink")版は[機械語](../Page/機械語.md "wikilink")を出力できるように改良された。

## 歴史

トンプソンは、[DEC社](https://ja.wikipedia.org/wiki/DEC社 "wikilink")製コンピュータ[PDP-7](../Page/PDP-7.md "wikilink")上で[UNIX](../Page/UNIX.md "wikilink")の開発を行っていたが、当時、[UNIX](../Page/UNIX.md "wikilink")上では[プログラムを](../Page/プログラム_\(コンピュータ\).md "wikilink")[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で記述することしかできなかった。そこでトンプソンは[UNIX](../Page/UNIX.md "wikilink")上で動作する[高級言語](https://ja.wikipedia.org/wiki/高級言語 "wikilink")の開発を始めた。トンプソンは[UNIX](../Page/UNIX.md "wikilink")の開発以前、[Multics](../Page/Multics.md "wikilink")の開発に携わっており、B言語は、[Multics](../Page/Multics.md "wikilink")上で動作していた[BCPL](../Page/BCPL.md "wikilink")を元に開発された。

B言語は本質的には、トンプソンがその時代の[ミニコンの](../Page/ミニコンピュータ.md "wikilink")[メモリ容量に収めるために](../Page/主記憶装置.md "wikilink")、不要と感じたコンポーネントを除去したBCPLシステムである。またトンプソンの好みに沿うような変更も行われた（たいていは、一般的なプログラムで空白以外の文字数を削減できるという方向であった\[3\]）。BCPLにあった[ALGOL](../Page/ALGOL.md "wikilink")由来の記法は大幅に改められた。代入演算子は、で採用された`:=`から、ALGOL開発メンバーの1人である[ハインツ・ルティスハウザー](https://ja.wikipedia.org/wiki/ハインツ・ルティスハウザー "wikilink")がかつてSuperplanで採用していた`=`に戻され、また比較演算子は`=`から`==`へ置き換えられた。

トンプソンは加減算代入演算子を発明し、`x =+ y`の形で実装した(C言語では順序が逆転して`+=`となった)。またB言語ではインクリメント、デクリメント演算子(`++` and `--`)が導入された。演算子を前につけるか後ろにつけるかで、変更前と変更後のどちらの値が式の結果に適用されるのかを選択できた。これらの新機能は最初のバージョンのB言語には見られなかった。デニス・リッチーによれば、多くの人はDEC PDP-11で導入された自動インクリメント・自動デクリメント・アドレッシングモードのために開発されたと思う人が多いが、Bが開発されたときにはPDP-11は存在しておらず歴史的に見てありえないとしている\[4\]。

[BCPL](../Page/BCPL.md "wikilink")や[Forth](../Page/Forth.md "wikilink")と同じくB言語はマシンのワード長である1つのデータ型のみを持っていた。多くの[演算子](../Page/演算子.md "wikilink")（例えば`+`、`-`、`*`、`/`）ではこれを整数として扱い、それ以外は[ポインタとして扱った](../Page/ポインタ_\(プログラミング\).md "wikilink")。それ以外の部分についてはC言語の初期バージョンとよく似ていた。C言語の[標準入出力ライブラリを彷彿とさせる](https://ja.wikipedia.org/wiki/標準Cライブラリ#入出力_\<stdio.h\> "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")がわずかながら存在していた\[5\]。

初期の頃は、初期の[UNIX](../Page/UNIX.md "wikilink")を使用した[DEC社](https://ja.wikipedia.org/wiki/DEC社 "wikilink")の[PDP-7](../Page/PDP-7.md "wikilink")用と[PDP-11](../Page/PDP-11.md "wikilink")用の実装があり、また[GCOS](../Page/GCOS.md "wikilink")というOSが動作する[ハネウェル](../Page/ハネウェル.md "wikilink")の36[ビット](../Page/ビット.md "wikilink")[メインフレーム](../Page/メインフレーム.md "wikilink")の実装もあった。最初にPDP-7用の[スレッデッドコード](https://ja.wikipedia.org/wiki/スレッデッドコード "wikilink")を出力する実装が開発され、次にリッチーがマシン語を出力するコンパイラをで実装した\[6\]\[7\]\[8\]。1970年にPDP-11が開発現場に導入され、スレッデッドコード版がPDP-11に移植された。アセンブラのdcとB言語自身はB言語で記述された。最初の[yacc](https://ja.wikipedia.org/wiki/yacc "wikilink")がこのPDP-11用に開発された。リッチーはこの時期にメンテナンスを引き受けていた\[9\]。

B言語の型のない設計はハネウェルやPDP-7などの多くの古いコンピュータでは意味のあることであったが、PDP-11以降のほぼ全てのコンピュータがサポートしている8ビットの[キャラクタデータ型にエレガントにアクセスすることが難しいことが問題になった](../Page/キャラクタ_\(コンピュータ\).md "wikilink")。リッチーは1971年に言語の変更を開始し、コンパイラがマシン語を出力するように変換すると同時に、最も顕著な拡張としてデータ型を変数に追加した。1971年から1972年にかけてB言語はNew B言語へ進化し、そしてアラン・スナイダー(Alan Snyder)の強い要求によって[プリプロセッサ](../Page/プリプロセッサ.md "wikilink")が加えられ、1972年から1973年の初期にC言語となった\[10\]。

1973年の夏の間にPDP-11用のUNIXがC言語で書き直され、一連の努力が成し遂げられた。1972～73年の間にハネウェル635とIBM [360](https://ja.wikipedia.org/wiki/System/360 "wikilink")/370に移植する必要があり、マイク・レスク(Mike Lesk)は後にC言語の標準入出力ライブラリとなる「汎用的なI/Oパッケージ」を書いた。

B言語は[C言語](../Page/C言語.md "wikilink")にほぼ置き換わった\[11\]。B言語はハネウェルのメインフレームGCOSで1990年代頃まで利用され続けていた\[12\]。また、小型システムの限定されたハードウェアを利用するためであったり、大規模なライブラリやツールやライセンスの問題、また単純に業務に必要十分であるからなどのような様々な理由により、一部の[組み込みシステム](../Page/組み込みシステム.md "wikilink")でも利用されていた\[13\] 。非常に大きな影響力のあった[AberMUDはB言語で記述されていた](../Page/MUD.md "wikilink")。

## コードの例

ケン・トンプソンによる*Users' Reference to B*より\[14\]

``` c
/* 以下の関数は負でない整数nをb進数の形で出力する（ただし2<=b<=10）。
   このルーチンはASCIIキャラクタのコードの値が
   0から9まで連続しているということを利用している。*/

printn(n, b) {
        extrn putchar;
        auto a;

        if (a = n / b)        /* 代入文であり、比較演算子ではない*/
                printn(a, b); /* 再帰 */
        putchar(n % b + '0');
}
```

``` c
/* 次のプログラムはネイピア数の小数点以下の部分を4000桁まで計算し、
   1行5文字のグループに分けて50文字を出力する。
   この手法は以下を単純に拡張した物であり、
     1/2! + 1/3! + ... = .111....
   それぞれ2桁、3桁、4桁…に対応する。 */

main() {
    extrn putchar, n, v;
    auto i, c, col, a;

    i = col = 0;
    while(i<n)
        v[i++] = 1;
    while(col<2*n) {
        a = n+1 ;
        c = i = 0;
        while (i<n) {
            c =+ v[i] *10;
            v[i++]  = c%a;
            c =/ a--;
        }

        putchar(c+'0');
        if(!(++col%5))
            putchar(col%50?' ': '*n');
    }
    putchar('*n*n');
}
v[2000];
n 2000;
```

## 脚注

## 参考文献

## 外部リンク

  - *[The Development of the C Language](http://www.bell-labs.com/usr/dmr/www/chist.html)*, [Dennis M. Ritchie](../Page/デニス・リッチー.md "wikilink"). [BCPL](../Page/BCPL.md "wikilink")と[Cとの関係の中でBを語っている](../Page/C言語.md "wikilink")。
  - *[Users' Reference to B](http://www.bell-labs.com/usr/dmr/www/kbman.html)*, Ken Thompson. Describes the [PDP-11](../Page/PDP-11.md "wikilink") version.
  - *[The Programming Language B](http://www.bell-labs.com/usr/dmr/www/bintro.html)*, S. C. Johnson & B. W. Kernighan, Technical Report CS TR 8, [Bell Labs](../Page/ベル研究所.md "wikilink") (January 1973). [ハネウェル](../Page/ハネウェル.md "wikilink")の製品用の[GCOS](../Page/GCOS.md "wikilink")バージョン。
  - *[C言語の起源をめぐって](http://nanyanen.jp/comp/corigin.html)* 戸田孝 2006年11月

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.