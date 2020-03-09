> この記事は[BASIC](https://ja.wikipedia.org/wiki/BASIC)から翻訳されています。


**BASIC**（ベーシック）は[手続き型プログラミング](https://ja.wikipedia.org/wiki/手続き型プログラミング "wikilink")言語のひとつ。

名前は「」（「初心者向け汎用記号命令コード」を意味する）の[バクロニム](https://ja.wikipedia.org/wiki/バクロニム "wikilink")である。

## 概要

いくつかの点で[FORTRAN](../Page/FORTRAN.md "wikilink")に似ている。構文は、FORTRANの文法が基になっているとしばしば解説されている。初心者向けの[プログラミング言語](../Page/プログラミング言語.md "wikilink")として、[1970年代](https://ja.wikipedia.org/wiki/1970年代 "wikilink")以降の[コンピュータ](https://ja.wikipedia.org/wiki/コンピュータ "wikilink")（特に[パソコン](../Page/パーソナルコンピュータ.md "wikilink")）で広く使われた。標準規格である[Full BASICの仕様は](https://ja.wikipedia.org/wiki/#Full_BASIC "wikilink")、よく知られているBASICとは異なり構造化などがきちんとしており、また [Microsoft Visual Basic .NET](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink") の仕様はよく知られているBASICとは全く異なりむしろFull BASICに近い、現代における有力な言語環境のひとつである。

### プログラム例と出力例

画面に次のように入力したとする。

``` basic
 10 REM 5つ数える
 20 FOR I = 1 TO 5
 30 PRINT I
 40 NEXT
 RUN
```

`RUN`命令を入力すると、それ以前に入力された[プログラムが実行される](https://ja.wikipedia.org/wiki/プログラム_\(コンピュータ\) "wikilink")。この場合の出力は次のとおり。

`1`
`2`
`3`
`4`
`5`

また、プログラムに編集を加えたい場合、続いて例えば次のように入力する。

``` basic
 10 REM 5つ数える(“3”だけ飛ばす)
 25 IF I = 3 THEN GOTO 40
 RUN
```

このように入力すると、`10`で始まる行が書き換えられ、20行目と30行目の間に25行目が挿入される。この場合の出力は次のとおり。

`1`
`2`
`4`
`5`

### 主な特徴

  - 歴史的な経緯から、[FORTRAN](../Page/FORTRAN.md "wikilink")やパソコンでは[C言語](../Page/C言語.md "wikilink")と比較されることが多い。
  - [高水準言語](https://ja.wikipedia.org/wiki/高水準言語 "wikilink")である。
  - （[ダートマスBASIC](https://ja.wikipedia.org/wiki/ダートマスBASIC "wikilink")はコンパイルしているが）[インタプリタ](https://ja.wikipedia.org/wiki/インタプリタ "wikilink")として実装された処理系が多い。
  - 編集環境を兼ねた一種の[シェル](https://ja.wikipedia.org/wiki/シェル "wikilink")のような[コマンドラインインタプリタ](https://ja.wikipedia.org/wiki/コマンドラインインタプリタ "wikilink")を持つものも多いが、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")の[REPL](https://ja.wikipedia.org/wiki/REPL "wikilink")のように洗練されたものではない。
  - 古いBASICではすべての行頭に[行番号](https://ja.wikipedia.org/wiki/行番号 "wikilink")を必要とし、GOTO文などの飛び先は行番号で指定する。行番号は、[テレタイプ端末](https://ja.wikipedia.org/wiki/テレタイプ端末 "wikilink")時代に処理系と一体の行指向[テキストエディタ](https://ja.wikipedia.org/wiki/テキストエディタ "wikilink")で扱うのに便利であった。現在でも[互換性](https://ja.wikipedia.org/wiki/互換性 "wikilink")のために両者を残している処理系もある。
  - 本来は、**RUN**などのように、プログラム外から処理系に指示を与えるものは[コマンド](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")（**命令**）、**FOR**などのようにプログラム中のものは**ステートメント**（[文](https://ja.wikipedia.org/wiki/文_\(プログラミング\) "wikilink")）、と、本来は（ダートマスBASICでは）明確な区別があったが、次第に混同されていった。
  - プログラム中の[予約語](https://ja.wikipedia.org/wiki/予約語 "wikilink")（キーワード）には文の他に関数がある。それらと同じ名前を変数に使うことはできない（Tiny BASIC等では変数は一文字といったものも多い）。
  - 文字列変数の内容等を除いて、大文字と小文字を区別しない。入力の時点で全て大文字に変換される処理系もあった。
  - 算術[演算子](https://ja.wikipedia.org/wiki/演算子 "wikilink")以外の[記号](https://ja.wikipedia.org/wiki/記号 "wikilink")は極力使わない。論理演算子は`AND`、`OR`、`XOR`、`NOT`である。[括弧](https://ja.wikipedia.org/wiki/括弧 "wikilink")は[演算の優先順位](https://ja.wikipedia.org/wiki/演算の優先順位 "wikilink")も、[関数の](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")[引数](https://ja.wikipedia.org/wiki/引数 "wikilink")も、[配列](https://ja.wikipedia.org/wiki/配列 "wikilink")もすべて「`()`」のみを用いる。ブロックも「`{}`」のような括弧ではなく「`FOR`文から`NEXT`文までの間」といった構文により指定する。
  - 代入と比較はどちらも「`=`」である。代入はLET文とするのが本来の形だが（文は全てキーワードから始まる、という規則により）、「`A = 1`」のような、キーワード「LET」を省略した代入の構文が好まれた。
  - [ファーストクラスの型は数値型と](https://ja.wikipedia.org/wiki/第一級オブジェクト "wikilink")[文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")型である。数値は[浮動小数点数](https://ja.wikipedia.org/wiki/浮動小数点数 "wikilink")だけのものもあるが、整数型などがあるものもある。文字列型の変数名は末尾に「`$`」を付ける、といった規則のものもある。
  - LEFT$, MID$, RIGHT$など、文字列操作関数が豊富なことが多い。
  - 明示的な変数宣言を必要とせず、変数を使用し始めたところで宣言したものと解釈される。
  - 使ったことのない変数を使うと勝手に変数が作られ、また中身は自動的に初期化される（数値型は0、文字列型は[空文字列](https://ja.wikipedia.org/wiki/空文字列 "wikilink")）。
  - プログラムは先頭行から実行される。

## 歴史

[1964年](https://ja.wikipedia.org/wiki/1964年 "wikilink")、[米国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[ダートマス大学](https://ja.wikipedia.org/wiki/ダートマス大学 "wikilink")にて、数学者[ジョン・ケメニー](https://ja.wikipedia.org/wiki/ジョン・ジョージ・ケメニー "wikilink")（[1926年](https://ja.wikipedia.org/wiki/1926年 "wikilink")-[1992年](https://ja.wikipedia.org/wiki/1992年 "wikilink")）とトーマス・カーツ（[1928年](https://ja.wikipedia.org/wiki/1928年 "wikilink")-）により、教育用などを目的として[ダートマスBASIC](https://ja.wikipedia.org/wiki/ダートマスBASIC "wikilink")が開発された。これは同時期にともに開発された、[タイムシェアリングシステム](https://ja.wikipedia.org/wiki/タイムシェアリングシステム "wikilink")[DTSS](https://ja.wikipedia.org/wiki/DTSS "wikilink")上の[ラインエディタ](https://ja.wikipedia.org/wiki/ラインエディタ "wikilink")（テレタイプ端末環境）で利用されるよう設計されていた。

BASICは、[GEとの提携を経て](https://ja.wikipedia.org/wiki/ゼネラル・エレクトリック "wikilink")、学外にも普及した。ダートマス大学のオリジナルは[コンパイラ](../Page/コンパイラ.md "wikilink")だったが（ただし、完全オンメモリ動作・1パスという、きわめて軽く動作するものであり、言語仕様もそのような「軽い」コンパイルのために設計されている）パソコンなどの商用版では基本機能を最小限にしたうえで[インタプリタ](https://ja.wikipedia.org/wiki/インタプリタ "wikilink")として実装されることが多く、独自の発展を遂げた。

### 8ビットパソコンの普及とBASIC

[1970年代](https://ja.wikipedia.org/wiki/1970年代 "wikilink")末から[1980年代](../Page/1980年代.md "wikilink")初頭にかけて、[8ビット](https://ja.wikipedia.org/wiki/8ビット "wikilink")[CPU](https://ja.wikipedia.org/wiki/CPU "wikilink")を使った自作[コンピュータ](https://ja.wikipedia.org/wiki/コンピュータ "wikilink")で[Tiny BASICを動かし](https://ja.wikipedia.org/wiki/Tiny_BASIC "wikilink")、その上でゲームを実行させる（[スタートレック](https://ja.wikipedia.org/wiki/スタートレック "wikilink")ゲーム等）のがホビーストの目標となった。

同時に、 メーカー製の[ターンキーシステム](https://ja.wikipedia.org/wiki/ターンキーシステム "wikilink")にBASICインタプリタが[ROMの形で搭載されはじめ](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")、一気に当時のマイコンにおける標準言語の立場を獲得した。この時に搭載されたBASICインタプリタはほとんどが[マイクロソフト](https://ja.wikipedia.org/wiki/マイクロソフト "wikilink")製で、同社躍進のきっかけとなった。また、マイクロソフト製BASICは、中間コードを使用する構造になっており、また汎用機を再現した極めて[エミュレータに近いランタイム形式の実行環境だったため](https://ja.wikipedia.org/wiki/エミュレータ_\(コンピュータ\) "wikilink")、当時の互換性が皆無なコンピュータ事情の中でも、スクリプト自体の移植は容易だった。

その後、（[MS-DOS](https://ja.wikipedia.org/wiki/MS-DOS "wikilink")発表以前の）パソコンに、操作を提供するのにも使われ、しばしば[ROM-BASIC](https://ja.wikipedia.org/wiki/ROM-BASIC "wikilink")として[ハードウェア](https://ja.wikipedia.org/wiki/ハードウェア "wikilink")に組み込まれた。 電源投入後にエディタ込みで利用できることから、現在における、シェル、[インタフェースとしての役割ももち](https://ja.wikipedia.org/wiki/インタフェース_\(情報技術\) "wikilink")、ローダなどの役割も担った。 入力の効率化のため、省略形式での入力や、1980年代後半には、[漢字](https://ja.wikipedia.org/wiki/漢字 "wikilink")の利用や、[ラベル](https://ja.wikipedia.org/wiki/ラベル "wikilink")、[インデント](https://ja.wikipedia.org/wiki/インデント "wikilink")への内部的な対応、C言語への橋渡しなど、様々な機種ごとの独自の発展を遂げた。

他の言語の進化に伴いBASICはあくまで初心者向けの言語でありプロにとっては論外のものということになった。しかし一方でプログラミングの専門家以外の人がプログラミングをするのにBASICが重宝されることも依然多い。例えば[UBASIC](https://ja.wikipedia.org/wiki/UBASIC "wikilink")や[十進BASIC](https://ja.wikipedia.org/wiki/十進BASIC "wikilink")はいずれも数学者が開発したものである。 また、当時のPCの処理速度から、処理の高速化が必要な部分はデータ形式でアセンブリ言語による処理を呼び出すなどの手法もとられた。

### 互換性とBASIC

[thumbのN](https://ja.wikipedia.org/wiki/ファイル:N-88BASIC_v1.0.gif "wikilink")88BASIC\]\] 各メーカーのパソコンに標準搭載されたBASICは、機種ごとに画面操作やI/O直接操作などの独自拡張が行われた。マイクロソフト製（[MS-BASIC](https://ja.wikipedia.org/wiki/MS-BASIC "wikilink")、[BASICA](https://ja.wikipedia.org/wiki/BASICA "wikilink")、[G-BASIC](https://ja.wikipedia.org/wiki/G-BASIC "wikilink")、[GW-BASIC](https://ja.wikipedia.org/wiki/GW-BASIC "wikilink")の移植版）のものや、その命令体系を引継ぎ実装したものである、[F-BASIC](https://ja.wikipedia.org/wiki/F-BASIC "wikilink")、[Hu-BASIC](https://ja.wikipedia.org/wiki/Hu-BASIC "wikilink")、[カタカナ](https://ja.wikipedia.org/wiki/カタカナ "wikilink")で表現するG-BASIC（前述のマイクロソフトの物とは異なる）、PETに由来する[S-BASIC](https://ja.wikipedia.org/wiki/S-BASIC "wikilink")、[SEGA](https://ja.wikipedia.org/wiki/SEGA "wikilink")のベーシックカートリッジ、Cを意識したX-BASICなど各社が独自にBASICを開発し、いわゆる「[方言](https://ja.wikipedia.org/wiki/方言_\(プログラミング言語\) "wikilink")」が生まれた。この結果、たとえBASICのメーカーが同じでも「あるパソコンで作ったBASICプログラムは、他のパソコンではそのままでは動かすことができない」ことの方がずっと多かった。

もっとも当時は群雄割拠の時代でもあり、特に市販ソフトが満足に出なくなったパソコンにおいては、BASICは重要な役割を果たした。

#### 方言の例

  - [カーソル](https://ja.wikipedia.org/wiki/カーソル "wikilink")位置を指定する`LOCATE`文は、別の処理系では`CURSOR`文
  - 音楽を演奏する`PLAY`文、`MUSIC`文とそれらに記述される[MML](https://ja.wikipedia.org/wiki/Music_Macro_Language "wikilink")
  - 画面モードを指定する`CONSOLE`文
  - [スプライト機能を使用する命令](https://ja.wikipedia.org/wiki/スプライト_\(映像技術\) "wikilink")
  - VRAMと配列変数の内容をやりとりする命令
  - 条件付きループを実現する`WHILE`〜`WEND`
  - `GOTO`, `GOSUB`文の飛び先を指定するラベル
  - `CALL`, `CMD`, `SET`などで始まる命令文

#### メイン・メモリの制限による処理系の実装例

初期のTiny BASICはともかくとしても、BASIC実装処理系のメイン・メモリの制限により言語仕様が極めて制限された実装が存在した。

  - 数値型は整数型のみ、また数値演算は整数演算のみ
  - 変数名は頭文字1文字または2文字程度しか認識しない
  - 文字列の長さが限られる（255文字など）
  - 配列の大きさ（添字の最大値）が限られる

#### 中間コードサイズを小さくしたり処理を速くする主なテクニック

処理プログラムの大きさや速度の制限を改善あるいは回避するテクニックを紹介する。いくつかは、ソースの読みやすさを犠牲にするようなテクニックでもあった。

  - プログラムの初めに全ての変数のデフォルトを整数だと宣言する（`DEFINT A-Z`）。これはきちんと%などを付けて整数変数として書いてあるプログラムでは意味がないし、小数演算があるプログラムなのにこれを書くとまともに動かなくなる。整数の範囲の演算しかしていないが、%を付けずに書かれているプログラムを後から改善する場合だけに意味のあるテクニック。
  - 命令を省略形で書く（`PRINT`→`?`、`LET A=B`→`A=B`、`REM`→`'` など）

<!-- end list -->

  -
    ただし、中間コードを採用している処理系では、`?`と入力しても`PRINT`に展開されるので、結果は変わらない。また、`REM`を`'`と書くのはかえってサイズが増える。

<!-- end list -->

  - 余白やコメントを入れない
  - `NEXT`の変数名を省略する（可能な処理系のみ）
  - 一行に複数の文を詰め込んで（マルチステートメント）を使用して行の制限一杯に命令文を詰め込む
  - よく使う変数は早めに確保する（実行時に毎回変数領域の先頭から検索されるため）
  - よく呼び出すサブルーチンは先頭に配置する（同じような理由。なお、一度通過した`GOTO`/`GOSUB`命令のオペランドを内部で行番号からメモリアドレスに書き換える処理系ではあまり効果がない）
  - キャラクタコードをバイナリと見立て、バイナリに相当するデータを直接プログラムに記述する

### コンパイラ

次のような[コンパイラ](../Page/コンパイラ.md "wikilink")がある。

  - *BASCOM*（マイクロソフト BASIC-80 [CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")用インタプリタ）
  - MS-DOS用[N88-BASIC](https://ja.wikipedia.org/wiki/N88-BASIC "wikilink")コンパイラ（[日本電気](https://ja.wikipedia.org/wiki/日本電気 "wikilink") [PC-9800シリーズ](https://ja.wikipedia.org/wiki/PC-9800シリーズ "wikilink")）
  - F-BASIC386コンパイラ（[富士通](../Page/富士通.md "wikilink") [FM TOWNS](../Page/FM_TOWNS.md "wikilink")）
  - [MSXべーしっ君](https://ja.wikipedia.org/wiki/MSX-BASIC "wikilink")（[アスキー](https://ja.wikipedia.org/wiki/アスキー_\(企業\) "wikilink") [MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")）
      - [実行ファイル](https://ja.wikipedia.org/wiki/実行ファイル "wikilink")は生成しない
  - [X-BASIC](https://ja.wikipedia.org/wiki/X-BASIC "wikilink")コンバーター（[シャープ](https://ja.wikipedia.org/wiki/シャープ "wikilink") [X68000](https://ja.wikipedia.org/wiki/X68000 "wikilink")）
      - [C言語](../Page/C言語.md "wikilink")に変換した上でのコンパイル
  - [FreeBASIC](https://ja.wikipedia.org/wiki/FreeBASIC "wikilink")コンパイラ([Microsoft_Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink"),[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink"),[DOSエクステンダ](https://ja.wikipedia.org/wiki/DOSエクステンダ "wikilink"),[Xbox](https://ja.wikipedia.org/wiki/Xbox_\(ゲーム機\) "wikilink"))
      - フリーで[GPL形式の](https://ja.wikipedia.org/wiki/GNU_General_Public_License "wikilink")[80386向けコンパイラで現代向けに多数の機能](../Page/Intel_80386.md "wikilink")（GUIアプリケーション作成や[オブジェクト指向プログラミング](https://ja.wikipedia.org/wiki/オブジェクト指向プログラミング "wikilink")機構の搭載[OpenGL](https://ja.wikipedia.org/wiki/OpenGL "wikilink")、[SDL](https://ja.wikipedia.org/wiki/SDL "wikilink")等多数の[ライブラリ](https://ja.wikipedia.org/wiki/ライブラリ "wikilink")を使用可能）追加が行われているが[QuickBASIC](https://ja.wikipedia.org/wiki/QuickBASIC "wikilink")との互換性も有る

しかし、パソコンに内蔵または標準添付されていたインタプリタと違い、コンパイラは別売であったり、高価であったり、実行には[ランタイムライブラリ](https://ja.wikipedia.org/wiki/ランタイムライブラリ "wikilink")を必要であったりする場合があった。このことから、BASICインタプリタによる開発に習熟したユーザーは、より高速で柔軟なプログラムを求めて、[機械語](https://ja.wikipedia.org/wiki/機械語 "wikilink")（[アセンブリ言語](https://ja.wikipedia.org/wiki/アセンブリ言語 "wikilink")）や、[C言語](../Page/C言語.md "wikilink")などに移行していった。

また、コンパイラと称していても、実際はインタプリタと[ソースコード](https://ja.wikipedia.org/wiki/ソースコード "wikilink")を同梱した[実行ファイル](https://ja.wikipedia.org/wiki/実行ファイル "wikilink")を作るだけ、というものもある。[中間表現](https://ja.wikipedia.org/wiki/中間表現 "wikilink")と、そのインタプリタ、という構成のものもある。

### 構造化とBASIC

急速に広まったBASICだが、構造化機能の無いBASICは教育に使うな、などと[コンピュータサイエンティストの一部から酷評されたりもした](https://ja.wikipedia.org/wiki/計算機科学 "wikilink")。BASIC批判の急先鋒としては[エドガー・ダイクストラ](../Page/エドガー・ダイクストラ.md "wikilink")の[1975年](https://ja.wikipedia.org/wiki/1975年 "wikilink")の発言\[1\]などが知られる（[Apple IIなどのパソコンが普及する以前の発言であることに注意](https://ja.wikipedia.org/wiki/Apple_II "wikilink")）。

局所変数が無いことなど問題は多いが、しばしばGOTOのような見た目にわかりやすい事柄ばかりが取り上げられがちである。

### 標準化

#### 基本BASIC

BASICの標準化が望まれたが、マイコンの急激な発展と、各メーカーの独自拡張が魅力であったという事情により、結局どの機種のBASICでも変わりが無いようなごく基本的な機能に絞った仕様が標準として制定された。ANSI X3.60-1978「American National Standard for the Programming Language Minimal BASIC」は、日本では JIS C 6207-1982「電子計算機プログラム言語 基本BASIC」として規格化された。制定直後にJISの分類の再編があり、電気電子のCから情報のXに移動してJIS X 3003となったが、次節のFull BASICのJIS化の際に改訂として同じ番号を使うという形で旧規格として消滅した。

日本では[1990年代](../Page/1990年代.md "wikilink")後半から、[高等学校](https://ja.wikipedia.org/wiki/高等学校 "wikilink")や[大学入試センター試験](https://ja.wikipedia.org/wiki/大学入試センター試験 "wikilink")の数学に、標準化された基本BASICの範囲で書かれたプログラミングが扱われるようになった。

#### Full BASIC

[ダートマスBASIC](https://ja.wikipedia.org/wiki/ダートマスBASIC "wikilink")は、他のBASIC（ケメニーらは「ストリート」BASIC、と呼んだ\[2\]）とは異なって既に1970年代後半から構造化などが進んでおり、ANSIでは新しい規格の策定も進んでいたが、これをパソコン向けにアレンジした[True BASICが](https://ja.wikipedia.org/wiki/True_BASIC "wikilink")、1984年に開発された（日本では[クレオから発売](https://ja.wikipedia.org/wiki/クレオ_\(ソフトウェア\) "wikilink")）。構造化の他、行列演算の機能など、学術的（特に数学的）な方面の拡張も特徴である。そしてTrue BASICとほぼ同一の構造化BASICである[Full BASICが](https://ja.wikipedia.org/wiki/Full_BASIC "wikilink")**ISO/IEC 10279** (Information technology−Programming languages −Full BASIC)が1991年に [INCITS](https://ja.wikipedia.org/wiki/情報技術規格国際委員会 "wikilink")/[ISO/IEC JTC 1によって](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink")、[JIS](https://ja.wikipedia.org/wiki/日本産業規格 "wikilink") は JIS X 3003-1993『電子計算機プログラム言語 Full BASIC , The Programming Language Full BASIC』 が1993年に規格化された。

  - Full BASICの主な特徴

:\*構造化に対応する制御文を追加した（`DO`〜`LOOP`、`DO WHILE`〜`LOOP WHILE`など）

:\*`IF`文が多行に渡るブロック`IF`（`IF`〜`THEN`〜`ELSE`〜`ENDIF`）も可能となった

:\*`LET`を省略できないようにした（True BASICでは`OPTION NOLET`または`NOLET`を実行すると省略可能）

:\*[スコープ](https://ja.wikipedia.org/wiki/スコープ "wikilink")の概念を取り入れた

:\*\*外部副プログラム（`EXTERNAL SUB`〜`END SUB`）や外部関数（`EXTERNAL FUNCTION`〜`END FUNCTION`）の中で[ローカル変数](https://ja.wikipedia.org/wiki/ローカル変数 "wikilink")が使用できるようになった

:\*\*副プログラムと関数は戻り値を戻すかどうかで区別される

:\*\*[再帰](https://ja.wikipedia.org/wiki/再帰 "wikilink")処理の実装が容易になった

:\*計算精度や丸めの方法を規定した

:\*配列の添字を1から始めるようにした（`OPTION BASE`命令で0から始まるようにすることも可能）

:\*[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")演算機能

:\*構文のアドホックな所などを極力排除した

:\*予約語を極力少なくした

:\*I/Oを直接操作するなどシステムに干渉する命令は持たないようにした（True BASICでは拡張ライブラリとして提供）

:\*グラフィック命令を規定した。なお、(0, 0) が、デフォルトでは、コンピュータ系に多い左上ではなく数学などで伝統的な左下である（変更できる。高機能なBASICに多かった、任意にスクリーンとウインドウのそれぞれの座標を設定できるタイプである）

:\*Minimal BASICの上位互換である

:\*パソコン向けのそれまでのBASICとは命令の互換性が低い

:\*\*サブルーチン（`GOSUB`〜`RETURN`）は規格として残ってはいるが、使用は推奨されない

### その他の現代化BASIC

#### QuickBASIC

マイクロソフトはFull BASIC規格の策定には参加しなかったが、[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")にFull BASICに類した構造化や特徴を追加した独自規格の[QuickBASIC](https://ja.wikipedia.org/wiki/QuickBASIC "wikilink")を発売した。これは自社のMS-DOS用の[GW-BASIC](https://ja.wikipedia.org/wiki/GW-BASIC "wikilink")の上位互換で、コンパイラ並に動作を高速にした上にコンパイルも出来るようにしたもので、Version4.5まで発売した後に[1991年](https://ja.wikipedia.org/wiki/1991年 "wikilink")の[Visual Basicへと繋がっていった](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")。

QuickBASIC との互換性を考慮した[フリーなBASICとして](../Page/フリーソフトウェア.md "wikilink")や[FreeBASIC](https://ja.wikipedia.org/wiki/FreeBASIC "wikilink")がある。

#### RATBAS

構造化ということを意識していなかったパソコン用のROM/Disk-Basic環境で、構造化プログラムを記述するために作られた[プリプロセッサ](https://ja.wikipedia.org/wiki/プリプロセッサ "wikilink")である。[アスキーの書籍の形](https://ja.wikipedia.org/wiki/アスキー_\(企業\) "wikilink")（アスキー書籍編集部編著「構造化BASIC RATBASのすすめ」 (ISBN 978-4-87148-152-6) ）で、[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に公開された。

これは、独自の構造化された構文で記述されたソースプログラムを処理し、行番号やGOTO文を使うROM/Disk-Basicに変換するプログラムで、すべてBasicで記述されていた。RATBASという名前は構造化Fortranの[Ratfor](https://ja.wikipedia.org/wiki/Ratfor "wikilink")などに倣ったものである。

RATBASは、[スタンドアローン](https://ja.wikipedia.org/wiki/スタンドアローン "wikilink")のBasicプログラムと、[μ-UXの外部コマンドとして作成されたサブセット版がある](https://ja.wikipedia.org/wiki/Uni+ "wikilink")。μ-UXとは、[年刊AhSKI\!](https://ja.wikipedia.org/wiki/年刊AhSKI! "wikilink")の[1984年](../Page/1984年.md "wikilink")号に掲載された、Disk-Basicで記述されたUnix風のオペレーティング環境である[Uni+](https://ja.wikipedia.org/wiki/Uni+ "wikilink")を拡張したものである。

#### その他

海外では[ボーランド](https://ja.wikipedia.org/wiki/ボーランド "wikilink")が独自に[ALGOL](https://ja.wikipedia.org/wiki/ALGOL "wikilink")風の拡張を施した[Turbo Basicを発売した](https://ja.wikipedia.org/wiki/Turbo_Basic "wikilink")。

### GUI時代とBASIC

近年ではマイクロソフトの独自拡張による[RAD環境](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")[Visual Basic](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink") (VB) や、[MS Officeなどで動作するそのサブセット](https://ja.wikipedia.org/wiki/Microsoft_Office "wikilink")[Visual Basic for Applications](https://ja.wikipedia.org/wiki/Visual_Basic_for_Applications "wikilink") (VBA)が[Windowsにおける代表的な](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")のひとつとして広く利用されている。もっともVisual Basicは、GUIに特化したRAD環境として大幅に拡張が施され、元のBASIC言語とは、かけ離れてしまっている。

BASICは依然として初心者向けの言語ではあるが、パソコンに添付されることはなくなった。プログラムの入門でもBASICを使わず、最初から[C言語](../Page/C言語.md "wikilink")などで教える教育機関も多い。無料で使える[Java](https://ja.wikipedia.org/wiki/Java "wikilink")などの、洗練された後発言語の普及により、開発環境としては選択肢の一つでしかなくなった。

また、コンパイラで開発した場合、実行ファイルとは別に、巨大なランタイムライブラリが必要となる処理系が多い。このため配布に必要なファイルのサイズが大きくなり、敬遠されることがある。それでもBASICは、依然として使われているのも事実である。

### オブジェクト指向とBASIC

現在、BASICも[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")化が見受けられる。その代表例が[Visual Basic.NETや](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.Net "wikilink")[REALbasic](https://ja.wikipedia.org/wiki/REALbasic "wikilink")や[ActiveBasic](https://ja.wikipedia.org/wiki/ActiveBasic "wikilink")や[FreeBASIC](https://ja.wikipedia.org/wiki/FreeBASIC "wikilink")等で、四者とも既に完全なオブジェクト指向言語になっていると言える。

## 主なBASIC

### 現在のパソコンのBASIC

#### マイクロソフトBASIC・ならびにその類似系

  - [Visual Basic](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink") - マイクロソフト

      - [Visual Basic for Applications](https://ja.wikipedia.org/wiki/Visual_Basic_for_Applications "wikilink") (VBA)
      - [Visual Basic.NET](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.Net "wikilink")

  - [Small Basic](https://ja.wikipedia.org/wiki/Small_Basic "wikilink") - マイクロソフト

  - [99Basic](https://ja.wikipedia.org/wiki/99Basic "wikilink") （Windows用フリーウェア 国産）

  - [ActiveBasic](https://ja.wikipedia.org/wiki/ActiveBasic "wikilink") （Windows用フリーウェア 国産）

  - [BASIC/98](https://ja.wikipedia.org/wiki/BASIC/98 "wikilink") （Windows用 国産 [N88-BASIC](https://ja.wikipedia.org/wiki/N88-BASIC "wikilink")互換） - 有限会社電脳組

  - [Xojo](https://ja.wikipedia.org/wiki/Xojo "wikilink")（旧:[REALbasic](https://ja.wikipedia.org/wiki/REALbasic "wikilink")）（Windows・[Mac OS](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")・[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")）

  - （Visual Basicに似たコードでJRE上で動くソフトを開発するコンパイラ）

  - [XBLite](https://ja.wikipedia.org/wiki/XBLite "wikilink")

  - [Android-Basic](https://ja.wikipedia.org/wiki/Android-Basic "wikilink") （Android用）

  - [FreeBASIC](https://ja.wikipedia.org/wiki/FreeBASIC "wikilink")（[QuickBASIC](https://ja.wikipedia.org/wiki/QuickBASIC "wikilink")互換、コンパイラ型、GPL）（Windows・Linux・[DOSエクステンダ](https://ja.wikipedia.org/wiki/DOSエクステンダ "wikilink")・[Xbox](https://ja.wikipedia.org/wiki/Xbox_\(ゲーム機\) "wikilink")）

  - ([QuickBASIC](https://ja.wikipedia.org/wiki/QuickBASIC "wikilink")互換)

#### 独自系

  - [FutureBASIC](https://ja.wikipedia.org/wiki/FutureBASIC "wikilink") （Mac OS、構文はQuickBASIC互換 ）
  - [BCX](https://ja.wikipedia.org/wiki/BCX "wikilink")（GPLv2 + BCX例外ライセンスのオープンソースソフトウェア BASIC → C言語トランスレータでインラインC/[C++](https://ja.wikipedia.org/wiki/C++ "wikilink")およびアセンブリを扱えるなどの特徴を持つ）
  - [UBASIC](https://ja.wikipedia.org/wiki/UBASIC "wikilink") （DOS用フリーウェア 多倍長演算に特化）
  - [DarkBASIC](https://ja.wikipedia.org/wiki/DarkBASIC "wikilink") （ゲーム製作に特化したBASIC言語、Windows専用、特に3Dゲーム）
  - [GLBasic](https://ja.wikipedia.org/wiki/GLBasic "wikilink") （GCCコンパイラを内部で利用するマルチプラットフォーム開発環境）

#### Full BASIC系（規格準拠）

  - \- [公式サイト(外部リンク)](https://www.truebasic.com/)（Full BASIC規格の原型、[MS-DOS](https://ja.wikipedia.org/wiki/MS-DOS "wikilink")・Windows・Mac OS・UNIX、現在は英語版のみ、BASICを作った[ジョン・ジョージ・ケメニー](https://ja.wikipedia.org/wiki/ジョン・ジョージ・ケメニー "wikilink")とによって作られたBASIC）

  - [十進BASIC](https://ja.wikipedia.org/wiki/十進BASIC "wikilink")\[3\] （JIS Full BASICに準拠、Windows・Linux・Mac OS用フリーウェア、英語名Decimal BASIC）

  - [Ultra BASIC](https://ja.wikipedia.org/wiki/Ultra_BASIC "wikilink") - 株式会社[ラネクシー](https://ja.wikipedia.org/wiki/ラネクシー "wikilink")

#### 旧式構文系

  - [Chipmunk Basic](https://ja.wikipedia.org/wiki/Chipmunk_Basic "wikilink")（Windows・Mac OS・[UNIX](../Page/UNIX.md "wikilink")用フリーウェア、インタプリタのみ）

<!-- end list -->

  - [PC-BASIC](https://ja.wikipedia.org/wiki/PC-BASIC "wikilink") (外部リンク)http://www.pc-basic.org/ (Windows・Mac OS・Linux・UNIX・GPL系・GW BASIC互換エミュレート機能搭載型インタープリター)

### AndroidのBASIC

  - [Tiny BASIC v2](https://play.google.com/store/apps/details?id=org.dyndns.vivi.TinyBASIC2) タートルグラフィックスを備えた Android 用 BASIC インタプリタ
  - BASIC\! 別名rfo-basic <http://basic.amsstudio.jp/>

\[4\]

  - [X11-BASIC - Androidアプリ](http://applion.jp/android/app/net.sourceforge.x11basic/X11-BASIC)

### iPhone / iPadのBASIC

  - [Hand BASIC](http://applion.jp/iphone/app/394924289/) - CBM Flavor　
  - [BASIC-II](https://itunes.apple.com/jp/app/basic-ii/id581692436?mt=8)　

### ゲーム機などのBASIC

  - [ファミリーベーシック](https://ja.wikipedia.org/wiki/ファミリーベーシック "wikilink") (NS-HuBASIC)（[ファミコン](https://ja.wikipedia.org/wiki/ファミリーコンピュータ "wikilink")、[任天堂](../Page/任天堂.md "wikilink")・[シャープ](https://ja.wikipedia.org/wiki/シャープ "wikilink")・[ハドソン](https://ja.wikipedia.org/wiki/ハドソン "wikilink")共同開発）
  - [PCエンジン](https://ja.wikipedia.org/wiki/PCエンジン "wikilink")でべろBASIC（PCエンジン用開発ツール、[徳間書店インターメディア](https://ja.wikipedia.org/wiki/徳間書店インターメディア "wikilink")が販売、[ハドソン](https://ja.wikipedia.org/wiki/ハドソン "wikilink")・[日本電気ホームエレクトロニクス](https://ja.wikipedia.org/wiki/日本電気ホームエレクトロニクス "wikilink")開発）
  - [GAME BASIC for SEGASATURN](https://ja.wikipedia.org/wiki/GAME_BASIC_for_SEGASATURN "wikilink") （[セガサターン](https://ja.wikipedia.org/wiki/セガサターン "wikilink")、MSX-BASICライク）
  - [BASIC STUDIO](https://ja.wikipedia.org/wiki/BASIC_STUDIO "wikilink") （[PlayStation 2](https://ja.wikipedia.org/wiki/PlayStation_2 "wikilink")、[アートディンク](https://ja.wikipedia.org/wiki/アートディンク "wikilink")開発）
  - [プチコン](https://ja.wikipedia.org/wiki/プチコン "wikilink")・プチコンmkII (SmileBasic)（[ニンテンドーDSi](https://ja.wikipedia.org/wiki/ニンテンドーDSi "wikilink")/DSiLL・[ニンテンドー3DS](https://ja.wikipedia.org/wiki/ニンテンドー3DS "wikilink")・[Newニンテンドー3DS](https://ja.wikipedia.org/wiki/Newニンテンドー3DS "wikilink")、JOEDOWN・[スマイルブーム](https://ja.wikipedia.org/wiki/スマイルブーム "wikilink")・[ロケットスタジオ](https://ja.wikipedia.org/wiki/ロケットスタジオ "wikilink")共同開発）
      - [プチコン3号](https://ja.wikipedia.org/wiki/プチコン3号 "wikilink") （ニンテンドー3DS・Newニンテンドー3DS）
      - [プチコン4](https://ja.wikipedia.org/wiki/プチコン4 "wikilink") (ニンテンドーSwitch)

### その他のBASIC(過去のパソコンなど)

#### 独自系

  - [Apple 6K BASIC](https://ja.wikipedia.org/wiki/Apple_6K_BASIC "wikilink") （[アップルコンピュータ製](https://ja.wikipedia.org/wiki/アップル_\(企業\) "wikilink")、[スティーブ・ウォズニアック](https://ja.wikipedia.org/wiki/スティーブ・ウォズニアック "wikilink")独力による開発実装。[Apple I](https://ja.wikipedia.org/wiki/Apple_I "wikilink"), [Apple II用](https://ja.wikipedia.org/wiki/Apple_II "wikilink") 別名 [Integer BASIC](https://ja.wikipedia.org/wiki/:en:Integer_BASIC "wikilink")）
  - [G-BASIC](https://ja.wikipedia.org/wiki/G-BASIC "wikilink") （[トミー](https://ja.wikipedia.org/wiki/トミー_\(企業\) "wikilink")[ぴゅう太](https://ja.wikipedia.org/wiki/ぴゅう太 "wikilink")用BASIC、命令後を日本語に置き換えてある。同機には別売のBASIC 1もあり） ※同機とは関係ない、マイクロソフト製の同名のBASICがある
  - MW-BASIC （BASIC-09 [OS-9](https://ja.wikipedia.org/wiki/OS-9 "wikilink")用）
  - [BASIC-G](https://ja.wikipedia.org/wiki/BASIC-G "wikilink") （[ソードの](https://ja.wikipedia.org/wiki/東芝パソコンシステム "wikilink")[M5のBASIC](https://ja.wikipedia.org/wiki/M5_\(コンピュータ\) "wikilink")、整数型しか使えないが高速だった。同機には実数用の[BASIC-F](https://ja.wikipedia.org/wiki/BASIC-F "wikilink")もあり）
  - [Tiny BASIC](https://ja.wikipedia.org/wiki/Tiny_BASIC "wikilink") （黎明期の[マイコン用など](../Page/パーソナルコンピュータ.md "wikilink")）
  - [WICS](https://ja.wikipedia.org/wiki/WICS "wikilink") （MZ-80K及びMZ-80Bシリーズ用のBASICに極力似せた表記方法を採用した、インタープリタ兼コンパイラ 整数型プログラミング言語）
  - [C-BASIC](https://ja.wikipedia.org/wiki/C-BASIC "wikilink") （[カシオ](https://ja.wikipedia.org/wiki/カシオ計算機 "wikilink")[FPシリーズ用のBASICで](https://ja.wikipedia.org/wiki/FP-1000 "wikilink")10進演算による精度の高い計算を得意とした。8ビット用のC82-BASICと[16ビット](https://ja.wikipedia.org/wiki/16ビット "wikilink")用C86-BASICがある）
  - SHARP BASIC （[ポケコン用のBASIC](https://ja.wikipedia.org/wiki/ポケットコンピュータ "wikilink")）
  - [X-BASIC](https://ja.wikipedia.org/wiki/X-BASIC "wikilink") （[X68000](https://ja.wikipedia.org/wiki/X68000 "wikilink")の[C言語](../Page/C言語.md "wikilink")ライクなBASIC、ハドソン製。）

#### マイクロソフト系

  - （[Microsoft BASIC](https://ja.wikipedia.org/wiki/Microsoft_BASIC "wikilink")）
  - [Apple 10K BASIC](https://ja.wikipedia.org/wiki/Apple_10K_BASIC "wikilink") （アップルコンピュータ Apple II+以降）
  - BASCOM （CP/M用BASICコンパイラ）
  - [F-BASIC](https://ja.wikipedia.org/wiki/F-BASIC "wikilink") （[FMシリーズのBASIC](https://ja.wikipedia.org/wiki/富士通#パーソナルコンピュータ "wikilink")、[富士通](../Page/富士通.md "wikilink")製）
  - [M-BASIC](https://ja.wikipedia.org/wiki/M-BASIC "wikilink") （[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")用のBASIC）
  - [MSX-BASIC](https://ja.wikipedia.org/wiki/MSX-BASIC "wikilink") （[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")用のマイクロソフトBASIC、スプライト機能などを拡張、N88などより原型に近い）
  - [N-BASIC](https://ja.wikipedia.org/wiki/N-BASIC "wikilink") （[PC-8000シリーズ](https://ja.wikipedia.org/wiki/PC-8000シリーズ "wikilink")などのBASIC）
  - [N80-BASIC](https://ja.wikipedia.org/wiki/N80-BASIC "wikilink") （[PC-8001mkIIなどのBASIC](https://ja.wikipedia.org/wiki/PC-8000シリーズ "wikilink")）
  - [N88-BASIC](https://ja.wikipedia.org/wiki/N88-BASIC "wikilink") （[PC-8800シリーズ](https://ja.wikipedia.org/wiki/PC-8800シリーズ "wikilink")（マイクロソフト製）、[PC-9800シリーズ](https://ja.wikipedia.org/wiki/PC-9800シリーズ "wikilink")（日本電気製）のBASIC、PC-9800シリーズ用は別途コンパイラもあり）
  - [N60-BASIC](https://ja.wikipedia.org/wiki/N60-BASIC "wikilink")、[N60m-BASIC](https://ja.wikipedia.org/wiki/N60m-BASIC "wikilink")、[N66-BASIC](https://ja.wikipedia.org/wiki/N66-BASIC "wikilink")、[N66SR-BASIC](https://ja.wikipedia.org/wiki/N66SR-BASIC "wikilink") （[PC-6000シリーズ](https://ja.wikipedia.org/wiki/PC-6000シリーズ "wikilink")、[PC-6600シリーズ](https://ja.wikipedia.org/wiki/PC-6600シリーズ "wikilink")のBASIC）
  - [N100 BASIC](https://ja.wikipedia.org/wiki/N100_BASIC "wikilink") （[PC-100](https://ja.wikipedia.org/wiki/PC-100 "wikilink")のBASIC）
  - [N82-BASIC](https://ja.wikipedia.org/wiki/N82-BASIC "wikilink") （[PC-8201のBASIC](https://ja.wikipedia.org/wiki/PC-8200シリーズ "wikilink")）
  - [Hu-BASIC](https://ja.wikipedia.org/wiki/Hu-BASIC "wikilink") （[ハドソン](https://ja.wikipedia.org/wiki/ハドソン "wikilink")製のマイクロソフト系命令セットのBASIC。固定のシステムをROMで持たない[MZ-80](https://ja.wikipedia.org/wiki/MZ-80 "wikilink")Kで利用できるよう市販されたが、後に[MZ-700](https://ja.wikipedia.org/wiki/MZ-700 "wikilink")や[X1/turbo/turboZシリーズでは標準添付のシステムとなり](https://ja.wikipedia.org/wiki/X1_\(コンピュータ\) "wikilink")、X1では名前を変えつつ標準のシステムとして最終機まで継承された。）
  - [BASIC-M25](https://ja.wikipedia.org/wiki/BASIC-M25 "wikilink") （シャープ[MZ-2500](https://ja.wikipedia.org/wiki/MZ-2500 "wikilink")用の実装。コピーライトはシャープとなっているが、ハドソン製でもマイクロソフト製でも無い。日本語のラベルや、インデントのタブコード化、常駐プログラムとの併用など本体に合わせ高機能なBASICとなっている。）
  - [BASIC-M28](https://ja.wikipedia.org/wiki/BASIC-M28 "wikilink") （シャープ[MZ-2861](https://ja.wikipedia.org/wiki/MZ-2861 "wikilink")）
  - [IchigoJam BASIC](https://ja.wikipedia.org/wiki/IchigoJam#プログラミング言語 "wikilink") (IchigoJam用の実装。MSXの影響を強く受けているため、独自拡張を含むもののMSX-BASICのサブセットの様な命令セットとなっている。）
  - [QBasic](https://ja.wikipedia.org/wiki/QBasic "wikilink") （QuickBASICの簡易版、[Windows 95](https://ja.wikipedia.org/wiki/Microsoft_Windows_95 "wikilink") / [98の](https://ja.wikipedia.org/wiki/Microsoft_Windows_98 "wikilink")[CD-ROM](../Page/CD-ROM.md "wikilink")に英語版が付属）
  - [QuickBASIC](https://ja.wikipedia.org/wiki/QuickBASIC "wikilink") （Visual Basicの原型となった構造化BASIC）
  - [Microsoft BASIC Professional Development System](https://ja.wikipedia.org/wiki/Microsoft_BASIC_Professional_Development_System "wikilink") （QuickBASICの進化形で、標準でISAMデータベースが構築でき、MS-MASM、MS-C、Quick C、MS-FORTRAN等とのミックスド・ランゲージ開発が可能な、プロユースの構造化BASIC）
  - SONY BASIC（ソニー[SMC-70](https://ja.wikipedia.org/wiki/SMC-70 "wikilink")、[SMC-777](https://ja.wikipedia.org/wiki/SMC-777 "wikilink")/Cに搭載されたBASICインタープリタ、マイクロソフト系命令セットを備えているが、直接の関係はなく、ビー・ユー・ジー社（現[ビー・ユー・ジーDMG森精機](https://ja.wikipedia.org/wiki/ビー・ユー・ジーDMG森精機 "wikilink")株式会社）が開発した\[5\]。）

<!-- end list -->

  -
    これらは命令セットの仕様が共通なだけで、必ずしもマイクロソフト製というわけではない。

#### コモドール系

  - [S-BASIC](https://ja.wikipedia.org/wiki/S-BASIC "wikilink") （[MZシリーズのBASIC](https://ja.wikipedia.org/wiki/MZ_\(コンピュータ\) "wikilink")、シャープ製）
  - [BASIC-S25](https://ja.wikipedia.org/wiki/BASIC-S25 "wikilink") （シャープ[MZ-2500](https://ja.wikipedia.org/wiki/MZ-2500 "wikilink")）
  - [BASIC LEVEL II他](https://ja.wikipedia.org/wiki/SC-3000 "wikilink") (SEGAのSC-3000/SG-1000等のためのBASIC)

<!-- end list -->

  -
    [MZ-80K](https://ja.wikipedia.org/wiki/MZ-80K "wikilink")が[PET 2001の影響を強く受けていることもあり](https://ja.wikipedia.org/wiki/PET_2001 "wikilink")、シャープ純正のBASICの命令セットは互換性のため後継製品もそれに準拠して独自拡張した物となっている。

#### Web系

  - [Quite BASIC(外部リンク)](http://www.quitebasic.com/) ブラウザ上でBASICコードを書いてWeb上で実行できるサービス

## 脚注

<references />

## 関連書籍

  - マイコンBASIC互換表 [CQ出版社](https://ja.wikipedia.org/wiki/CQ出版社 "wikilink")
  - Kemeny, John G. & Kurtz, Thomas E. (1985). *Back to BASIC: The History, Corruption and Future of the Language*. Addison-Wesley Publishing Company, Inc. ISBN 0-201-13433-0.
      - 松田健生訳、市川新解説（1990）『バック・トゥ・BASIC 開発者が語る言語の歴史と設計思想』[啓学出版](https://ja.wikipedia.org/wiki/啓学出版 "wikilink")、ISBN 4-7665-1074-7

[Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink") [Category:パソコンの歴史](https://ja.wikipedia.org/wiki/Category:パソコンの歴史 "wikilink") [Category:教育用プログラミング言語](https://ja.wikipedia.org/wiki/Category:教育用プログラミング言語 "wikilink")

1.  [:en:Edsger_W._Dijkstra\#How_do_we_tell_truths_that_might_hurt.3F_.281975.29](https://ja.wikipedia.org/wiki/:en:Edsger_W._Dijkstra#How_do_we_tell_truths_that_might_hurt.3F_.281975.29 "wikilink")
2.  英語で「[走り屋](https://ja.wikipedia.org/wiki/走り屋 "wikilink")による競走」を意味する [Street racing](https://ja.wikipedia.org/wiki/:en:Street_racing "wikilink") といったような street の語義を意識して使っている。
3.  [十進BASICのホームページ](http://hp.vector.co.jp/authors/VA008683/index.htm)
4.  AndroidでBASIC！で遊ぼう［改訂版］kindle 2016年11月20日　発行 著者：BASIC！友の会 発行：BASIC！友の会出版
5.