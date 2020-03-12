> この記事は[LINPACK](https://ja.wikipedia.org/wiki/LINPACK)から翻訳されています。


**LINPACK** (リンパック)は、主として[線型代数](https://ja.wikipedia.org/wiki/線型代数 "wikilink")の[数値計算を目的とした](https://ja.wikipedia.org/wiki/数値解析 "wikilink")、行列およびベクトルの演算が実装されている[ライブラリ](../Page/ライブラリ.md "wikilink")である。

## 概要

[MINPACK](https://ja.wikipedia.org/wiki/MINPACK "wikilink")、[EISPACK](https://ja.wikipedia.org/wiki/EISPACK "wikilink") と同様、米国[アルゴンヌ国立研究所](../Page/アルゴンヌ国立研究所.md "wikilink")で[FORTRAN](../Page/FORTRAN.md "wikilink")ライブラリとして開発された。実際に開発を行ったのは [ジャック・ドンガラ](https://ja.wikipedia.org/wiki/ジャック・ドンガラ "wikilink")、ジム・バンチ、、ギルバート・スチュアートである。1970年代から1980年代初期の[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")を対象として設計され\[1\]\[2\]、その後より洗練されたライブラリ[LAPACK](../Page/LAPACK.md "wikilink")に取って代わられた。

LINPACK は BLAS（[Basic Linear Algebra Subprograms](https://ja.wikipedia.org/wiki/Basic_Linear_Algebra_Subprograms "wikilink")、基本線形代数サブプログラム群）ライブラリを使ってベクトル演算や行列演算を行う。

後述するLINPACKベンチマークは、LINPACKのユーザーズマニュアルの一部として公開されたのが最初である。

## ベンチマーク

**LINPACK ベンチマーク**は LINPACK に基づいた[ベンチマーク](../Page/ベンチマーク.md "wikilink")プログラムで、システムの[浮動小数点演算性能を評価する](../Page/浮動小数点数.md "wikilink")。[ジャック・ドンガラ](https://ja.wikipedia.org/wiki/ジャック・ドンガラ "wikilink")が考案したもので、[理学](../Page/理学.md "wikilink")・[工学](../Page/工学.md "wikilink")で一般的な *n*×*n* の[線型方程式系](../Page/線型方程式系.md "wikilink")\[3\] *Ax* = *b* を解く速度を測定する。このベンチマークの最新版は[TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")で世界の高速なコンピュータの性能値としてランキングに使用されている\[4\]。

コンピュータが実世界の問題を解く性能の近似値を得ることを目的としている。しかし、1つの測定値でコンピュータシステムのあらゆる性能を代表させることは不可能であり、あくまでも1つの単純化である。それでも、メーカーが提供するピーク性能値に対してLINPACKベンチマークがよい補正を提供している。ピーク性能とは、そのコンピュータが理論上達成しうる最高性能であり、クロック周波数、1秒間の命令サイクル数、1サイクルで実行可能な演算回数などから計算される。実際の性能は常にピーク性能よりも低い\[5\]。コンピュータの性能は様々な要素が相互に絡み合った複雑な問題である。LINPACKベンチマークで測定するのは、64ビット浮動小数点演算（通常、加算と乗算）の1秒あたりの実行回数（[FLOPS](../Page/FLOPS.md "wikilink")）である。しかし、実アプリケーションを実行したときの性能は、LINPACKベンチマークを適切に設定して測定したときの最高性能よりずっと低くなる可能性が高い\[6\]。

### 歴史

LINPACKベンチマークは1979年、LINPACKのユーザーズマニュアルの付録として公開されたのが最初である\[7\]。LINPACKパッケージを使って問題を解く際にかかる時間をユーザーが推定する手がかりを与えることを目的として設計された。そのため、当初は大きさ100の行列問題を23種類用意していた。大きさは当時のメモリ容量を考慮して選択された。-1 から 1 の範囲内の浮動小数点数を10000個、無作為に生成し密係数行列を作る。そして、部分ピボット選択による[LU分解](../Page/LU分解.md "wikilink")を使用する。その後、行列の大きさを300や1000にしたり、制限を緩めるなどして、行列やベクトルの演算を実装するようになったハードウェアアーキテクチャによる最適化を役立てられるようにしていった\[8\]。オーダー1000の大きさの問題の場合、そのベンチマークを LINPACK 1000 と呼び、問題を解くアルゴリズムを修正可能である\[9\]。1991年には任意の大きさの問題を解くベンチマークが登場した\[10\]。これで[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")の極限性能に近い値を得られるようになり、その2年後に[TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")リストが公開されるようになった。

### 具体的なベンチマーク

#### LINPACK 100

1979年、LINPACKのユーザーズマニュアル\[11\]で公表されたオリジナルのベンチマークにほぼ近い。部分ピボット選択による[ガウスの消去法](../Page/ガウスの消去法.md "wikilink")で問題を解き、2/3n<sup>3</sup> + 2n<sup>2</sup> 回の浮動小数点演算を行う。*n* は 100 で、問題を定義する行列 *A* の次数である。サイズが小さく、ソフトウェアの柔軟性が欠けていたため、多くの最新のコンピュータでは限界性能を引き出すことができない。しかし、計算中心のユーザープログラムの性能を見積もるのにはある程度役立つ\[12\]。

#### LINPACK 1000

問題のサイズを大きくして行列の次数を1000とし、アルゴリズムを変更可能にしたため、コンピュータの限界に近い性能を引き出せるようになった。残っている制限は、相対精度を低くしないという点と、演算回数は 2/3n<sup>3</sup> + 2n<sup>2</sup> 回 (n = 1000) だという点である\[13\]。

#### HPLinpack

従来のベンチマークは並列コンピュータの性能測定には適していない\[14\]。そこで、並列コンピュータ向きの新たなベンチマーク Linpack’s Highly Parallel Computing benchmark、または HPLinpack ベンチマークが考案された。HPLinpackではサイズ n をそのマシンでの最高性能を引き出せる値にまで大きくできる。演算回数は 2/3n<sup>3</sup> + 2n<sup>2</sup> 回だがアルゴリズムは選択可能である。[シュトラッセンのアルゴリズム](../Page/シュトラッセンのアルゴリズム.md "wikilink")は演算回数を減らしてしまうので使えない\[15\]。精度は次の式が成り立つようになる必要がある。

\[{\lVert Ax-b\rVert\over \lVert A\rVert \lVert x\rVert n \epsilon} \leq O(1)\]

ここで \(\epsilon\) はそのマシンの精度、*n* は問題のサイズ\[16\]、\(\lVert \cdot \rVert\) は[行列ノルム](../Page/行列ノルム.md "wikilink")、\(O(1)\) は[O-記法である](../Page/ランダウの記号.md "wikilink")。

各システムについて、次の数値を報告する\[17\]。

  - R<sub>max</sub>: そのマシンで最大の問題についての性能（[GFLOPS](../Page/FLOPS.md "wikilink")）
  - N<sub>max</sub>: そのマシンでの最大の問題のサイズ
  - N<sub>1/2</sub>: Rmaxの半分の性能となるときの問題のサイズ
  - R<sub>peak</sub>: そのマシンの理論上のピーク性能（GFLOPS）

これらの結果を使って、[TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")リストが年に2回更新される\[18\]。

### 実装

前節ではベンチマークの基本的規則を解説している。それら規則に基づいたプログラムの[実装](../Page/実装.md "wikilink")は様々であり、[FORTRAN](../Page/FORTRAN.md "wikilink")による実装\[19\]、[C言語](../Page/C言語.md "wikilink")による実装\[20\]、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")による実装\[21\]などがある。

#### HPL

HPLはHPLinpackをC言語で実装したもので、本来はガイドラインとして書かれたものだが、TOP500でも広く使われている。なお、HPL以外のテクノロジーやパッケージを使うことに問題はない。HPLはn次の線型方程式系を生成し、部分ピボット選択によるLU分解でそれを解く。使用するには[MPI](https://ja.wikipedia.org/wiki/MPI "wikilink")と[BLASまたはVSIPLをインストールしておく必要がある](https://ja.wikipedia.org/wiki/Basic_Linear_Algebra_Subprograms "wikilink")\[22\]。

大まかに言えば、このアルゴリズムには次のような特徴がある\[23\]\[24\]。

  - 2次元ブロックで周期的データ配布を行う。
  - 様々な深さの[先読み](../Page/先読み.md "wikilink")を伴う right-looking 法の一種を使った[LU分解](../Page/LU分解.md "wikilink")
  - 再帰的パネル分解
  - パネル[ブロードキャスト](../Page/ブロードキャスト.md "wikilink")には6種類の方式がある。
  - 帯域幅を低減するスワップ・ブロードキャスト・アルゴリズム
  - 深さ1の先読みを伴う後退代入

### 批判

LINPACKベンチマークが成功した要因は、HPLinpackのスケーラビリティ\[25\]、1つの数値を生成するため比較が容易であるという事実、それまでの測定値を蓄積したデータベースが存在すること\[26\]が挙げられる。しかしリリース直後からLINPACKベンチマークには地道に最適化を施すプログラマだけが達成できる性能レベルを提供するもので、しかもその最適化はそのマシンでしか意味が無いという批判が浴びせられた\[27\]。また、解いている問題は密係数行列の線型方程式系であり、それが科学技術計算全般を代表するものではないという批判もある\[28\]。LINPACKベンチマークを推進してきた[ジャック・ドンガラ](https://ja.wikipedia.org/wiki/ジャック・ドンガラ "wikilink")は、CPUのピーク性能とCPU数だけが強調されており、帯域幅やネットワークへのストレスが十分でないと述べている\[29\]。[米国立スーパーコンピュータ応用研究所](../Page/米国立スーパーコンピュータ応用研究所.md "wikilink")のトム・ダニングはLINPACKベンチマークについて「興味深い現象の1つだ。それを知っているほとんど全員がそれをあざ笑う。彼らはその限界を理解しているが、何年にも渡って我々はその値を使ってきたため、一種のマインドシェアが生じている」と述べた\[30\]。ドンガラによれば、「システムの性能を様々な面から明らかにすることは重要」なので「TOP500の主催者はベンチマークの範囲を拡大する方法を積極的に模索している」という\[31\]。TOP500のベンチマークの拡張について可能性の高いものとして、[HPCチャレンジベンチマーク](https://ja.wikipedia.org/wiki/HPCチャレンジベンチマーク "wikilink") がある\[32\]。他に、倍精度浮動小数を要素とする行列の演算（特に乗算）を多用して、大規模な連立一次方程式を解くというベンチマークである点は共通だが、密ではなく疎な行列を対象とするHPCG（Conjugate Gradient、[共役勾配法](https://ja.wikipedia.org/wiki/共役勾配法 "wikilink")）や、そもそも数値計算ではない応用で近年重要性の増しているネットワーク構造（グラフ）の情報処理を対象とした[Graph500](https://ja.wikipedia.org/wiki/Graph500 "wikilink")などがある。

#### 測定にかかる時間の問題

[ジャック・ドンガラ](https://ja.wikipedia.org/wiki/ジャック・ドンガラ "wikilink")によれば、HPLinpackでよい性能値を得ようとすると測定に時間がかかるようになってきているという。2010年に開催された会議で、彼は「数年以内に」測定に2日半かかるようになるとの予想を行った\[33\]。

## 脚注

## 外部リンク

  - [LINPACK](http://www.netlib.org/linpack/)
  - [BLAS](http://www.netlib.org/blas/)
  - [TOP500 Supercomputing Sites](http://www.top500.org/)
  - [Linpack Benchmark -- Java Version](http://www.netlib.org/benchmark/linpackjava/) a web-based LINPACK benchmark
  - [The HPL benchmark](http://www.netlib.org/benchmark/hpl/) used in the [TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")

[Category:数値解析ソフトウェア](https://ja.wikipedia.org/wiki/Category:数値解析ソフトウェア "wikilink") [Category:数値線形代数](https://ja.wikipedia.org/wiki/Category:数値線形代数 "wikilink") [Category:ベンチマーク](https://ja.wikipedia.org/wiki/Category:ベンチマーク "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink") [Category:FORTRAN](https://ja.wikipedia.org/wiki/Category:FORTRAN "wikilink")

1.
2.
3.  ただし密係数行列。一般に、[差分法](../Page/差分法.md "wikilink")や[有限要素法](../Page/有限要素法.md "wikilink")などで解かれる大規模問題は、[連結リスト](../Page/連結リスト.md "wikilink")によって記述される[参照の局所性](../Page/参照の局所性.md "wikilink")の低い[疎行列](../Page/疎行列.md "wikilink")系であり、[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")の恩恵をほとんど受けない。（つまりメモリバンド幅によって性能が決まる。）したがって、必ずしも実アプリケーションの性能を示すものではなく、指標の一つとして考えるのが妥当であろう。
4.
5.
6.
7.
8.
9.
10.
11. [LINPACK users' manual](http://books.google.ch/books?id=AmSm1n3Vw0cC&lpg=PR5&ots=EDFdqJhr8x&dq=info%3Ahttp%3A%2F%2Fs3da3171290b34600.scholar.google.com%2F0&lr&pg=SL2-PA1#v=onepage&q&f=false)
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.