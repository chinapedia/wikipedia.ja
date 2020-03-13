> この記事は[Information Processing Language](https://ja.wikipedia.org/wiki/Information_Processing_Language)から翻訳されています。


**Information Processing Language**（**IPL**)とは、1956年ごろから[ランド研究所](../Page/ランド研究所.md "wikilink")および[カーネギー工科大学にて](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")[アレン・ニューウェル](../Page/アレン・ニューウェル.md "wikilink")、[クリフ・ショー](https://ja.wikipedia.org/wiki/クリフ・ショー "wikilink")、[ハーバート・サイモン](../Page/ハーバート・サイモン.md "wikilink")が開発した[プログラミング言語](../Page/プログラミング言語.md "wikilink")。ニューウェルは言語仕様設計と同時にアプリケーションのプログラミングも行い、ショーはシステムプログラミング、サイモンはアプリケーションのプログラマとしてもユーザーとしても活動した。

一般問題解決のための各種プログラミング要素を備えている。例えば、リスト、連想(association)、[スキーマ](https://ja.wikipedia.org/wiki/スキーマ "wikilink")（フレーム）、[動的メモリ確保](../Page/動的メモリ確保.md "wikilink")、[データ型](../Page/データ型.md "wikilink")、[再帰呼び出し](https://ja.wikipedia.org/wiki/再帰呼び出し "wikilink")、連想探索(associative retrieval)、引数としての関数、[ストリーム](../Page/ストリーム_\(プログラミング\).md "wikilink")、協調型マルチタスク（[ノンプリエンプティブ・マルチタスクのこと](../Page/マルチタスク.md "wikilink")）などである。IPLはアセンブリ言語のスタイルだったが、リスト処理の概念を開拓した。

## 言語仕様

IPLは次のような要素を持つ。

1.  シンボル群。全てのシンボルはアドレスおよび名前付きセルである。後の言語のシンボルとは異なり、シンボルは1文字とそれに続く番号で構成され、H1, A29, 9-7, 9-100 のように書かれる。
    1.  セル名が1つの英文字で始まる場合、*regional* であり、絶対アドレスを表す。
    2.  セル名が "9-" で始まる場合、*local* であり、単一のリスト内でのみ意味を持つ。あるリスト内の 9-1 は、別のリスト内の 9-1 とは別物である。
    3.  他のシンボル（例えば番号のみ）は *internal* である。
2.  セル群。リストはそれぞれ相互に参照を持つ複数のセルで構築される。セルにはいくつかのフィールドがある。
    1.  P は3ビットのフィールドで、そのセルを命令として実行する際の命令コードとして使われる。セルがデータの場合は未使用である。
    2.  Q は3値のフィールドで、そのセルが命令として使われる場合は間接参照に使われ、セルがデータの場合は未使用である。
    3.  SYMB はそのセルの値として使われるシンボルである。
3.  プリミティブプロセス群。現代の言語ではプリミティブ関数と呼ばれるものである。

IPLの主要なデータ構造はリストだが、多くの言語でのリストよりも複雑な構造を持っている。リストは実行も可能な一連のリンクされたシンボルから成り、それに加えて *description list* と呼ばれる属性名と値が交互に並んだリストが付属する。IPLには属性名を指定して対応する値にアクセスしたり値を変更したりするプリミティブがある。description list には（9-1 のような形式の）ローカル名が与えられる。下表は、S4とS5というシンボルを持つL1というリストと、それに付属するA1という属性にV1という値が対応しA2という属性にV2という値が対応している9-1という description list を示している。LINKが0となっているのは、リストの終端を意味する。100や101といったセル名は自動的に生成された内部シンボルであり無意味である。これらのセルはメモリ上ばらばらに存在する。L1は唯一の regional なシンボルなので、特別な場所に置かれグローバルに参照可能である。

<code>

| 名前  | SYMB | LINK |
| --- | ---- | ---- |
| L1  | 9-1  | 100  |
| 100 | S4   | 101  |
| 101 | S5   | 0    |
| 9-1 | 0    | 200  |
| 200 | A1   | 201  |
| 201 | V1   | 202  |
| 202 | A2   | 203  |
| 203 | V2   | 0    |

**IPL-V のリスト構造例**

</code>

IPLはリストを操作できる[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")である。特別な用途のレジスタとして使われるセルが存在する。例えばH1はプログラムカウンタである。H1のSYMBフィールドは現在の命令の名前となっている。しかし、H1はリストとして解釈される。H1のLINKフィールドは今風に言えば[コールスタック](https://ja.wikipedia.org/wiki/コールスタック "wikilink")のトップへのポインタである。例えば、[サブルーチン](../Page/サブルーチン.md "wikilink")呼び出しではH1のSYMBをそのスタックにプッシュする。

H2はフリーリストである。[プロシージャ](https://ja.wikipedia.org/wiki/プロシージャ "wikilink")がメモリを確保したい場合はH2からセルを獲得する。逆にプロシージャが完了したらメモリをH2に置く。関数に入る際、引数リストはH0にある。関数から抜ける際には結果をH0に置く。多くのプロシージャは成功か失敗かを示す[ブーリアン型](../Page/ブーリアン型.md "wikilink")の結果を返すが、それをH5に置く。W0-W9という10個のセルは一時格納場所としてどこからでも使える。それらのセルに値をセーブしリストアする際にはプロシージャは「道徳的に束縛されている」（CACMの論文での言葉）。

Pフィールドでは8種類の命令を表せる。サブルーチン呼び出し、SからH0へのプッシュ/ポップ、SにあるシンボルとSに付属しているリストの間でプッシュ/ポップ、Sへの値のコピー、条件分岐といった命令がある。ここで、Sは命令のターゲットを意味する。SはQ=0ならSUMBフィールドの値を意味し。Q=1ならSYMBに名前があるセル内のシンボル、Q=2ならSYMBに名前があるセル内のシンボルの示すセル内のシンボルを意味する。つまり、Qはセルの間接参照のレベルを示している。条件分岐以外の命令では、次に実行すべき命令はセルのLINKフィールドが示している。

IPLには約150の基本処理のライブラリがある。例えば次のような処理が実装されている。

  - シンボル同士が等しいかどうかの判定
  - リストの属性を探す、セットする、消去する。
  - リスト内の次のシンボルを求める。リストにシンボルを挿入する。リスト全体の消去、コピー。
  - 算術演算（シンボル名を対象とする）。
  - シンボルの操作。例えばシンボルが整数を表しているか否かの判定、シンボルをローカルなものにするなど。
  - I/O操作
  - 関数型言語のイテレータやフィルターに相当する "generator" がある。例えば数値のリストに対して個々のセルについて二乗を計算して新たなリストを作るといったことができる。

## 歴史

IPLの最初の利用例は、『[プリンキピア・マテマティカ](https://ja.wikipedia.org/wiki/プリンキピア・マテマティカ "wikilink")』（[バートランド・ラッセル](../Page/バートランド・ラッセル.md "wikilink")と[アルフレッド・ノース・ホワイトヘッド](../Page/アルフレッド・ノース・ホワイトヘッド.md "wikilink")の労作）の中の定理を[計算によって証明するデモンストレーションであった](../Page/自動定理証明.md "wikilink")。サイモンの自伝 *Models of My Life* によると、このアプリケーションは人手によるシミュレーションで最初に試されたという。彼の子供たちを演算装置に見立て、各人にプログラムの状態変数を保持するレジスタの役目をするカードを持たせたという。

IPL は開発者自身の初期の[人工知能](../Page/人工知能.md "wikilink")プログラムの実装に使われた。[Logic Theorist](https://ja.wikipedia.org/wiki/Logic_Theorist "wikilink")（1956年）、[GPS](../Page/General_Problem_Solver.md "wikilink")（1957年）、[コンピュータチェス](../Page/コンピュータチェス.md "wikilink")プログラム NSS（1958年）などである。

IPL にはいくつかのバージョンがある。IPL-I（実装されず）、IPL-II（1957年、[JOHNNIAC向け](https://ja.wikipedia.org/wiki/:en:JOHNNIAC "wikilink")）、IPL-III（実装はされた）、IPL-IV、IPL-V（1958年、[IBM 650](../Page/IBM_650.md "wikilink")、[IBM 704](../Page/IBM_704.md "wikilink")、[IBM 7090など広く実装された](../Page/IBM_7090.md "wikilink")）、IPL-VI が知られている。

しかし、この言語はすぐに[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")に取って代わられた。LISPはほぼ同等の機能を持ちながら文法が単純で[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")機能を備えていた。

## 後のプログラミング言語への影響

IPLは次のようなプログラミング言語機能を初めて導入した。

  - [リスト操作](../Page/リスト_\(抽象データ型\).md "wikilink") - ただし、リストの要素はアトムのみで、リストのリストは作れない。
  - 属性リスト - ただし、他のリストに付属させる形である。
  - [高階関数](../Page/高階関数.md "wikilink") - もともとアセンブリ言語なので、関数呼び出しの際にはそのアドレスを計算する。IPLはこのアセンブリ言語の特性を一般化した。
  - シンボルによる計算 - ただし、シンボルは「文字＋番号」という形式であり、普通の単語は使えない。
  - 仮想機械

これら機能の多くは一般化され、洗練されてLISPに導入された\[1\]。そして、LISPから後続の様々なプログラミング言語にも受け継がれた。

## 関連著作

  - Newell, A. and F.C. Shaw. "Programming the Logic Theory Machine." Feb. 1957. Proceedings of the Western Joint Computer Conference, pp. 230-240.
  - Newell, Allen, and Fred M. Tonge. 1960. "An Introduction to Information Processing Language V." CACM 3(4): 205-211.
  - Newell, Allen. 1964. *Information Processing Language-V Manual; Second Edition*. Rand Corporation \[Allen Newell\], Englewood Cliffs, NJ: Prentice-Hall.
  - Samuel, Arthur L.: Programming Computers to Play Games. In: Advances in Computers, Vol. 1, 1960, pp 165-192 (esp.: 171-175).

## 脚注

## 参考文献

  - [Allen Newell](http://stills.nap.edu/readingroom/books/biomems/anewell.html), ハーバート・サイモン著の伝記。全米科学アカデミー - IPLに関する短い記述を含む
  - [History of Programming Languages: IPL](http://hopl.murdoch.edu.au/showlanguage.prx?exp=13&language=IPL)
  - [Information Processing Language](http://foldoc.org/Information+Processing+Language), [FOLDOC](../Page/FOLDOC.md "wikilink")
  - [1](http://bitsavers.org/pdf/rand/ipl/) IPL documents from BitSavers.
  - [2](http://www-formal.stanford.edu/jmc/history/lisp/node2.html) influence of IPL on LISP.

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:人工知能の歴史](https://ja.wikipedia.org/wiki/Category:人工知能の歴史 "wikilink")

1.  [John McCarthy (1979) *History of Lisp* "LISP prehistory - Summer 1956 through Summer 1958."](http://www-formal.stanford.edu/jmc/history/lisp/node2.html)