> この記事は[Forth](https://ja.wikipedia.org/wiki/Forth)から翻訳されています。


**Forth**（フォース）は、[スタック](../Page/スタック.md "wikilink")指向の[プログラミング言語](../Page/プログラミング言語.md "wikilink")およびそのプログラミング環境である。Forth はしばしば、かつての習慣に従ってすべて[大文字](../Page/大文字.md "wikilink")で綴られることもあるが、[頭字語](../Page/頭字語.md "wikilink")ではない。

## 概要

Forth は[スタック指向であり](https://ja.wikipedia.org/wiki/スタック#スタック指向プログラミング言語 "wikilink")、[逆ポーランド記法](../Page/逆ポーランド記法.md "wikilink")（RPN）と同様の後置記法による記述が一番の特徴である。その他の特徴としては、[手続き型](../Page/手続き型プログラミング.md "wikilink")・[命令型であり](../Page/命令型プログラミング.md "wikilink")、言語としては全ての値は型としての区別なく扱われること（[型システム](../Page/型システム.md "wikilink")が無いこと）、制御構造などもプログラム可能であること（[リフレクション](../Page/リフレクション_\(情報工学\).md "wikilink")）といったものがある。

典型的な Forth の実装には、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink") における[Read–eval–print loop](https://ja.wikipedia.org/wiki/REPL "wikilink")（REPL）に対応する、入力されたワードを即座に実行する対話型の[インタプリタ](../Page/インタプリタ.md "wikilink")モードと（これは、正規の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")がないシステム向けの[シェル](../Page/シェル.md "wikilink")にも適している）、後の実行のために一連のワードを[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")するモードのふたつのモードがある。後者にはコロン（:）というワードにより遷移しセミコロン（;）というワードで脱する。

初期の実装や移植性を目的とした実装には[スレッデッドコード](https://ja.wikipedia.org/wiki/スレッデッドコード "wikilink")を生成するものもあるが、近年の実装では他の言語のコンパイラのように[最適化された目的コードを生成するものもある](../Page/最適化_\(情報工学\).md "wikilink")。

他の言語のシステムほどは人気はないが、商用においても Forth はいくつもの言語のベンダを引き止めるだけの十分なサポートを持っている。Forth は現在 [Open Firmware](../Page/Open_Firmware.md "wikilink") のような[ブートローダ](https://ja.wikipedia.org/wiki/ブートローダ "wikilink")や[宇宙開発](https://ja.wikipedia.org/wiki/宇宙開発 "wikilink")\[1\]、組込みシステム、[ロボット](../Page/ロボット.md "wikilink")制御などに使われている。[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")による実装であるは活発にメンテナンスされている。

## 特徴

Forth の環境はコンパイラと対話形式のシェルが一体化している。実行時環境に似ている[仮想マシン](https://ja.wikipedia.org/wiki/仮想マシン "wikilink")において、ユーザは対話的に定義し、「ワード」(words) とも[サブルーチン](../Page/サブルーチン.md "wikilink")を実行する。ソースコードとしてテスト、再定義、デバッグされることができるワードは、プログラム全体を再コンパイルしたり再起動することなく組み込まれる。変数、基本的な演算子など、すべての構文要素はプロシージャのように見える。たとえ特定のワードが最適化されても、サブルーチンの呼び出しを必要とするといけないので、これもまた依然としてサブルーチンとして有効である。言い換えれば、シェルは対話的に入力されたコマンドをそれが実行される前にマシンコードにコンパイルする（この振る舞いは一般的だが、必須ではない）。どのように結果のプログラムが格納されるかはForth 環境によってさまざまだが、理想的には手動でそのコードが再入力されたときとプログラムの実行は同じ影響を持つ。コンパイルされる関数はプログラムオブジェクトの特殊なクラスで対話的コマンドは厳密にインタープレットされる、[C言語](../Page/C言語.md "wikilink")と[Unixシェル](https://ja.wikipedia.org/wiki/Unixシェル "wikilink")の組み合わせとは対照的である。ほとんどのForth のユニークな性質はこの原理の結果である。対話性、スクリプティング、コンパイレーションがあることにより、Forth は [BBC Micro](https://ja.wikipedia.org/wiki/BBC_Micro "wikilink") や [Apple II](../Page/Apple_II.md "wikilink") シリーズのようなリソースが限られたコンピュータでよく使われ、[ファームウェア](../Page/ファームウェア.md "wikilink")や小さな[マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")などのアプリケーションで生き残っている。Cコンパイラがよりコンパクトで効率的なコードを生成しようとしている今まさにそのときでも、Forth の対話性における優位は保たれているのである。

### スタック

[再帰](../Page/再帰.md "wikilink")的な[サブルーチン](../Page/サブルーチン.md "wikilink")を持つすべてのプログラミング環境は[制御フロー](https://ja.wikipedia.org/wiki/制御フロー "wikilink")のために[スタック](../Page/スタック.md "wikilink") (stack) を実装している。この構造は典型的には[ローカル変数](../Page/ローカル変数.md "wikilink")やサブルーチンの[引数](../Page/引数.md "wikilink")も格納する（C言語のようなシステムにおける call-by-value）。Forth にはしばしばローカル変数がないこともあるが、call-by-value でもない。代わりに、中間的な値は第二のスタックにおいて保持される。ワードはスタックの最も上にある値を直接操作する。それゆえ、これは「パラメータ」または「データ」スタックと呼ばれたりもするが、ほとんどの場合は単に「スタック」である。それから、関数呼び出しスタックは「リンケージ」(lincage) もしくは「リターン」(return) スタックと呼ばれ、*rstack* とも略される。カーネルから提供された特殊な rstack 操作関数はそれがワード内で一時的なストレージとして使われることを可能にするが、その一方でこれは引数や操作データを渡すことに使うことはできない。Forthはスタックの概念をうまく利用しており、演算は[逆ポーランド記法](../Page/逆ポーランド記法.md "wikilink")により記述される。このため[構文解析](../Page/構文解析.md "wikilink")が極めて単純となり、プログラムおよび処理系が小さくて済む。これは、機器組み込み用プログラムでは有利な特徴である。

また、ルーチンは「ワード」単位で記述され、[コンパイルされる](../Page/コンパイラ.md "wikilink")。これらの「ワード」を集積して「ディクショナリ」を形成する。一般的なFORTH処理系におけるプログラミングは、[インタプリタ](../Page/インタプリタ.md "wikilink")上でのワード作成の積み重ねであり、対話的に行える。開発中でも部分的な処理を動かしてのテストがやりやすく、それらを適宜組み合わせてのテストも容易である。

ほとんどのワードはスタック上でのその効果の観点から定義される。典型的には、引数はワードが実行される前にスタックの一番上に置かれる。実行後は引数は消去され、何らかの返り値で置き換えられている。数学的な操作をするためには、これを[逆ポーランド記法](../Page/逆ポーランド記法.md "wikilink")のルールに従う。スタックの使用法を図解した以下の例を参照すること。

### 保守

Forth は単純だが拡張性のある言語である。そのモジュール性と拡張性は[CAD](../Page/CAD.md "wikilink")システムのような高度なプログラミングをも可能にする。しかしながら、拡張性は未熟なプログラマがわかりにくいコードを書くのも促すため、このことは Forth に「記述専用言語」との評判ももたらしている。大規模で複雑なプロジェクトでも成功裏に使われてきていて、有能でよく訓練されたプロフェッショナルによって開発されたアプリケーションが、何十年にもわたって発展していくハードウェアプラットフォーム上でも容易に保守されることを証明している\[2\]。Forth は天文学分野や宇宙開発分野という得意分野も持っている\[3\]。

その移植性、効率的なメモリ使用、短い開発期間および高速な実行スピードのため、Forth は今日でもいまだ多くの[組み込みシステム](../Page/組み込みシステム.md "wikilink")(小さなコンピュータ化されたデバイス)で使われている。これは近代的な[RISC](../Page/RISC.md "wikilink")プロセッサ上で効率的に実装されてきており、[マシン語としてのForthの利用も生み出されてきている](../Page/スタックマシン.md "wikilink")\[4\]。他の Forth の用途としては[アップル](../Page/アップル_\(企業\).md "wikilink")、[IBM](../Page/IBM.md "wikilink")、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")、[OLPC XO-1に使われる](https://ja.wikipedia.org/wiki/OLPC_XO-1 "wikilink")[Open Firmware](../Page/Open_Firmware.md "wikilink") [ブート](../Page/ブート.md "wikilink")ロムが含まれる。また、[FreeBSD](../Page/FreeBSD.md "wikilink")オペレーティングシステムの[FICL](http://ficl.sourceforge.net/)-based [first stage boot controllerもある](https://ja.wikipedia.org/wiki/BTX_\(boot_loader\) "wikilink")。

## 歴史

Forth は[チャールズ・ムーア](../Page/チャールズ・ムーア.md "wikilink")の[1958年](../Page/1958年.md "wikilink")から絶え間なく開発されていた個人的なプログラミングシステムから考案された\[5\]。1968年、家具と絨毯を扱う企業に雇われた際、このソフトウェアを[ミニコン上で](../Page/ミニコンピュータ.md "wikilink")[FORTRAN](../Page/FORTRAN.md "wikilink")を使って書き直したものがForthの原型である、という。Forth が他のプログラマに最初に公開されたのは[1970年](../Page/1970年.md "wikilink")代で、[アメリカ国立電波天文台](../Page/アメリカ国立電波天文台.md "wikilink")(NRAO)にいたアメリカの  によって始められたものである\[6\]。[1971年](https://ja.wikipedia.org/wiki/1971年 "wikilink")にNRAOの制御用ソフト作成において、ムーアはForthを完成させた。このNRAOにいた彼らの仕事のあと、チャールズ・ムーアとElizabeth Ratherは FORTH, Inc. を[1973年](../Page/1973年.md "wikilink")に設立し、その後の 10 年でさらに磨きをかけるとともにいくつものプラットフォームに Forth システムを移植した。

[1968年](https://ja.wikipedia.org/wiki/1968年 "wikilink")の"\[t\]he file holding the interpreter was labeled FOURTH, for 4th (next) generation software — but the [IBM 1130](https://ja.wikipedia.org/wiki/IBM_1130 "wikilink") operating system restricted file names to 5 characters."\[7\]において Forth は命名された。ムーアは compile-link-go 第三世代プログラミング言語の後継、または「第四世代」ハードウェアのためのソフトウェアとして Forth を見ており、用語として使われるようになっていた第四世代プログラミング言語 ([4GL](../Page/4GL.md "wikilink")) ではなかった。ムーアは、[アセンブラ](../Page/アセンブリ言語.md "wikilink")・FORTRAN・[BASIC](../Page/BASIC.md "wikilink")に続く4番目の言語という意味で、このソフトウェアに「fourth」と名付けるつもりだったが、このミニコンで取り扱えるファイル名は最大5文字であったため「FORTH」という名になったという。

チャールズ・ムーアはたびたび仕事を渡り歩いていたため、初期の言語開発の困難は異なる[コンピュータアーキテクチャ](https://ja.wikipedia.org/wiki/コンピュータアーキテクチャ "wikilink")への移植の容易さであった。Forth システムはしばしば新しい[ハードウェア](../Page/ハードウェア.md "wikilink")を育てるために使われていた。たとえば、Forthは[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")の新しい [Intel 8086](../Page/Intel_8086.md "wikilink") チップ上の最初の常駐ソフトウェアで、MacFORTHは[1984年](../Page/1984年.md "wikilink")の最初の[アップル](../Page/アップル_\(企業\).md "wikilink")[Macintosh](../Page/Macintosh.md "wikilink")の最初の常駐開発システムであった\[8\]。

Forth, Inc の microFORTH は[1976年](../Page/1976年.md "wikilink")に始まった[Intel 8080](../Page/Intel_8080.md "wikilink"), [Motorola 6800](../Page/MC6800.md "wikilink"), Zilog [Z80](../Page/Z80.md "wikilink") [マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")向けに開発された。MicroFORTH は　後に [1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")の [6502](https://ja.wikipedia.org/wiki/MOS_Technology_6502 "wikilink") のような他のアーキテクチャ向けの Forth システムを生成するのにホビーストたちにも使われた。広い普及は最終的に言語の標準化を誘導することとなった。共通の慣習は[事実上の標準](https://ja.wikipedia.org/wiki/事実上の標準 "wikilink")である FORTH-79\[9\] および FORTH-83\[10\] にそれぞれ[1979年](../Page/1979年.md "wikilink")、[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")に成文化された。これらの標準は[1994年](../Page/1994年.md "wikilink")に [ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")によって統合され、通常これは **ANS Forth**\[11\]（ANSI INCITS 215-1994 (R2001)、ISO/IEC 15145:1997(E)のベースとなった）と呼ぶ。

Forth は[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")代にはとてもよく使われるようになったが\[12\]、これは小さくかつ移植性が高いとして当時の小さなマイクロコンピュータにとてもよく適していたからである。すくなくともひとつのホームコンピュータ、[英国](https://ja.wikipedia.org/wiki/英国 "wikilink")の[Jupiter ACEは](https://ja.wikipedia.org/wiki/Jupiter_Ace "wikilink")　その[ROM常駐オペレーティングシステムに](../Page/Read_only_memory.md "wikilink") Forth を持っていた。[キヤノン・キャット](../Page/キヤノン・キャット.md "wikilink")もまた そのシステムプログラミングのために Forth を使っていた。さらに Rockwell も常駐 Forth カーネルを持つ R65F11 と R65F12 のシングルチップマイクロコンピュータを製造していた。

### 標準規格

  - Forth-77 Standard
  - Forth-78 Standard
  - Forth-79 Standard
  - Forth-83 Standard
  - Forth-94 Standard
  - ISO/IEC 15145:1997(E) - Information technology - Programming languages - Forth (First edition: 1997-04-15)

## プログラマの観点

Forthの後置記法は、データスタック（オペランドスタック、以下単にスタックと呼ぶ）を意識的に操作しなければならないというForthの特徴と密接に結びついている。すなわち、オペランドはそのままスタックに積まれ、後から現れる演算子などはスタックからそれを取り出して演算し、結果をスタックに積む、といったように動作する。多くの言語と違い、[バッカス・ナウア記法](../Page/バッカス・ナウア記法.md "wikilink")で構文が定義されているわけでもなく、伝統的にはコンパイラは、スレッデッドコードと呼ばれるシンプルな構造の目的コードを直接生成するだけである。また、文法の修正のような、多くの言語では実装の内部に手を入れる変更が必要なことが、Forthではそのようなワードを定義することで可能である（これは、Lispのマクロに少し似ている）。なお、データスタックの他にリターンスタックがあり、そちらはワードの呼出しの後で手続きを再開するアドレス等が積まれるスタックである（CPUのいわゆるスタックに似ている）。

たとえば、`25 * 10 + 50` は、次のように入力して計算する（「<kbd>⏎</kbd>」は、改行の入力。「ok」はForth処理系が結果の出力の後に付けるプロンプト）。

``` forth
25 10 * 50 + . ⏎
300 ok
```

[Stack1.svg](https://ja.wikipedia.org/wiki/File:Stack1.svg "fig:Stack1.svg") まず最初に数値 25 と 10 がこの順でスタックに積まれる。

[Forthstack1_5.png](https://ja.wikipedia.org/wiki/File:Forthstack1_5.png "fig:Forthstack1_5.png") ワード `*` がスタックの一番上にあるふたつの数を乗算し、その積に置き換える。

[Forthstack2.PNG](https://ja.wikipedia.org/wiki/File:Forthstack2.PNG "fig:Forthstack2.PNG") それから数値 50 をスタックに積む。

[Forthstack3.PNG](https://ja.wikipedia.org/wiki/File:Forthstack3.PNG "fig:Forthstack3.PNG") ワード `+` がこれに先ほどの積を加算する。最後に、`.` コマンドがスタックのトップを取り出して、それを、ユーザの端末に結果として出力する。

``` forth
 4 5 + .
```

これは、スタックに4を積み、さらに5を積み、スタック上の2つの値を取り出して加算、その結果をスタックに戻し、スタックの値を表示する操作を示している。

上記のように入力してエンター（⏎：リターン）を打鍵すると、画面上には下記のように結果が表示される。

``` forth
4 5 + .  ⏎
9 ok
```

Forth の構造化機能でさえもスタックベースである。たとえば、

``` forth
: FLOOR5 (n -- n')   DUP 6 < IF DROP 5 ELSE 1 - THEN ;
```

このコードは 次のコマンドを使うことによって `FLOOR5` が呼ばれる新しいワード（繰り返すが、「ワード」という単語はサブルーチンとして使われている）を定義する。`DUP`はスタックの数値を複製する。`6`がスタックの一番上に 6 を配置する。ワード `<` はスタックの一番上の二つの数（6 と `DUP` で複製された入力の値）を比較し、[真偽値](https://ja.wikipedia.org/wiki/真偽値 "wikilink")で置き換える。`IF`は真偽値をとり、その直後のコマンドを実行するか、`ELSE`までスキップするかを選択する。`DROP`はスタックの上の値を放棄する。そして、`THEN`は条件分岐の終端である。括弧に囲まれたテキストは、このワードが期待するスタックの数と値を返すかどうかを説明するコメントである。ワード `FLOOR5` は[C言語](../Page/C言語.md "wikilink")で書かれた次の関数に相当する。

``` c
 int floor5(int v) { return v < 6 ? 5 : v - 1; }
```

この関数はより簡潔につぎのように書かれる。

``` forth
: FLOOR5 (n -- n') 1- 5 MAX ;
```

このワードは次のように実行できる。

``` forth
1 FLOOR5 . ⏎
5 ok
8 FLOOR5 . ⏎
7 ok
```

最初に[インタプリタ](../Page/インタプリタ.md "wikilink")は数値 1（もしくは 8）をスタックにプッシュし、それからこの数値を再びポップし結果をプッシュする FLOOR5 を呼び出す。最後に、「.」の呼び出しは値をポップし、ユーザの[端末](../Page/端末.md "wikilink")にそれを表示する。

## 機能

Forth の[構文解析](../Page/構文解析.md "wikilink")は明確な文法がないので単純である。[インタプリタ](../Page/インタプリタ.md "wikilink")はユーザ入力デバイスから入力された行を読み、それから[区切り文字](https://ja.wikipedia.org/wiki/区切り文字 "wikilink")としての空白を使って単語に構文解析される。他の[空白文字](https://ja.wikipedia.org/wiki/空白文字 "wikilink")を認識するシステムもある。インタプリタがワードを見つけると、**ディクショナリ** (dictionary) からそのワードの検索を試みる。もしそのワードが見つかれば、インタプリタはワードに関連付けられたコードを実行し、それから入力システムの残りを構文解析するために復帰する。もしワードを発見することができないなら、ワードを[数](../Page/数.md "wikilink")だと仮定して数値への変換を試み、それをスタックにプッシュする。これが成功すれば、インタプリタは入力システムからの構文解析を継続する。辞書の参照と数値への変換の両方が失敗した場合、インタプリタはそのワードが認識できないという[エラー](../Page/エラー.md "wikilink")メッセージに続けてそのワードを表示し、入力ストリームをフラッシュし、ユーザからの新しい入力を待機する。

新規ワードの定義は、ワード`:`（コロン）から始まり、`;`（セミコロン）で終了する。たとえば、

`: X DUP 1+ . . ;`

のコードはワード `X` をコンパイルし、辞書にこの名前が発見できるようにする。コンパイルと言っても、文頭にコロン、その後にワードの名称を置き、そこから一連の式を並べておいて、文末にセミコロンを付加するだけでよい。`10 X` を[コンソール](../Page/コンソール.md "wikilink")に入力して実行すると、`11 10` が表示されるようになるだろう。

例えば、前述の式をfooという語（ワード）としてコンパイルするには、以下の通り記述する。記述法はコロン記号で始まりセミコロン記号で終わるので、「コロン定義」と呼ばれる。

```
 : foo 4 5 + . ;
```

コンパイルすることにより、FORTHの辞書（ディクショナリ）に、この語（ワード）が登録されることになる（この場合はfooが登録される）。

実のところ、FORTHでは「+」や「.」などの演算子や出力機能などの全てがワードである。こういった組み込み済みのワードと、ユーザが後からコロン定義（コンパイラ）で追加したワードと、2つの間に本質的な差異はない。コンパイルしたワードはただちに環境に組み込まれ、インタプリタより単独で実行できるようになる。つまり、そのFORTH処理系を拡張するのである。このような点より、FORTHは自己拡張性が高いと云われる。

プログラムの開発においては、処理毎に区切ってワードとして順次構築していくので、注意深く進めていけば自然ときれいに構造化されることになる。ワードは単独で実行できるため、部分に分けてのデバッグも容易である。また、それらのワードを使ってテスト用の処理（ワード）を気軽に作成して実行・テストできる。

多くの Forth システムは実行可能なワードを生成する特殊化された[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")を含む。この[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")はコンパイラの特殊な方言である。Forth アセンブラはしばしば命令の前に[引数](../Page/引数.md "wikilink")がくる逆ポーランド記法を使う。Forth アセンブラの普通の設計では命令をスタック上に構築し、それからこれを最後の段階でメモリにコピーする。Forth システムでは、番号（0..n, 実際のオペレーションコードとして使われる）付けされるかその目的に応じて名づけられた、製作者によって使われる名前でレジスタは参照されることもある。たとえば、スタックポインタとして使われるレジスタは「S」など\[13\]。

### オペレーティングシステムとファイル、マルチタスク

古典的な Forth システムでは伝統的に[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")も[ファイルシステム](../Page/ファイルシステム.md "wikilink")も使われない。コードは[ファイルに格納される代わりに](../Page/ファイル_\(コンピュータ\).md "wikilink")、[ソースコード](../Page/ソースコード.md "wikilink")は物理的なディスクアドレスに書かれたディスクブロックに格納される。ワード `BLOCK` はディスクスペースの1キロバイトサイズのブロックの数値からデータを格納しているバッファのアドレスへの変換に割り当てられ、Forth システムによって自動的に管理される。固定されたディスクブロック範囲にファイルが配置されるときには、システムのディスクアクセスが使われる実装もある。たいていはこれらはディスクブロックごとのレコードの整数をつかって、固定長バイナリレコードして実装される。高速な検索はキーデータ上の[ハッシュ](https://ja.wikipedia.org/wiki/ハッシュ "wikilink")アクセスによって実現される。

ふつうは cooperative なラウンドロビンスケジューリングであるマルチタスクは、通常利用可能である（ただし、マルチタスキング・ワードとサポートは ANSI Forth 規格ではカバーされていない）。ワード `PAUSE` は、次のタスクの配置や実行コンテキストのリストアための　現在のタスクの実行コンテキストの保存に使われる。どちらのタスクも自分自身のスタックやいくつかのコントロール変数のコピー、スクラッチエリアを持っている。タスクのスワップは単純で、効率的である。その結果、Forth マルチタスクは [Intel 8051](../Page/Intel_8051.md "wikilink"), [Atmel AVR](../Page/Atmel_AVR.md "wikilink"), and [TI MSP430のような非常に単純なマイクロコントローラでさえ有効である](https://ja.wikipedia.org/wiki/TI_MSP430 "wikilink")\[14\]。

その一方で、[Microsoft Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Linux](../Page/Linux.md "wikilink")、[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")のようなホストオペレーティングシステムのもとで実行され、ソースやデータのファイルのためにホストオペレーティングシステムのファイルシステムを利用する Forth システムもある。ANSI Forth 規格では　I/O のために使われたワードについて書かれている。他の標準的でない機能はホスト OS や[ウィンドウシステム](../Page/ウィンドウシステム.md "wikilink")へのシステムコールを発行するためのメカニズムも含み、多くはオペレーティングシステムから提供されるスケジューリングを採用する拡張を提供する。典型的には、タスク作成、一時停止、解体、および優先順位の変更のために、スタンドアロンのForthの `PAUSE`ワードとは大きくて異なったワードのセットを持っている。

### セルフコンパイルとクロスコンパイル

すべてのソースコードとともに十分な機能を有する Forth システムは自身をコンパイルすることができ、Forth プログラマはこのようなテクニックを普通メタ・コンピレーション (meta-compilation) と呼ぶ（ただし、この用語は普通の定義であるメタコンピレーションとは厳密には一致しない）。通常の方法はコンパイルされたビットをメモリに配置する一握りのワードの再定義である。コンパイラのワードはメモリ内のバッファエリアにリダイレクトされることができるフェッチとストアの、特別に命名されたバージョンを使う。このバッファエリアはコードバッファというより異なるアドレスから始まるメモリ領域へのシミュレートやアクセスをする。このコンパイラは対象のコンピュータのメモリとホストの（コンパイルする）コンピュータのメモリの両方にアクセスするワードを定義する\[15\]。

フェッチやストア操作がコード空間に再定義されたあと、コンパイラやアセンブラなどはフェッチやストアの新たな定義を使って再コンパイルされる。これはコンパイラとインタプリタのすべてのコードの効果的な再利用である。それから、Forth システムのコードはコンパイルされるが、このバージョンはバッファに格納される。このメモリ内のバッファはディスクに書きこまれ、これをテストのために一時的にメモリにロードする方法が提供される。新たなバージョンがきちんと機能するようなら、これは以前のバージョンに上書きされる。

異なる環境のためのバリエーションが多数存在する。組み込みシステム向けには、代わりに他のコンピュータのためにコードが書かれることになるが、このテクニックはクロスコンピレーションとして知られ、[シリアルポート](../Page/シリアルポート.md "wikilink")や単独の [TTL](../Page/Transistor-transistor_logic.md "wikilink") ビット越しでさえ、その上オリジナルのコンパイルするコンピュータのワード名やディクショナリの他の実行されない部分も維持する。このようなForthコンパイラのための最小の定義は　バイト単位のフェッチやストアをするワードと、実行される Forth ワード を命令するワードである。しばしばもっとも多くの時間のかかるリモートのポートへの書き込みの部分は、フェッチやストア、実行を実装するための初期化プログラムの構築であるが、多くの現代的なマイクロプロセッサ（[Motorola CPU32など](../Page/Motorola_CPU32.md "wikilink")）は、このタスクを排除する統合されたデバッグ機能を持っている\[16\]。

## 言語の構造

Forthの基本的なデータ構造は、「ワード」を実行可能なコードや名前のつけられたデータ構造を対応させる「ディクショナリ」である。このディクショナリは、門番（通常は NULL ポインタ）が発見されるまで最も新しく定義されたワードから最も古いワードまで進むリンクを用いた[連結リスト](../Page/連結リスト.md "wikilink")のツリーとして、メモリに展開される。コンテキストスイッチは異なる葉で開始するためにリスト検索を引き起こす。首位のメインの幹への枝のマージは最終的にルートの門番へ戻ってくるので、連結リスト検索は継続する 。そこはさまざまなディクショナリになることができる。メタコンピレーションのような稀なケースでは、ディクショナリは隔離されスタンドアロンである。この効果は名前空間のネストのそれに似ていて、コンテキストに依存するキーワードのオーバーロードが可能である。

定義されたワードは一般的に**ヘッド**と**ボディ**からなり、ヘッドは**名前フィールド** (NF) と**リンクフィールド** (LF) からなり、ボディは**コードフィールド** (CF) と**パラメータフィールド** (PF) からなる。

ディクショナリのエントリのヘッドとボディは、隣接していないかもしれないので別々に扱われる。たとえば、Forth プログラムが新しいプラットフォームのために再コンパイルされたとき、ヘッドはコンパイルするコンピュータに残るかもしれないが、ボディは新しいプラットフォームに行ってしまっている。組み込みシステムのようないくつかの環境によっては、ヘッドは不必要にメモリを占有する。しかしながら、もしターゲット自身が対話的なForthをサポートすることを期待されるなら、クロスコンパイラによってはヘッドをターゲット内に配置するかもしれない\[17\]。

### ディクショナリのエントリ

ディクショナリの厳密なフォーマットは規定されず、実装に依存する。しかしながら、いくつかのコンポーネントはほとんどいつも提示しており、しかし、厳密なサイズと順序は変わるかもしれない。記述された構造、ディクショナリエントリはこのように見えるかもしれない。

`structure`
`  byte:       flag           `` 3bit flags + length of word's name`
`  char-array: name           `` name's runtime length isn't known at compile time`
`  address:    previous       `` link field, backward ptr to previous word`
`  address:    codeword       `` ptr to the code to execute this word`
`  any-array:  parameterfield `` unknown length of data, words, or opcodes`
`end-structure forthword`

この名前フィールドはワードの名前の長さ（典型的には32バイト）を与えるプリフィックスで開始し、何ビットかはフラグ用である。それからワードの名前の文字表現がプリフィックスのあとに続く。特定のForth実装に依存するが、アラインメントのためひとつ以上の NUL ('0') バイトがあるかもしれない。

リンクフィールドは以前に定義されたワードへのポインタを含む。このポインタは次に古い隣接するワードへの、相対的な変位かもしれないし、絶対的なアドレスかもしれない。

このコードフィールドポインタは　コードを実行するワードのアドレスか、パラメータフィールド内のデータか、プロセッサ直接実行するであろうマシンコードの開始のいずれかになるだろう。ワードを定義するコロンでは、コードフィールドポインタはリターンスタック上の現在の Forth 命令ポインタ (instruction pointer, IP) を保存し、ワードを実行継続するための新たなアドレスを用いてIP をロードするワードを指し示す。これはプロセッサの call/return 命令が行っているのと同様である。

### コンパイラの構造

コンパイラ自身はモノリシックなプログラムではない。これは システムから可視な Forth ワードとプログラマから利用可能なものとからなっている。このことはプログラマが特殊な目的のためにコンパイラのワードを変更することを可能にする。

名前フィールド内の「コンパイル時」フラグは、「コンパイル時」の振る舞いのワードのセットである。ほとんどの単純なワードは、それがコマンドライン上で入力されたかコードに埋め込まれたかにかかわらず、同じコードが実行される。そのようにコンパイルされるとき、コンパイラはコードかワードへのスレッデッドポインタを単に配置する。

コンパイル時ワードの古典的な例は `IF` and `WHILE` といった制御構造である。Forth のすべての制御構造とほとんどすべてのコンパイラはコンパイル時ワードとして実装される。すべての Forth 制御フローワードは、プリミティブなワード`BRANCH`や`?BRANCH`（もしfalseなら分岐する）の各種の組み合わせをコンパイルするために、コンパイルの間に実行される。コンパイルの間、データスタックは制御構造のバランシング、ネスティング、ブランチアドレスのバックパッチングをサポートするのに使われる。コード断片

`... DUP 6 < IF DROP 5 ELSE 1 - THEN ...`

は定義の内側では典型的には次のような一連にコンパイルされる。

`... DUP LIT 6 < ?BRANCH 5  DROP LIT 5  BRANCH 3  LIT 1 - ...`

`BRANCH`のあとの数のは相対的なジャンプアドレスを表している。`LIT`は「リテラル」数値をデータスタックにプッシュするためのプリミティブなワードである。

#### コンパイル時と実行時

ワード `:`（コロン）は名前を引数として構文解析し、辞書にヘッダを作り（記述法はコロン記号で始まりセミコロン記号で終わるので、**コロン定義**, colon definition）、コンパイル状態に突入する。コンパイラは後続のワードをコンパイルしていく。このときワードが後述する即時ワードである場合は実行し、そうでない場合は実行時に呼び出されるようにコンパイルする。

ワード`;`（セミコロン）は現在の定義を終了し、実行状態へと復帰する。

システムの状態はワード `[`（左大括弧）及び `]`（右大括弧）を用いて手動で変更させることができ、それぞれ実行状態とコンパイル状態に突入する。ANS Forthでは、現在のインタプリタの状態は[フラグ](../Page/フラグ_\(コンピュータ\).md "wikilink") `STATE`から読み取ることができ、コンピレーションステート状態 true、そうでなければ false の値がこいる。をこのインタプリタの現在の状態による振る舞いコンパイル時**ステートスマートワード** (state-smart words) の実装を可能にする。

#### イミディエイトワード

ワード`IMMEDIATE`は、直近のコロン定義を、即時ワードにする。即時ワードは通常はコンパイル後ではなくコンピレーションの間に実行されるが、どちらのステートにおいてもプログラマにオーバーライドされることができる。`;` は即時ワードの一例である。ANS Forth では、ワードがイミディエイトとしてマークされていても、ワード `POSTPONE` は名前を引つけられたワードのコンピを強制的にコンパイルする。

#### 無名ワードと実行トークン

ANS Forth では、ワード `:NONAME` を用いて、次の`;`（セミコロン）までの後続のワードをコンパイルし、**実行トークン** (execution token) をデータスタック上に残す、無名のワードが定義できる。

ワード `EXECUTE` はデータスタックから実行トークンを取り出し、関連づけられたセマンティクスを実行することができる。またワード `COMPILE,`（COMPILE コンマ）は、データスタックから実行トークンを取り出し、コンパイルする。

ワード `'` (tick) は、ワード名を引数としてとりデータスタック上のワードに関連づけられた実行トークンを返す。

#### ワードの構文解析とコメント

ワード `:` (colon)、`POSTPONE`、`'` (tick)と `:NONAME` は、データスタックの代わりにユーザからの入力からそれらの引数をとる**構文解析ワード** (parsing words) の例である。別の例では、コロン定義において、次の右括弧を含む後続のワードを読み込んで無視し、コメントを配置するのに使われる `(`（左括弧）がある。同様に、ワード （バックスラッシュ）は現在の行の終端まで続くコメントのために使われる。

### コードの構造

ほとんどの Forth システムにおいて、コード定義のボディはマシン語といくつかの形式の[スレッデッドコード](https://ja.wikipedia.org/wiki/スレッデッドコード "wikilink")\[18\]からなる。非公式の FIG 規格 (Forth Interest Group) に従っているオリジナルの Forth は、TIL (Threaded Interpretive Language) である。これは [間接スレッディング](https://ja.wikipedia.org/wiki/スレッデッドコード#間接スレッディング "wikilink")(indirect-threading)とも呼ばれ、[直接スレッディング](https://ja.wikipedia.org/wiki/スレッデッドコード#直接スレッディング "wikilink")(direct-threading) と [サブルーチン・スレッディング](https://ja.wikipedia.org/wiki/スレッデッドコード#サブルーチン・スレッディング "wikilink")(subroutine-threading) も現在はよく使われるようになってきた。最初期のモダンな Forth はサブルーチン・スレッディングを使っており、マクロとしてシンプルなワードを挿入し、より小さく速いコードを生成するために [のぞき穴的最適化](https://ja.wikipedia.org/wiki/のぞき穴的最適化 "wikilink") や他の最適化戦略を実行した\[19\]。

### データオブジェクト

ワードが変数や他のデータオブジェクトであるとき、CPはそれを作成した定義ワードに関連付けられたランタイムコードを指している。定義ワードは特徴的な"defining behavior"（ディクショナリエントリの作成に加え、もしかしたらアロケートとデータ領域の初期化をする）を持っており、この定義しているワードによって構築されたワードのクラスのインスタンスの振る舞いの定義もする。たとえは、

  - `VARIABLE`
    初期化されていないものを命名する、one-cell memory location。`VARIABLE` のインスタンスの振る舞いはそのスタック上のアドレスを返す。
  - `CONSTANT`
    値を命名する（`CONSTANT`の引数として指定する）。インスタンスの振る舞いは値を返す。
  - `CREATE`
    位置を命名する。空間がこの場所に確保されるか、さもなくばこれは文字列か他の初期化された値を格納するためにそれがセットされることができる。インスタンスの振る舞いは、この空間の開始のアドレスを返す。

Forth は、カスタム定義の振る舞いとインスタンスの振る舞いを指定する、新しいアプリケーション特有の定義ワードをプログラマが定義できる機能もまた提供する。円形バッファ、I/Oポート上で命名されたビット、自動的にインデックス化された配列などの例がある。

これらに定義されたデータオブジェクトと同様のワードはスコープにおいてグローバルである。他の言語でローカル変数から提供された関数は、Forth ではデータスタックから提供される（しかし、Forth も真のローカル変数は持っている）。Forth のプログラミングスタイルは他の言語に比べ、ごく少数の名付けられたデータオブジェクトを使う。典型的にはこのようなデータオブジェクトは、たくさんのワードやタスク（マルチタスクの実装においては）によって使われるデータを格納するのに使われる\[20\]。

Forth は型システムを持たない。したがって値の操作は全てプログラマの責任で行われる。

## プログラミング

Forth で書かれたワードは実行可能な形式にコンパイルされる。古典的実装は、順に実行されるワードのアドレスのリストをコンパイルする。多くの現代的なシステムは実際のマシンコードを生成する（いくつかの外部ワードの呼び出しと、適当な場所に展開された他者のためのコードを含む）。最適化コンパイラをもつシステムもある。一般的な場合、Forth プログラムは実行可能形式としてロードされたとき実行されるコマンド (e.g., RUN) を含めた、Forthプログラムのコンパイル済みコードのメモリイメージとして保存されている。

開発中、プログラマは小さなコード片を開発したときに実行およびテストするためにインタプリタを使う。そのため、ほとんどの Forth プログラマは緩やかなトップダウン設計と、単体テストと統合の繰り返しによるボトムアップ開発を支持している\[21\]。

トップダウン設計では、普通まずプログラムを「語彙」へのプログラムを分割し、それらを最終的に必要なプログラムを書くための、高レベルなツールセットとして利用する。よく設計された Forth プログラムは自然言語のように読むことができ、単一の目的を達成するために用いられるだけでなく、関連する問題を解くプログラムを書くのに利用することができる\[22\]。

## コード例

### Hello world

*For an explanation of the tradition of programming "Hello World", see [Hello world](../Page/Hello_world.md "wikilink").*

実装の一つとしては、

`: HELLO  ( -- )  CR ." Hello, world!" ; HELLO `<cr>
`HELLO`

ワード `CR` (Carriage Return) は後続の出力を新しい行の上に表示するようにする。構文解析ワード `."` (dot-quote) はダブルクオートで区切られた文字列を読み、構文解析された文字列が実行時に表示されるように現在の定義にコードを追加する。文字列 `Hello, world!` からこの空白文字で区切っているワード `."` は、文字列には含まれていない。これは構文解析器が `."` を Forth ワードとして認識するために必要である。

標準的な Forth システムはインタプリタでもあり、同じ出力は次のコード片を Forth コンソールに入力することで得ることができる。

`CR .( Hello, world!)`

`.(` (dot-paren) は括弧で囲まれた文字列を構文解析し、これを表示するイミディエイトワードである。`."`と同様に、`Hello, world!` から空白文字で区切られた`.(` は文字列の一部ではない。

ワード `CR` は表示する文字列の前にくる。慣例的に、Forth インタプリタは新規行に出力を開始しない。また、慣例により、インタプリタは直前の行の終端、`ok`プロンプトの後で入力を待つ。他のプログラミング言語で時々そうであるような、Forth の `CR` にはバッファをフラッシュする暗黙の動作はない。

### コンピレーションステートとインタープリテーションステートの混用

ここに 実行されると単一の文字 `Q` を発行するワード `EMIT-Q` の定義がある。

`: EMIT-Q   81 (the ASCII value for the character 'Q') EMIT ;`

この定義は `Q` のASCII値 (81) を直接を使うことで書かれている。括弧の間の文字列はコメントで、コンパイラに無視される。ワード `EMIT` はデータスタックから値をとり、対応する文字を表示する。

次の `EMIT-Q` の再定義は、ワード`[`（左大括弧）、`]`（右大括弧）, `CHAR`、`LITERAL` をインタプリタステートを一時的に切り替えるために使っており、文字 `Q` のAscii値を計算し、コンピレーションステートを返し、計算した値を現在のコロン定義に追加する。

`: EMIT-Q   [ CHAR Q ]  LITERAL  EMIT ;`

構文解析ワード `CHAR` は空白で区切られたワードをパラメータとしてとり、データスタック上のその最初の文字の値を置く。ワード `[CHAR]` は `CHAR` のイミディエイトバージョンである。`[CHAR]`を使って、`EMIT-Q` の定義例は次のように書くことができる。

`: EMIT-Q   [CHAR] Q  EMIT ; `` Emit the single character 'Q'`

この定義はコメントを書くために （バックスラッシュ）を使っている。

`CHAR` と `[CHAR]`の両方は ANS Forth では事前に定義される。`IMMEDIATE` と `POSTPONE` と使って、`[CHAR]` はこのように定義することができる。

`: [CHAR]   CHAR  POSTPONE LITERAL ; IMMEDIATE`

### 完全な RC4 暗号プログラム

[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")、Ron Rivest は [RC4](../Page/RC4.md "wikilink") [暗号](../Page/暗号.md "wikilink")システムを [RSA Data Security, Inc.](https://ja.wikipedia.org/wiki/RSA_Data_Security,_Inc. "wikilink") のために開発した。このコードは非常に単純で、説明を読めば大抵のプログラマは書くことができる。

それぞれすべて値の異なった 256 バイトの配列がある（訳注:これが暗号ストリームの状態であり、鍵で適当に初期化する）。

この配列が使われるときはいつも、2つのバイトが交換されることによって変更される。

この交換はカウンタ *i* および *j* によって制御され、どちらも最初は 0 である。

新しい *i* を取得するには 1 を加算する。

新しい *j* を取得するには、新しい *i* の位置にある配列のバイトを加算する。

*i* と *j* の位置にある配列の値を交換する。

このコード（訳注:後のXORに使う値）は *i* と *j* の位置にある配列のバイトの和の位置にある配列のバイトである。

平文を暗号化したり暗号文を復号するためには、このバイトを XOR される。

配列は最初の設定によって 0 から 255 にかけて初期化される（訳注:手順の途中に書いてあるが、これは最初に行う）。

それから *i* と *j* を使う、*i* の位置にある配列のバイトを *j* に加算による新しい *j* とキーのバイトの取得、*i* と *j* のバイトの交換と手順は進んでいく。

最後に、*i* と *j* は 0 にセットされる。

すべての加算は 256 を法とするモジュラ演算である。

  -
    さらなる情報は、http://ciphersaber.gurus.com を参照すること。

以下の標準の Forth バージョンはコアのワードのみを使っている。

`0 VALUE ii`
`0 VALUE jj`
`CREATE S[] 256 CHARS ALLOT`

`: ARCFOUR  (c -- x)`
`   ii 1+ DUP TO ii 255 AND     ( -- i)`
`   S[] +  DUP C@           ( -- 'S[i] S[i]) `
`   DUP jj +  255 AND DUP TO jj ( -- 'S[i] S[i] j)`
`   S[] +  DUP C@ >R            ( -- 'S[i] S[i] 'S[j])`
`   OVER SWAP C!            ( -- 'S[i] S[i])`
`   R@ ROT C!           ( -- S[i])`
`   R> +                ( -- S[i]+S[j])`
`   255 AND S[] + C@            ( -- c x)`
`   XOR ;`

`: ARCFOUR-INIT (key len -- )`
`   256 MIN LOCALS| len key |`
`   256 0 DO  I  S[] I + C!  LOOP`
`   0 TO jj `
`   256 0  DO           (key len -- )`
`         key I len MOD + C@  `
`         S[] I  + C@  + jj + 255 AND TO jj`
`         S[] I  + DUP C@  SWAP (c1 addr1)`
`         S[] jj + DUP C@  (c1 addr1 addr2 c2) ROT C! C!`
`        LOOP`
`   0 TO ii  0 TO jj ;`

これはこのコードを検証する多くのテストのひとつである。

`CREATE KEY: 64 CHARS ALLOT`

`: !KEY (c1 c2 ... cn n—store the specified key of length n)`
`   DUP 63 U> ABORT" key too long (<64)"`
`   DUP KEY: C! KEY: + KEY: 1+ SWAP ?DO  I C!  -1 +LOOP ;`
` `
`   HEX  61 8A 63 D2 FB  5 !KEY`

`   KEY: COUNT ARCFOUR-INIT`

`   CR `
`      DC ARCFOUR 2 .R SPACE`
`      EE ARCFOUR 2 .R SPACE`
`      4C ARCFOUR 2 .R SPACE`
`      F9 ARCFOUR 2 .R SPACE`
`      2C ARCFOUR 2 .R`

`   CR .(Should be: F1 38 29 C9 DE)`

## 実装

Forth 仮想マシンは実装が単純で規格のリファレンス実装を持たないため、大量の言語実装が存在する。標準的な各種デスクトップコンピュータシステム ([POSIX](../Page/POSIX.md "wikilink"), [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink"), [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")) をサポートしていることに加え、これらの多くの Forth システムは各種の組み込みシステムもまた対象としている。[1994年](../Page/1994年.md "wikilink")の ANS Forth 規格に準拠するさらに有名ないくつかのシステムが列挙する。

  - [Gforth](https://ja.wikipedia.org/wiki/Gforth "wikilink") - GNUプロジェクトによる移植性の高い ANS Forth 実装
  - [Forth Inc.](http://www.forth.com/) - Forth の開発者たちによって設立され、[デスクトップ向け](../Page/デスクトップパソコン.md "wikilink") (SwiftForth) と組み込み向け (SwiftX) ANS Forth ソリューションを販売している
  - [MPE Ltd.](http://www.mpeforth.com/) - 高度に最適化されたデスクトップ (VFX) と 組み込み ANS Forth コンパイラ
  - [Open Firmware](../Page/Open_Firmware.md "wikilink") - ANS Forth に準拠した[ブートローダ](https://ja.wikipedia.org/wiki/ブートローダ "wikilink")と [BIOS](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink") の規格
  - [Freely available implementations](http://www.forth.org/compilers.html)
  - [Commercial implementations](http://www.forth.org/commercial.html)
  - プラットフォームごとにまとめられたより最新の一覧は [Forth systems](http://wiki.forthfreak.net/index.cgi?ForthSystems)

## Forthベースの言語等

  - Forthをベースにしてワードを日本語で記述可能にした言語として[Mindがある](../Page/Mind_\(プログラミング言語\).md "wikilink")
  - Forthをベースに、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")に改良した[Mac OS向けの開発システム](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")[Mops](../Page/Mops.md "wikilink")。[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")と[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")対応のPalo Alto Shipping Co.製のMach1（まっはわん）がある。
  - [Open Firmwareのシェル言語はForthベースである](../Page/Open_Firmware.md "wikilink")。SunのOpenBoot PROM（OBP）やCHRPベースのPower Macintoshの起動用[ファームウェア](../Page/ファームウェア.md "wikilink")はOpen Firmwareの実装である。
  - Forthを元にしたコマンド言語である[Ficl](https://ja.wikipedia.org/wiki/Ficl "wikilink")は[FreeBSD](../Page/FreeBSD.md "wikilink")のブートローダの実装に使われている。
  - 1985年ごろ、服飾メーカーとして知られる[JUN](../Page/JUN.md "wikilink")（株式会社ジュン）が開発したコンピュータグラフィックシステム[4D-Box](https://ja.wikipedia.org/wiki/4D-Box "wikilink")のオペレーション言語[0DL](https://ja.wikipedia.org/wiki/0DL "wikilink")はForthであった。

## 似た言語等

  - [PostScript](../Page/PostScript.md "wikilink")は、作者によれば影響されたものではないとしているが、Forthと同じく後置記法でスタック指向であり、類似性が指摘されることがある。
  - [TeleScript](https://ja.wikipedia.org/wiki/TeleScript "wikilink") [General Magic社が開発](https://ja.wikipedia.org/wiki/General_Magic "wikilink")・提供していた次世代エージェント指向の通信用プログラム言語。Forthアーキテクチャで実装されていた。

## 脚注

## 参考文献

  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
## 関連項目

  - [スタックマシン](../Page/スタックマシン.md "wikilink")
  - [colorForth](https://ja.wikipedia.org/wiki/colorForth "wikilink")
  - [pforth](https://ja.wikipedia.org/wiki/pforth "wikilink")
  - [Factor](../Page/Factor.md "wikilink")
  - [Joy (プログラミング言語)](https://ja.wikipedia.org/wiki/Joy_\(プログラミング言語\) "wikilink")
  - [STOIC](https://ja.wikipedia.org/wiki/STOIC "wikilink")
  - [Open Firmware](../Page/Open_Firmware.md "wikilink")

## 外部リンク

  - [Forth Interest Group (FIG)](http://www.forth.org/)
  - [Gforth](http://www.complang.tuwien.ac.at/forth/gforth/)（[GNU](../Page/GNU.md "wikilink")によるフリーのForth処理系）

<!-- end list -->

  - [comp.lang.forth](news://comp.lang.forth) - 活発な Forth の議論のある[Usenet](https://ja.wikipedia.org/wiki/Usenet "wikilink")ニュースグループ

  - [Forth Chips Page](http://www.ultratechnology.com/) — ハードウェアにおける Forth

  - [A Beginner's Guide to Forth](http://galileo.phys.virginia.edu/classes/551.jvn.fall01/primer.htm) by J.V. Noble

  - [Forth Links](http://forthlinks.com)

  - [Various Forth variants and ANSI docs](http://www.taygeta.com/forth.html)

  - [Starting FORTH](http://www.forth.com/starting-forth/) Leo Brodie により 1981年に出版された FORTH 入門書のオンラインバージョン

  - [Thinking Forth Project](http://thinking-forth.sourceforge.net/) 1984年に Leo Brodie により出版された独創的な書籍 Thinking Forth の21世紀版（2004年）など

  - [レオ・ブロディー(Leo Brodie) 著「Forth思考 ―問題解決のための言語と哲学―（原文2004年版）」](https://thinking-forth-ja.readthedocs.io/ja/latest/index.html)

  - [Computerworld Interview with Charles H. Moore on Forth](http://www.techworld.com.au/article/250530/-z_programming_languages_forth)

  - [FORTH Retro Podcast](http://retrobits.libsyn.com/index.php?post_id=456803) in two parts ([part I](http://retrobits.libsyn.com/index.php?post_id=456803), [part II](http://retrobits.libsyn.com/index.php?post_id=482023))

  -

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:仮想機械](https://ja.wikipedia.org/wiki/Category:仮想機械 "wikilink")

1.  [NASA applications of Forth](http://forth.gsfc.nasa.gov/)
2.
3.
4.
5.
6.
7.  {{ cite web | last = Moore | first = Charles H | year = 1991 | url = <http://www.colorforth.com/HOPL.html> | title = Forth - The Early Years | accessdate = 2006-06-03 }}
8.
9.
10.
11. {{ cite web | publisher = ANSI technical committee X3J14 | date = 24 March 1994 | url = <http://www.taygeta.com/forth/dpans.html> | title = Programming Languages: Forth | accessdate = 2006-06-03 }}
12.
13. {{ cite web | last = Rodriguez | first = Brad | url = <http://www.zetetics.com/bj/papers/6809asm.txt> | title = B.Y.O.ASSEMBLER | accessdate = 2006-06-19 }}
14. {{ cite web | last = Rodriguez | first = Brad | url = <http://www.zetetics.com/bj/papers/8051task.pdf> | title = MULTITASKING 8051 CAMELFORTH | format = PDF | accessdate = 2006-06-19 }}
15. {{ cite web | last = Rodriguez | first = Brad | year = 1995 | month = July | url = <http://www.zetetics.com/bj/papers/moving8.htm> | title = MOVING FORTH | accessdate = 2006-06-19 }}
16. {{ cite web | last = Shoebridge | first = Peter | date = 1998-12-21 | url = <http://www.zeecube.com/archive/bdm/index.htm> | title = Motorola Background Debugging Mode Driver for Windows NT | accessdate = 2006-06-19 }}
17.
18. [マルチスレッド・プログラミング](https://ja.wikipedia.org/wiki/マルチスレッド・プログラミング "wikilink")とは異なる
19.
20.
21.
22. The classic [washing machine example](http://www.forth.com/embedded/swiftx-embedded-systems-7.html) describes the process of creating a vocabulary to naturally represent the problem domain in a readable way.