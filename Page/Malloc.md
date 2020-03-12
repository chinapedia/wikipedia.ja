> この記事は[Malloc](https://ja.wikipedia.org/wiki/Malloc)から翻訳されています。


**malloc**（マロック, エムアロック）、**calloc**、**realloc**は、[動的メモリ確保](../Page/動的メモリ確保.md "wikilink")を行う[C言語](../Page/C言語.md "wikilink")の[標準ライブラリの](../Page/標準Cライブラリ.md "wikilink")[関数である](../Page/サブルーチン.md "wikilink")\[1\]\[2\]\[3\]。確保したメモリの解放には**free**関数を使用する。

`malloc`が使用する実際のメモリ確保機構には様々な実装がある。それらの性能は、実行時間と要求されるメモリの両面で様々である。

## 原理

[C言語](../Page/C言語.md "wikilink")は通常[メモリを](../Page/記憶装置.md "wikilink")「静的メモリ確保」か「自動メモリ確保」で管理する。静的変数は主記憶上にプログラムが存在する期間中ずっと確保されている。自動変数（[局所変数](https://ja.wikipedia.org/wiki/局所変数 "wikilink")）は通常[コールスタック](https://ja.wikipedia.org/wiki/コールスタック "wikilink")上に確保され、対応するサブルーチンが実行中の間だけ存在する。しかし、いずれの方法も限界があり、確保できるメモリ量（変数のサイズ）は[コンパイル時に決められてしまう](../Page/コンパイラ.md "wikilink")。必要なサイズが実行時でないと判明しない場合、例えばディスク上のファイルから任意のサイズのデータを読み込むような場合、固定サイズのデータオブジェクトだけでは不十分である。

確保されたメモリの生存期間（使用可能期間）も問題となる。静的でも自動的でも確保されたメモリの生存期間はあらゆる状況に対応できるものではない。スタック上のデータは複数の関数呼出をまたいで持続できないし、静的データは必要かどうかに関わらずプログラムが動作中ずっとメモリ領域を確保し続ける。しかし、そうではなく確保したメモリの生存期間をプログラマが自由に制御できる必要がある場合も多い。

これらの制限は[動的メモリ確保](../Page/動的メモリ確保.md "wikilink")を使用することで解決する。メモリの管理は明示的に行う必要が出てくるが、柔軟性が向上する。「[ヒープ領域](../Page/ヒープ領域.md "wikilink")」はこのために用意されたメモリ領域である。C言語では、`malloc`関数を使ってヒープ領域からメモリブロックを確保する。プログラムは`malloc`の[戻り値](https://ja.wikipedia.org/wiki/戻り値 "wikilink")である[ポインタを使って](../Page/ポインタ_\(プログラミング\).md "wikilink")、そのメモリブロックにアクセスする。メモリブロックが不要になったら、そのポインタを`free`に渡して解放し、他の用途に再利用できるようにする。

ヒープではなくCのスタックフレームから実行時に動的にメモリを確保するライブラリルーチンもある（[Unix系](../Page/Unix系.md "wikilink")の `alloca()`\[4\]、[Microsoft Visual C++におけるCランタイムライブラリの](../Page/Microsoft_Visual_C++.md "wikilink") `_malloca()`\[5\] など）。このように確保したメモリは呼び出した関数から抜ける時点で自動的に解放される。ただし、[スタックオーバーフロー](../Page/スタックオーバーフロー.md "wikilink")に注意する必要がある。[GCC言語拡張の](../Page/GNUコンパイラコレクション.md "wikilink")[可変長配列](../Page/可変長配列.md "wikilink")が[C99](../Page/C99.md "wikilink")標準でサポートされ\[6\]、実行時に大きさを決定でき任意の[静的スコープ](../Page/静的スコープ.md "wikilink")の範囲で存在するメモリ確保法が言語構文に組み込まれたが、[C11ではサポート必須ではなくオプションに格下げとなった](https://ja.wikipedia.org/wiki/C11_\(C言語\) "wikilink")。

## C言語での動的メモリアロケーション

`malloc`はC言語におけるヒープ領域からのメモリ確保に使われる基本関数である。その[関数プロトタイプ](https://ja.wikipedia.org/wiki/関数プロトタイプ "wikilink")は`stdlib.h`ヘッダに次のように定義されている\[7\]。

`void *malloc(size_t `<var>`size`</var>`)`

ここで、<var>`size`</var>バイトのメモリが確保される。確保が成功するとそのメモリブロックへのポインタが返される。

ANSI Cにおいて`malloc`が返すのは、[void型へのポインタ](https://ja.wikipedia.org/wiki/void_\(コンピュータ\) "wikilink") (`void *`) であり、そのポインタが指す領域のデータ型が不明であることを示している。C言語では汎用ポインタ`void *`と任意の型`T`へのポインタ`T *`との間の[型変換](../Page/型変換.md "wikilink") (キャスト) は暗黙的に実行されるため、`malloc`の戻り値は特に明示的な型変換を記述せずとも任意の型へのポインタ変数にそのまま代入できる。しかし、明示的に型変換を記述する必要が無いにもかかわらず、あえて意図的に型変換を記述することもある。明示的に型変換を記述する目的は、かつてANSI以前の仕様のC（K\&R C）においては、`void *`が存在せず、`malloc`は`char *`を返していたからである\[8\]\[9\]。また、C言語よりも厳密な型システムを持つ[C++](../Page/C++.md "wikilink")では、`T *`から`void *`への型変換は暗黙的に行なわれるものの、`void *`から`T *`への型変換は暗黙的に行なわれないため、C/C++両方でコンパイルすることのできるソースコードを書く際には型変換の記述が必要となる。

``` c
int *ptr = (int *)malloc(sizeof(int) * 10);
```

しかし、`stdlib.h`をインクルードし忘れた場合（`malloc`関数の[前方宣言](https://ja.wikipedia.org/wiki/前方宣言 "wikilink")がない場合）、Cコンパイラは`malloc`が`int`型を返す関数であるとみなす。`malloc`の戻り値を明示的に型変換していると、ヘッダーをインクルードし忘れたことに気づかない。一方、明示的に型変換していないと、コンパイル時に`int`をポインタ型変数に代入しようとしているとして何らかの警告あるいはエラーメッセージがコンパイラから表示されることでインクルード忘れに気づける可能性がある\[10\]\[11\]\[12\]。例えば[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")のシステムでLP64というデータモデルを採用している場合、`long`とポインタは64ビットだが、`int`は32ビットとなる。この場合`stdlib.h`のインクルード忘れに気づかないと、`malloc`が実際には64ビットのポインタを返すのに、32ビットの値を返すと暗に宣言したことになり、バグが生じる可能性がある。ただし、多くのコンパイラは宣言のない関数を使用していると（キャストの有無にかかわらず）コンパイル時に警告を出す。

### メモリの解放

`malloc`で確保されたメモリは持続性がある。プログラム終了時か明示的にプログラマが解放しない限り存在し続ける。解放は`free`関数で行われる。そのプロトタイプは次のようになる。

`void free(void *`<var>`pointer`</var>`)`

ここで、<var>`pointer`</var>の指すメモリブロックが解放される。

## 関連する関数

`malloc`はメモリブロックを確保して返すが、その領域は初期化されていない。必要に応じてメモリは個別に初期化する。例えば、[`memset`](https://ja.wikipedia.org/wiki/memset "wikilink")関数で初期化したり、個別の代入文で初期化したりする。他にも`calloc`（カロック、シーアロック）関数を使って、メモリ確保と初期化を行うこともできる。そのプロトタイプは以下のようになる。

`void *calloc(size_t `<var>`nelements`</var>`, size_t `<var>`bytes`</var>`)`

<var>`bytes`</var>のサイズのメモリ領域を<var>`nelements`</var>個格納できるメモリ領域を確保する。確保された領域はゼロで初期化される。

メモリブロックを大きくしたり小さくしたりできれば便利である。これは`malloc`と`free`を組み合わせて、新たなメモリブロックを確保して内容を前のメモリブロックからコピーし、前のメモリブロックを解放することで実現できる。しかし、この方法は回りくどい。代わりに`realloc`（リアロック）関数を使うことができる。そのプロトタイプは以下の通りである。

`void *realloc(void *`<var>`pointer`</var>`, size_t `<var>`bytes`</var>`)`

`realloc`は指定されたサイズのメモリ領域へのポインタを返す。新しいサイズが前のサイズより大きければブロックは大きくされ、逆ならば小さくされる。

`valloc`は`malloc`とほとんど同じだが、メモリ確保がページ境界になる点が異なる。`valloc`で確保された領域へのポインタを`realloc`に渡すことはできない[1](https://www.mkssoftware.com/docs/man3/valloc.3.asp)。また、これは標準Cライブラリに含まれる関数ではない。

## 使用例

スタック上に10個の整数の[配列](../Page/配列.md "wikilink")を作成する一般的な方法は次の通りである。

``` c
int array[10];
```

同様の配列を動的に確保するには、以下のように`malloc`を使う。

``` c
#include <stdlib.h>

/* 10個のintの配列のためのメモリを確保 */
int *ptr = malloc(sizeof(int) * 10);
if (NULL == ptr) {
    exit(EXIT_FAILURE); /* メモリを確保できなかったので終了 */
} else {
    /* 確保成功 */
    /* ここでその配列を使った処理を行う */

    /* 処理が完了し、使わなくなったメモリブロックを解放する */
    free(ptr);
    /* 解放したメモリにアクセスしてはならないことを示すため、NULLを代入しておく */
    ptr = NULL;
}
```

## 一般的なエラー

`malloc`および関連するC言語の関数の使用は[バグ](../Page/バグ.md "wikilink")の発生源になりやすい。

### 確保エラー

`malloc`は必ず成功するとは限らない。利用可能な空きメモリ領域がないとき、プログラムが限界値を超えてメモリを使用しようとしたときなど、`malloc`は[ヌルポインタ](https://ja.wikipedia.org/wiki/ヌルポインタ "wikilink")を返す。環境によって、このような状況の起きる可能性は異なる。もし`malloc`が失敗することを考慮していないプログラムで、`malloc`がヌルポインタを返してきたとき、プログラムはNULLに相当するアドレスにアクセスしてクラッシュするだろう。メモリ確保失敗をチェックすることは、ライブラリでは特に重要である。ライブラリはメモリ量が限られた状況でも使用される可能性がある。ライブラリ内でメモリ確保に失敗した場合、呼び出したアプリケーション側にエラーを通知して、アプリケーションプログラムに判断を委ねるのがよいとされる。

プロトタイピング目的で書かれたコードなどでは、メモリ確保失敗をチェックしないこともある。というのもメモリ確保に失敗するという状況は、[画像処理](../Page/画像処理.md "wikilink")などを除いた一般的な用途では珍しく、発生した場合には終了する以外にプログラミング上できることがないからでもある。ごく少量のメモリさえ確保に失敗するような状況では、メモリ確保失敗に対処したとしてもプログラムを正常に続行できる見込みがない。一方で、ライブラリ製品やアプリケーション製品では異常系すなわち例外処理への対処は重要であり、メモリ確保失敗への対処も例外ではない。

### メモリリーク

`malloc`で確保したメモリブロックを使用しなくなっても`free`で解放せず、次々と新たなメモリブロックを確保していると空きメモリが少なくなってくる。これを[メモリリーク](../Page/メモリリーク.md "wikilink")と呼ぶ。メモリリークによるメモリ消費が無視できない量に達すると[ページ置換アルゴリズム](../Page/ページ置換アルゴリズム.md "wikilink")によってページアウトが発生し、システム性能が低下する。さらに仮想記憶の容量限界に達すると、システム内の他の全プロセスでメモリ確保が失敗してシステムがストールする。メモリリークは、利用のたびにプロセスの起動・終了が行われるプログラムにおいて、特に重要な問題を引き起こさないため、メモリリークが混入した状態で出荷される商用プログラムは多い。しかしながら、連続稼動が要求される[サーバ](../Page/サーバ.md "wikilink")コンピュータ上のプログラム（[サービス](../Page/サービス.md "wikilink")、[デーモン](../Page/デーモン_\(ソフトウェア\).md "wikilink")）や、[組み込み](https://ja.wikipedia.org/wiki/組み込み "wikilink")プログラム等の場合は、メモリリークは死活問題とされる。

### 解放後の使用

ポインタが`free`関数に渡され、メモリが解放された後でその領域への参照を行っても、その内容は未定義であり利用できない。しかし、ポインタ自体が残っていると誤って使ってしまうことがある。次のコードはその例である。

``` c
int *ptr = malloc(sizeof(*ptr)); /* メモリ領域を動的確保 */
...
free(ptr);
/* ptr は解放済みの領域をまだ指したまま */
*ptr = 0; /* 何が起きるかわからない！ */
```

このようなコードは予測不能の振る舞いをする。メモリが解放された後でシステムがその領域を他の用途に転用しているかもしれない。従って解放済みメモリ領域へのポインタ（ダングリングポインタ; dangling pointer）を使った書き込みはプログラム内の別のデータを不正に書き換えてしまう。どういうデータを書き換えたかによって、その後のプログラムの動作も異なる。単なるデータ破壊で済むかもしれないし、クラッシュするかもしれない。特に破壊的なバグとしては、同じポインタを2回`free`関数に渡してしまうことであり、これを「二重解放; double free」と呼ぶ。これを防ぐため、解放した後でポインタ変数に`NULL`を格納することがある。ポインタ変数が無効な領域を指しているかどうかを後で調べるとき、`NULL`が格納されているかどうかで簡単に判定できるようになる。また、`free(NULL)`は何もしないことが規格で保証されているので、`NULL`を代入しておけば（`free`関数を再度呼んだとしても）二重解放の危険はない。この技法は寿命の長い[グローバル変数](../Page/グローバル変数.md "wikilink")でポインタを定義する場合は必須だが、寿命の短い[ローカル変数](../Page/ローカル変数.md "wikilink")でポインタを定義する場合でも[フールプルーフ](https://ja.wikipedia.org/wiki/フールプルーフ "wikilink")のために用いることができる。

``` c
int *ptr = malloc(sizeof(*ptr));
...
free(ptr);
ptr = NULL;
```

## 実装

メモリ管理の実装はオペレーティングシステム (OS) と（ハードウェア）アーキテクチャに大きく依存する。OSによってはmallocのためのアロケータを提供しているし、データ領域の制御関数を提供している場合もある。

同じ動的メモリアロケータでmallocだけでなく[C++](../Page/C++.md "wikilink")の `operator new` も実装していることが多い。そこでこれを malloc ではなく「アロケータ」と呼ぶ。

### ヒープ方式

[IA-32](../Page/IA-32.md "wikilink")アーキテクチャでのアロケータの実装には一般に[ヒープまたはデータセグメントが使用されている](../Page/ヒープ領域.md "wikilink")（[セグメント方式](../Page/セグメント方式.md "wikilink")）。 アロケータがメモリを確保するとき、ヒープに未使用領域がない場合はヒープを拡張することでメモリを確保する。

ヒープ方式は[フラグメンテーション](../Page/フラグメンテーション.md "wikilink")という問題がある。どのようなメモリ確保方式でもヒープではフラグメントが発生する。つまり、ヒープ上に飛び飛びに使用中領域と未使用領域が存在することになる。優秀なアロケータはヒープを拡張する前に未使用領域を再利用しようとする。しかし性能問題があるため、リアルタイムシステムでは代わりに「メモリプール」という方式を使う必要がある（特定サイズのメモリブロックのプールを予め用意しておく方式）。

ヒープ方式の欠点は、先頭位置が変更できないため、ヒープの最後の位置に使用中ブロックがある限り、ヒープを縮小することができないことである。従って、このような時は実際に使用しているメモリが少ないのにも関わらず、ヒープのアドレス空間に占める領域が拡大し続けるという問題が生じる。

[mmap](https://ja.wikipedia.org/wiki/mmap "wikilink")で確保した領域は、縮小したり開放したりすることができる。これらによって開放された領域は、OSのメモリ管理システムに委ねることになる。

### dlmalloc

[dlmalloc](http://g.oswego.edu/dl/html/malloc.html) は Doug Lea が[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")に開発を始めた汎用アロケータ。[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")ライセンス（CC0ライセンス）の[オープンソース](../Page/オープンソース.md "wikilink")ライブラリ。[GNU Cライブラリ](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink") (glibc) の malloc は、dlmalloc を元に作られている\[13\]。

ヒープ領域上のメモリは "chunk" という8バイト境界の[データ構造](../Page/データ構造.md "wikilink")として確保され、その中にヘッダ部と利用可能なメモリがある。chunk および利用中フラグがあるため、8バイトまたは16バイトのオーバヘッドを含めたメモリ確保が必要である。アロケートされていないchunkも他のフリーなchunkへのポインタを持つため、chunkの最小サイズは24バイトとなっている\[14\]。

アロケートされていないメモリは "bin" と呼ばれる同じサイズのchunkのグループに分けて管理される。binはchunkを双方向連結リストで連結したものである。

小さな領域 (\<256B) を確保するときには[2の累乗フリーリストが使われる](https://ja.wikipedia.org/wiki/動的メモリ確保#固定サイズブロック・アロケーション "wikilink")。領域が不足したときは、より大きなサイズ用の領域からプールを確保する\[15\]。

中程度の大きさの領域は、bitwiseトライ木により管理される。領域が不足したときは、（[sbrkによる](https://ja.wikipedia.org/wiki/brk "wikilink")）ヒープの拡張が行われる。

大きな領域(デフォルト値は \>= 256KB\[16\])は、[mmap](https://ja.wikipedia.org/wiki/mmap "wikilink")() が使える環境の場合、mmap() により直接確保される。この大きさならば、ページサイズ(通常4KB\[17\], CPUのアーキテクチャに依存する)単位でしか割り当てられないことによるオーバーヘッド、システムコールの遅さによるオーバーヘッドはほとんどない。一方で、先に述べたヒープ方式のアロケーションの問題が起こらないので、この方法が使われる。

### FreeBSDとNetBSD

[FreeBSD](../Page/FreeBSD.md "wikilink") 7.0以降と [NetBSD](../Page/NetBSD.md "wikilink") 5.0以降では、古い実装 (phkmalloc) をJason Evansが開発した[jemalloc](http://jemalloc.net/)に置換した。phkmalloc はマルチスレッド環境でのスケーラビリティに問題があった。[ロックの衝突を防ぐため](../Page/ロック_\(情報工学\).md "wikilink")、jemallocは[CPU](../Page/CPU.md "wikilink")毎に分離した "arena" と呼ばれる領域を用意する。実験によれば、スレッド数に比例して1秒間のmalloc回数が増えていくとき、phkmallocとdlmallocではスレッド数に反比例した性能を示した\[18\]。

### OpenBSD

[OpenBSD](../Page/OpenBSD.md "wikilink")の`malloc`関数の実装は`mmap`を使用している。ページサイズ以上の要求は`mmap`で行われ、ページサイズ未満なら`malloc`内で管理しているメモリプールから割り当てる。そのメモリプールも`mmap`で確保したものである。`free`を実行すると、`munmap`を使ってプロセスの[アドレス空間](../Page/アドレス空間.md "wikilink")からアンマップされて解放される。このシステムは[アドレス空間のレイアウトをランダム化することによってセキュリティを高めるための設計でもあり](https://ja.wikipedia.org/wiki/アドレス空間配置のランダム化 "wikilink")、OpenBSDの`mmap`が持つギャップページ機能も利用している（mmapで確保した領域が仮想空間上で隣接しないようにする機能）。また、解放後の領域は仮想空間としてマッピングが存在しないため、解放後のアクセスの検出も容易である（普通なら[セグメンテーション違反](../Page/セグメンテーション違反.md "wikilink")が発生してプログラムが終了する）。

### Hoard

は、スケーラブルなメモリ確保性能を目指したアロケータである。OpenBSDのアロケータと同様、Hoard は`mmap`のみを使用するが、64キロバイトのスーパーブロックと呼ばれる塊ごとにメモリを管理する。Hoardのヒープは論理的にグローバルな1つのヒープとプロセッサ毎のヒープに分けられている。さらにスレッド毎のキャッシュを持ち、制限された数のスーパーブロックを保持できる。確保はスレッド毎またはプロセッサ毎のヒープからのみ行い、解放されたスーパーブロックの多くはグローバルなヒープに戻して他のプロセッサが使えるようにする。このようにしてHoardではスレッド数に対してほぼ比例したスケーラビリティを維持しつつ、フラグメンテーションを最小に抑えている\[19\]。

### TCMalloc (thread-caching malloc)

スレッド毎に小さいメモリ確保のための領域を設ける。大きなメモリ確保にはmmapかsbrkを使用する。TCMallocは[Google](../Page/Google.md "wikilink")が開発したもので\[20\]、スレッドが終了した際にローカルな領域を掃除するガベージコレクション機能を備えている。マルチスレッド環境では、glibcのptmallocの2倍以上の性能を発揮するという\[21\]\[22\]。

### カーネル内

OSの[カーネル](../Page/カーネル.md "wikilink")でもアプリケーションと同様にメモリ確保が必要である。カーネル内にも`malloc`相当の関数はあるが、その実装はCライブラリのものとは大きく異なる。例えば、[DMA用のバッファには特別な制限が課せられることがあるし](../Page/Direct_Memory_Access.md "wikilink")、割り込み処理でメモリを動的に確保したい場合もある\[23\]。このため、カーネルの[仮想記憶](../Page/仮想記憶.md "wikilink")サブシステムと密に連携した `malloc` 実装が要求される。

## 最大確保サイズ

`malloc`が確保できるメモリブロックの最大サイズはシステムに依存する。特に物理メモリ量とOSの実装に依存する。理論上の最大値は`size_t`型（メモリ領域のサイズを表す符号なし整数）である。その最大値はか、C99標準の定数*SIZE_MAX*である。C言語標準は一回の確保で保証される最小値を提示している（[C89](https://ja.wikipedia.org/wiki/C89 "wikilink")では0x7FFF、[C99](../Page/C99.md "wikilink")では0xFFFF）。

## C++での利用

[C++](../Page/C++.md "wikilink")でも`malloc`関数は利用できるが、この利用は後述の問題を引き起こすため推奨されない。C++では言語の機能として[new演算子](https://ja.wikipedia.org/wiki/new演算子 "wikilink")、[delete演算子](https://ja.wikipedia.org/wiki/delete演算子 "wikilink")が用意されている\[24\]。`malloc`で確保したメモリ領域に対して`delete`したり、逆に`new`で確保した領域を`free`したりすると結果は未定義となる。`malloc`によって生まれたポインタと`new`によって生まれたポインタの混在はバグの温床であり、また、new/delete演算子と違い、malloc/free関数ではクラスの[コンストラクタ](../Page/コンストラクタ.md "wikilink")と[デストラクタ](../Page/デストラクタ.md "wikilink")が呼ばれないという違いもあり、C++での`malloc`は禁じ手の扱いである。

## 脚注

## 関連項目

  - [バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")
  - [メモリデバッガ](https://ja.wikipedia.org/wiki/メモリデバッガ "wikilink")
  - [メモリ保護](../Page/メモリ保護.md "wikilink")
  - [New演算子](../Page/New演算子.md "wikilink")

## 外部リンク

  - 英語ページ
      - [Definition of malloc in IEEE Std 1003.1 standard](http://www.opengroup.org/onlinepubs/9699919799/functions/malloc.html)

      - [Linux JMプロジェクト](https://ja.wikipedia.org/wiki/JM_Project "wikilink")

      - Gloger, Wolfram; [*The ptmalloc homepage*](http://www.malloc.de/en/index.html)

      - Berger, Emery; [*The Hoard homepage*](http://www.hoard.org/)

      - Douglas, Niall; [*The nedmalloc homepage*](http://www.nedprod.com/programs/portable/nedmalloc/)

      - Evans, Jason; [*The jemalloc homepage*](http://jemalloc.net/)

      - Berger, Emery; [*Hoard: A Scalable Memory Allocator for Multithreaded Applications*](https://people.cs.umass.edu/~emery/pubs/berger-asplos2000.pdf)

      - Michael, Maged M.; [*Scalable Lock-Free Dynamic Memory Allocation*](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.87.3870&rep=rep1&type=pdf)

      - [Memory Reduction (GNOME)](http://live.gnome.org/MemoryReduction) wiki page with lots of information about fixing malloc

      - [C99 standard draft, including TC1/TC2/TC3](http://www.open-std.org/jtc1/sc22/wg14/www/docs/n1256.pdf)

      - [Some useful references about C](http://paste.tclers.tk/1596)

      - [ISO/IEC 9899 – Programming languages – C](http://www.open-std.org/jtc1/sc22/wg14/www/standards)

      - ：dlmallocの仕組みを説明
  - 日本語の解説
      -   - Bartlett, Jonathan; [*Inside memory management* - The choices, tradeoffs, and implementations of dynamic allocation](http://www-106.ibm.com/developerworks/linux/library/l-memory/)：英語版

      -
[ru:Динамическое распределение памяти\#Язык программирования C (Си)](https://ja.wikipedia.org/wiki/ru:Динамическое_распределение_памяти#Язык_программирования_C_\(Си\) "wikilink")

[Category:メモリ管理](https://ja.wikipedia.org/wiki/Category:メモリ管理 "wikilink") [Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.  [C FAQ 日本語訳 7.7](http://www.kouno.jp/home/c_faq/c7.html#7)
10. [C FAQ 日本語訳 7.6](http://www.kouno.jp/home/c_faq/c7.html#6)
11.
12.
13.
14.
15.
16. <ftp://g.oswego.edu/pub/misc/malloc.c> の DEFAULT_MMAP_THRESHOLD
17.
18.
19.
20. [TCMalloc : Thread-Caching Malloc](https://gperftools.github.io/gperftools/tcmalloc.html)
21. Ghemawat, Sanjay; Menage, Paul; [*TCMalloc : Thread-Caching Malloc*](https://gperftools.github.io/gperftools/tcmalloc.html)
22.
23.
24.