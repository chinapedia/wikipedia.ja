> この記事は[C](https://ja.wikipedia.org/wiki/C)から翻訳されています。


**C言語**（シーげんご、）は、[1972年](https://ja.wikipedia.org/wiki/1972年 "wikilink")に[AT\&Tベル研究所の](https://ja.wikipedia.org/wiki/ベル研究所 "wikilink")[デニス・リッチー](https://ja.wikipedia.org/wiki/デニス・リッチー "wikilink")が主体となって開発した汎用[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。英語圏では「C language」または単に「C」と呼ばれることが多い。日本でも文書や文脈によっては同様に「C」と呼ぶことがある。[制御構文](https://ja.wikipedia.org/wiki/制御構文 "wikilink")などに[高水準言語](https://ja.wikipedia.org/wiki/高水準言語 "wikilink")の特徴を持ちながら、ハードウェア寄りの記述も可能な[低水準言語](https://ja.wikipedia.org/wiki/低水準言語 "wikilink")の特徴も併せ持つ。基幹系システムや、動作環境の資源制約が厳しい、あるいは実行速度性能が要求されるソフトウェアの開発に用いられることが多い。後発の[C++](https://ja.wikipedia.org/wiki/C++ "wikilink")や[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[C\#など](https://ja.wikipedia.org/wiki/C_Sharp "wikilink")、「C系」と呼ばれる派生言語の始祖でもある。[ANSI](https://ja.wikipedia.org/wiki/米国国家規格協会 "wikilink")、[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")、また[JISにより言語仕様が標準規格化されている](https://ja.wikipedia.org/wiki/日本産業規格 "wikilink")。

## 特徴

  - 汎用性が高い。プログラムの自由度が高く、また[機械語](https://ja.wikipedia.org/wiki/機械語 "wikilink")や[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")のような低水準言語と比較すると[ソースコード](https://ja.wikipedia.org/wiki/ソースコード "wikilink")の再利用性やメンテナンス性に優れており、目的に応じた拡張が容易であるため、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")や[アプリケーションソフトウェア](https://ja.wikipedia.org/wiki/アプリケーションソフトウェア "wikilink")・[ファームウェア](https://ja.wikipedia.org/wiki/ファームウェア "wikilink")の記述、[デバイスドライバ](https://ja.wikipedia.org/wiki/デバイスドライバ "wikilink")ー開発や機械制御など、あらゆる分野に適応している。
  - 対応する機器の範囲が広い。[パーソナルコンピュータ](https://ja.wikipedia.org/wiki/パーソナルコンピュータ "wikilink")はもちろん、自動車や家電の[組み込み用](https://ja.wikipedia.org/wiki/組み込みシステム "wikilink")[マイコンから](https://ja.wikipedia.org/wiki/マイクロコントローラ "wikilink")[スーパーコンピュータ](https://ja.wikipedia.org/wiki/スーパーコンピュータ "wikilink")まで、C言語を使用できるハードウェアは多様である。多目的性と、対応機器の多彩さのため、「コンピュータを使ってやること」は大抵、C言語で対応可能である。それゆえ、C言語のコード資産が蓄積されている環境は多岐に渡る。
  - 商用・非商用を問わず、採用ソフトウェア分野が広い。プログラム作成や[デバッグ](https://ja.wikipedia.org/wiki/デバッグ "wikilink")のための補助的なソフトウェア（[プログラミングツール](https://ja.wikipedia.org/wiki/プログラミングツール "wikilink")）が豊富である。
  - 機械語に変換するソフトウェア（[コンパイラ](https://ja.wikipedia.org/wiki/コンパイラ "wikilink")）などの開発環境が[CPU](https://ja.wikipedia.org/wiki/CPU "wikilink")に付属していたり無償だったりするものもあるため、ライセンス料の支払いをしなくても使用が始められる。
  - 開発時期が古いことから、文法に機械語の影響が強く、仕様自体は単純ではあるが明快ではなく難解である。この欠点を改良するためのちに開発された後発言語に比較し、プログラマが記述しなければならないことが多く、[低水準言語](https://ja.wikipedia.org/wiki/低水準言語 "wikilink")のように面倒で習得しにくい側面を持つ。
  - アマチュアからプロ技術者まで、プログラマ人口が多く、プログラマのコミュニティが充実している。C言語は使用者の多さから、正負の両面含め、プログラミング文化に大きな影響を及ぼしている。
  - 言語の適用先である[UNIX](https://ja.wikipedia.org/wiki/UNIX "wikilink")の場合、大抵のことが[スクリプト言語](https://ja.wikipedia.org/wiki/スクリプト言語 "wikilink")・[マクロプロセッサや](https://ja.wikipedia.org/wiki/マクロ_\(コンピュータ用語\)#マクロプロセッサ "wikilink")[フィルタやそれらの組み合わせで処理できるため](https://ja.wikipedia.org/wiki/フィルタ_\(ソフトウェア\) "wikilink")、うまく分野の棲み分けができていた面があった。仕様規格・派生言語も多く幅広い領域への移植の結果、適切でない分野にC言語が使われている場合もある。
  - C言語は[手続き型言語](https://ja.wikipedia.org/wiki/手続き型言語 "wikilink")である。[コンパイラ](https://ja.wikipedia.org/wiki/コンパイラ "wikilink")言語とOSを念頭に設計している。ハードウェアをある程度抽象化しつつも、必要に応じて[機械語](https://ja.wikipedia.org/wiki/機械語 "wikilink")や[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")のコードと同じことを実現できるようなコンピュータ寄りの言語仕様になっている。低水準な記述ができる高級言語とも、高級言語の顔をした低級言語とも言うことがある。
  - Cコンパイラは、移植の容易性、自由度、実行速度、コンパイル速度などを追求した。代わりにコンパイル後のコードの安全性を犠牲にしている。また、詳細を規格で規定せず処理系に委ねている部分が多く、C言語で書かれたソフトウェアでは処理系依存のコードが氾濫する原因となった。セキュリティー上の脆弱性や潜在的バグによる想定外の動作、コンパイラによる最適化の難しさといった問題を抱えており、最適化するとコンパイル速度が遅くなるなどの欠点が生じることがある。自動車分野では[MISRA CというC言語の部分集合](https://ja.wikipedia.org/wiki/MISRA_C "wikilink") (subset) を定義して、危険な機能の使用や記述を禁止するという制限を設けることでC言語を安全に利用するためのガイドラインを設けている。
  - [UNIX](https://ja.wikipedia.org/wiki/UNIX "wikilink")およびCコンパイラの移植性を高めるために開発してきた経緯から、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")[カーネル](https://ja.wikipedia.org/wiki/カーネル "wikilink")およびコンパイラ向けの低水準記述ができる。

### 機能と自由度

  - 文の区切りを終端記号 [セミコロン](https://ja.wikipedia.org/wiki/セミコロン "wikilink")「`;`」で表し、[改行文字にも](https://ja.wikipedia.org/wiki/改行コード "wikilink")[空白にも](https://ja.wikipedia.org/wiki/スペース "wikilink")[トークンの区切りとしての意味しか持たせない](https://ja.wikipedia.org/wiki/字句解析 "wikilink")「[フリーフォーマット](https://ja.wikipedia.org/wiki/フリーフォーマット_\(コンピュータ\) "wikilink")」という形式を採用している。中括弧`{ }`によるブロック構造および[スコープ](https://ja.wikipedia.org/wiki/スコープ "wikilink")をサポートする。
      - 記述作法についてはしばしば議論の対象となり、書籍も多数出版されている。
  - [ALGOL](https://ja.wikipedia.org/wiki/ALGOL "wikilink")の思想を受け継いで**[構造化](https://ja.wikipedia.org/wiki/構造化プログラミング "wikilink")**に対応している。手順を[入れ子構造で示して見通しの良い記述をすることができる](https://ja.wikipedia.org/wiki/ネスティング "wikilink")。原理的に**無条件分岐（[`goto`](https://ja.wikipedia.org/wiki/goto文 "wikilink")）**を使用する必要はなく、MISRA Cでは当初goto文を禁止していた。goto文を使わなければ、**[スパゲティプログラム](https://ja.wikipedia.org/wiki/スパゲティプログラム "wikilink")**と呼ばれる読みにくいプログラムになりにくい。
  - **[モジュール](https://ja.wikipedia.org/wiki/モジュール "wikilink")化**が[ファイルを単位として可能](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")。モジュール内だけで有効な名前を使うことが出来る[スコープ](https://ja.wikipedia.org/wiki/スコープ "wikilink")を持っている。
  - プログラムを[戻り値](https://ja.wikipedia.org/wiki/戻り値 "wikilink")つきの[サブルーチン](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")に分離できる。C言語ではこれを**[関数](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")**と呼び、関数内のプログラムコードでは、独立したスコープを持つ変数（[ローカル変数](https://ja.wikipedia.org/wiki/ローカル変数 "wikilink")）が使用できる。これにより、データの流れがブロックごとに完結するのでデバッグが容易になり、また関数の再帰呼び出しも可能となる。また、多人数での共同開発の際にも変数名の衝突が回避しやすくなる。なお、C言語ではUNIXのようなOSを前提としたホスト環境と、割り込み制御のようなOSを前提としないフリースタンディング環境とがある。ホスト環境では、プログラム開始直後に実行するプログラム要素を `main` という名前の関数として定義する\[1\]。プログラム中で再帰的に`main`関数を呼ぶことも可能（C++では不可能\[2\]\[3\]）。フリースタンディング環境では、エントリポイントと呼ばれるアドレスに置かれたコードをプログラムの開始点とするが、それがmain関数である必要はない。なお再帰呼び出しは、[スタックオーバーフロー](https://ja.wikipedia.org/wiki/スタックオーバーフロー "wikilink")の原因となるため、MISRA Cでは禁止している。

<!-- end list -->

  - システム記述言語として開発されたため、高級言語であるが[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")的な低水準の操作ができる。**[ポインタ演算](https://ja.wikipedia.org/wiki/ポインタ_\(プログラミング\) "wikilink")**、[ビット](https://ja.wikipedia.org/wiki/ビット "wikilink")ごとの[論理演算](https://ja.wikipedia.org/wiki/論理演算 "wikilink")、シフト[演算](https://ja.wikipedia.org/wiki/演算 "wikilink")などの機能を持ち、[ハードウェア](https://ja.wikipedia.org/wiki/ハードウェア "wikilink")に密着した処理を効率よく記述できる。これはオペレーティングシステムや[デバイスドライバ](https://ja.wikipedia.org/wiki/デバイスドライバ "wikilink")ーなどを記述する上では便利であるが、注意深く利用しないと発見しにくい[バグ](https://ja.wikipedia.org/wiki/バグ "wikilink")の原因となる。ライブラリ関数は、C言語規格が規定している関数と、OSが規定している関数との間の整合性、棲み分けなどが流動的である。MISRA Cのようないくつかの制約では、C言語規格が規定している関数の妥当性について指摘し、いくつかの関数を利用しないように規定している。

<!-- end list -->

  - ソースコードの記述に使う文字集合はANSI-C:1989(ISO/IEC 9899:1990)では[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")を標準としている。他の[ISO 646でも書けるように](https://ja.wikipedia.org/wiki/ISO_646 "wikilink")、3文字利用した[トライグラフ](https://ja.wikipedia.org/wiki/トライグラフ "wikilink")と呼ばれる表記法も存在する。その後、ISO/IEC 9899:1995 AMDなどでは[マルチバイト文字](https://ja.wikipedia.org/wiki/マルチバイト文字 "wikilink")セット対応の拡張を規定している。さらに、その後トライグラフは複数のコードを利用したシステムでしか利用がないため、より分かり易い2文字による[ダイグラフ](https://ja.wikipedia.org/wiki/ダイグラフ "wikilink")を規定している。
  - 組み込みの[整数型](https://ja.wikipedia.org/wiki/整数型 "wikilink")および[浮動小数点数](https://ja.wikipedia.org/wiki/浮動小数点数 "wikilink")型のほか、[構造体](https://ja.wikipedia.org/wiki/構造体 "wikilink")、[共用体](https://ja.wikipedia.org/wiki/共用体 "wikilink")、列挙体（[列挙型](https://ja.wikipedia.org/wiki/列挙型 "wikilink")）によるユーザー定義のデータ型や列挙定数をサポートする。構造体および共用体は[ビットフィールド](https://ja.wikipedia.org/wiki/ビットフィールド "wikilink")をサポートする。

### アセンブラとのインタフェース

  - 多くの処理系が[インラインアセンブラ](https://ja.wikipedia.org/wiki/インラインアセンブラ "wikilink")を搭載しているほか、アセンブラで出力したオブジェクトとのリンクが容易になっている。これにより速度が要求される部分だけを[アセンブリ言語](https://ja.wikipedia.org/wiki/アセンブリ言語 "wikilink")で記述するということが容易に行えることが多い。アセンブラとの[インタフェースは](https://ja.wikipedia.org/wiki/インタフェース_\(情報技術\) "wikilink")\#pragma asmなどを用いて局所化を図る努力はあるが、コンパイラごとに定義があり、CPUが同一であっても移植性が低い場合がある。

### コンパイラ仕様

  - コンパイラの処理が1パスで済む仕様になっている。ANSI-C:1989では宣言のない変数は`int`を想定することになっていた。ISO/IEC C:1999以降では[変数はその使用より前に宣言する必要がある](https://ja.wikipedia.org/wiki/変数_\(プログラミング\) "wikilink")。[関数の宣言がないと](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")、戻り値や引数を`int`型とみなす仕様は、が、型検査・型証明の仕組みが十分にないと不具合の原因になることがある。後継言語では記述によって先読みが必要になりうる。
  - マクロ記述やコンパイル条件の指定などが出来る前処理指令が標準化されている。前処理指令の解釈をする**[プリプロセッサ](https://ja.wikipedia.org/wiki/プリプロセッサ "wikilink")** (preprocessor) を持っている。プリプロセッサは、その名の通りコンパイル処理の前に自動的に実行される。コンパイラの機能として、プリプロセッサを通しただけの段階のソースコードを出力可能になっているものがある。前処理の結果を検査することで、設計者の意図と前処理の結果のずれがないか確認できる。

### 処理系の簡素化

処理系の簡素化のため、以下のように安全性を犠牲にした仕様が多い。なお、ホスト環境やプログラムの内容によっては、以下に対して脆弱性対策を施したとしても実行速度の低下が無視できる程度であることも多く、言語仕様側の欠点とみなされることも少なくない。

  - [配列](https://ja.wikipedia.org/wiki/配列 "wikilink")参照時の自動的な添字のチェックをしない
    これを要因とする代表的なバグが、固定長のバッファ領域をはみだしてデータの書き込みが行われてしまう「[バッファオーバーフロー](https://ja.wikipedia.org/wiki/バッファオーバーフロー "wikilink")」（[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")）である。標準ライブラリにはバッファオーバーフローを考慮していない関数があり、かつ多用されがちなため、しばしば[脆弱性](https://ja.wikipedia.org/wiki/脆弱性 "wikilink")の原因となる。また、プログラムにより明示的に制御（[動的メモリ確保](https://ja.wikipedia.org/wiki/動的メモリ確保 "wikilink")）することで[可変長配列](https://ja.wikipedia.org/wiki/可変長配列 "wikilink")の実現を可能にしているが、確保した領域の範囲外にアクセスしても自動的な伸長は行なわれない。
  - [文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")を格納するための特別な型が存在しない
    文字列には`char`型の配列を利用する。言語仕様上に特別な扱いはないが、[ヌル文字](https://ja.wikipedia.org/wiki/ヌル文字 "wikilink")（`'\0'`）を終端とする[文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")表現を使い、その操作をする[標準ライブラリ関数がある](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")。これは実質的にメモリ領域のポインタアクセスそのもので、固定長バッファに対して、それより長い可変長の文字列を書き込んでしまうことがあり、[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")の元凶の1つとなっている。後継言語では文字列処理を特に強化している場合が多く、標準ライブラリあるいは言語仕様による組み込みの文字列型を提供している。
  - 自動変数の自動的な初期化をしない
    自動変数（静的でないローカル変数）は変数の中でも最も頻繁に用いられる。初期化されていない変数を参照した場合、値は不定となるが、不定な値へのアクセスはであるので、[コンパイラ最適化](https://ja.wikipedia.org/wiki/コンパイラ最適化 "wikilink")の過程で想定しない形に改変することもある\[4\]。変数宣言・初期化の仕様による制限から、変数宣言の時点で初期化せず後で代入することで初期化に代えることが日常的で、誤って不定の値の変数を読み出す[バグ](https://ja.wikipedia.org/wiki/バグ "wikilink")を作り込みやすい。なお自動変数の自動とは 変数の領域の確保と開放が自動であるという意味であり、自動的に初期化されるという意味ではない。

### その他

  - ソースコード上の文字の大文字・小文字を区別する。
  - [入出力](https://ja.wikipedia.org/wiki/入出力 "wikilink")を含めほとんどの機能が、C言語自身で書かれた[ライブラリ](https://ja.wikipedia.org/wiki/ライブラリ "wikilink")によって提供される。このことは、C言語の機種依存性が低く、入出力関係ライブラリをのぞいた部分は[移植性](https://ja.wikipedia.org/wiki/移植性 "wikilink")（ポータビリティ）が高いことを意味する。さまざまな機種があるUNIXの世界でC言語が普及した理由のひとつである。
  - プログラムの実行に必要とする[ハードウェア](https://ja.wikipedia.org/wiki/ハードウェア "wikilink")資源が、アセンブラよりは多いが他の高級言語より少なくてすむため、現在さまざまな電化製品などの[組み込みシステム](https://ja.wikipedia.org/wiki/組み込みシステム "wikilink")でも使用されている。
  - 組み込み向けの場合は、プログラミング言語として、アセンブラ以外ではCとC++しか用意されていないことがある。その場合、他のプログラミング言語は、CやC++で書かれた処理系が存在すればコンパイルすることにより利用可能となることもあるが、メモリ制約などで動作しないことがある。
  - ANSI/ISOにより規格が標準化された後は言語仕様の変化が小さく安定していること、C言語のプログラマ人口やコード資産が多いこと、[C++](https://ja.wikipedia.org/wiki/C++ "wikilink")や[Objective-C](https://ja.wikipedia.org/wiki/Objective-C "wikilink")からC言語関数を直接利用できること、また必要に応じて他のプログラミング言語からC言語関数を呼び出すためのバインディングを記述することが容易であることなどから、[APIの外部仕様としてC言語の関数インターフェイスが選ばれることが多い](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink")。例えば[OpenGL](https://ja.wikipedia.org/wiki/OpenGL "wikilink")や[OpenCL](https://ja.wikipedia.org/wiki/OpenCL "wikilink")のようなオープン規格は第一級言語としてC言語を採用している。

### コード例

#### Hello worldプログラム

C言語の[Hello worldプログラムは](https://ja.wikipedia.org/wiki/Hello_world "wikilink")、ホスト環境を前提とするか、フリースタンディング環境を前提とするかで、方向性が異なる。ホスト環境を前提とする場合には、[標準入出力](https://ja.wikipedia.org/wiki/標準入出力 "wikilink")の利用により、動作をすぐに確かめることができる。以下では、[標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")の[ヘッダーファイル](https://ja.wikipedia.org/wiki/ヘッダーファイル "wikilink")`stdio.h`にて宣言されている、[`puts`](https://ja.wikipedia.org/wiki/puts "wikilink")関数あるいは[`printf`](https://ja.wikipedia.org/wiki/printf "wikilink")関数を利用したものを例示する。

``` c
/* int puts(const char* s) を使う場合。  */
#include <stdio.h>

int main(void)
{
    puts("Hello, world!");
    return 0;
}
```

``` c
/* int printf(const char* format, ...) を使う場合。  */
#include <stdio.h>

int main(int argc, char* argv[])
{
    printf("Hello, world!\n");
    return 0;
}
```

上記サンプルソース中の「`\n`」は[エスケープ文字](https://ja.wikipedia.org/wiki/エスケープ文字 "wikilink")`\`による改行を表す。なお、`printf` 関数は書式文字列とそれに対応する[可変個引数](https://ja.wikipedia.org/wiki/可変個引数 "wikilink")を受け取り、書式化された文字列として表示できる高機能な標準出力関数であるが、序盤から例示に使用している入門書もある。また、main関数は引数のないバージョンと、コマンドライン引数をポインタ配列として受け取るバージョンどちらを使ってもよい。main関数とprintf関数は、いずれも入門者や初学者にとっては最初の鬼門となる難解な関数であり、C言語によるプログラミングのハードルを高くしている一因でもある。

### 主な制御構造

  - [`do/while`](https://ja.wikipedia.org/wiki/do-while文 "wikilink")
  - [`for`](https://ja.wikipedia.org/wiki/for文 "wikilink")
  - [`goto`](https://ja.wikipedia.org/wiki/goto文 "wikilink")
  - [`if`](https://ja.wikipedia.org/wiki/if文 "wikilink")
  - [`return`](https://ja.wikipedia.org/wiki/return文 "wikilink")
  - [`switch`](https://ja.wikipedia.org/wiki/switch文 "wikilink")
  - [`while`](https://ja.wikipedia.org/wiki/while文 "wikilink")
  - [関数](https://ja.wikipedia.org/wiki/サブルーチン#関数 "wikilink")

### 主な標準ライブラリ関数

## 歴史

### 誕生

C言語は、AT\&Tベル研究所の[ケン・トンプソン](https://ja.wikipedia.org/wiki/ケン・トンプソン "wikilink")が開発した[B言語](https://ja.wikipedia.org/wiki/B言語 "wikilink")の改良として誕生した（[\#外部リンク](https://ja.wikipedia.org/wiki/#外部リンク "wikilink")の「The Development of the C Language」参照）。

[1972年](https://ja.wikipedia.org/wiki/1972年 "wikilink")、トンプソンと[UNIX](https://ja.wikipedia.org/wiki/UNIX "wikilink")の開発を行っていた[デニス・リッチー](https://ja.wikipedia.org/wiki/デニス・リッチー "wikilink")はB言語を改良し、実行可能な[機械語](https://ja.wikipedia.org/wiki/機械語 "wikilink")を直接生成するC言語のコンパイラを開発した\[5\]。後に、UNIXは大部分をC言語によって書き換えられ、C言語のコンパイラ自体も移植性の高い実装の[Portable C Compilerに置き換わったこともあり](https://ja.wikipedia.org/wiki/Portable_C_Compiler "wikilink")、UNIX上のプログラムはその後にC言語を広く利用するようになった。

ちなみに、「UNIXを開発するためにC言語が作り出された」と言われることがあるが、「The Development of the C Language」によると、これは正しくなく、経緯は以下の通りである。C言語は、当初はあくまでもOS上で動くユーティリティを作成する目的で作り出されたものであり、OSのカーネルを記述するために使われるようになるのは後の展開である。

  - UNIXの開発当初、[Multics](https://ja.wikipedia.org/wiki/Multics "wikilink")プロジェクトが目指していた高級言語によるOSの開発という目標は見送られた。
  - アセンブリ言語でUNIXが作成されると、OS上で動くユーティリティを作成するためのプログラミング言語が必要とされた。
  - ケン・トンプソンは、当初Fortranコンパイラを作ろうとしたが、途中で放棄し、新しい言語であるB言語を作成した。
  - B言語はインタプリタ言語であったため動作が遅く、B言語でユーティリティを作ることはあまりなかった。

<!-- end list -->

  -
    開発者達は、コンパイラなどのユーティリティを「システムプログラム」と呼んでいたが、それらの作成に使われる「システムプログラミング言語」は、OSのカーネルを作成するための言語という意味ではない\[6\]。

<!-- end list -->

  - B言語の欠点を解消するため、1971年に改良作業を開始した。
  - 1972年にC言語のコンパイラができあがり、UNIXバージョン2において、いくつかのユーティリティを作成するために使用された。

### UNIX環境とC言語

アセンブラとの親和性が高いために、ハードウェアに密着したコーディングがやりやすかったこと、言語仕様が小さいためコンパイラの開発が楽だったこと、小さな資源で動く実行プログラムを作りやすかったこと、UNIX環境での実績があり、後述のK\&Rといった解説文書が存在していたことなど、さまざまな要因からC言語は業務開発や情報処理研究での利用者を増やしていった。特にメーカー間でオペレーティングシステムやCPUなどのアーキテクチャが違うUNIX環境では再移植の必要性がしばしば生じて、プログラムをC言語で書いてソースレベル互換\[7\]を確保することが標準となった。

### C言語誕生時の環境と他言語との比較

C言語の開発当初に使われた入力端末はであったことが知られている\[8\]。 ASR-37は1967年制定の旧ASCII ISO R646-7bitにもとづいており、「`{`」および「`}`」の入力を行うことができたが、当時は一般的に使われていた入力端末ではなかった。 当時[PDP-11](https://ja.wikipedia.org/wiki/PDP-11 "wikilink")の入力端末として広く使われていたのは[ASR-33](https://ja.wikipedia.org/wiki/ASR-33 "wikilink")であるが、これは1963年制定の旧ASCIIであるASA X3.4に準拠しており、「`{`」や「`}`」の入力を行うことはできなかった\[9\]。

このことは、ブロック構造に「`{`」や「`}`」を用いるC言語（さらに元をたどれば[B言語](https://ja.wikipedia.org/wiki/B言語 "wikilink")）は、当時の一般的な環境では使用不可能であったことを示している。 これは、C言語はその誕生当初にあっては一般に広く使われることを想定しておらず、ベル研究所内部で使われることを一義的に考えた言語であったという側面の表れである。

これに対し、Pascalや[BASIC](https://ja.wikipedia.org/wiki/BASIC "wikilink")等の当初から広く使われることを想定した言語では、ブロック構造に記号を用いずに`begin`と`end`をトークンとして用いることや、コメント行を表す際に開始トークンとして`REM`という文字列を用いることなど、記号入力に制約がある多くの入力端末に対応できるように配慮されていた。この頃の他の言語やOSで大文字と小文字の区別をしないものが多いのも、当時は大文字しか入力できない環境も少なくなかったことの表れである。

このような事情のため、C言語が普及するのは、ASCII対応端末が一般化した1980年代に入ってからである。

現在、ブロック構造の書式等で、`{...}`形式のC言語と、`begin...end`等を使用する他の言語との比較において優劣を論じられることがあるが、開発時の環境等をふまえずに現時点での利便性のみで論じるのは適切ではない場合があることに留意が必要である。

### PCとC言語

[1980年代](../Page/1980年代.md "wikilink")に普及し始めた[パーソナルコンピュータ](https://ja.wikipedia.org/wiki/パーソナルコンピュータ "wikilink") (PC) は当初、[8ビット](https://ja.wikipedia.org/wiki/8ビット "wikilink")CPUでROM-BASICを搭載していたものも多く、BASICが普及していたが、1980年代後半以降、[16ビット](https://ja.wikipedia.org/wiki/16ビット "wikilink")CPUを採用しメモリも増えた（ROM-BASIC非搭載の）PCが主流になりだすと、が存在したこともあり、ユーザーが急増した。8ビットや[8086系のPCへの移植は](https://ja.wikipedia.org/wiki/Intel_8086 "wikilink")、ポインタなどに制限や拡張を加えることで解決していた。

### 現在のC言語

1990年代中盤以降は、最初に学ぶプログラミング言語としても主流となった。また、90年代中盤にはゲーム専用機（ゲームコンソール）の性能向上とプログラムの大規模化、マルチプラットフォーム展開を受け、開発言語がアセンブラからC言語に移行した。その後、PCのさらなる性能向上と普及、[GUI環境や](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[オブジェクト指向](https://ja.wikipedia.org/wiki/オブジェクト指向 "wikilink")の普及、インターネットおよびウェブブラウザの普及により、[C++](https://ja.wikipedia.org/wiki/C++ "wikilink")、[Visual Basic](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[C\#](https://ja.wikipedia.org/wiki/C_Sharp "wikilink")、[Objective-C](https://ja.wikipedia.org/wiki/Objective-C "wikilink")、[PHP](https://ja.wikipedia.org/wiki/PHP_\(プログラミング言語\) "wikilink")、[JavaScript](https://ja.wikipedia.org/wiki/JavaScript "wikilink")などの高水準言語の利用者が増加した。広く利用されるプログラミング言語の数は増加傾向にあり、相対的にC言語が使われる場面は減りつつある。特にアプリケーションソフトウェアなどの上位層の開発には、C言語よりも記述性に優れる[C++](https://ja.wikipedia.org/wiki/C++ "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[C\#などC言語派生の後発言語が利用されることが多くなっている](https://ja.wikipedia.org/wiki/C_Sharp "wikilink")。資源制約の厳しかったゲーム開発においても、ハードウェアの性能向上や[ミドルウェア](https://ja.wikipedia.org/wiki/ミドルウェア "wikilink")の普及により、C++やC\#などが使われる場面が増えている。しかし、C言語は比較的移植性に優れた言語であり、個人開発／業務用開発／学術研究開発や[プロプライエタリ](https://ja.wikipedia.org/wiki/プロプライエタリ "wikilink")／[オープンソース](https://ja.wikipedia.org/wiki/オープンソース "wikilink")を問わず、オペレーティングシステムやデバイスドライバーなどの下位層、クロスプラットフォームAPIの外部仕様、C++やJavaなどの高水準言語の処理系および実行環境の実装が困難な小規模の組み込みシステムなどで、2019年現在でも幅広く利用されている。

## C言語の規格

### K\&R

[リッチーと](https://ja.wikipedia.org/wiki/デニス・リッチー "wikilink")[カーニハンの共著である](https://ja.wikipedia.org/wiki/ブライアン・カーニハン "wikilink")「[The C Programming Language](https://ja.wikipedia.org/wiki/プログラミング言語C "wikilink")」\[10\]（[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")）を出版。その後標準ができるまで実質的なC言語の標準として参照。C言語は発展可能な言語で、この本の記述も発展の可能性のある部分は厳密な記述をしておらず、曖昧な部分が存在していた。C言語が普及するとともに、[互換性のない処理系が数多く誕生した](https://ja.wikipedia.org/wiki/方言_\(プログラミング言語\) "wikilink")。これはプログラミング言語でしばしば起こる現象であり、C言語固有の現象ではない。

### C89/C90

そこで、[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")/IEC JTC1と[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")は協同でC言語の規格の標準化を進め、[1989年](https://ja.wikipedia.org/wiki/1989年 "wikilink")12月にANSIがANSI X3.159-1989, American National Standard for Information Systems -Programming Language-Cを、[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")12月にISOがINTERNATIONAL STANDARD ISO/IEC 9899 : 1990(E) Programming Languages-Cを発行した。ISO/IEC規格のほうが章立てを追加しており、その後ANSIもISO/IEC規格にならって章立てを追加した。それぞれC89 (ANSI C89) およびISO/IEC C90という通称で呼ぶことがある。

日本では、これを翻訳したものを『JIS X 3010-1993 プログラム言語C』として、[1993年](https://ja.wikipedia.org/wiki/1993年 "wikilink")10月に制定した。

最大の特徴は、C++と同様の[関数プロトタイプ](https://ja.wikipedia.org/wiki/関数プロトタイプ "wikilink")\[11\]を導入して引数の型チェックを強化したことと、[`void`](https://ja.wikipedia.org/wiki/void_\(コンピュータ\) "wikilink")や`enum`などの新しい型を導入したことである。一方、「処理系に依存するものとする」に留めた部分も幾つかある（`int`型のビット幅、`char`型の符号、[ビットフィールド](https://ja.wikipedia.org/wiki/ビットフィールド "wikilink")の[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")、シフト演算の挙動、構造体などへのパディング等）。

規格では以下の3種類の自由を認めている部分がいくつかある\[12\]。

  - 規格で定義しないことを決めている「未定義」 (undefined)
  - 規格で選択肢を定義したもののどれにするかを決めておらず、処理系が選択する必要があるが、文書化の必要はない「未規定」 (unspecified)
  - 処理系ごとに決めて文書化する必要のある「処理系定義」 (implementation-defined)

これにより、プラットフォームやプロセッサアーキテクチャとの相性による有利不利が生じないような仕様になっている。

[8ビット](https://ja.wikipedia.org/wiki/8ビット "wikilink")/[16ビット](https://ja.wikipedia.org/wiki/16ビット "wikilink")/[32ビット](https://ja.wikipedia.org/wiki/32ビット "wikilink")など、レジスタ幅（[ワード](https://ja.wikipedia.org/wiki/ワード "wikilink")サイズ）の異なるプロセッサ (CPU) に対応・最適化できるようにするため、組み込み型の情報量（大きさ）や内部表現にも処理系の自由を認めている。型のバイト数は[`sizeof`](https://ja.wikipedia.org/wiki/sizeof "wikilink")演算子で取得し、各型の最小値・最大値は`limits.h`で定義されているマクロ定数で参照することとしている。ただし、1バイトあたりのビット数は規定されていない。`sizeof(char) == 1`すなわち`char`型が1バイトであることは常に保証されるが、8ビット（[オクテット](https://ja.wikipedia.org/wiki/オクテット_\(コンピュータ\) "wikilink")）とは限らない。実際のビット数は`CHAR_BIT`マクロ定数で取得できる。とはいえ、現実の多くの処理系では`char`型は8ビットである。また、その他の[整数型](https://ja.wikipedia.org/wiki/整数型 "wikilink")については、`sizeof(int) >= 2`、`sizeof(int) >= sizeof(short)`、`sizeof(long) >= sizeof(int)`、という大小関係が定められているだけである（符号無し型も同様）。多くの処理系では`short`型のサイズは2バイト（16ビット）であるが、`int`や`long`のサイズはCPUのレジスタ幅などによって決められることが多い。`int`型、`short`型、`long`型で符号を明示しない場合は`signed`を付けた符号付き型として扱われる。しかし`char`型に関しては、`signed`（符号付き）にするか、それとも`unsigned`（符号無し）にするかは処理系依存である。`char`型、`signed char`型、`unsigned char`型はそれぞれ異なる型として扱われる。

規格上には、BCPLやC++形式の1行コメント（`//…`）は無いが、オプションで対応した処理系も多く、gccやClangはGNU拡張`-std=gnu89`でサポートしている。

GNU Cコンパイラ や [Clang](https://ja.wikipedia.org/wiki/Clang "wikilink") では、`-std=c89`（または`-ansi`もしくは`-std=c90`）をつけることにより、GNU拡張を使わないC89規格に準拠したコンパイルを行うことができる<ref>C89規格に準拠しないソースコードをGNU Cコンパイラでコンパイル失敗させるには、

    gcc -ansi -pedantic -fstrict-aliasing -Wall -Wextra -Wmissing-declarations -Werror test.c

とすれば良い（→[エイリアシング](https://ja.wikipedia.org/wiki/エイリアシング "wikilink")）。</ref>。加えて、`-pedantic`をつければ診断結果が出る。商用のコンパイラではWatcom Cコンパイラが規格適合の比率が高いと言われていた。現在Open Watcomとして公開している。

C89には、下記の追加の訂正と追加を行った。

  - ISO/IEC 9899/COR1:1994
  - ISO/IEC 9899/AMD1:1995 - 英語圏での利用を想定して制定したC89に対して、国際化のため[ワイド文字](https://ja.wikipedia.org/wiki/ワイド文字 "wikilink")版ライブラリを追加したAmendment1が[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")に発行された。
  - ISO/IEC 9899/COR2:1996

### C99

[1999年](https://ja.wikipedia.org/wiki/1999年 "wikilink")[12月1日](https://ja.wikipedia.org/wiki/12月1日 "wikilink")に、ISO/IEC JTC1 SC22 WG14 で規格の改訂を行い、C++の機能のいくつかを取り込むことを含め機能を拡張し、ISO/IEC 9899:1999(E) Programming Language--C (Second Edition) を制定した。この版のC言語の規格を、通称として[C99](https://ja.wikipedia.org/wiki/C99 "wikilink")と呼ぶ。

日本では、日本産業規格 JIS X 3010: 2003「プログラム言語C」がある。

主な追加機能：

  - 変数宣言がブロックの先頭でなくても良くなった。
  - ブール代数を扱うための`_Bool`型が予約語に追加され、標準ライブラリとして`stdbool.h`を追加した。
  - 複素数を扱うための`_Complex`型や`_Imaginary`型を予約語に追加し、標準ライブラリとして、`complex.h`を追加した。
  - 少なくとも[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")の整数値を保持できる `long long int`型の追加。
  - オプションとして、固定幅かつ内部表現の規定された整数型の標準化（`stdint.h`）。
  - `//`による1行コメント。
  - インライン関数（`inline`キーワード）。
  - [可変長配列](https://ja.wikipedia.org/wiki/可変長配列 "wikilink")（`alloca`関数の代替）\[13\]。

C99は下記の訂正がある。

  - ISO/IEC 9899:1999 Cor. 1:2001(E)
  - ISO/IEC 9899:1999 Cor. 2:2004(E)
  - ISO/IEC 9899:1999 Cor. 3:2007(E)

### C11

[2011年](https://ja.wikipedia.org/wiki/2011年 "wikilink")[12月8日](https://ja.wikipedia.org/wiki/12月8日 "wikilink")に*ISO/IEC 9899:2011*（通称 **C11**）として改訂された。改訂による変更・追加・削除機能の一部を以下に記述する。

C11は[Unicode](https://ja.wikipedia.org/wiki/Unicode "wikilink")文字列（[UTF-32](https://ja.wikipedia.org/wiki/UTF-32 "wikilink")、[UTF-16](https://ja.wikipedia.org/wiki/UTF-16 "wikilink")、[UTF-8](https://ja.wikipedia.org/wiki/UTF-8 "wikilink")の各符号化方式）に標準で対応している。そのほか、`type-generic`式、C++と同様の無名構造体・無名共用体、排他的アクセスによるファイルオープン方法、quick_exitなどのいくつかの標準関数などを追加した。

また、`_Noreturn`関数指示子を追加した。`_Noreturn`は従来処理系ごとに独自に付加していた属性情報（たとえばgccでは`__attribute__((__noreturn__))`）を標準化したもので、「呼び出し元に戻ることがない」という特殊な関数についてその特性を示すためにある。`return`文を持たない関数という意味ではなく（規格では`return`文を持たなくとも、関数の最後の文の実行が終われば制御は呼び出し元に戻る）、この指示が意味するものは、当該の関数、ないしその内部から呼び出している関数の実行中に、必ず`_exit`や`execve`を実行したり、例外などで終了する、あるいは、`longjmp`による大域ジャンプで抜け出す\[14\]、[継続渡しスタイル](https://ja.wikipedia.org/wiki/継続渡しスタイル "wikilink")変換されたコードである、などのために、絶対に制御が呼び出し元に戻らない、という関数を指示するためにある。そのような関数は、スタックに戻りアドレスを積む通常の呼び出しではなく、スタックを消費しないジャンプによって実行できる。

[アラインメント機能](https://ja.wikipedia.org/wiki/データ構造アライメント "wikilink")、`_Atomic`型やC言語ネイティブの原始的なスレッド機能などを省略可能な機能として規格に組み込んだ。また、C99では規格上必須要件とされていた機能のうち、複素数型と可変長配列を省略可能なものに変更した。これらの省略可能な機能はC11規格合致の必須要件ではないので、仮に完全に規格合致の処理系であっても、対応していないかもしれない。C11規格では、省略可能な機能のうちコンパイラがどれを提供しているかを判別するために利用できる、テスト用のマクロを用意している。

これにより、[`gets`](https://ja.wikipedia.org/wiki/gets "wikilink")関数は廃止されている。

### C17

2018年に*ISO/IEC 9899:2018*（通称**C17**または**C18**）として改訂された。仕様の欠陥修正がメインのマイナーアップデートである\[15\]。

## 主なC言語処理系

大抵の処理系はC言語とC++両方をサポートしている。C言語とC++の共通部分を明確にし、二つの言語の違いに矛盾が生じないようにすることが課題になっている。

### Linux、Windows、UNIX用

  - [C++ Builder](https://ja.wikipedia.org/wiki/C++_Builder "wikilink")
    Windows/[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")/[iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")/[Android](https://ja.wikipedia.org/wiki/Android "wikilink")対応のC/C++コンパイラBCCを含む、[RADツール](https://ja.wikipedia.org/wiki/Rapid_Application_Development "wikilink")。以前はWindowsおよびx86のみがメインターゲットだったが、Clang/LLVMをベースに再設計され、多数のプラットフォームやアーキテクチャをサポートするようになった\[16\]。前身はDOS/Windows用の[Borland C/C++](https://ja.wikipedia.org/wiki/ボーランド "wikilink")。さらに前身としてTurbo C/C++がある。
  - [Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")
    [LLVMをバックエンドとして用いる](https://ja.wikipedia.org/wiki/Low_Level_Virtual_Machine "wikilink")[オープンソース](https://ja.wikipedia.org/wiki/オープンソース "wikilink")のC/C++・Objective-Cコンパイラ。多数のCPUに対応。
  - [GNUコンパイラコレクション](https://ja.wikipedia.org/wiki/GNUコンパイラコレクション "wikilink") (GCC)
    C/C++以外の言語もサポートし、多数のCPUやオペレーティングシステムに対応、組み込み向けも含む多様な開発に広く使われる[オープンソース](https://ja.wikipedia.org/wiki/オープンソース "wikilink")のコンパイラ。独自拡張機能も多い。
    GCC 4.5で実質的にC99を完全サポートした\[17\]。
    GCC 4.9で実質的にC11を完全サポートした\[18\]。
  - [Microsoft Visual C++](https://ja.wikipedia.org/wiki/Microsoft_Visual_C++ "wikilink") (MSVC)
    Windows系プラットフォーム用のC/C++コンパイラ。ANSI C準拠（バージョン2013にてC99ライブラリをほぼ実装したが、言語機能など規格自体はサポートされていない）。x86・x64が主だが、[Xbox 360](https://ja.wikipedia.org/wiki/Xbox_360 "wikilink")、[Windows CE等向けに](https://ja.wikipedia.org/wiki/Microsoft_Windows_Embedded_CE "wikilink")[PowerPC](https://ja.wikipedia.org/wiki/PowerPC "wikilink")、[ARM](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")、[MIPS](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ "wikilink")、[Itanium](https://ja.wikipedia.org/wiki/Itanium "wikilink")等に対応した版もある。前身としてMS-DOS・Windows用のMicrosoft C Compilerがある。またその廉価版としてQuick Cがあった\[19\]。
  - [Intel C++ Compiler](https://ja.wikipedia.org/wiki/Intel_C++_Compiler "wikilink") (ICL/ICC)
    [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")製の[IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink") ([x86](https://ja.wikipedia.org/wiki/x86 "wikilink")) および[Intel 64](https://ja.wikipedia.org/wiki/Intel_64 "wikilink") ([x64](https://ja.wikipedia.org/wiki/x64 "wikilink")) 用のC/C++コンパイラ。Windows/Linux/[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")/[Android](https://ja.wikipedia.org/wiki/Android "wikilink")向けがある。gcc互換。
    バージョン11.1までは[IA-64](https://ja.wikipedia.org/wiki/IA-64 "wikilink") ([Itanium](https://ja.wikipedia.org/wiki/Itanium "wikilink")) をサポートするが、バージョン12.0以降ではサポートされない\[20\]。
    C99\[21\]とC11\[22\]の対応リストが公開されている。バージョン18.0でC11にほぼ対応している。
  - Open Watcom C/C++
    Windows・Linux・[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")・MS-DOS・[DOSエクステンダ](https://ja.wikipedia.org/wiki/DOSエクステンダ "wikilink")を対象とするx86用C言語・C++コンパイラ。商用だったWatcom C/C++がオープンソース化したもの。
  - [Portable C Compiler](https://ja.wikipedia.org/wiki/Portable_C_Compiler "wikilink")
    gccが普及する以前のUNIXにおける標準的C言語コンパイラ。現在は[オープンソース](https://ja.wikipedia.org/wiki/オープンソース "wikilink")。
  - Digital Mars C/C++
    Windows・MS-DOS・DOSエクステンダを対象とするx86用のC言語・C++コンパイラ。無料版もある。[ウォルター・ブライト](https://ja.wikipedia.org/wiki/ウォルター・ブライト "wikilink")作でDatalight C、Zorland C、Zortech C/C++、Symantec C/C++と変遷している。

### 組み込み用、8ビット・16ビット・32ビット・64ビットCPU用（クロスコンパイラ）

  - [GreenHILS C/C++](https://ja.wikipedia.org/wiki/GreenHILS "wikilink")
    組み込み向けのC言語・C++コンパイラ。 Windows用・[Solaris](https://ja.wikipedia.org/wiki/Solaris "wikilink")用・[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")用があり、HP/UX用がver4ではあった。
  - [CodeWarrior C/C++](https://ja.wikipedia.org/wiki/CodeWarrior "wikilink")
    組み込み向けやゲーム機開発向けのC言語・C++コンパイラ。[Classic Mac OS用として発祥](https://ja.wikipedia.org/wiki/Classic_Mac_OS "wikilink")、かってはWindows用・[BeOS](https://ja.wikipedia.org/wiki/BeOS "wikilink")用・[Palm](https://ja.wikipedia.org/wiki/Palm "wikilink")用もあった。
  - [ARM C/C++](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")
    ARM CPU用C言語・C++コンパイラ。
  - [IAR C/C++](https://ja.wikipedia.org/wiki/IARシステムズ "wikilink")
    新旧の組み込み向けCPU各種を広くカバーする。現在は統合開発環境EW・SWに移行。ARM CPU用C言語・C++コンパイラが著名。ARMをコアにした各社のCPUに対応している。
  - High C
    元はx86向けで[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")用だが[80386のネイティブモードに対応したため](https://ja.wikipedia.org/wiki/Intel_80386 "wikilink")[FM TOWNSでも標準開発環境](https://ja.wikipedia.org/wiki/FM_TOWNS "wikilink")、「High C 386」として使用された。現在は各社[RISC](https://ja.wikipedia.org/wiki/RISC "wikilink")向け。
  - [BDS-C](https://ja.wikipedia.org/wiki/BDS-C "wikilink")
    [CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")（8080・Z80）用のサブセット（整数のみ）のK\&R系のC言語コンパイラ。現在は[パブリックドメインソフトウェア](https://ja.wikipedia.org/wiki/パブリックドメインソフトウェア "wikilink")。
  - Hitech-C
    [Z80](https://ja.wikipedia.org/wiki/Z80 "wikilink")、[PICなど](https://ja.wikipedia.org/wiki/PIC_\(コントローラ\) "wikilink")。
  - Lattice C
    1980年代に、日本で高い普及率を見せたコンパイラ。解説書も多く出版されていた。日本での発売はライフボート。初期版はマイクロソフトCコンパイラ1.0として発売された。商用利用のできない個人向けの「personal」版も販売されており、これの価格は19,800円であった\[23\]\[24\]
  - LSI C
    [8080](https://ja.wikipedia.org/wiki/Intel_8080 "wikilink")・[Z80](https://ja.wikipedia.org/wiki/Z80 "wikilink")用のLSI C-80（セルフ版・クロス版。現在はクロス版のみ）と、8086用の[LSI C-86がある](https://ja.wikipedia.org/wiki/LSI_C-86 "wikilink")。8086では機能限定（[スモールモデルのプログラムしか開発できず](https://ja.wikipedia.org/wiki/Intel_8086#プログラミングモデル "wikilink")、[デバッガ](https://ja.wikipedia.org/wiki/デバッガ "wikilink")がない）の「試食版」が[フリーソフトで公開され](https://ja.wikipedia.org/wiki/フリーウェア "wikilink")、広く使われた。

## 関連する主なプログラミング言語

### 先祖

  - [ALGOL](https://ja.wikipedia.org/wiki/ALGOL "wikilink")
    ヨーロッパ生まれのアルゴリズム記述言語。[Pascal](https://ja.wikipedia.org/wiki/Pascal "wikilink")やC言語などに影響を与えたとされる。
  - [BCPL](https://ja.wikipedia.org/wiki/BCPL "wikilink")
    [MULTICS](https://ja.wikipedia.org/wiki/MULTICS "wikilink")で作成された高級言語。
  - [B言語](https://ja.wikipedia.org/wiki/B言語 "wikilink")
    初期のUNIXで作成されたインタプリタ方式の高級言語。BCPLを元に作られ、Cの原型となった。

### 継承・拡張・サブセット

  - [C++](https://ja.wikipedia.org/wiki/C++ "wikilink")
    C言語を拡張して[オブジェクト指向](https://ja.wikipedia.org/wiki/オブジェクト指向 "wikilink")化したもの。当初はC言語の[スーパーセット](https://ja.wikipedia.org/wiki/スーパーセット "wikilink")だったが、現在は細かい部分において非互換仕様が増えている。
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
    C++よりも言語文法レベルでオブジェクト指向を重視した言語。[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")などの危険性が高いポインタといったローレベルな要素を言語文法から排除している。[仮想マシン](https://ja.wikipedia.org/wiki/仮想マシン "wikilink")（Java VM, JVM）上で動作する。
  - [C\#](https://ja.wikipedia.org/wiki/C_Sharp "wikilink")
    [マイクロソフト](https://ja.wikipedia.org/wiki/マイクロソフト "wikilink")が[.NET Framework向けに開発した言語](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。文法はC言語およびC++に近い書式を持ち、Javaと似ている部分も存在するが、機能的には[Delphi](https://ja.wikipedia.org/wiki/Delphi "wikilink")がベースとなっている。
  - [Cg](https://ja.wikipedia.org/wiki/Cg_\(プログラミング言語\) "wikilink")
    C言語を[GPU上での](https://ja.wikipedia.org/wiki/Graphics_Processing_Unit "wikilink")[3次元コンピュータグラフィックス](https://ja.wikipedia.org/wiki/3次元コンピュータグラフィックス "wikilink")処理用に特化させたもの（[シェーダー](https://ja.wikipedia.org/wiki/シェーダー "wikilink")言語、[シェーディング言語](https://ja.wikipedia.org/wiki/シェーディング言語 "wikilink")）。[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")によって開発された。
  - [Cyclone](https://ja.wikipedia.org/wiki/Cyclone_\(プログラミング言語\) "wikilink")
    C言語の上位互換セキュア実装。ポインタの扱いを厳格化して安全面に配慮して拡張したもの。その他リージョンベースメモリ管理システム、[正規表現](https://ja.wikipedia.org/wiki/正規表現 "wikilink")、タグ付共用体などを追加している。
  - [Objective-C](https://ja.wikipedia.org/wiki/Objective-C "wikilink")
    C言語を拡張してオブジェクト指向化したもの。C言語に [Smalltalk](https://ja.wikipedia.org/wiki/Smalltalk "wikilink") のオブジェクトシステムを取り付けたような設計で、互換性は保たれている。C言語からの拡張部分がC++と干渉しないため、C++と混在した記述が可能。
  - [SystemC](https://ja.wikipedia.org/wiki/SystemC "wikilink")
    [ハードウェア記述言語](https://ja.wikipedia.org/wiki/ハードウェア記述言語 "wikilink")向けに拡張したもの。書式はC++。EEE 1666-2005。ISO 8866:1991。
  - [Impulse_C](https://ja.wikipedia.org/wiki/Impulse_C "wikilink")
    [ハードウェア記述言語](https://ja.wikipedia.org/wiki/ハードウェア記述言語 "wikilink")向けに拡張したもの。書式はC。
  - [Unified Parallel C](https://ja.wikipedia.org/wiki/Unified_Parallel_C "wikilink")
    [並列計算](https://ja.wikipedia.org/wiki/並列計算 "wikilink")向けに[C99](https://ja.wikipedia.org/wiki/C99 "wikilink")を拡張して作られた言語。

その他にも、[OpenGL](https://ja.wikipedia.org/wiki/OpenGL "wikilink")シェーダー言語である[GLSL](https://ja.wikipedia.org/wiki/GLSL "wikilink")、[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")（[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")）シェーダー言語である[HLSL](https://ja.wikipedia.org/wiki/HLSL "wikilink")、[OpenCL](https://ja.wikipedia.org/wiki/OpenCL "wikilink")カーネル記述言語であるOpenCL-Cなど、C言語の文法的特徴を取り入れた派生言語や[DSLが多数存在する](https://ja.wikipedia.org/wiki/ドメイン固有言語 "wikilink")。

## 参考文献

2015年現在、初心者向けのイラスト入り入門書や[サブルーチン](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")のサンプル集の他、[組み込み機器の制御や](https://ja.wikipedia.org/wiki/組み込みシステム "wikilink")[科学技術計算](https://ja.wikipedia.org/wiki/科学技術計算 "wikilink")など目的を特化した専門書なども多数ある。便利な機能の説明はあっても、学習者の水準や目的にあった本を見つけるのは必ずしも容易でない。オープンソースのCコンパイラ、OSも大規模なものがあり、直接読み始めるのは困難になっている。オープンソースのOSの小規模なものから始めるとよい。

  - [プログラミング言語C](https://ja.wikipedia.org/wiki/プログラミング言語C "wikilink")
    ブライアン・カーニハン、デニス・リッチー 共著、[石田晴久](https://ja.wikipedia.org/wiki/石田晴久 "wikilink")訳、[共立出版](https://ja.wikipedia.org/wiki/共立出版 "wikilink")。
    「K\&R」として知られている「The C Programming Language」の邦訳。入門書ではなく、特にプログラミングそのものが初めてという読者には不適である。初版と2版があり、2版が現在も時折増刷している（邦訳では事情により、原書2版を基とした版には旧版と改訂新版がある。旧版は装丁が緑地で新版は白地である）。標準の制定以前は本書初版を言語仕様の参考文献として扱っていたが、現在は規格票を参照すべきであり、本書の記述は参考にとどめるべきである。
  - [Cプログラムの落とし穴](https://ja.wikipedia.org/wiki/Cプログラムの落とし穴 "wikilink")
    コーニグ、中村明訳、新紀元社
    Cプログラミングで嵌まるところを指摘している。MISRA Cでも参考文献になっている。
  - [Cパズルブック](https://ja.wikipedia.org/wiki/Cパズルブック "wikilink")
    アラン・R. フューアー、田中和明訳、カットシステム
    Cプログラミングの芸当を示し、読み書きを推奨しない例を示している。

## 脚注

## 外部リンク

  - [ISO C Working Group](http://www.open-std.org/jtc1/sc22/wg14/)
  - [The Development of the C Language](https://www.bell-labs.com/usr/dmr/www/chist.html) - C言語がどのように開発されたかがわかる文書
  - [stdio.h on Coding Programmer Page / C Library Reference and Examples](https://code-reference.com/c/stdio.h) - C Reference

[Category:C言語](https://ja.wikipedia.org/wiki/Category:C言語 "wikilink") [Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:JIS](https://ja.wikipedia.org/wiki/Category:JIS "wikilink") [Category:基本情報技術者試験](https://ja.wikipedia.org/wiki/Category:基本情報技術者試験 "wikilink")

1.  他の言語、例えば、[BASIC](https://ja.wikipedia.org/wiki/BASIC "wikilink")や[Pascal](https://ja.wikipedia.org/wiki/Pascal "wikilink")ではプログラム開始直後に実行するプログラム要素はサブルーチンや手続きや関数ではない。
2.  ISO/IEC 14882:2003 §3.6.1 「The function main shall not be used within a program.」
3.   §3.6.1 「関数mainは、プログラムの中で挙用してはならない。」
4.  [EXP33-C. 未初期化のメモリを参照しない](http://www.jpcert.or.jp/sc-rules/c-exp33-c.html) [JPCERT/CC](https://ja.wikipedia.org/wiki/JPCERT/CC "wikilink")、2014年3月25日（2014年8月22日閲覧）。
5.  [Portability of C Programs and the UNIX Systems](https://www.bell-labs.com/usr/dmr/www/portpap.html)
6.  [The Evolution of the Unix Time-sharing System](https://www.bell-labs.com/usr/dmr/www/hist.html)
7.  [ソースレベル互換](http://japan.zdnet.com/glossary/exp/%E3%82%BD%E3%83%BC%E3%82%B9%E3%83%AC%E3%83%99%E3%83%AB%E4%BA%92%E6%8F%9B/?s=4) - ZDNet Japan
8.
9.  <http://www.tohoho-web.com/ex/draft/kanji.htm>
10. 「K\&R」という通称がある。
11. C89においては[関数プロトタイプ](https://ja.wikipedia.org/wiki/関数プロトタイプ "wikilink")は必須ではない。
12. [C FAQ 11](http://www.kouno.jp/home/c_faq/c11.html)
13. [6.19 Arrays of Variable Length](http://gcc.gnu.org/onlinedocs/gcc/Variable-Length.html)
14. `setjmp.h`を参照。
15. [C の歴史 - cppreference.com](https://ja.cppreference.com/w/c/language/history)
16. [Clang 拡張 C++ コンパイラ - RAD Studio](http://docwiki.embarcadero.com/RADStudio/Rio/ja/Clang_%E6%8B%A1%E5%BC%B5_C%2B%2B_%E3%82%B3%E3%83%B3%E3%83%91%E3%82%A4%E3%83%A9)
17. [Status of C99 features in GCC - GNU Project - Free Software Foundation (FSF)](https://gcc.gnu.org/c99status.html)
18. [C11Status - GCC Wiki](https://gcc.gnu.org/wiki/C11Status)
19.
20. [インテル® C++ Composer XE 2011 Windows\* 版インストール・ガイドおよびリリースノート - w_ccompxe_2011.7.258_Release_Notes_ja_JP.pdf](http://registrationcenter-download.intel.com/akdlm/irc_nas/2371/w_ccompxe_2011.7.258_Release_Notes_ja_JP.pdf)
21. [C99 Support in Intel® C++ Compiler | Intel® Software](https://software.intel.com/en-us/articles/c99-support-in-intel-c-compiler)
22. [C11 Support in Intel C++ Compiler | Intel® Software](https://software.intel.com/en-us/articles/c11-support-in-intel-c-compiler)
23.  - 普及率、解説書の多さについて。
24.  - Personal版、解説書の多さについて。