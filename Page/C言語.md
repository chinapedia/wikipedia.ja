> この記事は[C言語](https://ja.wikipedia.org/wiki/C言語)から翻訳されています。


**C言語**（シーげんご、）は、[1972年](../Page/1972年.md "wikilink")に[AT\&Tベル研究所の](../Page/ベル研究所.md "wikilink")[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")が主体となって開発した汎用[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。英語圏では「C language」または単に「C」と呼ばれることが多い。日本でも文書や文脈によっては同様に「C」と呼ぶことがある。[制御構文](https://ja.wikipedia.org/wiki/制御構文 "wikilink")などに[高水準言語](../Page/高水準言語.md "wikilink")の特徴を持ちながら、ハードウェア寄りの記述も可能な[低水準言語](../Page/低水準言語.md "wikilink")の特徴も併せ持つ。基幹系システムや、動作環境の資源制約が厳しい、あるいは実行速度性能が要求されるソフトウェアの開発に用いられることが多い。後発の[C++](../Page/C++.md "wikilink")や[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[C\#など](../Page/C_Sharp.md "wikilink")、「C系」と呼ばれる派生言語の始祖でもある。[ANSI](../Page/米国国家規格協会.md "wikilink")、[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")、また[JISにより言語仕様が標準規格化されている](../Page/日本産業規格.md "wikilink")。

## 特徴

  - 汎用性が高い。プログラムの自由度が高く、また[機械語](../Page/機械語.md "wikilink")や[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")のような低水準言語と比較すると[ソースコード](../Page/ソースコード.md "wikilink")の再利用性やメンテナンス性に優れており、目的に応じた拡張が容易であるため、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")や[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")・[ファームウェア](../Page/ファームウェア.md "wikilink")の記述、[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")ー開発や機械制御など、あらゆる分野に適応している。
  - 対応する機器の範囲が広い。[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")はもちろん、自動車や家電の[組み込み用](../Page/組み込みシステム.md "wikilink")[マイコンから](../Page/マイクロコントローラ.md "wikilink")[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")まで、C言語を使用できるハードウェアは多様である。多目的性と、対応機器の多彩さのため、「コンピュータを使ってやること」は大抵、C言語で対応可能である。それゆえ、C言語のコード資産が蓄積されている環境は多岐に渡る。
  - 商用・非商用を問わず、採用ソフトウェア分野が広い。プログラム作成や[デバッグ](../Page/デバッグ.md "wikilink")のための補助的なソフトウェア（[プログラミングツール](https://ja.wikipedia.org/wiki/プログラミングツール "wikilink")）が豊富である。
  - 機械語に変換するソフトウェア（[コンパイラ](../Page/コンパイラ.md "wikilink")）などの開発環境が[CPU](../Page/CPU.md "wikilink")に付属していたり無償だったりするものもあるため、ライセンス料の支払いをしなくても使用が始められる。
  - 開発時期が古いことから、文法に機械語の影響が強く、仕様自体は単純ではあるが明快ではなく難解である。この欠点を改良するためのちに開発された後発言語に比較し、プログラマが記述しなければならないことが多く、[低水準言語](../Page/低水準言語.md "wikilink")のように面倒で習得しにくい側面を持つ。
  - アマチュアからプロ技術者まで、プログラマ人口が多く、プログラマのコミュニティが充実している。C言語は使用者の多さから、正負の両面含め、プログラミング文化に大きな影響を及ぼしている。
  - 言語の適用先である[UNIX](../Page/UNIX.md "wikilink")の場合、大抵のことが[スクリプト言語](../Page/スクリプト言語.md "wikilink")・[マクロプロセッサや](https://ja.wikipedia.org/wiki/マクロ_\(コンピュータ用語\)#マクロプロセッサ "wikilink")[フィルタやそれらの組み合わせで処理できるため](../Page/フィルタ_\(ソフトウェア\).md "wikilink")、うまく分野の棲み分けができていた面があった。仕様規格・派生言語も多く幅広い領域への移植の結果、適切でない分野にC言語が使われている場合もある。
  - C言語は[手続き型言語](https://ja.wikipedia.org/wiki/手続き型言語 "wikilink")である。[コンパイラ](../Page/コンパイラ.md "wikilink")言語とOSを念頭に設計している。ハードウェアをある程度抽象化しつつも、必要に応じて[機械語](../Page/機械語.md "wikilink")や[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")のコードと同じことを実現できるようなコンピュータ寄りの言語仕様になっている。低水準な記述ができる高級言語とも、高級言語の顔をした低級言語とも言うことがある。
  - Cコンパイラは、移植の容易性、自由度、実行速度、コンパイル速度などを追求した。代わりにコンパイル後のコードの安全性を犠牲にしている。また、詳細を規格で規定せず処理系に委ねている部分が多く、C言語で書かれたソフトウェアでは処理系依存のコードが氾濫する原因となった。セキュリティー上の脆弱性や潜在的バグによる想定外の動作、コンパイラによる最適化の難しさといった問題を抱えており、最適化するとコンパイル速度が遅くなるなどの欠点が生じることがある。自動車分野では[MISRA CというC言語の部分集合](https://ja.wikipedia.org/wiki/MISRA_C "wikilink") (subset) を定義して、危険な機能の使用や記述を禁止するという制限を設けることでC言語を安全に利用するためのガイドラインを設けている。
  - [UNIX](../Page/UNIX.md "wikilink")およびCコンパイラの移植性を高めるために開発してきた経緯から、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")[カーネル](../Page/カーネル.md "wikilink")およびコンパイラ向けの低水準記述ができる。

### 機能と自由度

  - 文の区切りを終端記号 [セミコロン](../Page/セミコロン.md "wikilink")「`;`」で表し、[改行文字にも](../Page/改行コード.md "wikilink")[空白にも](../Page/スペース.md "wikilink")[トークンの区切りとしての意味しか持たせない](../Page/字句解析.md "wikilink")「[フリーフォーマット](https://ja.wikipedia.org/wiki/フリーフォーマット_\(コンピュータ\) "wikilink")」という形式を採用している。中括弧`{ }`によるブロック構造および[スコープ](../Page/スコープ.md "wikilink")をサポートする。
      - 記述作法についてはしばしば議論の対象となり、書籍も多数出版されている。
  - [ALGOL](../Page/ALGOL.md "wikilink")の思想を受け継いで**[構造化](../Page/構造化プログラミング.md "wikilink")**に対応している。手順を[入れ子構造で示して見通しの良い記述をすることができる](../Page/ネスティング.md "wikilink")。原理的に**無条件分岐（[`goto`](https://ja.wikipedia.org/wiki/goto文 "wikilink")）**を使用する必要はなく、MISRA Cでは当初goto文を禁止していた。goto文を使わなければ、**[スパゲティプログラム](../Page/スパゲティプログラム.md "wikilink")**と呼ばれる読みにくいプログラムになりにくい。
  - **[モジュール](../Page/モジュール.md "wikilink")化**が[ファイルを単位として可能](../Page/ファイル_\(コンピュータ\).md "wikilink")。モジュール内だけで有効な名前を使うことが出来る[スコープ](../Page/スコープ.md "wikilink")を持っている。
  - プログラムを[戻り値](https://ja.wikipedia.org/wiki/戻り値 "wikilink")つきの[サブルーチン](../Page/サブルーチン.md "wikilink")に分離できる。C言語ではこれを**[関数](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")**と呼び、関数内のプログラムコードでは、独立したスコープを持つ変数（[ローカル変数](../Page/ローカル変数.md "wikilink")）が使用できる。これにより、データの流れがブロックごとに完結するのでデバッグが容易になり、また関数の再帰呼び出しも可能となる。また、多人数での共同開発の際にも変数名の衝突が回避しやすくなる。なお、C言語ではUNIXのようなOSを前提としたホスト環境と、割り込み制御のようなOSを前提としないフリースタンディング環境とがある。ホスト環境では、プログラム開始直後に実行するプログラム要素を `main` という名前の関数として定義する\[1\]。プログラム中で再帰的に`main`関数を呼ぶことも可能（C++では不可能\[2\]\[3\]）。フリースタンディング環境では、エントリポイントと呼ばれるアドレスに置かれたコードをプログラムの開始点とするが、それがmain関数である必要はない。なお再帰呼び出しは、[スタックオーバーフロー](../Page/スタックオーバーフロー.md "wikilink")の原因となるため、MISRA Cでは禁止している。

<!-- end list -->

  - システム記述言語として開発されたため、高級言語であるが[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")的な低水準の操作ができる。**[ポインタ演算](../Page/ポインタ_\(プログラミング\).md "wikilink")**、[ビット](../Page/ビット.md "wikilink")ごとの[論理演算](../Page/論理演算.md "wikilink")、シフト[演算](https://ja.wikipedia.org/wiki/演算 "wikilink")などの機能を持ち、[ハードウェア](../Page/ハードウェア.md "wikilink")に密着した処理を効率よく記述できる。これはオペレーティングシステムや[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")ーなどを記述する上では便利であるが、注意深く利用しないと発見しにくい[バグ](../Page/バグ.md "wikilink")の原因となる。ライブラリ関数は、C言語規格が規定している関数と、OSが規定している関数との間の整合性、棲み分けなどが流動的である。MISRA Cのようないくつかの制約では、C言語規格が規定している関数の妥当性について指摘し、いくつかの関数を利用しないように規定している。

<!-- end list -->

  - ソースコードの記述に使う文字集合はANSI-C:1989(ISO/IEC 9899:1990)では[ASCII](../Page/ASCII.md "wikilink")を標準としている。他の[ISO 646でも書けるように](https://ja.wikipedia.org/wiki/ISO_646 "wikilink")、3文字利用した[トライグラフ](https://ja.wikipedia.org/wiki/トライグラフ "wikilink")と呼ばれる表記法も存在する。その後、ISO/IEC 9899:1995 AMDなどでは[マルチバイト文字](../Page/マルチバイト文字.md "wikilink")セット対応の拡張を規定している。さらに、その後トライグラフは複数のコードを利用したシステムでしか利用がないため、より分かり易い2文字による[ダイグラフ](https://ja.wikipedia.org/wiki/ダイグラフ "wikilink")を規定している。
  - 組み込みの[整数型](../Page/整数型.md "wikilink")および[浮動小数点数](../Page/浮動小数点数.md "wikilink")型のほか、[構造体](../Page/構造体.md "wikilink")、[共用体](https://ja.wikipedia.org/wiki/共用体 "wikilink")、列挙体（[列挙型](../Page/列挙型.md "wikilink")）によるユーザー定義のデータ型や列挙定数をサポートする。構造体および共用体は[ビットフィールド](https://ja.wikipedia.org/wiki/ビットフィールド "wikilink")をサポートする。

### アセンブラとのインタフェース

  - 多くの処理系が[インラインアセンブラ](https://ja.wikipedia.org/wiki/インラインアセンブラ "wikilink")を搭載しているほか、アセンブラで出力したオブジェクトとのリンクが容易になっている。これにより速度が要求される部分だけを[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で記述するということが容易に行えることが多い。アセンブラとの[インタフェースは](../Page/インタフェース_\(情報技術\).md "wikilink")\#pragma asmなどを用いて局所化を図る努力はあるが、コンパイラごとに定義があり、CPUが同一であっても移植性が低い場合がある。

### コンパイラ仕様

  - コンパイラの処理が1パスで済む仕様になっている。ANSI-C:1989では宣言のない変数は`int`を想定することになっていた。ISO/IEC C:1999以降では[変数はその使用より前に宣言する必要がある](../Page/変数_\(プログラミング\).md "wikilink")。[関数の宣言がないと](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")、戻り値や引数を`int`型とみなす仕様は、が、型検査・型証明の仕組みが十分にないと不具合の原因になることがある。後継言語では記述によって先読みが必要になりうる。
  - マクロ記述やコンパイル条件の指定などが出来る前処理指令が標準化されている。前処理指令の解釈をする**[プリプロセッサ](../Page/プリプロセッサ.md "wikilink")** (preprocessor) を持っている。プリプロセッサは、その名の通りコンパイル処理の前に自動的に実行される。コンパイラの機能として、プリプロセッサを通しただけの段階のソースコードを出力可能になっているものがある。前処理の結果を検査することで、設計者の意図と前処理の結果のずれがないか確認できる。

### 処理系の簡素化

処理系の簡素化のため、以下のように安全性を犠牲にした仕様が多い。なお、ホスト環境やプログラムの内容によっては、以下に対して脆弱性対策を施したとしても実行速度の低下が無視できる程度であることも多く、言語仕様側の欠点とみなされることも少なくない。

  - [配列](../Page/配列.md "wikilink")参照時の自動的な添字のチェックをしない
    これを要因とする代表的なバグが、固定長のバッファ領域をはみだしてデータの書き込みが行われてしまう「[バッファオーバーフロー](https://ja.wikipedia.org/wiki/バッファオーバーフロー "wikilink")」（[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")）である。標準ライブラリにはバッファオーバーフローを考慮していない関数があり、かつ多用されがちなため、しばしば[脆弱性](../Page/脆弱性.md "wikilink")の原因となる。また、プログラムにより明示的に制御（[動的メモリ確保](../Page/動的メモリ確保.md "wikilink")）することで[可変長配列](../Page/可変長配列.md "wikilink")の実現を可能にしているが、確保した領域の範囲外にアクセスしても自動的な伸長は行なわれない。
  - [文字列](../Page/文字列.md "wikilink")を格納するための特別な型が存在しない
    文字列には`char`型の配列を利用する。言語仕様上に特別な扱いはないが、[ヌル文字](https://ja.wikipedia.org/wiki/ヌル文字 "wikilink")（`'\0'`）を終端とする[文字列](../Page/文字列.md "wikilink")表現を使い、その操作をする[標準ライブラリ関数がある](../Page/標準Cライブラリ.md "wikilink")。これは実質的にメモリ領域のポインタアクセスそのもので、固定長バッファに対して、それより長い可変長の文字列を書き込んでしまうことがあり、[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")の元凶の1つとなっている。後継言語では文字列処理を特に強化している場合が多く、標準ライブラリあるいは言語仕様による組み込みの文字列型を提供している。
  - 自動変数の自動的な初期化をしない
    自動変数（静的でないローカル変数）は変数の中でも最も頻繁に用いられる。初期化されていない変数を参照した場合、値は不定となるが、不定な値へのアクセスはであるので、[コンパイラ最適化](../Page/コンパイラ最適化.md "wikilink")の過程で想定しない形に改変することもある\[4\]。変数宣言・初期化の仕様による制限から、変数宣言の時点で初期化せず後で代入することで初期化に代えることが日常的で、誤って不定の値の変数を読み出す[バグ](../Page/バグ.md "wikilink")を作り込みやすい。なお自動変数の自動とは 変数の領域の確保と開放が自動であるという意味であり、自動的に初期化されるという意味ではない。

### その他

  - ソースコード上の文字の大文字・小文字を区別する。
  - [入出力](../Page/入出力.md "wikilink")を含めほとんどの機能が、C言語自身で書かれた[ライブラリ](../Page/ライブラリ.md "wikilink")によって提供される。このことは、C言語の機種依存性が低く、入出力関係ライブラリをのぞいた部分は[移植性](../Page/移植性.md "wikilink")（ポータビリティ）が高いことを意味する。さまざまな機種があるUNIXの世界でC言語が普及した理由のひとつである。
  - プログラムの実行に必要とする[ハードウェア](../Page/ハードウェア.md "wikilink")資源が、アセンブラよりは多いが他の高級言語より少なくてすむため、現在さまざまな電化製品などの[組み込みシステム](../Page/組み込みシステム.md "wikilink")でも使用されている。
  - 組み込み向けの場合は、プログラミング言語として、アセンブラ以外ではCとC++しか用意されていないことがある。その場合、他のプログラミング言語は、CやC++で書かれた処理系が存在すればコンパイルすることにより利用可能となることもあるが、メモリ制約などで動作しないことがある。
  - ANSI/ISOにより規格が標準化された後は言語仕様の変化が小さく安定していること、C言語のプログラマ人口やコード資産が多いこと、[C++](../Page/C++.md "wikilink")や[Objective-C](../Page/Objective-C.md "wikilink")からC言語関数を直接利用できること、また必要に応じて他のプログラミング言語からC言語関数を呼び出すためのバインディングを記述することが容易であることなどから、[APIの外部仕様としてC言語の関数インターフェイスが選ばれることが多い](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink")。例えば[OpenGL](../Page/OpenGL.md "wikilink")や[OpenCL](../Page/OpenCL.md "wikilink")のようなオープン規格は第一級言語としてC言語を採用している。

### コード例

#### Hello worldプログラム

C言語の[Hello worldプログラムは](../Page/Hello_world.md "wikilink")、ホスト環境を前提とするか、フリースタンディング環境を前提とするかで、方向性が異なる。ホスト環境を前提とする場合には、[標準入出力](https://ja.wikipedia.org/wiki/標準入出力 "wikilink")の利用により、動作をすぐに確かめることができる。以下では、[標準Cライブラリ](../Page/標準Cライブラリ.md "wikilink")の[ヘッダーファイル](https://ja.wikipedia.org/wiki/ヘッダーファイル "wikilink")`stdio.h`にて宣言されている、[`puts`](https://ja.wikipedia.org/wiki/puts "wikilink")関数あるいは[`printf`](https://ja.wikipedia.org/wiki/printf "wikilink")関数を利用したものを例示する。

``` c
// int puts(const char* s) を使う場合。
#include <stdio.h>

int main(void)
{
    puts("Hello, world!");
    return 0;
}
```

``` c
// int printf(const char* format, ...) を使う場合。
#include <stdio.h>

int main(int argc, char* argv[])
{
    printf("Hello, world!\n");
    return 0;
}
```

上記サンプルソース中の「`\n`」は[エスケープ文字](../Page/エスケープ文字.md "wikilink")`\`による改行を表す。なお、`printf` 関数は書式文字列とそれに対応する[可変個引数](https://ja.wikipedia.org/wiki/可変個引数 "wikilink")を受け取り、書式化された文字列として表示できる高機能な標準出力関数であるが、序盤から例示に使用している入門書もある。また、main関数は引数のないバージョンと、コマンドライン引数をポインタ配列として受け取るバージョンどちらを使ってもよい。main関数とprintf関数は、いずれも入門者や初学者にとっては最初の鬼門となる難解な関数であり、C言語によるプログラミングのハードルを高くしている一因でもある。

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

C言語は、AT\&Tベル研究所の[ケン・トンプソン](../Page/ケン・トンプソン.md "wikilink")が開発した[B言語](../Page/B言語.md "wikilink")の改良として誕生した（[\#外部リンク](https://ja.wikipedia.org/wiki/#外部リンク "wikilink")の「The Development of the C Language」参照）。

[1972年](../Page/1972年.md "wikilink")、トンプソンと[UNIX](../Page/UNIX.md "wikilink")の開発を行っていた[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")はB言語を改良し、実行可能な[機械語](../Page/機械語.md "wikilink")を直接生成するC言語のコンパイラを開発した\[5\]。後に、UNIXは大部分をC言語によって書き換えられ、C言語のコンパイラ自体も移植性の高い実装の[Portable C Compilerに置き換わったこともあり](../Page/Portable_C_Compiler.md "wikilink")、UNIX上のプログラムはその後にC言語を広く利用するようになった。

ちなみに、「UNIXを開発するためにC言語が作り出された」と言われることがあるが、「The Development of the C Language」によると、これは正しくなく、経緯は以下の通りである。C言語は、当初はあくまでもOS上で動くユーティリティを作成する目的で作り出されたものであり、OSのカーネルを記述するために使われるようになるのは後の展開である。

  - UNIXの開発当初、[Multics](../Page/Multics.md "wikilink")プロジェクトが目指していた高級言語によるOSの開発という目標は見送られた。
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

C言語の開発当初に使われた入力端末はであったことが知られている\[8\]。 ASR-37は1967年制定の旧ASCII ISO R646-7bitにもとづいており、「`{`」および「`}`」の入力を行うことができたが、当時は一般的に使われていた入力端末ではなかった。 当時[PDP-11](../Page/PDP-11.md "wikilink")の入力端末として広く使われていたのは[ASR-33](../Page/ASR-33.md "wikilink")であるが、これは1963年制定の旧ASCIIであるASA X3.4に準拠しており、「`{`」や「`}`」の入力を行うことはできなかった\[9\]。

このことは、ブロック構造に「`{`」や「`}`」を用いるC言語（さらに元をたどれば[B言語](../Page/B言語.md "wikilink")）は、当時の一般的な環境では使用不可能であったことを示している。 これは、C言語はその誕生当初にあっては一般に広く使われることを想定しておらず、ベル研究所内部で使われることを一義的に考えた言語であったという側面の表れである。

これに対し、Pascalや[BASIC](../Page/BASIC.md "wikilink")等の当初から広く使われることを想定した言語では、ブロック構造に記号を用いずに`begin`と`end`をトークンとして用いることや、コメント行を表す際に開始トークンとして`REM`という文字列を用いることなど、記号入力に制約がある多くの入力端末に対応できるように配慮されていた。この頃の他の言語やOSで大文字と小文字の区別をしないものが多いのも、当時は大文字しか入力できない環境も少なくなかったことの表れである。

このような事情のため、C言語が普及するのは、ASCII対応端末が一般化した1980年代に入ってからである。

現在、ブロック構造の書式等で、`{...}`形式のC言語と、`begin...end`等を使用する他の言語との比較において優劣を論じられることがあるが、開発時の環境等をふまえずに現時点での利便性のみで論じるのは適切ではない場合があることに留意が必要である。

### PCとC言語

[1980年代](../Page/1980年代.md "wikilink")に普及し始めた[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink") (PC) は当初、[8ビット](../Page/8ビット.md "wikilink")CPUでROM-BASICを搭載していたものも多く、BASICが普及していたが、1980年代後半以降、[16ビット](../Page/16ビット.md "wikilink")CPUを採用しメモリも増えた（ROM-BASIC非搭載の）PCが主流になりだすと、が存在したこともあり、ユーザーが急増した。8ビットや[8086系のPCへの移植は](../Page/Intel_8086.md "wikilink")、ポインタなどに制限や拡張を加えることで解決していた。

### 現在のC言語

1990年代中盤以降は、最初に学ぶプログラミング言語としても主流となった。また、90年代中盤にはゲーム専用機（ゲームコンソール）の性能向上とプログラムの大規模化、マルチプラットフォーム展開を受け、開発言語がアセンブラからC言語に移行した。その後、PCのさらなる性能向上と普及、[GUI環境や](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")の普及、インターネットおよびウェブブラウザの普及により、[C++](../Page/C++.md "wikilink")、[Visual Basic](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[C\#](../Page/C_Sharp.md "wikilink")、[Objective-C](../Page/Objective-C.md "wikilink")、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[JavaScript](../Page/JavaScript.md "wikilink")などの高水準言語の利用者が増加した。広く利用されるプログラミング言語の数は増加傾向にあり、相対的にC言語が使われる場面は減りつつある。特にアプリケーションソフトウェアなどの上位層の開発には、C言語よりも記述性に優れる[C++](../Page/C++.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[C\#などC言語派生の後発言語が利用されることが多くなっている](../Page/C_Sharp.md "wikilink")。資源制約の厳しかったゲーム開発においても、ハードウェアの性能向上や[ミドルウェア](../Page/ミドルウェア.md "wikilink")の普及により、C++やC\#などが使われる場面が増えている。しかし、C言語は比較的移植性に優れた言語であり、個人開発／業務用開発／学術研究開発や[プロプライエタリ](https://ja.wikipedia.org/wiki/プロプライエタリ "wikilink")／[オープンソース](../Page/オープンソース.md "wikilink")を問わず、オペレーティングシステムやデバイスドライバーなどの下位層、クロスプラットフォームAPIの外部仕様、C++やJavaなどの高水準言語の処理系および実行環境の実装が困難な小規模の組み込みシステムなどで、2019年現在でも幅広く利用されている。

## C言語の規格

### K\&R

[リッチーと](../Page/デニス・リッチー.md "wikilink")[カーニハンの共著である](../Page/ブライアン・カーニハン.md "wikilink")「[The C Programming Language](https://ja.wikipedia.org/wiki/プログラミング言語C "wikilink")」\[10\]（[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")）を出版。その後標準ができるまで実質的なC言語の標準として参照。C言語は発展可能な言語で、この本の記述も発展の可能性のある部分は厳密な記述をしておらず、曖昧な部分が存在していた。C言語が普及するとともに、[互換性のない処理系が数多く誕生した](../Page/方言_\(プログラミング言語\).md "wikilink")。これはプログラミング言語でしばしば起こる現象であり、C言語固有の現象ではない。

### C89/C90

そこで、[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")/IEC JTC1と[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")は協同でC言語の規格の標準化を進め、[1989年](../Page/1989年.md "wikilink")12月にANSIがANSI X3.159-1989, American National Standard for Information Systems -Programming Language-Cを、[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")12月にISOがINTERNATIONAL STANDARD ISO/IEC 9899 : 1990(E) Programming Languages-Cを発行した。ISO/IEC規格のほうが章立てを追加しており、その後ANSIもISO/IEC規格にならって章立てを追加した。それぞれC89 (ANSI C89) およびISO/IEC C90という通称で呼ぶことがある。

日本では、これを翻訳したものを『JIS X 3010-1993 プログラム言語C』として、[1993年](../Page/1993年.md "wikilink")10月に制定した。

最大の特徴は、C++と同様の[関数プロトタイプ](https://ja.wikipedia.org/wiki/関数プロトタイプ "wikilink")\[11\]を導入して引数の型チェックを強化したことと、[`void`](https://ja.wikipedia.org/wiki/void_\(コンピュータ\) "wikilink")や`enum`などの新しい型を導入したことである。一方、「処理系に依存するものとする」に留めた部分も幾つかある（`int`型のビット幅、`char`型の符号、[ビットフィールド](https://ja.wikipedia.org/wiki/ビットフィールド "wikilink")の[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")、シフト演算の挙動、構造体などへのパディング等）。

規格では以下の3種類の自由を認めている部分がいくつかある\[12\]。

  - 規格で定義しないことを決めている「未定義」 (undefined)
  - 規格で選択肢を定義したもののどれにするかを決めておらず、処理系が選択する必要があるが、文書化の必要はない「未規定」 (unspecified)
  - 処理系ごとに決めて文書化する必要のある「処理系定義」 (implementation-defined)

これにより、プラットフォームやプロセッサアーキテクチャとの相性による有利不利が生じないような仕様になっている。

[8ビット](../Page/8ビット.md "wikilink")/[16ビット](../Page/16ビット.md "wikilink")/[32ビット](../Page/32ビット.md "wikilink")など、レジスタ幅（[ワード](../Page/ワード.md "wikilink")サイズ）の異なるプロセッサ (CPU) に対応・最適化できるようにするため、組み込み型の情報量（大きさ）や内部表現にも処理系の自由を認めている。型のバイト数は[`sizeof`](https://ja.wikipedia.org/wiki/sizeof "wikilink")演算子で取得し、各型の最小値・最大値は`limits.h`で定義されているマクロ定数で参照することとしている。ただし、1バイトあたりのビット数は規定されていない。`sizeof(char) == 1`すなわち`char`型が1バイトであることは常に保証されるが、8ビット（[オクテット](https://ja.wikipedia.org/wiki/オクテット_\(コンピュータ\) "wikilink")）とは限らない。実際のビット数は`CHAR_BIT`マクロ定数で取得できる。とはいえ、現実の多くの処理系では`char`型は8ビットである。また、その他の[整数型](../Page/整数型.md "wikilink")については、`sizeof(int) >= 2`、`sizeof(int) >= sizeof(short)`、`sizeof(long) >= sizeof(int)`、という大小関係が定められているだけである（符号無し型も同様）。多くの処理系では`short`型のサイズは2バイト（16ビット）であるが、`int`や`long`のサイズはCPUのレジスタ幅などによって決められることが多い。`int`型、`short`型、`long`型で符号を明示しない場合は`signed`を付けた符号付き型として扱われる。しかし`char`型に関しては、`signed`（符号付き）にするか、それとも`unsigned`（符号無し）にするかは処理系依存である。`char`型、`signed char`型、`unsigned char`型はそれぞれ異なる型として扱われる。

規格上には、BCPLやC++形式の1行コメント（`//…`）は無いが、オプションで対応した処理系も多く、gccやClangはGNU拡張`-std=gnu89`でサポートしている。

GNU Cコンパイラ や [Clang](https://ja.wikipedia.org/wiki/Clang "wikilink") では、`-std=c89`（または`-ansi`もしくは`-std=c90`）をつけることにより、GNU拡張を使わないC89規格に準拠したコンパイルを行うことができる<ref>C89規格に準拠しないソースコードをGNU Cコンパイラでコンパイル失敗させるには、

    gcc -ansi -pedantic -fstrict-aliasing -Wall -Wextra -Wmissing-declarations -Werror test.c

とすれば良い（→[エイリアシング](https://ja.wikipedia.org/wiki/エイリアシング "wikilink")）。</ref>。加えて、`-pedantic`をつければ診断結果が出る。商用のコンパイラではWatcom Cコンパイラが規格適合の比率が高いと言われていた。現在Open Watcomとして公開している。

C89には、下記の追加の訂正と追加を行った。

  - ISO/IEC 9899/COR1:1994
  - ISO/IEC 9899/AMD1:1995 - 英語圏での利用を想定して制定したC89に対して、国際化のため[ワイド文字](../Page/ワイド文字.md "wikilink")版ライブラリを追加したAmendment1が[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")に発行された。
  - ISO/IEC 9899/COR2:1996

### C99

[1999年](../Page/1999年.md "wikilink")[12月1日](../Page/12月1日.md "wikilink")に、ISO/IEC JTC1 SC22 WG14 で規格の改訂を行い、C++の機能のいくつかを取り込むことを含め機能を拡張し、ISO/IEC 9899:1999(E) Programming Language--C (Second Edition) を制定した。この版のC言語の規格を、通称として[C99](../Page/C99.md "wikilink")と呼ぶ。

日本では、日本産業規格 JIS X 3010: 2003「プログラム言語C」がある。

主な追加機能：

  - 変数宣言がブロックの先頭でなくても良くなった。
  - ブール代数を扱うための`_Bool`型が予約語に追加され、標準ライブラリとして`stdbool.h`を追加した。
  - 複素数を扱うための`_Complex`型や`_Imaginary`型を予約語に追加し、標準ライブラリとして、`complex.h`を追加した。
  - 少なくとも[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")の整数値を保持できる `long long int`型の追加。
  - オプションとして、固定幅かつ内部表現の規定された整数型の標準化（`stdint.h`）。
  - `//`による1行コメント。
  - インライン関数（`inline`キーワード）。
  - [可変長配列](../Page/可変長配列.md "wikilink")（`alloca`関数の代替）\[13\]。

C99は下記の訂正がある。

  - ISO/IEC 9899:1999 Cor. 1:2001(E)
  - ISO/IEC 9899:1999 Cor. 2:2004(E)
  - ISO/IEC 9899:1999 Cor. 3:2007(E)

### C11

[2011年](../Page/2011年.md "wikilink")[12月8日](../Page/12月8日.md "wikilink")に*ISO/IEC 9899:2011*（通称 **C11**）として改訂された。改訂による変更・追加・削除機能の一部を以下に記述する。

C11は[Unicode](../Page/Unicode.md "wikilink")文字列（[UTF-32](../Page/UTF-32.md "wikilink")、[UTF-16](../Page/UTF-16.md "wikilink")、[UTF-8](../Page/UTF-8.md "wikilink")の各符号化方式）に標準で対応している。そのほか、`type-generic`式、C++と同様の無名構造体・無名共用体、排他的アクセスによるファイルオープン方法、quick_exitなどのいくつかの標準関数などを追加した。

また、`_Noreturn`関数指示子を追加した。`_Noreturn`は従来処理系ごとに独自に付加していた属性情報（たとえばgccでは`__attribute__((__noreturn__))`）を標準化したもので、「呼び出し元に戻ることがない」という特殊な関数についてその特性を示すためにある。`return`文を持たない関数という意味ではなく（規格では`return`文を持たなくとも、関数の最後の文の実行が終われば制御は呼び出し元に戻る）、この指示が意味するものは、当該の関数、ないしその内部から呼び出している関数の実行中に、必ず`_exit`や`execve`を実行したり、例外などで終了する、あるいは、`longjmp`による大域ジャンプで抜け出す\[14\]、[継続渡しスタイル](https://ja.wikipedia.org/wiki/継続渡しスタイル "wikilink")変換されたコードである、などのために、絶対に制御が呼び出し元に戻らない、という関数を指示するためにある。そのような関数は、スタックに戻りアドレスを積む通常の呼び出しではなく、スタックを消費しないジャンプによって実行できる。

[アラインメント機能](https://ja.wikipedia.org/wiki/データ構造アライメント "wikilink")、`_Atomic`型やC言語ネイティブの原始的なスレッド機能などを省略可能な機能として規格に組み込んだ。また、C99では規格上必須要件とされていた機能のうち、複素数型と可変長配列を省略可能なものに変更した。これらの省略可能な機能はC11規格合致の必須要件ではないので、仮に完全に規格合致の処理系であっても、対応していないかもしれない。C11規格では、省略可能な機能のうちコンパイラがどれを提供しているかを判別するために利用できる、テスト用のマクロを用意している。

これにより、[`gets`](https://ja.wikipedia.org/wiki/gets "wikilink")関数は廃止されている。

### C17

2018年に*ISO/IEC 9899:2018*（通称**C17**または**C18**）として改訂された。仕様の欠陥修正がメインのマイナーアップデートである\[15\]。

## 主なC言語処理系

大抵の処理系はC言語とC++両方をサポートしている。C言語とC++の共通部分を明確にし、二つの言語の違いに矛盾が生じないようにすることが課題になっている。

### Linux、Windows、UNIX用

  - [C++ Builder](../Page/C++_Builder.md "wikilink")
    Windows/[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")/[iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")/[Android](../Page/Android.md "wikilink")対応のC/C++コンパイラBCCを含む、[RADツール](../Page/Rapid_Application_Development.md "wikilink")。以前はWindowsおよびx86のみがメインターゲットだったが、Clang/LLVMをベースに再設計され、多数のプラットフォームやアーキテクチャをサポートするようになった\[16\]。前身はDOS/Windows用の[Borland C/C++](../Page/ボーランド.md "wikilink")。さらに前身としてTurbo C/C++がある。
  - [Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")
    [LLVMをバックエンドとして用いる](https://ja.wikipedia.org/wiki/Low_Level_Virtual_Machine "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")のC/C++・Objective-Cコンパイラ。多数のCPUに対応。
  - [GNUコンパイラコレクション](../Page/GNUコンパイラコレクション.md "wikilink") (GCC)
    C/C++以外の言語もサポートし、多数のCPUやオペレーティングシステムに対応、組み込み向けも含む多様な開発に広く使われる[オープンソース](../Page/オープンソース.md "wikilink")のコンパイラ。独自拡張機能も多い。
    GCC 4.5で実質的にC99を完全サポートした\[17\]。
    GCC 4.9で実質的にC11を完全サポートした\[18\]。
  - [Microsoft Visual C++](../Page/Microsoft_Visual_C++.md "wikilink") (MSVC)
    Windows系プラットフォーム用のC/C++コンパイラ。ANSI C準拠（バージョン2013にてC99ライブラリをほぼ実装したが、言語機能など規格自体はサポートされていない）。x86・x64が主だが、[Xbox 360](../Page/Xbox_360.md "wikilink")、[Windows CE等向けに](../Page/Microsoft_Windows_Embedded_CE.md "wikilink")[PowerPC](../Page/PowerPC.md "wikilink")、[ARM](../Page/ARMアーキテクチャ.md "wikilink")、[MIPS](../Page/MIPSアーキテクチャ.md "wikilink")、[Itanium](../Page/Itanium.md "wikilink")等に対応した版もある。前身としてMS-DOS・Windows用のMicrosoft C Compilerがある。またその廉価版としてQuick Cがあった\[19\]。
  - [Intel C++ Compiler](../Page/Intel_C++_Compiler.md "wikilink") (ICL/ICC)
    [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")製の[IA-32](../Page/IA-32.md "wikilink") ([x86](https://ja.wikipedia.org/wiki/x86 "wikilink")) および[Intel 64](https://ja.wikipedia.org/wiki/Intel_64 "wikilink") ([x64](https://ja.wikipedia.org/wiki/x64 "wikilink")) 用のC/C++コンパイラ。Windows/Linux/[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")/[Android](../Page/Android.md "wikilink")向けがある。gcc互換。
    バージョン11.1までは[IA-64](../Page/IA-64.md "wikilink") ([Itanium](../Page/Itanium.md "wikilink")) をサポートするが、バージョン12.0以降ではサポートされない\[20\]。
    C99\[21\]とC11\[22\]の対応リストが公開されている。バージョン18.0でC11にほぼ対応している。
  - Open Watcom C/C++
    Windows・Linux・[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")・MS-DOS・[DOSエクステンダ](../Page/DOSエクステンダ.md "wikilink")を対象とするx86用C言語・C++コンパイラ。商用だったWatcom C/C++がオープンソース化したもの。
  - [Portable C Compiler](../Page/Portable_C_Compiler.md "wikilink")
    gccが普及する以前のUNIXにおける標準的C言語コンパイラ。現在は[オープンソース](../Page/オープンソース.md "wikilink")。
  - Digital Mars C/C++
    Windows・MS-DOS・DOSエクステンダを対象とするx86用のC言語・C++コンパイラ。無料版もある。[ウォルター・ブライト](https://ja.wikipedia.org/wiki/ウォルター・ブライト "wikilink")作でDatalight C、Zorland C、Zortech C/C++、Symantec C/C++と変遷している。

### 組み込み用、8ビット・16ビット・32ビット・64ビットCPU用（クロスコンパイラ）

  - [GreenHILS C/C++](https://ja.wikipedia.org/wiki/GreenHILS "wikilink")
    組み込み向けのC言語・C++コンパイラ。 Windows用・[Solaris](../Page/Solaris.md "wikilink")用・[Linux](../Page/Linux.md "wikilink")用があり、HP/UX用がver4ではあった。
  - [CodeWarrior C/C++](../Page/CodeWarrior.md "wikilink")
    組み込み向けやゲーム機開発向けのC言語・C++コンパイラ。[Classic Mac OS用として発祥](../Page/Classic_Mac_OS.md "wikilink")、かってはWindows用・[BeOS](../Page/BeOS.md "wikilink")用・[Palm](../Page/Palm.md "wikilink")用もあった。
  - [ARM C/C++](../Page/ARMアーキテクチャ.md "wikilink")
    ARM CPU用C言語・C++コンパイラ。
  - [IAR C/C++](https://ja.wikipedia.org/wiki/IARシステムズ "wikilink")
    新旧の組み込み向けCPU各種を広くカバーする。現在は統合開発環境EW・SWに移行。ARM CPU用C言語・C++コンパイラが著名。ARMをコアにした各社のCPUに対応している。
  - High C
    元はx86向けで[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")用だが[80386のネイティブモードに対応したため](../Page/Intel_80386.md "wikilink")[FM TOWNSでも標準開発環境](../Page/FM_TOWNS.md "wikilink")、「High C 386」として使用された。現在は各社[RISC](../Page/RISC.md "wikilink")向け。
  - [BDS-C](../Page/BDS-C.md "wikilink")
    [CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")（8080・Z80）用のサブセット（整数のみ）のK\&R系のC言語コンパイラ。現在は[パブリックドメインソフトウェア](../Page/パブリックドメインソフトウェア.md "wikilink")。
  - Hitech-C
    [Z80](../Page/Z80.md "wikilink")、[PICなど](../Page/PIC_\(コントローラ\).md "wikilink")。
  - Lattice C
    1980年代に、日本で高い普及率を見せたコンパイラ。解説書も多く出版されていた。日本での発売はライフボート。初期版はマイクロソフトCコンパイラ1.0として発売された。商用利用のできない個人向けの「personal」版も販売されており、これの価格は19,800円であった\[23\]\[24\]
  - LSI C
    [8080](../Page/Intel_8080.md "wikilink")・[Z80](../Page/Z80.md "wikilink")用のLSI C-80（セルフ版・クロス版。現在はクロス版のみ）と、8086用の[LSI C-86がある](../Page/LSI_C-86.md "wikilink")。8086では機能限定（[スモールモデルのプログラムしか開発できず](https://ja.wikipedia.org/wiki/Intel_8086#プログラミングモデル "wikilink")、[デバッガ](../Page/デバッガ.md "wikilink")がない）の「試食版」が[フリーソフトで公開され](../Page/フリーウェア.md "wikilink")、広く使われた。

## 関連する主なプログラミング言語

### 先祖

  - [ALGOL](../Page/ALGOL.md "wikilink")
    ヨーロッパ生まれのアルゴリズム記述言語。[Pascal](../Page/Pascal.md "wikilink")やC言語などに影響を与えたとされる。
  - [BCPL](../Page/BCPL.md "wikilink")
    [MULTICS](https://ja.wikipedia.org/wiki/MULTICS "wikilink")で作成された高級言語。
  - [B言語](../Page/B言語.md "wikilink")
    初期のUNIXで作成されたインタプリタ方式の高級言語。BCPLを元に作られ、Cの原型となった。

### 継承・拡張・サブセット

  - [C++](../Page/C++.md "wikilink")
    C言語を拡張して[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")化したもの。当初はC言語の[スーパーセット](https://ja.wikipedia.org/wiki/スーパーセット "wikilink")だったが、現在は細かい部分において非互換仕様が増えている。
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
    C++よりも言語文法レベルでオブジェクト指向を重視した言語。[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")などの危険性が高いポインタといったローレベルな要素を言語文法から排除している。[仮想マシン](https://ja.wikipedia.org/wiki/仮想マシン "wikilink")（Java VM, JVM）上で動作する。
  - [C\#](../Page/C_Sharp.md "wikilink")
    [マイクロソフト](../Page/マイクロソフト.md "wikilink")が[.NET Framework向けに開発した言語](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。文法はC言語およびC++に近い書式を持ち、Javaと似ている部分も存在するが、機能的には[Delphi](../Page/Delphi.md "wikilink")がベースとなっている。
  - [Cg](../Page/Cg_\(プログラミング言語\).md "wikilink")
    C言語を[GPU上での](../Page/Graphics_Processing_Unit.md "wikilink")[3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")処理用に特化させたもの（[シェーダー](../Page/シェーダー.md "wikilink")言語、[シェーディング言語](../Page/シェーディング言語.md "wikilink")）。[NVIDIA](../Page/NVIDIA.md "wikilink")によって開発された。
  - [Cyclone](https://ja.wikipedia.org/wiki/Cyclone_\(プログラミング言語\) "wikilink")
    C言語の上位互換セキュア実装。ポインタの扱いを厳格化して安全面に配慮して拡張したもの。その他リージョンベースメモリ管理システム、[正規表現](../Page/正規表現.md "wikilink")、タグ付共用体などを追加している。
  - [Objective-C](../Page/Objective-C.md "wikilink")
    C言語を拡張してオブジェクト指向化したもの。C言語に [Smalltalk](../Page/Smalltalk.md "wikilink") のオブジェクトシステムを取り付けたような設計で、互換性は保たれている。C言語からの拡張部分がC++と干渉しないため、C++と混在した記述が可能。
  - [SystemC](../Page/SystemC.md "wikilink")
    [ハードウェア記述言語](../Page/ハードウェア記述言語.md "wikilink")向けに拡張したもの。書式はC++。EEE 1666-2005。ISO 8866:1991。
  - [Impulse_C](https://ja.wikipedia.org/wiki/Impulse_C "wikilink")
    [ハードウェア記述言語](../Page/ハードウェア記述言語.md "wikilink")向けに拡張したもの。書式はC。
  - [Unified Parallel C](https://ja.wikipedia.org/wiki/Unified_Parallel_C "wikilink")
    [並列計算](../Page/並列計算.md "wikilink")向けに[C99](../Page/C99.md "wikilink")を拡張して作られた言語。

その他にも、[OpenGL](../Page/OpenGL.md "wikilink")シェーダー言語である[GLSL](../Page/GLSL.md "wikilink")、[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")（[Direct3D](../Page/Direct3D.md "wikilink")）シェーダー言語である[HLSL](https://ja.wikipedia.org/wiki/HLSL "wikilink")、[OpenCL](../Page/OpenCL.md "wikilink")カーネル記述言語であるOpenCL-Cなど、C言語の文法的特徴を取り入れた派生言語や[DSLが多数存在する](../Page/ドメイン固有言語.md "wikilink")。

## 参考文献

2015年現在、初心者向けのイラスト入り入門書や[サブルーチン](../Page/サブルーチン.md "wikilink")のサンプル集の他、[組み込み機器の制御や](../Page/組み込みシステム.md "wikilink")[科学技術計算](https://ja.wikipedia.org/wiki/科学技術計算 "wikilink")など目的を特化した専門書なども多数ある。便利な機能の説明はあっても、学習者の水準や目的にあった本を見つけるのは必ずしも容易でない。オープンソースのCコンパイラ、OSも大規模なものがあり、直接読み始めるのは困難になっている。オープンソースのOSの小規模なものから始めるとよい。

  - [プログラミング言語C](https://ja.wikipedia.org/wiki/プログラミング言語C "wikilink")
    ブライアン・カーニハン、デニス・リッチー 共著、[石田晴久](../Page/石田晴久.md "wikilink")訳、[共立出版](../Page/共立出版.md "wikilink")。
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

1.  他の言語、例えば、[BASIC](../Page/BASIC.md "wikilink")や[Pascal](../Page/Pascal.md "wikilink")ではプログラム開始直後に実行するプログラム要素はサブルーチンや手続きや関数ではない。
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